---
title: „Robots.txt” failų tvarkymas
description: Šioje temoje aprašoma, kaip tvarkyti „robots.txt“ failus sprendime „Microsoft Dynamics 365 Commerce“.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
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
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4b3856a7a0b4b198e71ce9af6691b1d90362f3e7
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533418"
---
# <a name="manage-robotstxt-files"></a>„Robots.txt” failų tvarkymas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip tvarkyti „robots.txt“ failus sprendime „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Išimčių standartas robotams, arba „robots.txt“, yra standartas, kurį tinklapis naudoja bendrauti su interneto robotais. Juo nurodoma interneto robotams apie svetainės dalis, kurių robotas neturėtų pasiekti. Robotai dažnai naudojami ieškos moduliams indeksuojant svetaines.

Norėdami pašalinti robotus iš serverio, galite sukurti failą serveryje. Šiame faile nurodote robotų prieigos strategiją. Failas turi būti prieinama per HTTP vietinio URL **/robots.txt**. Failas „robots.txt“ padeda ieškos moduliui indeksuoti jūsų svetainės turinį.

Naudodami „Dynamics 365 Commerce“ galite nusiųsti savo domeno failą „robots.txt“. Kiekvienam „Commerce“ aplinkos domenui galite nusiųsti vieną failą „robots.txt“ ir susieti jį su tuo domenu.

Norėdami sužinoti daugiau informacijos apie failą „robots.txt“, apsilankykite [Interneto robotų puslapiai](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Failo „robots.txt“ nusiuntimas

Sukūrę ir redagavę savo „robots.txt“ failą pagal [robotų išimčių standartą](https://www.robotstxt.org/orig.html), įsitikinkite, kad failas yra pasiekiamas kompiuteryje, kuriame naudosite „Commerce“ kūrimo įrankius. Failas turi būti pavadintas **robots.txt**. Siekdami geriausių rezultatų, jis turi būti formatu, kuris yra nurodytas standarte. Kiekvienas „Commerce“ klientas yra atsakingas už failo „robots.txt“ turinio patvirtinimą ir palaikymą. Norėdami nusiųsti failą „robots.txt“, turite būti prisijungę prie „Commerce“ kaip sistemos administratorius.

Norėdami nusiųsti failą „robots.txt“ į „Commerce“, atlikite šiuos veiksmus.

1. Prisijunkite prie „Commerce“ kaip sistemos administratorius.
2. Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.
3. Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**. Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.
4. Pasirinkite **Valdyti**, kad nusiųstumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.
5. Dešinėje esančiame meniu pasirinkite mygtuką **Nusiųsti** (aukštyn nukreipta rodyklė) šalia domeno, susieto su failu „robots.txt“. Rodomas failo naršyklės dialogo langas.
6. Dialogo lange naršykite ir pasirinkite failą „robots.txt“, kurį norite nusiųsti į susietą domeną, ir pasirinkite **Atidaryti**, kad užbaigtumėte nusiuntimą.

> [!NOTE] 
> Įkėlimo metu „Commerce“ patikrina, ar failas yra tekstinis, bet nepatikrina failo turinio.

## <a name="download-a-robotstxt-file"></a>Failo „robots.txt“ atsisiuntimas

Norėdami atsisiųsti failą „robots.txt“ iš „Commerce“, atlikite šiuos veiksmus.

1. Prisijunkite prie „Commerce“ kaip sistemos administratorius.
2. Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.
3. Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**. Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.
4. Pasirinkite **Valdyti**, kad atsisiųstumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.
5. Dešinėje esančiame meniu pasirinkite mygtuką **Atsisiųsti** (žemyn nukreipta rodyklė) šalia domeno, susieto su failu „robots.txt“. Rodomas failo naršyklės dialogo langas.
6. Dialogo lange eikite į norimą vietą vietiniame diske, patvirtinkite arba įveskite failo vardą, tada pasirinkite **Įrašyti**, kad užbaigtumėte atsisiuntimą.

> [!NOTE]
> Ši procedūra gali būti naudojama atsisiųsti tik „robots.txt“ failų, kurie anksčiau buvo nusiųsti per „Commerce“ kūrimo įrankius.

## <a name="delete-a-robotstxt-file"></a>Failo „robots.txt“ naikinimas

Norėdami naikinti failą „robots.txt“ iš „Commerce“, atlikite šiuos veiksmus.

1. Prisijunkite prie „Commerce“ kaip sistemos administratorius.
2. Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.
3. Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**. Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.
4. Pasirinkite **Valdyti**, kad naikintumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.
5. Dešinėje esančiame meniu pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį šalia domeno, susieto su failu „robots.txt“. Atsiranda failų naršyklės langas.
6. Failų naršyklės lange naršykite ir pasirinkite failą „robots.txt“, kurį norite naikinti domene, ir pasirinkite **Atidaryti**. Pasirodys įspėjimo pranešimo langas.
7. Pranešimo lauke pasirinkite **Naikinti**, kad patvirtintumėte failo „robots.txt“ naikinimą.

> [!NOTE] 
> Ši procedūra gali būti naudojama naikinti tik „robots.txt“ failus, kurie anksčiau buvo nusiųsti per „Commerce“ kūrimo įrankius.

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

[El. prekybos svetainės kūrimas](create-ecommerce-site.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
