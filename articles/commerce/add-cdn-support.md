---
title: Turinio pristatymo tinklo (CDN) palaikymo įtraukimas
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: caed13c37c9043a2acea751c8a8b15261f26ecb2e10b6e64c0ce50f6ce9a68de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722059"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Turinio pateikimo tinklo (CDN) palaikymo įtraukimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).

Jums nustatant e-komercijos aplinką „Dynamics 365 Commerce“, galite konfigūruoti ją darbui su jūsų CDN paslaugomis. 

Jūsų tinkintas domenas gali būti įjungtas jūsų e-komercijos aplinkos suteikimo proceso metu. Jį taip pat galite nustatyti naudodami aptarnavimo užklausą, kai konfigūravimo procesas baigtas. E-komercijos aplinkos suteikimo procesas sukuria šeimininko pavadinimą, susijusį su aplinka. Pagrindinio kompiuterio pavadinimas yra šio formato, kuriame \<*e-commerce-tenant-name*\> yra jūsų aplinkos pavadinimas:

&lt;el.prekybos-numotojo-vardas&gt;.commerce.dynamics.com

Pagrindinio kompiuterio vardas arba galinis punktas, sugeneruotas konfigūruojant, palaiko tik \*.commerce.dynamics.com saugiųjų jungčių lygmens (SSL) sertifikatą. Jis nepalaiko pasirinktinių domenų SSL. Todėl turite nutraukti pasirinktinių savo CDN domenų SSL, o srautą iš CDN persiųsti pagrindinio kompiuterio vardui arba galiniam punktui, kurį sugeneravo „Commerce“. 

Be to, „Commerce“ *statika* („JavaScript“ arba pakopinių stilių sąrašo \[CSS\] failai) teikiama iš galinio punkto, kurį sugeneravo „Commerce“ (\*.commerce.dynamics.com). Statiką kaupti talpykloje galima, tik jei „Commerce“ sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas įdedamas už CDN.

## <a name="set-up-ssl"></a>Nustatyti SSL

Sukonfigūravę savo „Commerce“ aplinką naudodami suteiktą pasirinktinį domeną arba pateikę pasirinktinį aplinkos domeną naudodami aptarnavimo užklausą, pasirinktinį domeną, turite bendradarbiauti su „Commerce“ parengimo komanda planuodami DNS pakeitimus.

Kaip buvo minėta anksčiau, sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas palaiko tik \*.commerce.dynamics.com SSL sertifikatą. Jis nepalaiko pasirinktinių domenų SSL.

## <a name="cdn-services"></a>CDN tarnybos

Su „Commerce“ aplinka galima naudoti bet kurią CDN tarnybą. Toliau pateikti du pavyzdžiai.

- **„Microsoft Azure Front Door Service“** – „Azure“ CDN sprendimas. Norėdami apie „Azure Front Door Service“ gauti daugiau informacijos, žr. [„Azure Front Door Service“ dokumentaciją](/azure/frontdoor/).
- **„Akamai Dynamic Site Accelerator“** – norėdami gauti daugiau informacijos, žr. [„Dynamic Site Accelerator“](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN sąranka

CDN sąrankos procesą sudaro tolesni bendrieji veiksmai.

1. Sąsajos serverio pagrindinio kompiuterio įtraukimas.
1. Vidinio serverio baseino konfigūravimas.
1. Maršruto parinkimo taisyklių nustatymas.

### <a name="add-a-front-end-host"></a>Sąsajos serverio pagrindinio kompiuterio įtraukimas

Galima naudoti bet kurią CDN tarnybą, tačiau šios temos pavyzdyje naudojama „Azure Front Door Service“. 

Norėdami gauti informacijos apie tai, kaip nustatyti „Azure Front Door Service“, žr. [Greitas pasirengimas darbui: „Front Door“ profilio sukūrimas plačiai pasiekiamai visuotinei žiniatinklio programai](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigūruoti vidinio serverio baseiną „Azure Front Door Service“

Vidinio serverio baseino „Azure Front Door Service“ konfigūravimui, atlikite šiuos žingsnius.

1. Įtraukite **&lt;ecom-nuomotojo-pavadinimas&gt;.commerce.dynamics.com** į vidinį telkinį kaip pasirinktinę pagrindinę svetainę, turinčią vidinę pagrindinę antraštę **&lt;ecom-nuomotojo-pavadinimas&gt;.commerce.dynamics.com**.
1. Dalyje **Apkrovos išlyginimas** palikite numatytąsias reikšmes.
1. Išjunkite vidinio telkinio sveikatos patikrinimus.

Toliau pateiktas paveikslėlis rodo **Įtraukti serverį** teksto langelį „Azure Front Door Service“ su serverio pagrindinio kompiuterio įvestu pavadinimu.

![Dialogo langas Vidinio serverio telkinio įtraukimas.](./media/CDN_BackendPool.png)

Toliau pateiktas paveikslėlis rodo **Įtraukti serverio baseiną** teksto langelį „Azure Front Door Service“ nustatytosios apkrovos balansavimo vertėmis.

![Įtraukti serverio baseino teksto laukelio tęsinį.](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Įsitikinkite, kad išjungėte **Sveikatos tikrinimo duomenis** nustatydami savo „Azure Front Door Service”, skirtą „Commerce”.


### <a name="set-up-rules-in-azure-front-door-service"></a>„Azure Front Door Service“ taisyklių nustatymas

Norėdami sprendime „Azure Front Door Service“ nustatyti maršruto parinkimo taisyklę, atlikite tolesnius veiksmus.

1. Įtraukite maršruto parinkimo taisyklę.
1. Lauke **Pavadinimas** įveskite **numatytoji**.
1. Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.
1. Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.
1. Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\***.
1. Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.
1. Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.
1. Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**. 
1. Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.
1. Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.


> [!WARNING]
> Jei jūsų naudojamas domenas jau yra veikiantis ir paleistas, sukurkite paramos bilietą **Parama** dreną [„Microsoft Dynamics Lifecycle Services“](https://lcs.dynamics.com/) tam, kad gautumėte pagalbą tolesniems savo veiksmams. Dėl išsamesnės informacijos, žr.  [Gauti pagalbą „Finance and Operations“ programoms arba „Lifecycle Services (LCS)“](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Jei jūsų domenas yra naujas ir nėra iš anksto egzistuojantis gyvas domenas, galite įtraukti savo tinkintą domeną į „Azure Front Doore Service“ kongirūravimą. Tai leis žiniatinklio srautui vesti jūsų svetainę pro „Azure Front Door“ pavyzdį. Norėdami įtraukti pasirinktinį domeną (pavyzdžiui, `www.fabrikam.com`), turite sukonfigūruoti domeno kanoninį vardą (CNAME).

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **CNAME konfigūravimas**.

![Dialogo langas „CNAME” konfigūravimas.](./media/CNAME_Configuration.png)

Sertifikatą valdyti galite naudodami „Azure Front Door Service“ arba galite naudoti nuosavą pasirinktinio domeno sertifikatą.

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Pasirinktinio domeno HTTPS**.

![Dialogo langas Pasirinktinio domeno HTTPS.](./media/Custom_Domain_HTTPS.png)

Dėl išsamių instrukcijų apie kliento domeno įraukimą į savo „Azure Front Door“, žr. [Įtraukti tinkintą domentą į savo „Front Door“](/azure/frontdoor/front-door-custom-domain).

Dabar jūsų CDN turėtų būti tinkamai sukonfigūruotas, kad jį būtų galima naudoti su jūsų „Commerce“ svetaine.

## <a name="additional-resources"></a>Papildomi ištekliai

[Turinio pristatymo tinklo diegimo parinktys](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]