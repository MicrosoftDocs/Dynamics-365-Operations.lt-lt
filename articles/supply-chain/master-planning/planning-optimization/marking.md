---
title: Inventoriaus ženklinimas su „Planning Optimization“
description: Šiame skyriuje pateikta informacija apie parinktis, kurios yra prieinamos inventoriaus ženklinimui patvirtintuose užsakymuose jums naudojant „Planning Optimization“.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3b139673ddf17e13d6687db485208e1aeb3908dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809499"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="f761f-103">Inventoriaus ženklinimas su „Planning Optimization“</span><span class="sxs-lookup"><span data-stu-id="f761f-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f761f-104">Šiame skyriuje pateikta informacija apie parinktis, kurios yra prieinamos inventoriaus ženklinimui patvirtintuose užsakymuose jums naudojant „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="f761f-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="f761f-105">*Ženklinimas* naudojamas susieti paklausą ir pasiūlą.</span><span class="sxs-lookup"><span data-stu-id="f761f-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="f761f-106">Jis atspindi *fiksavimą*, kuris nurodo, kaip pagrindinis planavimas tikisi padengti paklausą.</span><span class="sxs-lookup"><span data-stu-id="f761f-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="f761f-107">Planavimo požiūriu, pagrindinis skirtumas tas, kad ženklinimas yra pastovesnis nei fiksavimas.</span><span class="sxs-lookup"><span data-stu-id="f761f-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="f761f-108">Ženklinimas buvo įvestas siekiant palaikyti specialius kaštų scenarijus pirmajam patenkančiam ir pirmajam išeinančiam (FIFO) ir paskutiniam įeinančiam ir pirmam išeinančiam (LIFO).</span><span class="sxs-lookup"><span data-stu-id="f761f-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="f761f-109">Nepaisant to, dabar jis taip pat naudojamas kai kuriuose ne kaštų scenarijuose.</span><span class="sxs-lookup"><span data-stu-id="f761f-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="f761f-110">Ženklinimas tarp pasiūlos ir paklausos yra pasirenkamas ir beveik pastovus.</span><span class="sxs-lookup"><span data-stu-id="f761f-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="f761f-111">Ženklinimas gali būti pašalinamas rankiniu būdu vartotojo arba vykdant pardavimo užsakymo eilutės sprogimą, kai **Ženklinimo pašalinimo** parinktis pasirenkama.</span><span class="sxs-lookup"><span data-stu-id="f761f-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="f761f-112">Fiksavimą valdo pagrindinis planavimas aprėpties metu susiejant paklausą su būtina pasiūla.</span><span class="sxs-lookup"><span data-stu-id="f761f-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="f761f-113">Fiksavimą galima naujinti kiekvieno planavimo vykdymo metu siekiant optimizuoti pasiūlą, kuri būtina padengti paklausą.</span><span class="sxs-lookup"><span data-stu-id="f761f-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="f761f-114">Kai pagrindinis planavimas naujina fiksavimo informaciją, jis laikosi esančio ženklinimo.</span><span class="sxs-lookup"><span data-stu-id="f761f-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="f761f-115">Fiksavimas prasideda įskaitant atitinkamą ženklinimą, turimas rezervacijas ir užsakymo rezervacijas tolesne seka:</span><span class="sxs-lookup"><span data-stu-id="f761f-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="f761f-116">Ženklinimas tarp pasiūlos ir paklausos</span><span class="sxs-lookup"><span data-stu-id="f761f-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="f761f-117">Turimo rezervacijos</span><span class="sxs-lookup"><span data-stu-id="f761f-117">On-hand reservations</span></span>
1. <span data-ttu-id="f761f-118">Užsakymo rezervacijos</span><span class="sxs-lookup"><span data-stu-id="f761f-118">On-order reservations</span></span>

<span data-ttu-id="f761f-119">Kai patvirtinate suplanuotą užsakymą, **Patvirtinimo** teksto laukelis rodo **Naujinto ženklinimo** laukelį, kurį naudojate siekiant nustatyti ženklinimo parinktis užsakymams sukurtiems patvirtinimo metu.</span><span class="sxs-lookup"><span data-stu-id="f761f-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="f761f-120">Pasirinkite vieną iš šių reikšmių:</span><span class="sxs-lookup"><span data-stu-id="f761f-120">Select one of the following values:</span></span>

- <span data-ttu-id="f761f-121">**Ne** – Joks inventoriaus ženklinimas nėra taikomas.</span><span class="sxs-lookup"><span data-stu-id="f761f-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="f761f-122">**Standartinis** – Inventoriaus ženklinimas yra naujinamas pagal fiksavimą.</span><span class="sxs-lookup"><span data-stu-id="f761f-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="f761f-123">Reikalavimo užsakymas (paklausa) yra ženklinamas pagal įgyvendinimo užsakymą (pasiūlą).</span><span class="sxs-lookup"><span data-stu-id="f761f-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="f761f-124">Jei keletas kiekių lieka įgyvendinimo užsakyme, jis neženklinamas ir atitinkama informacija paliekama tuščia.</span><span class="sxs-lookup"><span data-stu-id="f761f-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="f761f-125">Pavyzdžiui, jei pardavimo užsakymas 100 ea yra fiksuojamas pagal pirkimo užsakymą 150 ea, atitinkama informacija bus priskirta tik pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="f761f-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="f761f-126">**Išplėstas** – Tiek reikalavimo užsakymas (paklausa), tiek įgyvendinimo užsakymas (pasiūla) bus paženklinti nepriklausomai nuo bet kokio kiekio, kuris lieka įgyvendinimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="f761f-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="f761f-127">Pavyzdžiui, jei pardavimo užsakymas 100 ea yra fiksuojamas pagal pirkimo užsakymą 150 ea, atitinkama informacija bus priskirta tiek pardavimo užsakymui, tiek pirkimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="f761f-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]