---
title: Čekijos finansinio registravimo tarnybos integravimo pavyzdys
description: Šiame straipsnyje pateikta Čekijos Respublika finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: d255b03242a4cb7a72cef1e8e6fab901ecf953e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910503"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Čekijos finansinio registravimo tarnybos integravimo pavyzdys

[!include[banner](../includes/banner.md)]

Šiame straipsnyje pateikta Čekijos Respublika finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Siekiant patenkinti vietinius finansinius reikalavimus grynųjų pinigų registrams Čekijos Respublika, Dynamics 365 Commerce Čekijos respublika turi pavyzdinį kasos aparato (EKA) integravimą su išorine finansinio registravimo tarnyba. Pavyzdys išplečia finansinio [integravimo funkciją](fiscal-integration-for-retail-channel.md). Jis remiasi [EFR (elektroninio finansinio registro)](https://efsta.org/sicherheitsloesungen/)[sprendimu iš EFSTA](https://efsta.org/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR tarnyba užtikrina elektroninę pardavimo registraciją (EET – Elektro²² evidence tržeb), t. y. pardavimų duomenų perdavimas mokesčių institucijų fiskalinei žiniatinklio tarnybai.

EFR tarnyba turi būti laikoma "Commerce Hardware" stotis arba atskirame kompiuteryje, kurį galima prijungti prie "Hardware" stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš EFSTA. Norėdami gauti informacijos apie tai, kaip gauti EFR sprendimą ir jį valdyti, susisiekite su [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Scenarijai

Šiuos scenarijus apima Čekijos finansinio registravimo tarnybos integravimo pavyzdys.

- Grynųjų pinigų operacijų registravimas finansinio registravimo tarnybose.

    - Siųsti išsamius operacijos duomenis į finansinio registravimo tarnybą. Šie duomenys apima pardavimo eilutės informaciją ir informaciją apie nuolaidas, mokėjimus ir mokesčius. Finansinio registravimo tarnyba toliau siunčia duomenis į mokesčių inspekcijos žiniatinklio tarnybą ir gauna patvirtinimą iš jo, kuriame įtrauktas operacijos fiskalinio identifikavimo kodas.
    - Perimti iždo registracijos tarnybos atsakymą. Šis atsakymas apima finansinius duomenis, pvz., finansinio identifikavimo kodą, operacijos saugos kodą ir pan.
    - Spausdinti kvite užregistruotos operacijos finansinius duomenis.

- Dovanų kortelių operacijų ir kliento depozitų registravimas finansinio registravimo tarnybose.

    - Išduoti arba įtraukti pinigus į dovanų kortelę.
    - Registruoti kliento sąskaitos depozitą.
    - Sukurkite kliento užsakymą ir užregistruokite užsakymo depozitą.
    - Redaguoti kliento užsakymą ir nepaisyti užsakymo įmokos.
    - Atšaukti kliento užsakymą ir grąžinti užsakymo depozitą.

- Klaidos tvarkymą, pvz., šias pasirinktis.

    - Pakartokite fiskalinę registraciją, jei galima kartoti, pvz., jei fiskalinių registracijų tarnyba negalima, neparuošta arba neatsako.
    - Atidėti finansinio registravimo datą.
    - Praleisti ataskaitinį registravimą arba pažymėti operaciją kaip užregistruotą ir įtraukti informacijos kodus, kad būtų fiksuojama trikties priežastis ir papildoma informacija.
    - Patikrinkite finansinio registravimo tarnybos pasiekiamumą prieš atidarę naują pardavimo operaciją arba kai pardavimo operacija baigiama.

### <a name="gift-cards"></a>Dovanų kortelės

Finansinio registravimo tarnybos integravimo pavyzdys vykdo šias taisykles, susijusias su dovanų kortelėmis.

- Pardavimo eilutės, susijusios *su išdavimo dovanų* *kortele* arba pardavimo operacijose pridėtomis dovanų kortelės operacijomis, yra pažymimos specialiu atributu, kai operacija užregistruojama finansinio registravimo tarnybose.
- Mokėjimas dovanų kortele laikomas įprastu mokėjimu ir pažymėtas specialiu atributu, kai operacija užregistruota finansinio registravimo tarnybose.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Kliento sąskaitos depozitai ir kliento užsakymo depozitai

Finansinio registravimo tarnybos integravimo pavyzdys vykdo šias taisykles, susijusias su kliento sąskaitos depozitais ir kliento užsakymo depozitais.

- Operacija, susijusi su kliento sąskaitos depozitu arba kliento užsakymo depozitu, užregistruota finansinio registravimo tarnybose kaip viena eilutės operacija ir pažymėta specialiu atributu. Šioje eilutėje nurodyta depozito PVM grupė.
- Kai sukuriamas kliento užsakymas, t. y. kliento užsakymas, kuriame yra produktai, kuriuos klientas gali perkelti iš parduotuvės, ir produktai, kurie bus paimti arba išsiųsti vėliau, finansinio registravimo tarnybos užregistruotoje operacijoje yra eilutė už produktus, kurie yra vykdomi, ir užsakymo depozito eilutė.
- Mokėjimas iš kliento sąskaitos laikomas įprastu mokėjimu ir pažymimas specialiu atributu, kai operacija užregistruojama finansinio registravimo tarnybose.
- Kliento užsakymo depozito suma, taikoma kliento užsakymo paėmimo operacijai, laikoma įprastu mokėjimu ir pažymėta specialiu atributu, kai operacija užregistruojama finansinio registravimo tarnybose.

### <a name="offline-registration"></a>Registracija ne tinkle

Jei fiskalinių registracijų paslaugai nepavyksta perduoti operacijos duomenų į mokesčių institucijų fiskalinę žiniatinklio tarnybą (pvz., dėl atsakymo skirtasis laikas) ir gauti patvirtinimą iš žiniatinklio tarnybos (t. y. operacijos fiskalinio identifikavimo kodo), ji sugeneruoja vietinį operacijos parašą ir į atsakymą įtraukia jį bei specialų klaidos kodą. Finansinio registravimo tarnyba atstatius tinklo ryšį atstato operacijas originalia tvarka fone.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

Finansinio registravimo tarnyba palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainą. Todėl parduotuvių **ir klientų parinktis** Kaina su PVM turi **būti** nustatyta kaip Taip.

## <a name="set-up-commerce-for-the-czech-republic"></a>Nustatyti Čekijos komercijos prekybą

Šiame skyriuje aprašomi Komercijos parametrai, kurie yra specifiniai ir rekomenduojami Čekijos Respublikai. Daugiau informacijos ieškokite " [Commerce" pagrindinis puslapis](../index.md).

Norėdami naudoti Čekiją specifinę funkciją, turite nurodyti šiuos parametrus.

- Pirminiame juridinio subjekto adrese nustatykite šalies **/regiono lauką** **CZE** (Čekijos Respublika).
- Kiekvienos Čekijos Respublika, kuri yra Čekijos Respublikai, **EKA funkcijų profilyje nustatykite ISO** **kodo lauką CZ** (Čekijos Respublika).

Taip pat turite nurodyti šiuos Čekijos parametrus. Atkreipkite dėmesį, kad užbaigę nustatymą turite vykdyti atitinkamas paskirstymo užduotis.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Nustatyti PVM pagal Čekijos Respublika reikalavimus


Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM priemones, ieškokite [PVM peržiūra.](../../finance/general-ledger/indirect-taxes-overview.md)

### <a name="set-up-stores"></a>Parduotuvių nustatykite

**Puslapyje Visos parduotuvės** atnaujinkite parduotuvės informaciją. Tiksliau nustatykite šiuos parametrus.

- Lauke PVM **grupė nurodykite** PVM grupę, kurią reikia naudoti pardavimams numatytojam klientui.
- Nustatykite **parinktį Kainos su PVM** kaip **Taip**.
- Nustatykite **įmonės** pavadinimą lauke Pavadinimas. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės pavadinimas. Taip pat galite įtraukti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti mokesčio **identifikavimo numerio (TIN)** lauką kaip įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės identifikavimo numeris. Taip pat galite prie pardavimo kvito maketo pridėti įmonės identifikavimo numerį kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų nustatymas

Nustatyti EKA funkcijų šablonus.

- Kvitų **numeravimo** "FastTab" nustatykite kvitų **numeravimą**, sukurdami arba atnaujindami pardavimo, **pardavimo užsakymo** ir grąžinimo **kvitų** operacijų tipų įrašus.

### <a name="set-up-registration-numbers"></a>Nustatyti registracijos numerius

1. Eikite į **organizacijos administravimo \> visuotinės adresų knygelės \> registracijos tipų \> registracijos tipus**. Sukurkite naują registracijos tipą. Nurodykite **CZE** **·** (Čekijos Respublika) lauką Šalis/regionas ir apribokite jį organizacija.
2. Eikite į **organizacijos administravimo \> visuotinės adresų knygelės \> registracijos tipų \> registracijos kategorijas**. Kurti naują registracijos kategoriją. Pasirinkite registracijos tipą iš ankstesnio veiksmo ir nustatykite registracijos **kategoriją kaip** verslo **patalpos ID**.
3. Eikite į **Organizacijos valdymas \> Organizacijos \> Valdymo vienetai**. Kiekvienai Parduotuvei, esanei Čekijos Respublikai, pasirinkite su parduotuve susijusį vienetą. Adreso **"** FastTab" išplėskite išplečiamąjį **sąrašą** Daugiau pasirinkčių ir pasirinkite **Papildoma**. 
4. Atidarytame puslapyje **Tvarkyti adresus** turite nurodyti šiuos parametrus.

    - Adreso **"** FastTab" lauke **Šalis/regionas** nustatykite **CZE**.
    - **Registravimo ID** "FastTab" sukurkite naują įrašą. Pasirinkite anksčiau sukurtą registracijos tipą ir nustatykite registracijos numerį.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos teksto **puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atkreipkite dėmesį **, kad** lentelėje **pateiktos kalbos ID,** **teksto ID** ir teksto vertės yra tik pavyzdžiai. Juos galite pakeisti, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas **teksto ID** vertės turi būti unikalios ir turi būti lygios arba didesnės nei 900001.

Įtraukite šias EKA žymes į kalbos **teksto** EKA **skyrių** iš lentelės:

| Kalbos ID | Teksto ID | Tekstas                   |
|-------------|---------|------------------------|
| lt       | 900001  | ID klientos sąs. / pokladny |
| lt       | 900002  | B SD                    |
| lt       | 900003  | P SG                    |
| lt       | 900004  | FIK                    |
| lt       | 900005  | Informacija                   |
| lt       | 900006  | Sekos numeris        |

Pasirinktinių **laukų puslapyje** pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad antraštės teksto ID** reikšmės turi **atitikti teksto ID** vertes, kurias nurodėte kalbos **teksto** puslapyje:

| Vardas                 | Tipas    | Vaizdo aprašo teksto ID |
|----------------------|---------|-----------------|
| TLT                  | Gavimas | 900001          |
| SEC                  | Gavimas | 900002          |
| ŽENKLAS                 | Gavimas | 900003          |
| FISKALINĖS               | Gavimas | 900004          |
| INFORMACIJA                 | Gavimas | 900005          |
| IŠTISINIS NUMERAVIMAS     | Gavimas | 900006          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kurie išvardyti ankstesnėje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Kiekvieno reikiamo kvito formato atveju pakeiskite lauko Spausdinti veikimo būdą **vertę** į **Visada spausdinti**.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

- **Antraštė:** pridėkite šiuos laukus.

    - **Parduotuvės pavadinimas** ir **mokesčio ID**: šie laukai naudojami kvituose spausdinant įmonės pavadinimą ir tapatybės numerį. Taip pat galite įtraukti įmonės pavadinimą ir tapatybės numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės adresas**, **data**, **laikas 24 val**., **kvito numeris** ir **registro numeris**.
    - **Eilės numeris**: šis laukas identifikuoja grynųjų pinigų operacijos numerį finansinio registravimo tarnybose.

- **Eilutės:** įtraukite šiuos laukus.

    - **Prekės pavadinimas**
    - **Kiekis**
    - **Bendra kaina su mokesčiu**

- **Poraštė:** įtraukite šiuos laukus.

    - Mokėjimo laukus, kad būtų išspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, į vieną maketo **eilutę įtraukite** **laukus** Mokėjimo priemonės pavadinimas ir Mokėjimo priemonės suma.
    - **ID spausdinoovny/pokladny**: šiame lauke spausdinami verslo patalpų ir grynųjų pinigų registro identifikatoriai.
    - **BVZ**:: šiame lauke spausdinamas mokesčių mokėtojo saugos kodas, priskirtas finansinio registravimo tarnybos.
    - **FIK**: šiame lauke spausdinamas operacijos, kurią, sėkmingai registruojant tinkle, žiniatinklio tarnyba paskiria mokesčių inspekcijos, finansinis identifikavimo kodas.
    - **PVZ**.: šiame lauke spausdinamas mokesčių mokėtojo parašo kodas, kurį sugeneravo finansinio registravimo tarnyba atjungties registracijos atveju.
    - **Informacija**: šiame lauke spausdinami papildomi duomenys iš finansinių registracijų tarnybos.

Daugiau informacijos apie tai, kaip dirbti su kvitų formatais, ieškokite [Gavimo kvitų formatų nustatymas ir kūrimas](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Nustatyti Čekijos finansų integravimą

Čekijos finansinio registravimo tarnybos integravimo pavyzdys remiasi finansinio [integravimo funkcija ir](fiscal-integration-for-retail-channel.md) yra Mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ FiscalIntegration\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke, kuris yra sprendimų saugykloje (pvz., [pavyzdys, esantis release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas, kuris yra "Commerce Runtime (CRT) plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją programavimo virtualiojoje kompiuteryje (VM) ciklo Microsoft Dynamics tarnybose (LCS). Daugiau informacijos ieškokite Čekijos [Respublika (senesnės veiklos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-cze-fi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite finansinio registravimo procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Be to, pateikite pastabą apie finansinio registravimo proceso parametrus, bvz [., šios finansinio registravimo tarnybos integravimo pavyzdį](#set-up-the-registration-process).
1. [Nustatyti klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinkite neautomatinį atidėtos finansinio registravimo vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatyti registravimo procesą

Norėdami įjungti registravimo procesą, atlikite šiuos veiksmus norėdami nustatyti "Commerce Headquarters". Daugiau informacijos rasite "Commerce [" kanalų finansinio integravimo nustatykite](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųsti finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus:

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK/programos versiją (pvz., **[paleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> Efr**.
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą konfigūracijos faile Configurations **DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml (pvz \>., failas,** skirtas išleisti/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)
    1. Atsisiųskite finansinio jungties konfigūracijos **failą \>\> konfigūracijos failu konfigūracijos jungčių ConnectorEFRSample.xml** (pvz., [paleidimo / 9.33 failas](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra toliau esančiuuose "Retail" SDK, esantis LCS programuotojo VM, aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk\\ SampleExtensions CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\\\ konfigūracijos\\ DocumentProviderFiscalEFRSampleCzech.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ extension.EFRSample\\ Configuration\\ ConnectorEFRSample.xml
    > 
    > Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite pasirinktį **Įgalinti finansų integravimą** kaip **Taip**.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymą "Fiscal integration \> Fiscal"** dokumentų teikėjai ir įkelkite anksčiau atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce Channel" \> nustatymą "Fiscal integration \> Fiscal \>" jungtis ir įkelkite anksčiau atsisiųstą "Fiscal** Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" funkcinius profilius**. Sukurti naują jungties funkcinį profilį. Pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį. Pagal reikia [atnaujinti duomenų susiejimo](#default-data-mapping) parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**. Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją atnaujinkite](#fiscal-connector-settings) jungties parametrus.
1. Eikite į " **Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" jungties grupes**. Sukurkite naują anksčiau sukurto jungties funkcinių profilių finansinių jungčių grupę.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" registracijos procesus**. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso "** FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotiu, prie kurios bus prijungtas fiskalinis spausdintuvas. **"FastTab" Iždo išoriniuose** įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
1. Atidarykite paskirstymo grafiką (**"Retail and Commerce Retail ir Commerce \> IT \> Distribution"** grafiką) **ir pasirinkite užduotis 1070** **ir 1090**, kad duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas –** mokesčio procentų verčių, kurios nustatytos PVM kodams, susiejimas su atributo TaxG **(mokesčių grupė)** vertėmis užklausose, kurios siunčiamos į fiskalinę tarnybą. Čia yra numatytasis susiejimas:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM mokesčių grupę, kurią palaiko EFR finansinio registravimo tarnyba. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Čekijos Respublika, ieškokite [EFR nuorodoje](https://public.efsta.net/efr/).

- **Numatytosios PVM grupės** susiejimas – bet kurios PVM sumos, kurių negalima susieti su viena iš iš anksto nustatytų PVM grupių, bus priskiriamos numatytai (pagrindinei) PVM grupei. Čia yra numatytasis susiejimas:

    ```
    A
    ```

- **Depozito PVM grupės susiejimas** – kliento įmokos sumos ir kliento užsakymo depozito sumos bus priskiriamos depozito PVM grupei. Čia yra numatytasis susiejimas:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis** laikas milisekundiais, kurį fiskalinė jungtis lauks atsakymo iš fiskalinių registracijų tarnybos.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite Čekijos [Respublika (senesnės veiklos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-cze-fi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą Dynamics365Commerce.Solutions **FiscalIntegration\\ EFR.sln\\ ir sukurkite\\ jį.**
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** **aplanke Efr\\ ScaleUnit\\ ScaleUnit.EFR.Installer\\\\ talpyklos debug\\ net461** **raskite ScaleUnit.EFR.Installer diegimo** priemonės.
        - **Vietinė CRT "Modern POS":** **aplanke Efr\\ ModernPOS ModernPOS.EFR.Installer\\\\\\ talpyklos debug\\ net461** **raskite ModernPOS.EFR.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **" CRT Modern POS" vieta:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Įdiekite "Fiscal Connector" plėtinius:

    "Hardware" arba EKA kasos [aparate galite](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) įdiegti " [Fiscal Connector" plėtinius](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Įdiekite aparatūros stoties plėtinius:

        1. **Aplanke Efr\\ HardwareStation\\ HardwareStation.EFR.Installer\\ talpyklos\\ debug\\ net461** **raskite HardwareStation.EFR.Installer diegimo** priemonės.
        1. Paleiskite plėtinio diegimo programą iš komandų eilutės vykdydami šią komandą.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Įdiekite EKA plėtinius:

        1. Atidarykite EKA **iždo jungties pavyzdžio sprendimą Dynamics365Commerce.Solutions\\ FiscalIntegration\\ PosFiscalConnectorSample\\ Contoso.PosFiscalConnectorSample.sln** ir sukurkite jį.
        1. **Aplanke PosFiscalConnectorSample\\ StoreCommerce.Installer\\ bin\\ Debug\\ net461** **raskite Contoso.PosFiscalConnectorSample.StoreCommerce.Installer diegimo** priemonės.
        1. Paleiskite plėtinio diegimo programą iš komandų eilutės vykdydami šią komandą.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti [ir](fiscal-integration-sample-build-pipeline.md) paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio paketus, atlikite nurodytus veiksmus. **EFR build-pipeline.yml** šablono JAML **\\ failą galima rasti YAML_Files** saugyklos aplanke [Dynamics 365 Commerce Pardavimo](https://github.com/microsoft/Dynamics365Commerce.Solutions) galimybės.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Čekijos finansinio registravimo tarnybos integravimo pavyzdys remiasi finansinio [integravimo funkcija ir](fiscal-integration-for-retail-channel.md) yra Mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ FiscalIntegration\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke, kuris yra sprendimų saugykloje (pvz., [pavyzdys, esantis release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas CRT, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite Čekijos [Respublika (senesnės veiklos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-cze-fi-sample-sdk.md). Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti atsakymus iš fiskalinių registracijų tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

Yra viena **DocumentProviderEFRFiscalCZE** užklausų apdorojimo programa, skirta dokumentų teikėjui, kuris naudojamas finansinio registravimo tarnybos iždo dokumentams generuoti.

Ši apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas.

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas paslaugai konkretus dokumentas, kuris turi būti užregistruotas finansinio registravimo tarnybose.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, kliento sąskaitos depozitai ir klientų užsakymų depozitai.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš finansinių registracijų tarnybos. Šis atsakymas yra eilutėmis išrašomas į formą, kad būtų galima įrašyti.

#### <a name="configuration"></a>Konfigūracija

Finansinio dokumento **teikėjo konfigūracijos failas yra src\\ FiscalIntegration\\ Efr\\ konfigūracijų\\ DocumentProviders\\ DocumentProviderFiscalEFRSampleCzech.xml**[Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinio dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su finansinių registracijų tarnyba. Aparatūros stoties plėtinys naudoja HTTP protokolą dokumentams, kuriuos plėtinys CRT sugeneruoja finansinio registravimo tarnybai, pateikti. Jis taip pat tvarko atsakymus, gautus iš finansinio registravimo tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**EFRHandler užklausos** apdorojimo programa yra iždo registracijos tarnybos užklausų tvarkymo įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas.

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į finansinio registravimo tarnybą ir grąžina atsakymą iš jos.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama norint patikrinti finansinių registracijų tarnybos sveikumą.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama norint inicijuoti finansinių registracijų tarnybą.

#### <a name="configuration"></a>Konfigūracija

Finansinio jungties konfigūracijos **failas yra src\\ FiscalIntegration\\ Efr\\ konfigūracijų\\ jungčių\\ ConnectorEFRSample.xml**[Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinių jungčių parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="pos-fiscal-connector-extension-design"></a>EKA "Fiscal Connector" plėtinio dizainas

EKA finansinio jungties plėtinio paskirtis yra susisiekti su finansinio registravimo tarnyba iš EKA. Ryšio tikslais naudojamas HTTPS protokolas.

#### <a name="fiscal-connector-factory"></a>Finansinių jungčių gamykla

Iždo jungties gamyklos jungties pavadinimas susietas su "Fiscal Connector **" diegimas ir yra faile Pos.Extension\\ Connectors\\ FiscalConnectorFactory.ts**. Jungties pavadinimas turi atitikti "Commerce Headquarters" nurodytą finansinio jungties pavadinimą.

#### <a name="efr-fiscal-connector"></a>EFR iždo jungtis

EFR fiskalinė jungtis yra **Pos.Extension\\ Connectors\\ Efr\\ EfrFiscalConnector.ts faile**. Jis įdiegia **IFiscalConnector sąsają**, palaikančią šias užklausas:

- **FiscalRegisterSubmitDocumentClientRequest** – ši užklausa siunčia dokumentus finansinio registravimo tarnybai ir grąžina atsakymą iš jos.
- **FiscalRegisterIsReadyClientRequest** – ši užklausa naudojama norint patikrinti iždo dokumentų registracijos tarnybos sveikumą.
- **FiscalRegisterInitializeClientRequest** – ši užklausa naudojama norint inicijuoti finansinio registravimo tarnybą.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra sprendimų saugyklos **src\\ FiscalIntegration\\ Efr\\ konfigūracijų \\**[Dynamics 365 Commerce jungčių](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis** laikas milisekundiais, kurį jungtis lauks atsakymo iš fiskalinių registracijų tarnybos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
