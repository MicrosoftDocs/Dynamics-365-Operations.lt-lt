---
title: Modifikuoti esamą svetainės puslapį
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ modifikuoti esamą svetainės puslapį.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ddbef381e9ded18ed1c9226057cac482d4c6e24d
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698377"
---
# <a name="modify-an-existing-site-page"></a>Modifikuoti esamą svetainės puslapį

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ modifikuoti esamą svetainės puslapį.

## <a name="overview"></a>Peržiūrėti

Kai reikia modifikuoti puslapį, pirmausia jį atidarykite puslapio rengyklėje. Eikite į svetainę, kurioje yra jūsų puslapis, tada puslapių sąraše susiraskite norimą puslapį. Jei negalite rasti puslapio, galite naudoti kūrimo įrankio sudėtinės ieškos funkciją. Įveskite tikslų puslapio pavadinimą arba įveskite pirmas kelias jo raides, o tada – žvaigždutę (\*). Atsiranda filtruotas puslapių sąrašas. Galite naudoti šį sąrašą, norėdami rasti norimą puslapį. Radę teisingą puslapį, pasirinkite puslapio pavadinimą, kad puslapis būtų atidaromas puslapio rengyklėje.

> [!TIP]
> Jei puslapis matomas puslapio inspektoriuje, galite jį pasirinkti ir patikrinti prieš atidarydami jį puslapio rengyklėje. Tokiu būdu galite vienu metu patikrinti keletą puslapių.

Atidarę puslapį puslapio rengyklėje, turite įsitikinti, kad jis paimtas ir užrakintas. Kūrimo įrankio komandų juosta yra dinamiška, kontekstinė ir galinti skirti būsenas. Todėl joje rodomi tik veiksmai, kuriuos galite šiuo metu įvykdyti puslapyje. Pavyzdžiui, jei puslapis nepaimtas ir neužrakintas, komandų juostoje nerodomi mygtukai **Įrašyti** ir **Įrašyti ir atrakinti**. Taip pat puslapio būsena rodoma dešinėje lango pusėje.

Jei puslapis dar nepaimtas ir neužrakintas, pasirinkite komandų juostoje **Paimti ir užrakinti**. Komandų juosta pasikeičia, kad atsispindėtų nauja puslapio būsena. Taip pat gausite pranešimą, kuriame teigiama, kad puslapis paimtas ir užrakintas.

Kitas veiksmas – atlikti faktinius keitimus. Dažnai naudosite puslapio struktūros medį kairėje, norėdami rasti ir pasirinkti modulį, kurį norite keisti, o tada atliksite keitimus dešiniojoje ypatybių srityje. 

Tačiau jūsų keitimai kartais gali apimti modelių ar fragmentų pridėjimą arba pašalinimą. Norėdami įtraukti fragmentą ar modulį, naudokite puslapio struktūros medį, kad rastumėte atkarpą, į kurią norite įtraukti modulį arba fragmentą, ir tada pasirinkite daugtaškio mygtuką (**...**) tai atkarpai. Pasirodys meniu, kuriame yra komandų, skirtų pridėti modulį ar fragmentą. Norėdami pašalinti modulį arba fragmentą, suraskite ir pasirinkite jį puslapio struktūros medyje, pasirinkite daugtaškio mygtuką ir pasirinkite komandą, kad panaikintumėte modulį ar fragmentą.

> [!TIP]
> Taip pat galite peržiūrėti ir redaguoti bet kurio modulio, kuris matomas „ką matote, tą ir gaunate“ (WYSIWYG) peržiūoje, ypatybes, pasirinkdami jas tiesiogiai.

Atlikę keitimus ir peržiūrėję jų efektyvumą, turite puslapį įrašyti ir atrakinti, pasirinkdami komandų juostoje **Įrašyti ir atrakinti**. 

Norėdami nedelsiant publikuoti savo keitimus, komandų juostoje pasirinkite **Publikuoti**. Naujausia įrašyta ir atrakinta puslapio versija, kurią modifikavote, yra publikuojama ir tampa pasiekiama išoriniams vartotojams, kurie mato jūsų svetainę. 

## <a name="example-change-the-video-on-the-home-page"></a>Pavyzdys: Vaizdo įrašo keitimas pagrindiniame puslapyje

Šiame pavyzdyje parodyta, kaip modifikuoti pagrindinį puslapį, keičiant vaizdo įrašų leistuvo modulyje rodomą vaizdo įrašą.

1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairėje naršymo srityje pasirinkite **Puslapiai**.
1. Raskite ir pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.
1. Komandų juostoje pasirinkite **Paimti ir užrakinti**.
1. Puslapio struktūroje pasirinkite atkarpą **Pagrindinis**.
1. Atkarpoje **Pagrindinis** išplėskite visus nepastovius konteinerio modulius.
1. Suraskite ir pasirinkite vaizdo įrašų leistuvo modulį.
1. Dešiniojoje ypatybių srityje pasirinkite **vaizdo įrašo** ypatybę. Atsiranda išteklių parinkiklis.
1. Išteklių parinkiklyje pasirinkite galimą vaizdo įrašo išteklių arba pasirinkite **įkelti naują išteklių**, kad įkeltumėte naują vaizdo įrašo išteklių.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**, tada – **Įrašyti ir atrakinti**.
1. Lauke **Komentarai** įveskite **Pakeisti vaizdo įrašą** ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti atnaujintą puslapį, pasirinkite **Peržiūra**. Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.
1. Pasirinkite **Publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Pasirinkti puslapių maketus](select-page-layouts.md)

[Tvarkyti SEO metaduomenis](manage-seo-metadata.md)

[Įrašyti, peržiūrėti ir publikuoti puslapį](save-preview-publish-page.md)

[Papildyti produkto puslapį](enrich-product-page.md)

[Papildyti kategorijos nukreipimo puslapį](enrich-category-page.md)