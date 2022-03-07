---
title: Skelbimas baigtais į ne pagal numerio lentelę kontroliuojamą vietą (programa, 2016 m. gegužė)
description: Šiame užduoties vadove parodytas skelbimo baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę, pavyzdys.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f891b2e3b20993a08138dfac1aed4f4bab33c6b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576717"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Skelbimas baigtais į ne pagal numerio lentelę kontroliuojamą vietą (programa, 2016 m. gegužė)

[!include [banner](../../includes/banner.md)]

Šiame užduoties vadove parodytas skelbimo baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę, pavyzdys. Norint atlikti šią užduotį, būtina tinkama darbo strategija. Kaip nustatyti darbo strategiją, parodyta ankstesniame užduoties vadove. Norint atlikti šį užduoties vediklį, reikia „Dynamics AX“ programos 7.0.1 arba naujesnės versijos.




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
    * Kai gamybos užsakymas buvo paskelbtas baigtu, nebuvo sugeneruota jokio padėjimo darbo. Taip nutinka, nes yra apibrėžta darbo strategija, pagal kurią negalima generuoti darbo, kai produktas L0101 paskelbiamas baigtu 001 vietoje.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]