---
title: Vaizdų nusiuntimas
description: Šioje temoje aprašoma, kaip įkelti vaizdus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.
author: psimolin
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3b99aeff7eafd788c19204e22dbfc61f45b25408
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891527"
---
# <a name="upload-images"></a>Vaizdų nusiuntimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip įkelti vaizdus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.

„Commerce“ svetainės generatoriaus medijų biblioteka leidžia įkelti vaizdus po vieną arba masiškai naudojant aplankus. Visada turite įkelti vaizdo, kurio aukščiausia skiriamoji geba ir kokybė, versiją, nes vaizdo dydžio keitimo komponentas automatiškai optimizuos vaizdą skirtingoms peržiūros sritims ir jų stabdos taškams.

### <a name="image-information-specified-during-upload"></a>Įkėlimo metu nurodyta vaizdo informacija

Įkėliant vaizdą, galima nurodyti šią informaciją.

- **Antraštė, alternatyvusis tekstas, aprašas, raktiniai žodžiai**: vaizdo arba vaizdo įrašo metaduomenys. Pavadinimas ir alternatyvusis tekstas yra būtinosios vertės.
- **Pasirinkti kategoriją**:
    - **Nėra**: naudojama „e-Commerce“ istorijų vaizdui ar vaizdams.
    - **Produktas, kategorija, klientas, darbuotojas, katalogas**: naudojamas „Dynamics 365 Commerce“ daugiakanalio vaizdui ar vaizdams.
- **Publikuoti išteklius po įkėlimo**: pažymėjus šį žymės langelį, vaizdas arba vaizdai publikuojami iš karto po įkėlimo.

> [!NOTE]
> - Vaizdo ištekliai, kuriems priskirta kategorija, yra taip pat automatiškai žymimi kategorija kaip raktinis žodis, skirtas tam tikros kategorijos ištekliams ieškoti.
> - Produkto informacijos puslapiai dinamiškai generuoja Alt tekstą naudodami produkto pavadinimą, todėl pakeitus produkto vaizdo Alt tekstą nebus **paveiktas** **atvaizduotas** vaizdas.

### <a name="naming-conventions-for-omni-channel-images"></a>Daugiakanalių vaizdų pavadinimo konvencijos 

Jei konfigūravote medijos biblioteką kaip daugiakanalio vaizdo posistemį, galite naudoti vaizdo kategorijas, kad nuordytumėte, kuriai kategorijai priklauso įkeltas vaizdas. Taip pat yra pavadinimų suteikimo konvencijos, kurių reikia laikytis siekiant užtikrinti, kad vaizdai būtų tinkamai nuskaityti kituose kanaluose, pvz., elektroniniame kasos aparate (EKA).

Numatytoji vardų suteikimo konvencija priklauso nuo kategorijos:
- Katalogo vaizdai turi būti pavadinti „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**“
- Kategorijos vaizdai turi būti pavadinti „**/Categories/\{CategoryName\}.png**“
- Kliento vaizdai turi būti pavadinti „**/Customers/\{CustomerNumber\}.jpg**“
- Darbuotojų vaizdai turi būti pavadinti „**/Workers/\{WorkerNumber\}.jpg**“
- Produkto vaizdai turi būti pavadinti „**/Products/\{ProductNumber\}\_000_001.png**”
    - 001 yra vaizdo seka, kuri gali būti 001, 002, 003, 004 arba 005
- Produkto varianto vaizdai turi būti pavadinti „**/Produktai/\{Produkto numeris\} \^ \{Stilius\} \^ \{Dydis\} \^ \{Spalva\} \^\_000_001.png**”
    - Pavyzdžiui: 93039 \^&nbsp;\^ 2 \^ Juoda \^\_000_001.png
- Produkto varianto vaizdai su konfigūracijos dimensija turi būti pavadinti „**/Produktai/\{ProductNumber\}\^\{Konfigūracija\}\_000_001.png**”
    - Pavyzdžiui: 93039 \^ LB8017_000_001.png

> [!NOTE]
> Suteikiant produkto varianto pavadinimą, jeigu dimensijos reikšmė tuščia, failo pavadinime turi būti du tarpai tarp įterpties ženklų.

Ankstesniuose pavyzdžiuose naudojama numatytoji konfigūracija. Skyriklio simbolį ir dimensijas galima konfigūruoti, o tikslūs pavadinimų suteikimo reikalavimai gali skirtis atsižvelgiant į įdiegtį. Vienas būdas sužinoti tikslius pavadinimų suteikimo konvencijos reikalavimus yra naudoti naršyklės programų kūrėjų konsolę, siekiant patikrinti produkto varianto vaizdo užklausas, keičiant produkto dimensijas parduotuvės produkto išsamios informacijos puslapyje (PDP).

## <a name="upload-an-image"></a>Įkelti vaizdą

Norėdami įkelti vaizdą svetainės generatoriuje, atlikite šiuos veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.
1. Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.
1. Failo naršyklės lange eikite į ir pasirinkite vieną ar daugiau vaizdų failų, kuriuos norite įkelti, tada pasirinkite **Atverti**.
1. Dialogo lange **Įkelti medijos elementą** įveskite reikiamą pavadinimą ir alternatyvųjį tekstą.
1. Įveskite pasirinktinį aprašą ir raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją. 
1. Norėdami iš karto po nusiuntimo publikuoti vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.
1. Pasirinkite **Gerai**.

## <a name="upload-a-folder-of-images"></a>Įkelti vaizdų aplanką

Norėdami masiškai įkelti vaizdų aplanką svetainės generatoriuje, atlikite šiuos veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.
1. Komandų juostoje pasirinkite **Įkelti \> Įkelti aplanką**.
1. Failo naršyklės lange eikite į ir pasirinkite aplanką, kurį norite įkelti, tada pasirinkite **Atverti**.
1. Dialogo lange **Įkelti medijos elementus** įveskite pasirinktinius raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją. 
1. Norėdami iš karto po nusiuntimo publikuoti aplanke esančius vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.
1. Pasirinkite **Gerai**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Skaitmeninių išteklių valdymo apžvalga](dam-overview.md)

[Vaizdo įrašų nusiuntimas](dam-upload-video.md)

[Įkelti failus](dam-upload-files.md)

[Vaizdų apkarpymas](dam-crop-images.md)

[Vaizdų centro tinkinimas](dam-custom-focal-point.md)

[Naujinti ir aptarnauti statinius failus](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
