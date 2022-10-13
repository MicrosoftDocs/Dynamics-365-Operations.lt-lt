---
title: „Finance Insights“ pagrindinis puslapis
description: „Finance Insights” suteikia konfigūruojamus ir išplečiamus modelius, kad galėtumėte tiksliai ir sumaniai prognozuoti savo įmonės grynųjų pinigų srautus, numatyti, kada gausite mokėjimą už neapmokėtas gautinas sumas ir bus sugeneruotas biudžeto pasiūlymas, kuris gali pagreitinti jūsų biudžeto sudarymo procesą. Visos šios funkcijos paremtos išmaniaisiais mašininio mokymo modeliais.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2f04ef1a0de815596f629fede25a247c58e026f4
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643883"
---
# <a name="finance-insights-home-page"></a>„Finance Insights“ pagrindinis puslapis

[!include [banner](../includes/banner.md)]

Finansų įžvalgos pateikia konfigūruojamus ir extensible sprendimus, kurie padės sumai nuspėti savo įmonės pinigų srautą, numatyti, kada galite gauti neapmokėtų gautinų sumų mokėjimą ir generuoti biudžeto pasiūlymą, kuris gali padėti paspartinti biudžeto planavimo procesą. Šios funkcijos naudoja išmaniuosius mašinų mokymosi šablonus, kad galėtų kurti modelius, naudodami jūsų teikianus duomenis (įskaitant trečiosios šalies duomenis, pvz., vartotojo ataskaitų informaciją iš biuro). Šie intelektualūs pajėgumai informuoja apie sprendimų priėmimą ir padeda imtis veiksmų, kad būtų efektyviai reaguojama į dabartinę ir numatomą verslo įmonę. Jūs esate atsakingas už bet kokius duomenis, naudojamus su finansų informacijos duomenimis arba išvestis iš jų.

> [!NOTE]
> Finansų duomenis galima diegti Jungtinėse Amerikos Valstijose, Kanadoje, Jungtinėje Karalystėje, Europoje, Azijos Ramiojo vandenyne, Japonija, Australijoje ir Naujoje Zelandijoje. „Microsoft“ palaipsniui į palaikomų regionų sąrašą įtraukia daugiau regionų.

## <a name="prerequisites"></a>Būtinieji komponentai

Šiame skyriuje pateikiami „Finance Insights” naudojimo reikalavimai. Jei įmanoma, pateikiamos nuorodos į papildomus informacijos šaltinius.

### <a name="system-requirements"></a>Sistemos reikalavimai

Norint peržiūrėti „Finance Insights”, būtina 2 pakopos aplinka (kelių langelių). Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versijos reikalavimai

Šis straipsnis taikomas Microsoft Dynamics 365 10.0.21 ir vėlesnei finansų versijai.

### <a name="license-requirements"></a>Licencijos reikalavimai

Finansų žinių programos naudoja AI Builder kreditus finansiniams numatymams kurti. Visos būtinos šio failo licencijos įtraukiamos į nuomininko licenciją. Kiekvienam "Dynamics 365" finansų nuomininkui kas mėnesį pateikiami 20 000 AI Builder kreditai. Jei verslo poreikiams reikia papildomų kreditų, juos galima įsigyti tiesiogiai iš AI Builder.

### <a name="historical-data-requirements"></a>Retrospektyvos duomenų reikalavimai

Reikia bent vienerių metų kliento SF, kad būtų galima tinkamai išmokyti mašininio mokymosi modelį, kurį naudoja kliento mokėjimo prognozių funkcija. Grynųjų pinigų srautų prognozėms rekomenduojami trijų metų praeities duomenys. Intelektualiems biudžeto pasiūlymams rekomenduojama trijų metų retrospektyvaus biudžeto ir (arba) faktinių duomenų.

## <a name="configure-finance-insights"></a>„Finance Insights“ konfigūravimas

Prieš naudodami finansų žinias, turite atlikti konfigūracijos veiksmus. Daugiau informacijos apie tai, kaip sukonfigūruoti finansines įžvalgas, žr. [„Finance Insights” konfigūravimas](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Duomenų integratoriaus projekto kūrimas

Turite sukurti duomenų integratoriaus projektą, kad duomenys, kuriuos generuoja įrenginio mokymosi modelis, būtų patenka į "Dynamics 365" finansus. Šio projekto kūrimo veiksmų žr. [Duomenų integratoriaus projekto kūrimas](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>„Finance Insights” galimybių įjungimas

Atlikę konfigūravimo veiksmus ir nustatę demonstracinius duomenis, turite įjungti ir nustatyti kiekvieną pajėgumą, kurį planuojate naudoti: kliento mokėjimo prognozes, pinigų srautų prognozes ir biudžeto pasiūlymus.

### <a name="enable-customer-payment-predictions"></a>Kliento mokėjimo prognozių įjungimas
Jei naudojate demonstracinius duomenis, kad išbandytumėte kliento mokėjimo prognozes, jums gali tekti importuoti papildomus demonstracinius duomenis, kad galėtumėte sėkmingai sukurti savo DI modelį. 

Norėdami įgalinti kliento mokėjimų numatymą, turite atlikti veiksmų rinkinį, kad būtų sukurtas įrenginio mokymosi modelis, naudojantis jūsų organizacijos duomenis numatymams generuoti, kada klientai nori sumokėti neapmokėtas SF ir kai tikėtina, kad tam tikros SF bus apmokėtos. Norėdami gauti daugiau informacijos ir sužinoti konkrečius veiksmus, žr. [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimo įjungimas
Norėdami įjungti grynųjų pinigų srauto prognozavimą, turite atlikti konkrečius veiksmus, kad sukurtumėte mašininio mokymo modelį, kuris naudoja jūsų organizacijos duomenis generuodamas grynųjų pinigų srautų prognozes. Norėdami gauti daugiau informacijos ir sužinoti konkrečius veiksmus, žr. [Grynųjų pinigų srauto prognozių įjungimas](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Biudžeto pasiūlymų įjungimas

Biudžeto pasiūlymų funkcija naudoja mašininio mokymo modelį kartu su jūsų organizacijos retrospektyviniais duomenimis, kad sugeneruotų biudžeto pasiūlymą. Sugeneruotas pasiūlymas gali padėti pradėti biudžeto sudarymo procesą – tai yra efektyviau nei neautomatinis procesas. Norėdami nustatyti konkrečius šios priemonės įgalinamus veiksmus, žr. [Įjungti biudžeto pasiūlymus](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>„Finance Insights” funkcijų naudojimas

### <a name="using-customer-payment-predictions"></a>Kliento mokėjimo prognozių naudojimas

- Norėdami sužinoti, kaip kliento mokėjimo numatymas gali pateikti informaciją, kurios reikia norint aktyviai pradėti surinkimo veiklą, [žr. Kliento mokėjimo numatymą](use-customer-payment-predictions.md).
- Informacijos, kuri gali padėti įvertinti prognozavimo modelio efektyvumą po to, kai pradėjote naudotis šia funkcija, žr. [Pradinio kliento mokėjimo prognozavimo modelio įvertinimas](evaluate-payment-prediction.md).
- Informacijos, kuri gali padėti pakoreguoti duomenis, naudojamus prognozei sukurti, ir taip pagerinti jo efektyvumą, žr. [Prognozavimo modelio patobulinimas](improve-model.md).
- Norėdami daugiau sužinoti apie DI prognozavimo modelių rezultatus žr. [Mašininio mokymo modelių rezultatai](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Grynųjų pinigų srautų prognozių naudojimas

Grynųjų pinigų srauto prognozavimo pajėgumas gali padėti tiksliau įvertinti savo grynuosius pinigus. Pažangus pinigų srautų prognozavimas kuriamas remiantis esama pinigų srautų prognozavimo funkcija programoje "Dynamics 365 Finance". Norėdami peržiūrėti esamą pajėgumą, žr. [Grynųjų pinigų srauto prognozavimas](../cash-bank-management/cash-flow-forecasting.md).

- Norėdami sužinoti apie naujas pinigų srautų prognozių galimybes, žiūrėkite pinigų [srautų prognozę](cash-flow-forecast-intro.md).
- Norėdami informacijos apie išorinių duomenų importavimą, kurie bus įtraukti į grynųjų pinigų srauto prognozę čia, žr. [Išorinių duomenų naudojimas grynųjų pinigų srauto prognozėse](external-data-in-cash-flow.md). 
- Norėdami informacijos apie tai, kaip naudoti AI modelį ilgalaikiam grynųjų pinigų srautui prognozuoti, žr. [Grynųjų pinigų padėtis](cash-position.md).
- Norėdami informacijos apie grynųjų pinigų srauto padėtis ir grynųjų pinigų srauto prognozių kaip momentinių kopijų įrašymą bei norėdami palyginti momentinę kopiją su faktine prognoze žr. [Momentinių kopijų apžvalga](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Biudžeto pasiūlymo naudojimas

Norėdami daugiau informacijos apie tai, kaip pagreitinti biudžeto kūrimą, žr. [Biudžeto pasiūlymai](budget-proposals.md). 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
