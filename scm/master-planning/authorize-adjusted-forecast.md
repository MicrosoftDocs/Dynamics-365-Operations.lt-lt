---
title: "Leisti koreguota prognozė"
description: "Ne visus prognozės duomenis reikia įgalioti iš karto. Šiame straipsnyje paaiškinama, kaip galite nurodyti laikotarpį, kurį prognozė yra įgaliojama. Taip pat jame paaiškinama, kaip galima leisti prognozę naudoti konkrečioms įmonėms ir prognozės modeliams."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Leisti koreguota prognozė

Ne visus prognozės duomenis reikia įgalioti iš karto. Šiame straipsnyje paaiškinama, kaip galite nurodyti laikotarpį, kurį prognozė yra įgaliojama. Taip pat jame paaiškinama, kaip galima leisti prognozę naudoti konkrečioms įmonėms ir prognozės modeliams.

Ne visus prognozės duomenis reikia įgalioti iš karto. Galite nurodyti laikotarpio, kurį prognozė turi būti įgaliota, pradžios ir pabaigos datas. Ši funkcija suteikia galimybę blokuoti konkrečius rinkinius. 

Pradžios ir pabaigos datas, kad jūs nurodote turi atitikti pradžios ir pabaigos datas kibirą, prognozė yra generuojami. Sistema užtikrina, kad šis apribojimas ir automatiškai koreguoja datų, jei koreguoti nereikia. 

Puslapio **Autorizavimas** skirtuke **Informacija** galite peržiūrėti informaciją apie vėliausiai sugeneruotą prognozę. 

Galite pasirinkti, kurioms įmonėms ir kuriems prognozės modeliams leisti prognozę naudoti. Pagal numatytuosius parametrus tinklelyje yra įtrauktos visos įmonės, kurioms poreikio prognozė buvo sukurta. Įvedamas kiekvienos įmonės prognozės modelis, kuris atitinka bendrojo planavimo parametruose nustatytą dabartinį prognozės planą. Tačiau šį prognozės modelį galite pakeisti į bet kurį kitą šiai įmonei priklausantį prognozės modelį. Jei nesugeneruota jokių pasirinktos įmonės poreikio prognozės duomenų, importavimo metu gausite perspėjimo pranešimą. 

Labai svarbu suprasti, kokia yra žymės langelio **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus** paskirtis. Jei jūs atlikote rankiniu būdu su statistinės prognozės, patikslintos vertės leista naudoti, net jei šis žymės langelis nepažymėtas. Tačiau po autorizavimo pakeitimai yra panaikinami. Todėl kitą kartą generuojant prognozę ji bus tik statistinė prognozė ir neturės jokių neautomatinių perrašymų, net jei pasirinkta parinktis **Perkelti neautomatinius koregavimus į poreikio prognozę**. Todėl žymės langelį **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus** galima laikyti mechanizmu, kurį naudojant galima išsaugoti arba panaikinti visus neautomatinius pakeitimus.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


