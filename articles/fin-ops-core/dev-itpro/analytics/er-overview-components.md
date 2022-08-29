---
title: Elektroninių ataskaitų komponentai
description: Šiame straipsnyje aprašomi elektroninių ataskaitų (ER) komponentai.
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285038"
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

[![Siunčiamų formato komponentų duomenų srautas](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Norėdami paleisti vieną ER formato konfigūraciją ir generuoti siunčiamą elektroninį dokumentą, turite nustatyti formato konfigūracijos susiejimą.

#### <a name="format-components-for-incoming-electronic-documents"></a>Gaunamų elektroninių dokumentų formato komponentai
Formato komponentas yra gaunamo dokumento planas, kuris importuojamas vykdymo metu. Schemą sudaro toliau nurodyti elementai.

- Formatas, kuris apibrėžia vykdymo metu importuoto gaunamo elektroninio dokumento, kuriame yra duomenų, struktūrą ir turinį. Formato komponentas naudojamas išanalizuoti įvairiais formatais gaunamą dokumentą, pvz., teksto ir XML.
- Formato susiejimas, kuris sujungia atskirus formato elementus į konkrečios srities duomenų modelio elementus. Vykdymo metu duomenų modelio elementai nurodo duomenų srautą ir duomenų importavimo iš gaunamo dokumento taisykles, o tada išsaugo duomenų modelio duomenis.
- Formato tikrinimas kaip konfigūruojamų taisyklių, kurios vykdymo metu valdo duomenų importavimą pagal vykdymo kontekstą, rinkinys. Pavyzdžiui, gali būti taisyklė, kuri sustabdo banko išrašo, kuriame pateikiami tiekėjo mokėjimai, duomenų importavimą ir pritaiko išimtį, jei trūksta konkretaus tiekėjo atributų, pvz., tiekėjo identifikavimo kodo.

Šis pavyzdys rodo, kaip juda šių formatų duomenų srautai.

[![Gaunamų formato komponentų duomenų srautas](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Norėdami paleisti vieną ER formato konfigūraciją ir importuoti duomenis iš gaunamo elektroninio dokumento, turite nustatyti norimą formato konfigūracijos susiejimą, taip pat modelio susiejimo integravimo tašką. Galite naudoti tą patį modelio susiejimą ir paskirties vietas kartu su skirtingo tipo gaunamų dokumentų skirtingais formatais.


## <a name="component-versioning"></a>Komponento versijos kūrimas

Palaikomas ER komponento versijos kūrimas. Toliau pateikta ER komponentų pakeitimų valdymo darbo eiga.

1. Iš pradžių sukurta versija pažymėta kaip **Juodraštis**. Šią versiją galima redaguoti ir ją galima tikrinti.
2. Versiją **Juodraštis** galima konvertuoti į versiją **Baigta**. Šią versija galima naudoti vietiniuose ataskaitų teikimo procesuose.
3. Versiją **Baigta** galima konvertuoti į versiją **Bendrai naudojama**. Ši versija publikuojama „Microsoft Dynamics“ „Lifecycle Services“ (LCS) ir ją galima naudoti visuotiniuose ataskaitų teikimo procesuose.
4. Versiją **Bendrai naudojama** galima konvertuoti į versiją **Nebenaudojama**. Tada šią versiją bus galima naikinti.

Kai versijos būsena yra **Baigta** arba **Bendrai naudojama**, galima keistis duomenimis dar kitu būdu. Jei komponento būsena yra viena iš šių, galima atlikti toliau nurodytus veiksmus.

- Komponentą galima išdėstyti eilutėmis XML formatu ir eksportuoti kaip failą XML formatu.
- Komponentą galima sugrąžinti iš XML failo ir importuoti į programą kaip naują ER komponento versiją.

Daugiau informacijos rasite importuokite [naują duomenų modelio konfigūraciją ir išvesto](er-quick-start1-new-solution.md#ImportDataModel)[formato užbaigtos versijos eksportavimą](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Juodraščio versijos vykdyklėje

Savo asmeniniuose ER sistemos vartotojo parametruose galite įgalinti parinktį, kuri leidžia nurodyti, ar ER konfigūracijos juodraščio versiją reikia naudoti vykdyklėje. Informacijos, kaip padaryti, kad jūsų **ER** konfigūracijų pasirinktis Vykdyti juodraštį būtų galima, [ieškokite pažymėti pasirinktinį formatą kaip vykdyklė](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> ER vartotojo parametrai yra specifiniai įmonei ir vartotojui.

### <a name="draft-format-versions-at-runtime"></a>Juodraščio formato versijos vykdyklėje

Pagal numatytuosius nustatymus, kai paleidžiate ER sprendimą, jo formato komponentų juodraščio versijų nepaisoma. Todėl naudojama tik atitinkama versija, kurios būsena yra kita nei **Juodraštis**. Kartais galite norėti priversti ER naudoti juodraščio versijos savo ER formato konfigūraciją vykdyklėje. Pvz., kai į savo juodraščio versiją pristatote reikiamus pakeitimus, galite naudoti tą juodraščio versiją bandymo paleidimui atlikti. Tokiu būdu galite patikrinti savo pakeitimų teisingumą. Norėdami pradėti naudoti juodraščio formato versiją, turite [nustatyti](er-quick-start2-customize-report.md#MarkFormatRunnable)**atitinkamos** ER konfigūracijos pasirinktį Vykdyti juodraštį kaip **Taip.**

### <a name="draft-model-mapping-versions-at-runtime"></a>Juodraščio modelio susiejimo versijos vykdyklėje

Pagal numatytuosius nustatymus paleidus ER sprendimą visada naudojamos jo modelių susiejimo komponentų juodraščio versijos. Kartais galite norėti priversti ER nepaisyti jūsų ER modelio susiejimo konfigūracijos juodraščio versijos vykdyklėje. Versijoje **10.0.29** ir vėliau galite visada atsižvelgti į ER **modelio susiejimų funkcijos pasirinktį Vykdyti juodraštį, kad būtų galima valdyti modelio susiejimo versiją,** naudojamą vykdyklėje. Kai ši funkcija įgalinta, įvyksta toks veikimo būdas:

- Kai modelio **susiejimo** konfigūracijos parinktis **Vykdyti** juodraštį nustatyta kaip Ne, didžiausia ne juodraščio versija, naudojama vykdyklėje. Išimtis pateikiama, jei konfigūracija dabartiniame finansų egzemplioriuje negalima.
- Kai parinktis **Vykdyti juodraštį** nustatyta kaip **Taip**, jei modelio susiejimo konfigūracijai naudojama juodraščio versija vykdyklėje.

## <a name="component-date-effectivity"></a>Komponento galiojimo data

ER formato komponentų versijos galioja nuo datos. Galite nustatyti ER formato komponento datą "galioja nuo", kad nurodydami datą, kada komponentas įsigalioja ataskaitų procesuose. Programos seanso data naudojama apibrėžti, ar komponentas yra tinkamas vykdyti. Jei konkrečią dieną galioja konkreti versija, ataskaitų teikimo procesuose naudojama naujausia versija.

## <a name="component-access"></a>Prieiga prie komponento

Prieiga prie ER formato ir modelio susiejimo komponentų vykdyklėje priklauso nuo Tarptautinės standartizavimo organizacijos (ISO) šalies/regiono kodo parametro. Jei pasirinktos formato arba modelio susiejimo konfigūracijos versijos parametras tuščias, formatą arba modelio susiejimo komponentą galima pasiekti iš bet kurios įmonės vykdyklėje. Jei parametre yra ISO šalies / regiono kodų, formato arba modelio susiejimo komponentą galima naudoti tik iš įmonių, kurių pagrindinis adresas nustatytas vienam iš formato komponento ISO šalies / regiono kodų.

Skirtingos formato arba modelio susiejimo komponento versijos gali turėti skirtingus ISO šalių / regionų kodų parametrus.

Daugiau informacijos ieškokite nuo šalies [konteksto priklausomų ER modelio susiejimų konfigūravimas](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

