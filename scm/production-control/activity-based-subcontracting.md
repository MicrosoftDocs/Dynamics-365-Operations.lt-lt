---
title: Veikla pagal subrangos
description: "Šioje temoje aprašoma, išsamiai, kaip naudotis subrangos sutartis vykdoma veikla, gamybos srautas tausojančios gamybos."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Veikla pagal subrangos

Šioje temoje aprašoma, išsamiai, kaip naudotis subrangos sutartis vykdoma veikla, gamybos srautas tausojančios gamybos.

Microsoft Dynamics 365 operacijoms, yra du požiūriai dėl subrangos: gamybos užsakymų ir tausojančios gamybos. Tausojančios gamybos metode, subrangos darbų yra modeliuojama kaip paslauga, susijusi su gamybos srauto veikla. Specialios rūšies išlaidų grupės tipas, kuris pavadintas **tiesioginės užsakomosios paslaugos** buvo įvesta, ir subrangos paslaugas nebėra dalis komplektavimo specifikacijos (KS). Kaštų apskaitos subrangovo darbas yra visiškai integruotos į įkainojimo tausojančios gamybos sprendimas.

## <a name="production-flows-that-involve-subcontractors"></a>Gamybos srautai, susiję su subrangovais
Principo, pagal gamybos srauto nesikeičia, kai veikla yra subrangovai. Medžiagos vis dar teka tarp vietų, proceso veiklas konvertuoti medžiagos su produktais ir perdavimo veikla perkelti medžiagos arba gaminių iš vienos vietos į kitą. Galite modeliuoti vietas ir dirbti ląstelių kaip tiekėjo valdomos priskirdami tiekėjo sąskaitą, į sandėlį arba į išteklių išteklių grupės.  

Remiantis šių pajėgumų, tausojančios gamybos nereikalauja jokių specifinių funkcijų siekiant remti keitimąsi medžiagos ir produktai. Visus galimus scenarijus, kuriuose dalyvauja pardavėjai, kaip gamybos ar transporto paslaugų teikėjai gali būti modeliuojama pagal gamybos ir veiklos struktūrą.  

Pvz., rangovo darbų iš prekybos centrų, kurie yra subrangovo. Kai vėdinimo įrenginys yra ištuštinami subrangovas, kanban kortelės grąžinami surinkimo ląstelių bei kitas važtar. Prekybos centre kartą subrangovas yra tada papildyti. Pervežimus į ir iš subrangovo gali būti modeliuojama kaip aiškų perdavimo veiklai, kuria remiamas skinti ir ruošti siuntą. Jei aiškiai registracijos nėra būtina palaikyti fizinę transporto, perdavimo veikla gali būti praleidžiami.  

Rangovo galima pakrauti balanse bendrą gamybiniu pajėgumus. Pvz., gamybos srautas yra modeliuojama naudojant reguliaraus kanban taisykles. Planner naudoja kanban planavimo Taryba planuoti ir apkrovos lygį tiek darbo ląstelių pagal poreikį. Planner taip pat stebi konsoliduotą tiekimo grafiką prekybos centruose ant to **tiekimo planas** puslapis. Kelis subrangovai gali būti modeliuojama į vieną ar kelis gamybos srautai, o gali būti kelios kanban taisyklės, kad būtų galima tiekti tam pačiam produktui, į tą pačią vietą per įvairią veiklą. Planner konvertuoti kanbans į alternatyvių kanban taisyklę norėdami perplanuoti kanban, kuris buvo sukurtas vidaus gamybos alternatyvių procesų. Iš tiesų, rangovų darbas ląstelė pobūdis neturi poveikio gamybos srautas. Tas pats darbo principas galioja du lygiagrečiai vidaus darbo langelius arba du rangovų ląstelių.   

Kaip ir bet kuri kita veikla gamybos srautas, subrangos sutartis vykdoma veikla gali suvartoti ir padavimo inventorizuotos, neinventorizuotos (darbo procese \[ng\]), ir medžiagos, ir produktai. Visais atvejais planuojant ir vykdant subrangos sutartis vykdoma veikla procesai yra tas pats. Be to, jie tvarko tuos pačius kaip vidaus darbo procesus.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Pirkimo procesas už užsakytos veiklos (paslaugos)
Pirkimo procesą, subrangos sutartis vykdoma veikla yra pagrįstas fizinės medžiagų kiekio kitimą, užregistruoto kanban darbo eigos, pvz., pradėti arba užbaigti. Finansinius srautus, pavyzdžiui, išlaidų subrangovo darbas, yra antrinės srauto, kad taip fizinių srautų. Be to, pirkimo procesą yra nepriklausomi procesas, kuris leidžia rankiniu būdu koreguoti pirkimo dokumentų kiekviename žingsnyje. Čia yra pirkimo procesas subrangos sutartis vykdoma veikla:

1.  Kurti pirkimo sutartį. Pirkimo sutartį yra sukurta paslauga ir prijungtas prie gamybos srautas, veikla.
2.  Kurti pirkimo užsakymą. Išleidimo pirkimo užsakymą galite sukurti tarnybą, pagrįstą reguliaraus kanban darbo vietų. Darbo vietų, už tą pačią paslaugą galima suskirstyti į pirkimo užsakymo eilutės pagal dieną, savaitę arba mėnesį. Pirkimo užsakymo eilutes gali būti sukurtos bet kuriuo metu po to, kai kanban darbo vietų. Pirkimo užsakymo eilutes galima sukurti net po fakto. Ši parinktis paprastai būna pažymėtas, jei rangovo teikia paslaugas be papildomo pranešimo, pagal kanbans arba kanban kortelės, kad subrangovas gauna. Tokiu atveju gali būti sumažintas nukrypimus nuo pirkimo užsakymo SF.
3.  Generuoti kanban kortelės, medžiagos ir išrinkimo perduoti subrangovui paruošti perdirbti. Remiantis Išsamios modeliavimo gamybos srautas, rengiant daroma kanban valdybos organizuojant procesus naudojant išrinkimo ir paruošimo funkcijos. Kita vertus, rengiant daroma kanban valdyba perkėlimo užduotis naudojant išrinkimo ir pradžios arba pabaigos. Inventorizuotos medžiaga, abu procesai gali būti remiamos WMS skinti ir ruošti siuntą. Važtaraštį galima sukurti pagal poreikį.
4.  Generuoti kanban vėdinimo įrenginiai ir kanban kortelės. Po apdorojimo, kortelės yra grįžo iš subrangovo. Paprastai, kortelės yra, nurodantis medžiagos fizinės atgabentas važtaraštyje. Nuoroda į teikiamas paslaugas, nėra būtina. Medžiagą ar gaminį klientui yra registruota kanban valdyba, atsižvelgiant į tai, kanban kortelės. (Kanban valdybos veiklos procesas arba perdavimo užduočių kanban valdyba yra naudojamas, modeliuojamos veiklą.).
5.  Sukurkite kvitą konsultavimo. Konsultavimo gavimas gali būti panaudotas pakeisti pakavimo važtaraščio dokumento už gautas paslaugas. Gavimo patarimus galetu pagal subrangos veikla baigė kanban vietų pasirinkto laikotarpio. Kiekvienos užduoties gavimo, patarimai yra sukurti susietą pirkimo užsakymo eilutės. Gavusi patariamojo galima atspausdinti ir išsiųsti subrangovas gavimo patvirtinimas.
6.  Sukurti sąskaitą-faktūrą.

Procesas baigiasi, kai subrangovas išrašoma laikotarpiui. SF rungtynes yra padaryta prieš gavimo patarimus, kurie sukuriami. Nes gavimo patarimus nurodo tikslią faktinio gavimo medžiagos, trijų padėčių atitikimo supaprastintas.

## <a name="configuring-activities-for-subcontracting"></a>Konfigūruojant veiklos pasiūlymus subrangos darbams pagal
Šiuose skyriuose aprašoma, kaip konfigūruoti veiklos subrangos sutarčių sudarymą.

### <a name="subcontracted-services"></a>Užsakytos paslaugos

Mokėjimo elementą, kuris yra naudojamas pagal subrangos turi būti produktas, kuris turi šias ypatybes:

-   **Prekė:** paslaugos
-   **Atsargų modelio grupės:** ne įžuvinti

Šis reikalavimas mokymuisi naudoti pirmasis į, pirmasis iš (FIFO) atsargų modelis. **Pastaba:** produktų savikainos skaičiavimo reikalauja, kad būtų apibrėžta standartinė paslaugos kaina. Pirkimo sutartį su tiekėju yra būtinas. Priešingu atveju, paslaugos negalima naudoti veiklos pagrindu subrangos sutarčių sudarymą.

### <a name="subcontracted-process-activities"></a>Rangovų proceso veiklas

Norėdami sukonfigūruoti proceso veiklos subrangos sutartis vykdoma veikla, atlikite toliau nurodytus veiksmus.

1.  Konfigūruoti rangovų darbas ląstelė. Norėdami sukonfigūruoti darbas ląstelė kaip subrangovui, turite sukurti ištekliaus ir **tiekėjo** tipo ir susieti ją su darbo elemento (išteklių grupės). Vykdymo proceso išlaidų kategorija, su **tiesioginės užsakomosios paslaugos** išlaidų grupės tipas turėtų būti priskirta darbas ląstelė. Išlaidų kategorijų nustatymas ir kiekio nebūtini.
2.  Po proceso veiklos yra sukurtas ir susijusius su subrangovo darbas langelį, turite sukonfigūruoti tarnybos veiklos prieš gamybos srauto versija gali būti aktyvuota. Galite užbaigti šį veiksmą, **veiklos****detalės** puslapis. Veiklai, kurios yra susijusios su rangovų darbas ląstelė, į **paslaugų sąlygas** FastTab yra rodomas. Šis FastTab, įtraukti numatytąjį paslauga, kuri galioja visos produkcijos prekės. Jei konkretaus išvesties prekės reikalauja skirtingų paslaugų ar skirtingų paslaugų skaičiavimo parametrus (pvz., skirtingų paslaugų santykis), galite įtraukti kitų paslaugų veikla.

## <a name="subcontracted-transfer-activities"></a>Rangovų perdavimo veikla
Perdavimo veikla yra sukonfigūruotas kaip subrangos sutartis vykdoma veikla, priklausomai nuo to, kad **transportuoja** veiklos perdavimo nustatymas. Galimos toliau nurodytos pasirinktys:

-   **Siuntėjas** – veiklos samdo subrangovus jei perkėlimas iš sandėlio valdo tiekėjui (kaip apibrėžta pagal sandėlio ypatybę). Visų pasirinktų pirkimo sutartys už paslaugas turi būti paties tiekėjo ID kaip sandėlį.
-   **Gavėjas** – veiklos samdo subrangovus jei perdavimas į sandėlį valdo tiekėjui (kaip apibrėžta pagal sandėlio ypatybę). Visų pasirinktų pirkimo sutartys už paslaugas turi būti paties tiekėjo ID kaip sandėlį.
-   **Vežėjas** – veiklos samdo subrangovus bet tiekėjui, kuris teikia paslaugas. Padarymo vežėjas reikia sukurti sandėlio valdymas ir turi būti priskirtas tiekėjo sąskaitą.

Kalbant apie proceso veiklą, turite sukonfigūruoti numatyt±jç rangovų perdavimo veiklai, **paslaugų sąlygos** FastTab, į **veiklos****detalių** puslapis.

## <a name="service-quantity-calculation"></a>Paslaugų kiekio skaičiavimas
Visą pirkimo procesą remiantis prekės nuoroda paslaugą. Šios prekės nuoroda yra matuojamas matavimo vieneto kodą paslaugos. Paslaugų paprastai matuojamos paslaugos (vienetų) skaičius arba laiko. Skaičiuojant paslaugų kiekį, remiantis registruotų baigti kanban darbo vietas, galite naudoti šiuos metodus:

-   **Apskaičiavimą, kuris remiasi darbo vietų skaičius** – vieną kanban darbą yra lygus *n* paslaugas, nepriklausomai nuo to produkto kiekio, pateikto vienetų. Tausojančios gamybos, vienas darbas atitinka vieną krovinio vienetą. Šis skaičiavimo metodas taikomas visoms paslaugoms, kurios turi fiksuotą kainą už vėdinimo įrenginį. Todėl šis metodas dažniausiai taikomas perkėlimo veikla. Vis dėlto gali taip pat būti taikomas proceso veiklas, apdoroti visą vėdinimo įrenginiai.
-   **Apskaičiavimą, kuris remiasi produkto kiekis** – paslaugų kiekis yra susijęs su produkto kiekio, kuris planuojama pateikti. Kai skaičiuojamas tiekiamų produktų kiekis, klaidų kiekis gali būti arba įtrauktinų arba išskirtinų. Šis skaičiavimo metodas taikomas visais atvejais, kai paslaugų kaina vienam perdirbto produkto vienetui yra susitarta.
-   **Apskaičiavimą, kuris remiasi veiklos laikas** – teorinės veiklos laikai yra apskaičiuotos, remiantis perdirbimo metu veiklos, bendras perdirbtų kiekį ir našumo santykis perdirbtam produktui. Šis skaičiavimo metodas taikomas paslaugoms, apmokėtas valandą ir turėti atliekančioms laiku už perdirbtą produktą.

## <a name="cost-accounting-of-subcontracted-services"></a>Kaštų apskaitos užsakytos paslaugos
Užregistravus patariamasis gavimo ar tiekėjas pagal važtaraštį pirkimo užsakyme, kuris buvo sukurtas gamybos srauto (kitaip tariant, pirkimo užsakymas, sukurtas pagal kanban darbas skirtas subrangos sutartis vykdoma veikla), gavimo dienos vertė sudarė gamybiniu nebaigtos gamybos sąskaitose. Nuokrypių sąskaitos faktūros taip pat sudarė į gamybos srauto. Pradėta taikyti išlaidų kategorijos už subrangovų darbą. Ši išlaidų kategorija įgalinti skaidri sekti rangovų darbą, kuris yra priskirtas vykdomo projekto ir laikotarpio suvartoto vertę.  

Įkainojimą tausojančios gamybos sąnaudų laikotarpio pabaigoje padėčių apskaičiuoja tikrasis dispersijos iš produktų, kurie gaminami iš gamybos srautas laikotarpiu įkainojimo.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modeliavimo perdavimą, subrangos sutartis vykdoma veikla
Žmonės dažnai mano transporto neproduktyvių ir manau, kad jis nesukuria pridėtinės vertės. Tačiau lyginant su vidaus gamybos išlaidos, subrangos išlaidos laikytina papildoma transporto veiklos išlaidas. Gamybos srautas, kuri apima kelias vietas ir transporto paslaugų turėtų modelio transporto išlaidas kaip sąnaudas tiekiant produktus klientui. 

Veikla pagal subrangos tausojančios gamybos leidžia integruoti vežėjams ir transporto pardavėjai, medžiagų ar produktų perjunginėti vietas ir gamybos srautą. Pagal modeliavimo perkelti veiklos, galite priskirti vežėjas arba tiekėjo. Perdavimo veiklos/darbo pagrindas paslaugas bei pirkimo sutartis, ir jūs galite sukurti pirkimo ir gavimo patarimus, atsižvelgiant į faktines perdavimo užduočių. Ši funkcija yra tas pats kaip subrangovo proceso veiklos funkcijas.  

Todėl Dynamics 365 dabar palaiko KS skaičiavimas, kuris apima transporto paslaugas, sukurti susijusių pirkimo užsakymų, integruotas gavimo registracijos ir integruoti transporto operacijoms paslaugų išlaidas į gamybos srauto kainuoja.


