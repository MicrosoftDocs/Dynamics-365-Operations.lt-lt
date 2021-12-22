---
title: Vertinimo modelių nustatymas
description: Šioje procedūroje parodoma, kaip kurti naują ilgalaikio turto knygą ir susieti ją su ilgalaikio turto grupe.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be3b5578bd6509859c36f6a50ea9730e9ef1780e
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890717"
---
# <a name="set-up-value-models"></a>Vertinimo modelių nustatymas

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Šioje procedūroje parodoma, kaip kurti naują ilgalaikio turto knygą ir susieti ją su ilgalaikio turto grupe.

## <a name="create-a-book"></a>Knygos kūrimas
1. Eiti į **ilgalaikio \> turto nustatymo \> knygas**.
2. Pasirinkite **Nauja**.
3. Lauke **Knyga** įveskite vertę.
4. Lauke **Aprašas** įveskite reikšmę.
5. Nustatykite parinktį **Skaičiuoti** nusidėvėjimą kaip **Taip**.

    Jei **pasirinktis** Skaičiuoti nusidėvėjimą nustatyta kaip **Taip**, susieta turto knyga bus įtraukta į nusidėvėjimo pasiūlymus. Jei nustatyta **Ne**, turto knygos nusidėvėjimas nebus automatiškai nustatomas.

6. Lauke **Nusidėvėjimo** profilis įveskite arba pasirinkite vertę.

    * Alternatyvus nusidėvėjimo šablonas taip pat vadinamas nusidėvėjimo perjungimo metodu. Į šį šabloną nusidėvėjimo pasiūlymas persijungs, kai alternatyvus šablonas apskaičiuos nusidėvėjimo sumą, kuri yra lygi numatytajam nusidėvėjimo šablonui arba už jį didesnė.
    * Visiško nusidėvėjimo šablonas naudojamas neįprastas atvejais papildomai skaičiuojant turto nusidėvėjimą. Pavyzdžiui, galite tai naudoti norėdami įrašyti nusidėvėjimą įvykus gamtos katastrofai.
    * Jei pasirinksite Kurti **nusidėvėjimo koregavimus su pagrindo** koregavimais, atnaujinus turto vertę, nusidėvėjimo koregavimai bus sukuriami automatiškai. Kitu atveju atnaujinta turto vertė turės įtakos tik būsimiems nusidėvėjimo skaičiavimams.

7. Nustatykite parinktį **Kurti nusidėvėjimo koregavimus su pagrindo** koregavimais kaip **Taip**.

    * Pagal numatytuosius nustatymus ilgalaikio turto knygos operacijos registruojamos DK. Tačiau galite uždrausti knygos registravimą į DK, nustatydami **pasirinktį Registruoti DK** kaip **Ne**. Dk neregistruotos knygos paprastai naudojamos mokesčių ataskaitoms. Ši pasirinktis suteikia jums daugiau lankstumo panaikinti retrospektyvias turto knygos operacijas, nes operacijos nebuvo fiksuotos DK.
    * Pagal numatytuosius nustatymus, laukas Registravimo sluoksnis nustatomas kaip Dabartinis sluoksnis, jei knyga užregistruojama DK, o Nėra, jei **knyga** **·** **neužregistruota** DK. Atnaujinti lauko Registravimo sluoksnis **vertę**, jei šios knygos operacijos turėtų būti registruojamos skirtinguose sluoksniuose.

8. Apskaičiuoti teigiamą nusidėvėjimą.

    * Numatyta, kad **pasirinktis Skaičiuoti teigiamą** nusidėvėjimą nustatyta kaip **Ne**. Šis parametras nurodo, kad nusidėvėjimas kredituos pasirinktą turto knygą. Be to, pasirinktys Leisti aukštesnę nei įsigijimo kaina balansinę vertę ir Leisti neigiamą balansinę vertę yra nustatytos kaip Ne, todėl parametrai gali **būti** keičiami **·** **atskirai**. 
    * Norėdami apskaičiuoti teigiamą nusidėvėjimą, nustatykite **parinktį Skaičiuoti teigiamą** nusidėvėjimą kaip **Taip**. Šis parametras nurodo, kad nusidėvėjimas debetuos ilgalaikio turto knygą. Kai parinktis Skaičiuoti teigiamą nusidėvėjimą nustatyta kaip Taip, leisti aukštesnę nei įsigijimo kainos balansinę vertę ir leisti neigiamą balansinę vertę pasirinktys automatiškai bus nustatytos kaip Taip ir **jos** **bus** **·** **·** **užrakintos**. Šis užraktas padeda užtikrinti, kad teigiamas nusidėvėjimas bus taikomas tik ilgalaikiam turtui, įsigytam su neigiama balansine verte (kreditu). 

10. Lauke **Kalendorius** įveskite arba pasirinkite vertę.

    Išvestinių knygų operacijos bus registruojamos kitose knygose tuo pačiu metu. Galite kurti operacijas naudodami pagrindinę knygą – tada registravimo metu tikslios operacijų kopijos užregistruojamos išvestinėse knygose. Išvestinės knygos operacijos nėra perskaičiuojamos, todėl jos neturėtų būti naudojamos atliekant nusidėvėjimo operacijas.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Knygos susiejimas su ilgalaikio turto grupe

1. Pasirinkite **ilgalaikio turto** grupes.
2. Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę.
3. Lauke **Gyvavimo** laikas įveskite skaičių.

    * Nuvertėjimo laikotarpiai yra apskaičiuojami po tarnavimo laiko turto įvesties.
    * Mokesčių tvarkymo tikslais galite pagal poreikį nustatyti nusidėvėjimo konvenciją.
    * Ilgalaikio turto, susieto su nuoma, dėmeos laiko lauko vertės bus nepaisoma mažesniu nei nuomos sąlygos turto knygoje ir turto naudojimo **laikotarpiu**. Jei **nuosavybės perdavimo pasirinktis nustatyta kaip Taip nuomos knygoje, gyvavimo laiko lauko vertė visada bus** naudingas turto **naudojimo** **laikotarpis**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
