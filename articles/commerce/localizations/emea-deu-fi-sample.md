---
title: Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Vokietijai
description: Šioje temoje pateikta Vokietijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: ca747215a8dfb85237365880ad5bdd49e57ec949
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944693"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Vokietijai

[!include[banner](../includes/banner.md)]

Šioje temoje pateikta Vokietijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Siekiant patenkinti vietinius finansinius reikalavimus grynųjų pinigų registrams Vokietijoje, Vokietijos funkcionalume yra el. kasos aparato (EKA) ir išorinio Microsoft Dynamics 365 Commerce finansinio registravimo tarnybos pavyzdys. Pavyzdys išplečia finansinio [integravimo funkciją](fiscal-integration-for-retail-channel.md). Jis remiasi [EFR (elektroninio finansinio registro) sprendimu](https://www.efsta.eu/de/fiskalloesungen/deutschland) iš [EFSTA](https://www.efsta.eu/de/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR tarnyba turi būti laikoma "Retail Hardware" stotis arba atskirame kompiuteryje, kurį galima prijungti iš "Hardware" stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

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

        - TID
        - Operacijos pradžios data ir laikas
        - Operacijos pabaigos data ir laikas
        - Parašo skaitiklis
        - Tikrinti reikšmę
        - TSE serijos numeris

- **Kliento užsakymų registravimas finansinio registravimo tarnybose: registracijos procesas yra toks pats kaip pardavimo ir** grąžinimo grynaisiais pinigais ir grąžinimo procesas.
- **Operacijų, kurios apima dovanų korteles ir depozitus, registravimas: registracijos procesas yra toks pats kaip ir pardavimo ir** grąžinimo grynaisiais pinigais ir grąžinimo procesas.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Vartotojams pranešant apie finansinio registravimo triktis

Yra du būdai, kuriais finansinio registravimo tarnyba gali įspėti vartotojus apie finansinio registravimo metu triktį:

- Kvitų informacijos pranešimo lauke **spausdinkite papildomą** atsakymo informaciją.
- Rodyti pranešimus iš finansinių paslaugų kaip vartotojo pranešimus EKA.

    > [!NOTE]
    > Šiam pranešimų mechanizmui reikia, kad būtų įjungtas parametras Rodyti finansinių **registracijų** **pranešimus** "Connector" techninių profilių puslapyje.

#### <a name="printing-receipts"></a>Kvitų spausdinimas

Kvitų spausdinimas yra privalomas Vokietijoje. Visuose gavimuose turi būti bent ši informacija:

- Įmonės pavadinimas ir adresas
- Informacija apie prekes, įskaitant jų kainas ir kiekius
- Informacija apie gautus mokėjimus
- Informacija apie mokesčius, įskaitant bendras sumas pagal mokesčio tarifą
- Saugos duomenys:

    - TID
    - Operacijos pradžios data ir laikas
    - Operacijos pabaigos data ir laikas
    - Parašo skaitiklis
    - Tikrinti reikšmę
    - TSE serijos numeris

- Informacinis pranešimas

> [!NOTE]
> QR kodą taip pat galima išspausdinti kvituose. Nors QR kodas yra pasirinktinis, labai rekomenduojamas. Daugiau informacijos apie tai, kaip gauti QR kodą kaip finansinio registravimo tarnybos atsakymo dalį, žr. "EFR Guide DE" dokumentą, kuris paskelbtas \[\][EFSTA dokumentacijos](https://public.efsta.net/efr/) svetainėje.
>
> Kvitų **informacijos pranešimo lauke pateikiamas pranešimas iš finansinio registravimo** tarnybos. Pavyzdžiui, jei parašo įrenginys sulaužytas, kvite galima išspausdinti specialų tekstą.

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

**Uždarymo** pamainos operacija taip pat registruojama kaip nefinansinės operacijos finansinio registravimo paslaugoje naudojant **NFS** žymę.

### <a name="data-export-and-audit"></a>Duomenų eksportavimas ir auditas

Visas operacijas turi pasirašyti TSE, kad būtų užtikrintas jų vientisumas, autentiškumas ir užbaigtumas bei būtų išvengta įrašytų duomenų tvarkymo.

> [!WARNING]
> Galima naudoti tik patvirtintą TSE. Informacijos apie EFR sprendimo palaikomus EFR tipus ir modelius žr. dokumente "EFR Guide DE", kuris paskelbtas \[\][EFSTA dokumentacijos](https://public.efsta.net/efr/) svetainėje. Norėdami gauti daugiau informacijos, kaip pasirinkti ir įsigyti TSE, susisiekite [su](https://www.efsta.eu/at/kontakt) EFSTA.

Vokietijos įstatymai reikalauja DSFinV-K eksporto palaikymo. DSFinV-K eksportas gali būti suaktyvintas EFR sprendimas. Daugiau informacijos apie DSFinV-K eksportą ieškokite "EFR vadovas DE" dokumente, paskelbtame \[\][EFSTA dokumentacijos](https://public.efsta.net/efr/) svetainėje.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

Finansinio registravimo tarnyba palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainas. Todėl parduotuvių ir klientų parinktis Kainos su PVM turi būti **nustatyta** kaip **Taip**.

Finansinė tarnyba nepalaiko situacijų, kai tai pačiai operacijos eilutei taikomas daugiau nei vienas PVM kodas.

Finansinio integravimo sistema nepalaiko pardavimo pasiūlymų. Todėl šios operacijos nėra užregistruotos finansų tarnybose.

## <a name="set-up-commerce-for-germany"></a>Nustatyti Vokietijos "Commerce"

Šiame skyriuje aprašomi Vokietijos "Commerce" parametrai, kurie yra specifiniai ir rekomenduojami. Daugiau nustatymo informacijos ieškokite ["Commerce" pagrindinis](../index.md) puslapis.

Norėdami naudoti funkciją, būsią Vokietijai, turite nurodyti šiuos parametrus.

- Pirminiame juridinio subjekto adrese nustatykite **lauką Šalis/regionas** kaip **DEU** (Vokietija).
- Kiekvienos Vokietijoje įsikūrusios parduotuvės EKA funkcijų profilyje **nustatykite ISO kodo lauką** DE **·** (Vokietija).

Taip pat turite nurodyti šiuos Vokietijos parametrus. Baigę nustatymą būtinai vykdykite atitinkamas paskirstymo užduotis.

### <a name="set-up-vat-per-german-requirements"></a>Nustatyti PVM pagal Vokietijos reikalavimus

Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM priemones, ieškokite [PVM](../../finance/general-ledger/indirect-taxes-overview.md) peržiūra.

Pardavimo kvituose galite išspausdinti sutrumpintą PVM kodo kodą (pvz., "A" arba "B"). Kad ši funkcija būtų galima, nustatykite **PVM** kodų puslapyje **lauką Spausdinimo** kodas.

### <a name="set-up-stores"></a>Parduotuvių nustatykite

Puslapyje **Visos** parduotuvės atnaujinkite parduotuvės informaciją. Tiksliau nustatykite šiuos parametrus:

- Lauke **PVM grupė** nurodykite PVM grupę, kurią reikia naudoti pardavimams numatytojam klientui.
- Nustatykite **parinktį Kainos su PVM kaip** **Taip**.
- Nustatykite **įmonės** pavadinimą lauke Pavadinimas. Šis keitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės pavadinimas. Taip pat galite įtraukti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti mokesčio **identifikavimo numerio (TIN)** lauką kaip įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės identifikavimo numeris. Taip pat galite prie pardavimo kvito maketo pridėti įmonės identifikavimo numerį kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų kūrimas

Nustatyti EKA funkcijų šablonus. Kvitų **numeravimo "FastTab" nustatykite kvitų numeravimą, sukurdami arba atnaujindami pardavimo, pardavimo užsakymo ir** **grąžinimo** **·** **kvitų** operacijų tipų įrašus.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos **teksto puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atsikreipkite **dėmesį, kad lentelėje pateiktos kalbos ID, teksto ID ir teksto vertės** **yra tik** **pavyzdžiai**. Galite keisti juos, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas teksto ID vertės turi būti unikalios ir jos turi būti lygios arba **didesnės** 900001.

Šias EKA žymas įtraukite į **EKA** skyrių, kalbos **teksto** puslapyje.

| Kalbos ID | Teksto ID | Tekstas                                  |
|-------------|---------|---------------------------------------|
| en-JAV       | 900001  | QR kodas                               |
| en-JAV       | 900002  | Operacijos ID                        |
| en-JAV       | 900003  | Mažmeninės prekybos mokesčių spausdinimo kodas                 |
| en-JAV       | 900004  | Mokesčio suma (pardavimai)                    |
| en-JAV       | 900005  | Mokesčių pagrindas (pardavimas)                     |
| en-JAV       | 900006  | Operacijos pradžios data ir laikas           |
| en-JAV       | 900007  | Operacijos pabaigos data ir laikas             |
| en-JAV       | 900008  | Saugos elemento serijos numeris |
| en-JAV       | 900009  | Parašo skaitiklis                     |
| en-JAV       | 900010  | Tikrinti reikšmę                           |
| en-JAV       | 900011  | Informacinis pranešimas                          |

Pasirinktinių **laukų** puslapyje pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad antraštės teksto ID** reikšmės turi atitikti teksto ID **vertes**, kurias nurodėte kalbos **teksto** puslapyje.

| Pavadinimas                            | Tipas    | Vaizdo aprašo teksto ID |
|---------------------------------|---------|-----------------|
| QRCODE \_ DE                      | Gavimas | 900001          |
| OPERACIJOS \_ ID               | Gavimas | 900002          |
| RETAILPRINTCODE \_ DE             | Gavimas | 900003          |
| SALESTAMOUNT \_ DE              | Gavimas | 900004          |
| SALESTAXBASIS \_ DE               | Gavimas | 900005          |
| OPERACIJŲTARTDATETIME \_ DE DE    | Gavimas | 900006          |
| TRANSACTIONENDDATETIME \_ DE      | Gavimas | 900007          |
| SECURITYELEMENTSERIALNUMBER \_ DE | Gavimas | 900008          |
| PASIRAŠARAŠTINĖ \_ DE                 | Gavimas | 900009          |
| PASIRAŠYTI \_ DE                        | Gavimas | 900010          |
| INFOMESSAGE \_ DE                 | Gavimas | 900011          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kurie išvardyti ankstesnėje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Kiekvienam kvito formatui, kuris būtinas, pakeiskite lauko Spausdinti veikimo būdą **vertę** į Visada **spausdinti**.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

- **Antraštė:** Įtraukite šiuos laukus:

    - **Parduotuvės pavadinimo** **ir mokesčio ID** laukai, naudojami įmonės pavadinimui ir identifikavimo numeriui kvituose spausdinti. Taip pat galite įtraukti įmonės pavadinimą ir identifikavimo numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės** adresas, **data**, **laikas 24** val., **kvito** numeris ir registro **numerio** laukai.

- **Eilutės:** įtraukite šiuos laukus:

    - **Prekės pavadinimo** laukas
    - **Kiekio** laukas
    - **Visa kaina su mokesčio** lauku
    - **Mažmeninės prekybos mokesčių spausdinimo kodo laukas, naudojamas sutrumpintam kodui, atitinkančiam prekei** taikymą PVM kodą, išspausdinti

- **Poraštė:** įtraukite šiuos laukus:

    - Mokėjimo laukus, kad būtų išspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, į vieną maketo eilutę įtraukite **laukus Mokėjimo priemonės pavadinimas** ir Mokėjimo priemonės **suma**.
    - Mokesčių **išs pertraukos laukų** grupės laukai. Visi šios laukų grupės laukai turi būti išspausdinti vienoje atskiroje eilutėje.

        - **Mokesčio ID** laukas, kuris yra standartinis laukas, leidžiantis spausdinti kiekvieno PVM kodo PVM suvestinę. Laukas turi būti pridėtas prie naujos eilutės.
        - **Mokesčio** procento laukas, kuris yra standartinis laukas, naudojamas PVM kodo galiojamam mokesčio tarifui spausdinti.
        - **Mokesčių pagrindo (pardavimo) laukas, naudojamas spausdinant pvm kodo kvito bendrą** grynųjų pinigų pardavimo sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Mokesčio sumos (pardavimo) laukas, naudojamas spausdinant PVM kodo grynųjų pardavimo** kvitų mokesčių sumą.
        - **Mažmeninės prekybos mokesčių** spausdinimo kodo laukas, naudojamas sutrumpintam kodui, atitinkančiam PVM kodą, spausdinti.

    - Laukai, kuriuose yra iždo registravimo tarnybos pateikti saugiais operacijos duomenimis:

        - **Operacijos ID** laukas, kuris nurodo grynųjų pinigų operacijos numerį finansinio registravimo paslaugoje
        - **Operacijos pradžios datos ir laiko** laukas
        - **Operacijos pabaigos datos ir laiko** laukas
        - **Saugos elemento lauko serijos** numeris
        - **Parašo skaitiklio** laukas
        - **Tikrinimo vertės** laukas
        - **QR kodo laukas, naudojamas nuorodai į užregistruotas grynųjų** pinigų operacijas spausdinti QR kodo formoje

        > [!NOTE]
        > **QR kodo vertė** nuskaitoma iš finansinio registro atsakymo. EFR savo atsakyme grąžina QR kodą tik tada, jei EFR konfigūracijos atributų lauko vertė yra aprašyta **EFSTA** dokumentuose. QR kodo formatas **atributų** lauke, EFR konfigūracijoje, turi būti nustatytas kaip **BMP**.

    - **Informacinio** pranešimo laukas, kad pranešimai iš finansinių registracijų tarnybos galėtų būti rodomi kvituose. Pavyzdžiui, jei parašo įrenginys sulaužytas, kvite galima išspausdinti specialų tekstą.

Daugiau informacijos apie tai, kaip dirbti su gavimo formatais, ieškokite [Set up and design receipt formatus](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Nustatyti Finansų integravimą Vokietijai

Vokietijos finansinio registravimo tarnybos integravimo pavyzdys pagrįstas finansinio [integravimo funkcija ir yra mažmeninės prekybos SDK](fiscal-integration-for-retail-channel.md) dalis. Pavyzdys yra **sprendimų saugyklos src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra "Commerce" vykdymo laiko pratęsimas (CRT), ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Ankstesnę mažmeninės prekybos SDK versiją turite naudoti kūrėjo virtualioje mašinoje (VM) Microsoft Dynamics "Lifecycle Services" (LCS). Daugiau informacijos rasite Vokietijos [(senesnės veiklos) finansinio integravimo pavyzdžio diegimo](emea-deu-fi-sample-sdk.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite fiskalinės integracijos nustatymo veiksmus, aprašytus [Komercijos kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatyti fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Be to, atkreipkite dėmesį į fiskalinės registracijos proceso parametrus, [būdingus šiam fiskalinės registracijos tarnybos integravimo ėminiui](#set-up-the-registration-process).
1. [Nustatykite klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Mokesčių integravimo sistemos klaidų tvarkymo galimybės gali būti nevisiškai sulygiuotos su vietiniais finansiniais įstatymais.
    >
    > - Rekomenduojame finansinio registravimo proceso puslapyje palikti pasirinktį Tęsti dėl klaidos, kuri būtų išjungta, nes visos operacijos turi būti tinkamai užregistruotos, net jei pirmas bandymas registruoti finansinius **duomenis** **nesėkmingas**.
    > - Prieš įjungdami pasirinktį Praleisti arba Pažymėti kaip registruotą finansinio registravimo proceso puslapyje, šiuos finansinio registravimo proceso pakeitimus aptarkite su savo mokesčių konsultantu arba vietos **mokesčių** **·** **inspekcija**.

1. [Įgalinti neautomatinį atidėtų fiskalinės registracijos vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Nustatyti registracijos procesą

Norėdami įgalinti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte "Commerce" būstinę. Daugiau informacijos ieškokite [Set up fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite finansinio dokumento teikėjo ir finansinio jungties konfigūracijos failus:

    1. Atidaryti [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite teisingą išleidimo šakos versiją pagal savo SDK / programos versiją **[(pvz., leidimas / 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> Efr**.
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą konfigūracijos faile **Configurations \>\> DocumentProviders DocumentProviderFiscalEFRSampleGermany.xml (pvz., paleidimo** / [9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml) failas).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą **\> "Configurations \> Connectors ConnectorEFRSample.xml** (pvz., [išleidimo failą/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Šio finansinio integravimo pavyzdžio konfigūracijos failai yra šiuose LCS kūrėjo VM mažmeninės prekybos SDK aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.EFRSample \\ konfigūracijos \\ DocumentProviderFiscalEFRSampleGermany.xml
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

- **Mokėjimo priemonės tipo susiejimas – mokėjimo būdų susiejimas su atributo PayG (mokėjimų grupė) vertėmis užklausose,** **kurios** siunčiamos į fiskalinę tarnybą. Čia yra numatytasis susiejimas:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Pirmasis kiekvienos poros komponentas atitinka parduotuvei nustatytą mokėjimo būdą. Antrasis komponentas rodo atitinkamą mokėjimų grupę, kurią palaiko EFR finansinių registracijų tarnyba. Daugiau informacijos apie mokėjimų grupes, kurias EFR palaiko Vokietijoje, ieškokite [EFR](https://public.efsta.net/efr/) nuorodoje.

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

- **Įtraukti kliento duomenis – jei šis parametras įjungtas, užklausose į fiskalinę paslaugą bus pateikta kliento informacija, pvz., pavadinimai ir adresai, kai** klientas įtraukiamas į operaciją.
- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas – mokesčio procentų verčių, kurios nustatytos PVM kodams, susiejimas su** **atributo TaxG (mokesčių grupė) vertėmis užklausose, kurios siunčiamos į fiskalinę** tarnybą. Čia yra numatytasis susiejimas:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM mokesčių grupę, kurią palaiko EFR finansinio registravimo tarnyba. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Vokietijai, ieškokite [EFR](https://public.efsta.net/efr/) nuorodoje.

- **Dovanų kortelių ir depozitų mokesčių grupė – TaxG atributo vertė užklausose, kurios siunčiamos į fiskalinę paslaugą, atsižvelgiant į operacijas, kurias sudaro dovanų kortelės** **arba** depozitai. Čia yra numatytasis susiejimas:

    ```
    G
    ```

- **Neapmokestinimo PVM grupė – TaxG atributo vertė užklausose, kurios siunčiamos fiskalinei tarnybai, atsižvelgiant į operacijas, kurios neapmokestinamos** **mokesčių** įsipareigojimais. Čia yra numatytasis susiejimas:

    ```
    F
    ```

> [!NOTE]
> Numatytųjų duomenų susiejimo mokesčių parametrai yra atsakingi už mokesčių parametrų gretinimą sistemos ir mokesčių grupėse EFR paslaugoje. Mokesčių grupes kvituose galima spausdinti tik tada, jei pvm **kodų** puslapyje nustatytas **laukas Spausdinimo** kodas.

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis laikas milisekundiais, kurį fiskalinė jungtis lauks atsakymo iš** fiskalinių registracijų tarnybos.
- **Rodyti finansinio registravimo pranešimus** – ši vėliavėlė valdo, ar finansinių registracijų tarnybos grąžinimai turėtų būti rodomi operatoriui.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos rasite Vokietijos [(senesnės veiklos) finansinio integravimo pavyzdžio diegimo](emea-deu-fi-sample-sdk.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba [Dynamics 365 Commerce atsisiųskite](https://github.com/microsoft/Dynamics365Commerce.Solutions) sprendimų saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr.["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą **Dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ EFR.sln** ir sukurkite jį.
1. Diegti "Commerce" vykdyklės plėtinius:

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

    - Aplanke **Efr \\ HardwareStation \\ HardwareStation.EFR.Installer \\ talpyklos \\ debug \\ net461** raskite **HardwareStation.EFR.Installer diegimo** priemonės.
    - Paleiskite plėtinio diegimo programą iš komandų eilutės:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti ir paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio [paketus, atlikite nurodytus veiksmus.](fiscal-integration-sample-build-pipeline.md) **EFR build-pipeline.yml šablono JAML failą galima** rasti sprendimų saugyklos YAML_Files pardavimo galimybių **\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) aplanke.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Vokietijos finansinio registravimo tarnybos integravimo pavyzdys pagrįstas finansinio [integravimo funkcija ir yra mažmeninės prekybos SDK](fiscal-integration-for-retail-channel.md) dalis. Pavyzdys yra **sprendimų saugyklos src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra CRT plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos rasite Vokietijos [(senesnės veiklos) finansinio integravimo pavyzdžio diegimo](emea-deu-fi-sample-sdk.md) rekomendacijose. Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="crt-extension-design"></a>CRT plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, tikslas yra generuoti konkrečios paslaugos dokumentus ir tvarkyti atsakymus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

Yra viena dokumentų teikėjo užklausos apdorojimo programa **DocumentProviderEFRFiscalDEU.** Ši apdorojimo programa naudojama norint generuoti finansinio registravimo tarnybos finansinius dokumentus. Jis perimtas iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Jis grąžina su paslauga susijusius dokumentus, kurie turėtų būti užregistruoti fiskalinės registracijos tarnyboje.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest – ši užklausa grąžina atsakymą** kartu su išplėstiniais duomenimis.

#### <a name="configuration"></a>Konfigūravimas

Finansinio dokumento teikėjo konfigūracijos failas yra **src \\ FiscalIntegration \\ Efr konfigūracijų \\\\ DocumentProviders \\ DocumentProviderFiscalEFRSampleGermany.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo tikslas – įgalinti finansinio dokumento teikėjo parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra bendrauti su fiskalinės registracijos tarnyba.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EFRSample**. Ji naudoja HTTP protokolą dokumentams, kuriuos CRT sugeneruoja plėtinys, pateikti iždo registracijos tarnybai. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

**EFRHandler** užklausų apdorojimo programa yra registracijos tarnybos užklausų tvarkymo pradinis taškas. Ši apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į fiskalinės registracijos tarnybą ir pateikia iš jos atsakymą.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InicijuotiFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybai inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Fiskalinės jungties konfigūracijos failas yra **src \\ FiscalIntegration \\ Efr \\\\ Configurations \\ Connectors ConnectorEFRSample.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti fiskalinės jungties parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
