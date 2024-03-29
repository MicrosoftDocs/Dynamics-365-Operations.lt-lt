---
title: Gaunamų prekių apžvalgos profilio nustatymas
description: Šis straipsnis skirtas gavimų apžvalgos profilio nustatymui.
author: yufeihuang
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8517710f5d0be1859f86449152712d950281769a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872013"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Gaunamų prekių apžvalgos profilio nustatymas

[!include [banner](../../includes/banner.md)]

Šis straipsnis skirtas gavimų apžvalgos profilio nustatymui. Gaunamų prekių apžvalgos profilis yra rinkinys taisyklių, kurios taikomos, kai vartotojas atidaro puslapį „Gaunamų prekių apžvalga“. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Šią procedūrą paprastai atlieka gavimo klerkas.

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
11. Lauke **Sandėlis** pasirinkite 24 sandėlį. Tai numatytasis sandėlis, kuris bus naudojamas registruotoms šio profilio gaunamų prekių eilutėms.  
12. Lauke **Vieta** pasirinkite **Galinės durys**. Tai numatytoji vieta, kuri bus naudojama registruotoms šio profilio gaunamų prekių eilutėms.  
13. Išplėskite arba sutraukite skyrių **Gavimo užklausos informacija**.
14. Lauke **Apriboti į vietą** pasirinkite 2 vietą. Nustato filtrą, kad būtų rodomos tik šios teritorijos gaunamų prekių eilutės.  
15. Nustatykite parinkties **Pirkimo užsakymai** nuostatą **Taip**. Pasirinkite gaunamų prekių eilutes iš pirkimo užsakymų.  
16. Nustatykite parinkties **Perkėlimo užsakymai** nuostatą **Taip**. Pasirinkite gaunamų prekių eilutes iš perkėlimo užsakymų.  
17. Pasirinkite **Įrašyti**.
18. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
