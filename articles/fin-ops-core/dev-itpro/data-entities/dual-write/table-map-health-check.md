---
title: Lentelių schemos sveikatos patikros klaidų kodai
description: Šis skyrius apibūdina lentelių schemos sveikatos patikros klaidų kodus.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 4f0b92a6bc6c051a6bb24b49d3280ca5ecea3625
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725080"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Lentelių schemos sveikatos patikros klaidų kodai

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šis skyrius apibūdina lentelių schemos sveikatos patikros klaidų kodus.

## <a name="error-100"></a>Klaida 100

Klaidos pranešimas yra "Minimali būtina Finance and Operations platformos versija yra PU 43, norint vykdyti Finance and Operations rekomendacijas".

Naudojant šią funkciją reikia 10.0.19 arba vėlesnių programėlių versijos platformos Finance and Operations naujinimų.

## <a name="error-400"></a>Klaida 400

Klaidos pranešimas yra "Nerasta jokių įvykių registracijos duomenų objektui \{Finance and Operations UniqueEntityName\}, tai reiškia kad arba neveikia žemėlapis arba visų laukų susiejimai yra vienakrypčiai."

## <a name="error-500"></a>Klaida 500

Klaidos pranešimas "Nerasta projekto \{projekto pavadinimas\} konfigūracijos projektui. Tai gali būti arba projektas neįgalintas, arba visi laukų susiejimai yra vienakrypčiai nuo klientų įsitraukimo į Finance and Operations."

Patikrinkite žemėlapius lentelės žemėlapiui. Jei jie yra vienakrypčiai nuo klientų įsitraukimo programėlių iki Finance and Operations programėlių, tuomet tiesioginis sinchronizavimas iš Finance and Operations programėlės nėra generuojamas į Dataverse.

## <a name="error-900"></a>Klaida 900

Klaidos pranešimas yra: "Netinkamas šaltinio filtro \{sourceFilter\} formatas objektui \{Finance and Operations UniqueEntityName\}."

Šaltinio filtras, nurodytas lentelių žemėlapyje Finance and Operations programėlėje nėra sintaksiškai teisingas. Norėdami patikrinti filtro kriterijus, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Klaida 1000

Klaidos pranešimas yra, "Objekto \{Finance and Operations UniqueEntityName\} užklausa, naudojama dvigubo rašymo tiesioginio sinchronizavimo atveju, yra \{Finance and Operations EntityFilterQueryString\}. Įrašai, kurie atitinka užklausos kriterijus, bus paimti tiesioginiam sinchronizavimui.

Grąžinta objekto užklausa yra objekto atsarginė SQL užklausa. Patikrinkite ar užklausoje nėra vidinių sujungimų ar filtrų, kurie apibrėžia verslo duomenis, išrinktus tiesioginiam sinchronizavimui. Vidinės jungimai ir filtrai yra privalomos sąlygos, kurias reikia įvykdyti kiekvienam įrašui, išrinktam dvigubo rašymo tiesioginiam sinchronizavimui.

## <a name="error-1300"></a>Klaida 1300

Klaidos pranešimas yra: "Virtualieji laukai \{s.EntityFieldName\} skirti objektui \{Finance and Operations entityMetadata.EntityProperties.LogicalEntityName\}  gali nebūti sekami dvigubam rašymui".

Virtualūs laukai iš Finance and Operations lentelių nėra įgalinti sekimui. Tiesioginis sinchronizavimas gali sinchronizuoti duomenis, bet negalės pritaikyti stulpeliuose atliktų keitimų.

## <a name="error-1500"></a>Klaida 1500

Klaidos pranešimas yra: "Turi būti bent vienas laukas, susietas ne su klientų įsipareigojimo apžvalgos lauku, kad būtų galima sekti duomenų šaltinį \{duomenų šaltinyje.DataSourceName\}."

Objekto duomenų šaltinyje nėra jokių laukų, susietų su dvigubu rašymu. Dvigubo rašymo metu keitimai pateiktoje lentelėje nebus sekami.

## <a name="error-1600"></a>Klaida 1600

Klaidos pranešimas yra "Duomenų šaltinis: \{datasource.DataSourceName\} objektui \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} turi diapazoną. Tik diapazono sąlygą atitinkantys įrašai yra išrinkti išsiuntimui."

Objektai Finance and Operations programėlėse gali turėti duomenų šaltinius, kuriuose įgalinami filtrų diapazonai. Šie diapazonai apibrėžia įrašus, išrinktus kaip tiesioginio sinchronizavimo dalis. Jei kai kurie įrašai praleidžiami iš Finance and Operations programėlių į Dataverse, patikrinkite, ar įrašai atitinka objekto diapazono kriterijus. Paprastas būdas atlikti šią patikrą yra vykdyti SQL užklausą, panašią į pateiktą pavyzdį.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Klaida 1700

Klaidos pranešimas yra: Lentelė: \{datasourceTable.Key.subscribedTableName\} objektui \{datasourceTable.Key.entityName\} sekamas objektui \{origTableToEntityMaps.EntityName\}. Tos pačios sekamos lentelės dėl keletos objektų gali turėti įtakos tiesioginio sinchronizavimo operacijų sistemos našumui.

Jei tą pačią lentelę seka keli objektai, bet kokie lentelės pakeitimas suaktyvins susietų objektų dvigubo rašymo įvertinimą. Nors filtro sąlygos siųs tik galiojančius įrašus, įvertinimas gali sukelti efektyvumo problemų, jei yra ilgalaikių užklausų arba užklausų planų, kurie nėra inicijuoti. Šios problemos verslo atžvilgiu gali nepavykti išvengti. Tačiau, jei tarp kelių objektų yra daug susikertančių lentelių, turėtumėte apsvarstyti objekto supaprastinmą arba objektų užklausų optimizavimo tikrinimą.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
