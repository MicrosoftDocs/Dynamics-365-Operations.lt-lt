---
title: Objekto priklausomybės grandinė (sinchronizavimo tvarka)
description: Šioje temoje nurodoma sinchronizavimo tvarka, kurią turite sekti, kad sukurtumėte pradinius duomenis.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275492"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Objekto priklausomybės grandinė (sinchronizavimo tvarka)

[!include [banner](../../includes/banner.md)]

Ši tema nurodo sinchronizavimo tvarką, kurios reikia laikytis norint sukurti pradinius duomenis, jei nenaudojate objekto priklausomybių, kurias teikia **pradinio sinchronizavimo** funkcija. Jei nenaudojate **pradinio sinchronizavimo**, turite vykdyti kiekvieną objekto schemą atskirai.

## <a name="dynamics-365-supply-chain-management-entities"></a>„Dynamics 365 Supply Chain Management“ objektai

Toliau nurodyti „Supply Chain Management” objektai išvardyti tokia tvarka, kokia juos turite įjungti.

| Dvigubo rašymo funkcijos puslapyje esantis susiejimo pavadinimas | Subjekto metaduomenų pavadinimas programoje „Supply Chain Management” | Objekto metaduomenų pavadinimas tarnyboje „Common Data Service” | Pastabos |
|---|---|---|---|
| Vienetai ... mat. vnt.                                                                      | UnitOfMeasureEntity                                    | mat. vnt.                                          | |
| Vienetų konvertavimas ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Visi produktai ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Produkto dimensijų grupės ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Saugojimo dimensijų grupės ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Sekimo dimensijų grupės ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Spalvos ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Dydžiai ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Stiliai ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Konfigūracijos ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Išleisti produktai V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| „Common Data Service” išleisti išskirtieji produktai ... produktai                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | produktas                                      | |
| Produkto numerio nustatytas brūkšninis kodas ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Numatytieji užsakymo parametrai ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Numatytieji produkto užsakymo parametrai V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Konkretaus produkto vieneto konvertavimas ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Svetainės ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Sandėliai ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Žr. [1 pastabą](#scm-notes). |
| Bendrojo produkto spalvos ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Bendrojo produkto dydžiai ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Bendrojo produkto stiliai ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Bendrojo produkto konfigūracijos ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Produktų kategorijos ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Žr. [2 pastabą](#scm-notes). |
| Produktų kategorijų priskyrimai ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Produktų kategorijų hierarchijos ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Produktų kategorijų hierarchijų vaidmenys ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Atsargų perėjimas... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Sandėlio zonos ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Sandėlio zonų grupės ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Sandėlio vietos... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Žr. [3 pastabą](#scm-notes). |
| Sandėlio darbo antraštės ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Sandėlio darbo eilutės ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Žr. [4 pastabą](#scm-notes). |
| Pristatymo būdai ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Pristatymo sąlygos ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Pardavimo užsakymo kilmės kodai ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| „Common Data Service” pardavimo užsakymo antraštės ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| „Common Data Service” pardavimo užsakymo eilutės ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| „Common Data Service” pardavimo pasiūlymo antraštė ... pasiūlymai                               | SalesQuotationHeaderCommon Data ServiceEntity          | pasiūlymas                                        | |
| „Common Data Service” pardavimo pasiūlymo eilutės ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Pardavimo SF antraštės V2 ... sąskaitos faktūros                                               | SalesInvoiceHeaderV2Entity                             | SF                                      | |
| Pardavimo SF eilutės V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Susiejimui būdingos pastabos

1. Dėl vidinės priklausomybės gali reikėti paleisti pradinį sinchronizavimą du kartus.
2. Pagal numatytuosius parametrus pradinis sinchronizavimas išjungtas dėl pirminių ir antrinių ryšių (platforma netvarkomas „išmanusis“ užsakymas). Todėl esamos produktų kategorijos turi būti sinchronizuojamos rankiniu būdu (pavyzdžiui, atnaujinant kategorijos aprašą) tinkama tvarka (pirmiausia šakninė kategorija, po to antrinė ir antrinės antrinė). Eikite į **Produkto informacijos valdymas \> Sąranka \> Kategorijos ir atributai \> Kategorijų hierarchijos**. Puslapyje **Kategorijų hierarchijos** galite pasirinkti kiekvieną hierarchiją ir peržiūrėti joje esančias produktų kategorijas.
3. Jei susiejami tušti **ItemNumberInLocation** peržvalgos laukai ir pirma, antra ir trečia papildomos sandėlio zonos, nepavyks atlikti pradinio sinchronizavimo. Todėl kol kas šie susiejimai pašalinami.
4. Jei susiejamas tuščias **CaptureWeight** laukas, nepavyks atlikti pradinio sinchronizavimo. Todėl kol kas šie šis susiejimas pašalinamas.

### <a name="setup-related-information"></a>Su sąranka susijusi informacija

+ Kai įrašai sukuriami pirmą kartą objekte **Produktai**, „Dynamics 365” modeliu pagrįstose programose, jų būsena yra **Juodraštis**. Norėdami pakeisti būseną į **Aktyvus**, modeliu pagrįstoje programoje eikite į **Parametrai \>Administravimas \> Sistemos parametrai \> Pardavimas** ir nustatykite parinktį **Kurti aktyvios būsenos produktus** į **Taip**.
+ Jei kuriate įrašus objekte **Produktai**, „Dynamics 365” modeliu pagrįstose programose arba tarnyboje „Common Data Service”, prieš įjungdami dvigubą rašymą, tie įrašai bus atnaujinti tik tada, jei visas raktas, įskaitant **Įmonės**, sutampa su „Finance and Operations” programos duomenimis.
+ Objekto **Produktai** sinchronizavimas yra vienakryptis – iš „Finance and Operations” programų į „Common Data Service”. Jei objekte **Produktai**, „Dynamics 365” modeliu pagrįstose programose, susietas laukas yra atnaujinamas, o šis atnaujinimas bus perrašytas per kitą sinchronizavimoą iš „Finance and Operations” programos.

### <a name="known-issues"></a>Žinomos problemos

- Bandant panaikinti vienetą programoje „Finance and Operations” įvyksta klaida. Kai matavimo vienetai sinchronizuojami iš „Finance and Operations” programos į „Common Data Service”, pirmas tam tikros klasės vienetas bus sukurtas kaip pagrindinis vienetas ir bus išvengta naikinimo.

    **Mažinimas:** pirmiausia panaikinkite vienetą, esantį „Common Data Service”. Jis gali būti panaikintas „Finance and Operations” programoje.

- Bandant panaikinti operatyviąją svetainę programoje „Common Data Service” įvyksta klaida. Klaidos pranešimas nurodo, „Sistemos pranešimas: Įspėjimas: pagrindinio adreso panaikinti negalima.; Įspėjimas: Nepavyko panaikinti objekto įrašo, nes nepavyko patikrinti nurodyto duomenų šaltinio: InventSiteLogisticsLocation (InventSiteLogisticsLocation).” Ši klaida kilo dėl „Finance and Operations” programos duomenų objekto problemos.

    **Mažinimas:** „Finance and Operations” programoje galite panaikinti svetainę. Tada svetainė bus panaikinta tarnyboje „Common Data Service”, jei atitinkamas dvigubo rašymo susiejimas yra vykdomas.

## <a name="dynamics-365-finance-entities"></a>„Dynamics 365 Finance“ objektai

Toliau nurodyti „Dynamics 365 Finance” objektai išvardyti tokia tvarka, kokia juos turite įjungti.

| Dvigubo rašymo funkcijos puslapyje esantis susiejimo pavadinimas | Objekto metaduomenų pavadinimas tarnyboje „Finance” | Objekto metaduomenų pavadinimas tarnyboje „Common Data Service” | Pastabos |
|---|---|---|---|
| Valiutos ... transactioncurrencies                                            | CurrencyEntity                              | Valiuta                                   | |
| Valiutos kurso tipas ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Valiutos kurso valiutų pora ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| „Common Data Service” valiutos kursai ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Žr. [1 pastabą](#fin-notes). |
| Finansinio kalendoriaus integravimo objektas ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Ataskaitinių kalendorinių metų integravimo objektas ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Ataskaitinis kalendorinis laikotarpis ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Organizacijos hierarchijos tipas ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Žr. [1 pastabą](#fin-notes). |
| Organizacijos hierarchijos paskirtis ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Žr. [1 pastabą](#fin-notes). |
| Juridiniai subjektai ... msdyn_internalorganizations                                  | „OMLegalEntity”                               | msdyn_internalorganization                 | Žr. [1 pastabą](#fin-notes). |
| Juridiniai subjektai ... cdm_companies                                                | „OMLegalEntity”                               | cdm_company                                | |
| Valdymo vienetas ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Žr. [1 pastabą](#fin-notes). |
| Organizacijos hierarchija – paskelbta ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Žr. [1 pastabą](#fin-notes). |
| Pavadinimo afiksai ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Mokėjimo dienos „Common Data Service” ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Mokėjimo dienų eilutės „Common Data Service” V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Mokėjimo grafikas ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Mokėjimo grafiko eilutės ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Mokėjimo sąlygos ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Kliento mokėjimo būdas ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Tiekėjo mokėjimo būdas ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Klientų grupės ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Tiekėjų grupės ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| PVM grupės ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Prekės PVM grupės ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| PVM didžiosios knygos registravimo grupės V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Atleidimo nuo PVM kodo objektas „Common Data Service” ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| PVM rinkėjai ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| PVM kodai ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Žr. [1 pastabą](#fin-notes). |
| Finansinės dimensijos formatas ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Finansinės dimensijos ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Išskaitomų mokesčių grupės ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Išskaitomų mokesčių kodai ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Sąskaitų planas ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Didžioji knyga ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Žr. [1 pastabą](#fin-notes). |
| Pagrindinių sąskaitų kategorijos ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Pagrindinė sąskaita ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Klientai V3 ... sąskaitos                                                       | CustCustomerV3Entity                        | sąskaita                                    | Žr. [2 pastabą](#fin-notes). |
| Klientai V3 ... kontaktai                                                       | CustCustomerV3Entity                        | susisiekti                                    | Žr. [3 pastabą](#fin-notes). |
| Tiekėjai V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Žr. [2 pastabą](#fin-notes). |
| „Common Data Service” kontaktai V2 ... kontaktai                                    | smmContactPersonCommon Data ServiceV2Entity | susisiekti                                    | Žr. [4 pastabą](#fin-notes). |
| „Common Data Service” kontaktai V2 ... kontaktai                                    | smmContactPersonCommon Data ServiceV2Entity | susisiekti                                    | Žr. [5 pastabą](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Susiejimui būdingos pastabos

1. Vienakryptis sinchronizavimas vyksta iš „Finance and Operations” programų į „Common Data Service”.
2. Dėl vidinės priklausomybės gali reikėti paleisti pradinį sinchronizavimą keletą kartų. Įsitikinkite, kad pasirinkote **Klientas** kaip ryšio tipą, kai kuriate sąskaitą, naudodami puslapį **Sąskaitos**, esantį „Common Data Service”. Jei pirminio sinchronizavimo metu atsirado problemų su lauku **Pirminis kontaktas**, pašalinkite šį lauką iš susiejimo ir tada dar kartą vykdykite pradinį sinchronizavimą. Sėkmingai pasibaigus pradiniam sinchronizavimui, stabdykite susiejimą ir vėl prie jo pridėkite lauką **Pirminis kontaktas**. Tada paleiskite susiejimą, bet praleiskite pradinį sinchronizavimą. Lauko **Pirminis kontaktas** vertė nebus įtraukta į pradinį sinchronizavimą ir turėsite rankiniu būdu perkelti vertes.
3. Įsitikinkite, kad nustatėte parinktį **Parduodama** į **Taip** puslapyje **Kontaktai**, esančiame tarnyboje „Common Data Service”, kai bandysite sukurti tipo **Asmuo** klientą.
4. Šis susiejimas abiejose pusėse turi filtrą susieti kliento kontaktus. Atidarykite susiejimo išsamią informaciją, pasirinkite filtro mygtuką (piltuvėlio simbolį), esantį greta objekto pavadinimo **Sales.Contact** ir įsitikinkite, kad failo kriterijuose yra **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Šis susiejimas abiejose pusėse turi filtrą susieti tiekėjo kontaktus. Atidarykite susiejimo išsamią informaciją, pasirinkite filtro mygtuką (piltuvėlio simbolį), esantį greta objekto pavadinimo **Sales.Contact** ir įsitikinkite, kad filtro kriterijuose yra **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>„Dynamics 365 Human Resources“ objektai

Toliau nurodyti „Dynamics 365 Human Resources” objektai išvardyti tokia tvarka, kokia juos turite įjungti.

| Dvigubo rašymo funkcijos puslapyje esantis susiejimo pavadinimas | Objekto metaduomenų pavadinimas programoje „Human Resources“ | Objekto metaduomenų pavadinimas tarnyboje „Common Data Service” | Pastabos |
|---|---|---|---|
| cdm_jobfunction – užduoties funkcija                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes – užduočių tipai                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs – užduotys                                               |                                   | cdm_jobs                         | |
| cdm_jobs – užduoties išsami informacija                                        |                                   | cdm_jobs                         | |
| cdm_positiontype – PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions – pagrindinės pareigos                              | HcmPositionBaseEntity             | cdm_jobposition                  | Žr. [1 pastabą](#hr-notes). |
| cdm_jobposition – pareigų išsami informacija                            | HcmPositionDetailEntity           | cdm_jobposition                  | Žr. [1 pastabą](#hr-notes). |
| cdm_jobposition – pareigų trukmė                           | HcmPositionDurationEntity         | cdm_jobposition                  | Žr. [1 pastabą](#hr-notes). |
| cdm_jobposition – pareigų hierarchijos                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Žr. [1 pastabą](#hr-notes). |
| cdm_veteranstatus – seniai dirbančiojo būsena                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin – etninė kilmė                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode – kalbos kodas                              |                                   | cdm_languagecode                 | |
| cdm_worker – darbininkas                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments – įdarbininkai                                 |                                   | cdm_employments                  | |
| cdm_employments – įdarbinimo išsami informacija                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps – darbininko pareigų priskyrimas | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Žr. [2 pastabą](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Susiejimui būdingos pastabos

1. Vienas „Common Data Service” objektas susietas su keliais „Finance and Operations” programos objektais.
2. Šis susiejimas yra savo paties nuoroda.

## <a name="asset-management-entities"></a>Turto valdymo objektai

Toliau nurodyti „Dynamics 365 Supply Chain Management” turto valdymo objektai išvardyti tokia tvarka, kokia juos turite įjungti.

| Dvigubo rašymo funkcijos puslapyje esantis susiejimo pavadinimas | Objekto metaduomenų pavadinimas turto valdyme | Objekto metaduomenų pavadinimas tarnyboje „Common Data Service” | Pastabos |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Turto valdymo turto ciklo modelių būsenos               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Turto valdymo turto ciklo modeliai               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Turto valdymo funkcinių vietų ciklo modeliai | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Turto valdymo funkcinių vietų ciklo būsenos | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Turto valdymo turto tipai                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Turto valdymo funkcinių vietų tipai            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Turto valdymo funkcinės vietos                 | msdyn_functionallocations                | Žr. [pastabą](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Turto valdymo turtas                               | msdyn_customerassets                     | Žr. [pastabą](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Turto valdymo gamintojai                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Turto valdymo modeliai                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Turto valdymo garantija                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Susiejimui būdingos pastabos

- Dėl vidinės priklausomybės gali reikėti paleisti pradinį sinchronizavimą keletą kartų.
