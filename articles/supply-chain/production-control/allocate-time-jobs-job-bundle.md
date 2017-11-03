---
title: "Laiko paskirstymas sugrupuotų užduočių užduotims"
description: "Užduotis sugrupuoti galite modulyje Gamybos vykdymas. Tada puslapyje Užduočių sąrašas tuo pačiu metu galite pradėti kelias užduotis."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 26dc5a5a667f32d67fb86b3f765acaf37eeb38fb
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Laiko paskirstymas sugrupuotų užduočių užduotims

[!include[banner](../includes/banner.md)]


Užduotis sugrupuoti galite modulyje Gamybos vykdymas. Tada puslapyje Užduočių sąrašas tuo pačiu metu galite pradėti kelias užduotis.

Jei grupuojate užduotis, turite nustatyti kaip bendras visų užduočių registruotas laikas turi būti priskirtas kiekvienai užduočiai. Paskirstymą nustatykite pasirinkdami vieną iš šių lauko **Grupuoti tipus** dalies **Paskirstymo raktai** pasirinkčių:

-   **Įvertinimas** – laikas paskirstomas užduotims pagal įvertintą užduočių laiką.
-   **Užduotys** – laikas paskirstomas pagal visas sugrupuotas užduotis ir pagal tai, kiek laiko prireikė visoms užduotims užbaigti.
-   **Grynasis laikas** – laikas po lygiai paskirstomas visoms užduotims, tuo metu esančioms grupėje.
-   **Realusis laikas** – paskirstomas faktinis užduoties laikas. Išlaidos gali būti skaičiuojamos pagal faktines algalapio išlaidas. **Pastaba:** paskirstymo raktas **Realusis laikas** galimas tik, jei jūsų įmonėje naudojama atlyginimų funkcionalumą Laikas ir buvimas darbe.

Toliau pateikiami įvairių paskirstymo raktų naudojimo rezultatų pavyzdžiai.

## <a name="example-scenario"></a>Pavyzdinis scenarijus
Jūsų užduočių eilėje esančios užduotys turi būti baigtos. Pradedate pirmąją užduotį ir tada, kol ši užduotis vykdoma, pradedate antrąją ir trečiąją užduotis. Todėl susidaro trys sugrupuotos užduotys. Toliau pateikiamoje lentelėje parodytas įvertintas kiekvienos užduoties gamybos laikas.

| Užduotis   | Gamybos laikas |
|-------|-----------------|
| 1 užduotis | 1 valanda          |
| 2 užduotis | 3 valandos         |
| 3 užduotis | 4 valandos         |
| Bendroji suma | 8 valandos         |

Toliau pateikiamoje lentelėje nurodytos kiekvienai užduočiai atlikti sugaištos faktinės darbo valandos.

| Užduotis    | Pradžios laikas | Pabaigos laikas | Grupės laikas |
|--------|------------|----------|-------------|
| 1 užduotis  | 09:00      | 11.00    | 2 valandos     |
| 2 užduotis  | 10:00      | 13.00    | 3 valandos     |
| 3 užduotis  | 10:00      | 15:00    | 5 valandos     |
| Grupuoti | 09:00      | 15:00    | 6 valandos     |

Toliau pateikiamuose skyriuose aprašomi apskaičiuoto laiko kiekvienam paskirstymo raktui rezultatai.

## <a name="estimation-allocation-key"></a>Įvertinimo paskirstymo raktas
Ši lentelė parodo paskirstyto laiko skaičiavimo formulę. Štai formulė: Užduoties laikas = Bendrasis grupės laikas × (Įvertintas užduoties laikas ÷ Bendrasis įvertintas laikas)

| Užduotis   | Formulė           | Paskirstytas laikas |
|-------|-------------------|----------------|
| 1 užduotis | 6 × (1 ÷ 8) val. | 0,75 valandos      |
| 2 užduotis | 6 × (3 ÷ 8) val. | 2,25 valandos     |
| 3 užduotis | 6 × (4 ÷ 8) val. | 3,00 valandos     |

## <a name="jobs-allocation-key"></a>Užduočių paskirstymo raktas
Ši lentelė parodo paskirstyto laiko skaičiavimo formulę. Štai formulė: užduoties laikas = Bendrasis grupės laikas ÷ Užduočių skaičius

| Užduotis   | Formulė | Paskirstytas laikas |
|-------|---------|----------------|
| 1 užduotis | 6 ÷ 3   | 2 valandos        |
| 2 užduotis | 6 ÷ 3   | 2 valandos        |
| 3 užduotis | 6 ÷ 3   | 2 valandos        |

## <a name="net-time-allocation-key"></a>Grynojo laiko paskirstymo raktas
Ši lentelė parodo paskirstyto laiko skaičiavimo formulę. Štai formulė: Suskaičiuotas laikas pagal ataskaitą = Grupės laikas ÷ Užduočių skaičius

|                              | 09:00–10:00 (1 val.) | 10:00–11:00 (1 val.) | 11:00–13:00 (2 val.) | 13:00–15:00 (2 val.) | Paskirstytas laikas |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Grupės užduočių skaičius | 1                    | 3                    | 2                     | 1                     | Netaikoma |
| 1 užduotis                        | 1 ÷ 1 = 1 val.       | 1 ÷ 3 = 0,33 val.    | Netaikoma        | Netaikoma        | 1,33 valandos     |
| 2 užduotis                        | Netaikoma       | 1 ÷ 3 = 0,33 val.    | 2 ÷ 2 = 1 val.        | Netaikoma        | 1,33 valandos     |
| 3 užduotis                        | Netaikoma       | 1 ÷ 3 = 0,33 val.    | 2 ÷ 2 = 1 val.        | 2 ÷ 1 = 2 val.       | 3,33 valandos     |

## <a name="real-time-allocation-key"></a>Realiojo laiko paskirstymo raktas
Jei norite, kad gamybos išlaidos būtų apskaičiuotos remiantis realiomis išlaidomis, turite išvalyti pasirinktį **Išlaidų kategorija** puslapyje **Gamybos užsakymo numatytoji informacija**. Ši lentelė parodo paskirstyto laiko skaičiavimo formulę. Štai formulė: Faktinis užduoties laikas = Faktinis grupės laikas

| Užduotis   | Faktinis laikas |
|-------|-------------|
| 1 užduotis | 2 valandos     |
| 2 užduotis | 3 valandos     |
| 3 užduotis | 5 valandos     |

Tarkime, tris užduotis atlieka darbuotojas, kurio valandinis uždarbis yra 12,00 USD. Per laiką, kurį užtruko užduotims atlikti, neuždirbta jokių premijų už viršvalandžius ar priedų. Darbuotojas vykdė šias tris sugrupuotas užduotis šešias valandas. Todėl atlyginimo išlaidos yra 6 × 12,00 USD = 72,00 USD. Kai naudojate realiojo laiko paskirstymą, išlaidos už valandą perskaičiuojamos naudojant formulės Grynasis laikas koeficientą. Tada faktinis laikas, kurį užtruko kiekviena užduotis, perkeliamas kartu su ištaisyta valandos savikaina. Pavyzdys rodo, kad sugaištos šešios valandos, nors paskirstyta 10 valandų. Ši lentelė parodo savikainos skaičiavimo formulę. Štai formulė: savikaina už valandą = (Bendrasis grupės laikas vienai užduočiai (Grynasis laikas) ÷ Faktinis užduoties laikas) × Standartinė savikaina už valandą

| Užduotis   | Koreguotų išlaidų už valandą skaičiavimas | Koreguotos išlaidos už valandą | Paskirstytas laikas | Bendrosios užduoties išlaidos |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| 1 užduotis | (1,33 ÷ 2) × 12.00 USD                 | 8,00 USD                | 2 valandos        | 16,00 USD         |
| 2 užduotis | (1,33 ÷ 3) × 12.00 USD                 | 5,33 USD                | 3 valandos        | 16,00 USD         |
| 3 užduotis | (3,33 ÷ 5) × 12.00 USD                 | 8,00 USD                | 5 valandos        | 40,00 USD         |

Koreguotos išlaidos už valandą ir užduoties laikas registruojamas gamybos žurnale. **Pastaba:** jei pasirinksite pasirinktį **Išlaidų kategorija** skirtuke **Bendra**, esančiame puslapyje **Gamybos užsakymo numatytoji informacija**, faktinis kiekvienos užduoties laikas perkeliamas į gamybos žurnalą, kur savikaina taikoma konkrečios užduoties savikainos kategorijai.




