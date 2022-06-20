---
title: Mažmeninės kainos ataskaitos
description: Šiame straipsnyje pateikiama kainos ataskaitos priemonės, kurią galima naudoti norint peržiūrėti būsimus pateiktais produktais kainos pakeitimus, apžvalga.
author: shajain
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 84025cf148e1b5a92b78593fc093c629a3af4764
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899046"
---
# <a name="retail-price-reports"></a>Mažmeninės kainos ataskaitos

[!include [banner](includes/banner.md)]


Siekdami teikti konkurencingas kainas savo klientams, mažmenininkai dažnai keičia produktų kainas. Parduotuvių vadovai nori galimybės lengvai pasiekti nesenus arba būsimus kainų pakeitimus, kad jie galėtų suplanuoti, jog reikiami ištekliai atnaujintų kainų etiketes, rodomas parduotuvės lentynose. Mažmeninės prekybos 10.0 versijoje parduotuvės vadovas gali atidaryti ataskaitą **Kaina**, nuėjęs į **Visos parduotuvės \> Parduotuvė \> Kainų ataskaita** ir peržiūrėjęs atnaujintas su parduotuve susijusių produktų kainas. 

Kad būtų galima įjungti kainų ataskaitą, turi būti įjungtas parametras **Įgalinti parduotuvės kainų ataskaitą**. Šis parametras yra skirtuke **„Commerce“ parametrai \> Nuolaidos \> Įvairūs**. Atidarius puslapį **Kainų ataskaita**, rodomas dialogo langas su įvairiomis konfigūracijomis. Galimos konfigūracijos pateiktos toliau.

| Konfigūravimas | aprašymas |
|---|---|
| Pradžios data / pabaigos data| Generuotinos kainų ataskaitos datų intervalas. Šiuo metu trukmė apribota iki 7 dienų. |
| Kanalas| Parduotuvė, kuriai turėtų būti suformuota kainų ataskaita. |
| Rodyti produktus su turimomis atsargomis| Nustačius šio parametro parinktį **Taip**, bus rodomos tik tų produktų, kurių faktinių atsargų tuo metu yra parduotuvėje, kainos. |
| Rodyti variantų kainas | Nustačius šio parametro parinktį **Taip**, bus rodomi variantų ir bendrųjų produktų kainos. Šis parametras turėtų būti **Įjungtas** tik jei esate nustatę konkrečių variantų kainas, nes eilučių skaičius gali labai išaugti. Būsimuose leidimuose įjungsime dimensijomis pagrįstas kainas, kad parduotuvės vadovas galėtų pasirinkti dimensijas, kurių kainos turėtų būti rodomos. |
| Rodyti produktus su kainų pokyčiais | Nustačius šio parametro parinktį **Taip**, bus rodomos tik tų dienų, per kurias kaina buvo pakeista, kainos. *Vienos dienos prieš* pasirinktą **pradžios datą** kaina visada bus rodoma, kad parduotuvės vadovas galėtų lengvai nustatyti produktus, kurių kainos nepasikeitė per visą pasirinktą laikotarpį, ir taip pat peržiūrėti esamą kainą. |

Sugeneravus ataskaitą, galima atsisiųsti „Excel“ failą, jei reikia atlikti papildomų filtravimo veiksmų. Kainų ataskaitą taip pat galima naudoti norint patikrinti praeities datų produktų kainas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]