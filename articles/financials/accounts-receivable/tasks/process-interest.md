---
title: Palūkanų apdorojimas
description: Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549611"
---
# <a name="process-interest"></a>Palūkanų apdorojimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas. Šioje užduotyje naudojama demonstracinė įmonė USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Nustatyti palūkanas registravimo šablone
1. Pasirinkite Kreditas ir rinkiniai > Sąranka > Klientų registravimo šablonai.
2. Spustelėkite Redaguoti.
    * Iš išplečiamojo sąrašo pasirinkite palūkanų kodą. Jei nenorite skaičiuoti operacijų palūkanų naudodami šį registravimo šabloną, palikite lauką tuščią.  
    * Naudojant skirtuką Lentelių apribojimai, galima keisti būdą, kuriuo apdorojamos palūkanos. Jei šio lauko reikšmė nustatyta kaip Taip, bus skaičiuojamos šio registravimo šablono palūkanos.  

## <a name="calculate-interest"></a>Skaičiuoti palūkanas
1. Pasirinkite Kreditas ir rinkiniai > Palūkanos > Kurti delspinigių pažymas.
    * Turite pasirinkti operacijų, kurių palūkanas skaičiuosite, tipus. Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.  
    * Jei pasirinksite Palūkanos, skaičiuosite palūkanų palūkanas. Prieš įtraukiant šias operacijas, rekomenduojama patikrinti įstatymus, kuriais reguliuojama, kaip skaičiuoti palūkanų palūkanas.  
    * Palūkanos bus skaičiuojamos nuo šios datos iki pabaigos datos. Jei nenurodysite pradžios datos, tada visos neužregistruotos delspinigių pažymos bus atšauktos, o palūkanos bus perskaičiuotos nuo operacijos datos.  
2. Įveskite delspinigių pažymos datą.
    * Galima naudoti tris registravimo šablono parinktis: Sąskaita – naudokite kiekvienos delspinigių pažymos kliento sąskaitai priskirtą registravimo šabloną.   Pasirinkti – naudokite registravimo šabloną, kurį pasirenkate lauke Registravimo šablonas.   Operacija – naudokite atskirą registravimo šabloną iš operacijų, kuriose apskaičiuotos palūkanos kiekvienai delspinigių pažymai. Operacijos, kurios neturi priskirtų registravimo šablonų, naudos registravimo šabloną, kuris nustatytas formos Gautinų sumų parametrai srityje DK ir PVM.  
    * Pasirinkite registravimo šabloną čia, jei „Naudoti registravimo šabloną iš“ pakeitėte į „Pasirinkti“.  
3. Išplėskite arba sutraukite dalį Įtrauktini įrašai.
4. Spustelėkite Filtras.
5. Lauke Kriterijai įveskite Kliento ID. Pvz., įveskite „US-001‟.
6. Spustelėkite GERAI.
7. Spustelėkite GERAI.

## <a name="print-interest-notes"></a>Spausdinti delspinigių pažymas
1. Pasirinkite Kreditas ir rinkiniai > Palūkanos > Peržiūrėti ir apdoroti delspinigių pažymas.
2. Lauke Būsena pasirinkite „Sukurta‟.
3. Lauke Išspausdinta pasirinkite „Neišspausdinta‟.
4. Spustelėkite Spausdinti.
5. Išplėskite arba sutraukite dalį Įtrauktini įrašai.
6. Spustelėkite GERAI.
7. Uždarykite puslapį.

## <a name="post-the-interest-note"></a>Registruoti delspinigių pažymą
1. Pasirinkite delspinigių pažymą, kuri paruoštas registruoti (būsena yra Sukurta).
2. Spustelėkite Registruoti.
3. Įveskite delspinigių pažymos registravimo datą.
    * Pasirinkite Taip, jei norite sukurti kiekvienos delspinigių pažymos DK operaciją.     Jei Taip nepasirinksite, prireiks vienos operacijos, norint sukaupti ir užregistruoti DK visų kliento delspinigių pažymų delspinigius.  
4. Išplėskite arba sutraukite dalį Įtrauktini įrašai.
5. Spustelėkite GERAI.
6. Lauke Būsena pasirinkite „Užregistruota‟.

