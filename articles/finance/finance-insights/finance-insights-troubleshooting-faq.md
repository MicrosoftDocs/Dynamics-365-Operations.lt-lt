---
title: „Finance insights“ apie nustatymą trikčių šalinimas
description: Šiame straipsnyje pateikiamos problemos, kurios gali įvykti, kai naudojate finansų žinių galimybes. Taip pat paaiškinama, kaip išspręsti šias problemas.
author: panolte
ms.date: 02/11/2022
ms.topic: article
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
ms.author: panolte
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 1ee354a1c3d9b45eb12eeb3a6a29f2a6d5e4c34c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846921"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>„Finance insights“ apie nustatymą trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos problemos, kurios gali įvykti, kai naudojate finansų žinių galimybes. Taip pat paaiškinama, kaip išspręsti šias problemas.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Požymis: kodėl negalima susieti kliento mokėjimo žinių apie duomenų integravimo šablono paskirties stulpelį?

### <a name="resolution"></a>Sprendimas

Galbūt naudojate ankstesnės versijos šabloną. Prieš išleisdami 10.0.17 versiją peržiūrėkite klientus, sukonfigūravo **kliento mokėjimo žinių rezultatus (CDS į Fin ir Ops)** duomenų integravimo (DI) šabloną naudodami **mokėjimo numatymo rezultato (peržiūros)** objektą. Atnaujinę į 10.0.17 ar vėlesnę versiją, norėdami baigti susiejimą, turite naudoti **kliento mokėjimo žinių rezultatus (CDS į Fin ur Ops 10.0.17 ir vėlesnės)** DI versijos. Gali būti, kad negalėsite susieti DI šablono paskirties stulpelio, kol nebus atnaujintas duomenų valdymo objektų sąrašas ir jame atsiras **mokėjimo numatymo rezultato** objektas. Norėdami atnaujinti objektų sąrašą ir rodyti mokėjimo numatymo rezultatą, atlikite veiksmus ir 365 finansuose, Microsoft Dynamics ir (Dataverse Common Data Service anksčiau vadinama CDS\[ administratoriaus portalu).\]

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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Požymis: AI Builder Kai bandau atidaryti naudodami kliento mokėjimo numatyimų nustatymo puslapio saitus, kodėl gaunu tokį klaidos pranešimą: "Atsiprašome, čia atjungta?

### <a name="resolution"></a>Paaiškinimas

"Dynamics 365" finansų vartotojai turi Microsoft Power Apps turėti aplinkos vartotojo abonementą, tam vartotojo abonementui turi būti skirtas sistemos pritaikymo priemonės vaidmuo. Sistemos Microsoft Power Apps administratorius gali sukurti vartotojo abonementą ir priskirti vaidmenį. Tada, naudodami tą vartotojo <https://make.preview.powerapps.com/> abonementą, galite įeiti, ir bandyti saitus dar kartą.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Požymis: kodėl pinigų srautų prognozės darbo srityje nėra pinigų prognozės skirtuko, kuriame rodomi kokie nors duomenys?

### <a name="resolution"></a>Sprendimas

Pinigų srautų prognozės funkcija grynųjų pinigų ir banko valdymo srityje ir pinigų srautų prognozių funkcija turi būti nustatyta ir įgalinta „Finance insights“ srityje, kad duomenys būtų tinkamai rodomi pinigų **srautų prognozės** darbo srityje.

Pirmiausia nustatykite ir įgalinkite pinigų srautų prognozavimo ir likvidumo sąskaitas. Daugiau informacijos žr. [Pinigų srauto planavimas](../cash-bank-management/cash-flow-forecasting.md). Jei šis nustatymas baigtas, bet nematote jokių rezultatų, kuriuos tikitės, daugiau informacijos žr. pinigų srautų [prognozės nustatymo trikčių](../cash-bank-management/cash-flow-forecasting-tsg.md) šalinimas.

Po to patvirtinkite, kad pinigų srautų prognozių funkcija finansų žinių srityje (**grynųjų pinigų ir banko valdymas \> Nustatymai \> Finance Insights \> Pinigų srauto prognozės**) yra įgalintos ir kad AI modelio mokymas baigtas. Jei mokymas baigtas, norėdami pradėti mokymo proceso modelį, pasirinkite **Prognozė dabar**.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Požymis: kodėl nėra naujo priedo mygtuko, matomo ciklo Microsoft Dynamics tarnybose?

### <a name="resolution"></a>Paaiškinimas

Pirmiausia patikrinkite, **·** **·** **·** Microsoft Dynamics ar aplinkos tvarkytuvo arba projekto savininko vaidmuo priskirtas prisiregistravęs vartotojui ciklo tarnybų (LCS) lauke Projekto saugos vaidmuo. Naujiems papildiniai įdiegti reikalauja vieno iš šių projekto saugos vaidmenų.

Jei jums priskirtas tinkamas projekto saugos vaidmuo, gali tekti atnaujinti naršyklės langą, kad **būtų galima matyti naujo priedo diegimo** mygtuką.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Požymis: finansų žinių priedas nebūtinai turi būti diegiamas. Kodėl taip?

### <a name="resolution"></a>Paaiškinimas

Turi būti atlikti šie veiksmai.

- Patikrinkite, ar turite sistemos **administratoriaus** ir sistemos **pritaikymo vartotojo** prieigą "Power Portal" administravimo centre.
- Patikrinkite, ar "Dynamics 365" finansų arba ekvivalentinės licencijos yra taikomos papildinį diegiantiems vartotojams.
- Patikrinkite, ar užregistruota Azure AD ši programa Azure AD: 

  | Prašymas                  | Programos ID           |
  | ---------------------------- | ---------------- |
  | „Microsoft Dynamics ERP Microservices CDS“ | „703e2651-d3fc-48f5-942c-74274233dba8“ | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Požymis: klaida, "Neradome jokių pasirinkto filtro diapazono duomenų. Pasirinkite kitą filtro diapazoną ir bandykite dar kartą." 

### <a name="resolution"></a>Paaiškinimas

Patikrinkite duomenų integratoriaus nustatymą, AI Builder kad patvirtintumėte, jog jis veikia, kaip numatyta, ir duomenų gavimas iš atgal į finansus.  
Daugiau informacijos rasite Duomenų [integravimo projekto kūrimas](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Požymis: kliento mokėjimo numatymas AI Builder nesėkmingas, o klaidų teigiama, kad "Numatymas turi turėti tik 2 skirtingas rezultato vertes, kad būtų galima naudoti modelį traukinyje. Susiekite su dviem rezultatais ir apribojimu– "Mokymo ataskaitos išdavimas: IsNotMinRequiredDistinctNonNargValues".

### <a name="resolution"></a>Paaiškinimas

Ši klaida nurodo **, kad praėjusiais metais nepakanka retrospektyvinių operacijų, kurios atitinka kiekvieną kategoriją, aprašyą kategorijoje, aprašytaoje laiku,** **pavėluotai** ir labai pavėluotai **.** Norėdami ištaisyti šią klaidą, pakoregkite **labai vėlų** operacijos laikotarpį. Jei pakoreguojant **labai** vėlų operacijos laikotarpį klaida neištaisoma, **kliento** mokėjimų numatymas nėra geriausias būdas naudoti, nes mokymo tikslais reikia duomenų kiekvienoje kategorijoje.

Daugiau informacijos apie tai, kaip koreguoti **kategorijas Laiku**, **Pavėluota** **ir Labai vėlai**, žr [. Įgalinkite kliento mokėjimų numatymas](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Požymis: modelio mokymas nepavyko

### <a name="resolution"></a>Paaiškinimas

Pinigų **srautų prognozės** modelio mokymas reikalauja duomenų, kurių yra 100 ar daugiau operacijų, kurios apima daugiau nei metus. Rekomenduojame turėti mažiausiai dviejų metų duomenis su daugiau nei 1000 operacijų.

Kliento **mokėjimų numatymo funkcija reikalauja daugiau** nei 100 operacijų per praėjusius šešis iki devynių mėnesių. Operacijos gali būti laisvos formos SF, pardavimo užsakymai ir kliento mokėjimai. Šie duomenys turi būti paskirstyti laiku **, pavėluotai** ir **labai** **vėlai nustatyti** konfigūracijos **puslapyje**.    

Biudžeto **pasiūlymo funkcijai** reikia bent trijų metų biudžeto arba faktinių duomenų. Šis sprendimas naudoja trijų–dešimties metų duomenis projekcijose. Daugiau nei trys metai duos geresnių rezultatų. Pati data tinka geriausiai, kai vertės gali variacijos. Jei duomenyse yra visi pastovūs duomenys, pvz., nuomos išlaidos, mokymas gali nepavykti, nes trūksta pokyčio nereikalauja AI, kad būtų galima projektuoti sumas.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Požymis: klaidos pranešimas rodo, kad lentelės pavadinimu msdyn_paypredpredictionresultentities nėra. Nuotolinis serveris pateikė klaidą: (404) Nerasta..."

### <a name="resolution"></a>Paaiškinimas

Aplinkoje pasiektas maksimalus duomenų Paslaugų lentelės limitas. Daugiau informacijos apie limitą ieškokite straipsnio skyriuje **Įgalinti beveik** realiuoju laiku atliktus duomenų keitimus, [Eksportuokite į "Azure Data Azure Data Azure" apžvalgą](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
