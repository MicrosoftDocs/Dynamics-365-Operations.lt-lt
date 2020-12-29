---
title: Susipažinkite su datos ir laiko laukais
description: Supraskite, ko tikėtis naudojant laukus Data ir laikas programoje „Microsoft Dynamics 365 Human Resources”. Išsiaiškinkite, ko galima tikėtis sąveikaujant su laukų Data ir laikas duomenimis formoje „Human Resources”, išoriniame šaltinyje arba „Common Data Service”.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 027e46d53fd9704f5483e90409be53c1510e8cd4
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529857"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="06c70-104">Susipažinkite su datos ir laiko laukais</span><span class="sxs-lookup"><span data-stu-id="06c70-104">Understand Date and Time fields</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="06c70-105">**Datos ir laiko** laukai yra pagrindinės „Dynamics 365 Human Resources” sąvokos.</span><span class="sxs-lookup"><span data-stu-id="06c70-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="06c70-106">Svarbu suprasti, kaip dirbti su lauko **Data ir laikas** duomenimis „Dynamics 365 Human Resources” formose, „Common Data Service” ir išoriniuose šaltiniuose.</span><span class="sxs-lookup"><span data-stu-id="06c70-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="06c70-107">Skirtumo tarp laukų Data bei Data ir laikas duomenų tipų supratimas</span><span class="sxs-lookup"><span data-stu-id="06c70-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="06c70-108">Laukuose **Data ir laikas** yra laiko juostos informacija, o laukuose **Data** laukuose jos nėra.</span><span class="sxs-lookup"><span data-stu-id="06c70-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="06c70-109">Laukuose **Data** laukuose rodoma ta pati informacija bet kurioje vietoje.</span><span class="sxs-lookup"><span data-stu-id="06c70-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="06c70-110">Kai įvedate datą į lauką **Data**, „Human Resources” įrašo tą pačią datą į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="06c70-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="06c70-111">Kai duomenys rodomi lauke **Data ir laikas**, „Human Resources” koreguoja datą ir laiką pagal vartotojo laiko juostą, nustatytą formoje **Vartotojo parinktys** (**Bendra > Sąranka > Vartotojo parinktys**).</span><span class="sxs-lookup"><span data-stu-id="06c70-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="06c70-112">Datos ir laiko informacija, kurią įvedate lauke, gali skirtis nuo informacijos, įrašytos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="06c70-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="06c70-113">[![Forma „Vartotojo pasirinktys”](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="06c70-114">Datos ir laiko laukų formose supratimas</span><span class="sxs-lookup"><span data-stu-id="06c70-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="06c70-115">Įvedant duomenis lauke **Data ir laikas**, ekrane rodomi duomenys nėra tokie patys kaip duomenų bazėje saugomi duomenys, jei vartotojo laiko juosta nėra nustatyta kaip universalusis laikas (UTC).</span><span class="sxs-lookup"><span data-stu-id="06c70-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="06c70-116">Laukuose **Data ir laikas** duomenys visada saugomi kaip UTC.</span><span class="sxs-lookup"><span data-stu-id="06c70-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="06c70-117">[![Darbininko forma](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="06c70-118">Datos ir laiko laukų duomenų bazėje supratimas</span><span class="sxs-lookup"><span data-stu-id="06c70-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="06c70-119">Kai „Human Resources” įrašo lauko **Data ir laikas** reikšmę į duomenų bazę, jis išsaugo duomenis UTC.</span><span class="sxs-lookup"><span data-stu-id="06c70-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="06c70-120">Tai leidžia vartotojams matyti visus lauko **Data ir laikas** duomenis, susijusius su jų vartotojo parinktyse apibrėžta laiko juosta.</span><span class="sxs-lookup"><span data-stu-id="06c70-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="06c70-121">Aukščiau pateiktame pavyzdyje pradžios laikas yra laiko taškas, o ne konkreti data.</span><span class="sxs-lookup"><span data-stu-id="06c70-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="06c70-122">Keičiant prisijungusio vartotojo laiko juostą iš GMT +12:00 į GMT UTC, toks pats ką tik sukurtas įrašas rodo 2019-04-30 12:00:00 vietoj 2019-05-01 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="06c70-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="06c70-123">Toliau pateiktame pavyzdyje darbuotojo 000724 įdarbinimas tampa aktyvus tuo pačiu metu, neatsižvelgiant į laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="06c70-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="06c70-124">Darbuotojas bus aktyvus 2019-04-30 GMT laiko juostoje, kuri yra tokia pati kaip 2019-05-01, GMT +12:00 laiko juosta.</span><span class="sxs-lookup"><span data-stu-id="06c70-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="06c70-125">Abu nurodo tą patį laiko tašką, o ne konkrečią datą.</span><span class="sxs-lookup"><span data-stu-id="06c70-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="06c70-126">[![Darbininko forma](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="06c70-127">Datos ir laiko duomenys duomenų valdymo sistemoje, „Excel Common Data Service” ir „Power BI”</span><span class="sxs-lookup"><span data-stu-id="06c70-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="06c70-128">Duomenų valdymo sistema, „Excel” papildinys, „Common Data Service” ir „Power BI” ataskaitos yra sukurti taip, kad galėtų sąveikauti su duomenimis duomenų bazės lygiu.</span><span class="sxs-lookup"><span data-stu-id="06c70-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="06c70-129">Kadangi nėra kliento, kad būtų galima koreguoti lauko **Data ir laikas** duomenis pagal vartotojo laiko juostą, visos lauko **Data ir laikas** reikšmės yra UTC, o tai gali sukelti tam tikrų klaidingų prielaidų įvedant arba peržiūrint duomenis.</span><span class="sxs-lookup"><span data-stu-id="06c70-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="06c70-130">Duomenų bazė lauko **Data ir laikas** duomenis, pateikiamus per DMF, „Excel” ar „Common Data Service”, laiko UTC.</span><span class="sxs-lookup"><span data-stu-id="06c70-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="06c70-131">Tai gali sukelti tam tikrą painiavą, kai pateikta lauko **Data ir laikas** reikšmė nėra tokia, kokios tikėtasi, nes duomenis peržiūrintis vartotojas nenustatęs vartotojo laiko juostos į UTC.</span><span class="sxs-lookup"><span data-stu-id="06c70-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="06c70-132">Tas pats gali įvykti atvirkštiniu procesu, kai duomenys yra eksportuojami.</span><span class="sxs-lookup"><span data-stu-id="06c70-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="06c70-133">Lauko **Data ir laikas** duomenys eksportuotame DMF objekte gali skirtis nuo to, kas rodoma „Dynamics” kliente.</span><span class="sxs-lookup"><span data-stu-id="06c70-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="06c70-134">Kai naudojate išorinius šaltinius, pvz., DMF, norėdami peržiūrėti arba autorizuoti duomenis, svarbu nepamiršti, kad lauko **Data ir laikas** reikšmės pagal numatytuosius parametrus laikomos UTC, neatsižvelgiant į vartotojo kompiuterio laiko juostą ar dabartinius vartotojo laiko juostos parametrus.</span><span class="sxs-lookup"><span data-stu-id="06c70-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="06c70-135">Atvejų, kai tas pats įrašas rodomas skirtingose produkto srityse, pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="06c70-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="06c70-136">**„Human Resources“ vartotojo laiko zona nustatyta į UTC**</span><span class="sxs-lookup"><span data-stu-id="06c70-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="06c70-137">[![Darbininko forma](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="06c70-138">**„Human Resources” vartotojo laiko zona nustatyta į GMT + 12:00**</span><span class="sxs-lookup"><span data-stu-id="06c70-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="06c70-139">[![Darbininko forma](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="06c70-140">**„Excel”, naudojant „OData”**</span><span class="sxs-lookup"><span data-stu-id="06c70-140">**Excel Via OData**</span></span>

<span data-ttu-id="06c70-141">[![„Excel”, naudojant „OData”](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="06c70-142">**DMF paruošimas**</span><span class="sxs-lookup"><span data-stu-id="06c70-142">**DMF Staging**</span></span>

<span data-ttu-id="06c70-143">[![DMF paruošimas](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="06c70-144">**DMF eksportavimas**</span><span class="sxs-lookup"><span data-stu-id="06c70-144">**DMF Export**</span></span>

<span data-ttu-id="06c70-145">[![DMF paruošimas](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="06c70-146">**„Excel”, naudojant „Common Data Service”**</span><span class="sxs-lookup"><span data-stu-id="06c70-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="06c70-147">[![Excel, naudojant „Common Data Service”](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="06c70-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="06c70-148">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="06c70-148">See also</span></span>

[<span data-ttu-id="06c70-149">Datos ir laiko duomenys</span><span class="sxs-lookup"><span data-stu-id="06c70-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="06c70-150">Vartotojo pageidaujamos laiko zonos</span><span class="sxs-lookup"><span data-stu-id="06c70-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
