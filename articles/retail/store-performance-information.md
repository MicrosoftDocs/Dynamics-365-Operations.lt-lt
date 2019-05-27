---
title: Parduotuvės efektyvumo analizė
description: Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti parduotuvių našumą pagal savo „Microsoft Dynamics 365 for Retail“ duomenis.
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
ms.openlocfilehash: c975c021b6db49d1e25fd036f4955c7223e438ea
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569268"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="5c741-103">Parduotuvės našumo analizavimas</span><span class="sxs-lookup"><span data-stu-id="5c741-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c741-104">Šiame straipsnyje paaiškinama, kaip, naudodami atminties ir realaus laiko analitiką, galite pasiekti, ištirti ir suprasti parduotuvių našumą pagal savo „Microsoft Dynamics 365 for Retail“ duomenis.</span><span class="sxs-lookup"><span data-stu-id="5c741-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="5c741-105">Naudodami „Dynamics 365 for Retail“ vartotojai gali tirti parduotuvės efektyvumą realiuoju laiku skirtinguose organizacijos hierarchijos lygiuose per pasirinktą laikotarpį, atidarydami parengtą naudoti ataskaitą **Kanalo suvestinė** bet kurioje iš toliau nurodytų vietų.</span><span class="sxs-lookup"><span data-stu-id="5c741-105">As part of Dynamics 365 for Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="5c741-106">Darbo sritis **Mažmeninės prekybos parduotuvės valdymas** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės valdymas** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo suvestinė**</span><span class="sxs-lookup"><span data-stu-id="5c741-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="5c741-107">Darbo sritis **Mažmeninės prekybos parduotuvės finansai** &gt; **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės finansai** &gt; **Ataskaitos** &gt; **Ataskaita Kanalo suvestinė**</span><span class="sxs-lookup"><span data-stu-id="5c741-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="5c741-108">Dalis **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimo ataskaitos** &gt; **Ataskaita Kanalo suvestinė**</span><span class="sxs-lookup"><span data-stu-id="5c741-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="5c741-109">Šioje ataskaitoje toliau nurodytų suvestinių momentinė kopija pateikiama kaip parduotuvės efektyvumo tikrinimo dalis.</span><span class="sxs-lookup"><span data-stu-id="5c741-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="5c741-110">Bruto pardavimo suvestinė</span><span class="sxs-lookup"><span data-stu-id="5c741-110">Gross sales summary</span></span>
- <span data-ttu-id="5c741-111">Mokėjimo priemonės tipo suvestinė</span><span class="sxs-lookup"><span data-stu-id="5c741-111">Tender type summary</span></span>
- <span data-ttu-id="5c741-112">Mokesčių suvestinė</span><span class="sxs-lookup"><span data-stu-id="5c741-112">Tax summary</span></span>
- <span data-ttu-id="5c741-113">Kainų nepaisymo suvestinė</span><span class="sxs-lookup"><span data-stu-id="5c741-113">Price overrides summary</span></span>
- <span data-ttu-id="5c741-114">Nuolaidų suvestinė</span><span class="sxs-lookup"><span data-stu-id="5c741-114">Discounts summary</span></span>
