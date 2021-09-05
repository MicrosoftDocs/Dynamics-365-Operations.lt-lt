---
title: Planavimo optimizavimo nenaudojami parametrai
description: Šioje temoje pateikiami parametrai, į kuriuos Planavimo optimizavimas šiuo metu neatsižvelgia veikimo metu.
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1992523ae10f30196ebe55d7c7fe6a2549a3a12853da261bd4a129523b8e4ea2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714288"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Planavimo optimizavimo nenaudojami parametrai

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiami parametrai, į kuriuos Planavimo optimizavimas šiuo metu neatsižvelgia veikimo metu. Planavimo tarnyba gali praleisti parametrą, nes, pavyzdžiui, susijusios funkcijos dar nepalaikomos. Parametras taip pat galimai tapo pasenęs dėl funkcinių pokyčių.

Tolesniuose skyriuose pateikiami parametrai, kurių Planavimo optimizavimas nenaudoja konkrečiuose puslapiuose. Juose taip pat paaiškinta, kodėl kiekvienas parametras nėra naudojamas.

## <a name="master-planning-parameters-page"></a>Bendrojo planavimo parametrų puslapis

Planavimo optimizavimas nenaudoja šių parametrų ar parinkčių **Bendrojo planavimo parametrų** puslapyje:

- **Bendra** skirtukas:

    - **Dabartinės prognozės planas** – laukia *Prognozės* palaikymo.
    - **Dabartinis statinis pagrindinis planas** – laukia *Statinio plano kopijavimo į dinaminį* palaikymo.
    - **Dabartinis dinaminis pagrindinis planas** – laukia *Statinio plano kopijavimo į dinaminį* palaikymo.
    - **Kopijuoti užbaigtą ir atnaujintą statinį pagrindinį planą į dinaminį pagrindinį planą** – laukia *Statinio plano kopijavimo į dinaminį* palaikymo.
    - **Apskaičiuoto vėlavimo pradžios laikas** – laukia *Apskaičiuoto vėlavimo* palaikymo.
    - **Naudoti dinamines neigiamas dienas** – Planavimo optimizavimas visada naudoja *Dinaminių neigiamų dienų* principą.
    - **Šiandienos datos kalendorius** – laukia *Planavimo* palaikymo.
    - **Talpyklos naudojimas** – „Microsoft Azure” prenumeratos konfigūracija tvarkosi su efektyvumo taškais.
    - **Užduočių skaičius padėjėjo užduočių grupavime** – „Azure” prenumeratos konfigūracija tvarkosi su efektyvumo taškais.
    - **Prieš apdorojimą: automatiškai filtruoti pagal prekes, kurių poreikis yra tiesioginis** – „Azure” prenumeratos konfigūracija tvarkosi su efektyvumo taškais.
    - **Po apdorojimo: automatiškai filtruoti pagal prekes, kurių poreikis yra tiesioginis** – „Azure” prenumeratos konfigūracija tvarkosi su efektyvumo taškais.
    - **Užsakymų skaičius patvirtinimų grupavime** – „Azure” prenumeratos konfigūracija tvarkosi su efektyvumo taškais.
    - **Gijų skaičius** – „Azure” prenumeratos konfigūracija tvarkosi su efektyvumo taškais.
    - **Planavimo proceso skirtasis laikas minutėmis** – „Azure” prenumeratos konfigūracija tvarkosi su efektyvumo taškais.
    - **Planavimo pradžios laikas** – laukia *Planavimo* palaikymo.

- Skirtukas **Suplanuoti užsakymai**:

    - **Gavimo laikas** – laukia *Planavimo* palaikymo.
    - **Gamyba** – laukia *Planavimo* palaikymo.
    - **Projekto** skyriaus laukai – laukia *Planavimo* palaikymo.

- **Standartinio atnaujinimo** skirtukas:

    - **Atnaujinti žymėjimą** – laukia *Patvirtinimo* palaikymo.
    - **Jei įvyksta klaida, stabdyti patvirtinimą** – laukia *Patvirtinimo* palaikymo.
    - **Grupuoti pagal tiekėją** – laukia *Patvirtinimo* palaikymo.
    - **Grupuoti pagal pirkėjo grupę** – laukia *Patvirtinimo* palaikymo.
    - **Grupuoti pagal pirkimo sutartį** – laukia *Patvirtinimo* palaikymo.
    - **Grupuoti pagal laikotarpį** – laukia *Patvirtinimo* palaikymo.
    - **Rasti pirkimo sutartį** – laukia *Patvirtinimo* palaikymo.
    - **Grupuoti pagal planavimo prioritetą** – laukia *Patvirtinimo* palaikymo.
    - **Grupuoti pagal laikotarpį** – laukia *Patvirtinimo* palaikymo.

## <a name="coverage-groups-page"></a>Padengimo grupių puslapis

Planavimo optimizavimas nenaudoja šių parametrų ar parinkčių **Padengimo grupių** puslapyje:

- „FastTab“ **Bendra**.

    - **Teigiamos dienos** – laukia *Teigiamų dienų* palaikymo.
    - **Naudoti turimas atsargas** – laukia *Turimų atsargų naudojimo* palaikymo.
    - **Naudoti nurodytą KS arba formulės versiją** – laukia *Formulės versijų su sudėtiniu/šalutiniu produktu* palaikymo.
    - **Naudoti nurodytą maršruto versiją** – laukia *Poreikio su apibrėžta konkrečia KS arba maršruto reikalavimais* palaikymo.

- „FastTab“ skirtukas **Veiksmas**:

    - **Veiksmo pranešimas** – laukia *Veiksmų* palaikymo.
    - **Veiksmo laiko riba** – laukia *Veiksmų* palaikymo.
    - **Atidėjimo marža** – laukia *Veiksmų* palaikymo.
    - **Paankstinimo marža** – laukia *Veiksmų* palaikymo.
    - **Pagrindo data** – laukia *Veiksmų* palaikymo.
    - **Paankstinti** – laukia *Veiksmų* palaikymo.
    - **Atidėti** – laukia *Veiksmų* palaikymo.
    - **Sumažinti** – laukia *Veiksmų* palaikymo.
    - **Padidinti** – laukia *Veiksmų* palaikymo.
    - **Išvesti veiksmai** – laukia *Veiksmų* palaikymo.

- „FastTab” skirtukas **Kita**:

    - **Užblokuota laiko riba (dienomis)** – *Užblokuotos laiko ribos* palaikymas nesuplanuotas Planavimo optimizavime.
    - **KS išskleidimo laiko riba (dienomis)** – laukia *Planavimo* palaikymo.
    - **Pajėgumo planavimo laiko riba (dienomis)** – laukia *Planavimo* palaikymo.
    - **Patvirtintos paraiškos laiko riba (dienomis)** – laukia *Paraiškos* palaikymo.
    - **Prognozės plano laiko riba** – laukia *Prognozės* palaikymo.

- „FastTab” skirtukas **Vėlavimai**:

    - **Apskaičiuoti vėlavimai** – laukia *Apskaičiuoto vėlavimo* palaikymo.
    - **Apskaičiuoto vėlavimo ribos (dienomis)** – laukia *Apskaičiuoto vėlavimo* palaikymo.

## <a name="item-coverage-page"></a>Prekių padengimo puslapis

Planavimo optimizavimas nenaudoja šių parametrų ar parinkčių **Prekių padengimo** puslapyje:

- **Bendra** skirtukas:

    - **Suplanuoto užsakymo tipas** – Planavimo optimizavimas nepalaiko *„Kanban”* parinkties, laukia *„Kanban”* palaikymo.
    - **Užblokuota laiko riba (dienomis)** – *Užblokuotos laiko ribos* palaikymas nesuplanuotas Planavimo optimizavime.
    - **KS išskleidimo laiko riba (dienomis)** – laukia *Planavimo* palaikymo.
    - **Pajėgumo planavimo laiko riba (dienomis)** – laukia *Planavimo* palaikymo.
    - **Patvirtintos paraiškos laiko riba (dienomis)** – laukia *Paraiškos* palaikymo.
    - **Išpildyti minimumą** – Planavimo optimizavimas nepalaiko *Šiandienos datos*, *Pirmojo išdavimo* ir *Padengimo laiko ribos* parinkčių. Jis visada naudoja *Šiandienos data + įsigijimo laikas* parinktį.
    - **Minimalūs laikotarpiai** – laukia *Minimalaus atsargų lygio* palaikymo.
    - **Planavimo formulė** – laukia *Formulės versijų su sudėtiniu/šalutiniu produktais* palaikymo.
    - **Numatytasis prioritetas** – laukia *Formulės versijų su sudėtiniu/šalutiniu produktais* palaikymo.
    - **Dabartinis prioritetas** – laukia *Formulės versijų su sudėtiniu/šalutiniu produktais* palaikymo.
    - **Pakeista data** – laukia *Formulės versijų su sudėtiniu/šalutiniu produktais* palaikymo.
    - **Naudoti turimas atsargas** – laukia *Turimų atsargų naudojimo* palaikymo.

## <a name="master-plans-page"></a>Bendrųjų planų puslapis

Planavimo optimizavimas nenaudoja šių parametrų ar parinkčių **Bendrųjų planų** puslapyje:

- „FastTab“ **Bendra**.

    - **Įtraukti turimas atsargas** – laukia *Turimų atsargų naudojimo* palaikymo.
    - **Keisti turimas atsargas** – laukia *Turimų atsargų naudojimo* palaikymo.
    - **Naudoti turimas atsargas** – laukia *Turimų atsargų naudojimo* palaikymo.
    - **Įtraukti atsargų operacijas** – laukia *Turimų atsargų naudojimo* palaikymo.
    - **Įtraukti pardavimo pasiūlymus** – laukia *Pardavimo pasiūlymų* palaikymo.
    - **Įtraukti pasiūlymų patvirtinimus** – laukia *Pasiūlymų patvirtinimų* palaikymo.
    - **Naudoti laikymo trukmės datas** – Laukia *Laikymo trukmės* palaikymo.
    - **Įtraukti tęstinumo planą** – laukia *Tęstinumo planavimo* palaikymo.
    - **Planavimo metodas** – laukia *Planavimo* palaikymo.
    - **Baigtinė ypatybė** – laukia *Planavimo* palaikymo.
    - **Atgalinio planavimo pajėgumo laiko riba (dienomis)** – laukia *Planavimo* palaikymo.
    - **Baigtinis pajėgumas** – laukia *Planavimo* palaikymo.
    - **Baigtinio pajėgumo laiko riba** – laukia *Planavimo* palaikymo.
    - **Baigtinis pajėgumas ribotosios spartos ištekliams** – laukia *Planavimo* palaikymo.
    - **Pajėgumo laiko riba ribotosios spartos ištekliams** – laukia *Planavimo* palaikymo.
    - **Suplanuoti užsakymai** – Planavimo optimizavimas naudoja fiksuotas numeracijas.
    - **Seansas** – Planavimo optimizavimas naudoja fiksuotas numeracijas.
    - **Tęstinumo planas** – Planavimo optimizavimas naudoja fiksuotas numeracijas.

- „FastTab” skirtukas **Laiko ribos dienomis**:

    - **Užblokuoti** – *Užblokuotos laiko ribos* palaikymas nesuplanuotas Planavimo optimizavime.
    - **Išskleidimas** – laukia *Planavimo* palaikymo.
    - **Prognozės planas** – laukia papildomo *Prognozės* palaikymo.
    - **Pajėgumas** – laukia *Planavimo* palaikymo.
    - **Tęstinumo planas** – laukia *Tęstinumo planavimo* palaikymo.
    - **Veiksmo pranešimas** – laukia *Veiksmų* palaikymo.
    - **Apskaičiuoti vėlavimai** – laukia papildomo *Apskaičiuoto vėlavimo* palaikymo.
    - **Seka** – laukia *Gamybos* palaikymo.

- „FastTab” skirtukas **Apskaičiuoti vėlavimai**:

    - **Įsitikinti, kad suplanuoti užsakymai nesukurti prieš bendrojo planavimo vykdymo datą** – laukia *Apskaičiuotų vėlavimų* palaikymo.
    - **Pridėti apskaičiuotą vėlavimą prie poreikio datos** (skyriuje **Suplanuoti pirkimo užsakymai**) – laukia *Apskaičiuotų vėlavimų* palaikymo.
    - **Pridėti apskaičiuotą vėlavimą prie poreikio datos** (skyriuje **Suplanuoti gamybos užsakymai**) – laukia *Apskaičiuotų vėlavimų* palaikymo.
    - **Pridėti apskaičiuotą vėlavimą prie poreikio datos** (skyriuje **Suplanuoti perkėlimai**) – laukia *Apskaičiuotų vėlavimų* palaikymo.
    - **Pridėti apskaičiuotą vėlavimą prie poreikio datos** (skyriuje **Suplanuoti „kanban”**) – laukia *Apskaičiuotų vėlavimų* palaikymo.

- „FastTab” skirtukas **Seka**:

    - **Suplanuotų užsakymų seka po bendrojo planavimo** – laukia *Sekos* palaikymo.
    - **Talpyklos tipas** – laukia *Sekos* palaikymo.
    - **Laikotarpio tipas** – laukia *Sekos* palaikymo.
    - **Kampanijos ciklo talpyklų skaičius** – laukia *Sekos* palaikymo.

## <a name="released-product-details-page"></a>Puslapis Išleisto produkto informacija

Planavimo optimizavimas nenaudoja šio parametro parinkties **Išsamios išleisto produkto informacijos** puslapyje:

- „FastTab” skirtukas **Inžinerija**:

    - **Gamybos tipas** – Planavimo optimizavimas nepalaiko *Planavimo elemento* parinkties, laukia *Planavimo elementų* palaikymo.

## <a name="default-order-settings-page"></a>Numatytųjų užsakymo parametrų puslapis

Planavimo optimizavimas nenaudoja šio parametro **Numatytųjų užsakymo parametrų** puslapyje:

- „FastTab” skirtukas **Atsargos**:

    - **Pristatymo datos valdymas** – Planavimo optimizavimas nepalaiko *„CTP”* parinkties, laukia *„CTP”* palaikymo.

## <a name="working-time-calendars-page"></a>Darbo laiko kalendorių puslapis

Planavimo optimizavimas nenaudoja šio parametro **Darbo laiko kalendorių** puslapyje:

- **Pagrindinis kalendorius** – laukia *Pagrindinių kalendorių* palaikymo.

## <a name="batch-disposition-master-page"></a>Pagrindinis paketo perdavimo puslapis

Planavimo optimizavimas nenaudoja šio parametro **Pagrindinio paketo perdavimo** puslapyje:

- „FastTab” skirtukas **Nustatymas**:

    - **Aktyvus** – laukia *Paketų perdavimo kodų* palaikymo.