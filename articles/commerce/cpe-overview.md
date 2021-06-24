---
title: „Dynamics 365 Commerce” vertinimo aplinkos apžvalga
description: Šioje temoje apžvelgiama „Microsoft Dynamics 365 Commerce“ vertinimo aplinka.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c890d7c49b6607ab0cbad536bbf8a3649465a7c1
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193497"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="825ed-103">„Dynamics 365 Commerce” vertinimo aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="825ed-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="825ed-104">Šioje temoje apžvelgiama „Microsoft Dynamics 365 Commerce“ vertinimo aplinka.</span><span class="sxs-lookup"><span data-stu-id="825ed-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="825ed-105">Komercijos vertinimo aplinkos dažniausiai nėra prieinamos ir yra suteikiamos partneriams ir klientams atskiru jų prašymu.</span><span class="sxs-lookup"><span data-stu-id="825ed-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="825ed-106">Dėl išsamesnės informacijos, susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="825ed-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="825ed-107">Komercijos vertinimo aplinka yra pasirenkama „Dynamics 365 Commerce“ aplinka leidžianti partneriams ir potencialiems klientams išbandyti komercinius produktus.</span><span class="sxs-lookup"><span data-stu-id="825ed-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="825ed-108">Vertinimo aplinkos yra išankstinio konfigūravimo dalis ir sumažina reikalaujamus žingsnius po parengimo.</span><span class="sxs-lookup"><span data-stu-id="825ed-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="825ed-109">Kartu su keletu nežymių apribojimų, neveikiančių funkcionalumo ir savybių, komercijos vertinimo aplinka suteikia išbaigtą komercijos patirtį ir gali būti naudojama klientų ir įgyvendinimo partnerių siekiant įvertinti gaminį ir pateikti atsiliepimą bei pritaikymo ar neatitikimų analizę.</span><span class="sxs-lookup"><span data-stu-id="825ed-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="825ed-110">Komercijos vertinimo aplinkos apribojimai</span><span class="sxs-lookup"><span data-stu-id="825ed-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="825ed-111">Nepaisant to, kad Komercijos vertinimo aplinka suteikia visą rinkinį komercijos savybių ir funkcijų, esama keleto nežymių apribojimų:</span><span class="sxs-lookup"><span data-stu-id="825ed-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="825ed-112">Nepaisant to, kad Komercijos vertinimo aplinka neturi geografinių apribojimų, aplinkos komponentai, tokie kaip „Retail Cloud Scale Unit“ (RCSU) ir „e-Commerce“ programos gali būti parūpintos tik Jungtinėse Amerikos Valstijose.</span><span class="sxs-lookup"><span data-stu-id="825ed-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="825ed-113">Komercijos vertinimo aplinkos naudojimas yra apribotas 30 dienų nuo „e-Commerce“ suteikimo dienos.</span><span class="sxs-lookup"><span data-stu-id="825ed-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="825ed-114">Komercijos vertinimo aplinka gali būti sėkmingai patalpinta ir pradėta naudoti tik aplinkoje, naudojančioje demonstracinę topologiją, kai visi aplinkos komponentai yra patalpinti vienoje debesyje esančioje virtualioje mašinoje (VM).</span><span class="sxs-lookup"><span data-stu-id="825ed-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="825ed-115">Pagrindinis topologijos apribojimas yra konkuruojančių vartotojų skaičius palaikomoje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="825ed-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="825ed-116">Pradžia</span><span class="sxs-lookup"><span data-stu-id="825ed-116">Get started</span></span>

<span data-ttu-id="825ed-117">Komercijos vertinimo aplinkos parengimui, žr. [Komercijos vertinimo aplinkos nustatymas](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="825ed-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="825ed-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="825ed-118">Additional resources</span></span>

[<span data-ttu-id="825ed-119">Parenkite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="825ed-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="825ed-120">Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="825ed-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="825ed-121">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="825ed-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="825ed-122">Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="825ed-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="825ed-123">„Dynamics 365 Commerce“ vertinimo aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="825ed-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
