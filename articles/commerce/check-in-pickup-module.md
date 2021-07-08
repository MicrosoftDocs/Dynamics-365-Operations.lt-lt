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
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270588"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="43b5a-103">Registravimasis paėmimo moduliui</span><span class="sxs-lookup"><span data-stu-id="43b5a-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="43b5a-104">Ši tema paaiškina prisiregistravimo paėmimui modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="43b5a-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="43b5a-105">Įsiregistravimo paėmimo modulyje pateikiamas patvirtinimo puslapis klientams, kurie naudoja klientų įsiregistravimo galimybę „Dynamics 365 Commerce“ pranešti parduotuvei apie atvykimą.</span><span class="sxs-lookup"><span data-stu-id="43b5a-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="43b5a-106">Įregistravimas paėmimo moduliui taip pat leidžia konfigūruoti formą, kuri renka papildomą klientų informaciją ir palengvina užsakymo pristatymą.</span><span class="sxs-lookup"><span data-stu-id="43b5a-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="43b5a-107">Ši informacija apima kliento automobilio stovėjimo vietos numerį, jų transporto priemonės gamintojas ir modelis.</span><span class="sxs-lookup"><span data-stu-id="43b5a-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="43b5a-108">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="43b5a-108">Module properties</span></span>

| <span data-ttu-id="43b5a-109">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="43b5a-109">Property name</span></span> | <span data-ttu-id="43b5a-110">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="43b5a-110">Values</span></span> | <span data-ttu-id="43b5a-111">Aprašas</span><span class="sxs-lookup"><span data-stu-id="43b5a-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="43b5a-112">Patvirtinimo tekstas</span><span class="sxs-lookup"><span data-stu-id="43b5a-112">Confirmation text</span></span> | <span data-ttu-id="43b5a-113">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="43b5a-113">Text string</span></span> | <span data-ttu-id="43b5a-114">Antraštės turinys, rodomas įregistravimo patvirtinimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="43b5a-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="43b5a-115">Rodyti QR kodą</span><span class="sxs-lookup"><span data-stu-id="43b5a-115">Show QR code</span></span> | <span data-ttu-id="43b5a-116">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="43b5a-116">**True** or **False**</span></span> | <span data-ttu-id="43b5a-117">Kai ši ypatybė nustatyta kaip **Teisinga**, įregistravimo patvirtinimo puslapyje rodomas QR kodas, nurodantis užsakymo patvirtinimo ID.</span><span class="sxs-lookup"><span data-stu-id="43b5a-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="43b5a-118">Papildomos informacijos antraštė</span><span class="sxs-lookup"><span data-stu-id="43b5a-118">Additional information heading</span></span> | <span data-ttu-id="43b5a-119">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="43b5a-119">Text string</span></span> | <span data-ttu-id="43b5a-120">Antraštės turinys, rodomas sukonfigūrus papildomos informacijos laukus.</span><span class="sxs-lookup"><span data-stu-id="43b5a-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="43b5a-121">Papildomos informacijos raktai</span><span class="sxs-lookup"><span data-stu-id="43b5a-121">Additional information keys</span></span> | <span data-ttu-id="43b5a-122">Išteklių ID / išteklių reikšmės pora</span><span class="sxs-lookup"><span data-stu-id="43b5a-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="43b5a-123">Kiekvienas raktas sukuria formos lauką ir susietą žymę, naudojamus renkant papildomą klientų informaciją.</span><span class="sxs-lookup"><span data-stu-id="43b5a-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="43b5a-124">Papildomų informacijos raktų \> išteklių ID</span><span class="sxs-lookup"><span data-stu-id="43b5a-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="43b5a-125">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="43b5a-125">Text string</span></span> | <span data-ttu-id="43b5a-126">Kiekvienas informacijos raktas sukuria formos lauką ir susietą žymę, naudojamus renkant papildomą klientų informaciją.</span><span class="sxs-lookup"><span data-stu-id="43b5a-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="43b5a-127">Ši ypatybė nurodo papildomos informacijos raktą.</span><span class="sxs-lookup"><span data-stu-id="43b5a-127">This property identifies the additional information key.</span></span> <span data-ttu-id="43b5a-128">Sukūrus užduotį kasos punkte (EKA), šios ypatybės vertė rodoma kaip etiketė instrukcijų lauke.</span><span class="sxs-lookup"><span data-stu-id="43b5a-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="43b5a-129">Papildomų informacijos raktų \> išteklių vertė</span><span class="sxs-lookup"><span data-stu-id="43b5a-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="43b5a-130">Teksto eilutė</span><span class="sxs-lookup"><span data-stu-id="43b5a-130">Text string</span></span> | <span data-ttu-id="43b5a-131">EKA užduoties teksto lauko žymė.</span><span class="sxs-lookup"><span data-stu-id="43b5a-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="43b5a-132">Papildomų informacijos raktų \> būtini</span><span class="sxs-lookup"><span data-stu-id="43b5a-132">Additional information keys \> Required</span></span> | <span data-ttu-id="43b5a-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="43b5a-133">**True** or **False**</span></span> | <span data-ttu-id="43b5a-134">Ši ypatybė nurodo, ar klientai turi užpildyti formos lauką, kad galėtų tęsti.</span><span class="sxs-lookup"><span data-stu-id="43b5a-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="43b5a-135">Kai ši ypatybė nustatyta kaip Teisinga, žvaigždutė atvaizduota šalia formos žymos, o atliktas nulinis patikrinimas, siekiant neleisti klientams tęsti, jei neįvedami **jokia** vertė.</span><span class="sxs-lookup"><span data-stu-id="43b5a-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="43b5a-136">Įtraukti paėmimo modulio įregistravimą į puslapį</span><span class="sxs-lookup"><span data-stu-id="43b5a-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="43b5a-137">Paėmimo modulio registravimas turi būti pridėtas prie naujo puslapio, kurį sukuriate patvirtinti registravimas.</span><span class="sxs-lookup"><span data-stu-id="43b5a-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="43b5a-138">Šis puslapis bus naudojamas kaip klientų, kurie pasirenka mano čia esantį saitą ar mygtuką savo el. **laiške**, įregistravimo patvirtinimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="43b5a-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="43b5a-139">Konfigūruoti papildomos informacijos formą</span><span class="sxs-lookup"><span data-stu-id="43b5a-139">Configure the additional information form</span></span>

<span data-ttu-id="43b5a-140">Pagal numatytuosius nustatymus, jei nėra sukonfigūruotų papildomų informacijos raktų, modulis rodo klientams įregistravimo patvirtinimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="43b5a-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="43b5a-141">Kai rodomas įregistravimo patvirtinimas, EKA sukuriama parduotuvės, kurioje išrinktas užsakymas, užduotis.</span><span class="sxs-lookup"><span data-stu-id="43b5a-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="43b5a-142">Sukonfigūrus vieną ar daugiau papildomų informacijos raktų, klientai pirmiausia paraginamas įvesti informaciją.</span><span class="sxs-lookup"><span data-stu-id="43b5a-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="43b5a-143">Kai **pasirenkate** Pateikti, jiems rodomas įregistravimo patvirtinimas, o užduotis sukuriama EKA.</span><span class="sxs-lookup"><span data-stu-id="43b5a-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="43b5a-144">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="43b5a-144">Additional resources</span></span>

[<span data-ttu-id="43b5a-145">Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)</span><span class="sxs-lookup"><span data-stu-id="43b5a-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
