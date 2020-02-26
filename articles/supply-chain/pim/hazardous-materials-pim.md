---
title: Pavojingos medžiagos
description: Šioje temoje pateikiama informacija apie pavojingos medžiagos dokumentus ir informaciją, saugomą jūsų aplinkoje.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76dd6539e39bb77c546e613b290fc5decba9457f
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982313"
---
# <a name="hazardous-materials"></a>Pavojingos medžiagos

[!include [banner](../includes/banner.md)]

Informacija apie pavojingas medžiagas nustatoma produkto informacijos valdyme. Be to, šiame modulyje pateikiami dokumentai, kuriuos galima atspausdinti per sandėlio valdymą.

Kai siunčiate medžiagas, kurios klasifikuojamos kaip pavojingos prekės, prie siuntų turi būti pridėti papildomi dokumentai. Pavojingų medžiagų funkcijose klientai gali išsaugoti klasifikacijos informaciją ir susieti ją su leidimo prekėmis. Ši informacija gali būti naudojama ruošiant siuntimo dokumentus.

> [!IMPORTANT]
> Kad būtų lengviau tvarkyti pavojingų prekių siuntas, „Microsoft Dynamics 365 Supply Chain Management“ galite nustatyti papildomą nuorodos informaciją, susijusią su produktais. Taip pat galite nustatyti papildomus siuntos dokumentus. Tačiau sistema automatiškai neatitinka jūsų šalies arba regiono nuostatų. Tai priemonė, kuri gali būti naudinga jūsų bendrajai programai.

Kad galėtumėte naudoti šią funkciją, reikia nustatyti šiuos parametrus:

- **Produkto informacijos valdymas:** nustatykite kodus, kurie gali būti taikomi išleistoms prekėms.
- **Sandėlio valdymas:** norėdami spausdinti siuntimo informaciją, naudokite papildomus siuntimo dokumentus.

## <a name="product-information-management"></a>Produkto informacijos valdymas

Produkto informacijos valdyme yra sąrankos lentelių, kuriose galite pridėti nuorodos informaciją, pateikiamą pavojingų prekių sąrašuose, skirtuose kelių, oro ir jūrų transportui.

Čia pateiktos kai kurios dažnai nurodomos nuostatos:

- **ADR** – nuostatos, susijusios su tarptautiniu pavojingų krovinių vežimu keliais
- **CFR 49** – pavojingų prekių gabenimo Jungtinėse Valstijose nuostatos
- **IMDG** – Tarptautinis pavojingų krovinių vežimo jūra (IMDG) kodeksas
- **IATA** – Tarptautinės oro transporto asociacijos (IATA) pavojingų prekių gabenimo nuostatos

Kiekviena iš šių nuostatų turi pavojingų prekių sąrašą, kuriame pateikiami nuorodų kodai. Kiekvienos transportavimo rūšies sąrašai sujungiami į bendrai naudojamas tarptautines klasifikacijas. „Supply Chain Management“ pateikia tų sąrašų bendrai naudojamų kodų nuorodų lentelę. Kiekviename sąraše taip pat yra keli unikalūs kodai, kuriuos galima apibrėžti.

Norėdami pirmiausia konfigūruoti šią informaciją, sukurkite nuostatą, kurią galėtumėte naudoti pradiniams parametrams konfigūruoti.

## <a name="warehouse-management"></a>Sandėlio valdymas

Kai ruošiama siunta, galima atspausdinti kelias naujas ataskaitas. Šiose ataskaitose naudojama informacija, nustatyta produkto informacijos valdyme.
