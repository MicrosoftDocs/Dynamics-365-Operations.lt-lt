---
title: Darbo eigos patvirtinimo procesų veiksmai
description: Šiame straipsnyje aprašyti veiksmai, kurių kiekvienas darbo eigos patvirtinimo proceso dalyvis gali imtis.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2973454e585f8ee45c0b6ee95c8b41e93bc2d962
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694292"
---
# <a name="actions-in-workflow-approval-processes"></a>Darbo eigos patvirtinimo procesų veiksmai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašyti veiksmai, kurių kiekvienas darbo eigos patvirtinimo proceso dalyvis gali imtis.

Darbo eiga gali apimti keletą žmonių grupių: iniciatorių, užduočių priėmėjus, sprendimus priimančius asmenis ir tvirtintojus. Pavyzdžiui, šioje išlaidų ataskaitos darbo eigoje Samas yra iniciatorius, eilės nariai yra užduočių priėmėjai, Johnas yra sprendimų priėmėjas, o Frankas, Sue ir Ann yra tvirtintojai.

[![Darbo eiga\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)

Tolesniuose skyriuose paaiškinami darbo eigos veiksmai, kuriuos gali atlikti kiekviena grupė.

## <a name="actions-that-an-originator-can-perform"></a>Veiksmai, kuriuos gali atlikti iniciatorius

Iniciatorius paleidžia darbo eigos egzempliorių pateikdamas dokumentą apdoroti. Pvz., Samas turi spustelėti mygtuką **Pateikti**, esantį **Išlaidų ataskaitos** puslapyje, kad pateiktų savo išlaidų ataskaitą.

## <a name="actions-that-a-task-assignee-can-perform"></a>Veiksmai, kuriuos gali atlikti užduoties priėmėjas

Užduotis gali būti priskirta keliems žmonėms arba darbo elementų eilei, kurią stebi keli žmonės. Tačiau tik vienas asmuo gali atlikti užduotį. Pvz., Semas pateikė išlaidų ataskaitą ir savo produktų gavimo kvitus perdavė organizacijos Išlaidų ataskaitų skyriui, kad juos peržiūrėtų.

Eilę stebi „Adventure Works‟ Išlaidų ataskaitų skyriaus nariai. Julie, to skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį. Dabar ji gali atlikti vieną iš šių veiksmų: užbaigti, atmesti, perduoti, prašyti pakeisti, priskirti iš naujo ar išleisti.

> [!NOTE]
> Galimi veiksmai skiriasi – tai priklauso nuo to, kaip programinės įrangos kūrėjas sukūrė užduotį.

### <a name="complete"></a>Baigti

Kai naudotojas pabaigia užduotį, apdoroti pateiktas dokumentas priskiriamas kitam darbo eigos naudotojui, jei kitas naudotojas yra. Jei papildomas apdorojimas nereikalingas, darbo eigos procesas baigiasi.

Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį. Julie atlikus peržiūrą, dokumentas priskiriamas Johnui.

### <a name="reject"></a>Atmesti

Kai naudotojas atmeta dokumentą, darbo eigos procesas baigiasi.

Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį. Jei Julie atmeta išlaidų ataskaitą, darbo eigos procesas baigiasi.

Samas tada gali išlaidų ataskaitą pateikti iš naujo. Pirmiausia jis gali ataskaitą keisti, arba gali iš naujo pateikti pradinę versiją. Jei Samas pakartotinai pateikia išlaidų ataskaitą, darbo eigos procesas prasideda rankinės peržiūros užduotimi.

### <a name="delegate"></a>Perduoti

Kai vartotojas perduoda užduotį, užduotis priskiriama kitam vartotojui.

Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį. Julie šią užduotį perduoda Timui, kuris yra jos padėjėjas.

Timas tada veikia Julie vardu. Todėl, kai Timas atlieka peržiūrą, išlaidų ataskaita priskiriama Johnui, lygiai taip, jei užduotį būtų atlikusi Julie.

### <a name="request-change"></a>Reikalauti keitimo

Kai naudotojas reikalauja pateikto dokumento keitimo, dokumentas grąžinamas iniciatoriui.

Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį. Julie išlaidų ataskaitoje pastebi keletą klaidų ir reikalauja pakeitimų. Išlaidų ataskaita vėl siunčiama Samui.

Samas gali išlaidų ataskaitą pateikti iš naujo. Pirmiausia jis gali atlikti pageidautus keitimus, arba gali iš naujo pateikti pradinę versiją. Jei Samas pakartotinai pateikia išlaidų ataskaitą, darbo elementų eilės narys turi vėl peržiūrėti išlaidų ataskaitą ir produktų gavimo kvitus.

### <a name="reassign"></a>Priskirti iš naujo

Darbo elementų eilės nariai gali toje eilėje esančius dokumentus iš naujo priskirti kitai eilei.

Pavyzdžiui, eilę stebi Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė. Norėdama subalansuoti darbo krūvį, išlaidų ataskaitą ir prie jos pridėtus kvitus ji gali iš naujo priskirti kitai eilei.

### <a name="release"></a>Paleisti

Kartais darbo elementų eilės narys gali užduotį priimti, bet tada nuspręsti, kad jis ar ji užduoties atlikti negali. Šiuo atveju asmuo, kuris priėmė užduotį, dokumentą gali vėl išleisti į darbo elementų eilę.

Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį. Jei Julie nusprendžia, kad užduoties atlikti negali, ji gali dokumentą išleisti. Išlaidų ataskaita grąžinama į eilę, kad užduotį galėtų atlikti kiti „Adventure Works‟ Išlaidų ataskaitų skyriaus nariai.

## <a name="actions-that-a-decision-maker-can-perform"></a>Veiksmai, kuriuos gali atlikti sprendimų priėmėjas

Paprastai dokumentas priskiriamas sprendimų priėmėjui todėl, kad yra klausimas, į kurį turi atsakyti sprendimų priėmėjas. Atsakymas į klausimą paprastai yra **Taip** arba **Ne**, arba **Teisinga** arba **Klaidinga**. Jei sprendimų priėmėjas vieno iš tų pasirinkimų nepasirenka, jis arba ji sprendimą gali perduoti.

### <a name="choice-1-or-choice-2"></a>\[1 pasirinkimas\] arba \[2 pasirinkimas\]

Sprendimų priėmėjas turi atsakyti į klausimą, susijusį su dokumentu. Atsakymas į klausimą paprastai yra **Taip** arba **Ne**, arba **Teisinga** arba **Klaidinga**. Atsakymu, kurį pasirenka sprendimų priėmėjas, nustatoma darbo eigos šaka, naudojama apdoroti dokumentui.

Pvz., Samo išlaidų ataskaita priskiriama Johnui. Johnas turi nuspręsti, ar dėl dokumento informacijos reikia skambinti Samo vadovui. Jei Johnas nusprendžia, kad skambinti reikia, išlaidų ataskaita priskiriama Arethai, kuri tada turi paskambinti Samo vadovui. Jei Johnas nusprendžia, kad skambinti nereikia, išlaidų ataskaita priskiriama Frankui, kad ją patvirtintų.

### <a name="delegate"></a>Perduoti

Kai sprendimų priėmėjas sprendimą perduoda, dokumentas priskiriamas kitam naudotojui, kuris turi priimti sprendimą.

Pvz., Samo išlaidų ataskaita priskiriama Johnui. Johnas sprendimą perduoda Mariai, kuri yra jo padėjėja.

Maria tada veikia Johno vardu. Jei Maria nusprendžia, kad reikia skambinti Samo vadovui, išlaidų ataskaita priskiriama Arethai, kuri tada turi paskambinti Samo vadovui. Jei Maria nusprendžia, kad skambinti nereikia, išlaidų ataskaita priskiriama Frankui, kad ją patvirtintų.

## <a name="actions-that-an-approver-can-perform"></a>Veiksmai, kuriuos gali atlikti tvirtintojas

Kai dokumentas priskirtas tvirtintojui, tvirtintojas gali atlikti vieną iš šių veiksmų: patvirtinti, atmesti, perduoti arba prašyti pakeisti.

### <a name="approve"></a>Patvirtinti

Kai tvirtintojas patvirtina dokumentą, dokumentas priskiriamas kitam darbo eigos naudotojui, jei kitas naudotojas yra. Jei papildomas apdorojimas nereikalingas, darbo eigos procesas baigiasi.

Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 6 000 USD ir šis dokumentas priskiriamas Frankui. Kai Frankas patvirtina dokumentą, jis priskiriamas tvirtinti Sue. Kai Sue patvirtina išlaidų ataskaitą, darbo eigos procesas baigiasi.

### <a name="reject"></a>Atmesti

Kai tvirtintojas atmeta dokumentą, darbo eigos procesas baigiasi.

Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 12 000 USD ir šis dokumentas priskiriamas Sue. Jei Sue atmeta išlaidų ataskaitą, darbo eigos procesas baigiasi.

Samas gali išlaidų ataskaitą pateikti iš naujo. Pirmiausia jis gali atlikti keitimus, arba gali iš naujo pateikti pradinę išlaidų ataskaitos versiją. Jei Samas pakartotinai pateikia išlaidų ataskaitą, darbo eigos procesas prasideda tvirtinimo procesu.

### <a name="delegate"></a>Perduoti

Kai tvirtintojas perduoda dokumentą, dokumentas priskiriamas tvirtinti kitam vartotojui.

Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 12 000 USD ir šis dokumentas priskiriamas Frankui. Frenkas perduoda išlaidų ataskaitą Anai.

Tada Ann veikia Franko vardu. Todėl kai Ann patvirtina dokumentą, jis priskiriamas tvirtinti Sue, lygia taip, jei jį būtų patvirtinęs Frankas. Kai Sue patvirtina dokumentą, jis siunčiamas tvirtinti Ann.

### <a name="request-change"></a>Reikalauti keitimo

Kai tvirtintojas reikalauja dokumento keitimo, dokumentas grąžinamas iniciatoriui.

Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 12 000 USD ir šis dokumentas priskiriamas Sue. Jei Sue reikalauja pakeitimo, išlaidų ataskaita grąžinama Samui.

Samas gali išlaidų ataskaitą pateikti iš naujo. Pirmiausia jis gali atlikti pageidautus keitimus, arba gali iš naujo pateikti pradinę išlaidų ataskaitos versiją. Jeigu Samas pakartotinai pateikia išlaidų ataskaitą, ji siunčiama tvirtinti Frankui, nes Frankas yra pirmasis tvirtintojas patvirtinimo procese.
