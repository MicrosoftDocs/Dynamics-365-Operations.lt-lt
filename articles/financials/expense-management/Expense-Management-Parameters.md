---
title: "Išlaidų valdymo parametrai"
description: "Toliau pateikti parametrai kontroliuoja išlaidų valdymo veikimo būdą."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 22f766b780d10d4fc615660990729f008007787a
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="expense-management-parameters"></a>Išlaidų valdymo parametrai

[!include [banner](../includes/banner.md)]

-----------------------------

Parametrai kontroliuoja bendrąjį išlaidų valdymo veikimo būdą.

### <a name="general"></a>Bendra

| **Laukas**                                                | **Aprašymas**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standartinis kilometražo tarifas**                             | Įveskite išlaidų kompensacijos kilometražo tarifą. Tarifas bus padaugintas iš išlaidose įvesto kilometražo ir bus apskaičiuota kelionių išlaidų kompensuotina suma.                       |
|**Asmeninės išlaidos apmokėjo**                             | Pasirinkite, kas turi apmokėti visas kredito kortelės operacijų sumas, kurios klasifikuojamos kaip asmeninės.                                                                                                     |
|**Rodyti visą išlaidų ataskaitą detalizuojant atvirkštine tvarka**               | Pasirinkite šią pasirinktį, norėdami rodyti visas išlaidų ataskaitos išlaidas, kai peržiūrite konkretaus kvito, sugeneruoto registruojant išlaidų ataskaitą, pradinio dokumento informaciją.              |
|**Išankstinis kelionės patvirtinimas yra privalomas**                 | Pasirinkite šią pasirinktį, jei norite, kad kelionės paraiška turėtų būti pateikta ir patvirtinta prieš darbuotojui teikiant išlaidų ataskaitą.                                                                    |
|**Leisti prieš registruojant redaguoti paskirstymą**            | Pasirinkti, ar prieš registruojant galima redaguoti išlaidų ataskaitos paskirstymus.                                                                                                                 |
|**Įvertinti išlaidų valdymo strategijas**                     | Pasirinkite, kada išlaidos įvertinamos siekiant nustatyti, ar išlaidų strategija nepažeista. Išlaidų strategijos pažeidimų galima ieškoti, kai išlaidų įrašas įvestas ir įrašytas arba išlaidos pateiktos patvirtinti. Reikiamų kvitų strategijos taisyklės bus patikrintos, kai bus įrašyta išlaidų eilutė.                   |
|**Leisti vidinės įmonės išlaidų eilutes**                         | Pasirinkite, ar leisti išlaidų ataskaitoje išlaidas įvesti kitiems juridiniams subjektams.                                                                                                          |
|**Leisti redaguoti kredito kortelės išlaidų valiutos kursą** | Pasirinkite šią parinktį, jei norite vartotojui leisti redaguoti importuotų kreditinės kortelės išlaidų valiutos kursą.                                                                        |
|**Rodytini kelių lygių hierarchijos laukai**                  | Pasirinkite, kurie tvirtintojo laukai bus rodomi, kai išlaidų ataskaitos darbo eigos priskyrimo tipas nustatytas kaip hierarchija, o hierarchijos pasirinkimas nustatytas naudoti kelių lygių išlaidų tvirtinimo hierarchiją. Kai darbo eigoje naudojama kelių lygių tvirtinimo hierarchija, pasirinkti laukai bus rodomi ir redaguojami išlaidų ataskaitoje. |
|**Įveskite darbuotojo kredito kortelės numerį (2017 m. liepos mėn. naujinimas)**     | Pasirinkite, ar galima įvesti darbuotojui skirtą 15, ar 16 simbolių numerį puslapio **Kredito kortelės** lauke **Kortelės ID**.                                                                          |

### <a name="financial"></a>Finansinis

| **Laukas**                                                            | **Aprašymas**     |
|----------------------------------------------------------------------|------------------------------------|
|**DK kasdienio žurnalo pavadinimas**                                         | Pasirinkite DK žurnalo, kuriame užregistruojamos patvirtintos išlaidų ataskaitos, pavadinimą.            |
|**Įjungti mokesčių susigrąžinimą iš išlaidų**                                  | Pasirinkite šią parinktį, jei norite įjungti tinkamų išlaidų mokesčių susigrąžinimo funkciją. Šios parinkties negalima įjungti, jei įjungtos JAV PVM ir naudojimo mokesčio taisyklės.      |
|**Nedelsiant registruoti avansus grynaisiais pinigais**                                     | Pasirinkite šią parinktį, jei norite registruoti patvirtintą avansą grynaisiais pinigais, kai mokėjimo ir pervedimo procesas baigtas. Jei ši parinktis nepasirinkta, mokėjimo ir pervedimo procesas sugeneruos neužregistruotą bendrąjį žurnalą. |
|**Pataisyti apskaitos datą registruojant**                             | Pasirinkite šią parinktį, norėdami apskaitos datą naujinti registruojant išlaidas, jei dabartinis laikotarpis yra sulaikytas arba uždarytas. Apskaitos data bus nustatyta kaip kito atviro laikotarpio data.   |
|**Leisti grupuoti operacijas pagal mokėjimo būde nurodytą korespondentinę sąskaitą**      | Pasirinkite šią parinktį, norėdami išlaidų ataskaitos išlaidų operacijas apibendrinti pagal korespondentinę sąskaitą, nurodytą išlaidų mokėjimo būde.   
|**Mokestis įskaitytas**                                                   | Pasirinkite šią parinktį, jei PVM į išlaidų sumą norite įtraukti pagal numatytuosius parametrus.             |
|**Išduoti biudžeto rezervavimus uždarant kelionės paraiškas**            | Pasirinkite šią parinktį, norėdami išleisti rezervuotas lėšas, kai patvirtinta kelionės paraiška yra uždaryta.                                                                                   |
|**Leisti pateikti kelionės paraišką esant biudžeto pereikvojimui biudžeto registre ir projekto biudžete** | Pasirinkite šią parinktį, norėdami darbuotojams leisti pateikti patvirtinti kelionės paraiškas, kurios viršija biudžeto registre nustatytą leistiną biudžetą arba projekto leistiną biudžetą.            |
|**Leisti pateikti išlaidų ataskaitą esant biudžeto pereikvojimui biudžeto registre ir projekto biudžete**    | Pasirinkite šią parinktį, norėdami darbuotojams leisti pateikti patvirtinti išlaidų ataskaitas, kurios viršija biudžeto registre nustatytą leistiną biudžetą arba projekto leistiną biudžetą.                |
|**Leisti patvirtinti išlaidų ataskaitą esant biudžeto pereikvojimui tik biudžeto registre**                | Pasirinkite šią parinktį, norėdami leisti tvirtintojams tvirtinti išlaidų ataskaitas, kurios viršija biudžeto registre nustatytą leistiną biudžetą.                                                                       |

### <a name="per-diem"></a>Dienpinigiai

| **Laukai**                             | **Aprašymas**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimalus valandų skaičius, už kurį galima skirti dienpinigius**           | Įvesti numatytąjį minimalų skaičių valandų, kurias darbuotojas turi išdirbti per dieną, kad galėtų gauti dienpinigių išlaidoms, susijusioms su keliavimu.  Ši reikšmė yra naudojama tik kaip numatytoji dienpinigių tarifo pakopų lauko Minimalus valandų skaičius reikšmė.                                                                                      |
|**Maitinimo išlaidų procentas**                          | Įveskite numatytąjį maitinimui skiriamų dienpinigių procentą, kuris naudojamas pirmą ir paskutinę su keliavimu susijusių išlaidų dienas, kai laukas **Skaičiuoti maitinimo išlaidų sumažinimą pagal** nustatytas į parinktį **Maitinimo tipas (per dieną)** arba **Valgymų per dieną skaičius**. Pirmą ir paskutinę dieną darbo laikas gali būti trumpesnis nei įprastą darbo dieną. Todėl šioms dienoms skiriama dienpinigių suma gali skirtis nuo įprastos sumos. Jei procentas nustatytas kaip 0, pirmos ir paskutinės dienų atskaitymai bus 0,00. |
|**Viešbučio išlaidų procentas**                        | Įveskite numatytąjį viešbučiams skiriamų dienpinigių procentą, kuris naudojamas pirmą ir paskutinę su keliavimu susijusių išlaidų dienas. Pirmą ir paskutinę dieną darbo laikas gali būti trumpesnis nei įprastą darbo dieną. Todėl šioms dienoms skiriama dienpinigių suma gali skirtis nuo įprastos sumos. Jei procentas nustatytas kaip 0, pirmos ir paskutinės dienų atskaitymai bus 0,00.                                              |
|**Kitų išlaidų procentas**                        | Įveskite numatytąjį kitoms išlaidoms skiriamų dienpinigių procentą, kuris naudojamas pirmą ir paskutinę su keliavimu susijusių išlaidų dienas. Pirmą ir paskutinę dieną darbo laikas gali būti trumpesnis nei įprastą darbo dieną. Todėl šioms dienoms skiriama dienpinigių suma gali skirtis nuo įprastos sumos. Jei procentas nustatytas kaip 0, pirmos ir paskutinės dienų atskaitymai bus 0,00.                                                                                                     |
|**Pusryčiams skiriamos sumos sumažinimas procentais** | Įveskite dienpinigių pusryčiams sumažinimo sumą. Pavyzdžiui, jei darbuotojas gauna papildomus pusryčius, dienpinigių sumą galite sumažinti 10 procentų.                               |
|**Priešpiečiams skiriamos sumos sumažinimas procentais**    | Įveskite dienpinigių pietums sumažinimo sumą. Pavyzdžiui, jei darbuotojas gauna papildomus pietus, dienpinigių sumą galite sumažinti 15 procentų.                                       |
|**Pietums skiriamos sumos sumažinimas procentais**   | Įveskite dienpinigių vakarienei sumažinimo sumą. Pavyzdžiui, jei darbuotojas gauna papildomą vakarienę, dienpinigių sumą galite sumažinti 25 procentų.                                     |
|**Skaičiuoti maitinimo išlaidų sumažinimą pagal**         | Pasirinkite, kaip sistema skaičiuos maitinimo išlaidų dienpinigių sumažinimą, pasirinkdami, ar sumažinimas bus pagrįstas kelionės ar dienos maitinimo tipu, ar per dieną leistinų valgymų skaičiumi.|
|**Dienpinigių apvalinimas**                  | Pasirinkti apvalinimo tipą, naudojamą dienpinigių išlaidoms nustatyti. Jei pasirinksite įprastą apvalinimo būdą, visos dienpinigių išlaidos, kurių suma yra 0,50, bus apvalinamas iki 1,00, o visos dienpinigių išlaidos, kurių suma yra mažesnė nei 0,50, bus apvalinamos iki 0,00.                                                                                              |
|**Dienpinigių skaičiavimo pagrindas**         | Pasirinkite, ar dienpinigių suma skaičiuojama pagal kalendorinę dieną, ar pagal 24 valandų laikotarpį.       |

### <a name="fax-cover-pages"></a>Faksogramos tituliniai puslapiai

| **Laukas**                      | **Aprašymas**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instrukcijos**                   | Įveskite instrukcijas, kurių darbuotojai turės laikytis kurdami su išlaidų ataskaita susietiems kvitams siųsti naudojamos faksogramos titulinį puslapį. Spustelėkite mygtuką **Vertimai**, norėdami įvesti tekstą konkrečia kalba, kuris bus rodomas atsižvelgiant į vartotojo kalbą. |
|**Vartotojo ID (brūkšninio kodo informacija)** | Pasirinkę šią parinktį unikalųjį darbuotojo identifikatorių išsaugosite brūkšniniame kode, naudojamame faksogramos tituliniame puslapyje.                 |
|**Brūkšninis kodas**                      | Pasirinkite brūkšninį kodą, kuris naudojamas faksogramos tituliniame puslapyje. Brūkšninius kodus 39 ir 128 palaiko išlaidų valdymo sistema.               |

### <a name="anti-corruption"></a>Kova su korupcija

|                 <strong>Laukas</strong>                 |                                                                                                                                                                                            <strong>Aprašymas</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Rodyti kovos su korupcija patvirtinimą</strong>  | Pasirinkite šią parinktį, norėdami rodyti kovos su korupcija tekstą, kai kuriama nauja išlaidų ataskaita. Tada galima įjungti konkrečias išlaidų kategorijas, kurias nustačius išlaidų ataskaitoje reikės pasirinkti kovos su korupcija patvirtinimą. Pavyzdžiui, nustačius su vyriausybės pareigūno išlaidomis susijusią dovanų kategoriją, darbuotojui gali reikėti patvirtinti, kad išlaidos yra suderinamos su įmonės strategija, skirta vyriausybės tarnautojams. |
| <strong>Kovos su korupcija pranešimas, skirtas pateikėjui</strong> |                                                                                             Įveskite tekstą, kuris bus rodomas darbuotojui kuriant naują išlaidų ataskaitą. Spustelėkite mygtuką <strong>Vertimai</strong>, norėdami įvesti tekstą konkrečia kalba, kuris bus rodomas atsižvelgiant į vartotojo kalbą.                                                                                             |
| <strong>Kovos su korupcija pranešimas, skirtas tvirtintojui</strong>  |                                                                                             Įveskite tekstą, kuris bus rodomas tvirtintojui kuriant naują išlaidų ataskaitą. Spustelėkite mygtuką <strong>Vertimai</strong>, norėdami įvesti tekstą konkrečia kalba, kuris bus rodomas atsižvelgiant į vartotojo kalbą.                                                                                             |


