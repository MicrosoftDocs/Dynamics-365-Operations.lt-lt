---
title: Duomenų srities nustatymas iš naujo
description: Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988997"
---
# <a name="when-to-reset-a-data-mart"></a>Duomenų srities nustatymas iš naujo

Duomenų srities nustatymas iš naujo gali užimti daug laiko. Atsižvelgiant į aplinkybes, šis veiksmas gali būti netinkamas sprendimas. Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Kada reikia iš naujo nustatyti duomenų sritį?
Apsvarstykite šiuos dalykus prieš iš naujo nustatydami duomenų sritį. Jei atsakysite „taip” į vieną ar daugiau klausimų, vadinasi, jūsų organizacijai gali būti naudinga iš naujo nustatant duomenų sritį.

- Ar buvo atkurta programos duomenų bazė?
- Jei inicijavote pagalbos įvykį ir pagalbos inžinierius jums nurodė atlikti trikčių diagnostikos veiksmą – iš naujo nustatyti duomenų sritį?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Kada nėra tinkama iš naujo nustatyti duomenų sritį?
Tam tikrais atvejais nerekomenduojame iš naujo nustatyti duomenų sritį. Šiais atvejais. 

- Kyla našumo problemų, susietų su duomenų sinchronizavimu. 
- Jei turite pasikartojantį nustatymo iš naujo šabloną dėl šių priežasčių: 
  - **Trūksta duomenų** 
  - **Įstrigti integravimo būsena** 
  - **Pasenę įrašai** – vien dėl pasenusių įrašų nebūtinai atkurti duomenų sritį iš naujo. Jei jūsų duomenų rinkinys didelis, atkūrimo procedūra užtruks, tačiau mažai tikėtina, kad tai išspręs problemą.
 
## <a name="what-is-a-data-mart-reset"></a>Kaip nustatyti iš naujo duomenis?
- Nustatymas iš naujo bus pradedamas, tik tada, kai esamos užduotys bus įvykdytos. Tai užtikrina, kad senieji duomenys nėra įtraukiami. Šiuo metu gali pasirodyti pranešimas: „Nepavyko apdoroti duomenų srities nustatymo iš naujo dėl aktyvios užduoties. Bandykite vėliau”.
- Atkūrimo procedūra išjungs integravimo užduotis ir panaikins visus duomenų srities duomenis. Integravimas įjungtas iš naujo.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Jei iš naujo nustatysite duomenų saugyklą, prarasite jau sukurtas ataskaitas? 
Ne, jūsų ataskaitos saugomos SQL lentelėse, kurių neturi įtakos iš naujo nustatytas duomenų saugyklų nustatymas. Jei susiję su bet kokių jūsų sukurtos ataskaitos praradimu, galite sukurti atsarginę dizainų, kuriuos nenorite prarasti, kopijas. Norėdami sukurti atsarginę jų kopijas, atidarykite Ataskaitų konstruktorius ir pereikite į **Įmonė > Įmonės > Kūrimo blokai > Eksportavimas**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Ar būtina visiems vartotojams išeiti iš sistemos norint iš naujo nustatyti duomenų saugyklą?
Ne, vartotojai gali toliau dirbti sistemoje per duomenų saugyklų iš naujo. Tačiau, kol nebus baigtas nustatymas iš naujo, jie negalės pasiekti jokių ataskaitų, sukurtų su financial Reporter. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
