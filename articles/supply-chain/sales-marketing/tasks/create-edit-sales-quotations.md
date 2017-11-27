--- 
title: "Kurti ir redaguoti pardavimo pasiūlymus"
description: "Ši procedūra parodo, kaip sukurti ir atnaujinti pardavimo pasiūlymą."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 7ffa4fe8d87db5b3f8293ec9dbc042496d09d6e3
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="create-and-edit-sales-quotations"></a>Kurti ir redaguoti pardavimo pasiūlymus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip sukurti ir atnaujinti pardavimo pasiūlymą. Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF.


## <a name="create-a-sales-quotation"></a>Kurti pardavimo pasiūlymą
1. Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.
2. Spustelėkite Naujas.
3. Lauke Sąskaitos tipas pasirinkite 'Potencialus klientas'.
4. Lauke Potencialus klientas įveskite arba pasirinkite vertę.
5. Išplėskite skyrių Bendra.
    * Todėl, kad pasiūlymą kurti pasirinkote iš srities Pardavimas ir rinkodara, tipas automatiškai nustatomas į Pardavimo pasiūlymą. Norėdami sukurti projekto pasiūlymą, turite jį pasiekti iš modulio Projektų valdymas ir apskaita.   
6. Spustelėkite GERAI.
    * Laukai ir veiksmai pasiūlymo eilutėse yra labai panašūs į esančius pardavimo užsakymo eilutėse.   Kaip ir pardavimo užsakymus, pasiūlymus galima sukurti tam tikrai prekei arba, kai prekės numeris nežinomas arba jo nėra pasiūlymo kūrimo metu, pasiūlymus galima kurti pardavimo kategorijoje.  
7. Lauke Prekė įveskite arba pasirinkite vertę.
8. Lauke Prekė įveskite vertę.
9. Uždarykite puslapį.
10. Lauke Kiekis įveskite skaičių.
    * Jei yra eilutėje pasirinktos prekės galiojančių prekybos sutarčių, taikomos kainos ir nuolaidos automatiškai nukopijuojamos į pasiūlymo eilutę. Įsitikinkite, kad lauke Vieneto kaina yra vertė, taip pat, jei norite, galite įvesti nuolaidos vertes.  
11. Spustelėkite Įrašyti.
12. Srityje Veiksmas spustelėkite Pardavimo pasiūlymas.
13. Spustelėkite Sumos.
14. Spustelėkite GERAI.
15. Spustelėkite eilutę Pardavimo pasiūlymas.
16. Spustelėkite Kainos.
    * Puslapyje Paleisti kainos modeliavimą galite eksperimentuoti koreguodami pasiūlymo numatomas įplaukas arba pelningumą pagal norimą vieneto kainą, nuolaidos sumą, nuolaidos procentą, bendrąją sumą, maržą arba kontribucijos maržą.   Kai jus tenkina tiksliniai skaičiai, galite pasiūlymą taikyti pasiūlymo eilutei ir jos su kaina susiję laukai bus atitinkamai atnaujinti.  
    * Galite sukurti tiek kainos modeliavimų, kiek norite. Spustelėjus Naujas, kainų sąlygos iš dabartinio pasiūlymo eilutės nukopijuojamos į puslapį. Tada galite keisti vertes bet kuriame su kaina susijusiame lauke į tikslines. Pakeitus vieną iš laukų, bus suaktyvintas perskaičiavimas ir kituose laukuose. Norint, kad sistema skaičiuoti pardavimo maržą ir kontribucijos maržą, turi būti žinoma produkto vieneto savikaina. Naudodami skirtuką Modeliuotos kainos matysite išsamų pradinių kainų, siūlomų pakeitimų ir jų poveikio pasiūlymo sumos rodinį.   Paprastai, kai modeliuojant nustatoma nauja suma ir ji taikoma pasiūlymo eilutei, sistema perskaičiuoja ir įveda naują vertę lauke Vieneto kaina. Jei modeliavimas pagrįstas nauja marža arba nauja kontribucijos marža, atnaujinamas laukas Grynoji suma, o Vieneto kaina yra tuščias. Abiem atvejais bus panaikintos bet kokios nuolaidos, prieš modeliavimą buvusios pasiūlymo eilutėje.  
17. Uždarykite puslapį.
18. Veiksmų srityje spustelėkite Pasiūlymas.
19. Spustelėkite Siųsti pasiūlymą.
20. Lauke Spausdinti pasiūlymą pasirinkite Taip.
21. Spustelėkite GERAI.
    * Ataskaitą sugeneruoti gali užtrukti minutę. Neuždarykite puslapio, kol tai nebus padaryta.  
22. Uždarykite puslapį.

## <a name="update-a-sales-quotation"></a>Atnaujinti pardavimo pasiūlymą
1. Veiksmų srityje spustelėkite Vykdymas.
2. Spustelėkite Konvertuoti į klientą.
3. Lauke Kliento sąskaita surinkite reikšmę.
4. Spustelėkite Tikrinti.
    * Įsitikinkite, kad matote pranešimą, kuriame teigiama, kad įvestą sąskaitos numerį galima naudoti.  
5. Spustelėkite GERAI.
    * Dabar sistema sukūrė naują kliento sąskaitą potencialiam pasiūlymo klientui.  
6. Uždarykite puslapį.
7. Veiksmų srityje spustelėkite Vykdymas.
8. Spustelėkite Patvirtinti.
9. Lauke Priežastis įveskite arba pasirinkite vertę.
10. Spustelėkite GERAI.
11. Veiksmų srityje spustelėkite Bendra.
12. Spustelėkite Pardavimo užsakymai.
13. Uždarykite puslapį.


