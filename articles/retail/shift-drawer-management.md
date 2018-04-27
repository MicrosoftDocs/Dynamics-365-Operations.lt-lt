---
title: "Pamainos ir kasos stalčių valdymas"
description: "Šiame straipsnyje paaiškinta, kaip nustatyti ir naudoti dviejų tipų mažmeninės prekybos elektroninio kasos aparato (EKA) pamainas – bendrai naudojamą ir atskirą. Bendrai naudojimas pamainas keliose vietose gali naudoti keli vartotojai, o atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: lt-lt
ms.lasthandoff: 03/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Pamainos ir kasos stalčių valdymas

[!INCLUDE [banner](includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip nustatyti ir naudoti dviejų tipų mažmeninės prekybos elektroninio kasos aparato (EKA) pamainas – bendrai naudojamą ir atskirą. Bendrai naudojimas pamainas keliose vietose gali naudoti keli vartotojai, o atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas.

Galimi du mažmeninės prekybos elektroninio kasos aparato (EKA) pamainų tipai: atskira ir bendrai naudojama. Atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas. Bendrai naudojimas pamainas gali naudoti keli vartotojai keliose vietose. Todėl parduotuvėje galima veiksmingai sukurti keliems vartotojams skirtą vieną pamainą.

## <a name="standalone-shifts"></a>Atskiros pamainos
Atskiros pamainos naudojamos tradiciniu, pastoviu POS scenarijumi, kada kiekvieno EKA registro grynieji pinigai yra suderinamos atskirai. Pvz., parduotuvės aplinkoje paprastai yra keli fiksuoti EKA registrai, o kasininkas priskirtas kiekvienam registrui. Šiuo atveju kiekvienas registras greičiausiai naudoja atskirą pamainą, o kasininkas yra atsakingas už to registro kasos stalčiaus skyrelį arba fizinės formos grynuosius pinigus. Atskira pamaina apima visą veiklą tame registre per kasininko darbo pamainą. Veiklos gali apimti į kasos stalčiaus skyrelį padėtos sumos atidarymą, visas grynųjų pinigų išėmimo ir įdėjimo operacijas, pvz., inkasavimus ir srauto įrašą, ir mokėjimo priemonių deklaravimą pamainai pasibaigus.

### <a name="set-up-a-stand-alone-shift"></a>Atskiros pamainos nustatymas

Atskira pamaina priskiriama kasos stalčiaus lygyje. Šioje procedūroje paaiškinama, kaip nustatyt atskirą pamainą EKA registre.

1.  Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**.
2.  Pasirinkite naudotiną atskirtos pamainos aparatūros šabloną.
3.  „FastTab“ **Stalčius** patikrinkite, ar parinktis **Bendrai naudojamos pamainos stalčius** yra nustatyta į **Ne**.
4.  Spustelėkite **Įrašyti**.
5.  Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Registrai**.
6.  Pasirinkite registrą, kuriam reikalinga atskira pamaina, ir tada spustelėkite **Redaguoti**.
7.  Lauke **Aparatūros šablonas** pasirinkite aparatūros šabloną, kurį pasirinkote atlikdami 2 veiksmą.
8.  Spustelėkite **Įrašyti**.
9.  Spustelėkite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
10. Pasirinkite **1090** pasiskirstymo grafiką, o tada spustelėkite **Vykdyti dabar**, kad sinchronizuotumėte EKA keitimus.

### <a name="use-a-stand-alone-shift"></a>Atskiros pamainos naudojimas

1.  Prisijunkite prie EKA.
2.  Jei neatidaryta jokia pamaina, pasirinkite **Atidaryti naują pamainą**.
3.  Pasirinkite operaciją **Deklaruoti pradinę sumą** ir nurodykite grynųjų pinigų sumą, kuri bus įtraukta į kasos stalčiaus skyrelį darbo dienos pradžioje.
4.  Atlikite keletą operacijų.
5.  Pasibaigus dienai pasirinkite **Deklaruoti mokėjimo priemonę**, kad deklaruotumėte kasos stalčiuje likusią grynųjų pinigų sumą.
6.  Įveskite grynųjų pinigų sumą, o tada spustelėkite **Įrašyti**, kad įrašytumėte mokėjimo priemonės deklaravimą.
7.  Pasirinkite **Uždaryti pamainą**, kad uždarytumėte pamainą.

**Pastaba.** Pamainos metu galima atlikti kitas operacijas, priklausomai nuo vykdomų verslo procesų. Galima atlikti operacijas **Pinigų įnešimas į kasą**, **Inkasavimas** ir **Mokėjimo priemonės šalinimas**, norint dienos metu arba prieš uždarant pamainą iš kasos stalčiaus skyrelio išimti pinigus. Jei kasos stalčiaus skyrelyje yra per mažai pinigų, galima naudoti operaciją **Srauto įrašas**, norint į kasos stalčiaus skyrelį įdėti grynųjų pinigų.

## <a name="shared-shifts"></a>Bendrai naudojamos pamainos
Bendrai naudojama pamaina naudojama tada, kai visą darbo dieną keli kasininkai bendrai naudoja kasos stalčių arba kasos stalčių rinkinį. Paprastai bendrai naudojama pamaina yra naudojama mobiliojoje EKA aplinkoje. Mobiliojoje aplinkoje nė vienas kasininkas nėra priskirtas arba atsakingas už vieną kasos stalčių. Visi kasininkai turi turėti galimybę užregistruoti pardavimą ir įdėti pinigų į artimiausią kasos aparatą. Tokiu atveju kasos stalčiai, kuriuos kasininkai bendrai naudoja, įtraukiami į bendrai naudojamą pamainą. Visi bendrai naudojamos pamainos kasos stalčiai įtraukiami į vieną pamainą, kad būtų galima vykdyti su grynųjų pinigų valdymu susijusias tos pamainos veiklas. Todėl pradinė pamainos suma turėtų apimti visuose į bendrai naudojamą pamainą įtrauktuose kasos stalčiuose esančią grynųjų pinigų sumą. Taip pat mokėjimo priemonės deklaravimas bus visuose į bendrai naudojamą pamainą įtrauktuose kasos stalčiuose esanti grynųjų pinigų suma. **Pastaba:** kiekvienoje parduotuvėje vienu metu galima atidaryti tik vieną bendrai naudojamą pamainą. Toje pačioje parduotuvėje galima naudoti bendrai naudojamas pamainas ir atskiras pamainas.

### <a name="set-up-a-shared-shift"></a>Bendrai naudojamos pamainos nustatymas

1.  Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**.
2.  Pasirinkite naudotiną bendrai naudojamos pamainos aparatūros šabloną.
3.  „FastTab“ **Stalčius** parinktį **Bendrai naudojamos pamainos stalčius** nustatykite į **Taip**.
4.  Spustelėkite **Įrašyti**.
5.  Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Registrai**.
6.  Pasirinkite registrą, kuriam reikalinga bendrai naudojama pamaina, ir tada spustelėkite **Redaguoti**.
7.  Lauke **Aparatūros šablonas** pasirinkite aparatūros šabloną, kurį pasirinkote atlikdami 2 veiksmą.
8.  Spustelėkite **Įrašyti**.
9.  Spustelėkite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
10. Pasirinkite **1090** pasiskirstymo grafiką, o tada spustelėkite **Vykdyti dabar**, kad sinchronizuotumėte EKA keitimus.

### <a name="use-a-shared-shift"></a>Bendrai naudojamos pamainos naudojimas

1.  Prisijunkite prie EKA.
2.  Jei dar EKA dar neprijungtas prie aparatūros stoties, pasirinkite **Su stalčiumi nesusijusi operacija**, o tada pasirinkite operaciją **Pasirinkti aparatūros stotį**, kad suaktyvintumėte bendrai naudojamos pamainos aparatūros stotį. Šį veiksmą reikia atlikti tik pirmą kartą registrą įtraukiant į bendrai naudojamos pamainos aplinką.
3.  Atsijunkite nuo EKA ir vėl prisijunkite.
4.  Pasirinkite **Kurti naują pamainą**.
5.  Pasirinkite **Deklaruoti pradinę sumą**.
6.  Įveskite visų parduotuvės kasos stalčių, įtrauktų į bendrai naudojamą pamainą, pradinę sumą, o tada spustelėkite **Įrašyti**.
    -   Norėdami pradinės sumos dalį įtraukti į kiekvieną paskesnį kasos stalčių, naudokite operaciją **Pasirinkti aparatūros stotį**, kad suaktyvintumėte aparatūros stotį.
    -   Norėdami į konkretų kasos stalčių įtraukti kasos stalčiaus skyrelį, naudokite operaciją **Atidaryti stalčių**.
    -   Tęskite, kol visose bendrai naudojamos pamainos kasos stalčiuose bus reikiama pradinės sumos dalis.

7.  Pasibaigus dienai atidarykite kiekvieną kasos stalčių ir išimkite grynuosius pinigus.
8.  Išėmę grynuosius pinigus iš paskutinio kasos stalčiaus, suskaičiuokite visų kasos stalčių grynuosius pinigus.
9.  Naudokite operaciją **Deklaruoti mokėjimo priemonę**, kad deklaruotumėte bendrą grynųjų pinigų sumą visuose bendrai naudojamos pamainos kasos stalčiuose.
10. Naudokite operaciją **Uždaryti pamainą**, kad uždarytumėte bendrai naudojamą pamainą.

## <a name="shift-operations"></a>Pamainos operacijos
Pamainos būsenai pakeisti arba pinigų sumai stalčiuje padidinti ar sumažinti galima imtis įvairių veiksmų. Toliau pateiktame skyriuje aprašomos pamainos operacijos, skirtos „Dynamics 365 for Retail“ moderniai EKA ir debesies EKA.

**Atidaryta pamaina**

EKA reikia, kad pas vartotoją būtų aktyvi atidaryta pamaina ir būtų galima atlikti operacijas, kurių galutinė išraiška virstų finansine operacija, pvz., pardavimu, grąžinimu arba kliento užsakymu.  

Jungiantis prie EKA sistema pirmiausia patikrina, ar pas vartotoją dabartiniame kasos aparate yra pasiekiama aktyvi pamaina. Jei pasiekiamos aktyvios paskyros nėra, tada, priklausomai nuo sistemos konfigūracijos ir teisių, vartotojas gali atidaryti naują pamainą, pratęsti esamą arba tęsti prisijungimą ne stalčiaus režimu.

**Deklaruoti pradinę sumą**

Ši operacija paprastai būna pirmas veiksmas, kurį reikia atlikti naujai atidarytoje pamainoje. Pradinę grynųjų pamainos pinigų sumą stalčiuje nurodo vartotojai. Tai svarbu, nes priklausomai nuo šios sumos uždarant pamainą skaičiavimas gali būtų per didelis arba per mažas.

**Srauto įrašas**

Nefiksuoti įrašai yra ne pardavimo operacijos, atliekamos aktyvioje pamainoje, dėl kurių stalčiuje padidėja grynųjų pinigų suma. Įprastas nefiksuoto įrašo pavyzdys – papildyti grąžos likutį stalčiuje, kai šis baiginėjasi.

**Mokėjimo priemonės šalinimas**

Mokėjimo priemonės šalinimai yra ne pardavimo operacijos, atliekamos aktyvioje pamainoje, siekiant sumažinti grynųjų pinigų sumą stalčiuje. Ši operacija dažniausiai atliekama kartu su nefiksuotu įrašu kitoje pamainoje. Pavyzdžiui, 1 kasos aparate mažėja grąžos likutis, todėl vartotojas 2 kasos aparate atlieka mokėjimo priemonės šalinimą, kad sumažintų sumą stalčiuje. Tada 1 kasos aparate vartotojas atlieka nefiksuotą įrašą, kad padidintų sumą.

**Sustabdyti pamainą**

Vartotojai gali sustabdyti aktyvią pamainą, kad atlaisvintų dabartinį kasos aparatą kitam vartotojui arba perkeltų jo pamainą į kitą kasos aparatą (šis veiksmas dar dažnai vadinamas nefiksuojama kasa). 

Sustabdydami pamainą neleidžiate atlikti jokių naujų operacijų arba pakeitimų, kol pamaina nebus pratęsta toliau.

**Pratęsti pamainą**

Ši operacija leidžia vartotojui pratęsti anksčiau kasos aparate sustabdytą pamainą, kurioje dar nėra aktyvios pamainos.

**Mokėjimo priemonių deklaravimas**

Mokėjimo priemonių deklaravimas – tai veiksmas, kurį vartotojas atlieka, norėdamas nurodyti bendrą tuo metu stalčiuje esančių pinigų sumą. Šis veiksmas dažniausiai atliekamas prieš uždarant pamainą. Tai vertė, lyginama su prognozuojama pamaina, norint apskaičiuoti perviršio / trūkumo sumą.

**Pinigų įnešimas į įmonės kasą**

Pinigų įnešimus į įmonės kasą galima atlikti bet kuriuo metu, aktyvioje pamainoje. Atlikus šią operaciją iš stalčiaus pašalinami pinigai, todėl juos galima perkelti į saugesnę vietą, pvz., į seifą galiniame kambaryje. Bendra į įmonės kasą įneštų pinigų suma vis tiek įtraukiama į bendrąsias pamainos sumas, bet gali būti neskaičiuojama mokėjimo priemonių deklaravimo dalis.

**Inkasavimas**

Pinigų įnešimai į kasą, panašiai, kaip ir inkasavimas, taip pat atliekami aktyviose pamainose. Atlikus šią operaciją pinigai pašalinami iš pamainos, kad būtų pasiruošta banko indėliui.

**Uždaryti pamainą anonimiškai**

Anonimiškai uždaryta pamaina – tai nebeaktyvi, bet dar visiškai neuždaryta pamaina. Anonimiškai uždarytų pamainų, kitaip nei sustabdytų, toliau pratęsti negalima, tačiau kai kurias procedūras, pvz., pradinių sumų ir mokėjimo priemonių deklaravimus, galima atlikti vėliau arba kitame kasos aparate.

Anonimiškai uždarytos pamainos dažnai naudojamos kasos aparatui atlaisvinti, kad įtraukiant naują vartotoją arba pamainą prieš tai nereikėtų visiškai perskaičiuoti, derinti ir uždaryti pamainos. 

**Uždaryti pamainą**

Atlikus šią operaciją apskaičiuojamos bendrosios pamainos sumos, perviršio / trūkumo sumos ir galutinai užbaigiama aktyvi arba anonimiškai uždaryta pamaina. Uždarytų pamainų, negalima pratęsti ar modifikuoti.  

**Valdyti pamainas**

Ši operacija leidžia vartotojams peržiūrėti parduotuvės aktyvias, sustabdytas ir anonimiškai uždarytas pamainas. Priklausomai nuo pamainų teisių, vartotojai gali atlikti galutines uždarymo procedūras, pvz., mokėjimo priemonių deklaravimą, ir galutinai uždaryti anonimiškai uždarytas pamainas. Atlikdami šią operaciją vartotojai taip pat galės peržiūrėti ir panaikinti netinkamas pamainas, kai, retais atvejais, perjungiant iš autonominio režimo į internetinį režimą ir atvirkščiai, jos paliekamos prastos būsenos. Netinkamose pamainose nėra pateikiama finansinės informacijos ar operacijų duomenų, reikalingų derinimui atlikti. 

