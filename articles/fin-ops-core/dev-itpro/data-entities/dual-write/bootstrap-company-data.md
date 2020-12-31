---
title: DUK apie perkrovimą naudojant įmonės duomenis
description: Kaip, prieš įjungiant dvigubo rašymo ryšį, perkrauti „Dataverse“ ar kitų „Dynamics 365“ programų duomenis su įmonės informacija.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 8cd753a5b0d63833a911e0692c83c653e0278153
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683776"
---
# <a name="bootstrap-with-company-data-faq"></a><span data-ttu-id="c690e-103">DUK apie perkrovimą naudojant įmonės duomenis</span><span class="sxs-lookup"><span data-stu-id="c690e-103">Bootstrap with company data FAQ</span></span>
 
[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="why-do-i-need-bootstrapping"></a><span data-ttu-id="c690e-104">Kodėl man reikalinga perkrovimo funkcija?</span><span class="sxs-lookup"><span data-stu-id="c690e-104">Why do I need bootstrapping?</span></span> 
<span data-ttu-id="c690e-105">Galbūt turite „Dataverse“ ar kitos „Dynamics 365“ programos egzempliorių su verslo duomenimis ir norite įjungti dvigubo rašymo ryšį su jais.</span><span class="sxs-lookup"><span data-stu-id="c690e-105">You might have an existing Dataverse or other Dynamics 365 app instance with business data, and you want to enable dual-write connection against it.</span></span> <span data-ttu-id="c690e-106">Tokiu atveju prieš įjungdami dvigubo rašymo ryšį turite perkrauti „Dataverse“ ar kitų „Dynamics 365“ programų duomenis su įmonės informacija.</span><span class="sxs-lookup"><span data-stu-id="c690e-106">In this case, you need to bootstrap Dataverse or other Dynamics 365 app data with company information before enabling dual-write connection.</span></span>  
 
## <a name="when-should-i-use-bootstrapping"></a><span data-ttu-id="c690e-107">Kada reikėtų naudoti perkrovimo funkciją?</span><span class="sxs-lookup"><span data-stu-id="c690e-107">When should I use bootstrapping?</span></span> 
<span data-ttu-id="c690e-108">Įjungti dvigubo rašymo funkciją reikėtų prieš įjungiant lentelių schemas (atliekant 5-ąjį veiksmą).</span><span class="sxs-lookup"><span data-stu-id="c690e-108">You should use bootstrapping before enabling dual-write table maps (during step #5).</span></span>  
1. <span data-ttu-id="c690e-109">Norėdami nustatyti dvigubo rašymo ryšį tarp savo „Finance and Operations“ programos ir „ Dataverse“ ar kitos „Dynamics 365“ programos egzempliorių, kaip administratorius prisijunkite prie „Finance and Operations“ programos.</span><span class="sxs-lookup"><span data-stu-id="c690e-109">To setup the dual-write connection between instances of your Finance and Operations app and the Dataverse or other Dynamics 365 app, log in to the Finance and Operations app as an administrator.</span></span> 
2. <span data-ttu-id="c690e-110">Nueikite į modulį **Duomenų valdymas** ir spustelėkite mygtuką **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="c690e-110">Go to the **Data Management** module and click the **Dual-Write** button.</span></span> <span data-ttu-id="c690e-111">Taip paleidžiamas **duomenų integratorius**.</span><span class="sxs-lookup"><span data-stu-id="c690e-111">This launches the **Data Integrator**.</span></span> 
3. <span data-ttu-id="c690e-112">Sukurkite dvigubo rašymo ryšį vienai ar kelioms įmonėms.</span><span class="sxs-lookup"><span data-stu-id="c690e-112">Create the dual-write connection for one or more companies.</span></span>  
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="c690e-113">![Dvigubo rašymo ryšio kūrimas](media/dual-write-boot-1.png)</span><span class="sxs-lookup"><span data-stu-id="c690e-113">![Create dual-write connection](media/dual-write-boot-1.png)</span></span>
4. <span data-ttu-id="c690e-114">Įjunkite lentelės schemą **Cdm_companies**.</span><span class="sxs-lookup"><span data-stu-id="c690e-114">Enable the **Cdm_companies** table map.</span></span> <span data-ttu-id="c690e-115">Tai sinchronizuoja įmones iš „Finance and Operations“ programos į „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="c690e-115">This synchronizes companies from the Finance and Operations app to Dataverse.</span></span>  
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="c690e-116">![Lentelės schemos įjungimas](media/dual-write-boot-2.png)</span><span class="sxs-lookup"><span data-stu-id="c690e-116">![Enable the table map](media/dual-write-boot-2.png)</span></span>
5. <span data-ttu-id="c690e-117">„Dataverse“ ar kitos „Dynamics 365“ programos egzemplioriuje vykdykite perkrovimo kodo pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="c690e-117">Run the sample bootstrapping code on the Dataverse or other Dynamics 365 app instance.</span></span>  
6. <span data-ttu-id="c690e-118">Kai baigiama perkrauti ir sistema parengta tiesiogiai sinchronizuoti, įjunkite lentelių schemas.</span><span class="sxs-lookup"><span data-stu-id="c690e-118">When the bootstrapping is done and the system is ready for the live sync, enable the table maps.</span></span>  

    <span data-ttu-id="c690e-119">Įjungus lentelių schemas, suaktyvinamas pradinis įjungtų lentelių schemų duomenų sinchronizavimas.</span><span class="sxs-lookup"><span data-stu-id="c690e-119">Enabling the table maps triggers the initial data sync for the enabled table maps.</span></span> <span data-ttu-id="c690e-120">Tarp „Finance and Operations“ programos ir „Dataverse“ sinchronizuojami atitinkami įmonių, kurioms parinktas dvigubo rašymo ryšys, duomenys.</span><span class="sxs-lookup"><span data-stu-id="c690e-120">The data corresponding to the companies chosen on the dual-write connection is synchronized between the Finance and Operations app and Dataverse.</span></span> 
 
## <a name="how-to-i-use-the-code-sample"></a><span data-ttu-id="c690e-121">Kaip naudoti kodo pavyzdį?</span><span class="sxs-lookup"><span data-stu-id="c690e-121">How to I use the code sample?</span></span>
<span data-ttu-id="c690e-122">Pavyzdžio kodas yra C# programa, kurią galite įkelti į „Visual Studio“.</span><span class="sxs-lookup"><span data-stu-id="c690e-122">The sample code is a C# application that you can load in Visual Studio.</span></span> <span data-ttu-id="c690e-123">Pasitelkiamos „NuGet“ paketo „Dataverse“ SDK priklausomybės, kurias galite atnaujinti naudodami standartinius „Visual Studio“ įrankius.</span><span class="sxs-lookup"><span data-stu-id="c690e-123">It takes NuGet package dependencies on the Dataverse SDK, that you can refresh through standard Visual Studio tooling.</span></span> 

<span data-ttu-id="c690e-124">Sprendimą išskleidę ir atidarę „Visual Studio“ aplinkoje bei atkūrę „NuGet“ paketus, kode ieškokite **TODO**.</span><span class="sxs-lookup"><span data-stu-id="c690e-124">After unzipping and opening the solution in Visual Studio and restoring the NuGet packages, search for **TODO** in the code.</span></span> <span data-ttu-id="c690e-125">Kiekvienas turimas priimti sprendimas dėl įmonės informacijos perkrovimo būdo pažymėtas fraze **TODO**; taip pat pateiktas kodo pavyzdys, skirtas įdiegti kanoniškai.</span><span class="sxs-lookup"><span data-stu-id="c690e-125">Each decision you need to make about how you want to bootstrap company information is noted by a **TODO**, with sample code for a canonical implementation.</span></span> 

<span data-ttu-id="c690e-126">Kodo pavyzdžiu parodytas tik vienas iš daugybės būdų, kuriuos naudodami lentelių eilutes galite suskirstyti pagal įmonę.</span><span class="sxs-lookup"><span data-stu-id="c690e-126">The sample code shows only one of many ways you might categorize entity rows by company.</span></span> <span data-ttu-id="c690e-127">Keisdami skyriuose **TODO** pateiktą logiką, galite sukurti savo pasirinktinį suskirstymą.</span><span class="sxs-lookup"><span data-stu-id="c690e-127">By changing the logic in the **TODO** sections, you can create your custom categorization.</span></span> 
 
## <a name="what-should-i-expect"></a><span data-ttu-id="c690e-128">Ko reikėtų tikėtis?</span><span class="sxs-lookup"><span data-stu-id="c690e-128">What should I expect?</span></span>
<span data-ttu-id="c690e-129">Pagal numatytuosius parametrus pavyzdžio programoje galite pateikti verslo struktūros vienetų ir įmonės kodo sąsajų žodyną.</span><span class="sxs-lookup"><span data-stu-id="c690e-129">By default, the sample application lets you provide a dictionary of business unit-to-company code mappings.</span></span> <span data-ttu-id="c690e-130">Bet kuris objektas, kurį perkraunate naudodami lauką **OwningBusinessUnit**, automatiškai nustatomas naudoti nurodytą įmonę.</span><span class="sxs-lookup"><span data-stu-id="c690e-130">Any entity you bootstrap with an **OwningBusinessUnit** field is automatically set to use the specified company.</span></span> <span data-ttu-id="c690e-131">Objektui be lauko **OwningBusinessUnit**, pvz., produktui, įmonė bus nustatoma pagal sąsają su tuščia verslo struktūros vieneto reikšme.</span><span class="sxs-lookup"><span data-stu-id="c690e-131">Any entity without an **OwningBusinessUnit** field, such as product, will set the company based on the mapping with an empty business unit value.</span></span>

<span data-ttu-id="c690e-132">Konsolės programa tikisi vieno parametro – **–simulate** arba **–apply**.</span><span class="sxs-lookup"><span data-stu-id="c690e-132">The console application expects one parameter, either **–simulate** or **–apply**.</span></span> <span data-ttu-id="c690e-133">Jei naudojate komandų eilutės parametrą **–simulate**, neatnaujinami jokie duomenys.</span><span class="sxs-lookup"><span data-stu-id="c690e-133">If you use the **–simulate** command line parameter, then no data is updated.</span></span> <span data-ttu-id="c690e-134">Tame pačiame kataloge, kaip įrankis, generuojami tik **simulation_<entityname>.csv** failai, po vieną kiekvienam objektui, kuris būtų buvęs atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="c690e-134">Only **simulation_<entityname>.csv** files are generated in the same directory as the tool, one for each entity that would have been updated.</span></span> <span data-ttu-id="c690e-135">Dirbdami šiuos failus galite pakartotinai peržiūrėti, kad užtikrintumėte, jog kodas įmonės reikšmes atnaujina taip, kaip tikimasi.</span><span class="sxs-lookup"><span data-stu-id="c690e-135">You can iteratively review these files while working to ensure the code updates company values as expected.</span></span> 

<span data-ttu-id="c690e-136">Baigę dirbti su modeliuojamais naujinimais, naudokite parametrą **–apply**.</span><span class="sxs-lookup"><span data-stu-id="c690e-136">When you finish with the simulated updates, then use the **–apply** parameter.</span></span> <span data-ttu-id="c690e-137">Taip atnaujinamos visos eilutės, kuriose šiuo metu yra neteisinga įmonės reikšmė – paketomis po 1000 eilučių vienu metu (pagal numatytuosius parametrus).</span><span class="sxs-lookup"><span data-stu-id="c690e-137">This updates all rows that currently have an incorrect company value, in batches of 1000 rows at a time (by default).</span></span> <span data-ttu-id="c690e-138">Kodas pateikiamas su unikalumo patikrinimo funkcija – tai reiškia, kad galite jį vykdyti pakartotinai ir bus atnaujintos tik neteisingai priskirtos įmonės.</span><span class="sxs-lookup"><span data-stu-id="c690e-138">The code is idempotent as provided, meaning you can re-run it and only the incorrectly assigned companies will be updated.</span></span> <span data-ttu-id="c690e-139">Vykdomas su **–apply**, kodas generuoja atliktų pakeitimų CSV failus, kurie pavadinti **applied_<entityname>.csv**,</span><span class="sxs-lookup"><span data-stu-id="c690e-139">When running with **–apply**, the code outputs CSV files of the changes made, which are named **applied_<entityname>.csv**.</span></span> 

 ```csharp
 using Microsoft.Crm.Sdk.Messages;
using Microsoft.Xrm.Sdk;
using Microsoft.Xrm.Sdk.Messages;
using Microsoft.Xrm.Sdk.Query;
using Microsoft.Xrm.Tooling.Connector;
using System;
using System.Collections.Generic;
using System.Diagnostics;
using System.IO;

namespace BootstrapCompany
{
    /// <summary>
    /// Application to bootstrap the company field on existing rows in CDS in preparation for integration to Finance and Operations.
    /// </summary>
    /// <remarks>
    /// This application assumes that the target companies already exist in the CDS environment in the cdm_Company table and are
    /// identified by their company code. It also assumes that the current owning business unit of each row should be used
    /// to categorize by company. This logic can easily be updated to utilize alternate sources of categorization including
    /// custom tables, teams, custom fields on tables, or any other data. This code is provided only as a sample. 
    /// 
    /// To utilize this code, update each of the locations currently denoted with a TODO statement.
    /// 
    /// This code is provided AS IS with no warranties or guarantees, and confers no rights.
    /// </remarks>
    public class Program
    {
        /// <summary>
        /// The number of rows to query and update in CDS in a single operation.
        /// </summary>
        /// <remarks>
        /// The larger this number, the fewer calls will need to be made, so the faster the updates
        /// will complete. However, larger batch sizes are more likely to cause contention. Additionally,
        /// when SQL exceeds some threshold of locks (generally around 5,000), it will escalate to
        /// an entire table lock, which blocks all other activity in the live system on this table. As 
        /// such, a batch size of around 1,000 is relatively fast, while also relatively safe in terms
        /// of contention and transaction time.
        /// </remarks>
        const int requestBatchSize = 1000;

        /// <summary>
        /// The number of faults that may be seen in CDS before the operation is aborted and an exception is thrown.
        /// </summary>
        /// <remarks>
        /// An occassional error due to contention when updating large tables in production is expected, so by default
        /// errors are logged and skipped. However, if a large number of errors are seen, ignoring those errors
        /// in subsequent batches gets expensive, and is usually indicative of a larger issue that should be addressed
        /// before continuing. Faulted requests are *not* retried, but would be picked up in a subsequent run of this script.
        /// </remarks>
        const int maxFaultThreshold = 100;

        /// <summary>
        /// The maximum number of rows per business unit to export when simulating.
        /// </summary>
        /// <remarks>
        /// During simulation, queries are not batched since doing so would require ordering and so be slightly
        /// different from the actual execution logic. To keep this the same between both paths, simulates are
        /// not batched and so a separate maximum number of rows per business unit can be specified.
        /// </remarks>
        const int maxSimulateRecordsPerBusinessUnit = 10000;

        /// <summary>
        /// Whether or not operations should continue if any errors are encountered.
        /// </summary>
        /// <remarks>
        /// This is different than setting maxFaultThreshold = 0, since the first batch of updates will be processed
        /// together. If continueOnError is true and maxFaultThreshold is 0, it is possible that multiple errors may
        /// be encountered and at the same time some rows successfully updated. In a healthy system when updating
        /// a higher number of rows, an occasional spurious error is expected, so it is recommended this be left as true.
        /// </remarks>
        const bool continueOnError = true;

        #region private variables
        private static Dictionary<string, EntityReference> cachedCompanyReferences = new Dictionary<string, EntityReference>();
        #endregion

        /// <summary>
        /// The main execution loop of the program.
        /// </summary>
        /// <param name="args">No arguments are expected.</param>
        static void Main(string[] args)
        {
            if (args.Length != 1 && args[0] != "-simulate" && args[0] != "-apply")
            {
                Console.WriteLine("Usage: BootstrapCompany -simulate");
                Console.WriteLine("       BootstrapCompany -apply");
                Console.WriteLine("The -simulate flag will create a file called simulation.csv in the working");
                Console.WriteLine("directory, but will not change any data. The -apply flag will update live data");
                Console.WriteLine("in the same way that was demonstrated in the simulation.");

                return;
            }

            bool isSimulate = args[0].Equals("-simulate", StringComparison.OrdinalIgnoreCase);

            // Delete the simulation or applied files if existing
            foreach (string existingSimulate in Directory.EnumerateFiles(Directory.GetCurrentDirectory(), $"{(isSimulate ? "simulation" : "applied")}_*.csv"))
            {
                File.Delete(existingSimulate);
            }

            IOrganizationService orgService;

            // TODO: Provide your connection string details for your environment
            CrmServiceClient cdsConnection = new CrmServiceClient("AuthType=Office365;Username=youraliashere@yourdomainhere.com;Password=yourpasswordhere;URL=https://yourorganizationurlhere.crm.dynamics.com/;");
            orgService = (IOrganizationService)cdsConnection.OrganizationWebProxyClient != null ? (IOrganizationService)cdsConnection.OrganizationWebProxyClient : (IOrganizationService)cdsConnection.OrganizationServiceProxy;

            if (orgService != null)
            {
                // Get the current user ID to verify the connection was successful
                Guid userid = ((WhoAmIResponse)orgService.Execute(new WhoAmIRequest())).UserId;

                if (userid != Guid.Empty)
                {
                    Console.WriteLine("Connection Successful!");
                }

                // TODO: Provide a mapping of OwningBusinessUnit name to cdm_Company company ID. You can reuse
                // the same company ID for multiple business units if desired. In this example, it assumes that
                // the business unit named "USMF" is related to the company "USMF". If all rows were owned
                // by the same root business unit, then the first field in the dictionary should be set to the 
                // name of the root business unit, usually the same value as the organization (eg, "Contoso").
                Dictionary<string, string> businessUnitToCompanyMapping = new Dictionary<string, string>()
                {
                    { "", "USMF" }, // The default mapping to use for any entity that doesn't have an owningbusinessunit field
                    { "USMF", "USMF" },
                    { "FRRT", "FRRT" },
                };

                // TODO: Provide a list of tables for which the company field should be backfilled based
                // on owning business unit. The list below represents all existing tables for which a cdm_Company
                // lookup field was added as part of the Finance and Operations dual write project.
                BatchUpdateEntity(orgService, "account", "msdyn_company", businessUnitToCompanyMapping, true, isSimulate, "accountnumber", "name");
                BatchUpdateEntity(orgService, "contact", "msdyn_company", businessUnitToCompanyMapping, true, isSimulate, "fullname");
                // ... Add more here

                // Note, the product entity does not have an owningbusinessunit field like most other tables, so
                // assigning company by Business Unit is not applicable. In this case, whichever mapping specifies an
                // empty business unit will be used to categorize tables without an owningbusinessunit field.
                BatchUpdateEntity(orgService, "product", "msdyn_companyid", businessUnitToCompanyMapping, false, isSimulate, "productnumber");
            }
            else
            {
                Console.WriteLine("Connection failed...");
            }

            Console.WriteLine("Done");
            Console.ReadLine();
        }

        /// <summary>
        /// Updates all incorrectly assigned company relationships for the specified entity.
        /// </summary>
        /// <param name="orgService">The connection to CDS.</param>
        /// <param name="entityName">The logical name of the entity to update.</param>
        /// <param name="companyFieldName">The physical name of the field in the entity being updated which contains the cdm_Company id.</param>
        /// <param name="businessUnitToCompanyMapping">A dictionary of business unit name to company code.</param>
        /// <param name="hasOwningBusinessUnit">true if the entity has an owningbusinessunit field; otherwise, false.</param>
        /// <param name="isSimulate">true to simulate output; otherwise, false.</param>
        /// <param name="fieldsToExport">A set of fields to export into a CSV for this entity if simulating.</param>
        /// <returns>true if the entity was successfully processed without any errors; otherwise, false.</returns>
        private static bool BatchUpdateEntity(
            IOrganizationService orgService, 
            string entityName, 
            string companyFieldName, 
            Dictionary<string, string> businessUnitToCompanyMapping, 
            bool hasOwningBusinessUnit, 
            bool isSimulate, 
            params string[] fieldsToExport)
        {
            List<Guid> faultedIds = new List<Guid>();
            int totalRecordsProcessed = 0;
            Stopwatch stopwatch = new Stopwatch();
            stopwatch.Start();

            string fileName = isSimulate ? "simulation" : "applied";
            StreamWriter simulationWriter = new StreamWriter(Path.Combine(Directory.GetCurrentDirectory(), $"{fileName}_{entityName}.csv"), true);
            simulationWriter.Write("EntityName,EntityId,");
            foreach (string fieldToExport in fieldsToExport)
            {
                simulationWriter.Write($"{fieldToExport},");
            }
            simulationWriter.WriteLine("BusinessUnit,NewCompanyId");

            // Process each mapped business unit individually
            foreach (string businessUnitName in businessUnitToCompanyMapping.Keys)
            {
                Console.WriteLine("Updating any {0} rows for business unit {1} to company {2}...", entityName, businessUnitName, businessUnitToCompanyMapping[businessUnitName]);

                // The empty business unit value is only applicable for tables without an owning business unit field
                if (hasOwningBusinessUnit && string.IsNullOrEmpty(businessUnitName))
                {
                    continue;
                }
                else if (!hasOwningBusinessUnit && !string.IsNullOrEmpty(businessUnitName))
                {
                    continue;
                }

                var companyRef = GetCompanyReference(orgService, businessUnitToCompanyMapping[businessUnitName]);

                // Iteratively loop in batches to keep transaction lock size small
                bool moreRecordsExist = true;

                while (moreRecordsExist)
                {
                    moreRecordsExist = false;

                    // Find the first batch of rows for this business unit with the wrong company ID. Ordering
                    // is not explicity specified, but SQL will most likely process based on the index starting with
                    // company ID, since all new company ID fields added for Finance and Operations integration have
                    // also added a new index starting with company ID. Explicitly specifying order would reduce the
                    // query plan options for SQL and introduce unnecessary overhead.
                    QueryExpression query = new QueryExpression(entityName);
                    query.ColumnSet.AddColumns(companyFieldName);
                    foreach (string fieldToExport in fieldsToExport)
                    {
                        query.ColumnSet.AddColumn(fieldToExport);
                    }
                    query.Criteria.AddCondition(companyFieldName, ConditionOperator.NotEqual, companyRef.Id);

                    // TODO: Uncomment the line below if you only want to fill in companies that are empty
                    // as opposed to the line above which updates the company any time it differs from the 
                    // desired value
                    // query.Criteria.AddCondition(companyFieldName, ConditionOperator.Equal, Guid.Empty);

                    if (isSimulate)
                    {
                        // During simulation, get as a single block of rows to avoid positioning complexities
                        query.TopCount = maxSimulateRecordsPerBusinessUnit;
                    }
                    else
                    {
                        // Only batch rows during actual application, otherwise retrieve all as a single operation
                        query.TopCount = requestBatchSize + faultedIds.Count;
                    }

                    // For tables with an owning business unit, join based on business unit name
                    if (hasOwningBusinessUnit)
                    {
                        // TODO: Replace this logic with different algorithms to determine the correct company
                        // in situations where business unit is not the best way to categorize.
                        LinkEntity linkEntity = query.AddLink("businessunit", "owningbusinessunit", "businessunitid", JoinOperator.Inner);
                        linkEntity.Columns.AddColumns("name");
                        linkEntity.LinkCriteria.AddCondition("name", ConditionOperator.Equal, businessUnitName);
                    }

                    var multipleRequest = new ExecuteMultipleRequest()
                    {
                        Settings = new ExecuteMultipleSettings()
                        {
                            ContinueOnError = true,
                            ReturnResponses = true
                        },
                        Requests = new OrganizationRequestCollection()
                    };

                    EntityCollection result = orgService.RetrieveMultiple(query);

                    int rowsAddedToBatch = 0;

                    foreach (var entity in result.Entities)
                    {
                        // Skip any previously faulted ID's. These values will be re-queried with each batch
                        // which is inefficient, but is more efficient than passing hundreds of ID values to 
                        // the underlying SQL query to be skipped at the database level (assuming the 
                        // max fault count is relatively small).
                        if (faultedIds.Contains(entity.Id))
                        {
                            continue;
                        }

                        entity.Attributes[companyFieldName] = companyRef;
                        
                        UpdateRequest updateRequest = new UpdateRequest()
                        {
                            Target = entity
                        };

                        simulationWriter.Write($"{entityName},{entity.Id},");
                        foreach (string fieldToExport in fieldsToExport)
                        {
                            simulationWriter.Write($"{entity.Attributes[fieldToExport]},");
                        }
                        simulationWriter.WriteLine($"{businessUnitName},{businessUnitToCompanyMapping[businessUnitName]}");

                        // Only add the update request when applying for real
                        if (!isSimulate)
                        {
                            multipleRequest.Requests.Add(updateRequest);
                        }

                        rowsAddedToBatch++;
                        Console.Write(".");
                    }

                    totalRecordsProcessed += rowsAddedToBatch;

                    if (rowsAddedToBatch > 0 && !isSimulate)
                    {
                        Console.Write("Sending {0} updates in a batch", rowsAddedToBatch);
                        var updateResult = orgService.Execute(multipleRequest) as ExecuteMultipleResponse;
                        moreRecordsExist = true;
                        Console.WriteLine(" done");

                        // If any faults are encountered, flag those IDs to not be processed again
                        // in subsequent batches.
                        if (updateResult.IsFaulted)
                        {
                            foreach (var response in updateResult.Responses)
                            {
                                if (response.Fault != null)
                                {
                                    Console.WriteLine(response.Fault);
                                    faultedIds.Add(((UpdateRequest)multipleRequest.Requests[response.RequestIndex]).Target.Id);

                                    if (faultedIds.Count > 100)
                                    {
                                        throw new ApplicationException("Excessive number of update failures, aborting operation");
                                    }
                                }
                            }
                        }
                    }
                    else
                    {
                        Console.WriteLine("No {0} rows remain to be updated for {1}->{2}", entityName, businessUnitName, businessUnitToCompanyMapping[businessUnitName]);
                    }
                }
            }

            simulationWriter.Close();
            simulationWriter = null;

            stopwatch.Stop();
            Console.WriteLine("Processed {0} rows for the {1} entity in {2}ms.", totalRecordsProcessed, entityName, stopwatch.ElapsedMilliseconds);

            return (faultedIds.Count == 0);
        }

        /// <summary>
        /// Gets an entity reference to the company with the specified ID if one exists.
        /// </summary>
        /// <param name="orgService">The CDS connection.</param>
        /// <param name="companyId">The company ID to search for.</param>
        /// <returns>An entity reference if one exists; otherwise, null.</returns>
        private static EntityReference GetCompanyReference(IOrganizationService orgService, string companyId)
        {
            if (cachedCompanyReferences.ContainsKey(companyId))
            {
                return cachedCompanyReferences[companyId];
            }

            QueryExpression query = new QueryExpression("cdm_company");
            query.ColumnSet.AddColumns("cdm_companyid");
            query.Criteria.AddCondition("cdm_companycode", ConditionOperator.Equal, companyId);
            query.TopCount = 1;

            EntityCollection result = orgService.RetrieveMultiple(query);

            EntityReference entityRef = null;

            foreach (var entity in result.Entities)
            {
                entityRef = entity.ToEntityReference();
                break;
            }

            cachedCompanyReferences[companyId] = entityRef;

            return entityRef;
        }
    }
}

 ```
 
 
