---
title: Pavojingos medžiagos
description: Šioje temoje pateikiama informacija apie pavojingos medžiagos dokumentus ir informaciją, saugomą jūsų aplinkoje.
author: lachlancashMS
manager: tfehr
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
ms.openlocfilehash: 54e5dca38b31c9310d44bdda5f5af14ca1515541
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802706"
---
# <a name="hazardous-materials"></a>Pavojingos medžiagos

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Informacija apie pavojingas medžiagas nustatoma produkto informacijos valdyme. Be to, šiame modulyje pateikiami dokumentai, kuriuos galima atspausdinti per sandėlio valdymą.

Kai siunčiate medžiagas, kurios klasifikuojamos kaip pavojingos prekės, prie siuntų turi būti pridėti papildomi dokumentai. Pavojingų medžiagų funkcijose klientai gali išsaugoti klasifikacijos informaciją ir susieti ją su leidimo prekėmis. Ši informacija gali būti naudojama ruošiant siuntimo dokumentus.

> [!IMPORTANT]
> Pavojingų medžiagų funkcijos „Microsoft Dynamics 365 Supply Chain Management” teikia naudingų produkto informacijos laukų ir susijusių funkcijų kolekciją, kuri gali padėti jums įrašyti ir nurodyti informaciją, susijusią su pavojingais produktais. Šios funkcijos taip pat gali padėti jums kurti ir spausdinti siuntimo dokumentus, kuriuose yra tam tikra informacija apie bet kokias pavojingas medžiagas, kurias siunčiate. Tačiau sistema automatiškai neatitiks visų nuostatų, taikomų jūsų šalyje arba regione. Nors šios priemonės skirtos tam, kad būtų lengviau laikytis bendrųjų nuostatų, jos nėra pakankamos ar garantuotos tokiomis būti. Jūsų organizacija yra atsakinga už visų taikomų nuostatų žinojimą ir visų jų laikymuisi būtinų veiksmų atlikimą.

Kad galėtumėte naudoti šią funkciją, reikia nustatyti šiuos parametrus:

- **Produkto informacijos valdymas:** nustatykite kodus, kurie gali būti taikomi išleistoms prekėms.
- **Sandėlio valdymas:** norėdami spausdinti siuntimo informaciją, naudokite papildomus siuntimo dokumentus.

## <a name="product-information-management"></a>Produkto informacijos valdymas

Produkto informacijos valdyme yra sąrankos lentelių, kuriose galite pridėti nuorodos informaciją, pateikiamą pavojingų prekių sąrašuose, skirtuose kelių, oro ir jūrų transportui.

Čia pateiktos kai kurios dažnai nurodomos nuostatos:

- **ADR** – nuostatos, susijusios su tarptautiniu pavojingų krovinių vežimu keliais
- **CFR 49** – pavojingų krovinių gabenimo Jungtinėse Valstijose nuostatos
- **IMDG** – Tarptautinis jūra gabenamų pavojingų krovinių (IMDG) kodeksas
- **IATA** – Tarptautinės oro transporto asociacijos (IATA) pavojingų prekių gabenimo nuostatos

Kiekviena iš šių nuostatų turi pavojingų prekių sąrašą, kuriame pateikiami nuorodų kodai. Kiekvienos transportavimo rūšies sąrašai sujungiami į bendrai naudojamas tarptautines klasifikacijas. „Supply Chain Management“ pateikia tų sąrašų bendrai naudojamų kodų nuorodų lentelę. Kiekviename sąraše taip pat yra keli unikalūs kodai, kuriuos galima apibrėžti.

Norėdami pirmiausia konfigūruoti šią informaciją, sukurkite nuostatą, kurią galėtumėte naudoti pradiniams parametrams konfigūruoti.

## <a name="warehouse-management"></a>Sandėlio valdymas

Kai ruošiama siunta, galima atspausdinti kelias naujas ataskaitas. Šiose ataskaitose naudojama informacija, nustatyta produkto informacijos valdyme.
