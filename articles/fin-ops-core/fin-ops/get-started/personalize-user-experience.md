---
title: Vartotojo patirties personalizavimas
description: Šiame straipsnyje paaiškinama, kaip galite personalizuoti programą.
author: jasongre
manager: AnnBe
ms.date: 10/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 124609041163bbcaf1b86a6964fa3f56fcd8f755
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658765"
---
# <a name="personalize-the-user-experience"></a>Vartotojo patirties personalizavimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje paaiškinama, kaip galite personalizuoti programą.

Yra trys pagrindinės personalizavimo klasės.

- Sąrankos puslapyje atliekamas personalizavimas. Prie pavyzdžių priskiriama spalvų tema ir laiko juosta.
- Su puslapio naudojimu susijęs personalizavimas. Toks personalizavimas vadinamas *netiesioginiu* personalizavimu. Pavyzdžiui, sistema seka jūsų keičiamą tinklelio stulpelių plotį ir „FastTab“ sutrauktą arba išplėstą būseną.
- Personalizavimas, kurį atlieka vartotojas, norėdamas keisti puslapio išvaizdą pakeisdamas tai, kaip rodomas ar veikia to puslapio elementas, dažnai naudojantis interaktyvaus personalizavimo režimu. Toks personalizavimas vadinamas *tiesioginiu* personalizavimu. Pavyzdžiui, vartotojas gali įterpti elementų, juos slėpti arba keisti jų išdėstymo tvarką puslapyje.

Visi personalizavimo parametrai, kuriuos nustato vartotojas, taikomi tik tam vartotojui, nepriklausomai nuo personalizavimo tipo ir nuo to, su kokia įmone šiuo sąveikauja vartotojas. Vieno vartotojo atlikti puslapio keitimai neturi įtakos kitiems sistemos vartotojams.

## <a name="system-wide-options-for-the-current-user"></a>Dabartinio vartotojo visos sistemos parinktys

Puslapyje **Vartotojo parinktys** pateikiama keletas visos sistemos dabartinio vartotojo parametrų. Norėdami atidaryti puslapį **Vartotojo parinktys**, naršymo juostoje paspauskite mygtuką **Parametrai** (krumpliaračio simbolis), o po to paspauskite **Vartotojo parinktys**. Puslapyje **Vartotojo parinktys** yra keturi skirtukai, kuriuose nurodomi įvairūs vartotojo parametrai.

- **Vaizdas**: pasirinkite puslapio elementų spalvų temą ir numatytąjį dydį.
- **Nuostatos**: pasirinkite numatytąsias vertes, kurios naudojamos kaskart atidarius sistemą. Prie šių verčių priskiriama įmonė, pradinis puslapis ir numatytasis rodymo / redagavimo režimas. (Naudojantis rodymo / redagavimo režimu nustatoma, ar puslapis užrakintas peržiūrai, ar galima jį redaguoti kiekvieną kartą atidarius). Šiame skirtuke taip pat yra kalbos, laiko juostos, datos, laiko ir numerių formatų parinktys. Galiausiai šiame skirtuke yra keletas papildomų kiekviename leidime skirtingų nuostatų.
- **Paskyra**: koreguokite vartotojo vardą ir kitas su paskyra susijusias parinktis.
- **Darbo eiga**: pasirinkite su darbo eiga susijusias parinktis.

Naudodami puslapį **Vartotojo parinktys** galite ne tik pakeisti savo vartotojo parametrus, bet ir peržiūrėti bei panaikinti savo naudojimo duomenis ir personalizavimo parametrus. Tereikia veiksmų srityje pasirinkti **Naudojimo duomenys** .

Naudojantis programa, dauguma pasirinkčių išsaugomos, kad kitą kartą galėtumėte lengviau naudotis sistema. Skirtuke **Personalizavimas** galite peržiūrėti ir tvarkyti asmeninius sistemos puslapiams atliktus pakeitimus. Šiame skirtuke taip pat galite iš naujo nustatyti funkcijų paaiškinimus (t. y. iššokančiuosius langus, kuriuose esate supažindinami su naujomis sistemos funkcijomis). Būsite dar kartą įspėti apie anksčiau naudotas funkcijas.

> [!NOTE]
> Jei funkcija [Įrašyti rodiniai](saved-views.md) įjungta, galite peržiūrėti ir tvarkyti savo personalizavimo parametrus, pasirinkdami parinktį **Personalizavimas**, esančią veiksmų srities puslapyje **Vartotojo parinktys**.

## <a name="implicit-personalizations"></a>Netiesioginis personalizavimas

Netiesioginis personalizavimas atliekamas tiesiog sąveikaujant su tam tikrais valdikliais, kurie išsaugo savo esamą matomą būseną.

- **Tinklelio stulpeliai**: galite koreguoti tinklelio stulpelio plotį, kairėje arba dešinėje stulpelio antraštės pusėje pasirinkdami dydžio keitimo juostą ir slinkdami ją į kairę arba į dešinę, kol stulpelis bus reikiamo pločio. Programoje saugomas nustatytas stulpelio plotis. Tada, kitą kartą atidarius puslapį, kuriame yra tas tinklelis, bus pakeičiamas stulpelio dydis.
- **„FastTabs“**: kai kuriuose puslapiuose yra išplečiamos dalys, vadinamos *„FastTabs“*. Programoje saugoma informacija apie išplėstus ir sutrauktus „FastTabs“. Tada, kitą kartą atidarius puslapį, tie patys „FastTabs“ bus išplečiami arba sutraukiami, priklausomai nuo paskutinės sąveikos su puslapiu. Kai kuriais atvejais sutraukus „FastTab“ galima padidinti sistemos efektyvumą, nes programai nereikia nuskaityti „FastTabs“ informacijos, kol jie neišskleisti. Kaip vėliau paaiškinta šioje temoje, taip pat galite keisti puslapio „FastTabs“ tvarką.
- **„Fact Boxes”**: kai kuriuose puslapiuose yra **susijusios informacijos** sritis, rodanti tik skaityti skirtą informaciją, kuri susijusi su dabartine puslapio tema. Kiekviena **susijusios informacijos** srities dalis vadinama *„Fact Box“*. Galite išplėsti arba sutraukti **susijusios informacijos** sritį, taip pat galite išplėsti arba sutraukti atskiras „Fact Boxes“. Programa išsaugo šias nuostatas. Tada, kitą kartą atidarius į puslapį, priklausomai nuo paskutinės sąveikos su puslapiu, išplečiama arba sutraukiama **susijusios informacijos** sritis ir atskiros „Fact Boxes“. Kai kuriais atvejais sutraukus „FactBox“ galima padidinti sistemos efektyvumą, nes programai nereikia nuskaityti „FactBoxes“ informacijos, kol jos neišskleistos.
- **Veiksmų sritys**: šalia daugelio puslapių viršaus rodoma *Veiksmų sritis*. Veiksmų srityje yra daugeliui dabartiniame puslapyje galimų atlikti veiksmų skirtų mygtukų. Šie mygtukai skirtukuose dažnai sisteminami. Pagal numatytuosius parametrus galite „prisegti” visą atidarytą veiksmų sritį arba galite ją sutraukti. Tada, kitą kartą atidarius puslapį, veiksmų sritis bus atidaryta arba sutraukta, priklausomai nuo paskutinės sąveikos su puslapiu. Jei prisegate atidarytą veiksmų sritį, bus rodomas paskutinis naudotas skirtukas.
- **„QuickFilters“**: virš daugelio tinklelių rodomas *„QuickFilter“*. Naudodamiesi „QuickFilter“ galite filtruoti tinklelį pagal pasirinktą stulpelį. Programoje saugomas filtruojamas stulpelis. Tada, kitą kartą atidarius puslapį, kuriame yra tas tinklelis, tinklelis bus filtruojamas tame pačiame stulpelyje. Tačiau po to galite filtruoti kito stulpelio tinklelį.
- **Stulpelio antraštės filtrai**: jei filtruodami tinklelį naudojate *stulpelio antraštės filtrus*, norėdami rasti norimus duomenis, pagal poreikį galite keisti filtro operatorių. Pavyzdžiui, galite pakeisti operatoriaus parinktį iš **prasideda** į **tiksliai atitinka**. Kiekvieną kartą naudojant stulpelio antraštės filtrą ir keičiant filtro operatorių, programoje išsaugomi pakeitimai. Tada, kitą kartą filtruojant tą stulpelį atkuriamas filtro operatorius.
- **Naršymo sritis**: *naršymo sritis* atveriama paspaudus bet kurio puslapio viršutiniame kairiajame kampe esantį mygtuką **Išplėsti naršymo sritį**. (Šis mygtukas kartais vadinamas _mygtuku **Meniu**_, *mėsainiu*, *mėsainio stiliaus meniu* arba *mėsainio stiliaus mygtuku*.) Galite prisegti atvertą naršymo sritį arba galite ją sutraukti. Prisegus atvertą naršymo sritį, programa laikys ją atvertą, kol jos nesutrauksite.

## <a name="explicit-personalizations"></a>Tiesioginis personalizavimas

Pastebima, kad žmonės ir įmonės turi skirtingą nuomonę dėl duomenų, kurie jiems svarbiausi, taip pat dėl duomenų, kurie jiems nereikalingi pagal tai, kaip vadovaujama verslui. Jūs galite pasirinkti informacijos užsakymo ir sąveikavimo su informacija būdą. Taip pat galite nurodyti, kad tam tikra informacija turėtų būti paslėpta. Šios galimybės yra itin svarbios norint įgyti asmeninės ir gamybos patirties ir yra tiesioginio personalizavimo pavyzdžiai. Tiesioginis personalizavimas atliekamas turint aiškų tikslą pakeisti elemento arba puslapio išvaizdą arba elgesį.

### <a name="shortcut-menu-options"></a>Nuorodos meniu parinktys

Meniu nurodomi keli būdai, kaip tiesiogiai keisti puslapį, kad jis geriau atitiktų jūsų ar jūsų įmonės poreikius. (Nuorodų meniu taip pat vadinamas *spustelėjus dešinįjį pelės mygtuką rodomu meniu* arba *kontekstiniu meniu*.)

Įprastus ir svarbiausius puslapio keitimus galima atlikti tiesiogiai naudojantis nuorodos meniu parinktimis. Pavyzdžiui, pradedant nuo 17 platformos naujinio, norėdami įterpti tinklelio stulpelių arba juos slėpti, tiesiog dešiniuoju pelės mygtuku spustelėkite stulpelio antraštę, o po to paspauskite **Įterpti stulpelių** arba **Slėpti šį stulpelį**.

Be to, pačio paprasčiausio tipo personalizavimą galima atlikti dešiniuoju pelės mygtuku spustelėjus elementą, o po to paspaudus **Personalizuoti**. (Atkreipkite dėmesį, kad personalizuoti galima ne visus jūsų puslapyje esančius elementus.) Naudojant šį personalizavimo metodą rodomas elemento ypatybių langas.

![Elemento ypatybių personalizavimas](./media/personalization-element-properties.png)

Naudojantis ypatybių langu elementą galima personalizuoti toliau išvardytais būdais.

- Keisti elemento žymą.
- Slėpti elementą, kad jis nebūtų rodomas puslapyje. Lauko duomenys nepanaikinami ir nekeičiami. Tiesiog informacija daugiau neberodoma puslapyje.
- Įterpti informaciją į „FastTab“ suvestinės skyrių (jei elementas yra „FastTab“).
- Praleisti lauką, kad niekada nebūtų rodomas, kai puslapyje vykdote keitimus.
- Neleisti redaguoti lauke esančių (bet kurio įrašo) duomenų.

Priklausomai nuo elemento, ypatybių lange gali būti įterpta kitų personalizavimo galimybių. Pavyzdžiui, gali būti, kad naudojantis išklotinės ypatybių langu jums bus leista perkelti tą išklotinę į ataskaitų sritį, o naudojantis ataskaitų srities ypatybių langu – sukurti naują tos ataskaitų srities darbo sritį.

### <a name="the-personalization-toolbar"></a>Personalizavimo įrankių juosta

Norėdami puslapyje atlikti kelis pakeitimus arba tokius pakeitimus, kurių negalima atlikti naudojantis kitu mechanizmu (pvz., keisti elementų išdėstymo tvarką), galite naudotis įrankių juosta **Personalizavimas**. Norėdami atidaryti įrankių juostą **Personalizavimas**, atlikite vieną iš toliau pateiktų veiksmų.

- Elemento ypatybių lange pasirinkite **Pritaikyti šią formą asmeniniams poreikiams**.
- Bet kurio puslapio veiksmų srities skirtuke **Parinktys** esančioje grupėje **Personalizavimas**, pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**.
- Naršymo juostoje pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirinkite **Personalizavimas**.

[![Personalizavimo įrankių juosta](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Naršymas puslapyje

Kai atidaroma įrankių juosta **Personalizavimas**, esamas puslapis skirtas tik skaityti (kitaip tariant, negalite redaguoti duomenų), tačiau jis yra interaktyvus. Tiksliau sakant, galite išplėsti arba sutraukti **susijusios informacijos** sritį, perjungti skirtukus ir išplėsti arba sutraukti sekcijas taip pat, kaip paprastai atliekate šiuos veiksmus puslapyje. Norėdami taikyti personalizavimą sutraukiamame skyriuje arba skirtuke (pvz., slėpti „FastTab“), pasirinkite šalia skyriaus arba skirtuko esantį mygtuką (kai bus rodoma įvesties klaviatūra arba užvedę virš jo pelės žymiklį).

#### <a name="personalization-tools"></a>Personalizavimo įrankiai

Įrankių juostoje **Personalizavimas** galima naudoti toliau išvardytus įrankius.

- Įrankį **Pasirinkti** naudokite norėdami pasirinkti ir pakeisti elemento ypatybes. Norėdami naudoti šį įrankį, įrankių juostoje pasirinkite mygtuką **Pasirinkti**, tada pasirinkite norimą elementą. Rodomas elemento ypatybių langas ir jūs galite keisti visas to elemento ypatybes. Galite pakartoti procesą su kitais puslapio elementais, kuriuos galima personalizuoti. Atkreipkite dėmesį, kad kai kuriais atvejais gali nebūti kai kurių personalizavimo ypatybių. Pavyzdžiui, negalite užrakinti reikiamo lauko.
- Įrankį **Slėpti** naudokite norėdami paslėpti elementą puslapyje. Norėdami naudoti šį įrankį, įrankių juostoje pasirinkite mygtuką **Slėpti**, tada pasirinkite norimą paslėpti elementą. Naudojant įrankį **Slėpti** visi šiuo metu paslėpti elementai tampa matomi ir yra rodomi užtamsintame fone. Tada galite padaryti elementą matomą jį pasirinkdami. Norėdami pamatyti, kaip puslapis atrodys, kai elementai bus paslėpti, perjunkite į kitą personalizavimo įrankį.

    Galite slėpti privalomus laukus ir skyrius, kuriuose yra privalomų laukų. Tokiu būdu galite kurti supaprastintą platformą, kurioje nebus rodomi privalomi laukai, jei numatytosios vertės įvestos naudojant verslo logiką. Kai vartotojas bandys įrašyti puslapį, paslėpti privalomi laukai bus laikinai matomi, jei jie tušti.

- Pasirinkite įrankį **Įtraukti lauką**, norėdami lauką įtraukti į puslapį. Kai naudojate šį įrankį, galite pridėti tik tuos laukus, kurie yra puslapio apibrėžimo dalis. Norėdami gauti informacijos apie tai, kaip sukurti naujų laukų, kurie nėra dabartinio puslapio apibrėžimo dalis, žr. [Pasirinktiniai laukai](user-defined-fields.md). Paspaudus įrankių juostoje esantį mygtuką **Įtraukti lauką** pirmiausia būtina pasirinkti grupę arba sritį, į kurią norite įtraukti lauką. Dialogo lange bus rodomas su pasirinkta grupe arba sritimi susijusių laukų sąrašas. Dialogo lange pasirinkite vieną arba kelis norimus įterpti laukus, po to paspauskite **Įterpti**. Norėdami pašalinti pirmiau įtrauktą lauką, pakartokite šį procesą, bet panaikinkite lauko žymėjimą dialogo lange.
- Įrankį **Perkelti** naudokite norėdami perkelti elementą į kitą dabartinės elementų grupės vietą. Atkreipkite dėmesį, kad negalima perkelti elemento už jo pirminės grupės ribų. Norėdami naudoti šį įrankį, įrankių juostoje pasirinkite mygtuką **Perkelti**, tada pasirinkite norimą perkelti elementą. Pasirinkus elementą, programa nustato vietas, kur leidžiama perkelti elementą. Šios vietos vadinamos *nuvilkimo zonomis*. Velkant elementą dabartinėje grupėje kiekviena nuvilkimo zona rodoma kaip spalvota, paryškinta linija šalia srities, į kurią galima nuvilkti elementą.
- Įrankį **Praleisti** naudokite norėdami pašalinti elementą iš puslapio klaviatūros tabuliavimo sekos. Paspaudus įrankių juostoje esantį mygtuką **Praleisti** visi šiuo metu praleisti elementai yra rodomi užtamsintame fone. Galite interaktyviai pašalinti arba įtraukti laukus į skirtukų seką.
- Įrankį **Rodyti antraštėje** naudokite norėdami, kad laukas būtų rodomas „FastTab“ suvestinės skyriuje. Paspaudus įrankių juostoje esantį mygtuką **Rodyti antraštėje** visi pasirinkti suvestinės laukai rodomi užtamsintame fone. Pasirinkdami laukus į „FastTab“ suvestinę galite interaktyviai įtraukti laukų arba iš jos juos pašalinti.
- Įrankį **Užrakinti** naudokite norėdami pažymėti elementą kaip redaguojamą arba neredaguojamą. Paspaudus įrankių juostoje esantį mygtuką **Užrakinti** visi šiuo metu neredaguojami elementai yra rodomi užtamsintame fone. Tada vėl galite padaryti, kad juos būtų galima redaguoti. Atminkite, kad kai kurie laukai būtini ir jų negalima padaryti neredaguojamais. Šalia tų laukų rodomas spynos simbolis.
- Naudokite mygtuką **Įtraukti „PowerApp“** norėdami į puslapį įdėti programą, sukurtą naudojant „Microsoft PowerApps“. Norėdami gauti išsamios informacijos apie tai, kaip į puslapį įdėti „PowerApps“ programą, žr. [Įdėti „PowerApps“](embed-power-apps.md).
- Naudodami įrankį **Valyti** galite atkurti numatytąją įdiegus puslapį naudotą būseną. Visas dabartinio puslapio personalizavimas bus panaikintas. Veiksmo anuliuoti negalima. Todėl naudokite šį įrankį tik tada, jei tikrai norite atkurti puslapį.
- Naudodami įrankį **Importuoti** galite įkelti personalizavimą iš jūsų ar ko nors kito sukurto failo. Kai importuojate puslapio personalizavimo nustatymus, galite pasirinkti, ar jie turi būti įtraukti į esamus puslapio personalizavimo nustatymus, ar juos pakeisti. Veiksmo anuliuoti negalima. Todėl, kai importuojate personalizavimą, turite rankiniu būdu išvalyti arba anuliuoti keitimus, kurių nenorite.
- Naudodami įrankį **Eksportuoti** galite įrašyti savo puslapio personalizavimus į failą. Tada galite pasidalinti savo personalizavimais su kitais vartotojais. Tiems vartotojams tiesiog reikia importuoti failą, kuriame yra jūsų puslapio personalizavimai.
- Norėdami uždaryti įrankių juostą **Personalizavimas** ir vėl įjungti ankstesnę puslapio interaktyvią būseną, paspauskite mygtuką **Uždaryti**.

Paprastai, kai naudojama įrankių juosta **Personalizavimas**, jūsų personalizavimas įsigalioja iškart jį atlikus. Tačiau, jei funkcija [Įrašyti rodiniai](saved-views.md) yra įjungta, turite aiškiai įrašyti pasirinkto rodinio personalizavimą.

Kai kuriais atvejais paspaudus įrankį šalia elemento rodomas spynos simbolis. Šis simbolis reiškia, kad negalima keisti su pasirinktu įrankiu susijusių elemento ypatybių, nes pakeitus tokias ypatybes puslapis veiks netinkamai.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Išklotinės, sąrašo arba nuorodos įtraukimas į darbo sritį

Kai kuriuose puslapiuose, kuriuose yra sąrašų, galima veiksmų srities skirtuko **Parinktys** grupėje **Personalizavimas** esanti personalizavimo funkcija **Įtraukti į darbo sritį**. Ši funkcija suteikia galimybę perkelti susijusią informaciją iš dabartinio sąrašo į konkrečią darbo sritį. Darbo srityje rodoma informacija gali būti pagrįsta visu sąrašu arba filtruota ir surūšiuota sąrašo versija. Taip pat galite nurodyti, ar informacija darbo srityje rodoma kaip sąrašas, suvestinės išklotinė, kurioje gali būti rodomas sąrašo elementų skaičius, arba nuoroda.

> [!NOTE]
> Jei funkcija [Įrašyti rodiniai](saved-views.md) įjungta, į darbo sritį perkeliamas turinys yra tiesiogiai susietas su rodiniu. Rodinio užklausa naudojama norint gauti duomenis darbo srityje, o atitinkama darbo srities išklotinė arba saitas atidaro puslapį taip, kad rodinio užklausa ir personalizavimas būtų taikomi.

[![Įtraukti į darbo sritį](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Norėdami įtraukti sąrašą į darbo sritį, pirmiausia surūšiuokite arba filtruokite puslapio sąrašą, kad informacija būtų rodoma taip, kaip norite, kad ji būtų rodoma darbo srityje. (Jei funkcija Įrašyti rodiniai įjungta, negalite tęsti, kol neįrašysite rodinio, kuriame yra šios sąlygos.) Tada pasirinkite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Sąrašas**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite pasirinkti stulpelius, kurie turėtų būti rodomi darbo srities sąraše. Taip pat galite nurodyti darbo srities sąrašui naudojamą žymą.
- Norėdami suvestinę įtraukti į darbo sritį, pirmiausia filtruokite puslapio sąrašą, kad jame būtų rodomi duomenys, kuriuos reikia apibendrinti (arba kuriuos norite greitai rasti). (Jei funkcija Įrašyti rodiniai įjungta, negalite tęsti, kol neįrašysite rodinio, kuriame yra šios sąlygos.) Tada pasirinkite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Išklotinės dalis**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite nurodyti darbo srities išklotinei naudojamą žymą. Taip pat galite nurodyti, ar išklotinėje turėtų būti rodomas skaičius. Po to, kai išklotinė įtraukiama į darbo sritį, galite pasirinkti ją, kad atidarytumėte dabartinį puslapį iš darbo srities. Tada galite peržiūrėti filtruotą sąrašą, susietą su išklotine.
- Norėdami į darbo sritį įtraukti nuorodą, pirmiausia filtruokite puslapio sąrašą, kad jame būtų rodomi jus dominantys duomenys. (Jei funkcija Įrašyti rodiniai įjungta, negalite tęsti, kol neįrašysite rodinio, kuriame yra šios sąlygos.) Tada pasirinkite **Įtraukti į darbo sritį**. Pasirinkite darbo sritį, o po to lauke **Pateiktis** paspauskite **Nuoroda**. Paspaudus **Konfigūruoti** rodomas dialogo langas, kuriame galite nurodyti nuorodai naudojamą žymą. Arba galite nurodyti naujo skyriaus, kuriame yra ši nuoroda, žymą.

Į darbo sritį įtraukę savo sąrašą, išklotinę arba nuorodą galite atidaryti tą darbo sritį ir pakeisti jos elementų išdėstymo tvarką.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Suvestinės iš darbo srities įtraukimas į ataskaitų sritį

Kai kuriose darbo srityse pateikiamos skaičių išklotinės (t. y. išklotinės, kuriose nurodomi skaičiai) ir gali būti, kad norėsite, jog tos išklotinės būtų rodomos ir jūsų ataskaitų srityje. Darbo srityje dešiniuoju pelės mygtuku spustelėkite skaičiavimo plytelę, pasirinkite **Personalizavimas**, tada išklotinės ypatybių lange pasirinkite **Prisegti prie ataskaitų srities**. Tada, kitą kartą atidarius ir atnaujinus pasirinktą ataskaitų sritį, tas skaičius bus rodomas po tos darbo srities naršymo išklotine. Galite pasirinkti, kad tas skaičius būtų tiesiogiai perkeliamas į duomenis, kuriuos jis atitinka.

### <a name="personalizing-your-dashboard"></a>Ataskaitų srities personalizavimas

Ataskaitų sritis dažnai yra pirmasis atidarius programą rodomas puslapis. Galite personalizuoti ataskaitų sritį, kad joje būtų rodomos tik norimos matyti darbo srities išklotinės. Taip pat galite pakeisti išklotinių išdėstymo tvarką, kad jos būtų išdėstomos taip, kaip norite, pakeisti darbo srities naršymo išklotinių pavadinimus arba įtraukti naują darbo srities išklotinę.

Norėdami personalizuoti ataskaitų sritį, dešiniuoju pelės klavišu spustelėkite bet kurią išklotinę, po to paspauskite **Personalizuoti**, kad būtų atidaromas išklotinės ypatybių langas.

- Jei norite slėpti pasirinktą išklotinę arba pakeisti jos pavadinimą, tokį pakeitimą galite atlikti tiesiogiai ypatybių lange.
- Jei norite keisti darbo srities išklotinių išdėstymo tvarką, ypatybių lange paspaudę **Personalizuoti šią formą** atidarykite įrankių juostą **Personalizavimas**. Tada galite naudoti įrankį **Perkelti** ir pakeisti išklotinių išdėstymo tvarką.
- Norėdami įtraukti naują darbo srities išklotinę, ypatybių lange paspauskite **Įtraukti darbo sritį**. Nauja darbo srities išklotinė sukuriama ataskaitų srities apačioje. Galite pakeisti šios naujos darbo srities išklotinės pavadinimą. Į darbo sritį taip pat galite įtraukti sąrašų, išklotinių ir nuorodų, kaip aprašyta šios temos skyriuje [Sąrašų, išklotinių arba nuorodų įtraukimas į darbo sritis](#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalizations"></a>Personalizavimo parametrų administravimas

Personalizavę puslapį galite bendrinti personalizavimą su kitais vartotojais eksportuodami personalizuotą puslapį. Tada kitų vartotojų galite paprašyti atidaryti personalizuotą puslapį ir importuoti personalizavimo failą, kurį sukūrėte. Arba galite perduoti savo personalizavimą administratoriaus teises turinčiam vartotojui. Tokiu būdu tas vartotojas galės jūsų personalizavimo failą vienu metu taikyti keliems vartotojams.

Vartotojai, turintys administratoriaus teises, taip pat gali valdyti kitų vartotojų personalizavimą puslapyje **Personalizavimas**.

Šiame puslapyje yra keturi skirtukai, skirti klientams, kurie neįjungė funkcijos [Įrašyti rodiniai](saved-views.md).

- **Taikyti**: galite importuoti arba pasirinkti personalizavimą vienam ar daugiau vartotojų. Norėdami personalizavimą taikyti vienam ar keliems vartotojams, pirmiausia pasirinkite vaidmenį ir vartotojus, kuriems tas vaidmuo suteiktas. Tada pasirinkite esamą personalizavimą, taikykite pasirinktiems vartotojams arba importuokite personalizavimo failą. Personalizavimas patikrinamas ir taikomas visiems pasirinktiems vartotojams, kai jie kitą kartą atidarys pasirinktą puslapį.
- **Išvalyti**: galite išvalyti visus vieno ar kelių vartotojų puslapio ar darbo srities personalizavimus. Pirmiausia pasirinkite puslapį arba darbo sritį, kad būtų rodomas tą puslapį ar darbo sritį personalizavusių vartotojų sąrašas. Tada pažymėkite vartotojus, kurių puslapio ar darbo srities personalizavimą norėtumėte išvalyti, ir paspauskite **Valyti**. Panaikinami visi personalizavimai, kuriuos pasirinkti vartotojai taikė pasirinktam puslapiui arba darbo sričiai. Šio veiksmo anuliuoti negalima. Tačiau jei buvo įrašytas puslapio ar darbo srities personalizavimas, tokį personalizavimą galima importuoti iš naujo.
- **Vartotojai**: pasirinkite vartotoją, kad būtų rodomas vartotojo personalizuotų puslapių sąrašas. Tada galite įjungti arba išjungti pasirinkto vartotojo galimybę jam naudotis konkrečių puslapių arba visos sistemos personalizavimais. Taip pat galite importuoti, eksportuoti arba išvalyti vartotojo personalizavimą. Be to, galite iš naujo nustatyti vartotojo funkcijų paaiškinimus. Tokiu atveju, jei vartotojas anksčiau atmetė visus iššokančiuosius langus, kurie supažindino su naujomis funkcijomis, jie bus rodomi dar kartą, kai vartotojas susidurs su šiomis funkcijomis.
- **Sistema**: galite laikinai išjungti visų vartotojų sistemos personalizavimus. Šiuo atveju visi personalizavimai panaikinami visiems vartotojams, o visi puslapiai iš naujo nustatomi pagal numatytąją būseną. Jeigu vėliau vėl įjungsite personalizavimą, visi personalizavimai bus pritaikyti iš naujo. Taip pat galite visam laikui išjungti visus visų vartotojų sistemos personalizavimus. Panaikintų personalizavimų atkurti neįmanoma. Todėl prieš atlikdami šią užduotį būtinai eksportuokite visus personalizavimus, kurių vėliau gali prireikti.

Puslapyje **Personalizavimas** yra penki skirtukai, skirti klientams, kurie įjungė funkciją [Įrašyti rodiniai](saved-views.md).

- **Publikuoti rodiniai**: šie rodiniai publikuoti jūsų organizacijoje. Norėdami pakeisti vartotojus, kuriems skirti šie rodiniai, galite keisti saugos vaidmenis arba juridinius subjektus, susietus su kiekvienu rodiniu. Taip pat galite eksportuoti arba naikinti vieną ar daugiau publikuotų rodinių.
- **Nepublikuoti rodiniai**: šie rodiniai yra šablonų rodiniai, kurie buvo importuoti į jūsų sistemą, tačiau dar nebuvo publikuoti. Galite publikuoti, eksportuoti ar naikinti šiuos rodinius.
- **Asmeniniai rodiniai**: šiuos rodinius sukūrė sistemos vartotojai. Galite publikuoti asmeninį rodinį organizacijai arba kopijuoti vieną ar daugiau šių rodinių kitiems vartotojams. Taip pat galite pagal poreikį eksportuoti ar naikinti šiuos rodinius.
- **Vartotojai**: pasirinkite vartotoją, kad būtų rodomas vartotojo personalizuotų puslapių sąrašas. Tada galite įjungti arba išjungti pasirinkto vartotojo galimybę jam naudotis konkrečių puslapių arba visos sistemos personalizavimais. Taip pat galite importuoti, eksportuoti arba išvalyti vartotojo personalizavimą. Be to, galite iš naujo nustatyti vartotojo funkcijų paaiškinimus. Tokiu atveju, jei vartotojas anksčiau atmetė visus iššokančiuosius langus, kurie supažindino su naujomis funkcijomis, jie bus rodomi dar kartą, kai vartotojas susidurs su šiomis funkcijomis.
- **Sistema**: galite laikinai išjungti visų vartotojų sistemos personalizavimus. Šiuo atveju visi personalizavimai panaikinami visiems vartotojams, o visi puslapiai iš naujo nustatomi pagal numatytąją būseną. Jeigu vėliau vėl įjungsite personalizavimą, visi personalizavimai bus pritaikyti iš naujo. Taip pat galite visam laikui išjungti visus visų vartotojų sistemos personalizavimus. Panaikintų personalizavimų atkurti neįmanoma. Todėl prieš atlikdami šią užduotį būtinai eksportuokite visus personalizavimus, kurių vėliau gali prireikti.

Vartotojai, kurie turi prieigą prie puslapio **Personalizavimas**, taip pat gali importuoti asmeninius arba šablonų rodinius, naudodami veiksmų srities mygtuką **Importuoti rodinius**.

## <a name="personalizing-inventory-dimensions"></a>Atsargų dimensijų personalizavimas

Personalizuodami puslapyje atsargų dimensijų sąranką, atsižvelkite į parametrus, kurie buvo sukurti naudojant parinktį **Rodyti dimensiją**. Pavyzdžiui, naudojate personalizavimą, norėdami paslėpti paketo numerio atsargų dimensijos stulpelį, tačiau stulpelis rodomas kitą kartą atidarius puslapį. Taip atsitinka todėl, kad atsargų dimensijų stulpelių rodymas valdomas naudojant parametrus **Dimensijos rodinys**. Parametrai **Dimensijos rodinys** taikomi visuose puslapiuose ir naudojantis šiais parametrais panaikinamos visos personalizuotos atskirų puslapių atsargų dimensijų laukų sąrankos.

Todėl ankstesniame pavyzdyje, jei nenorite, kad puslapyje būtų rodomas paketo numerio atsargų dimensijos stulpelis, turite tame puslapyje panaikinti tos dimensijos parinkties **Rodyti dimensijas** žymėjimą.
