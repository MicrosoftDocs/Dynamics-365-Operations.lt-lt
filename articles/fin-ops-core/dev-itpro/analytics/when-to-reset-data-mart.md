---
title: Duomenų srities nustatymas iš naujo
description: Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093217"
---
# <a name="when-to-reset-a-data-mart"></a>Duomenų srities nustatymas iš naujo

Duomenų srities nustatymas iš naujo gali užimti daug laiko. Atsižvelgiant į aplinkybes, šis veiksmas gali būti netinkamas sprendimas. Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Kada reikia iš naujo nustatyti duomenų sritį?
Apsvarstykite šiuos dalykus prieš iš naujo nustatydami duomenų sritį. Jei atsakysite „taip” į vieną ar daugiau klausimų, vadinasi, jūsų organizacijai gali būti naudinga iš naujo nustatant duomenų sritį.

- Programos duomenų bazė buvo atkurta, tačiau nebuvo atkurta duomenų srities duomenų bazė.
- Jeigu matote neteisingus apskaitos laikotarpio duomenis, tai nėra ataskaitos maketo klaida.
- Jeigu matote neteisingus ataskaitinio laikotarpio duomenis, ir Ataskaitų kūrimo įrankio **Integravimo būsena** puslapyje išvardinti integravimo bandymų įrašai (įjunkite Ataskaitų kūrimo įrankį ir pasirinkite **Įrankiai > Integravimo būsena**).
- Inicijavote pagalbos įvykį ir pagalbos inžinierius jums nurodė atlikti trikčių diagnostikos veiksmą – iš naujo nustatyti duomenų sritį.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Kada nėra tinkama iš naujo nustatyti duomenų sritį?
Tam tikrais atvejais nerekomenduojame iš naujo nustatyti duomenų sritį. Šiais atvejais. 

- Kitais šioje temoje nenurodytais atvejais.
- Kyla veikimo problemų, susijusių su duomenų sinchronizavimu. Šiuo atveju duomenų srities nustatymas iš naujo tikriausiai nebus veiksmingas.
- Jei turite pasikartojantį nustatymo iš naujo šabloną dėl šių priežasčių: 
  - **Trūksta duomenų** – pirma, pašalinkite ataskaitos kūrimo įrankio ir duomenų sinchronizacijos problemas, pavyzdžiui, pastebėjote, kad susiejimas neįvyko nuo to laiko, kai buvo paskelbti trūkstami duomenys.
  - **Užstrigusi integravimo būsena** – jeigu integracija vyksta lėtai arba sustojo, mažai tikėtina, kad duomenų srities nustatymas iš naujo išspręs problemą.
  - **Bandymai atkurti nepavyko** – jeigu nepavyko atkurti po kelių bandymų dėl trūkstamų duomenų, rekomenduojame inicijuoti pagalbos incidentą ir išanalizuoti situaciją su pagalbos inžinieriumi prieš dar kartą bandant atkurti duomenų sritį.
  - **Pasenę įrašai** – vien dėl pasenusių įrašų nebūtinai atkurti duomenų sritį iš naujo. Jei jūsų duomenų rinkinys didelis, atkūrimo procedūra užtruks, tačiau mažai tikėtina, kad tai išspręs problemą.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Ko duomenų srities atkūrimas neatlieka  
- Nustatymas iš naujo bus pradedamas, tik tada, kai esamos užduotys bus įvykdytos. Tai užtikrina, kad senieji duomenys nėra įtraukiami. Šiuo metu gali pasirodyti pranešimas: „Nepavyko apdoroti duomenų srities nustatymo iš naujo dėl aktyvios užduoties. Bandykite vėliau”.
- Atkūrimo procedūra išjungs integravimo užduotis ir panaikins visus duomenų srities duomenis. Integravimas įjungtas iš naujo.

> [!NOTE]
> Šie aspektai pabrėžia du dalykus, kurių duomenų srities atkūrimas *neatliks*. <br>
> - Atkūrimo procedūra neišvalo ataskaitų kūrimo įrankių. <br>
> - Atkūrimo procedūra neišvalo pasirinktų įmonės ar vartotojų duomenų.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]