---
title: Sandėlio valdymo darbo krūvis debesiui ir krašto skalės vienetams
description: Šioje temoje pateikta informacija apie funkcijas, kurios įjungia skalės vienetus siekiant vykdyti pasirinktus procesus iš jūsų sandėlio valdymo darbo krūvio.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, InventTransferOrders, SalesTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d8b0f5a4878a924943f6f8876575d5247875811
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068114"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Sandėlio valdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne visos sandėlio valdymo verslo funkcijos yra visiškai palaikomos sandėliams, kurie vykdo darbo krūvį skalės vienete. Įsitikinkite, kad naudojate tik procesus, kuriuos atskirai aprašo šis skyrius, kaip palaikomus.

## <a name="warehouse-execution-on-scale-units"></a>Sandėlio vykdymas skalės vienetuose

„Warehouse management“ darbo krūviai įgalina debesies ir kraštų skalės vienetus, kad būtų paleisti pasirinkti procesai iš sandėlio valdymo galimybių.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradedant dirbti su sandėlio valdymo darbo krūviu, jūsų sistema turi būti paruošta taip, kaip aprašyta šiame skyriuje.

### <a name="deploy-a-scale-unit-with-the-warehouse-management-workload"></a>Įdiekite masto vienetą su sandėlio valdymo darbo krūviu

Privalote turėti „Dynamics 365 Supply Chain Management“ centrą ir skalės vienetą, kurie bus patalpinti sandėlio valdymo darbo krūvyje. Daugiau informacijos apie architektūrą ir diegimo procesą ieškokite [paskirstytos topologijos skalės vienetais](cloud-edge-landing-page.md).

### <a name="turn-on-required-features-in-feature-management"></a>Įjunkite reikiamas funkcijas funkcijų tvarkyme

Naudoti [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, kad įjungtumėte abi šias funkcijas. (Abi funkcijos yra išvardytos *Sandėlių valdymas* modulis.)

- Atskirti atidėjimo darbą nuo ASN
- (Peržiūros versija) Gaunamų ir išsiunčiamų sandėlio užsakymų svėrimo įrenginių palaikymas

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Kaip sandėlio vykdymo darbo krūviai veikia skalės vienetuose

Tam, kad procesai sandėlio valdymo darbo krūvyje veiktų, duomenys sinchronizuojami tarp centro ir skalės vienetų.

Skalės vienetas gali palaikyti tik turimus duomenis. Duomenų nuosavybės sąvoka skalės vienetams padeda apsisaugoti nuo kelių pagrindinių konfliktų. Dėl to, svarbu jums suprasti, kurie procesai turimi centro ir kurie turimi proceso duomenys vienetų.

Atsižvelgiant į verslo procesus, tas pats duomenų įrašas gali pakeisti nuosavybę tarp centro ir svarstyklių vienetų. Šio scenarijaus pavyzdys pateikiamas toliau pateiktame skyriuje.

> [!IMPORTANT]
> Kai kurie duomenys gali būti sukurti ir svarstyklių vienete, ir svarstyklių vienete. Pavyzdžiai gali **būti numerio** lentelės ir **paketų numeriai**. Jei scenarijus, kuriame tas pats unikalus įrašas sukuriamas ir centre, ir svarstyklių vienete tame pačiame sinchronizavimo cikle, pateikiamas paskirtų konfliktų tvarkymas. Kai taip nutinka, kito sinchronizavimo atlikti nepavyks, o jūs turite eiti į **sistemos administravimo > Užklausos > Darbo krūvio užklausos > Dubliuoti įrašus**, kur galima peržiūrėti ir sulieti duomenis.

## <a name="outbound-process-flow"></a>Siuntimo tvarkymo eiga

Prieš diegdami sandėlio valdymo darbo krūvį debesies arba krašto masto vienete, įsitikinkite, kad turite *Mastelio vienetų palaikymas siunčiamų užsakymų išleidimui į sandėlį* funkcija įjungta jūsų įmonės centre. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Warehouse management*
- **Funkcijos pavadinimas:** *Mastelio vienetų palaikymas siunčiamų užsakymų išleidimui į sandėlį*

Siunčiamų duomenų nuosavybės procesas priklauso nuo to, ar naudojate krovinio planavimo procesą. Visais atvejais centro valdo šaltinio dokumentus, pvz., pardavimo užsakymus ir perkėlimo užsakymus, užsakymų paskirstymo procesą ir *susijusių užsakymų* operacijų duomenis. Bet kai naudojate krovinio planavimo procesą, kroviniai bus sukurti ant centro ir todėl iš pradžių bus valdomi centro. Kaip *išleidimo į sandėlį* proceso dalis, krovinio duomenų nuosavybės teisės perkeliamos į paskirtą skalės vieneto diegimą, kuris taps vėlesnio siuntos bangos apdorojimo savininku *siuntimo bangos tvarkymo* (pvz., darbo paskirstymu, papildymo darbu ir poreikio darbo sukūrimu). Todėl sandėlio darbuotojai gali apdoroti siunčiamo pardavimo ir perkėlimo užsakymo darbą tik naudodami „Warehouse management“ „mobile app“, kuri prijungta prie diegimo ir paleisdami konkretaus skalės vieneto darbo krūvį.

Kai galutinio darbo proceso metu atsargos įrašomos į galutinę siuntimo vietą (Bajadoor), svarstyklių vienetas rodo, kad šaltinio dokumento atsargų operacijos atnaujinamos į *Paimta*. Kol šis procesas bus vykdomas ir bus sinchronizuojami atgal, atsargos, turimos skalės vieneto darbo krūvyje, bus faktiškai rezervuotos sandėlio lygiu, o jūs galėsite nedelsdami apdoroti siunčiamos siuntos patvirtinimą nelaukdami šio sinchronizavimo pabaigos. Tolesnis krovinio pardavimo važtaraštis ir SF išrašymas arba perkėlimo užsakymo siuntimas bus apdorojami centre.

Šioje diagramoje rodomas siuntimo srautas ir nurodoma, kur vyksta atskiri verslo procesai. (Pasirinkite diagramą, kad ją būtų galima padidinti.)

[![Siuntimo tvarkymo eiga.](media/wes_outbound_warehouse_processes-small.png "Siuntimo tvarkymo eiga")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Išeinančių tvarkymas su apkrovos planavimu

Naudojant krovinio planavimo procesą, kroviniai ir siuntos sukuriamos ant centro, o duomenų nuosavybės teisės perkeliamos į svarstyklių vienetus kaip išleidimo į sandėlį proceso dalis, kaip *pavaizduota šiame paveikslėlyje*.

![Išeinančių tvarkymas su apkrovos planavimu.](./media/wes_outbound_processing_with_load_planning.png "Išeinančių tvarkymas su apkrovos planavimu")

### <a name="outbound-processing-without-load-planning"></a>Išeinančių tvarkymas be apkrovos planavimo

Kai naudojate krovinio planavimo procesą, siuntos sukuriamos ant svarstyklių vienetų. Svarstyklių vienetais kroviniai sukuriami ir kaip bangavimo proceso dalis.

![Išeinančių tvarkymas be apkrovos planavimo.](./media/wes_outbound_processing_without_load_planning.png "Išeinančių tvarkymas be apkrovos planavimo")

## <a name="inbound-process-flow"></a>Gavimo proceso eiga

Centras turi tolesnius duomenis:

- Visi šaltinio dokumentai, tokie kaip pirkimo ir gamybos užsakymai
- Gavimo krovinio tvarkymas
- Visi išlaidų ir finansiniai naujinimai

> [!NOTE]
> Gaunamų ir siunčiamų pirkimo užsakymų srautai skiriasi savo konceptais. Galite dirbti su tuo pačiu sandėliu skalės vienetu arba centru, atsižvelgiant ar pirkimo užsakymas buvo išleistas į sandėlį. Užsakymą išleidę į sandėlį, su tuo užsakymu galite dirbti tik prisijungę į skalės vienetą.
>
> Jei naudojate procesą *Paleisti į sandėlį*, sukuriami [*sandėlio užsakymai*](cloud-edge-warehouse-order.md) ir susijusios gavimo eigos nuosavybė priskiriama skalės vienetui. Centras nebegalės registruoti gavimo.

Norėdami naudoti procesą *Išleisti į sandėlį* turite prisijungti prie šakotuvo. Norėdami sutvarkyti pirkimo užsakymą, eikite į vieną iš šių puslapių:

- **Įsigijimas ir šaltiniai > Pirkimo užsakymai > Visi pirkimo užsakymai > Sandėlis > Veiksmai > Išleisti į sandėlį**
- **Sandėlio valdymas > Išleisti į sandėlį > Automatinis pirkimo užsakymų išleidimas**

Naudodami funkciją **Automatinis pirkimo užsakymų išleidimas** galite pasirinkti konkrečias pirkimo užsakymo eilutes, grindžiamas užklausa. Įprastas scenarijus būtų nustatyti pasikartojančią paketinę užduotį, kuri išleidžia visas patvirtintas pirkimo užsakymo eilutes, kurias numatoma gauti kitą dieną.

Darbuotojas gali vykdyti gavimo procesą naudodamas sandėlio valdymo mobiliųjų įrenginių programėlę, susietą su skalės vienetu. Duomenys tuomet įrašomi pagal skalės vienetą ir pranešami pagal gavimo sandėlio užsakymą. Tolesnio atidėjimo tvarkymas ir kūrimas taip pat bus tvarkomas pagal skalės vienetą.

Jei nenaudojate *leidimo į sandėlį* procesą ir dėl to nenaudojate *sandėlio užsakymų*, centras gali sutvarkyti sandėlio gavimo ir darbo tvarkymą nepriklausomai nuo skalės vienetų.

![Gavimo tvarkymo eiga.](./media/wes-inbound-ga.png "Gavimo proceso eiga")

Kai darbuotojas gauna registraciją naudodamas „Warehouse Management“ mobiliosios programos gavimo procesą prieš skalės vienetą, kvitas įrašomas pagal susijusį sandėlio užsakymą, kuris saugomas svarstyklių vienetais. Skalės vieneto darbo krūvis duos signalą centrui, kad būtų atnaujinti susijusios pirkimo užsakymo eilutės operacijos į *Užregistruota*. Kai tik ji bus baigta, galėsite paleisti pirkimo užsakymo produkto gavimo kvitą centre.

Šioje diagramoje rodomas gavimo srautas ir nurodoma, kur vyksta atskiri verslo procesai. (Pasirinkite diagramą, kad ją būtų galima padidinti.)

[![Gavimo tvarkymo eiga](media/wes_inbound_warehouse_processes-small.png "Gavimo tvarkymo eiga")](media/wes_inbound_warehouse_processes.png)

## <a name="production-control"></a>Gamybos kontrolė

Sandėlio valdymo darbo krūvis palaiko šiuos tris gamybos srautus Sandėlio valdymo programoje:

- Ataskaita, kaip baigta ir atidėta
- Gamybos užsakymo pradžia
- Medžiagų sunaudojimo registravimas

### <a name="report-as-finished-and-put-away"></a>Ataskaita, kaip baigta ir atidėta

Darbuotojai gali naudotis **Praneškite apie baigtą ir atidėkite** srautą Sandėlio valdymo programoje, kad praneštumėte apie gamybos arba partijos užsakymą kaip baigtą. Jie taip pat gali pranešti apie užbaigtus partijos užsakymo papildomus produktus ir šalutinius produktus. Kai pranešama, kad užduotis yra baigta, sistema paprastai sugeneruoja sandėliavimo darbus masto vienete. Jei nereikalaujate atidėti darbo, galite nustatyti savo darbo politiką, kad jo praleistumėte.

### <a name="start-production-order"></a>Gamybos užsakymo pradžia

Darbuotojai gali naudotis **Pradėti gamybos užsakymą** srautą Sandėlio valdymo programėlėje, kad užregistruotumėte gamybos ar partijos užsakymo pradžią.

### <a name="register-material-consumption"></a>Medžiagų sunaudojimo registravimas

Darbuotojai gali naudotis **Registruoti medžiagų suvartojimą** srautą Sandėlio valdymo programoje, kad praneštumėte apie medžiagų suvartojimą gamybos arba partijos užsakymui. Tada sukuriamas atrinkimo sąrašo žurnalas, skirtas ataskaitinei medžiagai apie gamybos arba partijos užsakymą masto vienete. Žurnalo eilutėse atliekama fizinė sunaudotų atsargų rezervacija. Kai duomenys sinchronizuojami tarp mastelio įrenginio ir šakotuvo, sugeneruojamas atrinkimo sąrašo žurnalas ir paskelbiamas koncentratoriaus egzemplioriuje.

## <a name="supported-processes-and-roles"></a>Palaikomi procesai ir vaidmenys

Ne visi sandėlio valdymo procesai palaikomi sandėlio vykdymo darbo krūvyje skalės vienete. Dėl to, rekomenduojame jums priskirti vaidmenis, kurie atitinka funkcijas prieinamas kiekvienam vartotojui.

Norėdami palengvinti šį procesą, pavyzdžio vaidmuo pavadinimu *Sandėlio vadovas darbo krūvyje* yra įtrauktas į demonstracinius duomenis **Sistemos administravimas \> Sauga \> Saugos konfigūravimas**. Šio vaidmenis tikslas yra užtikrinti sandėlio vadovų prieiga prie sandėlio vykdymo darbo krūvio skalės vienete. Vaidmenys suteikia prieigą prie puslapių, kurie yra svarbūs darbo krūvio kontekste, patalpintame skalės vienete.

Vartotojo vaidmenys skalės vienete yra priskiriamos kaip pradinių duomenų sinchronizavimo dalis iš centro į skalės vienetą.

Norėdami keisti vaidmenis priskirtus vartotojui, eikite į **Sistemos administravimas \> Sauga \> Priskirti vartotojus vaidmenims**. Vartotojai besielgiantys kaip sandėlio vadovai tik skalės vienetuose turi būti priskiriami tik *Sandėlio vadovo darbo krūvio* vaidmenims. Toks požiūris užtikrins, kad tie vartotojai turės prieigą tik prie palaikomų funkcijų. Pašalinkite bet kuriuos vaidmenis, priskirtus tiems vartotojams.

Vartotojai besielgiantys kaip sandėlio tiek centre, tiek skalės vienetams, turi būti priskirti prie esančio *Sandėlio darbuotojo* vaidmenims. Atsiminkite, kad vaidmuo suteikia sandėlio darbuotojams prieigą prie funkcijos (tokią, kaip gaunamo perdavimo užsakymo tvarkymas), kuri pasirodo vartotojo sąsajoje (UI), tačiau šiuo metu nepalaikomos skalės vienetuose.

### <a name="supported-warehouse-execution-processes"></a>Palaikomi sandėlio vykdymo procesai

Tolesni sandėlio valdymo procesai gali būti įjungti sandėlio vykdymo darbo krūviui skalės vienete:

- Pasirinkti pardavimo ir perkėlimo užsakymų bangos metodai (tvirtinimas, apkrovos kūrimas, paskirstymas, poreikio papildymas, krovimas į konteinerius, darbo kūrimas ir bangos etikečių spausdinimas)

- Pardavimo ir perkėlimo užsakymų sandėlio darbo apdorojimas naudojant sandėlio programą (įskaitant papildymo darbą)
- Laukiantis turimas inventorius su sandėlio programa
- Inventoriiaus kūrimo ir vykdymo judėjimus su sandėlio programa
- Ciklų skaičiavimo darbo kūrimas ir apdorojimas naudojant sandėlio programą
- Atsargų koregavimo kūrimas naudojant sandėlio programą
- Pirkimo užsakymų ir atidėjimo darbo darymo registravimas su sandėlio programa

Šie darbų tipai gali būti sukurti skalės vienetui, todėl gali būti apdorojami kaip sandėlio valdymo darbo krūvio dalis:

- **Atsargų judėjimai** – Rankiniu būdu arba pagal šablono darbą vykstantys judėjimai.
- **Ciklų skaičiavimo** – Įtraukiant neatitikčių patvirtinimą ir atmetimo procesus kaip skaičiavimo operacijų dalis.
- **Pirkimo užsakymai** Atidėjimo darbas per sandėlio užsakymą, kai pirkimo užsakymai nėra susieti su kroviniais.
- **Prekybos užsakymai** – Pavyzdžio paėmimas ir pakrovimo darbas.
- **Pervedimo kvitas** – Per valstybinio numerio priėmimo apdorojimą.
- **Perkėlimo išdavimas** – Paprastas paėmimas ir pakrovimas.
- **Papildymas** – Neįskaitant žaliavų gamybai.
- **Baigtos prekės nudėtos** – po pranešimo, kad baigta, gamybos proceso.
- **Sudėties ir sudėties produktas padetas** – po ataskaitos baigto gamybos proceso.
<!-- - **Packed container picking** - After manual packing station processing. -->

Šiuo metu masto vienetuose nepalaikomi jokie kiti šaltinio dokumentų apdorojimo ar sandėlio darbų tipai. Pavyzdžiui, kai susiduriate su sandėlio vykdymo darbo krūviu masto vienete, negalite naudoti grąžinimo užsakymo gavimo proceso grąžinimo užsakymams apdoroti. Vietoj to, šį apdorojimą turi atlikti koncentratoriaus egzempliorius.

> [!NOTE]
> Nepalaikomų funkcijų mobiliojo įrenginio meniu elementai ir mygtukai nėra rodomi _Sandėlio valdymo mobiliųjų įrenginių programėlėje_, kai ji yra susieta su skalės vieneto diegimu.
>
> Norint nustatyti, kad Sandėlio valdymo programa mobiliesiems veiktų prieš debesies ar krašto mastelio įrenginį, reikia atlikti kelis papildomus veiksmus. Daugiau informacijos žr [Sukonfigūruokite saugyklos valdymo programą mobiliesiems debesies ir krašto mastelio vienetams](cloud-edge-workload-setup-warehouse-app.md).
>
> Kai vykdote darbo krūvį skalės vienete, negalite vykdyti nepalaikomų procesų konkretaus sandėlio centre. Toliau šioje temoje pateiktos lentelės dokumentuoja palaikomas galimybes.
>
> Pasirinktus sandėlio darbo tipus galima sukurti tiek centro, tiek skalės vienetuose, tačiau jie gali būti prižiūrimi tik juos sukūrusio centro arba skalės vieneto (diegimas, sukūręs duomenis).
>
> Net, kai konkretus procesas palaiko skalės vienetą, atkreipkite dėmesį, kad ne visi reikalingi duomenys gali būti sinchronizuoti iš centro į skalės vienetą arba iš skalės vienetą į centrą, dėl ko gali įvykti netikėtas sistemos apdorojimas. Šio scenarijaus pavyzdžiai:
>
> - Jei naudojate vietos nurodymo užklausą, kuri sujungia duomenų lentelės įrašą, egzistuojantį tik diegiant centrą.
> - Jei naudojate krovinio vietos būsenos ir (arba) vietos tūrio matavimo funkcijas. Šie duomenys nebus sinchronizuoti tarp diegimų, todėl jie veiks tik atnaujinant vieno iš diegimų turimų atsargų vietą.

Tolesnės sandėlio valdymo funkcijos šiuo metu nepalaikomos skalės vienetų darbo krūviams:

- Kroviniui priskirtų pirkimo užsakymo eilučių gavimo apdorojimas.
- Projekto pirkimo užsakymų gavimo apdorojimas.
- Savikainos valdymas, reisų naudojimas ir prekių sekimas tranzito metu.
- Įvesties ir išvesties apdorojimas prekėms, turinčioms aktyvias sekimo dimensijas **Savininkas** ir (arba) **Serijos numeris**.
- Atsargų, turinčių blokavimo būsenos vertę, apdorojimas.
- Atsargų būsenos keitimas bet kurio darbo perkėlimo proceso metu.
- Užsakymui įsipareigojusios, lanksčios, sandėlio lygio dimensijų rezervacijos.
- Funkcijos *Sandėlio vietos būsena* naudojimas (duomenys nėra sinchronizuojami tarp diegimų).
- Funkcijos *Vietos numerio lentelės padėtis* naudojimas.
- Funkcijų *Produktų filtrai* ir *Produktų filtrų grupės*, įskaitant **Dienų skaičius paketams sumaišyti** parametrą, naudojimas.
- Integravimas su kokybės valdymu.
- Apdorojimas su esamo svorio prekėmis.
- Apdorojimas su prekėmis, kurias galima naudoti transportavimo valdymui (TMS).
- Apdorojimas su neigiamomis turimomis atsargomis.
- Produktų duomenų bendrinimas tarp įmonių. <!-- Planned -->
- Sandėlio darbo apdorojimas su siuntimo pastabomis.
- Sandėlio darbo apdorojimas su medžiagų tvarkymu/„warehouse automation”.
- Produkto bendrųjų duomenų vaizdai (pavyzdžiui, Warehouse Management mobiliųjų įrenginių programėlėje).

> [!WARNING]
> Kai kurios sandėlio funkcijos nebus galimos sandėliams, kuriuose vykdomi sandėlio valdymo darbo krūviai skalės vienete, ir taip pat nepalaikoma centro arba skalės vieneto darbo krūvyje.
>
> Kitos galimybės gali būti apdorojamos abiejuose, tačiau kai kuriuose scenarijuose jas reikės naudoti kruopščiai, pavyzdžiui, kai bus atnaujintos to paties sandėlio tiek centro, tiek skalės vieneto atsargos dėl asinchroninio duomenų atnaujinimo proceso.
>
> Konkrečios funkcijos (pavyzdžiui, *blokavimo darbas*), kurias palaiko tiek centro, tiek skalės vienetai, bus palaikomas tik duomenų savininkui.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Siuntimas (palaikomas tik pirkimo ir perkėlimo užsakymams)

Tolesnė lentelė rodo, kurios siuntimo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Apdorojimas                                                      | Tranzito punktas | Sandėlio vykdymas darbo apkrovos skalės vienete |
|--------------------------------------------------------------|-----|------------------------------|
| Šaltinių dokumento tvarkymas                                   | Taip | Ne |
| Krovinio ir gabenimo valdymo tvarkymas                | Taip, bet tik krovinio planavimo procesai. Transportavimo valdymo apdorojimas nepalaikomas  | Ne |
| Išleisti į sandėlį                                         | Taip | Ne |
| Suplanuotas prekių skirstymas                                        | Ne  | Ne |
| Siuntos konsolidacija                                       | Taip, naudojant krovinio planavimą | Taip |
| Siuntimo bangos tvarkymas                                     | Ne  |Taip, išskyrus **krovinio kūrimą ir rūšiavimą** |
| Bangos siuntų tvarkymas                                  | Ne  | Taip|
| Sandėlio darbo tvarkymas (įsk. licencijos plokštelės spausdinimą)        | Ne  | Taip, bet tik prieš tai paminėtoms palaikomoms galimybėms |
| Klasterio paėmimas                                              | Ne  | Taip|
| Rankinis pakavimo apdorojimas, įskaitant „Supakuoto konteinerio paėmimo” darbo apdorojimą | Ne <P>Dalį apdorojimo galima atlikti po pradinio rinkimo proceso, kurį atlieka svarstyklių įrenginys, bet nerekomenduojama, nes sekančios užblokuotos operacijos.</p>  | Ne |
| Konteinerio pašalinimas iš grupės                                  | Ne  | Ne |
| Siuntimo rūšiavimo tvarkymas                                  | Ne  | Ne |
| Su kroviniu susijusių dokumentų spausdinimas                           | Taip | Taip|
| ASN kūrimo važtaraštis                            | Ne  | Taip|
| Siuntos patvirtinimas                                             | Ne  | Taip|
| Siuntos patvirtinimas su „Patvirtinti ir perkelti”            | Ne  | Taip|
| Važtaraščio ir sąskaitos faktūros išrašymo apdorojimas                        | Taip | Ne |
| Trumpas paėmimas (pardavimo ir perkėlimo užsakymai)                    | Ne  | Taip, nepašalinus šaltinio dokumentų rezervavimų|
| Perviršinis paėmimas (pardavimo ir perkėlimo užsakymai)                     | Ne  | Taip|
| Numerių lenteles konsolidavimas                                   | Ne  | Taip|
| Darbo vietų pakeitimas (pardavimo ir perkėlimo užsakymai)         | Ne  | Taip|
| Darbo užbaigimas (pardavimo ir perkėlimo užsakymai)                    | Ne  | Taip|
| Darbo ataskaitos spausdinimas                                            | Taip | Taip|
| Bangos žymė                                                   | Ne  | Taip|
| Darbo skaidymas                                                   | Ne  | Taip|
| Darbo apdorojimas – valdomas „transportavimo pakrovimo”            | Ne  | Ne |
| Sumažinti paimtą kiekį                                       | Ne  | Taip|
| Darbo atšaukimas                                                 | Ne  | Taip|
| Atšaukti siuntos patvirtinimą                                | Ne  | Taip|
| Prašymas atšaukti sandėlio užsakymo eilutes                      | Taip | Ne, bet prašymas bus patvirtintas arba atmestas |
| <p>Paleisti perkėlimo užsakymus, skirtus gauti</p><p>Šis procesas vyks automatiškai kaip perdavimo užsakymo siuntimo proceso dalis. Tačiau jį galima naudoti rankiniu būdu, kad būtų galima įgalinti valstybinio numerio ženklų priėmimą masto vienete, jei įeinančios sandėlio užsakymo eilutės buvo atšauktos arba kaip naujo darbo krūvio diegimo proceso dalis.</p> | Taip | Ne|

### <a name="inbound"></a>Gaunama

Tolesnė lentelė rodo, kurios gavimo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Apdorojimas                                                          | Tranzito punktas | Sandėlio vykdymas darbo apkrovos skalės vienete<BR>*(Prekės, pažymėtos „Taip”, yra taikomos tik sandėlio užsakymams)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Šaltinių&nbsp;dokumento&nbsp;tvarkymas                             | Taip | Ne |
| Krovinio ir gabenimo valdymo tvarkymas                    | Taip | Ne |
| Iškrovimo išlaidos ir tranzito prekių gavimas                       | Taip | Ne |
| Gautos siuntos patvirtinimas                                    | Taip | Ne |
| Pirkimo užsakymo leidimas į sandėlį (sandėlio užsakymo tvarkymas) | Taip | Ne |
| Prašymas atšaukti sandėlio užsakymo eilutes                            | Taip | Ne, bet prašymas bus patvirtintas arba atmestas |
| Pirkimo užsakymo pirminio dokumento produkto gavimo apdorojimas                        | Taip | Ne |
| Pirkimo užsakymo prekės gavimas ir atidėjimas                       | <p>Taip,&nbsp;kai&nbsp;nėra&nbsp;sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, kai pirkimo užsakymas nėra dalis <i>krovinio</i></p> |
| Pirkimo užsakymo eilutės gavimas ir atidėjimas                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, kai pirkimo užsakymas nėra dalis <i>krovinio</i></p></p> |
| Grąžinimo užsakymo gavimas ir atidėjimas                              | Taip | Ne |
| Skirtingų numerio lentelių gavimas ir atidėjimas                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip |
| Krovinio prekės gavimas                                              | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Pirkimo užsakymas Valstybinio numerio priėmimas ir padėjimas              | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Perdavimo užsakymas Valstybinio numerio priėmimas ir padėti             | Ne | Taip |
| Perkėlimo užsakymo prekės gavimas ir atidėjimas                       | Taip | Ne |
| Pirkimo užsakymo eilutės perkėlimas ir atidėjimas                       | Taip | Ne |
| Pirkimo užsakymo gavimas su pristatymo trūkumu                      | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip, bet tik atšaukus užklausą iš šakotuvo |
| Pirkimo užsakymas su pristatymo pertekliumi                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip  |
| Gavimas su *Prekių skirstymo* darbo kūrimu                 | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su *Kokybės užsakymo* darbo kūrimu                  | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su *Kokybės prekės pavyzdžio* darbo kūrimu          | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su *Kokybės patikros* darbo kūrimu       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su kokybės užsakymo kūrimu                            | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Darbo apdorojimas – valdoma *Grupės atidėjimo*                 | Taip | Ne |
| Darbo apdorojimas su *Trumpu paėmimu*                               | Taip | Ne |
| Darbo (siuntimo) atšaukimas                                            | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, bet tik tada, kai<b>Atšaukdami darbą, išregistruokite kvitą</b> parinktis ant<b>Sandėlio valdymo parametrai</b> puslapis išvalytas</p> |
| Numerio lentelės įkėlimas                                           | Taip | Taip |

### <a name="warehouse-operations-and-exception-handing"></a>Sandėlio operacijos ir išimčių tvarkymas

Tolesnė lentelė rodo, kurios sandėlio operacijos ir išimčių tvarkymo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Apdorojimas                                            | Tranzito punktas | Sandėlio vykdymas darbo apkrovos skalės vienete |
|----------------------------------------------------|-----|------------------------------|
| Licencijos lentelės užklausa                              | Taip | Taip                          |
| Prekės užklausa                                       | Taip | Taip                          |
| Vietos užklausa                                   | Taip | Taip                          |
| Sandėlio keitimas                                   | Taip | Taip                          |
| Judėjimas                                           | Taip | Taip                          |
| Judėjimas pagal šabloną                               | Taip | Taip                          |
| Sandėlio perkėlimas                                 | Taip | Ne                           |
| Perkėlimo užsakymo kūrimas iš sandėlio programos           | Taip | Ne                           |
| Keitimas (į/iš)                                | Taip | Taip, bet ne koregavimo scenarijui, kuriame atsargų rezervavimas turi būti pašalintas, naudojant atsargų koregavimo tipų parametrą **Pašalinti rezervavimus**</p>                           |
| Atsargų būsenos keitimas                            | Taip | Ne                           |
| Ciklo skaičiavimas ir Neatitikimų skaičiavimo tvarkymas | Taip | Taip                           |
| Spausdinti dar kartą žymę (numerio lentelės spausdinimas)             | Taip | Taip                          |
| Numerio lentelės versija                                | Taip | Ne                           |
| Numerio lentelių grupavimas                                | Taip | Ne                           |
| Pakavimas į įdėtąsias numerių lenteles                      | Taip | Ne                           |
| Vairuotojo įregistravimas                                    | Taip | Ne                           |
| Vairuotojo išregistravimas                                   | Taip | Ne                           |
| Siuntimo talpinimo kodo keitimas                      | Taip | Taip                          |
| Atidaryto užduočių sąrašo rodymas                             | Taip | Taip                          |
| Min/maks ir zonos ribinio papildymo apdorojimas| Taip <p>Rekomenduojama neįtraukti tų pačių vietas kaip užklausų dalies</p>| Taip                          |
| Vietos pildymo tvarkymas                  | Taip  | Taip<p>Atkreipkite dėmesį, kad nustatymą reikia atlikti skalės vienete</p>                           |
| Darbo blokavimas ir atblokavimas                             | Taip | Taip                          |
| Vartotojo keitimas                                        | Taip | Taip                          |
| Darbo telkinio keitimas                           | Taip | Taip                          |
| Atšaukti darbą                                        | Taip | Taip                          |

### <a name="production"></a>Gamyba

Tolesnė lentelė apibendrina, kurie „warehouse management“ gamybos scenarijai nėra (ir yra) palaikomi skalės vieneto darbo eigose, kaip rodoma tolesnėje lentelėje.

| Apdorojimas | Centras | Sandėlio vykdymas darbo apkrovos skalės vienete |
|---------|-----|----------------------------------------------|
| Gamybos užsakymo pirminio dokumento tvarkymas    | Taip | Ne |
| Išleisti į sandėlį                           | Taip | Ne |
| Gamybos užsakymo pradžia                         | Taip | Taip|
| Kurti sandėlio užsakymus                        | Taip | Ne |
| Prašymas atšaukti sandėlio užsakymo eilutes        | Taip | Ne, bet prašymas bus patvirtintas arba atmestas |
| Ataskaita apie baigtas ir atidėtas prekes | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip|
| Sudėtinio ir šalutinio produktų atidėjimas             | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip|
| Medžiagų sunaudojimo registravimas                  | Taip | Taip|
| Gamybos bangos tvarkymas                     | Taip | Ne |
| Žaliavų paėmimas                           | Taip | Ne |
| „Kanban“ atidėjimas                                | Taip | Ne |
| „Kanban“ paėmimas                                 | Taip | Ne |
| Tuščias „kanban“                                   | Taip | Ne |
| Gamybos nurašymas                               | Taip | Ne |
| Paskutinis produkcijos padėklas                         | Taip | Ne |
| Žaliavų papildymas                     | Ne  | Ne |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Sandėlio užsakymai, skirti debesies ir briaunos skalės vienetams

Kelios paketinės užduotys vykdomos tiek centre, tiek skalės vienetuose.

Naudodami šakotuvo diegimą galite rankiniu būdu prižiūrėti šias paketines užduotis:

- Tvarkykite šias paketines užduotis adresu **Sandėlių valdymas \> Periodinės užduotys \> Back-office darbo krūvio valdymas**:

    - Iš skalės vieneto į telkinį pranešimų procesorius
    - Registruoti šaltinio užsakymo kvitus
    - Užbaigti sandėlio užsakymus

- Tvarkykite šias paketines užduotis adresu **Sandėlių valdymas \> Periodinės užduotys \> Darbo krūvio valdymas**:

    - Iš sandėlio telkinio į skalės vienetą pranešimų procesorius
    - Apdoroti sandėlio užsakymo eilutės kvitus sandėlio kvito registravimui

Diegdami masto vienetus galite valdyti toliau nurodytas paketines užduotis **Sandėlių valdymas \> Periodinės užduotys \> Darbo krūvio valdymas**:

- Apdoroti bangos lentelės įrašus
- Iš sandėlio telkinio į skalės vienetą pranešimų procesorius
- Apdoroti sandėlio užsakymo eilutės kvitus sandėlio kvito registravimui

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
