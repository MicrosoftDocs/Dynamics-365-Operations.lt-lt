---
title: Prekių poreikių kūrimas pagal aptarnavimo užsakymus
description: Šiame straipsnyje aprašoma, kaip sukurti prekių poreikius aptarnavimo užsakymams.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2c90ff76121b436d0fec532268cd3383de0eab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888418"
---
# <a name="create-item-requirements-for-service-orders"></a>Prekių poreikių kūrimas pagal aptarnavimo užsakymus

[!include [banner](../includes/banner.md)]

Galite kurti aptarnavimo užsakymą, jei norite sekti ir valdyti klientams teikiamas paslaugas. Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių. Prekės poreikį galima nedelsiant panaudoti iš atsargų, arba jis gali inicijuoti tos prekės gamybos užsakymą.

Naudodami prekės poreikį vietoje prekės operacijos, galite planuoti pristatymą prieš faktiškai naudojant prekę, kurti pirkimo užsakymą, įtraukti prekę į prekybos sutarties sistemą bei įtraukti prekės poreikį į gamybos planavimą.

Prekės poreikiai aptarnavimo užsakymuose apdorojami vykdant projektą. Norint sukurti prekės poreikį aptarnavimo užsakyme, aptarnavimo užsakymą reikia priskirti prie projekto. Kai sukuriate aptarnavimo užsakymo prekės poreikį, galite peržiūrėti prekės poreikį pasirinkto projekto formoje **Projektai**.

## <a name="create-an-item-requirement-for-a-service-order"></a>Prekės poreikio aptarnavimo užsakymui sukūrimas

1. Eikite į **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.
1. Pažymėkite aptarnavimo užsakymą, kuriam norite sukurti prekės poreikį.
1. Dalies **Veiksmų sritis** skirtuke **Išsiuntimas** rinkitės **Prekės poreikis**.
1. Formoje **Prekių poreikis** įveskite reikiamos prekės informaciją. Daugiau informacijos apie konkrečius laukus žr. [Prekių poreikis (forma)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Prekės poreikio aptarnavimo sutarčiai sukūrimas

1. Eikite į **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.
1. Atidarykite aptarnavimo sutartį, kuriai norite sukurti prekės poreikį.
1. Norėdami sukurti naują eilutę, „FastTab” **Eilutės** pasirinkite **Įtraukti**.
1. Lauke **Operacijos tipas** pasirinkite **Prekė**.
1. Lauke **Prekių nustatymai** pasirinkite **Prekės poreikis**.
1. Lauke **Prekės numeris** pasirinkite prekę, kurios reikia aptarnavimo sutarčiai.
1. „FastTab“ **Eilutės informacija** skirtuko **Produktų dimensijos** lauke **Vieta** pasirinkite prekės atsargų vietą.
1. Norėdami kurti aptarnavimo užsakymą iš sutarties eilutės, „FastTab“ **Eilutės** rinkitės **Kurti aptarnavimo užsakymus** ir įveskite atitinkamą informaciją formoje **Kurti aptarnavimo užsakymus**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Automatiškai kurti aptarnavimo užsakymus](create-service-orders-automatically.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
