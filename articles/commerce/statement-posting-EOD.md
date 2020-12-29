---
title: Išrašų registravimo funkcionalumo patobulinimai
description: Šioje temoje aprašomi išrašų registravimo funkcijai atlikti patobulinimai.
author: josaw1
manager: AnnBe
ms.date: 05/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 68abef8f28c04a4f6f88e638c8abf944d06a32c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414418"
---
# <a name="improvements-to-statement-posting-functionality"></a>Išrašų registravimo funkcionalumo patobulinimai

[!include [banner](includes/banner.md)]

Šioje temoje aprašomas pirmas išrašų registravimo funkcijai atliktų patobulinimų rinkinys. Šie patobulinimai pateikiami „Microsoft Dynamics 365 for Finance and Operations 7.3.2“.

## <a name="activation"></a>Aktyvinimas

Pagal numatytuosius nustatymus, diegiant programą „Finance and Operations 7.3.2“ nustatoma, kad joje būtų naudojama senesnė išrašų registravimo funkcija. Norėdami įgalinti patobulintą išrašų registravimo funkciją, turite įjungti jos konfigūracijos raktą.

- Eikite į **Sistemos administravimas** \> **Sąranka** \> **Licencijos konfigūravimas**, po to mazge **Mažmeninė prekyba ir prekyba** panaikinkite žymės langelio **Išrašai (senesni)** žymėjimą ir pažymėkite žymės langelį **Mažmeninės prekybos išrašai**.

Įjungus naują srities **Išrašai** konfigūracijos raktą galima naudotis nauju meniu elementu, kurio pavadinimas **Išrašai**. Naudodamiesi šiuo meniu elementu galite patys sukurti, apskaičiuoti ir registruoti išrašus. Naudojantis šiuo meniu elementu taip pat bus galima matyti visus vykdant paketinį registravimą klaidas sukeliančius išrašus. (Įjungus srities **Išrašai (senesni)** konfigūracijos raktą meniu elemento pavadinimas **Atviri išrašai**.)

Naudojantis „Commerce“ atliekami toliau nurodyti su šiais konfigūracijos raktais siejami tikrinimai.

- Abiejų konfigūracijos raktų negalima įjungti tuo pačiu metu.
- Visoms atliekamoms nurodyto galiojančio išrašo operacijoms (kūrimo, skaičiavimo, naikinimo, registravimo ir t. t.) turi būti naudojami tie patys konfigūracijos raktai. Pavyzdžiui, kai įjungtas srities **Išrašai (senesni)** konfigūracijos raktas, negalite kurti ir skaičiuoti išrašo, o po to bandyti užregistruoti tą patį išrašą įjungę srities **Išrašai** konfigūracijos raktą.

> [!NOTE]
> Rekomenduojame naudotis srities **Išrašai** konfigūracijos raktu norint naudotis patobulinta išrašų registravimo funkcija, nebent esama svarių priežasčių naudotis srities **Išrašai (senesni)** konfigūracijos raktu. „Microsoft“ ir toliau investuos į naują ir patobulintą išrašų registravimo funkciją ir, norint ja pasinaudoti, svarbu kuo greičiau prie jos pereiti. Senesne išrašų registravimo funkcija nuo 8.0 leidimo nebebus naudojama.

## <a name="setup"></a>Sąranka

Tobulinant išrašų registravimo funkciją sukurti trys nauji puslapio **Prekybos parametrai** skirtuko **Registravimas** „FastTab“ skirtuko **Išrašas** parametrai.

- **Išjungti išrašų valymo funkciją** – ši parinktis taikoma tik naudojantis senesne išrašų registravimo funkcija. Rekomenduojame nustatyti šios parinkties reikšmę **Ne**, kad vartotojai negalėtų išvalyti išrašų, kurių būsena „pusiau užregistruoti“. Išvalius išrašus, kurių būsena „pusiau užregistruoti“, duomenys sugadinami. Šios parinkties reikšmę **Taip** turėtumėte nustatyti tik išskirtiniais atvejais.
- **Skaičiuojant rezervuoti atsargas** – norint rezervuoti atsargas rekomenduojame naudoti paketinę užduotį **Registruoti atsargas** ir nustatyti šios parinkties reikšmę **Ne**. Nustačius šios parinkties reikšmę **Ne** skaičiuojant ir naudojantis patobulinta išrašų registravimo funkcija nebandoma sukurti atsargų rezervavimo įrašų (jei įrašai nebuvo sukurti atliekant paketinę užduotį **Registruoti atsargas**). Naudojantis funkcija atsargų rezervavimo įrašai sukuriami tik registruojant. Šis diegimas atliktas norint įgyvendinti dizaino sprendimą ir buvo pagrįstas tuo, kad nuo skaičiavimo proceso iki registravimo proceso paprastai praeina nedaug laiko. Tačiau, jei norite rezervuoti atsargas, kai atliekamas skaičiavimas, galite nustatyti šios parinkties reikšmę **Taip**.

    Naudojantis senesne išrašo registravimo funkcija atsargos visada rezervuojamos vykstant išrašo skaičiavimo procesui (jei atsargos dar nerezervuotos atliekant paketinę užduotį **Registruoti atsargas**), nepriklausomai nuo to, kokia naudojama šios parinkties nuostata.

- **Reikia išjungti skaičiavimą** – nustačius šios parinkties reikšmę **Taip** išrašo registravimo procesas tęsiamas net jei skirtumas tarp išraše nurodytos apskaičiuotos sumos ir operacijos sumos yra didesnis negu parduotuvių „FastTab“ skirtuke **Išrašas** nurodyta ribinė reikšmė.

Be to, šie parametrai buvo įdiegti „FastTab“ skirtuke **Paketinis apdorojimas** skirtuke **Registravimas** puslapyje **Prekybos parametrai**. 

- **Maksimalus lygiagrečiai registruojamų išrašų skaičius** – šiame lauke apibrėžiamas paketinių užduočių, kurios bus naudojamos registruojant kelis išrašus, skaičius. 
- **Maksimalus užsakymų apdorojimo išrašui gijų skaičius** – šis laukas rodo maksimalų gijų skaičių, kurį naudoja paketinės užduoties išrašo registravimas, kad būtų galima kurti ir išrašyti vieno išrašo pardavimo užsakymus. Bendras gijų, kurias naudos išrašo registravimo procesas, skaičius bus apskaičiuojamas pagal šio parametro vertę, padaugintą iš vertės **Maksimalus lygiagrečiai registruojamų išrašų skaičius**. Nustačius per didelę šio parametro vertę galima neigiamai paveikti išrašo registravimo proceso efektyvumą.
- **Maksimalus operacijų eilučių skaičius telkime** – šiame lauke apibrėžiamas operacijų eilučių, kurios bus įtrauktos į vieną suvestinę operaciją prieš sukuriant naują, skaičius. Apibendrintos operacijos kuriamos remiantis skirtingais sumavimo kriterijais, pvz., klientais, darbo data ar finansinėmis dimensijomis. Svarbu pažymėti, kad viena operacijos eilutė nebus išskaidyta skirtingose suvestinėse operacijose. Tai reiškia, kad gali būti, kad suvestinės operacijos eilučių skaičius yra šiek tiek didesnis arba mažesnis, remiantis tokiais veiksniais, kaip atskirų produktų skaičius.
- **Didžiausias gijų, reikalingų parduotuvės operacijoms tikrinti, skaičius** – šiame lauke apibrėžiamas gijų, kurios bus naudojamos operacijoms tikrinti, skaičius. Operacijų tikrinimas yra būtinas veiksmas, kurį reikia atlikti prieš operacijas traukiant į išrašus. Be to, puslapio **Prekybos parametrai** skirtuko **Registravimas** „FastTab“ skirtuke **Dovanų kortelė** reikia apibrėžti elementą **Dovanų kortelės produktas**. Jį reikia apibrėžti, net jei organizacija dovanų kortelių nenaudoja.

> [!NOTE]
> Visi su išrašo registravimu susiję nustatymai ir parametrai, kurie nurodyti mažmeninės prekybos parduotuvėse ir puslapyje **Prekybos parametrai** taikomi naudojantis patobulinta išrašo registravimo funkcija.

## <a name="processing"></a>Vykdymas

Naudojantis meniu elementais **Skaičiuoti išrašų paketą** ir **Registruoti išrašų paketą** gali būti skaičiuojamas ir registruojamas išrašų paketas. Išrašai taip pat gali būti skaičiuojami ir registruojami neautomatiškai – naudojantis taikant patobulintą išrašų registravimo funkciją matomu meniu elementu **Išrašai**.

Išrašų paketo skaičiavimo ir registravimo procesas ir veiksmai yra tokie patys, kaip ir naudojantis senesne išrašo registravimo funkcija. Tačiau atlikta reikšmingų pagrindinio vidinio išrašų vykdymo patobulinimų. Dėl šių patobulinimų procesas lankstesnis, taip pat geriau matoma informacija apie būsenas ir klaidas. Todėl vartotojai gali pašalinti pagrindinę klaidų priežastį ir tęsti registravimo procesą nesugadindami duomenų, kad vėliau nereikėtų atlikti duomenų taisymų.

Toliau pateikiamuose skyriuose aprašomi kai kurie pagrindiniai vartotojo sąsajoje rodomų išrašų ir užregistruotų išrašų registravimo funkcijos patobulinimai.

### <a name="status-details"></a>Būsenos informacija

Sukurtas naujas išrašo skaičiavimo ir registravimo procesų būsenos modelis.

Toliau pateikiamoje lentelėje aprašomos įvairios būsenos ir kokia tvarka jos išdėstomos vykstant skaičiavimo procesui.

| Būsenų išdėstymo tvarka | Apskritis      | aprašymas |
|-------------|------------|-------------|
| 1           | Pradėta    | Išrašas sukurtas ir paruoštas skaičiuoti. |
| 2           | Pažymėta     | Išrašo apimties operacijos identifikuojamos pagal išrašo parametrus ir pažymimos nurodant išrašo ID. |
| 3           | Apskaičiuota | Išrašo eilutės apskaičiuotos ir rodomos. |

Toliau pateikiamoje lentelėje aprašomos įvairios būsenos ir kokia tvarka jos išdėstomos vykstant registravimo procesui.

| Būsenų išdėstymo tvarka | Apskritis                   | aprašymas |
|-------------|-------------------------|-------------|
| 1           | Patikrinta                 | Atliekami keli su parametrais (pavyzdžiui, perdavimo mokesčiu), taip pat su išrašu ir išrašo eilutėmis (pavyzdžiui, apskaičiuotos sumos ir operacijos sumos skirtumu) siejami tikrinimai. |
| 2           | Sukaupta              | Klientų, kurių vardai nurodyti arba nenurodyti, operacijos telkiamos pagal konfigūraciją. Kiekviena sutelkta operacija galiausiai konvertuojama į pardavimo užsakymą. |
| 3           | Kliento užsakymas sukurtas  | Pagal sutelktą operaciją sistemoje sukuriami pardavimo užsakymai. |
| 4           | Išrašyta kliento užsakymo SF | Išrašytos pardavimo užsakymų SF. |
| 5           | Nuolaidos užregistruotos        | Periodiniai nuolaidų žurnalai registruojami pagal konfigūraciją. |
| 6           | Pajamos / išlaidos užregistruotos   | Pajamų / išlaidų operacijos registruojamos kaip kvitai. |
| 7           | Kvitai susieti         | Mokėjimo žurnalai sukurti ir susieti su atitinkama sąskaita faktūra. |
| 8           | Mokėjimai užregistruoti         | Mokėjimo žurnalai užregistruoti. |
| 9           | Užregistruotos dovanų kortelės       | Dovanų kortelės operacijos registruojamos kaip kvitai. |
| 10          | Užregistruota                  | Išrašas pažymėtas kaip užregistruotas. |

Kiekviena pirmiau pateiktose lentelėse nurodyta būsena pagal pobūdį yra nepriklausoma, sukuriama hierarchinė būsenų priklausomybė. Tai priklausomybė, kuri juntama iš viršaus į apačią. Jei vykdydama būseną sistema aptinka klaidų, grąžinama ankstesnė išrašo būsena. Kiekvieną kartą bandant iš naujo vykdyti procesą tęsiama nuo būsenos, kurios nepavyko įvykdyti ir judama pirmyn. Toliau nurodomi šio metodo privalumai.

- Vartotojas mato visą būseną, kurią vykdant įvyko klaida.
- Duomenys išlieka nesugadinti. Pavyzdžiui, naudojantis senesne išrašo registravimo funkcija buvo atvejų, kai SF išrašomos tik kai kuriems pardavimo užsakymams, o kiti užsakymai lieka atviri. Taip pat buvo atvejų, kai kai kuriuose mokėjimo žurnaluose nebuvo nurodyta atitinkama SF, kurią reikia apmokėti, nes registruojant SF įvyko klaida.
- Naudodamiesi išrašo grupės **Išsami informacija apie vykdymą** mygtuku **Išsami informacija apie būseną** vartotojai gali matyti dabartinę išrašo būseną. Išsamios informacijos apie būseną puslapyje yra trys skyriai.

    - Pirmame skyriuje rodoma dabartinė išrašo būsena, taip pat klaidos kodas ir (įvykus klaidai) išsamus pranešimas apie klaidą.
    - Antrame skyriuje rodomos įvairios skaičiavimo proceso būsenos. Vaizdinėse užuominose nurodomos sėkmingai paleistos būsenos, būsenos, kurių nepavyko paleisti dėl klaidų, ir būsenos, kurios dar nepaleistos.
    - Trečiame skyriuje rodomos įvairios registravimo proceso būsenos. Vaizdinėse užuominose nurodomos sėkmingai paleistos būsenos, būsenos, kurių nepavyko paleisti dėl klaidų, ir būsenos, kurios dar nepaleistos.

Be to, antro ir trečio skyrių antraštėse rodoma bendroji atitinkamo proceso būsena.

### <a name="event-logs"></a>Įvykių žurnalai

Atliekamos įvairios išrašo operacijos (pavyzdžiui, kūrimo, skaičiavimo, valymo ir registravimo) ir išrašo galiojimo laikotarpiu gali būti pateikiami keli tos pačios operacijos pavyzdžiai. Pavyzdžiui, sukūręs ir apskaičiavęs išrašą vartotojas gali išvalyti išrašą ir apskaičiuoti jį dar kartą. Naudojantis išrašo grupės **Išsami informacija apie vykdymą** mygtuku **Įvykių žurnalai** galima gauti visą informaciją apie įvairių išraše nurodytų operacijų patikrinimus, taip pat informaciją apie tai, kada nurodyta tas operacijas atlikti.

### <a name="aggregated-transactions"></a>Sutelktos operacijos

Vykstant registravimo procesui pardavimo operacijos telkiamos pagal konfigūraciją. Šios sutelktos operacijos saugomos sistemoje ir naudojamos pardavimų užsakymams kurti. Kiekvieną kartą sutelkus operaciją sistemoje sukuriamas vienas atitinkamas pardavimo užsakymas. Naudodamiesi išrašo grupės **Išsami informacija apie vykdymą** mygtuku **Sutelktos operacijos** galite peržiūrėti sutelktas operacijas.

Sutelktos operacijos skirtuke **Išsami informacija apie pardavimo užsakymą** rodoma toliau išvardyta informacija.

- **Įrašo ID** – sutelktos operacijos ID.
- **Išrašo numeris** – išrašas, kuriam sutelkta operacija priklauso.
- **Data** – sutelktos operacijos sukūrimo data.
- **Pardavimo ID** – kai pagal sutelktą operaciją sukuriamas pardavimo užsakymas, pardavimo užsakymo ID. Jei šis laukas tuščias, atitinkamas pardavimo užsakymas nesukurtas.
- **Sutelktų eilučių skaičius** – bendras sutelktos operacijos ir pardavimo užsakymo eilučių skaičius.
- **Būsena** – paskutinė sutelktos operacijos būsena.
- **Sąskaitos faktūros ID** – kai išrašoma sutelktos operacijos pardavimo užsakymo SF, pardavimo sąskaitos faktūros ID. Jei šis laukas tuščias, pardavimo užsakymo sąskaita faktūra užregistruota.

Sutelktos operacijos skirtuke **Išsami informacija apie operaciją** rodomos visos į sutelktą operaciją įtrauktos operacijos. Sutelktos operacijos sutelktose eilutėse rodomi visi sutelkti operacijų įrašai. Sutelktose eilutėse taip pat rodoma tokia išsami informacija kaip prekė, variantas, kiekis, kaina, grynoji suma, vienetas ir sandėlis. Iš esmės, kiekviena sutelkta eilutė atitinka vieną pardavimo užsakymo eilutę.

Puslapyje **Sutelktos operacijos** naudodamiesi mygtuku **Eksportuoti pardavimo užsakymo XML failą** galite atsisiųsti tam tikros sutelktos operacijos XML failą. Naudodamiesi XML failu galite išspręsti su pardavimo užsakymo kūrimu ir registravimu susijusias problemas. Tiesiog atsisiųskite XML failą, įkelkite jį į bandomąją aplinką ir išspręskite problemą bandomojoje aplinkoje. Užregistruotų išrašų sutelktų operacijų XML failo atsisiuntimo funkcija naudotis negalima.

Sutelktos operacijos rodinyje nurodoma toliau išvardyta nauda.

- Vartotojas gali matyti sutelktas operacijas, kurių nepavyko įvykdyti kuriant pardavimo užsakymą, ir pardavimo užsakymus, kurių nepavyko sukurti išrašant SF.
- Vartotojas gali matyti, kaip operacijos telkiamos.
- Vartotojas gali sekti visus patikrinimus, nuo operacijų, taip pat pardavimo užsakymų iki pardavimo SF. Tikrinimų nebuvo galima sekti naudojantis senesne išrašų registravimo funkcija.
- Naudojantis sutelktu XML failu lengviau nustatyti problemas kuriant pardavimo užsakymą ir išrašant sąskaitas faktūras.

### <a name="journal-vouchers"></a>Žurnalo kvitai

Naudojantis išrašo grupės **Išsami informacija apie vykdymą** mygtuku **Žurnalo kvitai** rodomos visos įvairios sukurtos išrašo kvito operacijos, kurios susijusios su nuolaidomis, pajamų / išlaidų sąskaitomis, dovanų kortelėmis ir t. t.

Šiuo metu programoje rodomi tik registruotų išrašų duomenys.

### <a name="payment-journals"></a>Mokėjimo žurnalai

Paspaudus išrašo grupės **Išsami informacija apie vykdymą** mygtuką **Mokėjimo žurnalai** rodomi visi įvairūs sukurti išrašo mokėjimo žurnalai.

Šiuo metu programoje rodomi tik registruotų išrašų duomenys.

## <a name="other-improvements"></a>Kiti patobulinimai

Kiti vidiniai vartotojų matomi išrašų registravimo funkcijai atlikti patobulinimai. Štai keletas pavyzdžių:

- Telkimas neapima darbuotojų, terminalo ir pamainų objektų. Kadangi yra mažiau telkimo parametrų, turi būti vykdoma mažiau pardavimo užsakymo eilučių.
- Operacijų lentelėse atsirandančių aklaviečių skaičius sumažės sukūrus papildomas išplėstines lenteles ir operacijų lentelėse vietoje atnaujinimo operacijų atliekant įterpimo operacijas.
- Vykdomų paketinių užduočių skaičiui taikomi atitinkami parametrai ir jis ribotas. Todėl šis skaičius gali būti specialiai priderinamas pagal kliento aplinką. Naudojantis senesne išrašų registravimo funkcija vienu metu buvo sukuriamas neribotas paketinių užduočių skaičius. Rezultatai – nevaldomos apkrovos, pridėtinės išlaidos ir silpnosios vietos paketinio apdorojimo serveryje.
- Išrašai efektyviai išrikiuojami į eilę apdorojimui, pirmenybę suteikiant tiems išrašams, kuriuose operacijų skaičius didžiausias.
- Paketiniai procesai, pavyzdžiui, **Skaičiuoti išrašų paketą** ir **Registruoti išrašų paketą** vykdomi tik įjungus paketinį režimą. Naudodamiesi senesne išrašų registravimo funkcija vartotojai galėjo pasirinkti, kad šie paketiniai procesai būtų vykdomi interaktyviuoju režimu, t. y. kaip vienos gijos operacija, priešingai negu kelių gijų paketiniai procesai.
- Naudojantis senesne išrašų registravimo funkcija dėl bet kokios paketinės užduoties klaidos visa paketinė užduotis būdavo klaidos būsenos. Naudojantis patobulinta funkcija, jei pavyksta sėkmingai atlikti kitas paketines užduotis, dėl paketinės užduoties klaidų nerodoma, kad paketinė užduotis yra klaidos būsenos. Turėtumėte įvertinti paketinio vykdymo, atliekamo naudojantis puslapiu **Išrašai**, kuriame galite matyti visus dėl klaidų neužregistruotus išrašus, registravimo būseną.
- Naudojantis senesne išrašų registravimo funkcija po pirmo išrašo klaidos atvejo nepavyksta užregistruoti viso paketo. Likę išrašai nevykdomi. Naudojantis patobulinta funkcija ir atliekant paketinį vykdymą vykdomi visi išrašai, net jei kai kurių išrašų užregistruoti nepavyksta. Vienas privalumas – vartotojai mato tikslų išrašų, kuriuose esama klaidų, skaičių. Todėl vartotojams nėra būtina nuolat taisyti klaidas ir tol vykdyti išrašo registravimo procesą, kol užregistruojami visi išrašai.

## <a name="general-guidance-about-the-statement-posting-process"></a>Bendrieji nurodymai dėl išrašų registravimo proceso

- Rekomenduojame vykdyti išrašų paketo registravimo procesą, nes vykdant paketinius procesus galima pasinaudoti paketinės sistemos pranašumu, kadangi naudojamas kelių gijų režimas. Naudotis kelių gijų režimu reikia tam, kad būtų galima tvarkyti didelį kiekį operacijų, kurios paprastai rodomos atliekant išrašo registravimą.
- Norint, kad registravimas būtų nuoseklus, rekomenduojame įjungti neigiamas faktines prekių modelio grupės atsargas. Kai kuriais atvejais gali nepavykti užregistruoti neigiamų išrašų nenurodžius neigiamų faktinių atsargų. Pavyzdžiui, teoriškai, jei atsargose yra tik viena prekė ir buvo vykdomos tos prekės pardavimo ir grąžinimo operacijos, operaciją turėtų pavykti užregistruoti net ir tuo atveju, jei neigiamos atsargos neįjungtos. Tačiau, kadangi vykstant išrašo registravimo procesui į vieną kliento užsakymą įtraukiama ir pardavimo operacija, ir grąžinimo operacija, pardavimo eilutė nebūtinai bus užregistruota pirma, o po jos – grąžinimo eilutė. Todėl gali įvykti klaidų. Jei šioje situacijoje įjungiamos neigiamos atsargos, tai neturi neigiamos įtakos registruojant operaciją ir sistema atsargas nurodys teisingai.
- Skaičiuojant ir registruojant išrašus rekomenduojame naudotis telkimo funkcija. Taip pat rekomenduojame naudoti toliau nurodytas kai kurių telkimo parametrų nuostatas.

    - Eikite į **Mažmeninė prekyba ir prekyba** \> **Būstinės sąranka** \> **Parametrai** \> **Prekybos parametrai**. Po to skirtuko **Registravimas** „FastTab“ skirtuko **Atsargų atnaujinimas** lauke **Detalumo lygis** pasirinkite **Suvestinė**.
    - Eikite į **Mažmeninė prekyba ir prekyba** \> **Būstinės sąranka** \> **Parametrai** \> **Prekybos parametrai**. Po to skirtuko **Registravimas** „FastTab“ skirtuke **Telkimas** nustatykite parinkties **Kvito operacijos** reikšmę **Taip**.
