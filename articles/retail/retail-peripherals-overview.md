---
title: "Išorinių mažmeninės prekybos įrenginių apžvalga"
description: "Šioje temoje paaiškintos su išoriniais mažmeninės prekybos įrenginiais susijusios koncepcijos."
author: rubencdelgado
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: ba9c828efc39d45a78500d30295e5d1d6c770c99
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---

# <a name="retail-peripherals-overview"></a>„Retail” išorinių įrenginių apžvalga

[!include[banner](includes/banner.md)]


Šioje temoje paaiškintos su išoriniais mažmeninės prekybos įrenginiais susijusios koncepcijos. Joje apibūdinti įvairūs būdai, kaip išorinius įrenginius galima prijungti prie elektroninio kasos aparato (EKA), ir komponentai, skirti valdyti ryšį su EKA.

## <a name="concepts"></a>Koncepcijos

### <a name="pos-registers"></a>EKA registrai

Naršymas: spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Registrai**. EKA registras yra objektas, kuris naudojamas konkretaus EKA egzemplioriaus charakteristikoms nustatyti. Šios charakteristikos apima mažmeninės prekybos išorinių įrenginių, kurie bus naudojami registre, aparatūros šabloną ar nustatymą, su registru susietą parduotuvę ir prie registro prisijungusio vartotojo vaizdinę patirtį.

### <a name="devices"></a>Įrenginiai

Naršymas: spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Įrenginiai**. Įrenginys yra objektas, nurodantis su EKA registru susieto įrenginio fizinį egzempliorių. Sukūrus įrenginį, jis susiejamas su EKA registru. Įrenginio objektas seka informaciją apie POS registro suaktyvinimo laiką, naudojamo kliento tipą ir programų paketą, kuris buvo įdiegtas konkrečiame įrenginyje. Įrenginius galima susieti su šių tipų progrmomis: „Retail Modern POS“, „Retail Cloud POS“, „Retail Modern POS“ – „Windows Phone“, „Retail Modern POS“ – „Android“ ir „Retail Modern POS“ – „iOS“.

### <a name="retail-modern-pos"></a>„Retail Modern POS“

„Modern POS“ yra EKA programa, skirta „Microsoft Windows“. Ją galima įdiegti „Windows 10“ operacinėse sistemose (OS).

### <a name="cloud-pos"></a>Cloud POS

„Cloud POS“ yra naršyklėje veikianti „Modern POS“ programos versija, kurią galima pasiekti žiniatinklio naršyklėje.

### <a name="modern-pos-for-ios"></a>„Modern POS“, skirta „iOS“

„Modern POS“, skirta „iOS“, yra „iOS“ pagrįsta „Modern POS“ programos versija, kurią galima įdiegti „iOS“ įrenginiuose.

### <a name="modern-pos-for-android"></a>„Modern POS“, skirta „Android“

„Modern POS“, skirta „Android“, yra „Android“ pagrįsta „Modern POS“ programos versija, kurią galima įdiegti „Android“ įrenginiuose.

### <a name="pos-peripherals"></a>Išoriniai EKA įrenginiai

Išoriniai EKA įrenginiai yra tokie įrenginiai, kurie tiesiogiai palaiko EKA funkcijas. Šie išoriniai įrenginiai paprastai dalijami į tam tikras klases. Daugiau informacijos apie šias klases žr. šios temos skyriuje „Įrenginių klasės“.

### <a name="hardware-station"></a>Aparatūros stotis

Naršymas: spustelėkite **Mažmeninė prekyba** &gt; **Kanalai** &gt; **Mažmeninės prekybos parduotuvės** &gt; **Visos mažmeninės prekybos parduotuvės**. Pasirinkite parduotuvę, tada spustelėkite „FastTab“ **Aparatūros stotys**. Nustatymas **Aparatūros stotis** yra kanalo lygio nustatymas, naudojamas apibrėžti egzemplioriams, kuriuose bus įdiegta mažmeninės prekybos išorinių įrenginių logika. Šis nustatymas kanalo lygiu taikomas aparatūros stoties charakteristikoms nustatyti. Jis taip pat naudojamas norint pateikti aparatūros stočių, kurios galimos „Modern POS“ egzemplioriams pasirinktoje parduotuvėje, sąrašą. Aparatūros stotis yra įtaisyta „Windows“ skirtoje „Modern POS“ programoje. Be to, aparatūros stotį galima atskirai įdiegti kaip atskirą „Microsoft“ informacinių interneto paslaugų (IIS) programą. Tokiu atveju, ją galima pasiekti per tinklą.

### <a name="hardware-profile"></a>Aparatūros šablonas

Naršymas: spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**. Aparatūros šablonas yra įrenginių, kurie sukonfigūruoti EKA registrui arba aparatūros stočiai, sąrašas. Aparatūros šabloną galima tiesiogiai priskirti EKA registrui arba aparatūros stočiai.

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

Svarstykles galima prijungti prie kompiuterio per USB naudojant OEKA tvarkykles. Kai produktas, pažymėtas kaip „pasvertas“, įtraukiamas į operaciją, EKA nuskaito svorį iš svarstyklių, įtraukia produktą į operaciją ir naudoja kiekį, kurį pateikė svarstyklės.

### <a name="pin-pad"></a>PIN rinkiklis

Asmeninio identifikavimo numerio (PIN) rinkikliai palaikomi per OEKA, bet jie turi būti valdomi per mokėjimo jungtį.

### <a name="secondary-display"></a>Antrinis rodymas

Sukonfigūravus antrinį rodymą, pagrindinei informacijai rodyti naudojamas 2 „Windows“ ekranas. Antrinio ekrano paskirtis – palaikyti nepriklausomo programinės įrangos tiekėjo (ISV) plėtinį, nes antrinis ekranas iš karto nėra sukonfigūruojamas ir rodo ribotą turinį.

### <a name="payment-device"></a>Mokėjimo įrenginys

Mokėjimo įrenginio palaikymas įdiegiamas per mokėjimo jungtį. Mokėjimo įrenginiai gali atlikti vieną ar kelias funkcijas, kurias pateikia kitos įrenginių klasės. Pvz., mokėjimo įrenginys gali veikti kaip MSR / kortelių skaitytuvas, eilučių rodymas, parašo fiksavimo įrenginys ar PIN rinkiklis. Mokėjimo įrenginių palaikymas įdiegiamas nepriklausomai nuo atskiro įrenginio palaikymo, kuris teikiamas kitiems į aparatūros šabloną įtrauktiems įrenginiams.

## <a name="supported-interfaces"></a>Palaikomos sąsajos
### <a name="opos"></a>OEKA

Siekiant užtikrinti, kad su „Microsoft Dynamics 365 for Retail“ būtų galima naudoti kuo daugiau įrenginių, EKA skirtas OLE prekybos standartas yra pirminė mažmeninės prekybos išorinių įrenginių platforma, kuri yra palaikoma sprendime „Microsoft Dynamics 365 for Retail“. EKA skirtą OLE standartą sukūrė Nacionalinė mažmeninės prekybos federacija (NRF, angl. „National Retail Federation“), nustatanti pramonės standartų ryšio protokolus, skirtus išoriniams mažmeninės prekybos įrenginiams. OEKA yra plačiai taikomas EKA standartui skirto OLE diegimas. Jis sukurtas XX a. dešimto dešimtmečio viduryje ir nuo tada buvo keletą kartų atnaujintas. OEKA pateikia įrenginių tvarkyklių architektūrą, kuri leidžia lengvai integruoti EKA aparatūrą į „Windows“ pagrįstas EKA sistemas. OEKA valdikliai tvarko ryšį tarp suderinamos aparatūros ir EKA programinės įrangos. OEKA valdiklį sudaro dvi dalys:

-   **Valdymo objektas** – įrenginio klasės (pvz., eilutės rodymas) valdymo objektas pateikia programinės įrangos programos sąsają. „Monroe Consulting Services“ ([www.monroecs.com](http://www.monroecs.com/)) pateikia standartizuotą OEKA valdymo objektų rinkinį, jie dar vadinami bendraisiais valdymo objektais (CCOs). CCO yra naudojami „Microsoft Dynamics 365 for Retail“ EKA komponentui bandyti. Todėl bandymai padeda užtikrinti, kad jei „Microsoft Dynamics 365 for Retail“ palaiko įrenginių klasę per OEKA, tai daugelio įrenginių tipai gali būti palaikomi (jei gamintojas pateikia paslaugos objektą, sukurtą OEKA). Jūs neprivalote tiesiogiai patikrinti kiekvieno įrenginio tipo.
-   **Aptarnavimo objektas** – aptarnavimo objektas tiekia ryšį tarp valdymo objekto (CCO) ir įrenginio. Įrenginio aptarnavimo objektą paprastai teikia įrenginio gamintojas. Tačiau kai kuriais atvejais gali tekti aptarnavimo objektą atsisiųsti iš gamintojo žiniatinklio svetainės. Pvz,, galbūt bus galimas naujesnis aptarnavimo objektas. Gamintojo žiniatinklio svetainės adreso žr. aparatūros dokumentaciją.

[![Valdymo objektas ir aptarnavimo objektas](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) OLE, skirto EKA, OEKA diegimo palaikymas padeda užtikrinti, kad jei įrenginio gamintojai ir EKA leidėjai standartą įdiegė tinkamai, EKA sistemos ir palaikymo įrenginiai gali veikti kartu, net jei prieš tai nebuvo patikrinta, kaip jie kartu veikia. **Pastaba:** OEKA palaikymas neužtikrina visų įrenginių, turinčių OEKA tvarkykles, palaikymo. „Microsoft Dynamics 365 for Retail“ pirmiausia turi palaikyti to įrenginio tipą ar klasę per OEKA. Be to, aptarnavimo objektai gali ne visada būti atnaujinti pagal naujausią CCO versiją. Dar turite žinoti, kad apskritai aptarnavimo objektų kokybė yra skirtinga.

### <a name="windows"></a>„Windows“

EKA kvitų spausdinimas optimizuotas OEKA. OEKA yra daug greitesnis nei spausdinimas per „Windows“. Todėl pravartu naudoti OEKA, ypač mažmeninėje prekyboje, kur tenka spausdinti 40 stulpelių kvitus ir operacijų tempas turi būti greitas. Su dauguma įrenginių naudosite OEKA valdiklius. Tačiau, kai kurie OEKA kvitų spausdintuvai palaiko ir „Windows“ tvarkykles. Naudodami „Windows“ tvarkyklę, galite pasiekti naujausius šriftus ir tinkle vieną spausdintuvą susieti su keliais kasos aparatais. Tačiau, yra ir „Windows“ tvarkyklių naudojimo trūkumų. Toliau pateikiami keletas trūkumų pavyzdžių:

-   Kai naudojamos „Windows“ tvarkyklės, vaizdai sugeneruojami prieš spausdinant. Todėl spausdinama lėčiau, nei su tais spausdintuvais, su kuriais naudojami OEKA valdikliai.
-   Įrenginiai, kurie yra prijungti per spausdintuvą (nuosekliąja grandine) gali netinkamai veikti, kai naudojamos „Windows“ tvarkyklės. Pvz., gali neatsidaryti kasos stalčius arba kvitų spausdintuvas gali veikti ne taip, kaip tikimasi.
-   OEKA palaiko ir platesnį kintamųjų rinkinį, kurie būdingi mažmeninės prekybos kvitų spausdintuvams, pvz., popieriaus nuplėšimas arba kvito spausdinimas.

Jei OEKA valdikliai galimi tam „Windows“ spausdintuvui, kurį naudojate, spausdintuvas vis tiek turėtų tinkamai veikti su „Microsoft Dynamics 365 for Retail“.

### <a name="universal-windows-platform"></a>„Universal Windows Platform“

Išorinių mažmeninės prekybos įrenginių atveju, UWP susieta su „Windows“ įrenginių „prijungti ir leisti“ palaikymu. Prijungus įrenginį „prijungti ir leisti“ prie „Windows“ OS, kuri palaiko to tipo įrenginį, jokios tvarkyklės nereikia norint naudoti įrenginį taip, kaip numatyta. Pvz., jei „Windows“ aptinka „Bluetooth“ garsiakalbio įrenginį, OS žino, kad šio įrenginio klasės tipas yra **Garsiakalbis**. Taigi, jį traktuoja kaip garsiakalbį. Jokių papildomų nustatymų nereikia. EKA įrenginių atveju, galima prijungti daug USB įrenginių ir „Windows“ juos atpažins kaip žmonių sąsajos įrenginius (HID). Tačiau gali būti neįmanoma nustatyti, kokias galimybes įrenginys pateikia, nes įrenginys nenurodo įrenginio klasės arba tipo. Į sistemą „Windows 10“ įtrauktos brūkšninių kodų skaitytuvų ir MSR įrenginių klasės. Taigi, jei įrenginys sistemai „Windows 10“ nurodo, kad yra kuriai nors iš šių klasių priklausantis įrenginys, „Windows“ tam tikrais laikotarpiais klausys įvykių iš šio įrenginio. „Modern POS“ palaiko UWP MSR ir skaitytuvus. Todėl, kai ji pasirengusi priimti kurio nors iš šių įrenginių įvestį, o kuriai nors iš šių klasių priklausantis įrenginys prijungiamas, šį įrenginį galima naudoti. Pvz., jei prie kompiuterio su „Windows 10“ prijungiamas UWP brūkšninio kodo skaitytuvas, o brūkšninio kodo prisijungimas „Modern POS“ sukonfigūruotas, brūkšninio kodo skaitytuvas taps aktyvus prisijungimo ekrane. Jokių papildomų nustatymų nereikia. Į sistemą „Windows“ nuolat įtraukiama papildomų elektroninio kasos aparato UWP įrenginių klasių. Šios klasės apima kasos stalčių ir kvitų spausdintuvų klases. Laukiama šių naujų įrenginių klasių palaikymo „Modern POS“.

### <a name="keyboard-wedge"></a>Klavišinis kredito kortelių skaitytuvas

Klavišinio kredito kortelių skaitytuvo įrenginiai siunčia duomenis į kompiuterį taip, tarsi šie duomenys būtų įvesti klaviatūra. Todėl, pagal numatytuosius parametrus, aktyvus EKA laukas priims nuskaitytus arba perbraukus gautus duomenis. Kai kuriais atvejais, toks būdas lemia tai, kad netinkamo tipo duomenys nuskaitomi į netinkamą lauką. Pvz., brūkšninis kodas gali būti nuskaitytas į tą lauką, kuris skirtas įvesti kredito kortelės duomenis. Daugeliu atveju EKA veikia logika, kuri nustato, ar nuskaityti arba perbraukus gauti duomenys yra brūkšninis kodas, ar perbraukimas kortele. Todėl duomenys tvarkomi tinkamai. Tačiau, kai įrenginiai nustatomi kaip OEKA, o ne klavišiniai kredito kortelių skaitytuvų įrenginiai, galima geriau kontroliuoti tai, kaip naudojami iš šių įrenginių gauti duomenys, nes daugiau „žinoma“ apie tą įrenginį, iš kurio tie duomenys gauti. Pvz., duomenys iš brūkšninio kodo skaitytuvo automatiškai atpažįstami kaip brūkšninis kodas, o susietas įrašas duomenų bazėje randamas lengviau ir greičiau, nei naudojant bendrąją eilutės iešką, kaip tai daroma naudojant klavišinius kredito kortelių skaitytuvų įrenginius.

### <a name="native-printer"></a>Vietinis spausdintuvas

Vietinius (arba „Įrenginius“, nes tipas įvardintas aparatūros šablone) spausdintuvus galima sukonfigūruoti taip, kad paragintų vartotoją pasirinkti tą spausdintuvą, kuris sukonfigūruotas tam kompiuteriui. Jei sukonfigūruotas spausdintuvas, kurios tipas **Įrenginys** , kai „Modern POS“ aptinka spausdinimo komandą, vartotojas paraginamas iš sąrašo pasirinkti spausdintuvą. Šis veikimo būdas skiriasi nuo „Windows“ tvarkyklių veikimo būdo, nes **„Windows“** spausdintuvo tipas aparatūros šablone neparodo spausdintuvų sąrašo. Šiuo būdu reikalaujama, kad lauke **Įrenginio pavadinimas** būtų nurodytas įvardytas spausdintuvas.

### <a name="windows"></a>„Windows“

Spausdintuvams naudojamas tik **„Windows“** įrenginio tipas. Kai aparatūros šablone sukonfigūruotas „Windows“ spausdintuvas, turi būti pateiktas konkretaus spausdintuvo pavadinimas. Kai „Modern POS“ aptinka spausdinimo įvykius, jei sukonfigūruotas „Windows“ spausdintuvas, įvykis bus perduotas į nurodytą „Windows“ spausdintuvą. Vartotojas nebus paragintas pasirinkti spausdintuvą.

### <a name="network"></a>Tinklas

Į tinklą adresuojamus kasos stalčius, kvitų spausdintuvus ir mokėjimo terminalus galima naudoti tinkle, arba tiesiogiai per tarpprocesinio ryšio (IPC) aparatūros stotį, kuri yra įtaisyta „Windows“ skirtoje „Modern POS“ programoje, arba per IIS aparatūros stotį, skirtą kitiems „Modern POS“ klientams.

## <a name="hardware-station-deployment-options"></a>Aparatūros stoties diegimo parinktys
### <a name="ipc-built-in"></a>IPC (įtaisytasis)

Tarpprocesinio ryšio (IPC) aparatūros stotis yra įtaisyta „Windows“ skirtoje „Modern POS“ programoje. Norėdami naudoti IPC aparatūros stotį, priskirkite aparatūros šabloną registrui, kuris naudoja „Windows“ skirtą „Modern POS“ programą. Tada parduotuvei, kurioje registras bus naudojamas, sukurkite aparatūros stotį, kurios tipas **Paskirta**. Paleidus „Modern POS“, IPC aparatūros stotis bus aktyvi, o sukonfigūruoti išoriniai EKA įrenginiai bus parengti naudoti. Jeigu laikinai dėl tam tikrų priežasčių jums nereikia vietinės aparatūros, naudodami operaciją **Tvarkyti aparatūros stotis** išjunkite aparatūros stoties galimybes. „Modern POS“ taip pat gali naudoti IPC aparatūros stotį tiesioginiam ryšiui su išoriniais tinklo įrenginiais palaikyti.

### <a name="iis"></a>IIS

IIS arba atskirą aparatūros stoties versiją galima naudoti dviem būdais. Aprašas „IIS“ reiškia, kad EKA programa prie aparatūros stoties prisijungė per „Microsoft Internet Information Services“. EKA programa prisijungia prie IIS aparatūros stoties per žiniatinklio tarnybas, vykdomas kompiuteryje, prie kurio prijungti įrenginiai. Kai naudojamos IIS, išorinius mažmeninės prekybos įrenginius, kurie prijungti prie aparatūros stoties, gali naudoti bet kuris EKA registras, esantis tame pačiame tinkle kaip ir IIS aparatūros stotis. Dėl to, kad „Windows“ skirta „Modern POS“ apima įtaisytąjį išorinių mažmeninės prekybos įrenginių palaikymą, visos kitos „Modern POS“ programos turi naudoti IIS aparatūros stotį, ryšiui užmegzti su aparatūros šablone sukonfigūruotais EKA išoriniais įrenginiais. Todėl kiekvienu atveju, kai naudojama IIS aparatūros stotis, reikalingas kompiuteris, kuriame paleista žiniatinklio tarnyba ir programa, palaikančios ryšį su įrenginiais. IIS aparatūros stotis reikalinga visoms ne „Windows“ skirtoms „Modern POS“ programoms.

#### <a name="dedicated"></a>Paskirta

„Modern POS“ naudoja aparatūros stotį, kurios tipas **Paskirta**, siekiant nustatyti, ar išoriniai įrenginiai tiesiogiai prijungti prie kompiuterio, kuriame naudojama programa. Tačiau, tipą **Paskirta** galima naudoti ir IIS aparatūros stotyse. Tradiciniame fiksuotame EKA scenarijuje, kuriame „Cloud POS“ naudojamas kaip EKA programa; aparatūros stotis, kurios tipas **Paskirta**, naudojama tame pačiame kompiuteryje, kuriame paleista „Cloud POS“, įdiegtose IIS aparatūros stotyse. Iš mažmeninės prekybos išorinių įrenginių perspektyvos, paskirtoje IIS aparatūros stotyje geriau palaikomi mažmeninės prekybos išorinių įrenginių tradiciniai fiksuoti EKA scenarijai. Paskirtos aparatūros stotys palaiko visus išorinius įrenginius, kurie palaikomi aparatūros šablone.

#### <a name="shared"></a>Bendrai naudojama

Bendrai naudojamos aparatūros stotys skirtos per dieną naudoti keliuose EKA įrenginiuose. Bendrai naudojamos aparatūros stotys optimizuotos taip, kad palaikytų tik kasos stalčius, kvitų spausdintuvus ir mokėjimo terminalus. Negalima tiesiogiai prijungti atskirų brūkšninio kodo skaitytuvų, MSR, eilutės rodymų arba kitų įrenginių. Kitu atveju, kai keli EKA įrenginiai tuo pačiu metu bandys reikalauti patvirtinti tuos išorinius įrenginius, kils nesuderinamumų. Štai kaip tvarkomi palaikomų įrenginių nesuderinamumai:

-   **Kasos stalčius** – kasos stalčius atidarytas per įvykį, kuris išsiųstas į įrenginį. Vienintelis nesuderinamumas, kuris gali įvykti iškvietus kasos stalčių, gali įvykti tada, jei kasos stalčius jau yra atidarytas. Bendrai naudojamų aparatūros stočių atveju, aparatūros šablone kasos stalčius turi būti nustatytas į **Bendrai naudojama**. Šis nustatymas neleidžia EKA tikrinti, ar kasos stalčius jau yra atidarytas, kai išsiunčia atvirą komandą.
-   **Kvitų spausdintuvas** – jei dvi kvitų spausdinimo komandos tuo pačiu metu išsiunčiamos į aparatūros stotį, atsižvelgiant į įrenginį, viena iš komandų gali būti prarasta. Kai kuriuose prietaisuose yra vidinė atmintis arba telkinys, galintis padėti išvengti šios problemos. Jei spausdinimo komanda nėra sėkminga, kasininkas gauna klaidos pranešimą ir gali iš naujo bandyti atlikti komandą iš EKA.
-   **Mokėjimo terminalas** – jei kasininkas bando užregistruoti operaciją mokėjimo terminale, kuris jau naudojamas, pranešimas informuoja kasininką, kad tuo metu terminalas naudojamas ir paprašo kasininko dar kartą bandyti vėliau. Paprastai kasininkai gali matyti, kad terminalas tuo metu jau naudojamas, ir prieš vėl bandydami užregistruoti, palaukia, kol ta operacija bus baigta.

Būsimoje laidoje planuojamas patikrinimas, siekiant nustatyti, ar nepalaikomi įrenginiai yra nustatyti aparatūros šablone, kuris susietas su bendrai naudojama aparatūros stotimi. Jei bus aptikta nepalaikomų įrenginių, vartotojas gaus pranešimą apie tai, kad tie įrenginiai nėra palaikomi bendrai naudojamose aparatūros stotyse. Bendrai naudojamų aparatūros stočių atveju, parinktis **Pasirinkti mokant** registro lygiu yra nustatyta į **Taip**. Kai operacijos mokėjimo priemonė EKA pasirinkta, EKA vartotojas paraginamas pasirinkti aparatūros stotį. Kai aparatūros stotis pasirenkama tik mokėjimo metu, aparatūros stoties pasirinkimas įtraukiamas tiesiogiai į EKA mobilių scenarijų darbo eigą. Be to, bendrai naudojamuose scenarijuose eilutės rodymas nenaudojamas mokėjimo terminale. Jei mokėjimo terminalas naudojamas kaip eilutės rodymas, kitiems vartotojams šio terminalo naudojimas gali būti užblokuotas, kol operacija bus baigta. Mobiliuosiuose scenarijuose, eilutes galima įtraukti į operaciją ilgesnį laiką. Todėl parinktis **Pasirinkti mokant** yra reikalinga, siekiant užtikrinti optimalų įrenginio pasiekiamumą.

### <a name="network-peripherals"></a>Išoriniai tinklo įrenginiai

Aparatūros šablono įrenginių tinklo priskyrimas leidžia kasos stalčius, kvitų spausdintuvus ir mokėjimo terminalus prijungti per tinklo ryšį.

#### <a name="modern-pos-for-windows"></a>„Windows“ skirta „Modern POS“

Išoriniams tinklo įrenginiams IP adresus galite nurodyti dviejose vietose. Jei „Modern POS Windows“ klientas naudoja vieną išorinių tinklo įrenginių rinkinį, tų įrenginių IP adresus turite nustatyti naudodami paties registro veiksmų srities parinktį **IP konfigūracija**. Tinklo įrenginių, kurie bendrai naudojami tarp EKA registrų, atveju, aparatūros šablonas, kuriam priskirti įrenginiai, gali būti tiesiogiai susietas su bendrai naudojama aparatūros stotimi. Norėdami priskirti IP adresus, tą aparatūros stotį pasirinkite puslapyje **Mažmeninės prekybos parduotuvės**, tada naudodami parinktį **IP konfigūracija** iš skyriaus **Aparatūros stotys** nurodykite tinklo įrenginius, kurie priskiriami tai aparatūros stočiai. Aparatūros stotyse, kurios turi tik tinklo įrenginių, jums nereikės įdiegti pačios aparatūros stoties. Tokiu atveju, aparatūros stotis reikalinga tik tam, kad konceptualiai sugrupuotų tinklui adresuojamus įrenginius pagal jų vietą mažmeninės prekybos parduotuvėje.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>„Cloud POS“, „Modern POS“ skirta „iOS“ ir „Android“ skirta „Modern POS“

Logika, pagal kurią valdomi fiziškai prijungti ir tinklui adresuojami išoriniai įrenginiai, yra aparatūros stotyje. Todėl visiems POS klientams, išskyrus „Windows“ skirtą „Modern POS“, IIS stotis turi būti įdiegta ir būti aktyvi, kad leistų užmegzti ryšį tarp EKA ir išorinių įrenginių, neatsižvelgiant į tai, ar išoriniai įrenginiai yra fiziškai prijungti prie aparatūros stoties, ar adresuojami tinkle.

## <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija
### <a name="hardware-station-installation"></a>Aparatūros stoties diegimas

Išsamesnės informacijos žr. [Mažmeninės prekybos aparatūros stoties konfigūracija ir diegimas](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>„Windows“ skirtos „Modern POS“ nustatymas ir konfigūracija

Išsamesnės informacijos žr. [„Retail Modern POS“ konfigūracija ir diegimas](retail-modern-pos-device-activation.md).

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
| Cloud POS   | Nr.                   | Taip                  |
| „Android“     | Nr.                   | Taip                  |
| „iOS“         | Nr.                   | Taip                  |

### <a name="network-peripherals"></a>Išoriniai tinklo įrenginiai

Išoriniai tinklo įrenginiai gali būti palaikomi tiesiogiai per aparatūros stotį, kuri yra įdiegta į „Windows“ skirtą „Modern POS“ programą. Visiems kitiems klientams turite įdiegti IIS aparatūros stotį.

| Klientas      | IPC aparatūros stotis | IIS aparatūros stotis |
|-------------|----------------------|----------------------|
| „Windows“ programa | Taip                  | Taip                  |
| Cloud POS   | Nr.                   | Taip                  |
| „Android“     | Nr.                   | Taip                  |
| „iOS“         | Nr.                   | Taip                  |

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
<li>Tinklas <strong>Pastaba:</strong> Tik vienas stalčius gali būti nustatytas, jei stalčiui sukonfigūruota <strong>Naudoti bendrinamą pamainą</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>2 stalčius</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas <strong>Pastaba:</strong> Tik vienas stalčius gali būti nustatytas, jei stalčiui sukonfigūruota <strong>Naudoti bendrinamą pamainą</strong>.</li>
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

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visi „Modern POS“ klientai, turintys paskirtą IIS aparatūros stotį

**Pastaba:** kai IIS aparatūros stotis yra „paskirta“, tarp POS kliento ir aparatūros stoties yra tiesioginis ryšys.

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
<li>„Windows“ tvarkyklė <strong>Pastaba:</strong> aparatūros stoties vartotojas, norėdamas pasiekti „Windows“ spausdintuvą tinkle, turi turėti leidimą spausdintuvą pasiekti.</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="even">
<td>2 spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>„Windows“ tvarkyklė</li>
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
<li>Tinklas <strong>Pastaba:</strong> viename aparatūros šablone galima nustatyti tik vieną stalčių, jei stalčiui sukonfigūruota <strong>Naudoti bendrinamą pamainą</strong>.</li>
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

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visi „Modern POS“ klientai, turintys bendrai naudojamą IIS aparatūros stotį

**Pastaba:** kai IIS aparatūros stotis yra „bendrai naudojama“, tuo pačiu metu aparatūros stotį gali naudoti keli įrenginiai. Šiame scenarijuje turite naudoti tik tuos įrenginius, kurie išvardyti toliau pateikiamoje lentelėje. Jei bandysite bendrai naudoti įrenginius, kurie čia nėra išvardyti, pvz., brūkšninių kodų skaitytuvus ir MSR, keliems įrenginiams reikalaujant patvirtinti tą patį išorinį įrenginį, įvyks klaidų. Ateityje tokios konfigūracijos bus siekiama tiesiogiai išvengti.

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
<li>„Windows“ tvarkyklė <strong>Pastaba:</strong> aparatūros stoties vartotojas, norėdamas pasiekti „Windows“ spausdintuvą tinkle, turi turėti leidimą spausdintuvą pasiekti.</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="even">
<td>2 spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>„Windows“ tvarkyklė</li>
<li>Tinklas</li>
</ul></td>
</tr>
<tr class="odd">
<td>Išdavėjas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklas <strong>Pastaba:</strong> viename aparatūros šablone galima nustatyti tik vieną stalčių, jei stalčiui sukonfigūruota <strong>Naudoti bendrinamą pamainą</strong>.</li>
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
Išsamesnės informacijos apie tai, kaip kurti aparatūros šablonus, žr. [Apibrėžti ir prižiūrėti kanalų klientus, įskaitant registrus ir aparatūros stotis](define-maintain-channel-clients-registers-hw-stations.md). **Pastaba:** „Microsoft Dynamics 365 for Retail“ 1611 versijoje aparatūros stoties profilis nebenaudojamas. Atributai, kuriuos anksčiau nustatėte aparatūros stoties šablone, dabar yra pačios aparatūros stoties dalis.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>„Windows“ skirta „Modern POS“ su IPC (įtaisyta) aparatūros stotimi

Ši konfigūracija yra labiausiai įprasta tradicinių fiksuotų EKA registrų konfigūracija. Šiame scenarijuje aparatūros šablono informacija tiesiogiai susiejama su pačiu EKA registru. EFT terminalo numeris taip pat turi būti nustatytas pačiame registre. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurkite aparatūros šabloną, kur konfigūruojami visi reikiami išoriniai įrenginiai.
2.  Susiekite aparatūros šabloną su EKA registru.
3.  Sukurkite aparatūros stotį, kurios tipas **Paskirta**, mažmeninės prekybos parduotuvei, kurioje bus naudojamas EKA registras. Aprašas nėra būtinas. **Pastaba:** aparatūros stotyje neprivalote nustatyti jokių kitų ypatybių. Visa kita reikiama informacija, pvz., aparatūros šablonas, bus gauta iš paties registro.
4.  Spustelėkite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
5.  Pasirinkite paskirstymo grafiką **1090** norėdami sinchronizuoti naują parduotuvės aparatūros šabloną. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
6.  Pasirinkite paskirstymo grafiką **1040** norėdami sinchronizuoti naują parduotuvės aparatūros stotį. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
7.  Įdiekite ir suaktyvinkite „Windows“ skirtą „Modern POS“.
8.  Paleiskite „Windows“ skirtą „Modern POS“ ir pradėkite naudoti prijungtus išorinius įrenginius.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visi „Modern POS“ klientai, turintys paskirtą IIS aparatūros stotį

Šią konfigūraciją galima naudoti visiems „Modern POS“ klientams, kurie turi aparatūros stotį, išskirtinai naudojamą vieno EKA registro. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurkite aparatūros šabloną, kur konfigūruojami visi reikiami išoriniai įrenginiai.
2.  Sukurkite aparatūros stotį, kurios tipas **Paskirta**, mažmeninės prekybos parduotuvei, kurioje bus naudojamas EKA registras.
3.  Paskirtoje aparatūros stotyje nustatykite šias ypatybes:
    -   **Pagrindinio kompiuterio vardas** – pagrindinio kompiuterio, kuriame bus vykdoma aparatūros stotis, pavadinimas. **Pastaba:** „Cloud POS“ gali pašalinti **vietinis pagrindinis kompiuteris** siekiant nustatyti vietinį kompiuterį, kuriame vykdoma „Cloud POS“. Tačiau sertifikato, kurio reikia norint susieti „Cloud POS“ su aparatūros stotimi, kompiuterio vardas turi būti „Vietinis pagrindinis kompiuteris“. Siekiant išvengti problemų, rekomenduojame išvardyti kiekvienos parduotuvei paskirtos aparatūros stoties atvejį, kaip reikalaujama. Kiekvienos aparatūros stoties pagrindinio kompiuterio pavadinimas turi būti to kompiuterio, kuriame bus įdiegta aparatūros stotis, pavadinimas.
    -   **Prievadas** – aparatūros stoties ir „Modern POS“ kliento ryšiui palaikyti naudojamas prievadas.
    -   **Aparatūros šablonas** – jei aparatūros šablonas nepateikiamas pačioje aparatūros stotyje, bus naudojamas registrui priskirtas aparatūros šablonas.
    -   **EFT EKA numeris** – EFT terminalo ID, naudojamas, kai siunčiami EFT įgaliojimai. Šį ID pateikia kredito kortelių procesorius.
    -   **Paketo pavadinimas** – aparatūros stoties paketas, naudojamas įdiegiant aparatūros stotį.

4.  Spustelėkite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
5.  Pasirinkite paskirstymo grafiką **1090** norėdami sinchronizuoti naują parduotuvės aparatūros šabloną. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
6.  Pasirinkite paskirstymo grafiką **1040** norėdami sinchronizuoti naują parduotuvės aparatūros stotį. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
7.  Įdiekite aparatūros stotį. Išsamesnės informacijos apie tai, kaip įdiegti aparatūros stotį, žr. [Mažmeninės prekybos aparatūros stoties konfigūracija ir diegimas](retail-hardware-station-configuration-installation.md).
8.  Įdiekite ir suaktyvinkite „Modern POS“. Išsamesnės informacijos apie tai, kaip įdiegti „Modern POS“, žr. [„Retail Modern POS“ konfigūracija ir diegimas](retail-modern-pos-device-activation.md).
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
2.  Sukurkite **Bendrai naudojama** tipo aparatūros stotį mažmeninės prekybos parduotuvei, kurioje bus naudojamas EKA registras.
3.  Bendrai naudojamoje aparatūros stotyje nustatykite šias ypatybes:
    -   **Pagrindinio kompiuterio vardas** – pagrindinio kompiuterio, kuriame bus vykdoma aparatūros stotis, pavadinimas.
    -   **Aprašas** – tekstas, kuris padės identifikuoti aparatūros stotį, pvz., **Grąžinimai** arba **Parduotuvės pagrindinė**.
    -   **Prievadas** – aparatūros stoties ir „Modern POS“ kliento ryšiui palaikyti naudojamas prievadas.
    -   **Aparatūros šablonas** – kiekviena bendrai naudojama aparatūros stotis turi turėti aparatūros šabloną. Aparatūros šablonus gali bendrai naudoti aparatūros stotys, bet jie turi būti susieti su kiekviena aparatūros stotimi. Be to, rekomenduojame naudoti bendrai naudojamas pamainas, kai tą pačią aparatūros stotį naudoja keli įrenginiai. Norėdami nustatyti bendrai naudojamą pamainą, spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**. Kiekviename bendrai naudojamame aparatūros šablone pasirinkite kasos stalčių ir nustatykite parinktį **Bendrinamas pamainos stalčius** į **Taip**.
    -   **EFT EKA numeris** – EFT terminalo ID, naudojamas, kai siunčiami EFT įgaliojimai. Šį ID pateikia kredito kortelių procesorius.
    -   **Paketo pavadinimas** – aparatūros stoties paketas, naudojamas įdiegiant aparatūros stotį.

4.  Pakartokite 2 ir 3 veiksmus kiekvienai papildomai aparatūros stočiai, kuri reikalinga parduotuvėje.
5.  Spustelėkite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
6.  Pasirinkite paskirstymo grafiką **1090** norėdami sinchronizuoti naują parduotuvės aparatūros šabloną. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
7.  Pasirinkite paskirstymo grafiką **1040** norėdami sinchronizuoti naują parduotuvės aparatūros stotį. Spustelėję **Vykdyti dabar** sinchronizuokite EKA pakeitimus.
8.  Aparatūros stotį įdiekite kiekviename pagrindiniame kompiuteryje, kuriuos nustatėte atlikdami 2 ir 3 veiksmus. Išsamesnės informacijos apie tai, kaip įdiegti aparatūros stotį, žr. [Mažmeninės prekybos aparatūros stoties konfigūracija ir diegimas](retail-hardware-station-configuration-installation.md).
9.  Įdiekite ir suaktyvinkite „Modern POS“. Išsamesnės informacijos apie tai, kaip įdiegti „Modern POS“, žr. [„Retail Modern POS“ konfigūracija ir diegimas](retail-modern-pos-device-activation.md).
10. Prisijunkite prie „Modern POS“ ir pasirinkite **Atlikti su stalčiumi nesusijusią operaciją**.
11. Pradėkite operaciją **Tvarkyti aparatūros stotis**.

12. Spustelėkite **Tvarkyti**.
13. Aparatūros stoties tvarkymo puslapyje nustatykite aparatūros stoties įjungimo parinktį.
14. Pasirinkite naudojamą aparatūros stotį, tada spustelėkite **Susieti**.
15. Pakartokite 14 veiksmą kiekvienai aparatūros stočiai, kurią naudos „Modern POS“.
16. Kai visos reikalingos aparatūros stotys susietos, spustelėkite **Uždaryti**.
17. Aparatūros stoties pasirinkimo puslapyje spustelėję ką tik pasirinktą aparatūros stotį, ją suaktyvinsite. **Pastaba:** jei įrenginiai dažnai naudoja skirtingas aparatūros stotis, rekomenduojame taip sukonfigūruoti „Modern POS“, kad paragintų kasininkus pradedant mokėjimo procesą, pasirinkti aparatūros stotį. Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Registrai**. Pasirinkite registrą, tada nustatykite parinktį **Pasirinkti mokant** į **Taip**. Naudodami paskirstymo grafiką **1090** sinchronizuokite kanalo duomenų bazės pakeitimus.

## <a name="extensibility"></a>Išplečiamumas
Išsamesnės informacijos apie aparatūros stoties išplėtimo scenarjus, žr. [Aparatūros stoties išplėtimas](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Sauga
Pagal dabartinius saugos standartus, gamybos aplinkoje turi būti naudojami šie nustatymai: **Pastaba:** aparatūros stoties diegimo programa automatiškai atliks šiuos registro redagavimus kaip savitarnos diegimo dalį.

-   Saugiųjų jungčių lygmenį (SSL) reikia išjungti.
-   Įjungta ir naudojama turi būti tik transportavimo lygmens saugos (TLS) 1.2 versija (arba naujausia dabartinė versija). **Pastaba:** pagal numatytuosius parametrus išjungtas SSL ir visos TLS versijos, išskyrus 1.2 versiją. Norėdami redaguoti ar įgalinti šias vertes, atlikite šiuos veiksmus:
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

**Pastaba:** labai svarbu peržiūrėti IIS ir mokėjimo kortelių pramonės (PCI) reikalavimų saugos gaires.

## <a name="peripheral-simulator"></a>Periferinis simuliatorius
Išsamesnės informacijos žr. [Mažmeninės prekybos periferinis simuliatorius](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>„Microsoft“ išbandyti išoriniai įrenginiai
### <a name="ipc-built-in-hardware-station"></a>IPC (įtaisytoji) aparatūros stotis

Toliau nurodyti išoriniai įrenginiai buvo išbandyti naudojant IPC aparatūros stotį, kuri yra įtaisyta „Windows“ skirtoje „Modern POS“.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                |
|--------------|----------|-----------|-------------------------|
| „Epson“        | Tm-T88IV | OEKA      |                         |
| „Epson“        | TM-T88V  | OEKA      |                         |
| „Star“         | TSP650II | OEKA      |                         |
| „Star“         | TSP650II | Pasirinktinai    | Prijungtas per tinklą   |
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
| „APG“          | „Atwood“    | Pasirinktinai    | Prijungtas per tinklą   |
| „Star“         | SMD2-1317 | OEKA      |                         |
| „HP“           | QT457AA   | OEKA      |                         |

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
| „Star“         | TSP650II | OEKA      |                           |
| „Star“         | TSP650II | Pasirinktinai    | Prijungtas per tinklą     |
| „Star“         | TSP100   | OEKA      | Reikia TSP650II tvarkyklių |
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
| „APG“          | „Atwood“    | Pasirinktinai    | Prijungtas per tinklą |
| „Star“         | SMD2-1317 | OEKA      |                       |
| „HP“           | QT457AA   | OEKA      |                       |

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

Toliau nurodyti išoriniai įrenginiai buvo išbandyti naudojant bendrinamą IIS aparatūros stotį kartu su „Windows“ skirta „Modern POS“ ir „Cloud POS“. **Pastaba:** palaikomas tik spausdintuvas, mokėjimo terminalas ir kasos stalčius.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                  |
|--------------|----------|-----------|---------------------------|
| „Epson“        | Tm-T88IV | OEKA      |                           |
| „Epson“        | TM-T88V  | OEKA      |                           |
| „Star“         | TSP650II | OEKA      |                           |
| „Star“         | TSP650II | Pasirinktinai    | Prijungtas per tinklą     |
| „Star“         | TSP100   | OEKA      | Reikia TSP650II tvarkyklių |
| „HP“           | F7M67AA  | OEKA      | Teikiamas USB               |

#### <a name="payment-terminal"></a>Mokėjimo terminalas

| Gamintojas | Modelis | Sąsaja | Komentarai                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| „VeriFone“     | MX925 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |
| „VeriFone“     | MX915 | Pasirinktinai    | Reikia mokėjimo jungties tinkinimo; prijungiamas per tinklą ir USB |

#### <a name="cash-drawer"></a>Kasos stalčius

| Gamintojas | Modelis     | Sąsaja | Komentarai              |
|--------------|-----------|-----------|-----------------------|
| „APG“          | „Atwood“    | Pasirinktinai    | Prijungtas per tinklą |
| „Star“         | SMD2-1317 | OEKA      |                       |
| „HP“           | QT457AA   | OEKA      |                       |

## <a name="troubleshooting"></a>Trikčių šalinimas
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>„Modern POS“ gali pasirinkimo sąraše aptikti aparatūros stotį, bet negali atlikti susiejimo

**Sprendimas:** patikrinkite toliau pateikiamą galimų trikčių punktų sąrašą:

-   Kompiuteris, kuris vykdo „Modern POS“, pasitiki tuo sertifikatu, kuris naudojamas aparatūros stotį vykdančiame kompiuteryje.
    -   Norint patikrinti šį nustatymą, žiniatinklio naršyklėje eikite šiuo URL: https://&lt;Kompiuterio pavadinimas&gt;:&lt;Prievado numeris&gt;/HardwareStation/ping.
    -   Šiame URL naudojama ryšio užklausa, siekiant patikrinti, ar kompiuterį galima pasiekti, o naršyklė nurodo, ar sertifikatas patikimas. (Pvz., „Internet Explorer“ adreso juostoje pasirodo spynos piktograma. Spustelėjus šią piktogramą, „Internet Explorer“ patikrina, ar dabar naudojamas sertifikatas patikimas. Vietiniame kompiuteryje sertifikatą galite įdiegti peržiūrėję rodomo sertifikato informaciją.)
-   Aparatūros stotį vykdančiame kompiuteryje prievadas, kuris bus naudojamas aparatūros stotyje, atidaromas užkardoje.
-   Aparatūros stotis tinkamai įdiegė prekybininko sąskaitos informaciją naudojant įrankį Įdiegti prekybininko informaciją, kuris vykdomas aparatūros stoties diegimo programos pabaigoje.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>„Modern POS“ negali pasirinkimo sąraše aptikti aparatūros stoties

**Sprendimas:** šią problemą sukelti gali bet kuris iš šių veiksnių:

-   Aparatūros stotis būstinėje buvo nustatyta netinkamai. Atlikę anksčiau šioje temoje nurodytus veiksmus, patikrinkite, ar tinkamai įvestas aparatūros stoties šablonas ir aparatūros stotis.
-   Nebuvo įvykdytos kanalo konfigūracijos atnaujinimo užduotys. Tokiu atveju vykdykite kanalo konfigūracijos 1070 užduotį.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>„Modern POS“ neatspindi naujų kasos stalčiaus nustatymų

**Sprendimas:** uždarykite dabartinį paketą. Kasos stalčiaus pakeitimai nebus atnaujinti „Modern POS“ tol, kol nebus uždarytas dabartinis paketas.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>„Modern POS“ pateikia ataskaitą apie problemą su mažmeninės prekybos išoriniu įrenginiu

**Sprendimas:** toliau nurodytos kai kurios tipinės šios problemos priežastys:

-   Įsitikinkite, kad uždarytos kitos įrenginių tvarkyklių konfigūravimo priemonės. Jei šios priemonės atidarytos, jos gali neleisti „Modern POS“ arba aparatūros stočiai patvirtinti įrenginį.
-   Jei išorinis mažmeninės prekybos įrenginys bendrinamas su keliais EKA įrenginiais, įsitikinkite, kad jis priklauso vienai iš šių kategorijų:
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


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Mažmeninės prekybos periferinis simuliatorius](dev-itpro/retail-peripheral-simulator.md)




