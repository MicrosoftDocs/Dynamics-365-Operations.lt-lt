--- 
title: "Nustatyti ISO20022 kredito pervedimo mokėjimo būdą"
description: "Šioje procedūroje parodoma, kaip nustatyti tiekėjo mokėjimo būdą, skirtą atlikti ISO20022 kredito pervedimą arba kito tipo mokėjimą, naudojant elektronines ataskaitas failui generuoti."
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
ms.openlocfilehash: bed51f8749dfa0264ad39f51f9ceb295ac46fe93
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="ea4d2-103">Nustatyti ISO20022 kredito pervedimo mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="ea4d2-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea4d2-104">Šioje procedūroje parodoma, kaip nustatyti tiekėjo mokėjimo būdą, skirtą atlikti ISO20022 kredito pervedimą arba kito tipo mokėjimą, naudojant elektronines ataskaitas failui generuoti.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="ea4d2-105">Prieš atlikdami šią užduotį, turite nustatyti eksporto formato konfigūracijas ir mokėjimo sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="ea4d2-106">Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="ea4d2-107">Tai yra trečioji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="ea4d2-108">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="ea4d2-109">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="ea4d2-110">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea4d2-111">Pvz., filtruokite lauką Mokėjimo būdas reikšme „SEPA CT“.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="ea4d2-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-112">Click Edit.</span></span>
4. <span data-ttu-id="ea4d2-113">Lauke Laikotarpis pasirinkite „Iš viso‟.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="ea4d2-114">Lauke Mokėjimo tipas pasirinkite „Elektroninis mokėjimas“.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="ea4d2-115">Išplėskite dalį Failo formatai.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="ea4d2-116">Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="ea4d2-117">Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="ea4d2-118">Sąraše pasirinkite reikšmę ISO20022 kredito pervedimas (DE).</span><span class="sxs-lookup"><span data-stu-id="ea4d2-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="ea4d2-119">Jei sąrašas yra tuščias, nėra importuotos ir aktyvios tiekėjo mokėjimų eksporto formato konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="ea4d2-120">Lauke Kliento sąskaita pasirinkite „Bankas‟.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="ea4d2-121">Lauke Mokėjimo sąskaita nurodykite reikšmes „DEMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="ea4d2-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ea4d2-122">Click Save.</span></span>


