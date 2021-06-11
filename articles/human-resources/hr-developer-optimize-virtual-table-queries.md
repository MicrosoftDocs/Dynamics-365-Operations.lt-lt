---
title: „Dataverse“ virtualiųjų lentelių užklausų optimizavimas
description: „Dataverse” virtualiųjų lentelių užklausų efektyvumo optimizavimas ir trikčių diagnostika
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054913"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="288af-103">„Dataverse“ virtualiųjų lentelių užklausų optimizavimas</span><span class="sxs-lookup"><span data-stu-id="288af-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="288af-104">Problema</span><span class="sxs-lookup"><span data-stu-id="288af-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="288af-105">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="288af-105">Overview</span></span>

<span data-ttu-id="288af-106">Naudodami „Dataverse” virtualiąsias lenteles integravimų ir kitų duomenų ryšių su „Dynamics 365 Human Resources” vystymui, galite susidurti su užklausų pagal virtualiąsias lenteles efektyvumo problemomis.</span><span class="sxs-lookup"><span data-stu-id="288af-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="288af-107">Lėtas užklausų vykdymas gali atsitikti įvairiems klientams arba sąsajoms.</span><span class="sxs-lookup"><span data-stu-id="288af-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="288af-108">Pavyzdžiui, jums gali iškilti problemą šiomis sąlygomis:</span><span class="sxs-lookup"><span data-stu-id="288af-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="288af-109">Pateikiant virtualiosios lentelės užklausą per „Dataverse” Žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="288af-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="288af-110">Kuriant „Power App” pagal virtualiąją lentelę</span><span class="sxs-lookup"><span data-stu-id="288af-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="288af-111">Kuriant „Power BI” ataskaitą virtualioje lentelėje</span><span class="sxs-lookup"><span data-stu-id="288af-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="288af-112">Yra galimybė, kad visose šiose sąsajose iškils efektyvumo problema.</span><span class="sxs-lookup"><span data-stu-id="288af-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="288af-113">Viena iš lėto Personalo valdymui skirtų „Dataverse” virtualiųjų lentelių efektyvumo priežasčių yra su lentelės [naršymo ypatybėmis](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) susijusios virtualiosios lentelės išorinio rakto stulpeliai.</span><span class="sxs-lookup"><span data-stu-id="288af-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="288af-114">Kai virtualiajai lentelei sukuriamos naršymo ypatybės, išorinio rakto stulpelis automatiškai įtraukiamas į lentelę, kad būtų atspindima susijusios virtualiosios lentelės rakto stulpelio vertė.</span><span class="sxs-lookup"><span data-stu-id="288af-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="288af-115">Pavyzdžiui, stulpelis **„_mshr_fk_person_id_value”** yra įtraukiamas į **„mshr_hcmworkerbaseentity”** objektą naudojant išorinio rakto ypatybę iš **„mshr_dirpersonentity”** objekto.</span><span class="sxs-lookup"><span data-stu-id="288af-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="288af-116">Dėl to, kaip šių išorinio rakto stulpelių reikšmės yra tvarkomos lentelėje, reikšmių iškvietimas gali turėti neigiamos įtakos užklausos pagal virtualiąją lentelę efektyvumui.</span><span class="sxs-lookup"><span data-stu-id="288af-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="288af-117">Galimi požymiai</span><span class="sxs-lookup"><span data-stu-id="288af-117">Potential symptoms</span></span>

<span data-ttu-id="288af-118">Pavyzdys, kur galite pastebėti šį poveikį, yra užklausos pagal Darbuotojo (**„mshr_hcmworkerentity”**) arba Pagrindinio darbuotojo (**„mshr_hcmworkerbaseentity”**) objektą.</span><span class="sxs-lookup"><span data-stu-id="288af-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="288af-119">Galite pastebėti, kad efektyvumo problema pasireiškia keliais skirtingais būdais:</span><span class="sxs-lookup"><span data-stu-id="288af-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="288af-120">**Lėtas užklausos vykdymas**: Užklausą pagal virtualiąją lentelę gali pateikti tikėtuosius rezultatus, bet užtrukti daugiau laiko nei tikėtasi užklausos vykdymui užbaigti.</span><span class="sxs-lookup"><span data-stu-id="288af-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="288af-121">**Užklausos skirtasis laikas**: Užklausai gali baigtis skirtasis laikas ir būti grąžinama ši klaida: „Atpažinimo ženklas, skirtas iškviesti „Finance and Operations”, buvo gautas, bet „Finance and Operations” grąžino vidinę serverio klaidą („InternalServerError”).”</span><span class="sxs-lookup"><span data-stu-id="288af-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="288af-122">**Netikėta klaida**: Užklausa gali grąžinti 400 tipo klaidą su šiuo pranešimu: „Įvyko netikėta klaida.”</span><span class="sxs-lookup"><span data-stu-id="288af-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Klaidos tipas 400 „HcmWorkerBaseEntity” objekte](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="288af-124">**Buferizavimas**: Užklausa gali pernelyg daug naudoti serverio išteklius ir todėl patirti buferizavimą.</span><span class="sxs-lookup"><span data-stu-id="288af-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="288af-125">Tokiu atveju užklausa grąžina šią klaidą: „Buvo gautas atpažinimo ženklas „Finance and Operations” iškvietimui, tačiau „Finance and Operations” grąžino 429 tipo klaidą.”</span><span class="sxs-lookup"><span data-stu-id="288af-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="288af-126">Daugiau informacijos apie buferizavimą Personalo valdyme rasite [Buferizavimo DUK](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="288af-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Klaidos tipas 429 „HcmWorkerBaseEntity” objekte](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="288af-128">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="288af-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="288af-129">Į jūsų duomenų užklausą įtraukiamų stulpelių skaičiaus apribojimas</span><span class="sxs-lookup"><span data-stu-id="288af-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="288af-130">Naudojant virtualiąsias lenteles, vienas iš metodų, turinčių didžiausią potencialą pagerinti užklausų efektyvumą, yra riboti užklausoje pasirinktų stulpelių skaičių.</span><span class="sxs-lookup"><span data-stu-id="288af-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="288af-131">Bendrosios užklausos efektyvumo optimizavimo gairės yra riboti jūsų užklausoje grąžintų stulpelių skaičių tik iki jums reikalingų ypatybių.</span><span class="sxs-lookup"><span data-stu-id="288af-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="288af-132">Tai ypač pasakytina apie virtualiųjų lentelių išorinio rakto stulpelius.</span><span class="sxs-lookup"><span data-stu-id="288af-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="288af-133">Jeigu jūsų integravimui ar ataskaitai nereikia išorinio rakto stulpelių reikšmių, tada sukurkite užklausą, parenkančią tik tuos stulpelius, kurių jums reikia, išskyrus išorinio rakto stulpelius.</span><span class="sxs-lookup"><span data-stu-id="288af-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="288af-134">Stulpelių pasirinkimas „OData” užklausoje</span><span class="sxs-lookup"><span data-stu-id="288af-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="288af-135">Kai pateikiate virtualiosios lentelės užklausą per „Dataverse” Žiniatinklio API, galite apriboti į užklausą įtraukiamų stulpelių skaičių naudodami **„$select”** sistemos užklausos parinktį, ir apibrėžti stulpelius, kurių rezultatų jums turi būti grąžinami.</span><span class="sxs-lookup"><span data-stu-id="288af-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="288af-136">Norėdami maksimaliai padidinti efektyvumą, neįtraukite išorinio rakto stulpelių (su **_„mshr_FK”_** priešvardžiu) į užklausą.</span><span class="sxs-lookup"><span data-stu-id="288af-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="288af-137">Pavyzdžiui, ši užklausa pagal **„mshr_hcmworkerbaseentity”** objektą įtrauks tik į **„$select”** užklausos parinkties sąlygą įtrauktus stulpelius, išskyrus išorinio rakto reikšmes.</span><span class="sxs-lookup"><span data-stu-id="288af-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="288af-138">Tai labai pagerina užklausos, į kurią įtraukti visi lentelės stulpeliai, efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="288af-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="288af-139">Rekomendacija apriboti pasirinktų stulpelių skaičių taip pat taikoma, kai užklausos parinktis **„$expand”** naudojama užklausai išplėsti iki susijusių virtualiųjų lentelių per naršymo ypatybes.</span><span class="sxs-lookup"><span data-stu-id="288af-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="288af-140">Pavyzdžiui, šioje užklausoje yra stulpelių iš **„mshr_hcmworkerbaseentity”** objekto su išplėstiniais stulpeliais iš **„mshr_dirpersonentity”** objekto.</span><span class="sxs-lookup"><span data-stu-id="288af-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="288af-141">Atkreipkite dėmesį, kad užklausos parinktis **„$select”** taip pat yra įtraukta **„$expand”** užklausos parinkties sąlygą.</span><span class="sxs-lookup"><span data-stu-id="288af-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="288af-142">Naudojant šį duomenų gavimo metodą su užklausos parinktimi **„$select”** iš užklausos parinkties **„$expand”** sąlygos, turėtumėte pastebėti geresnį efektyvumą, kai naršymo ypatybė tarp objektų yra ryšys „daugelis su vienu”.</span><span class="sxs-lookup"><span data-stu-id="288af-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="288af-143">Galbūt nepamatysite tokio pat užklausos vykdymo laiko sumažėjimo, kai išplėsite ryšį „vienas su daugeliu”.</span><span class="sxs-lookup"><span data-stu-id="288af-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="288af-144">Daugiau informacijos apie „Dataverse” virtualiųjų lentelių ryšio apibrėžimą ieškokite [Lentelės ryšiai](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="288af-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="288af-145">Daugiau informacijos apie **„$select”** ir **„$expand”** sistemos užklausos parinktis, esančias „Dataverse” Žiniatinklio API, ieškokite [Susijusių objekto įrašų gavimas naudojant užklausą](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="288af-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="288af-146">Stulpelių pasirinkimas „Power BI” platformoje</span><span class="sxs-lookup"><span data-stu-id="288af-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="288af-147">Jei kurdami „Power BI” ataskaitą pagal „Dataverse” virtualiąją lentelę patiriate bet kurį iš anksčiau minėtų lėto efektyvumo požymių, galite pagerinti efektyvumą į ataskaitą neįtraukdami išorinio rakto stulpelių iš lentelėje pasirinktų stulpelių.</span><span class="sxs-lookup"><span data-stu-id="288af-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="288af-148">Pavyzdžiui, jei naudojate „Power BI Desktop” ataskaitos pagal **„mshr_hcmworkerbaseentity”** objektą kūrimui, galite naudoti tolesnius veiksmus stulpeliams, kuriuos norite įtraukti į ataskaitos užklausą, pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="288af-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="288af-149">„Power BI Desktop” pasirinkite **Daugiau...** iš **Gauti duomenis** išplečiamojo sąrašo, esančio veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="288af-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="288af-150">Lango **Gauti duomenis** ieškos lauke įveskite **„Common Data Service”**, pasirinkite **„Common Data Service”** jungtį, o tada – **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="288af-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="288af-151">„Common Data Service” lango lauke **Serverio Url** įveskite organizacijos URI jūsų „Dataverse” aplinkai ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="288af-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Jūsų „Dataverse” aplinkos URI pavadinimas](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="288af-153">Naršyklės lange išplėskite **Objektų** mazgą.</span><span class="sxs-lookup"><span data-stu-id="288af-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="288af-154">Ieškos lauke įveskite **„mshr_hcmworkerbaseentity”** ir pasirinkite objektą.</span><span class="sxs-lookup"><span data-stu-id="288af-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="288af-155">Pasirinkite **Transformuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="288af-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="288af-156">„Power Query“ rengyklės lange pasirinkite **Patobulinta rengyklė**.</span><span class="sxs-lookup"><span data-stu-id="288af-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="288af-157">Lange **Patobulinta rengyklė** atnaujinkite užklausą, kad ji atrodytų kaip žemiau, pridėdami arba pašalindami masyvo stulpelius taip, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="288af-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Užklausos atnaujinimas Patobulintoje rengyklėje, skirtoje „Power Query“ rengyklei](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="288af-159">Pasirinkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="288af-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="288af-160">Jeigu anksčiau gavote 429 tipo užklausos klaidą, jums gali reikėti palaukti kartojimo laikotarpio prieš atnaujinant užklausą, kad ji būtų sėkmingai baigta.</span><span class="sxs-lookup"><span data-stu-id="288af-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="288af-161">Paspauskite **Uždaryti & Taikyti** „Power Query“ rengyklės veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="288af-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="288af-162">Tada galėsite pradėti kurti „Power BI” ataskaitą pagal stulpelius, pasirinktus iš virtualiosios lentelės.</span><span class="sxs-lookup"><span data-stu-id="288af-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="288af-163">Stulpelių pasirinkimas „Power Apps” platformoje</span><span class="sxs-lookup"><span data-stu-id="288af-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="288af-164">Panašiai į „Dataverse” Žiniatinklio API užklausas ir „Power BI”, galite patobulinti „Power Apps” užklausų efektyvumą, pagrįstą „Dataverse” virtualiosiomis lentelėmis, neįtraukdami jūsų programos susijusių lentelių stulpelių.</span><span class="sxs-lookup"><span data-stu-id="288af-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="288af-165">Jei stulpeliai iš susijusios lentelės buvo įtraukti į puslapį, tada duomenų iškvietimui sukurtuose užklausų URL bus susijusios lentelės išorinio rakto ypatybės.</span><span class="sxs-lookup"><span data-stu-id="288af-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="288af-166">Tai, kaip ir aukščiau nurodyti [Stulpelių pasirinkimo „OData” užklausoje](#selecting-columns-in-power-apps) pavyzdžiai, sumažina efektyvumą dėl sukeltų papildomų duomenų peržvalgų.</span><span class="sxs-lookup"><span data-stu-id="288af-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="288af-167">Norėdami tai išspręsti, galite patikrinti, ar nei vienas duomenų laukas iš susijusių lentelių nebuvo įtrauktas į jokią jūsų „Power App” duomenų formą.</span><span class="sxs-lookup"><span data-stu-id="288af-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="288af-168">Medžio rodinio srityje pasirinkite duomenų formą ekranui.</span><span class="sxs-lookup"><span data-stu-id="288af-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="288af-169">Srityje **Ypatybės** pasirinkite **Redaguoti** ypatybei **Laukai**.</span><span class="sxs-lookup"><span data-stu-id="288af-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="288af-170">Srityje **Duomenys** patikrinkite, ar nei vienas iš pasirinktų laukų nėra duomenų šaltinio virtualiosios lentelės laukas.</span><span class="sxs-lookup"><span data-stu-id="288af-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="288af-171">Tarkim, jei vienas iš duomenų laukų, įtrauktų į programos puslapį, nurodo kitą lentelę, pavyzdžiui **„ThisItem.Worker.Name”**, kur **Darbuotojas** yra susijusi lentelė, tikėtina, kad duomenų efektyvumas gali sumažėti.</span><span class="sxs-lookup"><span data-stu-id="288af-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="288af-172">Galite naudoti [„Power Apps Monitor”](/powerapps/maker/monitor-overview), kad užtikrintumėte, jog tik jums reikalingi stulpeliai būtų įtraukti į užklausą, skirtą „Power App” duomenims gauti.</span><span class="sxs-lookup"><span data-stu-id="288af-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="288af-173">Galite peržiūrėti „getRows” (gauti eilutes) operacijai sukurtą URL, siekiant užtikrinti, kad jūsų pasirinkti stulpeliai programai bus optimalūs duomenims nuskaityti.</span><span class="sxs-lookup"><span data-stu-id="288af-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Naudokite „Power Apps Monitor” operacijai „getData” (gauti duomenis) analizuoti](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="288af-175">Duomenų užklausos filtravimas</span><span class="sxs-lookup"><span data-stu-id="288af-175">Filtering the data query</span></span>

<span data-ttu-id="288af-176">Kitas užklausų vykdymo efektyvumo metodas yra riboti užklausos rezultatuose grąžintų įrašų skaičių.</span><span class="sxs-lookup"><span data-stu-id="288af-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="288af-177">Tai galite atlikti filtruodami rezultatus ir taip užtikrindami, kad gaunate tik jums reikalingus įrašus.</span><span class="sxs-lookup"><span data-stu-id="288af-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="288af-178">Skaitykite [Filtravimo rezultatai](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) norėdami gauti daugiau informacijos apie užklausų duomenų filtravimą.</span><span class="sxs-lookup"><span data-stu-id="288af-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="288af-179">Užklausos puslapio dydžio ribojimas</span><span class="sxs-lookup"><span data-stu-id="288af-179">Limiting the page size of the query</span></span>

<span data-ttu-id="288af-180">Jei dirbate su dideliais duomenų rinkiniais, užklausų rezultatus galite padalinti į kelis puslapius pridėdami `odata.maxpagesize` nuostatos antraštę į duomenų užklausas.</span><span class="sxs-lookup"><span data-stu-id="288af-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="288af-181">Daugiau informacijos apie puslapių kaitą rasite [Puslapyje grąžinamų objektų skaičiaus nurodymas](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="288af-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="288af-182">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="288af-182">See also</span></span>

- [<span data-ttu-id="288af-183">Konfigūruokite „Dataverse“ virtualias lenteles</span><span class="sxs-lookup"><span data-stu-id="288af-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="288af-184">„Human Resources“ virtualiųjų lentelių DUK</span><span class="sxs-lookup"><span data-stu-id="288af-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="288af-185">Užklausų buferizavimo DUK</span><span class="sxs-lookup"><span data-stu-id="288af-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]