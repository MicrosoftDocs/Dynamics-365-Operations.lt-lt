---
title: Bendrosios produkto funkcijos
description: Šiame straipsnyje aprašomas produkto duomenų integravimas tarp finansų ir operacijų programėlių ir Dataverse.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a8071887678f16a0b8ee075d2aa24a07e4df5319
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885004"
---
# <a name="unified-product-experience"></a>Vieninga produkto patirtis

[!include [banner](../../includes/banner.md)]



Kai verslo ekosistema sudaryta iš „Dynamics 365“ programų, pvz., „Finance“, „Supply Chain Management“ ir „Sales“, natūralu, įmonės šias programas dažnai naudoja kaip produktų duomenų šaltinį. Taip yra todėl, kad šios programos sudaro patikimą produktų infrastruktūrą, papildytą sudėtingomis kainodaros koncepcijomis ir tiksliais turimų atsargų duomenimis. Įmonės, kurios naudoja išorinę produkto gyvavimo ciklo valdymo (PLM) sistemą, skirtą produktų duomenims gauti, gali įtraukti produktus iš „Finance and Operations“ programų į kitas „Dynamics 365“ programas. Vieninga produkto patirtis įtraukia integruotą produkto duomenų modelį į „Dataverse“, kad visi programos vartotojai, įskaitant „Power Platform“ vartotojus, galėtų naudotis gausiais produktų duomenimis, kurie gaunami iš „Finance and Operations“ programų.

Čia yra produkto duomenų modelis iš „Sales“.

![CE produktų duomenų modelis.](media/dual-write-product-4.jpg)

Čia yra produkto duomenų modelis iš „Finance and Operations“ programų.

![Finansų ir operacijų produktų duomenų modelis.](media/dual-write-products-5.jpg)

Šie du produktų duomenų modeliai buvo integruoti į „Dataverse“, kaip parodyta toliau.

![„Dynamics 365“ programų duomenų modelis.](media/dual-write-products-6.jpg)

Dvigubo rašymo lentelių schemos produktams sukurtos taip, kad duomenys būtų tik vienpusiai, beveik realiuoju laiku nuo finansų ir operacijų programėlių iki Dataverse. Tačiau produkto infrastruktūra buvo padaryta atvira, kad ją, esant poreikiui, būtų galima padaryti dvikrypte. Nors galite ją tinkinti, tai darytumėte prisiimdami riziką sau, nes „Microsoft“ to daryti nerekomenduoja.

## <a name="templates"></a>Šablonai

Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas. Kaip parodyta toliau esančioje lentelėje, sukurtas lentelių schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.

„Finance and Operations” programos | Kitos „Dynamics 365” programos | Aprašymas
-----------------------|--------------------------------|---
[Visi produktai](mapping-reference.md#138) | msdyn_globalproducts | Visų produktų lentelėje pateikiami visi finansų ir operacijų programėleje esantys produktai – ir išleisti produktai, ir neišleisti produktai.
[CDS išleisti išskirtieji produktai](mapping-reference.md#213) | Produktas | Lentelėje **Produktas** yra stulpelių, apibrėžiančių produktą. Tai yra atskirų produktų (produktų su potipio produktu) ir produkto variantų informacija. Toliau esančioje lentelėje nurodyti ryšiai.
[Spalvos](mapping-reference.md#170) | msdyn\_productcolors
[Konfigūracijos](mapping-reference.md#171) | msdyn\_productconfigurations
[Numatytieji užsakymo parametrai](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Produkto kategorijos](mapping-reference.md#166) | msdyn_productcategories | Kiekviena produktų kategorija ir informacija apie jos struktūrą bei charakteristikas yra įtraukta į produktų kategorijos lentelę.
[Produktų kategorijos priskyrimai](mapping-reference.md#167) | msdyn_productcategoryassignments | Norint produktą priskirti kategorijai galima naudoti produktų kategorijų priskyrimų lentelę.
[Produktų kategorijų hierarchijos](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Produktų klasifikavimui ar grupavimui naudojamos produktų hierarchijos. Kategorijų hierarchijos galimos tarnyboje „Dataverse” naudojant produkto kategorijų hierarchijos lentelę.
[Produktų kategorijų hierarchijų vaidmenys](mapping-reference.md#169) | „msdyn_productcategoryhierarchyroles” | Produktų hierarchijas galima naudoti su skirtingais „D365 Finance and Operations“ vaidmenimis. Jomis nurodoma, kuri kategorija naudojama su kiekvienu vaidmeniu ar kuris naudojamas produktų kategorijos vaidmens lentelė.
[Produkto numatytieji užsakymo parametrai V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Produkto dimensijų grupės](mapping-reference.md#173) | msdyn\_productdimensiongroups | Produkto dimensijų grupė nustato, kurios produkto dimensijos apibrėžia produktą.
[Bendrojo produkto spalvos](mapping-reference.md#187) | msdyn_sharedproductcolors | Lentelė **Bendrojo produkto spalva** nurodo spalvas, kurias gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
[Bendrojo produkto konfigūracijos](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Lentelė **Bendrojo produkto konfigūracija** nurodo konfigūracijas, kurias gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
[Bendrojo produkto dydžiai](mapping-reference.md#190) | msdyn_sharedproductsizes | Lentelė **Bendrojo produkto dydis** nurodo dydžius, kurių gali būti konkretus bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
[Bendrojo produkto stiliai](mapping-reference.md#191) | msdyn_sharedproductstyles | Lentelė **Bendrojo produkto stilius** nurodo stilius, kuriuos gali turėti tam tikras bendrasis produktas. Siekiant užtikrinti duomenų vientisumą, ši koncepcija perkelta į „Dataverse“.
[Produkto numerio nustatytas brūkšninis kodas](mapping-reference.md#164) | msdyn\_productbarcodes | Produktų brūkšniniai kodai naudojami siekiant unikaliai identifikuoti produktus.
[Konkretaus produkto vieneto konvertavimai](mapping-reference.md#176) | „msdyn_productspecificunitofmeasureconversions” |
[Išleisti produktai V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | Lentelėje **ms bendraproductdetails\_** yra stulpeliai iš finansų ir operacijų programėlių, kurie apibrėžia produktą, ir kuriuose yra produkto finansinė ir valdymo informacija.
[Dydžiai](mapping-reference.md#174) | msdyn\_productsizes
[Saugojimo dimensijų grupės](mapping-reference.md#177) | „msdyn_productstoragedimensiongroups” | Produkto saugojimo dimensijų grupė yra metodas, naudojamas nurodyti produkto patalpinimą sandėlyje.
[Stiliai](mapping-reference.md#178) | msdyn\_productsytles
[Sekimo dimensijų grupės](mapping-reference.md#179) | „msdyn_producttrackingdimensiongroups” | Produkto sekimo dimensijų grupė yra metodas, naudojamas produkto atsargų sekimui.
[Vienetai](mapping-reference.md#219) | mat. vnt.
[Vienetų konvertavimas](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Produktų integravimas

Šiame modelyje produktą atitinka dviejų lentelių kombinacija „Dataverse“: **Produktas** ir **msdyn\_sharedproductdetails**, kombinacija. Pirmoji lentelė apima produkto apibrėžtį (unikalų produkto identifikatorių, produkto pavadinimą ir aprašą), o antroji lentelė apima laukus, saugomus produkto lygyje. Šių dviejų lentelių kombinacija yra naudojama produktui apibrėžti pagal sandėliavimo vieneto (SKU) koncepciją. Kiekvieno išleisto produkto informacija bus įrašyta minėtose lentelėse (produkto ir bendrai naudojamo produkto informacija). Visiems produktams (išleistiems ir neišleistiems) sekti naudojama **Visuotiniai produktai** lentelė.

Kadangi produktą atitinka SKU, išskirtųjų produktų, bendrųjų produktų ir produkto variantų koncepcijas „Dataverse“ galima gauti tokiu būdu:

- **Produktai su potipio produktu** yra patys save apibrėžiantys produktai. Nereikia nurodyti jokių dimensijų. Pavyzdys yra konkreti knyga. Šiems produktams viena eilutė sukuriama **Produkto** lentelė, o kita eilutė sukuriama **msdyn\_sharedproductdetails** lentelėje. Nesukuriama produktų šeimos eilutė.
- **Bendrieji produktai** naudojami kaip bendri produktai, turintys aprašą ir taisykles, apibrėžiančias verslo procesų veikimo būdą. Remiantis šiais apibrėžimais galima generuoti išskirtuosius produktus, žinomus kaip produkto variantus. Pavyzdžiui, marškinėliai yra bendrasis produktas, kuris gali turėti spalvos ir dydžio dimensijas. Galima kurti variantus, turinčius skirtingas šių dimensijų kombinacijas, pavyzdžiui, mažus mėlynus marškinėlius arba vidutinio dydžio žalius marškinėlius. Integruojant produkto lentelėje sukuriama viena eilutė kiekvienam variantui. Ši eilutė apima konkretaus varianto informaciją, pavyzdžiui, skirtingas dimensijas. Bendroji produkto informacija saugoma **msdyn\_sharedproductdetails** lentelėje. (Ši bendra informacija laikoma produkto vadove.) Produkto vadovo informacija sinchronizuojama į „Dataverse“ iš karto po to, kai išleistas produkto vadovas yra sukuriamas (prieš tai kai išleidžiami variantai).
- **Išskirtieji produktai** nurodo visus produktų potipio produktus ir visus produkto variantus.

![Produktų duomenų modelis.](media/dual-write-product.png)

Įgalinus dvigubo rašymo funkciją, produktai iš finansų ir operacijų bus sinchronizuoti kituose "Dynamics 365" produktuose, kurių būsena **Juodraštis**. Jie įtraukiami į pirmą kaininių sąrašą ta pačia valiuta, naudojama klientų įsipareigojimo programoje ir kai kurių sąrašų pavadinime naudojant abėcėlės rikiavimo tvarka. Kitaip tariant, jie įtraukiami į pirmą programos "Dynamics 365" kainų sąrašą, kuris atitinka jūsų legalios lentelės valiutą, kurioje produktas pateikiamas finansų ir operacijų programoje. Jei nėra pateiktos valiutos kainoraščio, jis bus automatiškai sukurtas ir priskirtas produktui.

Dabartinis dvigubo rašymo parametrų diegimas, kuris susieja numatytąjį kainų sąrašą su vienetu, ieškoti valiutos, susijusios su finansų ir operacijų programa, ir rasti pirmą kainų sąrašą kliento įsipareigojimų programoje kainų sąrašo pavadinime abėcėlės tvarka. Norėdami nustatyti numatytąjį tam tikros valiutos kainoraštį, kai yra keletas tos valiutos kainoraščių, turite atnaujinti kainoraščio pavadinimą į tokį, kuris pagal abėcėlės tvarką yra ankstesnis nei bet kuris kitas tos pačios valiutos kainoraštis. Jei ji neturi jokio kainos sąrašo pateiktai valiutai, sukuriama nauja.

Pagal numatytuosius parametrus „Finance and Operations“ programų produktai su kitomis „Dynamics 365“ programomis sinchronizuojami būdami būsenos **Juodraštis**. Norint sinchronizuoti produktą, jam esant būsenos **Aktyvus**, kad jį, pavyzdžiui, galėtumėte tiesiogiai naudoti pardavimo užsakymų pasiūlymuose, reikia pasirinkti šį parametrą: skirtuke **Sistema > Administravimas > Sistemos administravimas > Sistemos parametrai > Pardavimas** pasirinkite **Kurti aktyvios būsenos produktus = taip**.

Kai produktai sinchronizuojami, **finansų** ir operacijų programoje turite įvesti pardavimo vieneto lauko vertę, nes tai yra privalomas pardavimo laukas.

Produktų šeimų kūrimas „Dynamics 365 Sales” nepalaikomas su produktų dvigubo rašymo sinchronizavimu.

Produktų sinchronizavimas vyksta iš finansų ir operacijų programos į Dataverse. Tai reiškia Dataverse, kad produktų lentelės stulpelių vertes galima keisti, bet kai sinchronizavimas paleidžiamas (kai produkto stulpelis modifikuojamas finansų ir operacijų programoje), Dataverse vertės bus perrašomos.

„Finance and operations” programos | „Customer engagement“ programos |
---|---
[CDS išleisti išskirtieji produktai](mapping-reference.md#213) | Produktas |
[Išleisti produktai V2](mapping-reference.md#189) | „msdyn_sharedproductdetails” |
[Visi produktai](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Produktų dimensijos

Produkto dimensijos – tai charakteristikos, identifikuojančios produkto variantą. Keturios produkto dimensijos (spalva, dydis, stilius ir konfigūracija) taip pat yra susietos su „Dataverse“ ir apibrėžia produkto variantus. Toliau pateiktame paveikslėlyje parodytas produkto spalvos dimensijos duomenų modelis. Tas pats modelis taikomas dydžiams, stiliams ir konfigūracijoms.

![Produkto dimensijų duomenų modelis.](media/dual-write-product-two.png)

„Finance and operations” programos | „Customer engagement“ programos |
---|---
[Spalvos](mapping-reference.md#170) | msdyn\_productcolors
[Dydžiai](mapping-reference.md#174) | msdyn\_productsizes
[Stiliai](mapping-reference.md#178) | msdyn\_productsytles
[Konfigūracijos](mapping-reference.md#171) | msdyn\_productconfigurations

Kai produkto dimensijos skiriasi (pvz., bendrasis produktas kaip produkto dimensjas turi dydį ir spalvą), kiekvienas išskirtasis produktas (t. y. kiekvienas produkto variantas) apibrėžiamas kaip šių produkto dimensijų derinys. Pavyzdžiui, produkto numeris B0001 yra ypač maži juodi marškinėliai, o produkto numeris B0002 yra maži juodi marškinėliai. Šiuo atveju apibrėžiami esami produkto dimensijų deriniai. Pavyzdžiui, marškinėliai iš prieš tai pateikto pavyzdžio gali būti ypač maži ir juodi, maži ir juodi, vidutinio dydžio ir juodi arba dideli ir juodi, bet jie negali būti ypač didelį ir juodi. Kitaip tariant, nurodomos galimos bendrojo produkto dimensijos, o variantai gali būti išleidžiami naudojant šias vertes.

Tam, kad būtų galima sekti produkto dimensijas, kurias gali turėti bendrasis produktas, kiekvienai produkto dimensijai „Dataverse“ sukuriamos ir susiejamos toliau nurodytos lentelės. Išsamesnės informacijos žr. [Product information overview](../../../../supply-chain/pim/product-information.md).

„Finance and operations” programos | „Customer engagement“ programos |
---|---
[Bendrojo produkto spalvos](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Bendrojo produkto konfigūracijos](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Bendrojo produkto dydžiai](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Bendrojo produkto stiliai](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Produkto numerio nustatytas brūkšninis kodas](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Numatytieji užsakymo parametrai ir su konkrečiu produktu susiję numatytieji užsakymo parametrai

Numatytuose užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Ši informacija pasiekiama tarnyboje „Dataverse“ naudojant numatytųjų užsakymo parametrų ir su konkrečiu produktu susijusių numatytųjų užsakymo parametrų objektą. Daugiau informacijos apie funkciją galite rasti Numatytųjų užsakymo [parametrų straipsnyje](../../../../supply-chain/production-control/default-order-settings.md).

„Finance and operations” programos | „Customer engagement“ programos |
---|---
[Numatytieji užsakymo parametrai](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Produkto numatytieji užsakymo parametrai V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Matavimo vienetas ir matavimo vieneto konvertavimai

Matavimo vienetai ir atitinkamas konvertavimas pasiekiami „Dataverse“ pagal diagramoje pavaizduotą duomenų modelį.

![Matavimo vieneto duomenų modelis.](media/dual-write-product-three.png)

Matavimo vieneto koncepcija yra integruota į „Finance and Operations“ programas ir kitas „Dynamics 365“ programas. Kiekvienai vieneto klasei „Finance and Operations“ programoje sukuriama vieneto grupė „Dynamics 365“ programoje, kurioje yra vienetai, priklausantys vieneto klasei. Kiekvienai vieneto grupei taip pat sukuriamas numatytasis pradinis vienetas.

„Finance and operations” programos | „Customer engagement“ programos |
---|---
[Konkretaus produkto vieneto konvertavimai](mapping-reference.md#176) | „msdyn_productspecificunitofmeasureconversions” |
[Vienetai](mapping-reference.md#219) | mat. vnt.
[Vienetų konvertavimas](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Pradinis sutampančių „Finance and Operations“ ir „Dataverse“ vienetų duomenų sinchronizavimas

### <a name="initial-synchronization-of-units"></a>Pradinis vienetų sinchronizavimas

Kai įjungta dvigubo rašymo funkcija, „Finance and Operations“ programų vienetai sinchronizuojami su kitomis „Dynamics 365“ programomis. Vienetų grupės, sinchronizuotos iš finansų ir operacijų Dataverse programėlių, turi vėliavų rinkinį, kuris nurodo, kad jos yra "Iš išorės tvarkomos".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Sutampantys vienetų ir vienetų klasių / grupių duomenys iš „Finance and Operations“ bei kitų „Dynamics 365“programų

Pirmiausia svarbu pažymėti, kad vieneto integravimo raktas yra msdyn_symbol. Todėl ši reikšmė tarnyboje „Dataverse“ ar kitose „Dynamics 365“ programose turi būti unikali. Kadangi kitose "Dynamics 365" programėlėse tai yra pora "Vienetų grupės ID" ir "Pavadinimas", kuri apibrėžia vieneto unikalumą, Dataverse turite apsvarstyti skirtingus vienetų duomenų atitikimo tarp finansų ir operacijų programėlių scenarijus ir.

Kai vienetai sutampa / persidengia „Finance and Operations“ programose ir kitose „Dynamics 365“ programose

+ **Vienetas priklauso kitose „Dynamics 365“ programose esančiai vienetų grupei, kuri atitinka susietą vienetų klasę „Finance and Operations“ programose**. Šiuo atveju stulpelyje, msdyn_symbol "Dynamics 365" programėlėse, turi būti užpildytas vieneto simbolis iš finansų ir operacijų programėlių. Taip gretinant duomenis vienetų grupė kitose „Dynamics 365“ programose bus nustatyta kaip „Tvarkoma išorėje”.
+ **Vienetas priklauso kitose „Dynamics 365“ programose esančiai vienetų grupei, kuri neatitinka susietos vienetų klasės „Finance and Operations“ programose („Finance and Operations“ programose nėra vienetų klasės, skirtos kitose „Dynamics 365“ programose esančiai vienetų klasei).** Tokiu atveju lauką msdyn_symbol reikia užpildyti atsitiktine eilute. Atkreipkite dėmesį, kad ši reikšmė kitose „Dynamics 365“ programose turi būti unikali.

Kai „Finance and Operations“ vienetų ir vienetų klasių kitose „Dynamics 365“ programose nėra

Kaip dvigubo rašymo vienetų grupių iš finansų ir operacijų programėlių dalis ir šie atitinkami vienetai sukuriami ir sinchronizuojami kitose "Dynamics 365" programėlėse Dataverse, o vienetų grupė bus nustatyta kaip "Iš išorės tvarkoma". Nereikia atlikti jokių papildomų perkrovimo veiksmų.

Kai kitose „Dynamics 365“ programose esančių vienetų nėra „Finance and Operations“ programose

Stulpelį „msdyn_symbol” reikia užpildyti visuose vienetuose. Vienetus visada galima sukurti atitinkamoje „Finance and Operations“ programų vienetų klasėje (jei tokia yra). Jei vieneto klasės nėra, pirmiausia reikia sukurti vieneto klasę (atkreipkite dėmesį, kad finansų ir operacijų programėlių vieneto klasės negalima sukurti, išskyrus plėtinį, jei išplečiate išvardijimo), atitinkančią kitą "Dynamics 365" programėlių vienetų grupę. Tada galite sukurti vienetą. Atkreipkite dėmesį, kad vieneto simbolis „Finance and Operations“ programose turi būti msdyn_symbol, anksčiau nurodytas kaip vieneto simbolis kitose „Dynamics 365“programose.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktų strategijos: dimensija, sekimas ir saugojimo grupės

Produktų strategijos yra strategijų rinkiniai, naudojami produktams apibrėžti ir aprašyti atsargų charakteristikoms. Produkto dimensijų grupę, produkto sekimo dimensijų grupę ir saugojimo dimensijų grupę galima rasti kaip produkto strategijas.

„Finance and operations” programos | „Customer engagement“ programos |
---|---
[Produkto dimensijų grupės](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Saugojimo dimensijų grupės](mapping-reference.md#177) | „msdyn_productstoragedimensiongroups” |
[Sekimo dimensijų grupės](mapping-reference.md#179) | „msdyn_producttrackingdimensiongroups” |

## <a name="product-hierarchies"></a>Produktų hierarchijos

„Finance and operations” programos | „Customer engagement“ programos |
---|---
[Produktų kategorijos priskyrimai](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Produktų kategorijų hierarchijos](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Produktų kategorijų hierarchijų vaidmenys](mapping-reference.md#169) | „msdyn_productcategoryhierarchyroles” |

## <a name="integration-key-for-products"></a>Produktų integravimo raktas

Siekiant unikaliai identifikuoti „Dynamics 365 for Finance and Operations“ ir „Dataverse“ produktus, naudojami integravimo raktai.
Tarnyboje „Dataverse“ produktas identifikuojamas unikaliu raktu **(productnumber)**. Jį sudaro jungtinis elementas **(company, msdyn_productnumber)**. **company** nurodo „Finance and Operations“ juridinį subjektą, o **msdyn_productnumber** – konkretaus „Finance and Operations“ produkto numerį.

Kitų „Dynamics 365“ programų vartotojams produktas vartotojo sąsajoje identifikuojamas kaip **msdyn_productnumber** (atkreipkite dėmesį, kad stulpelio žyma yra **Produkto numeris**). Produkto formoje rodoma ir company, ir msydn_productnumber. Tačiau stulpelis („productnumber”) – unikalus produkto raktas – nerodomas.

Jei kuriate programas, naudodami „Dataverse“, turėtumėte atkreipti dėmesį į **productnumber** (unikalaus produkto ID) naudojimą kaip integravimo kodą. Nenaudokite **msdyn_productnumber**, nes jis nėra unikalus.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Pradinis produktų sinchronizavimas ir duomenų perkėlimas iš „Dataverse“ į „Finance and Operations“

### <a name="initial-synchronization-of-products"></a>Pradinis produktų sinchronizavimas

Kai įgalintas dvigubo rašymo funkcija, produktai iš finansų ir operacijų programėlių sinchronizuojami su klientų Dataverse įsipareigojimo programėle. Produktai, sukurti naudojant Dataverse "Dynamics 365" programėles prieš dvigubo rašymo išrašant, nebus atnaujinti arba sugretinti su produktų duomenimis iš finansų ir operacijų programėlių.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>„Finance and Operations“ ir kitų „Dynamics 365“ programų produktų duomenų gretinimas

Jei tie patys produktai saugomi (persidengia / sutampa) Dataverse finansuose ir operacijose bei kitose "Dynamics 365" programėlėse, kai įgalinsite dvigubo rašymo produktų sinchronizavimą iš finansų ir operacijų, Dataverse o tame pačiame produkte bus rodomos dubliuotų eilučių.
Kad išvengtų ankstesnės situacijos, jei kitos "Dynamics 365" programėlės turi produktų, kurie persidengia / sutampa su finansais ir operacijomis, **administratorius** turi paleisti stulpelių rašymo sąrašą įmonė (pavyzdžiui, "USMF") **ir msdyn_productnumber** (pvz., "1234:Black:S") prieš sinchronizuojant produktus. Kitaip tariant, į šiuos du produkto stulpelius reikia įvesti atitinkamą finansų ir operacijų įmonę, Dataverse su kuria turi būti sugretintas produktas, ir produkto numerį.

Tada įjungus ir vykdant sinchronizavimą „Finance and Operations“ produktai bus sinchronizuojami su sutampančiais „Dataverse“ ir kitų „Dynamics 365“ programų produktais. Tai taikoma ir išskirtiesiems produktams, ir produktų variantams.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Produktų duomenų perkėlimas iš kitų „Dynamics 365“ programų į „Finance and Operations“

Jei kitose "Dynamics 365" programėlėse yra produktų, kurių nėra finansuose ir operacijose, **administratorius pirmiausia gali naudoti EcoResReleasedProductCreationV2Entity** tų produktų importavimui į finansus ir operacijas. Be to, jis gali sugretinti „Finance and Operations“ ir kitų „Dynamics 365“ programų produktų duomenis, kaip aprašyta pirmiau.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
