---
title: Sukurkite vidinę įmonės prekybą
description: Šioje temoje paaiškinama, kaip nustatyti vidinės įmonės prekybą
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
ms.openlocfilehash: 75d6679152a056f6883658911f93464252e5fe87
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548413"
---
# <a name="set-up-intercompany-trade"></a>Sukurkite vidinę įmonės prekybą

[!include [banner](../../includes/banner.md)]

Kad „Microsoft Dynamics 365 Supply Chain Management“ galėtų paleisti vidinės įmonės prekybą, turite nustatyti, kad klientai ir tiekėjai paleistų vidinės įmonės prekybą. Turite taip pat nustatyti mokėtinas, gautinas sumas, tiekimo ir šaltinio bei pardavimo ir rinkodaros vertes.

## <a name="before-you-set-up-intercompany-trade"></a>Prieš nustatant vidinės įmonės prekybą

Prieš nustatydami vidinės įmonės prekybą turite nuspręsti, kurie iš jūsų klientų yra vidinės įmonės klientai ir kurie iš jūsų tiekėjų yra vidinės įmonės tiekėjai. Kiekvienam juridiniam subjektui „Microsoft Dynamics 365 Supply Chain Management“ įmonės sąskaitų, kokią prekybos strategiją taikyti vidinės įmonės prekybos ryšiui su tam tikru vidinės įmonės klientu ar tiekėju.

Be to, rekomenduojame jums ir jūsų organizacijai susipažinti su vidinės įmonės parametrais.

- Aptarkite nustatymo pasekmes su vadybininkais, atsakingais už vidinės įmonės prekybą kiekviename juridiniame subjekte.
- Nustatykite atitinkamas kiekvieno juridinio subjekto vertes.

## <a name="set-up-trading-relations"></a>Nustatyti prekybos ryšius

Norėdami nustatyti vidinės įmonės prekybą klientams ir tiekėjams, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkti kliento sąskaitą.
1. Veiksmų srities skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Nurodyti kliento sąskaitos vidinės įmonės nustatymo parametrus. Šie parametrai apima juridinį subjektą, kuriame yra atitinkamas tiekėjas ir tiekėjo sąskaita. Šie parametrai apima kliento tiekėjo subjektą ir sąskaitą, pirkimo užsakymų strategijas, pardavimo užsakymo politimas, sutarčių konvertavimą, pardavimo sutartį bei pirkimo sutarčių strategijas. Taip pat galite nurodyti, ar naudoti duomenų vertes iš kliento sąskaitos, ar iš tiekėjo sąskaitos į kitą juridinį subjektą.
1. Likusiems juridinio subjekto vidinės įmonės klientams pakartokite 1–4 veiksmus.
1. Eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai**.
1. Pasirinkite tiekėjo sąskaitą.
1. Veiksmų srities skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Nurodyti tiekėjo sąskaitos vidinės įmonės nustatymo parametrus. Šie parametrai apima juridinį subjektą, kuriame yra atitinkamas kliento ir kliento sąskaita. Šie parametrai apima kliento tiekėjo subjektą ir sąskaitą, pirkimo užsakymų strategijas, pirkimo užsakymo politimas, sutarčių konvertavimą, pardavimo sutartį bei pirkimo sutarčių strategijas. Taip pat galite nurodyti, ar naudoti duomenų vertes iš tiekėjo sąskaitos, ar iš kliento sąskaitos į kitą juridinį subjektą.
1. Likusiems juridinio subjekto vidinės įmonės tiekėjams pakartokite 6–9 veiksmus.

## <a name="set-up-products"></a>Nustatykite produktus

Norėdami nustatyti vidinės įmonės prekybą klientams ir tiekėjams, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijas tvarkymas \> Produktai \> Visi produktai ir produkto šeimininkai**.
1. Apibrėžkite produktus, išleidžiamus juridiniams subjektams, kuriuose norite atlikti vidinės įmonės prekybą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
