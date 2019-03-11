---
title: Mažmeninės kainos ataskaitos
description: Šioje temoje apžvelgiama kainų ataskaitos funkcija, kurią galima naudoti norint peržiūrėti būsimus pateiktų produktų kainų pokyčius.
author: shajain
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 6db6d1c6b6eb1d69b40fe75d97eeb71564986707
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "353062"
---
# <a name="retail-price-reports"></a>Mažmeninės kainos ataskaitos

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]


Siekdami teikti konkurencingas kainas savo klientams, mažmenininkai dažnai keičia produktų kainas. Parduotuvių vadovai nori galimybės lengvai pasiekti nesenus arba būsimus kainų pakeitimus, kad jie galėtų suplanuoti, jog reikiami ištekliai atnaujintų kainų etiketes, rodomas parduotuvės lentynose. Išleidus „Dynamics 365 for Retail 10.0“, parduotuvės vadovas gali atidaryti ataskaitą **Kaina** pasirinkęs **Visos mažmeninės prekybos parduotuves \> Parduotuvė \> Kainų ataskaita** ir peržiūrėti atnaujintų su parduotuve susietų produktų kainas. 

Norėdami įjungti kainų ataskaitą, turite įjungti parametrą **Įjungti mažmeninės prekybos parduotuvės kainų ataskaitą**. Šis parametras pateiktas skirtuke **Mažmeninės prekybos parametrai \> Nuolaidos \> Įvairios**. Atidarius puslapį **Kainų ataskaita** rodomas dialogo langas ir įvairios konfigūracijos. Galimos konfigūracijos pateiktos toliau.

| Konfigūravimas | aprašymas |
|---|---|
| Pradžios data / pabaigos data| Generuotinos kainų ataskaitos datų intervalas. Šiuo metu trukmė apribota iki 7 dienų. |
| Kanalas| Generuotinos kainų ataskaitos mažmeninės prekybos parduotuvė. |
| Rodyti produktus su turimomis atsargomis| Nustačius šio parametro parinktį **Taip**, bus rodomos tik tų produktų, kurių faktinių atsargų tuo metu yra parduotuvėje, kainos. |
| Rodyti variantų kainas | Nustačius šio parametro parinktį **Taip**, bus rodomi variantų ir bendrųjų produktų kainos. Šis parametras turėtų būti **Įjungtas** tik jei esate nustatę konkrečių variantų kainas, nes eilučių skaičius gali labai išaugti. Būsimuose leidimuose įjungsime dimensijomis pagrįstas kainas, kad parduotuvės vadovas galėtų pasirinkti dimensijas, kurių kainos turėtų būti rodomos. |
| Rodyti produktus su kainų pokyčiais | Nustačius šio parametro parinktį **Taip**, bus rodomos tik tų dienų, per kurias kaina buvo pakeista, kainos. *Vienos dienos prieš* pasirinktą **pradžios datą** kaina visada bus rodoma, kad parduotuvės vadovas galėtų lengvai nustatyti produktus, kurių kainos nepasikeitė per visą pasirinktą laikotarpį, ir taip pat peržiūrėti esamą kainą. |

Sugeneravus ataskaitą, galima atsisiųsti „Excel“ failą, jei reikia atlikti papildomų filtravimo veiksmų. Kainų ataskaitą taip pat galima naudoti norint patikrinti praeities datų produktų kainas.
