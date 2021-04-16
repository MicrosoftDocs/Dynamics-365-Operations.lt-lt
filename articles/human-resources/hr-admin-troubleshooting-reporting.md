---
title: Ataskaitų parinktys
description: Šiame straipsnyje aiškinama, kaip išspręsti problemą, kai klientas nori tinkinti „Microsoft Dynamics 365 Human Resources“ ataskaitas arba sukurti naujų ataskaitų.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2d0fc6b2d4af6ad021943717645bfff7a27797a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803902"
---
# <a name="reporting-options"></a><span data-ttu-id="9e30e-103">Ataskaitų parinktys</span><span class="sxs-lookup"><span data-stu-id="9e30e-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9e30e-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="9e30e-104">**Environment details**</span></span>

<span data-ttu-id="9e30e-105">Ši problema taikoma visoms aplinkoms.</span><span class="sxs-lookup"><span data-stu-id="9e30e-105">This issue applies to all environments.</span></span>

<span data-ttu-id="9e30e-106">**Požymis**</span><span class="sxs-lookup"><span data-stu-id="9e30e-106">**Symptom**</span></span>

<span data-ttu-id="9e30e-107">Klientas nori tinkinti „Microsoft Dynamics 365 Human Resources“ ataskaitas arba sukurti naujų ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="9e30e-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="9e30e-108">**Išdavimas**</span><span class="sxs-lookup"><span data-stu-id="9e30e-108">**Issue**</span></span>

<span data-ttu-id="9e30e-109">Vartotojui nepavyksta tinkinti įdėtųjų „Microsoft Power BI“ ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="9e30e-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="9e30e-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="9e30e-110">**Solution**</span></span>

- <span data-ttu-id="9e30e-111">„Human Resources“ duomenis, kurių srautai juda į „Dataverse“, galima paskelbti naudojantis „Power Apps“ „Dataverse“ jungtimi su „Power BI Desktop“.</span><span class="sxs-lookup"><span data-stu-id="9e30e-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="9e30e-112">Atminkite, kad „Dataverse“ pateikiamas „Human Resources“ duomenų porinkinis.</span><span class="sxs-lookup"><span data-stu-id="9e30e-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="9e30e-113">Daugiau informacijos apie „Power BI“ ir ataskaitų sritis ieškokite temoje [„Power BI“ ataskaitų ir ataskaitų sričių, naudojant „Power Apps Common Data Service“, kūrimas](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="9e30e-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="9e30e-114">Elektronines ataskaitas (ER) galima naudoti kai kurioms „Human Resources“ ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="9e30e-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="9e30e-115">Kliento kuriamus tinkinimus galima atlikti per ER konfigūravimo pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="9e30e-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="9e30e-116">Duomenis į „Microsoft Excel“ arba „Microsoft Word“ galima eksportuoti naudojant įvairius duomenų objektus, pateikiamus „Human Resources“ integravus jį su „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="9e30e-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="9e30e-117">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="9e30e-117">**Long-term solution**</span></span>

<span data-ttu-id="9e30e-118">Bus pasiekiama papildomų „Power BI“ parinkčių, o „Dataverse“ priklausys daugiau duomenų ir objektų.</span><span class="sxs-lookup"><span data-stu-id="9e30e-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]