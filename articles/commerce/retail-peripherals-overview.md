---
title: Išoriniai įrenginiai
description: Šioje temoje pateikiama informacija apie sąvokas, susijusias su išoriniais įrenginiais, esančiais „Commerce“.
author: rubencdelgado
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7ab4ab4d04433ca03ac90acc583afceea2014e8e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989534"
---
# <a name="peripherals"></a>Išorinis įrenginys

[!include[banner](includes/banner.md)]

Šioje temoje pateikiama informacija apie sąvokas, susijusias su išoriniais įrenginiais, esančiais parduotuvėje. Joje apibūdinti įvairūs būdai, kaip išorinius įrenginius galima prijungti prie elektroninio kasos aparato (EKA), ir komponentai, skirti valdyti ryšį su EKA.

## <a name="concepts"></a>Koncepcijos

### <a name="pos-registers"></a>EKA registrai

Naršymas: spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **Registrai**. EKA registras yra objektas, kuris naudojamas konkretaus EKA egzemplioriaus charakteristikoms nustatyti. Šios savybės apima aparatūros profilį arba periferinių įrenginių, kurie bus naudojami registre, sąranką, parduotuvę, kuriai priskiriamas registras, ir vartotojo, kuris prisijungia prie to registro, vaizdinį efektą.

### <a name="devices"></a>Įrenginiai

Naršymas: spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **Įrenginiai**. Įrenginys yra objektas, nurodantis su EKA registru susieto įrenginio fizinį egzempliorių. Kai sukuriamas įrenginys, jis priskiriamas EKA registrui. Įrenginio objektas seka informaciją apie POS registro suaktyvinimo laiką, naudojamo kliento tipą ir programų paketą, kuris buvo įdiegtas konkrečiame įrenginyje. 

Įrenginius galima susieti su šių tipų progrmomis: „Retail Modern POS“, „Retail Cloud POS“, „Retail Modern POS“ – „Windows Phone“, „Retail Modern POS“ – „Android“ ir „Retail Modern POS“ – „iOS“.

### <a name="modern-pos"></a>„Modern POS“

„Modern POS“ yra EKA programa, skirta „Microsoft Windows“. Ją galima įdiegti „Windows 10“ operacinėse sistemose (OS).

### <a name="cloud-pos"></a>„Cloud POS“

„Cloud POS“ yra naršyklėje veikianti „Modern POS“ programos versija, kurią galima pasiekti žiniatinklio naršyklėje.

### <a name="modern-pos-for-ios"></a>„Modern POS“, skirta „iOS“

„Modern POS“, skirta „iOS“, yra „iOS“ pagrįsta „Modern POS“ programos versija, kurią galima įdiegti „iOS“ įrenginiuose.

### <a name="modern-pos-for-android"></a>„Modern POS“, skirta „Android“

„Modern POS“, skirta „Android“, yra „Android“ pagrįsta „Modern POS“ programos versija, kurią galima įdiegti „Android“ įrenginiuose.

### <a name="pos-peripherals"></a>Išoriniai EKA įrenginiai

Išoriniai EKA įrenginiai yra tokie įrenginiai, kurie tiesiogiai palaiko EKA funkcijas. Šie išoriniai įrenginiai paprastai dalijami į tam tikras klases. Norėdami gauti daugiau informacijos apie šias klases, žr. šios temos skyrių „Įrenginių klasės“.

### <a name="hardware-station"></a>Hardware station

Naršymas: Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalai** &gt; **Parduotuvės** &gt; **Visos parduotuvės**. Pasirinkite parduotuvę, tada spustelėkite „FastTab“ **Aparatūros stotys**. Nustatymas **Aparatūros stotis** yra kanalo lygio nustatymas, naudojamas apibrėžti egzemplioriams, kuriuose bus įdiegta išorinių įrenginių logika. Šis nustatymas kanalo lygiu taikomas aparatūros stoties charakteristikoms nustatyti. Jis taip pat naudojamas norint pateikti aparatūros stočių, kurios galimos „Modern POS“ egzemplioriams pasirinktoje parduotuvėje, sąrašą. Aparatūros stotis yra įmontuota į „Windows“ ir „Android“ šiuolaikines „Modern POS“ programas. Be to, aparatūros stotį galima atskirai įdiegti kaip atskirą „Microsoft“ informacinių interneto paslaugų (IIS) programą. Tokiu atveju prieiga galima per tinklą.

### <a name="hardware-profile"></a>Aparatūros šablonas

Naršymas: spauskite **„Retail and Commerce“** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**. Aparatūros šablonas yra įrenginių, kurie sukonfigūruoti EKA registrui arba aparatūros stočiai, sąrašas. Aparatūros šabloną galima tiesiogiai priskirti EKA registrui arba aparatūros stočiai.

## <a name="devices-classes"></a>Įrenginių klasės
Išroriniai EKA įrenginiai paprastai skirstomi į klases. Šiame skyriuje aprašyti įrenginiai, kuriuos palaiko „Modern POS“, ir pateikiama jų apžvalga.

### <a name="printer"></a>Spausdintuvas

Spausdintuvai apima įprastus EKA kvitų spausdintuvus ir viso puslapio spausdintuvus. Spausdintuvai palaikomi naudojant EKA skirtą objektų susiejimą ir įdėjimą (OEKA) ir „Microsoft Windows“ tvarkyklių sąsajas. Tuo pačiu metu galima naudoti nedaugiau kaip du spausdintuvus. Ši galimybė palaiko scenarijus, kai grynaisiais pinigais atsiskaitančių klientų kvitai spausdinami kvitų spausdintuvais, o klientų užsakymai, kuriuose pateikiama daugiau informacijos, spausdinami viso puslapio spausdintuvu. Kvitų spausdintuvus prie kompiuterio galima tiesiogiai prijungti per USB, prie tinklo prijungti per eternetą arba naudojant „Bluetooth“.

### <a name="scanner"></a>Skaitytuvas

Tuo pačiu metu galima naudoti nedaugiau kaip du brūkšninių kodų skaitytuvus. Ši galimybė palaiko scenarijus, kai mobilesnis skaitytuvas reikalingas tam, kad nuskaitytų dideles ar sunkias prekes, o fiksuotas įdėtasis skaitytuvas naudojamas daugumai įprasto dydžio prekių nuskaityti, siekiant pagreitinti išregistravimo laiką. Skaitytuvus gali palaikyti OEKA, „Universal Windows Platform“ (UWP) arba klavišinių kredito kortelių skaitytuvų sąsajos. Skaitytuvui prijungti prie kompiuterio galima naudoti USB arba „Bluetooth“.

### <a name="msr"></a>MSR

Vieną USB magnetinės juostelės skaitytuvą (MSR) galima nustatyti naudojant OEKA tvarkykles. Jei norite naudoti atskirą MSR, skirtą elektroninio lėšų pervedimo (EFT) mokėjimo operacijoms, MSR turi būti valdomas per mokėjimo jungtį. Atskirus MSR galima naudoti klientų lojalumo įrašams, darbuotojams prisijungti ir dovanų koretelių įrašams, neatsižvelgiant į mokėjimo jungtį.

### <a name="cash-drawer"></a>Kasos stalčius

Vienas aparatūros šablonas palaiko du kasos stalčius. Ši galimybė leidžia tuo pačiu metu prie vieno kasos aparato veikti dviem aktyvioms pamainoms. Bendrinamos pamainos atveju arba, kai kasos stalčių vienu metu naudoja keli mobilieji EKA įrenginiai, vienam aparatūros šablonui galimas tik vienas kasos stalčius. Kasos stalčius prie kompiuterio galima tiesiogiai prijungti per USB, prijungti prie tinklo arba prijungti prie kvitų spausdintuvo naudojant RJ12 sąsają. Kai kuriais atvejais kasos stalčių galima prijungti naudojant „Bluetooth“.

### <a name="line-display"></a>Eilutės rodymas

Eilučių rodymas naudojamas norint operacijos metu klientui parodyti produktus, operacijų balansus ir kitą naudingą informaciją. Vieną eilutės rodymą galima prijungti prie kompiuterio per USB naudojant OEKA tvarkykles.

### <a name="signature-capture"></a>Parašo fiksavimas

Parašo fiksavimo įrenginius galima tiesiogiai prijungti prie kompiuterio per USB naudojant OEKA tvarkykles. Sukonfigūravus parašo fiksavimą, klientas paraginamas pasirašyti ant prietaiso. Pasirašius, parašas parodomas kasininkui, kad šis jį priimtų.

### <a name="scale"></a>Mastelis

Svarstykles galima prijungti prie kompiuterio per USB naudojant OEKA tvarkykles. Kai prie operacijos pridedamas produktas, pažymėtas kaip „pasvertas“ produktas, EKA nuskaito svorį iš skalės, prideda produktą prie operacijos ir naudoja kiekį, kurį nurodė skalė.

### <a name="pin-pad"></a>PIN rinkiklis

Asmeninio identifikavimo numerio (PIN) rinkikliai palaikomi per OEKA, bet jie turi būti valdomi per mokėjimo jungtį.

### <a name="secondary-display"></a>Antrinis rodymas

Sukonfigūravus antrinį rodymą, pagrindinei informacijai rodyti naudojamas 2 „Windows“ ekranas. Antrinio ekrano paskirtis – palaikyti nepriklausomo programinės įrangos tiekėjo (ISV) plėtinį, nes antrinis ekranas iš karto nėra sukonfigūruojamas ir rodo ribotą turinį.

### <a name="payment-device"></a>Mokėjimo įrenginys

Mokėjimo įrenginio palaikymas įdiegiamas per mokėjimo jungtį. Mokėjimo įrenginiai gali atlikti vieną ar kelias funkcijas, kurias pateikia kitos įrenginių klasės. Pvz., mokėjimo įrenginys gali veikti kaip MSR / kortelių skaitytuvas, eilučių rodymas, parašo fiksavimo įrenginys ar PIN rinkiklis. Mokėjimo įrenginių palaikymas įdiegiamas nepriklausomai nuo atskiro įrenginio palaikymo, kuris teikiamas kitiems į aparatūros šabloną įtrauktiems įrenginiams.

## <a name="supported-interfaces"></a>Palaikomos sąsajos
### <a name="opos"></a>OEKA

Norint užtikrinti, kad su „Commerce“ būtų naudojamas didžiausias prietaisų asortimentas, EKA skirtas OLE pramonės standartas yra pagrindinė palaikoma išorinių įrenginių platforma. EKA skirtą OLE standartą sukūrė Nacionalinė mažmeninės prekybos federacija (NRF, angl. „National Retail Federation“), nustatanti pramonės standartų ryšio protokolus, skirtus išoriniams įrenginiams. OEKA yra plačiai taikomas EKA standartui skirto OLE diegimas. Jis sukurtas XX a. dešimto dešimtmečio viduryje ir nuo tada buvo keletą kartų atnaujintas. OEKA pateikia įrenginių tvarkyklių architektūrą, kuri leidžia lengvai integruoti EKA aparatūrą į „Windows“ pagrįstas EKA sistemas. OEKA valdikliai tvarko ryšį tarp suderinamos aparatūros ir EKA programinės įrangos. OEKA valdiklį sudaro dvi dalys:

-   **Valdymo objektas** – įrenginio klasės (pvz., eilutės rodymas) valdymo objektas pateikia programinės įrangos programos sąsają. „Monroe Consulting Services“ ([www.monroecs.com](http://www.monroecs.com/)) pateikia standartizuotą OEKA valdymo objektų rinkinį, jie dar vadinami bendraisiais valdymo objektais (CCOs). CCO naudojami „Commerce“ EKA komponentui patikrinti. Todėl testavimas padeda užtikrinti, kad jei „Commerce“ palaiko įrenginių klasę per OPOS, galima palaikyti daugelį įrenginių tipų, su ta sąlyga, kad gamintojas pateikia paslaugų objektą, kuris yra sukurtas OPOS. Jūs neprivalote tiesiogiai patikrinti kiekvieno įrenginio tipo.
-   **Aptarnavimo objektas** – aptarnavimo objektas tiekia ryšį tarp valdymo objekto (CCO) ir įrenginio. Įrenginio aptarnavimo objektą paprastai teikia įrenginio gamintojas. Tačiau kai kuriais atvejais gali tekti atsisiųsti paslaugų objektą iš gamintojo svetainės. Pvz,, galbūt bus galimas naujesnis aptarnavimo objektas. Gamintojo žiniatinklio svetainės adreso žr. aparatūros dokumentaciją.

[![Valdymo objektas ir aptarnavimo objektas](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) OLE diegimo palaikymas, skirtas OPOS, EKA padeda užtikrinti, kad jei įrenginių gamintojai ir EKA leidėjai tinkamai įgyvendins standartą, EKA sistemos ir jos palaikomi įrenginiai gali veikti kartu, net jei jie anksčiau nebuvo kartu išbandyti. 

> [!NOTE]
> OEKA palaikymas neužtikrina visų įrenginių, turinčių OEKA tvarkykles, palaikymo. „Commerce“ pirmiausia turi palaikyti to įrenginio tipą ar klasę per OEKA. Be to, aptarnavimo objektai gali ne visada būti atnaujinti pagal naujausią CCO versiją. Dar turite žinoti, kad apskritai aptarnavimo objektų kokybė yra skirtinga.

### <a name="windows"></a>„Windows“

EKA kvitų spausdinimas optimizuotas OEKA. OEKA yra daug greitesnis nei spausdinimas per „Windows“. Todėl pravartu naudoti OEKA, ypač aplinkose, kur spausdinami 40 stulpelių kvitai ir operacijų tempas turi būti greitas. Su dauguma įrenginių naudosite OEKA valdiklius. Tačiau, kai kurie OEKA kvitų spausdintuvai palaiko ir „Windows“ tvarkykles. Naudodami „Windows“ tvarkyklę, galite pasiekti naujausius šriftus ir tinkle vieną spausdintuvą susieti su keliais kasos aparatais. Tačiau, yra ir „Windows“ tvarkyklių naudojimo trūkumų. Toliau pateikiami keletas trūkumų pavyzdžių:

-   Kai naudojamos „Windows“ tvarkyklės, vaizdai sugeneruojami prieš spausdinant. Todėl spausdinama lėčiau, nei su tais spausdintuvais, su kuriais naudojami OEKA valdikliai.
-   Įrenginiai, prijungti prie spausdintuvo (prijungti žiedine grandine), gali neveikti, kai naudojamos „Windows“ tvarkyklės. Pvz., gali neatsidaryti kasos stalčius arba kvitų spausdintuvas gali veikti ne taip, kaip tikimasi.
-   OEKA palaiko ir platesnį kvitų spausdintuvams būdingų kintamųjų rinkinį, pvz., popieriaus nuplėšimas arba kvito spausdinimas.
-   „IIS“ aparatūros stotis nepalaiko „Windows“ spausdintuvų. 

Jei naudojamame „Windows“ spausdintuve yra OPOS valdikliai, jis vis tiek turėtų tinkamai veikti „Commerce“.

### <a name="universal-windows-platform"></a>„Universal Windows Platform“

Išorinių įrenginių atveju UWP susieta su „Windows“ įrenginių „prijungti ir leisti“ palaikymu. Prijungus įrenginį „prijungti ir leisti“ prie „Windows“ OS, kuri palaiko to tipo įrenginį, jokios tvarkyklės nereikia norint naudoti įrenginį taip, kaip numatyta. Pvz., jei „Windows“ aptinka „Bluetooth“ garsiakalbio įrenginį, OS žino, kad šio įrenginio klasės tipas yra **Garsiakalbis**. Taigi, jį traktuoja kaip garsiakalbį. Jokių papildomų nustatymų nereikia. EKA įrenginių atveju, galima prijungti daug USB įrenginių ir „Windows“ juos atpažins kaip žmonių sąsajos įrenginius (HID). Tačiau gali būti neįmanoma nustatyti, kokias galimybes įrenginys pateikia, nes įrenginys nenurodo įrenginio klasės arba tipo. Į sistemą „Windows 10“ įtrauktos brūkšninių kodų skaitytuvų ir MSR įrenginių klasės. Taigi, jei įrenginys sistemai „Windows 10“ nurodo, kad yra kuriai nors iš šių klasių priklausantis įrenginys, „Windows“ tam tikrais laikotarpiais klausys įvykių iš šio įrenginio. „Modern POS“ palaiko UWP MSR ir skaitytuvus. Todėl, kai ji pasirengusi priimti kurio nors iš šių įrenginių įvestį, o kuriai nors iš šių klasių priklausantis įrenginys prijungiamas, šį įrenginį galima naudoti. Pvz., jei prie kompiuterio su „Windows 10“ prijungiamas UWP brūkšninio kodo skaitytuvas, o brūkšninio kodo prisijungimas „Modern POS“ sukonfigūruotas, brūkšninio kodo skaitytuvas taps aktyvus prisijungimo ekrane. Jokių papildomų nustatymų nereikia. Į sistemą „Windows“ nuolat įtraukiama papildomų elektroninio kasos aparato UWP įrenginių klasių. Šios klasės apima kasos stalčių ir kvitų spausdintuvų klases. Laukiama šių naujų įrenginių klasių palaikymo „Modern POS“.

### <a name="keyboard-wedge"></a>Klavišinis kredito kortelių skaitytuvas

Klavišinio kredito kortelių skaitytuvo įrenginiai siunčia duomenis į kompiuterį taip, tarsi šie duomenys būtų įvesti klaviatūra. Todėl, pagal numatytuosius parametrus, aktyvus EKA laukas priims nuskaitytus arba perbraukus gautus duomenis. Kai kuriais atvejais, toks būdas lemia tai, kad netinkamo tipo duomenys nuskaitomi į netinkamą lauką. Pvz., brūkšninis kodas gali būti nuskaitytas į tą lauką, kuris skirtas įvesti kredito kortelės duomenis. Daugeliu atveju EKA veikia logika, kuri nustato, ar nuskaityti arba perbraukus gauti duomenys yra brūkšninis kodas, ar perbraukimas kortele. Todėl duomenys tvarkomi tinkamai. Tačiau kai įrenginiai nustatomi kaip OPOS, o ne kaip klaviatūros kredito kortelių skaitytuvo įrenginiai, galima kontroliuoti tų įrenginių duomenis, nes turima daugiau informacijos apie įrenginį, iš kurio gaunami duomenys. Pvz., duomenys iš brūkšninio kodo skaitytuvo automatiškai atpažįstami kaip brūkšninis kodas, o susietas įrašas duomenų bazėje randamas lengviau ir greičiau, nei naudojant bendrąją eilutės iešką, kaip tai daroma naudojant klavišinius kredito kortelių skaitytuvų įrenginius.

### <a name="native-printer"></a>Vietinis spausdintuvas

Vietinius (arba „Įrenginius“, nes tipas įvardintas aparatūros šablone) spausdintuvus galima sukonfigūruoti taip, kad paragintų vartotoją pasirinkti tą spausdintuvą, kuris sukonfigūruotas tam kompiuteriui. Jei sukonfigūruotas spausdintuvas, kurios tipas **Įrenginys** , kai „Modern POS“ aptinka spausdinimo komandą, vartotojas paraginamas iš sąrašo pasirinkti spausdintuvą. Šis veikimo būdas skiriasi nuo „Windows“ tvarkyklių veikimo būdo, nes **„Windows“** spausdintuvo tipas aparatūros šablone neparodo spausdintuvų sąrašo. Šiuo būdu reikalaujama, kad lauke **Įrenginio pavadinimas** būtų nurodytas įvardytas spausdintuvas.

### <a name="network"></a>Tinklas

Į tinklą adresuojamus kasos stalčius, kvitų spausdintuvus ir mokėjimo terminalus galima naudoti tinkle, arba tiesiogiai per tarpprocesinio ryšio (IPC) aparatūros stotį, kuri yra įtaisyta „Windows“ skirtoje „Modern POS“ programoje, arba per IIS aparatūros stotį, skirtą kitiems „Modern POS“ klientams.

## <a name="hardware-station-deployment-options"></a>Aparatūros stoties diegimo parinktys

### <a name="dedicated"></a>Paskirta

„Modern POS“ klientuose, skirtuose „Windows“ ir „Android“ yra **„Paskirtos“** arba įmontuotos aparatūros stotys. Šie klientai gali tiesiogiai susisiekti su periferiniais įrenginiais, naudodamiesi verslo logika, integruota programose. „Android“ programa palaiko tik tinklo įrenginius. Norėdami gauti daugiau informacijos apie „Android” periferinį palaikymą, apsilankykite straipsnio [Programos „POS Hybrid“ nustatymas, skirtas „Android” ir „iOS”](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp) puslapyje.

Norėdami naudoti paskirtą aparatūros įrangos stotį, priskirkite aparatūros profilį registrui, kuris naudos „Modern POS“, skirtą „Windows“ ar „Android“ programoms. Tada parduotuvei, kurioje registras bus naudojamas, sukurkite aparatūros stotį, kurios tipas **Paskirta**. Norėdami įjungti aparatūros stoties galimybes, paleiskite „Modern POS“ ne stalčiaus režime ir naudokite operaciją **Tvarkyti aparatūros stotis**, o paskirta aparatūros stotis bus aktyvi pagal numatytuosius nustatymus. Atsijunkite nuo „Modern POS“, tada vėl prisijunkite, atidarykite pamainą ir aparatūros profilyje sukonfigūruoti periferiniai įrenginiai bus tinkami naudoti. 

### <a name="shared"></a>Bendrinama 

Taip pat kartais vadinama „IIS“ aparatūros stotimi, „IIS“ reiškia, kad EKA programa jungiasi prie aparatūros stoties per „Microsoft Internet Information Services“. EKA programa prisijungia prie IIS aparatūros stoties per žiniatinklio tarnybas, vykdomas kompiuteryje, prie kurio prijungti įrenginiai. Kai naudojama bendro naudojimo aparatūros stotis, periferinius įrenginius, sujungtus su aparatūros stotimi, gali naudoti bet kuris EKA registras, esantis tame pačiame tinkle kaip ir IIS aparatūros stotis. Kadangi tik „Windows“ ir „Android“ skirtoje „Modern POS“ yra įmontuotas periferinių įrenginių palaikymas, visos kitos „Modern POS“ programos turi naudoti IIS aparatūros stotį, kad susisiektų su aparatūros profilyje sukonfigūruotais EKA periferiniais įrenginiais. Todėl kiekvienu atveju, kai naudojama IIS aparatūros stotis, reikalingas kompiuteris, kuriame paleista žiniatinklio tarnyba ir programa, palaikančios ryšį su įrenginiais. 

Bendra aparatūros stotis gali būti naudojama norint leisti keliems elektroninio kasos aparato klientams dalytis periferiniais prietaisais arba gali būti naudojama valdyti įsipareigotą rinkinį ar periferinius įrenginius vienam elektroniniam kasos aparatui. 

Kai aparatūros stotis naudojama palaikyti periferinių įrenginių pasidalijimą tarp kelių EKA klientų, turėtų būti naudojami tik grynųjų pinigų stalčiai, kvitų spausdintuvai ir mokėjimo terminalai. Negalima tiesiogiai prijungti atskirų brūkšninio kodo skaitytuvų, MSR, eilutės rodymų arba kitų įrenginių. Kitu atveju, kai keli EKA įrenginiai tuo pačiu metu bandys reikalauti patvirtinti tuos išorinius įrenginius, kils nesuderinamumų. Štai kaip tvarkomi palaikomų įrenginių nesuderinamumai:

-   **Kasos stalčius** – kasos stalčius atidarytas per įvykį, kuris išsiųstas į įrenginį. Vienintelis nesuderinamumas, kuris gali įvykti iškvietus kasos stalčių, gali įvykti tada, jei kasos stalčius jau yra atidarytas. Bendrai naudojamų aparatūros stočių atveju, aparatūros šablone kasos stalčius turi būti nustatytas į **Bendrai naudojama**. Šis nustatymas neleidžia EKA tikrinti, ar kasos stalčius jau yra atidarytas, kai išsiunčia atvirą komandą.
-   **Kvitų spausdintuvas** – jei dvi kvitų spausdinimo komandos tuo pačiu metu išsiunčiamos į aparatūros stotį, atsižvelgiant į įrenginį, viena iš komandų gali būti prarasta. Kai kuriuose prietaisuose yra vidinė atmintis arba telkinys, galintis padėti išvengti šios problemos. Jei spausdinimo komanda nėra sėkminga, kasininkas gauna klaidos pranešimą ir gali iš naujo bandyti atlikti komandą iš EKA.
-   **Mokėjimo terminalas** – jei kasininkas bando užregistruoti operaciją mokėjimo terminale, kuris jau naudojamas, pranešimas informuoja kasininką, kad tuo metu terminalas naudojamas ir paprašo kasininko dar kartą bandyti vėliau. Paprastai kasininkai gali matyti, kad terminalas tuo metu jau naudojamas, ir prieš vėl bandydami užregistruoti, palaukia, kol ta operacija bus baigta.

Būsimoje laidoje planuojamas patikrinimas, siekiant nustatyti, ar nepalaikomi įrenginiai yra nustatyti aparatūros šablone, kuris susietas su bendrai naudojama aparatūros stotimi. Jei bus aptikta nepalaikomų įrenginių, vartotojas gaus pranešimą apie tai, kad tie įrenginiai nėra palaikomi bendrai naudojamose aparatūros stotyse. Bendrai naudojamų aparatūros stočių atveju, parinktis **Pasirinkti mokant** registro lygiu yra nustatyta į **Taip**. Kai operacijos mokėjimo priemonė EKA pasirinkta, EKA vartotojas paraginamas pasirinkti aparatūros stotį. Kai aparatūros stotis pasirenkama tik mokėjimo metu, aparatūros stoties pasirinkimas įtraukiamas tiesiogiai į EKA mobilių scenarijų darbo eigą. Be to, bendrai naudojamuose scenarijuose eilutės rodymas nenaudojamas mokėjimo terminale. Jei mokėjimo terminalas naudojamas kaip eilutės rodymas, kitiems vartotojams šio terminalo naudojimas gali būti užblokuotas, kol operacija bus baigta. Mobiliuosiuose scenarijuose, eilutes galima įtraukti į operaciją ilgesnį laiką. Todėl parinktis **Pasirinkti mokant** yra reikalinga, siekiant užtikrinti optimalų įrenginio pasiekiamumą.

### <a name="network-peripherals"></a>Išoriniai tinklo įrenginiai

Aparatūros šablono įrenginių tinklo priskyrimas leidžia kasos stalčius, kvitų spausdintuvus ir mokėjimo terminalus prijungti per tinklo ryšį.

#### <a name="modern-pos-for-windows"></a>„Windows“ skirta „Modern POS“

Išoriniams tinklo įrenginiams IP adresus galite nurodyti dviejose vietose. Jei „Modern POS Windows“ klientas naudoja vieną išorinių tinklo įrenginių rinkinį, tų įrenginių IP adresus turite nustatyti naudodami paties registro veiksmų srities parinktį **IP konfigūracija**. Tinklo įrenginių, kurie bendrai naudojami tarp EKA registrų, atveju, aparatūros šablonas, kuriam priskirti įrenginiai, gali būti tiesiogiai susietas su bendrai naudojama aparatūros stotimi. Norėdami priskirti IP adresus, pasirinkite tą aparatūros stotį puslapyje **Parduotuvės** ir tada naudokite skyriuje **Aparatūros stotys** esančią parinktį **IP konfigūracija**, norėdami nurodyti tinklo įrenginius, kurie yra priskirti prie tos aparatūros stoties. Aparatūros stotyse, kurios turi tik tinklo įrenginių, jums nereikės įdiegti pačios aparatūros stoties. Tokiu atveju aparatūros stotis reikalinga tik tam, kad konceptualiai sugrupuotų tinklui adresuojamus įrenginius pagal jų vietą parduotuvėje.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>„Cloud POS“ ir „Modern POS“, skirti „iOS“

Logika, pagal kurią valdomi fiziškai prijungti ir tinklui adresuojami išoriniai įrenginiai, yra aparatūros stotyje. Todėl visuose EKA klientuose, išskyrus „Modern POS“, skirtus „Windows“ ir „Android“, turi būti įdiegta ir aktyvi IIS aparatūros stotis, kad EKA galėtų susisiekti su periferiniais įrenginiais, nepriklausomai nuo to, ar tie periferiniai įrenginiai yra fiziškai prijungti prie aparatūros stoties, ar iškviesti per tinklą.

## <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija
### <a name="hardware-station-installation"></a>Aparatūros stoties diegimas

Daugiau informacijos rasite [„Aparatūros stoties konfigūravimas ir diegimas“](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>„Windows“ skirtos „Modern POS“ nustatymas ir konfigūracija

Daugiau informacijos žr. [„Modern POS” (MPOS) konfigūravimas, diegimas ir aktyvinimas](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>„Modern POS“, skirto „Android“ ir „iOS“ nustatymas ir konfigūravimas

Daugiau informacijos žr. [Programos „POS hybrid” nustatymas, skirtas „Android” ir „iOS”](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp).

### <a name="opos-device-setup-and-configuration"></a>OEKA įrenginio nustatymas ir konfigūracija

Išsamesnės informacijos apie OEKA komponentus žr. šio dokumento skyrių „Palaikomos sąsajos". Paprastai OEKA tvarkykles pateikia įrenginio gamintojas. Kai įdiegiama OEKA įrenginio tvarkyklė, į „Windows“ registrą įtraukiamas raktas vienoje iš šių vietų:

-   **32 bitų sistemose:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64 bitų sistemose:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Registro vietoje „ServiceOPOS“ sukonfigūruoti įrenginiai išdėstomi pagal OEKA įrenginio klasę. Išsaugomos kelios įrenginių tvarkyklės.

## <a name="supported-scenarios-by-hardware-station-type"></a>Palaikomi scenarijai pagal aparatūros stoties tipą
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Kliento palaikymas – IPC aparatūros stotis lyginant su IIS aparatūros stotimi

Toliau pateikiamoje lentelėje parodyti palaikomi topologijų ir įdiegimo scenarijai.

| Klientas      | IPC aparatūros stotis | IIS aparatūros stotis |
|-------------|----------------------|----------------------|
| „Windows“ programa | Taip                  | Taip                  |
| „Cloud POS“   | Ne                   | Taip                  |
| „Android“     | Taip                  | Taip                  |
| „iOS“         | Ne                   | Taip                  |

### <a name="network-peripherals"></a>Išoriniai tinklo įrenginiai

Tinklo periferinius įrenginius galima palaikyti tiesiogiai per aparatūros stotį, integruotą į „Modern POS“, skirtą „Windows“ ir „Android“ programoms. Visiems kitiems klientams turite įdiegti IIS aparatūros stotį.

| Klientas      | IPC aparatūros stotis | IIS aparatūros stotis |
|-------------|----------------------|----------------------|
| „Windows“ programa | Taip                  | Taip                  |
| „Cloud POS“   | Ne                   | Taip                  |
| „Android“     | Taip                  | Taip                  |
| „iOS“         | Ne                   | Taip                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Palaikomų įrenginių tipai pagal aparatūros stoties tipą
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>„Windows“ skirta „Modern POS“ su IPC (įtaisyta) aparatūros stotimi

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Palaikoma įrenginio klasė</th>
<th>Palaikomos sąsajos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>„Windows“ tvarkyklė</li>
<li>Įrenginys</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="even">
<td>2 spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>„Windows“ tvarkyklė</li>
<li>Įrenginys</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eilutės rodymas</td>
<td>OEKA</td>
</tr>
<tr class="even">
<td>Dvigubas rodymas</td>
<td>„Windows“ tvarkyklė</td>
</tr>
<tr class="odd">
<td>MSR</td>
<td><ul>
<li>OEKA</li>
<li>UWP (Nustatymas nereikalingas.)</li>
<li>Klavišinis kredito kortelių skaitytuvas (Nustatymas nereikalingas.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Išdavėjas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas </br><strong>Pastaba.</strong> Jei sukonfigūruota stalčiaus parinktis <strong>Naudoti bendrinamą pamainą</strong>, galima nustatyti tik vieną stalčių.</li>
</ul></td>
</tr>
<tr class="odd">
<td>2 stalčius</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas </br><strong>Pastaba.</strong> Jei sukonfigūruota stalčiaus parinktis <strong>Naudoti bendrinamą pamainą</strong>, galima nustatyti tik vieną stalčių.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skaitytuvas</td>
<td><ul>
<li>OEKA</li>
<li>UWP (Nustatymas nereikalingas.)</li>
<li>Klavišinis kredito kortelių skaitytuvas (Nustatymas nereikalingas.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>2 skaitytuvas</td>
<td><ul>
<li>OEKA</li>
<li>UWP (Nustatymas nereikalingas.)</li>
<li>Klavišinis kredito kortelių skaitytuvas (Nustatymas nereikalingas.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Mastelis</td>
<td>OEKA</td>
</tr>
<tr class="odd">
<td>PIN rinkiklis</td>
<td>OEKA (Palaikymas teikiamas per mokėjimo jungties tinkinimą.)</td>
</tr>
<tr class="even">
<td>Parašo fiksavimas</td>
<td>OEKA</td>
</tr>
<tr class="odd">
<td>Mokėjimo terminalas</td>
<td><ul>
<li>Pasirinktinis įrenginio palaikymas</li>
<li>Tinklas (Išsamesnės informacijos žr. mokėjimo jungties dokumentaciją.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Visi „Modern POS“ klientai, turintys patvirtintą „Bendrą“ IIS aparatūros stotį

> [!NOTE]
> Kai IIS aparatūros stotis yra „patvirtinta“, tarp EKA kliento ir aparatūros stoties yra ryšys „vienas su vienu“.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Palaikoma įrenginio klasė</th>
<th>Palaikomos sąsajos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="even">
<td>2 spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eilutės rodymas</td>
<td>OEKA</td>
</tr>
<tr class="even">
<td>MSR</td>
<td>OEKA</td>
</tr>
<tr class="odd">
<td>Išdavėjas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas </br><strong>Pastaba.</strong> Jei sukonfigūruota stalčiaus parinktis <strong>Naudoti bendrinamą pamainą</strong>, viename aparatūros šablone galima nustatyti tik vieną stalčių.</li>
</ul></td>
</tr>
<tr class="even">
<td>2 stalčius</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skaitytuvas</td>
<td>OEKA</td>
</tr>
<tr class="even">
<td>2 skaitytuvas</td>
<td>OEKA</td>
</tr>
<tr class="odd">
<td>Mastelis</td>
<td>OEKA</td>
</tr>
<tr class="even">
<td>PIN rinkiklis</td>
<td>OEKA (Palaikymas teikiamas per mokėjimo jungties tinkinimą.)</td>
</tr>
<tr class="odd">
<td>Par. perimti</td>
<td>OEKA</td>
</tr>
<tr class="even">
<td>Mokėjimo terminalas</td>
<td><ul>
<li>Pasirinktinis įrenginio palaikymas</li>
<li>Tinklas (Išsamesnės informacijos žr. mokėjimo jungties dokumentaciją.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-shared-an-iis-hardware-station"></a>Visi „Modern POS“ klientai, turintys bendrą IIS aparatūros stotį

> [!NOTE]
> Kai IIS aparatūros stotis yra „bendrai naudojama“, tuo pačiu metu aparatūros stotį gali naudoti keli įrenginiai. Šiame scenarijuje turite naudoti tik tuos įrenginius, kurie išvardyti toliau pateikiamoje lentelėje. Jei bandysite bendrai naudoti įrenginius, kurie čia nėra išvardyti, pvz., brūkšninių kodų skaitytuvus ir MSR, keliems įrenginiams reikalaujant patvirtinti tą patį išorinį įrenginį, įvyks klaidų. Ateityje tokios konfigūracijos bus siekiama tiesiogiai išvengti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Palaikoma įrenginio klasė</th>
<th>Palaikomos sąsajos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="even">
<td>2 spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="odd">
<td>Išdavėjas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas </br><strong>Pastaba.</strong> Jei sukonfigūruota stalčiaus parinktis <strong>Naudoti bendrinamą pamainą</strong>, viename aparatūros šablone galima nustatyti tik vieną stalčių.</li>
</ul></td>
</tr>
<tr class="even">
<td>2 stalčius</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="odd">
<td>Mokėjimo terminalas</td>
<td><ul>
<li>Pasirinktinis įrenginio palaikymas</li>
<li>Tinklas (Išsamesnės informacijos žr. mokėjimo jungties dokumentaciją.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Palaikomų scenarijų konfigūracija
Išsamesnės informacijos apie tai, kaip kurti aparatūros šablonus, žr. [Apibrėžti ir prižiūrėti kanalų klientus, įskaitant registrus ir aparatūros stotis](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>„Windows“ skirta „Modern POS“ su IPC (įtaisyta) aparatūros stotimi

Ši konfigūracija yra labiausiai įprasta tradicinių fiksuotų EKA registrų konfigūracija. Šiame scenarijuje aparatūros šablono informacija tiesiogiai susiejama su pačiu EKA registru. EFT terminalo numeris taip pat turi būti nustatytas pačiame registre. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurkite aparatūros šabloną, kur konfigūruojami visi reikiami išoriniai įrenginiai.
2.  Susiekite aparatūros šabloną su EKA registru.
3.  Parduotuvei, kurioje bus naudojamas EKA registras, sukurkite aparatūros stotį, kurios tipas **Paskirta**. Aprašas nėra būtinas. 

    > [!NOTE]
    > Aparatūros stotyje neprivalote nustatyti jokių kitų ypatybių. Visa kita reikiama informacija, pvz., aparatūros šablonas, bus gauta iš paties registro.

4.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas**.
5.  Pasirinkite paskirstymo grafiką **1090** norėdami sinchronizuoti naują parduotuvės aparatūros šabloną. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
6.  Pasirinkite paskirstymo grafiką **1040** norėdami sinchronizuoti naują parduotuvės aparatūros stotį. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
7.  Įdiekite ir suaktyvinkite „Windows“ skirtą „Modern POS“.
8.  Paleiskite „Windows“ skirtą „Modern POS“ ir pradėkite naudoti prijungtus išorinius įrenginius.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>„Modern POS“, skirta „Android“, turi įmontuotą IPC aparatūros stotį

**Nauja versijai 10.0.8** – „Epson“ tinklo spausdintuvai ir grynųjų pinigų stalčiai, prijungti prie tų spausdintuvų per DK prievadą, dabar palaikomi „Modern POS“, skirtos „Android“ programai. Norėdami gauti daugiau informacijos, apsilankykite puslapyje [Programos „POS Hybrid“ nustatymas, skirtas „Android” ir „iOS”](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Visi „Modern POS“ klientai, turintys patvirtintą bendrą IIS aparatūros stotį

Šią konfigūraciją galima naudoti visiems „Modern POS“ klientams, kurie turi aparatūros stotį, išskirtinai naudojamą vieno EKA registro. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurkite aparatūros šabloną, kur konfigūruojami visi reikiami išoriniai įrenginiai.
2.  Parduotuvei, kurioje bus naudojamas EKA registras, sukurkite aparatūros stotį, kurios tipas **Paskirta**.
3.  Paskirtoje aparatūros stotyje nustatykite šias ypatybes:
    -   **Pagrindinio kompiuterio vardas** – pagrindinio kompiuterio, kuriame bus vykdoma aparatūros stotis, pavadinimas. 
    
        > [!NOTE]
        > „Cloud POS“ gali pašalinti **vietinį pagrindinį kompiuterį** siekiant nustatyti vietinį kompiuterį, kuriame vykdoma „Cloud POS“. Tačiau sertifikato, kurio reikia norint susieti „Cloud POS“ su aparatūros stotimi, kompiuterio vardas turi būti „Vietinis pagrindinis kompiuteris“. Siekiant išvengti problemų, rekomenduojame išvardyti kiekvienos parduotuvei paskirtos aparatūros stoties atvejį, kaip reikalaujama. Kiekvienos aparatūros stoties pagrindinio kompiuterio pavadinimas turi būti to kompiuterio, kuriame bus įdiegta aparatūros stotis, pavadinimas.
    
    -   **Prievadas** – aparatūros stoties ir „Modern POS“ kliento ryšiui palaikyti naudojamas prievadas.
    -   **Aparatūros šablonas** – jei aparatūros šablonas nepateikiamas pačioje aparatūros stotyje, bus naudojamas registrui priskirtas aparatūros šablonas.
    -   **EFT EKA numeris** – EFT terminalo ID, naudojamas, kai siunčiami EFT įgaliojimai. Šį ID pateikia kredito kortelių procesorius.
    -   **Paketo pavadinimas** – aparatūros stoties paketas, naudojamas įdiegiant aparatūros stotį.

4.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas**.
5.  Pasirinkite paskirstymo grafiką **1090** norėdami sinchronizuoti naują parduotuvės aparatūros šabloną. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
6.  Pasirinkite paskirstymo grafiką **1040** norėdami sinchronizuoti naują parduotuvės aparatūros stotį. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
7.  Įdiekite aparatūros stotį. Daugiau informacijos apie tai, kaip įdiegti aparatūros stotį, žr. [Mažmeninės prekybos aparatūros stoties konfigūracija ir diegimas](retail-hardware-station-configuration-installation.md).
8.  Įdiekite ir suaktyvinkite „Modern POS“. Daugiau informacijos apie tai, kaip įdiegti „Modern POS“, žr. [„Modern POS“ (MPOS) konfigūravimas, diegimas ir aktyvinimas](retail-modern-pos-device-activation.md).
9.  Prisijunkite prie „Modern POS“ ir pasirinkite **Atlikti su stalčiumi nesusijusią operaciją**.
10. Pradėkite operaciją **Tvarkyti aparatūros stotis**.
11. Spustelėkite **Tvarkyti**.
12. Aparatūros stoties tvarkymo puslapyje nustatykite aparatūros stoties įjungimo parinktį.
13. Pasirinkite naudojamą aparatūros stotį, tada spustelėkite **Susieti**.
14. Kai aparatūros stotis bus susieta, spustelėkite **Uždarykite**.
15. Aparatūros stoties pasirinkimo puslapyje spustelėję ką tik pasirinktą aparatūros stotį, ją suaktyvinsite.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visi „Modern POS“ klientai, turintys bendrai naudojamą IIS aparatūros stotį

Šią konfigūraciją galima naudoti visiems „Modern POS“ klientams, kurie aparatūros stotis bendrai naudoja su kitais įrenginiais. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurkite aparatūros šabloną, kur konfigūruojami reikiami išoriniai įrenginiai.
2.  Parduotuvei, kurioje bus naudojamas EKA registras, sukurkite aparatūros stotį, kurios tipas **Bendrinama**.
3.  Bendrai naudojamoje aparatūros stotyje nustatykite šias ypatybes:
    -   **Pagrindinio kompiuterio vardas** – pagrindinio kompiuterio, kuriame bus vykdoma aparatūros stotis, pavadinimas.
    -   **Aprašas** – tekstas, kuris padės identifikuoti aparatūros stotį, pvz., **Grąžinimai** arba **Parduotuvės pagrindinė**.
    -   **Prievadas** – aparatūros stoties ir „Modern POS“ kliento ryšiui palaikyti naudojamas prievadas.
    -   **Aparatūros šablonas** – kiekviena bendrai naudojama aparatūros stotis turi turėti aparatūros šabloną. Aparatūros šablonus gali bendrai naudoti aparatūros stotys, bet jie turi būti susieti su kiekviena aparatūros stotimi. Be to, rekomenduojame naudoti bendrai naudojamas pamainas, kai tą pačią aparatūros stotį naudoja keli įrenginiai. Norėdami nustatyti bendrą pamainą, spauskite **„Retail and Commerce“** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**. Kiekviename bendrai naudojamame aparatūros šablone pasirinkite kasos stalčių ir nustatykite parinktį **Bendrinamas pamainos stalčius** į **Taip**.
    -   **EFT EKA numeris** – EFT terminalo ID, naudojamas, kai siunčiami EFT įgaliojimai. Šį ID pateikia kredito kortelių procesorius.
    -   **Paketo pavadinimas** – aparatūros stoties paketas, naudojamas įdiegiant aparatūros stotį.

4.  Pakartokite 2 ir 3 veiksmus kiekvienai papildomai aparatūros stočiai, kuri reikalinga parduotuvėje.
5.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas**.
6.  Pasirinkite paskirstymo grafiką **1090** norėdami sinchronizuoti naują parduotuvės aparatūros šabloną. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
7.  Pasirinkite paskirstymo grafiką **1040** norėdami sinchronizuoti naują parduotuvės aparatūros stotį. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
8.  Aparatūros stotį įdiekite kiekviename pagrindiniame kompiuteryje, kuriuos nustatėte atlikdami 2 ir 3 veiksmus. Daugiau informacijos apie tai, kaip įdiegti aparatūros stotį, žr. [Mažmeninės prekybos aparatūros stoties konfigūracija ir diegimas](retail-hardware-station-configuration-installation.md).
9.  Įdiekite ir suaktyvinkite „Modern POS“. Daugiau informacijos apie tai, kaip įdiegti „Modern POS“, žr. [„Modern POS“ (MPOS) konfigūravimas, diegimas ir aktyvinimas](retail-modern-pos-device-activation.md).
10. Prisijunkite prie „Modern POS“ ir pasirinkite **Atlikti su stalčiumi nesusijusią operaciją**.
11. Pradėkite operaciją **Tvarkyti aparatūros stotis**.

12. Spustelėkite **Tvarkyti**.
13. Aparatūros stoties tvarkymo puslapyje nustatykite aparatūros stoties įjungimo parinktį.
14. Pasirinkite naudojamą aparatūros stotį, tada spustelėkite **Susieti**.
15. Pakartokite 14 veiksmą kiekvienai aparatūros stočiai, kurią naudos „Modern POS“.
16. Kai visos reikalingos aparatūros stotys susietos, spustelėkite **Uždaryti**.
17. Aparatūros stoties pasirinkimo puslapyje spustelėję ką tik pasirinktą aparatūros stotį, ją suaktyvinsite. 

> [!NOTE]
> Jei įrenginiai dažnai naudoja skirtingas aparatūros stotis, rekomenduojame taip sukonfigūruoti „Modern POS“, kad paragintų kasininkus pradedant mokėjimo procesą pasirinkti aparatūros stotį. Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **Registrai**. Pasirinkite registrą, tada nustatykite parinktį **Pasirinkti mokant** į **Taip**. Naudodami paskirstymo grafiką **1090** sinchronizuokite kanalo duomenų bazės pakeitimus.

## <a name="extensibility"></a>Išplečiamumas
Išsamesnės informacijos apie aparatūros stoties išplėtimo scenarjus, žr. [Aparatūros stoties išplėtimas](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Sauga
Pagal dabartinius saugos standartus gamybos aplinkoje turi būti naudojami šie parametrai: 

### <a name="hardware-station-installer"></a>Aparatūros stoties diegimo programa
Aparatūros stoties diegimo programa automatiškai atliks šiuos registro redagavimus kaip savitarnos diegimo dalį.
 
-   Saugiųjų jungčių lygmenį (SSL) reikia išjungti.
-   Įjungta ir naudojama turi būti tik transportavimo lygmens saugos (TLS) 1.2 versija (arba naujausia dabartinė versija). 

### <a name="ssl-and-tls"></a>SSL ir TLS
Pagal numatytuosius parametrus išjungtos SSL ir visos TLS versijos, išskyrus TLS 1.2 versiją. Norėdami redaguoti ar įgalinti šias vertes, atlikite šiuos veiksmus:
    1.  Paspaudę „Windows“ logotipo klavišą + R atidarysite langą **Vykdyti**.
    2.  Lauke **Atidaryti** įveskite **„Regedit“**, tada spustelėkite **Gerai**.
    3.  Jei pasirodo pranešimų laukas **Vartotojo paskyros valdymo tarnyba**, spustelėkite **Taip**.
    4.  Lange **Registro rengyklė** eikite į **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Siekiant leisti tik TLS 1.2 versiją, šie raktai jau įvesti automatiškai:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Neturi būti atidarytų jokių papildomų tinklo prievadų, nebent jie yra reikalingi dėl žinomų, nurodytų priežasčių.
-   Kryžminės kilmės išteklių bendrinimas turi būti išjungtas ir turi būti nurodyta leidžiama kilmė, kuri priimta.
-   Reikia naudoti tik patikimas sertifikavimo tarnybas sertifikatams gauti, kurie bus naudojami kompiuteriuose, vykdančiuose aparatūros stotį.

> [!NOTE]
> Labai svarbu peržiūrėti IIS ir mokėjimo kortelių pramonės (PCI) reikalavimų saugos gaires.

## <a name="peripheral-simulator"></a>Periferinis simuliatorius
Daugiau informacijos žr. [„Commerce“ periferinis simuliatorius](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>„Microsoft“ išbandyti išoriniai įrenginiai
### <a name="ipc-built-in-hardware-station"></a>IPC (įtaisytoji) aparatūros stotis

Toliau nurodyti išoriniai įrenginiai buvo išbandyti naudojant IPC aparatūros stotį, kuri yra įtaisyta „Windows“ skirtoje „Modern POS“.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                |
|--------------|----------|-----------|-------------------------|
| „Epson“        | Tm-T88IV | OEKA      |                         |
| „Epson“        | TM-T88V  | OEKA      |                         |
| „Epson“        | TM-T88   | Pasirinktinis    | Prijungtas per tinklą   |
| „Star“         | TSP650II | Pasirinktinis    | Prijungtas per tinklą   |
| „Star“         | mPOP     | OEKA      | Prijungtas per „Bluetooth“ |
| „HP“           | F7M67AA  | OEKA      | Teikiamas USB             |

#### <a name="bar-code-scanner"></a>Brūkšninio kodo skaitytuvas

| Gamintojas  | Modelis         | Sąsaja | Komentarai |
|---------------|---------------|-----------|----------|
| „Motorola“      | DS9208        | OEKA      |          |
| „Honeywell“     | 1900          | UWP       |          |
| Simbolis        | LS2208        | OEKA      |          |
| „HP Integrated“ | E1L07AA       | OEKA      |          |
| „Datalogic“     | „Magellan 8400“ | OEKA      |          |

#### <a name="pin-pad"></a>PIN rinkiklis

| Gamintojas | Modelis  | Sąsaja | Komentarai                                        |
|--------------|--------|-----------|-------------------------------------------------|
| „VeriFone“     | 1000SE | OEKA      | Reikia mokėjimo jungties tinkinimo |

#### <a name="payment-terminal"></a>Mokėjimo terminalas

| Gamintojas | Modelis | Sąsaja | Komentarai                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| „Equinox“      | L5300 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo                                |
| „VeriFone“     | MX925 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |
| „VeriFone“     | MX915 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |

#### <a name="cash-drawer"></a>Kasos stalčius

| Gamintojas | Modelis     | Sąsaja | Komentarai                |
|--------------|-----------|-----------|-------------------------|
| „Star“         | mPOP      | OEKA      | Prijungtas per „Bluetooth“ |
| „APG“          | „Atwood“    | Pasirinktinis    | Prijungtas per tinklą   |
| „Star“         | SMD2-1317 | OEKA      |                         |
| „HP“           | QT457AA   | OEKA      |                         |
| „Epson“        |           | Pasirinktinis    | „Epson“ spausdintuvas prijungtas prie tinklo per DK prievadą |

#### <a name="line-display"></a>Eilutės rodymas

| Gamintojas  | Modelis   | Sąsaja | Komentarai |
|---------------|---------|-----------|----------|
| „HP Integrated“ | G6U79AA | OEKA      |          |
| „Epson“         | M58DC   | OEKA      |          |

#### <a name="signature-capture"></a>Parašo fiksavimas

| Gamintojas | Modelis  | Sąsaja | Komentarai |
|--------------|--------|-----------|----------|
| „Scriptel“     | ST1550 | OEKA      |          |

#### <a name="scale"></a>Mastelis

| Gamintojas | Modelis         | Sąsaja | Komentarai |
|--------------|---------------|-----------|----------|
| „Datalogic“    | „Magellan 8400“ | OEKA      |          |

#### <a name="msr"></a>MSR

| Gamintojas | Modelis       | Sąsaja | Komentarai |
|--------------|-------------|-----------|----------|
| „Magtek“       | 21073075    | UWP       |          |
| „Magtek“       | 21073062    | OEKA      |          |
| „HP“           | IDRA-334133 | OEKA      |          |

### <a name="dedicated-iis-hardware-station"></a>Paskirta IIS aparatūros stotis

Toliau nurodyti išoriniai įrenginiai buvo išbandyti naudojant paskirtą (ne bendrinamą) IIS aparatūros stotį kartu su „Windows“ skirta „Modern POS“ ir „Cloud POS“.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                  |
|--------------|----------|-----------|---------------------------|
| „Epson“        | Tm-T88IV | OEKA      |                           |
| „Epson“        | TM-T88V  | OEKA      |                           |
| „Epson“        | TM-T88V  | Pasirinktinis    | Prisijungtas per tinklą     |
| „Star“         | TSP650II | Pasirinktinis    | Prijungtas per tinklą     |
| „HP“           | F7M67AA  | OEKA      | Teikiamas USB               |

#### <a name="bar-code-scanner"></a>Brūkšninio kodo skaitytuvas

| Gamintojas  | Modelis   | Sąsaja | Komentarai |
|---------------|---------|-----------|----------|
| „Motorola“      | DS9208  | OEKA      |          |
| Simbolis        | LS2208  | OEKA      |          |
| „HP Integrated“ | E1L07AA | OEKA      |          |

#### <a name="pin-pad"></a>PIN rinkiklis

| Gamintojas | Modelis  | Sąsaja | Komentarai                                        |
|--------------|--------|-----------|-------------------------------------------------|
| „VeriFone“     | 1000SE | OEKA      | Reikia mokėjimo jungties tinkinimo |

#### <a name="payment-terminal"></a>Mokėjimo terminalas

| Gamintojas | Modelis | Sąsaja | Komentarai                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| „Equinox“      | L5300 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo                                |
| „VeriFone“     | MX925 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |
| „VeriFone“     | MX915 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |

#### <a name="cash-drawer"></a>Kasos stalčius

| Gamintojas | Modelis     | Sąsaja | Komentarai              |
|--------------|-----------|-----------|-----------------------|
| „APG“          | „Atwood“    | Pasirinktinis    | Prijungtas per tinklą |
| „Star“         | SMD2-1317 | OEKA      |                       |
| „HP“           | QT457AA   | OEKA      |                       |
| „Epson“        |           | Pasirinktinis    | „Epson“ spausdintuvas prijungtas prie tinklo per DK prievadą |

#### <a name="line-display"></a>Eilutės rodymas

| Gamintojas  | Modelis   | Sąsaja | Komentarai |
|---------------|---------|-----------|----------|
| „HP Integrated“ | G6U79AA | OEKA      |          |
| „Epson“         | M58DC   | OEKA      |          |

#### <a name="signature-capture"></a>Parašo fiksavimas

| Gamintojas | Modelis  | Sąsaja | Komentarai |
|--------------|--------|-----------|----------|
| „Scriptel“     | ST1550 | OEKA      |          |

#### <a name="scale"></a>Mastelis

| Gamintojas | Modelis         | Sąsaja | Komentarai |
|--------------|---------------|-----------|----------|
| „Datalogic“    | „Magellan 8400“ | OEKA      |          |

#### <a name="msr"></a>MSR

| Gamintojas | Modelis       | Sąsaja | Komentarai |
|--------------|-------------|-----------|----------|
| „Magtek“       | 21073075    | UWP       |          |
| „Magtek“       | 21073062    | OEKA      |          |
| „HP“           | IDRA-334133 | OEKA      |          |

### <a name="shared-iis-hardware-station"></a>Bendrinama IIS aparatūros stotis

Toliau nurodyti išoriniai įrenginiai buvo išbandyti naudojant bendrinamą IIS aparatūros stotį kartu su „Windows“ skirta „Modern POS“ ir „Cloud POS“. 

> [!NOTE]
> Palaikomas tik spausdintuvas, mokėjimo terminalas ir kasos stalčius.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                  |
|--------------|----------|-----------|---------------------------|
| „Epson“        | TM-T88IV | OEKA      |                           |
| „Epson“        | TM-T88V  | OEKA      |                           |
| „Epson“        | TM-T88   | Pasirinktinis    | Prijungtas per tinklą     |
| „Star“         | TSP650II | Pasirinktinis    | Prijungtas per tinklą     |
| „HP“           | F7M67AA  | OEKA      | Teikiamas USB               |

#### <a name="payment-terminal"></a>Mokėjimo terminalas

| Gamintojas | Modelis | Sąsaja | Komentarai                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| „VeriFone“     | MX925 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |
| „VeriFone“     | MX915 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |

#### <a name="cash-drawer"></a>Kasos stalčius

| Gamintojas | Modelis     | Sąsaja | Komentarai              |
|--------------|-----------|-----------|-----------------------|
| „APG“          | „Atwood“    | Pasirinktinis    | Prijungtas per tinklą |
| „Star“         | SMD2-1317 | OEKA      |                       |
| „HP“           | QT457AA   | OEKA      |                       |
| „Epson“        |           | Pasirinktinis    | „Epson“ spausdintuvas prijungtas prie tinklo per DK prievadą |


## <a name="troubleshooting"></a>Trikčių šalinimas
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>„Modern POS“ savo pasirinkimo sąraše gali aptikti aparatūros stotį, tačiau ji negali baigti susiejimo

**Sprendimas:** patikrinkite toliau pateikiamą galimų trikčių punktų sąrašą:

-   Kompiuteris, kuris vykdo „Modern POS“, pasitiki tuo sertifikatu, kuris naudojamas aparatūros stotį vykdančiame kompiuteryje.
    -   Norėdami patikrinti šią sąranką, žiniatinklio naršyklėje eikite į šį URL: https://&lt;Kompiuterio pavadinimas&gt;&lt;Prievado numeris&gt;/HardwareStation/ping.
    -   Šiame URL naudojama ryšio užklausa, siekiant patikrinti, ar kompiuterį galima pasiekti, o naršyklė nurodo, ar sertifikatas patikimas. (Pvz., „Internet Explorer“ adreso juostoje pasirodo spynos piktograma. Spustelėjus šią piktogramą, „Internet Explorer“ patikrina, ar dabar naudojamas sertifikatas patikimas. Vietiniame kompiuteryje sertifikatą galite įdiegti peržiūrėję rodomo sertifikato informaciją.)
-   Aparatūros stotį vykdančiame kompiuteryje prievadas, kuris bus naudojamas aparatūros stotyje, atidaromas užkardoje.
-   Aparatūros stotis tinkamai įdiegė prekybininko sąskaitos informaciją naudojant įrankį Įdiegti prekybininko informaciją, kuris vykdomas aparatūros stoties diegimo programos pabaigoje.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>„Modern POS“ savo pasirinkimo sąraše negali aptikti aparatūros stoties

**Sprendimas:** šią problemą sukelti gali bet kuris iš šių veiksnių:

-   Aparatūros stotis nebuvo tinkamai nustatyta būstinėje. Atlikę anksčiau šioje temoje nurodytus veiksmus, patikrinkite, ar tinkamai įvestas aparatūros stoties šablonas ir aparatūros stotis.
-   Siekiant atnaujinti kanalo konfigūraciją, darbai nebuvo atlikti. Tokiu atveju vykdykite kanalo konfigūracijos 1070 užduotį.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>„Modern POS“ neatspindi naujų kasos stalčiaus nustatymų

**Sprendimas:** uždarykite dabartinį paketą. Kasos stalčiaus pakeitimai nebus atnaujinti „Modern POS“ tol, kol nebus uždarytas dabartinis paketas.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>„Modern POS“ praneša apie problemą, susijusią su periferiniu įrenginiu

**Sprendimas:** toliau nurodytos kai kurios tipinės šios problemos priežastys:

-   Įsitikinkite, kad uždarytos kitos įrenginių tvarkyklių konfigūravimo priemonės. Jei šios priemonės atidarytos, jos gali neleisti „Modern POS“ arba aparatūros stočiai patvirtinti įrenginį.
-   Jei išorinis įrenginys bendrinamas su keliais EKA įrenginiais, įsitikinkite, kad jis priklauso vienai iš toliau pateikiamų kategorijų.
    -   Kasos stalčius
    -   Kvitų spausdintuvas
    -   Mokėjimo terminalas

    Jei išorinis įrenginys nepriklauso kuriai nors iš šių kategorijų, aparatūros stotis nėra skirta įgalinti išorinį įrenginį, skirtą bendrinti su keliais EKA įrenginiais.
-   Kartais įrenginių tvarkyklės gali sukelti bendrųjų valdymo objektų (CCO) veikimo sutrikimų. Jei įrenginys buvo neseniai įdiegtas, bet neveikia tinkamai, arba pastebima kitų problemų, šias problemas dažnai galima išspręsti iš naujo įdiegus CCO. Norėdami atsisiųsti CCO, apsilankykite <http://monroecs.com/oposccos_current.htm>.
-   Jei išorinių pakeitimų dažnai atliekate tikrinimo ar trikčių diagnostikos metu, gali tekti iš naujo nustatyti IIS, o ne laukti, kol talpykla atsinaujins pati. Norėdami iš naujo nustatyti IIS, atlikite šiuos veiksmus:
    1.  Meniu **Pradėti** įveskite **CMD**.
    2.  Ieškos rezultatuose dešiniuoju pelės klavišu spustelėkite **Komandinė eilutė**, tada spustelėkite **Paleisti administratoriaus teisėmis**.
    3.  Lange **Komandinė eilutė** įveskite **iisreset /Restart** ir paspauskite „Enter“.
    4.  Po to, kai iš naujo paleista IIS, iš naujo paleiskite „Modern POS“.
-   Jei dažnai atliekate išorinių įrenginių keitimų, jei dažnai paleidžiate ir išeinate iš EKA kliento, DLL pagrindinės saugyklos procesas iš ankstesnio EKA seanso gali kliudyti dabartiniam seansui. Tokiu atveju įrenginio gali nepavykti naudoti, kol neuždarysite dinaminių saitų bibliotekos (DLL) pagrindinės saugyklos, kuri tvarko ankstesnį seansą. Norėdami uždaryti DLL pagrindinę saugyklą, atlikite šiuos veiksmus:
    1.  Meniu **Pradėti** įveskite **Užduočių tvarkytuvas**.
    2.  Ieškos rezultatuose spustelėkite **Užduočių tvarkytuvas**.
    3.  Užduočių tvarkytuvo skirtuke **Išsami informacija** spustelėję stulpelio antraštę, pažymėtą **Pavadinimas**, surūšiuosite lentelę abėcėlės tvarka pagal pavadinimą.
    4.  Slinkite žemyn, kol rasite dllhost.exe.
    5.  Pasirinkite kiekvieną DLL pagrindinę saugyklą, tada spustelėkite **Baigti užduotį**.
    6.  Po to, kai DLL pagrindinės saugyklos uždarytos, iš naujo paleiskite „Modern POS“.


<a name="additional-resources"></a>Papildomi ištekliai
--------

[„Commerce“ periferinis simuliatorius](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]