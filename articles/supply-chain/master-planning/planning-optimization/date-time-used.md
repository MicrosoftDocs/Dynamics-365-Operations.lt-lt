---
title: Datos ir laiko parametrai, naudojami „Planning Optimization“
description: Šiame straipsnyje pateikiama informacija apie datos ir laiko parametrus, kuriuos planavimo optimizavimas naudoja operacijos metu.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2ef78c73a1c7033735f9586229ff7ba21daaa5ef
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740910"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Datos ir laiko parametrai, naudojami „Planning Optimization“

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie datos ir laiko parametrus, kuriuos planavimo optimizavimas naudoja operacijos metu.

Kadangi pasenusio bendrojo planavimo modulis visuose skaičiavimuose naudoja operacijų datas, planavimo optimizavimas veikia pagal datos ir laiko vertes, kurios konvertuojamos į datas. Dėl tokio veikimo būdo skirtumo gali atsirasti situacijų, kai, pvz., prognozės operacijos, sukurtos vidurnaktį tą dieną, kai vykdomas bendrasis planavimas, neįtrauktos, nes „Planning Optimization“ mano, kad jos sukurtos iki esamos datos.

## <a name="parameters-for-issue-and-demand-transactions"></a>Išdavimo ir poreikio operacijų parametrai

Šioje lentelėje išvarditi parametrai, kuriuos „Planning Optimization“ naudoja, kai jis apdoroja išdavimo ir poreikio operacijas.

| Parametras | „Planning Optimization“ parametro pavadinimas | Aprašymas | Atitinkamas „Microsoft Dynamics 365 Supply Chain Management“ laukas (lentelėje ReqTrans) |
|---|---|---|---|
| Suplanuotas išdavimo laikas | `PlannedIssueTime` | Data nėra problema, kuriai dabar planuojama. | **Pabaigos data** (`FuturesDate`) ir **atidėta iki laiko** (`FuturesTime`) |
| Pageidaujamas išdavimo laikas | `RequestedIssueTime` | Išdavimo data, kurios prašė vartotojas ir kuri nustatyta „Supply Chain Management“ dalyje. Šis parametras taikomas tik išleistiems arba patvirtintiems suplanuotams užsakymams. Suplanuotų užsakymų laukas pagal numatytuosius nustatymus yra tuščias. | **Pareikalauta data** (`ReqDateDlvOrig`) |
| Būtinas problemos laikas | `RequiredIssueTime` | Reikiama išdavimo data, pakoreguota „Planning Optimization“. Jei pageidaujamas išdavimo laikas yra praeityje, kai vykdomas „Planning Optimization“, reikiamas išdavimo laikas bus pakoreguotas į pirmą atvirą dieną, kuri nėra ankstesnė nei šios dienos data. Jei pageidaujamas išdavimo laikas kalendoriuje pažymėtas kaip užblokuotas, reikiamas išdavimo laikas bus pakoreguotas į pirmą atvirą dieną iki tos datos. | **Poreikio data** (`ReqDate`) ir **poreikio laikas** (`ReqTime`) |
| Išdavimo laiko atidėjimas | `IssueTimeDelay` | Laiko skirtumas tarp suplanuoto išdavimo laiko ir pageidaujamo patvirtintų ir išleistų užsakymų išdavimo laiko arba reikalaujamo išdavimo laiko. | **Uždelsimas (dienomis)** ( `FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Gavimo ir tiekimo operacijų parametrai

Šioje lentelėje išvarditi parametrai, kuriuos „Planning Optimization“ naudoja, kai jis apdoroja gavimo ir tiekimo operacijas.

| Parametras | „Planning Optimization“ parametro pavadinimas | Aprašymas | Atitinkamas „Supply Chain Management“ laukas (lentelėje ReqTrans arba ReqPO) |
|---|---|---|---|
| Suplanuotas užimtumo laikas | `PlannedAvailabilityTime` | Data, kai gavimas suplanuotas kaip prieinamas. | **Poreikio data** (`ReqDate`) ir **poreikio laikas** (`ReqTime`) |
| Suplanuotas gavimo laikas | `PlannedReceiptTime` | Data, kai gavimas bus pristatytas į vietą. | **Iki datos** (`FuturesDate`), **Vėluojama iki laiko** (`FuturesTime`) ir **Pristatymo data** (`ReqDateDlv`) ar **Prašymo data** (`ReqDateDlvOrig`) jei užsakymas neišleistas. |
| Būtinas užimtumo laikas | `RequiredAvailabilityTime` | Reikiama prieinamumo data, pakoreguota „Planning Optimization“. | **Poreikio data** (`ReqDate`) ir **poreikio laikas** (`ReqTime`) |
| Tikėtinas gavimo laikas | `ExpectedReceiptTime` | Numatoma pateikto gavimo data. Vertę nustato „Supply Chain Management“ vartotojas, kuri nėra koreguojama „Planning Optimization“. Šis parametras taikomas tik išleisties gavimų atveju. | **Pareikalauta data** (`ReqDateDlvOrig`) |
| Būtinas gavimo laikas | `RequiredReceiptTime` | Reikiama gavimo data, pakoreguota „Planning Optimization“. | **Poreikio data** (`ReqDate`) ir **poreikio laikas** (`ReqTime`) |
| Suplanuoto užsakymo laikas | `PlannedOrderingTime` | Reikiama užsakyma data, apskaičiuota „Planning Optimization“. | **Užsakymo data** (`ReqDateOrder`) ir **Užsakymo laikas** (`ReqTimeOrder`) |
| Suplanuotos veiklos pradžios laikas | `PlannedActivityStartTime` | Data, kada turėtų prasidėti šio gavimo veikla. | **Pradžios data** (`SchedFromDate`) |
| Gavimo laiko atidėjimas | `ReceiptTimeDelay` | Laiko skirtumas tarp suplanuoto gavimo laiko ir reikalaujamo gavimo laiko. | **Uždelsimas (dienos)** ( `FuturesDays`) ir **uždelsimas iki laiko** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Dato parametro pavyzdžio naudojimas „Planning Optimization“

Toliau pateikti pavyzdžiai yra šiandienos lygyje, tačiau Planning Optimization“ vykdomas išsamesnį lygį. Pavyzdžiui, kadangi maržos gali būti valandomis, planavimo užsakymo laikas gali būti 2021 m. sausio 22 d., 11:35 val. ir t. t.

### <a name="example-1-simple-scenario"></a>1 pavyzdys: Paprastas scenarijus

Vienas pardavimo užsakymas, kuriam sausio 22 d. pareikalauta išdavimo laikas, padengia vienas pirkimo užsakymas. Galimi šie parametrai yra naudojami:

- Jokio gamybos laiko
- Nėra kalendorių (visos dienos atidarytos.)
- Nėra maržų

Toliau pateikiamoje iliustracijoje vaizduojamas šis scenarijus. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Pavyzdinis scenarijus.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>2 pavyzdys: Gamybos laiko scenarijus

Vienas pardavimo užsakymas, kuriam sausio 22 d. pareikalauta išdavimo laikas, padengia vienas pirkimo užsakymas. Galimi šie parametrai yra naudojami:

- Trys gamybos laiko dienos
- Nėra kalendorių (visos dienos atidarytos.)
- Nėra maržų

Toliau pateikiamoje iliustracijoje vaizduojamas šis scenarijus. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Gamybos laiko scenarijus.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>3 pavyzdys: Maržos scenarijus

Vienas pardavimo užsakymas, kuriam sausio 22 d. pareikalauta išdavimo laikas, padengia vienas pirkimo užsakymas. Galimi šie parametrai yra naudojami:

- Trys gamybos laiko dienos
- Keturių dienų užsakymo marža
- Penkių dienų užimtumo marža
- Nėra kalendorių (visos dienos atidarytos.)

Toliau pateikiamoje iliustracijoje vaizduojamas šis scenarijus. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Maržos scenarijus.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>4 pavyzdys: Delsos scenarijus

Vienas pardavimo užsakymas, kuriam sausio 22 d. pareikalauta išdavimo laikas, padengia vienas pirkimo užsakymas. Šiame pavyzdyje naudojami tie patys parametrai kaip 3 pavyzdys, bet planavimo data buvo perkelta į sausio 15 d. Atgalinio planavimo (raudoni žymekliai) nepavyksta, nes suplanuotas užsakymo laikas turi būti prieš šios dienos datą. Todėl bendrasis planavimas turi būti planuojamas į priekį ir atsiranda vėlavimas.

Toliau pateikiamoje iliustracijoje vaizduojamas šis scenarijus. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Delsos scenarijus.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>5 pavyzdys: Perkėlimo scenarijus

Vieną 1 sandėlio pardavimo užsakymą, kuriam nurodytas pageidaujamas išdavimo laikas sausio 22 d., padengia vienas perkėlimo užsakymas iš 2 sandėlio, kurį apima suplanuotas pirkimo užsakymas. Galimi šie parametrai yra naudojami:

- Trys perdavimo gamybos laiko dienos (sandėlis 1)
- Dvi pirkimo gamybos laiko dienos (sandėlis 2)
- Nėra kalendorių (visos dienos atidarytos.)

Toliau pateikiamoje iliustracijoje vaizduojamas šis scenarijus. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Perkėlimo scenarijus.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>6 pavyzdys: Gamybos laikas su kalendorių scenarijumi

Vienas pardavimo užsakymas, kuriam sausio 22 d. pareikalauta išdavimo laikas, padengia vienas pirkimo užsakymas. Galimi šie parametrai yra naudojami:

- Trys gamybos laiko dienos
- Išdavimo kalendorius (uždarytas penktadienį)
- Užimtumo kalendorius (uždarytas ketvirtadienį ir penktadienį)
- Gavimo kalendorius (uždarytas antradienį, trečiadienį ir sekmadienį)
- Gmaybos laiko kalendorius (uždarytas ketvirtadienį ir penktadienį)
- Užsakymo kalendorius (atidarytas pirmadienį ir šeštadienį)

Toliau pateikiamoje iliustracijoje vaizduojamas šis scenarijus. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![6 pavyzdys: Gamybos laikas su kalendorių scenarijumi.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>7 pavyzdys: Delsos laikas su kalendorių scenarijumi

Vienas pardavimo užsakymas, kuriam sausio 22 d. pareikalauta išdavimo laikas, padengia vienas pirkimo užsakymas. Šiame pavyzdyje naudojami tie patys parametrai kaip 6 pavyzdys, bet planavimo data buvo perkelta į sausio 13 d. Atgalinio planavimo (raudoni žymekliai) nepavyksta, nes suplanuotas užsakymo laikas turi būti prieš šios dienos datą. Todėl bendrasis planavimas turi būti planuojamas į priekį ir atsiranda vėlavimas.

Toliau pateikiamoje iliustracijoje vaizduojamas šis scenarijus. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Delsos laikas su kalendorių scenarijumi.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
