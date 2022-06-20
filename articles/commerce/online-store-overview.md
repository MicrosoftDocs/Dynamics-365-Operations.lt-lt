---
title: El. prekybos svetainės apžvalga
description: Šiame straipsnyje pateikta el. komercijos svetainių palaikymo apžvalga Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9b7e4d09eaa4f91478d27cbca5eaea48af86e676
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899126"
---
# <a name="e-commerce-site-overview"></a>El. prekybos svetainės apžvalga

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikta el. komercijos svetainių palaikymo apžvalga Microsoft Dynamics 365 Commerce. Ji apima informaciją apie tai, kaip e-komercijos interneto parduotuvės pradedamos ir valdomos „Dynamics 365 Commerce“. Jame taip pat pateiktos nuorodos į didesnį kiekį informacijos apie internetines parduotuves, kaip nustatyti ir konfigūruoti e-komercijos svetainę. Nors šis straipsnis apima daugelį pagrindinių dalykų, jis neapima visų reikalingų gamybos el. komercijos svetainių. Daugiau išplėstinių straipsnių galima rasti Dynamics 365 Commerce dokumentuose.

## <a name="online-store-channel"></a>Interneto parduotuvės kanalas

Iki jums sukuriant savo svetainę „Dynamics 365 Commerce“, mažiausiai vienas interneto parduotuvės kanalas turi būti nustatytas. Dėl daugiau informacijos, žr. [Nustatyti interneto kanalą](channel-setup-online.md). 

„Dynamics 365 Commerce“ naudojate interneto parduotuvės kanalą tam, kad sukurtumėte produktus, kainas, kalbas, mokėjimo metodus, pristatymo būdus, įgyvendinimo centrus ir kitus internetinės patirties aspektus, kurie turi būti prieinami jūsų klientams.

Tik vienas interneto parduotuvės kanalas turi būti nustatytas iki kol pradėsite su „Dynamics 365 Commerce“. Tačiau tik vienas e-komercijos saitas gali suteikti interneto patirtį kelioms interneto parduotuvėms. Pavyzdžiui, jei kelios interneto parduotuvės nustatomos siekiant palaikyti skirtingus geografinius regionus, vienas e-komercijos puslapių rinkinys gali būti naudojamas unikaliai patirčiai, kuri nustatyta kiekvienoje parduotuvėje. Daugiau informacijos apie tai, kaip sukonfigūruoti svetainę, kad būtų palaikomos kelios internetinės parduotuvės, žr. [Internetinės svetainės susiejimas su kanalu](associate-site-online-store.md).

Po to, kai internetinė parduotuvė yra nustatyta, ji gali būti susieta su „Dynamics 365 Commerce“ svetaine, kuri bus naudojama kaip jūsų el. parduotuvės vitrina. Daugiau informacijos apie internetines parduotuves ir kaip jas nustatyti rasite [Internetinių parduotuvių sąranka](/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Talpinkite naują e-komercijos nuomotoją

E-komercijos saito pradžioje, būsite paskatinti domeno pavadinimui. Dėl daugiau informacijos apie domenus „Commerce“, žr. [Konfigūruoti savo domeno pavadinimą](configure-your-domain-name.md) ir [Domenai „Dynamics 365 Commerce“](domains-commerce.md). Norėdami talpinti naują e-komercijos nuomotoją su [„Microsoft Dynamics Lifecycle Services“ (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), atlikite veiksmus [Talpinti naują e-komercijos nuomotoją](deploy-ecommerce-site.md). Kai jūsų e-komercijos nuomotojas nustatytas LCS, nuoroda su „Commerce“ saito kūrėju bus pateikta. Galite tuomet naudoti „Commerce“ saito kūrėją, kad pradėtumėte ir konfigūruotumėte e-komercijos saitus.

## <a name="initialize-your-e-commerce-site"></a>Pradėkite savo e-komercijos saitą

Jums pradėjus „Commerce“ saito kūrėją nuo LCS, pasirodo **Saitai** puslapis. Šiame puslapyje yra du iš anksto sukonfigūruoti saitai, **nustatytasis** ir **fabrikam**, kaip parodyta tolesniame paveikslėlyje.

![Saito puslapis „Commerce“ saito kūrimo įrankyje.](media/e-commerce-site-01.png)

Jums pasirinkus vieną iš saitų, būsite paskatinti pasirinkti domeno pavadinimą, numatytąjį interneto parduotuvės kanalą, palaikomą kalbą pasirinktam kanalui ir maršrutą. Jei naudojamas tik vienas kanalas, galite palikti maršrutą tuščią. Daugiau interneto parduotuvės kanalų ir kalbų galima sukonfigūruoti vėliau „Commerce“ saito kūrimo įrankyje. Kiekvienas papildomas kanalas ar kalba turės turėti unikalų maršrutą. Pavyzdžiui, turite du interneto kanalus, kurie susieti su vienu saitu ir domeno pavadinimas saitui yra  `www.fabrikam.com`. Tokiu atveju, maršrutas vienam kanalui gali būti nustatytoji vertė neturinti jokio maršruto (`https://www.fabrikam.com`), o antrasis kanalas gali būti nustatytas į naują maršrutą kaip **saitas2**, kuris turės URL `https://www.fabrikam.com/site2`. Tolesnis paveikslėlis rodo saito pradžios teksto laukelio „Commerce“ saito kūrimo įrankyje pavyzdį.

![Saito pradžios teksto laukelis „Commerce“ saito kūrimo įrankyje.](media/e-commerce-site-02.png)

Puslapis **Saitai** taip pat apima **Naujas saitas** mygtuką. Teksto laukelis pasirodo, kai pasirenkate šį mygtuką ir jis atspindi saito pradžios teksto laukelį, bet naudojamas siekiant sukurti naują saitą. Nauji saitai yra tušti. Jie neapima tų pačių numatytųjų šablonų, fragmentų, puslapių ir paveikslėlių, pateiktų su **numatytaisiais** ir **„fabrikam”** saitais. Nepaisant to, kaip būtina, galite atverti palaikymo bilietą siekiant paprašyti, jog numatytojo turinio kopija būtų įtraukta į naują tuščią saitą. Dėl daugiau informacijos, žr. [Sukurti e-komercijos saitą](create-ecommerce-site.md).

Po naujo saito pradžios „Commerce“ saito kūrimo įrankio **Pagrindinis** puslapis pasirodo. Šiame puslapyje yra nuorodos į bendrus veiksmus ir gairių turinį, kaip parodyta tolesniame paveikslėlyje.

![Nuorodos į Pagrindinį puslapį „Commerce“ saito kūrimo įrankyje.](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Keisti interneto parduotuvės kanalus ar įtraukti interneto parduotuvės kanalus į e-komercijos saitą

Po e-komercijos saito sukūrimo, galite keisti su juo susietą kanalą su tolesniais žingsniais [Susieti e-komercijos saitą su interneto kanalu](associate-site-online-store.md). Pavyzdys tolesniame paveikslėlyje rodo, kaip kanalo veikimo vieneto numeris (OUN) gali būti keičiamas **Kanalų** puslapyje (**Saito nustatymuose \> Kanaluose**). Jums pabaigus keitimą, įsitikinkite, kad pasirinkote **Įrašyti ir publikuoti**. Tokiu būdu, įsitikinsite, kad pakeitimas yra publikuotas.

![Kanalo puslapis „Commerce“ saito kūrimo įrankyje.](media/e-commerce-site-04.png)

Galite įtraukti naujus kanalus pasirinkdami **Įtraukti kanalą**. Norėdami įtraukti naujas kalbas į kanalą, pasirinkite kanalą ir tada rinkitės **Įtraukti vietinį** pasirodančiame kanalo teksto laukelyje. Prieš tai, kai vietiniai gali pasirodyti teksto laukelyje, juos reikia sukonfigūruoti iš anksto interneto parduotuvės kanale „Commerce“ štabe.

![Kanalo teksto laukelis „Commerce“ saito kūrimo įrankyje.](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Nustatykite „Azure B2C“ nuomotoją

„Dynamics 365 Commerce“ naudoja „Azure Active Directory“ („Azure AD“) verslo su klientu (B2C) siekiant palaikyti vartotojo prisijungimo informaciją ir autentifikavimo eigas. Dėl informacijos apie tai, kaip nustatyti „Azure B2C“ nuomotoją, žr. [Nustatyti B2C nuomotoją „Commerce“](set-up-b2c-tenant.md), [Nustatykite tinkintus puslapius vartotojo prisijungimams](custom-pages-user-logins.md) ir [Konfigūruokite keletą B2C nuomotojų „Commerce“ aplinkoje](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Numatytojo saito puslapio apžvalga

Saitai **numatytasis** ir **„fabrikam”** apima iš anksto konfigūruotus šablonus, fragmentus ir puslapius siekiant padėti jums pradėti. Daugiau informacijos ieškokite šiuose straipsniuose:

- [Pagrindinio puslapio apžvalga](quick-tour-home-page.md)
- [Produkto išsamios informacijos puslapio apžvalga](quick-tour-pdp.md)
- [Krepšelio ir pirkimo užbaigimo puslapių apžvalga](quick-tour-cart-checkout.md)
- [Sąskaitos valdymo puslapių apžvalga](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Valdyti saito nustatymus

Informacijos apie tai, kaip valdyti savo svetainės nustatymus, ieškokite šiame straipsnius:

- [Valdyti e-komercijos vartotojus ir vaidmenis](manage-ecommerce-users-roles.md)
- [Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei](search-engine-optimization-considerations.md)
- [Turinio saugos strategijos (CSP) tvarkymas](manage-csp.md)
- [Pasirinkti svetainės temą](select-site-theme.md)

## <a name="manage-site-content"></a>Valdyti saito turinį

Informacijos apie tai, kaip valdyti svetainės turinį, rasite rasite toliau pateikiamame straipsnius:

- [Puslapio modelio žodynas](page-elements-overview.md)
- [Dokumentų būsenos ir vykdymo ciklas](document-states-overview.md)
- [Šablonai ir išdėstymas](templates-layouts-overview.md)
- [Darbas su fragmentais](work-with-fragments.md)
- [Darbas su moduliais](work-with-modules.md)
- [Skaitmeninio turto valdymo apžvalga](dam-overview.md)
- [Modulių bibliotekos peržiūra](starter-kit-overview.md)

## <a name="additional-resources"></a>Papildomi ištekliai

[Sukurkite e-komercijos saitą](create-ecommerce-site.md)

[Talpinkite naują e-komercijos saitą](deploy-ecommerce-site.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Įgalinti parduotuvės nustatymą pagal vietą](enable-store-detection.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]