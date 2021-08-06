---
title: „Finance Insights” pagrindinis puslapis (peržiūra)
description: „Finance Insights” suteikia konfigūruojamus ir išplečiamus modelius, kad galėtumėte tiksliai ir sumaniai prognozuoti savo įmonės grynųjų pinigų srautus, numatyti, kada gausite mokėjimą už neapmokėtas gautinas sumas ir bus sugeneruotas biudžeto pasiūlymas, kuris gali pagreitinti jūsų biudžeto sudarymo procesą. Visos šios funkcijos paremtos išmaniaisiais mašininio mokymo modeliais.
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2086a33285d9a529480c5f34fb048105e65c2046
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638519"
---
# <a name="finance-insights-home-page-preview"></a>„Finance Insights” pagrindinis puslapis (peržiūra)

[!include [banner](../includes/banner.md)]

„Finance Insights” suteikia konfigūruojamus ir išplečiamus modelius, kad galėtumėte tiksliai ir sumaniai prognozuoti savo įmonės grynųjų pinigų srautus, numatyti, kada gausite mokėjimą už neapmokėtas gautinas sumas ir bus sugeneruotas biudžeto pasiūlymas, kuris gali pagreitinti jūsų biudžeto sudarymo procesą. Visos šios funkcijos paremtos išmaniaisiais mašininio mokymo modeliais. Kai šios naujos galimybės sujungiamos su tiekėjo mokėjimų ir surinkimų automatizavimu, jos suteikia galingą ir pažangią finansinę sistemą, kuri valdo sprendimų priėmimo procesą ir padeda imtis veiksmų siekiant veiksmingai reaguoti į dabartinius ir numatomus verslo iššūkius.

> [!NOTE]
> „Finance Insights” peržiūros versiją galima įdiegti Jungtinėse Amerikos Valstijose, Kanadoje, Jungtinėje Karalystėje, Europoje, Azijos Ramiojo vandenyno srityje, Australijoje ir Naujojoje Zelandijoje. „Microsoft“ palaipsniui į palaikomų regionų sąrašą įtraukia daugiau regionų. Kad būtų galima įgalinti „Finance insights” gamybos aplinkose, pirmiausia gamybos aplinkoje turi būti įgalintos [Eksportavimo į „Data Lake”](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) galimybės.

> [!NOTE]
> Šis funkcionalumas siūlomas kaip peržiūros versijos funkcijų rinkinys. Atsižvelgiant, kad tai peržiūros funkcija, neturėtumėte gautais mašininio mokymo modeliais pagrįsti savo verslo sprendimų ar biudžeto pasiūlymų. Jūsų naudojimasis šia funkcija valdomas pagal [Papildomas naudojimo sąlygas](https://go.microsoft.com/fwlink/?linkid=2105274) sąlygas.

## <a name="prerequisites"></a>Būtinieji komponentai

Šiame skyriuje pateikiami „Finance Insights” naudojimo reikalavimai. Jei įmanoma, pateikiamos nuorodos į papildomus informacijos šaltinius.

### <a name="legal-requirements"></a>Teisiniai reikalavimai

Norėdami pateikti paraišką dėl peržiūros versijos programos, užpildykite [„Finance Insights” „Dynamics 365 Finance“ peržiūros sutartį](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Sistemos reikalavimai

Norint peržiūrėti „Finance Insights”, būtina 2 pakopos aplinka (kelių langelių). Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versijos reikalavimai

Šis dokumentas taikomas „Finance and Operations“ 10.0.11 versijos programoms (35 platformos atnaujinimas) ir naujesnėms versijoms.

### <a name="historical-data-requirements"></a>Retrospektyvos duomenų reikalavimai

Reikia bent vienerių metų kliento SF, kad būtų galima tinkamai išmokyti mašininio mokymosi modelį, kurį naudoja kliento mokėjimo prognozių funkcija.

### <a name="role-and-permission-requirements"></a>Vaidmenų ir teisių reikalavimai

Bus atlikti „Microsoft Dynamics 365 Finance“, „Microsoft Dynamics Lifecycle Services“ (LCS) ir „Power Apps“ ir „Azure“ pakeitimai. Šiose aplinkose reikia tinkamų teisių. Toliau nurodoma keletas pakeitimų, kurie bus atlikti, pavyzdžių.

- Bus sukurta nauja aplinka „Microsoft Power Platform“.
- Saugyklos sąskaita, „Key Vault“ ir programa bus sukurtos „Azure“.
- „Active Directory“ nuomotojo administratorius turės autorizuoti „AI Builder“ programą, kad būtų suteikta prieiga prie duomenų telkinio.
- Funkcija bus įjungta „Dynamics 365“.

„Azure“, „Microsoft Dataverse“ ir LCS išteklių kūrimo ir valdymo proceso išmanymas bus naudingas, kai įvykdysite šį procesą.

## <a name="configure-finance-insights"></a>„Finance Insights” konfigūravimas

Turite atlikti keletą konfigūracijos veiksmų, kad galėtumėte naudoti „Finance Insights”. Daugiau informacijos, kaip konfigūruoti šį abonementą, žr. „Finance insights“.
  - Apie versijas iki 10.0.19: [Konfigūravimas „Finance insights“ (peržiūros versija) – versijoms iki 10.0.19](configure-for-fin-insites.md).
  - Versijoms 10.0.20 ir naujesnėms: [Konfigūravimas „Finance Insights“ (peržiūra) - versijoms 10.0.20 ir naujesnėms](configure-for-fin-insites-PubPrvw.md).

## <a name="create-a-data-integrator-project"></a>Duomenų integratoriaus projekto kūrimas

Jums reikės sukurti duomenų integratoriaus projektą, kad būtų galima mašininio mokymo modelio sugeneruotus duomenis siųsti į „Dynamics 365 Finance“. Šio projekto kūrimo veiksmų žr. [Duomenų integratoriaus projekto kūrimas](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>„Finance Insights” galimybių įjungimas

Atlikę konfigūravimo veiksmus ir nustatę demonstracinius duomenis, turite įjungti ir nustatyti kiekvieną pajėgumą, kurį planuojate naudoti: kliento mokėjimo prognozes, pinigų srautų prognozes ir biudžeto pasiūlymus.

### <a name="enable-customer-payment-predictions"></a>Kliento mokėjimo prognozių įjungimas
Jei naudojate demonstracinius duomenis, kad išbandytumėte kliento mokėjimo prognozes, jums gali tekti importuoti papildomus demonstracinius duomenis, kad galėtumėte sėkmingai sukurti savo DI modelį. 

Norėdami įjungti kliento mokėjimo prognozes, turite atlikti konkrečius veiksmus, kad galėtumėte kurti mašininio mokymo modelį, kuris naudoja jūsų organizacijos duomenis generuodamas prognozes apie tai, kada klientai gali apmokėti neapmokėtas SF ir kada gali būti apmokėtos konkrečios SF. Norėdami gauti daugiau informacijos ir sužinoti konkrečius veiksmus, žr. [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimo įjungimas
Norėdami įjungti grynųjų pinigų srauto prognozavimą, turite atlikti konkrečius veiksmus, kad sukurtumėte mašininio mokymo modelį, kuris naudoja jūsų organizacijos duomenis generuodamas grynųjų pinigų srautų prognozes. Norėdami gauti daugiau informacijos ir sužinoti konkrečius veiksmus, žr. [Grynųjų pinigų srauto prognozių įjungimas](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Biudžeto pasiūlymų įjungimas

Biudžeto pasiūlymų funkcija naudoja mašininio mokymo modelį kartu su jūsų organizacijos retrospektyviniais duomenimis, kad sugeneruotų biudžeto pasiūlymą. Sugeneruotas pasiūlymas gali padėti pradėti biudžeto sudarymo procesą – tai yra efektyviau nei neautomatinis procesas. Konkrečių šios funkcijos įjungimo veiksmų žr. [Biudžeto pasiūlymų įjungimas](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>„Finance Insights” funkcijų naudojimas

### <a name="using-customer-payment-predictions"></a>Kliento mokėjimo prognozių naudojimas

Pažangus grynųjų pinigų srauto prognozavimas sukurtas kaip priedas prie esamos grynųjų pinigų srauto prognozavimo funkcijos programoje „Dynamics 365 Finance“. Norėdami peržiūrėti esamą pajėgumą, žr. [Grynųjų pinigų srauto prognozavimas](../cash-bank-management/cash-flow-forecasting.md).

- Norėdami sužinoti, kaip kliento mokėjimo prognozės gali suteikti informacijos, kurios reikia, kad būtų galima aktyviai vykdyti surinkimo veiklą, žr. [Kliento mokėjimo prognozių naudojimas](use-customer-payment-predictions.md).
- Informacijos, kuri gali padėti įvertinti prognozavimo modelio efektyvumą po to, kai pradėjote naudotis šia funkcija, žr. [Pradinio kliento mokėjimo prognozavimo modelio įvertinimas](evaluate-payment-prediction.md).
- Informacijos, kuri gali padėti pakoreguoti duomenis, naudojamus prognozei sukurti, ir taip pagerinti jo efektyvumą, žr. [Prognozavimo modelio patobulinimas](improve-model.md).

Norėdami daugiau sužinoti apie DI prognozavimo modelių rezultatus žr. [Mašininio mokymo modelių rezultatai](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Grynųjų pinigų srautų prognozių naudojimas

Grynųjų pinigų srauto prognozavimo pajėgumas gali padėti tiksliau įvertinti savo grynuosius pinigus. 

- Norėdami sužinoti apie naujas grynųjų pinigų srauto prognozavimo galimybes žr. [Grynųjų pinigų srauto prognozavimas](cash-flow-forecast-intro.md).
- Norėdami informacijos apie išorinių duomenų importavimą, kurie bus įtraukti į grynųjų pinigų srauto prognozę čia, žr. [Išorinių duomenų naudojimas grynųjų pinigų srauto prognozėse](external-data-in-cash-flow.md). 
- Norėdami informacijos apie tai, kaip naudoti AI modelį ilgalaikiam grynųjų pinigų srautui prognozuoti, žr. [Grynųjų pinigų padėtis](cash-position.md).
- Norėdami informacijos apie grynųjų pinigų srauto padėtis ir grynųjų pinigų srauto prognozių kaip momentinių kopijų įrašymą bei norėdami palyginti momentinę kopiją su faktine prognoze žr. [Momentinių kopijų apžvalga](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Biudžeto pasiūlymo naudojimas

Norėdami daugiau informacijos apie tai, kaip pagreitinti biudžeto kūrimą, žr. [Biudžeto pasiūlymai](budget-proposals.md). 

## <a name="feedback-and-support"></a>Atsiliepimai ir palaikymas

Jei norite pateikti atsiliepimų ar reikia pagalbos, atsiųskite el. laišką [kliento mokėjimo įžvalgų (peržiūros versija)](mailto:fiap@microsoft.com) el. pašto adresu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
