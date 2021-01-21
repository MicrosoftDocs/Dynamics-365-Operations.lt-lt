---
title: Turimų atsargų duomenų objektų pratęsimas
description: Ši tema aprašo pavyzdį, kuris rodo, kaip įtraukti išplėstus laukelius į ATSARGŲTURIMOSVIETOSOBJEKTĄ ir ATSARGŲSANDĖLYJETURIMĄOBJEKTĄ peržiūras taip, kad turimų duomenų atsargų pajėgumo objektai galėtų veikti su plėtiniais.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: e276348a63bfdb9e712c0ea86e6c2a68c50872c0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665409"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="b1aa2-103">Turimų atsargų duomenų objektų pratęsimas</span><span class="sxs-lookup"><span data-stu-id="b1aa2-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1aa2-104">„Microsoft Dynamics 365 Supply Chain Management“ pateikia [plėtinių](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) funkcijas, kurios jums leidžia [įtraukti laukelius į lenteles per plėtinius](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span><span class="sxs-lookup"><span data-stu-id="b1aa2-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="b1aa2-105">Šioje temoje pateiktas pavyzdys, kuris rodo, kaip įtraukti išplėstus laukelius į `INVENTORSITEONHANDENTITY` ir `INVENTWAREHOUSEONHANDENTITY` peržiūras taip, kad turimų duomenų atsargų pajėgumo objektai galėtų veikti su plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="b1aa2-106">Dėl išsamesnės informacijos apie duomenų objektus, žr. [Duomenų valdymo peržiūrą](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="b1aa2-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b1aa2-107">Čia pateikiamas kai kurių turimų duomenų objektų atsargų sąrašą: </span><span class="sxs-lookup"><span data-stu-id="b1aa2-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="b1aa2-108">Turimos atsargos pagal vietą</span><span class="sxs-lookup"><span data-stu-id="b1aa2-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="b1aa2-109">Turimos atsargos pagal vietą V2</span><span class="sxs-lookup"><span data-stu-id="b1aa2-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="b1aa2-110">Turimos atsargos pagal sandėlį</span><span class="sxs-lookup"><span data-stu-id="b1aa2-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="b1aa2-111">Turimos atsargos sandėlyje v2</span><span class="sxs-lookup"><span data-stu-id="b1aa2-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="b1aa2-112">Po to, kai įtraukėte laukelius į lenteles, kurios yra naudojamos `inventSiteOnHandView` peržiūroje, privalote sinchronizuoti variklį taip, kad plėtiniai būtų tinkamai atpažinti.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="b1aa2-113">Išplėskite `InventSiteOnHandView` peržiūrą įtraukdami plėtinio laukelį.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="b1aa2-114">Išplėskite `InventSiteOnHandAggregatedView` peržiūrą su plėtinio laukeliais.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="b1aa2-115">Išplėskite `InventSiteOnHandAggregatedViewBuilder` peržiūros kūrėjo klasę keisdami `getExtensionFields()` būdą.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="b1aa2-116">Tokiu būdu, įkeliate senos peržiūros laukelius į naujos peržiūros laukelius, kai vykdoma peržiūros kūrėjo sinchronizacija.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="b1aa2-117">Pavyzdžiui, jūs įtraukėte tolesnius keturi laukelius į `InventTable` lentelę per plėtinius:</span><span class="sxs-lookup"><span data-stu-id="b1aa2-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="b1aa2-118">Tinkintas laukelis 1</span><span class="sxs-lookup"><span data-stu-id="b1aa2-118">Custom field 1</span></span>
- <span data-ttu-id="b1aa2-119">Tinkintas laukelis 2</span><span class="sxs-lookup"><span data-stu-id="b1aa2-119">Custom field 2</span></span>
- <span data-ttu-id="b1aa2-120">Tinkintas laukelis 3</span><span class="sxs-lookup"><span data-stu-id="b1aa2-120">Custom field 3</span></span>
- <span data-ttu-id="b1aa2-121">Tinkintas laukelis 4</span><span class="sxs-lookup"><span data-stu-id="b1aa2-121">Custom field 4</span></span>

<span data-ttu-id="b1aa2-122">Tuo atveju, privalote keisti `getExtensionFields()` būdą tolesniu būdu.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

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

<span data-ttu-id="b1aa2-123">Kai pabaigėte šiuos žingsnius, galite išplėsti turimas atsargas vietoje ir turimas atsargas pagal sandėlio duomenų objektus įtraukiant naujus laukelius.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="b1aa2-124">Tokiu būdu, užtikrinkite, kad išplėsti laukeliai yra pripažįstami ir įtraukti į duomenų perkėlimą, kuris naudoja tuos duomenų objektus.</span><span class="sxs-lookup"><span data-stu-id="b1aa2-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>