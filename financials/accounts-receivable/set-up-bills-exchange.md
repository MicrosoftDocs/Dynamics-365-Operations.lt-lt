---
title: "Įsakomųjų vekselių nustatymas"
description: "Šioje temoje aprašomi veiksmai nustatyti įsakomuosius vekselius."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Įsakomųjų vekselių nustatymas

Šioje temoje aprašomi veiksmai nustatyti įsakomuosius vekselius.

Įsakomieji vekseliai yra raštu ar elektroniniu būdu tvarka iš kliento, nurodantis, kad kitai šaliai, paprastai bankui, nurodyta suma turėtų mokėti įmonė. Kai naudojate įsakomąjį vekselį kaip mokėjimą už pardavimo užsakymo SF arba laisvos formos SF, kredituojate kliento sąskaitą. Kreditas saugomas įsakomojo vekselio kol klientas apmoka įsakomąjį vekselį bankui. Paprastai bus sudenkite SF su įsakomojo vekselio termino. Kai iš banko gausite pranešimą, kad įsakomasis vekselis apmokėtas, galite jį uždaryti. Galite piešti įsakomąjį vekselį per jūsų banką arba iš šių momentų:

-   Atėjus terminui. Šis metodas yra žinomas kaip kompetencija, rinkimo.
-   Iki datos, paprastai dėl nuolaidos data, nurodyta formoje mokėjimo sąlygas, kurie yra nustatyti kliento. Registruojant operaciją, nuolaidos suma užregistruojama išlaidų sąskaitoje. Likusi suma yra įsipareigojimas jums, kol bankas gauna mokėjimą iš kliento. Šis metodas yra žinomas kaip kompetencijos nuolaida.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Įsakomųjų vekselių šablonų registravimo nustatymas
Naudoti su **klientų registravimo šablonų** puslapis nustatyti registravimo šablonų, kuriuos galite naudoti su vekselių, protesto vekselių, perlaidos rinkimo ir perlaidų nuolaida. – Į **suminėje sąskaitoje** pasirinkite suminėje sąskaitoje rašyti įsakomojo vekselio sumos. Ši sąskaita yra debetuojama arba perduodamos, priklausomai nuo įsakomojo vekselio operacija:
-   Įsakomųjų vekselių, ši sąskaita debetuojama kai užregistruojamas įsakomąjį vekselį, ir kredituojama pavedimą nuolaida arba pavedimo rinkimo registruojamas.
-   Užprotestuotiems įsakomiesiems vekseliams ši sąskaita debetuojama kai užregistruojamas užprotestuotas įsakomasis vekselis.
-   Perdavimams inkasacijai ši sąskaita debetuojama kai užregistruojamas perdavimas inkasacijai.
-   Nuolaidos pavedimams ši sąskaita debetuojama kai užregistruojamas nuolaidos pavedimas.

– Į **sudengimo sąskaita** pasirinkite grynųjų pinigų sąskaitą po įsakomojo vekselio sumos. Ši sąskaita debetuojama kai sudengiamas įsakomasis vekselis. – Į **PVM išankstinai apmokėjimai** pasirinkite galutinę ataskaitą skelbti Kada vekseliai yra naudojami išankstinių apmokėjimų PVM. – Į **įsipareigojimų nuolaida sąskaitai** pasirinkite sąskaitą, skirtą registruoti perlaidos nuolaida su nuolaidos suma. Sąskaita kredituojama kai užregistruojamas pavedimas nuolaidai.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Gautinų sumų parametrai įsakomųjų vekselių nustatymas
Dėl į **sudaro gautinų sumų parametrai** p., numatytasis registravimo profilių dėl vekselių, yra įrašytos į **DK ir PVM** tab. Numeracijų yra nustatytos į **skaičių sekas** tab.
Nustatykite įsakomųjų vekselių žurnalų pavadinimus
------------------------------------------

Dėl to **žurnalų pavadinimai** psl., ne mažiau kaip penki naudoti įsakomųjų vekselių žurnalų pavadinimų kūrimas. Pateikiame žurnalo tipus:
-   **Kliento išduoto įsakomojo vekselio** – žurnalo pavadinimo atkreipti įsakomųjų vekselių žurnalų kūrimas.
-   **Kliento užprotestuoto įsakomojo vekselio** – užprotestuoti įsakomųjų vekselių žurnalą žurnalo pavadinimo kūrimas.
-   **Klientų Išrašyto įsakomojo vekselio** – žurnalo pavadinimo perbraižyti įsakomųjų vekselių žurnalų kūrimas.
-   **Kliento banko pavedimo** – pavedimų žurnalas žurnalo pavadinimo kūrimas.
-   **Kliento sudengtų įsakomųjų vekselių** – žurnalo pavadinimo sudengtų įsakomųjų vekselių žurnalų kūrimas.

Žurnalo kvito puslapyje kiekvieną įsakomųjų vekselių žurnalą, įvesti informaciją apie Įsakomasis vekselis, **vekselis** tab. Po to, kai vekselis žurnalo eilutės užregistruojamos, jūs galite peržiūrėti juos į **įsakomųjų vekselių žurnalą tyrimo** puslapis ir **įsakomųjų vekselių statistika** puslapis.
Nustatykite įsakomųjų vekselių mokėjimo metodą
-----------------------------------------------

Dėl į **mokėjimo būdai** puslapyje, įsteigti bent vieną mokėjimo metodą įsakomųjų vekselių. Jei bendradarbiaujate su daugiau nei vienas bankas, nustatyti mokėjimo kortelėmis, atitinkantį pavedimo formatą, kiekvienas bankas reikalauja įsakomuosius vekselius.
Nustatykite įsakomųjų vekselių mokėjimo mokesčius
-----------------------------------------

Mokėjimo mokestis – tai mokestis, susietas su mokėjimų iš klientų surinkimo procesu. Kelių mokėjimo mokesčio nustatymą linijos gali būti susiję kiekvieną mokėjimo mokestis. Nustatymo eilutes galite kontroliuoti, kaip numatytąjį sumos mokėjimo mokesčiai skaičiuojami. Pvz., galite sukurti nustatymo eilutes, taikomas mokėjimo būdams, mokėjimo specifikacijoms, valiutoms ir laikotarpiams. Taip pat galite sukurti nustatymo eilutes procentais arba suma, kuri yra pagrįsta dienų intervalais. Pavyzdžiui, galite nustatyti palūkanų procentas, pagrįstą laikotarpį, suma yra pradelsta. Jei bankas ima skirtingo dydžio mokesčius už skirtingų pavedimų tipai, pvz., **kolekcijos** ar **nuolaida**, įsteigti atskirą mokėjimo mokestis linijos kiekvieno pavedimo tipo.
Banko pavedimų failų pavedimo mokesčių nustatymas
------------------------------------------------

Dėl to **banko sąskaitų** puslapyje, galite nustatyti pavedimo mokesčių, banko mokesčiai už kiekvieno pavedimo failo, kuris sukuriamas. Pavedimo mokesčiai registruojami, kai pavedimas patvirtinamas ir žinomos realizuotų mokesčių sumos. Pavedimo mokesčiai skiriasi nuo mokėjimo mokesčius, kurie yra surinkti iš klientų ir pridėti prie žurnalo eilutes.
Nustatykite įsakomųjų vekselių dokumentų maketus
---------------------------------------------

Dėl to **banko sąskaitų** spustelėkite **nustatyti**, ir nurodykite dokumento maketą, ko reikia, nes kiekvienos banko sąskaitos, kad jums generuoti išspausdintų įsakomųjų vekselių dokumentus.
Nustatykite įsakomųjų vekselių klientus
--------------------------------------

Dėl į **Klientai** puslapių, kiekvienam klientui, kuris sutiko mokėti naudojant įsakomąjį vekselį, jūs galite nustatyti numatytąjį mokėjimo būdą, įsakomųjų vekselių, **neatliktus mokėjimus** tab.




