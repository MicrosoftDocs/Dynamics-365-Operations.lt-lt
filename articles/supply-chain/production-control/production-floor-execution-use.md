---
title: Kaip darbininkai naudoja gamybos vietos vykdymo sąsają
description: Šiame straipsnyje aprašoma, kaip naudoti gamybos laiko vykdymo sąsają darbuotojo požiūriu.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 876ee36c75a31ca89a9351d0ee1484e66076b6aa
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748719"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Kaip darbuotojai naudoja gamybos cecho vykdymo sąsają

[!include [banner](../includes/banner.md)]

Gamybos cecho vykdymo sąsaja yra optimizuota lietimo sąveikai. Jos dizainas suteikia vaizdo kontrastingumą, atitinkantį pritaikymo neįgaliesiems reikalavimus cecho aplinkose. Jis siūlo visas tas pačias funkcines galimybes kaip ir užduoties kortelės įrenginys. Tačiau ji taip pat leidžia vienu metu pradėti kelias užduočių sąrašo užduotis. (Ši galimybė taip pat vadinama *užduočių grupavimu*.) Be to, užduočių sąraše darbuotojai gali atidaryti vadovą, sukurtą „Microsoft Dynamics 365” vadove. Tokiu būdu galima gauti vaizdines „HoloLens” instrukcijas.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Prisijungimas prie gamybos cecho vykdymo sąsajos kaip darbuotojas

Kad darbuotojai galėtų pradėti naudoti įrenginį, prižiūrėtojas arba techniniai darbuotojai turi jį paruošti ir atidaryti tinkamą „Dynamics 365 Supply Chain Management” puslapį. Daugiau informacijos apie tai, kaip nustatyti įrenginį, žr. [Įrenginio nustatymas siekiant vykdyti gamybos cecho vykdymo sąsają](production-floor-execution-setup.md).

Kai įrenginys paruoštas, jame atsiranda prisijungimo puslapis. Šiame puslapyje pateikiama informacija apie vietinių darbo elementų užduočių būsenas. Ši informacija periodiškai atnaujinama. Puslapyje darbuotojai naudoja savo ženklo ID, kad prisijungtų. Nors darbuotojai neprivalo turėti „Supply Chain Management” vartotojo abonemento, jie privalo turėti *registruojamo laiko darbuotojo* abonementą, kurį gali naudoti prisijungdami.

![Gamybos cecho vykdymo sąsajos prisijungimo puslapis.](media/pfei-sign-in-page.png "Gamybos cecho vykdymo sąsajos prisijungimo puslapis")

Likusiuose šio straipsnio skyriuose aprašoma, kaip darbuotojai sąveikauja su sąsaja.

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

## <a name="my-jobs-tab"></a>Skirtukas Mano užduotys

Skirtukas **Mano** užduotys leidžia darbuotojams lengvai peržiūrėti visas nebaigtas ir specialiai jiems priskirtas užduotis. Tai naudinga įmonėse, kurių užduotys kartais arba visada priskiriamos konkretiems darbuotojams (žmogiškieji ištekliai), o ne kitų tipų ištekliams (pvz., įrenginiai).

Planavimo sistema automatiškai priskiria kiekvieną gamybos užduotį konkrečiam išteklių įrašui, o kiekvieno išteklių įrašo tipas (pvz., mašina arba žmogus). Kai nustatote darbuotoją kaip gamybos darbuotoją, galite susieti darbuotojo sąskaitą su unikaliu personalo įrašu.

Skirtuke **Mano** užduotys išvardytos visos neatliktos ir neužbaigtos užduotys, priskirtos prisiregistravęo darbuotojo personalo įrašui, jei prisiregistravęs darbuotojas yra prisiregistravęs. Joje niekada neišvardijamos užduotys, priskirtos įrenginiams ar kito tipo ištekliams, net jei prisiregistravęs darbuotojas pradėjo su tomis užduotimis dirbti.

Norėdami peržiūrėti visas pasirašyto darbuotojo pradėtas užduotis, neatsižvelgiant į išteklių, prie kurių priskirta kiekviena užduotis, tipą, **naudokite skirtuką Aktyvios** užduotys. Norėdami peržiūrėti visas nebaigtas užduotis, kurios atitinka vietinio užduočių filtro konfigūraciją, nepaisant darbuotojo arba pradžios būsenos, **naudokite skirtuką Visos** užduotys.

![Mano užduočių skirtukas.](media/pfei-my-jobs-tab.png "Skirtukas Mano užduotys")

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

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Teikti ataskaitą apie paketiniū užsakymų gerus kiekius, kurie turi sudėtinius ir šalutinius produktus

Darbuotojai gali naudoti gamybos vietos vykdymo sąsają pateikti informaciją apie partijinių užsakymų eigą. Ši ataskaita apima ataskaitos teikimą apie sudėtinius ir šalutinius produktus.

Kai kurie gamintojai, ypač proceso pramonės šakose, paketinius užsakymus naudoja savo gamybos procesams valdyti. Paketiniai užsakymai kuriami pagal formules, tas formules galima nustatyti taip, kad jų išeiga būtų sudėtiiniai ir šalutiniai produktai. Kai pranešamas tų paketinių užsakymų grįžtamasis ryšys, išeigos suma turi būti užregistruota formulėje ir taip pat sudėtiuose bei šalutiniuose produktuose.

Kai darbuotojas užbaigia arba dalinai atlieka paketinio užsakymo užduotį, jie gali pranešti apie kiekvieno produkto, kuris nurodytas kaip užsakymo išeiga, gerų arba nurašomų į atliekas kiekius. Produktų, kurie apibrėžti kaip paketinio užsakymo išeiga gali būti *Formulės*, *Sudėtinio produkto* ar *Šalutinioprodukto* tipo.

Norint pateikti gerų produktų kiekių ataskaitą, darbuotojas pasirenka užduotį skirtuke **Aktyvios užduotys** ir tada pasirenka **Teikti ataskaitą apie eigą**.

Tada **Teikti ataskaitą apie eigą** dialogo lange darbuotojas gali pasirinkti iš produktų, kurie apibrėžti kaip paketinio užsakymo išeiga, apie kuriuos bus teikiamos ataskaitos. Darbuotojas sąraše gali pasirinkti vieną arba daug produktų, tada pasirinkti **Teikti ataskaitą apie eigą**. Kiekvienam produktui pagal numatytuosius nustatymus kiekis yra tuščias, o darbuotojas kiekiui įvesti gali naudoti skaitinę klaviatūrą. Darbuotojas gali naudoti **Ankstesnis** ir **Sekantis** mygtukus, norėdamas judėti tarp pasirinktų produktų. Įvedęs kiekvieno produkto kiekį, darbuotojas gali atnaujinti užduoties būseną į *Vykdoma*, *Sustabdyta* arba *Baigta*.

![Teikti ataskaitą apie sudėtinius ir šalutinius produktus.](media/report-co-by-products.png "Teikti ataskaitą apie sudėtinius ir šalutinius produktus.")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Teikti ataskaitą apie planavimo prekių paketinius užsakymus

Kai darbuotojas baigia užduotį planavimo prekės paketiniame užsakyme, bus pateikta ataskaita tik apie sudėtinių ir šalutinių produktų kiekį, kadangi planavimo prekės neturi *Formulės* tipo prekės.

### <a name="reporting-co-product-variation"></a>Teikti ataskaitą apie sudėtinio produkto variaciją

Jei paketinis užsakymas sukurtas pagal formulės versiją, kai **Sudėtinio produkto variacijos** pasirinkimas nustatytas į *Taip*, darbuotojas gali pranešti apie sudėtinius produktus, kurie nėra paketinių užsakymų aprašo dalis. Ši funkcija naudojama scenarijuose, kur gamybos procese gali atsirasti netikėta produkto išeiga.

Tokiu atveju, darbuotojas gali pateikti ataskaitą apie sudėtinio produkto kiekį ataskaitų eigos dialogo lange pasirinkdamas **Sudėtinio produkto variacijos**. Tuomet darbuotojas gali pasirinkti iš visų išleistų produktų, apibrėžtų kaip sudėtiniai produktai.

### <a name="reporting-catch-weight-items"></a>Esamo svorio prekių ataskaita

Darbuotojai gali naudoti gamybos laiko vykdymo sąsają norėdami pranešti apie paketinių užsakymų, sukurtų esamo svorio prekėms, eigą. Paketiniai užsakymai kuriami pagal formules, kurias galima apibrėžti kaip esamo svorio prekes kaip sudėties prekes, sudėtinius produktus ir pagal produktus. Formulę taip pat galima apibrėžti, kad ji turėtų formulės eilutes, skirtas ingredientams, kurie apibrėžti kaip esamo svorio. Esamo svorio prekės turi sekti atsargas pagal du matavimo vienetus: esamo svorio kiekį ir atsargų kiekį. Pavyzdžiui, maisto pramonėje dėžes galima nurodyti kaip esamo svorio prekę, kur esamo svorio kiekis naudojamas dėžių kiekiui sekti, o atsargų kiekis naudojamas dėžių svoriui sekti.

## <a name="reporting-scrap"></a>Atliekų ataskaitos

Kai darbuotojas užbaigia arba iš dalies užbaigia užduotį, jis gali pateikti atliekų ataskaitą, pasirinkdamas užduotį skirtuke **Aktyvios užduotys** ir tada – **Teikti ataskaitą apie atliekas**. Tada dialogo lange **Teikti ataskaitą apie atliekas** darbuotojas įveda atliekų kiekį naudodamas skaičių klaviatūrą. Darbuotojas taip pat pasirenka priežastį (*Nėra*, *Įrenginys*, *Operatorius* arba *Medžiagos*).

![Dialogo langas Teikti ataskaitą apie atliekas.](media/pfei-report-scrap-dialog.png "Dialogo langas Teikti ataskaitą apie atliekas")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Koreguoti medžiagų suvartojimą ir rezervuoti medžiagas

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Darbuotojai gali koreguoti kiekvienos gamybos užduoties medžiagų suvartojimą. Ši funkcija naudojama scenarijuose, kuriuose faktinis medžiagų kiekis, kurį sunaudojo gamybos užduotis, buvo didesnis arba mažesnis nei suplanuotas kiekis. Todėl jį reikia koreguoti, kad būtų galima išlaikyti esamą atsargų lygį.

Darbuotojai taip pat gali rezervuoti paketų ir medžiagų serijos numerius. Ši funkcija naudojama scenarijuose, kuriuose darbuotojas turi neautomatiniu būdu nurodyti, kuris medžiagos paketas arba serijos numeris buvo suvartotas, kad atitiktų medžiagų poreikių reikalavimus.

Darbuotojai gali nurodyti koreguoti kiekį pasirinkdami Koreguoti **medžiagą**. Šį mygtuką galima naudoti šiose vietose:

- Ataskaitos nurašymo **dialogo** lange
- **Ataskaitos eigos dialogo** lange
- Dešinėje įrankių juostoje

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Medžiagų suvartojimo koregavimas ataskaitų nurašymo ir ataskaitos eigos dialogo languose

Kai darbuotojas įveda kiekį, kuris turi būti nurodytas **ataskaitų** **eigos** arba ataskaitos nurašymo ataskaitos dialogo lange, **mygtukas Koreguoti** medžiagą tampa galimas. Vartotojui pasirinkus šį mygtuką, pasirodys **dialogo langas Koreguoti** medžiagas. Šiame dialogo lange pateikiamas prekių, suplanuotų suvartoti pranešant apie užduoties prekių ar nurašytų į atliekas kiekį, sąrašas.

Sąrašas dialogo lange rodo šią informaciją:

- **Produkto numeris** – bendrasis produktas ir produkto variantas.
- **Produkto pavadinimas** – produkto pavadinimas.
- **Pasiūlymas** – įvertintas medžiagų kiekis, kuris bus suvartotas pranešant apie progresą ar nurašytą nurodytą užduoties kiekį.
- **Suvartojimas** – faktinis medžiagų kiekis, kuris bus suvartotas pranešant apie progresą ar nurašytą nurodytą užduoties kiekį.
- **Rezervuotas** – medžiagos kiekis, kuris buvo faktiškai rezervuotas atsargose.
- **Vienetas** – komplektavimo specifikacijos (KS) vienetas.

Dešinėje dialogo lango pusėje rodoma ši informacija:

- **Produkto numeris** – bendrasis produktas ir produkto variantas.
- **Įvertintas** – įvertintas sunaudoti kiekis.
- **Pradėta** – kiekis, pradėtas gamybos užduotyje.
- **Likęs** kiekis – įvertinto kiekio, likusio suvartoti kiekio.
- **Išleistas** kiekis – suvartotas kiekis.

Gali būti atlikti šie veiksmai:

- Darbuotojas gali nurodyti medžiagos kiekį, pasirinkdamas Koreguoti **suvartojimą**. Patvirtinus kiekį, suvartojimo stulpelyje nurodytas **kiekis** atnaujinamas pakoreguotu kiekiu.
- Darbuotojui pasirinkus Koreguoti **medžiagą**, sukuriamas gamybos išrinkimo dokumento žurnalas. Šiame žurnale yra tos pačios prekės ir kiekiai kaip ir Koreguotų **medžiagų** sąraše.
- Kai darbuotojas koreguoja kiekį dialogo lange **Koreguoti** medžiagas, **atitinkamos** žurnalo eilutės laukas Pasiūlymas atnaujinamas tuo pačiu kiekiu. Jei darbuotojas dialogo lange **Koreguoti** medžiagas **pasirenka** Atšaukti, išrinkimo sąrašas panaikinamas.
- Jei darbuotojas pasirenka Gerai **, išrinkimo sąrašas nėra panaikinamas**. Jis bus registruojamas, kai užduotis bus paskelbta dialogo lange **Ataskaitos nurašymas** **arba** Ataskaitos eiga.
- Jei ataskaitos eigos arba **ataskaitos nurašymo** dialogo lange **darbuotojas** pasirenka **Atšaukti, išrinkimo sąrašas panaikinamas**.

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>Koreguoti medžiagą iš pirminės arba antrinės įrankių juostos

Mygtuką **Koreguoti medžiagą galima** konfigūruoti, kad jis būtų rodomas pirminėje arba antrinėje įrankių juostoje. (Daugiau informacijos žr. [Sukurkite gamybos laiko vykdymo sąsają](production-floor-execution-tabs.md).) Darbuotojas gali pasirinkti **koreguoti gaminamos** gamybos užduoties medžiagą. Tokiu atveju pasirodys dialogo langas **Koreguoti medžiagą**, kuriame darbuotojas gali atlikti norimus koregavimus. Kai atidaromas dialogo langas, gamybos užsakymui sukuriamas gamybos išrinkimo sąrašas, kuriame yra pakoreguotų kiekių eilutės. Jei darbuotojas pasirenka Registruoti **dabar**, koregavimas patvirtinamas ir užregistruojamas išrinkimo sąrašas. Jei darbuotojas pasirenka Atšaukti **, išrinkimo sąrašas panaikinamas ir joks koregavimas** nebus atliktas.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Koreguoti esamo svorio prekių medžiagų suvartojimą

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Darbuotojai gali koreguoti esamo svorio prekių medžiagų suvartojimą. Ši funkcija naudojama scenarijuose, kuriuose faktinis esamo svorio medžiagų kiekis, kurį sunaudojo gamybos užduotis, buvo didesnis arba mažesnis nei suplanuotas kiekis. Todėl jį reikia koreguoti, kad būtų galima išlaikyti esamą atsargų lygį. Kai darbuotojas koreguoja esamo svorio prekės suvartojimą, jis gali koreguoti ir esamo svorio kiekį, ir atsargų kiekį. Pavyzdžiui, jei gamybos užduotis planuojama naudoti penkis langelius, kurių kiekvienos svoris įvertintas 2 kilogramais, darbuotojas gali koreguoti ir naudotinųjų dėžių skaičių, ir dėžių svorį. Sistema patikrins, ar nurodytas laukų svoris viršija nustatytą minimalią ir maksimalią ribinę vertę, apibrėžtą patvirtintame produkte.

### <a name="reserve-materials"></a>Rezervuoti medžiagas

Dialogo lange **Koreguoti medžiagas** darbuotojas gali atlikti ir koreguoti medžiagų rezervavimą, pasirinkdamas Rezervuoti **medžiagą**. Dialogo **langas Rezervuoti** medžiagas rodo kiekvienai saugojimo ir sekimo dimensijai skirtas faktiškai turimas prekės atsargas.

Jei medžiagos įgalintos sandėlio valdymo procesams (WMS), sąraše rodomos tik faktiškai turimos medžiagos įeimo vietos atsargos. Gamybos įvesties vieta nurodyta ištekliuje, kuriame suplanuota gamybos užduotis. Jei prekės numeris valdomas paketo arba serijos numeriu, rodomas visas faktiškai prieinamų paketo ir serijos numerių sąrašas. Norėdami nurodyti rezervuoti norimą kiekį, darbuotojas gali pasirinkti Rezervuoti **medžiagą**. Norėdami pašalinti esamą rezervavimą, darbuotojas gali pasirinkti Pašalinti **rezervavimą**.

Daugiau informacijos apie gamybos įvesties vietos nustatymą rasite šiame žurnalo skelbime: [gamybos įvesties vietos nustatymas](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Rezervavimai, kuriuos darbuotojas **atlieka** **·** **·** **dialogo lange Rezervuoti medžiagas, liks, kai dialogo lange Ataskaitos eiga arba Ataskaitos nurašyme darbuotojas pasirinksite** Atšaukti.
>
> Esamo svorio prekių rezervavimų koreguoti negalima.

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

## <a name="view-the-my-day-dialog"></a>Peržiūrėti dialogo langą "Mano diena"

Dialogo **lange Mano** diena darbuotojai pateikiami su savo registracijomis ir balansais. Dialogas padalintas į šiuos tris skyrius:

- Pagrindiniame skyriuje išvardijamos registracijos, kurias dabartinis darbuotojas atliko pasirinktą dieną. Ji atidaroma, rodant šios dienos registracijas ir pateikia datos išrinkėją, kuris leidžia darbuotojui peržiūrėti kitas dienas.
- Paskutiniame **apskaičiuotos dienos** balanso skyriuje rodomi dabartiniai darbuotojo apmokėto laiko, apmokėtų viršvalandžių, neatvykimų ir apmokėto neatvykimo balansai. Šios vertės paremtos registracijomis, apskaičiuotomis patvirtinimo proceso metu.
- Balansų **skyriuje** pateikiama pasirinktų registracijų kategorijų (pvz., atostogų, standartinio laiko ir viršvalandžių) balansų peržiūra apibrėžtu laikotarpiu. Šie balansai pagrįsti tuo, kaip statistiniai balansai nustatyti modulyje **Laikas ir lankomumas**. Daugiau informacijos apie tai, kaip nustatyti, žr. [Rodyti atostogų balansus gamybos laiko vykdymo sąsajoje](production-floor-execution-payroll-stats.md).

Administratoriai gali įtraukti šią **funkciją**[į sąsają, padėdami mygtuką Mano diena įrankių juostoje kiekvienam susijusiam skirtukui, kaip aprašyta dizaino gamybos laiko vykdymo sąsajoje.](production-floor-execution-tabs.md)

## <a name="working-in-teams"></a>Darbas komandose

Kai tai pačiai gamybos užduočiai priskirti keli darbuotojai, jie gali sudaryti komandą. Komanda gali paskirti vieną darbuotoją kaip vadininką. Likę darbuotojai automatiškai tampa to vad vadymi asistentais. Gautai komandai užduoties būseną turi užregistruoti tik vadovas. Laiko įrašai taikomi visiems komandos nariams.

### <a name="prerequisites"></a>Būtinieji komponentai

Norint naudotis komandomis, administratorius **·** **turi** įgalinti pagrindinės įrankių juostos asistento veiksmą gamybos laiko vykdymo sąsajos skirtuke Visos užduotys. Instrukcijų ieškokite Gamybos [laiko vykdymo sąsajos kūrimas](production-floor-execution-tabs.md).

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>Sukurti naują komandą, turi esančią vadovas ir asistentas

Darbuotojas gali registruotis kaip asistentas, skirtuke **Visos** užduotys **pasirinkdamas Asistentas**. Tada pasirodaajame **dialogo** lange Pasirinkti darbuotoją, kuris padės atlikti užduotis, darbuotojas gali pasirinkti darbuotojų, kurie aktyviai dirba su užduotimi, sąrašą. Darbuotojui patvirtinus jų pasirinkimą, jie tampa pasirinkto darbuotojo asistentu, kuris tampa naujos komandos vadu.

### <a name="assign-a-new-pilot-to-an-existing-team"></a>Priskirti naują vadovas esamai komandai

Kai komanda nori pasirinkti naują vadininką, dabartinis vadovas turi paskirti kitą komandos darbuotoją kaip naują vadininką. Paskirti naują vadininką, dabartinis pilotas skirtuke **Visos** užduotys **pasirenka asistentą**. Tada atidarytajame **dialogo lange** Keisti vadovas gali pasirinkti naują vadovas darbuotojų, kurie jau yra komandoje, sąraše. Kai dabartinis vadovas patvirtina savo pasirinkimą, jie visiškai numesta iš komandos. Tačiau, jei reikia, jie gali ir vėl būti komandos nariai.

### <a name="assistant-clocks-out"></a>Asistentas išeina iš darbo

Kai darbuotojas, kuris dirba kaip asistentas, išeina iš darbo, jis išeis iš komandos. Jei nuolatinės **komandos** ir **paleisti** *iš naujo atėjimo į darbą pasirinktys yra nustatytos kaip Taip*, darbuotojas, kuris išeina iš darbo, automatiškai kitą kartą ateis į darbą. Šias pasirinktis galite rasti laiko **ir lankomumo** parametrų **puslapio skirtuke** Bendra.

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
