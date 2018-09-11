--- 
title: "Į žurnalą įtraukti užregistruotus žurnalo įrašus"
description: "Šioje procedūroje parodoma, kaip į žurnalą įtraukti užregistruotus žurnalo įrašus."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 7936c5e99397eb635568fc6b754132541f957002
ms.contentlocale: lt-lt
ms.lasthandoff: 09/11/2018

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="a5397-103">Į žurnalą įtraukti užregistruotus žurnalo įrašus</span><span class="sxs-lookup"><span data-stu-id="a5397-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5397-104">Šioje procedūroje parodoma, kaip į žurnalą įtraukti užregistruotus žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="a5397-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="a5397-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="a5397-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="a5397-106">Patikrinkite įtraukimo į žurnalą parametrus dalyje DK > DK sąranka > DK parametrai.</span><span class="sxs-lookup"><span data-stu-id="a5397-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="a5397-107">Laukas Išplėstas DK žurnalas gali būti nustatytas į Taip arba Ne.</span><span class="sxs-lookup"><span data-stu-id="a5397-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="a5397-108">Jei nustatysite parametrą Taip, ataskaitos išvestis bus skirtinga.</span><span class="sxs-lookup"><span data-stu-id="a5397-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="a5397-109">Pasirinkite, ar laikotarpis gali būti uždarytas, jei įtraukimo į žurnalą procesas nebuvo paleistas.</span><span class="sxs-lookup"><span data-stu-id="a5397-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="a5397-110">Jei ši parinktis nustatyta į Taip, laikotarpio negalima uždaryti, kol įtraukimo į žurnalą procesas nebus baigtas.</span><span class="sxs-lookup"><span data-stu-id="a5397-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="a5397-111">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a5397-111">Close the page.</span></span>
5. <span data-ttu-id="a5397-112">Eikite į Didžioji knyga > Periodinės užduotys > Įtraukimas į žurnalą.</span><span class="sxs-lookup"><span data-stu-id="a5397-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="a5397-113">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="a5397-113">Click Filter.</span></span>
7. <span data-ttu-id="a5397-114">Paryškinkite eilutę su filtro kriterijais, kuriuos norite nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a5397-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="a5397-115">Lauke Kriterijai įveskite arba pasirinkite filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="a5397-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="a5397-116">Spustelėkite Gerai, kad uždarytumėte filtrų puslapį.</span><span class="sxs-lookup"><span data-stu-id="a5397-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="a5397-117">Spustelėkite Gerai, kad pradėtumėte įtraukimo į žurnalą procesą.</span><span class="sxs-lookup"><span data-stu-id="a5397-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="a5397-118">Kai procesas bus baigtas, bus sugeneruota ataskaita.</span><span class="sxs-lookup"><span data-stu-id="a5397-118">A report will be generated after the process is complete.</span></span>  


