---
title: Pagrindinių tarifų nustatymas
description: Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47fa7edeba81d826a00668a2da74113f552437f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974265"
---
# <a name="set-up-rate-masters"></a>Pagrindinių tarifų nustatymas

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą. Pagrindinius tarifus paprastai nustato logistikos vadovas atsižvelgdamas į su vežėjais pasirašytas sutartis. Šiame scenarijuje nustatysite pagrindinį tarifą oro vežėjui. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.

## <a name="set-up-break-master"></a>Nustatykite pertrūkio pagrindinius duomenis

1. Eikite į **Gabenimo valdymas > Nustatymai > Reitingavimas > Pagrindinių duomenų pertraukimas**. Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti. Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.  
1. Pasirinkite **Naujas**.
1. Laukelyje **Pagrindinių duomenų pertraukimas** įveskite vertę.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Laukelyje **Duomenų tipas** pasirinkite duomenų tipą.
1. Laukelyje **Palyginimas** įveskite būtiną palyginimo tipą (naudodami operatorius).
1. Laukelyje **Pertraukimo vienetas** įveskite pertraukimo vienetą.
1. Skyriuje **Išsami informacija** sukurkite tiek pertraukimų kiek reikia kainų struktūrai.
1. Pasirinkite **Įrašyti**.

## <a name="set-up-rate-master"></a>Nustatyti pagrindinį tarifą

1. Eikite į **Gabenimo valdymas > Nustatymai > Reitingavimas > Pagrindinių duomenų reitingavimas**.
1. Pasirinkite **Naujas**.
1. Laukelyje **Pagrindinių duomenų reitingavimas** įveskite vertę.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Laukelyje **Reitingavimo metaduomenų ID** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką. Reitingavimo metaduomenų ID nustatys duomenis būtinus pagrindinių duomenų reitingui, nes jie nustato tikėtinus metaduomenis gabenimo valdymo varikliui, kuris reitinguoja pagrindinius duomenis.  
1. Šiam pavyzdžiui, rinkitės P2P parinktį. Ją jau nustato demontraciniai duomenys.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Pasirinkite **Įrašyti**.

## <a name="set-up-rate-base"></a>Nustatyti tarifo pagrindą

1. Rinkitės **Reitinguoti pagrindinius**.
    * Tarifo pagrindas nulemia vežėjo tarifą ir gali būti naudojamas tarifų struktūrai nustatyti, nes jis nustato tarifų ribinius taškus, apibrėžtus bendrosiose ribose.  
2. Pasirinkite **Naujas**.
3. Laukelyje **Reitinguoti pagrindinius** įveskite vertę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Laukelyje **Pagrindinių duomenų pertraukimo** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.
    * Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti. Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.  
6. Šiam pavyzdžiui, naudokite svorį. Ją jau nustato demontraciniai duomenys.
7. Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.
8. Išpėskite **Išsamios informacijos** skyrių.
9. Pasirinkite **Naujas**.
10. Laukelyje **Pašto kodo rikiavimas pagal**, įveskite „30301".
11. Laukelyje **Pašto kodo rikiavimas į**, įveskite „30318".
12. Laukelyje **Šalies regiono rikiavimas**, įveskite „USA".
13. Laukelyje **<1 00 svarai** įveskite „100".
    * Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 1 svaras.  
14. Laukelyje **<5 00 svarai** įveskite „300".
    * Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 5 svarai.  
15. Laukelyje **<20 00 svarai** įveskite „500".
    * Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 20 svarų.  
16. Laukelyje **<100 00 svarai** įveskite „1000".
    * Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 100 svarų.  
17. Laukelyje **<1 000 00 svarai** įveskite „3000".
    * Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 1000 svarų.  
18. Pasirinkite **Įrašyti**.
19. Uždarykite puslapį.

## <a name="assign-rate-base"></a>Priskirti tarifo pagrindą

1. Išplėskite **Reitinguoti pagrindinius priskyrimus** skyrių.
2. Pasirinkite **Naujas**.
    * Kiekvienam pagrindiniam tarifui galite priskirti keletą tarifų pagrindų. Tai sudaro galimybę kiekvienam vežėjui sukurti keletą skirtingų kainos apvalinimo taisyklių, atsižvelgiant į paskirties vietas, paslaugas ar skirtingus tarifų pagrindus. Šioje procedūroje sukursite tik vieną tarifo pagrindo priskyrimą.  
3. Lauke **Pavadinimas** įveskite reikšmę.
4. Laukelyje **Reitinguoti pagrindinius duomenis** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.
5. Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.
6. Laukelyje **Paslaugos** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.
9. Laukelyje **Paėmimo pašto kodas**, įveskite „98052".
    * Nurodykite, nuo kurio pašto kodo galios šis tarifo pagrindo priskyrimas.
10. Laukelyje **Paėmimo regiono rikiavimas**, įveskite „USA".
11. Pasirinkite **Įrašyti**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]