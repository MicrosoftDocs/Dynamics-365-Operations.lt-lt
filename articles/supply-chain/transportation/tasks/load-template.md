---
title: Krovinių šablonai
description: Šiame straipsnyje aprašoma, kaip nustatyti krovinių šablonus ir kaip susieti krovinio šabloną su nauju kroviniu.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47b4925c528b64b835ce3e88659ee6ab0572eb2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844186"
---
# <a name="load-templates"></a>Krovinių šablonai

[!include [banner](../../includes/banner.md)]

Sukūrę naują krovinį galite priskirti krovinio šabloną. Krovinio šablone pateikta informacija apie įrangą ir apie matmenis, tokius kaip aukštis, plotis, gylis ir krovinio apimtis.

Šiame straipsnyje aprašoma, kaip nustatyti krovinių šablonus ir kaip susieti krovinio šabloną su nauju kroviniu.

## <a name="set-up-a-load-template"></a>Nustatyti krovinio šabloną

1. Eikite į **Gabenimo valdymas \> Nustatymai \> Krovinio kūrimas \> Krovinio šablonas**.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad įtrauktumėte naują šabloną arba **Redaguoti** tam, kad redaguotumėte esamą šabloną.
1. Eilutėje naujam ar esančiam šablonui, nustatykite tolesnius laukelius:

    - **Krovinio šablono ID** - Įveskite unikalų ID krovinio šablonui.
    - **Įranga** – Pasirinkite įrangą, kuri turi būti naudojama siekiant išsiųsti krovinį.
    - **Krovinio aukštis**, **Krovinio plotis** ir **Krovinio gylis** – Įveskite krovinio matmenis.
    - **Maks. leidžiamas krovinio tūris** ir **Maks. leidžiamas krovinio plotis** – Įveskite maksimalų leistiną krovinio svorį ir tūrį.
    - **Maks. leidžiamas bendras svoris** – Įveskite maksimalų leistiną bendrą krovinio svorį. Bendras krovinio svoris apima tiek pakuotės, tiek ir krovinio svorį.
    - **Maks. leidžiamas skaičius siunčiamų krovinio dalių** – Įveskite maksimalų skaičių krovinio dalių, kurios gali sudaryti krovinį.
    - **Padėkite krovinį ant grindų** – Pasirinkite šį žymimą laukelį, kad būtų naudojamas grindų krovinys. Ant grindų krovinio scenarijaus atveju, dėžės yra padėtos ant grindų iki lubų ir nuo sienos iki sienos talpykloje siekiant maksimizuoti talpą.

1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="associate-a-load-template-with-a-new-load"></a>Susiekite krovinio šabloną su naujų kroviniu

1. Eikite į **Gabenimo valdymas \> Planavimas \> Krovinio planavimo darbo sritis**.
1. Viršutinėje puslapio dalyje, pasirinkite vieną iš tolesnių skirtukų priklausomai nuo šaltinio dokumento tipo, kuriam kuriate krovinį: **Siuntimai**, **Pardavimo eilutės**, **Perdavimo eilutės** ar **Įsigijimo užsakymo eilutės**. 
1. Pasirinkite konkrečius dokumentus, kad suplanuotumėte krovinį.
1. Veiksmų srities **Tiekti ir pareikalauti** skirtuke **Pridėti** grupėje pasirinkite **Į naują krovinį**.
1. Teksto laukelyje **Krovinio šablonas** **Krovinio šablono ID** laukelyje pasirinkite taikomą šabloną.
1. Pasirinkite **GERAI** norėdami pritaikyti šabloną.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]