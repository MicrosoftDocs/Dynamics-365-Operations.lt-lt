---
title: Nustatyti alternatyvų rekomendacijų duomenų eigą
description: Šiame straipsnyje aprašoma, kaip konfigūruoti aplinką naudojant alternatyvią duomenų eigą, kad būtų pateikti duomenys pagal rekomendacijų tarnybą.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460106"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Nustatyti alternatyvų rekomendacijų duomenų eigą

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti aplinką naudojant alternatyvią duomenų eigą, kad būtų pateikti duomenys pagal rekomendacijų tarnybą.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Out-of-the dataflow palyginimas su alternatyvia duomenų srauto

Toliau pateiktame pavyzdyje vaizduojama duomenų srautai, kurie nėra duomenų srauto aplinkoje.

![Out-of-box duomenų eiga aplinkoje](media/reco-out-of-the-box-dataflow-2.png)

Šioje iliustracijoje parodyta alternatyvi duomenų eiga, kur objekto parduotuvės sinchronizavimo paketinė užduotis pakeičiama alternatyviais duomenų srauto veiksmais.

![Alternatyvi duomenų eiga aplinkoje](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Prielaidos

- Šiame straipsnyje laikoma, kad jau įgalinote jūsų aplinkos rekomendacijų paslaugą. Daugiau informacijos rasite Įgalinkite [produkto rekomendacijas](enable-product-recommendations.md).
- Kai dirbate su duomenų Apie saugojimo sąskaitos failais Microsoft Azure ir aplankais:

    - Galite naudoti "Azure" interneto portalo sąsają arba programą "Azure Storage Explorer".
    - Darbo su failais **ir aplankais pradžios taškai yra "dynamics365-financeandoperations** " konteineryje, kuris yra aplanke, kuris pavadintas, kad atitiktų jūsų aplinkos URL.
    - Jei jūsų sandbox aplinkos pavadinimas yra **MyUAT**, bus naudojamas aplinkos pagrindinis URL `myuat.sandbox.operations.dynamics.com`.
    - Jei prie to paties saugojimo abonemento prijungta daugiau nei viena aplinka, kiekviena aplinka turės savo šakninį aplanką.

## <a name="prerequisites"></a>Būtinieji komponentai

Kad būtų galima įdiegti alternatyvų duomenų srauto būdą, būtina įvykdyti toliau nurodytus būtinuosius komponentus.

### <a name="set-up-microsoft-power-platform"></a>Nustatyti Microsoft Power Platform

Norėdami nustatyti, Microsoft Power Platform vadovaukitės integravimo įjunkite [instrukcijas Microsoft Power Platform](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>Diegti eksportavimo į duomenų "Data" papildinę

Norėdami įdiegti papildinę "Eksportuoti į duomenis", vadovaukitės instrukcijomis, pateikiamomis ["Diegti eksportą į "Azure Data Azure" priedą](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Užsirašykite konfigūracijos vertes, nes jų prireiks kai kuriems toliau esantims žingsniams.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Lentelių konfigūravimas eksportuoti į "Dynamics 365"

Lentelės sinchronizavimas iš "Dynamics 365 Azure Data Lake Storage " į valdomas puslapyje **Eksportuoti į** duomenis. Kadangi šiame puslapyje šiuo metu nėra meniu elemento, jį atidaryti gali **tik sistemos administratoriaus** saugos vaidmens vartotojai.

Norėdami konfigūruoti lenteles, kurias reikia eksportuoti programoje "Dynamics 365", atlikite šiuos veiksmus.

1. Norėdami atidaryti puslapį **Eksportuoti į duomenų kaina**, `?mi=DataFeedsDefinitionWorkspace` pridėkite eilutę prie aplinkos pagrindinio URL, kaip parodyta šiame pavyzdyje:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Puslapyje Eksportuoti **į duomenis į "Skirtukas**[" ir kopijuokite šio straipsnio skyriuje RetailSales kubų lentelių](#list-of-retailsales-cube-tables) sąraše pateiktas lenteles.
1. Stulpelyje **Sistemos pavadinimas** išplėskite filtro pasirinkčių sąrašą.
1. Filtro tipui pasirinkti yra **vienas iš.** Tada perkelkite žymeklį į teksto lauką ir įklijuokite **lentelių, nukopijuotų iš puslapio Eksportuoti į duomenų lapą,** sąrašą.
1. Filtro pasirinkčių sąrašo apačioje pasirinkite **Taikyti**.
1. Pasirinkite visas tinklelio eilutes ir pasirinkite **Aktyvinti**.

> [!NOTE]
> Prieš pereidami prie kito veiksmo, visos eilutės turi būti atnaujintos į būseną **Vykdoma**. Jei reikia, pašalinkite ir išspręskite klaidas.

### <a name="create-a-synapse-workspace"></a>Sinapsės darbo srities kūrimas

Norėdami sukurti Sinapse darbo sritį, jei jos dar neturite, [vadovaukitės Sparčiosios paleisties instrukcijomis: Sukurkite Sinapse darbo sritį](/azure/synapse-analytics/quickstart-create-workspace).

Kad "Azure" ištekliai būtų sutvarkyti, rekomenduojame "Azure" išteklių grupėje įtraukti duomenų "Azure" saugyklos sąskaitą ir "Synapse" darbo sritį. Galite pakartotinai naudoti sukurtą saugojimo sąskaitą, kai įdiegėte eksportavimo į duomenų ryšio priedą.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Sukurti duomenų bazę Sinapse, kad būtų galima apdoroti rekomendacijų duomenis

Naudokite bendrosios duomenų modelio priemonės konsolės programą (CDMUtil_ConsoleApp), kad sukurtumėte duomenų bazę savo Sinapsės darbo srityje ir automatiškai užpildytumėte ją iš bendro duomenų modelio lentelių, kurios yra duomenų Laikmena. Mes rekomenduojame, kad jūs naudojate bendrosios duomenų modelio priemonę su savo duomenų baze programavimo aplinkoje, jei yra plėtinių.

> [!NOTE]
> Toliau pateikiami veiksmai reiškia, kad į "RetailSales" kubą nėra įtraukiama jokių plėtinių duomenų.

Norėdami sukurti duomenų bazę Sinapse, atlikite šiuos veiksmus.

1. Eikite [į Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) ir atlikite veiksmus, **norėdami atsisiųsti CDMUtilConsoleApp.zip** failą.
1. Išskleisti pašto failą į vietinį aplanką.
1. Atidarykite **CDMUtil_ConsoleApp.dll.config failą** teksto rengyklėje ir atnaujinkite šias vertes:

    1. Nustatykite nuomininko **ID vertę** ("Azure" nuomininko ID).
    1. Nustatykite **prieigos rakto** vertę (duomenų saugojimo sąskaitos prieigos raktą).

        1. "Azure" portale atidarykite savo saugojimo sąskaitą.
        1. Meniu, esančiame kairėje puslapio pusėje, pasirinkite Prieigos **raktus**.
        1. Puslapio viršuje pasirinkite Rodyti **raktus**.
        1. Pasirinkite vieno iš dviejų raktų laukų kopijavimo mygtuką ir į konfigūracijos faile įklijuokite vertę tarp dvigubo kabučių.

    1. Nustatykite **ManifestURL** reikšmę kaip failo **Tables.manifest.cdm.json** URL.Azure Data Lake Storage Norėdami gauti URL, naršykite prie failo "Azure" portale, pasirinkite elipsę (**...**), dešinėje rodinio pusėje, tada pasirinkite **Ypatybės**. URL yra pirmoji ypatybė, rodoma skirtuke **Peržiūra**.
    1. Nustatykite **TargetDbConnectionString** reikšmę kaip įtaisytojo serverio SQL telkinio, jūsų Sinapse darbo srities, ryšio eilutę.

        1. Sinapsės darbo srityje pasirinkite skirtuką **Valdyti**.
        1. Submeniu pasirinkite **SQL telkinius**.
        1. Pasirinkite įtaisyto **pavadinimo pavadinimą,** norėdami peržiūrėti telkinio ypatybes.
        1. Ypatybės dialogo lange pasirinkite ADO.NET norimą naudoti ryšio tipą. Tada nukopijuokite jungimosi eilutės vertę ir įklijuokite ją tarp konfigūracijos faile dvigubas kabutes.

        > [!NOTE]
        > Turite turėti teisę kurti duomenų bazes. Kad būtų lengviau naudotis, galite norėti naudoti integruotą sqladminuser **administratoriaus** abonementą.

    1. Išdėsto **ProcessEntities mazgą** ir nustatykite jo vertę kaip **teisingą** (pvz.`<add key="ProcessEntities" value ="true"/>`).

1. Įrašykite ir uždarykite **CDMUtil_ConsoleApp.dll.config** failą.
1. Nukopijuokite **failą EntityList.json** į / **Manifest katalogą**.
1. Komandinės eilutės lange vykdykite **cdmutil_consoleapp.exe**.

> [!NOTE]
> Peržiūrint išeigą, turėtų būti 35 objektai / rodiniai, mažiausiai 75 lentelės ir klaidų nėra.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Paruoškite duomenų Yra RetailSales su sujungti matavimų katalogą

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Kurti atsarginę dabartinio RetailSales kubo duomenų iš duomenų skelbimų saugyklos atsarginę kopijas

Paprasčiausias būdas sukurti atsarginę dabartinių RetailSales **kubo duomenų kopiją yra pervardyti katalogą RetailSales duomenų saugyklai RetailSales** **-** atsargine kopija ar kažkas panašiai. Jei vėliau reikės pašalinti trikčių šalinimą, šiuo metodu išsaugomi esami duomenys.

Kubo **aplanką /RetailSales** galima rasti šioje vietoje:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Kurti naują aplanką "RetailSales" ir įkelti modelio failą

Norėdami sukurti naują katalogą **RetailSales** ir įkelti **failą model.json** į duomenų saugyklą, atlikite šiuos veiksmus.

1. Sukurkite naują tuščią katalogą tame pačiame lygyje kaip ankstesnis katalogas ir pavadinkite jį **RetailSales**.
1. **Nusiųsti model.json** failą į naują katalogą.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Kurti pardavimo galimybes, siekiant nukopijuoti RetailSales kubo duomenis

Pardavimo galimybės perskaitys RetailSales kubo rodinius ir eksportuos duomenis į .csv failus Duomenų kaupime.

Norėdami sukurti pardavimo galimybes, kad būtų galima nukopijuoti RetailSales kubo duomenis, atlikite šiuos veiksmus.

1. Sinapsės darbo srityje pasirinkite skirtuką **Integruoti**.
1. Pasirinkite pliuso ženklą (**+**), tada pasirinkite Importuoti iš **pardavimo galimybių šablono**.
1. Atsisiųskite ir pasirinkite failą [ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files).
1. Pasirinkite su SQL duomenų baze susietą paslaugą.
1. Pasirinkite su saugojimo sąskaita susietą paslaugą.
1. Atidarykite **duomenų kopijavimo** įrankį ir pakeiskite aplanko **maršruto** ypatybę į **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Tikrinti pardavimo galimybių vykdymą

Rekomenduojame pardavimo galimybes išbandyti tik vienu rodinu. Šis **RetailSales_RetailMediaTemplateView** gerai, nes paprastai jame yra mažiau nei 10 eilučių.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Planuoti pardavimo galimybes, kurios bus paleisto pasikartojančiu grafiku

Kiekvieną kartą, kai veikia pardavimo galimybės, atsiranda "Azure" suvartojimas. Rekomenduojame suplanuoti vykdymą kas 48 valandas ar kas daugiau. Pardavimo galimybes visada galite vykdyti rankiniu būdu, jeigu duomenis reikia sinchronizuoti iš karto. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>"Dynamics 365" į duomenų saugyklas sinchronizavimo lentelių sąrašas

Toliau pateiktas lentelių sąrašas yra visų lentelių, reikalingų visam RetailSales kubui, subgrupė. Rekomendacijų tarnyba naudoja tik 15 RetailSales kubo peržiūrų ir pagal tai buvo išfiltruotas reikalingų lentelių sąrašas.

### <a name="list-of-retailsales-cube-tables"></a>RetailSales kubų lentelių sąrašas

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Katalogas
- Katalogo gamyba
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- „HcmWorker”
- Inventdim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE GRUPĘ
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIJOS HIERARCHIJA
- DIMENSIJOSHIERARCHYINTEGRATION
- DIMENSIJOSHIERARCHYLEVEL
- DIMENSIJOSPARAMETRAS
- OMExplodedOrganizationSecurity diagrama

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Peržiūrėti parametrų, kurie bus perduoti sinapse pardavimo galimybes, sąrašą

Toliau pateiktame kableliais atskirtų sąrašų yra RetailSales kubo rodinių, dėl kurių pardavimo galimybės atliks operaciją "pasirinkti". Tada ji kopijuos rezultatus į duomenų apie duomenų saugojimą.

RetailSales_RetailAssortmentRulesView, RetailSales_RetailChannelNavigationHierarchiesView, RetailSales_RetailChannelNavigationHierarchyCatalogProductsView, RetailSales_RetailChannelNavigationHierarchyCategoryNodesView, RetailSales_RetailChannelNavigationHierarchyCategoryProductsView, RetailSales_RetailMediaBaseUrlChannelView, RetailSales_RetailMediaRelativeUrlProductView, RetailSales_RetailMediaTemplateView, RetailSales_RetailOptOutCustomersView, RetailSales_RetailProductCategory, RetailSales_RetailProductTransaction, RetailSales_RetailProductVariantDimensionsView, RetailSales_RetailRecoListConfigurationParametersView, RetailSales_RetailRecoListsSharedParametersView, RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Pardavimo galimybių parametras turi būti rodinio pavadinimų, atskirtų viena kableliais, sąrašas. Negali būti tarpų arba eilutėje nurodyti papildomus kanalus.

## <a name="environment-specific-fixes"></a>Aplinkai brastos pataisos

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW pataisa

Rodinyje **RETAILCHANNELVIEW** yra užkoduotas skaičius, kuris nurodo mažmeninės prekybos kanalo tipo organizaciją. Faktinė tipo vertė gali pasikeisti iš aplinkos į aplinką arba iš nuomininkų į nuomininką.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Norėdami atnaujinti užs. ats. ats. atlikite šiuos veiksmus.

1. Programoje "Dynamics 365" peržiūrėkite savo **interneto kanalo ChannelID** vertę.
1. Egzemplioriuje, kuris yra "SQL Server Management Studio" (SSMS), kuris pridėtas prie sinapsės duomenų bazės, vykdykite šią užklausą.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Nukopijuokite vertę iš pirmo stulpelio (**INSTANCERELATIONTYPE**) ir įklijuokite į rodinio aprašą.

## <a name="troubleshooting"></a>Trikčių šalinimas

### <a name="pipeline-task-fails"></a>Pardavimo galimybių užduotis nesėkminga

Turi būti atlikti 15 pardavimo galimybių užduočių CopyData **užduoties** vykdymas. Jei bet koks vykdymas nesėkmingas, turite patikrinti, ar yra visi priklausomi SQL objektai ir ar paleistų užklausas. Paprasčiausias būdas gauti visų priklausomybių yra naudoti SSMS, kad būtų galima prisijungti prie duomenų bazės. Tada galėsite pasirinkti ir laikyti (arba spustelėti dešiniuoju pelės mygtuku) ir **naujame lange pasirinkti Generuoti KURTI**.

Klaidos pranešime gali būti šis tekstas:

- Klaida: "Source" pusėje įvyko triktis
- Klaida tvarkant išorinį failą: 'Maks. klaidų skaičius'.
- / RetailSales / RetailSales_xxxxxx

#### <a name="example-scenario"></a>Pavyzdinis scenarijus

Šiame pavyzdyje užduoties **RetailSales_RetailProductCategory**, o jūs gaunate klaidą "Maksimalus klaidų skaičius".

Norėdami suderinti klaidą, atlikite šiuos veiksmus.

1. Atidarykite **EntityList.json failą** teksto rengyklėje (pvz., Visual Studio Kodas).
1. Raskite darbo grupės rodinio **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Šis rodinys priklauso tik nuo kito rodinio: **RetailProductCategoryView** _. Raskite _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Šis rodinys priklauso nuo trijų kitų rodinių: RETAILPRODUCTCATEGORY **,** ECORESPRODUCTTRANSLATIONS **ir** RETAILCATEGORYEXPANDED **·**. Raskite kiekvienos iš šių rodinių apibrėžimus ir patraskite jų priklausomybes. Tęskite, kol rasite visus priklausomus rodinius.

    Čia pateikiamas visas priklausomybės medžio tvarkos sąrašas. Reikia patikrinti tryliktą rodinių.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE GRUPĘ
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SISTEMOSPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY KATEGORIJA
                - ECORESCATEGORYHIERARCHYROLE

1. Programoje Excel išrašuose sukurkite toliau nurodytą 13 **pasirinktų skaičių\*\<view_name\>**(). Vykdykite šiuos išrašus SSMS ir išsiųskite rezultatus tekstui. Tada paslinkite per rezultatus, kad pamatytumėte, ar rodiniai nepavyko. Pradinė klaida rodo, kad bent vienas rodinių bus nesėkmingas.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Vienas būdas, kaip patikrinti, ką ieškoma, yra sukurti šakninį priklausomą rodinį, kuris SSMS generuos rodinio aprašą. Tada patikrinkite, ar yra "Azure" duomenų įvardijami **r.filepath stulpeliai**. Šio stulpelio buvimo būsena nurodo, kad rodinys, kurį tikrinate, skaito duomenis iš Duomenų saugojimą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
