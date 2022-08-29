---
title: Tvarkyti SEO metaduomenis
description: Šiame straipsnyje aprašoma, kaip valdyti ieškos modulio optimizavimo (VZ) metaduomenis, kurie yra Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4b04d675a903279e667e1f5fcee387f05d979e81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276834"
---
# <a name="manage-seo-metadata"></a>Tvarkyti SEO metaduomenis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip valdyti ieškos modulio optimizavimo (VZ) metaduomenis, kurie yra Microsoft Dynamics 365 Commerce.

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
1. Puslapio rengyklės puslapio viršuje, kairėje pusėje, puslapio struktūros valdiklio viršuje pasirinkite **parinktį** Struktūros režimas (pavarų simbolis), tada pasirinkite Išplėstinio **struktūros rodinį**.
1. Struktūros rodinyje išplėskite medžio valdiklius, kad būtų rodomas HTML pagrindinės atminties **turinys**.
1. HTML atžymoje **pasirinkite norimą CB modulį (pvz.,** **Puslapio suvestinė,** Produkto puslapio **suvestinė,** Kategorijos puslapio suvestinė **ar** Metatags **·**).
1. Dešinėje pusėje esančioje ypatybės srityje redaguokite norimus PASIRINKTO CB modulio duomenis (pvz., **Title**, **Description** arba **Sharing image**).
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Komentarų **lauke** įveskite atnaujintus **JŪSŲ duomenis** ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**. Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.
1. Pasirinkite **Publikuoti**.

> [!TIP]
> Autoriai, **norėdami** perjungti pagrindinį struktūros rodinį į papildomą struktūros rodinį, gali naudoti parinktį Struktūros režimas (pavarų simbolis), **·** **esanti puslapio doroklio kairiojo struktūros valdiklio viršuje**. **Pagrindinis struktūros rodinys** yra numatytasis parametras ir filtruoja struktūrą, kad **joje būtų rodomi tik puslapio body** HTML laiko atžymos moduliai. **Išplėstinio struktūros rodinys** rodo visą puslapio modulį, įskaitant **HTML viršus**, **kūno pradžios** ir kūno pabaigos **atžymas**. Šis rodinys naudingas, kai autoriai turi redaguoti konkrečius ŠIO arba scenarijaus modulio puslapio parametrus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modifikuoti esamą svetainės puslapį](modify-existing-page.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Pasirinkti puslapių maketus](select-page-layouts.md)

[Įrašyti, peržiūrėti ir publikuoti puslapį](save-preview-publish-page.md)

[Papildyti produkto puslapį](enrich-product-page.md)

[Papildyti kategorijos nukreipimo puslapį](enrich-category-page.md)

[Patikrinti puslapio turinio pritaikymą neįgaliesiems](verify-accessibility.md)

[Sukurti dinaminius e-komercijos puslapius pagal URL parametrus](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
