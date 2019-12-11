---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696766"
---
# <a name="cart-module"></a>Krepšelio modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Krepšelio modulis yra konteineris, kuriame yra visi moduliai, kurių reikia norint rodyti krepšelyje esančias prekes. Pavyzdžiui, jame yra visos į krepšelį įtrauktos prekės, užsakymo suvestinė ir akcijų kodai.

Krepšelio modulis duomenis generuoja pagal krepšelio ID. Krepšelio ID yra naršyklės slapukas, pasiekiamas visoje svetainėje.

## <a name="cart-module-properties-and-slots"></a>Krepšelio modulio ypatybės ir vietos

Kaip konteineris krepšelio modulis valdo keletą pagrindinių ypatybių, pvz., antraštę ir plotį. Antraštė paprastai yra tekstas, pvz., **Pirkinių krepšelis**, **Jūsų krepšelis** ar **Jūsų krepšelio prekės**. Pločio parametru nustatoma, ar konteineryje esantys moduliai turi tilpti tame konteineryje, ar jie gali užpildyti ekraną.

Krepšelio puslapis yra padalytas į kelias sritis: krepšelio eilutės prekių, užsakymo suvestinės ir pirkimo užbaigimo bei funkcijos „rasti parduotuvėje“. Kiekviena sritis yra susieta su krepšelio modulio vieta, o kiekvienoje vietoje galima naudoti iš anksto nustatytą modulių rinkinį.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduliai, kuriuos galima naudoti krepšelio modulyje

- **Krepšelio eilutės prekės** – naudojant šį modulį rodoma visų į krepšelį įtrauktų prekių suvestinė. Informacija apima produkto pavadinimą, pasirinktus matmenis, kainą, kiekį ir nuolaidas. Šis modulis taip pat palaiko tokius veiksmus, kaip „pašalinti iš krepšelio“ ir „įtraukti į pageidavimų sąrašą“. Galima parinktis kiekvieną eilutės prekę siųsti arba atsiimti iš parduotuvės. Šią parinktį reikia sukonfigūruoti atskirai atsiėmimo parduotuvėje modulyje.
- **Užsakymo suvestinė** – naudojant šį modulį rodoma užsakymo suvestinė. Informacija apima tarpinę sumą, siuntimą, mokesčius ir sutaupomą sumą. Galima sukonfigūruoti šio modulio antraštę.
- **Akcijos kodas** – naudodamas šį modulį klientas gali panaudoti akcijų kodus. Akcijos kodą galima pritaikyti arba pašalinti.
- **Pirkimo užbaigimas** – naudojant šį modulį pradedamas pirkimo užbaigimo veiksmas ir vartotojas nukreipiamas į pirkimo užbaigimo puslapį. Reikia sukonfigūruoti tolesnius tris šio modulio saitus.

    - **Pirkimo užbaigimas** – šis saitas klientus priverčia prisijungti, jei jie dar neprisijungę.
    - **Pirkimo užbaigimas kaip svečiui** – naudodami šį saitą, pateikti užsakymus gali anoniminiai klientai. Jis rodomas tik tada, kai klientai nėra prisijungę.
    - **Grįžti prie pirkimo** – naudodami šį saitą klientai gali pereiti į pagrindinį puslapį ar bet kurį kitą puslapį ir toliau apsipirkti.

- **Raiškiojo turinio blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę. Pranešimai grindžiami turinio valdymo sistema (TVS). Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.
- **Atsiimti parduotuvėje** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas. Numatyta, kad šis modulis rodo parduotuves, kurios yra 50 mylių spinduliu nuo kliento vietos. Tačiau ieškos spindulį modulyje galima tinkinti. Jei yra įjungta atsargų tikrinimo funkcija, patikrinamos kiekvienos parduotuvės atsargos ir parodomas atitinkamas pranešimas apie atsargų buvimą arba nebuvimą.
- **Parduotuvių ieška naudojant „Bing“ žemėlapius** – šį modulį galima naudoti atsiėmimo parduotuvėje modulyje. Jį naudodami klientai gali ieškoti parduotuvių įvesdami vietą. Naudojant „Bing“ žemėlapių geokodavimo programų programavimo sąsają (API), kliento įvesta vieta konvertuojama į platumą ir ilgumą. Jei šis modulis nenaudojamas, rodomos tik tos parduotuvės, kurios yra netoli dabartinės kliento vietos, ir klientas kitos vietos ieškoti negali.

## <a name="cart-module-settings"></a>Krepšelio modulio parametrai

Galima konfigūruoti tolesnius tris krepšelio modulių parametrus.

- **Maksimalus kiekis** – maksimalus kiekvienos prekės skaičius, kurį galima įtraukti į krepšelį. Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.
- **Atsargų patikra** – kai reikšmė nustatoma kaip **Teisinga**, prekė į krepšelį įtraukiama tik tada, kai pirkimo langelio modulis užtikrina, kad yra jos atsargų. Ši atsargų patikra atliekama tiek tose situacijose, kai prekė bus siunčiama, tiek tose situacijose, kai ji bus atsiimama iš parduotuvės. Jei reikšmė nustatoma kaip **Klaidinga**, prieš prekę įtraukiant į krepšelį ir pateikiant užsakymą atsargos nepatikrinamos.
- **Atsargų buferis** – atsargos tvarkomos realiuoju laiku ir dideliam klientų skaičiui teikiant užsakymus gali būti sudėtinga turėti tikslų atsargų skaičių. Todėl galima nustatyti atsargų buferį. Jei, tikrinant atsargas, jų yra mažiau nei buferio suma, laikoma, kad produkto atsargų nėra. Todėl greitai pardudodant keliais kanalais, kai ne visiškai sinchronizuojamas atsargų kiekis, yra mažiau rizikos, kad bus parduota prekė, kurios atsargų nėra.

## <a name="retail-server-interaction"></a>Sąveika su „Retail Server“

Krepšelio modulis produkto informaciją gauna naudodamas „Retail Server“ API sąsajas. Visa informacija apie produktus iš „Retail Server“ gaunama naudojant krepšelio ID iš naršyklės slapuko.

## <a name="add-a-cart-module-to-a-page"></a>Krepšelio modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite fragmentą pavadinimu **krepšelio fragmentas** ir į jį įtraukite krepšelio modulį.
1. Krepšelio modulio vietoje **Krepšelio eilutės prekės** įtraukite krepšelio eilutės prekių modulį.
1. Vietoje **Užsakymo suvestinė** įtraukite užsakymo suvestinės modulį.
1. Vietoje **Akcijos kodas** įtraukite akcijos kodo modulį.
1. Vietoje **Pirkimo užbaigimas** įtraukite pirkimo užbaigimo modulį.
1. Vietoje **Rasti parduotuvėje** įtraukite atsiėmimo parduotuvėje modulį.
1. Atsiėmimo parduotuvėje modulyje pasirinkite vietą **Parduotuvių ieška** ir įtraukite parduotuvių ieškos naudojant „Bing“ žemėlapius modulį.
1. Fragmentą įrašykite ir atrakinkite bei publikuokite.
1. Sukurkite šabloną pavadinimu **krepšelio šablonas** ir į jį įtraukite ką tik sukurtą krepšelio fragmentą.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Sukurkite puslapį, kuriame naudojamas naujasis šablonas.
1. Puslapį įrašykite ir peržiūrėkite.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
