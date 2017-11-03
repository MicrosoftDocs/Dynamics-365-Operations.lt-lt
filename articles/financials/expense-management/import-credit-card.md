---
title: "Kredito kortelės operacijų importavimas ir tvarkymas"
description: "Šioje temoje paaiškinama, kaip importuoti ir tvarkyti su išlaidomis susijusias kredito kortelių operacijas. Šias operacijas galima nustatyti taip, kad jos būtų automatiškai importuojamos pasikartojančiu grafiku, arba jas galima pagal poreikį importuoti rankiniu būdu."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 3379e2f850653cb99231d4ab030b64beb72b626a
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Kredito kortelės operacijų importavimas ir tvarkymas

[!include[banner](../includes/banner.md)]

Su išlaidomis susijusias kredito kortelių operacijas galima nustatyti taip, kad jos būtų automatiškai importuojamos pasikartojančiu grafiku. Taip pat operacijas galima pagal poreikį importuoti rankiniu būdu. Kredito kortelių operacijos importuojamos naudojant duomenų objektą Kredito kortelių operacijos.

Norėdami gauti daugiau informacijos apie duomenų objektus, žr. [Duomenų objektai](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Importuoti kredito kortelės operacijas

1. Puslapyje **Kredito kortelių operacijos** pasirinkite **Importuoti operacijas**. Jei duomenų valdymo sritį atidarote pirmą kartą, kad galėtumėte tęsti, sistema turi atnaujinti duomenų objektų sąrašą.
2. Lauke **Pavadinimas** įveskite unikalų importavimo užduoties pavadinimą.
3. Lauke **Šaltinio duomenų formatas** pasirinkite failo, kuriame yra importuotinos kredito kortelių operacijos, formatą.
4. Pasirinkite **Nusiųsti**, tada raskite ir pasirinkite importuotiną failą.
5. Nusiuntę failą, pasirinkdami plytelės saitą **Peržiūrėti schemą**, patikrinkite kredito kortelių operacijų failo ir duomenų objekto Kredito kortelių operacijos stulpelių susiejimą. Jei yra susiejimo klaidų arba jei susiejimą turite keisti, tai darykite skirtukuose **Susiejimo vizualizacija** arba **Susiejimo informacija**.
6. Norėdami kredito kortelių operacijas automatizuoti, pasirinkite **Kurti pasikartojančią duomenų užduotį**. Tada galite nustatyti pasikartojimą, apibėžiantį, kaip dažnai kredito kortelių operacijas reikia importuoti. Baigę pasirinkite **Gerai**.
7. Norėdami dabar importuoti pasirinktą failą, pasirinkite **Importuoti**.
8. Jei importuojant įvyksta klaidų, galite peržiūrėti vykdymo žurnalą arba išdėstymo duomenis, kad matytumėte klaidas, kurias turite ištaisyti, kad padėtumėte užtikrinti sėkmingą importavimo procesą.

> [!NOTE]
> Jei turite importuoti daugiau nei vieną failo formatą, kiekvienam formato tipui turite sukurti atskiras importavimo užduotis.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Pakartotinis atleistų darbuotojų kredito kortelių operacijų priskyrimas

Nutraukus darbuotojo įrašą, darbuotojo „Active Directory“ domenų tarnybos (AD DS) paskyra išjungiama. Tačiau gali būti aktyvių kredito kortelių operacijų, kurias vis dar reikia įtraukti į išlaidas ir kurias reikia kompensuoti. Kai susietasis darbuotojas atleidžiamas, naudodami puslapį **Kredito kortelių operacijos** bet kuriai kredito kortelių operacijai galite iš naujo priskirti darbuotoją.

Pasirinkite vieną ar kelias kredito kortelių operacijas ir pasirinkite **Iš naujo priskirti operacijas**. Tada galite pasirinkti kitą darbuotoją, kuriam priskirsite kredito kortelių operacijas. Iš naujo priskyrus kredito kortelių operacijas, jas galima pasirinkti įtraukti į išlaidų ataskaitą ir apmokėti įprastu išlaidų ataskaitos kompensacijos procesu.

