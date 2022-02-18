---
title: „Finance insights“ apie nustatymą trikčių šalinimas
description: Šioje temoje išvardijamos problemos, kurios gali įvykti, kai naudojate „Finance insights“ galimybes. Taip pat paaiškinama, kaip išspręsti šias problemas.
author: panolte
ms.date: 01/29/2022
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
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: f77cddfdab22bef8af7f62d49723e330c4f13261
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064871"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>„Finance insights“ apie nustatymą trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šioje temoje išvardijamos problemos, kurios gali įvykti, kai naudojate „Finance insights“ galimybes. Taip pat paaiškinama, kaip išspręsti šias problemas.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Požymis: kodėl negalima susieti kliento mokėjimo žinių apie duomenų integravimo šablono paskirties stulpelį?

### <a name="resolution"></a>Sprendimas

Galbūt naudojate ankstesnės versijos šabloną. Prieš išleisdami 10.0.17 versiją peržiūrėkite klientus, sukonfigūravo **kliento mokėjimo žinių rezultatus (CDS į Fin ir Ops)** duomenų integravimo (DI) šabloną naudodami **mokėjimo numatymo rezultato (peržiūros)** objektą. Atnaujinę į 10.0.17 ar vėlesnę versiją, norėdami baigti susiejimą, turite naudoti **kliento mokėjimo žinių rezultatus (CDS į Fin ur Ops 10.0.17 ir vėlesnės)** DI versijos. Gali būti, kad negalėsite susieti DI šablono paskirties stulpelio, kol nebus atnaujintas duomenų valdymo objektų sąrašas ir jame atsiras **mokėjimo numatymo rezultato** objektas. Norėdami atnaujinti objektų sąrašą ir rodyti mokėjimo numatymo rezultatą, atlikite veiksmus ir „Microsoft Dynamics 365 Finance“ ir „Dataverse“ (anksčiau žinoma kaip „Common Data Service“ \[CDS\] administravimo portale).

### <a name="in-finance"></a>„Finance“

Atnaujinę atlikite šiuos veiksmus „Finance“ skyriuje.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Duomenų valdymas**.
2. **Duomenų valdymas** darbo srityje pasirinkite **Darbotvarkės parametrai** plytelę.
3. Darbo srityje **Duomenų importavimas/eksportavimo darbotvarkės parametrai** puslapyje rinkitės **Objekto nustatymas** ir tada rinkitės **Naujinti objekto sąrašą**.
4. Uždarykite **duomenų importavimo / eksportavimo sistemos parametrų** puslapį.
5. **Duomenų valdymas** darbo srityje pasirinkite **Duomenų objektai** plytelę.
6. Ieškoti „mokėjimo numatymo rezultato.“ Patikrinkite, ar **mokėjimo numatymo rezultato** objektas nėra peržiūros versija. Peržiūros versijos pavadinimas baigiasi „(peržiūra)." Jei matote tik objekto peržiūros versiją, susisiekite su „Microsoft" palaikymo tarnyba.

### <a name="in-dataverse"></a>„Dataverse“

Norėdami atnaujinti savo duomenų integravimo [„Power Platform“ projektus atlikite](https://admin.powerplatform.microsoft.com/environments) šiuos administratoriaus centro veiksmus.

1. Jei naudojate „Finance insights“ peržiūros versiją, pašalinkite DI projektą, kuris susijęs su **kliento mokėjimo žinių rezultatų (CDS į Fin irOps)** šablonu.
2. Atlikite duomenų [integratoriaus projekto kūrimo veiksmus](create-data-integrate-project.md). Naudokite **kliento mokėjimų žinių rezultatų (CDS į Fin ir Ops 10.0.17 ir vėlesnės versijos)** šabloną.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Požymis: kai bandau atidaryti AI Builder Kodėl naudodamas nuorodas Kliento mokėjimo numatymo sąrankos puslapyje gaunu tokį klaidos pranešimą: „Atsiprašome, įvyko atjungimas“?

### <a name="resolution"></a>Paaiškinimas

Dynamics 365 Finance vartotojai turi turėti a Microsoft Power Apps aplinkos vartotojo abonementą, o ta vartotojo paskyra turi turėti sistemos tinkinimo funkciją. The Microsoft Power Apps sistemos administratorius gali sukurti vartotojo abonementą ir priskirti vaidmenį. Tada galite eiti į<https://make.preview.powerapps.com/>, prisijunkite naudodami tą vartotojo paskyrą ir dar kartą bandykite nuorodas.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Požymis: kodėl pinigų srautų prognozės darbo srityje nėra pinigų prognozės skirtuko, kuriame rodomi kokie nors duomenys?

### <a name="resolution"></a>Sprendimas

Pinigų srautų prognozės funkcija grynųjų pinigų ir banko valdymo srityje ir pinigų srautų prognozių funkcija turi būti nustatyta ir įgalinta „Finance insights“ srityje, kad duomenys būtų tinkamai rodomi pinigų **srautų prognozės** darbo srityje.

Pirmiausia nustatykite ir įgalinkite pinigų srautų prognozavimo ir likvidumo sąskaitas. Daugiau informacijos žr. [Pinigų srauto planavimas](../cash-bank-management/cash-flow-forecasting.md). Jei šis nustatymas baigtas, bet nematote jokių rezultatų, kuriuos tikitės, daugiau informacijos žr. pinigų srautų [prognozės nustatymo trikčių](../cash-bank-management/cash-flow-forecasting-tsg.md) šalinimas.

Po to patvirtinkite, kad pinigų srautų prognozių funkcija finansų žinių srityje (**grynųjų pinigų ir banko valdymas \> Nustatymai \> Finance Insights \> Pinigų srauto prognozės**) yra įgalintos ir kad AI modelio mokymas baigtas. Jei mokymas baigtas, norėdami pradėti mokymo proceso modelį, pasirinkite **Prognozė dabar**.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Požymis: kodėl nerodomas mygtukas Įdiegti naują priedą Microsoft Dynamics Gyvenimo ciklo paslaugos?

### <a name="resolution"></a>Paaiškinimas

Pirmiausia patikrinkite, ar **Aplinkos vadybininkas** arba **Projekto savininkas** vaidmuo priskiriamas prisijungusiam vartotojui **Projekto saugumo vaidmuo** lauke Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Norint įdiegti naujus priedus, reikalingas vienas iš šių projekto saugos vaidmenų.

Jei jums priskirtas tinkamas projekto saugos vaidmuo, gali tekti atnaujinti naršyklės langą, kad pamatytumėte **Įdiekite naują priedą** mygtuką.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Požymis: neatrodo, kad įdiegiamas „Finance Insights“ papildinys. Kodėl taip?

### <a name="resolution"></a>Paaiškinimas

Turėjo būti atlikti šie veiksmai.

- Patikrinkite, ar turite **Sistemos administratorius** ir **Sistemos tinkinimo priemonė** pasiekti Power Portal administravimo centre.
- Patikrinkite, ar a Dynamics 365 Finance arba lygiavertė licencija taikoma vartotojui, kuris diegia priedą.
- Patikrinkite, ar toliau nurodyta Azure AD programėlė registruota Azure AD: 

  | Prašymas                  | Programos ID           |
  | ---------------------------- | ---------------- |
  | „Microsoft Dynamics ERP Microservices CDS“ | „703e2651-d3fc-48f5-942c-74274233dba8“ | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Požymis: Klaida „Neradome jokių pasirinkto filtro diapazono duomenų. Pasirinkite kitą filtro diapazoną ir bandykite dar kartą. 

### <a name="resolution"></a>Paaiškinimas

Patikrinkite duomenų integratoriaus sąranką, kad patikrintumėte, ar ji veikia taip, kaip tikėtasi, ir iškelia duomenis iš AI Builder atgal į Finansus.  
Daugiau informacijos žr [Sukurkite duomenų integravimo projektą](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Požymis: Kliento mokėjimo numatymo mokymas nepavyko ir AI Builder klaidos būsenos: „Numatymas turi turėti tik 2 skirtingas rezultatų vertes, kad būtų galima parengti modelį. Susiekite su dviem rezultatais ir permokykite“, „Mokymo ataskaitos problema: IsNotMinRequiredDistinctNonNullValues“.

### <a name="resolution"></a>Paaiškinimas

Ši klaida rodo, kad per pastaruosius metus nėra pakankamai istorinių operacijų, atitinkančių kiekvieną kategoriją, aprašytą **Laiku**, **·**, ir **Labai vėlai** kategorijas. Norėdami išspręsti šią klaidą, sureguliuokite **Labai vėlai** sandorio laikotarpis. Jei reguliuojate **Labai vėlai** operacijos laikotarpis nepašalina klaidos, **Klientų mokėjimo prognozės** nėra geriausias sprendimas naudoti, nes mokymo tikslais reikia duomenų kiekvienoje kategorijoje.

Norėdami gauti daugiau informacijos apie tai, kaip sureguliuoti **Laiku**, **·**, ir **Labai vėlai** kategorijas, žr [Įgalinti klientų mokėjimo prognozes](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Požymis: modelio mokymas nepavyko

### <a name="resolution"></a>Paaiškinimas

The **Pinigų srautų prognozė** modelio mokymui reikalingi duomenys, apimantys daugiau nei vienerius metus ir kuriuose yra daugiau nei 100 operacijų. Šios operacijos turi turėti įtakos likvidumo sąskaitoms, kurios yra įtrauktos į pinigų srautų prognozės sąranką.

The **Klientų mokėjimo prognozės** norint sukurti prognozes, reikia bent 100 klientų sąskaitų faktūrų ir mokėjimo operacijų per pastaruosius šešis ar devynis mėnesius.  
