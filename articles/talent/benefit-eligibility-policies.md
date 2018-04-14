---
title: "Išmokos tinkamumo strategijos"
description: "Šiame straipsnyje pateikta informacija apie išmokos tinkamumo strategijas, kuri padės jums nustatyti, kas turi teisę gauti konkrečias išmokas."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 46dba3a61cf96b19b5bc4d2956d028bbbeaaa60e
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="b6e1a-103">Išmokos tinkamumo strategijos</span><span class="sxs-lookup"><span data-stu-id="b6e1a-103">Benefit eligibility policies</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="b6e1a-104">Šioje temoje pateikta informacija apie išmokos tinkamumo strategijas, kuri padės jums nustatyti, kas turi teisę gauti konkrečias išmokas.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="b6e1a-105">Kai kuriate išmokas, nusprendžiate, kurias išmokas gaus kurie darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="b6e1a-106">Toliau pateikiamoje lentelėje parodyt išmokų pavyzdžiai, kurias galite mokėti tam tikriems darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="b6e1a-107">Išmoka</span><span class="sxs-lookup"><span data-stu-id="b6e1a-107">Benefit</span></span>          | <span data-ttu-id="b6e1a-108">Kam mokama išmoka</span><span class="sxs-lookup"><span data-stu-id="b6e1a-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="b6e1a-109">Sveikatos draudimas</span><span class="sxs-lookup"><span data-stu-id="b6e1a-109">Health insurance</span></span> | <span data-ttu-id="b6e1a-110">Visi darbuotojai</span><span class="sxs-lookup"><span data-stu-id="b6e1a-110">All employees</span></span>                   |
| <span data-ttu-id="b6e1a-111">Mobilusis telefonas</span><span class="sxs-lookup"><span data-stu-id="b6e1a-111">Mobile phone</span></span>     | <span data-ttu-id="b6e1a-112">Pardavėjai, vadovai</span><span class="sxs-lookup"><span data-stu-id="b6e1a-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="b6e1a-113">Automobilių stovėjimo leidimai</span><span class="sxs-lookup"><span data-stu-id="b6e1a-113">Parking passes</span></span>   | <span data-ttu-id="b6e1a-114">Administracija</span><span class="sxs-lookup"><span data-stu-id="b6e1a-114">Executives</span></span>                      |

<span data-ttu-id="b6e1a-115">Toliau pateikti komponentai naudojami tinkamumo strategijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="b6e1a-116">Strategijos taisyklių tipai</span><span class="sxs-lookup"><span data-stu-id="b6e1a-116">Policy rule types</span></span>
-   <span data-ttu-id="b6e1a-117">Išmokos tinkamumo strategijos</span><span class="sxs-lookup"><span data-stu-id="b6e1a-117">Benefit eligibility policies</span></span>

<span data-ttu-id="b6e1a-118">Strategijos taisyklių tipai apibrėžia užklausų parametrus, kurie naudojami kuriant konkrečias strategijos taisykles.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="b6e1a-119">Sukūrę strategijos taisyklių tipus, galite sukurti išmokų tinkamumo strategijas.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="b6e1a-120">Strategijos leidžia sukurti taisyklių rinkinius, kurie taikomi vienam arba daugiau juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="b6e1a-121">Kiekvienoje strategijoje galite peržiūrėti bet kurį i, išmok. tinkamumo strategijos taisyklių tipų, kuriuos sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="b6e1a-122">Galite apibrėžti strategijos taisyklės apimtį.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="b6e1a-123">Pavyzdžiui, jei sukuriate išmokų tinkamumo strategijos taisyklių tipą, pavadintą **Vadovų**, galite nurodyti, kokia taisyklė atitinka šią strategiją.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="b6e1a-124">Šiame pavyzdyje taisyklė gali nurodyti, kad bet koks užduoties pavadinimas, kuriame yra žodis „vadovas“, turėtų būti įtrauktas į šią taisyklę.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="b6e1a-125">Apibrėžę į strategiją įtrauktos taisyklės ar taisyklių parametrus, galite priskirti išmokai priskirti konkrečią taisyklę.</span><span class="sxs-lookup"><span data-stu-id="b6e1a-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="b6e1a-126">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="b6e1a-126">See also</span></span>
--------

[<span data-ttu-id="b6e1a-127">Išmokų programos apibrėžimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="b6e1a-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




