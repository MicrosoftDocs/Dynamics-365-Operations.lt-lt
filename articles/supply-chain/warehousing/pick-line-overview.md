---
title: Mobiliojo įrenginio meniu elemento nustatymas paėmimo eilučių peržiūrai pateikti
description: Šioje temoje paaiškinama, kaip nustatyti, kada visų darbo eilučių sąrašas bus rodomas sandėlio darbuotojams, kurie apdoroja sandėlio darbus mobiliajame įrenginyje. Ši funkcija gali būti naudinga sandėlio darbuotojams, kuriems dažnai reikia peržiūrėti paėmimo eilutes darbo užsakyme, kad jie galėtų optimizuoti savo paėmimų seką.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 433ed2152c47dbe698a640b099cb34727fe63452
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989698"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Mobiliojo įrenginio meniu elemento nustatymas paėmimo eilučių peržiūrai pateikti

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti pasirinktis, susijusias su mobiliųjų įrenginių meniu elementų, kurie naudojami išrinkimo darbui apdoroti, paėmimo eilutės peržiūra. Paėmimo eilutės peržiūra leidžia sandėlio darbuotojams peržiūrėti ir pasirinkti iš visų darbo eilučių, susijusių su jų dabartine užduotimi, sąrašo. Ši funkcija gali padėti darbuotojams optimizuoti savo paėmimų seką. Funkcija suteikia pasirinktis, kurios pakeičia standartinį **Praleidimo** mygtuką, kuris leidžia darbuotojams pereiti per eilutes po vieną pagal pastovią eilučių tvarką. (Tačiau vis tiek galima naudoti šį mygtuką.)

Administratoriai gali konfigūruoti kiekvieną meniu elementą atskirai, kad galėtų kontroliuoti, kaip, kada ir kur sandėlio programa pateikia paėmimo eilučių peržiūrą.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Darbo paėmimo eilutės apžvalgos funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** _sandėlio valdymas_
- **Funkcijos pavadinimas:** _Darbo paėmimo funkcijos apžvalga_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Meniu elementų konfigūravimas visų darbo eilučių sąrašui parodyti

Norėdami nustatyti mobiliojo įrenginio meniu elementą paėmimo eilučių peržiūrai pateikti, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite arba sukurkite meniu elementą, susijusį su paėmimo darbu ir nustatykite šias reikšmes:

    - **Režimas:** *Darbas*
    - **Naudoti esamą darbą:** *Taip*
    - **Nurodytas:** *Vartotojo nurodyta* arba *Sistemos nurodyta*

    Norėdami gauti daugiau informacijos apie tai, kaip kurti meniu elementus ir naudoti įvairius parametrus, galimus **Mobiliojo įrenginio meniu elementų** puslapyje, žr. [Mobiliųjų įrenginių nustatymas sandėlio darbui](configure-mobile-devices-warehouse.md).

1. „FastTab” skirtuke **Bendra** konfigūruokite šią funkciją nustatydami lauką **Rodyti darbo eilučių sąrašą** į vieną iš šių reikšmių:

    - **Rodyti tik pateikus užklausą** – darbuotojai gali pasirinkti peržiūrėti paėmimo eilučių naudodami mygtuką **Praleisti iki** sandėlio programoje.
    - **Rodyti kiekvieno paėmimo pradžioje** – darbuotojai mato sąrašą kiekvieną kartą, kai jie pradeda arba baigia paėmimo eilutę. Jie taip pat gali peržiūrėti sąrašą dar kartą pasirinkdami mygtuką **Praleisti iki** sandėlio programoje.
    - **Rodyti tik pirmo paėmimo pradžioje** – darbuotojai mato sąrašą kiekvieną kartą pradėdami naują paėmimo darbą, tačiau ne po kiekvienos eilutės. Jie taip pat gali peržiūrėti sąrašą dar kartą pasirinkdami mygtuką **Praleisti iki** sandėlio programoje.
    - **Niekada nerodyti** – įprastas **Praleisti** mygtukas atsiranda sandėlio programoje, o darbo eilučių sąrašo rodymas išjungiamas. Mygtukas **Praleisti** leidžia darbuotojui pereiti per eilutes po vieną pagal pastovią eilučių tvarką. Jie taip pat gali pereiti per sąrašą tiek kartų, kiek reikia, kol visos eilutės bus apdorotos.

1. Veiksmų srityje pasirinkite **Įrašyti**.

    Jei nustatote lauką **Rodyti darbo eilučių sąrašą** kaip bet kokią reikšmę, išskyrus *Niekada nerodyti*, mygtukas **Laukų sąrašas** tampa pasiekiamas veiksmų srityje.

1. Veiksmų srityje pasirinkite **Laukų sąrašas**.
1. Puslapyje **Laukų sąrašas** konfigūruokite informaciją, kurią kiekvienai sąrašo eilutei nurodo sandėlio programa.

    - Laukas **Pagrindinis valdiklis** visada nustatomas į *LineNum*. Todėl kiekviena eilutė sąraše prasideda eilutės numeriu.
    - Naudokite likusius **Rodymo lauko** laukus, norėdami pridėti ne daugiau septynių jums reikalingų papildomų rodymo laukų. Kiekviename lauke **Rodymo laukas** pasirinkite darbo eilutės lauko pavadinimą. Tada kiekvienoje eilutėje bus rodoma to lauko reikšmė. Reikšmės bus rodomos tokia tvarka, kurią pasirenkate čia. Galite palikti kai kuriuos **Rodymo lauko** laukus tuščius, jeigu jums nėra reikalingos visos septynios reikšmės.

1. Veiksmų srityje pasirinkite **Įrašyti** ir uždarykite **Laukų sąrašo** puslapį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]