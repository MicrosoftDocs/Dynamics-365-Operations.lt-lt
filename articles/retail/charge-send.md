---
title: "Užsakymo siuntimas iš kitos parduotuvės"
description: "Šioje temoje aprašoma mokesčių siuntimo funkcija."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: 41434614b01f9a00f2b8a56765ecb90ee07e3d90
ms.contentlocale: lt-lt
ms.lasthandoff: 03/06/2018

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="cb2a1-103">Užsakymo siuntimas iš kitos parduotuvės</span><span class="sxs-lookup"><span data-stu-id="cb2a1-103">Ship an order from a different store</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="cb2a1-104">Naudojant mokesčių siuntimo funkciją programoje „Dynamics 365 for Retail“ kliento užsakymus galima pateikti vienoje parduotuvėje, o išsiųsti iš kitos.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="cb2a1-105">Elektroninio kasos aparato (EKA) kliente esantys kliento užsakymai palaiko keletą įvykdymo parinkčių.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="cb2a1-106">Toliau nurodyta keletas įvykdymo parinkčių pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="cb2a1-107">Paėmimas iš tos pačios parduotuvės kitą dieną.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="cb2a1-108">Paėmimas iš kitos parduotuvės tą pačią dieną.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="cb2a1-109">Siuntimas iš numatytojo siuntimo sandėlio, priskirto parduotuvei, ir pristatymas nurodžius konkrečią datą.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="cb2a1-110">Taikant mokesčio siuntimo funkciją naudojamos toliau nurodytos EKA operacijos: Siųsti visus produktus ir Siųsti pasirinktus produktus.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="cb2a1-111">Tai parduotuvės klerkui leidžia pasirinkti vietą iš kurios siųsti ir kurioje užsakymas arba užsakymo eilutė gali būti įvykdyta.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="cb2a1-112">Pagal numatytuosius nustatymus vieta iš kurios siunčiama yra su parduotuve susietas siuntimo sandėlis.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="cb2a1-113">Tačiau parduotuvės klerkas gali pakeisti šią vietą ir pasirinkti bet kurią parduotuvei priskirtoje lokatorių grupėje apibrėžtą parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="cb2a1-114">Tokia pati galimybė suteikiama pasirenkant ir gavėjo adresus.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="cb2a1-115">Siuntimo metodai, kurios galima naudoti norint įvykdyti užsakymo eilutę, yra pagrįsti produktų pristatymo ir adresų leistinų režimų konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="cb2a1-116">Kadangi tinkamų pristatymo režimų taisyklės tvarkomos tik mažmeninių pardavimų valdyme (HQ), EKA klientas kreipiasi realiuoju laiku ir randa tinkamus siuntimo eilutės pristatymo režimus.</span><span class="sxs-lookup"><span data-stu-id="cb2a1-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


