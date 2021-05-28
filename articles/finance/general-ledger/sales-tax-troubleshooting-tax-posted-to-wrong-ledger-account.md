---
title: Mokestis registruojamas neteisingame DK sąskaitoje kvite
description: Šioje temoje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai mokesčiai registruojami į netinkamą DK sąskaitą kvite.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020096"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Mokestis registruojamas neteisingame DK sąskaitoje kvite

[!include [banner](../includes/banner.md)]

Publikavimo metu, mokesčiai gali būti publikuoti į ne tą DK paskyrą kvite. Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus. Šios temos pavyzdžiuose kaip verslo dokumentą naudojamas pardavimo užsakymas.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Rasti neteisingai užregistruotos mokesčio operacijos mokesčio kodą

1. Kvito **operacijų puslapyje pasirinkite** operaciją, su kuria norite dirbti, tada pasirinkite **Užregistruotas** PVM.

    [![Užregistruotas PVM mygtukas kvito operacijų puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Lauke **PVM kodas** peržiūrėkite vertę. Šiame pavyzdyje tai **19** PVM.

    [![PVM kodo laukas užregistruoto PVM puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Patikrinti mokesčio kodo DK registravimo grupę

1. Nueikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM kodai**.
2. Raskite ir pasirinkite mokesčio kodą, tada peržiūrėkite vertę lauke **DK registravimo** grupė. Šiame pavyzdyje tai **PVM**.

    [![DK publikavimo grupės laukelis PVM kodo puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Lauke **DK registravimo grupė** įveskite vertę. Norėdami peržiūrėti išsamią grupės konfigūracijos informaciją, pasirinkite saitą. Arba pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) lauke ir pasirinkite **Peržiūrėti** informaciją.

    [![Papildomos informacijos komandos peržiūra](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Mokėtino **PVM** lauke, atsižvelgiant į operacijos tipą, patikrinkite, ar sąskaitos numeris teisingas. Jei jos nėra, pasirinkite tinkamą sąskaitą, į ją įregistruokite. Šiame pavyzdyje pardavimo užsakymo PVM turi būti registruojamas mokėtino PVM sąskaitoje, 222200.

    [![Mokėtino PVM laukas DK registravimo grupių puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Toliau esančioje lentelėje pateikiama informacija apie kiekvieną DK registravimo **grupių puslapio** lauką.

    | Laukas                  | Aprašas |
    |------------------------|-------------|
    | Mokėtinas PVM      | Pagrindinė sąskaita išeinančiam PVM, kuris mokamas mokesčių įstaigai. |
    | Gautinas PVM   | Pagrindinė sąskaita ateinantiems mokesčiams, kurie gaunami iš mokesčių įstaigos. |
    | Naudojimo mokesčio išlaidos        | Pagrindinė sąskaita, naudojama atskaitomais naudojimo mokesčiais, kurių tiekėjai nepaiso mokesčių inspekcijos kaip Europos Sąjungos (ES) atvirkštinio apmokestinimo prekių ir paslaugų mokesčio (GST) / suderintos PVM (HST) dalimi. **Naudoti mokestį** turi būti pažymėtas PVM kodas PVM mokesčio grupėje, naudojamoje operacijoje. Šis laukas nepasiekiamas, jei puslapyje **Didžiosios knygos parametrai** pažymėta parinktis **Taikyti PVM apmokestinimo taisykles**. |
    | Mokėtinas naudojimo mokestis        | Pagrindinė sąskaita, naudojama gaunamiems naudojimo mokesčiams, mokėtinams mokesčių inspekcijai, registruoti. |
    | Sudengimo sąskaita     | Pagrindinė publikuoti grynąjį DK balansą naudojama sąskaita yra nurodyta **Naudoti PVM** ir **Gautinas PVM** laukelius. |
    | Tiekėjo mokėjimo nuolaida   | Pagrindinė sąskaita naudojama publikuoti grynųjų nuolaidą PVM kodui, susietam su šios DK publikavimo grupe. |
    | Kliento atvejo nuolaida | Pagrindinė sąskaita naudojama publikuoti grynųjų nuolaidą PVM kodui, susietam su šios DK publikavimo grupe. |

    Daugiau informacijos žr. [Didžiosios knygos registravimo grupių nustatymas pardavimo mokesčiui](tasks/set-up-ledger-posting-groups-sales-tax.md)

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Suderinti kodą, norint patikrinti DK dimensijas

Kode registravimo sąskaitą nustato DK dimensija. DK dimensija įrašo sąskaitos ID duomenų bazėje.

1. Pardavimo užsakymui pridėkite stabdos tašką mokesčių **saveAndPost::()** ir **Tax ::post()** metoduose. Skirti dėmesį į **\_ledgerDimension** vertę.

    [![Pardavimo užsakymo kodo pavyzdys, kuriame yra stabdos taškas](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Pirkimo užsakymui, įtraukite stabdos tašką **TaxPost::saveAndPost()** ir **TaxPost::postToTaxTrans()** metodus. Skirti dėmesį į **\_ledgerDimension** vertę.

    [![Pirkimo užsakymo kodo pavyzdys, kuriame yra stabdos taškas](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Vykdykite šią SQL užklausą, kad duomenų bazėje surasti rodomą sąskaitos vertę, pagrįstą įrašo ID, kuris įrašytas DK dimensijos.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Rodyti įrašo ID vertę](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Išnagrinėkite užduoties reikšmę, kad **_ledgerDimension** kur priskirta ši vertė. Paprastai vertė yra iš **TmpTaxWorkTrans**. Tokiu atveju turėtumėte įtraukti stabdos tašką **TmpTaxWorkTrans::insert()** ir **TmpTaxWorkTrans::update()** kad rastumėte, kur priskirta vertė.

## <a name="determine-whether-customization-exists"></a>Nustatyti, ar yra tinkinimas

Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas. Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
