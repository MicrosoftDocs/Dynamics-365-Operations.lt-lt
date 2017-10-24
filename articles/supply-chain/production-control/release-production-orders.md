---
title: "Pateikti gamybos užsakymus"
description: "Išleistas gamybos užsakymas yra užsakymas, kurį leista gaminti. Terminas Išleistas naudojamas apibūdinti gamybos užsakymo ciklo būsenai, kai gamybos užsakymą galima vykdyti gamybos ceche ir atliekant sandėlio procesus."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aa38c50a58bed5702332182b9e0827b863f536f7
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="release-production-orders"></a>Pateikti gamybos užsakymus

[!include[banner](../includes/banner.md)]


Išleistas gamybos užsakymas yra užsakymas, kurį leista gaminti. Terminas Išleistas naudojamas apibūdinti gamybos užsakymo ciklo būsenai, kai gamybos užsakymą galima vykdyti gamybos ceche ir atliekant sandėlio procesus. 

<a name="characteristics-of-the-released-state"></a>Būsenos Patvirtinta charakteristikos
-------------------------------------

Būsena **Patvirtinta** yra viena gamybos užsakymo ciklo būsenų. Gamybos užsakymus, kurie yra būsenos **Patvirtinta**, galima vykdyti gamybos ceche ir atliekant sandėlio procesus. Būsenos **Patvirtinta** charakteristikos yra tokios:

-   Gamybos užsakymo būseną galima pakeisti į **Patvirtinta** gamybos užsakyme arba vykdant paketinį vykdymą. Gamybos užsakymą taip pat galima atnaujinti automatiškai suplanuotuose gamybos užsakymuose, patvirtintuose puslapio **Bendrasis planas** lauke **Tvirtinimo laiko ribos**.
-   Būsena **patvirtintų** yra cecho operatoriams (operatoriams) skirtas signalas pradėti vykdyti gamybos užduotis ceche.
-   Gamybos dokumentai, pvz., maršruto kortelės, maršruto užduotys ir užduočių kortelės, suteikia informacijos apie gamybos užduotis ir gali būti išduodami.
-   Esant faktiškai rezervuotų medžiagų, generuojamas sandėlio darbas, kad būtų galima pasirinkti gamybos užsakymo medžiagas.

## <a name="releasing-jobs-to-the-shop-floor"></a>Užduočių perdavimas į cechą
Išleidus gamybos užsakymą, su užsakymu susijusios gamybos užduotys yra matomos ir paruoštos registruoti. Operatoriai gali atlikti užduočių registravimus, pvz., pradžios, pabaigos ir užbaigimo, arba puslapyje **Užduoties kortelės terminalas** arba **Užduoties kortelės įrenginys**. Registruotas laikas ir kiekis automatiškai perkeliami iš registracijos puslapių į gamybos žurnalus, kad būtų galima sekti sunaudotą laiką ir kiekį.

## <a name="route-cards"></a>Technologinės kortelės
Technologinė kortelė pateikia informacijos, gaunamos iš maršruto ir operacijų nustatymų bei iš operacijų ir užduočių planavimo metodų, apžvalgą.

## <a name="route-jobs"></a>Maršruto užduotys
Maršruto užduotyje pateikiama kiekviena smulki operacijos užduotis ir įtraukiamas nustatymo, proceso, laukimo eilėje ir transportavimo laikas. Pavyzdžiui, tokiai operacijai, kaip dažymas, gali prireikti atskirų užduočių, tokių kaip nustatymo laikas, dažymo proceso laikas ir laukimo eilėje laikas džiūvimui.

## <a name="job-cards"></a>Užduočių kortelės
Užduoties kortelė pateikia atskirų užduočių numerius tam tikrai operacijai. Kiekviename puslapyje pateikiama viena užduotis. Užduoties kortelėje įtraukiamos užduotys ir jų numatomi laikai gaunami iš maršruto ir operacijos nustatymo informacijos. Užduoties kortelėje galite atidaryti puslapį **Gamybos žurnalo eilutės**, **užduoties kortelė**. Žmonės, prižiūrintys operacijų išteklius, gali pateikti atsiliepimus apie gamybos procesą. Yra laukų kur galite įvesti suvartojimo statistiką ir informaciją, tokią kaip klaidų kiekis.

## <a name="warehouse-work-for-raw-material-picking"></a>Sandėlio darbas žaliavoms paimti
Žaliavų paėmimo darbas generuojamas paleidimo metu. Darbas generuojamas tik tam medžiagų kiekiui, kuris buvo faktiškai rezervuotas gamybos užsakymui prieš pateikiant užsakymą. Norint generuoti žaliavų paėmimo sandėlyje darbą reikalinga toliau nurodyta sąranka.

-   Žaliavų paėmimo vietos nurodymas nustato, iš kurios sandėlio vietos paimti medžiagas
-   Žaliavų bangos šablonas, kuriame sukonfigūruotos sandėlio darbo vykdymo strategijos
-   Gamybos įvesties vieta, nurodanti, kur dedamos medžiagos





