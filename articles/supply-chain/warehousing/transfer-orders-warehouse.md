---
title: Sandėlių perkėlimo užsakymų nustatymas
description: Šioje temoje aprašoma, kaip galite nustatyti sandėlių perkėlimo užsakymus.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 91db6e8f921bd674211f6d478b6d0f0a832c983c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847020"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Sandėlių perkėlimo užsakymų nustatymas 

[!include [banner](../includes/banner.md)]

Kurdami hierarchiją, palaikančią perkėlimo iš vieno sandėlio į kitą užsakymus, galite naudoti sandėlio lygius. Šiuo nustatymu paremtas bendrasis planavimas apskaičiuoja atskiro sandėlio lygio prekių poreikį ir nustatytame pagrindiniame sandėlyje sugeneruoja suplanuotus perkėlimo užsakymus, kad būtų galima juos vykdyti.

1.  Spustelėkite **Atsargų valdymas > Sąranka > Atsargų paskirstymas > Sandėliai**.

2.  Pasirinkite norimą papildyti sandėlį.

3.  „FastTab“ **Bendrasis planavimas** pasirinkite žymės langelį **Papildymas**.

4.  Lauke **Pagrindinis sandėlis** pasirinkite sandėlį, kurį norite nustatyti kaip pildomą sandėlį. Bendrasis planavimas apskaičiuoja, kokį kiekį perkelti į pasirinktą sandėlį, ir naudodamas objektą **Pagrindinis sandėlis** sugeneruoja suplanuotą perkėlimo užsakymą.
   
    > [!NOTE]
    > <P>Jei žymės langelis <STRONG>Papildymas</STRONG> išvalomas, pasirinktam sandėliui priskiriamas su parinktimi <STRONG>Pagrindinis sandėlis</STRONG> susietas sandėlio lygis, tačiau <STRONG>Pagrindinis sandėlis</STRONG> nenustatomas kaip papildymo sandėlis.</P>

5.  Uždarykite puslapį, kad būtų pritaikytas naujas nustatymas.


> [!TIP]
> <P>Jei norite priskirti papildymo sandėlį, prieš tai formoje puslapyje <STRONG>Saugojimo dimensijų grupės</STRONG> turite nustatyti saugojimo dimensiją kaip atsargų dimensiją. Šiame puslapyje pasirinkite sandėlio lauką <STRONG>Aktyvus</STRONG> ir lauką <STRONG>Padengimo planas dimensijomis</STRONG>.</P>

## <a name="set-up-transport-lead-time"></a>Transportavimo vykdymo laiko nustatymas

Turite taip pat nustatyti transportavimo tarp sandėlių vykdymo laiką puslapyje **Transportavimo dienos**. 
1. Pasirinkite **Atsargų valdymas > Sąranka > Paskirstymas > Transportavimo dienos**.
2. Lauke **Gavimo vieta** pasirinkite **sandėlį**.
3. Pasirinkite **Siuntimo sandėlis**, **Gavimo sandėlis** ir **Transportavimo dienos**. 
4. (Pasirinktinai) Taip pat galite nustatyti transportavimo laiką, atsižvelgdami į pristatymo būdą, skirtuke **Transportavimo dienos pagal pristatymo būdą**.
