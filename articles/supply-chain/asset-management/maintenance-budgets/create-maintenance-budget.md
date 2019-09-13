---
title: Priežiūros biudžetų kūrimas
description: Šioje temoje aiškinama, kaip biudžetą priežiūros biudžetą turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2c748fd230796643f1ed6279743da532e7cb320
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874813"
---
# <a name="create-maintenance-budgets"></a>Priežiūros biudžetų kūrimas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]



Priežiūros biudžetai naudojami norint apžvelgti prevencinės priežiūros numatytus kaštus. Biudžeto eilutės apskaičiuojamos pagal priežiūros grafiko eilutes, kuriose nurodyta numatyta pradžios data biudžeto laikotarpiu.

Priežiūros biudžetai pagrįsti kaštų tipais, kurie naudojami turto valdyme: **Prevencinis**, **Taisomasis** ir **Investicija**. Į aktyvų turtą, kuriam numatyta pakeitimo data biudžeto laikotarpiu ir susijusi pakeitimo vertė, įtraukti investicijų priežiūros biudžeto kaštai. Taisomosios priežiūros biudžeto kaštai yra įtraukti, jei buvusi taisymo data yra įtraukta į biudžeto skaičiavimą. Tokiu atveju taisomieji kaštai iš ankstesnio laikotarpio yra skaičiuojami tokiam pačiam laikotarpiui, kuriam skaičiuojate priežiūros biudžetą, ateityje.

## <a name="create-a-maintenance-budget"></a>Priežiūros biudžeto kūrimas

1. Pažymėkite **Turto valdymas** \> **Užklausos** \> **Priežiūros biudžetas** \> **Biudžetas**.
2. Pažymėkite **Kurti biudžetą**.
3. Lauke **Priežiūros biudžetas** įveskite biudžeto ID.
4. Lauke **Aprašas** įveskite aprašą.
4. „FastTab“ **Laikotarpis** laukuose **Nuo datos** ir **Iki datos** įveskite biudžeto laikotarpio pradžios ir pabaigos datas.
5. Norėdami įtraukti taisomojo biudžeto kaštus, kurie apskaičiuoti remiantis praėjusio laikotarpio faktiniais kaštais, lauke **Taisomasis nuo datos** įveskite laikotarpio, iš kurio turi būti įtrauktos šios išlaidos, pradžios datą.
6. Atsižvelgiant į biudžetui taikomą išsamumo lygį, nustatykite tinkamas penkias parinktis „FastTabs“ **Grupuoti pagal**.
7. Pasirinkite **Gerai**.
8. Pažymėkite **Biudžeto eilutės**, kad atidarytumėte puslapį **Priežiūros biudžeto eilutės**, kuriame galite peržiūrėti visas biudžeto eilutes, kurios buvo sukurtos laikotarpiui.
9. Norėdami patvirtinti biudžetą, pažymėkite jį puslapyje **Priežiūros biudžetai**, tada pažymėkite **Patvirtinti**. Tada dialogo lange **Patvirtinti biudžetą** pažymėkite **Gerai**. Jūsų vardas yra įvedamas lauke **Patvirtini** puslapyje **Priežiūros biudžetai**.

    > [!NOTE]
    > Patvirtinę priežiūros biudžetą, puslapyje **Priežiūros biudžeto eilutės** negalite perskaičiuoti arba koreguoti susijusių eilučių, nebent pirmiau pašalintumėte patvirtinimą. Norėdami pašalinti priežiūros biudžeto patvirtinimą, pažymėkite jį puslapyje **Priežiūros biudžetai**, tada pažymėkite **Patvirtinti**. Tada dialogo lange **Patvirtinti biudžetą** pažymėkite **Gerai**.

![1 pav.](media/01-maintenance-budgets.png)

Taip pat galite kurti naują priežiūros biudžetą nukopijuodami esamą biudžetą. Puslapyje **Priežiūros biudžetai** pažymėkite kopijuotiną biudžetą, tada pažymėkite **Kopijuoti**. Šis metodas yra naudingas, jei, pavyzdžiui, sukūrėte vieno mėnesio biudžetą ir norite jį kopijuoti į kitus mėnesius.

> [!NOTE]
> Priežiūros biudžetas skaičiuoja tik tuos biudžeto kaštus, kurie pagrįsti priežiūros grafiko eilutėmis. Norėdami apskaičiuoti faktiniu faktinius to paties laikotarpio kaštus, šį skaičiavimą galite atlikti puslapyje **Turto kaštų valdymas**. 
