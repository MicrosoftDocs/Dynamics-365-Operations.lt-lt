---
title: Paėmimo ir pakavimo trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti paimdami ir pakuodami „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.openlocfilehash: 1a54fa9dc21fb1691d74905a1215f4dfea31f136
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828135"
---
# <a name="troubleshoot-picking-and-packing"></a>Paėmimo ir pakavimo trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti paimdami ir pakuodami „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Gaunu tolesnį klaidos pranešimą: „Matmenų vietos negali būti paliktos tuščios, jei matmenų serijinis numeris yra nustatytas“.

### <a name="issue-description"></a>Problemos aprašas

Gausite šį klaidos pranešimą, jei sukursite perdavimo užsakymą serijinei prekei naudodami sandėlį, kuris yra įjungtas papildomam sandėlio valdymui (WMS) ir tuomet pabaigę darbą, bandysite patvirtinti siuntimą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

**Numatytoji gavimo vieta** laukelis yra tuščias ir skirtas perdavimo sandėliui „iš“ sandėlio. Norėdami ištaisyti šią problemą, nurodykite nustatytąją gavimo vietą perdavimo sandėlyje. Įsitikinkite, kad šį vieta yra licencijos lentelės valdoma.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Gaunu tolesnį klaidos pranešimą: „Licencijos lentelė negalioja."

### <a name="issue-description"></a>Problemos aprašas

Jūs gausite šį klaidos pranešimą sandėlio valdymo mobiliųjų įrenginių programėlėje, kai nuskaitysite licencijos lentelės ID.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Įsitikinkite, kad licencijos lentelės ID yra licencijos lentelės lentelėje ir kad prekės ir kiekiai licencijos lentelėje yra prieinami (kitaip tariant, jie nėra blokuojami).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Gaunu tolesnį klaidos pranšimą: „Laukelio krovinio svoris'(=-%1) gali būti sudarytas tik iš teigiamų skaičių. Naujinimas buvo atšauktas."

### <a name="issue-description"></a>Problemos aprašas

Gaunate šį klaidos pranešimą, jei yra atviras darbas jums apdorojant darbą iš pakavimo vietų į parengimo vietas arba iš parengimo vietų į dokų vietas.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Norėdami ištaisyti šią problemą, eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenų bazė \> Nuoseklumos tikrinimas** ir vykdykite procesą **Sandėlio krovinio svorio nuoseklumo tikrinimas**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Gaunu tolesnį klaidos pranešimą: „Kiekis negalioja %1 vienetui."

### <a name="issue-description"></a>Problemos aprašas

Gaunate šį klaidos pranešimą bandydami atlikti *atskyrimo paėmimo* darbą keliuose palaiduose kiekiuose.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Sandėlio darbuotojas privalo naudoti *Trumpo paėmimo* procesą sandėlio valdymo mobiliųjų įrenginių programėlėje. Jei bandote paimti keletą palaidų kiekių iš vienos vietos, galite taip pat naudoti parinktį **Visas** programoje.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Negaliu perkelti inventoriaus į vietą, kurią valdo licencijos plokštelė.

### <a name="issue-description"></a>Problemos aprašas

Negalite sumažinti paimto kiekio krovinyje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ankstesnėse versijose, negalite sumažinti paimto krovinio kiekio. Nepaisant to, galite dabar nepaimti licencijso lentelės valdomos vietos. Privalote nurodyti **Vietos** vertę ir **Licencijos lentelės** vertę apkrovos eilutei **Sumažinti paimtą kiekį** puslapyje.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Ar galiu spausdinti pristatymo važtaraštį ar sandėlio pakavimo lapą?

### <a name="issue-description"></a>Problemos aprašas

Norite spausdinti pristatymo važtaraštį ar sandėlio pakavimo lapą ar saito **Darbo audito šablono eilutės naujinimas** puslapyje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Jums spausdinant dokumentą naudodami Spausdinimo valdymo nustatymus, norint apriboti tikslą (saito/sandėlio) per Spausdinimo valdymą, o ne pasirinkimą **Redaguoti spausdinimo nustatymus** puslapyje **Darbo audito šablono eilutės naujinimas**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Negaliu atšaukti paėmimo kvito po to, kai jis publikuotas prekybos užsakyme.

### <a name="issue-description"></a>Problemos aprašas

Paimant ir siunčiant procesus įjungtus WMS, negalite atšaukti pakavimo kvitą po to, kai jis publikuotas iš pardavimo užsakyme.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Siekiant tinkamai publikuoti pakavimo kvitus prekėms, kurios bus įjungtos WMS, publikavimas turi vykti iš krovinio, o ne iš užsakymo. „Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Bendrrai, prekybos užsakymas, kuris buvo paimtas ir siųstas per sandėlio valdymo procesus gali būti supakuotas naujinant kvitą iš krovinio ar siuntimo ir prekybos užsakymo dokumente. Nepaisant to, jei pakuojate kvito naujinimą prekybos užsakyme iš pardavimo užsakymo dokumento, pakavimo dokumento grąžinimas negali būti atliekamas iš krovinio ar prekybos užsakymo. Dėl to, rekomenduojame jums naudoti pakavimo kvito publikavimą iš krovinio. Tokiu atveju, grąžinimas turi būti atliekamas, kai įjungtas krovinys.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Gaunu tolesnį klaidos pranešimą: „Nepakankamas darbas gali būti randamas klasteryje."

### <a name="issue-description"></a>Problemos aprašas

Jums naudojant *Sistemos kreipiamą klasterio paėmimo* procesą, jei konfigūruojate klasterio profilį, kai pavyzdžiui, 10 padėčių gali būti paimtos, procesas veikia kaip planuota, kai yra pakankamai darbo siekiant paimti iki 10 padėčių. Nepaisant to, jei yra tik aštuonios padėtys paėmimiui, gaunate šį klaidos pranešimą, nes nesama pakankamai darbo vienam klasteriui.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Siekiant ištaisyti šią problemą, redaguokite klasterio profilį ir nustatykite **Įjungti padėtis** parinktį į *Ne*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]