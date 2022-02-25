---
title: Duomenų srities nustatymo iš naujo DUK
description: Šioje temoje pateikiami atsakymai į kai kuriuos dažnai užduodamus klausimus apie duomenų srities nustatymą iš naujo.
author: jinniew
ms.date: 02/14/2022
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
ms.openlocfilehash: 53f45f469c39f9e389763aa0daed658e5a62d377
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119517"
---
# <a name="data-mart-resets-faq"></a>Duomenų srities nustatymo iš naujo DUK

Šioje temoje pateikiami atsakymai į kai kuriuos dažnai užduodamus klausimus apie duomenų srities nustatymą iš naujo. Duomenų srities nustatymas iš naujo gali būti ilgai trunkantis procesas ir, atsižvelgiant į aplinkybes, gali nebūti reikalingas sprendimas. Todėl šioje temoje pateikiama informacija apie aplinkybes, kai duomenų srities nustatymas iš naujo gali padėti, taip pat apie aplinkybes, kuomet jis padėti negali.

## <a name="what-is-a-data-mart-reset"></a>Kaip nustatyti iš naujo duomenis?

Duomenų srities nustatymas iš naujo išjungs integravimo užduotis, panaikins visus duomenų srities duomenis ir tada iš naujo įgalins integravimą.

Norint užtikrinti, kad seni duomenys nėra įterpti, duomenų srities nustatymą iš naujo galima pradėti tik atlikus esamas užduotis. Jei bandysite iš naujo nustatyti duomenų sritį neatlikę visų užduočių, galite gauti pranešimą, pavyzdžiui, „Duomenų srities nustatymo iš naujo nustatyti nepavyko apdoroti dėl aktyvios užduoties. Bandykite vėliau.“

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Kada turiu iš naujo nustatyti duomenų sritį?

Jei jūsų situacijai tinka vienas ar daugiau iš šių sakinių, jūsų organizacijai gali būti naudinga iš naujo nustatyti duomenų sritį:

- **Programos duomenų bazė buvo atkurta**
- **Atidarėte palaikymo bilietą** – palaikymo inžinierius nurodėte iš naujo nustatyti duomenų saugyklą kaip trikčių diagnostikos veiksmo dalį.
- **Didelis pasenusių įrašų procentas –** patys susenę įrašai nebūtinai atspindi duomenų saugyklų iš naujo nustatymus. Dėl didelės duomenų pasenusios procentinės dalies gali sumažėti bendras ataskaitos generavimas ir integravimo našumas bei gali būti papildomai naudojama duomenų bazės vieta. Rekomenduojame duomenų saugyklą nustatyti iš naujo, kad būtų pašalinti pasenusii duomenys, kai duomenų saugykloje yra daugiau nei 80% pasenusių duomenų.
 
> [!NOTE]
> Duomenų srities nustatymą iš naujo paveikia didžiosios knygos ir biudžeto operacijos jūsų duomenų bazėje. Priklausomai nuo operacijų skaičiaus jūsų sistemoje, duomenų srities nustatymas iš naujo gali būti atliktas per 15 minučių arba užtrukti iki keturių valandų. Jei jūsų nustatymas iš naujo užtrunka ilgiau nei keturias valandas, rekomenduojame kreiptis į klientų aptarnavimo tarnybą.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Kada duomenų srities nustatymas iš naujo yra netinkamas?

Šiomis tam tikromis aplinkybėmis nerekomenduojame jums iš naujo nustatyti duomenų sritį:

- Patiriate duomenų integravimo našumo problemas.
- Turite pasikartojantį nustatymo iš naujo šabloną dėl bet kurios iš šių priežasčių:

    - **Trūksta arba netikėtų duomenų ataskaitoje** – jei pastebite, kad duomenų nėra, atidarykite palaikymo kvitą "Microsoft", kad peržiūrėtumėte savo ataskaitos formatą ir galimus duomenų sinchronizavimo klausimus.
    - **Įstrigti integravimo būsena**
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Jei iš naujo nustatysite duomenų saugyklą, prarasite jau sukurtas ataskaitas?

Ne. Jūsų ataskaitos saugomos SQL lentelėse, kurių nepaveikia duomenų srities nustatymas iš naujo. Jei esate susirūpinę, kad prarasite savo sukurtas ataskaitas, galite sukurti atsargines dizainų, kurių nenorite prarasti, kopijas. Norėdami sukurti atsargines kopijas, atidarykite „Report Designer” ir eikite į **Įmonė \> Įmonės \> Kūrimo blokai \> Eksportavimas**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Ar visi vartotojai turi išeiti iš sistemos, kad galėčiau iš naujo nustatyti duomenų sritį?

Ne. Vartotojai gali ir toliau dirbti sistemoje duomenų srities nustatymo iš naujo metu. Tačiau, kol nebus baigtas nustatymas iš naujo, vartotojai negalės pasiekti jokių ataskaitų, sukurtų naudojant „Financial Reporter”.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
