---
title: Sinchronizuoti vidinės įmonės kainas ir nuolaidas
description: Šioje temoje paaiškinamas vidinės įmonės pardavimo ir pirkimo užsakymų kainų ir nuolaidų sinchronizavimas
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
ms.openlocfilehash: a9467e8d06a44cfaab9e3c8ea3944675c3eb8fb5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548414"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Sinchronizuoti vidinės įmonės kainas ir nuolaidas

[!include [banner](../../includes/banner.md)]

Vidinės įmonės pardavimo užsakymo kainos ir nuolaidos visada sinchronizuojamos su vidinės įmonės pirkimo užsakymo nuolaidomis ir kainomis. Kainas ir nuolaidas galite sinchronizuoti su pradiniu pardavimo užsakymu, kad visuose užsakymuose būtų nurodytos tos pačios kainos ir nuolaidos. Tai galite padaryti **vidinės įmonės** puslapyje, kuris naudojamas skirtuko **Bendra** puslapyjė **Visi klientai**, arba **Pardavimo ir rinkodaros** ar iš **Įsigijimo ir pirkimo**.

Laukas **Kaina ir nuolaida** sinchronizuojamas su vidinės įmonės pardavimo užsakymo eilute. Tai reiškia, kad pasirinkdami laukus **Leisti redaguoti kainas** ir **Leisti redagavimo nuolaidas** galite keisti ir tarpusavyje lyginti vidinės įmonės pardavimo ir pirkimo užsakymus. Vidinės įmonės pardavimo užsakymo vieneto kainos, kainos kiekio arba papildomų pardavimo išlaidų pakeitimai nulems kainą, nurodytą vidinės įmonės pirkimo užsakymo eilutėje.

Jei **Leisti redaguoti kainas** ir **Leisti nuolaidų redagavimo** yra įgalinti vidinės įmonės pardavimo užsakyme ar vidinės įmonės pirkimo užsakymą, kainą arba nuolaidą galite keisti neautomatiniu būdu bet kurį užsakymą. Priešingu atveju, jūs negalite.

Jei **Leisti redaguoti kainas** ir **Leisti nuolaidų redagavimo** yra nėra įgalinti vidinės įmonės pardavimo užsakyme, negalite keisti kainos (ar mokesčių) arba nuolaidos vidinės įmonės pardavimo užsakyme.

Jei **Leisti redaguoti kainas** ir **Leisti nuolaidų redagavimo** yra nėra įgalinti vidinės įmonės pirkimo užsakyme, negalite keisti kainos (ar mokesčių) arba nuolaidos vidinės įmonės pirkimo užsakyme.

Jei **Leisti redaguoti kainas** ir **Leisti nuolaidų redagavimo** yra įgalinti vidinės įmonės pikrimo užsakyme ir vidinės įmonės pardavimo užsakyme, galite keisti rankiniu būdu abu užsakymus. Tačiau dėl to gali įatsirasti situacija, kai atnaujinimai, kuriuos atliko vienas asmuo, yra panaikinti tame pačiame užsakyme kito žmogaus kitoje įmonėje.

> [!NOTE]
> Jei **Kainos ir nuolaidos** lauke įgalinote ir vidinės įmonės pirkimo užsakyme, ir vidinės įmonės pardavimo užsakyme, kainos kontroliuoti negalite.

Tam, kad išvengtumėte tokių konfliktų, geriausia yra leisti kainas ir nuolaidas keisti tik vidinės įmonės pardavimo užsakyme arba tik vidinės įmonės pirkimo užsakyme. Tai galite atlikti įgalindami abiejų užsakymų laukus **Leisti redaguoti kainą** ir **Leisti redaguoti nuolaidą**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
