---
title: "Aptarnavimo objektų grupės"
description: "Objektų grupės yra naudingos rūšiuojant ir filtruojant ataskaitų ir statistikos objektų duomenis."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: lt-lt
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="e0148-103">Aptarnavimo objektų grupės</span><span class="sxs-lookup"><span data-stu-id="e0148-103">Service object groups</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e0148-104">Objektų grupės yra naudingos rūšiuojant ir filtruojant ataskaitų ir statistikos objektų duomenis.</span><span class="sxs-lookup"><span data-stu-id="e0148-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="e0148-105">Pavyzdžiui, objektus galite grupuoti pagal geografinę vietovę arba pagal tipą.</span><span class="sxs-lookup"><span data-stu-id="e0148-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="e0148-106">Grupavimas pagal geografinę vietovę</span><span class="sxs-lookup"><span data-stu-id="e0148-106">Group by geographical location</span></span>

<span data-ttu-id="e0148-107">Šiuo grupavimo metodu galite parodyti, kur yra įvairūs jūsų įmonės aptarnaujami objektai.</span><span class="sxs-lookup"><span data-stu-id="e0148-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="e0148-108">Grupavimas pagal geografinę vietovę taip pat gali būti naudingas jei, pavyzdžiui, jums būtina identifikuoti objektus tam tikroje šalyje / regione, kuriems jūsų įmonė jau teikia aptarnavimo paslaugas.</span><span class="sxs-lookup"><span data-stu-id="e0148-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="e0148-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e0148-109">Example</span></span>

<span data-ttu-id="e0148-110">Klientas iš Belgijos paskambina į jūsų aptarnavimo centrą, norėdamas sukurti objekto „ABC“ aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="e0148-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="e0148-111">Pridėjote objektų grupę geografinei vietovei „Belgija“ prie visų Belgijoje aptarnaujamų objektų.</span><span class="sxs-lookup"><span data-stu-id="e0148-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="e0148-112">Naudodami šią grupę kaip filtrą, galite atlikti greitą paiešką ir nustatyti, ar programoje jau turite ABC įrašą, ar vis tik jums reikės nustatyti naują objektą.</span><span class="sxs-lookup"><span data-stu-id="e0148-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="e0148-113">Grupavimas pagal tipą</span><span class="sxs-lookup"><span data-stu-id="e0148-113">Group by type</span></span>

<span data-ttu-id="e0148-114">Šiuo grupavimo metodu galite parodyti jūsų įmonės aptarnaujamų objektų tipus.</span><span class="sxs-lookup"><span data-stu-id="e0148-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="e0148-115">Objektų grupavimas pagal tipą taip pat gali būti naudingas, jei, pavyzdžiui, norite sukurti naują objektą pagal panašius objektus, kurie jau egzistuoja programoje.</span><span class="sxs-lookup"><span data-stu-id="e0148-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="e0148-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e0148-116">Example</span></span>

<span data-ttu-id="e0148-117">Klientas paskambina norėdamas nustatyti oro kondicionavimo įrenginio „HIJ“ aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="e0148-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="e0148-118">Dar neturite šio įrenginio įrašo.</span><span class="sxs-lookup"><span data-stu-id="e0148-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="e0148-119">Tačiau nustatėte objektų grupę, pavadinimu Oro kondicionieriai, ir šią grupę pridėjote prie visų oro kondicionierių objektų.</span><span class="sxs-lookup"><span data-stu-id="e0148-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="e0148-120">Todėl galite greitai ieškoti ir identifikuoti visus kitus oro kondicionierių įrenginius, bei naudoti šių objektų šablonų informaciją, kad sukurtumėte HIJ aptarnavimo sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="e0148-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="e0148-121">Tokiu būdu naudodami objektų grupes galite greitai nustatyti naujus objektus ir apibrėžti, kokias aptarnavimo užduotis reikia atlikti šiuose objektuose.</span><span class="sxs-lookup"><span data-stu-id="e0148-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




