---
title: Susipažinkite su datos ir laiko laukais
description: Supraskite, ko tikėtis naudojant laukus Data ir laikas programoje „Microsoft Dynamics 365 Human Resources”.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7e5726f7e4beea1584b9a8e142212531ba1db56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051742"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="de668-103">Susipažinkite su datos ir laiko laukais</span><span class="sxs-lookup"><span data-stu-id="de668-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="de668-104">**Datos ir laiko** laukai yra pagrindinės „Dynamics 365 Human Resources” sąvokos.</span><span class="sxs-lookup"><span data-stu-id="de668-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="de668-105">Svarbu suprasti, kaip dirbti su **Data ir laiku** duomenimis formose, „Dataverse“ ir išorės šaltiniuose.</span><span class="sxs-lookup"><span data-stu-id="de668-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="de668-106">Skirtumo tarp laukų Data bei Data ir laikas duomenų tipų supratimas</span><span class="sxs-lookup"><span data-stu-id="de668-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="de668-107">Laukuose **Data ir laikas** yra laiko juostos informacija, o laukuose **Data** laukuose jos nėra.</span><span class="sxs-lookup"><span data-stu-id="de668-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="de668-108">Laukuose **Data** laukuose rodoma ta pati informacija bet kurioje vietoje.</span><span class="sxs-lookup"><span data-stu-id="de668-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="de668-109">Kai įvedate datą į lauką **Data**, „Human Resources” įrašo tą pačią datą į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="de668-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="de668-110">Kai duomenys rodomi lauke **Data ir laikas**, „Human Resources” koreguoja datą ir laiką pagal vartotojo laiko juostą, nustatytą formoje **Vartotojo parinktys** (**Bendra > Sąranka > Vartotojo parinktys**).</span><span class="sxs-lookup"><span data-stu-id="de668-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="de668-111">Datos ir laiko informacija, kurią įvedate lauke, gali skirtis nuo informacijos, įrašytos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="de668-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="de668-112">[![Forma „Vartotojo pasirinktys”](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="de668-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="de668-113">Datos ir laiko laukų formose supratimas</span><span class="sxs-lookup"><span data-stu-id="de668-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="de668-114">**Data ir laikas** duomenys yra rodomi ekrane nėra tokie patys kaip duomenys laikomi duomenų bazėje, jei vartotojo laiko zona nėra nustatyta koordinuotame universaliame laike (UTC).</span><span class="sxs-lookup"><span data-stu-id="de668-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="de668-115">Laukuose **Data ir laikas** duomenys visada saugomi kaip UTC.</span><span class="sxs-lookup"><span data-stu-id="de668-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="de668-116">[![Darbuotojo forma UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="de668-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="de668-117">Datos ir laiko laukų duomenų bazėje supratimas</span><span class="sxs-lookup"><span data-stu-id="de668-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="de668-118">Kai „Human Resources“ rašo **Datos ir laiko** vertę į duomenų bazę, jie laiko duomenis UTC.</span><span class="sxs-lookup"><span data-stu-id="de668-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="de668-119">Tai leidžia vartotojams matyti visus lauko **Data ir laikas** duomenis, susijusius su jų vartotojo parinktyse apibrėžta laiko juosta.</span><span class="sxs-lookup"><span data-stu-id="de668-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="de668-120">Aukščiau pateiktame pavyzdyje pradžios laikas yra laiko taškas, o ne konkreti data.</span><span class="sxs-lookup"><span data-stu-id="de668-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="de668-121">Keisdamas laiko juostą prisijungęs vartotojas iš GMT +12:00 į GMT UTC, tas pats įrašas rodo 04/30/2019 12:00:00, o ne 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="de668-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="de668-122">Toliau pateiktame pavyzdyje darbuotojo 000724 įdarbinimas tampa aktyvus tuo pačiu metu, neatsižvelgiant į laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="de668-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="de668-123">Darbuotojas bus aktyvus 2019-04-30 GMT laiko juostoje, kuri yra tokia pati kaip 2019-05-01, GMT +12:00 laiko juosta.</span><span class="sxs-lookup"><span data-stu-id="de668-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="de668-124">Abu nurodo tą patį laiko tašką, o ne konkrečią datą.</span><span class="sxs-lookup"><span data-stu-id="de668-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="de668-125">[![Darbuotojo forma GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="de668-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="de668-126">Datos ir laiko duomenys duomenų valdymo sistemoje, „Excel Dataverse” ir „Power BI”</span><span class="sxs-lookup"><span data-stu-id="de668-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="de668-127">Duomenų valdymo sistema, „Excel” papildinys, „Dataverse” ir „Power BI” ataskaitos yra sukurti taip, kad galėtų sąveikauti su duomenimis duomenų bazės lygiu.</span><span class="sxs-lookup"><span data-stu-id="de668-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="de668-128">Kadangi nėra jokio kliento, kuris taiso **Datos ir laiko** vartotojo duomenis laiko zonai, visos **Datos ir laiko** vertės yra UTC, kurios gali vesti į kai kurias neteisingas prielaidas įvedant ar peržiūrint duomenis.</span><span class="sxs-lookup"><span data-stu-id="de668-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="de668-129">**Datos ir laiko** duomenys pateikti per DMF, „Excel“ ar „Dataverse“ yra priimami būti UTC duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="de668-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="de668-130">Tai gali sukelti tam tikrą painiavą, kai pateikta lauko **Data ir laikas** reikšmė nėra tokia, kokios tikėtasi, nes duomenis peržiūrintis vartotojas nenustatęs vartotojo laiko juostos į UTC.</span><span class="sxs-lookup"><span data-stu-id="de668-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="de668-131">Tas pats gali įvykti atvirkštiniu procesu, kai duomenys yra eksportuojami.</span><span class="sxs-lookup"><span data-stu-id="de668-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="de668-132">Duomenys **Data ir laikas** eksportuoti DMF objekte gali skirtis nei tie, kurie rodomi „Dynamics“ kliente.</span><span class="sxs-lookup"><span data-stu-id="de668-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="de668-133">Naudojant išorės šaltinius, tokius kaip DMF tam, kad peržiūrėtumėte ir suteiktumėte leidimą duomenims, atminkite, kad **Datos ir laiko** vertės yra laikomos pagal nutylėjimą UTC nepriklausomai nuo vartotojo kompiuterio ar esamo vartotojo laiko zonos ar jos nustatymų.</span><span class="sxs-lookup"><span data-stu-id="de668-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="de668-134">Atvejų, kai tas pats įrašas rodomas skirtingose produkto srityse, pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="de668-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="de668-135">**„Human Resources“ vartotojo laiko zona nustatyta į UTC**</span><span class="sxs-lookup"><span data-stu-id="de668-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="de668-136">[![Darbuotojo forma nustatyta į UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="de668-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="de668-137">**„Human Resources” vartotojo laiko zona nustatyta į GMT + 12:00**</span><span class="sxs-lookup"><span data-stu-id="de668-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="de668-138">[![Darbuotojo forma nustatyta į GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="de668-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="de668-139">**„Excel”, naudojant „OData”**</span><span class="sxs-lookup"><span data-stu-id="de668-139">**Excel Via OData**</span></span>

<span data-ttu-id="de668-140">[![„Excel”, naudojant „OData”](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="de668-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="de668-141">**DMF paruošimas**</span><span class="sxs-lookup"><span data-stu-id="de668-141">**DMF Staging**</span></span>

<span data-ttu-id="de668-142">[![DMF paruošimas](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="de668-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="de668-143">**DMF eksportavimas**</span><span class="sxs-lookup"><span data-stu-id="de668-143">**DMF Export**</span></span>

<span data-ttu-id="de668-144">[![DMF eksportavimas](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="de668-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="de668-145">**„Excel”, naudojant „Dataverse”**</span><span class="sxs-lookup"><span data-stu-id="de668-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="de668-146">[![Excel, naudojant „Dataverse”](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="de668-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="de668-147">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="de668-147">See also</span></span>

[<span data-ttu-id="de668-148">Datos ir laiko duomenys</span><span class="sxs-lookup"><span data-stu-id="de668-148">Date and time data</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="de668-149">Vartotojo pageidaujamos laiko zonos</span><span class="sxs-lookup"><span data-stu-id="de668-149">User preferred time zones</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]