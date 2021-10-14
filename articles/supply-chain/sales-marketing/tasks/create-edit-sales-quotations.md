---
title: Kurti ir redaguoti pardavimo pasiūlymus
description: Ši procedūra parodo, kaip sukurti ir atnaujinti pardavimo pasiūlymą.
author: Henrikan
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c409d294565f89eac95e42f6207573d22859100
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578949"
---
# <a name="create-and-edit-sales-quotations"></a>Kurti ir redaguoti pardavimo pasiūlymus

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip sukurti ir atnaujinti pardavimo pasiūlymą. Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF.


## <a name="create-a-sales-quotation"></a>Kurti pardavimo pasiūlymą
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Sąskaitos tipas** pasirinkite „Potencialus klientas”.
4. Lauke **Potencialus klientas** įveskite arba pasirinkite vertę.
5. Išplėskite skyrių **Bendra**. Todėl, kad pasiūlymą kurti pasirinkote iš srities Pardavimas ir rinkodara, tipas automatiškai nustatomas į „Pardavimo pasiūlymą”. Norėdami sukurti projekto pasiūlymą, turite jį pasiekti iš modulio **Projektų valdymas ir apskaita**.
6. Spustelėkite **Gerai**. Laukai ir veiksmai pasiūlymo eilutėse yra labai panašūs į esančius pardavimo užsakymo eilutėse.   Kaip ir pardavimo užsakymus, pasiūlymus galima sukurti tam tikrai prekei arba, kai prekės numeris nežinomas arba jo nėra pasiūlymo kūrimo metu, pasiūlymus galima kurti pardavimo kategorijoje.     
7. Lauke **Prekė** įveskite arba pasirinkite vertę.
8. Lauke **Vieta** įveskite reikšmę.
9. Lauke **Kiekis** įveskite skaičių. Jei yra eilutėje pasirinktos prekės galiojančių prekybos sutarčių, taikomos kainos ir nuolaidos automatiškai nukopijuojamos į pasiūlymo eilutę. Įsitikinkite, kad lauke Vieneto kaina yra vertė, taip pat, jei norite, galite įvesti nuolaidos vertes. 
10. Spustelėkite **Įrašyti**.
11. **Veiksmų srityje** spustelėkite **Pardavimo pasiūlymas**.
12. Spustelėkite **Sumos**.
13. Spustelėkite **Gerai**.
14. Pasirinkite pardavimo pasiūlymo eilutę.
15. **Veiksmų srityje** spustelėkite **Pasiūlymas**.
16. Spustelėkite **Kainos modeliavimas**.
    - Puslapyje **Paleisti kainos modeliavimą** galite eksperimentuoti koreguodami pasiūlymo numatomas įplaukas arba pelningumą pagal norimą vieneto kainą, nuolaidos sumą, nuolaidos procentą, bendrąją sumą, maržą arba kontribucijos maržą. Kai jus tenkina tiksliniai skaičiai, galite pasiūlymą taikyti pasiūlymo eilutei ir jos su kaina susiję laukai bus atitinkamai atnaujinti.  
    - Galite sukurti tiek kainos modeliavimų, kiek norite. Spustelėjus **Naujas**, kainų sąlygos iš dabartinio pasiūlymo eilutės nukopijuojamos į puslapį. Tada galite keisti vertes bet kuriame su kaina susijusiame lauke į tikslines. Pakeitus vieną iš laukų, bus suaktyvintas perskaičiavimas ir kituose laukuose. Norint, kad sistema skaičiuoti pardavimo maržą ir kontribucijos maržą, turi būti žinoma produkto vieneto savikaina. Naudodami skirtuką Modeliuotos kainos matysite išsamų pradinių kainų, siūlomų pakeitimų ir jų poveikio pasiūlymo sumos rodinį. Paprastai, kai modeliuojant nustatoma nauja suma ir ji taikoma pasiūlymo eilutei, sistema perskaičiuoja ir įveda naują vertę lauke Vieneto kaina. Jei modeliavimas pagrįstas nauja marža arba nauja kontribucijos marža, atnaujinamas laukas Grynoji suma, o Vieneto kaina yra tuščias. Abiem atvejais bus panaikintos bet kokios nuolaidos, prieš modeliavimą buvusios pasiūlymo eilutėje.
17. **Veiksmų srityje** spustelėkite **Pasiūlymas**.
18. Spustelėkite **Siųsti pasiūlymą**.
19. Lauke **Spausdinti pasiūlymą** pasirinkite „Taip”.
20. Spustelėkite **Gerai**. Ataskaitą sugeneruoti gali užtrukti minutę. Neuždarykite puslapio, kol tai nebus padaryta.

## <a name="update-a-sales-quotation"></a>Atnaujinti pardavimo pasiūlymą
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai**.
2. **Veiksmų srityje** spustelėkite **Tolesnė veikla**.
3. Spustelėkite **Konvertuoti į klientą**.
4. Lauke **Kliento sąskaita** surinkite reikšmę.
5. Spustelėkite **Tikrinti**. Įsitikinkite, kad matote pranešimą, kuriame teigiama, kad įvestą sąskaitos numerį galima naudoti.  
6. Spustelėkite **Gerai**. Dabar sistema sukūrė naują kliento sąskaitą potencialiam pasiūlymo klientui.  
7. Uždarykite puslapį.
8. **Veiksmų srityje** spustelėkite **Tolesnė veikla**.
9. Spustelėkite **Patvirtinti**.
10. Lauke **Priežastis** įveskite arba pažymėkite reikšmę.
11. Spustelėkite **Gerai**.
12. **Veiksmų sritis** spustelėkite **Bendra**.
13. Spustelėkite **Pardavimo užsakymai**.
14. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]