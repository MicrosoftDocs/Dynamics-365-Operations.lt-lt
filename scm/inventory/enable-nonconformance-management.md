---
title: Veiksmai neatitikties reikalavimams atveju valdymo
description: "Šiame straipsnyje aprašytas pagrindinis nustatymas, kuris reikalingas norint naudoti neatitikimus. Jei norite naudoti kokybės užsakymus, reikalingi papildomi nustatymai."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 6f25e2930ff265df1f938cdf56e8a0f4993617af
ms.lasthandoff: 03/31/2017


---

# <a name="nonconformance-management"></a>Veiksmai neatitikties reikalavimams atveju valdymo

Šiame straipsnyje aprašytas pagrindinis nustatymas, kuris reikalingas norint naudoti neatitikimus. Jei norite naudoti kokybės užsakymus, reikalingi papildomi nustatymai. 

Norėdami įgalinti neatitikimo valdymą, atlikite toliau nurodytus veiksmus:

1.  Apibrėžkite su neatitiktimis susijusius atsargų ir sandėlio valdymo parametrus:
    -   Nustatykite parinkčiai **Naudoti kokybės valdymą** reikšmę **Taip**.
    -   Lauke **Valandinis tarifas** įveskite valandinį darbo tarifą vietine valiuta. Valandinis tarifas naudojamas apskaičiuojant su neatitikimu susijusias operacijų išlaidas. Valandinis tarifas ir apskaičiuotos išlaidos suteikia nuorodinės informacijos apie neatitiktį. Jie nesąveikauja su kitomis funkcijomis.
    -   Naudoti su **kokybės vadyba** spustelėkite į **ataskaitos nustatymas** puslapis nustatyti dokumento spausdinimo tipas. Galite spausdinti ataskaitą veiksmai neatitikties reikalavimams atveju, veiksmai neatitikties reikalavimams atveju žymę ar pataisymų ataskaita. Galite nurodyti daugiau nei vieną įrašo tipą, norėdami spausdinti skirtingus dokumentų tipus ant ataskaitos, arba spausdinti vidines ir išorines pastabas. Gali būti paranku naudoti puslapį **Dokumento tipas** apibrėžiant unikalų neatitikties dokumento tipą ir unikalų taisymų dokumento tipą. Pavyzdžiui, norite įvesti pastabas apie neatitiktį naudodami unikalų neatitikties dokumento tipą. Tokiu atveju nustatykite unikalų dokumento tipą ataskaitos parinktyse.
    -   Įgalinkite neatitikties ir taisymo nuorodų skaičių sekas.

2.  Įgalinkite vartotojo neatitikčių patvirtinimą. Norėdami kiekvienam vartotojui, kuris turi patvirtinti neatitikimą, priskirti darbuotoją naudokite lauką **Vardas** puslapyje **Vartotojai**. Sistema naudoja darbuotojus, kurie keičia neatitikties būseną, sekdama neatitikties istoriją. Vartotojai negali patvirtinti neatitikties, nebent jiems buvo priskirtas darbuotojo identifikatorius.
3.  Apibrėžkite problemų tipus, kurie bus priskirti neatitikčiai. Naudodami puslapį **Problemų tipai** apibrėžkite kokybės problemų, su kuriomis susiduriama įvairiuose neatitikimo tipuose, klasifikaciją. Galite nustatyti šiuos neatitikties tipus: **Vidinis**, **Kliento**, **Tiekėjo**, **Aptarnavimo užklausos**, **Gamybos** ir **Sudėtinio produkto gamybos**. Naudokite puslapį **Neatitikimų tipai**, kur galite leisti priskirti problemos tipą prie vieno ar daugiau neatitikimo tipų. Pavyzdžiui, problemos tipas, susijęs su defekto kodu, gali būti taikomas visiems neatitikčių tipams, tuo tarpu problemos tipas, susijęs su klientų skundais, gali būti taikomas tik **Kliento** ir **Aptarnavimo užklausos** neatitikčių tipams.
4.  Norėdami pateikti nurodymus apie medžiagų, turinčių defektų, tvarkymą, nurodykite sulaikymo zonas. Naudokite puslapį **Sulaikymo zonos**, kad apibrėžtumėte zonas, kurios gali būti priskirtos prie neatitikties. Išspausdintoje neatitikimo žymėje bus rodoma priskirta sulaikymo zona ir informacija apie naudojimą, nurodanti, kaip tvarkyti medžiagas su defektais. Zonos gali atitikti atsargų vietas arba operacijų išteklius.
5.  Nurodykite diagnostikos tipus, kurie bus priskirti koregavimui. Naudodami puslapį **Diagnozės tipai** nurodykite diagnostikos veiksmų klasifikaciją. Koregavimu nurodoma, kurio diagnostinio veiksmo turi būti imtasi, atsiradus patvirtintai neatitikčiai, ir kas turėtų imtis veiksmų. Juo taip pat nurodoma pageidaujama užbaigimo data ir planuojama užbaigimo data.
6.  Nurodykite susijusias operacijas, kurios bus priskirtos neatitikčiai. Norėdami nurodyti darbų, kurie gali būti atlikti atsiradus patvirtintai neatitikčiai, klasifikaciją, naudokite puslapį **Operacijos**. Priskyrę susijusią operaciją neatitikčiai taip pat galite pateikti išsamią informaciją , pvz., apie susijusią medžiagą, darbo valandas ir papildomas išlaidas, būtinas atliekant operaciją. Ši informacija naudojama skaičiuojant operacijos įvertintą savikainą. Išsami informacija ir įvertinta savikaina naudojamos kaip nuorodos. Susijusios kokybės operacijos skiriasi nuo galimų nurodyti gamybos maršruto operacijų.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kurti ir apdoroti neatitiktis (darbo vadovas)](https://ax.help.dynamics.com/en/wiki/create-and-process-a-nonconformance/)

[Quality management processes](quality-management-processes.md)

[Nustatykite būtinųjų sąlygų neatitikimų valdymo (darbo vadovas)](https://ax.help.dynamics.com/en/wiki/set-up-prequisites-for-nonconformance-management/)


