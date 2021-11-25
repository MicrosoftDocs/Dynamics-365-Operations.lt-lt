---
title: „Finance insights“ apie nustatymą trikčių šalinimas
description: Šioje temoje išvardijamos problemos, kurios gali įvykti, kai naudojate „Finance insights“ galimybes. Taip pat paaiškinama, kaip išspręsti šias problemas.
author: panolte
ms.date: 11/03/2021
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
ms.openlocfilehash: f3cac30a66ff3a74a7f67c11dd9fa14af79d10af
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752622"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>„Finance insights“ apie nustatymą trikčių šalinimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje išvardijamos problemos, kurios gali įvykti, kai naudojate „Finance insights“ galimybes. Taip pat paaiškinama, kaip išspręsti šias problemas.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Požymis: kodėl negalima susieti kliento mokėjimo žinių apie duomenų integravimo šablono paskirties stulpelį?

### <a name="resolution"></a>Sprendimas

Galbūt naudojate ankstesnės versijos šabloną. Prieš išleisdami 10.0.17 versiją peržiūrėkite klientus, sukonfigūravo **kliento mokėjimo žinių rezultatus (CDS į Fin ir Ops)** duomenų integravimo (DI) šabloną naudodami **mokėjimo numatymo rezultato (peržiūros)** objektą. Atnaujinę į 10.0.17 ar vėlesnę versiją, norėdami baigti susiejimą, turite naudoti **kliento mokėjimo žinių rezultatus (CDS į Fin ur Ops 10.0.17 ir vėlesnės)** DI versijos. Gali būti, kad negalėsite susieti DI šablono paskirties stulpelio, kol nebus atnaujintas duomenų valdymo objektų sąrašas ir jame atsiras **mokėjimo numatymo rezultato** objektas. Norėdami atnaujinti objektų sąrašą ir rodyti mokėjimo numatymo rezultatą, atlikite veiksmus ir „Microsoft Dynamics 365 Finance“ ir „Dataverse“ (anksčiau žinoma kaip „Common Data Service“ \[ CDS\] administravimo portale).

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

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Požymis: Kai bandau atidaryti AI generatorių naudojant kliento mokėjimų numatyimų nustatymo puslapio saitus, kodėl gaunu tokį klaidos pranešimą: "Atsiprašome, tai buvo atjungta?

### <a name="resolution"></a>Paaiškinimas

Dynamics 365 Finance vartotojai turi turėti Microsoft Power Apps aplinkos vartotojo abonementą, o tam vartotojo abonementui turi būti skirtas sistemos pritaikymo priemonės vaidmuo. Sistemos Microsoft Power Apps administratorius gali sukurti vartotojo abonementą ir priskirti vaidmenį. Tada, naudodami tą <https://make.preview.powerapps.com/> vartotojo abonementą, galite įeiti, ir bandyti saitus dar kartą.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Požymis: kodėl pinigų srautų prognozės darbo srityje nėra pinigų prognozės skirtuko, kuriame rodomi kokie nors duomenys?

### <a name="resolution"></a>Sprendimas

Pinigų srautų prognozės funkcija grynųjų pinigų ir banko valdymo srityje ir pinigų srautų prognozių funkcija turi būti nustatyta ir įgalinta „Finance insights“ srityje, kad duomenys būtų tinkamai rodomi pinigų **srautų prognozės** darbo srityje.

Pirmiausia nustatykite ir įgalinkite pinigų srautų prognozavimo ir likvidumo sąskaitas. Daugiau informacijos žr. [Pinigų srauto planavimas](../cash-bank-management/cash-flow-forecasting.md). Jei šis nustatymas baigtas, bet nematote jokių rezultatų, kuriuos tikitės, daugiau informacijos žr. pinigų srautų [prognozės nustatymo trikčių](../cash-bank-management/cash-flow-forecasting-tsg.md) šalinimas.

Po to patvirtinkite, kad pinigų srautų prognozių funkcija finansų žinių srityje (**grynųjų pinigų ir banko valdymas \> Nustatymai \> Finance Insights \> Pinigų srauto prognozės**) yra įgalintos ir kad AI modelio mokymas baigtas. Jei mokymas baigtas, norėdami pradėti mokymo proceso modelį, pasirinkite **Prognozė dabar**.
