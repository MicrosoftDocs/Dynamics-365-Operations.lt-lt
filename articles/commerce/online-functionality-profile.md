---
title: Internetinio funkcionalumo profilio kūrimas
description: Šioje temoje aprašoma, kaip sukurti internetinį funkcionalumo profilį, naudojant „Microsoft Dynamics 365 Commerce“.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969981"
---
# <a name="create-an-online-functionality-profile"></a>Internetinio funkcionalumo profilio kūrimas


[!include [banner](includes/banner.md)]

Šioje temoje apžvelgiamas internetinio funkcionalumo profilio nustatymas, naudojant „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

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
  
![Internetinio funkcionalumo profilio pavyzdys](media/online-functionality-profile.png)

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