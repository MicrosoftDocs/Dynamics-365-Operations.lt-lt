---
title: "Išteklių galimybės"
description: "Šiame straipsnyje pateikiama informacija apie išteklių pajėgumus. Pajėgumas yra operacijų ištekliaus gebėjimas atlikti tam tikrą veiklą. Šiame straipsnyje paaiškinama, kaip naudojami pajėgumai ir susijusios koncepcijos, pvz., įgudimo lygis ir prioritetas, siekiant pasirinkti tinkamus veiklos išteklius."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4463ca8e11115eb83323716faa4ed6b38937a3e4
ms.lasthandoff: 03/31/2017


---

# <a name="resource-capabilities"></a>Išteklių galimybės

Šiame straipsnyje pateikiama informacija apie išteklių pajėgumus. Pajėgumas yra operacijų ištekliaus gebėjimas atlikti tam tikrą veiklą. Šiame straipsnyje paaiškinama, kaip naudojami pajėgumai ir susijusios koncepcijos, pvz., įgudimo lygis ir prioritetas, siekiant pasirinkti tinkamus veiklos išteklius.

Pajėgumas yra operacijų ištekliaus gebėjimas atlikti tam tikrą veiklą. Operacijų ištekliui galima priskirti daugiau nei vieną pajėgumą, o pajėgumą galima priskirti daugiau nei vienam ištekliui. Ištekliams pajėgumus galite laikinai priskirti nurodydami pajėgumo priskyrimo pradžios ir pabaigos datas. Pasibaigus ištekliaus pajėgumui, negalima suplanuoti projekto arba gamybos, kuriai tas pajėgumas yra reikalingas, ištekliaus. Pasibaigusį pajėgumą galima atnaujinti. Pajėgumus galite naikinti, jei jie nėra aktyvaus gamybos užsakymo maršruto ryšio arba gamybos maršruto dalis. Apskritai, būkite atsargūs naikindami pajėgumus. Geriau pabandykite koreguoti išteklių, kuriems pajėgumas priskirtas, galiojimo datą. Pajėgumus galima priskirti visų tipų ištekliams: įrankiui, tiekėjui, mašinai, vietai, priemonei arba personalui.

## <a name="level"></a>Lygis
Daugelio išteklių funkciniai pajėgumai dažnai būna tie patys, bet įgudimo (pvz., stiprumo, apdorojimo greičio arba tikslumo) lygiai skiriasi. Todėl priskirdami pajėgumą ištekliui, lauke **Lygis** galite nurodyti reikšmę. Lygis yra paprasta skaitinė reikšmė. Jei nurodote, kad pajėgumas yra ištekliaus gamybos maršruto reikalavimas, taip pat galite nurodyti to pajėgumo lauko **Minimalus reikalingas lygis** reikšmę. Tada planavimo mechanizmas parenka tik išteklius su reikiamais pajėgumais, kurių lygis atitinka arba viršija šaltinio reikalavime nurodytą minimalų lygį.

## <a name="priority"></a>Pirmenybė
Operacijų ištekliams su tais pačiais pajėgumais galima priskirti prioritetą. Tada, jei daug išteklių pajėgumų planavimo reikalavimus, reikiamo lygio ir laisvų pajėgumų, planavimo modulis pasirinkti tarp šių išteklių. Jei **prioritetas** pažymėtas, **pirminių išteklių atrankos** lauko į **planavimo parametrų** p., šaltinį, kuris turi aukščiausią prioritetą (mažiausia skaitinė vertė, **prioritetas** lauko) pažymėtas pirmasis planavimo metu.

## <a name="resource-requirements"></a>Išteklių reikalavimai
Kai nustatote gamybos maršruto išteklių reikalavimus, vieną arba daugiau pajėgumų galite nurodyti kaip reikalavimus. Planuojant gamybą, maršruto operacijos išteklių reikalavimuose nustatyti pajėgumai yra suderinami su nustatytais išteklių pajėgumais. Pasirenkami ištekliai, kurių pajėgumai atitinka reikalavimus. Jei kelių išteklių funkcinis pajėgumas yra toks pats, bet skiriasi jo įgudimas (pvz., stiprumas, apdorojimo greitis arba tikslumas), galite nustatyti kelis pajėgumus arba naudoti pajėgumo lygį ištekliaus pajėgumo tinkamumui nustatyti. Toliau pateikiamas pavyzdys.

-   Maršrute gręžimo proceso laikas nustatomas kaip 10 vienetų per valandą, bet pats reikalavimas nurodomas kaip Gręžimas.
-   Jūs turite dvi gręžimo mašinas – M1 ir M2.
-   Gręžimo pajėgumas priskiriamas abiem ištekliams, mašinai M1 ir mašinai M2.
-   Mašina M1 gali gręžti du vienetus per valandą, o mašina M2 gręžti 11 vienetų per valandą.

Šiame pavyzdyje planavimo mechanizmas gali parinkti abi mašinas, nes jos abi atitinka pagrindinį pajėgumų reikalavimą (gręžimo). Tačiau mašina M1 gali gręžti tik du vienetus per valandą. Kadangi šis koeficientas yra daug mažesnis nei maršrute nurodytas 10 vienetų per valandą koeficientas, pasirinkus mašiną M1 gali kilti gamybos problemų. Toliau pateikiame du būdus, kuriais galima išspręsti šią problemą ir užtikrinti, kad būtų pasirinkta mašina M2.

-   Sukurkite du atskirus pajėgumus: mažos spartos gręžimo ir didelės spartos gręžimo. Nustatykite mažos spartos gręžimą kaip gręžimą, kurio apdorojimo laikas yra nuo vieno iki devynių vienetų per valandą. Nustatykite didelės spartos gręžimą kaip gręžimą, kurio gręžimo proceso laikas yra nuo 10 iki 19 vienetų per valandą. Tada priskirkite M1 mašina mažos spartos gręžimo funkcija ir priskirti M2 mašinos didelės spartos gręžimo funkcija. Galiausiai, pakeisti išteklių pajėgumo reikalavimas maršrutu greitųjų gręžimo. Tada planavimo mechanizmas parinks tinkamą mašiną (M2).
-   Naudokite pajėgumų lygį, norėdami nustatyti gręžimo mašinoms priskirto gręžimo pajėgumo tinkamumą. Nurodyti, kad M1 mašina yra gręžimo funkcija lygiu 2.0 ir kad M2 mašina yra gręžimo funkcija 11,0 lygyje. Nurodykite, kad 10,0 yra minimalus lygis, kuris yra būtinas gręžimo galimybės reikalavimas maršrutu. Tada planavimo mechanizmas nustatys, kad tik mašina M2 atitinka išteklių reikalavimus.

## <a name="competencies-for-human-resources"></a>Personalo kompetencijos
Jei turite tipo **Personalas** operacijų išteklių, susijusių su personalo darbuotojais, nustatydami gamybos maršruto išteklių reikalavimus taip pat galite pasinaudoti darbuotojų kompetencijomis. Kitaip tariant, taip pat galite nurodyti tam tikrų įgūdžių, kursų, sertifikatų arba pareigų reikalavimus. Tada planavimo mechanizmas galės parinkti su darbuotojais susietus išteklius pagal tų darbuotojų kompetencijas. Kompetencijos yra nustatomos srityje Personalas, o ne puslapyje **Išteklių pajėgumai**. Kai nustatote įgūdžius, kursai, sertifikatai arba pavadinimai kaip išteklių poreikius, turite naudoti funkciją žmogiškųjų išteklių ir susieti kiekvieno ištekliaus, kad **žmogiškųjų išteklių** tipo atitinkami darbuotojai. Jei nenaudojate žmogiškųjų išteklių funkcijas, jūs gali apibrėžti galimybes, **išteklių pajėgumus** puslapį, kuris primena arba dubliuoti kompetencija nuo žmogiškiesiems ištekliams. Tačiau puslapyje **Išteklių pajėgumai** nėra funkcijos, būtinos norint išlaikyti įgūdžius, kursus, sertifikatus arba pareigas.


