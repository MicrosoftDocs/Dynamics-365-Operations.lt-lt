---
title: Teksto bloko modulis
description: Šiame straipsnyje aprašomi teksto blokavimo moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270488"
---
# <a name="text-block-module"></a>Teksto bloko modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi teksto blokavimo moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Teksto bloko modulis yra modulis, kuris naudojamas teksto turiniui pridėti. Šis turinys gali būti informacinis arba reklaminis.

Teksto bloko moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje. Jie yra atskiri moduliai, nepriklausantys nuo puslapio konteksto ar kitų modulių.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Teksto bloko modulių pavyzdžiai el. prekyboje

Teksto bloko modulius galima naudoti toliau nurodytais būdais.

* Norint produktų išsamios informacijos puslapyje parodyti produktų ypatybes.
* Informaciniais tikslais bet kuriame puslapyje. Pavyzdžiui, juos naudojant galima paaiškinti lojalumo programų privalumus, aprašyti siuntimo ir grąžinimo strategijas, atsakyti į dažnai užduodamus klausimus arba pateikti turinio „apie mus“.
* Norint produktų išsamios informacijos puslapyje įtraukti pasirinktinių pranešimų. (Pavyzdžiui, „Didesni, nei 50 USD, užsakymai pristatomi nemokamai“).
* Norint produktų išsamios informacijos puslapiuose, krepšelio puslapiuose, pirkimo užbaigimo puslapiuose ir kituose puslapiuose įtraukti informaciją apie atsakomybės atsisakymą ir kontaktinę informaciją (pavyzdžiui, „Siunčiant ir grąžinant prekes taikomos parduotuvės strategijos“).

Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio teksto bloko modulio pavyzdys.

![Teksto bloko modulio pavyzdys.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Teksto bloko modulio ypatybės

| Ypatybės pavadinimas     | Reikšmė                                            | Aprašas |
|-------------------|--------------------------------------------------|-------------|
| Raiškusis tekstas         | Raiškusis tekstas                                        | Pastraipos tekstas. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas. |
| Pasirinktinis klasės pavadinimas | Pakopinio stiliaus aprašų (CSS) klasės pavadinimas        | Pasirinktinės CSS klasės, kurią kūrėjas teikia formatuoti šį modulį, pavadinimas. Klasės pavadinimas turi būti nurodytas temų pakete. |
| Šrifto dydis         | **Mažas**, **Vidutinis**, **Didelis** arba **X dydžio** | Turinio šrifto dydis. |

## <a name="add-a-text-block-module-to-a-page"></a>Teksto bloko modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti teksto bloko modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lange **Naujas šablonas** prie šablono **pavadinimo** įveskite **turinio šabloną**.
1. Teksto atminties **atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite numatytąjį puslapio **modulį**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį**, po Puslapio **pavadinimas** įveskite Turinio **puslapį ir** pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną** pasirinkite **Turinio šablonas** ir Pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**. 
1. Naujo puslapio **pagrindiniame** atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio modulio ypatybių srityje nustatykite ypatybę **Plotis** į **Užpildyti konteinerį**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Teksto blokas**, tada – **Gerai**. 
1. Teksto bloko modulio ypatybių srityje įtraukite tekstą į lauką **Raiškusis tekstas**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Reklaminės juostos modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Turinio bloko modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
