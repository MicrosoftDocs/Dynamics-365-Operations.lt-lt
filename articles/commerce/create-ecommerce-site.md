---
title: El. prekybos svetainės kūrimas
description: Šioje temoje aprašomi veiksmai ir pateikiama informacija, reikalinga kuriant naują El. prekybos svetainę „Dynamics 365 Commerce“ svetainių daryklėje.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096779"
---
# <a name="create-an-e-commerce-site"></a>El. prekybos svetainės kūrimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi veiksmai ir pateikiama informacija, reikalinga kuriant naują El. prekybos svetainę „Dynamics 365 Commerce“ svetainių daryklėje.

Prieš kurdami savo El. prekybos svetainę, pirma turite sukurti naują svetainę svetainių daryklėje. 


Norėdami pradėti kurti savo el. prekybos svetainę, pirmiausia turite sukurti naują svetainę svetainės kūrimo aplinkoje. Kad galėtumėte kurti naują svetainę, programoje „Commerce“ reikia sukurti bent vieną internetinę parduotuvę. 


## <a name="set-up-your-site"></a>Svetainės nustatymas

Norėdami nustatyti svetainę, atlikite toliau nurodytus veiksmus.

1. Atidarykite svetainių daryklės aplinką. „Microsoft Lifecycle Services“ (LCS) „Commerce“ aplinkos funkcijų puslapyje pateikiamas saitas į svetainių daryklę.
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

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

[Interneto parduotuvės kanalo integravimas](online-stores.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[„Robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
