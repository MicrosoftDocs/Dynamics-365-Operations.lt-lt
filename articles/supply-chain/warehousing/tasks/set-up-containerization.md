---
title: Krovimo į konteinerius nustatymas
description: Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f28be8993d5fc0a1632cf7a534808e64980c09b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977043"
---
# <a name="set-up-containerization"></a>Krovimo į konteinerius nustatymas

[!include [banner](../../includes/banner.md)]

Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas. Vykstant automatizuoto krovimo į konteinerius procesui, apdorojant bangą siuntoms sukuriami konteineriai ir paėmimo darbas, o darbo eilutes galima išskaidyti į kiekius, telpančius į konteinerius. Taip sandėlio darbininkams lengviau prekes paimti tiesiai į pasirinktą konteinerį. Palyginti su rankinio pakavimo procesu, tokias užduotis kaip konteinerių kūrimas, prekių priskyrimas ir konteinerių uždarymas automatizuoja sistema. Atliekant šią procedūrą naudojama demonstracinė įmonė USMF, o ją atlieka sandėlio vadovas.


## <a name="set-up-a-wave-template"></a>Bangos šablono nustatymas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Konfigūracija > Bangos > Bangos šablonai**.
2. Pasirinkite **Naujas**.
3. Lauke **Bangos šablono pavadinimas** įveskite reikšmę.
4. Lauke **Bangos šablono aprašas** įveskite reikšmę.
5. Lauke **Teritorija** įveskite arba pasirinkite reikšmę.
6. Lauke **Sandėlis** įveskite arba pasirinkite reikšmę.
7. Išplėskite dalį **Metodai**. Srityje **Pasirinkti metodai** pateikiami pasirinkto bangos šablono tipo metodai. Bangos šablone turi būti krovimo į konteinerius metodas.  
8. Lauke **Bangos veiksmo kodas** įveskite reikšmę. Įveskite įtraukto metodo bangos veiksmo kodą – tai gali būti bet koks kodas. Galima pridėti metodą daugiau nei vieną kartą ir priskirti skirtingus bangos veiksmo kodus. Norėdami tai padaryti, puslapyje **Bangos apdorojimo metodai** prie šio metodo pasirinkite **Galima kartoti šiuo metodu**.  
9. Pasirinkite **Įrašyti**.
10. Uždarykite puslapį.

## <a name="set-up-a-container-type"></a>Konteinerio tipo nustatymas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Konfigūracija > Konteineriai > Konteinerių tipai**. Savo konteinerius galite apibrėžti puslapyje **Konteinerių tipai**. Galite sukonfigūruoti faktines konteinerių dimensijas – taros svorį, didžiausią svorį, didžiausią tūrį, ilgį, plotį ir aukštį. Šiame pavyzdyje turime tris skirtingus dėžių dydžius.  
2. Pasirinkite **Naujas**.
3. Lauke **Konteinerio tipo kodas** įveskite reikšmę.
4. Lauke **Taros svoris** įveskite skaičių.
5. Lauke **Maksimalus svoris** įveskite skaičių.
6. Lauke **Tūris** įveskite skaičių.
7. Lauke **Ilgis** įveskite skaičių.
8. Lauke **Plotis** įveskite skaičių.
9. Lauke **Aukštis** įveskite skaičių.
10. Lauke **Aprašas** įveskite reikšmę.
11. Pasirinkite **Įrašyti**.
13. Norėdami sukurti iš viso tris konteinerių tipus, 2–11 etapus pakartokite dar du kartus.
14. Uždarykite puslapį.

## <a name="set-up-a-container-group"></a>Konteinerių grupės nustatymas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Konfigūracija > Konteineriai > Konteinerių grupės**.
2. Veiksmų srityje pasirinkite **Naujas**. Galite nustatyti logines konteinerių tipų grupes. Kiekvienai grupei galite nurodyti seką, kuria bus pakuojami konteineriai, ir konteinerių užpildymo procentą. Naudojami prekės matmenų dydžiai siekiant nustatyti, ar ji tilps konteineryje. Naudojamas konteineris, artimiausias prekės dydžio matmenims. Jei grupėje turite kelis konteinerių tipus, rekomenduojame išdėstyti seką pagal dydį, kad didžiausias konteineris sekoje būtų pirmas (Nr. 1), o mažiausias – paskutinis.    
3. Lauke **Konteinerio grupės ID** įveskite reikšmę, kurią sukūrėte anksčiau.
4. Lauke **Aprašas** įveskite reikšmę.
5. 2–4 etapus pakartokite visiems trims anksčiau sukurtiems konteinerių tipams.
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.

## <a name="set-up-a-container-build-template"></a>Konteinerio kūrimo šablono nustatymas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Konteineriai > Konteinerio kūrimo šablonai**.
2. Pasirinkite **Naujas**. Konteinerio kūrimo šablonas priklauso nuo to, kuris iš krovimo į konteinerius procesų atliekamas. Kiekvienu konteinerio kūrimo šablonu apibrėžiamas vienas krovimo į konteinerius procesas, kurį naudos bangos šablonas. Parinktimi **Redaguoti užklausą** galima apibrėžti sąlygas, kuriomis pasirinktas šablonas bus apdorojamas. Pavyzdžiui, galbūt krovimo į konteinerius procesą norėsite vykdyti tik su konkrečiais klientais, produktais ar sandėliais, arba į šabloną galite įtraukti atitinkamų užklausos intervalų. Lauku **Bangos veiksmo kodas** nustatoma, kaip konteinerio kūrimo šablonas susietas su bangos šablono veiksmais. Kai vykdoma banga, ja nustatoma, kuris konteinerio kūrimo šablonas (-ai) naudojamas inicijuoti krovimo į konteinerius procesui. Lauku Pagrindinis užklausos tipas nustatoma, ką pakuoti ir kuo grįsti filtro užklausą. 
3. Lauke **Konteinerio šablono ID** įveskite reikšmę.
4. Lauke **Konteinerių grupės ID** įveskite arba pasirinkite reikšmę.
5. Lauke **Bangos veiksmo kodas** įveskite reikšmę.
6. Pažymėkite žymės langelį **Leisti skaidyti paėmimus**.
7. Pasirinkite **Įrašyti**.
8. Pasirinkite **Konteinerio maišymo apribojimai**. Maišymo logikos skaidymais galima nustatyti paskirstymo eilučių pakavimo konteineriuose taisykles. Pavyzdžiui, jei įtrauksite **Laukas Prekės numeris**, prekes priskiriant konteineriams ir esant naujam prekės numeriui, bus sukurtas naujas konteineris. Taip darbininkai tame pačiame konteineryje nesupakuos paskirstymo eilučių dviem skirtingiems klientams.  
9. Pasirinkite **Naujas**.
10. Lauke **Lentelė** pasirinkite parinktį.
11. Lauke **Laukų pasirinkimas** įveskite arba pasirinkite reikšmę.
12. Pasirinkite **Gerai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]