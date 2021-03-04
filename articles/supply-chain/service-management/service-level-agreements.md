---
title: Aptarnavimo lygio sutarčių apžvalga
description: Teikiamų paslaugų sutartyje klientas sutinka su minimaliu atsiliepimo laiku, kuris remiasi laiku, nuo to, kai aptarnavimo įmonė užregistruoja problemą, iki tol, kai problema išsprendžiama.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01cdfe519e55ca2a9aa17f4ac181ee675b2793cf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433680"
---
# <a name="service-level-agreements-overview"></a>Aptarnavimo lygio sutarčių apžvalga       

[!include [banner](../includes/banner.md)]


Aptarnavimo lygio sutartis (ALS) yra sutartis tarp aptarnavimo įmonės ir kliento. ALS klientas sutinka su minimaliu atsiliepimo laiku, kuris remiasi laiku, nuo to, kai aptarnavimo įmonė užregistruoja problemą iki tol, kai problema išsprendžiama.

ALS suteikia standartinio lygio klientams siūlomą aptarnavimą, taip pat aiškiai nurodo aptarnavimo įmonei, kada turi būti baigta aptarnavimo užduotis.

Norint pasiūlyti klientams skirtingus aptarnavimo lygius, gali būti sukurtas bet koks ALS skaičius.

## <a name="create-a-service-level-agreement"></a>Kurti aptarnavimo sutartį

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo sutartys** \> **Aptarnavimo lygio sutartys**.

2.  Lauke **Aptarnavimo lygio sutartis** įveskite aptarnavimo lygio sutarties pavadinimą.

3.  Įveskite laiką, per kurį norite, kad būtų atlikti prie aptarnavimo lygio sutarties pridėti aptarnavimo skambučiai. Po to, jei norite, kad aptarnavimo lygio sutartis būtų grįsta tam tikru kalendoriumi, pasirinkite kalendorių.

## <a name="apply-a-service-level-agreement"></a>Taikyti aptarnavimo lygio sutartį

ALS taikoma tiesiogiai aptarnavimo sutarčiai.

Aptarnavimo užsakymai, kuriuos kuriate patys ir pridedate prie aptarnavimo sutarties ir kurie turi ALS, yra lyginami su šia ALS.

Aptarnavimo užsakymai, kuriuos jūs sukuriate automatiškai, prie ALS nepridedami.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Taikyti aptarnavimo lygio sutartį aptarnavimo sutarčiai

1.  Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**. Pasirinkite aptarnavimo sutartį, kuriai norite taikyti ALS, po to srityje **Veiksmų sritis** spustelėkite **Redaguoti**.

2.  Lauke **Aptarnavimo lygio sutartis** pasirinkite norimą priskirti ASL.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Taikyti aptarnavimo lygio sutartį aptarnavimo sutarties grupei

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutarčių grupės**.

2.  Lauke **Aptarnavimo lygio sutartis** pasirinkite norimą priskirti ASL.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Sekimo laikas aptarnavimo užsakyme nuo ALS

Sukūrus naują aptarnavimo sutarties, kuriai priskirta ALS, aptarnavimo užsakymą sukuriamas paslaugų suteikimo laiko intervalas ir sistema pradeda sekti paslaugų suteikimo laiką. Be to, galite nustatyti toliau nurodytas pasirinktis.

  - Jūs galite pradėti ir sustabdyti laiko įrašymą aptarnavimo užsakyme, norėdami registruoti laiko, praleisto aptarnavimo užsakymams, sumą.

  - Galite stebėti, ar yra laikomasi aptarnavimo lygio sutartyje nustatyto laiko intervalo.

  - Galite nurodyti priežasties kodus, kurie turi būti nustatyti, jei viršijamas aptarnavimo lygio sutarties laiko intervalas.

## <a name="see-also"></a>Taip pat žiūrėkite

[Aptarnavimo lygio sutarčių atitikimo peržiūra](view-compliance-with-service-level-agreements.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]