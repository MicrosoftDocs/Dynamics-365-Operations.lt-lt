---
title: Kliento mokėjimo prognozių naudojimas
description: Šioje temoje kalbama apie būtinuosius komponentus ir bendruosius veiksmus, kurių reikia norint naudoti bandomąją „Finance insights” versiją.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 0606118007c01fc21c2c61d2128a7ec014617fcc
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752789"
---
# <a name="use-customer-payment-predictions"></a>Kliento mokėjimo prognozių naudojimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip naudoti kliento mokėjimo prognozes. Prieš naudodami šią funkciją įsitikinkite, kad atlikote nustatymo veiksmus. Daugiau informacijos žr. [Klientų mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md).

Kliento mokėjimo numatymas galite peržiūrėti darbo srityje Valdyti kliento kreditą ir mokėjimų priežiūros darbo sritį ir dviejuose naujuose sąrašo puslapiuose: operacijos mokėjimo numatymų ir kliento **·** mokėjimo **·** **numatymų**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Darbo sritis Klientų kredito ir surinkimo valdymas

Kliento **kredito ir mokėjimų valdymo darbo srityje yra dvi naujos prognozės: operacijos mokėjimo** **numatymas** ir kliento mokėjimų **numatymas.**

### <a name="transaction-payment-predictions-list-page"></a>Operacijos mokėjimo numatymų sąrašo puslapis

Operacijų mokėjimo numatymų sąrašo puslapyje galite peržiūrėti atvirų operacijų mokėjimo tikimybę laiku, pavėluotai ir **·** labai **·** **·** **·** pavėluotai. Kiekvienoje tinklelio operacijoje stulpelyje **Tikimybė Laiku** rodoma tikimybė, kad SF bus apmokėta iki termino pabaigos datos. Jei dėl tikimybė, kad bus apmokėta laiku, yra mažesnė nei 50 procentų, prie procento, esančio stulpelyje **Tikimybė Laiku**, atsiranda raudonas apskritimas, kad būtų galima nurodyti pavėlavimo apmokėti riziką.

[![ Puslapis Mokėjimo prognozavimas pagal operaciją.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Srityje **Susijusi informacija** dešinėje puslapio pusėje rodoma daugiau informacijos apie prognozes.

- Tinklelyje pasirinkus operaciją, „FastTab“ **Mokėjimo prognozė** rodoma išsami informacija apie mokėjimo prognozes talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**. Skiltyje **Svarbiausi veiksniai** pateikiami pagrindiniai veiksniai, lemiantys prognozes. Svarbiausi veiksniai yra pasirinktos operacijos ir (arba) tos operacijos kliento atributai.
- „FastTab“ **Customer Insights** nurodo esamą pasirinktos operacijos kliento SF, mokėjimo ir surinkimo statistiką.
- „FastTab“ **Kliento retrospektyva** rodo kliento mokėjimo retrospektyvą talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.

Duomenys, esantys skiltyje **Svarbiausi veiksniai** ir „FastTab“ **Customer Insights** bei **Klientų retrospektyva**, padeda paaiškinti mokėjimo prognozes. Tai gali padėti padidinti jūsų pasitikėjimą prognozių veiksmingumu.

[![ Grafinių duomenų, susijusių su mokėjimais, indikatoriai srityje Susijusi informacija.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Kliento mokėjimo numatymų sąrašo puslapis

Kliento mokėjimo numatymų sąrašo puslapyje rodomas bendras atviras balansas, numatyta sumokėti laiku, pavėluotai ir **·** labai **·** **·** **·** pavėluotai sumokėti suma.

[![ Puslapis Mokėjimo prognozavimas pagal klientą.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

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

- Tinklelyje pasirinkus operaciją, „FastTab“ **Mokėjimo prognozė** rodoma išsami informacija apie mokėjimo prognozes talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.
- „FastTab“ **Customer Insights** nurodo esamą pasirinktos operacijos kliento SF, mokėjimo ir surinkimo statistiką.
- „FastTab“ **Kliento retrospektyva** rodo kliento mokėjimo retrospektyvą talpyklose **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.

Klientų žinių ir **kliento retrospektyvos** **·** "FastTabs" duomenys padeda paaiškinti mokėjimo numatymes. Tai gali padėti padidinti jūsų pasitikėjimą prognozių veiksmingumu.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Mokėjimo prognozių tikslinimas

Mokėjimo prognozių tikslumą galite peržiūrėti pasirinkę **Kreditas ir surinkimai \> Sąranka \> „Finance Insights” \> „Finance Insights” parametrai**. Skirtuke **Klientų mokėjimo įžvalgos**, skiltyje **Prognozės modelis** rodomas prognozės modelio tikslumas kaip procentinė dalis.

[![ Mokėjimo prognozių tikslumas.](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Jei jūsų netenkina tikslumas, pasirinkite saitą **Tikslinti modelį**, kad atidarytumėte „AI Builder“ plėtinio sąsają. Naudodami „AI Builder“ plėtinio sąsają, galite pasirinkti arba atšaukti laukų žymėjimą, kol pasirinksite laukus, kurie, jūsų manymu, yra svarbiausi, norėdami tiksliai prognozuoti mokėjimo tikimybes. Baigę, galite lengvai permokyti numatymo modelį ir publikuoti savo keitimus. Naujai parengtas prognozavimo modelis bus automatiškai naudojamas prognozuojant programoje „Dynamics 365 Finance“.

[![„AI Builder“ plėtinio sąsaja.](./media/ai-builder.png)](./media/ai-builder.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
