---
title: Trikties šalinimo sandėlio konfigūravimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti konfigūruodami „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994008"
---
# <a name="troubleshoot-warehouse-configuration"></a>Trikties šalinimo sandėlio konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti konfigūruodami „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Gaunu tolesnį klaidos pranešimą: „Licencijos lentelė ar vieta negalioja"

### <a name="issue-description"></a>Problemos aprašas

Gausite šį klaidos pranešimą jums nuskaitant licencijos lentelės ID ar vietą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Įsitikinkite, kad licencijos lentelės ID nėra rezervuotas kieno nors kito. Ši klaida naudojama siekiant atlikti veiksmus, kai vertę, kurią vartotojas nuskaitė sandėlio programoje buvo galiojanti vieta ir galiojantis licencijos lentelės ID. Nepaisant to, ši problema buvo išspręsta 10.0.11 versijoje.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Gaunu tolesnį klaidos pranešimą: „Licencijos lentelė turi būti nurodyta šiai vietai"

### <a name="issue-description"></a>Problemos aprašas

Gausite šį klaidos pranešimą, jei sukursite perdavimo užsakymą naudodami sandėlį, kuris yra įjungtas papildomam sandėlio valdymui (WMS) ir tuomet pabaigę darbą, bandysite patvirtinti siuntimą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

**Numatytoji gavimo vieta** laukelis yra tuščias ir skirtas perdavimo sandėliui „iš“ sandėlio. Norėdami ištaisyti šią problemą, nurodykite nustatytąją gavimo vietą perdavimo sandėlyje. Įsitikinkite, kad šį vieta yra licencijos lentelės valdoma.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Gaunu tolesnį klaidos pranešimą: „Negalite sukurti darbo šablono eilutės inventoriaus būsenos keitimui dėl to, kad darbo tipas neglaioja. Pasirinkite kitą darbo tipą."

### <a name="issue-description"></a>Problemos aprašas

Darbo šablonui, negalite pasirinkti *Inventoriaus būsenos keitimas* stulpelyje **Darbo tipas** skyriuje **Darbo šablono išsami informacija**.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. *Inventoriaus būsenos keitimo* darbo tipas yra naudojamas sistemos procesų. Jo konfigūruoti negalima. Kadangi darbo tipų sąrašai yra fiksuoti kaip numeravimas, papildomi objektai negali būti filtruojami iš **Darbo tipo** iškrentančio meniu.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Gaunu tolesnį klaidos pranešimą: „Kiekis negalioja 1% vienetui."

### <a name="issue-description"></a>Problemos aprašas

Kiekis negalioja *ea* vienetui, kai yra paėmimo darbas turintis keletą licencijos lentelių vienoje vietoje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Patikrinkite, ar **Vieneto sekos grupės ID** ir **Vieneto pavertimų** laukeliai išleistame produkte ar produkto variante yra nustatyti tinkamai.

Atkreipkite dėmesį, kad klaidos pranešimas buvo pagerintas versijoje 10.0.15 (žr. [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Naujas klaidos pranešimas yra, „Kiekis negalioja. Tikėtina %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Vietos kryptys pardavimo užsakymo padėjimo darbe, kelių SKU parinktis nevertina kelių vietų krypčių veiksmų.

### <a name="issue-description"></a>Problemos aprašas

Krypties vietos *Pardavimo užsakymų* darbo tvarkos tipas ir *Padėjimo* darbo tipas nevertina kelių vietos krypties veiksmų, kai **Kelių SKU** parinktis pasirenkama. Tik pirmasis vietos krypties veiksmas yra vertinamas.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Nauja funkcija, *Vertinti visus veiksmus kelioms SKU vietos kryptims* buvo įtraukta į versiją 10.0.15 (žr. [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Ši funkcija vertina visus veiksmus kelioms SKU vietos kryptims. Jei jums reikia šios funkcijos, naudokite [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad ją įjungtumėte.

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>Negaliu naudoti sandėlio programos, kad atlikčiau dalinį paėmimą.

### <a name="issue-description"></a>Problemos aprašas

Prekybos ir perdavimo užsakymams negalite praleisti prekių ir atlikti dalinio paėmimo.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Puslapyje **Mobilaus įrenginio meniu prekės** kiekvienai meniu prekei, kuri yra nustatyta siekiant apdoroti prekybos užsakymus ar perdavimo užsakymus, nustatykite **Leisti atskyrimo darbo** parinktį **Bendri** „FastTab“ į *Taip*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Kaip galiu atlikti inventoriaus būsenos keitimą daliniam kiekio darbui?

### <a name="issue-description"></a>Problemos aprašas

Norite atlikti inventoriaus būsenos keitimą daliniam bendram kiekiui.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Norėdami leisti darbuotojams atlikti šį keitimą, galite sukurti meniu prekę sandėlio programai. Puslapyje **Mobilaus įrenginio meniu prekės** sukurkite (ar redaguokite) meniu prekę, kuri turi tolesnius nustatymus:

- **Režimas:** *Darbas*
- **Naudoti sukurtą darbą:** *Ne*
- **Darbo sukūrimo procesas:** *Judėjimas*
- **Rodyti inventoriaus būseną:** *Taip*

Galite nustatyti kitus laukelius puslapyje, kaip būtina.
