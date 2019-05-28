---
title: DUK apie darbo eigas
description: Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509296"
---
# <a name="workflow-system"></a>Darbo eigos sistema

[!include [banner](../includes/banner.md)]

Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.

## <a name="notifications"></a>Pranešimai

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Kodėl gaunami keli pranešimai, kai atmetamas darbo elementas?
Kai atmetamas darbo elementas, tas darbo elementas užbaigiamas kaip atmestas. Sukuriamas kitas darbo elementas ir priskiriamas iniciatoriui. Tai reiškia, kad iniciatorius gaus pranešimą apie atmestą darbo elementą, taip pat atskiras pranešimas bus išsiųstas vartotojui, kuris priskirtas naujam darbo elementui „reikalaujama keisti“. 

Kiekvienas pranešimas skirtas skirtingam darbo elementui, tačiau dėl panašumų gali kilti painiava. Ieškome būdų, kaip šią situaciją išspręsti būsimuose leidimuose.

### <a name="why-are-my-workflow-exports-failing"></a>Kodėl man nepavyksta eksportuoti darbo eigos?
Šiuo metu darbo eigos eksportavimo funkcija yra ribojama darbo eigos pavadinimams neleidžiant viršyti 48 ženklų. Naudojant ilgesnius kaip 48 ženklų pavadinimus, pateikiama klaida „Serveriui nepavyko autentifikuoti užklausos“ ir (arba) neleidžiama eksportuoti failo be failo tipo. Šiame tinklaraščio įraše pateikiama išsamesnė informacija [Darbo eigos eksportavimo trikčių šalinimas](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
