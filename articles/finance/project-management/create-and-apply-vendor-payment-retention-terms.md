---
title: Mokėjimo tiekėjui užlaikymo sąlygų kūrimas ir taikymas
description: Šioje temoje pateikiama informacija apie tai, kaip nustatyti ir tvarkyti mokėjimo tiekėjui užlaikymo sąlygas.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410249"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="e5535-103">Mokėjimo tiekėjui užlaikymo sąlygų kūrimas ir taikymas</span><span class="sxs-lookup"><span data-stu-id="e5535-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="e5535-104">Projekto mokėjimo tiekėjui užlaikymo sąlygas nustatyti naudinga, kai jūsų organizacija nori užlaikyti tiekėjui atliekamų mokėjimų dalį.</span><span class="sxs-lookup"><span data-stu-id="e5535-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="e5535-105">Pavyzdžiui, kai norite sulaikyti mokėjimą tiekėjui, kol pristatyti produktai atitiks jūsų lūkesčius.</span><span class="sxs-lookup"><span data-stu-id="e5535-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="e5535-106">Mokėjimo tiekėjui užlaikymo sąlygas galima nurodyti derybų dėl tiekėjo sutarties metu.</span><span class="sxs-lookup"><span data-stu-id="e5535-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="e5535-107">Mokėjimo tiekėjui užlaikymo sąlygų kūrimas</span><span class="sxs-lookup"><span data-stu-id="e5535-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="e5535-108">Galite įvesti mokėjimo tiekėjui procentinę dalį, kurią norite užlaikyti, ir anksčiau užlaikytų sumų procentinę dalį, kurią norite atiduoti.</span><span class="sxs-lookup"><span data-stu-id="e5535-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="e5535-109">Sumos automatiškai užlaikomos tiekėjo SF, kol pasiekiama nurodyta sutarties pabaigimo būsena.</span><span class="sxs-lookup"><span data-stu-id="e5535-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="e5535-110">Nustatę užlaikymo sąlygas, galite jas taikyti bet kuriame šio tiekėjo projekte.</span><span class="sxs-lookup"><span data-stu-id="e5535-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="e5535-111">Vadovaudamiesi toliau pateiktais veiksmais nustatykite ir tvarkykite mokėjimo tiekėjui užlaikymo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="e5535-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="e5535-112">Eikite į **Projektų valdymas ir apskaita** > **Užlaikymas** > **Mokėjimo tiekėjui užlaikymo sąlygos**.</span><span class="sxs-lookup"><span data-stu-id="e5535-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="e5535-113">Pasirinkite **Nauja**, kad įtrauktumėte naują tiekėjo užlaikymo sąlygą.</span><span class="sxs-lookup"><span data-stu-id="e5535-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="e5535-114">Naujos sąlygos **Taisyklės ID** reikšmė įvedama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="e5535-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="e5535-115">Įveskite trumpą aprašymą lauke **Aprašymas**, „FastTab“ **Sąlygos** pasirinkite **Įtraukti eilutę** ir įveskite toliau pateiktas vertes:</span><span class="sxs-lookup"><span data-stu-id="e5535-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="e5535-116">**Pristatytų vienetų procentinė dalis** – įveskite sąlygoje naudojamą užbaigtumo procentinį dydį.</span><span class="sxs-lookup"><span data-stu-id="e5535-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="e5535-117">Sumos automatiškai užlaikomos tiekėjo SF, kol projekto užbaigtumo būsena netampa lygi jūsų nurodytam procentiniam dydžiui.</span><span class="sxs-lookup"><span data-stu-id="e5535-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="e5535-118">Pvz., jei įvedate 50,00, sumos užlaikomos, kol 50 procentų projekto nebūna baigta.</span><span class="sxs-lookup"><span data-stu-id="e5535-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="e5535-119">**Užlaikytina procentinė dalis** – įveskite tiekėjo SF sumos procentinę dalį, kuri bus užlaikyta.</span><span class="sxs-lookup"><span data-stu-id="e5535-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="e5535-120">Pvz., jei įvedate 10,00, užlaikoma 10 procentų tiekėjo SF sumos, kol nepasiekiamas projekto užbaigtumo procentinis dydis, nustatytas lauke **Pristatytų vienetų procentinė dalis**.</span><span class="sxs-lookup"><span data-stu-id="e5535-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="e5535-121">**Atiduodama procentinė dalis** – pasirinkite **Įtraukti eilutę** ir įveskite bet kurių anksčiau užlaikytų sumų procentinę dalį, kurią norite atiduoti esant pasirinktam projekto užbaigtumo lygiui.</span><span class="sxs-lookup"><span data-stu-id="e5535-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="e5535-122">Jei naudojate daugiau nei vieną skirtingų projekto užbaigtumo lygių etapą, įveskite atskirą kiekvienos užlaikymo taisyklės tiekėjo užlaikymo sąlygos eilutę.</span><span class="sxs-lookup"><span data-stu-id="e5535-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="e5535-123">Kiekvienoje eilutėje galima nurodyti vis kitą procentinę dalį, kurią norite užlaikyti ir kurią reikia atiduoti pasiekus kiekvieną sukurtą projekto užbaigtumo lygį.</span><span class="sxs-lookup"><span data-stu-id="e5535-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="e5535-124">Sukūrę užlaikymo sąlygas tiekėjui, galite jas taikyti bet kuriam šio tiekėjo projektui.</span><span class="sxs-lookup"><span data-stu-id="e5535-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="e5535-125">Tiekėjo užlaikymo sąlygų taikymas projektui</span><span class="sxs-lookup"><span data-stu-id="e5535-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="e5535-126">Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai** ir atidarykite projektą iš projektų sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="e5535-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="e5535-127">„FastTab“ konteineryje **Tiekėjo sutartys** pasirinkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="e5535-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="e5535-128">Lauke **Sąskaitos kodas** pasirinkite vieną iš toliau nurodytų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="e5535-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="e5535-129">**Lentelė** – tiekėjo užlaikymo sąlygos taikomos vienam tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="e5535-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="e5535-130">**Grupė** – tiekėjo užlaikymo sąlygos taikomos visiems tiekėjų grupės tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="e5535-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="e5535-131">**Visi** – tiekėjo užlaikymo sąlygos taikomos visiems tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="e5535-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="e5535-132">Lauke **Tiekėjas / tiekėjų grupė** pasirinkite tiekėją arba tiekėjų grupę, kuriam (-iai) taikomos tiekėjo užlaikymo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="e5535-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="e5535-133">Jei atlikdami ankstesnį veiksmą pasirinkote **Visi**, šio lauko naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="e5535-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="e5535-134">Lauke **Tiekėjo užlaikymo sąlygos** pasirinkite užlaikymo sąlygas, kurias sukūrėte ankstesnėje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="e5535-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="e5535-135">Jei projekte tiekėjui taip pat nustatytos sąlygos „mokėti sumokėjus“ (PWP), lauke **PWP ribinės vertės procentinis dydis** įveskite projekto ribinės vertės procentinį dydį.</span><span class="sxs-lookup"><span data-stu-id="e5535-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="e5535-136">Tiekėjo užlaikymo sąlygos taip pat rodomos pirkimo užsakymuose, kuriuos sukuriate tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="e5535-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
