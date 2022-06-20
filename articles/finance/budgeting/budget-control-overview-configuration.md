---
title: Biudžeto kontrolės apžvalga
description: Šiame straipsnyje pristatyta biudžeto kontrolės funkcija ir pateikiama informacija, kuri padės jums konfigūruoti biudžeto kontrolę, kad būtų optimizuotas jūsų organizacijos finansinių išteklių valdymas.
author: panolte
ms.date: 03/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27eb31919937e7f43a785616b547e3d6952eaaf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898304"
---
# <a name="budget-control-overview"></a>Biudžeto kontrolės apžvalga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pristatyta biudžeto kontrolės funkcija ir pateikiama informacija, kuri padės jums konfigūruoti biudžeto kontrolę, kad būtų optimizuotas jūsų organizacijos finansinių išteklių valdymas.

Biudžeto kontrolė palaiko organizacijos finansinių išteklių valdymą sąskaitų planas, darbo eiga, vartotojų grupės, šaltinio dokumentai ir žurnalai, konfigūruojamas galimų lėšų skaičiavimas, biudžeto ciklai ir ribinės vertės. Kai naudojami valdikliai, organizacija gali planuoti, matuoti, valdyti ir prognozuoti savo finansinių metų finansinius išteklius. 

Patvirtinus biudžetus sistemoje, galite naudoti biudžeto planus generuoti biudžeto registro įrašams, jei norite įrašyti organizacijos biudžeto išlaidas. Kitu atveju, galite sukurti biudžeto registro įrašus ar importuoti juos iš trečiosios šalies programos nenaudodami biudžeto planavimo funkcijos. 

Išlaidas galima įrašyti naudojant pagrindines sąskaitas ir finansines dimensijas. Bendras išlaidas galite konfigūruoti taip, kad jos atitiktų organizacijos strategijas ir reikalavimus grupuodami finansinių dimensijų ir pagrindinių sąskaitų kombinacijas. 

Toliau pateikiamoje diagramoje parodyta biudžeto kontrolės vieta įprasto biudžeto ciklo etapuose.

[![Įprastas biudžeto sudarymo ciklas.](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Galite konfigūruoti biudžeto kontrolę, atsižvelgdami į keletą veiksnių.

- **Finansinės dimensijos** – Kokias biudžeto ataskaitų ir faktinių sumų finansines dimensijas reikia naudoti ir kokios finansinės dimensijos reikalingos biudžetų valdymui? Ar yra konkrečių dimensijų kombinacijų ir pagrindinių sąskaitų, į kurias reikėtų atkreipti dėmesį? Pvz., ar reikia stebėti biudžeto faktines sumas pagal išlaidų centrą ir programą? Ar į kelionės išlaidas reikia atkreipti ypatingą dėmesį?
- **Laikas** – koks laikotarpis (ataskaitinis laikotarpis, ataskaitinis laikotarpis iki šios dienos ir t.t.) bus naudojamas vertinant turimas biudžeto lėšas?
- **Šaltinio dokumentai** – kokius biudžeto kontrolės šaltinio dokumentus reikia įvertinti? Ar reikėtų įvertinti kiekvieną dokumentų eilutę, ar visą dokumentą?
- **Turimų lėšų skaičiavimas** – ar skaičiuojant turimas lėšas turėtų būti atsižvelgiama į tokius dokumentus kaip pirkimo paraiškos (preliminarūs biudžeto rezervavimai) ir pirkimo užsakymai (biudžeto rezervavimai)? Ar skaičiuojant turėtų būti atsižvelgiama į juodraštinius dokumentus?
- **Nepaisymo teisės** – kas turi teisę viršyti leistiną biudžetą?

Biudžeto kontrolė visiškai integruota į programą. Todėl galite įvertinti ir suplanuotų pirkimų, ir faktinių pirkimų galimą biudžetą. Prieinamos biudžeto užklausos ir ataskaitos. Todėl vartotojai gali įvertinti biudžetą pagal biudžeto ciklą ir biudžeto tikslinimų arba perkėlimų formoje atlikti reikiamus koregavimus. Biudžeto vadybininkas taip pat gali eksportuoti biudžetą ir faktines sumas į „Microsoft Excel“, kad pagal poreikį galėtų geriau analizuoti ir pateikti prognozę.

## <a name="configuring-budget-control"></a>Biudžeto kontrolės konfigūravimas

### <a name="budget-cycle-time-span"></a>Biudžeto ciklo trukmė

Sukonfigūravę pagrindinį biudžetą, puslapyje **Biudžeto ciklo trukmė** galite nurodyti laiką arba biudžeto sudarymo ir biudžeto kontrolės pradžios ir pabaigos laikotarpius. Biudžeto ciklai dažnai atitinka finansinius kalendorius, tačiau gali apimti finansinius metus.

Kiti konfigūracijos veiksmai atliekami skirtukuose, atidaromuose iš **Biudžeto kontrolės konfigūracija** puslapio.

### <a name="define-parameters"></a>Nustatyti parametrus

Atsižvelgdami į galimas biudžeto finansines dimensijas, biudžeto kontrolei galite naudoti visas finansines dimensijas arba jų pogrupį. 

Taip pat, galite nurodyti numatytąjį laiko intervalą (pavyzdžiui, **Finansiniai metai**, **Finansiniai metai iki tam tikros dienos**, **Ataskaitinis laikotarpis** arba **Kas ketvirtį**), kuriuo biudžeto kontrolė bus vykdoma per susijusio biudžeto laikotarpį. Taip pat galite nurodyti numatytąjį biudžeto vadybininką ir ribinę vertę, kuri naudojama pranešti vartotojams, kai pasiekiama ribinė reikšmė. Vertės šiuose laukuose bus naudojamos kaip numatytosios vertės bet kurioje naujai sukurtoje biudžeto kontrolės taisyklėje arba biudžeto grupėje. Tačiau numatytąsias vertes galima keisti atskiroms grupėms arba taisyklėms. 

Biudžetų kūrimo ir įrašymo į biudžeto registrą būdas padeda nustatyti trukmę, kuri pasirenkama įvertinus turimas biudžeto lėšas. Jei sukuriama ir naudojama dimensijos reikšmės kombinacijos metinė suma, tada gali būti tinkamesnis požiūris pagal finansinius metus arba finansinius metus iki šios dienos. Tačiau jei organizacija, sukurianti biudžetą pagal ataskaitinį laikotarpį arba paskirstanti į ataskaitinius laikotarpius nori išsamesnės kontrolės, galbūt jai reikėtų pabandyti finansinio laikotarpio iki šios dienos arba ketvirčio trukmę. 

Taip pat, kadangi organizacijos kultūra susijusi su biudžeto sudarymu ir kontrole, ji padeda nustatyti konfigūraciją.

### <a name="over-budget-permissions"></a>Biudžeto viršijimo teisės

Toliau skirtuke **Biudžeto viršijimo teisės** galite nurodykite vartotojų grupes. Taip pat galite nurodyti, ar grupės nariais esantys vartotojai, turi teisę viršyti biudžetą. Galite neleisti vartotojams viršyti biudžeto ribinės reikšmės, kuri buvo nustatyta puslapyje **Biudžeto parametrai**, arba galite neleisti jiems viršyti biudžeto tam tikra suma, neatsižvelgiant į ribinę reikšmę. Atsižvelgiant į tai, kaip aktyviai organizacija valdo savo išlaidas, šios teisės gali jai padėti valdyti savo finansinius išteklius. 

### <a name="budget-funds-available"></a>Turimos biudžeto lėšos

Toliau skirtuke **Turimos biudžeto lėšos** galite nustatyti formulę, naudojamą turimoms biudžeto lėšoms apskaičiuoti. Atsižvelgiant į tai, kaip konservatyviai organizacija valdo savo finansinius išteklius, arba pagal taisykles ir pramoninius reikalavimus, į skaičiavimą gali būti įtraukti juodraštiniai arba neužregistruoti dokumentai. 

> [!NOTE]
> Jei skaičiavimas modifikuojamas biudžeto ciklo metu, pakeitimai neturės įtakos jokiams dokumentams, kurie anksčiau atliko biudžeto kontrolės patikrinimus ir buvo užregistruoti arba baigti. Naudojant funkciją, kuri pavadinta **Tik** sekimo sumos, galimų biudžeto lėšų apskaičiavime galima keisti duomenis, kurie duomenys sekami budgetSourceTracking lentelėse. Kai ši funkcija įjungta, sumos saugomos tik tada, jei jos yra pasirinktos naudoti galimame biudžeto lėšų skaičiavime. Daugiau informacijos rasite turimas [biudžeto lėšas](budget-funds-available.md).

### <a name="documents-and-journals"></a>Dokumentai ir žurnalai

Skirtuke **Dokumentai ir žurnalai** galite pasirinkti, kuriems šaltinio dokumentams ir žurnalams bus taikomi biudžeto kontrolės tikrinimai ir ar čekiai bus atliekami eilutės įrašo lygiu ar visame dokumente. Be to, nauja biudžeto kontrolės dokumentų filtravimo patobulinimo priemonė, **·** Microsoft Dynamics kuri yra pagal 365 finansų 10.0.27 versiją, pateikia užklausa pagrįstą filtro pasirinktį kiekvienam dokumentui, kuris įtrauktas į biudžeto kontrolę. Todėl galite nurodyti, kurių biudžeto kontrolės dokumentų biudžetas tikrinamas. Tokiu būdu priemonė įgalina tikrinti tik dokumento tipo subgrupį. Pavyzdžiui, galite patikrinti tik pirkimo užsakymus, kurių **telkinio** laukas nustatytas kaip **01**. Naujas stulpelis, kuris įtrauktas į dokumentų **ir žurnalų** skirtuką, nurodo, ar pasirinktam dokumentų tipui nustatyta užklausa. Be to, du nauji mygtukai, įtraukti į įrankių juostą virš dokumentų tinklelio, leidžia pridėti, redaguoti arba naikinti filtravimą. 

Turite sugretinti šaltinio dokumentus, kurių žymės langeliai pažymėti balansams, įtraukiamiems į turimų biudžeto lėšų skaičiavimą. Pavyzdžiui, jei pasirinkote **Biudžeto rezervavimai**, turite pasirinkti pasirinktį **Pirkimo užsakymai**. Atlikus pirkimo eilutės sumoms ir sąskaitoms taikomą biudžeto patikrą, rezervavimui priskiriama biudžeto kontrolės kategorija **Biudžeto rezervavimas**. Atlikus pirkimo paraiškos sumoms ir sąskaitoms taikomą biudžeto patikrą, rezervavimui priskiriama biudžeto kontrolės kategorija **Preliminarus biudžeto rezervavimas**. 

Jei **Biudžeto rezervavimas** ir (arba) **Preliminarus biudžeto rezervavimas** yra įtrauktas į turimų biudžeto lėšų skaičiavimą ir turi atsispindėti didžiosios knygos registravimo įrašuose, puslapio **Didžiosios knygos** parametrai grupėje **Įsipareigojimų apskaita** turite pažymėti šiuos pasirinkimus.

### <a name="assign-budget-models"></a>Priskirti biudžeto modelius

Toliau skirtuke **Biudžeto modelių priskyrimas** priskirkite biudžeto modelius į biudžeto kontrolę įtrauktinoms biudžeto ciklo trukmėms.

### <a name="define-budget-control-rules"></a>Nustatyti biudžeto valdymo taisykles

Toliau skirtuke **Biudžeto kontrolės taisyklių nustatymas** pagal finansines dimensijas, kurios įgalintos biudžeto kontrolei, turite sukurti konkrečias taisykles. Pvz., jei dėmesys sutelkiamas į skyriaus išlaidas arba išlaidų intervalą, galite šias išlaidas apibrėžti ir įvertinti naudodami šio skirtuko parametrus. Kiekvienai biudžeto valdymo taisyklei galite apibrėžti skirtingas ribines reikšmes. 

> [!Important]
> Biudžeto kontrolė bus įgalinta bet kuriai tipo **Pelnas ir nuostolis**, **Išlaidos**, **Įplaukos, Balansas, Įsipareigojimai, Kapitalas** arba **Turtas** pagrindinei sąskaitai. Jei **Apibrėžti biudžeto kontrolės taisykles** skirtuke yra taisyklė, kurioje yra tuščias kriterijus, biudžeto kontrolė bus įgalinta **visoms** finansinių dimensijų kombinacijoms, kuriose įtrauktos šių tipų pagrindinės sąskaitos. Todėl įsitikinkite, kad jūsų sukurtos biudžeto kontrolės taisyklės apibrėžia tik tuos finansinių dimensijų kombinacijų, kuriose svarbu įjungti biudžeto kontrolę, intervalus.

### <a name="select-main-accounts"></a>Pasirinkti pagrindines sąskaitas

Jei **Pagrindinė sąskaita** nepažymėta kaip biudžeto valdymo dimensija puslapyje **Apibrėžti parametrus**, bet valdomos konkrečios išlaidos, galite pasirinkti šias išlaidas skirtuke **Pasirinkti pagrindines sąskaitas**. Jei kaip biudžeto kontrolės dimensija pažymėta **Pagrindinė sąskaita**, nebūtini jokie įrašai.

### <a name="define-budget-groups"></a>Nustatyti biudžeto grupes

Toliau skirtuke **Apibrėžti biudžeto grupes** galite pasirinktinai apibrėžti finansinių dimensijų, kur biudžeto ištekliai bus kaupiami antrinei biudžeto patikrai atlikti, unikalias kombinacijas. Galite sukurti vieną įrašą, kuriame yra visa organizacija arba galite nurodyti kelias atskirus padalinius arba išlaidų centrus atitinkančias grupes.

### <a name="define-message-levels"></a>Nustatyti pranešimų lygius

Jei biudžeto kontrolės įspėjimo pranešimus reikia sulaikyti kuriai nors vartotojų grupei, šias grupes galite nurodyti puslapyje **Pranešimų lygių apibrėžimas**. Vartotojų grupių nariai ir toliau gaus klaidos pranešimus, kai pagal biudžeto viršijimo teises viršys turimas biudžeto lėšas.

### <a name="activate-budget-control"></a>Suaktyvinti biudžeto kontrolę

Po to, kai biudžeto kontrolė sukonfigūruota, galite ją įjungti ir suaktyvinti skirtuke **Biudžeto kontrolės suaktyvinimas**. Tada įsigalios juodraštinė versija.

> [!Important]
> Kai biudžeto kontrolė įjungta ir suaktyvinta ir po to, kai operacijos registruotos, metų viduryje jos išjungti negalima. Kai biudžeto kontrolė išjungta, veiklos nėra įrašomos biudžeto kontrolės tikslais, o biudžeto patikrinimai nebeatliekami. Todėl dokumentai, kurie jau buvo užregistruoti, su biudžeto kontrole susijusiose užklausose ir ataskaitose sumažinimo sumos arba balansai gali būti neteisingai atspindėti. Tai apima bet kokių atsisiuntimų arba dokumentų ir žurnalų koregavimo biudžeto kontrolės statistiką. 

Be to, atkreipkite dėmesį, kad prieš įjungiant biudžeto kontrolę užregistruotos operacijos, įskaitant biudžeto registro įrašus, nesvarstomos atliekant biudžeto kontrolę. Todėl biudžeto kontrolę įjungti rekomenduojama tik naujo biudžeto ciklo pradžioje. Įsitikinkite, kad biudžeto registro įrašuose, kuriuose nurodomi biudžeto kontrolės pradžios biudžeto balansai, biudžeto balansai atnaujinami tik įjungus biudžeto kontrolę. Bus patikrintos bet kurio atidaryto dokumento (pvz., pirkimo užsakymo) turimos biudžeto lėšos ir bus suteikiama biudžeto rezervacija, skirta biudžeto kontrolei, kai vartotojas pats dokumente pažymi biudžeto kontrolės žymės langelį.

## <a name="using-budget-control"></a>Biudžeto kontrolės naudojimas
Kai biudžeto kontrolė yra įjungta, jūs gaus biudžeto kontrolės įspėjimo ir klaidos pranešimus dokumentuose ir žurnaluose, kuriuose sukonfigūruota biudžeto kontrolė. Atminkite, kad biudžeto kontrolę galite konfigūruoti taip, kad vartotojai būtų įspėti, kai jie viršija biudžeto lėšas, bet vis dar gali patvirtinti arba registruoti operacijas. Išsamią nepavykusių biudžeto patikrinimų informaciją galite peržiūrėti puslapyje **Biudžeto patikrinimo klaidos ir įspėjimai**.

Iš šio puslapio vartotojai gali detalizuoti puslapį **Biudžeto kontrolės statistika pagal laikotarpį** norėdami peržiūrėti biudžeto tinkamumo informaciją ir pasirinktos biudžeto valdymo dimensijos kombinacijos rezervacijas. Vartotojai taip pat gali detalizuoti puslapį **Biudžeto kontrolės statistika** norėdami peržiūrėti biudžeto tinkamumą visoms finansinių dimensijų kombinacijoms, kurios naudojamos biudžeto kontrolėje. 

Jei biudžeto kontrolė įjungta pirkimo užsakymams, biudžeto vadybininkas gali naudodamas darbo sritį **Didžiosios knygos biudžetai ir prognozės** norėdamas peržiūrėti visų nepatvirtintų pirkimo užsakymų, turinčių biudžeto patikros įspėjimų ir klaidų, eilę. Jei biudžeto vadovui sukonfigūruotos biudžeto viršijimo teisės, pirkimo užsakymai gali būti patvirtinami tiesiogiai darbo srityje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
