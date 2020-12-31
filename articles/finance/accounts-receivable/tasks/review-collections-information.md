---
title: Surinkimo informacijos peržiūra
description: Ši procedūra padės peržiūrėti mokėjimų priežiūros informaciją, taip pat įvairias sąrankos parinktis ir mokėjimų priežiūros operacijas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b5cc07c5dfb2444ff086c8b1f3bcc7634d8644d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446013"
---
# <a name="review-collections-information"></a>Surinkimo informacijos peržiūra

[!include [banner](../../includes/banner.md)]

Ši procedūra padės peržiūrėti mokėjimų priežiūros informaciją, taip pat įvairias sąrankos parinktis ir mokėjimų priežiūros operacijas. Šioje procedūroje naudojama demonstracinė įmonė USMF.

## <a name="create-customer-pools"></a>Kurti klientų telkinį
1. Pasirinkite **Moduliai > Kreditas ir mokėjimai > Sąranka > Klientų telkiniai**.
- Naudokite šį puslapį, norėdami nustatyti klientų telkinius, t. y. užklausas, nustatančias klientų sąskaitų, kurios gali būti rodomos ir valdomos mokėjimų priežiūros arba skirstymo pagal terminus procesuose, grupę. Naudokite klientų telkinius, norėdami filtruoti informaciją puslapyje **Mokėjimų priežiūra** priežiūros sąrašas ir susijusiuose sąrašo puslapiuose. Norėdami filtruoti klientų sąskaitas, kurios yra įtraukiamos, kai sukuriamos skirstymo pagal terminus momentinės kopijos, taip pat galite naudoti klientų telkinius.  
- Norėdami filtruoti klientų sąskaitas, kurios yra įtraukiamos, kai sukuriamos skirstymo pagal terminus momentinės kopijos, galite naudoti klientų telkinius.  
2. Pasirinkite **Naujas**.
3. Lauke **Telkinio ID** įveskite reikšmę.
4. Lauke **Telkinio aprašas** įveskite reikšmę.
5. Spustelėkite **Pasirinkti telkinio kriterijus**.
6. Lauke **Kriterijai** surinkite reikšmę.
7. Pasirinkite **Gerai**.
8. Pasirinkite **Peržiūrėti kliento telkinį**.

## <a name="create-collections-agents"></a>Kurti mokėjimų priežiūros agentus
1. Naršymo srityje eikite į **Moduliai > Kreditas ir mokėjimų priežiūra > Konfigūracija > Mokėjimų priežiūros agentai.**  
- Naudokite šį puslapį, norėdami darbuotojus nustatyti kaip mokėjimų priežiūros agentus ir pasirinktinai priskirti juos klientų telkiniams. *Collections agent* yra asmuo, kuris dirba su klientais siekdamas užtikrinti, kad mokėjimai yra surenkami laiku.  
- Šiame puslapyje nustatyti mokėjimų priežiūros agentai yra automatiškai įtraukiami į mokėjimų priežiūros komandą. Puslapio **Gautinų sumų parametrai** lauke **Komanda** pasirinkus komandą, į tą komandą įtraukiami mokėjimų priežiūros agentai. Jei komanda nepasirinkta, automatiškai sukuriama nauja komanda pavadinimu Mokėjimų priežiūra ir mokėjimų priežiūros agentai yra įtraukiami į šią komandą.  
2. Pasirinkite norimą agentą, tada puslapyje pasirinkite **Pridėti**.
3. Lauko **Telkinio ID** išplečiamajame meniu pasirinkite norimą įrašą.
4. Pažymėkite arba išvalykite žymės langelį **Numatytasis telkinys**.
- Pasirinkite šią parinktį, norėdami į pasirinkto mokėjimų priežiūros agento filtrų sąrašus įtraukti visus klientų telkinius. Jei nepasirinkta ši parinktis, filtrų saraše rodomi tik mokėjimų priežiūros agentui priskirti klientų telkiniai.  

## <a name="create-aging-period-definition"></a>Kurti skirstymo pagal terminus laikotarpių aprašą
1. Naršymo srityje eikite į **Moduliai > Kreditas ir mokėjimų priežiūra > Konfigūracija >Skirstymo pagal terminus laikotarpio apibrėžimai**.
- Skirstymo pagal terminus laikotarpio apibrėžimus galite naudoti norėdami analizuoti klientų arba tiekėjų sąskaitų mokėjimo terminus, remdamiesi savo įvesta data. Kiekvienas skirstymo pagal terminus laikotarpis, kurį nustatote skirstymo pagal terminus laikotarpio apibrėžimui, atitinka stulpelį sąrašo puslapyje arba formoje ar ataskaitoje, kai atliekama analizė.  
2. Pasirinkite **Naujas**.
3. Lauke **Skirstymo pagal terminus laikotarpio apibrėžimas** surinkite reikšmę.
4. Lauke **Aprašymas įveskite** surinkite reikšmę.
- Nurodykite kiekvieno skirstymo pagal terminus laikotarpio, kurį norite įtraukti į skirstymo pagal terminus laikotarpio aprašą, pavadinimą, vienetą ir intervalą. Eilutė, kurios lauke Vienetas yra 0 (nulis), rodo datą, kurią vykdoma analizė. Eilutės prieš nulį kaip numatytąjį įrašą lauke Vienetas turės –1, o eilutės po nulio turės 1, tačiau tai galima keisti. Norėdami pertvarkyti eilutes, pasirinkite **Aukštyn** ir **Žemyn**. 0 (nulis) eilutės negalima perkelti.  
- Nustatykite žymeklį toje vietoje, kur norite įterpti naują eilutę, ir tada spustelėkite **Pridėti**.  
- Pasirinkite indikatorių, kuris nurodys skirstymo pagal terminus laikotarpį formoje **Mokėjimų peržiūra** ir sąrašo puslapyje. Pavyzdžiui, galite pasirinkti žalią indikatorių (dabartinis laikotarpis), geltoną indikatorių (praėjęs 30 d. laikotarpis) ir raudoną indikatorių (praėjęs 90 d. laikotarpis).  
- Pasirinkite skirstymo pagal terminus laikotarpio aprašo spausdinimo kryptį. Šis pasirinkimas nurodo stulpelių rodymo Klientų skirstymo pagal terminus ataskaitoje arba Klientų skirstymo pagal terminus ataskaitoje tvarką.  
  - Pirmyn – spausdinkite stulpelius tokia tvarka, kokia antraštės rodomos lentelėje (pradedant viršutine eilute).  
  - Atgal – spausdinkite stulpelius atvirkštine tai tvarkai, kokia antraštės rodomos lentelėje (pradedant apatine eilute).    

## <a name="setup-collections-parameters"></a>Nustatyti mokėjimų priežiūros parametrus
1. Pasirinkite **Moduliai > Kreditas ir mokėjimai > Sąranka > Gautinų sumų parametrai**.
2. Pasirinkti **Mokėjimų peržiūra** skiltį.
3. Išplėskite arba sutraukite sekciją **Numatytosios rinkinių reikšmės**.
- Pasirinkite numatytosios skirstymo pagal terminus momentinės kopijos, kuri bus naudojama formoje **Mokėjimų priežiūra**, skirstymo pagal terminus laikotarpio aprašą.  
- Pasirinkite komandą, kuriai formoje **Mokėjimų priežiūros agentai** priskiriami mokėjimų priežiūros agentai. Sąraše rodomos tik tipo Mokėjimų priežiūra komandos.  
4. Išplėskite arba sutraukite dalį **Nurašyti**.
- Pasirinkite kasdienių DK žurnalų pavadinimą, kuris bus naudojamas, kai operacija nurašoma naudojant formą **Mokėjimų priežiūra** arba susijusius sąrašo puslapius.  
- Numatytąjį nurašymo operacijų kūrimo priežasties kodą pasirinkite formoje **Mokėjimų priežiūra** arba susijusiuose sąrašo puslapiuose.  
- Pasirinkite šią parinktį, jei puslapyje **Mokėjimų priežiūra** arba susijusiuose sąrašo puslapiuose kurdami nurašymo operacijas norite sukurti atskirą PVM sumų žurnalo eilutę. Jei pasirinksite šią parinktį, galėsite lengvai sekti su nurašymo operacijas susijusias PVM sumas. PVM sumas galite sekti atskirai – dėl šios priežasties galėsite lengviau koreguoti paveikto laikotarpio PVM įsipareigojimus.  
5. Išplėskite arba sutraukite sekciją **El. pašto šablonas**
- Pasirinkite siunčiamų el. laiškų šabloną, naudodami formos **Mokėjimų priežiūra** veiksmą **El. paštas > Operacijos**, kurias reikia perduoti kontaktui.  
- Pasirinkite el. laiško šabloną, kuris bus naudojamas, kai kliento išrašą siųsite kaip el. laiško priedą, naudodami formos **Mokėjimų priežiūra** veiksmą **El. paštas > Išrašas**, kurį reikia perduoti kontaktui.  
- Pasirinkite siunčiamų el. laiškų šabloną, naudodami formos **Mokėjimų priežiūra** veiksmą **El. paštas > Operacijos**.  

## <a name="age-customer-balance"></a>Pagal terminus suskirstyti kliento balansą
1. Naršymo srityje eikite į **Moduliai > Kreditas ir mokėjimų priežiūra > Konfigūracija >Terminuotas klientų balansas**.
- Pasirinkite skirstymo pagal terminus laikotarpio aprašą. Skirstymo pagal terminus momentinės kopijos proceso metu operacijos skirstomos pagal laikotarpius, nurodytus pasirinkto skirstymo pagal terminus laikotarpio apraše.  
- Pasirinkite klientų telkinį arba palikite šį lauką tuščią, jei norite sukurti skirstymo pagal terminus momentinę kopiją visiems klientams. Pasirinkus klientų telkinį, skirstymo pagal terminus momentinės kopijos procesas taikomas tik toms kliento sąskaitoms, kurios yra klientų telkinio dalis. Pasirinkto kliento telkinio tipas turi būti Skirstymo pagal terminus momentinė kopija.  
- Pasirinkite datos tipą, kuriuo remiantis bus kuriama skirstymo pagal terminus momentinė kopija.  
  - Operacijos data – skirstykite operacijas pagal jų datą.    
  - Terminas – skirstykite operacijas pagal jų terminą.    
  - Dokumento data – skirstykite operacijas jų dokumento datą.  
- Pasirinkite datą, kurią norite naudoti kaip dabartinę skirstymo pagal terminus momentinės kopijos datą. Pagal šią datą apskaičiuojami skirstymo pagal terminus laikotarpiai.    
  - Šios dienos data – naudokite sistemos datą. Naudokite šią parinktį, jei nustatyta, kad apdorojimas bus vykdomas atliekant pasikartojančią paketinę užduotį. Jei naudojate šią datą, pasikartojančią paketinė užduotį galima vykdyti reguliariai (tuo metu naudojama sistemos data).    
  - Pasirinkta data – naudokite nurodytą datą. Jei pasirinksite šią parinktį, įveskite skirstymo pagal terminus datą.  
2. Pasirinkite **Gerai**.

## <a name="view-aged-customer-balances"></a>Peržiūrėti pagal terminus suskirstytus klientų balansus
1. Naršymo srityje eikite į **Moduliai > Kreditas ir mokėjimų priežiūra > Mokėjimų priežiūra > Terminuotas balansas.**
- Naudokite šį sąrašo puslapį, norėdami klientų balansus ir pagal terminus suskirstytas sumas peržiūrėti pagal skirstymo pagal terminus laikotarpį. Ši informacija saugoma skirstymo pagal terminus momentinėje kopijoje. Skirstymo per terminus laikotarpiai nustatomi pagal naudojamą skirstymo pagal terminus laikotarpio apibrėžimą. Skirstymo pagal terminus laikotarpio apibrėžimas imamas iš klientų telkinio, jei jis buvo nurodytas telkinio užklausoje. Jei klientų telkinyje nėra skirstymo pagal terminus laikotarpio aprašo, naudojamas numatytasis skirstymo pagal terminus laikotarpio aprašas, nurodytas formoje Gautinų sumų parametrai.  
2. Išplėskite **Kontaktas** „FactBox“. Čia galite peržiūrėti kontaktinę informaciją:
- Kliento mokėjimų peržiūros kontaktas.  
- Numatytasis kliento pardavėjas.  
3. Išplėskite **Kredito limitas** „FactBox“.
- Naudokite **Kredito informacija** „FactBox“, norėdami peržiūrėti kliento kredito limitą ir dabartinio balanso informaciją.  

## <a name="view-customer-collections-details"></a>Peržiūrėti klientų mokėjimų priežiūros informaciją
1. Įsitikinkite, kad pasirinktas norimas įrašas.
2. Išplėskite „FactBox“ parinktis **Adresas**, **Kontaktas**, **Skirstymas pagal terminus** ir **Kredito limitas**, kad peržiūrėtumėte pateiktą informaciją.
3. Veiksmų srityje spustelėkite **Surinkimas**.
- Naujinkite kliento skirstymo pagal terminus momentinę kopiją, dabartinę datą naudodami kaip skirstymo pagal terminus datą, su kuria bus lyginamos operacijų datos. Jei skirstymo pagal terminus momentinėje kopijoje yra kelių juridinių subjektų informacija, atnaujintoje skirstymo pagal terminus momentinėje kopijoje bus tų pačių juridinių subjektų rinkinio informacija. Sumos yra išsaugomos juridinio subjekto, prie kurio esate prisiregistravę, kai naujinate skirstymo pagal terminus momentinę kopiją, apskaitos valiuta.  
- Pasirinkite skirstymo pagal terminus laikotarpio aprašą. Pagal numatytuosius nustatymus rodomas skirstymo pagal terminus laikotarpio aprašas, susietas su kliento skirstymo pagal terminus momentine kopija. Skirstymo pagal terminus laikotarpio aprašas valdo skirstymo pagal terminus laikotarpius ir sumas, rodomas „FactBox“ **Suskirstyti pagal terminus balansai** ir **Kredito informacija**.  
- Atidarykite meniu, kuriame yra šie elementai:    
  - Įmonė – rodo sumas „FactBoxes“ „Suskirstyti pagal terminus balansai“ ir „Kredito informacija“, esančias juridinio subjekto apskaitos valiutoje.  
  - Klientas – rodo sumas „FactBoxes“ „Suskirstyti pagal terminus balansai“ ir „Kredito informacija“, esančias kliento valiutoje.  
- Kliento skirstymo pagal terminus momentinėje kopijoje pasirinkite vieną ar daugiau juridinių subjektų, kurie gali peržiūrėti informaciją. Sąraše rodomi juridiniai subjektai buvo pasirinkti kuriant skirstymo pagal terminus momentinę kopiją.  
- Peržiūrėkite kliento patvirtinimą „Microsoft Excel“ formatu. Galite pasirinkti į išrašą įtrauktinų operacijų intervalo pradžios datą ir pasirinkti įtraukti tik atviras operacijas arba atviras ir sudengtas operacijas. Jei skirstymo pagal terminus momentinėje kopijoje pateikta kelių juridinių subjektų informacija, įtraukiamos visų juridinių subjektų operacijos.  
- Atidarykite formą **Dokumentai**, kurioje galite kurti ar redaguoti dokumentus arba pastabas.  
4. Veiksmų srityje spustelėkite **Susisiekti**.  
- Atidarykite „Outlook“, kurią naudodami galite siųsti el. laišką kontaktui, nurodytam lauke Kontaktas. Jei mokėjimų kontaktas nenurodytas, naudojamas pirminis kliento adresas. Jei nenurodytas pagrindinis kontaktas, el. laiškai bus siunčiami pirmu formoje **Kontaktai** nurodytu adresu. Pasirinktos operacijos įtraukiamos kaip priedas. Priedas pateikiamas „Excel“ formatu, jame yra trys darbalapiai. El. laiškų kliento kontaktams šablonus galima nurodyti formoje **Gautinų sumų parametrai**.  
- Šio mygtuko naudoti negalima, jei šioje formoje pasirinkto kontakto el. pašto adresas nenustatytas.  
- Paruoškite išrašą ir atidarykite „Outlook“, kurią naudodami galite siųsti el. laišką su išrašu kaip priedu lauke **Kontaktas** nurodytu adresu. Jei mokėjimų kontaktas nenurodytas, naudojamas pirminis kliento adresas. Jei nenurodytas pagrindinis kontaktas, el. laiškai bus siunčiami pirmu formoje **Kontaktai** nurodytu adresu.  
- Šio mygtuko naudoti negalima, jei šioje formoje pasirinkto kontakto el. pašto adresas nenustatytas.  
- Atidarykite „Outlook“, kurią naudodami galite siųsti el. laišką darbuotojui, nurodytam klientui priskirtos pardavimo grupės pardavimo atstovu. Jei pasirinktos operacijos, jos įtraukiamos kaip priedas. Priedas pateikiamas „Excel“ formatu, jame yra du darbalapiai. El. laiškų pardavėjams šablonus galima nurodyti formoje **Gautinų sumų parametrai**.  
- Šio mygtuko naudoti negalima, jei šioje formoje rodomo pardavėjo el. pašto adresas nenustatytas.  
- Peržiūrėkite kliento DK operacijas ir atlikite veiksmus. Jei naudojate centralizuotus mokėjimus, pridedama informacija apie visus juridinius subjektus, kurie yra įtraukti į kliento skirstymo pagal terminus momentinę kopiją. Juridinių subjektų informaciją galite apriboti, pasirinkdami **Įmonė** veiksmų srities grupėje **Žymėti**.  
- Keiskite pasirinktų operacijų mokėjimų priežiūros būseną.    
  - Ginčų nebuvo – operacijai nebuvo atlikta jokių mokėjimų priežiūros veiksmų.    
  - Užginčyta – klientas informavo, kad kilo problema dėl operacijos.    
  - Pažadėta sumokėti – klientas sutiko apmokėti operacijos sumą.    
  - Išspręsta – visos su operacija susijusios problemos buvo išspręstos, nereikia jokių papildomų mokėjimų priežiūros veiksmų.  
- Atidarykite meniu ir pasirinkite vieną iš toliau pateiktų elementų, norėdami nurodyti, kurias operacijas rodyti šioje formoje:    
  - Atviros – rodyti tik neužbaigtas operacijas.    
  - Atviros ir uždarytos – rodyti visas operacijas, sudengtas ir nesudengtas.  
- Apdoroti pasirinktą mokėjimą kaip lėšų trūkumo (NSF) mokėjimą.    
  - Šį mygtuką galima naudoti tik jei pasirinkta operacija yra į mokėjimo žurnalą įvestas mokėjimas (kredito balansas be SF), operacijai priskirta banko sąskaita, o mokėjimas anksčiau nebuvo atšauktas.  
- Nurašykite pasirinktas operacijas.  
- Pažymėkite operacijas, kurias norite sudengti tarpusavyje.  
- Atidarykite formą **Originalus dokumentas**, kurioje galite peržiūrėti ir spausdinti pasirinktos operacijos dokumentą.  
- Atidarykite **meniu**, kuriame yra šie elementai:    
  - Rinkiniai – rodyti tik veiklą, sukurtą mokėjimų priežiūros formoje.    
  - Visos – rodykite visas kliento veiklas, nepriklausomai nuo to, kur jos buvo sukurtos.  
- Atidarykite **meniu**, kuriame yra šie elementai:    
  - Atvira – rodyti tik neužbaigtą veiklą.    
  - Atviros ir uždarytos – rodykite visas veiklas, nepriklausomai nuo jų būsenos.  
- Pasirinkite klientui priskirtą mokėjimų priežiūros atvejį arba palikite šį lauką tuščią. Jei pasirinktas atvejis, šioje formoje rodomos tik su atveju susietos operacijos ir veiklos.  
5. Pasirinkite **Rodyti sąrašą**.
- Pasirinkite kliento sąskaitą arba priimkite numatytąjį įrašą. Pagal numatytuosius nustatymus tai yra sąrašo puslapyje arba formoje, iš kurios atidarėte šią formą, pasirinkta kliento sąskaita. Jei formą atidarėte iš sąrašo puslapio, sąraše rodomi klientai, įtraukti į mokėjimų priežiūros telkinį, kuris naudojamas sąrašo puslapyje.  

