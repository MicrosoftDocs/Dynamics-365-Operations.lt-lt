--- 
title: "Nustatyti ES pardavimo sąrašo ataskaitas"
description: "Ši užduotis skirta jums padėti peržiūrėti būtinąsias sąlygas, kurių reikia laikytis norint teikti ES pardavimo sąrašo ataskaitas."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5c415b06debc882c9ecdacc1c89e64325df4d4c7
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-eu-sales-list-reporting"></a>Nustatyti ES pardavimo sąrašo ataskaitas

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ši užduotis skirta jums padėti peržiūrėti būtinąsias sąlygas, kurių reikia laikytis norint teikti ES pardavimo sąrašo ataskaitas. Daugiau informacijos apie ES pardavimo sąrašų ataskaitas, įskaitant būtinąsias sąlygas, žr. „Dynamics 365 for Finance and Operations“ žinyne.

ES pardavimo sąrašo ataskaitų „wiki‟ puslapį. Vadovas buvo sukurtas naudojant demonstracinių duomenų įmonės DEMF paslaugas ir dėl to kaip šalies / regiono pavyzdį naudojant Vokietiją. Vadovas taip pat kaip ES šalies / regiono pavyzdį naudoja Portugaliją.

Šios užduotys yra skirtos sistemų administratoriams.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Elektroninių ataskaitų konfigūracijų, skirtų ES pardavimų sąrašo ataskaitoms, importavimas
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Nustatyti kaip aktyvų.
3. Spustelėkite Saugyklos.
4. Spustelėkite Atidaryti.
5. Veiksmų srityje spustelėkite Parinktys.
6. Spustelėkite Išplėstinis filtras / rūšiavimas.
7. Spustelėkite Pridėti.
8. Lauke Laukas pasirinkite „Konfigūracijos pavadinimas“.
9. Lauke Kriterijai įveskite „ES pardavimų sąrašas (DE)“.
10. Spustelėkite GERAI.
11. Spustelėkite Importuoti.
12. Spustelėkite Taip.
13. Veiksmų srityje spustelėkite Parinktys.
14. Spustelėkite Išplėstinis filtras / rūšiavimas.
15. Spustelėkite Nustatyti iš naujo.
16. Spustelėkite Pridėti.
17. Lauke Laukas pasirinkite „Konfigūracijos pavadinimas“.
18. Lauke Kriterijai įveskite „ES pardavimų sąrašas pagal eilučių ataskaitą“.
19. Spustelėkite GERAI.
20. Spustelėkite Importuoti.
21. Spustelėkite Taip.

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>ES pardavimų sąrašo ataskaitų PVM kodų nustatymas
1. Pasirinkite Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai.
2. Naudodami spartųjį filtrą atfiltruokite lauką PVM kodas pagal reikšmę „PVM19“.
3. Išplėskite skyrių Ataskaitų nustatymai.
    * Patikrinkite, ar pasirinkties Neįtraukta nustatymas yra Nr.  
    * Norint pakeisti šį parametrą, jums gali reikėti atrakinti užduoties vadovą.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>ES pardavimų sąrašo ataskaitų PVM grupių nustatymas
1. Eikite į Mokestis > Netiesioginiai mokesčiai > PVM > PVM grupės.
2. Naudodami spartųjį filtrą atfiltruokite lauką PVM grupė pagal reikšmę „AR-DOM“.
3. Spustelėkite Redaguoti.
4. Išplėskite skyrių Nustatymas.
5. Sąraše pasirinkite pirmą eilutę.
6. Pažymėkite žymės langelį Neapmokestinama.
7. Sąraše pasirinkite antrą eilutę.
8. Pažymėkite žymės langelį Neapmokestinama.
9. Sąraše pasirinkite trečią eilutę.
10. Pažymėkite žymės langelį Neapmokestinama.

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>ES pardavimų sąrašo ataskaitų prekių PVM grupių nustatymas
1. Eikite į Mokestis > Netiesioginiai mokesčiai > PVM > Prekės PVM grupės.
2. Naudodami spartųjį filtrą atfiltruokite lauką Prekės PVM grupė pagal reikšmę „VISAS “.
    * Patikrinkite, ar pasirinkties Ataskaitos tipas nustatymas yra „Prekė“.  
    * Norint pakeisti šio lauko reikšmę, jums gali reikėti atrakinti užduoties vadovą.  
3. Naudodami spartųjį filtrą atfiltruokite lauką Prekės PVM grupė pagal reikšmę „RAUDONAS “.
    * Patikrinkite, ar pasirinkties Ataskaitos tipas nustatymas yra „Paslauga“.  
    * Norint pakeisti šio lauko reikšmę, jums gali reikėti atrakinti užduoties vadovą.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>ES pardavimų sąrašo ataskaitų šalies / regiono parametrų nustatymas
1. Eikite į Mokestis > Nustatymas > PVM > Šalies / regiono parametrai.
2. Spustelėkite Naujas.
3. Lauke Šalis / regionas įveskite „PRT“
4. Lauke PVM įveskite „PT“.

## <a name="create-tax-exempt-numbers"></a>PVM mokėtojo kodų kūrimas
1. Eikite į Mokestis > Nustatymas > PVM > PVM mokėtojo kodai.
2. Spustelėkite Naujas.
3. Lauke Šalis / regionas įveskite „PRT“
4. Lauke PVM mokėtojo kodas įveskite „PT12345“.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>ES pardavimų sąrašo ataskaitų parametrų nustatymas
1. Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.
2. Spustelėkite skirtuką ES pardavimų sąrašas.
3. Lauke Perkelti pirkinius pasirinkite Taip.
4. Išplėskite skyrių Apvalinimo taisyklės.
5. Nustatykite skyriaus Apvalinimo taisyklė parinktį „0.1“.
6. Lauke Naudoti minimalią reikšmę pasirinkite Taip.
7. Lauke Dešimtainių dalių skaičius įveskite „2“.
8. Išplėskite skyrių Elektroninės ataskaitos.
9. Lauke Failo formato susiejimas pasirinkite „ES pardavimų sąrašas (DE)“.
10. Lauke Ataskaitos formato susiejimas pasirinkite „ES pardavimų sąrašas pagal eilučių ataskaitą“.
11. Spustelėkite skirtuką Šalies / regiono ypatybės.
    * Patikrinkite, ar lauko Šalies / regiono tipas, skirto šalies / regiono DEU, nustatymas yra „Vietinis“.  
    * Norint pakeisti šio lauko reikšmę, jums gali reikėti atrakinti užduoties vadovą.  
12. Spustelėkite Naujas.
13. Lauke Šalis / regionas įveskite „PRT“
14. Lauke „Intrastat“ kodas įveskite „PT“.
15. Lauke Šalies / regiono tipas pasirinkite „ES“.
16. Spustelėkite skirtuką Numeracijos.
    * Patikrinkite, ar skaičių sekos kodas yra nurodytas priskiriant nuorodai „ES pardavimų sąrašas“.  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Kliento kūrimas ES pardavimų sąrašo ataskaitų demonstraciniams tikslams
1. Pasirinkite Gautinos sumos > Klientai > Visi klientai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite „PRT-001“.
4. Lauke Pavadinimas įveskite „Klientas iš Portugalijos“.
5. Lauke Klientų grupė pasirinkite „10“.
6. Lauke PVM grupė pasirinkite „AR-DOM“.
7. Lauke PVM mokėtojo kodas pasirinkite „PT12345“.
8. Lauke Šalis / regionas įveskite „PRT“
9. Spustelėkite Įrašyti.


