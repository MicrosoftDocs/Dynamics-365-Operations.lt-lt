---
title: Biudžeto planavimo integravimas su kitais moduliais
description: Biudžeto planus galima generuoti iš kelių skirtingų išteklių. Pagrindiniai periodinio proceso elementai yra tie patys, kaip ir visų išteklių elementai.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7456d0c6a9114fae71aff7b4070d86090e2c7c9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834180"
---
# <a name="budget-planning-integration-with-other-modules"></a>Biudžeto planavimo integravimas su kitais moduliais

[!include [banner](../includes/banner.md)]

 Biudžeto planus galima generuoti iš kelių skirtingų išteklių. Pagrindiniai periodinio proceso elementai yra tie patys, kaip ir visų išteklių elementai. 



<a name="periodic-processes-for-generating-budget-plans"></a>Biudžeto planų generavimo periodiniai procesai
----------------------------------------------

Biudžeto planus galima generuoti iš toliau nurodytų išteklių.

-   DK operacijos
-   Ilgalaikis turtas
-   Prognozuojamos pareigos
-   Projekto prognozė
-   Tiekimo prognozės
-   Poreikio prognozės
-   Biudžeto registro įrašai
-   Kiti biudžeto planai

Pagrindiniai periodinio proceso elementai yra tie patys, kaip ir visų procesų elementai. Skirtukai suteikia galimybę nurodyti šaltinio duomenis, paskirties (biudžeto plano) atributus ir parinktis, skirtas procesą vykdyti fone kaip paketinį vykdymą. Vėlesniuose šio straipsnio skyriuose aprašomi elementai, kurie gali būti rodomi ne visuose procesuose.

### <a name="actions"></a>Veiksmai

Galima naudoti tris bet kurio generavimo proceso veiksmus, nurodytus toliau.

-   **Kurti naują biudžeto planą** – sukuriamas naujas planas, kurio atributai pasirenkami sekcijoje **Paskirties vieta**. Šie atributai nebūtinai turi būti unikalūs. Todėl du planai gali turėti tokį patį pavadinimą ir kitas reikšmes.
-   **Pakeisti esamą biudžeto plano scenarijų** – panaikinami visi pasirinkto biudžeto plano scenarijaus paskirties biudžeto plano duomenys ir sukuriamos naujos eilutės, kuriose naudojami pasirinkto šaltinio duomenys.
-   **Atnaujinti esamą biudžeto plano scenarijų ir pridėti naujų duomenų** – atnaujinamos esamos paskirties plano eilutes, kurios atitinka šaltinio eilutes, ir sukuriamos naujos eilutės naujiems duomenims įtraukti. Gretinimas yra pagrįstas DK sąskaitos, datos, biudžeto klasės ir įvairių kitų laukų reikšmėmis. Pvz., kai biudžeto planus generuojate pagal prognozės pozicijas, pozicijos numeris yra svarbus laukas. Visos eilutės, kurių pozicijos numeris atitinka šaltinio pozicijos numerį, yra pakeičiamos naujomis eilutėmis iš šaltinio.

### <a name="source"></a>Šaltinis

Skirta visiems procesams: skirtuke **Šaltinis** galima filtruoti duomenis naudojant mygtuką **Filtras**. Pagal numatytuosius parametrus kiekvieno proceso konkretūs laukai yra įtraukiami į filtrą. Pvz., jei vykdomas procesas **Generuoti biudžeto planą pagal didžiąją knygą**, galima naudoti kategorijas **DK sąskaita** ir **Pagrindinė sąskaita** ir jos yra rodomos generavimo puslapyje. Į puslapį įtraukiami visi į filtrą įtraukti laukai bei kiti jūsų nurodyti kriterijai.

### <a name="target"></a>Uždavinys

Skirtuko **Paskirtis** parinktis **Retrospektyvinis** suteikia galimybę šaltinio duomenų datas naudoti kaip biudžeto plano įsigaliojimo datą. Paprastai įsigaliojimo data patekti į plano biudžeto ciklą. Kai parinktį **Retrospektyvinis** nustatote į **Taip**, naudojama šaltinio data (ir net metai), todėl praeities duomenis galima naudoti kaip lyginimo pagrindą. Biudžeto plano retrospektyvinių duomenų modifikuoti negalima ir yra nustatyta patvirtinta plano darbo eigos būsena. Tačiau būseną galima nustatyti iš naujo , jei reikia keisti kitus plano scenarijus.

Puslapio viršuje esantis laukas Į **Sudėti sumas pagal** taip pat lemia, kuri data yra naudojama. Šiame lauke sudedamos sumos ir pasirinktinai įsigaliojimo data yra nustatoma kaip pirmoji finansinių metų arba ataskaitinio laikotarpio data. 

Daugelį skirtuko <strong>Paskirtis</strong> laukų bus galima redaguoti arba tik skaityti, priklausomai nuo pasirinkto veiksmo. Jei vietoje to, kad kurtumėte naują biudžeto planą, nusprendžiate naujinti esamą, lauko **Biudžeto plano pavadinimas** nebus galima naudoti, bet bus suaktyvinti laukai, susiję su esamo plano pasirinkimu. Skirtukų **Paskirtis** ir **Šaltinis** lauko **Didžioji knyga** niekada negalima naudoti, nes jo reikšmė yra nustatoma pagal pasirinktą biudžeto planavimo procesą. 

Lauke **Biudžeto klasė** biudžeto plano eilutes galima nustatyti kaip išlaidų operacijas arba įplaukų operacijas. Paprastai įplaukų operacijos yra DK sąskaitos kreditai ir todėl jos yra įrašomos kaip neigiamos sumos. Paprastai šios operacijos biudžeto plane taip pat yra rodomos kaip neigiamos sumos. Tačiau biudžeto klasę į plano maketą įtraukę kaip lauką, galite nustatyti, kad įplaukos būtų rodomos kaip teigiamos sumos.

### <a name="generation-rules"></a>Generavimo taisyklės

Trijuose laukuose pateikiamos papildomų funkcijos: **Koeficientas**, **Minimalus** ir **Apvalinimo** **taisyklė**. 

Lauko **Koeficientas** reikšmė yra padauginama iš šaltinio sumos, siekiant nustatyti biudžeto plano sumą. Tada kurdami biudžeto plano eilutes galite atlikti koregavimus. Pavyzdžiui, galite įvesti **1,03**, norėdami nurodyti 3 procentų padidėjimą. Koeficientas turi būti teigiamas skaičius. 

Lauke **Minimalus** galima nustatyti kuriamos biudžeto plano eilutės ribinę sumą. Jei šaltinio suma yra mažesnė nei šis skaičius, biudžeto plano eilutė nėra kuriama. Įvedus reikšmę **0,00**, leidžiamos visos sumos, bet eilučių sumos gali būti ne tik teigiamos. (Nėra reikšmės, kuri leistų tik eilučių teigiamas sumas. Neigiamos sumos yra visada įtraukiamos ir jos paprastai nurodo kredito įrašus.)

Lauke **Apvalinimo taisyklė** galima nustatyti kuriamų biudžeto plano eilučių tikslumą. Sumas galima apvalinti iki artimiausio valiutos 1,00, 10,00, 100,00 ir t. t.

## <a name="notes-for-specific-processes"></a>Pastabos apie konkrečius procesus
### <a name="generate-budget-plan-from-general-ledger"></a>Generuoti biudžeto planą pagal didžiąją knygą

Kuriant biudžeto planą iš DK duomenų, lauko **Sudėti sumas pagal** reikšmė turi būti nustatyta kaip **Finansiniai metai**, jei parinktis **Retrospektyvinis** yra nustatyta kaip **Ne**. Šaltinio laikotarpiai ir datos gali neatitikti paskirties laikotarpių ir datų. Kadangi nėra patikimo būdo proceso metu susieti šias reikšmes, procesą galima apriboti iki pirmųjų metų. 

Paskirties vietoje lauko **Biudžeto klasė** reikšmė yra nustatoma kaip **Išlaidos** arba **Įplaukos**. Šis parametras naudojamas siekiant pasirinkti kuriamų eilučių atributą **Biudžeto tipas**, kai eilutės pagrindinės sąskaitos tipas nėra **Įplaukos** arba **Išlaidos**.

### <a name="generate-budget-plan-from-fixed-assets"></a>Generuoti biudžeto planą pagal ilgalaikį turtą

Vykdant procesą **Generuoti biudžeto planą pagal ilgalaikį turtą**, agreguoti pagal laikotarpį arba dieną negalima. Taip pat negalima planą nustatyti kaip retrospektyvinį. Šį periodinį procesą galite naudoti, norėdami numatomas ilgalaikio turto operacijas įtraukti į biudžeto planavimą.

### <a name="generate-budget-plan-from-forecast-positions"></a>Generuoti biudžeto planą pagal prognozuojamas pareigas

Proceso **Generuoti biudžeto planą pagal prognozės pozicijas** metu biudžeto plano eilutei priskiriama šaltinio prognozės pozicija. Poziciją galite peržiūrėti į biudžeto plano maketą įtraukdami prognozės poziciją kaip eilutę arba naudodami užklausą **Biudžeto plano eilutės**. Jei nenorite prognozės pozicijos priskirti biudžeto plano eilutėms, nustatykite parinktį **Įtraukti poziciją į biudžeto plano eilutę** kaip **Ne**.

Biudžeto plano eilutės sujungiamos pagal DK sąskaitą ir poziciją. Tačiau jūs galite pozicijos numerio neįtraukti, kad eilutės būtų sujungiamos tik pagal DK sąskaitą. Skirtuke **Paskirtis** parinktį **Įtraukti poziciją į biudžeto planą** nustatykite kaip **Ne**.

Lauke **Biudžeto plano FTE scenarijus** galima pasirinkti į biudžeto plano scenarijų įtraukti viso etato ekvivalentų (FTE) skaičių. Šiame lauke galima naudoti tik kiekio tipo scenarijus, įtrauktus į tikslinio biudžeto plano maketą. Jei pasirinksite FTE scenarijų, taip pat turite pasirinkti FTE pagrindinę sąskaitą. Ši sąskaita naudojama kuriant kiekio biudžeto plano eilutes. 

Šaltinyje pasirinkti biudžeto planavimo procesas ir biudžeto plano scenarijus nustato paskirties scenarijaus biudžeto planavimo procesą ir scenarijų. Kadangi šie atributai yra priskiriami prognozės pozicijoms, jie turi atitikti biudžeto planą. Todėl paskirties vietoje šių atributų modifikuoti negalima.

### <a name="generate-budget-plan-from-project-forecasts"></a>Generuoti biudžeto planą pagal projekto prognozes

Procesų **Generuoti biudžeto planą pagal projekto prognozes** ir **Generuoti biudžeto planą pagal prognozės pozicijas** metu į kiekio scenarijų galima įtraukti projekto kiekius (valandas, išlaidas ir prekes). Taip pat šių procesų metu naudojami panašūs biudžeto plano maketo stulpelių filtrai. 

Trys skirtuko **Šaltinis** sekcijos **Įtraukti išrašą** parinktys nurodo, kurios biudžeto plano eilutės bus kuriamos. Šios parinktys yra tos pačios, kaip ir parinktys, kurias galima naudoti biudžeto registro įrašus kuriant tiesiogiai pagal projekto prognozes. Nustatykite parinktį **Pelnas ir nuostolis** kaip **Taip**, norėdami kurti išlaidų ir įplaukų eilutes. Nustatykite parinktį **NG** kaip **Taip**, norėdami kurti nebaigtos gamybos įrašus. Nustatykite parinktį **Atlyginimo paskirstymas:** kaip **Taip**, norėdami kurti valandinių operacijų algalapio korespondentinių sąskaitų eilutes. 

Lauko **Biudžeto klasė** nėra, nes biudžeto klasę (**Išlaidos** arba **Įplaukos**) nustato šaltinis. 

Projektų biudžetus galima naudoti kaip šaltinį, pasirenkant prognozės modelį, kuriame yra projekto biudžeto sumos. Atminkite, kad projektų biudžetai sukuria projekto prognozės įrašus, kai jie yra patvirtinami.

Norėdami pasirinkti tik biudžeto plano eilučių išlaidas arba pajamas, naudokite filtrą ir pasirinkite <strong>Biudžeto atnaujinimai: sumos tipas = išlaidos</strong>. Norėdami pasirinkti tik vieno tipo prognozę, naudokite filtrą ir pasirinkite <strong>Biudžeto atnaujinimai: operacijos tipas = *xxx</strong>*. 

Biudžeto plano scenarijui generuoti galima naudoti tik vieną prognozės modelį. Jei paleisite vieno prognozės modelio procesą, o tada vykdysite naujinimą ir bandysite nurodyti kitą modelį, pirmasis modelis bus perrašytas, jei bus taikomi tas pats projektas ir tos pačios DK sąskaitos. Norėdami biudžeto plano scenarijų generuoti pagal daugiau nei vieną prognozės modelį, generuokite skirtingus biudžeto plano scenarijus ir naudokite paskirstymo parinktis jiems į kitą scenarijų įtraukti. 

Taip pat proceso **Generuoti biudžeto planą pagal projekto prognozes** metu biudžeto plano eilutei priskiriamas šaltinio projektas.

### <a name="generate-budget-plan-from-supply-forecast"></a>Generuoti biudžeto planą pagal tiekimo prognozę

Šaltinio filtravimo parinktys, naudojamos proceso **Generuoti biudžeto planą pagal tiekimo prognozę**, buvo sukurtos pagal funkcijos **Perkelti pirkimo biudžetą į DK** parinktis dėl šio proceso ir funkcijos panašumo.

### <a name="generate-budget-plan-from-demand-forecast"></a>Generuoti biudžeto planą pagal poreikio prognozę

Jei vykdote procesą **Generuoti biudžeto planą pagal poreikio prognozę**, parinktį **Pardavimo užsakymas** galite nustatyti kaip **Taip**, kad biudžeto plane būtų generuojamos įplaukų eilutės, parinktį **Suvartojimas** nustatyti kaip **Taip**, kad būtų sukurtos išlaidų eilutės, arba abi pasirinktis nustatyti kaip **Taip**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Generuoti biudžeto planą iš biudžeto registro įrašų

Jei vykdote procesą **Generuoti biudžeto planą pagal biudžeto registro įrašus**, šaltinis turi nurodyti vieną submodelį, vieną biudžeto kodą ir vieną įrašo numerį. Kitaip tariant, vienu metu galite kurti tik vieno biudžeto registro įrašo biudžeto plano eilutes. Tame pačiame biudžeto plane galite naudoti papildomus įrašus, jei procesą vykdysite po vieną kartą kiekvienam šaltinio įrašui.

### <a name="generate-budget-plan-from-budget-plan"></a>Generuoti biudžeto planą iš biudžeto plano

Vykdant procesą **Generuoti biudžeto planą pagal biudžeto planą**, skirtuko **Paskirtis** papildomų parinkčių rinkinys suteikia galimybę priskirti naujas finansines dimensijas. Jei pasirinkta finansinė dimensija, ta reikšmė bus naudojama visose biudžeto plano eilutėse. Todėl vieną biudžeto planą galima naudoti kaip kitų biudžeto planų pagrindą, bet taip pat galima naujiems biudžeto planams priskirti, pavyzdžiui, kitą padalinį arba išlaidų centrą.

## <a name="looking-back-from-the-budget-plan"></a>Žvelgiant atgal iš biudžeto plano
### <a name="budget-plans-by-dimension-set-inquiry"></a>Užklausa Biudžeto planai pagal dimensijų rinkinį

Galima naudoti kelias užklausos **Biudžeto planai pagal dimensijų rinkinį** parinktis, norint pateikti užklausą biudžeto plano duomenų šaltiniui nustatyti. 

Pasirinkite eilutę ir spustelėkite mygtuką **Biudžeto plano eilutės**, norėdami pateikti užklausą **Biudžeto plano eilutės**. Rezultatai filtruojami pagal pasirinktos eilutės dimensijų reikšmes. Tada galite taikyti papildomus parametrus. 

Naudokite mygtukus **Tiekimo prognozė** ir **Poreikio prognozė** šioms užklausoms pateikti. Abiem atvejais užklausa ieško prognozės eilučių, kurios galėjo sukurti biudžeto plano eilutes. 

Galima naudoti vieną iš papildomų ataskaitų – **Prognozės pozicijos pagal biudžeto planą**. Ši ataskaita yra ypač naudinga, kai norite nustatyti, ar pozicija buvo tinkamai priskirta biudžeto planams.



