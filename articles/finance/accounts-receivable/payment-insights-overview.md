---
title: Kliento mokėjimo įžvalgos (peržiūra)
description: Šiame straipsnyje aprašomos mokėjimo informacijos galimybės, kurios padeda suprasti atskirų klientų įprastas mokėjimo praktikas. Funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę.
author: ShivamPandey-msft
ms.date: 11/06/2019
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
ms.openlocfilehash: 5d2c811ac48a6bf29267192f61a33b6b47721659
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068173"
---
# <a name="customer-payment-insights-preview"></a>Kliento mokėjimo įžvalgos (peržiūra)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje aprašomos mokėjimo informacijos galimybės, kurios padeda suprasti atskirų klientų įprastas mokėjimo praktikas. Funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę. 

## <a name="overview"></a>Peržiūra

Gali būti sudėtinga prognozuoti, kada klientai apmokės sąskaitas faktūras. Dėl šios įžvalgos stokos, prognozuojami mažiau tikslūs grynųjų pinigų srautai, išieškojimo procesai pradedami per vėlai, o užsakymai yra patvirtinami klientams, kurie gali nevykdyti mokėjimo įsipareigojimų. Kliento mokėjimo įžvalgos (peržiūra) padeda organizacijoms nuspėti, kada kliento sąskaita faktūra bus apmokėta. Ši informacija gali padėti organizacijoms sukurti surinkimo strategijas, kurios padidintų tikimybę, kad būtų sumokėta laiku. 

## <a name="predictions"></a>Prognozės

Mokėjimo prognozės suteiks organizacijoms galimybę tobulinti savo verslo procesus padėdamos lengvai identifikuoti sąskaitas faktūras, kurios gali būti apmokėtos pavėluotai, ir imtis priemonių, kurios padidintų tikimybę apmokėjimą gauti laiku.

Naudodamosi mašininio mokymosi modeliu, kuris naudoja istorines sąskaitas-faktūras, mokėjimus ir kliento duomenis, kliento mokėjimo įžvalgos (peržiūra) tiksliau prognozuos, kada klientas apmokės neapmokėtą sąskaitą-faktūrą.

Kiekvienai atvirai sąskaitai faktūrai kliento mokėjimo įžvalgos (peržiūra) gali numatyti tris mokėjimo galimybes.

-   Tikimybė, kad mokėjimas bus atliktas laiku 
-   Tikimybė, kad mokėjimas bus atliktas pavėluotai
-   Tikimybė, kad mokėjimas bus atliktas labai pavėluotai

Kliento mokėjimo įžvalgos (peržiūra) taip pat pateikia bendrą kaupiamąjį numatomo mokėjimo rodinį, kad padėtų organizacijoms suprasti visą mokėjimo sumą, kurią jie gali tikėtis gauti iš kliento vienu iš trijų laikotarpiu – laiku, pavėluotai, labai pavėluotai.

[![Kaupiamasis mokėjimo prognozių rodinys.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Be to, kiekviena sąskaita faktūra yra priskirta tikimybei, kad bus apmokėta laiku. Jei apmokėjimo laiku tikimybė yra mažesnė nei 50 %, sąskaitos faktūros pažymimos raudonu apskritimu, kuris nurodo, kad šias sąskaitas faktūras gali reikėti išieškoti. 

[![Apmokėjimo tikimybių sąrašas.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Kliento apmokėjimo įžvalgos (peržiūra) taip pat pateikia kontekstinę informaciją, siekiant paaiškinti prognozavimą, pavyzdžiui, svarbiausius faktorius, kurie turi įtakos prognozėms, dabartinę verslo padėtį su klientu ir informaciją apie istorinį kliento apmokėjimą elgesį. Daugelyje įmonių išieškojimo procesas buvo reaktyvi veikla; išieškojimas procesas neprasideda iki sąskaitų faktūrų apmokėjimo termino. 

Naudodamos kliento mokėjimo įžvalgas (peržiūra), organizacijos gali aktyviau taikyti išieškojimą. Joms nebereikės laukti, kol operacijos pradės vėluoti, kad galėtų pradėti išieškojimo procesą. Vietoje to, jos gali naudoti mokėjimo prognozės funkciją, kad galėtų nustatyti, ar iniciatyvūs išieškojimai pagerins tikimybę, kad bus sumokėta laiku. Be to, mokėjimo prognozė suteikia įmonėms informacijos, kurios reikia norint pateisinti ankstyvą išieškojimo proceso pradžią.

## <a name="methodology"></a>Metodika

Kurti ir visuotinai diegti AI sprendimus yra sudėtinga. Reikia duomenų mokslininkų, temos ekspertų ir inžinierių komandos, kuri ilgą laiką dirba, kad suformuluotų, sukurtų, visuotinai įdiegtų ir išlaikytų naudotiną DI sprendimą. Mes stengiamės, kad AI sprendimus būtų lengva visuotinai įdiegti ir naudoti „Finance“. Iš anksto supakuojame finansų AI sprendimus, įtaisytus "Microsoft"AI Builder. Galutinis vartotojas vienu mygtuko paspaudimu gali visuotinai įdiegti AI sprendimą ir pradėti naudotis išmaniųjų prognozių privalumais. Jei organizacija nepatenkinta prognozių tikslumu, patyręs vartotojas vienu mygtuko paspaudimu gali įvesti „AI builder“ plėtinio patirtį, tada pasirinkti arba panaikinti laukų, skirtų generuoti prognozes, pasirinkimą. Kai pasiruošta, jie gali išmokyti ir publikuoti keitimus, o naujai išmokytas modelis bus automatiškai pasirenkamas prognozėms „Finance“.

## <a name="how-to-get-customer-payment-insights-preview"></a>Kaip gauti kliento mokėjimo įžvalgas (peržiūra)

Jei susidomėjote galimybe išbandyti kliento mokėjimo įžvalgas (peržiūra), siųskite el. laišką [Kliento mokėjimo įžvalgos (peržiūra)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Privatumo pranešimas

Naudojant peržiūrą (1) gali būti naudojama mažiau privatumo ir saugos priemonių nei "Dynamics 365" finansų ir operacijų tarnyba; (2) neįtrauktos į šios tarnybos lygio sutartį; (3) neturėtų būti naudojama asmeniniams duomenims ar kitiems duomenims, kuriems taikomi teisinių arba reguliavimo atitikties reikalavimai, apdoroti, o (4) yra ribotas jų palaikymas.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]

