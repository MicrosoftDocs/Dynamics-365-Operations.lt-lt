---
title: Sąskaitų plano skyriklio nustatymas, kad jis būtų unikalus
description: Šiame straipsnyje paaiškinama, kaip sąskaitų plano ir dimensijų verčių skyriklio turėti negalima. Atnaujinę turite pakeisti skyriklio reikšmes.
author: panolte
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 2fd29d747c7141b051e6c7c68db94abfd849f947
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123503"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Sąskaitų plano skyriklio nustatymas, kad jis būtų unikalus

[!include [banner](../includes/banner.md)]

Programoje „Microsoft Dynamics AX 2012“ sąskaitų planui ir dimensijų vertėms galite naudoti tą patį skyriklį. Dabartinėse finansų ir operacijų versijose negalima turėti to paties sąskaitų plano ir dimensijų pavadinimų bei verčių skyriklio. Jei yra pasikartojantis skyriklis, atnaujinę galite jį pakeisti. 

## <a name="update-delimiter"></a>Atnaujinkite skyriklį
Jei tarp sąskaitų plano, sąskaitų plano skyriklio ir projekto / subprojekto ID yra neatitikimas, formatą galima keisti. Kitų dimensijos skyriklių keisti negalima. 
- Sąskaitų plano skyriklį galite keisti atnaujinę versiją ir apsilankę parinktyje **DK parametrai** > **Sąskaitų planas ir dimensijos** > **Skyriklio keitimas**. 
- Jei vienintelis neatitikimas yra tarp projekto / subprojekto ID formato, tą reikšmę galite pakeisti parinktyje **Projektų valdymo ir apskaitos parametrai** > **Bendra** > **Subprojekto formato keitimas**. 

### <a name="other-considerations"></a>Kiti svarstymai
Panašus į projekto/subprojekto ID, bet kokie kiti pagrindinių duomenų įrašai, naudojami kaip finansinės dimensijos, pvz., tiekėjai ar klientai, neturėtų turėti sąskaitos ID reikšmių, kurios naudoja tą patį simbolį kaip sąskaitų plano skyriklis. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kaip nustatyti, ar jūsų aplinkoje reikia atnaujinti skyriklius 
Jei skyrikliai atnaujintoje aplinkoje neatitinka, segmentuoto įrašo valdiklyje arba dimensijų įrašo valdiklyje įvedant reikšmes gali kilti nestabilumų. Tai reiškia, kad įvesdami sąskaitos ir dimensijos kombinacijas visada turėsite naudoti peržvalgas arba iškeliamąjį meniu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

