---
title: Kas nauja ar pasikeitė „Dynamics 365 Supply Chain Management“ 10.0.6 (2019 m. lapkritis)
description: Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Supply Chain Management“ 10.0.6 funkcijos.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433642"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="6886a-103">Kas nauja ar pasikeitė „Dynamics 365 Supply Chain Management“ 10.0.6 (2019 m. lapkritis)</span><span class="sxs-lookup"><span data-stu-id="6886a-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6886a-104">Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.6 funkcijos.</span><span class="sxs-lookup"><span data-stu-id="6886a-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="6886a-105">Šios versijos komponavimo numeris yra 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="6886a-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="6886a-106">Nors bendro pasiekiamumo data yra lapkričio mėn., naujos funkcijos prieinamos su ankstyvu leidimu spalio mėn.</span><span class="sxs-lookup"><span data-stu-id="6886a-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="6886a-107">Daugiau informacijos apie versiją 10.0.6 žr. [Papildomi ištekliai](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="6886a-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="6886a-108">Produkto konfigūracijos modelių V2 duomenų objektas</span><span class="sxs-lookup"><span data-stu-id="6886a-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="6886a-109">„Produkto konfigūracijos modelių“ duomenų objekto antra versija yra išleista (vadinama „produktų konfigūracijos modeliai V2“).</span><span class="sxs-lookup"><span data-stu-id="6886a-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="6886a-110">Numatytasis šablonas „418 – produkto konfigūracijos modeliai“ taip pat turi būti toks, kad naudotų naują „produkto konfigūracijos modelių v2“ duomenų objektą importavimo / eksportavimo sistemos šablonuose.</span><span class="sxs-lookup"><span data-stu-id="6886a-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="6886a-111">Šablonas nebus automatiškai atnaujinamas, todėl jums reikės įkelti šabloną iš numatytojo rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="6886a-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="6886a-112">V2 objektas eksportuoja vieną eilutę kaip atskirą failą priede, o ne įterpinį, sprendžiant v1 objekto dydžio apribojimus.</span><span class="sxs-lookup"><span data-stu-id="6886a-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="6886a-113">Ką reikia daryti norint atlikti šį keitimą?</span><span class="sxs-lookup"><span data-stu-id="6886a-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="6886a-114">Kadangi v1 objektas buvo pasenęs, turite pradėti pereiti iš V1 į V2.</span><span class="sxs-lookup"><span data-stu-id="6886a-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="6886a-115">Jei naudojate šabloną „418-produkto konfigūracijos modeliai“, galite spustelėti mygtuką „įkelti numatytuosius šablonus“ ir iš naujo įkelti šabloną „418 – produkto konfigūracijos modeliai“</span><span class="sxs-lookup"><span data-stu-id="6886a-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="6886a-116">Jei norite išlaikyti suderinamumą su esamomis sistemomis, galite kol kas tęsti naudojimąsi esamu šablonu ir (pasenusiu) v1 objektu, kol savo integracijas perkelsite į naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="6886a-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="6886a-117">Funkcijų valdymo pagerinimai</span><span class="sxs-lookup"><span data-stu-id="6886a-117">Feature management enhancements</span></span>
<span data-ttu-id="6886a-118">Funkcijų valdymas dabar leidžia įjungti visas naujas funkcijas pagal numatytuosius parametrus, prašyti patvirtinimo, kad būtų įjungta funkcija, ir įjungti visas dar neįjungtas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="6886a-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="6886a-119">Už pirkimo sutartį atsakinga šalis</span><span class="sxs-lookup"><span data-stu-id="6886a-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="6886a-120">Dabar turite galimybę apibrėžti pirminės ir antrinės atsakomybės šalis pirkimo sutarties klasifikacijos formoje ir iš jos parengiamoje pirkimo sutartyje.</span><span class="sxs-lookup"><span data-stu-id="6886a-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="6886a-121">Tai leidžia vartotojams pamatyti tai, kas praleista sutartyse.</span><span class="sxs-lookup"><span data-stu-id="6886a-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="6886a-122">RFQ saitas pirkimo užsakymo eilutėj</span><span class="sxs-lookup"><span data-stu-id="6886a-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="6886a-123">Galite įtraukti nuorodos saitą iš pirkimo užsakymo eilučių atgal į atitinkamas RFQ eilutes, iš kurių jos atsirado, kad vartotojas galėtų lengvai gauti papildomą pasiūlymo patvirtinimo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="6886a-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6886a-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6886a-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6886a-125">Klaidų ištaisymai</span><span class="sxs-lookup"><span data-stu-id="6886a-125">Bug fixes</span></span>
<span data-ttu-id="6886a-126">Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.6 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="6886a-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="6886a-127">Platformos „update 30“</span><span class="sxs-lookup"><span data-stu-id="6886a-127">Platform update 30</span></span>
<span data-ttu-id="6886a-128">„Microsoft Dynamics 365 Supply Chain Management“ 10.0.6 sudaro platformos 30 naujinimas.</span><span class="sxs-lookup"><span data-stu-id="6886a-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="6886a-129">Norėdami daugiau sužinoti apie platformos 30 naujinimą, žr. [Kas nauja ar pakeista platformos 30 naujinime](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="6886a-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="6886a-130">„Dynamics 365“: 2019 m. 2-os leidimo bangos planas</span><span class="sxs-lookup"><span data-stu-id="6886a-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="6886a-131">Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?</span><span class="sxs-lookup"><span data-stu-id="6886a-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="6886a-132">Peržiūrėkite [„Dynamics 365“: 2019 m. 2-os leidimo bangos planas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="6886a-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="6886a-133">Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.</span><span class="sxs-lookup"><span data-stu-id="6886a-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="6886a-134">Pašalintos ir pasenusios „Supply Chain Management“ funkcijos</span><span class="sxs-lookup"><span data-stu-id="6886a-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="6886a-135">Temoje [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) aprašomos „Supply Chain Management“ funkcijos, kurios yra pašalintos, yra suplanuotos pašalinti arba yra pasenusios.</span><span class="sxs-lookup"><span data-stu-id="6886a-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="6886a-136">*Pašalinta* funkcija nebėra įtraukta į produktą.</span><span class="sxs-lookup"><span data-stu-id="6886a-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="6886a-137">*Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.</span><span class="sxs-lookup"><span data-stu-id="6886a-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="6886a-138">Prieš pašalinant iš produkto bet kokią funkciją, pranešimas apie nebenaudojimą bus paskelbtas [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) temoje 12 mėnesių prieš pašalinimą.</span><span class="sxs-lookup"><span data-stu-id="6886a-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="6886a-139">Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejatainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių.</span><span class="sxs-lookup"><span data-stu-id="6886a-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="6886a-140">Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.</span><span class="sxs-lookup"><span data-stu-id="6886a-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
