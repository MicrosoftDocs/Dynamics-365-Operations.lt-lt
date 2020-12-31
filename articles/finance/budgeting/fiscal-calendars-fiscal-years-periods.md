---
title: Ataskaitiniai kalendoriai, ataskaitiniai metai ir laikotarpiai
description: Šiame straipsnyje aptarti finansiniai kalendoriai, finansiniai metai ir laikotarpiai ir kaip juos naudoti juridiniams subjektams, ilgalaikiam turtui ir biudžeto sudarymui.
author: aprilolson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b23b152ed6348b8f20b5deccf94394de6fbe85d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446112"
---
# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Ataskaitiniai kalendoriai, ataskaitiniai metai ir laikotarpiai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aptarti finansiniai kalendoriai, finansiniai metai ir laikotarpiai ir kaip juos naudoti juridiniams subjektams, ilgalaikiam turtui ir biudžeto sudarymui.

Finansiniai kalendoriai suteikia rėmus organizacijos finansinei veiklai. Kiekviename finansiniame kalendoriuje yra vieneri ar keleri finansiniai metai, o kiekvienuose finansiniuose metuose yra keli laikotarpiai. Finansiniai kalendoriai gali būti grindžiami kalendoriniais metais nuo sausio 1 d. iki gruodžio 31 d. arba bet kokiomis kitomis pasirinktomis datomis. Pavyzdžiui, kai kurios organizacijos pasirenka finansinį kalendorių, kuris prasideda vienų metų liepos 1 d. ir baigiasi kitų metų birželio 30 d. 

Galite kurti kiek norite finansinių kalendorių, o finansiniame kalendoriuje galite kurti kiek norite finansinių metų. Kiekvienas finansinis kalendorius yra nepriklausomas nuo jūsų organizacijos, jį gali naudoti keli organizacijos juridiniai subjektai. Pavyzdžiui, organizacija turi aštuonis skyrius ir kiekvienas skyrius yra atskiras juridinis subjektas. Penki iš jų naudoja tą patį finansinį kalendorių, o trys – kitokius finansinius kalendorius. Galite kurti vieną finansinį kalendorių penkiems juridiniams subjektams, turintiems tą patį finansinį kalendorių, o tada kurti atskirus finansinius kalendorius kitiems juridiniams subjektams.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Finansinių kalendorių, finansinių metų ir laikotarpių kūrimas
Kurti ir naikinti ataskaitinius kalendorius, ataskaitinius metus ir laikotarpius galite Ataskaitinių kalendorių puslapyje. Taip pat galite skaidyti esamus laikotarpius ir kurti uždarymo laikotarpius, kuriais naudojantis galima baigti finansinius metus. 

Uždarymo laikotarpis naudojamas siekiant atskirti didžiosios knygos operacijas, generuojamas uždarant finansinius metus. Jei uždarymo operacijos priklauso vienam ataskaitiniam laikotarpiui, lengviau kurti finansines ataskaitas, kurios apima įvairių tipų uždarymo įrašus arba neapima jų. Jei finansiniai metai dalijami į 12 ataskaitinių laikotarpių, uždarymo laikotarpis paprastai yra 13 laikotarpis. Bet uždarymo laikotarpį galima sukurti iš bet kokio laikotarpio, kurio būsena yra Atidarytas. 

Kurdami uždarymo laikotarpį, pasirinkite laikotarpį, kurio būsena yra Atidarytas ir kuriame yra norimos naudoti datos. Naujasis uždarymo laikotarpis nukopijuos esamo laikotarpio pradžios ir pabaigos datas. Pradinis laikotarpis ir toliau egzistuos. Pavyzdžiui, pasirenkate 12 laikotarpį, kuris yra paskutinis finansinių metų laikotarpis ir kuriame yra datos nuo rugpjūčio 1 d. iki rugpjūčio 31 d. Įvedate uždarymo laikotarpio pavadinimą, pvz., Uždarymas. Sukūrę naują uždarymo laikotarpį, turite pradinį laikotarpį ir uždarymo laikotarpį. Abu turi datas, kurios prasideda rugpjūčio 1 d. ir baigiasi rugpjūčio 31 d.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Finansinių kalendorių pasirinkimas didžiosioms knygoms, ilgalaikiam turtui ir biudžeto ciklams
Finansiniai kalendoriai naudojami su ilgalaikio turto nusidėvėjimu, finansinėmis operacijomis ir biudžeto ciklais. Sukūrę finansinį kalendorių, galite naudoti jį keliems tikslams. Galite pasirinkti ilgalaikio turto knygos finansinį kalendorių ir paversti jį ilgalaikio turto kalendoriumi. Galite pasirinkti finansinį kalendorių didžiajai knygai ir paversti jį didžiosios knygos kalendoriumi. Taip pat galite pasirinkti finansinį kalendorių biudžeto ciklui ir paversti jį biudžeto kalendoriumi. Visiems jiems galite naudoti tą patį finansinį kalendorių.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Juridinio subjekto finansinio kalendoriaus pasirinkimas

Pasirinkite ataskaitinį kalendorių, kurį norite naudoti savo juridinio subjekto didžiajai knygai, formoje DK. Ataskaitinį kalendorių reikia pasirinkti formoje DK kiekvienam juridiniam subjektui. Pasirinkę ataskaitinį kalendorių, galite nustatyti laikotarpio būsenas ir teises puslapyje DK kalendorius bet kuriam iš laikotarpių, kurie yra ataskaitinių metų dalis.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Ilgalaikio turto finansinio kalendoriaus pasirinkimas

Galite pasirinkti ilgalaikio turto knygos finansinį kalendorių, ir tą finansinį kalendorių naudos ilgalaikis turtas, kuris naudoja pasirinktą knygą. Galite pasirinkti iš bet kurio ataskaitinio kalendoriaus, apibrėžto puslapyje Ataskaitiniai kalendoriai.

### <a name="define-budget-cycle-time-spans"></a>Biudžeto ciklo trukmės apibrėžimas

Biudžeto ciklas – tai laikotarpis, kurį naudojamas biudžetas. Biudžeto ciklas gali apimti dalį finansinių metų arba kelerius finansinius metus, pvz., dvimetį biudžeto ciklą sudaro dveji metai, o trimetį biudžeto ciklą – treji metai. Biudžeto ciklo trukmė apibrėžia į biudžeto ciklą įtrauktų laikotarpių skaičių. Norėdami nurodyti biudžeto ciklo trukmę, naudokite Biudžeto ciklų trukmių puslapį.

## <a name="maintain-periods-for-your-organization"></a>Jūsų organizacijos laikotarpių priežiūra
Puslapyje DK kalendorius galite peržiūrėti informaciją apie jūsų organizacijos naudojamą ataskaitinį kalendorių, ataskaitinius metus ir laikotarpius. Taip pat galite keisti laikotarpių būseną ir pasirinkti, kurie vartotojai gali registruoti apskaitos operacijas laikotarpiuose. Pvz., galite nurodyti, kad naujo laikotarpio pradžioje tam tikra vartotojų grupė turi baigti registruoti finansines operacijas į ankstesnį laikotarpį, o kitos grupės naudotu tik naują laikotarpį.





