---
title: Nuorodos į originalias sąskaitas kredito pranešimuose
description: Šioje temoje paaiškinta, kaip nustatyti ir spausdinti originalių sąskaitų numerius susijusiuose kredito pranešimuose.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d7f32c5d3d29be8d1d2742c4017c1719cbd47a8
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897337"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="a5ce7-103">Nuorodos į originalias sąskaitas kredito pranešimuose</span><span class="sxs-lookup"><span data-stu-id="a5ce7-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a5ce7-104">Kai kuriose šalyse ir regionuose yra teisinis reikalavimas, kad spausdinti kredito pranešimai apimtų nuorodas į originalias sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="a5ce7-105">Šioje temoje paaiškinta, kaip nustatyti ir spausdinti originalių sąskaitų numerius susijusiuose kredito pranešimuose.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a5ce7-106">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="a5ce7-106">Prerequisites</span></span>

- <span data-ttu-id="a5ce7-107">Darbo srityje **Funkcijų valdymas** įjunkite **Kredito sąskaitos išrašymo išdėstymas pardavimams ir projekto sąskaitos ataskaitoms** funkciją.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="a5ce7-108">Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a5ce7-108">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="a5ce7-109">Spausdintini reikiamų dokumentų formatai turi būti konfigūruojami spausdinimo valdyme.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="a5ce7-110">Šioje temoje aprašyta funkcija taikoma šiems dokumentams:</span><span class="sxs-lookup"><span data-stu-id="a5ce7-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="a5ce7-111">**Gautinos sumos**</span><span class="sxs-lookup"><span data-stu-id="a5ce7-111">**Accounts receivable**</span></span>

- <span data-ttu-id="a5ce7-112">Laisvos formos kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="a5ce7-112">Free text credit note</span></span>
- <span data-ttu-id="a5ce7-113">Kliento kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="a5ce7-113">Customer credit note</span></span>

<span data-ttu-id="a5ce7-114">**Projektų valdymas ir apskaita**</span><span class="sxs-lookup"><span data-stu-id="a5ce7-114">**Project management and accounting**</span></span>

- <span data-ttu-id="a5ce7-115">Projekto kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="a5ce7-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="a5ce7-116">Konfigūruoti gautinų sąskaitų parametrus</span><span class="sxs-lookup"><span data-stu-id="a5ce7-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="a5ce7-117">Atlikite šiuos žingsnius, kad nustatytumėte parametrą, kuris valdo, ar nuorodos į originalias sąskaitas yra spausdinamos susijusiose kredito pažymose.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="a5ce7-118">Eikite į **Gautinos sumos** \> **Nustatymai** \> **Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="a5ce7-119">Skirtuke **Naujiniai** „FastTab“ **Sąskaita** nustatykite **Taikyti kredito išrašymą sąskaitos išdėstymą į prekybos ir projekto sąskaitos ataskaitas** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Gautinų sąskaitų parametrų konfigūravimas](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="a5ce7-121">Nustatykite nuorodas į originalias sąskaitas</span><span class="sxs-lookup"><span data-stu-id="a5ce7-121">Define references to original invoices</span></span>

<span data-ttu-id="a5ce7-122">Naudokite tolesnes procedūras, kad nustatytumėte nuorodas į originalias sąskaitas pagal dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="a5ce7-123">Laisvos formos kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="a5ce7-123">Free text credit note</span></span>

1. <span data-ttu-id="a5ce7-124">Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="a5ce7-125">Kurkite naują kredito pažymą ar rinkitės esančią kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="a5ce7-126">Atidarykite sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-126">Open the invoice.</span></span>
4. <span data-ttu-id="a5ce7-127">Veiksmų juostoje **Sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Kredito sąskaitos išrašymas**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="a5ce7-128">Įveskite nuorodą į originalią sąskaitą ir rinkitės priežastį taisymui.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Nustatykite nuorodą laisvo teksto sąskaitai](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="a5ce7-130">Kliento kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="a5ce7-130">Customer credit note</span></span>

1. <span data-ttu-id="a5ce7-131">Eikite į **Gautinos sąskaitos** \> **Užsakymai** \> **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="a5ce7-132">Rinkitės ir atverkite išrašytą pardavimo užsakymą, kuris turi būti pataisytas.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="a5ce7-133">Veiksmų juostoje **Parduoti** skirtuke, **kredito pažyma** grupėje, rinkitės **Kredito pažyma**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="a5ce7-134">Įveskite taisymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-134">Enter the reason for the correction.</span></span> <span data-ttu-id="a5ce7-135">Nuoroda į originalią sąskaitą sukuriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-135">The reference to the original invoice is automatically established.</span></span>

![Nuorodos nustatymas prekybos užsakymui](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="a5ce7-137">Projekto kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="a5ce7-137">Project credit note</span></span>

1. <span data-ttu-id="a5ce7-138">Eikite į **Projekto valdymas ir apskaita** \> **Projekto sąskaitos** \> **Projekto sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="a5ce7-139">Rinkitės ir atverkite projekto sąskaitą, kuri turi būti pataisyta.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="a5ce7-140">Veiksmų juostoje **Projekto sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Rinktis kredito pažymą**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="a5ce7-141">Rinkitės **Kredito sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="a5ce7-142">Įveskite taisymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-142">Enter the reason for the correction.</span></span> <span data-ttu-id="a5ce7-143">Nuoroda į originalią sąskaitą sukuriama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-143">The reference to the original invoice is automatically established.</span></span>

![Nustatykite nuorodą laisvo projekto sąskaitai](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="a5ce7-145">Kredito pažymų spausdinimas</span><span class="sxs-lookup"><span data-stu-id="a5ce7-145">Printing credit notes</span></span>

<span data-ttu-id="a5ce7-146">Spausdindami laisvą tekstą, klientą ir projekto kredito pažymą, jis apims nuorodą į originalią sąskaitą ir taisymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Atspausdinta kredito pažyma](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="a5ce7-148">Įsitikinkite, kad spausdinami dokumentų formatai yra tinkamai sukonfigūruoti remiantis prielaida, kad nuorodos į originalias sąskaitas bus atspausdintos.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]