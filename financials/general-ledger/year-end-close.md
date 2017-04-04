---
title: "Uždarymas metų pabaigoje"
description: "Šioje temoje aprašoma reikalaujamos sąrankos ir veikia DK metų pabaigos uždaryti proceso veiksmai."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Uždarymas metų pabaigoje

Šioje temoje aprašoma reikalaujamos sąrankos ir veikia DK metų pabaigos uždaryti proceso veiksmai. 

Pasibaigus finansiniams metams, turite paleisti metų pabaigos uždaryti proceso perduoti pradinius balansus į naujus metus. Dauguma organizacijų, metų pabaigos uždaryti procesą bus paleisti kelis kartus. Pirmą kartą būtų gauti likučiai, perkelti į naujus finansinius metus. Metų pabaigoje uždaryti gali būti vėl paleiskite, kaip daug kartų yra reikia perkelti likučius iš reguliavimo įtraukimo į naujus finansinius metus. 

Per metų pabaigos uždaryti procesą, yra du tipai sukurtų operacijų. Atidarymo operacija visada yra sukurtas ir naudojamas sukurti pradinius balansus į naujus finansinius metus. Atidarymo operacijos rodo balanso DK sąskaitos likutį naujus finansinius metus ir atsvarų naujų finansinių metų pelno ir nuostolio DK sąskaitos likutį Nepaskirstytasis pelnas DK sąskaitoje. Uždaromos operacijos pasirinktinai sukuriamas pareikšti iki nulio uždaryti finansinių metų pelno ir nuostolio sąskaitų likučiai.

## <a name="prepare-to-run-the-year-end-close"></a>Parengti paleisti, metų pabaigoje uždaryti
Prieš pradėdami naudoti metų pabaigos uždaryti procesą, patvirtinti šie parametrai: 

Puslapyje **Pagrindinės sąskaita**

-   Patikrinti, **pagrindinės sąskaitos tipas** yra tinkamai apibrėžti kiekvienos pagrindinės sąskaitos. Pagrindinės sąskaitos tipas yra naudojamas nustatyti, ar pagrindinės sąskaitos likutis pareiškiamas pirmyn kaip pradinį likutį arba uždarytas į nepaskirstytąjį pelną atidarymo operacijų.
-   Ir **sąskaitos atidarymas** laukas gali būti naudojamas perduoti pagrindinės sąskaitos likutį į naują pagrindinės sąskaitos per metų pabaigos uždaryti. Yra įvesta nauja sąskaita ir **sąskaitos atidarymas** srityje. Paprastai tai bus naudojamas balanso pagrindinės sąskaitos kai sąskaita yra inaktyvuota ir naujos pagrindinės sąskaitos yra naudojamos naujus finansinius metus.

Dėl to **DK parametrų** puslapio pagal **užbaigti finansiniai metai**:

-   Į **naikinti uždaryti metus sandorių** variantas naudojamas nurodyti, ar sistemos sugeneruotas atidarymo operacijų iš ankstesnių metų pabaigos uždaryti išbraukti dar kartą paleidus metų pabaigos uždaryti. Jei ši pasirinktis bus nustatyta **taip**, panaikinamas ankstesnis atidarymo operacijos ir naują darbo operaciją yra sukurtas remiantis esamos pusiausvyros. Jei ši pasirinktis bus nustatyta **Nr**, ankstesnių atidarymo operacijos išlieka ir papildomus atidarymo operacijų yra sukurtas siekiant perkelti likučius į priekį nuo koreguoti operacijas, registruotas po ankstesnių metų pabaigos uždaryti.
-   Į **kurti uždarymo operacijas pervežant** variantas naudojamas kurti uždarymo operacijas siekiant pelno ir nuostolių sąskaitų likučius į nulinę padėtį uždaryti finansinius metus. Jei ši pasirinktis bus nustatyta **taip**, sukurtas sandorio atidarymo ir uždarymo operacijos. Jei ši pasirinktis bus nustatyta **Nr**, tik atidarymo operacija bus sukurtas, o kitų finansinių metų perkelti likučius. Pelno ir nuostolių sąskaitų likučių išlieka finansinių metų pabaigoje.
-   Į **finansinių metų būsenos nustatymas visam laikui uždaryti** parinktys yra naudojamos norint nustatyti finansinių metų būsena uždarytas visam laikui. Šį parametrą naudokite atsargiai, nes negalima atnaujinimo visų laikotarpių būsena uždarytas visam laikui, užkirsti kelią patikslinimai nebūtų paskelbtas fiskaliniais metais. Geriausia tai nustatyti **Nr**.
-   Į **kvito numeris turi būti užpildytas** parinktys yra naudojamos norint nustatyti, ar kvito numeris yra būtinas, kai veikia metų pabaigos uždaryti proceso. Tai geriausia reikalauti kvito numerį, kad būtų galima lengvai nustatyti atidarymo operacijų.

Dėl to **finansinio kalendoriaus** puslapis:

-   Kitų finansinių metų turi būti prieš paleidžiant metų pabaigos uždaryti. Kitų finansinių metų yra būtinas, siekiant sukurti pradžios balansų pradžios laikotarpiu.

Dėl to **knygos kalendoriaus** puslapis:

-   Pasirenkama: Galima nustatyti kiekvieno ataskaitinio laikotarpio finansinių metų uždaryti **palaikykite** užkirsti kelią naujų sandorių nuo įrašant. Nustačius koreguojančius įrašus, dėl sulaikymo laikotarpių gali būti atnaujintas registruoti koreguojančius įrašus, net jei metų pabaigos uždaryti procesas jau buvo paleista.

## <a name="define-year-end-close-templates"></a>Nurodykite finansinių metų pabaigos uždaryti šablonai
Po to, kai sistema yra sukonfigūruotas, metų pabaigos uždaryti procesas gali vykdyti. Dėl to **metų pabaigos uždaryti** puslapį, šabloną galima apibrėžti, kurių metų pabaigos uždaryti procesą juridinių asmenų grupės bus paleisti. Šablonas bus panaudota pakartotinai kiekvienų metų pabaigoje uždaryti, bet galima keisti pasikeitus jūsų organizacijoje. 

Pirma, nustatyti, kad **grupės pavadinimas** šabloną, ir pasirinkite finansinio kalendoriaus. Grupės pavadinimas turėtų nustatyti įtraukti juridinių asmenų grupės.  Pavyzdžiui, šablonai gali steigtis pagal geografinės padėties, su Šiaurės Amerikos teisės subjektai, EMEA juridiniai asmenys ir APAC juridinių asmenų grupės. 

Be to, juridiniai asmenys gali būti pridėta į šabloną. Juridiniai asmenys gali būti pridėta pažymėdami organizacijos hierarchiją arba pasirinkdami juridiniai asmenys. Jeigu pasirenkamas organizacinės hierarchijos, tik juridinių asmenų hierarchijoje, naudoti pasirinkto finansinio kalendoriaus bus įtraukti į šabloną. Jei naudojate juridinių asmenų įtraukti į šabloną, gali būti pridėta tik juridiniai asmenys su paties finansinio kalendoriaus. Paties finansinio kalendoriaus yra reikalinga, nes metų pabaigoje uždaryti vykdomas pasirinkdami finansiniais metais, kurie gali skirtis nuo kalendoriaus kalendorių. 

Pridėjus juridiniai subjektai, apibrėžti nepaskirstytojo pelno pagrindinės sąskaitos už kiekvienas juridinis asmuo. Kad **nuo praėjusių metų pabaigos uždaryti** laukas atnaujinamas kiekvieną kartą, metų pabaigos uždaryti vykdomas juridinio asmens. 

Į **finansinis aspektas** skirtukas naudojamas nurodyti, kurios finansinės dimensijos bus naudojama atidarymo operacijų. Atkreipkite dėmesį, kad jūs nustatyti parametrai svarbūs tik juridinis asmuo, pasirinktas dėl **juridinių asmenų** tinklelį. Kiekvienas juridinis asmuo tinklelyje bus pakartoti nustatymą. 

Į **perdavimo balanse matmenys** yra naudojami nustatyti, ar turėtų išlikti finansinės dimensijos apie operacijas, užregistruotas balanso sąskaitos atidarymo operacijos. Tai geriausia nustatyti šį kintamąjį į **taip**. Į **perdavimo pelno ir nuostolio dydis** yra naudojamas nurodyti, kurios finansinės dimensijos operacijas, užregistruotas pelno ir nuostolio ataskaita perduodama nepaskirstytojo pelno sąskaita. Pirma, nustatyti finansinės dimensijos susijusios su pasirinkto juridinio asmens. Tai apimtų visus finansinės dimensijos, užregistruotų per metus, net jeigu finansinių aspektų nėra aktyvi sąskaita struktūros dalis. Tada nustatykite kiekvienos dimensijos kaip **arti vieno** ar **uždaryti visus**.  Numatytoji reikšmė yra **uždaryti visus**, tvarko originalus finansinės dimensijos vertes, gautas užregistruotas operacijas ir jas naudoja, nes kuriant atidarymo likučius nepaskirstyto pelno sąskaitą. Atskiras nepaskirstytojo pelno pradžios balansus bus sukurta kiekvieno unikalus derinys dimensijų. Jei **arti vieno** yra pasirinkta, visos operacijos, užregistruotos su tos finansinės dimensijos bus apibendrinti į nepaskirstytojo pelno pradinis likutis dimensijos vertės lauke po **arti vieno**. Pavyzdžiui, Tarkime, kad visi sandoriai, finansinių metų buvo paskelbtas abonemento struktūrą, pagrindinės sąskaitos - departamentas. Departamento finansinio aspekto šablone **arti vieno** yra pažymėtas ir 100 yra įvesta vertė. Jei visas pajamas, visas operacijas, užregistruotas departamentų, 200, 300 ir 400 $100,000, vienas pradinis likutis bus sukurta Retained pajamos - 100. Jei pasirinksite **arti vieno** ir finansinės dimensijos vertės lauką paliksite tuščią, visos operacijos po į nepaskirstytąjį pelną su šios dimensijos vertė yra tuščia. 

Metų pabaigos uždaryti proceso neatitinka sąskaitos konstrukcijas. Juk sąskaitą struktūras gali pakeisti per finansinius metus ir tai ne visada įmanoma nustatyti atitinkamos sąskaitos struktūra dėl šių pokyčių.  Sukūrus atidarymo operacijų, balansai bus pateikta su finansinės dimensijos nurodytų metų pabaigos uždaryti šabloną. Pradžios balansą įrašų galėtų apimti finansinės dimensijos nebėra einamosios sąskaitos struktūra ir segmento derinių, kurie jau nebegalioja einamosios sąskaitos struktūra. Jei jūsų organizacija nori išskirti finansinės dimensijos nepaskirstytojo uždirbti pradinis likutis, nustatytas finansinio aspekto, kad reikia **arti vieno** ir tuščią dimensijos vertę.

## <a name="run-the-year-end-close-process"></a>Paleisti metų pabaigos uždaryti proceso
Po finansinių metų pabaigos uždaryti Šablonai yra sukurti, metų pabaigoje uždaryti procesas inicijuojamas pasirinkus **vykdyti finansinių metų** Naujintiveiksmų srityje. Žymėti viską arba pogrupis juridinių asmenų iš šablono, kurio norite paleisti metų pabaigos uždaryti. Kai veikia metų pabaigos uždaryti pirmą kartą per finansinius metus, greičiausiai bus pasirinkti visi juridiniai asmenys, sukurti balansų pradžios visi juridiniai asmenys. Jei jūs naudojate metų pabaigos uždaryti dar kartą, galite pasirinkti paleisti procesą tik juridiniams asmenims, kuriems buvo registruoti koreguojančius įrašus. 

Pasirinkite, kuriuos norėtumėte paleisti metų pabaigos uždaryti procesą prieš finansinių metų. Jei daugiau nei vieną uždarymo laikotarpiu yra paskutinė laikotarpio finansinių metų, į **laikotarpio pavadinimas** srityje taps prieinama, kad galite pasirinkti kurioje uždarymo laikotarpiu po uždarymo operacija, jei sąranka nustatyta sukurti uždarymo operacija. 

Įveskite kvito numeris, arba gali būti reikalaujama, atsižvelgiant į nustatymus apskritai DK parametrai. Tą patį kvito numerį bus naudojamas visi juridiniai asmenys, atrinkti metų pabaigos uždaryti procesą. Kvito numeris nėra sukurtas naudojant numeraciją. Tai geriausia kvito numerį, net jei tai nėra būtina. Įvesti čekio numerį, lengviau rasti atidarymo operacijos naujų finansinių metų. Jei nėra įrašytas kvito numeris, kvito yra tuščias atidarymo operacijos. 

Jei norite pakeisti ankstesnių metų pabaigos uždaryti pasirinktų finansinių metų, nustatyti **anuliuoti ankstesnį arti** į **taip**. Metų pabaigos uždaryti bus atšauktas, tačiau procesas gali būti pakartotas bet kuriuo metu. Jeigu sukeičiate pabaigos uždaryti, kad **nuo praėjusių metų pabaigos uždaryti** bus ne galima. 

Metų pabaigos uždaryti proceso pagal nutylėjimą paleisti paketais. Tai geriausia paleisti procesą paketais, vartotojas galėtų grįžti į kitas veiklos sritis. Po metų pabaigos uždaryti procesas bus baigtas, su **nuo praėjusių metų pabaigos uždaryti** bus atnaujintos sesijos data.

Daugiau informacijos rasite [uždaryti DK laikotarpio pabaigoje](close-general-ledger-at-period-end.md).


