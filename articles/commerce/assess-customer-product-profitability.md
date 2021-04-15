---
title: Įvertinti klientų ir produktų pelningumą
description: Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti klientus ir produktų pelningumą pagal savo „Dynamics 365 Commerce“ duomenis.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 80a2f38f2b3f039b17556116d6aea738faa1db50
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797334"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="63e25-103">Klientų ir produktų pelningumo vertinimas</span><span class="sxs-lookup"><span data-stu-id="63e25-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="63e25-104">Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti klientus ir produktų pelningumą pagal savo „Dynamics 365 Commerce“ duomenis.</span><span class="sxs-lookup"><span data-stu-id="63e25-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="63e25-105">„Commerce“ vartotojai gali tirti svarbiausių klientų (10–100) pelningumą skirtinguose organizacijos hierarchijos lygiuose pagal vieną iš toliau pateiktų kriterijų.</span><span class="sxs-lookup"><span data-stu-id="63e25-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="63e25-106">Pardavimo suma</span><span class="sxs-lookup"><span data-stu-id="63e25-106">Sales amount</span></span>
- <span data-ttu-id="63e25-107">Kiekis</span><span class="sxs-lookup"><span data-stu-id="63e25-107">Quantity</span></span>
- <span data-ttu-id="63e25-108">Bruto pelno marža</span><span class="sxs-lookup"><span data-stu-id="63e25-108">Gross profit margin</span></span>
- <span data-ttu-id="63e25-109">Maržos procentas</span><span class="sxs-lookup"><span data-stu-id="63e25-109">Margin percentage</span></span>

<span data-ttu-id="63e25-110">Šiam vertinimui atlikti galite naudoti parengtą naudoti ataskaitą **Svarbiausi klientai**, kurią galite atidaryti bet kurioje iš toliau pateiktų vietų.</span><span class="sxs-lookup"><span data-stu-id="63e25-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="63e25-111">Darbo sritis **Parduotuvės valdymas** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Kanalai** &gt; **Parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių klientų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="63e25-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="63e25-112">Skyrius **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Svarbiausių klientų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="63e25-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="63e25-113">Taip pat vartotojai gali tirti svarbiausių produktų (10–100) pelningumą skirtinguose organizacijos hierarchijos lygiuose pagal vieną iš toliau pateiktų kriterijų.</span><span class="sxs-lookup"><span data-stu-id="63e25-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="63e25-114">Pardavimo suma</span><span class="sxs-lookup"><span data-stu-id="63e25-114">Sales amount</span></span>
- <span data-ttu-id="63e25-115">Kiekis</span><span class="sxs-lookup"><span data-stu-id="63e25-115">Quantity</span></span>
- <span data-ttu-id="63e25-116">Bruto pelno marža</span><span class="sxs-lookup"><span data-stu-id="63e25-116">Gross profit margin</span></span>
- <span data-ttu-id="63e25-117">Maržos procentas</span><span class="sxs-lookup"><span data-stu-id="63e25-117">Margin percentage</span></span>

<span data-ttu-id="63e25-118">Šiam vertinimui atlikti galite naudoti parengtą naudoti ataskaitą **Svarbiausi produktai**, kurią galite atidaryti bet kurioje iš toliau pateiktų vietų.</span><span class="sxs-lookup"><span data-stu-id="63e25-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="63e25-119">Darbo sritis **Parduotuvės valdymas** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Kanalai** &gt; **Parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių produktų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="63e25-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="63e25-120">Darbo sritis **Kategorijų ir produktų valdymas** &gt; **Mažmeninė prekyba ir prekyba** &gt; **Produktai ir kategorijos** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos** &gt; **Svarbiausių produktų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="63e25-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="63e25-121">Skyrius **Užklausos ir ataskaitos**&gt; **Mažmeninė prekyba ir prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Svarbiausių produktų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="63e25-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]