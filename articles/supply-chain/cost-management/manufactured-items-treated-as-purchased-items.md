---
title: "Produktų, kuriuos galima gaminti arba įsigyti, nustatymas"
description: "Produktai gali būti gaunami įvairiais būdais: jų galima pagaminti arba įsigyti (nusipirkti). Šiame straipsnyje aprašomi keli dažni punktai, kuriuos reikėtų apsvarstyti konfigūruojant kelių produktų šaltinių naudojimą."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5ed8c93c13746249605ad8742549c23bb1e0e10
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>Produktų, kuriuos galima gaminti arba įsigyti, nustatymas

[!include [banner](../includes/banner.md)]

Produktai gali būti gaunami įvairiais būdais: jų galima pagaminti arba įsigyti (nusipirkti). Šiame straipsnyje aprašomi keli dažni punktai, kuriuos reikėtų apsvarstyti konfigūruojant kelių produktų šaltinių naudojimą. 

Keli šaltiniai paprastai naudojami nupirktai prekei, kuri kartais gaminama, arba kai prekė, kuri pirmiausia buvo gaminama prekė, pakeičiama į pirmiausia perkamą prekę. Prekė pradžioje bus priskirta kaip pagaminta prekė, kad būtų galima apibūdinti komplektavimo specifikaciją (KS) ir maršruto informaciją, ir palaikyti prekės gamybos užsakymus. Gamybos tipas turi būti nustatytas į **KS** (arba gamybos procese – į **Formulė** arba **Sudėtinis produktas**).

Naudodami standartines išlaidas, galite apskaičiuoti pagamintos prekės išlaidų įrašą. Tačiau prekės išlaidų įrašas negali sutapti su standartine kaina, kurios jums reikia pirkimo tikslais. Šiuo atveju standartinė kaina turi būti įvesta neautomatiškai ir suaktyvinta prekės kainos įrašui. Skaičiuodami išlaidas, galite naudoti specialią KS ir maršrutą, kurie nurodo produktų rinkinio pasiūlą per ataskaitinį laikotarpį, siekiant per tam tikrą laiką sumažinti nuokrypius. Be to, vienoje teritorijoje pagaminta prekė gali būti perkelta į kitą teritoriją. Todėl prekės savikaina turi būti įvesta neautomatiškai ir suaktyvinta teritorijai, į kurią prekė perkeliama. Kai naudojate pagamintą prekę kaip aukšto lygio produktų komponentą, komponento išlaidos turi būti laikomos nupirkta preke. Šios gairės taikomos nepriklausomai nuo to, ar komponento išlaidos buvo apskaičiuotos, ar įvestos neautomatiškai. Kitaip tariant, KS apskaičiavimas turi prekės išlaidas laikyti nupirktu komponentu, o ne naudoti prekės KS ir maršruto informaciją išlaidoms apskaičiuoti. 

Norėdami neleisti skaičiuoti, pasirinkite išskleidimo vėliavėlę **Stabdyti išskleidimą**, kuri yra KS skaičiavimo grupėje, priskirtoje prekei. Norėdami bendrojo planavimo skaičiavimams neleisti išskleisti poreikių naudojant prekę, prekės padengimo arba padengimo grupėje nustatykite išskleidimo ribą į 0 (nulį). Tada bendrojo planavimo skaičiavimas prekę laikys nupirkta preke ir daugiau neatliks prekės KS ir maršruto informacijos skaičiavimų.






