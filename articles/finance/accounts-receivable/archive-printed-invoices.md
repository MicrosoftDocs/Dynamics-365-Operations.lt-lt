---
title: Archyvuoti atspausdintas klientų sąskaitas faktūras su maišos numeriais
description: Šioje temoje paaiškinama, kaip įgalinti archyvavimą, kad būtų galima saugoti išspausdintas kliento sąskaitas-faktūras su „hash“ numeriais.
author: ilyako
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d502ec5d286573c72e207419b66f283183009c09
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557485"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="144c9-103">Archyvuoti atspausdintas klientų sąskaitas faktūras su maišos numeriais</span><span class="sxs-lookup"><span data-stu-id="144c9-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="144c9-104">Kai kuriose šalyse nustatytas teisinis reikalavimas sistemoje laikyti apskaičiuotus „hash“ numerius kartu su kai kurių dokumentų spaudiniais.</span><span class="sxs-lookup"><span data-stu-id="144c9-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="144c9-105">„Hash“ numerius galima naudoti teikiant ataskaitas valdžios institucijoms ir audito metu.</span><span class="sxs-lookup"><span data-stu-id="144c9-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="144c9-106">Šioje temoje paaiškinama, kaip konfigūruoti archyvavimą, kad būtų galima saugoti išspausdintas kliento sąskaitas-faktūras su „hash“ numeriais.</span><span class="sxs-lookup"><span data-stu-id="144c9-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="144c9-107">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="144c9-107">Prerequisites</span></span>

- <span data-ttu-id="144c9-108">**Funkcijų valdymo** darbo srityje įjunkite funkciją **Archyvuoti išspausdintas kliento sąsaitas-faktūras su „hash“ numeriais.**</span><span class="sxs-lookup"><span data-stu-id="144c9-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="144c9-109">Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="144c9-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="144c9-110">Konfigūruokite spausdinamus reikiamų dokumentų formatus srityje **Spausdinimo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="144c9-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="144c9-111">Ši funkcija taikoma toliau pateiktiems dokumentams.</span><span class="sxs-lookup"><span data-stu-id="144c9-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="144c9-112">**Gautinos sumos**</span><span class="sxs-lookup"><span data-stu-id="144c9-112">**Accounts receivable**</span></span>
- <span data-ttu-id="144c9-113">Kliento SF</span><span class="sxs-lookup"><span data-stu-id="144c9-113">Customer invoice</span></span>
- <span data-ttu-id="144c9-114">Kliento kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="144c9-114">Customer credit note</span></span>
- <span data-ttu-id="144c9-115">Laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="144c9-115">Free text invoice</span></span>
- <span data-ttu-id="144c9-116">Laisvos formos kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="144c9-116">Free text credit note</span></span>

<span data-ttu-id="144c9-117">**Projektų valdymas ir apskaita**</span><span class="sxs-lookup"><span data-stu-id="144c9-117">**Project management and accounting**</span></span>
- <span data-ttu-id="144c9-118">Projekto SF</span><span class="sxs-lookup"><span data-stu-id="144c9-118">Project invoice</span></span>
- <span data-ttu-id="144c9-119">Projekto kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="144c9-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="144c9-120">Klientų bendrųjų duomenų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="144c9-120">Configure customer master data</span></span>
<span data-ttu-id="144c9-121">Norėdami konfigūruoti kliento duomenis ir įjungti galimybę automatiškai įrašyti išspausdintas sąskaitas-faktūras kaip priedus, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="144c9-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="144c9-122">Eikite į **Gautinos sumos** > **Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="144c9-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="144c9-123">Pasirinkite klientą ir „FastTab“ skirtuke **Sąskaita-faktūra ir pristatymas**, esančiame skiltyje **EL. SĄSKAITA-FAKTŪRA**, laukelyje **el. sąskaitos-faktūros priedas** paspauskite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="144c9-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="144c9-124">Spausdinti sąskaitą-faktūrą</span><span class="sxs-lookup"><span data-stu-id="144c9-124">Print invoices</span></span>
<span data-ttu-id="144c9-125">Galite registruoti ir spausdinti bet kokį laisvos formos tekstą ir projekto sąskaitą-faktūrą arba kredito pažymą klientui, kurį sukonfigūravote ankstesnėje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="144c9-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="144c9-126">Atidarykite puslapį **Priedai** išspausdintai sąskaitos-faktūrai.</span><span class="sxs-lookup"><span data-stu-id="144c9-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="144c9-127">„FastTab“ skirtuke **Priedas**, esančiame laukelių grupėje **Papildomi duomenys**, laukelyje **Dokumento „hash“ numeris**, raskite įrašytą „hash“ numerį, apskaičiuotą išspausdintai sąskaitai-faktūrai.</span><span class="sxs-lookup"><span data-stu-id="144c9-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Priedo „hash“ numeris](media/attach-hash-num.jpg)
