---
title: SF fiksavimo sprendimo darbo sritis
description: Šiame straipsnyje pateikiama informacija apie SF fiksavimo sprendimo darbo sritį.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691000"
---
# <a name="invoice-capture-solution-workspace"></a>SF fiksavimo sprendimo darbo sritis

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>SF fiksavimo sprendimo peržiūros programa vieną šalia kitos

SF įvedimas į sistemą paprastai būna daug laiko reikalaujantis procesas, kuris yra skirtas klaidoms, nes klerkas, kad rinktų tinkamą informaciją, turi eiti keli priedų failai ir langai. Dokumentų peržiūros programa padės pagerinti jūsų darbo su SF patirtį, nes procesas bus paprastesnis, efektyvesnis ir tikslesnis.

Dokumentų peržiūros programa leidžia vartotojams tame pačiame lange atidaryti pradinį dokumentą ir atidaryti SF vieną šalia kitos. SF puslapyje yra užpildyta informacija, kuri gaunama iš originalaus SF dokumento. Peržiūros programa sukuria ryšį tarp SF puslapio laukų ir originalaus SF dokumento. Peržiūros programa padeda vartotojams rasti visas KLAIDAS, kurios yra SF puslapyje.

### <a name="open-the-side-by-side-viewer"></a>Atidaryti vieną šalia kitos peržiūros programą

Programoje Microsoft Dynamics 365 finansų galite atidaryti vieną šalia kitos peržiūros programą iš suvestinės puslapio sąrašo arba iš SF sąrašo puslapio. Taip pat galite jį atidaryti padvigubėdami (arba dukart spustelėdami) įrašą arba pasirinkdami SF numerį.

### <a name="using-the-side-by-side-viewer"></a>Vienos pusės peržiūros programos naudojimas

#### <a name="manually-review-an-invoice"></a>SF peržiūra rankiniu būdu

Importuotame SF dokumente gali reikėti peržiūrėti rankiniu būdu dėl klaidų arba įspėjimų. Vieną šalia kitos peržiūros programos dokumento antraštėje bus rodoma būsena **Importuota**, o dabartinė versija bus originali **versija**.

Norėdami pradėti peržiūrėti SF, pasirinkite Pradėti **peržiūrą**. Visi laukai tampa redaguojami. Laukas **Būsena** atnaujinama į **Peržiūrima**, o dabartinės **versijos laukas** atnaujinamas į Modifikuota **versija**.

#### <a name="view-and-work-with-messages"></a>Peržiūrėti ir dirbti su pranešimais

Vartotojai turi pradėti peržiūros procesą iš pranešimų srities. Klaidų pranešimai žymimi raudonais X, perspėjimo pranešimai yra žymimi trikampiu, o informaciniai pranešimai – apskritimu. Su pasitikėjimu susijusius pranešimus galima klasifikuoti kaip įspėjimus arba klaidas, atsižvelgiant į konfigūracijos grupės nustatytą ribą. Daugiau informacijos rasite SF fiksavimo [sprendimo konfigūracijos grupėse](invoice-capture-config-group.md).

Įspėjimų ir klaidų pranešimų galima nepaisyti pranešimų srityje, SF antraštėje arba SF eilutėse. Kai pranešimas ignoruojamas, jis neberodo kaip klaida arba perspėjimas, ir SF nepavyksta patikrinti.

- Norėdami nepaisyti pranešimų srities pranešimų srities, pasirinkite **Nepaisyti**. Norėdami iš naujo nustatyti pranešimą, kuris buvo ignoruotas, vėl pasirinkite **Nepaisyti**. Tada jo tipas pakeičiamas iš klaidos ar perspėjimo į informaciją.
- Norėdami nepaisyti pranešimų iš SF antraštės arba SF eilutės, lauke **pasirinkite** Nepaisyti. Pranešimo simbolis dingsta. Tačiau, ji vėl atsiras, jei pranešimas bus nustatytas iš naujo iš pranešimų srities.

Pranešimų, susijusių su SF antraštės laukais, pranešimų srityje pasirinkus pranešimą, žymeklis perkeliamas į atitinkamą antraštės skyriaus lauką.

#### <a name="proofread-and-edit-fields"></a>Redagavimo ir redagavimo laukai

Jei lauko vertė iš originalios SF perskaitoma naudojant optinį ženklų atpažinimą (OCR), lauke atsiranda simbolis. Jei pasirinksite simbolį, dokumentų peržiūros programa automatiškai didės ir išryškins vietą, iš kurios nuskaitoma lauko vertė, kad būtų galima patikrinti SF duomenis.

Norėdami iš naujo nustatyti pradinį dokumentų peržiūros programos parametrą, atlikite vieną iš šių veiksmų:

- Pasirinkite tą patį simbolį, kurį pasirinkote anksčiau.
- Pasirinkite mygtuką, esantį viršutiniame dešiniajame dokumentų peržiūros programos kampe.

Redaguokite laukus taip, kaip reikia. Redagavimas įrašomas automatiškai, kai žymeklis palieka lauką. Į dešinę nuo lauko esantis simbolis nurodo, kad laukas buvo atnaujintas rankiniu būdu. Atnaujinus puslapį, simbolis bus pašalintas.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>SF tikrinimas naujausiam pranešimui gauti

Redaguojant lauką, lauko vertė atnaujinama, bet nauji tikrinimo pranešimai nesugeneruojami. Norėdami gauti naujausias tikrinimo pranešimus, pasirinkite **Tikrinti**. Atnaujinami pranešimų srities, SF antraštės ir SF eilučių pranešimai.

#### <a name="complete-the-review"></a>Baigti peržiūrą

Norėdami baigti peržiūrą, pasirinkite Baigti **peržiūrą**. SF patvirtintos. Jei randama kokia nors klaida, dokumento būsena lieka **Peržiūrima** ir rodoma pranešimų juosta. Visi pranešimai, kas yra pranešimų srityje ir SF antraštėje bei eilutėse, automatiškai atnaujinami, kad būtų pateikta informacija apie nesėkmingo tikrinimo priežastis.

Kai visos blokavimo klaidos yra ištaisytos, peržiūrą galima užbaigti. Dokumento būsena atnaujinama į **Peržiūrėta**, todėl laukų redaguoti nebegalima. Galite iš naujo paleisti peržiūrą, dar kartą pasirinkdami **Pradėti** peržiūrą.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Generuoti laukiančią tiekėjo SF finansuose

Norėdami SIŲSTI SF dokumentą į prijungtą finansų aplinką, pasirinkite **Generuoti**. Jei SF sugeneruoti nepavyksta, pranešimų juostoje rodomas klaidos pranešimas.

#### <a name="void-an-invoice"></a>SF anuliuojama

Norėdami anuliuoti SF, pasirinkite **Anuliuoti**. Anuliuotos SF negalima peržiūrėti, bet jos nerodomas SF reikia **rankiniu būdu peržiūrimų** sąrašų.

### <a name="validation-logic"></a>Tikrinimo logika

Kai kurių vienas šalia kitos peržiūros programos pagrindinių laukų nėra SF išdėstymo duomenyse, bet jų reikia norint sugeneruoti laukiančias finansų SF. Šie laukai išvedami iš dabartinių SF išdėstymo duomenų ir finansų pagrindinių duomenų derinio.

Išvesti negalima laukuose: juridinis **subjektas**, **tiekėjo** kodas ir **prekės numeris**. Jos turi būti išvestos tokia tvarka. Jei lauko išvedimas nepavyksta, procesas sustabdomas.

1. **Juridinis subjektas** – juridinis subjektas išvestas pirmiausiai. Jei rasta juridinio subjekto aktyvi susiejimo taisyklė, juridinis subjektas išvedamas pagal įmonės pavadinimą ir įmonės adresą.
2. **Tiekėjo kodas** – tada tiekėjo kodas išvestas remiantis aktyvia susiejimo taisykle ir išvestinio juridinio subjekto bei tiekėjo pavadinimo ir tiekėjo adreso deriniu.
3. **Prekės numeris** – galiausiai, prekės pavadinimas išvedamas iš išdėstymo, remiantis šiais trimis informacijos tipais:

    - Sukonfigūruota susiejimo taisyklė
    - Išvestas juridinis subjektas
    - Išvestas tiekėjo kodas

Norėdami paleisti tikrinimą, vieną **šalia** kitos peržiūros programą pasirinkite Tikrinti. Šiuo metu tikrinimas atlieka šiuos tikrinimus:

- **Privalomas tikrinimas** – šis tikrinimas patikrina privalomus vienos pusės peržiūros programos laukus. Vartotojai gali pasirinkti, kurie laukai turi būti privalomi konfigūravimo **parametrų** puslapyje.
- **Patikimumo tikrinimo rezultatas** – vartotojai gali nustatyti perspėjimo ribinę vertę ir klaidos ribinę vertę, kad būtų nustatytas pasitikėjimo rezultatas. Šis tikrinimas susitelkia ties OCR patikimumo rezultatu, kuris yra žemiau tų ribinių verčių. Klaidos arba įspėjimo pranešimai bus rodomi remiantis tikrinimo rezultatu.
- **Juridinis** subjektas – šiuo čekiu tikrinama, ar juridinis subjektas yra finansuose. Jei juridinio subjekto finansų aplinkoje nėra, tikrinimas nepavyksta.

Kai pirmą kartą naudojama tarpinė **peržiūros** programa ir vartotojas pasirenka Tikrinti, vyksta išvedimo ir tikrinimo procesai. Jei SF yra tikslios, tikrinimo procesas vykdomas, kai vartotojas pasirenka Visą **peržiūrą**. Tai taip pat vykdoma, kai vartotojas pasirenka Generuoti **tiekėjo SF**.

Išvedimo procesas įvyksta prieš tikrinimo procesą ir visi įspėjimai ar klaidos gaunamos iš tikrinimo proceso. Finansuose bus registruojami perspėjimai ir klaidos.
