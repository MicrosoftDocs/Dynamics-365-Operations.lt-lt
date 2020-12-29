---
title: Nustatyti mobiliojo įrenginio meniu elementą Pirkimo užsakymo tipo darbui atlikti
description: Šioje temoje aprašyta, kaip nustatyti mobiliojo įrenginio meniu elementą.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86ccc39cb243354db337a5747701e9731c5ad775
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433805"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Nustatyti mobiliojo įrenginio meniu elementą Pirkimo užsakymo tipo darbui atlikti

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašyta, kaip nustatyti mobiliojo įrenginio meniu elementą. Šiame pavyzdyje meniu elementas naudojamas atliekant tipo Pirkimo užsakymas darbą. Darbo klasė, susieta su meniu elementu, nustato, kuris darbas yra galiojantis. Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Šią procedūrą paprastai atlieka sandėlio vadovas.


## <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas
1. Ieškos juostoje įveskite **Mobiliojo įrenginio meniu elementai** ir eikite į šią sritį.
2. Pasirinkite **Naujas**.
3. Lauke **Meniu elemento pavadinimas** įveskite reikšmę. Įveskite unikalią reikšmę. Pavyzdžiui, galite įvesti `POMove`. Įsiminkite reikšmę, nes jos reikės vėliau.  
4. Lauke **Pavadinimas** įveskite reikšmę. Tai yra pavadinimas, kuris bus rodomas mobiliajame įrenginyje. Pavyzdžiui, galite įvesti `PO Move`.  
5. Lauke **Režimas** pasirinkite **Darbas**.
6. Pasirinkite **Taip** lauke **Naudoti esamą darbą**.
    - Šis mobiliojo įrenginio meniu elementas yra naudojamas esamam darbui atlikti. Todėl šią reikšmę turite nustatyti kaip **Taip**.  
    - Laukas **Rodyti atsargų būseną** nustato, ar sandėlio darbuotojui mobiliajame įrenginyje bus rodoma turimų atsargų būsena.  
7. Lauke **Nurodyta pagal** pasirinkite **Sistemos grupavimas**. Lauke **Nurodyta pagal** pasirinkus kokią nors reikšmę, šio puslapio skyriuje **Bendra** bus rodomi papildomi laukai. Rodomi laukai priklauso nuo to, ką pasirinkote. Pasirinkus **Sistemos grupavimas** bus įtraukti du nauji laukai. Jie yra paaiškinti toliau.  
8. Lauke **Sistemos grupavimas** pasirinkite **Darbo telkinio ID**. Kai sandėlio darbuotojai atidarys šį meniu elementą, jų bus paprašyta nuskaityti darbo telkinio ID. Visi darbo užsakymai su šiuo darbo telkinio ID ir į šį meniu elementą įtrauktų darbo klasių atviros darbo užsakymo eilutės bus perkelti darbuotojui.  
9. Lauke **Sistemos grupavimo žyma** įveskite reikšmę. Šis tekstas rodomas vartotojui mobiliajame įrenginyje. Pavyzdžiui, galite įvesti **Darbo telkinys**.  
10. Lauke **Perrašyti numerio lentelę padedant** pasirinkite **Taip**. Ši parinktis leidžia sandėlio darbuotojams perrašyti tikslinę numerio lentelę, kai prekės padedamos vietoje, kuri kontroliuojama pagal numerio lentelę.  
11. Lauke **Grupinis atidėjimas** pasirinkite **Taip**.
    - Jei visose darbo užsakymo padėjimo eilutėse bendrai naudojama ta pati vieta, vartotojui bus pateikta viena bendra visų eilučių padėjimo instrukcija. 
    - Audito šablono ID: darbo audito šablonas leidžia nurodyti, kad meniu elemento darbo procesas turi būti nutrauktas, kad būtų galima atlikti kitą operaciją. Pavyzdžiui, jei šis meniu elementas skirtas gaunamam darbui, audito šablone gali būti reikalaujama, kad darbuotojas tikrintų temperatūrą. Proceso pertraukimo taškas nurodomas audito šablone, tai gali būti, pavyzdžiui, darbo pradžios ar pabaigos arba jo būsenos pakeitimo taškas.  
12. Išplėskite sekciją **Darbo klasės**.
13. Pasirinkite **Naujas**.
14. Lauke **Darbo klasės ID** įrašykite `Purchase`. Darbo telkinys riboja darbą, kuriam galima naudoti meniu elementą. Šiuo atveju jis bus naudojamas atviroms darbo užsakymo eilutėms, turinčioms pirkimo darbo klasės ID.  
15. Pasirinkite **Įrašyti**.

## <a name="set-up-work-confirmation"></a>Nustatykite darbo patvirtinimą
1. Pasirinkite **Darbo patvirtinimo sąranka**.
2. Lauke **Darbo tipas** pasirinkite **Pasirinkti**.
3. Pažymėkite žymės langelį **Automatinis patvirtinimas**. Darbo instrukcija, kurios darbo tipas yra Paėmimas, bus patvirtinta automatiškai. Ši instrukcija nebus pateikta vartotojui.  
4. Pasirinkite **Naujas**.
5. Lauke **Darbo tipas** pasirinkite „Padėjimas“.
6. Pažymėkite žymės langelį **Vietos patvirtinimas**. Sandėlio darbuotojas bus paprašytas atlikti patvirtinamąjį vietos nuskaitymą, kai prekė bus padėta.  
7. Pasirinkite **Įrašyti**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Meniu elemento įtraukimas į mobiliojo įrenginio meniu
1. Ieškos juostoje įveskite **Mobiliojo įrenginio meniu** ir eikite į šią sritį.
2. Pasirinkite **Redaguoti**.
3. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pavyzdžiui, filtruokite lauką **Pavadinimas** pagal reikšmę **gavimas**. Norite rasti meniu, kurį galite naudoti gavimo meniu elementams. Įmonėje USMF jis pavadintas **Gavimas**.  
4. Medyje pasirinkite **reikšmę**.
5. Pasirinkite rodyklę, kuri rodo į dešinę.
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.
