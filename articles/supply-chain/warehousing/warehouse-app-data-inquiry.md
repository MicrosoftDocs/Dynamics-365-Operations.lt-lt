---
title: Duomenų užklausa naudojant „Warehouse Management“ mobiliosios programėlės apėjimus
description: Šiame straipsnyje aprašoma, kaip konfigūruoti duomenų užklausos mobiliojo įrenginio meniu elementus ir naudoti juos kaip atsietų elementų dalį.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 39677ebfb9babeb7246ece4d27ab1813435ca12e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427854"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Duomenų užklausa naudojant „Warehouse Management“ mobiliosios programėlės apėjimus

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Priemonės įžanga

Suteikdami brūkšninių kodų nuskaitymo galimybę, sandėlio valdymo mobilioji programa leidžia lengvai ir tiksliai fiksuoti duomenis kaip dalį sandėlio procesų. Tačiau brūkšniniai kodai kartais sugadinamas ir tampa neperskaitomas arba jūsų verslo proceso srautuose reikalinga duomenų informacija gali neegzistuoti kaip brūkšninis kodas. Tokiais atvejais neautomatinis duomenų įvedimas gali ilgai užtrukti ir net gali trukti neteisingus duomenis. Rezultatai gali būti sumažinti poveikis ir žemesnis aptarnavimo lygis.

Naudodami kintamų duomenų užklausų procesą darbuotojai gali lengvai peržiūrėti reikiamą informaciją kaip įdėtųjų sandėlio valdymo mobiliųjų programų srautų dalį ir taikyti filtravimo parinktis, kad būtų rodomi tik atitinkami duomenys. Todėl pasirinkimas neautomatiniu būdu yra greitesnis ir tikslesnis.

Pavyzdžiui, pirkimo užsakymo gavimo sraute, pirkimo užsakymo numeris turi atitikti gaunant atsargas. Kaip šio proceso dalį galite lengvai konfigūruoti meniu elementus, kad galėtumėte peržiūrėti atitinkamų pirkimo užsakymų numerių kortelių sąrašą. Tokiu būdu galite tęsti gavimo eigą naudodami sparčiojo "point-to-select" būdą. Šiame straipsnyje pateikiami pavyzdiniai scenarijai, tačiau funkcijas galima naudoti ir bet kuriame arba visuose sandėlio valdymo mobiliųjų programų srautuose.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Įjungti duomenų užklausos srauto priemonę ir jos būtinąsias sąlygas

Kad būtų galima naudoti šiame straipsnyje aprašytas funkcijas, reikia atlikti toliau aprašytą procedūrą, kad būtų galima įjungti reikalingas funkcijas.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**. (Daugiau informacijos apie tai, kaip naudoti **Funkcijų valdymo** darbo sritis, žr [. Funkcijų valdymo apžvalgą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Jei paleisite 10.0.28 ar ankstesnę tiekimo grandinės valdymo versiją, įjunkite toliau nurodytą funkciją:

    - **Modulis:** *Warehouse management*
    - **Funkcijos pavadinimas:** *Sandėlio programos veiksmų instrukcija*

    Ši funkcija yra būtina sandėlio valdymo programos *duomenų užklausų srauto funkcijos* sąlyga. Kaip tiekimo grandinės valdymo versija 10.0.29, ji yra privaloma ir negali būti išjungta. Daugiau informacijos apie *Warehouse programos veiksmų instrukcijų* funkciją žr. [Warehouse Management mobiliosios programos veiksmų pavadinimų ir instrukcijų pritaikymas](mobile-app-titles-instructions.md).

1. Įjunkite funkciją, kuri pateikta tokiu būdu:

    - **Modulis:** *Warehouse management*
    - **Priemonės pavadinimas:** *Warehouse management programosapylankos*

    Ši funkcija yra būtina sandėlio valdymo programos *duomenų užklausų srauto funkcijos* sąlyga. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ji įjungta pagal numatytąjį nustatymą. Daugiau informacijos apie funkciją Sandėlio *valdymo programa rasite* mobiliojo [įrenginio meniu elementų veiksmų konfigūravimas pagal veiksmus](warehouse-app-detours.md).

1. Jei sandėlio *valdymo programos funkcijų funkcija nebuvo įjungta,* **\>\>\>** **atnaujinkite laukų pavadinimus sandėlio valdymo mobiliųjų įrenginių programoje, nuėję į Sandėlio valdymo nustatymo mobiliojo įrenginio programos laukų pavadinimus** ir pasirinkdami Kurti numatytąjį nustatymą. Pakartokite šį veiksmą su kiekvienu juridiniu subjektu (įmone), kuriame naudojate sandėlio valdymo mobiliąją programą. Daugiau informacijos rasite [Sandėlio valdymo mobiliųjų įrenginių programėlės laukų konfigūravimas](configure-app-field-names-priorities-warehouse.md).
1. Įjunkite funkciją, kuri pateikta tokiu būdu:

    - **Modulis:** *Warehouse management*
    - **Funkcijos pavadinimas: sandėlio** *valdymo programos duomenų užklausų srautas*

    Ši funkcija yra tokia, kuri aprašyta šiame straipsnyje.

## <a name="example-scenarios"></a>Scenarijų pavyzdžiai

Šiame straipsnyje naudojami pavyzdiniai scenarijai, kad parodytų, kaip galite naudoti sandėlio *valdymo programos* duomenų užklausų srauto priemonę, kad pagerinti pirkimo gavimo srautą. Scenarijuose naudojami standartiniai pavyzdiniai duomenys, įskaitant srautą, pavadintą Pirkimo *gauti*. Šis srautas pradedamas paraginant darbuotojus identifikuoti pirkimo užsakymo numerį, pagal kurį jie gaus. Norėdami padėti darbuotojams lengviau identifikuoti pirkimo užsakymą, galite pagerinti pirmą srauto puslapį pridėdami šias naujas užklausos pasirinktis kaip [parinktis](warehouse-app-detours.md):

- **Ieškoti pu pagal tiekėją** – atidarykite puslapį, kuriame darbuotojai paraginamas įvesti tiekėjo vardą arba tiekėjo vardo dalį. Gali būti naudojami pakaitos simboliai. Pavyzdžiui, jei darbuotojas tikisi, kad gaunamas pristatymas iš tiekėjo, kurio vardas įtrauktas į įmonės pavadinimą, jis gali *įvestiVz*., **\*** peržiūrėti atvirų pirkimo užsakymų, kuriuose yra šis tekstas, kortelių rinkinį. Kiekvienoje kortelėje yra keletas laukų, kuriuose pateikiama informacija apie kiekvieną pirkimo užsakymą. Be tiekėjo vardo, korteles galite kurti taip, kad jose būtų rodomas tiekėjo sąskaitos numeris, pristatymo data ir dokumento būsena.
- **Peržvelgti** šiandienos PU – atidarykite puslapį, kuriame darbuotojai neįversti įvesti duomenų, bet vietoj to rodomi iš anksto sukonfigūruoti filtrai (pvz., šiandienos data). Tada puslapyje rodomas kortelių rinkinys, kuris atitinka filtrą. Darbuotojai dirba pasirinkdami pirkimo užsakymo kortelę, pagal kurią jie nori registruoti atsargų prekes.
- **Ieškoti PU pagal prekę** – atidarykite puslapį, kuriame darbuotojai paraginamas nuskaityti bet kurios į pristatytas atsargas prekės brūkšninius kodus. Tada sraute pateikiami visi atviri pirkimo užsakymai, kuriuose yra nuskaitytų prekių numerių eilutės. Jei norite padengti situacijas, kai brūkšninio kodo negalima perskaityti, šiame puslapyje galite įtraukti kitą informacijos peržvalgą, kuri leidžia darbuotojams ieškoti prekių numerių konkrečiame pirkimo užsakyme.

Kiekvienu atveju darbuotojas identifikuoja pirkimo užsakymą, pasirinkdamas kortelę, ir grąžinamas į pirmą puslapį, kuriame rodomas pasirinkto pirkimo užsakymo numeris. Tada darbuotojas gali tęsti gaunamų atsargų prekių registravimo eigą.

## <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Norėdami dirbti naudodami pavyzdinius scenarijus, aprašytus šiame straipsnyje, turite būti sistemoje, kurioje įdiegti standartiniai [demonstraciniai](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) duomenys. Be to, prieš pradėdami turite pasirinkti *USMF* juridinį subjektą (įmonę).

## <a name="configure-the-mobile-device-menu-items"></a>Konfigūruoti mobiliojo įrenginio meniu elementus

Norėdami sukurti kiekvieną iš naujų užklausos pasirinkčių, kurias turite įtraukti į pirmą srauto puslapį, turite nustatyti ją kaip mobiliojo įrenginio meniu elementą. Vėliau užklausos pasirinktys bus galimos pagal pirkimo gavimo *srautą*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Kurti meniu elementą Peržvalgų PU pagal tiekėją

Peržvalgų **pudį sukurkite pagal tiekėjo** meniu elementą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite Naujas, kad įtraukumėte **mobiliojo** įrenginio meniu elementą.
1. Nustatykite šias naujo meniu elemento vertes:

    - **Meniu elemento pavadinimas:** *ieškoti pu pagal tiekėją*
    - **Pavadinimas:** *peržvalga pagal tiekėjus*
    - **Režimas:** *Netiesioginis*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Veiklos kodas:** *duomenų užklausa*
    - **Naudokite proceso vadovą:** *Taip* (ši vertė pasirenkama automatiškai.)
    - **Lentelės pavadinimas:** *PurchTable* (šioje lentelėje norite peržiūrėti pirkimo užsakymų numerius.)

1. Veiksmų srityje pasirinkite redagavimo **užklausą**, kad apibrėžtumėte užklausą, pagrįstą pasirinkta bazine lentele (šiuo atveju pirkimo užsakymų lentelė).
1. Užklausos doroklyje skirtuke **Diapazonas** pridėkite šias eilutes prie tinklelio.

    | Lentelė | Išvestinė lentelė | Laukas | Kriterijai |
    |---|---|---|---|
    | Pirkimo užsakymai | Pirkimo užsakymai | Pirkimo užsakymo būsena | Atviras užsakymas |
    | Pirkimo užsakymai | Pirkimo užsakymai | Pristatymo data | (dayRange(-10,10)) |
    | Pirkimo užsakymai | Pirkimo užsakymai | Tiekėjo vardas | |

1. Pasirinkite **Gerai**.

    Šiame pavyzdyje naujas meniu elementas konfigūruojamas taip, kad rastų atvirus pirkimo užsakymus, kuriuos tikimasi gauti bet kuriuo metu nuo 10 dienų po praėjęs iki 10 dienų ateityje.

    Užklausoje tiekėjo pavadinimo **stulpelis** *Kriterijai* buvo paliktas tuščias. Todėl darbuotojai galės nurodyti šią vertę, naudodami sandėlio valdymo mobiliąją programą.

    Jei norite nurodyti, kaip sąrašas bus rūšiuojamas, rūšiavimą galite nustatyti skirtuke **Rūšiavimas**.

1. Be užklausos apibrėžimo, turite pasirinkti, kurie laukai bus rodomi kortelėse, užklausos sąrašo puslapyje. Todėl veiksmų srityje pasirinkite laukų **sąrašą**.
1. **Laukų sąrašo puslapyje** nustatykite šias vertes:

    - **1 rodomas laukas:** *PurchId* (šis laukas bus rodomas kaip kiekvienos kortelės antraštė.)
    - **2 rodomas laukas:** *PurchStatus*
    - **3 rodomas laukas:** *PurchName*
    - **Rodyti 4 lauką:** *OrderAccount*
    - **5 rodinio laukas:** *DeliveryDate*
    - **6 rodymo laukas:** *displayDocumentStatus()* (Ši reikšmė yra rodymo metodas, kaip "()" pabaigoje rodo.)

1. Veiksmų srityje pasirinkite **Įrašyti**. Tada uždarykite puslapį.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Kurti meniu elementą "Ieškoti šiandienos POS"

Sukurkite **šiandienos meniu elemento peržvalgą** pagal šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite Naujas, kad įtraukumėte **mobiliojo** įrenginio meniu elementą.
1. Nustatykite šias naujos prekės vertes:

    - **Meniu elemento pavadinimas:** *ieškoti šiandienos POS*
    - **Pavadinimas:** *ieškoti šiandienos POS*
    - **Režimas:** *Netiesioginis*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Veiklos kodas:** *duomenų užklausa*
    - **Naudokite proceso vadovą:** *Taip* (ši vertė pasirenkama automatiškai.)
    - **Lentelės pavadinimas:** *PurchTable* (šioje lentelėje norite peržiūrėti pirkimo užsakymų numerius.)

1. Veiksmų srityje pasirinkite redagavimo **užklausą**, kad apibrėžtumėte užklausą, pagrįstą pasirinkta bazine lentele (šiuo atveju pirkimo užsakymų lentelė).
1. Užklausos doroklyje skirtuke **Diapazonas** pridėkite šias eilutes prie tinklelio.

    | Lentelė | Išvestinė lentelė | Laukas | Kriterijai |
    |---|---|---|---|
    | Pirkimo užsakymas | Pirkimo užsakymas | Pirkimo užsakymo būsena | Atviras užsakymas |
    | Pirkimo užsakymas | Pirkimo užsakymas | Pristatymo data | (Diena (0)) |

1. Pasirinkite **Gerai**.

    Šiame pavyzdyje naujas meniu elementas konfigūruojamas rasti atvirus pirkimo užsakymus, kuriuos tikimasi gauti šiandien.

    Jei norite nurodyti, kaip sąrašas bus rūšiuojamas, rūšiavimą galite nustatyti skirtuke **Rūšiavimas**.

1. Be užklausos apibrėžimo, turite pasirinkti, kurie laukai bus rodomi kortelėse, užklausos sąrašo puslapyje. Todėl veiksmų srityje pasirinkite laukų **sąrašą**.
1. **Laukų sąrašo puslapyje** nustatykite šias vertes:

    - **1 rodomas laukas:** *PurchName* (šis laukas bus rodomas kaip kiekvienos kortelės antraštė.)
    - **2 rodomas laukas:** *PurchId*
    - **3 rodomas laukas:** *PurchStatus*
    - **Rodomas laukas 4:** *DlvMode*
    - **5 rodomas laukas:** *DlvTerm*
    - **Rodyti 6 lauką:** *OrderAccount*
    - **7 rodymo laukas:** *VendorName()* (ši vertė yra rodymo metodas, kaip "()" pabaigoje nurodoma.)

1. Veiksmų srityje pasirinkite **Įrašyti**. Tada uždarykite puslapį.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Kurti meniu elementą Peržvalgų PU pagal elementą

Peržvalgų **pudį sukurkite pagal prekių** meniu elementą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite Naujas, kad įtraukumėte **mobiliojo** įrenginio meniu elementą.
1. Nustatykite šias naujos prekės vertes:

    - **Meniu elemento pavadinimas:** *ieškoti PU pagal prekę*
    - **Pavadinimas:** *peržvalga po pu pagal prekę*
    - **Režimas:** *Netiesioginis*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Veiklos kodas:** *duomenų užklausa*
    - **Naudokite proceso vadovą:** *Taip* (ši vertė pasirenkama automatiškai.)
    - **Lentelės pavadinimas:** *PurchLine* (norite ieškoti pirkimo užsakymo numerių, pagrįstų prekės numeriu, per eilutės duomenis.)

1. Veiksmų srityje pasirinkite užklausą Redaguoti, **kad** apibrėžtumėte užklausą, pagrįstą pasirinkta bazine lentele (šiuo atveju pirkimo užsakymo eilučių lentelė, *tačiau prijungdami prie PurchTable* galite naudoti bet kurią su antrašte susijusią vertę).
1. Užklausos doroklyje skirtuke **Diapazonas** pridėkite šias eilutes prie tinklelio.

    | Lentelė | Išvestinė lentelė | Laukas | Kriterijai |
    |---|---|---|---|
    | Pirkimo užsakymo eilutės | Pirkimo užsakymo eilutės | Eilutės būsena | Atviras užsakymas |
    | Pirkimo užsakymo eilutės | Pirkimo užsakymo eilutės | Pristatymo data | (dayRange(-10,10)) |
    | Pirkimo užsakymo eilutės | Pirkimo užsakymo eilutės | Prekės numeris | |

1. Pasirinkite **Gerai**.

    Šiame pavyzdyje naujas meniu elementas konfigūruojamas taip, kad rastų atviras pirkimo užsakymo eilutes, kurias tikimasi gauti bet kuriuo metu nuo 10 dienų po praeito iki 10 dienų ateityje.

    Užklausoje prekės numerio **stulpelis** *Kriterijai* buvo paliktas tuščias. Todėl darbuotojai galės nurodyti šią vertę, naudodami sandėlio valdymo mobiliąją programą.

    Jei norite nurodyti, kaip sąrašas bus rūšiuojamas, rūšiavimą galite nustatyti skirtuke **Rūšiavimas**.

1. Be užklausos apibrėžimo, turite pasirinkti, kurie laukai bus rodomi kortelėse, užklausos sąrašo puslapyje. Todėl veiksmų srityje pasirinkite laukų **sąrašą**.
1. **Laukų sąrašo puslapyje** nustatykite šias vertes:

    - **1 rodomas laukas:** *PurchId* (šio lauko vertė bus naudojama kaip kiekvienos kortelės antraštė.)
    - **2 rodomas laukas:** *VendAccount*
    - **3 rodomas laukas:** *PurchQty*
    - **4 rodomas laukas:** *PurchUnit*
    - **5 rodomas laukas:** *PurchStatus*

1. Veiksmų srityje pasirinkite **Įrašyti**. Tada uždarykite puslapį.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Naujų mobiliojo įrenginio meniu elementų įtraukimas į meniu

Jūsų trys nauji mobiliojo įrenginio meniu elementai paruošti pridėti prie mobiliojo įrenginio meniu. Šią užduotį būtina atlikti prieš tai, kai meniu elementai gali būti naudojami kaip deimo proceso dalis. Šiame pavyzdyje jūs sukursite naują submeniu ir prie jo pridėsite naujus meniu elementus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujo įrašo antraštėje nustatykite šias vertes:

    - **Pavadinimas:** *užklausti*
    - **Aprašas:** *pateikti užklausą*

1. Sąraše Galimi **meniu ir meniu elementai pasirinkite** pirmą iš ką tik sukurtų mobiliojo įrenginio meniu elementų. Tada pasirinkite rodyklės dešinėn mygtuką, jei norite perkelti šį elementą į **meniu struktūros** sąrašą.
1. Pakartokite ankstesnį veiksmą su kitais dviem naujais meniu elementais.
1. Kairėje sąrašo srityje pasirinkite pagrindinį **meniu**.
1. Sąraše Galimi **meniu ir meniu elementai** slinkti žemyn iki **meniu** skyriaus ir pasirinkite naują **meniu Pateikti užklausą**. Tada pasirinkite rodyklės dešinėn mygtuką, jei norite perkelti šį elementą į **meniu struktūros** sąrašą.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Konfigūruoti savo mobiliojo įrenginio veiksmus

Norėdami užbaigti nustatymą, **·** *dabar turite naudoti atsieti konfigūraciją puslapyje Mobiliojo įrenginio veiksmai, kad į esamą pirkimo užsakymo identifikavimo veiksmą pirkimo gavimo sraute pridėtumėte tris naujus mobiliojo įrenginio meniu* elementus.

1. Pereikite prie sandėlio **valdymo nustatymo \> > mobiliojo įrenginio \> veiksmų**.
1. Filtro lauke **įveskite** *PU numerį*. Tada išplečiamajame *sąraše pasirinkite Veiksmo* ID: "PONum".
1. Kol tinklelyje pasirinktas rastas įrašas, veiksmų srityje **pasirinkite** Įtraukti veiksmo konfigūraciją. Kuris pasirodo išplečiamajame dialogo lange, nustatykite meniu **elemento lauką** Kaip Gauti *pirkimą*. Tada pasirinkite Gerai **,** kad uždarytumėte dialogo langą.
1. Naujos veiksmo konfigūracijos (**Pirkimo gimas: PONum**)**informacijos** puslapyje, esančiame "FastTab" Galimi nustatymai (meniu elementai), **įrankių** juostoje pasirinkite Įtraukti.
1. Dialogo lange **Pridėti de eską** raskite ir pasirinkite **peržvalgų POS pagal anksčiau** sukurtą tiekėjo meniu elementą.
1. Pasirinkite **Gerai**, norėdami uždaryti dialogo langą ir įtraukti pasirinktą meniu elementą į sąrašą nustatymai.
1. Pasirinkite naują skirtuką, o tada pasirinkite Pasirinkti laukus **, kurie bus siųsti į** įrankių juostą.
1. Dialogo **lange** **pasirinkti** laukus pridėkite prie skyriaus Siųsti iš pirkimo gavimo, nes nenorite perkelti jokių verčių į de ši meniu elementą. Tačiau dalyje Išvesti **atgal iš** pirkimo ir pirkimo peržvalgų pagal tiekėją nustatykite tokią jau pridėtos tuščios eilutės vertę:

    - **Kopijuoti iš pirkimo užsakymo peržvalgos pagal tiekėją:** *pirkimo užsakymas*
    - **Įklijuoti į pirkimo užsakymą: pirkimo** *užsakymas*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Kitų dviejų naujų meniu elementų 4–9 veiksmus pakartokite (**šiandien peržiūrėkite PU** **ir peržiūrėkite pu pagal prekę**). Dėl pirkimo **užsakymo peržvalgos** pagal tiekėjo meniu elementą nenorite siųsti jokių duomenų į šiuos mokėjimo užsakymus, tačiau norite grąžinti pirkimo užsakymo numerį.
1. Uždarykite puslapį.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Pamėginkite pirkimo gavimo srautą, kuris turi duomenų užklausą kaip de imo

Norėdami patikrinti savo naują mobiliosios programos sąranką, atlikite šiuos veiksmus.

1. Sukurkite kelis pirkimo užsakymus, kurių eilutės skirti sandėliui 51.
1. Mobiliajame įrenginyje arba emuliatoriuje, kuriame veikia sandėlio valdymo mobiliųjų įrenginių programėlę, prisijunkite prie 51 sandėlio įrašydami *„51”* kaip vartotojo ID, o *„1”* – kaip slaptažodį.
1. Mobiliojo įrenginio meniu pasirinkite Gaunamas **ir Tada –** Gauti **pirkimą**.

    Turėtumėte matyti toliau nurodytą puslapį, kuriame yra trys nauji meniu elementai.

    ![Pirkimo gavimas naudojant PU numerį.](media/wma-purchase-receive-po-num-with-detours.png "Pirkimo gavimas naudojant PU numerį")

1. Išbandykite skirtingas galimybes ir atkreipkite dėmesį, kad galite grąžinti pirkimo užsakymo numerį pasirinkdami vieną iš sąrašo kortelių.

    ![Pirkimo gavimas naudojant PU peržvalgą pagal tiekėją, 1 pavyzdys.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Pirkimo gavimas naudojant PU peržvalgą pagal tiekėją, 1 pavyzdys")

    ![Pirkimo gavimas naudojant PU peržvalgą pagal tiekėją, 2 pavyzdys.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Pirkimo gavimas naudojant PU peržvalgą pagal tiekėją, 2 pavyzdys")

> [!TIP]
> Užuot **paleidę** gavimo srautą, atlikdami peržvalgą iš pirkimo gavimo meniu elemento, galite pradėti nuo užklausų srauto (**\>\> pagrindinis užklausos peržvalgos POS** pagal tiekėją) ir iškviesti pasižiūrėti, kaip vykdyti norimą srautą, pasirinkdami vieną iš kortelių sąraše. Norėdami naudoti šį būdą, galite **nurodyti** **nuo puslapio Mobiliojo įrenginio veiksmai reikšmę, kurios veiksmo ID** *vertė yra GenericDataInquiryList.* Jei jūsų [*sistemai įjungta sandėlio*](warehouse-app-detours.md) valdymo mobiliosios programos funkcijos kelių lygių funkcija, galite įtraukti ir papildomą atsieimą, jei reikia (ši funkcija įtraukia dviejų lygių palaikymą ir gali būti pritaikyta, kad būtų palaikomi papildomi lygiai).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
