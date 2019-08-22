---
title: Peržiūrėti turto punktą
description: Šioje temoje aprašoma „“ paskirstytų užsakymų tvarkymo (DOM) funkcija.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63e5ec5b2a47706763df8105932d722986535a9b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783459"
---
# <a name="asset-view"></a>Peržiūrėti turto punktą

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje aprašoma „“ paskirstytų užsakymų tvarkymo (DOM) funkcija. Puslapyje **Turto rodinys** rodomas aktyvusis turtas ir funkcinės vietos medžio rodinyje. Todėl galite lengvai gauti turto ryšių su funkcinėmis vietomis apžvalgą. Be to, galite peržiūrėti išsamią informaciją apie funkcines vietas, turtą ir susijusias komplektavimo specifikacijas (KS). Taip pat galite greitai peržiūrėti aktyviąsias priežiūros užklausas ir darbo užsakymus, susijusius su turtu.

1. Pasirinkite **Asset management** \> **Common** \> **Assets** \> **Asset view**.
2. Norėdami pakeisti puslapyje rodomą rodinį, lauke **Rodinys** pasirinkite naują reikšmę.

    > [!NOTE]
    > Numatytasis rodinys, kuris rodomas atidarius **Asset view** puslapį, priklauso nuo vertės, kuri pasirinkta **View** skirtuko lapo **Assets** lauko **Asset management parameters** puslapio lauke (**Asset management** \> **Setup** \> **Asset management parameters**).

Dešiniojoje puslapio pusėje „FastTabs“ skirtukuose rodoma pasirinkto rodinio informacija.

Naršymo kelyje, kuris yra rodomas virš medžio rodinio, rodomas dabartinis žymėjimas medžio rodinyje. Naudojamas toks šio naršymo kelio formatas:

Funkcinės vietos ID / Funkcinės vietos ID (jei yra daugiau nei viena funkcinė vieta) \> Turto ID / Turto ID (jei yra daugiau nei vienas turtas) – Elemento numeris.

Jei medžio rodinyje pasirinkote turtą, galite pasirinkti **Aktyviosios užklausos** arba **Aktyvieji darbo užsakymai**, kad peržiūrėtumėte priežiūros užklausas arba darbo užsakymus, susijusius su turtu. Taip pat galite pasirinkti **Atidaryti** \> **Funkcinė vieta**, **Turtas** arba **Turto BOM,** kad būtų atidarytas susijęs vaizdas.

Parinktis **Asset functional locations**, kurią galite pasirinkti lauke **View**, taip pat yra pasiekiama visose turto peržvalgose, kuriose galite pasirinkti turtą. Medžio rodinys yra rodomas skirtuke **Asset view**, pavyzdžiui, ten, kur galite [create an asset](../objects/create-an-object.md), sukurti priežiūros užklausą arba sukurti darbo užsakymą.
