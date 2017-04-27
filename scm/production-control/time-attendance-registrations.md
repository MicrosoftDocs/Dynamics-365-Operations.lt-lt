---
title: Laiko ir buvimo darbe registracija
description: "Laiko registravimo darbuotojai gali įvesti skirtingų tipų laiko registracijas, pavyzdžiui, atėjimo į darbą, išėjimo iš darbo, netiesioginių veiklų registravimo ir neatvykimo registravimo. Šiame straipsnyje aprašomos registracijos, jų skaičiavimas, tvirtinimas ir darbo eigos naudojimas norint į tabelių tvirtinimo procesą įtraukti struktūrą ir automatinį tvirtinimą."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f82033798dbe603c0f2e2c92f91d28985c12b3b4
ms.lasthandoff: 03/31/2017


---

# <a name="time-and-attendance-registration"></a>Laiko ir buvimo darbe registracija

[!include[banner](../includes/banner.md)]


Laiko registravimo darbuotojai gali įvesti skirtingų tipų laiko registracijas, pavyzdžiui, atėjimo į darbą, išėjimo iš darbo, netiesioginių veiklų registravimo ir neatvykimo registravimo. Šiame straipsnyje aprašomos registracijos, jų skaičiavimas, tvirtinimas ir darbo eigos naudojimas norint į tabelių tvirtinimo procesą įtraukti struktūrą ir automatinį tvirtinimą. 

<a name="registrations"></a>Registracijos
-------------

Įmonių, kurios naudoja laiko ir buvimo darbe registracijas, darbuotojai turi registruoti darbe praleidžiamą laiką ir lankomumą. Kai kurių įmonių darbuotojams registruotis gali reikėti tik atėjus į darbą ir išeinant iš jo. Kitose įmonėse darbuotojai taip pat gali turėti registruoti faktinių veiklų, kurias jie atlieka, laiko sąnaudas ir pertraukas. Numatyti laiko ir lankomumo vartotojai nurodyti toliau.
-   Darbuotojai, kurie turi registruoti laiką ir lankomumą reguliariais intervalais, pavyzdžiui, kasdien, kas savaitę arba kas dvi savaites.
-   Prižiūrėtojai, vadovai ir darbo užmokestį skaičiuojantys buhalteriai, kurie skaičiuoja, tvirtina ir perkelia darbuotojo registracijas toliau apdoroti.

| **Pastaba **                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jei vykdote laiko ir lankomumo registracijas vykdydami gamybą, visos projektų, projekto veiklų, netiesioginių veiklų, neatvykimo kodų ir viršvalandžių bei nukrypimo laiko registracijos bus įrašytos ir naudojamos atlyginimams abiejuose moduliuose apskaičiuoti. |

## <a name="time-registrations-workers"></a> Laiko registracijų darbuotojai
Norėdami registruoti laiką ir neatvykimą, darbuotojus reikia nustatyti kaip laiko registracijos darbuotojus įmonėje, kurioje jie dirba.

Atlikus sąranką darbuotojai gali įvesti skirtingų tipų registracijas.

-   Atėjimo į darbą ir išėjimo iš darbo registracijos, kai atvykstama arba išvykstama iš darbo.
-   Laiko ir prekių suvartojimas gamybos užduotyse.
-   Laikas, kurį sunaudoja cecho mašina, jei ji nurodyta kaip išteklius.

| **Pastaba **                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darbuotojui gali būti automatiškai priskiriamos laiko registracijos, atliktos naudojant konkrečią cecho mašiną, jei darbuotojas nusprendžia dirbti kaip mašinos asistentas, kai jis pradeda gamybos užduotį. |

-   Projektų ir projektų veiklų laiko registracijos.
-   Projekto mokesčių bei prekių suvartojimo registravimas naudojant atitinkamus projekto mokesčių žurnalus ir projekto prekių žurnalus.
-   Suplanuotas neatvykimas.
-   Neatvykimas, kai vėluojama atvykti į darbą arba iš darbo išeinama anksčiau nei planuota.
-   Darbo pertraukos, užregistruotos neautomatiniu būdu arba sistemos automatiškai apskaičiuotos.
-   Netiesioginės veiklos, t. y. negamybinės veiklos, kurias darbuotojas gali vykdyti darbo dienos metu. Šių veiklų pavyzdžiai apima susitikimus arba savo darbo srities valymą.
-   Viršvalandžiai, kurie gali būti registruojami kaip viršvalandžiai, nukrypimo laikas arba viršvalandžiai.

## <a name="adding-clockout-registrations"></a>Išėjimo iš darbo registracijos įtraukimas
Jei darbo dienos pabaigoje darbuotojas pamiršta užregistruoti išėjimą iš darbo, trūkstamą registraciją galima įtraukti paleidžiant paketinę užduotį. Sistema palygins atėjimo į darbą ir išėjimo iš darbo laikus pagal susietą darbuotojo šabloną ir automatiškai įterps trūkstamą išėjimo iš darbo registraciją, kad ji atitiktų šablono pabaigos laiką. Atėjimo į darbą ir išėjimo iš darbo registracijos yra labai svarbios toliau skaičiuojant ir tvirtinant laiko registracijas prieš juos perkeliant į algalapį.

## <a name="calculating-registrations"></a>Registracijų skaičiavimas
Kai registracijos darbuotojui priskiriama skaičiavimo grupė, kuri paprastai yra susijusi su konkrečia komanda, pamaina arba darbo grupe. Komandos vadovas arba prižiūrėtojas paprastai patikrina darbuotojų registracijas ir todėl jis yra atsakingas už kasdienį atitinkamų skaičiavimo grupių skaičiavimo vykdymą. Skaičiavimo proceso metu komandos vadovas arba prižiūrėtojas gali atlikti toliau nurodytus veiksmus.
-   Taisyti klaidingas registracijas. Pvz., keisti gamybos užduočių perjungimo kodus ir koreguoti grįžtamąjį ryšį.
-   Įtraukti trūkstamas registracijas. Pvz., kurti išėjimo iš darbo registracijas ir kurti neatvykimo operacijas.
-   Naikinti neteisingas registracijas.

Kadangi užregistruotas laikas turi atitikti darbuotojo laiko profilį prieš skaičiuojant registracijas, galite perrašyti bet kurio darbuotojo, turinčio savo standartinio darbo laiko profilio išimčių, darbo laiko profilį. Jei darbuotojo profilis yra dieninė pamaina, o darbuotojas sutiko dirbti naktinėje pamainoje neapmokant už viršvalandžius, komandos vadovas arba prižiūrėtojas turi perrašyti numatytąjį darbuotojo profilį, kad darbo laiką apskaičiuotų naudodamas standartinį nakties tarifą, o ne viršvalandžių tarifą. Skaičiavimas taip pat rodys klaidą, jei trūksta neatvykimo registracijos. Ji turi būti įtraukta, kad būtų užbaigtas skaičiavimas.

## <a name="approving-registrations"></a>Registracijų tvirtinimas
Kaip laiko registracijos darbuotojui priskiriate skaičiavimo grupę, taip turite priskirti ir patvirtinimo grupę. Paprastai grupė bus būdinga konkrečiai komandai, pamainai arba darbo grupei. Turite patvirtinti laiko registracijas, kurios buvo apskaičiuotos teisingai (tai reiškia, kad skaičiavimas turi būti atliktas be klaidų), kad mokėjimo elementus būtų galima generuoti ir vėliau perkelti į algalapio sistemą. Algalapio administratorius paprastai tvirtins registracijas, o prieš patvirtindamas jis gali atlikti toliau nurodytus veiksmus.
-   Perrašyti atskirų darbuotojų mokėjimo sutartis.
-   Įtraukti neautomatiškai nustatomas premijas.
-   Įvesti papildomą informaciją apie neatvykimo registracijas.

| **Pastaba **                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jei tam tikriems darbuotojams buvo skaičiuojami viršvalandžiai, viršvalandžiai gali būti paskirstyti specialiems darbams dienos metu. Tai tinka, jei darbo išlaidos skaičiuojamos pagal darbuotojo mokėjimą. |

## <a name="approving-registrations-using-workflow"></a> Registracijų tvirtinimas naudojant darbo eigą
Galite nustatyti darbo eigos tvirtinimo procesą, kurio metu automatiškai patvirtinamos registracijos, atitinkančios darbo eigos taisykles, paliekant tik nuokrypius, kurie turi būti tvarkomi neautomatiškai. Jei darbo eigos tvirtinimo funkcija yra suaktyvinta, komandos vadovas arba prižiūrėtojas pateikia apskaičiuotas registracijas patvirtinti. Darbo eigos procesas sukurs atitinkamus patvirtinimus bei užduotis ir tada juos priskirs tinkamiems vartotojams bei vaidmenims, kaip nurodyta darbo eigoje. Galima naudoti du laiko ir lankomumo darbo eigos patvirtinimus.

| Darbo eiga                                  | Paskirtis                                                                                                   | Registracijos tipas                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bendras laiko ir buvimo darbe dienų skaičius            | Darbo eiga tikrina registracijas pagal, pvz., numatomą dienos darbo valandų skaičių. |                                                                                                                                                                                                                                                       |
| Laiko ir buvimo darbe žurnalo registracija. | Darbo eiga tikrina kiekvieno registracijos tipo registracijos datą.                           | Laikas ir buvimas darbe • Atėjimas į darbą • Išėjimas iš darbo • Neatvykimas • Pertrauka • Perjungimo kodas • Projektas • Projekto veikla • Netiesioginės veiklos gamybos užduotys • Eilė prieš • Sąranka • Procesas • Persidengimas • Transportas • Eilė po • Pradėti asistuoti • Sustabdyti asistavimą |

 

## <a name="transferring-approved-registrations"></a>Patvirtintų registracijų perkėlimas
Patvirtinus registracijas jas galima perkelti į periodinę atlyginimo užduotį. Perkeltos registracijos užregistruojamos į veiklą arba užduotį, su kuria jos yra susijusios, pvz., į gamybos užsakymą arba projektą. Algalapio operacijos kiekvienam darbuotojui generuojamos pagal registracijas.  

## <a name="reversing-transferred-registrations"></a>Perkeltų registracijų atšaukimas
Operacijų atšaukimo užduotį galima vykdyti (pakartoti), kol neįvykdytas periodinio atlyginimo mokėjimo pervedimas. Tai reiškia, algalapio duomenys buvo perkelti į išorinį failą. Kai atšaukiama, visos registracijos panaikinamos, o registruotos gamybos užsakymų arba projektų operacijos yra korespondentinės neutralios.

| **Pastaba **                                                 |
|----------------------------------------------------------|
| Išorinį failą galima importuoti į algalapio sistemą. |

## <a name="registrations-in-electronic-timecards"></a>Registracijos elektroninėse laiko kortelėse
Darbuotojams, kurių atliekamų užduočių greitas grįžtamasis ryšys nėra būtinas (pvz., gamybos užduočių), bet kurie vykdo projekto veiklas, gali būti naudinga naudoti elektroninę laiko kortelę. Elektroninės laiko kortelių suteikia galimybę lanksčiau įvesti registracijas bet kuriuo metu ir atsižvelgiant į jūsų verslo grafiką – kasdien, kas savaitę arba kai darbuotojas yra vėl darbe po to, kai buvo neatvykęs. Norėdami naudoti elektronines laiko korteles arba šiuos darbuotojus, darbuotojo informacijoje turite nurodyti Naudoti laiko kortelę. Naudodamas elektronines laiko korteles darbuotojas gali registruoti toliau nurodytus elementus.

-   Data
-   Registracijos tipas
-   Užduoties nuoroda, pvz., projektas, netiesioginė veikla arba gamybos užsakymas
-   Užduoties identifikavimas
-   Laiko suvartojimas
-   Projekto mokesčiai
-   Projekto prekės





