---
title: Išjungti taisykles, naudojamas vykdant operacijų tikrinimo procesą
description: Šioje temoje aprašomos funkcijos, skirtos išjungti operacijų tikrinimo taisykles, veikiančias „Microsoft Dynamics 365 Commerce“.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919532"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Išjungti taisykles, naudojamas vykdant operacijų tikrinimo procesą

[!include [banner](../includes/banner.md)]

Mažmenininkai gali turėti unikalius jiems skirtus verslo scenarijus ir procesus. Todėl ne visos taisyklės, kurios yra įtrauktos į prekybos operacijų tikrinimo procesą, taikomos visiems mažmenininkams. Skirtumams suderinti „Microsoft Dynamics 365 Commerce” suteikia funkcijas, kurias galima naudoti netaikomoms taisyklėms išjungti.

Norėdami peržiūrėti taisyklių, kurios galimos vykdant operacijų tikrinimo procesą jūsų aplinkoje, sąrašą ir pamatyti kiekvienos taisyklės būseną, eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> „Commerce“ parametrai** ir pasirinkite skirtuką **Operacijos tikrinimas**. Visos įjungtos taisyklės naudojamos operacijoms tikrinti per procesą **Tikrinti parduotuvės operacijas** ir jos turi būti įvykdytos, kad operacijos būtų surinktos ir užregistruotos operacijų išraše.

Pagal numatytuosius nustatymus kiekvienos taisyklės būsena nustatyta kaip **Įjungta**. Todėl visos taisyklės naudojamos operacijoms patikrinti prieš jas perkeliant į prekybos operacijų išrašus. Norėdami išjungti taisyklę, pakeiskite jos būseną į **Išjungta**. Į išjungtas taisykles neatsižvelgiama tikrinant operacijas per procesą **Tikrinti parduotuvės operacijas**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
