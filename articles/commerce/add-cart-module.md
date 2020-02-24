---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025441"
---
# <a name="cart-module"></a>Krepšelio modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Krepšelio modulis naudojamas norint parodyti prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant. Pavyzdžiui, jame yra visos į krepšelį įtrauktos prekės ir užsakymo suvestinė. Be to, jis leidžia klientui taikyti arba pašalinti akcijų kodus.

Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą. Jis taip pat palaiko saitą **Grįžti prie pirkimo**. Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.

Krepšelio modulis duomenis generuoja pagal krepšelio ID. Krepšelio ID yra naršyklės slapukas, pasiekiamas visoje svetainėje.

## <a name="cart-module-properties-and-slots"></a>Krepšelio modulio ypatybės ir vietos

Krepšelio modulyje yra ypatybė **Antraštė**, kurią galima nustatyti kaip **Pirkinių krepšelis** ir **Jūsų krepšelio prekės**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduliai, kuriuos galima naudoti krepšelio modulyje

- **Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę. Pranešimai grindžiami turinio valdymo sistema (TVS). Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.
- **Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas. Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves. Parduotuvės parinkiklio modulis yra integruotas su „Bing“ žemėlapių geokodavimo programos programavimo sąsaja (API), kad vieta būtų konvertuojama į platumą ir ilgumą. Reikalingas „Bing“ žemėlapių API raktas ir jį reikia įtraukti į mažmeninės prekybos bendrinamus parametrus puslapyje „Dynamics 365 Retail“. Šis modulis palaiko dvi ypatybes – **Ieškos spindulys** ir **Paslaugų saito sąlygos**. Ypatybė **Ieškos spindulys** nurodo parduotuvių ieškos spindulį, išreikštą myliomis. Jei nenurodyta jokia reikšmė, naudojamas numatytasis ieškos spindulys, kuris yra 50 mylių. Jei naudojami „Bing“ žemėlapiai arba bet kokia išorinė paslauga, ypatybė **Paslaugos saito sąlygos** gali būti naudojama norint pateikti saitą į paslaugos sąlygas. Paslaugos saito sąlygų reikia „Bing“ žemėlapių paslaugai. 

## <a name="cart-module-settings"></a>Krepšelio modulio parametrai

Krepšelio moduliai turi šiuos parametrus, kuriuos galima konfigūruoti einant į **Svetainės parametrai \> Plėtiniai**:

- **Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį. Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.
- **Atsargų patikra** – kai reikšmė nustatoma kaip **Teisinga**, prekė į krepšelį įtraukiama tik tada, kai pirkimo langelio modulis užtikrina, kad yra jos atsargų. Ši atsargų patikra atliekama tiek tose situacijose, kai prekė bus siunčiama, tiek tose situacijose, kai ji bus atsiimama iš parduotuvės. Jei reikšmė nustatoma kaip **Klaidinga**, prieš prekę įtraukiant į krepšelį ir pateikiant užsakymą atsargos nepatikrinamos.
- **Atsargų buferis** – ši ypatybė naudojama norint nurodyti atsargų buferio skaičių. Atsargos tvarkomos realiuoju laiku ir dideliam klientų skaičiui teikiant užsakymus gali būti sudėtinga turėti tikslų atsargų skaičių. Jei, tikrinant atsargas, jų yra mažiau nei buferio suma, laikoma, kad produkto atsargų nėra. Todėl greitai pardudodant keliais kanalais, kai ne visiškai sinchronizuojamas atsargų kiekis, yra mažiau rizikos, kad bus parduota prekė, kurios atsargų nėra.
- **Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą. Šis maršrutas gali būti sukonfigūruotas svetainės lygiu. Naudojant šią konfigūraciją, mažmeninės prekybos klientai gali grįžta į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas. Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.

## <a name="add-a-cart-module-to-a-page"></a>Krepšelio modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite fragmentą pavadinimu **Krepšelio fragmentas** ir į jį įtraukite krepšelio modulį.
1. Į krepšelio modulį įtraukite antraštę.
1. Įtraukite parduotuvės parinkiklio modulį į krepšelio modulį.
1. Įrašykite fragmentą, baikite redagavimą ir publikuokite.
1. Sukurkite šabloną pavadinimu **Krepšelio šablonas** ir į jį įtraukite ką tik sukurtą krepšelio fragmentą.
1. Įrašykite šabloną, baikite redagavimą ir publikuokite.
1. Sukurkite puslapį, kuriame naudojamas naujasis šablonas.
1. Puslapį įrašykite ir peržiūrėkite.
1. Baikite puslapio redagavimą ir publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
