---
title: „Dynamics 365 Commerce“ vertinimo aplinkos DUK
description: Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a0c6f82432a4786f23f12122f3806c3b96a05c8f
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193599"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="b4f09-103">DUK apie „Dynamics 365 Commerce” vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="b4f09-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4f09-104">Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="b4f09-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="b4f09-105">**Ar galime naudoti komercijos vertinimo aplinką kaip „e-Commerce“ parduotuvę savo klientams, kurie jau įgyvendino „Retail“?**</span><span class="sxs-lookup"><span data-stu-id="b4f09-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="b4f09-106">Nr.</span><span class="sxs-lookup"><span data-stu-id="b4f09-106">No.</span></span> <span data-ttu-id="b4f09-107">Komercijos vertinimo aplinka yra skirta tik vertinimui.</span><span class="sxs-lookup"><span data-stu-id="b4f09-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="b4f09-108">Jei reikia aplinkos klientui, kuris yra įsidiegęs „Retail“, kreipkitės į „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="b4f09-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="b4f09-109">**Ar gali komercijos vertinimo aplinka būti naudojama „e-Commerce“ savybių parengimui esančioje aplinkoje ar programose, kurios įgyvendino „Retail“?**</span><span class="sxs-lookup"><span data-stu-id="b4f09-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="b4f09-110">Ne (dažniausiai).</span><span class="sxs-lookup"><span data-stu-id="b4f09-110">No (mostly).</span></span> <span data-ttu-id="b4f09-111">Komercijos vertinimo komponentai yra prieinami tik aplinkose, kurios atitinka konfigūravimus, nustatytus būtinosiose sąlygose ir parengimo gide.</span><span class="sxs-lookup"><span data-stu-id="b4f09-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="b4f09-112">Taip pat, reikalaujama demo duomenų pagrindo versija nebus prieinama aplinkose, kurios turi pirmąją versiją, ankstesnę nei 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="b4f09-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="b4f09-113">**Kiek kainuoja patalpinti komercijos vertinimo aplinką „Microsoft Azure“ per „Microsoft Dynamics Lifecycle Services“ (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="b4f09-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="b4f09-114">Įprasta „Dynamics 365 Finance“/„Dynamics 365 Supply Chain Management“/„Dynamics 365 Commerce“ būstinės demo aplinka (virtuali mašina \[VM\]) bus patalpinta jūsų „Azure“ prenumeratoje.</span><span class="sxs-lookup"><span data-stu-id="b4f09-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="b4f09-115">Norėdami įvertinti šiuos kaštus, galite naudoti [„Azure“ kainų skaičiuotuvą](https://azure.microsoft.com/pricing/calculator/).</span><span class="sxs-lookup"><span data-stu-id="b4f09-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="b4f09-116">Kiti komponentai, tokie kaip „Commerce Scale Unit“, komercijos vietos kūrimo įrankis ir jūsų „e-Commerce“ vieta bus prieinama kaip programinės įrangos paslaugos (SaaS) ir patalpinti „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="b4f09-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="b4f09-117">**Kokios „Azure“ geografinės sritys šiuo metu palaikomos komercijos vertinimo aplinkoje?**</span><span class="sxs-lookup"><span data-stu-id="b4f09-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="b4f09-118">Komercijos vertinimo aplinka gali būt patalpinta tik Šiaurės Amerikos regione.</span><span class="sxs-lookup"><span data-stu-id="b4f09-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="b4f09-119">**Ar galima atsisiųsti virtualųjį standųjį diską (VHD), kuriame yra visavertės „OneBox“ virtualiosios mašinos (VM) parinktis?**</span><span class="sxs-lookup"><span data-stu-id="b4f09-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="b4f09-120">„Dynamics 365 Commerce“ ir „Commerce Scale Unit“ yra visa programinė įranga, kaip paslaugų (Saas) ir turi būti patalpinta debesyje.</span><span class="sxs-lookup"><span data-stu-id="b4f09-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="b4f09-121">**Kiek laiko galima naudoti komercijos vertinimo aplinką?**</span><span class="sxs-lookup"><span data-stu-id="b4f09-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="b4f09-122">Komercijos vertinimo aplinka turi 30 dienų laiko limitą nuo dienos, kai SaaS komponentai, tokie kaip „Commerce Scale Unit“, komercijos vietos kūrimo įrankis ir jūsų „e-Commerce“ vieta yra suteikta.</span><span class="sxs-lookup"><span data-stu-id="b4f09-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="b4f09-123">**Ar galiu pratęsti komercijos vertinimo aplinkos laikotarpį?**</span><span class="sxs-lookup"><span data-stu-id="b4f09-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="b4f09-124">Laikotarpio pratęsimas yra išimtis iš taisyklės ir vertinamas kiekvienu atskiru atveju skirtingai.</span><span class="sxs-lookup"><span data-stu-id="b4f09-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="b4f09-125">Turėtumėte susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="b4f09-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4f09-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b4f09-126">Additional resources</span></span>

[<span data-ttu-id="b4f09-127">„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra</span><span class="sxs-lookup"><span data-stu-id="b4f09-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b4f09-128">Parenkite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="b4f09-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b4f09-129">Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="b4f09-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b4f09-130">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="b4f09-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="b4f09-131">Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="b4f09-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]