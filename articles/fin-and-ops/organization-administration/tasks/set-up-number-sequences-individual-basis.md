--- 
title: "Atskirų numeracijų nustatymas"
description: "Numerių sekos naudojamos generuojant perskaitomus, unikalius identifikatorius bendrųjų duomenų įrašams ir operacijų įrašams, kuriems jie reikalingi."
author: sericks007
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e2808e57dc8d137fac892d48e99d7687ff1bf81
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Atskirų numeracijų nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Numerių sekos naudojamos generuojant perskaitomus, unikalius identifikatorius bendrųjų duomenų įrašams ir operacijų įrašams, kuriems jie reikalingi. Pagrindinių duomenų arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas nuoroda. Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda. Galite nustatyti visas reikiamas numeracijas tuo pačiu metu naudodami vedlį Numeracijų nustatymas arba galite sukurti ar modifikuoti atskiras numeracijas naudodami puslapį Numeracijos.

1. Pasirinkite Organizacijos administravimas > Numeracijos > Numeracijos.
2. Spustelėkite Numeracija.
3. Lauke Numeracijos kodas įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Išplėskite dalį Aprėpties parametrai.
    * „FastTab“ skirtuke Aprėpties parametrai pasirinkite numeracijos aprėptį ir aprėpties reikšmes.     Apimtis nustato, kokios organizacijos naudoja numeraciją. Be to, numeracijose, kurių aprėptis ne Bendrai naudojama, o kitokia, gali būti segmentų, atitinkančių jų aprėptį. Pvz., numeracijoje, kurios aprėptis Juridinio subjekto, gali būti juridinio subjekto segmentas. Daugiau informacijos apie aprėptis žr. žinyno temoje „Numeracijos apžvalga“.  
6. Išplėskite skyrių Segmentai.
    * „FastTab“ skirtuke Segmentai apibrėžkite numeracijos formatą įtraukdami, pašalindami ir pertvarkydami segmentus.  
    * Visų aprėpčių numeracijose gali būti pastoviųjų segmentų ir raidinių-skaitinių segmentų. Pastoviuosiuose segmentuose yra raidinių-skaitinių simbolių, kurie nekinta. Naudokite šį segmentų tipą, kad tarp numeracijos segmentų įtrauktumėte brūkšnelį ar kitų skyriklių. Skaitiniuose-raidiniuose segmentuose yra skaičių ženklų (#) ir ampersandų (&). Šie simboliai nurodo raides ir skaičius, kurie padidėja kaskart panaudojus skaičių iš sekos. Naudokite skaičiaus ženklą (#) norėdami nurodyti didėjančius skaičius ir ampersandus (&) norėdami nurodyti didėjančias raides. Pvz., pagal formatą #####_2014 sukuriamos sekos 00001_2014, 00002_2014 ir t.t.     Turi būti bent vienas segmentas, sudarytas ir raidžių ir skaitmenų. Apimties segmentai, pvz., įmonė arba juridinis subjektas, nėra būtini. Tačiau jei neįtrauksite apimties segmentų į formatą, pasirinktos nuorodos skaičiai bus vis tiek generuojami pagal apimtį.  
7. Išplėskite dalį Nuorodos.
    * „FastTab“ skirtuke Nuorodos pasirinkite dokumento tipą arba įrašą, kuriam norite priskirti šią numeraciją.     Šis veiksmas nėra būtinas dirbant su sekomis, kurios nurodomos pagal specialius programos naudojimo modelius. Šiais scenarijais naujas skaičius generuojamas naudojant numeracijos kodo arba ID reikšmę nenaudojant nuorodos. Specialiojo programos naudojimo modelio pavyzdys yra kvitų seriją, kuri naudojama konkrečiuose žurnalo pavadinimuose. Tačiau nerekomenduojama naudoti tokių modelių.  
8. Išplėskite skyrių Bendra.
    * „FastTab“ skirtuke Bendra nurodykite, ar numeracija yra neautomatinė, ar tęstinė, ar netęstinė. Be to, galite įvesti mažiausią ir didžiausią skaičius, kuriuos galima naudoti numeracijoje.     Nerekomenduojama keisti netęstinių numeracijų į tęstines numeracijas. Numeracija nebus tikrai tęstinė. Dėl tokio keitimo taip pat gali įvykti besidubliuojančių raktų pažeidimų duomenų bazėje. Be to, tęstinės numeracijos turi daugiau įtakos našumui.   
9. Spustelėkite Įrašyti.


