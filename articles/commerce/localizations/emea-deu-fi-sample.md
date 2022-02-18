---
title: Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Vokietijai
description: Šioje temoje pateikiama Vokietijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 128c94407a283bf45e5626de060cee82430f087b
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076867"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Vokietijai

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama Vokietijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.

Kad atitiktų vietinius mokesčių reikalavimus kasos aparatams Vokietijoje,Microsoft Dynamics 365 Commerce Vokietijai skirta funkcija apima pavyzdinį pardavimo vietos (POS) integravimą su išorine mokesčių registravimo paslauga. Mėginys pratęsia [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md). Jis pagrįstas [EFR (elektroninis mokesčių registras)](https://www.efsta.eu/de/fiskalloesungen/deutschland) sprendimas iš [EFSTA](https://www.efsta.eu/de/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR paslauga turėtų būti talpinama mažmeninės prekybos aparatūros stotyje arba atskirame kompiuteryje, prie kurio galima prisijungti iš aparatinės įrangos stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

„Microsoft“ neišleidžia jokios aparatinės įrangos, programinės įrangos ar dokumentų iš EFSTA. Norėdami gauti informacijos apie tai, kaip gauti EFR sprendimą ir jį naudoti, susisiekite [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Scenarijai

Toliau pateikiami scenarijai apima fiskalinės registracijos paslaugos integravimo pavyzdį Vokietijoje.

### <a name="sales-operations"></a>Pardavimo operacijos

- **Grynųjų pinigų pardavimo ir grąžinimo registravimas mokesčių registravimo tarnyboje:**

    Pardavimo operacijų registracija apima šiuos veiksmus:

    1. Sandorio registravimo pradžia

        Kiekvienos operacijos pradžia registruojama techniniame saugos elemente (TSE), kuris yra prijungtas prie EFR paslaugos. Po registracijos TSE priskiria operacijos ID (TID).

    2. Sandorio pabaigos registracija

        Kai sandoris sudaromas POS, jis registruojamas naudojant tą patį TID, kuris buvo priskirtas registruojant operacijos pradžią. Tuo metu smulkūs sandorių duomenys siunčiami fiskalinės registracijos tarnybai. Šie duomenys apima pardavimo linijos informaciją ir informaciją apie nuolaidas, mokėjimus ir mokesčius.

    3. Fiskalinės registracijos tarnybos atsakymo fiksavimas

        Saugumo duomenys gaunami iš TSE kaip atsakymo dalis ir išsaugomi operacijos metu kanalo duomenų bazėje. Saugos duomenis sudaro ši informacija:

        - TID
        - Sandorio pradžios data ir laikas
        - Sandorio pabaigos data ir laikas
        - Parašo skaitiklis
        - Patikrinkite vertę
        - USE serijos numeris

- **Klientų užsakymų registravimas fiskalinės registracijos tarnyboje:** Registracijos procesas yra toks pat kaip grynųjų pinigų pardavimo ir grąžinimo procesas.
- **Operacijų, susijusių su dovanų kortelėmis ir indėliais, registracija:** Registracijos procesas yra toks pat kaip grynųjų pinigų pardavimo ir grąžinimo procesas.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Vartotojų informavimas apie fiskalinės registracijos klaidas

Yra du būdai, kaip mokesčių registravimo paslauga gali pranešti vartotojams apie fiskalinės registracijos metu įvykusias klaidas:

- Atspausdinkite papildomą informaciją iš atsakymo **Informacinis pranešimas** laukelį ant kvitų.
- Rodyti pranešimus iš mokesčių tarnybos kaip vartotojo pranešimus POS.

    > [!NOTE]
    > Šis pranešimo mechanizmas reikalauja, kad **Rodyti fiskalinės registracijos pranešimus** parametras ant **Jungčių techniniai profiliai** puslapis būtų įjungtas.

#### <a name="printing-receipts"></a>Kvitų spausdinimas

Kvito spausdinimas Vokietijoje yra privalomas. Visuose kvituose turi būti bent ši informacija:

- Įmonės pavadinimas ir adresas
- Informacija apie prekes, įskaitant jų kainas ir kiekius
- Informacija apie gautus mokėjimus
- Informacija apie mokesčius, įskaitant bendras sumas pagal mokesčio tarifą
- Saugumo duomenys:

    - TID
    - Sandorio pradžios data ir laikas
    - Sandorio pabaigos data ir laikas
    - Parašo skaitiklis
    - Patikrinkite vertę
    - USE serijos numeris

- Informacinis pranešimas

> [!NOTE]
> QR kodą taip pat galima atspausdinti ant kvitų. Nors QR kodas yra neprivalomas, tai labai rekomenduojama. Daugiau informacijos apie tai, kaip gauti QR kodą kaip atsakymo iš fiskalinės registracijos tarnybos dalį, žr. „EFR vadovas\[ DE\] “ dokumentas, paskelbtas [EFSTA dokumentacija](https://public.efsta.net/efr/) Interneto svetainė.
>
> The **Informacinis pranešimas** kvitų laukelyje rodomas fiskalinės registracijos tarnybos pranešimas. Pavyzdžiui, sugedus parašo įrenginiui, ant kvito galima atspausdinti specialų tekstą.

#### <a name="voided-suspended-and-recalled-transactions"></a>Anuliuotos, sustabdytos ir atšauktos operacijos

- Anuliuotas sandoris registruojamas kaip prašymas nutraukti sandorį fiskalinės registracijos tarnyboje.
- Sustabdyta operacija registruojama kaip prašymas nutraukti sandorį fiskalinės registracijos tarnyboje.
- Sustabdytos operacijos atšaukimas registruojamas kaip naujos operacijos pradžia fiskalinės registracijos tarnyboje.

### <a name="non-sales-transactions-and-shift-closing"></a>Ne pardavimo sandoriai ir pamainos uždarymas

Šios ne pardavimo operacijos yra registruojamos kaip nefiskalinės operacijos fiskalinės registracijos tarnyboje naudojant **NFS** žyma:

- Deklaruoti pradinę sumą
- Nefiksuotas įrašas
- Mokėjimo priemonės šalinimas
- Pinigų įnešimas į kasą
- Inkasavimas
- Pajamų sąskaitos
- Išlaidų sąskaitos

The **Uždaryti pamainą** operacija taip pat registruojama kaip nefiskalinė operacija fiskalinės registracijos tarnyboje naudojant **NFS** žyma.

### <a name="data-export-and-audit"></a>Duomenų eksportas ir auditas

Visi sandoriai turi būti pasirašyti TSE, kad būtų užtikrintas jų vientisumas, autentiškumas ir išsamumas bei būtų išvengta manipuliavimo įrašytais duomenimis.

> [!WARNING]
> Galima naudoti tik sertifikuotą USE. Norėdami gauti informacijos apie TSE tipus ir modelius, kuriuos palaiko EFR sprendimas, žr. EFR vadovą\[ DE\] “ dokumentas, paskelbtas [EFSTA dokumentacija](https://public.efsta.net/efr/) Interneto svetainė. Norėdami gauti informacijos apie tai, kaip pasirinkti ir gauti USE, kreipkitės į [EFSTA](https://www.efsta.eu/at/kontakt).

Pagal Vokietijos taisykles reikalinga parama DSFinV-K eksportui. DSFinV-K eksportą galima suaktyvinti EFR sprendime. Daugiau informacijos apie DSFinV-K eksportą rasite „EFR vadove\[ DE\] “ dokumentas, paskelbtas [EFSTA dokumentacija](https://public.efsta.net/efr/) Interneto svetainė.

### <a name="limitations-of-the-sample"></a>Mėginio apribojimai

Fiskalinės registracijos paslauga palaiko tik tuos atvejus, kai pardavimo mokestis yra įtrauktas į kainas. Todėl, **Kainos nurodytos su pardavimo mokesčiais** parinktis turi būti nustatyta į **Taip** tiek parduotuvėms, tiek pirkėjams.

Fiskalinė paslauga nepalaiko situacijų, kai tai pačiai operacijos eilutei taikomas daugiau nei vienas pardavimo mokesčio kodas.

Fiskalinės integracijos sistema nepalaiko pardavimo kainų. Todėl šios operacijos nėra registruotos mokesčių tarnyboje.

## <a name="set-up-commerce-for-germany"></a>Nustatykite „Commerce“ Vokietijoje

Šiame skyriuje aprašomi „Commerce“ nustatymai, būdingi Vokietijai ir jai rekomenduojami. Norėdami gauti daugiau informacijos apie sąranką, žr [Prekybos pagrindinis puslapis](../index.md).

Norėdami naudoti tik Vokietijai būdingas funkcijas, turite nurodyti šiuos nustatymus.

- Pirminiame juridinio asmens adresu nustatykite **Šalis/regionas** laukas į **DEU** (Vokietija).
- Kiekvienos Vokietijoje esančios parduotuvės POS funkcijų profilyje nustatykite **ISO kodas** laukas į **DE** (Vokietija).

Taip pat turite nurodyti toliau nurodytus Vokietijos nustatymus. Baigę sąranką būtinai paleiskite atitinkamas platinimo užduotis.

### <a name="set-up-vat-per-german-requirements"></a>Nustatykite PVM pagal Vokietijos reikalavimus

Turite sukurti pardavimo mokesčių kodus, pardavimo mokesčių grupes ir prekių pardavimo mokesčių grupes. Taip pat turite nustatyti produktų ir paslaugų pardavimo mokesčių informaciją. Norėdami gauti daugiau informacijos apie tai, kaip nustatyti ir naudoti pardavimo mokesčio funkcijas, žr [Pardavimo mokesčių apžvalga](../../finance/general-ledger/indirect-taxes-overview.md).

Pardavimo kvite galite atspausdinti sutrumpintą pardavimo mokesčio kodą (pvz., „A“ arba „B“). Kad ši funkcija būtų prieinama, nustatykite **Kodas spausdinimui** lauke ant **Pardavimo mokesčių kodai** puslapį.

### <a name="set-up-stores"></a>Įrengti parduotuves

Ant **Visos parduotuvės** puslapyje, atnaujinkite parduotuvės informaciją. Tiksliau, nustatykite šiuos parametrus:

- Viduje konors **Pardavimo mokesčių grupė** lauke nurodykite pardavimo mokesčių grupę, kuri turėtų būti naudojama parduodant numatytajam klientui.
- Nustatyti **Kainos nurodytos su pardavimo mokesčiais** galimybė į **Taip**.
- Nustatyti **vardas** lauką į įmonės pavadinimą. Šis pakeitimas padeda užtikrinti, kad įmonės pavadinimas būtų rodomas pardavimo kvite. Arba galite pridėti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti **Mokesčių mokėtojo kodas (TIN)** laukelyje į įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad įmonės identifikavimo numeris būtų nurodytas pardavimo kvite. Arba galite pridėti įmonės identifikavimo numerį į pardavimo kvito maketą kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Nustatykite funkcijų profilius

Nustatykite POS funkcijų profilius. Ant **Kvitų numeracija** FastTab, nustatykite kvitų numeravimą kurdami arba atnaujindami įrašus **Išpardavimas**, **užsakymas**, ir **Grįžti** gavimo operacijų tipai.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruokite pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami POS kvitų formatuose. Numatytoji kvito sąranką kuriančio vartotojo įmonė turėtų būti tas pats juridinis asmuo, kuriame sukurta kalbos teksto sąranka. Arba tos pačios kalbos tekstai turėtų būti sukurti ir vartotojo numatytoje įmonėje, ir parduotuvės, kuriai sukurta sąranka, juridiniame subjekte.

Ant **Kalbos tekstas** puslapyje pridėkite šiuos kvito maketų pasirinktinių laukų etikečių įrašus. Atkreipkite dėmesį, kad **Kalbos ID**, **ID**, ir **Tekstas** lentelėje pateiktos vertės yra tik pavyzdžiai. Galite juos pakeisti, kad atitiktų jūsų poreikius. Tačiau, **Teksto ID** naudojamos reikšmės turi būti unikalios ir turi būti lygios arba didesnės už 900001.

Pridėkite šias POS etiketes prie **POS** skyrių **Kalbos tekstas** puslapį.

| Kalbos ID | Teksto ID | Tekstas                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR kodas                               |
| en-US       | 900002  | Operacijos ID                        |
| en-US       | 900003  | Mokesčių mažmeninės prekybos spausdinimo kodas                 |
| en-US       | 900004  | Mokesčio suma (pardavimas)                    |
| en-US       | 900005  | Mokesčių bazė (pardavimas)                     |
| en-US       | 900006  | Operacijos pradžios data ir laikas           |
| en-US       | 900007  | Operacijos pabaigos data ir laikas             |
| en-US       | 900008  | Apsaugos elemento serijos numeris |
| en-US       | 900009  | Parašo skaitiklis                     |
| en-US       | 900010  | Patikrinkite vertę                           |
| en-US       | 900011  | Informacinis pranešimas                          |

Ant **Pasirinktiniai laukai** puslapyje pridėkite toliau nurodytus kvito maketų pasirinktinių laukų įrašus. Atkreipkite dėmesį, kad **Antraštės teksto ID** reikšmės turi atitikti **Teksto ID** vertes, kurias nurodėte **Kalbos tekstas** puslapį.

| Pavadinimas                            | Tipas    | Vaizdo aprašo teksto ID |
|---------------------------------|---------|-----------------|
| QR KODAS\_ DE                      | Gavimas | 900001          |
| TRANSACTIONID\_ DE               | Gavimas | 900002          |
| MAŽmeninės prekybos SPAUSDINIMO KODAS\_ DE             | Gavimas | 900003          |
| SALESTAXAMOUNT\_ DE              | Gavimas | 900004          |
| PARDAVIMO PAGRINDAS\_ DE               | Gavimas | 900005          |
| TRANSACTIONSTARTDATETIME\_ DE    | Gavimas | 900006          |
| TRANSACTIONENDDATETIME\_ DE      | Gavimas | 900007          |
| SECURITYELEMENTSERIJOS NUMERIS\_ DE | Gavimas | 900008          |
| PARAŠŲ SKAITIS\_ DE                 | Gavimas | 900009          |
| PASIŽYMAS\_ DE                        | Gavimas | 900010          |
| INFORMACIJA\_ DE                 | Gavimas | 900011          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kaip nurodyta ankstesnėje lentelėje. Dėl neteisingo tinkinto lauko pavadinimo kvituose trūks duomenų.

### <a name="configure-receipt-formats"></a>Konfigūruoti kvitų formatus

Kiekvienam reikalaujamam kvito formatui pakeiskite reikšmę **Spausdinimo elgsena** laukas į **Visada spausdinkite**.

Kvito formato kūrėjo programoje į atitinkamas kvito dalis pridėkite šiuos pasirinktinius laukus. Atminkite, kad laukų pavadinimai atitinka kalbos tekstus, kuriuos apibrėžėte ankstesniame skyriuje.

- **Antraštė:** Pridėkite šiuos laukus:

    - **Parduotuvės pavadinimas** ir **Mokesčių identifikavimo numeris** laukelius, kuriais ant kvitų atspausdinamas įmonės pavadinimas ir identifikavimo numeris. Arba galite pridėti įmonės pavadinimą ir identifikavimo numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės adresas**, **·**, **24h**, **numeris**, ir **Registro numeris** laukai.

- **Linijos:** Pridėkite šiuos laukus:

    - **Daikto pavadinimas** lauke
    - **Kiekis** lauke
    - **Visa kaina su mokesčiais** lauke
    - **Mokesčių mažmeninės prekybos spausdinimo kodas** laukas, naudojamas sutrumpintam kodui, atitinkančiam prekei taikomą pardavimo mokesčio kodą, atspausdinti

- **Poraštė:** Pridėkite šiuos laukus:

    - Mokėjimo laukelius, kad būtų atspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, pridėkite **Konkurso pavadinimas** ir **Konkurso suma** laukus į vieną maketo eilutę.
    - Laukai, esantys **Mokesčių suskaidymas** lauko grupė. Visi šios laukų grupės laukai turi būti atspausdinti vienoje atskiroje eilutėje.

        - **Mokesčių ID** laukas, kuris yra standartinis laukas, leidžiantis atspausdinti kiekvieno pardavimo mokesčio kodo PVM suvestinę. Laukas turi būti įtrauktas į naują eilutę.
        - **Mokesčių procentas** laukas, kuris yra standartinis laukas, naudojamas pardavimo mokesčio kodo galiojančiam mokesčio tarifui spausdinti.
        - **Mokesčių bazė (pardavimas)** lauką, kuris naudojamas spausdinti kvito bendrą pardavimo grynaisiais pinigais sumą pagal PVM kodą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Mokesčio suma (pardavimas)** lauką, kuris naudojamas spausdinti kvito mokesčio sumą už pardavimą grynaisiais pagal PVM kodą.
        - **Mokesčių mažmeninės prekybos spausdinimo kodas** lauką, kuris naudojamas spausdinti sutrumpintą kodą, atitinkantį pardavimo mokesčio kodą.

    - Laukai, kuriuose yra saugių operacijų duomenų, kuriuos grąžina fiskalinės registracijos tarnyba:

        - **Operacijos ID** laukelis, identifikuojantis grynųjų pinigų operacijos fiskalinės registracijos tarnyboje numerį
        - **Sandorio pradžios datos laikas** lauke
        - **Operacijos pabaigos datos laikas** lauke
        - **Apsaugos elemento serijos numeris** lauke
        - **Parašo skaitiklis** lauke
        - **Patikrinkite vertę** lauke
        - **QR kodas** laukelį, kuriame spausdinama nuoroda į registruotą grynųjų pinigų operaciją QR kodo pavidalu

        > [!NOTE]
        > The **QR kodas** vertė gaunama iš fiskalinio registro atsakymo. EFR savo atsakyme pateikia QR kodą tik tuo atveju, jei reikšmė **Atributai** EFR konfigūracijos laukas aprašytas EFSTA dokumentacijoje. QR kodo formatas **Atributai** EFR konfigūracijos laukas turi būti nustatytas į **BMP**.

    - **Informacinis pranešimas** lauke, kad mokesčių registravimo tarnybos pranešimai būtų rodomi kvituose. Pavyzdžiui, sugedus parašo įrenginiui, ant kvito galima atspausdinti specialų tekstą.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su kvito formatais, žr [Nustatykite ir suprojektuokite kvitų formatus](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Nustatyti fiskalinę integraciją Vokietijoje

Mokesčio registracijos paslaugos integravimo pavyzdys Vokietijoje yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Efr** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra komercijos vykdymo laiko pratęsimas (CRT) ir fiskalinę jungtį, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos žr [Vokietijos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-deu-fi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

Atlikite fiskalinės integracijos sąrankos veiksmus, kaip aprašyta [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat atkreipkite dėmesį į fiskalinės registracijos proceso nustatymus [būdingas šiam fiskalinės registracijos paslaugos integravimo pavyzdžiui](#set-up-the-registration-process).
1. [Nustatykite klaidų tvarkymo nustatymus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Fiskalinės integracijos sistemos klaidų valdymo galimybės gali būti nevisiškai suderintos su vietiniais fiskaliniais reglamentais.
    >
    > - Rekomenduojame palikti **Tęskite klaidą** parinktis ant **Fiskalinės registracijos procesas** puslapis išjungtas, nes visos operacijos turi būti teisingai užregistruotos, net jei pirmasis fiskalinės registracijos bandymas nebuvo sėkmingas.
    > - Prieš įjungdami **Praleisti** arba **Pažymėti kaip registruotą** parinktis ant **Fiskalinės registracijos procesas** puslapyje, turėtumėte aptarti šiuos fiskalinės registracijos proceso pakeitimus su mokesčių konsultantu arba vietine mokesčių tarnyba.

1. [Įgalinti atidėtos fiskalinės registracijos vykdymą rankiniu būdu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatykite registracijos procesą

Norėdami įjungti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte „Commerce“ būstinę. Daugiau informacijos žr [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite mokesčių dokumentų teikėjo ir fiskalinės jungties konfigūracijos failus:

    1. Atidaryk [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla.
    1. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją (pvz.,**[išleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atviras **src \> Fiskalinė integracija \> Efr**.
    1. Atsisiųskite fiskalinio dokumento teikėjo konfigūracijos failą adresu **Konfigūracijos \> Dokumentų teikėjai \> DocumentProviderFiscalEFRSampleGermany.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą adresu **Konfigūracijos \> Jungtys \> JungtisEFRSample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra šiuose mažmeninės prekybos SDK aplankuose kūrėjo VM LCS:
    >
    > - **Fiskalinio dokumento teikėjo konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Konfigūracija\\ DocumentProviderFiscalEFRSampleGermany.xml
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

- **Konkurso tipo kartografavimas** – Mokėjimo būdų susiejimas su vertėmis **PayG** (mokėjimo grupė) atributas užklausose, kurios siunčiamos fiskalinei tarnybai. Čia yra numatytasis atvaizdavimas:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Pirmasis kiekvienos poros komponentas reiškia mokėjimo metodą, kuris yra nustatytas parduotuvėje. Antrasis komponentas reiškia atitinkamą mokėjimų grupę, kurią palaiko EFR fiskalinės registracijos paslauga. Norėdami gauti daugiau informacijos apie mokėjimo grupes, kurias EFR palaiko Vokietijoje, žr [EFR nuoroda](https://public.efsta.net/efr/).

    Mokėjimo būdų atvaizdavimo pavyzdys atitinka parduotuvės mokėjimo būdus, sukonfigūruotus standartiniuose demonstraciniuose duomenyse.

    | Mokėjimo būdas | Mokėjimo būdo pavadinimas |
    |----------------|---------------------|
    | 1              | Grynieji pinigai                |
    | 2              | Tikrinti               |
    | 3              | Kortelė                |
    | 4              | Kliento kodas    |
    | 5              | Kita               |
    | 6              | Valiuta            |
    | 7              | Kvitas             |
    | 8              | Dovanų kortelė           |
    | 9              | Mokėjimo priemonės šalinimas / nefiksavimas |
    | 10             | Lojalumo kortelės       |
    | 11             | Ne vietiniai patikrinimai    |

    Todėl turite modifikuoti pavyzdinį susiejimą pagal mokėjimo metodus, sukonfigūruotus jūsų programoje.

- **Įtraukite klientų duomenis** – Jei šis parametras įjungtas, tais atvejais, kai klientas įtraukiamas į operaciją, fiskalinės tarnybos užklausose bus pateikta klientų informacija, pvz., vardai ir adresai.
- **Pridėtinės vertės mokesčio (PVM) tarifų kartografavimas** – Mokesčių procentinių verčių, nustatytų pardavimo mokesčio kodams, susiejimas su vertėmis **MokestisG** (mokesčių grupė) atributas užklausose, kurios siunčiamos fiskalinei tarnybai. Čia yra numatytasis atvaizdavimas:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Pirmasis kiekvienos poros komponentas reiškia PVM mokesčių grupę, kurią palaiko EFR fiskalinės registracijos paslauga. Antrasis komponentas reiškia atitinkamą PVM tarifą. Norėdami gauti daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Vokietijoje, žr [EFR nuoroda](https://public.efsta.net/efr/).

- **Dovanų kortelių ir indėlių mokesčių grupė** – Vertė **MokestisG** atributas užklausose, kurios siunčiamos fiskalinei tarnybai, atsižvelgiant į operacijas, susijusias su dovanų kortelėmis ar indėliu. Čia yra numatytasis atvaizdavimas:

    ```
    G
    ```

- **Mokesčių grupė neapmokestinama PVM** – Vertė **MokestisG** atributas užklausose, kurios siunčiamos fiskalinei tarnybai, remiantis operacijomis, kurios yra atleistos nuo mokestinių prievolių. Čia yra numatytasis atvaizdavimas:

    ```
    F
    ```

> [!NOTE]
> Mokesčių nustatymai numatytajame duomenų atvaizde yra atsakingi už mokesčių nustatymų atitikimą sistemoje ir mokesčių grupėmis EFR paslaugoje. Mokesčių grupės gali būti spausdinamos ant kvitų tik tuo atveju, jei **Kodas spausdinimui** laukas nustatytas **Pardavimo mokesčių kodai** puslapį.

#### <a name="fiscal-connector-settings"></a>Fiskalinės jungties nustatymai

Šie nustatymai įtraukti į fiskalinės jungties konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Galinio taško adresas** – Fiskalinės registracijos paslaugos URL.
- **Laikas baigėsi** – Laikas milisekundėmis, per kurį fiskalinė jungtis lauks atsakymo iš fiskalinės registracijos tarnybos.
- **Rodyti fiskalinės registracijos pranešimus** – Ši žyma valdo, ar operatoriui turi būti rodomi pranešimai, kuriuos grąžina fiskalinės registracijos paslauga.

### <a name="configure-channel-components"></a>Konfigūruokite kanalo komponentus

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Vokietijos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-deu-fi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

#### <a name="set-up-the-development-environment"></a>Nustatykite kūrimo aplinką

Norėdami nustatyti kūrimo aplinką pavyzdžiui išbandyti ir išplėsti, atlikite šiuos veiksmus.

1. Klonuokite arba atsisiųskite [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją. Daugiau informacijos žr [Atsisiųskite mažmeninės prekybos SDK pavyzdžius ir nuorodų paketus iš „GitHub“ ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą adresu **Dynamics365Commerce.Solutions\\ Fiskalinė integracija\\ Efr\\ EFR.sln**, ir pastatyti jį.
1. Įdiekite „Commerce“ vykdymo laiko plėtinius:

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

    - Viduje konors **Efr\\ HardwareStation\\ HardwareStation.EFR.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **HardwareStation.EFR.Installer** montuotojas.
    - Paleiskite plėtinio diegimo programą iš komandinės eilutės:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Atlikite nurodytus veiksmus [Nustatykite fiskalinės integracijos pavyzdžio kūrimo dujotiekį](fiscal-integration-sample-build-pipeline.md) sugeneruoti ir išleisti Cloud Scale Unit ir savitarnos dislokuojamus paketus fiskalinės integracijos pavyzdžiui. The **EFR build-pipeline.yml** šablono YAML failą galima rasti **Dujotiekis\\ YAML_Failai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla.

## <a name="design-of-extensions"></a>Priestatų projektavimas

Mokesčio registracijos paslaugos integravimo pavyzdys Vokietijoje yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Efr** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra pratęsimas CRT ir fiskalinė jungtis, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Vokietijos fiskalinės integracijos pavyzdžio diegimo gairės (palikimas)](emea-deu-fi-sample-sdk.md). Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

### <a name="crt-extension-design"></a>CRT pratęsimo dizainas

Plėtinio, kuris yra fiskalinių dokumentų teikėjas, tikslas – generuoti konkrečiai paslaugai skirtus dokumentus ir tvarkyti fiskalinės registracijos tarnybos atsakymus.

#### <a name="request-handler"></a>Užklausų tvarkytojas

Dokumentų teikėjui yra vienas užklausų tvarkytojas, **DocumentProviderEFRFiscalDEU**. Šis tvarkytuvas naudojamas fiskaliniams dokumentams formuoti mokesčių registravimo paslaugai. Jis paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkrečiai paslaugai skirtą dokumentą, kuris turėtų būti užregistruotas fiskalinės registracijos tarnyboje.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Ši užklausa grąžina atsakymą kartu su išplėstiniais duomenimis.

#### <a name="configuration"></a>Konfigūracija

Fiskalinio dokumento teikėjo konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ Efr\\ Konfigūracijos\\ Dokumentų teikėjai\\ DocumentProviderFiscalEFRSampleGermany.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – leisti fiskalinių dokumentų teikėjo nustatymus konfigūruoti iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių registravimo tarnyba.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EFRSample**. Jis naudoja HTTP protokolą, kad pateiktų dokumentus, kuriuos CRT pratęsimas generuoja fiskalinės registracijos paslaugą. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **EFRHandler** užklausų tvarkytojas yra įvesties taškas, kuriame tvarkomos užklausos į fiskalinės registracijos tarnybą. Šis tvarkytuvas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Pagal šią užklausą dokumentai siunčiami fiskalinės registracijos tarnybai ir iš jos grąžinamas atsakymas.
- **IsReadyFiscalDeviceRequest** – Šis prašymas naudojamas fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama fiskalinės registracijos paslaugai inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Fiskalinės jungties konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ Efr\\ Konfigūracijos\\ Jungtys\\ JungtisEFRSample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – leisti fiskalinės jungties nustatymus konfigūruoti iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
