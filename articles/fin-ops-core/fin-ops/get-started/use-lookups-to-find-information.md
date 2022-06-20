---
title: Informacijos ieška naudojant peržvalgas
description: Šiame straipsnyje jūs sužinosite apie peržvalgos funkcijas ir gausite keletą naudingų patarimų, kaip optimaliai naudotis peržvalgomis sistemoje.
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee309330c165dfb0b67f647afc3514d4c827dad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901529"
---
# <a name="find-information-by-using-lookups"></a>Informacijos ieška naudojant peržvalgas

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Daugelyje laukų yra peržvalgos, kurias naudodami galite lengvai surasti tinkamą ar norimą reikšmę. Į peržvalgas buvo įtrauktos kelios patobulintos funkcijos, todėl šiuos valdiklius bus galima dažniau naudoti, o vartotojai dirbs našiau. Šiame straipsnyje jūs sužinosite apie šias naujas peržvalgos funkcijas ir gausite keletą naudingų patarimų, kaip optimaliai naudotis peržvalgomis sistemoje.

## <a name="responsive-lookups"></a>Reaguojančios peržvalgos

Vartotojai, naudodami ankstesnes versijas ir sąveikaudami su peržvalgos valdikliu, turi atlikti akivaizdų veiksmą, kad būtų atidarytas išplečiamasis meniu. Šiose versijose meniu gali būti atidaromas įvedus žvaigždutę (\*) valdiklyje, kad pagal dabartinę valdiklio reikšmę peržvalgoje būtų išfiltruotas turinys, spustelėjus išplečiamąjį mygtuką arba naudojant sparčiuosius klavišus **Alt**+**rodyklė žemyn**. Kad geriau atitiktų dabartines žiniatinklio tendencijas, peržvalgos valdikliai modifikuoti pritaikius toliau nurodytas veikimo ypatybes.

- Nuo šiol peržvalgos išplečiamasis meniu bus automatiškai atidaromas po trumpos pauzės įvedant tekstą, o išplečiamojo meniu turinys bus išfiltruojamas pagal peržvalgos valdiklio reikšmę.

    Atminkite, kad nuo šiol įvedus žvaigždutę (\*) automatiškai nebeatidaromas išplečiamasis meniu.

- Atidarius peržvalgos išplečiamąjį meniu bus atliekami toliau nurodyti veiksmai.

    - Žymiklis išliks peržvalgos valdiklyje (o įvesties vieta nebus perkelta į išplečiamąjį meniu), todėl galėsite toliau modifikuoti valdiklio reikšmę. Tačiau vartotojas naudodamas klavišus **Rodyklė aukštyn** ir **Rodyklė žemyn** ir toliau galės keisti išplečiamojo meniu eilutes, o paspaudęs klavišą „Enter“ galės pasirinkti esamą išplečiamojo meniu eilutę.
    - Išplečiamojo meniu turinys bus koreguojamas modifikavus peržvalgos valdiklio reikšmę.

Pavyzdžiui, panagrinėkime peržvalgos lauką **Miestas**.

Kai įvesties vieta – laukas **Miestas**, galite pradėti ieškoti norimo miesto įvesdami kelias raides, pvz., „col“. Nustojus įvesti tekstą bus automatiškai atidaryta peržvalga, kurioje bus išfiltruoti „col“ prasidedantys miestai.

[![„typeaheadLookupExample”.](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

Šiuo metu žymiklis ir toliau išlieka peržvalgos lauke. Jei toliau įvesite tekstą ir reikšmė bus „colum“, peržvalgos turinys bus automatiškai pakoreguotas pagal naujausią valdiklio reikšmę.

![„updateFilterLookupExample”.](./media/updatefilterlookupexample.png)

Net jei įvesties vieta ir toliau bus peržvalgos valdiklyje, naudodami klavišus **Rodyklė aukštyn** arba **Rodyklė žemyn** galėsite pažymėti norimą pasirinkti eilutę. Jei paspausite klavišą **Enter**, peržvalgoje bus pasirinkta pažymėta eilutė, o valdiklio reikšmė bus atnaujinta.

![„changingSelectionLookup”.](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Ne vien tik ID įvedimas

Vartotojai, įvesdami duomenis, paprastai bando identifikuoti objektą, pvz., klientą ar tiekėją, pagal pavadinimą, o ne objektą nurodantį identifikatorių. Daugelio (bet ne visų) peržvalgų atveju dabar galima įvesti duomenis pagal kontekstą. Vartotojas, naudodamas šią efektyvią duomenų įvedimo funkciją, peržvalgos valdiklyje gali įvesti ID arba atitinkamą pavadinimą.

Pavyzdžiui, panagrinėkime lauką **Kliento sąskaita**, kai kuriamas pardavimo užsakymas. Šiame lauke nurodomas kliento **sąskaitos ID**, tačiau vartotojas, kurdamas pardavimo užsakymą, šiame lauke paprastai įvestų **sąskaitos pavadinimą**, o ne **sąskaitos ID**, pvz., „Forest Wholesales“, o ne „US-003“.

Jei vartotojas peržvalgos valdiklyje pradėjo įvesti **sąskaitos ID**, bus automatiškai atidarytas išplečiamasis meniu (kaip aprašyta ankstesnėje dalyje), o vartotojui bus pateikta toliau pavaizduota peržvalga.

[![Kontekstinė peržvalga įvedus kliento sąskaitos ID.](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Tačiau nuo šiol vartotojas gali įvesti ir **sąskaitos pavadinimo** pradžią. Jei bus aptikta įvesta pradžia, tada vartotojui bus pateikiama toliau pavaizduota peržvalga. Atkreipkite dėmesį, kaip stulpelis **Pavadinimas** perkeliamas ir nustatomas pirmuoju peržvalgos stulpeliu bei kaip peržvalgoje išrikiuojama ir išfiltruojama pagal stulpelį **Pavadinimas**.

[![Kontekstinė peržvalga įvedus kliento pavadinimą.](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Tinklelio stulpelių antraščių naudojimas siekiant tiksliau išfiltruoti ir išrikiuoti

Vartotojas, naudodamas patobulintas ankstesniuose dviejuose skyriuose aprašytas peržvalgos funkcijas ir atlikdamas peržvalgos lauko **ID** arba **Pavadinimas** pradžios iešką, gali žymiai geriau naršyti peržvalgos eilutes. Tačiau esant tam tikroms situacijoms reikia naudoti išplėstines filtravimo (ar rikiavimo) parinktis reikiamai eilutei surasti. Esant šioms situacijoms vartotojas turi naudoti filtravimo ir rikiavimo parinktis peržvalgoje esančiose tinklelio stulpelių antraštėse. Pavyzdžiui, pardavimo užsakymo eilutėje tekstą įvedantis darbuotojas turi surasti reikiamą produktą – „kabelį“. Nėra jokių produktų pavadinimų, prasidedančių „kabelis“, todėl valdiklyje **Prekės numeris** įvedus „kabelis“ nepateikiama jokių rezultatų.

![„emptyitemlookup”.](./media/emptyitemlookup.png)

Vartotojas turi išvalyti peržvalgos valdiklio reikšmę, atidaryti peržvalgos išplečiamąjį meniu ir naudodamas tinklelio stulpelių antraštę išfiltruoti išplečiamojo meniu turinį, kaip nurodyta toliau pateiktoje iliustracijoje. Pelę (ar jutiklinį ekraną) naudojantis vartotojas tiesiog spustelėjęs (ar palietęs) bet kurią stulpelio antraštę gali pasiekti to stulpelio filtravimo ir rikiavimo parinktis. Klaviatūrą naudojantis vartotojas turi tiesiog antrą kartą paspausti **Alt**+**Rodyklė** **žemyn**, kad įvesties vieta būtų išplečiamajame meniu, po to vartotojas naudodamas tabuliavimo klavišą gali pereiti į reikiamą stulpelį, tada paspaudęs **Ctrl**+**G** gali atidaryti tinklelio stulpelio antraštės išplečiamąjį meniu.

[![„gridfilteritemlookup”.](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

Pritaikęs filtrą (žr. toliau pateiktą vaizdą) vartotojas gali įprastai surasti ir pasirinkti eilutę.

![„filtereditemlookup”.](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]