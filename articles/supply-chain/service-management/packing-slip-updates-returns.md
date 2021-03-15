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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c82e43beddb8bae0a56b0894ce484ca7605b42e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006721"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]