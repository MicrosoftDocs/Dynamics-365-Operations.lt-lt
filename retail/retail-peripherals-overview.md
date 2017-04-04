---
title: "Mažmeninės prekybos periferinių įrenginių apžvalga"
description: "Šioje temoje paaiškinama sąvokos, kurios yra susiję su mažmeninės prekybos periferiniai įrenginiai. Jame aprašoma įvairių būdų, kaip kad periferinius įrenginius galima prijungti prie pardavimo (POS) ir komponentai, yra atsakinga už ryšį su POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Mažmeninės prekybos periferinių įrenginių apžvalga

Šioje temoje paaiškinama sąvokos, kurios yra susiję su mažmeninės prekybos periferiniai įrenginiai. Jame aprašoma įvairių būdų, kaip kad periferinius įrenginius galima prijungti prie pardavimo (POS) ir komponentai, yra atsakinga už ryšį su POS.

<a name="concepts"></a>Koncepcijos
--------

### <a name="pos-registers"></a>EKA registrai

Navigacija: Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**registrų**. Pardavimo (PV) registras yra subjektas, kuris yra naudojamas nustatyti konkrečiu atveju į gamintojų organizacijų ypatybes. Šios savybės apima aparatūros profilis arba sąrankos mažmeninės prekybos periferiniai įrenginiai, kurie bus naudojami registrą, kuris registre yra susietas su parduotuvės ir regėjimo patirtį, kad vartotojas, kuris prisijungia prie tame registre.

### <a name="devices"></a>Įrenginiai

Navigacija: Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**įrenginiai**. Įrenginys yra objektas, nurodantis su EKA registru susieto įrenginio fizinį egzempliorių. Kai įtaisas, jis yra susietas su POS registrą. Įrenginio objektas seka informaciją apie POS registro suaktyvinimo laiką, naudojamo kliento tipą ir programų paketą, kuris buvo įdiegtas konkrečiame įrenginyje. Įrenginiai gali būti atvaizduota šios paraiškos tipai: mažmeninės prekybos šiuolaikinės EKA, Retail POS debesis, mažmeninės prekybos šiuolaikinės EKA – Windows Phone, mažmeninės prekybos šiuolaikinės EKA – "Android" ir mažmeninės prekybos šiuolaikinės EKA – "iOS".

### <a name="retail-modern-pos"></a>„Retail Modern POS“

Šiuolaikinės EKA yra POS programa, skirta Microsoft Windows. Ji gali būti įdiegta "Windows 10" operacinėje sistemoje (OSs).

### <a name="cloud-pos"></a>Cloud POS

POS debesiui šiuolaikinės EKA programos, pasiekiama interneto naršyklėje naršyklės versija.

### <a name="modern-pos-for-ios"></a>Šiuolaikinės POS, skirta "iOS"

Šiuolaikinės POS, skirta "iOS" yra iOS pagrindu versija šiuolaikinės POS programa, kuri gali būti įdiegta "iOS" įrenginiuose.

### <a name="modern-pos-for-android"></a>Šiuolaikinės POS, "Android"

Šiuolaikinės EKA "Android" yra "Android" pagrindu versija šiuolaikinės POS programa, kuri gali būti įdiegta "Android" įrenginiuose.

### <a name="pos-peripherals"></a>POS periferiniai įrenginiai

POS periferiniai įrenginiai yra įrenginiai, kurie aiškiai pasisakė už POS funkcijas. Šie išoriniai įrenginiai paprastai yra skirstomi į specialius kursus. Daugiau informacijos apie šios klasės, rasite šios temos skyriuje "Įrenginio klasės".

### <a name="hardware-station"></a>Aparatūros stotis

Navigacija: Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalai**&gt;**mažmeninės prekybos parduotuvėse**&gt;**visi mažmeninės prekybos parduotuvėse**. Pasirinkite parduotuvę, tada spustelėkite „FastTab“ **Aparatūros stotys**. Į **aparatūrą stotis** aplinkoje yra kanalo lygmens parametras, kuris yra naudojamas apibrėžti atvejai, kai bus dislokuotos mažmeninės prekybos periferinių logika. Šis parametras lygiu kanalas naudojamas nustatyti aparatūros stoties charakteristikos. Jis taip pat naudojamas sąrašas aparatūros stotys, skirtos šiuolaikinės EKA instancijos konkrečioje parduotuvėje. Aparatūros stotis pastatyta į šiuolaikinės EKA programos "Windows". Aparatūros stotis gali būti naudojami savarankiškai kaip atskira "Microsoft" interneto informacijos paslaugas (IIS) programa. Šiuo atveju, ji gali būti prieinama per tinklą.

### <a name="hardware-profile"></a>Aparatūros šablonas

Navigacija: Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros profiliai**. Aparatūros profilis yra sąrašą įrenginių, kurie sukonfigūruoti POS registrą arba aparatūros stoties. Techninės įrangos profilį galite susieti tiesiogiai su POS registrą ar aparatūros stotis.

## <a name="devices-classes"></a>Įrenginių klasių
POS periferiniai įrenginiai paprastai skirstomi į klases. Šiame skyriuje aprašoma ir apžvelgiamos šiuolaikinės EKA palaiko įrenginiai.

### <a name="printer"></a>Spausdintuvas

Spausdintuvai yra tradicinis POS gavimo spausdintuvai ir viso puslapio spausdintuvai. Spausdintuvas palaiko per objektų susiejimo ir įterpties mažmeninės prekybos EKA (OEKA) ir Microsoft Windows tvarkyklės sąsajos. Iki dviejų spausdintuvai gali būti naudojamas vienu metu. Šią funkciją palaiko scenarijų, kai cash-and-carry pirkėjo kvitus spausdinamas gavimo spausdintuvai, kadangi klientų užsakymus, kurie veža daugiau informacijos, yra nurodyti ant viso puslapio spausdintuvą. Gavimo spausdintuvai gali prijungti tiesiogiai prie kompiuterio per USB, per Ethernet tinkle arba prijungtas "Bluetooth" ryšiu.

### <a name="scanner"></a>Skaitytuvas

Iki dviejų brūkšninių kodų skaitytuvai gali būti naudojamas vienu metu. Šią funkciją palaiko scenarijų, kur skaitytuvo, kuris yra daugiau mobiliųjų būtina norint nuskaityti didelės arba sunkiųjų elementų, kadangi ilgalaikio įdėtasis skaitytuvo vartojamas daugelyje standartinio dydžio elementus, pagreitinti kasos kartus. Skaitytuvai gali būti remiami OEKA, universalios Windows platformos (UWP) arba klaviatūra pleišto sąsajas. USB arba "Bluetooth" gali būti naudojamas prijungti skaitytuvą prie kompiuterio.

### <a name="msr"></a>MSR

Vienas USB magnetine juostele skaitytojas (MSR) galite nustatyti naudodami OPOS vairuotojai. Jei norite naudoti atskiras MSR elektroninių pinigų pervedimas (EFT) mokėjimo operacijoms, MSR turi valdyti mokėjimo jungtį. Atskiras MSRs galima klientų lojalumo įrašas, darbuotojo prisijungimo, ir dovanų kortelės įrašo, neatsižvelgiant į mokėjimo jungtis.

### <a name="cash-drawer"></a>Pinigų stalčius

Dvi pinigų stalčiai gali būti remiamos už aparatūros profilyje. Ši galimybė leidžia dvi aktyvios pamainomis per registrą galima tuo pačiu metu. Tuo atveju, kai bendra pamainą arba kasos stalčiaus, kurį naudoja kelis mobiliojo POS prietaisai vienu metu, tik viena pinigų stalčius yra leidžiami aparatūros profilis. Pinigų stalčiai gali prijungtas tiesiogiai prie kompiuterio per USB, prijungtas prie tinklo arba prisijungę prie gavimo spausdintuvo per RJ12 sąsają. Kai kuriais atvejais pinigų stalčiai taip pat gali būti prijungtas per "Bluetooth".

### <a name="line-display"></a>Eilutės rodymas

Parodyti produktus, operacijų balansus ir kita naudinga informacija klientui operacijos metu naudojami eilutėje rodomas. Vienos eilutės ekranas gali būti prijungtas prie kompiuterio per USB naudojant OPOS vairuotojai.

### <a name="signature-capture"></a>Parašo fiksavimas

Parašas surinkimo prietaisai gali būti prijungtas tiesiogiai prie kompiuterio per USB naudojant OPOS vairuotojai. Sukonfigūravus parašas surinkimo, klientas yra raginami prisijungti įrenginyje. Po pasirašymo, ji rodoma prie kasos priimti.

### <a name="scale"></a>Mastelis

Svarstyklės gali būti prijungtas prie kompiuterio per USP naudojant OPOS vairuotojai. Kai produktas, kuris yra pažymėtas kaip "Weighed" produktas yra įtrauktas į sandorį, Go skaito svorio skalė, prideda produkto sandorio ir naudoja kiekį, kad skalė.

### <a name="pin-pad"></a>PIN rinkiklis

Asmeninio identifikavimo numerio (PIN) trinkelės sustiprina OEKA, tačiau jie turi būti tvarkomi per mokėjimo jungtį.

### <a name="secondary-display"></a>Antrinis ekranas

Kai ekranas yra sukonfigūruotas, skaičiumi "2" "Windows" rodymo naudojamas norint parodyti pagrindinę informaciją. Antrinis ekranas tikslas remti nepriklausomas programinės įrangos tiekėjas (ISV) pratęsimo, nes out of the box, antrinis ekranas yra ne konfigūruojama ir rodo ribotą kiekį.

### <a name="payment-device"></a>Mokėjimo įrenginys

Mokėjimo įrenginių palaikymas yra įgyvendinama per mokėjimo jungtis. Mokėjimų prietaisai gali atlikti vieną ar daugelį funkcijų, kurias kiti įrenginio klasės numatyti. Pvz., mokėjimo įrenginį gali veikti kaip MSR/kortelių skaitytuvas, eilutės ekranas, parašo įrašymo įrenginiu, arba PIN pad. Parama mokėjimų prietaisai yra atliktas nepriklausomai nuo atskirų įrenginių palaikymas, tai yra numatyta kituose įrenginiuose, kurie yra įtraukti į aparatūros profilis.

## <a name="supported-interfaces"></a>Palaikomas sąsajos
### <a name="opos"></a>OEKA

Kad būtų užtikrinta, kad didžiausią asortimentą įrenginių galima naudojant Microsoft Dynamics 365 operacijų - mažmeninės prekybos, OLE POS pramonės standartas yra pagrindinis mažmeninių periferinių įrenginių platformą, kuri palaiko Microsoft Dynamics 365 operacijų - mažmeninės prekybos. OLE, POS standartas buvo pagamintas iš nacionalinių mažmeninės prekybos federacija (NGRP), kuris nustato standartines komunikacijos protokolų mažmeninės prekybos periferinių įrenginių. OEKA yra plačiai taikomą OLE POS standartui įgyvendinti. Ji buvo sukurta 1990 m. Vidurio ir buvo atnaujinta keletą kartų nuo tada. OEKA numatyta įrenginio tvarkyklės architektūra, kuri leidžia lengvai integruoti POS aparatūros su Windows-pagrindu POS sistemas. OEKA kontroliuoja rankena suderinamos aparatūros ir POS terminalų programinė įranga bendravimą. OEKA control susideda iš dviejų dalių:

-   **Objektui Control** – objekto valdymo įrenginio klasės (pvz., eilutėje rodomas) numatyta sąsaja programinės įrangos programa. Monroe konsultavimo paslaugas ([www.monroecs.com](http://www.monroecs.com/)) suteikia standartizuotas OEKA kontrolės objektus, kurie yra žinomi kaip bendros kontrolės objektai (CCOs). Į CCOs yra naudojami išbandyti Microsoft Dynamics 365 operacijų - Retail POS komponentas. Todėl bandymai padeda užtikrinti, kad Microsoft Dynamics 365 operacijų - mažmeninės prekybos palaiko įrenginio klasė per OEKA, daugelis įrenginių tipų gali būti palaikomas, jeigu gamintojas pateikia paslaugų objektą, kuris yra pastatytas OEKA. Jūs neturite aiškiai išbandyti kiekvieną įrenginio tipą.
-   **Aptarnavimo objekto** – aptarnavimo objekto teikia bendravimas tarp valdymo objektų (CCO) ir įrenginio. Paprastai, aptarnavimo objekto įrenginio teikia į įrenginio gamintoją. Tačiau, kai kuriais atvejais, jums gali tekti aptarnavimo objekto atsisiųsti iš gamintojo svetainės. Pavyzdžiui, neseniai aptarnavimo objektą galima atsisiųsti. Norėdami rasti gamintojo svetainės adresą, ieškokite aparatūros dokumentacijoje.

[![Kontrolės objektas ir aptarnavimo objekto](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) parama OEKA įgyvendinant OLE POS padeda užtikrinti, kad, jei įrenginio gamintojo ir POS leidėjų tinkamai įgyvendinti standarto, POS sistemos, bei palaikantys įrenginiai gali dirbti kartu, net jei jie anksčiau nebuvo tiriami kartu. **Pastaba:** OEKA paramos negarantuoja paramą visiems prietaisams, kurie turi OPOS vairuotojai. Microsoft Dynamics 365 operacijų - mažmeninės prekybos pirmiausia turi palaikyti šio prietaiso tipo ar klasės, per OEKA. Be to, paslaugų objektai ne visada gali būti atnaujinti į naujausią versiją, kad CCOs. Jums taip pat reikėtų žinoti, kad, apskritai, paslaugų objektų kokybė skiriasi.

### <a name="windows"></a>„Windows“

Kvitams spausdinti EKA yra optimizuota OEKA. OEKA linkęs būti daug greičiau nei spausdinimas per langus. Taigi, tai gera idėja naudoti OEKA, ypač mažmeninės prekybos aplinkoje, kur 40 stulpelių kvitai spausdinami ir operacijos turi būti greitas. Daugumai prietaisų, jūs naudojate OEKA kontrolę. Vis dėlto kai kurie OEKA gavimo spausdintuvai taip pat palaiko Windows tvarkykles. Naudojant "Windows" tvarkyklę, galite pasiekti naujausią šriftus ir vieną spausdintuvą, keliuose kasos aparatuose. Tačiau yra trūkumų naudojant "Windows" tvarkyklių. Štai keletas pavyzdžių iš šių trūkumų:

-   Naudojant "Windows" tvarkyklių, vaizdai yra teikiamos prieš spausdinimą. Todėl, spausdinant linkęs būti lėtesnis nei yra apie spausdintuvus, kurie naudoja OEKA kontrolę.
-   Prietaisus, prijungtus per ("ramunės-grandinės") spausdintuvas gali veikti netinkamai kai naudojamos "Windows" tvarkyklių. Pvz., kasos stalčiaus, gali neatsidaryti arba kvito spausdintuvas gali ne žodžio, kaip tikėjotės.
-   OEKA taip pat palaiko didesnę rinkinį kintamųjų, kurie yra būdingi mažmeninės prekybos gavimo spausdintuvai, pvz., popieriaus pjaustymo arba važtaraščio spausdinimas.

Jei OEKA kontrolė yra prieinama "Windows" spausdintuvo, kurį naudojate, spausdintuvas vis tiek turėtų veikti tinkamai naudojant Microsoft Dynamics 365 operacijų - mažmeninės prekybos.

### <a name="universal-windows-platform"></a>Universalus Windows platforma

UWP, tais atvejais, kai mažmeninės prekybos periferinę įrangą, yra susijusi su Windows palaikymą Plug and Play įrenginiai. Prisijungus prie "Windows" OS versijos, kuri palaiko tam įtaiso tipui, Plug and Play įrenginį be vairuotojo reikalingas prietaisas gali būti naudojamas pagal paskirtį. Pavyzdžiui, jei "Windows" aptinka "Bluetooth" garsiakalbis įrenginys, OS žino kad prietaisas turi ir **garsiakalbis** klasės tipo. Todėl ir ji gydo tą įrenginį kaip kalbėtojas. Nereikia jokių papildomų nustatymų. POS prietaisai, daugelis USB įrenginių gali būti prijungti, ir "Windows" atpažins jas kaip žmogaus sąsajos įrenginių (HIDs). Tačiau ji gali būti gali nustatyti pajėgumus, užtikrina prietaiso, nes prietaisas nėra nurodyti klasės ar rūšies įrenginiai. "Windows 10", buvo pridėta įrenginio klasės brūkšninių kodų skaitytuvai ir MSRs. Todėl, jei įrenginys pareiškia, kad į "Windows 10" kaip vieną iš šių klasių įrenginį, Windows bus išgirsti renginių nuo prietaiso reikiamu laiku. Šiuolaikinės EKA palaiko UWP MSRs ir skeneriai. Todėl, kai jis yra paruoštas iš vieno iš šių įrenginių, ir prijungtas įtaisas, kuris priklauso vienai iš šių klasių, prietaisas gali būti naudojamas. Pavyzdžiui, jei UWP brūkšninių kodų skaitytuvas yra prijungtas prie kompiuterio su "Windows 10", ir brūkšninį kodą prisijungdami sukonfigūruotas šiuolaikinės EKA, brūkšninių kodų skaitytuvo taps aktyvi prisijungimo ekrane. Nereikia jokių papildomų nustatymų. Taško paslaugos UWP prietaisų klases yra pridedama prie "Windows". Šios klasės yra klasės pinigų stalčiai ir gavimo spausdintuvai. Šių naujų įrenginių klasių Šiuolaikinės pos parama yra laukiama.

### <a name="keyboard-wedge"></a>Klaviatūros pleišto

Klaviatūros pleišto įrenginių siųsti duomenis į kompiuterį, jei tie duomenys buvo atspausdintos ant klaviatūros. Todėl, pagal numatytuosius nustatymus, lauką, kuriame yra aktyvūs Go gaus duomenis, kurie yra nuskaitomi arba swiped. Kai kuriais atvejais, šią problemą gali sukelti netinkamo tipo duomenis nuskaityti į neteisingas lauko. Pvz., į lauką, kuris yra skirtas kredito kortelės duomenų įvedimą gali nuskaityti brūkšninį kodą. Daugeliu atvejų, gamintojų organizacijoms, kurios nustato, ar duomenis, kurie yra nuskaitomi arba swiped brūkšninį kodą ar kortelės perbraukimas yra logika. Todėl, kad duomenys būtų tvarkomi teisingai. Tačiau, kai įrenginiai yra nustatytas kaip OEKA vietoj klaviatūros pleišto įrenginiai, yra labiau kontroliuoti, kaip duomenis iš šių įrenginių gali būti vartojamas, nes daugiau "žinoma" apie prietaisą, kad duomenys yra kilęs iš. Pvz., duomenis iš brūkšninių kodų skaitytuvas yra automatiškai pripažįstamas brūkšninį kodą, ir susijęs įrašas duomenų bazėje rasti lengviau ir greičiau nei jei bendrasis eilutės paieška buvo naudojami kaip klaviatūra pleišto įrenginių atveju.

### <a name="native-printer"></a>Gimtoji spausdintuvas

Gimtoji (arba "Device" kaip tipas pavadintas aparatūros profilyje) spausdintuvai gali būti konfigūruojamas raginti vartotoją pasirinkti spausdintuvą, kuris yra sukonfigūruotas naudoti kompiuterį. Kai spausdintuvą, su **prietaiso** tipo yra sukonfigūruotas, jei šiuolaikinės EKA susiduria su spausdinimo komandą, kad vartotojas paraginamas pasirinkti spausdintuvą sąraše. Taip skiriasi nuo elgesį Windows tvarkykles, nes į **Windows** spausdintuvo tipo aparatūros profilyje nerodo spausdintuvų sąrašas. Vietoj to, jis reikalauja pateikti pavadintas spausdintuvą kad **įrenginio pavadinimas** srityje.

### <a name="windows"></a>„Windows“

Į **Windows** prietaiso tipas yra naudojamas tik spausdintuvai. Kai spausdintuvą, Windows yra sukonfigūruotas naudojant aparatūros šabloną, reikia pateikti konkrečių spausdintuvo pavadinimą. Kai šiuolaikinės EKA susiduria spausdinimo įvykius, jei spausdintuvą, Windows yra sukonfigūruotas, renginys bus perduoti į nurodytą "Windows" spausdintuvas. Vartotojas nebus būsite paraginti pasirinkti spausdintuvą.

### <a name="network"></a>Tinklas

Tinklo adresavimo pinigų stalčiai, gavimas spausdintuvai ir mokėjimo terminalai gali būti naudojamas tinkle, tiesiogiai Interprocess komunikacijos (IPC) aparatūros stotis, kuri yra įmontuota į šiuolaikinės POS for Windows programa ar IIS aparatūros stoties kitų šiuolaikinės EKA klientams.

## <a name="hardware-station-deployment-options"></a>Aparatūros stoties diegimo parinktys
### <a name="ipc-built-in"></a>IPC (vidinis)

Interprocess komunikacijos (IPC) aparatūros stotis pastatyta į šiuolaikinės POS for Windows programa. Naudoti IPC aparatūros stotis, aparatūros šabloną priskirti registrą, kuri bus naudojama moderni POS for Windows programa. Tada sukurkite aparatūros stotį į **skirti** tipo parduotuvės, kur bus naudojamas registrą. Paleidus šiuolaikinės EKA, IPC aparatūros stotis bus aktyvus, ir POS periferiniai įrenginiai, kurie buvo sukonfigūruoti bus paruoštas naudoti. Jei dėl kokios nors priežasties laikinai neturi reikalauti vietos aparatūros, naudoti su **valdyti aparatūros stočių** operacijos išjungti aparatūros stoties galimybes. Šiuolaikinės EKA taip pat galite naudoti IPC aparatūros stoties bendrauti tiesiogiai su periferiniai įrenginiai, tinklo.

### <a name="iis"></a>IIS

Galite naudoti IIS, atskira versija aparatūros stoties dviem būdais. Aprašo "IIS" reiškia, kad POS programa prisijungia prie Microsoft Internet Information Services aparatūros stotimi. POS programa prisijungia prie IIS aparatūros stoties per žiniatinklio tarnybas, kurios veikia kompiuteryje, kai įrenginiai yra prijungti. Naudojant IIS, mažmeninės prekybos periferinių įrenginių, kurie prijungti prie aparatūros stotis gali būti naudojama iš bet POS registrą, kuris yra tame pačiame tinkle kaip IIS aparatūros stotis. Nes tik šiuolaikinės POS skirtą "Windows" palaiko įtaisytąjį mažmeninės prekybos periferinius įrenginius, visas šiuolaikinės EKA programas turite naudoti IIS aparatūros stoties bendrauti su POS periferiniai įrenginiai, kuriuos esate sukonfigūravę techninės įrangos profilį. Todėl kiekvienu atveju IIS aparatūros stoties reikia kompiuteryje, kuriame veikia tinklo tarnybos ir programa, kuri bendrauja su įrenginiu. IIS aparatūros stotis yra reikalingi visų ne-"Windows" šiuolaikinės EKA programas.

#### <a name="dedicated"></a>Paskirta

Šiuolaikinės EKA naudoja aparatūros stočių ir **skirti** tipo aptikti, kad periferiniai įrenginiai yra prijungti tiesiogiai prie kompiuterio, kai app yra naudojama. Vis dėlto, **skirti** tipo taip pat gali būti naudojamas IIS aparatūros stotys. Į tradicines, pastovaus POS scenarijų, kuris naudoja debesies POS kaip POS programa, kad **skirti** aparatūros stoties tipas yra naudojamas IIS aparatūros stotelės, išdėstytos tame pačiame kompiuteryje, kuriame veikia debesyje POS. Mažmeniniam lygiui periferinę įrangą, skirtą IIS aparatūros stotis turi geriau mažmeninės prekybos periferinių palaikymo tradicinių, pastovaus POS scenarijų. Speciali įranga stotis palaiko visi periferiniai įrenginiai, kuris palaiko aparatūros profilyje.

#### <a name="shared"></a>Bendrai naudojama

Bendras įrangos stotims, skirtoms naudoti kelis POS prietaisai per dieną metu. Bendra aparatūros stotys yra optimali, siekiant remti tik pinigų stalčiai, gavimas spausdintuvai ir mokėjimo terminalų. Tiesiogiai negalite prisijungti atskiras brūkšninių kodų skaitytuvai, MSRs, eilutėje rodomas, svarstyklės ar kitus įrenginius. Priešingu atveju konfliktai bus įvykti bandant reikalauti tų išorinių įrenginių vienu metu kelis POS prietaisai. Štai kaip konfliktų yra valdomas palaikomi įrenginiai:

-   **Grynųjų pinigų stalčių** – kasos stalčius atidaromas per įvykį, kuris siunčiamas į įrenginį. Vienintelė problema, kad gali atsirasti, kai pinigų stalčius yra vadinama kyla, jei kasos stalčius jau atidaryta. Tuo atveju, kai bendra aparatūros stočių, turi būti nustatyta kasos stalčiaus **bendro naudojimo** aparatūros profilyje. Šis parametras neleidžia go patikrinti, ar kasos stalčius jau atidaryta, kai ji siunčia atidaryti komandos.
-   **Kvitų spausdintuvu** -jei du kvito spausdinimo komandos siunčiami į aparatūros stotis tuo pačiu metu, vienas iš komandos gali būti prarastas, priklausomai nuo įrenginio. Kai kuriuose įrenginiuose yra vidinės atminties arba kaupimas, galite išvengti šios problemos. Jei spausdinimo komandą nesėkmingas, kasa gauna klaidos pranešimą ir gali pakartoti spausdinimo komandą iš EKA.
-   **Mokėjimo terminalas** – jei kasininkas bando dalyvauti konkurse terminalo mokėjimo operaciją, kurią jau naudojamas, žinutę praneša kasininkas kad terminalo yra naudojamas ir prašo kasą, kad bandyti dar kartą vėliau. Paprastai, kasininkai matyti, kad terminalas jau naudoja ir lauks kol kita operacija bus baigta prieš jie bando dar kartą konkurse.

Tikrinimo planuojama ateityje išleisti, siekiant nustatyti, ar nepalaikoma įrenginiai yra nustatyti techninės įrangos profilį, kuris yra susietas su bendra aparatūros stoties. Nustačius nepalaikomas įrenginius vartotojas gaus pranešimą, kuriame teigiama, kad prietaisai nepalaiko bendra aparatūros stotys. Tuo atveju, kai bendra aparatūros stočių, į **pasirinkite pagal konkurso** parinktis nustatyta **taip** lygmeniu registrą. POS vartotojo tada paraginti pasirinkite aparatūros stotį pasirinkus konkursą EKA kasos operacijos. Pasirinkus aparatūros stoties tik konkurso metu, aparatūros stoties pasirinkimas papildomas tiesiogiai prie POS darbo eigos mobiliojo ryšio scenarijų. Kaip papildoma nauda, eilutės ekranas mokėjimo terminalo nenaudojamas bendrai naudojamą scenarijų. Jeigu mokėjimo terminalas yra eilutės ekranas, kiti vartotojai gali blokuoti naudojant tą terminalą, kol operacija bus baigta. Mobiliojo ryšio scenarijų, linijos gali būti pridėtas sandorio per ilgesnį laikotarpį. Todėl, kad **pasirinkite pagal konkurso** variantas yra reikalinga siekiant užtikrinti optimalų prietaiso.

### <a name="network-peripherals"></a>Tinklo periferiniai įrenginiai

Tinklo pavadinimas įrenginių aparatūros profilyje leidžia pinigų stalčiai, gavimas spausdintuvai ir mokėjimo terminalų prijungti per tinklo ryšį.

#### <a name="modern-pos-for-windows"></a>Šiuolaikinės POS, skirta "Windows"

Dviejose vietose, galite nurodyti IP adresus tinklo periferiniams įrenginiams. Jei šiuolaikinės POS Windows klientas naudoja vieningi tinklo periferiniai įrenginiai, turėtumėte nustatyti IP adresus tų įrenginių naudojant į **IP konfigūracijos** variantas ir veiksmų srityje, registras, pats. Tuo atveju, kai tinklo įrenginiai, kurie bus dalijamasi tarp EKA registrus, techninės įrangos profilį, tinklo įrenginių jai gali susieti tiesiogiai su bendra aparatūros stoties. Priskirti IP adresus, pasirinkite šio aparatūros stoties į **mažmeninės prekybos parduotuvėse** puslapio ir tada naudokite su **IP konfigūraciją** variantas, **aparatūros stočių** skyriuje nurodyti tinklo įrenginiai, kurie yra priskirtas šios stoties aparatūrą. Dėl aparatūros stotys, kurios turi tik tinklo įrenginius, jūs neturite įdiegti aparatūros stotis pati. Tokiu atveju aparatūros stotis gali būti reikalinga tik konceptualiai grupės tinklo adresavimo prietaisus pagal jų buvimo vietą mažmeninės prekybos parduotuvėje.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Debesų kompiuterijos POS, iOS šiuolaikinės POS ir modernus EKA "Android"

Logika, kad diskai fiziškai prijungtas ir tinklo adresavimo periferiniai įrenginiai esanti aparatūra stoties. Todėl visi POS klientams išskyrus šiuolaikinės POS for Windows, IIS aparatūros stotis turi būti įdiegta ir aktyvus, jei norite įgalinti POS bendrauti su periferiniai įrenginiai, nepriklausomai nuo to, ar tie periferiniai įrenginiai yra fiziškai prijungtas prie aparatūros stoties ar spręsti per tinklą.

## <a name="setup-and-configuration"></a>Sąranka ir konfigūravimas
### <a name="hardware-station-installation"></a>Aparatūra stoties diegimas

Informacijos ieškokite [mažmeninė prekyba aparatūra stoties konfigūracijos ir diegti](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Šiuolaikinės POS, skirtą "Windows" sąranka ir konfigūravimas

Informacijos ieškokite [mažmeninė šiuolaikinės EKA konfigūracijos ir diegti](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OEKA įrenginio sąranka ir konfigūravimas

Daugiau informacijos apie OEKA komponentus, rasite šio dokumento skyriuje "Palaiko sąsajas". Paprastai, prietaiso gamintojo pateiktais OPOS vairuotojai. Kai OEKA įrenginio tvarkyklė yra įdiegta, ji suteikia raktą Windows registro vienoje iš šių vietų:

-   **32-bitų sistema:** HKEY\_vietos\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bitų sistemai:** HKEY\_vietos\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Per ServiceOPOS registro vieta, sukonfigūruotas prietaisus yra organizuotas pagal OEKA įrenginio klasė. Išsaugota kelių įrenginių tvarkykles.

## <a name="supported-scenarios-by-hardware-station-type"></a>Palaikomos scenarijus iš stoties jungčiai
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klientų palaikymas – IPC aparatūros stoties vs IIS aparatūros stotis

Šioje lentelėje yra topologijos ir visuotinio diegimo scenarijai, kuriuos palaiko.

| Klientas      | IPC aparatūros stotis | IIS aparatūros stotis |
|-------------|----------------------|----------------------|
| "Windows" programėlės | Taip                  | Taip                  |
| Cloud POS   | Nr.                   | Taip                  |
| "Android"     | Nr.                   | Taip                  |
| "iOS"         | Nr.                   | Taip                  |

### <a name="network-peripherals"></a>Tinklo periferiniai įrenginiai

Tinklo periferiniai įrenginiai gali būti remiami tiesiogiai aparatūros stotis, kuri yra įmontuota į šiuolaikinės POS for Windows programa. Ir visi kiti Klientai, turite įdiegti IIS aparatūros stoties.

| Klientas      | IPC aparatūros stotis | IIS aparatūros stotis |
|-------------|----------------------|----------------------|
| "Windows" programėlės | Taip                  | Taip                  |
| Cloud POS   | Nr.                   | Taip                  |
| "Android"     | Nr.                   | Taip                  |
| "iOS"         | Nr.                   | Taip                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Palaikomų įrenginių tipų iš stoties jungčiai
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Šiuolaikinės POS Windows IPC (integruotas) aparatūros stotelės

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Palaikomas įrenginys klasė</th>
<th>Palaikomas sąsajos</th>
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
<li>UWP (jokios sąrankos nereikia.)</li>
<li>Klaviatūros pleišto (jokios sąrankos nereikia.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Išdavėjas</td>
<td><ul>
<li>OEKA</li>
<li>Tinklo <strong>Pastaba:</strong> tik vieną stalčių galima nustatyti, jei <strong>naudoti bendrai perėjimas</strong> yra sukonfigūruotas stalčiuje.</li>
</ul></td>
</tr>
<tr class="odd">
<td>2 stalčius</td>
<td><ul>
<li>OEKA</li>
<li>Tinklo <strong>Pastaba:</strong> tik vieną stalčių galima nustatyti, jei <strong>naudoti bendrai perėjimas</strong> yra sukonfigūruotas stalčiuje.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skaitytuvas</td>
<td><ul>
<li>OEKA</li>
<li>UWP (jokios sąrankos nereikia.)</li>
<li>Klaviatūros pleišto (jokios sąrankos nereikia.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>2 skaitytuvas</td>
<td><ul>
<li>OEKA</li>
<li>UWP (jokios sąrankos nereikia.)</li>
<li>Klaviatūros pleišto (jokios sąrankos nereikia.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Mastelis</td>
<td>OEKA</td>
</tr>
<tr class="odd">
<td>PIN rinkiklis</td>
<td>OEKA (parama yra teikiama per pritaikymas mokėjimo jungties).</td>
</tr>
<tr class="even">
<td>Parašo fiksavimas</td>
<td>OEKA</td>
</tr>
<tr class="odd">
<td>Mokėjimo terminalas</td>
<td><ul>
<li>Vartotojo įrenginių palaikymas</li>
<li>Tinklo (daugiau informacijos ie¹kokite mokėjimo jungtis.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visos šiuolaikinės EKA klientams, kurie skirtą IIS aparatūros stotis

**Pastaba:** kai IIS aparatūros stotis yra "skirta," yra tiesioginis ryšys tarp EKA kliento ir aparatūros stoties.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Palaikomas įrenginys klasė</th>
<th>Palaikomas sąsajos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>Windows tvarkyklė <strong>Pastaba:</strong> For Windows spausdintuvų naudojimas tinkle, aparatūros stoties vartotojas turi turėti teisę prieiti prie spausdintuvo.</li>
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
<li>Tinklo <strong>Pastaba:</strong> tik vieną stalčių už techninės įrangos profilį galima nustatyti, jei <strong>naudoti bendrai perėjimas</strong> yra sukonfigūruotas stalčiuje.</li>
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
<td>OEKA (parama yra teikiama per pritaikymas mokėjimo jungties).</td>
</tr>
<tr class="odd">
<td>SIG. perimti</td>
<td>OEKA</td>
</tr>
<tr class="even">
<td>Mokėjimo terminalas</td>
<td><ul>
<li>Vartotojo įrenginių palaikymas</li>
<li>Tinklo (daugiau informacijos ie¹kokite mokėjimo jungtis.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visos šiuolaikinės EKA klientams, kurie bendrai IIS aparatūros stotis

**Pastaba:** kai IIS aparatūros stotis "bendrai", kelis įrenginius naudoti aparatūros stotis tuo pačiu metu. Pagal šį scenarijų, jūs turėtumėte naudoti tik tie prietaisai, kurie yra išvardyti toliau pateiktoje lentelėje. Jei bandote bendrai naudoti prietaisus, kurie nėra išvardyti čia, pvz., brūkšninių kodų skaitytuvai ir MSRs, klaidos atsiranda tada, kai kelis įrenginius prisiekinėja pačiu įrenginiu. Ateityje tokia konfigūracija bus aiškiai neleido.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Palaikomas įrenginys klasė</th>
<th>Palaikomas sąsajos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Spausdintuvas</td>
<td><ul>
<li>OEKA</li>
<li>Windows tvarkyklė <strong>Pastaba:</strong> For Windows spausdintuvų naudojimas tinkle, aparatūros stoties vartotojas turi turėti teisę prieiti prie spausdintuvo.</li>
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
<li>Tinklo <strong>Pastaba:</strong> tik vieną stalčių už techninės įrangos profilį galima nustatyti, jei <strong>naudoti bendrai perėjimas</strong> yra sukonfigūruotas stalčiuje.</li>
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
<li>Vartotojo įrenginių palaikymas</li>
<li>Tinklo (daugiau informacijos ie¹kokite mokėjimo jungtis.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Palaikomos scenarijus konfigūracija
Daugiau informacijos apie tai, kaip sukurti aparatūros profiliai, rasite [nustatyti ir išlaikyti kanalo klientams, taip pat registruose ir aparatūros stočių](define-maintain-channel-clients-registers-hw-stations.md). **Pastaba:** "Microsoft Dynamics 365" operacijų versija 1611, aparatūros stoties profilis nebenaudojamas. Atributus, kurie buvote nustatę aparatūros stoties profilyje dabar yra dalis aparatūros stotis pati.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Šiuolaikinės POS Windows IPC (integruotas) aparatūros stotelės

Ši konfigūracija yra labiausiai būdingas konfigūracijos tradicinių, pastovaus POS registrų. Pagal šį scenarijų, aparatūros profilio informacija atvaizduojama tiesiai į registrą, pati. EFT terminalo numerį reikėtų nustatyti į registrą, pati. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurti techninės įrangos profilį, kur reikalaujama periferiniai įrenginiai yra sukonfigūruotas.
2.  Aparatūros šabloną priskirti POS registrą.
3.  Sukurti aparatūros stotį į **skirti** tipo mažmeninės prekybos parduotuvės, kur bus naudojamas POS registrą. Aprašas yra pasirinktinis. **Pastaba:** jums nereikia nustatyti kitos savybės aparatūros stotyje. Visos kitos būtinos informacijos, pvz., techninės įrangos profilį, ateis iš registro, pati.
4.  Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**.
5.  Pasirinkite į **1090** pasiskirstymo grafikas sinchronizuoti naują aparatūros profilį į parduotuvę. Spustelėkite **surengę** su sinchronizavimo go.
6.  Pasirinkite į **1040** pasiskirstymo grafikas sinchronizuoti naują aparatūros stotis prie parduotuvės. Spustelėkite **surengę** su sinchronizavimo go.
7.  Įdiegus ir suaktyvinus šiuolaikinės POS for Windows.
8.  Šiuolaikinės POS, Windows paleisti, ir pradėti naudoti prijungtų periferinių įrenginių.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Visos šiuolaikinės EKA klientams, kurie skirtą IIS aparatūros stotis

Šią konfigūraciją gali būti naudojamas visus šiuolaikinės EKA klientams, kurie aparatūros stotį, kuri yra naudojama tik viena POS registruotis. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurti techninės įrangos profilį, kur reikalaujama periferiniai įrenginiai yra sukonfigūruotas.
2.  Sukurti aparatūros stotį į **skirti** tipo mažmeninės prekybos parduotuvės, kur bus naudojamas POS registrą.
3.  Speciali įranga stotyje, nustatyti šias ypatybes:
    -   **Pagrindinio kompiuterio pavadinimas** – pagrindiniame kompiuteryje, kur bus paleisti aparatūros stotelės pavadinimą. **Pastaba:** debesis POS galima išspręsti **localhost** nustatyti, kur debesys POS veikia vietiniame kompiuteryje. Tačiau, sertifikatas, kurio reikia norint suporuoti debesis POS su aparatūros stoties taip pat turi "Localhost" kaip kompiuterio vardas. Siekiant išvengti problemų, rekomenduojame, kad nurodai egzempliorius, kiekviena speciali įranga stotis parduotuvės, kaip reikalaujama. Kiekvienas aparatūros geležinkelio stotį, pagrindinio kompiuterio vardas turėtų būti tikro kompiuterio vardo kur aparatūros stotis bus dislokuotos.
    -   **Uosto** – prievadą naudoti techninės įrangos geležinkelio stotį, bendrauti su šiuolaikinės EKA klientas.
    -   **Aparatūros profilis** – jei aparatūros profilis nėra sąlyga aparatūros stotis pati, bus galima naudoti techninės įrangos profilį, kuris yra priskirtas registras.
    -   **EFT POS numeris** – The EFT terminalų ID naudoti siunčiant EFT leidimus. Ši ID teikia kredito kortelės procesorių.
    -   **Paketo pavadinimą** – į aparatūros komplektas naudoti naudojant aparatūros stotis yra.

4.  Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**.
5.  Pasirinkite į **1090** pasiskirstymo grafikas sinchronizuoti naują aparatūros profilį į parduotuvę. Spustelėkite **surengę** su sinchronizavimo go.
6.  Pasirinkite į **1040** pasiskirstymo grafikas sinchronizuoti naują aparatūros stotis prie parduotuvės. Spustelėkite **surengę** su sinchronizavimo go.
7.  Įdiegti aparatūrą stoties. Daugiau informacijos apie tai, kaip įdiegti aparatūros stoties, rasite [mažmeninė prekyba aparatūra stoties konfigūracijos ir diegti](retail-hardware-station-configuration-installation.md).
8.  Įdiegus ir suaktyvinus šiuolaikinės EKA. Daugiau informacijos apie tai, kaip įdiegti šiuolaikinės EKA, rasite [mažmeninė šiuolaikinės EKA konfigūracijos ir diegti](retail-modern-pos-device-activation.md).
9.  Prisijunkite prie šiuolaikinės EKA ir pasirinkite **atlikti ne Stalčiaus operacijas,**.
10. Paleisti į **valdyti aparatūros stočių** operacijos.
11. Spustelėkite **tvarkyti**.
12. Aparatūros stoties valdymo puslapyje, nustatykite parinktį įjungti aparatūros stoties.
13. Pasirinkite naudoti, ir spustelėkite aparatūros stotis **pora**.
14. Aparatūros stotis sujungta, spustelėkite **arti**.
15. Aparatūros stoties pasirinkimo puslapyje spustelėkite pažymėtą aparatūros stotis, kad jį suaktyvintumėte.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Visos šiuolaikinės EKA klientams, kurie bendrai IIS aparatūros stotis

Šią konfigūraciją gali būti naudojamas visus šiuolaikinės EKA klientams, kad dalis aparatūros stotys su kitais įrenginiais. Norėdami nustatyti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Sukurti techninės įrangos profilį, kur reikalaujama periferiniai įrenginiai yra sukonfigūruotas.
2.  Sukurti aparatūros stotį į **bendro naudojimo** tipo mažmeninės prekybos parduotuvės, kur bus naudojamas POS registrą.
3.  Bendra aparatūros stotyje, nustatyti šias ypatybes:
    -   **Pagrindinio kompiuterio pavadinimas** – pagrindiniame kompiuteryje, kur bus paleisti aparatūros stotelės pavadinimą.
    -   **Aprašymas** – tekstą, kuris padės nustatyti aparatūros stoties, pvz., **deklaracijas** arba **dirbanti parduotuvė**.
    -   **Uosto** – prievadą naudoti techninės įrangos geležinkelio stotį, bendrauti su šiuolaikinės EKA klientas.
    -   **Aparatūros profilis** – bendra aparatūros stotys, kiekvienas aparatūros stotis turi turėti techninės įrangos profilį. Aparatūros profiliai gali būti dalijamasi tarp aparatūros stotys, tačiau jie priskirti kiekvienai aparatūros stoties. Be to, mes rekomenduojame naudoti bendro naudojimo pokyčiai keliuose įrenginiuose naudojant tą pačią bendro naudojimo įrangos stotį. Norėdami nustatyti bendras poslinkis, spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros profiliai**. Kiekvienos bendros techninės įrangos profilį, pasirinkite kasos stalčius, o nustatyti, **bendro naudojimo pamainą Stalčiaus** į **taip**.
    -   **EFT POS numeris** – The EFT terminalų ID naudoti siunčiant EFT leidimus. Ši ID teikia kredito kortelės procesorių.
    -   **Paketo pavadinimą** – į aparatūros komplektas naudoti naudojant aparatūros stotis yra.

4.  Pakartokite 2 ir 3 kiekvienos papildomos aparatūros stoties, reikalingas parduotuvėje.
5.  Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**.
6.  Pasirinkite į **1090** pasiskirstymo grafikas sinchronizuoti naują aparatūros profilį į parduotuvę. Spustelėkite **surengę** su sinchronizavimo go.
7.  Pasirinkite į **1040** pasiskirstymo grafikas sinchronizuoti naują aparatūros stotis prie parduotuvės. Spustelėkite **surengę** su sinchronizavimo go.
8.  Įdiegti aparatūrą stotis kiekviename pagrindiniame kompiuteryje, galite nustatyti 2 ir 3 veiksmus. Daugiau informacijos apie tai, kaip įdiegti aparatūros stoties, rasite [mažmeninė prekyba aparatūra stoties konfigūracijos ir diegti](retail-hardware-station-configuration-installation.md).
9.  Įdiegus ir suaktyvinus šiuolaikinės EKA. Daugiau informacijos apie tai, kaip įdiegti šiuolaikinės EKA, rasite [mažmeninė šiuolaikinės EKA konfigūracijos ir diegti](retail-modern-pos-device-activation.md).
10. Prisijunkite prie šiuolaikinės EKA ir pasirinkite **atlikti ne Stalčiaus operacijas,**.
11. Paleisti į **valdyti aparatūros stočių** operacijos.

12. Spustelėkite **tvarkyti**.
13. Aparatūros stoties valdymo puslapyje, nustatykite parinktį įjungti aparatūros stoties.
14. Pasirinkite naudoti, ir spustelėkite aparatūros stotis **pora**.
15. Kartokite 14 kiekvienai aparatūros stotis, kuri naudoja šiuolaikinės EKA.
16. Po to, kai visos būtinos aparatūros stotys yra susieti, spustelėkite **arti**.
17. Aparatūros stoties pasirinkimo puslapyje spustelėkite pažymėtą aparatūros stotis, kad jį suaktyvintumėte. **Pastaba:** jei įrenginiuose dažnai naudojamos skirtingoms aparatūros stotys, rekomenduojame sukonfigūruoti šiuolaikinės EKA Norėdami paraginti kasininkus pasirinkite aparatūros stoties, kai jie pradėti pirkimo procesą. Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**registrų**. Pasirinkite registrą ir tada nustatykite į **pasirinkite pagal konkurso** į **taip**. Naudoti su **1090** pasiskirstymo grafikas sinchronizuoti kanalo duomenų bazės keitimus.

## <a name="extensibility"></a>Išplečiamumas
Informacijos apie išplėtimo scenarijus, techninės įrangos geležinkelio stotį rasite [aparatūros stoties išplėtimo](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Sauga
Atitinka naujausius saugumo standartus, šiuos parametrus reikėtų naudoti gamybos aplinkoje: **Pastaba:** aparatūros stoties diegimo programa automatiškai atliks šiuos registro redagavimą diegiant per savitarną.

-   Saugiųjų jungčių lygmuo (SSL) turi būti išjungtas.
-   Tik transportavimo lygmens saugos (TLS) 1.2 versija (arba didžiausia dabartinėje) turėtų įjungtas ir naudojamas. **Pastaba:** pagal numatytuosius nustatymus SSL ir TLS išskyrus TLS 1.2 visi versija yra išjungta. Norėdami redaguoti arba įgalinti šias reikšmes, atlikite šiuos veiksmus:
    1.  Paspauskite "Windows" logotipo klavišas + R ir atidarykite su **paleisti** lango.
    2.  – Į **atviras** lauke, įveskite **Regedit**, ir tada spustelėkite **gerai**.
    3.  Jei su **vartotojo abonemento valdymo tarnybos** pranešimo langas, spustelėkite **taip**.
    4.  – Į **registro redaktorių** langą, eikite į **HKEY\_vietos\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Šie raktai automatiškai įrašyti leisti TLS 1.2 tik:
        -   TLS 1.2Server: įjungtas = 1
        -   TLS 1.2Server:DisabledByDefault = 0
        -   TLS 1.2Client: įjungtas = 1
        -   TLS 1.2Client:DisabledByDefault = 0
        -   TLS 1.1Server: įjungtas = 0
        -   TLS 1.1Client: įjungtas = 0
        -   TLS 1.0Server: įjungtas = 0
        -   TLS 1.0Client: įjungtas = 0
        -   SSL 3.0Server: įjungtas = 0
        -   SSL 3.0Client: įjungtas = 0
        -   SSL 2.0Server: įjungtas = 0
        -   SSL 2.0Client: įjungtas = 0
-   Jokių papildomų tinklo prievadų turi būti atviras, nebent jie yra žinomi, nurodytos priežastys.
-   Cross-kilmės išteklių dalijimasis turi būti išjungtas ir turite nurodyti leistiną kilmę, kad priimami.
-   Tik patikimos sertifikavimo institucijos vartoti gauti sertifikatus, kuris bus naudojamas kompiuteriams, paleisti aparatūros stoties.

**Pastaba:** labai svarbu, kad peržiūrėtumėte saugumo gairių IIS ir mokėjimo kortelių pramonė (PCI) reikalavimus.

## <a name="peripheral-simulator"></a>Periferinis simuliatorius
Informacijos ieškokite [mažmeninė periferinių simuliatorius](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested periferinių įrenginių
### <a name="ipc-built-in-hardware-station"></a>IPC (integruotas) aparatūros stotis

Šiuos įrenginius buvo atliktas naudojant IPC aparatūros stotis, kuri yra įmontuota į šiuolaikinės POS for Windows.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                |
|--------------|----------|-----------|-------------------------|
| Epson        | TM-T88IV | OEKA      |                         |
| Epson        | TM-T88V  | OEKA      |                         |
| Žvaigždė         | TSP650II | OEKA      |                         |
| Žvaigždė         | TSP650II | Pasirinktinai    | Prijungta per tinklą   |
| Žvaigždė         | mPOP     | OEKA      | Prijungtas "Bluetooth" ryšiu |
| HP           | F7M67AA  | OEKA      | Energija varomas USB             |

#### <a name="bar-code-scanner"></a>Brūkšninių kodų skaitytuvas

| Gamintojas  | Modelis         | Sąsaja | Komentarai |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OEKA      |          |
| Honeywell     | 1900          | UWP       |          |
| Simbolis        | LS2208        | OEKA      |          |
| Integruota HP | E1L07AA       | OEKA      |          |
| Datalogic     | Magellan 8400 | OEKA      |          |

#### <a name="pin-pad"></a>PIN rinkiklis

| Gamintojas | Modelis  | Sąsaja | Komentarai                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OEKA      | Reikia pritaikyti mokėjimo jungties |

#### <a name="payment-terminal"></a>Mokėjimo terminalas

| Gamintojas | Modelis | Sąsaja | Komentarai                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Lygiadienis      | L5300 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungties                                |
| VeriFone     | MX925 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungtis; prijungta per tinklą ir USB |
| VeriFone     | MX915 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungtis; prijungta per tinklą ir USB |

#### <a name="cash-drawer"></a>Pinigų stalčius

| Gamintojas | Modelis     | Sąsaja | Komentarai                |
|--------------|-----------|-----------|-------------------------|
| Žvaigždė         | mPOP      | OEKA      | Prijungtas "Bluetooth" ryšiu |
| APG          | Atwood    | Pasirinktinai    | Prijungta per tinklą   |
| Žvaigždė         | SMD2-1317 | OEKA      |                         |
| HP           | QT457AA   | OEKA      |                         |

#### <a name="line-display"></a>Eilutės rodymas

| Gamintojas  | Modelis   | Sąsaja | Komentarai |
|---------------|---------|-----------|----------|
| Integruota HP | G6U79AA | OEKA      |          |
| Epson         | M58DC   | OEKA      |          |

#### <a name="signature-capture"></a>Parašo fiksavimas

| Gamintojas | Modelis  | Sąsaja | Komentarai |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OEKA      |          |

#### <a name="scale"></a>Mastelis

| Gamintojas | Modelis         | Sąsaja | Komentarai |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OEKA      |          |

#### <a name="msr"></a>MSR

| Gamintojas | Modelis       | Sąsaja | Komentarai |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OEKA      |          |
| HP           | IDRA-334133 | OEKA      |          |

### <a name="dedicated-iis-hardware-station"></a>Skirta IIS aparatūros stotis

Šiuos įrenginius buvo atliktas naudojant specialią (ne bendra) IIS aparatūros stotis kartu su šiuolaikinės POS for Windows ir debesies POS.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OEKA      |                           |
| Epson        | TM-T88V  | OEKA      |                           |
| Žvaigždė         | TSP650II | OEKA      |                           |
| Žvaigždė         | TSP650II | Pasirinktinai    | Prijungta per tinklą     |
| Žvaigždė         | TSP100   | OEKA      | Reikalaujama, kad TSP650II tvarkyklės |
| HP           | F7M67AA  | OEKA      | Energija varomas USB               |

#### <a name="bar-code-scanner"></a>Brūkšninių kodų skaitytuvas

| Gamintojas  | Modelis   | Sąsaja | Komentarai |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OEKA      |          |
| Simbolis        | LS2208  | OEKA      |          |
| Integruota HP | E1L07AA | OEKA      |          |

#### <a name="pin-pad"></a>PIN rinkiklis

| Gamintojas | Modelis  | Sąsaja | Komentarai                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OEKA      | Reikia pritaikyti mokėjimo jungties |

#### <a name="payment-terminal"></a>Mokėjimo terminalas

| Gamintojas | Modelis | Sąsaja | Komentarai                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Lygiadienis      | L5300 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungties                                |
| VeriFone     | MX925 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungtis; prijungta per tinklą ir USB |
| VeriFone     | MX915 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungtis; prijungta per tinklą ir USB |

#### <a name="cash-drawer"></a>Pinigų stalčius

| Gamintojas | Modelis     | Sąsaja | Komentarai              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pasirinktinai    | Prijungta per tinklą |
| Žvaigždė         | SMD2-1317 | OEKA      |                       |
| HP           | QT457AA   | OEKA      |                       |

#### <a name="line-display"></a>Eilutės rodymas

| Gamintojas  | Modelis   | Sąsaja | Komentarai |
|---------------|---------|-----------|----------|
| Integruota HP | G6U79AA | OEKA      |          |
| Epson         | M58DC   | OEKA      |          |

#### <a name="signature-capture"></a>Parašo fiksavimas

| Gamintojas | Modelis  | Sąsaja | Komentarai |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OEKA      |          |

#### <a name="scale"></a>Mastelis

| Gamintojas | Modelis         | Sąsaja | Komentarai |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OEKA      |          |

#### <a name="msr"></a>MSR

| Gamintojas | Modelis       | Sąsaja | Komentarai |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OEKA      |          |
| HP           | IDRA-334133 | OEKA      |          |

### <a name="shared-iis-hardware-station"></a>Bendra IIS aparatūros stotis

Šiuos įrenginius buvo atliktas naudojant bendrai naudojamą IIS aparatūros stotis kartu su šiuolaikinės POS for Windows ir debesies POS. **Pastaba:** tik spausdintuvo, mokėjimo terminalą, ir grynųjų pinigų stalčius yra palaikomi.

#### <a name="printer"></a>Spausdintuvas

| Gamintojas | Modelis    | Sąsaja | Komentarai                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OEKA      |                           |
| Epson        | TM-T88V  | OEKA      |                           |
| Žvaigždė         | TSP650II | OEKA      |                           |
| Žvaigždė         | TSP650II | Pasirinktinai    | Prijungta per tinklą     |
| Žvaigždė         | TSP100   | OEKA      | Reikalaujama, kad TSP650II tvarkyklės |
| HP           | F7M67AA  | OEKA      | Energija varomas USB               |

#### <a name="payment-terminal"></a>Mokėjimo terminalas

| Gamintojas | Modelis | Sąsaja | Komentarai                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungtis; prijungta per tinklą ir USB |
| VeriFone     | MX915 | Pasirinktinai    | Reikia pritaikyti mokėjimo jungtis; prijungta per tinklą ir USB |

#### <a name="cash-drawer"></a>Pinigų stalčius

| Gamintojas | Modelis     | Sąsaja | Komentarai              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Pasirinktinai    | Prijungta per tinklą |
| Žvaigždė         | SMD2-1317 | OEKA      |                       |
| HP           | QT457AA   | OEKA      |                       |

## <a name="troubleshooting"></a>Trikčių šalinimas
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Šiuolaikinės EKA gali aptikti aparatūros stotis į savo sąrašą, atrankos, tačiau ji negali atlikti Kergimas

**Sprendimas:** patikrinti galimą nepakankamumas taškų sąrašas:

-   Kompiuteryje, kuriame veikia modernus EKA pasitiki sertifikatą, kuriame yra naudojama reikiamame kompiuteryje, kuriame veikia įrangos stoties.
    -   Norėdami patikrinti šį nustatymą, naudodami žiniatinklio naršyklę, eikite į šį URL: https://&lt;kompiuterio vardas&gt;:&lt;prievado numerį&gt;/HardwareStation/stalo.
    -   Šis URL naudoja ping patikrinkite, ar kompiuteris gali būti prieinama, ir naršyklė rodo, ar sertifikatas laikomas patikimu. (Pvz., "Internet Explorer" užrakto piktograma rodoma adreso juostoje. Spustelėjus šią piktogramą, "Internet Explorer" patikrina, ar sertifikatas yra šiuo metu patikimas. Galite įdiegti sertifikatą vietiniame kompiuteryje peržiūrėti informaciją apie sertifikatą, kuris yra rodomas.)
-   Kompiuteryje, kuriame veikia įrangos stoties, uostą, kuris bus naudojamas aparatūros stoties atidaroma užkarda.
-   Aparatūros stoties teisingai įrengtas prekybinės sąskaitos informaciją per diegti prekybos informacijos įrankis, kuris veikia aparatūros stoties diegimo programos pabaigoje.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Šiuolaikinės EKA nepavyksta aptikti aparatūros stotis į savo sąrašą, atrankos

**Sprendimas:** bet kurios iš šių veiksnių gali sukelti šią problemą:

-   Aparatūros stoties dar buvo nustatytas teisingai būstinė. Atlikite anksčiau aprašytus įsitikinti, kad teisingai įrašyti aparatūros stoties profilį ir aparatūros stoties.
-   Darbo vietos ne buvo paleista atnaujinti kanalui konfigūruoti. Tokiu atveju vykdykite užduotį 1070 kanalo konfigūracijai.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Šiuolaikinės EKA neatspindi naujus pinigų Stalčiaus parametrus

**Sprendimas:** arti dabartinio paketo. Kasos stalčiaus pakeitimai nėra atnaujintas iki šiuolaikinės EKA tol, kol neuždarytas esamo paketo.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Šiuolaikinės EKA praneπimus problema su periferinių mažmeninė prekyba

**Sprendimas:** čia yra keletas tipiškų priežasčių šis klausimas:

-   Įsitikinkite, kad kitas prietaiso tvarkyklės konfigūravimo priemones yra uždarytos. Jei šių įmonių dirba, jie gali neleisti šiuolaikinės POS arba aparatūros stotis iš prietaiso.
-   Jei mažmeninė periferinės bendrinamas su keliais POS prietaisai, įsitikinkite, kad ji priklauso vienai iš šių kategorijų:
    -   Pinigų stalčius
    -   Kvitų spausdintuvu
    -   Mokėjimo terminalas

    Jei į periferinius nepriklauso vienai iš šių kategorijų, aparatūros stotis nėra siekiama leisti išoriniu įrenginiu dalijasi keli POS prietaisai.
-   Kartais, tvarkyklės gali sukelti bendrą valdymo objektai (CCOs) gali nustoti tinkamai veikti. Jei įrenginį neseniai buvo įdiegta, bet ji tinkamai neveikia arba pastebite kitų problemų, dažnai gali išspręsti problemą, iš naujo įdiegti į CCOs. Norėdami atsisiųsti į CCOs, aplankyti <http://monroecs.com/oposccos_current.htm>.
-   Jei dažnai periferinių pakeitimus bandymų arba trikčių diagnostika, gali tekti iš naujo nustatyti IIS užuot laukusios, kol į talpyklą, atšviežinta. Norėdami iš naujo nustatyti IIS, atlikite šiuos veiksmus:
    1.  Nuo to **pradėti** meniu, tipo **CMD**.
    2.  Ieškos rezultatuose dešiniuoju pelės mygtuku spustelėkite **komandinės eilutės**, ir tada spustelėkite **vykdyti kaip administratorius**.
    3.  – Į **komandinės eilutės** lange, tipo **iisreset norite** ir paspauskite Enter.
    4.  Paleidę IIS iš naujo, iš naujo paleiskite šiuolaikinės EKA.
-   Kai darote dažnai keisti į periferinius įrenginius, jei jūs taip pat dažnai paleidimas ir išjungimas kliento POS, dllhost procesas nuo ankstesnės POS sesijos gali trukdyti esamam seansui. Tokiu atveju įrenginys gali būti naudojamos tol, kol uždarysite dinaminių saitų bibliotekos (DLL) kompiuterį, kurį valdo ankstesnės sesijos. Norėdami uždaryti DLL pagrindinio kompiuterio, atlikite šiuos veiksmus:
    1.  Nuo to **pradėti** meniu, tipo **užduočių tvarkytuvo**.
    2.  Ieškos rezultatuose spustelėkite **užduočių tvarkytuvo**.
    3.  Task Manager, ant to **detalių** skirtuką, spustelėkite stulpelio antraštę, pažymėtas **pavadinimas** rūšiuoti lentelę abėcėlės tvarka pagal pavadinimą.
    4.  Slinkite žemyn, kol rasite dllhost.exe.
    5.  Pasirinkite kiekvieną DLL pagrindinio kompiuterio, o tada spustelėkite **užbaigti užduotį**.
    6.  Po to, kai buvo uždarytos DLL šeimininkai, iš naujo paleiskite šiuolaikinės EKA.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Mažmeninės prekybos periferinių simuliatorius](retail-peripheral-simulator.md)


