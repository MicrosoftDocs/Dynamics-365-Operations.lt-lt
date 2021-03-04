---
title: Sandėlio valdymo darbo krūvis debesiui ir krašto skalės vienetams
description: Šioje temoje pateikta informacija apie funkcijas, kuriso įjungia skalės vienetus siekiant vykdyti pasirinktus procesus iš jūsų sandėlio valdymo darbo krūvio.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516838"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Sandėlio valdymo darbo krūvis debesiui ir krašto skalės vienetams

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ne visos verslo funkcijos yra visiškai palaikomos viešoje peržiūroje, kai darbo apkrovos skalės vienetai yra naudojami. Įsitikinkite, kad naudojate tik procesus, kuriuos atskirai aprašo šis skyrius, kaip palaikomus.

## <a name="warehouse-execution-on-scale-units"></a>Sandėlio vykdymas skalės vienetuose

Šioje temoje pateikta informacija apie funkcijas, kurios įjungia sandėlio valdymo pajėgumus. Debesies skalės vienetai vykdo savo darbo krūvius debesyje naudodami paskirto tvarkymo pajėgumą jūsų pasirinktame „Microsoft Azure“ regione. Dėl krašto skalės vienetų, galite vykdyti kai kuriuos darbo krūvius nepriklausomai nuo patalpų, net ir kai skalės vienetai laikinai atjungti nuo debesies.

Šioje temoje sandėlio valdymo vykdymai sandėlyje, kuris nustatytas skalės vienete yra žinomi kaip *Sandėlio vykdymo sistema* (*WES*).

## <a name="prerequisites"></a>Būtinieji komponentai

Privalote turėti „Dynamics 365 Supply Chain Management“ centrą ir skalės vienetą, kurie bus patalpnti sandėlio valdymo darbo krūvyje. Dėl daugiau informacijos apie talpinimo procesą ir architektūrą, žr. [Debesies ir krašto skalės vienetų gamyba ir sandėlio valdymo darbo krūviai](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Kaip WES darbo krūviai veikia skalės vienetuose

Tam, kad procesai sandėlio valdymo darbo krūvyje veiktų, duomenys sinchronizuojami tarp centro ir skalės vienetų.

Skalės vienetas gali palaikyti tik turimus duomenis. Duomenų nuosavybės sąvoka skalės vienetams padeda apsisaugoti nuo kelių pagrindinių konfliktų. Dėl to, svarbu jums suprasti, kurie procesai turimi centro ir kurie turimi skalės vienetų.

Skalės vienetai turi tolesnius duomenis:

- **Bangos tvarkymo duomenys** – Pasirinkti bangos tvarkymo metodai yra tvarkomi kaip skalės vieneto bangos tvarkymo dalis.
- **Darbo tvarkymo duomenys** – Tolesni darbo tvarkos tipo tvarkymai yra palaikomi:

    - Inventoriaus judėjimai (rankiniai judėjimai ir pagal šablono darbą)
    - Pirkimo užsakymai (atidėjimo darbas per sandėlio užsakymą)
    - Prekybos užsakymai (pavyzdžio paėmimas ir pakrovimo darbas)

- **Sandėlio darbo gavimo duomenys** – Šie duomenys naudojami tik pirkimo užsakymams, kurie yra rankiniu būdu paleisti į sandėlį.
- **Licencijos lentelės duomenys** – Licencijos lentelės gali būti sukurtos centre ir skalės vienete. Paskirtas konflikto valdymas buvo patvirtintas. Atminkite, kad šie duomenys nėra būdingi sandėliui.

## <a name="outbound-process-flow"></a>Siuntimo tvarkymo eiga

Centras turi tolesnius duomenis:

- Visi šaltinio dokumentai, tokie kaip pardavimo užsakymas ir perdavimo užsakymai
- Užsakymo paskyrimas ir siuntimo krūvio tvarkymas
- Norėdami paleisti į sandėlį, siuntimo sukūrimas ir bangos kūrimo procesai

Skalės vienetai turi realų bangos tvarkymą (tokį kaip darbo skyrimą, pildymo darbą ir paklausos darbo kūrimą) po bangos paleidimo. Dėl to, sandėlio darbuotojai gali tvarkyti siuntimo darbą naudodami sandėlio programą, sujungtą su skalės vienetu.

![Bangos tvarkymo eiga](./media/wes_wave_processing_flow.png "Bangos tvarkymo eiga")

## <a name="inbound-process-flow"></a>Gavimo tvarkymo eiga

Centras turi tolesnius duomenis:

- Visi šaltinio dokumentai, tokie kaip pirkimo užsakymas ir pardavimo grąžinimo užsakymai
- Gavimo krovinio tvarkymas

> [!NOTE]
> Gavimo pirkimo užsakymo eiga yra sąvokos skirtumas iš siuntimo eigos, kurioje skalės vienetas atlieka tvarkymą priklausomai nuo to, ar užsakymas paleistas į sandėlį.

Jei naudojate *paleidimo į sandėlį* procesą, sandėlio užsakymai sukuriami ir susijusios gaunančios eigos nuosavybė priskirta skalės vienetui. Centras nebegalės registruoti gavimo.

Darbuotojas gali vykdyti gavimo procesą naudodamas sandėlio programą, sujungtą su skalės vienetu. Duomenys tuomet įrašomi pagal skalės vienetą ir pranešami pagal gavimo sandėlio užsakymą. Tolesnio atidėjimo tvarkymas ir kūrimas taip pat bus tvarkomas pagal skalės vienetą.

Jei nenaudojate *leidimo į sandėlį* procesą ir dėl to nenaudojate *sandėlio užsakymų*, centras gali sutvarkyti sandėlio gavimo ir darbo tvarkymą nepriklausomai nuo skalės vienetų.

![Gavimo tvarkymo eiga](./media/wes_Inbound_flow.png "Gavimo tvarkymo eiga")

## <a name="supported-processes-and-roles"></a>Palaikomi procesai ir vaidmenys

Ne visi sandėlio valdymo procesai palaikomi WES darbo krūvyje skalės vienete. Dėl to, rekomenduojame jums priskirti vaidmenis, kurie atitinka funkcijas prieinamas kiekvienam vartotojui.

Norėdami palengvinti šį procesą, pavyzdžio vaidmuo pavadinimu *Sandėlio vadovas darbo krūvyje* yra įtrauktas į demonstracinius duomenis **Sistemos administravimas \> Sauga \> Saugos konfigūravimas**. Šio vaidmenis tikslas yra užtikrinti sandėlio vadovų prieiga prie WES skalės vienete. Vaidmenys suteikia prieigą prie puslapių, kurie yra svarbūs darbo krūvio kontekste, patalpintame skalės vienete.

Vartotojo vaidmenys skalės vienete yra priskiriamos kaip pradinių duomenų sinchronizavimo dalis iš centro į skalės vienetą.

Norėdami keisti vaidmenis priskirtus vartotojui, eikite į **Sistemos administravimas \> Sauga \> Priskirti vartotojams vaidmenis** skalės vienete. Vartotojai besielgiantys kaip sandėlio vadovai tik skalės vienetuose turi būti priskiriami tik *Sandėlio vadovo darbo krūvio* vaidmenims. Toks požiūris užtikrins, kad tie vartotojai turės prieigą tik prie palaikomų funkcijų. Pašalinkite bet kuriuos vaidmenis, priskirtus tiems vartotojams.

Vartotojai besielgiantys kaip sandėlio tiek centre, tiek skalės vienetams, turi būti priskirti prie esančio *Sandėlio darbuotojo* vaidmenims. Atsiminkite, kad vaidmuo suteikia sandėlio darbuotojams prieigą prie funkcijos (tokią, kaip perdavimo užsakymo tvarkymas), kuris pasirodo vartotojo sąsajoje (UI), tačiau šiuo metu nepalaikomos skalės vienetuose.

## <a name="supported-wes-processes"></a>Palaikomi WES procesai

Tolesni sandėlio valdymo procesai gali būti įjungti WES darbo krūviui skalės vienete:

- Pasirinkti bangos tvarkymo metodai yra įjungti prekybos užsakymams ir paklausos papildymui
- Vykdymo darbo užsakymai iš prekybos užsakymai ir paklausos papildyma sandėlio darbui naudodami sandėlio programą
- Laukiantis turimas inventorius su sandėlio programa
- Inventoriiaus kūrimo ir vykdymo judėjimus su sandėlio programa
- Pirkimo užsakymų ir atidėjimo darbo darymo registravimas su sandėlio programa

Tolesni darbo užsakymo tipai šiuo metu palaikomi WES darbo krūviuose skalės vieneto talpinimuose:

- Pardavimo užsakymai
- Papildymas
- Atsargų perkėlimas
- Įsigijimo užsakymai, kurie yra susieti su sandėlio užsakymais

Nėra kito šaltinių dokumento tvarkymo šiuo metu palaikomo skalės vienetuose. Pavyzdžiui, WES darbo krūvis skalės vienete, negalite atlikti jame šių veiksmų:

- Paleisti perlaidos užsakymo.
- Tvarkyti išvesties sandėlio paėmimo ir siuntimo operacijų.

> [!IMPORTANT]
> Jei naudojate darbo krūvį skalės vienete, negalite nepalaikyti tvarkymo konkretaus sandėlio centre.

Tolesnės sandėlio valdymo funkcijos šiuo metu nepalaikomos skalės vienetuose:

- Įvesties ir išvesties tvarkymas prekėms, kurios neturi jokių sekimo matmenų (tokių kaip bendri ar serijos numerio matmenys)
- Inventoriaus būsenos keitimų tvarkymas
- Inventoriaus tvarkymas, kuris turi blokavimo būsenos vertę
- Integravimas su kokybės valdymu
- Integravimas su gamyba
- Svorio pagavimo prekių tvarkymas
- Per didelio pristatymo ar nepristatymo tvarkymas
- Neigiamo turimo inventoriaus tvarkymas

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Siuntimas (palaikomas prekybos užsakymams ir paklausos pildymui)

Tolesnė lentelė rodo, kurios siuntimo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

> [!WARNING]
> Kadangi tik prekybos užsakymo tvarkymas palaikomas, siuntimo sandėlio valdymo tvarkymas negali būti naudojamas perdavimo užsakymams.
>
> Kai kurios sandėlio funkcijos nebus prieinamos sandėliuose, kuriuose veikia sandėlio valdymo darbo krūvių skalės vienete.

| Apdoroti                                                      | Tranzito punktas | WES darbo krūvis skalės vienete |
|--------------------------------------------------------------|-----|------------------------------|
| Šaltinių dokumento tvarkymas                                   | Taip | nr. |
| Krovinio ir gabenimo valdymo tvarkymas                | Taip | nr. |
| Išleisti į sandėlį                                         | Taip | nr. |
| Siuntos konsolidacija                                       | nr.  | nr. |
| Kryžminis dokas (paėmimo darbas)                                 | nr.  | nr. |
| Siuntimo bangos tvarkymas                                     | Ne, tačiau bango būsenos užbaigimą tvarko centras |<p>Taip, bet tolesni pajėgumai nepalaikomi:</p><ul><li>Paralelinio darbo kūrimas</li><li>Krovinio kūrimas ir rūšiavimas</li><li>Krovimas į konteinerius</li><li>Bangos žymos spausdinimas</li></li></ul><p><b>Pastaba:</b> Patekite į centrą ir tą būtina padaryti norint užbaigti bangos statusą kaip bangos tvarkymo dalį.</p> |
| Sandėlio darbo tvarkymas (įsk. licencijos plokštelės spausdinimą)     | nr.  | <p>Taip, bet tik tolesni pajėgumai nepalaikomi:</p><ul><li>Pardavimo paėmimas (nenaudojant įjungtų sekimo matmenų)</li><li>Pardavimo krovinys (nenaudojant įjungtų sekimo matmenų)</li></ul> |
| Klasterio paėmimas                                              | nr.  | nr. |
| Pakavimo tvarkymas                                           | nr.  | nr. |
| Siuntimo rūšiavimo tvarkymas                                  | nr.  | nr. |
| Su kroviniu susijusių dokumentų spausdinimas                           | Taip | nr. |
| ASN kūrimo važtaraštis                            | Taip | nr. |
| Siuntimo patvirtinimas ir pakavimo kvito tvarkymas                | Taip | nr. |
| Trumpas paėmimas (prekybos užsakymas)                                 | nr.  | nr. |
| Darbo atšaukimas                                            | nr.  | nr. |
| Darbo vietų pakeitimas (prekybos užsakymai)                      | nr.  | nr. |
| Darbo užbaigimas (prekybos užsakymai)                                 | nr.  | nr. |
| Blokuoti ir atblokuoti darbą                                       | nr.  | nr. |
| Keisti vartotoją                                                  | nr.  | nr. |
| Spausdinti darbo atsakaitą                                            | nr.  | nr. |
| Bangos žymė                                                   | nr.  | nr. |
| Atšaukti darbą                                                 | nr.  | nr. |

### <a name="inbound"></a>Gaunama

Tolesnė lentelė rodo, kurios gavimo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Apdoroti                                                          | Tranzito punktas | WES darbo krūvis skalės vienete |
|------------------------------------------------------------------|-----|------------------------------|
| Šaltinių&nbsp;dokumento&nbsp;tvarkymas                                       | Taip | nr. |
| Krovinio ir gabenimo valdymo tvarkymas                    | Taip | nr. |
| Siuntimo tvirtinimas                                            | Taip | nr. |
| Pirkimo užsakymo leidimas į sandėlį (sandėlio užsakymo tvarkymas) | Taip | nr. |
| Pirkimo užsakymo prekės gavimas ir atidėjimas                        | <p>Taip,&nbsp;kai&nbsp;nėra&nbsp;sandėlio užsakymo</p><p>Ne,kai yra sandėlio užsakymas</p> | <p>Taip, kai yra sandėlio užsakymas ir kai pirkimo užsakymas nėra <i>krovinio</i> dalis. Nepaisant to, du mobilių įrenginių meniu prekių turi būti naudojama, viena gavimo (<i>Pirkimo užsakymo prekės gavimas</i>) ir kitas su <b>Naudoti esamą užsakymą</b> parinktimi įjungta siekiant tvarkyti atidėjimą.</p><p>Ne, kai nėra sandėlio užsakymo.</p> |
| Gaunama ir atidedama pirkimo užsakymo eilutė                        | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne,kai yra sandėlio užsakymas</p> | nr. |
| Grąžinimo užsakymo gavimas ir atidėjimas                               | Taip | nr. |
| Skirtingų numerio lentelių gavimas ir atidėjimas                        | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne,kai yra sandėlio užsakymas</p> | nr. |
| Krovinio prekės gavimas                                              | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne,kai yra sandėlio užsakymas</p> | nr. |
| Numerio lentelės gavimas ir atidėjimas                              | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne,kai yra sandėlio užsakymas</p> | nr. |
| Perkėlimo užsakymo prekės gavimas ir atidėjimas                        | Taip | nr. |
| Perkeliama ir atidedama pirkimo užsakymo eilutė                        | Taip | nr. |
| Darbo atšaukimas                                                | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne,kai yra sandėlio užsakymas</p> | <p>Taip, bet <b>Neregistruotas gavimas atšaukiant darbo</b> parinktis (esanti <b>Sandėlio valdymo parametrų</b> puslapyje) nepalaikoma.</p> |
| Pirkimo užsakymo gamybos kvito tvarkymas                        | Taip | nr. |
| Kryžminio doko darbo kūrimas kaip gavimo dalis                 | <p>Taip, kai nėra sandėlio užsakymo</p><p>Ne,kai yra sandėlio užsakymas</p> | nr. |

### <a name="warehouse-operations-and-exception-handing"></a>Sandėlio operacijos ir išskirtinis tvarkymas

Tolesnė lentelė rodo, kurios sandėlio operacijos ir išskirtinės tvarkymo funkcijos palaikomos ir kada jos palaikomos, kai sandėlio valdymo darbo krūviai yra naudojami debesies ir krašto skalės vienetuose.

| Apdoroti                                            | Tranzito punktas | WES darbo krūvis skalės vienete |
|----------------------------------------------------|-----|------------------------------|
| Licencijos lentelės užklausa                              | Taip | Taip                          |
| Prekės užklausa                                       | Taip | Taip                          |
| Vietos užklausa                                   | Taip | Taip                          |
| Keisti sandėlį                                   | Taip | Taip                          |
| Judėjimas                                           | nr.  | Taip                          |
| Judėjimas pagal šabloną                               | nr.  | Taip                          |
| Keitimas (į/iš)                                | Taip | nr.                           |
| Ciklo skaičiavimas ir Neatitikimų skaičiavimo tvarkymas | Taip | nr.                           |
| Spausdinti dar kartą žymę (numerio lentelės spausdinimas)             | Taip | nr.                           |
| Numerio lentelės versija                                | Taip | nr.                           |
| Numerio lentelių grupavimas                                | Taip | nr.                           |
| Vairuotojo registravimas                                    | Taip | nr.                           |
| Vairuotojo išregistravimas                                   | Taip | nr.                           |
| Keisti siuntimo talpinimo kodą                      | Taip | nr.                           |
| Rodyti atidarytą užduočių sąrašą                             | Taip | nr.                           |
| Konsoliduoti numerių lenteles                         | nr.  | nr.                           |
| Pašalinti konteinerį iš grupės                        | nr.  | nr.                           |
| Atšaukti darbą                                        | nr.  | nr.                           |
| Min./maks. pildymo tvarkymas                   | nr.  | nr.                           |
| Vietos pildymo tvarkymas                  | nr.  | nr.                           |

### <a name="production"></a>Gamyba

Sandėlio valdymo integravimas gamybos scenarijams šiuo metu nepalaikomas, kaip rodoma tolesnėje lentelėje.

| Apdoroti | Tranzito punktas | WES darbo krūvis skalės vienete |
|---------|-----|------------------------------|
| <p>Visi sandėlio valdymo procesai yra susiję su gamyba. Štai keletas pavyzdžių:</p><li>Išleisti į sandėlį</li><li>Gamybis bangos tvarkymas</li><li>Žaliavų paėmimas</li><li>Baigtos prekės atidėtos</li><li>Sudėtinis produktas ir šalutinis produktas atidėti</li><li>„Kanban“ atidėtas</li><li>„Kanban“ paėmimas</li><li>Pradėti gamybos užsakymą</li><li>Gamybos nurašymas</li><li>Paskutinis produkcijos padėklas</li><li>Registruoti medžiagų sunaudojimą</li><li>Tuščias „kanban“</li></ul> | nr. | nr. |

## <a name="maintaining-scale-units-for-wes"></a>Palaikyti skalės vienetus WES

Keli bendri darbai vykdoma tiek centre, tiek skalės vienetuose.

Centro taplinime galite rankiniu būdu palaikyti bendrus darbus. Galite valdyti tolesnius tris darbus **Sandėlio valdymas \> Periodinės užduotys \> Galinio ofiso darbo krovos valdymas**:

- Apdoroti darbo būsenos naujinimo įvykį
- Apdoroti bangos vykdymo valdymo perdavimo įvykius
- Registruoti šaltinio užsakymo kvitus

Darbo krūvio skalės vienetuose, galite valdyti tolesnius du bendrus darbus **Sandėlio valdymas \> Periodinės užduotys \> Darbo krūvio valdymas**:

- Tvarkyti bangos lentelės įrašus
- Apdoroti bangos vykdymo valdymo perdavimo įvykius


[!INCLUDE[footer-include](../../includes/footer-banner.md)]