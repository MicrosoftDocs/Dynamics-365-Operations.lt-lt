---
title: Išmokos tinkamumo strategijos
description: Šiame straipsnyje pateikta informacija apie išmokos tinkamumo strategijas, kuri padės jums nustatyti, kas turi teisę gauti konkrečias išmokas.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 87a080c47e34a3265afea6494ff1733dac5bc384
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053110"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="a234f-103">Teisės į išmoką strategijos</span><span class="sxs-lookup"><span data-stu-id="a234f-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a234f-104">Šiame straipsnyje pateikta informacija apie išmokos tinkamumo strategijas, kuri padės jums nustatyti, kas turi teisę gauti konkrečias išmokas.</span><span class="sxs-lookup"><span data-stu-id="a234f-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="a234f-105">Kai kuriate išmokas, nusprendžiate, kurias išmokas gaus kurie darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="a234f-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="a234f-106">Toliau pateikiamoje lentelėje parodyt išmokų pavyzdžiai, kurias galite mokėti tam tikriems darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="a234f-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="a234f-107">Išmoka</span><span class="sxs-lookup"><span data-stu-id="a234f-107">Benefit</span></span>          | <span data-ttu-id="a234f-108">Kam mokama išmoka</span><span class="sxs-lookup"><span data-stu-id="a234f-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="a234f-109">Sveikatos draudimas</span><span class="sxs-lookup"><span data-stu-id="a234f-109">Health insurance</span></span> | <span data-ttu-id="a234f-110">Visi darbuotojai</span><span class="sxs-lookup"><span data-stu-id="a234f-110">All employees</span></span>                   |
| <span data-ttu-id="a234f-111">Mobilusis telefonas</span><span class="sxs-lookup"><span data-stu-id="a234f-111">Mobile phone</span></span>     | <span data-ttu-id="a234f-112">Pardavėjai, vadovai</span><span class="sxs-lookup"><span data-stu-id="a234f-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="a234f-113">Automobilių stovėjimo leidimai</span><span class="sxs-lookup"><span data-stu-id="a234f-113">Parking passes</span></span>   | <span data-ttu-id="a234f-114">Administracija</span><span class="sxs-lookup"><span data-stu-id="a234f-114">Executives</span></span>                      |

<span data-ttu-id="a234f-115">Toliau pateikti komponentai naudojami tinkamumo strategijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="a234f-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="a234f-116">Strategijos taisyklių tipai</span><span class="sxs-lookup"><span data-stu-id="a234f-116">Policy rule types</span></span>
-   <span data-ttu-id="a234f-117">Išmokos tinkamumo strategijos</span><span class="sxs-lookup"><span data-stu-id="a234f-117">Benefit eligibility policies</span></span>

<span data-ttu-id="a234f-118">Strategijos taisyklių tipai apibrėžia užklausų parametrus, kurie naudojami kuriant konkrečias strategijos taisykles.</span><span class="sxs-lookup"><span data-stu-id="a234f-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="a234f-119">Sukūrę strategijos taisyklių tipus, galite sukurti išmokų tinkamumo strategijas.</span><span class="sxs-lookup"><span data-stu-id="a234f-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="a234f-120">Strategijos leidžia sukurti taisyklių rinkinius, kurie taikomi vienam arba daugiau juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="a234f-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="a234f-121">Kiekvienoje strategijoje galite peržiūrėti bet kurį i, išmok. tinkamumo strategijos taisyklių tipų, kuriuos sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="a234f-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="a234f-122">Galite apibrėžti strategijos taisyklės apimtį.</span><span class="sxs-lookup"><span data-stu-id="a234f-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="a234f-123">Pavyzdžiui, jei sukuriate išmokų tinkamumo strategijos taisyklių tipą, pavadintą **Vadovų**, galite nurodyti, kokia taisyklė atitinka šią strategiją.</span><span class="sxs-lookup"><span data-stu-id="a234f-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="a234f-124">Šiame pavyzdyje taisyklė gali nurodyti, kad bet koks užduoties pavadinimas, kuriame yra žodis „vadovas“, turėtų būti įtrauktas į šią taisyklę.</span><span class="sxs-lookup"><span data-stu-id="a234f-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="a234f-125">Apibrėžę į strategiją įtrauktos taisyklės ar taisyklių parametrus, galite priskirti išmokai priskirti konkrečią taisyklę.</span><span class="sxs-lookup"><span data-stu-id="a234f-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]