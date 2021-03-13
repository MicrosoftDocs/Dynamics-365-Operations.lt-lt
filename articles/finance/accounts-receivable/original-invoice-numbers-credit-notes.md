---
title: Nuorodos į originalias sąskaitas kredito pranešimuose
description: Šioje temoje paaiškinta, kaip nustatyti ir spausdinti originalių sąskaitų numerius susijusiuose kredito pranešimuose.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2021
ms.locfileid: "5100007"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="26edb-103">Nuorodos į originalias sąskaitas kredito pranešimuose</span><span class="sxs-lookup"><span data-stu-id="26edb-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="26edb-104">Kai kuriose šalyse ir regionuose yra teisinsi reikalvimas, kad spausdinti kredito pranešimai apimtų nuorodas į originalias sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="26edb-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="26edb-105">Šioje temoje paaiškinta, kaip nustatyti ir spausdinti originalių sąskaitų numerius susijusiuose kredito pranešimuose.</span><span class="sxs-lookup"><span data-stu-id="26edb-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="26edb-106">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="26edb-106">Prerequisites</span></span>

- <span data-ttu-id="26edb-107">Darbo srtiyje **Funkcijų valdymas** įjunkite **Kredito sąskaitos išrašymo išdėstymas pardavimams ir projekto sąskaitos ataskaitoms** funkciją.</span><span class="sxs-lookup"><span data-stu-id="26edb-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="26edb-108">Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26edb-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="26edb-109">Spausdintinti reikiamų dokumentų formatai turi būti konfigūruojami spausdinimo valdyme.</span><span class="sxs-lookup"><span data-stu-id="26edb-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="26edb-110">Šioje temoje aprašyta funkcija taikoma šiems dokumentams:</span><span class="sxs-lookup"><span data-stu-id="26edb-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="26edb-111">**Gautinos sumos**</span><span class="sxs-lookup"><span data-stu-id="26edb-111">**Accounts receivable**</span></span>

- <span data-ttu-id="26edb-112">Laisvos formos kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="26edb-112">Free text credit note</span></span>
- <span data-ttu-id="26edb-113">Kliento kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="26edb-113">Customer credit note</span></span>

<span data-ttu-id="26edb-114">**Projektų valdymas ir apskaita**</span><span class="sxs-lookup"><span data-stu-id="26edb-114">**Project management and accounting**</span></span>

- <span data-ttu-id="26edb-115">Projekto kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="26edb-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="26edb-116">Konfigūruoti gautinų sąskaitų parametrus</span><span class="sxs-lookup"><span data-stu-id="26edb-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="26edb-117">Atlikite šiuos žingsnius, kad nustatytumėte parametrą, kuris valdo, ar nuorodos į originalias sąskaitas yra spausdinamos susijusiose kredito pažymose.</span><span class="sxs-lookup"><span data-stu-id="26edb-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="26edb-118">Eikite į **Gautinos sumos** \> **Nustatymai** \> **Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="26edb-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="26edb-119">Skirtuke **Naujiniai** „FastTab“ **Sąskaita** nustatykite **Taikyti kredito išrašymą sąskaitos išdėstymą į prekybos ir projekto sąskaitos ataskaitas** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="26edb-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Gautinų sąskaitų parametrų konfigūravimas](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="26edb-121">Nustatykite nuorodas į originalias sąskaitas</span><span class="sxs-lookup"><span data-stu-id="26edb-121">Define references to original invoices</span></span>

<span data-ttu-id="26edb-122">Naudokite tolesnes procedūras, kad nustatytumėte nuorodoas į originalias sąskaitas pagal dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="26edb-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="26edb-123">Laisvos formos kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="26edb-123">Free text credit note</span></span>

1. <span data-ttu-id="26edb-124">Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.</span><span class="sxs-lookup"><span data-stu-id="26edb-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="26edb-125">Kurkite naują kredito pažymą ar rinkitės esančią kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="26edb-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="26edb-126">Atidarykite sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="26edb-126">Open the invoice.</span></span>
4. <span data-ttu-id="26edb-127">Veiksmų juostoje **Sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Kredito sąskaitos išrašymas**.</span><span class="sxs-lookup"><span data-stu-id="26edb-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="26edb-128">Įveskite nuorodą į originalią sąskaitą ir rinkiės priežastį taisymui.</span><span class="sxs-lookup"><span data-stu-id="26edb-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Nustatykite nuorodą laisvo teksto sąskaitai](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="26edb-130">Kliento kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="26edb-130">Customer credit note</span></span>

1. <span data-ttu-id="26edb-131">Eikite į **Gautinos sąskaitos** \> **Užsakymai** \> **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="26edb-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="26edb-132">Rinkitės ir atverkite išrašytą pardavimo užsakymą, kuris turi būti pataisytas.</span><span class="sxs-lookup"><span data-stu-id="26edb-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="26edb-133">Veiksmų juostoje **Parduoti** skirtuke, **kredito pažyma** grupėje, rinkitės **Kredito pažyma**.</span><span class="sxs-lookup"><span data-stu-id="26edb-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="26edb-134">Įveskite taisymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="26edb-134">Enter the reason for the correction.</span></span> <span data-ttu-id="26edb-135">Nuoroda į orignalią sąskaitą sukuriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="26edb-135">The reference to the original invoice is automatically established.</span></span>

![Nuorodos nustatymas prekybos užsakymui](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="26edb-137">Projekto kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="26edb-137">Project credit note</span></span>

1. <span data-ttu-id="26edb-138">Eiktie į **Projekto valdymas ir apskaita** \> **Projekto sąskaitos** \> **Projekto sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="26edb-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="26edb-139">Rinkitės ir atverkite projekto sąskaitą, kuri turi būti pataisyta.</span><span class="sxs-lookup"><span data-stu-id="26edb-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="26edb-140">Veiksmų juostoje **Projekto sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Rinktis kredito pažymą**.</span><span class="sxs-lookup"><span data-stu-id="26edb-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="26edb-141">Rinkitės **Kredito sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="26edb-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="26edb-142">Įveskite taisymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="26edb-142">Enter the reason for the correction.</span></span> <span data-ttu-id="26edb-143">Nuoroda į orignalią sąskaitą sukuriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="26edb-143">The reference to the original invoice is automatically established.</span></span>

![Nustatykite nuorodą laisvo projekto sąskaitai](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="26edb-145">Kredito pažymų spausdinimas</span><span class="sxs-lookup"><span data-stu-id="26edb-145">Printing credit notes</span></span>

<span data-ttu-id="26edb-146">Spausdindami laisvą tekstą, klientą ir projekto kredito pažymą, jis apims nuorodą į originalią sąskaitą ir taisymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="26edb-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Atspausdinta kredito pažyma](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="26edb-148">Įsitikinkite, kad spausdinami dokumentų formatai yra tinkamai sukonfigūruoti remiantis prielaida, kad nuorodos į originalias sąskaitas bus atspausdintos.</span><span class="sxs-lookup"><span data-stu-id="26edb-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>
