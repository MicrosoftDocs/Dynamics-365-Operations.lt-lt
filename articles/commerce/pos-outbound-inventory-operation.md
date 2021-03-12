---
title: Siunčiamų atsargų operacija EKA
description: Šioje temoje aprašomos siunčiamų atsargų operacijų elektroniniame kasos aparate (EKA) galimybės.
author: hhaines
manager: annbe
ms.date: 07/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: b8f0daf96e782e5ba6c985847bad81312e48d30b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976619"
---
# <a name="outbound-inventory-operation-in-pos"></a>Siunčiamų atsargų operacija EKA

[!include [banner](includes/banner.md)]


„Microsoft Dynamics 365 Commerce“ 10.0.10 ir naujesnėse versijoje gaunamos ir siunčiamos operacijos elektroniniame kasos aparate (EKA) keičia paėmimo ir gavimo operacijas.

> [!NOTE]
> 10.0.10 ir naujesnėse versijoje bet kokios naujos EKA programos funkcijos, susijusios su parduotuvės atsargų gavimu pagal pirkimo užsakymus ir perkėlimo užsakymus, bus pridėtos prie operacijos „Gaunamos operacijos“. Jei šiuo metu naudojate EKA paėmimo ir gavimo operaciją, rekomenduojame sukurti strategiją, skirtą pakeisti šią operaciją naujomis gaunamomis ir siunčiamomis operacijomis. Nors paėmimo ir gavimo operacija nebus pašalinta iš produkto, po 10.0.9. versijos į ją nebebus investuojama funkciniu ir našumo požiūriu.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Būtinoji sąlyga: nesinchroninės dokumentų sistemos konfigūravimas

Išorės operacija apima vykdymo pagerinimus siekiant užtikrinti, kad naudotojai turintys didelės apimties gaunamus publikavimus daugelyje parduotuvių ar bendrovių bei didelius inventoriaus dokumentus, galėtų apdoroti tuos dokumentus prekyvos štabe (HQ) be pertraukū ar klaidų. Taikant šiuos patobulinimus, reikia naudoti nesinchroninę dokumentų sistemą.

Naudojant nesinchronizuotą dokumento darbotvarkę, galite atlikti išorės dokumento keitimus iš POS į prekybos štabą (HQ) ir tuomet eiti prie kitų užduočių, kol komercijos štabo (HQ) apdorojimas pasirodo fone. Norėdami užtikrinti, kad užregistruota sėkmingai, galite patikrinti dokumento būseną EKA dokumentų sąrašo puslapyje **Siunčiamos operacijos**. POS programoje galite taip pat naudoti išorės operacijos įjungimo dokumento sąrašą tam, kad pamatytumėte visus dokumentus, kurių negalima buvo publikuoti komercijos štabe (HQ). Jei dokumentas sužlunga, POS naudotojai gali atlikti korekcijas ir tuomet bandyti dar kartą apdoroti jį į komercijos štabą (HQ).

> [!IMPORTANT]
> Būtina sukonfigūruoti nesinchroninę dokumentų sistemą, kad įmonė galėtų naudoti siuntimo operacijas EKA.

Norėdami sukonfigūruoti nesinchroninę dokumentų sistemą, atlikite toliau pateikiamas procedūras.

### <a name="create-and-configure-a-number-sequence"></a>Numeracijos kūrimas ir konfigūravimas

1. Eikite į **Organizacijos administravimas \> Numeracijos \> Numeracijos**.
2. Puslapyje **Numeracijos** sukurkite numeraciją.
3. Laukuose **Numeracijos kodas** ir **Pavadinimas** įveskite vartotojo nustatytas vertes.
4. „FastTab“ elemente **Nuorodos** pasirinkite **Įtraukti**.
5. Lauke **Sritis** pasirinkite **Prekybos parametrai**.
6. Lauke **Nuoroda** pasirinkite **Mažmeninės prekybos dokumento operacijos identifikatorius**.
7. Skyriaus **Sąranka** „FastTab“ elemente **Bendra** parinktyje **Ištisinis** nustatykite vertę **Ne**, kad išvengtumėte našumo problemų.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Dviejų paketinių užduočių, skirtų dokumentų apdorojimo ir stebėjimo užduotims, kūrimas ir planavimas

> [!NOTE]
> Komercinėje versijoje 10.0.13 ir velesnėje, neprivalote konfigūruoti pakeitinių užduočių per paketinės užduotės sistemą. Paketiniai procesai gali būti konfigūruojami per **Mažmeninė prekyba ir Komercija > Mažmeninės prekybos ir Komercijos IT** meniu. Naudokite **Mažmeninės prekybos dokumento operacijų stebėjimą** ir **Mažmeninės prekybos dokumento operacijos apdorojimo** meniu parinktis paketinių užduočių konfigūravimui

Jūsų sukurtos paketinės užduotys bus naudojamos dokumentams, kurių nepavyko sukurti arba kurių kūrimui skirtas laikas baigėsi, apdoroti. Taip pat jos bus naudojamos, kai aktyvių atsargų dokumentų, apdorojamų EKA, skaičius viršys sistemos sukonfigūruotą vertę.

1. Pasirinkite **Sistemos administravimas \> Užklausos \> Paketinės užduotys**.
2. Puslapyje **Paketinė užduotis** sukurkite dvi paketines užduotis.

    - Norėdami vykdyti klasę **RetailDocumentOperationMonitorBatch**, sukonfigūruokite vieną užduotį.
    - Norėdami vykdyti klasę **RetailDocumentOperationProcessingBatch**, sukonfigūruokite kitą užduotį.

3. Suplanuokite, kad naujos paketinės užduotys būtų vykdomos reguliariai. Pavyzdžiui, nustatykite grafiką, pagal kurį užduotys būtų vykdomos kas penkias minutes.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Būtinoji sąlyga: įtraukti siunčiamą operaciją į EKA ekrano maketą

Prieš jūsų organizacijai naudojant siunčiamų operacijų funkciją, reikia sukonfigūruoti EKA operaciją **Siunčiamos operacijos** viename ar daugiau [EKA ekrano maketų](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Prieš diegdami naują operaciją gamybos aplinkoje, įsitikinkite, kad kruopščiai ją išbandėte ir apmokėte savo vartotojus ją naudoti.

## <a name="overview"></a>Peržiūrėti

Siunčiamos operacijos leidžia EKA vartotojams atlikti toliau pateikiamas užduotis.

- Registruoti siuntas perkėlimo užsakymų dokumentuose tai atvejais, kai vartotojo parduotuvė yra nustatytas siuntimo sandėlis.
- Peržiūrėti informaciją apie retrospektyvinių perkėlimo užsakymų siuntas, kurias registravo parduotuvė.
- Kurti naujas siunčiamų perkėlimo užsakymų užklausas.

Kai siunčiama operacija pradedama naudojant EKA programą, rodomas sąrašo puslapio rodinys. Šiame rodinyje parodomi atidaryti perkėlimo užsakymų dokumentai su atsargų eilutėmis, kurias dabartinė vartotojo parduotuvė ketina siųsti ir įvykdyti. Norėdami rasti ir pasirinkti dokumentą, vartotojai gali slinkti sąrašu arba naudotis ieškos funkcija.

Siunčiamų atsargų dokumentų sąraše yra trys skirtukai.

- **Aktyvūs** – šiame skirtuke parodomi perkėlimo užsakymai, kurių būsena yra **Pageidaujama** arba **Iš dalies išsiųsta**. Užsakymuose yra eilučių arba kiekių eilutėse, kuriuos turi išsiųsti vartotojo dabartinė parduotuvė. Šis skirtukas taip pat rodo užsakymus, kurie turi **Apdorojimo HQ** statusą (kuris reiškia, kad jie laukia sėkmingo publikavimo iš komercijos štabo (HQ) patvirtinimo) ar **Apdorojimas nepavyko** (kuris reiškia, kad publikavimas į komercijos štabą (HQ) nebuvo sėkmingas ir naudotojas privalo koreguoti duomenis ir bandyti dar kartą pateikti užsakymą).
- **Juodraštis** – šiame skirtuke rodomos naujos siunčiamų perkėlimo užsakymų užklausos, kurias sukūrė vartotojo parduotuvė. Tačiau dokumentai buvo įrašyti tik vietoje. Jie dar nebuvo pateikti į komercijos štabą (HQ) apdorojimui.
- **Baigti** – šiame skirtuke rodomas perkėlimo užsakymų dokumentų, kuriuos parduotuvė visiškai išsiuntė per pastarąsias septynias dienas, sąrašas. Šis skirtukas skirtas tik informacijai pateikti. Visa informacija apie dokumentus yra tik skaitomi parduotuvės duomenys.

Kai peržiūrite dokumentus bet kuriuose skirtukuose, pagal lauką **Būsena** suprasite, koks yra dokumento etapas.

- **Juodraštis** – perkėlimo užsakymo dokumentas buvo įrašytas tik vietoje į parduotuvės kanalo duomenų bazę. Nėra informacijos apie jų perdavimo užsakymo prašymą pateikti juos komercijos štabui (HQ).
- **Užklausta** – Prekybos užsakymas ar perdavimo užsakymas buvo sukurtas komercijos štabe (HQ) ir yra visas atidarytas. Vartotojo dabartinė parduotuvė dar neapdorojo siuntų pagal šį dokumentą.
- **Iš dalies išsiųsta** – perkėlimo užsakymo dokumente yra viena ar daugiau eilučių arba dalinių eilutės kiekių, kurie buvo registruoti kaip siunčiami siuntimo sandėlių. Galima gauti šias išsiųstas eilutes naudojant gaunamą operaciją.
- **Visiškai išsiųsta** – visos perkėlimo užsakymo eilutės ir visi eilutės kiekiai užregistruoti kaip išsiųsti siuntimo sandėlio.
- **Vykdoma** – ši būsena naudojama informuoti įrenginių vartotojus, kad su dokumentu aktyviai dirba kitas vartotojas.
- **Pristabdyta** – ši būsena rodoma pasirinkus **Pristabdyti gavimą**, siekiant laikinai sustabdyti gavimo procesą.
- **Aprodojimas HQ** – Dokumentas buvo pateiktas komercijos štabui (HQ) iš POS programos, tačiau nebuvo sėkmingai publikuotas komercijos štabe (HQ). Atliekamas nesinchroninis dokumento registravimo procesas. Po to, kai dokumentas buvo sėkmingai publikuotas komercijos štabe (HQ), jo statusas turi būti atnaujintas į **Visiškai gautą** ar **Gautą iš dalies**.
- **Apdorojimas nepavyko** – Komercijos štabe (HQ) dokumentas buvo publikuotas ir atmestas.  Srityje **Išsami informacija** nurodoma, kodėl nepavyko užregistruoti. Dokumentas turi būti redaguojamas ištaisant duomenų klaidas ir tuomet turi būti dar kartą įkeltas į komercijos štabą (HQ) apdorojimui.

Kai sąraše pasirenkate dokumento eilutę, rodoma sritis **Išsami informacija**. Šioje srityje pateikiama papildoma informacija apie dokumentą, pvz., siuntimo ir datos informacija. Eigos juostoje rodoma, kiek prekių dar reikia apdoroti. Jei dokumentas nebuvo sėkmingai apdorotas į Komercijos štabą (HQ), **Išsamios informacijos** juosta taip pat rodo klaidų pranešimus, susijusius su gedimu.

Norėdami peržiūrėti išsamią informaciją apie dokumentą, dokumentų sąrašo puslapio rodinyje programos juostoje galite pasirinkti **Užsakymo informacija**. Taip pat galite aktyvinti gavimo apdorojimą tinkamose dokumento eilutėse.

Dokumentų sąrašo puslapio rodinyje taip pat galite sukurti naują siunčiamo perkėlimo užsakymą, skirtą parduotuvei.

## <a name="transfer-order-shipping-process"></a>Perkėlimo užsakymų siuntimo procesas

Pasirinkę perkėlimo užsakymo dokumentą skirtuke **Aktyvieji**, galite pasirinkti **Užsakymo informacija**, kad pradėtumėte įvykdymo procesą. Atsiranda rodinys **Visas užsakymų sąrašas**. Šiame puslapyje rodomos visos dokumento eilutės, kuriose yra prekė. Jame taip pat pateikiama informacija apie užsakytą kiekį.

Kiekvieną kartą nuskaičius brūkšninį kodą, prie lauke **Dabar siunčiama** pateikiamo kiekio pridedamas vienas vienetas. Taip pat galite įvesti siuntimo kiekį, programos juostoje pasirinkdami **Siųsti produktą**, įvesdami prekės ID ir kiekį. Jei prekė kontroliuojama pagal vietą, galite patvirtinti arba nustatyti dokumento eilutės siuntimo vietą.

Rodinyje **Visas užsakymų sąrašas** galite rankiniu būdu pasirinkti eilutę sąraše ir po to atnaujinti pasirinktos eilutės **Siunčiama dabar** kiekį srityje **Išsami informacija**.

### <a name="over-delivery-shipping-validations"></a>Pristatymo perviršio siuntimo tikrinimas

Tikrinimas vykdomas dokumento eilučių gavimo proceso metu. Jis apima pristatymo perviršio tikrinimą. Jei vartotojas bando gauti daugiau atsargų, nei buvo užsakyta pirkimo užsakyme, bet pristatymo perviršis nesukonfigūruotas arba gautas kiekis viršija pirkimo užsakymo eilutėje sukonfigūruotą leistiną pristatymo perviršio nuokrypį, vartotojas gauna klaidą ir jam neleidžiama gauti perteklinio kiekio.

### <a name="underdelivery-close-lines"></a>Pristatymo trūkumo uždarymo eilutės

„Commerce“ 10.0.12 versijoje buvo įtrauktos funkcijos, leidžiančios EKA vartotojams siuntimo užsakymo siuntimo metu uždaryti arba atšaukti likusius kiekius, jei siuntimo sandėlis nustato, kad jis negali išsiųsti viso pageidauto kiekio. Kiekius taip pat galima uždaryti arba atšaukti vėliau. Norint naudoti šią funkciją, įmonė turi būti sukonfigūruota leisti perkėlimo užsakymų pristatymo trūkumą. Be to, turi būti nurodytas perkėlimo užsakymo eilutės pristatymo trūkumo procentas.

Siekiant konfigūruoti bendrovės leidimą perduodamų užsakymų nepakankamam pristatymui, komercijos štabe (HQ), eikite į **Inventoriaus valdymą \> Nustatymus \> Inventoriaus ir sandėlio valdymo parametrai**. Puslapio **Atsargų ir sandėlio valdymo parametrai** skirtuke **Perkėlimo užsakymai** įjunkite parametrą **Priimti pristatymo trūkumą**. Tada paleiskite **1070** paskirstymo grafiko užduotį, kad parametrų pakeitimai būtų sinchronizuojami jūsų parduotuvės kanale.

Perkėlimo užsakymo eilutės pristatymo trūkumo procentai gali būti iš anksto nustatyti produktams kaip produkto konfigūracijos „Commerce“ pagrindiniame komponente dalis. Kitu atveju, jie gali būti siunčiami ar užrašomi specialioje užsakymo perdavimo eilutėje Komercijos biure (HQ).

Po to, kai organizacija užbaigia konfigiūruoti užsakymo perdavimo nepakankamą pristatymą, POS naudotojai matys naują **Uždaryti likusį kiekį** parinktį **Išsamios informacijos** juostoje, kai jie pasirinks išorės persiunčiamo užsakymo liniją **Išorės operacijos** funkcijoje. Kai naudotojas pabaigia siuntimą naudodamas **Pabaigti vykdymą** operaciją, jie gali siųsti užklausą į komercijos štabą (HQ) tam, kad panaikintų likusį neišsiųstą kiekį.  Jei vartotojas uždaro likusį kiekį, komercija atlieka patvirtinimą siekiant patikrinti, ar atšauktas kiekis yra nepristatyto užsakymo paklaidos intervale nustatytame persiunčiamo užsakymo eilutėje. Jei iki galo nepristatyto užsakymo paklaida viršijama, klaidos pranešimas rodomas ir naudotojas nebegali uždaryti likusio kiekio, kol anksčiau išsiųstas ir „dabar siunčiamas“ kiekis neatitinka ar neviršija nepakankamai pristatytos paklaidos.

Po to, kai siuntimas yra sinchronizuojamas komercijos biure (HQ), **Siųsti dabar** laukelyje nustatyti kiekiai siunčiamo užsakymo eilutėje POS yra atnaujinami į siuntimo statusą biuro štabe (HQ). Visas neišsiųstas kiekis, kuris anksčiau būtų buvęs laikomas kiekiu „Liko išsiųsti“ (t. y. kiekiu, kuris bus siunčiamas vėliau), vietoj to yra laikomas atšauktu kiekiu. Perkėlimo užsakymo eilutėje kiekis „Liko išsiųsti“ yra nustatytas kaip **0** (nulis), o eilutė laikoma visiškai išsiųsta.

### <a name="shipping-location-controlled-items"></a>Pagal vietą kontroliuojamų prekių siuntimas

Jei siunčiamos prekės yra pagal vietą kontroliuojamos prekės, vartotojai gali pasirinkti vietą, kurioje jie nori išduoti atsargas siuntimo proceso metu. Rekomenduojame sukonfigūruoti numatytąją parduotuvės sandėlio siuntimo vietą, kad šis procesas būtų efektyvesnis. Net jei numatytoji vieta sukonfigūruota, vartotojai gali pagal poreikį nepaisyti siuntimo vietos pasirinktose eilutėse.

Vykdant operaciją atsižvelgiama į konfigūraciją **Galimas tuščias gavimas**, esančią saugojimo dimensijoje **Vieta**, ir nereikalaujama, kad vietos dimensija būtų įvesta, jei sukonfigūruotas tuščias gavimas. Jei negalima naudoti tuščių prekės gavimo vietų, EKA programoje rodoma klaida ir reikalaujama, kad prieš registruojant gavimą būtų įvesta vieta.

### <a name="ship-all"></a>Siųsti viską

Jei reikia, galite pasirinkti **Siųsti viską** programos juostoje, kad greitai pakeistumėte visų dokumento eilučių kiekį **Siunčiama dabar** į didžiausią galimą atitinkamų eilučių įvykdomą kiekį.

### <a name="cancel-fulfillment"></a>Atšaukti įvykdymą

Naudokite **Atšaukti vykdymą** funkciją programose juostoje tik, jei norite pagrįsti dokumentą ir nenorite išsaugoti pakeitimų. Pavyzdžiui, iš pradžių pasirinkote netinkamą dokumentą ir nenorite, kad būtų įrašyti ankstesni siuntimo duomenys.

### <a name="pause-fulfillment"></a>Pristabdyti įvykdymą

Jei įvykdote perkėlimo užsakymą, galite naudoti funkciją **Pristabdyti įvykdymą**, jei norite padaryti pertrauką procese. Pavyzdžiui, jums gali reikėti atlikti kitą veiksmą iš POS, tokį kaip skambinimą prekybos klinetui ar siuntimo į komercijos biuro (HQ) vėlavimo publikavimą.

Kai pasirenkate **Pristabdyti įvykdymą**, dokumento būsena pakeičiama į **Pristabdyta**. Todėl vartotojas žinos, kad dokumento duomenys įvesti, bet dokumentas dar nepatvirtintas. Kai būsite pasirengę tęsti įvykdymo procesą, pasirinkite pristabdytą dokumentą ir pasirinkite **Užsakymo informacija**. Visi anksčiau įrašyti **Siunčiama dabar** kiekiai bus išsaugoti ir juos galima peržiūrėti rodinyje **Visas užsakymų sąrašas**.

### <a name="review"></a>Peržiūrėti

Prieš paskutinį komercijos biuro įsipareigojimą, galite naudoti **Peržiūros** funkciją tam, kad patvirtintumėte išorės dokumentą. Ši funkcija praneša jums apie potencialiai trūkstančius ar netikslius duomenis, kurie gali sukelti apdorojimo klaidą ir pateikti jums galimybę ištaisyti problemas prieš pateikiant vykdymo užklausą. Tam, kad įjungtumėte **Peržiūros** funkciją programose juostoje, įjunkite **Vidaus ir išorės inventoriaus veiksmų POS tvirtinimo** funkciją per savybių valdymą komercijos štabe (HQ).

**Peržiūros** funkcija patvirtina tolesnes problemas išorės dokumente:
- **Per didelis siuntimas** – dabar siuntimo kiekis yra didesnis nei užsakytas kiekis. Šios problemos rimtumą nulemia per didelis gavimo konfigūravimas biuro štabe (HQ).
- **Per mažas siuntimas** – dabar siuntimo kiekis yra mažesnis nei užsakytas kiekis. Šios problemos rimtumą nulemia per mažo gavimo konfigūravimas biuro štabe (HQ).
- **Serijinis numeris** – serijinis numeris nėra pateiktas ir neprieinamas serijiniuose elementuose, kurie reikalauja serijinio numerio registravimui inventoriuje.
- **Vieta nenustatyta** – vieta nėra nustatyta vietos kontroliuojamam elementui, kuriame vieta negali būti tuščia.
- **Panaikinti eilutes** – užsakymas turi komercijos štabo (HQ) naudotojo panaikintų eilučių, kurios yra nežinomos POS programai.

Jei **Komercijos parametrai** > **Atsargos** > **Saugoti atsargų operacijas** nustatysite parametro **Įjungti automatinį patvirtinimą** reikšmę **Taip**, pasirinkus funkciją **Baigti įvykdymą** patvirtinimas bus vykdomas automatiškai.

### <a name="finish-fulfillment"></a>Baigti įvykdymą

Kai baigsite įvesti visus produktų **Siunčiama dabar** kiekius, turite pasirinkti **Baigti įvykdymą** programos juostoje.

Naudojant nesinchroninį dokumentų apdorojimą, gavimas pateikiamas naudojant nesinchroninę dokumentų sistemą. Laikas, kurio reikia dokumentui užregistruoti, priklauso nuo dokumento dydžio (eilučių skaičiaus) ir bendro apdorojamų duomenų srauto serveryje. Paprastai šis procesas atliekamas per keletą sekundžių. Jei dokumento užregistruoti nepavyksta, vartotojui pranešama per dokumentų sąrašą **Siuntimo operacijos** skirtuke **Aktyvieji**, kur dokumento būsena bus pakeista į **Apdoroti nepavyko**. Vartotojas gali pasirinkti neapdorotą dokumentą EKA, kad pamatytų klaidų pranešimus ir nepavykusio apdorojimo priežastį srityje **Išsami informacija**. Neapdorotas dokumentas lieka neužregistruotas ir reikia, kad vartotojas grįžtų prie dokumento eilučių, EKA pasirinkęs **Užsakymo informacija**. Vartotojas turi ištaisyti dokumento klaidas. Pataisęs dokumentą, vartotojas gali bandyti dar kartą jį apdoroti, programos juostoje pasirinkdamas **Baigti įvykdymą**.

## <a name="create-an-outbound-transfer-order"></a>Siunčiamo perkėlimo užsakymo kūrimas

EKA vartotojai gali kurti naujus perkėlimo užsakymų dokumentus. Norėdami pradėti procesą, programos juostoje pasirinkite **Naujas**, būdami pagrindiniame dokumentų sąraše **Siuntimo operacijos**. Matysite paraginimą pasirinkti sandėlį ar parduotuvę **Perkelti į**, į kuriuos dabartinė parduotuvė siųs atsargas. Galimos tik vertės, pasirinktos parduotuvės įvykdymo grupės konfigūracijoje. Siunčiamo perkėlimo užsakymo užklausoje dabartinė parduotuvė perkėlimo užsakyme visada bus sandėlis **Perkelti į**. Tos vertės pakeisti negalima.

Laukuose **Siuntimo data**, **Gavimo data** ir **Pristatymo būdas** įveskite reikiamas vertes. Galite taip pat įtraukti pastabą, kuri bus laikoma kartu su perduodamo užsakymo antrašte, kaip priedą prie dokumento komercijos štabe (HQ).

Sukūrę antraštės informaciją, galite įtraukti produktų į perkėlimo užsakymą. Norėdami pradėti prekių ir norimų kiekių įtraukimo procesą, nuskaitykite brūkšninius kodus arba pasirinkite **Įtraukti produktą**.

Po to, kai eilutės buvo įrašytos į išorės perdavimo užsakymą, turite pasirinkti **Įrašyti** tam, kad įrašytumėte dokumento pakeitimus vietiniu lygmeniu ar **Pateikti reikalavimą** tam, kad pateiktumėte užsakymo informaciją komercijos štabui (HQ) tolesniam apdorojimui. Jei pasirinksite **Įrašyti**, dokumento juodraštis bus saugomas kanalo duomenų bazėje, o siuntimo sandėlis negalės vykdyti dokumento, kol jis nebus sėkmingai apdorotas naudojant **Pateikti užklausą**. Pasirinnkite **Įrašyti** tik, jei nesate pasirengę įsipareigoti prašymui komercijos biure (HQ) apdorojimui.

Jei dokumentas įrašomas vietoje, jį rasite skirtuke **Juodraščiai** dokumentų sąraše **Gaunamos operacijos**. Kol dokumento būsena yra **Juodraštis**, galite jį redaguoti pasirinkdami **Redaguoti**. Pagal poreikį galite atnaujinti, įtraukti ar naikinti eilutes. Be to, galite panaikinti visą dokumentą, kurio būsena yra **Juodraštis**, pasirinkę **Naikinti** skirtuke **Juodraščiai**.

Po to, kai projektinis dokumentais buvo sėkmingai pateiktas komercijos štabe (HQ), jis pasirodo **Aktyvieji** skirtukte ir turi **Reikalaujamų** statusą. Nuo šiol dokumentą gali redaguoti tik siuntimo sandėlio vartotojai, EKA programoje pasirinkę **Siuntimo operacija**. Gavimo sandėlio vartotojai gali peržiūrėti perkėlimo užsakymą skirtuke **Aktyvieji**, esančiame dokumentų sąraše **Gaunamos operacijos**, tačiau jie negali jo redaguoti arba naikinti. Redagavimo užraktu užtikrinama, kad nekiltų konfliktų gaunančiam prašytojui pakeitus perkėlimo užsakymą tuo pačiu metu, kai siunčiantis siuntėjas aktyviai paima ir siunčia užsakymą. Jei, pateikus perkėlimo užsakymą, gaunanti parduotuvė arba sandėlis turi pateikti pakeitimų, reikia susisiekti su siunčiančiu siuntėju ir paprašyti įvesti pakeitimus.

Dokumentui įgijus būseną **Pageidaujama**, jis yra paruoštas įvykdymo apdorojimui, vykdomam siuntimo sandėlyje. Kai siunta apdorojama naudojant siunčiamą operaciją, perkėlimo užsakymo dokumentų būsena pakeičiama iš **Pageidaujama** į **Visiškai išsiųsta** arba **Iš dalies išsiųsta**. Dokumentams įgijus būseną **Visiškai išsiųsta** arba **Iš dalies išsiųsta**, gaunanti parduotuvė arba sandėlis gali pagal juos registruoti gavimus, naudodami gaunamų operacijų gavimo procesą.

Visiškai išsiųsti perkėlimo užsakymai perkeliami į skirtuką **Atlikta** dokumentų sąraše **Siuntimo operacijos**. Ten juos tik skaitymo režimu septynias dienas mato siunčiančios parduotuvės arba sandėlio vartotojai.

## <a name="related-topics"></a>Susijusios temos

[Atvežamų atsargų operacija EKA](pos-inbound-inventory-operation.md)
