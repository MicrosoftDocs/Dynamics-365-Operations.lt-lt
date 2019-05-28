---
title: Funkcijų valdymo apžvalga
description: Šioje temoje aprašoma funkcijų valdymo priemonė ir kaip ją naudoti.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538701"
---
# <a name="feature-management-overview"></a>Funkcijų valdymo apžvalga

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funkcijos įtraukiamos ir atnaujinamos kiekvieną kartą išleidus „Microsoft Dynamics 365 for Finance and Operations“. Funkcijų valdymo patirtis suteikia darbo sritį, kurioje galite peržiūrėti kiekviename leidime pristatytų funkcijų sąrašą. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją.

## <a name="the-feature-management-workspace"></a>Funkcijų valdymo darbo sritis.

Galite atidaryti **Funkcijų valdymo** darbo sritį, pasirinkdami reikiamą plytelę ataskaitų srityje. Pasirodys puslapis, kuriame pateikiamas visų leidimų, kuriuos palaiko funkcijos valdymo patirtis, funkcijų sąrašas. Ilgainiui „Microsoft“ patobulins funkcijų valdymo patirtį, kad į ją būtų įtrauktos papildomos funkcijos, padedančios tvarkyti funkcijos.

Funkcijų sąraše pateikiama toliau nurodyta informacija.

- **Funkcijos pavadinimas** – pridėtos funkcijos aprašymas.
- **Įgalinta būsena** – simbolis nurodo, ar funkcija įjungta (varnelė), ar neįgalinta (tuščia), ar ji numatyta įjungti (laikrodis), ar yra privalomai įjungta (spyna). Čia rodomas parametras naudojamas visiems juridiniams subjektams. Atkreipkite dėmesį, kad net jei funkcija buvo įjungta, ją vis dar valdo sauga. Todėl funkcija bus prieinama tik tiems vartotojams, kurie turi prieigą prie jos, atsižvelgiant į jų saugos vaidmenį. Ji taip pat bus prieinama tik juridiniams subjektams, prie kurių vartotojas turi prieigą.
- **Įgalinimo data** – data, kai funkcija buvo įjungta arba bus įjungta, jei data ateityje.
- **Funkcija įtraukta** – data, kai funkcija buvo įdėta į jūsų aplinką. Ši data automatiškai įvedama, kai atnaujinate savo aplinką mėnesio išleidimo ciklais.
- **Modulis** – modulis, kurį paveikė nauja funkcija.

Pasirinkus funkciją, išsamios informacijos srityje rodoma papildoma informacija funkcijų sąrašo dešinėje. Srities viršuje matysite funkcijos pavadinimą, datą, kada funkcija buvo papildyta, modulį, kuris yra paveiktas funkcijos ir saitą **Sužinoti daugiau**. Pasirinkite šį saitą norėdami peržiūrėti funkcijos dokumentaciją. Jei dokumentacija nepasiekiama, būsite nukreipti į laikiną puslapį. Informacijos srityje taip pat yra laukas **Komentarai**, į kurį galite įtraukti savo komentarus apie funkciją.

**Funkcijų valdymo** darbo srityje taip pat yra keli skirtukai, kuriuose yra funkcijų sąrašas. 
- **Nauja** – parodo visas funkcijas, kurios buvo pridėtos po paskutinio mėnesio atnaujinimo. Jei praleidote mėnesinius naujinimus, jame bus įtrauktos visos naujos funkcijos, nuo paskutinio naujinimo. Naujausios funkcijos rodomos sąrašo viršuje. Bendras naujų funkcijų skaičius taip pat rodomas plytelėje puslapio viršuje.
- **Neįgalinta** – rodomos visos neįjungtos funkcijos. Naujausios funkcijos rodomos sąrašo viršuje. Bendras naujų funkcijų skaičius taip pat rodomas plytelėje puslapio viršuje.
- **Suplanuota** – rodo visas funkcijas, kurios suplanuotos įjungti ateityje. Funkcijos, kurios bus įjungtos anksčiausiai, bus rodomos sąrašo viršuje. Bendras naujų funkcijų skaičius taip pat rodomas plytelėje puslapio viršuje.
- **Visos** – rodo visas funkcijas. Naujausios funkcijos rodomos sąrašo viršuje.


## <a name="enable-a-feature"></a>Įgalinti funkcija

Jei funkcija neįgalinta, išsamios informacijos srityje atsiranda mygtukas **Įgalinti**. Šį mygtuką galite naudoti, jei norite įgalinti funkciją.

1. Pasirinkite norimą įgalinti funkciją, tada išsamios informacijos srityje pasirinkite **Įgalinti.**
2. Atsiranda slankiklis, kuriame galima nurodyti datą, kada turi būti suaktyvinta funkcija. Pagal numatytuosius parametrus nustatoma esama data.
3. Norėdami įgalinti funkciją, pasirinkite **Įgalinti**.

Kai kurių priemonių negalima išjungti po to, kai jas įgalinsite. Jei funkcija, kurią mėginate įgalinti, negali būti išjungta, gausite įspėjimą. Šiuo metu galite pasirinkti **Atšaukti**, norėdami atšaukti operaciją ir palikti funkciją išjungtą. Tačiau, jei pasirinksite **Įgalinti** ir įjungsite funkciją, negalėsite jos išjungti vėliau.

Kai funkcija įjungta, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad funkcija buvo įjungta arba nurodo, kada funkcija bus įjungta ateityje. Jei naudojate būsimą datą, ši funkcija bus rodoma sąraše **Suplanuota**. Šis pranešimas bus rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše. Ateityje planuojamos funkcijos bus įjungtos vidurnaktį, atliekant paketinį vykdymą pagal laiko zoną, kuri parenkama pagal sistemos datą. 

## <a name="reschedule-a-feature"></a>Iš naujo suplanuoti funkciją

Jei funkcija įgalinta, išsamios informacijos srityje atsiranda mygtukas **Perplanuoti**. Šį mygtuką galite naudoti, jei norite pakeisti **Įgalinimo data**.

1. Pasirinkite suplanuotą funkciją, kurią norite perplanuoti, tada išsamios informacijos srityje pasirinkite **Perplanuoti.**
2. Atsiranda slankiklis, kuriame galima nurodyti datą, kada turi būti suaktyvinta funkcija. 
3. Pasirinkite **Įgalinti**, jei norite perplanuoti priemonę **Išjungti**, kad atšauktumėte planą.

## <a name="disable-a-feature"></a>Funkcijos išjungimas

Jei funkcija jau įgalinta, išsamios informacijos srityje atsiranda mygtukas **Išjungti**. Šį mygtuką galite naudoti, jei norite išjungti funkciją. Mygtukas **Išjungti** neveikia, jei funkcija negali būti išjungta ją įjungus.

- Pasirinkite norimą išjungti funkciją, tada išsamios informacijos srityje pasirinkite **Išjungti.**

- Funkcija išjungiama, o data išvaloma.

Kai funkcija išjungta, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad ši funkcija dar neįgalinta ir bus rodoma sąraše **Neįgalinta**. Pranešimas bus rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše.

## <a name="features-that-must-be-enabled"></a>Funkcijos, kurias reikia įjungti

Gali būti pristatyta svarbi funkcija, kurią būtina įjungti automatiškai, kai naujinate. Ji bus įgalinta automatiškai, kai ateis **Įgalinimo data**. Informacijos srityje po **Sužinokite daugiau** pasirodys pranešimas. Šis pranešimas nurodo, kad funkcija buvo įgalinta arba bus automatiškai įgalinta, kai ateis **Įgalinimo data**. Jis bus rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše.

## <a name="assigning-roles"></a>Vaidmenų priskyrimas

**Funkcijų valdymo** darbo sritį gali atidaryti sistemos administratoriai ir vartotojai, kuriems priskirtas funkcijų tvarkymo arba funkcijų peržiūros vaidmuo, kuris buvo sukurti siekiant palaikyti funkcijos valdymo patirtį. Funkcijų tvarkymo vaidmens vartotojai gali įjungti arba išjungti bet kokią funkciją. Jie taip pat gali atnaujinti funkcijos komentarų sekciją. Vartotojai, esantys funkcijos peržiūros vaidmenyje, gali tik peržiūrėti darbo sritį **Funkcijų valdymas**. Jie negali įjungti arba išjungti funkcijų.

Funkcijų tvarkymo vaidmuo ir funkcijų peržiūros vaidmuo neperrašo esamos saugos, kurią turi vartotojas. Vaidmenys kontroliuoja tik prieigą prie funkcijų įgalinimo. Jie nesuteikia prieigos prie pačios funkcijos.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Funkcijų valdymo naudojimas, siekiant įgalinti ISV funkcijas arba pasirinktines funkcijas

Funkcijų valdymo procesas šiuo metu negalimas ISV priemonėms arba pasirinktinėms funkcijoms. Mes pridedame papildomų funkcijų, siekdami pagerinti priemonių valdymą ir, kai šie patobulinimai yra baigti, mes suteiksime funkcijų valdymo galimybę visoms funkcijoms ir pateiksime konkrečias instrukcijas, kaip atnaujinti savo funkciją, kad ją galėtumėte naudoti.

## <a name="feature-management-and-flighting"></a>Funkcijų valdymas ir versijos

Funkcija valdymas leidžia jums kontroliuoti funkcijas, kurios siunčiamos kiekviename leidime. Versijos leidžia „Microsoft“ komandoms paleisti funkcijas ribotam klientų skaičiui, kad funkcijos galėtų būti išbandytos ir patikrintos nepakenkiant visiems klientams. Funkcijų valdymas nekontroliuoja funkcijų versijų.
