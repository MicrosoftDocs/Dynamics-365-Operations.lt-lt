---
title: Prekės poreikių kūrimas pagal aptarnavimo užsakymus
description: Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a730ae945af15c7bd4020c734bac971d8186e2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "312214"
---
# <a name="create-item-requirements-for-service-orders"></a>Prekės poreikių kūrimas pagal aptarnavimo užsakymus 

[!include [banner](../includes/banner.md)]


Galite kurti aptarnavimo užsakymą, jei norite sekti ir valdyti klientams teikiamas paslaugas. Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių. Prekės poreikį galima nedelsiant panaudoti iš atsargų, arba jis gali inicijuoti tos prekės gamybos užsakymą.

Naudodami prekės poreikį vietoje prekės operacijos, galite planuoti pristatymą prieš faktiškai naudojant prekę, kurti pirkimo užsakymą, įtraukti prekę į prekybos sutarties sistemą bei įtraukti prekės poreikį į gamybos planavimą.

Prekės poreikiai aptarnavimo užsakymuose apdorojami vykdant projektą. Norint sukurti prekės poreikį aptarnavimo užsakyme, aptarnavimo užsakymą reikia priskirti prie projekto. Kai sukuriate aptarnavimo užsakymo prekės poreikį, galite peržiūrėti prekės poreikį pasirinkto projekto formoje **Projektai**.

## <a name="create-an-item-requirement-for-a-service-order"></a>Prekės poreikio aptarnavimo užsakymui sukūrimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.

2.  Pažymėkite aptarnavimo užsakymą, kuriam norite sukurti prekės poreikį.

3.  Dalies **Veiksmų sritis** skirtuke **Išsiuntimas** spustelėkite **Prekės poreikis**.

4.  Formoje **Prekių poreikis** įveskite reikiamos prekės informaciją. Daugiau informacijos apie konkrečius laukus žr. [Prekių poreikis (forma)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Prekės poreikio aptarnavimo sutarčiai sukūrimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.

2.  Atidarykite aptarnavimo sutartį, kuriai norite sukurti prekės poreikį.

3.  „FastTab“ **Eilutės** spustelėję **Pridėti** sukursite naują eilutę.

4.  Lauke **Operacijos tipas** pasirinkite **Prekė**.

5.  Lauke **Prekių nustatymai** pasirinkite **Prekės poreikis**.

6.  Lauke **Prekės numeris** pasirinkite prekę, kurios reikia aptarnavimo sutarčiai.

7.  „FastTab“ **Eilutės informacija** skirtuko **Produktų dimensijos** lauke **Vieta** pasirinkite prekės atsargų vietą.

8.  Norėdami kurti aptarnavimo užsakymą iš sutarties eilutės, „FastTab“ **Eilutės** spustelėkite **Kurti aptarnavimo užsakymus** ir įveskite atitinkamą informaciją formoje **Kurti aptarnavimo užsakymus**. 


## <a name="see-also"></a>Taip pat žiūrėkite

[Automatiškai kurti aptarnavimo užsakymus](create-service-orders-automatically.md).

  


