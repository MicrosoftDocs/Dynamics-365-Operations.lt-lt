---
title: Inventoriaus ženklinimas su „Planning Optimization“
description: Šiame skyriuje pateikta informacija apie parinktis, kurios yra prieinamos inventoriaus ženklinimui patvirtintuose užsakymuose jums naudojant „Planning Optimization“.
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
ms.openlocfilehash: 8d06527d125837b056729574517ca5ed6738fcff
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468362"
---
# <a name="inventory-marking-with-planning-optimization"></a>Inventoriaus ženklinimas su „Planning Optimization“

[!include [banner](../../includes/banner.md)]

Šiame skyriuje pateikta informacija apie parinktis, kurios yra prieinamos inventoriaus ženklinimui patvirtintuose užsakymuose jums naudojant „Planning Optimization“.

*Ženklinimas* naudojamas susieti paklausą ir pasiūlą. Jis atspindi *fiksavimą*, kuris nurodo, kaip pagrindinis planavimas tikisi padengti paklausą. Planavimo požiūriu, pagrindinis skirtumas tas, kad ženklinimas yra pastovesnis nei fiksavimas.

Ženklinimas buvo įvestas siekiant palaikyti specialius kaštų scenarijus pirmajam patenkančiam ir pirmajam išeinančiam (FIFO) ir paskutiniam įeinančiam ir pirmam išeinančiam (LIFO). Nepaisant to, dabar jis taip pat naudojamas kai kuriuose ne kaštų scenarijuose. Ženklinimas tarp pasiūlos ir paklausos yra pasirenkamas ir beveik pastovus. Ženklinimas gali būti pašalinamas rankiniu būdu vartotojo arba vykdant pardavimo užsakymo eilutės sprogimą, kai **Ženklinimo pašalinimo** parinktis pasirenkama.

Fiksavimą valdo pagrindinis planavimas aprėpties metu susiejant paklausą su būtina pasiūla. Fiksavimą galima naujinti kiekvieno planavimo vykdymo metu siekiant optimizuoti pasiūlą, kuri būtina padengti paklausą. Kai pagrindinis planavimas naujina fiksavimo informaciją, jis laikosi esančio ženklinimo.

Fiksavimas prasideda įskaitant atitinkamą ženklinimą, turimas rezervacijas ir užsakymo rezervacijas tolesne seka:

1. Ženklinimas tarp pasiūlos ir paklausos
1. Turimo rezervacijos
1. Užsakymo rezervacijos

Kai patvirtinate suplanuotą užsakymą, **Patvirtinimo** teksto laukelis rodo **Naujinto ženklinimo** laukelį, kurį naudojate siekiant nustatyti ženklinimo parinktis užsakymams sukurtiems patvirtinimo metu. Pasirinkite vieną iš šių reikšmių:

- **Ne** – Joks inventoriaus ženklinimas nėra taikomas.
- **Standartinis** – Inventoriaus ženklinimas yra naujinamas pagal fiksavimą. Reikalavimo užsakymas (paklausa) yra ženklinamas pagal įgyvendinimo užsakymą (pasiūlą). Jei keletas kiekių lieka įgyvendinimo užsakyme, jis neženklinamas ir atitinkama informacija paliekama tuščia. Pavyzdžiui, jei pardavimo užsakymas 100 ea yra fiksuojamas pagal pirkimo užsakymą 150 ea, atitinkama informacija bus priskirta tik pardavimo užsakymui.
- **Išplėstas** – Tiek reikalavimo užsakymas (paklausa), tiek įgyvendinimo užsakymas (pasiūla) bus paženklinti nepriklausomai nuo bet kokio kiekio, kuris lieka įgyvendinimo užsakyme. Pavyzdžiui, jei pardavimo užsakymas 100 ea yra fiksuojamas pagal pirkimo užsakymą 150 ea, atitinkama informacija bus priskirta tiek pardavimo užsakymui, tiek pirkimo užsakymui.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]