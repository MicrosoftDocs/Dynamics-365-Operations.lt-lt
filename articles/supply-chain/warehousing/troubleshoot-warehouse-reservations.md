---
title: Sandėlio valdymo rezervacijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1ea23059d56ebf387a95a1378e2a3cd47556d5f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993878"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Sandėlio valdymo rezervacijų trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Gaunu tolesnį klaidos pranešimą: „Rezervacijų negalima panaikinti dėl to, kad sukurtas darbas remiasi rezervacijomis.“

### <a name="issue-description"></a>Problemos aprašas

Negalite atrezrervuoti inventoriaus pardavimo eilutėje, nes eilutei yra atvertas darbas.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Nustatykite, ar atviro pakavimo grupės darbas yra skirtas siekiant perkelti prekę iš pakavimo stoties į kitą stotį (tokią kaip *Baydoor*). Peržiūrėkite įrašus **Darbo sukūrimo istorijos žurnale** ir **Išsamios darbo informacijos** puslapiuose siekiant nustatyti, kas fiziškai rezervuoja inventorių ir tada užbaikite bei panaikinkite darbą siekiant atlaisvinti rezervaciją.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Gaunu tolesnį klaidos pranešimą: „Inventoriaus kiekis -%1 negali būti atnaujintas dėl nepakankamų inventoriaus perlaidų prekei %2...."

### <a name="issue-description"></a>Problemos aprašas

Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis. Štai visas klaidos pranešimo tekstas:

> Inventoriaus kiekis -%1 negali būti naujinamas dėl nepakankamų inventoriaus perlaidų prekei %2 su matmenimis Dydis=%3, Spalva=%4, Prieda=%5, Saitas=%6, Sandėlis=%7, Vieta=%8, Inventoriaus būsena=Prieinamas, Licensijos plokštelė=%9, Palaido kiekio numeris=%10 ataskaitos ID %11 partijos ID %12.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį. Pavyzdžiui, šios perlaidos gali atverti kiekio užsakymus, inventoriaus blokavimo įrašus ar išvesties užsakymus.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Gaunu tolesnį klaidos pranešimą: „Fiziškai turima...negalima rezervuoti dėl to, kad tik 0,00 yra prieinama inventoriuje."

### <a name="issue-description"></a>Problemos aprašas

Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis. Štai visas klaidos pranešimo tekstas:

> Fiziškai turima Saitas=%1, Sandėlis=%2, Inventoriaus būsena=Prieinama, Palaido kiekio numeris=%3, Savininkas=%4: %5 negalima rezervuoti, nes tik 0.00 yra prieinama inventoriuje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Šią klaidą greičiausiai sukelia atviras darbas. Pabaikite darbą arba gaukite nesukūrę darbo. Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį. Pavyzdžiui, šios perlaidos gali būti atviri kiekio užsakymai, inventoriaus blokavimo įrašai ar išvesties užsakymai.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Gaunu tolesnį klaidos pranešimą: „Tam kad būtų priskirtos prie bangos, krovinio eilutės turi nurodyti matmenis virš vietos. Norėdami priskirti šiuos matmenis, rezervuokite ir iš naujo sukurkite krovinio eilutę."

### <a name="issue-description"></a>Problemos aprašas

Jums naudojant prekę, kuri turi „palaidas kiekis aukščiau“ rezervacijos hierarchiją (su **Palaido kiekio** matmenimis esančiais *virš* tos **Vietos** matmenų), **Paleista į sandėlį** komanda **Įkelti suplanuotą darbo slenkstį** puslapyje daliniam kiekiui neveikia. Gaunate šį klaidos pranešimą ir joks darbas nesukuriamas daliniam kiekiui.

Nepaisant to, jei naudojant prekę, kuri turi „palaidas kiekis žemiau“ rezervacijos hierarchiją (su **Palaido kiekio** matmenimis esančiais *žemiau* tos **Vietos** matmenų), ygalite atlaisvinti krovinį nuo **Įkelti suplanuotą darbo slenkstį** puslapyje daliniam kiekiui neveikia.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. Jei padedate matmenis virš **Vietos** matmens rezervacijos hierarchijoje, jis turi būti nurodytas prieš paleidžiant į sandėlį. „Microsoft“ įvertino šią klaidą ir nustatė, kad jos funkcijos apribojimai išleidžiami į sandėlį iš krovinio planavimo darbo slenksčio. Daliniai kiekiai negali būti išleisti, jei vieneri ar keli matmenys virš **Vietos** nenurodyti.

Dėl išsamesnės informacijos, žr. [Lanksti sandėlio lygmens matmenų rezervacijos politika](flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]