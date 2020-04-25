---
title: Skaičiuoti „kanban“ kiekio pasiūlymus
description: Šios procedūros tikslas yra optimizuoti „kanban“ dydį ir kiekį pagal konkrečią „kanban“ taisyklę, naudojant „kanban“ kiekio skaičiavimą.
author: ChristianRytt
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa6a01d8f918c45aaa454e5234f80c312d7a5061
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212393"
---
# <a name="calculate-kanban-quantity-suggestions"></a>Skaičiuoti „kanban“ kiekio pasiūlymus

[!include [banner](../../includes/banner.md)]

Šios procedūros tikslas yra optimizuoti „kanban“ dydį ir kiekį pagal konkrečią „kanban“ taisyklę, naudojant „kanban“ kiekio skaičiavimą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta vertės srauto vadybininkui. Būtina, kad užbaigtumėte procedūrą „Į „kanban“ taisyklę įtraukti naują „kanban“ kiekio skaičiavimo strategiją“.


## <a name="create-a-kanban-quantity-calculation"></a>Kurti „kanban“ kiekio skaičiavimą
1. Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ kiekio skaičiavimas > Skaičiuoti „kanban“ kiekį.
2. Spustelėkite Naujas.
3. Lauke „Pavadinimas“, įveskite „Speaker2016“.
4. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite strategiją, kurią sukūrėte procedūroje „Į „kanban“ taisyklę įtraukti naują „kanban“ kiekio skaičiavimo strategiją“. Pvz., „Speaker2016“.  
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke „Taisyklės aktyvumo pradžios data“ nustatykite tokią datą ir laiką: „2012-12-17T08:00:00“.
    * Ši data naudojama kaip pagrindas nustatant, kurios fiksuotos „kanban“ taisyklės įtraukiamos į „kanban“ kiekio skaičiavimą.  
7. Lauke „Patenkinto poreikio laikotarpio pradžios data“ nustatykite tokią datą ir laiką: „2012-11-17T09:00:00“.
    * Data, nuo kurios buvusios poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.  
8. Lauke „Patenkinto poreikio laikotarpio pabaigos data“ nustatykite tokią datą ir laiką: „2012-12-17T07:59:59“.
    * Data, iki kurios buvusios poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.  
9. Lauke „Poreikio laikotarpio pradžios data“ nustatykite tokią datą ir laiką: „2012-12-17T08:00:00“.
    * Data, nuo kurios dabartinės poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.  
10. Lauke „Poreikio laikotarpio pabaigos data“ nustatykite tokią datą ir laiką: „2013-01-16T07:59:59“.
    * Data, iki kurios dabartinės poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.  

## <a name="generate-kanban-quantity-proposal"></a>Generuoti „kanban“ kiekio pasiūlymą
1. Spustelėkite Įrašyti.
2. Spustelėkite „Generuoti“.
    * Tai generuoja „kanban“ taisyklės 000020 „kanban“ kiekio pasiūlymo eilutę.  

## <a name="run-kanban-quantity-calculation"></a>Vykdyti „kanban“ kiekio skaičiavimą
1. Spustelėkite „Skaičiuoti“.
    * Tai apskaičiuoja „kanban“ kiekio pasiūlymą.  
2. Spustelėkite GERAI.
3. Sąraše pažymėkite pasirinktą eilutę.
    * Atkreipkite dėmesį, kad siūlomas „kanban“ kiekis yra 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Pakeisti produktų kiekį ir dar kartą skaičiuoti
1. Nustatykite produkto kiekio reikšmę „5“.
2. Spustelėkite „Skaičiuoti“.
3. Spustelėkite GERAI.
    * Atkreipkite dėmesį, kad, kai „kanban“ kiekis yra 5, pasiūlymas pakeičiamas į 4 „kanban“ kiekį.  
    * Tai lemia aplinkybė, kad, esant mažesniam produkto kiekiui, reikia didesnio kiekio „kanban“, kad būtų patenkintas poreikis.  

## <a name="update-kanban-rule"></a>Atnaujinti „kanban“ taisyklę
1. Lauke „Taisyklės įsigaliojimo data“ įveskite datą ir laiką.
    * Nustatykite ateities datą parinkčiai „Taisyklės aktyvumo pradžios data“. Pvz., šiandien + vieneri metai.  
2. Spustelėkite Naujinti.
3. Spustelėkite GERAI.
4. Uždarykite puslapį.

## <a name="validate-change-on-kanban-rule"></a>Patvirtinti „kanban“ taisyklės pakeitimą
1. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkti „kanban“ taisyklę, kuri buvo sukurta ankstesnėje papildomoje užduotyje. Tai turėtų būti pirmoji „kanban“ taisyklė pagal numerį surūšiuotame sąraše.  
3. Perjunkite skyriaus „Išsami informacija“ išplėtimą.
    * Atkreipkite dėmesį į įsigaliojimo datą, kuri reiškia, kad ši taisyklė iki šios datos neaktyvinama.  
4. Perjunkite skyriaus „Kiekiai“ išplėtimą.
    * Atkreipkite dėmesį, kad tai yra numatytasis kiekis, kurį įvedėte į „kanban“ kiekio skaičiavimą.  
    * Atkreipkite dėmesį, kad tai yra fiksuotas 4 „kanban“ kiekis iš „kanban“ kiekio skaičiavimo.  
5. Spustelėkite skirtuką „ListPanel“.

