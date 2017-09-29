---
title: "Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes"
description: "Šiame straipsnyje aprašoma, kaip iš praeities duomenų, kurie naudojami poreikio prognozei apskaičiuoti, pašalinti pašalines reikšmes. Pašalinę pašalines reikšmes, galite padidinti prognozės tikslumą."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ea3f08b20e25af6ebb738c2373b65532d74a0c80
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="55442-104">Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes</span><span class="sxs-lookup"><span data-stu-id="55442-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="55442-105">Šiame straipsnyje aprašoma, kaip iš praeities duomenų, kurie naudojami poreikio prognozei apskaičiuoti, pašalinti pašalines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="55442-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="55442-106">Pašalinę pašalines reikšmes, galite padidinti prognozės tikslumą.</span><span class="sxs-lookup"><span data-stu-id="55442-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="55442-107">Pašalinę pašalines reikšmes galite padidinti prognozės tikslumą.</span><span class="sxs-lookup"><span data-stu-id="55442-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="55442-108">Ši užduotis nėra privaloma.</span><span class="sxs-lookup"><span data-stu-id="55442-108">This is an optional task.</span></span> <span data-ttu-id="55442-109">Toliau pateikta proceso apžvalga.</span><span class="sxs-lookup"><span data-stu-id="55442-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="55442-110">Norėdami atidaryti puslapį **Pašalinių reikšmių šalinimas**, kuriame, naudodami užklausą, galėtumėte pasirinkti šalintinas operacijas, spustelėkite **Bendrasis planavimas** &gt; **Sąranka** &gt; **Poreikio prognozė** &gt; **Pašalinių reikšmių šalinimas**.</span><span class="sxs-lookup"><span data-stu-id="55442-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="55442-111">Pasirinkite įmonę, kuriai užklausa taikoma, tada įveskite pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="55442-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="55442-112">**Užklausos datos** laukas automatiškai nustatomas į dabartinę datą.</span><span class="sxs-lookup"><span data-stu-id="55442-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="55442-113">Pažymėkite žymės langelį **Aktyv.**, kad iš praeities duomenų pašalintumėte operacijas, rastas naudojant užklausą.</span><span class="sxs-lookup"><span data-stu-id="55442-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="55442-114">Šis parametras pradės veikti, kai kursite pagrindinę prognozę.</span><span class="sxs-lookup"><span data-stu-id="55442-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="55442-115">Puslapyje **Pašalinių reikšmių šalinimo užklausa** galite pridėti, šalinti ir pasirinkti kriterijus, apibrėžiančius, kurios operacijos bus pašalintos skaičiuojant pagrindinę prognozę.</span><span class="sxs-lookup"><span data-stu-id="55442-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="55442-116">Pvz., pasirinkite konkrečią prekę arba užsakymo operaciją, kurią norite pašalinti.</span><span class="sxs-lookup"><span data-stu-id="55442-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="55442-117">Spustelėkite **Rodyti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="55442-117">Click **Display transactions**.</span></span> <span data-ttu-id="55442-118">Puslapyje **Pašalinių reikšmių operacijos** išvardijamos operacijos, kurios atitinka jūsų užklausoje nurodytus kriterijus ir kurios apskaičiuojant poreikio prognozę bus pašalintos iš praeities duomenų.</span><span class="sxs-lookup"><span data-stu-id="55442-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="55442-119">**Pastaba:** taip pat galite sukurti užklausą, paremtą esama užklausa.</span><span class="sxs-lookup"><span data-stu-id="55442-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="55442-120">Pasirinkite užklausą, kurią norite kopijuoti, tada spustelėkite **Dubliuoti**.</span><span class="sxs-lookup"><span data-stu-id="55442-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="55442-121">Lauke **Užklausos data** identifikuojama versija.</span><span class="sxs-lookup"><span data-stu-id="55442-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="55442-122">Užklausą galite naudoti tokią, kokia ji yra, arba galite spustelėti **Redaguoti užklausą** ir modifikuoti kriterijus.</span><span class="sxs-lookup"><span data-stu-id="55442-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="55442-123">Neprivaloma: galite modifikuoti naujosios užklausos pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="55442-123">You can optionally modify the name and description of the new query.</span></span>

<a name="see-also"></a><span data-ttu-id="55442-124">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="55442-124">See also</span></span>
--------

[<span data-ttu-id="55442-125">Įvadas į poreikio prognozes</span><span class="sxs-lookup"><span data-stu-id="55442-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="55442-126">Prognozės tikslumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="55442-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)



