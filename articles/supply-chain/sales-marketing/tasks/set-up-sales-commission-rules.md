---
title: Nustatyti pardavimo komisinių taisykles
description: Ši procedūra nurodo, kaip nustatyti ir įgalinti pardavimo komisinių skaičiavimą ir sekimą.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4507405039cd27a071e0f0ed8bfad31fd30f16f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203209"
---
# <a name="set-up-sales-commission-rules"></a>Nustatyti pardavimo komisinių taisykles

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip nustatyti ir įgalinti pardavimo komisinių skaičiavimą ir sekimą. Procedūra nurodo, kaip sukurti klientų ir prekių komisinių grupes ir kaip susieti pasirinktą klientą ir produktą su atitinkamomis grupėmis. Tada tos grupės naudojamos nustatant komisinių skaičiavimą, kad būtų galima sukurti kliento, prekės ir pardavimo atstovų derinį, kuris turi atitikti pardavimo užsakyme nurodytą derinį, kad pardavėjai turėtų teisę į komisinius. Nėra būtina sukurti klientų ir prekių komisinių grupes, nes komisiniai gali būti apskaičiuojami ir atskiram klientui ir / arba prekei. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisinių grupių ir komisinių tarifų nustatymas
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Komisiniai > Komisinius gaunančių klientų grupės**.
2. Pasirinkite **Naujas**.
3. Lauke **Grupė** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Pasirinkite **Įrašyti**.
6. Uždarykite puslapį.
7. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Komisiniai > Prekių grupės**.
8. Pasirinkite **Naujas**.
9. Lauke **Grupė** įveskite reikšmę.
10. Lauke **Pavadinimas** įveskite reikšmę.
11. Pasirinkite **Įrašyti**.
12. Uždarykite puslapį.
13. Eikite į **Pardavimai ir rinkodara > Komisiniai > Pardavimo grupės**.
    - Komisinių pardavimo grupė nurodo pardavimo atstovo vaidmenis atliekančius darbuotojus, kuriems, kai su tam tikra pardavimo grupe susietas klientas nusiperka tam tikras prekes, gali būti paskirti komisiniai.  
    - Demonstracinių duomenų įmonėje USMF yra pardavimo grupė, pavadinta "Pard. atst. JAV."  
14. Pasirinkę **Veiksmų sritis**, pasirinkite **Bendra**.
15. Spustelėkite **Pard. atst.**. Puslapyje Pardavimo atstovai rodomas įmonės pardavimo skyriuje dirbančių ir su specialia komisinių grupe susietų žmonių sąrašas. Tai pačiai grupei galite priskirti keletą pardavimo atstovų ir nurodyti jiems priklausančios komisinio mokesčio dalies procentinę reikšmę. Bendra komisinių dalis tarp visų darbuotojų neturi viršyti 100. 
16. Sąraše pažymėkite pasirinktą eilutę.
17. Pasirinkite **Redaguoti**.
18. Nustatykite parinkties **Komisinių dalis** reikšmę „50“.
19. Spustelėkite **Naujas**.
20. Lauke **Pavadinimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
21. Norėdami rasti įrašų, naudokite **Spartusis filtras**. Pavyzdžiui, filtruokite lauką Pavadinimas reikšme „Susan Burk‟.
22. Spustelėkite **Pažymėti**.
23. Nustatykite parinkties **Komisinių dalis** reikšmę „50“.
24. Spustelėkite **Įrašyti**.
25. Eikite į **Pardavimai ir rinkodara > Komisiniai > Komisinių skaičiavimas**. Puslapyje **Komisinių skaičiavimas** nurodote komisinių tarifą, kurį darbuotojas turėtų gauti už pardavimo operaciją, jei joje naudojamas iš anksto nustatytas kliento ir produkto derinys. Nustatydami komisinių tarifą turite nurodyti komisinių skaičiavimo pagrindą ir tai, ar prie jų turėtų būti priskaičiuojamos nuolaidos. Taip pat galite įvesti galiojimo laikotarpį, kuriuo komisinių tarifas aktyvus.  
26. Spustelėkite **Naujas**.
27. Lauke **Prekės kodas** pasirinkite „Grupė“.
28. Lauke **Prekės ryšys** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
29. Sąraše raskite ir pasirinkite anksčiau sukurtą grupę.
30. Lauke **Kliento kodas** pasirinkite Grupė.
31. Lauke**Kliento ryšys** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
32. Sąraše raskite ir pasirinkite anksčiau nustatytą grupę.
33. Lauke **Pard. atst. ryšys** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
34. Sąraše raskite ir pasirinkite norimą įrašą.
    - Palikite parinktį „Prieš apskaičiuojant eilutės nuolaidą“.  
    - Palikite parinktį „Įplaukos“ kaip komisinių vertės skaičiavimo pagrindą.    
35. Lauke Komisinių procentas įveskite skaičių.
36. Spustelėkite **Įrašyti**.

## <a name="setting-up-commission-posting"></a>Komisinių registravimo nustatymas
1. Eikite į **Naršymo sritis > Pardavimas ir rinkodara > Komisiniai > Komisinių registravimas**. Komisiniai mokesčiai mokami darbuotojams ir todėl turi būti nustatyti taip, kad būtų užtikrintas tinkamas finansų registravimas atitinkamose **DK** sąskaitose. Tai atliekama puslapyje **Komisinių registravimas**. Peržiūrėkite dabartinei įmonei galimus taikyti nustatymus. Paprastai komisinių sumos registruojamos paskirtoje išlaidų sąskaitoje ir koresponduojamos į paskirtą mokėtinos sumos sąskaitą. Jei neturite nustatę komisinių registravimo taisyklių, sistema negalės išrašyti pardavimo užsakymo, kuriam gali būti paskaičiuoti komisiniai, sąskaitos faktūros.  
2. Uždarykite puslapį.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Komisinių grupės priskyrimas klientui ir produktui
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Klientai > Visi klientai**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite **Redaguoti**.
5. Išplėskite dalį **Pardavimo užsakymo numatytieji nustatymai**.
6. Lauke **Komisinių grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše pasirinkite anksčiau sukurtą grupę.
8. Lauke **Pardavimo grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Spustelėkite **Įrašyti**.
11. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.
12. Norėdami rasti įrašų, naudokite **Filtras**. Pvz., filtruokite lauką Prekės numeris reikšme „T0020 “.
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Spustelėkite **Redaguoti**.
15. Išplėskite dalį **Pardavimas**.
16. Lauke **Komisinių grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
17. Sąraše pasirinkite anksčiau sukurtą komisinių grupę.
18. Pasirinkite **Įrašyti**.

