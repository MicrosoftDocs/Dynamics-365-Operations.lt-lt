---
title: Kaštų ir datos valdymas
description: Šioje temoje aiškinamas kaštų ir datos valdymas turto valdyme.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c09dee94891fb78c22e8cf9f203cb7f5531bb968
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6016141"
---
# <a name="cost-and-date-control"></a>Kaštų ir datos valdymas

[!include [banner](../../includes/banner.md)]

Turto valdyme galite apskaičiuoti kaštus, kad galėtumėte peržiūrėti faktinius kaštus, palygintus su turto, funkcinių vietų ir darbo užsakymų biudžeto kaštais. Faktiniai kaštai pagrįsti užregistruotomis operacijomis.

Taip galite apskaičiuoti datą, jei norite palyginti darbo užsakymų suplanuotas pradžios ir pabaigos datas su faktinėmis pradžios ir pabaigos datomis.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Turto, funkcinių vietų ir dar užsakymų kaštų valdymas

Su turtu, funkcinėmis vietomis ir darbo užsakymais susiję skaičiavimai yra beveik identiški. Vienintelis skirtumas – atliekant turto ir funkcinių vietų skaičiavimą, į skaičiavimą galite įtraukti antrinį turtą ir antrines vietas. Data yra operacijos, kai registracija buvo įrašyta, data.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto kaštų valdymas** arba **Funkcinės vietos kaštų valdymas** arba **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymo kaštų valdymas**.

2. Dialogo lange **Turto kaštų valdymas** / **Funkcinės vietos kaštų valdymas** / **Darbo užsakymo kaštų valdymas** pasirinkite skaičiuotiną laiko intervalą.

3. Jei reikia, pažymėkite finansinių matmenų rinkinį, kad jis būtų įtrauktas į skaičiavimą.

4. Perjungimo mygtuke **Praleisti nulį** pažymėkite Taip, jei nenorite, kad būtų rodomi nulinių kaštų rezultatai.

5. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti kaštų valdymo eilutėse. 

    Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra turi kelių lygių hierarchiją, visos kaštų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų.

    Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, kaštų valdymo eilutes.

6. Perjungimo mygtuke **Rodyti atvirus patvirtintus** pažymėkite Taip, jei norite į skaičiavimą įtraukti tą stulpelį.

7. Perjungimo mygtuke **Įtraukti antrinį turtą** pasirinkite Taip, kad atskirose eilutėse būtų rodomi su antriniu turtu susiję kaštai.

8. Jei norite apriboti iešką, „FastTab“ konteineryje **Įtrauktini įrašai** galite pasirinkti konkretų turtą / funkcines vietas / darbo užsakymus.

9. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

    Toliau pateiktame paveiksle rodomas dialogo langas **Turto kaštų valdymas**.

    ![Dialogo langas „Turto kaštų valdymas“](media/01-controlling-and-reporting.png)

10. Puslapyje **Turto kaštų valdymas** spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas skaičiavimo išsamumo lygis. Pažymėti mygtukai **Grupuoti pagal** yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

## <a name="example-of-calculation-results-in-asset-cost-control"></a>Turto kaštų valdymas skaičiavimo rezultatų pavyzdys

Toliau pateiktoje ekrano kopijoje rodomas **Turto kaštų valdymas** skaičiavimo rezultatų pavyzdys.

- Lauke **Originalus biudžetas** rodomi biudžeto kaštai iš darbo užsakymo prognozės. 
- Lauke **Patvirtinti kaštai** rodoma bendra išlaidų suma, kurią juridinis asmuo įsipareigojo sau sumokėti. 
- Laukuose **Atviri patvirtinti kaštai** rodomi įsipareigojimai sumokėti už elementus, valandas ir paslaugas, kurias užsakėte arba gavote, bet neapmokėjote. 
- Kai visos naudojimo registracijos užregistruotos, lauke **Faktiniai kaštai** rodomi susiję kaštai.

![„Turto kaštų valdymas“ skaičiavimo rezultatų pavyzdys](media/02-controlling-and-reporting.png)

Kitas būdas skaičiuoti kaštus – atlikti kelis pasirinkimus **Visas turtas** arba **Aktyvus turtas**. Tada skirtuke **Bendra** spustelėkite mygtuką **Kaštų valdymas**. Dialogo lange **Turto kaštų valdymas** pažymėtas turtas yra automatiškai įtraukiamas į „FastTab“ **Įtrauktini įrašai** lauką **Turtas**. Spustelėkite **Gerai** ir rodomas pasirinkto turto kaštų skaičiavimas. Tą pačią procedūrą galima atlikti su funkcinėmis vietomis dalyje **Visos funkcinės vietos** arba **Aktyvios funkcinės vietos** ir su darbo užsakymais dalyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

## <a name="work-order-date-control"></a>Darbo užsakymo datos kontrolė

Naudokite šį puslapį, kad galėtumėte peržiūrėti numatytas pradžios ir pabaigos datas, palygintas su darbo užsakymų pradžios ir pabaigos datomis.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymo datos valdymas**.

2. Spustelėkite **Skaičiuoti**.

3. Lauke **Funkcinė sritis** pažymėkite funkcinę vietą.

4. Laukuose **Pradžios data** ir **Pabaigos data** įveskite intervalą, kuriam norite atlikti skaičiavimą. Bus įtraukti visi darbo užsakymai, kurių numatoma pradžios data patenka į intervalą.

5. Spustelėkite **Gerai**.

6. Spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pažymėti mygtukai **Grupuoti pagal** yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

## <a name="example-of-calculation-results-in-work-order-date-control"></a>Darbo užsakymo datos valdymas skaičiavimo rezultatų pavyzdys

Toliau pateiktoje ekrano kopijoje rodomas rezultatų **Darbo užsakymo datos valdymas** pavyzdys.

- Lauke **Vid. pradžios delsa** rodomas dienų tarp darbo užsakymo suplanuotos pradžios datos, palygintos su faktine pradžios data, skirtumas. Jei, pavyzdžiui, faktinė pradžios data buvo dvi dienos iki suplanuotos pradžios datos, lauke bus rodoma „-2“.  
- Lauke **Vid. pabaigos delsa** rodomas dienų tarp darbo užsakymo suplanuotos pabaigos datos, palygintos su faktine pabaigos data, skirtumas. Jei, pavyzdžiui, faktinė pabaigos data buvo trys dienos iki suplanuotos pabaigos datos, lauke bus rodoma „3“.  
- Laukuose **Įvykiai** rodomas laiko nuokrypių, susijusių su darbo užsakymo suplanuota ir faktine pradžios data ir suplanuota ir faktine pradžios data, skaičius.

![„Darbo užsakymo datos valdymas“ skaičiavimo rezultatų pavyzdys](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]