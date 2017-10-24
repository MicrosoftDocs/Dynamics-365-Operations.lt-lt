---
title: "Seniausio paketo paėmimas mobiliajame įrenginyje"
description: "Šioje temoje aprašoma, kaip nustatyti ir taikyti seniausio paketo paėmimo parinktis iš mobiliojo įrenginio."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="78262-103">Seniausio paketo paėmimas mobiliajame įrenginyje</span><span class="sxs-lookup"><span data-stu-id="78262-103">Pick oldest batch on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="78262-104">Konfigūraciją **Paimti seniausią paketą** galite pasiekti per mobiliojo įrenginio meniu, ir jis leidžia priversti sandėlio darbininkus paimti seniausią paketą jų dabartinėje vietoje arba juos apie tai įspėti.</span><span class="sxs-lookup"><span data-stu-id="78262-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="78262-105">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="78262-105">Where it applies</span></span>
<span data-ttu-id="78262-106">Parinktis Paimti seniausią paketą sukonfigūruota mobiliojo įrenginio meniu elementuose ir turi įtakos toliau nurodytiems paketo paėmimo elementams.</span><span class="sxs-lookup"><span data-stu-id="78262-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="78262-107">Kaip nustatyti konfigūraciją Paimti seniausią paketą</span><span class="sxs-lookup"><span data-stu-id="78262-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="78262-108">Prekėms, kurioms yra nustatyta naudoti esamą darbą, parinktis **Paimti seniausią paketą** mobiliojo įrenginio meniu gali būti nustatyta kaip **Nėra**, **Įspėti**, arba **Priversti**.</span><span class="sxs-lookup"><span data-stu-id="78262-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="78262-109">**Nėra**: darbininkai negaus jokių pranešimų ir galės paimti bet kurį paketą savo vietoje.</span><span class="sxs-lookup"><span data-stu-id="78262-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="78262-110">**Įspėti** ir **Priversti**: darbininkui pasirinkus paketą, virš paketo valdiklio bus rodomas (-i) paketas (-ai) su seniausia galiojimo data</span><span class="sxs-lookup"><span data-stu-id="78262-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="78262-111">Jei vietos numerio lentelės kontroliuojamos, virš numerio lentelių valdiklio bus rodomas numerio lentelių, kuriose yra seniausias paketas, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="78262-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="78262-112">**Įspėti**: jei darbininkas pasirenka numerio lentelę arba paketą, kuris nėra rodomas sąraše, valdiklis ištuštėja ir rodomas įspėjimas, jog yra senesnis paketas, kurį galima pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="78262-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="78262-113">Kad būtų leidžiama tęsti darbą, darbuotojas gali dar kartą pasirinkti tą pačią numerio lentelę arba paketą.</span><span class="sxs-lookup"><span data-stu-id="78262-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="78262-114">**Priversti**: darbininkai ir toliau gaus pranešimą, kad yra senesnis paketas, kurį reikia paimti.</span><span class="sxs-lookup"><span data-stu-id="78262-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

