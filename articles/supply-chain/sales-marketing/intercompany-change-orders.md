---
title: Keisti vidinės įmonės užsakymus
description: Šioje temoje paaiškinami vidinės įmonės užsakymai ir grąžinimo keitimai
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
ms.openlocfilehash: 1129794bf0ac6513770f8b2a0eeb7fb6154d7942
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548434"
---
# <a name="change-intercompany-orders"></a>Keisti vidinės įmonės užsakymus

[!include [banner](../../includes/banner.md)]

Jums pakeitus vidinės įmonės pardavimo ar pirkimo užsakymą, atitinkamas pardavimo ar pirkimo užsakymas dukterinėje įmonėje taip pat atspindės šį pokytį.

## <a name="adding-new-lines"></a>Naujų eilučių pridėjimas

Jei pradinis pardavimo užsakymas yra vidinės įmonės užsakymų grandinės dalis arba jei pradinis pardavimo užsakymas yra ne tiesioginis pristatymas, prie vidinės įmonės pardavimo ir pirkimo užsakymų galite pridėti naujų eilučių. Jei pradinis pardavimo užsakymas yra ne tiesioginis pristatymas, galite pridėti ir naujų eilučių. Jei pradinis pardavimo užsakymas yra tiesioginis pristatymas, naujų eilučių prie vidinės įmonės pardavimo ir pirkimo užsakymų galite pridėti tik tada, jei vidinės įmonės parametrų FastTab, **kuris yra pasirinktas** pradinio pardavimo užsakymo laukas **Leisti netiesioginį kūrimą**.

## <a name="changing-prices-and-discounts"></a>Kainų ir nuolaidų keitimas

Jei vidinės įmonės puslapyje pažymėti žymės langeliai **Leisti redaguoti kainą** ir **Leisti nuolaidos redagavimą** žymimi laukeliai yra pasirinkti **Vidinės įmonės** puslapyje.

Jums pakeitus vienos esamos vidinės įmonės pardavimo užsakymo eilutės vieneto kainą, vidinės įmonės pirkimo užsakyme pateikta vieneto kaina taip pat keičiasi.

Jums pakeitus bet kurį vidinės įmonės pardavimo užsakymo eilutės nuolaidos lauką, atnaujina atitinkamus vidinės įmonės pirkimo užsakymo nuolaidos laukus.

## <a name="changing-and-adding-new-charges"></a>Naujų papildomų išlaidų keitimas ir pridėjimas

Jei vidinės įmonės puslapyje pažymėti žymės langeliai **Leisti redaguoti kainą** ir **Leisti nuolaidos redagavimą** žymimi laukeliai yra pasirinkti puslapyje **Vidinė įmonė**.

Jei vidinės įmonės pardavimo užsakymo antraštėje pridedate naują mokestį, o naują mokestį – į vidinės įmonės pardavimo eilutę, abu mokesčiai nukopijuojami į vidinės įmonės pirkimo užsakymą. Todėl vidinės įmonės pardavimo užsakyme ir vidinės įmonės pirkimo užsakyme yra ta pati bendra suma. Papildomos išlaidos niekada nėra kopijuojamos į pradinį pardavimo užsakymą.

## <a name="copying-a-fee"></a>Mokesčio kopijavimas

Norėdami kopijuoti mokestį į pradinį pardavimo užsakymą, sukurkite jį kaip naują pardavimo eilutę; šią naują pardavimo eilutę kurkite naudodami **Paslaugas**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Kiekių keitimas ir vidinės įmonės pirkimo bei pardavimo užsakymų eilučių naikinimas

Keisti kiekį bei naikinti vidinės įmonės pirkimo ar pardavimo užsakymo eilutę galite tik tada, jei eilutė buvo sukurta tiesiogiai formoje **Pardavimo užsakymai** ar **Pirkimo užsakymo** formą. Po šio keitimo vidinės įmonės pirkimo ar pardavimo užsakymas / užsakymo eilutės taps šaltiniu.

## <a name="origins-of-orders-and-order-lines"></a>Užsakymų tipai ir užsakymų eilučių kilmė

Vidinės įmonės užsakymai ir užsakymų eilutės gali būti dviejų būsenų:

- **Išvestinis** – užsakymas buvo automatiškai sukurtas kaip vidinės įmonės užsakymų grandinės dalis.
- **Šaltinis** – užsakymą rankiniu būdu sukūrė vartotojas.

Būsena yra nurodyta vidinės įmonės pirkimo užsakymų ir pardavimo užsakymų antraštėse lauke **Būsena** lauke. Šis laukas yra vidinės **įmonės nustatymų** „FastTab", pardavimo užsakyme ir pirkimo užsakymo nustatymo **Nustatymas**.

Tai **Išvestinės** ir **šaltinio** kilmės taikomos tik vidinės įmonės užsakymams. Tai **Kilmės** todėl kitų pardavimo užsakymų, pirkimo užsakymų bei užsakymo eilučių laukas bus tuščias. Pradiniame pardavimo užsakyme šis laukas taip pat bus tuščias.

## <a name="example-derived-origin"></a>Pavyzdys: išvestinė kilmė

Pradinį pardavimo užsakymą kuriate išoriniam klientui. Šį pardavimo užsakymą sudaro viena užsakymo eilutė. Pagal pagrindinį pardavimo užsakymą kuriamas vieną užsakymo eilutę turintis vidinės įmonės pirkimo užsakymas, pagal kurį kuriamas vidinės įmonės pardavimo užsakymas, kuriame yra viena užsakymo eilutė. Vidinės įmonės pirkimo užsakymo antraštė ir užsakymo eilutė yra automatiškai sukuriamos pagal pradinį pardavimo užsakymą.

Vertė **Kilmės** laukas **Nustatymas** „FastTab“ vidinės įmonės pirkimo užsakyme ir **Vidinės įmonės nustatyme** „FastTab“ vidinės įmonės pardavimo užsakymo antraštėje yra **Išvestas**. Vertė **Kilmė** laukas **Eilutės informacija** pirkimo užsakymo skirtuke ir pardavimo užsakymo eilutės taip pat yra **Išvestas**.

Jei užsakymo eilutės kilmė yra **Išvesta** negalite tiesiogiai jos panaikinti. Užsakytą kiekį taip pat galite keisti tik šaltinyje, pagal kurį sukurta užsakymo eilutė. Užsakytą kiekį taip pat galite keisti tik šaltinyje, pagal kurį sukurta užsakymo eilutė.

Jei pradinis pardavimo užsakymas ir pradinio pardavimo užsakymo eilutė yra vidinės įmonės užsakymų grandinės dalis, užsakytus kiekius galite keisti naudodami pradinį pardavimo užsakymą bei taip pat galite naikinti pradinio pardavimo užsakymo eilutes.

## <a name="example-source-origin"></a>Pavyzdys: šaltinio kilmė

Jūs sukuriate pirkimo užsakymą vidinės įmonės tiekėjui. Vidinės įmonės pirkimo užsakymas ir užsakymo eilutė yra **Šaltinio** būsenos. Todėl šis vidinės įmonės pirkimo užsakymas bus valdiklis, o automatiniu būdu sukurtas vidinės įmonės pardavimo užsakymas tiekėjo įmonėje bus **Išvestas**.

Be to, užsakymo eilutėje, sukurtoje vidinės įmonės pirkimo užsakyme, pateikti užsakyti kiekiai negali būti keičiami vidinės įmonės pardavimo užsakyme. Užsakymo eilutę galima panaikinti tik iš vidinės įmonės pirkimo užsakymo. Jei prie vidinės įmonės pardavimo užsakymo pridedama nauja eilutė, vidinės įmonės pardavimo užsakymo eilutė bus laikoma sukurta **Šaltinio**.

Kai pradinis pardavimo užsakymas yra vidinės įmonės užsakymų grandinės dalis, naudojant pradinį pardavimo užsakymą visada galima valdyti vidinės įmonės užsakymus ir užsakymų eilutes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
