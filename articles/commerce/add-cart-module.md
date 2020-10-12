---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818280"
---
# <a name="cart-module"></a>Krepšelio modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūra

Krepšelio modulyje rodomos prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant. Šiame modulyje taip pat rodoma užsakymo suvestinė, be to, klientui leidžiama taikyti arba pašalinti reklaminius kodus.

Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą. Jis taip pat palaiko saitą **Grįžti prie pirkimo**. Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.

Krepšelio modulis generuoja duomenis pagal krepšelio ID, kuris yra naršyklės slapukas, pasiekiamas visoje svetainėje. 

Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.

![Krepšelio modulio, esančio „Fabrikam” svetainėje, pavyzdys](./media/cart2.PNG)

Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys. Šiame pavyzdyje yra eilutės prekės paėmimo mokestis.

![Krepšelio modulio su eilutės prekės tvarkymo mokesčiu pavyzdys](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Krepšelio modulio ypatybės ir vietos

| Ypatybė | Reikšmės | aprašymas |
|----------------|--------|-------------|
| Antraštė | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**) | Vežimėlio antraštė, tokia kaip „Apsipirkimo maišelis“ arba „Prekės jūsų vežimėlyje“. |
| Rodyti nėra sandėlyje klaidas | **Teisinga** arba **Klaidinga** | Jei ši ypatybė nustatyta į **Tiesa**, vežimėlio puslapyje bus rodomos su atsargomis susijusios klaidos. Rekomenduojame nustatyti šią ypatybę į **Tiesa**, jei atsargų tikrinimai yra taikomi svetainėje. |
| Rodyti eilutės prekių siuntimo mokesčius | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatytą į **Teisinga**, vežimėlio eilučių prekės rodys siuntimo mokesčius, jei tokia informacija yra prieinama. Ši savybė nėra palaikoam „Fabrikam“ temoje, nes vartotojai pasirenka siuntimą tik išsiregistravimo sraute. Nepaisant to, šią funkciją galima įjungti kituose darbo srautuose, jei tai taikoma. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduliai, kuriuos galima naudoti krepšelio modulyje

- **Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę. Pranešimai grindžiami turinio valdymo sistema (TVS). Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.
- **Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas. Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves. Daugiau informacijos apie šį modulį žr. [Parduotuvės parinkiklio modulis](store-selector.md).

## <a name="module-properties"></a>Modulio ypatybės

Dalyje **Svetainės parametrai \> Plėtiniai** galima konfigūruoti toliau pateiktus krepšelio modulio parametrus:

- **Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį. Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.
- **Atsargos** – norėdami gauti informacijos apie atsargų parametrų taikymą, žr. [Atsargų parametrų taikymas](inventory-settings.md).
- **Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą. Maršrutas gali būti sukonfigūruotas svetainės lygiu, leidžiant mažmeninės prekybos klientams grįžti į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas. Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.

## <a name="add-a-cart-module-to-a-page"></a>Krepšelio modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.
1. Dialogo lange **Naujas fragmentas** pasirinkite **Krepšelio** modulį.
1. Dalyje **Fragmento pavadinimas** įveskite pavadinimą **Krepšelio fragmentas** ir pasirinkite **Gerai**.
1. Pasirinkite vietą **Krepšelis**.
1. Dešinėje pusėje esančioje ypatybių srityje pasirinkite pieštuko simbolį, į laukelį įveskite antraštės tekstą ir pasirinkite varnelės simbolį.
1. Vietoje **Krepšelis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Parduotuvės parinkiklis**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite šablono pavadinimą.
1. Struktūros medyje pasirinkite vietą **Pagrindinė dalis**, pasirinkite daugtaškį (**...**), tada – **Įtraukti fragmentą**.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite **Krepšelio fragmentas** fragmentą ir pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite anksčiau sukurtą šabloną, įveskite puslapio pavadinimą ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)

[Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md)
