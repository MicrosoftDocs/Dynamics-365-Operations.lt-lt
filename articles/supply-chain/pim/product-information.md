---
title: "Produktų informacijos peržiūra"
description: "Šioje temoje pateikiama informacijos apie produktų informacijos valdymą. Valdant produktų informaciją, dirbama su bendrinama produkto apibrėžtimi, kategorizacija ir identifikatoriais visuose juridiniuose subjektuose bei konkrečiomis produkto konfigūracijomis, kad būtų galima prisiderinti prie verslo procesų."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3a6a41f192b1c79f0f8ee40bf62c8b30ee7200c8
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="product-information-overview"></a>Produktų informacijos peržiūra

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Šioje temoje pateikiama informacijos apie produktų informacijos valdymą. Valdant produktų informaciją, dirbama su bendrinama produkto apibrėžtimi, kategorizacija ir identifikatoriais visuose juridiniuose subjektuose bei konkrečiomis produkto konfigūracijomis, kad būtų galima prisiderinti prie verslo procesų. 

Produktų informacija yra tiekimo grandinės ir mažmeninės prekybos programų pagrindas visose pramonės šakose. Ji nurodo procesus ir technologijas, kuriuos naudojant pirmiausia centralizuotai valdoma informacija apie produktus (pavyzdžiui, keliose tiekimo grandinėse). Labai svarbu, kad būtų naudojamos bendrinamos produktų apibrėžtys, dokumentacija, atributai ir identifikatoriai. Įvairiuose verslo sprendimo moduliuose būtina turėti konkretaus produkto informaciją ir konfigūraciją, kad būtų galima valdyti verslo procesus, susijusius su konkrečiais produktais, produktų šeimomis ar produktų kategorijomis.

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

Produkto apibrėžtį galima sukurti „Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidime. Ją taip pat galima importuoti iš produktų ciklo valdymo (PLM), produktų duomenų valdymo (PDM) ar produktų informacijos valdymo (PIM) sistemų. Kai naudojamas daugiau nei vienas „Finance and Operations‟ egzempliorius, vienas iš jų paprastai naudojamas kaip pagrindinis produktų duomenų egzempliorius visiems kitiems egzemplioriams. Taip daryti galima pasitelkiant didelę duomenų objektų grupę, kuriuos naudojant produktų apibrėžčių duomenis galima eksportuoti ir importuoti iš vieno egzemplioriaus į kitą.

Kad produktų duomenis galėtumėte platinti keliuose egzemplioriuose, „Finance and Operations‟ leidžia naudoti „Common Data Service‟. Produktų apibrėžtis iš „Finance and Operations‟ egzemplioriaus galima eksportuoti į „Common Data Service‟. Tada, naudojant produktų apibrėžtis, galima kitas verslo programas, pvz., „Microsoft Dynamics 365 for Sales‟, užpildyti produktų duomenimis.

Atkreipkite dėmesį, kad dinamiškose ir lanksčiose organizacijose produktų informacijos duomenys keičiasi kiekvieną dieną. Todėl tikslių ir faktinių produktų duomenų priežiūra yra labai svarbus atskiras verslo procesas.

## <a name="product-masters-and-product-variants"></a>Bendrieji produktai ir produktų variantai

Lanksčiame pasaulyje, kuriame produktus reikia greitai pritaikyti pagal klientų reikalavimus, produktų apibrėžtyse nurodomas produktų rinkinys, o ne išskirtieji produktai. Sprendime „Microsoft Dynamics 365 for Finance and Operations‟ tokie produktai vadinami *bendraisiais produktais*. Bendruosiuose produktuose apibrėžiama ir pateikiamos taisyklės, kaip išskirtieji produktai aprašomi ir veikia vykstant verslo procesams. Pagal šias apibrėžtis galima generuoti išskirtuosius produktus. Šie išskirtieji produktai vadinami *produktų variantais*.

Sprendime „Finance and Operations‟ bendrasis produktas susiejamas su produktų dimensijų grupe ir konfigūravimo technologija, kad būtų galima nurodyti verslo taisykles. Produktų dimensijos (Spalva, Dydis, Stilius ir Konfigūracija) yra konkretus atributų rinkinys, kurį naudojant programoje galima apibrėžti ir sekti konkretų susijusių produktų veikimą. Šios dimensijos taip pat vartotojams padeda ieškoti produktų ir juos nustatyti.

## <a name="configuration-technologies"></a>Konfigūravimo technologijos

Galite rinktis iš trijų konfigūravimo technologijų:

- Iš anksto apibrėžtus variantus apibrėžia iš anksto apibrėžtos produktų dimensijos. Į varianto apibrėžtį įeina konkretaus tinkamo dimensijų, pvz., Spalva, Stilius ir Dydis, derinio apibrėžtis. Kiekvienas derinys sukuria išskirtojo produkto variantą.
- Konfigūravimo pagal dimensijas funkcija paprastai naudojama gamybos situacijose ir apibrėžiant komplektavimo specifikacijas (KS) ji leidžia naudoti dimensiją Konfigūracija. Pasirinkus konkrečią konfigūraciją sistema naudoja tai konfigūracijai tinkamų planavimo ir gamybos KS eilučių pogrupį. Ši sąvoka taip pat vadinama *visuotine KS*, nes viena bendrai naudojama KS naudojama visoms produkto konfigūracijoms.
- Konfigūravimo pagal apribojimus funkcija naudoja produkto konfigūracijos modelį ir apibūdina visus galimus atributus ir komponentus, kurių reikia norint viename modelyje apibūdinti visus galimus produkto variantus. Atributų derinių apribojimus galima apibūdinti naudojant reguliariuosius reiškinius ar apribojimus pagal lenteles. Valdant produktų informaciją konfigūracijų modeliai ir konfigūratoriai tampa vis svarbesni ir yra naudojami visose pramonės šakose.

Planuojant diegti „Finance and Operations‟ labai svarbu verslo procesui parinkti tinkamą konfigūravimo technologiją. Įdiegus produkto negalima konvertuoti iš vieno modelio į kitą.

## <a name="product-variant-model-definition-workspace"></a>Darbo sritis Produktų variantų modelių apibrėžimas

Darbo srityje **Produktų variantų modelių apibrėžimas** apžvelgiami bendrieji produktai. Joje taip pat rodoma bendrųjų produktų ir susijusių variantų pateikimo konkretiems juridiniams subjektams būsena.

## <a name="released-products"></a>Patvirtinti produktai

Konkrečiam juridiniam subjektui pateikti produktai vadinami *pateiktais produktais*. Produktus vienu metu galima masiškai pateikti vienam juridiniam subjektui ar keliems juridiniams subjektams. Kadangi gali reikėti įtraukti įvairias atskiro juridinio subjekto produktų ypatybes ir atributus, darbo srityje **Pateiktų produktų priežiūra** galite stebėti ir užbaigti neseniai pateiktus produktus kiekviename juridiniame subjekte arba antrinėse juridinio subjekto organizacijose.

### <a name="released-product-maintenance-workspace"></a>Darbo sritis Pateiktų produktų priežiūra

Darbo sritį **Pateiktų produktų priežiūra** galite konfigūruoti pasirinkę meniu elementą **Konfigūruoti mano darbo sritį**. Pasirinkite kategorijų hierarchiją ir kategoriją, pagal kurias reikia filtruoti darbo sritį. Norėdami darbo srityje koreguoti aktualius produktų duomenis, taip pat galite dienomis apibrėžti **neseniai pateiktų produktų** ir **sustabdytų pateiktų produktų** laiko ribas.

Darbo sritį sudaro plytelių ir dviejų sąrašų suvestinė. Sąraše **Atviri atvejai** rodomi produktų keitimo atvejai, kai pasirinktos produktų kategorijų hierarchijos produktai nėra baigti ir uždaryti. Sąraše **Neseniai pateikti** rodomi produktai, pateikti laiko ribose, nustatytose darbo srities konfigūracijoje. Tikrinamas kiekvienas sąrašo elementas ir rodoma tikrinimo būsena. Ši būsena gali nurodyti, kad nebaigta būtina juridinio subjekto konfigūracija. Sąraše galite tiesiogiai pasiekti puslapius **Išsami pateiktų produktų informacija**, **Produktų atributų priežiūra**, **Produktų kategorijų priežiūra**, **Numatytieji užsakymų parametrai** ir **Teksto vertimai** bei baigti būtiną produkto konfigūraciją.

### <a name="manually-creating-a-new-released-product"></a>Naujo pateikto produkto kūrimas rankiniu būdu

Rankiniu būdu sukurti pateiktą produktą galite vienu veiksmu – tai priklauso nuo organizacijos verslo procesų ir taisyklių, nurodančių, ar turi būti naudojama ši funkcija. Naudojant šią funkciją sukuriamas naujas produktas, kuris automatiškai pateikiamas dabartiniam juridiniam subjektui. Norėdami sukurti naują produktą, darbo srityje **Pateiktų produktų priežiūra** arba sąrašo puslapyje **Pateiktas produktas** spustelėkite **Pateikti produktai**.

