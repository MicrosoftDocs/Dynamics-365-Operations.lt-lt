---
title: Susieti atsargų paketus
description: Šiame straipsnyje pateikiama informacijos apie tai, kaip konsoliduoti du arba kelis atsargų paketus sulietame pakete.
author: pjacobse
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d43733455765bc8b69ce8595c46b00942ddac6b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228592"
---
# <a name="merge-inventory-batches"></a>Susieti atsargų paketus

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacijos apie tai, kaip konsoliduoti du arba kelis atsargų paketus sulietame pakete.

Kai suliejate paketus, skaičiavimai gali padėti optimizuoti sulieto paketo charakteristikas ir atributus. Pasirinkę šaltinio paketus, prieš užregistruodami sulietąjį paketą, jį galite peržiūrėti ir pakeisti. Taip pat paketų suliejimą galite perkelti į atsargų žurnalą patvirtinti. Atsargas tada galima rezervuoti ar registruoti tiesiai iš to atsargų žurnalo. Kai užregistruojate susietą paketą, pakoreguojamos šaltinio paketų ir susieto paketo atsargos.

## <a name="are-there-any-prerequisites"></a>Ar yra kokių nors būtinųjų sąlygų?
Taip, yra keletas dalykų, kuriuos reikia nustatyti prieš naudojant paketų susiejimo įrankius. Būtinosios sąlygos aprašomos pateiktoje lentelėje.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Puslapis</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Žurnalų pavadinimai, atsargos</td>
<td>Turite sukurti tipo KS žurnalo pavadinimą, naudojamą pagal numatytuosius parametrus, kai paketų suliejimus registruojate atsargų žurnaluose. Nebūtina, bet rekomenduojama: galite nurodyti, kad būtų automatiškai rezervuojama, kai paketų suliejimas perkeliamas į atsargų žurnalą. Priešingu atveju yra pavojus, kad turimos atsargos gali būti pakeistos, kai nustatoma paketų suliejimo informacija ir užregistruojamas žurnalas. Norėdami įjungti automatinį žurnalo pavadinimo rezervavimą, lauke <strong><strong>Rezervavimas</strong></strong> pasirinkite <strong>Automatinis</strong>.</td>
</tr>
<tr class="even">
<td>Atsargų ir sandėlio valdymo parametrai</td>
<td>Turite nurodyti atsargų žurnalo numatytąjį žurnalo pavadinimą.</td>
</tr>
<tr class="odd">
<td>Patvirtinti produktai</td>
<td>Toliau pateikti rekomenduojami prekės parametrai.
<ul>
<li>Norėdami automatiškai sugeneruoti sulietų paketų numerius, išleistą produktą turite priskirti paketų numerių grupei. Be to, paketo numerį galite įvesti neautomatiškai, kai kuriate susietą paketą, arba galite pasirinkti esamą paketo numerį. Jei pasirenkate esamą paketo numerį, įsitikinkite, kad pasirinktas paketas nebuvo&#39; įtrauktas į jokias atsargų operacijas.</li>
<li>Jei&#39; naudojate pateikto produkto laikymo trukmės ar galiojimo pabaigos datas, sulieto paketo datos apskaičiuojamos remiantis lauko <strong>Paketo suliejimo datos skaičiavimas</strong> pasirinkimu. Galimos toliau nurodytos pasirinktys:
<ul>
<li><strong>Anksčiausia</strong> – skaičiuojama pagal anksčiausią datą, nurodytą pasirinktam paketo suliejimo šaltinio paketui.</li>
<li><strong>Vėliausia</strong> – skaičiuojama pagal vėliausią datą, nurodytą pasirinktam paketo suliejimo šaltinio paketui.</li>
<li><strong>Rankinis</strong> – neskaičiuojama. Jei data visuose šaltinio paketuose vienoda, ji pasiūloma. Tą datą galima pakeisti. Jei data šaltinio paketuose nesutampa&#39;, ją įvesti galite rankiniu būdu.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Paketo Nr. grupė</td>
<td>Pasirinktinai: jei norite sugeneruoti paketo numerį kurdami susietą paketą, turite pateiktam produktui priskirti paketų numerių grupę. Kitu atveju galite įvesti paketo numerį neautomatiškai.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Kada reikėtų sulieti atsargų paketus?
Toliau pateikti keli scenarijų pavyzdžiai, kada gali būti naudinga sulieti paketus.

-   Vaikščiodamas savo sandėlyje Sammy'is pastebi, kad yra keletas tos pačios prekės paketų su mažais kiekiais. Jis tikisi gauti kelias naujas siuntas ir pastebi, kad gali atlaisvinti grindų vietos susiedamas likusius kiekius į naują paketą.
-   Sammy'is gauna atsargų ir nori susieti naują paketą su jau gautu paketu siekdamas pagerinti esamo paketo atributo reikšmę. Tokiu būdu sukuriate naują paketą.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Ar galima susieti paketus iš kelių vietų ir juridinių subjektų?
Ne, galite susieti tik tos pačios vietos ir sandėlio saugojimo dimensijų paketus, esančius viename juridiniame subjekte. Tačiau galite nurodyti kitą susieto paketo vietą ir padėklo ID.

## <a name="can-i-merge-partial-quantities"></a>Ar galima sulieti dalinius kiekius?
Ne, galima sulieti tik visą paketų kiekį. Paketų suliejimo funkcija skirta naudoti kaip atsargų funkcija, o ne kaip gamybos funkcija.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Ką daryti, jei skiriasi paketų atributų vertės?
Kai pasirenkate šaltinio paketus, kuriuos norite sujungti su sulietu paketu, „Supply Chain Management“ patikrina, ar visi paketai turi charakteristikas arba atributų reikšmes. Kai atributo reikšmė yra tokia pati, ji pasiūloma sulietam paketui. Tą reikšmę galite keisti. Nesutampančios atributų reikšmės susietame pakete paliekamos nenurodytos, jas galite įvesti neautomatiškai. Jei atributo reikšmės paketo atributo tipas yra sveikasis skaičius arba trupmena ir ne visų šaltinio paketų reikšmės vienodos, reikšmė bus apskaičiuota naudojant svertinį vidurkį. Apskaičiuota vertė suapvalinama iki mažesnės arba didesnės vertės. Jei šaltinio paketo reikšmė yra nenurodyta, paketas ir jo kiekis į skaičiavimą neįtraukiami. **Pavyzdys** Šiame pavyzdyje parodytas susieto paketo svertinio vidurkio skaičiavimas. Dviejų šaltinio paketų vertė nenurodyta – paketo atributo tipas yra sveikasis skaičius. Šaltinio paketams priskiriamas nurodytas atributas.

| Atributas | Minimumas | Padidinimas | Maksimumas |
|-----------|---------|-----------|---------|
| Kategorija     | 3       | 3         | 30      |

Šaltinio paketai turi nurodytas atributo **Kategorijos paketas** reikšmes.

| Paketas | Kiekis | Atributas | Atributo vertė |
|-------|----------|-----------|-----------------|
| B1    | 10       | Kategorija     | Tuščias           |
| B2    | 15       | Kategorija     | 15              |
| B3    | 20       | Kategorija     | 20              |
| B4    | 25       | Kategorija     | Tuščias           |
| B5    | 30       | Kategorija     | 25              |

Kai įtraukiate šiuos paketus kaip šaltinio paketus, sulietam paketui priskiriamos nurodytos reikšmės.

| Paketas | Kiekis | Atributas | Atributo vertė |
|-------|----------|-----------|-----------------|
| B6    | 100      | Kategorija     | 21              |

B1 ir B4 paketų reikšmės bei kiekiai neįtraukiami skaičiuojant svertinį vidurkį. Todėl sulieto paketo reikšmė apskaičiuojama nurodytu būdu.

| Vertė | Kiekis (svoris)                              | Santykinis svoris | Santykinis svoris × vertė                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0,230769231     | 3,461538462                                                           |
| 20    | 20                                             | 0,307692308     | 6,153846154                                                           |
| 25    | 30                                             | 0,461538462     | 11,53846154                                                           |
|       | **Iš viso:** 65 – tai yra svorių suma. |                 | **Iš viso**: 21,5384615, suapvalinama iki 21 (artimiausio sveikojo skaičiaus). |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Ką daryti, jei paketų datos skiriasi?
Jei skiriasi paketų datos, kai kurios datos apskaičiuojamos pagal reikšmes, esančias puslapio **Paketų suliejimas** „FastTab‟ skirtuko **Sulietas paketas** grupėje **Paketo datos**. Sistema apskaičiuoja grupės **Paketo datos** laukų reikšmes. Šios reikšmės – tai gamybos data, galiojimo data, pranešimo apie laikymo pabaigą data ir galiojimo pabaigos data. Datos apskaičiuojamos remiantis prekės parametrais, nustatytais puslapio **Išleisto produkto informacija** laukų grupėje **Prekės duomenys**. Reikšmes galite pakeisti arba įvesti rankiniu būdu. Visų kitų datų skaičiavimai nėra atliekami. Toks pat principas taikomas paketų atributų vertėms. Jei visų šaltinio paketų data vienoda, ta data pasiūloma sulietam paketui. Jei visų šaltinio paketų data nevienoda, data sulietame pakete nenurodoma, galite ją įvesti rankiniu būdu.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Ką daryti, jei skiriasi norimų susieti paketų dimensijos?
Produktų dimensijos, sekimo dimensijos ir saugojimo dimensijos tvarkomos toliau nurodytu būdu.

-   **Produktų dimensijos** – visos pasirinktos prekės produktų dimensijos turi būti vienodos. Produktų dimensijų paketų sulieti negalima.
-   **Sekimo dimensijos** – jei nurodyta prekės paketo numerių grupė, naujas paketo numeris sugeneruojamas automatiškai. Jei paketo numerių grupė prekei nepriskirta, galite pasirinkti esamą paketą arba įvesti numerį rankiniu būdu. Serijos numeriai perkeliami iš šaltinio paketo į susieto paketo atsargų žurnalo eilutes.
-   **Saugojimo dimensijos** – vietos ir sandėlio saugojimo dimensijos turi būti vienodos visuose šaltinio paketuose ir sulietame pakete. Tačiau galite nurodyti naują susieto paketo vietos ir padėklo ID.

## <a name="how-does-posting-work"></a>Kaip veikia registravimas?
Registravimas veikia dviem būdais, atsižvelgiant į tai, ar naudojate žurnalų patvirtinimo procesą. Galite naudoti veiksmus **Perkelti į žurnalą** ir **Registruoti paketų suliejimą** norėdami perkelti paketo suliejimą į žurnalą, kur jį galima patikrinti ir užregistruoti, arba galite paketo suliejimą užregistruoti tiesiogiai. Pagrindinis dviejų veiksmų skirtumas yra tas, kad perkeliant į žurnalą paketų suliejimas neregistruojamas. Abiem veiksmais sukuriamas naujas paketas, jei nepasirinktas esamas, atnaujinama visa paketo informacija ir atributų reikšmės bei sukuriamas atsargų žurnalas.

-   **Perkelti į žurnalą** – paketų suliejimo informaciją perkelti į naują atsargų žurnalą. Jei nustatėte automatinį rezervavimą, rezervuojami šaltinio paketų kiekiai. Paketų suliejimo informacijos pakeisti negalima. Norėdami modifikuoti paketų suliejimą, turite panaikinti žurnalą. Žurnalas gali būti naudojamas kaip užduotis, kurią vėliau turi atlikti kitas darbuotojas. Paketo kiekio rezervavimas žurnalo eilutėje yra saugomas. Toks paskirstymas kokybės planuotojui ar sandėlio vadovui leidžia kurti užduotis savo darbuotojams.
-   **Registruoti paketų suliejimą** – paketų suliejimą registruoti tiesiogiai. Šį veiksmą galima atlikti įvykus fiziniam suliejimui.

Galite patvirtinti paketų suliejimo atsargų žurnalą sąrašo puslapyje **Visi paketų suliejimai**. Spustelėkite **Žurnalas** &gt; **Registruoti**. Užregistravus žurnalą, negalima pakeisti sulieto paketo informacijos. Kai perkeliate paketų susiejimą į atsargų žurnalą, informaciją galite pakeisti, tik jei žurnalas panaikinamas.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Kai susieju esamo svorio prekę, kodėl esamo svorio informacijos negaliu matyti atsargų žurnale?
Esamo svorio prekių paketus galite sulieti kaip ir visas kitas prekes. Tačiau esamo svorio informacija nerodoma atsargų žurnale. Prieš perkeliant paketų suliejimą į atsargų žurnalą rekomenduojame patikrinti esamo svorio informaciją.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]