---
title: Neatitikimo valdymo būtinųjų sąlygų nustatymas
description: Šioje temoje paaiškinta, kaip įgalinti neatitikimo valdymo procesus.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c4de822dcda604241416165a961e4b0bacaeb5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433850"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Neatitikimo valdymo būtinųjų sąlygų nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinta, kaip įgalinti neatitikimo valdymo procesus. Neatitiktyje apibūdinama procedūra arba prekė, kuri turi kokybės problemų, aprašomojoje informacijoje pateiktas problemos šaltinis ir tipas. Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF. Šią procedūrą paprastai atlieka kokybės vadovas.


## <a name="enable-quality-management-processes-within-the-company"></a>Kokybės valdymo procesų įmonėje įgalinimas
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų ir sandėlio valdymo parametrai**.
2. Pasirinkite skirtuką **Kokybės valdymas**.
3. Lauke **Naudoti kokybės valdymą** pasirinkite **Taip**, kad įgalintumėte įmonės kokybės valdymo procesus.
4. Lauke **Valandinis tarifas** įveskite vietine valiuta išreikštą skaičių. Valandinis tarifas naudojamas apskaičiuojant su neatitikimu susijusias operacijų išlaidas. Valandinis tarifas ir apskaičiuotos išlaidos suteikia nuorodos informacijos apie neatitiktį ir nesąveikauja su kitomis funkcijomis.  
5. Pasirinkite **Ataskaitos sąranka**, kad nustatytumėte kokybės ataskaitų pastabų tipus, kurie bus naudojami skirtingose kokybės valdymo ataskaitose.

## <a name="enable-user-for-nonconformance-processing"></a>Leidimas vartotojui apdoroti neatitiktis
1. Naršymo srityje eikite į **Moduliai > Sistemos administravimas > Vartotojai > Vartotojai**. 
2. Naudodami spartųjį filtrą raskite vartotoją, kuris tvirtins arba atmes neatitikimo įrašus. Pavyzdžiui, filtruokite lauką **Vardas** pagal reikšmę `Ricardo`. Norėdamas apdoroti neatitikimo patvirtinimą, vartotojas, kuris patvirtina arba atmeta neatitikimus, puslapyje **Vartotojai** turi turėti priskirtą reikšmę „Vardas“. Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.  
3. Pažymėkite pageidaujamo įrašo eilutę.
4. Pasirinkite **Vartotojo parinktys**.
5. Pasirinkti skirtuką **Nuostatos**.
6. Lauke **Įgalinti dokumentų tvarkymą** pasirinkite **Taip**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Neatitikčių apdorojimo diagnostikos tipų apibrėžimas
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Kokybės valdymas > Diagnozės tipai**. Naudodami puslapį **Diagnozės tipai** nurodykite diagnostikos veiksmų klasifikaciją. Koregavimu identifikuojama, kurio diagnostinio veiksmo turi būti imtasi, atsiradus patvirtintai neatitikčiai, kas turėtų jį atlikti bei pageidaujamą ir planuojamą baigimo datą.  
2. Pasirinkite **Naujas**.
3. Lauke **Diagnostika** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Neatitikčių apdorojimo kokybės išlaidų apibrėžimas
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Kokybės valdymas > Kokybės išlaidos**. Norėdami nustatyti išlaidų klasifikaciją, kuri bus naudojama su neatitikimais susijusiose operacijose, naudokite puslapį **Kokybės išlaidos**.  
2. Pasirinkite **Naujas**.
3. Lauke **Kokybės išlaidos** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.

## <a name="define-the-operations-for-nonconformance-processing"></a>Neatitikčių apdorojimo operacijų apibrėžimas
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Kokybės valdymas > Operacijos**. Norėdami nustatyti darbo, kuris gali būti atliekamas dėl patvirtinto neatitikimo, klasifikaciją, naudokite puslapį **Operacijos**. Susiję operaciją su neatitiktimi galite nurodyti informaciją apie susijusią medžiagą, darbo valandas ir papildomas išlaidas, būtinas atliekant operaciją. Šia informacija bus remiamasi skaičiuojant operacijos atlikimo numatytas išlaidas.  
2. Pasirinkite **Naujas**.
3. Lauke **Operacija** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.

## <a name="define-problem-types-for-nonconformance-processing"></a>Neatitikčių apdorojimo problemų tipų apibrėžimas
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Kokybės valdymas > Problemų tipai**. Norėdami nustatyti kokybės problemų, su kuriomis susiduriama esant įvairių tipų neatitikimams, klasifikaciją, naudokite puslapį **Problemų tipai**. Neatitikimų tipai gali būti: **Vidaus**, **Klientas**, **Tiekėjas**, **Aptarnavimo užklausa**, **Gamyba** ir **Sudėtinio produkto gamyba**. Vieną problemos tipą galima susieti su keliais neatitikčių tipais.  
2. Pasirinkite **Naujas**.
3. Lauke **Problemos tipas** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Pasirinkite **Neatitikimų tipai**. Naudokite puslapį **Neatitikimų tipai**, kad problemos tipą leistumėte naudoti vienam arba daugiau neatitikimų tipų. Pavyzdžiui, problemos, susijusios su defekto kodu, tipas gali būti taikomas visiems neatitikimų tipams, tuo tarpu problemos, susijusios su klientų skundais, tipas gali būti taikomas tik klientų ir aptarnavimo užklausų neatitikimų tipams.  
6. Pasirinkite **Naujas**.
7. Naujos eilutės lauke **Neatitikimo tipas** pasirinkite parinktį.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Neatitikčių apdorojimo sulaikymo zonų apibrėžimas
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Kokybės valdymas > Sulaikymo zonos**.
2. Pasirinkite **Naujas**.
3. Lauke **Sulaikymo zona** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Uždarykite puslapį.

