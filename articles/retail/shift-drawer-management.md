---
title: Pamainos ir kasos stalčių valdymas
description: Šioje temoje paaiškinama, kaip mažmeninės prekybos elektroniniame kasos aparate (EKA) nustatyti ir naudoti pamainas.
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7ad3c3fd17e88f364be12c122e2f5c155b7b9064
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "313019"
---
# <a name="shift-and-cash-drawer-management"></a>Pamainos ir kasos stalčių valdymas

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip mažmeninės prekybos elektroniniame kasos aparate (EKA) nustatyti ir naudoti pamainas.

Sprendime „Microsoft Dynamics 365 for Retail“ terminu *pamaina* aprašomas EKA operacijų duomenų rinkimas tarp dviejų laiko taškų. Numatoma kiekvienos pamainos pinigų suma palyginama su apskaičiuota ir deklaruota suma.

Paprastai pamainos pradedamos darbo dienos pradžioje. Tuo metu vartotojas deklaruoja pradinę sumą, esančią kasos stalčiuje. Tada visą dieną atliekamos pardavimo operacijos. Galiausiai dienos pabaigoje suskaičiuojamas stalčius ir deklaruojamos galutinės sumos. Pamaina baigiama ir sugeneruojama Z ataskaita. Z ataskaita nurodo, ar yra perteklius, ar – trūkumas.

## <a name="typical-shift-scenarios"></a>Įprastos pamainų situacijos

„Retail“ siūlo kelias konfigūravimo parinktis ir EKA operacijas, kad būtų galima atlikti įvairius EKA dienos pabaigos verslo procesus. Šiame skyriuje aprašomos kelios įprastos pamainų situacijos.

### <a name="fixed-till"></a>Fiksuotas kasos stalčiaus skyrelis

Paprastai ši situacija naudojama dažniausiai. Ji vis dar plačiai naudojama. Fiksuoto kasos stalčiaus skyrelio pamainoje ji ir skyrelis susieti su konkrečiu kasos aparatu. Jie iš vieno kasos aparato į kitą neperkeliami. Fiksuoto kasos stalčiaus skyrelio pamainą gali naudoti vienas vartotojas arba bendrai naudoti keli vartotojai. Fiksuoto kasos stalčiaus skyrelio pamainų nereikia niekaip specialiai konfigūruoti.

### <a name="floating-till"></a>Nefiksuotas kasos stalčiaus skyrelis

Nefiksuoto kasos stalčiaus skyrelio pamainoje ją ir kasos stalčių galima perkelti iš vieno kasos aparato į kitą. Nors su vienu kasos aparato stalčiumi gali būti susieta tik viena aktyvi pamaina, pamainas galima sustabdyti ir pratęsti vėliau arba kitame kasos aparate.

Pavyzdžiui, parduotuvėje yra du kasos aparatai. Kiekvienas kasos aparatas atidaromas dienos pradžioje, kai kasininkas pradeda naują pamainą ir nurodo pradinę sumą. Kai vienas kasininkas pasirengęs daryti pertrauką, jis sustabdo savo pamainą ir iš kasos stalčiaus išima skyrelį. Tą kasos aparatą tada gali naudoti kiti kasininkai. Prie jo gali prisijungti ir savo pamainą pradėti kitas kasininkas. Pasibaigus pirmojo kasininko pertraukai, jis savo pamainą gali pratęsti atsilaisvinus vienam iš kitų kasos aparatų. Nefiksuoto kasos stalčiaus skyrelio pamainų nereikia niekaip specialiai konfigūruoti ir joms nereikia jokių specialių teisių.

### <a name="single-user"></a>Vienas vartotojas

Daug mažmenininkų vienoje pamainoje dažniau leidžia dirbti tik vienam vartotojui, kad būtų lengviau užtikrinti aukščiausio lygio atskaitomybę už kasos stalčiuje esančius grynuosius pinigus. Jei naudoti su pamaina susietą kasos stalčiaus skyrelį leidžiama tik vienam vartotojui, tik jį galima laikyti atsakingu už bet kokius neatitikimus. Jei pamainą naudoja daugiau nei vienas vartotojas, sunku nustatyti, kas suklydo ar kas galbūt bando vogti iš kasos stalčiaus skyrelio.

### <a name="multiple-users"></a>Keletas naudotojų

Kai kurie mažmenininkai pasiruošę paaukoti atskaitomybės lygį, kurį suteikia vieno vartotojo pamainos, ir vienoje pamainoje leisti dirbti daugiau nei vienam vartotojui. Taip paprastai elgiamasi, kai vartotojų yra daugiau nei laisvų kasos aparatų ir lankstumo bei greičio poreikis yra svarbesnis už nuostolių galimybę. Tai taip tai įprasta, kai parduotuvių vadovai neturi savo pamainų, tačiau prireikus gali naudoti bet kurio iš kasininkų pamainas. Kad galėtų prisijungti prie pamainos, kurią pradėjo kitas vartotojas, ir ją naudoti, vartotojas turi turėti EKA teisę **Leisti jungtis prie kelių pamainų**.

### <a name="shared-shift"></a>Bendrai naudojama pamaina

Bendrai naudojamos pamainos konfigūracija mažmenininkams leidžia turėti vieną pamainą, naudojamą keliuose kasos aparatuose, kasos stalčiuose ir kurią naudoja keli vartotojai. Bendrai naudojamoje pamainoje naudojama viena pradinė suma ir viena galutinė suma, kurios sumuojamos tarp visų kasos stalčių. Bendrai naudojamas pamainas dažniausiai renkamasi naudojant mobiliuosius įrenginius. Tokioje situacijoje atskiras kasos stalčius kiekvienam kasos aparatui nerezervuojamas. Vietoj to visi kasos aparatai gali bendrai naudoti vieną kasos stalčių.

Kad parduotuvėje būtų galima naudoti bendrai naudojamas pamainas, kasos stalčius dalyje **Mažmeninė prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Aparatūros profiliai \> Stalčius** turi būti sukonfigūruotas kaip bendrai naudojamos pamainos stalčius. Be to, vartotojai turi turėti vieną ar abi bendrai naudojamų pamainų teises (Leisti valdyti bendrai naudojamą pamainą ir Leisti naudoti bendrai naudojamą pamainą).

> [!NOTE]
> Kiekvienoje parduotuvėje vienu metu gali būti pradėta tik viena bendrai naudojama pamaina. Toje pačioje parduotuvėje galima naudoti bendrai naudojamas pamainas ir atskiras pamainas.

## <a name="shift-and-drawer-operations"></a>Pamainų ir stalčių operacijos

Pamainos būsenai pakeisti arba pinigų sumai kasos stalčiuje padidinti ar sumažinti galima atlikti įvairias operacijas. Šiame skyriuje aprašomos šios pamainų operacijos, skirtos „Microsoft Dynamics 365 for Retail“ sprendimams „Modern POS“ ir „Cloud POS“.

### <a name="open-shift"></a>Atidaryta pamaina

Vartotojams norint naudojant EKA atlikti bet kokias operacijas, kuriomis bus gauta finansinė operacija, pvz., pardavimas, grąžinimas ar kliento užsakymas, jiems reikia turėti aktyvią pradėtą pamainą.

Vartotojui prisijungus prie EKA, sistema pirmiausia patikrina, ar esamame kasos aparate tas vartotojas turi aktyvią pamainą. Jei aktyvios paskyros nėra, vartotojas gali pradėti naują pamainą, pratęsti esamą arba prisijungti ne stalčiaus režimu – tai priklauso nuo sistemos konfigūracijos ir vartotojo teisių.

### <a name="declare-start-amount"></a>Deklaruoti pradinę sumą

Ši operacija dažnai yra pirma operacija, kuri atliekama naujai pradėtoje pamainoje. Atlikdami šią operaciją vartotojai nurodo pradinę grynųjų pamainos pinigų sumą kasos stalčiuje. Ši operacija yra svarbi, nes baigus pamainą skaičiuojant perteklių / trūkumą atsižvelgiama į pradinę sumą.

### <a name="float-entry"></a>Nefiksuotas įrašas

*Nefiksuoti įrašai* yra ne pardavimo operacijos, atliekamos aktyvioje pamainoje siekiant kasos stalčiuje padidinti grynųjų pinigų sumą. Įprastas nefiksuoto įrašo pavyzdys – operacija, kuria papildomas stalčiaus grąžos likutis, kai šis baiginėjasi.

### <a name="tender-removal"></a>Mokėjimo priemonės šalinimas

*Mokėjimo priemonės šalinimai* yra ne pardavimo operacijos, atliekamos aktyvioje pamainoje, siekiant sumažinti grynųjų pinigų sumą kasos stalčiuje. Ši operacija dažniausiai naudojama kartu su operacija Nefiksuotas įrašas, atliekama kitoje pamainoje. Pavyzdžiui, kadangi 1 kasos aparate baiginėjasi grąžos likutis, vartotojas 2 kasos aparate atlieka mokėjimo priemonės šalinimo operaciją, kad sumažintų sumą savo kasos stalčiuje. Tada vartotojas 1 kasos aparate atlieka fiksuoto įrašo operaciją, kad padidintų sumą savo kasos stalčiuje.

### <a name="suspend-shift"></a>Sustabdyti pamainą

Vartotojai gali sustabdyti aktyvią pamainą, kad dabartinį kasos aparatą atlaisvintų kitam vartotojui arba savo pamainą perkeltų į kitą kasos aparatą (tokiu atveju pamaina dažnai vadinama nefiksuoto kasos stalčiaus skyrelio pamaina).

Sustabdžius pamainą neleidžiama atlikti jokių naujų pamainos operacijų ar pakeitimų, kol pamaina nebus pratęsta.

### <a name="resume-shift"></a>Pratęsti pamainą

Ši operacija vartotojams leidžia kasos aparate, kuris dar neturi aktyvios pamainos, pratęsti anksčiau sustabdytą pamainą.

### <a name="tender-declaration"></a>Mokėjimo priemonių deklaravimas

Ši operacija atliekama norint nurodyti visą pinigų sumą, šiuo metu esančią kasos stalčiuje. Vartotojai šią operaciją dažniausiai atlieka prieš baigdami pamainą. Nurodyta suma palyginama su numatoma pamainos suma ir taip apskaičiuojama pertekliaus / trūkumo suma.

### <a name="safe-drop"></a>Pinigų įnešimas į įmonės kasą

Aktyvioje pamainoje bet kada galima atlikti pinigų įnešimo į seifą operaciją. Atliekant šią operaciją iš stalčiaus išimama pinigų, kad juos būtų galima perkelti į saugesnę vietą, pvz., į seifą galiniame kambaryje. Visa įrašyta į seifą įneštų pinigų suma įtraukiama į bendrąsias pamainos sumas, tačiau jos nereikia skaičiuoti deklaruojant mokėjimo priemones.

### <a name="bank-drop"></a>Inkasavimas

Kaip ir įnešami į seifą, aktyviose pamainose pinigai inkasuojami. Atlikus šią operaciją pinigai pašalinami iš pamainos, kad būtų pasiruošta banko indėliui.

### <a name="blind-close-shift"></a>Uždaryti pamainą anonimiškai

*Anonimiškai baigtos pamainos* yra nebeaktyvios, tačiau jos nėra visiškai baigtos. Kitaip nei sustabdytų pamainų, anonimiškai baigtų pamainų pratęsti negalima. Tačiau vėliau arba kitame kasos aparate su jomis galima atlikti tokias operacijas kaip Deklaruoti pradinę sumą ir Mokėjimo priemonių deklaravimas.

Anonimiškai baigtos pamainos dažnai naudojamos norint naujam vartotojui ar pamainai atlaisvinti kasos aparatą ir kad prieš tai nereikėtų visiškai suskaičiuoti, suderinti ir baigti pamainos.

### <a name="close-shift"></a>Uždaryti pamainą

Atliekant šią operaciją apskaičiuojamos bendrosios pamainos sumos ir pertekliaus / trūkumo sumos, o tada galutinai užbaigiama aktyvi arba anonimiškai baigta pamaina. Jei vartotojas turi reikiamas teises, taip pat išspausdinama pamainos Z ataskaita. Baigtų pamainų pratęsti ar modifikuoti negalima.

### <a name="print-x"></a>Spausdinti X

Šia operacija sugeneruojama ir išspausdinama esamos aktyvios pamainos X ataskaita.

### <a name="reprint-z"></a>Perspausdinti Z

Šia operacija perspausdinama paskutinė Z ataskaita, kurią sistema sugeneravo baigiant pamainą.

### <a name="manage-shifts"></a>Valdyti pamainas

Ši operacija vartotojams leidžia peržiūrėti visas aktyvias, sustabdytas ir anonimiškai baigtas parduotuvės pamainas. Jei turi reikiamas teises, vartotojai su anonimiškai baigtomis pamainomis gali atlikti galutines baigimo procedūras, pvz., operacijas Mokėjimo priemonių deklaravimas ir Baigti pamainą. Atlikdami šią operaciją vartotojai taip pat gali peržiūrėti ir panaikinti netinkamas pamainas, kai, retais atvejais, perjungiant iš autonominio režimo į internetinį ir atvirkščiai, jos paliekamos blogos būsenos. Šiose netinkamose pamainose nėra jokios finansinės informacijos ar operacijų duomenų, reikalingų derinimui atlikti.

## <a name="shift-and-drawer-permissions"></a>Pamainų ir stalčių teisės

Tolesnės EKA teisės lemia, ką įvairiose situacijose gali ir ko negali atlikti vartotojas.

- **Įgalinti anoniminį uždarymą**
- **Leisti spausdinti X ataskaitą**
- **Leisti spausdinti Z ataskaitą**
- **Leisti mokėjimo priemonių deklaravimą**
- **Leisti srauto deklaravimą**
- **Atidaryti stalčių be pardavimo**
- **Leisti jungtis prie kelių pamainų** – ši teisė vartotojui leidžia prisijungti prie kito vartotojo pradėtos pamainos ir ją naudoti. Šios teisės neturintys vartotojai gali prisijungti tik prie savo pradėtų pamainų ir naudoti tik jas.
- **Leisti valdyti bendrai naudojamą pamainą** – vartotojai šią teisę privalo turėti norėdami pradėti arba baigti bendrai naudojamą pamainą.
- **Leisti naudoti bendrai naudojamą pamainą** – vartotojai šią teisę privalo turėti norėdami prisijungti prie bendrai naudojamos pamainos ir ją naudoti.

## <a name="back-office-end-of-day-considerations"></a>Ką dienos pabaigoje reikėtų apsvarstyti tarnybiniame biure

EKA aparate pamainos ir kasos stalčius derinami kitaip nei skaičiuojant išrašus apibendrinami operacijų duomenys. Svarbu šį skirtumą suprasti. Pamainos duomenys EKA aparate (Z ataskaita) ir tarnybiniame biure apskaičiuotas išrašas gali pateikti skirtingus rezultatus – tai priklauso nuo jūsų konfigūracijos ir verslo procesų. Šis skirtumas nebūtinai reiškia, kad neteisingi pamainos duomenys ar apskaičiuotas išrašas, arba kad yra problemų su duomenimis. Jis tiesiog reiškia, kad nurodyti parametrai gali įtraukti papildomų operacijų arba operacijų įtraukti mažiau, arba kad operacijos skirtingai apibendrintos.

Nors kiekvienas mažmenininkas taiko skirtingus verslo reikalavimus, kad išvengtumėte situacijų, kai pasitaiko tokio tipo skirtumų, savo sistemą rekomenduojame nustatyti taip, kaip nurodyta toliau.

Eikite į **Mažmeninė prekyba \> Kanalai \> Mažmeninės prekybos parduotuvės \> Visos mažmeninės prekybos parduotuvės \> Išrašas / baigimas** ir kiekvienos parduotuvės laukus **Išrašo metodas** bei **Baigimo metodas** nustatykite kaip **Pamaina**.

Tokia sąranka padeda užtikrinti, kad į tarnybinio biuro išrašus būtų įtrauktos tos pačios operacijos kaip EKA pamainos ir kad duomenys būtų apibendrinami pagal tą pamainą.

Norėdami apie išrašų ir baigimo metodus gauti daugiau informacijos, žr. [„Retail” išrašo parduotuvės konfigūracijos](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).
