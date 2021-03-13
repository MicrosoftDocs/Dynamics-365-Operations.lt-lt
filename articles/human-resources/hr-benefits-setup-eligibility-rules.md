---
title: Tinkamumo taisyklių ir parinkčių konfigūravimas
description: Tinkamumo taisyklių ir parinkčių valdant išmokas programoje „Microsoft Dynamics 365 Human Resources“ nustatymas.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2920a03eaec226b306d03ebf8b899113128c410e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113543"
---
# <a name="configure-eligibility-rules-and-options"></a>Tinkamumo taisyklių ir parinkčių konfigūravimas

Sukonfigūravus reikiamus išmokų valdymo parametrus programoje „Microsoft Dynamics 365 Human Resources“, galima kurti tinkamumo taisykles, grupavimus, laikotarpius ir programas, kurias susiesite su išmokų planais.

## <a name="create-an-eligibility-rule"></a>Kurti tinkamumo taisyklę

Tinkamumo taisyklėse apibrėžiama, kurie darbuotojai gali registruotis kiekvienam išmokų planui gauti. Apibrėžę tinkamumo taisykles, priskiriate jas išmokų planams. Tada galite apdoroti registracijos tinkamumą, kad matytumėte kurie darbuotojai yra tinkami kiekvienam planui gauti. 

Atviros registracijos metu darbuotojai gali pasirinkti išmokų planus. Jeigu pagal tinkamumo taisykles darbuotojai tampa netinkamais išmokų planui gauti po to, kai jau užsiregistravo, jie automatiškai neišregistruojami. Paprastai nutikus gyvenimo įvykiui, kuris turi įtakos plano tinkamumui, darbuotojui inicijuojamas registracijos laikotarpis, per kurį jis turi pasirinkti planą, kurį turi teisę gauti. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Norėdami kurti tinkamumo taisyklę, skirtuke **Tinkamumo taisyklės** pasirinkite **Nauja**. Norėdami peržiūrėti su tinkamumo taisykle susietus planus, pasirinkite **Pridedami planai**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Tinkamumo taisyklė** | Unikalus tinkamumo taisyklės identifikatorius. |
   | **Aprašas** | Tinkamumo taisyklės aprašas. |
   | **Galiojimo pradžios data ir laikas** | Tinkamumo taisyklės pradžios data. | 
   | **Galiojimo pabaigos data ir laikas** | Tinkamumo taisyklės pabaigos data. |
   | **Naudoti darbuotojo tipą** | Nurodo, ar naudoti darbuotoją atitinkantį darbuotojo tipą išmokų tinkamumo taisyklėje. |
   | **Darbininko tipas** | Darbuotojo tipas, jei perjungiklis **Naudoti darbuotojo tipą** nustatytas kaip **Taip**. |
   | **Naudoti darbuotojo būseną** | Nurodo, ar naudoti darbuotojo įdarbinimo būseną išmokų tinkamumo taisyklėje. |
   | **Būsena** | Darbuotojo būsena, jei perjungiklis **Naudoti darbuotojo būseną** nustatytas kaip **Taip**. Jei perjungiklis **Naudoti darbuotojo būseną** nustatytas kaip **Ne**, šis laukas nenaudojamas. |
   | **Naudoti įdarbinimo kategoriją** | Nurodo, ar naudoti darbuotojo **įdarbinimo kategorijos** reikšmę išmokų tinkamumo taisyklėje. | 
   | **Įdarbinimo kategorija** | Darbuotojo įdarbinimo kategorija, jei perjungiklis **Naudoti įdarbinimo kategoriją** nustatytas kaip **Taip**. |
   | **Naudoti naują samdos taisyklę** | Nurodo, ar naudoti naujos samdos laikotarpio reikšmę kuriant išmokų tinkamumo taisyklę. |
   | **Registracijos laikotarpis** | Laikotarpis, per kurį leidžiama naujos samdos registracija. Jei tą patį nustatėte parametruose, parametrų nustatymams teikiama pirmenybė. |
   | **Naudoti ankstesnę įdarbinimo būseną** | Nurodo, ar naudoti ankstesnę darbuotojo įdarbinimo būseną išmokų tinkamumo taisyklėje. Pavyzdžiui, galite nurodyti tinkamumo taisyklę, kuri atsisako visų darbuotojų, kurie per 90 dienų nuo ankstesnio įdarbinimo perėjo iš būsenos **Atleistas** į būseną **Įdarbintas**, draudimo laukimo laikotarpio. |

4. Dalyje **Papildomi kriterijai** pasirinkite šias pasirinktis ir, jei reikia, pridėkite informaciją:

   | Parinktis | Aprašymas |
   | --- | --- |
   | **Tinkamas amžius** | Nurodo amžiaus intervalą ar intervalus, reikalingus tinkamumo taisyklei atitikti. |
   | **Tinkamas skyrius** | Nurodo padalinį arba padalinius, kuriems turi priklausyti darbuotojas, kad atitiktų tinkamumo taisyklę. |
   | **Tinkamas įdarbinimo tipas** | Nurodo įdarbinimo tipą ar tipus, kuriems turi būti priskiriamas darbuotojas, kad atitiktų tinkamumo taisyklę. Pavyzdžiui, dirbantis visą darbo dieną arba ne visą darbo dieną. |
   | **Tinkamas darbas** | Nurodo užduotį ar užduotys, atitinkančias tinkamumo taisyklę. Užduotys yra siejamos su pareigomis, o pareigas užima darbuotojai. |
   | **Tinkama užduoties funkcija** | Nurodo užduotie funkciją ar funkcijas, atitinkančias tinkamumo taisyklę. Pavyzdžiui, pardavėjai arba techniniai darbuotojai. |
   | **Tinkamas darbo tipas** | Nurodo užduoties tipą ar tipus, atitinkančius tinkamumo taisyklę. Pavyzdžiui, administratorius arba vadovas. |
   | **Tinkamas juridinis subjektas** | Nurodomas juridinis subjektas arba juridiniai subjektai, atitinkantys tinkamumo taisyklę. Pavyzdžiui, „Contoso Entertainment System“, JAV. |
   | **Tinkama kompensacijos sritis** | Nurodoma darbuotojo vietą, atitinkančią tinkamumo taisyklę. Pavyzdžiui, JAV centras. |
   | **Tinkamos pareigos** | Nurodomos vienos ar daugiau pareigų, atitinkančių tinkamumo taisyklę. Pavyzdžiui, personalo asistentas arba personalo vadybininkas. |
   | **Tinkamų pareigų tipas** | Nurodomas pareigų tipas ar tipai, atitinkantys tinkamumo taisyklę. Pavyzdžiui, dirbantis visą dieną. |
   | **Tinkama būsena** | Nurodomos valstijos arba provincijos, atitinkančios tinkamumo taisyklę. Pavyzdžiui, Šiaurės Dakota, JAV arba Britų Kolumbija, Kanada. |
   | **Tinkamos įdarbinimo sąlygos** | Nurodomos įdarbinimo sąlygos, atitinkančios tinkamumo taisyklę. Pavyzdžiui, neterminuota arba grupinė sutartis. |
   | **Tinkama sąjunga** | Nurodoma narystė profesinėje sąjungoje, atitinkanti tinkamumo taisyklę. Pavyzdžiui, Amerikos keltuvų vairuotojai. </br></br>Naudojant profesine sąjunga grindžiama tinkamumo taisyklę, turi būti užpildyta darbuotojo narystės sąjungoje pabaigos data. Šio lauko negalima palikti tuščio. |
   | **Tinkamas pašto indeksas** | Nurodomi pašto indeksai, atitinkantys tinkamumo taisyklę. Pavyzdžiui, 58104. |

5. Dalyje **Papildoma informacija** galite peržiūrėti šią papildomą informaciją:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Tinkamo vartotojo laukas** | Nurodomos papildomos tinkamumo taisyklės, grindžiamos kliento apibrėžtais laukais. |
   | **Tinkamumo tipas** | Nurodoma kriterijų kategorija, kurią pasirinkote dalyje **Papildomi kriterijai**. |
   | **Tinkamumo rekomendacija** | Nurodomos reikšmės, kurias pasirinkote dalyje **Papildomi kriterijai**. |
   | **Aprašas** | Aprašas, kurį pasirinkote dalyje **Papildomi kriterijai**. |

6. Pasirinkite **Įrašyti**.

## <a name="configure-bundles"></a>Konfigūruoti grupes

Grupės yra susijusių išmokų planų rinkiniai. Galite naudoti išmokų grupes, kad grupuotumėte išmokų planus, kuriuos darbuotojai turi pasirinkti norėdami užsiregistruoti tam tikriems išmokų planams, kurie gali priklausyti nuo kitų išmokų planų registracijų. Galite naudoti grupavimą tokiais atvejais:

- Sveikatos plano grupė, kurią sudaro didelių atskaitymų sveikatos draudimas ir susieta sveikatos taupomoji sąskaita (HSA).

- Gyvybės draudimo planas ir privalomas darbuotojo gyvybės draudimo planas grupuojamas priklausomojo gyvybės draudimo planu. Taip būtų užtikrinama, kad darbuotojas nepasirinktų priklausomojo gyvybės draudimo neužsiregistravęs darbuotojo draudimui gauti.

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Grupavimas**, pasirinkite **Naujas**, kad kurtumėte grupavimą. Norėdami peržiūrėti su grupavimu susietus planus, pasirinkite **Pridedami planai**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Grupavimas** | Unikalus grupavimo identifikatorius. |
   | **Aprašas** | Grupavimo aprašas. |
   | **Meistras** | Nurodoma, ar vienas iš grupėje esančių planų turi būti pažymėtas kaip pagrindinis planas. Pagrindinis planas turi būti pasirenkamas kaip grupės dalis atviros registracijos metu, kad išmokų administratorius galėtų patvirtinti darbuotojo išmokų pasirinkimus. |
   | **Galiojimo pradžios data ir laikas** | Grupavimo aktyvinimo data ir laikas. |
   | **Galioja iki** | Grupavimo galiojimo pabaigos data. Numatytasis parametras yra 2154-12-31, kuris atitinka niekada. |

4. Pasirinkite **Įrašyti**.

## <a name="configure-periods"></a>Laikotarpių konfigūravimas

Laikotarpiai apibrėžia išmokų galiojimo terminus ir laiką, kai darbuotojams leidžiama registruotis. Galite sukurti tiek laikotarpių, kiek norite, kad būtų išlaikyti atviros registracijos išmokoms gauti ir išmokų padengimo laikotarpiai. Išmokų plano metai gali atitikti kalendorinius metus arba jų neatitikti. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Laikotarpiai**, pasirinkite **Naujas**, kad kurtumėte laikotarpį. Norėdami vykdyti procesą, per kurį visi galiojantys aktyvūs išmokų planai bus pridėti prie išmokų laikotarpio, pasirinkite **Pridėti planus**. Norėdami peržiūrėti su grupavimu susietus planus, pasirinkite **Pridedami planai**. 

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Laikotarpis** | Unikalus laikotarpio identifikatorius. |
   | **Galiojimo pradžios data ir laikas** | Pradžios data ir laikas, kai išmokos laikotarpis yra aktyvus. |
   | **Galiojimo pabaigos data ir laikas** | Pradžios data ir laikas, kai išmokos laikotarpis tampa neaktyvus. |
   | **Registracijos pradžia** | Atviros registracijos pradžios data. Atvira registracija yra registracija, kai darbuotojas gali pasirinkti išmokas išmokų savitarnoje. |
   | **Registracijos pabaiga** | Atviros registracijos pabaigos data. |
   | **Atviri** | Nurodo, ar laikotarpis yra atviras, atsižvelgiant į sistemos datą ir galiojimo pradžios bei galiojimo pabaigos datas ir laiką. | 
   | **Ankstesnis laikotarpis** | Nurodomas išmokos laikotarpis, kuris yra ankstesnis nei pasirinktos išmokos laikotarpis. Ši informacija naudojama per išmokos tinkamumo registraciją, kad būtų galima priskirti planus, padengimo pasirinktis ir ankstesnių metų gavėjus. |
 
4. Pasirinkite **Įrašyti**.

## <a name="use-a-flex-credit-program"></a>Naudoti lanksčiųjų kreditų programą

Galite naudoti lanksčiųjų kreditų programas, kad užregistruotumėte darbuotojus išmokoms gauti pagal iš anksto nustatytą lanksčiųjų kreditų skaičių. Darbuotojai gali pasirinkti, kaip priskirti savo lanksčiuosius kreditus. Pavyzdžiui, jeigu darbuotojui taikomas sutuoktinio sveikatos draudimo planas, jie gali norėti naudoti kreditus, kuriuos būtų naudoję sveikatos draudimui, kitoms išmokoms.

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Laikotarpiai** pasirinkite **Lanksčiųjų kreditų programos**.

3. Pasirinkite lanksčiojo kredito programą, kuri bus taikoma. Šiuose laukuose pateikiama tokia informacija:

   | Laukas | Aprašymas |
   | --- | --- |
   | Išmokos kredito ID | Unikalus lanksčiųjų kreditų programos identifikatorius. |
   | Aprašymas | Lanksčiųjų kreditų programos aprašas. | 
   | Data Nuo | Lanksčiųjų kreditų aktyvinimo data ir laikas. |
   | Data Iki | Lanksčiųjų kreditų programos pabaigos data. Galite palikti numatytąją vertę (2154-12-31), kad nurodytumėte, jog lanksčiųjų kreditų programai nėra suplanuotos galiojimo pabaigos. |
   | Bendra kreditų vertė | Kreditų skaičius, kurį kiekvienas darbuotojas turės naudoti savo išmokoms. |
   | Proporcingumo taisyklė | Taisyklė, naudojama proporcingai paskirstyti lanksčiuosius kreditus, kai darbuotojas pasamdytas lanksčiųjų kreditų laikotarpio viduryje. </br></br><ul><li>**Nėra** – darbuotojas negauna lanksčiųjų kreditų, jei jis pasamdytas po lanksčiųjų kreditų programos laikotarpio pradžios.</li><li>**Visas kreditas** – darbuotojas gauna visą lanksčiųjų kreditų sumą, neatsižvelgiant į tai, kada jis įdarbintas.</li><li>**Proporcingai paskirstyti** – darbuotojas gauna proporcingai paskirstytą lanksčiųjų kreditų sumą, pagrįstą pagal tai, kada įdarbinimo pradžios data.</li></ul> |
   | Lanksčiųjų kreditų proporcingumo formulė | Taisyklė, naudojama proporcingai paskirstyti lanksčiuosius kreditus darbuotojams, pasamdytiems lanksčiųjų kreditų programos išmokų laikotarpio viduryje. Proporcingumas paremtas įdarbinimo pradžios data. Šis laukas naudojamas, tik jei lauke **Proporcingumo taisyklė** pasirinkote **Proporcingai paskirstyti**. </br></br><ul><li>**Kasdien** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna kasdien. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio dienų skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 400 dienų, sistema padalins bendrą lanksčiųjų kreditų skaičių iš 400, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per dieną gauna darbuotojai.</li><li>**Einamasis mėnuo** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna per mėnesį, ir suapvalinamas iki esamo mėnesio. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio mėnesių skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 15 mėnesių, sistema padalins bendrą lanksčiųjų kreditų skaičių iš 15, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per mėnesį gauna darbuotojai.</li><li>**Kitas mėnuo** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna per mėnesį, ir suapvalinamas iki kito mėnesio. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio mėnesių skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 15 mėnesių, sistema padalina bendrą lanksčiųjų kreditų skaičių iš 15, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per mėnesį gauna darbuotojai.</li></ul> |
   
   Įsitikinkite, kad kiekvienas išmokų planas yra registruojamas tik vienoje lanksčiojo kredito programoje per išmokos laikotarpį. Kitaip sistema nežinos, kokią lanksčiojo kredito programą naudoti, suteikiant lanksčiuosius kreditus, ir jums kils problemų. 

## <a name="configure-programs"></a>Programų konfigūravimas

Programos – tai išmokų planų, turinčių bendrų tinkamumo taisyklių, rinkinys. Galite nustatyti tinkamumo taisykles, skirtas visai programai, o ne kiekvienam atskiram planui. Pavyzdžiui, programa „Contoso Canada FTE“ arba vadovų lygmens programa „Contoso Europe”. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Programos**, pasirinkite **Nauja**, kad kurtumėte programą. Norėdami nustatyti išimtis darbuotojams, kurie neatitinka tinkamumo taisyklių reikalavimų, pasirinkite **Tinkamumo taisyklės nepaisymas**. Norėdami peržiūrėti su programa susietus planus, pasirinkite **Pridedami planai**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Programa** | Unikalus programos identifikatorius. |
   | **Aprašas** | Programos aprašas. | 
   | **Galiojimo pradžios data ir laikas** | Programos aktyvinimo data ir laikas. |
   | **Galiojimo pabaigos data ir laikas** | Programos galiojimo pabaigos data ir laikas. Numatytasis parametras yra 2154-12-31, kuris atitinka niekada. |
   | **Padengimo laukimo laikotarpis** | Laikotarpis, kurį darbuotojas turi palaukti, kol išmokų programa bus dengiama. |
   | **Atskaitymo laukimo laikotarpis** | Laikotarpis, kurį darbuotojas laukia, kol prasidės atskaitymai pagal išmokų programą. |
   | **Tinkamumo taisyklės** | Pasirinkite išmokos programai taikomas tinkamumo taisykles. Šio puslapio skirtuke **Tinkamumo taisyklės** galite apibrėžti tinkamumo taisykles. |
   
4. Pasirinkite **Įrašyti**.
