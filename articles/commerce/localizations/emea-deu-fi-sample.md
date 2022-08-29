---
title: Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Vokietijai
description: Šiame straipsnyje pateikta Vokietijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-05-29
ms.openlocfilehash: c3fdc0c378ad57300213357eccd50d817e06789a
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313947"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Vokietijai

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikta Vokietijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Siekiant patenkinti vietinius finansinius reikalavimus grynųjų pinigų registrams Vokietijoje, Dynamics 365 Commerce Vokietijos funkcionalume yra el. kasos aparato (EKA) ir išorinio finansinio registravimo tarnybos pavyzdys. Pavyzdys išplečia finansinio [integravimo funkciją](fiscal-integration-for-retail-channel.md). Jis remiasi [EFR (elektroninio finansinio registro)](https://www.efsta.eu/de/fiskalloesungen/deutschland)[sprendimu iš EFSTA](https://www.efsta.eu/de/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR tarnyba turi būti laikoma "Retail Hardware" stotis arba atskirame kompiuteryje, kurį galima prijungti iš "Hardware" stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra "Commerce" programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš EFSTA. Norėdami gauti informacijos apie tai, kaip gauti EFR sprendimą ir jį valdyti, susisiekite su [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Scenarijai

Šiuos scenarijus apima Vokietijos finansinių registracijų tarnybos integravimo pavyzdys.

### <a name="sales-operations"></a>Pardavimo operacijos

- **Grynųjų pinigų ir atliekamo pardavimo bei grąžinimo registravimas finansinio registravimo tarnybose:**

    Pardavimo operacijų registravimas apima šiuos veiksmus:

    1. Operacijos pradžios registravimas

        Kiekvienos operacijos pradžia užregistruojama techninės saugos elemente (TSE), kuris prijungtas prie EFR tarnybos. Užregistravimo metu TSE priskiria operacijos ID (TID).

    2. Operacijos pabaigos registracija

        Kai operacija pasibaigs EKA, ji užregistruojama naudojant tą patį TID, kuris buvo priskirtas registruojant operacijos pradžios operaciją. Tuo metu išsami operacijos informacija siunčiama į finansinio registravimo tarnybą. Šie duomenys apima pardavimo eilutės informaciją ir informaciją apie nuolaidas, mokėjimus ir mokesčius.

    3. Finansinių dokumentų registracijos tarnybos atsakymo fiksavimas

        Saugos duomenys gaunami iš TSE kaip atsakymo dalis ir išsaugomi kanalo duomenų bazės operacijoje. Saugos duomenis sudaro ši informacija:

        - Tid
        - Operacijos pradžios data ir laikas
        - Operacijos pabaigos data ir laikas
        - Parašo skaitiklis
        - Tikrinti reikšmę
        - TSE serijos numeris

- **Kliento užsakymų registravimas finansinio registravimo tarnybose:** registracijos procesas yra toks pats kaip pardavimo ir grąžinimo grynaisiais pinigais ir grąžinimo procesas.
- **Operacijų, kurios apima dovanų korteles ir depozitus, registravimas:** registracijos procesas yra toks pats kaip ir pardavimo ir grąžinimo grynaisiais pinigais ir grąžinimo procesas.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Vartotojams pranešant apie finansinio registravimo triktis

Yra du būdai, kuriais finansinio registravimo tarnyba gali įspėti vartotojus apie finansinio registravimo metu triktį:

- Kvitų informacijos pranešimo lauke spausdinkite **papildomą** atsakymo informaciją.
- Rodyti pranešimus iš finansinių paslaugų kaip vartotojo pranešimus EKA.

    > [!NOTE]
    > Šiam pranešimų mechanizmui reikia, kad **būtų įjungtas parametras** **Rodyti finansinių registracijų pranešimus** "Connector" techninių profilių puslapyje.

#### <a name="printing-receipts"></a>Kvitų spausdinimas

Kvitų spausdinimas yra privalomas Vokietijoje. Visuose gavimuose turi būti bent ši informacija:

- Įmonės pavadinimas ir adresas
- Informacija apie prekes, įskaitant jų kainas ir kiekius
- Informacija apie gautus mokėjimus
- Informacija apie mokesčius, įskaitant bendras sumas pagal mokesčio tarifą
- Saugos duomenys:

    - Tid
    - Operacijos pradžios data ir laikas
    - Operacijos pabaigos data ir laikas
    - Parašo skaitiklis
    - Tikrinti reikšmę
    - TSE serijos numeris

- Informacinis pranešimas

> [!NOTE]
> QR kodą taip pat galima išspausdinti kvituose. Nors QR kodas yra pasirinktinis, labai rekomenduojamas. Daugiau informacijos apie tai, kaip gauti QR kodą kaip finansinio registravimo tarnybos atsakymo dalį, ieškokite dokumente "EFR Guide \[DE\][", kuris paskelbtas EFSTA dokumentacijos](https://public.efsta.net/efr/) svetainėje.
>
> Kvitų **informacijos** pranešimo lauke pateikiamas pranešimas iš finansinio registravimo tarnybos. Pavyzdžiui, jei parašo įrenginys sulaužytas, kvite galima išspausdinti specialų tekstą.

#### <a name="voided-suspended-and-recalled-transactions"></a>Anuliuotos, sustabdytos ir atšauktos operacijos

- Anuliuota operacija užregistruojama kaip prašymas atleisti operaciją iš finansinių registracijų tarnybos.
- Sulaikyta operacija užregistruojama kaip prašymas atleisti operaciją finansinio registravimo tarnybose.
- Sulaikytos operacijos atšaukimas registruojamas kaip naujos operacijos pradžia finansinių registracijų tarnybose.

### <a name="non-sales-transactions-and-shift-closing"></a>Ne pardavimo operacijos ir pamainos uždarymas

Šios ne pardavimo operacijos registruojamos kaip nefinansinės operacijos finansinio registravimo paslaugos metu, naudojant **NFS** žymę:

- Deklaruoti pradinę sumą
- Nefiksuotas įrašas
- Mokėjimo priemonės šalinimas
- Pinigų įnešimas į kasą
- Inkasavimas
- Pajamų sąskaitos
- Išlaidų sąskaitos

Uždarymo **pamainos** operacija taip pat registruojama kaip nefinansinės operacijos finansinio registravimo paslaugoje naudojant **NFS** žymę.

### <a name="data-export-and-audit"></a>Duomenų eksportavimas ir auditas

Visas operacijas turi pasirašyti TSE, kad būtų užtikrintas jų vientisumas, autentiškumas ir užbaigtumas bei būtų išvengta įrašytų duomenų tvarkymo.

> [!WARNING]
> Galima naudoti tik patvirtintą TSE. Informacijos apie EFR sprendimo palaikomus EFR tipus ir modelius žr. dokumente "EFR Guide \[DE\][", kuris paskelbtas EFSTA dokumentacijos](https://public.efsta.net/efr/) svetainėje. Norėdami gauti daugiau informacijos, kaip pasirinkti ir įsigyti TSE, susisiekite su [EFSTA](https://www.efsta.eu/at/kontakt).

Vokietijos įstatymai reikalauja DSFinV-K eksporto palaikymo. DSFinV-K eksportas gali būti suaktyvintas EFR sprendimas. Daugiau informacijos apie DSFinV-K eksportą ieškokite "EFR guide \[DE\]" [dokumente, paskelbtame EFSTA dokumentacijos](https://public.efsta.net/efr/) svetainėje.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

Finansinio registravimo tarnyba palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainas. Todėl parduotuvių **ir klientų parinktis** Kainos su PVM turi **būti** nustatyta kaip Taip.

Finansinė tarnyba nepalaiko situacijų, kai tai pačiai operacijos eilutei taikomas daugiau nei vienas PVM kodas.

Finansinio integravimo sistema nepalaiko pardavimo pasiūlymų. Todėl šios operacijos nėra užregistruotos finansų tarnybose.

## <a name="set-up-commerce-for-germany"></a>Nustatyti Vokietijos "Commerce"

Šiame skyriuje aprašomi Vokietijos "Commerce" parametrai, kurie yra specifiniai ir rekomenduojami. Daugiau nustatymo informacijos ieškokite " [Commerce" pagrindinis puslapis](../index.md).

Norėdami naudoti funkciją, būsią Vokietijai, turite nurodyti šiuos parametrus.

- Pirminiame juridinio subjekto adrese nustatykite lauką **Šalis/regionas** kaip **DEU** (Vokietija).
- Kiekvienos Vokietijoje įsikūrusios parduotuvės EKA funkcijų profilyje nustatykite **ISO kodo lauką** **DE** (Vokietija).

Taip pat turite nurodyti šiuos Vokietijos parametrus. Baigę nustatymą būtinai vykdykite atitinkamas paskirstymo užduotis.

### <a name="set-up-vat-per-german-requirements"></a>Nustatyti PVM pagal Vokietijos reikalavimus

Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM priemones, ieškokite [PVM peržiūra.](../../finance/general-ledger/indirect-taxes-overview.md)

Pardavimo kvituose galite išspausdinti sutrumpintą PVM kodo kodą (pvz., "A" arba "B"). Kad ši funkcija būtų galima, nustatykite **PVM** kodų puslapyje lauką **Spausdinimo** kodas.

### <a name="set-up-stores"></a>Parduotuvių nustatykite

**Puslapyje Visos parduotuvės** atnaujinkite parduotuvės informaciją. Tiksliau nustatykite šiuos parametrus:

- Lauke PVM **grupė nurodykite** PVM grupę, kurią reikia naudoti pardavimams numatytojam klientui.
- Nustatykite **parinktį Kainos su PVM** kaip **Taip**.
- Nustatykite **įmonės** pavadinimą lauke Pavadinimas. Šis keitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės pavadinimas. Taip pat galite įtraukti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti mokesčio **identifikavimo numerio (TIN)** lauką kaip įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės identifikavimo numeris. Taip pat galite prie pardavimo kvito maketo pridėti įmonės identifikavimo numerį kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų nustatymas

Nustatyti EKA funkcijų šablonus. Kvitų **numeravimo** "FastTab" nustatykite kvitų **numeravimą**, sukurdami arba atnaujindami pardavimo, **pardavimo užsakymo** ir grąžinimo **kvitų** operacijų tipų įrašus.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos teksto **puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atkreipkite dėmesį **, kad** lentelėje **pateiktos kalbos ID,** **teksto ID** ir teksto vertės yra tik pavyzdžiai. Juos galite pakeisti, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas **teksto ID** vertės turi būti unikalios ir turi būti lygios arba didesnės nei 900001.

Šias EKA žymas įtraukite į **EKA** skyrių, kalbos **teksto** puslapyje.

| Kalbos ID | Teksto ID | Tekstas                                  |
|-------------|---------|---------------------------------------|
| lt       | 900001  | QR kodas                               |
| lt       | 900002  | Operacijos ID                        |
| lt       | 900003  | Mažmeninės prekybos mokesčių spausdinimo kodas                 |
| lt       | 900004  | Mokesčio suma (pardavimai)                    |
| lt       | 900005  | Mokesčių pagrindas (pardavimas)                     |
| lt       | 900006  | Operacijos pradžios data ir laikas           |
| lt       | 900007  | Operacijos pabaigos data ir laikas             |
| lt       | 900008  | Saugos elemento serijos numeris |
| lt       | 900009  | Parašo skaitiklis                     |
| lt       | 900010  | Tikrinti reikšmę                           |
| lt       | 900011  | Informacinis pranešimas                          |

Pasirinktinių **laukų puslapyje** pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite dėmesį **, kad antraštės teksto ID** reikšmės turi **atitikti teksto ID** vertes, kurias nurodėte kalbos **teksto** puslapyje.

| Vardas                            | Tipas    | Vaizdo aprašo teksto ID |
|---------------------------------|---------|-----------------|
| QRCODE\_ DE                      | Gavimas | 900001          |
| OPERACIJOS ID\_               | Gavimas | 900002          |
| RETAILPRINTCODE\_ DE             | Gavimas | 900003          |
| SALESTAMOUNT\_ DE              | Gavimas | 900004          |
| SALESTAXBASIS\_ DE               | Gavimas | 900005          |
| OPERACIJŲTARTDATETIME\_ DE DE    | Gavimas | 900006          |
| TRANSACTIONENDDATETIME\_ DE      | Gavimas | 900007          |
| SECURITYELEMENTSERIALNUMBER\_ DE | Gavimas | 900008          |
| PASIRAŠARAŠTINĖ\_ DE                 | Gavimas | 900009          |
| PASIRAŠYTI\_ DE                        | Gavimas | 900010          |
| INFOMESSAGE\_ DE                 | Gavimas | 900011          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kurie išvardyti ankstesnėje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Kiekvieno kvito formato atveju pakeiskite lauko Spausdinti veikimo būdą vertę **į** Visada **spausdinti**.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

- **Antraštė:** Įtraukite šiuos laukus:

    - **Parduotuvės pavadinimo** ir **mokesčio ID** laukai, naudojami įmonės pavadinimui ir identifikavimo numeriui kvituose spausdinti. Taip pat galite įtraukti įmonės pavadinimą ir identifikavimo numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės adresas**, **data**, **laikas 24 val**., **kvito numeris** ir registro **numerio** laukai.

- **Eilutės:** įtraukite šiuos laukus:

    - **Prekės pavadinimo** laukas
    - **Kiekio** laukas
    - **Visa kaina su mokesčio lauku**
    - **Mažmeninės prekybos mokesčių** spausdinimo kodo laukas, naudojamas sutrumpintam kodui, atitinkančiam prekei taikymą PVM kodą, išspausdinti

- **Poraštė:** įtraukite šiuos laukus:

    - Mokėjimo laukus, kad būtų išspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, į vieną maketo **eilutę įtraukite** **laukus** Mokėjimo priemonės pavadinimas ir Mokėjimo priemonės suma.
    - Mokesčių išs **pertraukos laukų grupės** laukai. Visi šios laukų grupės laukai turi būti išspausdinti vienoje atskiroje eilutėje.

        - **Mokesčio ID** laukas, kuris yra standartinis laukas, leidžiantis spausdinti kiekvieno PVM kodo PVM suvestinę. Laukas turi būti pridėtas prie naujos eilutės.
        - **Mokesčio procento** laukas, kuris yra standartinis laukas, naudojamas PVM kodo galiojamam mokesčio tarifui spausdinti.
        - **Mokesčių pagrindo (pardavimo)** laukas, naudojamas spausdinant pvm kodo kvito bendrą grynųjų pinigų pardavimo sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Mokesčio sumos (pardavimo)** laukas, naudojamas spausdinant PVM kodo grynųjų pardavimo kvitų mokesčių sumą.
        - **Mažmeninės prekybos mokesčių** spausdinimo kodo laukas, naudojamas sutrumpintam kodui, atitinkančiam PVM kodą, spausdinti.

    - Laukai, kuriuose yra iždo registravimo tarnybos pateikti saugiais operacijos duomenimis:

        - **Operacijos ID** laukas, kuris nurodo grynųjų pinigų operacijos numerį finansinio registravimo paslaugoje
        - **Operacijos pradžios datos ir laiko** laukas
        - **Operacijos pabaigos datos ir laiko** laukas
        - **Saugos elemento lauko serijos** numeris
        - **Parašo skaitiklio** laukas
        - **Tikrinimo vertės** laukas
        - **QR kodo** laukas, naudojamas nuorodai į užregistruotas grynųjų pinigų operacijas spausdinti QR kodo formoje

        > [!NOTE]
        > QR **kodo vertė** nuskaitoma iš finansinio registro atsakymo. EFR savo atsakyme grąžina QR **kodą** tik tada, jei EFR konfigūracijos atributų lauko vertė yra aprašyta EFSTA dokumentuose. QR kodo formatas atributų **lauke**, EFR konfigūracijoje, turi būti nustatytas kaip **BMP**.

    - **Informacinio** pranešimo laukas, kad pranešimai iš finansinių registracijų tarnybos galėtų būti rodomi kvituose. Pavyzdžiui, jei parašo įrenginys sulaužytas, kvite galima išspausdinti specialų tekstą.

Daugiau informacijos apie tai, kaip dirbti su kvitų formatais, ieškokite [Gavimo kvitų formatų nustatymas ir kūrimas](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Nustatyti Finansų integravimą Vokietijai

Vokietijos finansinio registravimo tarnybos integravimo pavyzdys pagrįstas finansinio [integravimo funkcija ir](fiscal-integration-for-retail-channel.md) yra "Commerce SDK" dalis. Pavyzdys yra sprendimų saugyklos **src\\ FiscalIntegration\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas, kuris yra "Commerce Runtime (CRT) plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie "Commerce SDK" naudojimą, [žr. "Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ir nustatykite nepriklausomos pakuotės SDK pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Vokietijos finansinių registracijų tarnybos integravimo pavyzdys yra "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba senesnę versiją, reikia naudoti ankstesnę "Retail SDK" versiją programavimo virtualiojoje kompiuteryje (VM) Microsoft Dynamics ciklo tarnybose (LCS). Daugiau informacijos ieškokite Vokietijos [(senesnės veiklos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-deu-fi-sample-sdk.md).

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite finansinio registravimo procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Be to, pateikite pastabą apie finansinio registravimo proceso parametrus, bvz [., šios finansinio registravimo tarnybos integravimo pavyzdį](#set-up-the-registration-process).
1. [Nustatyti klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Mokesčių integravimo sistemos klaidų tvarkymo galimybės gali būti nevisiškai sulygiuotos su vietiniais finansiniais įstatymais.
    >
    > - Rekomenduojame **finansinio** **registravimo** proceso puslapyje palikti pasirinktį Tęsti dėl klaidos, kuri būtų išjungta, nes visos operacijos turi būti tinkamai užregistruotos, net jei pirmas bandymas registruoti finansinius duomenis nesėkmingas.
    > - Prieš įjungdami **pasirinktį Praleisti** **·** **arba** Pažymėti kaip registruotą finansinio registravimo proceso puslapyje, šiuos finansinio registravimo proceso pakeitimus aptarkite su savo mokesčių konsultantu arba vietos mokesčių inspekcija.

1. [Įgalinkite neautomatinį atidėtos finansinio registravimo vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatyti registravimo procesą

Norėdami įjungti registravimo procesą, atlikite šiuos veiksmus norėdami nustatyti "Commerce Headquarters". Daugiau informacijos rasite "Commerce [" kanalų finansinio integravimo nustatykite](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųsti finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus:

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją.
    1. Atidaryti **src \> FiscalIntegration \> Efr**.
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą konfigūracijos faile **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml**.
    1. Atsisiųskite finansinio jungties konfigūracijos failą konfigūracijos **jungčių \>\> connectorEFRSample.xml.**

    > [!NOTE]
    > Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra toliau esančiuuose "Retail" SDK, esantis LCS programuotojo VM, aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk\\ SampleExtensions CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\\\ konfigūracijos\\ DocumentProviderFiscalEFRSampleGermany.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ extension.EFRSample\\ Configuration\\ ConnectorEFRSample.xml

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite pasirinktį **Įgalinti finansų integravimą** kaip **Taip**.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymą "Fiscal integration \> Fiscal"** dokumentų teikėjai ir įkelkite anksčiau atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce Channel" \> nustatymą "Fiscal integration \> Fiscal \>" jungtis ir įkelkite anksčiau atsisiųstą "Fiscal** Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" funkcinius profilius**. Sukurti naują jungties funkcinį profilį. Pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį. Pagal reikia [atnaujinti duomenų susiejimo](#default-data-mapping) parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**. Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją atnaujinkite](#fiscal-connector-settings) jungties parametrus.
1. Eikite į " **Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" jungties grupes**. Sukurkite naują anksčiau sukurto jungties funkcinių profilių finansinių jungčių grupę.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" registracijos procesus**. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso "** FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotyje, prie kurios bus prijungta iždo registracijos tarnyba. **"FastTab" Iždo išoriniuose** įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
1. Atidarykite paskirstymo grafiką (**"Retail and Commerce Retail ir Commerce \> IT \> Distribution"** grafiką) **ir pasirinkite užduotis 1070** **ir 1090**, kad duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Mokėjimo priemonės tipo** susiejimas – mokėjimo būdų susiejimas **su atributo PayG** (mokėjimų grupė) vertėmis užklausose, kurios siunčiamos į fiskalinę tarnybą. Čia yra numatytasis susiejimas:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Pirmasis kiekvienos poros komponentas atitinka parduotuvei nustatytą mokėjimo būdą. Antrasis komponentas rodo atitinkamą mokėjimų grupę, kurią palaiko EFR finansinių registracijų tarnyba. Daugiau informacijos apie mokėjimų grupes, kurias EFR palaiko Vokietijai, ieškokite [EFR nuorodoje](https://public.efsta.net/efr/).

    Mokėjimo metodų pavyzdžio susiejimas atitinka parduotuvės mokėjimo metodus, kurie sukonfigūruoti standartiniuose demonstraciniai duomenyse.

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
    | 11             | Ne vietiniai čekiai    |

    Todėl turite modifikuoti pavyzdžio susiejimą pagal mokėjimo metodus, kurie sukonfigūruoti jūsų programoje.

- **Įtraukti kliento duomenis** – jei šis parametras įjungtas, užklausose į fiskalinę paslaugą bus pateikta kliento informacija, pvz., pavadinimai ir adresai, kai klientas įtraukiamas į operaciją.
- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas –** mokesčio procentų verčių, kurios nustatytos PVM kodams, susiejimas su atributo TaxG **(mokesčių grupė)** vertėmis užklausose, kurios siunčiamos į fiskalinę tarnybą. Čia yra numatytasis susiejimas:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM mokesčių grupę, kurią palaiko EFR finansinio registravimo tarnyba. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Vokietijai, ieškokite [EFR nuorodoje](https://public.efsta.net/efr/).

- **Dovanų kortelių ir depozitų mokesčių grupė –** TaxG **atributo vertė užklausose, kurios siunčiamos į fiskalinę paslaugą, atsižvelgiant į operacijas**, kurias sudaro dovanų kortelės arba depozitai. Čia yra numatytasis susiejimas:

    ```
    G
    ```

- **Neapmokestinimo PVM grupė** – **TaxG** atributo vertė užklausose, kurios siunčiamos fiskalinei tarnybai, atsižvelgiant į operacijas, kurios neapmokestinamos mokesčių įsipareigojimais. Čia yra numatytasis susiejimas:

    ```
    F
    ```

> [!NOTE]
> Numatytųjų duomenų susiejimo mokesčių parametrai yra atsakingi už mokesčių parametrų gretinimą sistemos ir mokesčių grupėse EFR paslaugoje. Mokesčių grupes kvituose galima spausdinti tik tada, jei **pvm** kodų puslapyje nustatytas **laukas Spausdinimo** kodas.

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis** laikas milisekundiais, kurį fiskalinė jungtis lauks atsakymo iš fiskalinių registracijų tarnybos.
- **Rodyti finansinio registravimo pranešimus** – ši vėliavėlė valdo, ar finansinių registracijų tarnybos grąžinimai turėtų būti rodomi operatoriui.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!NOTE]
> - Vokietijos finansinių registracijų tarnybos integravimo pavyzdys yra "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Daugiau informacijos ieškokite Vokietijos [(senesnės veiklos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-deu-fi-sample-sdk.md).
> - Jūsų aplinkoje įdiegti "Commerce" pavyzdžiai nėra automatiškai atnaujinami, kai taikote "Commerce" komponentų aptarnavimo arba kokybės naujinimus. Reikiamus pavyzdžius turite atnaujinti neautomatiniu būdu.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą Dynamics365Commerce.Solutions **FiscalIntegration\\ EFR.sln\\ ir sukurkite\\ jį.**
1. Diegti "Commerce" vykdyklės plėtinius:

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

Vokietijos finansinio registravimo tarnybos integravimo pavyzdys pagrįstas finansinio [integravimo funkcija ir](fiscal-integration-for-retail-channel.md) yra "Commerce SDK" dalis. Pavyzdys yra sprendimų saugyklos **src\\ FiscalIntegration\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas CRT, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie "Commerce SDK" naudojimą, [žr. "Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md)[ir nustatykite nepriklausomos pakuotės SDK pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Vokietijos finansinių registracijų tarnybos integravimo pavyzdys yra "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Daugiau informacijos ieškokite Vokietijos [(senesnės veiklos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-deu-fi-sample-sdk.md).

### <a name="crt-extension-design"></a>CRT plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti atsakymus iš fiskalinių registracijų tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

Yra viena dokumentų teikėjo užklausos apdorojimo programa **DocumentProviderEFRFiscalDEU**. Ši apdorojimo programa naudojama norint generuoti finansinio registravimo tarnybos finansinius dokumentus. Jis perimtas iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas paslaugai konkretus dokumentas, kuris turi būti užregistruotas finansinio registravimo tarnybose.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – ši užklausa grąžina atsakymą kartu su išplėstiniais duomenimis.

#### <a name="configuration"></a>Konfigūracija

Finansinio dokumento **teikėjo konfigūracijos failas yra src\\ FiscalIntegration\\ Efr\\ konfigūracijų\\ DocumentProviders\\ DocumentProviderFiscalEFRSampleGermany.xml**[Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinio dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su finansinių registracijų tarnyba.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EFRSample**. Ji naudoja HTTP protokolą dokumentams, kuriuos sugeneruoja CRT plėtinys, pateikti iždo registracijos tarnybai. Jis taip pat tvarko atsakymus, gautus iš finansinio registravimo tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**EFRHandler užklausos** apdorojimo programa yra iždo registracijos tarnybos užklausų tvarkymo įvesties taškas. Ši apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

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
