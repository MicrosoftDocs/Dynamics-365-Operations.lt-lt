---
title: Numatytųjų aprašų registruojant automatiškai nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti numatytąjį tekstą, naudojamą aprašyti apskaitos įrašams, automatiškai registruojamiems didžiojoje knygoje. Galite nustatyti numatytąjį aprašo tekstą naudodami laisvos formos tekstą arba pasirinkdami fiksuotus kintamuosius.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117366"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="0cd91-104">Numatytųjų aprašų registruojant automatiškai nustatymas</span><span class="sxs-lookup"><span data-stu-id="0cd91-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cd91-105">Šioje temoje paaiškinta, kaip nustatyti numatytąjį tekstą, naudojamą aprašyti apskaitos įrašams, automatiškai registruojamiems didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="0cd91-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="0cd91-106">Galite nustatyti numatytąjį aprašo tekstą naudodami laisvos formos tekstą arba pasirinkdami fiksuotus kintamuosius.</span><span class="sxs-lookup"><span data-stu-id="0cd91-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="0cd91-107">Atlikdami kai kurių tipų operacijas arba tam tikrose šalyse ar regionuose taip pat galite įtraukti tekstą iš laukų „Microsoft Dynamics AX“ duomenų bazėje, susietų su šių tipų operacijomis.</span><span class="sxs-lookup"><span data-stu-id="0cd91-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="0cd91-108">Operacijos tipų bei šalių ir regionų sąrašą žr. skyriuje [Pasirinktinai: kito teksto įtraukimas į numatytuosius aprašus](#optional-add-other-text-to-default-descriptions), esančiame toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="0cd91-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="0cd91-109">Numatytųjų aprašų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0cd91-109">Set up default descriptions</span></span>

1. <span data-ttu-id="0cd91-110">Eikite į **Organizacijos administravimas** \> **Sąranka** \> **Numatytieji aprašai**.</span><span class="sxs-lookup"><span data-stu-id="0cd91-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="0cd91-111">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0cd91-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="0cd91-112">Lauke **Aprašas** pasirinkite operacijos tipą, kuriam bus kuriamas numatytasis aprašas.</span><span class="sxs-lookup"><span data-stu-id="0cd91-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="0cd91-113">Lauke **Kalba** pasirinkite kalbą, kuriai taikomas šis aprašas.</span><span class="sxs-lookup"><span data-stu-id="0cd91-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="0cd91-114">Lauke **Tekstas** įveskite numatytąjį aprašą.</span><span class="sxs-lookup"><span data-stu-id="0cd91-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="0cd91-115">Tekstą galite įvesti lauke arba galite naudoti vieną arba kelis iš toliau nurodytų laisvos formos teksto kintamųjų:</span><span class="sxs-lookup"><span data-stu-id="0cd91-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="0cd91-116">**%1** – Pridėti operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="0cd91-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="0cd91-117">**%2** – Pridėti identifikatorių, kuris atitinka dokumento tipą, kuris yra registruojamas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="0cd91-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="0cd91-118">Pvz., naudojant su SF susijusius operacijų tipus, kintamasis **%2** įtraukia SF numerį.</span><span class="sxs-lookup"><span data-stu-id="0cd91-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="0cd91-119">**%3** – Pridėti identifikatorių, susijusį su dokumento tipu, kuris yra registruojamas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="0cd91-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="0cd91-120">Pvz., naudojant su SF susijusius operacijų tipus, kintamasis **%3** įtraukia kliento sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="0cd91-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="0cd91-121">Pasirinktinai: kito teksto įtraukimas į numatytuosius aprašus</span><span class="sxs-lookup"><span data-stu-id="0cd91-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="0cd91-122">Atlikdami tam tikrų tipų operacijas tam tikrose šalyse ar regionuose, į numatytuosius aprašus galite įtraukti tekstą, gautą iš su šiais operacijų tipais susijusių laukų duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="0cd91-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="0cd91-123">Toliau pateiktame sąraše nurodyti operacijų tipai bei šalys ir regionai, kuriems taikoma ši galimybė.</span><span class="sxs-lookup"><span data-stu-id="0cd91-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="0cd91-124">**Operacijų tipai**</span><span class="sxs-lookup"><span data-stu-id="0cd91-124">**Transaction types**</span></span>

<span data-ttu-id="0cd91-125">Atlikdami operacijas, kurių tipai susiję su šiais dokumentų tipais, į numatytuosius aprašus galite įtraukti kitą tekstą:</span><span class="sxs-lookup"><span data-stu-id="0cd91-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="0cd91-126">Kliento SF</span><span class="sxs-lookup"><span data-stu-id="0cd91-126">Customer invoices</span></span>
- <span data-ttu-id="0cd91-127">Kliento kredito pažymos</span><span class="sxs-lookup"><span data-stu-id="0cd91-127">Customer credit notes</span></span>
- <span data-ttu-id="0cd91-128">Kliento mokėjimai grynaisiais</span><span class="sxs-lookup"><span data-stu-id="0cd91-128">Customer cash payments</span></span>
- <span data-ttu-id="0cd91-129">Tiekėjo mokėjimai</span><span class="sxs-lookup"><span data-stu-id="0cd91-129">Vendor payments</span></span>
- <span data-ttu-id="0cd91-130">Pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="0cd91-130">Sales orders</span></span>
- <span data-ttu-id="0cd91-131">Pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="0cd91-131">Purchase orders</span></span>
- <span data-ttu-id="0cd91-132">Atsargų žurnalai</span><span class="sxs-lookup"><span data-stu-id="0cd91-132">Inventory journals</span></span>
- <span data-ttu-id="0cd91-133">Bendrasis planavimas (MRP)</span><span class="sxs-lookup"><span data-stu-id="0cd91-133">Master planning (MRP)</span></span>
- <span data-ttu-id="0cd91-134">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="0cd91-134">Fixed assets</span></span>

<span data-ttu-id="0cd91-135">**Šalys ir regionai**</span><span class="sxs-lookup"><span data-stu-id="0cd91-135">**Countries and regions**</span></span>

<span data-ttu-id="0cd91-136">Ši parinktis galima šiose šalyse ir regionuose:</span><span class="sxs-lookup"><span data-stu-id="0cd91-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="0cd91-137">Brazilija</span><span class="sxs-lookup"><span data-stu-id="0cd91-137">Brazil</span></span>
- <span data-ttu-id="0cd91-138">Kinija</span><span class="sxs-lookup"><span data-stu-id="0cd91-138">China</span></span>
- <span data-ttu-id="0cd91-139">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="0cd91-139">Czech Republic</span></span>
- <span data-ttu-id="0cd91-140">Rytų Europa</span><span class="sxs-lookup"><span data-stu-id="0cd91-140">Eastern Europe</span></span>
- <span data-ttu-id="0cd91-141">Vengrija</span><span class="sxs-lookup"><span data-stu-id="0cd91-141">Hungary</span></span>
- <span data-ttu-id="0cd91-142">Indija</span><span class="sxs-lookup"><span data-stu-id="0cd91-142">India</span></span>
- <span data-ttu-id="0cd91-143">Japonija</span><span class="sxs-lookup"><span data-stu-id="0cd91-143">Japan</span></span>
- <span data-ttu-id="0cd91-144">Lietuva</span><span class="sxs-lookup"><span data-stu-id="0cd91-144">Lithuania</span></span>
- <span data-ttu-id="0cd91-145">Latvija</span><span class="sxs-lookup"><span data-stu-id="0cd91-145">Latvia</span></span>
- <span data-ttu-id="0cd91-146">Lenkija</span><span class="sxs-lookup"><span data-stu-id="0cd91-146">Poland</span></span>
- <span data-ttu-id="0cd91-147">Rusija</span><span class="sxs-lookup"><span data-stu-id="0cd91-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="0cd91-148">Teksto įtraukimas į numatytuosius aprašus</span><span class="sxs-lookup"><span data-stu-id="0cd91-148">Add text to default descriptions</span></span>

<span data-ttu-id="0cd91-149">Atlikę veiksmus, nurodytus [Numatytųjų aprašų nustatymas](#set-up-default-descriptions) prieš tai šioje temoje, įtraukite į numatytuosius aprašus kitą tekstą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="0cd91-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="0cd91-150">„FastTab“ **Parametrai** pasirinkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="0cd91-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="0cd91-151">Lauke **Nuorodų lentelė** pasirinkite duomenų bazės lentelę, iš kurios norite įtraukti parametro duomenis į aprašą.</span><span class="sxs-lookup"><span data-stu-id="0cd91-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="0cd91-152">Lauke **Nuorodos laukas** pasirinkite lauką, iš kurio norite įtraukti parametro duomenis į aprašą.</span><span class="sxs-lookup"><span data-stu-id="0cd91-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="0cd91-153">Norėdami pridėti daugiau parametrų, kartokite 1–3 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0cd91-153">Repeat steps 1 through 3 to add more parameters.</span></span>
