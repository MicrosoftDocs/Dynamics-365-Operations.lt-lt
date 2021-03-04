---
title: Siuntimių ir krovinio kūrimo trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami krovinio kūrimu ir siuntimu „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645337"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Siuntimių ir krovinio kūrimo trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami krovinio kūrimu ir siuntimu „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Gaunu tolesnį klaidos pranešimą: „Negalite sukurti krovinio eilutės šiam užsakymo eilutei, nes joje esantys inventoriaus matmenys negalioja...“

### <a name="issue-description"></a>Problemos aprašas

Gaunate tolesnį klaidos pranešimą bandydami išleisti grąžinimo prekybos užsakymą į sandėlį.

> Gaunu tolesnį klaidos pranešimą: „Negalite sukurti krovinio eilutės šiam užsakymo eilutei, nes joje esantys inventoriaus matmenys negalioja. Neegalite susieti inventoriaus matmenų, kurios yra nustatytos po vietos matmenimis rezervacijos hierarchijoje. Pašalinkite negaliojančius matmenis iš prekybos eilutės.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Deja, produktas nepalaiko krovinio apdorojimo prekybos grąžinimo procese. Dėl to, negalite išleisti grąžinimo prekybos užsakymo į sandėlį.

Prekybos užsakymo perlaidose, negalite nurodyti inventoriaus matmenų, kurie yra žemiau **Vietos** matmenų rezervacijos hierarchijoje. Išsprendimas skirtas pašalinti negaliojančius matmenis iš prekybos eilutės.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Gaunu tolesnį klaidos pranešimą: „Viena iš eilučių jau yra krovinyje. Negali išleisti į sandėlį.“

### <a name="issue-description"></a>Problemos aprašas

Jei rankiniu būdu sukuriate krovinius arba jei nustatote procesą taip, kad kroviniai jau sukuriami prieš prekybos užsakymo eilutės objektą, prielaida yra tokia, kad tolesnis išleidimas bus atliktas rankiniu būdu ir kad maršrutas bei kainos iš krovinio bus naudojamos.

Kitu galimu scenarijumi, bandote atlikti automatinį paleidimą į sandėlį, tačiau bangos procesui nepavyko sukurti darbą. Dėl to, atviras siuntimas ar krovinys vis dar yra sukurtas. Šis atviras siuntimas arba krovinys tuomet užblikuoja vėlesnius bandymus automatiškai paleisti užsakymą iki tol, kol panaikinsite atvirą siuntimą ar krovinį, arba rankiniu būdu iš naujo apdorosite bangą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Galite išleisti iš prekybos užsakymo puslapio ar automatinis paleidimas gali būti atliktas iš išleidimo prekybos užsakymo puslapio tik jei nėra jokio krovinio prieš išleidimą į sandėlį. Krovinys bus sukuriamas automatiniu būdu po bangos apdorojimo.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Gaunu tolesnį klaidos pranešimą: „Pristatymo važtaraščio koregavimas negali būti apdorojamas. Pristatymo važtaraštyje yra tik prekės, kurias veikia sandėlio valdymo procesai, nes jų nepalaiko pristatymo važtarščio koregavimas."

### <a name="issue-description"></a>Problemos aprašas

Po to, kai publikuojate pristatymo važtaraštį, nebegalite jo atšaukti, nes **Atšaukimo** mygtukas yra neprieinamas. Taip pat, negali koreguoti pristatymo važtaraščio. Jei bandote, gausite šį klaidos pranešimą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Siekiant tinkamai publikuoti pakavimo kvitus prekėms, kurios įjungtos papildomama sandėlio valdymui (WMS), privalote publikuoti iš krovinio, o ne tiesiogiai iš užsakymo.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Kaip galiu sukurti darbą iš išvesties krovinių, o ne bangų?

### <a name="issue-description"></a>Problemos aprašas

Pateikiamas vienas iš būdų pakartotinai sukurti šią problemą.

1. Sukurkite išvesties krovinį naudodami prekybos užsakymą ar perdavimo užsakymą.
2. Išleiskite krovinį į sandėlį.
3. Atkreipkite dėmesį, kad dar nebuvo sukurtas joks paėmimo darbas.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Jei darbas turi būti sukurtas nedelsiant, kai krovinys paleiždiamas, turite atitinkamai sukonfigūruoti bangos šabloną. Bangos šablone, nustatykite tolesnes parinktis į *Taip*:

- Automatiškai kurti bangą
- Apdoroti bangą išleidžiant ją į sandėlį
- Automatizuoti bangos išleidimą

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Negaliu išleisti dalinio siųsto krovinio.

### <a name="issue-description"></a>Problemos aprašas

Negalite išleisti dalinio siųsto krovinio į sandėlį. Jums atliekant išleidimą į sandėlį, rodomas pranešimas „Veiksmas užbaigtas“, bet nieko nevyksta ir likusiam kiekiui nėra sukuriamas joks darbas. Ši problema atsitinka jums naudojant transportavimo krovinio funkciją ir kai yra nebaigta rezervacija.

### <a name="issue-resolution"></a>Problemos paaiškinimas

[KB problema 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Dalinai siunčiami kroviniai gali būti iš naujo suplanuojami bangai arba pakartotinai apdorojami") yra ištaisyta [versijoje 10.0.15](../get-started/whats-new-scm-10-0-15.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]