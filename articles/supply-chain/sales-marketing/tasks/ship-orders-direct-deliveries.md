---
title: Užsakymų siuntimas kaip tiesioginių pristatymų
description: Ši procedūra parodo, kaip kurti pardavimo užsakymo tiesioginį pristatymą.
author: omulvad
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchEditLines, PurchTableReferences, MCRDropShipWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bce2674b321475bc516724f74bac2d3a648e257
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843366"
---
# <a name="ship-orders-as-direct-deliveries"></a>Užsakymų siuntimas kaip tiesioginių pristatymų

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip kurti pardavimo užsakymo tiesioginį pristatymą. Tiesioginį pristatymą naudojate, kai norite siųsti prekes klientui tiesiogiai iš tiekėjo, vietoj to, kad pirma jas siųstumėte į savo sandėlį. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Norėdami sėkmingai baigti antrąją antrinę užduotį „Kurti tiesioginius pristatymus iš darbastalio“, įsitikinkite, kad, pasirinktos pardavimo užsakymo prekės numatytasis Tiekėjas nurodytas Patvirtintų pagrindinių produktų Pirkimo „FastTab“.

## <a name="set-an-individual-order-for-direct-delivery"></a>Nustatyti atskirą tiesioginio pristatymo užsakymą
1. Eikite į **Valdymo skiltį > Moduliai > Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Customer accound** įveskite arba pasirinkite reikšmę ir tada pasirinkite **OK**.
4. Įveskite arba pasirinkite vertes laukuose **Prekės numeris** ir **Svetainė**, tada spustelėkite **Įrašyti**.
5. Tada veiksmų srityje, skirtuke **Pardavimo užsakymas**, pasirinkite **Tiesioginis pristatymas**. Puslapyje Kurti pristatymą išvardytos visos atvirų pardavimo užsakymų eilutės taip, kaip nukopijuota iš pardavimo užsakymo. Galite peržiūrėti užsakymo informaciją ir, jei reikia, galite modifikuoti informaciją, pvz., pirkimo kiekį ir kainų nustatymo sąlygas, prieš kurdami tiesioginį pristatymą.  
6. Lauke **Include all**pasirinkite **Yes**.
    - Jei tiesioginį pristatymą norite sugeneruoti tik pardavimo užsakymo eilučių pogrupiui, pažymėkite jas atskirai.  
    - Lauke **Vendor account** gali būti įvestas arba dar nebūti įvestas tiekėjo numeris. Jei yra nustatytas produkto numatytasis tiekėjas (susietame Prekės padengime), šis tiekėjas bus nukopijuotas į eilutę. Priešingu atveju, tiekėją turite įvesti rankiniu būdu. Šiame pavyzdyje pasirinksime naują tiekėją kitame veiksme, net jei jis jau įvestas.   
7. Lauke **Vendor account** įveskite arba pasirinkite reikšmę ir tada pasirinkte **OK**. Pranešimas informuoja, kad pirkimo užsakymas sukurtas.   
8. Išplėskite skyrių **Line details** section.
9. Pasirinkite skirtuką **Delivery** ir patikrinkite, ar laukas **Direct delivery** yra nustatytas į **Yes**.
10. Veiksmų srityje spustelėkite **General**.
11. Pasirinkite **Susiję užsakymai**.
12. Spustelėkite norėdami sekti saitą lauke **Purchase order**.
13. Išplėskite skyrių **Eilutės informacija** ir pasirinkite skirtuką **Adresas**.
    - Atkreipkite dėmesį, kad šios pirkimo užsakymo eilutės pristatymo adresas yra kliento pristatymo adresas, o ne jūsų įmonės adresas.  
    - Jeigu pakeisite pristatymo adresą pardavimo užsakymo eilutėje arba pradinio pardavimo užsakymo eilutėje, pristatymo adresas atitinkamoje užsakymo eilutėje bus automatiškai atnaujintas.  
14. Pasirinkti **Delivery** sąlygas.
    - Kaip ir pardavimo užsakymo eilutės, taip ir susieto pirkimo užsakymo eilutės tipas irgi nustatytas į Tiesioginis pristatymas.  
    - Pirkimo užsakymo eilutės Pristatymo data ir Patvirtinta pristatymo data yra nustatytos į Pageidaujama gavimo data ir Patvirtinta gavimo data iš atitinkamos pradinio pardavimo užsakymo eilutės.   
    - Jei atnaujinsite bet kurią iš šių datų arba pirkimo eilutėje, arba pardavimo eilutėje, atitinkamo užsakymo datos bus automatiškai atnaujintos.     
    - Pirkimo užsakymas, kuriame nustatyta prekes pristatyti tiesiogiai klientui, yra specialiu būdu susietas su pradiniu pardavimo užsakymu. Šis susiejimas nustato taisyklę, kad pardavimo užsakymo važtaraščio atnaujinimo negalima atlikti iš paties pardavimo užsakymo, jis turi būti atliekamas naudojant pirkimo užsakymą. Tačiau kliento SF išrašymas atliekamas pagal pardavimo užsakymą.  
15. Veiksmų srityje pasirinkite **Pirkimas**.
16. Pasirinkite **Confirmation**.
17. Pasirinkite **Gerai**.
18. Veiksmų srityje pasirinkite **„Gauti“**.
19. Pasirinkite **„Produkto gavimo kvitas“**.
20. Lauke **Produkto gavimo kvitas** įveskite vertę.
21. Pasirinkite **Gerai**.
22. Veiksmų srityje spustelėkite **General**.
23. Pasirinkite **Susiję užsakymai** ir pažymėkite norimą įrašą.
    - Po to, kai pirkimo užsakymas buvo atnaujintas kaip gautas, arba, kitaip tariant, po to, kai tiekėjas išsiuntė prekes jūsų kliento adresu, pradinio pardavimo užsakymo būsena automatiškai atnaujinama į Pristatyta.  
    - Dabar galima išrašyti pardavimo užsakymo SF.    
24. Pasirinkite **Gerai**.
25. Uždarykite puslapį.
26. Pasirinkite **Gerai**. Uždarykite formą ir grįžkite į pradžios puslapį.

## <a name="create-direct-deliveries-from-the-workbench"></a>Kurti tiesioginius pristatymus iš darbastalio
1. Eikite į **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.
2. Pasirinkite **Naujas**.
3. Lauke **Customer account** įveskite arba pasirinkite reikšmę ir tada spauskite **OK**.
4. Lauke **Item number** ir **site** įveskite arba pasirinkite reikšmę.
5. Išplėskite skyrių **Eilutės informacija** ir pasirinkite skirtuką **Adresas**. Užuot sukūrę tiesioginį pristatymą kaip pardavimo užsakymo apdorojimo dalį, kaip ir ankstesnėje procedūroje, galite pasirinkti šią užduotį perduoti pirkimo specialistui. Norint pardavimo užsakymo eilutę įtraukti į tiesioginio pristatymo tvarkymo procesą, turite eilutėje pažymėti tiesioginį pristatymą.  
6. Lauke **Direct delivery** pasirinkite **Yes**.
    - Jei prekei jau nustatytas tiesioginis pristatymas pagal numatytuosius nustatymus, užsakymo eilutės įraše laukas bus automatiškai nustatytas į Taip. Galite nustatyti prekės tiesioginį pristatymą Patvirtinto produkto pagrindiniame rodinyje, nustatydami tiesioginio pristatymo pasirinktį į Taip ir pasirinkę numatytąjį Tiesioginio pristatymo sandėlį.  
    - Kadangi dar nesukurtas pirkimo užsakymas, Tiesioginio pristatymo būsena nustatyta į Turi būti pristatyta tiesiogiai.   
7. Pasirinkite **Įrašyti**.
8. Uždarykite formą ir grįžkite į SF sąrašą.
9. Įvesti ieškos kriterijų `Direct delivery` ieškos lauke.
    - Tiesioginio pristatymo puslapis veikia kaip darbastalis, teikiantis pirkimo agentui visų pardavimo užsakymo eilučių, kurios turi būti tiesiogiai pristatytos, apžvalgą ir tai leidžia jiems kurti atitinkamus pirkimo užsakymus. Be to, jie gali peržiūrėti atidarytus tiesioginio pristatymo užsakymus ir patvirtintus užsakymus skirtukuose Patvirtinimas ir Pristatymas.  
    - Sukūrus tiesioginio pristatymo užsakymą, jis automatiškai perkeliamas į skirtuką Patvirtinimas. Galite patvirtinti užsakymą tiesiogiai iš šio puslapio. Kai pirkimas patvirtintas, jis bus automatiškai perkeltas į skirtuką Pristatymas, iš kurio galite registruoti jo gavimą.  

