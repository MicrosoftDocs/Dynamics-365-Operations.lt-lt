---
title: Globalizacijos funkcijos užbaigimas, publikavimas ir diegimas
description: Šiame straipsnyje pateikiama informacija apie globalizavimo funkcijų ciklą.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 9d4a408f2169b220fefd9ab7e9f3b37217fb3cfe
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710841"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Globalizacijos funkcijos užbaigimas, publikavimas ir diegimas

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Elektroninių SF išrašymo priemonių versijos

Elektroninių SF išrašymo priemonės yra versijos. Sukūrus naują versiją, versijos numeris automatiškai padidinamas.

Elektroninių SF išrašymo priemonių versijos veikia pagal ciklą, kuriame yra iki trijų būsenų:

- **Juodraštis** – kai priemonės versija yra šios būsenos, galite redaguoti jos konfigūracijos atributus ir artefaktus (pvz., failo formato konfigūracijas).
- **Atlikta** – ši būsena nurodo, kad baigėte redaguoti funkcijos versiją ir neketinate ją atnaujinti. Kai priemonės versija turi šią būseną, nebegalite jos redaguoti ar kurio nors iš jos komponentų.
- **Publikuota** – ši būsena nurodo, kad priemonės versija publikuota visuotinje saugykloje, kuri susieta su jūsų organizacija. Kai priemonės versija turi šią būseną, nebegalite jos redaguoti ar kurio nors iš jos komponentų.

Galite nurodyti naujos **elektroninių SF** išrašymo priemonės versijos galiojimo pradžios datą. Tokiu būdu galite nurodyti numatytąją versiją, kurią galima naudoti arba kurią galima perrašyti, kai funkcija įdiegta paslaugų aplinkoje.

Norėdami pakeisti elektroninės SF išrašymo priemonės versijos būseną, atlikite šiuos veiksmus.

1. Prisijungti prie savo reguliavimo kongigūravimo paslaugų (RCS) paskyros.
2. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
3. Kairėje elektroninio SF išrašymo **priemonių puslapio pusėje** pasirinkite elektroninių SF išrašymo priemonę.
4. **Skirtuko Versijos** puslapio dešinėje pusėje pasirinkite versiją.
5. Pasirinkite **būsenos Keitimas**, o tada pasirinkite **Atlikta** (jei dabartinė būsena yra **Juodraštis** **) arba Publikuota** (jei dabartinė būsena yra **Baigta**).
6. Pranešimo lauke pasirinkite Taip, kad **patvirtintumėte** užklausą.

Neautomatinis keitimas iš **būsenos** Baigta į Publikuota **yra** pasirinktinis. Elektroninių SF išrašymo priemonių versijos automatiškai atnaujinamos **į** būseną Publikuota, kai jos įdiegiamos į aptarnavimo aplinką.

Galite sekti būseną skirtuko Versijos **stulpelyje** Priemonės **versija**.

## <a name="deploy-feature-versions"></a>Diegti funkcijų versijas

RCS naudojate komandą **Diegti** norėdami publikuoti elektroninių SF išrašymo funkcijos versiją paskirties tarnybos aplinkoje arba prijungtoje programoje.

1. Kairėje elektroninio SF išrašymo **priemonių puslapio pusėje** pasirinkite elektroninių SF išrašymo priemonę.
2. Skirtuko Versijos **puslapyje**, dešinėje puslapio pusėje, pasirinkite elektroninių SF išrašymo priemonės versiją, kurią norite diegti į aptarnavimo aplinką arba prijungtą programą. Pasirinktos versijos būsena turi būti Baigta **arba** **Publikuota**.
3. Pasirinkite **Diegti**, tada pasirinkite vieną arba abi šias parinktis, kad apibrėžtumėte diegimo tikslą:

    - **Prijungta programa** – tai pasirinktinė, bet turi būti naudojama, jei norite, kad konfigūravimas, pateiktas programos nustatyme, būtų įrašytas Microsoft Dynamics į 365 Dynamics 365 Supply Chain Management finansų egzempliorių arba anksčiau buvo su juo susietas. Praleidus šio tipo diegimą reikia rankiniu būdu konfigūruoti parametrus, apibrėžtus finansų arba tiekimo grandinės valdymo programos nustatyme.
    - **Tarnybos aplinka** – į aptarnavimo aplinką įdiegia elektroninio SF išrašymo priemonės versiją. Tada elektroninis SF išrašymas yra paruoštas gauti ir apdoroti elektroninius dokumentus, kuriuos siunčia finansų ar tiekimo grandinės valdymas.

> [!NOTE]
> Paprastai jūs pakeisite elektroninių ataskaitų (ER) funkcijos, kurią reikia įdiegti į aptarnavimo aplinką, parametrus. Prisijungusio prašymo pakeitimai bus reti. Naujas versijas turėtumėte įdiegti tik prijungtai programai tik keisdami atitinkamus savo programos parametrus.

Norėdami nustatyti, ar tam tikros versijos elektroninių SF išrašymo funkcija įdiegta tam tikroje aplinkoje, peržiūrėkite informaciją skirtuke **Aplinkos**.

## <a name="remove-feature-versions"></a>Pašalinti priemonių versijas

RCS galite iš aptarnavimo **aplinkos** pašalinti konkrečią elektroninių SF išrašymo funkcijos versiją, jei ji buvo įdiegta ten.

> [!IMPORTANT]
> Mygtukas **Atšaukti** veikia tik aptarnavimo aplinkose. Ji neišjungia nieko iš susijusios programos dabartinei elektroninių SF išrašymo funkcijai.

## <a name="rebase-electronic-invoicing-features"></a>Perbase elektroninių SF išrašymo priemones

Kai viena elektroninio SF išrašymo priemonė išvedama iš kitos, **galite pasirinkti Rebase**, kad atnaujindami išvestąją priemonę pakeitimais, kurie buvo atlikti pradinėje (pirminėje) priemonėje.

Norėdami iš naujo sukurti išvestinės priemonės versiją, atlikite šiuos veiksmus.

1. Gauti naujausią priemonės versiją importuojant ją iš visuotinės saugyklos. Daugiau informacijos rasite Importavimo [funkcija iš visuotinės saugyklos](e-invoicing-import-feature-global-repository.md).
2. Funkcijų sąraše pasirinkite funkciją, kurią norite pritaikyti kitoje vietoje.
3. Skirtuke **Versijos pasirinkite** Naujas, kad sukurtumėte **juodraščio** versiją.
4. Pasirinkite **Pritaikyti kitoje vietoje**.
5. Dialogo lange **Perba** duomenų bazė pasirinkite priemonės, į kurią norite perbase, versiją.
6. Pasirinkite **Gerai**.
7. Peržiūrėkite funkcijos komponentus ir atlikite būtinus pakeitimus.
8. Pasirinkite **Pakeisti būseną**, kad užbaigtumėte pritaikytą kitoje vietoje funkciją. Kai pritaikymas kitoje vietoje baigiamas, galite atlikti papildomus veiksmus.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Gauti konkrečią elektroninių SF išrašymo priemonių versiją

Kai sukuriate naują elektroninio SF išrašymo priemonės versiją, sistema sukuria paskutinės funkcijos versijos kopiją. Jei norite naudoti ankstesnę funkcijos versiją kaip naujos versijos pagrindą, pasirinkite versiją, tada pasirinkite Gauti **šią versijos komandą**. Sukuriama nauja priemonės juodraščio versija, kuri yra pasirinktos versijos kopija.
