---
title: Dokumentų numeravimas ir kuponų chronologija
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir naudoti chronologinius numerius taikomiems dokumentams ir susijusiems kvitams.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.custom: 401195
ms.search.form: NumberSequenceGroup
ms.openlocfilehash: 1a1b8887eff625d9e4095380fbb7c8963682ef3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272435"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Dokumentų numeravimas ir kuponų chronologija

[!include [banner](../includes/banner.md)]


Kai kuriose šalyse galioja teisiniai reikalavimai numeruoti dokumentus ir susijusius kuponus chronologine tvarka. Chronologiją turi palaikyti laikotarpiai. Visi skaičiai, priklausantys ankstesniems laikotarpiams turi būti mažesni nei skaičiai priklausantys vėlesniems. Norėdami atitikti šį reikalavimą, buvo įdiegta chronologinių numerių funkcija. Šiame straipsnyje paaiškinama, kaip konfigūruoti ir naudoti chronologinius numerius taikomiems dokumentams ir susijusiems kvitams.

## <a name="prerequisites"></a>Būtinieji komponentai

Funkcijos valdymo darbo srityje įjunkite **Chronologinio numeravimo** funkciją. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Konfigūruokite chronologinį numeravimą

Chronologiniai numeravimai paveikia tolesnius dokumentus.

**Gautinos sumos**
- Kliento SF
- Kliento SF kvitas
- Pardavimo kredito pažyma
- Pardavimo kredito pažymos kvitas
- Laisvos formos SF
- Laisvos formos SF kvitas
- Laisvos formos kredito pažyma
- Laisvos formos kredito pažymos kvitas
- Važtaraštis
- Važtaraščio kvitas
- Važtaraščio pataisos kvitas
- Delspinigių pažymos kvitas
- Priminimo laiško kvitas

**Mokėtinos sumos**
- SF kvitas
- Kredito pažymos kvitas
- Gavimo dokumento kvitas

**Projektų valdymas**
- PVM sąskaita faktūra
- SF kvitas
- Kredito sąskaita
- Kredito pažymos kvitas 

### <a name="define-number-sequences"></a>Nustatykite skaičių sekas

Norėdami nustatyti skaičių sekas, eikite į **Organizacijos administravimas** > **Skaičių sekos** > **Skaičių sekos**. Galite nustatyti tiek skaičių sekų, kiek jums reikia padengti paveiktus laikotarpius būtiniems dokumentams. 

Nurodykite įmonę kiekvienai skaičių sekai. Skaičių sekos segmentai turi būti nustatyti taip, kad pateiktų chronologinę laikotarpių tvarką. Pavyzdžiui, segmento pavadinimai gali apimti specialius priešdėlius, kurie nurodo konkretų laikotarpį.

![Skaičių sekos nustatymai.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Konfigūruoti skaičių sekos grupes

Norėdami konfigūruoti skaičių sekos grupes, eikite į **Gautinos sąskaitos** > **Nustatymai** > **Gautinų sąskaitaų parametrai**. Skirtuke **Skaičių sekos** nustatykite tiek skaičių grupių, kiek jums reikia padengti paveiktų laikotarpių. 

Kiekvienai grupei **Nuorodos** skyriuje pasirinkite vieną palaikomą dokumento nuorodą ir **Skaičių sekos kodas** laukelyje nurodykite į skaičių seką, kuri anksčiau buvo sukurta susijusiam laikotarpiui.

![Numeravimo sekų grupės nustatymas.](media/chrono-num-sequence-group.jpg)

Panašiai, konfigūruokite skaičių sekų grupes **Mokėtinos sąskaitos** ir **Projekto valdymas ir apskaitos** moduliai.

### <a name="configure-number-sequence-groups-chronology"></a>Konfigūruoti skaičių sekos grupių chronologija

Norėdami konfigūruoti sekos grupių chronologiją, eikite į **Organizacijos administravimas** > **Skaičių sekos** > **Chronologinės skaičių sekos grupės**. Nustatykite taikomas sąlygas skaičių sekos grupėms.

![Chronologinių skaičių nustatymas.](media/chrono-num-sequence-group-period.jpg)

| Laukas            | Aprašas                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Galioja  | Skaičių sekos grupės taikomumo pradžios data. |
| Galiojimas      | Skaičių sekos grupės taikomumo pabaigos data. Jei netaikoma pabaigos data, pasirinkite **Niekada**. |
| Numeracijų grupė | Skaičių sekos grupė, kuri bus naudojama siekiant sukurti dokumentų skaičius laikotarpio metu. |
| Pradinė numerių sekų grupė | Šis skaičiaus sekos grupės kodas yra naudojamas papildomiems filtrams atvejais, kai dokumentai jau turi konkrečią priskirtą *nuolatinį* skaičiaus sekos grupę. Tuščia vertė yra laikoma konkrečia verte. Jei jums reikia ignoruoti preliminariai priskirtą grupę, naudokite **Nustatytąją** parinktį šiam nustatymui. |
| Numatyta | Jei įjungta, sistema ignoruos preliminariai paskirtą dokumento numerių skaičiaus grupę ir naudos tik laikotarpių pradžios ir pabaigos datas taikomumo analizei. Jei išjungta, sistema naudos visą kombinaciją **Galiojantis** + **Pabaigos** + **Originali skaičių sekos grupė** pasirinkimui. |

## <a name="document-posting"></a>Dokumento publikavimas
Jums publikuojant dokumentą, atitinkama skaičių sekos grupė yra priskirta dokumentai pagal jo publikavimo datą ir tuomet naudojama siekiant sukurti dokumento numerį pagal aptiktą skaičių seką. Sistema pateikia pranešimą dėl skaičiaus sekos grupės priskyrimo.

![Dokumento numeris.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> Kai kuriose šalyse yra konkreti jau dokumento numeravimui taikoma logika. Tokiu atveju, šaliai galiojanti konkreti logika viršys **Chronologinio numeravimo** funkciją.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
