---
title: Gautinų sumų registravimas
description: Šiame straipsnyje paaiškinama, kaip sukonfigūruotas gautinų sumų registravimas, ir pateikiami registravimo konfigūracijų pavyzdžiai.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492bbd31cae08a93cd68e5ce120d02a62141241b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874580"
---
# <a name="accounts-receivable-posting"></a>Gautinų sumų registravimas

[!include [banner](../includes/banner.md)]

Pirminis gautinų sumų modulio **registravimo** šablonas yra kliento registravimo šablonas. Šis registravimo šablonas nustato suminė sąskaitą, kuri naudojama, kai klientų balansai registruojami DK. Su suminė sąskaita yra pagrindinė sąskaita. Tai dar vadinama gautinų sumų prekybos sąskaita.

Daugiau informacijos žr. [Kliento publikavimo profiliai](../accounts-receivable/customer-posting-profiles.md).

Kelios registravimo konfigūracijos šalia kliento registravimo šablono galimos gautinose sumose. Toliau pateikiami skyriai pateikia daugiau informacijos apie kitas registravimo konfigūracijas.

## <a name="posting-accounts-for-methods-of-payment"></a>Mokėjimo būdų registravimo sąskaitos

Mokėjimo būdai apibrėžia, kaip mokėjimas bus registruojamas DK. Jie taip pat kontroliuoja mokėjimo išeigos elgseną. Paprastai kiekvienam mokėjimo tipui, kurį priima jūsų organizacija, sukuriamas vienas mokėjimo būdas (pvz., grynaisiais pinigais, čekiu, kredito kortele, pinigų užsakymu ir pervedimu už pinigų pervedimą).

Bendrosios "**FastTab**" skyriaus **Registravimas** laukai kontroliuoja, kaip mokėjimas bus registruojamas DK. Pirmiausia turite pasirinkti vertę lauke **Sąskaitos** tipas. Sąskaitos tipas, kurį pasirenkate, kontroliuoja mokėjimo sąskaitos **lauko elgseną**. Rekomenduojame sąskaitos tipo lauke **pasirinkti** Bankas **·**, o tada pasirinkti banko sąskaitą mokėjimo **sąskaitos** lauke. Šis būdas naudingas, kai sistema užregistruos mokėjimą banko papildomos knygos metu, kuris palaiko suderinimą ir kitus su grynaisiais pinigais susijusius procesus. Šioje lentelėje pateikiamas registravimo šablono konfigūracijos pavyzdys, jei naudojate grynųjų pinigų ir **banko valdymo modulį**.

| Registravimo tipas | Kodo tipas | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Bankas | Bankas | "Contoso" bankas | Su turtu susijęs banko kodas | Kreditas | Ne | Įveskite kiekvieno mokėjimo būdo pagrindinę sąskaitą į lauką **Mokėjimo** sąskaita. |

Jei planuojate naudoti grynųjų pinigų ir banko valdymą, **·** **turite** pasirinkti DK lauke Sąskaitos tipas, o tada pasirinkti pagrindinę sąskaitą mokėjimo **sąskaitos** lauke. Šioje lentelėje pateikiamas registravimo šablono konfigūracijos pavyzdys, jei nenaudojate grynųjų pinigų ir banko valdymo.

| Registravimo tipas | Kodo tipas | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Didžioji knyga | Didžioji knyga | 100100: "Contoso" bankas | Turtas | Kreditas | Ne | Įveskite kiekvieno mokėjimo būdo pagrindinę sąskaitą į lauką **Mokėjimo** sąskaita. |

## <a name="bridging-accounts"></a>Tarpinės sąskaitos

Tarpinis registravimas yra dviejų veiksmų procesas, naudojamas registruojant mokėjimus. Tai pasirinktinė priemonė, kurią galima naudoti, pavyzdžiui, su nulinio balanso banko sąskaitomis. Tai gali padėti užtikrinti, kad banko suderinimo procesas būtų sklandesnis ir laiku atliktas. Pirmuoju veiksmu mokėjimas registruojamas laikinoje sąskaitoje (tarpinė sąskaita). Antruoju veiksmu užregistruotas įrašas atšaukiamas ir užregistruojamas banko sąskaitoje, kai mokėjimas išvalo banką. Šioje lentelėje pateikiamas registravimo šablono konfigūracijos pavyzdys, skirtas tarpinis registravimas.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| DK žurnalas | 130725 | Neapuoti grynieji pinigai | Įsipareigojimai | Debetas | Taip | Įveskite kiekvieno mokėjimo būdo pagrindinę sąskaitą tarpinės **sąskaitos lauke**. |

Daugiau informacijos rasite Tarpinių [mokėjimų nustatykite ir apdorokite](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Kliento mokėjimo nuolaidų registravimo sąskaitos

Jei jūsų organizacija siūlo mokėjimo nuolaidas klientams greitai sumokėti, turite sukonfigūruoti mokėjimo nuolaidos kodus ir nurodyti, kaip nuolaidos turėtų būti registruojamos DK. Galimos kelios pagrindinės sąskaitos, naudojamos kliento mokėjimo nuolaidai registruoti, pasirinkimo pasirinktys.

Daugiau informacijos rasite mokėjimo [nuolaidos](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Mokėjimo mokesčių registravimo sąskaitos

Mokėjimo mokesčiai leidžia automatiškai įtraukti mokestį į kliento mokėjimą, kai taikomas sąlygų rinkinys. Klientui gali būti mokami mokėjimo mokesčiai arba jie gali būti registruojami į jūsų banko sąskaitą kaip išlaidos. Štai keletas pavyzdžių:

- Jūs apmokestinate klientus 3 procentais nuo bendrosios mokėjimo sumos, jei jie moka naudodami kredito kortelę.
- Jūsų bankas $1.00 išlaidas už kiekvieną apdorojamą pervedimą, o pervedimo mokestis yra į išlaidas.

Konfigūruodami kliento mokėjimo mokestį, **·** **jei** nustatote lauką Mokestis klientui, **pagrindinės** sąskaitos laukas tampa negalimas, ir sistema mokesčiui registruoti naudoja kliento registravimo šabloną. Jei lauke Mokesčiai nustatote **DK** **·**, **pagrindinės** sąskaitos lauką turite nustatyti kaip pagrindinę sąskaitą, kurioje bus registruojamas mokėjimo mokestis. Paprastai ši pagrindinė sąskaita bus išlaidų sąskaita. Šioje lentelėje pateikiamas registravimo šablono konfigūracijos pavyzdys, skirtas mokėjimo mokesčiui registruoti.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| DK žurnalas | 618190 | Banko mokesčio išlaidos | Išlaidos | Debetas | Ne |  Jei **lauke** Mokestis pasirinkta **DK**, pasirinkite šią sąskaitą **mokėjimo mokesčio** lauke Pagrindinė sąskaita. |

Daugiau informacijos žr. [Nustatyti mokėjimo klientams mokesčius](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Mokesčių kodų registravimas

Jei prie eilutės prekių turite sekti pardavimo sumas, galite naudoti mokesčių kodus. Pavyzdžiui, jūs galite nustatyti transportavimo ir tvarkymo mokesčius savo klientams, arba galite išlaidas kai kuriems transportavimo ir tvarkymo mokesčiams viduje. Galite nurodyti, ar šios sumos registruojamos išlaidų sąskaitose, ar pridėtos prie prekių išlaidų.

Galite kurti gautinų ir mokėtinų sumų išlaidų kodus. Konfigūruodami išlaidų kodą, turite nurodyti registravimą. Registravimas valdo ir debeto sąskaitą, ir kredito sąskaitą. Galite pasirinkti kiekvieno sukurto išlaidų tipo registravimo tipą. Šioje lentelėje pateikiami įprasti gautinų sumų išlaidų kodų pavyzdžiai.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Mokestis | 411400 | Įplaukos – mokesčiai | Įplaukos | Kreditas | Ne | **Pavyzdys, jei lėšų nepakanka: debeto** klientas / tiekėjas ir kredito DK sąskaita |
| Užsakymas, krovinių pervežimas | 403500 | Įplaukos – transportavimas | Įplaukos | Kreditas | Ne | **Klientui taikomas transportavimo pavyzdys:** debeto klientas / tiekėjas ir kredito DK sąskaita |
| Grąžinimas\* | 403200 | Nuolaida | Įplaukos | Debetas | Ne | **Kliento grąžinimo pavyzdys: debeto** DK sąskaita ir kreditas – klientas / tiekėjas |

\* Grąžinimo atveju registravimas naudojamas tik tada, kai išlaidų kodas įtraukiamas į pirkimo užsakymo antraštę arba eilutę. Išplėstinės grąžinimo funkcijos, kurias galima naudoti programoje "Microsoft Dynamics 365 Supply Chain Management ", leidžia labiau valdyti ir automatiškai naudoti grąžinimus. Norėdami gauti daugiau informacijos, žr [. Kliento grąžinimus](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Ankstesnėje lentelėje pateikiami trys įprasti registravimo tipų, kuriuos galima naudoti išlaidų kodams, pavyzdžiai. Jis turėtų būti naudojamas kaip gairė ir pavyzdys. Nėra išsamesnio visų galimų naudoti kombinacijų ar registravimo tipų sąrašo.

Daugiau informacijos rasite Dalyje [Kurti išlaidų kodą](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Komisinių sąskaitų registravimas

Galite pasirinktinai konfigūruoti sistemą, kad ji apskaičiuotų pardavimo atstovo komisinius arba pardavimo atstovų grupę pateiktame pardavimo užsakyme. Jei įgalinsite šią funkciją, turite sukonfigūruoti registravimo sąskaitą, kuri naudojama komisiniams apskaičiuoti. Ši konfigūracija atliekama Pardavimo ir **rinkodaros modulio** Komisinių **registravimo** puslapyje.

Daugiau informacijos rasite Pardavimo [komisinių taisyklių rinkinys](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).
