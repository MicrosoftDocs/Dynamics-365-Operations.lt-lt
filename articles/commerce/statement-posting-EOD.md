---
title: Išrašų registravimo funkcionalumo patobulinimai
description: Šioje temoje aprašomi išrašų registravimo funkcijai atlikti patobulinimai.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: be9aa68aec1fd7deff315234a6dbf41edc3d6819
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649024"
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

> [!NOTE]
> Nuo "Commerce" 10.0.14 versijos leidimo, kai **įgalinta "Retail" išrašų – informacijos santraukos** funkcija, **paketinė užduotis Registruoti atsargas** nebetaikoma ir jos negalima paleisti.

## <a name="processing"></a>Vykdoma

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

Registravimo proceso metu grynųjų pinigų ir nešiojimo operacijos sujungiamos pagal klientą ir produktą. Todėl sukuriamų pardavimo užsakymų ir eilučių skaičius sumažinamas. Agreguotos operacijos saugomos sistemoje ir naudojamos pardavimo užsakymams kurti. Kiekvieną kartą sutelkus operaciją sistemoje sukuriamas vienas atitinkamas pardavimo užsakymas. 

Jei išrašas nėra visiškai užregistruotas, išraše galite peržiūrėti apibendrintas operacijas. Veiksmų srities skirtuko Išrašas **grupėje Vykdymo informacija** pasirinkite **Agreguotos** operacijos **.**

![Nevisiškai užregistruoto išrašo agreguotų operacijų mygtukas.](media/aggregated-transactions.png)

Užregistruotų išrašų suvestines operacijas galite peržiūrėti puslapyje Užregistruotos **ataskaitos**. Veiksmų srityje pasirinkite **Užklausos**, tada pasirinkite **Agreguotos operacijos**.

![Užregistruotų išrašų agreguotų operacijų komanda.](media/aggregated-transactions-posted-statements.png)

Sumuotos **operacijos FastTab Pardavimo užsakymo informacija** rodoma ši informacija:

- **Įrašo ID** – sutelktos operacijos ID.
- **Išrašo numeris** – išrašas, kuriam sutelkta operacija priklauso.
- **Data** – sutelktos operacijos sukūrimo data.
- **Pardavimo ID** – kai pagal sutelktą operaciją sukuriamas pardavimo užsakymas, pardavimo užsakymo ID. Jei šis laukas tuščias, atitinkamas pardavimo užsakymas nesukurtas.
- **Sutelktų eilučių skaičius** – bendras sutelktos operacijos ir pardavimo užsakymo eilučių skaičius.
- **Būsena** – paskutinė sutelktos operacijos būsena.
- **Sąskaitos faktūros ID** – kai išrašoma sutelktos operacijos pardavimo užsakymo SF, pardavimo sąskaitos faktūros ID. Jei šis laukas tuščias, pardavimo užsakymo sąskaita faktūra užregistruota.
- **Klaidos kodas** – šis laukas nustatomas, jei agregavimas yra klaidos būsenoje.
- **Klaidos pranešimas** – šis laukas nustatomas, jei agregavimas yra klaidos būsenoje. Jame pateikiama išsami informacija apie tai, kas sukėlė proceso nesėkmę. Norėdami išspręsti problemą, galite naudoti klaidos kodo informaciją, tada iš naujo paleisti procesą rankiniu būdu. Atsižvelgiant į skiriamosios gebos tipą, suvestinius pardavimus gali tekti panaikinti ir apdoroti naujame pareiškime.

![Laukai, esantys agreguotos operacijos FastTab Pardavimo užsakymo informacija.](media/aggregated-transactions-error-message-view.png)

Agreguotos **operacijos FastTab Operacijos informacija** rodo visas operacijas, kurios buvo įtrauktos į agreguotą operaciją. Sutelktos operacijos sutelktose eilutėse rodomi visi sutelkti operacijų įrašai. Sutelktose eilutėse taip pat rodoma tokia išsami informacija kaip prekė, variantas, kiekis, kaina, grynoji suma, vienetas ir sandėlis. Iš esmės, kiekviena sutelkta eilutė atitinka vieną pardavimo užsakymo eilutę.

![Sukauptos operacijos informacijos FastTab.](media/aggregated-transactions-sales-details.png)

Kai kuriais atvejais agreguotos operacijos gali neužregistruoti konsoliduoto pardavimo užsakymo. Tokiais atvejais klaidos kodas bus susietas su išrašo būsena. Norėdami peržiūrėti tik sukauptas operacijas, kuriose yra klaidų, pažymėdami žymės langelį galite įgalinti **filtrą Rodyti tik gedimus** agreguotų operacijų rodinyje. Įjungę šį filtrą, rezultatus apribojate tik apibendrintomis operacijomis, kuriose yra klaidų, kurias reikia išspręsti. Informacijos apie tai, kaip ištaisyti šias klaidas, ieškokite [Redaguoti ir tikrinti užsakymą internetu ir asinchronines kliento užsakymo operacijas](edit-order-trans.md).

![Apibendrintų operacijų rodinio filtro Rodyti tik gedimus žymės langelis.](media/aggregated-transactions-failure-view.png)

**Puslapyje Agreguotos operacijos** galite atsisiųsti konkrečios agreguotos operacijos XML pasirinkdami **Eksportuoti agregavimo duomenis**. Galite peržiūrėti XML bet kuriame XML formatatoriuje, kad pamatytumėte faktinę duomenų informaciją, susijusią su pardavimo užsakymo kūrimu ir registravimu. Užregistruotų išrašų sutelktų operacijų XML failo atsisiuntimo funkcija naudotis negalima.

![Mygtukas Eksportuoti agregavimo duomenis puslapyje Agreguotos operacijos.](media/aggregated-transactions-export.png)

Jei negalite ištaisyti klaidos taisydami pardavimo užsakymo duomenis arba pardavimo užsakymą palaikančius duomenis, galimas mygtukas Naikinti kliento **užsakymą**. Norėdami panaikinti užsakymą, pasirinkite nepavykusią agreguotą operaciją, tada pasirinkite **Naikinti kliento užsakymą**. Tiek agreguota operacija, tiek atitinkamas pardavimo užsakymas bus panaikinti. Dabar galite peržiūrėti operacijas naudodami redagavimo ir audito funkciją. Arba jie gali būti apdorojami per naują pareiškimą. Ištaisę visas nesėkmes, galite tęsti išrašo registravimą vykdydami atitinkamo išrašo registravimo išrašo funkciją.

![Apibendrintų operacijų rodinyje esantį mygtuką Naikinti kliento užsakymą.](media/aggregated-transactions-delete-cust-order.png)

Suvestinių operacijų rodinyje pateikiami šie privalumai:

- Vartotojas gali matyti sutelktas operacijas, kurių nepavyko įvykdyti kuriant pardavimo užsakymą, ir pardavimo užsakymus, kurių nepavyko sukurti išrašant SF.
- Vartotojas gali matyti, kaip operacijos telkiamos.
- Vartotojas gali sekti visus patikrinimus, nuo operacijų, taip pat pardavimo užsakymų iki pardavimo SF. Tikrinimų nebuvo galima sekti naudojantis senesne išrašų registravimo funkcija.
- Agreguotas XML failas leidžia lengviau nustatyti problemas kuriant pardavimo užsakymą ir išrašant SF.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
