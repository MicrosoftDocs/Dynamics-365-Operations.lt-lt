---
title: Ganto diagramos naudojimas užduotims planuoti
description: Naudodami Ganto diagramas gamybos planuotojai gali valdyti ir optimizuoti gamybos planus.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage, GanttColorTable, GanttReqExplosionColor, GanttReqExplosionSetup, GanttTable, GanttTimescaleSetup, GanttWrkCtr, GanttWrkCtrColor, GanttWrkCtrJobInfo, GanttWrkCtrLoadResources, GanttWrkCtrMoveJob, GanttWrkCtrSetup, GanttWrkCtrView
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 180fb7b31ea826c546aa8472a7ef4025a3b8865a783a5b662ed30b69f98acf92
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730207"
---
# <a name="gantt-chart-for-job-scheduling"></a>Ganto diagramos naudojimas užduotims planuoti

[!include [banner](../includes/banner.md)]

Ganto diagrama yra skirta suteikti teisę gamybos planuotojams valdyti ir optimizuoti gamybos planą. Ganto diagrama išskaidrina operacijų srautą, tampa paprasta reguliuoti gamybos grafiką ir atsižvelgti į medžiagų arba išteklių trūkumus. Tai padeda planuotojams geriau išnaudoti turimus išteklius, sumažinti nebaigtą gamybą ir optimizuoti gamybos užsakymų našumo laiką.

Ganto diagramoje yra pavaizduota apibrėžto laiko intervalo suplanuota veikla. Veikla planuojama ištekliams, kurių pajėgumas nustatytas pajėgumų kalendoriuje. Ganto diagramoje galima parodyti pateiktų tipų veiklą.

-   Užduotys iš gamybos užsakymų, kuriuose yra suplanuotos užduotys.
-   Užduotys iš suplanuotų gamybos užsakymų.
-   Suplanuota projekto užduočių veikla, kurios tipas Valandų prognozės.

Ganto diagramą galima atidaryti dviem skirtingais būdais, **Užsakymo rodinys** ir **Išteklių rodinys**. Rodinyje **Užsakymo rodinys** veikla grupuojama pagal gamybos užsakymus Tai gali būti naudinga, pvz., jei norite tvarkyti visų užduočių, priklausančių tiems patiems užsakymams, apžvalgą. **Išteklių rodinyje** visos užduotys yra grupuojamos pagal atskirus išteklius. Šis rodinys gali būti naudingas optimizuojant planą išteklių lygiu, pvz., įrenginio arba įrenginių grupės. Tolesniuose paveikslėliuose pateiktos Ganto diagramos rodo **Užsakymo rodinį** ir **Išteklių rodinį** su šiais pagrindiniais elementais:

1.  Ganto diagramos veikla
2.  Medžiagų trūkumo piktograma
3.  Medžiagų pasiekiamumo piktograma
4.  Užsakymo pristatymo datos piktograma
5.  Pajėgumo juosta

## <a name="order-view"></a>Užsakymo rodinys

[![Užsakymo rodinys.](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Išteklių rodinys
[![Išteklių rodinys.](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Veiklos
Veikla rodoma kaip juostos ir išdėstoma laiko skalės tinklelyje nurodant suplanuotą pradžios ir pabaigos laiką, todėl juostų ilgis yra proporcingas laikui, kuris būtinas veiklai atlikti. Veikla rodoma pagal laiko skalę. Galite reguliuoti laiko skalę meniu, kuriame pasirenkate pradžios ir pabaigos datą bei laiko vienetą, pvz., valandas arba dienas. Reguliuodami laiko skalę galite nustatyti laiko intervalo centrą, kuriame norite tvarkyti veiklą. 

Norint gauti geresnę apžvalgą yra skirtingų parinkčių, kuriomis galima valdyti veiklos spalvą. Galite konfigūruoti atskirą veiklos spalvą, naudoti temos spalvą, kuri yra bendra programoje naudojama spalvų tema, arba nustatyti, kad spalva būtų valdoma pagal gamybos užsakymų spalvos kodą. 

Veiklos laiko intervalas turi šešėlinį foną. Laikotarpiai su baltu šešėliu rodo laiko intervalą su nustatytu veiklos išteklių pajėgumu, o laikotarpiai su pilku šešėliu rodo laiko intervalus be nustatyto pajėgumo. 

Kairiojoje diagramos pusėje yra papildomos informacijos apie veiklą, pvz., išteklius, kuriems yra suplanuota veikla, ir gamybos užsakymo numeris. Ryšys tarp tam pačiam užsakymui priklausančių užduočių rodomas rodykle. 

Daugiau informacijos apie veiklą galite gauti veiklos dialogo lange. Norėdami atidaryti dialogo langą, dukart spustelėkite veiklą arba pasirinkite meniu **Informacija**. Veiklos dialogo lange galite matyti suplanuotą pradžios ir pabaigos datą, laiko informaciją ir kurias medžiagas planuojama naudoti veikloje. 

Veiklą galima grupuoti grupavimo lygiuose. Grupavimo lygiai yra hierarchiniai ir gali būti naudojami norint logiškai grupuoti veiklą. Pavyzdžiui, jei turite maketą, kuriame gamybos veikla grupuojama pagal teritoriją, gamybos vienetus, išteklių grupes ir išteklius, galite naudoti grupavimo lygius norėdami grupuoti veiklą pagal tą maketą. Grupavimo lygius galima išplėsti ir sutraukti arba atskiru grupavimo lygiu, arba visais diagramos lygiais, naudojant meniu mygtukus **Išplėsti viską** ir **Sutraukti viską**. Be to, atidarę diagramą galite konfigūruoti ir išplėstinus arba sutrauktinus grupavimo lygius.

### <a name="material-availability"></a>Medžiagų pasiekiamumas

Galima nustatyti, kad Ganto diagrama suteiktų planuotojui išsamios informacijos apie individualios veiklos medžiagų būseną. Pavyzdžiui, tai gali būti naudinga, jei medžiaga vėluoja ir tai paveiks gamybos planą. Šiuo atveju medžiagų klausimai bus pažymėti Ganto diagramoje siekiant padėti planuotojui suprasti pasekmes ir atlikti būtinus pakeitimus. 

Užduotis bus rodoma su medžiagų trūkumo piktograma, jei užduoties grafiko pradžios data yra vėlesnė nei užduoties naudojamų medžiagų pasiekiamumo data. Medžiagų pasiekiamumo data apskaičiuojama remiantis iškvietimo informacija dinaminiame pagrindiniame plane. Pavyzdžiui, medžiagų trūkumo piktograma pasirodys užduotyje, kurioje naudojama medžiaga, susieta su pirkimo užsakymu, kurio gavimas vėlesnis nei suplanuota užduoties pradžios data.

### <a name="indicator-of-material-availability-date"></a>Medžiagų pasiekiamumo datos indikatorius

Kai nustatote, kad diagramoje būtų rodomos užduotys su medžiagų trūkumu, taip pat rodoma piktograma su užduoties medžiagų pasiekiamumo data. Piktograma bus rodoma, tik jei medžiagų pasiekiamumo data yra nustatytame diagramos laiko intervale. Jei medžiagų pasiekiamumo data nepatenka į nustatytą laiko intervalą, išsamesnės informacijos apie medžiagų pasiekiamumą galima gauti iš medžiagų sąrašo užduoties dialogo lange. Be to, sąraše yra piktograma, rodanti vėluojančias užduoties medžiagas. Galite perplanuoti užduotį medžiagų pasiekiamumo datą naudodami kaip pradžios datą.

### <a name="indicator-of-order-delivery-date"></a>Užsakymo pristatymo datos indikatorius

Ši piktograma rodo gamybos užsakymo pristatymo datą. Piktograma matoma tik užsakymo rodinyje.

### <a name="capacity-bar"></a>Pajėgumo juosta

Galite sukonfigūruoti diagramą, kad rodytų išteklių pajėgumo juostą. Ši juosta suteikia veiklos išteklių pajėgumo apžvalgą pagal diagramoje apibrėžtą laiko intervalą. Pajėgumo juosta nerodoma laikotarpiams, kuriems ištekliai nėra rezervuoti. Laikotarpiais, kai ištekliai yra rezervuoti pagal pajėgumą, rodoma ištisinė pajėgumo juosta. Laikotarpiais, kai rezervuota per daug išteklių, juosta bus storesnė ir raudona. Pvz., jei persidengia dvi užduotys, pajėgumo juosta nurodys per didelį rezervavimą konkrečiame laiko intervale. Pajėgumo juosta planuojant užduotį atnaujinama dinamiškai. Pajėgumo juostą įgalinate meniu **Rodyti pajėgumo juostą**. Ji gali būti rodoma **Išteklių rodinyje**. Jei norite gauti išsamesnį išteklių pajėgumų rodinį, naudokite diagramą **Pajėgumas**, kurią galima atidaryti iš meniu arba pasirinktos veiklos kontekstinio meniu.

## <a name="job-scheduling-in-the-gantt-chart"></a>Užduočių planavimas Ganto diagramoje
Ganto diagramoje siūloma skirtingų gamybos plano koregavimo parinkčių. Ganto diagramoje galite iš naujo suplanuoti veiklą naudodami nuvilkimo sąveiką arba grafiko meniu. Planavimo procese galite atsižvelgti į išteklių pajėgumą, galimybes ir medžiagų apribojimus.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Planuoti užduotį naudojant nuvilkimo sąveiką

Galite iš naujo suplanuoti užduotį nustatytame laiko intervale, naudodami nuvilkimo sąveiką. Galite iš naujo suplanuoti užduotį tik naudodami tuos pačius išteklius, vienu metu galite planuoti tik vieną užduotį.

### <a name="schedule-a-job-from-the-menu"></a>Planuoti užduotį meniu

Meniu **Planuoti užduotis** galite suplanuoti vieną ar daugiau diagramoje pasirinktų užduočių remdamiesi planavimo kryptimi ir planavimo data bei laiku. Galimos trys planavimo kryptys.

-   Pirmyn nuo planavimo datos
-   Atgal nuo planuotos datos
-   Persiųsti nuo medžiagų pasiekiamumo datos

Ganto diagramoje neįmanoma suplanuoti užduoties, kuri nepatenka į nustatytą laiko intervalą. Jei tai padarysite, užduotis liks nesuplanuota ir gausite klaidos pranešimą „Nepavyko suplanuoti užduoties įkeltą laikotarpį“.

### <a name="schedule-previous-jobs"></a>Planuoti ankstesnes užduotis

Veiklos tinkle, pvz., kai užduotys priklauso tam pačiam gamybos užsakymui, galite naudoti funkciją **Planuoti ankstesnes užduotis** norėdami suplanuoti ankstesnes užduotis, susijusias su pasirinkta tinklo užduotimi. Šiame pavyzdyje pažymėta veikla yra pasirinkta užduotis. Diagrama rodoma prieš suplanuojant ankstesnę užduotį ir ją suplanavus. 

[![Ankstesnės užduoties planavimas.](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Planuoti kitas užduotis

Galite naudoti funkciją **Planuoti kitas užduotis** norėdami suplanuoti kitas užduotis, susijusias su pasirinkta veiklos tinklo užduotimi. Šiame pavyzdyje pažymėta veikla yra pasirinkta užduotis. Diagrama rodoma prieš suplanuojant kitą užduotį ir ją suplanavus. 

[![Kitos užduoties planavimas.](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Planuoti aplink užduotį

Galite naudoti funkciją **Planuoti aplink užduotį** norėdami suplanuoti tolesnę užduotį ir ankstesnę užduotį, susijusią su pasirinkta veiklos tinklo užduotimi. Šiame pavyzdyje pažymėta veikla yra pasirinkta užduotis. Diagrama rodoma prieš suplanuojant užduotį ir ją suplanavus. 

[![Planuoti aplink užduotį.](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Išdėstyti darbus

Galite naudoti funkciją **Išdėstyti** norėdami išdėstyti pasirinktą to paties ištekliaus veiklą. Ši veikla gali būti tame pačiame veiklos tinkle, tačiau taip pat gali priklausyti skirtingiems tinklams. Kai naudojate išdėstymo funkciją, bus pašalinti laiko tarpai, esantys tarp pasirinktų veiklų. Galite naudoti šią funkciją norėdami optimizuoti išteklių pajėgumo naudojimą. Diagrama rodoma prieš suplanuojant užduotį ir ją suplanavus. 

[![Užduoties išdėstymas.](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Iš naujo priskirti veiklą iš vieno ištekliaus kitam

Galite iš naujo priskirti užduotį iš vieno ištekliaus kitam. Tai gali būti naudinga situacijose, kai įrenginys yra sugedęs arba per daug rezervuotas, o jums reikia rasti kitą išteklių, galintį atlikti užduotį.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Veiklos priskyrimas iš naujo naudojant nuvilkimo sąveiką

**Išteklių** rodinyje galite iš naujo priskirti veiklą kitam ištekliui (Ganto diagramoje) naudodami nuvilkimo sąveiką. Galite tai padaryti pasirinkę eilutę, kurioje suplanuota veikla. Pasirinkus eilutę galima nuvilkti ją į diagramos, sugrupuotos pagal skirtingą išteklių grupavimo lygį, išteklių.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Veiklos priskyrimas iš naujo iš užduočių planavimo meniu

Galite iš naujo priskirti užduotį iš dialogo lango **Planuoti užduotį**, atidaryto meniu **Planuoti užduotį**. Iš šio meniu galite tik iš naujo priskirti užduotį ištekliui, kuris jau įkeltas į Ganto diagramą. Jei pasirenkate tik vieną užduotį, tada išteklių išplečiamasis sąrašas bus rūšiuojamas pagal taikytinus išteklius. Jei pasirenkate daugiau užduočių, tada nebus informacijos apie taikytinus išteklius iš išteklių sąrašo.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Įkelti papildomų išteklių į Ganto diagramą
**Išteklių rodinyje** galite pasirinkti įkelti papildomų išteklių į Ganto diagramą. Tai gali būti naudinga, jei norite užduočiai, kuri suplanuota įrenginiui, kuris pernelyg rezervuotas arba sugedęs, rasti alternatyvių išteklių. Puslapyje **Įkelti papildomų išteklių** gausite sąrašą išteklių, kurie tinkami pagal datą atidarius sąrašą. Pirmiausia bus pateikiami taikytini ištekliai, susiję su pasirinkta Ganto diagramos užduotimi. Jei pasirinkote kelias užduotis, prieš atidarant sąrašą nebus rodomi taikytini ištekliai. Puslapyje **Įkelti papildomų išteklių** galite pasirinkti vieną ar daugiau išteklių, kurie bus įkelti į Ganto diagramą, kai patvirtinsite savo pasirinkimą. Jei nėra užduočių, suplanuotų pasirinktam ištekliui Ganto diagramos laiko intervale, tada ištekliai bus išdėstyti pagal išteklių grupavimo lygį, Ganto diagramos veiklos sąrašo apačioje.

### <a name="access-the-gantt-chart"></a>Prieiga prie Ganto diagramos

Ganto diagramą galima atidaryti iš šių puslapių.


|                                                 <strong>Puslapis</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Aprašymas</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Gamybos užsakymų sąrašas ir informacija</strong>                                    | Puslapyje <strong>Gamybos užsakymų sąrašas ir informacija</strong> galite atidaryti Ganto diagramą iš vieno ar daugiau pasirinktų užsakymų. Atidarant diagramą iš meniu <strong>Ganto diagrama</strong> bus įkeltos visos užduotys, susijusios su pasirinktais gamybos užsakymais, taip pat ir užduotys iš kitų gamybos užsakymų, kurie suplanuoti tiems patiems ištekliams. Atidarant diagramą iš meniu elemento <strong>Ganto diagrama – sparčioji peržiūra</strong> bus įkeltos tik užduotys, susijusios su pasirinktais gamybos užsakymais. Šiame rodinyje užduočių negalima planuoti. |
|                                               <strong>Ištekliai</strong>                                                |                                                                                                                                                        Puslapyje <strong>Ištekliai</strong> galite atidaryti Ganto diagramą iš meniu elemento <strong>Ganto diagrama</strong>. Pasirinkus į diagramą bus įkeltos visos užduotys, suplanuotos ištekliui pasirinktame laiko intervale.                                                                                                                                                         |
|                                            <strong>Išteklių grupė</strong>                                             |                                                                                                                                                 Puslapyje <strong>Išteklių grupė</strong> galite atidaryti Ganto diagramą iš meniu elemento <strong>Ganto</strong> diagrama. Pasirinkus, pasirinktame laiko intervale bus rodomos visos užduotys, suplanuotos ištekliams išteklių grupėje.                                                                                                                                                 |
|                                             <strong>Ganto diagramos</strong>                                              |                                                                                 Puslapyje <strong>Ganto diagramos</strong> galite konfigūruoti Ganto diagramas pagal išteklius ir išteklių grupes. Pvz., jei norite valdyti tam tikrų išteklių arba išteklių grupių gamybos veiklą, tada atskirai juos sukonfigūruokite puslapyje <strong>Ganto diagramos</strong>. Galite atidaryti Ganto diagramą iš kiekvienos konfigūracijos.                                                                                 |
|                                       <strong>Valandų prognozės</strong> (projektas)                                        |                                                                                                                              Ištekliams galima planuoti projekto veiklą, kurios tipas <strong>Valandų prognozė</strong>. Meniu <strong>Planavimas</strong> puslapyje <strong>Valandų prognozė</strong> Ganto diagramą galite atidaryti užsakyme ir peržiūrėti suplanuotą užduoties projekto veiklą, kurios tipas – Valandų prognozė.                                                                                                                               |
|           <strong>Atliktina užduotis</strong> (sąrašas <strong>Gamybos vietos valdymo</strong> darbo srityje)            |                                                                                               <strong>Atliktinų užduočių sąrašo gamybos vietos valdyme</strong> darbo sritis rodo užduotis iš gamybos ir paketinių užsakymų, kurios atliekamos naudojant pasirinktus darbo srities išteklius. Meniu elemente <strong>Ganto diagrama</strong> galite atidaryti Ganto diagramą ir visos sąraše pasirinktos užduotys bus įkeltos į diagramą.                                                                                               |
| <strong>Gamybos užsakymai, kuriuos reikia išleisti</strong> (atidaromi iš <strong>Gamybos vietos valdymo</strong> darbo srities) |                                                                                                                                         Gamybos užsakymų, kuriuos reikia išleisti, puslapis, atidaromas <strong>Gamybos vietos valdymo</strong> darbo srities. Šiame puslapyje rodomi suplanuoti gamybos ir paketiniai užsakymai, laukiantys išleidimo. Šiame puslapyje galite atidaryti pasirinktų gamybos užsakymų Ganto diagramą.                                                                                                                                          |

## <a name="additional-resources"></a>Papildomi ištekliai  
[Vaizdinis planavimas naudojant Ganto diagramą (gamybos ir paketiniai užsakymai) (vaizdo įrašas)](https://youtu.be/BtbuShkGj4I)

[Vaizdinis gamybos planavimas (demonstracinis scenarijus)](/dynamics/s-e/)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]