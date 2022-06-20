---
title: Turto nuomos ataskaitos
description: Šiame straipsnyje pateikiamos ir trumpai aprašomos ataskaitos, kurias galima naudoti turto dalyje.
author: moaamer
ms.date: 04/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a6e6eb851b9b2dce7259a5355326dd594a940b8c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856718"
---
# <a name="asset-leasing-reports"></a>Turto nuomos ataskaitos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos ir trumpai aprašomos ataskaitos, kurias galima naudoti turto dalyje. (Dauguma ataskaitų rodomos, atliekant šiuos veiksmus ar veiksmus, kurie yra labai panašūs, kaip pažymėta). 

- Norėdami peržiūrėti daugumą modulio Turto nuoma ataskaitų, eikite į **Turto nuoma > Užklausos ir ataskaitos > Nuomos ataskaitos** ir pasirinkite ataskaitą, kurią norite peržiūrėti. Ataskaitoms, kurioms reikalingas kitoks parinkimo kelias, atidaryti skirti veiksmai yra įtraukiami tos ataskaitos aprašą. 
- Kai pasirenkate spausdintiną ataskaitą, atidaromas parametrų puslapis, kuriame galima filtruoti į ataskaitą įtrauktą informaciją. Įveskite filtro kriterijus, tada pasirinkite **Gerai** ataskaitai generuoti. Sugeneruotoje ataskaitoje bus rodoma informacija, patenkanti į jūsų nurodytus filtrus.

## <a name="asset-movement"></a>Turto perkėlimas
Ataskaita Turto dinamika naudojama kaip užregistruotų keitimų taikymo ataskaita, skirta kiekvienos nuomos naudojimo teise valdomo turto balansams. Ši ataskaita leidžia peržiūrėti turto nuomos operacijas per nurodytą laikotarpį. Ataskaitoje yra tolesni laukai. 

|     Ataskaitos laukai                  |     aprašymas                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Pradžios data              |     Anksčiausios nuomos versijos pradžios data.                     |   
|     Nuomos terminas                     |     Dabartinė nuomos laikotarpio versija.                            |
|     Trumpalaikė nuoma               |     Jei nuoma klasifikuojama kaip trumpalaikė, rodoma **Taip**.         |
|     Mažos vertės turto nuoma                |     Jei nuoma klasifikuojama kaip mažos vertės turto nuoma, rodoma **Taip**.          |
|     Pradinis naudojimo teise valdomas turtas     |     Pradinio pripažinimo žurnalo įraše nurodyta pradinė naudojimo teise valdomo turto vertė.      |
|     Pradinis balansas              |     Naudojimo teise valdomo turto balansinė vertė nuo **pradžios datos**.                         |
|     Laikotarpio nusidėvėjimo išlaidos    |     Nusidėvėjimo išlaidų suma, fiksuojama apibrėžtame ataskaitos datų intervale.        |
|     Sukauptas nusidėvėjimas       |     Sukaupto nusidėvėjimo suma nuo **pradžios datos**.                               |
|     Nuvertėjimas                     |     Turto pablogėjimo suma apibrėžtame ataskaitos datų intervale.               |
|     Pakeitimai                  |     Naudojimo teise valdomo turto koregavimo suma tarp datos parametrų.                            |
|     Balansinė vertė                 |     Naudojimo teise valdomo turto balansinė vertė, kuri yra grynoji sukaupto nusidėvėjimo suma **pabaigos dieną**.    |

## <a name="differences-report"></a>Skirtumų ataskaita
Ataskaitoje Skirtumai rodomi skirtumai tarp informacijos, kuri yra įkeliama į nuomos importo sistemą, ir informacijos, kuri šiuo metu yra sistemoje. Tai leidžia palyginti, kas buvo pakoreguota, atnaujinta ar įtraukta naudojant nuomos importo sistemą.  

Ataskaitos reikšmės priklauso nuo pasirinktos nuomos. Ataskaitoje bus rodomi tik tie laukai, kurie skiriasi nuo to, kas šiuo metu yra sistemoje ir kas yra išdėstymo lentelėse. Senoji reikšmė yra tai, kas šiuo metu yra sistemoje, arba tai, kas sistemoje buvo anksčiau, atsižvelgiant į tai, ar buvo vykdomas importavimo procesas. Naujoji reikšmė yra tai, kas yra išdėstymo lentelėje ir kas pakeis senąją reikšmę.

## <a name="five-years-undiscounted-payment-forecast"></a>Penkerių metų nediskontuotų mokėjimų prognozė
Ataskaitoje Penkerių metų nediskontuotų mokėjimų prognozė rodomi planuojami nediskontuoti nuomos mokesčiai, kurie turi būti sumokėti kitų penkerių metų laikotarpiu nuo datos, nurodytos ataskaitos parametruose. Ataskaitoje yra tolesni laukai. 

|     Ataskaitos laukai         |     aprašymas                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Nuomos aprašas     |     Nuomos aprašas iš nuomos antraštės.                                                      |
|     Nuomos ID              |     Unikalus nuomos ID.                                                                              |
|     Rezervuoti                  |     Nuomos knyga, susijusi su knygos ID.                                                         |
|     Klasifikacija        |     Nuomos klasifikacija.                                                                  |
|     Registravimo sluoksnis         |     Sluoksnis, kuriame ši nuoma registruojama.                                                         |
|     Valiuta              |     Nuomos valiuta.                                                                        |
|     Dabartiniai               |     Visų nuomos mokesčių, mokėtinų per ateinančius 12 mėnesių nuo ataskaitos datos, suma.          |
|     13–24 mėn.          |     Visų nuomos mokesčių, mokėtinų 13–24 mėn. nuo ataskaitos datos, suma.           |
|     25–36 mėn.          |     Visų nuomos mokesčių, mokėtinų 25–36 mėn. nuo ataskaitos datos, suma.           |
|     37–48 mėn.          |     Visų nuomos mokesčių, mokėtinų 37–48 mėn. nuo ataskaitos datos, suma.           |
|     49–60 mėn.          |     Visų nuomos mokesčių, mokėtinų 49–60 mėn. nuo ataskaitos datos, suma.           |
|     Po to            |     Visų nuomos mokesčių, mokėtinų 61 mėn. nuo ataskaitos datos arba vėliau, suma.              |

## <a name="gaap-cash-flows-report"></a>GAAP grynųjų pinigų srautų ataskaita
GAAP atskleidimo ataskaita atitinka JAV GAAP atskleidimo reikalavimą, nurodytą 842-20-50-4(g)(1). Norėdami peržiūrėti šią ataskaitą, eikite į **Turto nuoma > Užklausos ir ataskaitos > Atskleidimas > GAAP – grynųjų pinigų srautai**. 

|     Ataskaitos laukai                                 |     Aprašymas                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Nuo datos <br> Iki datos                        |     Nurodo datų intervalą, naudojamą į ataskaitą įtraukiamai informacijai riboti.      |
|     Juridinis subjektas                                  |     Juridinis subjektas, susijęs su nuoma.                                      |
|     Nuomos tipas                                    |     Nuomos klasifikacija – finansinė arba veiklos.           |
|     Nuomos ID                                      |     Unikalus nuomos ID.                                                      |
|     Nuomos aprašas                             |     Nuomos aprašas iš nuomos antraštės.                              |
|     Nuomos knyga                                    |     Nuomos knyga, į kurią nurodo eilutė.                        |
|     Registravimo sluoksnis                                 |     Kiekviena ilgalaikiam turtui priskirta knyga nustatoma konkrečiame registravimo sluoksnyje, turinčiame bendrą nusidėvėjimo tikslą.                          |
|     Nuomos grupė                                   |     Grupė, su kuria susieta nuoma.                                     |
|     Valiuta                                      |     Naudotos operacijų valiutos santrumpa. Visose ataskaitose operacijų valiuta bus konvertuota į ataskaitų valiutą.                      |
|     Finansinė nuoma – veiklos grynųjų pinigų srautai         |     Visų užregistruotų kintamųjų mokėjimų ir visų palūkanų mokėjimų, užregistruotų iš amortizacijos grafiko tarp datos parametrų, suma.        |
|     Finansinė nuoma – finansinių grynųjų pinigų srautai           |     Visų pagrindinių mokėjimų iš amortizacijos grafiko tarp datos parametrų suma.       |
|     Veiklos nuoma – veiklos grynųjų pinigų srautai       |     Visų užregistruotų nuomos mokesčių ir užregistruotų kintamųjų mokėjimų tarp datos parametrų suma.            |

## <a name="lease-balances-forecast"></a>Nuomos balansų prognozė
Prognozėje Nuomos balansai pateikiama informacija tiesiai iš įsipareigojimo amortizacijos grafiko ir turto nusidėvėjimo grafiko. Ataskaitoje pateikiamos prognozuojamos nuomos įsipareigojimo sumos ir naudojimo teise valdomas turtas per tam tikrą laikotarpį, įskaitant numatomas šios nuomos išlaidas. Ataskaitoje yra tolesni laukai.

|     Ataskaitos laukai                 |     aprašymas                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Pradinis balansas             |     Pradžios likutis nuomos amortizacijos grafike už laikotarpį, apimantį ataskaitos pradžios datą.            |
|     Pradinis pripažinimas           |     Jei nuomos pradžios data patenka į nurodytą ataskaitos datų intervalą, šiame stulpelyje bus rodoma pradinio pripažinimo žurnalo įrašo įsipareigojimo sąskaitos reikšmė.      |
|     Mokėjimai                      |     Nuomos mokėjimų, kurie patenka į nurodytą ataskaitos datų intervalą, suma.                               |
|     Pomėgiai                      |     Nuomos palūkanų sąnaudų, kurios patenka į nurodytą ataskaitos datų intervalą, suma.                    |
|     Pabaigos likutis                |     Nuomos įsipareigojimų balansas **pabaigos dieną**.                                                             |
|     Trumpalaikis įsipareigojimas          |     Trumpalaikio įsipareigojimo suma nuomos amortizacijos grafike **pabaigos dieną**.                           |
|     Ilgalaikis įsipareigojimas           |     Ilgalaikio įsipareigojimo suma nuomos amortizacijos grafike **pabaigos dieną**.                            |
|     Pradinė balansinė vertė      |     Pradinė balansinė vertė nuomojamo turto nusidėvėjimo grafike už laikotarpį, apimantį ataskaitos pradžios datą      |
|     Pradinis pripažinimas           |     Jei nuomos pradžios data patenka tarp ataskaitos datų parametrų, šiame stulpelyje bus rodoma pradinio pripažinimo žurnalo įrašo turto sąskaitos reikšmė.            |
|     Likvidavimo išlaidos          |     Nuomos nusidėvėjimo išlaidų, kurios patenka į nurodytą ataskaitos datų intervalą, suma.                  |
|     Pabaigos likutis                |     Nuomos turto balansas **pabaigos dieną**.                                                              |
|     Kapitalo koregavimas             |     Pradžios balansas, iš jo atėmus pradžios balansinę vertę.                                                             |

## <a name="lease-commencements-report"></a>Ataskaita Nuomos pradžia
Ataskaitoje Nuomos pradžia rodomos visos nuomos, prasidėjusios nurodytame datų intervale, įskaitant pradinius įsipareigojimo ir naudojimo teise valdomo turto balansus. Ataskaitoje yra tolesni laukai. 

|     Ataskaitos laukai                 |     aprašymas                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Pradžios data             |     Pradinio pripažinimo žurnalo įrašo, kuris buvo užregistruotas tai nuomos versijai, data.         |
|     Pradinio įsipareigojimo suma      |     Įsipareigojimo suma iš pradinio pripažinimo žurnalo įrašo.                                  |
|     Pradinė turto suma          |     Turto suma iš pradinio pripažinimo žurnalo įrašo.                                      |

## <a name="lease-modification-report"></a>Ataskaita Nuomos keitimas
Ataskaitoje Nuomos keitimas rodomos visos nuomos, pakeistos nurodytame datų intervale. Ataskaitoje taip pat rodomas vartotojas, kuris pakoregavo nuomą, ir bendroji pakoreguoto įsipareigojimo suma. Ataskaitoje yra tolesni laukai. 

|     Ataskaitos laukai                 |     aprašymas           |
|---------------------------------  |-------------------------  |
|     Koregavo                   |     Asmens, kuris modifikavo nuomą, vartotojo vardas.                                |
|     Koregavimo data               |     Koregavimo žurnalo įrašo registravimo data.                        |
|     Koregavimai                   |     Bet kurio koregavimo žurnalo įrašo, užregistruoto nuomos įsipareigojimų sąskaitoje tarp datos parametrų, suma. Kredito operacijos bus rodomos kaip teigiamos, o debeto – kaip neigiamos.       |
|     Pelno (nuostolių) suma            |     Bet kurio koregavimo žurnalo įrašo, užregistruoto nuomos pelno / nuostolių sąskaitoje tarp datos parametrų, suma. Kredito operacijos bus rodomos kaip teigiamos, o debeto – kaip neigiamos.       |
|     Nepaskirstytas pelnas             |     Bet kurio koregavimo žurnalo įrašo, užregistruoto nuomos nepaskirstyto pelno sąskaitoje tarp datos parametrų, suma.      |
|     Pabaigos įsipareigojimų balansas      |     Gautas įsipareigojimų balansas nuomos koregavimo dieną.           |

## <a name="lease-movement-report"></a>Ataskaita Nuomos dinamika
Ataskaita Nuomos dinamika naudojama kaip užregistruotų keitimų taikymo ataskaita, skirta kiekvienos nuomos įsipareigojimų balansams. Ši ataskaita vartotojui leidžia peržiūrėti nuomos įsipareigojimų operacijas per nurodytą laikotarpį.

|     Ataskaitos laukai             |     aprašymas                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Pradžios data         |     Anksčiausios nuomos versijos pradžios data.    |
|     Nuomos terminas                |     Anksčiausios nuomos versijos nuomos terminas.           |
|     Likę mokėjimai        |     Nuomos mokesčių, kurie dar neužregistruoti, skaičius.                       |
|     Pradinis balansas         |     Visų operacijų, turinčių įtakos nuomos įsipareigojimams iki ataskaitos pradžios dienos, suma.             |
|     Pradinis pripažinimas       |     Bet kurios nuomos pradinio pripažinimo operacijos, kuri buvo užregistruota nurodytame ataskaitos datų intervale, suma.     |
|     Mokėjimai                  |     Nuomos mokėjimo operacijų, kurios užregistruotos nurodytame ataskaitos datų intervale, suma. Reikšmės šiame stulpelyje bus rodomos kaip neigiamos sumos, nes mokėjimai mažina nuomos įsipareigojimų balansą.  |
|     Pomėgiai                  |     Sukauptų nuomos palūkanų, kurios užregistruotos nurodytame ataskaitos datų intervale, suma.            |
|     Koregavimai               |     Nuomos užregistruotų koregavimo operacijų, kurios patenka į nurodytą ataskaitos datų intervalą, suma.                               |
|     Pabaigos likutis            |     Visų nuomos įsipareigojimų operacijų, kurios užregistruotos iki ataskaitos **pabaigos datos**, balansas.                  |

## <a name="lease-transactions-report"></a>Ataskaita Nuomos operacijos
Užklausa Nuomos operacijos parodo visus žurnalo įrašus, kuriuos sugeneravo modulis Turto nuoma. Kiekvienas žurnalo įrašas yra susijęs su knygos ID, iš kurio jis kilęs. Tai leidžia lengvai susieti žurnalo įrašą su atitinkama nuoma. Užklausa Nuomos operacijos veikia panašiai kaip didžiosios knygos puslapis **Kvitų operacijos**.

## <a name="weighted-average-discount-rate-report"></a>Ataskaita Svertinio vidurkio nuolaidos koeficientas
Ataskaita Svertinio vidurkio nuolaidos koeficientas atitinka JAV GAAP atskleidimo reikalavimą, nurodytą ASC 842-20-50-4(g)(4), taikomą svertinio vidurkio nuolaidos koeficientui. Norėdami peržiūrėti šią ataskaitą, eikite į **Turto nuoma > Užklausos ir ataskaitos > Atskleidimas > Svertinio vidurkio nuolaidos koeficientas**. Ataskaitoje yra tolesni laukai. 

|     Ataskaitos laukai                     |     aprašymas                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Įsigaliojimo data                        |     Šioje ataskaitoje bus įtrauktos visos nuomos, kurios buvo pradėtos dieną, sutampančią su datos parametru **Įsigaliojimas**, arba anksčiau. Ši ataskaita turi būti vykdoma paskutinę atskleistino laikotarpio dieną.      |
|     Juridinis subjektas                      |     Juridinis subjektas, susijęs su nuoma.                           |
|     Nuomos ID                          |     Unikalus nuomos ID.                                                  |
|     Nuomos aprašas                 |     Nuomos aprašas iš nuomos antraštės.                          |
|     Rezervuoti                              |     Rodomos nuomos konkretus knygos tipas.                                                                                                                                            |
|     Registravimo sluoksnis                     |     Kiekviena ilgalaikiam turtui priskirta knyga nustatoma konkrečiame registravimo sluoksnyje, turinčiame bendrą nusidėvėjimo tikslą.      |
|     Nuomos grupė                       |     Grupė, kuriai priklauso nuoma.                                 |
|     Nuolaidos koeficientas                     |     Koeficientas, naudojamas norint taikyti nuolaidą nuomos mokesčiams.                             |
|     Valiuta                          |     Naudotos operacijų valiutos santrumpa. Visose ataskaitose operacijų valiuta bus konvertuota į ataskaitų valiutą.  |
|     Likę nuomos mokesčiai          |     Bendroji nesumokėtų nuomos mokesčių iš mokėjimo grafiko suma, likusi **įsigaliojimo** dieną.            |
|     Likę svertiniai mokėjimai       |     Likę nuomos mokesčiai, padauginti iš naudojamo nuolaidos koeficiento.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
