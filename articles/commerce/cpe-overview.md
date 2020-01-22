---
title: „Commerce” peržiūros aplinkos apžvalga
description: Šioje temoje apžvelgiama „Microsoft Dynamics 365 Commerce“ peržiūros aplinka.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906075"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="30aed-103">„Commerce” peržiūros aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="30aed-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="30aed-104">Šioje temoje apžvelgiama „Microsoft Dynamics 365 Commerce“ peržiūros aplinka.</span><span class="sxs-lookup"><span data-stu-id="30aed-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="30aed-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="30aed-105">Overview</span></span>

<span data-ttu-id="30aed-106">„Commerce“ peržiūros aplinka yra pasirenkama visapusė „Dynamics 365 Commerce“ peržiūros aplinka, kurią naudodami galimi klientai gali išbandyti „Commerce“ produktą prieš jį išleidžiant visai visuomenei.</span><span class="sxs-lookup"><span data-stu-id="30aed-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="30aed-107">Be kai kurių nedidelių apribojimų, kurie neturi įtakos funkcijoms ar veikimui, „Commerce“ peržiūros aplinkoje suteikiamos visos „Commerce“ funkcijos ir, ją naudodami, klientai bei diegimo partneriai gali įvertinti produktą, pateikti atsiliepimų ir atlikti tinkamumo / trūkumų analizę.</span><span class="sxs-lookup"><span data-stu-id="30aed-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="30aed-108">„Commerce“ peržiūros aplinkos apribojimai</span><span class="sxs-lookup"><span data-stu-id="30aed-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="30aed-109">Nors „Commerce“ peržiūros aplinkoje suteikiamos visos „Commerce“ funkcijos ir galimybės, yra keletas nedidelių apribojimų, nurodytų toliau.</span><span class="sxs-lookup"><span data-stu-id="30aed-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="30aed-110">Nors pačiai „Commerce“ peržiūros aplinkai netaikomi jokie geografiniai apribojimai, aplinkos komponentus, pvz., „Retail Cloud Scale Unit“ (RCSU) ir el. prekybos programas, galima parengti tik Jungtinėse Valstijose.</span><span class="sxs-lookup"><span data-stu-id="30aed-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="30aed-111">„Commerce“ peržiūos aplinkos naudojimo terminas apribotas iki 30 dienų nuo el. prekybos parengimo datos.</span><span class="sxs-lookup"><span data-stu-id="30aed-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="30aed-112">„Commerce“ peržiūros aplinką sėkmingai įdiegti ir inicijuoti galima tik tokioje aplinkoje, kurioje naudojama demonstracinė topologija ir visi aplinkos komponentai yra įdiegti vienoje virtualiojoje mašinoje (VM).</span><span class="sxs-lookup"><span data-stu-id="30aed-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="30aed-113">Pagrindinis šios „OneBox“ VM topologijos apribojimas yra vienu metu dirbančių vartotojų skaičius, kurį gali palaikyti peržiūros aplinka.</span><span class="sxs-lookup"><span data-stu-id="30aed-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="30aed-114">„Commerce“ peržiūros aplinką galima įvertinti tik tol, kol „Commerce“ produktas nėra pasiekiamas visuotinai.</span><span class="sxs-lookup"><span data-stu-id="30aed-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="30aed-115">Po visuotinio pasiekiamumo etapo bus galima naudoti naujas demonstracines aplinkas.</span><span class="sxs-lookup"><span data-stu-id="30aed-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="30aed-116">Darbo pradžia</span><span class="sxs-lookup"><span data-stu-id="30aed-116">Get started</span></span>

<span data-ttu-id="30aed-117">Jei norite „Commerce“ peržiūros aplinką parengti, žr. [„Commerce“ peržiūros aplinkos parengimas](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="30aed-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30aed-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="30aed-118">Additional resources</span></span>

[<span data-ttu-id="30aed-119">„Commerce” peržiūros aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="30aed-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="30aed-120">„Commerce” peržiūros aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="30aed-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="30aed-121">Pasirenkamų „Commerce” peržiūros aplinkos funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="30aed-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="30aed-122">DUK apie „Commerce” peržiūros aplinką</span><span class="sxs-lookup"><span data-stu-id="30aed-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
