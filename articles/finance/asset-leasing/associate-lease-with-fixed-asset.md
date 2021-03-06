---
title: Ilgalaikio turto susiejimas su nuomomis
description: Temoje paaiškinama, kaip susieti esamą ilgalaikį turtą su nauja nuoma.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881353"
---
# <a name="associate-fixed-assets-with-leases"></a>Ilgalaikio turto susiejimas su nuomomis

[!include [banner](../includes/banner.md)]

Temoje paaiškinama, kaip susieti esamą ilgalaikį turtą su nauja nuoma. Kai susiejate ilgalaikį turtą su nuoma, ilgalaikio turto įsigijimo kaina bus naudojimo teise valdomo turto pirminio pripažinimo vertė.

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

> [!NOTE]
> Jei susiejate ilgalaikį turtą su nuoma, mygtukai **Turto nusidėvėjimas** ir **Nuomos nuvertėjimas** modulyje Turto nuoma yra išjungti. Ilgalaikio turto nusidėvėjimo ir nuomos nuvertėjimo operacijas galite peržiūrėti dalyje Ilgalaikis turtas. Mygtukas **Turto operacijos**, kuriuo atidaroma užklausos forma, taip pat išjungtas. Taip pat galite atidaryti **ilgalaikio turto operacijų** užklausos formą dalyje Ilgalaikis turtas.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
