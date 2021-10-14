---
title: Grąžinimų valdymo registravimo sąranka
description: Šioje temoja aprašoma, kaip nustatyti registravimo šablonus. Registravimo šablonai yra naudojami nustatyti grąžinimo valdymo skaičiavimo eilučių įrašų registravimui.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: edffccfec552d90ce704190b4be0b4594964fa81
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574334"
---
# <a name="rebate-management-posting-setup"></a>Grąžinimų valdymo registravimo sąranka

[!include [banner](../includes/banner.md)]

Grąžinimų valdymo registravimo šablonai yra naudojami nustatyti grąžinimo valdymo skaičiavimo eilučių įrašų registravimui. Kai sandorio antraštėje pasirenkamas registravimo šablonas, jis pritaikomas visoms sandorio eilutėms.

Ši funkcija veikia tarp įmonių (juridinių subjektų). Galite nurodyti įmonę, kurioje bus kaupiamos nuostatos ir kuriai bus apmokami pareikalavimai. Taip pat galite nustatyti skirtingas nuostatas debeto sąskaitoms ir nurašymo kredito sąskaitoms pagal šaltinio registruojamą įmonę.

Norėdami nustatyti grąžinimo valdymo registravimo šablonus klientams ir tiekėjams, eikite į **Grąžinimų valdymas \> Grąžinimų valdymo registravimo sąranka \> Grąžinimų valdymo registravimo šablonai**. Puslapyje **Grąžinimų valdymo registravimo šablonai** yra sąrašo sritis, kurioje rodomi visi jūsų turimi šablonai. Veiksmų srityje esančius mygtukus galite naudoti šablonų įtraukimui į sąrašą arba jų pašalinimui.

Likusiuose šios temos skyriuose aprašoma, kaip naudoti galimus laukus kuriant arba redaguojant profilį.

## <a name="posting-profile-header"></a>Registravimo šablono antraštė

Šioje lentelėje aprašomi parametrai, kurie galimi kiekvieno grąžinimo valdymo registravimo šablono antraštės skyriuje.

| Laukas | Aprašas |
|---|---|
| Registravimo šablonas | Įveskite unikalųjį šablono pavadinimą. |
| Aprašas | Įveskite šablono aprašymą. |
| Modulis | Pasirinkite su šablonu susietų mokesčių ir autorinių honorarų modulį (*Klientas* arba *Tiekėjas*). |
| Tipas | Pasirinkite šablono tipą (*Grąžinimas* arba *Autorinis honoraras*). |
| Mokėjimo tipas | <p>Šiame lauke nustatomas užregistruoto grąžinimo išeigos formatas.<p><p>Kai laukas **Tipas** nustatytas į *Grąžinimas*, galimos šios vertės:</p><ul><li>*Mokėti naudojant mokėtinas sumas* – kai klientas registruoja grąžinimą, sukuriama tiekėjo sąskaita faktūra pavedimo tiekėjui, kuri nustatoma kuriant grąžinimo klientą. Ataskaitos – kai tiekėjas registruoja grąžinimą, sukuriama tiekėjo sąskaita faktūra grąžinimo tiekėjo sąskaitai.</li><li>*Kliento atskaitymai* – kai registruojate grąžinimą, sukuriamas kliento atskaitymų žurnalas, skirtas grąžinimo klientui.</li><li>*Mokesčių sąskaita faktūra kliento atskaitymams* – kai registruojate grąžinimą, sukuriama laisvos formos sąskaita faktūra, skirta grąžinimo klientui.</li><li>*Prekybos išlaidos* – kai registruojate grąžinimą, sukuriamas kliento atskaitymų žurnalas, skirtas grąžinimo klientui.</li><li>*Ataskaitos* – kai registruojate grąžinimą, sukuriamas kliento atskaitymų žurnalas, skirtas grąžinimo klientui.</li></ul><p>Kai laukas **Tipas** nustatytas į *Autorinis honoraras*, galimos šios vertės:</p><ul><li>*Mokėti naudojant mokėtinas sumas* – kai registruojate grąžinimą, sukuriama tiekėjo sąskaita faktūra grąžinimo tiekėjo sąskaitai.</li><li>*Ataskaitos* – kai registruojate grąžinimą, sukuriama tiekėjo sąskaita faktūra grąžinimo tiekėjo sąskaitai.</li></ul><p>Daugiau informacijos rasite sekančiame skyriuje [Mokėjimo tipai](#payment-types). |
| Įmonė | Pasirinkite įmonę (juridinį subjektą), kurioje bus kaupiamos nuostatos ir kuriai bus apmokami pareikalavimai. |

### <a name="payment-types"></a>Mokėjimo tipai

Šioje lentelėje apibendrinama, kaip įvairūs lauko **Mokėjimo tipas** parametrai daro įtaką mokėjimų registravimo vietai. Mokėjimai gali būti registruojami kliento sąskaitoje, tiekėjo sąskaitoje arba pavedimo sąskaitoje, atsižvelgiant į paskirties operaciją ir grąžinimo tipą.

| Mokėjimo tipas | Paskirties operacijos tipas | Grąžinimo tipas | Mokėjimas (kam) (SF sąskaita) |
|---|---|---|---|
| Mokėti pagal mokėtinas sumas | Tiekėjo SF žurnalas | Kliento grąžinimas | Kliento pavedimo tiekėjo sąskaita |
| Mokėti pagal mokėtinas sumas | Tiekėjo SF žurnalas | Kliento autorinis honoraras | Tiekėjo kodas |
| Mokėti pagal mokėtinas sumas | Tiekėjo SF žurnalas | Tiekėjo grąžinimas | Tiekėjo kodas |
| Kliento atskaitymai | Kasdieninis žurnalas | Kliento grąžinimas | Kliento sąskaita |
| Mokesčių sąskaita faktūra kliento atskaitymams | Laisvos formos SF | Kliento grąžinimas | Kliento sąskaita |
| Prekybos išlaidos | Kasdieninis žurnalas | Kliento grąžinimas | Kliento sąskaita |
| Ataskaitos | Kasdieninis žurnalas | Kliento grąžinimas | Kliento sąskaita |
| Ataskaitos | Tiekėjo SF žurnalas | Kliento autorinis honoraras | Tiekėjo kodas |
| Ataskaitos | Tiekėjo SF žurnalas | Tiekėjo grąžinimas | Tiekėjo kodas |

> [!NOTE]
> Atsižvelkite į šiuos dalykus, kai nustatote [Grąžinimo valdymo sandorius](rebate-management-deals.md):
>
> - Sandoriams, kurių laukas **Derinti pagal** nustatytas į *Sandoris*, negalite naudoti dinaminės sandorio sąskaitos registravimo metu. Turite naudoti nurodytą kliento arba tiekėjo sąskaitą.
> - Sandoriams, kurių laukas **Derinti pagal** nustatytas į *Eilutė*, galite naudoti registravimo šabloną, kuris pasislenka į dinaminę sandorio sąskaitą sandorio eilutėje, kadangi klientas arba tiekėjas yra nustatytas pagal sandorio eilutę.

## <a name="posting-fasttab"></a>„FastTab“ registravimas

Šioje lentelėje aprašomi laukai, kurie galimi kiekvieno grąžinimo valdymo registravimo šablono „FastTab” **Registravimas**.

| Laukas | Aprašas |
|---|---|
| Kredito tipas | Pasirinkite, ar kredituoti didžiosios knygos ar kliento sąskaitą. Jei antraštėje esantis laukas **Mokėjimo tipas** nustatytas į *Mokesčių sąskaita faktūra kliento atskaitymams*, šis laukas nustatomas į *Didžiosios knygos sąskaita*. Tiekėjo grąžinimams šis laukas nustatytas kaip *Didžiosios knygos sąskaita*. |
| Kredito sąskaita | Pasirinkite sąskaitą, į kurią registruojamos kredito sumos, kai atliekamos grąžinimo nuostatos. Ši sąskaita taip pat bus naudojama kaip poslinkio sąskaita, kai grąžinimas bus užregistruotas kredituoti klientui arba debetuoti tiekėjui. |
| Žurnalo pavadinimas<br>(Skyriuje **Nuostata**) | Pasirinkite žurnalo, kuris bus naudojamas užregistruotoms nuostatoms įrašyti, pavadinimą. |
| Tipas | Pasirinkite, ar norite registruoti grąžinimo didžiosios knygos, kliento ar tiekėjo sąskaitoje. Jei antraštėje esantis laukas **Mokėjimo tipas** nustatytas į *Mokesčių sąskaita faktūra kliento atskaitymams*, šis laukas nustatomas į *Klientas/Tiekėjas*. |
| Sąskaitos šaltinio naudojimas | <p>Pasirinkite vieną iš šių reikšmių:</p><ul><li>*Fiksuota sąskaita* – jei pasirinksite šią vertę, turėsite nurodyti sąskaitą lauke **Grąžinimo sąskaita**.</li><li>*Sandorio eilutės sąskaita* – naudokite kliento arba tiekėjo sąskaitą, nurodytą grąžinimo eilutėje. Šią reikšmę galite pasirinkti tik tiems sandoriams, kurių laukas **Derinti pagal** nustatytas į *Eilutė* ir lauko **Sąskaitos kodas** sandorio eilutės nustatytos į *Lentelė*. Ji netaikomas kliento autorinių atlyginimų registravimo šablonams arba tiekėjo grąžinimams, pagrįstiems pardavimo užsakymais.</li></ul> |
| Grąžinimų sąskaita | Sąskaita, kurioje registruojamos faktinės grąžinimų išlaidos. |
| Žurnalo pavadinimas<br>(Lauko **Grąžinimų valdymas** grupėje) | Pasirinkite žurnalo pavadinimą, kurį norite naudoti grąžinimo sumos kredito pastabos registravimui klientui arba tiekėjui. Šis laukas yra negalimas, kai antraštėje esantis laukas **Mokėjimo tipas** nustatytas į *Mokesčių sąskaita faktūra kliento atskaitymams*. Klientų grąžinimo žurnalams bus galimi *Kasdienio* žurnalo tipo pavadinimai. Klientų autoriniams atlyginimams ir tiekėjo grąžinimams bus galimi *Tiekėjo SF įrašymo* žurnalo tipo pavadinimai. |
| Prekės PVM grupė | Nurodykite, ar grąžinimas yra apmokestinamas. |
| Žurnalo pavadinimas<br>(Lauko **Nurašyti** grupėje) | Jei užregistruotas grąžinimas nėra lygus nuostatai, skirtumą galima nurašyti. Pasirinkite žurnalo, kuris bus naudojamas užregistruotiems nurašymams įrašyti, pavadinimą. |

## <a name="posting-by-company-fasttab"></a>Registravimo pagal įmonę „FastTab”

Kiekvieno grąžinimo valdymo registravimo šablono „FastTab” **Registravimas pagal įmonę** leidžia jums nurodyti kiekvienos įmonės (juridinio subjekto) registravimo sąskaitą tinklelyje.

Naudokite įrankių juostos mygtukus, norėdami įtraukti įmones į tinklelį ir pašalinti jas. Kiekvieną kartą įtraukdami eilutę į tinklelį naudokite lauką **Įmonė**, jei norite nurodyti juridinį subjektą tai eilutei. Tada laukas **pavadinimas** nustatomas automatiškai.

Kiekvienai įmonei pasirinkite eilutę ir įveskite šią informaciją naudodami laukus, esančius žemiau tinklelio:

- **Debeto tipas** – pasirinkite, ar debetuoti didžiosios knygos ar tiekėjo sąskaitą. Kliento grąžinimams ir autoriniams atlyginimams šis laukas nustatytas kaip *Didžiosios knygos sąskaita*.
- **Debeto sąskaita** – įveskite sąskaitą, į kurią registruojama debeto suma, kai atliekamos grąžinimo nuostatos.
- **Pagrindinė sąskaita** – pasirinkite nurašymų pagrindinę sąskaitą.
