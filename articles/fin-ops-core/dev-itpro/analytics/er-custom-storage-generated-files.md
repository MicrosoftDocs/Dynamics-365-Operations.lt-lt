---
title: Pasirinktinės saugyklos vietos sugeneruotiems dokumentams nurodymas
description: Šioje temoje paaiškinama, kaip išplėsti elektroninio ataskaitų (ER) formatų sugeneruotų dokumentų saugojimo vietų sąrašą.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 146e7fb5fefbecabc99c2978b52eb0e782da0322
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562219"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="1e4b3-103">Pasirinktinės saugyklos vietos sugeneruotiems dokumentams nurodymas</span><span class="sxs-lookup"><span data-stu-id="1e4b3-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1e4b3-104">Elektroninių ataskaitų (ER) sistemos programavimo sąsaja (API) suteikia galimybę išplėsti ER formatų sugeneruotų dokumentų saugojimo vietų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="1e4b3-105">Šioje temoje paaiškinama, kaip pridėti pasirinktines sugeneruotų dokumentų saugojimo vietas, pavedant atlikti užduotį kurti ER paskirties vietas numatytoje paskirties gamykloje ir tada įdiegti pasirinktinę klasę, kurios paskirties logika yra.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e4b3-106">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="1e4b3-106">Prerequisites</span></span>

<span data-ttu-id="1e4b3-107">Diekite topologiją, kuri palaiko nuolatinę komponavimo versiją.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="1e4b3-108">Daugiau informacijos žr. [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir testavimo automatizavimo funkciją, diegimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="1e4b3-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="1e4b3-109">Taip pat vienam iš toliau nurodytų vaidmenų reikia prieigos prie šios topologijos.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="1e4b3-110">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="1e4b3-110">Electronic reporting developer</span></span>
- <span data-ttu-id="1e4b3-111">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="1e4b3-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="1e4b3-112">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="1e4b3-112">System administrator</span></span>

<span data-ttu-id="1e4b3-113">Taip pat jums reikia prieigos prie šios topologijos kūrimo aplinkos.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="1e4b3-114">Visos užduotys šioje temoje gali būti atliktos naudojant **USMF** įmonę.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="1e4b3-115">Ilgalaikio turto keitimų taikymas ER formatu</span><span class="sxs-lookup"><span data-stu-id="1e4b3-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="1e4b3-116">Norėdami sugeneruoti dokumentus, kuriems planuojate pridėti pasirinktinę saugojimo vietą, [importuokite](er-download-configurations-global-repo.md) **ilgalaikio turto keitimų taikymo** ER formato konfigūraciją į dabartinę topologiją.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Konfigūracijos saugyklos puslapis](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="1e4b3-118">Ilgalaikio turto keitimų taikymo ataskaitos vykdymas</span><span class="sxs-lookup"><span data-stu-id="1e4b3-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="1e4b3-119">Pasirinkite **Ilgalaikis turtas** \> **Užklausos ir ataskaitos** \> **Operacijų ataskaitos** \> **Ilgalaikio turto keitimų taikymas**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="1e4b3-120">Lauke **Pradžios data** įveskite **2017-01-01** (2017 m. sausio 1 d.).</span><span class="sxs-lookup"><span data-stu-id="1e4b3-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="1e4b3-121">Lauke **Pabaigos data** įveskite **2017-01-31** (2017 m. sausio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="1e4b3-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="1e4b3-122">Lauke **Valiuta** pasirinkite **Apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="1e4b3-123">Lauke **Formato konvertavimas** pasirinkite **Ilgalaikio turto keitimų taikymas**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="1e4b3-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-124">Select **OK**.</span></span>

![Ilgalaikio turto keitimų taikymo ataskaitos vykdymo dialogo langas](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="1e4b3-126">Programoje „Microsoft Excel“ peržiūrėkite siunčiamą dokumentą, kurį sugeneruoja ir kurį galima atsisiųsti.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="1e4b3-127">Tai yra [numatytoji](electronic-reporting-destinations.md#default-behavior) ER formato, kurio [paskirties vietos](electronic-reporting-destinations.md) besukonfigūruotos ir kuris veikia interaktyviuoju režimu, elgsena.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="1e4b3-128">Šaltinio kodo peržiūra</span><span class="sxs-lookup"><span data-stu-id="1e4b3-128">Review the source code</span></span>

<span data-ttu-id="1e4b3-129">Peržiūrėkite klasės `AssetRollForwardService` metodo `generateReportByGER()` kodą.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="1e4b3-130">Atkreipkite dėmesį, kad `Run()` metodas naudojamas iškviesti ER sistemą ir generuoti ataskaitą **Ilgalaikio turto keitimų taikymas**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="1e4b3-131">Šaltinio kodo modifikavimas</span><span class="sxs-lookup"><span data-stu-id="1e4b3-131">Modify the source code</span></span>

1. <span data-ttu-id="1e4b3-132">Savo „Visual Studio“ projekte pridėkite naują klasę (`AssetRollForwardDestination` šiame pavyzdyje) ir įrašykite kodą, kad būtų galima vykdyti sugeneruotų **ilgalaikio turto keitimo taikymo** ataskaitų pasirinktinę paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="1e4b3-133">`new()` metodas sukurtas tam, kad būtų galima gauti pradinį objekto ER paskirties objektą ir programos logiką – valdomą parametrą, kuris nurodo pasirinktinę vietą, kur turi būti saugomos sugeneruotos ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="1e4b3-134">Šiame pavyzdyje tinkinama vieta yra serverio, kuriame veikia programos objektų serverio (AOS) paslauga, vietinės failų sistemos aplanko pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="1e4b3-135">`saveFile()` metodas sukurtas siekiant išsaugoti sugeneruotą dokumentą serverio, kuriame paleista AOS tarnyba, vietinės failų sistemos aplanke.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="1e4b3-136">Savo „Visual Studio“ projekte pridėkite naują klasę (`AssetRollForwardDestinationFactory` šiame pavyzdyje) ir įveskite kodą, kad nustatytumėte pasirinktinę paskirties gamyklą, kuri leidžia kurti paskirties vietą numatytoje paskirties gamykloje, ir suvynioti failo paskirties vietą su savo paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="1e4b3-137">Modifikuokite esamą `AssetRollForwardService` klasę ir rašykite kodą, kad būtų galima nustatyti pasirinktinę paskirties gamyklos ataskaitos vykdytoją.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="1e4b3-138">Atkreipkite dėmesį, kad sukūrus pasirinktinę paskirties gamyklą, į programą orientuotas parametras, nurodantis paskirties aplanką.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="1e4b3-139">Tokiu būdu šis tikslinis aplankas naudojamas, kad būtų saugomi sugeneruoti failai.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="1e4b3-140">Įsitikinkite, kad nurodytas aplankas (**c:\\0** šiame pavyzdyje) yra vietiniame failų sistemos serveryje, kuris paleidžia AOS tarnybą.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="1e4b3-141">Kitu atveju išimtis [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) bus pateikta vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="1e4b3-142">Perkurkite savo projektą.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="1e4b3-143">Ilgalaikio turto keitimų taikymo ataskaitos pakartotinis vykdymas</span><span class="sxs-lookup"><span data-stu-id="1e4b3-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="1e4b3-144">Pasirinkite **Ilgalaikis turtas** \> **Užklausos ir ataskaitos** \> **Operacijų ataskaitos** \> **Ilgalaikio turto keitimų taikymas**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="1e4b3-145">Lauke **Pradžios data** įveskite **2017-01-01**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="1e4b3-146">Lauke **Pabaigos data** įveskite **2017-01-31**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="1e4b3-147">Lauke **Valiuta** pasirinkite **Apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="1e4b3-148">Lauke **Formato konvertavimas** pasirinkite **Ilgalaikio turto keitimų taikymas**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="1e4b3-149">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-149">Select **OK**.</span></span>
7. <span data-ttu-id="1e4b3-150">Naršykite sugeneruotą failą aplanke **C:\\0**.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="1e4b3-151">Kadangi `originDestination` objektas nėra naudojamas `AssetRollForwardDestination` šiame pavyzdyje pateiktame objekte, tai, kad būtų galima nepaisyti vykdymo proceso vietos, ER formato [paskirties vietose](electronic-reporting-destinations.md) esančios konfigūracijos bus ignoruojamos.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e4b3-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1e4b3-152">Additional resources</span></span>

- [<span data-ttu-id="1e4b3-153">Elektroninių ataskaitų (ER) paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="1e4b3-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="1e4b3-154">Išplečiamumo pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="1e4b3-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]