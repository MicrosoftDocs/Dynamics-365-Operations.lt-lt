---
title: Slėpti mokesčių skaidymą užsakymo suvestinėse
description: Šioje temoje aprašoma, kaip slėpti mokesčių suskaidytą informaciją užsakymų suvestinėse krepšelyje, tikrinimo, užsakymo patvirtinimo ir užsakymo informacijos puslapiuose Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648136"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Slėpti mokesčių skaidymą užsakymo suvestinėse

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašoma, kaip slėpti mokesčių suskaidytą informaciją užsakymų suvestinėse krepšelyje, tikrinimo, užsakymo patvirtinimo ir užsakymo informacijos puslapiuose Microsoft Dynamics 365 Commerce.

Pagal numatytuosius Dynamics 365 Commerce nustatymus rodo mokesčių suskaidytą informaciją užsakymų suvestinėse krepšelyje, tikrinimo, užsakymo patvirtinimo ir užsakymo informacijos puslapius. Kaip ir "Commerce" 10.0.27 versijos paleidimas, "Commerce" svetainės generatoriuje yra parinktis, kuri leidžia slėpti mokesčių skaidymą užsakymo suvestinėse.

Šiame pavyzdyje pateikiamas dviejų užsakymo suvestinių pavyzdys. Pirmasis rodo mokesčio lūžio informaciją, o antrasis – jį paslepia.

![Krepšelių, kuriuose rodoma ir paslėpta mokesčių skaidymą, pavyzdžiai.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Parinktis slėpti mokesčių lūžio informaciją užsakymo suvestinėse galima tik tada, kai el. komercijos kanalo kainų su PVM parinktis nustatyta kaip Taip "Commerce Headquarters", **mažmeninės** prekybos ir komercijos **kanalų** **saugyklose \>\> visos parduotuvėse.\>** 
> - Pagal numatytuosius nustatymus **, svetainės generatoriuje įgalinta pasirinktis** Rodyti mokesčių skaidymą užsakymo suvestinėje.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Slėpti mokesčių skaidymą užsakymo suvestinėse

Norėdami paslėpti mokesčių skaidymą užsakymo suvestinėse, atlikite šiuos veiksmus.

1. "Commerce" svetainės generatoriuje eikite į svetainę, kurią norite naujinti.
1. Eiti į **Svetainės parametrai \> Plėtiniai**.
1. Išvalykite žymės **langelį Rodyti mokesčių skaidymą užsakymo** suvestinėje.

Norėdami rodyti mokesčių suskaidytą informaciją užsakymo suvestinėse, pažymėkite žymės **langelį Rodyti mokesčių suskaidytą užsakymą suvestinėje**.  

Šioje iliustracijoje rodomas žymės langelis **Rodyti mokesčių skaidymą užsakymo suvestinėje** pažymėtas ir pasirinktas vietos generatoriuje.

![Rodyti mokesčių skaidymą užsakymo suvestinės pasirinktyje vietos generatoriuje.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[PVM apžvalga](/finance/general-ledger/indirect-taxes-overview)

[Internetinių užsakymų PVM konfigūravimas](sales-tax-config.md)

[Trikčių šalinimas: netinkamai apskaičiuojami internetinių užsakymų mokesčiai](troubleshoot/tax-miscalculated-online-order.md)
