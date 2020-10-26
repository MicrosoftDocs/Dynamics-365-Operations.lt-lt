---
title: Aptarnavimo objektų grupės
description: Objektų grupės yra naudingos rūšiuojant ir filtruojant ataskaitų ir statistikos objektų duomenis.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4438487fa234cf093b557bca9455717b2cd3ca0b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979237"
---
# <a name="service-object-groups"></a><span data-ttu-id="fc8d1-103">Aptarnavimo objektų grupės</span><span class="sxs-lookup"><span data-stu-id="fc8d1-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc8d1-104">Objektų grupės yra naudingos rūšiuojant ir filtruojant ataskaitų ir statistikos objektų duomenis.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="fc8d1-105">Pavyzdžiui, objektus galite grupuoti pagal geografinę vietovę arba pagal tipą.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="fc8d1-106">Grupavimas pagal geografinę vietovę</span><span class="sxs-lookup"><span data-stu-id="fc8d1-106">Group by geographical location</span></span>

<span data-ttu-id="fc8d1-107">Šiuo grupavimo metodu galite parodyti, kur yra įvairūs jūsų įmonės aptarnaujami objektai.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="fc8d1-108">Grupavimas pagal geografinę vietovę taip pat gali būti naudingas jei, pavyzdžiui, jums būtina identifikuoti objektus tam tikroje šalyje / regione, kuriems jūsų įmonė jau teikia aptarnavimo paslaugas.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="fc8d1-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="fc8d1-109">Example</span></span>

<span data-ttu-id="fc8d1-110">Klientas iš Belgijos paskambina į jūsų aptarnavimo centrą, norėdamas sukurti objekto „ABC“ aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="fc8d1-111">Pridėjote objektų grupę geografinei vietovei „Belgija“ prie visų Belgijoje aptarnaujamų objektų.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="fc8d1-112">Naudodami šią grupę kaip filtrą, galite atlikti greitą paiešką ir nustatyti, ar programoje jau turite ABC įrašą, ar vis tik jums reikės nustatyti naują objektą.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="fc8d1-113">Grupavimas pagal tipą</span><span class="sxs-lookup"><span data-stu-id="fc8d1-113">Group by type</span></span>

<span data-ttu-id="fc8d1-114">Šiuo grupavimo metodu galite parodyti jūsų įmonės aptarnaujamų objektų tipus.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="fc8d1-115">Objektų grupavimas pagal tipą taip pat gali būti naudingas, jei, pavyzdžiui, norite sukurti naują objektą pagal panašius objektus, kurie jau egzistuoja programoje.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="fc8d1-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="fc8d1-116">Example</span></span>

<span data-ttu-id="fc8d1-117">Klientas paskambina norėdamas nustatyti oro kondicionavimo įrenginio „HIJ“ aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="fc8d1-118">Dar neturite šio įrenginio įrašo.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="fc8d1-119">Tačiau nustatėte objektų grupę, pavadinimu Oro kondicionieriai, ir šią grupę pridėjote prie visų oro kondicionierių objektų.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="fc8d1-120">Todėl galite greitai ieškoti ir identifikuoti visus kitus oro kondicionierių įrenginius, bei naudoti šių objektų šablonų informaciją, kad sukurtumėte HIJ aptarnavimo sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="fc8d1-121">Tokiu būdu naudodami objektų grupes galite greitai nustatyti naujus objektus ir apibrėžti, kokias aptarnavimo užduotis reikia atlikti šiuose objektuose.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="fc8d1-122">Aptarnavimo objektų grupių kūrimas</span><span class="sxs-lookup"><span data-stu-id="fc8d1-122">Create service object groups</span></span>

<span data-ttu-id="fc8d1-123">Sukurkite grupes, kurioms galite priskirti aptarnavimo objektus.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="fc8d1-124">Aptarnavimo objektai – tai atsargų prekės ir kiti produktai, kuriems teikiamos aptarnavimo paslaugos.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="fc8d1-125">Grupuodami aptarnavimo objektus galite kurti panašių ir susijusių aptarnavimo objektų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="fc8d1-126">Pavyzdžiui, aptarnavimo objektų grupę gali sudaryti du aptarnavimo objektai: vienas aptarnavimo objektas yra rinkinys, o kitas – rinkinio diegimo paslauga.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="fc8d1-127">Norėdami kurti aptarnavimo objektų grupes, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="fc8d1-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="fc8d1-128">Spustelėkite **Aptarnavimo valdymas > Sąranka > Aptarnavimo objektai > Aptarnavimo objektų grupės**.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="fc8d1-129">Spustelėję **Nauja** sukurkite naują aptarnavimo objektų grupę.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="fc8d1-130">Įveskite unikalų aptarnavimo objektų grupės pavadinimą ir, pasirinktinai, aprašą.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="fc8d1-131">Naudodamiesi forma **Aptarnavimo objektai** galite priskirti aptarnavimo objektus grupei.</span><span class="sxs-lookup"><span data-stu-id="fc8d1-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="fc8d1-132">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="fc8d1-132">See also</span></span>

[<span data-ttu-id="fc8d1-133">Aptarnavimo objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="fc8d1-133">Create service objects</span></span>](create-service-objects.md)


