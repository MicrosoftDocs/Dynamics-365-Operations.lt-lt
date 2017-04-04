---
title: "Tiekėjo dalinės sumos mokėjimai"
description: "Kartais tiekėjui galite atlikti mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma. Šiame straipsnyje aprašomos įvairios parinktys šiai situacijai spręsti. Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Tiekėjo dalinės sumos mokėjimai

Kartais tiekėjui galite atlikti mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma. Šiame straipsnyje aprašomos įvairios parinktys šiai situacijai spręsti. Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų. 

<a name="cash-discount-amounts"></a>Mokėjimo nuolaidos sumos
---------------------

Tiekėjas gali jums suteikti mokėjimo nuolaidą apmokant SF iki termino pabaigos. Pavyzdžiui, įvedate sąskaitą faktūrą 100,00 sumai, kurioje nurodyta 2 % mokėjimo nuolaida, jei SF apmokama per 10 dienų. Galutinis terminas yra 30 dienų. Jei mokėjimo pasiūlymą naudoja mokėjimo nuolaida kaip kriterijų pasirinkdami sąskaitos faktūros, ir pasiūlymas yra paleisti arba iki mokėjimo nuolaidos data, SF pasirinktas mokėjimo, o mokėjimo sukuriamas 98.00. Nuolaida gali būti išnuomoti už vienkartinį mokėjimą, kuris buvo sukurtas rankiniu būdu.

## <a name="partial-payments-with-cash-discounts"></a>Daliniai mokėjimai taikant mokėjimo nuolaidas
Kai atliekate dalinį mokėjimą, galite planuoti atlikti papildomą dalinį mokėjimą, kad visiškai sudengtumėte SF. Imtis dėl dalinio mokėjimo nuolaida, turite nustatyti į ** apskaičiuoti mokėjimo nuolaidas dėl dalinio mokėjimo ** galimybę **taip** ant to **sąskaita mokėtinų sumų parametrai** puslapis. 

Pavyzdžiui, galite gauti 2 % mokėjimo nuolaidą, jei SF apmokama per 10 dienų nuo jo išdavimo. Užregistruota 100,00 sumos sąskaita faktūra. Jei atliksite mokėjimą su Sage 49.00 per 10 dienų, įvedus debetas, su Sage 49.00 mokėjimo žurnalą. Kai nustatote dalinis apmokėjimas į **Settle atviros operacijos** puslapyje, **1,00** pasirodo, **mokėjimo nuolaidos suma imtis** srityje. 

> [!NOTE] 
> Jei įvedate dalinis apmokėjimas ir palikti visas SF suma, **sudengtina suma** srityje, į **mokėjimo nuolaidos suma imtis** laukas yra automatiškai perskaičiuojama registruojant operacijas.

## <a name="credit-notes-with-cash-discounts"></a>Kredito pažymos su mokėjimo nuolaidomis
Galite grąžinti kai kurias prekes, įtrauktas į SF, ir gauti kredito pažymą. Jei mokėjimo nuolaida pritaikyta originaliai SF, galite atimti nuolaidos vertę ir gauti teisingos sumos grąžinimą. Jei į ** apskaičiuoti mokėjimo nuolaidas kredito pažymoms ** parinktis nustatyta **taip** ant, **sudaro mokėtinų sumų parametrai** puslapyje, nuolaida apskaičiuojama automatiškai kredito pažymos. 

Pavyzdžiui, galite gauti 2 % mokėjimo nuolaidą, jei SF apmokama per 10 dienų nuo jo išdavimo. Užregistruota 100,00 sumos SF. Jei galite grąžinti prekes ir gauti kredito pažymą, kredito pažymą galite įvesti visą sumą iš sąskaitos faktūros originalas, 100,00, kartu su 2 procentų mokėjimo nuolaidos, kurios taip pat yra nustatytos grąžinimo pažyma.  Kai peržiūrite kredito pažymos apie į **atsiskaitymams** puslapyje, **98.00** pasirodo, **sudengtina suma** srityje, ir **-2.00** pasirodo, **mokėjimo nuolaidos suma** lauko. Nuolaidos suma registruojama mokėjimo nuolaidos sąskaitoje.

## <a name="overpaymentunderpayment-amounts"></a>Permokėjimo / neprimokėjimo sumos
Galite atlikti dalinį mokėjimą, kai suma, kurią vis dar reikia sudengti, yra labai maža. Pvz., tiekėjo SF suma yra 1 000,00 ir jūs sumokate 999,90. Jei likusi suma yra mažesnė už sumą, kuri nurodyta prie permokėjimų arba neprimokėjimų puslapyje **Mokėtinų sumų parametrai**, skirtumas automatiškai užregistruojamas permokėjimų / neprimokėjimų DK sąskaitoje.


