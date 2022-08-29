---
title: Vaizdo įrašų įkėlimas
description: Šiame straipsnyje aprašoma, kaip įkelti vaizdo įrašus į svetainės Microsoft Dynamics 365 Commerce generatorių.
author: josaw1
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 3f6c426984c84e657e99b12e9522080c3042db4a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278549"
---
# <a name="upload-videos"></a>Vaizdo įrašų įkėlimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įkelti vaizdo įrašus į svetainės Microsoft Dynamics 365 Commerce generatorių.

„Commerce“ svetainės generatoriaus medijos biblioteka leidžia įkelti vaizdo įrašus. Visada turite įkelti vaizdo įrašo, kurio aukščiausia sparta bitais ir skiriamoji geba, versiją, nes vaizdo įrašas bus automatiškai konvertuojamas ir bus tinkamas skirtingoms peržiūros sritims ir jų stabdos taškams.

### <a name="video-information-specified-during-upload"></a>Įkėlimo metu nurodyta vaizdo įrašo informacija

Įkeliant vaizdo įrašą galima nurodyti šią informaciją.

- **Pavadinimas, aprašas, raktiniai žodžiai**: vaizdo įrašo metaduomenys.
- **Automatiškai generuoti paslėptuosius titrus**: nurodo, ar turi būti automatiškai sugeneruotos paslėptieji vaizdo įrašo titrai (tik anglų kalba palaikoma). 
- **Paslėptieji titrai**: nurodo naudotinus paslėptuosius titrus.
- **Įprastas garsas**: nurodo įprastą garso įrašą, kuris bus naudojamas.
- **Miniatiūra**: nurodo vaizdo įrašo miniatiūrą. Jei miniatiūra nenustatyta, ji bus sugeneruota automatiškai.
- **Apibūdinamasis garsas**: nurodo apibūdinamąjį garso įrašą, kuris bus naudojamas.

## <a name="upload-a-video"></a>Vaizdo įrašo įkėlimas

Norėdami įkelti vaizdo įrašą svetainės generatoriuje, atlikite šiuos veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.
1. Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.
1. Failo naršyklės lange eikite į ir pasirinkite vieną ar daugiau vaizdo įrašo failų, kuriuos norite įkelti, tada pasirinkite **Atverti**.
1. Dialogo lange **Įkelti medijos elementą** įveskite reikiamą pavadinimą ir alternatyvųjį tekstą.
1. Įveskite pasirinktinį aprašą ir raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją. 
1. Norėdami iš karto po nusiuntimo publikuoti vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**
1. Pasirinkite **Gerai**.

Jei vienu metu įkeliate kelių tipų išteklius (pvz., vaizdus ir vaizdo įrašus), dialogo lange **Įkelti medijos elementą** galėsite nurodyti tik raktinius žodžius, ar failai bus publikuojami iš karto po įkėlimo, ir ar paslėptieji titrai turėtų būti automatiškai sugeneruoti vaizdo įrašams. Visi ištekliai naudos tuos pačius raktinius žodžius.

## <a name="additional-resources"></a>Papildomi ištekliai

[Skaitmeninių išteklių valdymo apžvalga](dam-overview.md)

[Vaizdų nusiuntimas](dam-upload-images.md)

[Įkelti failus](dam-upload-files.md)

[Vaizdų apkarpymas](dam-crop-images.md)

[Vaizdų centro tinkinimas](dam-custom-focal-point.md)

[Naujinti ir aptarnauti statinius failus](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
