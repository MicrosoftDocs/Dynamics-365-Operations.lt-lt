---
title: "Pažangaus banko suderinimo MT940 importavimas – Sudėtinis duomenų objekto atnaujinimas"
description: "Į banko išrašo importavimo objektą reikia įtraukti eilės numerį, kad būtų palaikomas MT940 formatas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0fb86cd4264d5420c479e14f7eed41e480c88b63
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="21b8e-103">Pažangaus banko suderinimo MT940 importavimas – Sudėtinis duomenų objekto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="21b8e-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="21b8e-104">Į banko išrašo importavimo objektą reikia įtraukti eilės numerį, kad būtų palaikomas MT940 formatas.</span><span class="sxs-lookup"><span data-stu-id="21b8e-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="21b8e-105">Norėdami įtraukti banko išrašo importavimo objektą, kad būtų palaikomas MT940 formatas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21b8e-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="21b8e-106">Kompiliuokite ir sinchronizuokite šiuos objektus:</span><span class="sxs-lookup"><span data-stu-id="21b8e-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="21b8e-107">Sudėtinis objektas\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="21b8e-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="21b8e-108">Objektas\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="21b8e-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="21b8e-109">Objektas\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="21b8e-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="21b8e-110">Objektas\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="21b8e-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="21b8e-111">Objektas\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="21b8e-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="21b8e-112">Lentelės\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="21b8e-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="21b8e-113">Duomenų valdymas\\duomenų projektai.</span><span class="sxs-lookup"><span data-stu-id="21b8e-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="21b8e-114">Įkelkite MT940 importavimo projektą(-us)</span><span class="sxs-lookup"><span data-stu-id="21b8e-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="21b8e-115">Pakeiskite XSLT.</span><span class="sxs-lookup"><span data-stu-id="21b8e-115">Change XSLT.</span></span>
            -   <span data-ttu-id="21b8e-116">Spustelėkite **Peržiūrėti schemą**.</span><span class="sxs-lookup"><span data-stu-id="21b8e-116">Click **View map**.</span></span>
            -   <span data-ttu-id="21b8e-117">Banko išrašo dokumente spustelėkite **Peržiūrėti schema**.</span><span class="sxs-lookup"><span data-stu-id="21b8e-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="21b8e-118">Spustelėkite **Pakeitimai**</span><span class="sxs-lookup"><span data-stu-id="21b8e-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="21b8e-119">Panaikinkite failą BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="21b8e-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="21b8e-120">Pridėkite naują BankReconiliation-to-Composite.xsl versiją.</span><span class="sxs-lookup"><span data-stu-id="21b8e-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="21b8e-121">Makete **Šaltinio duomenys** rodykite **Eilės numeris**.</span><span class="sxs-lookup"><span data-stu-id="21b8e-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="21b8e-122">Šaltinio duomenų formatas = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="21b8e-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="21b8e-123">Objekto pavadinimas = Banko išrašai.</span><span class="sxs-lookup"><span data-stu-id="21b8e-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="21b8e-124">Nusiuntimo duomenų failas = nauja SampleBankCompositeEntity.xml versija.</span><span class="sxs-lookup"><span data-stu-id="21b8e-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="21b8e-125">Jei norite perrašyti esamą failą, spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="21b8e-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="21b8e-126">Jeigu norite sugeneruoti naują susiejimą, spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="21b8e-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="21b8e-127">Patikrinkite, ar susietas E**ilės numeris**.</span><span class="sxs-lookup"><span data-stu-id="21b8e-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="21b8e-128">Išrašo objekte spustelėkite **Peržiūrėti schema**.</span><span class="sxs-lookup"><span data-stu-id="21b8e-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="21b8e-129">Patikrinkite, ar objektas **SequenceNumber** susietas nuo šaltinio iki išdėstymo.</span><span class="sxs-lookup"><span data-stu-id="21b8e-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="21b8e-130">Importuokite naują išrašą.</span><span class="sxs-lookup"><span data-stu-id="21b8e-130">Import the new statement.</span></span>




