---
title: Priežiūros grafiko išlaidos
description: Šioje temoje aiškinama priežiūros grafiko savikaina skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9686efb228e123671ba93a37480d2daac8d038a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252971"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="a5a3e-103">Priežiūros grafiko išlaidos</span><span class="sxs-lookup"><span data-stu-id="a5a3e-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a5a3e-104">Turto valdyme galite priežiūros grafiko eilutėse apskaičiuoti biudžeto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="a5a3e-105">Ši funkcija naudinga, kai norite peržiūrėti numatomas išlaidas, pavyzdžiui, išlaidas, susijusias su planuotomis prevencinėmis priežiūros užduotimis kitiems metams.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="a5a3e-106">Skaičiavimai grindžiami jau esamomis priežiūros grafiko eilutėmis, kurių tipas atitinka skiltis „Priežiūros planai“, „Priežiūros ciklai“ ir „Priežiūros užklausos“.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="a5a3e-107">Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Priežiūros grafiko savikaina**.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="a5a3e-108">Dialogo lange **Priežiūros grafiko savikaina** galite pasirinkti **Finansinės dimensijos rinkinys**, jei norite matyti savikainas, grupuojamas pagal finansinius dydžius.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="a5a3e-109">Finansinės dimensijos rinkinius galite rasti **DK** > **Klientų diagramos** > **Dimensijos** > **Finansinės dimensijos rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="a5a3e-110">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti priežiūros grafiko eilutėse.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="a5a3e-111">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros grafiko eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemiau esančių funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="a5a3e-112">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, priežiūros grafiko eilutes.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="a5a3e-113">Jei norite atlikti skaičiavimus tam tikram turtui, spustelėkite **Filtras** „FastTab“ **Įrašuose įtraukti** ir pasirinkite atitinkamą turtą.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="a5a3e-114">Jei reikia, galite taip pat nurodyti datą **Numatoma pradžia** savikainai apskaičiuoti arba pasirinkti kitą **būseną** skaičiuoti savikainą.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="a5a3e-115">Norėdami pradėti skaičiuoti savikainą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="a5a3e-116">Skirtuke **Priežiūros grafiko savikaina** > grupės veiksmų srityje **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas reikalingas išsamumo lygis savikainai skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="a5a3e-117">Pažymėti veiksmų srities grupės mygtukai yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="a5a3e-118">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="a5a3e-119">Spustelėkite mygtuką **Skaičiuoti savikainą**, jei norite naujai skaičiuoti savikainą.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="a5a3e-120">Toliau pateiktame paveikslėlyje pateikiami priežiūros grafiko savikainos skaičiavimo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="a5a3e-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![1 pav.](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]