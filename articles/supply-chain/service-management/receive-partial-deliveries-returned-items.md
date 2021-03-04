---
title: Grąžintų prekių dalinių pristatymų gavimas
description: Daliniai pristatymai apibrėžiami kalbant apie grąžinimo užsakymo eilutes, ne apie grąžinimo užsakymo siuntas.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf35169d8afd6e88b8ebe921514ed6d55607a4dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433340"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Grąžintų prekių dalinių pristatymų gavimas    

[!include [banner](../includes/banner.md)]


Daliniai pristatymai apibrėžiami kalbant apie grąžinimo užsakymo eilutes, ne apie grąžinimo užsakymo siuntas.

Tai reiškia, kad, jei gaunate visą kiekį, nurodytą vienoje grąžinimo užsakymo eilutėje, bet nieko negaunate iš kitose grąžinimo užsakymo eilutėse nurodyto kiekio, šis pristatymas nėra dalinis. Tačiau, jei grąžinimo užsakymo eilutėje nurodyta grąžinti 10 konkrečios prekės vienetų, bet gaunate tik keturis, tai yra dalinis pristatymas.

Jei grąžinimo siuntą sudaro ne visas grąžinimo užsakymo eilutėje nurodytas kiekis, siuntą galite atidėti į šalį ir laukti, kol bus pristatyta likusi grąžinto kiekio dalis, arba galite užregistruoti dalinį kiekį.

## <a name="register-and-post-a-partial-quantity"></a>Dalinio kiekio registravimas

1.  Pasirinkę gautiną grąžinimo užsakymą formoje **Gavimų peržiūra – sandėlis: %1, rampa: %2, žurnalo pavadinimas: %3** spustelėkite **Pradėti gavimo žurnalą**, kad sukurtumėte gavimo žurnalą, ir spustelėkite **Žurnalai** \> **Rodyti gavimų žurnalus pagal gavimus**, kad atidarytumėte formą **Vietos žurnalas**.

2.  Pasirinkite eilutę iš žurnalo, su kuriuo norite dirbti, tada spustelėkite **Eilutės**, kad atidarytumėte formą **Žurnalo eilutės, vietos**.

3.  Pasirinkite prekės, kurios dalinis kiekis buvo pristatytas, numerio eilutę, tada spustelėję **Funkcijos** \> **Skaidyti** atidarykite formą **Skaidyti**.

4.  Lauke **Skaidyti kiekį** įveskite bendrą gautų prekių skaičių, tada spustelėkite **Gerai**.

5.  Formoje **Žurnalo eilutės, vietos** pasirinkite pristatytų prekių kiekio eilutę, tada spustelėkite **Registruoti**. Pristačius prekes, galite registruoti eilutę papildomam kiekiui.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]