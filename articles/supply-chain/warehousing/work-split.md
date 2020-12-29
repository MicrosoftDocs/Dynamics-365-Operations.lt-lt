---
title: Darbo skaidymas
description: Šiame temoje paaiškinama informacija apie darbo atskyrimo funkciją. Ši funkcija leidžia jums atskirti didelius darbo užsakymus į keletą mažesnių darbo užsakymų, kuriuos galite tuomet priskirti keliems sandėlio darbuotojų. Tokiu būdu tas pats darbas gali būti paimamas vienu metu kelių sandėlio darbuotojų.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4434067"
---
# <a name="work-split"></a>Darbo skaidymas

Darbo atskyrimo funkcija leidžia jums atskirti didelio darbo ID (tai reiškia, darbo užsakymus su keliomis linijomis) į keletą mažesnių darbo ID ir tuomet priskirti juos keliems sandėlio darbuotojams. Tokiu būdu tas pats darbas sukūrimo numeris gali būti paimamas vienu metu kelių sandėlio darbuotojų.

> [!IMPORTANT]
> Galite išskirti keletą darbo užsakymų, kurie turi būseną *Atviras* ar *Vykdomas*.

## <a name="turn-on-the-work-split-functionality"></a>Įjunkite darbo atskyrimo funkciją

Prieš tai, kai galėsite naudoti darbo atskyrimo funkciją, turite įjungti funkciją ir būtinųjų sąlygių funkcijų savo sistemoje. Administratoriai gali naudoti [funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nustatymus tam, kad patikrintų funkcijų būseną ir jas įjungtų kaip būtina.

Pirmiausia įjunkite būtinąsias sąlygas *Organizacijos sklaidos darbo blokavimo* funkciją, jei ji dar nėra įjungta. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Organizacijos sklaidos darbo blokavimas*

> [!NOTE]
> Įjungus šią funkciją, duomenų pagerinamas yra automatiškai taikomos įjungus funkciją visuose juridiniuose asmenyse.

Toliau, įjunkite *Darbo atskyrimo* funkciją, kuri yra įrašyta tolesne tvarka:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Darbo atskyrimas*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Darbo išsamios informacijos pagerinimas ir Visi darbo puslapiai

*Darbo atskyrimo* funkcija įtraukia tolesnius du mygtukus į **Darbo** skirtuką veiksmų juostoje **Darbo išsamioje informacijoje** ir **Visų darbų** puslapyse:

- **Atskyrimo darbas** – Atskirkite esamo darbo ID į keletą mažesnių darbų ID, kurie gali būti tvarkomi atskirų darbuotojų.
- **Atšaukite darbo atskyrimo seansą** – Atšaukite darbo atskyrimo seansą ir padarykite darbą prieinamą tvarkymui.

![Atskyrimo darbas ir Atšaukimo darbo atskyrimo seanso mygtukai](media/Work_split_buttons.png "Atskyrimo darbas ir Atšaukimo darbo atskyrimo seanso mygtukai")

> [!IMPORTANT]
> **Atskyrimo darbo** mygtukas nebus prieinamas, jei nebus patenkintos tolesnės sąlygos:
>
> - Darbo būsena yra kas kita, o ne *Atvira* ar *Vykdoma*.
> - Talpyklos ID yra susietas su darbo ID. (Talpykla negali būti sistemiškai atskiriama, nes jai reikia fizinių veiksmų.)
> - Darbas yra susietas su klasteriu.
> - Darbo užsakymo tipas yra kas kita, o ne vienas iš tolesnių tipų:
>
>    - Pardavimo užsakymai
>    - Žaliavų paėmimas
>    - Perkėlimo išdavimas
>
> - Darbą šiuo metu atskiria kitas vartotojas. Jei bandote atverti atskyrimo langą darbui, kurį jau atskiria kitas vartotojas, gausite šį klaidos pranešimą: „Darbas su ID \#\#\#\# šiuo metu atskiriamas. Bandykite po kelių minučių. Jei ir toliau gaunate šį pranešimą, susisiekite su vadovu."

Nauja darbo blokavimo priežastis, *Atskirti darbą*, rodomas, kai darbo ID yra atskyrimo procese. Jis rodomas tiek **Atskirti darbą** puslapyje ir sandėlio programoje, jei vartotojas bando vykdyti darbą. Kai blokavimo priežastys yra naudojamos, **Blokuota bangos** laukelio pavadinimas iš darbo ID yra pakeistas į **Blokuotas**.

## <a name="initiate-a-work-split"></a>Pradėkite darbo atskyrimą

Funkcija įtraukia naują **Atskyrimo darbo** puslapį, kuris leidžia vartotojams atskirti darbų linijas nuo darbo ID. Kai puslapis pirmą kartą atveriamas, jis rodo eilutes, kurios turi darbo būseną *Atvira* ir jei jos parengtos atskyrimui. Veiksmų juostoje pasirinkite **Atskirti darbą** tam, kad apdorotumėte pasirinktą darbą.

Norėdami atskirti darbą atlikite šiuos žingsnius.

1. Atverkite vieną iš tolesnių darbo langų:

    - **Darbo išsami informacija** (**Sandėlio valdymas \> Darbas \> Išsami darbo informacija**)
    - **Visi darbai** (**Sandėlio valdymas \> Darbas \> Visi darbai**)

1. Tinklelyje pasirinkite darbo ID atskyrimui. **Darbo užsakymo tipas** laukelis turi būti nustatytas viena iš tolesnių verčių:

    - Pardavimo užsakymai
    - Žaliavų paėmimas
    - Perkėlimo išdavimas

1. Veiksmų juostoje pasirinkite **Darbo** skirtuką **Darbo** grupėje, pasirinkite **Atskirti darbą**.

    **Atskirti darbą** puslapis pasirodo ir rodo darbo eilutes, kurios yra atvertos ir gali būti atskirtos. Pagal nutylėjimą, tik prieinamos darbo eilutės yra rodomos. Norėdami peržiūrėti visas eilutes darbo ID (pavyzdžiui, eilutes, kurių darbo tipas yra *Padėti*), pasirinkite **Rodyti visas eilutes** žymimą laukelį virš tinklelio.

    Rodomas tolesnis pranešimas:„Vartotojai negali apdoroti darbo eilučių, kol nepabaigėte atskyrimo ir neuždarėte šio puslapio."

    **Darbo blokavimo priežastis** laukelis esamam darbui bus nustatytas į *Atskirti darbą* ir darbas bus užblokuotas.

    ![Blokavimo priežastis](media/Blocking_reason.png "Blokavimo priežastis")

1. Pasirinkite eilutes, kad pašalintumėte iš esamo darbo ID ir įtrauktumėte naują darbo ID. Atistinka šis įvykis:

    - Jums atskyrus darbą, pasirinkta eilutė ar eilutės iš originalaus darbo ID yra atšaukiamos ir tuomet nukopijuojamos į naują darbo ID.
    - Esanti darbo šablono struktūra ir padėjimo vieta (taip pat ateities padėjimo/paėmimo poros) yra užrezervuojamos iš anksto. Tolesnio darbo ID laukelių vertės yra nukopijuojamos iš originalaus darbo į naują:

        - Krovinio ID
        - Siuntos ID
        - Darbo užsakymo tipas
        - Užsakymo numeris
        - Vieta
        - Sandėlis
        - Darbo prioritetas
        - Darbo telkinio ID
        - Bangos ID
        - Darbo sukūrimo numeris

    - Tolesni laukeliai nenukopijuojami į naują darbo ID:

        - **Darbo ID** – Naujas darbo ID yra sukuriamas pagal atitinkamą skaičių seką.
        - **Darbo būsena** – Šis laukelis nustatytas į *Atviras*.
        - **Užrakino** – Šis laukelis pagal nutylėjimą nustatytas tuščias.
        - **Tikslinės licencijos lentelės ID** – Šis laukelis paliekamas tuščias.
        - **Sukūrimo data ir valanda** – Šis laukelis nustatytas esamai datai ir laikui rodyti.
        - **Užblokuota/užšaldyta banga** – Šis laukelis yra iš naujo suprojektuojamas originaliam darbo ID ir naujam darbo ID.

1. Veiksmų juosoje rinkitės **Atskirti darbą**.

Darbo atskyrimo metu, rodomas tolesnis pranešimas: „Apdorojimo operacija - Atskirti darbą“. Kai šis pranešimas matomas, galite atšaukti operaciją pasirinkę **Atšaukti** pranešimo laukelyje.

Jei **Rodyti visas eilutes** žymimas laukelis yra atžymimas, atskirta ir atšaukta eilutės nebebus rodoma tinklelyje. Jei žymimas laukelis yra pasirinktas, turėtumėte matyti **Darbo būsenos** laukelio vertę tai eilutei, kuri buvo pakeista į *Atšaukta*.

Tolesnis pranešimas yra rodomas siekiant parodyti, kad naujas darbo ID buvo sukurtas: „Darbas \#\#\#\# buvo sukurtas atskiriant nuo originalaus darbo \#\#\#\#."

Kitos darbo eilutės nuo originalaus darbo ID (toks kaip *Padėti* eilutės) buvo pataisytos kaip būtina tam, kad atsipindėtų atšauktas darbo eilutes. Pavyzdžiui, jei originalaus darbo ID *Padėti* eilutė 15 kiekiui ir *Paėmimo* eilutės, kurių bendras kiekis yra 10 buvo atšauktos, naujas *Padėjimo* kiekis originalaus darbo ID dabar bus 5.

Naujas darbas nebus nedelsiant priskirtas bet kuriam vartotojui. Nepaisant to, galite priskirti jį dabar vartotojui kaip reikia naudodami standartinę funkciją **Darbo išsamios informacijos** puslapyje.

> [!IMPORTANT]
> Galite atskirti tik darbo ID, kurie turi du ar daugiau esamų darbo eilučių. Jei pasirenkate **Atskirti darbą** kai yra tik viena darbo eilutė, gausite tolesnį klaidos pranešimą: „Mažiausiai viena darbo eilutė turi likti pradiniame darbe." Tokiu atveju, atskyrimas neįvyks.

## <a name="finish-a-work-split"></a>Pabaikite darbo atskyrimą

Norėdami pabaigti darbo atskyrimą, *Atskirti darbą* blokavimo priežastis turi būti pašalinta. Yra du būdai atlikti šį žingsnį:

- Darbą atskiriantis darbuotojas užveria **Atskirti darbą** puslapį pasirinkdamas **Užverti** mygtuką (**X**) viršutiniame dešiniame kampe. Uždarius puslapį, *Atskirti darbą* blokavimo priežastis bus panaikinta. *Blokavimo* būsena šiam darbui bus parengta iš naujo ir jei nebėra daugiau blokavimo priežasčių jam. darbas bus atblokuotas.
- Bet kuri vartotojas atidaro darbo ID ir pasirenka **Atšaukti darbo atskyrimo seansą** mygtuką veiksmų juostoje. Taigi *Atskirti darbą* vlokavimo priežastis bus panaikinta ir *Blokavimo* būsena šiam darbui bus parengta iš naujo, kai tik **Atskirti darbą** langas bus užvertas.

Po to, kai *Atskirti darbą* blokavimo priežastis yra panaikinta, darbas gali vykti mobiliame įrenginyje su sąlyga, kad **Blokuotas** būsena yra nustatyta į *Ne* darbo ID.

## <a name="user-blocking-on-the-warehouse-app"></a>Vartotojo blokavimas sandėlio programoje

Jei bandote naudoti sandėlio programą, kad vykdytumėte paėmimo darbą pagal atskiriamą darbo ID, gausite tolesnį klaidos pranešimą: „Darbas su ID  \#\#\#\# šiuo metu atskiriamas." Jei gaunate šį pranešimą, pasirinkite **Atšaukti**. Tuomet galite tęsti šio darbo apdorojimą.

## <a name="other-blocked-operations"></a>Kitos užblokuotos operacijos

Bet kurios operacijos, kurios keičia darbo eilutes, darbo inventoriaus perdavimus ar papildymo nuoradas, kurios susijusios su atskiriamu darbu neveiks ir bus rodomas tolesnis klaidos pranešimas : „Darbas su ID \#\#\#\# šiuo metu yra atskiriamas."
