---
title: Vieninga produkto patirtis
description: Šioje temoje aprašomas produkto duomenų integravimas tarp „Finance and Operations“ programų ir „Common Data Service“.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
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
ms.openlocfilehash: bcc2c3d2530153a225a94fa0fb3cc990abbf65b4
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769734"
---
# <a name="unified-product-experience"></a>Vieninga produkto patirtis

[!include [banner](../includes/banner.md)]

Kai verslo ekosistema sudaryta iš „Dynamics 365“ programų, pvz., „Finance“, „Supply Chain Management“ ir „Sales“, natūralu, įmonės šias programas dažnai naudoja kaip produktų duomenų šaltinį. Taip yra todėl, kad šios programos sudaro patikimą produktų infrastruktūrą, papildytą sudėtingomis kainodaros koncepcijomis ir tiksliais turimų atsargų duomenimis. Įmonės, kurios naudoja išorinę produkto gyvavimo ciklo valdymo (PLM) sistemą, skirtą produktų duomenims gauti, gali įtraukti produktus iš „Finance and Operations“ programų į kitas „Dynamics 365“ programas. Vieninga produkto patirtis įtraukia integruotą produkto duomenų modelį į „Common Data Service“, kad visi programos vartotojai, įskaitant „Power Platform“ vartotojus, galėtų naudotis gausiais produktų duomenimis, kurie gaunami iš „Finance and Operations“ programų.

Čia yra produkto duomenų modelis iš „Sales“.

![CE produktų duomenų modelis](media/dual-write-product-4.jpg)

Čia yra produkto duomenų modelis iš „Finance and Operations“ programų.

![„Finance and Operations“ produktų duomenų modelis](media/dual-write-products-5.jpg)

Šie du produktų duomenų modeliai buvo integruoti į „Common Data Service“, kaip parodyta toliau.

![„Dynamics 365“ programų duomenų modelis](media/dual-write-products-6.jpg)

Produktų dvigubo rašymo objektų schemos sukurtos taip, kad duomenų perdavimas vyktų viena kryptimi beveik realiuoju laiku iš „Finance and Operations“ programų į „Common Data Service“. Tačiau produkto infrastruktūra buvo padaryta atvira, kad ją, esant poreikiui, būtų galima padaryti dvikrypte. Nors galite ją tinkinti, tai darytumėte prisiimdami riziką sau, nes „Microsoft“ to daryti nerekomenduoja.

## <a name="templates"></a>Šablonai

Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas. Kaip parodyta toliau esančioje lentelėje, sukurtas objektų schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.

„Finance and Operations” | Kitos „Dynamics 365” programos | Aprašymas
-----------------------|--------------------------------|---
Išleisti produktai V2 | msdyn\_sharedproductdetails | Objekte **msdyn\_sharedproductdetails** yra produktą apibrėžiantys laukai iš „Finance and Operations“ programų ir kuriuose pateikima produkto finansinė ir valdymo informacija. Toliau esančioje lentelėje nurodyti ryšiai.
„Common Data Service“ išleisti išskirtieji produktai | Produktas | Objekte **Produktas** yra laukų, kurie apibrėžia produktą. Tai yra atskirų produktų (produktų su potipio produktu) ir produkto variantų informacija. Toliau esančioje lentelėje nurodyti ryšiai.
Identifikuotas produkto numerio brūkšninis kodas | msdyn\_productbarcodes | Produktų brūkšniniai kodai naudojami siekiant unikaliai identifikuoti produktus.
Numatytieji užsakymo parametrai | msdyn\_productdefaultordersettings
Konkretaus produkto numatytieji užsakymo parametrai | msdyn_productdefaultordersettings
Produkto dimensijų grupės | msdyn\_productdimensiongroups | Produkto dimensijų grupė nustato, kurios produkto dimensijos apibrėžia produktą. 
Saugojimo dimensijų grupės | msdyn\_productstoragedimensiongroups | Produkto saugojimo dimensijų grupė yra metodas, naudojamas nurodyti produkto patalpinimą sandėlyje.
Sekimo dimensijų grupės | msdyn\_producttrackingdimensiongroups | Produkto sekimo dimensijų grupė yra metodas, naudojamas produkto atsargų sekimui.
Spalvos | msdyn\_productcolors
Dydžiai | msdyn\_productsizes
Stiliai | msdyn\_productsytles
Konfigūracijos | msdyn\_productconfigurations
Bendrojo produkto spalvos | msdyn_sharedproductcolors | Objektas **Bendrojo produkto spalva** nurodo spalvas, kurias gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Common Data Service“.
Bendrojo produkto dydžiai | msdyn_sharedproductsizes | Objektas **Bendrojo produkto dydis** nurodo dydžius, kurių gali būti konkretus bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Common Data Service“.
Bendrojo produkto stiliai | msdyn_sharedproductstyles | Objektas **Bendrojo produkto stilius** nurodo stilius, kuriuos gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Common Data Service“.
Bendrojo produkto konfigūracijos | msdyn_sharedproductconfigurations | Objektas **Bendrojo produkto konfigūracija** nurodo konfigūracijas, kurias gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Common Data Service“.
Visi produktai | msdyn_globalproducts | Visų produktų objektas apima visus „Finance and Operations“ pasiekiamus objektus, t. y. išleistus produktus ir neišleitus produktus.
Vienetas | mat. vnt.
Vienetų konvertavimas | msdyn_ unitofmeasureconversions
Būdingo produkto matavimo vieneto konvertavimas | msdyn_productspecificunitofmeasureconversion
Produkto kategorijos | msdyn_productcategories | Kiekviena produktų kategorija ir informacija apie jos struktūrą bei charakteristikas yra įtraukta į produktų kategorijos objektą. 
Produktų kategorijų hierarchijos | msdyn_productcategoryhierarhies | Produktų hierarchijos naudojamos produktus skirstant į kategorijas arba grupuojant. Kategorijų hierarchijos tarnyboje „Common Data Service“ pasiekiamos naudojant objektą Produktų kategorijų hierarchija. 
Produktų kategorijų hierarchijų vaidmenys | msdyn_productcategoryhierarchies | Produktų hierarchijas galima naudoti su skirtingais „D365 Finance and Operations“ vaidmenimis. Norint nurodyti, kuri kategorija naudojama su kiekvienu vaidmeniu, naudojamas produktų kategorijos vaidmens objektas su tolesnėmis sąsajomis. 
Produktų kategorijos priskyrimai | msdyn_productcategoryassignments | Norint produktą priskirti kategorijai, galima naudoti produktų kategorijų priskyrimų objektą.

## <a name="integration-of-products"></a>Produktų integravimas

Šiame modelyje produktą atitinka dviejų objektų kombinacija „Common Data Service“: **Produktas** ir **msdyn\_sharedproductdetails**, kombinacija. Pirmasis objektas apima produkto apibrėžtį (unikalų produkto identifikatorių, produkto pavadinimą ir aprašą), o antrasis objektas apima laukus, saugomus produkto lygyje. Šių dviejų objektų kombinacija naudojama produktui apibrėžti pagal sandėliavimo vieneto (SKU) koncepciją. Kiekvieno išleisto produkto informacija bus įrašyta minėtuose objektuose (produkto ir bendrai naudojamo produkto informacija). Visiems produktams (išleistiems ir neišleistiems) sekti naudojamas objektas **Visuotiniai produktai**. 

Kadangi produktą atitinka SKU, išskirtųjų produktų, bendrųjų produktų ir produkto variantų koncepcijas „Common Data Service“ galima gauti tokiu būdu:

- **Produktai su potipio produktu** yra patys save apibrėžiantys produktai. Nereikia nurodyti jokių dimensijų. Pavyzdys yra konkreti knyga. Šiems produktams vienas įrašas sukuriamas **produkto** objekte, o kitas įrašas sukuriamas **msdyn\_sharedproductdetails** objekte. Nesukuriamas produktų šeimos įrašas.
- **Bendrieji produktai** naudojami kaip bendri produktai, turintys aprašą ir taisykles, apibrėžiančias verslo procesų veikimo būdą. Remiantis šiais apibrėžimais galima generuoti išskirtuosius produktus, žinomus kaip produkto variantus. Pavyzdžiui, marškinėliai yra bendrasis produktas, kuris gali turėti spalvos ir dydžio dimensijas. Galima kurti variantus, turinčius skirtingas šių dimensijų kombinacijas, pavyzdžiui, mažus mėlynus marškinėlius arba vidutinio dydžio žalius marškinėlius. Integruojant, produkto lentelėje sukuriamas vienas įrašas kiekvienam variantui. Šis įrašas apima konkretaus varianto informaciją, pavyzdžiui, skirtingas dimensijas. Bendroji produkto informacija saugoma objekte **msdyn\_sharedproductdetails**. (Ši bendroji informacija saugoma bendrajame produkte.) Be to, kiekvienam bendrajam produktui sukuriamas vienas produktų šeimos įrašas. Bendrojo produkto informacija sinchronizuojama su Common Data Service sukūrus išleistą bendrąjį produktą (bet prieš išleidžiant variantus).
- **Išskirtieji produktai** nurodo visus produktų potipio produktus ir visus produkto variantus. 

![Produktų duomenų modelis](media/dual-write-product.png)

Įjungus dvigubo rašymo funkciją, programos iš „Finance and Operations“ bus sinchronizuotos su kitomis „Dynamics 365“ programomis, kurių būsena yra **Juodraštis.** Jie pridedami prie pirmo kainoraščio su ta pačia valiuta. Kitaip tariant, išleidžiant produktą programoje „Finance and Operations“, jie įtraukiami į pirmąjį kainoraštį „Dynamics 365“ programoje, kuris atitinka jūsų juridinio subjekto valiutą. 

Pagal numatytuosius parametrus „Finance and Operations“ programų produktai su kitomis „Dynamics 365“ programomis sinchronizuojami būdami būsenos **Juodraštis**. Norint sinchronizuoti produktą, jam esant būsenos **Aktyvus**, kad jį, pavyzdžiui, galėtumėte tiesiogiai naudoti pardavimo užsakymų pasiūlymuose, reikia pasirinkti šį parametrą: skirtuke **Sistema > Administravimas > Sistemos administravimas > Sistemos parametrai > Pardavimas** pasirinkite **Kurti aktyvios būsenos produktus = taip**. 

Atkreipkite dėmesį, kad produktai sinchronizuojami iš „Finance and Operations“ į „Common Data Service“. Tai reiškia, kad tarnyboje „Common Data Service“ produktų objektų laukų reikšmes keisti galima, tačiau, suaktyvinus sinchronizavimą (kai produkto laukas modifikuojamas „Finance and Operations“ programoje), „Common Data Service“ reikšmės bus perrašytos. 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [products](dual-write/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](dual-write/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](dual-write/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Produktų dimensijos 

Produkto dimensijos – tai charakteristikos, identifikuojančios produkto variantą. Keturios produkto dimensijos (spalva, dydis, stilius ir konfigūracija) taip pat yra susietos su „Common Data Service“ ir apibrėžia produkto variantus. Toliau pateiktame paveikslėlyje parodytas produkto spalvos dimensijos duomenų modelis. Tas pats modelis taikomas dydžiams, stiliams ir konfigūracijoms. 

![Produktų duomenų modelis](media/dual-write-product-2.PNG)

[!include [product colors](dual-write/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](dual-write/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](dual-write/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](dual-write/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Kai produkto dimensijos skiriasi (pvz., bendrasis produktas kaip produkto dimensjas turi dydį ir spalvą), kiekvienas išskirtasis produktas (t. y. kiekvienas produkto variantas) apibrėžiamas kaip šių produkto dimensijų derinys. Pavyzdžiui, produkto numeris B0001 yra ypač maži juodi marškinėliai, o produkto numeris B0002 yra maži juodi marškinėliai. Šiuo atveju apibrėžiami esami produkto dimensijų deriniai. Pavyzdžiui, marškinėliai iš prieš tai pateikto pavyzdžio gali būti ypač maži ir juodi, maži ir juodi, vidutinio dydžio ir juodi arba dideli ir juodi, bet jie negali būti ypač didelį ir juodi. Kitaip tariant, nurodomos galimos bendrojo produkto dimensijos, o variantai gali būti išleidžiami naudojant šias vertes.

Tam, kad būtų galima sekti produkto dimensijas, kurias gali turėti bendrasis produktas, kiekvienai produkto dimensijai „Common Data Service“ sukuriami ir susiejami toliau nurodyti objektai. Išsamesnės informacijos žr. [Product information overview](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](dual-write/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](dual-write/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](dual-write/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](dual-write/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](dual-write/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Numatytieji užsakymo parametrai ir konkretaus produkto numatytieji užsakymo parametrai

Numatytuose užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Ši informacija pasiekiama tarnyboje „Common Data Service“ naudojant numatytųjų užsakymo parametrų ir konkretaus produkto numatytųjų užsakymo parametrų objektą. Daugiau informacijos apie funkciją galite perskaityti [temoje Numatytieji užskaymų parametrai](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](dual-write/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](dual-write/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Matavimo vienetas ir matavimo vieneto konvertavimai

Matavimo vienetai ir atitinkami konvertavimai tarnyboje „Common Data Service“ pasiekiami pagal diagramoje pavaizduotą duomenų modelį.

![Produktų duomenų modelis](media/dual-write-product-3.PNG)

Matavimo vieneto koncepcija yra integruota į „Finance and Operations“ programas ir kitas „Dynamics 365“ programas. Kiekvienai vieneto klasei „Finance and Operations“ programoje sukuriama vieneto grupė „Dynamics 365“ programoje, kurioje yra vienetai, priklausantys vieneto klasei. Kiekvienai vieneto grupei taip pat sukuriamas numatytasis pradinis vienetas. 

[!include [unit of measure](dual-write/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](dual-write/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product specific unit of measure conversions](dual-write/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Pradinis sutampančių „Finance and Operations“ ir „Common Data Service“ vienetų duomenų sinchronizavimas

### <a name="initial-synchronization-of-units"></a>Pradinis vienetų sinchronizavimas

Kai įjungta dvigubo rašymo funkcija, „Finance and Operations“ programų vienetai sinchronizuojami su kitomis „Dynamics 365“ programomis. Su vienetų grupėmis, iš „Finance and Operations“ programų sinchronizuotomis į „Common Data Service“, pateikiamas vėliavėlių rinkinys, nurodantis, kad jos „Tvarkomos išorėje“.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Sutampantys vienetų ir vienetų klasių / grupių duomenys iš „Finance and Operations“ bei kitų „Dynamics 365“programų

Pirmiausia svarbu pažymėti, kad vieneto integravimo raktas yra msdyn_symbol. Todėl ši reikšmė tarnyboje „Common Data Service“ ar kitose „Dynamics 365“ programose turi būti unikali. Kadangi kitose „Dynamics 365“ programose vieneto unikalumą apibrėžia elementų Vienetų grupės ID ir Pavadinimas pora, turite apsvarstyti skirtingus scenarijus vienetų duomenims gretinti tarp „Finance and Operations“ programų ir „Common Data Service“.

Kai vienetai sutampa / persidengia „Finance and Operations“ programose ir kitose „Dynamics 365“ programose

+ **Vienetas priklauso kitose „Dynamics 365“ programose esančiai vienetų grupei, kuri atitinka susietą vienetų klasę „Finance and Operations“ programose**. Šiuo atveju kitose „Dynamics 365“ programose esantį lauką msdyn_symbol reikia užpildyti vieneto simboliu iš „Finance and Operations“ programų. Taip gretinant duomenis vienetų grupė kitose „Dynamics 365“ programose bus nustatyta kaip Tvarkoma išorėje.
+ **Vienetas priklauso kitose „Dynamics 365“ programose esančiai vienetų grupei, kuri neatitinka susietos vienetų klasės „Finance and Operations“ programose („Finance and Operations“ programose nėra vienetų klasės, skirtos kitose „Dynamics 365“ programose esančiai vienetų klasei).** Tokiu atveju lauką msdyn_symbol reikia užpildyti atsitiktine eilute. Atkreipkite dėmesį, kad ši reikšmė kitose „Dynamics 365“ programose turi būti unikali.

Kai „Finance and Operations“ vienetų ir vienetų klasių kitose „Dynamics 365“ programose nėra

Atliekant dvigubo rašymo procesą, „Finance and Operations“ programų vienetų grupės ir atitinkami vienetai kuriami bei sinchronizuojami kitose „Dynamics 365“ programose ir tarnyboje „Common Data Service“, o vienetų grupė bus nustatyta kaip Tvarkoma išorėje. Nereikia atlikti jokių papildomų perkrovimo veiksmų.

Kai kitose „Dynamics 365“ programose esančių vienetų nėra „Finance and Operations“ programose

Lauką msdyn_symbol reikia užpildyti visuose vienetuose. Vienetus visada galima sukurti atitinkamoje „Finance and Operations“ programų vienetų klasėje (jei tokia yra). Jei vienetų klasės nėra, pirmiausia reikia sukurti vienetų klasę (atkreipkite dėmesį, kad „Finance and Operations“ programose vienetų klasės kurti negalite, išskyrus išplėtimo situaciją, jei išplečiate išvardijimą), atitinkančią kitų „Dynamics 365“ programų vienetų grupę. Tada galite sukurti vienetą. Atkreipkite dėmesį, kad vieneto simbolis „Finance and Operations“ programose turi būti msdyn_symbol, anksčiau nurodytas kaip vieneto simbolis kitose „Dynamics 365“programose.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktų strategijos: dimensija, sekimas ir saugojimo grupės

Produktų strategijos yra strategijų rinkiniai, naudojami produktams apibrėžti ir aprašyti atsargų charakteristikoms. Produkto dimensijų grupę, produkto sekimo dimensijų grupę ir saugojimo dimensijų grupę galima rasti kaip produkto strategijas. 

[!include [product dimension group](dual-write/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](dual-write/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](dual-write/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Produktų hierarchijos

[!include [product category hierarchy](dual-write/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](dual-write/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](dual-write/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](dual-write/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Produktų integravimo raktas 

Siekiant unikaliai identifikuoti „Dynamics 365 for Finance and Operations“ ir „Common Data Service“ produktus, naudojami integravimo raktai. Tarnyboje „Common Data Service“ produktas identifikuojamas unikaliu raktu **(productnumber)**. Jį sudaro jungtinis elementas **(company, msdyn_productnumber)**. **company** nurodo „Finance and Operations“ juridinį subjektą, o **msdyn_productnumber** – konkretaus „Finance and Operations“ produkto numerį. 

Kitų „Dynamics 365“ programų vartotojui produktas vartotojo sąsajoje identifikuojamas kaip **msdyn_productnumber** (atkreipkite dėmesį, kad lauko žyma yra **Produkto numeris**). Produkto formoje rodoma ir company, ir msydn_productnumber. Tačiau laukas (productnumber) – unikalus produkto raktas – nerodomas. 

Atkreipkite dėmesį, kad, jei programos yra sukurtos „Common Data Service“ pagrindu, reikia ypač atkreipti dėmesį į tai, kad kaip integravimo raktas būtų naudojamas unikalus produkto ID, o ne msdyn_productnumber, nes pastarasis nėra unikalus. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Pradinis produktų sinchronizavimas ir duomenų perkėlimas iš „Common Data Service“ į „Finance and Operations“

### <a name="initial-synchronization-of-products"></a>Pradinis produktų sinchronizavimas 

Kai įjungta dvigubo rašymo funkcija, „Dynamics 365 Finance and Operations“ produktai sinchronizuojami su „Common Data Service“ ir kitomis „Dynamics 365“ programomis. Atkreipkite dėmesį, kad tarnyboje „Common Data Service“ ir kitose „Dynamics 365“ programose prieš dvigubą rašymą sukurti produktai nebus atnaujinami ar gretinami su produktų duomenimis iš „Finance and Operations“.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>„Finance and Operations“ ir kitų „Dynamics 365“ programų produktų duomenų gretinimas

Jei tie patys produktai laikomi (persidengia / sutampa) programoje „Finance and Operations“ ir tarnyboje „Common Data Service“ bei kitose „Dynamics 365“ programose, įjungus dvigubo rašymo funkciją bus sinchronizuojami „Finance and Operations“ produktai, o tarnyboje „Common Data Service“ atsiras pasikartojantys to paties produkto įrašai.
Siekdamas išvengti ankstesnės situacijos, jei kitose „Dynamics 365“ programose yra persidengiančių / sutampančių „Finance and Operations“ produktų, dvigubo rašymo funkciją įjungiantis administratorius prieš produktų sinchronizavimą turi perkrauti laukus **Įmonė** (pavyzdys: USMF) ir **msdyn_productnumber** (pavyzdys: 1234:Black:S). Kitaip tariant, į šiuos du „Common Data Service“ produkto laukus reikia įvesti atitinkamą „Finance and Operations“ įmonę, su kuria produktas turi sutapti, ir jos produkto numerį. 

Tada įjungus ir vykdant sinchronizavimą „Finance and Operations“ produktai bus sinchronizuojami su sutampančiais „Common Data Service“ ir kitų „Dynamics 365“ programų produktais. Tai taikoma ir išskirtiesiems produktams, ir produktų variantams. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Produktų duomenų perkėlimas iš kitų „Dynamics 365“ programų į „Finance and Operations“

Jei kitose „Dynamics 365“ programose yra produktų, kurių nėra programoje „Finance and Operations“, administratorius gali pirmiausia naudoti **EcoResReleasedProductCreationV2Entity**, kad tuos produktus importuotų į „Finance and Operations“. Be to, jis gali sugretinti „Finance and Operations“ ir kitų „Dynamics 365“ programų produktų duomenis, kaip aprašyta pirmiau. 
