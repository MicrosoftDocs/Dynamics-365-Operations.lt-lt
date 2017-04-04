---
title: "SF išdavimo data"
description: "Šiame straipsnyje paaiškinama, kaip nustatyti parametrus ir apskaičiuoti klientų SF ir tiekėjų SF išdavimo terminus Europos Sąjungoje (ES)."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10923
ms.assetid: 64ea3343-df94-4a52-b839-6328c8a282bd
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 6121be0dd02659e4e8466b0c1381678be64fefc2
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-issue-deadline"></a>SF išdavimo data

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
| Susijusios nustatymo užduotys | Puslapyje **Datų intervalai** nustatykite datos intervalą, naudojamą SF išdavimo datai apskaičiuoti. (Spustelėkite **bendrosios knygos**&gt;**DK nustatymas**&gt;**datos intervalus**.) Dėl į **užsienio prekybos parametrai** puslapyje, nustatyti užsienio prekybos ypatybes įvairių šalių/regionų. (Spustelėkite **mokesčių**&gt;**parametrai**&gt;**užsienio prekybos**&gt;**užsienio prekybos parametrai**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>SF išdavimo datos skaičiavimo taisyklė
Naudokite puslapį **Nustatyti SF išdavimo datos skaičiavimą**, kad nustatytumėte SF išdavimo datos skaičiavimo taisyklę priskirdami datos intervalo kodą šalies / regiono tipui.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Klientų SF ir kredito pažymų datos valdiklio parametrai
Galite nustatyti datos valdiklio parametrus užtikrindami, kad kliento operacijų klientų SF ir kredito pažymos sugeneruojamos per nurodytą laikotarpį nuo pristatymo datos. Šiuos parametrus galite rasti puslapio **Gautinų sumų parametrai** srityje **SF datos valdymas**.

## <a name="example"></a>Pavyzdys
Norėdami nustatyti "Microsoft Dynamics 365" operacijų apskaičiuoti sąskaitos-faktūros išdavimo terminai siuntoms ES viduje penkioliktą dieną mėnesio, einančio po tiekimo yra pristatomi, sukurti datos intervalo kodą ir skaičiavimo taisyklę, kuri turi šiuos parametrus.

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

-   **Pardavimo užsakymai** – kai sukuriate pardavimo užsakymą ir užregistruojate važtaraštį, važtaraštyje apskaičiuojamas ir atnaujinamas SF išdavimo data. Terminas skaičiuojamas pagal datų intervalą, kuris yra susietas su šalies/regiono, kuris yra nurodytas pristatymo adresą iš pardavimo užsakymo. Užregistravus važtaraštį, galite patikrinti sąskaitos-faktūros išdavimo termino datą į **SF išdavimo terminas** lauko į **važtaraščio žurnalą** puslapis. (Spustelėkite **pardavimo ir rinkodaros**&gt;**pardavimų užsakymą**&gt;**užsakymo pristatymas**&gt;**važtaraščio**.) Galite peržiūrėti visus važtaraščius, nėra SF ir sąskaitos-faktūros išdavimo terminai, dėl to **važtaraščių neišrašyta** puslapis. (Spustelėkite **pardavimo ir rinkodaros**&gt;**pardavimų užsakymą**&gt;**užsakymo pristatymas**&gt;**važtaraščių neišrašyta**.)
-   **Pirkimo užsakymai** – kai sukuriate pirkimo užsakymą ir užregistruojate produkto gavimo kvitą, produkto gavimo kvite apskaičiuojamas ir atnaujinamas SF išdavimo data. Terminas apskaičiuojamas pagal datos intervalą, susietą su šalimi / regionu, kuris nurodytas tiekėjo pagrindiniame adrese. Užregistravę produkto gavimo kvitą, galite patikrinti SF išdavimo terminą lauke **SF išdavimo terminas** puslapyje **Produkto gavimo kvitų žurnalas**. (Spustelėkite **pirkimo ir apsirūpinimo**&gt;**pirkimo užsakymų**&gt;**preparatų**&gt;**produkto gavimo**.) Galite peržiūrėti visų važtaraščių sugretinimą, nėra SF ir sąskaitos-faktūros išdavimo terminai, dėl to **važtaraščiai neišrašyta** puslapis. (Spustelėkite **pirkimo ir apsirūpinimo**&gt;**pirkimo užsakymų**&gt;**preparatų**&gt;**važtaraščiai neišrašyta**.)

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
<td>Configuration Keys</td>
<td>Spustelėkite <strong>sistemos administravimo</strong>&gt;<strong>parametrai</strong>&gt;<strong>licencijavimo</strong>&gt;<strong>licencijos konfigūravimo</strong>. Spustelėkite konfigūracijos raktą <strong>Didžioji knyga</strong>.</td>
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




