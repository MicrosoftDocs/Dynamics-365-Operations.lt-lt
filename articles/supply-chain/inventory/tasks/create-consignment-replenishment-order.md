---
title: Kurti naują konsignacijos papildymo užsakymą
description: Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3e33008d04ea8bb7d145c7b63cec23a4a45dd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "315503"
---
# <a name="create-a-consignment-replenishment-order"></a>Kurti naują konsignacijos papildymo užsakymą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą. Joje taip pat parodoma, kaip įrašyti produktų gavimą, kad konsignacijos atsargos būtų užregistruotas tiekėjui priklausančios turimos atsargos. Paprastai šią procedūrą atlieka įsigijimo specialistas. Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.




## <a name="create-a-consignment-replenishment-order"></a>Konsignacijos papildymo užsakymo kūrimas
1. Eikite į Įsigijimas ir šaltinio pasirinkimas > Konsignacija > Konsignacijos papildymo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo kodas įveskite tiekėją US-104.
    * Turite pasirinkti tiekėją, kuris puslapyje Atsargų savininkai yra užregistruotas kaip savininkas.  
4. Spustelėkite GERAI.
5. Spustelėkite Pridėti eilutę.
6. Lauke Prekės numeris įveskite M9211CI.
    * Turite pasirinkti prekę, kuri nustatyta konsignacijos atsargose.  
7. Lauke Kiekis įveskite skaičių.
8. Lauke Pageidaujama pristatymo data įveskite datą.
    * MPP mechanizmas naudoja pageidaujamas ir patvirtintas datas, kad nustatytų numatomą prekių gavimo datą.  
9. Lauke Patvirtinta pristatymo data įveskite datą.
10. Išplėskite skyrių Eilutės informacija.
11. Spustelėkite skirtuką Atsargų dimensijos.
12. Jei norite, kad puslapyje Atsargų dimensijų savininkas būtų rodomas savininkas, atnaujinkite puslapį.
    * Dabar tiekėjas US-104 yra nurodytas kaip savininkas.  

## <a name="check-the-inventory-transaction-status"></a>Atsargų operacijos būsenos patikra
1. Spustelėkite Atsargos.
2. Spustelėkite Operacijos.
3. Sąraše pažymėkite pasirinktą eilutę.
    * Atkreipkite dėmesį, kad laukas Gavimas laukas nustatytas į parinktį Užsakytas.  
4. Uždarykite puslapį.

## <a name="receive-items"></a>Gauti prekes
1. Spustelėkite Produkto gavimo kvitas.
2. Lauke Išorinis produkto gavimo kvitas įveskite reikšmę.
3. Lauke Kiekis įveskite skaičių, kuris yra mažesnis nei čia rodomas kiekis. 
4. Spustelėkite GERAI.

## <a name="check-the-on-hand-inventory"></a>Turimų atsargų patikra
1. Spustelėkite Atsargos.
2. Spustelėkite Turimas kiekis.
3. Spustelėkite Apžvalga.
    * Prekės, kurios nebuvo gautos kaip tiekėjui priklausančios konsignacijos atsargos, yra turimos atsargos. Likęs konsignacijos papildymo užsakymo kiekis rodomas lauke Užsakyta iš viso.  
4. Uždarykite puslapį.
5. Spustelėkite Uždaryti.

