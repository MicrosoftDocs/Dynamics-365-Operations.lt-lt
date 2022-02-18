---
title: Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai
description: Šioje temoje pateikiama Austrijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: d720bffb98965bdc0276660d2a2e50d2bf155e74
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077170"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama Austrijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.

Kad atitiktų vietinius mokesčių reikalavimus kasos aparatams Austrijoje,Dynamics 365 Retail Austrijai skirta funkcija apima pavyzdinį pardavimo vietos (POS) integravimą su išorine mokesčių registravimo paslauga. Mėginys pratęsia [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md). Jis pagrįstas [EFR (elektroninis mokesčių registras)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) sprendimas iš [EFSTA](https://www.efsta.eu/at/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR paslauga turėtų būti talpinama mažmeninės prekybos aparatūros stotyje arba atskirame įrenginyje, prie kurio galima prisijungti iš aparatinės įrangos stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

„Microsoft“ neišleidžia jokios aparatinės įrangos, programinės įrangos ar dokumentų iš EFSTA. Norėdami gauti informacijos apie tai, kaip gauti EFR sprendimą ir jį naudoti, susisiekite [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scenarijai

Austrijos fiskalinės registracijos paslaugos integravimo pavyzdys apima šiuos scenarijus:

- Grynųjų pinigų operacijų registravimas fiskalinės registracijos tarnyboje:

    - Išsamius operacijų duomenis siųskite mokesčių registravimo tarnybai. Šie duomenys apima pardavimo linijos informaciją ir informaciją apie nuolaidas, mokėjimus ir mokesčius.
    - Užfiksuokite atsakymą iš fiskalinės registracijos tarnybos. Šis atsakymas apima skaitmeninį parašą ir nuorodą į registruotą operaciją.
    - Užregistruokite mokesčius ir susiekite juos su fiskalinės registracijos tarnybos mokesčių kodais.
    - Kvite atsispausdinkite registruotos operacijos QR kodą.

- Dovanų kortelių operacijų ir klientų indėlių kaip negrynųjų pinigų operacijų registravimas fiskalinės registracijos tarnyboje:

    - Išleiskite dovanų kortelę arba pridėkite prie jos pinigų.
    - Užregistruokite kliento sąskaitos indėlį.
    - Užregistruokite kliento užsakymo įmoką.

- Ne pardavimo sandorių ir įvykių registravimas negrynaisiais pinigais fiskalinės registracijos tarnyboje:

    - Atidaryti pamainą ir uždaryti pamainą
    - Pradinė suma, plaukiojantis įvedimas ir konkurso pašalinimas
    - Kainos perrašymas
    - Mokesčio perrašymas
    - Išspausdinta kvito kopija
    - Atidaryti stalčių
    - Spausdinti X ataskaitą
    - Spausdinti Z ataskaitą

- Spausdinti dienos pabaigos ataskaitas (X/Z ataskaitas), kuriose yra Austrijai būdingi laukai:

    - Bendras klientams pristatytų produktų ar paslaugų skaičius
    - Pardavimų suskirstymas pagal mokesčių tarifus
    - Mokėjimų suskirstymas pagal kasininką/kasos aparato operatorių
    - Kainų nuolaidos ir grąžinimai, mažinantys kasdienius pardavimus
    - Nulinis pardavimas (dovanos)

- Klaidų apdorojimas, pvz., šios parinktys:

    - Bandykite iš naujo registruotis, jei įmanoma, pvz., jei fiskalinės registracijos paslauga nepasiekiama, neparengta arba nereaguoja.
    - Atidėti fiskalinę registraciją.
    - Praleiskite fiskalinę registraciją arba pažymėkite operaciją kaip registruotą ir įtraukite informacinius kodus, kad užfiksuotumėte gedimo priežastį ir papildomą informaciją.
    - Prieš atidarant naują pardavimo operaciją arba užbaigiant pardavimo operaciją, patikrinkite, ar yra prieinama fiskalinės registracijos paslauga.

### <a name="gift-cards"></a>Dovanų kortelės

Fiskalinės registracijos paslaugos integravimo pavyzdys įgyvendina šias taisykles, susijusias su dovanų kortelėmis:

- Išskirkite pardavimo eilutes, kurios yra susijusios su *Išduoti dovanų kortelę* ir *Pridėti prie dovanų kortelės* operacijos iš grynųjų pinigų operacijos. Užuot registruodami šias eilutes kaip grynųjų pinigų operacijos dalį, užregistruokite jas kaip atskirą negrynųjų pinigų operaciją fiskalinės registracijos tarnyboje.
- Nespausdinkite mokesčių grupės suskirstymo ir QR kodo ant kvito, jei kvite yra tik dovanų kortelės eilutės.
- Atspausdinkite visą dovanų kortelių, kurios išduodamos arba iš naujo apmokestinamos atliekant operaciją, sumą atskirai nuo grynųjų pinigų operacijos sumos ant kvito.
- Išsaugokite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į atitinkamą fiskalinę operaciją.
- Apmokėjimas dovanų kortele laikomas įprastu mokėjimu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Klientų indėliai ir klientų užsakymų indėliai

Fiskalinės registracijos paslaugos integravimo pavyzdys įgyvendina šias taisykles, susijusias su klientų indėliais ir klientų užsakymų įnašais:

- Užregistruokite operaciją negrynaisiais pinigais, jei operacija yra kliento indėlis.
- Užregistruokite operaciją negrynaisiais pinigais, jei operaciją sudaro tik kliento užsakymo užstatas arba kliento užsakymo užstato grąžinimas.
- Sukūrę hibridinį kliento užsakymą, iš mokėjimo eilučių išskaičiuokite kliento užsakymo įmokos sumą.
- Išsaugokite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į fiskalinę operaciją hibridiniam kliento užsakymui.

### <a name="limitations-of-the-sample"></a>Mėginio apribojimai

Fiskalinės registracijos paslauga palaiko tik tuos atvejus, kai pardavimo mokestis yra įtrauktas į kainą. Todėl, **Kaina su pardavimo mokesčiu** parinktis turi būti nustatyta į **Taip** tiek parduotuvėms, tiek pirkėjams.

## <a name="set-up-commerce-for-austria"></a>Nustatyti „Commerce“ Austrijoje

Šiame skyriuje aprašomi „Commerce“ nustatymai, būdingi Austrijai ir rekomenduojami jai. Norėdami gauti daugiau informacijos apie sąranką, žr [Prekybos pagrindinis puslapis](../index.md).

Norėdami naudoti Austrijai būdingas funkcijas, turite nurodyti šiuos nustatymus:

- Pirminiame juridinio asmens adresu nustatykite **Šalis/regionas** laukas į **AUT** (Austrija).
- Kiekvienos parduotuvės, esančios Austrijoje, POS funkcijų profilyje nustatykite **ISO kodas** laukas į **AT** (Austrija).

Taip pat turite nurodyti šiuos Austrijos nustatymus. Atminkite, kad baigę sąranką turite vykdyti atitinkamas platinimo užduotis.

### <a name="set-up-vat-per-austrian-requirements"></a>Nustatykite PVM pagal Austrijos reikalavimus

Turite sukurti pardavimo mokesčių kodus, pardavimo mokesčių grupes ir prekių pardavimo mokesčių grupes. Taip pat turite nustatyti produktų ir paslaugų pardavimo mokesčių informaciją. Norėdami gauti daugiau informacijos apie tai, kaip nustatyti ir naudoti pardavimo mokesčio funkcijas, žr [Pardavimo mokesčių apžvalga](../../finance/general-ledger/indirect-taxes-overview.md).

Pardavimo kvite galite atspausdinti sutrumpintą pardavimo mokesčio kodą (pvz., „A“ arba „B“). Kad ši funkcija būtų prieinama, nustatykite **Spausdinti kodą** lauke ant **Pardavimo mokesčių kodai** puslapį.

### <a name="set-up-stores"></a>Įrengti parduotuves

Ant **Visos parduotuvės** puslapyje, atnaujinkite parduotuvės informaciją. Tiksliau, nustatykite šiuos parametrus:

- Viduje konors **Pardavimo mokesčių grupė** lauke nurodykite pardavimo mokesčių grupę, kuri turėtų būti naudojama parduodant numatytajam klientui.
- Nustatyti **Kainos nurodytos su pardavimo mokesčiais** galimybė į **Taip**.
- Nustatyti **vardas** lauką į įmonės pavadinimą. Šis pakeitimas padeda užtikrinti, kad įmonės pavadinimas bus nurodytas pardavimo kvite. Arba galite pridėti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti **Mokesčių mokėtojo kodas (TIN)** laukelyje į įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad įmonės identifikavimo numeris bus nurodytas pardavimo kvite. Arba galite pridėti įmonės identifikavimo numerį į pardavimo kvito maketą kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Nustatykite funkcijų profilius

Nustatykite POS funkcijų profilius:

- Ant **Kvitų numeracija** FastTab, nustatykite kvitų numeravimą kurdami arba atnaujindami įrašus **Išpardavimas**, **užsakymas**, ir **Grįžti** gavimo operacijų tipai.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruokite pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami POS kvitų formatuose. Numatytoji kvito sąranką kuriančio vartotojo įmonė turėtų būti tas pats juridinis asmuo, kuriame sukurta kalbos teksto sąranka. Arba tos pačios kalbos tekstai turėtų būti sukurti ir vartotojo numatytoje įmonėje, ir parduotuvės, kuriai sukurta sąranka, juridiniame subjekte.

Ant **Kalbos tekstas** puslapyje pridėkite šiuos kvito maketų pasirinktinių laukų etikečių įrašus. Atkreipkite dėmesį, kad **Kalbos ID**, **ID**, ir **Tekstas** lentelėje pateiktos vertės yra tik pavyzdžiai. Galite juos pakeisti, kad atitiktų jūsų poreikius. Tačiau, **Teksto ID** naudojamos reikšmės turi būti unikalios ir turi būti lygios arba didesnės už 900001.

Pridėkite šias POS etiketes prie **POS** skyrių **Kalbos tekstas** iš lentelės:

| Kalbos ID | Teksto ID | Tekstas                      |
|-------------|---------|---------------------------|
| en-US       | 900001  | QR kodas                   |
| en-US       | 900002  | Nepertraukiamas skaičius         |
| en-US       | 900003  | Mokesčių mažmeninės prekybos spausdinimo kodas     |
| en-US       | 900004  | Iš viso (pardavimas)             |
| en-US       | 900005  | Bendras mokestis (pardavimas)         |
| en-US       | 900006  | Iš viso įtraukti mokesčius (pardavimas) |
| en-US       | 900007  | Mokesčio suma (pardavimas)        |
| en-US       | 900008  | Mokesčių bazė (pardavimas)         |

Ant **Pasirinktiniai laukai** puslapyje pridėkite toliau nurodytus kvito maketų pasirinktinių laukų įrašus. Prisimink tai **Antraštės teksto ID** reikšmės turi atitikti **Teksto ID** vertes, kurias nurodėte **Kalbos tekstas** puslapis:

| Pavadinimas                 | Tipas    | Vaizdo aprašo teksto ID |
|----------------------|---------|-----------------|
| QR KODAS               | Gavimas | 900001          |
| NUOLATINIS NUMERIS     | Gavimas | 900002          |
| MAŽmeninės prekybos SPAUSDINIMO KODAS      | Gavimas | 900003          |
| SALESTOTAL           | Gavimas | 900004          |
| PARDAVIMO MOKESČIO        | Gavimas | 900005          |
| IŠPARDAVIMAS INCLUDETAX | Gavimas | 900006          |
| SALESTAXAMOUNT       | Gavimas | 900007          |
| PARDAVIMO PAGRINDAS        | Gavimas | 900008          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kaip nurodyta ankstesnėje lentelėje. Dėl neteisingo tinkinto lauko pavadinimo kvituose trūks duomenų.

### <a name="configure-receipt-formats"></a>Konfigūruoti kvitų formatus

Kiekvienam reikiamam kvito formatui pakeiskite reikšmę **Spausdinimo elgsena** laukas į **Visada spausdinkite**.

Kvito formato kūrėjo programoje į atitinkamas kvito dalis pridėkite šiuos pasirinktinius laukus. Atminkite, kad laukų pavadinimai atitinka kalbos tekstus, kuriuos apibrėžėte ankstesniame skyriuje.

- **Antraštė:** Pridėkite šiuos laukus:

    - **Parduotuvės pavadinimas** ir **Mokesčių identifikavimo numeris** laukelius, kuriais ant kvitų atspausdinamas įmonės pavadinimas ir asmens kodas. Arba galite pridėti įmonės pavadinimą ir tapatybės numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės adresas**, **·**, **24h**, **numeris**, ir **Registro numeris** laukai.
    - **Nepertraukiamas skaičius** laukelius, identifikuoti grynųjų pinigų operacijos numerį fiskalinės registracijos tarnyboje.

- **Linijos:** Pridėkite šiuos laukus:

    - **Daikto pavadinimas**.
    - **Kiekis**.
    - **Visa kaina su mokesčiais**.
    - **Mokesčių mažmeninės prekybos spausdinimo kodas**, kuris naudojamas spausdinti sutrumpintą kodą, atitinkantį prekei taikomą pardavimo mokesčio kodą.

- **Poraštė:** Pridėkite šiuos laukus:

    - Mokėjimo laukelius, kad būtų atspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, pridėkite **Konkurso pavadinimas** ir **Konkurso suma** laukus į vieną maketo eilutę.
    - **Iš viso pardavimų** lauko grupė:

        - **Iš viso (pardavimas)** laukelį, kuriame spausdinama visa kvito grynųjų pinigų pardavimo suma. Suma be mokesčių. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Iš viso įtraukti mokesčius (pardavimas)** laukelį, kuriame spausdinama visa kvito grynųjų pinigų pardavimo suma. Į sumą įeina mokesčiai. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Bendras mokestis (pardavimas)** lauką, kuris naudojamas spausdinti kvito bendrą mokesčių sumą už pardavimą grynaisiais. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.

    - **Mokesčių suskaidymas** lauko grupė. Visi šios laukų grupės laukai turi būti atspausdinti vienoje atskiroje eilutėje.

        - **Mokesčių ID** laukas, kuris yra standartinis laukas, leidžiantis atspausdinti kiekvieno pardavimo mokesčio kodo PVM suvestinę. Laukas turi būti įtrauktas į naują eilutę.
        - **Mokesčių procentas** laukas, kuris yra standartinis laukas, naudojamas pardavimo mokesčio kodo galiojančiam mokesčio tarifui spausdinti.
        - **Mokesčių bazė (pardavimas)** lauką, kuris naudojamas spausdinti kvito bendrą pardavimo grynaisiais pinigais sumą pagal PVM kodą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Mokesčio suma (pardavimas)** lauką, kuris naudojamas spausdinti kvito mokesčio sumą už pardavimą grynaisiais pagal PVM kodą.
        - **Mokesčių mažmeninės prekybos spausdinimo kodas** lauką, kuris naudojamas spausdinti sutrumpintą kodą, atitinkantį pardavimo mokesčio kodą.

    - **QR kodas** laukelį, kuriame spausdinama nuoroda į registruotą grynųjų pinigų operaciją QR kodo pavidalu.

        > [!NOTE]
        > The **QR kodas** vertė gaunama iš fiskalinio registro atsakymo. EFR savo atsakyme pateikia QR kodą tik tuo atveju, jei reikšmė **Atributai** EFR konfigūracijos laukas aprašytas EFSTA dokumentacijoje. QR kodo formatas **Atributai** EFR konfigūracijos laukas turi būti nustatytas į **BMP**.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su kvito formatais, žr [Nustatykite ir suprojektuokite kvitų formatus](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Nustatyti fiskalinę Austrijos integraciją

Austrijos mokesčių registravimo paslaugos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Efr** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra komercijos vykdymo laiko pratęsimas (CRT) ir fiskalinę jungtį, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos žr [Austrijos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-aut-fi-sample-sdk.md). Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

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
    1. Atviras **Konfigūracijos \> Dokumentų teikėjai** ir atsisiųskite fiskalinių dokumentų teikėjo konfigūracijos failus: **DocumentProviderFiscalEFRSampleAustria.xml** ir **DocumentProviderNonFiscalEFRSampleAustria.xml** (pavyzdžiui, [išleidžiamų failų vieta/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą adresu **Konfigūracijos \> Jungtys \> JungtisEFRSample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra šiuose mažmeninės prekybos SDK aplankuose kūrėjo VM LCS:
    >
    > - **Fiskalinių dokumentų teikėjo konfigūracijos failai:** RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Konfigūracija
    > - **Fiskalinės jungties konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ HardwareStation\\ Plėtinys.EFRSpavyzdys\\ Konfigūracija
    > 
    > Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Ant **Generolas** skirtuką, nustatykite **Įgalinti fiskalinę integraciją** galimybė į **Taip**.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių dokumentų teikėjai** ir įkelkite fiskalinių dokumentų teikėjo konfigūracijos failus, kuriuos atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės jungtys** ir įkelkite fiskalinės jungties konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių funkciniai profiliai**. Sukurkite du naujus jungties funkcinius profilius, po vieną kiekvienam fiskalinių dokumentų teikėjui, kurį įkėlėte anksčiau, ir pasirinkite fiskalinę jungtį, kurią įkėlėte anksčiau. Atnaujinkite [duomenų atvaizdavimo nustatymus](#default-data-mapping) kaip reikalaujama.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių techniniai profiliai**. Sukurkite naują jungties techninį profilį ir pasirinkite fiskalinę jungtį, kurią įkėlėte anksčiau. Atnaujinkite [jungties nustatymai](#fiscal-connector-settings) kaip reikalaujama.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių jungčių grupės**. Sukurkite dvi naujas fiskalinių jungčių grupes, po vieną kiekvienam anksčiau sukurtam jungties funkciniam profiliui.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės registracijos procesai**. Sukurkite naują fiskalinės registracijos procesą ir du fiskalinės registracijos proceso veiksmus ir pasirinkite anksčiau sukurtas fiskalinių jungčių grupes.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų profilį, susietą su parduotuve, kurioje turėtų būti suaktyvintas registracijos procesas. Ant **Fiskalinės registracijos procesas** FastTab, pasirinkite fiskalinės registracijos procesą, kurį sukūrėte anksčiau. Norėdami įgalinti nefiskalinių įvykių registraciją POS, **Funkcijos** FastTab, apačioje **POS**, nustatyti **Auditas** galimybė į **Taip**.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros profilį, susietą su aparatūros stotimi, prie kurios bus prijungtas fiskalinis spausdintuvas. Ant **Fiskaliniai periferiniai įrenginiai** FastTab, pasirinkite jungties techninį profilį, kurį sukūrėte anksčiau.
1. Atidarykite platinimo tvarkaraštį (**Mažmeninė prekyba ir prekyba \> Mažmeninė prekyba ir IT \> Platinimo grafikas**) ir pasirinkite darbus **1070** ir **1090** perkelti duomenis į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytasis duomenų atvaizdavimas

Šis numatytasis duomenų atvaizdavimas įtrauktas į fiskalinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) tarifų kartografavimas** – Mokesčių procentinių verčių, nustatytų pardavimo mokesčio kodams, susiejimas su vertėmis **MokestisG** (mokesčių grupė) atributas užklausose, kurios siunčiamos fiskalinei tarnybai. Čia yra numatytasis atvaizdavimas:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Pirmasis kiekvienos poros komponentas reiškia PVM mokesčių grupę, kurią palaiko EFR fiskalinės registracijos paslauga. Antrasis komponentas reiškia atitinkamą PVM tarifą. Norėdami gauti daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Austrijoje, žr [EFR nuoroda](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Fiskalinės jungties nustatymai

Šie nustatymai įtraukti į fiskalinės jungties konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Galinio taško adresas** – Fiskalinės registracijos paslaugos URL.
- **Įrenginio skirtasis laikas** – Laikas milisekundėmis, per kurį fiskalinė jungtis lauks atsakymo iš fiskalinės registracijos tarnybos.
- **Rodyti fiskalinės registracijos pranešimus** – Ši žyma valdo, ar operatoriui turi būti rodomi pranešimai, kuriuos grąžina fiskalinės registracijos paslauga.

### <a name="configure-channel-components"></a>Konfigūruokite kanalo komponentus

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Austrijos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-aut-fi-sample-sdk.md).
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
    1. Paleiskite plėtinio diegimo programą iš komandinės eilutės.

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Atlikite nurodytus veiksmus [Nustatykite fiskalinės integracijos pavyzdžio kūrimo dujotiekį](fiscal-integration-sample-build-pipeline.md) sugeneruoti ir išleisti Cloud Scale Unit ir savitarnos dislokuojamus paketus fiskalinės integracijos pavyzdžiui. The **EFR build-pipeline.yml** šablono YAML failą galima rasti **Dujotiekis\\ YAML_Failai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla.

## <a name="design-of-extensions"></a>Priestatų projektavimas

Austrijos mokesčių registravimo paslaugos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Efr** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra pratęsimas CRT ir fiskalinė jungtis, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Austrijos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-aut-fi-sample-sdk.md). Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

### <a name="commerce-runtime-extension-design"></a>Prekybos vykdymo laiko plėtinio dizainas

Plėtinio, kuris yra fiskalinių dokumentų teikėjas, tikslas – generuoti konkrečiai paslaugai skirtus dokumentus ir tvarkyti fiskalinės registracijos tarnybos atsakymus.

#### <a name="request-handler"></a>Užklausų tvarkytojas

Yra dvi dokumentų teikėjų užklausų tvarkyklės:

- **DocumentProviderEFRFiscalAUT** – Šis tvarkytuvas naudojamas fiskaliniams dokumentams fiskalinės registracijos paslaugai generuoti.
- **DocumentProviderEFRNonFiscalAUT** – Šis tvarkytuvas naudojamas nefiskaliniams dokumentams fiskalinės registracijos paslaugai generuoti.

Šie tvarkytojai yra paveldėti iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkrečiai paslaugai skirtą dokumentą, kuris turėtų būti užregistruotas fiskalinės registracijos tarnyboje.
- **GetNonFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks nefiskalinis dokumentas turi būti sugeneruotas. Jis grąžina konkrečiai paslaugai skirtą dokumentą, kuris turėtų būti užregistruotas fiskalinės registracijos tarnyboje.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas, Z ataskaitos spausdinimas, klientų sąskaitos depozitai, klientų užsakymų depozitai, audito įvykiai ir ne pardavimo operacijos.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Ši užklausa grąžina fiskalinės registracijos tarnybos atsakymą. Šis atsakymas yra serijinis, kad sudarytų eilutę, kad būtų galima išsaugoti.

#### <a name="configuration"></a>Konfigūracija

Fiskalinio dokumento teikėjo konfigūracijos failai yra **src\\ Fiskalinė integracija\\ Efr\\ Konfigūracijos\\ Dokumentų teikėjai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla:

- **DocumentProviderFiscalEFRSampleAustria** – Fiskalinių dokumentų fiskalinių dokumentų teikėjo konfigūracijos failas.
- **DocumentProviderNonFiscalEFRSampleAustria** – Nefiskalinių dokumentų fiskalinių dokumentų teikėjo konfigūracijos failas.

Šių failų tikslas – leisti fiskalinių dokumentų teikėjo nustatymus konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių registravimo tarnyba. Aparatinės įrangos stoties plėtinys naudoja HTTP protokolą, kad pateiktų dokumentus CRT plėtinys generuoja fiskalinės registracijos paslaugą. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **EFRHandler** užklausų tvarkytojas yra įvesties taškas, kuriame tvarkomos užklausos į fiskalinės registracijos tarnybą.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Fiskalinė jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Pagal šią užklausą dokumentai siunčiami fiskalinės registracijos tarnybai ir iš jos grąžinamas atsakymas.
- **IsReadyFiscalDeviceRequest** – Šis prašymas naudojamas fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama fiskalinės registracijos paslaugai inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Fiskalinės jungties konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ Efr\\ Konfigūracijos\\ Jungtys\\ JungtisEFRSample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – leisti fiskalinės jungties nustatymus konfigūruoti iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
