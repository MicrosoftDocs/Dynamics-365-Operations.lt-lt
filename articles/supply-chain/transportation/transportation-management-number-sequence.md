---
title: Gabenimo valdymo nuolaidos skaičių seka
description: Šiame skyriuje paaiškinta, kaip nustatyti skaičių seką gabenimo valdymui.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cc19110f481c11ab28532d69a4689c1db048f6c3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233372"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="481d0-103">Gabenimo valdymo nuolaidos skaičių seka</span><span class="sxs-lookup"><span data-stu-id="481d0-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="481d0-104">Naudokite **Skaičių sekas** puslapį gabenimo valdymo modulyje siekiant nustatyti įvairius pro skaičius.</span><span class="sxs-lookup"><span data-stu-id="481d0-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="481d0-105">Pro skaičiai yra naudojami vežėjų siekiant organizuoti ir stebėti kiekvieno siuntimo progresą.</span><span class="sxs-lookup"><span data-stu-id="481d0-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="481d0-106">Sukurkite skaičių seką pro skaičiui</span><span class="sxs-lookup"><span data-stu-id="481d0-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="481d0-107">Norėdami sukurti skaičių seką pro skaičiui, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="481d0-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="481d0-108">Eikite į **Gabenimo valdymas \> Nustatymai \> Vežėjai \> Skaičių sekos**.</span><span class="sxs-lookup"><span data-stu-id="481d0-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="481d0-109">Pasirinkite **Naujas**, kad sukurtumėte naują skaičių seką.</span><span class="sxs-lookup"><span data-stu-id="481d0-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="481d0-110">Įveskite unikalų ID ir būdo pavadinimo aprašą skaičių sekai.</span><span class="sxs-lookup"><span data-stu-id="481d0-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="481d0-111">Laukelyje **Skaičių sekos tipas**, *Pro skaičius* yra vienintelė parinktis.</span><span class="sxs-lookup"><span data-stu-id="481d0-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="481d0-112">Laukelyje **TIkrinti skaitmenį**, *Tikrinti skaitmenį* yra vienintelė parinktis ir nustatyta kaip bendras variklis.</span><span class="sxs-lookup"><span data-stu-id="481d0-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="481d0-113">„FastTab“ **Seka** pateikite informaciją apie seką.</span><span class="sxs-lookup"><span data-stu-id="481d0-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="481d0-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="481d0-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="481d0-115">Susiekita skaičių seką su siunčiančiu vežėju</span><span class="sxs-lookup"><span data-stu-id="481d0-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="481d0-116">Norėdami susieti skaičių seką su vežėju, elkitės taip:</span><span class="sxs-lookup"><span data-stu-id="481d0-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="481d0-117">Eikite į **Transportavimo valdymas \> Nustatymas \> Vežėjai \> Siuntų vežėjai**.</span><span class="sxs-lookup"><span data-stu-id="481d0-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="481d0-118">Pasirinkite gabenimo vežėją.</span><span class="sxs-lookup"><span data-stu-id="481d0-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="481d0-119">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="481d0-119">Select **Edit**.</span></span>
1. <span data-ttu-id="481d0-120">„FastTav“ **Apžvalga**, pasirinkite parinktį **Pro skaičiaus seka** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="481d0-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="481d0-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="481d0-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]