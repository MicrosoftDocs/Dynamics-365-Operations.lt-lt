---
title: IoT analizės scenarijaus sąranka
description: Šioje temoje aprašoma, kaip konfigūruoti IoT analizės scenarijų programoje „Supply Chain Management“.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597173"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="b5a8c-103">IoT analizės scenarijaus sąranka</span><span class="sxs-lookup"><span data-stu-id="b5a8c-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5a8c-104">Šioje temoje aprašoma, kaip konfigūruoti IoT analizės scenarijų programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="b5a8c-105">Prieš konfigūruodami scenarijus turite [sukonfigūruoti LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b5a8c-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="b5a8c-106">Šioje temoje konfigūruosite scenarijų **Įrangos prastovos**, kad įrenginiui sugedus, programoje „Supply Chain Management“ būtų sugeneruotas pranešimas.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="b5a8c-107">Scenarijaus **Įrangos prastovos** konfigūravimas programoje „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="b5a8c-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="b5a8c-108">Scenarijus **Įrangos prastovos** susieja dalinio išjungimo signalą su įrenginio įspėjimo ribine verte.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="b5a8c-109">Įrenginys stebimas tik tada, kai jis pasirinktas scenarijuje ir nustatytas veikti programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="b5a8c-110">Jeigu laikas nuo įrengino paskutinio gauto dalinio išjungimo signalo yra didesnis už įspėjimo ribinę vertę, suaktyvinamas pranešimas **Įrenginys neveikia**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="b5a8c-111">Jeigu įrenginys vis dar veikia, kai gaunamas kitas **Dalinio išjungimo** signalas, suaktyvinamas pranešimas **Įrenginys veikia**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="b5a8c-112">Jei įrenginys neveikia 30 min., suaktyvinamas naujas pranešimas **Įrenginys neveikia**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="b5a8c-113">Scenarijus **Įrangos prastovos** turi toliau nurodytas priklausomybes.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="b5a8c-114">Norint suaktyvinti įspėjimą, susietame įrenginyje turi būti paleistas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="b5a8c-115">Signalas, atitinkantis susieto įrenginio dalinio išjungimo signalą, turi būti išsiųstas į „IoT Hub“ su unikaliu ypatybės pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="b5a8c-116">„IoT Hub“ pranešime turi būti „Unix“ milisekundžių laiko žymos ypatybė.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="b5a8c-117">Norėdami konfigūruoti scenarijų, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="b5a8c-118">Prisijunkite prie „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="b5a8c-119">Įgalinkite IoT analizės funkcijos vėliavėlę.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="b5a8c-120">Daugiau informacijos žr. [Funkcijų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b5a8c-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="b5a8c-121">Sukonfigūruokite metriką.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-121">Configure the metrics.</span></span> <span data-ttu-id="b5a8c-122">Daugiau informacijos žr. [Kaip sukonfigūruoti metriką](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="b5a8c-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="b5a8c-123">Eikite į **Gamybos kontrolė**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="b5a8c-124">Eikite į **Sąranka \> IoT analizė \> Scenarijaus valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="b5a8c-125">Plytelėje **Įrangos prastovos** spustelėkite **Konfigūruoti**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="b5a8c-126">Konfigūracijos vedlys prasideda puslapiu **Įrangos jutiklio schemos apibrėžimas**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="b5a8c-127">Tikslas – programoje „Supply Chain Management“ nustatyti schemą, kuri atitiktų IoT pranešimų JSON formatą.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="b5a8c-128">Galima apibrėžti kelias pranešimų schemas.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="b5a8c-129">Daugiau informacijos, žr. [Pranešimų schemų formatai, skirti „IoT Hub“](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="b5a8c-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="b5a8c-130">Šiame pavyzdyje pranešimų apkrovoje yra pranešimų su šiuo formatu paketas:</span><span class="sxs-lookup"><span data-stu-id="b5a8c-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="b5a8c-131">Įtraukite į lentelę eilutę.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="b5a8c-132">Nustatykite **Schemos pavadinimas** reikšmę kaip **ID**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="b5a8c-133">Nustatykite **Schemos kelias** reikšmę kaip **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="b5a8c-134">Nustatykite **Aprašas** reikšmę kaip **Pranešimo ID**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="b5a8c-135">Įtraukite į lentelę eilutę.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="b5a8c-136">Nustatykite **Schemos pavadinimas** reikšmę kaip **Laiko žyma**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="b5a8c-137">Nustatykite **Schemos kelias** reikšmę kaip **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="b5a8c-138">Nustatykite **Aprašas** reikšmę kaip **Pranešimo laiko žyma**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="b5a8c-139">Įtraukite į lentelę eilutę.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="b5a8c-140">Nustatykite **Schemos pavadinimas** reikšmę kaip **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="b5a8c-141">Nustatykite **Schemos kelias** reikšmę kaip **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="b5a8c-142">Nustatykite **Aprašas** reikšmę kaip **Pranešimo reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="b5a8c-143">Jums nebūtina pranešime apibrėžti visų ypatybių. Apibrėžkite tik tas, kurios jums reikalingos.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="b5a8c-144">Šiame pavyzdyje nesukūrėte eilutės **Šakninė laiko žyma**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="b5a8c-145">**Šakninė laiko žyma** kelias bus **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="b5a8c-146">Norėdami eiti į puslapį **Įrangos jutiklio schemos susiejimas** spustelėkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="b5a8c-147">Eilutėje **Įrangos išteklių ID** nustatykite **Schemos pavadinimas** reikšmę kaip **ID**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="b5a8c-148">Leistinos reikšmės rodomos išplėčiamojoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="b5a8c-149">Eilutėje **UTC laikas** nustatykite **Schemos pavadinimas** reikšmę kaip **Laiko žyma**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="b5a8c-150">Leistinos reikšmės rodomos išplėčiamojoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="b5a8c-151">Eilutėje **Dalinai sugeneruotas signalas** nustatykite **Schemos pavadinimas** reikšmę kaip **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="b5a8c-152">Leistinos reikšmės rodomos išplėčiamojoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="b5a8c-153">Norėdami atidaryti puslapį **Įrangos išteklių ID konfigūracija** spustelėkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="b5a8c-154">Atlikdami šį veiksmą galite susieti „IoT Hub“ pranešimų reikšmes su „Supply Chain Management“ ištekliais.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="b5a8c-155">Lentelėje **Signalo duomenų reikšmės** įtraukite naują eilutę ir stulpelyje **Reikšmė** įveskite **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="b5a8c-156">Reikšmė **IoTInt.Machine1225.PartOut** gaunama iš JSON ypatybės **id** „IoT Hub“ pranešime.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="b5a8c-157">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-157">Click **Save**.</span></span>
    3. <span data-ttu-id="b5a8c-158">Lentelėje **Verslo įrašo susiejimas** spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="b5a8c-159">Numatytoji ypatybės **Verslo įrašo tipas** reikšmė yra įvesta automatiškai, ir jums jos keisti nereikia.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="b5a8c-160">Stulpelyje **Verslo įrašas** pasirinkite „Supple Chain Management“ įrenginio išteklių, iš kurio siunčiama ši signalo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="b5a8c-161">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-161">Click **Save**.</span></span>
    6. <span data-ttu-id="b5a8c-162">Kartokite šiuos veiksmus įtraukdami naujo verslo įrašo **Machine1226** susiejimą.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="b5a8c-163">Su vienu „Supply Chain Management“ įrašu galite susieti kelias signalo duomenų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="b5a8c-164">Norėdami pasirinkti, kuriuos įrenginius apdoroti, naudokite stulpelį **Pasirinkta**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="b5a8c-165">Jums nebūtina apibrėžti visų signalų reikšmių ir pasirinkti visų įrenginių.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="b5a8c-166">Spustelėkite **Pirmyn**, jei norite pereiti į puslapį **Dalinai sugeneruoto signalo konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="b5a8c-167">Lentelėje **Signalo duomenų reikšmės** įtraukite eilutę ir nustatykite ypatybės **Reikšmė** reikšmę kaip **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="b5a8c-168">Reikšmė **Teisinga** gaunama iš JSON ypatybės **value** „IoT Hub“ pranešime.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="b5a8c-169">Savo scenarijuje galite pridėti tiek reikšmių, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="b5a8c-170">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-170">Click **Save**.</span></span>
20. <span data-ttu-id="b5a8c-171">Norėdami eiti į puslapį **Įrangos prastovos ribinė vertė** spustelėkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="b5a8c-172">Nurodyti įrenginiai yra anksčiau su signalo reikšmėmis susieti įrenginiai.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="b5a8c-173">Šiame veiksme apibrėžiate ribinę vertę, kad nustatytumėte, ar įrenginys sugedo.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="b5a8c-174">Pavyzdžiui, jei nustatysite ribinę vertę 10, „Supply Chain Management“ sugeneruos pranešimą, jei 10 minučių iš įrenginio nebus gautas dalinio išjungimo pranešimas.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="b5a8c-175">Norėdami pereiti puslapį **Įgalinti scenarijų**, spustelėkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="b5a8c-176">Norėdami įgalinti scenarijų, perjunkite slankiklį.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="b5a8c-177">Spustelėkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-177">Click **Finish**.</span></span>

<span data-ttu-id="b5a8c-178">Scenarijaus sąranka baigta.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-178">The scenario setup is complete.</span></span> <span data-ttu-id="b5a8c-179">IoT analizės papildinys pradės automatiškai apdoroti „IoT Hub“ pranešimus.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="b5a8c-180">Scenarijaus **Produkto kokybė** konfigūravimas programoje „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="b5a8c-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="b5a8c-181">Scenarijus **Produkto kokybė** sugeneruoja pranešimą, jei prekės atributas nepatenka į nurodytą diapazoną.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="b5a8c-182">Pavyzdžiui, jutiklis galėtų siųsti kiekvienos prekės svorį į „IoT Hub“.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="b5a8c-183">Jei prekė per sunki arba per lengva, programoje „Supply Chain Management“ būtų sugeneruotas pranešimas.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="b5a8c-184">Scenarijus turi toliau nurodytas priklausomybes.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="b5a8c-185">Tam, kad būtų suaktyvintas įspėjimas, gamybos užsakymas turi būti vykdomas susietame įrenginyje ir generuoti produktą su susieto paketo atributu.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="b5a8c-186">Signalas, atitinkantis paketo atributą, turi būti išsiųstas į „IoT Hub“ su unikaliu ypatybės pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="b5a8c-187">„IoT Hub“ pranešime turi būti „Unix“ milisekundžių laiko žymos ypatybė.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="b5a8c-188">Scenarijaus **Gamybos atidėjimai** konfigūravimas programoje „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="b5a8c-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="b5a8c-189">Scenarijus **Gamybos atidėjimai** generuoja pranešimą, jei gamybos našumas yra mažesnis už ribinę vertę.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="b5a8c-190">Šiame scenarijuje signalas **PartOut** siunčiamas į „IoT Hub“ kiekvienai pagamintai prekei.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="b5a8c-191">Programoje „Supply Chain Management“ užsakymo atidėjimas apskaičiuojamas pagal tai, kiek laiko suplanuota vykdyti gamybos užsakymą, kiek prekių turėtų būti pagaminta, kaip ilgai vykdoma užduotis ir kiek signalų **PartOut** gauta.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="b5a8c-192">Perspėjimas dėl atidėjimo būtų sugeneruotas, jei užduoties signalų **PartOut** skaičius yra mažesnis už numatytos reikšmės ribinę vertę.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="b5a8c-193">Scenarijus turi toliau nurodytas priklausomybes.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="b5a8c-194">Norint suaktyvinti įspėjimą, susietame įrenginyje turi būti paleistas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="b5a8c-195">Signalas, atitinkantis susieto įrenginio dalinio išjungimo signalą, turi būti išsiųstas į „IoT Hub“ su unikaliu ypatybės pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="b5a8c-196">„IoT Hub“ pranešime turi būti „Unix“ milisekundžių laiko žymos ypatybė.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="b5a8c-197">Kaip išjungti scenarijų</span><span class="sxs-lookup"><span data-stu-id="b5a8c-197">How to disable a scenario</span></span>

<span data-ttu-id="b5a8c-198">Norėdami išjungti scenarijų, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="b5a8c-199">Programoje „Supply Chain Management“ eikite į **Gamybos kontrolė \> Sąranka \> IoT analizė \> Scenarijaus valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="b5a8c-200">Scenarijuje spustelėkite **Konfigūruoti**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="b5a8c-201">Norėdami pereiti į paskutinį vedlio skirtuką spustelėkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="b5a8c-202">Norėdami išjungti scenarijų, perjunkite slankiklį.</span><span class="sxs-lookup"><span data-stu-id="b5a8c-202">Toggle the slider to disable the scenario.</span></span>
