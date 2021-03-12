---
title: Gaunamų prekių apžvalgos profilio nustatymas
description: Šioje temoje aprašyta gaunamų prekių apžvalgos profilio sąranka.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ecfe132d9b0e096c5fdf015f80a6efb34c9b178
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961439"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Gaunamų prekių apžvalgos profilio nustatymas

[!include [banner](../../includes/banner.md)]]

Šioje temoje aprašyta gaunamų prekių apžvalgos profilio sąranka. Gaunamų prekių apžvalgos profilis yra rinkinys taisyklių, kurios taikomos, kai vartotojas atidaro puslapį „Gaunamų prekių apžvalga“. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Šią procedūrą paprastai atlieka gavimo klerkas.

1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Paskirstymas > Gaunamų prekių apžvalgos profiliai**.
2. Pasirinkite **Naujas**. Beveik visada teks dirbti tame pačiame sandėlyje iškraunant krovinių pilnus sunkvežimius, todėl turėtumėte sukurti gaunamų prekių apžvalgos profilį, kad supaprastintumėte gautų prekių registravimo procesą.  
3. Lauke **Gaunamų prekių apžvalgos profilio pavadinimas** įveskite reikšmę.
4. Lauke **Rodyti eilutes** pažymėkite parinktį. Pasirinkite, kurias gaunamų prekių eilutes rodyti:  

    - **Visos** – rodomos visos eilutės nepriklausomai nuo būsenos.   
    - **Vykdoma** – rodomos gaunamų prekių, kurių eiga yra Baigta arba Iš dalies, eilutės. Tai reiškia, kad kiekvienai eilutei gaunamų prekių žurnale užregistruotas visas kiekis arba dalis kiekio.   
    - **Nebaigta** – rodomos gaunamų prekių, kurių eiga yra Nėra arba Iš dalies, eilutės. Tai reiškia, kad kiekvienai eilutei gavimo žurnale buvo užregistruota dalis kiekio arba kiekio užregistruota nebuvo.  

5. Išplėskite arba sutraukite skyrių **Gavimo parinktys**.
6. Lauke **Dienos, skaičiuojant pirmyn** įveskite reikšmę. Nustato filtrą, kad būtų rodomos per artimiausias kelias dienas numatomų gauti gaunamų prekių eilutės (atsižvelgiant į jūsų nustatytą skaičių).  
7. Lauke **Dienos, skaičiuojant atgal** įveskite reikšmę. Nustato filtrą, kad būtų rodomos prieš kelias dienas numatytų gauti gaunamų prekių eilutės.  
8. Lauke **Sandėliai** įveskite reikšmę. Filtruokite vieną ar daugiau sandėlių.  
9. Lauke **Pristatymo būdas** pasirinkite reikšmę. Nustato filtrą, kad būtų rodomos tik šio pristatymo būdo gaunamų prekių eilutės.  
10. Lauke **Pavadinimas** pasirinkite WHS.
11. Lauke **Sandėlys** pasirinkite 24 sandėlį. Tai numatytasis sandėlis, kuris bus naudojamas registruotoms šio profilio gaunamų prekių eilutėms.  
12. Lauke **Vieta** pasirinkite **Galinės durys**. Tai numatytoji vieta, kuri bus naudojama registruotoms šio profilio gaunamų prekių eilutėms.  
13. Išplėskite arba sutraukite skyrių **Gavimo užklausos informacija**.
14. Lauke **Apriboti į vietą** pasirinkite 2 vietą. Nustato filtrą, kad būtų rodomos tik šios teritorijos gaunamų prekių eilutės.  
15. Nustatykite parinkties **Pirkimo užsakymai** nuostatą **Taip**. Pasirinkite gaunamų prekių eilutes iš pirkimo užsakymų.  
16. Nustatykite parinkties **Perkėlimo užsakymai** nuostatą **Taip**. Pasirinkite gaunamų prekių eilutes iš perkėlimo užsakymų.  
17. Pasirinkite **Įrašyti**.
18. Uždarykite puslapį.

