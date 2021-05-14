---
title: Sandėlio valdymo darbo krūvis debesiui ir krašto skalės vienetams
description: Šioje temoje pateikta informacija apie funkcijas, kurios įjungia skalės vienetus siekiant vykdyti pasirinktus procesus iš jūsų sandėlio valdymo darbo krūvio.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9bdb9529c8b630182a2036e9d116909f9e92bb83
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944418"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Sandėlio valdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne visos sandėlio valdymo verslo funkcijos yra visiškai palaikomos sandėliams, kurie vykdo darbo krūvį skalės vienete. Įsitikinkite, kad naudojate tik procesus, kuriuos atskirai aprašo šis skyrius, kaip palaikomus.

## <a name="warehouse-execution-on-scale-units"></a>Sandėlio vykdymas skalės vienetuose

Šioje temoje pateikta informacija apie funkcijas, kurios įjungia sandėlio valdymo pajėgumus.

Šioje temoje sandėlio valdymo vykdymai sandėlyje, kuris nustatytas skalės vienete yra žinomi kaip *Sandėlio vykdymo sistema* (*WES*).

## <a name="prerequisites"></a>Būtinieji komponentai

Privalote turėti „Dynamics 365 Supply Chain Management“ centrą ir skalės vienetą, kurie bus patalpinti sandėlio valdymo darbo krūvyje. Daugiau informacijos apie diegimo procesą ir architektūrą rasite [Naudokite skalės vienetus padidinti atsparumą „Supply Chain Management” darbo krūviams](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Kaip WES darbo krūviai veikia skalės vienetuose

Tam, kad procesai sandėlio valdymo darbo krūvyje veiktų, duomenys sinchronizuojami tarp centro ir skalės vienetų.

Skalės vienetas gali palaikyti tik turimus duomenis. Duomenų nuosavybės sąvoka skalės vienetams padeda apsisaugoti nuo kelių pagrindinių konfliktų. Dėl to, svarbu jums suprasti, kurie procesai turimi centro ir kurie turimi skalės vienetų.

Skalės vienetai turi tolesnius duomenis:

- **Siuntimo bangos tvarkymo duomenys** – Pasirinkti bangos tvarkymo metodai yra tvarkomi kaip skalės vieneto bangos tvarkymo dalis.
- **Darbo apdorojimo** duomenys – sandėlio darbas, sukurtas svarstyklių vienetais, priklauso šiam konkrečiam skalės vienetui. Palaikomi šie darbo užsakymų apdorojimo tipai:

  - **Atsargų judėjimai** (rankiniu būdu arba pagal šablono darbą vykstantys judėjimai)
  - **Ciklų** skaičiavimo ir patvirtinimo / atmetimo procesas kaip skaičiavimo operacijų dalis
  - **Pirkimo užsakymai** (atidėjimo darbas per sandėlio užsakymą, kai pirkimo užsakymai nėra susieti su kroviniais)
  - **Prekybos užsakymai** (pavyzdžio paėmimas ir pakrovimo darbas)
  - **Perkėlimo užsakymai** (tik siunčiami su pavyzdžio paėmimo ir pakrovimo darbu)

- **Sandėlio darbo gavimo duomenys** – Šie duomenys naudojami tik pirkimo užsakymams, kurie buvo rankiniu būdu paleisti į sandėlį.
- **Licencijos lentelės duomenys** – Licencijos lentelės gali būti sukurtos centre ir skalės vienete. Paskirtas konflikto valdymas buvo patvirtintas. Atminkite, kad šie duomenys nėra būdingi sandėliui.

## <a name="outbound-process-flow"></a>Siuntimo tvarkymo eiga

Centras turi tolesnius duomenis:

- Visi šaltinio dokumentai, tokie kaip pardavimo užsakymas ir perdavimo užsakymai
- Užsakymo paskyrimas ir siuntimo krūvio tvarkymas
- Paleidimo į sandėlį, siuntimo kūrimo, bangos kūrimo ir bangos užbaigimo procesai

Skalės vienetai turi realų bangos tvarkymą (tokį kaip darbo skyrimą, pildymo darbą ir paklausos darbo kūrimą) po bangos paleidimo. Todėl sandėlio darbuotojai gali apdoroti siuntimo darbą naudodami sandėlio valdymo mobiliųjų įrenginių programėlę, susietą su skalės vienetu.

![Bangos tvarkymo eiga](./media/wes-wave-processing-ga.png "Bangos tvarkymo eiga")

### <a name="process-work-and-ship"></a>Apdoroti darbą ir siuntą

Kai galutinio darbo proceso metu atsargos įrašomos į galutinę siuntimo vietą (Bajadoor), svarstyklių vienetas rodo, kad šaltinio dokumento atsargų operacijos atnaujinamos į *Paimta*. Kol šis procesas bus vykdomas ir bus sinchronizuojamas atgal, atsargos, turimos skalės vieneto darbo krūvyje, bus faktiškai rezervuotos sandėlio lygiu.

Kai tik centro centras atnaujins operacijas į *Paimta*, jis gali apdoroti siunčiamos siuntos patvirtinimą ir susijusį krovinio pardavimo važtaraštį arba perkėlimo užsakymo siuntą.

![Siuntimo tvarkymo eiga](./media/WES-outbound-processing-19.png "Siuntimo tvarkymo eiga")

## <a name="inbound-process-flow"></a>Gavimo proceso eiga

Centras turi tolesnius duomenis:

- Visi šaltinio dokumentai, tokie kaip pirkimo užsakymas ir pardavimo grąžinimo užsakymai
- Gavimo krovinio tvarkymas
- Visi išlaidų ir finansiniai naujinimai

> [!NOTE]
> Gaunamų ir siunčiamų pirkimo užsakymų srautai skiriasi savo konceptais. Galite dirbti su tuo pačiu sandėliu skalės vienetu arba centru, atsižvelgiant ar pirkimo užsakymas buvo išleistas į sandėlį. Užsakymą išleidę į sandėlį, su tuo užsakymu galite dirbti tik prisijungę į skalės vienetą.
>
> Jei naudojate procesą *Paleisti į sandėlį*, sukuriami [*sandėlio užsakymai*](cloud-edge-warehouse-order.md) ir susijusios gavimo eigos nuosavybė priskiriama skalės vienetui. Centras nebegalės registruoti gavimo.

Norėdami naudoti procesą *Išleisti į sandėlį* turite prisijungti prie šakotuvo. Norėdami jį paleisti arba suplanuoti, eikite į vieną iš šių puslapių:

- **Įsigijimas ir šaltiniai > Pirkimo užsakymai > Visi pirkimo užsakymai > Sandėlis > Veiksmai > Išleisti į sandėlį**
- **Sandėlio valdymas > Išleisti į sandėlį > Automatinis pirkimo užsakymų išleidimas**

Naudodami funkciją **Automatinis pirkimo užsakymų išleidimas** galite pasirinkti konkrečias pirkimo užsakymo eilutes, grindžiamas užklausa. Įprastas scenarijus būtų nustatyti pasikartojančią paketinę užduotį, kuri išleidžia visas patvirtintas pirkimo užsakymo eilutes, kurias numatoma gauti kitą dieną.

Darbuotojas gali vykdyti gavimo procesą naudodamas sandėlio valdymo mobiliųjų įrenginių programėlę, susietą su skalės vienetu. Duomenys tuomet įrašomi pagal skalės vienetą ir pranešami pagal gavimo sandėlio užsakymą. Tolesnio atidėjimo tvarkymas ir kūrimas taip pat bus tvarkomas pagal skalės vienetą.

Jei nenaudojate *leidimo į sandėlį* procesą ir dėl to nenaudojate *sandėlio užsakymų*, centras gali sutvarkyti sandėlio gavimo ir darbo tvarkymą nepriklausomai nuo skalės vienetų.

![Gavimo tvarkymo eiga](./media/wes-inbound-ga.png "Gavimo proceso eiga")

Atliekant gavimo registraciją sandėlio programos gavimo procesu pagal skalės vieneto sandėlio užsakymą, skalės vieneto darbo krūvis duos signalą centrui, kad susijusių pirkimo užsakymo eilučių operacijos būtų atnaujintos į *Užregistruotas*. Kai tik ji bus baigta, galėsite paleisti pirkimo užsakymo produkto gavimo kvitą centre.

![Gavimo tvarkymo eiga](./media/WES-inbound-processing-19.png "Gavimo tvarkymo eiga")

## <a name="supported-processes-and-roles"></a>Palaikomi procesai ir vaidmenys

Ne visi sandėlio valdymo procesai palaikomi WES darbo krūvyje skalės vienete. Dėl to, rekomenduojame jums priskirti vaidmenis, kurie atitinka funkcijas prieinamas kiekvienam vartotojui.

Norėdami palengvinti šį procesą, pavyzdžio vaidmuo pavadinimu *Sandėlio vadovas darbo krūvyje* yra įtrauktas į demonstracinius duomenis **Sistemos administravimas \> Sauga \> Saugos konfigūravimas**. Šio vaidmenis tikslas yra užtikrinti sandėlio vadovų prieiga prie WES skalės vienete. Vaidmenys suteikia prieigą prie puslapių, kurie yra svarbūs darbo krūvio kontekste, patalpintame skalės vienete.

Vartotojo vaidmenys skalės vienete yra priskiriamos kaip pradinių duomenų sinchronizavimo dalis iš centro į skalės vienetą.

Norėdami keisti vaidmenis priskirtus vartotojui, eikite į **Sistemos administravimas \> Sauga \> Priskirti vartotojus vaidmenims**. Vartotojai besielgiantys kaip sandėlio vadovai tik skalės vienetuose turi būti priskiriami tik *Sandėlio vadovo darbo krūvio* vaidmenims. Toks požiūris užtikrins, kad tie vartotojai turės prieigą tik prie palaikomų funkcijų. Pašalinkite bet kuriuos vaidmenis, priskirtus tiems vartotojams.

Vartotojai besielgiantys kaip sandėlio tiek centre, tiek skalės vienetams, turi būti priskirti prie esančio *Sandėlio darbuotojo* vaidmenims. Atsiminkite, kad vaidmuo suteikia sandėlio darbuotojams prieigą prie funkcijos (tokią, kaip gaunamo perdavimo užsakymo tvarkymas), kuri pasirodo vartotojo sąsajoje (UI), tačiau šiuo metu nepalaikomos skalės vienetuose.

## <a name="supported-wes-processes"></a>Palaikomi WES procesai

Tolesni sandėlio valdymo procesai gali būti įjungti WES darbo krūviui skalės vienete:

- Pasirinkti pardavimo ir perkėlimo užsakymų bangos metodai (paskirstymas, poreikio papildymas, krovimas į konteinerius, darbo kūrimas ir bangos etikečių spausdinimas)

- Pardavimo ir perkėlimo užsakymų sandėlio darbo apdorojimas naudojant sandėlio programą (įskaitant papildymo darbą)
- Laukiantis turimas inventorius su sandėlio programa
- Inventoriiaus kūrimo ir vykdymo judėjimus su sandėlio programa
- Ciklų skaičiavimo darbo kūrimas ir apdorojimas naudojant sandėlio programą
- Atsargų koregavimo kūrimas naudojant sandėlio programą
- Pirkimo užsakymų ir atidėjimo darbo darymo registravimas su sandėlio programa

Tolesni darbo užsakymo tipai šiuo metu palaikomi WES darbo krūviuose skalės vieneto talpinimuose:

- Pardavimo užsakymai
- Perkėlimo išdavimas
- Papildymas
- Atsargų perkėlimas
- Ciklo skaičiavimas
- Pirkimo užsakymai (susieti su sandėlio užsakymais)

Jokie kiti šaltinių dokumento tvarkymo arba sandėlio darbo tipo šiuo metu nėra palaikomi skalės vienetuose. Pavyzdžiui, negalite WES darbo krūviui skalės vienete atlikti perkėlimo užsakymo gavimo proceso (perkėlimo gavimo); vietoje to, jis turi būti tvarkomas centro elemento.

> [!NOTE]
> Nepalaikomų funkcijų mobiliojo įrenginio meniu elementai ir mygtukai nėra rodomi _Sandėlio valdymo mobiliųjų įrenginių programėlėje_, kai ji yra susieta su skalės vieneto diegimu.

> [!WARNING]
> Kai vykdote darbo krūvį skalės vienete, negalite vykdyti nepalaikomų procesų konkretaus sandėlio centre. Toliau šioje temoje pateiktos lentelės dokumentuoja palaikomas galimybes.
>
> Pasirinktus sandėlio darbo tipus galima sukurti tiek centro, tiek skalės vienetuose, tačiau jie gali būti prižiūrimi tik juos sukūrusio centro arba skalės vieneto (diegimas, sukūręs duomenis).
>
> Net, kai konkretus procesas palaiko skalės vienetą, atkreipkite dėmesį, kad ne visi reikalingi duomenys gali būti sinchronizuoti iš centro į skalės vienetą arba iš skalės vienetą į centrą, dėl ko gali įvykti netikėtas sistemos apdorojimas. Pavyzdžiai:
> 
> - Jei naudojate vietos nurodymo užklausą, kuri sujungia duomenų lentelės įrašą, egzistuojantį tik diegiant centrą.
> - Jei naudojate krovinio vietos būsenos ir (arba) vietos tūrio matavimo funkcijas. Šie duomenys nebus sinchronizuoti tarp diegimų, todėl jie veiks tik atnaujinant vieno iš diegimų turimų atsargų vietą.

Tolesnės sandėlio valdymo funkcijos šiuo metu nepalaikomos skalės vienetų darbo krūviams:

- Kroviniui priskirtų pirkimo užsakymo eilučių gavimo apdorojimas
- Projekto pirkimo užsakymų gavimo apdorojimas
- Įvesties ir išvesties apdorojimas prekėms, turinčioms aktyvias sekimo dimensijas **Savininkas** ir (arba) **Serijos numeris**
- Atsargų, turinčių blokavimo būsenos vertę, apdorojimas
- Atsargų būsenos keitimas bet kurio darbo perkėlimo proceso metu
- Užsakymui įsipareigojusios, lanksčios, sandėlio lygio dimensijų rezervacijos
- Funkcijos *Sandėlio vietos būsena* naudojimas (duomenys nėra sinchronizuojami tarp diegimų)
- Funkcijos *Vietos numerio lentelės padėtis* naudojimas
- Funkcijų *Produktų filtrai* ir *Produktų filtrų grupės*, įskaitant **Dienų skaičius paketams sumaišyti** parametrą, naudojimas
- Integravimas su kokybės valdymu
- Apdorojimas su esamo svorio prekėmis
- Apdorojimas su prekėmis, kurias galima naudoti transportavimo valdymui (TMS)
- Apdorojimas su neigiamomis turimomis atsargomis
- Sandėlio darbo apdorojimas su pasirinktiniais darbo tipais
- Sandėlio darbo apdorojimas su siuntimo pastabomis
- Sandėlio darbo apdorojimas su medžiagų tvarkymu/„warehouse automation”
- Produkto bendrųjų duomenų vaizdo naudojimas (pavyzdžiui, sandėlio valdymo mobiliųjų įrenginių programėlėje)

> [!WARNING]
> Kai kurios sandėlio funkcijos nebus galimos sandėliams, kuriuose vykdomi sandėlio valdymo darbo krūviai skalės vienete, ir taip pat nepalaikoma centro arba skalės vieneto darbo krūvyje.
> 
> Kitos galimybės gali būti apdorojamos abiejuose, tačiau kai kuriuose scenarijuose jas reikės naudoti kruopščiai, pavyzdžiui, kai bus atnaujintos to paties sandėlio tiek centro, tiek skalės vieneto atsargos dėl asinchroninio duomenų atnaujinimo proceso.
> 
> Konkrečios funkcijos (pavyzdžiui, *blokavimo darbas*), kurias palaiko tiek centro, tiek skalės vienetai, bus palaikomas tik duomenų savininkui.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Siuntimas (palaikomas tik pirkimo ir perkėlimo užsakymams)

Tolesnė lentelė rodo, kurios siuntimo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Procesas                                                      | Centras | WES darbo krūvis skalės vienete |
|--------------------------------------------------------------|-----|------------------------------|
| Šaltinių dokumento tvarkymas                                   | Taip | Ne |
| Krovinio ir gabenimo valdymo tvarkymas                | Taip | Ne |
| Išleidimas į sandėlį                                         | Taip | Ne |
| Suplanuotas prekių skirstymas                                        | Ne  | Ne |
| Siuntos konsolidacija                                       | Taip | Ne |
| Siuntimo bangos tvarkymas                                     | Taip, tačiau centras tvarko tik bangos inicijavimą ir užbaigimą. Tai reiškia, kad siuntimo perkėlimo ir pirkimo užsakymo apdorojimą gali tvarkyti tik skalės vienetas.|<p>Ne, inicijavimą ir užbaigimą tvarko centras, o **Krovinio kūrimas ir rūšiavimas** yra nepalaikoma<p><b>Pastaba:</b> Prieiga į centrą yra būtina norint užbaigti bangos statusą kaip bangos tvarkymo dalį.</p> |
| Bangos siuntų tvarkymas                                  | Taip | Ne |
| Sandėlio darbo tvarkymas (įsk. licencijos plokštelės spausdinimą)        | Ne  | <p>Taip, bet tik aukščiau paminėtoms palaikomoms galimybėms. |
| Klasterio paėmimas                                              | Ne  | Taip|
| Rankinis pakavimo apdorojimas, įskaitant „Supakuoto konteinerio paėmimo” darbo apdorojimą | Ne <P>Kai kuriuos apdorojimus galima atlikti po pradinio išrinkimo proceso, apdorojamo skalės vieneto, tačiau tai nerekomenduojama dėl šių užblokuotų operacijų.</p>  | Ne |
| Konteinerio pašalinimas iš grupės                                  | Ne  | Ne |
| Siuntimo rūšiavimo tvarkymas                                  | Ne  | Ne |
| Su kroviniu susijusių dokumentų spausdinimas                           | Taip | Ne |
| ASN kūrimo važtaraštis                            | Taip | Ne |
| Siuntos patvirtinimas                                             | Taip | Ne |
| Siuntos patvirtinimas su „Patvirtinti ir perkelti”            | Ne  | Ne |
| Važtaraščio ir sąskaitos faktūros išrašymo apdorojimas                        | Taip | Ne |
| Trumpas paėmimas (pardavimo ir perkėlimo užsakymai)                    | Ne  | Ne |
| Perviršinis paėmimas (pardavimo ir perkėlimo užsakymai)                     | Ne  | Ne |
| Darbo vietų pakeitimas (pardavimo ir perkėlimo užsakymai)         | Ne  | Taip|
| Darbo užbaigimas (pardavimo ir perkėlimo užsakymai)                    | Ne  | Taip|
| Darbo ataskaitos spausdinimas                                            | Taip | Ne |
| Bangos žymė                                                   | Ne  | Taip|
| Darbo skaidymas                                                   | Ne  | Taip|
| Darbo apdorojimas – valdomas „transportavimo pakrovimo”            | Ne  | Ne |
| Paimto kiekio sumažinimas                                       | Ne  | Ne |
| Darbo atšaukimas                                                 | Ne  | Ne |
| Siuntos patvirtinimo atšaukimas                                | Taip | Taip |

### <a name="inbound"></a>Gaunama

Tolesnė lentelė rodo, kurios gavimo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Procesas                                                          | Centras | WES darbo krūvis skalės vienete<BR>*(Prekės, pažymėtos „Taip”, yra taikomos tik sandėlio užsakymams)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Šaltinių&nbsp;dokumento&nbsp;tvarkymas                             | Taip | Ne |
| Krovinio ir gabenimo valdymo tvarkymas                    | Taip | Ne |
| Gautos siuntos patvirtinimas                                    | Taip | Ne |
| Pirkimo užsakymo leidimas į sandėlį (sandėlio užsakymo tvarkymas) | Taip | Ne |
| Sandėlio užsakymo eilučių atšaukimas<p>Atminkite, kad tai palaikoma tik tada, kai eilutėje neįvyko jokia registracija</p> | Taip | Ne |
| Pirkimo užsakymo prekės gavimas ir atidėjimas                       | <p>Taip,&nbsp;kai&nbsp;nėra&nbsp;sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, kai pirkimo užsakymas nėra dalis <i>krovinio</i></p> |
| Pirkimo užsakymo eilutės gavimas ir atidėjimas                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | <p>Taip, kai pirkimo užsakymas nėra dalis <i>krovinio</i></p></p> |
| Grąžinimo užsakymo gavimas ir atidėjimas                              | Taip | Ne |
| Skirtingų numerio lentelių gavimas ir atidėjimas                       | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne, kai yra sandėlio užsakymas</p> | Ne |
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

| Procesas                                            | Centras | WES darbo krūvis skalės vienete |
|----------------------------------------------------|-----|------------------------------|
| Licencijos lentelės užklausa                              | Taip | Taip                          |
| Prekės užklausa                                       | Taip | Taip                          |
| Vietos užklausa                                   | Taip | Taip                          |
| Sandėlio keitimas                                   | Taip | Taip                          |
| Judėjimas                                           | Taip | Taip                          |
| Judėjimas pagal šabloną                               | Taip | Taip                          |
| Sandėlio perkėlimas                                 | Taip | Ne                           |
| Perkėlimo užsakymo kūrimas iš sandėlio programos           | Taip | nr.                           |
| Keitimas (į/iš)                                | Taip | Taip, bet ne koregavimo scenarijui, kuriame atsargų rezervavimas turi būti pašalintas, naudojant atsargų koregavimo tipų parametrą **Pašalinti** rezervavimus.</p>                           |
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
| Darbo atšaukimas                                        | Taip | Taip                          |


### <a name="production"></a>Gamyba

Sandėlio valdymo gamybos scenarijai šiuo metu nepalaikomi skalės vieneto darbo eigose, kaip rodoma tolesnėje lentelėje.

| Apdorojimas | Centras | WES darbo krūvis skalės vienete |
|---------|-----|------------------------------|
| <p>Visi sandėlio valdymo procesai yra susiję su gamyba. Štai keletas pavyzdžių:</p><li>Išleidimas į sandėlį</li><li>Gamybos bangos tvarkymas</li><li>Žaliavų paėmimas</li><li>RAF ir baigtų prekių atidėjimas</li><li>Sudėtinio ir šalutinio produktų atidėjimas</li><li>„Kanban“ atidėjimas</li><li>„Kanban“ paėmimas</li><li>Gamybos užsakymo pradžia</li><li>Gamybos nurašymas</li><li>Paskutinis produkcijos padėklas</li><li>Medžiagų sunaudojimo registravimas</li><li>Tuščias „kanban“</li></ul> | Taip | Ne |

## <a name="maintaining-scale-units-for-wes"></a>Skalės vienetų WES palaikymai

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
