---
title: Užsakymų pranešimų rodymas elektroniniame kasos aparate (EKA)
description: Šioje temoje aprašyta, kaip įjungti užsakymų pranešimų rodymą elektroniniame kasos aparate ir pranešimų sistemoje.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 04dd57aabcbdf5291f06317800b69f29f15d2763
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023361"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Užsakymų pranešimų rodymas elektroniniame kasos aparate (EKA)

[!include [banner](includes/banner.md)]

Modernioje mažmeninės prekybos aplinkoje parduotuvės atstovams priskiriamos įvairios užduotys, pvz., pagalba klientams, operacijų įvedimas, inventorizacijos atlikimas ir užsakymų parduotuvėje priėmimas. Elektroninio kasos aparato (EKA) klientas – tai viena programa, kurioje atstovai gali atlikti visas šias užduotis ir daug kitų. Kadangi per dieną reikia atlikti įvairias užduotis, gali reikėti, kad atstovams būtų pranešama, kai kažkam reikia skirti dėmesio. EKA pranešimų sistema mažmenininkams padeda leisdama konfigūruoti pranešimus pagal vaidmenį. „Dynamics 365 for Retail“, turinčiam 5 programos naujinį, šie pranešimai gali būti sukonfigūruoti tik vykdant EKA operacijas.


Šiuo metu sistema gali rodyti tik pranešimus apie užsakymų vykdymo operacijas. Tačiau kadangi sistema sukurta taip, kad ją būtų galima išplėsti, programuotojai ilgainiui galės parašyti bet kokios operacijos pranešimų apdorojimo programą ir tos operacijos pranešimus rodyti el. kasos aparate.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Užsakymo įvykdymo operacijų pranešimų įjungimas

Norėdami įjungti užsakymų vykdymo operacijų pranešimus, atlikite toliau nurodytus veiksmus.

1. Eikite į **„Retail and Commerce“** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Operacijos**.
2. Suraskite operaciją **Užsakymų vykdymas** ir prie jos pažymėkite žymės langelį **Įjungti pranešimus**, kad nurodytumėte, jog pranešimų sistema turi klausyti šios operacijos apdorojimo programos. Jei apdorojimo programa įdiegta, tada šios operacijos pranešimai bus rodomi el. kasos aparate.
3. Skirtuke „Commerce“ eikite į **„Retail and Commerce“** &gt; **Darbuotojai** &gt; **Darbininkai** &gt; ir atidarykite su darbuotoju susijusius EKA leidimus. Išplėskite „FastTab“ **Pranešimai**, įtraukite operaciją **Užsakymų vykdymas** ir lauką **Rodymo tvarka** nustatykite kaip **1**. Jei sukonfigūruotas daugiau nei vienas pranešimas, šis laukas naudojamas išdėstyti pranešimus. Pranešimai, kurių lauko **Rodymo tvarka** reikšmė yra mažesnė, rodomi virš pranešimų, kurių reikšmė didesnė. Pranešimai, kurių lauko **Rodymo tvarka** reikšmė yra **1**, rodomi viršuje.

    Pranešimai rodomi tik apie tas operacijas, kurios yra įtrauktos į „FastTab“ **Pranešimai**, ir ten įtraukti operacijų galite, tik jei puslapyje **EKA operacijos** prie tų operacijų pažymėtas žymės langelis **Įjungti pranešimus**. Be to, pranešimai apie tam tikrą operaciją darbininkams rodomi, tik jei ta operacija įtraukta į tų darbininkų EKA teises.

    > [!NOTE]
    > Pranešimų galima nepaisyti vartotojo lygiu. Atidarykite darbininko įrašą, pasirinkite **EKA teisės** ir redaguokite vartotojo pranešimų prenumeratą.

4. Eikite į **„Retail and Commerce“** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Funkcionalumo profiliai**. Lauke **Pranešimų intervalas** nurodykite, kaip dažnai turi būti rodomi pranešimai. Dėl kai kurių pranešimų EKA turi realiuoju laiku kreiptis į tarnybinio biuro programą. Tokie kreipimaisi naudoja jūsų tarnybinio biuro programos skaičiavimo pajėgumus. Todėl, nustatydami pranešimų intervalą, turite atsižvelgti į savo verslo poreikius ir kreipimųsi realiuoju laiku poveikį tarnybinio biuro programai. Reikšmė **0** (nulis) pranešimus išjungia.
5. Eikite į **„Retail and Commerce“** &gt; **„Retail and Commerce IT“** &gt; **Paskirstymo grafikas**. Pasirinkite grafiką **1060** (**Darbuotojai**), kad sinchronizuotumėte pranešimų prenumeratos parametrus, tada pasirinkite **Vykdyti dabar**. Tada pasirinkite grafiką **1070** (**Kanalo konfigūravimas**), kad sinchronizuotumėte teisių intervalą, tada pasirinkite **Vykdyti dabar**.

## <a name="view-notifications-in-the-pos"></a>Pranešimų peržiūra el. kasos aparate

Jums atlikus ankstesnius veiksmus, darbininkai el. kasos aparate galės peržiūrėti pranešimus. Norėdami peržiūrėti pranešimus, spustelėkite viršutiniame dešiniajame EKA kampe esančią pranešimų piktogramą. Rodomas pranešimų centras, kuriame rodomi užsakymų vykdymo operacijos pranešimai. Pranešimų centras turėtų rodyti toliau nurodytas užsakymų vykdymo operacijos grupes.

- **Paėmimas parduotuvėje** – šioje grupėje rodomas užsakymų, kurių pristatymo būdas **Paėmimas**, o paėmimas suplanuotas dabartinėje parduotuvėje, skaičius. Galite paspausti grupėje rodomą skaičių, kad atidarytumėte puslapį **Užsakymų vykdymas**. Tokiu atveju puslapis bus filtruojamas, kad jame būtų rodomi tik aktyvūs užsakymai, kuriuos nustatyta paimti iš dabartinės parduotuvės.
- **Siųsti iš parduotuvės** – šioje grupėje rodomas užsakymų, kurių pristatymo būdas **Siuntimas**, o siuntimas suplanuotas iš dabartinės parduotuvės, skaičius. Galite paspausti grupėje rodomą skaičių, kad atidarytumėte puslapį **Užsakymų vykdymas**. Tokiu atveju puslapis bus filtruojamas, kad jame būtų rodomi tik aktyvūs užsakymai, kuriuos nustatyta siųsti iš dabartinės parduotuvės.

Kai parduotuvei priskiriami nauji vykdytini užsakymai, pranešimų piktograma pasikeičia ir nurodo, kad yra naujų pranešimų, o atitinkamose grupėse rodomas skaičius atnaujinamas. Nors grupės atnaujinamos reguliariai, EKA vartotojai gali bet kada grupes atnaujinti rankiniu būdu, pasirinkdami prie grupės esantį mygtuką **Atnaujinti**. Galiausiai, jei grupėje yra nauja prekė, kurios darbininkas neperžiūrėjo, grupėje rodomas sprogimo simbolis, nurodantis naują turinį.

## <a name="enable-live-content-on-pos-buttons"></a>Tiesioginio turinio įjungimas ant EKA mygtukų

Ant EKA mygtukų dabar gali būti rodomas skaičius, kad darbininkai galėtų lengviau nustatyti, į kurias užduotis reikia nedelsiant atkreipti dėmesį. Norėdami ant EKA mygtuko rodyti šį skaičių, turite atlikti pranešimų sąranką, aprašyta anksčiau šioje temoje (t. y., turite įjungti operacijos pranešimus, nustatyti pranešimų intervalą ir atnaujinti darbininko EKA teisių grupę). Be to, turite atidaryti mygtukyno dizaino įrankį, peržiūrėti mygtuko ypatybes ir pažymėti žymės langelį **Įjungti tiesioginį turinį**. Lauke **Turinio lygiuotė** galite pasirinkti, ar skaičius rodomas viršutiniame dešiniajame mygtuko kampe (**Viršuje, dešinėje**), ar centre (**Centre**).

> [!NOTE]
> Tiesioginį operacijų turinį galima įjungti, tik jei puslapyje **EKA operacijos** prie jų pažymėtas žymės langelis **Įjungti pranešimus**, kaip aprašyta anksčiau šioje temoje.

Tolesnėje iliustracijoje rodomi tiesioginio turinio parametrai mygtukyno dizaino įrankyje.

![Tiesioginio turinio nustatymai mygtuko dizaino įrankyje](./media/ButtonGridDesigner.png "Tiesioginio turinio nustatymai mygtuko dizaino įrankyje")

Norėdami rodyti pranešimų skaičių ant mygtuko, turite užtikrinti, kad būtų atnaujintas teisingas ekrano maketas. Norėdami nustatyti ekrano maketą, kurį naudos EKA, viršutiniame dešiniajame kampe pasirinkite piktogramą **Parametrai** ir įsidėmėkite **Ekrano maketo ID** ir **Maketo skiriamąją gebą**. Dabar naudodami naršyklę „Edge“ eikite į puslapį **Ekrano maketas**, suraskite anksčiau įsidėmėtą **Ekrano maketo ID** ir **Maketo skiriamąją gebą** ir pažymėkite žymės langelį **Įjungti tiesioginį turinį**. Eikite į **„Retail and Commerce“ \> „Retail and Commerce IT“ \> Paskirstymo grafikas** ir paleiskite 1090 (registrai) užduotį, kad susinchronizuotumėte maketo pakeitimus.


![Raskite EKA naudojamą ekrano maketą](./media/Choose_screen_layout.png "Raskite ekrano maketą")

Tolesnėje iliustracijoje rodoma, kaip įvairių dydžių mygtukus veikia lauko **Turinio lygiuotė** parinktys **Viršuje, dešinėje** ir **Centre**.

![Tiesioginis turinys EKA mygtukuose](./media/ButtonsWithLiveContent.png "Tiesioginis turinys EKA mygtukuose")
