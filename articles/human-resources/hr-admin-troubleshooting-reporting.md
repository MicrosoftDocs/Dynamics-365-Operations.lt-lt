---
title: Ataskaitų parinktys
description: Šiame straipsnyje aiškinama, kaip išspręsti problemą, kai klientas nori tinkinti „Microsoft Dynamics 365 Human Resources“ ataskaitas arba sukurti naujų ataskaitų.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010011"
---
# <a name="reporting-options"></a><span data-ttu-id="6c296-103">Ataskaitų parinktys</span><span class="sxs-lookup"><span data-stu-id="6c296-103">Reporting options</span></span>

<span data-ttu-id="6c296-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="6c296-104">**Environment details**</span></span>

<span data-ttu-id="6c296-105">Ši problema taikoma visoms aplinkoms.</span><span class="sxs-lookup"><span data-stu-id="6c296-105">This issue applies to all environments.</span></span>

<span data-ttu-id="6c296-106">**Požymis**</span><span class="sxs-lookup"><span data-stu-id="6c296-106">**Symptom**</span></span>

<span data-ttu-id="6c296-107">Klientas nori tinkinti „Microsoft Dynamics 365 Human Resources“ ataskaitas arba sukurti naujų ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="6c296-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="6c296-108">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="6c296-108">**Issue**</span></span>

<span data-ttu-id="6c296-109">Vartotojui nepavyksta tinkinti įdėtųjų „Microsoft Power BI“ ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="6c296-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="6c296-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="6c296-110">**Solution**</span></span>

- <span data-ttu-id="6c296-111">„Human Resources“ duomenis, kurių srautai juda į „Common Data Service“, galima paskelbti naudojantis „Power Apps“ „Common Data Service“ jungtimi su „Power BI Desktop“.</span><span class="sxs-lookup"><span data-stu-id="6c296-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="6c296-112">Atminkite, kad „Common Data Service“ pateikiamas „Human Resources“ duomenų porinkinis.</span><span class="sxs-lookup"><span data-stu-id="6c296-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="6c296-113">Daugiau informacijos apie „Power BI“ ir ataskaitų sritis ieškokite temoje [„Power BI“ ataskaitų ir ataskaitų sričių, naudojant „Power Apps Common Data Service“, kūrimas](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="6c296-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="6c296-114">Elektronines ataskaitas (ER) galima naudoti kai kurioms „Human Resources“ ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="6c296-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="6c296-115">Kliento kuriamus tinkinimus galima atlikti per ER konfigūravimo pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="6c296-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="6c296-116">Duomenis į „Microsoft Excel“ arba „Microsoft Word“ galima eksportuoti naudojant įvairius duomenų objektus, pateikiamus „Human Resources“ integravus jį su „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="6c296-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="6c296-117">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="6c296-117">**Long-term solution**</span></span>

<span data-ttu-id="6c296-118">Bus pasiekiama papildomų „Power BI“ parinkčių, o „Common Data Service“ priklausys daugiau duomenų ir objektų.</span><span class="sxs-lookup"><span data-stu-id="6c296-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
