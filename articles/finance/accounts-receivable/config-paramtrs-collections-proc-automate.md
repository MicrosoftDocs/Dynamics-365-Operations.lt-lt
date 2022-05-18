---
title: Mokėjimo proceso automatizavimo parametrų konfigūravimas
description: Šioje temoje aprašomi parametrai, paveikiantys automatizuotus mokėjimų procesus, ir pateikia gaires, kaip juos nustatyti, kad automatizuotas procesas atspindėtų jūsų tikslus.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e7a7e048a371fc90456368206b91c29c4b1264d5
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734402"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Mokėjimo proceso automatizavimo parametrų konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi parametrai, paveikiantys automatizuotus mokėjimų procesus, ir pateikia gaires, kaip juos nustatyti, kad automatizuotas procesas atspindėtų jūsų tikslus. Daugiau informacijos apie tai, kaip automatizuoti mokėjimų priežiūros procesus, rasite [Mokėjimų priežiūros procesų automatizavime](collections-process-automate.md).

## <a name="general"></a>Bendroji
Įveskite numerį į **Klientų procentinė dalis paketinei užduočiai**, jei norite nustatyti paketinių užduočių numerį vienam automatizavimo procesui. Nustatykite **Registruoti mokėjimų priežiūros laiškus automatiškai** į **Taip**, kad mokesčių priežiūros laiško veiksmo tipas registruotų laišką automatizavimo metu. Nustatykite **Kurti automatizavimų veiklas** į **Taip**, jog sukurtumėte ir uždarytumėte ne veiklos veiksmo tipų veiklas, skirtas visų paskyroje atliktų automatizuotų veiksmų peržiūrai. Nurodykite, kiek dienų bus saugoma mokesčių priežiūros retrospektyva **Dienos, kiek bus saugoma mokėjimų priežiūros proceso automatizavimo retrospektyva**. Kai SF pasiekia paskutinį mokėjimų priežiūros proceso veiksmą, ji nebus naudojama būsimiems procesų automatizavimo veiksmų tipams kurti, jei **Neįtraukti SF aktyvavus paskutinį proceso veiksmą** nustatyta į **Taip**. Kita seniausia SF nustato tolesnį proceso automatizavimo veiksmą, kad būtų užtikrinti tolesni mokėjimų priežiūros proceso automatizavimo veiksmai. 

## <a name="payment-predictions"></a>Mokėjimų prognozės
Pradedant nuo 10.0.21 versijos, „Finance insights” klientų mokėjimo prognozės numato, ar SF bus apmokėta laiku, vėlai ar labai vėlai. Galite konfigūruoti kiekvieną iš šių kategorijų „Finance insights”. Jei numatoma, kad bus vėluojama apmokėti SF, svarbu pradėti mokėjimų priežiūros procesą prieš SF apmokėjimo terminą. Šios prognozės gali būti naudojamos mokėjimų priežiūros veikloms kurti, kai vykdomi mokėjimų priežiūros proceso automatizavimai. Nustatykite **Įgalinti mokėjimų prognozes** į **Taip**, jei norite naudoti kliento mokėjimų prognozes, kad kurtumėte mokėjimų priežiūros veiklas, remiantis tikimybe, jog SF bus apmokėta pavėluotai. 

Daugiau informacijos apie kliento mokėjimų prognozes ir „Finance insights” rasite [Kliento mokėjimų prognozės](payment-insights-overview.md).

Kai vykdomas kliento mokėjimo prognozės modelis, jis priskiria procentą prognozei, jog SF bus apmokėta laiku, vėlai arba labai vėlai. Galite naudoti šią informaciją automatiškai pradėti mokėjimų priežiūros veiklas naudodami mokėjimų priežiūros proceso automatizavimą tikėtinais vėluojančio mokėjimo atvejais. Šiuos procentinius dydžius galite peržiūrėti **Kliento mokėjimo prognozes** arba **Operacijos mokėjimo prognozės** puslapiuose, esančiuose po **Kreditas ir mokėjimų priežiūra > Mokėjimų priežiūra**. 

Jei kliento SF vidutinio mokėjimo prognozė yra mažesnė nei sąlyginio etalono procentas, nesukuriama jokia veikla. Jei SF prognozė yra didesnė arba lygi sąlyginio etalono procentui, klientui sukuriama viena veikla. Laukui **Prognozė: Vėluoja** įveskite **Sąlyginio etalono procentą** nuo tada, kai mokėjimų priežiūros proceso automatizavimas turėtų sukurti mokėjimų priežiūros veiklas. Tai yra pavėluoto ir labai pavėluoto sukaupta reikšmė. Pasirinkite **Verslo dokumento šabloną**, kurį naudosite sukurtai veiklai arba naujos veiklos sukūrimui. Tai identifikuoja **Tipą**, **Tikslą** ir **Dienas iki veiklos uždarymo**. Įvesti bet kokias **Pastabas**, kurios bus numatytos kaip aprašymas sukūrus veiklą. Laukui **Prognozė: Labai vėluoja** įveskite **Sąlyginio etalono procentą** nuo tada, kai mokėjimų priežiūros proceso automatizavimas turėtų sukurti mokėjimų priežiūros veiklas klientui, kuris, prognozuojama, sumokės SF labai vėlai. Pasirinkite **Verslo dokumento šabloną**, kurį naudosite sukurtai veiklai. Tai identifikuoja **Tipą**, **Tikslą** ir **Dienas iki veiklos uždarymo**. Įvesti bet kokias **Pastabas**, kurios bus numatytos kaip aprašymas sukūrus veiklą. 

### <a name="example"></a>Pavyzdys
Jei pavėluoto sąlyginio etalono procentinė dalis yra nustatyta į 60%. Kai vykdomos kliento mokėjimo prognozės kiekvienai sąskaitai, sistema priskiria procentą prognozei bus apmokėta laiku, vėlai arba labai vėlai. Jei mokėjimo prognozė, kad SF bus apmokėta vėlai yra 59% arba mažesnė, automatizuotas mokėjimų priežiūros procesas nekurs mokėjimų priežiūros veiklos. Jei kliento SF apmokėjimo prognozė yra didesnė arba lygi 60%, mokėjimų priežiūros veikla sukuriama mokėjimų priežiūros proceso automatizavimo metu. 

> [!NOTE]
> Labai vėluojančio mokėjimo prognozė yra įvertinama prieš labai vėluojančio mokėjimo prognozę, nes labai vėluojantis mokėjimas apima SF, kurios, prognozuojama, bus apmokėtos pavėluotai. Mokėjimų priežiūros procesas generuoja tik vieną veiklą, jei SF patenka tiek į vėluojančio, tiek į labai vėluojančio mokėjimosąlyginį etaloną. Tokiu atveju sistema naudoja labai vėluojančią veiklą ir verslo dokumentą, nes labai vėluojantis mokėjimo prioritetas yra didesnis. Visi kiti jau sugeneruoti veiksmai nebus generuojami antrą kartą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
