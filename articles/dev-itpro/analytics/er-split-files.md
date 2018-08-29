---
title: "Sugeneruotų XML failų skaidymas pagal failo dydį ir turinio kiekį"
description: "Šioje temoje pateikta informacija apie tai, kaip skaidyti sugeneruotus failus pagal failo dydį ir turinio elementų kiekį."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 0f13194575e2f19f585f09ffad99144c9a9fc3b1
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Sugeneruotų XML failų skaidymas pagal failo dydį ir turinio kiekį

[!include[banner](../includes/banner.md)]

Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus generuoti siunčiamus dokumentus XLS formatu. Kartais šie dokumentai gali būti priimti tik tada, kai atitinka konkrečius kriterijus, pvz., maksimalus failo dydis arba didžiausias kai kurių XML mazgų skaičius. Galite kurti ER formatus, skirtus generuoti elektroninius dokumentus, kurie atitiktų šių dokumentų gavėjų nurodytus reikalavimus.

- FAILO formato elementui, galite nustatyti failo dydžio ribą kaip ER išraišką. Viršijus nustatytą ribą generuojant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.
- Bet kuriam formatui XML ELEMENTAS galite nustatyti elementų skaičiaus ribą kaip ER išraišką. Sugeneruotame faile viršijus nustatytą XML mazgų ribą vykdant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.
- Bet kuriam formato XML SEKA elementui galite nustatyti antrinių elementų skaičiaus ribą kaip ER išraišką. Sugeneruotame faile viršijus nustatytą formato elemento įdėtųjų XML mazgų ribą vykdant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.
- Galite pažymėti bet kurį XML ELEMENTAS formato elementą kaip neperkeliamąjį. Tokiu būdu galite išlaikyti įdėtuosius XML mazgų elementus, sugeneruotus pagal formato elementą, viename sugeneruotame faile.

Be to, be formato elementų XML ELEMENTAS ir XML SEKA, XML mazgams įtraukti į sugeneruotą failą galite naudoti formato elementą NEAPDOROTAS XML. Tačiau mazgų, kuriuos įtrauksite naudodami formato elementą NEAPDOROTAS XML, nėra paisoma skaičiuojant mazgus, siekiant įvertinti elementų skaičiaus ribas.

Jei sukonfigūravote formato elemento FAILAS failų paskirties vietas, kuris sukonfigūruotas skaidyti sugeneruotą išvestį, kai viršijamos konkrečios ribos, kiekviena sugeneruotos išvesties dalis siunčiama į sukonfigūruotą failo paskirties vietą kaip atskiras failas. Norėdami unikaliai pavadinti failus, kurie sukuriami suskaidžius išvestį, turite sukonfigūruoti formato elemento FAILAS ER išraišką. Jei norite įtraukti NUMERACIJA tipo ER duomenų šaltinį, numeracija bus didinama su kiekviena suskaidytos išvesties dalimi.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlį **ER XML failai, suskaidyti atsižvelgiant į failo dydį arba turinio elementų kiekį**, kuris yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** verslo proceso dalis ir gali būti atsisiųstas iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684). Šis užduočių vedlys padės ER formato konfigūravimo proceso metu, norint skaidyti sugeneruotus failus atsižvelgiant į failo dydžio ir turinio elementų kiekio ribas. Norėdami užbaigti užduočių vedlį, turite atsisiųsti šiuos failus:

- [ER modelio konfigūracija – XmlFilesSplittingModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER formato konfigūracija – XmlFilesSplittingFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a>Papildomi ištekliai
[Elektroninių ataskaitų paskirties vietos](electronic-reporting-destinations.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

