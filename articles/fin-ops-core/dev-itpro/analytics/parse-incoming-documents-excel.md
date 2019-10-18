---
title: Gaunamų dokumentų analizė „Excel“ formatu
description: Šioje temoje pateikiama informacija apie elektroninių ataskaitų (ER) formatų kūrimą, norint analizuoti gaunamų „Microsoft Excel“ failų turinį.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3f83271327df186d407516ff1a197800ffc8c78c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249361"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="16681-103">Gaunamų dokumentų analizė „Excel“ formatu</span><span class="sxs-lookup"><span data-stu-id="16681-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="16681-104">Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus analizuoti gaunamus „Microsoft Excel“ failus, kurie atitinka „Microsoft Excel“ darbaknygių duomenis (XLSX formato failus).</span><span class="sxs-lookup"><span data-stu-id="16681-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="16681-105">Tada galite naudoti šių failų turinį programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="16681-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="16681-106">Tai naudinga, jei:</span><span class="sxs-lookup"><span data-stu-id="16681-106">This is useful if you:</span></span>

- <span data-ttu-id="16681-107">Sukurkite naują modelį ir formatą ir patikrinkite juos vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="16681-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="16681-108">Tokiu atveju, „Excel“ imituoja faktinius programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="16681-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="16681-109">Tvarkykite duomenis už savo programos ribų programoje „Excel“ ir importavę šiuos duomenis pateikite konkrečią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="16681-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="16681-110">Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlius **ER importavimo duomenys iš „Microsoft Excel“ failo (1 dalis: formato kūrimas)** ir **ER importavimo duomenys iš „Microsoft Excel“ failo (2 dalis: duomenų importavimas)** (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalys).</span><span class="sxs-lookup"><span data-stu-id="16681-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="16681-111">Šie užduočių vedliai parodys jums, kaip galima analizuoti gaunamą „Excel“ failą naudojant ER formatą, skirtą importuoti informaciją iš gaunamų dokumentų ir atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="16681-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="16681-112">Užduočių vedlių failus galite atsisiųsti iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="16681-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="16681-113">Atsisiųskite šiuos failus norėdami užbaigti aukščiau minėtus užduočių vedlius:</span><span class="sxs-lookup"><span data-stu-id="16681-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="16681-114">Turinio aprašas</span><span class="sxs-lookup"><span data-stu-id="16681-114">Content description</span></span>                         | <span data-ttu-id="16681-115">Failas</span><span class="sxs-lookup"><span data-stu-id="16681-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="16681-116">Gaunamas failas XLSX formatu – šablonas</span><span class="sxs-lookup"><span data-stu-id="16681-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="16681-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="16681-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="16681-118">Gaunamas failas XLSX formatu – duomenų pavyzdys</span><span class="sxs-lookup"><span data-stu-id="16681-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="16681-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="16681-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="16681-120">Jei dar neleidote šio užduoties vedlio, [ER reikiamų konfigūracijų kūrimas norint importuoti duomenis iš išorinio failo](./tasks/er-required-configurations-import-data.md) dabartinėje „Finance and Operations“ programoje, atsisiųskite šį failą.</span><span class="sxs-lookup"><span data-stu-id="16681-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="16681-121">Turinio aprašas</span><span class="sxs-lookup"><span data-stu-id="16681-121">Content description</span></span>    | <span data-ttu-id="16681-122">Failas</span><span class="sxs-lookup"><span data-stu-id="16681-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="16681-123">ER modelio konfigūracija</span><span class="sxs-lookup"><span data-stu-id="16681-123">ER model configuration</span></span> | [<span data-ttu-id="16681-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="16681-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
