---
title: Turto gedimų išlaidų kontrolė
description: Šioje temoje aiškinamas turto gedimo kaštų valdymas turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c34180ad99db29147587bb002aaa6badc918717
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652246"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="5cfb8-103">Turto gedimų išlaidų kontrolė</span><span class="sxs-lookup"><span data-stu-id="5cfb8-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5cfb8-104">Turto valdyme galite apskaičiuoti turto gedimo registracijų kaštus, kad peržiūrėtumėte faktinius kaštus, palygintus su biudžeto kaštais.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="5cfb8-105">Faktiniai kaštai pagrįsti užregistruotomis operacijomis.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="5cfb8-106">Data yra gedimo data, kada įrašytas požymis.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="5cfb8-107">Spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimo kaštų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="5cfb8-108">Dialoge lange **Turto gedimo kaštų valdymas** pažymėkite finansinių matmenų rinkinį, kad jis būtų įtrauktas į skaičiavimą, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="5cfb8-109">Perjungimo mygtuke **Praleisti nulį** pažymėkite Taip, jei nenorite, kad būtų rodomi nulinių kaštų rezultatai.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="5cfb8-110">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti kaštų valdymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="5cfb8-111">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos turto gedimo kaštų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="5cfb8-112">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, turto gedimo kaštų valdymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="5cfb8-113">Jei norite apriboti iešką, „FastTab“ **Įtrauktini įrašai** galite pažymėti konkretų turtą, gedimų datas ir gedimo priežastis.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="5cfb8-114">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="5cfb8-115">Spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5cfb8-116">Pažymėti mygtukai **Grupuoti pagal** yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="5cfb8-117">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="5cfb8-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5cfb8-118">Example</span></span>

<span data-ttu-id="5cfb8-119">Šis pavyzdyje parodytas turto gedimo kaštų valdymo skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="5cfb8-120">Lauke **Originalus biudžetas** rodomi biudžeto kaštai iš darbo užsakymo prognozės.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="5cfb8-121">Lauke **Faktiniai kaštai** rodomi darbo užsakymuose užregistruoti kaštai.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="5cfb8-122">Lauke **Skirti kaštai** rodomi bendri kaštai, kuriuos jūsų įmonė skyrė pagal darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![1 pav.](media/05-controlling-and-reporting.png)

<span data-ttu-id="5cfb8-124">Informacijos, kaip nustatyti gedimus, žr. temoje [Gedimų valdymas](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="5cfb8-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>
