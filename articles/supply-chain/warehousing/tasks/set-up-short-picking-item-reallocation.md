---
title: Prekių perskirstymo nustatymas nevisiško paėmimo atveju
description: Šiame straipsnyje aprašoma, kaip įgalinti sandėlio darbuotojus greitai rasti alternatyvias vietas, jei vietoje, į kurias jie buvo nukreipti, nepakanka atsargų.
author: Mirzaab
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4e6d7f9b09434346cb0f3670d10437ef8197822
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875020"
---
# <a name="set-up-short-picking-item-reallocation"></a>Prekių perskirstymo nustatymas nevisiško paėmimo atveju

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda įgalinti sandėlio darbuotojus greitai rasti kitas vietas, jei toje vietoje, į kurią jie buvo nukreipti, nėra pakankamai atsargų. 

Perskirstymo procesą kontroliuoja **Darbo išimtys** ir naudoja sandėlio **darbuotojas.**

Galima naudoti Automatinius, Neautomatinius arba abu perskirstymo procesus:

- Automatiniame perskirstyme naudojami vietos nurodymai siekiant sužinoti, ar prekės yra pasiekiamos kitoje vietoje. Jei įmanoma, darbas bus atnaujintas ir sandėlio programos vartotojas bus nukreiptas į kitą vietą.
- Neautomatinis perskirstymas leidžia sandėlio programos vartotojui pasirinkti iš vienos ar daugiau vietų, kuriose yra nerezervuoti prekių kiekiai. 
- Automatinis ir neautomatinis – jei sistemai nepavyko atlikti automatinio perskirstymo, o vietos su nerezervuotais kiekiais yra pasiekiamos, naudotojas bus paragintas pasirinkti vietą.

## <a name="set-up-work-exceptions"></a>Nustatyti užduočių išimtis
Galima apibrėžti keletą užduočių išimčių naudojant skirtingas prekių perskirstymo strategijas įgalinti sandėlio darbuotoją pasirinkti vieną iš jų, atsižvelgiant į jo apdorojamos siuntos specifikacijas.

Kuriant šią procedūrą naudota demonstracinių duomenų įmonė yra USMF.

1. **Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Užduotys > Užduočių išimtys**.
2. Spustelėkite **Naujas** 
3. Lauke **Užduoties išimties kodas** įveskite reikšmę. Tai bus šios išimties pavadinimas. Pavyzdžiui, Neautomatinis nevisiškas paėmimas.
4. Lauke **Aprašo laukas** surinkite reikšmę. Tai bus trumpas šios išimties naudojimo aprašas. Pavyzdžiui, „Trumpalaikis išrinkimas“ – prekė yra nepasiekiama.
5. **Išimties** tipo lauke pasirinkite **Trumpalaikis išrinkimas**.
6. Pažymėkite žymės langelį **Koreguoti atsargas**. Ši parinktis automatiškai nustatys atsargų lygį į 0 toje vietoje, iš kurios bus vykdomas trumpalaikis išrinkimas.
7. Lauke **Numatytojo koregavimo tipo kodas** įveskite arba pasirinkite reikšmę. Pavyzdžiui, programoje USMF galite pasirinkti **Pašalinti rezervacijas Adj Out**. Kiekviename koregavimo tipo kode yra keturios charakteristikos: pavadinimas, aprašas, atsargų žurnalo pavadinimas ir **Pašalinti rezervacijas**. Jei funkcija **Pašalinti rezervacijas** yra įjungta, trumpalaikio išrinkimo eilutės rezervacijos bus pašalintos.  
8. Lauke **Prekių perskirstymas** pasirinkite reikšmę, pavyzdžiui, Neautomatinis. Jei pasirinksite Neautomatinis arba Automatinis ir neautomatinis, reikia įgalinti sandėlio darbuotoją reikia naudoti neautomatinio perskirstymo funkciją.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Darbuotojo nustatymas naudoti neautomatinį perskirstymą

Kuriant šią procedūrą naudota demonstracinių duomenų įmonė yra USMF.

1. Uždarykite puslapį.
2. **Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Darbuotojas**.
3. Spustelėkite **Redaguoti**.
4. Pasirinkite darbuotoją iš sąrašo. Pavyzdžiui, Julija Funderburk.
5. Išplėskite „FastTab“ skirtuką **Vartotojai**.
6. Pasirinkite **Vartotojo ID** iš sąrašo. Pavyzdžiui, 24.
7. Išplėskite „FastTab“ skirtuką **Užduotys**.
8. Lauke **Leisti neautomatinį prekių perskirstymą** pasirinkite **Taip**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]