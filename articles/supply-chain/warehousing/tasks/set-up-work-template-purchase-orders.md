---
title: Pirkimo užsakymų darbo šablono nustatymas
description: Šioje temoje aprašyta, kaip nustatyti paprastą darbo šabloną, kuris bus naudojamas atidedant gautas prekes.
author: Mirzaab
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32dbdd8243c6b37cfe0c42d2e7b06adfa32a947a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572294"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Pirkimo užsakymų darbo šablono nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašyta, kaip nustatyti paprastą darbo šabloną, kuris bus naudojamas atidedant gautas prekes. Darbo šablonai nustato instrukcijų rinkinį, pateiktą sandėlio darbuotojui mobiliajame įrenginyje, perkeliant prekes iš gavimo srities. Šią procedūrą galite naudoti su demonstracinių duomenų įmonės USMF nurodytais duomenimis. Prieš paleisdami šį vadovą, sukurkite darbo telkinio ID. Šiame pavyzdyje naudojamas darbo telkinio ID, iškviestas iš Gaunama. Ši procedūra skirta sandėlio vadovui.

1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Darbas > Darbo šablonai**.
2. Lauke **Darbo užsakymo tipas** pasirinkite **Pirkimo užsakymai**.

## <a name="create-a-work-template-header"></a>Sukurti darbo šablono antraštę
1. Pasirinkite **Naujas**.
2. Lauke **Sekos skaičius** įveskite skaičių. Tai seka, pagal kurią yra vertinami darbo šablonai. Seką, jei reikia, galite modifikuoti.  
3. Lauke **Darbo šablonas** įveskite reikšmę. Tai unikalus šio šablono identifikatorius.  
4. Lauke **Darbo šablono aprašas** įveskite reikšmę.
    - Jei neužpildysite visos informacijos, reikalingos šablonui, ir nepasirinksite **Įrašyti**, parinktis **Galioja** nebus tikrinama.  
    - Darbo užsakymo, kurio tipas yra **Pirkimo užsakymas**, automatiškai apdoroti negalima, todėl palikite parinkties **Apdoroti automatiškai** nuostatą **Ne**.  
5. Lauke **Darbo telkinio ID** įveskite reikšmę. Darbo telkinio ID leidžia skirstyti darbą į grupes. Čia nustatyta reikšmė bus numatytoji kiekvieno darbo, sukurto naudojant šį šabloną, reikšmė.  
6. Lauke **Darbo prioritetas** įveskite `1`. Tai nurodo darbo svarbą, o čia nustatyta vertė bus kiekvieno darbo, sukurto naudojant šį šabloną, numatytoji vertė.  
7. Pasirinkite **Įrašyti**. Reikia įrašyti darbo šablono antraštę, kad mygtukas **Redaguoti užklausą** taptų pasiekiamas.  

## <a name="set-up-the-query-for-the-work-template"></a>Nustatyti darbo šablono užklausą
1. Pasirinkite **Redaguoti užklausą**. Nustatysime apribojimą, kad šabloną būtų galima naudoti tik konkrečiame sandėlyje.  
2. Pasirinkite **Įtraukti**.
3. Naujos eilutės lauke **Laukas** įveskite `warehouse`.
4. Lauke **Kriterijai** įveskite reikšmę.
5. Pasirinkite **Gerai**.
6. Pasirinkite **Taip**.

## <a name="set-work-template-details"></a>Nustatyti darbo šablono informaciją
1. Pasirinkite **Naujas**.
2. Lauke **Darbo tipas** pasirinkite **Pasirinkti**.
3. Lauke **Darbo klasės ID** įrašykite `purchase`. Čia nustatyta darbo klasė bus numatytoji visose paėmimo tipo darbo eilutėse, kurios sukurtos naudojant šį šabloną. Darbo klasės negalima nepaisyti darbo užsakymo eilutėse. Darbo klasės naudojamos nukreipti ir (arba) apriboti darbo tipo užsakymo eilutes, kurias sandėlio darbuotojas gali apdoroti mobiliajame įrenginyje.  
4. Pasirinkite **Naujas**.
5. Lauke **Darbo tipas** pasirinkite **Padėjimas**.
6. Lauke **Darbo klasės ID** įveskite reikšmę. Paėmimo ir padėjimo instrukcijos yra rinkinys. Kiekvienas paėmimo / padėjimo rinkinys turi būti tos pačios darbo klasės. Naudokite tą pačią darbo klasę, kurią nurodėte paėmimo instrukcijoje.  
7. Pasirinkite **Įrašyti**. Atkreipkite dėmesį, kad žymimasis langelis **Galioja** dabar yra pažymėtas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]