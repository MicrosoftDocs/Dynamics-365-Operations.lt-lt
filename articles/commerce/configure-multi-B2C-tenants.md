---
title: Kelių B2C nuomotojų konfigūravimas „Commerce“ aplinkoje
description: Šioje temoje aprašoma, kada ir kaip viename kanale nustatyti kelis „Microsoft Azure Active Directory“ („Azure AD“) verslas–vartotojui (B2C) nuomotojus, skirtus vartotojo autentifikavimui paskirtoje „Dynamics 365 Commerce“ aplinkoje.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6ca48badbe15b7e1bf543716a9b0e3da31477a20
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096518"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Kelių B2C nuomotojų konfigūravimas „Commerce“ aplinkoje

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kada ir kaip viename kanale nustatyti kelis „Microsoft Azure Active Directory“ („Azure AD“) verslas–vartotojui (B2C) nuomotojus, skirtus vartotojo autentifikavimui paskirtoje „Dynamics 365 Commerce“ aplinkoje.

## <a name="overview"></a>Peržiūra

„Dynamics 365 Commerce“ naudoja „Azure AD“ B2C debesies tapatumo paslaugą vartotojo kredencialams ir autentifikavimo srautams palaikyti. Vartotojai gali naudoti autentifikavimo srautus, norėdami prisiregistruoti, prisijungti ir nustatyti slaptažodį iš naujo. „Azure AD“ B2C saugoma vartotojo slapto autentifikavimo informacija, pvz., vartotojo vardas ir slaptažodis. Vartotojo įrašas yra unikalus kiekvienam B2C nuomotojui ir naudoja vartotojo vardą (el. pašto adresą), kredencialus arba socialinės tapatybės teikimo įrankio kredencialus.

Daugeliu atveju „Commerce“ aplinkoje naudojamas vienas „Azure AD“ B2C nuomotojas. „Commerce“ klientai gali kurti ir publikuoti kelias svetaines toje pačioje „Commerce“ aplinkoje, o šiose svetainėse bus naudojami tie patys kliento kredencialai. Tačiau jei aplinkoje esančios svetainės turi būti traktuojamos kaip skirtingi prekių ženklai ir rodomos vartotojams kaip atskiros įmonės, B2C nuomotoją galima sukonfigūruoti kanalui, kuris naudojamas svetainės / prekės ženklo atskyrimui.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Aplinkybės, kai vienam kanalui nustatyti keli B2C nuomotojai

Dažnai, kai kiekvienas kanalas ar svetainė traktuojami kaip atskiros įmonės, vartotojo autentifikavimo srautų „Commerce“ aplinkoje atžvilgiu geriausia yra naudoti atskirus juridinius subjektus. Tačiau jei norite, kad kiekvienas kanalas / svetainė liktų toje pačioje aplinkoje ir juridiniame subjekte, bet kiekviena svetainė turėtų atskirą vartotojo autentifikavimą, svarbu, kad prieš tęsdami atsižvelgtumėte į šiuos punktus:

- Vartotojai turės savo individualius kredencialus kiekvienam kanalui / svetainei.

    Tas pats asmuo gali turėti dvi atskiras kiekvieno kanalo / svetainės paskyras, nes kiekviena paskyra bus unikalus įrašas atskiram B2C nuomotojui.

- „Microsoft Dynamics“ aplinkoje į visuotines įrašų paieškas bus sugrąžinti atskiri kliento įrašai.

    Jei vartotojas naudoja tą patį el. pašto adresą kanaluose / svetainėse, visuotinės klientų paieškos sugrąžins kiekvieno kanalo / svetainės rezultatus. (Bus rodomas kanalo indikatorius.)

- Adresų knygelė gali būti naudojama vartotojams grupuoti, kad juos būtų galima sekti per kanalą.
- Kliento įrašų skaičius kanalui gali padidėti, o šis padidinimas gali paveikti visuotinių klientų paieškų efektyvumą.
- B2C nuomotojai turi būti rūpestingai susieti su kanalu siekiant padėti išvengti situacijų, kai klientai užsiregistruoja prie klaidingo nuomotojo. Kitu atveju gali kilti neaiškumų arba sekimo problemų.

Toliau pateiktoje iliustracijoje parodomi keli B2C nuomotojai „Commerce“ aplinkoje.

![Keli B2C nuomotojai „Commerce“ aplinkoje](media/MultiB2C_In_Environment.png)

Jei nuspręsite, kad jūsų verslui reikia individualių B2C nuomotojų vienam kanalui toje pačioje „Commerce“ aplinkoje, atlikite tolesniuose skyriuose esančias procedūras, kad galėtumėte užklausti šią funkciją.

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>Užklausti, kad jūsų aplinkoje būtų įjungtas B2C kanalui

Šiuo metu, jei norite, kad individualūs B2C nuomotojai kanalui būtų pasiekiami toje pačioje „Commerce“ aplinkoje, turite pateikti užklausą „Dynamics 365 Commerce“. Norėdami gauti daugiau informacijos, žr. [Gauti „Lifecycle Services“ (LCS) palaikymą](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) arba aptarkite problemą su savo "Commerce“ sprendimų kontaktiniu asmeniu.

## <a name="configure-b2c-tenants-in-your-environment"></a>B2C nuomotojų konfigūravimas savo aplinkoje

Norėdami sukonfigūruoti B2C nuomotojus savo aplinkoje, atlikite atitinkamas procedūras šiame skyriuje.

### <a name="add-an-azure-ad-b2c-tenant"></a>„Azure AD“ B2C nuomotojo įtraukimas

Norėdami pridėti „Azure AD“ B2C nuomotoją prie savo aplinkos, atlikite šiuos veiksmus.

1. Prisijunkite prie savo aplinkos „Commerce“ svetainės kūrimo įrankio kaip sistemos administratorius. Norėdami sukonfigūruoti „Azure AD“ B2C nuomotojus, turite būti „Commerce“ sistemos administratorius.
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Nuomotojo parametrai**.
1. Pasirinkite **B2C parametrai**, tada pasirinkite **Valdyti**.
1. Pasirinkite **Įtraukti B2C programą**, o tada įveskite šią informaciją:

    - **Programos pavadinimas**: įveskite pavadinimą, kuris turi būti naudojamas programoje valdymo „Commerce“ aplinkoje kontekste. Rekomenduojame naudoti programos pavadinimą, kurį pasirinkote nustatydami „Azure AD“ B2C programą „Azure“ portale. Tokiu būdu galite padėti išvengti neaiškumų, kai valdote B2C nuomotojus „Commerce“ aplinkoje.
    - **Nuomotojo vardas**: įveskite B2C nuomotojo pavadinimą, kaip jis rodomas „Azure“ portale.
    - **Pamiršti slaptažodžio strategijos ID**: įveskite strategijos ID (strategijos pavadinimą „Azure“ portale).
    - **Registruoti / prijungti strategijos ID**: įveskite strategijos ID (strategijos pavadinimą „Azure“ portale).
    - **Kliento GUID**: įveskite „Azure AD“ B2C nuomotojo ID, kaip jis rodomas „Azure“ portale (ne programos ID B2C nuomotojui).
    - **Redaguoti profilio strategijos ID**: įveskite strategijos ID (strategijos pavadinimą „Azure“ portale).

1. Įvedę šią informaciją, pasirinkite **Gerai**, kad įrašytumėte pakeitimus.

> [!NOTE]
> Turite palikti laukus, pvz., **Aprėptis**, **Neinteraktyvios strategijos ID**, **Neinteraktyvaus kliento ID**, **Prisijungumo pasirinktinis domenas** ir **Registruoti strategijos ID**, tuščius, nebent „Dynamics 365 Commerce“ komanda nurodo jas nustatyti.
Dabar jūsų naujas „Azure AD“ B2C nuomotojas turi pasirodyti sąraše po **Tvarkyti B2C programas**.

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>„Azure AD“ B2C nuomotojo tvarkymas arba naikinimas

1. Prisijunkite prie savo aplinkos „Commerce“ svetainės kūrimo įrankio kaip sistemos administratorius. Norėdami sukonfigūruoti „Azure AD“ B2C nuomotojus, turite būti „Commerce“ sistemos administratorius.
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Nuomotojo parametrai**.
1. Pasirinkite **B2C parametrai**, tada pasirinkite **Valdyti**.
1. Norėdami redaguoti B2C nuomotoją, pasirinkite šalia jo esantį pieštuko simbolį. Norėdami panaikinti B2C nuomotoją, pasirinkite šalia jo esantį šiukšliadėžės simbolį.
1. Norėdami suaktyvinti savo keitimus, paspauskite **Įrašyti** ir pasirinkite **Publikuoti**.

> [!WARNING]
> Kai B2C nuomotojas sukonfigūruotas paleistoje / publikuotoje svetainėje, vartotojai gali būti prisiregistravę naudojant su nuomotoju esančias paskyras. Jei panaikinsite sukonfigūruotą nuomotoją meniu **Nuomotojo parametrai\> B2C nuomotojas**, jūs pašalinsite to B2C nuomotojo svetainių, kurios susietos su bet kuriuo nuomotojo kanalu, susiejimą. Šiuo atveju vartotojai gali nebegalėti prisijungti prie savo paskyrų. Todėl kai panaikinate sukonfigūruotą nuomotoją, būkite itin atsargūs.
>
> Kai sukonfigūruotas nuomotojas panaikinamas, B2C nuomotojas ir jo įrašai bus išlaikyti, tačiau to nuomotojo „Commerce“ sistemos konfigūracija bus pakeista arba pašalinta. Vartotojai, kurie bando užsiregistruoti ar prisijungti prie svetainės, sukurs naują paskyros įrašą numatytame arba naujai susietame B2C, kuris sukonfigūruotas svetainės kanalui.
## <a name="configure-your-channel-with-a-b2c-tenant"></a>Savo kanalo konfigūravimas su B2C nuomotoju

1. Prisijunkite prie savo aplinkos „Commerce“ svetainės kūrimo įrankio kaip sistemos administratorius. Norėdami sukonfigūruoti „Azure AD“ B2C nuomotojus, turite būti „Commerce“ sistemos administratorius.
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.
1. Pasirinkite **Kanalai** ir pasirinkite kanalą, kurį norite konfigūruoti.
1. Dešinėje esančioje ypatybių srityje esančiame lauke **Pasirinkti B2C programą** pasirinkite sukonfigūruotą „Azure AD“ B2C nuomotoją, kurį norite naudoti šiam kanalui.
1. Komandų juostoje pasirinkite **Įrašyti ir publikuoti**, kad patvirtinutmėte naują arba atnaujintą konfigūraciją.

> [!WARNING]
> Pakeitus B2C programą, priskirtą kanalui, pašalinamos dabartinės nuorodos, kurios buvo nustatytos visiems vartotojams, kurie jau yra užsiregistravę aplinkoje. Šiuo atveju bet kokie kredencialai, susieti su šiuo metu priskirta B2C programa, nebus prieinami vartotojams. Todėl keiskite kanalo „Azure AD“ B2C konfigūraciją tik jei nustatote kanalą pirmą kartą ir nėra užsiregistravusių vartotojų. Kitu atveju vartotojams gali reikėti registruotis iš naujo, kad būtų sukurtas įrašas naujame „Azure AD“ B2C nuomotoje.
## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

[E. prekybos svetainės kūrimas](create-ecommerce-site.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[„Robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
