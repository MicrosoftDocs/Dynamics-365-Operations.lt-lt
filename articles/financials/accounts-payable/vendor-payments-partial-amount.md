---
title: "Tiekėjo dalinės sumos mokėjimai"
description: "Kartais tiekėjui galite atlikti mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma. Šiame straipsnyje aprašomos įvairios parinktys šiai situacijai spręsti. Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cc8e2864343b5e9fee8eaf058a51360d15e425a
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-payments-for-a-partial-amount"></a>Tiekėjo dalinės sumos mokėjimai

[!include[banner](../includes/banner.md)]


Kartais tiekėjui galite atlikti mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma. Šiame straipsnyje aprašomos įvairios parinktys šiai situacijai spręsti. Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų. 

<a name="cash-discount-amounts"></a>Mokėjimo nuolaidos sumos
---------------------

Tiekėjas gali jums suteikti mokėjimo nuolaidą apmokant SF iki termino pabaigos. Pavyzdžiui, įvedate sąskaitą faktūrą 100,00 sumai, kurioje nurodyta 2 % mokėjimo nuolaida, jei SF apmokama per 10 dienų. Galutinis terminas yra 30 dienų. Jei mokėjimo pasiūlyme sąskaitos faktūros pasirinkimo kriterijumi laikoma mokėjimo nuolaida, o pasiūlymas bus įvykdytas mokėjimo nuolaidos dieną ar prieš ją, bus pasirinkta apmokėti pagal šią sąskaitą faktūrą ir bus sukurta 98,00 siekianti mokėjimo suma. Galima pritaikyti mokėjimo nuolaidą ir neautomatiškai sukurtam vienkartiniam mokėjimui.

## <a name="partial-payments-with-cash-discounts"></a>Daliniai mokėjimai taikant mokėjimo nuolaidas
Kai atliekate dalinį mokėjimą, galite planuoti atlikti papildomą dalinį mokėjimą, kad visiškai sudengtumėte SF. Norėdami daliniam mokėjimui taikyti mokėjimo nuolaidą, puslapyje **Mokėtinų sumų parametrai** turite nustatyti parinkties **Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas** reikšmę **Taip**. 

Pavyzdžiui, galite gauti 2 % mokėjimo nuolaidą, jei SF apmokama per 10 dienų nuo jo išdavimo. Užregistruota 100,00 sumos sąskaita faktūra. Jei per 10 dienų sumokėsite 49,00, mokėjimų žurnale įvedate 49,00 siekiantį debetą. Kai sudengsite dalinį mokėjimą puslapyje **Sudengti atidarytas operacijas**, lauke **Taikytina mokėjimo nuolaidos suma** bus rodoma **1,00**. 

> [!NOTE] 
> Pastaba. Jei įvesite dalinį mokėjimą ir lauke **Sudengtina suma** paliksite visą sąskaitos faktūros sumą, laukas **Taikytina mokėjimo nuolaidos suma** bus perskaičiuotas automatiškai, kai registruosite operacijas.

## <a name="credit-notes-with-cash-discounts"></a>Kredito pažymos su mokėjimo nuolaidomis
Galite grąžinti kai kurias prekes, įtrauktas į SF, ir gauti kredito pažymą. Jei mokėjimo nuolaida pritaikyta originaliai SF, galite atimti nuolaidos vertę ir gauti teisingos sumos grąžinimą. Jei puslapyje **Mokėtinų sumų parametrai** nustatyta parinkties **Skaičiuoti kredito pažymų mokėjimo nuolaidas** reikšmė **Taip**, automatiškai apskaičiuojama kredito pažymos nuolaida. 

Pavyzdžiui, galite gauti 2 % mokėjimo nuolaidą, jei SF apmokama per 10 dienų nuo jo išdavimo. Užregistruota 100,00 sumos SF. Jei grąžinsite prekes ir gausite kredito pažymą, pagal kredito pažymą galėsite įvesti visą pradinės SF 100,00 siekiančią sumą bei kredito pažymoje taip pat nustatytą 2 % mokėjimo nuolaidą.  Peržiūrint kredito pažymą puslapyje **Sudengti operacijas**, lauke **Sudengtina suma** bus rodoma **98,00**, o lauke **Mokėjimo nuolaidos suma** bus rodoma **–2,00**. Nuolaidos suma registruojama mokėjimo nuolaidos sąskaitoje.

## <a name="overpaymentunderpayment-amounts"></a>Permokėjimo / neprimokėjimo sumos
Galite atlikti dalinį mokėjimą, kai suma, kurią vis dar reikia sudengti, yra labai maža. Pvz., tiekėjo SF suma yra 1 000,00 ir jūs sumokate 999,90. Jei likusi suma yra mažesnė už sumą, kuri nurodyta prie permokėjimų arba neprimokėjimų puslapyje **Mokėtinų sumų parametrai**, skirtumas automatiškai užregistruojamas permokėjimų / neprimokėjimų DK sąskaitoje.


Daugiau informacijos žr. [Tiekėjo mokėjimų apžvalga](../cash-bank-management/tasks/vendor-payment-overview.md).

