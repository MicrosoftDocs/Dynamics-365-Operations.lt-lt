---
title: Kaina Power BI turinio valdymas
description: "Šioje temoje aprašoma, kas įeina į išlaidų valdymą Power BI turinį. Jis paaiškina, kaip jas pasiekti Power BI ir pateikia informaciją apie duomenų modelio ir subjektai, kurie yra naudojami kurti turinį."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Kaina Power BI turinio valdymas

Šioje temoje aprašoma, kas įeina į išlaidų valdymą Power BI turinį. Jis paaiškina, kaip jas pasiekti Power BI ir pateikia informaciją apie duomenų modelio ir subjektai, kurie yra naudojami kurti turinį.

# <a name="overview"></a>Apžvalga

Pagal **išlaidų valdymo** Microsoft Power BI turinys yra skirtas atsargų apskaitininkų arba organizacijoje asmenys, kurie yra atsakingi už atsargų. Pagal **išlaidų valdymo** Power BI turinys suteikia vadybinių įžvalgų atsargų ir work in pažangą (NG) atsargas ir kaip išlaidų srautai per jas pagal kategorijas per tam tikrą laiką. Informaciją taip pat galima kaip išsamios finansinės ataskaitos priedas.

## <a name="key-measures"></a>Pagrindinės priemonės

+ Pradinis balansas
+ Pabaigos likutis
+ Grynasis pokytis
+ Grynasis pokytis %
+ Skirstymas pagal terminus

## <a name="key-performance-indicators"></a>Pagrindiniai efektyvumo indikatoriai
+ Atsargų apyvarta
+ Atsargų tikslumas

CostAggregatedCostStatementEntryEntity pagrindinis duomenų šaltinis yra CostStatementCache lentelėje. Šioje lentelėje yra valdoma pagal duomenų rinkinio talpyklą. Pagal numatytuosius nustatymus lentelėje atnaujinama kas 24 valandas, tačiau taip pat galima rankiniu būdu atnaujinimus duomenų talpyklos konfigūracijos. Tada galite padaryti rankiniu būdu atnaujinti pagal **išlaidų valdymo** ar **išlaidų analizė** darbo srities. Paleidus CostStatementCache naujinimą, turite atnaujinti OData ryšio energiją BI.com pamatyti atnaujintus duomenis svetainėje. Dispersija (pirkimo, gamybos) priemonių, Power BI turinį yra susijusios tik su prekėmis, kurios yra vertinama normatyvinės savikainos metodu, atsargų. Gamybos dispersija apskaičiuojama kaip skirtumas tarp aktyvų sąnaudų ir įvykdytų išlaidų. Gamybos nuokrypis apskaičiuojamas, kai gamybos užsakymo būsena iš **baigta**. Daugiau informacijos apie gamybos dispersija rūšių ir kaip apskaičiuoti kiekvieno tipo, rasite [apie analizuojant dispersijos gamybos užsakymo](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Naudotis prieigos prie turinio Power BI
Pagal **išlaidų valdymo** Power BI turinys yra PowerBI.com. Daugiau informacijos apie tai, kaip prisijungti ir įkelti jūsų Microsoft Dynamics 365 operacijų duomenis, rasite [turinio prieigos Power BI PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Rodikliai, kurie yra įtraukti į Power BI turinys
Turinys apima ataskaitų puslapių rinkinį. Kiekviename puslapyje sudaro metriką, kuri yra ryškinamos diagramas, plytelės ir lentelių rinkinys. Toliau pateiktoje lentelėje apžvelgiama, vizualizacijos, pagal **išlaidų valdymo** Power BI turinį.

| Ataskaitų puslapio | Diagramos | Pareigos |
|---|---|---|
|Atsargų bendrą (numatytasis iš dabartinio laikotarpio) |Tikslumas |Atsargos priemones:<br>Atsargų, galutinis likutis<br>Grynojo atsargų pokyčio<br>Atsargų grynasis pokytis %<br>|
| |Atsargų apyvarta | |
| |Galutinis likutis iš išteklių grupės atsargų | |
| |Atsargų grynąjį pokytį iš kategorijos pavadinimas 1 lygio ir 2 lygio kategorijos pavadinimas| |
| |Pirkimo dispersijos išteklių grupės ir kategorijos pavadinimas 3 lygio | |
|Atsargų pagal svetainės (numatytasis iš dabartinio laikotarpio) |Galutinis likutis iš svetainės pavadinimą ir išteklių grupės atsargų | |
| |Atsargų funkciją svetainės pavadinimą ir išteklių grupės | |
| |Galutinis likutis iš miesto ir išteklių grupės atsargų | |
|Atsargų pagal išteklių grupės (numatytasis iš dabartinio laikotarpio) |Atsargos priemonės | |
| |Atsargų tikslumas suma pagal išteklių grupes | |
| |Atsargų pasuktas sumos iš išteklių grupė | |
|Atsargų YOY (numatytasis einamųjų metų prieš praėjusių metų) |Atsargos priemonės | |
| |Atsargų KPI:<br>Atsargų apyvarta<br>Atsargų tikslumas | |
| |Galutinis likutis metų ir išteklių grupės atsargų | |
| |Pirkimo dispersijos metų ir kategorijos pavadinimas lygis 3 | |
|Atsargų senėjimas (įsipareigojimų einamųjų metų) |Atsargų senėjimo kvartalo ir išteklių grupės | |
| |Atsargų senėjimo kvartalo ir svetainės pavadinimas | |
|Vykdomo projekto bendrą (numatytasis iš dabartinio laikotarpio) |Vykdomo projekto grynosios pakeisti kategorijos pavadinimas 1 lygio ir 2 lygio kategorijos pavadinimas |Darbai nebaigtų darbų priemones:<br>Vykdomo projekto pabaigos balansas<br>Vykdomo projekto grynasis pokytis<br>Vykdomo projekto grynasis pokytis %<br> |
| |Gamybos dispersijos išteklių grupės ir kategorijos pavadinimas 3 lygio | |
| |Vykdomo projekto grynasis pokytis, išteklių grupės | |
|Nebaigtų darbų site (numatytasis iš dabartinio laikotarpio) |Darbai nebaigtos gamybos priemonių | |
| |Vykdomo projekto grynosios pakeisti svetainės pavadinimą ir kategorijos pavadinimas 2 lygio | |
| |Gamybos dispersijos svetainės pavadinimą ir 3 lygio kategorijos pavadinimas | |

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Dinamika 365 operacijų duomenys yra naudojamas užpildyti ataskaitos puslapius pagal **išlaidų valdymo** Power BI turinį. Šie duomenys yra vaizduojamas kaip bendra matavimų, kurie yra pastatytas įmonės parduotuvėje, kuri yra "Microsoft" SQL duomenų bazę, kuri yra optimizuota Google analytics. Daugiau informacijos rasite [apžvalga, Power BI integracija su įmonės parduotuvė](power-bi-integration-entity-store.md). Šie pagrindiniai bendra matavimai naudojami turinio pagrindu.

| Objektas            | Pagrindinis bendras matavimo | Duomenų šaltinis Dynamics 365 operacijoms | Laukas             | aprašymas                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Ataskaitoje įrašai | Grynasis pokytis                | CostAggregatedCostStatementEntryEntity      | Suma (\[sumos\])   | Suma numatytąja valiuta |
| Ataskaitoje įrašai | Pakitimų neto kiekis       | CostAggregatedCostStatementEntryEntity      | Suma (\[kiekis\]) |                                   |

Ši lentelė parodo, kaip pagrindinis bendras matavimai naudojami sukurti keletą apskaičiuotus matavimus ir turinio duomenų rinkinyje.

| Mato vnt.                                 | Kaip apskaičiuojamas priemonė                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pradinis balansas                       | \[Galutinis likutis\]-\[grynasis pokytis\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Pradžioje likučio kiekis              | \[Pabaigos likučio kiekis\]-\[Net pakeisti kiekį\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Pabaigos likutis                          | SKAIČIUOTI (suma (\[suma\]), filtras (ALLEXCEPT ("Finansų kalendoriai", "Finansų kalendoriai"\[LedgerRecId\], "ūkio subjektų"\[ID\], "ūkio subjektų"\[pavadinimas\], "Žurnalai"\[valiutos\], 'DK'\[Aprašymas\], 'DK'\[pavadinimas\]), "Finansų kalendoriai"\[data\]&lt;= MAX ("Finansų kalendoriai"\[dienos\])))                                                                                                                                                                                           |
| Pabaigos likučio kiekis                 | SKAIČIUOTI (suma (\[kiekis\]), filtras (ALLEXCEPT ("Finansų kalendoriai", "Finansų kalendoriai"\[LedgerRecId\], "ūkio subjektų"\[ID\], "ūkio subjektų"\[pavadinimas\], 'DK'\[valiutos\], 'DK'\[Aprašymas\], "Žurnalai"\[pavadinimas\]), "Finansų kalendoriai"\[data\]&lt;= MAX ("Finansų kalendoriai"\[dienos\])))                                                                                                                                                                                         |
| Atsargų, pradinis likutis             | SKAIČIUOTI (\[pradinis likutis\], 'Ataskaitoje įrašai'\[sakinio tipo\] = "Atsargos")                                                                                                                                                                                                                                                                                                                                                                                      |
| Atsargų, galutinis likutis                | SKAIČIUOTI (\[galutinis likutis\], 'Ataskaitoje įrašai'\[sakinio tipo\] = "Atsargos")                                                                                                                                                                                                                                                                                                                                                                                         |
| Grynojo atsargų pokyčio                    | SKAIČIUOTI (\[grynasis pokytis\], 'Ataskaitoje įrašai'\[sakinio tipo\] = "Atsargos")                                                                                                                                                                                                                                                                                                                                                                                             |
| Atsargų pakitimų neto kiekis           | SKAIČIUOTI (\[grynojo pokyčio kiekis\], 'Ataskaitoje įrašai'\[sakinio tipo\] = "Atsargos")                                                                                                                                                                                                                                                                                                                                                                                    |
| Atsargų grynasis pokytis %                  | Jei (\[atsargų pabaigos balansas\] = 0, 0, \[inventorinio kiekio pakitimų neto\] / \[atsargų pabaigos balansas\])                                                                                                                                                                                                                                                                                                                                                                           |
| Atsargų paversti suma                | Jei (arba (\[atsargų vidutinis likutis\]&lt;= 0, \[atsargų parduoti ar suvartoti klausimais\]&gt;= 0), 0, ABS (\[atsargų parduoti ar suvartoti klausimais\]) /\[atsargų vidutinis likutis\])                                                                                                                                                                                                                                                                                                  |
| Vidutinis atsargų likutis               | (\[Atsargų pabaigos balansas\] + \[atsargų pradžios likutis\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Atsargų parduoti ar suvartoti klausimais       | \[Parduotos atsargos\] + \[atsargos sunaudotos medžiagų savikaina\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Atsargos sunaudotos medžiagų savikaina        | SKAIČIUOTI (\[inventorinio kiekio pakitimų neto\], 'Ataskaitoje įrašai'\[kategorijos pavadinimas - 2 lygio\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Parduotos atsargos                          | SKAIČIUOTI (\[inventorinio kiekio pakitimų neto\], 'Ataskaitoje įrašai'\[kategorijos pavadinimas - 2 lygio\_\] = "Pardavėjas")                                                                                                                                                                                                                                                                                                                                                                             |
| Atsargų tikslumas suma            | Jei (\[atsargų pabaigos balansas\]&lt;= 0, jei (arba (\[atsargų apskaičiuota suma\]&lt;&gt; 0, \[atsargų pabaigos balansas\]&lt; 0), 0, 1), MAX (0, (\[atsargų pabaigos balansas\] -ABS (\[atsargų apskaičiuota suma\])) /\[atsargų pabaigos balansas\]))                                                                                                                                                                                                                              |
| Atsargų, apskaičiuota suma                | SKAIČIUOTI (\[inventorinio kiekio pakitimų neto\], 'Ataskaitoje įrašai'\[kategorijos pavadinimas - 3 lygio\_\] = "Inventorizacija")                                                                                                                                                                                                                                                                                                                                                                         |
| Atsargų skirstymas pagal terminus                         | Jei (ISBLANK (maks ("Finansų kalendoriai"\[dienos\])), blank(), MAX (0, MIN (\[atsargų senėjimo pažymų kiekį\], \[atsargų senėjimas pabaigos likučio kiekis\] - \[atsargų senėjimo pažymų kiekį ateityje\]))) \*\[atsargų avg vieneto savikaina\]                                                                                                                                                                                                                                |
| Atsargų senėjimas kvitų kiekis       | Jei (\[minDate\] = \[minDateAllSelected\], skaičiuoti (\[inventorinio kiekio pakitimų neto kiekis\], "Ataskaitoje įrašai"\[kiekis\]&gt; 0, filtras (ALLEXCEPT ("Finansų kalendoriai", "Finansų kalendoriai"\[LedgerRecId\], "ūkio subjektų"\[ID\], "ūkio subjektų"\[pavadinimas\], 'DK'\[valiutos\], "Žurnalai"\[Aprašymas\], 'DK'\[pavadinimas\]), "Finansų kalendoriai"\[data\]&lt;= MAX ("Finansų kalendoriai"\[dienos\]))), skaičiuoti (\[inventorinio kiekio pakitimų neto kiekis\], "Ataskaitoje įrašai"\[kiekis\]&gt; 0)) |
| Senėjimo atsargų pabaigos likučio kiekis | \[Atsargų pabaigos likučio kiekis\] + skaičiuoti (\[inventorinio kiekio pakitimų neto kiekis\], filtras (ALLEXCEPT ("Finansų kalendoriai", "Finansų kalendoriai"\[LedgerRecId\], "ūkio subjektų"\[ID\], "ūkio subjektų"\[pavadinimas\], "Žurnalai"\[valiutos\], 'DK'\[Aprašymas\], 'DK'\[pavadinimas\]), "Finansų kalendoriai"\[data\]&gt; maks ("Finansų kalendoriai"\[dienos\])))                                                                                                                                 |
| Atsargų senėjimo pajamas ateityje  | SKAIČIUOTI (\[inventorinio kiekio pakitimų neto\], "Ataskaitoje įrašai"\[suma\]&gt; 0, filtras (ALLEXCEPT ("Finansų kalendoriai", "Finansų kalendoriai"\[LedgerRecId\], "ūkio subjektų"\[ID\], "ūkio subjektų"\[pavadinimas\], 'DK'\[valiutos\], "Žurnalai"\[Aprašymas\], 'DK'\[pavadinimas\]), "Finansų kalendoriai"\[data\]&gt; MAX ("Finansų kalendoriai"\[dienos\])))                                                                                                                                             |
| Atsargų avg vieneto savikaina                 | SKAIČIUOTI (\[atsargų pabaigos balansas\] / \[atsargų pabaigos likučio kiekis\], ALLEXCEPT ("Finansų kalendoriai", "Finansų kalendoriai"\[LedgerRecId\], "ūkio subjektų"\[ID\], "ūkio subjektų"\[pavadinimas\], 'DK'\[valiuta\], 'DK'\[Aprašymas\], 'DK'\[pavadinimas\]))                                                                                                                                                                                                                 |
| Pirkimo dispersijos                      | SKAIČIUOTI (suma (\[suma\]), "Ataskaitoje įrašai"\[kategorijos pavadinimas - 2 lygio\_\] = "Procured", 'Ataskaitoje įrašai'\[sakinio tipo\] = "Nukrypimas")                                                                                                                                                                                                                                                                                                                              |
| Nebaigtų darbų pradžios balansas                   | SKAIČIUOTI (\[pradinis likutis\], 'Ataskaitoje įrašai'\[sakinio tipo\] = "Vykdomas projektas")                                                                                                                                                                                                                                                                                                                                                                                            |
| Vykdomo projekto pabaigos balansas                      | SKAIČIUOTI (\[galutinis likutis\], 'Ataskaitoje įrašai'\[sakinio tipo\] = "Vykdomas projektas")                                                                                                                                                                                                                                                                                                                                                                                               |
| Vykdomo projekto grynasis pokytis                          | SKAIČIUOTI (\[grynasis pokytis\], 'Ataskaitoje įrašai'\[sakinio tipo\] = "Vykdomas projektas")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Vykdomo projekto grynasis pokytis %                        | Jei (\[ng, galutinis likutis\] = 0, 0, \[ng grynasis pokytis\] / \[ng galutinis likutis\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Gamybos dispersijos                    | SKAIČIUOTI (suma (\[suma\]), "Ataskaitoje įrašai"\[kategorijos pavadinimas - 2 lygio\_\] = "ManufacturedCost", 'Ataskaitoje įrašai'\[sakinio tipo\] = "Nukrypimas")                                                                                                                                                                                                                                                                                                                      |
| Kategorijos pavadinimas - 1 lygis                 | Perjungti (\[kategorijos pavadinimas - 1 lygio\_\], "Nė vienas", "Niekas", "NetSourcing", "Grynoji apsirūpinimo", "NetUsage", "Grynasis naudojimo", "NetConversionCost", "Grynasis konvertavimo kaina", "NetCostOfGoodsManufactured", "Grynoji pagamintų prekių savikainą", "BeginningBalance", "Pradinis likutis")                                                                                                                                                                                                         |
| Kategorijos pavadinimas - 2 lygis                 | Perjungti (\[kategorijos pavadinimas - 2 lygio\_\], "Nė vienas", "Nėra", "Procured", "Procured", "Disposed", "Disposed", "Perkeltas", "Perkeltas", "Pardavėjas", "Pardavėjas", "ConsumedMaterialsCost", "Sunaudotos žaliavos", "ConsumedManufacturingCost", "Sunaudotos gamybos kaštus", "ConsumedOutsourcingCost", "Suvartotas užsakomųjų paslaugų kaina", "ConsumedIndirectCost", "Suvartota netiesioginės išlaidos", "ManufacturedCost", "Pagaminimo kaina", "Dispersijos", "Dispersijos")                            |
| Kategorijos pavadinimas - lygis 3                 | Perjungti (\[kategorijos pavadinimas - 3 lygio\_\], "Nė vienas", "Niekas", "Skaičiavimas", "Niekas", "ProductionPriceVariance", "Pagaminimo kaina", "QuantityVariance", "Kiekis", "SubstitutionVariance", "Pakeitimo", "ScrapVariance", "Laužas", "LotSizeVariance", "Lotas", "RevaluationVariance", "Perkainojimo", "PurchasePriceVariance", "Pirkimo kainą", "CostChangeVariance", "Sąnaudų kaita", "RoundingVariance", "Apvalinimo nukrypimas")                                                   |

Pagrindiniai matmenys yra naudojamas kaip filtrų Supjaustykite bendra matavimų pasiekti didesnio detalumo ir suteikia gilesnių analitinių įžvalgų.

| Objektas           | Atributų pavyzdžiai                       |
|------------------|----------------------------------------------|
| Objektai         | ID, pavadinimas                                     |
| Finansiniai kalendoriai | Kalendorius, mėnesio, metų ketvirčio laikotarpiu,       |
| KPI tikslai        | Atsargų tikslumas tikslas, atsargų paversti tikslas |
| Didžiosios knygos          | Valiuta, pavadinimas, Aprašymas                  |
| Vietos            | ID, pavadinimas, šalis, miestas                      |

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)



