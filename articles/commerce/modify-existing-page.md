---
title: Modifikuoti esamą svetainės puslapį
description: Šiame straipsnyje aprašoma, kaip modifikuoti esamą svetainės puslapį Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/14/2020
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
ms.openlocfilehash: fb5348c2f29625647f06e48233f877a847677486
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286924"
---
# <a name="modify-an-existing-site-page"></a>Modifikuoti esamą svetainės puslapį

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip modifikuoti esamą svetainės puslapį Microsoft Dynamics 365 Commerce.

Kai reikia modifikuoti puslapį, pirmiausia jį atidarykite puslapio rengyklėje. Eikite į svetainę, kurioje yra jūsų puslapis, tada puslapių sąraše susiraskite norimą puslapį. Jei negalite rasti puslapio, galite naudoti kūrimo įrankio sudėtinės ieškos funkciją. Įveskite tikslų puslapio pavadinimą arba įveskite pirmas kelias jo raides, o tada – žvaigždutę (\*). Atsiranda filtruotas puslapių sąrašas. Galite naudoti šį sąrašą, norėdami rasti norimą puslapį. Radę teisingą puslapį, pasirinkite puslapio pavadinimą, kad puslapis būtų atidaromas puslapio rengyklėje.

> [!TIP]
> Jei puslapis matomas puslapio inspektoriuje, galite pasirinkti **Redaguoti** ir išregistruoti puslapį prieš atidarydami jį puslapio rengyklėje. Tokiu būdu galite vienu metu patikrinti keletą puslapių.

Atidarę puslapį puslapio rengyklėje, turite įsitikinti, kad jis paimtas ir užrakintas. Kūrimo įrankio komandų juosta yra dinamiška, kontekstinė ir galinti skirti būsenas. Todėl joje rodomi tik veiksmai, kuriuos galite šiuo metu įvykdyti puslapyje. Pavyzdžiui, jei puslapis nepaimtas ir neužrakintas, komandų juostoje nerodomi mygtukai **Įrašyti** ir **Baigti redagavimą**. Taip pat puslapio būsena rodoma dešinėje lango pusėje.

Jei puslapis dar nepaimtas ir neužrakintas, pasirinkite komandų juostoje **Redaguoti**. Komandų juosta pasikeičia, kad atsispindėtų nauja puslapio būsena. Taip pat gausite pranešimą, kuriame teigiama, kad puslapis paimtas ir užrakintas.

Kitas veiksmas – atlikti faktinius keitimus. Dažnai naudosite puslapio struktūros medį kairėje, norėdami rasti ir pasirinkti modulį, kurį norite keisti, o tada atliksite keitimus dešiniojoje ypatybių srityje. 

Tačiau jūsų keitimai kartais gali apimti modelių ar fragmentų pridėjimą arba pašalinimą. Norėdami įtraukti fragmentą ar modulį, naudokite puslapio struktūros medį, kad rastumėte atkarpą, į kurią norite įtraukti modulį arba fragmentą, ir tada pasirinkite daugtaškio mygtuką (**...**) tai atkarpai. Pasirodys meniu, kuriame yra komandų, skirtų pridėti modulį ar fragmentą. Norėdami pašalinti modulį arba fragmentą, suraskite ir pasirinkite jį puslapio struktūros medyje, pasirinkite daugtaškio mygtuką ir pasirinkite komandą, kad panaikintumėte modulį ar fragmentą.

> [!TIP]
> Taip pat galite peržiūrėti ir redaguoti bet kurio modulio, kuris matomas puslapio daryklės peržiūroje, ypatybes, pasirinkdami jas tiesiogiai.

Atlikę keitimus ir peržiūrėję jų efektyvumą, turite puslapį įrašyti ir atrakinti, pasirinkdami komandų juostoje **Baigti redagavimą**. 

Norėdami nedelsiant publikuoti savo keitimus, komandų juostoje pasirinkite **Publikuoti**. Naujausia įrašyta ir atrakinta puslapio versija, kurią modifikavote, yra publikuojama ir tampa pasiekiama išoriniams vartotojams, kurie mato jūsų svetainę. 

## <a name="example-change-the-video-on-the-home-page"></a>Pavyzdys: Vaizdo įrašo keitimas pagrindiniame puslapyje

Šiame pavyzdyje parodyta, kaip modifikuoti pagrindinį puslapį, keičiant vaizdo įrašų leistuvo modulyje rodomą vaizdo įrašą.

1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairėje naršymo srityje pasirinkite **Puslapiai**.
1. Raskite ir pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.
1. Komandų juostoje pasirinkite **Redaguoti**.
1. Puslapio struktūroje pasirinkite atkarpą **Pagrindinis**.
1. Atkarpoje **Pagrindinis** išplėskite visus nepastovius konteinerio modulius.
1. Suraskite ir pasirinkite vaizdo įrašų leistuvo modulį.
1. Dešiniojoje ypatybių srityje pasirinkite **vaizdo įrašo** ypatybę. Atsiranda išteklių parinkiklis.
1. Išteklių parinkiklyje pasirinkite galimą vaizdo įrašo išteklių arba pasirinkite **įkelti naują išteklių**, kad įkeltumėte naują vaizdo įrašo išteklių.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
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

[Patikrinti puslapio turinio pritaikymą neįgaliesiems](verify-accessibility.md)

[Sukurti dinaminius e-komercijos puslapius pagal URL parametrus](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
