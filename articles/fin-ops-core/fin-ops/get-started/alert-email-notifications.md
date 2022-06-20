---
title: Kliento įspėjimų pranešimai el. paštu
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti taisykles, pagal kurias bus siunčiami iš anksto nurodyti el. paštu siunčiamų įvykių pranešimai.
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 469c7fdda40780d6e559819103d73d7a4e7132a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878284"
---
# <a name="client-alert-notifications-by-email"></a>Kliento įspėjimų pranešimai el. paštu

[!include [banner](../includes/banner.md)]

Galite nustatyti pasirinktines įspėjimo taisykles, kurios stebi filtruotus duomenų rodinius ir automatiškai siunčia el. pašto pranešimus, kai įvyksta iš anksto nurodyti įvykiai. Parinktis siųsti el. pašto pranešimus suteikiama pasirinkus bet kurį palaikomą įspėjimo tipą ir ją taip pat galite įjungti pasirinkus esamas įspėjimo taisykles.

Taip pat galite naudoti integruotus valdiklius, kad sukurtumėte įspėjimo taisykles, kurios stebi sistemos paketinių užduočių filtruotą vaizdą. Stebėdami lauko **Būsena** reikšmę, taip pat galite sukonfigūruoti įspėjimo taisykles, kurios siunčia el. laišką, kai paketinės užduoties vykdymas nepavyksta. Kai sukursite šias įspėjimo taisykles, galėsite nebetikrinti verslo duomenų pakeitimų ataskaitose. Vietoj to, išmanioji pakeitimų atlikimo tarnyba gali stebėti už jus.

Kliento įspėjimai priklauso nuo el. pašto posistemės, kuri teikiama integruojant su „Microsoft Office“. Rekomenduojame naudoti „Simple Mail Transfer Protocol“ (SMTP) teikėją, el. laiškų pristatymas nepriklausytų tik nuo vietos pašto kliento.

Norėdami siųsti pranešimus el. paštu, klientai turi sukonfigūruoti integruotas el. pašto paslaugas. El. pašto pranešimai siunčiami gavėjams įspėjimo savininkų vardu.

Daugiau informacijos apie tai, kaip konfigūruoti el. paštą, žr. [El. laiškų konfigūravimas ir siuntimas](../organization-administration/configure-email.md).

Toliau pateiktame vaizde rodomas dialogo langas **Kurti įspėjimo taisyklę**, į kurį dabar įtraukta parinktis **Siųsti el. laišką**.

[![Dialogo langas Kurti įspėjimo taisyklę, kuriame parinktis Siųsti el. laišką nustatyta į Taip.](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kai parinktis **Siųsti el. laišką** nustatyta į **Taip**, įspėjimo pranešimai bus toliau pristatomi iš veiksmų centro.

## <a name="alert-notification-email-templates"></a>Įspėjimo pranešimų el. pašto šablonai

Paslauga siunčia el. pašto pranešimus naudodama iš anksto nustatytus el. laiškų šablonus, kad pristatytų pagrindinę įspėjimo pranešimo informaciją.

Šiame vaizde rodoma įspėjimo pranešimų struktūra juos gavus el. paštu.

[![Įrašų kūrimo, laukų pakeitimo ir šablonų naikinimo įspėjimo pranešimai, pagrįsti šablonu.](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]