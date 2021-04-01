---
title: Priežiūros būsena
description: Šioje temoje aprašoma, kaip skaičiuoti priežiūros būseną skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f65bfc7b5ef9651853a12bab2ed83dbb8562ba6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253739"
---
# <a name="maintenance-status"></a>Priežiūros būsena

[!include [banner](../../includes/banner.md)]

 

Skiltyje Turto valdymas galite vykdyti skaičiavimus, norėdami matyti nurodyto laikotarpio naujų, aktyvių ir baigtų priežiūros užklausų, darbo užsakymų ir prižiūrimo turto prastovos veiklų apžvalgą. Tai pat galite matyti nurodyto laikotarpio baigtų sąlygų įvertinimų skaičių. Naudokite šį skaičiavimą peržiūrėti darbo krūvį, susijusį su gautinomis ir baigtomis priežiūros užklausomis ir darbo užsakymais.

## <a name="make-a-maintenance-status-calculation"></a>Vykdykite priežiūros būsenos skaičiavimą

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Priežiūros būsena**.

2. Dialogo lange **Apskaičiuoti būseną** pasirinkite laiko intervalą, pagal kurį norite atlikti skaičiavimą, laukuose **Nuo datos** ir **Iki datos**.

3. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti priežiūros eilutėse. 

  Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl būseną į eilutę galėsite įtraukti iš žemiau esančių funkcinių vietų. 
  
  Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, priežiūros eilutes.

4. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

5. Spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pažymėti mygtukai **Grupuoti pagal** yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

6. Nepamirškite spustelėti mygtuko **Naujinti**, kad skaičiavimai kiekvienąkart atsinaujintų, kai atliksite keitimus suaktyvindami arba išjungdami mygtukus **Grupuoti pagal** arba atlikdami naujo laikotarpio skaičiavimą.

7. Spustelėkite **Būsena**, jei norite sukurti naują priežiūros būsenos skaičiavimą.

>[!NOTE]
>Skiltyje **Priežiūros būsena** rezultatai formuojami tik iš priežiūros užklausų ir darbo užsakymų, kurie turi faktinius pradžios datą ir laiką. Pabaigos data ir laikas gali būti tušti.

## <a name="example-1"></a>1 pavyzdys

Toliau pateiktoje ekrano kopijoje yra suaktyvinti mygtukai **Metai** ir **Mėnuo**. Pasirinkę šias **Grupuoti pagal** parinktis, galite matyti bendrą mėnesinę darbo krūvio ir našumo, susijusio su priežiūros užklausomis ir darbo užsakymais, apžvalgą. 

![Mėnesinio darbo krūvio pavyzdys](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>2 pavyzdys

Toliau pateiktoje ekrino kopijoje buvo įterpta informacija apie funkcines vietas. Dabar galite palyginti darbo krūvį ir našumą funkcinėse vietose, kuriose gali nurodyti geografines vietas, gamyklas arba darbo vietas. 

![Mėnesinio darbo krūvio su funkcinėmis vietomis pavyzdys](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]