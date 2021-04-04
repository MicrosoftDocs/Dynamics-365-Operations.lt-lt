---
title: „Dynamics 365 Commerce” vertinimo aplinkos apžvalga
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
ms.openlocfilehash: cc6bffba6ee402c6b48d6a3c8f8356eb32b5423b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478025"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="65f44-103">„Dynamics 365 Commerce” vertinimo aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="65f44-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65f44-104">Šioje temoje apžvelgiama „Microsoft Dynamics 365 Commerce“ vertinimo aplinka.</span><span class="sxs-lookup"><span data-stu-id="65f44-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="65f44-105">Komercijos vertinimo aplinkos dažniausiai nėra prieinamos ir yra suteikiamos partneriams ir klientams atskyru jų prašymu.</span><span class="sxs-lookup"><span data-stu-id="65f44-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="65f44-106">Dėl išsamesnės informacijos, susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="65f44-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="65f44-107">Komercijos vertinimo aplinka yra pasirenkama „Dynamics 365 Commerce“ aplinka leidžianti partneriams ir potencialiems klientams išbandyti komercinius produktus.</span><span class="sxs-lookup"><span data-stu-id="65f44-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="65f44-108">Vertinimo aplinkos yra išankstinio konfigūravimo dalis ir sumažina reikalaujamus žingsnius po parengimo.</span><span class="sxs-lookup"><span data-stu-id="65f44-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="65f44-109">Kartu su keletu nežymių apribojimų, neveikiančių funkcionalumo ir savybių, komercijos vertinimo aplinka suteikia išbaigtą komercijos patirtį ir gali būti naudojama klientų ir įgyvendinimo partnerių siekiant įvertinti gaminį ir pateikti atsiliepimą bei pritaikymo ar neatitikimų analizę.</span><span class="sxs-lookup"><span data-stu-id="65f44-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="65f44-110">Komercijos vertinimo aplinkos apribojimai</span><span class="sxs-lookup"><span data-stu-id="65f44-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="65f44-111">Nepaisant to, kad Komercijos vertinimo aplinka suteikia visą rinkinį komercijos savybių ir funkcijų, esama keleto nežymių apribojimų:</span><span class="sxs-lookup"><span data-stu-id="65f44-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="65f44-112">Nepaisant to, kad Komercijos vertinimo aplinka neturi geografinių apribojimų, aplinkos komponentai, tokie kaip „Retail Cloud Scale Unit“ (RCSU) ir „e-Commerce“ programos gali būti parūpintos tik Jungtinėse Amerikos Valstijose.</span><span class="sxs-lookup"><span data-stu-id="65f44-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="65f44-113">Komercijos vertinimo aplinkos naudojimas yra apribotas 30 dienų nuo „e-Commerce“ suteikimo dienos.</span><span class="sxs-lookup"><span data-stu-id="65f44-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="65f44-114">Komercijos vertinimo aplinka gali būti sėkmingai patalpinta ir pradėta naudoti tik aplinkoje, naudojančioje demonstracinę topologiją, kai visi aplinkos komponentai yra patalpinti vienoje debesyje esančioje virtualioje mašinoje (VM).</span><span class="sxs-lookup"><span data-stu-id="65f44-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="65f44-115">Pagrindinis topologijos apribojimas yra konkuruojančių vartotojų skaičius palaikomoje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="65f44-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="65f44-116">Pradžia</span><span class="sxs-lookup"><span data-stu-id="65f44-116">Get started</span></span>

<span data-ttu-id="65f44-117">Komercijos vertinimo aplinkos parengimui, žr. [Komercijos vertinimo aplinkos nustatymas](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="65f44-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65f44-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="65f44-118">Additional resources</span></span>

[<span data-ttu-id="65f44-119">Parenkite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="65f44-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="65f44-120">Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="65f44-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="65f44-121">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="65f44-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="65f44-122">Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="65f44-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="65f44-123">„Dynamics 365 Commerce“ vertinimo aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="65f44-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
