---
title: Atsargų pasiekiamumas dvigubam rašymui
description: Šioje temoje pateikiama informacija apie atsargų pasiekiamumo tikrinimą dvigubo rašymo funkcijoje.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839554"
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

„Finance and Operations” programos | „Customer engagement“ programa | Aprašymas 
---|---|---
[CDS turimų atsargų įrašai](#145) | „msdyn_inventoryonhandentries” |
[CDS turimų atsargų užklausos](#147) | „msdyn_inventoryonhanrequests” |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a> Turimų CDS atsargų įrašai („msdyn_inventoryonhandentries”)

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Dataverse“.

„Finance and Operations“ laukas | Schemos tipas | „Customer engagement“ laukas | Numatytoji reikšmė
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>Turimų CDS atsargų užklausos (msdyn_inventoryonhandrequests)

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Dataverse“.

„Finance and Operations“ laukas | Schemos tipas | „Customer engagement“ laukas | Numatytoji reikšmė
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]