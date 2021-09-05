---
title: Vertinimo modelių nustatymas
description: Šioje procedūroje parodoma, kaip kurti naują ilgalaikio turto knygą ir susieti ją su ilgalaikio turto grupe.
author: moaamer
ms.date: 08/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46c26e5fad3c5c60d87c2fea2b29043c69b82b5d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344663"
---
# <a name="set-up-value-models"></a>Vertinimo modelių nustatymas

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]


Šioje procedūroje parodoma, kaip kurti naują ilgalaikio turto knygą ir susieti ją su ilgalaikio turto grupe. Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.

## <a name="create-a-book"></a>Knygos kūrimas
1. Pasirinkite Ilgalaikis turtas > Sąranka > Knygos.
2. Spustelėkite Naujas.
3. Lauke Knyga įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
    * Pasirinkus Skaičiuoti nusidėvėjimą, susijusi knyga bus įtraukta į nusidėvėjimo pasiūlymus. Jei parinktis nepasirinkta, turto knyga nebus automatiškai nudėvima.  
5. Lauke Skaičiuoti nusidėvėjimą pasirinkite Taip.
6. Lauke Nusidėvėjimo šablonas įveskite arba pasirinkite reikšmę.
    * Alternatyvus nusidėvėjimo šablonas taip pat vadinamas nusidėvėjimo perjungimo metodu. Į šį šabloną nusidėvėjimo pasiūlymas persijungs, kai alternatyvus šablonas apskaičiuos nusidėvėjimo sumą, kuri yra lygi numatytajam nusidėvėjimo šablonui arba už jį didesnė.  
    * Visiško nusidėvėjimo šablonas naudojamas neįprastas atvejais papildomai skaičiuojant turto nusidėvėjimą. Pavyzdžiui, galite tai naudoti norėdami įrašyti nusidėvėjimą įvykus gamtos katastrofai.  
    * Pasirinkus Kurti nusidėvėjimo koregavimus su pagrindo koregavimais, nusidėvėjimo koregavimai bus automatiškai sukurti atnaujinus turto vertę. Jei parinktis nepasirinkta, atnaujinta turto vertė turės įtakos tik tolimesniems nusidėvėjimo skaičiavimams.  
7. Lauke Kurti nusidėvėjimo koregavimus su pagrindo koregavimais pasirinkite Taip.
    * Pagal numatytuosius parametrus ilgalaikio turto knygos operacijos bus registruojamos DK. Galite išjungti knygos registravimo DK funkciją, nustatydami lauką Registruoti DK į parinktį Ne. Knygos, kurios neregistruojamos DK, paprastai naudojamos mokesčių registravimo tikslais. Taip suteikiama daugiau lankstumo naikinant ankstesnes turto knygos operacijas, nes jos nebuvo perkeltos į DK.  
    * Pagal numatytuosius parametrus registravimo sluoksnis nustatomas į parinktį Dabartinis sluoksnis, jei knyga registruojama DK, arba į parinktį Nė vienas, jei knyga neregistruojama DK. Jei reikia, kad šios knygos operacijos būtų registruojamos į kitą sluoksnį, atnaujinkite registravimo sluoksnį.  
8. Lauke Kalendorius įveskite arba pasirinkite reikšmę.
    * Išvestinių knygų operacijos bus registruojamos kitose knygose tuo pačiu metu. Galite kurti operacijas naudodami pagrindinę knygą – tada registravimo metu tikslios operacijų kopijos užregistruojamos išvestinėse knygose. Išvestinės knygos operacijos nėra perskaičiuojamos, todėl jos neturėtų būti naudojamos atliekant nusidėvėjimo operacijas.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Knygos susiejimas su ilgalaikio turto grupe
1. Spustelėkite Ilgalaikio turto grupės.
2. Lauke Ilgalaikio turto grupė įveskite arba pasirinkite reikšmę.
3. Lauke Dėvėjimo laikas įveskite skaičių.

  - Nuvertėjimo laikotarpiai yra apskaičiuojami po tarnavimo laiko turto įvesties.  
  - Mokesčių tvarkymo tikslais galite pagal poreikį nustatyti nusidėvėjimo konvenciją.
  - Ilgalaikio turto, kuris susietas su nuoma, vertė dėmeos laiko lauke bus nepaisoma mažesnio nei nuomos sąlygos turto knygoje arba turto **naudojimo laikotarpis**. Jei **nuosavybės perdavimo** laukas yra nustatytas į **Taip** uomos knygoje, gyvavimo laiko lauke nurodyta **Tarnavimo vertės** laukas bus naudingas turto naudojimo laikotarpis.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
