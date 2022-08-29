---
title: Internetinių funkcijų šablono kūrimas
description: Šiame straipsnyje aprašoma, kaip kurti interneto funkcijų profilį Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5ce81900cd0648132748167d03906afc64e97f25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276807"
---
# <a name="create-an-online-functionality-profile"></a>Internetinių funkcijų šablono kūrimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama interneto funkcijų šablono nustatymo peržiūra Microsoft Dynamics 365 Commerce.

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
