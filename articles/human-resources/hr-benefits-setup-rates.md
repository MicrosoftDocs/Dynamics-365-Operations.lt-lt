---
title: Tarifų konfigūravimas
description: Tarifai programoje „Microsoft Dynamics 365 Human Resources“ nustato, kiek darbdaviai ir darbuotojai prisideda prie išmokos.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37fb24bdda1d49291b88c6728e11aecf9863cc66
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324824"
---
# <a name="configure-rates"></a>Tarifų konfigūravimas

Tarifai nustato, kiek darbdaviai ir darbuotojai prisideda prie išmokos. Reikšmė gali būti tiek suma, tiek lanksčiųjų kreditų skaičius, atsižvelgiant į jūsų konfigūraciją.

Naudokite tarifus, kad nustatytumėte, kiek darbuotojai ir darbdaviai moka už kiekvieną išmoką, priklausomai nuo keleto veiksnių. Padengimo tarifai priklauso nuo datos, todėl galite turėti archyvinį tarifų įrašą. 

## <a name="set-up-rates"></a>Tarifų nustatymas

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tarifai**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Tarifas** | Unikalus pavadinimas, nurodantis išmokos tarifą. |
   | **Aprašas** | Išmokos tarifo aprašas. |
   | **Galioja** | Data, nuo kurios įsigalioja tarifas. Dabartinė sistemos data yra numatytoji reikšmė. Ši data turėtų būti jūsų išmokų laikotarpiu arba prieš jį. Patariame nustatyti šią datą į išmokų plano datą. |
   | **Galiojimas** | Tarifo pabaigos data. Data 2154-12-31 (kuri reiškia niekada) yra numatytoji reikšmė. |
   | **Naudoti pakopas** |  Naudokite šį lauką, jei turite logiką, kuri turi būti naudojama tarifui nustatyti. Pavyzdžiui, jei tarifas turi didėti pagal amžių, pasirinkite reikšmę čia. Pasirinkite **Viena pakopa** vienos pakopos išmokų tarifui arba **Dviguba pakopa** dviejų pakopų išmokų tarifui. Dvigubos pakopos pavyzdys yra pakopa, kuri pagrįsta lytimi ir amžiumi. Pasirinkę reikšmę, pasirinkite **Veiksmai** ir **Pakopos tarifai**. Jei turite fiksuotą tarifą, kuris nesikeičia, palikite šį lauką tuščią. |
   | **Mokėjimo dažnumas** | Nurodykite, kaip dažnai išmokos priedų tarifas turėtų būti mokamas išmokų teikėjui. Toliau šiame straipsnyje aprašomi kursai, kuriuos įvedate puslapyje, bus pagrįsti čia nurodytų mokėjimų dažnumu. Pavyzdžiui, jei šiame lauke įvesite **Kas mėnesį**, o darbuotojo tarifą įvesite **„$100”**, laikoma, kad išmoka darbuotojui kainuos $100 per mėnesį. Tačiau darbuotojui gali būti mokama du kartus per mėnesį, atsižvelgiant į išmokų mokėjimo dažnumą, kuris nustatytas darbuotojo įraše. Tokiu atveju, kai darbuotojas prisijungia prie **darbuotojo savitarnos**, jo mokėtina suma bus $50, nes darbuotojo savitarnoje rodomas tarifas yra pagrįstas **Darbuotojo savitarna** darbuotojo mokėjimo dažnumu. |
   | **Mokėjimo dažnumo apvalinimas** | Tarifo apvalinimo metodai: Standartinis, Sumažintas, Įprastas, Į mažesnę pusę ir Į didesnę pusę. </br></br><ul><li>**Standartinis** – Visada suapvalina į didesnę pusę. Pavyzdžiui, 10,611 bus suapvalinta iki 10,62. -10,231 bus suapvalinta iki -10,23. </li><li>**Sumažintas** – Visada suapvalina į mažesnę pusę. Pavyzdžiui, 10,619 bus suapvalinta iki 10,61. -10,231 bus suapvalinta iki -10,24. </li><li>**Įprastas** – dešimtainės vertės, kurios baigiasi 5 arba didesniu skaičiumi, bus suapvalintos į didesnę pusę. Dešimtainės vertės, kurios baigiasi 4 arba mažesniu skaičiumi, bus suapvalintos į mažesnę pusę. Pavyzdžiui, 10,615 bus suapvalinta iki 10,62. -10,235 bus suapvalinta iki -10,24. 10,614 bus suapvalinta iki 10,61. -10,234 bus suapvalinta iki -10,23. </li><li>**Į mažesnę pusę** – suapvalina link nulio. Pavyzdžiui, 10,619 bus suapvalinta iki 10,61. -10,231 bus suapvalinta iki -10,23. </li><li>**Į didesnę pusę** – suapvalina toliau nuo nulio. Pavyzdžiui, 10,619 bus suapvalinta iki 10,62. -10,231 bus suapvalinta iki -10,24. |
   | **Nerūkančio darbuotojo suma** | Mokesčio suma, kurią išmokos teikėjas taiko nerūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Nerūkančio darbdavio suma** | Mokesčio suma, kurią išmokos teikėjas taiko nerūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui, ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Rūkančio darbuotojo suma** | Mokesčio suma, kurią išmokos teikėjas taiko rūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Rūkančio darbdavio suma** | Mokesčio suma, kurią išmokos teikėjas taiko rūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Administracinė suma** | Administracinė suma, mokama trečiosios šalies administratoriui. Tai yra suma, kurią darbdavys moka trečiosios šalies administratoriui, ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Lanksčiųjų kreditų tarifas** | Lanksčiųjų kreditų, kuriuos kainuoja išmoka, skaičius. Taikoma tik išmokų planų, susietų su lanksčiųjų kreditų programomis, tarifams. Jei naudojate pakopų tarifus, lanksčiųjų kreditų tarifas nustatomas einant į „Veiksmai“ > „Pakopų tarifai“. |
   | **Keitimo įsigaliojimo data** | Tarifo pasikeitimo įsigaliojimo data. Sistema automatiškai pakeis išmokų tarifą ir atnaujins visus su šiuo tarifu susijusius išmokų planus, jeigu jūs vykdote tarifo keitimo naujinimo apdorojimą. Nustatykite šią datą tik tuo atveju, jei norite, kad sistema automatiškai naujintų darbuotojų išmokų planus pagal šį tarifą. Paprastai tai taikoma tik automatiniam būsimų tarifų keitimų apdorojimui. Pakeitimo **įsigaliojimo data turi** atitikti išmokos tarifo įsigaliojimo ir galiojimo pabaigos datas. |
   | **Tarifas pakeistas** | Žymimasis langelis **Tarifo pakeitimas atliktas** bus pasirenkamas automatiškai, kai išmokų tarifo pakeitimai bus užbaigti apdorojus tarifo pakeitimo atnaujinimą. |

4. Norėdami sekti ir tvarkyti išmokų tarifo sąrankos keitimus, pasirinkite **Veiksmai**, tada pasirinkite **Tvarkyti versijas**.

5. Pasirinkite **Įrašyti**. 

## <a name="set-up-tier-rates"></a>Nustatyti pakopų tarifus

Galite naudoti pakopų tarifus tarifų sąrankoje, jeigu tarifas skiriasi priklausomai nuo įvairių veiksnių. Pavyzdžiui, galite konfigūruoti pakopų tarifus, ir jeigu jūsų amžius yra iki 34,99 m., nerūkančiojo suma bus lygi 2. Jei jūsų amžius yra iki 39,99, nerūkančiojo suma bus lygi 3.

Taip pat galite naudoti dvigubas pakopas. Jeigu formoje **Tarifų sąranka** pasirinksite **Dviguba pakopa**, skirta reikšmei **Naudoti pakopas**, galėsite apibrėžti tarifus pagal dvi dimensijas. Pavyzdžiui, galite konfigūruoti dvigubos pakopos sistemą, ir jeigu esate vyras ir jūsų amžius yra iki 34,99 m., nerūkančiojo suma bus lygi 2. Jeigu esate vyras ir jūsų amžius yra iki 39,99, nerūkančiojo suma bus lygi 3. Jeigu esate moteris ir jūsų amžius yra iki 34,99, nerūkančiojo suma bus lygi 1,8. Jeigu esate moteris ir jūsų amžius yra iki 39,99, nerūkančiojo suma bus lygi 2,8.

> [!IMPORTANT]
> Darbuotojo įrašo dalyje **Asmeninė informacija** yra skirta nurodyti, ar darbuotojas yra rūkantis. Jei darbuotojas registruojamas kaip rūkantis, bus naudojamas rūkančiojo tarifas. (Rūkančių darbuotojų nustatymas niekada nerodomas darbuotojui.)
   
1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tarifai**.

2. Pasirinkite vieną ar daugiau tarifų iš sąrašo, pasirinkite **Veiksmai**, tada pasirinkite **Pakopų tarifai**.

3. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | aprašymas |
   | --- | --- | 
   | **Aprašas** | **Aprašas** lauko vertė pritaikyta iš aprašo, esančio kurso nustatymo įraše. Taip yra lengviau nustatyti, su kokia tarifo sąranka susieti pakopų tarifai. |
   | **Pakopos kodas** | Pakopų kodo pasirinkimas. Pakopų kodai apibrėžiami **pakopų kodų** puslapyje. Sistema automatiškai rodys pakopų kodo aprašą kairėje esančiame tinklelyje. |
   | **Pakopos tipas** | Nurodo, kuris laukas turi būti naudojamas kaip pakopų tarifo apskaičiavimo proceso atrankos kriterijus. Pvz.:</br></br><ul><li>Jei naudojamas **Amžius**, sistema naudos darbuotojo gimimo datą išmokos tarifo skaičiavimo metu.</li><li>Jei naudojamas **Atlyginimas**, sistema naudos darbuotojo metinį išmokų atlyginimą išmokų tarifo skaičiavimo metu.</li><li>Jei naudojamas **Darbo tipas**, sistema naudoja darbuotojo dabartinį aktyvų pareigų įrašą, kad nustatytų darbo tipą pagal su pareigomis susietą darbo įrašą.</li></ul></br></br>Pakopų tipai: **Amžius**, **Atlyginimas**, **Faktinis**, **Lytis**, **Pilno etato ekvivalentas**, **Darbo tipas**, **Kompensacijų regionas** ir **Lygis**. | 
   | **Lygis** | Vertė, kuri turi būti naudojama kartu su pakopų tipu išmokų tarifo apskaičiavimo proceso metu. Pavyzdys:</br></br><ul><li>Jei pakopos tipas yra **Amžius**, bus naudojama amžiaus vertė.</li><li>Jei pakopos tipas yra **Atlyginimas** bus naudojamas atlyginimo suma.</li><li> Jei pakopos tipas yra **Darbo tipas**, bus naudojamas darbo tipas.</li></ul></br></br>Kai pakopos tipas yra **Amžius** arba **Atlyginimas**, **lauko Lygis** vertė nurodo apatinę pakopos ribą. Jei pakopos tipas yra **Darbo tipas**, sistema naudoja tikslaus atitikimo metodą pakopos tarifo atrinkimo metu. |
   | **Skaičiavimo tipas** | Nurodo, kaip apskaičiavimo sumos lauke naudoti sumą ir kokį matematinį skaičiavimą atlikti, jei reikia. Jei skaičiavimo tipas yra fiksuota suma, sistema naudoja tokius sumos laukus, kokie yra. Jei skaičiavimo tipas yra už atlyginimo ar padengimo sumą $, sistema matematiniuose skaičiavimuose naudoja skaičiavimo sumą ir skaičiavimo kryptį.</br></br>Jei skaičiavimo tipas yra už atlyginimo sumą $, sistema naudos šią matematinę lygtį:</br></br>metinis išmokų atlyginimas, padalytas iš skaičiavimo sumos (suapvalintos į didžiąją arba mažąją pusę), padaugintos iš rūkančiam arba nerūkančiam darbuotojui ar darbdaviui skirtos sumos.</br></br>Jei skaičiavimo tipas yra už atlyginimo sumą $, sistema naudos šią matematinę lygtį:</br></br>padengimo suma, padalyta iš skaičiavimo sumos (suapvalintos į didžiąją arba mažąją pusę), padaugintos iš rūkančiam arba nerūkančiam darbuotojui ar darbdaviui skirtos sumos.</br></br>Abiejuose skaičiavimuose skaičiavimo kryptis naudojama siekiant nustatyti, ar metinį išmokų atlyginimą arba padengimo sumą, padalytą iš skaičiavimo sumos, suapvalinti į didžiąją ar mažąją pusę. |
   | **Skaičiavimo suma** | Suma, kurią reikia naudoti išmokos tarifo apskaičiavimo procese. Ši suma bus daliklis matematiškai apskaičiuojant pakopos tarifą. |
   | **Skaičiavimo kryptis** | Kryptis, kuria apskaičiuoti rezultato suma turėtų būti suapvalinta. Sistema palaiko tris skaičiavimo kryptis: tuščias (tikslus metodas), **Didinti** ir **Sumažinti**.</br></br><ul><li>Jei tuščia, sistema naudos tikslų atlyginimo / padengimo sumos apskaičiavimą, padalytą iš skaičiavimo sumos. Jei ši vertė turi trupmeną, sistema tai naudos skaičiuodama.</li><li>Jei pasirenkama **Didinti**, sistema padidins atlyginimo / padengimo sumos matematinį apskaičiavimą, padalintą iš skaičiavimo sumos iki kito sveikojo skaičiaus (vadinasi, 12,25 padidės iki 13).</li><li>Jei pasirenkama **Mažinti**, sistema sumažins atlyginimo / padengimo sumos matematinį apskaičiavimą, padalintą iš skaičiavimo sumos į dabartinį sveikąjį skaičių (vadinasi, 12,25 sumažės iki 12).</li></ul> |
   | **Nerūkančio darbuotojo suma** | Mokesčio suma, kurią išmokos teikėjas taiko nerūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui, ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Nerūkančio darbdavio suma** | Mokesčio suma, kurią išmokos teikėjas taiko nerūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui, ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Rūkančio darbuotojo suma** | Mokesčio suma, kurią išmokos teikėjas taiko nerūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui, ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Rūkančio darbdavio suma** | Mokesčio suma, kurią išmokos teikėjas taiko nerūkančiam darbuotojui. Tai yra suma, kurią darbdavys moka išmokos teikėjui, ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Administracinė suma** | Administracinė suma, mokama trečiosios šalies administratoriui. Tai yra suma, kurią darbdavys moka trečiosios šalies administratoriui, ir kuri turi būti grindžiama mokėjimo dažnumu, skirtu tarifui nustatyti. |
   | **Lanksčiųjų kreditų nerūkančiojo tarifas** | Lanksčiųjų kreditų, kuriuos kainuoja išmoka, skaičius, remiantis skaičiavimu, nustatytu nerūkančiųjų pakopos lygyje. Pavyzdžiui, jei skaičiavimo tipas yra **Už padengimo sumą $**, skaičiavimo suma yra 10 000, nerūkantiesiems taikomas lanksčiųjų kreditų tarifas yra 6 (tai reiškia, kad jeigu nerūkantis darbuotojas pasirenka 10 000 $ padengimą, jis kainuos 6 lanksčiuosius kreditus). Pasirinkus 20 000 $ padengimą, jis kainuos 12 lanksčiųjų kreditų ir t. t. |
   | **Lanksčiųjų kreditų tarifas, taikomas rūkantiesiems** | Lanksčiųjų kreditų, kuriuos kainuoja išmoka, skaičius, remiantis skaičiavimu, nustatytu rūkančiųjų pakopos lygyje. |

5. Pasirinkite **Įrašyti**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
