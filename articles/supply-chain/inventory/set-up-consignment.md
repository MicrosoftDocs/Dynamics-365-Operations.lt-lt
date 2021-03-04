---
title: Konsignacijos nustatymas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti gaunamų konsignacijos atsargų operacijas.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 51f7d6b0402ebbed417554978fc8d927f6b9c606
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433866"
---
# <a name="set-up-consignment"></a>Konsignacijos nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sukonfigūruoti gaunamų konsignacijos atsargų operacijas.

Konsignacijos atsargos yra tiekėjo turimos atsargos, kurios laikomos jūsų vietoje. Kai esate pasiruošę vartoti ar naudoti atsargas, atsargos tampa jūsų nuosavybe. Šioje temoje aprašoma sąranka, reikalinga norint įgalinti konsignacijos procesą. Daugiau informacijos apie konsignacijos procesus, žr. [Konsignacijos nustatymas](consignment.md).

## <a name="inventory-owners"></a>Atsargų savininkai
Norėdami įrašyti faktines gaunamos konsignacijos atsargas, turite nurodyti tiekėją, kuriam jos priklauso. Tai atliekama puslapyje **Atsargų savininkas**. Pasirinkus **Tiekėjo sąskaita** sugeneruojamos numatytosios laukų **Vardas** ir **Savininkas** vertės. Lauko **Savininkas** vertė matoma tiekėjui, todėl jeigu jūsų tiekėjo paskyros vardus kitiems gali būti sunku atpažinti, gali tekti juos pakeisti. Lauką **Savininkas** galima redaguoti, bet tik iki veiksmo, kai išsaugomas įrašas **Atsargų savininkas**. Lauke **Vardas** įrašomas su tiekėjo paskyra susietos šalies vardas ir jo negalima keisti.

[![atsargų savininkai](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Sekimo dimensijų grupė
Konsignacijos procesuose ketinamus naudoti elementus būtina susieti su **Sekimo dimensijų grupe**, kurios dimensijos **Savininkas** nuostata **Aktyvi**. Visada pažymėtos dimensijos Savininkas parinktys **Faktinės atsargos** ir **Finansinės atsargos**. Parinktis **Padengimo planas pagal dimensiją** niekada nepažymimas.

[![sekimo dimensijų grupė](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Atsargų nuosavybės pakeitimo žurnalas
Žurnalas **Atsargų nuosavybės pakeitimas** naudojamas norint įrašyti konsignacijos atsargų savininko pakeitimą iš tiekėjo į jį naudojantį juridinį subjektą. Kaip ir bet kuriame atsargų žurnale, jame turi būti nurodytas atsargų žurnalo pavadinimas. Šie pavadinimai sukuriami puslapyje **Atsargų žurnalo pavadinimai** ir turi būti nustatyta dalies **Žurnalo tipas** parinktis **Nuosavybės pakeitimas**.

[![atsargų nuosavybės pakeitimo žurnalas](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Tiekėjų bendradarbiavimas konsignacijos procesuose
Jei jūsų tiekėjai naudoja tiekėjų bendradarbiavimo sąsają, jie gali ją panaudoti norėdami stebėti atsargų suvartojimą jūsų vietoje. Daugiau informacijos apie tiekėjų parengimą naudoti tiekėjų bendradarbiavimo funkciją žr. [Tiekėjo portalo vartotojų sauga](../procurement/configure-security-vendor-portal-users.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]