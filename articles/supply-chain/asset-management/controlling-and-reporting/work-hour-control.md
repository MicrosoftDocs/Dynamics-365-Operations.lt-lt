---
title: Darbo valandų valdymas
description: Šiame straipsnyje paaiškinama turto valdymo darbo valandų kontrolė.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f5f5dbb23c4d6c86bee7612c4ade65ef4b1cee8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869755"
---
# <a name="work-hour-control"></a>Darbo valandų valdymas

[!include [banner](../../includes/banner.md)]

 

Modulyje Turto valdymas galite apskaičiuoti valandas, kad galėtumėte apžvelgti faktines valandas, palygintas su turto, funkcinių vietų ar darbo užsakymų biudžeto valandomis. Faktinės valandos yra pagrįstos užregistruotomis operacijomis.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Turto, funkcinių vietų ir darbo užsakymų darbo valandų valdymas

Su turtu, funkcinėmis vietomis ir darbo užsakymais susiję skaičiavimai yra beveik identiški. Vienintelis skirtumas – skaičiuodami turto ir funkcinių vietų valandas, galite įtraukti antrinį turtą ir antrines vietas. Data yra operacijos, kai registracija buvo įrašyta, data.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto valandų valdymas** arba **Funkcinių vietų valandų valdymas** arba **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymų valandų valdymas**.

2. Dialogo lange **Turto valandų valdymas**.

3. Dialogo lango **Turto valandų valdymas** / **Funkcinių vietų valandų valdymas** / **Darbo užsakymų valandų valdymas** laukuose **Pradžios data** ir **Pabaigos data** pasirinkite skaičiuotiną laikotarpį.

4. Jei reikia, pasirinkite, kad skaičiuojant būtų įtrauktas **finansinių dimensijų rinkinys**.

5. Perjungimo mygtuke **Praleisti nulį** pasirinkite Taip, jei nenorite, kad būtų rodomi nulinių valandų rezultatai.

6. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti valandų valdymo eilutėse. 

    Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinių vietų hierarchija yra kelių lygių, visos valandų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršutiniame lygyje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje esančių funkcinių vietų. 
    
    Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, valandų valdymo eilutes.

7. Perjungimo mygtuke **Įtraukti antrinį turtą** pasirinkite Taip, kad atskirose eilutėse būtų rodomi su antriniu turtu susiję kaštai.

8. Jei norite apriboti iešką, „FastTab“ konteineryje **Įtrauktini įrašai** galite pasirinkti konkretų turtą / funkcines vietas / darbo užsakymus.

9. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

10. Puslapyje **Turto valandų valdymas** spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas skaičiavimo išsamumo lygis. Pažymėti mygtukai **Grupuoti pagal** yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

## <a name="example"></a>Pavyzdys

Toliau pateiktoje ekrano kopijoje rodomas **Turto valandų valdymas** skaičiavimo pavyzdys.

- Lauke **Pradinis biudžetas** rodomos biudžeto valandos iš darbo užsakymo prognozės. 
- Lauke **Faktinės valandos** rodomos darbo užsakymuose užregistruotos valandos. 
- Lauke **Skirtos valandos** rodomos visos valandos, kurias jūsų įmonė skyrė pagal darbo užsakymus.

![Turto valandų valdymo skaičiavimo pavyzdys.](media/04-controlling-and-reporting.png)

Kitas būdas skaičiuoti valandas – atlikti kelis pasirinkimus srityse **Visas turtas** arba **Aktyvus turtas**. Tada spustelėkite mygtuką **Valandų valdymas**, esantį „FastTab“ **Bendra**. Pasirinktas turtas automatiškai įterpiamas į „FastTab“ **Įtrauktini įrašai** lauką **Turtas**. Dialogo lange **Turto valandų valdymas** spustelėkite **Gerai** – bus rodomas pasirinkto turto skaičiavimas. Tą pačią procedūrą galima atlikti su funkcinėmis vietomis dalyje **Visos funkcinės vietos** arba **Aktyvios funkcinės vietos** ir su darbo užsakymais dalyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]