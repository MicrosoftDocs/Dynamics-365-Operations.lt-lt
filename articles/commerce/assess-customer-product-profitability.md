---
title: Įvertinti klientų ir produktų pelningumą
description: Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti klientus ir produktų pelningumą pagal savo „Dynamics 365 Commerce“ duomenis.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3770832cb8eee96931d8f8e68c726d5e09d3fceb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980059"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="4f50b-103">Klientų ir produktų pelningumo vertinimas</span><span class="sxs-lookup"><span data-stu-id="4f50b-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f50b-104">Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti klientus ir produktų pelningumą pagal savo „Dynamics 365 Commerce“ duomenis.</span><span class="sxs-lookup"><span data-stu-id="4f50b-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="4f50b-105">„Commerce“ vartotojai gali tirti svarbiausių klientų (10–100) pelningumą skirtinguose organizacijos hierarchijos lygiuose pagal vieną iš toliau pateiktų kriterijų.</span><span class="sxs-lookup"><span data-stu-id="4f50b-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="4f50b-106">Pardavimo suma</span><span class="sxs-lookup"><span data-stu-id="4f50b-106">Sales amount</span></span>
- <span data-ttu-id="4f50b-107">Kiekis</span><span class="sxs-lookup"><span data-stu-id="4f50b-107">Quantity</span></span>
- <span data-ttu-id="4f50b-108">Bruto pelno marža</span><span class="sxs-lookup"><span data-stu-id="4f50b-108">Gross profit margin</span></span>
- <span data-ttu-id="4f50b-109">Maržos procentas</span><span class="sxs-lookup"><span data-stu-id="4f50b-109">Margin percentage</span></span>

<span data-ttu-id="4f50b-110">Šiam vertinimui atlikti galite naudoti parengtą naudoti ataskaitą **Svarbiausi klientai**, kurią galite atidaryti bet kurioje iš toliau pateiktų vietų.</span><span class="sxs-lookup"><span data-stu-id="4f50b-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="4f50b-111">Darbo sritis **Parduotuvės valdymas** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Kanalai** &gt; **Parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių klientų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="4f50b-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="4f50b-112">Skyrius **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Svarbiausių klientų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="4f50b-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="4f50b-113">Taip pat vartotojai gali tirti svarbiausių produktų (10–100) pelningumą skirtinguose organizacijos hierarchijos lygiuose pagal vieną iš toliau pateiktų kriterijų.</span><span class="sxs-lookup"><span data-stu-id="4f50b-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="4f50b-114">Pardavimo suma</span><span class="sxs-lookup"><span data-stu-id="4f50b-114">Sales amount</span></span>
- <span data-ttu-id="4f50b-115">Kiekis</span><span class="sxs-lookup"><span data-stu-id="4f50b-115">Quantity</span></span>
- <span data-ttu-id="4f50b-116">Bruto pelno marža</span><span class="sxs-lookup"><span data-stu-id="4f50b-116">Gross profit margin</span></span>
- <span data-ttu-id="4f50b-117">Maržos procentas</span><span class="sxs-lookup"><span data-stu-id="4f50b-117">Margin percentage</span></span>

<span data-ttu-id="4f50b-118">Šiam vertinimui atlikti galite naudoti parengtą naudoti ataskaitą **Svarbiausi produktai**, kurią galite atidaryti bet kurioje iš toliau pateiktų vietų.</span><span class="sxs-lookup"><span data-stu-id="4f50b-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="4f50b-119">Darbo sritis **Parduotuvės valdymas** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Kanalai** &gt; **Parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių produktų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="4f50b-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="4f50b-120">Darbo sritis **Kategorijų ir produktų valdymas** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Produktai ir kategorijos** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių produktų ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="4f50b-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="4f50b-121">Skyrius **Užklausos ir ataskaitos**&gt; **Mažmeninė prekyba ir prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Svarbiausių produktų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="4f50b-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
