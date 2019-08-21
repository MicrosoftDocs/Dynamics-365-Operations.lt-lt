---
title: Krovimo į konteinerius nustatymas
description: Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba435ee145a8516391d7864bdfe338b0f3862f49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847212"
---
# <a name="set-up-containerization"></a>Krovimo į konteinerius nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas. Vykstant automatizuoto krovimo į konteinerius procesui, apdorojant bangą siuntoms sukuriami konteineriai ir paėmimo darbas, o darbo eilutes galima išskaidyti į kiekius, telpančius į konteinerius. Taip sandėlio darbininkams lengviau prekes paimti tiesiai į pasirinktą konteinerį. Palyginti su rankinio pakavimo procesu, tokias užduotis kaip konteinerių kūrimas, prekių priskyrimas ir konteinerių uždarymas automatizuoja sistema. Atliekant šią procedūrą naudojama demonstracinė įmonė USMF, o ją atlieka sandėlio vadovas.


## <a name="set-up-a-wave-template"></a>Bangos šablono nustatymas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Konfigūracija > Bangos > Bangos šablonai**.
2. Pasirinkite **Naujas**.
3. Lauke **Wave template name** įveskite reikšmę.
4. Lauke **Wave template description** įveskite reikšmę.
5. Lauke **Site** įveskite arba pasirinkite reikšmę.
6. Lauke **Warehouse** įveskite arba pasirinkite reikšmę.
7. Išplėskite dalį **Methods**. Srityje **Selected methods** pateikiami pasirinkto bangos šablono tipo metodai. Bangos šablone turi būti krovimo į konteinerius metodas.  
8. Lauke **Wave step code** įveskite reikšmę. Įveskite įtraukto metodo bangos veiksmo kodą – tai gali būti bet koks kodas. Įtraukti metodą galimą keletą kartų ir galima priskirti skirtingus bangos veiksmų kodus. Norėdami tai padaryti, puslapyje **Wave process methods**prie šio metodo pasirinkite **Repeatable for this method**.  
9. Pasirinkite **Įrašyti**.
10. Uždarykite puslapį.

## <a name="set-up-a-container-type"></a>Konteinerio tipo nustatymas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Konfigūracija > Konteineriai > Konteinerių tipai**. Savo konteinerius galite apibrėžti puslapyje **Container types**. Galite sukonfigūruoti faktines konteinerių dimensijas – taros svorį, didžiausią svorį, didžiausią tūrį, ilgį, plotį ir aukštį. Šiame pavyzdyje turime tris skirtingus dėžių dydžius.  
2. Pasirinkite **Naujas**.
3. Lauke **Container type code** įveskite reikšmę.
4. Lauke **Tare weight** įveskite skaičių.
5. Lauke **Didžiausias svoris** įveskite skaičių.
6. Lauke **Tūris** įveskite skaičių.
7. Lauke **Ilgis** įveskite skaičių.
8. Lauke **Plotis** įveskite skaičių.
9. Lauke **Aukštis** įveskite skaičių.
10. Lauke **Description field**surinkite reikšmę.
11. Pasirinkite **Įrašyti**.
13. Norėdami sukurti iš viso tris konteinerių tipus, 2–11 etapus pakartokite dar du kartus.
14. Uždarykite puslapį.

## <a name="set-up-a-container-group"></a>Konteinerių grupės nustatymas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Konfigūracija > Konteineriai > Konteinerių grupės**.
2. Veiksmų srityje pasirinkite **„Naujas“**. Galite nustatyti logines konteinerių tipų grupes. Kiekvienai grupei galite nurodyti seką, kuria bus pakuojami konteineriai, ir konteinerių užpildymo procentą. Naudojami prekės matmenų dydžiai siekiant nustatyti, ar ji tilps konteineryje. Naudojamas konteineris, artimiausias prekės dydžio matmenims. Jei grupėje turite kelis konteinerių tipus, rekomenduojame išdėstyti seką pagal dydį, kad didžiausias konteineris sekoje būtų pirmas (Nr. 1), o mažiausias – paskutinis.    
3. Lauke **Konteinerio grupės ID** įveskite reikšmę, kurią sukūrėte anksčiau.
4. Lauke **Description field**surinkite reikšmę.
5. 2–4 etapus pakartokite visiems trims anksčiau sukurtiems konteinerių tipams.
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.

## <a name="set-up-a-container-build-template"></a>Konteinerio kūrimo šablono nustatymas
1. Pasirinkite **Modules > Warehouse management > Setup > Containers > Container build templates**.
2. Pasirinkite **Naujas**. Konteinerio kūrimo šablonas priklauso nuo to, kuris iš krovimo į konteinerius procesų atliekamas. Kiekvienu konteinerio kūrimo šablonu apibrėžiamas vienas krovimo į konteinerius procesas, kurį naudos bangos šablonas. Parinktimi **Edit query** galima apibrėžti sąlygas, kuriomis pasirinktas šablonas bus apdorojamas. Pavyzdžiui, galbūt krovimo į konteinerius procesą norėsite vykdyti tik su konkrečiais klientais, produktais ar sandėliais, arba į šabloną galite įtraukti atitinkamų užklausos intervalų. Lauku **Wave step code** nustatoma, kaip konteinerio kūrimo šablonas susietas su bangos šablono veiksmais. Kai vykdoma banga, ja nustatoma, kuris konteinerio kūrimo šablonas (-ai) naudojamas inicijuoti krovimo į konteinerius procesui. Lauku Pagrindinis užklausos tipas nustatoma, ką pakuoti ir kuo grįsti filtro užklausą. 
3. Lauke **Container template ID** įveskite reikšmę.
4. Lauke **Container group ID** įveskite arba pasirinkite reikšmę.
5. Lauke **Wave step code** įveskite reikšmę.
6. Pažymėkite žymės langelį **Allow split picks**.
7. Pasirinkite **Įrašyti**.
8. Spustelėkite**Containier mixing constraints**. Maišymo logikos skaidymais galima nustatyti paskirstymo eilučių pakavimo konteineriuose taisykles. Pavyzdžiui, jei įtrauksite lauką **Item number field**, prekes priskiriant konteineriams ir esant naujam prekės numeriui, bus sukurtas naujas konteineris. Taip darbininkai tame pačiame konteineryje nesupakuos paskirstymo eilučių dviem skirtingiems klientams.  
9. Pasirinkite **Naujas**.
10. Lauke **Table** pasirinkite parinktį.
11. Lauke **Field Select** įveskite arba pasirinkite reikšmę.
12. Pasirinkite **Gerai**.

