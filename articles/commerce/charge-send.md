---
title: Perkelkite užsakymus iš kitos parduotuvės naudodami mokesčių siuntimo funkciją.
description: Šioje temoje aprašoma mokesčių siuntimo funkcija.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0bbebcc7b2ab89bf2f5db7294acfca1d8a5ad96e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023380"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="93775-103">Perkelkite užsakymus iš kitos parduotuvės naudodami mokesčių siuntimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="93775-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93775-104">Naudojant mokesčių siuntimo funkciją programoje „Commerce“ kliento užsakymus galima pateikti vienoje parduotuvėje, o išsiųsti iš kitos.</span><span class="sxs-lookup"><span data-stu-id="93775-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="93775-105">Elektroninio kasos aparato (EKA) kliente esantys kliento užsakymai palaiko keletą įvykdymo parinkčių.</span><span class="sxs-lookup"><span data-stu-id="93775-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="93775-106">Toliau nurodyta keletas įvykdymo parinkčių pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="93775-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="93775-107">Paėmimas iš tos pačios parduotuvės kitą dieną.</span><span class="sxs-lookup"><span data-stu-id="93775-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="93775-108">Paėmimas iš kitos parduotuvės tą pačią dieną.</span><span class="sxs-lookup"><span data-stu-id="93775-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="93775-109">Siuntimas iš numatytojo siuntimo sandėlio, priskirto parduotuvei, ir pristatymas nurodžius konkrečią datą.</span><span class="sxs-lookup"><span data-stu-id="93775-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="93775-110">Taikant mokesčio siuntimo funkciją naudojamos toliau nurodytos EKA operacijos: Siųsti visus produktus ir Siųsti pasirinktus produktus.</span><span class="sxs-lookup"><span data-stu-id="93775-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="93775-111">Tai parduotuvės klerkui leidžia pasirinkti vietą iš kurios siųsti ir kurioje užsakymas arba užsakymo eilutė gali būti įvykdyta.</span><span class="sxs-lookup"><span data-stu-id="93775-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="93775-112">Pagal numatytuosius nustatymus vieta iš kurios siunčiama yra su parduotuve susietas siuntimo sandėlis.</span><span class="sxs-lookup"><span data-stu-id="93775-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="93775-113">Tačiau parduotuvės klerkas gali pakeisti šią vietą ir pasirinkti bet kurią parduotuvei priskirtoje lokatorių grupėje apibrėžtą parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="93775-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="93775-114">Tokia pati galimybė suteikiama pasirenkant ir gavėjo adresus.</span><span class="sxs-lookup"><span data-stu-id="93775-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="93775-115">Siuntimo metodai, kurios galima naudoti norint įvykdyti užsakymo eilutę, yra pagrįsti produktų pristatymo ir adresų leistinų režimų konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="93775-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="93775-116">Kadangi tinkamų pristatymo režimų taisyklės tvarkomos tik „Headquarters“ (HQ), EKA klientas kreipiasi realiuoju laiku ir randa tinkamus siuntimo eilutės pristatymo režimus.</span><span class="sxs-lookup"><span data-stu-id="93775-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>