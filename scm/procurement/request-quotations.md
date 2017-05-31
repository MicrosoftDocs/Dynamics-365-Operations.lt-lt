---
title: "Pasiūlymo patvirtinimai (RFQ)"
description: "Šiame straipsnyje apžvelgiamos pasiūlymo užklausos (RFQ), kurias organizacijos išduoda, kai turi pirkti prekes arba paslaugas ir gauti konkurencingų pasiūlymų iš kelių tiekėjų. RFQ tiekėjų prašoma pateikti nurodyto prekių kiekio kainas ir pristatymo laiką. Be to, galite paprašyti tiekėjų nurodyti, ar bus papildomų išlaidų, pvz., siuntimo išlaidų, arba nuolaidų didelių užsakymų ar ankstyvo tiekėjo SF apmokėjimo atveju."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d681f4c107a9dbc1ea8c5e1de38b2d45cf19bcfa
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="request-for-quotations-rfqs"></a>Pasiūlymo patvirtinimai (RFQ)

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgiamos pasiūlymo užklausos (RFQ), kurias organizacijos išduoda, kai turi pirkti prekes arba paslaugas ir gauti konkurencingų pasiūlymų iš kelių tiekėjų. RFQ tiekėjų prašoma pateikti nurodyto prekių kiekio kainas ir pristatymo laiką. Be to, galite paprašyti tiekėjų nurodyti, ar bus papildomų išlaidų, pvz., siuntimo išlaidų, arba nuolaidų didelių užsakymų ar ankstyvo tiekėjo SF apmokėjimo atveju.

Pasiūlymo patvirtinimo (RFQ) procesas apima šias užduotis:

-   RFQ kūrimas ir siuntimas vienam ar keliems tiekėjams
-   RFQ atsakymų (kainų pasiūlymų) gavimas ir registravimas
-   Priimtų kainų pasiūlymų perkėlimas į pirkimo užsakymą, pirkimo sutartį ar pirkimo paraišką

Toliau esančiame paveikslėlyje pateikiama RFQ proceso apžvalga.  

[![Pasiūlymo patvirtinimo procesas](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Galite sukurti RFQ iš suplanuotų užsakymų, pirkimo paraiškos arba įvesti rankiniu būdu. Jūsų kuriamas RFQ vadinamas RFQ atveju ir tai yra pagrindinis dokumentas, naudojamas išduodant RFQ kiekvienam tiekėjui. Parengę RFQ atvejį ir įtraukę į RFQ atvejį tiekėjų spustelėkite **Siųsti** ir bus sukurtas kiekvieno tiekėjo, kuriam nusiuntėte RFQ, RFQ žurnalas. Galite konfigūruoti siuntimo veiksmo spausdinimo valdymo parametrą, kad kiekvieno tiekėjo ataskaita būtų spausdinama arba siunčiama kiekvieno tiekėjo el. pašto adresu. Be to, naudojant kiekvieno tiekėjo RFQ žurnalą galima generuoti ataskaitą, kurią galima siųsti arba pakartotinai siųsti tiekėjui vėliau. Taip pat galite konfigūruoti siuntimo veiksmą, kad būtų sugeneruotas atsakymo lapas, kurį tiekėjas gali užpildyti.  

Jei reikia keisti RFQ išsiuntus dokumentą, galite pakartotinai siųsti RFQ tiekėjams, kai baigsite.  

Gavę pasiūlymų, turite įvesti juos į puslapį **Pasiūlymų patvirtinimų atsakymai**. Jei pasirinksite parinktį **Kopijuoti duomenis į atsakymą**, duomenys, pvz., kiekis ir datos, iš RFQ atvejo nukopijuojami į atsakymą. Galite keisti šiuos duomenis, kad jie atspindėtų tiekėjo pasiūlymą.  

Jei reikalingas tam tikro tiekėjo antras atsakymo pakartojimas, puslapyje**Pasiūlymo patvirtinimo atsakymas** spustelėkite **Grąžinti**. Grąžinimo veiksmas sugeneruoja naują žurnalą ir ataskaitą, kuri bus išspausdinta, archyvuota ir išsiųsta pagal jūsų spausdinimo valdymo parametrus.  

Jei į RFQ atvejį įtraukiate vertinimo kriterijų, RFQ atsakymas turės vertinimo sritį, kurioje galima įvesti rezultatus. Bendras rezultatas bus rodomas, kai palyginsite atsakymus puslapyje **Palyginti atsakymus**, kur taip pat galima palyginti kitus atsakymų duomenis, pvz., eilutės kainą, pristatymo datą ir bendrąją kainą.  

Nusprendę dėl kainos pasiūlymo arba dalinio kainos pasiūlymo, galite juos priimti ir atmesti likusius. Generuojami priėmimo žurnalai, atmetimo žurnalai ir atitinkamos ataskaitos. Jie bus išspausdinti, archyvuoti ir išsiųsti pagal jūsų spausdinimo valdymo parametrus. Priėmus kainos pasiūlymą arba konkrečias kainos pasiūlymo eilutes sugeneruojama pirkimo sutartis arba pirkimo užsakymas arba atnaujinama pirkimo paraiška, atsižvelgiant į RFQ pirkimo tipą. Galite sukurti prekybos sutartį, kurią vėliau galėsite naudoti bet kuriuose atsakymuose, nepaisant to, ar juos priėmėte, ar atmetėte.  

RFQ būsena rodoma RFQ antraštėje ir priklauso nuo RFQ eilučių būsenos. Būsena nurodo, kiek RFQ jau apdorotas. Kiekvienas RFQ turi dvi būsenos vertes: mažiausią ir didžiausią. Mažiausia būsena yra mažiausiai pažengęs etapas iš visų RFQ eilučių, o didžiausia būsena yra labiausiai pažengęs etapas iš visų RFQ eilučių. Pavyzdžiui, jei sukurtai eilutei galioja mažiausiai pažengęs RFQ etapas, mažiausia RFQ būsena yra **Sukurta**. Jei RFQ eilutės labiausiai pažengęs etapas yra išsiuntimas tiekėjui, aukščiausia RFQ būsena bus **Išsiųsta**. Būsenos atnaujinamos automatiškai, apdorojant RFQ.  

Galite peržiūrėti mažiausią ir didžiausią būsenas RFQ antraštėje sąrašo puslapyje **Visi pasiūlymų patvirtinimai**. Galite peržiūrėti mažiausią ir didžiausią RFQ eilutės būsenas puslapio **Pasiūlymo patvirtinimai** skirtuke **Eilutės**.  

RFQ apdorojimo būsenų seka:

1.  **Sukurta**
2.  **Išsiųsta**
3.  **Gauta**
4.  **Priimta**/**Atšaukta**/**Atmesta**

Būsenos bus išsamiau aprašytos vėlesniuose šio straipsnio skyriuose.

## <a name="setting-up-rfq-functionality"></a>RFQ funkcijų nustatymas
Prieš kurdami RFQ atvejį, turite nustatyti RFQ informaciją puslapyje **Paraiškų parametrai**. Kai kuriate yra RFQ atvejį, galite nurodyti numatytąsias vertes, kurios yra kopijuojamos į RFQ. Galite nurodyti šias numatytąsias vertes:

-   Naujų RFQ pirkimo tipas: **Pirkimo užsakymas** arba **Pirkimo sutartis**
-   Galiojimo pabaigos datos ir laiko parametrai
-   Pristatymo informacija ir mokėjimo sąlygos.
-   Laukai, kuriuos reikia įtraukti į RFQ atsakymą

Galite nepaisyti šių verčių konkrečiame RFQ atvejyje. Taip pat turite sukonfigūruoti pakeitimo procesą. Kaip šios konfigūracijos dalį galite įjungti lauko blokavimo funkciją. Kai įjungta lauko blokavimo funkcija, įsigijimo specialistas, kuris nori pakeisti RFQ, pirma turi spustelėti mygtuką **Kurti**, esantį skirtuko **Pasiūlymas** dalyje **Pakeitimas**. Atnaujinus RFQ pakeitimu įsigijimo specialistas turi užbaigti procesą spustelėdamas **Baigti**.** **Atlikus baigimo veiksmą sugeneruojamas el. laiškas, kuriuo tiekėjams pranešama apie pakeistą RFQ. Pasirinkite tiekėjui siunčiamo el. pašto pranešimo šabloną puslapyje **Paraiškų parametrai**. Kai sukuriamas šablonas, jame gali būti tokių pakeitimo atpažinimo ženklų:

-   %Kainos pasiūlymo grąžinimo priežastis%
-   %Pakeitimo priežastis%
-   %Pakeitimą parengė%
-   %Įmonė%

Atpažinimo ženklus %Kainos pasiūlymo grąžinimo priežastis% ir %Pakeitimo priežastis% įsigijimo specialistas pakeičia tekstu, kurį gali įvesti atlikęs šiuos pakeitimus naudodamas vedlį **Pakeitimas**. Atpažinimo ženklų %Pakeitimą parengė% ir %Įmonė% vertės automatiškai paimamos iš RFQ.  

Jei RFQ atsakyme siekdami nurodyti, kodėl pasiūlymas buvo atmestas ar priimtas, norite naudoti priežasčių kodus, turite nustatyti priežasčių kodus puslapyje **Tiekėjų priežastys**.  

Galite konfigūruoti išspausdintų arba saugomų RFQ dokumentų išvaizdą dalies Paraiškos puslapyje **Formos nustatymas**.  

Kai sukuriate pirkimo užsakymo RFQ ir prie RFQ pridedate atsargų prekę, sugeneruojama atsargų operacija, kurios gavimo būsena yra **Pasiūlymo gavimas**. Kai naudojate bendrąjį planą apskaičiuodami atsargas, atsižvelgiama tik į šios būsenos RFQ eilutes. Jei norite, kad į bendrąjį planą kaip numatomas gavimas būtų įtrauktos RFQ eilutės, turite sukonfigūruoti šią veikseną bendrojo planavimo nustatyme.  

Kaip pirkimo vadovas ar agentas galite kurti ir tvarkyti siūlymų tipus, kad atitiktų jūsų organizacijos įsigijimo poreikius. Kiekvieno siūlymo tipas gali veikti vertinimo metodus. Vertinimo metodus sudaro tam tikri kriterijai, kuriuos galima naudoti vertinant kainos pasiūlymus. Siūlymų tipus, vertinimo būdus ir vertinimo kriterijus turite nustatyti puslapiuose **Siūlymo tipas** ir **Vertinimo būdas**.

## <a name="creating-and-sending-an-rfq"></a>RFQ kūrimas ir siuntimas
Sukuriate RFQ, pasirenkate tiekėjus, kurių kainų pasiūlymus norite gauti į RFQ, ir išsiunčiate RFQ tiekėjams. Spausdinimo valdymą galite naudoti, kad nukreiptumėte RFQ ataskaitas ir atsakymų lapų ataskaitas į pasirinktą vietą.  

RFQ galite sukurti pirkimo tipui **Pirkimo užsakymas** arba **Pirkimo sutartis**.  

Jei RFQ generuojamas iš pirkimo paraiškos, automatiškai priskiriamas tipas **Pirkimo paraiška**. Negalima neautomatiniu būdu sukurti tipo **Pirkimo paraiška** RFQ. Jei RFQ tipas yra **Pirkimo užsakymas**:

-   Kuriant RFQ eilutes generuojamos atsargų operacijos, kurių gavimo būsena yra **Pasiūlymo gavimas**.
-   Priėmus kainos pasiūlymą generuojamas pirkimo užsakymas.

Jei RFQ tipas yra **Pirkimo sutartis**:

-   RFQ naudojamas kaip sutartis tam tikram produkto kiekiui arba vertei pirkti per tam tikrą laikotarpį. Turite pasirinkti datų intervalą, kuris bus taikomas pirkimo sutarčiai, ir asmens, kuris valdo pirkimo sutartį, vardą.
-   Priėmus kainos pasiūlymą generuojama pirkimo sutartis.

RFQ iš pirkimo paraiškos galite sukurti tik jei pirkimo paraiškos būsena yra **Peržiūrima**ir jūs esate priskirti atlikti kitą darbo eigos užduotį. Pirkimo paraiškos eilutės naujinamos automatiškai, kai priimate eilutes iš RFQ atsakymų (kainos pasiūlymų), kuriuos gavote iš tiekėjų. Negalite užbaigti, atmesti ir patvirtinti pirkimo paraiškos arba atlikti su ja kitų veiksmų, kai vykdomas RFQ.  

Kai kuriate RFQ, galite pasirinkti konkretų siūlymo tipą. Pagal siūlymo tipą nustatomas vertinimo kriterijų rinkinys, naudojamas RFQ atsakymams vertinti.  

Prie RFQ atvejo galite pridėti klausimyną. Šis klausimynas rodomas visuose atsakymuose išsiuntus RFQ.  

Pasirinkti tiekėjus, įtrauktinus į RFQ atvejį, galima trimis būdais:

-   Įtraukti tiekėjus po vieną.
-   Ieškoti visų tiekėjų, atitinkančių nurodytus kriterijus.
-   Automatiškai įtraukti visus tiekėjus, patvirtintus pagal įsigijimo kategorijas, naudojamas RFQ eilutėse.

Kai RFQ atvejis bus paruoštas, spustelėkite **Siųsti**. Siuntimo veiksmas sugeneruoja žurnalus ir ataskaitas, kurie bus išspausdinti, archyvuoti ir išsiųsti pagal jūsų spausdinimo valdymo parametrus.  

Jei išsiųsdami užklausą tiekėjams puslapyje **Pasiūlymo patvirtinimo siuntimas** pažymėjote žymės langelius **Naudoti tiekėją perskaičiuojant kainas** ir **Naudoti prekių informaciją pagal tiekėją**, tam tikra konkretaus tiekėjo informacija įvedama automatiškai. Šią informaciją galima modifikuoti puslapyje **Pasiūlymo patvirtinimo atsakymas**.  

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena, kai sukuriate RFQ ir siunčiate ją tiekėjams.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Veiksmas**                         | **Žemiausia RFQ antraštės būsena** | **Aukščiausia RFQ antraštės būsena**                   | **Žemiausia RFQ eilutės būsena** | **Aukščiausia RFQ eilutės būsena** |
| Sukurkite RFQ antraštę ir eilutę.    | Sukurta                      | Sukurta                                         | Sukurta                    | Sukurta                     |
| Siųskite RFQ konkrečiam tiekėjui. | Išsiųsta                         | Išsiųsta                                            | Išsiųsta                       | Išsiųsta                        |
| Pridėti kitą tiekėją.                | Sukurta                      | Išsiųsta (RFQ išsiųstas tik vienam tiekėjui.) | Sukurta                    | Išsiųsta                        |
| Išsiųsti RFQ antram tiekėjui. | Išsiųsta                         | Išsiųsta                                            | Išsiųsta                       | Išsiųsta                        |

**Pastaba.** Galite į RFQ įtraukti daugiau tiekėjų bet kuriuo metu ir mažiausia bei didžiausia būsenos pasikeis, atspindėdamos naujus tiekėjus. Pavyzdžiui, jei gavote pasiūlymus iš visų tiekėjų ir priėmėte bent pasiūlymo vieną eilutę, žemiausia būsena RFQ antraštėse bus **Atmesta**, o aukščiausia būsena – **Priimta**. Jeigu įtraukiate naują tiekėją, žemiausia bet kurios eilutės būsena yra **Sukurta**. Todėl žemiausia būsena RFQ antraštėje pakeičiama į **Sukurta**, o aukščiausia būsena lieka **Priimta**.

## <a name="amending-an-rfq"></a>RFQ keitimas
Kartais turite pakeisti RFQ jį išsiuntę. Tai gali įvykti, nes, pvz., pasikeitė pristatymo datos, norite papildomų produktų arba kitokio produktų kiekio. Galite konfigūruoti pakeitimo procesą, kad jis būtų labiau arba mažiau ribojamas.  

Jei pasirenkate labiau ribojamą pakeitimo procesą, RFQ atvejyje turite spustelėti **Kurti**, kad pradėtumėte pakeitimą prieš keisdami RFQ atvejo laukus. Atlikę pakeitimus turite spustelėti **Baigti**. Jums bus pateikiami nurodymai, kaip įtraukti informaciją į el. pašto pranešimą, siunčiamą norint perspėti tiekėjus apie pakeitimą. Atnaujinta RFQ ataskaita, kurioje yra pastaba apie pakeitimą, automatiškai pridedama prie pranešimo.  

Jei pasirenkate mažiau ribojamą pakeitimo procesą, neturite sukurti pakeitimo prieš keisdami jau išsiųsto RFQ atvejo laukus. Tačiau turite patys į RFQ atvejį įtraukti pakeitimo pastabą.

## <a name="receiving-and-registering-rfq-replies"></a>RFQ atsakymų gavimas ir registravimas
Siunčiant RFQ atsakymo lapas bus sugeneruotas automatiškai. Gavę atsakymus (kainos pasiūlymus) į RFQ, turite įvesti kiekvieno tiekėjo informaciją konkretaus tiekėjo RFQ atsakymo lape. Jei įtraukėte vertinimo kriterijų, galite atsakymus įvertinti. Tada galite palyginti tiekėjų kainų pasiūlymus ir įvertinti juos pagal savo vertinimo kriterijus, pvz., geriausią bendrąją kainą arba geriausią bendrąjį pristatymo laiką.  

Jei į RFQ atvejį įtrauktas klausimynas, turite patys įvesti atsakymus į klausimus atsakymo lape.  

Jei reikia įtraukti alternatyvių eilučių ir RFQ atvejyje tai leidžiama, „FastTab“ skirtuke **Pirkimo pasiūlymo eilutės** spustelėkite **Įtraukti eilutę**. Tada įveskite informaciją apie produktą, pvz., prekės numerį arba įsigijimo kategoriją, kiekį, kainą ir nuolaidą.  

Jeigu įvedėte atsakymą, bet jums reikalingas naujas tiekėjo pasiūlymas, galite RFQ persiųsti. Taip bus sukurti nauji žurnalas ir ataskaita, kuriuos galite naudoti prašyti pakeitimų iš tiekėjo.  

Galite matyti visų RFQ ir jų atsakymų būsenų peržiūrą puslapyje **Pasiūlymo patvirtinimo stebėjimas**.  

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena gaunant kainų pasiūlymus ir registruojant informaciją RFQ atsakymo lape.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Veiksmas**                                     | **Žemiausia kainos pasiūlymo būsena** | **Aukščiausia kainos pasiūlymo būsena** | **Žemiausia RFQ antraštės būsena** | **Aukščiausia RFQ antraštės būsena** | **Žemiausia RFQ eilutės būsena** | **Aukščiausia RFQ eilutės būsena** |
| Užregistruoti vieno tiekėjo kainos pasiūlymą ir jį išsaugoti.        | Išsiųsta                  | Gauta               | Išsiųsta                         | Gauta                      | Išsiųsta                       | Gauta                    |
| Užregistruoti antro tiekėjo kainos pasiūlymą ir jį išsaugoti. | Gauta              | Gauta               | Gauta                     | Gauta                      | Gauta                   | Gauta                    |

**Pastaba.** Jei grąžinsite kainos pasiūlymą tiekėjui tolesnėms deryboms, žemiausia ir aukščiausia būsenos liks **Gauta**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Kainos pasiūlymų priėmimas ir atmetimas bei priimtų kainos pasiūlymų perkėlimas į tolesnius dokumentus

Radę geriausią kainos pasiūlymą, pvz., pasiūlymą su geriausia bendrąja kaina, jį priimkite. To tiekėjo RFQ atsakymo būsena atnaujinama į **Priimta**. Kai priimate kainos pasiūlymą arba konkrečias kainos pasiūlymo eilutes, automatiškai sugeneruojamas pirkimo užsakymas ar pirkimo sutartis, o jūs galite atmesti kitų tiekėjų kainų pasiūlymus.  

Kai priimate RFQ atsakymą, kurio tipas yra **Pirkimo paraiška**, RFQ atsakymo eilutės atnaujina toliau nurodytą pirkimo paraiškos eilučių informaciją.

-   Vnt. kaina
-   Nuolaida procentais
-   Nuolaidos suma
-   Pirkimo mokesčiai
-   Eilutės išlaidos
-   Tiekėjas
-   Išorinis skaičius
-   Išorinis aprašymas

Atsakyme galite įtraukti priežasties kodą, norėdami paaiškinti, kodėl priimtas arba atmestas kainos pasiūlymas.  

Galite priimti kai kurias kainos pasiūlymo eilutes ir atmesti kitas. Taip pat galite priimti eilutes iš įvairių tiekėjų. Tik turėkite omenyje, kad, jei priimate kai kurias eilutes, būsite paraginti atmesti visas kitas. Todėl, jei norite priimti kitų eilučių, gavę raginimą turite spustelėti **Atšaukti**.  

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena, kai priimate ir atmetate tiekėjų kainos pasiūlymus.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Veiksmas**              | **Žemiausia kainos pasiūlymo būsena** | **Aukščiausia kainos pasiūlymo būsena** | **Žemiausia RFQ antraštės būsena** | **Aukščiausia RFQ antraštės būsena** | **Žemiausia RFQ eilutės būsena** | **Aukščiausia RFQ eilutės būsena** |
| Priimti vieną pasiūlymų. | Gauta              | Priimta               | Gauta                     | Priimta                      | Gauta                   | Priimta                    |
| Atmesti kitus kainos pasiūlymus.  | Atmesta              | Priimta               | Atmesta                     | Priimta                      | Atmesta                   | Priimta                    |






