---
title: Prekės poreikių kūrimas pagal aptarnavimo užsakymus
description: Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ae44088a1b53ac5e7e9ba09ed7ff611a08d2ed0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996705"
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

4.  Formoje **Prekių poreikis** įveskite reikiamos prekės informaciją. Daugiau informacijos apie konkrečius laukus žr. [Prekių poreikis (forma)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]