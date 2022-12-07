---
title: Asinchroninės užsakymų sinchronizavimo problemos
description: Šiame straipsnyje aprašomos bendros asinchroninio užsakymo kūrimo klaidos priežastys Microsoft Dynamics 365 Commerce ir pateikiami trikčių diagnostikos veiksmai, padėsiantys sistemos vartotojams ir partneriams suprasti, kas nutiko.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815762"
---
# <a name="asynchronous-order-synchronization-issues"></a>Asinchroninės užsakymų sinchronizavimo problemos

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašomos bendros asinchroninio užsakymo kūrimo klaidos priežastys Microsoft Dynamics 365 Commerce ir pateikiami trikčių diagnostikos veiksmai, padėsiantys sistemos vartotojams ir partneriams suprasti, kas nutiko.

## <a name="symptom"></a>Požymis

Asinchroniniai užsakymai, Dynamics 365 Commerce sukurti iš el. komercijos arba kasos serverio (EKA), nėra atspindėti "Commerce Headquarters".

## <a name="troubleshooting"></a>Trikčių šalinimas

Užsakymo sukurti gali nepavykti būstinėje dėl skirtingų priežasčių, atsižvelgiant į etapą, kurio metu užsakymo kūrimo procesas nepavyko. Toliau pateikiami trikčių šalinimo veiksmai pereis per galimas šaknies priežastis.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Patikrinkite, ar su asinchroninis užsakymu susijusi operacija pasiekė "Headquarters"

Būstinėse eikite į "Retail" ir " **Commerce \> " užklausų ir ataskaitų internetinės \> saugyklos operacijas el. komercijos užsakymams**. Jei turite užsakymo patvirtinimo numerį, filtruokite operacijas įvesdami patvirtinimo numerį kanalo **nuorodos ID lauke** . Jei neturite patvirtinimo numerio, filtruokite operacijas įvesdami kliento sąskaitos numerį.

EKA užsakymuose atidarykite **parduotuvės operacijų** puslapį ir filtruoti įrašus pagal kvito numerį arba kliento sąskaitos numerį. Jei operacija nerastos, **vykdykite P-0001 kanalo** operacijų užduotį, kuri sinchronizuoja operacijas iš kanalų į būstinę.  **Jei P-0001 užduotis** nepavyksta, atidarykite palaikymo bilietą užduočiai atlikti.  **Jei P-0001** užduotis sėkminga, bet operacijos vis dar nerodomas būstinėje, atidarykite palaikymo bilietą, kuriame yra atitinkama informacija.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Patikrinti sinchronizavimo būseną, jei operacija yra būstinėje, bet ji nėra susieta su pardavimo užsakymu

Jei operacija yra būstinėje, bet pardavimo užsakymas nesukurtas, **atidarykite** parduotuvės operacijų interneto puslapį ir pasirinkite sinchronizavimo **būsenos** "FastTab". Jei užsakymų sinchronizavimo **užduotis bandė sinchronizuoti šią operaciją,** laukiančio užsakymo būsenos **lauke turi būti rodoma** būsena Pavyko arba **Nepavyko**  **.** Jei būsena yra **Sėkminga**, šioje operacijoje turi būti pardavimo užsakymo laukas. Jei būsena yra **Nepavyko**, galite peržiūrėti klaidos informaciją lauke **Užsakymo klaidos informacija**, kuris yra sinchronizavimo **būsenos** "FastTab". Jei jokios iš šių būsenų nerodoma, nebuvo bandyta apdoroti operaciją. Šiuo atveju, norėdami vykdyti sinchronizavimo **užduotį**, puslapio viršuje galite pasirinkti Sinchronizuoti užsakymą.

Įsitikinkite, kad **užsakymų** sinchronizavimo užduotis suplanuota vykdyti periodiškai, kad asinchroninės operacijos būtų kuriamos kaip užsakymai pardavimo užsakymuose.

Šiose sekcijose pateikiama informacija apie kai kurias bendras klaidas ir siūlomas pataisas.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Informacijos apie užsakymo klaidą lauke rodomas šis klaidos pranešimas: "Viršyta numeracija"

Numeracija naudojama pardavimo užsakymams pardavimo būstinėje kurti. Jei visi numeracijai leidžiami skaičiai yra per daug pereina, sistema sugeneruoja šį klaidos pranešimą. Numeraciją, naudojamą pardavimo užsakymams kurti, galima rasti gautinų sumų **parametrų numeracijoje \> Pardavimo \> užsakymas**. Norėdami ištaisyti šią klaidą, ištaisykite esamą numeraciją arba pakeiskite ją nauja numeracija.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Informacijos apie užsakymo klaidą laukas rodo šį klaidos pranešimą: "Norint apdoroti kredito kortelės operacijas, turi būti numatytoji mokėjimo paslauga"

Norėdami ištaisyti šią klaidą, patvirtinkite, kad numatytasis mokėjimas nustatytas būstinėje. Jei numatytasis mokėjimas nėra nustatytas, jį reikia nustatyti. Eikite **į gautinų \> sumų mokėjimo \> nustatymo mokėjimo** paslaugas ir įsitikinkite, **·**  **kad** vienos mokėjimo tarnybos numatytasis naujų kredito kortelių parinkties procesorius nustatytas kaip Taip.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Informacijos apie užsakymo klaidą laukas rodo sąskaitos struktūros klaidos pranešimą

Sąskaitos struktūros klaidos pranešimo tekstas gali skirtis, kaip rodomi toliau pateikti pavyzdžiai. Tačiau klaidos bendrai turi bendrą šakninį priežastį, kuri susijusi su sąskaitos struktūros konfigūracija.

- "Žurnalo paketo numerio registravimo rezultatai 0009656328 kvitas ARP-000959899 1,00 ARP-000959899 įmonėje us jūsų bus užregistruotas kaip permokėjimas arba neprimokėjimas.
- "Žurnalų paketo numerio registravimo rezultatai 0009656328 kvitas ARP-000959899 kvitas ARP-000959901 sąskaitos struktūra, skirta deriniui 618160, netinkamas bendrai naudojamai DK įmonės pagrindinei sąskaitai"
- "Žurnalų paketo numerio registravimo rezultatai 0009656328 kvitas ARP-000959899 kvitas ARP-000959901 pranešta iš įmonės sąskaitų us uždavimo duomenys"
- "Žurnalų paketo, į kuriuos 0009656328 žurnalo ARP-000959899. Registravimas atšauktas, registravimo rezultatai
    
Norėdami ištaisyti šias klaidas, peržiūrėkite sąskaitų struktūras tikslumui. Daugiau informacijos ieškokite Configure [account structures](/dynamics365/finance/general-ledger/configure-account-structures).
    
Kai klaida ištaisyta, pasirinkite nepavykusią operaciją, **o** tada puslapio viršuje pasirinkite Sinchronizuoti užsakymą, kad būtų vykdoma sinchronizavimo užduotis.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Kitų tipų klaidos, dėl kurių gali reikėti ištaisyti operacijos duomenis

Norėdami ištaisyti kitų tipų klaidas, dėl kurių gali reikėti fiksuoti operacijos duomenis, galite naudoti funkciją Redaguoti ir audito operacijas. Daugiau informacijos rasite Edit [ir audit transactions](../edit-order-trans.md).
