---
title: Kliento mokėjimo prognozių naudojimas (peržiūros versija)
description: Šioje temoje kalbama apie būtinuosius komponentus ir bendruosius veiksmus, kurių reikia norint naudoti bandomąją finansinių įžvalgų versiją.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: aa4a4975fc2ccdd91d5beb32060d68f7e77dbcb7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645654"
---
# <a name="use-customer-payment-predictions-preview"></a>Kliento mokėjimo prognozių naudojimas (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip naudoti kliento mokėjimo prognozes. Prieš naudodami šią funkciją įsitikinkite, kad atlikote nustatymo veiksmus. Daugiau informacijos žr. [Klientų mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md).

Kliento mokėjimo prognozes galite peržiūrėti darbo srityje **Klientų kredito ir surinkimo valdymas** ir dviejuose naujuose sąrašų puslapiuose, **Mokėjimo prognozavimas pagal operaciją** ir **Mokėjimo prognozavimas pagal klientą**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Darbo sritis Klientų kredito ir surinkimo valdymas

Darbo sritis **Klientų kredito ir surinkimo valdymas** apima dvi naujas plyteles, **Mokėjimo prognozavimas pagal operaciją** ir **Klientai su prognozuojamais žymaus vėlavimo balansais**.

- Plytelėje **Mokėjimo prognozavimas pagal operaciją** rodomas atidarytų kliento operacijų, kurių mokėjimo tikimybė mažesnė nei 50 procentų talpykloje **Laiku**, skaičių. Galite pasirinkti šią plytelę, kad galėtumėte atidaryti sąrašo puslapį **Mokėjimo prognozavimas pagal operaciją**.
- Plytelėje **Klientai su prognozuojamais žymaus vėlavimo balansais** nurodo klientų, kurių daugiau nei pusė viso likučio (50 procentų) yra numatoma apmokėti per vėluojant ir (arba) žymiai vėluojant, skaičių. Galite pasirinkti šią plytelę, kad galėtumėte atidaryti sąrašo puslapį **Mokėjimo prognozavimas pagal klientą**.

[![Darbo sritis Klientų kredito ir surinkimo valdymas](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Sąrašo puslapis Mokėjimo prognozavimas pagal operaciją

Sąrašo puslapyje **Mokėjimo prognozavimas pagal operaciją** galite peržiūrėti atidarytų operacijų mokėjimo tikimybę talpykloje **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**. Kiekvienoje tinklelio operacijoje stulpelyje **Tikimybė Laiku** rodoma tikimybė, kad SF bus apmokėta iki termino pabaigos datos. Jei dėl tikimybė, kad bus apmokėta laiku, yra mažesnė nei 50 procentų, prie procento, esančio stulpelyje **Tikimybė Laiku**, atsiranda raudonas apskritimas, kad būtų galima nurodyti pavėlavimo apmokėti riziką.

[![Puslapis Mokėjimo prognozavimas pagal operaciją](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Srityje **Susijusi informacija** dešinėje puslapio pusėje rodoma daugiau informacijos apie prognozes.

- Tinklelyje pasirinkus operaciją, „FastTab“ **Mokėjimo prognozė** rodoma išsami informacija apie mokėjimo prognozes talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**. Skiltyje **Svarbiausi veiksniai** pateikiami pagrindiniai veiksniai, lemiantys prognozes. Svarbiausi veiksniai yra pasirinktos operacijos ir (arba) tos operacijos kliento atributai.
- „FastTab“ **Customer Insights** nurodo esamą pasirinktos operacijos kliento SF, mokėjimo ir surinkimo statistiką.
- „FastTab“ **Kliento retrospektyva** rodo kliento mokėjimo retrospektyvą talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.

Duomenys, esantys skiltyje **Svarbiausi veiksniai** ir „FastTab“ **Customer Insights** bei **Klientų retrospektyva**, padeda paaiškinti mokėjimo prognozes. Tai gali padėti padidinti jūsų pasitikėjimą prognozių veiksmingumu.

[![Grafinių duomenų, susijusių su mokėjimais, indikatoriai srityje Susijusi informacija](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Sąrašo puslapis Mokėjimo prognozavimas pagal klientą

Sąrašo puslapyje **Mokėjimo prognozavimas pagal klientą** rodo visą atidarytą balansą ir sumą, kuri, prognozuojama, bus sumokėta talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.

[![Puslapis Mokėjimo prognozavimas pagal klientą](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Kiekvienos talpyklos mokėjimo suma apskaičiuojama kaip operacijos balanso svertinio vidurkio suma. Ši suma skaičiuojama pagal kiekvienos talpyklos mokėjimo tikimybes.

Pavyzdžiui, klientui priskirtos trys atidarytos operacijos, kurių kiekvienoje talpykloje yra šios mokėjimo tikimybės.

| Operacija | Suma | Mokėjimo laiku tikimybė | Mokėjimo pavėlavus tikimybė | Mokėjimo žymiai pavėlavus tikimybė |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 procentų                  | 50 procentų               | 40 procentų                    |
| T2          | 1000  | 50 procentų                  | 30 procentų               | 20 procentų                    |
| T3          | 10,000 | 1 procentų                   | 4 procentų                | 95 procentų                    |

Šiuo atveju kiekvienos talpyklos mokėjimai planuojami, kaip nurodyta toliau.

| Talpyklos   | Operacija T1      | Operacija T2         | Operacija T3            | Bendroji suma |
|-----------|---------------------|------------------------|---------------------------|-------|
| Laiku   | 100 × 10 ÷ 100 = 10 | 1000 × 50 ÷ 100 = 500 | 10 000 × 1 ÷ 100 = 100    | 610   |
| Vėliau      | 100 × 50 ÷ 100 = 50 | 1000 × 30 ÷ 100 = 300 | 10 000 × 4 ÷ 100 = 400    | 750   |
| Labai vėluoja | 100 × 40 ÷ 100 = 40 | 1000 × 20 ÷ 100 = 200 | 10 000 × 95 ÷ 100 = 9500 | 9,740 |

Skiltyje **Susijusi informacija** dešinėje puslapio pusėje rodoma daugiau informacijos apie prognozes.

- Tinklelyje pasirinkus operaciją, „FastTab“ **Mokėjimo prognozė** rodoma išsami informacija apie mokėjimo prognozes talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**. Skiltyje **Svarbiausi veiksniai** pateikiami pagrindiniai veiksniai, lemiantys mokėjimus. Svarbiausi veiksniai yra pasirinktos operacijos ir (arba) tos operacijos kliento atributai.
- „FastTab“ **Customer Insights** nurodo esamą pasirinktos operacijos kliento SF, mokėjimo ir surinkimo statistiką.
- „FastTab“ **Kliento retrospektyva** rodo kliento mokėjimo retrospektyvą talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.

Duomenys, esantys skiltyje **Svarbiausi veiksniai** ir „FastTab“ **Customer Insights** bei **Klientų retrospektyva**, padeda paaiškinti mokėjimo prognozes. Tai gali padėti padidinti jūsų pasitikėjimą prognozių veiksmingumu.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Mokėjimo prognozių tikslinimas

Mokėjimo prognozių tikslumą galite peržiūrėti pasirinkę **Kreditas ir surinkimai \> Sąranka \>Finansinės įžvalgos \> Finansinių įžvalgų parametrai**. Skirtuke **Klientų mokėjimo įžvalgos**, skiltyje **Prognozės modelis** rodomas prognozės modelio tikslumas kaip procentinė dalis.

[![Mokėjimo prognozių tikslumas](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Jei jūsų netenkina tikslumas, pasirinkite saitą **Tikslinti modelį**, kad atidarytumėte „AI Builder“ plėtinio sąsają. Naudodami „AI Builder“ plėtinio sąsają, galite pasirinkti arba atšaukti laukų žymėjimą, kol pasirinksite laukus, kurie, jūsų manymu, yra svarbiausi, norėdami tiksliai prognozuoti mokėjimo tikimybes. Baigę, galite lengvai permokyti numatymo modelį ir publikuoti savo keitimus. Naujai parengtas prognozavimo modelis bus automatiškai naudojamas prognozuojant programoje „Dynamics 365 Finance“.

[![„AI Builder“ plėtinio sąsaja](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Išleidimo informacija

Bandomąją modulio Finansinės įžvalgos viešosios peržiūros versiją galima įdiegti Jungtinėse Amerikos Valstijose, Europoje ir Jungtinėje Karalystėje. „Microsoft“ palaipsniui į palaikomų regionų sąrašą įtraukia daugiau regionų.

Viešosios peržiūros versijos funkcijos gali ir turi būti įjungtos tik 2 pakopos smėlio dėžės aplinkose. Sąrankos ir DI modelių, sukurtų smėlio dėžės aplinkoje, negalima perkelti į gamybos aplinką. Norėdami gauti daugiau informacijos, žr. [„Microsoft Dynamics 365“ peržiūros versijų papildomos naudojimo sąlygos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Privatumo pranešimas

Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.
