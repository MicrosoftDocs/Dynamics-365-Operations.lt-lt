---
title: "Konfigūracijos taisyklės"
description: "Šiame straipsnyje pateikiama bendra informacija apie konfigūravimo taisykles. Konfigūravimo taisyklėmis apibrėžiami ryšiai tarp komplektavimo specifikacijos (KS) produktų, kurie naudoja konfigūravimo pagal dimensijas technologiją."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 72395b5068f0893d79be6f8095dae988c224d0aa
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2017

---

# <a name="configuration-rules"></a><span data-ttu-id="d7e27-104">Konfigūracijos taisyklės</span><span class="sxs-lookup"><span data-stu-id="d7e27-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d7e27-105">Šiame straipsnyje pateikiama bendra informacija apie konfigūravimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="d7e27-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="d7e27-106">Konfigūravimo taisyklėmis apibrėžiami ryšiai tarp komplektavimo specifikacijos (KS) produktų, kurie naudoja konfigūravimo pagal dimensijas technologiją.</span><span class="sxs-lookup"><span data-stu-id="d7e27-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="d7e27-107">Konfigūracijos taisyklės galimos nurodžius konfigūravimą pagal dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d7e27-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="d7e27-108">Konfigūracijos taisyklės naudojamos komplektavimo specifikacijoje (KS) įgalinti arba uždrausti konkrečias prekių kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="d7e27-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="d7e27-109">Sukūrus KS ir atitinkamas prekes priskyrus jų atitinkamoms konfigūracijos grupėms, galima nustatyti vieną ar daugiau konfigūracijos taisyklių.</span><span class="sxs-lookup"><span data-stu-id="d7e27-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="d7e27-110">Jei dvi prekės susijusios viena su kita, siekiant užtikrinti įtraukimą naudojamas operatorius **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="d7e27-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="d7e27-111">Jei dvi prekės yra nesuderinamos, siekiant užtikrinti neįtraukimą naudojamas operatorius **Atsisakyti pasirinkimo**.</span><span class="sxs-lookup"><span data-stu-id="d7e27-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="d7e27-112">**Pastaba.** Ši informacija taikoma tik bendriesiems produktams, kuriuose naudojama konfigūravimo pagal dimensijas technologija.</span><span class="sxs-lookup"><span data-stu-id="d7e27-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="d7e27-113">Vėliau pakeistos konfigūracijos taisyklės neturi įtakos esamoms konfigūracijoms.</span><span class="sxs-lookup"><span data-stu-id="d7e27-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="d7e27-114">Kita vertus, svarbu, kad taisykles nustatytumėte prieš nustatydami konfigūraciją ir patikrintumėte taisykles, jei manote, kad jos galėjo būti pakeistos.</span><span class="sxs-lookup"><span data-stu-id="d7e27-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="d7e27-115">**Pastaba.** Taikant metodą **Pasirinkti** išvestinės konfigūracijos grupė, prekės numeris ir konfigūracija pasirenkami automatiškai.</span><span class="sxs-lookup"><span data-stu-id="d7e27-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="d7e27-116">Taikant metodą **Atsisakyti pasirinkimo** išvestinės konfigūracijos grupės, prekės numerio ir konfigūracijos pasirinkti negalima.</span><span class="sxs-lookup"><span data-stu-id="d7e27-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="d7e27-117">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="d7e27-117">See also</span></span>
--------

[<span data-ttu-id="d7e27-118">Produktų konfigūravimas pagal dimensijas</span><span class="sxs-lookup"><span data-stu-id="d7e27-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)



