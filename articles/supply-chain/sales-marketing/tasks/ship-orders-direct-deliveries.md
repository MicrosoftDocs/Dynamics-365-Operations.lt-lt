---
title: Užsakymų siuntimas kaip tiesioginių pristatymų
description: Ši procedūra parodo, kaip kurti pardavimo užsakymo tiesioginį pristatymą.
author: omulvad
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a8f214a56c6a5013cab8233d5b2e0126deb9220
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966110"
---
# <a name="ship-orders-as-direct-deliveries"></a>Užsakymų siuntimas kaip tiesioginių pristatymų

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip kurti pardavimo užsakymo tiesioginį pristatymą. Tiesioginį pristatymą naudojate, kai norite siųsti prekes klientui tiesiogiai iš tiekėjo, vietoj to, kad pirma jas siųstumėte į savo sandėlį. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Norėdami sėkmingai baigti antrąją antrinę užduotį „Kurti tiesioginius pristatymus iš darbastalio“, įsitikinkite, kad, pasirinktos pardavimo užsakymo prekės numatytasis Tiekėjas nurodytas Patvirtintų pagrindinių produktų Pirkimo „FastTab“.

## <a name="set-an-individual-order-for-direct-delivery"></a>Nustatyti atskirą tiesioginio pristatymo užsakymą
1. Eikite į **Valdymo skiltį > Moduliai > Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento sąskaita** įveskite arba pasirinkite reikšmę ir tada pasirinkite **Gerai**.
4. Įveskite arba pasirinkite vertes laukuose **Prekės numeris** ir **Svetainė**, tada spustelėkite **Įrašyti**.
5. Tada veiksmų srityje, skirtuke **Pardavimo užsakymas**, pasirinkite **Tiesioginis pristatymas**. Puslapyje Kurti pristatymą išvardytos visos atvirų pardavimo užsakymų eilutės taip, kaip nukopijuota iš pardavimo užsakymo. Galite peržiūrėti užsakymo informaciją ir, jei reikia, galite modifikuoti informaciją, pvz., pirkimo kiekį ir kainų nustatymo sąlygas, prieš kurdami tiesioginį pristatymą.  
6. Lauke **Įtraukti viską** pasirinkite **Taip**.
    - Jei tiesioginį pristatymą norite sugeneruoti tik pardavimo užsakymo eilučių pogrupiui, pažymėkite jas atskirai.  
    - Lauke **Tiekėjo sąskaita** gali būti įvestas arba dar nebūti įvestas tiekėjo numeris. Jei yra nustatytas produkto numatytasis tiekėjas (susietame Prekės padengime), šis tiekėjas bus nukopijuotas į eilutę. Priešingu atveju, tiekėją turite įvesti rankiniu būdu. Šiame pavyzdyje, kitame veiksme pasirinksime naują tiekėją, net jei jis jau yra įvestas.   
7. Lauke **Tiekėjo sąskaita** įveskite arba pasirinkite reikšmę ir tada pasirinkte **Gerai**. Pranešimas informuoja, kad pirkimo užsakymas sukurtas.   
8. Išplėskite skyrių **Eilutės informacija** section.
9. Pasirinkite skirtuką **Pristatymas** ir patikrinkite, ar laukas **Tiesioginis pristatymas** yra nustatytas į **Taip**.
10. Veiksmų srityje spustelėkite **Bendra**.
11. Pasirinkite **Susiję užsakymai**.
12. Spustelėkite norėdami sekti saitą lauke **Pirkimo užsakymas**.
13. Išplėskite skyrių **Eilutės informacija** ir pasirinkite skirtuką **Adresas**.
    - Atkreipkite dėmesį, kad šios pirkimo užsakymo eilutės pristatymo adresas yra kliento pristatymo adresas, o ne jūsų įmonės adresas.  
    - Jeigu pakeisite pristatymo adresą pardavimo užsakymo eilutėje arba pradinio pardavimo užsakymo eilutėje, pristatymo adresas atitinkamoje užsakymo eilutėje bus automatiškai atnaujintas.  
14. Pasirinkite skirtuką **Pristatymas**.
    - Kaip ir pardavimo užsakymo eilutės, taip ir susieto pirkimo užsakymo eilutės tipas irgi nustatytas į Tiesioginis pristatymas.  
    - Pirkimo užsakymo eilutės Pristatymo data ir Patvirtinta pristatymo data yra nustatytos į Pageidaujama gavimo data ir Patvirtinta gavimo data iš atitinkamos pradinio pardavimo užsakymo eilutės.   
    - Jei atnaujinsite bet kurią iš šių datų arba pirkimo eilutėje, arba pardavimo eilutėje, atitinkamo užsakymo datos bus automatiškai atnaujintos.     
    - Pirkimo užsakymas, kuriame nustatyta prekes pristatyti tiesiogiai klientui, yra specialiu būdu susietas su pradiniu pardavimo užsakymu. Šis susiejimas nustato taisyklę, kad pardavimo užsakymo važtaraščio atnaujinimo negalima atlikti iš paties pardavimo užsakymo, jis turi būti atliekamas naudojant pirkimo užsakymą. Tačiau kliento SF išrašymas atliekamas pagal pardavimo užsakymą.  
15. Veiksmų srityje pasirinkite **Pirkimas**.
16. Pasirinkite **Patvirtinimas**.
17. Pasirinkite **Gerai**.
18. Veiksmų srityje pasirinkite **„Gauti“**.
19. Pasirinkite **„Produkto gavimo kvitas“**.
20. Lauke **Produkto gavimo kvitas** įveskite vertę.
21. Pasirinkite **Gerai**.
22. Veiksmų srityje spustelėkite **Bendra**.
23. Pasirinkite **Susiję užsakymai** ir pažymėkite norimą įrašą.
    - Po to, kai pirkimo užsakymas buvo atnaujintas kaip gautas, arba, kitaip tariant, po to, kai tiekėjas išsiuntė prekes jūsų kliento adresu, pradinio pardavimo užsakymo būsena automatiškai atnaujinama į Pristatyta.  
    - Dabar galima išrašyti pardavimo užsakymo SF.    
24. Pasirinkite **Gerai**.
25. Uždarykite puslapį.
26. Pasirinkite **Gerai**. Uždarykite formą ir grįžkite į pradžios puslapį.

## <a name="create-direct-deliveries-from-the-workbench"></a>Kurti tiesioginius pristatymus iš darbastalio
1. Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento sąskaita** įveskite arba pasirinkite reikšmę ir tada spauskite **Gerai**.
4. Lauke **Prekių skaičius** ir **vieta** įveskite arba pasirinkite reikšmę.
5. Išplėskite skyrių **Eilutės informacija** ir pasirinkite skirtuką **Adresas**. Užuot sukūrę tiesioginį pristatymą kaip pardavimo užsakymo apdorojimo dalį, kaip ir ankstesnėje procedūroje, galite pasirinkti šią užduotį perduoti pirkimo specialistui. Norint pardavimo užsakymo eilutę įtraukti į tiesioginio pristatymo tvarkymo procesą, turite eilutėje pažymėti tiesioginį pristatymą.  
6. Lauke **Tiesioginis pristatymas** pasirinkite **Taip**.
    - Jei prekei jau nustatytas tiesioginis pristatymas pagal numatytuosius nustatymus, užsakymo eilutės įraše laukas bus automatiškai nustatytas į Taip. Galite nustatyti prekės tiesioginį pristatymą Patvirtinto produkto pagrindiniame rodinyje, nustatydami tiesioginio pristatymo pasirinktį į Taip ir pasirinkę numatytąjį Tiesioginio pristatymo sandėlį.  
    - Kadangi dar nesukurtas pirkimo užsakymas, Tiesioginio pristatymo būsena nustatyta į Turi būti pristatyta tiesiogiai.   
7. Pasirinkite **Įrašyti**.
8. Uždarykite formą ir grįžkite į SF sąrašą.
9. Įvesti ieškos kriterijų `Direct delivery` ieškos lauke.
    - Tiesioginio pristatymo puslapis veikia kaip darbastalis, teikiantis pirkimo agentui visų pardavimo užsakymo eilučių, kurios turi būti tiesiogiai pristatytos, apžvalgą ir tai leidžia jiems kurti atitinkamus pirkimo užsakymus. Be to, jie gali peržiūrėti atidarytus tiesioginio pristatymo užsakymus ir patvirtintus užsakymus skirtukuose Patvirtinimas ir Pristatymas.  
    - Sukūrus tiesioginio pristatymo užsakymą, jis automatiškai perkeliamas į skirtuką Patvirtinimas. Galite patvirtinti užsakymą tiesiogiai iš šio puslapio. Kai pirkimas patvirtintas, jis bus automatiškai perkeltas į skirtuką Pristatymas, iš kurio galite registruoti jo gavimą.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]