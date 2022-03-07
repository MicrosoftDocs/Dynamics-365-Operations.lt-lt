---
title: Vidinės įmonės pardavimo užsakymo kūrimas vidiniam naudojimui
description: Šioje temoje paaiškinama, kaip sukurti vidinės įmonės pardavimo užsakymą vidiniam naudojimui
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0718a1560ec42df2a0a12e8b81484aa3be46d2d8
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548420"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Vidinės įmonės pardavimo užsakymo kūrimas vidiniam naudojimui

[!include [banner](../../includes/banner.md)]

Dažniausiai, vidinės įmonės pardavimo užsakymas automatiškai kuriamas pagal vidinės įmonės pirkimo užsakymą. Taip pat galite neautomatiniu būdu sukurti vidinės įmonės pardavimo užsakymą, kuris tada sugeneruoja vidinės įmonės pirkimo užsakymą vidinės įmonės kliento juridiniame subjekte.

![Vidinės įmonės vidinis pardavimo procesas](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Vidinės įmonės pardavimo užsakymo kūrimas neautomatiniu būdu

Atlikite šiuos veiksmus naudodami B juridinį subjektą, kaip parodyta pavyzdyje.

1. Eikite į **Gautinos sumos \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Pardavimo užsakymas** pardavimo užsakymui sukurti.
1. Puslapyje **Kurti pardavimo užsakymą** pasirinkite kliento kodą. „FastTab“ **Bendri** patikrinkite, ar pažymėtas **vidinės įmonės** žymės langelis. Tai nurodo, kad pasirinktas klientas yra vidinės įmonės klientas.
1. Įveskite arba modifikuokite informaciją, tada rinkitės **Gerai** ir tada užpildykite užsakymo eilutes kaip įprasta.

    **Pristatymo adreso** lauko vertė nukopijuojama iš vidinės įmonės pardavimo užsakymo antraštės į vidinės įmonės pirkimo užsakymo antraštę. Lauko **Prekės numeris** vertė, įskaitant produkto dimensijas, ir lauko **Pristatymo data** bei **Valiutos kodas** vertės nukopijuojamos iš vidinės įmonės pardavimo užsakymo eilučių į vidinės įmonės pirkimo užsakymo eilutes.

1. Norėdami peržiūrėti susijusį **Vidinės įmonės** pirkimo užsakymą, užsakymo antraštėje.
1. Norėdami peržiūrėti informaciją apie **vidinės įmnės** prekybos atsargas, užsakymo eilutėse pasirinkite Vidinės įmonė.

> [!TIP]
> Vidinės įmonės pardavimo užsakymus galite peržiūrėti **vidinės įmonės** užsakymų puslapyje.

> [!NOTE]
> Jei dirbate su vidinę įmonėje, rekomenduojame išvalyti žymės langelį **Naikinti užsakymą išrašius SF** žymimą laukelį **gautinų sumų parametrų** puslapyje. Kitu atveju susijęs pirkimo užsakymas panaikinamas. Jei dirbate su vidinę įmonėje, rekomenduojame **Naikinti pirkimo užsakymą po SF** žymimą laukelį **Mokėtinų sumų parametrų** puslapyje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
