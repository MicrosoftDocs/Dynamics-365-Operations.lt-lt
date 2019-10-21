---
title: Atskirų numeracijų nustatymas
description: Šiame straipsnyje aprašoma, kaip nustatyti skaičių sekas individualiai.
author: sericks007
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 818e641d19444e94a287134b68b25d52a05021d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189872"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Atskirų numeracijų nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti skaičių sekas individualiai. Numerių sekos naudojamos generuojant perskaitomus, unikalius identifikatorius bendrųjų duomenų įrašams ir operacijų įrašams, kuriems jie reikalingi. Pagrindinių duomenų arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas nuoroda. Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda. Galite nustatyti visas reikiamas numeracijas tuo pačiu metu naudodami vedlį **Nustatyri numeraciją** arba galite sukurti ar modifikuoti atskiras numeracijas naudodami puslapį **Numeracija**.

1. Eikite į **naršymo sritį > Moduliai > Organizacijos administravimas > Numeracija > Numeracija**.
2. Pasirinkite **Numeravimas**.
3. Lauke **Numeracijos kodas** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. „FastTab“ skirtuke **Aprėpties parametrai** pasirinkite numeracijos aprėptį ir aprėpties reikšmes ir pasirinkite reikšmes iš sąrašo. Apimtis nustato, kokios organizacijos naudoja numeraciją. Be to, numeracijose, kurių aprėptis ne **Bendrinama**, o kitokia, gali būti segmentų, atitinkančių jų aprėptį. Pvz., numeracijoje, kurios aprėptis **Juridinis subjektas**, gali būti juridinio subjekto segmentas. Daugiau informacijos apie aprėptis žr. žinyno temoje [Numeracijos apžvalga](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview). 
6. Išplėskite skyrių **Segmentai**.
    - Būdami „FastTab“  nustatykite numeracijos formatą įtraukdami, pašalindami ir pertvarkydami segmentus.  
    - Visų aprėpčių numeracijose gali būti *Pastovūs segmentai* ir *Raidiniai-skaitiniai segmentai*. Pastoviuosiuose segmentuose yra raidinių-skaitinių simbolių, kurie nekinta. Naudokite šį segmentų tipą, kad tarp numeracijos segmentų įtrauktumėte brūkšnelį ar kitų skyriklių. Skaitiniuose-raidiniuose segmentuose yra skaičių ženklų (#) ir ampersandų (&). Šie simboliai nurodo raides ir skaičius, kurie padidėja kaskart panaudojus skaičių iš sekos. Naudokite skaičiaus ženklą (#) norėdami nurodyti didėjančius skaičius ir ampersandus (&) norėdami nurodyti didėjančias raides. Pvz., pagal formatą `#####_2014`sukuriamos sekos,`00002_2014` `00001_2014`ir t.t. Turi būti bent vienas segmentas, sudarytas ir raidžių ir skaitmenų. Apimties segmentai, pvz., įmonė arba juridinis subjektas, nėra būtini. Tačiau jei neįtrauksite apimties segmentų į formatą, pasirinktos nuorodos skaičiai bus vis tiek generuojami pagal apimtį.  
7. Išplėskite dalį **Nurodos**. Būdami „FastTab“  pasirinkite dokumento tipą arba įrašą, kuriam norite priskirti šią numeraciją. Šis veiksmas nėra būtinas dirbant su sekomis, kurios nurodomos pagal specialius programos naudojimo modelius. Šiais scenarijais naujas skaičius generuojamas naudojant numeracijos kodo arba ID reikšmę nenaudojant nuorodos. Specialiojo programos naudojimo modelio pavyzdys yra kvitų seriją, kuri naudojama konkrečiuose žurnalo pavadinimuose. Tačiau nerekomenduojama naudoti tokių modelių.  
8. Išplėskite skyrių **Bendra**. „FastTab“ skirtuke Bendra nurodykite, ar numeracija yra neautomatinė, ar tęstinė, ar netęstinė. Be to, galite įvesti mažiausią ir didžiausią skaičius, kuriuos galima naudoti numeracijoje. Nerekomenduojama keisti netęstinių numeracijų į tęstines numeracijas. Numeracija nebus tikrai tęstinė. Dėl tokio keitimo taip pat gali įvykti besidubliuojančių raktų pažeidimų duomenų bazėje. Be to, tęstinės numeracijos turi daugiau įtakos našumui.   
9. Spustelėkite **Įrašyti**.

