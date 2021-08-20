---
title: Sandėlio valdymo rezervacijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5f3a9ab907c3cb0e6b99c414a78b6878bd5353274472c54e1f5eaf1d167f046a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773110"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Sandėlio valdymo rezervacijų trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.

Informaciją temomis apie paketo ir serijos numerių registracijas rasite [Sandėlio paketo ir serijos rezervacijų hierarchijos trikčių diagnostika](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
