---
title: „Dynamics 365 Commerce“ vertinimo aplinkos peržiūra
description: Šioje temoje apžvelgiama „Microsoft Dynamics 365 Commerce“ vertinimo aplinka.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e08c2f327771d7731b836840006d63b6ecb7dfc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000955"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="4aa57-103">„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra</span><span class="sxs-lookup"><span data-stu-id="4aa57-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4aa57-104">Šioje temoje apžvelgiama „Microsoft Dynamics 365 Commerce“ vertinimo aplinka.</span><span class="sxs-lookup"><span data-stu-id="4aa57-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="4aa57-105">Komercijos vertinimo aplinkos dažniausiai nėra prieinamos ir yra suteikiamos partneriams ir klientams atskyru jų prašymu.</span><span class="sxs-lookup"><span data-stu-id="4aa57-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="4aa57-106">Dėl išsamesnės informacijos, susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="4aa57-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="4aa57-107">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="4aa57-107">Overview</span></span>

<span data-ttu-id="4aa57-108">Komercijos vertinimo aplinka yra pasirenkama „Dynamics 365 Commerce“ aplinka leidžianti partneriams ir potencialiems klientams išbandyti komercinius produktus.</span><span class="sxs-lookup"><span data-stu-id="4aa57-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="4aa57-109">Vertinimo aplinkos yra išankstinio konfigūravimo dalis ir sumažina reikalaujamus žingsnius po parengimo.</span><span class="sxs-lookup"><span data-stu-id="4aa57-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="4aa57-110">Kartu su keletu nežymių apribojimų, neveikiančių funkcionalumo ir savybių, komercijos vertinimo aplinka suteikia išbaigtą komercijos patirtį ir gali būti naudojama klientų ir įgyvendinimo partnerių siekiant įvertinti gaminį ir pateikti atsiliepimą bei pritaikymo ar neatitikimų analizę.</span><span class="sxs-lookup"><span data-stu-id="4aa57-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="4aa57-111">Komercijos vertinimo aplinkos apribojimai</span><span class="sxs-lookup"><span data-stu-id="4aa57-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="4aa57-112">Nepaisant to, kad Komercijos vertinimo aplinka suteikia visą rinkinį komercijos savybių ir funkcijų, esama keleto nežymių apribojimų:</span><span class="sxs-lookup"><span data-stu-id="4aa57-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="4aa57-113">Nepaisant to, kad Komercijos vertinimo aplinka neturi geografinių apribojimų, aplinkos komponentai, tokie kaip „Retail Cloud Scale Unit“ (RCSU) ir „e-Commerce“ programos gali būti parūpintos tik Jungtinėse Amerikos Valstijose.</span><span class="sxs-lookup"><span data-stu-id="4aa57-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="4aa57-114">Komercijos vertinimo aplinkos naudojimas yra apribotas 30 dienų nuo „e-Commerce“ suteikimo dienos.</span><span class="sxs-lookup"><span data-stu-id="4aa57-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="4aa57-115">Komercijos vertinimo aplinka gali būti sėkmingai patalpinta ir pradėta naudoti tik aplinkoje, naudojančioje demonstracinę topologiją, kai visi aplinkos komponentai yra patalpinti vienoje debesyje esančioje virtualioje mašinoje (VM).</span><span class="sxs-lookup"><span data-stu-id="4aa57-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="4aa57-116">Pagrindinis topologijos apribojimas yra konkuruojančių vartotojų skaičius palaikomoje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="4aa57-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="4aa57-117">Pradžia</span><span class="sxs-lookup"><span data-stu-id="4aa57-117">Get started</span></span>

<span data-ttu-id="4aa57-118">Komercijos vertinimo aplinkos parengimui, žr. [Komercijos vertinimo aplinkos nustatymas](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="4aa57-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4aa57-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4aa57-119">Additional resources</span></span>

[<span data-ttu-id="4aa57-120">Parenkite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="4aa57-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="4aa57-121">Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="4aa57-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="4aa57-122">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="4aa57-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="4aa57-123">Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="4aa57-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="4aa57-124">„Dynamics 365 Commerce“ vertinimo aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="4aa57-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
