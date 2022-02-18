---
title: Atskiras dvigubo rašymo programų orkestravimo paketas
description: Dviejų rašymo programų orkestravimo paketas nebėra vienas paketas, bet buvo suskirstytas į mažesnius paketus. Šioje temoje paaiškinami sprendimai ir žemėlapiai, kurie yra kiekviename pakete, ir jo priklausomybė nuo kitų paketų.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: e2f870368dc662032a3e7ca7ddca902feb23a713
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063267"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Atskiras dvigubo rašymo programų orkestravimo paketas

[!include [banner](../../includes/banner.md)]



Anksčiau „Dual-Write Application Orchestration“ paketas buvo vienas paketas, kuriame buvo šie sprendimai:

- „Dynamics 365“ pastabos
- Dynamics 365 Finance ir Operacijų bendrasis inkaras
- Dynamics 365 Finance ir operacijų dvigubo rašymo objektų žemėlapiai
- „Dynamics 365 Asset Management“ programa
- „Dynamics 365 Asset Management“.
- „HCM Common“
- „Dynamics 365“ tiekimo grandinė išplėsta
- „Dynamics 365 Finance Extended“
- Dynamics 365 Finance ir Operations Common
- „Dynamics 365 Company“.
- Valiutos kursai
- „Field Service Common“.

Kadangi tai buvo vienas paketas, šis paketas klientams sukūrė „viskas arba nieko“ situaciją. Tačiau „Microsoft“ dabar jį suskirstė į mažesnius paketus. Todėl klientas gali pasirinkti tik jiems reikalingų sprendimų paketus. Pavyzdžiui, jei esate „Microsoft“.Dynamics 365 Supply Chain Management klientas ir nereikia integruoti su Dynamics 365 Human Resources, pastabas ir turto valdymą, tuos sprendimus galite neįtraukti į įdiegtus sprendimus. Kadangi pagrindinių sprendimų pavadinimai, leidėjas ir žemėlapio versijos išlieka tos pačios, šis pakeitimas yra nenutrūkstamas. Esami įrenginiai turi būti atnaujinti.

![Atskira pakuotė.](media/separated-package-1.png)

Šioje temoje paaiškinami sprendimai ir žemėlapiai, kurie yra kiekviename pakete, ir jo priklausomybė nuo kitų paketų.

## <a name="dual-write-application-core"></a>Dvigubo rašymo programos branduolys

„Dual-Write Application Core“ paketas leidžia vartotojams įdiegti ir konfigūruoti dvigubą rašymą be jokios kliento įtraukimo programos. Jame yra šie penki sprendimai.

| Unikalus pavadinimas                           | Rodyti pavadinimą                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | „Dynamics 365 Company“.                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance ir Operations Common |
| Valiutų kursai                 | Valiutos kursai                    |
| msdyn_DualWriteAppCoreMaps            | Dviejų rašymo programų pagrindinių objektų žemėlapiai   |
| msdyn_DualWriteAppCoreAnchor          | Dviejų rašymo programų pagrindinis inkaras        |

Šiame pakete yra šie žemėlapiai.

| „Finance and Operations” programos     | „Customer engagement“ programos                    |
|---------------------------------|---------------------------------------------|
| Valdymo vienetas                  | msdyn_internalorganizations                 |
| Organizacijos hierarchija          | msdyn_internalorganizationhierarchies       |
| Juridiniai subjektai                  | msdyn_internalorganizations                 |
| Juridiniai subjektai                  | cdm_companies                               |
| Organizacijos hierarchijos tikslai | msdyn_internalorganizationhierarchypurposes |
| Valiutos kurso valiutų pora     | „msdyn_currencyexchangeratepairs”             |
| Pavadinimo afiksai                    | msdyn_nameaffixes                           |
| Valiutos kurso tipas              | „msdyn_exchangeratetypes”                     |
| CDS valiutos kursai              | „msdyn_currencyexchangerates”                 |
| Organizacijos hierarchijos tipas     | msdyn_internalorganizationhierarchytypes    |
| Valiutos                      | transactioncurrencies                       |
| Mišriosios realybės vadovų objektas     | msmrw_guides                                |

**Informacija apie priklausomybę**

„Dual-Write Application Core“ paketas nėra priklausomas nuo kitų paketų.

## <a name="dual-write-human-resources"></a>Žmogiškieji ištekliai dviem rašmenimis

Dvigubo rašymo žmogiškųjų išteklių pakete yra sprendimai ir žemėlapiai, reikalingi žmogiškųjų išteklių duomenims sinchronizuoti. Jame yra šie trys sprendimai.

| Unikalus pavadinimas                | Rodyti pavadinimą                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | „HCM Common“                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources subjektų žemėlapiai |
| msdyn_Dynamics365HCMAchor | Dynamics 365 Human Resources inkaras      |

Šiame pakete yra šie žemėlapiai.

| „Finance and Operations” programos | „Customer engagement“ programos         |
|-----------------------------|----------------------------------|
| Etninė kilmė              | cdm_ethnicorigins                |
| Kompensavimo užduoties funkcija   | cdm_jobfunctions                 |
| Pareigybės V2                | cdm_jobpositions                 |
| Operacijos                        | cdm_jobs                         |
| Kompensavimo užduoties tipas       | cdm_jobtypes                     |
| Kalbų kodai              | cdm_languages                    |
| Pareigų tipas               | cdm_positiontypes                |
| Pareigų priskyrimai darbininkams | cdm_positionworkerassignmentmaps |
| Seniai dirbančiojo būsena              | cdm_veteranstatus              |
| Darbuotojas                      | cdm_workers                      |
| Įdarbinimas pagal įmonę      | cdm_employments                  |

**Informacija apie priklausomybę**

Dvigubo rašymo žmogiškųjų išteklių paketas priklauso nuo „Dual-write Application Core“ paketo. Todėl prieš diegdami „Dual-write“ žmogiškųjų išteklių paketą turėtumėte įdiegti „Dual-write Application Core“ paketą.

## <a name="dual-write-supply-chain"></a>Dvigubo rašymo tiekimo grandinė

Dvigubo rašymo tiekimo grandinės pakete yra sprendimai ir žemėlapiai, reikalingi tiekimo grandinės valdymo duomenims sinchronizuoti. Jame yra šie trys sprendimai.

| Unikalus pavadinimas                                | Rodyti pavadinimą                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | „Dynamics 365“ tiekimo grandinė išplėsta                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management išplėstiniai objektų žemėlapiai |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management prailgintas inkaras      |

Šiame pakete yra šie žemėlapiai.

| „Finance and Operations” programos                 | „Customer engagement“ programos                      |
|---------------------------------------------|-----------------------------------------------|
| Vienetai                                       | mat. vnt.                                          |
| CDS pardavimo užsakymų antraštės                     | salesorders                                   |
| CDS pardavimo užsakymo eilutės                       | salesorderdetails                             |
| CDS pardavimo pasiūlymo antraštė                  | pasiūlymai                                        |
| CDS pardavimo pasiūlymo eilutės                   | quotedetails                                  |
| CDS išleisti išskirtieji produktai              | produktai                                      |
| Sandėlio zonos                             | msdyn_warehousezones                          |
| Sandėlio zonų grupės                       | msdyn_warehousezonegroups                     |
| Sandėlio darbo eilutės                        | msdyn_warehouseworklines                      |
| Sandėlio darbo antraštės                      | msdyn_warehouseworkheaders                    |
| Sandėliai                                  | msdyn_warehouses                              |
| Atsargų perėjimas                             | msdyn_warehouseaisles                         |
| Vienetų konvertavimas                            | msdyn_unitofmeasureconversions                |
| Pristatymo sąlygos                           | msdyn_termsofdeliveries                       |
| Pristatymo būdai                           | msdyn_shipvias                                |
| Bendrojo produkto stiliai                       | msdyn_sharedproductstyles                     |
| Pardavimo sąskaitos faktūros eilutės V2                      | invoicedetails                                |
| Pardavimo SF antraštės V2                    | SF                                      |
| Bendrojo produkto dydžiai                        | msdyn_sharedproductsizes                      |
| Išleisti produktai V2                        | „msdyn_sharedproductdetails”                    |
| Bendrojo produkto konfigūracijos               | msdyn_sharedproductconfigurations             |
| Bendrojo produkto spalvos                       | msdyn_sharedproductcolors                     |
| Pardavimo užsakymo kilmės kodai                    | „msdyn_salesorderorigins”                       |
| Produkto gavimo antraštė                      | msdyn_purchaseorderceipts                   |
| Produkto gavimo eilutė                        | msdyn_purchaseorderceiptproducts            |
| Pirkimo užsakymo antraštės V2                   | msdyn_purchaseorders                          |
| CDS pirkimo užsakymo eilutės iš dalies panaikintas objektas | msdyn_purchaseorderproducts                   |
| CDS pirkimo užsakymo eilutės objektas              | msdyn_purchaseorderproducts                   |
| Sekimo dimensijų grupės                   | „msdyn_producttrackingdimensiongroups”          |
| Stiliai                                      | msdyn_productstyles                           |
| Saugojimo dimensijų grupės                    | „msdyn_productstoragedimensiongroups”           |
| Konkretaus produkto vieneto konvertavimai           | „msdyn_productspecificunitofmeasureconversions” |
| Produkto numatytieji užsakymo parametrai V2           | msdyn_productspecificdefaultordersettings     |
| Dydžiai                                       | msdyn_productsizes                            |
| Produkto dimensijų grupės                    | msdyn_productdimensiongroups                  |
| Numatytieji užsakymo parametrai                      | msdyn_productdefaultordersettings             |
| Konfigūracijos                              | msdyn_productconfigurations                   |
| Visi produktai                                | msdyn_globalproducts                          |
| Spalvos                                      | msdyn_productcolors                           |
| Produktų kategorijų hierarchijų vaidmenys            | „msdyn_productcategoryhierarchyroles”           |
| Produktų kategorijų hierarchijos                | msdyn_productcategoryhierarchies              |
| Produktų kategorijos priskyrimai                | msdyn_productcategoryassignments              |
| Produkto kategorijos                          | msdyn_productcategories                       |
| Sandėlis, vietos                         | msdyn_inventorylocations                      |
| CDS inventorius įjungtas                            | „msdyn_inventoryonhandentries”                  |
| Produkto kategorijos                          | msdyn_productcategories                       |
| CDS inventorius įjungtas                            | „msdyn_inventoryonhanrequests”                 |
| Produkto numerio nustatytas brūkšninis kodas           | msdyn_product barcodes                         |
| Lojalumo kortelė                                | msdyn_loyaltycards                            |
| Atlygio taškai už lojalumą                       | „msdyn_loyaltyrewardpoints”                     |
| Kainos klientų grupės                       | msdyn_pricecustomergroups                     |
| Teritorijos                                       | msdyn_operationalsites                        |
| CDS pardavimo pasiūlymo eilutės                   | quotedetails                                  |
| CDS pardavimo užsakymo eilutės                       | salesorderdetails                             |

**Informacija apie priklausomybę**

Dvigubo rašymo tiekimo grandinės paketas priklauso nuo šių trijų paketų. Todėl prieš diegdami dvigubo rašymo tiekimo grandinės paketą turėtumėte įdiegti šiuos paketus.

- Dviejų rašymo programų paketas
- Dviejų raštų finansų paketas
- Dviejų raštų žmogiškųjų išteklių paketas

## <a name="dual-write-finance"></a>Dviejų raštų finansai

„Dual-write Finance“ pakete yra sprendimai ir žemėlapiai, kurių reikia sinchronizuoti Dynamics 365 Finance duomenis. Jame yra šie keturi sprendimai.

| Unikalus pavadinimas                            | Rodyti pavadinimą                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | „Dynamics 365 Finance Extended“             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance išplėstiniai objektų žemėlapiai |
| „FieldServiceCommon“.                     | „Field Service Common“.                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance prailgintas inkaras      |

Šiame pakete yra šie žemėlapiai.

| „Finance and Operations” programos             | „Customer engagement“ programos        |
|-----------------------------------------|---------------------------------|
| Išskaitomo mokesčio grupės                  | msdyn_atidedamųmokesčiųgrupės      |
| CDS kontaktai V2 (klientas)              | kontaktai                        |
| CDS kontaktai V2 (tiekėjas)                | kontaktai                        |
| Klientai V3                            | kontaktai                        |
| Išskaitomų mokesčių kodai                   | msdyn_atidedamųmokesčiųkodai       |
| Tiekėjai V2                              | msdyn_vendors                   |
| Tiekėjo mokėjimo būdas                   | msdyn_vendorpaymentmethods      |
| Tiekėjų grupės                           | msdyn_vendorgroups              |
| Sąskaitų planas                       | „msdyn_chartofaccountses”         |
| Didžiosios knygos PVM registravimo grupės V2      | msdyn_mokesčiųregistravimogrupės          |
| Prekės PVM grupė                    | msdyn_mokesčiųprekiųgrupės             |
| PVM grupės                        | msdyn_mokesčiųgrupės                 |
| Atleidimo nuo PVM kodo objekto CDS        | msdyn_mokesčiųlengvatųkodai            |
| Klientų grupės                         | msdyn_customergroups            |
| Kliento mokėjimo būdas                 | msdyn_customerpaymentmethods    |
| Finansinės dimensijos                    | „msdyn_dimensionattributes”       |
| PVM rinkėjai                   | msdyn_mokesčiųinspekcijos            |
| Finansinės dimensijos formatas              | „msdyn_financialdimensionformats” |
| Ataskaitinis kalendorinis laikotarpis                  | „msdyn_fiscalcalendarperiods”     |
| Ataskaitinio kalendoriaus integravimo objektas      | „msdyn_fiscalcalendars”           |
| Ataskaitinių kalendorinių metų integravimo objektas | „msdyn_fiscalcalendaryears”       |
| Mokėjimo sąlygos                        | msdyn_paymentterms              |
| Mokėjimo grafikas                        | msdyn_paymentschedules          |
| Mokėjimo grafiko eilutės                  | msdyn_paymentschedulelines      |
| Mokėjimo dienos CDS                        | msdyn_paymentdays               |
| Mokėjimo dienos eilutės CDS V2                | msdyn_paymentdaylines           |
| Korespondentinė sąskaita, subsąskaita                            | „msdyn_mainaccounts”              |
| Pagrindinių sąskaitų kategorijos                 | „msdyn_mainaccountcategories”     |
| Ledger                                  | „msdyn_ledgers”                   |
| Klientai V3                            | sąskaitos                        |

**Informacija apie priklausomybę**

„Dual-write“ finansų paketas priklauso nuo „Dual-write Application Core“ paketo. Todėl prieš diegdami „Dual-write“ finansų paketą turėtumėte įdiegti „Dual-write Application Core“ paketą.

## <a name="dual-write-notes"></a>Dvigubo rašymo pastabos

Dvigubo rašymo pastabų pakete yra sprendimai ir žemėlapiai, kurių reikia pastabų ar komentarų duomenims sinchronizuoti. Jame yra šie keturi sprendimai.

| Unikalus pavadinimas                  | Rodyti pavadinimą                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | „Dynamics 365“ pastabos             |
| Dynamics365NotesExtended     | „Dynamics 365“ pastabos išplėstos    |
| msdyn_Dynamics365NotesMaps   | „Dynamics 365“ užrašų objektų žemėlapiai |
| msdyn_Dynamics365NotesAnchor | „Dynamics 365“ užrašų inkaras      |

Šiame pakete yra šie žemėlapiai.

| „Finance and Operations”                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Pardavimo užsakymo antraštės dokumento priedai    | anotacijos         |
| Kliento priedai                       | anotacijos         |
| Tiekėjo dokumentų priedai                | anotacijos         |
| Pirkimo užsakymo antraštės dokumento priedai | anotacijos         |

**Informacija apie priklausomybę**

„Dual-write Notes“ paketas priklauso nuo šių dviejų paketų. Todėl prieš diegdami „Dual-write Notes“ paketą turėtumėte įdiegti šiuos paketus.

- Dviejų rašymo programų paketas
- Dviejų raštų finansų paketas

## <a name="dual-write-asset-management"></a>Dvigubo rašymo turto valdymas

Dvigubo rašymo turto valdymo pakete yra sprendimai ir žemėlapiai, kurių reikia norint sinchronizuoti turto duomenis iš tiekimo grandinės valdymo arba Dynamics 365 Field Service. Jame yra šie keturi sprendimai.

| Unikalus pavadinimas                          | Rodyti pavadinimą                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | „Dynamics 365 Asset Management“.             |
| Dynamics365AssetManagementApp        | „Dynamics365 Asset Management“ programa          |
| msdyn_DualWriteAssetManagementMaps   | „Dynamics 365 Asset Management“ objektų žemėlapiai |
| msdyn_DualWriteAssetManagementAnchor | „Dynamics 365 Asset Management“ inkaras      |

Šiame pakete yra šie žemėlapiai.

| „Finance and Operations” programos                           | „Customer engagement“ programos                |
|-------------------------------------------------------|-----------------------------------------|
| Turto valdymo garantija                             | msdyn_warranties                        |
| Turto valdymo modeliai                               | msdyn_models                            |
| Turto valdymo gamintojai                        | msdyn_manufacturers                     |
| Turto valdymo funkcinių vietų tipai            | msdyn_functionallocationtypes           |
| Turto valdymo funkcinės vietos                 | msdyn_functionallocations               |
| Turto valdymo funkcinių vietų ciklo būsenos | msdyn_functionallocationlifecyclestates |
| Turto valdymo funkcinių vietų ciklo modeliai | msdyn_functionallocationlifecyclemodels |
| Turto valdymo turtas                               | msdyn_customerassets                    |
| Turto valdymo turto tipai                          | msdyn_customerassetcategories           |
| Turto valdymo turto ciklo modelių būsenos               | msdyn_assetlifecyclestates              |
| Turto valdymo turto ciklo modeliai               | msdyn_assetlifecyclemodels              |

**Informacija apie priklausomybę**

Dvigubo rašymo turto valdymo paketas priklauso nuo dvigubo rašymo programos pagrindinio paketo. Todėl prieš diegdami dvigubo rašymo turto valdymo paketą turėtumėte įdiegti „Dual-write Application Core“ paketą.

## <a name="packages-required-for-project-operations"></a>Projekto operacijoms reikalingi paketai
Projekto operacijos priklauso nuo šių paketų. Todėl prieš diegdami Project Operations turėtumėte įdiegti šiuos paketus.

- Dviejų rašymo programų paketas
- Dviejų raštų finansų paketas
- Dvigubo rašymo tiekimo grandinės paketas
- Dvigubo rašymo turto valdymo paketas
- Dviejų raštų žmogiškųjų išteklių paketas
