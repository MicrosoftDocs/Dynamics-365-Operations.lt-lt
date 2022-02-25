---
title: Elektroninių ataskaitų komponentai
description: Šioje temoje aprašomi elektroninių ataskaitų (ER) komponentai.
author: nselin
ms.date: 09/28/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.topic: overview
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a24aa52c805722c20045b6227ceac0103cfbe6b
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324040"
---
# <a name="electronic-reporting-components"></a>Elektroninių ataskaitų komponentai

[!include [banner](../includes/banner.md)]

Elektroninės ataskaitos (ER) palaiko šiuos komponentų tipus:

- Duomenų modelis
- Modelio susiejimas
- Formatuoti
- Metaduomenys

## <a name="data-model-component"></a>Duomenų modelio komponentas

Duomenų modelio komponentas abstrakčiai vaizduoja duomenų struktūrą. Jis yra naudojamas tam tikrai verslo domeno sričiai aprašyti pakankamai išsamiai, kad būtų tenkinami tos srities ataskaitų reikalavimai. Duomenų modelio komponentą sudaro toliau nurodytos dalys.

- **Duomenų modelis** – kaip domenui būdingų verslo objektų rinkinys ir hierarchiškai susistemintas jų ryšių aprašas.
- **Modelio susiejimas** – Kuris susieja pasirinktus duomenų šaltinius su atskirais duomenų modelio elementais, vykdymo metu nurodančiais duomenų srautą ir taisykles, pagal kurias verslo duomenys įvedami į duomenų modelio komponentą.

Duomenų modelio verslo objektas pateikiamas kaip konteineris ar įrašas. Verslo subjekto ypatybės pateikiamos kaip duomenų elementai ar laukai. Kiekvienas duomenų elementas turi unikalų pavadinimą, žymę, aprašą ir reikšmę. Kiekvieno duomenų elemento reikšmė gali būti sukurta taip, kad būtų atpažinta kaip eilutė, sveikasis skaičius, realusis skaičius, data, išvardijimas ar Bulio logika. Be to, tai gali būti kitas duomenų įrašas arba įrašų sąrašas.

Viename duomenų modelio komponente gali būti kelios domenui būdingų verslo objektų hierarchijos. Jame taip pat gali būti modelio susiejimai, kurie vykdymo metu palaiko konkretų ataskaitai būdingą vykdymo laiką. Hierarchijos yra atskiriamos pagal vieną įrašą, kuris buvo pasirinktas kaip šakninis modelio susiejimo įrašas. Pavyzdžiui, mokėjimo domeno srities duomenų modelis gali palaikyti tolesnius susiejimus.


- Įmonė \> Tiekėjas \> AP domeno mokėjimo operacijos
- Klientas \> Įmonė \> AR domeno mokėjimo operacijos

Atkreipkite dėmesį, kad verslo objektai, pvz., įmonė ir mokėjimo operacijos, yra kuriami vieną kartą. Skirtingi susiejimai, jei reikia, gali juos naudoti dar kartą.

## <a name="model-mapping-component"></a>Modelio susiejimo komponentas

Modelio susiejimo nuorodos susieja pasirinktus duomenų šaltinius su atskirais duomenų modelio elementais, vykdymo metu nurodančiais duomenų srautą ir taisykles, pagal kurias verslo duomenys įvedami į duomenų modelio komponentą.

Modelio susiejimas, kuris palaiko siunčiamus elektroninius dokumentus, turi šias galimybes:

- Jis gali naudoti skirtingus duomenų tipus kaip duomenų modelio duomenų šaltinius. Šie duomenų tipus apima lenteles, duomenų metodus ir numerius.
- Jis palaiko vartotojo įvesties parametrus, kuriuos galima apibrėžti kaip duomenų modelio šaltinius, kai kai kuriuos duomenis reikia nurodyti vykdymo laike.
- Jis palaiko duomenų transformavimą į reikiamas grupes. Su juo Jūs galite filtruoti, rūšiuoti ir sumuoti duomenis, taip pat pridėti loginius apskaičiuotus laukus, sukurtus su formulėmis, panašiomis į „Microsoft Excel“ formules. Daugiau informacijos žr. [Formulės kūrimo įrankis elektroninėje ataskaitoje (ER)](general-electronic-reporting-formula-designer.md).

Modelio susiejimas, kuris palaiko gaunamus elektroninius dokumentus, turi šias galimybes:

- Jis gali naudoti skirtingus „Finance and Operations“ naujinamus duomenų elementus kaip tikslus. Šie duomenų elementai apima lenteles, duomenų objektus ir rodinius. Duomenis galima atnaujinti naudojant ateinančius duomenis iš gaunamų elektroninių dokumentų. Vieno modelio susiejime galima naudoti kelis tikslus.
- Jis palaiko vartotojo įvesties parametrus, kuriuos galima apibrėžti kaip duomenų modelio šaltinius, kai kai kuriuos duomenis reikia nurodyti vykdymo laike.

Duomenų modelio komponentas yra skirtas kiekvienam verslo domenui, kuris naudojamas kaip suvienodintas duomenų šaltinis ataskaitoms teikti. Bendrasis duomenų šaltinis užduoja ataskaitas nuo faktinio duomenų šaltinių diegimo. Komponento verslo koncepcijos ir funkcijos, pateiktos tokia forma, dėl kurios ataskaitų formato pirminis kūrimas ir tolesnė priežiūra tampa efektyvesnė.

## <a name="format-component"></a>Formato komponentas

### <a name="format-components-for-outgoing-electronic-documents"></a>Siunčiamų elektroninių dokumentų formato komponentai

Formato komponentas yra ataskaitų kūrimo planas, kuris bus generuojamas vykdymo laiku. Schemą sudaro toliau nurodyti elementai.

- Formatas, kuris apibrėžia vykdymo metu sugeneruoto siunčiamo elektroninio dokumento struktūrą ir vykdymo laike.
- Duomenų šaltiniai kaip vartotojo įvesties parametrų rinkinys ir domenui būdingų duomenų modelis, kuris naudoja pasirinktą modelio susiejimą.
- Formato susiejimas kaip formato duomenų šaltinių susiejimų su atskirais formato elementais, vykdymo metu nurodančiais vykdymo laiką ir formato išvesties kūrimo taisykles, susiejimų rinkinys.
- Formato tikrinimas kaip konfigūruojamų taisyklių, kurios vykdymo metu valdo ataskaitos generavimą pagal vykdymo laiką, rinkinys. Pavyzdžiui, gali būti taisyklė, kuri sustabdo tiekėjo mokėjimų išeigos generavimą ir pritaiko išimtį, jei trūksta konkrečių pasirinkto tiekėjo atributų, pvz., banko sąskaitos numerio.

Formato komponentas palaiko tolesnes funkcijas.

- Ataskaitos išeigos kaip atskirų skirtingų formatų, pvz., teksto, XML, „Microsoft Word“ dokumento ar darbalapio, failų kūrimas
- Kelių failų kūrimas atskirai ir tų failus galudinant juos į „zip“ failus

Formato komponentas leidžia pridėti toliau nurodytus tam tikrus failus, kurie gali būti naudojami ataskaitų išeigoje.

- „Excel“ darbaknyges, kuriose yra darbalapis, galima naudoti kaip OPENXML darbalapio formato išeigos šabloną
- „Word“ failus, kuriuose yra dokumentas, kurį galima naudoti kaip „Microsoft Word“ dokumento formato išeigos šabloną
- Kiti failai, kurie gali būti įtraukti į formato išeigą kaip iš anksto apibrėžti failai

Šis pavyzdys rodo, kaip juda šių formatų duomenų srautai.

[![Gaunamų formato komponentų duomenų srautas.](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Norėdami paleisti vieną ER formato konfigūraciją ir importuoti duomenis iš gaunamo elektroninio dokumento, turite nustatyti norimą formato konfigūracijos susiejimą, taip pat modelio susiejimo integravimo tašką. Galite naudoti tą patį modelio susiejimą ir paskirties vietas kartu su skirtingo tipo gaunamų dokumentų skirtingais formatais.

## <a name="component-versioning"></a>Komponento versijos kūrimas

Palaikomas ER komponento versijos kūrimas. Toliau pateikta ER komponentų pakeitimų valdymo darbo eiga.

1. Pradinė sukurta versija pažymima kaip **Juodraštis**. Šią versiją galima redaguoti ir ją galima tikrinti.
2. Versiją **Juodraštis** galima konvertuoti į versiją **Baigta**. Šią versija galima naudoti vietiniuose ataskaitų teikimo procesuose.
3. Versiją **Baigta** galima konvertuoti į versiją **Bendrai naudojama**. Ši versija publikuojama „Microsoft Dynamics“ „Lifecycle Services“ (LCS) ir ją galima naudoti visuotiniuose ataskaitų teikimo procesuose.
4. Versiją **Bendrai naudojama** galima konvertuoti į versiją **Nebenaudojama**. Tada šią versiją bus galima naikinti.

Kai versijos būsena yra **Baigta** arba **Bendrai naudojama**, galima keistis duomenimis dar kitu būdu. Jei komponento būsena yra viena iš šių, galima atlikti toliau nurodytus veiksmus.

- Komponentą galima išdėstyti eilutėmis XML formatu ir eksportuoti kaip failą XML formatu.
- Komponentą galima sugrąžinti iš XML failo ir importuoti į programą kaip naują ER komponento versiją.

## <a name="component-date-effectivity"></a>Komponento galiojimo data

ER komponento versijos turi galiojimo datą. Galite nustatyti ER komponento datą Galioja nuo, kad nurodytumėte datą, nuo kurios šis komponentas galioja ir jį galima naudoti ataskaitų teikimo procesuose. Programos seanso data naudojama apibrėžti, ar komponentas yra tinkamas vykdyti. Jei konkrečią dieną galioja konkreti versija, ataskaitų teikimo procesuose naudojama naujausia versija.

## <a name="component-access"></a>Prieiga prie komponento

Prieiga prie ER formato komponentų priklauso nuo Tarptautinės standartų organizacijos (ISO) valstybės / regiono kodo parametro. Kai šis pasirinktos formato konfigūracijos versijos parametras nenurodytas, formato komponentą galima pasiekti iš bet kurios įmonės vykdymo laiku. Jei šiame parametre yra ISO valstybės / regiono kodai, formatas komponentą galima pasiekti tik iš tų įmonių, kurių pagrindinis adresas nurodytas kaip vienas iš formato komponento ISO valstybės / regiono kodų.

Skirtingos duomenų formato komponento versijos gali turėti skirtingus ISO valstybės / regiono kodų parametrus.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

