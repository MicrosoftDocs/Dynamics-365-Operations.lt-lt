---
title: "Įspėjimo taisyklių kūrimas"
description: "Šioje temoje pateikiama informacija apie įspėjimus ir paaiškinama, kaip kurti įspėjimo taisyklę, kad būtumėte įspėti apie įvykius, pvz., atėjusią tam tikrą dieną arba konkretų įvykusį pasikeitimą."
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: cbf4917424e72a70a6d513b5daf45f6bf9cd57c7
ms.contentlocale: lt-lt
ms.lasthandoff: 12/18/2018

---

# <a name="create-alert-rules"></a><span data-ttu-id="f7cc2-103">Įspėjimo taisyklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7cc2-103">Create alert rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a><span data-ttu-id="f7cc2-104">Darbo pradžia</span><span class="sxs-lookup"><span data-stu-id="f7cc2-104">Getting started</span></span>

<span data-ttu-id="f7cc2-105">Prieš nustatydami įspėjimo taisyklę nuspręskite, kada ar kokiais atvejais norite gauti įspėjimus.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="f7cc2-106">Kai žinote, apie kokį įvykį norite būti įspėti, programoje „Microsoft Dynamics 365 for Finance and Operations“ raskite puslapį, kuriame pateikiami duomenys, esantys to įvykio priežastimi.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-106">When you know which event you want to be notified about, in Microsoft Dynamics 365 for Finance and Operations find the page where the data that causes that event appears.</span></span> <span data-ttu-id="f7cc2-107">Įvykis gali būti tam tikra atėjusi diena arba atliktas konkretus pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="f7cc2-108">Todėl turite rasti puslapį, kuriame nurodyta data arba vietą, kurioje rodomas pasikeitęs laukas arba sukurtas naujas įrašas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="f7cc2-109">Turėdami šią informaciją, galite kurti įspėjimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="f7cc2-110">Kai sukuriate įspėjimo taisyklę, nustatote kriterijus, kuriuos reikia įvykdyti prie suaktyvinant įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="f7cc2-111">Žinokite, kad kriterijus yra įvykio buvimo ir nurodytų sąlygų tenkinimo sutapimas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-111">You can think of criteria as a match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="f7cc2-112">Kai įvykis įvyksta, sistema pradeda tikrinti atsižvelgdama į „Finance and Operations“ nustatytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-112">When an event occurs, the system starts to perform a check according to the conditions that are set up in Finance and Operations.</span></span>

## <a name="events"></a><span data-ttu-id="f7cc2-113">Įvykiai</span><span class="sxs-lookup"><span data-stu-id="f7cc2-113">Events</span></span>

<span data-ttu-id="f7cc2-114">Įvykis, kuris suaktyvina įspėjimo taisyklę, gali būti atėjusi tam tikra diena arba konkretus įvykęs pasikeitimas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-114">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="f7cc2-115">Įvykių paleidikliai apibrėžti dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane, kai**.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-115">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="f7cc2-116">Konkrečiam laukui priskirti įvykiai priklauso nuo pasirinkto paleidiklio.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-116">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="f7cc2-117">Pavyzdžiui, jei nustatote įspėjimo taisyklę, skirtą laukui **Pradžios data**, tinkami termino įvykiai.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-117">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="f7cc2-118">Todėl tipo **terminas** įvykis priskiriamas tam laukui.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-118">Therefore, the **is due in** event type is available for that field.</span></span> <span data-ttu-id="f7cc2-119">Tačiau tokiam laukui kaip **Išlaidų centras** termino tipo įvykis nėra tinkamas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-119">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="f7cc2-120">Todėl tipo **terminas** įvykis nepriskiriamas tam laukui.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-120">Therefore, the **is due in** event type isn't available.</span></span> <span data-ttu-id="f7cc2-121">Priskiriamas tipo **pasikeitė** įvykis.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-121">Instead, the **has changed** event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="f7cc2-122">Įvykių tipai</span><span class="sxs-lookup"><span data-stu-id="f7cc2-122">Event types</span></span>

<span data-ttu-id="f7cc2-123">Toliau nurodyti trijų tipų įvykiai, kurie gali įvykti.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-123">Three types of events can occur:</span></span>

- <span data-ttu-id="f7cc2-124">**Kūrimo ir naikinimo tipų įvykiai** – šie įvykiai suaktyvina įspėjimą, kai sukuriamas arba panaikinamas įrašas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-124">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="f7cc2-125">**Naujinimo tipo įvykiai** – šie įvykiai suaktyvina įspėjimą, kai pasikeičia konkretaus lauko duomenys.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-125">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="f7cc2-126">**Termino tipo įvykiai** – šie įvykiai suaktyvina įspėjimą, kai ateina tam tikra diena.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-126">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="f7cc2-127">Įvykusius pakeitimus gali inicijuoti vartotojas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-127">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="f7cc2-128">Pavyzdžiui, vartotojas pakeičia pirkimo užsakymo pristatymo datą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-128">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="f7cc2-129">Be to, pakeitimai gali įvykti kaip proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-129">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="f7cc2-130">Pavyzdžiui, puslapio laukas **Būsena** pasikeičia, kad atspindėtų įvairių sistemos procesų ciklą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-130">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="f7cc2-131">Sąlygos</span><span class="sxs-lookup"><span data-stu-id="f7cc2-131">Conditions</span></span>

<span data-ttu-id="f7cc2-132">Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane dėl** galite naudoti sąlygas, kad valdytumėte, kada jus įspėti apie įvykius.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-132">On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="f7cc2-133">Pavyzdžiui, galite nurodyti, kad sistema turėtų jus įspėti, kai pasikeičia pirkimo užsakymų būsena, tačiau tik jei būsena atitinka tam tikrą sąlygų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-133">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="f7cc2-134">Pavyzdžiui, jūs norite, kad jus įspėtų, kai pirkimo užsakymo būsena pasikeičia į **Gauta**.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-134">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="f7cc2-135">Šis būsenos pasikeitimas yra įvykis, kuri suaktyvina įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-135">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="f7cc2-136">Taip pat turite nuspręsti, apie kuriuos pirkimo užsakymus reikia jus įspėti.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-136">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="f7cc2-137">Pavyzdžiui, galite pasirinkti vieną iš toliau nurodytų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-137">For example, you can select one of the following options.</span></span> <span data-ttu-id="f7cc2-138">Šios pasirinktis nurodo įspėjimo taisyklės sąlygas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-138">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="f7cc2-139">**Dabartinis pasirinktas įrašas** – gaunate įspėjimą, kai konkretaus pirkimo užsakymo būsena pasikeičia į **Gauta**.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-139">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="f7cc2-140">**Visi įrašai** – gaunate įspėjimą, kai prekės pirkimo užsakymo būsena pasikeičia aktyvaus puslapio rodinyje.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-140">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="f7cc2-141">Kurdami tam tikrų įrašų taisykles galite naudoti puslapyje pateiktus išplėstinius filtrus.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-141">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="f7cc2-142">Pavyzdžiui, galite kurti įspėjimą, kuris suaktyvinamas, kai pasikeičia visų pirkimo užsakymų, susijusių su konkrečios klientų grupės klientais, būsena.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-142">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="f7cc2-143">Taisyklės galiojimo pabaiga</span><span class="sxs-lookup"><span data-stu-id="f7cc2-143">Expiry of rule</span></span>

<span data-ttu-id="f7cc2-144">Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane iki** galite nurodyti, kiek laiko įspėjimo taisyklė turėtų būti aktyvi.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-144">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="f7cc2-145">Įspėjimo turinys</span><span class="sxs-lookup"><span data-stu-id="f7cc2-145">Alert contents</span></span>

<span data-ttu-id="f7cc2-146">Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane nurodant** galite nurodyti pranešimo temą ir tekstą, kurios bus naudojamos įspėjimų pranešimuose.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-146">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="f7cc2-147">Vartotojo ID</span><span class="sxs-lookup"><span data-stu-id="f7cc2-147">User ID</span></span>

<span data-ttu-id="f7cc2-148">Dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane ir** galite nurodyti, kuris vartotojas turėtų gauti įspėjimo gauti įspėjimų pranešimus.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-148">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="f7cc2-149">Pagal numatytuosius parametrus pasirinktas jūsų vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-149">By default, your user ID is selected.</span></span> <span data-ttu-id="f7cc2-150">Šią parinktį gali naudoti tik organizacijos administratoriai.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-150">This option is restricted to organization administrators.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="f7cc2-151">Įspėjimo taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7cc2-151">Create an alert rule</span></span>

1. <span data-ttu-id="f7cc2-152">Atidarykite puslapį, kuriame yra norimi stebėti duomenys.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-152">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="f7cc2-153">Veiksmų srityje, skirtuke **Parinktys**, grupėje **Bendrinti** pasirinkite **Kurti įspėjimo taisyklę**.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-153">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="f7cc2-154">Dialogo lango **Įspėjimo taisyklės kūrimas** lauke **Laukas** pasirinkite lauką, kurį norite stebėti.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-154">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="f7cc2-155">Lauke **Įvykis** pasirinkite tinkamumo įvykio tipą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-155">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="f7cc2-156">„FastTab“ **Įspėti mane dėl** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-156">On the **Alert me for** FastTab, select an option.</span></span>
6. <span data-ttu-id="f7cc2-157">Jei norite, kad nuo tam tikros dienos įspėjimo taisyklė būtų neaktyvi, „FastTab“ **Įspėti mane iki** pasirinkite pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-157">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="f7cc2-158">„FastTab“**Įspėti mane ir** lauke **Tema** pasirinkite numatytąją el. laiško antraštės temą arba įveskite naują temą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-158">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="f7cc2-159">Tekstas yra naudojamas kaip temos antraštė el. laiške, kurį gausite, kai bus suaktyvintas įspėjimas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-159">The text is used as the subject heading for the email message that you receive when an alert is triggered.</span></span>
8. <span data-ttu-id="f7cc2-160">Lauke **Pranešimas** įveskite pasirinktinį pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-160">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="f7cc2-161">Tekstas yra naudojamas kaip pranešimas, kurį gausite, kai bus suaktyvintas įspėjimas.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-161">The text is used as the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="f7cc2-162">Pasirinkite **Gerai** norėdami išsaugoti parametrus ir sukurti įspėjimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="f7cc2-162">Select **OK** to save the settings and create the alert rule.</span></span>

