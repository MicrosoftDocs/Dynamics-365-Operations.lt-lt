---
title: Atskirto dvigubo rašymo programos instrumentavimo paketas
description: Dvigubo rašymo programos instrumentavimo paketas nebėra vienas paketas, bet jis atskirtas į mažesnius paketus. Šioje temoje paaiškinami sprendimai ir schemos, kurias sudaro kiekvienas paketas, ir jo priklausomybė nuo kitų paketų.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3fe1b7707df72927fba78ee9659502cc62471799
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924984"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Atskirto dvigubo rašymo programos instrumentavimo paketas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Anksčiau dvigubo rašymo programos instrumentų paketas buvo vienas paketas, kuriame yra šie sprendimai:

- "Dynamics 365" pastabos
- Dynamics 365 Finance and Operations Įprastas prieraišo žymę
- Dynamics 365 Finance and Operations Dvigubo rašymo objektų schemos
- "Dynamics 365" turto valdymo programa
- "Dynamics 365" turto valdymas
- „HCM Common“
- "Dynamics 365" tiekimo grandinės išplėstinė
- „Dynamics 365 Finance Extended“
- Dynamics 365 Finance and Operations Bendras
- "Dynamics 365" įmonė
- Valiutų kursai
- Bendroji laukų tarnyba

Kadangi tai buvo viena pakuotė, šis paketas sukūrė "visą arba nieko" situaciją klientams. Tačiau Microsoft dabar atskirta ją į mažesnes pakuotes. Todėl klientas gali pasirinkti tik toms sprendimų, kurių reikia, paketus. Pavyzdžiui, jei esate "Microsoft" klientas ir jums nereikia integravimo su, pastabų ir turto valdymo, galite pašalinti tuos sprendimus iš Dynamics 365 Supply Chain Management Dynamics 365 Human Resources įdiegtų sprendimų. Kadangi toliau esantys sprendimų pavadinimai, leidėjų ir žemėlapių versijos lieka tokie patys, šis pakeitimas yra nesulaužinis. Reikia atnaujinti esamas įdiegtis.

![Atskirta pakuotė.](media/separated-package-1.png)

Šioje temoje paaiškinami sprendimai ir schemos, kurias sudaro kiekvienas paketas, ir jo priklausomybė nuo kitų paketų.

## <a name="dual-write-application-core"></a>Dvigubo rašymo programos branduolys

Dvigubo rašymo programos pagrindinis paketas leidžia vartotojams įdiegti ir konfigūruoti dvigubo rašymo be kliento įsipareigojimo programos. Jame yra šie penki sprendimai.

| Unikalus pavadinimas                           | Rodyti pavadinimą                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | "Dynamics 365" įmonė                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Bendras |
| Valiutų kursai                 | Valiutų kursai                    |
| msdyn_DualWriteAppCoreMaps            | Dvigubo rašymo prašymų pagrindinės objektų schemos   |
| msdyn_DualWriteAppCoreAnchor          | Dvigubo rašymo prašymų pagrindinis inkaras        |

Šioje pakuotėje yra tokios schemos.

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

**Priklausomybės informacija**

Dvigubo rašymo programos pagrindinis paketas priklauso nuo kitų paketų.

## <a name="dual-write-human-resources"></a>Dvigubo rašymo žmogiškieji ištekliai

Dvigubo rašymo personalo pakete yra sprendimai ir schemos, kurių reikia personalo duomenims sinchronizuoti. Jame yra trys toliau pateikti sprendimai.

| Unikalus pavadinimas                | Rodyti pavadinimą                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | „HCM Common“                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources objektų schemos |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources Inkaro      |

Šioje pakuotėje yra tokios schemos.

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
| Seniai dirbančiojo būsena              | cdm_veteranstatuses              |
| Darbuotojas                      | cdm_workers                      |
| Įdarbinimas pagal įmonę      | cdm_employments                  |

**Priklausomybės informacija**

Dvigubo rašymo personalo paketas priklauso nuo dvigubo rašymo programos pagrindinio paketo. Todėl turėtumėte įdiegti dvigubo rašymo programos pagrindinį paketą prieš diegdami dvigubo rašymo personalo paketą.

## <a name="dual-write-supply-chain"></a>Dvigubo rašymo tiekimo grandinė

Dvigubo rašymo tiekimo grandinės pakete yra sprendimai ir schemos, kurių reikia norint sinchronizuoti tiekimo grandinės valdymo duomenis. Jame yra trys toliau pateikti sprendimai.

| Unikalus pavadinimas                                | Rodyti pavadinimą                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | "Dynamics 365" tiekimo grandinės išplėstinė                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management išplėstinių objektų schemos |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management išplėstinis inkaras      |

Šioje pakuotėje yra tokios schemos.

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
| Produkto gavimo antraštė                      | msdyn_purchaseorderreceipts                   |
| Produkto gavimo eilutė                        | msdyn_purchaseorderreceiptproducts            |
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
| CDS atsargos                            | „msdyn_inventoryonhandentries”                  |
| Produkto kategorijos                          | msdyn_productcategories                       |
| CDS atsargos                            | „msdyn_inventoryonhanrequests”                 |
| Produkto numerio nustatytas brūkšninis kodas           | msdyn_productbarcodes                         |
| Lojalumo kortelė                                | msdyn_loyaltycards                            |
| Atlygio taškai už lojalumą                       | „msdyn_loyaltyrewardpoints”                     |
| Kainos klientų grupės                       | msdyn_pricecustomergroups                     |
| Teritorijos                                       | msdyn_operationalsites                        |
| CDS pardavimo pasiūlymo eilutės                   | quotedetails                                  |
| CDS pardavimo užsakymo eilutės                       | salesorderdetails                             |

**Priklausomybės informacija**

Dvigubo rašymo tiekimo grandinės paketas priklauso nuo šių trijų pakuočių. Todėl turite įdiegti šiuos paketus prieš diegdami dvigubo rašymo tiekimo grandinės paketą.

- Dvigubo rašymo programos pagrindinis paketas
- Dvigubo rašymo finansų paketas
- Dvigubo rašymo personalo paketas

## <a name="dual-write-finance"></a>Dvigubo rašymo finansai

Dvigubo rašymo finansų pakete yra sprendimai ir schemos, kurių reikia duomenims Dynamics 365 Finance sinchronizuoti. Jame yra tokie keturi sprendimai.

| Unikalus pavadinimas                            | Rodyti pavadinimą                               |
|----------------------------------------|-------------------------------------------|
| "Dynamics365FinanceExtended"             | „Dynamics 365 Finance Extended“             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance išplėstinių objektų schemos |
| FieldServiceCommon                     | Bendroji laukų tarnyba                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance išplėstinis inkaras      |

Šioje pakuotėje yra tokios schemos.

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

**Priklausomybės informacija**

Dvigubo rašymo finansų paketas priklauso nuo dvigubo rašymo programos pagrindinio paketo. Todėl turėtumėte įdiegti dvigubo rašymo programos pagrindinį paketą prieš diegdami dvigubo rašymo finansų paketą.

## <a name="dual-write-notes"></a>Dvigubo rašymo pastabos

Dvigubo rašymo pažymų pakete yra sprendimai ir schemos, kurių reikia norint sinchronizuoti pastabų ar komentarų duomenis. Jame yra tokie keturi sprendimai.

| Unikalus pavadinimas                  | Rodyti pavadinimą                   |
|------------------------------|--------------------------------|
| "Dynamics365Notes"             | "Dynamics 365" pastabos             |
| "Dynamics365NotesExtended"     | Išplėstinės "Dynamics 365" pastabos    |
| msdyn_Dynamics365NotesMaps   | "Dynamics 365" pastabų objektų schemos |
| msdyn_Dynamics365NotesAnchor | "Dynamics 365" pastabų prieraišo      |

Šioje pakuotėje yra tokios schemos.

| „Finance and Operations“                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Pardavimo užsakymo antraštės dokumento priedai    | Komentarus         |
| Kliento priedai                       | Komentarus         |
| Tiekėjo dokumentų priedai                | Komentarus         |
| Pirkimo užsakymo antraštės dokumento priedai | Komentarus         |

**Priklausomybės informacija**

Dvigubo rašymo pastabų paketas priklauso nuo šių dviejų pakuočių. Todėl turite įdiegti šiuos paketus prieš diegdami dvigubo rašymo pastabų paketą.

- Dvigubo rašymo programos pagrindinis paketas
- Dvigubo rašymo finansų paketas

## <a name="dual-write-asset-management"></a>Dvigubo rašymo turto valdymas

Dvigubo rašymo turto valdymo pakete yra sprendimai ir schemos, kurių reikia norint sinchronizuoti turto duomenis iš tiekimo grandinės valdymo Dynamics 365 Field Service arba. Jame yra tokie keturi sprendimai.

| Unikalus pavadinimas                          | Rodyti pavadinimą                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | "Dynamics 365" turto valdymas             |
| Dynamics365AssetManagementApp        | "Dynamics365" turto valdymo programa          |
| msdyn_DualWriteAssetManagementMaps   | "Dynamics 365" turto valdymo objektų schemos |
| msdyn_DualWriteAssetManagementAnchor | "Dynamics 365" turto valdymo inkaras      |

Šioje pakuotėje yra tokios schemos.

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

**Priklausomybės informacija**

Dvigubo rašymo turto valdymo paketas priklauso nuo dvigubo rašymo programos pagrindinio paketo. Todėl turėtumėte įdiegti dvigubo rašymo programos pagrindinį paketą prieš diegdami dvigubo rašymo turto valdymo paketą.

## <a name="packages-required-for-project-operations"></a>Pakuotės, būtinos projekto operacijoms
Projekto operacijos priklauso nuo šių paketų. Todėl turite įdiegti šiuos paketus prieš diegdami Projekto operacijas.

- Dvigubo rašymo programos pagrindinis paketas
- Dvigubo rašymo finansų paketas
- Dvigubo rašymo tiekimo grandinės paketas
- Dvigubo rašymo turto valdymo paketas
- Dvigubo rašymo personalo paketas
