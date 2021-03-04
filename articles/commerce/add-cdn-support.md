---
title: Turinio pristatymo tinklo (CDN) palaikymo įtraukimas
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).
author: brianshook
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: 0e888fca4a5401f1df6e61b10358489846ad4b0e
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517213"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Turinio pristatymo tinklo (CDN) palaikymo įtraukimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).

## <a name="overview"></a>Peržiūra

Jums nustatant e-komercijos aplinką „Dynamics 365 Commerce“, galite konfigūruoti ją darbui su jūsų CDN paslaugomis. 

Jūsų tinkintas domenas gali būti įjungtas jūsų e-komercijos aplinkos suteikimo proceso metu. Jį taip pat galite nustatyti naudodami aptarnavimo užklausą, kai konfigūravimo procesas baigtas. E-komercijos aplinkos suteikimo procesas sukuria šeimininko pavadinimą, susijusį su aplinka. Pagrindinio kompiuterio pavadinimas yra šio formato, kuriame \<*e-commerce-tenant-name*\> yra jūsų aplinkos pavadinimas:

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
1. Konfigūruoti vidinio serverio baseiną.
1. Nustatykite maršruto parinkimo ir kaupimo talpykloje taisykles.

### <a name="add-a-front-end-host"></a>Sąsajos serverio pagrindinio kompiuterio įtraukimas

Galima naudoti bet kurią CDN tarnybą, tačiau šios temos pavyzdyje naudojama „Azure Front Door Service“. 

Norėdami gauti informacijos apie tai, kaip nustatyti „Azure Front Door Service“, žr. [Greitas pasirengimas darbui: „Front Door“ profilio sukūrimas plačiai pasiekiamai visuotinei žiniatinklio programai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigūruoti vidinio serverio baseiną „Azure Front Door Service“

Vidinio serverio baseino „Azure Front Door Service“ konfigūravimui, atlikite šiuos žingsnius.

1. Įtraukti **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** vidinio serverio baseiną, kaip tinkintą pagrindinį kompiuterį, kuris turi tuščią vidinio serverio pagrindinio kompiuterio antraštę.
1. Dalyje **Apkrovos išlyginimas** palikite numatytąsias reikšmes.

Toliau pateiktas paveikslėlis rodo **Įtraukti serverį** teksto langelį „Azure Front Door Service“ su serverio pagrindinio kompiuterio įvestu pavadinimu.

![Dialogo langas Vidinio serverio telkinio įtraukimas](./media/CDN_BackendPool.png)

Toliau pateiktas paveikslėlis rodo **Įtraukti serverio baseiną** teksto langelį „Azure Front Door Service“ nustatytosios apkrovos balansavimo vertėmis.

![Įtraukti serverio baseino teksto laukelio tęsinį](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>„Azure Front Door Service“ taisyklių nustatymas

Norėdami sprendime „Azure Front Door Service“ nustatyti maršruto parinkimo taisyklę, atlikite tolesnius veiksmus.

1. Įtraukite maršruto parinkimo taisyklę.
1. Lauke **Pavadinimas** įveskite **numatytoji**.
1. Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.
1. Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.
1. Skyriuje **Atitinkančios iškarpos**, viršutiniame laukelyje įveskite **/\** _.
1. Skyriuje **Maršruto išsami informacija**, nustatykite **Maršruto tipo** parinktį į **Pirmyn**.
1. Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.
1. Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**. 
1. Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.
1. Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.

Norėdami sprendime „Azure Front Door Service“ nustatyti kaupimo talpykloje taisyklę, atlikite tolesnius veiksmus.

1. Įtraukite kaupimo talpykloje taisyklę.
1. Lauke **Pavadinimas** įveskite **statika**.
1. Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.
1. Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.
1. Skyriuje **Atitinkančios iškarpos**, viršutiniame laukelyje **/\_msdyn365/\_scnr/\** _.
1. Skyriuje **Maršruto išsami informacija**, nustatykite **Maršruto tipo** parinktį į **Pirmyn**.
1. Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.
1. Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.
1. Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.
1. Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.
1. Lauke **Užklausos eilučių kaupimo talpykloje būdas** pasirinkite **Talpykloje kaupti kiekvieną unikalų URL**.
1. Laukų grupėje **Dinaminis glaudinimas** pasirinkite parinktį **Įjungta**.

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Taisyklės įtraukimas**.

![Dialogo langas Taisyklės įtraukimas](./media/CDN_CachingRule.png)

> [!WARNING]
> Jei jūsų naudojamas domenas jau yra veikiantis ir paleistas, sukurkite paramos bilietą **Parama** dreną [„Microsoft Dynamics Lifecycle Services“](https://lcs.dynamics.com/) tam, kad gautumėte pagalbą tolesniems savo veiksmams. Dėl išsamesnės informacijos, žr.  [Gauti pagalbą „Finance and Operations“ programoms arba „Lifecycle Services (LCS)“](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Jei jūsų domenas yra naujas ir nėra iš anksto egzistuojantis gyvas domenas, galite įtraukti savo tinkintą domeną į „Azure Front Doore Service“ kongirūravimą. Tai leis žiniatinklio srautui vesti jūsų svetainę pro „Azure Front Door“ pavyzdį. Norėdami įtraukti pasirinktinį domeną (pavyzdžiui, `www.fabrikam.com`), turite sukonfigūruoti domeno kanoninį vardą (CNAME).

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **CNAME konfigūravimas**.

![Dialogo langas CNAME konfigūravimas](./media/CNAME_Configuration.png)

Sertifikatą valdyti galite naudodami „Azure Front Door Service“ arba galite naudoti nuosavą pasirinktinio domeno sertifikatą.

Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Pasirinktinio domeno HTTPS**.

![Dialogo langas Pasirinktinio domeno HTTPS](./media/Custom_Domain_HTTPS.png)

Dėl išsamių instrukcijų apie kliento domeno įraukimą į savo „Azure Front Door“, žr. [Įtraukti tinkintą domentą į savo „Front Door“](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).

Dabar jūsų CDN turėtų būti tinkamai sukonfigūruotas, kad jį būtų galima naudoti su jūsų „Commerce“ svetaine.

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Talpinkite naują e-komercijos nuomotoją](deploy-ecommerce-site.md)

[Sukurkite e-komercijos saitą](create-ecommerce-site.md)

[Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](associate-site-online-store.md)

[„robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]