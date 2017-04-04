---
title: "Projekto sąnaudų kaupimo apie pirkimo kvitai"
description: "Šioje temoje aprašoma, kaip sukauptų projekto išlaidų pirkimo kvitus gali būti stebimi Microsoft Dynamics 365 operacijoms."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projekto sąnaudų kaupimo apie pirkimo kvitai

Šioje temoje aprašoma, kaip sukauptų projekto išlaidų pirkimo kvitus gali būti stebimi Microsoft Dynamics 365 operacijoms. 

SF projektui dažnai atvyksta vėliau nei prekės ir paslaugos yra teikiamos, kurios gali daryti didelę įtaką projekto pagrindinius veiklos rodiklius (KPI). Tai svarbu, kad būtų galima stebėti šias operacijas tiek finansų ir projektų ataskaitas.

Šį pavyzdį scenarijų iliustruoja tai. 

Contoso konsultavimo pradėjo naują nuotolinių išteklių diegimo projektą. Pirkimo užsakymas sukurtas pirkti kompiuterį už projektą. Kompiuteris kainuos $1500 ir montavimo paslaugos kainuos $150. Pardavėjas turi pristatyti ir įdiegta į kompiuterį, bet SF dar nepasiekė Contoso konsultacijos. Projektų vadovas norėtų matyti projekto sąnaudų kaupimo $1650 prieš pristatant SF. Šias išlaidas taip pat turėtų atsispindėti bendrovės mėnesio pabaigos finansinės ataskaitos. 

Sukauptos išlaidos turi būti traukiama į finansų lygį bei projekto lygio atskaitomybę. Dynamics 365 operacijoms, finansų važtaraščio atnaujinimas gali būti stebimi elementą ir pirkimų kategorijų. 

Daiktų, dėl į **sudaro mokėtinų sumų parametrai** puslapyje, pasirinkite į **užregistruoti važtaraščiai DK** variantas.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Pirkimų kategorijoms, dėl į **kategorija politika paprastai** puslapyje, pasirinkite **perkamosios** strategijas, o tada pasirinkite **kaupti pirkimo sąskaita gavus** ruožams viešųjų pirkimų.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Į **pirkimo išlaidų JT išrašytoje SF** ir **pirkimo kaupimo** sudaro **registravimo nustatymo** bus naudojamas registruojant kvitus, kurie yra susiję su produkto gavimo.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Naudojant šį patį scenarijų, pažiūrėkime, kaip parašėte važtaraštyje turės įtakos DK ir informaciją apie projektą. 

**1 veiksmas:** sukurti ir patvirtinti naują pirkimo užsakymą įrašyti kompiuterio $150 $1500 ir diegimo paslaugų pirkimo projektas.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Kai pirkimo užsakymas bus patvirtintas, projekto sukuriamos operacijos padarytas išlaidas. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Fiksuota savikaina operacijos turės į **operacijos kilmę** laukas nustatytas kaip **pirkimo užsakymo**. Sukurti ir patvirtinti pirkimo užsakymą nesukuria sandorių projektui. 

**2 veiksmas:** gauti pristatytas prekes ir paslaugas ir važtaraštyje yra registruotas. 

Parašėte važtaraštyje generuoti ir registruoti į DK kvitas. Kvito debetuoti pirkimo išlaidos, JT SF išrašyta sąskaita, ar pirkimo kaupimo sąskaitą. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Registravimo važtaraštyje naudos registravimo nustatymas pirkimų kategorijas ir produktų ir ne į registravimo nustatymus projektų kategorijoms. Kad būtų teisingai atspindėtas finansinio poveikio pirkimo sukauptų, šis nustatymas turi būti suderintas. 

Yra galimybė žemėlapį pirkimų kategorijos projektų grupių, **pirkimų kategorijos** puslapis.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3 veiksmas:** kūrimas projekto pirkimo užsakymo SF. 

Dynamics 365 operacijų, registravimo važtaraštyje neturi įtakos projekto informacija. Laikinas problemos sprendimas, gali generuoti projekto tiekėjo SF tiesiogiai užregistravus pirkimo kvitas. Eikite į į **pirkimo užsakymo** puslapis &gt;**SF skirtuke**&gt;**sukurti**&gt;**SF**. Tai sukuria laukianti SF dokumentą, kuris atnaujina informaciją apie projektą. 

Kūrimas projekto pirkimo užsakymo SF sukurs laukiama projekto operacijas. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

– Į **padarytas išlaidas** puslapyje, įrašus, sukurtus atliekant 1 veiksmą bus uždarytas ir naujų įrašų bus sukurtas atspindėti išlaidų įsipareigojimą iš laukianti SF. Į **operacijos kilmę** lauko, nes bus nustatyta fiksuota savikaina **tiekėjo SF**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Tiekėjo SF yra laukimo būsenoje tol, kol faktinės tiekėjo SF atvyksta.


