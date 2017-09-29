--- 
title: "Nustatyti numeracijas naudojant vedlį"
description: "Numerių sekos naudojamos generuojant perskaitomus, unikalius identifikatorius bendrųjų duomenų įrašams ir operacijų įrašams, kuriems jie reikalingi."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96c1bc711350b447611977c3f2070fbc08fbae0f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="f2e9f-103">Nustatyti numeracijas naudojant vedlį</span><span class="sxs-lookup"><span data-stu-id="f2e9f-103">Set up number sequences by using a wizard</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2e9f-104">Numerių sekos naudojamos generuojant perskaitomus, unikalius identifikatorius bendrųjų duomenų įrašams ir operacijų įrašams, kuriems jie reikalingi.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="f2e9f-105">Pagrindinių duomenų arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas nuoroda.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="f2e9f-106">Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="f2e9f-107">Ši procedūra paaiškina, kaip vienu kartu nustatyti visas reikiamas numerių sekas naudojant vedlį.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="f2e9f-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f2e9f-109">Pasirinkite Organizacijos administravimas > Numeracijos > Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="f2e9f-110">Spustelėkite „Generuoti“.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-110">Click Generate.</span></span>
3. <span data-ttu-id="f2e9f-111">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-111">Click Next.</span></span>
    * <span data-ttu-id="f2e9f-112">Šiame puslapyje galite modifikuoti identifikavimo kodą, mažiausią reikšmę ir didžiausią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="f2e9f-113">Be to, galite nurodyti, ar numeracija turi būti nuolatinė.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="f2e9f-114">Nepasirinkite parinkties „Ištisinė“, jei turite iš anksto priskirti numerių sekos numerius.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="f2e9f-115">Norėdami įtraukti aprėpties segmentą į numerių sekos formatą, pasirinkite formatą sąraše, tada spustelėkite „Įtraukti aprėptį į formatą“.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="f2e9f-116">Norėdami pašalinti aprėpties segmentą iš numerių sekos formato, pasirinkite formatą sąraše, tada spustelėkite „Pašalinti aprėptį iš formato“.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="f2e9f-117">Norėdami neįtraukti numerių sekos į automatinį generavimą, pasirinkite numerių seką sąraše, tada spustelėkite „Ištrinti“.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="f2e9f-118">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-118">Click Next.</span></span>
5. <span data-ttu-id="f2e9f-119">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="f2e9f-119">Click Finish.</span></span>

