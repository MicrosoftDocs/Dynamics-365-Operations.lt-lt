---
title: Siuntų vežėjų nustatymas
description: Šioje temoje aprašyta, kaip nustatyti siuntų vežėją ir jo išsamią informaciją, pavyzdžiui, tarnybą, siuntimo būdą, transportavimo mokėjimo priemonę, transportavimo apribojimus ir siuntimo tarifą.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e6a29dce877a53d125c5a151da6cfbb13d46b29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201599"
---
# <a name="set-up-shipping-carriers"></a>Siuntų vežėjų nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašyta, kaip nustatyti siuntų vežėją ir jo išsamią informaciją, pavyzdžiui, tarnybą, siuntimo būdą, transportavimo mokėjimo priemonę, transportavimo apribojimus ir siuntimo tarifą. Transportavimo koordinatorius tada gali priskirti siuntų vežėją gaunamam arba siunčiamam kroviniui.


## <a name="create-a-new-shipping-carrier"></a>Kurti naują siuntų vežėją
1. Eikite į **Naršymo sritis > Moduliai > Transportavimo valdymas > Sąranka > Vežėjai > Siuntų vežėjai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Siuntų vežėjas** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Būdas** išplečiamajame meniu pažymėkite parinktį.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Įvesti bendrą siuntų vežėjo informaciją
1. Perjunkite skyriaus **Apžvalga** išplėtimą.
2. Pažymėkite arba atžymėkite žymės langelį **Aktyvinti siuntų vežėją**.
3. Lauke **Tiekėjo sąskaita** išplečiamajame meniu pažymėkite parinktį. Pasirinkite tiekėjo sąskaitą, kad priskirtumėte siuntų vežėjui.  
4. Lauke **Transportavimo mokėjimo priemonės tipas** pažymėkite parinktį. Norėdami naudoti transportavimo mokėjimo priemonės puslapį pasirinkite **Neautomatinis**, o norėdami atnaujinti mokėjimo priemonę naudojant elektroninius duomenų mainus (EDI), pasirinkite **EDI**.  
5. Pažymėkite arba atžymėkite žymės langelį **Aktyvinti vežėjų vertinimą**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Sukurti siuntų vežėjui būtinas paslaugas
1. Perjunkite skyriaus **Paslaugos** išplėtimą.
2. Pasirinkite **Naujas**.
3. Lauke **Vežėjo tarnyba** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Transportavimo būdas** išplečiamajame meniu pažymėkite parinktį.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Nustatyti vežėjo adresą (pasirinktinai)
1. Perjunkite skyriaus **Adresai** išplėtimą.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas arba aprašas** įveskite reikšmę.
4. Lauke **Šalis / regionas** išplečiamajame meniu pažymėkite parinktį.
5. Lauke **Pašto indeksas** išplečiamajame meniu pažymėkite parinktį.
6. Lauke **Gatvė** įveskite reikšmę.
7. Pasirinkite **Gerai**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Nustatyti siuntų vežėjo vertinimo šabloną
1. Perjunkite skyriaus **Vertinimo profiliai** išplėtimą.
2. Pasirinkite **Naujas**.
3. Lauke **Vertinimo profilis** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Vieta** išplečiamajame meniu pažymėkite parinktį.
6. Lauke **Sandėlys** išplečiamajame meniu pažymėkite parinktį.
7. Lauke **Tarifų mechanizmas** išplečiamajame meniu pažymėkite parinktį. Pasirinkite tarifų mechanizmą, kuris atitinka jūsų sutartį su vežėju.  
8. Lauke **Pagrindinis tarifas** išplečiamajame meniu pažymėkite parinktį.
9. Lauke **Tranzito laiko mechanizmas** išplečiamajame meniu pažymėkite parinktį.
10. Pasirinkite **Įrašyti**.

