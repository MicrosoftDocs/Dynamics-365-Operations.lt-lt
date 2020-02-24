---
title: ER ALLITEMS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ALLITEMS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79c43b6ecdb307433b0c2091840c21a5ada3a689
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917447"
---
# <a name="ALLITEMS">ER ALLITEMS funkcija</a>

[!include [banner](../includes/banner.md)]

`ALLITEMS` funkcija veikia kaip atminties pasirinkimas ir pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę kaip įrašų sąrašą, kuris nurodo visus elementus, atitinkančius nurodytą kelią.

## <a name="syntax"></a>Sintaksė

```
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