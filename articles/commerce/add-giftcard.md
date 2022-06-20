---
title: Dovanų kortelės modulis
description: Šiame straipsnyje aprašomi dovanų kortelių moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cc3d51b9891469b8bb0fa38ae2bcd0b27eee56f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869495"
---
# <a name="gift-card-module"></a>Dovanų kortelės modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi dovanų kortelių moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Dovanų kortelių moduliai yra įprasta mokėjimo forma, naudojama „e-Commerce” operacijose, ir juos galima naudoti pirkimo užbaigimo moduliuose, kad dovanų kortelės būtų priimtos. Dovanų kortelės modulis palaiko „Dynamics 365”, „SVS” ir „Givex” dovanų korteles. „SVS” ir „Givex” dovanų kortelėmis apmokama naudojant „Adyen” mokėjimo paslaugų teikėją. Daugiau informacijos apie išorinių dovanų kortelių, pvz., „SVS” ir „Givex”, palaikymą žr. [Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md).

> [!NOTE]
> „SVS” ir „Givex” dovanų kortelių panaudojimo pirkimo užbaigimo srauto metu palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.11 leidime. 

Galimi du dovanų kortelių moduliai:

- **Dovanų kortelė** – šis modulis gali būti naudojamas pirkimo užbaigimo puslapyje, norint naudoti dovanų kortelę kaip mokėjimo priemonę. 
- **Dovanų kortelės balanso tikrinimas** – šis modulis gali būti naudojamas bet kuriame puslapyje, norint patikrinti dovanų kortelės balansą. Šis modulis pasiekiamas 10.0.14 arba vėlesnio leidimo „Commerce“.

> [!NOTE]
> Dovanų kortelės balanso tikrinimo modulio palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.14 leidime.

Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio dovanų kortelės modulio pavyzdys.

![Dovanų kortelės modulio pavyzdys.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modulio ypatybės

- **Rodyti papildomus laukus** – ši ypatybė nurodo, kuriuos laukus reikia rodyti kartu su dovanų kortelės numeriu, kuris visada rodomas pagal numatytuosius nustatymus, naudojant dovanų korteles. Pavyzdžiui, kai kurios dovanų kortelės palaiko asmeninio identifikacijos numerio (PIN) rodymą, o kitos palaiko PIN ir galiojimo datos rodymą. Taip pat gali būti, kad ši ypatybė nustatyta į Nėra, tokiu atveju būtų rodomas tik dovanų kortelės numeris ir nebūtų jokių papildomų laukų.

    Palaikomos šios vertės:

    - PIN
    - Galiojimo pabaigos data
    - PIN ir galiojimo data 
    - None

- **Įjungti svečių vartotojams** – Kai ši ypatybė įjungta, svečiai vartotojai gali pasinaudoti ar patikrinti balansą dovanų kortelėse. Šiai nuosavybei reikia, kad „Commerce Headquarters" būtų įgalinta anoniminė (svečio) prieiga prie dovanų kortelių. Daugiau informacijos rasite įgalinti [mokėjimus dovanų kortele už svečio išregistravimas](#enable-gift-card-payments-for-guest-checkout).

> [!IMPORTANT]
> Ypatybė **Įgalinti svečiui pasiekiama** pagal „Commerce" 10.0.21 versiją. Tam reikia, kad būtų įdiegta „Commerce“ modulio bibliotekos paketo versija 9.31.

## <a name="site-settings-for-gift-card-modules"></a>Dovanų kortelių modulių svetainės parametrai

„Commerce“ svetainių rengyklės dalyje **Svetainės parametrai \> Plėtiniai** yra dovanų kortelės modulio parametras pavadinimu **Palaikomos dovanų kortelės tipas**. Šis parametras palaiko tris toliau pateiktas reikšmes.
- **„Dynamics 365” dovanų kortelė** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Dynamics 365” dovanų kortelėmis. Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.
- **„SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Givex” ir „SVS” dovanų kortelėmis. Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems ir anoniminiams vartotojams.
- **„Dynamics 365”, „SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti „Dynamics 365”, „Givex” ir „SVS” dovanų kortelėmis. Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.

> [!IMPORTANT]
> Šie parametrai pasiekiami „Dynamics 365 Commerce” 10.0.11 leidime ir reikalingi tik tada, kai reikia „SVS” ar „Givex” dovanų kortelių palaikymo. Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Išplėsti vidines dovanų korteles, skirtas naudoti el. komercijos parduotuvėsfrontėse

Pagal numatytuosius nustatymus vidinės dovanų kortelės nėra optimizuotos naudoti el. „Commerce Storefronts". Todėl prieš leisdami mokėjimui naudoti vidines dovanų korteles, turėtumėte jas konfigūruoti su plėtiniais, kurie padeda jas apsaugoti. Štai dovanų kortelių sritys, kurias turėtumėte išplėsti prieš leisdami naudoti vidines dovanų korteles gamyboje:

- **Dovanų kortelės** numeris – numeracijos naudojamos vidinių dovanų kortelių dovanų kortelių numeriams generuoti. Kadangi skaičių sekas galima lengvai nuspėti, turite išplėsti dovanų kortelių numerių generavimą, kad išduotams dovanų kortelių numeriams būtų naudojamos atsitiktinės, kriptografijos saugos eilutės.
- **GetBalance** – **GetBalance** API naudojamas dovanų kortelių balansams ieškoti. Pagal numatytuosius nustatymus, ši API yra vieša. Jei PIN nėra būtina ieškoti dovanų kortelių balansų, kyla pavojus, kad bruto force atakos galėtų naudoti GetBalance API, norint ieškoti dovanų kortelių numerių, kurie turi **balansus**. Diegę vidinių dovanų kortelių IR API buferizavimo PIN reikalavimus, galite sumažinti riziką.
- **PIN** – pagal numatytąjį nustatymą vidinės dovanų kortelės nepalaiko PIN. Turėtumėte išplėsti vidines dovanų korteles, kad likučiams ieškoti būtų reikalingas PIN. Šią funkciją taip pat galima naudoti dovanų kortelėms užrakinti po klaidingų bandymų įvesti PIN iš eilės.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Įgalinti mokėjimus dovanų kortele išsiregistrregistrus

Numatyta, kad mokėjimai dovanų kortele neįgalinti svečiui (anoniminiam) išregistravimas. Norėdami įjungti juos, atlikite toliau nurodytus veiksmus.

1. „Commerce“ štabe eikite į **Mažmeninė prekyba ir komercija \> Kanalo sąranka \> POS nustatymai \> POS \> POS operacijos**.
1. Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku) tinklelio antraštę, tada pasirinkite Įterpti **stulpelius**.
1. **Įterpimo** stulpelių dialogo lange pažymėkite žymės **langelį AllowAnonymousAccess**.
1. Pasirinkite **Naujinti**.
1. **520** operacijų (dovanų kortelės likutis) ir **214** atveju **nustatykite AllowAnonymousAccess** vertę  **kaip** 1.
1. Pasirinkite **Įrašyti**.
1. Naudodami **1090** paskirstymo grafiką sinchronizuokite kanalo duomenų bazės pakeitimus. 

## <a name="add-a-gift-card-module-to-a-page"></a>Dovanų kortelės modulio įtraukimas į puslapį

Instrukcijų, kaip įtraukti dovanų kortelės modulį į pirkimo užbaigimo puslapį ir nustatyti reikiamas ypatybes, žr. [Pirkimo užbaigimo modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
