---
title: „Dataverse“ integravimo konfigūravimas
description: Galite įjungti arba išjungti integravimą tarp „Microsoft Dataverse“ ir „Dynamics 365 Human Resources“. Galite taip pat peržiūrėti sinchronizavimo išsamią informaciją, pašalinti sekimo duomenis ir iš naujo sinchronizuoti lentelę siekiant padėti pašalinti duomenų problemas tarp dviejų aplinkų.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890033"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="432b2-104">„Dataverse“ integravimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="432b2-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="432b2-105">Galite įjungti arba išjungti integravimą tarp „Microsoft Dataverse“ ir „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="432b2-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="432b2-106">Galite taip pat peržiūrėti sinchronizavimo išsamią informaciją, panaikinti sekimo duomenis ir iš naujo sinchronizuoti lentelę, kad padėtumėte šalinti duomenų problemas tarp dviejų aplinkų.</span><span class="sxs-lookup"><span data-stu-id="432b2-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="432b2-107">Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="432b2-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="432b2-108">Kai išjungiate integravimą, vartotojai gali vykdyti „Human Resources“ arba „Dataverse“ keitimus, tačiau tie keitimai nėra sinchronizuojami tarp dviejų aplinkų.</span><span class="sxs-lookup"><span data-stu-id="432b2-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="432b2-109">Pagal numatytuosius parametrus duomenų integravimas tarp „Human Resources“ ir „Dataverse“ yra išjungtas.</span><span class="sxs-lookup"><span data-stu-id="432b2-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="432b2-110">Galbūt norėsite išjungti integravimą šiais atvejais:</span><span class="sxs-lookup"><span data-stu-id="432b2-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="432b2-111">Jūs užpildote duomenis naudodami duomenų valdymo sistemą ir turite importuoti duomenis kelis kartus, kad jie taptų tinkamos būsenos.</span><span class="sxs-lookup"><span data-stu-id="432b2-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="432b2-112">Yra problemų, susijusių su duomenimis, esančiais „Human Resources“ arba „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="432b2-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="432b2-113">Jei išjungsite integravimą, galite panaikinti įrašą vienoje aplinkoje, jo nepanaikindami kitoje.</span><span class="sxs-lookup"><span data-stu-id="432b2-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="432b2-114">Kai vėl įjungsite integraciją, įrašas aplinkoje, kurioje jis nebuvo panaikintas, sinchronizuojamas atgal į aplinką, kur jis buvo panaikintas.</span><span class="sxs-lookup"><span data-stu-id="432b2-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="432b2-115">Sinchronizavimas prasideda, kai kitą kartą paleidžiama paketinė užduotis **„Dataverse“ integravimo praleistų užklausų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="432b2-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="432b2-116">Kai išjungiate duomenų integravimą, įsitikinkite, kad neredaguojate to paties įrašo abiejose aplinkose.</span><span class="sxs-lookup"><span data-stu-id="432b2-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="432b2-117">Kai vėl įjungsite integravimą, paskutinis redaguotas įrašas bus sinchronizuojamas.</span><span class="sxs-lookup"><span data-stu-id="432b2-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="432b2-118">Todėl, jei abiejose aplinkose neatliekate tų pačių keitimų, gali būti prarasti duomenys.</span><span class="sxs-lookup"><span data-stu-id="432b2-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="432b2-119">Prieiga prie „Dataverse“ integravimo puslapio</span><span class="sxs-lookup"><span data-stu-id="432b2-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="432b2-120">„Human Resources“ egzemplioriuje, kur norite peržiūrėti arba konfigūruoti parametrus integravimui su „Dataverse“, pasirinkite plytelę **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="432b2-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="432b2-121">[![Plytelė Sistemos administravimas](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="432b2-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="432b2-122">Pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="432b2-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="432b2-123">[![Saitų skirtukas](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="432b2-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="432b2-124">Dalyje **Integravimai** pasirinkite **„Dataverse“ konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="432b2-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="432b2-125">[![„Dataverse“ konfigūracijos saitas](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="432b2-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="432b2-126">Duomenų integravimo tarp „Human Resources“ ir „Dataverse“ įjungimas ir išjungimas</span><span class="sxs-lookup"><span data-stu-id="432b2-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="432b2-127">Norėdami įjungti integravimą, nustatykite **Įjungti „Dataverse“ integravimo** parinktį į **Taip** **„Microsoft Dataverse“ integravimo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="432b2-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="432b2-128">Kai įjungiate integravimą, duomenys bus sinchronizuojami kitą kartą, kai vykdoma paketinė užduotis **„Dataverse“ integravimo praleistų užklausų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="432b2-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="432b2-129">Po to, kai paketinė užduotis bus baigta, visi duomenys turėtų būti pasiekiami.</span><span class="sxs-lookup"><span data-stu-id="432b2-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="432b2-130">Norėdami išjungti integravimą, nustatykite parinktį į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="432b2-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="432b2-131">[![„Dataverse“ integravimo įjungimas arba išjungimas](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="432b2-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="432b2-132">Primygtinai rekomenduojame išjungti „Dataverse“ integravimą atliekant duomenų perkėlimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="432b2-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="432b2-133">Dideli duomenų įkėlimai gali reikšmingai pabloginti veikimą.</span><span class="sxs-lookup"><span data-stu-id="432b2-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="432b2-134">Pavyzdžiui, 2000 darbuotojų atnaujinimas gali užimti kelias valandas, kol integravimas bus įjungtas ir mažiau nei valandą jo išjungimui.</span><span class="sxs-lookup"><span data-stu-id="432b2-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="432b2-135">Šiame pavyzdyje pateikti skaičiai yra tik demonstracijos tikslais.</span><span class="sxs-lookup"><span data-stu-id="432b2-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="432b2-136">Tikslus laiko kiekis įrašų importavimui gali labai skirtis priklausomai nuo daugybės faktorių.</span><span class="sxs-lookup"><span data-stu-id="432b2-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="432b2-137">Duomenų integravimo išsamios informacijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="432b2-137">View data integration details</span></span>

<span data-ttu-id="432b2-138">**Administravimo** „FastTab“ **„Microsoft Dataverse“ integravimo** puslapyje galite matyti, kaip eilutės yra susietas kartu tarp „Human Resources“ ir „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="432b2-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="432b2-139">Norėdami peržiūrėti eilutes, rinkitės lentelę **„Dataverse“ lentelės** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="432b2-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="432b2-140">Tinklelis rodo visas eilutes, kurios yra siejamos su pasirinkta lentele.</span><span class="sxs-lookup"><span data-stu-id="432b2-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="432b2-141">Ne visos „Dataverse“ lentelės dabar yra įtrauktos į sąrašą.</span><span class="sxs-lookup"><span data-stu-id="432b2-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="432b2-142">Tik lentelės, kurios palaiko tinkintų laukelių naudojimą pasirodys tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="432b2-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="432b2-143">Naujos lentelės taps prieinamos per nuolatinius „Human Resources“ leidimus.</span><span class="sxs-lookup"><span data-stu-id="432b2-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="432b2-144">Tinklelyje yra šie laukai:</span><span class="sxs-lookup"><span data-stu-id="432b2-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="432b2-145">**„Dataverse“ lentelė** – Lentelės pavadinimas „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="432b2-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="432b2-146">**„Dataverse“ nuoroda į lentelę** – Identifikatorius, kurį „Dataverse“ naudoja idenfitikuoti įrašą.</span><span class="sxs-lookup"><span data-stu-id="432b2-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="432b2-147">Ši vertė atitinka „Human Resources“ vertę **RecId**.</span><span class="sxs-lookup"><span data-stu-id="432b2-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="432b2-148">Galite rasti identifikatorių, kai atversite „Dataverse“ lentelę „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="432b2-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="432b2-149">**„Human Resources“ objekto pavadinimas** – „Human Resources“ objektas, kuris paskutinis sinchronizavimo duomenis į „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="432b2-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="432b2-150">Objektas gali būti arba „Dataverse“ priešvardis, arba kitas priešvardis.</span><span class="sxs-lookup"><span data-stu-id="432b2-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="432b2-151">**„Human Resources“ nuoroda** – **RecId** vertė, susieta su „Human Resources“ įrašu.</span><span class="sxs-lookup"><span data-stu-id="432b2-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="432b2-152">**Pašalintas iš „Dataverse“** – Vertė, kuri identifikuoja, ar eilutė buvo pašalinta iš „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="432b2-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="432b2-153">Įrašai „Human Resources“ atitinka eilutes „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="432b2-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="432b2-154">Pašalinkite „Human Resources“ sąsajos įrašą iš „Dataverse“ eilutės</span><span class="sxs-lookup"><span data-stu-id="432b2-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="432b2-155">Jei jums kyla problemų sinchronizuojant duomenis tarp „Human Resources“ ir „Dataverse”, galite jas išspręsti išvalydami sekimą ir leisdami iš naujo nustatyti sekimo lentelę.</span><span class="sxs-lookup"><span data-stu-id="432b2-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="432b2-156">Jei pašalinsite sąsają ir tada keisite ar naikinsite eilutę „Dataverse“, keitimai nebus sinchronizuojami „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="432b2-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="432b2-157">Jei darote keitimus „Human Resources“, naujas sekimo įrašas yra kuriamas ir eilutė yra naujinama „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="432b2-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="432b2-158">Pašalinkite „Human Resources“ sąsajos įrašą ir „Dataverse“eilutes pasirinkdami lentelę **„Dataverse“ lentelės** laukelyje ir tada rinkitės **Naikinti sekimo informaciją**.</span><span class="sxs-lookup"><span data-stu-id="432b2-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="432b2-159">[![Sekimo informacijos valymas](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="432b2-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="432b2-160">Norėdami vykdyti visą sinchronizavimą lentelėje, kai ištrinsite sekimą, žr. kitą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="432b2-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="432b2-161">Sinchronizuoti lentelę tarp „Human Resources“ ir „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="432b2-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="432b2-162">Naudokite šią procedūrą, kai:</span><span class="sxs-lookup"><span data-stu-id="432b2-162">Use this procedure when:</span></span>

- <span data-ttu-id="432b2-163">„Dataverse” keitimai atliekami per ilgai, kad būtų rodomi programoje „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="432b2-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="432b2-164">Išvalę sekimą turite atnaujinti sekimo lentelę.</span><span class="sxs-lookup"><span data-stu-id="432b2-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="432b2-165">Norėdami vykdyti visą sinchronizavimą lentelėje tarp „Human Resources“ ir „Dataverse“:</span><span class="sxs-lookup"><span data-stu-id="432b2-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="432b2-166">Rinkitės lentelę **„Dataverse“ lentelės** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="432b2-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="432b2-167">Pasirinkite **Sinchronizuoti dabar**.</span><span class="sxs-lookup"><span data-stu-id="432b2-167">Select **Sync now**.</span></span>

<span data-ttu-id="432b2-168">[![Visiško sinchronizavimo paleidimas](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="432b2-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="432b2-169">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="432b2-169">See also</span></span>

[<span data-ttu-id="432b2-170">„Dataverse“ lentelės</span><span class="sxs-lookup"><span data-stu-id="432b2-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="432b2-171">Konfigūruokite „Dataverse“ virtualias lenteles</span><span class="sxs-lookup"><span data-stu-id="432b2-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="432b2-172">„Human Resources“ virtualių lentelių DUK</span><span class="sxs-lookup"><span data-stu-id="432b2-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="432b2-173">Kas yra „Microsoft Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="432b2-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="432b2-174">Terminologijos naujinimai</span><span class="sxs-lookup"><span data-stu-id="432b2-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]