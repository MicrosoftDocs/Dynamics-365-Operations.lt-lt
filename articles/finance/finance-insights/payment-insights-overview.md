---
title: Kliento mokėjimo prognozės
description: Šiame straipsnyje aprašomos mokėjimo numatymos, kurios gali padėti geriau suprasti kliento įprastas mokėjimo praktikas. Ši funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5d16b42b4538a18ca3dd9d3bac25ed1af1441ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903166"
---
# <a name="customer-payment-predictions"></a>Kliento mokėjimo prognozės

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos mokėjimo numatymos, kurios gali padėti geriau suprasti kliento įprastas mokėjimo praktikas. Ši funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę.

## <a name="overview"></a>Peržiūra

Organizacijoms dažnai sudėtinga prognozuoti, kada klientai apmokės sąskaitas faktūras. Stingant įžvalgų, gali kilti toliau nurodytos problemos.

- Mažiau tikslios pinigų srautų prognozės
- Per vėlai pradedami surinkimo procesai
- Užsakymai, išleidžiami klientams, kurie gali nesumokėti

Kliento mokėjimų numatymas padeda organizacijoms nuspėti, kada bus apmokėta kliento SF. Todėl jos gali sukurti surinkimo strategijas, padedančias padidinti tikimybę, kad bus apmokama laiku.

## <a name="predictions"></a>Prognozės

Mokėjimo prognozės leidžia organizacijoms tobulinti savo verslo procesus, padėdamos jiems identifikuoti SF, kurios gali būti apmokamos pavėluotai. Organizacija gali naudoti šią informaciją, kad atliktų veiksmus, gerinančius tikimybę, jog joms bus sumokėta laiku.

Kliento mokėjimo prognozių funkcija naudoja mašininio mokymo modelį, kad tiksliau nuspėtų, kada klientas apmokės nepadengtą SF. Šiame mašininio mokymo modelyje yra retrospektyviniai SF, mokėjimo ir kliento duomenys.

Kiekvienai atidarytai SF ši funkcija priskiria tris mokėjimo tikimybes.

- Tikimybė, kad mokėjimai bus atlikti laiku
- Tikimybė, kad mokėjimai bus atlikti pavėluotai
- Tikimybė, kad mokėjimai bus atlikti žymiai pavėluotai

Funkcija taip pat pateikia apibendrintą numatomų mokėjimų rodinį.

[![Kaupiamasis mokėjimo prognozių rodinys.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Kiekviena sąskaita faktūra yra priskirta tikimybei, kad bus sumokėta laiku. Jei SF apmokėjimo laiku tikimybė yra mažesnė nei 50 procentų, SF pažymimos raudonu apskritimu, kuris nurodo, kad gali reikėti perduoti jas mokėjimų priežiūros agentui patikrinti.

[![Apmokėjimo tikimybių sąrašas.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Kliento mokėjimo prognozių funkcija taip pat pateikia kontekstinę informaciją, kuri paaiškina prognozes. Ši informacija apima svarbiausius veiksnius, kurie paveikė prognozes, dabartinę verslo padėtį su klientu ir retrospektyvinę informaciją apie kliento mokėjimo elgseną.

Daugelyje įmonių surinkimo procesas buvo reaktyvi veikla. Kitaip tariant, išieškojimas procesas neprasideda iki sąskaitų faktūrų apmokėjimo termino. Naudodamos kliento mokėjimo prognozes, organizacijos gali aktyviau taikyti išieškojimą. Joms nebereikės laukti, kol operacija pradės vėluoti, kad galėtų pradėti išieškojimo procesą. Vietoje to, jos gali naudoti mokėjimo prognozės funkciją, kad galėtų nustatyti, ar iniciatyvūs išieškojimai pagerins tikimybę, kad bus sumokėta laiku.

## <a name="methodology"></a>Metodika

Anksčiau paprastai būdavo nelengva sukurti ir įdiegti dirbtinio intelekto (DI) sprendimą. Tam reikėdavo komandos, jungiančios duomenų mokslininkus, srities ekspertus ir inžinierius, kurie ilgą laiką dirba, kad suformuluotų, sukurtų, visuotinai įdiegtų ir išlaikytų naudotiną DI sprendimą. Kliento mokėjimų numatymas leidžia lengvai diegti ir naudoti AI sprendimą Microsoft Dynamics 365 finansuose. "Microsoft" iš anksto supakuoja AI sprendimus, įtaisytus "Microsoft"AI Builder. Todėl vartotojai gali naudoti DI sprendimą vienu pelės klavišu, norėdami pasinaudoti pažangių prognozių pranašumais. Jei nesate patenkinti numatymais, maitinimo vartotojas gali (dar kartą spustelėjus pelę) AI Builder įvesti išplėtimo patirtį ir pasirinkti arba išvalyti laukus, kurie naudojami numatymams generuoti. Kai esate pasiruošę, galite „išmokyti“ modelį ir publikuoti keitimus. Naujai suplanuotas modelis bus automatiškai paimtas, kad būtų galima generuoti numatymas "Dynamics 365 Finance".

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
