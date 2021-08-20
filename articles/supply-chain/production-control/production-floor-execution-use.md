---
title: Kaip darbuotojai naudoja gamybos cecho vykdymo sąsają
description: Šioje temoje aprašoma, kaip darbuotojo atžvilgiu naudoti gamybos cecho vykdymo sąsają.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c2215ae4162616fec892a8bce6cff5d5f68e5aa1457b41d86bb540bdcff87197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747870"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Kaip darbuotojai naudoja gamybos cecho vykdymo sąsają

[!include [banner](../includes/banner.md)]

Gamybos cecho vykdymo sąsaja yra optimizuota lietimo sąveikai. Jos dizainas suteikia vaizdo kontrastingumą, atitinkantį pritaikymo neįgaliesiems reikalavimus cecho aplinkose. Jis siūlo visas tas pačias funkcines galimybes kaip ir užduoties kortelės įrenginys. Tačiau ji taip pat leidžia vienu metu pradėti kelias užduočių sąrašo užduotis. (Ši galimybė taip pat vadinama *užduočių grupavimu*.) Be to, užduočių sąraše darbuotojai gali atidaryti vadovą, sukurtą „Microsoft Dynamics 365” vadove. Tokiu būdu galima gauti vaizdines „HoloLens” instrukcijas.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Prisijungimas prie gamybos cecho vykdymo sąsajos kaip darbuotojas

Kad darbuotojai galėtų pradėti naudoti įrenginį, prižiūrėtojas arba techniniai darbuotojai turi jį paruošti ir atidaryti tinkamą „Dynamics 365 Supply Chain Management” puslapį. Daugiau informacijos apie tai, kaip nustatyti įrenginį, žr. [Įrenginio nustatymas siekiant vykdyti gamybos cecho vykdymo sąsają](production-floor-execution-setup.md).

Kai įrenginys paruoštas, jame atsiranda prisijungimo puslapis. Šiame puslapyje pateikiama informacija apie vietinių darbo elementų užduočių būsenas. Ši informacija periodiškai atnaujinama. Puslapyje darbuotojai naudoja savo ženklo ID, kad prisijungtų. Nors darbuotojai neprivalo turėti „Supply Chain Management” vartotojo abonemento, jie privalo turėti *registruojamo laiko darbuotojo* abonementą, kurį gali naudoti prisijungdami.

![Gamybos cecho vykdymo sąsajos prisijungimo puslapis.](media/pfei-sign-in-page.png "Gamybos cecho vykdymo sąsajos prisijungimo puslapis")

Likę šios temos skyriai apibūdina, kaip darbuotojai naudoja sąsają.

## <a name="all-jobs-tab"></a>Skirtukas Visos užduotys

Skirtuke **Visos užduotys** pateikiamas užduočių sąrašas, kuriame nurodytos visos gamybos užduotys, kurių būsena yra *Nepradėta*, *Sustabdyta* arba *Pradėta*. (Šį skirtuko pavadinimą galima tinkinti ir jūsų sistemoje jis gali būti kitoks.)

![Skirtukas Visos užduotys.](media/pfei-all-jobs-tab.png "Skirtukas Visos užduotys")

Užduočių sąraše yra toliau pateikti stulpeliai. Skaičiai atitinka skaičius ankstesnėje iliustracijoje.

1. **Pasirinkimo stulpelis** – kairioje pusėje esantis stulpelis naudoja žymės varneles užduotims, kurias pasirinko darbuotojas, nurodyti. Vienu metu darbuotojai gali pasirinkti kelias sąrašo užduotis. Norėdami pasirinkti visas sąrašo užduotis, pažymėkite žymės langelį stulpelio antraštėje. Pasirinkus vieną užduotį, informacija apie šią užduotį rodoma apatinėje puslapio dalyje.
1. **Užduoties būsenos stulpelis** – šiame stulpelyje naudojami simboliai kiekvienos užduoties būsenai nurodyti. Užduočių, kurių simbolio šiame stulpelyje nėra, būsena yra *Nepradėta*. Žalias trikampis nurodo užduotis, kurių būsena yra *Pradėta*. Dvi geltonos vertikalios linijos nurodo užduotis, kurių būsena yra *Sustabdyta*.
1. **Didelio prioriteto stulpelis** – šiame stulpelyje naudojami šauktuko ženklai užduotims, kurių prioritetas didelis, nurodyti.
1. **Užsakymas** – šiame stulpelyje rodomas užduoties gamybos užsakymo numeris.
1. **Aprašas** – šiame stulpelyje rodomas operacijos, kurios dalis yra užduotis, aprašas.
1. **Pageidaujama** – šiame stulpelyje rodomas kiekis, kurį užduotis planuoja pagaminti.
1. **Pradėta** – šiame stulpelyje rodomas jau pradėtas užduoties kiekis.
1. **Užbaigta** – šiame stulpelyje rodomas jau užbaigtas užduoties kiekis.
1. **Nurašyta** – šiame stulpelyje rodomas nurašytas užduoties kiekis.
1. **Liko** – šiame stulpelyje rodomas kiekis, kurį užduotis dar turi atlikti.

## <a name="active-jobs-tab"></a>Skirtukas Aktyvios užduotys

Skirtukuose **Aktyvios užduotys** rodomas visų užduočių, kurias prisijungęs darbuotojas jau pradėjo, sąrašas. (Šį skirtuko pavadinimą galima tinkinti ir jūsų sistemoje jis gali būti kitoks.)

![Skirtukas Aktyvios užduotys.](media/pfei-active-jobs-tab.png "Skirtukas Aktyvios užduotys")

Aktyvių užduočių sąraše yra toliau pateikti stulpeliai:

- **Pasirinkimo stulpelis** – kairioje pusėje esantis stulpelis naudoja žymės varneles užduotims, kurias pasirinko darbuotojas, nurodyti. Vienu metu darbuotojai gali pasirinkti kelias sąrašo užduotis. Norėdami pasirinkti visas sąrašo užduotis, pažymėkite žymės langelį stulpelio antraštėje. Pasirinkus vieną užduotį, informacija apie šią užduotį rodoma apatinėje puslapio dalyje.
- **Užsakymas** – šiame stulpelyje rodomas užduoties gamybos užsakymo numeris.
- **Aprašas** – šiame stulpelyje rodomas operacijos, kurios dalis yra užduotis, aprašas.
- **Pageidaujama** – šiame stulpelyje rodomas kiekis, kurį užduotis planuoja pagaminti.
- **Pradėta** – šiame stulpelyje rodomas jau pradėtas užduoties kiekis.
- **Užbaigta** – šiame stulpelyje rodomas jau užbaigtas užduoties kiekis.
- **Nurašyta** – šiame stulpelyje rodomas nurašytas užduoties kiekis.
- **Liko** – šiame stulpelyje rodomas kiekis, kurį užduotis dar turi atlikti.

## <a name="my-machine-tab"></a>Skirtukas Mano mašina

Skirtukas **Mano mašina** leidžia darbuotojams pasirinkti turtą, kuris yra sujungtas su įrenginio ištekliais, esančiais skirtuko **Visos užduotys** filtrų rinkinyje. Tada darbuotojas gali peržiūrėti pasirinkto turto būseną ir sveikatą skaitydamas vertes (ne daugiau keturių pasirinktų skaitiklių) ir naujausių priežiūros užklausų bei užregistruotų prastovų sąrašus. Darbuotojas taip pat gali reikalauti pasirinkto turto priežiūros ir registruoti bei redaguoti įrenginio prastovą. (Šį skirtuko pavadinimą galima tinkinti ir jūsų sistemoje jis gali būti kitoks.)
 
![Mano mašina skirtukas.](media/pfei-my-machine-tab.png "Skirtukas Mano mašina")

Skirtuke **Mano mašina** yra šie stulpeliai. Skaičiai atitinka skaičius ankstesnėje iliustracijoje.

1. **Mašinos turtas** – pasirinkite įrenginio turtą, kurį norite sekti. Pradėkite vesti pavadinimą, kurį norite pasirinkti iš sutampančių turtų sąrašo arba pasirinkite padidinamo stiklo piktogramą, kad pasirinktumėte iš viso turto, susieto su užduočių sąrašo filtro ištekliais, sąrašo.

    > [!NOTE]
    > „Supply Chain Management” vartotojai gali priskirti išteklius kiekvienam turtui, kaip reikalinga, naudodami **Visas turtas** puslapį (skirtuke **Ilgalaikis turtas** naudojant **Ištekliai** išplečiamąjį sąrašą). Daugiau informacijos žiūrėkite[Turto kūrimas](../asset-management/objects/create-an-object.md).

1. **Nustatymai** – pasirinkite pavarų piktogramą atidaryti dialogo langui, kuriame galėsite pasirinkti, kuriuos skaitiklius peržiūrėti pasirinktam įrenginio turtui. Šių skaitiklių reikšmės rodomos skirtuko **Turto valdymas** viršuje. Meniu **Parametrai** (rodomas toliau pateiktoje ekrano nuotraukoje) leidžia įgalinti ne daugiau keturių skaitiklių. Skaitiklio pasirinkimui naudokite peržvalgos lauką, esantį plytelės viršuje, kiekvienam skaitikliui, kurį norite įgalinti. Peržvalgos lauke pateikiami visi su turtu susiję skaitikliai, pasirinkti puslapio **Turto valdymas** viršuje. Nustatykite kiekvieną skaitiklį stebėti arba **Bendrą** arba **Faktinę** skaitiklio reikšmę. Pavyzdžiui, jei nustatote skaitiklį sekti, kiek valandų veikia mašina, tada turite nustatyti jį kaip **Bendra**. Jei nustatote skaitiklį matuoti vėliausią atnaujintą temperatūrą ar slėgį, tada turite nustatyti jį kaip **Faktinė**. Norėdami įrašyti parametrus ir uždaryti dialogo langą, pasirinkite **Gerai**.

    ![Skirtuko Mano mašina parametrai.](media/pfei-my-machine-tab-settings.png "Skirtuko Mano mašina parametrai")

1. **Priežiūros užklausa** – pasirinkite šį mygtuką, jei norite atidaryti dialogo langą, kuriame galite sukurti priežiūros užklausą. Galėsite pateikti aprašą ir pastabą. Užklausa bus pateikta „Supply Chain Management” vartotojui, kuris tada galės konvertuoti priežiūros užklausą į priežiūros darbo užsakymą.
1. **Registruoti prastovą** – pasirinkite šį mygtuką, jei norite atidaryti dialogo langą, kuriame galite registruoti įrenginio prastovą. Galėsite pasirinkti priežasties kodą ir įvesti prastovos datos / laiko trukmę. Įrenginių prastovos registracija naudojama skaičiuojant įrenginio turto efektyvumą.
1. **Peržiūrėti arba redaguoti** – pasirinkite šį mygtuką, jei norite atidaryti dialogo langą, kuriame galite redaguoti arba peržiūrėti esamus prastovos įrašus.


## <a name="starting-and-completing-production-jobs"></a>Gamybos užduočių pradžia ir pabaiga

Darbuotojai pradeda gamybos užduotį, pasirinkdami užduotį skirtuke **Visos užduotys** ir tada pasirinkdami **Pradėti užduotį**, kad būtų atidarytas dialogo langas **Pradėti užduotį**.

![Dialogo langas Pradėti užduotį.](media/pfei-start-job-dialog.png "Dialogo langas Pradėti užduotį")

Darbuotojai naudoja dialogo langą **Pradėti užduotį**, kad patvirtintų gamybos kiekį ir pradėtų užduotį. Darbuotojai gali koreguoti kiekį pasirinkdami lauką **Kiekis** ir naudodami atsiradusią skaičių klaviatūrą. Tada darbuotojai pasirenka **Pradėti**, kad pradėtų dirbti su užduotimi. Dialogo langas **Pradėti užduotį** uždaromas, o užduotis įtraukiama į skirtuką **Aktyvios užduotys**.

Darbuotojai gali pradėti bet kokios būsenos užduotį. Kai darbuotojas pradeda užduotį, kurios būsena yra *Nepradėta*, dialogo lango **Pradėti užduotį** lauke **Kiekis** iš pradžių rodomas visas kiekis. Kai darbuotojas pradeda užduotį, kurios būsena yra *Pradėta* arba *Sustabdyta*, lauke **Kiekis** iš pradžių rodomas likęs kiekis.

## <a name="reporting-good-quantities"></a>Prekių kiekių ataskaitos

Kai darbuotojas užbaigia arba iš dalies užbaigia užduotį, jis gali pateikti prekių kiekių, kurie buvo pagaminti, ataskaitą, pasirinkdamas užduotį skirtuke **Aktyvios užduotys** ir tada – **Teikti ataskaitą apie eigą**. Tada dialogo lange **Teikti ataskaitą apie eigą** darbuotojas įveda prekių kiekį naudodamas skaičių klaviatūrą. Kiekio laukas pagal numatytuosius nustatymus yra tuščias. Įvedęs kiekį, darbuotojas gali atnaujinti užduoties būseną į *Vykdoma*, *Sustabdyta* arba *Baigta*.

![Dialogo langas Teikti ataskaitą apie eigą.](media/pfei-report-progress-dialog.png "Dialogo langas Teikti ataskaitą apie eigą")

## <a name="reporting-scrap"></a>Atliekų ataskaitos

Kai darbuotojas užbaigia arba iš dalies užbaigia užduotį, jis gali pateikti atliekų ataskaitą, pasirinkdamas užduotį skirtuke **Aktyvios užduotys** ir tada – **Teikti ataskaitą apie atliekas**. Tada dialogo lange **Teikti ataskaitą apie atliekas** darbuotojas įveda atliekų kiekį naudodamas skaičių klaviatūrą. Darbuotojas taip pat pasirenka priežastį (*Nėra*, *Įrenginys*, *Operatorius* arba *Medžiagos*).

![Dialogo langas Teikti ataskaitą apie atliekas.](media/pfei-report-scrap-dialog.png "Dialogo langas Teikti ataskaitą apie atliekas")

## <a name="completing-a-job-and-starting-a-new-job"></a>Užduoties užbaigimas ir naujos užduoties pradėjimas

Paprastai darbuotojai užbaigia užduotį pasirinkdami vieną ar daugiau dabartinių užduočių skirtuke **Aktyvios užduotys** ir tada pasirinkdami **Teikti ataskaitą apie eigą**. Tada jie įveda pagamintą kiekį (prekių kiekį) ir nustato būseną į *Baigta*. Jei pasirinkta daugiau nei viena užduotis, darbuotojas naudoja mygtukus **Ankstesnis** ir **Sekantis**, norėdamas pereiti nuo vienos prie kitos užduoties. Norėdamas sukurti naują užduotį, darbuotojas ją pasirenka skirtuke **Visos užduotys** ir tada pasirenka **Pradėti užduotį**.

Darbuotojas taip pat gali pradėti naują užduotį, kol ankstesnė užduotis vis dar atidaryta. Vėlgi, darbuotojas pasirenka naują užduotį skirtuke **Visos užduotys** ir tada pasirenka **Pradėti užduotį**. Tačiau šiuo atveju dialogo langas **Pradėti užduotį** praneša darbuotojui, kad jie šiuo metu dirba su užduotimi, todėl jie turi sustabdyti arba užbaigti tą užduotį prieš pradedami naują užduotį.

## <a name="working-on-multiple-jobs-in-parallel"></a>Darbas su keliomis užduotimis vienu metu

Vienas darbuotojas vienu metu gali dirbti su keliomis užduotimis (t. y. lygiagrečiai). Tokiu atveju užduočių, su kuriomis dirba darbuotojas, rinkinys vadinamas *užduočių grupe*. Darbuotojas gali įtraukti naujų užduočių į grupę arba užbaigti vieną ar daugiau grupės užduočių. Toliau pateikti du scenarijai rodo, kaip darbuotojas gali dirbti su užduotimis lygiagrečiai.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>1 scenarijus. Darbuotojas, neturintis aktyvių užduočių, nori pradėti dvi užduotis ir dirbti su jomis lygiagrečiai

Darbuotojas pasirenka tas dvi užduotis skirtuke **Visos užduotys** ir tada pasirenka **Pradėti užduotį**. Dialogo lange **Pradėti užduotį** rodomos abi pasirinktos užduotys, o darbuotojas gali koreguoti kiekį, kad pradėtų darbą su kiekviena užduotimi. Tada darbuotojas patvirtina dialogo langą ir gali pradėti abi užduotis.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>2 scenarijus. Darbuotojas, turintis dvi aktyvias atliekamas užduotis, nori pradėti trečią užduotį ir dirbti su tomis dvejomis užduotimis lygiagrečiai

Darbuotojas pasirenka trečią užduotį skirtuke **Visos užduotys** ir tada pasirenka **Grupavimas**. Dialogo lange **Grupavimas** darbuotojas gali koreguoti kiekį, kad pradėtų darbą. Tada darbuotojas patvirtina dialogo langą pasirinkdamas **Grupavimas**.

## <a name="working-on-indirect-activities"></a>Darbas su netiesioginėmis veiklomis

Netiesioginės veiklos yra veiklos, kurios nėra tiesiogiai susijusios su gamybos užsakymu. Netiesioginės veiklos gali būti lanksčiai apibrėžtos, kaip aprašyta [Laiko ir buvimo darbe netiesioginių veiklų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Pavyzdžiui, „Contoso” cecho darbuotoja Shannon nori dalyvauti įmonės susitikime, o susitikimai laikomi netiesiogine veikla. Taikomas vienas iš toliau pateiktų dviejų scenarijų.

- **Shannon dirba su viena ar daugiau aktyvių užduočių.** Shannon pasirenka **Veikla**, nurodo veiklą (susitikimas) ir patvirtina pasirinkimą. Pasirodo pranešimas, kuriame pranešama, kad ji turi nebaigtų užduočių. Shannon gali pasirinkti užbaigti arba sustabdyti užduotis, su kuriomis ji dirba, prieš eidama į susitikimą.
- **Shannon neturi aktyvių užduočių.** Shannon pasirenka **Veikla**, nurodo veiklą (susitikimas) ir patvirtina pasirinkimą. Dabar ji užregistruota kaip dalyvaujanti susitikime.

Abiem atvejais, kai Shannon patvirtina jos pasirinkimą, ji pereina prie prisijungimo puslapio arba puslapio, laukiančio, kol ji patvirtins, kad sugrįžo po netiesioginės veiklos. Atsiradęs puslapis priklauso nuo gamybos cecho vykdymo sąsajos konfigūracijos. (Daugiau informacijos žr. [Gamybos cecho vykdymo sąsajos konfigūravimas](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Pertraukų registravimas

Darbuotojai gali registruoti pertraukas. Pertraukas galima lanksčiai apibrėžti, kaip aprašyta [Apmokėjimas pagal registracijas](pay-based-on-registrations.md).

Darbuotojas užregistruoja pertrauką pasirinkdamas **Pertrauka**, tada pasirinkdamas kortelę, vaizduojančią pertraukos tipą (pvz., pietūs). Darbuotojui patvirtinus pasirinkimą, įrenginys rodo prisijungimo puslapį arba puslapį, laukiantį, kol darbuotojas patvirtins, kad grįžo po pertraukos. Atsiradęs puslapis priklauso nuo gamybos cecho vykdymo sąsajos konfigūracijos. (Daugiau informacijos žr. [Gamybos cecho vykdymo sąsajos konfigūravimas](production-floor-execution-configure.md).)

## <a name="opening-instructions"></a>Instrukcijų atidarymas

Darbuotojai gali atidaryti dokumentą, pridėtą prie užduoties, pasirinkdami **Instrukcijos**. Mygtukas **Instrukcijos** pasiekiamas, jei dokumentas susietas su užduotimi bendruosiuose duomenyse. Pavyzdžiui, dokumentą, pridėtą prie produkto „Supply Chain Management” puslapyje **Išleisti produktai**, darbuotojai galės atidaryti cecho vykdymo sąsajoje.

## <a name="opening-mixed-reality-guides-for-hololens"></a>„HoloLens” mišriosios realybės vadovų atidarymas

[„Dynamics 365 Guides”](https://dynamics.microsoft.com/mixed-reality/guides/) gali padėti darbuotojams suteikdama praktinį mokymąsi, kurio metu naudojama mišrioji realybė. Galite apibrėžti standartinius procesus su nuosekliomis instrukcijomis, kurios padės jūsų darbuotojams naudoti reikalingus įrankius ir dalis bei suteiks informacijos, kaip naudoti šiuos įrankius realiose darbo situacijose. Toliau pateikta proceso apžvalga.

1. Kiekvieną kartą, kai darbuotojas atidaro užduočių sąrašą cecho vykdymo sąsajoje, sąsaja randa visus atitinkamus vadovus rodomoms užduotims.
1. Darbuotojas pasirenka **Vadovai**, norėdamas peržiūrėti vadovų sąrašą.
1. Darbuotojas pasirenka atitinkamą vadovą sąraše.
1. Cecho vykdymo sąsajoje rodomas pasirinkto vadovo QR kodas.
1. Darbuotojas užsideda „HoloLens” ir žvilgteli į QR kodą, kad vadovas būtų pradėtas.
1. Darbuotojas dirba su vadovu, kad sužinotų apie užduotį.

Daugiau informacijos apie tai, kaip kurti, priskirti ir naudoti „HoloLens” vadovus, žr. [Mišriosios realybės vadovų teikimas vadovams gamybos metu](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]