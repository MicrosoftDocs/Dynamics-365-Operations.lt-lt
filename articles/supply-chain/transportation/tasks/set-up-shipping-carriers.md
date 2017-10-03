--- 
title: "Siuntų vežėjų nustatymas"
description: "Ši procedūra nurodo, kaip nustatyti siuntų vežėją ir nurodyti kitą informaciją, tokią kaip paslauga, siuntimo būdas, transportavimo mokėjimo priemonė, transportavimo apribojimai ir siuntimo tarifas."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: eec121859b7135741ccf204fd507ef0790f1c8d4
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-shipping-carriers"></a>Siuntų vežėjų nustatymas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip nustatyti siuntų vežėją ir nurodyti kitą informaciją, tokią kaip paslauga, siuntimo būdas, transportavimo mokėjimo priemonė, transportavimo apribojimai ir siuntimo tarifas. Transportavimo koordinatorius tada gali priskirti siuntų vežėją gaunamam arba siunčiamam kroviniui.


## <a name="create-a-new-shipping-carrier"></a>Kurti naują siuntų vežėją
1. Pasirinkite Transportavimo valdymas > Nustatymas > Vežėjai > Siuntų vežėjai.
2. Spustelėkite Naujas.
3. Lauke „Siuntų vežėjas“ įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke „Režimas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Įvesti bendrą siuntų vežėjo informaciją
1. Perjunkite skyriaus „Apžvalga“ išplėtimą.
2. Pažymėkite arba atžymėkite žymės langelį „Suaktyvinti siuntų vežėją“.
3. Lauke „Tiekėjas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite tiekėjo sąskaitą, kad priskirtumėte siuntų vežėjui.  
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke „Transportavimo mokėjimo priemonės tipas“ pasirinkite parinktį.
    * Pasirinkite vadovą, kad galėtumėte naudoti transportavimo mokėjimo priemonės puslapį, arba pasirinkite EDI, kad atnaujintumėte mokėjimo priemonę naudodami elektroninių duomenų mainus (EDI).  
7. Pažymėkite arba atžymėkite žymės langelį „Suaktyvinti vežėjo vertinimą“.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Sukurti siuntų vežėjui būtinas paslaugas
1. Perjunkite skyriaus „Paslaugos“ išplėtimą.
2. Spustelėkite Naujas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke „Vežėjo paslauga“ įveskite reikšmę.
5. Lauke Pavadinimas surinkite reikšmę.
6. Lauke „Transportavimo metodas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Nustatyti vežėjo adresą (pasirinktinai)
1. Perjunkite dalies Adresai išplėtimą.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas arba aprašas surinkite reikšmę.
4. Lauke „Šalis / Regionas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke „Pašto kodas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke Gatvė surinkite reikšmę.
10. Spustelėkite GERAI.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Nustatyti siuntų vežėjo vertinimo šabloną
1. Perjunkite skyriaus „Vertinimo šablonai“ išplėtimą.
2. Spustelėkite Naujas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke „Vertinimo profilis“ įveskite reikšmę.
5. Lauke Pavadinimas surinkite reikšmę.
6. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
10. Sąraše raskite ir pasirinkite norimą įrašą.
11. Sąraše spustelėkite saitą pasirinktoje eilutėje.
12. Lauke „Tarifų mechanizmas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite tarifų mechanizmą, kuris atitinka jūsų sutartį su vežėju.  
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Sąraše spustelėkite saitą pasirinktoje eilutėje.
15. Lauke „Pagrindinis tarifas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
16. Sąraše raskite ir pasirinkite norimą įrašą.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Lauke „Tranzito laiko mechanizmas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
19. Sąraše spustelėkite saitą pasirinktoje eilutėje.
20. Spustelėkite Įrašyti.


