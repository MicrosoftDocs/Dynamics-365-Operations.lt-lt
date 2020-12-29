---
title: Parduotuvės efektyvumo analizė
description: Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti parduotuvių našumą pagal savo „Dynamics 365 Commerce“ duomenis.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8d95bb0927de5a1906efe180cb9e725c380a724f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414417"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="d6d68-103">Parduotuvės našumo analizavimas</span><span class="sxs-lookup"><span data-stu-id="d6d68-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6d68-104">Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti parduotuvių našumą pagal savo „Dynamics 365 Commerce“ duomenis.</span><span class="sxs-lookup"><span data-stu-id="d6d68-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="d6d68-105">Naudodami „Retail“ vartotojai gali tirti parduotuvės našumą realiuoju laiku skirtinguose organizacijos hierarchijos lygiuose per pasirinktą laikotarpį, atidarydami parengtą naudoti ataskaitą **Kanalo suvestinė** bet kurioje iš toliau nurodytų vietų.</span><span class="sxs-lookup"><span data-stu-id="d6d68-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="d6d68-106">Darbo sritis **Mažmeninės prekybos parduotuvės valdymas** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo suvestinė**</span><span class="sxs-lookup"><span data-stu-id="d6d68-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="d6d68-107">Darbo sritis **Mažmeninės prekybos parduotuvės finansai** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės finansai** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo suvestinė**</span><span class="sxs-lookup"><span data-stu-id="d6d68-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="d6d68-108">Dalis **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Ataskaita Kanalo suvestinė**</span><span class="sxs-lookup"><span data-stu-id="d6d68-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="d6d68-109">Šioje ataskaitoje toliau nurodytų suvestinių momentinė kopija pateikiama kaip parduotuvės efektyvumo tikrinimo dalis.</span><span class="sxs-lookup"><span data-stu-id="d6d68-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="d6d68-110">Bruto pardavimo suvestinė</span><span class="sxs-lookup"><span data-stu-id="d6d68-110">Gross sales summary</span></span>
- <span data-ttu-id="d6d68-111">Mokėjimo priemonės tipo suvestinė</span><span class="sxs-lookup"><span data-stu-id="d6d68-111">Tender type summary</span></span>
- <span data-ttu-id="d6d68-112">Mokesčių suvestinė</span><span class="sxs-lookup"><span data-stu-id="d6d68-112">Tax summary</span></span>
- <span data-ttu-id="d6d68-113">Kainų nepaisymo suvestinė</span><span class="sxs-lookup"><span data-stu-id="d6d68-113">Price overrides summary</span></span>
- <span data-ttu-id="d6d68-114">Nuolaidų suvestinė</span><span class="sxs-lookup"><span data-stu-id="d6d68-114">Discounts summary</span></span>
