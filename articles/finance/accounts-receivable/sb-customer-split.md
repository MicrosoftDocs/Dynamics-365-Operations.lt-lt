---
title: Kliento skaidymo pagal atsiskaitymo grafikus
description: Šiame straipsnyje aprašoma, kaip skaidyti klientą, kai naudojamas abonemento sąskaitų apmokėjimas.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746334"
---
# <a name="customer-split-on-billing-schedules"></a>Kliento skaidymo pagal atsiskaitymo grafikus

Atsiskaitymo grafike SF kodas *yra klientas*, kuris gauna pardavimo užsakymo SF, kad galėtų apmokėti sąskaitą. Kai kuriuose scenarijuose SF gali apmokėti daugiau nei vienas klientas. Klientų **skaidymo** funkcija leidžia įtraukti daugiau klientų, kurių sąskaitą galima išrašyti pagal tą patį sąskaitų pateikimo grafiką. Norėdami įjungti šią funkciją, eikite į **Abonemento atsiskaitymo \> pasikartojančios sutarties atsiskaitymo nustatymo \> pasikartojančios \>** sutarties atsiskaitymo parametrus ir nustatykite kliento **skaidymo** parinktį **taip**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Kliento išskaidyta atsiskaitymo grafiko antraštėje

Sukūrus atsiskaitymo grafiką, į atsiskaitymo grafiko antraštę galima įtraukti papildomų klientų.

Norėdami įtraukti klientą, atlikite šiuos veiksmus.

1. Skirtuke **Atsiskaitymo grafikas** pasirinkite Kliento skaidymo **parinktis**. Viršuje **esančiuose** kliento **sąskaitos ir kliento** sąskaitos pavadinimo laukuose nurodomas klientas, kuris priskirtas kaip atsiskaitymo **grafiko klientas**.

    > [!NOTE]
    > Kliento kodas, kurį pridedate, negali būti toks pat kaip mokėtojo kodas.

2. Kliento skaidymo **eilučių skirtuke** pasirinkite **Įtraukti eilutę**.
3. Pasirinkite klientą ir įveskite kiekvienos to kliento SF procentą.
4. Pagal numatytuosius nustatymus, atsiskaitymo grafiko pradžios ir pabaigos datos yra naudojamos kaip pradžios ir pabaigos datos. Įveskite skirtingas pradžios ir pabaigos datas, jei naujasis klientas moka nurodytą procentą tik tam tikrai atsiskaitymo grafiko dalisi. Pavyzdžiui, jei sąskaitų pateikimo grafiko pradžios data yra sausio 1 d., o pabaigos data – gruodžio 31 d., o naujam klientui išrašomos 40 procentų už pirmus devynis mėnesius, nurodykite sausio 1 d. kaip pradžios datą, o rugsėjo 30 d. – kaip pabaigos datą, **ir kaip procentą įveskite 40,00**.

Į kliento skaidymo eilutes galite įtraukti daugiau nei vieną klientą. Šiuo atveju bendra įvesta procentinė dalis neturi viršyti 100 procentų. Įveskite kliento nuorodą ir kliento paraišką kaip informacijos laukus, kurie bus rodomi pardavimo užsakymo eilutėje SF **generavimo proceso** metu.

Eilutės duomenys rodo pridėtų klientų kontaktinę informaciją, pristatymo adresą, kliento sąskaitos adresą ir mokėjimo informaciją. Ši informacija taip pat bus rodoma klientų pardavimo užsakyme.

Kai į atsiskaitymo grafiko antraštę įtraukiate kliento informaciją išskaidytą informaciją, jei atsiskaitymo grafike yra negautų mokėjimo grafiko eilučių, gausite tokį pranešimą, kuriame raginama atlikti keitimus: "Ar norite atlikti keitimus iš antraštės į eilutes? Pakeitimai tik atnaujins atsiskaitymo grafiko eilutes, kurių sąskaitos neišrašomos." Pasirinkite **Taip,** jei norite atnaujinti klientų išskaidytą informaciją sąskaitų pateikimo grafiko eilutėje. Pakeitimai nebus atnaujinti, jei sąskaitų pateikimo grafiko eilutei jau buvo išrašyta sąskaita.

Jei sąskaitų pateikimo grafikas sukuriamas naudojant kopijavimo grafiko **pasirinktį**, numatytoji informacija bus įvesta kliento skaidymo antraštės eilutėse. Tai negali būti tas pats kaip kliento kodas.

Kai SF **generavimo** procesas yra baigtas, bus sukurti keli pardavimo užsakymai. (Jei naudojamas automatinis registravimas, bus sukurtos ir kelios pardavimo SF.) Šiuos pardavimo užsakymus ir pardavimo **SF** **galima** peržiūrėti sf skirtuke SF, eilutės informacijos puslapio "FastTab **", kuriame pateikta išsami informacija apie** sąskaitas. **Atsiskaitymo** informacijos eilutėje rodomas kartotinis, nurodantis, kad sukurti keli pardavimo užsakymai ir pardavimo SF.

## <a name="customer-split-on-billing-schedule-lines"></a>Kliento skaidymo atsiskaitymo grafiko eilutėse

Kliento skaidymo galima įtraukti į atskiras sąskaitų pateikimo grafiko eilutes, jei norite išskaidyti tik konkrečias sąskaitų pateikimo grafiko eilutes. Eilutėje **pažymėkite žymės langelį** Kliento skaidinys, **tada** atnaujinkite arba įveskite kliento išskaidytą informaciją, meniu suskaidytas klientas.

Audito informacija atnaujinama, jei atsiskaitymo grafiko sąskaita jau pateikta, bet procentinė dalis buvo pakeista atsiskaitymo grafiko eilutėje. Visos eilutės, kurių sf iš naujo išrašytos po pakeitimo, naudos naująjį procentą.

> [!NOTE]
> - Kliento skaidymo parinkties negalima naudoti su laikomas produktais.
> - Jei pažymėtas **žymės langelis Neišrašyto** sąskaitos įplaukos, **kliento skaidymo** žymės langelio pažymėti negalima.
> - Jei naudojate tik **įplaukų išskaidymo** parinktį, pirminėje eilutėje yra **Kliento** skaidymo pasirinktis, bet nėra antrinių eilučių elementų.
