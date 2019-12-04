---
title: Konfigūracijos taisyklės
description: Šiame straipsnyje pateikiama bendra informacija apie konfigūravimo taisykles. Konfigūravimo taisyklėmis apibrėžiami ryšiai tarp komplektavimo specifikacijos (KS) produktų, kurie naudoja konfigūravimo pagal dimensijas technologiją.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d81bb8e570b61d214ab3f6b7c40c1135977f9ee
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813643"
---
# <a name="configuration-rules"></a><span data-ttu-id="3e052-104">Konfigūracijos taisyklės</span><span class="sxs-lookup"><span data-stu-id="3e052-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e052-105">Šiame straipsnyje pateikiama bendra informacija apie konfigūravimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="3e052-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="3e052-106">Konfigūravimo taisyklėmis apibrėžiami ryšiai tarp komplektavimo specifikacijos (KS) produktų, kurie naudoja konfigūravimo pagal dimensijas technologiją.</span><span class="sxs-lookup"><span data-stu-id="3e052-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="3e052-107">Konfigūracijos taisyklės galimos nurodžius konfigūravimą pagal dimensijas.</span><span class="sxs-lookup"><span data-stu-id="3e052-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="3e052-108">Konfigūracijos taisyklės naudojamos komplektavimo specifikacijoje (KS) įgalinti arba uždrausti konkrečias prekių kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="3e052-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="3e052-109">Sukūrus KS ir atitinkamas prekes priskyrus jų atitinkamoms konfigūracijos grupėms, galima nustatyti vieną ar daugiau konfigūracijos taisyklių.</span><span class="sxs-lookup"><span data-stu-id="3e052-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="3e052-110">Jei dvi prekės susijusios viena su kita, siekiant užtikrinti įtraukimą naudojamas operatorius **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="3e052-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="3e052-111">Jei dvi prekės yra nesuderinamos, siekiant užtikrinti neįtraukimą naudojamas operatorius **Atsisakyti pasirinkimo**.</span><span class="sxs-lookup"><span data-stu-id="3e052-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="3e052-112">**Pastaba.** Ši informacija taikoma tik bendriesiems produktams, kuriuose naudojama konfigūravimo pagal dimensijas technologija.</span><span class="sxs-lookup"><span data-stu-id="3e052-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="3e052-113">Vėliau pakeistos konfigūracijos taisyklės neturi įtakos esamoms konfigūracijoms.</span><span class="sxs-lookup"><span data-stu-id="3e052-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="3e052-114">Kita vertus, svarbu, kad taisykles nustatytumėte prieš nustatydami konfigūraciją ir patikrintumėte taisykles, jei manote, kad jos galėjo būti pakeistos.</span><span class="sxs-lookup"><span data-stu-id="3e052-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="3e052-115">**Pastaba.** Taikant metodą **Pasirinkti** išvestinės konfigūracijos grupė, prekės numeris ir konfigūracija pasirenkami automatiškai.</span><span class="sxs-lookup"><span data-stu-id="3e052-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="3e052-116">Taikant metodą **Atsisakyti pasirinkimo** išvestinės konfigūracijos grupės, prekės numerio ir konfigūracijos pasirinkti negalima.</span><span class="sxs-lookup"><span data-stu-id="3e052-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="3e052-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3e052-117">Additional resources</span></span>
--------

[<span data-ttu-id="3e052-118">Dimensijomis pagrįstos produktų konfigūracijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="3e052-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)



