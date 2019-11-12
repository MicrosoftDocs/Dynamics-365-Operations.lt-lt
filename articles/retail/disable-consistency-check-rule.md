---
title: Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles
description: Šioje temoje aprašomos funkcijos, skirtos išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles, veikiančias „Microsoft Dynamics 365 Retail“.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586302"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mažmenininkai gali turėti unikalius jiems skirtus verslo scenarijus ir procesus. Todėl ne visos taisyklės, kurios pagal numatytuosius nustatymus yra įtrauktos į mažmeninės prekybos operacijų vientisumo tikrintuvą, taikomos visiems mažmenininkams. Norint atsižvelgti į skirtumus, „Microsoft Dynamics 365 Retail” suteikia funkcijas, kurias galima naudoti netaikomoms taisyklėms išjungti.

Norėdami peržiūrėti sąrašo taisykles, prieinamas mažmeninės prekybos operacijų vientisumo tikrintuve jūsų aplinkoje, ir norėdami peržiūrėti kiekvienos taisyklės būseną, eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai** ir pasirinkite skirtuką **Operacijų tikrinimas**.

Pagal numatytuosius nustatymus kiekvienos taisyklės būsena nustatyta kaip **Įjungta**. Todėl visos taisyklės naudojamos mažmeninės prekybos operacijoms patikrinti prieš jas perkeliant į mažmeninės prekybos išrašus. Norėdami išjungti taisyklę, pakeiskite jos būseną į **Išjungta**. Į išjungtas taisykles neatsižvelgiama tikrinant mažmeninės prekybos operacijas išrašų apskaičiavimo proceso metu.

Norėdami apeiti visą tikrinimo procesą nepaisydami įjungtų taisyklių, eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai** ir tada skirtuke **Operacijų tikrinimas** nustatykite parinktį **Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvą** į **Taip**. Nustačius šią parinktį į **Ne**, jos nebus galima nustatyti atgal į **Taip** naudojantis vartotojo sąsaja (UI).
