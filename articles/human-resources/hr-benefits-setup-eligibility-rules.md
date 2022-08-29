---
title: Tinkamumo taisyklių ir parinkčių konfigūravimas
description: Šiame straipsnyje aprašoma, kaip nustatyti tinkamumo taisykles ir parinktis dalyje Išmokų valdymas programoje "Microsoft"Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
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
ms.openlocfilehash: 5540a2c39b3f9f53600e5edd5c63c99cec1fb000
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337342"
---
# <a name="configure-eligibility-rules-and-options"></a>Tinkamumo taisyklių ir parinkčių konfigūravimas 

Sukonfigūravę reikalingus išmokų valdymo parametrus programoje, galite kurti tinkamumo taisykles, grupavimus, laikotarpius ir programas, kuriuos susiesite su jūsų išmokų planais.

Tinkamumo taisyklės yra naudojamos norint nustatyti, ar darbuotojai atitinka plano reikalavimus. Darbuotojai turi atitikti bent vieną taisyklės sąlygų, kad būtų laikomi atitinkančiais reikalavimus išmokai gauti. Pavyzdžiui, plane turite dvi taisykles. Pirmoje taisyklėje (1 eilutė) nurodoma, kad darbuotojo tipas turi būti **Darbuotojas**. Antroje taisyklėje (2 eilutė) nurodoma, kad darbuotojas turi būti įdarbintas pilnu etatu. Todėl darbuotojai, kurie atitinka 1 taisyklę, yra tinkami, net jei jie dirba nepilnu etatu.

Tačiau galite nustatyti vieną taisyklę, turinčią kelias sąlygas. Tokiu atveju, darbuotojai turi atitikti visas taisyklės sąlygas, kad būtų laikomi atitinkančiais reikalavimus išmokai gauti. Pavyzdžiui, turite taisyklę, pavadintą **Darbuotojas pilnu etatu**. Šioje taisyklėje nurodoma, kad darbuotojo tipas turi būti **Darbuotojas** *ir* darbuotojas turi būti įdarbintas pilnu etatu. Todėl darbuotojai turi atitikti abi tinkamumo taisyklės sąlygas.

> [!IMPORTANT]
> Nors viena tinkamumo taisyklė turi būti susieta su kiekvienu išmokų planu. Su išmoka galite susieti kelias taisykles.

## <a name="create-an-eligibility-rule"></a>Kurti tinkamumo taisyklę

Tinkamumo taisyklėse apibrėžiama, kurie darbuotojai gali registruotis kiekvienam išmokų planui gauti. Apibrėžę tinkamumo taisykles, priskiriate jas išmokų planams. Tada galite apdoroti registracijos tinkamumą, kad matytumėte kurie darbuotojai yra tinkami kiekvienam planui gauti. 

Atviros registracijos metu darbuotojai gali pasirinkti išmokų planus. Jeigu pagal tinkamumo taisykles darbuotojai tampa netinkamais išmokų planui gauti po registracijos, jie nėra automatiškai išregistruojami. Paprastai nutikus gyvenimo įvykiui, kuris turi įtakos plano tinkamumui, darbuotojui inicijuojamas registracijos laikotarpis, per kurį jis turi pasirinkti planą, kurį turi teisę gauti. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Tinkamumo taisyklės** pasirinkite **Nauja**, kad sukurtumėte tinkamumo taisyklę. Norėdami peržiūrėti su tinkamumo taisykle susietus planus, pasirinkite **Pridedami planai**.

3. Nurodykite šių laukų reikšmes.

   | Laukas | Aprašas |
   | --- | --- |
   | **Tinkamumo taisyklė** | Unikalus tinkamumo taisyklės identifikatorius. |
   | **Aprašas** | Tinkamumo taisyklės aprašas. |
   | **Galiojimo pradžios data ir laikas** | Tinkamumo taisyklės pradžios data. | 
   | **Galiojimo pabaigos data ir laikas** | Tinkamumo taisyklės pabaigos data. |
   | **Naudoti darbuotojo tipą** | Nurodo, ar naudoti darbuotojo tipą išmokų tinkamumo taisyklėje. |
   | **Darbininko tipas** | Darbuotojo tipas, jei perjungiklis **Naudoti darbuotojo tipą** nustatytas kaip **Taip**. |
   | **Naudoti darbuotojo būseną** | Nurodo, ar reikia naudoti darbuotojo įdarbinimo būseną išmokų tinkamumo taisyklėje. |
   | **Būsena** | Darbuotojo būsena, jei perjungiklis **Naudoti darbuotojo būseną** nustatytas kaip **Taip**. Jei perjungiklis **Naudoti darbuotojo būseną** nustatytas į **Ne**, šis laukas nėra naudojamas. |
   | **Naudoti įdarbinimo kategoriją** | Nurodo, ar naudoti darbuotojo **Įdarbinimo kategorijos** reikšmę kaip išmokų tinkamumo taisyklės dalį. | 
   | **Įdarbinimo kategorija** | Darbuotojo įdarbinimo kategorija, jei perjungiklis **Naudoti įdarbinimo kategoriją** nustatytas į **Taip**. |
   | **Naudoti naują samdos taisyklę** | Nurodo, ar naudoti naujo samdinio laikotarpio reikšmę kaip išmokų tinkamumo taisyklės dalį. |
   | **Registracijos laikotarpis** | Laikotarpis, per kurį leidžiama naujos samdos registracija. Jei tą patį nustatėte parametruose, parametrų nustatymams teikiama pirmenybė. |
   | **Naudoti ankstesnę įdarbinimo būseną** | Nurodo, ar naudoti ankstesnę darbuotojo įdarbinimo būseną kaip išmokų tinkamumo taisyklės dalį. Pavyzdžiui, galite nurodyti tinkamumo taisyklę, kuri atsisako visų darbuotojų, kurie per 90 dienų nuo ankstesnio įdarbinimo perėjo iš būsenos **Atleistas** į būseną **Įdarbintas**, draudimo laukimo laikotarpio. |

4. Dalyje **Papildomi kriterijai** pasirinkite šias parinktis ir pridėkite informaciją, jei reikia.

   | Parinktis | Aprašas |
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
   | **Tinkama sąjunga** | Nurodoma narystė profesinėje sąjungoje, atitinkanti tinkamumo taisyklę. Pavyzdžiui, Amerikos keltuvų vairuotojai.</br></br>Naudojant profesine sąjunga pagrįstą tinkamumo taisyklę, turi būti užpildyta darbuotojo narystės sąjungoje pabaigos data. Negalite palikti jos tuščios. |
   | **Tinkamas pašto indeksas** | Nurodomi pašto indeksai, atitinkantys tinkamumo taisyklę. Pavyzdžiui, 58104. |

5. Dalyje **Papildoma informacija** galite peržiūrėti šią papildomą informaciją.

   | Laukas | Aprašas |
   | --- | --- |
   | **Tinkamo vartotojo laukas** | Nurodomos papildomos tinkamumo taisyklės, grindžiamos kliento apibrėžtais laukais. |
   | **Tinkamumo tipas** | Nurodoma kriterijų kategorija, kurią pasirinkote dalyje **Papildomi kriterijai**. |
   | **Tinkamumo rekomendacija** | Nurodomos reikšmės, kurias pasirinkote dalyje **Papildomi kriterijai**. |
   | **Aprašas** | Aprašas, kurį pasirinkote dalyje **Papildomi kriterijai**. |

6. Pasirinkite **Įrašyti**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Pasirinktinių laukų naudojimas tinkamumo taisyklėms

[Pasirinktiniai laukai](hr-developer-custom-fields.md) gali būti kuriami Personalo programoje papildomos informacijos sekimui. Šie laukai gali būti pridėti tiesiogiai prie vartotojo sąsajos, o stulpelis bus dinamiškai pridedamas prie esamos lentelės.  

Pasirinktiniai laukai gali būti naudojami tinkamumo procese. Tinkamumo taisyklės gali naudoti vieną ar daugiau pasirinktinių laukų reikšmių, kad nustatytų darbuotojo tinkamumą.  Norėdami pridėti pasirinktinį lauką prie esamos taisyklės arba sukurti naują taisyklę, eikite į **Išmokų valdymas > Saitai > Nustatymas > Tinkamumo taisyklės > Pasirinktinio lauko tinkamumas**. Šiame puslapyje galite sukurti taisyklę, kurioje naudojamas vienas ar keli pasirinktiniai laukai, taip pat galite apibrėžti kelias kiekvieno pasirinktinio lauko vertes tinkamumui nustatyti.

Toliau pateiktos lentelės palaiko pasirinktinius laukus, kuriuos galima panaudoti apdorojant tinkamumą:

- Darbuotojas („HcmWorker”)  
- Užduotis („HcmJob”)  
- Pareigos („HcmPosition”)  
- Pareigų informacija („HcmPositionDetail”)  
- Darbininko paskyrimas į pareigas  
- Įdarbinimas („HcmEmployment”)  
- Įdarbinimo informacija („HcmEmploymentDetails”)  
- Užduoties informacija („HcmJobDetails”)  

Toliau pateikti pasirinktiniai laukų tipai yra palaikomi apdorojant tinkamumą:

- Tekstas  
- Išrinkimo sąrašas  
- Numeris  
- Dešimtainis  
- Žymės langelis  

Šioje lentelėje rodoma pasirinktinio lauko tinkamumo formos lauko informacija.

| Laukas  | Aprašas |
|--------|-------------|
| Pavadinimas | Kuriamų kriterijų pavadinimas. |
| Lentelės pavadinimas | Lentelės, kurioje yra tinkamumo taisyklei naudojamas pasirinktinis laukas, pavadinimas. |
| Lauko pavadinimas | Laukas, kuris bus naudojamas tinkamumo taisyklei. |
| Operatoriaus tipas | Rodomas operatorius, naudotas pasirinktinio lauko tinkamumo konfigūracijoje. |
| Reikšmė | Rodoma reikšmė, naudota pasirinktinio lauko tinkamumo konfigūracijoje. |

## <a name="eligibility-logic"></a>Tinkamumo logika

Toliau pateiktuose skyriuose aprašoma, kaip apdorojamas išmokų tinkamumas.

### <a name="rules-assigned-to-a-plan"></a>Planui priskirtos taisyklės 
Kai išmokų planui yra priskirtos kelios tinkamumo taisyklės, darbuotojas turi atitikti bent vieną taisyklę, kad būtų tinkamas užsiregistruoti išmokų plane.  Toliau pateiktame pavyzdyje darbuotojas turi atitikti **Užduoties tipo** arba **Aktyvių darbuotojų** taisyklės reikalavimus.

![Darbuotojas turi atitikti Užduoties tipo arba Aktyvių darbuotojų taisyklės reikalavimus.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Tinkamumo taisyklės kriterijai 
Taisyklėje apibrėžiate kriterijus, sudarančius taisyklę. Aukščiau pateiktame pavyzdyje **Užduoties tipo** taisyklės kriterijus yra toks, kuriame Užduoties tipas = Direktoriai. Todėl darbuotojas turi būti direktorius, kad būtų tinkamas. Tai yra tokia taisyklė, kurioje yra tik vienas kriterijus.

Galite apibrėžti taisykles, kurios turi kelis kriterijus. Kai nustatote kelis tinkamumo taisyklės kriterijus, darbuotojas turi atitikti kiekvieną tos taisyklės kriterijų, kad būtų tinkamas išmokų planui. 

Pavyzdžiui, aukščiau esanti taisyklė **Aktyvūs darbuotojai** yra sudaryta iš šių kriterijų. Kad darbuotojas būtų tinkamas pagal **Aktyvių darbuotojų** taisyklę, darbuotojas turi būti įdarbintas juridinio subjekto USMF *ir* jo pareigų tipas turi būti pilnos darbo dienos.  

![Tinkamumo taisyklės kriterijai.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Kelios kriterijų sąlygos

Taisykles galima toliau išplėsti, kad būtų galima naudoti kelias sąlygas viename kriterijuje. Darbuotojas turi atitikti bent vieną sąlygą, kad būtų tinkamas. Kuriant pagal aukščiau pateiktą pavyzdį, galima toliau išplėsti **Aktyvių darbuotojų** taisyklę, kad būtų įtraukti ir nepilną darbo dieną dirbantys darbuotojai. Todėl dabar darbuotojas turi būti USMF darbuotojas *ir* dirbti pilną arba nepilną darbo dieną.  

![Kelios sąlygos kriterijams.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Pasirinktinio lauko kriterijaus tinkamumo sąlygos 
Panašiai kaip ir aukščiau, pasirinktiniai laukai gali būti naudojami tinkamumo taisyklėms kurti ir dirbti tuo pačiu būdu. Pavyzdžiui, galbūt norėsite pasiūlyti interneto mokesčių kompensaciją Fargo ir Kopenhagos darbuotojams, kurie dirba iš namų, nes interneto išlaidos tose vietose yra didesnės. Norėdami tai padaryti, sukurkite du pasirinktinius laukus: **Biuro vieta** (išrinkimo sąrašas) ir **Darbas iš namų** (žymės langelis). Tada sukurkite taisyklę, pavadintą **WFH darbuotojai**. Taisyklės kriterijus yra ten, kur **Biuro vieta = Fargo** arba **Kopenhaga** *ir* ten, kur **Darbas iš namų = Taip**.

Pasirinktines tinkamumo taisykles reikėtų nustatyti taip, kaip nurodyta toliau pateiktame paveikslėlyje. 

![Tinkamumo sąlygos pasirinktinio lauko kriterijuje.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Konfigūruoti grupes

Grupės yra susijusių išmokų planų rinkiniai. Galite naudoti išmokų grupes, kad grupuotumėte išmokų planus, kuriuos darbuotojai turi pasirinkti norėdami užsiregistruoti tam tikriems išmokų planams, kurie gali priklausyti nuo kitų išmokų planų registracijų. Galite naudoti grupavimą tokiais atvejais:

- Sveikatos plano grupė, kurią sudaro didelių atskaitymų sveikatos draudimas ir susieta sveikatos taupomoji sąskaita (HSA).

- Gyvybės draudimo planas ir privalomas darbuotojo gyvybės draudimo planas grupuojamas priklausomojo gyvybės draudimo planu. Taip būtų užtikrinama, kad darbuotojas nepasirinktų priklausomojo gyvybės draudimo neužsiregistravęs darbuotojo draudimui gauti.

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Grupavimas**, pasirinkite **Naujas**, kad kurtumėte grupavimą. Norėdami peržiūrėti su grupavimu susietus planus, pasirinkite **Pridedami planai**.

3. Nurodykite šių laukų reikšmes.

   | Laukas | Aprašas |
   | --- | --- |
   | **Grupuoti** | Unikalus grupavimo identifikatorius. |
   | **Aprašas** | Grupavimo aprašas. |
   | **Meistras** | Nurodoma, ar vienas iš grupėje esančių planų turi būti pažymėtas kaip pagrindinis planas. Pagrindinis planas turi būti pasirenkamas kaip grupavimo dalis atviros registracijos metu, kad išmokų administratorius galėtų patvirtinti darbuotojo išmokų pasirinkimus. |
   | **Galiojimo pradžios data ir laikas** | Grupavimo aktyvinimo data ir laikas. |
   | **Galioja iki** | Grupavimo galiojimo pabaigos data. Numatytasis parametras yra 2154-12-31, kuris atitinka niekada. |

4. Pasirinkite **Įrašyti**.

## <a name="configure-periods"></a>Laikotarpių konfigūravimas

Laikotarpiai apibrėžia išmokų galiojimo terminus ir laiką, kai darbuotojams leidžiama registruotis. Galite sukurti tiek laikotarpių, kiek norite, kad būtų išlaikyti atviros registracijos išmokoms gauti ir išmokų padengimo laikotarpiai. Išmokų plano metai gali atitikti kalendorinius metus arba jų neatitikti. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Laikotarpiai**, pasirinkite **Naujas**, kad kurtumėte laikotarpį. Norėdami vykdyti procesą, per kurį visi galiojantys aktyvūs išmokų planai bus pridėti prie išmokų laikotarpio, pasirinkite **Pridėti planus**. Norėdami peržiūrėti su grupavimu susietus planus, pasirinkite **Pridedami planai**. 

3. Nurodykite šių laukų reikšmes.

   | Laukas | Aprašas |
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

Galite naudoti lanksčiųjų kreditų programas, kad užregistruotumėte darbuotojus išmokoms gauti pagal iš anksto nustatytą lanksčiųjų kreditų skaičių. Darbuotojai gali pasirinkti, kaip priskirti savo lanksčiuosius kreditus. Pavyzdžiui, jeigu darbuotojui yra taikomas sutuoktinio sveikatos draudimo planas, jis gali norėti naudoti kreditus, kuriuos būtų naudojęs sveikatos draudimui kitoms išmokoms.

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Laikotarpiai** pasirinkite **Lanksčiųjų kreditų programos**.

3. Pasirinkite lanksčiojo kredito programą, kuri bus taikoma. Laukuose pateikiama tokia informacija.

   | Laukas | Aprašas |
   | --- | --- |
   | **Išmokos kredito ID** | Unikalus lanksčiųjų kreditų programos identifikatorius. |
   | **Aprašymas** | Lanksčiųjų kreditų programos aprašas. | 
   | **Data Nuo** | Lanksčiųjų kreditų aktyvinimo data ir laikas. |
   | **Data Iki** | Lanksčiųjų kreditų programos pabaigos data. Galite palikti numatytąją vertę (12/31/2154), kad nurodytumėte, jog lanksčiųjų kreditų programa neturi suplanuotos galiojimo pabaigos. |
   | **Bendra kreditų vertė** | Kreditų skaičius, kurį kiekvienas darbuotojas turės naudoti savo išmokoms. |
   | **Proporcingumo taisyklė** | Taisyklė, naudojama proporcingai paskirstyti lanksčiuosius kreditus, kai darbuotojas pasamdytas lanksčiųjų kreditų laikotarpio viduryje. </br></br><ul><li>**Nėra** – darbuotojas negauna lanksčiųjų kreditų, jei jis pasamdytas po lanksčiųjų kreditų programos laikotarpio pradžios.</li><li>**Visas kreditas** – darbuotojas gauna visą lanksčiųjų kreditų sumą, neatsižvelgiant į tai, kada jis įdarbintas.</li><li>**Proporcingai paskirstyti** – darbuotojas gauna proporcingai paskirstytą lanksčiųjų kreditų sumą, pagrįstą pagal tai, kada įdarbinimo pradžios data.</li></ul> |
   | **Lanksčiųjų kreditų proporcingumo formulė** | Taisyklė, naudojama proporcingai paskirstyti lanksčiuosius kreditus darbuotojams, pasamdytiems lanksčiųjų kreditų programos išmokų laikotarpio viduryje. Proporcingumas paremtas įdarbinimo pradžios data. Šis laukas naudojamas, tik jei lauke **Proporcingumo taisyklė** pasirinkote **Proporcingai paskirstyti**. </br></br><ul><li>**Kasdien** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna kasdien. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio dienų skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 400 dienų, sistema padalins bendrą lanksčiųjų kreditų skaičių iš 400, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per dieną gauna darbuotojai.</li><li>**Einamasis mėnuo** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna per mėnesį, ir suapvalinamas iki esamo mėnesio. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio mėnesių skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 15 mėnesių, sistema padalins bendrą lanksčiųjų kreditų skaičių iš 15, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per mėnesį gauna darbuotojai.</li><li>**Kitas mėnuo** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna per mėnesį, ir suapvalinamas iki kito mėnesio. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio mėnesių skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 15 mėnesių, sistema padalina bendrą lanksčiųjų kreditų skaičių iš 15, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per mėnesį gauna darbuotojai.</li></ul> |
   
   Įsitikinkite, kad kiekvienas išmokų planas yra registruojamas tik vienoje lanksčiojo kredito programoje per išmokos laikotarpį. Kitu atveju, sistema nežinos, kokią lanksčiojo kredito programą naudoti suteikiant lanksčiuosius kreditus ir jums kils problemų. 

## <a name="configure-programs"></a>Programų konfigūravimas

Programos – tai išmokų planų, turinčių bendrų tinkamumo taisyklių, rinkinys. Galite nustatyti tinkamumo taisykles, skirtas visai programai, o ne kiekvienam atskiram planui. Pavyzdžiui, programa „Contoso Canada FTE“ arba vadovų lygmens programa „Contoso Europe”. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Tinkamumo taisyklės ir parinktys**.

2. Skirtuke **Programos**, pasirinkite **Nauja**, kad kurtumėte programą. Norėdami nustatyti išimtis darbuotojams, kurie neatitinka tinkamumo taisyklių reikalavimų, pasirinkite **Tinkamumo taisyklės nepaisymas**. Norėdami peržiūrėti su programa susietus planus, pasirinkite **Pridedami planai**.

3. Nurodykite šių laukų reikšmes.

   | Laukas | Aprašas |
   | --- | --- |
   | **Programa** | Unikalus programos identifikatorius. |
   | **Aprašas** | Programos aprašas. | 
   | **Galiojimo pradžios data ir laikas** | Programos aktyvinimo data ir laikas. |
   | **Galiojimo pabaigos data ir laikas** | Programos galiojimo pabaigos data ir laikas. Numatytasis parametras yra 2154-12-31, kuris atitinka niekada. |
   | **Padengimo laukimo laikotarpis** | Laikotarpis, kurį darbuotojas turi palaukti, kol išmokų programa bus dengiama. |
   | **Atskaitymo laukimo laikotarpis** | Laikotarpis, kurį darbuotojas laukia, kol prasidės atskaitymai pagal išmokų programą. |
   | **Tinkamumo taisyklės** | Pasirinkite išmokos programai taikomas tinkamumo taisykles. Šio puslapio skirtuke **Tinkamumo taisyklės** galite apibrėžti tinkamumo taisykles. |
   
4. Pasirinkite **Įrašyti**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
