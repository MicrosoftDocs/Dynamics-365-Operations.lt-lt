---
title: Senesnių paketų sandėlyje rodymo konfigūravimas mobiliajame įrenginyje
description: Šioje temoje aprašoma, kaip nustatyti mobilųjį įrenginį, kad jame būtų rodomas vietų su senesniais už dabartinę darbo eilutės vietą paketų vietų sąrašas.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 946266e73d59bdf383f1f91cdf70dd58f01b995c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "352648"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Senesnių paketų sandėlyje rodymo konfigūravimas mobiliajame įrenginyje

[!include [banner](../includes/banner.md)]

Konfigūracija **Rodyti senesnius paketus sandėlyje** leidžia rodyti vietų su senesniais už dabartinę darbo eilutės vietą paketų vietų sąrašą. Rodomame vietų sąraše pateikiama informacija apie senesnius toje vietoje paketus ir galiojimo data bei kiekvieno paketo faktinės atsargos. Galite pasirinkti paėmimą iš naujos vietos arba tęsti paėmimą iš dabartinės vietos. 
- Paėmimas iš naujos vietos – jei pasirinksite naują vietą, iš kurios norite atlikti paėmimą, dabartinė darbo eilutė bus atnaujinta į naują vietą, o darbas bus tęsiamas įprastai naujoje vietoje. Kad nauja vieta būtų tinkama, joje turi būti pakankamai kiekio, kad jo užtektų visai darbo eilutei. Jei reikalaujamo kiekio nėra, darbo eilutė atnaujinta nebus ir bus rodomas sąrašas. 
- Paėmimo tęsimas iš dabartinės vietos – jei ir toliau naudosite dabartinės darbo eilutės vietą, darbo eilutės kiekiai toliau bus imami iš pradinės vietos.

## <a name="where-it-applies"></a>Kai taikoma
Parinktis Senesnių paketų sandėlyje rodymas sukonfigūruota mobiliojo įrenginio meniu elementuose ir paveikia toliau nurodytus paketo paėmimo elementus.

## <a name="set-up-display-older-batches-within-warehouse"></a>Parinkties Senesnių paketų sandėlyje rodymo nustatymas
Konfigūraciją **Senesnių paketų sandėlyje rodymas** galima naudoti mobiliojo įrenginio meniu elementams, kai parinktis **Paimti seniausią paketą** nustatyta į **Įspėti**.

- Parinktyje **Sandėlio valdymas** > **Sąranka** > **Mobilusis įrenginys** > **Mobiliojo įrenginio meniu elementai** nustatykite meniu elemento parinktį **Naudoti esamą darbą** į **Taip** ir lauke **Paimti seniausią paketą** pasirinkite **Įspėti**. 

