---
title: Vidinės įmonės užsakymų mokesčių nustatymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti vidinės įmonės užsakymų mokesčius
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7b84c0bac6c31139170a99afc65cd08d70bd018e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885847"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Vidinės įmonės užsakymų mokesčių nustatymas

[!include [banner](../../includes/banner.md)]

Galite nustatyti mokesčius, įtrauktinus į vidinės įmonės užsakymus. Kai į vidinės įmonės pardavimo užsakymą įtraukiamas mokestis, jis automatiškai sinchronizuojamas su vidinės įmonės pirkimo užsakymu. Tai veikia abiem atvejais – iš vidinės įmonės pardavimo užsakymo į pirkimo užsakymą ir atvirkščiai.

Norėdami įtraukti pelną į vidinės įmonės pardavimo užsakymą, taip pat galite naudoti mokesčius, apibrėždami mokestį kaip vidinės įmonės procentą.

Kai nustatote vidinės įmonės užsakymams taikytinus mokesčius, leidžiate apskaičiuoti vidinės įmonės pardavimo užsakymo vidaus pelną iš pradinio pardavimo užsakymo grynosios sumos. Galite norėti tai padaryti, jei jūsų vidinės įmonės tiekėjas parduoda jums savikaina. Toliau pateiktoje procedūroje aprašoma, kaip tai padaryti vidinės įmonės klientams. Galite naudoti tą pačią procedūrą tiekėjams.

1. Pasirinkite **Gautinos sumos \> Nustatymas \> Keitimai \> Kliento keitimo grupės**.
1. Sukurkite mokesčių grupę.
1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**. Pasirinkite kliento sąskaitos nuorodą. Veiksmų juostoje pasirinkite **Kliento** skirtuką ir tada pasirinkite **Pardavimo užsakymas** „FastTab“.
1. Rinkitės **Regatuoti** veiksmų srityje, kad būtų galima redaguoti lauką. Skirtuke **Mokesčių grupės** pasirinkite vidinės įmonės mokesčių grupę, kurią nustatėte atlikdami 2 veiksmą.
1. Pasirinkite **Gautinos sumos \> Nustatymas \> Mokesčiai \> Automatinės išlaidos**.
1. Užpildydami reikiamus laukus, nustatykite mokesčius.
1. Skirtuke **Kliento sąsaja** pasirinkite vidinės įmonės mokesčių grupę, kurią nustatėte atlikdami 2 veiksmą.
1. „FastTab“ **Eilutės** laukelyje **Kategorija** rinkitės **Vidinės įmonės procentas**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
