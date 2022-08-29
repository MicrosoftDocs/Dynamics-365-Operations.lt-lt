---
title: Nustatyti ir naudoti išplėstinį registravimosi galimybę
description: Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti išplėstinės Microsoft Dynamics 365 Commerce point sale (EKA) programos registravimosi galimybę.
author: boycezhu
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.industry: Retail
ms.search.form: RetailFunctionalityProfile
ms.openlocfilehash: e2fc39b1b7fb34f49c061dcc324c28cf5a89277c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283701"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Nustatyti ir naudoti išplėstinį registravimosi galimybę

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti išplėstinės Microsoft Dynamics 365 Commerce point sale (EKA) programos registravimosi galimybę.

Debesies EKA (CPOS) ir "Modern POS" (MPOS) suteikia išplėstinį registravimosi galimybę, kuris leidžia parduotuvės darbuotojams prisijungti prie EKA programos nuskaitant brūkšninius kodus arba perbraukus kortele naudojant magnetinės juostelės skaitytuvą (MSR).

## <a name="set-up-extended-logon"></a>Nustatyti išplėstinį registrėjimą

Norėdami nustatyti išplėstinę EKA kasos aparatų registracijas parduotuvėse, atlikite šiuos veiksmus.

1. Programoje "Commerce Headquarters" eikite į " **Retail" ir "Commerce \> Channel" \> nustatymo EKA \> nustatymo EKA \> funkcijų šablonus**. 
2. Kairiajame naršymo lange pasirinkite funkcijų šabloną, susietą su parduotuve.
3. Skirtuke **Funkcijos** FastTab, dalyje Papildomos **registravimosi autentifikavimo** pasirinktys, atitinkamai nustatykite **šias pasirinktis kaip** **Taip** arba Ne:

    - **Registravimasis prie darbuotojų** brūkšninio **kodo** – nustatykite šią parinktį kaip Taip, jei norite, kad jūsų darbuotojai prisiregistruotų prie EKA nuskaitę brūkšninius kodus. 
    - **Darbuotojo brūkšninio kodo** registravimasis reikalauja slaptažodžio – **nustatykite** šią parinktį kaip Taip, jei norite, kad jūsų darbuotojai, prisiregistrudami prie EKA, perskaitytų brūkšninius kodus, turėtų įvesti slaptažodį.
    - **Darbuotojo kortelės** registravimasis – nustatykite šią **pasirinktį** kaip Taip, jei norite, kad jūsų darbuotojai prisiregistruotų prie EKA perbraukdami kortele.
    - **Darbuotojo kortelei** registruotis reikia slaptažodžio – **nustatykite** šią parinktį kaip Taip, jei norite, kad jūsų darbuotojai turėtų įvesti slaptažodį, kai prisiregistruos prie EKA, perbraukdami kortele.

Brūkšninis kodas arba kortelė susieta su kredencialais, kuriuos galima priskirti darbuotojui. Kredencialus turi turėti mažiausiai šeši simboliai. Eilutė, kurioje yra pirmieji penki simboliai, *turi būti unikali ir laikoma kredencialų ID*, kuris naudojamas ieškoti darbuotojo. Likę simboliai naudojami saugos tikrinimui. Pavyzdžiui, turite dvi korteles, kurių vienos kredencialai yra 12345DGYDEYTDW, o vienos kredencialai yra 12345EWUTBDAJH. Šių dviejų kortelių kredencialų ID 12345 yra toks pats, abiejų šių kortelių negalima priskirti darbuotojams.

## <a name="assign-extended-logon"></a>Priskirti išplėstinį registr vardą

Pagal numatytuosius parametrus tik vadovai gali darbuotojams priskirti išplėstinės registracijos funkciją. Norėdami priskirti išplėstinės registracijos funkciją, EKA pasirinkite **Išplėstinė registracija**. Tada ieškokite darbuotojo, ieškos lauke įvesdami darbuotojo operatoriaus ID. Pasirinkite darbuotoją ir spustelėkite **Priskirti**. Kitame puslapyje perbraukite arba nuskaitykite išplėstinę registraciją, kad priskirtumėte darbuotoją. Jei perbraukimas arba nuskaitymas sėkmingas, mygtukas **Gerai** tampa aktyvus. Spustelėkite **Gerai**, norėdami įrašyti to darbuotojo išplėstinę registraciją.

## <a name="delete-extended-logon"></a>Panaikinti išplėstinį registrėjimą

Norėdami panaikinti darbuotojui priskirtą išplėstinę registraciją, ieškokite darbuotojo naudodami operaciją **Išplėstinė registracija**. Pasirinkite darbuotoją ir spustelėkite **Atšaukti priskyrimą**. Pašalinami visi su tuo darbuotoju susieti išplėstinės registracijos kredencialai.

## <a name="use-extended-logon"></a>Naudoti išplėstinį registrėjimą

Sukonfigūravus išplėstą registravimąsi ir darbuotojui priskiriamas brūkšninis kodas arba magnetinė juostelė, kai rodomas EKA registravimosi puslapis, darbuotojas tiesiog turi perbraukti ar nuskaityti savo kortelę. Jei prieš tęsiant registrėjimąsi reikia slaptažodžio, darbuotojas raginamas įvesti savo slaptažodį.

## <a name="extend-extended-logon"></a>Išplėstinė prisijungimo informacija

Norint naudoti išplėstinę registravimosi galimybę, reikia, kad kredencialų ilgis būtų mažiausiai šeši simboliai ir kad pirmieji penki kredencialų ID būtų unikalūs. Iš pradžių jis buvo naudojamas kaip pavyzdys, kurį programuotojai gali pritaikyti, kad atitiktų konkretaus diegimo reikalavimus. (Pvz., jį galima pritaikyti, kad būtų galima palaikyti daugiau simbolių arba naudoti kitas saugos tikrinimo taisykles.) Išsamesnės informacijos apie tai, kaip kurti išplėstinio registravimosi plėtinius, [žr. išplėstinę MPOS ir Debesies EKA registravimosi funkcijų išplėtimą](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Registravimosi tarnybą taip pat galima išplėsti, kad būtų palaikomi papildomi išplėstiniai registravimosi įrenginiai, pvz., palmių skaitytuvai. Daugiau informacijos ieškokite [EKA extensibility dokumentacijoje](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
