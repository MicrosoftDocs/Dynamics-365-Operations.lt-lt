---
title: Numeracijų nustatymas naudojant vediklį
description: Šioje temoje paaiškinta, kaip naudojant vedlį tuo pačiu metu nustatyti visas reikalingas numeracijas.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b79924e2c8d94b5e5e160a123e9b0cde0971fd96
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560488"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="36351-103">Numeracijų nustatymas naudojant vediklį</span><span class="sxs-lookup"><span data-stu-id="36351-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36351-104">Numerių sekos naudojamos generuojant perskaitomus, unikalius identifikatorius bendrųjų duomenų įrašams ir operacijų įrašams, kuriems jie reikalingi.</span><span class="sxs-lookup"><span data-stu-id="36351-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="36351-105">Pagrindinių duomenų arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas nuoroda.</span><span class="sxs-lookup"><span data-stu-id="36351-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="36351-106">Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda.</span><span class="sxs-lookup"><span data-stu-id="36351-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="36351-107">Šioje temoje paaiškinta, kaip naudojant vedlį tuo pačiu metu nustatyti visas reikalingas numeracijas.</span><span class="sxs-lookup"><span data-stu-id="36351-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="36351-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="36351-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="36351-109">Eikite į **Naršymo sritis > Moduliai > Organizacijos administravimas > Numeracijos > Numeracijos**.</span><span class="sxs-lookup"><span data-stu-id="36351-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="36351-110">Pasirinkite **Generuoti**.</span><span class="sxs-lookup"><span data-stu-id="36351-110">Select **Generate**.</span></span>
3. <span data-ttu-id="36351-111">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="36351-111">Select **Next**.</span></span>

   - <span data-ttu-id="36351-112">Šiame puslapyje galite modifikuoti identifikavimo kodą, mažiausią reikšmę ir didžiausią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36351-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="36351-113">Be to, galite nurodyti, ar numeracija turi būti nuolatinė.</span><span class="sxs-lookup"><span data-stu-id="36351-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="36351-114">Jei turite iš anksto priskirti numerius numeracijai, nepažymėkite parinkties **Nuolatinė**.</span><span class="sxs-lookup"><span data-stu-id="36351-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="36351-115">Norėdami į numeracijos formatą įtraukti aprėpties segmentą, sąraše pasirinkite formatą ir pažymėkite **Įtraukti aprėptį į formatą**.</span><span class="sxs-lookup"><span data-stu-id="36351-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="36351-116">Norėdami iš numeracijos formato pašalinti aprėpties segmentą, sąraše pasirinkite formatą ir pažymėkite **Pašalinti aprėptį iš formato**.</span><span class="sxs-lookup"><span data-stu-id="36351-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="36351-117">Norėdami, kad numeracija nebūtų automatiškai generuojama, sąraše pasirinkite numeraciją ir pažymėkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="36351-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="36351-118">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="36351-118">Select **Next**.</span></span>
5. <span data-ttu-id="36351-119">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="36351-119">Select **Finish**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]