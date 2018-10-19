---
title: "Kliento operacijų sąrašo puslapis"
description: "Šioje temoje pateikiama informacija apie Kliento operacijų sąrašo puslapį, skirtą „Microsoft Dynamics 365 for Finance and Operations“"
author: mikefalkner
manager: aolson
ms.date: 08/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 79479f6949c52830918598583ee91dd85d2d7ac3
ms.contentlocale: lt-lt
ms.lasthandoff: 10/01/2018

---

# <a name="customer-transactions-list-page"></a>Kliento operacijų sąrašo puslapis

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Peržiūrėti sudengimus

Veiksmų srities mygtukas **Sudengimų peržiūra** suteikia greitą prieigą prie sudengimų retrospektyvos ir papildomos informacijos apie visą sudengimo operaciją. Taip pat galite peržiūrėti papildomas operacijas, susijusias su pasirinkta operacija, nes jos buvo įtrauktos į tą patį sudengimą arba nes jos yra mokėjimai, sukurti tame pačiame mokėjimo žurnale.

1. Pasirinkite **Gautinos sumos \> Visi klientai**.
2. Pasirinkite operacijų turintį klientą, tada veiksmų srities skirtuke **Klientas** pasirinkite **Operacijos**.
3. Pasirinkite norimą ištirti operaciją, paskui veiksmų srityje pasirinkite **Sudengimų peržiūra**.

    Rodomas dialogo langas **Sudengimų peržiūra**, kuriame vaizduojama pasirinkta operacija bei visi ja sudengti dokumentai. Šia dialogo langas panašus į sudengimo restrospektyvos rodinį, tačiau jame pateikti visi susiję dokumentai.

4. Šiame dialogo lange galite atlikti įvairias užduotis. Pasirinkite vieną arba daugiau kvitų, o tada paspauskite vieną iš toliau nurodytų mygtukų.

    - **Peržiūrėti susijusius mokėjimus** – Rodyti visas mokėjimų žurnalo operacijas, sukurtas mokėjimo žurnale, kuris susijęs su pasirinktu dokumentu. Be to, rodomi visi sudengimai, susiję su tais mokėjimais. Peržiūrint susijusius mokėjimus šio mygtuko žyma pasikeičia į **Sudengimų peržiūra**. Pasirinkite **Sudengimų peržiūra**, kad būtų rodomos tik tos operacijos, kurios buvo rodomos, kai pirmą kartą atidarėte dialogo langą **Sudengimų peržiūra**.
    - **Peržiūrėti retrospektyvą** – Rodyti kvitų sudengimo retrospektyvą. Pasirinkite **Uždaryti** norėdami uždaryti dialogo langą.
    - **Peržiūrėti apskaitą** – Rodyti visus su pasirinktais dokumentais susijusius kvitus. Pasirinkite **Uždaryti** norėdami uždaryti dialogo langą.
    - **Eksportuoti** – eksportuokite pasirinktus kvitus į „Microsoft Excel“.
    - **Operacijų sudengimas** – Šis mygtukas rodomas tik tuo atveju, jei pradinis pasirinktas dokumentas nebuvo visiškai sudengtas. Pasirinkus šį mygtuką rodomas dialogo langas **Operacijų sudengimas**, kuriame galite pasirinkti sudengimo operacijas.
    - **Sudengimų anuliavimas** – Šis mygtukas rodomas tik tuo atveju, jei pradinis pasirinktas dokumentas buvo visiškai sudengtas. Pasirinkus šį mygtuką pasirodo dialogo langas **Sudengimų anuliavimas**, kuriame galite atšaukti atliktus to dokumento sudengimus.

## <a name="global-transactions"></a>Visuotinės operacijos

Į klientų puslapį įtrauktas mygtukas **Visuotinės operacijos**. Naudodamiesi šiuo mygtuku galite peržiūrėti visas kliento operacijas visuose juridiniuose subjektuose. Sąrašo puslapyje **Kliento operacijos** rodomos tik tų juridinių subjektų operacijos, prie kurių vartotojas turi prieigą (priklausomai nuo jo / jos saugos parametrų).

Sąrašo puslapyje rodomos visos tą patį šalies ID kaip ir klientas, nuo kurio pradėjote, turinčių klientų operacijos. Pavyzdžiui, jei klientas US-001 viename juridiniame subjekte turi tą patį šalies ID kaip klientas DE-001 kitame juridiniame subjekte, rodomos visos abiejų klientų ID operacijos.

Sąrašo puslapio **Kliento operacijos** meniu skiriasi, priklausomai nuo operacijos juridinio subjekto. Pavyzdžiui, jei funkcija gali naudotis tik Šveicarijos juridiniai subjektai, tos funkcijos meniu parinktys rodomos tik pasirinkus Šveicarijos operaciją.

Norėdami pasinaudoti funkcija, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Gautinos sumos \> Visi klientai**.
2. Pasirinkite klientą, tada veiksmų srities skirtuko **Klientas** grupėje **Operacijos** pasirinkite **Visuotinės operacijos**.

## <a name="more-transaction-filters"></a>Daugiau operacijų filtrų 

Atidarytų operacijų rodymo filtras pakeistas nauju filtru, kuriuo naudodamiesi galite peržiūrėti daugiau operacijų derinių. Galimos toliau nurodytos lauko **Rodyti** parinktys.

- **Visos** – Rodyti visas pasirinktų klientų operacijas (atidarytas ir uždarytas).
- **Uždarytos** – Rodyti tik visiškai sudengtas ir uždarytas operacijas.
- **Atidarytos** – Rodyti tik tas operacijas, kurios dar ne visiškai sudengtos.
- **Atidarytos nuo datos** – Rodyti tik tas operacijas, kurios dar ne visiškai sudengtos nuo jūsų nurodytos datos. Pasirinkę šią parinktį galite keisti šalia filtro rodomą datą. Sąraše rodomos operacijos, prie kurių po jūsų nurodytos datos rodoma vertė **Paskutinio sudengimo data**, net jeigu tos operacijos visiškai sudengtos. Tačiau balansas reiškia balansus nuo dabartinės datos, ne nuo pasirinktos datos.

Taip pat pridėtas filtras, kuriuo naudodamiesi galite slėpti valiutos konvertavimo operacijas. Tiesiog pažymėkite žymės langelį **Slėpti valiutos perkainojimus**.

## <a name="more-easily-modify-due-dates-and-discount-dates"></a>Lengviau modifikuoti terminus ir nuolaidų datas

Galite atnaujinti atidarytų klientų operacijų terminus ir nuolaidų datas. Išleidus 8.1 versiją, pagerinta patirtis. Dabar sąrašo puslapyje **Kliento operacijos** galite pridėti terminų. Sąrašo puslapyje **Kliento operacijos** spustelėję terminą dialogo lange **Atnaujinti terminą ir mokėjimo nuolaidos datas** taip pat galite pakeisti terminus, nuolaidų datas, mokėjimo sąlygas ir mokėjimo nuolaidos sąlygas.

### <a name="activate-the-feature"></a>Funkcijos suaktyvinimas

Norėdami sąrašo puslapyje **Kliento operacijos** naudodamiesi dialogo langu **Atnaujinti terminą ir mokėjimo nuolaidos datas** pridėti terminų ir pakeisti operacijos mokėjimo parametrus, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
2. Skirtuke **Sudengimai** nustatykite srities **Rodyti terminą ir leisti koreguoti** parinktį **Taip**.
3. Tam, kad būtų galima naudotis šia funkcija, įtraukti nauji kliento operacijų veiksmai. Šie laukai užpildomi atlikus naują operaciją. Jie taip pat užpildomi atidarius dialogo langą **Atnaujinti terminą ir mokėjimo nuolaidos datas**. Nustatę srities **Rodyti terminą ir leisti koreguoti** parinktį **Taip** matysite dialogo langą **Naujinti mokėjimo informaciją**.  Norėdami iškart atnaujinti esamas operacijas, pasirinkite **Atnaujinti visas esamas operacijas**. Arba, norėdami užpildyti tik naujų operacijų laukus, pasirinkite **Tęsti be naujinimo**.

Dabar terminas įtrauktas į sąrašo puslapį **Kliento operacijos** ir jūs galite lengviau pakeisti operacijų terminus ir mokėjimo nuolaidų datas.

### <a name="modify-the-payment-settings"></a>Mokėjimo parametrų keitimas

Sąrašo puslapyje **Kliento operacijos** rodomos visos kliento operacijos. Pasirinkus operacijos terminą rodomas dialogo langas **Atnaujinti terminą ir mokėjimo nuolaidos datas**. Šiame dialogo lange rodoma pagrindinė termino data ir nuolaidos skaičiavimai, terminas, mokėjimo sąlygos, mokėjimo nuolaidos sąlygos ir mokėjimo nuolaidos datos.

Kekvieno lauko poveikis redaguojamai operacijai skirtingas.

- **Pagrindinės datos koregavimas:** Terminas ir nuolaidų datos pakeičiamos taip, lyg pagrindinė data būtų dokumento data.
- **Termino koregavimas:** Keičiamas tik terminas.
- **Nuolaidų datų koregavimas:** Keičiamos tik nuolaidų datos.
- **Mokėjimo sąlygų koregavimas:** Terminas keičiamas atsižvelgiant į pagrindinę datą ir mokėjimo sąlygas.
- **Mokėjimo nuolaidos sąlygų koregavimas:** Mokėjimo nuolaidos keičiamos atsižvelgiant į pagrindinę datą ir mokėjimo nuolaidos sąlygas.

Baigę redaguoti mokėjimo parametrus, pasirinkite **Uždaryti** ir įrašykite pakeitimus.

