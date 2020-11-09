---
title: Eksperimento hipotezės ir metrikos nustatymas
description: Šioje temoje aprašoma, kaip nustatyti eksperimento, kurį vykdysite „e-Commerce“ svetainėje „Dynamics 365 Commerce”, hipotezę ir sėkmės metriką.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930250"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="35e42-103">Eksperimento hipotezės ir sėkmės metrikos nustatymas</span><span class="sxs-lookup"><span data-stu-id="35e42-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="35e42-104">Pirmojo eksperimento ciklo etapo metu nustatoma eksperimento hipotezė ir metrika, sekama norint įvertinti sėkmę.</span><span class="sxs-lookup"><span data-stu-id="35e42-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="35e42-105">Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su [eksperimento nustatymu ir vykdymu](experimentation-overview.md) „e-Commerce“ svetainėje „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="35e42-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="35e42-106">Papildomi veiksmai aprašomi kitose temose.</span><span class="sxs-lookup"><span data-stu-id="35e42-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="35e42-107">[ ![Vartotojo eksperimentavimo kelionė – nustatymas](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="35e42-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="35e42-108">Hipotezė yra teiginys, kuriame numatote eksperimento rezultatą.</span><span class="sxs-lookup"><span data-stu-id="35e42-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="35e42-109">Daug veiksnių padeda apibrėžti hipotezę, pvz., tyrimai apie vartotojų elgseną ir jūsų surinkti svetainių duomenys.</span><span class="sxs-lookup"><span data-stu-id="35e42-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="35e42-110">Kurdami hipotezę nurodysite prielaidą ar teoriją, kurią norite patvirtinti atlikdami eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="35e42-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="35e42-111">Jūsų eksperimento hipotezės pavyzdys gali būti „*mano pagrindiniame puslapyje esančių baltų marškinėlių nuotrauka vasaros mėnesiais padidins paspaudimų rodiklį labiau nei tamsaus megztinio nuotrauka, nes vasarą žmonės nori dėvėti ką nors lengvo ir šviesaus.*”</span><span class="sxs-lookup"><span data-stu-id="35e42-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="35e42-112">Tokiu atveju sukurkite variacijas, apimančias baltų marškinėlių ir tamsaus megztinio atvejus, ir publikuokite abi tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="35e42-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="35e42-113">Norint patvirtinti hipotezę, eksperimento sėkmė arba nesėkmė turėtų būti tiesiogiai susieta su vartotojų veiksmais; pavyzdžiui, jei svetainės vartotojas spusteli saitą arba mygtuką.</span><span class="sxs-lookup"><span data-stu-id="35e42-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="35e42-114">Šie veiksmai turi atitikti įvykius, kurie bus pateikti eksperimentą stebinčiai trečiosios šalies paslaugai.</span><span class="sxs-lookup"><span data-stu-id="35e42-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="35e42-115">Ilgainiui vartotojų, atliekančių veiksmą, procentinė dalis bus susumuota kaip metrika, kurią galėsite naudoti ataskaitoms generuoti ir analizei atlikti.</span><span class="sxs-lookup"><span data-stu-id="35e42-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="35e42-116">Norėdami peržiūrėti visus galimus įvykius ir atributus, žr. temą [„Commerce” komponentų įvykiai triktims diagnozuoti ir šalinti](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="35e42-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="35e42-117">Ankstesnis veiksmas</span><span class="sxs-lookup"><span data-stu-id="35e42-117">Previous step</span></span>
[<span data-ttu-id="35e42-118">Eksperimentavimas „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="35e42-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="35e42-119">Kitas veiksmas</span><span class="sxs-lookup"><span data-stu-id="35e42-119">Next step</span></span>
[<span data-ttu-id="35e42-120">Eksperimento nustatymas</span><span class="sxs-lookup"><span data-stu-id="35e42-120">Set up an experiment</span></span>](experimentation-setup.md)