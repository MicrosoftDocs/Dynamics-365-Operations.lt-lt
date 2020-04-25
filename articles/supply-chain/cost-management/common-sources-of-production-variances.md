---
title: Bendrieji gamybos nuokrypių šaltiniai
description: Šis straipsnis paaiškina įvairius įprastus kiekvieno gamybos nuokrypio tipo šaltinius.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da09e24d7ed041686385b8239287288228d3668e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201967"
---
# <a name="common-sources-of-production-variances"></a>Bendrieji gamybos nuokrypių šaltiniai

[!include [banner](../includes/banner.md)]

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




