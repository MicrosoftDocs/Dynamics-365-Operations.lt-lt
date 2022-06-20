---
title: Vidinės įmonės prekybos tiekėjų, klientų ir prekių nustatymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti vidinės įmonės prekybos tiekėjus, klientus ir prekes
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
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945761"
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
1. Nustatę vidinės įmonės parametrus, uždarykite vidinės **įmonės puslapį, kad** grįžkite prie pasirinktos kliento informacijos.
1. Išplėskite **išsamios informacijos "** FastTab" ir nustatykite **Vidinės įmonės užsakymų kūrimas kaip** *Taip*. Jei norite, kad užsakymai būtų pristatomi tiesiogiai klientams, nustatykite **Tiesioginį pristatymą** kaip *Taip*.

    > [!NOTE]
    > Jei jūsų organizacija kai kurias prekes saugo ir pristato klientams, tada tikriausiai nenorėsite vidinės įmonės užsakymų kurti automatiškai, nepaisydami to, net jei turite reikiamos prekės atsargų, ar ne. Norėdami išjungti automatinį prekių, kurių atsargų kartais turite, užsakymų generavimą, **nustatykite Vidinės įmonės užsakymus kaip** *Ne*.

1. Jei norite leisti netiesiogiai kurti papildomas pardavimo užsakymo eilutes, nustatykite Sukurti **netiesioginio užsakymo eilutes kaip** *Taip*. Vartotojas gali pridėti vidinės įmonės pardavimo užsakymo eilutes prie pradinio pardavimo užsakymo.

> [!WARNING]
> Jei leisite kurti užsakymo eilutes netiesiogiai, kartu leisite ir visus pradinio pardavimo užsakymo papildymus, kuriuos rasite vidinės įmonės pardavimo užsakyme. Kiekvienas papildymas apdorojamas klientui ir pridedamas prie užsakymo ir SF. Be to, visi su pardavimu susiję dokumentai spausdinami ir registruojami automatiškai. Vartotojai neįspėti apie papildymą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
