---
title: Vaizdų nusiuntimas
description: Šioje temoje aprašoma, kaip įkelti vaizdus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.
author: psimolin
ms.date: 03/03/2020
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799234"
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
> Vaizdo ištekliai, kuriems priskirta kategorija, yra taip pat automatiškai žymimi kategorija kaip raktinis žodis, skirtas tam tikros kategorijos ištekliams ieškoti.

### <a name="naming-conventions-for-omni-channel-images"></a>Daugiakanalių vaizdų pavadinimo konvencijos 

Jei konfigūravote medijos biblioteką kaip daugiakanalio vaizdo posistemį, galite naudoti vaizdo kategorijas, kad nuordytumėte, kuriai kategorijai priklauso įkeltas vaizdas. Taip pat yra pavadinimų suteikimo konvencijos, kurių reikia laikytis siekiant užtikrinti, kad vaizdai būtų tinkamai nuskaityti kituose kanaluose, pvz., elektroniniame kasos aparate (EKA).

Numatytoji vardų suteikimo konvencija priklauso nuo kategorijos:
- Katalogo vaizdai turi būti pavadinti „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**“
- Kategorijos vaizdai turi būti pavadinti „**/Categories/\{CategoryName\}.png**“
- Kliento vaizdai turi būti pavadinti „**/Customers/\{CustomerNumber\}.jpg**“
- Darbuotojų vaizdai turi būti pavadinti „**/Workers/\{WorkerNumber\}.jpg**“
- Produkto vaizdai turi būti pavadinti „**/Products/\{ProductNumber\}_000_001.png**“
    - 001 yra vaizdo seka, kuri gali būti 001, 002, 003, 004 arba 005
- Produkto varianto vaizdai turi būti pavadinti „**/Produktai/\{Produkto numeris\} \^ \{Stilius\} \^ \{Dydis\} \^ \{Spalva\} \^\_000_001.png**”
    - Pavyzdžiui: 93039 \^\^2 \^ Juoda \^_000_001.png

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
