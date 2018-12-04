--- 
title: "Nustatyti pirkimo užsakymų darbo šabloną"
description: "Ši procedūra sutelkta į paprasto darbo šablono nustatymą, kuris bus naudojamas padedant gautas prekes."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Nustatyti pirkimo užsakymų darbo šabloną

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra sutelkta į paprasto darbo šablono nustatymą, kuris bus naudojamas padedant gautas prekes. Darbo šablonai nustato instrukcijų rinkinį, pateiktą sandėlio darbuotojui mobiliajame įrenginyje, perkeliant prekes iš gavimo srities. Šią procedūrą galite naudoti su demonstracinių duomenų įmonės USMF nurodytais duomenimis. Prieš paleisdami šį vadovą, sukurkite darbo telkinio ID. Šiame pavyzdyje naudojamas darbo telkinio ID, iškviestas iš Gaunama. Ši procedūra skirta sandėlio vadovui.

1. Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.
2. Lauke Darbo užsakymo tipas pasirinkite „Pirkimo užsakymai“.

## <a name="create-a-work-template-header"></a>Sukurti darbo šablono antraštę
1. Spustelėkite Naujas.
2. Lauke Sekos numeris įveskite skaičių.
    * Tai seka, pagal kurią yra vertinami darbo šablonai. Seką, jei reikia, galite modifikuoti.  
3. Lauke „Darbo šablonas“ įveskite reikšmę.
    * Tai unikalus šio šablono identifikatorius.  
4. Lauke Darbo šablonas įveskite vertę.
    * Pasirinktis Galiojantis nebus pažymėta tol, kol užpildysite visą informaciją, kuri yra reikalinga pagal šabloną, ir spustelėsite įrašyti.  
    * Pirkimo užsakymo tipo darbo užsakymo negalima automatiškai apdoroti, todėl pasirinktį Automatiškai apdoroti palikite nustatytą kaip Ne.  
5. Lauke Darbo telkinio ID įveskite vertę.
    * Darbo telkinio ID leidžia skirstyti darbą į grupes. Čia nustatyta vertė bus bet kurio darbo, sukurto naudojant šį šabloną, numatytoji vertė.  
6. Lauke Darbo prioritetas įveskite '1'.
    * Tai nurodo darbo svarbą, o čia nustatyta vertė bus kiekvieno darbo, sukurto naudojant šį šabloną, numatytoji vertė.  
7. Spustelėkite Įrašyti.
    * Pirma turite įrašyti darbo šablono antraštę, tik tada galimas mygtukas Redaguoti užklausą.  

## <a name="set-up-the-query-for-the-work-template"></a>Nustatyti darbo šablono užklausą
1. Spustelėkite Redaguoti užklausą.
    * Mes nustatysime apribojimą, pagal kurį šablonas gali būti naudojamas tik tam tikrame sandėlyje.  
2. Spustelėkite Pridėti.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Laukas įveskite 'sandėlis'.
5. Lauke Kriterijai surinkite reikšmę.
6. Spustelėkite GERAI.
7. Spustelėkite Taip.

## <a name="set-work-template-details"></a>Nustatyti darbo šablono informaciją
1. Spustelėkite Naujas.
2. Lauke Darbo tipas pasirinkite 'Paimti'.
3. Lauke Darbo klasės ID įveskite 'pirkimas'.
    * Čia nustatyta darbo klasė bus numatytoji visose paėmimo tipo darbo eilutėse, kurios sukurtos naudojant šį šabloną. Darbo klasės negalima nepaisyti darbo užsakymo eilutėse. Darbo klasės naudojamos nukreipti ir (arba) apriboti darbo tipo užsakymo eilutes, kurias sandėlio darbuotojas gali apdoroti mobiliajame įrenginyje.  
4. Spustelėkite Naujas.
5. Lauke Darbo tipas pasirinkite „Padėjimas“.
6. Lauke Darbo klasės ID surinkite reikšmę.
    * Paėmimo ir padėjimo instrukcijos yra rinkinys. Kiekvienas paėmimo / padėjimo rinkinys turi būti tos pačios darbo klasės. Naudokite tą pačią darbo klasę, kurią nurodėte paėmimo instrukcijoje.  
7. Spustelėkite Įrašyti.
    * Atkreipkite dėmesį, kad dabar žymės langelis Galiojantis yra pažymėtas.  


