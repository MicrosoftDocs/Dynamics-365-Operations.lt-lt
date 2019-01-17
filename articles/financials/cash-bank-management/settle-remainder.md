---
title: "Sudengti likutį"
description: "Galite sudengti iš sudengimo veiklos likusią sumą, taikydami ją DK sąskaitai."
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 075d0f5dc0c9dc4e46dc92a2da75da9f7a207472
ms.openlocfilehash: e67bd36adc92bffea48087d0322ab14e9c066a4e
ms.contentlocale: lt-lt
ms.lasthandoff: 12/06/2018

---

# <a name="settle-remainder"></a>Sudengti likutį

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

Galite sudengti iš sudengimo veiklos likusią sumą, taikydami ją DK sąskaitai arba kitam klientui. Galite sudengti likutį sudengdami į žurnalą įvestas sumas arba tik sudengdami atidarytas operacijas.

## <a name="setting-up-defaults"></a>Numatytųjų parametrų nustatymas 
Prieš naudodami funkciją Sudengti likutį, turite ją įgalinti ir nustatyti numatytuosius parametrus

1)  Spustelėkite **Gautinos sumos > Parametrai > Sudengimai** arba **Mokėtinos sumos > Parametrai > Sudengimai**
2)  Pasirinkite skirtuką **Sudengimas** ir spustelėkite **Įgalinti likučio sudengimą**
3)  Lauke **Numatytasis priežasties kodas** pasirinkite numatytąjį priežasties kodą. Priežasčių kodai turi būti jau nustatyti **Gautinos sumos >  Sąranka > Kliento nurašymo priežasčių kodai** arba **Mokėtinos sumos > Sąranka > Kliento nurašymo priežasčių kodai**. **Numatytoji likučio sudengimo sąskaita** bus numatytoji nurašymo priežasties kodui priskirta sąskaita.
3)  Atnaujinti **Numatytoji likučio sudengimo sąskaita**, jei reikia.
4)  Lauke **Numatytasis žurnalo pavadinimas** pasirinkite mokėjimų žurnalą, kurį naudosite norėdami sukurti mokėjimų žurnalą, kai tik sudengsite atidarytas operacijas. Jei įgalinsite likučio sudengimo funkciją, turėsite įtraukti numatytąjį žurnalo pavadinimą.

## <a name="settle-remainder-from-a-journal"></a>Sudengti likutį iš žurnalo
Jei neįgalinsite funkcijos **Sudengti likutį**, vis tiek galėsite įvesti operaciją žurnale, o tada sudengti operacijas pagal tai, kaip jau darėte anksčiau. Spustelėjus mygtuką **Gerai**, atviras sąskaitos faktūros balansas sumažinamas grynųjų pinigų suma. Jei grynieji pinigai nevisiškai sudengia sąskaitą faktūrą, ji paliekama atidaryta su likusia suma, kurią reikės sudengti vėliau.

Kai įgalinta funkcija **Sudengti likutį**, likusią sumą galite sudengti DK sąskaitoje. Taip pat galite perkelti likutį į kitą kliento sąskaitą (kliento operacijoms) arba kitam tiekėjui (tiekėjo operacijoms), užuot palikę atidarytas SF. 

Norėdami sudengti likutį iš puslapio **Sudengimas**, atlikite toliau nurodytus veiksmus.

1)  Puslapyje **Sudengimas** pažymėkite SF arba operacijas, kurias norite sudengti.
2)  Spustelėkite mygtuką **Sudengti likutį**.
3)  Bus rodomas dialogo langas, kuriame nurodoma su DK sąskaita sudengiama suma, likučiui sudengti naudojama data, parametrų numatytasis priežasties kodas ir parametrų numatytoji sąskaita. 
4)  Jei norite pakeisti numatytąją priežastį, pasirinkite naują sudengimo priežastį. Sudengimo sąskaita bus pakeista į su priežasties kodu susietą sąskaitą.
5)  Redaguokite sudengimo sąskaitą, jei norite ją pakeisti.
6)  Jei sudengiate kliento operacijas ir norite, kad likutis būtų perkeltas kitam klientui, tada pasirinkite klientą **Sudengti likutį su kliento sąskaita**. Jei sudengiate tiekėjo operacijas ir norite, kad likutis būtų perkeltas kitam tiekėjui, tada pasirinkite tiekėją **Sudengti likutį su tiekėjo sąskaita**.
6)  Spustelėkite **Sudengti likutį**.
7)  Bus rodomas puslapis **Žurnalas**. Į žurnalą bus įtraukta papildoma žurnalo eilutė su likučio sudengimo suma kaip suma ir su sudengimo likučio sąskaita kaip korespondentine sąskaita. Jei įtraukėte klientą arba tiekėją, kad galėtumėte perkelti sudengimo sumą kitam klientui arba tiekėjui, tada į žurnalą bus įtraukta papildoma eilutė, kad sudengimo suma būtų perkelta tam klientui arba tiekėjui.

Registruojant žurnalą, atidaryta operacija bus visiškai sudengta. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Sudengti likutį, kai tik sudengiate atidarytas operacijas
Taip pat galite sudengti likutį, kai sudengiate atidarytas operacijas be žurnalo.

Norėdami sudengti likutį, atlikite toliau nurodytus veiksmus.

1)  Puslapyje **Sudengimas** pažymėkite SF arba operacijas, kurias norite sudengti
2)  Spustelėkite **Sudengti likutį**
3)  Bus rodomas dialogo langas, kuriame nurodoma su DK sąskaita sudengiama suma, likučiui sudengti naudojama data, parametrų numatytasis priežasties kodas ir parametrų numatytoji sąskaita. 
4)  Jei norite pakeisti numatytąją priežastį, pasirinkite naują sudengimo priežastį. Sudengimo sąskaita bus pakeista į su priežasties kodu susietą sąskaitą.
5)  Redaguokite **sudengimo sąskaitą**, jei norite ją pakeisti.
6)  Jei sudengiate kliento operacijas ir norite, kad likutis būtų perkeltas kitam klientui, tada pasirinkite klientą **Sudengti likutį su kliento sąskaita**. Jei sudengiate tiekėjo operacijas ir norite, kad likutis būtų perkeltas kitam tiekėjui, tada pasirinkite tiekėją **Sudengti likutį su tiekėjo sąskaita**
7)  Taip pat galite pasirinkti sukurti mokėjimų žurnalą su sudengimo likučiu arba tiesiog jį registruoti be žurnalo. Funkcijai **Redaguoti žurnale** pasirinkite **Taip** mokėjimų žurnalui sukurti. Galėsite redaguoti kuriamą mokėjimų žurnalą.
8)  Spustelėkite **Sudengti likutį**. Pasirinkus sukurti žurnalą, mygtukas pasikeičia į **Kurti žurnalą**. Spustelėkite **Kurti žurnalą**.
9)  Jei sukūrėte mokėjimų žurnalą, jo puslapį atidarysite spustelėję **Sudengti likutį**. Į žurnalą bus įtraukta žurnalo eilutė su likučio sudengimo suma kaip suma ir su sudengimo likučio sąskaita kaip korespondentine sąskaita. Jei įtraukėte klientą arba tiekėją, kad galėtumėte perkelti sudengimo sumą kitam klientui arba tiekėjui, tada į žurnalą bus įtraukta papildoma eilutė, kad sudengimo suma būtų perkelta tam klientui arba tiekėjui.

