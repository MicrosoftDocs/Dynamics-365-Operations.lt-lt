---
title: Internetinio funkcionalumo profilio kūrimas
description: Šioje temoje aprašoma, kaip sukurti internetinį funkcionalumo profilį, naudojant „Microsoft Dynamics 365 Commerce“.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d6dcbb5b9ea01035396e90a6809cb1568c3a4fc86def41cf36732588b5046da7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716199"
---
# <a name="create-an-online-functionality-profile"></a>Internetinių funkcijų šablono kūrimas

[!include [banner](includes/banner.md)]

Šioje temoje apžvelgiamas internetinio funkcionalumo profilio nustatymas, naudojant „Microsoft Dynamics 365 Commerce“.

Internetiniame funkcionalumo profilyje pateikiami įvairūs internetinių kanalų parametrai. Kiekvienas internetinis kanalas turi nurodyti internetinį funkcionalumo profilį.

## <a name="create-an-online-functionality-profile"></a>Internetinio funkcionalumo profilio kūrimas

Toliau paaiškinama, kaip sukurti internetinį funkcionalumo profilį, naudojant „Commerce“ būstinės programą.

1. Naršymo srityje eikite į **Moduliai \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcionalumo profiliai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Profilis** įveskite profilio ID.
1. Lauke **Aprašymas** įveskite vertę (toliau nurodytame paveikslėlyje„Adventure Works Profile“).
1. Skyriuje **Funkcijos**, jei reikia, pakeiskite nustatymus **KREPŠELIS**, **MAŽMENINĖS PREKYBOS KLIENTAI** arba **UŽBAIGTI PIRKIMĄ**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau parodytame paveikslėlyje pavaizduotas internetinio funkcionalumo profilio pavyzdys.
  
![Internetinio funkcionalumo profilio pavyzdys.](media/online-functionality-profile.png)

## <a name="functions"></a>Funkcijos

- **Sujungti produktus**: įjungus šią funkciją, krepšelis gali atnaujinti kiekį, kai ta pati prekė pridedama kelis kartus.
- **Leisti atlikti mokėjimą neapmokant už prekes**: įjungus šią funkciją apdorojamas scenarijus, kai į krepšelį dedamų prekių kaina yra 0,00 USD.
- **Kurti klientą asinchroniniu režimu**: tai yra senesnis parametras, taikomas trečiųjų šalių „e-Commerce“ kanalams ir netaikomas „Dynamics 365“ „e-Commerce“ svetainei.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų apžvalga](channels-overview.md)

[Kanalo sąrankos būtinieji komponentai](channels-prerequisites.md)

[Interneto kanalo nustatymas](channel-setup-online.md)

[Mažmeninės prekybos kanalo nustatymas](channel-setup-retail.md)

[Skambučių centro kanalo nustatymas](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
