---
title: Turinio pristatymo tinklo (CDN) palaikymo įtraukimas
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb757672fffb56892837c066d552773908dd1ec1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696973"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Turinio pristatymo tinklo (CDN) palaikymo įtraukimas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).

## <a name="overview"></a>Peržiūrėti

Programoje „Dynamics 365 Commerce“ nustatydami el. prekybos aplinką, galite sukonfigūruoti, kad ji veiktų su CDN tarnyba. 

Jūsų pasirinktinį domeną galima įjungti konfigūruojant el. prekybos aplinką. Jį taip pat galite nustatyti naudodami aptarnavimo užklausą, kai konfigūravimo procesas baigtas. Konfigūruojant el. prekybos aplinką sugeneruojamas su aplinka susietas pagrindinio kompiuterio vardas. Toliau nurodytas šio pagrindinio kompiuterio vardo formatas, kuriame *el. prekybos-nuomotojo-vardas* yra jūsų aplinkos pavadinimas.

&lt;el.prekybos-numotojo-vardas&gt;.commerce.dynamics.com

Pagrindinio kompiuterio vardas arba galinis punktas, sugeneruotas konfigūruojant, palaiko tik \*.commerce.dynamics.com saugiųjų jungčių lygmens (SSL) sertifikatą. Jis nepalaiko pasirinktinių domenų SSL. Todėl turite nutraukti pasirinktinių savo CDN domenų SSL, o srautą iš CDN persiųsti pagrindinio kompiuterio vardui arba galiniam punktui, kurį sugeneravo „Commerce“. 

Be to, „Commerce“ *statika* („JavaScript“ arba pakopinių stilių sąrašo \[CSS\] failai) teikiama iš galinio punkto, kurį sugeneravo „Commerce“ (\*.commerce.dynamics.com). Statiką kaupti talpykloje galima, tik jei „Commerce“ sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas įdedamas už CDN.

## <a name="set-up-ssl"></a>SSL nustatymas

Norėdami padėti užtikrinti, kad būtų nustatytas SSL ir talpykloje kaupiama statika, turite sukonfigūruoti, kad jūsų CDN būtų susietas su pagrindinio kompiuterio vardu, kurį „Commerce“ sugeneravo jūsų aplinkai. Taip pat turite talpykloje kaupti tik tolesnį statikos šabloną. 

/\_msdyn365/\_scnr/\*

Sukonfigūravę savo „Commerce“ aplinką naudodami suteiktą pasirinktinį domeną arba pateikę pasirinktinį aplinkos domeną naudodami aptarnavimo užklausą, pasirinktinį domeną nukreipkite į „Commerce“ sugeneruotą pagrindinio kompiuterio vardą arba galinį punktą.

Kaip buvo minėta anksčiau, sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas palaiko tik \*.commerce.dynamics.com SSL sertifikatą. Jis nepalaiko pasirinktinių domenų SSL.

## <a name="cdn-services"></a>CDN tarnybos

Su „Commerce“ aplinka galima naudoti bet kurią CDN tarnybą. Toliau pateikti du pavyzdžiai.

- **„Microsoft Azure Front Door Service“** – „Azure“ CDN sprendimas. Norėdami apie „Azure Front Door Service“ gauti daugiau informacijos, žr. [„Azure Front Door Service“ dokumentaciją](https://docs.microsoft.com/azure/frontdoor/).
- **„Akamai Dynamic Site Accelerator“** – norėdami gauti daugiau informacijos, žr. [„Dynamic Site Accelerator“](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN sąranka

CDN sąrankos procesą sudaro tolesni bendrieji veiksmai.

1. Įtraukite sąsajos serverio pagrindinį kompiuterį.
1. Sukonfigūruokite vidinio serverio telkinį.
1. Nustatykite maršruto parinkimo ir kaupimo talpykloje taisykles.

### <a name="add-a-front-end-host"></a>Sąsajos serverio pagrindinio kompiuterio įtraukimas

Galima naudoti bet kurią CDN tarnybą, tačiau šios temos pavyzdyje naudojama „Azure Front Door Service“. 

Norėdami gauti informacijos apie tai, kaip nustatyti „Azure Front Door Service“, žr. [Greitas pasirengimas darbui: „Front Door“ profilio sukūrimas plačiai pasiekiamai visuotinei žiniatinklio programai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Vidinio serverio telkinio sukonfigūravimas sprendime „Azure Front Door Service“

Norėdami sprendime „Azure Front Door Service“ sukonfigūruoti vidinio serverio telkinį, atlikite tolesnius veiksmus.

1. Į vidinio serverio telkinį įtraukite **&lt;el.prek-nuomotojo-vardas&gt;.commerce.dynamics.com** kaip pasirinktinį pagrindinį kompiuterį su tuščia vidinio serverio pagrindinio kompiuterio antrašte.
1. Dalies **Būklės patikros** lauke **Kelias** įveskite **/keepalive**.
1. Lauke **Intervalas (sekundės)** įveskite **255**.
1. Dalyje **Apkrovos išlyginimas** palikite numatytąsias reikšmes.

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Vidinio serverio telkinio įtraukimas**.

![Dialogo langas Vidinio serverio telkinio įtraukimas](./media/CDN_BackendPool.png)

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

Norėdami sprendime „Azure Front Door Service“ nustatyti kaupimo talpykloje taisyklę, atlikite tolesnius veiksmus.

1. Įtraukite kaupimo talpykloje taisyklę.
1. Lauke **Pavadinimas** įveskite **statika**.
1. Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.
1. Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.
1. Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\_msdyn365/\_scnr/\***.
1. Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.
1. Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.
1. Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.
1. Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.
1. Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.
1. Lauke **Užklausos eilučių kaupimo talpykloje būdas** pasirinkite **Talpykloje kaupti kiekvieną unikalų URL**.
1. Laukų grupėje **Dinaminis glaudinimas** pasirinkite parinktį **Įjungta**.

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Taisyklės įtraukimas**.

![Dialogo langas Taisyklės įtraukimas](./media/CDN_CachingRule.png)

Įdiegę šią pradinę konfigūraciją, į „Azure Front Door Service“ konfigūraciją turite įtraukti savo pasirinktinį domeną. Norėdami įtraukti pasirinktinį domeną (pavyzdžiui, `www.fabrikam.com`), turite sukonfigūruoti domeno kanoninį vardą (CNAME).

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **CNAME konfigūravimas**.

![Dialogo langas CNAME konfigūravimas](./media/CNAME_Configuration.png)

> [!NOTE]
> Jei jūsų naudosimas domenas jau aktyvus ir paleistas, kreipkitės į palaikymo tarnybą, kad šį domeną būtų galima naudoti su „Azure Front Door Service“ ir nustatyti testą.

Sertifikatą valdyti galite naudodami „Azure Front Door Service“ arba galite naudoti nuosavą pasirinktinio domeno sertifikatą.

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Pasirinktinio domeno HTTPS**.

![Dialogo langas Pasirinktinio domeno HTTPS](./media/Custom_Domain_HTTPS.png)

Dabar jūsų CDN turėtų būti tinkamai sukonfigūruotas, kad jį būtų galima naudoti su jūsų „Commerce“ svetaine.

## <a name="additional-resources"></a>Papildomi ištekliai

[Interneto parduotuvės peržiūra](online-store-overview.md)

[E. prekybos svetainės kūrimas](create-ecommerce-site.md)

[Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Įgalinti parduotuvės nustatymą pagal vietą](enable-store-detection.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)
