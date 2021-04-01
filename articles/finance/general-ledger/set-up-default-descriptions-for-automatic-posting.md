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
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5955b796cbc7917eb5500b96c879d1b0819d2edc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204863"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="f97a2-104">Numatytųjų aprašų registruojant automatiškai nustatymas</span><span class="sxs-lookup"><span data-stu-id="f97a2-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f97a2-105">Šioje temoje paaiškinta, kaip nustatyti numatytąjį tekstą, naudojamą aprašyti apskaitos įrašams, automatiškai registruojamiems didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="f97a2-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="f97a2-106">Galite nustatyti numatytąjį aprašo tekstą naudodami laisvos formos tekstą arba pasirinkdami fiksuotus kintamuosius.</span><span class="sxs-lookup"><span data-stu-id="f97a2-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="f97a2-107">Atlikdami kai kurių tipų operacijas arba tam tikrose šalyse ar regionuose taip pat galite įtraukti tekstą iš laukų „Microsoft Dynamics AX“ duomenų bazėje, susietų su šių tipų operacijomis.</span><span class="sxs-lookup"><span data-stu-id="f97a2-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="f97a2-108">Operacijos tipų bei šalių ir regionų sąrašą žr. skyriuje [Pasirinktinai: kito teksto įtraukimas į numatytuosius aprašus](#optional-add-other-text-to-default-descriptions), esančiame toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="f97a2-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="f97a2-109">Numatytųjų aprašų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f97a2-109">Set up default descriptions</span></span>

1. <span data-ttu-id="f97a2-110">Eikite į **Organizacijos administravimas** \> **Sąranka** \> **Numatytieji aprašai**.</span><span class="sxs-lookup"><span data-stu-id="f97a2-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="f97a2-111">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f97a2-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="f97a2-112">Lauke **Aprašas** pasirinkite operacijos tipą, kuriam bus kuriamas numatytasis aprašas.</span><span class="sxs-lookup"><span data-stu-id="f97a2-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="f97a2-113">Lauke **Kalba** pasirinkite kalbą, kuriai taikomas šis aprašas.</span><span class="sxs-lookup"><span data-stu-id="f97a2-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="f97a2-114">Lauke **Tekstas** įveskite numatytąjį aprašą.</span><span class="sxs-lookup"><span data-stu-id="f97a2-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="f97a2-115">Tekstą galite įvesti lauke arba galite naudoti vieną arba kelis iš toliau nurodytų laisvos formos teksto kintamųjų:</span><span class="sxs-lookup"><span data-stu-id="f97a2-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="f97a2-116">**%1** – Pridėti operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="f97a2-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="f97a2-117">**%2** – Pridėti identifikatorių, kuris atitinka dokumento tipą, kuris yra registruojamas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="f97a2-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="f97a2-118">Pvz., naudojant su SF susijusius operacijų tipus, kintamasis **%2** įtraukia SF numerį.</span><span class="sxs-lookup"><span data-stu-id="f97a2-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="f97a2-119">**%3** – Pridėti identifikatorių, susijusį su dokumento tipu, kuris yra registruojamas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="f97a2-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="f97a2-120">Pvz., naudojant su SF susijusius operacijų tipus, kintamasis **%3** įtraukia kliento sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="f97a2-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="f97a2-121">Pasirinktinai: kito teksto įtraukimas į numatytuosius aprašus</span><span class="sxs-lookup"><span data-stu-id="f97a2-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="f97a2-122">Atlikdami tam tikrų tipų operacijas tam tikrose šalyse ar regionuose, į numatytuosius aprašus galite įtraukti tekstą, gautą iš su šiais operacijų tipais susijusių laukų duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="f97a2-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="f97a2-123">Toliau pateiktame sąraše nurodyti operacijų tipai bei šalys ir regionai, kuriems taikoma ši galimybė.</span><span class="sxs-lookup"><span data-stu-id="f97a2-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="f97a2-124">**Operacijų tipai**</span><span class="sxs-lookup"><span data-stu-id="f97a2-124">**Transaction types**</span></span>

<span data-ttu-id="f97a2-125">Atlikdami operacijas, kurių tipai susiję su šiais dokumentų tipais, į numatytuosius aprašus galite įtraukti kitą tekstą:</span><span class="sxs-lookup"><span data-stu-id="f97a2-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="f97a2-126">Kliento SF</span><span class="sxs-lookup"><span data-stu-id="f97a2-126">Customer invoices</span></span>
- <span data-ttu-id="f97a2-127">Kliento kredito pažymos</span><span class="sxs-lookup"><span data-stu-id="f97a2-127">Customer credit notes</span></span>
- <span data-ttu-id="f97a2-128">Kliento mokėjimai grynaisiais</span><span class="sxs-lookup"><span data-stu-id="f97a2-128">Customer cash payments</span></span>
- <span data-ttu-id="f97a2-129">Tiekėjo mokėjimai</span><span class="sxs-lookup"><span data-stu-id="f97a2-129">Vendor payments</span></span>
- <span data-ttu-id="f97a2-130">Pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f97a2-130">Sales orders</span></span>
- <span data-ttu-id="f97a2-131">Pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f97a2-131">Purchase orders</span></span>
- <span data-ttu-id="f97a2-132">Atsargų žurnalai</span><span class="sxs-lookup"><span data-stu-id="f97a2-132">Inventory journals</span></span>
- <span data-ttu-id="f97a2-133">Bendrasis planavimas (MRP)</span><span class="sxs-lookup"><span data-stu-id="f97a2-133">Master planning (MRP)</span></span>
- <span data-ttu-id="f97a2-134">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="f97a2-134">Fixed assets</span></span>

<span data-ttu-id="f97a2-135">**Šalys ir regionai**</span><span class="sxs-lookup"><span data-stu-id="f97a2-135">**Countries and regions**</span></span>

<span data-ttu-id="f97a2-136">Ši parinktis galima šiose šalyse ir regionuose:</span><span class="sxs-lookup"><span data-stu-id="f97a2-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="f97a2-137">Brazilija</span><span class="sxs-lookup"><span data-stu-id="f97a2-137">Brazil</span></span>
- <span data-ttu-id="f97a2-138">Kinija</span><span class="sxs-lookup"><span data-stu-id="f97a2-138">China</span></span>
- <span data-ttu-id="f97a2-139">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="f97a2-139">Czech Republic</span></span>
- <span data-ttu-id="f97a2-140">Rytų Europa</span><span class="sxs-lookup"><span data-stu-id="f97a2-140">Eastern Europe</span></span>
- <span data-ttu-id="f97a2-141">Vengrija</span><span class="sxs-lookup"><span data-stu-id="f97a2-141">Hungary</span></span>
- <span data-ttu-id="f97a2-142">Indija</span><span class="sxs-lookup"><span data-stu-id="f97a2-142">India</span></span>
- <span data-ttu-id="f97a2-143">Japonija</span><span class="sxs-lookup"><span data-stu-id="f97a2-143">Japan</span></span>
- <span data-ttu-id="f97a2-144">Lietuva</span><span class="sxs-lookup"><span data-stu-id="f97a2-144">Lithuania</span></span>
- <span data-ttu-id="f97a2-145">Latvija</span><span class="sxs-lookup"><span data-stu-id="f97a2-145">Latvia</span></span>
- <span data-ttu-id="f97a2-146">Lenkija</span><span class="sxs-lookup"><span data-stu-id="f97a2-146">Poland</span></span>
- <span data-ttu-id="f97a2-147">Rusija</span><span class="sxs-lookup"><span data-stu-id="f97a2-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="f97a2-148">Teksto įtraukimas į numatytuosius aprašus</span><span class="sxs-lookup"><span data-stu-id="f97a2-148">Add text to default descriptions</span></span>

<span data-ttu-id="f97a2-149">Atlikę veiksmus, nurodytus [Numatytųjų aprašų nustatymas](#set-up-default-descriptions) prieš tai šioje temoje, įtraukite į numatytuosius aprašus kitą tekstą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="f97a2-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="f97a2-150">„FastTab“ **Parametrai** pasirinkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="f97a2-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="f97a2-151">Lauke **Nuorodų lentelė** pasirinkite duomenų bazės lentelę, iš kurios norite įtraukti parametro duomenis į aprašą.</span><span class="sxs-lookup"><span data-stu-id="f97a2-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="f97a2-152">Lauke **Nuorodos laukas** pasirinkite lauką, iš kurio norite įtraukti parametro duomenis į aprašą.</span><span class="sxs-lookup"><span data-stu-id="f97a2-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="f97a2-153">Norėdami pridėti daugiau parametrų, kartokite 1–3 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f97a2-153">Repeat steps 1 through 3 to add more parameters.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]