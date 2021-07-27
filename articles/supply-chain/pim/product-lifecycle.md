---
title: Produkto ciklo būsenos apžvalga
description: Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną.
author: cvocph
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 0ebd482ad7dfde5393f4c03541a2ae1bca76ca7c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2021
ms.locfileid: "6340047"
---
# <a name="product-lifecycle-state-overview"></a>Produkto ciklo būsenos apžvalga

[!include [banner](../includes/banner.md)]

Produkto ciklo būsena nurodo išleisto produkto arba produkto varianto ciklo būseną. Produkto ciklo būsenas apibrėžia vartotojas, paprastai – produktų vadovas arba produktų bendrųjų duomenų vadovas. Konkrečius verslo procesus, pvz., bendrąjį planavimą, gali paveikti konkreti ciklo būsena.

Išleistą produktą arba produkto variantą galima susieti su produkto ciklo būsena, kuri nurodo, kokia yra esama konkretaus produkto arba varianto būsena. Galite nurodyti bet kokį produkto ciklo būsenų skaičių, priskirdami būsenos pavadinimą ir aprašą. Galite pasirinkti vieną ciklo būseną kaip numatytąją naujų išleistų produktų būseną. Išleisto produkto variantai perima produkto ciklo būseną iš atitinkamo išleisto bendrojo produkto, kai jie sukuriami. Keičiant išleisto bendrojo produkto ciklo būseną galima atnaujinti visus esamus variantus, kurių pradinė būsena tokia pati.  

## <a name="create-a-new-product-lifecycle-state"></a>Naujos produkto ciklo būsenos kūrimas

- Norėdami sukurti naują produkto gyvavimo ciklo būseną, žr. [Sukurkite naują produkto gyvavimo ciklo būseną](tasks/new-product-lifecycle-state.md).

- Norėdami sukurti numatytąją produkto gyvavimo ciklo būseną, žr. [Sukurkite numatytąją produkto gyvavimo ciklo būseną](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Produkto ciklo būsenos susiejimas su išleistais produktais  

Yra keli būdai, kaip galima susieti produkto ciklo būseną su išleistais produktais arba produkto variantais.

- Kuriant naują išleistą produktą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai.
- Išleidžiant produktą į juridinį subjektą, numatytoji **Produkto ciklo būsena** priskiriama automatiškai.
- Išleidžiant produkto variantą į juridinį subjektą, **Produkto ciklo būsena**, susieta su išleistu bendruoju produktu šiame juridiniame subjekte, automatiškai priskiriama naujam variantui.

Galite neautomatiškai atnaujinti produkto ciklo būseną, naudodami:

- sąrašo puslapį **Išleisti produktai** arba **Informacijos rodinys**;
- sąrašo puslapį **Išleisti produkto variantai** arba **Informacijos rodinys**.
- Raskite pasenusius produktus arba produkto variantus pagal paklausą ir susiekite ciklo būseną.  

Dėl išsamesnės informacijos:

- Norėdami susieti produkto gyvavimo ciklo būseną su išleisto produkto pagrindiniais duomenimis, žr. [Priskirti produkto gyvavimo ciklo būseną išleisto produkto pagrindiniams duomenims](tasks/product-lifecycle-state-released-product-master.md).

- Norėdami susieti produkto gyvavimo ciklo būseną su išleistu produktu, žr. [Priskirti produkto gyvavimo ciklo būseną išleisto produkto pagrindiniams duomenims](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Poveikis bendrajam planavimui

Produkto ciklo būsena turi tik vieną kontrolės žymę: **Galima planuoti**. Pagal numatytuosius parametrus šis parametras nustatytas į parinktį **Taip** visose sukurtose produkto ciklo būsenose, bet galima nustatyti parinktį **Ne**. Nustačius **Ne**, susieti išleisti produktai arba išleisti produkto variantai yra:

- neįtraukiami į bendrąjį planavimą;
- neįtraukiami į KS lygio skaičiavimą.

Dėl išsamios informacijos apie tai, kaip naudoti produkto gyvavimo ciklo būseną siekiant išmesti produktus ir pagrindinio planavimo ir BOM-level skaičiuoklės, žr. [Sukurti produkto gyvavimo ciklo būseną siekiant išmesti produktus iš pagrindinio planavimo](tasks/exclude-products-master-planning.md)

> [!NOTE]
> Siekiant padidinti efektyvumą, labai rekomenduojame susieti visus pasenusius išleistus produktus arba produkto variantus, ypač dirbant su vienkartinio produkto konfigūracijos variantais, su produkto ciklo būsena, kuri bendrajame planavime yra išjungta.  

## <a name="default-migration-import-and-export"></a>Numatytasis perėjimas, importavimas ir eksportavimas

Produktų ciklo būsenas palaiko duomenų objektai ir ciklo būseną galima nustatyti į kintamąją būseną naudojant arba išleisto produkto duomenų objektą, arba išleisto varianto duomenų objektą.

## <a name="find-obsolete-products-and-products-variants"></a>Pasenusių produktų ir produktų variantų radimas

Galite vykdyti modeliavimo analizę, norėdami rasti pasenusius išleistus produktus arba produkto variantus ir tada atnaujinti jų produkto ciklo būseną. Norėdami surasti nebegaliojančius produktus, žr. [Surasti nebegaliojančius produktų variantus ir priskirti produkto gyvavimo ciklo būseną](tasks/obsolete-product-variants.md). Šioje temoje aprašom, kaip surasti nebegaliojančius išleistus produktus ar jų variantus ir kaip susieti produkto gyvavimo ciklo būseną su nebegaliojančiais produktais. Jame taip pat parodoma, kaip peržiūrėti modeliavimo rezultatus ir įvertinti, kiek produktų ir produkto variantų bus susieti su nauja produkto ciklo būsena vykdant naujinimą be modeliavimo.  

Vykdydami analizę modeliavimo režimu, produktai ir produkto variantai, identifikuoti kaip pasenę, rodomi konkrečioje formoje, kurioje juos galima lengvai peržiūrėti. Atliekant analizę ieškoma operacijų ir konkrečių bendrųjų duomenų, kad būtų identifikuoti produktai, kurių poreikio nėra per kintantį laikotarpį ir iš poreikio negalima generuoti jokių bendrųjų duomenų. Naujų išleistų produktų per kintantį laikotarpį galima neįtraukti į analizę. Kai analizės modeliavimas pateikia numatytąjį rezultatą, vartotojas gali vykdyti analizę ir nustatyti visų produktų, kurie analizėje nurodyti kaip pasenę, naują produkto ciklo būseną.  

> [!NOTE]
> Atminkite, kad visą analizę ir naujinimą reikia atlikti tame pačiame juridiniame subjekte.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijai

Naudokite toliau nurodytus išleistų produktų arba produkto variantų pasirinkimo ir naujinimo kriterijus.

- Produkto arba produkto varianto produkto ciklo būsena turi skirtis nuo naujos norimos būsenos.
- Produktas arba produkto variantas buvo sukurtas prieš keletą dienų atsižvelgiant į dienų skaičių, kuris įvestas pasirinkimo dialogo lange.
- Nėra produkto arba produkto varianto atvirų gamybos užsakymų (= būsena < baigėsi).
- Nėra produkto arba produkto varianto atvirų atsargų operacijų (= būsena išdavimas ReservPhysical į QuotationIssue arba būsenos gavimas Registrered į QuotationReceipt).
- Nėra produkto arba produkto varianto atsargų operacijų per paskutines dienas.
- Nėra produkto arba produkto varianto ateities poreikio arba tiekimo prognozės.  
- Produkto arba produkto varianto minimalus atsargų lygis nenustatytas prekės padengime.
- Nėra produkto arba produkto varianto aktyvių fiksuoto kiekio „kanban“ taisyklių.  
- Nėra produkto arba produkto varianto aptarnavimo užsakymo eilučių.
- Nėra produkto arba produkto varianto aktyvių ar būsimų pardavimo arba pirkimo sutarties eilučių.
- Produktas arba produkto variantas nenaudojamas KS, susietoje su produkto arba varianto, kuris planavime nustatytas kaip aktyvus, nepasibaigusia patvirtinta KS versija.

## <a name="related-topics"></a>Susijusios temos

- [Naujos produkto ciklo būsenos kūrimas](tasks/new-product-lifecycle-state.md)
- [Numatytosios produkto ciklo būsenos kūrimas](tasks/default-product-lifecycle-state.md)
- [Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui](tasks/product-lifecycle-state-released-product-master.md)
- [Produkto ciklo būsenos priskyrimas išleistam produktui](tasks/product-lifecycle-state-released-product.md)
- [Pasenusių produkto variantų radimas ir produkto ciklo būsenos priskyrimas](tasks/obsolete-product-variants.md)
- [Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]