---
title: Gaunamų dokumentų analizė JSON formatu
description: Šioje temoje paaiškinama, kaip nustatyti elektroninių ataskaitų (ERŲ) formatus, kad būtų išanalizuoti gaunami dokumentai „JavaScript Object Notation“ (JSON) formatu.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b4ed81bb5527ea8e02caaa1262a57960dd7cdf29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685768"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="e4254-103">Gaunamų dokumentų analizė JSON formatu</span><span class="sxs-lookup"><span data-stu-id="e4254-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e4254-104">Galite sukurti elektroninių ataskaitų (ER) formatus ir išanalizuoti gaunamus elektroninius dokumentus, kuriuose yra duomenų teksto formatu „JavaScript“ pagrindu (kitaip tariant, failų „JavaScript Object Notation“ \[JSON\] formatu).</span><span class="sxs-lookup"><span data-stu-id="e4254-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="e4254-105">Norėdami apie šią funkciją sužinoti daugiau, atsisiųskite toliau pateiktoje lentelėje nurodytus failus ir paleiskite ER užduočių vedlį Formato konfigūracijos kūrimas importuojant duomenis iš išorinio JSON failo.</span><span class="sxs-lookup"><span data-stu-id="e4254-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="e4254-106">Šiame užduočių vedlyje nurodoma, kaip naudojantis ER formatu išanalizuoti gaunamą JSON failą, kad būtų galima atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="e4254-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="e4254-107">Pareigos</span><span class="sxs-lookup"><span data-stu-id="e4254-107">Title</span></span>                                  | <span data-ttu-id="e4254-108">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="e4254-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="e4254-109">ER formato konfigūracija</span><span class="sxs-lookup"><span data-stu-id="e4254-109">ER format configuration</span></span>                | [<span data-ttu-id="e4254-110">Tiekėjų failo trans_JSON.xml importavimo formatas</span><span class="sxs-lookup"><span data-stu-id="e4254-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="e4254-111">Gaunamo failo .csv formatu pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e4254-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="e4254-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="e4254-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="e4254-113">Reikalavimai</span><span class="sxs-lookup"><span data-stu-id="e4254-113">Requirements</span></span>

<span data-ttu-id="e4254-114">Norint atlikti ER užduočių vedlio Formato konfigūracijos kūrimas importuojant duomenis iš išorinio JSON failo veiksmus, turi būti laikomasi toliau nurodyto reikalavimo.</span><span class="sxs-lookup"><span data-stu-id="e4254-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="e4254-115">Pirminiai JSON failo elementai gali būti tik objekto elementai.</span><span class="sxs-lookup"><span data-stu-id="e4254-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="e4254-116">Įdėtieji objekto elementai turėtų būti ypatybių elementai, kad būtų sukuriama tinkama JSON struktūra.</span><span class="sxs-lookup"><span data-stu-id="e4254-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="e4254-117">JSON masyvai gali būti tik įdėtieji objekto ypatybių elementų elementai.</span><span class="sxs-lookup"><span data-stu-id="e4254-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="e4254-118">JSON masyvus gali sudaryti tik JSON objektai.</span><span class="sxs-lookup"><span data-stu-id="e4254-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="e4254-119">Juose negali būti tiesioginių eilučių / skaitinių verčių ir įdėtųjų masyvų.</span><span class="sxs-lookup"><span data-stu-id="e4254-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="e4254-120">Šių masyvų elementai išanalizuojami formate nurodyta tvarka.</span><span class="sxs-lookup"><span data-stu-id="e4254-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="e4254-121">Atsižvelgiama į kiekvieno JSON objekto daugialypumo nuostatas.</span><span class="sxs-lookup"><span data-stu-id="e4254-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="e4254-122">Be to, turite užbaigti užduočių vedlį [ER reikiamų konfigūracijų kūrimas, norint importuoti duomenis iš išorinio failo](tasks/er-required-configurations-import-data.md), jei jo dar neužbaigėte.</span><span class="sxs-lookup"><span data-stu-id="e4254-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="e4254-123">Atsisiųskite toliau nurodytą failą norėdami užbaigti užduočių vedlį.</span><span class="sxs-lookup"><span data-stu-id="e4254-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="e4254-124">Pareigos</span><span class="sxs-lookup"><span data-stu-id="e4254-124">Title</span></span>                  | <span data-ttu-id="e4254-125">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="e4254-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="e4254-126">ER modelio konfigūracija</span><span class="sxs-lookup"><span data-stu-id="e4254-126">ER model configuration</span></span> | [<span data-ttu-id="e4254-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="e4254-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
