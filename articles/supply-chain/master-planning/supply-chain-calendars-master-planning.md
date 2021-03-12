---
title: Kalendoriai ir bendrasis planavimas
description: Šioje temoje apžvelgiami tiekimo grandinės kalendoriai ir tai, kaip jie paveikia bendrąjį planavimą.
author: t-benebo
manager: tfehr
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: bbbd60ddfd46904374a2cf3ad4a09f96805bd2bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001804"
---
# <a name="calendars-and-master-planning"></a>Kalendoriai ir bendrasis planavimas

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiami tiekimo grandinės kalendoriai ir tai, kaip jie paveikia bendrąjį planavimą.  Paaiškinami skirtingi kalendoriai, naudojami bendrojo planavimo mechanizme, įskaitant tai, kaip jie paveikia siuntimo ir gavimo datas suplanuotuose užsakymuose. Galiausiai pateikiamos rekomendacijos dėl kalendorių priskyrimo, naudojimo ir atnaujinimo.

## <a name="definition-of-a-calendar"></a>Kalendoriaus aprašas

Kalendorių, kurį naudosite savo organizacijoje, galite nustatyti puslapyje **Organizacijos administravimas > Sąranka > Kalendoriai > Kalendoriai**. 

Kiekvienas datos įrašas kalendoriuje gali būti **atidarytas**, **uždarytas** arba **pagrindinis kalendorius**. Tai nurodyta puslapio **Darbo laikas** stulpelyje **Valdymas**. Kiekvienos datos informacija 
- **Atidarytas** – nurodo, kad darbas atliekamas pasirinktą dieną. Kalendorius bus atnaujinamas pagal darbo laiko šabloną.
- **Uždarytas** – nurodo darbą, kuris nėra atliekamas konkrečią dieną. 
- **Pagrindinis kalendorius** – nurodo, kad konkreti data paveldės darbo laikus ir atidarytą / uždarytą būseną iš pagrindinio kalendoriaus. Todėl atnaujinant pagrindinį kalendorių, pasirinktas kalendorius iš jo perima operacijų laiką. 

Uždarymo datų žymės langelis **Uždaryta paimti** priskiriamas automatiškai. Atidarytų datų parinktį **Uždaryta paimti** galite pasirinkti neautomatiškai. Tai nurodo, kad darbas atliekamas konkrečią dieną, bet siuntimas neatliekamas. 

## <a name="calendars-that-affect-master-planning"></a>Kalendoriai, kurie paveikia bendrąjį planavimą

### <a name="calendar-for-a-coverage-group"></a>Padengimo grupės kalendorius
Padengimo grupė nurodo bendrą rinkinį, sudarytą iš parametrų, naudojamų papildant prekes, priklausančias konkretaus padengimo grupei. 

Norėdami įtraukti padengimo grupės kalendoriu, pasirinkite **Bendrasis planavimas > Sąranka > Padengimas > Padengimo grupės**. Raskite padengimo grupę, kuriai norite priskirti kalendorių, tada pasirinkite jį lauke **Kalendorius**.

Padengimo grupę galima priskirti skirtinguose puslapiuose. 
    - Prekės puslapyje **Išleisto produkto informacija**. Norėdami pamatyti prekės padengimo grupę, pasirinkite **Produkto informacijos valdymas > Produktai > Išleisti produktai** ir pasirinkite prekę, kad atidarytumėte puslapį **Išleistų produktų informacija**. Prekės padengimo grupę galite peržiūrėti „FastTab“ **Planas**.
    - Puslapyje **Prekių padengimas**. Išleistų produktų informacijos puslapyje spustelėkite **Prekės padengimas**, kad atidarytumėte prekės padengimo puslapį. Apžvalgos skirtuke galite matyti skirtingus papildymo parametrus priklausomai nuo vietos, sandėlio ir produkto dimensijų. Kiekvienos prekės padengimo grupė bus nuskaityta iš padengimo grupės, nurodytos puslapyje **Išleisto produkto informacija**. Tai galima perrašyti skirtuke **Bendra** naudojant funkciją **Naudoti konkrečius parametrus** arba **Nepaisyti grupės parametrų**.
    - Puslapyje **Bendrojo planavimo parametrai**. Jei prekės padengimo grupė nenustatyta ankstesniuose puslapiuose, bendrasis planavimas naudos bendrą padengimo grupę, nustatytą bendrojo planavimo parametruose. Tai nustatoma lauke **Bendra padengimo grupė**, pasirinkus **Bendrasis planavimas > Sąranka > Bendrojo planavimo parametrai**. 

### <a name="calendar-for-a-vendor"></a>Tiekėjo kalendorius
Norėdami nurodyti tiekėjo darbo dienas, galite priskirti pirkimo kalendorių tiekėjui tiekėjo puslapyje **Pirkimo užsakymo numatytosios reikšmė**. 

Norėdami nustatyti tiekėjo kalendorių, turite sukurti kalendorių pasirinkdami **Organizacijos administravimas > Kalendoriai > Kalendoriai**. Sukūrus kalendorių, jis turi būti priskirtas tiekėjui. Pasirinkite **Mokėtinos sumos > Tiekėjai > Visi tiekėjai** ir pasirinkite tiekėją, kuram norite priskirti kalendorių. Tada tiekėjo puslapio „FastTab“ **Pirkimo užsakymo numatytosios reikšmė** priskirkite naują pirkimo kalendorių naudodami išplečiamajį meniu. 

Tiekėjo kalendorius nurodo dienas, kuriomis tiekėjas priima teikiamus pirkimo užsakymus, ir datas, kuriomis tiekėjas pristato užsakymus į jūsų įmonę. Taigi, tiekėjo, kuriam priskirtas pirkimo kalendorius, pirkimo užsakymo datos bus datos, kalendoriuje nurodytos kaip atidarytos. Tų užsakymų pristatymo datos taip pat bus atidarytos dienos ir tokiu būdu paveiks nupirktos prekės gamybos laiką. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Nupirktos prekės gamybos laiko nurodymas

Norėdami nurodyti prekės pirkimo gamybos laiką (ir jei reikia atsižvelgti tik į darbo dienas), turite atidaryti numatytųjų produkto užsakymo parametrų puslapį, pateiktą dalyje **Produkto informacijos valdymas > Produktai > Išleisti produktai**, ir pasirinkite **Numatytieji užsakymo parametrai**. 

> [!Note]
> **Darbo dienos**, pateiktos po pirkimo gamybos laiku, nurodo tiekėjo darbo dienas. Pvz., pristatymo tik antradieniais kalendorius, kai gamybos laikas yra 10 dienų ir darbo dienų žymės langelis yra pažymėtas, nurodo, kad prekė būtų pristatyta per 10 savaičių (10 antradienių).
Taigi, dažniausiai nerekomenduojama pasirinkti darbo dienas kaip pirkimo užsakymo gamybos laiką.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Gamybos laiko nustatymas prekybos sutarčių puslapyje

Bendrąjį planavimą galima nustatyti įtraukti visas tiekėjų prekybos sutartis. Prekybos sutartys yra fiksuotų kainų ar nuolaidų sutartys, nustatomos ir priskiriamos vienam ar daugiau klientų arba tiekėjų vykdant vieno produkto ar kelių produktų pardavimą arba pirkimą. Pasirinkite **Bendrasis planavimas > Sąranka > Bendrojo planavimo parametrai** ir skirtuke **Suplanuoti užsakymai** pasirinkite **Rasti prekybos sutartis**, kad planuojant būtų įtrauktos prekybos sutartys. Bendrasis planavimas gali pasirinkti tiekėją su **minimaliu gamybos laiku** arba su **žemiausia vieneto kaina**.

### <a name="calendar-for-a-warehouse"></a>Sandėlio kalendorius
Kalendorių galite priskirti sandėliui, norėdami nurodyti atidarytas gavimo ir siuntimo datas. Jei joks kalendorius nebuvo priskirtas sandėliui, laikoma, kad jis atidarytas visomis dienomis. 

> [!Note]
> Kalendoriaus priskyrimas tranzito sandėliui jokio poveikio neturės. Tranzito sandėliai naudojami perkėlimo užsakymams palaikyti. Taikomas užsakymų siuntimo ir gavimo datas apibrėžia atidarytos dienos siuntimo sandėlyje bei gavimo sandėlyje ir pristatymo būdo kalendorius.

#### <a name="closed-for-pickup-policy"></a>Strategija Uždaryta, negalima paimti
Norėdami nurodyti, kad sandėlis atidarytas prekėms gauti, bet paėmimas negalimas, sandėlio kalendoriuje galite naudoti strategiją **Uždaryta, negalima paimti**. Tai taikoma ir kliento paėmimams. 

### <a name="transport-calendar"></a>Transportavimo kalendorius 
Norėdami nurodyti datas, kurias galima naudoti siuntimo perkėlimo užsakymuose iš **siuntimo sandėlio**, galite priskirti **transportavimo kalendorių**. Transportavimo kalendorių galite nustatyti pagal pristatymo būdą arba pagal pristatymo būdą ir siuntimo sandėlį. Transportavimo kalendorius nustatomas pasirinkus **Pardavimas ir rinkodara > Sąranka > Paskirstymas > Pristatymo būdai**. Pasirinkite pristatymo būdą ir spustelėkite mygtuką **Transportavimo kalendorius**.

Galima kurti kiekvieno sandėlio ir pristatymo būdo eilutę, kai kalendorius įtraukiamas į stulpelį **Transportavimo kalendorius**. Ji nurodo transportavimo kalendorių, kuris bus taikomas, kai prekės siunčiamos iš sandėlio naudojant nurodytą pristatymo būdą. Norėdami taikyti transportavimo kalendorių visoms tam tikro pristatymo būdo siuntoms, eilutę galima sukurti nenurodžius sandėlio.  Tai turės įtakos visoms tam tikro pristatymo būdo siuntoms, nepriklausomai nuo sandėlio. 

Jei joks transportavimo kalendorius nepriskiriamas, laikoma, kad visos dienos yra atidarytos vykdyti transportavimą.

### <a name="calendar-for-a-customer"></a>Kliento kalendorius
Norėdami nurodyti datas, kuriomis klientas gali priimti pristatymus, galite klientui priskirti gavimo kalendorių. Jei klientui nepriskirtas joks kalendorius, laikoma, kad klientas gali gauti užsakymus visomis dienomis. Tai turės įtakos pardavimo užsakymo eilučių gavimo datai. Jei pardavimo užsakymo eilutėse pasirinksite datą, kuri kliento kalendoriuje nėra „atidaryta“, sistema nurodys, kad gavimo data yra netinkama. 

Atkreipkite dėmesį, kad galima įtraukti tik vieną kiekvieno kliento kalendorių. Jei norite įtraukti kiekvieno skirtingo kliento adreso kalendorių, galite kurti klientą, kuriam priskirtas vienas adresas, ir tada priskirti atitinkamą kalendorių. 

Pageidaujama pardavimo užsakymo eilučių gavimo data priklauso nuo kliento kalendoriaus ir pristatymo datos valdymo būdo. Daugiau informacijos apie tai, kaip apskaičiuojama anksčiausia pristatymo data, žr. [Užsakymų vykdymo perspektyva](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Juridinio subjekto siuntimo kalendorius
Norėdami nurodyti datas, kuriomis juridinis subjektas gali siųsti prekes, galite nustatyti siuntimo kalendorių pasirinkę **Organizacijos administravimas > Organizacijos > Juridiniai subjektai**. Pasirinkite juridinį subjektą ir įtraukite kalendorių skirtuko **Užsienio prekyba ir logistika** lauke **Siuntimo kalendorius**. Siuntimo kalendoriuje veiks kaip visų juridinio subjekto sandėlio kalendorių numatytųjų reikšmių šaltinis. 

## <a name="how-calendars-affect-dates-in-planning"></a>Kaip kalendoriai paveikia datas planavimo metu

### <a name="order-date-of-a-planned-purchase-order"></a>Suplanuoto pirkimo užsakymo data 
Suplanuoto pirkimo užsakymo data nurodo datą, kurią pateikiamas užsakymas. Tai bus atidaryta data tiekėjo kalendoriuje ir padengimo grupės kalendoriuje. Kartais tiekėjams reikalingas kelių dienų rezervas, nurodantis, kada jie gauna pirkimo užsakymą ir kada jie gali siųsti prekes. Šios datos nurodytos tiekėjo rezervo dienose. Tačiau jei nupirkta prekė priskiriama padengimo grupei rezervo dienomis, šios rezervo dienos perrašys tiekėjo rezervo dienas.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Suplanuoto pirkimo užsakymo pristatymo data
Pirkimo gavimo data nurodo datą, kurią gausite prekes. Tai bus atidaryta data kalendoriuje. Kalendorius, į kurį bus atsižvelgiama siekiant nurodyti, kokiomis dienomis galima gauti pirkimo užsakymus, nurodytas toliau (nuo aukščiausio iki žemiausio prioriteto). 
1. Tiekėjo kalendorius
1. Padengimo grupės kalendorius
1. Gavimo sandėlio kalendorius

Atminkite, kad padengimo grupės kalendorių galima nustatyti skirtinguose puslapiuose, prioritetas jam bus taikomas toliau nurodyta tvarka.
1. Prekės padengimo grupė puslapyje **Prekės padengimas**
1. Prekės padengimo grupė puslapyje **Išleistų produktų informacija**
1. Numatytoji prekės padengimo grupė puslapyje **Bendrojo planavimo parametrai**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Suplanuoto perkėlimo užsakymo pristatymo data
Kuriant perkėlimo tarp dviejų sandėlių užsakymą, siuntimo data ir gavimo data įtraukiamos į perkėlimo užsakymo antraštę kartu su siuntimo sandėliu ir gavimo sandėliu. Skirtumas tarp šių dviejų datų yra numatomas transportavimo tarp sandėlių laikas (dienomis).

Suplanuoto perkėlimo užsakymo siuntimo data nurodo datą, kurią prekės siunčiamos iš siuntimo sandėlio. Kalendoriai, naudojami nurodant galimą siuntimo datą, yra išvardyti toliau pagal prioritetą. 
1. Siuntimo sandėlio kalendorius
1. Padengimo grupės kalendorius (žr. pirmiau aprašytą šio kalendoriaus atsarginį užsakymą) Jei nustatytas sandėlio kalendorių rinkinys, siuntimo data bus atidaryta data kalendoriuje. Jei sandėlio kalendorių rinkinys nenustatytas, bus naudojamas padengimo grupės kalendorius. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Suplanuoto perkėlimo užsakymo gavimo data
Perkėlimo užsakymo gavimo data nurodoma, kai prekės gaunamos į gavimo sandėlį.

Kalendoriai, naudojami nurodant gavimo datą, yra išvardyti toliau pagal prioritetą. 
1. Padengimo grupės kalendorius 
1. Gavimo sandėlio kalendorius Jei nustatytas padengimo kalendorių rinkinys, gavimo data bus atidaryta data kalendoriuje. Jei padengimo grupės kalendorius nenustatytas, bus naudojamas sandėlio kalendorius. 

Ieškant suplanuoto perkėlimo siuntimo ir gavimo datų, taip pat atsižvelgiama į vartotojo nustatytą siuntimo ir gavimo rezervą. 

## <a name="using-calendars-in-master-planning"></a>Kalendorių naudojimas bendrajame planavime

### <a name="assignment-of-scm-calendars"></a>SCM kalendorių priskyrimas
Svarbu nustatyti kalendorius identifikuoti įmonės darbo dienas. Geriausia yra nustatyti kiekvieno elemento kalendorių nurodant skirtingas darbo dienas. Kitaip tariant, visi išoriniai kalendoriai (kliento, tiekėjo) ir visi vidiniai kalendoriai (sandėlio, padengimo grupės ir pristatymo būdo), susiję su įmone.

### <a name="recommendation-on-warehouse-calendars"></a>Sandėlio kalendorių rekomendacija
Rekomenduojama priskirti po vieną kalendorių sandėliui, kad būtų įtraukti tik konkretūs sandėlio pakeitimai. Pvz., dviejų ar daugiau sandėlių darbo dienos gali sutapti, bet paėmimo strategija – skirtis. Tokiu atveju geriausia kiekvienam sandėliui priskirti kalendorių ir atitinkamą paėmimo politiką, kad sistema įtrauktų geriausias suplanuotų pirkimo, perkėlimo ir gamybos užsakymų datas. Jei sandėlio kalendoriai nenustatyti, juridinio subjekto kalendorių galima naudoti kaip sandėlio kalendoriaus numatytųjų reikšmių šaltinį. 

### <a name="recommendation-of-coverage-group-calendars"></a>Padengimo grupės kalendorių rekomendacija
Naudojant padengimo grupės kalendorių svarbu atsižvelgti į perrašymo elgseną, susijusią su gavimo datomis bendrajame planavime. Taigi, rekomenduojama jį naudoti atsargiai. Tai ypač naudinga tuo atveju, kai papildymas turi būti vykdomas konkrečiomis savaitės dienomis. 

### <a name="updating-scm-related-calendars"></a>Su SCM susijusių kalendorių naujinimas
Nors svarbu visus atitinkamus kalendorius priskirti atitinkamai vietai (tiekėjui, klientui, sandėliui, pristatymo būdui arba padengimo grupei), taip pat svarbu juos atnaujinti, kad būtų matomi pakeitimai. Sistema nustatys gamybos, perkėlimo, pirkimo ir pardavimo užsakymų datas, priklausomai nuo priskirtų kalendorių derinio. Geriausia yra išsiaiškinti, kas yra atsakingas už kalendorių priskyrimą ir atnaujinimą atitinkamose srityse. Jei darbo dienomis įvyktų gedimas arba kitas neįprastas pakeitimas, būtina kalendorių atitinkamai atnaujinti. Visos užduotys, kurios priklauso nuo kalendorių, pvz., bendrasis planavimas ir gamybos planavimas, turi būti vykdomos iš naujo po kalendorių atnaujinimo. 
