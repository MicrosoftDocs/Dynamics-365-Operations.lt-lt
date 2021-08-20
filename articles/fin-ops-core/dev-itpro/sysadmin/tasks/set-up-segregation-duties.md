---
title: Nustatyti pareigų atskyrimą
description: Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c06ce9325d7b0894ba53d6b9782f495a48280d45e538b048d883ab86f05dabf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755753"
---
# <a name="set-up-segregation-of-duties"></a>Nustatyti pareigų atskyrimą

[!include [banner](../../includes/banner.md)]

Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai. Ši koncepcija vadinama pareigų atskyrimu. Pavyzdžiui, galbūt nenorite, kad tas pats asmuo patvirtintų prekių gavimą ir apmokėtų tiekėjui. Pareigų atskyrimas padeda sumažinti apgaulės riziką ir nustatyti klaidas arba pažeidimus. Taip pat galite naudoti pareigų atskyrimą norėdami taikyti vidinės kontrolės strategijas. Norėdami sukurti taisyklę, atlikite tolesnę procedūrą. Turite būti sistemos administratorius, kad galėtumėte atlikti procedūrą.

1. Eikite į **Sistemos administravimas** > **Sauga** > **Pareigų atskyrimas** > **Pareigų atskyrimo taisyklės**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite taisyklės reikšmę.
4. Lauke **Pirmoji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą. Pasirinkite pirmą taisyklės kontroliuojamą pareigą.
6. Lauke **Antroji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. 
7. Sąraše raskite ir pasirinkite norimą įrašą. Pasirinkite antrą taisyklės kontroliuojamą pareigą.
10. Lauke **Svarba** pasirinkite parinktį. Pasirinkite rizikos, patiriamos, kai tas pats vartotojas arba vaidmuo atlieka abi pareigas, svarbą.  
11. Lauke **Saugos rizika** įveskite reikšmę. Įveskite saugos rizikos aprašą.  
12. Lauke **Saugos sumažinimas** įveskite reikšmę. Įveskite veiksmų, kuriuos atliekate siekdami sumažinti saugos riziką, aprašą. Pavyzdžiui, riziką galite sumažinti atlikdami išsamesnes proceso apžvalgas, kas mėnesį atlikdami vadybinę peržiūrą arba dalindamiesi ištekliais su kitais padaliniais.     
13. Spustelėkite **Įrašyti**.

> [!IMPORTANT] 
> Sukuriant taisyklę, pareigų atskyrimo taisyklių laikymasis nėra patvirtintas. Galite sukurti taisyklę, kuri sukurs esamų vaidmenų nesuderinamumą. Esami vartotojo vaidmens priskyrimai gali būti nesuderinami su nauja taisykle. Sukūrę arba modifikuodami taisyklę, turite patikrinti atitikimą. Daugiau informacijos žr. [Pareigų atskyrimo konfliktų nustatymas ir sprendimas](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]