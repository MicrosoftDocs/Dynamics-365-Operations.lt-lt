---
title: "Mokėtinų ir Gautinų sumų užsienio valiutos kurso pasikeitimas"
description: "Dėl valiutos kursų svyravimų laikui bėgant kinta atvirų operacijų užsienio valiutomis teorinė vertė (balansinė vertė). Šiame straipsnyje pateikiama informacija apie užsienio valiutos kurso pasikeitimo procesą, kuris vykdomas norint atnaujinti atvirų operacijų Mokėtinų ir Gautinų sumų vertę."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 69a57cc5a2d652efc2ee14906c64b0dc741da31c
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Mokėtinų ir Gautinų sumų užsienio valiutos kurso pasikeitimas

Dėl valiutos kursų svyravimų laikui bėgant kinta atvirų operacijų užsienio valiutomis teorinė vertė (balansinė vertė). Šiame straipsnyje pateikiama informacija apie užsienio valiutos kurso pasikeitimo procesą, kuris vykdomas norint atnaujinti atvirų operacijų Mokėtinų ir Gautinų sumų vertę. 

Atvirų tiekėjo operacijų užsienio valiutomis teorinė, arba balansinė, vertė laikui bėgant kinta dėl valiutos kursų svyravimų. Norėdami atnaujinti atvirų operacijų Mokėtinų ir Gautinų sumų vertę, vykdykite užsienio valiutos kurso pasikeitimo procesą. Užsienio valiutos kurso pasikeitimą galima vykdyti ir Mokėtinoms, ir Gautinoms sumoms. Šio proceso metu naudojamas naujas valiutos kursas atviroms arba nesudengtoms sumoms perkainoti nurodyta data. Skirtumai tarp pradinių užregistruotų sumų ir perkainotų sumų sukels nerealizuotas pelnas arba nuostolis kiekvienos atviros operacijos. Mokėtinų ir gautinų sumų sąskaitos subledgers tada atnaujintas, kad atspindėtų nerealizuotas pelnas arba nuostolis, o apskaitos įrašas registruojamas į DK.

## <a name="simulate-a-foreign-currency-revaluation"></a>Užsienio valiutos kurso keitimo modeliavimas
Prieš perkainodami atvirų operacijų užsienio valiutos sumas, galite vykdyti užsienio valiutos kurso pasikeitimo ta pačia data ir metodu modeliavimo ataskaitą. Norėdami vykdyti modeliavimo ataskaitą puslapyje **Užsienio valiutos kurso pasikeitimas** spustelėkite mygtuką **Modeliavimas**. Ataskaitoje pateikiama negauto pelno arba nepatirto nuostolio sumos peržiūra, atsižvelgiant į nustatytus modeliavimo parametrus.

## <a name="process-a-foreign-currency-revaluation"></a>Užsienio valiutos kurso pasikeitimo apdorojimas
Naudoti į **valiutos kurso** puslapio pagal **periodines užduotis** perkainoti atviros operacijos. Galite paleisti procesą realiuoju laiku arba suplanuoti, kad jis būtų paleistas naudojant paketą. Kai nustatote perkainojimo proceso parametrus, būtinai patikrinkite, ar norite spausdinti ataskaitą apie rezultatus. Perkainojimo ataskaita negali būti perspausdintas, po to, kai procesas bus baigtas. Jei sugeneruosite užsienio valiutos kurso pasikeitimo ataskaitą, joje bus rodomi įvairių kliento / tiekėjo lygio ir valiutos lygio balansai:

-   Klientų arba tiekėjų, turinčių operacijų užsienio valiuta, kurios kursas buvo pasikeitęs, balansai. Rodomi šie balansai:
    -   Bendrasis pradinis balansas užsienio valiuta.
    -   Bendroji užsienio valiutos suma, nurodyta apskaitos valiuta pagal ankstesnį perkainojimą.
    -   Bendroji užsienio valiutos suma, nurodyta apskaitos valiuta pagal dabartinį perkainojimą.
    -   Skirtumas tarp ankstesnio ir dabartinio perkainojimo. Šis skirtumas yra papildomas negautas pelnas arba nepatirtas nuostolis.
-   Bendras negautas pelnas arba nepatirtas nuostolis kiekviena valiuta.

Sukuriamas įrašas kiekvieną kartą, kai vykdote užsienio valiutos kurso pasikeitimą. Iš įrašo puslapyje **Užsienio valiutos vertinimas** pasirinkę **Operacijos** peržiūrėkite išsamų dėl perkainojimo sukurtų operacijų sąrašą. Kiekvieno kvito operacijos yra atviros operacijos, kuri buvo įvertintas iš naujo. Jei atvira operacija buvo įvertintas iš naujo daugiau nei vieną kartą, pamatysite du įrašus, kurie naudoja pačiame kvite. Vienas įrašas bus atjungimo ir ankstesnių nerealizuotas pelnas arba nuostolis, o kitas įrašas bus naujas nerealizuotas pelnas arba nuostolis. Norėdami vykdyti perkainojimo procesą, spustelėkite mygtuką **Užsienio valiutos kurso pasikeitimas**. Nustatykite atitinkamus parametrus šiems parametrams:

-   **Metodas** – pasirinktoje užsienio valiutos kurso pasikeitimo užduotyje naudojamas metodas:
    -   **Standartas** – užsienio valiutos kurso pasikeitimo užduotys registruojamos nepaisant to, ar rezultatas yra pelnas, ar nuostolis.
    -   **Minimumas** – užsienio valiutos kurso pasikeitimo užduotys registruojamos tik, jei rezultatas yra nuostolis.
    -   **Sąskaitos faktūros data** – užsienio valiutos kurso pasikeitimo užduotyse naudojamas pradinis operacijų, kurios perkainojamos pagal pradinę apskaitos valiutos vertę, valiutos kursas. Atšauktas bet koks užsienio valiutos kurso pasikeitimo koregavimo poveikis.
-   **Registravimo data** – visų randamų operacijų, kurių sumos tą datą yra atviros (nesudengtos), data. Registravimo dieną užsienio valiutos sumos yra perkainojamos naudojant puslapyje **Valiutų kursai** įvestus valiutos kursus. Kai registravimo dieną užsienio valiutos sumos yra perkainojamos, ši data tampa paskutine užsienio valiutos kurso pasikeitimo data operacijose, kurios yra koreguotos. Nusprendus vykdyti ankstesnės datos nei vėliausia jau koreguotų operacijų užsienio valiutos kurso pasikeitimo data užsienio valiutos kurso pasikeitimą, periodine užduotimi nekoreguojamos operacijos, kurios ankstesnę registravimo datą yra atviros, bet turi dar ankstesnę paskutinio užsienio valiutos kurso pasikeitimo datą.
-   **Kurso data** – data, kuri nustato užsienio valiutos kurso pasikeitimo operacijoje naudojamą valiutos kursą.
-   **Naudoti registravimo šabloną iš** – registravimo šablonas, naudojamas įvesti numatytąją pagrindinę Gautinų sumų ir Mokėtinų sumų sąskaitą užsienio valiutos perkainojimo operacijų apskaitos įrašams:
    -   **Registravimas** – naudojamos kliento operacijos registravimo šablonas.
    -   **Pasirinkti** – įveskite registravimo šabloną lauke **Registravimo šablonas**.
-   **Registravimo šablonas** – jei **Pasirinkti** pasirinkta lauke **Naudoti registravimo šabloną iš**, šiame lauke įvestas registravimo šablonas nustato užsienio valiutos kurso pasikeitimo operacijų registravimo šabloną.
-   **Finansinės dimensijos** – finansinės dimensijos, kurios užregistruotos užsienio valiutos kurso pasikeitimo operacijų apskaitos įrašuose:
    -   **Nėra** – neužregistruota jokių finansinių dimensijų. Jei jūsų sąskaitos struktūroje yra reikiama finansinė dimensija, perkainojimo procesas vis dar vykdomas ir sukuriami apskaitos įrašai, kurie neturi finansinių dimensijų. Pirma gausite perspėjimo pranešimą, kad galėtumėte atšaukti perkainojimą.
    -   **Lentelė** – kliento sąskaitos arba tiekėjo sąskaitos finansinės dimensijos užregistruotos užsienio valiutos kurso pasikeitimo operacijose.
    -   **Registravimas** – perkainojamos ir užsienio valiutos pasikeitimo operacijoje registruojamos operacijos finansinė dimensija. Pagal numatytuosius nustatymus, finansinės dimensijos iš pradinės operacijos AR / AP didžiosios knygos sąskaitos bus naudojama perkainavimo operacijos AR / AP pagrindinėje sąskaitoje, o finansinės dimensijos iš pradinės operacijos išlaidų / turto / įplaukų didžiosios knygos sąskaitos bus naudojamos perkainojimo operacijos negauto pelno / nepatirtų nuostolių pagrindinėje sąskaitoje.



