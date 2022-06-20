---
title: Mokėtinų sumų registravimas
description: Šiame straipsnyje paaiškinama, kaip konfigūruojamas mokėtinų sumų registravimas, ir pateikiami registravimo konfigūracijų pavyzdžiai.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b3593e01ed4d0a88b5816803f1d67fa7ed5e0f6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908015"
---
# <a name="accounts-payable-posting"></a>Mokėtinų sumų registravimas

[!include [banner](../includes/banner.md)]

Pirminis mokėtinų sumų modulio **registravimo** šablonas yra tiekėjo registravimo šablonas. Šis registravimo šablonas nustato suminė sąskaitą, kuri naudojama, kai tiekėjo balansai registruojami DK. Su suminė sąskaita yra pagrindinė sąskaita. Tai dar vadinama mokėtinų sumų prekybos sąskaita.

Daugiau informacijos ieškokite Tiekėjo [registravimo šablonuose](../accounts-payable/vendor-posting-profiles.md).

Mokėtinose sumose be tiekėjo registravimo šablono galimos kelios registravimo konfigūracijos. Toliau pateikiami skyriai pateikia daugiau informacijos apie kitas registravimo konfigūracijas.

## <a name="methods-of-payment-posting-accounts"></a>Mokėjimo registravimo sąskaitų metodai

Mokėjimo būdai apibrėžia, kaip mokėjimas bus registruojamas DK. Jie taip pat kontroliuoja mokėjimo išeigos elgseną. Paprastai kiekvienam jūsų organizacijos mokėjimo tipui sukuriamas vienas mokėjimo būdas (pvz., grynieji pinigai, čekis, kredito kortelė, pinigų užsakymas ir paslaugos).

Laukai, **·** **skyriaus** Registravimas, kuris yra Bendrajame "FastTab **·**", mokėjimo būdų puslapyje (**Mokėtinos sumos > Mokėjimo nustatymas >** Mokėjimo būdai) kontroliuoja, kaip mokėjimas bus registruojamas DK. Pirmiausia turite pasirinkti vertę lauke **Sąskaitos** tipas. Sąskaitos tipas, kurį pasirenkate, kontroliuoja mokėjimo sąskaitos **lauko elgseną**. Rekomenduojame sąskaitos tipo lauke **pasirinkti** Bankas **·**, o tada pasirinkti banko sąskaitą mokėjimo **sąskaitos** lauke. Šis būdas naudingas, kai sistema užregistruos mokėjimą banko papildomos knygose, palaikančioje suderinimą ir kitus su grynaisiais pinigais susijusius procesus. Šioje lentelėje pateikiamas registravimo šablono konfigūracijos pavyzdys, jei naudojate grynųjų pinigų ir **banko valdymo modulį**.

| Registravimo tipas | Kodo tipas | Mokėjimo sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Bankas | Bankas | Amerikos Bankas | Su turtu susijęs banko kodas | Debetas | Ne | Įveskite kiekvieno mokėjimo būdo pagrindinę sąskaitą į lauką **Mokėjimo** sąskaita. |

Jei planuojate naudoti grynųjų pinigų ir banko valdymą, **·** **turite** pasirinkti DK lauke Sąskaitos tipas, o tada pasirinkti pagrindinę sąskaitą mokėjimo **sąskaitos** lauke. Šioje lentelėje rodomas registravimo šablono konfigūracijos pavyzdys, jei nenaudojate **grynųjų** pinigų ir banko valdymo.

| Registravimo tipas | Kodo tipas |Mokėjimo sąskaitos pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Didžioji knyga | Didžioji knyga | 100100: Amerikos bankas | Turtas | Debetas | Ne | Įveskite kiekvieno mokėjimo būdo pagrindinę sąskaitą į lauką **Mokėjimo** sąskaita. |

## <a name="bridging-accounts"></a>Tarpinės sąskaitos

Tarpinis registravimas yra dviejų veiksmų procesas, naudojamas registruojant mokėjimus. Tai pasirinktinė priemonė, kurią galima naudoti, pavyzdžiui, su nulinio balanso banko sąskaitomis. Tai gali padėti užtikrinti, kad banko suderinimo procesas būtų sklandesnis ir laiku atliktas. Pirmuoju veiksmu mokėjimas registruojamas laikinoje sąskaitoje (tarpinė sąskaita). Antruoju veiksmu užregistruotas įrašas atšaukiamas ir užregistruojamas banko sąskaitoje, kai mokėjimas išvalo banką. Šioje lentelėje pateikiamas registravimo šablono konfigūracijos pavyzdys, skirtas tarpinis registravimas.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| DK žurnalas | 130725 | Neapuoti grynieji pinigai | Įsipareigojimai | Debetas | Taip | Įveskite kiekvieno mokėjimo būdo pagrindinę sąskaitą tarpinės **sąskaitos lauke**. |

Daugiau informacijos rasite Tarpinių [mokėjimų nustatykite ir apdorokite](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Kliento mokėjimo nuolaidų registravimo sąskaitos

Jei jūsų organizacija mokėjimo nuolaidas gauna iš tiekėjų, kad galėtų greitai atlikti mokėjimus, turite sukonfigūruoti mokėjimo nuolaidos kodus ir nurodyti, kaip nuolaidos turėtų būti registruojamos DK. Galimos kelios pagrindinės sąskaitos, naudojamos kliento mokėjimo nuolaidai registruoti, pasirinkimo pasirinktys.

Daugiau informacijos rasite mokėjimo [nuolaidos](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Mokėjimo mokesčių registravimo sąskaitos

Mokėjimo mokesčiai leidžia automatiškai pridėti mokestį prie tiekėjo mokėjimo, kai taikomas sąlygų rinkinys. Mokėjimo mokesčiai gali būti mokami tiekėjui arba jie gali būti registruojami į jūsų banko sąskaitą kaip išlaidos. Štai keletas pavyzdžių:

- Tiekėjas sumoka 3 procentais bendrosios mokėjimo sumos, jei mokate naudodamiesi kredito kortele.
- Jūsų bankas $1.00 kiekvieno jūsų apdorojamo pervedimo išlaidų pervedimą, o mokestis yra į išlaidas.

Jei konfigūruojate tiekėjo mokėjimo mokestį, **·** **jei** nustatote lauką Mokestis tiekėjui, **pagrindinės** sąskaitos laukas tampa negalimas, ir sistema mokesčiui registruoti naudoja tiekėjo registravimo šabloną. Jei lauke Mokesčiai nustatote **DK** **·**, **pagrindinės** sąskaitos lauką turite nustatyti kaip pagrindinę sąskaitą, kurioje bus registruojamas mokėjimo mokestis. Paprastai ši pagrindinė sąskaita bus išlaidų sąskaita. Šioje lentelėje pateikiamas registravimo šablono konfigūracijos pavyzdys, skirtas mokėjimo mokesčiui registruoti.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| DK žurnalas | 618190 | Banko mokesčio išlaidos | Išlaidos | Debetas | Ne | Jei **lauke** Mokestis pasirinkta **DK**, pasirinkite šią sąskaitą lauke **Pagrindinė sąskaita**, kuris yra **mokėjimo mokesčio** puslapyje. |

Daugiau informacijos žr. [Nustatyti tiekėjo mokėjimo mokesčius](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Išlaidų kodo registravimo sąskaitos

Jei turite sekti pirkimo sumas kartu su eilutės prekėmis, galite naudoti išlaidų kodus. Pavyzdžiui, jūsų tiekėjas gali jums taikyti transportavimo ir tvarkymo mokesčius, arba tai gali išlaidas kai kuriems transportavimo ir tvarkymo mokesčiams viduje. Galite nurodyti, ar šios sumos registruojamos išlaidų sąskaitose, ar pridėtos prie prekių išlaidų.

Galite kurti gautinų ir mokėtinų sumų išlaidų kodus. Konfigūruodami išlaidų kodą, turite nurodyti registravimą. Registravimas valdo ir debeto sąskaitą, ir kredito sąskaitą. Kurdami išlaidų kodus, galite pasirinkti registravimo tipą, kuris naudojamas kiekvienam mokesčio kodui. Šioje lentelėje pateikiami įprastų mokėtinų sumų išlaidų kodų pavyzdžiai **mokesčių kodų** puslapyje.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Pirkimo mokestis | Palikite lauką tuščią. | Netaikoma | Elementas | Debetas | Ne | **Prekės pirkimo mokesčio pavyzdys:** </p><ul><li>**Debeto tipo** laukas = **Prekė**</li><li>  **Kredito tipo** laukas = Klientas **/Tiekėjas**.</li><li> Registruojant prekę naudojama pagrindinė sąskaita iš atsargų registravimo šablono. |
| Užsakymas, krovinių pervežimas | 600120 | Krovinio pervežimas | Įplaukos | Debetas | Ne | **Transportavimo, kuris mokamas tiekėjui, pavyzdys:** </p><ul><li>**Debeto** tipo laukas = **DK sąskaita**</li><li> **Kredito tipo** laukas = Klientas **/Tiekėjas** |
| Grąžinimas\* | 503160 | Tiekėjo grąžinimas (sąlaja COGS)| Išlaidos | Kreditas | Ne | **Tiekėjo grąžinimo pavyzdys:**</p><ul><li>**Debeto tipo** laukas = Klientas **/Tiekėjas**</li><li>**Kredito tipo** laukas = **DK sąskaita** |

\* Grąžinimo atveju registravimas naudojamas tik tada, kai išlaidų kodas įtraukiamas į pirkimo užsakymo antraštę arba eilutę. Išplėstinės grąžinimo funkcijos, kurias galima naudoti programoje "Microsoft Dynamics 365 Supply Chain Management ", leidžia labiau valdyti ir automatiškai naudoti grąžinimus. Daugiau informacijos rasite Tiekėjo [grąžinimai](../../supply-chain//procurement/vendor-rebates.md).

Ankstesnėje lentelėje pateikiami trys įprasti registravimo tipų, kuriuos galima naudoti išlaidų kodams, pavyzdžiai. Jis turėtų būti naudojamas kaip gairė ir pavyzdžių pasirinkimas. Nėra išsamesnio visų galimų naudoti kombinacijų ar registravimo tipų sąrašo.

Daugiau informacijos rasite Dalyje [Kurti išlaidų kodą](../accounts-receivable/create-charges-codes.md).
