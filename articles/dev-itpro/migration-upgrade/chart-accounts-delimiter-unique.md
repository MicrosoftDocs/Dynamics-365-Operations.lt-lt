---
title: "Sąskaitų plano skyriklis turi būti unikalus"
description: "Programoje „Dynamics 365 for Finance and Operations“ sąskaitų plano ir dimensijų reikšmių skyrikliai negali būti tokie patys. Atnaujinę turite pakeisti skyriklio reikšmes."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a>Sąskaitų plano skyriklis turi būti unikalus

[!INCLUDE [banner](../includes/banner.md)]

Programoje „Microsoft Dynamics AX 2012“ sąskaitų planui ir dimensijų vertėms galite naudoti tą patį skyriklį. Programoje „Dynamics 365 for Finance and Operations“ sąskaitų plano ir dimensijų reikšmių skyrikliai negali būti tokie patys. Jei yra pasikartojantis skyriklis, atnaujinę galite jį pakeisti. 

Ši funkcija yra pasiekiama:
- „Dynamics 365 for Finance and Operations‟ 8.0 versijoje
- „Dynamics 365 for Finance and Operations“ 7.1 versijoje, KB 4094701, įvesti finansinių dimensijų negalite tada, kai dimensijų vertėse yra sąskaitų plano skyriklis
- „Dynamics 365 for Finance and Operations“ 7.2 versijoje, KB 4092967, subprojekto kaip dimensijos negalite pasirinkti tada, kai subprojekto formate yra dimensijos skyriklis

## <a name="update-delimiter"></a>Atnaujinkite skyriklį
Jei tarp sąskaitų plano, sąskaitų plano skyriklio ir projekto / subprojekto ID yra neatitikimas, formatą galima keisti. Kitų dimensijos skyriklių keisti negalima. 
- Sąskaitų plano skyriklį galite keisti atnaujinę „Finance and Operations“ versiją ir apsilankę parinktyje **DK parametrai** > **Sąskaitų planas ir dimensijos** > **Skyriklio keitimas**. 
- Jei vienintelis neatitikimas yra tarp projekto / subprojekto ID formato, tą reikšmę galite pakeisti parinktyje **Projektų valdymo ir apskaitos parametrai** > **Bendra** > **Subprojekto formato keitimas**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kaip nustatyti, ar jūsų aplinkoje reikia atnaujinti skyriklius 
Jei skyrikliai atnaujintoje aplinkoje neatitinka, segmentuoto įrašo valdiklyje arba dimensijų įrašo valdiklyje įvedant reikšmes gali kilti nestabilumų. Tai reiškia, kad įvesdami sąskaitos ir dimensijos kombinacijas visada turėsite naudoti peržvalgas arba iškeliamąjį meniu.

