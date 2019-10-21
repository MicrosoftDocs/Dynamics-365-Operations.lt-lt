---
title: Kliento įspėjimų pranešimai el. paštu
description: Šioje temoje pateikiama informacija apie tai, kaip nustatyti taisykles, kurios siunčia el. pašto pranešimus įvykus iš anksto nurodytiems įvykiams.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ba92c3dc1debed7e98210168d1a135e2cf567aec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191298"
---
# <a name="client-alert-notifications-by-email"></a>Kliento įspėjimų pranešimai el. paštu

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Galite nustatyti pasirinktines įspėjimo taisykles, kurios stebi filtruotus duomenų rodinius ir automatiškai siunčia el. pašto pranešimus, kai įvyksta iš anksto nurodyti įvykiai. Parinktis siųsti el. pašto pranešimus suteikiama pasirinkus bet kurį palaikomą įspėjimo tipą ir ją taip pat galima įjungti pasirinkus esamas įspėjimo taisykles.

Taip pat galite naudoti integruotus valdiklius, kad sukurtumėte įspėjimo taisykles, kurios stebi sistemos paketinių užduočių filtruotą vaizdą. Stebėdami lauko **Būsena** reikšmę, taip pat galite sukonfigūruoti įspėjimo taisykles, kurios siunčia el. laišką, kai paketinės užduoties vykdymas nepavyksta. Sukūrę šias įspėjimo taisykles, galėsite nebetikrinti verslo duomenų pakeitimų ataskaitose. Vietoj to, išmanioji pakeitimų atlikimo tarnyba gali stebėti už jus.

Kliento įspėjimai priklauso nuo el. pašto posistemės, kuri teikiama integruojant su „Microsoft Office“. Rekomenduojame naudoti „Simple Mail Transfer Protocol“ (SMTP) teikėją, el. laiškų pristatymas nepriklausytų tik nuo vietos pašto kliento.

Norėdami siųsti pranešimus el. paštu, klientai turi sukonfigūruoti integruotas el. pašto paslaugas. El. pašto pranešimai siunčiami gavėjams įspėjimo savininkų vardu.

Daugiau informacijos apie tai, kaip konfigūruoti el. paštą, žr. [El. laiškų konfigūravimas ir siuntimas](../organization-administration/configure-email.md).

Toliau pateiktame vaizde rodomas dialogo langas **Kurti įspėjimo taisyklę**, į kurį dabar įtraukta parinktis **Siųsti el. laišką**.

[![Dialogo langas Kurti įspėjimo taisyklę, kuriame parinktis Siųsti el. laišką nustatyta į Taip](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kai parinktis **Siųsti el. laišką** nustatyta į **Taip**, įspėjimo pranešimai bus toliau pristatomi iš veiksmų centro.

## <a name="alert-notification-email-templates"></a>Įspėjimo pranešimų el. pašto šablonai

Paslauga siunčia el. pašto pranešimus naudodama iš anksto nustatytus el. laiškų šablonus, kad pristatytų pagrindinę įspėjimo pranešimo informaciją.

Toliau pateiktame vaizde rodoma įspėjimo pranešimų struktūra juos gavus el. paštu.

[![Įrašų kūrimo, laukų pakeitimo ir šablonų naikinimo įspėjimo pranešimai, pagrįsti šablonu](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)