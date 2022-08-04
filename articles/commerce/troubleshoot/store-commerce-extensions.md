---
title: Parduotuvės "Commerce" plėtinio trikčių šalinimas
description: Šiame straipsnyje paaiškinama, kaip šalinti plėtinio problemas " Microsoft Dynamics 365 Commerce Store Commerce" programoje.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b440183e255e05c4f93a4f11106be2967163ff74
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169023"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Parduotuvės "Commerce" plėtinio trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip šalinti plėtinio problemas " Microsoft Dynamics 365 Commerce Store Commerce" programoje.

## <a name="extensions-packages-arent-loaded"></a>Neįkelta plėtinių paketų

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Plėtinių paketai nėra rodomi EKA parametrų \> puslapyje

Gali būti, kad "Commerce runtime" (CRT) paleidiniai nebuvo atnaujinti, kad būtų įtraukti plėtinio paketas, arba jie nėra įdiegti. Norėdami gauti daugiau informacijos, žr [. "Commerce runtime(CRT) extensibility ir triggers"](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>EKA parametrų puslapyje rodomi plėtinių \> paketai, bet deklaracija neįkelta

Patvirtinkite, kad "Store Commerce **Extensions\\\\Microsoft Dynamics" aplanke yra plėtinių paketų, kurie yra aplanke C:\\ Program Files\\ 365\\ 10.0**. Jei pakuotė yra, ten turi būti **EKA** aplankas, kuriame yra deklaracija.

Jei EKA **aplanko nėra**, patvirtinkite, kad "Store Commerce" projektas tinkamai nurodo pardavimo vietos (EKA) plėtinio projektą. Patikrinkite projekto nuorodos maršrutą ir įsitikinkite, kad jis yra. 

Toliau pateiktame pavyzdyje diegimo programos projekte yra problemų dėl nurodytų plėtinio projektų.

![Netinkama parduotuvės "Commerce Installer" projekto nuoroda.](media/ReferenceNotValid.png)

Jei plėtinio projekto nuoroda tinkamai įtraukta, diegimo programos projekte nebus jokio perspėjimo ar priklausomybės problemos, kaip parodyta toliau pateiktame pavyzdyje.

!["Store Commerce Installer" projekto nuoroda tinkama.](media/ReferenceValid.png)
