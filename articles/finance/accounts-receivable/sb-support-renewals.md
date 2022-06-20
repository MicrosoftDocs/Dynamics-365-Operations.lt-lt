---
title: Palaikymas ir atnaujinimas
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir naudoti pardavimo užsakymų palaikymo ir atnaujinimo procesą, siekiant sukurti prekių atnaujinimo grafiką.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b40e0136883d909755480a3ce101627297bd9ffb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896527"
---
# <a name="support-and-renewals"></a>Palaikymas ir atnaujinimas 

Šiame straipsnyje paaiškinama, kaip įvesti palaikymo prekes arba atnaujinti prekes, kai įvedate pardavimo užsakymus. Šios prekės naudojamos apskaičiuojant pradinės palaikymo sutarties išlaidų sumą ir (arba) atnaujinimo sumą, kuri naudojama kuriant sąskaitų pateikimo grafiką abonemento sąskaitose. Pavyzdžiui, jūsų įmonė parduoda serverį klientui, o jūs siūlote pirmųjų metų duomenų atsarginės kopijos abonementą ir pasirinktį atnaujinti tą abonementą kasmet. Palaikymo *prekė yra* pirmųjų metų abonementas, o atnaujinimo *prekė yra* kiekvieno paskesnio metų atnaujinimas.

Galima įvesti palaikymo sutarties, atnaujinimo sutarties arba abiejų informacijos informaciją. Kai įvedate palaikymo sutarties informaciją, į pardavimo užsakymą įtraukiama tik palaikymo prekė. Kai įvedate atnaujinimo sutarties informaciją, atnaujinimo prekė naudojama sąskaitų pateikimo grafikui sukurti.

## <a name="support-and-renewal-setup"></a>Palaikymo ir atnaujinimo nustatymas

Puslapyje Palaikymo **ir atnaujinimo lygiai** galite nustatyti skirtingus palaikymo ir atnaujinimo prekių lygius. Palaikymas arba atnaujinimas gali būti pradinės prekės sumos procentas arba tai gali būti standartinė suma.

Numatytuosius palaikymo lygius galite pasirinkti periodinių **sutarties atsiskaitymo parametrų** puslapyje.

Pavyzdžiui, įmonė gali pasiūlyti šiuos palaikymo ir atnaujinimo lygius.

| Palaikymo lygis | Palaikymo procentinė dalis | Atnaujinimo procentinė dalis |
|---|---|---|
| Neribota | 40 % | 30 % |
| Aukso | 25 % | 18% |
| Sidabro | 20 % | 14% |
| Bronzos | 15 % | 10 % |

Norėdami sukurti palaikymo ar atnaujinimo lygį, atlikite šiuos veiksmus.

1. Puslapyje Palaikymas **ir atnaujinimo lygiai** pasirinkite **Naujas**.
2. **Lauke Palaikymo lygis** įveskite unikalų pavadinimą.
3. Lauke **Aprašas** įveskite aprašą.
4. **Lauke Palaikymo skaičiavimo metodas** pasirinkite palaikymo skaičiavimo metodą. Jei pasirinksite **Procentas**, įveskite palaikymo procentą lauke **Palaikymo** procentas.
5. **Atnaujinimo skaičiavimo metodo lauke** pasirinkite atnaujinimo skaičiavimo metodą. Jei pasirinksite **Procentą**, įveskite atnaujinimo procentą atnaujinimo **procento** lauke.
6. Pasirinkite **Įrašyti**.

### <a name="fields"></a>Laukai

Puslapyje **Palaikymo ir atnaujinimo** lygiai yra šie laukai.

| Laukas | Aprašymas |
|---|---|
| Palaikymo lygis | Unikalus palaikymo ar atnaujinimo lygio identifikatorius (pavyzdžiui, auksinė **arba** sidabro **·**). |
| Aprašymas | Palaikymo arba atnaujinimo lygio aprašas. |
| Palaikymo skaičiavimo būdas | Pasirinkite lygio : procentinės dalies arba standartinės **sumos** – **palaikymo skaičiavimo metodą**. |
| Palaikymo procentinė dalis | Jei kaip palaikymo **skaičiavimo** metodą pasirinkote Procentas, nurodykite procentą, kuris naudojamas palaikymo prekės kainai apskaičiuoti. Jei pasirinkote **standartinę** sumą kaip skaičiavimo metodą, suma nurodoma kuriant operaciją. |
| Atnaujinimo skaičiavimo būdas | Pasirinkite lygio : procentinės arba standartinės sumos **atnaujinimo** **skaičiavimo metodą**. |
| Atnaujinimo procentinė dalis | Jei pasirinkote **procentą** kaip atnaujinimo skaičiavimo metodą, nurodykite procentą, kuris naudojamas atnaujinimo prekės kainai apskaičiuoti. Jei pasirinkote **standartinę** sumą kaip skaičiavimo metodą, suma nurodoma kuriant operaciją. |

## <a name="support-and-renewal-process"></a>Palaikymo ir atnaujinimo procesas

Palaikymo ir atnaujinimo funkcija gali taikyti skirtingus palaikymo lygius prekėms ir atnaujinti atnaujinimo informaciją abonemento sąskaitos pateikimo metu.

Prieš naudojant palaikymo ir atnaujinimo funkciją, turi būti atlikta ši užduotis.

1. Puslapyje Palaikymo **ir atnaujinimo lygiai** sukurkite bent vieną palaikymo arba atnaujinimo lygį.
2. Prekių nustatymo **puslapyje susieti** prekę su palaikymo ir atnaujinimo prekėmis. Ši užduotis būtina tik tuo atveju, jei norite nustatyti numatytąsias palaikymo ir (arba) atnaujinimo prekių vertes.
3. Periodinio **sutarties atsiskaitymo parametrų** puslapyje nurodykite numatytuosius naujų atsiskaitymo grafikų palaikymo ir atnaujinimo parametrus.

Norėdami prekėms taikyti skirtingus palaikymo lygius ir atnaujinti atnaujinimo informaciją, atlikite šiuos veiksmus.

1. **Puslapyje Visi pardavimo užsakymai** sukurkite pardavimo užsakymą.
2. Pardavimo užsakymo **eilutėse "** FastTab" pridėkite prekę.
3. Skirtuke **SF** pasirinkite Palaikymas ir atnaujinimas **Įtraukti palaikymą \> ir atnaujinimą**.
4. **Puslapio Palaikymas ir atnaujinimas,** antraštės skyrius atnaujinamas parametrais iš periodinio **sutarties atsiskaitymo parametrų** puslapio. Šios vertės taikomos visoms palaikymo ir atnaujinimo prekėms. (Pvz., jei atsiskaitymo dažnumas nustatytas kaip **Kiekvienais** metais visų pardavimo eilučių, sukurtų su atnaujinimo preke, dažnis yra metinis.) Norėdami susieti pardavimo užsakymą su esamu atsiskaitymo grafiku, pasirinkite vertę lauke **Atsiskaitymo grafiko** numeris.
5. Norėdami pakeisti palaikymo arba atnaujinimo pradžios datą, nustatykite parinktį **Perrašyti pradžios datą** kaip **Taip**.
6. Norėdami pridėti arba redaguoti palaikymo elementą, pažymėkite žymės **langelį** Palaikymas, tada įveskite palaikymo elementą lauke **Palaikymo** elementas. Prekė pridedama prie pardavimo užsakymo.
7. Norėdami įtraukti ar redaguoti atnaujinimo prekę, pažymėkite **atnaujinimo** žymės langelį, tada įveskite atnaujinimo prekę atnaujinimo **prekės** lauke. Kai pardavimo užsakymui išrašoma SF, bus sukurtas atsiskaitymo grafikas, kuriame yra prekė.
8. Pasirinkite **Gerai**.
9. Skirtuke **Generuoti** pasirinkite **SF**. Kai pardavimo užsakymas užregistruojamas, sukuriamas atsiskaitymo grafikas. Pranešimo informacoje rodomas pranešimas, kuriame yra atsiskaitymo grafiko informacija.
10. Visų / **aktyvių atsiskaitymo grafikų** sąrašo puslapyje pasirinkite atsiskaitymo grafiko numerį, **kad peržiūrėtumėte išsamią atsiskaitymo grafiko informaciją atsiskaitymo grafiko** puslapyje.
11. Atsiskaitymo grafiko **eilutėse** "FastTab" **pasirinkite Palaikymas ir** atnaujinimas, kad peržiūrėtumėte sukurtų eilučių informaciją.

> [!NOTE]
> Jei reikia pakeisti atsiskaitymo grafiko eilutės atnaujinimo pradžios datą, **·** **galite redaguoti eilutės, kuri yra atsiskaitymo grafikų puslapyje, pradžios datos** reikšmę. Kai atidarote eilutės **puslapį Peržiūrėti** atsiskaitymo informaciją, laukas **Atsiskaitymo pradžios data** atnaujinamas nauja data. Atsiskaitymo **pabaigos datos** vertė perskaičiuojama atsižvelgiant į atsiskaitymo dažnumą. Atnaujinimo pradžios datą galima atnaujinti tik tuo atveju, jei nebuvo sukurta ir užregistruota pirmoji atnaujinimo sąskaitų pateikimo grafiko SF. Sukūrus ir užregistrus pirmą SF, pradžios datos redaguoti negalima.

Galimas tik pardavimo užsakymo palaikymo ir atnaujinimo procesas. Kai į pardavimo užsakymą įtraukiate palaikymo ir atnaujinimo prekes, galite sukurti naują atsiskaitymo grafiką arba įtraukti atnaujinimo prekę į esamą sąskaitų pateikimo grafiką.

## <a name="support-and-renewal-audit"></a>Palaikymo ir atnaujinimo auditas

Audito puslapio **Palaikymas ir atnaujinimas** galite peržiūrėti informaciją apie atsiskaitymo grafiko eilutes, kurios sukurtos iš atnaujinimo prekės pardavimo užsakyme. Ši parinktis galima, kai atsiskaitymo grafiko eilutės elementas yra atnaujinimo prekė.

Norėdami redaguoti atsiskaitymo grafiko eilutės palaikymo ir atnaujinimo informaciją, atlikite šiuos veiksmus.

1. Puslapyje Visi **atsiskaitymo grafikai** pasirinkite atsiskaitymo grafiko numerį.
2. **Atsiskaitymo grafiko eilučių** skyriuje pasirinkite eilutę, tada pasirinkite Palaikymas ir **atnaujinimas**.
3. Peržiūrėkite visą palaikymo arba atnaujinimo prekės informaciją.
4. Atlikite reikalingus palaikymo lygio arba atnaujinimo procento ar sumos pakeitimus, tada įveskite reikšmę lauke **Pakeitimo** priežastis.
5. Pasirinkite **procesą**.

### <a name="fields"></a>Laukai

Audito **puslapio Palaikymas ir** atnaujinimas apima šiuos laukus.

| Laukas | Aprašymas |
|-------|-------------|
| Prekės numeris | Atsiskaitymo grafiko eilutės prekės numeris. |
| Produkto pavadinimas | Produkto pavadinimas. |
| Palaikymo plano lygis | Peržiūrėkite arba pakeiskite atnaujinimo elemento palaikymo lygį. |
| Atnaujinimo procentinė dalis | Įveskite atnaujinimo procentinę dalį, naudojamą, kai vieneto kaina apskaičiuojama atnaujinti prekę atsiskaitymo grafike. |
| Atnaujinimo suma | Įveskite atnaujinimo sumą, kuri naudojama, kai vieneto kaina apskaičiuojama atnaujinant prekę atsiskaitymo grafike. |
| Keitimo priežastis | Įveskite palaikymo ir atnaujinimo informacijos keitimo priežastį. Turite įvesti priežastį, keisdami atnaujinimo **procentą**, atnaujinimo **sumą** arba palaikymo **plano lygio** vertę. |
| Pradinė pardavimo prekė | Pradinis pardavimo prekės numeris iš pardavimo užsakymo. |
| Pradinė grynoji suma | Pradinė grynoji prekės suma. |
| Pradinis palaikymo lygis | Pradinis prekės palaikymo lygis. |
| Pradinė atnaujinimo procentinė dalis | Pradinis prekės atnaujinimo procentas. |
| Pradinė atnaujinimo suma | Pradinė prekės atnaujinimo suma. |
| **Tinklelis** | |
| Pradinis palaikymo lygis | Ankstesnis palaikymo lygis. |
| Pradinė atnaujinimo procentinė dalis | Ankstesnis atnaujinimo procentas. |
| Pradinė atnaujinimo suma | Ankstesnė atnaujinimo suma. |
| Modifikavo | Pakeitimą vartotojo, kuris atliko keitimą, vardas. |
| Pakeitimo data ir laikas | Keitimo data. |
| Priežastis | Keitimo priežastis. |
