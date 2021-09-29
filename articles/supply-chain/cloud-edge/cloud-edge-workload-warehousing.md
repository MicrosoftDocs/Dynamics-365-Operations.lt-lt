---
title: Sandėlio valdymo darbo krūvis debesiui ir krašto skalės vienetams
description: Šioje temoje pateikta informacija apie funkcijas, kurios įjungia skalės vienetus siekiant vykdyti pasirinktus procesus iš jūsų sandėlio valdymo darbo krūvio.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c3f703e39e5e9d475dcb4f96dfb400a961ae2dcf
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500432"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Sandėlio valdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne visos sandėlio valdymo verslo funkcijos yra visiškai palaikomos sandėliams, kurie vykdo darbo krūvį skalės vienete. Įsitikinkite, kad naudojate tik procesus, kuriuos atskirai aprašo šis skyrius, kaip palaikomus.

## <a name="warehouse-execution-on-scale-units"></a>Sandėlio vykdymas skalės vienetuose

„Warehouse management“ darbo krūviai įgalina debesies ir kraštų skalės vienetus, kad būtų paleisti pasirinkti procesai iš sandėlio valdymo galimybių.

## <a name="prerequisites"></a>Būtinieji komponentai

Privalote turėti „Dynamics 365 Supply Chain Management“ centrą ir skalės vienetą, kurie bus patalpinti sandėlio valdymo darbo krūvyje. Daugiau informacijos apie architektūrą ir diegimo procesą ieškokite [paskirstytos topologijos skalės vienetais](cloud-edge-landing-page.md).

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Kaip sandėlio vykdymo darbo krūviai veikia skalės vienetuose

Tam, kad procesai sandėlio valdymo darbo krūvyje veiktų, duomenys sinchronizuojami tarp centro ir skalės vienetų.

Skalės vienetas gali palaikyti tik turimus duomenis. Duomenų nuosavybės sąvoka skalės vienetams padeda apsisaugoti nuo kelių pagrindinių konfliktų. Dėl to, svarbu jums suprasti, kurie procesai turimi centro ir kurie turimi proceso duomenys vienetų.

Atsižvelgiant į verslo procesus, tas pats duomenų įrašas gali pakeisti nuosavybę tarp centro ir svarstyklių vienetų. Šio scenarijaus pavyzdys pateikiamas toliau pateiktame skyriuje.

> [!IMPORTANT]
> Kai kurie duomenys gali būti sukurti ir svarstyklių vienete, ir svarstyklių vienete. Pavyzdžiai gali **būti numerio** lentelės ir **paketų numeriai**. Jei scenarijus, kuriame tas pats unikalus įrašas sukuriamas ir centre, ir svarstyklių vienete tame pačiame sinchronizavimo cikle, pateikiamas paskirtų konfliktų tvarkymas. Kai taip nutinka, kito sinchronizavimo atlikti nepavyks, o jūs turite eiti į **sistemos administravimo > Užklausos > Darbo krūvio užklausos > Dubliuoti įrašus**, kur galima peržiūrėti ir sulieti duomenis.

## <a name="outbound-process-flow"></a>Siuntimo tvarkymo eiga

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
- **Perkėlimo išdavimas** – Paprastas paėmimas ir pakrovimas.
- **Papildymas** – Neįskaitant žaliavų gamybai.
- **Baigtos prekės nudėtos** – po pranešimo, kad baigta, gamybos proceso.
- **Sudėties ir sudėties produktas padetas** – po ataskaitos baigto gamybos proceso.

Jokie kiti šaltinių dokumento tvarkymo arba sandėlio darbo tipo šiuo metu nėra palaikomi skalės vienetuose. Pavyzdžiui, negalite sandėlio vykdymo darbo krūviui skalės vienete atlikti perkėlimo užsakymo gavimo proceso (perkėlimo gavimo); vietoje to, jis turi būti tvarkomas centro elemento.

> [!NOTE]
> Nepalaikomų funkcijų mobiliojo įrenginio meniu elementai ir mygtukai nėra rodomi _Sandėlio valdymo mobiliųjų įrenginių programėlėje_, kai ji yra susieta su skalės vieneto diegimu.
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
- Sandėlio darbo apdorojimas su siuntimo pastabomis.
- Sandėlio darbo apdorojimas su medžiagų tvarkymu/„warehouse automation”.
- Produkto bendrųjų duomenų vaizdo naudojimas (pavyzdžiui, „Warehouse Management“ mobiliųjų įrenginių programėlėje).

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
| Šaltinių dokumento tvarkymas                                   | Taip | nr. |
| Krovinio ir gabenimo valdymo tvarkymas                | Taip, bet tik krovinio planavimo procesai. Transportavimo valdymo apdorojimas nepalaikomas  | nr. |
| Iškrovimo išlaidos ir tranzito prekių gavimas                                         | Taip | nr. |
| Išleisti į sandėlį                                         | Taip | nr. |
| Suplanuotas prekių skirstymas                                        | nr.  | nr. |
| Siuntos konsolidacija                                       | Taip, naudojant krovinio planavimą | Taip |
| Siuntimo bangos tvarkymas                                     | nr.  |Taip, išskyrus **krovinio kūrimą ir rūšiavimą** |
| Bangos siuntų tvarkymas                                  | nr.  | Taip|
| Sandėlio darbo tvarkymas (įsk. licencijos plokštelės spausdinimą)        | nr.  | Taip, bet tik prieš tai paminėtoms palaikomoms galimybėms |
| Klasterio paėmimas                                              | nr.  | Taip|
| Rankinis pakavimo apdorojimas, įskaitant „Supakuoto konteinerio paėmimo” darbo apdorojimą | Ne <P>Kai kuriuos apdorojimus galima atlikti po pradinio išrinkimo proceso, apdorojamo skalės vieneto, tačiau tai nerekomenduojama dėl šių užblokuotų operacijų.</p>  | Ne |
| Konteinerio pašalinimas iš grupės                                  | Ne  | Ne |
| Siuntimo rūšiavimo tvarkymas                                  | nr.  | nr. |
| Su kroviniu susijusių dokumentų spausdinimas                           | Taip | Taip|
| ASN kūrimo važtaraštis                            | nr.  | Taip|
| Siuntos patvirtinimas                                             | nr.  | Taip|
| Siuntos patvirtinimas su „Patvirtinti ir perkelti”            | nr.  | nr. |
| Važtaraščio ir sąskaitos faktūros išrašymo apdorojimas                        | Taip | nr. |
| Trumpas paėmimas (pardavimo ir perkėlimo užsakymai)                    | nr.  | Taip, nepašalinus šaltinio dokumentų rezervavimų|
| Perviršinis paėmimas (pardavimo ir perkėlimo užsakymai)                     | nr.  | Taip|
| Darbo vietų pakeitimas (pardavimo ir perkėlimo užsakymai)         | nr.  | Taip|
| Darbo užbaigimas (pardavimo ir perkėlimo užsakymai)                    | nr.  | Taip|
| Darbo ataskaitos spausdinimas                                            | Taip | Taip|
| Bangos žymė                                                   | nr.  | Taip|
| Darbo skaidymas                                                   | nr.  | Taip|
| Darbo apdorojimas – valdomas „transportavimo pakrovimo”            | Ne  | Ne |
| Sumažinti paimtą kiekį                                       | nr.  | nr. |
| Atšaukti darbą                                                 | nr.  | nr. |
| Atšaukti siuntos patvirtinimą                                | nr.  | Taip|

### <a name="inbound"></a>Gaunama

Tolesnė lentelė rodo, kurios gavimo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Apdorojimas                                                          | Tranzito punktas | Sandėlio vykdymas darbo apkrovos skalės vienete<BR>*(Prekės, pažymėtos „Taip”, yra taikomos tik sandėlio užsakymams)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Šaltinių&nbsp;dokumento&nbsp;tvarkymas                             | Taip | Ne |
| Krovinio ir gabenimo valdymo tvarkymas                    | Taip | Ne |
| Gautos siuntos patvirtinimas                                    | Taip | Ne |
| Pirkimo užsakymo leidimas į sandėlį (sandėlio užsakymo tvarkymas) | Taip | Ne |
| Sandėlio užsakymo eilučių atšaukimas<p>Atminkite, kad tai palaikoma tik tada, kai eilutėje neįvyko jokia registracija</p> | Taip | Ne |
| Pirkimo užsakymo prekės gavimas ir atidėjimas                       | <p>Taip,&nbsp;kai&nbsp;nėra&nbsp;sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, kai pirkimo užsakymas nėra dalis <i>krovinio</i></p> |
| Pirkimo užsakymo eilutės gavimas ir atidėjimas                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, kai pirkimo užsakymas nėra dalis <i>krovinio</i></p></p> |
| Grąžinimo užsakymo gavimas ir atidėjimas                              | Taip | Ne |
| Skirtingų numerio lentelių gavimas ir atidėjimas                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip |
| Krovinio prekės gavimas                                              | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Numerio lentelės gavimas ir atidėjimas                             | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Perkėlimo užsakymo prekės gavimas ir atidėjimas                       | Taip | Ne |
| Pirkimo užsakymo eilutės perkėlimas ir atidėjimas                       | Taip | Ne |
| Darbo (siuntimo) atšaukimas                                            | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, bet tik tada, kai <b>Išregistruoti gavimą atšaukiant darbą</b> parinktis (esanti <b>Sandėlio valdymo parametrų</b> puslapyje) yra išvalyta</p> |
| Pirkimo užsakymo gamybos kvito tvarkymas                        | Taip | Ne |
| Pirkimo užsakymo gavimas su pristatymo trūkumu                      | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip, bet tik atšaukus užklausą iš šakotuvo |
| Pirkimo užsakymas su pristatymo pertekliumi                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Taip  |
| Gavimas su *Prekių skirstymo* darbo kūrimu                 | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su *Kokybės užsakymo* darbo kūrimu                  | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su *Kokybės prekės pavyzdžio* darbo kūrimu          | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su *Kokybės patikros* darbo kūrimu       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Gavimas su kokybės užsakymo kūrimu                            | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
| Darbo apdorojimas – valdoma *Grupės atidėjimo*                 | Taip | Ne |
| Darbo apdorojimas su *Trumpu paėmimu*                               | Taip | nr. |
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
| Perkėlimo užsakymo kūrimas iš sandėlio programos           | Taip | nr.                           |
| Keitimas (į/iš)                                | Taip | Taip, bet ne koregavimo scenarijui, kuriame atsargų rezervavimas turi būti pašalintas, naudojant atsargų koregavimo tipų parametrą **Pašalinti rezervavimus**</p>                           |
| Atsargų būsenos keitimas                            | Taip | nr.                           |
| Ciklo skaičiavimas ir Neatitikimų skaičiavimo tvarkymas | Taip | Taip                           |
| Spausdinti dar kartą žymę (numerio lentelės spausdinimas)             | Taip | Taip                          |
| Numerio lentelės versija                                | Taip | Ne                           |
| Numerio lentelių grupavimas                                | Taip | Ne                           |
| Pakavimas į įdėtąsias numerių lenteles                                | Taip | Ne                           |
| Vairuotojo įregistravimas                                    | Taip | Ne                           |
| Vairuotojo išregistravimas                                   | Taip | Ne                           |
| Siuntimo talpinimo kodo keitimas                      | Taip | Taip                          |
| Atidaryto užduočių sąrašo rodymas                             | Taip | Taip                          |
| Numerių lenteles konsolidavimas                         | Taip | Ne                           |
| Min/maks ir zonos ribinio papildymo apdorojimas| Taip <p>Rekomenduojama neįtraukti tų pačių vietas kaip užklausų dalies</p>| Taip                          |
| Vietos pildymo tvarkymas                  | Taip  | Taip<p>Atkreipkite dėmesį, kad nustatymą reikia atlikti skalės vienete</p>                           |
| Darbo blokavimas ir atblokavimas                             | Taip | Taip                          |
| Vartotojo keitimas                                        | Taip | Taip                          |
| Darbo telkinio keitimas                           | Taip | Taip                          |
| Atšaukti darbą                                        | Taip | Taip                          |

### <a name="production"></a>Gamyba

Tolesnė lentelė apibendrina, kurie „warehouse management“ gamybos scenarijai nėra (ir yra) palaikomi skalės vieneto darbo eigose, kaip rodoma tolesnėje lentelėje.

| Apdorojimas | Tranzito punktas | Sandėlio vykdymas darbo apkrovos skalės vienete |
|---------|-----|------------------------------|
| Ataskaita apie baigtas ir atidėtas prekes | Taip | Taip |
| Sudėtinis produktas ir šalutinis produktas atidėti | Taip | Taip |
| <p>Visi kiti sandėlio valdymo procesai susiję su gamyba, įskaitant:</p><li>Išleisti į sandėlį</li><li>Gamybos bangos tvarkymas</li><li>Žaliavų paėmimas</li><li>„Kanban“ atidėtas</li><li>„Kanban“ paėmimas</li><li>Pradėti gamybos užsakymą</li><li>Gamybos nurašymas</li><li>Paskutinis produkcijos padėklas</li><li>Registruoti medžiagų sunaudojimą</li><li>Tuščias „kanban“</li></ul> | Taip | nr. |
| Žaliavų papildymas | nr. | nr. |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Sandėlio užsakymai, skirti debesies ir briaunos skalės vienetams

Kelios paketinės užduotys vykdomos tiek centre, tiek skalės vienetuose.

Centro diegime galite rankiniu būdu palaikyti paketines užduotis. Galite valdyti tolesnes paketines užduotis **Sandėlio valdymas \> Periodinės užduotys \> Galinio ofiso darbo krovos valdymas**:

- Iš skalės vieneto į telkinį pranešimų procesorius
- Registruoti šaltinio užsakymo kvitus
- Užbaigti sandėlio užsakymus

Darbo krūvio skalės vienetuose, galite valdyti tolesnes paketines užduotis **Sandėlio valdymas \> Periodinės užduotys \> Darbo krūvio valdymas**:

- Tvarkyti bangos lentelės įrašus
- Iš sandėlio telkinio į skalės vienetą pranešimų procesorius
- Apdoroti sandėlio užsakymo eilučių kiekio atnaujinimo užklausas

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
