---
title: Tikrinti vidinės įmonės užsakymo kainų nesutapimus
description: Šiame straipsnyje paaiškinama, kaip patikrinti vidinės įmonės užsakymo kainų nesutapimų
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ca27e86545ba8179c595e55487dbbf49cd9ec528
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890689"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Tikrinti vidinės įmonės užsakymo kainų nesutapimus

[!include [banner](../../includes/banner.md)]

Šią procedūrą galite naudoti, norėdami vidinės įmonės užsakymuose patikrinti, ar nėra kainų nesutapimų.

1. Eikite į **Įsigijimo ir pirkimo užsakymo \>periodinį \>išvalymo \> patikrinti vidinės įmonės užsakymo kainų nesutapus**.
1. Jei reikia, nustatykite paketinę užduotį, tada rinkitės **Gerai**, kad galėtumėte tikrinti vidinės įmonės pardavimo ir pirkimo užsakymų kainas ir nuolaidas. Jei formą norite uždaryti neatlikę patikrinimo, rinkitės **Atšaukti**.

    > [!TIP]
    > Jei yra sinchronizavimo arba kainų problemų, jos bus pateiktos rodomame informaciniame pranešime. Nuorodos informaciniame pranešimą galite išspausdinti.

1. Informaciniame pranešime du kartus spustelėkite reikiamą eilutę, kad atidarytumėte dabartinį juridinį subjektą. Atidarykite susijusio juridinio subjekto užsakymą pasirinkdami **Vidinė įmonė** ir tada **vidinės įmonės pirkimo užsakymą** ar **vidinės įmonės pardavimo užsakymą**.

    > [!NOTE]
    > Kaip leisti atnaujinti vidinės įmonės užsakymą:
    >
    > 1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
    > 1. Veiksmų srities skirtuke **Bendra** rinkitės **Vidinė įmonė**.
    > 1. Puslapyje **Vidinės įmonės** rinkitės **Pirkimo užsakymo strategijos** ar **Pardavimo užsakymo strategijos**.
    > 1. Abiejuose **srityse pasirinkite Leisti redaguoti kainą** ir **Leisti nuolaidos redagavimą**.

1. Atidarykite reikiamą vidinės įmonės užsakymą, kuriame norite laikyti kainą.
1. Kiekvienoje užsakymo eilutėje pakeiskite eilutės lauką **Vieneto kaina** o tada pakeiskite jo reikšmę atgal į buvusią. Pakeiskite eilutės lauką **Nuolaida** į priekį ir atgal bei pakeiskite susijusius laukus **Pirkimų mokesčiai** ar **Pardavimų keitimai** laukelius atgal ir pirmyn. Šis verčių keitimas pirmyn ir atgal suaktyvins kainų, nuolaidų ir papildomų išlaidų sinchronizavimą iš šios vidinės įmonės užsakymo eilutės į nurodytą vidinės įmonės užsakymo eilutę taip, kad jos bus automatiškai sulygiuotos.

    > [!NOTE]
    > Šis sinchronizavimas galimas, tik jei vidinės įmonės pardavimo užsakymui nebuvo išrašyta SF. Jei vidinės įmonės pardavimo užsakymui buvo užregistruota SF ir sukurtas kliento SF žurnalas, pakeitimai turi būti atlikti tiesiogiai vidinės įmonės pirkimo užsakymo eilutėse nustatant kainas, nuolaidas ir papildomas išlaidas, lygias esančioms vidinės įmonės kliento SF žurnale. Jei tai nepadaroma, vidinės įmonės pirkimo užsakymui negali būti užregistruota SF, nes bus užsakymo sumų neatitikimas.

1. Kartokite procedūrą, kol visi vidinės įmonės pirkimo ir pardavimo užsakymai bus sinchronizuoti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
