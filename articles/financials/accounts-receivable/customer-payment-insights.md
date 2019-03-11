---
title: Kliento mokėjimo įžvalgos (peržiūra)
description: Šioje temoje aprašoma, kaip kliento mokėjimo įžvalgos gali padėti prognozuoti, kada bus apmokėta sąskaita faktūra, ir organizacijoms padėti kurti optimizacijos strategijas, kurios padidintų apmokėjimo laiku tikimybę.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "344667"
---
# <a name="customer-payment-insights-preview"></a>Kliento mokėjimo įžvalgos (peržiūra)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Ši funkcija yra tikslinio leidimo dalis ir ja gali naudotis tik vartotojai, sutikę su privačiąja peržiūra. Ši funkcija bus įtraukta į būsimą bendrai prieinamą leidimą.

# <a name="overview"></a>Apžvalga

Organizacijoms dažnai sudėtinga prognozuoti, kada klientas apmokės sąskaitas faktūras. Kai neįmanoma to nuspėti, gali kilti šie padariniai – netikslios pinigų srautų prognozės, neefektyvūs surinkimo procesai, tikimybė pateikti užsakymus klientams, kurie kelia didelę kredito riziką. Kliento mokėjimo įžvalgos (peržiūra) naudoja mašininį mokymąsi, kad nuspėtų, kada bus apmokėta sąskaita faktūra. Be to, ji pateikia optimizavimo strategiją, kuri gali būti pritaikyta tam, kad būtų maksimaliai padidinta klientų apmokėjimo laiku tikimybė.

## <a name="predictions"></a>Prognozės

Mokėjimo prognozės leidžia organizacijoms pagerinti verslo procesus šiais būdais:

-   Nesunkiai nustatant sąskaitas faktūras, kurios, remiantis prognozėmis, bus apmokėtos pavėluotai.
-   Imkitės reikiamų priemonių, kad padidintumėte sąskaitos apmokėjimo laiku šansus.

Kliento mokėjimo įžvalgos (peržiūra) naudoja mašininį mokymąsi, kad nuspėtų, kada bus apmokėta sąskaita faktūra. Ji naudoja retrospektyvinius sąskaitų faktūrų, mokėjimų ir klientų duomenis, kad sukurtų mašininio mokymosi modelį, kuris naudojamas nuspėti, kada sąskaita faktūra bus apmokėta.

Kliento mokėjimo įžvalgos (peržiūra) numato tris kiekvienos neapmokėtos sąskaitos faktūros apmokėjimo galimybes:

-  Galimybę, kad mokėjimas bus atliktas laiku (neviršijus sąskaitos faktūros apmokėjimo termino).
-  Galimybę, kad mokėjimas bus atliktas per 30 dienų nuo sąskaitos faktūros apmokėjimo termino.
-  Galimybę, kad mokėjimas bus atliktas vėliau nei per 30 dienų nuo sąskaitos faktūros apmokėjimo termino.

Mokėjimų galimybę galima peržiūrėti prognozių srityje.

[![Mokėjimų prognozės](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Kiekvienai sąskaitai faktūrai taip pat priskiriama tikimybė, kad mokėjimas bus įvykdytas, naudojant vieną iš anksčiau pateiktų trijų prognozuojamų mokėjimo scenarijų. Scenarijus, kurio mokėjimo tikimybė yra didžiausia, yra labiausiai tikėtinas scenarijus.


Pavyzdžiui, tarkime, kad sąskaitai faktūrai prognozuojama 71 procentų tikimybė, jog ji bus apmokėta laiku, 13 procentų – jog ji bus apmokėta per 30 dienų nuo apmokėjimo termino ir 16 procentų – jog ji bus apmokėta per vėliau nei 30 dienų nuo apmokėjimo termino. Remiantis didžiausia tikimybė – kad sąskaita faktūra bus apmokėta laiku, todėl sąskaita faktūra bus pažymėta tikimybe, jog ji bus apmokėta laiku.

[![Mokėjimų prognozės](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimizavimo strategijos

Neskaitant mokėjimo prognozių, kliento mokėjimo įžvalgos (peržiūra) gali naudoti optimizavimo strategijas, kad pagerintų apmokėjimo laiku šansus. Dėl to organizacijos gali atlikti galimų situacijų analizes, leisdamos vartotojams pakoreguoti sąskaitų faktūrų ir klientų parametrus ir tada palyginti atitinkamą poveikį sąskaitų faktūrų apmokėjimui laiku.

Pavyzdžiui, organizacija gali norėti įvertinti sąskaitų faktūrų mokėjimo nuolaidos poveikį mokėjimo laiku tikimybei. Kai sąskaitos faktūros yra optimizuotos naudoti naują nuolaidą, vartotojai gali patikrinti nuolaidos taikymo poveikį sąskaitų faktūrų apmokėjimo laiku tikimybei. Jei nuolaidos taikymo kaina yra minimali, lyginant ją su nauda, kai mokėjimai bus surinkti laiku, organizacija gali pasirinkti ateityje taikyti pasirinktą nuolaidą visiems atviriems užsakymams.

> [!NOTE] 
> Šiuo metu kliento mokėjimo įžvalgose (peržiūra) kaip optimizavimo strategija galima tik nuolaida.

[![Optimizuotos prognozės](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Kliento mokėjimo įžvalgų (peržiūra) gavimas

Jei susidomėjote galimybe išbandyti kliento mokėjimo įžvalgas (peržiūra), rašykite [Finansinių įžvalgų peržiūros komandai](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Privatumo patvirtinimas

Peržiūros saugo klientų duomenis JAV. Be to, peržiūros (1) gali naudoti mažiau privatumo ir saugos priemonių nei „Dynamics 365 for Finance and Operations“ paslauga, (2) jos nėra įtrauktos į susitarimą dėl šios paslaugos lygio, (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.
