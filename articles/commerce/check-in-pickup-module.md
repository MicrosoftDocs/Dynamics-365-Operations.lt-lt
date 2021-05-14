---
title: Registravimasis paėmimo moduliui
description: Ši tema paaiškina prisiregistravimo paėmimui modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937604"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="e0219-103">Registravimasis paėmimo moduliui</span><span class="sxs-lookup"><span data-stu-id="e0219-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e0219-104">Ši tema paaiškina prisiregistravimo paėmimui modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e0219-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e0219-105">Įsiregistravimo paėmimo modulyje pateikiamas patvirtinimo puslapis klientams, kurie naudoja klientų įsiregistravimo galimybę „Dynamics 365 Commerce“ pranešti parduotuvei apie atvykimą.</span><span class="sxs-lookup"><span data-stu-id="e0219-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="e0219-106">Įregistravimas paėmimo moduliui taip pat leidžia konfigūruoti formą, kuri renka papildomą klientų informaciją ir palengvina užsakymo pristatymą.</span><span class="sxs-lookup"><span data-stu-id="e0219-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="e0219-107">Ši informacija apima kliento automobilio stovėjimo vietos numerį, jų transporto priemonės gamintojas ir modelis.</span><span class="sxs-lookup"><span data-stu-id="e0219-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="e0219-108">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="e0219-108">Module properties</span></span>

| <span data-ttu-id="e0219-109">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="e0219-109">Property name</span></span> | <span data-ttu-id="e0219-110">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="e0219-110">Values</span></span> | <span data-ttu-id="e0219-111">Aprašas</span><span class="sxs-lookup"><span data-stu-id="e0219-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e0219-112">Patvirtinimo tekstas</span><span class="sxs-lookup"><span data-stu-id="e0219-112">Confirmation text</span></span> | <span data-ttu-id="e0219-113">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="e0219-113">Text string</span></span> | <span data-ttu-id="e0219-114">Antraštės turinys, rodomas įregistravimo patvirtinimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e0219-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="e0219-115">Rodyti QR kodą</span><span class="sxs-lookup"><span data-stu-id="e0219-115">Show QR code</span></span> | <span data-ttu-id="e0219-116">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="e0219-116">**True** or **False**</span></span> | <span data-ttu-id="e0219-117">Kai ši ypatybė nustatyta kaip **Teisinga**, įregistravimo patvirtinimo puslapyje rodomas QR kodas, nurodantis užsakymo patvirtinimo ID.</span><span class="sxs-lookup"><span data-stu-id="e0219-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="e0219-118">Papildomos informacijos antraštė</span><span class="sxs-lookup"><span data-stu-id="e0219-118">Additional information heading</span></span> | <span data-ttu-id="e0219-119">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="e0219-119">Text string</span></span> | <span data-ttu-id="e0219-120">Antraštės turinys, rodomas sukonfigūrus papildomos informacijos laukus.</span><span class="sxs-lookup"><span data-stu-id="e0219-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="e0219-121">Papildomos informacijos raktai</span><span class="sxs-lookup"><span data-stu-id="e0219-121">Additional information keys</span></span> | <span data-ttu-id="e0219-122">Išteklių ID / išteklių reikšmės pora</span><span class="sxs-lookup"><span data-stu-id="e0219-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="e0219-123">Kiekvienas raktas sukuria formos lauką ir susietą žymę, naudojamus renkant papildomą klientų informaciją.</span><span class="sxs-lookup"><span data-stu-id="e0219-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="e0219-124">Papildomų informacijos raktų \> išteklių ID</span><span class="sxs-lookup"><span data-stu-id="e0219-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="e0219-125">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="e0219-125">Text string</span></span> | <span data-ttu-id="e0219-126">Kiekvienas informacijos raktas sukuria formos lauką ir susietą žymę, naudojamus renkant papildomą klientų informaciją.</span><span class="sxs-lookup"><span data-stu-id="e0219-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="e0219-127">Ši ypatybė nurodo papildomos informacijos raktą.</span><span class="sxs-lookup"><span data-stu-id="e0219-127">This property identifies the additional information key.</span></span> <span data-ttu-id="e0219-128">Sukūrus užduotį kasos punkte (EKA), šios ypatybės vertė rodoma kaip etiketė instrukcijų lauke.</span><span class="sxs-lookup"><span data-stu-id="e0219-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="e0219-129">Papildomų informacijos raktų \> išteklių vertė</span><span class="sxs-lookup"><span data-stu-id="e0219-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="e0219-130">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="e0219-130">Text string</span></span> | <span data-ttu-id="e0219-131">EKA užduoties teksto lauko žymė.</span><span class="sxs-lookup"><span data-stu-id="e0219-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="e0219-132">Papildomų informacijos raktų \> būtini</span><span class="sxs-lookup"><span data-stu-id="e0219-132">Additional information keys \> Required</span></span> | <span data-ttu-id="e0219-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="e0219-133">**True** or **False**</span></span> | <span data-ttu-id="e0219-134">Ši ypatybė nurodo, ar klientai turi užpildyti formos lauką, kad galėtų tęsti.</span><span class="sxs-lookup"><span data-stu-id="e0219-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="e0219-135">Kai ši ypatybė nustatyta kaip Teisinga, žvaigždutė atvaizduota šalia formos žymos, o atliktas nulinis patikrinimas, siekiant neleisti klientams tęsti, jei neįvedami **jokia** vertė.</span><span class="sxs-lookup"><span data-stu-id="e0219-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="e0219-136">Įtraukti paėmimo modulio įregistravimą į puslapį</span><span class="sxs-lookup"><span data-stu-id="e0219-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="e0219-137">Paėmimo modulio registravimas turi būti pridėtas prie naujo puslapio, kurį sukuriate patvirtinti registravimas.</span><span class="sxs-lookup"><span data-stu-id="e0219-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="e0219-138">Šis puslapis bus naudojamas kaip klientų, kurie pasirenka mano čia esantį saitą ar mygtuką savo el. **laiške**, įregistravimo patvirtinimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="e0219-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="e0219-139">Konfigūruoti papildomos informacijos formą</span><span class="sxs-lookup"><span data-stu-id="e0219-139">Configure the additional information form</span></span>

<span data-ttu-id="e0219-140">Pagal numatytuosius nustatymus, jei nėra sukonfigūruotų papildomų informacijos raktų, modulis rodo klientams įregistravimo patvirtinimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="e0219-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="e0219-141">Kai rodomas įregistravimo patvirtinimas, EKA sukuriama parduotuvės, kurioje išrinktas užsakymas, užduotis.</span><span class="sxs-lookup"><span data-stu-id="e0219-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="e0219-142">Sukonfigūrus vieną ar daugiau papildomų informacijos raktų, klientai pirmiausia paraginamas įvesti informaciją.</span><span class="sxs-lookup"><span data-stu-id="e0219-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="e0219-143">Kai **pasirenkate** Pateikti, jiems rodomas įregistravimo patvirtinimas, o užduotis sukuriama EKA.</span><span class="sxs-lookup"><span data-stu-id="e0219-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e0219-144">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e0219-144">Additional resources</span></span>

[<span data-ttu-id="e0219-145">Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)</span><span class="sxs-lookup"><span data-stu-id="e0219-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
