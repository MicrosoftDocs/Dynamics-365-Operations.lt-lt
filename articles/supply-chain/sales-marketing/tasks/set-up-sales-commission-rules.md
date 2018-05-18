--- 
title: "Nustatyti pardavimo komisinių taisykles"
description: "Ši procedūra nurodo, kaip nustatyti ir įgalinti pardavimo komisinių skaičiavimą ir sekimą."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 3d5c38b1f07803242350fe016b45c45d49c0b59b
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="set-up-sales-commission-rules"></a>Nustatyti pardavimo komisinių taisykles

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip nustatyti ir įgalinti pardavimo komisinių skaičiavimą ir sekimą. Procedūra nurodo, kaip sukurti klientų ir prekių komisinių grupes ir kaip susieti pasirinktą klientą ir produktą su atitinkamomis grupėmis. Tada tos grupės naudojamos nustatant komisinių skaičiavimą, kad būtų galima sukurti kliento, prekės ir pardavimo atstovų derinį, kuris turi atitikti pardavimo užsakyme nurodytą derinį, kad pardavėjai turėtų teisę į komisinius. Nėra būtina sukurti klientų ir prekių komisinių grupes, nes komisiniai gali būti apskaičiuojami ir atskiram klientui ir / arba prekei. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisinių grupių ir komisinių tarifų nustatymas
1. Pasirinkite Pardavimai ir rinkodara > Komisiniai > Komisinius gaunančių klientų grupės.
2. Spustelėkite Naujas.
3. Lauke Grupė įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Spustelėkite Įrašyti.
6. Uždarykite puslapį.
7. Pasirinkite Pardavimai ir rinkodara > Komisiniai > Prekių grupės.
8. Spustelėkite Naujas.
9. Lauke Grupė įveskite reikšmę.
10. Lauke Pavadinimas surinkite reikšmę.
11. Uždarykite puslapį.
12. Pasirinkite Pardavimai ir rinkodara > Komisiniai > Pardavimo grupės.
    * Komisinių pardavimo grupė nurodo pardavimo atstovo vaidmenis atliekančius darbuotojus, kuriems, kai su tam tikra pardavimo grupe susietas klientas nusiperka tam tikras prekes, gali būti paskirti komisiniai.  
    * Demonstracinių duomenų įmonėje USMF yra pardavimo grupė, pavadinta "Pard. atst. JAV."  
13. Veiksmų srityje spustelėkite Bendra.
14. Spustelėkite Pardavimo atstovas.
    * Puslapyje Pardavimo atstovai rodomas įmonės pardavimo skyriuje dirbančių ir su specialia komisinių grupe susietų žmonių sąrašas. Tai pačiai grupei galite priskirti keletą pardavimo atstovų ir nurodyti jiems priklausančios komisinio mokesčio dalies procentinę reikšmę. Bendra komisinių dalis tarp visų darbuotojų neturi viršyti 100.  
15. Sąraše pažymėkite pasirinktą eilutę.
16. Spustelėkite Redaguoti.
17. Nustatykite pasirinkties Komisinių dalis reikšmę „50“.
18. Spustelėkite Naujas.
19. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
20. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pavyzdžiui, filtruokite lauką Pavadinimas reikšme „Susan Burk‟.
21. Spustelėkite Pažymėti.
22. Nustatykite pasirinkties Komisinių dalis reikšmę „50“.
23. Spustelėkite Įrašyti.
24. Pasirinkite Pardavimai ir rinkodara > Komisiniai > Komisinių skaičiavimas.
    * Komisinių skaičiavimo puslapyje nurodote komisinių tarifą, kurį darbuotojas turėtų gauti už pardavimo operaciją, jei joje naudojamas iš anksto nustatytas kliento ir produkto derinys. Nustatydami komisinių tarifą turite nurodyti komisinių skaičiavimo pagrindą ir tai, ar prie jų turėtų būti priskaičiuojamos nuolaidos. Taip pat galite įvesti galiojimo laikotarpį, kuriuo komisinių tarifas aktyvus.  
25. Spustelėkite Naujas.
26. Lauke Prekės kodas pasirinkite „Grupė‟.
27. Lauke „Prekės ryšys“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
28. Sąraše raskite ir pasirinkite anksčiau sukurtą grupę.
29. Sąraše spustelėkite saitą pasirinktoje eilutėje.
30. Lauke Kliento kodas pasirinkite „Grupė‟.
31. Lauke Kliento ryšys spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
32. Sąraše raskite ir pasirinkite anksčiau nustatytą grupę.
33. Lauke Pard. atst. ryšys spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
34. Sąraše raskite ir pasirinkite norimą įrašą.
    * Palikite parinktį „Prieš apskaičiuojant eilutės nuolaidą“.  
    * Palikite parinktį „Įplaukos“ kaip komisinių vertės skaičiavimo pagrindą.    
35. Lauke Komisinių procentas įveskite skaičių.
36. Spustelėkite Įrašyti.

## <a name="setting-up-commission-posting"></a>Komisinių registravimo nustatymas
1. Pasirinkite Pardavimai ir rinkodara > Komisiniai > Komisinių registravimas.
    * Komisiniai mokesčiai mokami darbuotojams ir todėl turi būti nustatyti taip, kad būtų užtikrintas teisingas finansų registravimas atitinkamose DK sąskaitose. Tai atliekama puslapyje Komisinių registravimas. Peržiūrėkite dabartinei įmonei galimus taikyti nustatymus. Paprastai komisinių sumos registruojamos paskirtoje išlaidų sąskaitoje ir koresponduojamos į paskirtą mokėtinos sumos sąskaitą. Jei neturite nustatę komisinių registravimo taisyklių, sistema negalės išrašyti pardavimo užsakymo, kuriam gali būti paskaičiuoti komisiniai, sąskaitos faktūros.  
2. Uždarykite puslapį.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Komisinių grupės priskyrimas klientui ir produktui
1. Pasirinkite Pardavimas ir rinkodara > Klientai > Visi klientai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite Redaguoti.
5. Išplėskite skyrių Pardavimo užsakymo numatytieji nustatymai.
6. Lauke Komisinių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše pasirinkite anksčiau sukurtą grupę.
8. Lauke Pardavimo grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Spustelėkite Įrašyti.
11. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
12. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Prekės numeris reikšme „T0020 “.
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Spustelėkite Redaguoti.
15. Išplėskite skyrių Pardavimas.
16. Lauke Komisinių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
17. Sąraše pasirinkite anksčiau sukurtą komisinių grupę.


