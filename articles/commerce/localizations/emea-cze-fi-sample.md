---
title: Čekijos Respublikos mokesčių registravimo paslaugos integravimo pavyzdys
description: Šioje temoje pateikiama Čekijos Respublikos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 990de96f57f4a22b4d58da5f970b1b96f5fc21f5
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077095"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Čekijos Respublikos mokesčių registravimo paslaugos integravimo pavyzdys

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama Čekijos Respublikos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.

Kad atitiktų vietinius mokesčių reikalavimus kasos aparatams Čekijoje,Dynamics 365 Commerce Čekijos Respublikai skirta funkcija apima pavyzdinį pardavimo vietos (POS) integravimą su išorine mokesčių registravimo paslauga. Mėginys pratęsia [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md). Jis pagrįstas [EFR (elektroninis mokesčių registras)](https://efsta.org/sicherheitsloesungen/) sprendimas iš [EFSTA](https://efsta.org/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR paslauga užtikrina elektroninę pardavimų registraciją (EET – Elektronická bizonyíték tržeb), ty pardavimo duomenų perdavimą internetu į mokesčių institucijų fiskalinę žiniatinklio paslaugą.

EFR paslauga turėtų būti talpinama „Commerce Hardware“ stotyje arba atskirame įrenginyje, prie kurio galima prisijungti iš „Hardware“ stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

„Microsoft“ neišleidžia jokios aparatinės įrangos, programinės įrangos ar dokumentų iš EFSTA. Norėdami gauti informacijos apie tai, kaip gauti EFR sprendimą ir jį naudoti, susisiekite [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Scenarijai

Toliau pateikiami scenarijai taikomi mokesčių registravimo paslaugų integravimo pavyzdyje Čekijoje.

- Grynųjų pinigų operacijų registravimas fiskalinės registracijos tarnyboje.

    - Išsamius operacijų duomenis siųskite mokesčių registravimo tarnybai. Šie duomenys apima pardavimo linijos informaciją ir informaciją apie nuolaidas, mokėjimus ir mokesčius. Fiskalinės registracijos paslauga toliau siunčia duomenis į mokesčių inspekcijos žiniatinklio paslaugą ir iš jos gauna patvirtinimą, kuriame nurodytas operacijos fiskalinis identifikavimo kodas.
    - Užfiksuokite atsakymą iš fiskalinės registracijos tarnybos. Šis atsakymas apima fiskalinius duomenis, tokius kaip fiskalinis identifikavimo kodas, operacijos saugos kodas ir kt.
    - Išspausdinkite registruotos operacijos fiskalinius duomenis ant kvito.

- Dovanų kortelių operacijų ir klientų indėlių registravimas fiskalinės registracijos tarnyboje.

    - Išleiskite dovanų kortelę arba pridėkite prie jos pinigų.
    - Užregistruokite kliento sąskaitos indėlį.
    - Sukurkite kliento užsakymą ir užregistruokite užstatą.
    - Redaguokite kliento užsakymą ir nepaisykite užsakymo užstato.
    - Atšaukti kliento užsakymą ir grąžinti užstatą už užsakymą.

- Klaidų apdorojimas, pvz., šios parinktys.

    - Bandykite iš naujo registruotis, jei įmanoma, pvz., jei fiskalinės registracijos paslauga nepasiekiama, neparengta arba nereaguoja.
    - Atidėti fiskalinę registraciją.
    - Praleiskite fiskalinę registraciją arba pažymėkite operaciją kaip registruotą ir įtraukite informacinius kodus, kad užfiksuotumėte gedimo priežastį ir papildomą informaciją.
    - Prieš atidarant naują pardavimo operaciją arba užbaigiant pardavimo operaciją, patikrinkite, ar yra prieinama fiskalinės registracijos paslauga.

### <a name="gift-cards"></a>Dovanų kortelės

Fiskalinės registracijos paslaugos integravimo pavyzdys įgyvendina šias taisykles, susijusias su dovanų kortelėmis.

- Pardavimo linijos, susijusios su *Išduoti dovanų kortelę* arba *Pridėti prie dovanų kortelės* operacijos pardavimo sandoryje pažymimos specialiu atributu, kai sandoris registruojamas fiskalinės registracijos tarnyboje.
- Apmokėjimas dovanų kortele laikomas įprastu mokėjimu ir pažymimas specialiu atributu, kai operacija užregistruojama fiskalinės registracijos tarnyboje.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Kliento sąskaitos indėliai ir klientų užsakymų indėliai

Fiskalinės registracijos paslaugos integravimo pavyzdys įgyvendina šias taisykles, susijusias su kliento sąskaitos įnašais ir kliento užsakymo įnašais.

- Operacija, susijusi su kliento sąskaitos indėliu arba kliento užsakymo indėliu, fiskalinės registracijos tarnyboje registruojama kaip vienos eilutės operacija ir pažymima specialiu atributu. Šioje eilutėje nurodoma indėlio PVM grupė.
- Kai sukuriamas hibridinis kliento užsakymas, tai yra kliento užsakymas, kuriame yra prekių, kurias klientas gali išsinešti iš parduotuvės, taip pat gaminių, kuriuos vėliau atims ar išsiųs, operacija registruojama fiskalinės registracijos tarnyboje. yra eilutės produktams, kurie atliekami, taip pat eilutė užsakymo užstatui.
- Mokėjimas iš kliento sąskaitos yra laikomas įprastu mokėjimu ir pažymimas specialiu atributu, kai operacija užregistruojama fiskalinės registracijos tarnyboje.
- Kliento užsakymo depozito suma, taikoma kliento užsakymui *Paimti* operacija yra laikoma eiliniu mokėjimu ir pažymima specialiu atributu, kai operacija registruojama fiskalinės registracijos tarnyboje.

### <a name="offline-registration"></a>Registracija neprisijungus

Jei fiskalinės registracijos paslaugai nepavyksta perduoti operacijų duomenų į mokesčių institucijų fiskalinę žiniatinklio paslaugą (pavyzdžiui, dėl atsakymo skirtojo laiko) ir negauti patvirtinimo iš žiniatinklio tarnybos (ty operacijos fiskalinio identifikavimo kodo), jis sugeneruoja vietinį operacijos parašą ir į atsakymą įtraukia jį bei specialų klaidos kodą. Fiskalinės registracijos paslauga iš naujo siunčia operacijas pradine tvarka fone, kai tik atkuriamas tinklo ryšys.

### <a name="limitations-of-the-sample"></a>Mėginio apribojimai

Fiskalinės registracijos paslauga palaiko tik tuos atvejus, kai pardavimo mokestis yra įtrauktas į kainą. Todėl, **Kaina su pardavimo mokesčiu** parinktis turi būti nustatyta į **Taip** tiek parduotuvėms, tiek pirkėjams.

## <a name="set-up-commerce-for-the-czech-republic"></a>Nustatyti komerciją Čekijoje

Šiame skyriuje aprašomi prekybos nustatymai, būdingi ir rekomenduojami Čekijos Respublikai. Daugiau informacijos žr [Prekybos pagrindinis puslapis](../index.md).

Norėdami naudoti Čekijoje būdingas funkcijas, turite nurodyti šiuos nustatymus.

- Pirminiame juridinio asmens adresu nustatykite **Šalis/regionas** laukas į **CZE** (Čekijos Respublika).
- Kiekvienos Čekijos Respublikoje esančios parduotuvės POS funkcijų profilyje nustatykite **ISO kodas** laukas į **CZ** (Čekijos Respublika).

Taip pat turite nurodyti šiuos Čekijos Respublikos nustatymus. Atminkite, kad baigę sąranką turite vykdyti atitinkamas platinimo užduotis.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Nustatykite PVM pagal Čekijos Respublikos reikalavimus


Turite sukurti pardavimo mokesčių kodus, pardavimo mokesčių grupes ir prekių pardavimo mokesčių grupes. Taip pat turite nustatyti produktų ir paslaugų pardavimo mokesčių informaciją. Norėdami gauti daugiau informacijos apie tai, kaip nustatyti ir naudoti pardavimo mokesčio funkcijas, žr [Pardavimo mokesčių apžvalga](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Įrengti parduotuves

Ant **Visos parduotuvės** puslapyje, atnaujinkite parduotuvės informaciją. Tiksliau, nustatykite šiuos parametrus.

- Viduje konors **Pardavimo mokesčių grupė** lauke nurodykite pardavimo mokesčių grupę, kuri turėtų būti naudojama parduodant numatytajam klientui.
- Nustatyti **Kainos nurodytos su pardavimo mokesčiais** galimybė į **Taip**.
- Nustatyti **vardas** lauką į įmonės pavadinimą. Šis pakeitimas padeda užtikrinti, kad įmonės pavadinimas bus nurodytas pardavimo kvite. Arba galite pridėti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti **Mokesčių mokėtojo kodas (TIN)** laukelyje į įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad įmonės identifikavimo numeris bus nurodytas pardavimo kvite. Arba galite pridėti įmonės identifikavimo numerį į pardavimo kvito maketą kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Nustatykite funkcijų profilius

Nustatykite POS funkcijų profilius.

- Ant **Kvitų numeracija** FastTab, nustatykite kvitų numeravimą kurdami arba atnaujindami įrašus **Išpardavimas**, **užsakymas**, ir **Grįžti** gavimo operacijų tipai.

### <a name="set-up-registration-numbers"></a>Nustatykite registracijos numerius

1. Eiti į **Organizacijos administravimas \> Pasaulinė adresų knyga \> Registracijos tipai \> Registracijos tipai**. Sukurkite naują registracijos tipą. Nurodykite **Šalis/regionas** laukas į **CZE** (Čekijos Respublika) ir apsiriboti organizacija.
2. Eiti į **Organizacijos administravimas \> Pasaulinė adresų knyga \> Registracijos tipai \> Registracijos kategorijos**. Sukurkite naują registracijos kategoriją. Iš ankstesnio veiksmo pasirinkite registracijos tipą ir nustatykite **Registracijos kategorija** į **Verslo patalpos ID**.
3. Eikite į **Organizacijos valdymas \> Organizacijos \> Valdymo vienetai**. Kiekvienai Čekijos Respublikoje esančiai parduotuvei pasirinkite su parduotuve susijusį vienetą. Ant **Adresas** „FastTab“ išplėskite **Daugiau pasirinkimų** išskleidžiamajame sąraše ir pasirinkite **Išplėstinė**. 
4. Ant atidarytos **Tvarkyti adresus** puslapyje turite nurodyti šį nustatymą.

    - Ant **Adresas** „FastTab“ nustatė **Šalis/regionas** laukas į **CZE**.
    - Ant **Registracijos ID** FastTab sukurti naują įrašą. Pasirinkite anksčiau sukurtą registracijos tipą ir nustatykite registracijos numerį.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruokite pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami POS kvitų formatuose. Numatytoji kvito sąranką kuriančio vartotojo įmonė turėtų būti tas pats juridinis asmuo, kuriame sukurta kalbos teksto sąranka. Arba tos pačios kalbos tekstai turėtų būti sukurti ir vartotojo numatytoje įmonėje, ir parduotuvės, kuriai sukurta sąranka, juridiniame subjekte.

Ant **Kalbos tekstas** puslapyje pridėkite šiuos kvito maketų pasirinktinių laukų etikečių įrašus. Atkreipkite dėmesį, kad **Kalbos ID**, **ID**, ir **Tekstas** lentelėje pateiktos vertės yra tik pavyzdžiai. Galite juos pakeisti, kad atitiktų jūsų poreikius. Tačiau, **Teksto ID** naudojamos reikšmės turi būti unikalios ir turi būti lygios arba didesnės už 900001.

Pridėkite šias POS etiketes prie **POS** skyrių **Kalbos tekstas** iš lentelės:

| Kalbos ID | Teksto ID | Tekstas                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID provozovny/pokladny |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Informacija                   |
| en-US       | 900006  | Sekos numeris        |

Ant **Pasirinktiniai laukai** puslapyje pridėkite toliau nurodytus kvito maketų pasirinktinių laukų įrašus. Prisimink tai **Antraštės teksto ID** reikšmės turi atitikti **Teksto ID** vertes, kurias nurodėte **Kalbos tekstas** puslapis:

| Pavadinimas                 | Tipas    | Vaizdo aprašo teksto ID |
|----------------------|---------|-----------------|
| TLT                  | Gavimas | 900001          |
| SEC                  | Gavimas | 900002          |
| PASIŽYMAS                 | Gavimas | 900003          |
| FISKALINĖ               | Gavimas | 900004          |
| INFORMACIJA                 | Gavimas | 900005          |
| NUOLATINIS NUMERIS     | Gavimas | 900006          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kaip nurodyta ankstesnėje lentelėje. Dėl neteisingo tinkinto lauko pavadinimo kvituose trūks duomenų.

### <a name="configure-receipt-formats"></a>Konfigūruoti kvitų formatus

Kiekvienam reikiamam kvito formatui pakeiskite reikšmę **Spausdinimo elgsena** laukas į **Visada spausdinkite**.

Kvito formato kūrėjo programoje į atitinkamas kvito dalis pridėkite šiuos pasirinktinius laukus. Atminkite, kad laukų pavadinimai atitinka kalbos tekstus, kuriuos apibrėžėte ankstesniame skyriuje.

- **Antraštė:** Pridėkite šiuos laukus.

    - **Parduotuvės pavadinimas** ir **Mokesčių identifikavimo numeris** : šie laukai naudojami įmonės pavadinimui ir tapatybės numeriui spausdinti ant kvitų. Arba galite pridėti įmonės pavadinimą ir tapatybės numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės adresas**, **·**, **24h**, **numeris**, ir **Registro numeris**.
    - **Eilės numeris** : šis laukas nurodo grynųjų pinigų operacijos fiskalinės registracijos tarnyboje numerį.

- **Linijos:** Pridėkite šiuos laukus.

    - **Prekės pavadinimas**
    - **Kiekis**
    - **Visa kaina su mokesčiais**

- **Poraštė:** Pridėkite šiuos laukus.

    - Mokėjimo laukelius, kad būtų atspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, pridėkite **Konkurso pavadinimas** ir **Konkurso suma** laukus į vieną maketo eilutę.
    - **ID provozovny/pokladny** : šiame laukelyje spausdinami verslo patalpų ir kasos aparato identifikatoriai.
    - **BKP** : šiame laukelyje spausdinamas mokesčių mokėtojo apsaugos kodas, kurį priskiria fiskalinės registracijos tarnyba.
    - **FIK** : šiame lauke išspausdinamas operacijos fiskalinis identifikavimo kodas, kurį mokesčių inspekcijos žiniatinklio tarnyba priskiria sėkmingos registracijos internetu atveju.
    - **PKP** : šiame laukelyje spausdinamas mokesčių mokėtojo parašo kodas, kurį sugeneruoja fiskalinės registracijos tarnyba registruojantis neprisijungus.
    - **Informacija** : šiame lauke spausdinama papildoma informacija iš fiskalinės registracijos tarnybos.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su kvito formatais, žr [Nustatykite ir suprojektuokite kvitų formatus](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Nustatyti Čekijos Respublikos fiskalinę integraciją

Čekijos Respublikos mokesčių registravimo paslaugos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Efr** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra komercijos vykdymo laiko pratęsimas (CRT) ir fiskalinę jungtį, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos žr [Čekijos Respublikos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-cze-fi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

Atlikite fiskalinės integracijos sąrankos veiksmus, kaip aprašyta [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat atkreipkite dėmesį į fiskalinės registracijos proceso nustatymus [būdingas šiam fiskalinės registracijos paslaugos integravimo pavyzdžiui](#set-up-the-registration-process).
1. [Nustatykite klaidų tvarkymo nustatymus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinti atidėtos fiskalinės registracijos vykdymą rankiniu būdu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatykite registracijos procesą

Norėdami įjungti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte „Commerce“ būstinę. Daugiau informacijos žr [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite mokesčių dokumentų teikėjo ir fiskalinės jungties konfigūracijos failus:

    1. Atidaryk [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla.
    1. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją (pvz.,**[išleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atviras **src \> Fiskalinė integracija \> Efr**.
    1. Atsisiųskite fiskalinio dokumento teikėjo konfigūracijos failą adresu **Konfigūracijos \> Dokumentų teikėjai \> DocumentProviderFiscalEFRSampleCzech.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą adresu **Konfigūracijos \> Jungtys \> JungtisEFRSample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra šiuose mažmeninės prekybos SDK aplankuose kūrėjo VM LCS:
    >
    > - **Fiskalinio dokumento teikėjo konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Konfigūracija\\ DocumentProviderFiscalEFRSampleCzech.xml
    > - **Fiskalinės jungties konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ HardwareStation\\ Plėtinys.EFRSpavyzdys\\ Konfigūracija\\ JungtisEFRSample.xml
    > 
    > Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Ant **Generolas** skirtuką, nustatykite **Įgalinti fiskalinę integraciją** galimybė į **Taip**.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių dokumentų teikėjai** ir įkelkite fiskalinio dokumento teikėjo konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės jungtys** ir įkelkite fiskalinės jungties konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių funkciniai profiliai**. Sukurkite naują jungties funkcinį profilį. Pasirinkite dokumento teikėją ir jungtį, kurią įkėlėte anksčiau. Atnaujinkite [duomenų atvaizdavimo nustatymus](#default-data-mapping) kaip reikalaujama.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių techniniai profiliai**. Sukurkite naują jungties techninį profilį ir pasirinkite fiskalinę jungtį, kurią įkėlėte anksčiau. Atnaujinkite [jungties nustatymai](#fiscal-connector-settings) kaip reikalaujama.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių jungčių grupės**. Sukurkite naują fiskalinių jungčių grupę jungties funkciniam profiliui, kurį sukūrėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės registracijos procesai**. Sukurkite naują fiskalinės registracijos procesą ir fiskalinės registracijos proceso veiksmą ir pasirinkite anksčiau sukurtą fiskalinių jungčių grupę.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų profilį, susietą su parduotuve, kurioje turėtų būti suaktyvintas registracijos procesas. Ant **Fiskalinės registracijos procesas** FastTab, pasirinkite fiskalinės registracijos procesą, kurį sukūrėte anksčiau.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros profilį, susietą su aparatūros stotimi, prie kurios bus prijungtas fiskalinis spausdintuvas. Ant **Fiskaliniai periferiniai įrenginiai** FastTab, pasirinkite jungties techninį profilį, kurį sukūrėte anksčiau.
1. Atidarykite platinimo tvarkaraštį (**Mažmeninė prekyba ir prekyba \> Mažmeninė prekyba ir IT \> Platinimo grafikas**) ir pasirinkite darbus **1070** ir **1090** perkelti duomenis į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytasis duomenų atvaizdavimas

Šis numatytasis duomenų atvaizdavimas įtrauktas į fiskalinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) tarifų kartografavimas** – Mokesčių procentinių verčių, nustatytų pardavimo mokesčio kodams, susiejimas su vertėmis **MokestisG** (mokesčių grupė) atributas užklausose, kurios siunčiamos fiskalinei tarnybai. Čia yra numatytasis atvaizdavimas:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Pirmasis kiekvienos poros komponentas reiškia PVM mokesčių grupę, kurią palaiko EFR fiskalinės registracijos paslauga. Antrasis komponentas reiškia atitinkamą PVM tarifą. Norėdami gauti daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Čekijoje, žr [EFR nuoroda](https://public.efsta.net/efr/).

- **Numatytasis PVM grupės susiejimas** – Visos PVM sumos, kurių negalima susieti su viena iš iš anksto nustatytų PVM grupių, bus priskirtos numatytajai (pagrindinei) PVM grupei. Čia yra numatytasis atvaizdavimas:

    ```
    A
    ```

- **Indėlių PVM grupės atvaizdavimas** – Kliento indėlio sumos ir kliento užsakymo indėlio sumos bus priskiriamos indėlio PVM grupei. Čia yra numatytasis atvaizdavimas:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Fiskalinės jungties nustatymai

Šie nustatymai įtraukti į fiskalinės jungties konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Galinio taško adresas** – Fiskalinės registracijos paslaugos URL.
- **Laikas baigėsi** – Laikas milisekundėmis, per kurį fiskalinė jungtis lauks atsakymo iš fiskalinės registracijos tarnybos.

### <a name="configure-channel-components"></a>Konfigūruokite kanalo komponentus

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Čekijos Respublikos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-cze-fi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

#### <a name="set-up-the-development-environment"></a>Nustatykite kūrimo aplinką

Norėdami nustatyti kūrimo aplinką pavyzdžiui išbandyti ir išplėsti, atlikite šiuos veiksmus.

1. Klonuokite arba atsisiųskite [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją. Daugiau informacijos žr [Atsisiųskite mažmeninės prekybos SDK pavyzdžius ir nuorodų paketus iš „GitHub“ ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą adresu **Dynamics365Commerce.Solutions\\ Fiskalinė integracija\\ Efr\\ EFR.sln**, ir pastatyti jį.
1. Diegti CRT plėtiniai:

    1. Surask CRT plėtinio diegimo programa:

        - **Prekybos masto vienetas:** Viduje konors **Efr\\ ScaleUnit\\ ScaleUnit.EFR.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ScaleUnit.EFR.Installer** montuotojas.
        - **Vietinis CRT Šiuolaikinėje POS:** Viduje konors **Efr\\ Šiuolaikinis POS\\ ModernPOS.EFR.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ModernPOS.EFR.Installer** montuotojas.

    1. Pradėkite CRT plėtinio diegimo programa iš komandinės eilutės:

        - **Prekybos masto vienetas:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Vietinis CRT Šiuolaikinėje POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatinės įrangos stoties plėtinius:

    1. Viduje konors **Efr\\ HardwareStation\\ HardwareStation.EFR.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **HardwareStation.EFR.Installer** montuotojas.
    1. Paleiskite plėtinio diegimo programą iš komandinės eilutės:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Atlikite nurodytus veiksmus [Nustatykite fiskalinės integracijos pavyzdžio kūrimo dujotiekį](fiscal-integration-sample-build-pipeline.md) sugeneruoti ir išleisti Cloud Scale Unit ir savitarnos dislokuojamus paketus fiskalinės integracijos pavyzdžiui. The **EFR build-pipeline.yml** šablono YAML failą galima rasti **Dujotiekis\\ YAML_Failai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla.

## <a name="design-of-extensions"></a>Priestatų projektavimas

Čekijos Respublikos mokesčių registravimo paslaugos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Efr** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra pratęsimas CRT ir fiskalinė jungtis, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Čekijos Respublikos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-cze-fi-sample-sdk.md). Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

### <a name="commerce-runtime-extension-design"></a>Prekybos vykdymo laiko plėtinio dizainas

Plėtinio, kuris yra fiskalinių dokumentų teikėjas, tikslas – generuoti konkrečiai paslaugai skirtus dokumentus ir tvarkyti fiskalinės registracijos tarnybos atsakymus.

#### <a name="request-handler"></a>Užklausų tvarkytojas

Yra vienas **DocumentProviderEFRFiscalCZE** dokumentų teikėjo užklausų tvarkytojas, naudojamas fiskaliniams dokumentams formuoti fiskalinės registracijos paslaugai.

Šis tvarkytuvas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas.

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkrečiai paslaugai skirtą dokumentą, kuris turėtų būti užregistruotas fiskalinės registracijos tarnyboje.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimai, klientų sąskaitos įnašai ir klientų užsakymų įnašai.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Ši užklausa grąžina fiskalinės registracijos tarnybos atsakymą. Šis atsakymas yra serijinis, kad sudarytų eilutę, kad būtų galima išsaugoti.

#### <a name="configuration"></a>Konfigūracija

Fiskalinio dokumento teikėjo konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ Efr\\ Konfigūracijos\\ Dokumentų teikėjai\\ DocumentProviderFiscalEFRSampleCzech.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – leisti fiskalinių dokumentų teikėjo nustatymus konfigūruoti iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių registravimo tarnyba. Aparatinės įrangos stoties plėtinys naudoja HTTP protokolą, kad pateiktų dokumentus CRT plėtinys generuoja fiskalinės registracijos paslaugą. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **EFRHandler** užklausų tvarkytojas yra įvesties taškas, kuriame tvarkomos užklausos į fiskalinės registracijos tarnybą.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas.

- **SubmitDocumentFiscalDeviceRequest** – Pagal šią užklausą dokumentai siunčiami fiskalinės registracijos tarnybai ir iš jos grąžinamas atsakymas.
- **IsReadyFiscalDeviceRequest** – Šis prašymas naudojamas fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama fiskalinės registracijos paslaugai inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Fiskalinės jungties konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ Efr\\ Konfigūracijos\\ Jungtys\\ JungtisEFRSample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – leisti fiskalinės jungties nustatymus konfigūruoti iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
