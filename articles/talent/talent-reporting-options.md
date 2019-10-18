---
title: Ataskaitų parinktys sprendime „Talent“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai klientas nori tinkinti „Microsoft Dynamics 365 Talent“ ataskaitas arba sukurti naujų ataskaitų.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 50342c847200d015a66c6f22007070bb26c6caef
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009357"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="38ef0-103">Ataskaitų parinktys sprendime „Talent“</span><span class="sxs-lookup"><span data-stu-id="38ef0-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38ef0-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="38ef0-104">**Environment details**</span></span>

<span data-ttu-id="38ef0-105">Ši problema taikoma visoms aplinkoms.</span><span class="sxs-lookup"><span data-stu-id="38ef0-105">This issue applies to all environments.</span></span>

<span data-ttu-id="38ef0-106">**Požymis**</span><span class="sxs-lookup"><span data-stu-id="38ef0-106">**Symptom**</span></span>

<span data-ttu-id="38ef0-107">Klientas nori tinkinti „Microsoft Dynamics 365 Talent“ ataskaitas arba sukurti naujų ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="38ef0-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="38ef0-108">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="38ef0-108">**Issue**</span></span>

<span data-ttu-id="38ef0-109">Vartotojui nepavyksta tinkinti įdėtųjų „Microsoft Power BI“ ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="38ef0-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="38ef0-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="38ef0-110">**Solution**</span></span>

- <span data-ttu-id="38ef0-111">„Core HR“ duomenis, kurių srautai juda į „Common Data Service“, galima paskelbti naudojantis „PowerApps“ „Common Data Service“ jungtimi su „Power BI Desktop“.</span><span class="sxs-lookup"><span data-stu-id="38ef0-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="38ef0-112">Atminkite, kad „Common Data Service“ pateikiamas „Core HR“ duomenų subrinkinys.</span><span class="sxs-lookup"><span data-stu-id="38ef0-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="38ef0-113">Daugiau informacijos apie „Power BI“ ir ataskaitų sritis ieškokite temoje [„Power BI“ ataskaitų ir ataskaitų sričių, naudojant „PowerApps Common Data Service“, kūrimas](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="38ef0-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="38ef0-114">Elektronines ataskaitas (ER) galima naudoti kai kurioms „Talent“ ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="38ef0-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="38ef0-115">Kliento kuriamus tinkinimus galima atlikti per ER konfigūravimo pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="38ef0-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="38ef0-116">Duomenis į „Microsoft Excel“ arba „Microsoft Word“ galima eksportuoti naudojant įvairius duomenų objektus, pateikiamus „Talent“ integravus jį su „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="38ef0-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="38ef0-117">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="38ef0-117">**Long-term solution**</span></span>

<span data-ttu-id="38ef0-118">Bus pasiekiama papildomų „Power BI“ parinkčių, o „Common Data Service“ priklausys daugiau duomenų ir objektų.</span><span class="sxs-lookup"><span data-stu-id="38ef0-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
