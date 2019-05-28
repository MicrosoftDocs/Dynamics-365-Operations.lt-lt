---
title: Nustatyti mobiliojo įrenginio meniu elementą Pirkimo užsakymo tipo darbui atlikti
description: Šioje procedūroje nurodoma, kaip nustatyti mobiliojo įrenginio meniu elementą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 326a0039d2769ee5f459a87c302c93604d2379aa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545884"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Nustatyti mobiliojo įrenginio meniu elementą Pirkimo užsakymo tipo darbui atlikti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje nurodoma, kaip nustatyti mobiliojo įrenginio meniu elementą. Šiame pavyzdyje meniu elementas naudojamas atliekant tipo Pirkimo užsakymas darbą. Galiojantis darbas nustatomas pagal darbo klasę, kuri susieta su meniu elementu. Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Šią procedūrą paprastai atlieka sandėlio vadovas.


## <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas
1. Eikite į Mobiliojo įrenginio meniu elementai.
2. Spustelėkite Naujas.
3. Lauke Meniu elemento pavadinimas surinkite reikšmę.
    * Įveskite unikalią reikšmę. Pavyzdžiui, galite įvesti „POMove“. Įsiminkite reikšmę, nes jos reikės vėliau.  
4. Lauke Pavadinimas surinkite reikšmę.
    * Tai yra pavadinimas, kuris bus rodomas mobiliajame įrenginyje. Pavyzdžiui, galite įvesti „PO Move“.  
5. Lauke Režimas pasirinkite „Darbas“.
6. Lauke Naudoti esamą darbą pasirinkite Taip.
    * Šis mobiliojo įrenginio meniu elementas yra naudojamas esamam darbui atlikti. Todėl turite šią reikšmę nustatyti į parinktį Taip.  
    * Laukas Rodyti atsargų būseną nustato, ar turimų atsargų būsena bus rodoma sandėlio darbuotojo mobiliajame įrenginyje.  
7. Lauke Nukreipė pasirinkite 'Sistemos grupavimas'.
    * Kai ką nors pasirenkate lauke Nukreipė, šio puslapio dalyje Bendra rodomi papildomi laukai. Rodomi laukai priklauso nuo to, ką pasirinkote. Pasirinkus Sistemos grupavimas, įtraukiami du nauji laukai. Jie yra paaiškinti toliau.  
8. Lauke Sistemos grupavimas pasirinkite WorkPoolId.
    * Sandėlio darbuotojams atidarius šią meniu elementą, jie bus prašyti nuskaityti darbo telkinio ID. Visi darbo užsakymai su šiuo darbo telkinio ID ir į šį meniu elementą įtrauktų darbo klasių atviros darbo užsakymo eilutės bus perkelti darbuotojui.  
9. Lauke Sistemos grupavimo žyma įveskite vertę.
    * Šis tekstas rodomas vartotojui mobiliajame įrenginyje. Pavyzdžiui, galite įvesti Darbo telkinys.  
10. Pildydami lauke Nepaisyti numerio lentelės pasirinkite Taip.
    * Ši parinktis leidžia sandėlio darbuotojams perrašyti tikslinę numerio lentelę, kai prekės padedamos vietoje, kuri kontroliuojama pagal numerio lentelę.  
11. Lauke Grupinis atidėjimas pasirinkite Taip.
    * Jei visose darbo užsakymo padėjimo eilutėse bendrai naudojama ta pati vieta, vartotojui bus pateikta viena bendra visų eilučių padėjimo instrukcija.  
    * Audito šablono ID: darbo audito šablonas leidžia nurodyti, kad meniu elemento darbo procesas turi būti nutrauktas, kad būtų galima atlikti kitą operaciją. Pavyzdžiui, jei šis meniu elementas skirtas gaunamam darbui, audito šablone gali būti reikalaujama, kad darbuotojas tikrintų temperatūrą. Proceso pertraukimo taškas nurodomas audito šablone, tai gali būti, pavyzdžiui, darbo pradžios ar pabaigos arba jo būsenos pakeitimo taškas.  
12. Išplėskite skyrių Darbo klasės.
13. Spustelėkite Naujas.
14. Lauke Darbo klasės ID įveskite Pirkimas.
    * Darbo telkinys riboja darbą, kuriam galima naudoti meniu elementą. Šiuo atveju jis bus naudojamas atviroms darbo užsakymo eilutėms, turinčioms pirkimo darbo klasės ID.  
15. Spustelėkite Įrašyti.

## <a name="set-up-work-confirmation"></a>Nustatykite darbo patvirtinimą
1. Spustelėkite Darbo patvirtinimo nustatymas.
2. Lauke Darbo tipas pasirinkite 'Paimti'.
3. Pažymėkite žymės langelį Automatinis patvirtinimas.
    * Darbo instrukcija, kurios darbo tipas yra Paėmimas, bus patvirtinta automatiškai. Ši instrukcija nebus pateikta vartotojui.  
4. Spustelėkite Naujas.
5. Lauke Darbo tipas pasirinkite „Padėjimas“.
6. Pažymėkite žymės langelį Vietos patvirtinimas.
    * Sandėlio darbuotojas bus paprašytas atlikti patvirtinamąjį vietos nuskaitymą, kai prekė bus padėta.  
7. Spustelėkite Įrašyti.
8. Uždarykite puslapį.
9. Uždarykite puslapį.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Meniu elemento įtraukimas į mobiliojo įrenginio meniu
1. Eikite į Mobiliojo įrenginio meniu.
2. Spustelėkite Redaguoti.
3. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Pavadinimas verte 'gaunama'.
    * Norite rasti meniu, kurį galite naudoti gavimo meniu elementams. USMF tai vadinama Gaunama.  
4. Medyje pasirinkite 'vertė'.
5. Spustelėkite į dešinę pusę rodančią rodyklę.
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.

