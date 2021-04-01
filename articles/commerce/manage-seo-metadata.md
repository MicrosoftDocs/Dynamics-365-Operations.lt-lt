---
title: Tvarkyti SEO metaduomenis
description: Šioje temoje aprašoma, kaip valdyti ieškos modulio optimizavimo (SEO) metaduomenis programoje „Microsoft Dynamics 365 Commerce“.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00942befef9f9b6a878766bbbb5341426e31db2c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252611"
---
# <a name="manage-seo-metadata"></a>Tvarkyti SEO metaduomenis


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip valdyti ieškos modulio optimizavimo (SEO) metaduomenis programoje „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Svetainės SEO metaduomenys gali būti valdomi naudojant svetainės struktūromis ir puslapio metaduomenimis.
    
## <a name="site-maps"></a>Svetainės struktūros

Svetainės struktūra yra žiniatinklio svetainės puslapių XML formatu kompiuterio skaitomas sąrašas. Jis skirtas vartoti ieškos moduliuose, kad jie galėtų pateikti geresnius ieškos rezultatus jūsų svetainėje. Gali būti, kad svetainės struktūros neautomatiniu būdu parenkamos ieškos moduliui vartoti arba publikuojamos faile robots.txt.

„Dynamics 365 Commerce“ palaiko automatinį svetainės struktūrų generavimą. Svetainės struktūros atnaujinamos automatiškai, kai puslapiai publikuojami ar jų publikavimas atšaukiamas.

### <a name="turn-on-site-map-generation"></a>Svetainės struktūros generavimo įjungimas

1. Prisijunkite prie turinio kūrimo įrankio.
1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairėje naršymo srityje pasirinkite **Svetainės valdymas**.
1. Įsitikinkite, kad įjungta parinktis **Svetainės struktūros įgalintos**.

## <a name="page-metadata"></a>Puslapio metaduomenys

„Dynamics 365 Commerce“ galite tvarkyti atskirų puslapių SEO metaduomenis. Šią informaciją galite peržiūrėti ir modifikuoti puslapio konteinerio skyriuje **SEO ypatybės**. Toliau nurodytos SEO metaduomenų ypatybės yra palaikomos:

- Pareigos
- Aprašymas
- SEO raktažodžiai
- „Aria“ žymos
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Puslapio metaduomenų modifikavimas

Norėdami modifikuoti metaduomenis, atlikite šiuos veiksmus.

1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairėje naršymo srityje pasirinkite **Puslapiai**.
1. Pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.
1. Komandų juostoje pasirinkite **Redaguoti**.
1. Dešiniojoje ypatybių srityje išplėskite **Numatytosios metažymės**.
1. Norėdami įtraukti naują metažymę, pasirinkite **Įtraukti** ir lauke įveskite žymę. Norėdami pašalinti esamą metažymę, pasirinkite šiukšliadėžės simbolį jos dešinėje.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Lauke **Komentarai** įveskite **Atnaujintos metažymės** ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**. Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.
1. Pasirinkite **Publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modifikuoti esamą svetainės puslapį](modify-existing-page.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Pasirinkti puslapių maketus](select-page-layouts.md)

[Įrašyti, peržiūrėti ir publikuoti puslapį](save-preview-publish-page.md)

[Papildyti produkto puslapį](enrich-product-page.md)

[Papildyti kategorijos nukreipimo puslapį](enrich-category-page.md)

[Patikrinti puslapio turinio pritaikymą neįgaliesiems](verify-accessibility.md)

[Sukurti dinaminius e-komercijos puslapius pagal URL parameterus](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]