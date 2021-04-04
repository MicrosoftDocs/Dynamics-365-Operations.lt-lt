---
title: Asmeninės informacijos redagavimo apribojimas
description: Apribokite darbuotojus redaguoti kontaktinius „Dynamics 365 Human Resources“ duomenis.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503041"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="675ad-103">Asmeninės informacijos redagavimo apribojimas</span><span class="sxs-lookup"><span data-stu-id="675ad-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="675ad-104">Šioje temoje aprašoma, kaip apriboti darbuotojų kontaktinės informacijos „Dynamics 365 Human Resources“ redagavimą.</span><span class="sxs-lookup"><span data-stu-id="675ad-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="675ad-105">Galbūt norėsite neleisti darbuotojams redaguoti tam tikros kontaktinės informacijos, pvz., darbo vietos ar el. pašto adreso.</span><span class="sxs-lookup"><span data-stu-id="675ad-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="675ad-106">Kad galėtumėte naudoti šią funkciją, pirmiausia funkcijų valdymo srityje įjunkite funkciją **(Peržiūra) Darbuotojams apriboti prieigą prie adreso ir kontaktinės informacijos pridėjimo ar redagavimo pasirinktais tikslais**.</span><span class="sxs-lookup"><span data-stu-id="675ad-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="675ad-107">Daugiau informacijos apie peržiūros versijos funkcijų įjungimą žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="675ad-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="675ad-108">![Įjungti peržiūros funkciją](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="675ad-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="675ad-109">Pasirinkite informaciją, kurią darbuotojas gali pridėti arba redaguoti</span><span class="sxs-lookup"><span data-stu-id="675ad-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="675ad-110">Žmogiškuosiuose ištekliuose, pasirinkite **Personalo valdymas**, pasirinkite **Nuorodos** ir tuomet pasirinkite **Žmogiškųjų išteklių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="675ad-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Eikite į personalo parametrus](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="675ad-112">Puslapyje **Personalo parametrai** pasirinkite skirtuką **Darbuotojų savitarna**.</span><span class="sxs-lookup"><span data-stu-id="675ad-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Darbuotojo savitarnos pasirinkimas](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="675ad-114">Skirtuke **Darbuotojo savitarna** atžymėkite visą informaciją skyriuje **Adresas ir kontaktinė informacija**, kurios nenorite leisti darbuotojams pridėti ar redaguoti.</span><span class="sxs-lookup"><span data-stu-id="675ad-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="675ad-115">Šiame pavyzdyje atžymėjome verslo **Įmonės** kontaktinę informaciją.</span><span class="sxs-lookup"><span data-stu-id="675ad-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Įmonės kontaktinės informacijos redagavimo ribojimas](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="675ad-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="675ad-117">Select **Save**.</span></span>

   ![Įrašyti pakeitimus](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="675ad-119">Darbuotojo patirtis</span><span class="sxs-lookup"><span data-stu-id="675ad-119">Employee experience</span></span>

<span data-ttu-id="675ad-120">Apriboję darbuotojo teises pridėti ar redaguoti kontaktinius duomenis, jis informaciją matys, bet jos keisti negalės.</span><span class="sxs-lookup"><span data-stu-id="675ad-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="675ad-121">Šiame pavyzdyje, kai darbuotojams neleidžiama redaguoti **Įmonės** kontaktinių duomenų, jie šią informaciją matus darbuotojo savitarnoje:</span><span class="sxs-lookup"><span data-stu-id="675ad-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Įmonės kontaktinių duomenų peržiūra](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="675ad-123">Tačiau jiems pasirinkus įmonės kontaktinius duomenis, sritis **Redaguoti adresą** bus skirta tik skaityti ir jokių laukelių jie keisti negalės.</span><span class="sxs-lookup"><span data-stu-id="675ad-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Įmonės kontaktiniai duomenys rodomi kaip skirti tik skaityti](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="675ad-125">Be to, darbuotojui pasirinkus **Pridėti**, kad jis pridėtų naują adresą, jis negalės pasirinkti **Įmonė** išskleidžiamajame laukelyje **Paskirtis**.</span><span class="sxs-lookup"><span data-stu-id="675ad-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Darbuotojas negali pridėti įmonės adreso](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="675ad-127">Darbuotojai tą patį pamatys ir pasirinkę **Kontaktiniai duomenys** puslapyje **Asmeninė informacija** ir pridėdami naują adresą.</span><span class="sxs-lookup"><span data-stu-id="675ad-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="675ad-128">Išskleidžiamajame laukelyje **Paskirtis** rodomi tik informacijos, kurią galima pridėti, tipai.</span><span class="sxs-lookup"><span data-stu-id="675ad-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Darbuotojas paskirties išskleidžiamajame laukelyje įmonės pasirinkti negali](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="675ad-130">**Kontaktiniai duomenys** nėra rodomi tinklelyje **Paskirtis**.</span><span class="sxs-lookup"><span data-stu-id="675ad-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Paskirtis rodoma kontaktinių duomenų tinklelyje](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="675ad-132">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="675ad-132">See also</span></span>

[<span data-ttu-id="675ad-133">Darbuotojų ir vadovų savitarnos apžvalga</span><span class="sxs-lookup"><span data-stu-id="675ad-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="675ad-134">„Human Resources“ parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="675ad-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="675ad-135">Redaguoti asmeninę informaciją</span><span class="sxs-lookup"><span data-stu-id="675ad-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)