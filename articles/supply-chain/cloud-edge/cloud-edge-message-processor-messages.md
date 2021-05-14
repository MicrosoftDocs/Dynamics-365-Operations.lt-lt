---
title: Pranešimų procesoriaus pranešimai
description: Šioje temoje pateikiama informacija apie pranešimų procesoriaus pranešimų funkciją, kuri skirta skalės vieneto darbo krūviui.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b1428e2e657e653874d4ec07605932a32bd803b2
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938255"
---
# <a name="message-processor-messages"></a><span data-ttu-id="57d20-103">Pranešimų procesoriaus pranešimai</span><span class="sxs-lookup"><span data-stu-id="57d20-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="57d20-104">Pranešimų procesoriaus pranešimai naudojami, kai paleisti debesies ir kraštų [skalės vienetai, skirti gamybos darbo krūviui](cloud-edge-workload-manufacturing.md) ir [sandėlio valdymo darbo](cloud-edge-workload-warehousing.md) krūviui.</span><span class="sxs-lookup"><span data-stu-id="57d20-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="57d20-105">Centro ir svarstyklių vieneto diegimo aplinkose keičiamasi labai daug duomenų, kad jos būtų sinchronizuojamos, tačiau pranešimų procesorius apdoros tik keletą šių *duomenų* mainų.</span><span class="sxs-lookup"><span data-stu-id="57d20-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="57d20-106">Galite peržiūrėti pranešimus, kuriuos apdorojo pranešimų procesorius, nueikite į Sistemos administravimas **> Pranešimų procesorius > Pranešimų procesoriaus** pranešimai.</span><span class="sxs-lookup"><span data-stu-id="57d20-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="57d20-107">Pranešimų tinklelio stulpeliai ir filtrai</span><span class="sxs-lookup"><span data-stu-id="57d20-107">Message grid columns and filters</span></span>

<span data-ttu-id="57d20-108">Galite naudoti laukus pranešimų procesoriaus pranešimų puslapio viršuje, norėdami **padėti** rasti visus konkrečius jūsų ieškomus pranešimus.</span><span class="sxs-lookup"><span data-stu-id="57d20-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="57d20-109">Dauguma šių filtrų atitinka pranešimų tinklelio stulpelių antraštes.</span><span class="sxs-lookup"><span data-stu-id="57d20-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="57d20-110">Galimi šie filtrai ir stulpelių antraštės:</span><span class="sxs-lookup"><span data-stu-id="57d20-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="57d20-111">**Pranešimo** tipas – nurodo pranešimo tipą.</span><span class="sxs-lookup"><span data-stu-id="57d20-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="57d20-112">**Pranešimų eilė** – nurodo eilės, kurioje bus apdorojamas pranešimas, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="57d20-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="57d20-113">Pateiktos šios eilės:</span><span class="sxs-lookup"><span data-stu-id="57d20-113">The following queues are provided:</span></span>
  - <span data-ttu-id="57d20-114">*Skalės vienetas koncentratoriui*</span><span class="sxs-lookup"><span data-stu-id="57d20-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="57d20-115">*Iš telkinio į sandėlį vykdymo skalės vienetas*</span><span class="sxs-lookup"><span data-stu-id="57d20-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="57d20-116">*Telkinys, skirtas gamybos vykdymo skalės vienetui*</span><span class="sxs-lookup"><span data-stu-id="57d20-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="57d20-117">**Pranešimo** būsena – nurodo pranešimo būseną.</span><span class="sxs-lookup"><span data-stu-id="57d20-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="57d20-118">Yra tokios būsenos:</span><span class="sxs-lookup"><span data-stu-id="57d20-118">The following states exists:</span></span>
  - <span data-ttu-id="57d20-119">*Eilėje* – pranešimą gali apdoroti pranešimų procesorius.</span><span class="sxs-lookup"><span data-stu-id="57d20-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="57d20-120">*Apdorotos* – pranešimas buvo sėkmingai apdorotas pranešimo tvarkytojo.</span><span class="sxs-lookup"><span data-stu-id="57d20-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="57d20-121">*Atšaukta –* pranešimas buvo apdorotas, bet apdoroti nepavyko.</span><span class="sxs-lookup"><span data-stu-id="57d20-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="57d20-122">**Pranešimo turinys** – Šis filtras atlieką visą teksto paiešką pagal pranešimo turinį.</span><span class="sxs-lookup"><span data-stu-id="57d20-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="57d20-123">(Pranešimo turinys nerodomas tinklelyje.) Filtras kaip tarpus traktuoja svarbiausius simbolius (pvz., „-") ir visus tarpų simbolius traktuoja kaip „Boolean“ AR operatorius.</span><span class="sxs-lookup"><span data-stu-id="57d20-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="57d20-124">T=Pvz., tai reiškia, kad ieškosite konkrečios vertės, lygios `journalid` „USMF-123456", sistema surasti visus pranešimus, kuriuose yra „USMF" arba „123456", kurie tikriausiai bus ilgas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="57d20-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="57d20-125">Todėl būtų geriau tik įvesti „123456", nes taip bus pateikti išsamesni rezultatai.</span><span class="sxs-lookup"><span data-stu-id="57d20-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="57d20-126">Pavyzdinio pranešimo tipas: Prašyti atsargų koregavimo finansinio atnaujinimo</span><span class="sxs-lookup"><span data-stu-id="57d20-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="57d20-127">Pavyzdžiui, pranešimo tipas Reikalauti atsargų koregavimo finansinio atnaujinimo naudojamas kuriant ir registruojant inventorizacijos žurnalą centre, kai darbuotojas naudoja sandėlio programą atsargų koregavimui dėl svarstyklių vieneto valdymo **darbo** *krūvio* [registruoti](cloud-edge-warehouse-inventory-adjustment.md).</span><span class="sxs-lookup"><span data-stu-id="57d20-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="57d20-128">Kadangi šis konkretus procesas kyla iš svarstyklių vieneto, pranešimų eilės lauke svarstyklių **vienetas** *bus rodomas kaip svarstyklių vienetas ir* centras.</span><span class="sxs-lookup"><span data-stu-id="57d20-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="57d20-129">Šiam pranešimo tipui skalės vieneto darbo krūvis įrašo pranešimą kaip sandėlio programos atsargų koregavimo operacijos dalį.</span><span class="sxs-lookup"><span data-stu-id="57d20-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="57d20-130">Tada pranešimo duomenys perkeliami į tą patį procesą, naudojamą [„Commerce Data Exchange" architektūroje](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="57d20-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="57d20-131">Pranešimas bus atnaujintas, kad būtų rodoma **pranešimo būsena** darbo *eilėje*.</span><span class="sxs-lookup"><span data-stu-id="57d20-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="57d20-132">Tada pranešimų procesorius bando apdoroti pranešimą ir atnaujina pranešimo būseną į Apdorota sėkmingai arba **Atšaukta** *trikties* *metu*.</span><span class="sxs-lookup"><span data-stu-id="57d20-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="57d20-133">Peržiūrėti pranešimų žurnalą, pranešimų turinį ir informaciją</span><span class="sxs-lookup"><span data-stu-id="57d20-133">View the message log, message content, and details</span></span>

<span data-ttu-id="57d20-134">Išsamią informaciją apie pranešimą galite rasti pasirinkę jį tinklelyje ir atidarydami žurnalo arba pranešimo turinio skirtukus pranešimų tinklelyje, kuriame rodomas kiekvienas **apdorojimo** **įvykis**.</span><span class="sxs-lookup"><span data-stu-id="57d20-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="57d20-135">Pranešimo **turinys priklauso nuo pranešimo** **tipo, todėl jo teksto ilgis bus** skirtingas.</span><span class="sxs-lookup"><span data-stu-id="57d20-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="57d20-136">Įprastas pranešimo turinio tekstas prasidės su a **{** ir baigsis su a **}** tuo tarpu tarp jų bus laukelių pavadinimai, tokie kaip `journalId` ir vėliau a **:** ir vertė, tokia kaip *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="57d20-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="57d20-137">Žurnalo skirtuke **esančioje** įrankių juostoje yra šie mygtukai:</span><span class="sxs-lookup"><span data-stu-id="57d20-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="57d20-138">**Žurnalas** – rodo apdorojimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="57d20-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="57d20-139">Tai ypač naudinga norint suprasti pranešimų, kurių apdorojimo rezultatas yra **Nepavyko,** apdorojimo *trikties* priežastis.</span><span class="sxs-lookup"><span data-stu-id="57d20-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="57d20-140">**Grupavimas** – kelios pranešimų apdorojimo operacijos gali būti paleidžiaos kaip to paties paketinio vykdymo dalis.</span><span class="sxs-lookup"><span data-stu-id="57d20-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="57d20-141">Pasirinkite šį mygtuką, jei norite peržiūrėti visus duomenis.</span><span class="sxs-lookup"><span data-stu-id="57d20-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="57d20-142">Pavyzdžiui, galite pamatyti, ar yra priklausomybių, kurioms sistema reikalauja apdoroti konkrečius pranešimus tam tikra seka.</span><span class="sxs-lookup"><span data-stu-id="57d20-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="57d20-143">Pranešimų procesoriaus paketinė užduotis</span><span class="sxs-lookup"><span data-stu-id="57d20-143">Message processor batch job</span></span>

<span data-ttu-id="57d20-144">Paleidus debesį ir diegiant kraštų, pranešimų procesoriaus paketinė užduotis bus automatiškai išskaiduota, kai bus sukurtas naujas apdoroti skirtas pranešimas, todėl jums nereikia planuoti šios užduoties *rankiniu* būdu.</span><span class="sxs-lookup"><span data-stu-id="57d20-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="57d20-145">Jei reikia, paketinę užduotį galite pasiekti nueię į Sistemos administravimas **> Pranešimų procesorius > Pranešimų** procesorius.</span><span class="sxs-lookup"><span data-stu-id="57d20-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="57d20-146">Pranešimo apdorojimas rankiniu būdu arba atšaukimas</span><span class="sxs-lookup"><span data-stu-id="57d20-146">Manually process or cancel a message</span></span>

<span data-ttu-id="57d20-147">Jei reikia, galite neautomatiniu būdu apdoroti arba atšaukti pranešimą, priklausomai nuo dabartinės jo būsenos.</span><span class="sxs-lookup"><span data-stu-id="57d20-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="57d20-148">Norėdami tai padaryti, pasirinkite tinklelyje rodoimą pranešimą ir veiksmų **srityje pasirinkite Procesas** arba **Atšaukti**</span><span class="sxs-lookup"><span data-stu-id="57d20-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="57d20-149">Nustatyti verslo įvykius, kurie turėtų pateikti įspėjimus dėl nesėkmingų rezultatų</span><span class="sxs-lookup"><span data-stu-id="57d20-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="57d20-150">Be filtravimo pranešimo būsenos reikšmės Atšaukta, kad būtų galima pateikti užklausą dėl nepavykusių pranešimų, galite nustatyti centro verslo įvykius, kad įspėtų jus **apie** *nesėkmingus* [rezultatus](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="57d20-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="57d20-151">Norėdami tai padaryti, suaktyvinkite verslo įvykio, pavadinto *Pranešimų procesoriaus pranešimas* apdorotą **Verslo įvykių katalogo** puslapį (**Sistemos administravimas > Sąranka > Verslo įvykiai > Verslo įvykių katalogas**).</span><span class="sxs-lookup"><span data-stu-id="57d20-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="57d20-152">Kaip aktyvinimo proceso dalį jūs nurodysite, ar įvykis yra konkretus vienam ar visiems juridiniams subjektams ir pateikite galinio punkto pavadinimą, kurį **pirmiausia** reikia apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="57d20-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="57d20-153">Jei **Numatytas verslo įvykis atsitinka** yra nustatytas į *„Microsoft Power Automate“* (o ne į *HTTPS*, pavyzdžiui), **Galutinio taško pavadinimas** bus automatiškai sukuriamas „Supply Chain Management“ pagal *„Microsoft Power Automate“* nustatymus.</span><span class="sxs-lookup"><span data-stu-id="57d20-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="57d20-154">Pavyzdys: „Microsoft Power Automate“</span><span class="sxs-lookup"><span data-stu-id="57d20-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="57d20-155">Šiame pavyzdyje naudokite Kai verslo įvykis įvyksta išsiunčiant el. laiškus, kuriuose yra Sistemos pranešimo pranešimai ir hipersaitai, kad atidarytumėte pranešimo procesoriaus pranešimų puslapį, skirta tam tikro nepavykusio pranešimo **pranešimą** diegiant *Microsoft Power Automate* **centrą**.</span><span class="sxs-lookup"><span data-stu-id="57d20-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="57d20-156">Jei reikia, galite pridėti papildomą logiką, kad pranešimai būtų išsiunčiami lygiagrečiai, naudojant skirtingus kanalus ir valdyti gavėjus, remiantis įvykio duomenimis.</span><span class="sxs-lookup"><span data-stu-id="57d20-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="57d20-157">[„Power Automate“](https://preview.flow.microsoft.com), sukurkite naują automatizuotą debiesies srautą srauto paleidikliui **Įvykus veiklos įvykiui - „Fin & Ops App“ („Dynamics 365“)** po kurios seka **„Parse JSON“** ir **Siųsti el. laišką** veiksmus, kaip parodyta tolesniame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="57d20-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automatizuotas debesies srautas":::

1. <span data-ttu-id="57d20-159">Kai verslo įvykis įvyksta, galite peržiūrėti ar įvesti centro egzempliorių pagal kategoriją ir tada apdorojamas verslo įvykio pranešimų procesoriaus pranešimas, kaip parodyta toliau pateiktame **kaip** **parodyta** **toliau** **pateiktame** *pavyzdyje*.</span><span class="sxs-lookup"><span data-stu-id="57d20-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Kai vyksta verslo įvykis, veiksmas":::

1. <span data-ttu-id="57d20-161">Įveskite **veiksmą Parse** JSON, **schemą,** apibrėžiaą išplėstinius laukus.</span><span class="sxs-lookup"><span data-stu-id="57d20-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="57d20-162">Galite naudoti atsisiuntimo schemos parinktį verslo įvykių katalogo puslapyje „Supply Chain Management“ arba *pradėti* įklijuodami **į** pavyzdinį schemos tekstą.</span><span class="sxs-lookup"><span data-stu-id="57d20-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="57d20-163">Šis pavyzdis tekstas pateikiamas po šio pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="57d20-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Išanalizuoti JSON veiksmą":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="57d20-165">El. laiško siuntimo veiksme galite pasirinkti atskirus laukus arba pradėti įklijuodami el. **laiško** pranešimo pavyzdį į **lauką** Tekstas.</span><span class="sxs-lookup"><span data-stu-id="57d20-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="57d20-166">Šis pavyzdis tekstas pateikiamas po šio pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="57d20-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate el. laiško siuntimo veiksmas":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="57d20-168">Įrašant verslo įvykį, jis bus automatiškai suaktyvintas ir paruoštas naudoti kaip „Supply Chain Management“ dalis.</span><span class="sxs-lookup"><span data-stu-id="57d20-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
