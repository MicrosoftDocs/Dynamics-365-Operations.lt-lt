---
title: Nustatykite išskaitomo mokesčio kodus TDS mokesčių tipui
description: Šioje temoje paaiškinama, kaip nustatyti (TDS) išskaitomo periodinio mokesčio kodus.
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
ms.openlocfilehash: add91eaef2ad091df7fd45e3de2dfe3993e6d62fdcbbcfcf95a7fc4953189239
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754884"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Nustatykite išskaitomo mokesčio kodus TDS mokesčių tipui

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti (TDS) išskaitomo periodinio mokesčio kodus.

1. Eikite į **Mokestis \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Išskaitomo mokesčio kodai**.

    [![Išskaitomų mokesčių kodų puslapis.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Norėdami sukurti **TDS** išskaitomo mokesčio kodą, veiksmų srityje pasirinkite Naujas ir įveskite reikiamą informaciją.
3. Norėdami mokesčių kodą klasifikuoti kaip TDS mokesčio kodą, skirtuko **Bendra** „FastTab" **mokesčio tipo** lauke pasirinkite **TDS**.
4. Į lauką **Sudengimo laikotarpis** rinkitės TDS sudengimo laikotarpį TDS mokesčių kodui.
5. Lauke **Pagrindinė sąskaita** pasirinkite DK sąskaitą, į kurią turėtų būti registruojama TDS suma.
6. Gautinų **sumų sąskaitos** lauke pasirinkite gautinų sumų sąskaitą, į kurią turėtų būti registruojama TDS suma, atskaityta pardavimo operacijose.

    Laukas **Šaltinis** automatiškai nustatomas į **Bendros sumos procentas**, todėl vertės keisti negalima.

    > [!NOTE]
    > TDS mokesčio tipo mokesčių kodų kilmės negalima nustatyti kaip **Grynosios sumos procentinė** išraiška.

7. Lauke **Išskaitomo mokesčio komponentas** pasirinkite TDS mokesčio komponentą TDS mokesčių kodui.
8. Veiksmų juostoje rinkitės **Vertės** norėdami atidaryti **Išskaitomo mokesčio vertės** puslapį.
9. Lauke **Pradžios data** įveskite TDS vertės pradžios datą. Lauke **Iki datos** įveskite pabaigos datą.

    > [!NOTE]
    > Laukeliai **minimali riba**, **Viršutinė riba** ir **Neįtraukti %** laukeliai nėra prieinami mokesčių TDS mokesčio tipo kodams.

10. Lauke **Reikšmė** įveskite procentinę TDS dalį TDS mokesčių kodui.
11. Norėdami grįžti į **išskaitomo mokesčio vertes** laikotarpių puslapį uždarykite **išskaitomo mokesčio kodų** puslapį.

    > [!NOTE]
    > Išskaitomo mokesčio kodų puslapio mygtuko **Ribos** negalima naudoti su TDS **mokesčio tipo mokesčių** kodais.

12. Uždarykite puslapį.
