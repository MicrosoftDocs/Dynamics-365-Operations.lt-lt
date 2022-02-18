---
title: Planavimo optimizavimo nenaudojami parametrai
description: Šioje temoje pateikiami parametrai, į kuriuos Planavimo optimizavimas šiuo metu neatsižvelgia veikimo metu.
author: ChristianRytt
ms.date: 09/02/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 01edccbf1a50264b3867e303cbca44eb1b1d7dd9
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087504"
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

## <a name="coverage-groups-page"></a>Padengimo grupių puslapis

Planavimo optimizavimas nenaudoja šių parametrų ar parinkčių **Padengimo grupių** puslapyje:

- „FastTab“ **Bendra**.

  - **Teigiamos dienos** – The *Teigiamos dienos* vertė nenaudojama. Naudojant planavimo optimizavimą, teigiamos dienos laikomos begalinėmis.
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

- **Gamybos laikas** skirtukas:

  - **Pirkimo laikas** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, „Planning Optimization“ naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.
  - **Gamybos laikas** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, „Planning Optimization“ naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.
  - **Perdavimo laikas** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, „Planning Optimization“ naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.
  - **Darbo dienos** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, „Planning Optimization“ naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.

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

- **Veiksmo pranešimas** FastTab:

  - **Atnaujinkite atidėtą datą kaip reikalavimo datą** - Šis parametras nutraukiamas naudojant planavimo optimizavimą.

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

- **Pirkimo laiko** „FastTab“:

  - **Pirkimo pagrindinis laikas** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, „Planning Optimization“ naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.
  - **Darbo dienos** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, „Planning Optimization“ naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.

- „FastTab” skirtukas **Atsargos**:

  - **Pristatymo datos valdymas** – Planavimo optimizavimas nepalaiko *„CTP”* parinkties, laukia *„CTP”* palaikymo.
  - **Atsargų pagrindinis laikas** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, planavimo optimizavimas naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.
  - **Darbo dienos** – „Planning Optimization“ tarnybos versijose, kurios yra senesnės nei 2021 m. rugpjūčio 6 d. leidimas, „Planning Optimization“ naudoja šį parametrą tinkamam užsakymo ir pristatymo datoms apskaičiuoti, tačiau pats apskaičiuotas gamybos laikas neišskaičiuotas suplanuotiems užsakymams. Vėlesnėse versijose aptarnavimas naudoja ir apskaičiuotą gamybos laiką, kad nustatytų pasirinktį **Gamybos laikas** laukelyje ir **Darbo dienos** kaip reikalaujama susijusiame suplanuotame užsakyme.

## <a name="working-time-calendars-page"></a>Darbo laiko kalendorių puslapis

Planavimo optimizavimas nenaudoja šio parametro **Darbo laiko kalendorių** puslapyje:

- **Pagrindinis kalendorius** – laukia *Pagrindinių kalendorių* palaikymo.

## <a name="batch-disposition-master-page"></a>Pagrindinis paketo perdavimo puslapis

Planavimo optimizavimas nenaudoja šio parametro **Pagrindinio paketo perdavimo** puslapyje:

- „FastTab” skirtukas **Nustatymas**:

  - **Aktyvus** – laukia *Paketų perdavimo kodų* palaikymo.
