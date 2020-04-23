---
title: „Lean“ organizacijos modeliavimas
description: Šiame straipsnyje pateikta informacija apie svarbiausias „lean“ organizacijos modeliavimo koncepcijas.
author: cvocph
manager: tfehr
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33e734aef938c7b58d5c936f6eae32e4f0ab3ba7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211450"
---
# <a name="modeling-a-lean-organization"></a>„Lean“ organizacijos modeliavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie svarbiausias „lean“ organizacijos modeliavimo koncepcijas. 

Paprastai „lean manufacturing“ scenarijui sudaryti naudojamas ne vien tik nesusijusių „kanban“ taisyklių arba medžiagų tiekimo strategijų rinkinys. Konkrečiam gamybos arba tiekimo scenarijui skirtą įvairiuose darbo elementuose ir vietose paskirstomą medžiagų ir produktų srautą galima apibrėžti kaip procesų arba perkėlimų veiklų seką ar mažą tinklą. Ši tinklo seka vadinama gamybos eiga.

## <a name="production-flows-in-lean-manufacturing"></a>Gamybos eigos „lean manufacturing“
Gamybos užsakymuose, kurie sudaryti pagal gamybos užsakymus, medžiaga išduodama konkrečiam gamybos užsakymui. Atliekant operacijų seką, kuri pagrįsta komplektavimo specifikacija (KS) ir maršrutais, produktai sukuriami ir galiausiai gaunami tiekimo vietoje. Gamybos užsakymų našumo laikas gali būti nuo kelių minučių iki kelių savaičių. Gamybos užsakyme sukaupiamos visos susijusios išlaidos, medžiagos ir darbas. 

Siekiant sumažinti pristatymo iš vieno darbo centro į kitą vykdymo laiką ir atsargų perviršį, kurį lemia paketinė gamyba, „lean manufacturing“ gamybos ir sandėlio papildymo procesuose pradedami naudoti „kanban“ papildymo ir prekybos centrų antriniai procesai. Vykdant šiuos antrinius procesus paprastai nutraukiamas iš dalies nepriklausomų „kanban“ ciklų kūrimas. Apdorojant baigto produkto užsakymą daugiau nebesuaktyvinamas neužbaigto produkto „kanban“ papildymo antrinis procesas. 

Kad būtų iš naujo nustatytas įvairių pateikiamų „kanban“ scenarijų gamybos ir išlaidų kontekstas, kaip svarbiausias „lean manufacturing“ procesas pradėtos naudoti pagal veiklas sudarytos gamybos eigos. Visos „kanban“ taisyklės paremtos šia iš anksto nustatyta struktūra. Pagal veiklas sukurtas modelis palaiko kuo įvairiausių scenarijų sąranką. Tačiau, šis modelis nėra sudėtingesnis cecho darbuotojams, todėl, kad visuose scenarijuose naudojama ta pati pagal veiklą sukurta vartotojo sąsaja.

## <a name="semi-finished-products-non-bom-levels"></a>Neužbaigti produktai (ne KS lygiai)
Naudojant „lean manufacturing“ vienoje sistemoje integruojami inventorizuotų bei neužbaigtų produktų „kanban“, todėl vartotojai visuomet juos galės naudoti vienoje vietoje. Dėl šios architektūros savybių papildomų KS lygių nebereikia įvesti, siekiant įgalinti „kanban“, kuriuos ketinama naudoti su pusiau baigtais produktais. Ši architektūra taip pat padeda iki minimumo sumažinti atsargų operacijų.

## <a name="products-and-material-in-work-in-progress"></a>Nebaigtos gamybos produktai ir medžiagos
Jei vykdant bet kurį išrinkimo procesą arba registruojant „kanban“ bus atliekamos suvartotų prekių operacijos, sumažinus paketų dydžius tiek, kad šie idealiai tiktų „lean manufacturing“ vienos prekės srautui, gali gerokai padaugėti atsargų operacijų. Taikant gamybos eigos architektūrą ir kartu naudojant saugomus išėmimų „kanban“ galima perkelti medžiagas į gamybos eigos procesą arba perkelti sandėliavimo vienetų dydžius. Išduotos medžiagos vertė įtraukiama į nebaigtos gamybos sąskaitą, kuri susieta su gamybos eiga Šis elgesys panašus į elgesį su medžiagomis, kurios išduodamos gamybos užsakymui. Tokį patį principą galima taikyti produktams ir neužbaigtiems produktams. Jei vykdant gamybos eigos procesą šie produktai nebus sukuriami, perkeliami arba suvartojami, nebūtina atlikti atsargų operacijų. Produktus užregistravus atsargose, gamybos eigos NG sąskaitos vertė sumažinama atėmus susijusią standartinę savikainą.

## <a name="value-streams-and-value-stream-mapping"></a>Vertės srautai ir vertės srautų susiejimas
„Lean manufacturing“ architektūrą įkvėpė Womack ir Jones suformuluoti penki „lean“ principai: kliento vertė, vertės srautas, srautas, „traukimas“ ir tobulinimas. Rekomenduojamas „lean manufacturing“ sprendimų įgyvendinimo gamybos srityje metodas – verčių srautų susiejimas (VSM). Šį metodą Rother ir Shook aprašė „Lean Manufacturing Institute“ instituto išleistame leidinyje „Learning to See“. 

Būsimą vertės srautą galima modeliuoti kaip gamybos eigos versiją. Visi vertės srauto procesai modeliuojami kaip proceso veiklos. Jei reikia užregistruoti perkėlimo būseną arba integruoti į atsargų išrinkimo ar konsoliduotų siuntimų procesus, perkėlimus galima modeliuoti kaip perkėlimo veiklas. 

Pats vertės srautas modeliuojamas kaip valdymo vienetas. Todėl vertės srautą galima naudoti kaip finansinę dimensiją.

Daugiau informacijos apie valdymo vienetų kūrimą ieškokite srityje [Valdymo vieneto kūrimas](../../fin-and-ops/organization-administration/tasks/create-operating-unit.md).

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>„Lean manufacturing" įkainojimas remiantis gamybos eiga
Periodiškai konsolidavus gamybos eigos išlaidas pataisoma susietos NG sąskaitos vertė bei sudaromos sąlygos nustatyti produktų, kurie tiekiami vykdant gamybos eigos procesą, nuokrypius.

## <a name="continuous-improvement"></a>Nuolatinis tobulinimas
Kad būtų geriau laikomasi nuolatinio tobulinimo principo, gamybos eigos procesai vykdomi naudojant daug laiko sąnaudų nereikalaujančias versijas. Todėl esamą gamybos eigos versiją bei visas susijusias „kanban“ taisykles galima kopijuoti į būsimą gamybos eigos versiją. Be to, būsimą gamybos eigos versiją galima modeliuoti prieš ją patvirtinant ir suaktyvinant gamybai vykdyti. Siekiant perėjimo data ir vėliau užtikrinti nenutrūkstamą medžiagų srautą, senų gamybos eigos versijų „kanban“ automatiškai susiejami su nauja versija.

## <a name="simplicity"></a>Paprastumas
„Lean manufacturing“ vykdyti pasirenkame gamybos eigų ir veiklų metodą, kurį taikant ir naudojant tą pačią pakeičiamą architektūrą galima modeliuoti paprastus ir sudėtingus gamybos scenarijus. Atidžiau išnagrinėjus veiklos koncepciją pastebima, kad šią gamybos sistemą paprasta naudoti cechų ir logistikos srities darbuotojams – tiems vartotojams, kuriems ji iš tiesų reikalinga. Naudojant visiems „lean manufacturing“ variantams bendrą vartotojo sąsają pranešama apie pagal veiklas sukurtas užduotis, o ne atsargų operacijas, o sudėtingi verslo procesai iš vartotojo sąsajos perkeliami į gamybos eigą, kuri yra pagrindinis „lean manufacturing“ procesas.



