---
title: ES įrašų sertifikatai
description: Šiame straipsnyje pateikiama informacijos apie įvežimo į Europos Sąjungą (ES) sertifikatus.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00b9e80a931c57722a92c3432f9c1006082b1bfbdd844d72c4d5962e106925dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779796"
---
# <a name="eu-entry-certificates"></a>Įvežimo į ES sertifikatai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacijos apie įvežimo į Europos Sąjungą (ES) sertifikatus.

Galite atlikti toliau nurodytas užduotis, susijusias su Europos Sąjungos (ES) įrašo sertifikatu.

-   Kurti ir išduoti ES įrašo sertifikatą kartu su važtaraščiu arba kliento SF, susijusia su prekių tiekimu arba paslaugų teikimu ES šalyse / regionuose.
-   Gauti ES įrašo sertifikatą, kurį pasirašė ES klientas.
-   Nusiųsti pasirašytą ES įrašo sertifikatą, gautą iš kliento arba trečiosios šalies, atsakingos už prekių pristatymą klientui.
-   Susieti nusiųstą ES įrašo sertifikatą su kliento SF.
-   Atnaujinti nusiųsto ES įrašo sertifikato būseną.

## <a name="prerequisites"></a>Būtinieji komponentai
Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.

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
<td>Šalis/regionas</td>
<td>Pagrindinis juridinio subjekto adresas turi būti ES valstybėje narėje.</td>
</tr>
<tr class="even">
<td>Susijusios nustatymo užduotys</td>
<td><ul>
<li><strong>Gautinų sumų parametrų</strong> puslapyje pasirinkite parinktis <strong>Įgalinti įrašų sertifikatų valdymą</strong> ir <strong>Įgalinti įrašų sertifikatų išdavimą</strong>.</li>
<li><strong>Klientų</strong> puslapyje, <strong>SF ir pristatymo</strong> „FastTab‟ pasirinkite parinktį <strong>Įrašo sertifikatas būtinas</strong> , kad nurodytumėte, jog klientui būtinas ES įrašo sertifikatas. Pasirinkite parinktį <strong>Išduoti įrašo sertifikatą</strong>, kad klientui išduotumėte juridinio subjekto ES įrašo sertifikatą.</li>
<li><strong>Gautinų sumų parametrų</strong> puslapyje pasirinkite <strong>Įrašo sertifikato</strong> nuorodos numeracijos kodą.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Susijusios operacijos</td>
<td><ul>
<li>Kurkite kliento kodą.</li>
<li>Sukurkite pardavimo užsakymą.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>ES įrašo sertifikato kūrimas, registravimas ir įkėlimas
Galite sukurti ES įrašo sertifikatą automatiškai arba rankiniu būdu. ES įrašo sertifikatas sukuriamas ir užregistruojamas automatiškai, kai užregistruojate važtaraštį arba SF, skirtą klientui, naudodami puslapį **Važtaraščio registravimas** arba **SF registravimas**. Norėdami kliento SF ES įrašo sertifikatą kurti arba perspausdinti neautomatiškai, naudokite puslapį **SF žurnalas**. Be to, galite naudoti **Įrašų sertifikatų žurnalo** puslapį, kad įvestumėte informaciją apie trečiosios šalies išduotą ES įrašo sertifikatą.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>ES įrašo sertifikato kūrimas automatiškai arba rankiniu būdu

Automatiškai sukurti ES įrašo sertifikatą galite naudodami važtaraštį **Visų pardavimo užsakymų** puslapyje arba naudodami SF  **Pardavimo užsakymo** puslapyje. Norėdami ES įrašo sertifikatą sukurti rankiniu būdu, galite naudoti SF **SF žurnalo** puslapyje. Tačiau prieš rankiniu būdu kurdami ES įrašo sertifikatą, turite pakeisti SF sertifikato būseną.

### <a name="registering-an-eu-entry-certificate"></a>ES įrašo sertifikato registravimas

Jei reikalingas registravimas, galite naudoti **Įrašų sertifikatų žurnalo** puslapį, kad registruotumėte trečiosios šalies išduotą ES įrašo sertifikatą.

### <a name="uploading-a-received-eu-entry-certificate"></a>Gauto ES įrašo sertifikato įkėlimas

Naudodami puslapį **Priedai** galite įkelti gautą ES įrašo sertifikatą, kurį pasirašė ES klientas. Įkėlę sertifikatą, jį galite susieti su SF kaip įrodymą, kad prekės buvo pristatytos. Šio įrodymo reikia, jei turite išduoti SF, kurioje nėra pridėtinės vertės mokesčio (PVM), ir jis taip pat naudojamas atliekant auditą.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Neprivaloma: sertifikato būsenos ir SF spausdinimo būsenos naujinimas

Atnaujinti įrašo sertifikato būseną ir kliento SF spausdinimo būseną galite naudodami **SF žurnalo** puslapį.

## <a name="technical-information-for-system-administrators"></a>Techninė informacija sistemos administratoriams
Jei neturite prieigos prie puslapių, kurie naudojami užduočiai atlikti, kreipkitės į sistemos administratorių ir pateikite informaciją, kuri yra rodoma toliau pateiktoje lentelėje.

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
<td>Saugos vaidmenys ir pareigos</td>
<td>Norėdami nustatyti ir sukurti ES įrašų sertifikatus, skirtus prekėms arba paslaugoms, jums turi būti priskirtas saugos vaidmuo, kuris paprastai priklauso šioms pareigybėms:
<ul>
<li><strong>Gautinų sumų klerkas</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Klientų aptarnavimo atstovas</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Pardavimo klerkas</strong> (TradeSalesClerk)</li>
<li><strong>Siuntimo klerkas</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]