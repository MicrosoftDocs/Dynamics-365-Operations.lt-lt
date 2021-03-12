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
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7c408068ece94d47c0f41e286a2ce0ae7efd23dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972505"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="91f90-103">Nuolaidų mažmeninės prekybos produktams nesuteikimo parinktys</span><span class="sxs-lookup"><span data-stu-id="91f90-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91f90-104">Yra įvairių priežasčių, dėl kurių mažmenininkai gali norėti nesuteikti kai kuriems produktams nuolaidų EKA akcijų arba išpardavimų metu.</span><span class="sxs-lookup"><span data-stu-id="91f90-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="91f90-105">Šios parinktys, kurias galima rasti išleistų produktų skirtuke **„+Commerce“**, leidžia sukonfigūruoti produktą, kad būtų išvengta visų ar rankiniu būdu nustatomų nuolaidų.</span><span class="sxs-lookup"><span data-stu-id="91f90-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="91f90-106">Parametrus taip pat galima nurodyti kategorijos lygiu iš kategorijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="91f90-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="91f90-107">**Neleisti jokių nuolaidų** – pasirinkite šią parinktį norėdami neleisti šiam produktui taikyti jokių tipų nuolaidų.</span><span class="sxs-lookup"><span data-stu-id="91f90-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="91f90-108">Tai apima akcijas prekių rinkiniams, nuolaidas dėl kiekio ir rankinės eilutės ir operacijų nuolaidas, kurias pardavimų metu taiko EKA vartotojas.</span><span class="sxs-lookup"><span data-stu-id="91f90-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="91f90-109">**Neleisti rankiniu būdu nustatomų nuolaidų** – pasirinkite šią parinktį norėdami neleisti rankiniu būdu nustatomos eilutės arba operacijos nuolaidų, kurias pardavimo metu taiko EKA vartotojas.</span><span class="sxs-lookup"><span data-stu-id="91f90-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="91f90-110">Produktai su šia parinktimi vis tiek gali būti įtraukiami į reklamines akcijas, pvz., nuolaidas prekių rinkiniams ir kiekio nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="91f90-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="91f90-111">Šie parametrai neapriboja kainos perrašymo operacijos, nes nustatoma bazinė kaina, kuri nėra laikoma nuolaida.</span><span class="sxs-lookup"><span data-stu-id="91f90-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="91f90-112">[![Neleisti nuolaidų lauko](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="91f90-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
