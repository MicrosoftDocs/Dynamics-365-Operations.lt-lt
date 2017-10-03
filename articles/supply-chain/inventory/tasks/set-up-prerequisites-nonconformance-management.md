---
title: "Nustatyti valdymo būtinąsias sąlygas"
description: "Naudokite šią procedūrą, kad įgalintumėte neatitikčių valdymo procesus."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: e8f7ec305316b5290019ec28deed1cae382e93b3
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-prerequisites-for-management"></a>Nustatyti valdymo būtinąsias sąlygas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Naudokite šią procedūrą, kad įgalintumėte neatitikčių valdymo procesus. Neatitiktyje apibūdinama procedūra arba prekė, kuri turi kokybės problemų, aprašomojoje informacijoje pateiktas problemos šaltinis ir tipas. Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF. Šią procedūrą paprastai atlieka kokybės vadovas.


## <a name="enable-quality-management-processes-within-the-company"></a>Kokybės valdymo procesų įmonėje įgalinimas
1. Pasirinkite Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai.
2. Spustelėkite skirtuką Kokybės valdymas.
3. Lauke Naudoti kokybės valdymą pasirinkite Taip.
    * Pasirinkite šį parametrą, kad įgalintumėte įmonės kokybės valdymo procesus.  
4. Lauke Valandinis tarifas įveskite skaičių.
    * Naudokite lauką Valandinis tarifas, kad įvestumėte valandinį darbo tarifą vietine valiuta. Valandinis tarifas naudojamas apskaičiuojant su neatitikimu susijusias operacijų išlaidas. Valandinis tarifas ir apskaičiuotos išlaidos suteikia nuorodos informacijos apie neatitiktį ir nesąveikauja su kitomis funkcijomis.  
5. Spustelėkite Ataskaitų sąranka.
    * Šiame puslapyje galima apibrėžti kokybės ataskaitų pastabų tipus, kurie bus naudojami įvairių rūšių kokybės valdymo ataskaitose.  
6. Uždarykite puslapį.
7. Uždarykite puslapį.

## <a name="enable-user-for-nonconformance-processing"></a>Leidimas vartotojui apdoroti neatitiktis
1. Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.
    * Norint apdoroti neatitikties patvirtinimą, neatitiktis patvirtinusiam ar atmetusiam vartotojui puslapyje Vartotojai turi būti priskirta reikšmė Pavadinimas. Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.  
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Pavadinimas reikšme „Ricardo‟.
    * Naudokite filtrą, kad rastumėte vartotoją, kuris tvirtins arba atmes neatitikimo įrašus.  
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Norėdami apdoroti neatitikties patvirtinimą, pasirūpinkite, kad neatitiktis patvirtinusiam ar atmetusiam vartotojui puslapyje Vartotojai būtų priskirta reikšmė Pavadinimas.  
4. Spustelėkite Vartotojo parinktys.
5. Spustelėkite skirtuką Nuostatos.
6. Lauke Įgalinti dokumentų tvarkymą pasirinkite Taip.
    * Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.  
7. Uždarykite puslapį.
8. Uždarykite puslapį.
9. Uždarykite puslapį.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Neatitikčių apdorojimo diagnostikos tipų apibrėžimas
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Diagnostikos tipai.
    * Naudodami puslapį Diagnozės tipai nurodykite diagnostikos veiksmų klasifikaciją. Koregavimu identifikuojama, kurio diagnostinio veiksmo turi būti imtasi, atsiradus patvirtintai neatitikčiai, kas turėtų jį atlikti bei pageidaujamą ir planuojamą baigimo datą.  
2. Spustelėkite Naujas.
3. Lauke Diagnostikos įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Uždarykite puslapį.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Neatitikčių apdorojimo kokybės išlaidų apibrėžimas
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Kokybės išlaidos.
    * Naudokite puslapį Kokybės išlaidos, kad apibrėžtumėte išlaidų, kurios bus naudojamos su neatitiktimis susijusiose operacijose, klasifikaciją.  
2. Spustelėkite Naujas.
3. Lauke Išlaidų kodas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Uždarykite puslapį.

## <a name="define-the-operations-for-nonconformance-processing"></a>Neatitikčių apdorojimo operacijų apibrėžimas
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Operacijos.
    * Norėdami nurodyti darbų, kurie gali būti atlikti atsiradus patvirtintai neatitikčiai, klasifikaciją, naudokite puslapį Operacijos. Susiję operaciją su neatitiktimi galite nurodyti informaciją apie susijusią medžiagą, darbo valandas ir papildomas išlaidas, būtinas atliekant operaciją. Šia informacija bus remiamasi skaičiuojant operacijos atlikimo numatytas išlaidas.  
2. Spustelėkite Naujas.
3. Lauke Operacija įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Uždarykite puslapį.

## <a name="define-problem-types-for-nonconformance-processing"></a>Neatitikčių apdorojimo problemų tipų apibrėžimas
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Problemų tipai.
    * Naudodami puslapį Problemų tipai apibrėžkite kokybės problemų, su kuriomis susiduriama įvairiuose neatitikimo tipuose, klasifikaciją. Neatitikčių tipai – tai Vidinis, Kliento, Tiekėjo, Aptarnavimo užklausos, Gamybos ir Sudėtinio produkto gamybos. Vieną problemos tipą galima susieti su keliais neatitikčių tipais.  
2. Spustelėkite Naujas.
3. Lauke Problemos tipas įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Neatitikčių tipai.
    * Naudokite puslapį Neatitikčių tipai, kur galite leisti priskirti problemos tipą vienam ar keliems neatitikčių tipams. Pavyzdžiui, problemos, susijusios su defekto kodu, tipas gali būti taikomas visiems neatitikimų tipams, tuo tarpu problemos, susijusios su klientų skundais, tipas gali būti taikomas tik klientų ir aptarnavimo užklausų neatitikimų tipams.  
6. Spustelėkite Naujas.
7. Sąraše pažymėkite pasirinktą eilutę.
8. Lauke Neatitikties tipas pasirinkite parinktį.
9. Uždarykite puslapį.
10. Uždarykite puslapį.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Neatitikčių apdorojimo sulaikymo zonų apibrėžimas
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės valdymas > Sulaikymo zonos.
2. Spustelėkite Naujas.
3. Lauke Sulaikymo zona įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Uždarykite puslapį.

