---
title: Palūkanų apdorojimas
description: Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad30984f55017ee275af15ddb4f1a46c6a50db69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992944"
---
# <a name="process-interest"></a>Palūkanų apdorojimas

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas. Šioje užduotyje naudojama demonstracinė įmonė USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Nustatyti palūkanas registravimo šablone
1. Parinktyje **Naršymo sritis** eikite į **Moduliai > Kreditas ir mokesčių rinkimas > Sąranka > Kliento registravimo šablonai**.
2. Spustelėkite **Redaguoti**.
3. Parinktyje **Sąrankos „fastTab“**, lauke **Palūkanų kodas** išplečiamajame sąraše pasirinkite delspinigių kodą. Jei nenorite skaičiuoti operacijų palūkanų naudodami šį registravimo šabloną, palikite lauką tuščią. „FastTab“ **Lentelės apribojimai** leidžia jums keisti, kaip palūkanos apdorojamos. Jei šio lauko reikšmė nustatyta kaip Taip, bus skaičiuojamos šio registravimo šablono palūkanos.  

## <a name="calculate-interest"></a>Skaičiuoti palūkanas
1. Skiltyje **Naršymo sritis** eikite į **Moduliai > Kreditas ir mokesčių rinkimas > Palūkanos > Kurti delspinigių pažymas**.
2. Turite pasirinkti operacijų, kurių palūkanas skaičiuosite, tipus. Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.  
3. Jei nustatysite skiltyje **Palūkanos** reikšmę Taip, bus skaičiuojami palūkanų delspinigiai. Prieš įtraukiant šias operacijas, rekomenduojama patikrinti įstatymus, kuriais reguliuojama, kaip skaičiuoti palūkanų palūkanas.  
4. Lauke **Nuo datos** įveskite datą, nuo kurios bus pradėtos skaičiuoti palūkanos. Jei nenurodysite skiltyje **Nuo datos** reikšmę, tada visos neįregistruotos delspinigių pažymos bus atšauktos ir palūkanos bus perskaičiuojamos nuo operacijos datos.
5. Lauke **Iki datos** įveskite datą, iki kurios palūkanos bus skaičiuojamos.
6. Lauke **Naudoti registravimo šabloną iš** pasirinkite parinktį. Yra trys registravimo šablonų parinktys:
    - Sąskaita – naudokite registravimo šabloną, priskirtą kliento sąskaitai, kiekvienai delspinigių pažymai. 
    - Pasirinkti – naudokite registravimo šabloną, kurį pasirenkate lauke Registravimo šablonas.
    - Operacija – naudokite atskirą registravimo šabloną iš operacijų, kuriose apskaičiuotos palūkanos kiekvienai delspinigių pažymai. Operacijos, kurios neturi priskirtų registravimo šablonų, naudos registravimo šabloną, kuris nustatytas formos Gautinų sumų parametrai srityje DK ir PVM.  
7. Išplėskite „fastTab“ **Įtrauktini įrašai**.
8. Spustelėkite **Filtras**.
9. Lauke **Kriterijai** įveskite Kliento ID. Pvz., įveskite „US-001‟.
6. Spustelėkite **Gerai**.
7. Spustelėkite **Gerai**.

## <a name="print-interest-notes"></a>Spausdinti delspinigių pažymas
1. Skiltyje **Naršymo sritis** eikite į **Moduliai > Kreditas ir Mokesčių rinkimas > Palūkanos > Peržiūrėti ir apdoroti delspinigių pažymas**.
2. Lauke **Būsena** pasirinkite „Sukurta“.
3. Lauke **Išspausdinta** pasirinkite „Neišspausdinta“.
4. Spustelėkite **Spausdinti**.
5. Išplėskite „fastTab“ **Įtrauktini įrašai**.
6. Spustelėkite **Gerai**.
7. Uždarykite puslapį.

## <a name="post-the-interest-note"></a>Registruoti delspinigių pažymą
1. Pasirinkite delspinigių pažymą, kuri paruoštas registruoti (būsena yra Sukurta).
2. Spustelėkite **Registruoti.**
3. Įveskite delspinigių pažymos registravimo datą. Pasirinkite Taip, jei norite sukurti kiekvienos delspinigių pažymos DK operaciją. Jei Taip nepasirinksite, prireiks vienos operacijos, norint sukaupti ir užregistruoti DK visų kliento delspinigių pažymų delspinigius.  
4. Išplėskite „fastTab“ **Įtrauktini įrašai**.
5. Spustelėkite **Gerai**.
6. Lauke **Būsena** pasirinkite „Įregistruota“.

