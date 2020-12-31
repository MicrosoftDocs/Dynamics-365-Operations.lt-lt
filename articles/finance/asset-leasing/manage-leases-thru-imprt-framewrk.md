---
title: Nuomų valdymas per nuomos importavimo sistemą
description: Šioje temoje paaiškinama, kaip naudoti nuomos importavimo sistemą siekiant pakoreguoti kelias nuomos sutartis tuo pačiu metu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d7a7d2afd8f352bc167ec8c0a354ee4ac0a9e77b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446197"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="dfd89-103">Nuomų valdymas per nuomos importavimo sistemą</span><span class="sxs-lookup"><span data-stu-id="dfd89-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfd89-104">Šioje temoje paaiškinama, kaip naudoti nuomos importavimo sistemą siekiant pakoreguoti kelias nuomos sutartis vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="dfd89-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="dfd89-105">Naudodami šią funkciją galite sutaupyti laiko ir taip pat galite užtikrinti tikslesnius koregavimus, sumažindami žmogiškosios klaidos galimybę.</span><span class="sxs-lookup"><span data-stu-id="dfd89-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="dfd89-106">Be to, ši funkcija gali sujungti „Microsoft Dynamics 365 Finance“ su išoriniais duomenų subjektais, kad galėtų veiksmingai įkelti duomenis.</span><span class="sxs-lookup"><span data-stu-id="dfd89-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="dfd89-107">Gali būti naudojami šie duomenų objektai, siekiant integruoti turto nuomą su išorinėmis sistemomis.</span><span class="sxs-lookup"><span data-stu-id="dfd89-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="dfd89-108">Nuomos paruošimas</span><span class="sxs-lookup"><span data-stu-id="dfd89-108">Lease staging</span></span>
- <span data-ttu-id="dfd89-109">Mokėjimo sutarties sudarymas</span><span class="sxs-lookup"><span data-stu-id="dfd89-109">Payment contract staging</span></span>
- <span data-ttu-id="dfd89-110">Vykdomosios sutarties paruošimas</span><span class="sxs-lookup"><span data-stu-id="dfd89-110">Executory contract staging</span></span>

<span data-ttu-id="dfd89-111">Galite naudoti importavimo procesą, norėdami koreguoti nuomą, atnaujinti nefinansinę informaciją arba pridėti naujų nuomos išlaidų.</span><span class="sxs-lookup"><span data-stu-id="dfd89-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="dfd89-112">Galite peržiūrėti ir redaguoti nuomos duomenis prieš juos importuodami.</span><span class="sxs-lookup"><span data-stu-id="dfd89-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="dfd89-113">Sistema gali vykdyti šiuos tris procesus, naudodama nuomos importavimo paketą.</span><span class="sxs-lookup"><span data-stu-id="dfd89-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="dfd89-114">Proceso tipas</span><span class="sxs-lookup"><span data-stu-id="dfd89-114">Process type</span></span>  | <span data-ttu-id="dfd89-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="dfd89-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="dfd89-116">Pridėti įrašą</span><span class="sxs-lookup"><span data-stu-id="dfd89-116">Add record</span></span>    | <span data-ttu-id="dfd89-117">Perkelta nuoma, kurios proceso tipas yra šis, sukuria nuomą sistemoje.</span><span class="sxs-lookup"><span data-stu-id="dfd89-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="dfd89-118">Kad būtų galima patvirtinti mokėjimus, turi būti patvirtinta neautomatiniu būdu, o pradinis pripažinimo žurnalo įrašas turi būti registruojamas neautomatiniu būdu po perkėlimo.</span><span class="sxs-lookup"><span data-stu-id="dfd89-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="dfd89-119">Atnaujinti įrašą</span><span class="sxs-lookup"><span data-stu-id="dfd89-119">Update record</span></span> | <span data-ttu-id="dfd89-120">Perkelta nuomos sutartis, kurios šio proceso tipo atnaujinimo lauko vertės jau yra sistemoje.</span><span class="sxs-lookup"><span data-stu-id="dfd89-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="dfd89-121">Atnaujinami tik tie laukai, kurie pasirinkti puslapyje **Atnaujinimo laukų pasirinkimas**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="dfd89-122">Rekomenduojame pasirinkti nefinansinius laukus puslapyje **Atnaujinimo laukų pasirinkimas**, nes šio proceso tipas nekoreguoja nuomos.</span><span class="sxs-lookup"><span data-stu-id="dfd89-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="dfd89-123">Koreguoti įrašą</span><span class="sxs-lookup"><span data-stu-id="dfd89-123">Adjust record</span></span> | <span data-ttu-id="dfd89-124">Perkelta nuoma, kurios proceso tipas yra šis, koreguoja nuomą.</span><span class="sxs-lookup"><span data-stu-id="dfd89-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="dfd89-125">Dėl šio pakeitimo finansinė nuoma keičiama.</span><span class="sxs-lookup"><span data-stu-id="dfd89-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="dfd89-126">Po to, kai nuoma apdorojama, sistema sukuria naują įmokų grafiką naudodama naujus duomenis iš nuomos importavimo paketo.</span><span class="sxs-lookup"><span data-stu-id="dfd89-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="dfd89-127">Sistema nepatvirtina darbo grafiko arba įrašo pataisymų žurnalo įrašą.</span><span class="sxs-lookup"><span data-stu-id="dfd89-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="dfd89-128">Po to, kai informacija įkeliama naudojant darbo sritį **Duomenų valdymas**, atidarykite puslapį **Importavimo antraštė** (**Turto nuoma \> Nuomos importavimo sistema \> Importavimo antraštė**).</span><span class="sxs-lookup"><span data-stu-id="dfd89-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="dfd89-129">Šiame puslapyje pateikiami visi anksčiau nurodyti trys duomenų objektai.</span><span class="sxs-lookup"><span data-stu-id="dfd89-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="dfd89-130">Norėdami peržiūrėti nuomos išdėstymo duomenis prieš vykdydami apdorojimą, pasirinkite **Išdėstymo duomenys**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="dfd89-131">Funkcija lyginti leidžia palyginti įrašą, kurį importuojate, su atitinkamu įrašu, kuris jau yra jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="dfd89-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="dfd89-132">Norėdami palyginti atskirą nuomos įrašą, pasirinkite nuomą ir pasirinkite **Lyginti**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="dfd89-133">Turite atlikti šį veiksmą, kad būtų sugeneruota ataskaita **Skirtumai**, prieš perkeldami nuomos įrašus.</span><span class="sxs-lookup"><span data-stu-id="dfd89-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="dfd89-134">Funkcija lyginti sulygina išdėstymo duomenų vertes su nuomos, kuri šiuo metu yra sistemoje, vertėmis.</span><span class="sxs-lookup"><span data-stu-id="dfd89-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="dfd89-135">Funkcija Lyginti neveikia, jei nuomos proceso tipas yra **Įtraukti įrašą**, nes nėra ką lyginti su šia nuoma.</span><span class="sxs-lookup"><span data-stu-id="dfd89-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="dfd89-136">Norėdami palyginti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Periodiškai \> Palyginimas** ir pasirinkite **Lyginti**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="dfd89-137">Kiekvienam objektui galite peržiūrėti skirtumus tarp to, kas šiuo metu yra sistemoje, ir kas yra išdėstymo lentelėse.</span><span class="sxs-lookup"><span data-stu-id="dfd89-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="dfd89-138">Kiekvienam išdėstymo lentelės objektui pasirinkite **Peržiūrėti skirtumus**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="dfd89-139">Pasirodys dialogo langas, rodantis dabartinę vertę ir siūlomą išdėstymo vertę.</span><span class="sxs-lookup"><span data-stu-id="dfd89-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="dfd89-140">Taip pat galite atnaujinti išdėstymo vertę pakeisdami ją stulpelyje **Nauja reikšmė** ir tada pasirinkdami **Atnaujinti išdėstymą**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="dfd89-141">Norėdami užtikrinti, kad įrašus būtų galima įtraukti į sistemą neįkeliant klaidų, galite patvirtinti nuomą.</span><span class="sxs-lookup"><span data-stu-id="dfd89-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="dfd89-142">Prieš perkeliant nuomos įrašą, sistema vykdo kelis tikrinimus, siekdama užtikrinti, kad įrašas bus sėkmingai importuotas.</span><span class="sxs-lookup"><span data-stu-id="dfd89-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="dfd89-143">Norėdami patikrinti atskirą nuomą, pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="dfd89-144">Norėdami patikrinti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Periodiškai \> Tikrinimas** ir pasirinkite **Lyginti**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="dfd89-145">Norėdami apdoroti atskirą nuomą, puslapyje **Importavimo antraštė** pasirinkite **Perkelti nuomos įrašus**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="dfd89-146">Kai perkeliama nuoma, sistema atlieka veiksmą, kuris nurodytas lauke **Proceso tipas**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="dfd89-147">Norėdami patikrinti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Periodiškai \> Tikrinimas** ir pasirinkite **Lyginti**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="dfd89-148">Palyginus nuomas, galite vykdyti ataskaitą, kad peržiūrėtumėte kiekvienos nuomos, įtrauktos į importavimo ID, skirtumus.</span><span class="sxs-lookup"><span data-stu-id="dfd89-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="dfd89-149">Norėdami paleisti vienos nuomos ataskaitą, pasirinkite nuomos duomenis, o tada pasirinkite **Lyginti ir peržiūrėti ataskaitą \> Skirtumų ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="dfd89-150">Norėdami patikrinti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Užklausos ir ataskaitos \> Skirtumų ataskaita** ir pasirinkite **Lyginti**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="dfd89-151">Atnaujinamų laukų nustatymas</span><span class="sxs-lookup"><span data-stu-id="dfd89-151">Set up update fields</span></span>

<span data-ttu-id="dfd89-152">Jei naudojate nuomos importavimo sistemą norėdami atnaujinti nuomą, o proceso tipas yra **Atnaujinti įrašą**, galite pasirinkti konkrečius atnaujintinus laukus.</span><span class="sxs-lookup"><span data-stu-id="dfd89-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="dfd89-153">Pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Sąranka \> Atnaujinimo laukų pasirinkimas**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="dfd89-154">Pasirodžiusiame puslapyje pasirinkite atnaujintus laukus ir pasirinkite žalią rodyklę, kad perkeltumėte jas į sąrašą **Pasirinkti laukai**.</span><span class="sxs-lookup"><span data-stu-id="dfd89-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="dfd89-155">Tik sąrašo **Pasirinkti laukai** laukai gali būti atnaujinami naudojant nuomos importavimo paketą.</span><span class="sxs-lookup"><span data-stu-id="dfd89-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>
