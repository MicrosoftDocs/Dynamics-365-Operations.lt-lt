---
title: Pakoreguotos prognozės įgaliojimas
description: Ne visus prognozės duomenis reikia įgalioti iš karto. Šiame straipsnyje paaiškinama, kaip galite nurodyti laikotarpį, kurį prognozė yra įgaliojama. Taip pat jame paaiškinama, kaip galima leisti prognozę naudoti konkrečioms įmonėms ir prognozės modeliams.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de7384e94a4b97cf515bb437ad546a8a5f96aa77
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815231"
---
# <a name="authorize-an-adjusted-forecast"></a>Pakoreguotos prognozės įgaliojimas

[!include [banner](../includes/banner.md)]

Ne visus prognozės duomenis reikia įgalioti iš karto. Šiame straipsnyje paaiškinama, kaip galite nurodyti laikotarpį, kurį prognozė yra įgaliojama. Taip pat jame paaiškinama, kaip galima leisti prognozę naudoti konkrečioms įmonėms ir prognozės modeliams.

Ne visus prognozės duomenis reikia įgalioti iš karto. Galite nurodyti laikotarpio, kurį prognozė turi būti įgaliota, pradžios ir pabaigos datas. Ši funkcija suteikia galimybę blokuoti konkrečius rinkinius. 

Nurodomos pradžios ir pabaigos datos turi atitikti rinkinio, kuriame prognozė generuojama, pradžios ir pabaigos datas. Sistema taiko šį apribojimą ir automatiškai koreguoja datas, jei reikia. 

Puslapio **Autorizavimas** skirtuke **Informacija** galite peržiūrėti informaciją apie vėliausiai sugeneruotą prognozę. 

Galite pasirinkti, kurioms įmonėms ir kuriems prognozės modeliams leisti prognozę naudoti. Pagal numatytuosius parametrus tinklelyje yra įtrauktos visos įmonės, kurioms poreikio prognozė buvo sukurta. Įvedamas kiekvienos įmonės prognozės modelis, kuris atitinka bendrojo planavimo parametruose nustatytą dabartinį prognozės planą. Tačiau šį prognozės modelį galite pakeisti į bet kurį kitą šiai įmonei priklausantį prognozės modelį. Jei nesugeneruota jokių pasirinktos įmonės poreikio prognozės duomenų, importavimo metu gausite perspėjimo pranešimą. 

Labai svarbu suprasti, kokia yra žymės langelio **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus** paskirtis. Jei atlikote neautomatinių pagrindinės statistinės prognozės koregavimų, patikslintas reikšmes leidžiama naudoti, net jei šis žymės langelis išvalytas. Tačiau po autorizavimo pakeitimai yra panaikinami. Todėl kitą kartą generuojant prognozę ji bus tik statistinė prognozė ir neturės jokių neautomatinių perrašymų, net jei pasirinkta parinktis **Perkelti neautomatinius koregavimus į poreikio prognozę**. Todėl žymės langelį **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus** galima laikyti mechanizmu, kurį naudojant galima išsaugoti arba panaikinti visus neautomatinius pakeitimus.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)

[Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md)



