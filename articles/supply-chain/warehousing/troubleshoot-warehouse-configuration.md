---
title: Trikties šalinimo sandėlio konfigūravimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti konfigūruodami „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.openlocfilehash: 60873cb76ee08dd5a4bd4ed8b38cc4845b500453bf34bd10708b105448b58c9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735092"
---
# <a name="troubleshoot-warehouse-configuration"></a>Trikties šalinimo sandėlio konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti konfigūruodami „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Gaunu tolesnį klaidos pranešimą: „Licencijos lentelė ar vieta negalioja"

### <a name="issue-description"></a>Problemos aprašas

Gausite šį klaidos pranešimą jums nuskaitant licencijos lentelės ID ar vietą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Įsitikinkite, kad licencijos lentelės ID nėra rezervuotas kieno nors kito. Ši problema įprastai atsirasdavo, kai reikšmė, kurią vartotojas nuskaitė sandėlio valdymo mobiliųjų įrenginių programėlėje, buvo tiek galiojanti vieta, tiek galiojantis licencijos lentelės ID. Nepaisant to, ši problema buvo išspręsta 10.0.11 versijoje.

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

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>Negaliu naudoti sandėlio valdymo mobiliųjų įrenginių programėlės, kad atlikčiau dalinį paėmimą.

### <a name="issue-description"></a>Problemos aprašas

Prekybos ir perdavimo užsakymams negalite praleisti prekių ir atlikti dalinio paėmimo.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Puslapyje **Mobilaus įrenginio meniu prekės** kiekvienai meniu prekei, kuri yra nustatyta siekiant apdoroti prekybos užsakymus ar perdavimo užsakymus, nustatykite **Leisti atskyrimo darbo** parinktį **Bendri** „FastTab“ į *Taip*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Kaip galiu atlikti inventoriaus būsenos keitimą daliniam kiekio darbui?

### <a name="issue-description"></a>Problemos aprašas

Norite atlikti inventoriaus būsenos keitimą daliniam bendram kiekiui.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Norėdami leisti darbuotojams atlikti šį keitimą, galite sukurti meniu prekę sandėlio valdymo mobiliųjų įrenginių programėlei. Puslapyje **Mobilaus įrenginio meniu prekės** sukurkite (ar redaguokite) meniu prekę, kuri turi tolesnius nustatymus:

- **Režimas:** *Darbas*
- **Naudoti sukurtą darbą:** *Ne*
- **Darbo sukūrimo procesas:** *Judėjimas*
- **Rodyti inventoriaus būseną:** *Taip*

Galite nustatyti kitus laukelius puslapyje, kaip būtina.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Vietos profilio rampos valdymo profilis nekliudo atsargų tipų susimaišymui.

### <a name="issue-description"></a>Problemos aprašas

Jūs naudojate *siuntos konsolidacijų strategijas*. Nustatėte *rampos valdymo profilį* kaip *vietos profilį*, tačiau sukūrus darbą, atsargų tipai susimaišo galutinėje vietoje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Rampos valdymo profiliai reikalauja iš anksto suskaidyti darbą. Kitaip tariant, rampos valdymo profilis tikisi, kad darbo antraštėje nebus kelių padėjimo vietų.

Norint, kad rampos valdymo profilis efektyviai valdytų atsargų maišymą, reikia nustatyti darbo antraštės lūžį.

Šiame pavyzdyje mūsų rampos valdymo profilis sukonfigūruotas taip, kad **Atsargų tipai, kurių negalima maišyti** būtų nustatytas į *Siuntos ID*, o mes jam nustatysime darbo antraštės lūžį:

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Pasirinkite **Darbo užsakymo tipą** redagavimui (pavyzdžiui, *Pirkimo užsakymai*).
1. Pasirinkite darbo šabloną redagavimui.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Atidarykite **Rikiavimo** skirtuką ir pridėkite eilutę su šiais parametrais:
    - **Lentelė** - *Laikinos darbo operacijos*
    - **Išvestinė lentelė** - *Laikinos darbo operacijos*
    - **Laukas** - *Siuntos ID*
1. Pasirinkite **Gerai**.
1. Grįžtate į **Darbo šablonų** puslapį. Veiksmų juostoje pasirinkite **Darbo antraštės lūžiai**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Pasirinkite žymės langelį, susietą su **Lauko pavadinimo** *Siuntos ID*.
1. Veiksmų srityje pasirinkite **Įrašyti**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
