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
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Pasirinktinės saugyklos vietos sugeneruotiems dokumentams nurodymas

[!include[banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) sistemos programavimo sąsaja (API) suteikia galimybę išplėsti ER formatų sugeneruotų dokumentų saugojimo vietų sąrašą. Šioje temoje paaiškinama, kaip pridėti pasirinktines sugeneruotų dokumentų saugojimo vietas, pavedant atlikti užduotį kurti ER paskirties vietas numatytoje paskirties gamykloje ir tada įdiegti pasirinktinę klasę, kurios paskirties logika yra.

## <a name="prerequisites"></a>Būtinieji komponentai

Diekite topologiją, kuri palaiko nuolatinę komponavimo versiją. Daugiau informacijos žr. [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir testavimo automatizavimo funkciją, diegimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Taip pat vienam iš toliau nurodytų vaidmenų reikia prieigos prie šios topologijos.

- Elektroninės ataskaitos kūrėjas
- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Taip pat jums reikia prieigos prie šios topologijos kūrimo aplinkos.

Visos užduotys šioje temoje gali būti atliktos naudojant **USMF** įmonę.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Ilgalaikio turto keitimų taikymas ER formatu

Norėdami sugeneruoti dokumentus, kuriems planuojate pridėti pasirinktinę saugojimo vietą, [importuokite](er-download-configurations-global-repo.md) **ilgalaikio turto keitimų taikymo** ER formato konfigūraciją į dabartinę topologiją.

![Konfigūracijos saugyklos puslapis](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Ilgalaikio turto keitimų taikymo ataskaitos vykdymas

1. Pasirinkite **Ilgalaikis turtas** \> **Užklausos ir ataskaitos** \> **Operacijų ataskaitos** \> **Ilgalaikio turto keitimų taikymas**.
2. Lauke **Pradžios data** įveskite **2017-01-01** (2017 m. sausio 1 d.).
3. Lauke **Pabaigos data** įveskite **2017-01-31** (2017 m. sausio 31 d.).
4. Lauke **Valiuta** pasirinkite **Apskaitos valiuta**.
5. Lauke **Formato konvertavimas** pasirinkite **Ilgalaikio turto keitimų taikymas**.
6. Pasirinkite **Gerai**.

![Ilgalaikio turto keitimų taikymo ataskaitos vykdymo dialogo langas](./media/er-custom-storage-generated-files-runtime-dialog.png)

Programoje „Microsoft Excel“ peržiūrėkite siunčiamą dokumentą, kurį sugeneruoja ir kurį galima atsisiųsti. Tai yra [numatytoji](electronic-reporting-destinations.md#default-behavior) ER formato, kurio [paskirties vietos](electronic-reporting-destinations.md) besukonfigūruotos ir kuris veikia interaktyviuoju režimu, elgsena.

## <a name="review-the-source-code"></a>Šaltinio kodo peržiūra

Peržiūrėkite klasės `AssetRollForwardService` metodo `generateReportByGER()` kodą. Atkreipkite dėmesį, kad `Run()` metodas naudojamas iškviesti ER sistemą ir generuoti ataskaitą **Ilgalaikio turto keitimų taikymas**.

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

## <a name="modify-the-source-code"></a>Šaltinio kodo modifikavimas

1. Savo „Visual Studio“ projekte pridėkite naują klasę (`AssetRollForwardDestination` šiame pavyzdyje) ir įrašykite kodą, kad būtų galima vykdyti sugeneruotų **ilgalaikio turto keitimo taikymo** ataskaitų pasirinktinę paskirties vietą.

    - `new()` metodas sukurtas tam, kad būtų galima gauti pradinį objekto ER paskirties objektą ir programos logiką – valdomą parametrą, kuris nurodo pasirinktinę vietą, kur turi būti saugomos sugeneruotos ataskaitos. Šiame pavyzdyje tinkinama vieta yra serverio, kuriame veikia programos objektų serverio (AOS) paslauga, vietinės failų sistemos aplanko pavadinimas.
    - `saveFile()` metodas sukurtas siekiant išsaugoti sugeneruotą dokumentą serverio, kuriame paleista AOS tarnyba, vietinės failų sistemos aplanke.

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

2. Savo „Visual Studio“ projekte pridėkite naują klasę (`AssetRollForwardDestinationFactory` šiame pavyzdyje) ir įveskite kodą, kad nustatytumėte pasirinktinę paskirties gamyklą, kuri leidžia kurti paskirties vietą numatytoje paskirties gamykloje, ir suvynioti failo paskirties vietą su savo paskirties vieta.

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

3. Modifikuokite esamą `AssetRollForwardService` klasę ir rašykite kodą, kad būtų galima nustatyti pasirinktinę paskirties gamyklos ataskaitos vykdytoją. Atkreipkite dėmesį, kad sukūrus pasirinktinę paskirties gamyklą, į programą orientuotas parametras, nurodantis paskirties aplanką. Tokiu būdu šis tikslinis aplankas naudojamas, kad būtų saugomi sugeneruoti failai.

    > [!NOTE] 
    > Įsitikinkite, kad nurodytas aplankas (**c:\\0** šiame pavyzdyje) yra vietiniame failų sistemos serveryje, kuris paleidžia AOS tarnybą. Kitu atveju išimtis [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) bus pateikta vykdymo metu.

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

4. Perkurkite savo projektą.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Ilgalaikio turto keitimų taikymo ataskaitos pakartotinis vykdymas

1. Pasirinkite **Ilgalaikis turtas** \> **Užklausos ir ataskaitos** \> **Operacijų ataskaitos** \> **Ilgalaikio turto keitimų taikymas**.
2. Lauke **Pradžios data** įveskite **2017-01-01**.
3. Lauke **Pabaigos data** įveskite **2017-01-31**.
4. Lauke **Valiuta** pasirinkite **Apskaitos valiuta**.
5. Lauke **Formato konvertavimas** pasirinkite **Ilgalaikio turto keitimų taikymas**.
6. Pasirinkite **Gerai**.
7. Naršykite sugeneruotą failą aplanke **C:\\0**.

> [!NOTE]
> Kadangi `originDestination` objektas nėra naudojamas `AssetRollForwardDestination` šiame pavyzdyje pateiktame objekte, tai, kad būtų galima nepaisyti vykdymo proceso vietos, ER formato [paskirties vietose](electronic-reporting-destinations.md) esančios konfigūracijos bus ignoruojamos.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)
- [Išplečiamumo pagrindinis puslapis](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]