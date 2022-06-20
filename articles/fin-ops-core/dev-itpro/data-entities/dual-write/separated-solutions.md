---
title: Atskirto dvigubo rašymo programos instrumentavimo paketas
description: Dvigubo rašymo programos instrumentavimo paketas nebėra vienas paketas, bet jis atskirtas į mažesnius paketus. Šiame straipsnyje paaiškinami sprendimai ir schemos, kad kiekvienas paketas yra, ir jo priklausomybė nuo kitų paketų.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 504939f1f98c18005c092cabc1d040b420402c93
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874818"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Atskirto dvigubo rašymo programos instrumentavimo paketas

[!include [banner](../../includes/banner.md)]



Anksčiau dvigubo rašymo programos instrumentų paketas buvo vienas paketas, kuriame yra šie sprendimai:

- "Dynamics 365" pastabos
- "Dynamics 365" finansų ir operacijų bendrasis inkaras
- "Dynamics 365" finansų ir operacijų dvigubo rašymo objektų schemos
- "Dynamics 365" turto valdymo programa
- "Dynamics 365" turto valdymas
- „HCM Common“
- "Dynamics 365" tiekimo grandinės išplėstinė
- „Dynamics 365 Finance Extended“
- "Dynamics 365" finansų ir operacijų bendrosios operacijos
- "Dynamics 365" įmonė
- Valiutų kursai
- Bendroji laukų tarnyba

Kadangi tai buvo viena pakuotė, šis paketas sukūrė "visą arba nieko" situaciją klientams. Tačiau Microsoft dabar atskirta ją į mažesnes pakuotes. Todėl klientai gali pasirinkti tik savo reikalauti sprendimo paketus. Pavyzdžiui, jei esate "Microsoft Dynamics 365 Supply Chain Management Dynamics 365 Human Resources" klientas ir jums nereikia integravimo su, pastabų ir turto valdymo, galite pašalinti tuos sprendimus iš įdiegtų sprendimų. Kadangi toliau esantys sprendimų pavadinimai, leidėjų ir žemėlapių versijos lieka tokie patys, šis pakeitimas yra nesulaužinis. Reikia atnaujinti esamas įdiegtis.

![Atskirta pakuotė.](media/separated-package-1.png)

Šiame straipsnyje paaiškinami sprendimai ir schemos, kad kiekvienas paketas yra, ir jo priklausomybė nuo kitų paketų.

## <a name="dual-write-application-core"></a>Dvigubo rašymo programos branduolys

Dvigubo rašymo programos pagrindinis paketas leidžia vartotojams įdiegti ir konfigūruoti dvigubo rašymo be kliento įsipareigojimo programos. Jame yra šie penki sprendimai.

| Unikalus pavadinimas                           | Rodomas pavadinimas                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | "Dynamics 365" įmonė                       |
| Dynamics365FinanceAndOperationsCommon | "Dynamics 365" finansų ir operacijų bendrosios operacijos |
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

| Unikalus pavadinimas                | Rodomas pavadinimas                             |
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
| Užduotys                        | cdm_jobs                         |
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

| Unikalus pavadinimas                                | Rodomas pavadinimas                                              |
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
| Svetainės                                       | msdyn_operationalsites                        |
| CDS pardavimo pasiūlymo eilutės                   | quotedetails                                  |
| CDS pardavimo užsakymo eilutės                       | salesorderdetails                             |

**Priklausomybės informacija**

Dvigubo rašymo tiekimo grandinės paketas priklauso nuo šių trijų pakuočių. Todėl turite įdiegti šiuos paketus prieš diegdami dvigubo rašymo tiekimo grandinės paketą.

- Dvigubo rašymo programos pagrindinis paketas
- Dvigubo rašymo finansų paketas
- Dvigubo rašymo personalo paketas

## <a name="dual-write-finance"></a>Dvigubo rašymo finansai

Dvigubo rašymo finansų pakete yra sprendimai ir schemos, kurių reikia norint sinchronizuoti "Dynamics 365" finansų duomenis. Jame yra tokie keturi sprendimai.

| Unikalus pavadinimas                            | Rodomas pavadinimas                               |
|----------------------------------------|-------------------------------------------|
| "Dynamics365FinanceExtended"             | „Dynamics 365 Finance Extended“             |
| msdyn_Dynamics365FinanceExtendedMaps   | "Dynamics 365" išplėstinių finansų objektų schemos |
| FieldServiceCommon                     | Bendroji laukų tarnyba                      |
| msdyn_Dynamics365FinanceExtendedAnchor | "Dynamics 365" finansų išplėstinis inkaras      |

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
| Pagrindinė sąskaita                            | „msdyn_mainaccounts”              |
| Pagrindinių sąskaitų kategorijos                 | „msdyn_mainaccountcategories”     |
| Didžioji knyga                                  | „msdyn_ledgers”                   |
| Klientai V3                            | sąskaitos                        |

**Priklausomybės informacija**

Dvigubo rašymo finansų paketas priklauso nuo dvigubo rašymo programos pagrindinio paketo. Todėl turėtumėte įdiegti dvigubo rašymo programos pagrindinį paketą prieš diegdami dvigubo rašymo finansų paketą.

## <a name="dual-write-notes"></a>Dvigubo rašymo pastabos

Dvigubo rašymo pažymų pakete yra sprendimai ir schemos, kurių reikia norint sinchronizuoti pastabų ar komentarų duomenis. Jame yra tokie keturi sprendimai.

| Unikalus pavadinimas                  | Rodomas pavadinimas                   |
|------------------------------|--------------------------------|
| "Dynamics365Notes"             | "Dynamics 365" pastabos             |
| "Dynamics365NotesExtended"     | Išplėstinės "Dynamics 365" pastabos    |
| msdyn_Dynamics365NotesMaps   | "Dynamics 365" pastabų objektų schemos |
| msdyn_Dynamics365NotesAnchor | "Dynamics 365" pastabų prieraišo      |

Šioje pakuotėje yra tokios schemos.

| „Finance and Operations”                     | Customer Engagement |
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

Dvigubo rašymo turto valdymo pakete yra sprendimai ir schemos, kurių reikia norint sinchronizuoti turto duomenis iš tiekimo grandinės valdymo arba Dynamics 365 Field Service. Jame yra tokie keturi sprendimai.

| Unikalus pavadinimas                          | Rodomas pavadinimas                              |
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

## <a name="dual-write-party-and-global-address-book-solutions"></a>Dvigubo rašymo šalies ir visuotinės adresų knygelės sprendimai

Dvigubo rašymo šalies ir visuotinės adresų knygelės pakete yra šie sprendimai ir schemos, reikalingi šalies ir visuotinės adresų knygelės duomenims sinchronizuoti. 

| Unikalus pavadinimas                       | Rodomas pavadinimas                            |
|-----------------------------------|-----------------------------------------|
| Šalis                             | Šalis                                   |
| "Dynamics365GABExtended"            | "Dynamics 365 GAB" išplėstas               |
| Dynamics365GABDualWriteEntityMaps | "Dynamics 365 GAB" dvigubo rašymo objekto schemos |
| Dynamics365GABParty_Anchor        | "Dynamics 365 GAB" ir šalis              |

Šioje pakuotėje yra tokios schemos.

| „Finance and operations” programos | „Customer engagement“ programos | 
|-----------------------------|--------------------------|
| CDS šalys | msdyn_parties | 
| CDS pašto adreso vietos | msdyn_postaladdresscollections | 
| CDS pašto adreso istorija V2 | msdyn_postaladdresses | 
| CDS šalies pašto adreso vietos. | msdyn_partypostaladdresses | 
| Šalies kontaktai V3 | msdyn_partyelectronicaddresses | 
| Klientai V3 | sąskaitos | 
| Klientai V3 | kontaktai | 
| Tiekėjai V2 | msdyn_vendors | 
| Kontaktinio asmens pareigos | msdyn_salescontactpersontitles | 
| Baigiamosios mandagumo frazės | msdyn_complimentaryclosings | 
| Pasisveikinimai | msdyn_salutations | 
| Sprendimų priėmimo vaidmenys | msdyn_decisionmakingroles | 
| Įdarbinimo užduočių funkcijos | msdyn_employmentjobfunctions | 
| Lojalumo lygiai | msdyn_loyaltylevels | 
| Asmeninių savybių tipai | msdyn_personalcharactertypes | 
| Kontaktai V2 | msdyn_contactforparties | 
| CDS pardavimo pasiūlymo antraštė | pasiūlymai | 
| CDS pardavimo užsakymų antraštės | salesorders | 
| Pardavimo SF antraštės V2 | SF | 
| CDS adreso vaidmenys | msdyn_addressroles |

**Priklausomybės informacija**

Dvigubo rašymo šalies ir visuotinės adresų knygelės sprendimai priklauso nuo šių trijų paketų. Todėl turite įdiegti šiuos paketus prieš diegdami dvigubo rašymo ir visuotinės adresų knygelės sprendimų paketą.

- Dvigubo rašymo programos pagrindinis paketas
- Dvigubo rašymo finansų paketas
- Dvigubo rašymo tiekimo grandinės paketas
