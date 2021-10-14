---
title: Slankiojo vidurkio atsarginės savikainos seka
description: Šioje temoje pateikiama informacija apie slankiojo vidurkio skaičiavimų atsarginių savikainų sekas „Microsoft Dynamics 365 Supply Chain Management”.
author: AndersGirke
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d91b3b4b8d49e59aa03d62f4dd101b5a1ec18c41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568212"
---
# <a name="moving-average-fallback-cost-sequence"></a>Slankiojo vidurkio atsarginės savikainos seka

[!include [banner](../includes/banner.md)]

Vienas būdas apskaičiuoti savo atsargų savikainą yra naudoti _slankųjį vidurkį_. Su kiekviena atsargų preke gali būti susietos daugiausiai trys savikainos reikšmės:

- **Paskutinis išdavimas** – paskutinė išdavimo savikaina, priskirta prieš atsargoms tampant neigiamomis
- **Aktyvi savikaina** – paskutinė savikaina, suaktyvinta įkainojimo versijoje
- **Prekės kaina** – savikaina, nurodyta išleistam produktui

Norėdama nustatyti, kurią iš šių savikainos reikšmių naudoti slankiojo vidurkio skaičiavimuose, sistema naudoja _atsarginės savikainos seką_, kad nustatytų reikšmes prioriteto tvarka. Jei pageidaujama savikainos reikšmė neprieinama, sistema naudoja sekančią pageidaujamą reikšmę ir t. t.

Ankstesnėse „Microsoft Dynamics 365 Supply Chain Management” versijose sistema naudojo fiksuotą atsarginės savikainos seką (_Paskutinis išdavimas, Aktyvi savikaina, Prekės kaina_). 10.0.11 versijoje ši seka vis dar yra numatytoji seka. Tačiau, taip pat galite įjungti funkciją, leidžiančią pasirinkti iš trijų galimų atsarginių savikainų sekų. Ši funkcija gali būti ypač naudinga organizacijoms, kurios reguliariai naudoja neigiamų atsargų reikšmes.

Kad atsarginės savikainos sekos parinkiklis taptų pasiekiamas, jūs (arba administratorius) turite naudoti [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte funkciją pavadinimu _Slankiojo vidurkio atsarginės savikainos seka_.

Norėdami pasirinkti slankiojo vidurkio skaičiavimų atsarginės savikainos seką, atlikite toliau pateiktus veiksmus.

1. Atidarykite puslapį **Parametrai**.
2. Skirtuko **Atsargų apskaita** skyriuje **Slankusis vidurkis** nustatykite lauką **Atsarginės savikainos seka** į vieną iš toliau pateiktų reikšmių.

    - **Paskutinis išdavimas, Aktyvi savikaina, Prekės kaina** – ši seka yra numatytoji seka. Tai ta pati seka, kuri naudojama, jei funkcija _Slankiojo vidurkio atsarginės savikainos seka_ neįjungta.
    - **Aktyvi savikaina, Paskutinis leidimas**
    - **Aktyvi savikaina, Prekės kaina** – organizacijoms gali kilti našumo problemų, jei jos naudoja verslo procesus, kuriuose atsargos reguliariai tampa neigiamos, ir tuo pačiu metu yra didelis operacijų kiekis. Šis parametras gali padėti sušvelninti šias našumo problemas.

![Atsargų apskaitos parametrai.](media/inventory-accounting-parameters.png "Atsargų apskaitos parametrai")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]