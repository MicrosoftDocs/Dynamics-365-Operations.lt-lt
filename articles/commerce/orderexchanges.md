---
title: Pakeitimo sukonfigūravimas ir apdorojimas grąžinimo užsakyme
description: Šioje temoje paaiškinama, kaip sukonfigūruoti pakeitimą „Dynamics 365 Commerce“ grąžinime.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 488f6fb5af6451bc462566a9714054b49eb1a80b8264528778797f6a39647764
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758341"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Pakeitimo sukonfigūravimas ir apdorojimas grąžinimo užsakyme

[!include [banner](includes/banner.md)]

Ankstesnėse „Dynamics 365 Commerce“ versijose grąžinimai pagal klientų užsakymus buvo apdorojami naudojant grąžinimo užsakymo dokumentą būstinės komponente. Tačiau, naudojant grąžinimo užsakymo dokumentą, galima apdoroti tik grąžinamus produktus. Grąžinamus produktus nurodo neigiamas kiekis grąžinimo užsakymo eilutėse. Priešingai, pardavimą nurodo teigiamas kiekis. Tačiau grąžinimo užsakymo dokumentas teigiamų kiekių nepalaiko. Dėl šio apribojimo ankstesnėse programos versijose nebuvo palaikomi scenarijai, kai produktai pakeičiami naudojant grąžinimo užsakymo dokumentą.

Tačiau įtraukta funkcijų, kad būtų palaikomi scenarijai, kai pakeitimai atliekami grąžinimo užsakymuose. Dabar „Commerce“ šių tipų operacijas apdoroja naudodama ne grąžinimo užsakymo dokumentą, o pardavimo užsakymo dokumentą.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>„Commerce“ sukonfigūravimas, kad būtų palaikomi pakeitimai grąžinimo užsakymuose

> [!NOTE]
> „Commerce“ 10.0.20 ir vėlesnėse versijose galima naudoti naują funkciją pavadinimu „Bendrojo grąžinimo apdorojimo funkcija EKA“. Jei įjungsite šią funkciją, toliau pateiktų nustatymo veiksmų atlikti nebūtina. **Grąžinimų kaip pardavimo užsakymų apdorojimas** tampa visam laiku sukonfigūruotu parametru ir jo pakeisti negalėsite.

Norėdami konfigūruoti sistemą, kad ji palaikų grąžinimo užsakymų pakeitimus, atlikite šiuos veiksmus (jei nesate įjungę funkcijos **Bendrojo grąžinimo apdorojimo funkcija EKA**).

1. Eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> „Commerce“ parametrai**. „FastTab“ konteineryje **Klientų užsakymai** parinktį **Grąžinimo užsakymus apdoroti kaip pardavimo užsakymus** nustatykite kaip **Taip**.
2. Vykdykite užduotį **Visuotinis konfigūracijų platinimo grafikas** (**1110**).

## <a name="make-an-exchange"></a>Pakeitimas

Kai sistema yra sukonfigūruota taip, kaip aprašyta ankstesniame skyriuje, elektroninio kasos aparato (EKA) vartotojas vis tiek grąžinimui apdoroti turi pasirinkti pardavimo užsakymą arba pardavimo SF, kaip ankstesnėse programos versijose. Tačiau, kai į krepšelį įtraukiama grąžinamų prekių, vartotojas į jį galės įtraukti naujų pardavimo eilučių.

Vartotojas turi nustatyti visus šių naujų pardavimo eilučių atributus, kurių reikia, kad būtų galima apdoroti kliento užsakymo eilutę. Šie atributai apima pristatymo būdą ir įvykdymo vietą. Mokėtina operacijos suma bus grynoji grąžinimo užsakymo eilučių ir pardavimo užsakymo eilučių suma. Atlikus mokėjimą už operaciją, grąžinimo užsakymas būstinės komponente bus užregistruotas kaip pardavimo užsakymo dokumentas ir sistema iš karto grąžinamoms eilutėms išrašys sąskaitą faktūrą.

Kad geriau matytųsi įvairios krepšelio sumos, į krepšelį įtraukti trys nauji sumos laukai. Šiuos naujus laukus įtraukti į EKA vartotojo sąsają galite naudodami ekrano dizaino įrankį.

- **Pritaikytas depozitas** – operacijai pritaikyta depozito suma, kai vartotojas paima kliento užsakymą. Jei depozitas neperrašomas ir sukonfigūruotas 10 procentų depozitas, šiame lauke suma lygi 90 procentų visos kliento užsakymo sumos.
- **Išsinešimo suma** – visa eilučių suma, kai, kuriant ar redaguojant kliento užsakymą arba kliento užsakymą pakeičiant, pristatymo būdas buvo nustatytas kaip **Išsinešimas**. Šiame lauke esanti suma yra su mokesčiais.
- **Grąžinimo suma** – visa eilučių, kuriose pakeičiant kliento užsakymą nurodyta neigiamų kiekių, suma. Šiame lauke esanti suma yra su mokesčiais.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
