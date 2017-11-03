---
title: "Bendrieji gamybos nuokrypių šaltiniai"
description: "Šis straipsnis paaiškina įvairius įprastus kiekvieno gamybos nuokrypio tipo šaltinius."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 041cd20e6b0ab7d1cb31e8925aa3a755ea556706
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="common-sources-of-production-variances"></a>Bendrieji gamybos nuokrypių šaltiniai

[!include[banner](../includes/banner.md)]


Šis straipsnis paaiškina įvairius įprastus kiekvieno gamybos nuokrypio tipo šaltinius. 

Štai keletas įprastų **partijos dydžio** nuokrypio šaltinių:

-   Gamybos užsakymo prekių kiekis skiriasi nuo skaičiavimo kiekio, naudojamo atliekant standartinį išlaidų skaičiavimą. Šis kiekis sudaro amortizuojamų pastovių išlaidų pagrindą.
-   Gamybos užsakymo pastovių išlaidų vertė skiriasi nuo pastovių išlaidų, naudojamų atliekant standartinį išlaidų skaičiavimą. Gamybos užsakymo pastovios išlaidos gali skirtis dėl keleto priežasčių. Pvz., pastovios išlaidos gali atspindėti šiuos veiksnius:
    -   rankiniu būdu atlikti gamybos komplektavimo specifikacijų (KS) arba maršruto keitimai;
    -   skirtingos KS versijos arba maršruto versijos pasirinkimas kuriant gamybos užsakymą;
    -   suplanuoti prekei priskirtos KS versijos arba maršruto versijos inžineriniai pakeitimai.

Štai keletas įprastų **gamybos kainos** nuokrypio šaltinių:

-   Paskelbto maršruto planavimo operacijos išlaidų kategorija (ir išlaidų kategorijos kaina) skiriasi nuo išlaidų kategorijos, naudojamos atliekant standartinį išlaidų skaičiavimą.
-   Išlaidų kategorijos kainos aktyvios išlaidos skiriasi nuo išlaidų kategorijos kainos, naudojamos atliekant standartinį išlaidų skaičiavimą.

Štai keletas įprastų **gamybos kiekio** nuokrypio šaltinių:

-   Medžiagos komponento išdavimas per didelis arba per mažas.
-   Maršruto planavimo operacijos ataskaitos laikas per ilgas arba per trumpas.
-   Gaunamas pirminės prekės kiekis lyginant su užsakymo kiekiu per didelis arba per mažas. Tačiau komponentus išduodate ir ataskaitas apie operacijas teikiate visas, pagal gamybos užsakymo kiekį.

Štai keletas įprastų **gamybos pakaitalo** nuokrypio šaltinių:

-   Medžiagos komponento, neįtraukto į gamybos KS, išdavimas.
-   Komponento įtraukimas į gamybos KS rankiniu būdu ir šio komponento paskelbimas sunaudotu.
-   Prekės paskelbimas sunaudota, kai ji nėra rankiniu būdu įtraukiama į gamybos KS.
-   Operacijos įtraukimas į gamybos maršrutą rankiniu būdu ir šios operacijos paskelbimas sunaudota.
-   Sukūrę gamybos užsakymą, pasirenkate KS versiją, kuri skiriasi nuo standartiniame skaičiavime naudojamos KS versijos.
-   Sukūrę gamybos užsakymą, pasirenkate maršruto versiją, kuri skiriasi nuo standartiniame išlaidų skaičiavime naudojamos KS versijos.





