---
title: Važtaraščių naujinimas grąžinimams
description: Prieš tai, kai grąžintos prekės bus gautos į atsargas, turi būti atnaujintas užsakymo, kuriam jos priklauso, važtaraštis.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e3ea1fc5a7d75682df431b73be40b28ba6f6bc9
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830008"
---
# <a name="packing-slip-updates-for-returns"></a>Važtaraščių naujinimas grąžinimams  

[!include [banner](../includes/banner.md)]


Prieš tai, kai grąžintos prekės bus gautos į atsargas, turi būti atnaujintas užsakymo, kuriam jos priklauso, važtaraštis. Tik tada, kai SF atnaujinimo procesas yra finansinės operacijos atnaujinimas, važtaraščio atnaujinimas yra fizinis atsargų įrašo atnaujinimas, t. y. jo metu atliekami atsargų pakeitimai. Grąžinimo atvejais važtaraščio atnaujinimo metu atliekami tie žingsniai, kurie priskirti perdavimo veiksmui.

Važtaraščio atnaujinimas gali būti atliktas arba prekių gavimo žurnale, arba grąžinimo užsakyme.

Vienu iš važtaraščio registravimo proceso metu atliekamų veiksmų gali būti važtaraščio nuorodos numerio, esančio kliento siuntimo dokumentuose, susiejimas su užsakymo eilutėmis. Šis susiejimas nėra privalomas ir naudojamas tik kaip nuoroda. Joks operacijos atnaujinimas nesukuriamas.

Jei gautos ne visos numatytos grąžinimo prekės, atnaujindami važtaraštį įtraukite tik gautą kiekį. Likusias prekes palikite užsakyme, kol bus gauta visa grąžinimo siunta.

Jei prekė išsiųsta atgal iš sulaikymo į siuntimo ir gavimo padalinį, pvz., kai sulaikymo inspektorius nežino, kur laikyti prekę atsargose, turi būti atnaujintas atitinkamas važtaraštis, kad būtų tinkamai užregistruotas ir veiktų perdavimo kodas, kuris nurodytas kaip sulaikymo rezultatas.

Kai atnaujinate važtaraštį grąžintai prekei iš pardavimo sutarties, tos prekės pardavimo sutarties įsipareigojimas automatiškai atnaujinamas, kad atspindėtų kiekio ar sumos pokytį. 

## <a name="see-also"></a>Taip pat žiūrėkite

[SF naujinimas grąžinimams](perform-invoice-updates-for-returns.md)

  


