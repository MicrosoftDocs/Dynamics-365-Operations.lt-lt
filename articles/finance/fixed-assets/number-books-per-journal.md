---
title: Vieno žurnalo knygų skaičius
description: Šioje temoje aprašomas ryšys tarp žurnalų ir turto knygų kuriant ilgalaikio turto įsigijimo arba nusidėvėjimo pasiūlymą vykdant paketinę užduotį. Galite nurodyti maksimalų knygų, įtrauktų į kiekvieną įsigijimą ir dėl nusidėvėjimo, skaičių.
author: moaamer
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e948b4353d0216f1e09019a98319e343bd535861
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822038"
---
# <a name="number-of-books-per-journal"></a>Vieno žurnalo knygų skaičius

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas ryšys tarp žurnalų ir turto knygų kuriant ilgalaikio turto įsigijimo arba nusidėvėjimo pasiūlymą vykdant paketinę užduotį. Galite nurodyti maksimalų visų pirkimo ir nusidėvėjimo knygų skaičių, naudojant laukus, esančius puslapio **Ilgalaikio turto parametrai** skirtuko **Bendra** skiltyje **Vieno žurnalo knygų skaičius** (**Ilgalaikis turtas \> Sąranka \> Ilgalaikio turto parametrai**). Šie laukai leidžia paskirstyti turto knygų, skirtų pirkimo žurnalui ir nusidėvėjimo žurnalui, skaičių.

Įsigijimo pasiūlymo numatytoji vertė yra bent 10 000 knygų. Nusidėvėjimo pasiūlymo numatytoji vertė yra bent 2000 knygų.

Pavyzdžiui, jei yra 4000 ilgalaikio turto ir dvi knygos yra susietos su kiekvienu turtu, viena knyga bus užregistruota dabartiniame sluoksnyje, o kita knyga bus užregistruota mokesčių sluoksnyje. Jei įsigysite 4000 ilgalaikio turto vienetų per paketinį vykdymą, paketinė užduotis, kuri sukuria vieną ilgalaikio turto įsigijimo žurnalą, sudarys 4000 turto knygas.

> [!NOTE]
> Sukurtas žurnalas bus naudojamas, kol baigiama paketinė užduotis.
>
> Išvestinė knyga neįtraukta į didžiausią knygų, skirtų žurnalui, skaičių.

Norėdami vykdyti nusidėvėjimą tam pačiam įsigyto turto rinkiniui, galite naudoti paketinį apdorojimą. Pavyzdžiui, paketinė užduotis sukuria du nusidėvėjimo žurnalus, kurių kiekvienas susideda iš 2000 turto knygų. Pirmajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 1 iki 2000. Antrajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 2001 iki 4000.

Paketinio vykdymo užduotis neįtraukia uždarytų knygų. Pavyzdžiui, atliekant nusidėvėjimo paketinę užduotį, uždaromos 10 iš pirmųjų 2000 knygų. Tokiu atveju pirmajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 1 iki 2011. Antrajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 2012 iki 4000.

> [!NOTE]
> Jei turite ilgalaikio turto PVM su skirtingais skyrikliais (pvz., – arba /) ir sukuriate ilgalaikio turto operacijas paketinėse užduotyse, turite paleisti atskirą paketinę užduotį kiekvienam skyriklio tipui. Sistema negali apdoroti skirtingų skyriklių toje pačioje paketinėje užduotyje.

Knygų skaičiaus limitas yra pritaikytas, jei tame pačiame žurnale nėra dubliuotų turto ID. Tačiau, jei turto ID yra toks pats kaip knygos ID, galima viršyti žurnalo žurnalų skaičių, kad turto ID liktų tame pačiame žurnale.

Pavyzdžiui, yra 5001 ilgalaikio turto ID, trys knygos yra susietos su kiekvienu ilgalaikio turto ID, o kiekviena turto knyga užregistruojama tame pačiame registravimo lygmenyje. Vykdote nebegaliojimą tris mėnesius iš eilės be santraukos.  Nusidėvėjimo žurnalas bus sukurtas naudojant paketines užduotis, o sistema sukurs septynis žurnalus, kuriuose yra 667 ilgalaikio turto ID ir trys knygos kiekvienam ilgalaikio turto ID. Rezultatas bus 2001 knyga. Todėl per tris mėnesius bus 6003 žurnalo eilutės, kad būtų išlaikyti tie patys turto ID tame pačiame žurnale. Sistema taip pat sukurs po vieną žurnalą, kuriame yra 332 ilgalaikio turto ID ir trys knygos kiekvienam ilgalaikio turto identifikatoriui. Per tris mėnesius bus 2988 eilutės.

> [!NOTE] 
> Jei **Santrauko nebegaliojimo** parametras yra įjungtas jums kuriant nebegaliojimo pasiūlymą, tuomet vertė **Knygų skaičius žurnale - Nebegaliojimo pasiūlymas** laukelyje neturi jokio poveikio. Šiuo atveju, knygų skaičius žurnale yra 6000, o tai vidaus nustatytas apribojimas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
