---
title: "Išplėstinio banko suderinimo apžvalga"
description: "Išplėstinė banko sąskaitų derinimo leidžia jums importuoti elektroninio banko ataskaitas ir automatiškai suderinti su banko operacijų Microsoft Dynamics 365 operacijoms.  Šiame straipsnyje paaiškinami derinimo nustatymo procesai."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Išplėstinio banko suderinimo apžvalga

Išplėstinė banko sąskaitų derinimo leidžia jums importuoti elektroninio banko ataskaitas ir automatiškai suderinti su banko operacijų Microsoft Dynamics 365 operacijoms.  Šiame straipsnyje paaiškinami derinimo nustatymo procesai.  

Yra keletas vienetų, kuris turi būti nustatytas prieš naudodami funkciją Išplėstinė banko susitaikymo. Daugiau informacijos apie nustatymą banko pareiškimą importo, rasite [nustatyti banko pareiškimą importo procesas](set-up-advanced-bank-reconciliation-import-process.md).  Nustatyti susitaikymo proceso reikalavimai yra išsamiau išdėstyti toliau.

## <a name="transaction-codes"></a>Operacijų kodai
Operacijų kodai gali būti naudojamas kaip dalis banko derinimo atitikimo taisyklės.  Operacijų kodai padės suderinti tik tų pačių tipų sandorius tarp Dynamics 365 operacijas ir banko išrašą.  Kad tai tokio tipo atitiktį, jums pirmiausia nustatyti tipai, naudojami banko operacijų Dynamics 365 operacijoms, tada žemėlapis tiems tipams, į ataskaitą operacijų kodus, kuriuos naudoja jūsų banko.  Operacijų tipus dinamika 365 operacijas banko operacijų yra nustatytos į **banko operacijos tipas** puslapis.  Tai taip pat, kur nurodyti pagrindinę sąskaitą naudoti darbai, susiję su šios operacijos tipą. 

Nustačius jūsų Dynamics 365 operacijas bankas operacijų kodus, jūs tada žemėlapį į operaciją kodai, naudoti elektroninius banko išrašus.  Šis planavimo procesas yra atliekamas naudojant į **operacijos kodas kartografavimo** puslapis.  Operacijos kodas prieskyra baigta atskirai kiekvienos banko sąskaitos.

## <a name="matching-rules-and-matching-rule-sets"></a>Gretinimo taisyklės ir gretinimo taisyklių rinkiniai
Atitikimo taisyklės leidžia jums nustatyti kriterijus, automatinė derinimo Dynamics 365 operacijas banko operacijas ir banko išrašo operacijas.  Nustatyti atitikimo taisyklių būtų daroma **susitaikymo atitikimo taisyklės** puslapis.  Daugiau informacijos rasite [nustatyti banko terminų atitikimo taisyklės](set-up-bank-reconciliation-matching-rules.md). 

Apibrėžti grupės atitikimo taisyklių, kurios vykdomos iš eilės banko susitaikymo proceso metu naudojamos atitikimo taisyklių rinkinių.  Konfigūruojami atitikimo taisyklių rinkinių, **atitikimo taisyklių rinkinių derinimo** puslapis.

## <a name="cash-and-bank-management-parameters"></a>Grynųjų pinigų ir banko valdymo parametrai
Yra daug parametrų, būdingų pažangių banko susitaikymo procesą į **pinigų ir banko valdymo parametrai** puslapis.  Į **Rodyti ataskaitos eilutės suma, debeto/kredito** pasikeičia sumos atsižvelgiant į **banko pareiškimą** puslapis.  Jei ši parinktis pažymėta, banko pareiškimas sandorio sumos bus rodomas atskiras debeto ir kredito stulpeliuose.  Jei nepažymėsite, banko pareiškimas sandorio sumos bus rodomos vieną sumą stulpelyje su atitinkamu ženklu. 

Parametrų puslapyje pateiktų tikrinimo galimybių nepaisyti pasirinkimus dėl atitikimo taisyklės.  Pavyzdžiui, negalite rankiniu būdu arba automatiškai suderinti dokumentai už dieną skirtumui nustatyti parametrų puslapyje.  Taip pat, jei galimybė **patvirtinti sandorio tipo žemėlapių** yra pažymėtas, operacijų tipai turi susieti Dynamics 365 operacijas banko operacijos ir banko išrašo operacijos tam, kad sandoriai turi būti rankiniu būdu arba automatiškai. 

Taip pat turite sukonfigūruoti reikia numeracijas, **pinigų ir banko valdymo parametrai** puslapis.  Dėl to **skaičių sekas** skirtuke, nustatyti numeracijos kodus atsisiuntimo **ID, išrašo ID, derinti ID ir banko susitaikymo** nuorodos.

## <a name="bank-account-reconciliation-options"></a>Banko sąskaitos derinimo parinktys
Pirma turite įgalinti pažangiosios banko sąskaitų derinimo banko sąskaitos.  Nemažai papildomos parinktys galimos su **banko sąskaitos** psl. Kai pažangiosios banko susitaikymo funkcija yra įjungta. 

**Naudoti banko ataskaitas kaip patvirtinti elektroninio mokėjimo** funkcija sujungia funkciją banko susitaikymo su elektroninio mokėjimo būsenos.  Kai tai yra įjungtas, banko dokumentas bus automatiškai sukurta dėl elektroninio mokėjimo būsena bus nustatyta kaip **išsiųsta**.  Be to, elektroninių mokėjimo statusas bus atnaujintas nuo **išsiųsta** į **priimti** po to, kai mokėjimas yra suderinta, susitaikė, o paskelbtas. 

Į **banko sąskaitos pavadinimas atskaitomybėje** lauke yra vardas, naudojamas banko sąskaitos savo elektroninius banko išrašus.  Šis pavadinimas yra naudojamas nustatant, kokių sandorių importuoti banko sąskaitos ataskaitos, kuri gali būti pateikiama informacija apie kelių banko sąskaitų. 

Galimybė **derinti po importo** bus automatiškai patvirtinti banko išrašą, sukurti naują banko sąskaitų derinimo ir darbalapio ir paleiskite numatytuosius atitinkamus taisyklių rinkinį.  Šią funkciją automatizuoja procesą iki pat operacijos, kurios turi būti vykdoma rankiniu būdu.  Banko sąskaitos parametras bus numatytoji importuojant.


