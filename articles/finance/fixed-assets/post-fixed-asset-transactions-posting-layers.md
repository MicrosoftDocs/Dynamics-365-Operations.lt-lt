---
title: Registruoti ilgalaikio turto operacijas registravimo sluoksniuose
description: Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 538366163bac8ba593bd5575459ddb9b0079094150187dfb8c04490f467f9798
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757078"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Registruoti ilgalaikio turto operacijas registravimo sluoksniuose

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos.

Ilgalaikio turto nusidėvėjimas skaičiuojamas įvairiais būdais ir siekiant įvairių tikslų. Mokestiniais tikslais nusidėvėjimas apskaičiuojamas pagal tuo metu nustatytų mokesčių taisykles, kad prieš skaičiuojant mokesčius turtas nuvertėtų kaip galima daugiau. Ataskaitose fiksuojamas nusidėvėjimas apskaičiuojamas pagal apskaitos įstatymus ir standartus. Įvairių tipų nusidėvėjimas apskaičiuojamas ir registruojamas atskirai skirtinguose registravimo sluoksniuose.

Kiekviena ilgalaikiam turtui priskirta knyga nustatoma konkrečiame registravimo sluoksnyje, turinčiame bendrą nusidėvėjimo tikslą. Galima naudoti dešimt registravimo sluoksnių: Dabartinis, Operacijos, Mokestis ir septynis tipo Pasirinktinis sluoksnius. Taip pat galite išjungti knygos registravimo DK funkciją, nustatydami lauką Registruoti DK į parinktį Ne. Tada laukas Registravimo sluoksnis automatiškai nustatomas į parinktį Nėra. Knygos, kurios neregistruojamos DK, paprastai naudojamos mokesčių registravimo tikslais. Tokiu būdu suteikiama daugiau lankstumo naikinant ankstesnes turto knygos operacijas, nes jos nebuvo perkeltos į DK.

Ilgalaikio turto žurnalai nustatomi naudojant puslapį Žurnalų pavadinimai, kurį galima atidaryti pasirinkus DK > Žurnalo nustatymas > Žurnalų pavadinimai. Kiekvieną žurnalą, kuriame galima registruoti nusidėvėjimą, apibūdina jo pavadinimas, kuris gali būti priskirtas tik vienam registravimo sluoksniui. Žurnalo registravimo sluoksnio keisti negalima. Šis apribojimas padeda užtikrinti, kad kiekvieno registravimo sluoksnio operacijos bus saugomos atskirai. Kiekviename registravimo sluoksnyje turi būti sukurtas bent vienas žurnalo pavadinimas. Jei naudojate knygas, kurios DK neregistruojamos, taip pat turite sukurti žurnalą, kuriame registravimo sluoksnis yra nustatytas į parinktį Nėra.

Puslapyje Ilgalaikio turto registravimo šablonai galite nustatyti DK sąskaitas, kuriose registruojamos ilgalaikio turto operacijos. Kiekviename registravimo šablone turite pasirinkti reikiamą operacijos tipą bei knygą ir nurodyti DK sąskaitas. Nustatykite kiekvienos knygos, kuri bus registruojama DK, registravimo šablono įrašą.

Ilgalaikį turtą galima įvesti į dokumentus, kurie palaiko tik **dabartinį** registravimo sluoksnį, pvz., **Pirkimo užsakymas**, **Laukianti tiekėjo SF**, **Pardavimo užsakymas** arba **Laisvos formos SF**. Pasirinkus ilgalaikio turto ID bet kuriame iš šių dokumentų, turto knyga filtruojama pagal **dabartinį** registravimo sluoksnį ir bus užpildyta automatiškai registruojant, kai sistema patikrins, ar ilgalaikio turto registravimo sluoksnis yra **Dabartinis**. Jei šio tikrinimo negalima baigti, registravimo procesas bus sustabdytas. 

> [!NOTE] 
> Naudodami išvestines knygas, operacijas galite vienu metu registruoti skirtinguose registravimo sluoksniuose. Pagrindinės knygos operacijos kuriamos žurnale arba šaltinio dokumente, kuriame yra registravimo sluoksnis, atitinkantis knygos registravimo sluoksnį. Išvestinės knygos operacijos registruojamos atitinkamuose registravimo sluoksniuose. 


Norėdami gauti daugiau informacijos, žr. [Išvestinės knygos](derived-books.md) ir [Registravimas naudojant išvestines knygas](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]