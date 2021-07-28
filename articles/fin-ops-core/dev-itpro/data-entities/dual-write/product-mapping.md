---
title: Vieninga produkto patirtis
description: Šioje temoje aprašomas produkto duomenų integravimas tarp programų „Finance and Operations“ ir „Dataverse“.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 115eaad4f11fc4fb5321f0d8bb9d4f5a9f2f2c7c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358598"
---
# <a name="unified-product-experience"></a>Bendrosios produkto funkcijos

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Kai verslo ekosistema sudaryta iš „Dynamics 365“ programų, pvz., „Finance“, „Supply Chain Management“ ir „Sales“, natūralu, įmonės šias programas dažnai naudoja kaip produktų duomenų šaltinį. Taip yra todėl, kad šios programos sudaro patikimą produktų infrastruktūrą, papildytą sudėtingomis kainodaros koncepcijomis ir tiksliais turimų atsargų duomenimis. Įmonės, kurios produkto duomenims gauti naudoja Produkto ciklo tapatybės valdymo sistemą, gali nukreipti produktus iš programų „Finance and Operations“ į kitas „Dynamics 365“ programas. Bendroji produkto funkcija leidžia integruoti produktų duomenų modelį į „Dataverse“, kad visi programų vartotojai, įskaitant „Power Platform“ vartotojus, galėtų naudotis išsamiais produktų, gaunamų iš „Finance and Operations“ programų, duomenimis.

Čia yra produkto duomenų modelis iš „Sales“.

![CE produktų duomenų modelis.](media/dual-write-product-4.jpg)

Čia pateiktas programų „Finance and Operations“ produktų duomenų modelis.

![„Finance and Operations“ produktų duomenų modelis.](media/dual-write-products-5.jpg)

Šie du produktų duomenų modeliai buvo integruoti į „Dataverse“, kaip parodyta toliau.

![„Dynamics 365“ programų duomenų modelis.](media/dual-write-products-6.jpg)

Produktų, turinčių dvigubą rašymą, lentelių schemos buvo sukurtos duomenų srautui tik į vieną pusę, beveik realiu laiku, iš programų „Finance and Operations“ į „Dataverse“. Tačiau produkto infrastruktūra buvo padaryta atvira, kad ją, esant poreikiui, būtų galima padaryti dvikrypte. Nors galite ją tinkinti, tai darytumėte prisiimdami riziką sau, nes „Microsoft“ to daryti nerekomenduoja.

## <a name="templates"></a>Šablonai

Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas. Kaip parodyta toliau esančioje lentelėje, sukurtas lentelių schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.

„Finance and Operations” programėlės | Kitos „Dynamics 365” programos | aprašymas
-----------------------|--------------------------------|---
Išleisti produktai V2 | msdyn\_sharedproductdetails | Lentelė **msdyn\_sharedproductdetails** apima programų „Finance and Operations“ stulpelius, kurie apibūdina produktą ir kuriuose yra produkto finansinė ir valdymo informacija. 
„Dataverse“ išleisti išskirtieji produktai | Produktas | Lentelėje **Produktas** yra stulpelių, apibrėžiančių produktą. Tai yra atskirų produktų (produktų su potipio produktu) ir produkto variantų informacija. Toliau esančioje lentelėje nurodyti ryšiai.
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
Bendrojo produkto spalvos | msdyn_sharedproductcolors | Lentelė **Bendrojo produkto spalva** nurodo spalvas, kurias gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
Bendrojo produkto dydžiai | msdyn_sharedproductsizes | Lentelė **Bendrojo produkto dydis** nurodo dydžius, kurių gali būti konkretus bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
Bendrojo produkto stiliai | msdyn_sharedproductstyles | Lentelė **Bendrojo produkto stilius** nurodo stilius, kuriuos gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
Bendrojo produkto konfigūracijos | msdyn_sharedproductconfigurations | Lentelė **Bendrojo produkto konfigūracija** nurodo konfigūracijas, kurias gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
Visi produktai | msdyn_globalproducts | Visų produktų lentelėje yra tiek jau išleisti produktai, tiek neišleisti produktai, ir juos galima rasti „Finance and Operations“ programose.
Vienetas | mat. vnt.
Vienetų konvertavimas | msdyn_ unitofmeasureconversions
Būdingo produkto matavimo vieneto konvertavimas | msdyn_productspecificunitofmeasureconversion
Produkto kategorijos | msdyn_productcategories | Kiekviena produktų kategorija ir informacija apie jos struktūrą bei charakteristikas yra įtraukta į produktų kategorijos lentelę. 
Produktų kategorijų hierarchijos | msdyn_productcategoryhierarhies | Produktų klasifikavimui ar grupavimui naudojamos produktų hierarchijos. Kategorijų hierarchijos galimos tarnyboje „Dataverse” naudojant produkto kategorijų hierarchijos lentelę. 
Produktų kategorijų hierarchijų vaidmenys | msdyn_productcategoryhierarchies | Produktų hierarchijos gali būti naudojamos skirtingoms „D365 Finance and Operations“ užduotims. Jomis nurodoma, kuri kategorija naudojama su kiekvienu vaidmeniu ar kuris naudojamas produktų kategorijos vaidmens lentelė. 
Produktų kategorijos priskyrimai | msdyn_productcategoryassignments | Norint produktą priskirti kategorijai galima naudoti produktų kategorijų priskyrimų lentelę.

## <a name="integration-of-products"></a>Produktų integravimas

Šiame modelyje produktą atitinka dviejų lentelių kombinacija „Dataverse“: **Produktas** ir **msdyn\_sharedproductdetails**, kombinacija. Pirmoji lentelė apima produkto apibrėžtį (unikalų produkto identifikatorių, produkto pavadinimą ir aprašą), o antroji lentelė apima laukus, saugomus produkto lygyje. Šių dviejų lentelių kombinacija yra naudojama produktui apibrėžti pagal sandėliavimo vieneto (SKU) koncepciją. Kiekvieno išleisto produkto informacija bus įrašyta minėtose lentelėse (produkto ir bendrai naudojamo produkto informacija). Visiems produktams (išleistiems ir neišleistiems) sekti naudojama **Visuotiniai produktai** lentelė. 

Kadangi produktą atitinka SKU, išskirtųjų produktų, bendrųjų produktų ir produkto variantų koncepcijas „Dataverse“ galima gauti tokiu būdu:

- **Produktai su potipio produktu** yra patys save apibrėžiantys produktai. Nereikia nurodyti jokių dimensijų. Pavyzdys yra konkreti knyga. Šiems produktams viena eilutė sukuriama **Produkto** lentelė, o kita eilutė sukuriama **msdyn\_sharedproductdetails** lentelėje. Nesukuriama produktų šeimos eilutė.
- **Bendrieji produktai** naudojami kaip bendri produktai, turintys aprašą ir taisykles, apibrėžiančias verslo procesų veikimo būdą. Remiantis šiais apibrėžimais galima generuoti išskirtuosius produktus, žinomus kaip produkto variantus. Pavyzdžiui, marškinėliai yra bendrasis produktas, kuris gali turėti spalvos ir dydžio dimensijas. Galima kurti variantus, turinčius skirtingas šių dimensijų kombinacijas, pavyzdžiui, mažus mėlynus marškinėlius arba vidutinio dydžio žalius marškinėlius. Integruojant produkto lentelėje sukuriama viena eilutė kiekvienam variantui. Ši eilutė apima konkretaus varianto informaciją, pavyzdžiui, skirtingas dimensijas. Bendroji produkto informacija saugoma **msdyn\_sharedproductdetails** lentelėje. (Ši bendra informacija laikoma produkto vadove.) Produkto vadovo informacija sinchronizuojama į „Dataverse“ iš karto po to, kai išleistas produkto vadovas yra sukuriamas (prieš tai kai išleidžiami variantai).
- **Išskirtieji produktai** nurodo visus produktų potipio produktus ir visus produkto variantus. 

![Produktų duomenų modelis.](media/dual-write-product.png)

Įgalinus dvigubo rašymo funkciją, „Finance and Operations“ programos bus sinchronizuojamos kituose „Dynamics 365“ produktuose, būsenoje **Juodraštis**. Jie yra pridedami prie pirmo kainoraščio su ta pačia valiuta. Kitaip tariant, jie pridedami prie pirmojo „Dynamics 365“ programos kainoraščio, atitinkančio jūsų juridinę lentelę, kurioje produktas išleidžiamas „Finance and Operations“ programoje, valiutą. Jei nėra pateiktos valiutos kainoraščio, jis bus automatiškai sukurtas ir priskirtas produktui. 

Dabartinis dvigubo rašymo priedų, kurie susieja numatytąjį kainoraštį su vienetu, diegimas ieško valiutos, susijusios su programa Finance and Operations, ir randa pirmą kainoraštį klientų įtraukimo programoje, naudodamas rūšiavimą abėcėlės tvarka kainoraščio pavadinime. Norėdami nustatyti numatytąjį tam tikros valiutos kainoraštį, kai yra keletas tos valiutos kainoraščių, turite atnaujinti kainoraščio pavadinimą į tokį, kuris pagal abėcėlės tvarką yra ankstesnis nei bet kuris kitas tos pačios valiutos kainoraštis.

Pagal numatytuosius nustatymus produktai, esantys programoje „Finance and Operations“, sinchronizuojami kitose „Dynamics 365“ programose, būsenoje **Juodraštis**. Norint sinchronizuoti produktą, jam esant būsenos **Aktyvus**, kad jį, pavyzdžiui, galėtumėte tiesiogiai naudoti pardavimo užsakymų pasiūlymuose, reikia pasirinkti šį parametrą: skirtuke **Sistema > Administravimas > Sistemos administravimas > Sistemos parametrai > Pardavimas** pasirinkite **Kurti aktyvios būsenos produktus = taip**. 

Kai produktai sinchronizuojami, „Finance and Operations” programos lauke **Pardavimo vienetas** turite įvesti reikšmę, nes tai yra privalomas „Sales” laukas.

Produktų šeimų kūrimas „Dynamics 365 Sales” nepalaikomas su produktų dvigubo rašymo sinchronizavimu.

Produktų sinchronizavimas vyksta iš „Finance and Operations“ programos į „Dataverse“. Tai reiškia, kad produkto lentelės stulpelių vertes galima pakeisti „Dataverse“, tačiau suaktyvinus sinchronizavimą (kai produkto stulpelis modifikuojamas „Finance and Operations“ programoje), bus perrašytos „Dataverse“ esančios vertės. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Produktų dimensijos 

Produkto dimensijos – tai charakteristikos, identifikuojančios produkto variantą. Keturios produkto dimensijos (spalva, dydis, stilius ir konfigūracija) taip pat yra susietos su „Dataverse“ ir apibrėžia produkto variantus. Toliau pateiktame paveikslėlyje parodytas produkto spalvos dimensijos duomenų modelis. Tas pats modelis taikomas dydžiams, stiliams ir konfigūracijoms. 

![Produkto dimensijų duomenų modelis.](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Kai produkto dimensijos skiriasi (pvz., bendrasis produktas kaip produkto dimensjas turi dydį ir spalvą), kiekvienas išskirtasis produktas (t. y. kiekvienas produkto variantas) apibrėžiamas kaip šių produkto dimensijų derinys. Pavyzdžiui, produkto numeris B0001 yra ypač maži juodi marškinėliai, o produkto numeris B0002 yra maži juodi marškinėliai. Šiuo atveju apibrėžiami esami produkto dimensijų deriniai. Pavyzdžiui, marškinėliai iš prieš tai pateikto pavyzdžio gali būti ypač maži ir juodi, maži ir juodi, vidutinio dydžio ir juodi arba dideli ir juodi, bet jie negali būti ypač didelį ir juodi. Kitaip tariant, nurodomos galimos bendrojo produkto dimensijos, o variantai gali būti išleidžiami naudojant šias vertes.

Tam, kad būtų galima sekti produkto dimensijas, kurias gali turėti bendrasis produktas, kiekvienai produkto dimensijai „Dataverse“ sukuriamos ir susiejamos toliau nurodytos lentelės. Išsamesnės informacijos žr. [Product information overview](../../../../supply-chain/pim/product-information.md). 

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Numatytieji užsakymo parametrai ir su konkrečiu produktu susiję numatytieji užsakymo parametrai

Numatytuose užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Ši informacija pasiekiama tarnyboje „Dataverse“ naudojant numatytųjų užsakymo parametrų ir su konkrečiu produktu susijusių numatytųjų užsakymo parametrų objektą. Daugiau informacijos apie funkciją galite perskaityti [temoje Numatytieji užskaymų parametrai](../../../../supply-chain/production-control/default-order-settings.md).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Matavimo vienetas ir matavimo vieneto konvertavimai

Matavimo vienetai ir atitinkamas konvertavimas pasiekiami „Dataverse“ pagal diagramoje pavaizduotą duomenų modelį.

![Matavimo vieneto duomenų modelis.](media/dual-write-product-three.png)

Matavimo vieneto koncepcija yra integruota tarp programų „Finance and Operations“ ir kitų „Dynamics 365“ programų. Kiekvienai programos „Finance and Operations“ vienetų klasei „Dynamics 365“ programoje sukuriama vienetų grupė, kurioje yra vienetų klasei priklausantys vienetai. Kiekvienai vieneto grupei taip pat sukuriamas numatytasis pradinis vienetas. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Pradinis vienetų duomenų suderinimo tarp „Finance and Operations“ ir „Dataverse“ sinchronizavimas

### <a name="initial-synchronization-of-units"></a>Pradinis vienetų sinchronizavimas

Įgalinus dvigubo rašymo funkciją, programų „Finance and Operations“ vienetai sinchronizuojami su kitomis „Dynamics 365“ programomis. Vienetų grupės, susinchronizuotos iš „Finance and Operations“ programų, esančių „Dataverse“, yra pažymėtos vėliavėle, kuri rodo, kad jos yra „Tvarkomos išorėje“.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Vienetų ir vienetų klasių / grupių duomenų suderinimas iš „Finance and Operations“ ir kitų „Dynamics 365“ programų

Pirmiausia svarbu pažymėti, kad vieneto integravimo raktas yra msdyn_symbol. Todėl ši reikšmė tarnyboje „Dataverse“ ar kitose „Dynamics 365“ programose turi būti unikali. Kadangi kitose „Dynamics 365“ programose yra pora „Vieneto grupės ID“ ir „Pavadinimas“, kuri apibrėžia vieneto unikalumą, reikia atsižvelgti į skirtingus būdus, kaip galima suderinti vienetų duomenis tarp programų „Finance and Operations“ ir „Dataverse“.

Skirta vienetams, atitinkantiems / sutampantiems programose „Finance and Operations“ ir kitose „Dynamics 365“ programose.

+ **Kitose „Dynamics 365“ programose vienetas priklauso vienetų grupei, kuri atitinka susietą vienetų klasę programose „Finance and Operations“**. Tokiu atveju, stulpelis „msdyn_symbol“ kitose „Dynamics 365“ programose turi būti užpildytas vieneto simboliu iš „Finance and Operations“ programų. Taip gretinant duomenis vienetų grupė kitose „Dynamics 365“ programose bus nustatyta kaip „Tvarkoma išorėje”.
+ **Vienetas priklauso vienetų grupei kitose „Dynamics 365“ programose, kurios neatitinka susietos vienetų klasės programose „Finance and Operations“ (vienetų klasė neegzistuoja programose „Finance and Operations“, skirtose vienetų klasei kitose „Dynamics 365“ programose).** Tokiu atveju lauką msdyn_symbol reikia užpildyti atsitiktine eilute. Atkreipkite dėmesį, kad ši reikšmė kitose „Dynamics 365“ programose turi būti unikali.

Jei vienetai ir vienetų klasės, esančios programose „Finance and Operations“, neegzistuoja kitose „Dynamics 365“ programose:

Kaip dvigubo rašymo funkcijos dalis, vienetų grupės, esančios „Finance and Operations“ programose, ir jas atitinkantys vienetai yra sukuriami ir sinchronizuojami kitose „Dynamics 365“ programose ir „Dataverse“, o vienetų grupė nustatoma kaip „Tvarkoma išorėje“. Nereikia atlikti jokių papildomų perkrovimo veiksmų.

Skirta vienetams kitose „Dynamics 365“ programose, kurie neegzistuoja programose „Finance and Operations“.

Stulpelį „msdyn_symbol” reikia užpildyti visuose vienetuose. Vienetus visada galima sukurti programose „Finance and Operations“, atitinkamoje vienetų klasėje (jei ji egzistuoja). Jei vieneto klasės nėra, pirmiausia reikia sukurti vienetų klasę (įsidėmėkite, kad vienetų klasės negalite sukurti „Finance and Operations“ programose, išskyrus atvejus, kai praplečiate išvardijimą), atitinkančią kitą „Dynamics 365“ programų vienetų grupę. Tada galite sukurti vienetą. Įsidėmėkite, kad vieneto simbolis programose „Finance and Operations“ turi būti „msdyn_symbol“, kuris nurodytas anksčiau kitose vieneto „Dynamics 365“ programose.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktų strategijos: dimensija, sekimas ir saugojimo grupės

Produktų strategijos yra strategijų rinkiniai, naudojami produktams apibrėžti ir aprašyti atsargų charakteristikoms. Produkto dimensijų grupę, produkto sekimo dimensijų grupę ir saugojimo dimensijų grupę galima rasti kaip produkto strategijas. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Produktų hierarchijos

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Produktų integravimo raktas 

Siekiant unikaliai identifikuoti „Dynamics 365 for Finance and Operations“ ir „Dataverse“ produktus, naudojami integravimo raktai. Tarnyboje „Dataverse“ produktas identifikuojamas unikaliu raktu **(productnumber)**. Jį sudaro jungtinis elementas **(company, msdyn_productnumber)**. **Įmonė** nurodo juridinį subjektą, esantį „Finance and Operations“, ir **„msdyn_productnumber“** nurodo konkretaus produkto „Finance and Operations“ produkto numerį. 

Kitų „Dynamics 365“ programų vartotojams produktas vartotojo sąsajoje identifikuojamas kaip **msdyn_productnumber** (atkreipkite dėmesį, kad stulpelio žyma yra **Produkto numeris**). Produkto formoje rodoma ir company, ir msydn_productnumber. Tačiau stulpelis („productnumber”) – unikalus produkto raktas – nerodomas. 

Jei kuriate programas, naudodami „Dataverse“, turėtumėte atkreipti dėmesį į **productnumber** (unikalaus produkto ID) naudojimą kaip integravimo kodą. Nenaudokite **msdyn_productnumber**, nes jis nėra unikalus. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Pradinis produktų ir duomenų perkėlimo iš „Dataverse“ į „Finance and Operations“ sinchronizavimas

### <a name="initial-synchronization-of-products"></a>Pradinis produktų sinchronizavimas 

Kai įjungta dvigubo rašymo funkcija, „Finance and Operations“ programos yra sinchronizuojamos su „Dataverse“ ir „Customer Engagement” programomis. Produktai, kurie buvo sukurti „Dataverse“ ir kitose „Dynamics 365“ programose prieš išleidžiant dvigubą rašymą, nebus atnaujinti arba suderinti su „Finance and Operations“ programų produktų duomenimis.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Produkto duomenų suderinimas iš „Finance and Operations“ ir kitų „Dynamics 365“ programų.

Jei „Finance and Operations“ ir „Dataverse“ bei kitose „Dynamics 365“ programose laikomi tie patys produktai (sutampa / atitinka), įgalinus dvigubo rašymo funkciją, susinchronizuojami produktai iš „Finance and Operations“, o eilučių kopijos atsiranda „Dataverse“ tam pačiam produktui.
Jei kitose „Dynamics 365“ programose yra produktų, kurie sutampa / atitinka „Finance and Operations“, tada prieš produktų susinchronizavimą, dvigubo rašymo funkciją įgalinantis administratorius privalo perkrauti stulpelius **Įmonė** (pavyzdžiui, „USMF“) ir **„msdyn_productnumber”** (pavyzdžiui, „1234: Black:S“). Kitaip tariant, šiuos du „Dataverse“ produkto stulpelius reikia užpildyti atitinkamai „Finance and Operations“ įmonei, kuriai produktas turi būti suderintas su produkto numeriu. 

Kai vyksta sinchronizacija, „Finance and Operations“ produktai sinchronizuojami su suderintais „Dataverse“ ir kitose „Dynamics 365“ programose esančiais produktais. Tai taikoma ir išskirtiesiems produktams, ir produktų variantams. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Produktų duomenų perkėlimas iš kitų „Dynamics 365“ programų į „Finance and Operations.“

Jei kitose „Dynamics 365“ programose yra produktų, kurių nėra „Finance and Operations“, administratorius pirmiausia gali naudoti **EcoResReleasedProductCreationV2Entity**, importuodamas tuos produktus į „Finance and Operations“. Taip pat suderinkite „Finance and Operations“ ir kitų „Dynamics 365“ programų produktų duomenis, kaip aprašyta aukščiau. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
