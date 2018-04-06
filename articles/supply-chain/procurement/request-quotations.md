---
title: "Pasiūlymų patvirtinimai (RFQ)"
description: "Šioje temoje pateikiama pasiūlymų patvirtinimų (RFQ) apžvalga. Organizacijos išduoda RFQ, kai nori pirkti prekes arba paslaugas ir gauti konkurencingų pasiūlymų iš kelių tiekėjų."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b86363004b8702d1a654f2a1da49bba82fc8ff2a
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="requests-for-quotation-rfqs"></a>Pasiūlymų patvirtinimai (RFQ)

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama pasiūlymų patvirtinimų (RFQ) apžvalga. Organizacijos išduoda RFQ, kai nori pirkti prekes arba paslaugas ir gauti konkurencingų pasiūlymų iš kelių tiekėjų. RFQ tiekėjų prašoma pateikti nurodyto prekių kiekio kainas ir pristatymo laiką. Be to, galite paprašyti tiekėjų nurodyti, ar bus papildomų išlaidų, pvz., siuntimo išlaidų, arba nuolaidų didelių užsakymų ar ankstyvo tiekėjo SF apmokėjimo atveju.

RFQ procesą sudaro toliau pateiktos užduotys.

1. RFQ kūrimas ir siuntimas vienam ar keliems tiekėjams.
2. RFQ atsakymų (kainos siūlymų) gavimas ir registravimas.
3. Priimtų kainos siūlymų perkėlimas į pirkimo užsakymą, pirkimo sutartį ar pirkimo paraišką.

Toliau esančiame paveikslėlyje pateikiama RFQ proceso apžvalga.

[![RFQ procesas](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Galite sukurti RFQ iš suplanuotų užsakymų, pirkimo paraiškos arba įvesti neautomatiniu būdu. Kuriamas RFQ vadinamas RFQ atveju. RFQ atvejis yra pagrindinis dokumentas, naudojamas RFQ kiekvienam tiekėjui išduoti.

Paruošę RFQ atvejį ir įtraukę tiekėjus, RFQ atvejyje pasirinkite **Siųsti**. Generuojamas kiekvieno tiekėjo, kuriam siunčiate RFQ, RFQ žurnalas. Galite konfigūruoti siuntimo veiksmo spausdinimo valdymo parametrą, kad kiekvieno tiekėjo ataskaita būtų spausdinama arba siunčiama kiekvieno tiekėjo el. pašto adresu. Be to, naudojant kiekvieno tiekėjo RFQ žurnalą galima generuoti ataskaitą, kurią galima siųsti arba pakartotinai siųsti tiekėjui vėliau. Taip pat galite konfigūruoti siuntimo veiksmą, kad būtų sugeneruotas atsakymo lapas, kurį tiekėjas gali užpildyti.

Šioje temoje aprašomas RFQ tvarkymo procesas, kai nenaudojamas tiekėjo bendradarbiavimas. Jei jūsų sistemoje nustatytas tiekėjo bendradarbiavimas, tiekėjai gali įvesti kainos siūlymus tiesiai į „Microsoft Dynamics 365 for Finance and Operations“. Jei reikia daugiau informacijos, žr. temą [Tiekėjo bendradarbiavimas su klientais](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Jei reikia pakeisti išsiųstą RFQ, baigę galite pakartotinai išsiųsti RFQ tiekėjams naudodami du keitimo veiksmus: kurti ir baigti.

Gavę pasiūlymų el. paštu, turite įvesti juos į puslapį **Pasiūlymų patvirtinimų atsakymai**. Jei pasirinksite parinktį **Kopijuoti duomenis į atsakymą**, duomenys, pvz., kiekis ir datos, iš RFQ atvejo nukopijuojami į atsakymą. Galite keisti šiuos duomenis, kad jie atspindėtų tiekėjo pasiūlymą.

Jei reikalingas tiekėjo antras atsakymo pakartojimas, puslapyje **Pasiūlymo patvirtinimo atsakymas** pasirinkite **Grąžinti**. Grąžinimo veiksmas sugeneruoja naują žurnalą ir ataskaitą, kuri bus išspausdinta, archyvuota ir išsiųsta pagal jūsų spausdinimo valdymo parametrus.

Jei į RFQ atvejį įtraukiate vertinimo kriterijų, RFQ atsakymas turės vertinimo sritį, kurioje galima įvesti rezultatus. Bendras rezultatas bus rodomas, kai palyginsite atsakymus puslapyje **Palyginti atsakymus**. Tame puslapyje taip pat galima palyginti kitus atsakymų duomenis, pvz., eilutės kainą, pristatymo datą ir bendrąją kainą.

Nusprendę dėl kainos pasiūlymo arba dalinio kainos pasiūlymo, galite juos priimti ir atmesti likusius. Generuojami priėmimo žurnalai, atmetimo žurnalai ir atitinkamos ataskaitos ir jie bus išspausdinti, archyvuoti bei išsiųsti pagal jūsų spausdinimo valdymo parametrus. Priėmus kainos pasiūlymą arba konkrečias kainos pasiūlymo eilutes sugeneruojama pirkimo sutartis arba pirkimo užsakymas arba atnaujinama pirkimo paraiška, atsižvelgiant į RFQ pirkimo tipą. Galite sukurti prekybos sutartį, kurią vėliau galėsite naudoti bet kuriuose atsakymuose, nepaisant to, ar juos priėmėte, ar atmetėte.

RFQ būsena rodoma RFQ antraštėje ir priklauso nuo RFQ eilučių būsenos. Būsena nurodo, kiek RFQ jau apdorotas. Kiekvienas RFQ turi dvi būsenos vertes: mažiausią būseną ir didžiausią būseną. Mažiausia būsena yra mažiausiai pažengęs etapas iš visų RFQ eilučių, o didžiausia būsena yra labiausiai pažengęs etapas iš visų RFQ eilučių. Pavyzdžiui, jei sukurtai eilutei galioja mažiausiai pažengęs RFQ etapas, mažiausia RFQ būsena yra **Sukurta**. Jei RFQ eilutės labiausiai pažengęs etapas yra išsiuntimas tiekėjui, aukščiausia RFQ būsena bus **Išsiųsta**. Būsenos atnaujinamos automatiškai, apdorojant RFQ.

Galite peržiūrėti mažiausią ir didžiausią būsenas RFQ antraštėje sąrašo puslapyje **Visi pasiūlymų patvirtinimai**. Galite peržiūrėti mažiausią ir didžiausią RFQ eilutės būsenas puslapio **Pasiūlymo patvirtinimai** skirtuke **Eilutės**.

Toliau nurodyta RFQ apdorojimo būsenų seka.

1. **Sukurta**
2. **Išsiųstas**
3. **Gauta**
4. **Priimta**, **Atšaukta** arba **Atmesta**

Šios būsenos bus išsamiau aprašytos vėlesniuose šios temos skyriuose.

## <a name="setting-up-rfq-functionality"></a>RFQ funkcijų nustatymas

Prieš kurdami RFQ atvejį, turite nustatyti RFQ informaciją puslapyje **Paraiškų parametrai**. Kai kuriate yra RFQ atvejį, galite nurodyti numatytąsias vertes, kurios yra kopijuojamos į RFQ. Galite nurodyti šias numatytąsias vertes:

- Naujų RFQ pirkimo tipas: **Pirkimo užsakymas** arba **Pirkimo sutartis**
- Galiojimo data ir laikas
- Pristatymo informacija ir mokėjimo sąlygos
- Laukai, kuriuos reikia įtraukti į RFQ atsakymą

Galite nepaisyti šių verčių konkrečiame RFQ atvejyje.

Taip pat turite sukonfigūruoti pakeitimo procesą. Kaip šios konfigūracijos dalį galite įjungti lauko blokavimo funkciją. Kai įjungta lauko blokavimo funkcija, įsigijimo specialistas, kuris nori pakeisti RFQ, pirma turi pasirinkti mygtuką **Kurti**, esantį skirtuko **Pasiūlymas** dalyje **Pakeitimas**. Tada, atnaujinus RFQ pakeitimu įsigijimo specialistas turi užbaigti procesą spustelėdamas **Baigti**. Atlikus veiksmą Baigti sugeneruojamas el. laiškas, kuriuo tiekėjams pranešama apie pakeistą RFQ.

Pasirinkite tiekėjui siunčiamo el. pašto pranešimo šabloną puslapyje **Paraiškų parametrai**. Kai sukuriamas šablonas, jame gali būti tokių pakeitimo atpažinimo ženklų:

- %RFQ atvejis%
- %Kainos pasiūlymo grąžinimo priežastis%
- %Pakeitimo priežastis%
- %Pakeitimą parengė%
- %Įmonė%
- %RFQ atvejo pavadinimas%
- %ExpiryDateTime%
- %Date%

Atpažinimo ženklus %Kainos pasiūlymo grąžinimo priežastis% ir %Pakeitimo priežastis% įsigijimo specialistas pakeičia tekstu, kurį gali įvesti atlikęs šiuos pakeitimus naudodamas vedlį **Pakeitimas**. Atpažinimo ženklų %Pakeitimą parengė% ir %Įmonė% vertės automatiškai paimamos iš RFQ. Atpažinimo ženklas %Date% pakeičiamas esama data.

El. laiško šablono taip pat būtinas, jei atšaukiate išsiųstą RFQ. El. laiško šablonas naudojamas siunčiant atšaukimo pranešimą tiekėjo kontaktiniams asmenims. Šabloną reikia pasirinkti puslapyje **Paraiškų parametrai**. Kai sukuriamas šablonas, jame gali būti toliau nurodytų pakeitimo atpažinimo ženklų.

- %Nutraukimo priežastis%
- %RFQ atvejis% 
- %RFQ nutraukta%
- %Įmonė%
- %RFQ atvejo pavadinimas%
- %Date%

Atpažinimo ženklas %Reason for cancellation% pakeičiamas tekstu, kurį įsigijimo specialistas gali įvesti vedlyje **Atšaukimas**. Atpažinimo ženklas %Date% pakeičiamas esama data.

Jei RFQ atsakyme siekdami nurodyti, kodėl pasiūlymas buvo atmestas ar priimtas, norite naudoti priežasčių kodus, turite nustatyti priežasčių kodus puslapyje **Tiekėjų priežastys**.

Galite konfigūruoti išspausdintų arba saugomų RFQ dokumentų išvaizdą dalies paraiškų puslapyje **Formos nustatymas**.

> [!NOTE]
> Jei naudojama viešojo sektoriaus konfigūracija, norint atlikti jau išsiųsto RFQ keitimus reikia naudoti pakeitimo procesą. Išsiuntus RFQ laukai užrakinami. Todėl, norint atlikti RFQ keitimus, reikia pasirinkti **Kurti** ir pradėti keitimo procesą, kaip aprašyta pirmiau. Tai valdo lauko blokavimo parinktis **Užrakinti išsiųstus RFQ**, esanti puslapyje **Paraiškų parametrai**. Pagal numatytuosius parametrus šis parametras nustatytas į parinktį **Taip** ir naudojant viešojo sektoriaus konfigūraciją tai yra numatytoji reikšmė, kurios negalima keisti. Todėl, nors pakeitimo procesą galima tvarkyti neautomatiniu būdu viešojo sektoriaus konfigūracijoje, jį reikia naudoti viešojo sektoriaus konfigūracijoje.

Kai sukuriate pirkimo užsakymo RFQ ir prie RFQ pridedate atsargų prekę, sugeneruojama atsargų operacija, kurios gavimo būsena yra **Pasiūlymo gavimas**. Kai naudojate bendrąjį planą apskaičiuodami atsargas, atsižvelgiama tik į šios būsenos RFQ eilutes. Jei norite, kad į bendrąjį planą kaip numatomas gavimas būtų įtrauktos RFQ eilutės, turite sukonfigūruoti šią veikseną bendrojo planavimo nustatyme.

Pirkimo vadovas arba agentas gali kurti ir tvarkyti siūlymų tipus, kad atitiktų jūsų organizacijos įsigijimo poreikius. Kiekvieno siūlymo tipą galima susieti su vertinimo būdu. Vertinimo metodus sudaro tam tikri kriterijai, kuriuos galima naudoti vertinant kainos pasiūlymus. Siūlymų tipus, vertinimo būdus ir vertinimo kriterijus turite nustatyti puslapiuose **Siūlymo tipas** ir **Vertinimo būdas**.

## <a name="creating-and-sending-an-rfq"></a>RFQ kūrimas ir siuntimas

Sukuriate RFQ, pasirenkate tiekėjus, kurių kainų pasiūlymus norite gauti į RFQ, ir išsiunčiate RFQ tiekėjams. Spausdinimo valdymą galite naudoti, kad nukreiptumėte RFQ ataskaitas ir atsakymų lapų ataskaitas į pasirinktą vietą.

Galite kurti pirkimo tipo **Pirkimo užsakymas** arba **Pirkimo sutartis** RFQ.

Jei RFQ tipas **Pirkimo užsakymas**, įvyksta toliau pateikti scenarijai.

- Kuriant RFQ eilutes generuojamos atsargų operacijos, kurių gavimo būsena yra **Pasiūlymo gavimas**.
- Priėmus kainos pasiūlymą generuojamas pirkimo užsakymas.

Jei RFQ tipas **Pirkimo sutartis**, įvyksta toliau pateikti scenarijai.

- RFQ naudojamas kaip sutartis tam tikram produkto kiekiui arba vertei pirkti per tam tikrą laikotarpį. Turite pasirinkti datų intervalą, kuris bus taikomas pirkimo sutarčiai, ir asmens, kuris valdo pirkimo sutartį, vardą.
- Priėmus kainos pasiūlymą generuojama pirkimo sutartis.

Jei RFQ generuojamas iš pirkimo paraiškos, automatiškai priskiriamas tipas **Pirkimo paraiška**. Negalima neautomatiniu būdu sukurti tipo **Pirkimo paraiška** RFQ.

RFQ iš pirkimo paraiškos galite sukurti tik jei pirkimo paraiškos būsena yra **Peržiūrima** ir jūs esate priskirti atlikti kitą darbo eigos užduotį. Pirkimo paraiškos eilutės naujinamos automatiškai, kai priimate eilutes iš RFQ atsakymų (kainos pasiūlymų), kuriuos gavote iš tiekėjų. Negalite užbaigti, atmesti ir patvirtinti pirkimo paraiškos arba atlikti su ja kitų veiksmų, kai vykdomas RFQ.

Kai kuriate RFQ, galite pasirinkti siūlymo tipą. Pagal siūlymo tipą nustatomas vertinimo kriterijų rinkinys, naudojamas RFQ atsakymams vertinti.

Prie RFQ atvejo galite pridėti klausimyną. Šis klausimynas rodomas visuose atsakymuose išsiuntus RFQ.

Pasirinkti tiekėjus, įtrauktinus į RFQ atvejį, galima trimis būdais:

- Įtraukti tiekėjus po vieną.
- Ieškoti visų tiekėjų, atitinkančių nurodytus kriterijus.
- Automatiškai įtraukti visus tiekėjus, patvirtintus pagal įsigijimo kategorijas, naudojamas RFQ eilutėse.

Kai RFQ atvejis bus paruoštas, pasirinkite **Siųsti**. Siuntimo veiksmas sugeneruoja žurnalus ir ataskaitas, kurie bus išspausdinti, archyvuoti ir išsiųsti pagal jūsų spausdinimo valdymo parametrus.

Jei išsiųsdami RFQ tiekėjams puslapyje **Pasiūlymo patvirtinimo siuntimas** nustatėte parinktis **Naudoti tiekėją perskaičiuojant kainas** ir **Naudoti prekių informaciją pagal tiekėją** į **Taip**, tam tikra konkretaus tiekėjo informacija įvedama automatiškai. Šią informaciją galima modifikuoti puslapyje **Pasiūlymo patvirtinimo atsakymas**.

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena, kai sukuriate RFQ ir siunčiate ją tiekėjams.

| Veiksmas                             | Žemiausia RFQ antraštės būsena | Aukščiausia RFQ antraštės būsena                        | Žemiausia RFQ eilutės būsena | Aukščiausia RFQ eilutės būsena |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Sukurkite RFQ antraštę ir eilutę.    | Sukurta                  | Sukurta                                          | Sukurta                | Sukurta |
| Siųskite RFQ konkrečiam tiekėjui. | Išsiųsta                     | Išsiųsta                                             | Išsiųsta                   | Išsiųsta |
| Pridėti kitą tiekėją.                | Sukurta                  | Išsiųsta (RFQ išsiųstas tik vienam tiekėjui.) | Sukurta                | Išsiųsta |
| Išsiųsti RFQ antram tiekėjui. | Išsiųsta                     | Išsiųsta                                             | Išsiųsta                   | Išsiųsta |

> [!NOTE]
> Galite į RFQ įtraukti daugiau tiekėjų bet kuriuo metu ir mažiausia bei didžiausia būsenos bus atnaujintos, nurodant naujus tiekėjus. Pavyzdžiui, jei gavote pasiūlymus iš visų tiekėjų ir priėmėte bent pasiūlymo vieną eilutę, žemiausia būsena RFQ antraštėse bus **Atmesta**, o aukščiausia būsena – **Priimta**. Jeigu įtraukiate naują tiekėją, žemiausia bet kurios eilutės būsena yra **Sukurta**. Todėl žemiausia būsena RFQ antraštėje atnaujinama į **Sukurta**, o aukščiausia būsena lieka **Priimta**.

## <a name="amending-an-rfq"></a>RFQ keitimas

Kartais turite pakeisti RFQ jį išsiuntę. RFQ gali reikėti pakeisti, pavyzdžiui, jei pasikeitė pristatymo datos, norite papildomų produktų arba kitokio produktų kiekio. Galite konfigūruoti pakeitimo procesą, kad jis būtų labiau arba mažiau ribojamas.

Jei sukonfigūruojate mažiau ribojamą pakeitimo procesą, prieš keisdami jau išsiųsto RFQ atvejo laukus RFQ atvejyje turite pasirinkti**Kurti**, kad pradėtumėte keitimą. Atlikę keitimus turite pasirinkti **Baigti**. Jums bus pateikiami nurodymai, kaip įtraukti informaciją į el. laišką, siunčiamą norint perspėti tiekėjus apie pakeitimą. Atnaujinta RFQ ataskaita, kurioje yra pastaba apie pakeitimą, automatiškai pridedama prie el. laiško.

Jei sukonfigūruosite mažiau ribojamą pakeitimo procesą, neturite pasirinkti **Kurti** prieš keisdami jau išsiųsto RFQ atvejo laukus. Tačiau turite patys į RFQ atvejį įtraukti pakeitimo pastabą ir pakartotinai išsiųsti atvejį. Turėkite omenyje, kad šį metodą galima naudoti tik jei nė vienas atsakymas (kainos siūlymas) nebuvo redaguotas. Jei įvedėte atsakymą ir jo būsena yra **Gauta**, mygtuko **Siųsti** naudoti negalima. Tokiu atveju turite pasirinkti **Kurti** ir **Baigti**, kaip turite daryti vykdydami labiau apribotą procesą. Tada atsakymas nustatomas iš naujo, kad atspindėtų RFQ atvejo keitimus. 

Jei tiekėjai naudoja tiekėjo bendradarbiavimo sąsają pasiūlymams įvesti, visada turite naudoti pakeitimo procesą, kad praneštumėte tiekėjams apie RFQ atvejo keitimus. Šis reikalavimas padeda išvengti atvejų, kai tiekėjai teikia kainos siūlymus naudodami pasenusį RFQ atvejį, kol jų kainos siūlymas vis dar tvarkomas. Daugiau informacijos apie tiekėjo bendradarbiavimą žr. puslapyje [Tiekėjo bendradarbiavimas su išoriniais tiekėjais](vendor-collaboration-work-external-vendors.md). 

Jei norite pakviesti papildomus tiekėjus siūlyti kainą ir nebuvo atlikta jokių RFQ atvejo keitimų, galite naudoti mygtuką **Siųsti**. Įtraukti tiekėjai bus rodomi puslapyje **Siųsti** ir gaus kvietimą el. paštu.

## <a name="receiving-and-registering-rfq-replies"></a>RFQ atsakymų gavimas ir registravimas

Siunčiant RFQ atsakymo lapas bus sugeneruotas automatiškai. Gavę atsakymus (kainos pasiūlymus) į RFQ, turite įvesti kiekvieno tiekėjo informaciją konkretaus tiekėjo RFQ atsakymo lape. Jei įtraukėte vertinimo kriterijų, galite atsakymus įvertinti. Tada galite palyginti tiekėjų kainų pasiūlymus ir įvertinti juos pagal savo vertinimo kriterijus, pvz., geriausią bendrąją kainą arba geriausią bendrąjį pristatymo laiką.

Jei į RFQ atvejį įtrauktas klausimynas, turite patys įvesti atsakymus į klausimus atsakymo lape.

Taip pat galite įvesti alternatyvias eilutes, jei RFQ atvejyje galima įvesti alternatyvias eilutes. „FastTab“ **Pirkimo pasiūlymo eilutės** pasirinkite **Įtraukti eilutę**. Tada įveskite informaciją apie produktą, pvz., prekės numerį arba įsigijimo kategoriją, kiekį, kainą ir nuolaidą.

Jeigu įvedėte atsakymą, bet jums reikalingas naujas tiekėjo pasiūlymas, galite RFQ persiųsti. Bus sukurti nauji žurnalas ir ataskaita, kuriuos galite naudoti norėdami prašyti pakeitimų iš tiekėjo.

Galite matyti visų RFQ ir jų atsakymų būsenų peržiūrą puslapyje **Pasiūlymo patvirtinimo stebėjimas**.

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena gaunant kainų pasiūlymus ir registruojant informaciją RFQ atsakymo lape.

| Veiksmas                                         | Žemiausia kainos pasiūlymo būsena | Aukščiausia kainos pasiūlymo būsena | Žemiausia RFQ antraštės būsena | Aukščiausia RFQ antraštės būsena | Žemiausia RFQ eilutės būsena | Aukščiausia RFQ eilutės būsena |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Užregistruokite vieno tiekėjo kainos siūlymą ir jį išsaugokite.        | Išsiųstas              | Gauta           | Išsiųstas                     | Gauta                  | Išsiųstas                   | Gauta |
| Užregistruokite antro tiekėjo kainos pasiūlymą ir jį išsaugokite. | Gauta          | Gauta           | Gauta                 | Gauta                  | Gauta               | Gauta |

> [!NOTE]
> Jei grąžinsite kainos pasiūlymą tiekėjui tolesnėms deryboms, žemiausia ir aukščiausia būsenos liks **Gauta**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Kainos pasiūlymų priėmimas ir atmetimas bei priimtų kainos pasiūlymų perkėlimas į tolesnius dokumentus

Radę geriausią kainos pasiūlymą, pvz., pasiūlymą su geriausia bendrąja kaina, jį priimkite. Galite priimti kai kurias kainos pasiūlymo eilutes ir atmesti kitas. Taip pat galite priimti eilutes iš įvairių tiekėjų. Turėkite omenyje, kad, jei priimate kai kurias eilutes, būsite paraginti atmesti visas kitas. Todėl, jei norite priimti kitų eilučių, gavę raginimą turite pasirinkti **Atšaukti**. Kiekvieno tiekėjo, kurio kainos siūlymą arba eilutes priimate, RFQ atsakymo būsena atnaujinama į **Priimta**. 

Kai priimate kainos siūlymą arba konkrečias kainos siūlymo eilutes, automatiškai sugeneruojamas pirkimo užsakymas ar pirkimo sutartis. Tada galite atmesti kitų tiekėjų kainos siūlymus.

Atsakyme galite įtraukti priežasties kodą, norėdami paaiškinti, kodėl priimtas arba atmestas kainos pasiūlymas.

Kai priimate RFQ atsakymą, kurio tipas yra **Pirkimo paraiška**, RFQ atsakymo eilutės atnaujina toliau nurodytą pirkimo paraiškos eilučių informaciją.

- Vnt. kaina
- Nuolaida procentais
- Nuolaidos suma
- Pirkimo mokesčiai
- Eilutės išlaidos
- Tiekėjas
- Išorinis skaičius
- Išorinis aprašymas

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena, kai priimate ir atmetate tiekėjų kainos pasiūlymus.

| Veiksmas                      | Žemiausia kainos pasiūlymo būsena | Aukščiausia kainos pasiūlymo būsena | Žemiausia RFQ antraštės būsena | Aukščiausia RFQ antraštės būsena | Žemiausia RFQ eilutės būsena | Aukščiausia RFQ eilutės būsena |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Priimti vieną pasiūlymų.     | Gauta          | Priimta           | Gauta                 | Priimta                  | Gauta               | Priimta |
| Atmeskite visus kitus kainos siūlymus.  | Atmestas          | Priimta           | Atmestas                 | Priimta                  | Atmestas               | Priimta |

