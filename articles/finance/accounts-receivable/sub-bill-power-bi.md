---
title: Prenumeratų sąskaitų valdymo „Power BI“ turinys
description: Šiame straipsnyje aprašoma, kas yra abonemento atsiskaitymo turinyje Microsoft Power BI.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: 6cee01eb5b8bb8296b6e7f638b565c999ccc023e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849966"
---
# <a name="subscription-billing-power-bi-content"></a>Prenumeratų sąskaitų valdymo „Power BI“ turinys

[!include[banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kas yra abonemento atsiskaitymo turinyje Microsoft Power BI. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti. 

## <a name="overview"></a>Apžvalga

Abonemento atsiskaitymo turinys Power BI buvo sukurtas abonementinių sąskaitų tarnautojams ir vadovams. Joje pateikiama pagrindinė abonemento atsiskaitymo metrika, pvz., kas mėnesį pasikartojančios įplaukos (MRR) atsiskaitymo grafikams, mažėjantis balansas ir atidėjimo grafikų informacija. Ji naudoja sąskaitų pateikimo grafikų ir atidėjimo grafikų duomenis pasikartojančių pajamų ir įplaukų apžvalgai pateikti.

Turinyje Power BI yra trys skirtukai, kurie pateikia keturias analitines ataskaitas: 

- **Analitikai – MRR** – šiame skirtuke pateikiama periodinių **mėnesinių** sąskaitų pateikimo ataskaita ir **atsiskaitymo grafiko informacijos** ataskaita.
- **Analitikai – šio** skirtuko lapas pateikia **įplaukų ataskaitą**.
- **Analitikai – mažėjantis balansas** – šis skirtukas pateikia mažėjančios **vertės** ataskaitą.

## <a name="view-data-on-the-analytical-reports"></a>Peržiūrėti analitinių ataskaitų duomenis

Prieš tai, kai galėsite peržiūrėti analitinių ataskaitų duomenis, turite paleisti periodinį procesą, kuris sugeneruoja ataskaitų duomenis kiekvienai ataskaitai. Šie duomenys, kurių reikia ataskaitoms, turi būti sugeneruoti, nes jie tiesiai duomenų bazėje saugomi. 

1. Eikite į **Abonemento sąskaitų pateikimo \> periodines sutarties atsiskaitymo \> periodines užduotis \> MRR analitinės** ataskaitos paketinį vykdymą ir atlikite šiuos veiksmus:

    1. Įvesti ne daugiau kaip trijų metų datos diapazoną.
    2. Pasirinktinai: nustatykite pasikartojančią paketinio vykdymo užduotį, kad duomenys būtų periodiškai atnaujinami.
    3. Pasirinkite **Gerai**.

2. Kai paketinė užduotis baigiama vykdyti, eikite į sistemos **administravimo nustatymo \>\> objektų saugyklą** ir **atnaujinkite MRR ataskaitos suminį** matavimą. 
3. Eikite **į Abonemento sąskaitų \> išrašymo įplaukų ir išlaidų atidėjimų periodines \> užduotis \> analitinės ataskaitos paketinio vykdymo** eiga ir atlikite šiuos veiksmus:

    1. Įveskite ne ilgesnį nei 26 laikotarpių pradžios ir pabaigos datą. 
    2. Jei norite peržiūrėti dabartinio laikotarpio prognozuojamą buvusių laikotarpių sumą, dabartinio **laikotarpio prognozės praeities sumas nustatykite** kaip **Taip**.
    3. Pasirinktinai: nustatykite pasikartojančią paketinio vykdymo užduotį, kad duomenys būtų periodiškai atnaujinami.
    4. Pasirinkite **Gerai**. 

4. Kai paketinė užduotis baigiama vykdyti, eikite į Sistemos **administravimo nustatymo \>\> objektų saugyklą** ir atnaujinkite ataskaitos **sujungti** matavimą.
5. Eikite į **Abonemento sąskaitų išrašymo \> įplaukų ir išlaidų atidėjimų periodines \> užduotis \> Analitinės ataskaitos mažėjančios vertės paketinį** vykdymą ir atlikite šiuos veiksmus:

    1. Įveskite ne ilgesnį nei 26 laikotarpių pradžios ir pabaigos datą. 
    2. Jei norite peržiūrėti dabartinio laikotarpio prognozuojamą buvusių laikotarpių sumą, dabartinio **laikotarpio prognozės praeities sumas nustatykite** kaip **Taip**.
    3. Pasirinktinai: nustatykite pasikartojančią paketinio vykdymo užduotį, kad duomenys būtų periodiškai atnaujinami.
    4. Pasirinkite **Gerai**.

6. Kai paketinė užduotis baigiama vykdyti, eikite į Sistemos **administravimo nustatymo \>\> objektų saugyklą** ir atnaujinkite mažėjančios **vertės ataskaitos sudėti** kartu matą.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio

Abonemento atsiskaitymo Power BI turinys rodomas Abonemento atsiskaitymo **darbo** srityje.
