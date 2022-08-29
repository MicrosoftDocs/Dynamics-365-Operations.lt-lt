---
title: Lentelių schemos sveikatos patikros klaidų kodai
description: Šiame straipsnyje aprašomi lentelės būsenos tikrinimo klaidos kodai.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: d3f413f34296fd01da6741bb49658285394cbd17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288767"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Lentelių schemos sveikatos patikros klaidų kodai

[!include [banner](../../includes/banner.md)]



Šiame straipsnyje aprašomi lentelės būsenos tikrinimo klaidos kodai.

## <a name="error-100"></a>Klaida 100

Klaidos pranešimas yra "Minimali reikalaujama finansų ir operacijų platformos versija yra PU 43, norint vykdyti finansų ir operacijų rekomendacijas."

Naudojant šią funkciją reikia 10.0.19 arba vėlesnių finansų ir operacijų programėlių versijos platformos naujinimų.

## <a name="error-400"></a>Klaida 400

Klaidos pranešimas yra " \{Nepavyko rasti objekto finansų ir operacijų UniqueEntityName\} verslo įvykių registracijos duomenų, tai reiškia, kad schema nepa vykdoma arba visi laukų susiejimai yra vienakryptis."

## <a name="error-500"></a>Klaida 500

Klaidos pranešimas "Nerasta projekto \{projekto pavadinimas\} konfigūracijos projektui. Tai gali būti arba projektas neįgalintas, arba visi laukų susiejimai yra vienakryptiai nuo kliento įsipareigojimo iki finansų ir operacijų."

Patikrinkite žemėlapius lentelės žemėlapiui. Jei jie yra vienakryptis nuo klientų įsipareigojimo programėlių iki finansų ir operacijų programėlių, tiesioginis sinchronizavimas iš finansų ir operacijų programėlių į negeneruojamas Dataverse.

## <a name="error-900"></a>Klaida 900

Klaidos pranešimas yra: "Netinkamas objekto finansų ir \{operacijų UniqueEntityName šaltinio \} filtro sourceFilter\{ formatas\}".

Šaltinio filtras, nurodytas finansų ir operacijų programėlių lentelių sąrangoje, nėra teisingas. Norėdami patikrinti filtro kriterijus, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Klaida 1000

Klaidos pranešimas yra " Objekto \{finansų ir operacijų UniqueEntityName\}\{užklausa, naudojama dvigubo rašymo tiesioginį sinchronizavimą yra finansų ir operacijų EntityFilterQueryString \}. Įrašai, kurie atitinka užklausos kriterijus, bus paimti tiesioginiam sinchronizavimui.

Grąžinta objekto užklausa yra objekto atsarginė SQL užklausa. Patikrinkite ar užklausoje nėra vidinių sujungimų ar filtrų, kurie apibrėžia verslo duomenis, išrinktus tiesioginiam sinchronizavimui. Vidinės jungimai ir filtrai yra privalomos sąlygos, kurias reikia įvykdyti kiekvienam įrašui, išrinktam dvigubo rašymo tiesioginiam sinchronizavimui.

## <a name="error-1300"></a>Klaida 1300

Klaidos pranešimas yra: "Virtualiųjų \{laukų s.EntityFieldName\}\{, skirtas objekto finansų ir operacijų EntityMetadata.EntityProperties.LogicalEntityName\} negalima sekti dėl dvigubo rašymo."

Virtualiieji laukai iš finansų ir operacijų lentelių nėra įgalinti sekti. Tiesioginis sinchronizavimas gali sinchronizuoti duomenis, bet negalės pritaikyti stulpeliuose atliktų keitimų.

## <a name="error-1500"></a>Klaida 1500

Klaidos pranešimas yra: "Turi būti bent vienas laukas, susietas ne su klientų įsipareigojimo apžvalgos lauku, kad būtų galima sekti duomenų šaltinį \{duomenų šaltinyje.DataSourceName\}."

Objekto duomenų šaltinyje nėra jokių laukų, susietų su dvigubu rašymu. Dvigubo rašymo metu keitimai pateiktoje lentelėje nebus sekami.

## <a name="error-1600"></a>Klaida 1600

Klaidos pranešimas yra "Duomenų šaltinis: duomenų \{šaltinis. Objekto finansų ir\} operacijų \{DataSourceName.EntityProperties.LogicalEntityName yra\} diapazonas. Tik diapazono sąlygą atitinkantys įrašai yra išrinkti išsiuntimui."

Finansų ir operacijų programėlių objektai gali turėti duomenų šaltinius, kuriuose įjungtas filtrų diapazonas. Šie diapazonai apibrėžia įrašus, išrinktus kaip tiesioginio sinchronizavimo dalis. Jei kai kurie įrašai praleidžiami iš finansų ir operacijų programėlių Dataverse, patikrinkite, ar įrašai atitinka objekto diapazono kriterijus. Paprastas būdas atlikti šią patikrą yra vykdyti SQL užklausą, panašią į pateiktą pavyzdį.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Klaida 1700

Klaidos pranešimas yra: Lentelė: \{datasourceTable.Key.subscribedTableName\} objektui \{datasourceTable.Key.entityName\} sekamas objektui \{origTableToEntityMaps.EntityName\}. Tos pačios sekamos lentelės dėl keletos objektų gali turėti įtakos tiesioginio sinchronizavimo operacijų sistemos našumui.

Jei tą pačią lentelę seka keli objektai, bet kokie lentelės pakeitimas suaktyvins susietų objektų dvigubo rašymo įvertinimą. Nors filtro sąlygos siųs tik galiojančius įrašus, įvertinimas gali sukelti efektyvumo problemų, jei yra ilgalaikių užklausų arba užklausų planų, kurie nėra inicijuoti. Šios problemos verslo atžvilgiu gali nepavykti išvengti. Tačiau, jei tarp kelių objektų yra daug susikertančių lentelių, turėtumėte apsvarstyti objekto supaprastinmą arba objektų užklausų optimizavimo tikrinimą.

## <a name="error-1800"></a>Klaida 1800
Klaidos pranešimas yra: "Duomenų šaltinis: objekto {} CustCustomerV3Entity apima diapazono reikšmę. Gavimo įrašų gavimo į finansus ir operacijas Dataverse gali paveikti objekto diapazono vertės. Patikrinkite finansų ir operacijų Dataverse įrašų, kurie neatitinka filtro kriterijų ir kurie neatitinka jūsų parametrų tikrinimo, atnaujinimus."

Jei finansų ir operacijų programėlėse nurodytas objekto diapazonas, Dataverse gavimo sinchronizavimas nuo finansų ir operacijų programėlių turėtų būti patikrintas dėl įrašų, kurie neatitinka šio diapazono kriterijų, atnaujinimo būdo. Bet kuris įrašas, kuris neatitinka diapazono, laikomas objekto įterpimo operacija. Jei esamo įrašo nėra esamo lentelėje, įterpimo nebus. Rekomenduojame prieš diegiant į gamybą išbandyti šį naudojimo atvejį visiems scenarijams.

## <a name="error-1900"></a>Klaida 1900
Klaidos pranešimas yra "Objektas: turi duomenų {} šaltinius, kurie nėra sekami dėl siunčiamo dvigubo rašymo. Tai gali paveikti tiesioginio sinchronizavimo užklausos našumą. Perdaryti objektą finansuose ir operacijose norint pašalinti nenaudojamus duomenų šaltinius ir lenteles arba įdiegti getEntityRecordIdsImpactedByTableChange, kad optimizuotumėte vykdyklės užklausas."

Jei yra daug duomenų šaltinių, kurių nenaudojama sekant faktinio tiesioginio sinchronizavimo iš finansų ir operacijų programėlių, gali būti, kad objekto našumas gali paveikti tiesioginį sinchronizavimą. Norėdami optimizuoti sekamas lenteles, naudokite metodą getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Klaida 5000
Klaidos pranešimas yra: "Sinchroniniai klaidas registruojami objekto sąskaitų duomenų valdymo įvykiams. Tai gali daryti įtaką pradinio sinchronizavimo ir tiesioginio sinchronizavimo importavimo našumui Dataverse. Kad programa našūs, pakeiskite parametrų į nesinchroninį apdorojimą. Užregistruotų svetainės sąrašas {}."

Sinchroniniai objekto balansai gali paveikti Dataverse tiesioginio sinchronizavimo ir sinchroninio sinchronizavimo našumą, kai jis pridedamas prie operacijos apkrovos. Rekomenduojama arba išjungti balansą, arba padaryti šiuos "async", jei pradinio sinchronizavimo arba tiesioginio sinchronizavimo metu susiduriate su lėtu įkėlimo laiku.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

