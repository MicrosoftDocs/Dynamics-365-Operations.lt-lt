---
title: Atsargų pasiekiamumas dvigubam rašymui
description: Šiame straipsnyje pateikta informacija apie tai, kaip tikrinti atsargų prieinamumą dvigubo rašymo metu.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: efd175dfbe49549561bdb7d697c8bc47016f1d5d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908268"
---
# <a name="inventory-availability-in-dual-write"></a>Atsargų pasiekiamumas dvigubam rašymui

[!include [banner](../../includes/banner.md)]

Naudodami atsargų pasiekiamumą, galite patikrinti savo atsargas prieš pridėdami produktą į **Kainos**, **Užsakymai** arba **Sąskaitos faktūros** puslapį „Microsoft Dynamics 365 Sales”. Pavyzdžiui, patikrinkite atsargas ir nustatykite įvykdymo datą kaip vieną iš pagrindinių užduočių [potencialaus grynųjų pinigų](dual-write-prospect-to-cash.md) proceso metu.

Jeigu nepakanka atsargų, galite įvertinti pristatymo datą pagal suplanuotų atsargų gavimą ir išdavimą. Taip pat galite patikrinti produkto prieinamų atsargų (ATP) informaciją, kurioje galima rasti ATP kiekį iš anksto apibrėžtoje laiko riboje.

## <a name="on-hand-inventory"></a>Turimos atsargos

„Dynamics 365 Sales“ naujas **Turimos atsargos** mygtukas pridėtas **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapių antraštėse. Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę ir produktą, kurio turimas atsargas norite patikrinti. Šis dialogo langas parodo tokią pačią informaciją kaip [Turimos atsargos](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialogo langas grąžina atsargų informaciją iš „Dynamics 365 Supply Chain Management”. Pateikiama informacija apie šiuos kiekius:

- Turimas kiekis
- Rezervuotas turimas kiekis
- Prieinamas turimas kiekis
- Užsakytas kiekis.
- Užsakymo kiekis
- Rezervuotas užsakytas kiekis
- Bendras prieinamas kiekis

## <a name="atp-information"></a>ATP informacija

„Sales” naujas **ATP informacija** mygtukas pridėtas prie eilutės elementų **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapiuose. Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę, produktą, atsargų vietą, atsargų sandėlį ir užsakymo kiekį. Šis dialogo langas turi tuos pačius parametrus, aprašytus [Užsakymo vykdymo įsipareigojimuose](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialogo langas grąžina ATP informaciją iš „Supply Chain Management”. Pateikiama informacija apie šiuos kiekius:

- ATP kiekis
- Gavimo kiekis
- Išdavimo kiekis
- Turimas kiekis

## <a name="how-it-works"></a>Kaip tai veikia

Kai pasirenkate mygtuką **Turimos atsargos** puslapiuose **Pasiūlymai**, **Užsakymai**, arba **Sąskaitos faktūros** tiesioginio dvigubo rašymo iškvietimas pateikiamas **Turimų atsargų** API. API apskaičiuoja turimos tam tikro produkto atsargas. Rezultatas saugomas **„InventCDSInventoryOnHandRequestEntity”** ir **„InventCDSInventoryOnHandEntryEntity”** lentelėse, o tada įrašomas į „Dataverse” naudojant dvigubą rašymą. Norėdami naudoti šią funkciją, turite paleisti šias dvigubo rašymo schemas. Praleiskite pradinį sinchronizavimą, kai paleidžiate schemas.

- Turimų CDS atsargų įrašai („msdyn_inventoryonhandentries”)
- Turimų CDS atsargų užklausos („msdyn_inventoryonhandrequests”)

## <a name="templates"></a>Šablonai

Šie šablonai yra galimi rodyti turimų atsargų duomenims.

„Finance and operations” programos | „Customer engagement“ programos     | Aprašas
---|---|---
[CDS turimų atsargų įrašai](mapping-reference.md#145) | „msdyn_inventoryonhandentries” |
[CDS turimų atsargų užklausos](mapping-reference.md#147) | „msdyn_inventoryonhanrequests” |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
