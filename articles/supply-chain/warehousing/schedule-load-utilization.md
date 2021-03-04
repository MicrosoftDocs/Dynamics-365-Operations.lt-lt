---
title: Planuoti apkrovos efektyvumą
description: Šioje temoje paaiškinama, kaip nustatyti ir planuoti sandėlio apkrovą.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433384"
---
# <a name="schedule-load-utilization"></a>Planuoti apkrovos efektyvumą

[!include[banner](../includes/banner.md)]

Galite suplanuoti pasirinktų tipų vietų apkrovos efektyvumą, taip pat numatyti esamą bei būsimą apkrovos efektyvumą. Galite numatyti apkrovą vienoje ar keliose vietose, pagal zonos ar sandėlio arba pagal zonos ir sandėlio derinio apkrovos vienetus.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Planuokite ir peržiūrėkite sandėlio arba vietos apkrovą

Norėdami planuoti vietų, sandėlių arba zonų apkrovą, sukuriate erdvės naudojimo sąranką ir susiejate ją su bendruoju planu.

Vietos naudojimo sąrankoje pasinaudodami vietos tipais, pavyzdžiui, **Buferinė vieta** ir **Paėmimo vieta**, galite nurodyti, kaip turi būti numatomas vietos naudojimas. Taip pat nurodote sandėliavimo apkrovos režimą, pvz., **Zona**.

Būsimo erdvės naudojimo projekcija grindžiama informacija, apskaičiuota susijusiame bendrajame plane. Bendruosiuose planuose prognozuojamas išteklių planavimas gaunamiems ir siunčiamiems gamybos ir operacijų užsakymams. Laisvos erdvės projekcija grindžiama ryšiu tarp erdvės naudojimo sąrankos ir pasirinkto bendrojo plano.

Naudodamiesi sandėliavimo apkrovos režimu, kurį pasirinkote erdvės naudojimo sąrankoje, galite nurodyti, ar reikia numatyti kiekvieno sandėlio arba zonos apkrovą, arba ar projekcijos turi apimti informaciją ir apie sandėlius, ir apie zonas. Taip pat nurodote, ar skaičiuojant apkrovos efektyvumą reikia pašalinti užblokuotas vietas.

Sukurdami ataskaitą **Sandėlio apkrovos efektyvumas** galite numatyti vietos naudojimą. Kurdami šią ataskaitą, galite nurodyti, ar reikia planuoti kiekvienos vietos, ar kelių vietų, ar pasirinkto apkrovos vieneto, pvz., zonos ar sandėlio apkrovos efektyvumą.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Kurkite erdvės naudojimo sąranką sandėliui

1. Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Sandėlio stebėjimas** \> **Vietos naudojimas**.
2. Norėdami kurti vietos naudojimo sąranką, pasirinkite **Nauja**. Nurodykite naujos sąrankos ID ir pavadinimą.
3. Lauke **Sandėliavimo apkrovos režimas** pasirinkite, ar erdvės naudojimo apžvalgoje turi būti rodoma informacija pagal sandėlį, zoną arba sandėlį ir zoną.
4. Nustatykite parinkties **Neįtraukti užblokuotų vietų** reikšmę **Taip**, kad užblokuotos atsargų vietos nebūtų įtraukiamos skaičiuojant laisvą vietą. Galite blokuoti įvesties ir išvesties atsargų vietą, puslapio **Atsargų vietos** „FastTab“ elemento **Kita** lauke **Įvestis užblokuota** arba **Išvestis užblokuota** nurodydami vietos blokavimo priežastį.
5. „FastTab“ skirtuke **Vietos tipas** pasirinkite, kokių tipų vietas reikia įtraukti į vietos naudojimo skaičiavimą. Turite pasirinkti bent vieną vietos tipą projekcijai.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Susiekite erdvės naudojimo sąranką su bendruoju planu

1. Pasirinkite **Atsargų valdymas** \> **Periodinės užduotys** \> **Apkrovos efektyvumo planavimas**.
2. Lauke **Bendrasis planas** pasirinkite bendrąjį planą.
3. Lauke **Dienų skaičius** nurodykite, kiek dienų reikia įtraukti į dabartinių ir būsimų darbo krūvių projekciją.
4. Lauke **Vietos naudojimas** pasirinkite erdvės naudojimo sąranką, kurią naudosite dabartinių ir būsimų darbo krūvių projekcijoje.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Nurodykite apkrovos naudojimo projekciją ir peržiūrėkite informaciją

1. Pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Fizinės atsargų ataskaitos** \> **Sandėlio apkrovos efektyvumas**.
2. Lauke **Rodoma pagal** pasirinkite erdvės naudojimo projekcijos lygį.

    - **Vieta** – numatykite kiekvienos vietos erdvės naudojimą. Ši projekcija naudinga, jei, pvz., norite peržiūrėti visus vietos sandėlius, kad galėtumėte subalansuoti erdvės naudojimą keliuose sandėliuose.
    - **Apkrovos vienetas** – numatykite zonų arba sandėlių erdvės naudojimą. Laisva vieta tada numatoma pagal sukūrus vietos efektyvumo sąranką puslapio **Vietos naudojimas** lauke **Sandėliavimo apkrovos režimas** pasirinktą reikšmę.

3. Priklausomai nuo ankstesniame veiksme pasirinktos reikšmės, atlikite vieną iš toliau nurodytų veiksmų.

    - Jei lauke **Rodyti pagal** pasirinkote **Vieta**, rodomas laukas **Vieta**. Pasirinkite vieną ar kelias vietas, kurias norite įtraukti į projekciją.
    - Jei lauke **Rodyti pagal** pasirinkote **Apkrovos vienetas**, rodomas laukas **Apkrovos vienetas**. Pasirinkite apkrovos vienetą.

4. Lauke **Apkrovos tipas** pasirinkę **Tūris** arba **Svoris** nurodykite sandėlio valdymo vienetą, kurio erdvę numatysite.
5. Lauke **Vietos naudojimo sąranka** pasirinkite vietos naudojimo sąranką, kuria bus grindžiama projekcija.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]