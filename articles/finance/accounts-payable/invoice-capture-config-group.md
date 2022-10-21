---
title: SF fiksavimo sprendimo konfigūracijos grupės
description: Šiame straipsnyje pateikiama bendroji informacija apie konfigūracijos grupes SF fiksavimo sprendimas.
author: sunfzam
ms.date: 09/28/2022
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
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691005"
---
# <a name="invoice-capture-solution-configuration-groups"></a>SF fiksavimo sprendimo konfigūracijos grupės

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Naudodami konfigūracijos grupes vartotojai gali valdyti SF laukų sąrašą ir neautomatinį juridinių subjektų peržiūros parametrą. Vartotojai gali nustatyti skirtingų juridinių subjektų SF konfigūracijas grupėse. Visi juridiniai subjektai toje pačioje konfigūracijos grupėje naudoja tuos pačius SF laukus ir rankinio peržiūros parametrus.

## <a name="manage-configuration-groups"></a>Tvarkyti konfigūracijos grupes

Jei norite tvarkyti konfigūracijos grupes naudodami programą, eikite į Sąranka **ir** pasirinkite Sistemos nustatymas **Konfigūracijos \> grupių komponento nustatymas**.

**Puslapyje Apibrėžti konfigūracijos** grupes pagrindinis skirtukas rodomas nustatytų konfigūracijos grupių sąrašas. Taip pat rodoma numatytoji konfigūracijos grupė. Kiekvienai konfigūracijos grupei galimi šie veiksmai:

- **Kopijuoti konfigūracijos** grupę – galite sukurti naują konfigūracijos grupę dėsdami esamą grupę. Naujos grupės vertės yra tokios pačios, kaip ir pradinė visų laukų grupė, išskyrus Grupės **pavadinimas** ir **Grupės aprašymas**. Dublię konfigūracijos grupę, pasirinkite **Gerai**.
- **Naikinti konfigūracijos grupes** – norėdami panaikinti konfigūracijos grupę, pasirinkite ją, o tada pasirinkite **Naikinti**.

    > [!NOTE]
    > Numatytosios konfigūracijos grupės panaikinti negalima.

- **Redaguoti konfigūracijos grupės ID** – norėdami redaguoti konfigūracijos grupės ID, **pasirinkite lauką Grupės ID** ir atnaujinkite vertę. Grupės ID neturi būti tarpų arba specialiųjų simbolių ir jis neturi viršyti 20 simbolių.

    > [!NOTE]
    > Lauko Grupės **ID** vertę galima atnaujinti tik vieną kartą.

- **Redaguoti konfigūracijos grupės aprašymą – norėdami** redaguoti konfigūracijos grupės aprašymą, **pasirinkite lauką Aprašymas** ir atnaujinkite vertę.
- **Keisti neautomatinio peržiūros** nustatymus – vartotojai gali nuspręsti, ar SF turi būti peržiūrėta rankiniu būdu. Norėdami pakeisti neautomatinį peržiūros parametrą, pasirinkite parinktį **Reikalingas peržiūra rankiniu** būdu. Galimos toliau nurodytos parinktys:

    - **Visada tikrinti rankiniu būdu** – pasirinkite šią pasirinktį, jei konfigūracijos grupės SF visada reikia peržiūrėti rankiniu būdu.
    - **Klaidų ir įspėjimų atveju** pasirinkite šią pasirinktį, jei SF, kuriose yra klaidų pranešimų arba įspėjimo pranešimų, reikia peržiūrėti rankiniu būdu.
    - **Klaidų atveju pasirinkite** šią pasirinktį, jei SF, kuriose yra klaidų pranešimų, reikia peržiūrėti rankiniu būdu.

- **Pakeisti patikimumo rezultato parametrą** – patikimumo rezultatas yra metaduomenys, kuriuos SF fiksavimo sprendimas pateikia atpažinto SF duomenų tikslumo ataskaitai. Kuo didesnis rezultatas, tuo tikslesni duomenys gali būti. Konfigūracija leidžia vartotojams apibrėžti, kada reikia rankiniu būdu peržiūrėti, remiantis patikimumo rezultatu. Vartotojai gali pakeisti SF patikimumo rezultato ribą. Norėdami atnaujinti patikimumo rezultato parametrą, pasirinkite patikimumo **rezultato** lauką ir atnaujinkite vertę.

    Yra du įspėjimų dėl patikimumo rezultatų tipai:

    - **Įspėjimas** – SF laukai, kurių patikimumo rezultatai viršija perspėjimo ribinę vertę, laikomi tinkamais. Perspėjimo ribinė vertė turi būti didesnė už klaidos slenkstį ir mažesnė nei 100.
    - **Klaida** – SF laukai, kurių patikimumo rezultatai viršija klaidos ribinę vertę, laikomi nepavykusi. Vartotojui bus rodomi klaidų pranešimai. Klaidos ribinė vertė turi būti didesnė nei 0 (nulis) ir mažesnė už perspėjimo ribinę vertę. Bus rodomi perspėjimo pranešimai SF laukams, kurie pasitiki perspėjimo ribinės vertės ir klaidos ribinės vertės rezultatais.

- **Valdyti SF laukus** – vartotojai gali valdyti SF laukų, rodomų viena šalia kitos peržiūros programoje, sąrašą. SF lauko **valdymo skirtuke** pasirinkite pavarų simbolį, pasirinkite SF laukus, kuriuos norite įtraukti, tada pasirinkite **Įrašyti**. Pasirinkti laukai bus įtraukti į sąrašą. Norėdami pašalinti SF lauką iš sąrašo, lauke **pasirinkite** Pašalinti.

### <a name="manage-file-filters-optional"></a>Valdyti failų filtrus (pasirinktinai)

Naudodami failų filtrus vartotojai gali nurodyti papildomus gaunamų SF failų filtrus. Failai, kurie neatitinka filtro kriterijų, bus gauti ir bus rodomi **gautų** failų sąraše, bet juose bus rodomos failo tikrinimo klaidos. Šis veikimo būdas skiriasi nuo kanale nustatytų filtrų veikimo būdo. Naudojant šiuos filtrus, failai, kurie neatitinka kriterijų, iš viso gaunami nebus. Vartotojai gali peržiūrėti gaunamus failus ir nuspręsti, ar kiekvienas failas yra netinkama SF ir jie gali nebenaudojami failo ar rankiniu būdu įtraukti ją atpažinimui ir įtraukimui į užfiksuotas SF.

Įdiegus SF fiksavimo sprendimą, nustatomas numatytasis failų filtras. Šis failų filtras yra visuotinis. Jei norite nustatyti skirtingus filtro parametrus, galite atnaujinti numatytąjį filtrą. Jei laukas privalomas, pasirinkite **Būtina**. 

### <a name="accepted-file-size"></a>Priimtas failo dydis

Galite pasirinkti priimtų failų dydžius.

> [!NOTE]
> Failai, kurių kaina didesnė nei 20 480 kilobaitų (KB), nepalaikomi.

### <a name="supported-file-types"></a>Palaikomi failų tipai

Šiuo metu palaikomi šie failų tipai:

- PDF
- PNG
- JPG
- JPEG
- Tif
- TIFF
