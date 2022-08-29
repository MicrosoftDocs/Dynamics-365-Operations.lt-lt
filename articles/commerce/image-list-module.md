---
title: Vaizdų sąrašo modulis
description: Šiame straipsnyje aprašomi vaizdų sąrašo moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: e89624a98d3cbdd861391e994386ae57d2c38aa0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269841"
---
# <a name="image-list-module"></a>Vaizdų sąrašo modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi vaizdų sąrašo moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Vaizdų sąrašo modulis gali būti naudojamas norint lengvai įtraukti vaizdų rinkinį (masyvą) į svetainės puslapius. Kiekvienas masyvo vaizdas gali būti sukonfigūruotas naudojant paragrafo tekstą ir saito URL. Vaizdų sąrašo modulis geriausiai tinka prekės ženklo logotipams arba sąrašui, kuriame yra logotipų, rodyti.

> [!IMPORTANT]
> - Vaizdų sąrašo modulis galimas „Commerce” modulių bibliotekoje kaip 10.0.20 „Dynamics 365 Commerce” versijos dalis.
> - Vaizdų sąrašo modulis rodomas „Adventure Works” temoje.

Šioje iliustracijoje pateikiamas pavyzdys, kuriame vaizdų sąrašo modulis rodo teksto sąrašą, kuriame yra logotipų „Adventure Works” „verslas vartotojui” (B2C) svetainės puslapyje.

![Vaizdų sąrašo modulio, kuriame rodomas teksto sąrašas su logotipais, pavyzdys](./media/Image_list.PNG)

Šioje iliustracijoje pateikiamas pavyzdys, kuriame vaizdų sąrašo modulis rodo prekės ženklų logotipus „Adventure Works” „verslas verslui” (B2B) svetainės puslapyje.

![Vaizdų sąrašo modulio, kuriame rodomi prekės ženklo logotipai, pavyzdys](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Vaizdų sąrašo modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė       | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Vaizdų sąrašo modulio teksto antraštė. |
| Vaizdų sąrašas    | Vaizdai, tekstas ir URL | Kiekviena masyvo prekė yra vaizdas, einantis kartu su paragrafo tekstu ir URL. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Vaizdų sąrašo modulio įtraukimas į naują puslapį

Norėdami į naują puslapį įtraukti vaizdų sąrašo modulį ir nustatyti reikiamas ypatybes „Commerce” svetainių daryklėje, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir atidarykite jūsų svetainės pagrindinio puslapio rinkodaros šabloną (arba sukurkite naują rinkodaros šabloną).
1. Numatytojo **puslapio** pagrindiniame atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite vaizdo sąrašo **modulį**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir atidarykite pagrindinį svetainės puslapį (arba sukurkite naują pagrindinį puslapį naudodami rinkodaros šabloną).
1. Numatytojo **puslapio** pagrindiniame atrinkinyje pasirinkite elipsės mygtuką (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite sąrašą **Vaizdas**, tada pasirinkite **Gerai**.
1. Vaizdų sąrašo modulio ypatybių srityje pridėkite antraštę (pavyzdžiui, **Mūsų prekės ženklai**).
1. Įtraukite vaizdų sąrašo elementą ir nurodykite paveikslėlį, paragrafo tekstą ir nukreipimo URL.
1. Jei reikia, įtraukite ir sukonfigūruokite papildomus vaizdų sąrašo elemento modulius.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[„Adventure Works” tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
