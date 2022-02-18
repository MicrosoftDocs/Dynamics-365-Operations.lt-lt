---
title: Lentelių schemos sveikatos patikros klaidų kodai
description: Šis skyrius apibūdina lentelių schemos sveikatos patikros klaidų kodus.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061283"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Lentelių schemos sveikatos patikros klaidų kodai

[!include [banner](../../includes/banner.md)]



Šis skyrius apibūdina lentelių schemos sveikatos patikros klaidų kodus.

## <a name="error-100"></a>Klaida 100

Klaidos pranešimas yra toks: „Minimali reikalinga „Finance and Operations“ platformos versija yra PU 43, kad būtų galima vykdyti „Finance and Operations“ rekomendacijas.

Norint naudoti funkciją, reikia atnaujinti 10.0.19 ar naujesnės versijos „Finance and Operations“ programų platformą.

## <a name="error-400"></a>Klaida 400

Klaidos pranešimas yra „Nerasta subjekto verslo įvykių registracijos duomenų\{ Finance and Operations UniqueEntityName\} Tai reiškia, kad žemėlapis neveikia arba visi lauko žemėlapiai yra vienakrypčiai.

## <a name="error-500"></a>Klaida 500

Klaidos pranešimas "Nerasta projekto \{projekto pavadinimas\} konfigūracijos projektui. Gali būti, kad projektas neįjungtas arba visi lauko atvaizdai yra vienakrypčiai nuo klientų įtraukimo į finansus ir operacijas.

Patikrinkite žemėlapius lentelės žemėlapiui. Jei jie yra vienakrypčiai iš klientų įtraukimo programų į programas „Finance and Operations“, tiesioginiam sinchronizavimui iš „Finance and Operations“ programų srautas negeneruojamas Dataverse.

## <a name="error-900"></a>Klaida 900

Klaidos pranešimas yra „Neteisingas šaltinio filtras\{ šaltinio filtras\} subjekto formatas\{ Finance and Operations UniqueEntityName\} “.

Šaltinio filtras, nurodytas „Finance and Operations“ programų lentelės žemėlapyje, nėra sintaksiškai teisingas. Norėdami patikrinti filtro kriterijus, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Klaida 1000

Klaidos pranešimas yra „Subjektas\{ Finance and Operations UniqueEntityName\} užklausa, naudojama dvigubo rašymo tiesioginiam sinchronizavimui\{ Finance and Operations EntityFilterQueryString \}. Įrašai, kurie atitinka užklausos kriterijus, bus paimti tiesioginiam sinchronizavimui.

Grąžinta objekto užklausa yra objekto atsarginė SQL užklausa. Patikrinkite ar užklausoje nėra vidinių sujungimų ar filtrų, kurie apibrėžia verslo duomenis, išrinktus tiesioginiam sinchronizavimui. Vidinės jungimai ir filtrai yra privalomos sąlygos, kurias reikia įvykdyti kiekvienam įrašui, išrinktam dvigubo rašymo tiesioginiam sinchronizavimui.

## <a name="error-1300"></a>Klaida 1300

Klaidos pranešimas yra „Virtualūs laukai\{ s.EntityFieldName\} subjektui\{ Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} negali būti stebimas dėl dvigubo rašymo.

Virtualūs laukai iš lentelių „Finance and Operations“ neįjungti stebėjimui. Tiesioginis sinchronizavimas gali sinchronizuoti duomenis, bet negalės pritaikyti stulpeliuose atliktų keitimų.

## <a name="error-1500"></a>Klaida 1500

Klaidos pranešimas yra: "Turi būti bent vienas laukas, susietas ne su klientų įsipareigojimo apžvalgos lauku, kad būtų galima sekti duomenų šaltinį \{duomenų šaltinyje.DataSourceName\}."

Objekto duomenų šaltinyje nėra jokių laukų, susietų su dvigubu rašymu. Dvigubo rašymo metu keitimai pateiktoje lentelėje nebus sekami.

## <a name="error-1600"></a>Klaida 1600

Klaidos pranešimas yra „Duomenų šaltinis:\{ duomenų šaltinis.DataSourceName\} subjektui\{ Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} turi diapazoną. Tik diapazono sąlygą atitinkantys įrašai yra išrinkti išsiuntimui."

„Finance and Operations“ programose esantys subjektai gali turėti duomenų šaltinių, kuriuose įgalinti filtrų diapazonai. Šie diapazonai apibrėžia įrašus, išrinktus kaip tiesioginio sinchronizavimo dalis. Jei kai kurie įrašai praleidžiami iš „Finance and Operations“ programų į Dataverse, patikrinkite, ar įrašai atitinka objekto diapazono kriterijus. Paprastas būdas atlikti šią patikrą yra vykdyti SQL užklausą, panašią į pateiktą pavyzdį.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Klaida 1700

Klaidos pranešimas yra: Lentelė: \{datasourceTable.Key.subscribedTableName\} objektui \{datasourceTable.Key.entityName\} sekamas objektui \{origTableToEntityMaps.EntityName\}. Tos pačios sekamos lentelės dėl keletos objektų gali turėti įtakos tiesioginio sinchronizavimo operacijų sistemos našumui.

Jei tą pačią lentelę seka keli objektai, bet kokie lentelės pakeitimas suaktyvins susietų objektų dvigubo rašymo įvertinimą. Nors filtro sąlygos siųs tik galiojančius įrašus, įvertinimas gali sukelti efektyvumo problemų, jei yra ilgalaikių užklausų arba užklausų planų, kurie nėra inicijuoti. Šios problemos verslo atžvilgiu gali nepavykti išvengti. Tačiau, jei tarp kelių objektų yra daug susikertančių lentelių, turėtumėte apsvarstyti objekto supaprastinmą arba objektų užklausų optimizavimo tikrinimą.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
