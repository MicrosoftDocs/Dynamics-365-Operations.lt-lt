---
title: Finansinės dimensijos ir pagrindinės sąskaitos, naudojamos iš dešinės į kairę rašomose kalbose
description: Šiame straipsnyje aprašomi sprendimai, kuriuos reikia priimti naudojant dešiniosios ir kairiosios pusės kalbą, taip pat reikia nustatyti finansines dimensijas ir pagrindines sąskaitas.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b1e2c0ef5cd405232332847078c70af42f056e17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866766"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finansinės dimensijos ir pagrindinės sąskaitos, naudojamos iš dešinės į kairę rašomose kalbose

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi kai kurie diegimo sprendimai, į kuriuos turėtumėte atsižvelgti naudodami dešiniosios ir kairiosios pusės kalbą, ir turite nustatyti finansines dimensijas ir pagrindines sąskaitas.

Finansinės dimensijos ir pagrindinės sąskaitos yra pagrindiniai taikymo planavimo etapo komponentai. Sistemoje sukūrus finansines dimensijas ir pagrindines sąskaitas, jos yra naudojamos puslapiuose **Sąskaitų struktūrų konfigūravimas**, **Išplėstinės taisyklės struktūros** ir **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas**. Tuose puslapiuose nustatyta tvarka sistemoje naudojama duomenims įvesti ir naudoti. Kai kuriose sistemos vietose, finansinės dimensijos ir pagrindinės sąskaitos rodomos atskiruose laukuose. Kitose vietose, pvz., žurnaluose, finansinės dimensijos ir pagrindinės sąskaitos rodomos vienoje eilutėje.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Kaip geriausia nustatyti finansines dimensijas ir pagrindines sąskaitas, kai sistemoje naudojama kalba, kurioje rašoma iš dešinės į kairę

- Kai renkatės sąskaitų plano skyriklį, pasirinkite vieną iš dvigubų skyriklių: dvigubą brūkšnelį (`--`), dvigubą juostą (`||`), dvigubą tašką (`..`) arba dvigubą pabraukimą (`\\`).
- Kurdami finansinių dimensijų ir pagrindinių sąskaitų reikšmes, naudokite tik kalbos, kurioje rašoma iš dešinės į kairę, skaitmenis.
- Nenaudokite pasirinkto sąskaitų plano skyriklio finansinių dimensijų ir pagrindinių sąskaitų reikšmėse.

Laikydamiesi šių patarimų, užtikrinsite, kad vartotojo nurodyta tvarka būtų nuosekliai rodoma visoje sistemoje.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
