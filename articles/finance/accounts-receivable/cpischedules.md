---
title: Vartotojų kainų indekso grafikas
description: Šiame straipsnyje paaiškinama, kaip sukurti vartotojo kainų indeksų (CPI) grafikų, kuriuos gaunate iš interneto, sąrašą, kad padėtumėte nustatyti perskyrimo mokestį abonemento sąskaitose.
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
ms.openlocfilehash: f08b79ee00baab3713d9ccc24a7595b1de7a7768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904879"
---
# <a name="consumer-price-index-schedule"></a>Vartotojų kainų indekso grafikas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip kurti, naikinti, peržiūrėti ir apdoroti vartotojo kainos indekso (CPI) grafikus. CPI grafikas gali būti naudojamas nustatyti vartotojų prekių ir paslaugų kainas, kurias pridedate kaip sąskaitų pateikimo grafiko eilutes. Tada CPI grafiką galima naudoti su perskyrimo ir nuolaidos kainomis atsiskaitymo grafike, arba jis gali būti apdorojamas rankiniu būdu, norint atnaujinti atsiskaitymo sumas sąskaitų pateikimo grafikuose. Galite rankiniu būdu įvesti CPI grafikus arba importuoti juos naudodami CPI grafiko sudėtinį objektą.

Norėdami įtraukti CPI grafiką, atlikite šiuos veiksmus.

1. Vartotojo kainų **indekso grafiko** puslapyje pasirinkite **Naujas**.
2. Vartotojo kainų **indekso grafiko** lauke įveskite unikalų pavadinimą.
3. Lauke **Aprašas** įveskite aprašą.
4. Skirtuke **Vartotojo kainų indekso grafikas** pasirinkite **Įtraukti**.
5. Vartotojo kainos **indekso datos lauke** nurodykite datą, kada naujas CPI grafikas taps aktyvus.
6. Vartotojo kainų **indekso grafiko** lauke įveskite pavadinimą, kurį įvedėte 2 žingsniu.
7. Pasirinkite **Įrašyti**.

Norėdami panaikinti CPI grafiko datą, atlikite šiuos veiksmus.

1. Vartotojo kainų **indekso grafiko** puslapyje pasirinkite vieną ar daugiau eilučių, kurias norite naikinti, tada pasirinkite **Šalinti**.
2. Norėdami panaikinti visą CPI grafiką, veiksmų srityje pasirinkite **Naikinti**. Negalima panaikinti pasirinkto CPI grafiko, jei jis susietas su bet kuriuo atsiskaitymo grafiku.
3. Veiksmų srityje pasirinkite Procesas, norėdami **atnaujinti** atsiskaitymo grafikus, kurie naudoja pasirinktą CPI grafiką. Paskutinės CPI datos ir grafiko sumos bus naudojamos atnaujinti atsiskaitymo grafiko kainas.
4. Vartotojo kainų **indekso** proceso "FastTab **" peržiūrėkite atnaujintą atsiskaitymo grafiko** numerį, prekės numerį, **·** **atsiskaitymo** pradžios datą, **atsiskaitymo pabaigos** datą, **·** **perskyrimo datą ir perskyrimo dažnumo** laukus.

Kai CPI grafikai nustatyti, juos galima naudoti perskyrimo ir nuolaidos kainų pokyčiams atsiskaitymo grafikuose.

## <a name="cpi-calculation"></a>CPI skaičiavimas

Šiuose pavyzdžiuose laikotarpis yra nuo 2020 m. sausio 1 d. iki 2022 m. gruodžio 31 d. Pagrindinis CPI tarifas (CPI vertė paleidus sutartį) yra 105,65. 2021 m. sausio 1 d. dabartinis CPI yra 110,5. 2022 m. sausio 1 d. dabartinis CPI yra 114,25. Pradinė suma yra $1,000.

**1 pavyzdys**

Periodinio **sutarties atsiskaitymo parametrų** puslapyje nustatote vartotojo kainos **indekso skaičiavimo lauką** kaip Pagrindinio **vartotojo kainos indeksą**.

2021 m. sausio 1 d. laikotarpio pirmoji perskyrimo suma apskaičiuojama tokiu būdu, remiantis pradine suma:

1 000 + (110,5 – 105,65) &divide; 105,65 &times; 1 000 = 1 045,91

Perskyrimo suma 2022 m. sausio 1 d. laikotarpiui apskaičiuojama tokiu būdu:

1 000 + (114,25 – 105,65) &divide; 105,65 &times; 1 000 = 1 081,40

**2 pavyzdys**

Periodinio **sutarties atsiskaitymo parametrų** puslapyje nustatote vartotojo kainos indekso **skaičiavimo lauką** kaip Išankstinis **vartotojo kainos indeksas**.

2021 m. sausio 1 d. laikotarpio pirmoji perskyrimo suma apskaičiuojama tokiu būdu, remiantis pradine suma:

1 000 + (110,5 – 105,65) &divide; 105,65 &times; 1 000 = 1 045,91

Perskyrimo suma 2022 m. sausio 1 d. laikotarpiui apskaičiuojama tokiu būdu, remiantis pirmą perskyrimo suma:

1 045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1 045,91 = 1 081,40

> [!NOTE]
> Perskyrimo procese visada naudojama paskutinė CPI vertė, nepaisant indekso datos. Pavyzdžiui, jei perskyrimo data yra rugsėjį, tačiau vėliausia CPI vertė yra liepos mėn. indeksas. Neįvedėma jokių koregavimų po to, kai įvestas rugsėjo indeksas.

## <a name="prorated-escalation"></a>Perskyrimo projekcija

Jei perskyrimo įvyksta atsiskaitymo laikotarpio viduryje, suma yra perskirti. Pavyzdžiui, atsiskaitymo laikotarpis yra nuo 2020 m. rugpjūčio 1 d. iki 2021 m. liepos 31 d. 2019 m. rugsėjo 1 d. CPI data yra 244. 2020 m. rugsėjo 1 d. CPI data yra 250. Jei ankstesnis tarifas yra 1000, skaičiuojant laikotarpio sąskaitų pateikimo sumą naudojamos šios formulės:

* *CPI pakeitimai* = (250 – 244) &divide; 244 = 2,459%
* *Dabartinis* kursas = 1000 &times; 2,459% = 1024,59
* *Dienų skaičius pagal dabartinį kursą* = 2021 m. liepos 31 d. – 2020 m. rugsėjo 1 d. = 334
* *Ankstesnis* kursas = 1000
* *Dienų skaičius ankstesniu koeficientu* = 2020 m. rugpjūčio 31 d. – 2020 m. rugpjūčio 1 d. = 31
* *Bendras atsiskaitymo laikotarpio* dienų skaičius = 2021 m. liepos 31 d. – 2020 m. rugpjūčio 1 d. + 1 = 365
* *Atsiskaitymo suma šiuo* laikotarpiu = (1000 &times; 31 &divide; 365) + (1,024,59 &times; 334 &divide; 365) = 1,022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Perskyrimas, naudojantis CPI ir procentinę dalį

Perskyrimus galima atlikti naudojant CPI. CPI plius 3 procentų perskyrimas prasideda 2020 m. sausio 1 d. ir jo dažnis yra metinis.

- Suma, kuri yra išrašyta 2019 m. sausio 1 d., iki 2020 m. gruodžio 31 d., yra 4000.
- Bus perskirtas atsiskaitymo laikotarpis yra 2020 m. sausio 1 d. – 2020 m. gruodžio 31 d.
- 2018 m. gruodžio 1 d. CPI data yra 205,3. 2019 m. gruodžio 1 d. CPI data yra 219,6.

Jei ankstesnis tarifas yra 4000, šio laikotarpio sąskaitų suma apskaičiuojama tokiu būdu:

- *CPI pakeitimai* = (219,6 – 205,3) &divide; 205,3 = 6,965%
- *Dabartinis* kursas = (4 000 &times; 6,965 %) – 4000 = 278,60
- *Procentiniai* pokyčiai = (4 000 &times; 1,03) – 4000 = 120
- *Atsiskaitymo suma* = 4 000 + 278,6 + 120 = 4 398,6
