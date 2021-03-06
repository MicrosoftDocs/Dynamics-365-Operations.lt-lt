---
title: Parametrų mokėtinos sąskaitose ir gautinose sąskaitose TDS nustatymas
description: Šioje temoje aiškinama, kaip nustatyti mokėtinų sumų ir gautinų sumų parametrus, kad būtų palaikomi šaltinio (TDS) atskaitymai.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023448"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Parametrų mokėtinos sąskaitose ir gautinose sąskaitose TDS nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip nustatyti mokėtinų sumų ir gautinų sumų parametrus, kad būtų palaikomi šaltinio (TDS) atskaitymai.

1. Eikite į **Mokestis \> Sąranka \> Parametrai \> Gautinų sumų parametrai**.
2. Skirtuke **Naujinimai** pasirinkite **Naujinti užsakymo eilutes**, kad atidarytumėte dialogo langą **Naujinti užsakymo eilutes**.
3. Sekcijos **TDS grupė** lauke **TDS grupės naujinimas** nurodykite metodą, kuris bus naudojamas TDS grupei atnaujinti eilutės lygiu. Šis parametras naudojamas atnaujinant TDS grupę užsakymo antraštėje. Galimos toliau nurodytos parinktys:

    - **Niekada** – TDS grupė neatnaujinama užsakymo eilutėse, kai ji atnaujinama užsakymo antraštėje.
    - **Visada** – TDS grupė automatiškai naujinama užsakymo eilutėse, kai ji atnaujinama užsakymo antraštėje.
    - **Raginimas** – vartotojai gauna pranešimą, raginantį atnaujinti užsakymo eilučių TDS grupę.
4. Pasirinkite **Gerai**.

    [![Dialogo langas Atnaujinti užsakymo eilutes](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Eikite į **Mokestis \> Sąranka \> Parametrai \> Gautinų mokėtinų sumų parametrai**.
6. Skirtuko **Bendra** „FastTab“ **Skaidymas pagal pristatymo informaciją** nustatykite parinktį **Produkto gavimo kvitas** kaip **Taip,** kad užregistruotumėte ir padalintumėte produkto gavimo kvitą, kuriame yra skirtingi pristatymo adresai ir mokesčių sąskaitų numeriai (BLSK). Jei ši pasirinktis nustatyta kaip **Ne**, negalite registruoti pirkimo važtaraščio, kuriame yra skirtingi pristatymo adresai ir BLSK.
7. Nustatykite parinktį **SF** kaip **Taip**, kad užregistruotumėte ir padalintumėte pirkimo SF, kurioje yra skirtingi pristatymo adresai ir BLSK.

    [![Skaidyti pagal „FastTab“ pristatymo informacija](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Uždarykite puslapį.
