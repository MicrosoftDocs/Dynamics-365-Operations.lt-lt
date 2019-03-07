---
title: Ataskaitų parinktys sprendime „Talent“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai klientas nori tinkinti „Microsoft Dynamics 365 for Talent“ ataskaitas arba sukurti naujų ataskaitų.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "305530"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="f25b5-103">Ataskaitų parinktys sprendime „Talent“</span><span class="sxs-lookup"><span data-stu-id="f25b5-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f25b5-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="f25b5-104">**Environment details**</span></span>

<span data-ttu-id="f25b5-105">Ši problema taikoma visoms aplinkoms.</span><span class="sxs-lookup"><span data-stu-id="f25b5-105">This issue applies to all environments.</span></span>

<span data-ttu-id="f25b5-106">**Požymis**</span><span class="sxs-lookup"><span data-stu-id="f25b5-106">**Symptom**</span></span>

<span data-ttu-id="f25b5-107">Klientas nori tinkinti „Microsoft Dynamics 365 for Talent“ ataskaitas arba sukurti naujų ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="f25b5-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="f25b5-108">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="f25b5-108">**Issue**</span></span>

<span data-ttu-id="f25b5-109">Vartotojui nepavyksta tinkinti įdėtųjų „Microsoft Power BI“ ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="f25b5-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="f25b5-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="f25b5-110">**Solution**</span></span>

- <span data-ttu-id="f25b5-111">„Core HR“ duomenis, kurių srautai juda į „Common Data Service for Apps“, skirtą programoms, galima paskelbti naudojantis „PowerApps“ CDS jungtimi su „Power BI Desktop“.</span><span class="sxs-lookup"><span data-stu-id="f25b5-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="f25b5-112">Atminkite, kad „Common Data Service“, skirtoje programoms, pateikiamas „Core HR“ duomenų subrinkinys.</span><span class="sxs-lookup"><span data-stu-id="f25b5-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="f25b5-113">Daugiau informacijos apie „Power BI“ ir ataskaitų sritis ieškokite temoje [„Power BI“ ataskaitų ir ataskaitų sričių, naudojant „PowerApps Common Data Service“, kūrimas](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="f25b5-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="f25b5-114">Elektronines ataskaitas (ER) galima naudoti kai kurioms „Talent“ ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="f25b5-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="f25b5-115">Kliento kuriamus tinkinimus galima atlikti per ER konfigūravimo pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="f25b5-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="f25b5-116">Duomenis į „Microsoft Excel“ arba „Microsoft Word“ galima eksportuoti naudojant įvairius duomenų objektus, pateikiamus „Talent“ integravus jį su „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="f25b5-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="f25b5-117">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="f25b5-117">**Long-term solution**</span></span>

<span data-ttu-id="f25b5-118">Bus pasiekiama papildomų „Power BI“ parinkčių, o „Common Data Service“, skirtai programoms, priklausys daugiau duomenų ir objektų.</span><span class="sxs-lookup"><span data-stu-id="f25b5-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>
