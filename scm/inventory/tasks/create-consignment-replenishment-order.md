---
title: "Kurti naują konsignacijos papildymo užsakymą"
description: "Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 5e268f640be11b0905457ff6b7697c90411f53e5
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Kurti naują konsignacijos papildymo užsakymą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą. Joje taip pat parodoma, kaip įrašyti produktų gavimą, kad konsignacijos atsargos būtų užregistruotas tiekėjui priklausančios turimos atsargos. Paprastai šią procedūrą atlieka įsigijimo specialistas. Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.




## <a name="create-a-consignment-replenishment-order"></a>Kurti naują konsignacijos papildymo užsakymą
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

