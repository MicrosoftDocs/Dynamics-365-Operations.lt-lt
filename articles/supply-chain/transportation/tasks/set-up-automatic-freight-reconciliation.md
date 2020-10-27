---
title: Automatinio transportavimo derinimo nustatymas
description: Šioje procedūroje parodoma, kaip nustatyti automatinio transportavimo derinimo duomenis.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f11edc15821faad84485d5b81e4a9ded0b7e974
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985298"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Automatinio transportavimo derinimo nustatymas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip nustatyti automatinio transportavimo derinimo duomenis. Tai paprastai atlieka sandėlio vadovas. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.


## <a name="set-up-the-freight-bill-type"></a>Transportavimo sąskaitos tipo nustatymas
1. Eikite į Transportavimo valdymas > Sąranka > Transportavimo mokesčių derinimas > Transportavimo sąskaitos tipas.
    * Transportavimo sąskaitos tipas apibrėžia, kaip transportavimo sąskaita ir vežėjo SF turi būti derinamos.  
2. Spustelėkite Naujas.
3. Lauke Transportavimo sąskaitos tipas įveskite reikšmę.
4. Lauke Mechanizmo rinkinys įveskite Microsoft.Dynamics.Ax.Tms.dll.
    * Tai yra standartinė transportavimo valdymo gretinimo mechanizmo kodų biblioteka.  
5. Lauke Mechanizmo klasė įveskite Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.
    * Tai yra standartinė transportavimo valdymo gretinimo mechanizmo klasė.  
6. Spustelėkite Naujas.
7. Lauke Aprašas pasirinkite reikšmę, kuri turėtų atitikti transportavimo sąskaitos ir vežėjo SF reikšmes.  
8. Lauke Būtina gretinti pasirinkite Taip.
    * Jei nustatote šio lauko reikšmę Taip, lauke Aprašas pasirinkta reikšmė turi sutapti tiek transportavimo sąskaitoje, tiek vežėjo SF. Jei nustatysite parinktį Ne, vienoje iš šių sąskaitų laukas gali būti tuščias.  
9. Spustelėkite Įrašyti.

## <a name="set-up-the-freight-bill-type-assignment"></a>Transportavimo sąskaitos tipo priskyrimo nustatymas
1. Uždarykite puslapį.
2. Eikite į Transportavimo valdymas > Sąranka > Transportavimo mokesčių derinimas > Transportavimo sąskaitos tipo priskyrimai.
    * Transportavimo sąskaitos tipo priskyrimas naudojamas norint nurodyti, kuris transportavimo sąskaitos tipas naudojamas konkrečiam vežėjui.   
3. Spustelėkite Naujas.
4. Lauke Režimas įveskite arba pasirinkite reikšmę.
5. Lauke Siuntos vežėjas įveskite arba pasirinkite reikšmę.
6. Lauke Transportavimo sąskaitos tipas pasirinkite transportavimo sąskaitos tipą, kurį sukūrėte anksčiau.
7. Uždarykite puslapį.

## <a name="set-up-the-audit-master"></a>Pagrindinio audito nustatymas
1. Eikite į Transportavimo valdymas > Sąranka > Transportavimo mokesčių derinimas > Pagrindinis auditas.
    * Pagrindinis auditas nurodo automatinio transportavimo derinimo nuokrypio ribas. Jis nurodo sumą, kuria transportavimo sąskaitos ir vežėjo SF piniginės sumos gali skirtis, kad vis tiek būtų galima derinti. Jis taip pat apibrėžia, kaip tvarkyti nesutapimus.  
2. Spustelėkite Naujas.
3. Lauke Pagrindinio audito ID įveskite reikšmę.
4. Lauke Siuntos vežėjas pasirinkite tą patį siuntos vežėją, kurį pasirinkote anksčiau.
5. Lauke Transportavimo sąskaitos tipas pasirinkite transportavimo sąskaitos tipą, kurį sukūrėte anksčiau.
6. Išplėskite Nuokrypis skyrių.
7. Lauke Mažiausias leistinas nuokrypio lygis įveskite skaičių.
8. Lauke Didžiausias leistinas nuokrypio lygis įveskite skaičių.
9. Išplėskite skyrių Rezultatas.
10. Lauke Permokėjimo priežasties įveskite arba pasirinkite reikšmę.
    * Jei piniginė suma transportavimo sąskaitoje ir vežėjo SF skiriasi, permokėjimo ir neprimokėjimo priežasties kodai nurodo sąskaitas, kuriose skirtumas turi būti užregistruotas, jei skirtumas neviršija leistinų lygių.  
11. Lauke Neprimokėjimo priežasties įveskite arba pasirinkite reikšmę.
12. Uždarykite puslapį.

