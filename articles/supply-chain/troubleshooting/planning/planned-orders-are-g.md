---
title: Bendrasis planavimas generuoja vienišų produktų suplanuotus užsakymus
description: Suplanuoti užsakymai yra sukuriami vienišiems produktams po pagrindinio planavimo vykdymo.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742009"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Bendrasis planavimas generuoja vienišų produktų suplanuotus užsakymus

KB numeris: 4614729

## <a name="symptoms"></a>Požymiai

Suplanuoti užsakymai yra sukuriami vienišiems produktams po pagrindinio planavimo vykdymo.

## <a name="resolution"></a>Skiriamoji geba

Išleistų produktų parinkties **„Phantom“** parametras nustato numatytąjį komplektavimo specifikacijos (KS) eilutės tipą. Kai nustatyta prinktias **„Phantom“** į *Taip*, sistema vis tiek sukurs suplanuotus prekės užsakymus, tačiau kiekvienam suplanuotam užsakymui bus nustatyta parinktis **Tiesiogiai išvestas poreikis** bus nustatyta kaip *Taip*. Todėl suplanuoto gamybos užsakymo negalima patvirtinti pats. Jis visada bus automatiškai įtrauktas, kai patvirtinsite pirminį gamybos užsakymą. Be to, suplanuoto vienišo užsakymo KS eilutės bus įtrauktos į pirminio gamybos užsakymo KS.
