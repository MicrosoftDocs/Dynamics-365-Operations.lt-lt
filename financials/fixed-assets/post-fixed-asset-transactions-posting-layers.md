---
title: Registruojamos ilgalaikio turto operacijos registravimo sluoksniai
description: "Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
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

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Registruojamos ilgalaikio turto operacijos registravimo sluoksniai

Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos.

Ilgalaikio turto nusidėvėjimas skaičiuojamas įvairiais būdais ir siekiant įvairių tikslų. Mokestiniais tikslais nusidėvėjimas apskaičiuojamas pagal tuo metu nustatytų mokesčių taisykles, kad prieš skaičiuojant mokesčius turtas nuvertėtų kaip galima daugiau. Ataskaitose fiksuojamas nusidėvėjimas apskaičiuojamas pagal apskaitos įstatymus ir standartus. Įvairių tipų nusidėvėjimas apskaičiuojamas ir registruojamas atskirai skirtinguose registravimo sluoksniuose.

Kiekviena ilgalaikiam turtui priskirta knyga nustatoma konkrečiame registravimo sluoksnyje, turinčiame bendrą nusidėvėjimo tikslą. Galima naudoti dešimt registravimo sluoksnių: Dabartinis, Operacijos, Mokestis ir septynis tipo Pasirinktinis sluoksnius. Taip pat galite išjungti knygos registravimo DK funkciją, nustatydami lauką Registruoti DK į parinktį Ne. Tada laukas Registravimo sluoksnis automatiškai nustatomas į parinktį Nėra. Paprastai, mokestinių ataskaitų teikimo tikslais naudojami knygas, nereikia registruoti į DK. Šis metodas suteikia jums daugiau lankstumo ištrinti istorinę sandorių turto knygos, nes jie nebuvo įsipareigoję DK.

Ilgalaikio turto žurnalai nustatomi naudojant puslapį Žurnalų pavadinimai, kurį galima atidaryti pasirinkus DK > Žurnalo nustatymas > Žurnalų pavadinimai. Kiekvieną žurnalą, kuriame galima registruoti nusidėvėjimą, apibūdina jo pavadinimas, kuris gali būti priskirtas tik vienam registravimo sluoksniui. Registravimo sluoksniui leidinyje negali būti pakeistas. Šis apribojimas padeda užtikrinti, kad kiekvieno registravimo sluoksnio operacijos bus saugomos atskirai. Kiekviename registravimo sluoksnyje turi būti sukurtas bent vienas žurnalo pavadinimas. Jei naudojate knygas, nereikia registruoti į DK, taip pat turite sukurti žurnalo, kur registravimo sluoksniui nustatomas kaip nėra.

Puslapyje Ilgalaikio turto registravimo šablonai galite nustatyti DK sąskaitas, kuriose registruojamos ilgalaikio turto operacijos. Kiekviename registravimo šablone turite pasirinkti reikiamą operacijos tipą bei knygą ir nurodyti DK sąskaitas. Nustatykite kiekvienos knygos, kuri bus registruojama DK, registravimo šablono įrašą.

> [!NOTE] 
> Naudojant išvestinio knygų, galima registruoti operacijas į skirtingas registravimo sluoksniuose tuo pačiu metu. Pagrindinės knygos operacijas galite kurti žurnale, kuriame yra registravimo sluoksnis, atitinkantis knygos registravimo sluoksnį. Išvestinės knygos operacijos registruojamos atitinkamuose registravimo sluoksniuose.

Daugiau informacijos ieškokite [gautų knygų](derived-books.md) ir [registravimas naudojant išvestinio knygos](post-derived-value-models.md).


