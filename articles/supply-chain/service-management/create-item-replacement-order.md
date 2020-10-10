---
title: Prekės pakeitimo užsakymo kūrimas
description: Prekių pakeitimo užsakymai dažniausiai kuriami tada, kai produktas yra jau grąžintas ir patikrintas.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63c175d12cac91648cb57a3f41d1769e81d57af
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830104"
---
# <a name="create-an-item-replacement-order"></a>Prekės pakeitimo užsakymo kūrimas 

[!include [banner](../includes/banner.md)]


Prekių pakeitimo užsakymai dažniausiai kuriami tada, kai produktas yra jau grąžintas ir patikrintas. Tačiau, jei prekė turi būti pakeista anksčiau, nei ji grąžinama, ar kai originali prekė nebus grąžinta, galite sukurti prekės pakeitimo užsakymą iškart po to, kai sukūrėte grąžinimo užsakymą.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Kurti pakeitimo užsakymą gavus prekę, kuri yra grąžinama

1.  Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**.

2.  Sukurkite naują grąžinimo užsakymą arba pasirinkite grąžintą užsakymą iš sąrašo, kad atidarytumėte formą **Grąžinimo užsakymas – RMA numeris: %1, %2**.

3.  Spustelėkite **Grąžinimo eilutė**, tada pasirinkite **Prekės pakaitalas**.

4.  Pasirinkite prekę, kuria norite pakeisti grąžinamą prekę. Įveskite prekės specifikacijas, ir tada spustelėkite **Taikyti**.

5.  Spustelėję **Važtaraštis** generuokite grąžinimo užsakymo važtaraštį. Pardavimo užsakymas yra sugeneruotas keičiamai prekei, kurią pasirinkote.
    
    Keičiamai prekei sukūrus pardavimo užsakymą, pardavimo sutartys yra ieškomos automatiškai, jei yra taikoma pardavimo sutartis, ji taikoma šiam pardavimo užsakymui.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Kurti pakeitimo užsakymą, kol gausite elementą, kuris bus grąžintas

1.  Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**.

2.  Sukurkite naują grąžinimo užsakymą arba pasirinkite grąžinimo užsakymą iš sąrašo, kad atidarytumėte formą **Grąžinimo užsakymas – RMA numeris: %1, %2**.

3.  Jei norite nustatyti grąžintos prekės pardavimo užsakymą, spustelėkite **Rasti pardavimo užsakymą**. Užpildykite formą **Rasti pardavimo užsakymą** ir spustelėję **Gerai** uždarykite formą ir grįžkite į formą **Grąžinimo užsakymas – RMA numeris: %1, %2**. Pardavimo užsakymo eilutė, skirta grąžintai prekei, nukopijuojama į grąžinimo užsakymą.

4.  Spustelėję **Pakeitimo užsakymas** atidarykite formą **Kurti pardavimo užsakymą**.

5.  Pažymėkite žymės langelį **Kopijuoti grąžinimo užsakymo eilutes**, jei norite perkelti informaciją iš jūsų pasirinkto grąžinimo užsakymo formoje **Grąžinimo užsakymas – RMA numeris: %1, %2** į šį pardavimo užsakymą.

6.  Įveskite arba modifikuokite informaciją kaip reikia.
    
    Jei nustatėte pardavimo užsakymą 3 veiksme, ir jei grąžintos prekės pardavimo užsakymo eilutė yra susieta su pardavimo sutartimi, taikomos pardavimo sutarties dėl prekės pakeitimo užsakymo identifikatorius bus automatiškai rodomas lauke **Pardavimo sutarties ID**.

7.  Spustelėję **Gerai** uždarykite formą **Kurti pardavimo užsakymą** ir atidarykite formą **Pardavimo užsakymas**, kur galite toliau įvesti informaciją apie naują pardavimo užsakymą. Visos taikomos grąžinimo užsakymo eilutės bus nukopijuotos į naują pardavimo užsakymą. 
    
    Jei pardavimo sutarties identifikatorius automatiškai rodomas lauke **Pardavimo sutarties ID**, tada pardavimo sutartis buvo susieta su prekės pakeitimo užsakymo pardavimo užsakymo antrašte. Jei yra taikomas dar neįvykdytas įsipareigojimas pardavimo sutartyje, ir pardavimo užsakymas sukurtas iki pardavimo sutarties galiojimo pabaigos, yra nustatomas saitas tarp pardavimo sutarties eilutės ir pardavimo užsakymo eilutės. Todėl informacija iš pardavimo sutarties, pvz., prekės kaina, kopijuojama į naują pardavimo užsakymo eilutę. 
  


