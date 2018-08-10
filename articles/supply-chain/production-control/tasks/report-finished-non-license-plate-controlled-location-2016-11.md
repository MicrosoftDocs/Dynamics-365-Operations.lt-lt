--- 
title: "Skelbimas baigtais į ne pagal numerio lentelę kontroliuojamą vietą "
description: "Šiame užduoties vadove parodytas skelbimo baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę, pavyzdys."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34fac03a0ff3d71a2349b66f8f85e4e124dcd708
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a>Skelbimas baigtais į ne pagal numerio lentelę kontroliuojamą vietą  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame užduoties vadove parodytas skelbimo baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę, pavyzdys. Norint atlikti šią užduotį, būtina tinkama darbo strategija. Kaip nustatyti darbo strategiją, parodyta ankstesniame užduoties vadove. Norint atlikti šį užduoties vediklį, reikia „Dynamics AX‟ programos 7.0.1 arba naujesnės versijos.




## <a name="set-up-an-output-location"></a>Išeigos vietos nustatymas
1. Pasirinkite Organizacijos administravimas > Ištekliai > Išteklių grupės.
2. Sąraše pasirinkite išteklių grupę 5102.
3. Spustelėkite Redaguoti.
4. Lauke Išeigos sandėlis įveskite „51‟.
5. Lauke Išeigos vieta įveskite „001‟.
    * 001 vieta nėra kontroliuojama pagal numerio lentelę. Ne pagal numerio lentelę kontroliuojamą išeigos vietą galite nustatyti tik jei yra tinkama vietos darbo strategija.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Gamybos užsakymo sukūrimas ir jo skelbimas baigtu
1. Uždarykite puslapį.
2. Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.
3. Spustelėkite Naujas gamybos užsakymas.
4. Lauke Prekės numeris įveskite „L0101‟.
5. Spustelėkite Kurti.
6. Srityje Veiksmas spustelėkite Gamybos užsakymas.
7. Spustelėkite Įvertinti.
8. Spustelėkite Gerai.
9. Spustelėkite Pradėti.
10. Spustelėkite skirtuką Bendra.
11. Lauke Automatinis KS suvartojimas pasirinkite Niekada.
12. Spustelėkite Gerai.
13. Spustelėkite Skelbti baigtu.
14. Spustelėkite skirtuką Bendra.
15. Lauke Leisti klaidą pasirinkite Taip.
16. Spustelėkite Gerai.
17. Veiksmų srityje spustelėkite Sandėlis.
18. Spustelėkite Darbo informacija.
    * Kai gamybos užsakymas buvo paskelbtas baigtu, nebuvo sugeneruota jokio padėjimo darbo. Taip nutinka, nes yra apibrėžta darbo strategija, pagal kurią negalima generuoti darbo, kai produktas L0101 paskebiamas baigtu 001 vietoje.  


