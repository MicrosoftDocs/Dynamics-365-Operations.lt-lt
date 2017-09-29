---
title: "Brūkšninių kodų nustatymas"
description: "Šiame straipsnyje aprašyta, kaip naudoti brūkšninius kodus sprendime „Microsoft Dynamics 365 for Retail“."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fdc56bf468babd4b0b0652d9791114af676c8470
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="407d4-103">Brūkšninių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="407d4-103">Set up bar codes</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="407d4-104">Šiame straipsnyje aprašyta, kaip naudoti brūkšninius kodus sprendime „Microsoft Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="407d4-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="407d4-105">Brūkšninius kodus galite naudoti norėdami pirkti ir parduoti produktus, sekti produktų variantus ir nustatyti klientus ir darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="407d4-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="407d4-106">Brūkšninius kodus dar galite naudoti norėdami išduoti ir patvirtinti kuponus, dovanų korteles, ir kredito pažymas.</span><span class="sxs-lookup"><span data-stu-id="407d4-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="407d4-107">Galite taip nustatyti mažmenines prekybos produktus, kad jie būtų su standartiniais arba pasirinktiniais vietiniais brūkšniniais kodais.</span><span class="sxs-lookup"><span data-stu-id="407d4-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="407d4-108">Produktai gali turėti daugiau nei vieną brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="407d4-108">Products can have more than one bar code.</span></span> <span data-ttu-id="407d4-109">Pvz., produktas gali turėti keletą brūkšninių kodų, jei jis atvežtas iš įvairių gamintojų arba jei jis turi variantų, pagal dydį, stilių ar spalvą.</span><span class="sxs-lookup"><span data-stu-id="407d4-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="407d4-110">Brūkšniniai kodai gali apimti produkto svorį arba kainą.</span><span class="sxs-lookup"><span data-stu-id="407d4-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="407d4-111">Brūkšninių kodų skaičių sekos yra šablonai, naudojami brūkšniniams kodams kurti.</span><span class="sxs-lookup"><span data-stu-id="407d4-111">Bar code masks are templates that are used to create bar codes.</span></span> <span data-ttu-id="407d4-112">**Pastaba:** kiekvienam variantų deriniui priskyrę unikalų brūkšninį kodą galėsite nuskaityti brūkšninį kodą registre ir leisti programai nustatyti, kuris produkto variantas parduodamas.</span><span class="sxs-lookup"><span data-stu-id="407d4-112">**Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="407d4-113">Taip pat galite kaupti ir pagal variantą peržiūrėti pardavimo statistiką.</span><span class="sxs-lookup"><span data-stu-id="407d4-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="407d4-114">Kiekvienai dydžių, spalvų ir stilių grupei galima priskirti unikalų numerį, identifikuojantį tą grupę brūkšniniame kode.</span><span class="sxs-lookup"><span data-stu-id="407d4-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="407d4-115">„Microsoft Dynamics 365 for Retail“ brūkšninio kodo skaičių seką naudoja tam, kad būtų automatiškai sugeneruoti kiekvieno variantų derinio brūkšniniai kodai.</span><span class="sxs-lookup"><span data-stu-id="407d4-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="407d4-116">Ši funkcija gali būti naudinga, jei yra daug dydžių, spalvų ir stilių, nes kombinacijų skaičius žymiai padidėja kartu su kiekvienu papildomai įtrauktu varianto kodu.</span><span class="sxs-lookup"><span data-stu-id="407d4-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="407d4-117">Jei ši funkcija nenaudojama, kiekvienai kombinacijai brūkšninius kodus, reiškiančius produkto variantą, reikia priskirti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="407d4-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span> <span data-ttu-id="407d4-118">Brūkšninius kodus galite kurti rankiniu būdu arba automatiškai.</span><span class="sxs-lookup"><span data-stu-id="407d4-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="407d4-119">Norėdami kurti brūkšninius kodus, atlikite nurodytas užduotis ta tvarka, kuria jos išvardytos.</span><span class="sxs-lookup"><span data-stu-id="407d4-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1.  <span data-ttu-id="407d4-120">[Brūkšninio kodo skaičių sekos simbolių nustatymas](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="407d4-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2.  <span data-ttu-id="407d4-121">[Brūkšninių kodų skaičių sekų nustatymas](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="407d4-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3.  <span data-ttu-id="407d4-122">Konfigūruokite brūkšninių kodų nustatymus.</span><span class="sxs-lookup"><span data-stu-id="407d4-122">Configure bar code setups.</span></span>
4.  <span data-ttu-id="407d4-123">Kurkite produktų brūkšninius kodus.</span><span class="sxs-lookup"><span data-stu-id="407d4-123">Create bar codes for products.</span></span>


<a name="see-also"></a><span data-ttu-id="407d4-124">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="407d4-124">See also</span></span>
--------

[<span data-ttu-id="407d4-125">Brūkšninių kodų skaičių sekų nustatymas</span><span class="sxs-lookup"><span data-stu-id="407d4-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)




