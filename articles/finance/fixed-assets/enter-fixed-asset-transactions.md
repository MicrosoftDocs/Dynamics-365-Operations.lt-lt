---
title: Ilgalaikio turto operacijų parinktys
description: Šioje temoje aprašomi galimi skirtingi metodai ilgalaikio turto operacijoms kurti.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 129f88037691096c22478e4f186667a502e394ec
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674479"
---
# <a name="fixed-asset-transaction-options"></a>Ilgalaikio turto operacijų parinktys

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aprašomi galimi skirtingi metodai ilgalaikio turto operacijoms kurti.

Galite nustatyti, kad ilgalaikis turtas būtų integruotas su mokėtinomis sumomis, gautinomis sumomis, paraiškomis ir didžiąja knyga. Taip pat galite perkelti prekes atsargų valdyme į ilgalaikį turtą, jei norite tas prekes naudoti viduje.

## <a name="accounts-payable"></a>Mokėtinos sumos
Ilgalaikio turto operacijas Galite įvesti puslapyje Žurnalo kvitas. Šį puslapį galima atidaryti iš puslapio SF žurnalas. Žurnalo kvito puslapį taip pat galite atidaryti iš SF patvirtinimo žurnalo puslapio. Korespondentinės sąskaitos tipo lauke pasirinkite Ilgalaikis turtas. Tada lauke Korespondentinė sąskaita pasirinkite ilgalaikio turto numerį. Skirtuke Ilgalaikis turtas įveskite reikšmes laukuose Operacijos tipas ir Knygos.

## <a name="accounts-receivable"></a>Gautinos sumos
Ilgalaikio turto operacijas galite įvesti puslapyje Laisvos formos SF.  Puslapyje Laisvos formos SF, SF eilučių tinklelyje pasirinkite eilutės prekę. Spustelėkite „FastTab‟ Eilutės informacija. Įveskite ilgalaikio turto numerį ir likvidavimo operacijos knygą. Laisvos formos sąskaitų faktūrų ilgalaikio turto operacijos tipas visuomet yra Likvidavimas – pardavimas.

## <a name="procurement-and-sourcing"></a>Paraiškos
Ilgalaikio turto operacijas Galite įvesti puslapyje Pirkimo užsakymas. Norėdami sukurti pirkimo užsakymą, įveskite reikalingą informaciją ir spustelėkite Gerai. Pirkimo užsakymo puslapyje spustelėkite „FastTab‟ Eilutės informacija. Tada skirtuke Ilgalaikis turtas įveskite informaciją apie ilgalaikį turtą. 

Norėdami užregistruoti esančio ilgalaikio turto įsigijimo operaciją, nurodykite ilgalaikio turto numerį, knygą ir operacijos tipą. Negalima registruoti ilgalaikio turto, jei šios informacijos nėra. Norėdami registruoti naujo ilgalaikio turto įsigijimo operaciją, pasirinkite parinktį Naujas ilgalaikis turtas? ir pasirinkite ilgalaikio turto grupę, kuriai norite priskirti naują turtą. Tačiau nebus galima nei viena iš ilgalaikio turto laukų eilučių, jei elementas bus atsargų modelių grupėje, kuriai naudojamas standartinių išlaidų atsargų modelis. Be to, parinktys, apibrėžtos puslapyje Ilgalaikio turto parametrai, nustato, ar galite registruoti įsigijimo operacijas iš pirkimo modulių. 

Kai pirkimo užsakymas arba Ilgalaikio turto atsargų žurnalas naudojami įsigyti ilgalaikiam turtui, pasikeičia atsargų reikšmė.

## <a name="general-ledger"></a>Didžioji knyga
Bet kokį ilgalaikio turto operacijos tipą galima registruoti puslapyje Bendrasis žurnalas. Taip pat galite naudoti žurnalus ilgalaikio turto operacijoms registruoti.

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Ilgalaikio turto operacijų tipų įvedimo pasirinktys


| Operacijos tipas                    | Modulis                   | Pasirinktys                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Įsigijimas, Įsigijimo koregavimas | Ilgalaikis turtas             | Ilgalaikis turtas, Atsargos į ilgalaikį turtą   |
|                                     | Didžioji knyga           | Pagrindinis žurnalas                           |
|                                     | Mokėtinos sumos         | SF žurnalas, SF patvirtinimo žurnalas |
|                                     | Paraiškos | Pirkimo užsakymas                            |
| Nusidėvėjimas                        | Ilgalaikis turtas             | Ilgalaikis turtas                              |
|                                     | Didžioji knyga           | Pagrindinis žurnalas                           |
| Likvidavimas                            | Ilgalaikis turtas             | Ilgalaikis turtas                              |
|                                     | Didžioji knyga           | Pagrindinis žurnalas                           |
|                                     | Gautinos sumos      | Laisvos formos SF                         |

Ilgalaikio turto likusių nusidėvėjimo laikotarpių reikšmė nėra atnaujinama, kai nusidėvėjimo operacijos tipo žurnalo eilutė sukuriama neautomatiškai arba importuojama naudojant duomenų objektą. Likusių laikotarpių reikšmė atnaujinama, kai nusidėvėjimo pasiūlymo procesas naudojamas žurnalo eilutei sukurti.

Norėdami daugiau informacijos žr. [Ilgalaikio turto integravimas](fixed-asset-integration.md).

Sistema neleidžia registruoti to paties laikotarpio nusidėvėjimo du kartus. Pavyzdžiui, jei du vartotojai atskirai sukuria sausio mėnesio nusidėvėjimo pasiūlymus, pirmo vartotojo nusidėvėjimas bus registruojamas pirmame žurnale. Kai antrasis vartotojas užregistruoja nusidėvėjimą antrame žurnale, sistema patikrina paskutinio nusidėvėjimo vykdymo datą ir neregistruoja to paties laikotarpio nusidėvėjimo antrą kartą.

### <a name="transactions-that-require-a-different-voucher-number"></a>Operacijos, kurioms reikia skirtingo kvito numerio

Toliau nurodytose ilgalaikio turto operacijose bus naudojami skirtingi kvitų numeriai:

- Atliekamas papildomas turto įsigijimas ir skaičiuojamas nusidėvėjimas atgaline data.
- Turtas suskaidomas.
- Įjungiamas parametras, naudojamas norint apskaičiuoti nusidėvėjimą likviduojant, po to turtas likviduojamas.
- Turto paslaugos data yra ankstesnė nei įsigijimo data. Dėl to registruojamas nusidėvėjimo koregavimas.

> [!NOTE]
> Įvesdami operacijas, įsitikinkite, kad visos operacijos taikomos tam pačiam ilgalaikiam turtui. Kvitas nebus registruojamas, jei jame bus daugiau nei vienas ilgalaikis turtas, net jei didžiosios knygos puslapio **Žurnalų pavadinimai** laukas **Naujas kvitas** nustatytas į **Tik vienas kvito numeris**. Jei į kvitą įtraukiate daugiau nei vieną ilgalaikį turtą, gausite tokį pranešimą pranešimas: „Viename kvite gali būti tik viena ilgalaikio turto operacija” ir negalėsite registruoti kvito.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
