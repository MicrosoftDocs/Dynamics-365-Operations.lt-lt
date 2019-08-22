---
title: Sąskaitų plano skyriklio nustatymas, kad jis būtų unikalus
description: Programoje „Dynamics 365 for Finance and Operations“ sąskaitų plano ir dimensijų reikšmių skyrikliai negali būti tokie patys. Atnaujinę turite pakeisti skyriklio reikšmes.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 8cc05772e7ee125a5ce8603c4d5f8719e8895c73
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851776"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Sąskaitų plano skyriklio nustatymas, kad jis būtų unikalus

[!include [banner](../includes/banner.md)]

Programoje „Microsoft Dynamics AX 2012“ sąskaitų planui ir dimensijų vertėms galite naudoti tą patį skyriklį. Programoje „Dynamics 365 for Finance and Operations“ sąskaitų plano ir dimensijų reikšmių skyrikliai negali būti tokie patys. Jei yra pasikartojantis skyriklis, atnaujinę galite jį pakeisti. 

Ši funkcija yra pasiekiama:
- „Dynamics 365 for Finance and Operations“ 8.0 versija
- „Dynamics 365 for Finance and Operations“ 7.1 versijoje, KB 4094701, įvesti finansinių dimensijų negalite tada, kai dimensijų vertėse yra sąskaitų plano skyriklis
- „Dynamics 365 for Finance and Operations“ 7.2 versijoje, KB 4092967, subprojekto kaip dimensijos negalite pasirinkti tada, kai subprojekto formate yra dimensijos skyriklis

## <a name="update-delimiter"></a>Atnaujinkite skyriklį
Jei tarp sąskaitų plano, sąskaitų plano skyriklio ir projekto / subprojekto ID yra neatitikimas, formatą galima keisti. Kitų dimensijos skyriklių keisti negalima. 
- Sąskaitų plano skyriklį galite keisti atnaujinę „Finance and Operations“ versiją ir apsilankę parinktyje **DK parametrai** > **Sąskaitų planas ir dimensijos** > **Skyriklio keitimas**. 
- Jei vienintelis neatitikimas yra tarp projekto / subprojekto ID formato, tą reikšmę galite pakeisti parinktyje **Projektų valdymo ir apskaitos parametrai** > **Bendra** > **Subprojekto formato keitimas**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kaip nustatyti, ar jūsų aplinkoje reikia atnaujinti skyriklius 
Jei skyrikliai atnaujintoje aplinkoje neatitinka, segmentuoto įrašo valdiklyje arba dimensijų įrašo valdiklyje įvedant reikšmes gali kilti nestabilumų. Tai reiškia, kad įvesdami sąskaitos ir dimensijos kombinacijas visada turėsite naudoti peržvalgas arba iškeliamąjį meniu.
