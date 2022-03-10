---
title: Išleisti į sandėlį
description: Šioje temoje pateikiama informacija apie išleidimo į sandėlį procesą. Čia aprašomi objektai, kurie sukuriami išleidžiant užsakymą į sandėlį, ir pasirinktys, kurias galite naudoti procesui inicijuoti.
author: mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3269bf3f8a5475fb85e6b51514db29006be9aab1
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376213"
---
# <a name="release-to-warehouse"></a>Išleisti į sandėlį

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiama informacija apie išleidimo į sandėlį procesą. Čia aprašomi objektai, kurie sukuriami išleidžiant užsakymą į sandėlį, ir pasirinktys, kurias galite naudoti procesui inicijuoti.

## <a name="release-to-warehouse-overview"></a>Išleidimo į sandėlį peržiūrą

Išleidimas į sandėlį yra procesas, kai atsargos paruošios išsiųsti. Paleidus užsakymą į sandėlį, sistema sukuria krovinio eilutes ir siuntas. Jei nustatytas automatinis bangos apdorojimas, sukuriami kroviniai ir būtinas darbas. Susijusių objektų konfigūracija priklauso nuo sistemos parametrų. Šiame temos skyriuje peržiūrimi objektai, sukurti išleidžiant į sandėlį, ir juos apibrėžiami sistemos parametrai.

Siunta *yra* to paties kliento ar to paties pristatymo adreso pardavimo užsakymo ar perkėlimo užsakymo eilučių grupė.

Krovinys yra pardavimo užsakymo ar perkėlimo užsakymo eilučių, sugrupuotų kartu ir kurios paprastai perkeliamos viename sunkvežimiuose, automobiliuose ar kituose transportavimo *kursuose*, grupė. Krovinys gali turėti vieną ar daug siuntų. Galite rankiniu būdu sukurti krovinį pridėdami užsakymo eilutes prie naujo krovinio. Šiuo atveju užsakymo eilutės priskiriamos prie krovinio prieš inicijuojant išleidimo į sandėlį procesą ir jos gali būti išleistos tik iš krovinio planavimo **darbo srityje puslapio**.

Sandėlio *darbas* yra bet kuri sandėlio operacija, kurią atlieka sandėlio darbuotojas. Paprastai sandėlio darbo operacijas sudaro mažiausiai du veiksmai vienas po kito: sandėlio darbuotojas paima turimas atsargas vienoje vietoje ir tada padeda paimtas atsargas kitoje vietoje.

Paleidus užsakymą į sandėlį, sistema sukuria krovinio eilutes ir *siuntas bei* grupes į siuntas. Siuntos konsolidavimo procesas leidžia automatizuotą siuntos konsolidavimą išleidimo į sandėlį proceso metu. - Norėdami gauti daugiau informacijos, žr. [Siuntų konsolidavimo strategijos](about-shipment-consolidation-policies.md).

Sistema naudoja *bangas*, kad kurdama siuntos paėmimo darbą ir krovinius. Turi būti galimas bangos, kurią norite sukurti, tipo bangos *šablonas ir užsakymo* eilutės sandėlio bangos šablonas. Bangos šablono *Siuntimas* tipas yra naudojamas siekiant siųsti bangos šabloną pardavimo ir perkėlimo užsakymo prekių siuntimui.

Kiekviename bangos šablone yra *bangos metodų*. Bangos metodai atlieka veiksmus, pvz., kuria bangos darbą arba kuria krovinius. Pavyzdžiui, siuntimo bangos šablone gali būti krovinių kūrimo, eilučių paskirstymo bangoms, papildymo ir bangos išrinkimo darbo kūrimo metodų. Bangos šablonas nustato daug parametrų, kaip nustatyta banga bus generuojama ir apdorojama, įskaitant tuos veiksmus, kuriuos reikia atlikti rankiniu būdu ir tuos, kurie atliekami automatiškai. Daugiau informacijos rasite [Bangos šablonai](wave-templates.md). Todėl, atsižvelgiant į jūsų bangos šablono konfigūraciją, banga sukuriama automatiškai, apdorojama ir išleidžiama, kai išleidžiate užsakymą į sandėlį, arba kai kurie arba visi šie veiksmai atliekami rankiniu būdu atlikus išleidimą į sandėlį.

Kai banga apdorojama, sistema sukuria paėmimo darbą, remdamasi tinkamu *darbo šablonu* ir *vietos nuostatas*, ir padaro jį prieinamą mobiliųjų įrenginių darbą. Darbo šablonas nustato, kaip atliekamas kiekvieno sandėlio proceso darbas, o vietos direktyvos nurodo atsargų perkėlimo paėmimo ir padavimo vietas. Dėl išsamesnės informacijos, žr. [Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietos nurodymus](control-warehouse-location-directives.md).

> [!NOTE]
> Pagal numatytuosius nustatymus bangos apdorojamos paketiniu režimu.

Apdorojant bangą, sistema paprastai sukuria naują kiekvienos siuntos krovinį, kuriam nepriskirtas joks krovinys. Jei norite, kad vietoj esamų krovinių sistema priskirų nepriskirtas siuntas, galite naudoti išplėstinio bangos krovinio kūrimo funkciją. Daugiau informacijos žr. [Išplėstinis krovinio kūrimas bangos metu](advanced-load-building-during-wave.md).

Pardavimo **užsakymų ir** perkėlimo **užsakymų puslapiuose** alite peržiūrėti objektus, kurie sukurti užsakymo eilutėms išleidimo į sandėlį proceso metu.

- **Pardavimo užsakymai** puslapis:

    - „FastTab“ **Pardavimo užsakymo eilutėse** rinkitės **Sandėlis** ir tada meniu rinkitės **Siuntimo informaciją** kad atidarytumėte susijusias siuntas,, **Krovinio informaciją** kad atidarytumėte susijusius krovinius ar **darbo informaciją** norėdami atidaryti susijusio darbo informaciją.
    - Išsamios **eilutės informacijos** „FastTab" pasirinkite skirtuką **Krovinys**, norėdami peržiūrėti susijusius krovinius.

- **Perkėlimo užsakymų** puslapis:

    - Veiksmų srities skirtuke **Siuntimas** skirtuke rinkitės **Siuntos informacija** kad atidarytumėte susijusias siuntas, arba **Krovinio informacija** kad atidarytumėte susijusius krovinius.
    - Perkėlimo **užsakymo eilutėse** „FastTab" pasirinkite **Darbo informaciją** kad atidarytumėte susijusią darbo informaciją.

Apibendrinant, kai užsakymas išleidžiamas į sandėlį, pats automatizuotiausias srautas veikia tokiu būdu:

1. Sistema sukuria užsakymo siuntą ir bangą.
1. Banga apdorojama.
1. Sistema sukuria krovinį ir darbo ID.

Kai kurie šio srauto veiksmai gali būti atlikti rankiniu būdu, tai priklauso nuo bangos šablonų, darbo šablonų ir vietos nurodymų parametrų. Tačiau bendras srautas lieka toks pat.

Turite kelias pasirinktis, kaip išleisti užsakymą į sandėlį. Galite atlikti operaciją neautomatiniu būdu arba nustatyti paketinę užduotį. Likusiuose šios temos skyriuose išsamiai peržiūrima įvairūs būdai, kaip galite išleisti į sandėlio operaciją.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Išleisti į sandėlį rankiniu būdu iš pardavimo užsakymų ir perkėlimo užsakymų puslapių

Galite išleisti užsakymą į sandėlį tiesiogiai iš **pardavimo užsakymų** puslapio arba **užsakymų puslapio** pasirinkdami **Išleisti į sandėlį**.

- Pardavimo **užsakymų puslapyje** mygtukas yra veiksmų srities **Sandėlis** skirtuke.
- Pardavimo **užsakymų puslapyje** mygtukas yra veiksmų srities **Siuntimas** skirtuke.

Pardavimo **užsakymų puslapyje** vienu metu galite pateikti keletą pardavimo užsakymų.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Išleisti į sandėlį rankiniu būdu iš išleidimo į sandėlį puslapių

Sistema šiuo metu pateikia tris puslapius, kuriuose galite peržiūrėti kelių užsakymų eilutes ir paleisti jas į sandėlį:

- **Išleisti į sandėlį** (**„Warehouse management“ \> Išleisti į sandėlį \> Išleisti į sandėlį**) – šis puslapis leidžia dirbti su pardavimo užsakymais ir perkėlimo užsakymais. Tačiau jis veikia lėčiau nei kiti du puslapiai. Šis puslapis greitai bus pasenusias.
- **Išleidimo pardavimo užsakymų į sandėlį** (**„Warehouse management“ \> Išleisti į sandėlį \> Išleisti į sandėlį pardavimo užsakymus**) – šis puslapis leidžia dirbti su pardavimo užsakymais ir perkėlimo užsakymais. Tačiau jos našumas didesnis nei puslapio **Išleisti į sandėlį** našumas.
- **Išleidimo perdavimo užsakymų į sandėlį** (**„Warehouse management“ \> Išleisti į sandėlį \> Išleisti į sandėlį perdavimo užsakymus**) – šis puslapis leidžia dirbti su perdavimo užsakymais ir perkėlimo užsakymais. Tačiau jos našumas didesnis nei puslapio **Išleisti į sandėlį** našumas.

Visuose trijuose puslapiuose galima naudoti panašias funkcijas, kaip aprašyta likusioje šio skyriaus dalyje. Visi jie leidžia pasirinkti užsakymo eilutes arba visus užsakymus ir paleisti jas į sandėlį.

Kiekvieną puslapį sudaro viršutinė dalis, kurioje galite pasirinkti užsakymo eilutes, ir apatinė dalis, kurioje galite inicijuoti išleidimo į sandėlį procesą. Viršutinėje dalyje galite naudoti filtrus pardavimo užsakymo eilutėms, kurias norite pateikti, ieškoti. Puslapyje **šleisti į sandėl** viršutiniame skyriuje pateikiami atskiri pardavimo ir perkėlimo užsakymų skirtukai, o kiekvienas iš kitų dviejų puslapių rodo tik vieno tipo užsakymą.

Įrankių juosta viršutinėje dalyje apima šiuos mygtukus, kuriuos galite naudoti norėdami pasirinkti užsakymo eilutes į sandėlį:

- **Įtraukti** – pasirinkite vieną ar daugiau užsakymo eilučių viršutinėje dalyje, tada pasirinkite šį mygtuką tose eilutėse, kurios yra apatinėje dalyje.
- **Pridėti viską** – pridėti visas eilutes iš viršutinės sekcijos į apatinę dalį.
- **Pridėti užsakymą** – pasirinkite užsakymą, tada pasirinkite šį mygtuką, norėdami iš to užsakymo pridėti visas eilutes į apatinę dalį.

Baigę įtraukti eilutes į apatinę dalį, pažymėkite kiekvieną eilutę, kurią norite paleisti. Tada įrankių **juostoje pasirinkite** Išleisti į sandėlį, kad šias eilutes būtų galima paleisti į sandėlį.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Rankinis išleidimas į sandėlį iš krovinio planavimo darbo stalo puslapio

Užsakymus į sandėlį galite išleisti rankiniu būdu, naudodami puslapį **Krovinio planavimo darbo** srityje. Šis puslapis leidžia tvarkyti užsakymo eilutes į krovinius ir išleisti šiuos krovinius į sandėlį.

Norėdami atverti **Krovinio planavimo darbo stalas** puslapyje eikite į **Warehouse management \> Kroviniai**. Taip pat galite jį atidaryti iš **pardavimo užsakymų** ir **perkėlimo užsakymų** puslapių. Viršutinėje puslapio dalyje galite pasirinkti pardavimo užsakymo eilutes skirtuke **Pardavimo eilutės** ir perkėlimo užsakymo eilutes skirtuke **Perkėlimo eilutės** tada pridėti tas eilutes prie naujo arba esamo krovinio.

Veiksmų srities **skirtuke Tiekimas ir** poreikis yra šie mygtukai, kuriuos galite naudoti, norėdami į krovinį įtraukti užsakymo eilutes viršutinėje dalyje:

- **Naujam kroviniui** – pasirinkite vieną ar daugiau užsakymo eilučių viršutinėje dalyje, tada sukurkite naują apkrovą ir įtraukite tas eilutes, kurios yra apatinėje dalyje.
- **Esamam kroviniui** – pasirinkite vieną ar daugiau užsakymo eilučių viršutinėje dalyje, tada sukurkite esamą apkrovą ir įtraukite tas eilutes, kurios yra apatinėje dalyje.
- **Visas užsakymas naujam kroviniui** – pasirinkite vieną ar daugiau užsakymo eilučių viršutinėje dalyje, tada sukurkite visas eilutes iš tų užsakymų.
- **Visas užsakymas esamam kroviniui** – pasirinkite vieną ar daugiau užsakymo eilučių viršutinėje dalyje, tada tą užsakymą iš esamo krovinio.

Apatinėje dalyje galite peržiūrėti sukurtus krovinius. Norėdami išleisti krovinius į sandėlį, juos pasirinkite ir tada rinkitės **Išleidimas \> Išleidimas į sandėlį** įrankių juostoje. Jei naudojate automatinį bangos apdorojimą, nes kroviniai jau priskirti užsakymo eilutėms, sistema sukuria siuntas ir darbo SF, kai atliekama išleidimo į sandėlį operacija.

## <a name="automatic-release-to-the-warehouse"></a>Automatinis išleidimas į sandėlį

Norėdami automatiškai paleisti užsakymus į sandėlį, naudokite **automatinio pardavimo užsakymų paleidimo** ir **automatinio perkėlimo užsakymų paleidimo** užduotis.

Norėdami nustatyti paketinę užduotį išleidžia į prekybos užsakymus, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Automatinis pardavimo užsakymų išleidimas**.
1. Dialogo lange **Automatinis prekybos užsakymų išleidimas** „FastTab“ skirtuke **Parametrai** nustatykite šiuos laukelius:

    - Parametras **Išleidžiamas kiekis** – pasirinkite, ar visas kiekis ar kaip paketas turi būti išleistas visas kiekis, ar fiziškai rezervuotas kiekis į sandėlį.
    - **Leisti išleisti iš dalies išleistų užsakymų** – nurodyti, ar likę iš dalies išleistų užsakymų kiekiai turėtų būti išleisti į sandėlį.
    - **Rezervuoti išleidžiant prekes** – nurodykite, ar kiekiai, kurie buvo automatiškai rezervuoti pardavimo užsakymui, turi išlikti rezervuoti, jei išleidimo į sandėlį procesas nepavyksta.
    - **Grupuoti paleidimus pagal klientą** – nurodyti, ar sistema turi apdoroti kiekvieno kliento paleidimą į sandėlį atskirai, ar išleisti visus pardavimo užsakymus tuo pačiu metu. Kai ši parinktis nustatyta kaip *Taip*, sistema surinks visas pasirinkto kliento pardavimo užsakymo eilutes, išleis šiuos užsakymus į sandėlį, tada apdoros kitą klientą. Kai ši parinktis nustatyta kaip *Ne*, sistema išleis visas galimas pardavimo užsakymo eilutes vienos paleisti į sandėlį operacijos metu. Įgalindami šią pasirinktį, galite padidinti paleidimo į sandėlį proceso efektyvumą ir efektyvumą. Tačiau šią pasirinktį reikia naudoti kartu su bangos šablonais, sukonfigūruotais apdoroti bangas išleidžiant į sandėlį, nes šis derinys gali sugeneruoti daug vieno kliento bangų, kurių kiekviena iš jų sugeneruota tik tam klientui. Jei norite generuoti darbą, kuriame kelių klientų siuntos sujungiamos, turite arba išjungti grupės išleidimą pagal klientą, *arba* sukonfigūruokite bangos šablonus, kad būtų naudojamas atidėtas apdorojimas.
    - **Užrakintas užsakymų tvarkymas** – pasirinkite, kaip sistema turi tvarkyti pardavimo užsakymus, kurie šiuo metu yra užrakinti, nes juos redaguoja kiti vartotojai arba procesai:

        - *Palaukite, kol užsakymai bus atrakinti* – sistema turi laukti, kol užsakymai bus atrakinti, prieš išleidžiant juos į sandėlį. Šiuo atveju paleidimo į sandėlį procesas gali užtrukti.
        - *Praleisti užrakintus užsakymus* – sistema turi praleisti užrakintus užsakymus.

    - **Tinkami užsakymo tipai** – pasirinkite pardavimo užsakymų tipus, kuriuos norite įtraukti į paketą.
    - **Kredito limito tipas** – pasirinkite, ar kredito limitų tikrinimai turi būti atliekami paleidimo į sandėlį proceso metu ir, jei čekiai turėtų būti atlikti, operacijos informaciją, kuri bus įtraukta į juos.

1. Norėdami kontroliuoti, kurie užsakymai turi būti apdorojami, **įrašuose, kuriuos norite įtraukti** į „FastTab", pasirinkite **Filtras**. Atsiranda standartinis užklausos dialogo langas, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip tik kitiems fono užduočių tipams „Microsoft Dynamics 365 Supply Chain Management“.
1. Dalyje **Vykdyti fone** "FastTab" rinkitės, ar užduotis ji būtų vykdoma paketiniu režimu ir (ar) nustatyti esamą grafiką. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Pasirinkite **Gerai**, jei norite pritaikyti parametrus pradėkite leidimo į sandėlį procesą.

Norėdami nustatyti paketinę užduotį išleidžia į perdavimo užsakymus, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Automatinis perkėlimo užsakymų išleidimas**.
1. Dialogo lange **Automatinis perdavimo užsakymų išleidimas** „FastTab“ skirtuke **Parametrai** nustatykite šiuos laukelius:

    - Parametras **Išleidžiamas kiekis** – pasirinkite, ar visas kiekis ar kaip paketas turi būti išleistas visas kiekis, ar fiziškai rezervuotas kiekis į sandėlį.
    - **Leisti išleisti iš dalies išleistų užsakymų** – nurodyti, ar likę iš dalies išleistų užsakymų kiekiai turėtų būti išleisti į sandėlį.
    - **Grupuoti paleidimus pagal paskirties sandėlį** – nurodykite, ar sistema turi paleisti visus perkėlimo užsakymus tuo pačiu metu, ar turi grupuoti perkėlimo užsakymo eilutes pagal paskirties sandėlį, o tada paleisti kiekvieną grupę į sandėlį atskirai.

1. Norėdami kontroliuoti, kurie užsakymai turi būti apdorojami, **įrašuose, kuriuos norite įtraukti** į „FastTab", pasirinkite **Filtras**. Atsiranda standartinis užklausos dialogo langas, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip tik kitam darbui „Supply Chain Management“ fono užduočių tipams.
1. Dalyje **Vykdyti fone** "FastTab" rinkitės, ar užduotis ji būtų vykdoma paketiniu režimu ir (ar) nustatyti pakartojimo grafiką. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Pasirinkite **Gerai**, jei norite pritaikyti parametrus pradėkite leidimo į sandėlį procesą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
