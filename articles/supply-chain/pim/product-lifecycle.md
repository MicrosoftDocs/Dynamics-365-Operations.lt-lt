---
title: "Produkto ciklo būsena"
description: "Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną."
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: conradv
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 236b0253f20330f09f07dbcfa19257350fb5d37f
ms.openlocfilehash: 8ef72de3f226a3270ac0145a20e4da7dfe64f4ba
ms.contentlocale: lt-lt
ms.lasthandoff: 02/08/2018

---

# <a name="product-lifecycle-state"></a>Produkto ciklo būsena 

[!include [banner](../includes/banner.md)]

Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną. Produkto ciklo būsenas apibrėžia vartotojas, paprastai – produktų vadovas arba produktų bendrųjų duomenų vadovas. Konkrečius verslo procesus, pvz., bendrąjį planavimą, gali paveikti konkreti ciklo būsena.   

Išleistą produktą arba produkto variantą galima susieti su produkto ciklo būsena, kuri nurodo, kokia yra esama konkretaus produkto arba varianto būsena. Galite nurodyti bet kokį produkto ciklo būsenų skaičių, priskirdami būsenos pavadinimą ir aprašą. Galite pasirinkti vieną ciklo būseną kaip numatytąją naujų išleistų produktų būseną. Išleisto produkto variantai perima produkto ciklo būseną iš atitinkamo išleisto bendrojo produkto, kai jie sukuriami. Keičiant išleisto bendrojo produkto ciklo būseną galima atnaujinti visus esamus variantus, kurių pradinė būsena tokia pati.  

## <a name="create-a-new-product-lifecycle-state"></a>Naujos produkto ciklo būsenos kūrimas 

- Norėdami kurti naują produkto ciklo būseną, paleiskite arba perskaitykite užduočių vedlį **Naujos produkto ciklo būsenos kūrimas**. 

-  Norėdami kurti numatytąją produkto ciklo būseną, paleiskite arba perskaitykite užduočių vedlį **Numatytosios produkto ciklo būsenos kūrimas**.   

## <a name="associate-product-lifecycle-states-to-released-products"></a>Produkto ciklo būsenos susiejimas su išleistais produktais  

Yra keli būdai, kaip galima susieti produkto ciklo būseną su išleistais produktais arba produkto variantais.

-  Kuriant naują išleistą produktą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai. 
-  Išleidžiant produktą į juridinį subjektą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai. 
-  Išleidžiant produkto variantą į juridinį subjektą, **Produkto ciklo būsena**, susieta su išleistu bendruoju produktu šiame juridiniame subjekte, automatiškai priskiriama naujam variantui. 

Galite neautomatiškai atnaujinti produkto ciklo būseną, naudodami: 

-    sąrašo puslapį **Išleisti produktai** arba **Informacijos rodinys**; 
-  sąrašo puslapį **Išleisti produkto variantai** arba **Informacijos rodinys**. 
-  Raskite pasenusius produktus arba produkto variantus pagal paklausą ir susiekite ciklo būseną.  

Norėdami išsamesnės informacijos apie tai, kaip susieti produkto ciklo būsenas, paleiskite arba perskaitykite du toliau nurodytus užduočių vedlius.

-  Norėdami susieti produkto ciklo būseną su išleistu bendruoju produktu, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui**. 

-  Norėdami susieti produkto ciklo būseną su išleistu produktu, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos priskyrimas išleistam produktui**. 

## <a name="impact-on-master-planning"></a>Poveikis bendrajam planavimui 

Produkto ciklo būsena turi tik vieną kontrolės žymę: **Galima planuoti**. Pagal numatytuosius parametrus šis parametras nustatytas į parinktį **Taip** visose sukurtose produkto ciklo būsenose, bet galima nustatyti parinktį **Ne**. Nustačius **Ne**, susieti išleisti produktai arba išleisti produkto variantai yra: 

-  neįtraukiami į bendrąjį planavimą; 
-  neįtraukiami į KS lygio skaičiavimą. 

Daugiau informacijos apie tai, kaip naudoti produkto ciklo būseną norint pašalinti produktus iš bendrojo planavimo ir lygio KS skaičiavimo, paleiskite arba perskaitykite užduočių vedlį **Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo**.

> [!NOTE]
> Siekiant padidinti efektyvumą, labai rekomenduojame susieti visus pasenusius išleistus produktus arba produkto variantus, ypač dirbant su vienkartinio produkto konfigūracijos variantais, su produkto ciklo būsena, kuri bendrajame planavime yra išjungta.  

## <a name="default-migration-import-and-export"></a>Numatytasis perėjimas, importavimas ir eksportavimas 

Produkto ciklo būsenų nepalaiko duomenų objektai ir ciklo būsenos negalima nustatyti į kintamąją būseną naudojant išleisto produkto duomenų objektus.

-  Vykdant perėjimą iš ankstesnių leidimų, visų produktų ir produkto variantų ciklo būsena bus nenurodyta.  
-  Kai importuojami išleisti produktai naudojant duomenų objektą, kuriant bus taikoma numatytoji ciklo būsena.  
-  Kai importuojami išleisti produkto variantai naudojant duomenų objektą, bus importuojama išleisto bendrojo produkto ciklo būsena.   

## <a name="find-obsolete-products-and-products-variants"></a>Pasenusių produktų ir produktų variantų radimas 

Galite vykdyti modeliavimo analizę, norėdami rasti pasenusius išleistus produktus arba produkto variantus ir tada atnaujinti jų produkto ciklo būseną. Norėdami rasti pasenusius produktus, paleiskite arba perskaitykite užduočių vedlį **Pasenusių produkto variantų radimas ir produkto ciklo būsenos priskyrimas**. Šiame užduočių vedlyje parodoma, kaip rasti pasenusius išleistus produktus arba produkto variantus ir kaip susieti produkto ciklo būseną su pasenusiais produktais. Jame taip pat parodoma, kaip peržiūrėti modeliavimo rezultatus ir įvertinti, kiek produktų ir produkto variantų bus susieti su nauja produkto ciklo būsena vykdant naujinimą be modeliavimo.  

Vykdydami analizę modeliavimo režimu, produktai ir produkto variantai, identifikuoti kaip pasenę, rodomi konkrečioje formoje, kurioje juos galima lengvai peržiūrėti. Atliekant analizę ieškoma operacijų ir konkrečių bendrųjų duomenų, kad būtų identifikuoti produktai, kurių poreikio nėra per kintantį laikotarpį ir iš poreikio negalima generuoti jokių bendrųjų duomenų. Naujų išleistų produktų per kintantį laikotarpį galima neįtraukti į analizę. Kai analizės modeliavimas pateikia numatytąjį rezultatą, vartotojas gali vykdyti analizę ir nustatyti visų produktų, kurie analizėje nurodyti kaip pasenę, naują produkto ciklo būseną.  

> [!NOTE]
> Atminkite, kad visą analizę ir naujinimą reikia atlikti tame pačiame juridiniame subjekte.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijai 

Naudokite toliau nurodytus išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijus. 

-    Produkto arba produkto varianto produkto ciklo būsena turi skirtis nuo naujos norimos būsenos. 
-  Produktas arba produkto variantas buvo sukurtas prieš keletą dienų atsižvelgiant į dienų skaičių, kuris įvestas pasirinkimo dialogo lange. 
-  Nėra produkto arba produkto varianto atvirų gamybos užsakymų (= būsena < baigėsi). 
-  Nėra produkto arba produkto varianto atvirų atsargų operacijų (= būsena išdavimas ReservPhysical į QuotationIssue arba būsenos gavimas Registrered į QuotationReceipt). 
-  Nėra produkto arba produkto varianto atsargų operacijų per paskutines dienas. 
-  Nėra produkto arba produkto varianto ateities poreikio arba tiekimo prognozės.  
-  Produkto arba produkto varianto minimalus atsargų lygis nenustatytas prekės padengime. 
-  Nėra produkto arba produkto varianto aktyvių fiksuoto kiekio „kanban“ taisyklių.  
-  Nėra produkto arba produkto varianto aptarnavimo užsakymo eilučių. 
-  Nėra produkto arba produkto varianto aktyvių ar būsimų pardavimo arba pirkimo sutarties eilučių. 
-  Produktas arba produkto variantas nenaudojamas KS, susietoje su produkto arba varianto, kuris planavime nustatytas kaip aktyvus, nepasibaigusia patvirtinta KS versija.

## <a name="related-topics"></a>Susijusios temos

-  [Naujos produkto ciklo būsenos kūrimas (užduočių vedlys)](tasks/new-product-lifecycle-state.md)
-  [Numatytosios produkto ciklo būsenos kūrimas (užduočių vedlys)](tasks/default-product-lifecycle-state.md)
-  [Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui (užduočių vedlys)](tasks/product-lifecycle-state-released-product-master.md)
-  [Produkto ciklo būsenos priskyrimas išleistam produktui (užduočių vedlys)](tasks/product-lifecycle-state-released-product.md)
-  [Pasenusių produkto variantų radimas ir produkto ciklo būsenos priskyrimas (užduočių vedlys)](tasks/obsolete-product-variants.md)
-  [Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo (užduočių vedlys)](tasks/exclude-products-master-planning.md)

