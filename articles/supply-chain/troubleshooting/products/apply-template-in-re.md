---
title: Negalima taikyti šablono išleistame produkte
description: Negalima taikyti šablono išleistame produkte.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026738"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="92829-103">Negalima kurti šablono išleistame produkte.</span><span class="sxs-lookup"><span data-stu-id="92829-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="92829-104">KB numeris: 4612097</span><span class="sxs-lookup"><span data-stu-id="92829-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="92829-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="92829-105">Symptoms</span></span>

<span data-ttu-id="92829-106">Kai sukuriate naują išleistą produktą, naudodami dialogo langą **Naujas išleistas produktas**, galite pasirinkti šabloną.</span><span class="sxs-lookup"><span data-stu-id="92829-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="92829-107">Šablonas turi pateikti numatytuosius daugelio naujo išleisto produkto laukų parametrus.</span><span class="sxs-lookup"><span data-stu-id="92829-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="92829-108">Tačiau kai kurie arba visi laukai nėra nustatomi jums pažymus šabloną.</span><span class="sxs-lookup"><span data-stu-id="92829-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="92829-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="92829-109">Cause</span></span>

<span data-ttu-id="92829-110">Daug puslapių „Microsoft Dynamics 365 Supply Chain Management“ leidžia jums sukurti šabloną, kuris nustato pradinius įrašams, kurie rodomi tuose puslapiuose, parametrus.</span><span class="sxs-lookup"><span data-stu-id="92829-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="92829-111">Vieną iš šių šablonų galite sukurti **veiksmų srities** skirtuke **Pasirinktys** pasirinkdami Įrašo informacija.</span><span class="sxs-lookup"><span data-stu-id="92829-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="92829-112">Tačiau išleisti produktai yra daug sudėtingesni nei dauguma kitų įrašų tipų.</span><span class="sxs-lookup"><span data-stu-id="92829-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="92829-113">Nepaisant to, kad galite pasirinkti **Įrašo informacija** puslapyje **Išleisti produktai** tačiau norėdami sukurti šabloną galite pasirinkti jį, kai kuriate išleistą produktą, šablone nebus pateikti numatytų naujo išleisto produkto laukų verčių.</span><span class="sxs-lookup"><span data-stu-id="92829-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="92829-114">Todėl išleistiems produktams negalite naudoti „įrašų informacijos“ šablonų.</span><span class="sxs-lookup"><span data-stu-id="92829-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="92829-115">Užuot tai darę, turite sukurti paskirtus produktų šablonus.</span><span class="sxs-lookup"><span data-stu-id="92829-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="92829-116">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="92829-116">Resolution</span></span>

<span data-ttu-id="92829-117">Norėdami sukurti produkto šabloną, naudokite **Šablonas** meniu **Produktas** skirtuke veiksmuų juostoje, o ne **Įrašo informacijos** mygtuką **Parinktys** skirtuke.</span><span class="sxs-lookup"><span data-stu-id="92829-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="92829-118">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="92829-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="92829-119">Veiksmų juostoje **Produktas** skirtuke **Nauja** grupė rinkitės **Šablonas** ir rinkitės **Kurti asmeninį šabloną** ar **Kurti bendrintą šabloną**, kaip tinkama.</span><span class="sxs-lookup"><span data-stu-id="92829-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
