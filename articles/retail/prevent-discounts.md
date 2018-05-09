---
title: "Nuolaidų nesuteikimas mažmeninės prekybos produktams"
description: "Yra įvairių priežasčių, dėl kurių mažmenininkai gali norėti nesuteikti kai kuriems produktams nuolaidų EKA akcijų arba išpardavimų metu."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3b10270ea410b45d8c39885b3b87183b078378e0
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="prevent-discounts-for-retail-products"></a><span data-ttu-id="e889a-103">Nuolaidų nesuteikimas mažmeninės prekybos produktams</span><span class="sxs-lookup"><span data-stu-id="e889a-103">Prevent discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e889a-104">Yra įvairių priežasčių, dėl kurių mažmenininkai gali norėti nesuteikti kai kuriems produktams nuolaidų EKA akcijų arba išpardavimų metu.</span><span class="sxs-lookup"><span data-stu-id="e889a-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="e889a-105">Tolesnės pasirinktys, kurias galima rasti produktų skirtuke **Mažmeninė prekyba** leis konfigūruoti produktą, kad jam nebūtų teikiamos jokios arba pasirinktinės nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="e889a-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="e889a-106">Parametrus taip pat galima nurodyti kategorijos lygiu iš mažmeninės prekybos kategorijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="e889a-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

<span data-ttu-id="e889a-107">**Neleisti jokių nuolaidų**: pasirinkite šią pasirinktį norėdami neleisti šiam produktui taikyti jokių tipų nuolaidų.</span><span class="sxs-lookup"><span data-stu-id="e889a-107">**Prevent all discounts**: Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="e889a-108">Tai apima akcijas prekių rinkiniams, nuolaidas dėl kiekio ir rankinės eilutės ir operacijų nuolaidas, kurias pardavimų metu taiko EKA vartotojas.</span><span class="sxs-lookup"><span data-stu-id="e889a-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>

<span data-ttu-id="e889a-109">**Neleisti rankiniu būdu nustatomų nuolaidų**: pasirinkite šią pasirinktį norėdami neleisti rankiniu būdu nustatomos eilutės arba operacijos nuolaidų, kurias pardavimo metu taiko EKA vartotojas.</span><span class="sxs-lookup"><span data-stu-id="e889a-109">**Prevent manual discounts**: Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="e889a-110">Produktai su šia parinktimi vis tiek gali būti įtraukiami į reklamines akcijas, pvz., nuolaidas prekių rinkiniams ir kiekio nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="e889a-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

<span data-ttu-id="e889a-111">**Pastaba**: šie parametrai neapriboja kainos perrašymo operacijos, nes nustatoma bazinė kaina, kuri nėra laikoma nuolaida.</span><span class="sxs-lookup"><span data-stu-id="e889a-111">**Note**: These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>  

<span data-ttu-id="e889a-112">[![neleisti nuolaidų lauko](./media/prevent discounts.png)](./media/prevent discounts.png)</span><span class="sxs-lookup"><span data-stu-id="e889a-112">[![prevent discounts field](./media/prevent discounts.png)](./media/prevent discounts.png)</span></span>

