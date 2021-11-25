---
title: „Finance Insights“ pagrindinis puslapis
description: „Finance Insights” suteikia konfigūruojamus ir išplečiamus modelius, kad galėtumėte tiksliai ir sumaniai prognozuoti savo įmonės grynųjų pinigų srautus, numatyti, kada gausite mokėjimą už neapmokėtas gautinas sumas ir bus sugeneruotas biudžeto pasiūlymas, kuris gali pagreitinti jūsų biudžeto sudarymo procesą. Visos šios funkcijos paremtos išmaniaisiais mašininio mokymo modeliais.
author: ShivamPandey-msft
ms.date: 11/15/2021
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dfc4d9cb5be4d8d287122fd33bf09b0570498169
ms.sourcegitcommit: a46f0bf9f58f559bbb2fa3d713ad86875770ed59
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2021
ms.locfileid: "7813752"
---
# <a name="finance-insights-home-page"></a>„Finance Insights“ pagrindinis puslapis

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finansinės įžvalgos pateikia konfigūruojamus ir išplečiamus sprendimus, kurie padės protingai prognozuoti įmonės pinigų srautus, numatyti, kada galite gauti mokėjimą už nesumokėtas gautinas sumas, ir sugeneruoti biudžeto pasiūlymą, kuris gali padėti pagreitinti biudžeto sudarymo procesą. Šios funkcijos naudoja pažangius mašininio mokymosi šablonus modeliams kurti naudojant jūsų pateikiami duomenis (įskaitant trečiosios šalies duomenis, pvz., biuro vartotojų ataskaitos informaciją). Šios pažangios galimybės padeda priimti sprendimus ir padeda veiksmingai reaguoti į dabartinius ir numatomus verslo iššūkius. Esate atsakingi už visus duomenis, naudojamus su "Finance" įžvalgomis arba jų išvedimas.

> [!NOTE]
> Finansų įžvalgų peržiūrą galima diegti Jungtinėse Amerikos Valstijose, Kanadoje, Jungtinėje Karalystėje, Europoje, Azijos ir Ramiojo vandenyno regione, Japonijoje, Australijoje ir Naujojoje Zelandijoje. „Microsoft“ palaipsniui į palaikomų regionų sąrašą įtraukia daugiau regionų.

## <a name="prerequisites"></a>Būtinieji komponentai

Šiame skyriuje pateikiami „Finance Insights” naudojimo reikalavimai. Jei įmanoma, pateikiamos nuorodos į papildomus informacijos šaltinius.

### <a name="legal-requirements"></a>Teisiniai reikalavimai

Norėdami pateikti paraišką dėl peržiūros versijos programos, užpildykite [„Finance Insights” „Dynamics 365 Finance“ peržiūros sutartį](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Sistemos reikalavimai

Norint peržiūrėti „Finance Insights”, būtina 2 pakopos aplinka (kelių langelių). Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versijos reikalavimai

Ši tema taikoma "Microsoft" Dynamics 365 Finance 10.0.21 ir vėlesnes versijai.

### <a name="historical-data-requirements"></a>Retrospektyvos duomenų reikalavimai

Reikia bent vienerių metų kliento SF, kad būtų galima tinkamai išmokyti mašininio mokymosi modelį, kurį naudoja kliento mokėjimo prognozių funkcija. Pinigų srautų prognozėms rekomenduojami trejų metų istoriniai duomenys. Išmaniems biudžeto pasiūlymams rekomenduojami treji metai istorinio biudžeto ir (arba) faktinių faktų.

## <a name="configure-finance-insights"></a>„Finance Insights“ konfigūravimas

Prieš naudodami "Finance insights", turite atlikti konfigūravimo veiksmus. Daugiau informacijos apie tai, kaip sukonfigūruoti finansines įžvalgas, žr. [„Finance Insights” konfigūravimas](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Duomenų integratoriaus projekto kūrimas

Jums reikės sukurti duomenų integratoriaus projektą, kad būtų galima mašininio mokymo modelio sugeneruotus duomenis siųsti į „Dynamics 365 Finance“. Šio projekto kūrimo veiksmų žr. [Duomenų integratoriaus projekto kūrimas](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>„Finance Insights” galimybių įjungimas

Atlikę konfigūravimo veiksmus ir nustatę demonstracinius duomenis, turite įjungti ir nustatyti kiekvieną pajėgumą, kurį planuojate naudoti: kliento mokėjimo prognozes, pinigų srautų prognozes ir biudžeto pasiūlymus.

### <a name="enable-customer-payment-predictions"></a>Kliento mokėjimo prognozių įjungimas
Jei naudojate demonstracinius duomenis, kad išbandytumėte kliento mokėjimo prognozes, jums gali tekti importuoti papildomus demonstracinius duomenis, kad galėtumėte sėkmingai sukurti savo DI modelį. 

Norėdami įgalinti kliento mokėjimo prognozes, turite atlikti veiksmų rinkinį, kad sukurtumėte mašininio mokymosi modelį, kuris naudoja jūsų organizacijos duomenis, kad sugeneruotų prognozes apie tai, kada klientai gali apmokėti neapmokėtas sąskaitas faktūras ir kada gali būti apmokėtos konkrečios sąskaitos faktūros. Norėdami gauti daugiau informacijos ir sužinoti konkrečius veiksmus, žr. [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimo įjungimas
Norėdami įjungti grynųjų pinigų srauto prognozavimą, turite atlikti konkrečius veiksmus, kad sukurtumėte mašininio mokymo modelį, kuris naudoja jūsų organizacijos duomenis generuodamas grynųjų pinigų srautų prognozes. Norėdami gauti daugiau informacijos ir sužinoti konkrečius veiksmus, žr. [Grynųjų pinigų srauto prognozių įjungimas](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Biudžeto pasiūlymų įjungimas

Biudžeto pasiūlymų funkcija naudoja mašininio mokymo modelį kartu su jūsų organizacijos retrospektyviniais duomenimis, kad sugeneruotų biudžeto pasiūlymą. Sugeneruotas pasiūlymas gali padėti pradėti biudžeto sudarymo procesą – tai yra efektyviau nei neautomatinis procesas. Konkrečių šios funkcijos įjungimo veiksmų žr. [Biudžeto pasiūlymų įjungimas](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>„Finance Insights” funkcijų naudojimas

### <a name="using-customer-payment-predictions"></a>Kliento mokėjimo prognozių naudojimas

- Norėdami sužinoti, kaip kliento mokėjimo prognozės gali pateikti informaciją, reikalingą aktyviai pradėti surinkimo veiklą, [žr](use-customer-payment-predictions.md).
- Informacijos, kuri gali padėti įvertinti prognozavimo modelio efektyvumą po to, kai pradėjote naudotis šia funkcija, žr. [Pradinio kliento mokėjimo prognozavimo modelio įvertinimas](evaluate-payment-prediction.md).
- Informacijos, kuri gali padėti pakoreguoti duomenis, naudojamus prognozei sukurti, ir taip pagerinti jo efektyvumą, žr. [Prognozavimo modelio patobulinimas](improve-model.md).
- Norėdami daugiau sužinoti apie DI prognozavimo modelių rezultatus žr. [Mašininio mokymo modelių rezultatai](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Grynųjų pinigų srautų prognozių naudojimas

Grynųjų pinigų srauto prognozavimo pajėgumas gali padėti tiksliau įvertinti savo grynuosius pinigus. Išmanusis pinigų srautų prognozavimas grindžiamas esama pinigų srautų prognozavimo funkcija Dynamics 365 Finance. Norėdami peržiūrėti esamą pajėgumą, žr. [Grynųjų pinigų srauto prognozavimas](../cash-bank-management/cash-flow-forecasting.md).

- Norėdami sužinoti apie naujas grynųjų pinigų srauto prognozavimo galimybes žr. [Grynųjų pinigų srauto prognozavimas](cash-flow-forecast-intro.md).
- Norėdami informacijos apie išorinių duomenų importavimą, kurie bus įtraukti į grynųjų pinigų srauto prognozę čia, žr. [Išorinių duomenų naudojimas grynųjų pinigų srauto prognozėse](external-data-in-cash-flow.md). 
- Norėdami informacijos apie tai, kaip naudoti AI modelį ilgalaikiam grynųjų pinigų srautui prognozuoti, žr. [Grynųjų pinigų padėtis](cash-position.md).
- Norėdami informacijos apie grynųjų pinigų srauto padėtis ir grynųjų pinigų srauto prognozių kaip momentinių kopijų įrašymą bei norėdami palyginti momentinę kopiją su faktine prognoze žr. [Momentinių kopijų apžvalga](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Biudžeto pasiūlymo naudojimas

Norėdami daugiau informacijos apie tai, kaip pagreitinti biudžeto kūrimą, žr. [Biudžeto pasiūlymai](budget-proposals.md). 

## <a name="feedback-and-support"></a>Atsiliepimai ir palaikymas

Jei jus domina atsiliepimų teikimas arba jei jums reikia palaikymo, siųskite el. laiškus ["Finance" įžvalgoms](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
