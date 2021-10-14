---
title: Vidinės įmonės prekybos tiekėjų, klientų ir prekių nustatymas
description: Ši tema paaiškina, kaip nustatyti vidinės įmonės prekybos tiekėjus, klientus ir prekes
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 062b8fe956fef0f8172d26aac3df54b93e1941ef
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548416"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Vidinės įmonės prekybos tiekėjų, klientų ir prekių nustatymas

[!include [banner](../../includes/banner.md)]

Norėdami savo organizaciją parengti vidinės įmonės prekybai, turite nurodyti tiekėjus ir klientus, su kuriais galėsite prekiauti viduje. Tada šiuos tiekėjus ir klientus turite susieti su prekėmis, kurias perkate arba parduodate.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Tiekėjai \> Visi tiekėjai**.
1. Pasirinkti tiekėją, kuris bus apibrėžiamas kaip vidinės įmonės tiekėjas.
1. Veiksmų srities skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Nurodyti tiekėjo sąskaitos vidinės įmonės nustatymo parametrus. Šie parametrai apima kliento juridinį subjektą ir sąskaitą, pardavimo užsakymų strategijas, pirkimo užsakymo strategijas, verčių konvertavimą, pirkimo sutartį bei pardavimo sutarčių strategijas. Taip pat galite nurodyti, ar naudoti duomenų vertes iš tiekėjo sąskaitos, ar iš kliento sąskaitos į kitą juridinį subjektą.
1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. **Išleistų produktų** sąrašo puslapyje pasirinkite prekes, kurias norite priskirti tiekėjui, kad prekes būtų galima naudoti vidinės įmonės prekyboje. Kiekvienoje prekėje atverkite **Išleisto produkto informacija** puslapį. Skirtuke **Pirkimas** laukelyje **Tiekėjas** tipo tiekėjo numeris.
1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkti klientą, kuris bus apibrėžiamas kaip vidinės įmonės klientas.
1. Veiksmų srities skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Nurodyti kliento sąskaitos vidinės įmonės nustatymo parametrus. Šie parametrai apima kliento tiekėjo subjektą ir sąskaitą, pirkimo užsakymų strategijas, pardavimo užsakymo strategijas, verčių konvertavimą, pardavimo sutartį bei pirkimo sutarčių strategijas. Taip pat galite nurodyti, ar naudoti duomenų vertes iš kliento sąskaitos, ar iš tiekėjo sąskaitos į kitą juridinį subjektą.
1. Klientų **puslapyje** ir **SF ir pristatymo** „FastTab", pažymėkite žymės langelį **Kurti vidinės įmonės užsakymus**. Jei norite, kad užsakymai būtų pristatomi tiesiogiai klientams, pažymėkite žymės langelį **Tiesioginis pristatymas**.

    > [!NOTE]
    > Jei jūsų organizacija kai kurias prekes saugo ir pristato klientams, tada tikriausiai nenorėsite vidinės įmonės užsakymų kurti automatiškai, nepaisydami to, net jei turite reikiamos prekės atsargų, ar ne. Norėdami išjungti automatinį prekių, kurių atsargų kartais turite, užsakymų generavimą, nežymėkite **Kurti vidinės įmonės užsakymus** žymimą laukelį.

1. Jei norite leisti netiesiogiai kurti papildomas pardavimo užsakymo eilutes, pažymėkite žymės langelį **Kurti netiesioginio užsakymo** eilutes. Vartotojas gali pridėti vidinės įmonės pardavimo užsakymo eilutes prie pradinio pardavimo užsakymo.

> [!WARNING]
> Jei leisite kurti užsakymo eilutes netiesiogiai, kartu leisite ir visus pradinio pardavimo užsakymo papildymus, kuriuos rasite vidinės įmonės pardavimo užsakyme. Kiekvienas papildymas apdorojamas klientui ir pridedamas prie užsakymo ir SF. Be to, visi su pardavimu susiję dokumentai spausdinami ir registruojami automatiškai. Vartotojai neįspėti apie papildymą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
