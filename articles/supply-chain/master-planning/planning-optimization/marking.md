---
title: Inventoriaus ženklinimas su „Planning Optimization“
description: Šiame straipsnyje pateikiama informacija apie pasirinktis, kurias galima naudoti žymint atsargas patvirtintiuose užsakymuose, kai naudojate planavimo optimizavimą.
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
ms.openlocfilehash: 2f1902ba76db59b61b0437eb3cd68ee94018b7c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844474"
---
# <a name="inventory-marking-with-planning-optimization"></a>Inventoriaus ženklinimas su „Planning Optimization“

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie pasirinktis, kurias galima naudoti žymint atsargas patvirtintiuose užsakymuose, kai naudojate planavimo optimizavimą.

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