---
title: Nuolaidų mažmeninės prekybos produktams nesuteikimo parinktys
description: Yra įvairių priežasčių, dėl kurių mažmenininkai gali norėti nesuteikti kai kuriems produktams nuolaidų EKA akcijų arba išpardavimų metu.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: c9d3e7af95dffddfddc34059d93a2a5a350d08e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550749"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="cf344-103">Nuolaidų mažmeninės prekybos produktams nesuteikimo parinktys</span><span class="sxs-lookup"><span data-stu-id="cf344-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf344-104">Yra įvairių priežasčių, dėl kurių mažmenininkai gali norėti nesuteikti kai kuriems produktams nuolaidų EKA akcijų arba išpardavimų metu.</span><span class="sxs-lookup"><span data-stu-id="cf344-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="cf344-105">Tolesnės pasirinktys, kurias galima rasti produktų skirtuke **Mažmeninė prekyba** leis konfigūruoti produktą, kad jam nebūtų teikiamos jokios arba pasirinktinės nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="cf344-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="cf344-106">Parametrus taip pat galima nurodyti kategorijos lygiu iš mažmeninės prekybos kategorijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="cf344-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="cf344-107">**Neleisti jokių nuolaidų** – pasirinkite šią parinktį norėdami neleisti šiam produktui taikyti jokių tipų nuolaidų.</span><span class="sxs-lookup"><span data-stu-id="cf344-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="cf344-108">Tai apima akcijas prekių rinkiniams, nuolaidas dėl kiekio ir rankinės eilutės ir operacijų nuolaidas, kurias pardavimų metu taiko EKA vartotojas.</span><span class="sxs-lookup"><span data-stu-id="cf344-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="cf344-109">**Neleisti rankiniu būdu nustatomų nuolaidų** – pasirinkite šią parinktį norėdami neleisti rankiniu būdu nustatomos eilutės arba operacijos nuolaidų, kurias pardavimo metu taiko EKA vartotojas.</span><span class="sxs-lookup"><span data-stu-id="cf344-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="cf344-110">Produktai su šia parinktimi vis tiek gali būti įtraukiami į reklamines akcijas, pvz., nuolaidas prekių rinkiniams ir kiekio nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="cf344-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="cf344-111">Šie parametrai neapriboja kainos perrašymo operacijos, nes nustatoma bazinė kaina, kuri nėra laikoma nuolaida.</span><span class="sxs-lookup"><span data-stu-id="cf344-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="cf344-112">[![neleisti nuolaidų lauko](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="cf344-112">[![prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
