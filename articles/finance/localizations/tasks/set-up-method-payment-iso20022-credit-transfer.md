---
title: Nustatyti ISO20022 kredito pervedimo mokėjimo būdą
description: Šioje procedūroje parodoma, kaip nustatyti tiekėjo mokėjimo būdą, skirtą atlikti ISO20022 kredito pervedimą arba kito tipo mokėjimą, naudojant elektronines ataskaitas failui generuoti.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92bc314e69628f2a287ba7c9a7c2d3d73a0bfd33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988107"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="4bfb7-103">Nustatyti ISO20022 kredito pervedimo mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="4bfb7-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bfb7-104">Šioje procedūroje parodoma, kaip nustatyti tiekėjo mokėjimo būdą, skirtą atlikti ISO20022 kredito pervedimą arba kito tipo mokėjimą, naudojant elektronines ataskaitas failui generuoti.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="4bfb7-105">Prieš atlikdami šią užduotį, turite nustatyti eksporto formato konfigūracijas ir mokėjimo sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="4bfb7-106">Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="4bfb7-107">Tai yra trečioji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="4bfb7-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="4bfb7-109">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="4bfb7-110">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4bfb7-111">Pvz., filtruokite lauką Mokėjimo būdas reikšme „SEPA CT“.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="4bfb7-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-112">Click Edit.</span></span>
4. <span data-ttu-id="4bfb7-113">Lauke Laikotarpis pasirinkite „Iš viso‟.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="4bfb7-114">Lauke Mokėjimo tipas pasirinkite „Elektroninis mokėjimas“.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="4bfb7-115">Išplėskite dalį Failo formatai.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="4bfb7-116">Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="4bfb7-117">Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="4bfb7-118">Sąraše pasirinkite reikšmę ISO20022 kredito pervedimas (DE).</span><span class="sxs-lookup"><span data-stu-id="4bfb7-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="4bfb7-119">Jei sąrašas yra tuščias, nėra importuotos ir aktyvios tiekėjo mokėjimų eksporto formato konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="4bfb7-120">Lauke Kliento sąskaita pasirinkite „Bankas‟.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="4bfb7-121">Lauke Mokėjimo sąskaita nurodykite reikšmes „DEMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="4bfb7-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-122">Click Save.</span></span>

