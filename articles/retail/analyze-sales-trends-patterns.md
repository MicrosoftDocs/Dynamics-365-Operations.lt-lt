---
title: Pardavimo tendencijų ir modelių analizavimas
description: Programoje „Dynamics 365 Retail“ galite realiu laiku tirti pardavimo tendencijas ir modelius.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, SysReportViewerForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c54e707d312d7ac3bbcad71a914e528859038a13
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025822"
---
# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="4721c-103">Pardavimo tendencijų ir modelių analizavimas</span><span class="sxs-lookup"><span data-stu-id="4721c-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4721c-104">Programoje „Dynamics 365 Retail“ galite realiu laiku tirti pardavimo tendencijas ir modelius.</span><span class="sxs-lookup"><span data-stu-id="4721c-104">You can study sales trends and patterns in real time in Dynamics 365 Retail.</span></span>

<span data-ttu-id="4721c-105">Naudodami „Retail“ vartotojai gali tirti pardavimo tendencijas ir modelius realiuoju laiku skirtinguose organizacijos hierarchijos lygiuose pasirinktu metų laikotarpiu, naudodami parengtą naudoti ataskaitą **Kanalo pardavimai pagal metus**.</span><span class="sxs-lookup"><span data-stu-id="4721c-105">As part of Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="4721c-106">Šią ataskaitą atidaryti galite iš bet kurios iš tolesnių vietų.</span><span class="sxs-lookup"><span data-stu-id="4721c-106">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="4721c-107">Darbo sritis **Mažmeninės prekybos parduotuvės valdymas** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo pardavimai pagal metus**</span><span class="sxs-lookup"><span data-stu-id="4721c-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="4721c-108">Darbo sritis **Mažmeninės prekybos parduotuvės finansai** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės finansai** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo pardavimai pagal metus**</span><span class="sxs-lookup"><span data-stu-id="4721c-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="4721c-109">Dalis **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Ataskaita Kanalo pardavimai pagal metus**</span><span class="sxs-lookup"><span data-stu-id="4721c-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="4721c-110">Vartotojai tirti pardavimo tendencijas ir modelius taip pat gali pagal valandą skirtinguose organizacijos hierarchijos lygiuose pasirinktu laikotarpiu, naudodami parengtą naudoti ataskaitą **Kanalo pardavimai pagal valandą**.</span><span class="sxs-lookup"><span data-stu-id="4721c-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="4721c-111">Šią ataskaitą atidaryti galite iš bet kurios iš tolesnių vietų.</span><span class="sxs-lookup"><span data-stu-id="4721c-111">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="4721c-112">Darbo sritis **Mažmeninės prekybos parduotuvės valdymas** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo pardavimai pagal valandas**</span><span class="sxs-lookup"><span data-stu-id="4721c-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="4721c-113">Darbo sritis **Mažmeninės prekybos parduotuvės finansai** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės finansai** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo pardavimai pagal valandas**</span><span class="sxs-lookup"><span data-stu-id="4721c-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="4721c-114">Dalis **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Ataskaita Kanalo pardavimai pagal valandas**</span><span class="sxs-lookup"><span data-stu-id="4721c-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>
