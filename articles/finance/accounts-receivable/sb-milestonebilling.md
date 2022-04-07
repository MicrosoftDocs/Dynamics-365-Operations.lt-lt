---
title: Etapo šablonai
description: Šioje temoje paaiškinama, kaip nustatyti rodyklės atsiskaitymo pasisąrašymo informaciją abonemento sąskaitose.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 863ec55c8ba2fcc9d0e624fcca06f4491ce839ac
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462914"
---
# <a name="milestone-billing"></a>Rodyklės atsiskaitymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti rodyklės atsiskaitymo funkcijos šablonus abonemento sąskaitose. Kiekvienai rodyklės šablono eilutei galite nurodyti paskirstymo procentą arba sumą. Tada galite priskirti rodyklės šabloną atsiskaitymo grafiko elementams, kurie naudoja rodyklės atsiskaitymo funkciją.

## <a name="add-a-template"></a>Įtraukti šabloną

Norėdami įtraukti rodyklės šabloną, atlikite šiuos veiksmus.

1. Eikite į **Abonemento atsiskaitymo pasikartojančios \> sutarties atsiskaitymo nustatymo \> rodyklės \> šablonus**.
2. Pasirinkite **Nauja**.
3. Lauke Rodyklės **šablonas** įveskite unikalų naujo šablono identifikatorių.
4. Lauke **Aprašas** įveskite aprašą.
5. **Lauke Paskirstymo metodas** pasirinkite paskirstymo metodą.
6. Pasirinktinai: lauke **Bendroji** suma nurodykite bendrą šablono sumą.
7. Norėdami pridėti eilutę, pasirinkite **Įtraukti**. Tada lauke **Prekės numeris** pasirinkite naujos eilutės prekės numerį.
8. Atlikite vieną iš šių veiksmų, atsižvelgdami į vertę, kurią pasirinkote paskirstymo **metodo** lauke:

    - Jei pasirinkote **Procentinį** dydį kaip paskirstymo **metodą**, lauke Procentai nurodykite kiekvienos eilutės paskirstymo procentą. Jei nurodysite procentus, procentų suma, rodoma lauke **Bendra procentinė** išraiška turi būti lygi **100**.
    - Jei kintama **suma** pasirinkta kaip paskirstymo metodas, lauke **Suma** nurodykite kiekvienos eilutės sumą.
    - Jei kaip **paskirstymo metodą** pasirinkote Lygi suma, sumos nurodyti nereikia. Kiekviena eilutė bus atnaujinta teisinga procentine dalimi ir suma, atsižvelgiant į į šabloną pridėtų prekių skaičių.

9. Pasirinkite **Įrašyti**.

## <a name="delete-a-template"></a>Šablono naikinimas

Norėdami panaikinti rodyklės šabloną, atlikite šiuos veiksmus.

1. Pasirinkite vieną ar daugiau eilučių, kurias norite naikinti, tada pasirinkite **Naikinti**.
2. Kai paraginamas patvirtinti veiksmą, pasirinkite **Taip**.

## <a name="milestone-template-fields"></a>Rodyklės šablono laukai

Rodyklės **šablono** puslapyje yra šie laukai.

| Laukas | Aprašymas |
|-------|-------------| 
| Etapo šablonas | Unikalus rodyklės šablono identifikatorius. |
| Aprašymas | Rodyklės šablono aprašymas. |
| Paskirstymo metodas | <p>Pasirinkite paskirstymo metodą:</p><ul><li>**Baigimo procentas** – kiekvienai eilutei naudojama kaupiamoji užbaigimo vertė.</li><li>**Procentas** – gali būti nurodyta paskirstymo procento suma. Visų procentų suma turi būti lygi 100.</li><li>**Kintama** suma – gali būti nurodyta paskirstymo suma. Paskirstymo suma nurodoma operacijos lygyje.</li><li>**Lygi suma** – paskirstymo procentai apskaičiuojami automatiškai ir vienodai padalijami šablone prekėms.</li></ul> |
| Bendroji suma | Nurodykite šablono rodyklės sumą. |
| **Linijos** | |
| Prekės numeris | Pasirinkite rodyklės šablono prekės numerį. |
| Produkto pavadinimas | Prekės pavadinimas. |
| Procentai | <p>Įveskite eilutės paskirstymo procentą:</p><ul><li>Jei lauke **Paskirstymo** metodas nustatytas **procentas**, nurodykite eilutės procentą.</li><li>Jei lauke **Paskirstymo metodas** nustatyta Lygi **suma**, procentai automatiškai padalijami į lygias procentines dalis, remiantis šablone esančių prekių skaičiumi.</li></ul><p>Visų procentų suma turi būti lygi 100.</p><p>Jei antraštėje **nurodyta** bendros sumos vertė ir jūs pakeičiate eilutės **Procento** vertę, sumos **vertė** atnaujinama. Jei, priešingai, pakeičiate sumos **vertę**, procentinė **vertė** atnaujinama.</p> |
| Suma | <p>Eilutės paskirstymo suma:</p><ul><li>Jei lauke **Paskirstymo** metodas nustatyta kintama **suma**, nurodykite eilutės sumą.</li><li>Jei lauke **Paskirstymo metodas** **nustatyta** Lygi suma, suma automatiškai padalijama į lygias sumas, **remiantis** šablone esančių prekių skaičiumi ir bendra sumos verte, nurodyta antraštėje.</li></ul><p>Visų sumų suma turi būti lygi bendros sumos **vertei**, kuri nurodyta antraštėje.</p><p>Jei antraštėje **nurodyta** bendros sumos vertė ir jūs pakeičiate **eilutės** sumos vertę, procentinė **vertė** atnaujinama. Jei, priešingai, pakeičiate procento **vertę**, **atnaujinama** sumos vertė.</p> |
| **Sumos** | |
| Bendrasis procentas | Procentų suma. Visų procentų suma turi būti lygi 100. |
| Bendroji suma | Visų eilučių **sumos** verčių suma. Ši suma turi būti lygi **bendros** sumos vertei, kuri nurodyta antraštėje. |
| Likusi suma | Likusi suma. Vertė apskaičiuojama iš antraštės bendrosios **sumos** atėmus visų eilučių sumos **verčių** sumą.|

## <a name="milestone-allocation"></a>Etapo paskirstymas

Prieš pradėdami naudoti rodyklės funkciją, turite atlikti šias užduotis.

1. Pridėti vieną ar daugiau rodyklės šablonų.
2. Sukurkite atsiskaitymo grafiko grupę. Nurodykite **rodyklės** tipą kaip prekės tipą ir pasirinkite šabloną.
3. Prekių nustatymo **puslapyje** (Abonemento atsiskaitymo **pasikartojančios \> sutarties atsiskaitymo nustatymo \>\> prekės**) pasirinkite prekės ryšį ir rodyklės šabloną prekės nustatymui.

Sukūrę rodyklės šablonus, atsiskaitymo grafiko grupes ir elementus, galite sukurti atsiskaitymo grafiką, kuriame naudojama rodyklės funkcija.

Norėdami nustatyti atsiskaitymo tvarkaraštį, kuriame naudojami etapai, atlikite šiuos veiksmus.

1. Iš visų **/ aktyvių atsiskaitymo grafikų** sąrašo **, kuriame pateikti sąskaitų pateikimo grafikai**, pasirinkite **Nauja**.
2. Puslapyje Visi **sąskaitų pateikimo grafikai** sukurkite naują sąskaitų pateikimo grafiką ir nurodykite kliento kodą bei pradžios datą.
3. Atsiskaitymo grafiko **eilučių** skyriuje pasirinkite Įtraukti **eilutę**. Tada pridėkite prekės numerį ir nustatykite prekės **tipo lauką** Rodyklė **·**.

    Jei nustatytas numatytasis prekės rodyklės šablonas, rodyklės įvykiai automatiškai pridedami prie atsiskaitymo grafiko eilučių. Rodyklės eilučių pabaigos datos yra tuščios.

    Jei prekei nustatytas joks rodyklės šablonas, pasirinkite Rodyklės **paskirstymą**. Tada rodyklės paskirstymo **puslapyje** pasirinkite rodyklės šabloną ir atlikite reikalingus atnaujinimus. Tada pasirinkite **Uždaryti,** norėdami grįžti į atsiskaitymo grafiką ir baigti kurti atsiskaitymo grafiką.

4. Norėdami sukurti SF atsiskaitymo grafikui, turite atnaujinti kiekvieno rodyklės įvykio pabaigos datą. Viename atsiskaitymo grafike galite atnaujinti rodyklės įvykio pabaigos datą atsiskaitymo grafiko eilutėse. Norėdami atnaujinti kelis atsiskaitymo grafikus, pasirinkite Naujinti **užbaigimo datos procesą**.
5. Atnaujinę pabaigos datą, galite sukurti SF. Norėdami naudoti vieną atsiskaitymo grafiką, visų **atsiskaitymo** grafikų **puslapyje pasirinkite Generuoti** SF. Norėdami sukurti kelių sąskaitų pateikimo grafikų SF, pasirinkite Generuoti SF arba Generuoti SF **paketinį** vykdymą dalyje **Periodinės** užduotys **.**

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Redaguoti rodyklės paskirstymą atsiskaitymo grafiko eilutėje

Norėdami redaguoti rodyklės paskirstymą atsiskaitymo grafiko eilutėje, atlikite šiuos veiksmus.

1. Atsiskaitymo grafikų **puslapyje** > **Visi** arba aktyvūs atsiskaitymo grafikai, **lauke Grafiko numeris** pasirinkite atsiskaitymo grafiko numerį.
2. Atsiskaitymo grafiko **eilučių skyriuje** įveskite prekę, nurodykite rodyklės **elementą** ir pasirinkite Rodyklės **paskirstymą**.
3. Rodyklės **šablono** lauke, pasirinkite rodyklės šabloną.
4. Pasirinkite **procesą**. Rodyklės šablono eilutės automatiškai pridėtos prie atsiskaitymo grafiko eilučių.

## <a name="milestone-allocation-fields"></a>Rodyklės paskirstymo laukai

Rodyklės **paskirstymo** puslapyje yra šie laukai.

| Laukas | Aprašymas |
|-------|-------------|
| Pirminė prekė | Pirminio elemento numeris. |
| Išplėstinė kaina | <p>Išplėstinė prekės kaina. Vertė atitinka atsiskaitymo grafiko **eilutės** grynosios sumos vertę.</p></p>Pirminėje rodyklės prekėje numatytoji vertė yra bendroji **sumos vertė**, nurodyta rodyklės šablone. Jei bendroji suma yra 0 (nulis), numatytoji vertė yra atsiskaitymo **grafiko** eilutės grynoji sumos vertė.</p> |
| Etapo šablonas | Eilutės elemento rodyklės šablono ID. |
| Šablono aprašas | Rodyklės šablono aprašymas. |
| Paskirstymo metodas | Paskirstymo metodas, naudojamas rodyklės šablone. |
| **Linijos** | Numatytosios visų eilučių vertės remiasi pasirinktu rodyklės šablonu. Jei reikia, juos galima keisti. |
| Prekės numeris | Rodyklės paskirstymo šablono prekės numeris. |
| Produkto pavadinimas | Produkto pavadinimas. |
| Procentai | <p>Eilutės paskirstymo procentas. Visų procentų suma turi būti lygi 100.</p><p>Jei pakeisite **eilutės** procento vertę, grynoji **sumos** vertė bus atnaujinta. Jei, priešingai, pakeičiate grynosios **sumos vertę**, procentas **atnaujinamas**.</p> |
| Grynoji suma | <p>Eilutės paskirstymo suma. Visų eilučių grynųjų sumų suma turi būti lygi išplėstinės **kainos** vertei, kuri nurodyta antraštėje.</p><p>Jei pakeisite **eilutės grynosios** sumos vertę, procentinė **vertė** bus atnaujinta. Priešingai, jei pakeičiate procento **vertę**, **grynoji suma** atnaujinama.</p> |
| **Sumos** | |
| Bendrasis procentas | Procentinių **verčių** suma visose eilutėse. Ši suma turi būti lygi 100. |
| Bendroji suma | Visų eilučių **grynosios sumos** verčių suma. Ši suma turi būti lygi **antraštės** nurodytai išplėstinės kainos vertei. |
| Likusi suma | Likusi suma. Vertė skaičiuojama kaip išplėstinės kainos **vertė iš** antraštės atėmus visų eilučių **Grynosios** sumos verčių sumą. Galutinė suma turi būti lygi 0 (nuliui). |
