---
title: "Pirkimo užsakymo apžvalga"
description: "Šiame straipsnyje pateikiama bendra informacija apie pirkimo užsakymus (PU) ir saitai į papildomus straipsnius, susijusius su įvairiomis PU eigos būsenomis."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 88fa3fb97621e0f4a226a45b36809e824c807420
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-order-overview"></a>Pirkimo užsakymo apžvalga

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama bendra informacija apie pirkimo užsakymus (PU) ir saitai į papildomus straipsnius, susijusius su įvairiomis PU eigos būsenomis.

Pirkimo užsakymas (PU) yra dokumentas, kuris nurodo sutartį su tiekėju, pagal kurią perkamos prekės arba paslaugos. Dokumentas taip pat suteikia galimybę sekti užsakymo produkto gavimo kvitus, sukurtus pagal užsakymą, ir vėliau sekti tiekėjo SF, kurias tiekėjas išrašo pagal užsakymą, apskaitą.  

Puslapyje **Pirkimo užsakymai** pateikiama galimų užsakymų apžvalga ir jame tuos užsakymus keisti. Kai atidarote PU, galite pasirinkti rodinį **Antraštė**, kuriame yra tik vieną kartą nurodyta kiekvieno PU informacija, pvz., tiekėjo duomenis. Taip pat galite pasirinkti rodinį **Eilutės**, kuriame galite keisti užsakymo eilutes. Paprastai modifikuojant PU perjungiami abu rodiniai. Mokesčiai nėra pateikiami tiesiogiai puslapyje **Pirkimo užsakymai**, bet juos galima pasiekiami naudojant užsakymo antraščių ir eilučių meniu.  

Pateikiama daug ataskaitų, kuriose galite peržiūrėti informaciją apie PU, produkto gavimo kvitus ir tiekėjo SF. Šias ataskaitas galima rasti moduliuose **Įsigijimas ir šaltinio pasirinkimas** ir **Mokėtinos sumos**.  

Darbo srityse **Pirkimo užsakymo rengimas** ir **Pirkimo užsakymo gavimas ir apdorojimas** galima peržiūrėti PU ir įvairių jų esamų būsenų sąrašus. Jose taip pat pateikiama veiksmų, kuriuose reikia atlikti, suvestinė. Darbo sritis **Pirkimo užsakymo rengimas** yra orientuota į PU kūrimą ir peržiūrą, užsakymo apdorojimą, siekiant jį patvirtinti, ir patvirtinimą iš tiekėjo. Darbo sritis **Pirkimo užsakymų gavimas ir apdorojimas** yra orientuota į prekių ir paslaugų gavimo apdorojimą pagal PU. Joje pateikiami sąrašai, kuriuose pateikiama informacijos apie uždelstus gavimo kvitus arba kvitus, kurių prekes netrukus turi pristatyti tiekėjas. Šios darbo sritys nėra skirtos atlikti su gavimais susijusias veiklas, kurios atliekamos sandėlyje. Tos veiklos atliekamos naudojant modulių **Atsargų valdymas** ir **Sandėlio valdymas** puslapius. Tiekėjo SF turėtų būti apdorotos naudojant darbo sritį **Tiekėjo SF įrašas**, o mokėjimai turėtų būti apdoroti naudojant darbo sritį **Tiekėjo mokėjimai**.  

Toliau nurodytuose straipsniuose pateikiama įvairių PU etapų apžvalga.

-   [Pirkimo užsakymo kūrimas](purchase-order-creation.md)
-   [Pirkimo užsakymo patvirtinimas](purchase-order-approval-confirmation.md)
-   [Produkto gavimas pagal pirkimo užsakymą](product-receipt-against-purchase-orders.md)
-   [Tiekėjo SF apžvalga](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)

## <a name="types-of-purchase-orders"></a>Pirkimo užsakymų tipai
Yra trys PU tipai: Kurdami PU turite nurodyti tipą. Numatytąjį naujų užsakymų tipą galite nustatyti puslapyje **Įsigijimo ir šaltinio pasirinkimo parametrai**.

| PU tipas        | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Žurnalas        | Naudokite šį tipą juodraštiniam užsakymui kurti. Šio tipo užsakymas neturi įtakos atsargų kiekiams ir negeneruoja atsargų operacijų. PU žurnalo eilutės neįtraukiamos į bendrąjį planavimą.                                                                                                       |
| Pirkimo užsakymas | Naudokite šį tipą, kai norite kurti užsakymus, kuriuos turi patvirtinti tiekėjas, ir kai užsakymai apdorojami kuriant gavimo kvitus bei išrašant SF prieš mokėjimą tiekėjui. Šis PU tipas yra labiausiai paplitęs.                                                                          |
| Grąžintas užsakymas | Naudokite šį tipą, kai tiekėjui grąžinate prekes. Kuriant šio tipo užsakymą reikia nurodyti grąžinamų medžiagų autorizavimo (RMA) numerį, kurį jums suteikia tiekėjas. RMA numeris nurodomas PU skirtuke **Bendra**. Užsakymo eilutėse turi būti neigiami kiekiai. |

## <a name="purchase-order-statuses"></a>Pirkimo užsakymo būsenos
PU naudojami keli būsenos laukai, kurie nurodo apie užsakymo eigą. Visi šie laukai yra rodomi užsakymo rodinyje **Antraštė**, o keli iš jų taip pat rodomi visų užsakymų tinklelio peržiūroje. Lauke **Būsena** rodoma užsakymo kiekių būsena. Galimos šios vertės:

-   **Atviras užsakymas** – užsakymas yra sukurtas ir jame nurodyti kiekiai.
-   **Gautas** -kai kurie kiekiai gauti, bet jiems SF dar nebuvo išrašyta.
-   **SF išrašyta** – SF išrašyta visam užsakymo kiekiui. **Pastaba.** Jei užsakymo SF išrašyta *iš dalies*, netinka nei būsena **Gautas**, nei būsena **SF išrašyta**. Todėl užsakymo būsena vis dar bus **Atviras užsakymas**.
-   **Atšauktas** – užsakymas buvo patvirtintas, bet vėliau atšauktas. Todėl ši būsena nurodo, kad užsakyme nebėra jokių atvirų kiekių.

Lauke **Dokumento būsena** galima greitai peržiūrėti užsakymo eigos būseną pagal apdorotus dokumentus. Jame rodoma vėliausiai baigto užsakymo dokumento būsena. Galimos šios vertės:

-   **Nėra** – apdorotų užsakymo dokumentų dar nėra.
-   **Pirkimo užklausa** – pirkimo užklausa buvo sukurta ir laukiama tiekėjo atsiliepimų apie užsakymą.
-   **Pirkimo užsakymas** – užsakymo patvirtinimas buvo apdorotas.
-   **Produkto gavimo kvitas** – užsakymo produkto gavimo kvitas buvo apdorotas.
-   **SF** – užsakymo SF buvo apskaityta.

Laukas **Patvirtinimo būsena** naudojamas, kai naudojamas PU peržiūros procesas arba darbo eiga. Galimos šios vertės:

-   **Juodraštis**, **Peržiūrima** ir **Atmesta** – šios būsenos taikomos tik tada, kai naudojama PU patvirtinimo darbo eiga.
-   **Patvirtinta** – ši būsena yra priskiriama užsakymams, kurių patvirtinimo darbo eiga baigta. Užsakymų, sukurtų nenaudojant patvirtinimo darbo eigos, būsena iš karto nustatoma į **Patvirtinta**.
-   **Išorinė peržiūra** – ši būsena naudojama, kai tiekėjui siunčiama pirkimo užklausa, kad tiekėjas galėtų patvirtinti PU sąlygas. Ši būsena taip pat naudojamas vykdant procesą, inicijuotą veiksmu **Patvirtinimo užklausa**. Šio proceso metu tiekėjo prašoma patvirtinti PU sąlygas prisijungiant prie jūsų sistemos ir užregistruojant užsakymo patvirtinimą arba atmetimą.
-   **Patvirtinta** – ši būsena yra priskiriama patvirtinus užsakymą. Paprastai ši būsena yra paskutinė užsakymui priskiriama patvirtinimo būsena.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Pirkimo užsakymo kūrimas](purchase-order-creation.md)

[Pirkimo užsakymo patvirtinimas](purchase-order-approval-confirmation.md)

[Produkto gavimas pagal pirkimo užsakymą](product-receipt-against-purchase-orders.md)

[Tiekėjo SF apžvalga](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)




