---
title: Sukurkite e-komercijos saitą
description: Ši tema aprašo žingsnius ir informaciją, kurie yra būtini norint sukurti e-komercijos saitą „Dynamics 365 Commerce“ saito kūrimo įrankyje.
author: bicyclingfool
ms.date: 03/10/2022
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
ms.openlocfilehash: 37734e2ceea3a50c70a2f7945329d4a9cf660cc6
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402780"
---
# <a name="create-an-e-commerce-site"></a>Sukurkite e-komercijos saitą

[!include [banner](includes/banner.md)]

Ši tema aprašo žingsnius ir informaciją, kurie yra būtini norint sukurti e-komercijos saitą „Dynamics 365 Commerce“ saito kūrimo įrankyje.

Kai jūsų suteikiate licenciją „Dynamics 365 Commerce“ pajėgumams, saito kūrimo įrankis bus aprūpintas pradžios saitu, kurį galėsite naudoti pagal jūsų turimo saito pagrindus. Tačiau, jei norite pradėti nuo nulio, arba, jei norite sukurti antrą svetainę, turite sukurti naują svetainę svetainės kūrimo aplinkoje. 

## <a name="site-creation-prerequisites"></a>Būtinos vietos kūrimo sąlygos

Svetainės generatoriaus vartotojas turi turėti "Microsoft Azure Active Directory " (Azure AD) vartotojo abonementą, Azure AD įtrauktą į saugos grupę, priskirtą el. komercijos sistemos administratoriams. Norėdami gauti daugiau informacijos, žr [. naujo el. komercijos nuomininko diegimą](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD svečias jūsų nuomininke gali turėti skirtingas prieigos Azure AD teises. Net jeigu Azure AD įtraukta į saugos grupę, priskirtą el. komercijos sistemos administratoriams, Azure AD **svečiui** gali reikėti koreguoti išorinių vartotojų teisių parametrus, kad būtų galima sukurti el. komercijos svetainę "Commerce". 

Norėdami koreguoti išorinių Azure AD **vartotojų** nustatymus, atlikite šiuos veiksmus.

1. "Azure" portale pereikite į savo nuomininką Azure AD.
1. Eikite į **vartotojo parametrus \> Išoriniai vartotojai** ir pasirinkite saitą **Tvarkyti išorinius bendradarbiavimo** parametrus. Atidaromas išorinio **bendradarbiavimo puslapis**, kuriame galima nustatyti vartotojo prieigą, svečio kviesti parametrus ir bendradarbiavimo apribojimus. 
1. Koreguoti išorinius bendradarbiavimo parametrus pagal jūsų įmonės saugos strategijas. 

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

## <a name="rename-your-site"></a>Pervardykite savo svetainę

Norėdami pervardyti savo svetainę svetainės generatoriuje, atlikite šiuos veiksmus.

1. Norėdami atidaryti svetainių sąrašo rodinį, viršutiniame **dešiniajame** kampe pasirinkite Svetainės perjungimo priemonė, tada pasirinkite Tvarkyti **svetaines**. 
1. Pasirinkite žymės langelį, esantį šalia svetainės, kurią norite pervardyti, tada komandų **juostoje** pasirinkite Pervardyti.
1. Dialogo lange **Naujos svetainės** pavadinimas įveskite naują svetainės pavadinimą ir pasirinkite **Gerai**. Svetainės sąrašas bus atnaujinta, kad būtų rodomas naujas svetainės pavadinimas.

## <a name="delete-a-site"></a>Svetainės naikinimas

Norėdami panaikinti svetainę svetainės generatoriuje, atlikite šiuos veiksmus.

1. Norėdami atidaryti svetainių sąrašo rodinį, viršutiniame **dešiniajame** kampe pasirinkite Svetainės perjungimo priemonė, tada pasirinkite Tvarkyti **svetaines**.
1. Pasirinkite svetainę, kurią norite naikinti, tada komandų juostoje **pasirinkite** Naikinti.
1. Dialogo lange **\<site name\>** Naikinti įveskite svetainės pavadinimą ir pasirinkite **Naikinti**.

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
