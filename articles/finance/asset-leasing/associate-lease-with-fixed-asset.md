---
title: Ilgalaikio turto susiejimas su nuomomis
description: Šiame straipsnyje paaiškinama, kaip susieti esamą ilgalaikį turtą su nauja nuoma.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5cc341008d25da544ec35d5660b5ff0b38f2287b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895115"
---
# <a name="associate-fixed-assets-with-leases"></a>Ilgalaikio turto susiejimas su nuomomis

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje paaiškinama, kaip susieti esamą ilgalaikį turtą su nauja nuoma. Kai susiejate ilgalaikį turtą su nuoma, ilgalaikio turto įsigijimo kaina bus naudojimo teise valdomo turto pirminio pripažinimo vertė.

Kad galėtumėte susieti ilgalaikį turtą su nuoma, turite sukurti ilgalaikio turto įrašą dalyje Ilgalaikis turtas. Tada puslapyje **Nuomos suvestinė** turite sukurti nuomą ir susieti turtą su ta nuoma.

1. Įtraukite nuomą, atlikdami veiksmus, nurodytus temoje [Nuomų įtraukimas arba kopijavimas](add-lease.md). Puslapio **Nuomos įtraukimas** lauke **Ilgalaikio turto numeris** pasirinkite turtą, kuris dar nebuvo įsigytas.
2. Pasirinkite **Knygos** ir patvirtinkite mokėjimo grafiką.
3. Pasirinkite **Pradinis pripažinimas**.
4. Pasirinkite **Turto nuomos žurnalas**.

    Nuomos pradinio pripažinimo žurnalo įrašas debetuoja ilgalaikio turto sumą, kuri paprastai debetuojama į naudojimo teise valdomo turto sąskaitą.

    Dabar galite peržiūrėti ilgalaikio turto operacijos tipą ir knygą.

5. Pasirinkite **Žurnalo informacija**.
6. Pasirinkite **Eilutės**, norėdami peržiūrėti atskiras žurnalo įrašo eilutes.
7. Pasirinkite žurnalo eilutę, kurioje yra turtas, tada pasirinkite skirtuką **Ilgalaikis turtas**.

    Skirtuke **Ilgalaikis turtas** rodomas operacijos tipas ir knyga. Numatyta, kad laukas **Operacijos tipas** nustatytas kaip **Įsigijimas**, o laukas **Knyga** nustatytas kaip dabartinė ilgalaikio turto knyga.

Užregistravus pradinio pripažinimo žurnalo įrašą, operacija rodoma kaip ilgalaikio turto įsigijimo operacija. Norėdami peržiūrėti operacijų lentelę, eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**, pasirinkite reikiamą turtą ir **Vertinimai**. Turėtumėte matyti, kad pradinio pripažinimo žurnalo įrašas sukūrė nurodyto ilgalaikio turto įsigijimo operaciją.

Ilgalaikį turtą dabar galima nudėvėti naudojant standartinę ilgalaikio turto nusidėvėjimo funkciją dalyje Ilgalaikis turtas. Daugiau informacijos apie nusidėvėjimą žr. [Nusidėvėjimo metodai ir konvencijos](../fixed-assets/depreciation-methods-conventions.md).

Kai nuoma yra susieta su ilgalaikiu turtu, ilgalaikio turto knygos laukas **Dėvėjimo laikas** bus atnaujintas, kad sutaptų su toliau pateikiamų kriterijų mažiausia reikšme. 

 - Turto naudingo naudojimo laikas
 - Susietoje nuomos knygoje nurodytas nuomos terminas

Jei **nuosavybės perdavimo** laukas yra nustatytas į **Taip** uomos knygoje, gyvavimo laiko lauke nurodyta **Tarnavimo vertės** laukas bus naudingas turto naudojimo laikotarpis. 
 
Kaskart pakoregavus nuomą, dėvėjimo laikas bus atnaujinamas siekiant užtikrinti, kad naudojimo teise valdomas turtas yra nusidėvėjęs per nuomos terminą taip pat kaip jis buvo nusidėvėjęs turto nuomoje.

> [!NOTE]
> Jei susiejate ilgalaikį turtą su nuoma, mygtukai **Turto nusidėvėjimas** ir **Nuomos nuvertėjimas** modulyje Turto nuoma yra išjungti. Ilgalaikio turto nusidėvėjimo ir nuomos nuvertėjimo operacijas galite peržiūrėti dalyje Ilgalaikis turtas. Mygtukas **Turto operacijos**, kuriuo atidaroma užklausos forma, taip pat išjungtas. Taip pat galite atidaryti **ilgalaikio turto operacijų** užklausos formą dalyje Ilgalaikis turtas.  

Puslapiuose **Ilgalaikis turtas** ir **Ilgalaikio turto knyga** bus rodomas su ilgalaikiu turtu susietas nuomos ID. Jeigu ilgalaikis turtas yra susietas su nuoma, puslapio **Ilgalaikis turtas** „FastTab“ **Nuomos informacija** bus rodomi nuomos ID ir nuomos aprašas. Su nuomos knygomis susietų ilgalaikio turto knygų laukuose **Nuomos ID**, **Nuomos aprašas** ir **Knygos tipas** bus rodoma pasirinktos ilgalaikio turto knygos informacija, kuri pateikiama „FastTab“ **Nuomos informacija**, siekiant nurodyti, kas yra susieta su nuomos knyga.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
