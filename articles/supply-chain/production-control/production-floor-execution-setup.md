---
title: Įrenginio, skirto paleisti gamybos cecho vykdymo sąsają, nustatymas
description: Gamybos cecho vykdymo sąsaja nustatoma kiekviename įrenginyje, esančiame gamybos ceche. Įmonės paprastai nustato kiekvieną įrenginį skirtingai, atsižvelgdamos į įrenginio paskirtį. Pavyzdžiui, įmonės priėmimo vietoje gali būti vienas įrenginys, kurį naudodami darbuotojai registruojasi atėję į darbą ir išeidami, o ceche – kitas įrenginys, kurį naudodami darbuotojai valdo savo užduotis.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 57f09bf907407e19ae0e693de64510f7f4efbf0b
ms.sourcegitcommit: f27f5d07c040bdca1bcd616f5d3f2320d3b3337e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/15/2020
ms.locfileid: "4433902"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Įrenginio, skirto paleisti gamybos cecho vykdymo sąsają, nustatymas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Gamybos cecho vykdymo sąsaja nustatoma kiekviename įrenginyje, esančiame gamybos ceche. Įmonės paprastai nustato kiekvieną įrenginį skirtingai, atsižvelgdamos į įrenginio paskirtį. Pavyzdžiui, įmonės priėmimo vietoje gali būti vienas įrenginys, kurį naudodami darbuotojai registruojasi atėję į darbą ir išeidami, o ceche – kitas įrenginys, kurį naudodami darbuotojai valdo savo užduotis.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Konkretaus įrenginio konfigūracijos ir filtrų nustatymas

Norėdami nustatyti įrenginio konfigūraciją ir užduočių filtrus, prisijunkite prie puslapio **Gamybos cecho vykdymas** naudodami abonementą, kuriame yra saugos vaidmuo, apimantis *prižiūrėtojo laiko priežiūros* pareigą. (Iš visų parengtų naudoti saugos vaidmenų šią pareigą turi tik *cecho prižiūrėtojas*.) Tada atlikite toliau pateiktus veiksmus.

1. Eikite į įrenginį, kurį norite nustatyti, ir prisijunkite prie „Microsoft Dynamics 365 Supply Chain Management” kaip cecho prižiūrėtojas. (Naudokite abonementą, kuriame yra *prižiūrėtojo laiko priežiūros* pareiga.)
1. Įsitikinkite, kad įrenginiui, kurį nustatote, konfigūracija yra galima. Jei nėra konfigūracijos, pateikiama numatytoji konfigūracija. Daugiau informacijos apie tai, kaip nustatyti konfigūraciją, žr. [Gamybos cecho vykdymo sąsajos konfigūravimas](production-floor-execution-configure.md).
1. Eikite į **Gamybos kontrolė \> Gamybos vykdymas \> Gamybos cecho vykdymas**.

    Jei gamybos cecho vykdymo sąsaja jau buvo sukonfigūruota bent vieną kartą dabartiniame įrenginyje, atsiranda prisijungimo puslapis. Kitu atveju atsiranda pasveikinimo puslapis.

1. Prisijungimo puslapyje arba pasveikinimo puslapyje pasirinkite **Konfigūruoti**.
1. Sąraše pasirinkite konigūraciją.
1. Pasirinkite **Toliau**.
1. Pasirinkite vieną ar kelis filtrus, kuriuos taikysite dabartiniame įrenginyje. Šie filtrai padės užtikrinti, kad įrenginyje būtų rodomos tik tinkamos užduotys. Norėdami nustatyti filtrą, pasirinkite filtro tipą, kad būtų atidarytas reikšmių sąrašas, o tada pasirinkite reikšmę, kurią norite filtruoti. Galimi toliau pateikti filtrai.

    - **Gamybos vienetas** – šis filtras yra aukščiausio lygio filtras. Paprastai jis nurodo didelę darbo vietą, kurioje yra kelios išteklių grupės ir atskiri ištekliai jose.
    - **Išteklių grupė** – šis filtras yra vidurinio lygio filtras. Paprastai jis nurodo susijusių išteklių rinkinį ribotoje darbo srities vietoje. Jei pirmiausia pasirenkate filtrą **Gamybos vienetas**, išteklių grupių sąraše rodomos tik to vieneto grupės. Kitu atveju jame rodomos visos galimos išteklių grupės.
    - **Ištekliai** – šis filtras yra konkrečiausias filtras. Paprastai jis nurodo konkretų įrenginį arba kitus pavienius išteklius. Jei pirmiausia pasirenkate filtrą **Išteklių grupė** ir (arba) **Gamybos vienetas**, išteklių sąraše rodomi tik tos grupės ar vieneto ištekliai. Kitu atveju jame rodomos visi galimi ištekliai.

1. Pasirinkite **Gerai**.
1. Atsiranda prisijungimo puslapis ir jūsų įrenginys parengtas naudoti.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Leisti darbuotojui keisti numatytuosius filtrus

Galite suteikti konkretiems darbuotojams teisę pakeisti filtrų nustatymus bet kokiame įrenginyje, kurį jie naudoja. Gamybos cecho vykdymo sąsaja darbuotojams, turintiems šią teisę, puslapiuose **Visos užduotys** ir **Aktyvi užduotis** pateikia mygtuką **Filtras**.

> [!NOTE]
> Jei darbuotojas keičia filtrą, naujas filtras taikomas nuo to momento visiems vartotojams, kurie prisijungia prie to įrenginio.

Norėdami leisti darbuotojui keisti numatytuosius užduočių filtrus, nustatytus įrenginyje, atlikite toliau pateiktus veiksmus.

1. Eikite į **Laikas ir buvimas darbe \> Nustatymas \> Laiko registracijos darbuotojai**.
1. Pasirinkite darbuotoją sąraše, kad būtų atidarytas to darbuotojo puslapis **Laiko registracijos darbuotojai**.
1. Skirtuke **Laiko registracija** nustatykite parinktį **Nustatyti filtrus** į *Taip*.

## <a name="run-the-interface-in-full-screen-mode"></a>Sąsajos vykdymas viso ekrano režimu

Dažnai vykdysite gamybos cecho vykdymo sąsają įrenginyje, kuris naudojamas tik šiam tikslui. Todėl gali būti naudinga vykdyti sąsają viso ekrano režimu, nerodant jokios naršymo juostos ir (arba) naršyklės.

- Norėdami paslėpti naršymo sritį, rodomą „Supply Chain Management”, pridėkite toliau nurodytą tekstą prie URL pabaigos naršyklės adreso juostoje: `\&limitednav=true`.
- Norėdami taip pat paslėpti naršyklės adreso juostą, naudokite naršyklės vietinį viso ekrano režimą. (Instrukcijas rasite jūsų naršyklės dokumentacijoje.)

Viršutinėje toliau pateiktos iliustracijos dalyje rodoma, kaip sąsaja atrodo pagal numatytuosius nustatymus. Apatinė dalis rodo, kaip ji atrodo viso ekrano režimu, kai naršymo sritis paslėpta.

![Standartinė ir viso ekrano sąsaja](media/pfei-full-screen.png "Standartinė ir viso ekrano sąsaja")

## <a name="extend-the-session-past-12-hours"></a>12 val. seanso pratęsimas

Pagal numatytuosius nustatymus gamybos cecho vykdymo sąsaja automatiškai atsijungia, jei ji nenaudojama 12 valandų. „Supply Chain Management” vartotojas tokiu atveju turi vėl prisijungti. Tačiau galite pratęsti skirtojo laiko ribą iki 90 dienų.

Norėdami pratęsti skirtojo laiko ribą, prisijunkite prie „Supply Chain Management” ir eikite į **Sistemos administravimas \> Vartotojai \> Seanso pratęsimas**. Nurodykite „Supply Chain Management” vartotojo abonementą, kuris naudojamas prisijungimui prie įrenginio, ir valandų, per kurias seansas turėtų išlikti aktyvus, skaičių.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]