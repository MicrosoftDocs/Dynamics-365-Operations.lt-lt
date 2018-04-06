---
title: "Planuoti krovinių transportavimo maršrutus su keliomis stotelėmis"
description: "Šiame straipsnyje aprašomi įvairūs elementai, naudojami transportavimo maršrutams programoje „Dynamics 365 for Finance and Operations“ planuoti."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 16255e812773ed35c0e34ec26a8a689ea09632bd
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Planuoti krovinių transportavimo maršrutus su keliomis stotelėmis

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomi įvairūs elementai, naudojami transportavimo maršrutams programoje „Microsoft Dynamics 365 for Finance and Operations“ planuoti.

Maršruto planus ir maršruto vadovus galite naudoti sudėtingiems transportavimo maršrutams, kurie turi keletą stotelių, planuoti. Jei tas pats maršrutas bus naudojamas reguliariai, galite nustatyti suplanuotą maršrutą.

## <a name="route-plans"></a>Maršruto planai
Maršruto planą sudaro maršruto segmentai su informacija apie maršruto stoteles, kuriose sustojama, ir kiekvienam segmentui naudojamus vežėjus. Maršruto stoteles turite nustatyti kaip tranzito punktus. Tranzito punktas gali būti tiekėjas, sandėlis, klientas ar tiesiog perkrovimo vieta, kurioje pakeičiamas vežėjas. Įvairius kiekviename segmente taikomus mokesčius galite nustatyti kaip „vietų tarifus“. Štai keletas pavyzdžių:

-   Mokesčiai už kelionę į nurodytus segmentus
-   Mokesčiai už prekių paėmimą
-   Mokesčiai už prekių padėjimą

Kiekvienas maršruto planas turi būti sugretintas su maršruto vadovu.

## <a name="route-guides"></a>Maršruto vadovai
Maršruto vadovas apibrėžia krovinio gretinimo su konkrečiu maršruto planu kriterijus. Pavyzdžiui, galite nurodyti pradinio tranzito punkto ir paskirties vietos tranzito punkto konteinerio tūrį arba svorį ir siuntimo vežėją, tarnybą arba grupę. Maršruto vadovą galite rasti puslapyje **Tarifo ir maršruto darbo sritis**, kuriame krovinius galima sugretinti su maršrutais neautomatiniu arba automatiniu būdu. Jei maršruto vadovas skirtas suplanuotam maršrutui, jį taip pat galima rasti puslapyje **Krovinio kūrimo darbo sritis**.

## <a name="scheduled-routes"></a>Suplanuoti maršrutai
Suplanuotas maršrutas yra iš anksto nustatytas maršruto planas, kuriame nurodytas pristatymo datų grafikas. Suplanuoti ir nesuplanuoti maršrutai skiriasi tuo, kaip jiems priskiriami kroviniai. Jei nesuplanuotą maršrutą priskiriate naudodami tarifo ir maršruto darbo sritį, patvirtinami tik krovinys ir maršruto vadovas. Jei priskiriate suplanuotą maršrutą, taip pat atsižvelgiama į užsakymų ir tranzito punktų datas bei adresus ir maršruto plano datą. Jums nereikia naudoti puslapio Tarifo ir maršruto darbo sritis, norint neautomatiniu būdu krovinius priskirti suplanuotam maršrutui. Galite naudoti puslapį Krovinio kūrimo darbo sritis, norėdami nurodyti, kad pasirinkto suplanuoto maršruto kroviniai būtų sudaromi pagal pardavimo užsakymų klientų adresus ir pristatymo datas. Suplanuotų maršrutų maršruto plane nurodomi fiksuoti pradinis ir paskirties tranzito punktai. Paprastai nurodomi tie patys visų segmentų siuntimo vežėjas ir tarnyba, tačiau jie gali skirtis. Paskirties vietos tranzito punktai sudaromi naudojant klientų, kurie yra aplankomi maršruto metu, pašto kodus. Galima nurodyti kelis vieno maršruto plano maršruto grafikus. Maršruto planas turi būti sugretintas su maršruto vadovu. Tačiau suplanuotų maršrutų planą galima susieti tik su vienu maršruto vadovu. Maršruto grafikas yra naudojamas tik faktiniams maršrutams puslapyje **Maršruto grafikas** kurti. Nurodydami krovinius puslapyje Krovinio kūrimo darbo sritis, galite naudoti numatytąjį krovinių šabloną.

## <a name="load-building-workbench"></a>Krovinio kūrimo darbo sritis
Kroviniams nurodyti puslapyje Krovinio kūrimo darbo sritis naudojami klientų adresai ir pristatymo datos iš pardavimo užsakymų bei galimi suplanuoti maršrutai. Pagal numatytuosius parametrus darbo srityje įvedamos maršrute nurodytos reikšmės. Tačiau galite pasirinkti pradžios datą, kuri yra ankstesnė nei maršrute nurodyta pradžios data. Kai krovinys nurodomas, tikrinami visų atvirų pardavimo užsakymų pristatymo adresai ir pristatymo datos. Jei pristatymo adreso pašto kodas atitinka nurodytą tranzito punkto pašto kodą, o pristatymo data yra patenka į kriterijuose nurodytą diapazoną, kroviniui kurti pasiūlomas pardavimo užsakymas. Taip pat atsižvelgiama į krovinių šablone nurodytą apimtį. Vienu metu siūlomas tik vienas krovinys. Jei yra neįtrauktų pardavimo užsakymų, gali prireikti naudoti kitą krovinio šabloną (pvz., krovinio šabloną, skirtą didesniam sunkvežimiui ar konteineriui) arba suplanuoti papildomą pristatymą.




