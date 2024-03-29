---
title: Kurti naują konsignacijos papildymo užsakymą
description: Šiame straipsnyje paaiškinama, kaip sukurti konsignacijos papildymo užsakymą, kuriame galima sekti numatomą tiekėjo pristatymą į savo konsignacijai atsargas.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a1d0a7d322b17d3d80dd9fade2b037dd148d9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859407"
---
# <a name="create-a-consignment-replenishment-order"></a>Kurti naują konsignacijos papildymo užsakymą

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukurti konsignacijos papildymo užsakymą, kuriame galima sekti numatomą tiekėjo pristatymą į savo konsignacijai atsargas. Joje taip pat parodoma, kaip įrašyti produktų gavimą, kad konsignacijos atsargos būtų užregistruotas tiekėjui priklausančios turimos atsargos. Paprastai šią procedūrą atlieka įsigijimo specialistas. Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.

## <a name="create-a-consignment-replenishment-order"></a>Konsignacijos papildymo užsakymo kūrimas
1. Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Siunta > Siuntos papildymo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Tiekėjo sąskaita** pažymėkite tiekėją **US-104** (turite pažymėti tiekėją, kuris puslapyje **atsargų savininkai** registruotas kaip savininkas). 
4. Pasirinkite **Gerai**.
5. Pasirinkite **Pridėti eilutę**.
6. Lauke **Elemento numeris** įveskite `M9211CI` (turite pažymėti elementą, kuris nustatytas siuntos atsargoms).
7. Lauke **Kiekis** įveskite skaičių.
8. Lauke **Pageidaujama pristatymo data** įveskite datą. MPP mechanizmas naudoja pageidaujamas ir patvirtintas datas, kad nustatytų numatomą prekių gavimo datą.  
9. Lauke **Patvirtinta pristatymo data** įveskite datą.
10. Išplėskite skyrių **Eilutės informacija** section.
11. Pasirinkite skirtuką **Atsargų matmenys**.
12. Norėdami lauke **Atsargų matmenų savininkas** matyti savininką, atnaujinkite puslapį. Dabar tiekėjas US-104 yra nurodytas kaip savininkas.  

## <a name="check-the-inventory-transaction-status"></a>Atsargų operacijos būsenos patikra
1. Pasirinkite **Atsargos**.
2. Pasirinkite **Operacijos**.
3. Pageidaujamoje eilutėje pažymėkite, kad laukas **Gavimas** nustatytas kaip **Užsakyta**.  
4. Uždarykite puslapį.

## <a name="receive-items"></a>Gauti prekes
1. Pasirinkite **„Produkto gavimo kvitas“**.
2. Lauke **Išorinis produkto gavimas** įveskite reikšmę.
3. Lauke **Kiekis** įveskite skaičių, kuris mažesnis nei čia parodytas skaičius. 
4. Pasirinkite **Gerai**.

## <a name="check-the-on-hand-inventory"></a>Turimų atsargų patikra
1. Pasirinkite **Atsargos**.
2. Pažymėkite **Turima**.
3. Pažymėkite **Apžvalga**. Prekės, kurios nebuvo gautos kaip tiekėjui priklausančios konsignacijos atsargos, yra turimos atsargos. Likęs siuntos atsargų užsakymo kiekis rodomas lauke **Iš viso užsakyta**.  
4. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]