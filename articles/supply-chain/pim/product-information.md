---
title: Produktų informacijos peržiūra
description: Šiame straipsnyje pateikiama informacija apie produkto informacijos valdymą. Valdant produktų informaciją, dirbama su bendrinama produkto apibrėžtimi, kategorizacija ir identifikatoriais visuose juridiniuose subjektuose bei konkrečiomis produkto konfigūracijomis, kad būtų galima prisiderinti prie verslo procesų.
author: t-benebo
ms.date: 06/01/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa06e718d2acc44cfced7db842814c48fb210d1e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867875"
---
# <a name="product-information-overview"></a>Produktų informacijos peržiūra

[!include [banner](../includes/banner.md)]



Šiame straipsnyje pateikiama informacija apie produkto informacijos valdymą. Valdant produktų informaciją, dirbama su bendrinama produkto apibrėžtimi, kategorizacija ir identifikatoriais visuose juridiniuose subjektuose bei konkrečiomis produkto konfigūracijomis, kad būtų galima prisiderinti prie verslo procesų. 

Informacija apie produktus yra tiekimo grandinės ir prekybos programų pagrindas visose pramonės šakose. Ji nurodo procesus ir technologijas, kuriuos naudojant pirmiausia centralizuotai valdoma informacija apie produktus (pavyzdžiui, keliose tiekimo grandinėse). Labai svarbu, kad būtų naudojamos bendrinamos produktų apibrėžtys, dokumentacija, atributai ir identifikatoriai. Įvairiuose verslo sprendimo moduliuose būtina turėti konkretaus produkto informaciją ir konfigūraciją, kad būtų galima valdyti verslo procesus, susijusius su konkrečiais produktais, produktų šeimomis ar produktų kategorijomis.

## <a name="product-definition"></a>Produkto apibrėžtis

Produktą pirmiausia apibrėžia produkto numeris, pavadinimas ir aprašas. Tačiau, norint apibūdinti produktą ar paslaugą, taip pat būtini kiti duomenys:

- Produkto tipas: prekė arba paslauga
- Produkto potipis: išskirtieji produktai arba bendrieji produktai
- Produkto varianto modelio apibrėžtis:

     - Produktų dimensijos ir dimensijų grupės
     - Produktų nomenklatūra
     - Produkto konfigūracijos modeliai

- Produkto susiejimas su viena ar keliomis kategorijomis
- Produktų ir kategorijų atributų apibrėžimas
- Produkto vaizdai
- Priedai
- Matavimo vienetai ir susiję konvertavimai
- Visų pavadinimų ir aprašų vertimai

## <a name="distribution-export-and-import-of-product-data"></a>Produkto duomenų platinimas, eksportavimas ir importavimas

Produkto apibrėžtį galima sukurti „Supply Chain Management”. Ją taip pat galima importuoti iš produktų ciklo valdymo (PLM), produktų duomenų valdymo (PDM) ar produktų informacijos valdymo (PIM) sistemų. Kai naudojamas daugiau nei vienas „Supply Chain Management” egzempliorius, vienas iš jų paprastai naudojamas kaip pagrindinis produktų duomenų egzempliorius visiems kitiems egzemplioriams. Taip daryti galima pasitelkiant didelę duomenų objektų grupę, kuriuos naudojant produktų apibrėžčių duomenis galima eksportuoti ir importuoti iš vieno egzemplioriaus į kitą.

Kad produktų duomenis būtų galima platinti keliuose egzemplioriuose, „Supply Chain Management” galima naudoti „Microsoft Dataverse“. Produktų apibrėžtis iš „Supply Chain Management” egzemplioriaus galima eksportuoti į „Microsoft Dataverse“. Tada, naudojant produktų apibrėžtis, galima kitas verslo programas, pvz., „Dynamics 365 Sales“, užpildyti produktų duomenimis.

Atkreipkite dėmesį, kad dinamiškose ir lanksčiose organizacijose produktų informacijos duomenys keičiasi kiekvieną dieną. Todėl tikslių ir faktinių produktų duomenų priežiūra yra labai svarbus atskiras verslo procesas.

## <a name="product-masters-and-product-variants"></a>Bendrieji produktai ir produktų variantai

Lanksčiame pasaulyje, kuriame produktus reikia greitai pritaikyti pagal klientų reikalavimus, produktų apibrėžtyse nurodomas produktų rinkinys, o ne išskirtieji produktai. „Supply Chain Management” tokie produktai vadinami *bendraisiais produktais*. Bendruosiuose produktuose apibrėžiama ir pateikiamos taisyklės, kaip išskirtieji produktai aprašomi ir veikia vykstant verslo procesams. Pagal šias apibrėžtis galima generuoti išskirtuosius produktus. Šie išskirtieji produktai vadinami *produktų variantais*.

Bendrasis produktas susiejamas su produktų dimensijų grupe ir konfigūravimo technologija, kad būtų galima nurodyti verslo taisykles. Produktų dimensijos (Spalva, Dydis, Stilius ir Konfigūracija) yra konkretus atributų rinkinys, kurį naudojant programoje galima apibrėžti ir sekti konkretų susijusių produktų veikimą. Šios dimensijos taip pat vartotojams padeda ieškoti produktų ir juos nustatyti.

## <a name="configuration-technologies"></a>Konfigūravimo technologijos

Galite rinktis iš trijų konfigūravimo technologijų:

- Iš anksto apibrėžtus variantus apibrėžia iš anksto apibrėžtos produktų dimensijos. Į varianto apibrėžtį įeina konkretaus tinkamo dimensijų, pvz., Spalva, Stilius ir Dydis, derinio apibrėžtis. Kiekvienas derinys sukuria išskirtojo produkto variantą.
- Konfigūravimo pagal dimensijas funkcija paprastai naudojama gamybos situacijose ir apibrėžiant komplektavimo specifikacijas (KS) ji leidžia naudoti dimensiją Konfigūracija. Pasirinkus konkrečią konfigūraciją sistema naudoja tai konfigūracijai tinkamų planavimo ir gamybos KS eilučių pogrupį. Ši sąvoka taip pat vadinama *visuotine KS*, nes viena bendrai naudojama KS naudojama visoms produkto konfigūracijoms.
- Konfigūravimo pagal apribojimus funkcija naudoja produkto konfigūracijos modelį ir apibūdina visus galimus atributus ir komponentus, kurių reikia norint viename modelyje apibūdinti visus galimus produkto variantus. Atributų derinių apribojimus galima apibūdinti naudojant reguliariuosius reiškinius ar apribojimus pagal lenteles. Valdant produktų informaciją konfigūracijų modeliai ir konfigūratoriai tampa vis svarbesni ir yra naudojami visose pramonės šakose.

Planuojant diegti „Supply Chain Management”, labai svarbu verslo procesui parinkti tinkamą konfigūravimo technologiją. Įdiegus produkto negalima konvertuoti iš vieno modelio į kitą.

## <a name="product-variant-model-definition-workspace"></a>Darbo sritis Produktų variantų modelių apibrėžimas

Darbo srityje **Produktų variantų modelių apibrėžimas** apžvelgiami bendrieji produktai. Joje taip pat rodoma bendrųjų produktų ir susijusių variantų pateikimo konkretiems juridiniams subjektams būsena.

## <a name="released-products"></a>Patvirtinti produktai

Konkrečiam juridiniam subjektui pateikti produktai vadinami *pateiktais produktais*. Produktus vienu metu galima masiškai pateikti vienam juridiniam subjektui ar keliems juridiniams subjektams. Kadangi gali reikėti įtraukti įvairias atskiro juridinio subjekto produktų ypatybes ir atributus, darbo srityje **Pateiktų produktų priežiūra** galite stebėti ir užbaigti neseniai pateiktus produktus kiekviename juridiniame subjekte arba antrinėse juridinio subjekto organizacijose.

### <a name="released-product-maintenance-workspace"></a>Darbo sritis Pateiktų produktų priežiūra

Darbo sritį **Pateiktų produktų priežiūra** galite konfigūruoti pasirinkę meniu elementą **Konfigūruoti mano darbo sritį**. Pasirinkite kategorijų hierarchiją ir kategoriją, pagal kurias reikia filtruoti darbo sritį. Norėdami darbo srityje koreguoti aktualius produktų duomenis, taip pat galite dienomis apibrėžti **neseniai pateiktų produktų** ir **sustabdytų pateiktų produktų** laiko ribas.

Darbo sritį sudaro plytelių ir dviejų sąrašų suvestinė. Sąraše **Atviri atvejai** rodomi produktų keitimo atvejai, kai pasirinktos produktų kategorijų hierarchijos produktai nėra baigti ir uždaryti. Sąraše **Neseniai pateikti** rodomi produktai, pateikti laiko ribose, nustatytose darbo srities konfigūracijoje. Tikrinamas kiekvienas sąrašo elementas ir rodoma tikrinimo būsena. Ši būsena gali nurodyti, kad nebaigta būtina juridinio subjekto konfigūracija. Sąraše galite tiesiogiai pasiekti puslapius **Išsami pateiktų produktų informacija**, **Produktų atributų priežiūra**, **Produktų kategorijų priežiūra**, **Numatytieji užsakymų parametrai** ir **Teksto vertimai** bei baigti būtiną produkto konfigūraciją.

### <a name="manually-creating-a-new-released-product"></a>Naujo pateikto produkto kūrimas rankiniu būdu

Rankiniu būdu sukurti pateiktą produktą galite vienu veiksmu – tai priklauso nuo organizacijos verslo procesų ir taisyklių, nurodančių, ar turi būti naudojama ši funkcija. Naudojant šią funkciją sukuriamas naujas produktas, kuris automatiškai pateikiamas dabartiniam juridiniam subjektui. Norėdami sukurti naują produktą, darbo srityje **Pateiktų produktų priežiūra** arba sąrašo puslapyje **Pateiktas produktas** spustelėkite **Pateikti produktai**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]