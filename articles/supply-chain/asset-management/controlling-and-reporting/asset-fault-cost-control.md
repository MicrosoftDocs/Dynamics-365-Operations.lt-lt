---
title: Turto gedimų išlaidų kontrolė
description: Šioje temoje aiškinamas turto gedimo kaštų valdymas turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c34180ad99db29147587bb002aaa6badc918717
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652246"
---
# <a name="asset-fault-cost-control"></a>Turto gedimų išlaidų kontrolė

[!include [banner](../../includes/banner.md)]

 

Turto valdyme galite apskaičiuoti turto gedimo registracijų kaštus, kad peržiūrėtumėte faktinius kaštus, palygintus su biudžeto kaštais. Faktiniai kaštai pagrįsti užregistruotomis operacijomis. Data yra gedimo data, kada įrašytas požymis.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimo kaštų valdymas**.

2. Dialoge lange **Turto gedimo kaštų valdymas** pažymėkite finansinių matmenų rinkinį, kad jis būtų įtrauktas į skaičiavimą, jei reikia.

4. Perjungimo mygtuke **Praleisti nulį** pažymėkite Taip, jei nenorite, kad būtų rodomi nulinių kaštų rezultatai.

5. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti kaštų valdymo eilutėse. 

    Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos turto gedimo kaštų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. 
    
    Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, turto gedimo kaštų valdymo eilutes.

6. Jei norite apriboti iešką, „FastTab“ **Įtrauktini įrašai** galite pažymėti konkretų turtą, gedimų datas ir gedimo priežastis.

7. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

8. Spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pažymėti mygtukai **Grupuoti pagal** yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

## <a name="example"></a>Pavyzdys

Šis pavyzdyje parodytas turto gedimo kaštų valdymo skaičiavimas.

- Lauke **Originalus biudžetas** rodomi biudžeto kaštai iš darbo užsakymo prognozės. 
- Lauke **Faktiniai kaštai** rodomi darbo užsakymuose užregistruoti kaštai. 
- Lauke **Skirti kaštai** rodomi bendri kaštai, kuriuos jūsų įmonė skyrė pagal darbo užsakymus.

    ![1 pav.](media/05-controlling-and-reporting.png)

Informacijos, kaip nustatyti gedimus, žr. temoje [Gedimų valdymas](../setup-for-work-orders/fault-management.md).
