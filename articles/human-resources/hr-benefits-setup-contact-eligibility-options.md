---
title: Asmeninių kontaktų tinkamumo parinkčių konfigūravimas
description: Asmeninių kontaktų tinkamumo parinkčių konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“. Asmeniniai kontaktai gali būti gavėjai arba priklausomieji.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009961"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="1c6a3-104">Asmeninių kontaktų tinkamumo parinkčių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1c6a3-104">Configure personal contact eligibility options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1c6a3-105">Šiame straipsnyje paaiškinama, kaip konfigūruoti asmeninių kontaktų tipus, siekiant gauti išmokas programoje „Microsoft Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1c6a3-106">Asmeniniai kontaktai gali būti gavėjai arba priklausomieji.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="1c6a3-107">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Asmeninių kontaktų tinkamumo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="1c6a3-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-108">Select **New**.</span></span>

3. <span data-ttu-id="1c6a3-109">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="1c6a3-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1c6a3-110">Laukas</span><span class="sxs-lookup"><span data-stu-id="1c6a3-110">Field</span></span> | <span data-ttu-id="1c6a3-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1c6a3-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1c6a3-112">**Tinkamumo parinktis**</span><span class="sxs-lookup"><span data-stu-id="1c6a3-112">**Eligibility option**</span></span> | <span data-ttu-id="1c6a3-113">Unikalus tinkamumo parinkties pavadinimas arba kodas, skirtas nustatyti tinkamumo parinktį.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="1c6a3-114">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="1c6a3-114">**Description**</span></span> | <span data-ttu-id="1c6a3-115">Trumpas tinkamumo parinkties aprašas.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="1c6a3-116">**Kontakto tinkamumo kodas**</span><span class="sxs-lookup"><span data-stu-id="1c6a3-116">**Contact eligibility code**</span></span> | <span data-ttu-id="1c6a3-117">Sistemos kodas, kuris geriausiai apibūdina asmens tinkamumo parinktį.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="1c6a3-118">Galite rinkti iš:</span><span class="sxs-lookup"><span data-stu-id="1c6a3-118">You can choose from:</span></span> <ul><li><span data-ttu-id="1c6a3-119">Ryšys</span><span class="sxs-lookup"><span data-stu-id="1c6a3-119">Relationship</span></span></li><li><span data-ttu-id="1c6a3-120">Studentas</span><span class="sxs-lookup"><span data-stu-id="1c6a3-120">Student</span></span></li><li><span data-ttu-id="1c6a3-121">Vyresnis priklausomasis</span><span class="sxs-lookup"><span data-stu-id="1c6a3-121">Overage dependent</span></span></li><li><span data-ttu-id="1c6a3-122">Vyresnio amžiaus neįgalus priklausomasis</span><span class="sxs-lookup"><span data-stu-id="1c6a3-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="1c6a3-123">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="1c6a3-123">**Status**</span></span> | <span data-ttu-id="1c6a3-124">Tinkamumo parinkties būsena.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-124">The status of the eligibility option.</span></span> <span data-ttu-id="1c6a3-125">Jei tinkamumo parinkties būsena nustatyta kaip neaktyvi, negalėsite pasirinkti šio asmeninio kontakto tinkamumo parinkties, skirtos asmeniniams kontaktams.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="1c6a3-126">**Ryšys**</span><span class="sxs-lookup"><span data-stu-id="1c6a3-126">**Relationship**</span></span> | <span data-ttu-id="1c6a3-127">Nurodo ryšį tarp asmeninio kontakto ir darbuotojo.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="1c6a3-128">Šis laukas aktyvus tik tada, kai kontakto tinkamumo kodas nustatytas kaip „Ryšys“.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="1c6a3-129">**Amžius**</span><span class="sxs-lookup"><span data-stu-id="1c6a3-129">**Age**</span></span> | <span data-ttu-id="1c6a3-130">Maksimalus terminas, per kurį asmeninis kontaktas turi teisę gauti išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="1c6a3-131">Šis laukas aktyvus tik tada, kai pasirenkate ryšį.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="1c6a3-132">Šis terminas lyginamas su apskaičiuotu asmeninio kontakto terminu.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="1c6a3-133">Apskaičiuotas terminas yra: (padengimo data – asmeninio kontakto gimimo data / 365).</span><span class="sxs-lookup"><span data-stu-id="1c6a3-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="1c6a3-134">Šis skaičius visada yra sveikasis skaičius.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="1c6a3-135">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1c6a3-135">Select **Save**.</span></span> 
