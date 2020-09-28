---
title: Projekto išteklių planavimo našumas
description: Šioje temoje pateikiama informacija apie tai, kaip padidinti daugelio projektų išteklių planavimo našumą.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760619"
---
# <a name="project-resource-scheduling-performance"></a>Projekto išteklių planavimo našumas

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Našumo problemos, susijusios su išteklių planavimu, gali įvykti, kai projektų skaičius pasiekia tūkstančius. Siekiant padidinti išteklių planavimo našumą, siūloma funkcija, leidžianti vartotojams sutrumpinti laiką, kurio reikia išteklių pasiekiamumo formai paleisti. Tiksliau sakant, taip pašalinamas išteklių pajėgumų sumavimų sinchronizavimo procesas ir naudojama lentelė **ResProjectResource** siekiant paspartinti išteklių peržvalgą. Atkreipkite dėmesį, kad lentelė **ResRollup** nebebus naudojama.

> [!IMPORTANT]
> Jei yra priklausomybė nuo išteklių pajėgumų sumavimų sinchronizavimo proceso arba lentelės **ResProjectResource**, nenaudokite šios funkcijos.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Išteklių planavimo našumo didinimo įjungimas
Norėdami įjungti išteklių planavimo našumo didinimą, atlikite toliau pateiktus veiksmus.

1. Eikite į **Funkcijų valdymas** > **Visi** ir funkcijų sąraše suraskite **Įjungti projektų išteklių planavimo našumo didinimo funkciją**.
2. Pasirinkite **Įjungti dabar**.

> [!NOTE]
> Jeigu nerandate funkcijos sąraše, pasirinkite **Tikrinti, ar yra naujinimų**, kad sąrašas būtų atnaujintas.

3. Atnaujinkite naršyklę ir eikite į **Projektų valdymas ir apskaita** > **Laikotarpio** > **Projekto ištekliai** > **Sinchronizuoti išteklių kalendorių pajėgumą visose įmonėse**.
4. Nustatykite **Pašalinti esamus pajėgumo įrašus** į **Taip** , kad būtų pašalinti ankstesni duomenys. Jei norite generuoti papildančius duomenis, nustatykite į **Ne**.
5. Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio metu turi būti sugeneruoti duomenys. Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datų nebūtina nurodyti.
6. Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.
7. Pasirinkite **Gerai**.

 > [!NOTE]
 > Bendrieji duomenys bus paskirstyti į lentelę **ResCalendarCapacity** visose jūsų aplinkos įmonėse, kad paketinė užduotis būtų vykdoma tik viename juridiniame subjekte. Šios paketinės užduoties duomenys reikalingi, kad būtų galima apskaičiuoti išteklių pajėgumą naudojant susijusį kalendorių.

8. Eikite į **Projektų valdymas ir apskaita** > **Laikotarpio** > **Projekto ištekliai** > **Automatiškai įvesti projekto išteklius visose įmonėse** ir pasirinkite **Gerai** . Tai yra bendrųjų duomenų naujinimo scenarijus lentelėse **ResProjectResource**, **ResCalendarDateTimeRange** ir **ResEffectiveDateTimeRange**. Reikšmės, skirtos laukui **PSAPRojSchedRole.RootActivity**, taip pat atnaujinamos. Jei nevykdoma, gausite įspėjimą, kai bandysite vykdyti išteklių planavimo operacijas.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Išteklių planavimo našumo didinimo išjungimas

1. Eikite į **Funkcijų valdymas** > **Visi** ir raskite **Įjungti projektų išteklių planavimo našumo didinimo funkciją**.
2. Pasirinkite funkciją ir tada pasirinkite mygtuką **Išjungti**.
3. Atnaujinkite naršyklę.
4. Eikite į **Projektų valdymas ir apskaita** > **Laikotarpio** > **Pajėgumo sinchronizavimas** > **Sinchronizuoti išteklių pajėgumų sumavimus**.
5. Norėdami pašalinti ankstesnius duomenis, puslapyje **Pajėgumų sumavimų sinchronizavimas** nustatykite **Pašalinti esamus pajėgumo įrašus** į **Taip** . Jei norite generuoti papildančius duomenis, nustatykite į **Ne**.
6. Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio metu turi būti sugeneruoti duomenys. Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datų nebūtina nurodyti.
7. Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.
8. Pasirinkite **Gerai**.

> [!NOTE]
> Bendrieji duomenys bus paskirstyti į lentelę **ResRollup** visose jūsų aplinkos įmonėse, kad paketinė užduotis būtų vykdoma tik viename juridiniame subjekte. Ši paketinė užduotis reikalinga visuose rodiniuose **Išteklių pasiekiamumas**. Jei ši paketinė užduotis nevykdoma, **ResRollup** duomenys bus generuojami iš karto, o tai gali užtrukti.
