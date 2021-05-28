---
title: Integruoto kanalo išplėstinės automatinės išlaidos
description: Šioje temoje aprašomos papildomos „Commerce“ kito kanalo užsakymų mokesčių tvarkymo galimybės naudojant pažangias automatinio apmokestinimo funkcijas.
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
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
ms.dyn365.ops.version: 10
ms.openlocfilehash: 0eb1f112430005945b4f82b99ef9cc718c56de65
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022712"
---
# <a name="omni-channel-advanced-auto-charges"></a>Integruoto kanalo išplėstinės automatinės išlaidos

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama informacija apie išplėstinių automatinių išlaidų funkcijų, kurias galima rasti „Dynamics 365 for Retail“ 10.0 versijoje, konfigūracijas ir diegimą.

Įgalinus išplėstines automatinių išlaidų funkcijas, užsakymuose, sukurtuose bet kuriame palaikomame „Commerce“ kanale (elektroniniame kasos aparate (EKA), skambučių centre ir internete), galima naudotis [automatinių išlaidų](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfigūracijų privalumais, apibrėžtais ERP programoje, tiek antraščių, tiek eilutės lygio mokesčiams.

Ankstesniuose nei „Retail“ 10.0 versija leidimuose [automatinės išlaidos](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfigūracijos pasiekiamos tik jei užsakymai sukurti „e-Commerce“ ir skambučių centro kanaluose. 10.0 arba naujesnėse versijose EKA sukurti užsakymai gali naudoti automatinių išlaidų konfigūracijas. Tokiu būdu įvairios papildomos išlaidos gali būti sistematiškai įtraukiamos į pardavimo operacijas.

Naudojant ankstesnius nei 10.0 versija leidimus, EKA vartotojas paraginamas neautomatiškai įvesti siuntimo mokestį tipo „siųsti viską“ arba „siųsti pasirinktus“ POS operacijos metu. Nors įvairių išlaidų programos galimybės naudojamos atsižvelgiant į tai, kaip išlaidos rašomos užsakyme, sistematiškas skaičiavimas nevykdomas – skaičiuojama remiantis vartotojo įvestimi siekiant nustatyti išlaidų vertę. Išlaidas galima įtraukti tik kaip vieną „siuntimo“ susijusių išlaidų kodą ir jų negalima lengvai redaguoti arba keisti EKA jas sukūrus.

Neautomatinio įvedimo raginimai įtraukti siuntimo išlaidas vis dar teikiami 10.0 ir naujesnėse versijose. Jei organizacija neįjungia parametro **Išplėstinės automatinės išlaidos**, EKA raginimai neautomatiškai įvesti mokesčius nepasikeis.

Naudojant išplėstinių automatinių išlaidų funkciją EKA vartotojai gali sistematiškai apskaičiuoti bet kokias nurodytas įvairias išlaidas pagal automatinių išlaidų nustatymo lenteles. Taip pat, vartotojai galės įtraukti arba redaguoti neribotą skaičių papildomų išlaidų ir mokesčių į bet kurią EKA pardavimo operaciją antraštės arba eilutės lygiu (atsiskaitymo grynaisiais arba kliento užsakymams).

## <a name="enable-advanced-auto-charges"></a>Išplėstinių automatinių išlaidų įjungimas

Puslapyje **„Retail and Commerce“ \> Būstinės sąranka \> Parametrai \> „Commerce“ parametrai**, eikite į skirtuką **Kliento užsakymai**. „FastTab“ **Išlaidos** nustatykite **Naudoti išplėstines automatines išlaidas** į **Taip**.

![Išplėstinių automatinių išlaidų parametras](media/advancedchargesparameter.png)

Įjungus išplėstines automatines išlaidas, vartotojai neberaginami neautomatiškai įvesti siuntimo išlaidas EKA terminale kuriant tipo „siųsti viską“ arba „siųsti pasirinktus“ kliento užsakyme. EKA užsakymo išlaidos sistematiškai skaičiuojamos ir įtraukiamos į EKA operaciją (jei aptinkama atitinkama automatinių išlaidų lentelė, kuri atitinka kuriamos užsakymo kriterijus). Vartotojai taip pat gali įtraukti arba redaguoti antraštės arba eilutės lygio išlaidas neautomatiškai naudodami naujai sukurtas EKA operacijas, kurias galima įtraukti į EKA ekrano maketus.

Įgalinus išplėstines automatines išlaidas, esami **„Commerce“ parametrai**, skirti **Siuntimo išlaidų kodas** ir **Grąžinti siuntimo išlaidas**, nebenaudojami. Šie parametrai taikomi tik jei parametras **Naudoti išplėstines automatines išlaidas** nustatytas į parinktį **Ne**.

Prieš įjungdami šią funkciją įsitikinkite, kad patikrinote ir apmokėte savo darbuotojus, nes funkcijos įjungimas pakeis verslo procesų srautą – siuntimo ar kitų išlaidų skaičiavimą ir įtraukimą į EKA pardavimo užsakymus. Įsitikinkite, kad suprantate proceso srauto poveikį kuriant operacijas iš EKA. Kuriant skambučių centro ir „e-Commerce“ užsakymus, išplėstinių automatinių išlaidų įjungimo poveikis yra minimalus. Skambučių centro ir „e-Commerce“ programos ir toliau veiks kaip anksčiau – elgsena susijusi su automatinių išlaidų lentelėmis, skirtomis papildomiems užsakymo mokesčiams apskaičiuoti. Skambučių centro kanalo vartotojai ir toliau galės neautomatiškai redaguoti bet kurias sistemos apskaičiuotas automatines išlaidas antraštės ar eilutės lygiu arba neautomatiškai įtraukti įvairių išlaidų antraštės ar eilutės lygiu.

## <a name="add-pos-operations"></a>Įtraukite EKA operacijas

Tam, kad išplėstinės automatinės išlaidos tinkamai veiktų jūsų EKA programos aplinkoje, įtrauktos naujos EKA operacijos. Šios operacijos turi būti įtrauktos į jūsų [EKA ekrano maketus](/dynamics365/unified-operations/retail/pos-screen-layouts) ir įdiegtos į EKA įrenginius, kaip diegiate išplėstines automatines išlaidas. Jei šios operacijos neįtraukiamos, vartotojai negalės valdyti arba tvarkyti EKA operacijų įvairių išlaidų ir niekaip negalės koreguoti ar keisti išlaidų reikšmių, kurios sistematiškai apskaičiuojamos pagal automatinių išlaidų konfigūracijas. Rekomenduojame bent jau įdiegti operaciją **Valdyti išlaidas** į EKA maketą.

Toliau nurodytos naujos operacijos.

- **142 – valdyti išlaidas**. Naudokite šią operaciją, kad leistumėte EKA vartotojams peržiūrėti ir redaguoti įvairias EKA operacijos išlaidas, kurios bus įtrauktos neautomatiškai arba sistematiškai atliekant automatinių išlaidų skaičiavimus.
- **141 – įtraukti antraštės išlaidas**. Naudokite šią operaciją, kad suteiktumėte vartotojui galimybę neautomatiškai įtraukti įvairias išlaidas į bet kurią EKA pardavimo operaciją antraštės lygiu (ir pasirinkti naudotiną išlaidų kodą).
- **140 – įtraukti eilutės išlaidas**. Naudokite šią operaciją, kad suteiktumėte vartotojui galimybę neautomatiškai įtraukti įvairias išlaidas į bet kurią EKA pardavimo operacijos eilutę eilutės lygiu (ir pasirinkti naudotiną išlaidų kodą).
- **143 – perskaičiuoti išlaidas**. Naudokite šią operaciją, kad atliktumėte visą pardavimo operacijos išlaidų perskaičiavimą. Visos anksčiau vartotojo perrašytos automatinės išlaidos bus perskaičiuotos pagal dabartinę krepšelio konfigūraciją.

Kaip ir tvarkant visas POS operacijas, prieš vykdant operaciją galima reikalauti vadovo saugos konfigūracijas.

Svarbu atkreipti dėmesį, kad pirmiau išvardytas EKA operacijas taip pat galima įtraukti į EKA maketą, net jei parametras **Naudoti išplėstines automatines išlaidas** yra išjungtas. Tokiu atveju organizacijos vis tiek gaus papildomas galimybes peržiūrėti neautomatiškai įtrauktas išlaidas ir jas redaguoti naudojant operaciją **Valdyti išlaidas**. Vartotojai taip pat gali naudoti EKA operacijas **Įtraukti antraštės išlaidas** ir **Įtraukti eilutės išlaidas**, net kai parametras **Naudoti išplėstines automatines išlaidas** yra išjungtas. Operacija **Perskaičiuoti išlaidas** yra mažiau funkcionali, jei naudojama, kai parametras **Naudoti išplėstines automatines išlaidas** yra išjungtas. Tokiu atveju jokios sumos nebūtų perskaičiuojamos, o bet kokios išlaidos, neautomatiškai įtrauktos į operaciją, būtų tiesiog nustatytos į 0,00 USD.

## <a name="use-case-examples"></a>Naudojimo atvejų pavyzdžiai

Šiame skyriuje pateikiami pavyzdžių naudojimo atvejai, kurie padės suprasti automatinių išlaidų ir kitų išlaidų konfigūraciją bei naudojimą, vykdant kanalų užsakymus. Šie pavyzdžiai iliustruoja programos veikimą, kai parametras **Naudoti išplėstines automatines išlaidas** įjungtas.

### <a name="auto-charges-header-charges-example"></a>Automatinių išlaidų antraštės išlaidų pavyzdys

#### <a name="use-case-scenario"></a>Naudojimo atvejis

Mažmenininkas nori automatiškai pridėti išlaidas už krovinių gabenimą, kai bet kuriame „Commerce“ kanale sudaromos operacijos, kurių metu klientui reikia siųsti produktus. Mažmenininkas siūlo du pristatymo būdus: žeme ir oru. Jei klientas nusprendžia naudoti pristatymo žeme būdą ir užsakymo vertė yra mažesnė nei 100 USD, pardavėjas nori klientui priskirti 10,00 USD transportavimo išlaidas. Jei užsakymas yra daugiau nei 100 USD vertės ir klientas pasirenka siuntimą žeme, klientui nereikės mokėti jokių papildomų transportavimo išlaidų. Jei klientas pasirenka visų užsakymų pristatymą oru, nepriklausomai nuo jų bendros vertės, klientui bus priskirtos 20,00 USD transportavimo mokestis.

#### <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija

Šiam scenarijui būtina sukonfigūruoti dvi automatinių išlaidų lenteles.

Pasirinkite **Gautinos sumos \> Išlaidų sąranka \> Automatinės išlaidos**.

Sukonfigūruokite dvejas skirtingas antraštės lygio automatines išlaidas. Sukonfigūruokite vienerias išlaidas už pristatymo būdą „Žeme“, ir vienerias – už pristatymo būdą „Oru“. Šiuo atveju sukonfigūruokite jas naudoti „Visiems klientams“.

Pristatymo žeme išlaidų puslapio **Automatinės išlaidos** eilutės dalyje nurodykite išlaidas, kurios bus taikomos užsakymams, vertiems 0,01–100,00 USD, kaip 10,00 USD. Sukurkite kitą išlaidų eilutę, kad nurodytumėte, jog užsakymams, vertiems 100,01 USD ir daugiau, išlaidos nebus priskiriamos.

![Dviejų automatinių išlaidų lentelių pavyzdys](media/headerchargesexample.png)

Pristatymo oru išlaidų automatinių išlaidų formos eilutės dalyje nurodykite 20,00 USD išlaidas, kurios bus taikomos visiems užsakymams (vertiems 0,01–9 999 999,00 USD).

Nusiųskite pakeitimus į „Commerce Scale Unit“ / „Channel DB“, kad EKA galėtų juos naudoti, vykdydamas užduotį **1040 paskirstymo grafikas**.

#### <a name="sales-processing-for-this-scenario"></a>Šio scenarijaus pardavimo vykdymas

Įvykdžius pirmiau pateiktus konfigūravimo veiksmus ir pritaikius pakeitimus kanalo duomenų bazei, bet kuri kliento užsakymo arba pardavimo operacija, sukurta EKA, skambučių centre arba „e-Commerce“ kanaluose, kuriuose antraštės lygiu nustatyti pristatymo žeme arba oru būdai, naudos šias išlaidas ir jas automatiškai taikys pardavimui.

Šiuo metu išlaidos bus taikomos visoms pardavimo operacijoms, sukurtoms juridiniame subjekte, kuris naudoja šiuos pristatymo būdus, nes nėra galimybės nurodyti, kad automatinių išlaidų konfigūracija būtų taikoma tik konkrečiam pardavimo kanalui.

Kadangi tokiuose užsakymuose nėra aiškiai apibrėžtos „antraštės“, vykdant EKA ir „e-Commerce“ scenarijus antraštės lygio išlaidos bus taikomos tik jei visos operacijos pardavimo eilutės yra nustatytos siųsti tuo pačiu pristatymo būdu. Jei taikomi mišrus EKA ar „e-Commerce“ sukurtų operacijų vykdymo būdai, bus vertinamos ir taikomos tik eilutės lygio automatinės išlaidos.

Vykdant skambučių centro scenarijų, vartotojas gali kontroliuoti pristatymo būdo nustatymą užsakymo antraštėje, todėl antraštės lygio išlaidos bus taikomos šiems užsakymams net jei kai kurios pardavimo eilutės sukonfigūruotos naudoti kitą pristatymo būdą. Skambučių centro užsakymų antraštės lygio išlaidos visada bus pagrįstos pristatymo būdu, nustatytu pardavimo užsakymo antraštės lygiu.

### <a name="auto-charges-line-charges-example"></a>Automatinių išlaidų eilutės išlaidų pavyzdys

#### <a name="use-case-scenario"></a>Naudojimo atvejis 

Mažmenininkas nori priskirti papildomas išlaidas klientui už nustatymo mokesčius, kai klientas įsigija konkretaus modelio kompiuterį. Šiame kompiuteryje reikia atlikti papildomus privalomus nustatymo veiksmus, kuriuos mažmenininkas atliks kliento vardu. Mažmenininkas informavo klientus, kad už šį nustatymą bus taikomas papildomas mokestis. Mažmenininkas nori valdyti išlaidas, susijusias su šiuo mokesčiu, atskirai nuo produkto pardavimo kainos dėl finansinių ataskaitų tikslų. Įsigijus šį konkretų kompiuterį bet kuriame kanale, klientas turės sumokėti 19,99 USD nustatytą mokestį.

#### <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija

Šiuo atveju būtina sukonfigūruoti vieną eilutės lygio automatinių išlaidų lentelę.

Pasirinkite **Gautinos sumos \> Išlaidų sąranka \> Automatinės išlaidos**.

Nustatykite išplečiamojo meniu **Lygis** parinktį **Eilutė** ir sukurkite naują automatinių išlaidų įrašą, skirtą visiems klientams ir konkrečiam produktui arba produktų grupei, kurioje nustatymo mokesčiai bus taikomi.

![Vienos eilutės lygio automatinių išlaidų lentelės pavyzdys](media/linechargesexample.png)

Nusiųskite išlaidas į „Commerce Scale Unit“ / „Channel DB“, kad EKA galėtų juos naudoti, vykdydamas užduotį **1040 paskirstymo grafikas**.

#### <a name="sales-processing-for-this-scenario"></a>Šio scenarijaus pardavimo vykdymas

Įvykdžius pirmiau pateiktus konfigūravimo veiksmus ir pritaikius pakeitimus kanalo duomenų bazei, bet kuri kliento užsakymo arba pardavimo operacija, kuri sukurta EKA, skambučių centre arba „e-Commerce“ ir kurios užsakyme yra ši prekė, suaktyvins sistematišką eilutės lygio išlaidų įtraukimą į bendrą užsakymo sumą.

Šiuo metu išlaidos bus taikomos bet kuriai juridiniame subjekte sukurtai pardavimo eilutei, kuri atitinka eilutės lygio automatinių išlaidų konfigūraciją, nes nėra galimybės sukonfigūruoti, kad eilutės lygio automatinės išlaidos būtų taikomos tik konkrečiam pardavimo kanalui.

### <a name="manual-header-charges-example"></a>Neautomatinių antraštės išlaidų pavyzdys

#### <a name="use-case-scenario-description"></a>Naudojimo atvejo aprašymas

Mažmenininkas taiko išimtį įprastam procesui ir siūlo specialias produktų pristatymo į namus paslaugas klientams, kurie produktus užsisako parduotuvėje. Mažmenininkas ir klientas sutinka, kad klientas už šią paslaugą sumokės papildomą 25 USD tvarkymo mokestį. Užsakymo priėmėjas turi įtraukti šį papildomą mokestį į operaciją. Kadangi mokestis yra bendro tipo mokestis ir nėra susijęs su jokiu konkrečiu produktu užsakyme, bus naudojamos antraštės išlaidos.

#### <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija

Įsitikinkite, kad mokesčių kodas, kuris bus naudojamas šiame scenarijuje, yra tinkamai sukonfigūruotas: pasirinkite **Gautinos sumos \> Išlaidų sąranka \> Išlaidos** ir nurodykite atitinkamą scenarijaus išlaidų kodą.

![Išlaidų pavyzdys](media/chargesexample.png)

Jei mokestis turi būti laikomas su „siuntimu“ susijusiomis išlaidomis dėl su siuntimu susijusių nuolaidų ar akcijų, išlaidų kode nustatykite parinkties **Siuntimo mokestis** reikšmę **Taip**. Jei šis mokestis taip pat gali būti sistematiškai grąžinamas grąžinimo operacijos apdorojimo EKA programoje metu, nustatykite parinkties **Gražinamas** reikšmę **Taip**. Vėliavėlė **Grąžinamas** taikoma tik kai parametras **Naudoti išplėstines automatines išlaidas** nustatytas į parinktį **Taip**.

Nusiųskite išlaidas į „Commerce Scale Unit“ / „Channel DB“, kad EKA galėtų juos naudoti, vykdydamas užduotį **1040 paskirstymo grafikas**.

Operacija **Įtraukti antraštės išlaidas** turi būti sukonfigūruota jūsų [POS ekrano makete](/dynamics365/unified-operations/retail/pos-screen-layouts), kad mygtuku, kuris pasiekiamas vartotojui iš EKA, būtų galima iškviesti šią operaciją (141 operacija). Ekrano maketo pakeitimai taip pat turi būti paskirstyti kanale per paskirstymo grafiko funkciją.

#### <a name="sales-processing-of-manual-header-charges"></a>Neautomatinių antraštės išlaidų pardavimo apdorojimas

Norėdamas vykdyti šį scenarijų EKA programoje, EKA vartotojas įprastai sukurs pardavimo operaciją, įtraukdamas produktus ir bet kokias kitas konfigūracijas į pardavimą. Prieš surinkdamas mokėjimą vartotojas turi vykdyti operaciją **Įtraukti antraštės išlaidas**, kuri paragins vartotoją pasirinkti išlaidų kodą ir įvesti išlaidų vertę. Kai vartotojas baigia procesą, mokestis bus įtrauktas į pardavimo užsakymą kaip antraštės lygio išlaidos.

Šis procesas gali būti taikomas skambučių centrui naudojant esamą funkciją **Išlaidos**, kurią galima rasti įrankių juostos skirtuke **Pardavimas**. Puslapyje **Tvarkyti išlaidas** vartotojas gali įtraukti naują išlaidų eilutę į užsakymo antraštę.

### <a name="manual-line-charges-example"></a>Neautomatinių eilutės išlaidų pavyzdys

#### <a name="use-case-scenario"></a>Naudojimo atvejis

Klientas pageidauja, kad dvi iš penkių pardavimo užsakymo prekių būtų supakuotos kaip dovanos. Mažmenininkas siūlo pasirinktinę paslauga taikydamas 2,00 USD mokestį už vieną prekę. Užsakymo priėmėjas turi priskirti šiuos mokesčius konkrečioms prekėms, kurias reikia supakuoti kaip dovanas.

#### <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija

Įsitikinkite, kad mokesčių kodas, kuris bus naudojamas šiame scenarijuje, yra tinkamai sukonfigūruotas: pasirinkite **Gautinos sumos \> Išlaidų sąranka \> Išlaidos** ir nurodykite atitinkamą scenarijaus išlaidų kodą.

Jei mokestis turi būti laikomas su „siuntimu“ susijusiomis išlaidomis dėl su siuntimu susijusių nuolaidų ar akcijų, išlaidų kode nustatykite parinkties **Siuntimo mokestis** reikšmę **Taip**. Jei mokestis taip pat gali būti sistematiškai grąžinamas grąžinimo operacijos apdorojimo EKA programoje metu, nustatykite parinkties **Gražinamas** reikšmę **Taip**. Vėliavėlė **Grąžinamas** taikoma tik kai parametras **Naudoti išplėstines automatines išlaidas** nustatytas į parinktį **Taip**.

Nusiųskite išlaidas į „Commerce Scale Unit“ / „Channel DB“, kad EKA galėtų juos naudoti, vykdydamas užduotį **1040 paskirstymo grafikas**.

Operacija **Įtraukti eilutės išlaidas** turi būti sukonfigūruota jūsų [POS ekrano makete](/dynamics365/unified-operations/retail/pos-screen-layouts), kad mygtuku, kuris pasiekiamas vartotojui iš EKA, būtų galima iškviesti šią operaciją (140 operacija). Ekrano maketo pakeitimai taip pat turi būti paskirstyti kanale per paskirstymo grafiko funkciją.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Neautomatinių eilutės išlaidų pardavimo apdorojimas

Norėdamas vykdyti šį scenarijų EKA programoje, EKA vartotojas įprastai sukurs pardavimo operaciją, įtraukdamas produktus ir bet kokias kitas konfigūracijas į pardavimą. Prieš surinkdamas mokėjimą vartotojas turi pasirinkti konkrečią eilutę, kurioje bus taikomas mokestis, iš EKA prekių sąrašo ekrano ir vykdyti operaciją **Įtraukti eilutės išlaidas**. Vartotojas bus paragintas pasirinkti išlaidų kodą ir įvesti išlaidų vertę. Kai vartotojas baigia procesą, mokestis susiejamas su eilute ir įtraukiamas į bendras užsakymo išlaidas eilutės lygiu. Vartotojas gali kartoti papildomų eilutės išlaidų įtraukimo į kitas operacijos prekių eilutes procesą, jei reikia.

Tą patį procesą galima taikyti skambučių centre naudojant funkciją „tvarkyti išlaidas“, pateiktą puslapio **Pardavimo užsakymas** skilties **Pardavimo užsakymo eilutės** išplečiamajame meniu **Finansai**. Pasirinkus šią parinktį, atsidarys puslapis **Tvarkyti išlaidas**, kuriame vartotojas gali įtraukti naujas konkrečios eilutės išlaidas į operaciją.

## <a name="additional-features"></a>Papildomos funkcijos

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Išlaidų redagavimas EKA pardavimo operacijoje

Operacija **Valdyti išlaidas** (142) turėtų būti įtraukta į [POS ekrano maketą](/dynamics365/unified-operations/retail/pos-screen-layouts), kad vartotojas galėtų peržiūrėti ir redaguoti arba perrašyti bet kokias sistemos apskaičiuotas ar neautomatiniu būdu sukurtas antraštės arba eilutės lygio išlaidas. Jei operacija neįtraukta, vartotojai negalės koreguoti EKA operacijos išlaidų vertės, taip pat jie negalės peržiūrėti išlaidų informacijos, pvz., išlaidų kodo, susieto su išlaidų tipu.

EKA puslapyje **Valdyti išlaidas** vartotojas gali peržiūrėti tiek antraštės, tiek eilutės lygio išlaidų informaciją. Vartotojas gali naudoti šiame puslapyje teikiamą funkciją **Redaguoti** ir keisti mokėtiną sumą konkrečioje išlaidų eilutėje. Kai išlaidų eilutė perrašoma neautomatiškai, ji nebus sistematiškai perskaičiuojama, nebent vartotojas inicijuos operaciją **Perskaičiuoti išlaidas**.

Jei **Mokesčio perrašymo priežasties kodas** buvo sukonfigūruotas sąrankos puslapyje **„Commerce“ parametrai**, vartotojas bus raginamas pateikti priežasties kodą, kai EKA programoje bus pakeistos išlaidos.

Jei užfiksuotas perrašytų išlaidų priežasties kodas, taip pat pateikiama nauja ataskaita, kurioje galima peržiūrėti ir tikrinti šiuos perrašymus. Ataskaitą galima rasti **„Retail and Commerce“ \> Užklausos ir ataskaitos \> Mokesčių perrašymo retrospektyva**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>EKA grąžinimo operacijos išlaidų grąžinimas

Jei parametras **Naudoti išplėstines automatines išlaidas** nustatytas į **Taip**, esamas „Commerce“ parametras, skirtas **Grąžinti siuntimo išlaidas**, nebetaikomas. Norėdami nurodyti, kurios išlaidos klientui turėtų būti sistematiškai grąžinamos, kai naudojamos išplėstinės automatinės išlaidos, įsitikinkite, kad susijusių išlaidų kodas nustatymo puslapyje **Išlaidų kodas** yra sukonfigūruotas kaip **Gražinamas**. Apdorodami paskirstymo grafiką įsitikinkite, kad parametrai buvo susinchronizuoti su „Commerce“ kanalo duomenų bazėmis.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Grąžinimo užsakymo operacijos išlaidų grąžinimas

Išlaidos nėra sistemingai grąžinamos į **Grąžinimo užsakymai**, sukurtus „Commerce“. Vartotojai privalo pasirinkti parinktį **Kopijuoti išlaidas**, kai kuriamas **Grąžinimo užsakymas**. Jei parinktis **Kopijuoti išlaidas** nepasirenkama, pradinės pardavimo operacijos išlaidos nebus automatiškai grąžinamos. Jei parinktis **Kopijuoti išlaidas** pasirenkama, visos išlaidos bus nukopijuotos į grąžinimo užsakymą ir vartotojas galės neautomatiškai redaguoti ar pašalinti visas išlaidas, kurių jie nenori grąžinti. Šiuo metu vykstant skambučių centro grąžinimo užsakymo procesui neatsižvelgiama į vėliavėlę **Grąžinamas**, pateiktą sąrankoje **Išlaidų kodas**.

### <a name="configuring-pos-receipts-to-show-charges"></a>EKA kvitų konfigūravimas rodyti išlaidas

Toliau nurodyti kvito elementai įtraukti į kvito eilutę ir poraštę, kad veiktų išplėstinių automatinių išlaidų funkcija.

- **Eilutės siuntimo išlaidos** – šį eilutės lygio elementą galima naudoti norint prisiminti konkrečius išlaidų kodus, kurie pritaikyti pardavimo eilutei. Čia bus rodomi tik išlaidų kodai, kurie puslapyje **Išlaidų kodas** buvo pažymėti tipo **Siuntimas** išlaidos.
- **Eilutės kitos išlaidos** – šį eilutės lygio elementą galima naudoti norint prisiminti bet kokius konkrečius ne siuntimo išlaidų kodus, kurie pritaikyti pardavimo eilutei. **Sulyginkite kitus keitimus** yra mokesčių kodai, kai **Siuntimas** vėliava **Išlaidų kodų** puslapyje nebuvo įjungtas.
- **Užsakymo siuntimo mokesčių informacija** – šis poraštės lygio elementas rodo aprašymus, skirtus užsakymui taikomiems išlaidų kodams, kurie sąrankos puslapyje **Išlaidų kodas** pažymėti kaip tipo **Siuntimas** išlaidos.
- **Užsakymo siuntimo išlaidos** – šis poraštės lygio elementas rodo su siuntimu susijusių išlaidų vertę doleriais.
- **Užsakymo kitų išlaidų informacija** – šis poraštės lygio elementas rodo aprašymą, skirtą užsakymui taikomiems išlaidų kodams, kurie nepažymėti kaip su siuntimu susijusios išlaidos.
- **Užsakymo kitos išlaidos** – šis poraštės lygio elementas rodo su siuntimu nesusijusių kitų išlaidų vertę doleriais.

Organizacijoms rekomenduojama taip pat įtraukti laisvos formos teksto laukų į kvito poraštę, kad būtų apibrėžtos sritys, kuriose primenamos išlaidos.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Draudimas išlaidas skaičiuoti, kol EKA užsakymas nebaigtas

Kai kurios organizacijos norės palaukti, kol vartotojas baigs įtraukti visas pardavimo eilutes į EKA operaciją, prieš skaičiuodamos išlaidas. Norėdami drausti skaičiuoti išlaidas, kol prekės įtraukiamos į EKA operaciją, įjunkite parametrą **Neautomatinis išlaidų skaičiavimas**, pateiktą parduotuvės naudojamame **funkcijų šablone**. Įjungus šį parametrą EKA vartotojas privalės naudoti operaciją **Apskaičiuoti bendras sumas**, kai jis baigs įtraukti produktus į EKA operaciją. Tada operacija **Apskaičiuoti bendras sumas** suaktyvins užsakymo antraštės arba eilučių taikomų automatinių išlaidų skaičiavimą.

### <a name="charges-override-reports"></a>Išlaidų perrašymo ataskaitos

Jei vartotojai neautomatiškai perrašo apskaičiuotas išlaidas arba įtraukia neautomatines išlaidas į operaciją, šiuos duomenis bus galima patikrinti ataskaitoje **Išlaidų perrašymo retrospektyva**. Ataskaitą galima rasti **„Retail and Commerce“ \> Užklausos ir ataskaitos \> Mokesčių perrašymo retrospektyva**. Svarbu atkreipti dėmesį, kad šioje ataskaitoje reikalingi duomenys yra importuojami iš kanalo duomenų bazės HQ naudojant „P“ paskirstymo grafiko užduotis. Todėl informacija apie perrašymus, neseniai atliktus EKA, gali būti pateikiama šioje ataskaitoje ne iš karto, kol ši užduotis nenusiuntė parduotuvės operacijos duomenų į HQ.

## <a name="additional-resources"></a>Papildomi ištekliai

[Automatinių išlaidų įjungimas ir konfigūravimas pagal kanalą](auto-charges-by-channel.md)

[Proporcingas antraštės išlaidų paskirstymas atitinkančioms pardavimo eilutėms](pro-rate-charges-matching-lines.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
