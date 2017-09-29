--- 
title: "Importuoti ISO20022 kredito pervedimo konfigūraciją"
description: "Šioje procedūroje parodoma, kaip importuoti tiekėjo mokėjimų elektroninių ataskaitų konfigūraciją."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="97eec-103">Importuoti ISO20022 kredito pervedimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="97eec-103">Import ISO20022 credit transfer configuration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97eec-104">Šioje procedūroje parodoma, kaip importuoti tiekėjo mokėjimų elektroninių ataskaitų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="97eec-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="97eec-105">Vokietijos ISO 20022 kredito pervedimo formatas naudojamas kaip pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="97eec-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="97eec-106">Šią procedūrą galima taikyti ir kitam galimam elektroninių ataskaitų formatui.</span><span class="sxs-lookup"><span data-stu-id="97eec-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="97eec-107">Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, tačiau galite naudoti bet kokią demonstracinių duomenų įmonę šiai užduočiai atlikti.</span><span class="sxs-lookup"><span data-stu-id="97eec-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="97eec-108">Tai yra pirmoji iš penkių užduočių, kuriose bendrai aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="97eec-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="97eec-109">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="97eec-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="97eec-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="97eec-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="97eec-111">Galimų konfigūracijos teikėjų sąraše pasirinkite „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="97eec-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="97eec-112">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="97eec-112">Click Set active.</span></span>
4. <span data-ttu-id="97eec-113">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="97eec-113">Click Repositories.</span></span>
5. <span data-ttu-id="97eec-114">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="97eec-114">Click Open.</span></span>
6. <span data-ttu-id="97eec-115">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="97eec-115">Click Show filters.</span></span>
7. <span data-ttu-id="97eec-116">Taikykite šiuos filtrus: lauke Konfigūracijos pavadinimas įveskite filtro reikšmę ISO20022 kredito pervedimas (DE) naudodami filtro operatorių Prasideda.</span><span class="sxs-lookup"><span data-stu-id="97eec-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="97eec-117">Arba konfigūraciją raskite sąraše, ją pasirinkite ir tada perkelkite į importavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="97eec-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="97eec-118">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="97eec-118">Click Import.</span></span>
    * <span data-ttu-id="97eec-119">Jei mygtuko Importuoti naudoti negalima, tai reiškia, kad ši konfigūracija jau importuota.</span><span class="sxs-lookup"><span data-stu-id="97eec-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="97eec-120">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="97eec-120">Click Yes.</span></span>

