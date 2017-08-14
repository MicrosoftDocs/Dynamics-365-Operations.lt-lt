---
title: "Neatitikimų valdymas"
description: "Šiame straipsnyje aprašytas pagrindinis nustatymas, kuris reikalingas norint naudoti neatitikimus. Jei norite naudoti kokybės užsakymus, reikalingi papildomi nustatymai."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7a6f7c12ab5fe5e67ffb844c1dbc6cd688ecd4d5
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="nonconformance-management"></a>Neatitikimų valdymas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašytas pagrindinis nustatymas, kuris reikalingas norint naudoti neatitikimus. Jei norite naudoti kokybės užsakymus, reikalingi papildomi nustatymai. 

Norėdami įgalinti neatitikimo valdymą, atlikite toliau nurodytus veiksmus:

1.  Apibrėžkite su neatitiktimis susijusius atsargų ir sandėlio valdymo parametrus:
    -   Nustatykite parinkčiai **Naudoti kokybės valdymą** reikšmę **Taip**.
    -   Lauke **Valandinis tarifas** įveskite valandinį darbo tarifą vietine valiuta. Valandinis tarifas naudojamas apskaičiuojant su neatitikimu susijusias operacijų išlaidas. Valandinis tarifas ir apskaičiuotos išlaidos suteikia nuorodinės informacijos apie neatitiktį. Jie nesąveikauja su kitomis funkcijomis.
    -   Naudokite skirtuką **Kokybės valdymas**> puslapyje **Ataskaitos sąranka** , kad apibrėžtumėte spausdinamo dokumento tipą. Galite atspausdinti neatitikties ataskaitą, neatitikties žymę arba taisymo ataskaitą. Galite nurodyti daugiau nei vieną įrašo tipą, norėdami spausdinti skirtingus dokumentų tipus ant ataskaitos, arba spausdinti vidines ir išorines pastabas. Gali būti paranku naudoti puslapį **Dokumento tipas** apibrėžiant unikalų neatitikties dokumento tipą ir unikalų taisymų dokumento tipą. Pavyzdžiui, norite įvesti pastabas apie neatitiktį naudodami unikalų neatitikties dokumento tipą. Tokiu atveju nustatykite unikalų dokumento tipą ataskaitos parinktyse.
    -   Įgalinkite neatitikties ir taisymo nuorodų skaičių sekas.

2.  Įgalinkite vartotojo neatitikčių patvirtinimą. Norėdami kiekvienam vartotojui, kuris turi patvirtinti neatitikimą, priskirti darbuotoją naudokite lauką **Vardas** puslapyje **Vartotojai**. Sistema naudoja darbuotojus, kurie keičia neatitikties būseną, sekdama neatitikties istoriją. Vartotojai negali patvirtinti neatitikties, nebent jiems buvo priskirtas darbuotojo identifikatorius.
3.  Apibrėžkite problemų tipus, kurie bus priskirti neatitikčiai. Naudodami puslapį **Problemų tipai** apibrėžkite kokybės problemų, su kuriomis susiduriama įvairiuose neatitikimo tipuose, klasifikaciją. Galite nustatyti šiuos neatitikties tipus: **Vidinis**, **Kliento**, **Tiekėjo**, **Aptarnavimo užklausos**, **Gamybos** ir **Sudėtinio produkto gamybos**. Naudokite puslapį **Neatitikimų tipai**, kur galite leisti priskirti problemos tipą prie vieno ar daugiau neatitikimo tipų. Pavyzdžiui, problemos tipas, susijęs su defekto kodu, gali būti taikomas visiems neatitikčių tipams, tuo tarpu problemos tipas, susijęs su klientų skundais, gali būti taikomas tik **Kliento** ir **Aptarnavimo užklausos** neatitikčių tipams.
4.  Norėdami pateikti nurodymus apie medžiagų, turinčių defektų, tvarkymą, nurodykite sulaikymo zonas. Naudokite puslapį **Sulaikymo zonos**, kad apibrėžtumėte zonas, kurios gali būti priskirtos prie neatitikties. Išspausdintoje neatitikimo žymėje bus rodoma priskirta sulaikymo zona ir informacija apie naudojimą, nurodanti, kaip tvarkyti medžiagas su defektais. Zonos gali atitikti atsargų vietas arba operacijų išteklius.
5.  Nurodykite diagnostikos tipus, kurie bus priskirti koregavimui. Naudodami puslapį **Diagnozės tipai** nurodykite diagnostikos veiksmų klasifikaciją. Koregavimu nurodoma, kurio diagnostinio veiksmo turi būti imtasi, atsiradus patvirtintai neatitikčiai, ir kas turėtų imtis veiksmų. Juo taip pat nurodoma pageidaujama užbaigimo data ir planuojama užbaigimo data.
6.  Nurodykite susijusias operacijas, kurios bus priskirtos neatitikčiai. Norėdami nurodyti darbų, kurie gali būti atlikti atsiradus patvirtintai neatitikčiai, klasifikaciją, naudokite puslapį **Operacijos**. Priskyrę susijusią operaciją neatitikčiai taip pat galite pateikti išsamią informaciją , pvz., apie susijusią medžiagą, darbo valandas ir papildomas išlaidas, būtinas atliekant operaciją. Ši informacija naudojama skaičiuojant operacijos įvertintą savikainą. Išsami informacija ir įvertinta savikaina naudojamos kaip nuorodos. Susijusios kokybės operacijos skiriasi nuo galimų nurodyti gamybos maršruto operacijų.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Neatitikčių kūrimas ir apdorojimas (užduočių vedlys)](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-process-non-conformance)

[Kokybės valdymo procesai](quality-management-processes.md)

[Neatitikimo valdymo būtinųjų sąlygų nustatymas(užduočių vedlys)](/dynamics365/unified-operations/supply-chain/inventory/tasks/set-up-prerequisites-nonconformance-management)




