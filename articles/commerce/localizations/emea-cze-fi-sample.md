---
title: Čekijos finansinio registravimo tarnybos integravimo pavyzdys
description: Šioje temoje pateikta Čekijos Respublika finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 0a04ebb7685ff0b72207d9268b4aea980679572e
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944994"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Čekijos finansinio registravimo tarnybos integravimo pavyzdys

[!include[banner](../includes/banner.md)]

Šioje temoje pateikta Čekijos Respublika finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Siekiant patenkinti vietinius finansinius reikalavimus grynųjų pinigų registrams Čekijos Respublika, Čekijos respublika turi pavyzdinį kasos aparato Dynamics 365 Commerce (EKA) integravimą su išorine finansinio registravimo tarnyba. Pavyzdys išplečia finansinio [integravimo funkciją](fiscal-integration-for-retail-channel.md). Jis remiasi [EFR (elektroninio finansinio registro)](https://efsta.org/sicherheitsloesungen/) sprendimu iš [EFSTA](https://efsta.org/) ir įgalina ryšį EFR tarnyba per HTTPS protokolą. EFR tarnyba užtikrina elektroninę pardavimo registraciją (EET – Elektro²² evidence tržeb), t. y. pardavimų duomenų perdavimas mokesčių institucijų fiskalinei žiniatinklio tarnybai.

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

- Pardavimo eilutės, susijusios su išdavimo dovanų kortele arba pardavimo operacijose pridėtomis dovanų kortelės operacijomis, yra pažymimos specialiu atributu, kai operacija užregistruojama *finansinio* registravimo *tarnybose*.
- Mokėjimas dovanų kortele laikomas įprastu mokėjimu ir pažymėtas specialiu atributu, kai operacija užregistruota finansinio registravimo tarnybose.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Kliento sąskaitos depozitai ir kliento užsakymo depozitai

Finansinio registravimo tarnybos integravimo pavyzdys vykdo šias taisykles, susijusias su kliento sąskaitos depozitais ir kliento užsakymo depozitais.

- Operacija, susijusi su kliento sąskaitos depozitu arba kliento užsakymo depozitu, užregistruota finansinio registravimo tarnybose kaip viena eilutės operacija ir pažymėta specialiu atributu. Šioje eilutėje nurodyta depozito PVM grupė.
- Kai sukuriamas kliento užsakymas, t. y. kliento užsakymas, kuriame yra produktai, kuriuos klientas gali perkelti iš parduotuvės, ir produktai, kurie bus paimti arba išsiųsti vėliau, finansinio registravimo tarnybos užregistruotoje operacijoje yra eilutė už produktus, kurie yra vykdomi, ir užsakymo depozito eilutė.
- Mokėjimas iš kliento sąskaitos laikomas įprastu mokėjimu ir pažymimas specialiu atributu, kai operacija užregistruojama finansinio registravimo tarnybose.
- Kliento užsakymo depozito suma, taikoma kliento užsakymo paėmimo operacijai, laikoma įprastu mokėjimu ir pažymėta specialiu atributu, kai operacija užregistruojama *finansinio* registravimo tarnybose.

### <a name="offline-registration"></a>Registracija ne tinkle

Jei fiskalinių registracijų paslaugai nepavyksta perduoti operacijos duomenų į mokesčių institucijų fiskalinę žiniatinklio tarnybą (pvz., dėl atsakymo skirtasis laikas) ir gauti patvirtinimą iš žiniatinklio tarnybos (t. y. operacijos fiskalinio identifikavimo kodo), ji sugeneruoja vietinį operacijos parašą ir į atsakymą įtraukia jį bei specialų klaidos kodą. Finansinio registravimo tarnyba atstatius tinklo ryšį atstato operacijas originalia tvarka fone.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

Finansinio registravimo tarnyba palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainą. Todėl parduotuvių ir klientų parinktis Kaina su PVM turi būti **nustatyta** kaip **Taip**.

## <a name="set-up-commerce-for-the-czech-republic"></a>Nustatyti Čekijos komercijos prekybą

Šiame skyriuje aprašomi Komercijos parametrai, kurie yra specifiniai ir rekomenduojami Čekijos Respublikai. Daugiau informacijos ieškokite ["Commerce" pagrindinis](../index.md) puslapis.

Norėdami naudoti Čekiją specifinę funkciją, turite nurodyti šiuos parametrus.

- Pirminiame juridinio subjekto adrese nustatykite **šalies/regiono** lauką **CZE** (Čekijos Respublika).
- Kiekvienos Čekijos Respublika, kuri yra Čekijos Respublikai, EKA funkcijų profilyje nustatykite ISO kodo **lauką** **CZ** (Čekijos Respublika).

Taip pat turite nurodyti šiuos Čekijos parametrus. Atkreipkite dėmesį, kad užbaigę nustatymą turite vykdyti atitinkamas paskirstymo užduotis.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Nustatyti PVM pagal Čekijos Respublika reikalavimus


Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM priemones, ieškokite [PVM](../../finance/general-ledger/indirect-taxes-overview.md) peržiūra.

### <a name="set-up-stores"></a>Parduotuvių nustatykite

Puslapyje **Visos** parduotuvės atnaujinkite parduotuvės informaciją. Tiksliau nustatykite šiuos parametrus.

- Lauke **PVM grupė** nurodykite PVM grupę, kurią reikia naudoti pardavimams numatytojam klientui.
- Nustatykite **parinktį Kainos su PVM kaip** **Taip**.
- Nustatykite **įmonės** pavadinimą lauke Pavadinimas. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės pavadinimas. Taip pat galite įtraukti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti mokesčio **identifikavimo numerio (TIN)** lauką kaip įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės identifikavimo numeris. Taip pat galite prie pardavimo kvito maketo pridėti įmonės identifikavimo numerį kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų kūrimas

Nustatyti EKA funkcijų šablonus.

- Kvitų **numeravimo "FastTab" nustatykite kvitų numeravimą, sukurdami arba atnaujindami pardavimo, pardavimo užsakymo ir** **grąžinimo** **·** **kvitų** operacijų tipų įrašus.

### <a name="set-up-registration-numbers"></a>Nustatyti registracijos numerius

1. Eikite **į organizacijos administravimo visuotinės adresų \>\> knygelės registracijos tipų registracijos \>** tipus. Sukurkite naują registracijos tipą. Nurodykite **CZE (Čekijos Respublika) lauką Šalis/regionas** ir **apribokite** jį organizacija.
2. Eikite **į organizacijos administravimo visuotinės adresų \>\> knygelės registracijos tipų registracijos \>** kategorijas. Kurti naują registracijos kategoriją. Pasirinkite registracijos tipą iš ankstesnio veiksmo ir nustatykite registracijos **kategoriją** kaip verslo patalpos **ID**.
3. Eikite į **Organizacijos valdymas \> Organizacijos \> Valdymo vienetai**. Kiekvienai Parduotuvei, esanei Čekijos Respublikai, pasirinkite su parduotuve susijusį vienetą. Adreso **·** "FastTab" išplėskite **išplečiamąjį** sąrašą Daugiau pasirinkčių ir pasirinkite **Papildoma**. 
4. Atidarytame puslapyje **Tvarkyti** adresus turite nurodyti šiuos parametrus.

    - Adreso **·** "FastTab" lauke **Šalis /** regionas nustatykite **CZE**.
    - Registravimo **ID** "FastTab" sukurkite naują įrašą. Pasirinkite anksčiau sukurtą registracijos tipą ir nustatykite registracijos numerį.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos **teksto puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atsikreipkite **dėmesį, kad lentelėje pateiktos kalbos ID, teksto ID ir teksto vertės** **yra tik** **pavyzdžiai**. Juos galite pakeisti, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas teksto ID vertės turi būti unikalios ir jos turi būti lygios arba **didesnės** 900001.

Įtraukite šias EKA žymes į **kalbos** teksto EKA skyrių iš **lentelės**:

| Kalbos ID | Teksto ID | Tekstas                   |
|-------------|---------|------------------------|
| en-JAV       | 900001  | ID klientos sąs. / pokladny |
| en-JAV       | 900002  | B SD                    |
| en-JAV       | 900003  | P SG                    |
| en-JAV       | 900004  | FIK                    |
| en-JAV       | 900005  | Informacija                   |
| en-JAV       | 900006  | Sekos numeris        |

Pasirinktinių **laukų** puslapyje pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad** antraštės teksto ID reikšmės turi atitikti teksto ID **vertes**, kurias nurodėte kalbos **teksto** puslapyje:

| Pavadinimas                 | Tipas    | Vaizdo aprašo teksto ID |
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

Pakeiskite kiekvieno reikiamo kvito formato lauko Spausdinti veikimo būdą **reikšmę** į **Visada** spausdinti.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

- **Antraštė:** pridėkite šiuos laukus.

    - **Parduotuvės pavadinimas** **ir mokesčio** ID: šie laukai naudojami kvituose spausdinant įmonės pavadinimą ir tapatybės numerį. Taip pat galite įtraukti įmonės pavadinimą ir tapatybės numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės** adresas, **data**, **laikas 24** val., **kvito** numeris ir registro **numeris**.
    - **Sekos** numeris: šis laukas identifikuoja grynųjų pinigų operacijos numerį finansinio registravimo tarnybose.

- **Eilutės:** įtraukite šiuos laukus.

    - **Prekės pavadinimas**
    - **Kiekis**
    - **Bendra kaina su mokesčiu**

- **Poraštė:** įtraukite šiuos laukus.

    - Mokėjimo laukus, kad būtų išspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, į vieną maketo eilutę įtraukite **laukus Mokėjimo priemonės pavadinimas** ir Mokėjimo priemonės **suma**.
    - **ID provozovny/pokladny** : šiame lauke spausdinami verslo patalpų ir kasos identifikatoriai.
    - **BKP** : šiame lauke spausdinamas mokesčių mokėtojo saugos kodas, kurį priskiria fiskalinės registracijos tarnyba.
    - **FIK** : šiame lauke spausdinamas operacijos, kurią mokesčių institucijų žiniatinklio tarnyba priskiria sėkmingos registracijos internetu atveju, finansinio identifikavimo kodas.
    - **PKP** : šiame lauke spausdinamas mokesčių mokėtojo parašo kodas, kurį sugeneruoja fiskalinės registracijos tarnyba registracijos neprisijungus atveju.
    - **Informacija** : šiame lauke spausdinama papildoma fiskalinės registracijos tarnybos informacija.

Daugiau informacijos apie tai, kaip dirbti su gavimo formatais, ieškokite [Set up and design receipt formatus](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Nustatyti Čekijos Respublikos fiskalinę integraciją

Čekijos fiskalinės registracijos tarnybos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcija](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **sprendimų saugyklos src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra "Commerce" vykdymo laiko pratęsimas (CRT), ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Ankstesnę mažmeninės prekybos SDK versiją turite naudoti kūrėjo virtualioje mašinoje (VM) Microsoft Dynamics "Lifecycle Services" (LCS). Daugiau informacijos ieškokite [Čekijos Respublikos fiskalinės integracijos imties diegimo gairėse (palikimas)](emea-cze-fi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite fiskalinės integracijos nustatymo veiksmus, aprašytus [Komercijos kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatyti fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Be to, atkreipkite dėmesį į fiskalinės registracijos proceso parametrus, [būdingus šiam fiskalinės registracijos tarnybos integravimo ėminiui](#set-up-the-registration-process).
1. [Nustatykite klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinti neautomatinį atidėtų fiskalinės registracijos vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Nustatyti registracijos procesą

Norėdami įgalinti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte "Commerce" būstinę. Daugiau informacijos ieškokite [Set up fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite finansinio dokumento teikėjo ir finansinio jungties konfigūracijos failus:

    1. Atidaryti [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite teisingą išleidimo šakos versiją pagal savo SDK / programos versiją **[(pvz., leidimas / 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> Efr**.
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą **dalyje Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml** (pvz., [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą **\> "Configurations \> Connectors ConnectorEFRSample.xml** (pvz., [išleidimo failą/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Šio finansinio integravimo pavyzdžio konfigūracijos failai yra šiuose LCS kūrėjo VM mažmeninės prekybos SDK aplankuose:
    >
    > - **Finansinio dokumento teikėjo konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.EFRSample \\ Configuration \\ DocumentProviderFiscalEFRSampleCzech.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ extension.EFRSample \\ Configuration \\ ConnectorEFRSample.xml
    > 
    > Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite **pasirinktį Įgalinti** fiskalinį integravimą kaip **Taip**.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" dokumentų teikėjai ir įkelkite anksčiau **\>\>\>** atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" jungtis ir įkelkite anksčiau **\>\>\>** atsisiųstą "Fiscal Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir \> "Commerce" kanalo nustatymo \> "Fiscal integration \> Connector" funkcinius** profilius. Sukurti naują jungties funkcinį profilį. Pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį. Pagal reikia [atnaujinti duomenų](#default-data-mapping) susiejimo parametrus.
1. Eikite į **"Retail" ir \> "Commerce \> Channel" nustatymo "Fiscal \> integration Connector" techninius profilius.** Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją](#fiscal-connector-settings) atnaujinkite jungties parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymo "Fiscal integration \> Fiscal" jungties** grupes. Sukurkite naują anksčiau sukurto jungties funkcinių profilių finansinių jungčių grupę.
1. Eikite į **"Retail" ir "Commerce \>\> Channel" nustatymo "Fiscal integration \> Fiscal" registracijos** procesus. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso** "FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotiu, prie kurios bus prijungtas fiskalinis spausdintuvas. **"FastTab" Iždo** išoriniuose įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
1. Atidarykite paskirstymo grafiką **("Retail and Commerce Retail" ir "Commerce IT Distribution" grafiką) ir pasirinkite \> užduotis \>** **1070 ir** **1090, kad** duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas – mokesčio procentų verčių, kurios nustatytos PVM kodams, susiejimas su** **atributo TaxG (mokesčių grupė) vertėmis užklausose, kurios siunčiamos į fiskalinę** tarnybą. Čia yra numatytasis susiejimas:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM mokesčių grupę, kurią palaiko EFR finansinio registravimo tarnyba. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Čekijos Respublika, ieškokite [EFR](https://public.efsta.net/efr/) nuorodoje.

- **Numatytosios PVM grupės susiejimas – bet kurios PVM sumos, kurių negalima susieti su viena iš iš anksto nustatytų PVM grupių, bus priskiriamos numatytai** (pagrindinei) PVM grupei. Čia yra numatytasis susiejimas:

    ```
    A
    ```

- **Depozito PVM grupės** susiejimas – kliento įmokos sumos ir kliento užsakymo depozito sumos bus priskiriamos depozito PVM grupei. Čia yra numatytasis susiejimas:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis laikas milisekundiais, kurį fiskalinė jungtis lauks atsakymo iš** fiskalinių registracijų tarnybos.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite [Čekijos Respublikos fiskalinės integracijos imties diegimo gairėse (palikimas)](emea-cze-fi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba [Dynamics 365 Commerce atsisiųskite](https://github.com/microsoft/Dynamics365Commerce.Solutions) sprendimų saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr.["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą **Dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ EFR.sln** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** **aplanke Efr \\\\ ScaleUnit ScaleUnit.EFR.Installer talpyklos \\\\ debug \\ net461** raskite **ScaleUnit.EFR.Installer diegimo** priemonės.
        - **Vietinė CRT "Modern POS": aplanke** **Efr \\ ModernPOS \\ ModernPOS.EFR.Installer talpyklos \\\\ debug \\ net461** raskite **ModernPOS.EFR.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **"Modern CRT POS" vieta:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatūros stoties plėtinius:

    1. Aplanke **Efr \\ HardwareStation \\ HardwareStation.EFR.Installer \\ talpyklos \\ debug \\ net461** raskite **HardwareStation.EFR.Installer diegimo** priemonės.
    1. Paleiskite plėtinio diegimo programą iš komandų eilutės:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti ir paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio [paketus, atlikite nurodytus veiksmus.](fiscal-integration-sample-build-pipeline.md) **EFR build-pipeline.yml šablono JAML failą galima** rasti sprendimų saugyklos YAML_Files pardavimo galimybių **\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) aplanke.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Čekijos fiskalinės registracijos tarnybos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcija](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **sprendimų saugyklos src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra plėtinys, ir fiskalinė jungtis, kuri CRT "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite [Čekijos Respublikos fiskalinės integracijos imties diegimo gairėse (palikimas)](emea-cze-fi-sample-sdk.md). Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, tikslas yra generuoti konkrečios paslaugos dokumentus ir tvarkyti atsakymus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

Yra viena **documentProviderEFRFiscalCZE** dokumentų teikėjo užklausų apdorojimo programa, naudojama fiskalinės registracijos tarnybos fiskaliniams dokumentams generuoti.

Ši apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas.

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Jis grąžina su paslauga susijusius dokumentus, kurie turėtų būti užregistruoti fiskalinės registracijos tarnyboje.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimai, klientų sąskaitų indėliai ir klientų užsakymų indėliai.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš fiskalinės registracijos tarnybos. Šis atsakymas serijizuotas, kad būtų galima suformuoti eilutę, kad ji būtų paruošta įrašyti.

#### <a name="configuration"></a>Konfigūravimas

Finansinio dokumento teikėjo konfigūracijos failas yra **src \\ FiscalIntegration \\ Efr \\ Configurations \\ DocumentProviders \\ DocumentProviderFiscalEFRSampleCzech.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo tikslas – įgalinti finansinio dokumento teikėjo parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra bendrauti su fiskalinės registracijos tarnyba. Aparatūros stoties plėtinys naudoja HTTP protokolą dokumentams, kuriuos CRT plėtinys sugeneruoja, pateikti į fiskalinės registracijos tarnybą. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

**EFRHandler** užklausų apdorojimo programa yra registracijos tarnybos užklausų tvarkymo pradinis taškas.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

Jungtis palaiko šias užklausas.

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į fiskalinės registracijos tarnybą ir pateikia iš jos atsakymą.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InicijuotiFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybai inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Fiskalinės jungties konfigūracijos failas yra **src \\ FiscalIntegration \\ Efr \\\\ Configurations \\ Connectors ConnectorEFRSample.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti fiskalinės jungties parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
