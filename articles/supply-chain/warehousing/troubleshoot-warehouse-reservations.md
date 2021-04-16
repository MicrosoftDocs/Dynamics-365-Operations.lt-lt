---
title: Sandėlio valdymo rezervacijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828111"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="0a3db-103">Sandėlio valdymo rezervacijų trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="0a3db-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a3db-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0a3db-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0a3db-105">Informaciją temomis apie paketo ir serijos numerių registracijas rasite [Sandėlio paketo ir serijos rezervacijų hierarchijos trikčių diagnostika](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="0a3db-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="0a3db-106">Gaunu tolesnį klaidos pranešimą: „Rezervacijų negalima panaikinti dėl to, kad sukurtas darbas remiasi rezervacijomis.“</span><span class="sxs-lookup"><span data-stu-id="0a3db-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0a3db-107">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="0a3db-107">Issue description</span></span>

<span data-ttu-id="0a3db-108">Negalite atrezrervuoti inventoriaus pardavimo eilutėje, nes eilutei yra atvertas darbas.</span><span class="sxs-lookup"><span data-stu-id="0a3db-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0a3db-109">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="0a3db-109">Issue resolution</span></span>

<span data-ttu-id="0a3db-110">Nustatykite, ar atviro pakavimo grupės darbas yra skirtas siekiant perkelti prekę iš pakavimo stoties į kitą stotį (tokią kaip *Baydoor*).</span><span class="sxs-lookup"><span data-stu-id="0a3db-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="0a3db-111">Peržiūrėkite įrašus **Darbo sukūrimo istorijos žurnale** ir **Išsamios darbo informacijos** puslapiuose siekiant nustatyti, kas fiziškai rezervuoja inventorių ir tada užbaikite bei panaikinkite darbą siekiant atlaisvinti rezervaciją.</span><span class="sxs-lookup"><span data-stu-id="0a3db-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="0a3db-112">Gaunu tolesnį klaidos pranešimą: „Inventoriaus kiekis -%1 negali būti atnaujintas dėl nepakankamų inventoriaus perlaidų prekei %2...."</span><span class="sxs-lookup"><span data-stu-id="0a3db-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0a3db-113">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="0a3db-113">Issue description</span></span>

<span data-ttu-id="0a3db-114">Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis.</span><span class="sxs-lookup"><span data-stu-id="0a3db-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="0a3db-115">Štai visas klaidos pranešimo tekstas:</span><span class="sxs-lookup"><span data-stu-id="0a3db-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="0a3db-116">Inventoriaus kiekis -%1 negali būti naujinamas dėl nepakankamų inventoriaus perlaidų prekei %2 su matmenimis Dydis=%3, Spalva=%4, Prieda=%5, Saitas=%6, Sandėlis=%7, Vieta=%8, Inventoriaus būsena=Prieinamas, Licensijos plokštelė=%9, Palaido kiekio numeris=%10 ataskaitos ID %11 partijos ID %12.</span><span class="sxs-lookup"><span data-stu-id="0a3db-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0a3db-117">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="0a3db-117">Issue resolution</span></span>

<span data-ttu-id="0a3db-118">Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį.</span><span class="sxs-lookup"><span data-stu-id="0a3db-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="0a3db-119">Pavyzdžiui, šios perlaidos gali atverti kiekio užsakymus, inventoriaus blokavimo įrašus ar išvesties užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0a3db-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="0a3db-120">Gaunu tolesnį klaidos pranešimą: „Fiziškai turima...negalima rezervuoti dėl to, kad tik 0,00 yra prieinama inventoriuje."</span><span class="sxs-lookup"><span data-stu-id="0a3db-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0a3db-121">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="0a3db-121">Issue description</span></span>

<span data-ttu-id="0a3db-122">Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis.</span><span class="sxs-lookup"><span data-stu-id="0a3db-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="0a3db-123">Štai visas klaidos pranešimo tekstas:</span><span class="sxs-lookup"><span data-stu-id="0a3db-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="0a3db-124">Fiziškai turima Saitas=%1, Sandėlis=%2, Inventoriaus būsena=Prieinama, Palaido kiekio numeris=%3, Savininkas=%4: %5 negalima rezervuoti, nes tik 0.00 yra prieinama inventoriuje.</span><span class="sxs-lookup"><span data-stu-id="0a3db-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0a3db-125">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="0a3db-125">Issue resolution</span></span>

<span data-ttu-id="0a3db-126">Šią klaidą greičiausiai sukelia atviras darbas.</span><span class="sxs-lookup"><span data-stu-id="0a3db-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="0a3db-127">Pabaikite darbą arba gaukite nesukūrę darbo.</span><span class="sxs-lookup"><span data-stu-id="0a3db-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="0a3db-128">Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį.</span><span class="sxs-lookup"><span data-stu-id="0a3db-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="0a3db-129">Pavyzdžiui, šios perlaidos gali būti atviri kiekio užsakymai, inventoriaus blokavimo įrašai ar išvesties užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0a3db-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
