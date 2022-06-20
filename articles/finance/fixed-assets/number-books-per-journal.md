---
title: Vieno žurnalo knygų skaičius
description: Šiame straipsnyje aprašomas ryšys tarp žurnalų ir turto knygų, kai naudodami paketinę užduotį kuriate ilgalaikio turto įsigijimą arba nusidėvėjimo pasiūlymą. Galite nurodyti maksimalų knygų, įtrauktų į kiekvieną įsigijimą ir dėl nusidėvėjimo, skaičių.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2dbd50963cf13f00e09b82e884cd8ebc0b67d424
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883335"
---
# <a name="number-of-books-per-journal"></a>Vieno žurnalo knygų skaičius

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas ryšys tarp žurnalų ir turto knygų, kai naudodami paketinę užduotį kuriate ilgalaikio turto įsigijimą arba nusidėvėjimo pasiūlymą. Galite nurodyti maksimalų visų pirkimo ir nusidėvėjimo knygų skaičių, naudojant laukus, esančius puslapio **Ilgalaikio turto parametrai** skirtuko **Bendra** skiltyje **Vieno žurnalo knygų skaičius** (**Ilgalaikis turtas \> Sąranka \> Ilgalaikio turto parametrai**). Šie laukai leidžia paskirstyti turto knygų, skirtų pirkimo žurnalui ir nusidėvėjimo žurnalui, skaičių.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
