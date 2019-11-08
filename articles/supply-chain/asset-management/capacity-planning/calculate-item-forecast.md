---
title: Apskaičiuoti elemento prognozę
description: Šioje temoje aiškinama, kaip skaičiuoti elemento prognozę turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 65d95507e27ade373008e2046ac4691c271484ca
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652453"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="6adfa-103">Apskaičiuoti elemento prognozę</span><span class="sxs-lookup"><span data-stu-id="6adfa-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6adfa-104">Taip, kaip galite atlikti pajėgumo skaičiavimus, aprašytus ankstesniame skyriuje, taip pat galite skaičiuoti toliau nurodytų elementų prognozes:</span><span class="sxs-lookup"><span data-stu-id="6adfa-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="6adfa-105">priežiūros grafiko eilutės</span><span class="sxs-lookup"><span data-stu-id="6adfa-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="6adfa-106">darbo užsakymai, kurie dar nėra suplanuoti</span><span class="sxs-lookup"><span data-stu-id="6adfa-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="6adfa-107">suplanuoti darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="6adfa-107">scheduled work orders</span></span>

<span data-ttu-id="6adfa-108">Tai naudinga, jei norite peržiūrėti numatytą elementų naudojimą (atsarginių dalių ir kitų elementų, kurių reikia norint įvykdyti darbo užsakymą) konkrečiu periodu.</span><span class="sxs-lookup"><span data-stu-id="6adfa-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="6adfa-109">Galima apskaičiuoti viso turto arba pasirinkto turto elementų prognozę.</span><span class="sxs-lookup"><span data-stu-id="6adfa-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="6adfa-110">Taip pat galite skaičiuoti prižiūrimo turto prastovos veiklą (**Visos prižiūrimo turto prastovos veiklos** arba **Aktyvios prižiūrimo turto prastovos veiklos**) arba darbo užsakymų telkinį (**Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai**).</span><span class="sxs-lookup"><span data-stu-id="6adfa-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="6adfa-111">Spustelėkite mygtuką **Turto valdymas** > **Užklausos** > **Elemento prognozė** arba **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** / **Aktyvių darbo užsakymų telkiniai** >pasirinkti darbo užsakymų telkinį sąraše > **Elemento prognozė** arba mygtuką **Turto valdymas** > **Bendrieji dalykai** > **Prižiūrimo turto prastovos veiklos** > **Visos prižiūrimo turto prastovos veiklos** / **Aktyvios prižiūrimo turto prastovos veiklos** > pasirinkti prižiūrimo turto prastovos veiklą sąraše > **Elemento prognozė**.</span><span class="sxs-lookup"><span data-stu-id="6adfa-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="6adfa-112">Dialoge **Skaičiuoti elemento prognozę** laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** pažymėkite skaičiavimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="6adfa-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="6adfa-113">Perjungimo mygtuke **Įtraukti priežiūros grafiką** pažymėkite Taip, jei norite į prognozės skaičiavimą įtraukti priežiūros grafiko eilutes.</span><span class="sxs-lookup"><span data-stu-id="6adfa-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="6adfa-114">Perjungimo mygtuke **Įtraukti darbo užsakymą** pažymėkite Taip, jei norite į prognozės skaičiavimą įtraukti darbo užsakymo užduotis.</span><span class="sxs-lookup"><span data-stu-id="6adfa-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="6adfa-115">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti elementų prognozės eilutėse.</span><span class="sxs-lookup"><span data-stu-id="6adfa-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="6adfa-116">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros grafikos eilutės ir darbo užsakymai, skirti funkcinei vietai, bus rodomi viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="6adfa-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="6adfa-117">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, visas priežiūros grafiko eilutes ir visus darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="6adfa-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="6adfa-118">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6adfa-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="6adfa-119">Grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis.</span><span class="sxs-lookup"><span data-stu-id="6adfa-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="6adfa-120">Toliau pateiktoje ekrano kopijoje pasirinkti mygtukai **Grupuoti pagal** yra pažymėti mėlynai.</span><span class="sxs-lookup"><span data-stu-id="6adfa-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="6adfa-121">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="6adfa-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="6adfa-122">Spustelėkite mygtuką **Rodyti matmenis**, jei norite matyti elementus, susijusius su produktu, saugykla arba sekimo matmenimis.</span><span class="sxs-lookup"><span data-stu-id="6adfa-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="6adfa-123">Pažymėkite atitinkamus žymės langelius ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6adfa-123">Select the relevant check boxes, and click **OK**.</span></span>

![1 pav.](media/02-capacity-planning.png)
