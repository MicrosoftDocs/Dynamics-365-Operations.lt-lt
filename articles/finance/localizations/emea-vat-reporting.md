---
title: PVM ataskaitos Europoje
description: Šiame straipsnyje pateikiama bendra informacija apie pridėtinės vertės mokesčio (PVM) išrašo kai kurioms Europos šalims nustatymą ir generavimo.
author: mrolecki
ms.date: 03/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 266844
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
ms.openlocfilehash: 54be8844fadf744cc5527001737ab470fcec46d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283418"
---
# <a name="vat-reporting-for-europe"></a>PVM ataskaitos Europoje

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama bendra informacija apie pridėtinės vertės mokesčio (PVM) išrašo kai kurioms Europos šalims nustatymą ir generavimo.

Šiame straipsnyje pateikiamas bendras PVM išrašo nustatymo ir generavimo būdas. Šį metodą gali bendrai naudoti vartotojai, kurių juridiniai subjektai yra toliau nurodytose šalyse / regionuose.

-   Austrija
-   Belgija
-   Čekijos Respublika
-   Estija
-   Suomija
-   Vokietija
-   Latvija
-   Lietuva
-   Nyderlandai
-   Švedija

> [!IMPORTANT]
> Šiame straipsnyje aprašomos Priemonės, skirti Austrijai, Čekijos Respublikai, Vokietijai, Nyderlandaii ir Švedijai, yra pasenusios. Daugiau informacijos rasite Pašalintos [ir pasenusios funkcijos](../get-started/removed-deprecated-features-finance.md).
> Norėdami daugiau sužinoti apie naują PVM deklaracijų dizainą atitinkamose šalyse, naudokite šioje lentelėje pateikiamus saitus.
> 
>
> | Šalis        | Papildoma informacija                                                          |
> |----------------|---------------------------------------------------------------------------------|
> | Austrija        | [PVM deklaracija (Austrija)](emea-aut-vat-declaration-austria.md)       |                                                                           
> | Čekijos Respublika | [PVM deklaracija (Čekijos Respublika)](emea-cze-vat-declaration-tax-declaration-model.md) |
> | Danija        | [PVM deklaracija (Danija)](emea-dnk-vat-declaration-denmark.md)         |
> | Prancūzija         | [PVM deklaracija (Prancūzija)](emea-fra-vat-declaration-preview-france.md)       |
> | Vokietija        | [PVM deklaracija (Vokietija)](emea-deu-vat-declaration-germany.md)           |
> | Nyderlandai    | [PVM deklaracija (Nyderlandai)](emea-nl-vat-declaration-netherlands.md)    |
> | Norvegija         | [PVM grąžinimas su tiesioginiu pateikimu „Altinn“](emea-nor-vat-return.md) |
> | Ispanija          | [PVM deklaracija (Ispanija)](emea-esp-vat-declaration-spain.md)              |
> | Švedija         | [PVM deklaracija (Švedija)](emea-swe-vat-declaration-sweden.md)          |
> | Šveicarija    | [PVM deklaracija (Šveicarija)](emea-che-vat-declaration-switzerland.md) |
> | Jk             | [Pasirengimas integruoti į MRD PVM](emea-gbr-mtd-vat-integration.md) |

## <a name="vat-statement-overview"></a>PVM išrašo apžvalga
PVM išrašas pagrįstas PVM operacijų sumomis. PVM išrašo generavimo procesas yra PVM apmokėjimo proceso, kuris vykdomas naudojant funkciją Sudengti ir užregistruoti PVM, dalis. Ši funkcija apskaičiuoja nurodyto laikotarpio PVM. Sudengimo skaičiavimas apima mokesčio operacijos pasirinkto sudengimo laikotarpio užregistruotą PVM. PVM išrašo duomenų skaičiavimo procesas pagrįstas ryšiu tarp PVM kodų ir PVM ataskaitų kodų, kai PVM ataskaitų kodai atitinka PVM išrašų langelius (arba XML žymes). Reikia nustatyti kiekvieno PVM kodo kiekvieno operacijos tipo PVM ataskaitų kodus, pvz., kaip apmokestinamą pardavimą, apmokestinamus pirkimus, apmokestinamą importą. Šių tipų operacijos aprašomos PVM kodų skyriuje, skirtame PVM ataskaitoms, vėliau šiame straipsnyje.

Reikia nustatyti kiekvieno PVM ataskaitų kodo konkretų ataskaitos maketą. Tuo pat metu PVM kodai yra susiejami su konkrečiu PVM rinkėju per PVM sudengimo laikotarpius. Reikia nustatyti kiekvieno PVM rinkėjo ataskaitos maketą. Todėl PVM kodo ataskaitos sąrankoje galima pasirinkti tik PVM ataskaitų kodus su tuo pačiu ataskaitos maketu, kuris nustatytas ir priskirtas PVM rinkėjui PVM kodo PVM sudengimo laikotarpiuose. PVM operacija, sugeneruota užregistravus užsakymą arba žurnalą, apima PVM kodą, PVM šaltinį, PVM kryptį ir operacijos sumas (mokesčio bazinę sumą ir mokesčio sumą apskaitos valiuta, PVM valiuta ir operacijos valiuta). Atsižvelgiant į mokesčio operacijos atributų derinį, operacijos sumos sudaro bendras PVM kodų nurodytų PVM ataskaitų kodų sumas. Tolesnėje iliustracijoje pavaizduotas duomenų ryšys.

![diagrama.](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>PVM išrašo sąranka
Norėdami generuoti PVM išrašą, turite atlikti tolesnius veiksmus.

### <a name="sales-tax-authorities-for-vat-reporting"></a>PVM rinkėjų nustatymas PVM ataskaitoms teikti

Prieš nustatydami PVM ataskaitų kodus, turite pasirinkti tinkamą PVM rinkėjo ataskaitos maketą. Puslapio **PVM rinkėjai** dalyje **Bendra** pasirinkite **Ataskaitos maketas**. Šis maketas bus naudojamas nustatant PVM ataskaitų kodus.

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a>PVM ataskaitų kodai

PVM ataskaitų kodai yra langelių kodai PVM išraše arba žymių pavadinimai XML formatu. Šie kodai naudojami ataskaitos sumoms sujungti ir paruošti. Kai konfigūruojate PVM išrašo elektroninių ataskaitų formatą, bus naudojami galutinių sumų pavadinimai. PVM ataskaitų kodus galite kurti ir tvarkyti puslapyje **PVM ataskaitų kodai**. Kiekvienam kodui turite priskirti ataskaitos maketą. Sukūrę PVM ataskaitų kodus, galite kodus pasirinkti puslapio **PVM kodai** dalyje **Ataskaitų sąranka**. <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>PVM kodai, skirti PVM ataskaitos teikti

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> PVM operacijų bazines sumas ir mokesčių sumas galima sujungti PVM išrašo ataskaitų koduose (XML žymės arba deklaracijos langeliai). Tai galima nustatyti puslapyje <strong>PVM kodai</strong> susiejant PVM kodų skirtingų operacijų tipų PVM ataskaitų kodus. Toliau pateikiamoje lentelėje aprašomi PVM kodų ataskaitų sąrankos operacijų tipai. Skaičiuojant įtraukiamos visų šaltinių tipų, išskyrus PVM, operacijos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Operacijos tipas</strong></td>
<td><strong>Operacijų ir sumų, kurios bus apskaičiuotos, aprašas operacijos tipe</strong></td>
</tr>
<tr class="even">
<td><strong>Apmokestinamas pardavimas</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį/</li>
<li>Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Neapmokestinamas pardavimas</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Mokėtinas PVM</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Apmokestinamo pardavimo kredito pažyma</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Neapmokestinamo pardavimo kredito pažyma</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>PVM pardavimo kredito pažymoje</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Apmokestinami pirkimai</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Neapmokestinami pirkimai</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Gautinas PVM</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Apmokestinama pirkimo kredito pažyma</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>PVM pirkimo kredito pažyma</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>PVM pirkimo kredito pažymoje</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Apmokestinamas importas</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong></li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Korespondentinis apmokėjimas už importą</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Apmokestinama importo kredito pažyma</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
e<li><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Korespondentinio apmokėjimo už importą kredito pažyma</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li>Mokesčio kryptis yra <strong>Naudojimo mokestis</strong>.</li>
d<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Naudojimo mokestis</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Koresp. naudojimo mokestis</strong></td>
<td>Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> atšaukta suma.
<ul>
<li>Operacijos data patenka į pasirinktą laikotarpį.</li>
<li><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</li>
<li>Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Ankstesnėje lentelėje laikoma, kad toliau pateikti kriterijai yra patenkinami. 
> -   Mokesčių bazinė suma yra operacijos suma iš lauko **Pradinė suma apskaitos valiuta**.
> -   Mokesčių suma yra perėjimo suma iš lauko **Faktinė PVM suma apskaitos valiuta**.

### <a name="configure-the-er-model-and-format-for-the-report"></a>ER modelio ir ataskaitos formato konfigūravimas

Galite naudoti elektronines ataskaitas (ER), kad sukonfigūruotumėte išrašus ir ataskaitas bei eksportuotumėte duomenis skirtingais elektroniniais formatais nekeisdami X++ kodo. Papildoma informacija:

-   [Elektroninių ataskaitų apžvalga](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
-   [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [Lokalizavimo reikalavimai – GER konfigūracijos kūrimas](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a>PVM išrašų konkrečiai šaliai būdingi ištekliai
Kiekvienos šalies PVM išrašas turi atitikti šalies teisės reikalavimus. Toliau pateiktoje lentelėje nurodytoms šalims priskiriami PVM išrašų iš anksto nustatyti bendrieji modeliai ir formatai.


| Šalis        | Papildoma informacija                                                          |
|----------------|---------------------------------------------------------------------------------|
| Austrija        | [PVM išrašo informacija, skirta Austrijai](emea-aut-vat-statement-details.md)         |
| Belgija        |                                                                                 |
| Čekijos Respublika | [Čekijos PVM išrašas](emea-cze-vat-statement-details.md)   |
| Estija        | [PVM išrašo informacija, skirta Estijai](emea-est-vat-statement-details.md) |
| Suomija        | [PVM ataskaita (Suomija)](emea-fin-sales-tax-payment-report-finland.md)          |
| Vokietija        | [PVM deklaracija (Vokietija)](emea-de-vat-declaration.md)                       |
| Italija          | [Išsami informacija apie Italijos PVM išrašus](emea-ita-vat-statements-details.md)            |
| Latvija         | [PVM išrašo informacija, skirta Latvijai](emea-lva-vat-statement-details.md)           |
| Lietuva      | [PVM išrašo informacija, skirta Lietuvai](emea-ltu-vat-statement-details.md)         |
| Nyderlandai    | [PVM deklaracija (Nyderlandai)](emea-nl-vat-declaration.md)           |
| Švedija         | [PVM ataskaita (Švedija)](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
