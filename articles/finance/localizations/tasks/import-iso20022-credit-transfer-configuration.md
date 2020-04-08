---
title: Importuoti ISO20022 kredito pervedimo konfigūraciją
description: Šioje procedūroje parodoma, kaip importuoti tiekėjo mokėjimų elektroninių ataskaitų konfigūraciją.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140046"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="e9d81-103">Importuoti ISO20022 kredito pervedimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="e9d81-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9d81-104">Šioje procedūroje parodoma, kaip importuoti tiekėjo mokėjimų elektroninių ataskaitų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="e9d81-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="e9d81-105">Vokietijos ISO 20022 kredito pervedimo formatas naudojamas kaip pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e9d81-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="e9d81-106">Šią procedūrą galima taikyti ir kitam galimam elektroninių ataskaitų formatui.</span><span class="sxs-lookup"><span data-stu-id="e9d81-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="e9d81-107">Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, tačiau galite naudoti bet kokią demonstracinių duomenų įmonę šiai užduočiai atlikti.</span><span class="sxs-lookup"><span data-stu-id="e9d81-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="e9d81-108">Tai yra pirmoji iš penkių užduočių, kuriose bendrai aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="e9d81-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="e9d81-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="e9d81-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="e9d81-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="e9d81-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e9d81-111">Galimų konfigūracijos teikėjų sąraše pasirinkite „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="e9d81-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="e9d81-112">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="e9d81-112">Click Set active.</span></span>
4. <span data-ttu-id="e9d81-113">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="e9d81-113">Click Repositories.</span></span>
5. <span data-ttu-id="e9d81-114">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="e9d81-114">Click Open.</span></span>
6. <span data-ttu-id="e9d81-115">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="e9d81-115">Click Show filters.</span></span>
7. <span data-ttu-id="e9d81-116">Taikykite šiuos filtrus: lauke Konfigūracijos pavadinimas įveskite filtro reikšmę ISO20022 kredito pervedimas (DE) naudodami filtro operatorių Prasideda.</span><span class="sxs-lookup"><span data-stu-id="e9d81-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="e9d81-117">Arba konfigūraciją raskite sąraše, ją pasirinkite ir tada perkelkite į importavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="e9d81-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="e9d81-118">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="e9d81-118">Click Import.</span></span>
    * <span data-ttu-id="e9d81-119">Jei mygtuko Importuoti naudoti negalima, tai reiškia, kad ši konfigūracija jau importuota.</span><span class="sxs-lookup"><span data-stu-id="e9d81-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="e9d81-120">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="e9d81-120">Click Yes.</span></span>

