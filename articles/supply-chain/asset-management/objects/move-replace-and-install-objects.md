---
title: Turto perkėlimas, keitimas ir diegimas
description: Šiame straipsnyje paaiškinama, kaip perkelti, pakeisti ir įdiegti turtą turto valdymo dalyje.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a6b5a2904d21782ae422d06eaaf03c5d5e51ab9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015585"
---
# <a name="move-replace-and-install-assets"></a>Turto perkėlimas, keitimas ir diegimas

[!include [banner](../../includes/banner.md)]

 

Šiame straipsnyje paaiškinama, kaip perkelti, pakeisti ir įdiegti turtą turto valdymo dalyje. Galima sukurti atskirą turtą, kuris neturi jokių ryšių su kitu turtu, arba galima sukurti turto struktūrą, apimančią pagrindinį turtą (aukščiausio lygio turtas) ir susijusį antrinį turtą (antrinis turtas). Turto valdyme yra trys būdai kaip galima perkelti ir keisti turto vietą:

- **Perkelti** – perkelkite turtą į kitą turto struktūrą arba į kitą tos pačios turto struktūros vietą.
- **Pakeisti** – laikinai pašalinkite turtą iš turto struktūros, kad jį būtų galima pataisyti arba atnaujinti, o vėliau vėl įtraukti atnaujintą turtą į turto struktūrą. Taip pat galima visam laikui pakeisti naudotą turtą nauju turtu.
- **Diegti** – funkcinėje vietoje diekite pagrindinį turtą ir visus susijusius antrinius turtus.

> [!NOTE]
> Turtas, kurį perkeliate, pakeičiate arba įdiegiate, gali būti susijęs su kita funkcine vieta. Tokiu atveju turtas gali naudoti funkcinei vietai skirtas finansines dimensijas. Puslapyje **Funkcinių vietų tipai** nustatomas funkcinių vietų finansinių dimensijų valdymas.

## <a name="move-asset"></a>Turto perkėlimas

Norėdami perkelti turtą į kitą turto struktūrą arba į kitą tos pačios turto struktūros vietą naudokite funkciją **Perkelti turtą**. Taip pat galima perkelti turtą iš turto struktūros, kad jis taptų atskiru turtu be jokių struktūros ryšių.

> [!NOTE]
> Nenaudokite šios funkcijos, jei turtas atnaujinamas arba laikinai pakeičiamas. Todėl naudokite funkciją **Pakeisti turtą**, kuri toliau aprašyta šiame straipsnyje.

1. Pasirinkite Turto **valdymo turtas** \> **Visas** \> **turtas arba** Aktyvus **turtas.**
2. Sąraše pasirinkite perkeliamą turtą. Jei turtas turi antrinį turtą, taip pat perkelsite ir tą turtą.
3. Pasirinkite **Perkelti turtą**.
4. Norėdami perkelti turtą taip, kad jis taptų turto struktūros dalimi, pasirinkite naują pagrindinį turtą lauke **Pagrindinis turtas**. Jei perkeliate antrinį turtą ir norite jį padaryti atskiru turtu, be jokių struktūros ryšių, lauką **Pagrindinis turtas** palikite tuščią.
5. Pagal numatytuosius nustatymus lauke **Galioja** nustatoma dabartinė data ir laikas. Tačiau galima pasirinkti kitą datą ir laiką, nuo kurio pradeda galioti turto perkėlimas.
6. Pasirinkite **Gerai**.

## <a name="replace-asset"></a>Turto pakeitimas

Funkciją **Pakeisti turtą** naudokite norėdami remontuoti, atnaujinti ar visam laikui pakeisti susidėvėjusį turtą nauju turtu. Ši funkcija naudojama pakeisti antrinį turtą turto struktūroje. Pagrindiniam turtui (t. y. turtui, kuris šiuo metu neturi pagrindinio turto) šis pakeitimas atliekamas funkcinėje vietoje. Daugiau informacijos apie tai, kaip pakeisti pagrindinį turtą funkcinėje vietoje žr. [Turto diegimas funkcinėse vietose](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Jei remonto dirbtuvės susietos su gamybos skyriumi, galima kurti funkcines vietas, pvz. **Remonto dirbtuvės**, **Atliekos** ir **Saugykla**, kad būtų galima tvarkyti turto remontą ir pakeitimą.

1. Pasirinkite Turto **valdymo turtas** \> **Visas** \> **turtas arba** Aktyvus **turtas.**
2. Sąraše pasirinkite antrinį turtą, kurį norite pakeisti. Jei turtas turi antrinį turtą, taip pat pakeičiamas ir tas turtas.
3. Pasirinkite **Pakeisti turtą**.

    Lauke **Struktūros keitimas** rodoma paskutinė data ir laikas, kada pasirinktas turtas ir susijęs antrinis turtas buvo perkeltas į turto struktūrą.

4. Lauko **Tikslinė funkcinė vieta** dalyje **Pasirinktas turtas** pasirinkite funkcinę vietą, į kurią norite perkelti turtą. Pavyzdžiui, pasirinkite vietą **Remonto dirbtuvės** arba **Atliekos**.

    **Pagrindinis turtas** dalies lauke **Galioja** pateikta paskutinė data ir laikas, kada dabartinėje funkcinėje vietoje buvo įdiegtas arba perkeltas pagrindinis turtas ir susijęs antrinis turtas.

5. Dalies **Naujas turtas** lauke **Turtas** pasirinkite turtą, kurį norite įterpti kaip laikiną arba nuolatinį pakeičiamą turtą. Šis turtas šiuo metu gali būti kitoje funkcinėje vietoje, pvz. **Saugykla**.
7. Pagal numatytuosius nustatymus lauke dalies **Galioja nuo** lauke **Galioja** nustatoma dabartinė data ir laikas. Tačiau galima pasirinkti kitą datą ir laiką, nuo kurio pradeda galioti turto pakeitimas.
8. Pasirinkite **Gerai**.

## <a name="install-asset"></a>Turto diegimas

Naudokite funkciją **Diegti turtą**, kad įdiegtumėte turto struktūrą funkcinėje vietoje.

> [!NOTE]
> Visada pasirinkite pagrindinį turtą. Pagrindinis turtas ir su juo susijęs antrinis turtas bus perkeltas į pasirinktą funkcinę vietą.

1. Pasirinkite Turto **valdymo turtas** \> **Visas** \> **turtas arba** Aktyvus **turtas.**
2. Sąraše pasirinkite pagrindinį turtą, kurį norite įdiegti kitoje funkcinėje vietoje.
3. Pasirinkite **Diegti turtą**.

    Dalyje **Atributai** pateikti pagrindiniam turtui nustatyti atributai.

4. Lauke **Funkcinė vieta** pasirinkite naują vietą.
5. Pagal numatytuosius nustatymus lauke **Galioja** nustatoma dabartinė data ir laikas. Tačiau galima pasirinkti kitą datą ir laiką, nuo kurio pradeda galioti diegimas turto struktūroje.
6. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]