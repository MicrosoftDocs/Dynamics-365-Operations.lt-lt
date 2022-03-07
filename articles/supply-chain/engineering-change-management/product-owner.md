---
title: Produktų savininkai
description: Šioje temoje pateikta informacija apie produkto savininkus. Produkto savininkas yra vartotojų grupė atsakinga už konkrečius produktus. Tik grupės nariai gali išleisti minėtus produktus. Produkto savininkas gali taip pat būti naudojamas patvirtinimo darbo eigoje.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4de6399f83eeb0b0e1ea6fb13e86fb6dca456ff1c9b113e024afec97cc5b68af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766732"
---
# <a name="product-owners"></a>Produktų savininkai

[!include [banner](../includes/banner.md)]

Produkto savininkas yra vartotojų grupė atsakinga už konkrečius produktus. Kai produkto savininko grupė yra priskirta produktui, tik tos grupės nariai gali išleisti produktą. Produkto savininkas gali taip pat būti naudojamas patvirtinimo darbo eigoje inžinerijos keitimo valdyme.

Produkto savininkai yra bendrieji nustatymai. Dėl to, jie yra prieinami visiems juridiniams asmenims.

## <a name="create-a-product-owner-group"></a>Sukurkite produkto savininko grupę

Norėdami sukurti produkto savininko grupę ir įtraukti į ją narius, atlikite šiuos žingsnius.

1. Eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Produkto savininkai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Laukelyje **Produkto savininkas** įveskite grupės pavadinimą.
4. Laukelyje **Pavadinimas** įveskite grupės aprašą.
5. „FastTab“ **Nariai** įtraukite darbuotojus, kurie turi būti grupės nariai.

## <a name="assign-a-product-owner-to-a-product"></a>Priskirkite produkto savininką produktui

Siekiant priskirti produkto savininką produktui, atlikite šiuos žingsnius.

1. Atverkite **Produkto išsamios informacijos** puslapį atitinkamam produktui ar pagrindiniam produktui.
1. „FastTab“ **Bendri** nustatykite **Produkto savininko** laukelį į atitinkamo produkto savininko grupės pavadinimą.

Kol produkto savininkas yra priskirtas produktui, tik produkto savininko grupės nariai gali redaguoti **Produkto savininko** nustatymus.

Produkto savininkas yra taip pat matomas **Išleistų produktų** puslapyje.

## <a name="product-owners-and-product-releases"></a>Produkto savininkai ir produkto leidimai

Tik vartotojai iš produkto produkto savininko grupės gali išleisti tą produktą. Nepaisant to, yra išimtis, kai produktas yra vaikiška prekė ir jos valdanti prekė yra išleidžiama valdančio savininko. Kitaip tariant, jei produktas yra kito produkto KS dalis, sistema netikrina kiekvienos prekės KS produkto savininko. Ji tikrina tik valdančios prekės produkto savininką.

Pavyzdžiui, produktas X yra priskirtas *Kūrimo biurų* produkto savininko grupei. Produktas X taip pat yra KS Y produkto dalis, kuris yra priskirtas *Projektavimo garsiakalbių* produkto savininko grupei. Jei naudotojas iš *Projektavimo garsiakalbių* produkto savininko grupės išleidžia Y produktą ir jo KS, produktas X bus išleistas kartu su produktu Y.

## <a name="product-owners-and-approvals"></a>Produkto savininkai ir patvirtinimai

Kadangi produkto savininkai žino, ar konkretūs inžineriniai pakeitimai tiks jų produktams, dažnai apsimoka įtraukti juos kaip patvirtinimo proceso dalį inžinerijos keitimo valdyme. Galite įgyvendinti šį požiūrį nustatydami produkto savininkus kaip pagrindinius tiekėjus darbo eigose, kurios naudojamos inžinerijos pokyčio valdymui. Sistema tuomet priskirs patvirtinimo užduotis darbo eigose atsižvelgiant į produktus, kurie yra inžinerijos keitimo užklausose ir inžinerijos keitimo užsakymuose. Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]