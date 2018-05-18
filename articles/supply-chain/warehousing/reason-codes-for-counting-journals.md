---
title: "Atsargų skaičiavimo priežasčių kodai"
description: "Šioje temoje aprašoma, kaip nustatyti ir taikyti atsargų skaičiavimo priežasčių kodus."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe01425fa236655731e6e0723f3a1e57c05035cc
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="reason-codes-for-inventory-counting"></a>Atsargų skaičiavimo priežasčių kodai

[!include [banner](../includes/banner.md)]

Priežasčių kodai suteikia galimybę analizuoti skaičiavimo procesą rezultatus ir visus to proceso metu įvykusius neatitikimus. Galite nurodyti skaičiavimo priežastį, pvz., sugadintas padėklas arba atsargų koregavimas, pagal atsargų pavyzdžius.

## <a name="recommendation"></a>Rekomendacija

Prieš nustatant sistemą rekomenduojame nustatyti darbo su priežasčių kodais strategiją. Pavyzdžiui, pabandykite atsakyti į toliau nurodytus klausimus.

- Ar sandėliuose priežasčių kodai turėtų būti privalomi?
- Ar kai kuriose prekėse priežasčių kodai turėtų būti privalomi, ar pasirenkami?
- Kiek priežasčių kodų jums reikia?
- Kaip brūkšninių kodų skaitytuvų vartotojai turėtų naudoti priežasčių kodus? Ar priežasčių kodai turėtų būti iš anksto pasirenkami, privalomi arba neredaguojami?
- Ar sandėlio darbuotojams reikalingi skirtingų tipų priežasčių kodai mobiliuosiuose skaitytuvuose? Jei atsakymas teigiamas, galite kurti daugiau meniu elementų ir juos priskirti skirtingiems žmonėms.

## <a name="where-reason-codes-apply"></a>Kur taikomi priežasčių kodai

Galite kurti kelias priežasčių kodų strategijas ir kiekvienai priežasčių kodų strategijai galite priskirti dvi skaičiavimo priežasčių kodų strategijas. Skaičiavimo priežasčių kodų strategijas galima naudoti sandėlio lygiu arba prekės lygiu.

## <a name="set-up-reason-code-policies"></a>Priežasčių kodų strategijų nustatymas

1. Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Atsargos** \> **Skaičiavimo priežasčių kodų strategijos** ir sukurkite naują priežasčių kodų strategiją.
2. Lauke **Skaičiavimo priežasties kodo tipas** pasirinkite **Privalomas** arba **Pasirinktinis**, norėdami nurodyti, ar priežasties kodo pasirinkimas yra pasirinktinis, ar privalomas veiksmas viename iš toliau nurodytų skaičiavimo žurnalų.

    - Ciklo skaičiavimas (mobilusis įrenginys)
    - Vietos skaičiavimas (mobilusis įrenginys)
    - Ribinės reikšmės skaičiavimas (mobilusis įrenginys)
    - Koregavimo taikymas (mobilusis įrenginys)
    - Koregavimo atšaukimas (mobilusis įrenginys)
    - Žurnalo skaičiavimas (raiškusis klientas)

Taip pat galite nustatyti atskirų sandėlių ir produktų priežasčių kodus. Nustatant produktų priežasčių kodus galima nepaisyti sandėlių sąrankos.

## <a name="mandatory-reason-codes"></a>Privalomi priežasčių kodai

Jei sandėlių arba prekių priežasčių kodų konfigūracijoje nustatytas parametras **Privalomas**, žurnalo skaičiavimo negalima atlikti ir uždaryti, kol nepateiktas priežasties kodas.

### <a name="set-up-reason-codes-for-warehouses"></a>Sandėlių priežasčių kodų nustatymas

1. Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Atsargų paskirstymas** \> **Sandėliai**.
2. Skirtuko **Sandėlis** lauke **Skaičiavimo priežasčių kodų strategija** pasirinkite vieną iš toliau nurodytų parinkčių.

    - **Tuščia** – nustatytas prekės parametras naudojamas nustatant, ar produkto žurnalų skaičiavimas yra privalomas.
    - **Privalomas** – priežasties kodas yra visada privalomas skaičiuojant sandėlio žurnalus.
    - **Pasirinktinis** – priežasties kodas nėra privalomas skaičiuojant sandėlio žurnalus.

### <a name="set-up-reason-codes-for-products"></a>Produktų priežasčių kodų nustatymas

1. Pasirinkite **Produkto informacijos valdymas** \> **Produktai** \> **Išleisti produktai**.
2. Skirtuke **Produktas** pasirinkite **Skaičiavimo priežasčių kodų strategija**, tada pasirinkite vieną iš toliau nurodytų parinkčių.

    - **Tuščia** – nustatytas sandėlio parametras naudojamas nustatant, ar produkto žurnalų skaičiavimas yra privalomas.
    - **Privalomas** – priežasties kodas yra visada privalomas skaičiuojant produkto žurnalus. Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.
    - **Pasirinktinis** – priežasties kodas nėra privalomas skaičiuojant produkto žurnalus. Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.

### <a name="use-reason-codes-in-counting-journals"></a>Priežasčių kodų naudojimas skaičiavimo žurnaluose

Skaičiavimo žurnale galite įtraukti toliau nurodytų tipų skaičiavimo priežasčių kodus.

- Ciklo skaičiavimas
- Vietos skaičiavimas
- Ribinės reikšmės skaičiavimas
- Koregavimo taikymas
- Koregavimo atšaukimas

Priežasčių kodai įtraukiami į žurnalo eilutes tipo **Skaičiavimo žurnalas** skaičiavimo žurnaluose.

1. Pasirinkite **Atsargų valdymas** \> **Žurnalo įrašai** \> **Prekės skaičiavimas** \> **Skaičiavimas**.
2. Skaičiavimo žurnalo eilutės informacijos lauke **Skaičiavimo priežasties kodas** pasirinkite parinktį.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Įrašytos skaičiavimo retrospektyvos peržiūra pagal priežasčių kodus

- Pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Skaičiavimo retrospektyva**, tada lauke **Skaičiavimo priežasties kodas** peržiūrėkite skaičiavimo retrospektyvą, kuri buvo įrašyta naudojant priežasties kodą.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Priežasties kodo naudojimas kiekiui koreguoti

1. Puslapyje **Turimos atsargos** pasirinkite **Koreguoti kiekį**. Puslapį **Turimos atsargos** galite atidaryti keliais būdais. Pavyzdžiui, pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Turimos atsargos**.
2. Pasirinkite **Koreguoti kiekį**, tada lauke **Skaičiavimo priežasties kodas** pasirinkite priežasties kodą.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementų priežasčių kodų konfigūravimas

Mobiliojo įrenginio meniu elemente galite konfigūruoti bet kokio tipo skaičiavimo priežasčių kodus. Mobiliojo įrenginio meniu elemento konfigūracija apima toliau nurodytą informaciją.

- Informacija apie tai, ar atliekant skaičiavimą priežasties kodas rodomas darbuotojui, kuriam priklauso mobilusis įrenginys.
- Numatytasis priežasties kodas, rodomas mobiliojo įrenginio meniu elemente.
- Informacija apie tai, ar vartotojas gali redaguoti priežasties kodą.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Priežasčių kodų nustatymas mobiliajame įrenginyje

1. Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**.
2. Skirtuke **Ciklo skaičiavimas** pasirinkite **Ciklo skaičiavimas**.
3. Lauke **Numatytasis skaičiavimo priežasties kodas** nustatykite numatytąjį priežasties kodą, kuris turi būti įrašomas, kai skaičiavimas atliekamas naudojant mobiliojo įrenginio meniu elementą.
4. Lauke **Rodyti skaičiavimo priežasties kodą** pasirinkite **Eilutė**, kad įrašius kiekvieną nuokrypį būtų rodomas priežasties kodas. Taip pat galite pasirinkti **Slėpti**, jei priežasties kodas neturėtų būti rodomas.
5. Nustatykite parinkties **Redaguoti skaičiavimo priežasties kodą** reikšmę **Taip** arba **Ne**. Jei nustatote šios parinkties reikšmę **Taip**, darbuotojas gali redaguoti priežasties kodą, kai atliekant skaičiavimą jis rodomas mobiliajame įrenginyje.

> [!NOTE]
> Mygtuką **Ciklo skaičiavimas** galima įjungti bet kuriame mobiliojo įrenginio meniu elemente, kuriame galima atlikti skaičiavimą. Pavyzdžiai: vietos skaičiavimo, vartotojo nurodyto darbo ir sistemos nurodyto darbo meniu elementai.

## <a name="cycle-count-approvals"></a>Ciklo skaičiavimo patvirtinimai

Prieš patvirtinant skaičiavimą, vartotojas gali keisti priežasties kodą, susietą su skaičiavimu. Patvirtinus skaičiavimą, priežasties kodas įvedamas skaičiavimo žurnalo eilutėse.

### <a name="modify-cycle-count-approvals"></a>Ciklo skaičiavimo patvirtinimų keitimas

1. Pasirinkite **Sandėlio valdymas** \> **Ciklo skaičiavimas** \> **Peržiūros laukiantis ciklo skaičiavimo darbas**.
2. Pasirinkite **Ciklo skaičiavimas**, tada lauke **Priežasties kodas** pasirinkite naują priežasties kodą.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Procesų Koregavimo taikymas ir Koregavimo atšaukimas mobiliojo įrenginio meniu elemento keitimas

1. Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**, tada pasirinkite **Koregavimo taikymas ir atšaukimas**.
2. Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Ne**.
3. Lauke **Darbo kūrimo procesas** pasirinkite **Koregavimo taikymas**.

Į mobiliojo įrenginio meniu elementą bus įtraukti toliau nurodyti laukai, kai darbo kūrimo proceso metu pasirenkamas **Koregavimo taikymas** arba **Koregavimo atšaukimas**.

- Numatytasis skaičiavimo priežasties kodas
- Rodyti skaičiavimo priežasties kodą
- Redaguoti skaičiavimo priežasties kodą

