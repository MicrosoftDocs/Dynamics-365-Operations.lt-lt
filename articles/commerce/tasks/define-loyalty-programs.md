---
title: " Nustatyti lojalumo programas"
description: Ši procedūra padeda nustatyti lojalumo programą su dviem lojalumo pakopomis.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91f30d4d1b66e5b4b90f7df67d8f76a95a100338
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414391"
---
# <a name="define-loyalty-programs"></a> Nustatyti lojalumo programas

[!include [banner](../includes/banner.md)]

Ši procedūra padeda nustatyti lojalumo programą su dviem lojalumo pakopomis. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.

1. Eikite į Mažmeninė prekyba ir prekyba> ... > Lojalumo programos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Pridėti eilutę.
6. Lauke Lygis įveskite skaičių.
7. Lauke Pakopa įveskite lojalumo pakopos pavadinimą.
8. Lauke Aprašas surinkite reikšmę.
9. Lauke Datų intervalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Šis datų intervalas turėtų apimti ateitį. Pavyzdžiui, jei datų intervalas, pasirinktas aukso pakopai, yra vienerių metų laikotarpis, kiekvienas klientas, kuris patenka į aukso pakopą, gali gauti su ja susijusius atlygius vienerius metus. Jei klientui būnant aukso pakopoje ta pakopa jam priskiriama iš naujo, data, kada baigiasi pakopos galiojimas, pratęsiama dar metams, pradedant nuo tos dienos, kai pakopa buvo priskirta iš naujo.  
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Spustelėkite Pridėti eilutę.
12. Lauke Lygis įveskite skaičių.
13. Lauke Pakopa įveskite lojalumo pakopos pavadinimą.
14. Lauke Aprašas surinkite reikšmę.
15. Lauke Datų intervalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
16. Sąraše spustelėkite saitą pasirinktoje eilutėje.
17. Spustelėkite Įrašyti.
18. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pakopos taisyklės nurodo mažiausią atlygio taškų skaičių, kurį reikia surinkti per tam tikrą laikotarpį, norint pakopą priskirti.  
19. Perjunkite sekcijos Pakopos taisyklės išplėtimą.
20. Spustelėkite Naujas.
    * Vienai pakopai galite nustatyti daugiau nei vieną pakopos taisyklę. Pavyzdžiui, galite pasirinkti tris skirtingus kriterijus pakopai gauti: išleidžiant 500 JAV dolerių per mėnesį, išleidžiant 500 JAV dolerių per metus ir įvykdant 20 operacijų per metus. Norėdami tai padaryti, turėsite sukurti tris pakopos taisykles.  
21. Lauke Atlygio taškas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Tai turėtų būti neišnaudojami atlygio už lojalumą taškai.  
22. Sąraše spustelėkite saitą pasirinktoje eilutėje.
23. Lauke Išduotų taškų minimumas įveskite skaičių.
    * Jei pakopa yra žemiausio lygio ir visi klientai gali ją gauti tiesiog dalyvaudami šioje programoje, įveskite „0“.  
24. Lauke Vertinimo data spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Šis datų intervalas turėtų apimti praeitį. Tik šio datų intervalo metu gauti taškai bus įtraukiami skaičiuojant mažiausią išduotų taškų vertę.  
25. Sąraše spustelėkite saitą pasirinktoje eilutėje.
26. Spustelėkite Įrašyti.
27. Sąraše raskite ir pasirinkite norimą įrašą.
28. Spustelėkite Naujas.
29. Lauke Atlygio taškas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
30. Sąraše spustelėkite saitą pasirinktoje eilutėje.
31. Lauke Išduotų taškų minimumas įveskite skaičių.
32. Lauke Vertinimo data spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Šis datų intervalas turėtų apimti praeitį.  
33. Sąraše spustelėkite saitą pasirinktoje eilutėje.
34. Spustelėkite Įrašyti.
35. Spustelėkite Kainų grupės.
    * Jei lojaliems klientams norite suteikti nuolaidas. vieną arba daugiau kainų grupių turėsite priskirti lojalumo programai ir priskirti kainų grupes nuolaidoms. Rekomenduojama nenaudoti kainų grupių skirtingų tipų nuolaidų objektams.  Pavyzdžiui, nenaudokite tos pačios kainų grupės lojalumo nuolaidai ir kanalo nuolaidai.  
36. Lauke Kainų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Puslapio viršuje esantis saitas Kainų grupės yra skirtas lojalumo programai. „Fasttab“ Programos pakopos esantis saitas Kainų grupės yra skirtas tik konkrečiai lojalumo pakopai.  
37. Sąraše spustelėkite saitą pasirinktoje eilutėje.
38. Spustelėkite Įrašyti.
39. Uždarykite puslapį.
40. Spustelėkite Įrašyti.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]