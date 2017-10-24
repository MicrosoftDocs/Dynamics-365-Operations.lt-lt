---
title: "Mišrių numerio lentelių gavimas"
description: "Šioje temoje aprašoma, kaip naudoti mišrių numerio lentelių gavimą, norint užregistruoti ir sukurti kelių prekių darbą su mobiliuoju įrenginiu."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e785d71e7ae3c5f60d36d8b190001b5e356c626
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="17c4e-103">Mišrių numerio lentelių gavimas</span><span class="sxs-lookup"><span data-stu-id="17c4e-103">Mixed license plate receiving</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="17c4e-104">Mišrių numerio lentelių gavimas leidžia sukurti numerio lentelę, sudarytą iš kelių prekių, prieš registruojant ir kuriant atidėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="17c4e-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="17c4e-105">Numerio lentelė, sudaryta iš kelių prekių, gavimo rampoje neturi būti padalyta tam, kad užregistruotumėte kiekvieną prekę.</span><span class="sxs-lookup"><span data-stu-id="17c4e-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="17c4e-106">Naudodami su preke susijusį srautą, kad nustatytumėte šaltinio dokumento eilutes, galite nuskaityti brūkšninius kodus prekės valdiklyje.</span><span class="sxs-lookup"><span data-stu-id="17c4e-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="17c4e-107">Jei brūkšniniame kode sukonfigūruoti kiekis ir matavimo vienetas (MV), prekė ir kiekis bus automatiškai pridėti į mišrią numerio lentelę, ir jūs būsite grąžinti į ekraną, skirtą nuskaityti kitą prekę.</span><span class="sxs-lookup"><span data-stu-id="17c4e-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="17c4e-108">Tai leidžia greitai nuskaityti visas prekes neatliekant patvirtinimo kiekviename veiksme.</span><span class="sxs-lookup"><span data-stu-id="17c4e-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="17c4e-109">Mišrios numerio lentelės gavimo sraute gali būti rodomas į mišrią numerio lentelę jau nuskaitytų prekių sąrašas, čia galite modifikuoti arba koreguoti prekės kiekį.</span><span class="sxs-lookup"><span data-stu-id="17c4e-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="17c4e-110">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="17c4e-110">Where it applies</span></span>

<span data-ttu-id="17c4e-111">Mišrios numerio lentelės gavimas yra mobiliojo įrenginio gavimo srautas, skirtas užregistruoti ir sukurti kelių eilučių / prekių darbą tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="17c4e-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="17c4e-112">Tai naudinga, jei gaunate gavimo numerio lenteles su keliomis prekėmis.</span><span class="sxs-lookup"><span data-stu-id="17c4e-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="17c4e-113">Kaip nustatyti mišrių numerio lentelių gavimą</span><span class="sxs-lookup"><span data-stu-id="17c4e-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="17c4e-114">Mišrių numerio lentelių gavimas nustatomas kaip mobiliojo įrenginio meniu elementas.</span><span class="sxs-lookup"><span data-stu-id="17c4e-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="17c4e-115">Turite sukurti naują meniu elementą režimu Darbas, kuriame nenaudojamas esamas darbas, ir naudojamas vienas iš nurodytų metodų.</span><span class="sxs-lookup"><span data-stu-id="17c4e-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="17c4e-116">Mišrių numerio lentelių gavimas</span><span class="sxs-lookup"><span data-stu-id="17c4e-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="17c4e-117">Mišrių numerio lentelių gavimas ir padėjimas</span><span class="sxs-lookup"><span data-stu-id="17c4e-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="17c4e-118">Parinktys, skirtos identifikuoti šaltinio dokumento eilutes, yra pirkimo užsakymo prekė, pirkimo užsakymo eilutė, grąžinimo užsakymas, perkėlimo užsakymo prekė ir perkėlimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="17c4e-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="17c4e-119">Šios parinktys gali pakeisti gavimo užsakymą vienoje numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="17c4e-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="17c4e-120">Paskutinė parinktis yra pagal krovinio prekę.</span><span class="sxs-lookup"><span data-stu-id="17c4e-120">The last option is by load item.</span></span> <span data-ttu-id="17c4e-121">Į numerio lentelę galite pridėti kelias prekes, tačiau negalite keisti vieno krovinio į kitą.</span><span class="sxs-lookup"><span data-stu-id="17c4e-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>

