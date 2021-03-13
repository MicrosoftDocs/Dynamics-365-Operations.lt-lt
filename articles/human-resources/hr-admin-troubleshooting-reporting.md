---
title: Ataskaitų parinktys
description: Šiame straipsnyje aiškinama, kaip išspręsti problemą, kai klientas nori tinkinti „Microsoft Dynamics 365 Human Resources“ ataskaitas arba sukurti naujų ataskaitų.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113528"
---
# <a name="reporting-options"></a><span data-ttu-id="af6a8-103">Ataskaitų parinktys</span><span class="sxs-lookup"><span data-stu-id="af6a8-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="af6a8-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="af6a8-104">**Environment details**</span></span>

<span data-ttu-id="af6a8-105">Ši problema taikoma visoms aplinkoms.</span><span class="sxs-lookup"><span data-stu-id="af6a8-105">This issue applies to all environments.</span></span>

<span data-ttu-id="af6a8-106">**Požymis**</span><span class="sxs-lookup"><span data-stu-id="af6a8-106">**Symptom**</span></span>

<span data-ttu-id="af6a8-107">Klientas nori tinkinti „Microsoft Dynamics 365 Human Resources“ ataskaitas arba sukurti naujų ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="af6a8-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="af6a8-108">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="af6a8-108">**Issue**</span></span>

<span data-ttu-id="af6a8-109">Vartotojui nepavyksta tinkinti įdėtųjų „Microsoft Power BI“ ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="af6a8-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="af6a8-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="af6a8-110">**Solution**</span></span>

- <span data-ttu-id="af6a8-111">„Human Resources“ duomenis, kurių srautai juda į „Dataverse“, galima paskelbti naudojantis „Power Apps“ „Dataverse“ jungtimi su „Power BI Desktop“.</span><span class="sxs-lookup"><span data-stu-id="af6a8-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="af6a8-112">Atminkite, kad „Dataverse“ pateikiamas „Human Resources“ duomenų porinkinis.</span><span class="sxs-lookup"><span data-stu-id="af6a8-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="af6a8-113">Daugiau informacijos apie „Power BI“ ir ataskaitų sritis ieškokite temoje [„Power BI“ ataskaitų ir ataskaitų sričių, naudojant „Power Apps Common Data Service“, kūrimas](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="af6a8-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="af6a8-114">Elektronines ataskaitas (ER) galima naudoti kai kurioms „Human Resources“ ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="af6a8-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="af6a8-115">Kliento kuriamus tinkinimus galima atlikti per ER konfigūravimo pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="af6a8-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="af6a8-116">Duomenis į „Microsoft Excel“ arba „Microsoft Word“ galima eksportuoti naudojant įvairius duomenų objektus, pateikiamus „Human Resources“ integravus jį su „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="af6a8-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="af6a8-117">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="af6a8-117">**Long-term solution**</span></span>

<span data-ttu-id="af6a8-118">Bus pasiekiama papildomų „Power BI“ parinkčių, o „Dataverse“ priklausys daugiau duomenų ir objektų.</span><span class="sxs-lookup"><span data-stu-id="af6a8-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>
