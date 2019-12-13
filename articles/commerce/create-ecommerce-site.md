---
title: E. prekybos svetainės kūrimas
description: Šioje temoje aprašomos užduotys, susijusios su naujos el. prekybos svetainės kūrimu programoje „Dynamics 365 Commerce“.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697134"
---
# <a name="create-an-e-commerce-site"></a>E. prekybos svetainės kūrimas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomos užduotys, susijusios su naujos el. prekybos svetainės kūrimu programoje „Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Norėdami pradėti kurti savo el. prekybos svetainę, pirmiausia turite sukurti naują svetainę svetainės kūrimo aplinkoje. Kad galėtumėte kurti naują svetainę, programoje „Dynamics 365 Retail“ reikia sukurti bent vieną internetinę parduotuvę. 

## <a name="set-up-your-site"></a>Svetainės nustatymas

Norėdami nustatyti svetainę, atlikite toliau nurodytus veiksmus.

1. Sprendime „Microsoft Lifecycle Services“ (LCS) pasirinkite svetainės kūrimo aplinkos saitą. 
1. Svetainės kūrimo aplinkos pagrindiniame puslapyje pasirinkite **Nauja svetainė**.
1. Dialogo lange **Nauja svetainė** nurodykite tolesnę informaciją.

| Laukas                               | Aprašymas |
|-------------------------------------|-------------|
| Svetainės pavadinimas                           | Įveskite rodomą svetainės pavadinimą, kuris turi būti naudojamas svetainės kūrimo aplinkoje. Šis pavadinimas matomas tik kūrimo aplinkoje ir klientams rodomas nebus. |
| Svetainės administratoriaus saugos grupė | Nurodykite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupę, valdančią vartotojus, kuriems šioje svetainėje priskirtas svetainės administratoriaus vaidmuo. |
| Numatytasis kanalas (valdymo vieneto numeris) | Pasirinkite internetinę parduotuvę, kurios el. parduotuvė bus ši svetainė. Jei norite, kad el. prekybos svetainė palaikytų kelias internetines parduotuves, po to, kai svetainė nustatoma, turite parduotuves susieti su savo svetaine dalyje **Svetainės parametrai**. |
| Numatytoji kalba                            | Nurodykite numatytąją šios internetinės parduotuvės ir rinkos kalbą. Internetinė parduotuvė gali palaikyti kelias kalbas. Jei norite, kad ši arba kita internetinė parduotuvė palaikytų kelias kalbas, tai turite sukonfigūruoti dalyje **Svetainės parametrai**, kai svetainė nustatyta.  |
| Domenas                              | Pasirinkite domeno vardą, kuris bus šios internetinės parduotuvės domenas. Jei sprendime LCS nekonfigūravote jokių domenų, šį lauką galite palikti tuščią. Sukonfigūravę domeną sprendime LCS, jį turite įtraukti į internetinę parduotuvę dalyje **Svetainės parametrai**.  |
| Maršrutas                              | Kai jūsų svetainė palaiko daugiau nei vieną tam tikro domeno vardo kalbą, naudodami kelio lauką sukurkite unikalų to domeno ir kalbos derinio svetainės URL. Jei kalba, kurią nurodėte lauke **Numatytoji kalba**, yra vienintelė palaikoma šio domeno kalba arba toliau bus numatytoji kalba jums svetainę lokalizavus papildomomis kalbomis, rekomenduojame šį lauką palikti tuščią. |


Sukūrę svetainę, patikrinti, ar ji susieta su internetine parduotuve, galite pasirinkdami skirtuką **Produktai**. Turėtumėte matyti produktų asortimentą, priskirtą internetinei parduotuvei. Taip pat galite naudoti viršutinėje kairiojoje puslapio dalyje esantį išplečiamąjį meniu ir priskirtus produktus pasiekti pagal kategoriją.

## <a name="additional-resources"></a>Papildomi ištekliai

[Interneto parduotuvės peržiūra](online-store-overview.md)

[Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Įgalinti parduotuvės nustatymą pagal vietą](enable-store-detection.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[Turinio kūrimo pagrindinio puslapio peržiūra](authoring-home-overview.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)
