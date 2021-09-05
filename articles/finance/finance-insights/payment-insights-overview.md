---
title: Kliento mokėjimo prognozės
description: Šioje temoje aprašomas mokėjimo prognozavimo pajėgumas, kuris gali padėti geriau suprasti įprastas klientų atsiskaitymo praktikas. Ši funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 21a773b37020aeff969469e29be68e7f7ef44d93
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386666"
---
# <a name="customer-payment-predictions"></a>Kliento mokėjimo prognozės

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas mokėjimo prognozavimo pajėgumas, kuris gali padėti geriau suprasti įprastas klientų atsiskaitymo praktikas. Ši funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę.

## <a name="overview"></a>Peržiūra

Organizacijoms dažnai sudėtinga prognozuoti, kada klientai apmokės sąskaitas faktūras. Stingant įžvalgų, gali kilti toliau nurodytos problemos.

- Mažiau tikslios pinigų srautų prognozės
- Per vėlai pradedami surinkimo procesai
- Užsakymai, išleidžiami klientams, kurie gali nesumokėti

Kliento mokėjimo prognozės (peržiūra) padeda organizacijoms nuspėti, kada kliento sąskaita faktūra bus apmokėta. Todėl jos gali sukurti surinkimo strategijas, padedančias padidinti tikimybę, kad bus apmokama laiku.

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

Anksčiau paprastai būdavo nelengva sukurti ir įdiegti dirbtinio intelekto (DI) sprendimą. Tam reikėdavo komandos, jungiančios duomenų mokslininkus, srities ekspertus ir inžinierius, kurie ilgą laiką dirba, kad suformuluotų, sukurtų, visuotinai įdiegtų ir išlaikytų naudotiną DI sprendimą. Kliento mokėjimo prognozės leidžia lengvai įdiegti ir naudoti DI sprendimą programoje „Microsoft Dynamics 365 Finance“. „Microsoft“ iš anksto supakuoja DI sprendimus, kurie yra įdiegti ant „Microsoft AI Builder“. Todėl vartotojai gali naudoti DI sprendimą vienu pelės klavišu, norėdami pasinaudoti pažangių prognozių pranašumais. Jei netenkinta prognozių tikslumas, patyręs vartotojas vienu mygtuko spustelėjimu gali atidaryti „AI Builder“ plėtinio sąsają, tada pasirinkti arba panaikinti laukų, skirtų generuoti prognozes, pasirinkimą. Kai esate pasiruošę, galite „išmokyti“ modelį ir publikuoti keitimus. Naujai parengtas modelis bus automatiškai naudojamas prognozuojant programoje „Dynamics 365 Finance“.

## <a name="release-details"></a>Išleidimo informacija

Bandomąją „Finance Insights” viešosios peržiūros versiją galima įdiegti Jungtinėse Amerikos Valstijose, Europoje ir Jungtinėje Karalystėje. „Microsoft“ palaipsniui į palaikomų regionų sąrašą įtraukia daugiau regionų.

Viešosios peržiūros versijos funkcijos turi būti įjungtos tik 2 pakopos smėlio dėžės aplinkose. Sąrankos ir DI modelių, sukurtų smėlio dėžės aplinkoje, negalima perkelti į gamybos aplinką. Norėdami gauti daugiau informacijos, žr. [„Microsoft Dynamics 365“ peržiūros versijų papildomos naudojimo sąlygos](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
