---
title: ER ALLITEMS funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ALLITEMS elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: bb469955c66baf875eea80dde8199986e69e2e71
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274116"
---
# <a name="allitems-er-function"></a>ER ALLITEMS funkcija

[!include [banner](../includes/banner.md)]

`ALLITEMS` funkcija veikia kaip atminties pasirinkimas ir pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę kaip įrašų sąrašą, kuris nurodo visus elementus, atitinkančius nurodytą kelią.

## <a name="syntax"></a>Sintaksė

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumentai

`path`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Kelias turi būti nurodytas kaip tinkamas duomenų tipo *Įrašų sąrašas* duomenų šaltinio elemento kelias. Duomenų elementai, pvz., kelio eilutė ir data, kūrimo metu modulio Elektroninės ataskaitos (ER) reiškinių daryklėje turėtų pateikti klaidą.

Nerekomenduojame šios funkcijos naudoti su operacijų duomenų šaltiniais, kuriuose gali būti daug duomenų. Vietoj to apsvarstykite galimybę naudoti funkciją [ALLTEMSQUERY](er-functions-list-allitemsquery.md).

## <a name="example-1"></a>1 pavyzdys

Jei `SPLIT("abcdef" , 2)`įvesite kaip duomenų šaltinį **DS**, reiškinys `COUNT( ALLITEMS (DS))` pateiks **3**.

## <a name="example-2"></a>2 pavyzdys

Jei kaip duomenų tipo *Įrašų sąrašas* duomenų šaltinį įvedate **Vend**, nurodantį programos lentelę VendTable, reiškinys `ALLITEMS (Vend.'<Relations'.ContactPerson)` pateikia plokščiu padarytą įrašų sąrašą, turintį lentelės **ContactPerson** struktūrą ir kuriame yra visi kontaktiniai asmenys, kuriuos galima pasiekti naudojant ryšį **ContactPerson.ContactForParty == VendTable.Party**, ir kuris visiems tiekėjams pasiekiamas nurodytoje tiekėjų lentelėje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
