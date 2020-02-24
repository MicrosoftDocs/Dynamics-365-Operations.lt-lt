---
title: Produktų, kurie nėra parduotuvės asortimento dalis, pardavimas ir grąžinimas
description: Naudodami „Dynamics 365 Commerce“ galite parduoti ir grąžinti į asortimentus neįtrauktus produktus.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023441"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="ae2d6-103">Produktų, kurie nėra parduotuvės asortimento dalis, pardavimas ir grąžinimas</span><span class="sxs-lookup"><span data-stu-id="ae2d6-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae2d6-104">Bet kokiam mažmenininkui dažnai pasitaiko situacija, kai reikia klientams parduoti produktus ar iš klientų priimti grąžinamus produktus net jei konkretūs produktai jų parduotuvėje neplatinami (kitaip tariant, produktai nėra įtraukti į parduotuvės asortimentą).</span><span class="sxs-lookup"><span data-stu-id="ae2d6-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="ae2d6-105">Toliau nurodomi įprasti scenarijai.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="ae2d6-106">Mažmenininkas konkrečioje parduotuvėje neplatina visų savo produktų.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="ae2d6-107">Likę produktai saugomi sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="ae2d6-108">Parduotuvės atstovas gali klientui padėti ir produktų ieškoti ar juos naršyti sandėlyje, įtraukti produktus į krepšelį ir pasirinkdamas pristatymo būdą, pvz., iš sandėlio siųsti tam tikru adresu arba klientui leisti produktą pasiimti iš dabartinės ar kitos parduotuvės, užbaigti pirkimą.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="ae2d6-109">Mažmenininkas konkrečių produktų parduotuvėje neplatina arba jų neturi kliento aplankytoje parduotuvėje, tačiau produktai yra kitose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="ae2d6-110">Parduotuvės atstovas gali klientui padėti ir produktų ieškoti ar juos naršyti kitoje parduotuvėje, įtraukti produktus į krepšelį ir pasirinkdamas pristatymo būdą užbaigti pirkimą.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="ae2d6-111">Mažmenininkas konkrečiame mieste ar pašto indekso teritorijoje arba aplink juos turi daug parduotuvių ir nenori versti klientų produktus grąžinti į tą pačią parduotuvę, kurioje jie buvo įsigyti.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="ae2d6-112">Todėl klientai produktus gali grąžinti į bet kurią parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="ae2d6-113">Tokios dažnos situacijos mažmenininkams pateikiamos sprendime „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="ae2d6-114">Naudodami „Commerce‟ galite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="ae2d6-115">Produktų ieškoti ar juos naršyti kitose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="ae2d6-116">Ieškoti visų patvirtintų produktų ar juos naršyti.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="ae2d6-117">Kurti atsiskaitymo grynaisiais pinigais operacijas ar klientų užsakymus.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="ae2d6-118">Pasirinkti klientų užsakymų pristatymo parinktis.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="ae2d6-119">Produktus paimti dabartinėje parduotuvėje arba kitoje parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="ae2d6-120">Užsakymą atšaukti dabartinėje parduotuvėje arba kitoje parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="ae2d6-121">Grąžinti užsakymą su kvitu ar be jo dabartinėje parduotuvėje arba kitoje parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="ae2d6-121">Return an order with or without the receipt at the current store or another store.</span></span>
