---
title: Brūkšninių kodų nustatymas
description: Šiame straipsnyje aprašyta, kaip naudoti brūkšninius kodus sprendime „Dynamics 365 Commerce“.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52801e0d09b1d7da50719966700ca45275d702f7
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057283"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="e4325-103">Brūkšninių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="e4325-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4325-104">Šiame straipsnyje aprašyta, kaip naudoti brūkšninius kodus sprendime „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e4325-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e4325-105">Brūkšninius kodus galite naudoti norėdami pirkti ir parduoti produktus, sekti produktų variantus ir nustatyti klientus ir darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="e4325-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="e4325-106">Brūkšninius kodus dar galite naudoti norėdami išduoti ir patvirtinti kuponus, dovanų korteles, ir kredito pažymas.</span><span class="sxs-lookup"><span data-stu-id="e4325-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="e4325-107">Galite taip nustatyti produktus, kad jie būtų su standartiniais arba pasirinktiniais vietiniais brūkšniniais kodais.</span><span class="sxs-lookup"><span data-stu-id="e4325-107">You can set up products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="e4325-108">Produktai gali turėti daugiau nei vieną brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="e4325-108">Products can have more than one bar code.</span></span> <span data-ttu-id="e4325-109">Pvz., produktas gali turėti keletą brūkšninių kodų, jei jis atvežtas iš įvairių gamintojų arba jei jis turi variantų, pagal dydį, stilių ar spalvą.</span><span class="sxs-lookup"><span data-stu-id="e4325-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="e4325-110">Brūkšniniai kodai gali apimti produkto svorį arba kainą.</span><span class="sxs-lookup"><span data-stu-id="e4325-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="e4325-111">Brūkšninių kodų skaičių sekos yra šablonai, naudojami brūkšniniams kodams kurti.</span><span class="sxs-lookup"><span data-stu-id="e4325-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="e4325-112">Kiekvienam variantų deriniui priskyrę unikalų brūkšninį kodą galėsite nuskaityti brūkšninį kodą registre ir leisti programai nustatyti, kuris produkto variantas parduodamas.</span><span class="sxs-lookup"><span data-stu-id="e4325-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="e4325-113">Taip pat galite kaupti ir pagal variantą peržiūrėti pardavimo statistiką.</span><span class="sxs-lookup"><span data-stu-id="e4325-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="e4325-114">Kiekvienai dydžių, spalvų ir stilių grupei galima priskirti unikalų numerį, identifikuojantį tą grupę brūkšniniame kode.</span><span class="sxs-lookup"><span data-stu-id="e4325-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="e4325-115">„Commerce“ brūkšninio kodo skaičių seką naudoja tam, kad būtų automatiškai sugeneruoti kiekvieno variantų derinio brūkšniniai kodai.</span><span class="sxs-lookup"><span data-stu-id="e4325-115">Commerce uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="e4325-116">Ši funkcija gali būti naudinga, jei yra daug dydžių, spalvų ir stilių, nes kombinacijų skaičius žymiai padidėja kartu su kiekvienu papildomai įtrauktu varianto kodu.</span><span class="sxs-lookup"><span data-stu-id="e4325-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="e4325-117">Jei ši funkcija nenaudojama, kiekvienai kombinacijai brūkšninius kodus, reiškiančius produkto variantą, reikia priskirti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="e4325-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="e4325-118">Brūkšninius kodus galite kurti rankiniu būdu arba automatiškai.</span><span class="sxs-lookup"><span data-stu-id="e4325-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="e4325-119">Norėdami kurti brūkšninius kodus, atlikite nurodytas užduotis ta tvarka, kuria jos išvardytos.</span><span class="sxs-lookup"><span data-stu-id="e4325-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="e4325-120">[Brūkšninio kodo skaičių sekos simbolių nustatymas](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="e4325-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="e4325-121">[Brūkšninių kodų skaičių sekų nustatymas](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="e4325-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="e4325-122">Konfigūruokite brūkšninių kodų nustatymus.</span><span class="sxs-lookup"><span data-stu-id="e4325-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="e4325-123">Kurkite produktų brūkšninius kodus.</span><span class="sxs-lookup"><span data-stu-id="e4325-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4325-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e4325-124">Additional resources</span></span>

[<span data-ttu-id="e4325-125">Brūkšninių kodų skaičių sekų nustatymas</span><span class="sxs-lookup"><span data-stu-id="e4325-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)