---
title: Registruoti ilgalaikio turto operacijas registravimo sluoksniuose
description: "Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 4b112eee303604149c7609972a60c2014d4be423
ms.lasthandoff: 03/31/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Registruoti ilgalaikio turto operacijas registravimo sluoksniuose

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos.

Ilgalaikio turto nusidėvėjimas skaičiuojamas įvairiais būdais ir siekiant įvairių tikslų. Mokestiniais tikslais nusidėvėjimas apskaičiuojamas pagal tuo metu nustatytų mokesčių taisykles, kad prieš skaičiuojant mokesčius turtas nuvertėtų kaip galima daugiau. Ataskaitose fiksuojamas nusidėvėjimas apskaičiuojamas pagal apskaitos įstatymus ir standartus. Įvairių tipų nusidėvėjimas apskaičiuojamas ir registruojamas atskirai skirtinguose registravimo sluoksniuose.

Kiekviena ilgalaikiam turtui priskirta knyga nustatoma konkrečiame registravimo sluoksnyje, turinčiame bendrą nusidėvėjimo tikslą. Galima naudoti dešimt registravimo sluoksnių: Dabartinis, Operacijos, Mokestis ir septynis tipo Pasirinktinis sluoksnius. Taip pat galite išjungti knygos registravimo DK funkciją, nustatydami lauką Registruoti DK į parinktį Ne. Tada laukas Registravimo sluoksnis automatiškai nustatomas į parinktį Nėra. Knygos, kurios neregistruojamos DK, paprastai naudojamos mokesčių registravimo tikslais. Tokiu būdu suteikiama daugiau lankstumo naikinant ankstesnes turto knygos operacijas, nes jos nebuvo perkeltos į DK.

Ilgalaikio turto žurnalai nustatomi naudojant puslapį Žurnalų pavadinimai, kurį galima atidaryti pasirinkus DK > Žurnalo nustatymas > Žurnalų pavadinimai. Kiekvieną žurnalą, kuriame galima registruoti nusidėvėjimą, apibūdina jo pavadinimas, kuris gali būti priskirtas tik vienam registravimo sluoksniui. Žurnalo registravimo sluoksnio keisti negalima. Šis apribojimas padeda užtikrinti, kad kiekvieno registravimo sluoksnio operacijos bus saugomos atskirai. Kiekviename registravimo sluoksnyje turi būti sukurtas bent vienas žurnalo pavadinimas. Jei naudojate knygas, kurios DK neregistruojamos, taip pat turite sukurti žurnalą, kuriame registravimo sluoksnis yra nustatytas į parinktį Nėra.

Puslapyje Ilgalaikio turto registravimo šablonai galite nustatyti DK sąskaitas, kuriose registruojamos ilgalaikio turto operacijos. Kiekviename registravimo šablone turite pasirinkti reikiamą operacijos tipą bei knygą ir nurodyti DK sąskaitas. Nustatykite kiekvienos knygos, kuri bus registruojama DK, registravimo šablono įrašą.

> [!NOTE] 
> Naudodami išvestines knygas, operacijas galite vienu metu registruoti skirtinguose registravimo sluoksniuose. Pagrindinės knygos operacijas galite kurti žurnale, kuriame yra registravimo sluoksnis, atitinkantis knygos registravimo sluoksnį. Išvestinės knygos operacijos registruojamos atitinkamuose registravimo sluoksniuose.

Norėdami gauti daugiau informacijos, žr. [Išvestinės knygos](derived-books.md) ir [Registravimas naudojant išvestines knygas](post-derived-value-models.md).




