---
title: SF išdavimo data
description: Šiame straipsnyje paaiškinama, kaip nustatyti parametrus ir apskaičiuoti klientų SF ir tiekėjų SF išdavimo terminus Europos Sąjungoje (ES).
author: AdamTrukawka
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 10923
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
ms.openlocfilehash: 73838bfa4148002ef00013189cf08236ebc0c379
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337372"
---
# <a name="invoice-issue-deadline"></a>SF išdavimo data

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti parametrus ir apskaičiuoti klientų SF ir tiekėjų SF išdavimo terminus Europos Sąjungoje (ES).

Europos Sąjungos (ES) Direktyva 45/2010 ir kitos direktyvos reikalauja, kad už siuntas ES viduje (ES vidaus siuntos) sąskaitos faktūros turi būti išrašomos penkioliktą arba ankstesnę mėnesio dieną po pristatymo. Tuo pačiu metu kiekviena ES šalis gali turėti skirtingus SF išdavimo datas vidaus pristatymams. SF išdavimo datos funkcija leidžia suderinti datų intervalą pagal šalies / regiono tipą. Tada visų siuntų iš tam tikro tipo šalies / regiono SF išdavimo data apskaičiuojamas naudojant taisykles, nustatančias nurodytą datos intervalą. Be to, galite gauti visus važtaraščius su konkrečiu SF išdavimo data, filtruoti pagal SF išdavimo datą periodiškai išrašant SF ir valdyti pardavimo SF išdavimo datą registruojant SF. Galite nustatyti datos intervalo kodą, o tada nustatyti SF išdavimo datos skaičiavimo taisyklę priskirdami datos intervalo kodą šalies / regiono tipui. Skaičiavimo taisyklė naudojama toliau išvardytų operacijų sąskaitų faktūrų išdavimo datai apskaičiuoti.

-   ES vidaus siuntos
-   Vidaus siuntos ES valstybėje narėje

Taip pat galite nustatyti datos valdiklius užtikrindami, kad kliento operacijų klientų SF ir kredito pažymos sugeneruojamos per nurodytą laikotarpį nuo pristatymo datos.

## <a name="prerequisites"></a>Būtinieji komponentai
Toliau pateikiamoje lentelėje nurodytos sąlygos, kurias reikia išpildyti prieš naudojant SF išdavimo datos funkciją.

| Kategorija            | Būtinoji sąlyga                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Šalis/regionas      | Pagrindinis juridinio subjekto adresas turi būti ES valstybėje narėje.                                                                                                                                                                                                                                                                                                                    |
| Susijusios nustatymo užduotys | Puslapyje **Datų intervalai** nustatykite datos intervalą, naudojamą SF išdavimo datai apskaičiuoti. (Spustelėkite **Didžioji knyga** &gt; **DK sąranka** &gt; **Datų intervalai**.) Puslapyje **Užsienio prekybos parametrai** nustatykite įvairių šalių / regionų užsienio prekybos ypatybes. (Spustelėkite **Mokestis** &gt; **Sąranka** &gt; **Užsienio prekyba** &gt; **Užsienio prekybos parametrai**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>SF išdavimo datos skaičiavimo taisyklė
Naudokite puslapį **Nustatyti SF išdavimo datos skaičiavimą**, kad nustatytumėte SF išdavimo datos skaičiavimo taisyklę priskirdami datos intervalo kodą šalies / regiono tipui.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Klientų SF ir kredito pažymų datos valdiklio parametrai
Galite nustatyti datos valdiklio parametrus užtikrindami, kad kliento operacijų klientų SF ir kredito pažymos sugeneruojamos per nurodytą laikotarpį nuo pristatymo datos. Šiuos parametrus galite rasti puslapio **Gautinų sumų parametrai** srityje **SF datos valdymas**.

## <a name="example"></a>Pavyzdys
Norėdami, kad kaip ES vidaus siuntų SF išdavimo datą būtų skaičiuojama penkiolikta kito mėnesio diena po pristatymo, sukurkite datos intervalo kodą ir skaičiavimo taisyklę, kurie turėtų tokius parametrus.

### <a name="date-interval-code"></a>Datos intervalo kodas

| Laukas                                                           | Vertė                           |
|-----------------------------------------------------------------|---------------------------------|
| Datos intervalo kodas                                              | 15 NM                           |
| Prekės/Paslaugos pavadinimas                                                     | Penkiolikta kito mėnesio diena |
| Prieš (laukų grupėįe **Iki datos**)                         | Mėnuo                           |
| Pradžia / pabaiga (laukų grupėįe **Iki datos**)                      | Pabaigti                             |
| + / - (laukų grupėįe **Iki datos**)                            | 15                              |
| Dienos, mėnesiai, metai arba laikotarpiai (laukų grupėje **Iki datos**) | Dienos                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>SF išdavimo datos skaičiavimo taisyklė

| Laukas               | Vertė                                                     |
|---------------------|-----------------------------------------------------------|
| Šalies / regiono tipas | **ES**                                                    |
| Pradžios data          | Įveskite datą, kada įsigalioja dabartinės nustatymo eilutės. |
| Datos intervalo kodas  | **15 NM**                                                 |

## <a name="next-steps"></a>Kiti veiksmai
Nustatę parametrus, kad būtų skaičiuojamos SF išdavimo terminų datos, galite sukurti ir registruoti toliau nurodytas operacijas, kad būtų automatiškai apskaičiuoti ir atnaujinti SF išdavimo terminai:

-   **Pardavimo užsakymai** – kai sukuriate pardavimo užsakymą ir užregistruojate važtaraštį, važtaraštyje apskaičiuojamas ir atnaujinamas SF išdavimo data. Terminas apskaičiuojamas pagal datos intervalą, susietą su šalimi / regionu, kuris nurodytas pardavimo užsakymo pristatymo adrese. Užregistravę važtaraštį galite patikrinti SF išdavimo terminą lauke **SF išdavimo terminas** puslapyje **Važtaraščių žurnalas**. (Spustelėkite **Pardavimas ir rinkodara** &gt; **Pardavimo užsakymas** &gt; **Užsakymo siuntimas** &gt; **Važtaraštis**.) Visus važtaraščius, kurių SF neišrašyta, ir jų SF išdavimo terminus galite peržiūrėti puslapyje **Važtaraščiai, kuriems išrašyta SF**. (Spustelėkite **Pardavimas ir rinkodara** &gt; **Pardavimo užsakymas** &gt; **Užsakymo siuntimas** &gt; **Važtaraščiai, kuriems neišrašyta SF**.)
-   **Pirkimo užsakymai** – kai sukuriate pirkimo užsakymą ir užregistruojate produkto gavimo kvitą, produkto gavimo kvite apskaičiuojamas ir atnaujinamas SF išdavimo data. Terminas apskaičiuojamas pagal datos intervalą, susietą su šalimi / regionu, kuris nurodytas tiekėjo pagrindiniame adrese. Užregistravę produkto gavimo kvitą, galite patikrinti SF išdavimo terminą lauke **SF išdavimo terminas** puslapyje **Produkto gavimo kvitų žurnalas**. (Spustelėkite **Pirkimas ir tiekėjų parinkimas** &gt; **Pirkimo užsakymai** &gt; **Produktų gavimas** &gt; **Produkto gavimo kvitas**.) Visus produktų gavimo kvitus, kurių SF neišrašyta, ir jų SF išdavimo terminus galite peržiūrėti puslapyje **Važtaraščiai, kuriems išrašyta SF**. (Spustelėkite **Pirkimas ir tiekėjų parinkimas** &gt; **Pirkimo užsakymai** &gt; **Produktų gavimas** &gt; **Produktų gavimo kvitai, kuriems neišrašyta SF**.)

## <a name="technical-information-for-system-administrators"></a>Techninė informacija sistemos administratoriams
Jei neturite prieigos prie puslapių, kurie naudojami šiame straipsnyje minimoms užduotims atlikti, kreipkitės į sistemos administratorių ir pateikite informaciją, kuri yra rodoma toliau pateiktoje lentelėje.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorija</th>
<th>Būtinoji sąlyga</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Konfigūracijos raktai</td>
<td>Spustelėkite <strong>Sistemos administravimas</strong> &gt; <strong>Nustatymas</strong> &gt; <strong>Licencijavimas</strong> &gt; <strong>Licencijos konfigūracija</strong>. Spustelėkite konfigūracijos raktą <strong>Didžioji knyga</strong>.</td>
</tr>
<tr class="even">
<td>Saugos vaidmenys ir pareigos</td>
<td>Norėdami atlikti šią užduotį, turite būti saugos vaidmens, apimančio toliau nurodytas pareigas, narys.
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (įgalinti SF ir grynųjų pinigų procesą)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (įgalinti SF ir mokėjimo procesą)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Saugos vaidmenys ir teisės</td>
<td>Norėdami atlikti šią užduotį, turite būti saugos vaidmens, apimančio toliau nurodytas teises, narys.
<ul>
<li><strong>CustPackingSlipJournalView</strong> (peržiūrėti pardavimo važtaraščius)</li>
<li><strong>VendPackingSlipJournalView</strong> (peržiūrėti produkto gavimo žurnalą iš pirkimo užsakymo)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (skaičiuoti SF išdavimo terminus)</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
