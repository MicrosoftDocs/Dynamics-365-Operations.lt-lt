---
title: "Biudžeto kontrolės apžvalga"
description: "Šis straipsnis pristato biudžeto kontrolės ir pateikia informaciją, kad padėtų jums nustatyti biudžeto valdymo Microsoft Dynamics 365 operacijoms, kad jūs galite valdyti finansinius išteklius."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60493
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 04e0c066511c1fedf33784944441326201fc2df8
ms.lasthandoff: 03/31/2017


---

# <a name="budget-control-overview"></a>Biudžeto kontrolės apžvalga

Šis straipsnis pristato biudžeto kontrolės ir pateikia informaciją, kad padėtų jums nustatyti biudžeto valdymo Microsoft Dynamics 365 operacijoms, kad jūs galite valdyti finansinius išteklius.

<a name="overview"></a>Apžvalga
--------

Biudžeto kontrolės Microsoft Dynamics 365 operacijoms palaiko valdymo organizacijos finansinių išteklių per diagramos sąskaitas, darbo eigos, vartotojų grupes, šaltinio dokumentų ir žurnalų, konfigūruojama turimas lėšas, biudžeto ciklus ir ribinės vertės apskaičiavimas. Kai naudojami valdikliai, organizacija gali planuoti, matuoti, valdyti ir prognozuoti savo finansinių metų finansinius išteklius. 

Dynamics 365 operacijoms patvirtinus biudžetus, biudžeto planų galite generuoti biudžeto registro įrašus įrašyti biudžeto išlaidų organizacija. Taip pat galite sukurti arba biudžeto registro įrašams importuoti iš trečiųjų šalių programos, o ne naudojant biudžeto planavimo funkcija. 

Išlaidas galima įrašyti naudojant pagrindines sąskaitas ir finansines dimensijas. Bendras išlaidas galima konfigūruoti taip, kad jos atitiktų organizacijos strategijas ir reikalavimus, finansinių dimensijų ir pagrindinių sąskaitų grupavimo kombinacijas. 

Toliau pateikiamoje diagramoje parodyta biudžeto kontrolės vieta įprasto biudžeto ciklo etapuose.

[![BudgetingCycle](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Galite konfigūruoti biudžeto kontrolė atsižvelgiant į kelis veiksnius:

-   **Finansinės dimensijos** – kokias biudžeto ataskaitų ir faktinių sumų finansines dimensijas reikia naudoti ir kokios finansinės dimensijos reikalingos norint kontroliuoti biudžetą? Ar yra konkrečių dimensijų kombinacijų ir pagrindinių sąskaitų, į kurias reikėtų atkreipti dėmesį? Pvz., ar reikia stebėti biudžeto faktines sumas pagal išlaidų centrą ir programą? Ar į kelionės išlaidas reikia atkreipti ypatingą dėmesį?
-   **Laikas** – koks laikotarpis (ataskaitinis laikotarpis, ataskaitinis laikotarpis iki šios dienos ir t.t.) bus naudojamas vertinant turimas biudžeto lėšas?
-   **Šaltinių dokumentų** -kas šaltinio dokumentus reikia įvertinti biudžeto valdymo? Dokumentus reikia įvertinti kiekvienoje eilutėje arba dokumentą?
-   **Turimų lėšų skaičiavimas** – ar skaičiuojant turimas lėšas turėtų būti atsižvelgiama į tokius dokumentus kaip pirkimo paraiškos (preliminarūs biudžeto rezervavimai) ir pirkimo užsakymai (biudžeto rezervavimai)? Ar skaičiuojant turėtų būti atsižvelgiama į juodraštinius dokumentus?
-   **Nepaisymo teisės** – kas turi teisę viršyti leistiną biudžetą?

Biudžeto kontrolė yra visiškai integruota su Dynamics 365 operacijoms. Todėl galite įvertinti ir suplanuotų pirkimų, ir faktinių pirkimų galimą biudžetą. Prieinamos biudžeto užklausos ir ataskaitos. Todėl vartotojai gali įvertinti biudžetą pagal biudžeto ciklą ir biudžeto tikslinimų arba perkėlimų formoje atlikti reikiamus koregavimus. Biudžeto vadybininkas taip pat gali eksportuoti biudžetą ir faktines sumas į „Microsoft Excel“, kad pagal poreikį galėtų geriau analizuoti ir pateikti prognozę.

## <a name="configuring-budget-control"></a>Biudžeto kontrolės konfigūravimas
### <a name="budget-cycle-time-span"></a>Biudžeto ciklo trukmė

Sukonfigūravę pagrindinį biudžetą, puslapyje **Biudžeto ciklo trukmė** galite nurodyti laiką arba biudžeto sudarymo ir biudžeto kontrolės pradžios ir pabaigos laikotarpius. Biudžeto ciklai dažnai atitinka finansinius kalendorius, tačiau gali apimti finansinius metus.

Tolesni veiksmai konfigūracijos duomenys įrašyti į įvairias skirtukų į **biudžeto kontrolės konfigūracijos** puslapis.

### <a name="define-parameters"></a>Nustatyti parametrus

Atsižvelgdami į galimas biudžeto finansines dimensijas, biudžeto kontrolei galite naudoti visas finansines dimensijas arba jų pogrupį. 

Be to, galite nurodyti numatytąjį laiko intervalą (pvz., **Finansiniai metai**, ** Finansiniai metai iki šios dienos**, **Ataskaitinis laikotarpis** arba **Kas ketvirtį**), kurio biudžeto kontrolė bus atlikta per susijusio biudžeto ciklo trukmę. Taip pat galite nurodyti numatytąjį biudžeto vadybininką ir ribinę vertę, kuri naudojama pranešti vartotojams, kai pasiekiama ribinė reikšmė. Vertės šiuose laukuose bus naudojamos kaip numatytosios vertės bet kurioje naujai sukurtoje biudžeto kontrolės taisyklėje arba biudžeto grupėje. Tačiau numatytąsias vertes galima keisti atskiroms grupėms arba taisyklėms. 

Biudžetų kūrimo ir įrašymo į biudžeto registrą būdas padeda nustatyti trukmę, kuri pasirenkama įvertinus turimas biudžeto lėšas. Jei sukuriama ir naudojama dimensijos reikšmės kombinacijos metinė suma, tada gali būti tinkamesnis požiūris pagal finansinius metus arba finansinius metus iki šios dienos. Tačiau jei organizacija, sukurianti biudžetą pagal ataskaitinį laikotarpį arba paskirstanti į ataskaitinius laikotarpius nori išsamesnės kontrolės, galbūt jai reikėtų pabandyti finansinio laikotarpio iki šios dienos arba ketvirčio trukmę. 

Be to, kadangi organizacijos kultūra susijusi su biudžeto sudarymu ir biudžeto kontrole, ji padeda nustatyti konfigūraciją.

### <a name="over-budget-permissions"></a>Biudžeto viršijimo teisės

Toliau skirtuke **Biudžeto viršijimo teisės** galite nurodykite vartotojų grupes. Taip pat galite nurodyti, ar grupės nariais esantys vartotojai, turi teisę viršyti biudžetą. Galite neleisti vartotojams viršyti biudžeto ribinės reikšmės, kuri buvo nustatyta puslapyje **Biudžeto parametrai**, arba galite neleisti jiems viršyti biudžeto tam tikra suma, neatsižvelgiant į ribinę reikšmę. Atsižvelgiant į tai, kaip aktyviai organizacija valdo savo išlaidas, šios teisės gali jai padėti valdyti savo finansinius išteklius. 

### <a name="budget-funds-available"></a>Turimos biudžeto lėšos

Toliau skirtuke **Turimos biudžeto lėšos** galite nustatyti formulę, naudojamą turimoms biudžeto lėšoms apskaičiuoti. Atsižvelgiant į tai, kaip konservatyviai organizacija valdo savo finansinius išteklius, arba pagal taisykles ir pramoninius reikalavimus, į skaičiavimą gali būti įtraukti juodraštiniai arba neužregistruoti dokumentai. 

> [!NOTE] 
> Jei apskaičiuojant yra pakeista biudžeto ciklo metu, keitimai nebus jokių dokumentų, anksčiau priėmė biudžeto valdymo patikrinimus, ir kuri buvo paskelbta arba baigti.

### <a name="documents-and-journals"></a>Dokumentai ir žurnalai

Toliau skirtuke **Dokumentai ir žurnalai** galite pasirinkti, kuriems šaltinio dokumentams ir žurnalams bus taikomi biudžeto kontrolės patikrinimai, ir tai, ar bus tikrinama eilutės įrašo ar viso dokumento lygiu. 

Turite sugretinti šaltinio dokumentus, kurių žymės langeliai pažymėti balansams, įtraukiamiems į turimų biudžeto lėšų skaičiavimą. Pavyzdžiui, jei pasirinkote **Biudžeto rezervavimai**, turite pasirinkti pasirinktį **Pirkimo užsakymai**. Atlikus pirkimo eilutės sumoms ir sąskaitoms taikomą biudžeto patikrą, rezervavimui priskiriama biudžeto kontrolės kategorija **Biudžeto rezervavimas**. Atlikus pirkimo paraiškos sumoms ir sąskaitoms taikomą biudžeto patikrą, rezervavimui priskiriama biudžeto kontrolės kategorija **Preliminarus biudžeto rezervavimas**. 

Jei **Biudžeto rezervavimas** ir / arba **Preliminarus biudžeto rezervavimas** įtrauktas į turimų biudžeto lėšų skaičiavimą ir turi atsispindėti didžiosios knygos registravimo įrašuose, puslapyje **Didžiosios knygos parametrai** turite įgalinti įsipareigojimų apskaitą.  

### <a name="assign-budget-models"></a>Priskirti biudžeto modelius

Toliau skirtuke **Biudžeto modelių priskyrimas** priskirkite biudžeto modelius į biudžeto kontrolę įtrauktinoms biudžeto ciklo trukmėms.

### <a name="define-budget-control-rules"></a>Nustatyti biudžeto valdymo taisykles

Toliau skirtuke **Biudžeto kontrolės taisyklių nustatymas** pagal finansines dimensijas, kurios įgalintos biudžeto kontrolei, turite sukurti konkrečias taisykles. Pvz., jei dėmesys sutelkiamas į skyriaus išlaidas arba išlaidų intervalą, galite šias išlaidas apibrėžti ir įvertinti naudodami šio skirtuko parametrus. Kiekvienai biudžeto valdymo taisyklei galite apibrėžti skirtingas ribines reikšmes. 

> [!Important]
> Biudžeto kontrolė bus įjungtas pagrindinis abonementas, ir **pelno ir nuostolio**, **išlaidų**, **pajamų, balanse, atsakomybės, akcijų** ar **turto** tipo. Jei šiame skirtuke yra taisyklė, kurioje yra tuščias kriterijus, biudžeto kontrolė bus įgalinta **visoms **finansinių dimensijų kombinacijoms, kuriose įtrauktos šių tipų pagrindinės sąskaitos. Todėl įsitikinkite, kad jūsų sukurtos biudžeto kontrolės taisyklės apibrėžia tik tuos finansinių dimensijų kombinacijų, kuriose svarbu įjungti biudžeto kontrolę, intervalus.  

### <a name="select-main-accounts"></a>Pasirinkti pagrindines sąskaitas

Jei **Pagrindinė sąskaita** nepažymėta kaip biudžeto valdymo dimensija puslapyje **Apibrėžti parametrus**, bet konkrečios išlaidos, galite pasirinkti šias išlaidas skirtuke **Pasirinkti pagrindines sąskaitas**. Jei **Pagrindinė sąskaita** pažymėta kaip biudžeto kontrolės dimensija, nebūtini jokie įrašai.  

### <a name="define-budget-groups"></a>Nustatyti biudžeto grupes

Toliau skirtuke **Apibrėžti biudžeto grupes** galite pasirinktinai apibrėžti finansinių dimensijų, kur biudžeto ištekliai bus kaupiami antrinei biudžeto patikrai atlikti, unikalias kombinacijas. Galite sukurti vieną įrašą, kuriame yra visa organizacija arba galite nurodyti kelias atskirus padalinius arba išlaidų centrus atitinkančias grupes.  

### <a name="define-message-levels"></a>Nustatyti pranešimų lygius

Jei biudžeto kontrolės įspėjimo pranešimus reikia sulaikyti kuriai nors vartotojų grupei, šias grupes galite nurodyti puslapyje **Pranešimų lygių apibrėžimas**. Vartotojų grupių nariai ir toliau gaus klaidos pranešimus, kai pagal biudžeto viršijimo teises viršys turimas biudžeto lėšas.

### <a name="activate-budget-control"></a>Suaktyvinti biudžeto kontrolę

Po to, kai biudžeto kontrolės sukonfigūruota, galite ją įjungti ir suaktyvinti skirtuke **Biudžeto kontrolės suaktyvinimas**. Tada įsigalios juodraštinė versija.
> [!Important]
> Po to, kai biudžeto kontrolę, yra įjungtas ir aktyvus, o po to, kai registruojamos operacijos, ji turėtų būti išjungiama metų viduryje. Kai biudžeto kontrolė išjungta, veiklos nėra įrašomos biudžeto kontrolės tikslais, o biudžeto patikrinimai nebeatliekami. Todėl dokumentai, kurie jau buvo užregistruoti, su biudžeto kontrole susijusiose užklausose ir ataskaitose sumažinimo sumos arba balansai gali būti neteisingai atspindėti. Tai apima bet kokių atsisiuntimų arba dokumentų ir žurnalų koregavimo biudžeto kontrolės statistiką. 

Be to, atkreipkite dėmesį, kad prieš įjungiant biudžeto kontrolę užregistruotos operacijos, įskaitant biudžeto registro įrašus, nesvarstomos atliekant biudžeto kontrolę. Todėl biudžeto kontrolę įjungti rekomenduojama tik naujo biudžeto ciklo pradžioje. Įsitikinkite, kad biudžeto registro įrašuose, kuriuose nurodomi biudžeto kontrolės pradžios biudžeto balansai, biudžeto balansai atnaujinami tik įjungus biudžeto kontrolę. Bus patikrintos bet kurio atidaryto dokumento (pvz., pirkimo užsakymo) turimos biudžeto lėšos ir bus suteikiama biudžeto rezervacija, skirta biudžeto kontrolei, kai vartotojas pats dokumente pažymi biudžeto kontrolės žymės langelį.

## <a name="using-budget-control"></a>Biudžeto kontrolės naudojimas
Kai biudžeto kontrolė įjungta, dokumentuose, kuriuose sukonfigūruota biudžeto kontrolė, vartotojai gaus biudžeto kontrolės įspėjimo ir klaidos pranešimus. Atminkite, kad biudžeto kontrolę galite konfigūruoti taip, kad vartotojai būtų įspėti, kai jie viršija biudžeto lėšas, bet vis dar gali patvirtinti arba registruoti operaciją. Išsamią nepavykusių biudžeto patikrinimų informaciją vartotojai gali peržiūrėti puslapyje **Biudžeto patikrinimo klaidos ir įspėjimai**.   

Iš šio puslapio vartotojai gali gręžti į **biudžeto kontrolės statistinius duomenis pagal laikotarpį** puslapis peržiūrėti biudžeto galimybes išsamią informaciją ir rezervuoti pasirinktą biudžeto kontrolės dimensijų derinys. Vartotojai taip pat gali detalizuoti puslapį **Biudžeto kontrolės statistika ** norėdami peržiūrėti biudžeto tinkamumą visoms finansinių dimensijų kombinacijoms, kurios naudojamos biudžeto kontrolėje. 

Jei biudžeto kontrolė įjungta pirkimo užsakymams, biudžeto vadybininkas gali naudodamas darbo sritį **Didžiosios knygos biudžetai ir prognozės** norėdamas peržiūrėti visų nepatvirtintų pirkimo užsakymų, turinčių biudžeto patikros įspėjimų ir klaidų, eilę. Jei biudžeto vadybininkui sukonfigūruotos biudžeto viršijimo teisės, jis / ji gali patvirtinti pirkimo užsakymus tiesiogiai darbo srityje.    


