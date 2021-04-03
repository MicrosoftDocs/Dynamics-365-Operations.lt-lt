---
title: Nebenaudokite konfigūracijų RCS visuotinėje saugykloje
description: Šioje temoje aprašoma, kaip nutraukti konfigūracijų naudojimą RCS visuotinėje saugykloje.
author: JaneA07
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 35d0af91161d898b09557a83913019609c71e836
ms.sourcegitcommit: e9d19f25e64cf4d1c1d07c8031a7081454a6f79e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2021
ms.locfileid: "5474253"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="cc6c4-103">Nebenaudokite konfigūracijų RCS visuotinėje saugykloje</span><span class="sxs-lookup"><span data-stu-id="cc6c4-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc6c4-104">Šioje temoje aprašoma, kaip nutraukti konfigūracijos naudojimą RCS visuotinėje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="cc6c4-105">Anksčiau buvo galima panaikinti tik tas konfigūracijas, kurių nebereikia.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="cc6c4-106">Tačiau dabar išleistą konfigūraciją galima pažymėti kaip **Nebenaudojamą** RCS visuotinėje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="cc6c4-107">Naudojant šią funkciją taip pat galima atlikti nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="cc6c4-108">Pateikite išankstinius pranešimus, kai konfigūracijos planuojama nebenaudoti.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="cc6c4-109">Įtraukite taikomą informaciją apie pakeitimo konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="cc6c4-110">Konkrečiai konfigūracijai datą nustatykite kaip **Palaikoma iki**, kad praneštumėte naudotojui, jog ji nebebus tęsiama.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="cc6c4-111">Kai nebenaudosite konfigūracijos versijos, galėsite nurodyti toliau nurodytą pasirenkamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="cc6c4-112">**Pakaitinė konfigūracija**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="cc6c4-113">**Pakeitimo konfigūracijos versija**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="cc6c4-114">**Laisvos formos pastaba**: šį laukelį naudokite dokumentacijos saitams ar nuorodoms pateikti</span><span class="sxs-lookup"><span data-stu-id="cc6c4-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="cc6c4-115">**Palaikoma iki**: šiame laukelyje pateikiama siūloma data, iki kurios bus palaikoma dabartinė konfigūracija / versija.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="cc6c4-116">Šią datą reikia atnaujinti neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="cc6c4-117">Jei norite nutraukti konfigūravimą, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="cc6c4-118">Pasirinkite, ar norite nutraukti vienos ar visų versijų, kurių vienos operacijos parametrai tokie patys, naudojimą, parinktį **Visos versijos** nustatydami kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="cc6c4-119">Parametrą **Nebenaudoti** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="cc6c4-120">Pasirinkite **Gerai**, jei konfigūracijų naudoti nebenorite.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="cc6c4-121">Laukelis **Nebenaudojimo data** pasirodys išsaugojus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Konfigūracijos informacijos nebenaudojimas](media/Discontinue-details-2.png)
  
<span data-ttu-id="cc6c4-123">Konfigūraciją galima vėl pakeisti į **Bendrinama** arba bet kuriuo metu sureguliuoti nebenaudojimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="cc6c4-124">Jei bendrinate konfigūraciją, nurodykite datą **Palaikoma iki** ir visą kitą informaciją, susijusią su nebenaudojimu, kad nurodytumėte savo planus tolesniam nebenaudojimui.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="cc6c4-125">Jei norite bendrinti informaciją apie planuojamą nebenaudojimą, prieš nutraukdamas konfigūravimą, naudotojas gali iš anksto užpildyti visus laukelius, susijusius su pakeitimu, tačiau parametrą **Nebenaudoti** turi nustatyti kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc6c4-126">Nebenaudojimas neriboja operacijų su konfigūracijomis.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="cc6c4-127">Galite toliau importuoti, vykdyti arba išvesti konfigūracijas. Šie laukeliai pateikiami tik informacijos tikslais.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="cc6c4-128">Finansų srityje šios informacijos rodymas palaikomas, pradedant 10.0.14 versija</span><span class="sxs-lookup"><span data-stu-id="cc6c4-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="cc6c4-129">Pradedant nuo 10.0.14 versijos, „Dynamics 365 Finance“ palaiko nebenaudojimo informacijos rodymą.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="cc6c4-130">Puslapyje **Visuotinė saugykla** galima peržiūrėti naujausią su nebenaudojimu susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="cc6c4-131">Numatyta, kad nebenaudojamos konfigūracijos bus išfiltruojamos.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="cc6c4-132">Puslapyje **Importuotos konfigūracijos** („ERSolutionTable“) rodomos konfigūracijos, kurios jau nebebuvo naudojamos jas importavus.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="cc6c4-133">Toms konfigūracijoms, kurios buvo nebenaudojamos po importavimo, nebenaudojimo informaciją galima sinchronizuoti vykdant užduotį **Konfigūracijų atnaujinimų importavimas**.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


