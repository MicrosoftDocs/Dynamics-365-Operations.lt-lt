---
title: "Kliento dalinės sumos mokėjimai"
description: "Kartais klientai atlieka mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma. Šiame straipsnyje aprašytos įvairios pasirinktys šiai situacijai tvarkyti. Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6e4fac197e75b80609486be7ea7c50c4b48beeb7
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="customer-payments-for-a-partial-amount"></a>Kliento dalinės sumos mokėjimai

[!include[banner](../includes/banner.md)]


Kartais klientai atlieka mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma. Šiame straipsnyje aprašytos įvairios pasirinktys šiai situacijai tvarkyti. Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų.

<a name="partial-payment-with-no-discount"></a>Dalinis mokėjimas be nuolaidos
--------------------------------

Klientai gali sumokėti dalį sumos, nes tiesiog neturi pakankamai grynųjų pinigų visai sąskaitos faktūros sumai apmokėti arba kilus konfliktui dėl prekės, už kurią išrašyta sąskaita faktūra. Tokiu atveju sąskaitą faktūrą galima iš dalies sudengti atliekant mokėjimą. Sąskaita faktūra liks atidaryta ir joje bus rodomas balansas.

## <a name="discount-amounts"></a>Nuolaidos sumos
Galima suteikti klientams mokėjimo nuolaidą apmokant sąskaitą faktūrą iki termino pabaigos. Pavyzdžiui, įvedate sąskaitą faktūrą 100,00 sumai, kurioje nurodyta 2 % mokėjimo nuolaida, jei sąskaita faktūra apmokama per 10 dienų. Galutinis terminas yra 30 dienų. Jei gaunate 98,00 mokėjimą per 10 dienų, įvedate 98,00 sumos mokėjimą. Tada, kai sąskaita faktūra bus pažymėta sudengti, mokėjimo nuolaida bus pritaikoma automatiškai.

## <a name="partial-payments-with-cash-discounts"></a>Daliniai mokėjimai taikant mokėjimo nuolaidas
Kai klientai atlieka dalinį mokėjimą, jie gali planuoti atlikti papildomą dalinį mokėjimą, kad visiškai sudengtų sąskaitą faktūrą. Norėdami taikyti daliniam mokėjimui mokėjimo nuolaidą, puslapyje **Gautinų sumų parametrai** turite nustatyti parinkties **Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas** reikšmę **Taip**. 

Pavyzdžiui, galite pasiūlyti 2 % mokėjimo nuolaida, jei sąskaita faktūra apmokama per 10 dienų nuo jo išdavimo. Užregistruota 100,00 sumos sąskaita faktūra. Jei gaunate 49,00 mokėjimą per 10 dienų, mokėjimų žurnale įvedate 49,00 sumos kreditą. Kai sudengsite dalinį mokėjimą puslapyje **Sudengti operacijas**, lauke **Taikytina mokėjimo nuolaidos suma** bus rodoma **1,00**. Nuolaidos suma registruojama mokėjimo nuolaidos sąskaitoje. 

> [!NOTE] 
> Pastaba. Jei įvesite dalinį mokėjimą ir lauke **Sudengtina suma** paliksite visą sąskaitos faktūros sumą, laukas **Taikytina mokėjimo nuolaidos suma** bus perskaičiuotas automatiškai, kai registruosite operacijas.

## <a name="credit-notes-with-discounts"></a>Kredito pažymos su nuolaidomis
Jei klientai grąžins kai kurias prekes, įtrauktas į sąskaitą faktūrą, galite išduoti kredito pažymą. Jei pradinei sąskaitai faktūrai buvo pritaikyta mokėjimo nuolaida, klientui taikoma kredito pažyma turėtų būti grynoji mokėjimo nuolaidos, pritaikytos klientui, suma. Jei puslapyje **Gautinų sumų parametrai** nustatyta parinkties **Skaičiuoti kredito pažymų mokėjimo nuolaidas** reikšmė **Taip**, kredito pažymos nuolaida apskaičiuojama automatiškai. 

Pavyzdžiui, pasiūlėte mokėjimo sąlygas, pagal kurias numatoma 2 % nuolaida, jei sąskaita faktūra apmokama per 10 dienų nuo jo išdavimo. Buvo užregistruota sąskaita faktūra 100,00 sumai, ir klientui buvo pritaikyta mokėjimo nuolaida. Jei klientas grąžins prekes ir jūs išduosite kredito pažymą, galėsite įvesti 100,00 sumos kredito pažymą. Peržiūrint kredito pažymą puslapyje **Sudengti atidarytas operacijas**, lauke **Sudengtina suma** bus rodoma **98,00**, o lauke **Mokėjimo nuolaidos suma** bus rodoma **–2,00**. Nuolaidos suma registruojama mokėjimo nuolaidos sąskaitoje.

## <a name="overpaymentunderpayment-amounts"></a>Permokėjimo / neprimokėjimo sumos
Klientams atliekant mokėjimą, gali būti labai maža suma, kurią vis tiek reikia sudengti. Pavyzdžiui, pateikėte klientui sąskaitą faktūrą 1 000,00 sumai, o klientas sumokėjo 999,90. Jei likusi suma yra mažesnė už sumą, kuri nurodyta prie permokėjimų arba neprimokėjimų puslapyje **Gautinų sumų parametrai**, skirtumas automatiškai užregistruojamas permokėjimų / neprimokėjimų DK sąskaitoje.

## <a name="full-settlement"></a>Visiškas sudengimas
Klientai gali atlikti dalinį mokėjimą, jei likusi suma nebus mokama, tačiau yra didesnė nei neprimokėjimo suma, nurodyta puslapyje **Mokėtinų sumų parametrai**. Jei norite pažymėti sąskaitą faktūrą kaip visiškai sudengtą, galite naudoti parinktį **Visiškas sudengimas**, esančią puslapyje **Sudengti operaciją**. (Galite įgalinti visiško sudengimo funkciją naudodami konfigūracijos raktą.) Pavyzdžiui, užregistruota sąskaita faktūra 1 000,00 sumai, o klientas sumoka 990,00. Jūs sutarėte, kad klientui nereikia mokėti likusios 10,00 sumos. Pažymėję sąskaitą faktūrą sudengti, galite taip pat pažymėti parinktį **Visiškas sudengimas**. Tada sąskaita faktūra bus laikoma visiškai sudengta. 10,00 skirtumas registruojamas mokėjimo nuolaidos sąskaitoje kaip papildoma mokėjimo nuolaidos suma.


Daugiau informacijos žr. [Mokėti kliento mokėjimus](tasks/deposit-customer-payments.md).

