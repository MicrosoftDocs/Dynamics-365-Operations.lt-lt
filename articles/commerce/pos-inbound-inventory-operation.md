---
title: Gaunamų atsargų operacijos EKA
description: Šioje temoje aprašomos gaunamų atsargų operacijų elektroniniame kasos aparate (EKA) galimybės.
author: hhaines
manager: annbe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: b212906dcf037171af264c60720f361215eed599
ms.sourcegitcommit: 437170338c49b61bba58f822f8494095ea1308c2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2020
ms.locfileid: "3123904"
---
# <a name="inbound-inventory-operation-in-pos"></a>Gaunamų atsargų operacijos EKA

[!include [banner](includes/banner.md)]

„Microsoft Dynamics 365 Commerce“ 10.0.10 ir naujesnėse versijoje gaunamos ir siunčiamos operacijos elektroniniame kasos aparate (EKA) keičia paėmimo ir gavimo operacijas.

> [!NOTE]
> 10.0.10 ir naujesnėse versijoje bet kokios naujos EKA programos priemonės, susijusios su parduotuvės atsargų gavimu pagal pirkimo užsakymus ir perkėlimo užsakymus, bus pridėtos prie EKA operacijos **Gaunamos operacijos**. Jei šiuo metu naudojate EKA paėmimo ir gavimo operaciją, rekomenduojame sukurti strategiją, skirtą pakeisti šią operaciją naujomis gaunamomis ir siunčiamomis operacijomis. Nors paėmimo ir gavimo operacija nebus pašalinta iš produkto, po 10.0.9. versijos į ją nebebus investuojama funkciniu ir našumo požiūriu.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Būtinoji sąlyga: nesinchroninės dokumentų sistemos konfigūravimas

Gavimo operacija apima našumo patobulinimus, siekiant užtikrinti, kad vartotojai, registruojantys daug gavimų daugelyje parduotuvių ar įmonių ir tvarkantys didelius atsargų dokumentus, galėtų apdoroti šiuos dokumentus „Commerce“ būstinėje laiku ir be klaidų. Taikant šiuos patobulinimus, reikia naudoti nesinchroninę dokumentų sistemą.

Kai naudojama nesinchroninė dokumentų sistema, galite patvirtinti gaunamų dokumentų keitimus iš EKA į „Commerce“ būstinę, o tada pereiti prie kitų užduočių, kai fone apdorojamas siuntimas į „Commerce“ būstinę. Norėdami užtikrinti, kad užregistruota sėkmingai, galite patikrinti dokumento būseną EKA dokumentų sąrašo puslapyje **Gaunamos operacijos**. EKA programoje taip pat galite naudoti gaunamų operacijų aktyvų dokumentų sąrašą, kad pamatytumėte visus dokumentus, kurių nepavyko užregistruoti „Commerce“ būstinėje. Jie nepavyksta apdoroti dokumento, EKA naudotojai gali jį taisyti ir tada vėl bandyti apdoroti jį „Commerce“ būstinėje.

> [!IMPORTANT]
> Būtina sukonfigūruoti nesinchroninę dokumentų sistemą, kad įmonė galėtų naudoti gavimo operacijas EKA.

Norėdami sukonfigūruoti nesinchroninę dokumentų sistemą, atlikite toliau pateikiamas procedūras.

### <a name="create-and-configure-a-number-sequence"></a>Numeracijos kūrimas ir konfigūravimas

1. Eikite į **Organizacijos administravimas \> Numeracijos \> Numeracijos**.
2. Puslapyje **Numeracijos** sukurkite numeraciją.
3. Laukuose **Numeracijos kodas** ir **Pavadinimas** įveskite vartotojo nustatytas vertes.
4. „FastTab“ elemente **Nuorodos** pasirinkite **Įtraukti**.
5. Lauke **Sritis** pasirinkite **Prekybos parametrai**.
4. Lauke **Nuoroda** pasirinkite **Mažmeninės prekybos dokumento operacijos identifikatorius**.
5. Skyriaus **Sąranka** „FastTab“ elemente **Bendra** parinktyje **Ištisinis** nustatykite vertę **Ne**, kad išvengtumėte našumo problemų.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Dviejų paketinių užduočių, skirtų dokumentų apdorojimo ir stebėjimo užduotims, kūrimas ir planavimas

Jūsų sukurtos paketinės užduotys bus naudojamos dokumentams, kurių nepavyko sukurti arba kurių kūrimui skirtas laikas baigėsi, apdoroti. Taip pat jos bus naudojamos, kai aktyvių atsargų dokumentų, apdorojamų EKA, skaičius viršys sistemos sukonfigūruotą vertę.

1. Pasirinkite **Sistemos administravimas \> Užklausos \> Paketinės užduotys**.
2. Puslapyje **Paketinė užduotis** sukurkite dvi paketines užduotis.

    - Norėdami vykdyti klasę **RetailDocumentOperationMonitorBatch**, sukonfigūruokite vieną užduotį.
    - Norėdami vykdyti klasę **RetailDocumentOperationProcessingBatch**, sukonfigūruokite kitą užduotį.

2. Suplanuokite, kad naujos paketinės užduotys būtų vykdomos reguliariai. Pavyzdžiui, nustatykite grafiką, pagal kurį užduotys būtų vykdomos kas penkias minutes.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Būtinoji sąlyga: įtraukti gaunamą operaciją į EKA ekrano maketą

Prieš jūsų organizacijai naudojant gaunamų operacijų funkciją, reikia sukonfigūruoti EKA operaciją **Gaunamos operacijos** viename ar daugiau [EKA ekrano maketų](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Prieš diegdami naują operaciją gamybos aplinkoje, įsitikinkite, kad kruopščiai ją išbandėte ir apmokėte savo vartotojus ją naudoti.

## <a name="overview"></a>Peržiūrėti

Gaunamos operacijos leidžia EKA vartotojams atlikti toliau pateikiamas užduotis.

- Gauti atsargas pagal patvirtintus pirkimo užsakymo dokumentus arba išsiųstus perkėlimo užsakymo dokumentus į parduotuvės atsargas.
- Peržiūrėti informaciją apie retrospektyvinius atsargų gavimus per septynių dienų laikotarpį po to, kai dokumentas buvo visiškai gautas.
- Kurti naujas gaunamų perkėlimo užsakymų užklausas.

Kai gaunama operacija pradedama naudojant EKA programą, rodomas sąrašo puslapio rodinys. Šiame rodinyje parodomi atidaryti pirkimo užsakymų ir perkėlimo užsakymų dokumentai su atsargų eilutėmis, kurias pagal grafiką turi gauti dabartinė parduotuvė. Norėdami rasti ir pasirinkti konkretų dokumentą, vartotojai gali slinkti sąrašu arba naudotis ieškos funkcija.

Gaunamų atsargų dokumentų sąraše yra trys skirtukai.

- **Aktyvieji** – šiame skirtuke rodomi visiškai arba iš dalies atidaryti dokumentai, kuriuose yra eilučių ar kiekių eilutėse, kurias dar reikia gauti.
- **Juodraštis** – šiame skirtuke rodomos naujos gaunamų perkėlimo užsakymų užklausos, kurias sukūrė parduotuvė. Tačiau dokumentai buvo įrašyti tik vietoje. Jie dar nebuvo pateikti „Commerce“ būstinei apdoroti.
- **Baigti** – šiame skirtuke rodomas pirkimo užsakymų ar perkėlimo užsakymų dokumentų, kuriuos parduotuvė visiškai gavo per pastarąsias septynias dienas, sąrašas. Šis skirtukas skirtas tik informacijai pateikti. Visa informacija apie dokumentus yra tik skaitomi parduotuvės duomenys.

Kai peržiūrite dokumentus bet kuriuose skirtukuose, pagal lauką **Būsena** suprasite, koks yra dokumento etapas.

- **Juodraštis** – perkėlimo užsakymo dokumentas buvo įrašytas tik vietoje į parduotuvės kanalo duomenų bazę. Jokia informacija apie perkėlimo užsakymo užklausą dar nebuvo pateikta „Commerce“ būstinei.
- **Pageidaujama** – pirkimo užsakymas arba perkėlimo užsakymas buvo sukurtas „Commerce“ būstinėje ir yra visiškai atidarytas. Kol kas neapdorota jokių su dokumentu susijusių gavimų. Apdorojant pirkimo užsakymo dokumento tipo dokumentus, gavimas gali prasidėti bet kada, kol būsena yra **Pageidaujama**.
- **Iš dalies išsiųsta** – perkėlimo užsakymo dokumente yra viena ar daugiau eilučių arba dalinių eilutės kiekių, kurie buvo registruoti kaip siunčiami siuntimo sandėlių. Galima gauti šias išsiųstas eilutes naudojant gaunamą operaciją.
- **Visiškai išsiųsta** – visos perkėlimo užsakymo eilutės ir visi eilutės kiekiai užregistruoti kaip išsiųsti siuntimo sandėlio. Galima gauti visą dokumentą naudojant gaunamą operaciją.
- **Gauta iš dalies** – kai kurios eilutės arba eilučių kiekiai pirkimo užsakyme ar perkėlimo užsakymo dokumente gauti parduotuvėje, bet kai kurios eilutės lieka atidarytos.
- **Viskas gauta** – gautos visos pirkimo užsakymo ar perkėlimo užsakymo dokumento eilutės ir kiekiai. Dokumentai yra prieinami tik skirtuke **Baigti** ir parduotuvės vartotojai gali juos tik skaityti.
- **Vykdoma** – ši būsena naudojama informuoti įrenginių vartotojus, kad su dokumentu aktyviai dirba kitas vartotojas.
- **Pristabdyta** – ši būsena rodoma pasirinkus **Pristabdyti gavimą**, siekiant laikinai sustabdyti gavimo procesą.
- **Apdorojama būstinėje** – dokumentas buvo pateiktas „Commerce“ būstinei EKA programoje, tačiau jis dar nebuvo sėkmingai užregistruotas „Commerce“ būstinėje. Atliekamas nesinchroninis dokumento registravimo procesas. Sėkmingai užregistravus dokumentą „Commerce“ būstinėje, jo būsena turi būti atnaujinta į **Viskas gauta** arba **Gauta iš dalies**.
- **Apdoroti nepavyko** – dokumentas buvo užregistruotas „Commerce“ būstinėje ir atmestas. Srityje **Išsami informacija** nurodoma, kodėl nepavyko užregistruoti. Siekiant ištaisyti duomenų klaidas, dokumentą reikia redaguoti, tada jį reikia pakartotinai pateikti „Commerce“ būstinei apdoroti.

Kai sąraše pasirenkate dokumento eilutę, rodoma sritis **Išsami informacija**. Šioje srityje pateikiama papildoma informacija apie dokumentą, pvz., siuntimo ir datos informacija. Eigos juostoje rodoma, kiek prekių dar reikia apdoroti. Jeigu dokumento nepavyko sėkmingai apdoroti „Commerce“ būstinėje", srityje **Išsami informacija** taip pat rodomi su triktimi susiję klaidų pranešimai.

Norėdami peržiūrėti išsamią informaciją apie dokumentą, dokumentų sąrašo puslapio rodinyje programos juostoje galite pasirinkti **Užsakymo informacija**. Taip pat galite aktyvinti gavimo apdorojimą tinkamose dokumento eilutėse.

Dokumentų sąrašo puslapio rodinyje taip pat galite sukurti naują gaunamo perkėlimo užsakymo užklausą, skirtą parduotuvei. Dokumentų būsena lieka **Juodraštis** ir juos galima koreguoti arba panaikinti, kol jie bus pateikti apdoroti į „Commerce“ būstinę. Juos pateikus į „Commerce“ būstinę, perkėlimo užsakymo eilučių nebegalima pakeisti naudojant EKA programą.

## <a name="receiving-process"></a>Gavimo procesas

Pasirinkę pirkimo užsakymą arba perkėlimo užsakymo dokumentą skirtuke **Aktyvieji**, galite pasirinkti **Užsakymo informacija**, kad pradėtumėte gavimo procesą.

Pagal numatytuosius nustatymus pateikiamas rodinys **Gaunama dabar**. Šis rodinys optimizuotas brūkšniniams kodams nuskaityti. Jis gali būti naudojamas nuskaitytų prekių sąrašui sudaryti, kad būtų galima gauti šias prekes. Norėdami pradėti gavimo procesą, galite pradėti nuskaityti prekių brūkšninius kodus.

Kadangi prekių brūkšniniai kodai nuskaitomi naudojant rodinį **Gaunama dabar**, programa patikrina prekes pagal pasirinkto pirkimo ar perkėlimo užsakymo dokumentą, kad įsitikintų, jog kiekviena nuskaityta prekė atitinka tinkamą dokumento prekę. Laikoma, kad kaskart nuskaitant brūkšninį kodą rodinyje **Gaunama dabar**, gaunamas kiekis yra vienas vienetas, nebent kiekis būtų įtrauktas į brūkšninį kodą. Galite pakartotinai nuskaityti brūkšninius kodus šiame rodinyje, norėdami sukurti visų gaunamų prekių ir kiekių sąrašą.

### <a name="example-scenario"></a>Pavyzdinis scenarijus

Vartotojas gauna pirkimo užsakymą, kuriame yra 10 brūkšninio kodo 5657900266 vienetų. Vartotojas gali nuskaityti tą brūkšninį kodą 10 kartų, kad kaskart nuskenavus į lauką **Gaunama dabar** būtų pridedama po vieną vienetą. Vartotojui baigus nuskaityti, prekės eilutėje esančiame lauke **Gaunama dabar** bus rodoma, kad gautas kiekis yra 10 vienetų.

Tačiau jei prekių kiekis yra didelis, vartotojas gali nuspręsti įvesti kiekį rankiniu būdu, o ne nuskaityti kiekvienos gaunamos prekės brūkšninį kodą. Šiuo atveju vartotojas gali nuskaityti brūkšninį kodą vieną kartą, kad įtrauktų prekę į sąrašą **Gaunama dabar**. Tada vartotojas gali pasirinkti susijusią eilutę, esančią rodinyje **Gaunama dabar**, o tada srityje **Išsami informacija**, kuri rodoma dešinėje puslapio pusėje, atnaujinti prekės lauką **Gaunamas kiekis** .

Nors rodinys **Gaunama dabar** yra optimizuotas brūkšniniams kodams nuskaityti, vartotojai programos juostoje taip pat gali pasirinkti **Gauti produktą**, o tada dialogo lange įvesti prekės ID arba brūkšninio kodo duomenis. Įvedus ir patikrinus prekę, vartotojas paraginamas įvesti gaunamą kiekį.

Rodinyje **Gaunama dabar** vartotojams suteikiama galimybė pamatyti gaunamus produktus. Taip pat galima naudoti rodinį **Visas užsakymų sąrašas**. Šiame rodinyje pateikiamas visas pasirinkto pirkimo ar perkėlimo užsakymo dokumento eilučių sąrašas. Vartotojai gali rankiniu būdu pasirinkti eilutes sąraše ir tada srityje **Išsami informacija** atnaujinti pasirinktos eilutės lauką **Gaunamas kiekis**. Rodinyje **Visas užsakymų sąrašas** vartotojai gali nuskaityti brūkšninius kodus arba jie gali naudoti funkciją **Gauti produktą**, kad įvestų prekės ID arba brūkšninį kodą ir duomenis apie gaunamą kiekį, prieš tai nepasirinkdami atitinkamą prekės eilutę sąraše.

### <a name="over-receiving-validations"></a>Patikros gavus per daug

Tikrinimas vykdomas dokumento eilučių gavimo proceso metu. Jis apima pristatymo perviršio tikrinimą. Jei vartotojas bando gauti daugiau atsargų, nei buvo užsakyta pirkimo užsakyme, bet pristatymo perviršis nesukonfigūruotas arba gauta suma viršija pirkimo užsakymo eilutėje sukonfigūruotą leistiną pristatymo perviršio nuokrypį, vartotojas gauna klaidą ir jam neleidžiama gauti perteklinio kiekio.

Gavimo viršijimas neleidžiamas perkėlimo užsakymų dokumentuose. Vartotojai visada gaus klaidų, jei mėgins gauti daugiau, nei buvo išsiųsta pagal perkėlimo užsakymo eilutę.

### <a name="receiving-location-controlled-items"></a>Pagal vietą kontroliuojamų prekių gavimas

Jei gaunamos prekės yra pagal vietą kontroliuojamos prekės, vartotojai gali pasirinkti vietą, kurioje jie nori gauti prekes gavimo proceso metu. Rekomenduojame sukonfigūruoti numatytąją parduotuvės sandėlio gavimo vietą, kad šis procesas būtų efektyvesnis. Net jei numatytoji vieta sukonfigūruota, vartotojai gali pagal poreikį nepaisyti gavimo vietos pasirinktose eilutėse.

Vykdant operaciją atsižvelgiama į konfigūraciją **Galimas tuščias gavimas**, esančią saugojimo dimensijoje **Vieta**, ir nereikalaujama, kad vietos dimensija būtų įvesta, jei sukonfigūruotas tuščias gavimas. Jei negalima naudoti tuščių prekės gavimo vietų, EKA programoje rodoma klaida ir reikalaujama, kad prieš registruojant gavimą būtų įvesta vieta.

### <a name="receive-all"></a>Gauti viską

Jei reikia, galite pasirinkti **Gauti viską** programos juostoje, kad greitai pakeistumėte visų dokumento eilučių kiekį **Gaunama dabar** į didžiausią galimą atitinkamų eilučių gaunamą kiekį.

### <a name="cancel-receiving"></a>Atšaukti gavimą

Naudokite funkciją **Atšaukti gavimą** programos juostoje tik tada, jei norite išeiti iš dokumento, neįrašę jokių pakeitimų. Pavyzdžiui, iš pradžių pasirinkote netinkamą dokumentą ir nenorite, kad būtų įrašyti ankstesni gavimo duomenys.

### <a name="pause-receiving"></a>Pristabdyti gavimą

Jei gaunate atsargų, galite naudoti funkciją **Pristabdyti gavimą**, jei norite padaryti pertrauką gavimo procese. Pavyzdžiui, norite atlikti kitą EKA operaciją, pavyzdžiui, įforminti pardavimą klientui arba atidėti gavimo registravimą.

Kai pasirenkate **Pristabdyti gavimą**, dokumento būsena pakeičiama į **Pristabdyta**. Todėl vartotojai žinos, kad dokumento duomenys įvesti, bet dokumentas dar nepatvirtintas. Kai būsite pasirengę tęsti gavimo procesą, pasirinkite pristabdytą dokumentą ir pasirinkite **Užsakymo informacija**. Visi anksčiau įrašyti **Gaunama dabar** kiekiai išsaugomi ir juos galima peržiūrėti rodinyje **Visas užsakymų sąrašas**.

### <a name="finish-receiving"></a>Baigti gavimą

Kai baigsite įvesti visus produktų **Gaunama dabar** kiekius, turite pasirinkti **Baigti gavimą** programos juostoje, kad būtų galima apdoroti gavimą.

Kai vartotojai užbaigia pirkimo užsakymo gavimą, jie paraginami įvesti vertę lauke **Gavimo numeris**, jei ši funkcija sukonfigūruota. Paprastai ši vertė atitinka tiekėjo važtaraščio identifikatorių. Duomenys **Gavimo numeris** bus saugomi „Commerce“ būstinės produktų gavimo kvitų žurnale. Perkėlimo užsakymų gavimų gavimo numeriai nefiksuojami.

Naudojant nesinchroninį dokumentų apdorojimą, gavimas pateikiamas naudojant nesinchroninę dokumentų sistemą. Laikas, kurio reikia dokumentui užregistruoti, priklauso nuo dokumento dydžio (eilučių skaičiaus) ir bendro apdorojamų duomenų srauto serveryje. Paprastai šis procesas atliekamas per keletą sekundžių. Jei dokumento užregistruoti nepavyksta, vartotojui pranešama per dokumentų sąrašą **Gaunamos operacijos**, kur dokumento būsena bus pakeista į **Apdoroti nepavyko**. Vartotojas gali pasirinkti neapdorotą dokumentą EKA, kad pamatytų klaidų pranešimus ir nepavykusio apdorojimo priežastį srityje **Išsami informacija**. Neapdorotas dokumentas lieka neužregistruotas ir reikia, kad vartotojas grįžtų prie dokumento eilučių, EKA pasirinkęs **Užsakymo informacija**. Vartotojas turi ištaisyti dokumento klaidas. Pataisęs dokumentą, vartotojas gali bandyti dar kartą jį apdoroti, programos juostoje pasirinkdamas **Baigti įvykdymą**.

## <a name="create-an-inbound-transfer-order"></a>Gaunamo perkėlimo užsakymo kūrimas

EKA vartotojai gali kurti naujus perkėlimo užsakymų dokumentus. Norėdami pradėti procesą, programos juostoje pasirinkite **Naujas**, būdami pagrindiniame dokumentų sąraše **Gaunamos operacijos**. Matysite paraginimą pasirinkti sandėlį ar parduotuvę **Perkelti iš**, iš kurių atsargos bus pristatomos į parduotuvės vietą. Galimos tik vertės, pasirinktos parduotuvės įvykdymo grupės konfigūracijoje. Gaunamo perkėlimo užsakymo užklausoje dabartinė parduotuvė perkėlimo užsakyme visada bus sandėlis **Perkelti iš**. Tos vertės pakeisti negalima.

Laukuose **Siuntimo data**, **Gavimo data** ir **Pristatymo būdas** įveskite reikiamas vertes. Taip pat galite parašyti pastabą, kuri bus saugoma kartu su perkėlimo užsakymo antrašte kaip „Commerce“ būstinės dokumento priedas.

Sukūrę antraštės informaciją, galite įtraukti produktų į perkėlimo užsakymą. Norėdami pradėti prekių ir norimų kiekių įtraukimo procesą, pasirinkite **Įtraukti produktą**. Srityje **Išsami informacija** į žurnalo eilutes taip pat galite įtraukti konkrečioms eilutėms skirtų pastabų. Šios pastabos bus saugomos kaip eilutės priedas.

Įvedę gaunamo perkėlimo užsakymo eilutes, turite pasirinkti **Įrašyti**, kad dokumento keitimai būtų įrašyti vietoje, arba pasirinkti **Pateikti užklausą**, kad išsami užsakymo informacija būtų pateikta „Commerce“ būstinei tolesniam apdorojimui atlikti. Jei pasirinksite **Įrašyti**, dokumento juodraštis bus saugomas kanalo duomenų bazėje, o siuntimo sandėlis negalės vykdyti dokumento, kol jis nebus sėkmingai apdorotas naudojant **Pateikti užklausą**. Pasirinkite **Įrašyti** tik tada, jei nesate pasirengę pateikti užklausos „Commerce“ būstinei apdoroti.

Jei dokumentas įrašomas vietoje, jį rasite skirtuke **Juodraščiai** dokumentų sąraše **Gaunamos operacijos**. Kol dokumento būsena yra **Juodraštis**, galite jį redaguoti pasirinkdami **Redaguoti**. Pagal poreikį galite atnaujinti, įtraukti ar naikinti eilutes. Be to, galite panaikinti visą dokumentą, kurio būsena yra **Juodraštis**, pasirinkę **Naikinti** skirtuke **Juodraščiai**.

Sėkmingai pateikus dokumento juodraštį „Commerce“ būstinei, jis rodomas skirtuke **Aktyvieji** skirtuke ir jo būsena yra **Pageidaujama**. Šiuo metu gaunančios parduotuvės arba sandėlio vartotojai nebegali redaguoti pateikto gaunamo perkėlimo užsakymo dokumento. Dokumentą gali redaguoti tik siuntimo sandėlio vartotojai, EKA programoje pasirinkę **Siuntimo operacija**. Redagavimo užraktu užtikrinama, kad nekiltų konfliktų gaunančiam prašytojui pakeitus perkėlimo užsakymą tuo pačiu metu, kai siunčiantis siuntėjas aktyviai paima ir siunčia užsakymą. Jei, pateikus perkėlimo užsakymą, gaunanti parduotuvė arba sandėlis turi pateikti pakeitimų, reikia susisiekti su siunčiančiu siuntėju ir paprašyti įvesti pakeitimus.

Dokumentui įgijus būseną **Pageidaujama**, jis matomas skirtuke **Aktyvieji**. Tačiau, gaunanti parduotuvė arba sandėlis dar jo gauti negali. Siuntimo sandėliui išsiuntus visus perkėlimo užsakymo punktus arba jų dalį, gaunanti parduotuvė arba sandėlis gali registruoti gavimus EKA. Siunčiančiai šaliai apdorojus perkėlimo užsakymo dokumentus, jų būsena pakeičiama iš **Pageidaujama** į **Išsiųsta** arba **Iš dalies išsiųsta**. Dokumentams įgijus būseną **Išsiųsta** arba **Iš dalies išsiųsta**, gaunanti parduotuvė arba sandėlis gali pagal juos registruoti gavimus, naudodami gaunamų operacijų gavimo procesą.

## <a name="related-topics"></a>Susijusios temos

[Siunčiamų atsargų operacijos EKA](pos-outbound-inventory-operation.md)
