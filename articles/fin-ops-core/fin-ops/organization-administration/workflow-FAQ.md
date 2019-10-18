---
title: DUK apie darbo eigas
description: Šioje temoje atsakoma į dažnai užduodamus klausimus apie darbo eigos sistemą.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14aa9b56da005e8e3ca121589d0e22c60f34343b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189780"
---
# <a name="workflow-faq"></a>DUK apie darbo eigas

[!include [banner](../includes/banner.md)]

Šioje temoje atsakoma į dažnai užduodamus klausimus apie darbo eigos sistemą.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Kodėl gaunami keli pranešimai, kai atmetamas darbo elementas?
Kai atmetamas darbo elementas, tas darbo elementas užbaigiamas kaip atmestas. Sukuriamas kitas darbo elementas ir priskiriamas iniciatoriui. Tai reiškia, kad iniciatorius gaus pranešimą apie atmestą darbo elementą, taip pat atskiras pranešimas bus išsiųstas vartotojui, kuris priskirtas naujam darbo elementui „reikalaujama keisti“. 

Kiekvienas pranešimas skirtas skirtingam darbo elementui, tačiau dėl panašumų gali kilti painiava. Ieškome būdų, kaip šią situaciją išspręsti būsimuose leidimuose.

## <a name="why-are-my-workflow-exports-failing"></a>Kodėl man nepavyksta eksportuoti darbo eigos?
Šiuo metu darbo eigos eksportavimo funkcija yra ribojama darbo eigos pavadinimams neleidžiant viršyti 48 ženklų. Naudojant ilgesnius kaip 48 ženklų pavadinimus, pateikiama klaida „Serveriui nepavyko autentifikuoti užklausos“ ir (arba) neleidžiama eksportuoti failo be failo tipo. Šiame tinklaraščio įraše pateikiama išsamesnė informacija [Darbo eigos eksportavimo trikčių šalinimas](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Ar darbo eigos pateikėjas gali ją taip pat ir tvirtinti?
Taip, darbo eigos pateikėjas taip pat gali ją tvirtinti, jei darbo eiga taip sukonfigūruota. Jei norite to neleisti, nustatykite **Darbo eigos parametrai > Bendra > Tvirtintojas > Neleisti tvirtinti pateikėjui** reikšmę **Taip**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Ar galiu įtraukti įspėjimų į darbo eigas, kad vartotojams būtų teikiami pranešimai?
Toliau pateikiamos kelios pagrindinės sritys, susijusios su įspėjimų įtraukimų į darbo sritis norint teikti pranešimus vartotojams, į kurias reikia atkreipti dėmesį.
- Įspėjimų palyginimas su darbo eigų pranešimų mechanizmais
    - Galima nustatyti įrašų pakeitimų įspėjimus. Darbo eigos keičia įrašus, todėl galima nustatyti įspėjimą, susijusį su darbo eigos inicijuotu įrašo pakeitimu. Vis dėlto, įspėjimų naudojimas nėra tobulas sprendimas, nes darbo eigose įtaisytos skirtingos pranešimų parinktys.
- Standartiniai darbo eigų pranešimai 
    - Darbo eigose yra įtaisytų el. pašto pranešimų. Klientas gali konfigūruoti pranešimus, kad vartotojams būtų siunčiami el. laiškai. Šie pranešimai neinicijuoja veiksmų centro pranešimų vartotojams.
    - Būsimame naujinime veiksmų centro pranešimą, kad vartotojui būtų priskirtas darbo eigos darbo elementas. 
- Pranešimų įtraukimas į darbo eigas
    - Galima sukurti veiksmų centro pranešimų konkretiems vartotojams, pvz., darbo eigos pranešimų, sukurtų naudojant X++.
    - [Darbo eigose yra verslo įvykių](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), kuriuos klientas gali naudoti norėdamas suaktyvinti srautus su ieškomais pranešimais.   

Apibendrinant, jei vartotojas negauna tinkamo pranešimo iš veiksmų centro, kai jam priskiriamas darbo eigos darbo elementas, naudokite [darbo eigos verslo įvykius](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) programoje „Microsoft Flow, kad pateiktumėte papildomų arba kitokių pranešimų.
