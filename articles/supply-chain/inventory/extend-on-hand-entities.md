---
title: Turimų atsargų duomenų objektų pratęsimas
description: Šiame straipsnyje pateikiamas pavyzdys, kaip įtraukti išplėstinius laukus į INVENTORSITEONHANDENTITY ir INVENTWAREWEONHANDENTITY rodinius, kad turimų atsargų duomenų objektų galimybės galėtų veikti su plėtiniais.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 352b466a185bcd0778ea17e598129864c1547987
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906043"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Turimų atsargų duomenų objektų pratęsimas

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management“ pateikia [plėtinių](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) funkcijas, kurios jums leidžia [įtraukti laukelius į lenteles per plėtinius](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Šiame straipsnyje pateikiamas pavyzdys, kaip `INVENTORSITEONHANDENTITY``INVENTWAREHOUSEONHANDENTITY` į juos įtraukti išplėstinius laukus ir rodinius, kad turimų atsargų duomenų objektų galimybės galėtų dirbti su plėtiniais. Dėl išsamesnės informacijos apie duomenų objektus, žr. [Duomenų valdymo peržiūrą](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Čia pateikiamas kai kurių turimų duomenų objektų atsargų sąrašą:
>
> - Turimos atsargos pagal vietą
> - Turimos atsargos pagal vietą V2
> - Turimos atsargos pagal sandėlį
> - Turimos atsargos sandėlyje v2

Po to, kai įtraukėte laukelius į lenteles, kurios yra naudojamos `inventSiteOnHandView` peržiūroje, privalote sinchronizuoti variklį taip, kad plėtiniai būtų tinkamai atpažinti.

1. Išplėskite `InventSiteOnHandView` peržiūrą įtraukdami plėtinio laukelį.
1. Išplėskite `InventSiteOnHandAggregatedView` peržiūrą su plėtinio laukeliais.
1. Išplėskite `InventSiteOnHandAggregatedViewBuilder` peržiūros kūrėjo klasę keisdami `getExtensionFields()` būdą. Tokiu būdu, įkeliate senos peržiūros laukelius į naujos peržiūros laukelius, kai vykdoma peržiūros kūrėjo sinchronizacija.

Pavyzdžiui, jūs įtraukėte tolesnius keturi laukelius į `InventTable` lentelę per plėtinius:

- Tinkintas laukelis 1
- Tinkintas laukelis 2
- Tinkintas laukelis 3
- Tinkintas laukelis 4

Tuo atveju, privalote keisti `getExtensionFields()` būdą tolesniu būdu.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Kai pabaigėte šiuos žingsnius, galite išplėsti turimas atsargas vietoje ir turimas atsargas pagal sandėlio duomenų objektus įtraukiant naujus laukelius. Tokiu būdu, užtikrinkite, kad išplėsti laukeliai yra pripažįstami ir įtraukti į duomenų perkėlimą, kuris naudoja tuos duomenų objektus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]