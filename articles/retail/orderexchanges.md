---
title: Pakeitimo sukonfigūravimas ir apdorojimas grąžinimo užsakyme
description: Šioje temoje paaiškinama, kaip sukonfigūruoti pakeitimą „Microsoft Dynamics 365 for Retail“ grąžinime.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "302631"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Pakeitimo sukonfigūravimas ir apdorojimas grąžinimo užsakyme

[!include [banner](includes/banner.md)]

Ankstesnėse „Microsoft Dynamics 365 for Retail“ versijose grąžinimai pagal klientų užsakymus buvo apdorojami naudojant „Retail Headquarters“ grąžinimo užsakymo dokumentą. Tačiau, naudojant grąžinimo užsakymo dokumentą, galima apdoroti tik grąžinamus produktus. Grąžinamus produktus nurodo neigiamas kiekis grąžinimo užsakymo eilutėse. Priešingai, pardavimą nurodo teigiamas kiekis. Tačiau grąžinimo užsakymo dokumentas teigiamų kiekių nepalaiko. Dėl šio apribojimo ankstesnėse „Retail“ versijose nebuvo palaikomi scenarijai, kai produktai pakeičiami naudojant grąžinimo užsakymo dokumentą.

Tačiau įtraukta funkcijų, kad būtų palaikomi scenarijai, kai pakeitimai atliekami grąžinimo užsakymuose. Dabar „Retail“ šių tipų operacijas apdoroja naudodama ne grąžinimo užsakymo dokumentą, o pardavimo užsakymo dokumentą.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>„Retail“ sukonfigūravimas, kad būtų palaikomi pakeitimai grąžinimo užsakymuose

Norėdami sukonfigūruoti sistemą, kad būtų palaikomi pakeitimai grąžinimo užsakymuose, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai**. „FastTab“ konteineryje **Klientų užsakymai** parinktį **Grąžinimo užsakymus apdoroti kaip pardavimo užsakymus** nustatykite kaip **Taip**.
2. Vykdykite užduotį **Visuotinis konfigūracijų platinimo grafikas** (**1110**).

## <a name="make-an-exchange"></a>Pakeitimas

Kai sistema yra sukonfigūruota taip, kaip aprašyta ankstesniame skyriuje, elektroninio kasos aparato (EKA) vartotojas vis tiek grąžinimui apdoroti turi pasirinkti pardavimo užsakymą arba pardavimo SF, kaip ankstesnėse „Retail“ versijose. Tačiau, kai į krepšelį įtraukiama grąžinamų prekių, vartotojas į jį galės įtraukti naujų pardavimo eilučių.

Vartotojas turi nustatyti visus šių naujų pardavimo eilučių atributus, kurių reikia, kad būtų galima apdoroti kliento užsakymo eilutę. Šie atributai apima pristatymo būdą ir įvykdymo vietą. Mokėtina operacijos suma bus grynoji grąžinimo užsakymo eilučių ir pardavimo užsakymo eilučių suma. Atlikus mokėjimą už operaciją, grąžinimo užsakymas komponente „Retail Headquarters“ bus užregistruotas kaip pardavimo užsakymo dokumentas ir sistema iš karto grąžinamoms eilutėms išrašys sąskaitą faktūrą.

Kad geriau matytųsi įvairios krepšelio sumos, į krepšelį įtraukti trys nauji sumos laukai. Šiuos naujus laukus įtraukti į EKA vartotojo sąsają galite naudodami ekrano dizaino įrankį.

- **Pritaikytas depozitas** – operacijai pritaikyta depozito suma, kai vartotojas paima kliento užsakymą. Jei depozitas neperrašomas ir sukonfigūruotas 10 procentų depozitas, šiame lauke suma lygi 90 procentų visos kliento užsakymo sumos.
- **Išsinešimo suma** – visa eilučių suma, kai, kuriant ar redaguojant kliento užsakymą arba kliento užsakymą pakeičiant, pristatymo būdas buvo nustatytas kaip **Išsinešimas**. Šiame lauke esanti suma yra su mokesčiais.
- **Grąžinimo suma** – visa eilučių, kuriose pakeičiant kliento užsakymą nurodyta neigiamų kiekių, suma. Šiame lauke esanti suma yra su mokesčiais.
