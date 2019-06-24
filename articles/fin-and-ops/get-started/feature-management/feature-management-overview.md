---
title: Funkcijų valdymo apžvalga
description: Šioje temoje aprašoma funkcijų valdymo priemonė ir kaip ją naudoti.
author: mikefalkner
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: b200156a623c67a562cc1a5952899e3a77517528
ms.sourcegitcommit: bbc9aa0d6b94a942e1f4d5b038601509dcc87937
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/05/2019
ms.locfileid: "1619149"
---
# <a name="feature-management-overview"></a>Funkcijų valdymo apžvalga

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funkcijos įtraukiamos ir atnaujinamos kiekvieną kartą išleidus „Microsoft Dynamics 365 for Finance and Operations“. Funkcijų valdymo patirtis suteikia darbo sritį, kurioje galite peržiūrėti kiekviename leidime pristatytų funkcijų sąrašą. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją.

## <a name="the-feature-management-workspace"></a>Funkcijų valdymo darbo sritis.

Galite atidaryti **Funkcijų valdymo** darbo sritį, pasirinkdami reikiamą plytelę ataskaitų srityje. Pasirodys puslapis, kuriame pateikiamas visų leidimų, kuriuos palaiko funkcijos valdymo patirtis, funkcijų sąrašas. Ilgainiui „Microsoft“ patobulins funkcijų valdymo patirtį, kad į ją būtų įtrauktos papildomos funkcijos, padedančios tvarkyti funkcijos.

Funkcijų sąraše pateikiama toliau nurodyta informacija.

- **Funkcijos pavadinimas** – pridėtos funkcijos aprašymas.
- **Įjungimo būsena** – simbolis nurodo, ar funkcija įjungta (varnelė), ar neįgalinta (tuščia), ar ji numatyta įjungti (laikrodis), ar yra privalomai įjungta (spyna). Čia rodomas parametras naudojamas visiems juridiniams subjektams. Atkreipkite dėmesį, kad net jei funkcija buvo įjungta, ją vis dar valdo sauga. Todėl funkcija bus prieinama tik tiems vartotojams, kurie turi prieigą prie jos, atsižvelgiant į jų saugos vaidmenį. Ji taip pat bus prieinama tik juridiniams subjektams, prie kurių vartotojas turi prieigą.
- **Įjungimo data** – diena, kurią funkcija buvo įjungta arba yra suplanuota ją įjungti.
- **Funkcija įtraukta** – data, kai funkcija buvo įdėta į jūsų aplinką. Ši data automatiškai įvedama, kai atnaujinate savo aplinką mėnesio išleidimo ciklais.
- **Modulis** – modulis, kurį paveikė nauja funkcija.

Pasirinkus funkciją, išsamios informacijos srityje rodoma papildoma informacija funkcijų sąrašo dešinėje. Srities viršuje matysite funkcijos pavadinimą, datą, kada funkcija buvo papildyta, modulį, kuris yra paveiktas funkcijos ir saitą **Sužinoti daugiau**. Pasirinkite šį saitą norėdami peržiūrėti funkcijos dokumentaciją. Jei dokumentacija nepasiekiama, būsite nukreipti į laikiną puslapį. Informacijos srityje taip pat yra laukas **Komentarai**, į kurį galite įtraukti savo komentarus apie funkciją.

Darbo srityje **Funkcijų valdymas** taip pat yra keli skirtukai ir kiekviename iš jų pateikiamas funkcijų sąrašas.

- **Nauja** – šis skirtukas rodo visas funkcijas, kurios buvo įtrauktos po paskutinio mėnesio atnaujinimo. Jei neįdiegėte kurio nors mėnesio atnaujinimo, skirtuke bus parodytos visos naujos funkcijos, kurios buvo įtrauktos po paskutinio jūsų atnaujinimo. Naujausios funkcijos rodomos sąrašo viršuje. Bendras naujų funkcijų skaičius taip pat rodomas plytelėje puslapio viršuje.
- **Neįjungta** – šiame skirtuke rodomos visos neįjungtos funkcijos. Naujausios funkcijos rodomos sąrašo viršuje. Bendras naujų neįjungtų funkcijų skaičius taip pat rodomas plytelėje puslapio viršuje.
- **Suplanuota** – šiame skirtuke rodomos visos funkcijos, kurios suplanuotos įjungti ateityje. Funkcijos, kurios bus įjungtos anksčiausiai, rodomos sąrašo viršuje. Bendras naujų suplanuotų funkcijų skaičius taip pat rodomas plytelėje puslapio viršuje.
- **Visos** – šiame skirtuke rodomos visos funkcijos. Naujausios funkcijos rodomos sąrašo viršuje.

## <a name="turn-on-a-feature"></a>Funkcijos įjungimas

Jei funkcija neįjungta, informacijos srityje rodomas mygtukas **Įjungti dabar**. Šį mygtuką galite naudoti, kad funkciją įjungtumėte.

- Pasirinkite norimą įjungti funkciją, tada informacijos srityje pasirinkite **Įjungti dabar**. Funkcija įjungta.

Įjungus kai kurias funkcijas, jų išjungti negalima. Jei funkcija, kurią mėginate įjungti, negali būti išjungta, gausite įspėjimą. Šiuo metu galite pasirinkti **Atšaukti**, norėdami atšaukti operaciją ir palikti funkciją išjungtą. Tačiau, jei pasirinksite **Įjungti** ir įjungsite funkciją, negalėsite jos išjungti vėliau.

Kai funkcija įjungta, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad funkcija buvo įjungta, arba nurodo, kada funkcija suplanuota įjungti ateityje. Jis rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše.

Funkcijos, kurios yra suplanuotos įjungti ateityje, rodomos skirtuke **Suplanuota**. Paketinis vykdymas jas įjungs nurodytos dienos vidurnaktį, atsižvelgiant į sistemoje nustatytą laiko juostą.

## <a name="reschedule-a-feature"></a>Iš naujo suplanuoti funkciją

Jei funkcija suplanuota įjungti ateityje, informacijos srityje atsiranda mygtukas **Planuoti**. Šį mygtuką galite naudoti, jei norite pakeisti lauko **Įjungimo data** vertę į kitą datą.

1. Pasirinkite suplanuotą funkciją, kurią norite perplanuoti, tada informacijos srityje pasirinkite **Planuoti**.
2. Pasirodžiusio dialogo lango lauke **Įjungimo data** nurodykite naują funkcijos įjungimo datą.
3. Pasirinkite **Įgalinti**, jei norite perplanuoti priemonę **Išjungti**, kad atšauktumėte planą.

## <a name="turn-off-a-feature"></a>Funkcijos išjungimas

Jei funkcija jau įjungta, informacijos srityje atsiranda mygtukas **Išjungti**. Šį mygtuką galite naudoti, kad funkciją išjungtumėte. Mygtukas **Išjungti** neveikia, jei funkcija negali būti išjungta ją įjungus.

- Pasirinkite norimą išjungti funkciją, tada informacijos srityje pasirinkite **Išjungti.** Funkcija išjungiama ir laukas **Įjungimo data** išvalomas.

Kai funkcija išjungta, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad funkcija dar nebuvo įjungta. Jis rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše. Neįjungtos funkcijos rodomos skirtuke **Neįjungta**.

## <a name="features-that-must-be-turned-on"></a>Funkcijos, kurias reikia įjungti

Kartais įtraukiama svarbi funkcija, kurią būtina įjungti automatiškai, kai naujinate. Šios funkcijos bus automatiškai įjungiamos lauke **Įjungimo data** nurodytą dieną. Naudojant šias funkcijas, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad funkcija buvo įjungta, arba nurodo, kada funkcija bus įjungta ateityje. Jis rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše.

## <a name="turn-on-all-features-automatically"></a>Automatinis visų funkcijų įjungimas

Pagal numatytuosius nustatymus visos į jūsų aplinką įtrauktos funkcijos yra išjungtos, nebent jos yra privalomos funkcijos. Tačiau, jei norite automatiškai įjungti visas naujas funkcijas, galite naudoti išplečiamąjį sąrašą, esantį darbo srities pavadinime, kad pakeistumėte tai, kas atsitinka, kai įtraukiamos naujos funkcijos.

- Pasirinkite **Visos naujos funkcijos bus įjungtos pagal numatytuosius parametrus**, kad visos naujos funkcijos būtų automatiškai įjungiamos įtraukiant jas į jūsų aplinką.
- Pasirinkite **Visos naujos funkcijos bus išjungtos pagal numatytuosius parametrus**, kad visos naujos funkcijos būtų automatiškai išjungiamos įtraukiant jas į jūsų aplinką.

## <a name="assigning-roles"></a>Vaidmenų priskyrimas

Darbo sritį **Funkcijų valdymas** gali atidaryti sistemos administratoriai ir vartotojai, kuriems priskirtas vaidmuo Funkcijų tvarkytojas arba Funkcijų tikrintojas. Šie du vaidmenys buvo sukurti, kad būtų palaikoma funkcijų valdymo sąsaja. Funkcijų tvarkymo vaidmens vartotojai gali įjungti arba išjungti bet kokią funkciją. Jie taip pat gali atnaujinti funkcijos lauką **Komentarai**. Vartotojai, esantys funkcijos peržiūros vaidmenyje, gali tik peržiūrėti darbo sritį **Funkcijų valdymas**. Jie negali įjungti arba išjungti funkcijų.

Funkcijų tvarkymo vaidmuo ir funkcijų peržiūros vaidmuo neperrašo esamos saugos, kurią turi vartotojas. Jie paprasčiausiai valdo tai, ar vartotojas gali įjungti arba išjungti funkcijas. Jie nesuteikia prieigos prie pačios funkcijos.

## <a name="features-that-use-configuration-keys"></a>Funkcijos, naudojančios konfigūracijos raktus

Jei funkcija naudoja konfigūracijos raktą, bet konfigūracijos raktas nėra įjungtas, darbo srities **Funkcijų valdymas** galimų funkcijų sąraše funkcija nerodoma. Įjungę konfigūracijos raktą, turite atnaujinti funkcijų sąrašą naudodami elementą **Tikrinti naujinius**. Tada funkcija bus rodoma funkcijų sąraše.

Jei išjungsite konfigūracijos raktą, funkcija nebus pašalinta iš funkcijų sąrašo.

## <a name="data-entities"></a>Duomenų objektai

Duomenų objektas pavadinimu **Funkcijų valdymas** suteikia galimybę eksportuoti funkcijų valdymo parametrus iš vienos aplinkos ir importuoti juos į kitą aplinką. Šis objektas atnaujina tik esamas funkcijas. Objekto verslo logika taip pat padeda užtikrinti, kad atlikus importavimą bus taikomos tos pačios taisyklės, kurios naudojamos darbo srityje **Funkcijų valdymas**. Pavyzdžiui, negalite perrašyti privalomų funkcijų nustatymo pašalindami datą importavimo metu.

Toliau pateikiami pavyzdžiai apibūdina, kas atsitinka, kai duomenis importuojami naudojant objektą **Funkcijų valdymas**.

- Jei lauko **Įjungta** vertę pakeisite į **Taip**, ši funkcija bus įjungta, o lauke **Įjungimo data** bus nustatyta esama data.
- Jei lauko **Įjungta** vertę pakeisite į **Ne** paliksite lauką **Įjungimo data** tuščią, funkcija bus išjungta, o laukas **Įjungimo data** – išvalytas. Negalite išjungti privalomos funkcijos arba funkcijos, kurios negalima išjungti ją įjungus.
- Jei lauko **Įjungimo data** vertę pakeisite į būsimą datą, funkcija bus suplanuota įjungti tą dieną.
- Jei lauko **Įjungta** vertę pakeisite į **Taip**, o lauko **Įjungimo data** vertę pakeisite į būsimą datą, ši funkcija bus įjungti tą dieną. 
- Jei lauko **Įjungta** vertę pakeisite į **Ne**, o lauko **Įjungimo data** vertę pakeisite į būsimą datą, ši funkcija bus įjungti tą dieną.
- Jei funkcija įjungta, o jūs įtraukiate lauką **Įjungimo data**, kuris nustatytas į būsimą datą, funkcija lieka įjungta. Norėdami perplanuoti funkciją, turite pakeisti lauko **Įjungta** vertę į **Ne**.

## <a name="feature-management-and-flighting"></a>Funkcijų valdymas ir versijos

Funkcijų valdymas suteikia galimybę kontroliuoti funkcijas, kurios įtraukiamos į kiekvieną leidimą. Versijos suteikia galimybę „Microsoft“ komandoms išleisti funkcijas ribotam klientų skaičiui, kad funkcijos galėtų būti išbandytos ir patikrintos nepakenkiant visiems klientams. Funkcijų valdymas nekontroliuoja funkcijų versijų.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Funkcijų valdymo naudojimas, siekiant įgalinti ISV funkcijas arba pasirinktines funkcijas

Funkcijų valdymas šiuo metu negalimas, jei funkcijas pateikė nepriklausomi programinės įrangos tiekėjai (ISV) arba jei jos pasirinktinės funkcijos. Tačiau „Microsoft“ įtraukia daugiau funkcijų, kad funkcijų valdymas būtų patobulintas. Baigusi šiuos patobulinimus „Microsoft“ suteiks galimybę naudoti funkcijų valdymą tvarkant visas funkcijas ir pateiks funkcijų naujinimo instrukcijas.
