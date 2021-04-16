---
title: Užsakymų pranešimų rodymas elektroniniame kasos aparate (EKA)
description: Šioje temoje aprašyta, kaip įjungti užsakymų pranešimų rodymą elektroniniame kasos aparate ir pranešimų sistemoje.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7b28a33dff4af6bf2b97db825a5a8304213f3a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796491"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Užsakymų pranešimų rodymas elektroniniame kasos aparate (EKA)

[!include [banner](includes/banner.md)]

Parduotuvės atstovams gali būti priskirtos įvairios parduotuvės užduotys, pvz., užsakymų vykdymas arba atsargų gavimo ar inventorizacijos atlikimas. Elektroninio kasos aparato (EKA) klientas – tai viena programa, kurioje atstovams gali būti pranešta apie visas šias užduotis. EKA pranešimų sistema mažmenininkams padeda leisdama konfigūruoti pranešimus pagal vaidmenį. Programoje „Dynamics 365 Retail“ su 5 programos naujinimu šiuos pranešimus galima konfigūruoti EKA operacijoms.

Sistema gali rodyti *užsakymo vykdymo* operacijos pranešimus, o „Commerce“ versijoje 10.0.18 taip pat gali būti rodomi *užsakymo atšaukimo* operacijos pranešimai. Tačiau kadangi sistema sukurta taip, kad ją būtų galima išplėsti, programuotojai gali [parašyti bet kokios operacijos pranešimų apdorojimo programą](dev-itpro/extend-pos-notification.md) ir tos operacijos pranešimus rodyti el. kasos aparate.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Užsakymo įvykdymo ar atšaukimo operacijų pranešimų įjungimas

Norėdami įjungti užsakymų vykdymo ar atšaukimo operacijų pranešimus, atlikite toliau nurodytus veiksmus.

1. Eikite į **„Retail” ir „Commerce” \> Kanalo sąranka \> EKA sąranka \> EKA \> Operacijos**.
1. Suraskite operaciją **Užsakymo vykdymas** arba **Atšaukti užsakymą** ir tada pasirinkite operacijos parinktį **Įjungti pranešimus**, kad nurodytumėte, jog pranešimų sistema turi klausyti šios operacijos apdorojimo programos. Jei apdorojimo programa įdiegta, tada šios operacijos pranešimai bus rodomi el. kasos aparate.
1. Eikite į **„Retail“ ir „Commerce“ \> Darbuotojai \> Darbininkai**.
1. Pasirinkite skirtuką **„Commerce”**, darbuotojo eilutę ir tada – **EKA teisės**. Pasirinkite „FastTab” **Pranešimai**, kad jį išplėstumėte, tada įtraukite operacijas, kurių pranešimus įgalinote. Jei konfigūruojamas vienas darbuotojo pranešimas, įsitikinkite, kad nustatyta reikšmė **Rodymo tvarka** nustatyta į **1**. Konfigūruodami daugiau nei vieną operaciją, nustatykite vertes **Rodymo tvarka**, kad nurodytumėte tvarką, kuria turi būti rodomi pranešimai. 

      Rodomi tik operacijų, kurios įtrauktos į „FastTab” **Pranešimai**, pranešimai. Ten operacijas galite įtraukti tik tada, jei tų operacijų žymės langeliai **Įgalinti pranešimus** yra pasirinkti puslapyje **EKA operacijos**. Be to, pranešimai apie tam tikrą operaciją darbininkams rodomi, tik jei ta operacija įtraukta į tų darbininkų EKA teises.

    > [!NOTE]
    > Pranešimų galima nepaisyti vartotojo lygiu. Norėdami tai atlikti, atidarykite darbininko įrašą, pasirinkite **EKA teisės** ir redaguokite vartotojo pranešimų prenumeratą.

1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Lauke **Pranešimų intervalas** nurodykite, kaip dažnai turi būti rodomi pranešimai. Dėl kai kurių pranešimų EKA turi realiuoju laiku kreiptis į tarnybinio biuro programą. Tokie kreipimaisi naudoja jūsų tarnybinio biuro programos skaičiavimo pajėgumus. Todėl, nustatydami pranešimų intervalą, turite atsižvelgti į savo verslo poreikius ir kreipimųsi realiuoju laiku poveikį tarnybinio biuro programai. Reikšmė **0** (nulis) pranešimus išjungia.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**. Pasirinkite grafiką **1060** (**Darbuotojai**), kad sinchronizuotumėte pranešimų prenumeratos parametrus, tada pasirinkite **Vykdyti dabar**. Tada pasirinkite grafiką **1070** (**Kanalo konfigūravimas**), kad sinchronizuotumėte teisių intervalą, tada pasirinkite **Vykdyti dabar**.

## <a name="view-notifications-in-the-pos"></a>Pranešimų peržiūra el. kasos aparate

Jums atlikus ankstesnius veiksmus, darbininkai el. kasos aparate galės peržiūrėti pranešimus. Norėdami peržiūrėti pranešimus, spustelėkite viršutiniame dešiniajame EKA kampe esančią pranešimų piktogramą. Atsiranda pranešimų sritis, kurioje rodomi pranešimai apie darbuotojui sukonfigūruotas operacijas. 

Pranešimų sritis rodys toliau nurodytas **užsakymo vykdymo** operacijos grupes.

- **Paėmimas parduotuvėje** – šioje grupėje rodomas atskirų užsakymo eilučių, kurių paėmimas suplanuotas dabartinėje parduotuvėje, skaičius. Galite pasirinkti grupės numerį, kad operacija **Užsakymo vykdymas** būtų atidaryta naudojant filtrą, kad joje būtų rodomos tik aktyvios užsakymo eilutės, nustatytos paėmimui iš dabartinės parduotuvės.
- **Siųsti iš parduotuvės** – šioje grupėje rodomas atskirų užsakymų eilučių, sukonfigūruotų siuntimui iš dabartinės vartotojo parduotuvės, skaičius. Galite pasirinkti grupės numerį, kad operacija **Užsakymo vykdymas** būtų atidaryta naudojant filtruotą rodinį, kad joje būtų rodomos tik aktyvios užsakymo eilutės, nustatytos siuntimui iš dabartinės parduotuvės.

Pranešimų sritis rodys toliau nurodytas **užsakymo atšaukimo** operacijos grupes.

- **Užsakymai, kuriuos reikia įvykdyti** – ši grupė nurodo užsakymų, sukonfigūruotų paėmimui iš dabartinės vartotojo parduotuvės arba siuntimui iš jos, skaičių. Galite pasirinkti grupės numerį, kad operacija **Atšaukti užsakymą** būtų atidaryta naudojant filtruotą rodinį, rodantį tik tuos atidarytus užsakymus, kuriuos turi įvykdyti dabartinė vartotojo parduotuvė, naudodama paėmimo iš parduotuvės arba siuntimo iš parduotuvės scenarijų.
- **Užsakymai, kuriuos reikia paimti** – šioje grupėje rodomas užsakymų, kurių paėmimas suplanuotas dabartinėje parduotuvėje, skaičius. Galite pasirinkti grupės numerį, kad operacija **Atšaukti užsakymą** būtų atidaryta naudojant filtruotą rodinį, rodantį tik tuos atidarytus užsakymus, kuriuos turi paimti iš dabartinės vartotojo parduotuvės.
- **Užsakymai, kuriuos reikia išsiųsti** – šioje grupėje rodomas užsakymų, kuriuos reikia išsiųsti iš dabartinės vartotojo parduotuvės, skaičius. Galite pasirinkti grupės numerį, kad operacija **Atšaukti užsakymą** būtų atidaryta naudojant filtruotą rodinį, rodantį tik tuos atidarytus užsakymus, kuriuos turi išsiųsti iš dabartinės vartotojo parduotuvės.

Tiek užsakymo vykdymo, tiek užsakymo atšaukimo pranešimo atveju, kai nauji užsakymai paimami proceso metu, pranešimo piktograma pasikeičia, siekiant nurodyti, kad yra naujų pranešimų ir kad atnaujinamas atitinkamų grupių skaičius. Nors grupės atnaujinamos reguliariai, EKA vartotojai gali bet kada grupes atnaujinti rankiniu būdu, pasirinkdami prie grupės esantį mygtuką **Atnaujinti**. Galiausiai, jei grupėje yra nauja prekė, kurios darbininkas neperžiūrėjo, grupėje rodomas sprogimo simbolis, nurodantis naują turinį.

## <a name="enable-live-content-on-pos-buttons"></a>Tiesioginio turinio įjungimas ant EKA mygtukų

Ant EKA mygtukų dabar gali būti rodomas skaičius, kad darbininkai galėtų lengviau nustatyti, į kurias užduotis reikia nedelsiant atkreipti dėmesį. Norėdami ant EKA mygtuko rodyti šį skaičių, turite atlikti pranešimų sąranką, aprašyta anksčiau šioje temoje (t. y., turite įjungti operacijos pranešimus, nustatyti pranešimų intervalą ir atnaujinti darbininko EKA teisių grupę). Be to, turite atidaryti mygtukyno dizaino įrankį, peržiūrėti mygtuko ypatybes ir pažymėti žymės langelį **Įjungti tiesioginį turinį**. Lauke **Turinio lygiuotė** galite pasirinkti, ar skaičius rodomas viršutiniame dešiniajame mygtuko kampe (**Viršuje, dešinėje**), ar centre (**Centre**).

> [!NOTE]
> Tiesioginį operacijų turinį galima įjungti, tik jei puslapyje **EKA operacijos** prie jų pažymėtas žymės langelis **Įjungti pranešimus**, kaip aprašyta anksčiau šioje temoje.

Tolesnėje iliustracijoje rodomi tiesioginio turinio parametrai mygtukyno dizaino įrankyje.

![Tiesioginio turinio nustatymai mygtuko dizaino įrankyje](./media/ButtonGridDesigner.png "Tiesioginio turinio nustatymai mygtuko dizaino įrankyje")

Norėdami rodyti pranešimų skaičių ant mygtuko, turite užtikrinti, kad būtų atnaujintas teisingas ekrano maketas. Norėdami nustatyti ekrano maketą, kurį naudos EKA, viršutiniame dešiniajame kampe pasirinkite piktogramą **Parametrai** ir įsidėmėkite **Ekrano maketo ID** ir **Maketo skiriamąją gebą**. Dabar naudodami naršyklę „Edge“ eikite į puslapį **Ekrano maketas**, suraskite anksčiau įsidėmėtą **Ekrano maketo ID** ir **Maketo skiriamąją gebą** ir pažymėkite žymės langelį **Įjungti tiesioginį turinį**. Eikite į **Mažmeninė prekyba ir komercija \> Mažmeninės prekybos ir komercijos ID \> Paskirstymo grafikas** ir paleiskite 1090 (registrai) užduotį, kad susinchronizuotumėte maketo pakeitimus.

![Raskite EKA naudojamą ekrano maketą](./media/Choose_screen_layout.png "Raskite ekrano maketą")

Tolesnėje iliustracijoje rodoma, kaip įvairių dydžių mygtukus veikia lauko **Turinio lygiuotė** parinktys **Viršuje, dešinėje** ir **Centre**.

![Tiesioginis turinys EKA mygtukuose](./media/ButtonsWithLiveContent.png "Tiesioginis turinys EKA mygtukuose")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
