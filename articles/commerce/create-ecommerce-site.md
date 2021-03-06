---
title: Sukurkite e-komercijos saitą
description: Ši tema aprašo žingsnius ir informaciją, kurie yra būtini norint sukurti e-komercijos saitą „Dynamics 365 Commerce“ saito kūrimo įrankyje.
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61fe44df7165780be2dd00be3f210ab2da05ddfe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795792"
---
# <a name="create-an-e-commerce-site"></a>Sukurkite e-komercijos saitą

[!include [banner](includes/banner.md)]

Ši tema aprašo žingsnius ir informaciją, kurie yra būtini norint sukurti e-komercijos saitą „Dynamics 365 Commerce“ saito kūrimo įrankyje.

Kai jūsų suteikiate licenciją „Dynamics 365 Commerce“ pajėgumams, saito kūrimo įrankis bus aprūpintas pradžios saitu, kurį galėsite naudoti pagal jūsų turimo saito pagrindus. Tačiau, jei norite pradėti nuo nulio, arba, jei norite sukurti antrą svetainę, turite sukurti naują svetainę svetainės kūrimo aplinkoje. 

## <a name="set-up-your-site"></a>Svetainės nustatymas

Norėdami nustatyti svetainę, atlikite toliau nurodytus veiksmus.

1. Atidarykite svetainių daryklės aplinką. „Microsoft Lifecycle Services“ (LCS) „Commerce“ aplinkos funkcijų puslapyje pateikiamas saitas į svetainių daryklę.
1. Svetainės kūrimo aplinkos pagrindiniame puslapyje pasirinkite **Nauja svetainė**.
1. Dialogo lange **Nauja svetainė** nurodykite tolesnę informaciją.

| Laukas                               | Aprašymas |
|-------------------------------------|-------------|
| Svetainės pavadinimas                           | Įveskite rodomą svetainės pavadinimą, kuris turi būti naudojamas svetainės kūrimo aplinkoje. Šis pavadinimas matomas tik kūrimo aplinkoje ir klientams rodomas nebus. |
| Svetainės administratoriaus saugos grupė | Nurodykite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupę, valdančią vartotojus, kuriems šioje svetainėje priskirtas svetainės administratoriaus vaidmuo. |
| Numatytasis kanalas (valdymo vieneto numeris) | Pasirinkite internetinę parduotuvę, kurios el. parduotuvė bus ši svetainė. Jei norite, kad jūsų e-komercijos saitas palaikytų keletą interneto parduotuvių, turite susieti parduotuves su jūsų saitu **Saito nustatymuose** nustačius saitą. |
| Numatytoji kalba                            | Nurodykite numatytąją šios internetinės parduotuvės ir rinkos kalbą. Internetinė parduotuvė gali palaikyti kelias kalbas. Jei norite, kad ši arba kita internetinė parduotuvė palaikytų kelias kalbas, tai turite sukonfigūruoti dalyje **Svetainės parametrai**, kai svetainė nustatyta.  |
| Domenas                              | Pasirinkite domeno vardą, kuris bus šios internetinės parduotuvės domenas. Jei sprendime LCS nekonfigūravote jokių domenų, šį lauką galite palikti tuščią. Sukonfigūravę domeną sprendime LCS, jį turite įtraukti į internetinę parduotuvę dalyje **Svetainės parametrai**.  |
| Maršrutas                              | Kai jūsų svetainė palaiko daugiau nei vieną tam tikro domeno vardo kalbą, naudodami kelio lauką sukurkite unikalų to domeno ir kalbos derinio svetainės URL. Jei kalba, kurią nurodėte lauke **Numatytoji kalba**, yra vienintelė palaikoma šio domeno kalba arba toliau bus numatytoji kalba jums svetainę lokalizavus papildomomis kalbomis, rekomenduojame šį lauką palikti tuščią. |


Sukūrę svetainę, patikrinti, ar ji susieta su internetine parduotuve, galite pasirinkdami skirtuką **Produktai**. Turėtumėte matyti produktų asortimentą, priskirtą internetinei parduotuvei. Taip pat galite naudoti viršutinėje kairiojoje puslapio dalyje esantį išplečiamąjį meniu ir priskirtus produktus pasiekti pagal kategoriją.

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Talpinkite naują e-komercijos nuomotoją](deploy-ecommerce-site.md)

[Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](associate-site-online-store.md)

[„robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]