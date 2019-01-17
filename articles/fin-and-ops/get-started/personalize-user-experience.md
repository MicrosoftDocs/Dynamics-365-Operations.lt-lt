---
title: Vartotojo patirties personalizavimas
description: "Šiame straipsnyje paaiškinama, kaip galite personalizuoti „Microsoft Dynamics 365 for Finance and Operations‟."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7344f460fcb443a78b254e2387fbf5c9134bf674
ms.openlocfilehash: 1860b603f789aabca1ca58848a88e11a6e08e31f
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---

# <a name="personalize-the-user-experience"></a>Vartotojo patirties personalizavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip galite personalizuoti „Microsoft Dynamics 365 for Finance and Operations‟.

Yra trys pagrindinės „Dynamics 365 for Finance and Operations“ personalizavimo klasės.

- Sąrankos puslapyje atliekamas personalizavimas. Prie pavyzdžių priskiriama spalvų tema ir laiko juosta.
- Su puslapio naudojimu susijęs personalizavimas, vadinamas *netiesioginiu* personalizavimu. Pavyzdžiui, „Finance and Operations“ seka jūsų keičiamą tinklelio stulpelių plotį ir „FastTab“ sutrauktą arba išplėstą būseną.
- Personalizavimas, kurį atlieka vartotojas, norėdamas keisti puslapio išvaizdą pakeisdamas tai, kaip rodomas ar veikia to puslapio elementas, dažnai naudojantis interaktyvaus personalizavimo režimu. Toks personalizavimas vadinamas *tiesioginiu* personalizavimu. Pavyzdžiui, vartotojas gali įterpti elementų, juos slėpti arba keisti jų išdėstymo tvarką puslapyje.

Visi personalizavimo parametrai, kuriuos nustato „Finance and Operations“ vartotojas, taikomi tik tam vartotojui, nepriklausomai nuo personalizavimo tipo ir nuo to, su kokia įmone šiuo sąveikauja vartotojas. Vieno vartotojo atlikti puslapio keitimai neturi įtakos kitiems sistemos vartotojams.

## <a name="system-wide-options-for-the-current-user"></a>Dabartinio vartotojo visos sistemos parinktys

Puslapyje **Vartotojo parinktys** pateikiama keletas visos sistemos dabartinio vartotojo parametrų. Norėdami atidaryti puslapį **Vartotojo parinktys**, naršymo juostoje paspauskite meniu **Parametrai** (krumpliaračio simbolis), o po to paspauskite **Vartotojo parinktys**. Puslapyje **Vartotojo parinktys** yra keturi skirtukai, kuriuose nurodomi įvairūs vartotojo parametrai.

- **Vaizdas**: pasirinkite puslapio elementų spalvų temą ir numatytąjį dydį.
- **Nuostatos**: pasirinkite numatytąsias vertes, kurios naudojamos kaskart atidarius „Finance and Operations“. Prie šių verčių priskiriama įmonė, pradinis puslapis ir numatytasis rodymo / redagavimo režimas. (Naudojantis rodymo / redagavimo režimu nustatoma, ar puslapis užrakintas peržiūrai, ar galima jį redaguoti kiekvieną kartą atidarius). Šiame skirtuke taip pat yra kalbos, laiko juostos, datos, laiko ir numerio formato parinktys. Galiausiai šiame skirtuke yra keletas papildomų kiekviename leidime skirtingų nuostatų.
- **Paskyra**: koreguokite vartotojo vardą ir kitas su paskyra susijusias parinktis.
- **Darbo eiga**: pasirinkite su darbo eiga susijusias parinktis.

## <a name="implicit-personalizations"></a>Netiesioginis personalizavimas

Netiesioginis personalizavimas atliekamas tiesiog sąveikaujant su tam tikrais valdikliais, kurie „įsimeną“ savo esamą matomą būseną.

- **Tinklelio stulpeliai**: galite koreguoti tinklelio stulpelio plotį, kairėje arba dešinėje stulpelio antraštės pusėje pasirinkdami dydžio keitimo juostą ir slinkdami ją į kairę arba į dešinę, kol stulpelis bus reikiamo pločio. „Finance and Operations“ saugomas nustatytas stulpelio plotis. Tada, kiekvieną kartą atidarius puslapį, kuriame yra tas tinklelis, pakeičiamas stulpelio dydis.
- **„FastTabs“**: kai kuriuose puslapiuose yra išplečiamos dalys, vadinamos *„FastTabs“*. „Finance and Operations“ saugoma informacija apie išplėstus ir sutrauktus „FastTabs“. Tada, kiekvieną kartą sugrįžus į puslapį, tie patys „FastTabs“ išplečiami arba sutraukiami, priklausomai nuo paskutinės sąveikos su puslapiu. Kai kuriais atvejais sutraukus „FastTab“ galima padidinti sistemos efektyvumą, nes „Finance and Operations“ nereikia nuskaityti to „FastTab“ informacijos, kol „FastTab“ neišskleistas. Kaip vėliau paaiškinta šioje temoje, taip pat galite keisti puslapio „FastTabs“ tvarką.
- **„Fact Boxes“**: kai kuriuose puslapiuose yra dalis, vadinama *„Fact Box“ sritimi*. Šioje srityje yra tik skaityti skirta informacija, kuri susijusi su dabartine puslapio tema. Kiekviena „Fact Box“ srities dalis vadinama *„Fact Box“*. Galite slėpti arba rodyti visą „Fact Box“ sritį, taip pat galite išplėsti arba sutraukti atskiras „Fact Boxes“. „Finance and Operations“ saugomos jūsų nuostatos. Tada, kiekvieną kartą grįžus į puslapį, priklausomai nuo paskutinės sąveikos su puslapiu, atkuriama „Fact Box“ srities būsena ir atskiri „Fact Boxes“. Kai kuriais atvejais sutraukus „Fact Box“ galima padidinti sistemos efektyvumą, nes „Finance and Operations“ nereikia nuskaityti to „Fact Box“ informacijos, kol „Fact Box“ neišskleistas.
- **Veiksmų sritys**: šalia daugelio puslapių viršaus rodoma *Veiksmų sritis*. Veiksmų srityje yra daugeliui dabartiniame puslapyje galimų atlikti veiksmų skirtų mygtukų. Šie mygtukai skirtukuose dažnai sisteminami. Pagal numatytuosius parametrus galite prisegti visą atidarytą veiksmų sritį arba galite ją sutraukti. Tada, kitą kartą atidarius puslapį, „Finance and Operations“ atkuria prisegtą veiksmų srities būseną. Jei veiksmų sritis prisegama atverta, „Finance and Operations“ taip pat rodo paskutinių naudotų veiksmų skirtuką.
- **„QuickFilters“**: virš daugelio tinklelių rodomas *„QuickFilter“*. Naudodamiesi „QuickFilter“ galite filtruoti tinklelį pagal pasirinktą stulpelį. „Finance and Operations“ saugomas filtruojamas stulpelis. Tada, kitą kartą atidarius puslapį, kuriame yra tas tinklelis, tinklelis bus filtruojamas tame pačiame stulpelyje. Tačiau po to galite filtruoti kito stulpelio tinklelį.
- **Stulpelio antraštės filtrai**: jei filtruodami tinklelį naudojate *stulpelio antraštės filtrus*, norėdami rasti norimus duomenis, pagal poreikį galite keisti filtro operatorių. Pavyzdžiui, galite pakeisti operatoriaus parinktį iš **prasideda** į **tiksliai atitinka**. Kiekvieną kartą naudojant stulpelio antraštės filtrą ir keičiant filtro operatorių „Finance and Operations“ saugomi pakeitimai. Tokiu būdu kitą kartą filtruojant tą stulpelį atkuriamas filtro operatorius.
- **Naršymo sritis**: *Naršymo sritis* atveriama paspaudus bet kurio puslapio kairiosios srities mygtuką **Meniu**. (Mygtukas **Meniu** kartais vadinamas *mėsainiu*, *mėsainio stiliaus meniu* arba *mėsainio stiliaus mygtuku*.) Galite prisegti atvertą naršymo sritį arba ji gali likti sutraukta. Prisegus atvertą naršymo sritį „Finance and Operations“ laikys ją atvertą, kol jos nesutrauksite.

## <a name="explicit-personalizations"></a>Tiesioginis personalizavimas

Pastebima, kad žmonės ir įmonės turi skirtingą nuomonę dėl duomenų, kurie jiems svarbiausi, taip pat dėl duomenų, kurie jiems nereikalingi pagal tai, kaip vadovaujama verslui. Naudodamiesi „Finance and Operations“ galite pasirinkti informacijos užsakymo ir sąveikavimo su informacija būdą. Taip pat galite nurodyti, kad tam tikra informacija turėtų būti paslėpta. Šios galimybės yra itin svarbios norint įgyti asmeninės ir gamybos patirties ir yra tiesioginio personalizavimo pavyzdžiai. Tiesioginis personalizavimas atliekamas turint aiškų tikslą pakeisti elemento arba puslapio išvaizdą arba elgesį.

### <a name="shortcut-menu-options"></a>Nuorodos meniu parinktys

Meniu nurodomi keli būdai, kaip tiesiogiai keisti puslapį, kad jis geriau atitiktų jūsų ar jūsų įmonės poreikius. (Nuorodų meniu taip pat vadinamas *spustelėjus dešinįjį pelės mygtuką rodomu meniu* arba *kontekstiniu meniu*.)

Įprastus ir svarbiausius puslapio keitimus galima atlikti tiesiogiai naudojantis nuorodos meniu parinktimis. Pavyzdžiui, pradedant nuo 17 platformos naujinio, norėdami įterpti tinklelio stulpelių arba juos slėpti, tiesiog dešiniuoju pelės mygtuku spustelėkite tinklelio stulpelio antraštę, o po to paspauskite **Įterpti stulpelių** arba **Slėpti šį stulpelį**.

Be to, pačio paprasčiausio tipo personalizavimą galima atlikti dešiniuoju pelės mygtuku spustelėjus elementą, o po to paspaudus **Personalizuoti**. (Atkreipkite dėmesį, kad personalizuoti galima ne visus jūsų puslapyje esančius elementus.) Naudojant šį personalizavimo metodą rodomas elemento ypatybių langas.

[![Elemento ypatybių personalizavimas](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

Naudojantis ypatybių langu elementą galima personalizuoti toliau išvardytais būdais.

- Keisti elemento žymą.
- Slėpti elementą, kad jis nebūtų rodomas puslapyje. Lauko duomenys nepanaikinami ir nekeičiami. Tiesiog informacija daugiau neberodoma puslapyje.
- Įterpti informaciją į „FastTab“ suvestinės skyrių (jei elementas yra „FastTab“).
- Praleisti lauką, kai paspaudus tabuliavimo klavišą pereinama nuo vieno prie kito puslapio lauko.
- Neleisti redaguoti lauke esančių (bet kurio įrašo) duomenų.

Priklausomai nuo elemento, ypatybių lange gali būti įterpta kitų personalizavimo galimybių. Pavyzdžiui, gali būti, kad naudojantis išklotinės ypatybių langu jums bus leista perkelti tą išklotinę į ataskaitų sritį, o naudojantis ataskaitų srities ypatybių langu – sukurti naują tos ataskaitų srities darbo sritį.

### <a name="the-personalization-toolbar"></a>Personalizavimo įrankių juosta

Norėdami puslapyje atlikti kelis pakeitimus arba atlikti tokius pakeitimus, kurių negalima atlikti naudojantis kitais mechanizmais (pvz., pertvarkymo elementais), galite naudotis įrankių juosta **Personalizavimas**. Norėdami atidaryti įrankių juostą **Personalizavimas**, elemento ypatybių lange paspauskite **Personalizuoti šią formą**. Mygtuką **Personalizuoti šią formą** taip pat galite paspausti kiekvieno puslapio veiksmų srities skirtuko **Parinktys** grupėje **Personalizuoti**.

[![Personalizavimo įrankių juosta](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

#### <a name="navigating-the-page"></a>Naršymas puslapyje

Galimybė naršyti puslapyje, kai atidaryta **Personalizavimo įrankių juosta**, priklauso nuo naudojamos platformos versijos.

- Prieš įdiegiant 19 platformos naujinį, kol atidaryta įrankių juosta **Personalizavimas**, puslapį galima tik skaityti (negalite nieko įvesti) ir puslapis yra neinteraktyvus (galite atlikti tik matomų puslapio elementų pakeitimus). Norėdami keisti sutraukto skyriaus arba kito skirtuko elementus, turite uždaryti įrankių juostą **Personalizavimas**, išplėsti skyrių arba įjungti norimą skirtuką, o paskui iš naujo atidaryti įrankių juostą **Personalizavimas**.

- Pradedant nuo 19 platformos naujinio, jei atidaryta įrankių juosta **Personalizavimas**, puslapį vis dar galima tik skaityti, bet jis daug labiau interaktyvus. Tiksliau tariant, kol atidaryta įrankių juosta **Personalizavimas**, galite išplėsti arba sutraukti „FactBox“ sritį, perjungti skirtukus ir išplėsti ar sutraukti skyrius, lygiai taip pat, kaip tai įprastai atliekate puslapyje. Norėdami taikyti personalizavimo pakeitimą sutraukiamame skyriuje arba skirtuke (pvz., slėpti „FastTab“), paspauskite šalia sutraukiamo skyriaus arba skirtuko esantį mygtuką (kai bus rodoma įvesties klaviatūra arba užvedę virš jo pelės žymiklį).

#### <a name="personalization-tools"></a>Personalizavimo įrankiai

Įrankių juostoje **Personalizavimas** galima naudoti toliau išvardytus įrankius.

- Įrankį **Pasirinkti** naudokite norėdami pasirinkti ir pakeisti elemento ypatybes. Paspauskite įrankį **Pasirinkti**, o po to pasirinkite elementą, kurio ypatybes norite keisti. Kai pasirenkate elementą, rodomas elemento ypatybių langas ir jūs galite keisti visas to elemento ypatybes. Galite pakartoti procesą su kitais to puslapio elementais, kuriuos galima personalizuoti. Tačiau kai kurie elementai naudojami išskirtinai, todėl naudodamiesi „Finance and Operations“ kai kurių jų ypatybių keisti negalėsite. Todėl pasirinkę elementą galite pastebėti, kad kai kurių jo ypatybių keisti negalima. Pavyzdžiui, negalite slėpti reikiamo lauko.
- Įrankį **Perkelti** naudokite norėdami perkelti elementą į kitą dabartinės elementų grupės vietą. (Negalima perkelti elemento už jo pirminės grupės ribų). Paspauskite įrankį **Perkelti**, o po to pasirinkite norimą perkelti elementą. Pasirinkus elementą „Finance and Operations“ nuskaito puslapį ir nustato, kur galima perkelti elementą. Po to sukuria „nuvilkimo zonų“ seką. Velkant elementą dabartinėje grupėje kiekviena „nuvilkimo zona“ rodoma kaip spalvota, paryškinta linija šalia srities, į kurią galima nuvilkti elementą.
- Įrankį **Slėpti** naudokite norėdami paslėpti elementą puslapyje. Paspauskite įrankį **Slėpti**, o po to pasirinkite norimą paslėpti elementą. Paspaudus įrankį **Slėpti** visi šiuo metu paslėpti elementai tampa matomi ir yra rodomi užtamsintame fone. Po to galite vėl juos rodyti. Paspaudę įrankį **Pasirinkti**, galite matyti, kaip puslapis atrodys, kai pasirinkti elementai bus paslėpti.

    - Pradedant nuo platformos 18 naujinio, galite slėpti privalomus laukus ir skyrius, kuriuose yra privalomų laukų. Tai suteikia galimybę kurti supaprastintą platformą, kurioje nebus rodomi numatytieji verslo logikos privalomi laukai. Paslėpti privalomi laukai taip pat yra laikinai rodomi, jei jie yra tušti, kai bandoma įrašyti.

- Įrankį **Suvestinė** naudokite norėdami, kad elementas būtų rodomas „FastTab“ suvestinės skyriuje. Įrankis Suvestinė taikomas tik „FastTab“ skyriuje esantiems laukams. Paspaudus įrankį **Suvestinė** visi pasirinkti suvestinės laukai rodomi užtamsintame fone. Pasirinkdami laukus į „FastTab“ suvestinę galite interaktyviai įtraukti laukų arba iš jos juos pašalinti.
- Įrankį **Praleisti** naudokite norėdami pašalinti elementą iš puslapio klaviatūros tabuliavimo sekos. Paspaudus įrankį **Praleisti** visi šiuo metu praleisti elementai yra rodomi užtamsintame fone. Tada vėl galite juos padaryti skirtukų sekos dalimi.
- Įrankį **Redaguoti** naudokite norėdami pažymėti elementą kaip redaguojamą arba neredaguojamą. Paspaudus įrankį **Redaguoti** visi šiuo metu neredaguojami elementai rodomi užtamsintame fone. Tada vėl galite padaryti, kad juos būtų galima redaguoti. Atminkite, kad kai kurie laukai būtini ir jų negalima padaryti neredaguojamais. Šalia tų laukų rodomas spynos simbolis.
- Naudodamiesi mygtuku **Įterpti** galite matyti į puslapį galimų įterpti elementų sąrašą.

    - Paspaudę mygtuko **Įterpti** įrankį **Laukas** savo puslapyje galite įterpti lauką. Naudodamiesi įrankiu **Laukas** galite įtraukti tik tuos laukus, kurie yra puslapio apibrėžimo dalis, tačiau šiuo metu puslapyje nerodomi. Norėdami gauti informacijos apie tai, kaip sukurti naujų laukų, kurie nėra dabartinio puslapio apibrėžimo dalis, žr. [Pasirinktiniai laukai](user-defined-fields.md). Paspaudus įrankį **Laukas** pirmiausia būtina pasirinkti grupę arba sritį, į kurią norite įtraukti lauką. Dialogo lange rodomas su pasirinkta grupe arba sritimi susijusių laukų sąrašas. Dialogo lange pasirinkite vieną arba kelis norimus įterpti laukus, po to paspauskite **Įterpti**. Norėdami pašalinti pirmiau įtrauktą lauką, pakartokite šį procesą, bet panaikinkite lauko žymėjimą dialogo lange.
    - Paspaudę mygtuko **Įterpti** įrankį **„PowerApp“** į puslapį galite įdėti naudojantis „Microsoft PowerApps“ sukurtą programą. Norėdami gauti išsamios informacijos apie tai, kaip į puslapį įdėti „PowerApps“ programą, žr. [Įdėti „PowerApps“](embed-power-apps.md).

- Paspaudę mygtuką **Valdyti** galite peržiūrėti su visomis dabartinio puslapio personalizacijomis susijusių valdymo parinkčių sąrašą.

    - Paspaudę **Valyti** galite atkurti numatytąją įdiegus puslapį naudotą būseną. Visos dabartinio puslapio personalizacijos panaikinamos. Veiksmo anuliuoti negalima. Todėl naudokitės šia parinktimi tik tada, jei tikrai norite atkurti puslapį.
    - Paspaudę **Importuoti** galite įkelti personalizaciją iš jūsų ar ko nors kito sukurto puslapio failo. Visi dabartiniai jūsų puslapio personalizavimai pakeičiami personalizavimais iš pasirinkto failo.
    - Norėdami įrašyti savo puslapio personalizavimus į failą, paspauskite  **Eksportuoti**. Galite pasidalinti savo personalizavimais su kitais vartotojais. Tiems vartotojams tiesiog reikia importuoti failą, kuriame yra jūsų puslapio personalizavimai.

- Norėdami uždaryti įrankių juostą **Personalizavimas** ir vėl įjungti ankstesnę puslapio interaktyvią būseną, paspauskite mygtuką **Uždaryti**.

Naudojantis įrankių juosta **Personalizavimas** įrašymo operacijos tiesioginės. Jūsų personalizavimai įsigalioja iškart juos atlikus ir nereikia spausti mygtuko **Įrašyti**. Kai kuriais atvejais paspaudus įrankį šalia elemento rodomas spynos simbolis. Šis simbolis reiškia, kad negalima keisti su pasirinktu įrankiu susijusių elemento ypatybių, nes pakeitus tokias ypatybes puslapis veiks netinkamai.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Išklotinės, sąrašo arba nuorodos įtraukimas į darbo sritį

Kai kuriuose puslapiuose, kuriuose pateikiami sąrašai, galima naudotis papildomomis personalizavimo funkcijomis. Naudodamiesi veiksmų srities skirtuko **Parinktys** grupės **Personalizuoti** mygtuku **Įtraukti į darbo sritį** galite matyti konkrečios darbo srities dabartinio sąrašo informaciją. Galite matyti filtruotą ir surūšiuotą darbo srities informacijos rodinį arba numatytąjį rodinį. Taip pat galite nurodyti, ar informacija darbo srityje rodoma kaip sąrašas, kaip suvestinės išklotinė, kurioje gali būti rodomas sąrašo elementų skaičius, arba kaip nuoroda.

[![Įtraukti į darbo sritį](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Norėdami įtraukti sąrašą į darbo sritį, pirmiausia surūšiuokite arba filtruokite puslapio sąrašą, kad informacija būtų rodoma taip, kaip norite, kad ji būtų rodoma darbo srityje. Po to paspauskite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Sąrašas**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite pasirinkti stulpelius, kurie turėtų būti rodomi darbo srities sąraše. Taip pat galite nurodyti darbo srities sąrašui naudojamą žymą.
- Norėdami suvestinę įtraukti į darbo sritį, pirmiausia filtruokite puslapio sąrašą, kad jame būtų rodomi duomenys, kuriuos norite apibendrinti (arba kuriuos norite greitai rasti). Po to paspauskite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Išklotinės dalis**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite nurodyti darbo srities išklotinei naudojamą žymą. Taip pat galite nurodyti, ar išklotinėje turėtų būti rodomas skaičius. Į darbo sritį įtraukę išklotinę galite ją pažymėti, kad būtų atidaromas dabartinis darbo srities puslapis, ir peržiūrėti su išklotine susietą filtruotą sąrašą.
- Norėdami į darbo sritį įtraukti nuorodą, pirmiausia filtruokite puslapio sąrašą, kad jame būtų rodomi jus dominantys duomenys. Po to paspauskite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Nuoroda**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite nurodyti nuorodai naudojamą žymą. Arba galite nurodyti naujo skyriaus, kuriame bus ši nuoroda, žymą.

Į darbo sritį įtraukę savo sąrašą, išklotinę arba nuorodą galite atidaryti tą darbo sritį ir pakeisti jos elementų išdėstymo tvarką.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Suvestinės iš darbo srities įtraukimas į ataskaitų sritį

Kai kuriose darbo srityse pateikiamos skaičių išklotinės (t. y. išklotinės, kuriose nurodomi skaičiai) ir gali būti, kad norėsite, jog tos išklotinės būtų rodomos ir jūsų ataskaitų srityje. Darbo srityje dešiniuoju pelės mygtuku spustelėkite skaičių išklotinę, o po to pasirinkite **Personalizuoti**. Tada išklotinės ypatybių lange paspauskite **Prisegti prie ataskaitų srities**. Kitą kartą atidarius (ir atnaujinus) pasirinktą ataskaitų sritį, tas skaičius bus rodomas po tos darbo srities naršymo išklotine. Galite pasirinkti, kad tas skaičius būtų tiesiogiai perkeliamas į duomenis, kuriuos jis atitinka.

### <a name="personalizing-your-dashboard"></a>Ataskaitų srities personalizavimas

Ataskaitų sritis dažnai yra pirmas atidarius „Finance and Operations“ rodomas puslapis. Galite personalizuoti ataskaitų sritį, kad joje būtų rodomos tik norimos matyti darbo srities išklotinės. Taip pat galite pakeisti išklotinių išdėstymo tvarką, kad jos būtų išdėstomos taip, kaip norite, pakeisti darbo srities naršymo išklotinių pavadinimus arba įtraukti visiškai naują darbo srities išklotinę.

Norėdami personalizuoti ataskaitų sritį, dešiniuoju pelės klavišu spustelėkite bet kurią išklotinę, po to paspauskite **Personalizuoti**, kad būtų atidaromas išklotinės ypatybių langas.

- Jei norite slėpti pasirinktą išklotinę arba pakeisti jos pavadinimą, tokį pakeitimą galite atlikti tiesiogiai ypatybių lange.
- Jei norite keisti darbo srities išklotinių išdėstymo tvarką, ypatybių lange paspaudę **Personalizuoti šią formą** atidarykite įrankių juostą **Personalizavimas**. Tada galite naudoti įrankį **Perkelti** ir pakeisti išklotinių išdėstymo tvarką.
- Norėdami sukurti naują darbo srities išklotinę, ypatybių lange paspauskite **Įtraukti darbo sritį**. Nauja darbo srities išklotinė sukuriama ataskaitų srities apačioje. Galite pakeisti šios naujos darbo srities išklotinės pavadinimą. Į darbo sritį taip pat galite įtraukti sąrašų, išklotinių ir nuorodų, kaip aprašyta šios temos skyriuje [Sąrašų, išklotinių arba nuorodų įtraukimas į darbo sritis](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalization"></a>Personalizavimo parametrų administravimas

Personalizavę puslapį galite bendrinti personalizavimą su kitais vartotojais eksportuodami personalizuotą puslapį. Tada kitų vartotojų galite paprašyti atidaryti personalizuotą puslapį ir importuoti personalizavimo failą, kurį sukūrėte. Arba galite perduoti savo personalizavimą administratoriaus teises turinčiam vartotojui. Tokiu būdu tas vartotojas galės jūsų personalizavimo failą vienu metu taikyti keliems vartotojams.

Vartotojai, turintys administratoriaus teises, taip pat gali valdyti kitų vartotojų personalizavimą puslapyje **Personalizavimas**. Šiame puslapyje yra keturi skirtukai:

- **Taikyti**: galite importuoti arba pasirinkti personalizavimą vienam ar daugiau vartotojų. Norėdami personalizavimą taikyti vienam ar keliems vartotojams, pirmiausia pasirinkite vaidmenį ir vartotojus, kuriems tas vaidmuo suteiktas. Tada pasirinkite esamą personalizavimą, taikykite pasirinktiems vartotojams arba importuokite personalizavimo failą. Personalizavimas patikrinamas ir taikomas visiems pasirinktiems vartotojams, kai jie kitą kartą atidarys pasirinktą puslapį.
- **Išvalyti**: galite išvalyti visus vieno ar kelių vartotojų puslapio ar darbo srities personalizavimus. Pirmiausia pasirinkite puslapį arba darbo sritį, kad būtų rodomas tą puslapį ar darbo sritį personalizavusių vartotojų sąrašas. Tada pažymėkite vartotojus, kurių puslapio ar darbo srities personalizavimą norėtumėte išvalyti, ir paspauskite **Valyti**. Panaikinami visi personalizavimai, kuriuos pasirinkti vartotojai taikė pasirinktam puslapiui arba darbo sričiai. Šio veiksmo anuliuoti negalima. Tačiau jei buvo įrašytas puslapio ar darbo srities personalizavimas, tokį personalizavimą galima importuoti iš naujo.
- **Vartotojo vadovas**: pasirinkite vartotoją, kad būtų rodomas jo arba jos personalizuotų puslapių sąrašas. Tada galite įjungti arba išjungti pasirinkto vartotojo galimybę jam naudotis konkrečių puslapių arba visos sistemos personalizavimais. Taip pat galite importuoti, eksportuoti arba išvalyti pasirinkto vartotojo personalizavimą.
- **Sistema**: galite laikinai išjungti visus visų vartotojų sistemos personalizavimus. Tokiu atveju personalizavimai panaikinami. Nustatoma numatytoji visų vartotojų puslapių būsena. Jeigu vėliau iš naujo suaktyvinsite personalizavimą, visi personalizavimai bus pritaikyti iš naujo. Taip pat galite visam laikui išjungti visus visų vartotojų sistemos personalizavimus. Panaikintų personalizavimų atkurti neįmanoma. Todėl prieš atlikdami šią užduotį būtinai eksportuokite visus personalizavimus, kurių vėliau gali prireikti.

## <a name="personalization-of-inventory-dimensions"></a>Atsargų dimensijų personalizavimo duomenys

Personalizuodami puslapyje atsargų dimensijų sąranką, atsižvelkite į parametrus, kurie buvo sukurti naudojant parinktį **Rodyti dimensiją**. Pavyzdžiui, naudojate personalizavimą, norėdami paslėpti paketo numerio atsargų dimensijos stulpelį, tačiau stulpelis rodomas kitą kartą atidarius puslapį. Taip atsitinka todėl, kad atsargų dimensijų stulpelių rodymas valdomas naudojant parametrus **Dimensijos rodinys**.

Parametrai **Dimensijos rodinys** taikomi visuose puslapiuose ir naudojantis šiais parametrais panaikinamos visos personalizuotos atskirų puslapių atsargų dimensijų laukų sąrankos.

Todėl ankstesniame pavyzdyje, jei nenorite, kad būtų rodomas paketo numerio atsargų dimensijos stulpelis, turite lentelėje panaikinti tos dimensijos parinkties **Rodyti dimensijas** žymėjimą. Galiausiai šis pakeitimas bus taikomas ne tik vienam konkrečiam puslapiui, tačiau visiems puslapiams.

