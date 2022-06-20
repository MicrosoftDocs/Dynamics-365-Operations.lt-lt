---
title: Atsiskaitymo grafikų nutraukimas
description: Šiame straipsnyje paaiškinama, kaip atleisti atsiskaitymo grafikus ir atsiskaitymo grafiko eilutes dalyje Abonemento sąskaitos išrašymas.
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
ms.openlocfilehash: 4fce23f3cf35ef8c388ce13fc422f268a2bd8e32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872563"
---
# <a name="terminate-billing-schedules"></a>Atsiskaitymo grafikų nutraukimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip atleisti atsiskaitymo grafikus ir atsiskaitymo grafiko eilutes dalyje Abonemento sąskaitos išrašymas. Kai išeisite iš atsiskaitymo grafiko, jo būsena turi būti **Aktyvus**. Jos būsena negali būti **Sulaikyta**. Taip pat, kai išeisite iš atsiskaitymo grafiko eilutės, jos būsena turi būti **Aktyvi**. Kai išeisite iš atsiskaitymo grafiko eilutės, mokėjimo grafiko antraštės dalis nebus paveikta.

Norėdami atleisti atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę, eikite į vieną iš šių vietų:

- Visų **/ aktyvių atsiskaitymo grafikų** sąrašo puslapis
- Konkretus atsiskaitymo grafikas puslapyje **Visi atsiskaitymo grafikai**
- Konkreti atsiskaitymo grafiko eilutė, pateikiama visų **atsiskaitymo grafikų** puslapyje

> [!NOTE]
> Jei norite vienu metu atleisti keletą atsiskaitymo grafikų, naudokite masinio atleidimo **apdorojimo** puslapį.

## <a name="terminate-a-billing-schedule-or-line"></a>Atleisti atsiskaitymo grafiką arba eilutę

Norėdami atleisti atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę, atlikite šiuos veiksmus.

1. Pasirinkite atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę, tada pasirinkite **Atleisti**. 
2. Nustatykite **atleidimo datą**, **atleidimo tipą** ir **priežasties kodo** laukus.
3. Nustatykite kredito **pasirinkties** lauką Išduoti **kreditą**.
4. Pasirinkite **Atleisti**.

Atsiskaitymo grafiko būsena keičiasi pagal pasirinktą atleidimo tipą. Jei kaip atleidimo **tipą pasirinkote** liko vekselio likutis, visų atsiskaitymo grafiko eilučių būsena yra Paskutinis **sąskaitos išrašymas**. Atsiskaitymo grafiko būsena lieka aktyvi **, kol** apdorojama paskutinė SF. Po to, kai paskutinį kartą apdorojama SF, būsena atnaujinama **į Nutraukta**. Jei kaip atleidimo **tipą pasirinkote** Koreguoti grafiką, atsiskaitymo grafiko būsena iš karto atnaujinama į **Atleista**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Atleisti atsiskaitymo grafiką arba eilutę ir taikyti grąžinimą

Norėdami atleisti atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę ir taikyti grąžinimą, atlikite šiuos veiksmus.

1. Pasirinkite atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę, tada pasirinkite **Atleisti**.
2. Nustatykite **atleidimo datą**, atleidimo **tipą**, priežasties **kodą** ir kredito **parinkties** laukus.
3. Pasirinkite **Atleisti nuo grąžinimo**. Rodomas **masinio atleidimo apdorojimo** puslapis ir jis filtruojamas, kad jame būtų rodomas atsiskaitymo grafikas.
4. Pasirinkite **Peržiūrėti,** norėdami peržiūrėti atsiskaitymo grafiko eilutes, tada pasirinkite **Procesas**.

Apdoroę kreditą atidarykite atsiskaitymo informacijos **puslapį, norėdami** peržiūrėti kreditą, kuris buvo taikomas atsiskaitymo grafikui. Jei kredito suma didesnė nei 0 (nulis), visos būsimos neįrašytos eilutės panaikinamos ir pakeičiamos atsiskaitymo informacijos eilutėmis, kuriose rodomos neigiamos kredito, kuris buvo taikomas atsiskaitymo grafikui, sumos.

### <a name="view-example"></a>Peržiūrėti pavyzdį

Atsiskaitymo grafike yra ši informacija:

- Pradžios data yra 2020 m. sausio 1 d.
- Pabaigos data yra 2020 m. gruodžio 31 d.
- Atsiskaitymo laikotarpio suma yra 100,00 per mėnesį.
- SF sukurtos atsiskaitymo laikotarpiams nuo sausio iki liepos mėn.
- Sutarties nutraukimo data yra 2020 m. birželio 15 d.

Kai kredito koregavimas apdorojamas, visi būsimi atsiskaitymo laikotarpiai (nuo rugpjūčio iki gruodžio) pašalinami iš **puslapio Rodyti atsiskaitymo** informaciją. Kredito koregavimo eilutė pridedama po liepos mėn. atsiskaitymo laikotarpio:

- Birželio 16 d. – liepos 31 d., jos kredito suma 150,00

Jei naudojama ne anksčiau kaip įplaukų priemonė, ne **anksčiau kaip įplaukų žurnalo įrašo įrašo** puslapis atnaujinamas atleidimo įrašu.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Atleisti atsiskaitymo grafiką arba eilutę netaikant kredito

Norėdami atleisti atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę netaikę kredito, atlikite šiuos veiksmus.

1. Pasirinkite atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę, tada pasirinkite **Atleisti**.
2. Nustatykite **atleidimo datos lauką**.
3. Nustatykite lauke **Atleidimo tipas** stat. **Nėra koregavimo**. Laukas **Kreditas automatiškai** nustatomas į Kredito **nėra**.
3. Nustatykite **lauką Priežasties** kodas.
4. Lauke Atleidimo **pastabos** įveskite reikiamas pastabas.
5. Pasirinkite **Atleisti**. 

Kai apdorojamas nutraukimas, pašalinamos visos informacijos apie sąskaitas eilutės po atleidimo datos. (Šiose eilutėse yra eilutė, kurioje yra atleidimo data.) Negalima sukurti atmestose eilutėse SF. Jei nutraukimas pašalinamas, visos atmestos eilutės vėl įtraukiamas į informacijos **apie** sąskaitas puslapį ir tampa galima išrašyti SF.

## <a name="fields"></a>Laukai

Informacijos **apie sąskaitas puslapyje** yra šie laukai.

| Laukas | Aprašymas |
|-------|-------------| 
| Atleidimo data | Pasirinkite datą, kada norite atleisti atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę. |
| Nutraukimo tipas | <p>Pasirinkite atleidimo tipą:</p><ul><li>**Koreguoti grafiką** – nutraukimo eilutės atsiskaitymo laikotarpius atleidimo datą ir pakeiskite eilutės būseną į Paskutinis **sąskaitos išrašymas**. Jei yra eilutės elemento atidėjimo grafikas, jis koreguojamas atšaukiant sumą, kuri neturi būti atpažinta. Jei sąskaitos pateikimo pradžios data yra po atleidimo datos, likę atsiskaitymo laikotarpiai pašalinami.</li><li>**Likęs** vekselis – pridėkite bet kokią likusią atsiskaitymo laikotarpio sumą į atleidimo laikotarpį ir pakeiskite eilutės būseną į Paskutinis **sąskaitos išrašymas**. Jei yra eilutės elemento atidėjimo grafikas, atidėjimo pabaigos data atnaujinama. Jei atsiskaitymo pradžios data yra po atleidimo datos, į atsiskaitymo laikotarpį įtraukiama bendroji visų likusių atsiskaitymo laikotarpių suma, o likę atsiskaitymo laikotarpiai pašalinami.</li><li>**Nėra koregavimo** – nutraukti nurodytos nutraukimo datos eilutės atsiskaitymo laikotarpius. Jokių koregavimų nėra. Kai pasirinktas šis atleidimo tipas, kredito pasirinkties **lauke** nustatyta **Reikšmė** Nėra kredito, o kasdienio **vartojimo prorate** laukas nustatytas kaip **Ne**. Abu šie laukai tampa tik skaitomi ir jų keisti negalima.</li></ul> |
| Kredito parinktis | <p>Pasirinkite, kaip kreditas bus taikomas, kai atmesite atsiskaitymo grafiko eilutę:</p><ul><li>**Kredito koregavimas** – kurti sąskaitų pateikimo grafiko kredito koregavimą, kai eilutė nutraukta. Kredito koregavimas rodomas būsimam atsiskaitymo grafiko atsiskaitymo laikotarpiui. Koregavimas taip pat automatiškai koreguoja kito atsiskaitymo laikotarpio SF sumą, kol kreditas baigiamas taikyti atsiskaitymo grafikui.</li><li>**Išdavimo** kreditas – kurti kredito pažymą, kai nutrauktas atsiskaitymo grafikas arba atsiskaitymo grafiko eilutė.</li><li>**Nėra kredito** – nekurti kredito koregavimo arba kredito pažymos, kai nutrauktas atsiskaitymo grafikas arba atsiskaitymo grafiko eilutė. Ši pasirinktis galima tik tada, kai naudojate koregavimo tipo **Nutraukimas** norint atleisti atsiskaitymo grafiką.</li></ul><p>Numatytoji pasirinktis yra periodinio **sutarties atsiskaitymo parametrų** puslapyje.</p> |
| Tikslinės paskirties šifras | Pasirinkite atleidimo priežasties kodą. |
| Priežasties aprašymas | Priežasties kodo aprašymas. |
| Nutraukimo pastabos | Įveskite bet kokias pastabas apie nutraukimą. |

<!--## Additional information-->
