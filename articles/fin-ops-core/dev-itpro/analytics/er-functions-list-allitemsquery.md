---
title: ER ALLITEMSQUERY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ALLITEMSQUERY funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 647019a103006c8b74bc26885c51f5372dcf0c42
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917516"
---
# <a name="ALLITEMSQUERY">ER ALLITEMSQUERY funkcija</a>

[!include [banner](../includes/banner.md)]

`ALLITEMSQUERY` funkcija veikia kaip sujungta SQL užklausa. Ji pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę, sudarytą iš įrašų sąrašo, kuriame nurodomi visi elementai, atitinkantys nurodytą kelią.

## <a name="syntax"></a>Sintaksė

```
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumentai

`path`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas. Jame turi būti bent vienas ryšys.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Nurodytas kelias turi būti apibrėžtas kaip tinkamas duomenų tipo *Įrašų sąrašas* duomenų šaltinio elemento kelias. Jame taip pat turi būti bent vienas ryšys. Duomenų elementai, pvz., kelio *Eilutė* ir *Data*, kūrimo metu modulio Elektroninės ataskaitos (ER) reiškinių daryklėje turėtų pateikti klaidą.

Kai ši funkcija taikoma duomenų tipo *Įrašų sąrašas* duomenų šaltiniams, nurodantiems programos objektą, kurį galima tiesiogiai iškviesti naudojant SQL (pvz., lentelę, objektą ar užklausą), ji veikia kaip sujungta SQL užklausa. Priešingu atveju ji veikia atmintyje kaip funkcija [ALLITEMS](er-functions-list-allitems.md).

## <a name="example"></a>Pavyzdys

Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:

- Duomenų šaltinis **CustInv**, kuris priklauso tipui *Lentelės įrašai* ir susijęs su lentele CustInvoiceTable
- Duomenų šaltinis **FilteredInv**, kuris priklauso tipui *Apskaičiuotasis laukas* ir turi reiškinį `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- **JourLines**, kuris priklauso tipui *Apskaičiuotasis laukas* ir turi reiškinį `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Kai vykdote modelio susiejimą norėdami iškviesti duomenų šaltinį **JourLines**, vykdomas tolesnis SQL sakinys.

```
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)