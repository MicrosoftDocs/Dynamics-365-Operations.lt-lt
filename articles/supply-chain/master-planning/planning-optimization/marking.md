---
title: Atsargų žymėjimas
description: Šiame straipsnyje pateikiama informacija apie pasirinktis, kurias galima naudoti žymint atsargas patvirtintiuose užsakymuose.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740609"
---
# <a name="inventory-marking"></a>Atsargų žymėjimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie pasirinktis, kurias galima naudoti žymint atsargas patvirtintiuose užsakymuose.

*Ženklinimas* naudojamas susieti paklausą ir pasiūlą. Jis atspindi *fiksavimą*, kuris nurodo, kaip pagrindinis planavimas tikisi padengti paklausą. Planavimo požiūriu, pagrindinis skirtumas tas, kad ženklinimas yra pastovesnis nei fiksavimas.

Ženklinimas buvo įvestas siekiant palaikyti specialius kaštų scenarijus pirmajam patenkančiam ir pirmajam išeinančiam (FIFO) ir paskutiniam įeinančiam ir pirmam išeinančiam (LIFO). Nepaisant to, dabar jis taip pat naudojamas kai kuriuose ne kaštų scenarijuose. Ženklinimas tarp pasiūlos ir paklausos yra pasirenkamas ir beveik pastovus. Ženklinimas gali būti pašalinamas rankiniu būdu vartotojo arba vykdant pardavimo užsakymo eilutės sprogimą, kai **Ženklinimo pašalinimo** parinktis pasirenkama.

Fiksavimą valdo pagrindinis planavimas aprėpties metu susiejant paklausą su būtina pasiūla. Fiksavimą galima naujinti kiekvieno planavimo vykdymo metu siekiant optimizuoti pasiūlą, kuri būtina padengti paklausą. Kai pagrindinis planavimas naujina fiksavimo informaciją, jis laikosi esančio ženklinimo.

Fiksavimas prasideda įskaitant atitinkamą ženklinimą, turimas rezervacijas ir užsakymo rezervacijas tolesne seka:

1. Ženklinimas tarp pasiūlos ir paklausos
1. Turimo rezervacijos
1. Užsakymo rezervacijos

Kai patvirtinate suplanuotą užsakymą, **Patvirtinimo** teksto laukelis rodo **Naujinto ženklinimo** laukelį, kurį naudojate siekiant nustatyti ženklinimo parinktis užsakymams sukurtiems patvirtinimo metu. Pasirinkite vieną iš šių reikšmių:

- *Ne* – Joks inventoriaus ženklinimas nėra taikomas.
- *Standartinis* – Inventoriaus ženklinimas yra naujinamas pagal fiksavimą. Reikalavimo užsakymas (paklausa) yra ženklinamas pagal įgyvendinimo užsakymą (pasiūlą). Jei keletas kiekių lieka įgyvendinimo užsakyme, jis neženklinamas ir atitinkama informacija paliekama tuščia. Pavyzdžiui, jei pardavimo užsakymas 100 ea yra fiksuojamas pagal pirkimo užsakymą 150 ea, atitinkama informacija bus priskirta tik pardavimo užsakymui.
- *Išplėstas* – Tiek reikalavimo užsakymas (paklausa), tiek įgyvendinimo užsakymas (pasiūla) bus paženklinti nepriklausomai nuo bet kokio kiekio, kuris lieka įgyvendinimo užsakyme. Pavyzdžiui, jei pardavimo užsakymas 100 ea yra fiksuojamas pagal pirkimo užsakymą 150 ea, atitinkama informacija bus priskirta tiek pardavimo užsakymui, tiek pirkimo užsakymui.
- *Vieno lygio standartas* – naudojamas vieno lygio žymėjimas. Vieno lygio žymėjimas žymi tik pagrindinę prekę, o ne jos komplektavimo specifikacijos (KS) komponentus. Todėl patvirtię galite palikti gamybos užsakymų komponentų priskyrimus kintamus. Naudojant vieno lygio žymėjimą sistema gali optimizuoti, kad sistema gali atlikti paskutiniųjų minučių poreikio pokyčius. Standartiniu *vieno* lygio žymėjimu poreikio užsakymai žymimi pagal jų įvykdymo užsakymus, bet įvykdymo užsakymai nepažymėti, jei yra likęs kiekis.
- *Išplėstinis vieno* lygio – naudojamas vieno lygio žymėjimas. Išplėstinio *vieno* lygio žymėjimo metu poreikio užsakymai žymimi pagal jų įvykdymo užsakymus, o įvykdymo užsakymai visada žymimi, neatsižvelgiant į tai, ar liko kiekio.

Norėdami nustatyti numatytąją žymėjimo pasirinktį savo sistemai, eikite į Bendrojo **planavimo \> nustatymo \> bendrojo planavimo parametrus**. Tada standartinio atnaujinimo **skirtuke** nustatykite **pageidaujamą** pasirinkties atnaujinimo žymėjimo lauką.

> [!NOTE]
> Vieno *lygio standartinio* ir *vieno lygio išplėstinės* *pasirinktys* galimos tik jei jūsų sistemoje įgalinta gamybos pagal užsakymą tiekimo automatizavimo funkcija. Daugiau informacijos apie šią funkciją ir apie tai, kaip ją įgalinti, ieškokite gamybos [pagal užsakymą tiekimo automatizavimą](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
