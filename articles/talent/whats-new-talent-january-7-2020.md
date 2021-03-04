---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2020 m. sausio 7 d.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462002"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2020 m. sausio 7 d.)

Šiame straipsnyje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2697 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Negalima panaikinti darbininkų, kurie neturi įdarbinimo įrašų – (386157)

Šiuo keitimu į formą **Nedirbantys darbininkai** įtraukiama panaikinimo parinktis. Darbininkai rodomi šioje formoje, kai nėra įrašų apie būsimą, aktyvų arba praeityje buvusį įdarbinimą. Šiame leidime panaikinimo funkcija įjungta tik sistemos administratoriams. Tačiau kitą savaitę pasirodysiančiame leidime bus atnaujintos saugos funkcijos, todėl visi vartotojai, kuriems priskiriamas personalo asistento vaidmuo, galės panaikinti nedirbančius darbininkus. Šiuos keitimus taip pat galite atlikti neautomatiniu būdu, atlikdami tolesnius veiksmus.

1. Eikite į **Saugos konfigūracija**.
2. Skirtuke **Teisės** filtruokite sąrašą **Teisės**, kad būtų rodoma parinktis **Prižiūrėti darbininkus**.
3. Stulpelyje **Nuorodos** pasirinkite **Rodyti meniu elementus**.
4. **Rodyti meniu elementus** pasirinkite **HcmWOrkersWithoutEmployment**.
5. Prie funkcijos **Panaikinti** teisės pasirinkite „Suteikti”.
6. Pasirinkite skirtuką **Nepublikuoti objektai**.
7. Pasirinkite **Publikuoti viską**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]