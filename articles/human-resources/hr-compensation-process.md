---
title: Kompensavimo apdorojimas
description: Kompensavimo apdorojimas suteikia galimybę apskaičiuoti naujos bazinės kompensacijos sumas darbuotojams pagal kapitalo koregavimus, nuopelnų padidinimo tikslus ir našumą.
author: andreabichsel
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 01dd4223bfe4b24f484c1bc070d4c8aa376853fbf32d309b107333fcbdf87080
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732398"
---
# <a name="process-compensation"></a>Kompensavimo apdorojimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensavimo apdorojimas suteikia galimybę apskaičiuoti naujos bazinės kompensacijos sumas darbuotojams pagal kapitalo koregavimus, nuopelnų padidinimo tikslus ir našumą. Šiame straipsnyje apžvelgiamas pastoviosios atlyginimo dalies planų bazinio kompensacijos srauto apdorojimas neatsižvelgiant į darbuotojo našumą.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Naujų kompensacijos sumų ir biudžetų planavimas
Tam, kad suteiktumėte darbuotojams nuopelnų padidinimą, turite nustatyti savo padalinių fiksuotą didinimo biudžetą: Kompensacijų valdymas > Saitai > Nuopelnų didinimo tikslai. (Taip pat galite atidaryti šią formą per padalinį: Organizacija > Padaliniai.) Čia galite nurodyti, ar tam tikrai profesinei sąjungai ar vietai priklausantiems darbuotojams turėtų būti taikomas skirtingas padidinimo procentas. Laukai **Biudžetas** ir **Valiuta** yra informaciniai ir gali būti naudojami norint pažymėti biudžeto valiutos sumą.

## <a name="set-up-the-compensation-process"></a>Kompensavimo proceso nustatymas
Apdorojimo įvykis suteikia galimybę nurodyti kompensavimo apdorojimo parametrus. Tai apima datų laikotarpį, skirtą įvertinti siekiant nustatyti kompensacijos sumas ir datą, nuo kurios turėtų įsigalioti naujos kompensacijos sumos.

Pasirinktinai galite įtraukti fiksuoto užmokesčio paskirstymo samdos datą, jei jūsų pastoviosios atlyginimo dalies planuose naudojama procentinė samdos taisyklė. Tokių planų atveju kiekvienas, kuris buvo pasamdytas laikotarpiu nuo ciklo pradžios datos iki fiksuoto užmokesčio paskirstymo samdos datos, gaus 100 % jų apskaičiuoto nuopelnų ar bendrojo padidinimo. Asmenys, kurie buvo pasamdyti laikotarpiu nuo fiksuoto užmokesčio paskirstymo samdos datos iki ciklo pabaigos datos gaus jiems apskaičiuoto padidinimo dalį pagal tai, kiek dienų iš visų ciklo dienų jie buvo įdarbinti. Pavyzdžiui, jei ciklas trunka nuo sausio 1 d. iki gruodžio 31 d., o fiksuoto užmokesčio samdos paskirstymo data yra balandžio 1 d., kovo mėn. pasamdytas darbuotojas gaus visą apskaičiuotą padidinimą, tuo tarpu liepos 1 d. pasamdytas darbuotojas gaus maždaug pusė apskaičiuoto padidinimo.

Apdorojimo įvykio **Tam tikra** data yra naudojama tik apdorojant tam tikrus kintamosios atlyginimo dalies planus ir čia aptariama nebus. **Peržiūros terminas** yra terminas, skirstas pateikti visas rekomendacijas, kad naujas kompensacijos sumas būtų galima įkelti į darbuotojo įrašą. Peržiūros data yra tik informacinė.

Išsaugojus apdorojimo įvykio parametrus, spustelėkite mygtuką **Sąranka**, kad nurodytumėte planus, kuriuos norite įtraukti į šį proceso vykdymą, ir pastoviosios atlyginimo dalies veiksmus, kuriuos norite atlikti kiekviename plane.

Spustelėkite skirtuko **Planai** mygtuką **Pridėti**, kad prie apdorojimo įvykio pridėtumėte kompensavimo planą. Stulpeliai **Naudoti kitą svertą**, **Sverto faktorius** ir **Sverto aprašymas** naudojami tik kintamosios atlyginimo dalies planuose ir šiame straipsnyje neaptariami.

Įrašykite įrašą, tada spustelėkite skirtuko **Veiksmai** mygtuką **Pridėti**, kad pridėtumėte pastoviosios atlyginimo dalies veiksmus į pasirinktą planą. Naudokite parinktį **Įjungti rekomendaciją**, norėdami įvesti sumą, kitą nei apskaičiuotas veiksmo siūlomas padidinimas. Norėdami veiksmą skaičiuoti pagal ankstesnio veiksmo rezultatus, kad būtų galima susieti keletą kompensavimo veiksmų, pažymėkite parinktį **Naudoti ankstesnius rezultatus**; pastoviosios atlyginimo dalies veiksmai yra kompensavimo logikos tipai, kuriems galite suteikti aprašomuosius pavadinimus. Kategorijų ir intervalų planų atveju, galite įtraukti tik pastoviosios atlyginimo dalies veiksmus, kurie tipai nurodyti toliau.

| Pastoviosios atlyginimo dalies veiksmo tipas | Funkcijos                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kapitalas                        | Kapitalo veiksmai palygins darbuotojo užmokesčio tarifą ciklo pabaigos dieną su darbuotojo užduotyje nurodyto lygio žemiausiu atskaitos tašku. Jei darbuotojo užmokesčio tarifas yra mažesnis už minimalų atskaitos tašką, bus apskaičiuotas padidinimas, kurio reikia, kad darbuotojas pasiektų minimalų diapazono tašką.                                                                                |
| Nuopelnas                         | Nuopelnų veiksmai padidinimą apskaičiuos pagal darbuotojo užmokesčio tarifą ciklo pabaigos dieną ir padidinimo procentą, nurodytą darbuotojo padalinio, profesinės sąjungos ir vietos fiksuoto padidinimo biudžete.                                                                                                                                                                                         |
| Bendra                       | Bendrieji veiksmai padidinimą apskaičiuos pagal procentą arba paskirs darbuotojams standartinę sumą. Tai nustatoma remiantis skirtuko **Bendra** dalies **Pastovioji atlyginimo dalis** parametrais.                                                                                                                                                                                                                        |
| Skatinimas                     | Paaukštinimo pareigose veiksmai pateikia įvardytą vietą, kurioje galite skirti padidinimą, todėl būtinai pažymėkite parinktį **Įgalinti rekomendaciją**, kad galėtumėte įvesti rekomendaciją darbuotojams, kurie bus paaukštinti pareigose.  Prie darbuotojų be rekomenduojamo padidinimo pastoviosios atlyginimo dalies įrašo nebus pridėtas veiksmas **Paaukštinimas pareigose**.                                                                       |
| Kitokio lygio pakeitimas            | Ankstesniame pavyzdyje **Pažeminimas pareigose** yra mūsų **pastoviosios atlyginimo dalies** veiksmo, kurio tipas **Kitokio lygio pakeitimas**, pavadinimas. Taip sugeneruojamas 0 (nulinis) siūlomas padidinimas, tad galite įvesti rekomendaciją sumą ir koreguoti darbuotojo užmokesčio tarifą. (Būtinai pažymėkite parinktį **Įjungti rekomendaciją**.) Prie rekomendacijų neturinčių darbuotojų pastoviosios atlyginimo dalies įrašų šis veiksmas pridėtas nebus. |

Į veiksmo planą galite įtraukti tik **pastoviosios atlyginimo dalies** veiksmus, kurių tipas Veiksmas.

| Pastoviosios atlyginimo dalies veiksmo tipas | Funkcijos                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Žingsnis                           | Skirtuke Bendra nurodykite ar šis veiksmas Žingsnis turėtų perkelti darbuotojus į priekį 0 žingsnių, 1 žingsniu arba dviem žingniais.                                                                                  |
|                                | **0 žingsnių** – darbuotojui bus taikomas žingsnio, kuriame šiuo metu yra, užmokesčio tarifas.                                                                                                                      |
|                                | **1 žingsnis** – sistema patikrins, ar darbuotojas jau pasiekė paskutinį savo lygio atskaitos tašką.                                                                                             |
|                                | **2 žingsniai** – sistema perkels darbuotoją dviem žingsniais pirmyn jo dabartiniame lygyje. Sistema gali perkelti darbuotoją vienu arba nuliu žingsnių, tiktai jei jis pasiekia savo lygio paskutinį atskaitos tašką. |

## <a name="run-the-compensation-process"></a>Vykdyti kompensacijos procesą
Nustačius apdorojimo įvykį ir nustačius reikalingus datos laukus, planus ir veiksmus, puslapyje **Proceso įvykis** galite spustelėti **Vykdyti procesą**. Tai atlikus bus atidarytas dialogo langas **Vykdyti kompensavimo proceso įvykius**. Šiame dialogo lange galite spustelėti parinktį **Rodyti apdorojimo rezultatus** ir peržiūrėti kaip buvo apskaičiuotos kiekvieno darbuotojo kompensacijos sumos. Spustelėjus **Gerai** bus vykdomas kompensavimo procesas visų darbuotojų, kuriems taikomi pasirinkti kompensavimo planai ciklo pabaigos dieną.

## <a name="view-the-process-results"></a>Proceso rezultatų peržiūra
Norėdami peržiūrėti proceso rezultatus, atidarykite puslapį **Proceso rezultatai**. Kiekvieną kartą vykdant apdorojimo įvykį, bus sukurtas naujas kompensavimo įvykis. Tokiu būdu galite vykdyti bandomuosius procesus, atlikti koregavimus ir vykdyti kompensavimo įvykį keletą kartų, kad peržiūrėtumėte, kokią įtaką įvairūs pakeitimai turi darbuotojo kompensacijai.

Puslapyje **Proceso rezultatai** pateikiama informacija apie proceso vykdymą, įskaitant vykdymo laiką, vartotojus, kurie vykdė procesą, ir ar proceso vykdymo metu neįvyko klaidų. Taip pat galite pažymėti parinktį **Užrakinta**, kad išjungtumėte mygtuką **Įkelti kompensaciją** ir kad niekas negalėtų įkelti kompensavimo įvykių į darbuotojo įrašus. Spustelėjus mygtuką **Darbuotojų rezultatai** bus rodomas darbuotojų, įtrauktų į vykdymą, sąrašas.

Parinktyje **Darbuotojo rezultatai** rodoma informacija apie patį procesą, taip pat proceso metu atlikti kompensacijos veiksmai. Skyriuje **Pastovioji atlyginimo dalis** bus pateiktas kiekvieno veiksmo, įtraukto į kompensavimo plano apdorojimo įvykį, įrašas. Stulpeliuose **Dabartinis siūlymas** ir **Rekomendacija** bus rodoma daugiau informacijos apie veiksmą, pasirinktą skyriuje **Pastovioji atlyginimo dalis**. Jei veiksme buvo pažymėta **Įjungti rekomendacijas**, laukus Rekomendacija bus galima redaguoti. Tai leis jums rankiniu būdu koreguoti darbuotojo sumas. Pastaba: jei pažymėjote apdorojimo įvykio veiksmo parinktį **Naudoti ankstesnius rezultatus**, turite neautomatiškai atnaujinti bet kokių priklausomųjų veiksmų sumas.

Peržiūrėję darbuotojo kompensacijos sumas ir atlikę rekomenduojamų reikšmių koregavimus, galite pakeisti **Būseną** eilutėje **Darbuotojo įvykis**, kad nurodytumėte, ar įvykis buvo patvirtintas ar turėtų būti ignoruojamas. Pasirinktinai galite ištrinti darbuotojo rekomendacijos pakeitimus, spustelėdami mygtuką **Perskaičiuoti**. Esamo darbuotojo įvykio būsena bus pažymėta kaip Nepaisyti, ir bus sukurtas naujas darbuotojo įvykis su perskaičiuotomis reikšmėmis.

## <a name="loading-approved-compensation-changes"></a>Patvirtintų kompensacijos pakeitimų įkėlimas
Kai vieno ar daugiau darbuotojų įvykių būsena buvo atnaujinta į Patvirtinta, jie gali būti įkelti į darbuotojų pastoviųjų atlyginimo dalių įrašus. Tai galite padaryti po vieną pasirinkdami kiekvieną darbuotojo įvykį ir spustelėdami mygtuką **Įkelti darbuotojo kompensaciją**, esantį puslapyje **Darbuotojo rezultatai**, arba spustelėdami **Įkelti kompensaciją** puslapyje **Proceso rezultatai**, kad įkeltumėte visus patvirtintus darbuotojo įvykius vienu metu.

Dialogo lange **Įkelti kompensaciją** spustelėjus **Gerai**, į puslapį **Darbuotojo pastovioji atlyginimo dalis** bus pridėtos nenulinės kompensacijos veiksmo eilutės.


[!INCLUDE[footer-include](../includes/footer-banner.md)]