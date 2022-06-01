---
title: Atnaujinti perkelti biudžetą sumažinus pirkimo užsakymus ir SF
description: Šioje temoje aprašoma, kaip valdyti, kas atsitinka su perkėlu biudžetu, kai pirkimo užsakymai atšaukiami arba mažinami, ir kai SF yra sumažinamos.
author: TaylorVH
ms.date: 02/11/2022
ms.topic: article
ms.search.form: LedgerFund
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2022-02-01
ms.openlocfilehash: 3b0f06b8d5a38252fc8ff6662f3d454adffffe60
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2022
ms.locfileid: "8803050"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Atnaujinti perkelti biudžetą sumažinus pirkimo užsakymus ir SF

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aprašoma, kaip valdyti, kas atsitinka su perkėlu biudžetu, kai pirkimo užsakymai atšaukiami arba mažinami, ir kai SF yra sumažinamos.

Informacijos apie tai, kaip metų gale apdorojami pirkimo užsakymai, ieškokite apdoroti [pirkimo užsakymus metų pabaigoje](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Įjungti arba išjungti SF nuokrypių biudžeto sumažinimą

Kai pirkimo užsakymas atšaukiamas arba sumažinamas, sistema visada gali atnaujinti perkėlimų biudžetą. Tačiau, jei norite atnaujinti perkėlimą biudžeto sumažinus SF, turite įjungti perkėlimų biudžeto mažinimo funkciją, *kai SF su pirkimo užsakymu sumažinama naudojant nuokrypio* priemonę. Administratoriai šią funkciją gali įjungti arba išjungti ieškodami jos funkcijų **[valdymo darbo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** srityje.

## <a name="purchase-order-reductions-and-cancellations"></a>Pirkimo užsakymų sumažinimai ir atšaukimas

*Nepaisant* to, ar sumažinti perkėlimą biudžetą, kai SF sumažinama pagal pirkimo užsakymą, kai įjungta nuokrypio funkcija, perkėlimo biudžetas bus atnaujintas, kai pirkimo užsakymo kvalifikuojimas bus atšauktas arba sumažintas. Galite nustatyti, kad kiekvienos DK lėšos atsakytumėte vienu iš šių būdų:

- Išlaikyti sukurtą perkėlą biudžetą.
- Automatiškai koreguoti perkėlimą biudžetą, kad būtų pašalintos atšauktos arba sumažintos sumos.

Tik pirkimo užsakymo eilutės, kuriose yra paskirstymų su lėšomis, galima atlikti automatinį biudžeto koregavimą. Automatinis biudžeto koregavimas įvyksta, kai pirkimo užsakymas patvirtinamas arba patvirtinamas pirkimo užsakymo sumažinimas.

## <a name="invoice-reductions"></a>SF sumažinimai

Kai sumažinti *perkėlimą* į biudžetą, kai SF prieš pirkimo užsakymą sumažinama su įjungta nuokrypio funkcija, galite nurodyti, ar kiekvienas lėšos turėtų sumažinti perkėlimą, kai SF sumažinama, kartu su kai pirkimo užsakymas sumažinamas arba atšaukiamas. SF turi būti skirta pirkimo užsakymui, turima perkėlusį biudžetą. Sumažinimai apima kainų nuokrypius, mokesčių nuokrypius ir mokesčių nuokrypius. Kai išrašant SF sumažinamas perkelties pirkimo užsakymas, sukuriamas nuokrypis. Kai SF užregistruota, pirkimo užsakymo biudžeto rezervavimas bus sumažintas nuokrypio suma. Priemonė taip pat sukurs automatinį nuokrypio sumos biudžeto koregavimą.

Kai mažinti *perkėlinį* biudžetą, kai SF pagal pirkimo užsakymą sumažinama išjungus nuokrypio priemonę, šiame scenarijuje persiuntimo biudžetas sumažinamas. Todėl likęs nuokrypio sumos perkėlimas į biudžetą paliekamas atgal.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Sukonfigūruokite kiekvieno lėšų atliekamo biudžeto parinktis

Atlikite šiuos veiksmus su kiekvienu DK lėšomis, kurie turėtų sumažinti perkėlinį biudžetą, kai sumažinamas pirkimo užsakymas arba SF.

1. Eikite **į DK \> sąskaitų lėšų \> planą \>**.
1. Pasirinkite lėšas, kurias norite nustatyti.
1. Dalyje **Pirkimo užsakymo metų pabaigos procesas įsitikinkite**, kad parinktis **Perrašyti pasirinktą metų pabaigos parinktį** nustatyta kaip *Taip*.
1. Nustatykite **būseną** Perkeliamas **biudžetas,** kai perkeliamas pirkimo užsakymas atšaukiamas arba sumažinamas, kaip reikalaujate. Parametrai gali šiek tiek skirtis, atsižvelgiant į tai, *ar* jūsų sistemoje įjungta nukrypimo priemonė, kai pirkimo užsakymo SF sumažinama naudojant nuokrypio priemonę.

    - Kai priemonė išjungta, sistema reaguoja tik į atšauktus arba sumažintus pirkimo užsakymus. Parinkties parametrai veikia taip:

        - *Ne* – sistema sukuria biudžeto registro įrašą likusiam atšauktų arba sumažintų pirkimo užsakymų balansui.
        - *Taip* – sistema leidžia atšaukti arba sumažinti pirkimo užsakymus, bet nesukuria biudžeto registro įrašo. Perkelti biudžeto likučius galima naudoti suvartojimui kitais dokumentais.

    - Kai priemonė įjungta, sistema pereis ir į SF nuokrypius, ir atšauktų arba sumažintų pirkimo užsakymų. Parinkties parametrai veikia taip:

        - *Ne* – esant SF nuokrypiams sistema sukuria biudžeto registro įrašą pagal pirkimo užsakymą nuokrypio sumažinimo sumai. Atšaukties arba sumažinto pirkimo užsakymų atveju šis parametras turi tokį patį poveikį išjungus priemonę.
        - *Taip* – kai SF nuokrypiai nustatyti, sistema leidžia sumažinti SF, bet nesukuria biudžeto registro įrašo. Perkelti biudžeto likučius galima naudoti suvartojimui kitais dokumentais. Atšaukties arba sumažinto pirkimo užsakymų atveju šis parametras turi tokį patį poveikį išjungus priemonę.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Pirkimo užsakymo metų pabaigos procesas](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Tvarkyti bendrojo biudžeto lėšų rezervavimus](general-budget-reservation-tasks.md)
- [Fondai viešajame sektoriuje](funds-public-sector.md)
- [Nustatyti viešojo sektoriaus lėšas](tasks/set-up-fund-public-sector.md)
