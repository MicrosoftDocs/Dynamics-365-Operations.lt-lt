---
title: Pagrindinio planavimo trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su pagrindiniu planavimu.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1492854b7d2da480942800e378be9d2bb60bb1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645070"
---
# <a name="troubleshoot-master-planning"></a>Pagrindinio planavimo trikčių šalinimas

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su pagrindiniu planavimu.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Medžiagų važtaraščio sprogimas elgiasi kitaip patvirtintiems gamybos užsakymams ir apskaičiuotiems gamybos užsakymams, kai darbai sukuriami rankiniu būdu.

### <a name="issue-description"></a>Problemos aprašas

Patvirtinus gamybos užsakymą, prekės nėra sprogdinamos, kai sprogdinate medžiagų aprašą (BOM). Nepaisant to, jums rankiniu būdu sukuriant darbo užsakymą ir tada apskaičiuojant gamybos užsakymą, prekės yra sprogdinamos.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Sistema dirba kaip tikėtasi. Sprogimas, įvykstantis kai gamybos užsakymas yra patvirtinamas, rodys į suplanuotą užsakymą, bet bus nerodoma, jog suplanuotas užsakymas šiuo metu ir šiuo atveju yra patvirtintas. Nepaisant to, jei gakybos užsakymas buvo apskaičiuotas, sprogimas yra paskatinamas iš išleisto gamybos užsakymo, kai nėra jokio suplanuoto užsakymo.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Vėlinimo vertė nėra naujinama, kai iš naujo suplanuoju suplanuotą užsakymą.

Norėdami naujinti suplanuotų užsakymų pavėlinimą, atverkite **Naujo suplanavimo** teksto laukelį suplanuotam užsakymui. „FastTab“ **Sprogimas** įsitikinkite, kad **Atlikti sprogimą po pakartotinio suplanavimo** parinktis yra nustatyta į *Taip*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Gamybos naujas suplanavimas neapima saugos maržų, kurios yra nustatytos prekės apimtyje fiksuotam tiekimui.

### <a name="issue-description"></a>Problemos aprašas

Pagrindinis planavimas apima saugos maržas. Nepaisant to, saugos maržos ignoruojamos planuojant prekybos užsakymus, kai jie yra suplanuojami iš anksto.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Į maržas atsižvelgiama tik pagrindinio planavimo metu, o ne rankiniu būdu planuojant. Maržos skirtos veikti kaip buferis planavimo etapo metu tam, kad suteiktų šiokią tokią esamo proceso „maržą“.

Norėdami gauti norimą rezultatą, galite pašalinti maržą. Maršrutas turi būti tuomet atnaujintas taip, kad apimtų norimą laiką (pavyzdžiui, laukimo laiką). Tiek pagrindinis, tiek ir rankinis planavimas turi tuomet duoti tą patį rezultatą.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Suplanuoti užsakymai sukuriami net jei turime prekes atsargoje ir prekybos užsakymai jiems jau egzistuoja.

Galite ištaisyti šią problemą didindami **Teigiamų dienų** vertę atitinkamoms grupėms **Apimties grupės** puslapyje. Dėl šio pakeitimo sistema nustatys, ar turimas inventorius gali būti naudojamas paklausai. Tuomet naujas suplanuotas užsakymas nebus sukuriamas atsargų prekėms.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Pagrindinis planavimas nesilaiko pajėgumo apribojimų ir yra suplanuotas daugiau nei prieinamas pajėgumas.

### <a name="issue-description"></a>Problemos aprašas

Jums naudojant operacijos planavimą, kai yra baigtinis pajėgumas ir kai maršrutas nurodo reikalavimų mišinį tiek išteklių grupei, tiek ir atskiriems resursams, yra nedidelė per didelio rezervavimo tikimybė dėl būdo, kuriuo algoritmas patvirtina pajėgumo konfliktus. Per didelis rezervavimas gali įvykti jums naudojant padedančius įrankius siekiant vykdyti pagrindinį planavimą. Labiausiai tikėtina, kad jis įvyks, jei yra per daug darbų turinčių atitinkamą trumpą vykdymo laiką.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Jei reikia, kad nebūtų per didelio rezervavimo veikimo planavimui, galite atlikti vienos linijos pagrindinio planavimo dalies naują planavimą įjungdami **Tikslus baigtas pajėgumas operacijos planavimui** parinktį puslapyje **Pagrindinio planavimo parametrai**. Ši parinktis nėra prieinama pagal nutylėjimą. Privalote rankiniu būdu įtraukti ją į puslapį naudodami suasmenintas funkcijas. Jums naudojant šią parinktį, planavimas bus vykdomas lėčiau dėl paralelaus apdorojimo trūkumo.

## <a name="planned-orders-take-a-long-time-to-update"></a>Suplanuoti užsakymai užtrunka ilgai, kai yra naujinami.

### <a name="issue-description"></a>Problemos aprašas

Naujinant reikalavimo kiekį ir (arba) pristatymo datą suplanuotame užsakyme, dažniausiai užtrunka mažiausiai 30 sekundžių, kad vienas užsakymas įrašytų naujinimą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ši žinoma problema su inkoproporuotu pagrindinio planavimo varikliu. Jį sukelia jį remiantis automatinis sprogimas per BOM struktūrą redagavimo metu. Ši problema pažymėta „Planning Optimization“, kurioje planavimo įrankis gali būti naujinti ir tvirtinti atitinkamus užsakymus ir kai norima, paskatinti planavimo vykdymą siekiant atnaujinti suplanuotus užsakymus po ja esančiai BOM struktūrai.

Vienas būdas skirtas pagerinti vykdymą su inkorporuotu pagrindinio planavimo varikliu yra tokia:

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Pasirinkite kelią.
1. Išplėskite **Laiko tvora dienomis** „FastTab“.
1. Nustatykite **Sprogimą** į *Taip* ir nustatykite tolesnio laukelio nustatymą į 0 (taip).

> [!NOTE]
> Toks bus ribojimas sprogimų laikotarpiui, kurie įvyko per šį pagrindinį planavimą ir vienos dienos metu.
