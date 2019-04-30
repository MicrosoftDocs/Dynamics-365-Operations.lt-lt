---
title: Ataskaitų pagal įstatymą dėl prieinamos sveikatos priežiūros (ACA) generavimas
description: Funkcijos pasiekiamos siekiant padėti darbdaviams, kuriems reikia sekti formose 1095-B ir 1095-C pateiktą informaciją, pagrindžiant Darbdavio įgaliojimų dalį pagal įstatymą dėl prieinamos sveikatos priežiūros. Atkreipkite dėmesį, kad ši funkcija įjungta tik juridiniams subjektams Jungtinėse Amerikos Valstijose.
author: andreabichsel
manager: AnnBe
ms.date: 12/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: f03e414683465e7275d6c48a843306abefbacaf0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "859464"
---
# <a name="generate-affordable-care-act-aca-reports"></a>Ataskaitų pagal įstatymą dėl prieinamos sveikatos priežiūros (ACA) generavimas

[!include [banner](includes/banner.md)]

Funkcijos pasiekiamos siekiant padėti darbdaviams, kuriems reikia sekti formose 1095-B ir 1095-C pateiktą informaciją, pagrindžiant **Darbdavio įgaliojimų** dalį pagal įstatymą dėl prieinamos sveikatos priežiūros. Atkreipkite dėmesį, kad ši funkcija įjungta tik juridiniams subjektams Jungtinėse Amerikos Valstijose.

## <a name="getting-started"></a>Darbo pradžia
Pradėdami sekti informaciją, kurią reikia pranešti formose 1095-B ir 1095-C, pirmiausia turite sukurti vieną ar daugiau prieinamos sveikatos priežiūros draudimo grupių. Šios sveikatos priežiūros draudimo grupės bus naudojamos siekiant nurodyti darbuotojui pateiktą draudimo pasiūlymą, darbuotojams tenkančią mažiausios mėnesinės įmokos dalį (jei išlaidos viršija federalinę skurdo ribą), taip pat Saugų prieglobstį, kurį naudoja darbdavys, jei taikoma. Naudodami įstatymo dėl prieinamos sveikatos priežiūros grupes, galėsite tvarkyti šių laukų informaciją neliesdami kiekvieno darbuotojo įrašo, kai sąlygos yra tos pačios. Be to, prieinamos sveikatos priežiūros draudimo grupes galima lengvai priskirti vienam ar daugiau darbuotojų, naudojant puslapyje pateiktą funkciją Masinis priskyrimas.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Kelių draudimo grupės versijų išlaikymas
Galite išlaikyti kelias draudimo grupės versijas, o tai leidžia atlikti pakeitimus ir išlaikyti grupės informaciją aktualią nekuriant naujos grupės ir iš naujo nepriskiriant darbuotojų prie jos, kai kas nors jūsų organizacijoje arba siūlomose išmokose pasikeičia. 

Sukūrę reikalingas prieinamos sveikatos priežiūros draudimo grupes, galite pasirinkti masiškai priskirti grupes darbuotojams, naudodami puslapyje pateiktą funkciją **Masinis priskyrimas**, arba galite eiti į kiekvieno darbuotojo įrašą ir nurodyti, ar tam darbuotojui reikia sekti ir pranešti ACA informaciją, taip pat priskirti darbuotoją prieinamos sveikatos priežiūros draudimo grupei.

Jei darbuotojo prieinamos sveikatos priežiūros draudimo informacijos sekti ir pranešti nereikia, pavyzdžiui, jei darbuotojas dirba ne visą darbo dieną, lauke **Nurodyti draudimą** gali būti nustatyta reikšmė Ne. Nors kiekvieną darbuotoją, kurio ACA informaciją reikia sekti, būtina priskirti prieinamos sveikatos priežiūros draudimo grupei, vis dar galite pakeisti parinktis **Draudimo pasiūlymas**, **Darbuotojui tenkanti išlaidų dalis** ir **Saugus prieglobstis** bet kurį mėnesį arba mėnesius, kuriais gali reikėti kitokių reikšmių, nei įvestos prieinamos sveikatos priežiūros draudimo grupėje.

Norėdami įvesti bet kokios prieinamos sveikatos priežiūros draudimo grupės reikšmių išimtis, spustelėkite saitą Prieinamos sveikatos priežiūros draudimas, kurį rasite skirtuko Įdarbinimas skyriaus Papildoma informacija puslapyje Darbininko informacija.

## <a name="reporting-health-care-coverage"></a>Sveikatos priežiūros draudimo ataskaitos
Be sekimo, koks sveikatos draudimas pasiūlytas visą darbo dieną dirbančiam darbuotojui (jei apskritai pasiūlytas), ar darbdavys siūlo darbdavio remiamą savarankišką sveikatos draudimą, į kurį įtrauktas darbuotojas (nepaisant, ar darbuotojas dirba visą darbo dieną ar ne visą), 1095-C formoje reikia pateikti papildomą informaciją. Kiekvienas darbuotojas (įskaitant priklausomuosius), kuriems taikomi darbdavio remiami išmokų planai, turi būti įtrauktas į tų mėnesių, kuriais planai buvo taikomi, ataskaitą. 

Galite nurodyti, ar turi būti pranešta apie kiekvieną Išmokų planą, pasirinkdami žymės langelį **Reikia perduoti ACA**.

Be to, jei darbuotojai pasirinko išmokos taikymą savo priklausomiesiems, puslapyje Prižiūrėti išmokas galite nurodyti datas, kada kiekvieno darbuotojo priklausomiesiems buvo taikomos išmokos. Kad nurodytumėte, kad priklausomajam taikoma išmoka, pasirinkite mygtuką Redaguoti veiksmų srityje Priklausomųjų „FastTab“.

Puslapyje **Priklausomųjų draudimo datų tvarkytuvas** galite nurodyti datas, kada priklausomajam buvo taikoma išmoka. Šiame puslapyje įvedus datas, puslapyje **Prižiūrėti išmokas** bus automatiškai pasirinktas žymės langelis **Apdraustas**.

## <a name="generate-1095b-and-1095c-forms"></a>Generuoti 1095B ir 1095C formas
Taip pat galite generuoti 109-B ir 1095-C formas iš produkto ir jas paskirstyti kiekvienam darbuotojui. Elektroniniu būdu generuojamus 1095-C ir atitinkamos 1094-C siunčiamus failus, kuriuos galima naudoti siunčiant į IRS, taip pat galima generuoti ir iš sistemos.  

Generuodami 1095-C formą, įveskite atitinkamus mokestinius metus ir nurodykite, ar socialinio draudimo numeriai turėtų būti paslėpti. Jei spausdinate 1095-C formas, skirtas daugiau nei 500 darbuotojų, gausite daugiau nei vieną PDF failą. Rekomenduojama padidinti į **maksimalų failo dydį** lange **Dokumentų valdymo parametrai** iki 150 MB.

## <a name="viewing-information"></a>Informacijos peržiūra
Norėdami peržiūrėti, kurie darbuotojai buvo priskirti kiekvienai draudimo grupei, kurių darbuotojų nereikia įtraukti į ataskaitą ir kurie darbuotojai nepriskirti, galite naudoti puslapį **Darbininko prieinamos sveikatos priežiūros draudimas**.

Jei numatytųjų prieinamos sveikatos priežiūros draudimo grupės reikšmių nepaisoma, prie pakeistos reikšmės atsiras žvaigždutė. Jei visų 12 mėnesių reikšmės sutampa ir jų nebuvo nepaisoma, reikšmė bus išspausdinta stulpelyje **Visi 12 mėnesių**.

Taip pat galite naudoti užklausos langą, kad suprastumėte, kurie darbuotojai buvo pažymėti kaip Nereikia perduoti ACA, o tai reiškia, kad jums nereikia sekti, ar jiems buvo pasiūlytas draudimas, o metų pabaigoje jiems nereikės išduoti 1095-C. Pasirinkdami **Nereikia perduoti ACA** lauke **Filtruoti pagal**, galite generuoti sąrašą visų darbuotojų, kurie buvo pažymėti kaip neturintys gauti 1095-C.

Be darbuotojų, kurių atveju nereikia perduoti ACA, peržiūros taip pat galite peržiūrėti darbuotojus, kurie nepriskirti (laukas **ACA ataskaitos draudimas** yra tuščias) arba priskirti prieinamos sveikatos priežiūros draudimo grupei, kuri metais, pasirinktais lauke **Metai**, nebegalioja.

Galite eksportuoti darbuotojų sąrašus, kurie sugeneruoti naudojant filtravimo parinktis, į „Excel“.

Jei jums reikia pranešti apie apdraustus asmenis, nes kaip darbdavys teikiate savarankišką draudimą, taip pat galite peržiūrėti priklausomuosius, kuriems taikomi išmokų planai ir kurie buvo pažymėti kaip **Reikia perduoti ACA**, veiksmų srities juostelėje pasirinkdami veiksmą Peržiūrėti priklausomojo draudimą.

**Pastaba:** užklausos lange bus rodomos tik tos išmokos, kurių planas buvo pažymėtas kaip **Reikia perduoti ACA**.
