---
title: "Mažmeninės prekybos periferinių simuliatorius"
description: "Šioje temoje aprašoma, periferinių simulator įrankis, kuris pateikiamas Microsoft Dynamics &quot;365&quot; operacijų - mažmeninės prekybos."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Mažmeninės prekybos periferinių simuliatorius

Šioje temoje aprašoma, periferinių simulator įrankis, kuris pateikiamas Microsoft Dynamics "365" operacijų - mažmeninės prekybos.

<a name="overview"></a>Apžvalga
--------

Microsoft Dynamics 365 operacijų - mažmeninės prekybos periferinių simuliatorius yra įrankis, kuris padeda jums sukurti, išbandyti ir šalinti periferinius įrenginius, kurie yra naudojami mažmeninės prekybos aplinkoje. Periferinė simuliatorius galite racionalizuoti mažmeninės prekybos periferinių įrenginių bandymų ir nustatyti problemas, kurias sukelia sugedęs tvarkyklės arba neteisingas nustatymas. Periferinė simuliatorius yra darbalaukio programa, kuri siūlo virtualių versijų prietaisai kad Dynamics 365 operacijoms - mažmeninės prekybos palaiko. Skirsnis, skirtas kiekvienai virtualaus įrenginio rodo sąveiką tarp įrenginio ir mažmeninė point of sale (POS). Taip pat galite naudoti jį įvesčiai, kuris galioja atliekant įvairius POS scenarijus. Periferinė simuliatorius palaiko POS ir šių virtualių įrenginių sąveika:

-   **Spausdintuvas** – periferinė simuliatorius gali parodyti kvitai, kasos čekių spausdintuvas sukonfigūruotos.
-   **Linijos ekrane** – galite konfigūruoti virtualaus eilutės ekranas rodo veiklos fizinės linijos ekrane.
-   **Magnetinės juostelės skaitytuvas (MSR)** – imituoti magnetine juostele įvykių Go galite siųsti iš periferinių simuliatorius.
-   **Stalčių** – jūs galite imituoti fizinio grynųjų pinigų stalčius.
-   **2 stalčių** – nustatę antrą kasos stalčiaus periferinių simuliatorius, jūs galite imituoti scenarijų, kad įtraukti bendrą POS registrą, kuriame yra dvi aktyvios pamainomis.
-   **Skeneris** – Virtuali brūkšninių kodų skaitytuvo, kuris palaiko periferinę simuliatorius gali išduoti brūkšninio kodo nuskaitymo įvykius.
-   **Mastelio** – Virtuali skalė leidžia imituoti pasvertą elementų sąveika su EKA.
-   **Asmeninio identifikavimo numerio (PIN) pad** – jūs galite imituoti PIN pad operacijas. **Pastaba:** turi įgyvendinti paramos fizinės PIN pad per mokėjimo jungtį.
-   **Parašas surinkimo** – periferinė simuliatorius yra virtualus parašo įvedimo įrenginį, galite nustatyti greitai parašų, kurie yra reikalingi kai kurie pasiūlymai, pvz., kliento sąskaitos mokėjimai.

Taip pat galite naudoti periferinių simuliatorius imituoti klaviatūros pleišto įvykius, kurie yra kilę iš brūkšninių kodų skaitytuvo ir MSR. Virtualus periferinių simuliatorius specialiai palaiko objektų susiejimo ir įdėjimo Retail POS (OEKA) įrenginiai.

## <a name="key-scenarios"></a>Pagrindinis scenarijus
### <a name="troubleshooting"></a>Trikčių šalinimas

Periferinių simuliatorius galite naudoti norėdami pašalinti įrenginio nustatymas. Jei jūs neturite periferinių simuliatorius ar antrojo įrenginio tos pačios klasės, gali būti sunku nustatyti, kur yra kilę klausimai. Tačiau kai periferinių simuliatorius, galite sukurti virtualių įrenginių, ir paleisti pačią kodo maršrutų ir verslo logika, kurie yra naudojami fizinių įrenginių. Žvelgiant iš periferinių simuliatorius, pagrindinis skirtumas tarp virtualios ir fizinės įrenginiai yra aptarnavimo objekto, ar įrenginio tvarkyklė. Įrenginio gamintojo pateiktais fizinių įrenginių aptarnavimo objekto. Priešingai, periferinių Simulator, paslaugų objektai yra pateikiami kaip dalis periferinių simuliatorius. Kai periferinių treniruoklis veikia tinkamai, jei prietaisas neveikia tinkamai, pasikeitus įrenginio pavadinimą aparatūros profilyje yra nekilnojamojo įrenginio pavadinimą, galite manyti, kad yra problemų su aptarnavimo objekto, kad gamintojas.

### <a name="training"></a>Mokymasis

Periferinė simuliatorius galite pridėti realus sluoksnis kasininko darbo mokymą, kai nėra fizinių aparatinės įrangos įrengimas. Kai periferinių simuliatorius yra įtrauktas į mokymo planus, kasininkas gali efektyviau bendrauti su EKA numatant įvesties pavyzdžiui produkto bar kodas nuskaito ir dovanų kortelės brūkšt, o stebėdami, kuriuos gavimus spausdinamos konkrečiam sandoriui.

### <a name="testing"></a>Bandymai

Periferinė simuliatorius galite išbandyti produkto brūkšninius kodus, gavimo formatai ir taip toliau, jums nereikės diegti fizinį aparatūros virtualioje aplinkoje. Nes fizinės aparatūros nėra būtina, ir jums nereikės diegti POS kliento aparatūros stoties ar fiziniame kompiuteryje, galite greičiau bandymas pakeitimai atgal biure.

## <a name="set-up-the-peripheral-simulator"></a>Nustatykite periferinę simuliatorius
### <a name="set-up-a-hardware-profile"></a>Nustačius techninės įrangos profilį

1.  Norėdami nustatyti periferinių simuliatorius, eikite į **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros profiliai**.
2.  Norėdami sukurti naują profilį, spustelėkite **naujas**.
3.  Įveskite reikšmes į **profilis numeris** ir **Aprašymas** laukus.
4.  Naudokite šioje lentelėje nustatyti virtualių įrenginių, kurie turi būti išbandytos. Čia yra paaiškinimas iš lentelės stulpeliai:
    -   **Prietaisas** – šiame stulpelyje suteikia FastTab, kad jums išplėsti prietaiso pavadinimą.
    -   **Įrenginio tipas** – šiame stulpelyje suteikia vertę, kurią pasirinksite lauką, kuris pažymėtas įrenginio pavadinimą.
    -   **Įrenginio pavadinimas** – šiame stulpelyje suteikia tikslią reikšmę, įveskite įrenginio pavadinimą. **Svarbu:** įrenginių pavadinimai, kurie čia duodami reikalingi, nes aparatūros stoties naudoja šiuos specifinius pavadinimus spręsti įrenginius. Jei nenorite naudoti šių konkrečių pavadinimų, prietaiso nebus galima naudoti.

    | Įrenginys            | Įrenginio tipas | Įrenginio pavadinimas              |
    |-------------------|-------------|--------------------------|
    | Spausdintuvas           | OEKA        | MockOPOSPrinter          |
    | Eilutės rodymas      | OEKA        | MockOPOSLineDisplay      |
    | MSR               | OEKA        | MockOPOSMSR              |
    | Išdavėjas            | OEKA        | MockOPOSDrawer1          |
    | Drawer2           | OEKA        | MockOPOSDrawers          |
    | Skaitytuvas           | OEKA        | MockOPOSScanner          |
    | Mastelis             | OEKA        | MockOPOSScale            |
    | PIN rinkiklis           | OEKA        | MockOPOSPinPad           |
    | Parašo fiksavimas | OEKA        | MockOPOSSignatureCapture |

**Pastaba:** jokios specialios sąrankos aparatūros profilyje turi imituoti klaviatūros pleišto įvykius iš brūkšninio kodo skaitytuvo ir MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Aparatūros šabloną priskirti registrą

1.  Sukūrus techninės įrangos profilį, eikite į **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**registrų**.
2.  – Į **POS registrų** sąrašą, spustelėkite nuorodą į **registro Nr.** lauko registrui, kad turėtų naudoti periferinių simuliatorius.
3.  Spustelėkite **Redaguoti**.
4.  – Į **profiliai** skyrių, į **techninės įrangos profilį** pasirinkite techninės įrangos profilį, kurį sukūrėte virtualus periferiniams įrenginiams.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Sinchronizuoti kanalo duomenų bazės keitimus

1.  Eikite į **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**.
2.  Pasirinkite į **1090** pasiskirstymo grafikas.
3.  Spustelėkite **surengę** Norėdami sinchronizuoti keitimus su EKA.

Po to, kai duomenys yra sinchronizuojami, naujas aparatinės įrangos profilis ir pakeitimus registre yra kanalo duomenų bazėje.

## <a name="install-the-peripheral-simulator"></a>Įdiegti periferinius simuliatorius
1.  Eikite į **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros profiliai**.
2.  Spustelėkite **atsisiųsti**, ir tada spustelėkite **PeripheralSimulator**. **Pastaba:** jūs turite išjungti iššokančių langų blokavimo programos prieš atsisiųsdami periferinių simuliatorius.
3.  Kai atsisiuntimas bus baigtas, atidaryti ir **Parsisiųsti** katalogą ir dukart spustelėkite **VirtualPeripherals.msi** Norėdami paleisti diegimo programą.
4.  Įdiegti periferinių simuliatorius naudojant numatytuosius parametrus.

Be periferinių simuliatorius, turite įdiegti bendrą kontrolės objektus iš Monroe konsultavimo paslaugas. Priešingu atveju, periferinių simuliatorius tinkamai neveiks. Norėdami atsisiųsti bendros kontrolės objektus, eikite į <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Naudojant periferinę simuliatorius
Pradėti periferinių simuliatorius, spustelėkite **pradėti** jūsų kompiuteryje, tipo **mažmeninės prekybos periferinių simuliatorius**, ir tada pasirinkite programėlę, kai jis pasirodys paieškos rezultatuose. Pradėjus periferinių simuliatorius, spustelėkite įrenginio vardą, jei norite peržiūrėti palaikomus įrenginius. Šie įrenginiai bus nurodytas kaip skirtukų kairėje lango pusėje. Norėdami peržiūrėti konkretų įrenginį, spustelėkite skirtuką įrenginio.

### <a name="line-display-capabilities"></a>Eilutės rodymo galimybes

Eilutės ekranas yra pirmasis įrenginys, kuris yra nurodytas periferinių simuliatorius. Kai sukonfigūruotas virtualus eilutės ekranas, tai rodo eilutės elementų, kaip jie nuskaityti POS sandoryje. Be linijos, ekrane rodomos viso, kad dėl EKA pasirinkus konkursą. Jis taip pat rodo, kad balansas jei pasiūlymas yra įrašytas, tačiau pusiausvyrą vis dar dėl sandorio. Kai POS, nėra naudojama, pranešimas gali būti rodomas rodo, kad kasos nedirba. Turite sukonfigūruoti pranešimas dėl **linija ekrano** FastTab aparatūros profilyje.

### <a name="cash-drawer-capabilities"></a>Grynųjų pinigų stalčių galimybes

Grynųjų pinigų stalčius yra antrasis įrenginys, kuris yra nurodytas periferinių simuliatorius. Kai aparatūros profilis yra sukonfigūruotas naudoti virtualių pinigų stalčiai, Go atsidaro kasos stalčiaus aktyvus SHIFT reaguojant į Stalčiaus operacijas pvz., mokėjimo priemonių deklaravimus, ir, kad kasininkas gali padaryti pakeisti arba piniginį per standartinį cash-and-carry sandorius. Virtualių pinigų stalčiai turi etiketes **Main Stalčiaus** ir **vidurinis stalčius**. Šios etiketės atstovauti stalčių ir stalčių 2 techninės įrangos profilį, atitinkamai. Kai stalčiuje uždaryti, uždaro kasos stalčiaus vaizdas yra rodomas, o mygtuką uždarytas grynųjų pinigų stalčius yra pažymėtas **Atidaryti stalčių**. Jei spustelėsite šį mygtuką, vaizdas pakeitė vaizdą atidarytos kasos stalčiaus, rodo, kad jau atidarytas stalčius. Pažymėti mygtuką atidaryti kasos stalčių **uždaryti stalčių**. Kelių operacijų EKA gali sukelti kasos stalčius atidaryti. Dauguma operacijų negali būti vykdomas, o kasos stalčius. Išimtys yra kai kurios dienos pabaigos procedūrų. Jei POS vartotojas gauna klaidos pranešimą, kuriame teigiama, kad operacijos negalima atlikti, o kasos stalčius, vartotojas turi uždaryti virtualios ir fizinės kasos stalčiaus elgtis. Jei kasos stalčius yra pažymėtas kaip **bendro naudojimo**, techninės įrangos profilį, sistema nėra patikrinti, kad stalčius yra uždarytas prieš operaciją. Veiklos pajamos kaip įprasta, net jei kasos stalčius yra atvira. Taip palaiko scenarijų kai pardavimo darbuotojai dalijasi pinigų stalčiai ir kai vienas bendradarbis naudoja kasos stalčius, o kitos asocijuotos įmonės atlieka nesusijusių užduotis savo POS įrenginys. Pakeitimus, kurie bus atlikti kasos stalčius yra ne akivaizdus iki dabartinio perėjimas yra uždarytas ir atidarytas naujas pamainą.

### <a name="msr-capabilities"></a>MSR galimybes

Periferinė simuliatorius suteikia tvirtą paramą virtualus MSR operacijoms dirbant arba OEKA arba klaviatūros pleišto režimu. OEKA režimas reikalauja, kad MSR būti sukonfigūruotas dirbti kaip OEKA įrenginio aparatūros profilyje. Klaviatūros pleišto režimu tiesiog siunčia klaviatūros pleišto duomenų įvykius į Microsoft Windows. Be skirtumų nustatymo, OEKA ir klaviatūra pleišto režimai skiriasi vienu iš šių būdų:

-   POS klientas leidžia OEKA MSR įrenginių konkrečių scenarijų, pvz., scenarijus, magnetinės juostelės duomenis Lojalumo ar dovanų kortelę įrašo.
-   Klaviatūros pleišto režimu, periferinių simuliatorius siunčia klaviatūros pleišto duomenis į lauką, kuris yra aktyvus, kai duomenys siunčiami. Toks elgesys panašus elgesį, kuris kyla, jei duomenys yra įvesti klaviatūra. Naudoti MSR kaip klaviatūros Klin, vartotojas turi pereiti į mažmeninės prekybos šiuolaikinės POS (MPOS) įsitikinkite, kad teisingai srityje yra gauti duomenys. Todėl, galite konfigūruoti pavėlavus, taip, kad vartotojas turi laiko įsitikinti, kad duomenys bus išsiųstas į tinkamą lauką.

#### <a name="testing-gift-and-payment-card-swipes"></a>Bandymų dovanų ir mokėjimo kortelės Kiepskie alus

Virtualus MSR, taip pat teikianti periferinių simuliatorius leidžia jums konfigūruoti konkrečių MSR duomenų išbandyti dovanų ir mokėjimo kortelės brūkšt scenarijai. Sukurti kortelę, spustelėkite pliuso ženklą (**+**) mygtuką ir pasirinkite kortelės tipą. Tada nurodykite kortelės numerį arba stebėti duomenis, kurie turi būti siunčiami POS, kartu su galiojimo pabaigos mėnesį ir metus už kortelę, kuri jums apibrėžti. Reikšmė, kurią galite pasirinkti, kad **kortelės tipas** laukas yra tik etiketę, kuri gali būti atvaizduota kortelę. Ši žymė lengviau identifikuoti korteles, kai jie yra swiped per periferinių simuliatorius. Jūs galite pasirinkti kortelės, kad sukonfigūruoti periferinių simuliatorius naudojant rodyklę kairėn (**&lt;**) ir rodyklė į dešinę (**&gt;**) mygtukai virš atvaizdo kortelės. Galite redaguoti ir naikinti korteles naudojant į **redaguoti** ir **panaikinti** mygtukus šalia esantį pliuso ženklą (**+**) mygtuką.

### <a name="pin-pad"></a>PIN rinkiklis

Galite konfigūruoti PIN pad simuliatorius imituoti OEKA PIN pad. Su elektroninių pinigų pervedimas (EFT) operaciją yra atliekama EKA ir reikalauja PIN įrašas, aparatūros stotis ragina PIN įrenginiui paraginti įvesti PIN kodą. Dirbti, PIN pad periferinių simuliatorius reikia EFT mokėjimas jungties pagalba.

### <a name="printer"></a>Spausdintuvas

Virtualus periferinių spausdintuvas tik rodo gavimus spausdinamas nuo POS. Jei spausdinimo operaciją kelis kvitus, galite slinkti per įplaukos.

#### <a name="configure-receipt-printing"></a>Kvito spausdinimo konfigūravimas

1.  Eikite į **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros profiliai**.
2.  Pasirinkite techninės įrangos profilį, kurį sukūrėte virtualus periferiniams įrenginiams.
3.  Dėl to **spausdintuvo** FastTab, spustelėkite **redaguoti**.
4.  – Į **gavimo profilio ID** pasirinkite kvitų šabloną.
5.  Click **Save**.

### <a name="scale"></a>Mastelis

Masto produktas yra įtraukta į POS operaciją, ir pagal skalę yra sukonfigūruotas, Go nuskaito svorio skalė. Už virtualios ir fizinės apimties, gaminio ar svoris turėtų būti nurodyta prieš produkto yra įtraukta į operaciją. Prieš pridėdami masto produkto operacijai, eikite į periferinių simuliatorius masto ir naudoti pliuso ženklą (**+**) ir minuso ženklą (**–**) mygtukai būtų suderintas su svoriu, tai skalė turėtų pranešti. Taip pat galite įvesti norimą svorį, tiesiai į **dabartinė vertė** srityje. Galite koreguoti masto svorio vienetais, naudojant pliuso ženklą (**+**), **redaguoti**, ir **panaikinti** mygtukus. Tokiu būdu galima nurodyti vienetai pagal produktų, kurie yra pasverti ar lokalė, kur naudojamas skalės.

#### <a name="configure-a-scale-product"></a>Konfigūruoti masto produktas

1.  Eikite į **mažmeninė ir****prekybos**&gt;**produktų ir kategorijų**&gt;**išleistas produktų kategorijos**.
2.  Atidarykite produkto įrašą.
3.  Pasirinkite produktą pasverti.
4.  Dėl į **mažmeninės prekybos** FastTab, nustatyti į **masto produkto** iš **Nr** į **taip**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Sinchronizuoti kanalo duomenų bazės keitimus

1.  Eikite į **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**.
2.  Pasirinkite į **1040** pasiskirstymo grafikas.
3.  Spustelėkite **surengę** Norėdami sinchronizuoti keitimus su EKA.

Po to, kai duomenys yra sinchronizuojami, kai masto produktas yra įtraukta į POS operaciją, Go patikrina svorį skale.

### <a name="signature-capture"></a>Parašo fiksavimas

Virtualus parašas surinkimo įrenginys paragina vartotoją pateikti parašo virtualus parašas surinkimo padas konkurso, kuris naudojamas reikalauja pasirašyti. Vartotojas sutinka parodyti EKA pasirašymas. Kasininkas gali priimti parašas. Parašas yra tada išsaugotas kartu su paraiška ir sinchronizuojamas su galinis biuras bei kitų sandorių duomenis.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Konkursui vykdyti reikia pasirašyti

1.  Eikite į **mažmeninės prekybos ir prekybos**&gt;**kanalai**&gt;**mažmeninės prekybos parduotuvėse**&gt;**visi mažmeninės prekybos parduotuvėse**.
2.  Pasirinkite mažmeninės prekybos parduotuvėje.
3.  Spustelėkite **Redaguoti**.
4.  Spustelėkite **nustatyti**, ir tada, kad **nustatyti** spustelėkite **mokėjimo būdai**.
5.  Spustelėkite **Redaguoti**.
6.  Pasirinkite mokėjimo būdą, kuris reikalauja parašą.
7.  – Į **bendrojo** skyriuje, kaip **parašo Capture**, nustatyti į **vartojimo pasirašymo įrašymo įrenginys** galimybę **taip**.
8.  – Į **parašas surinkimo minimali suma** įveskite minimalią sumą, kurią turėtų sukelti parašas surinkimo.

#### <a name="synchronize-changes-to-the-channel-database"></a>Sinchronizuoti kanalo duomenų bazės keitimus

1.  Eikite į **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**.
2.  Pasirinkite į **1070** pasiskirstymo grafikas.
3.  Spustelėkite **surengę** Norėdami sinchronizuoti keitimus su EKA.

Po to, kai duomenys yra sinchronizuota, kai pasiūlymas yra naudojama, kad reikia parašo, o suma atitinka parašo ribą, Go ragina pasirašyti virtualų parašas surinkimo įrenginio.

## <a name="additional-configuration"></a>Papildomos konfigūracijos
Galite redaguoti periferinių simuliatorius konfigūracijos failą, siekiant tinkamai išspręsti scenarijų, kurie išbandote. Jūs galite rasti konfigūracijos failą į C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigūracijos failas aprašo vienetai, kuriuos galima atlikti bandymus skalė, kortelės rūšis, kuriuos galima bandyti ir brūkšninių kodų tipai. Pvz., pakeisti teksto reikšmes į konfigūracijos failą, galite pridėti naują kortelės tipą arba matavimo vienetą, kuriame galima pasirinkti vykdymo metu. Naujos reikšmės bus rodomos po programą iš naujo.

## <a name="troubleshooting"></a>Trikčių šalinimas
Veiklos periferinių Simulator prisijungęs per periferinių simuliatorius. Žurnalą galite rasti C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Periferinė simuliatorius taip pat teikia klausimus "Windows" įvykių žurnale, kurį galite gauti **programos ir tarnybų žurnalai**&gt;**"Microsoft"**&gt;**DynamicsAX**. Jei keitimus, atliktus techninės įrangos profilį arba kitose srityse yra ne akivaizdus MPOS arba periferinių simuliatorius, patikrinti platinimo duomenų apsikeitimo valdymo užduotys, kurį naudojote sinchronizuoti duomenis kanalo duomenų bazei. Jei pakeitimai buvo sinchronizuotas, bet vis dar nėra aišku, EKA, paleisti iš naujo kliento POS. Keisti sukonfigūruotą pinigų stalčiai nėra veiksmingi, tol, kol sukuriamas naujas pamainą. Todėl jei pakeičiate pinigų stalčiai, įsitikinkite, kad visada uždaryti esamą perėjimas išbandyti naują pinigų Stalčiaus nustatymą. Kartais, jei gamintojo tvarkyklė po bendros kontrolės objektus nuo Monroe konsultavimo paslaugų, vairuotojas gali sukelti bendrą valdymo objektai gali nustoti tinkamai veikti. Šiuo atveju, reikėtų iš naujo bendro valdymo objektų.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Retail peripherals overview](retail-peripherals-overview.md)


