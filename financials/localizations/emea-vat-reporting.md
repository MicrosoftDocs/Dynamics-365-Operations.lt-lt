---
title: "PVM ataskaitų Europos"
description: "Šioje temoje pateikiama bendra informacija apie nustatymas ir generavimas pridėtinės vertės mokestis (PVM) ataskaita dėl kai kuriose Europos šalyse."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266844
ms.assetid: 06798e29-6140-489e-9b4e-66b45b26be2b
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 84a639b25c64821e00ca4397f42f69298953e599
ms.lasthandoff: 03/31/2017


---

# <a name="vat-reporting-for-europe"></a>PVM ataskaitų Europos

Šioje temoje pateikiama bendra informacija apie nustatymas ir generavimas pridėtinės vertės mokestis (PVM) ataskaita dėl kai kuriose Europos šalyse.

Šioje temoje pateikta bendras požiūris į nustatymas ir generavimas PVM ataskaitą. Šis požiūris yra taikomi vartotojams – juridiniams asmenims šiose šalyse/regionuose:

-   Austrija
-   Belgija
-   Čekijos Respublika
-   Estija
-   Suomija
-   Vokietija
-   Latvija
-   Lietuva
-   Olandija
-   Švedija

## <a name="vat-statement-overview"></a>PVM ataskaitos apžvalga
PVM ataskaitos remiasi mokesčių operacijų sumos. PVM ataskaitos kūrimo procesas yra dalis PVM mokėjimo procesas, kuri įgyvendinama per funkciją nusistovėti ir po PVM. Ši funkcija apskaičiuoja pardavimo mokestis, mokamas už tam tikrą laikotarpį. Sudengimo skaičiavimas yra užregistruotas PVM pasirinkta sudengimo laikotarpio mokesčių operacijų. Apskaičiuoti PVM ataskaitą duomenys: procesas remiasi PVM kodus ir PVM ataskaitų kodus, kur PVM ataskaitų kodai atitinka PVM ataskaitos laukus (arba XML žymes) santykį. Kiekvienas PVM kodas, PVM ataskaitų kodai turėtų būti nustatyti kiekvienos rūšies operacijas, pvz., apmokestinamų prekybos sandorių, apmokestinamų pirkimų, už importą. Aprašytas šios rūšies sandorius su [PVM kodai, PVM ataskaitų](#Sales tax codes for VAT reporting) skyriuje šioje temoje.

Kiekvienas PVM ataskaitos kodą, turėtų būti nustatyta nestandartinį ataskaitos formatą. Be to, PVM kodus yra susiję su konkrečių PVM rinkėjo PVM sudengimo laikotarpius per. Kiekvienas PVM rinkėjui, turėtų būti nustatyta ataskaitos maketas. Taigi, tik PVM ataskaitų kodai patį ataskaitos maketą, nustatomas už PVM rinkėjo PVM sudengimo laikotarpius PVM kodas galima pasirinkti ataskaitos nustatymo, PVM kodas. PVM operacijos sugeneruota komandiruotės įsakymą arba žurnalą yra PVM kodą, PVM šaltinis, PVM kryptis ir balansų (PVM ir mokesčio suma numatytąja valiuta, PVM valiuta ir operacijos valiuta). Remiantis mokesčių operacijų atributų derinys, balansų kurti bendrą sumą PVM ataskaitų kodai nurodyti PVM kodų. Šioje iliustracijoje pateikta duomenų ryšį.

![diagrama](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>PVM ataskaitos nustatymas
Kurti PVM ataskaitą turite nustatyti taip.

### <a name="sales-tax-authorities-for-vat-reporting"></a>PVM rinkėjui skirtas PVM ataskaitą

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Prieš nustatydami PVM ataskaitų kodus, pasirinkite tinkamą ataskaitos maketą PVM rinkėjui. Dėl į **PVM rinkėjus** p., be į **bendrojo** skyrių, pasirinkite a **ataskaitos maketas**. Šis maketas bus naudojamas nustatant PVM ataskaitų kodai.

### <a name="sales-tax-reporting-codes"></a>PVM ataskaitų kodai

PVM ataskaitų kodai yra kodus PVM pareiškimą arba žyma pavadinimuose XML formatu. Šie kodai yra naudojami kaupti ir parengti sumų ataskaita. Kai konfigūruojate elektroninio atsiskaitymo formos PVM ataskaitos, rezultatas sumos pavadinimai bus naudojami. Jūs galite kurti ir tvarkyti PVM ataskaitų kodai ant to **PVM ataskaitų kodai** puslapis. Turite priskirti kiekvieną kodą ataskaitos maketas. Kai sukuriate PVM ataskaitų kodus, galite pasirinkti kodų, kad **ataskaitos nustatymas** skirsnis, **PVM kodus** puslapis. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>PVM kodai, PVM ataskaitos

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).-->Bazinės sumos ir mokesčių sumos sandoriai gali būti subendrinami PVM ataskaitų kodus PVM ataskaitos (XML žymes arba deklaracija dėžės). Jūs galite tai nustatyti susiejant PVM ataskaitų kodai, PVM kodų skirtingus operacijų tipus, **PVM kodus** puslapis. Šioje lentelėje pateikiami ataskaitos nustatymas PVM kodų operacijų tipus. Į skaičiavimus įtrauktos operacijos visų tipų šaltinių, – tik PVM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transaction type</strong></td>
<td><strong>Sandorių ir sumos priskaičiuojamos operacijos tipas Aprašymas</strong></td>
</tr>
<tr class="even">
<td><strong>Apmokestinami pardavimai</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra pasirinktame laikotarpyje /</li>
<li>Pardavimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>mokėtinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Neapmokestinami pardavimai</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pardavimas yra eksporto (<strong>mokesčių kryptimi</strong> yra <strong>neapmokestinami pardavimai</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax payable</strong></td>
<td>Suma <strong>mokesčių sumos</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pardavimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>mokėtinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable sales credit note</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pardavimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>mokėtinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Fakso atleisti pard.</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pardavimas yra eksporto (<strong>mokesčių kryptimi</strong> yra <strong>neapmokestinami pardavimai</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on sales credit note</strong></td>
<td>Suma <strong>mokesčių sumos</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pardavimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>mokėtinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable purchases</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pirkimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free purchase</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pirkimas yra importo (<strong>mokesčių kryptimi</strong> yra <strong>Neapmokestinami pirkimai</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax receivable</strong></td>
<td>Suma <strong>mokesčių sumos</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pirkimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable purchase credit note</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pirkimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tax exempt purchase credit note</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pirkimas yra importo (<strong>mokesčių kryptimi</strong> yra <strong>Neapmokestinami pirkimai</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on purchase credit note</strong></td>
<td>Suma <strong>mokesčių sumos</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Pirkimas yra vidaus (<strong>mokesčių kryptimi</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li><strong>Mokesčių kryptimi</strong> yra <strong>naudoti mokesčių</strong></li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import</strong></td>
<td>Atšaukta suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li><strong>Mokesčių kryptimi</strong> yra <strong>naudoti mokesčių</strong>.</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import credit note</strong></td>
<td>Suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
e<li><strong>Mokesčių kryptimi</strong> yra <strong>naudoti mokesčių</strong>.</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import credit note</strong></td>
<td>Atšaukta suma <strong>mokesčių bazės sumas</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li>Kryptis yra <strong>naudoti mokesčių</strong>.</li>
d<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Use tax</strong></td>
<td>Suma <strong>mokesčių sumos</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li><strong>Mokesčių kryptimi</strong> yra <strong>naudoti mokesčių</strong>.</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset use tax</strong></td>
<td>Atšaukta suma <strong>mokesčių sumos</strong> mokesčių operacijų, kurios atitinka šias sąlygas:
<ul>
<li>Operacijos data yra per pasirinktą laikotarpį.</li>
<li><strong>Mokesčių kryptimi</strong> yra <strong>naudoti mokesčių</strong>.</li>
<li>Operacija <strong>PVM</strong> ar <strong>mokesčio suma</strong>&gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Už pirmiau pateiktoje lentelėje, daroma prielaida, kad laikomasi šių kriterijų: 
> -   PVM yra operacijos suma nuo to **kilmės apskaitos valiuta** srityje.
> -   Mokesčio suma yra perėjimas nuo to **tikrasis PVM suma numatytąja valiuta** srityje.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigūruoti ER modelio ir ataskaitų formos

Elektroninių ataskaitų (ER) galite konfigūruoti ataskaitas ir ataskaitą ir eksportuoti duomenis elektroninių formatų nekeičiant X ++ kodą. Papildoma informacija:

-   [Elektroninių ataskaitų apžvalga](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Lokalizacijos reikalavimus – sukurti GER konfigūraciją](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>Countryspecific išteklių dėl PVM ataskaitas
Kiekvienos šalies PVM ataskaitos turi atitikti šalies teisės aktų reikalavimus. Yra iš anksto nustatytas bendras modelių ir dėl šioje lentelėje išvardintų šalių PVM ataskaitų formos.


| Šalis        | Papildoma informacija                                                          |
|----------------|---------------------------------------------------------------------------------|
| Austrija        |  [PVM ataskaitos duomenys Austrijos](emea-aut-vat-statement-details.md)         |
| Belgija        |                                                                                 |
| Čekijos Respublika |  [PVM ataskaita detalių, Čekija](emea-cze-vat-statement-details.md)   |
| Estija        |  [PVM ataskaitos duomenys Estijai](emea-est-vat-statement-details.md) |
| Suomija        |                                                                                 |
| Vokietija        |                                                                                 |
| Italija          | [PVM ataskaitos duomenys Italijoje](emea-ita-vat-statements-details.md)            |
| Latvija         | [PVM ataskaitos duomenys Latvijai](emea-lva-vat-statement-details.md)           |
| Lietuva      | [PVM ataskaitos duomenys Lietuvai](emea-ltu-vat-statement-details.md)         |
| Olandija    |                                                                                 |
| Švedija         |                                                                                 |




