---
title: "Išplėstinio banko suderinimo apžvalga"
description: "Pažangaus banko derinimo funkcija suteikia galimybę importuoti elektroninius banko išrašus ir automatiškai juos suderinti su banko operacijomis programoje „Microsoft Dynamics 365 for Operations“.  Šiame straipsnyje paaiškinami derinimo nustatymo procesai."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3322f2edbe9f4eedce509de5a60c5ec8883db3a
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Išplėstinio banko suderinimo apžvalga

[!include[banner](../includes/banner.md)]


Pažangaus banko derinimo funkcija suteikia galimybę importuoti elektroninius banko išrašus ir automatiškai juos suderinti su banko operacijomis programoje „Microsoft Dynamics 365 for Operations“.  Šiame straipsnyje paaiškinami derinimo nustatymo procesai.  

Prieš naudojant išplėstinio banko derinimo funkciją, reikia nustatyti keletą elementų. Daugiau informacijos apie banko išrašo importavimo nustatymą žr. dalyje [Banko išrašo importavimo proceso nustatymas](set-up-advanced-bank-reconciliation-import-process.md).  Derinimo proceso nustatymo reikalavimai išdėstyti toliau.

## <a name="transaction-codes"></a>Operacijų kodai
Operacijų kodus galima naudoti kaip dalį banko išrašo derinimo gretinimo taisyklių.  Naudojant operacijų kodus galima sugretinti tik to pačio tipo operacijas tarp „Dynamics 365 for Operations“ ir banko išrašo.  Norėdami atlikti šio tipo gretinimą, pirmiausia turite nurodyti operacijų tipus, naudojamus „Dynamics 365 for Operations“ banko operacijoms vykdyti, tada turite tuos tipus sugretinti su jūsų banko naudojamais sudengimo operacijų kodais.  „Dynamics 365 for Operations“ banko operacijų tipai nurodyti puslapyje **Banko operacijų tipai**.  Šiame puslapyje taip pat galima nurodyti pagrindinę sąskaitą, kuri bus naudojama su operacijos tipu susijusiems elementams registruoti. 

Kai „Dynamics 365 for Operations“ banko operacijų tipai nurodyti, susiekite juos su operacijų kodais, naudojamais elektroniniuose banko išrašuose.  Susiejimo procesas vykdomas naudojant puslapį **Operacijos kodo susiejimas**.  Operacijos kodo susiejimas kiekvienoje banko sąskaitoje vykdomas atskirai.

## <a name="matching-rules-and-matching-rule-sets"></a>Gretinimo taisyklės ir gretinimo taisyklių rinkiniai
Naudojant gretinimo taisykles galima nustatyti automatinio „Dynamics 365 for Operations“ banko operacijų ir banko išrašo operacijų derinimo kriterijus.  Gretinimo taisyklės nustatomos puslapyje **Derinimo gretinimo taisyklės**.  Daugiau informacijos žr. dalyje [Banko derinimo gretinimo taisyklių nustatymas](set-up-bank-reconciliation-matching-rules.md). 

Gretinimo taisyklių rinkiniai naudojami siekiant nurodyti gretinimo taisyklių, kurios iš eilės vykdomos derinimo proceso metu, grupę.  Gretinimo taisyklių rinkiniai konfigūruojami puslapyje **Derinimo gretinimo taisyklių rinkiniai**.

## <a name="cash-and-bank-management-parameters"></a>Grynųjų pinigų ir banko valdymo parametrai
Puslapyje **Grynųjų pinigų ir banko valdymo parametrai** pateikiama daug parametrų, būdingų išplėstinio banko derinimo procesui.  Naudojant parinktį **Rodyti išrašo eilutės debeto / kredito sumą** galima pakeisti sumų rodinį puslapyje **Banko išrašas**.  Jei ši parinktis pažymėta, banko išrašo operacijos sumos bus rodomos atskiruose debeto ir kredito stulpeliuose.  Jei jos nepažymėsite, banko išrašo operacijos sumos bus rodomos viename sumų stulpelyje, naudojant atitinkamą ženklą. 

Parametrų puslapyje nustatytos tikrinimo parinktys perrašo gretinimo taisyklėse nustatytas parinktis.  Pavyzdžiui, negalite neautomatiniu arba automatiniu būdu derinti dokumentų, jei jų datų skirtumas didesnis, nei nurodyta parametrų puslapyje.  Be to, jei parinktis **Tvirtinti operacijos tipo susiejimą** yra pažymėta, „Dynamics 365 for Operations“ banko operacijų ir banko išrašo operacijų tipai turi būti susieti, kad operacijas būtų galima gretinti neautomatiniu arba automatiniu būdu. 

Taip pat turite sukonfigūruoti reikiamas numeracijas puslapyje **Grynųjų pinigų ir banko valdymo parametrai**.  Skirtuke **Numeracijos** nustatykite nuorodų **Atsiuntimo ID, Išrašo ID, Derinimo ID ir Banko derinimas** numeracijų kodus.

## <a name="bank-account-reconciliation-options"></a>Banko sąskaitos derinimo parinktys
Pirma turite įjungti banko sąskaitos išplėstinį banko derinimą.  Įjungus išplėstinio banko derinimo funkciją, puslapyje **Banko sąskaita** galima naudoti daug papildomų parinkčių. 

Parinktis **Naudoti bankų išrašus kaip elektroninių mokėjimų patvirtinimus** banko derinimo funkciją suderina su elektroninio mokėjimo būsenomis.  Kai ji įjungta, bus automatiškai sukurtas elektroninio mokėjimo, kurio būsena nustatyta kaip **Išsiųsta**, banko dokumentas.  Be to, elektroninio mokėjimo būsena bus atnaujinta iš **Išsiųsta** į **Gauta**, kai mokėjimas bus sugretintas, suderintas ir užregistruotas. 

Lauke **Banko sąskaitos pavadinimas išrašuose** nurodytas banko sąskaitos pavadinimas, naudojamas elektroniniuose banko išrašuose.  Šis pavadinimas naudojamas nustatant, kokias banko sąskaitos operacijas importuoti iš išrašo, kuriame gali būti pateikiama informacija apie kelias banko sąskaitas. 

Pasirinkus parinktį **Derinti importavus**, bus automatiškai patvirtintas banko išrašas, sukurtas naujas banko derinimas ir darbalapis bei įvykdytas numatytasis gretinimo taisyklių rinkinys.  Ši funkcija automatizuoja procesą iki pat to momento, kai operacijas reikia gretinti neautomatiniu būdu.  Importuojant banko sąskaitos parametras taps numatytuoju nustatymu.




