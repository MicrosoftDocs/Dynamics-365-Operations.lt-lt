---
title: DK paskirstymo taisyklės
description: Šiame straipsnyje pateikiama informacija apie didžiosios knygos paskirstymo taisykles. Jame aprašomi įvairūs šių paskirstymo taisyklių komponentai ir galimi naudoti jų paskirstymo metodai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abbeb1bb4481139dff902916362a479f94fb96e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559391"
---
# <a name="ledger-allocation-rules"></a>DK paskirstymo taisyklės

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie didžiosios knygos paskirstymo taisykles. Jame aprašomi įvairūs šių paskirstymo taisyklių komponentai ir galimi naudoti jų paskirstymo metodai.

DK paskirstymo taisyklės naudojamos norint automatiškai apskaičiuoti ir generuoti paskirstymo žurnalus ir sąskaitos įrašus, kad būtų paskirstyti DK balansai arba fiksuotos sumos. Paskirstymo metodai gali būti kintantys arba fiksuoti. DK paskirstymo taisyklėms galima naudoti toliau nurodytus paskirstymo metodus.

-   **Pagrindas** – šis kintantis metodas naudojamas, kai paskirstymas priklauso nuo faktinio DK balanso, atsižvelgiant į filtro kriterijus. Pavyzdžiui, reklamos išlaidas galima paskirstyti remiantis kiekvieno departamento pardavimais, proporcingais viso departamento pardavimams.
-   **Fiksuotas procentas** ir **Fiksuota dalis** – naudojant šiuos metodus, paskirstymo procentas arba dalis nustatoma tiesiogiai taisyklei. Pvz., reklamos išlaidas galima paskirstyti taip, kad A padalinys gautų 70 procentų, o B padalinys gautų 30 procentų reklamos išlaidų.
-   **Tolygiai** – naudojant šį metodą suma tolygiai paskirstoma kiekvienoje nurodytoje paskirties vietoje. Pvz., jei nurodytos A ir B padalinių paskirties vietos, reklamos išlaidas galima paskirstyti taip, kad A ir B padaliniai gautų po 50 procentų reklamos išlaidų.

Jei Pagrindas naudojamas kaip paskirstymo taisyklės paskirstymo metodas, taip pat privalote nurodyti atskiras DK paskirstymo pagrindo taisykles. Vykdydami procesą „Apdoroti paskirstymo užklausą“ vartotojai gali apdoroti DK paskirstymo taisyklę ir peržiūrėti gautus paskirstymo žurnalo įrašus prieš užregistruodami arba panaikindami apskaičiuotus paskirstymus.

## <a name="components-of-ledger-allocation-rules"></a>DK paskirstymo taisyklių komponentai
Kiekviena paskirstymo taisyklė turi keturis komponentus: bendrą, šaltinio, paskirties ir korespondentinį. Papildomas komponentas, DK paskirstymo pagrindo taisyklės, yra reikalingos, jei Pagrindas naudojamas kaip paskirstymo metodas. Kiekvienas komponentas suteikia svarbią informacijos dalį, reikalingą paskirstymams apdoroti.

-   **Bendra** – šiame komponente vartotojas nurodo parinktis, pvz., paskirstymo metodą, vidinės įmonės taisyklių parametrus ir tai, ar taisyklė yra aktyvi.
-   **Šaltinis** – šiame komponente vartotojas nurodo paskirstymo šaltinio duomenis. Paskirstymas gali būti pagrįstas DK balansais (**Duomenų šaltinis** = **DK**) arba fiksuotomis sumomis (**Duomenų šaltinis** = **Fiksuota reikšmė**). Kai **Duomenų šaltinis** nustatytas kaip **DK**, turi būti nurodyti DK paskirstymo taisyklės šaltinio filtro kriterijai (pvz., reklamos išlaidos).
-   **Paskirties vieta** – šis komponentas apibrėžia, kaip paskirstymo skaičiavimų rezultatas turi būti paskirstytas ir kaip už jį turi būti atsiskaityta. Pvz., galima sukurti vieną kiekvieno padalinio paskirties eilutę.
-   **Korespondentinis** – šis komponentas apibrėžia, kaip pagrindinės sąskaitos ir dimensijos turėtų būti nustatytos korespondentinėms įvestims, kurios subalansuoja paskirties įrašus. Paprastai naudojamos vartotojo nurodytos parinktys, o ne šaltinyje nurodytos sąskaitos ir dimensijos. Kai **Duomenų šaltinis** nustatytas kaip **Fiksuota reikmė**, **Šaltinis** negali būti naudojamas kaip parinktis.
-   **DK paskirstymo pagrindo taisyklės** – šios taisyklės naudoja savo šaltinio filtro kriterijus, kad nustatytų, kurie DK balansai turi būti naudojami paskirstant (pvz., įplaukos pagal padalinį). Kiekviena paskirstymo pagrindo taisyklė gali būti taikoma su daugeliu paskirstymo taisyklių.




