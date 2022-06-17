---
title: Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas
description: Šiame straipsnyje aprašoma, kaip redaguoti ir tikrinti internetinio užsakymo ir asinchroninio kliento užsakymo operacijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c4219e082466bdfd1426710cecf25fd350d0767
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873064"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip redaguoti ir tikrinti internetinio užsakymo ir asinchroninio kliento užsakymo operacijas „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Apžvalga

„Commerce“ 10.0.5 ir 10.0.6 versijos skiriasi tuo, kad į pastarąją buvo įtrauktas atsiskaitymo grynaisiais operacijų (pvz., pardavimo ir grąžinimo) ir grynųjų pinigų valdymo operacijų (pvz., srauto įrašo ir mokėjimo priemonės šalinimo) redagavimo palaikymas. „Commerce“ 10.0.7 versijoje įtrauktas internetinio užsakymo operacijų ir asinchroninio kliento užsakymo operacijų redagavimo palaikymas.

## <a name="edit-and-audit-order-transactions"></a>Užsakymo operacijų redagavimas ir tikrinimas

Norėdami redaguoti ir tikrinti užsakymo operacijas „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Įdiekite [„Microsoft Dynamics Office Add-in“](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Puslapio **Mažmeninės prekybos parametrai** skirtuko **Kliento užsakymai** „FastTab“ **Užsakymas** nurodykite sulaikymo kodą, skirtą **Užsakymo sinchronizavimo klaidų sulaikymo kodas**.
1. Atidarykite darbo sritį **Parduotuvės finansai**. Plytelėmis **Internetinio užsakymo sinchronizavimo klaidos** ir **Kliento užsakymo sinchronizavimo klaidos** pateikiamas iš anksto filtruotas mažmeninės prekybos operacijos puslapio rodinys. Kiekvienoje rodomi operacijų įrašai, kurių atitinkamo užsakymo tipo sinchronizavimas nepavyko.
1. Atidarykite puslapį **Internetinio užsakymo sinchronizavimo klaidos** arba puslapį **Kliento užsakymo sinchronizavimo klaidos**. Pasirinkite įrašą, kad peržiūrėtumėte išsamią sinchronizavimo klaidos informaciją. „FastTab“ **Sinchronizavimo būsena** pateikiama ši išsami klaidos informacija:

    - Laukiama užsakymo būsena
    - Išsami užsakymo klaidos informacija
    - Pakeitimo data ir laikas
    - Mėginimų skaičius

1. Jei išsamia klaidos informacija nurodoma, kad įrašą reikia ištaisyti, pasirinkite **„Office“ papildinys** ir pasirinkite **Redaguoti pasirinktą operaciją**. Atidaromas „Excel“ failas, kuriame rodoma išsami pasirinktos operacijos informacija.

    - Jei redaguojama operacija yra internetinio užsakymo operacija, „Excel“ faile yra šie darbalapiai:

        - **Operacija** – šiame darbalapyje pateikiama išsami antraštės informacija apie operaciją.
        - **Pardavimo operacija** – šiame darbalapyje pateikiama išsami eilutės informacija apie operaciją.
        - **Mokėjimo operacijos** – šiame darbalapyje pateikiama išsami informacija apie operacijos mokėjimo eilutes.
        - **Nuolaidų operacijos** – šiame darbalapyje pateikiama su nuolaidomis susijusi informacija apie operaciją.
        - **Mokesčių operacijos** – šiame darbalapyje pateikiama su mokesčiais susijusi informacija apie operaciją.
        - **Išlaidų operacijos** – šiame darbalapyje pateikiami su išlaidomis susiję duomenys apie operaciją.

    - Jei redaguojama operacija yra asinchroninio kliento užsakymo operacija, „Excel“ faile yra šie darbalapiai:

        - **Eilutės** – šiame darbalapyje pateikiama išsami antraštės ir eilutės informacija apie operaciją.
        - **Mokėjimai** – šiame darbalapyje pateikiama išsami informacija apie operacijos mokėjimo eilutes.
        - **Nuolaidos** – šiame darbalapyje pateikiama su nuolaidomis susijusi informacija apie operaciją.
        - **Mokesčiai** – šiame darbalapyje pateikiama su mokesčiais susijusi informacija apie operaciją.
        - **Išlaidos** – šiame darbalapyje pateikiami su išlaidomis susiję duomenys apie operaciją.

1. „Excel“ faile lauke **Laukiama užsakymo būsena** įveskite **Redaguojama** ir tada publikuokite keitimą. Tokiu būdu per apdorojimą užduotis **Sinchronizuoti užsakymą**, vykdoma paketiniu režimu, nepraleis šio įrašo.
1. „Excel” faile modifikuokite atitinkamus laukus ir tada įkelkite duomenis atgal į „Commerce“ būstinę naudodami „Dynamics Excel“ papildinio publikavimo funkciją. Publikavus duomenis, pakeitimai bus rodomi sistemoje. Publikuojant, vartotojo atlikti keitimai netikrinami.
1. Visą keitimų įrašų seką galima peržiūrėti pasirinkus **Peržiūrėti įrašo sekimą** antraštėje **Mažmeninės prekybos operacijos** (antraštės lygmens keitimai) ir atitinkamame skyriuje bei operacijų puslapio įraše. Pavyzdžiui, visi su pardavimo eilutėmis susiję pakeitimai bus rodomi puslapyje **Pardavimo operacijos**, o visi su mokėjimais susiję pakeitimai – puslapyje **Mokėjimo operacijos**. Pakeitimams palaikoma toliau pateikiama išsami audito informacija:

    - Pakeitimo data ir laikas
    - Laukas
    - Sena vertė
    - Nauja vertė
    - Modifikavo

1. Atlikę ir publikavę keitimus, pasirinkite **Sinchronizuoti užsakymą**, kad būtų nedelsiant pradėtas sinchronizavimo procesas. Taip pat galite palaukti, kol paketiniu režimu vykdant sinchronizavimo procesą bus apdorota operacija.

Pagal numatytuosius parametrus, sėkmingai sinchronizavus užsakymus, jie yra perkeliami į sulaikymo būseną, atsižvelgiant į sulaikymo kodą, apibrėžtą „Commerce“ parametruose. Užsakymų sulaikymas turi būti pašalintas, kad užsakymus būtų galima toliau apdoroti norint juos įvykdyti arba atlikti kitas operacijas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas](edit-cash-trans.md)

[Mažmeninės prekybos operacijų finansinių dimensijų redagavimas](edit-financial-dim.md)

[„Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas](create-excel-edit.md)

[Laukų įtraukimas į „Excel“ darbaknygę norint redaguoti mažmeninės prekybos operacijas](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]