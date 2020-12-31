---
title: Vartotojo patirties personalizavimas
description: Šiame straipsnyje paaiškinama, kaip galite personalizuoti programą.
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e46c392c43b63ef443f66d8ea8f9e91a9df3d126
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693237"
---
# <a name="personalize-the-user-experience"></a>Vartotojo patirties personalizavimas

[!include [banner](../includes/banner.md)]

Ši tema paaiškina, kaip galite personalizuoti programą ir apima tolesnius subjektus: 

- **Plačios sistemo parinktys** – Šios personalizavimo parinktys yra sukurtis nustatymų puslapyje ir prieinamos visiems vartotojams. Prie pavyzdžių priskiriama spalvų tema ir laiko juosta. 
- **Apribota personalizavimo prieiga** – Šiame prieigos lygmenyje, vartotojo veiksmai yra susisieti su tipiniu puslapio naudojimu ir yra automatiškai įrašomi programos ir atkuriame kitą kartą, kai apsilankote puslapyje. Pavyzdžiui, programos parduotuvės stulpelių tinklelio plotis, jei juos keičiate ir išplėstas ar sutrauktas „FastTabs“ statusas. 
- **Visa personalizuotas prieiga** – Šiame prieigos lygyje, vartotojai turi prieigą prie visų personalizuotų programos galimybių. Konkrečiau, jie turi prieigą prie **Personalizavimo** įrankių juostos. 
- **Personalizavimų bendrinimas** – Vartotojai turintys visą personalizavimo prieigą gali eksportuoti jų puslapio personalizavimus ir bendrinti juos su kitais vartotojais.
- **Personalizavimų valdymas** – Privilegijuoti vartotojai gali prieiti prie **Personalizavimo** administravimo puslapio tam, kad valdytų visus personalizavimus organizaciniu lygiu. 

## <a name="system-wide-options-for-the-current-user"></a>Dabartinio vartotojo visos sistemos parinktys

Puslapyje **Vartotojo parinktys** pateikiama keletas visos sistemos dabartinio vartotojo parametrų. Šios parinktys yra prieinamos visiems vartotojams, netgi vartotojams, kuriems nebuvo suteikta jokia prieiga prie personalizavimo. Tam, kad atvertumėte **Vartotojo parinkčių** puslapį, pasirinkite **Nustatymai** mygtuką naršymo juostoje ir tuomet pasirinkite **Vartotojo parinktys**. Puslapyje **Vartotojo parinktys** yra keturi skirtukai, kuriuose nurodomi įvairūs vartotojo parametrai.

- **Vaizdas**: pasirinkite puslapio elementų spalvų temą ir numatytąjį dydį.
- **Nuostatos**: pasirinkite numatytąsias vertes, kurios naudojamos kaskart atidarius sistemą. Šios vertės apima nustatytąją bendrovę, pradinį puslapį ir nustatąjį peržiūros ar redagavimo režimą. (Naudojantis rodymo / redagavimo režimu nustatoma, ar puslapis užrakintas peržiūrai, ar galima jį redaguoti kiekvieną kartą atidarius). Šiame skirtuke taip pat yra kalbos, laiko juostos, datos, laiko ir numerių formatų parinktys. Galiausiai šiame skirtuke yra keletas papildomų kiekviename leidime skirtingų nuostatų.
- **Paskyra** – Peržiūrėti ar redaguoti jūsų vartotojo vardą ir kitas su paskyra susijusias parinktis.
- **Darbo eiga**: pasirinkite su darbo eiga susijusias parinktis.

Kartu su jūsų vartotojo nustatymų keitimu, galite taip pat peržiūrėti ir panaikinti savo naudojimo duomenis ir personalizavimus **Naudotojo parinktys** puslapyje. Tam, kad nustatytumėte savo naudojimo duomenis, pasirinkite **Naudojimo duomenys** veiksmų juostoje. Skirtuke **Personalizavimas** galite peržiūrėti ir tvarkyti asmeninius sistemos puslapiams atliktus pakeitimus. Šiame skirtuke taip pat galite iš naujo nustatyti funkcijų paaiškinimus (t. y. iššokančiuosius langus, kuriuose esate supažindinami su naujomis sistemos funkcijomis). Būsite dar kartą įspėti apie anksčiau naudotas funkcijas.

> [!NOTE]
> Jei funkcija [Įrašyti rodiniai](saved-views.md) įjungta, galite peržiūrėti ir tvarkyti savo personalizavimo parametrus, pasirinkdami parinktį **Personalizavimas**, esančią veiksmų srities puslapyje **Vartotojo parinktys**.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Apribota personalizavimo prieiga (anksčiau besąlygiški personalizavimai)

**Apribota personalizavimo prieigos** lygmenyje, vartotojo veiksmai yra susisieti su tipiniu puslapio naudojimu ir yra automatiškai įrašomi programos ir atkuriame kitą kartą, kai apsilankote puslapyje. Nereikalingas joks atskiras įrašymo veiksmas. 

Toliau pateiktas veiksmų sąrašas, kuris patenka į tipinį puslapio naudojimą ir yra įtrauktas apribotoje personalizavimo prieigoje: 

- **Tinklelio stulpelio pločiai** – galite sureguliuoti stulpelio plotį tinklelyje, pasirinkdami dydžio juostą stulpelio antraštės kairėje arba dešinėje pusėje ir stumdami ją kairėn arba dešinėn, kol stulpelis yra norimo pločio. Programoje saugomas nustatytas stulpelio plotis. Tuomet, kitą kartą, kai atidarote puslapį, stulpelio dydis bus pakeistas į tą plotį.
- **Tinklelio poraštė ir bendri stulpeliai** – *(Prieinami tik, kai naujas tinklelio kontroliavimas yra įjungtas)* Galite nuspręsti, ar bendras kiekis turi būti rodomas skaitmeninio stulpelio apačioje tinklelyje ir ar tinklelio apačia turi būti matoma. Programa laiko šias ypatybes ir jas taiko kitą kartą, kai atidarote puslapį. Norėdami gauti daugiau informacijos, žr. [Tinklelio galimybės](grid-capabilities.md). 
- **„FastTabs“**: kai kuriuose puslapiuose yra išplečiamos dalys, vadinamos *„FastTabs“*. Programa talpina informaciją apie „FastTabs“, kuriuos jūs išpletėte ar sutraukėte. Kitą kartą, kai atidarote puslapį, tie patyes „FastTabes“ bus išplečiami arba sutraukiami priklausomai nuo paskutinės sąveikos puslapyje. Kai kuriais atvejais sutraukus „FastTab“ galima padidinti sistemos efektyvumą, nes programai nereikia nuskaityti „FastTabs“ informacijos, kol jie neišskleisti. Kaip paaiškinta vėliau šioje temoje, galite taip pat pakeisti „FastTabs“ užsakymus puslapyje.
- **„FactBoxes“** – Kai kurie puslapiai turi **Susijusios informacijos** juostą, kuri rodo tik skaitymui skirtą informaciją, susijusią su dabartiniu puslapio subjektu. Kiekvienas skyrius **Susijusios informacijos** juostoje yra žinomas kaip *„FactBox“*. Galite išplėsti ar sutraukti **Susijusios informacijos** juostą ir galite taip pat išplėsti ar sutraukti atskiras „FactBoxes“. Programa išsaugo šias nuostatas. Kitą kartą, kai atidarote puslapį **Susijusios informacijos** juosta ir atskiros „FactBoxes“ bus išplėstos arba sutrauktos priklausomai nuo paskutinės jūsų sąveikos puslapyje. Kai kuriais atvejais galite pagerinti sistemos veikimą sutraukdami **Susijusios informacijos** juostą arba „FactBox“, nes programa nebeturi gauti informacijos „FactBoxes“, kol jos yra išplėstos.
- **Veiksmų sritys**: šalia daugelio puslapių viršaus rodoma *Veiksmų sritis*. Veiksmų srityje yra daugeliui dabartiniame puslapyje galimų atlikti veiksmų skirtų mygtukų. Šie mygtukai skirtukuose dažnai sisteminami. Galite *smeigti* visą veiksmų juostą atidarytą arba galite ją sutraukti pagal nutylėjimą. Kitą kartą, kai atidarote puslapį, veiksmų juosta bus atidaryta arba sutraukta priklausomai nuo paskutinės jūsų sąveikos su puslapiu. Jei susmeigėte atvirą veiksmų juostą, bus rodomas paskutinis skirtukas, kurį naudojote.
- **„QuickFilters“**: virš daugelio tinklelių rodomas *„QuickFilter“*. „QuickFilter“ leidžia jums filtruoti tinklelį pagal vieną pasirinktą stulpelį. Programoje saugomas filtruojamas stulpelis. Tuomet, kitą kartą, kai atidarote puslapį, tinklelis naudos tą patį stulpelį filtravimui pagal nutylėjimą. Nepaisant to, galite vis dar pasirinkti skirtingus stulpelius filtravimui tinklelyje.
- **Stulpelio antraštės filtrai** – Kai filtruojate tinklelį naudodami *stulpelio antraštės filtrus*, galite keisti filtro operatorių, kaip norite tam, kad surastumėte norimus duomenis. Pavyzdžiui, galite pakeisti operatoriaus parinktį iš **prasideda** į **tiksliai atitinka**. Kiekvieną kartą naudojant stulpelio antraštės filtrą ir keičiant filtro operatorių, programoje išsaugomi pakeitimai. Tada, kitą kartą filtruojant tą stulpelį atkuriamas filtro operatorius.
- **Naršymo sritis**: *naršymo sritis* atveriama paspaudus bet kurio puslapio viršutiniame kairiajame kampe esantį mygtuką **Išplėsti naršymo sritį**. (Šis mygtukas kartais vadinamas _mygtuku **Meniu**_, *mėsainiu*, *mėsainio stiliaus meniu* arba *mėsainio stiliaus mygtuku*.) Galite prisegti atvertą naršymo sritį arba galite ją sutraukti. Prisegus atvertą naršymo sritį, programa laikys ją atvertą, kol jos nesutrauksite.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Viso personalizavimo prieiga (ankstesni atskiri personalizavimai)

**Visa personalizuotas prieiga** lygyje, vartotojai turi prieigą prie visų personalizuotų programos teikiamų galimybių. Kadangi įvairūs asmenys ir bendrovės turi skirtingus poreikius, jiems sąveikaujant su programa, ypač naudojamų laukelių sąlygomis, personalizavimas suteikia įrankius, leidžiančius vartotojams ir organizacijų kūrėjui turėti programoje sutvarkytą ir sąveikaujančią informaciją. Šios savybės yra pagrindinės pateikiant supaprastintas, optimizuotas patirtis programoje, kuriso yra išdirbtos jums ir jūsų organizacijai. 

Jei [Išsaugotos peržiūros](saved-views.md) funkija yra įjungta, atskiras įrašymas yra reikalaujamas tam, kad šie pakeitimai vartotojo patirtyje būtų konkrečiai peržiūrimi. Kai **Įrašytos peržiūros** funkcija yra išjungta, šie pakeitimai automatiškai įrašomi.

Toliau pateikti skyriai apima personalizavimo galimybių apimtį, kurios yra prieinamos vartotojams **Visa personalizuotas prieiga** lygyje. Štai keletas galimybių:

- Nuorodos meniu parinktys
- **Personalizavimo** įrankių juosta
- Plytų, sąrašų ir nuorodų į darbo sritis įtraukimas
- Suvestinės iš darbo srities įtraukimas į ataskaitų sritį
- Ataskaitų srities personalizavimas

### <a name="shortcut-menu-options"></a>Nuorodos meniu parinktys

Trumpųjų mygtukų meniu pateikia kelią keisti puslapio sąsają tam, kad ji geriau atitiktų jūsų reikalavimus ar jūsų organizacijos reikalavimus. (Trumpųjų mygtukų meniu taip pat žinomas kaip *dešiniojo paspaudimo meniu* arba *konteksto meniu*.)

Įprastus ir svarbiausius puslapio keitimus galima atlikti tiesiogiai naudojantis nuorodos meniu parinktimis. Pavyzdžiui, jei norite įtraukti ar paslėpti stulpelius tinklelyje, tik dešiniu mygtuku paspauskite stulpelio antraštę ir tuomet pasirinkite **Įterpti stulpelius** arba **Slėpti šį stulpelį**.

Taip pat, pagrindiniai personalizavimo tipai yra prieinami spaudžiant dešiniu mygtuku elementą ir tuomet pasirenktant **Personalizuoti**. (Atkreipkite dėmesį, kad ne visi elementai jūsų puslapyje gali būti personalizuoti.) Kai naudojate šį personalizavimo metodą, pasirodo elemento *ypatybių langas*.

![Elemento ypatybių personalizavimas](./media/cli-element-property-window.png)

Naudojantis ypatybių langu elementą galima personalizuoti toliau išvardytais būdais.

- Keisti elemento žymą.
- Slėpti elementą, kad jis nebūtų rodomas puslapyje. Lauko duomenys nepanaikinami ir nekeičiami. Tik informacija nebėra rodoma puslapyje.
- Įterpti informaciją į „FastTab“ suvestinės skyrių (jei elementas yra „FastTab“).
- Praleisti lauką, kad niekada nebūtų rodomas, kai puslapyje vykdote keitimus.
- Neleisti redaguoti lauke esančių (bet kurio įrašo) duomenų.
- Nurodykite lauką, kurio reikės duomenims įvesti. Jei šiame lauke neįvesta jokia reikšmė, jis bus pažymėtas raudonu rėmeliu ir žvaigždute, kad būtų nurodyta ši būsena. Ši parinktis yra prieinama tik pradedant nuo 10.0.11 versijos, kai [Įrašytos peržiūros](saved-views.md) ir **Paskirti laukeliai kaip reikalaujami naudojant personalizavimą** funkcijos yra įjungtos.

Priklausomai nuo elemento, ypatybių lange gali būti įterpta kitų personalizavimo galimybių. Pavyzdžiui, ypatybės langas plytoje gali leisti jums paskatinti, kad plyta ataskaitų srytyje ir ypatybių langas elementams nustatytoje ataskaitų srityje gali leisti jums sukurti naują tinkintą darbo sritį.

### <a name="the-personalization-toolbar"></a>Personalizavimo įrankių juosta

Jei norite sukurti keletą puslapio pakeitimų arba pakeitimus, kurie nėra prieinami per kitus mechanizmus (pavyzdžiui, jei norite iš naujo sutvarkyti elementus), galite naudoti **Personalizavimo** įrankių juostą. Norėdami atidaryti įrankių juostą **Personalizavimas**, atlikite vieną iš toliau pateiktų veiksmų.

- Pasirinkite **Ctrl+Shift+P** bet kuriame elemente puslapyje.
- Elemento ypatybių lange pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**.
- Bet kurio puslapio veiksmų srities skirtuke **Parinktys** esančioje grupėje **Personalizavimas**, pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**.
- Naršymo juostoje pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirinkite **Personalizavimas**.

[![Personalizavimo įrankių juosta](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Naršymas puslapyje

Kai atidaroma įrankių juosta **Personalizavimas**, esamas puslapis skirtas tik skaityti (kitaip tariant, negalite redaguoti duomenų), tačiau jis yra interaktyvus. Konkrečiau, galite išplėsti ar sutraukite **Susijusios informacijos** juostą, perjungti skirtukus ir išplėsti ar suskleisti skyrius, taip kaip įprastai naudotumėte šių veiksmų puslapyje atlikimui. Norėdami taikyti personalizavimą sutraukiamame skyriuje arba skirtuke (pvz., slėpti „FastTab“), pasirinkite šalia skyriaus arba skirtuko esantį mygtuką (kai bus rodoma įvesties klaviatūra arba užvedę virš jo pelės žymiklį).

#### <a name="personalization-tools"></a>Personalizavimo įrankiai

Įrankių juostoje **Personalizavimas** galima naudoti toliau išvardytus įrankius.

- Įrankį **Pasirinkti** naudokite norėdami pasirinkti ir pakeisti elemento ypatybes. Norėdami naudoti šį įrankį, įrankių juostoje pasirinkite mygtuką **Pasirinkti**, tada pasirinkite norimą elementą. Elemento ypatybių langas pasirodo ten, kur galite keisti bet kurias šio elemento ypatybes. Galite pakartoti procesą su kitais puslapio elementais, kuriuos galima personalizuoti. Atkreipkite dėmesį, kad kai kuriais atvejais gali nebūti kai kurių personalizavimo ypatybių. Pavyzdžiui, negalite užrakinti reikiamo lauko.
- Įrankį **Slėpti** naudokite norėdami paslėpti elementą puslapyje. Norėdami naudoti šį įrankį, įrankių juostoje pasirinkite mygtuką **Slėpti**, tada pasirinkite norimą paslėpti elementą. Jums naudojant **Slėpti** įrankį, visi elementai šiuo metu nepaslėpti yra rodomi, tačiau jie yra rodomi patamsėjusiame konteineryje. Tada galite padaryti elementą matomą jį pasirinkdami. Tam, kad pamatytumėte, kaip puslapis atrodys elementus paslėpus, perjunkite į kitą personalizavimo įrankį arba uždaryti personalizavimo įrankių juostą.
- Naudokite **Įtraukti laukelius** įrankį tam, kad įtrauktumėte laukelius į savo puslapį. Kai naudojate šį įrankį, galite pridėti tik tuos laukus, kurie yra puslapio apibrėžimo dalis. Norėdami gauti informacijos apie tai, kaip sukurti naujų laukų, kurie nėra dabartinio puslapio apibrėžimo dalis, žr. [Pasirinktinių laukų kūrimas ir darbas su jais](user-defined-fields.md). Kai pasirenkate **Įtraukti laukelius** mygtuką įrankių juostoje, pirmiausia turite pasirinkti tinkelelį arba skyrių, kuriame norite įtraukti laukelius. Teksto laukelis rodys laukelių sąrašą, kuris yra susijęs su pasirinktu tinkleliu ar skyriumi. Teksto laukelyje pasirinkite vieną ar keltis įtraukiamus laukelius ir tuomet pasirinkite **Atnaujinti**. Norėdami pašalinti pirmiau įtrauktą lauką, pakartokite šį procesą, bet panaikinkite lauko žymėjimą dialogo lange.
- Įrankį **Perkelti** naudokite norėdami perkelti elementą į kitą dabartinės elementų grupės vietą. Atkreipkite dėmesį, kad negalima perkelti elemento už jo pirminės grupės ribų. Norėdami naudoti šį įrankį, įrankių juostoje pasirinkite mygtuką **Perkelti**, tada pasirinkite norimą perkelti elementą. Pasirinkus elementą, programa nustato vietas, kur leidžiama perkelti elementą. Šios vietos vadinamos *nuvilkimo zonomis*. Velkant elementą dabartinėje grupėje kiekviena nuvilkimo zona rodoma kaip spalvota, paryškinta linija šalia srities, į kurią galima nuvilkti elementą.
- Įrankį **Praleisti** naudokite norėdami pašalinti elementą iš puslapio klaviatūros tabuliavimo sekos. Paspaudus įrankių juostoje esantį mygtuką **Praleisti** visi šiuo metu praleisti elementai yra rodomi užtamsintame fone. Galite interaktyviai pašalinti arba įtraukti laukus į skirtukų seką.
- Įrankį **Rodyti antraštėje** naudokite norėdami, kad laukas būtų rodomas „FastTab“ suvestinės skyriuje. Paspaudus įrankių juostoje esantį mygtuką **Rodyti antraštėje** visi pasirinkti suvestinės laukai rodomi užtamsintame fone. Galite interaktyviai įtraukti laukelius į „FastTab“ santrauką arba pašalinti laukelius iš santraukos pasirinkdami laukelius.
- Naudokite įrankį **Reikalauti**, kad nurodytumėte elementą, būtiną duomenims įvesti. Paspaudus įrankių juostoje esantį mygtuką **Reikalauti** visi personalizuoti elementai, kad jų būtų reikalaujama, yra rodomi užtamsintame fone. Tada vėl galite padaryti, kad jų nebūtų reikalaujama. Ši parinktis yra prieinama tik pradedant nuo 10.0.12 versijos ir vėlesnių, kai **Paskirti laukeliai turi būti naudojami personalizavimui** funkcija yra įjungta.
- Įrankį **Užrakinti** naudokite norėdami pažymėti elementą kaip redaguojamą arba neredaguojamą. Paspaudus įrankių juostoje esantį mygtuką **Užrakinti** visi šiuo metu neredaguojami elementai yra rodomi užtamsintame fone. Tada vėl galite padaryti, kad juos būtų galima redaguoti. Atminkite, kad kai kurie laukai būtini ir jų negalima padaryti neredaguojamais. Šalia tų laukų rodomas spynos simbolis.
- Naudokite **Įtraukti programą iš „Power Apps“** įrankį tam, kad įdėtumėte programą, kuri buvo sukurta naudojant „Microsoft Power Apps“ į puslapį. Norėdami gauti išsamesnės informacijos apie tai, kaip įdėti programą iš „Power Apps“ į puslapį, žr. [Įdėti programą iš „Power Apps“](embed-power-apps.md). Ši parinktis yra prieinama tik jei [Įrašytos peržiūros](saved-views.md) funkcija yra išjungta.
- Norėdami įdėti programą į puslapį, sukurtą naudojant „Microsoft Power Apps“ arba trečiosios šalies programą, spauskite mygtuką **Pridėti programą**. Ši parinktis yra prieinama tik jei [Įrašytos peržiūros](saved-views.md) funkcija yra įjungta. 
- Naudodami įrankį **Valyti** galite atkurti numatytąją įdiegus puslapį naudotą būseną. Visas dabartinio puslapio personalizavimas bus panaikintas. Šio veiksmo grąžinti negalima. Todėl naudokite šį įrankį tik tada, jei tikrai norite atkurti puslapį. Kai **Įrašytų peržiūrų** funkcija yra įjungta, šis įrankis pašalina personalizavimą esamai peržiūrai.
- Naudodami įrankį **Importuoti** galite įkelti personalizavimą iš jūsų ar ko nors kito sukurto failo. 

    - Kai **Įrašytų peržiūrų** funkcija yra išjungta, galite pasirinkti, ar įtraukti ar pakeisti jūsų esančius personalizavimus su personalizavimais, kurie yra importuojame puslapyje. Šio veiksmo grąžinti negalima. Todėl, kai importuojate personalizavimą, turite rankiniu būdu išvalyti arba anuliuoti keitimus, kurių nenorite.
    - Kai **Įrašytų peržiūrų** funkcija yra įjungta, importuoti personalizavimai puslapyje taps peržiūromis. Jei peržiūra jau egzistuoja, turėsite parinktį importavimą praleisti, pakeisti esamą peržiūrą su tuo pačiu vardu arba pervardyti importuojamą peržiūrą.

- Naudodami įrankį **Eksportuoti** galite įrašyti savo puslapio personalizavimus į failą. Tada galite pasidalinti savo personalizavimais su kitais vartotojais. Tiems vartotojams tiesiog reikia importuoti failą, kuriame yra jūsų puslapio personalizavimai. Kai **Įrašytų peržiūrų** funkcija yra įjungta, šis įrankis įrašo jūsų esamą peržiūrą į failą bendrinimui.
- Norėdami uždaryti įrankių juostą **Personalizavimas** ir vėl įjungti ankstesnę puslapio interaktyvią būseną, paspauskite mygtuką **Uždaryti**.

Paprastai, kai naudojama įrankių juosta **Personalizavimas**, jūsų personalizavimas įsigalioja iškart jį atlikus. Tačiau, jei funkcija [Įrašyti rodiniai](saved-views.md) yra įjungta, turite aiškiai įrašyti pasirinkto rodinio personalizavimą.

Kai kuriais atvejais paspaudus įrankį šalia elemento rodomas spynos simbolis. Šis simbolis reiškia, kad negalima keisti su pasirinktu įrankiu susijusių elemento ypatybių, nes pakeitus tokias ypatybes puslapis veiks netinkamai.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Plytų, sąrašų ir nuorodų į darbo sritį įtraukimas

Kai kuriuose puslapiuose, kuriuose yra sąrašų, galima veiksmų srities skirtuko **Parinktys** grupėje **Personalizavimas** esanti personalizavimo funkcija **Įtraukti į darbo sritį**. Ši funkcija suteikia galimybę perkelti susijusią informaciją iš dabartinio sąrašo į konkrečią darbo sritį. Darbo srityje rodoma informacija gali būti pagrįsta visu sąrašu arba filtruota ir surūšiuota sąrašo versija. Taip pat galite nurodyti, ar informacija darbo srityje rodoma kaip sąrašas, suvestinės išklotinė, kurioje gali būti rodomas sąrašo elementų skaičius, arba nuoroda.

> [!NOTE]
> Jei funkcija [Įrašyti rodiniai](saved-views.md) įjungta, į darbo sritį perkeliamas turinys yra tiesiogiai susietas su rodiniu. Peržiūros užklausa yra naudojama gauti duomenis į darbo sritį ir atitinkama plyta ar nuoroda darbo srityje atidaro puslapį į tą peržiūrą taip, kad peržiūros užklausa ir personalizavimas jai yra taikomas. Jei peržiūra yra atnaujinama, atitinkami darbo srities elementai bus keičiami į naują peržiūros sąvoką.

[![Įtraukti į darbo sritį](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Norėdami įtraukti sąrašą į darbo sritį, pirmiausia surūšiuokite arba filtruokite puslapio sąrašą, kad informacija būtų rodoma taip, kaip norite, kad ji būtų rodoma darbo srityje. (Jei **Įrašytos peržiūros** funkcija yra įjungta, nebegalite tęsti kol įrašysite peržiūrą, turinčią šias sąlygas.) Tuomet pasirinkite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Sąrašas**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite pasirinkti stulpelius, kurie turėtų būti rodomi darbo srities sąraše. Taip pat galite nurodyti darbo srities sąrašui naudojamą žymą.
- Tam, kad įtrauktumėte plytą į darbo sritį, pirmiausia filtruokite sąrašą puslapyje taip, kad jis rodytų duomenis, kurie turi būti apibendrinti ir prie kurių norite prieiti greitai. (Jei **Įrašytos peržiūros** funkcija yra įjungta, nebegalite tęsti kol įrašysite peržiūrą, turinčią šias sąlygas.) Tuomet pasirinkite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Išklotinės dalis**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite nurodyti darbo srities išklotinei naudojamą žymą. Taip pat galite nurodyti, ar išklotinėje turėtų būti rodomas skaičius. Po to, kai išklotinė įtraukiama į darbo sritį, galite pasirinkti ją, kad atidarytumėte dabartinį puslapį iš darbo srities. Tada galite peržiūrėti filtruotą sąrašą, susietą su išklotine.
- Norėdami į darbo sritį įtraukti nuorodą, pirmiausia filtruokite puslapio sąrašą, kad jame būtų rodomi jus dominantys duomenys. (Jei **Įrašytos peržiūros** funkcija yra įjungta, nebegalite tęsti kol įrašysite peržiūrą, turinčią šias sąlygas.) Tuomet pasirinkite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Nuoroda**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite nurodyti nuorodai naudojamą žymą. Arba galite nurodyti naujo skyriaus, kuriame yra ši nuoroda, žymą.

Į darbo sritį įtraukę savo sąrašą, išklotinę arba nuorodą galite atidaryti tą darbo sritį ir pakeisti jos elementų išdėstymo tvarką.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Suvestinės iš darbo srities įtraukimas į ataskaitų sritį

Kai kuriose darbo srityse pateikiamos skaičių išklotinės (t. y. išklotinės, kuriose nurodomi skaičiai) ir gali būti, kad norėsite, jog tos išklotinės būtų rodomos ir jūsų ataskaitų srityje. Darbo srityje dešiniuoju pelės mygtuku spustelėkite skaičiavimo plytelę, pasirinkite **Personalizavimas**, tada išklotinės ypatybių lange pasirinkite **Prisegti prie ataskaitų srities**. Kitą kartą, kai atidarote ir perkraunate tvarkaraštį, skaičiavimas pasirodys po naršymo plytomis toje darbo srityje. Galite pasirinkti, kad tas skaičius būtų tiesiogiai perkeliamas į duomenis, kuriuos jis atitinka.

### <a name="personalizing-your-dashboard"></a>Ataskaitų srities personalizavimas

Ataskaitų sritis dažnai yra pirmasis atidarius programą rodomas puslapis. Jis gali būti personalizuotas kaip bet kuris puslapis sistemoje naudojant tuos pačius mechanizmus aprašytus anksčiau šiame skyriuje. 

> [!WARNING]
> Šiuo metu, kai slepiate turinį ataskaitų srityje, svarbu, kad tiesiogiai nustatytumėte plytą, o ne sritį aplink ją. Jei slepiate grupę aplink plytą, gali būti netikėtų rezultatų, jei keletas plytų bus pirdėtos vėliau arba jei sistema perjungiama į kitą kalbą.

Viena unikali personalizavimo savybė ataskaitų srityje yra galimybė įtraukti plytas. 

- Jei **Viso puslapio programų** savybė yra išjungta, jūs pridedate naują plytą dešinio klavišo elemento paspaudimu ataskaitų srityje ir tuomet pasirenkate  **Įtraukti darbo sritį**. Nauja darbo srities išklotinė sukuriama ataskaitų srities apačioje. Galite pakeisti šios naujos darbo srities išklotinės pavadinimą. Galite taip pat įtraukti sąrašus, plytas ir nuorodas į darbo sritį, kaip aprašyta [Plytų, sąrašų ir nuorodų įtraukimas į darbo sritį](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace) skyrių šioje temoje.
- Jei **Viso puslapio programų** savybė yra įjungta, jūs pridedate naują plytą dešinio klavišo elemento paspaudimu ataskaitų srityje ir tuomet pasirenkate  **Įtraukti programą**. Teksto laukelyje, pasirinkite, ar norite įtraukti plytą į naują darbo sritį ar plyta turi turinį iš „Power Apps“ ar svetainės. Tuomet atlikite žingsnius, kad sukonfigūruotumėte savo pasirinktą parinktį. Nauja plyta sukuriama ataskaitų srities apačioje. 

## <a name="sharing-personalizations"></a>Personalizavimo bendrinimas

Personalizavę puslapį galite bendrinti personalizavimą su kitais vartotojais eksportuodami personalizuotą puslapį. Galite tuomet paprašyti kitų vartotojų importuoti personalizuojamą failą. Arba galite perduoti savo personalizavimą administratoriaus teises turinčiam vartotojui. Tokiu būdu tas vartotojas galės jūsų personalizavimo failą vienu metu taikyti keliems vartotojams, naudodamas administravimo puslapį **Personalizavimas**.

## <a name="administration-of-personalizations"></a>Personalizavimo parametrų administravimas

**Personalizavimo** puslapis yra personalizavimo valdymo organizacijos lygmeniu centras. Turinys ir galimybės šiame puslapyje priklauso nuo to, ar **Įrašytų peržiūrų** funkcija buvo įjungta.

Klientams, kurie įjungė **Išsaugotų peržiūrų** funkciją, žr. „Peržiūrų tvarkymas globaliai" skyrių esantį [Įrašytos peržiūros](saved-views.md) temoje.

Klientams, kurie dar neįjungė [Išsaugotų peržiūrų](saved-views.md) funkcijos, šis puslapis turi keturis skirtukus:

- **Taikyti**: galite importuoti arba pasirinkti personalizavimą vienam ar daugiau vartotojų. Norėdami personalizavimą taikyti vienam ar keliems vartotojams, pirmiausia pasirinkite vaidmenį ir vartotojus, kuriems tas vaidmuo suteiktas. Tada pasirinkite esamą personalizavimą, taikykite pasirinktiems vartotojams arba importuokite personalizavimo failą. Personalizavimas patikrinamas ir taikomas visiems pasirinktiems vartotojams, kai jie kitą kartą atidarys pasirinktą puslapį.
- **Išvalyti**: galite išvalyti visus vieno ar kelių vartotojų puslapio ar darbo srities personalizavimus. Pirmiausia pasirinkite puslapį arba darbo sritį, kad būtų rodomas tą puslapį ar darbo sritį personalizavusių vartotojų sąrašas. Tada pažymėkite vartotojus, kurių puslapio ar darbo srities personalizavimą norėtumėte išvalyti, ir paspauskite **Valyti**. Panaikinami visi personalizavimai, kuriuos pasirinkti vartotojai taikė pasirinktam puslapiui arba darbo sričiai. Šio veiksmo anuliuoti negalima. Tačiau jei buvo įrašytas puslapio ar darbo srities personalizavimas, tokį personalizavimą galima importuoti iš naujo.
- **Vartotojai**: pasirinkite vartotoją, kad būtų rodomas vartotojo personalizuotų puslapių sąrašas. Tada galite įjungti arba išjungti pasirinkto vartotojo galimybę jam naudotis konkrečių puslapių arba visos sistemos personalizavimais. Taip pat galite importuoti, eksportuoti arba išvalyti vartotojo personalizavimą. Be to, galite iš naujo nustatyti vartotojo funkcijų paaiškinimus. Tokiu atveju, jei vartotojas anksčiau atmetė visus iššokančiuosius langus, kurie supažindino su naujomis funkcijomis, jie bus rodomi dar kartą, kai vartotojas susidurs su šiomis funkcijomis.
- **Sistema**: galite laikinai išjungti visų vartotojų sistemos personalizavimus. Šiuo atveju visi personalizavimai panaikinami visiems vartotojams, o visi puslapiai iš naujo nustatomi pagal numatytąją būseną. Jeigu vėliau vėl įjungsite personalizavimą, visi personalizavimai bus pritaikyti iš naujo. Taip pat galite visam laikui išjungti visus visų vartotojų sistemos personalizavimus. Panaikintų personalizavimų atkurti neįmanoma. Todėl prieš atlikdami šią užduotį būtinai eksportuokite visus personalizavimus, kurių vėliau gali prireikti.

## <a name="personalizing-inventory-dimensions"></a>Atsargų dimensijų personalizavimas

Personalizuodami puslapyje atsargų dimensijų sąranką, atsižvelkite į parametrus, kurie buvo sukurti naudojant parinktį **Rodyti dimensiją**. Pavyzdžiui, naudojate personalizavimą, norėdami paslėpti paketo numerio atsargų dimensijos stulpelį, tačiau stulpelis rodomas kitą kartą atidarius puslapį. Taip atsitinka todėl, kad atsargų dimensijų stulpelių rodymas valdomas naudojant parametrus **Dimensijos rodinys**. Parametrai **Dimensijos rodinys** taikomi visuose puslapiuose ir naudojantis šiais parametrais panaikinamos visos personalizuotos atskirų puslapių atsargų dimensijų laukų sąrankos.

Todėl ankstesniame pavyzdyje, jei nenorite, kad puslapyje būtų rodomas paketo numerio atsargų dimensijos stulpelis, turite tame puslapyje panaikinti tos dimensijos parinkties **Rodyti dimensijas** žymėjimą.
