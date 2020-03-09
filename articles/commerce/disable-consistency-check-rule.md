---
title: Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles
description: Šioje temoje aprašomos funkcijos, skirtos išjungti operacijų vientisumo tikrintuvo taisykles, veikiančias „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: 51a02d6f305cbad9784cf1b811188d0e06b6f15b
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057642"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mažmenininkai gali turėti unikalius jiems skirtus verslo scenarijus ir procesus. Todėl ne visos taisyklės, kurios pagal numatytuosius nustatymus yra įtrauktos į prekybos operacijų vientisumo tikrintuvą, taikomos visiems mažmenininkams. Skirtumams suderinti „Microsoft Dynamics 365 Commerce” suteikia funkcijas, kurias galima naudoti netaikomoms taisyklėms išjungti.

Norėdami peržiūrėti sąrašo taisykles, prieinamas operacijų vientisumo tikrintuve jūsų aplinkoje, ir norėdami peržiūrėti kiekvienos taisyklės būseną, eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> „Commerce“ parametrai** ir pasirinkite skirtuką **Operacijų tikrinimas**.

Pagal numatytuosius nustatymus kiekvienos taisyklės būsena nustatyta kaip **Įjungta**. Todėl visos taisyklės naudojamos operacijoms patikrinti prieš jas perkeliant į prekybos išrašus. Norėdami išjungti taisyklę, pakeiskite jos būseną į **Išjungta**. Į išjungtas taisykles neatsižvelgiama tikrinant operacijas išrašų apskaičiavimo proceso metu.

Norėdami apeiti visą tikrinimo procesą nepaisydami įjungtų taisyklių, eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> „Commerce“ parametrai** ir tada skirtuke **Operacijų tikrinimas** nustatykite parinktį **Išjungti „Commerce“ operacijų vientisumo tikrintuvą** į **Taip**. Nustačius šią parinktį į **Ne**, jos nebus galima nustatyti atgal į **Taip** naudojantis vartotojo sąsaja (UI).
