---
title: Susieti kuro indeksą su vežėju kaip mokestį už papildomas paslaugas
description: Šiame vadove nurodoma, kaip sukurti papildomų paslaugų priskyrimą, vežėjo papildomų paslaugų mokestį, papildomo degalų mokesčio papildomų paslaugų šabloną ir susieti vežėjo degalų indeksą su vežėju.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbd58fb6b03f3c6eb5e54f811d98ad636e65a94
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146381"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="ee84b-103">Susieti kuro indeksą su vežėju kaip mokestį už papildomas paslaugas</span><span class="sxs-lookup"><span data-stu-id="ee84b-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee84b-104">Šiame vadove nurodoma, kaip sukurti papildomų paslaugų priskyrimą, vežėjo papildomų paslaugų mokestį, papildomo degalų mokesčio papildomų paslaugų šabloną ir susieti vežėjo degalų indeksą su vežėju.</span><span class="sxs-lookup"><span data-stu-id="ee84b-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="ee84b-105">Prieš paleisdami šį vadovą turite nustatyti vežėjo degalų indeksą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="ee84b-106">Norėdami tai padaryti, galite naudoti vadovą „Nustatyti vežėjo degalų indeksą“.</span><span class="sxs-lookup"><span data-stu-id="ee84b-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="ee84b-107">Šias nustatymo užduotis paprastai atlieka logistikos vadovas.</span><span class="sxs-lookup"><span data-stu-id="ee84b-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="ee84b-108">Kuriant šią procedūrą buvo naudojami USMF demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="ee84b-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="ee84b-109">Kurti papildomų paslaugų šabloną</span><span class="sxs-lookup"><span data-stu-id="ee84b-109">Create an accessorial master</span></span>
1. <span data-ttu-id="ee84b-110">Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Papildomų paslaugų šablonai.</span><span class="sxs-lookup"><span data-stu-id="ee84b-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="ee84b-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ee84b-111">Click New.</span></span>
3. <span data-ttu-id="ee84b-112">Lauke „Papildomų paslaugų šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee84b-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="ee84b-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee84b-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ee84b-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ee84b-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="ee84b-115">Kurti vežėjo papildomų paslaugų mokestį</span><span class="sxs-lookup"><span data-stu-id="ee84b-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="ee84b-116">Pasirinktie Transportavimo valdymas > Nustatymas > Vertinimas > Vežėjo papildomų paslaugų mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="ee84b-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="ee84b-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ee84b-117">Click New.</span></span>
3. <span data-ttu-id="ee84b-118">Lauke „Vežėjo papildomų paslaugų ID“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee84b-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="ee84b-119">Lauke „Siuntų vežėjas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ee84b-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ee84b-121">Šiame pavyzdyje pasirinkite „Sunkvežimio vežėjas“.</span><span class="sxs-lookup"><span data-stu-id="ee84b-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="ee84b-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee84b-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ee84b-123">Lauke „Vežėjo paslauga“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ee84b-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee84b-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ee84b-125">Lauke „Papildomų paslaugų šablonas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ee84b-126">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ee84b-127">Šiame pavyzdyje pasirinkite naujai sukurtą papildomų paslaugų šabloną.</span><span class="sxs-lookup"><span data-stu-id="ee84b-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="ee84b-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ee84b-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="ee84b-129">Kurti papildomų paslaugų priskyrimą</span><span class="sxs-lookup"><span data-stu-id="ee84b-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="ee84b-130">Spustelėkite „Papildomų paslaugų priskyrimai“.</span><span class="sxs-lookup"><span data-stu-id="ee84b-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="ee84b-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ee84b-131">Click New.</span></span>
3. <span data-ttu-id="ee84b-132">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee84b-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ee84b-133">Perjunkite skyriaus „Kriterijai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="ee84b-134">Kriterijuose visada galite taikyti papildomą degalų mokestį arba šiame pavyzdyje galite pasirinkti, kad jis būtų taikomas tik tam tikrame regione.</span><span class="sxs-lookup"><span data-stu-id="ee84b-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="ee84b-135">Lauke „Pašto kodas iš“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee84b-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="ee84b-136">Lauke „Pašto kodas į“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee84b-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="ee84b-137">Perjunkite skyriaus „Skaičiavimas“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="ee84b-138">Skaičiavimo skyriuje galite nurodyti, kaip skaičiuoti papildomą degalų mokestį.</span><span class="sxs-lookup"><span data-stu-id="ee84b-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="ee84b-139">Šis skaičiavimas priklauso nuo papildomų paslaugų vieneto, kurį pasirinkote skaičiavimo pagrindu.</span><span class="sxs-lookup"><span data-stu-id="ee84b-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="ee84b-140">Lauke „Mokesčio už papildomas paslaugas tipas“ pasirinkite „Papildomas degalų mokestis“.</span><span class="sxs-lookup"><span data-stu-id="ee84b-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="ee84b-141">Lauke „Papildomų paslaugų vienetas“ pasirinkite „Kilometražas“.</span><span class="sxs-lookup"><span data-stu-id="ee84b-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="ee84b-142">Lauke „Regionas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ee84b-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee84b-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ee84b-144">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ee84b-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="ee84b-145">Atnaujinti vežėjo vertinimo profilį</span><span class="sxs-lookup"><span data-stu-id="ee84b-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="ee84b-146">Pasirinkite Transportavimo valdymas > Nustatymas > Vežėjai > Siuntų vežėjai.</span><span class="sxs-lookup"><span data-stu-id="ee84b-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="ee84b-147">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ee84b-148">Perjunkite skyriaus „Vertinimo šablonai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="ee84b-149">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="ee84b-149">Click Edit.</span></span>
5. <span data-ttu-id="ee84b-150">Lauke „Vežėjo degalų indeksas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee84b-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ee84b-151">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee84b-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ee84b-152">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ee84b-152">Click Save.</span></span>

