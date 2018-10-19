---
title: "Tiekėjo operacijų sąrašo puslapis"
description: "Šioje temoje pateikiama informacija apie puslapį Tiekėjo operacijų sąrašas, skirtas „Microsoft Dynamics 365 for Finance and Operations“"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 53740f6ed0d463de5ba962f1ba15b208634a0739
ms.contentlocale: lt-lt
ms.lasthandoff: 10/01/2018

---

# <a name="vendor-transactions-list-page"></a>Tiekėjo operacijų sąrašo puslapis

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Peržiūrėti sudengimus

Veiksmų srities mygtukas **Sudengimų peržiūra** suteikia greitą prieigą prie sudengimų retrospektyvos ir papildomos informacijos apie visą sudengimo operaciją. Taip pat galite peržiūrėti papildomas operacijas, susijusias su pasirinkta operacija, nes jos buvo įtrauktos į tą patį sudengimą arba nes jos yra mokėjimai, sukurti tame pačiame mokėjimo žurnale.

1. Pasirinkite **Mokėtinos sumos \> Visi tiekėjai**.
2. Pasirinkite operacijų turintį tiekėją, tada veiksmų srities skirtuke **Tiekėjas** pasirinkite **Operacijos**.
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

Į tiekėjo puslapį įtrauktas mygtukas **Visuotinės operacijos**. Naudodamiesi šiuo mygtuku galite peržiūrėti visas tiekėjo operacijas visuose juridiniuose subjektuose. Sąrašo puslapyje **Tiekėjo operacijos** rodomos tik tų juridinių subjektų operacijos, prie kurių vartotojas turi prieigą (priklausomai nuo jo / jos saugos parametrų).

Sąrašo puslapyje rodomos visos tą patį šalies ID kaip ir tiekėjas, nuo kurio pradėjote, turinčių tiekėjų operacijos. Pavyzdžiui, jei tiekėjas US-001 viename juridiniame subjekte turi tą patį šalies ID kaip tiekėjas DE-001 kitame juridiniame subjekte, rodomos visos abiejų tiekėjų ID operacijos.

Sąrašo puslapio **Tiekėjo operacijos** meniu skiriasi, priklausomai nuo operacijos juridinio subjekto. Pavyzdžiui, jei funkcija gali naudotis tik Šveicarijos juridiniai subjektai, tos funkcijos meniu parinktys rodomos tik pasirinkus Šveicarijos operaciją.

Norėdami pasinaudoti funkcija, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Mokėtinos sumos** \> **Visi tiekėjai**.
2. Pasirinkite tiekėją, tada veiksmų srities skirtuko **Tiekėjas** grupėje **Operacijos** pasirinkite **Visuotinės operacijos**.

## <a name="more-transaction-filters"></a>Daugiau operacijų filtrų

Atidarytų operacijų rodymo filtras pakeistas nauju filtru, kuriuo naudodamiesi galite peržiūrėti daugiau operacijų derinių. Galimos toliau nurodytos lauko **Rodyti** parinktys.

- **Visos** – Rodyti visas pasirinktų tiekėjų operacijas (atidarytas ir uždarytas).
- **Uždarytos** – Rodyti tik visiškai sudengtas ir uždarytas operacijas.
- **Atidarytos** – Rodyti tik tas operacijas, kurios dar ne visiškai sudengtos.
- **Atidarytos nuo datos** – Rodyti tik tas operacijas, kurios dar ne visiškai sudengtos nuo jūsų nurodytos datos. Pasirinkę šią parinktį galite keisti šalia filtro rodomą datą. Sąraše rodomos operacijos, prie kurių po jūsų nurodytos datos rodoma vertė **Paskutinio sudengimo data**, net jeigu tos operacijos visiškai sudengtos. Tačiau balansas reiškia balansus nuo dabartinės datos, ne nuo pasirinktos datos.

Taip pat pridėtas filtras, kuriuo naudodamiesi galite slėpti valiutos konvertavimo operacijas. Tiesiog pažymėkite žymės langelį **Slėpti valiutos perkainojimus**.

## <a name="more-easily-modify-due-dates-and-discount-dates"></a>Lengviau modifikuoti terminus ir nuolaidų datas

Galite atnaujinti atidarytų klientų operacijų terminus ir nuolaidų datas. Išleidus 8.1 versiją, pagerinta patirtis. Dabar sąrašo puslapyje **Tiekėjo operacijos** galite pridėti terminus. Sąrašo puslapyje **Tiekėjo operacijos** spustelėję terminą dialogo lange **Atnaujinti terminą ir mokėjimo nuolaidos datas** taip pat galite pakeisti terminus, nuolaidų datas, mokėjimo sąlygas ir mokėjimo nuolaidos sąlygas.

### <a name="activate-the-feature"></a>Funkcijos suaktyvinimas

Norėdami sąrašo puslapyje **Tiekėjo operacijos** naudodamiesi dialogo langu **Atnaujinti terminą ir mokėjimo nuolaidos datas** pridėti terminų ir pakeisti operacijos mokėjimo parametrus, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.
2. Skirtuke **Sudengimai** nustatykite srities **Rodyti terminą ir leisti koreguoti** parinktį **Taip**.
3. Tam, kad būtų galima naudotis šia funkcija, įtraukti nauji tiekėjo operacijų veiksmai. Šie laukai užpildomi atlikus naują operaciją. Jie taip pat užpildomi atidarius dialogo langą **Atnaujinti terminą ir mokėjimo nuolaidos datas**. Nustatę srities **Rodyti terminą ir leisti koreguoti** parinktį **Taip** matysite dialogo langą **Naujinti mokėjimo informaciją**.  Norėdami iškart atnaujinti esamas operacijas, pasirinkite **Atnaujinti visas esamas operacijas**. Arba, norėdami užpildyti tik naujų operacijų laukus, pasirinkite **Tęsti be naujinimo**.

Dabar terminas įtrauktas į sąrašo puslapį **Tiekėjo operacijos** ir jūs galite lengviau pakeisti operacijų terminus ir mokėjimo nuolaidų datas.

### <a name="modify-the-payment-settings"></a>Mokėjimo parametrų keitimas

Sąrašo puslapyje **Tiekėjo operacijos** rodomos visos tiekėjo operacijos. Pasirinkus operacijos terminą atidaromas dialogo langas. Šiame dialogo lange rodoma pagrindinė termino data ir nuolaidos skaičiavimai, terminas, mokėjimo sąlygos, mokėjimo nuolaidos sąlygos ir mokėjimo nuolaidos datos.

Kekvieno lauko poveikis redaguojamai operacijai skirtingas.

- **Pagrindinės datos koregavimas:** Terminas ir nuolaidų datos pakeičiamos taip, lyg pagrindinė data būtų dokumento data.
- **Termino koregavimas:** Keičiamas tik terminas
- **Nuolaidų datų koregavimas:** Keičiamos tik nuolaidų datos.
- **Mokėjimo sąlygų koregavimas:** Terminas keičiamas atsižvelgiant į pagrindinę datą ir mokėjimo sąlygas.
- **Mokėjimo nuolaidos sąlygų koregavimas:** Mokėjimo nuolaidos keičiamos atsižvelgiant į pagrindinę datą ir mokėjimo nuolaidos sąlygas.

Baigę redaguoti mokėjimo parametrus, pasirinkite **Uždaryti** ir įrašykite pakeitimus.

