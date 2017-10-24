---
title: "Įvertinti klientų ir produktų pelningumą"
description: "Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti klientus ir produktų pelningumą pagal savo „Microsoft Dynamics 365 for Retail‟ duomenis."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 84a9e0b3936adcf2ed99fddca77dd57dfedeb050
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="b6e50-103">Klientų ir produktų pelningumo vertinimas</span><span class="sxs-lookup"><span data-stu-id="b6e50-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b6e50-104">Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti klientus ir produktų pelningumą pagal savo „Microsoft Dynamics 365 for Retail‟ duomenis.</span><span class="sxs-lookup"><span data-stu-id="b6e50-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="b6e50-105">„Dynamics 365 for Retail“ vartotojai gali tirti svarbiausių klientų (10–100) pelningumą skirtinguose organizacijos hierarchijos lygiuose pagal vieną iš toliau pateiktų kriterijų.</span><span class="sxs-lookup"><span data-stu-id="b6e50-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="b6e50-106">Pardavimo suma</span><span class="sxs-lookup"><span data-stu-id="b6e50-106">Sales amount</span></span>
-   <span data-ttu-id="b6e50-107">Kiekis</span><span class="sxs-lookup"><span data-stu-id="b6e50-107">Quantity</span></span>
-   <span data-ttu-id="b6e50-108">Bruto pelno marža</span><span class="sxs-lookup"><span data-stu-id="b6e50-108">Gross profit margin</span></span>
-   <span data-ttu-id="b6e50-109">Maržos procentas</span><span class="sxs-lookup"><span data-stu-id="b6e50-109">Margin percentage</span></span>

<span data-ttu-id="b6e50-110">Šiam vertinimui atlikti galite naudoti parengtą naudoti ataskaitą **Svarbiausi klientai**, kurią galite atidaryti bet kurioje iš toliau pateiktų vietų.</span><span class="sxs-lookup"><span data-stu-id="b6e50-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="b6e50-111">Darbo sritis **Mažmeninės prekybos parduotuvės valdymas** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių klientų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="b6e50-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="b6e50-112">Dalis **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Svarbiausių klientų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="b6e50-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="b6e50-113">Taip pat vartotojai gali tirti svarbiausių produktų (10–100) pelningumą skirtinguose organizacijos hierarchijos lygiuose pagal vieną iš toliau pateiktų kriterijų.</span><span class="sxs-lookup"><span data-stu-id="b6e50-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="b6e50-114">Pardavimo suma</span><span class="sxs-lookup"><span data-stu-id="b6e50-114">Sales amount</span></span>
-   <span data-ttu-id="b6e50-115">Kiekis</span><span class="sxs-lookup"><span data-stu-id="b6e50-115">Quantity</span></span>
-   <span data-ttu-id="b6e50-116">Bruto pelno marža</span><span class="sxs-lookup"><span data-stu-id="b6e50-116">Gross profit margin</span></span>
-   <span data-ttu-id="b6e50-117">Maržos procentas</span><span class="sxs-lookup"><span data-stu-id="b6e50-117">Margin percentage</span></span>

<span data-ttu-id="b6e50-118">Šiam vertinimui atlikti galite naudoti parengtą naudoti ataskaitą **Svarbiausi produktai**, kurią galite atidaryti bet kurioje iš toliau pateiktų vietų.</span><span class="sxs-lookup"><span data-stu-id="b6e50-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="b6e50-119">Darbo sritis **Mažmeninės prekybos parduotuvės valdymas** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių produktų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="b6e50-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="b6e50-120">Darbo sritis **Kategorijų ir produktų valdymas** &gt; **Mažmeninė prekyba** &gt; **Produktai ir kategorijos** &gt; **Mažmeninės prekybos parduotuvių valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių produktų ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="b6e50-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="b6e50-121">Dalis **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Svarbiausių produktų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="b6e50-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




