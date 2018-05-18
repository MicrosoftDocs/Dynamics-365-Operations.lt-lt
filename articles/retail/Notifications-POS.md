---
title: "Užsakymų pranešimų rodymas elektroniniame kasos aparate"
description: "Šioje temoje aprašyta, kaip įjungti užsakymų pranešimų rodymą elektroniniame kasos aparate ir pranešimų sistemoje. Ilgainiui programuotojai šiuos pranešimus galės išplėsti ir naudoti ne tik su užsakymų vykdymo operacijomis."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: a55af4c26d74cc392d3c53aacb66e0a8bc97abf2
ms.contentlocale: lt-lt
ms.lasthandoff: 03/13/2018

---

# <a name="show-order-notifications-in-the-point-of-sale"></a>Užsakymų pranešimų rodymas elektroniniame kasos aparate

[!include [banner](includes/banner.md)]

Modernioje mažmeninės prekybos aplinkoje parduotuvės atstovams priskiriamos įvairios užduotys, pvz., pagalba klientams, operacijų įvedimas, inventorizacijos atlikimas ir užsakymų parduotuvėje priėmimas. Elektroninio kasos aparato (EKA) klientas – tai viena programa, kurioje atstovai gali atlikti visas šias užduotis ir daug kitų. Kadangi per dieną reikia atlikti įvairias užduotis, gali reikėti, kad atstovams būtų pranešama, kai kažkam reikia skirti dėmesio. EKA pranešimų sistema mažmenininkams padeda leisdama konfigūruoti pranešimus pagal vaidmenį. Programoje „Microsoft Dynamics 365 for Retail“ su 5 programos naujinimu šiuos pranešimus galima konfigūruoti tik EKA operacijoms.

Šiuo metu sistema gali rodyti tik pranešimus apie užsakymų vykdymo operacijas. Tačiau kadangi sistema sukurta taip, kad ją būtų galima išplėsti, programuotojai ilgainiui galės parašyti bet kokios operacijos pranešimų apdorojimo programą ir tos operacijos pranešimus rodyti el. kasos aparate.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Užsakymo įvykdymo operacijų pranešimų įjungimas

Norėdami įjungti užsakymų vykdymo operacijų pranešimus, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Operacijos**.
2. Suraskite operaciją **Užsakymų vykdymas** ir prie jos pažymėkite žymės langelį **Įjungti pranešimus**, kad nurodytumėte, jog pranešimų sistema turi klausyti šios operacijos apdorojimo programos. Jei apdorojimo programa įdiegta, tada šios operacijos pranešimai bus rodomi el. kasos aparate.
3. Eikite į **Mažmeninė prekyba** &gt; **Darbuotojai** &gt; **Darbininkai** &gt;, skirtuke Mažmeninė prekyba atidarykite su darbininku susietas EKA teises. Išplėskite „FastTab“ **Pranešimai**, įtraukite operaciją **Užsakymų vykdymas** ir lauką **Rodymo tvarka** nustatykite kaip **1**. Jei sukonfigūruotas daugiau nei vienas pranešimas, šis laukas naudojamas išdėstyti pranešimus. Pranešimai, kurių lauko **Rodymo tvarka** reikšmė yra mažesnė, rodomi virš pranešimų, kurių reikšmė didesnė. Pranešimai, kurių lauko **Rodymo tvarka** reikšmė yra **1**, rodomi viršuje.

    Pranešimai rodomi tik apie tas operacijas, kurios yra įtrauktos į „FastTab“ **Pranešimai**, ir ten įtraukti operacijų galite, tik jei puslapyje **EKA operacijos** prie tų operacijų pažymėtas žymės langelis **Įjungti pranešimus**. Be to, pranešimai apie tam tikrą operaciją darbininkams rodomi, tik jei ta operacija įtraukta į tų darbininkų EKA teises.

    > [!NOTE]
    > Pranešimų galima nepaisyti vartotojo lygiu. Atidarykite darbininko įrašą, pasirinkite **EKA teisės** ir redaguokite vartotojo pranešimų prenumeratą.

4. Eikite į **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Funkcijų profiliai**. Lauke **Pranešimų intervalas** nurodykite, kaip dažnai turi būti rodomi pranešimai. Dėl kai kurių pranešimų EKA turi realiuoju laiku kreiptis į tarnybinio biuro programą. Tokie kreipimaisi naudoja jūsų tarnybinio biuro programos skaičiavimo pajėgumus. Todėl, nustatydami pranešimų intervalą, turite atsižvelgti į savo verslo poreikius ir kreipimųsi realiuoju laiku poveikį tarnybinio biuro programai. Reikšmė **0** (nulis) pranešimus išjungia.
5. Eikite į **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**. Pasirinkite grafiką **1060** (**Darbuotojai**), kad sinchronizuotumėte pranešimų prenumeratos parametrus, tada pasirinkite **Vykdyti dabar**. Tada pasirinkite grafiką **1070** (**Kanalo konfigūravimas**), kad sinchronizuotumėte teisių intervalą, tada pasirinkite **Vykdyti dabar**.

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

![Tiesioginio turinio parametrai mygtukyno dizaino įrankyje](./media/ButtonGridDesigner.png "Tiesioginio turinio parametrai mygtukyno dizaino įrankyje")

Tolesnėje iliustracijoje rodoma, kaip įvairių dydžių mygtukus veikia lauko **Turinio lygiuotė** parinktys **Viršuje, dešinėje** ir **Centre**.

![Tiesioginis turinys ant EKA mygtukų](./media/ButtonsWithLiveContent.png "Tiesioginis turinys ant EKA mygtukų")

