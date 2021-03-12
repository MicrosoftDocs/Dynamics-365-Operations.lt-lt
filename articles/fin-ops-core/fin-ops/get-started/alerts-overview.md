---
title: Įspėjimų apžvalga
description: Šioje temoje pateikiama bendra informacija apie įspėjimus. Įspėjimus galite naudoti, kad būtumėte informuoti apie įvykius, kuriuos norite sekti darbo dienos metu.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 473f53d230d7272ba0fcf78bd05d7020635a870f
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798592"
---
# <a name="alerts-overview"></a><span data-ttu-id="ee115-104">Įspėjimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ee115-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="ee115-105">Apie įspėjimus</span><span class="sxs-lookup"><span data-stu-id="ee115-105">About alerts</span></span>
<span data-ttu-id="ee115-106">Įspėjimai sistemoje sudaro pranešimo apie svarbius įvykius sistemą.</span><span class="sxs-lookup"><span data-stu-id="ee115-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="ee115-107">Įspėjimus galite naudoti, kad būtumėte informuoti apie įvykius, kuriuos norite sekti darbo dienos metu.</span><span class="sxs-lookup"><span data-stu-id="ee115-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="ee115-108">Galite lengvai kurti savo įspėjimų taisyklių rinkinį, kad jums būtų pranešama apie pavėluotus pristatymus, panaikintus užsakymus, pasikeitusias kainas ar kitus įvykius, į kuriuos reikia reaguoti.</span><span class="sxs-lookup"><span data-stu-id="ee115-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="ee115-109">Įmonės išteklių planavimui (ERP) būdingi keletas atvejų, kuriais galima naudoti įspėjimų funkciją.</span><span class="sxs-lookup"><span data-stu-id="ee115-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="ee115-110">Štai keletas pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="ee115-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="ee115-111">1 atvejis: naujų pardavimo užsakymų įspėjimo taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="ee115-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="ee115-112">Atidaryti puslapį **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ee115-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="ee115-113">Veiksmų srityje, skirtuke **Parinktys**, grupėje **Bendrinti** pasirinkite **Kurti pasirinktinį įspėjimą**.</span><span class="sxs-lookup"><span data-stu-id="ee115-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="ee115-114">Dialogo lange **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane, kai** lauke **Įvykis** pasirinkite **Įrašas sukurtas**.</span><span class="sxs-lookup"><span data-stu-id="ee115-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="ee115-115">2 atvejis: pristatymo datos nukėlimo įspėjimo taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="ee115-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="ee115-116">Atidaryti puslapį **Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ee115-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="ee115-117">Pasirinkite pirkimo užsakymo ID, kad pasiektumėte pirkimo užsakymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="ee115-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="ee115-118">Išplėskite „FastTab“ **Pirkimo užsakymo antraštė**.</span><span class="sxs-lookup"><span data-stu-id="ee115-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="ee115-119">Veiksmų srityje, skirtuke **Parinktys**, grupėje **Bendrinti** pasirinkite **Kurti pasirinktinį įspėjimą**.</span><span class="sxs-lookup"><span data-stu-id="ee115-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="ee115-120">Dialogo lange **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane, kai** lauke **Laukas** pasirinkite **Pristatymo data**.</span><span class="sxs-lookup"><span data-stu-id="ee115-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="ee115-121">Lauke **Įvyks** pasirinkite **buvo atidėtas**.</span><span class="sxs-lookup"><span data-stu-id="ee115-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="ee115-122">Uždarius dialogo langą **Įspėjimo taisyklės kūrimas** taisyklė rodoma puslapyje **Įspėjimų taisyklių tvarkymas**.</span><span class="sxs-lookup"><span data-stu-id="ee115-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="ee115-123">Puslapyje **Įspėjimų taisyklių tvarkymas** galite naujinti esamas įspėjimų taisykles.</span><span class="sxs-lookup"><span data-stu-id="ee115-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="ee115-124">Pavyzdžiui, galite modifikuoti įvykių paleidiklius, atnaujinti įvykių pranešimus ir galiojimo datas.</span><span class="sxs-lookup"><span data-stu-id="ee115-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="ee115-125">Norėdami atidaryti puslapį **Įspėjimų taisyklių tvarkymas**, naudokite mygtuką **Įspėti mane**, esantį veiksmų srities skirtuke **Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="ee115-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="ee115-126">Kas įvyksta sukūrus įspėjimo taisyklę?</span><span class="sxs-lookup"><span data-stu-id="ee115-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="ee115-127">Kai kuriate įspėjimo taisykles, iš anksto numatytą įvykį susiejate su tam tikru lauku.</span><span class="sxs-lookup"><span data-stu-id="ee115-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="ee115-128">Pavyzdžiui, ateina lauke nurodyta diena arba pasikeičia lauko turinys.</span><span class="sxs-lookup"><span data-stu-id="ee115-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="ee115-129">Taip pat galite susieti įvykį su konkretaus puslapio įrašais.</span><span class="sxs-lookup"><span data-stu-id="ee115-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="ee115-130">Pavyzdžiui, įrašas sukuriamas arba įrašas panaikinamas.</span><span class="sxs-lookup"><span data-stu-id="ee115-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="ee115-131">Kai įvyksta pasirinktas įvykis, susijęs su lauku arba puslapio įrašu, jums siunčiamas įspėjimas.</span><span class="sxs-lookup"><span data-stu-id="ee115-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="ee115-132">Pavyzdžiui, sukuriate taisyklę ir susiejate konkrečios pirkimo užsakymo eilutės lauką **Pristatymo data** su įvykiu **praėjo prieš tiek laiko**.</span><span class="sxs-lookup"><span data-stu-id="ee115-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="ee115-133">Nustatote penkių dienų laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="ee115-133">You set the time frame to five days.</span></span> <span data-ttu-id="ee115-134">Tokiu atveju įspėjimas siunčiamas praėjus 5 dienoms po tos pirkimo užsakymo eilutės pristatymo datos.</span><span class="sxs-lookup"><span data-stu-id="ee115-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="ee115-135">Be to, įspėjimo taisykles galite patobulinti nustatydami sąlygas.</span><span class="sxs-lookup"><span data-stu-id="ee115-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="ee115-136">Pavyzdžiui, jus galima įspėti apie sukurtus naujus konkrečių tiekėjų kodų pirkimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="ee115-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="ee115-137">Pasirengimas nustatyti įspėjimą</span><span class="sxs-lookup"><span data-stu-id="ee115-137">Preparing for an alert</span></span>

<span data-ttu-id="ee115-138">Prieš nustatydami įspėjimo taisyklę nuspręskite, kada ar kokiais atvejais norite gauti įspėjimus.</span><span class="sxs-lookup"><span data-stu-id="ee115-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="ee115-139">Kai žinote, apie kokį įvykį norite būti įspėti, raskite puslapį, kuriame pateikiami duomenys, esantys to įvykio priežastimi.</span><span class="sxs-lookup"><span data-stu-id="ee115-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="ee115-140">Įvykis gali būti tam tikra atėjusi diena arba atliktas konkretus pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="ee115-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="ee115-141">Todėl turite rasti puslapį, kuriame nurodyta data arba vietą, kurioje rodomas pasikeitęs laukas arba sukurtas naujas įrašas.</span><span class="sxs-lookup"><span data-stu-id="ee115-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="ee115-142">Turėdami šią informaciją, galite kurti įspėjimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="ee115-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="ee115-143">Įspėjimo taisyklės komponentai</span><span class="sxs-lookup"><span data-stu-id="ee115-143">Components of an alert rule</span></span>

<span data-ttu-id="ee115-144">Įspėjimo taisyklę sudaro penki komponentai</span><span class="sxs-lookup"><span data-stu-id="ee115-144">An alert rule has five components:</span></span>

- <span data-ttu-id="ee115-145">**Įvykis** – įvykis, kuris suaktyvina įspėjimo taisyklę, gali būti atėjusi tam tikra diena arba konkretus įvykęs pasikeitimas.</span><span class="sxs-lookup"><span data-stu-id="ee115-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="ee115-146">Įvykiai nustatomi dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Siųsti el. pašto įspėjimus apie užduočių būsenų pasikeitimus**.</span><span class="sxs-lookup"><span data-stu-id="ee115-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="ee115-147">**Sąlyga** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane dėl** galite pasirinkti sąlygos apimtį, kad valdytumėte, kada jus įspėti apie įvykius.</span><span class="sxs-lookup"><span data-stu-id="ee115-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="ee115-148">Taisyklę galite taikyti tik esamam įrašui arba visiems puslapyje matomiems įrašams.</span><span class="sxs-lookup"><span data-stu-id="ee115-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="ee115-149">Jei taisyklė bus taikoma visuose juridiniuose subjektuose, galite nustatyti parametro **Visoje organizacijoje** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ee115-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="ee115-150">**Taisyklės galiojimo pabaiga** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane iki** galite nurodyti, kiek laiko įspėjimo taisyklė turėtų būti aktyvi.</span><span class="sxs-lookup"><span data-stu-id="ee115-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="ee115-151">**Turinys** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane nurodant** galite nurodyti pranešimo temą ir tekstą, kurios bus naudojamos įspėjimų pranešimuose.</span><span class="sxs-lookup"><span data-stu-id="ee115-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="ee115-152">**Vartotojas** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti ką** galite nurodyti, kuris vartotojas turėtų gauti įspėjimo gauti įspėjimų pranešimus.</span><span class="sxs-lookup"><span data-stu-id="ee115-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="ee115-153">Pagal numatytuosius parametrus pasirinktas jūsų vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="ee115-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ee115-154">Šią parinktį gali naudoti tik organizacijos administratoriai.</span><span class="sxs-lookup"><span data-stu-id="ee115-154">This option is restricted to organization administrators.</span></span>

## <a name="videos"></a><span data-ttu-id="ee115-155">Vaizdo įrašai</span><span class="sxs-lookup"><span data-stu-id="ee115-155">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="ee115-156">Kaip naudoti įspėjimus filtruojamiems duomenis stebėti</span><span class="sxs-lookup"><span data-stu-id="ee115-156">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="ee115-157">Vaizdo įrašas [Kaip naudoti įspėjimus filtruojamiems duomenis stebėti](https://youtu.be/ZYKMcv6kl9s) (pateiktas pirmiau) yra įtrauktas į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) „YouTube“.</span><span class="sxs-lookup"><span data-stu-id="ee115-157">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="ee115-158">Įspėjimo taisyklės parinktys</span><span class="sxs-lookup"><span data-stu-id="ee115-158">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="ee115-159">Vaizdo įrašas [Įspėjimo taisyklės parinktys](https://youtu.be/cpzimwOjicM) (pateiktas pirmiau) yra įtrauktas į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) „YouTube“.</span><span class="sxs-lookup"><span data-stu-id="ee115-159">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


