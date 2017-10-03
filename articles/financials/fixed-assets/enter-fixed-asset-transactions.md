---
title: "Ilgalaikio turto operacijų parinktys"
description: "Šiame straipsnyje aprašomi galimi skirtingi metodai ilgalaikio turto operacijoms kurti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 40ab6f8d7e7b7a04ec1533acf2919dea345b0804
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-transaction-options"></a>Ilgalaikio turto operacijų parinktys

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomi galimi skirtingi metodai ilgalaikio turto operacijoms kurti.

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

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Ilgalaikio turto operacijų tipų įvedimo pasirinktys


| Operacijos tipas                    | Modulis                   | Pasirinktys                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Įsigijimas, Įsigijimo koregavimas | Ilgalaikis turtas             | Ilgalaikis turtas, Atsargos į ilgalaikį turtą   |
|                                     | Didžioji knyga           | Pagrindinis žurnalas                           |
|                                     | Mokėtinos sumos         | SF žurnalas, SF patvirtinimo žurnalas |
|                                     | Paraiškos | Pirkimo užsakymas                            |
| Nusidėvėjimas                        | Ilgalaikis turtas             | Ilgalaikis turtas                              |
|                                     | DK           | Pagrindinis žurnalas                           |
| Likvidavimas                            | Ilgalaikis turtas             | Ilgalaikis turtas                              |
| ** **                               | DK           | Pagrindinis žurnalas                           |
| ** **                               | Gautinos sumos      | Laisvos formos SF                         |



Norėdami daugiau informacijos žr. [Ilgalaikio turto integravimas](fixed-asset-integration.md).




