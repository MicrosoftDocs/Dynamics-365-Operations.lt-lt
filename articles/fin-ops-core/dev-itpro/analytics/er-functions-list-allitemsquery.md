---
title: ER ALLITEMSQUERY funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ALLITEMSQUERY elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e350dfbe800ddc3e7b1f388fb951d091a283f4e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285312"
---
# <a name="allitemsquery-er-function"></a>ER ALLITEMSQUERY funkcija

[!include [banner](../includes/banner.md)]

`ALLITEMSQUERY` funkcija veikia kaip sujungta SQL užklausa. Ji pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę, sudarytą iš įrašų sąrašo, kuriame nurodomi visi elementai, atitinkantys nurodytą kelią.

## <a name="syntax"></a>Sintaksė

```vb
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

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
