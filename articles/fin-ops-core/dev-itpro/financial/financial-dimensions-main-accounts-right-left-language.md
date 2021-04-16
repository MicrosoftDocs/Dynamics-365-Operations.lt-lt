---
title: Finansinės dimensijos ir pagrindinės sąskaitos, naudojamos iš dešinės į kairę rašomose kalbose
description: Šioje temoje aprašomi kai kurie sprendimai, kuriuos turėtumėte priimti, kai naudojate kalbą, kurioje rašoma iš dešinės į kairę, ir norite nustatyti finansines dimensijas bei pagrindines sąskaitas.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 508f4ed4de367770acddc77a6ff5e7e36fd20729
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748142"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finansinės dimensijos ir pagrindinės sąskaitos, naudojamos iš dešinės į kairę rašomose kalbose

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi kai kurie diegimo sprendimai, kuriuos turėtumėte apsvarstyti, kai naudojate kalbą, kurioje rašoma iš dešinės į kairę, ir norite nustatyti finansines dimensijas bei pagrindines sąskaitas.

Finansinės dimensijos ir pagrindinės sąskaitos yra pagrindiniai taikymo planavimo etapo komponentai. Sistemoje sukūrus finansines dimensijas ir pagrindines sąskaitas, jos yra naudojamos puslapiuose **Sąskaitų struktūrų konfigūravimas**, **Išplėstinės taisyklės struktūros** ir **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas**. Tuose puslapiuose nustatyta tvarka sistemoje naudojama duomenims įvesti ir naudoti. Kai kuriose sistemos vietose, finansinės dimensijos ir pagrindinės sąskaitos rodomos atskiruose laukuose. Kitose vietose, pvz., žurnaluose, finansinės dimensijos ir pagrindinės sąskaitos rodomos vienoje eilutėje.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Kaip geriausia nustatyti finansines dimensijas ir pagrindines sąskaitas, kai sistemoje naudojama kalba, kurioje rašoma iš dešinės į kairę

- Kai renkatės sąskaitų plano skyriklį, pasirinkite vieną iš dvigubų skyriklių: dvigubą brūkšnelį (`--`), dvigubą juostą (`||`), dvigubą tašką (`..`) arba dvigubą pabraukimą (`\\`).
- Kurdami finansinių dimensijų ir pagrindinių sąskaitų reikšmes, naudokite tik kalbos, kurioje rašoma iš dešinės į kairę, skaitmenis.
- Nenaudokite pasirinkto sąskaitų plano skyriklio finansinių dimensijų ir pagrindinių sąskaitų reikšmėse.

Laikydamiesi šių patarimų, užtikrinsite, kad vartotojo nurodyta tvarka būtų nuosekliai rodoma visoje sistemoje.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]