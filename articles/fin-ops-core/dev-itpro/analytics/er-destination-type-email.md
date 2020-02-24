---
title: El. pašto ER paskirties vietos tipas
description: Šioje temoje pateikiama informacija apie tai, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno APLANKO ar FAILO komponento el. pašto paskirties vietą.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019906"
---
# <a name="EmailDestinationType">El. pašto paskirties vieta</a>

[!include [banner](../includes/banner.md)]

Galite sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno APLANKO ar FAILO komponento el. pašto paskirties vietą. Remiantis paskirties vietos nustatymu, sugeneruotas dokumentas pristatomas kaip el. laiško priedas.

Nustatykite parinktį **Įgalinta** į **Taip**, norėdami siųsti išvesties failą el. paštu. Įgalinę šią parinktį, galite nurodyti el. laiško gavėjus ir redaguoti el. laiško temą bei tekstą. Galite nustatyti nuolatinį el. laiško temos ir teksto tekstą arba galite naudoti ER [formules](er-formula-language.md), norėdami el. laiškų tekstą kurti dinamiškai. 

ER el. pašto adresus galite konfigūruoti dviem būdais. Konfigūravimą galima baigti taip pat, kaip jį baigia spausdinimo valdymo funkcija, arba galima nustatyti el. pašto adresą, naudojant tiesioginę nuorodą į ER konfigūraciją per formulę.

[![El. pašto paskirties vietos įgalinimas](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>El. pašto adresų tipai

Pasirinkus laukų **Kam** arba **Kopija** parinktį **Redaguoti**, rodomas dialogo langas **Siųsti el. laišką**. Tada galite pasirinkti norimą naudoti el. pašto adreso tipą. Šiuo metu palaikomi el. pašto tipai **Konfigūravimo el. laiškas** ir **Spausdinimo valdymas**.

[![El. laiško tipo pasirinkimas](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Spausdinimo valdymas

Jei pasirinksite el. laiško tipą **Spausdinimo valdymas**, galite įvesti fiksuotus el. pašto adresus lauke **Kam**. 

[![Fiksuotų el. pašto adresų konfigūravimas](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Norėdami naudoti nefiksuotus el. pašto adresus, turite pasirinkti failo paskirties vietos el. pašto šaltinio tipą. Palaikomos šios vertės: **Klientas**, **Tiekėjas**, **Potencialus klientas**, **Kontaktas**, **Konkurentas**, **Darbuotojas**, **Pretendentas**, **Galimas tiekėjas** ir **Neleidžiamas tiekėjas**. Pasirinkę el. pašto šaltinio tipą, naudokite šalia lauko **El. pašto šaltinio sąskaita** esantį mygtuką, kad atidarytumėte formą **Formulės dizaino įrankis**. Šią formą galite naudoti norėdami pridėti formulę, kuri vykdymo metu pateikia pasirinkto šaltinio tipo **šalies sąskaitą** iš apdoroto dokumento į el. pašto paskirties vietą.

[![El. pašto šaltinio sąskaitos konfigūravimas](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formulės būdingos ER konfigūracijai. Srityje **Formulė** įveskite konkretaus dokumento nuorodą į kliento arba tiekėjo šalies tipą. Užuot rinkę tekstą, galite surasti duomenų šaltinio mazgą, atitinkantį kliento ar tiekėjo sąskaitą, ir tada pasirinkti **Įtraukti duomenų šaltinį**, kad atnaujintumėte formulę. Pavyzdžiui, jei naudojate **ISO 20022 kredito perkėlimo** konfigūraciją, tiekėjo sąskaitą atitinkantis mazgas yra `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Jei įvesite eilutės vertę, pvz., `"DE-001"`, ir įrašysite formulę, el. laiškas bus išsiųstas tiekėjo kontaktiniam asmeniui, **DE-001**.


[![ER formulių dizaino įrankio puslapis](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![El. pašto šaltinio sąskaitos konfigūravimas](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Konfigūravimo el. laiškas

Naudokite šį el. pašto tipą, jei jūsų naudojamos konfigūracijos duomenų šaltiniuose yra mazgas, pateikiantis **el. pašto adresą**. Galite naudoti duomenų šaltinius ir funkcijas formulės dizaino įrankyje, kad gautumėte teisingai suformatuotą el. pašto adresą. Pavyzdžiui, jei naudojate **ISO 20022 kredito perkėlimo** konfigūraciją, tiekėjo kontaktinio asmens el. pašto adresą atitinkantis mazgas yra `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![El. pašto adreso šaltinio konfigūravimas](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)
- [Elektroninių ataskaitų (ER) formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)
