---
title: „Recency“, dažnumo ir piniginės (RFM) analizės nustatymas
description: Šioje temoje aiškinama, kaip nustatyti jūsų klientų „Recency“, dažnumo ir piniginę (RFM) analizę.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c7cb79fa82b579bee01e51cb635597cc5f711a98
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414422"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>„Recency“, dažnumo ir piniginės (RFM) analizės nustatymas

[!include [banner](includes/banner.md)]

Šioje temoje aiškinama, kaip nustatyti jūsų klientų „Recency“, dažnumo ir piniginę (RFM) analizę.

„Recency“, dažnumo ir piniginę (RFM) analizė yra rinkodaros įrankis, kurį jūsų organizacija gali naudoti generuojamiems klientų pirkimų duomenims įvertinti. Nustačius RFM analizę, klientams, kai šie perka, priskiriamas apskaičiuotas RFM rezultatas. RFM rezultatas gali būti trijų skaitmenų vertinimas arba sudėtinis numeris – tai priklauso nuo to, kaip jūsų organizacija sukonfigūravo RFM analizę. Toliau nurodyta, kaip skaičiuojamas įvertinimas, jei jūsų organizacija rezultatuose naudoja trijų skaitmenų vertinimą.

- Pirmasis skaitmuo yra kliento „recency“ vertinimas (kaip seniai klientas pirko iš jūsų organizacijos).
- Antrasis skaitmuo yra kliento pirkimų dažnio vertinimas (kaip dažnai klientas perka iš jūsų organizacijos).
- Trečiasis skaitmuo yra kliento piniginės vertės vertinimas (kiek klientas išleidžia, pirkdamas iš jūsų organizacijos).

Pavyzdžiui, jūsų organizacija vertinimus nustato skalėje nuo 1 iki 5, kai 5 yra aukščiausias vertinimas. Šiuo atveju 535 kliento vertinimas nurodo toliau pateiktą informaciją apie klientą.

- **„Recency“ vertinimas 5** – klientas pastaruoju metu pirko.
- **Dažnumo vertinimas 3** – klientas gana dažnai perka produktus iš jūsų organizacijos.
- **Piniginės vertės vertinimas 5** – pirkdamas klientas išleidžia didelę pinigų sumą.

Jei jūsų organizacija naudoja sudėtinį rezultatų numerį, atskiri vertinimai sudedami. Naudojant tą patį pavyzdį kliento vertinimas yra 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Savo organizacijos klientų RFM analizės nustatymas

1. Pasirinkite **Skambučių centras** \> **Laikotarpio** \> **RFM analizė**.
2. Puslapyje **RFM analizė** pasirinkite **Nauja**. Lauke **RFM aprašas** įveskite RFM aprašo pavadinimą. Pavyzdžiui, aprašą galite pavadinti RFM-A.
3. Įveskite šio RFM aprašo pradžios ir pabaigos datas.
4. „FastTab“ **General** atlikite toliau nurodytus veiksmus.

    - Jei, skaičiuojant kiekvieną RFM rezultato dalį, turi būti naudojamas tas pats klientų skaičius, pažymėkite žymės langelį **Tolygus paskirstymas**.
    - Norėdami sudėti tris rezultatus, pažymėkite žymės langelį **Sudėti rezultatus**. Tuomet, pavyzdžiui., kliento RFM rezultatas būtų 13, o ne 535.
    - Norėdami, kad sistema būtinai išsaugotų klientų statistinius duomenis, pažymėkite žymės langelį **Įrašyti retrospektyvą** – tuomet duomenys galės būti naudojami RFM rezultatui apskaičiuoti.

5. „FastTab“ **Recency** atlikite toliau nurodytus veiksmus.

    - Lauke **Padaliniai** įveskite daliklių arba grupių numerį, kuris bus naudojamas klientų „recency“ rezultatui apskaičiuoti. Pavyzdžiui, jei turite 100 klientų, daliklis 5 reiškia, kad kiekvienam rezultatui sudaryti tenka 20 klientų. 20 vėliausiai pirkusių klientų „recency“ rezultatas bus 5. Kitų 20 klientų „recency“ rezultatas – 4, ir t. t. Jei turite 50 klientų, 10 klientų „recency“ rezultatas bus 5, 10 klientų – 4, ir t. t.
    - Lauke **Prioritetas** pasirinkite, kokią reikšmę, skaičiuojant kliento RFM rezultatą, suteiksite „recency“ parametrui kitų parametrų atžvilgiu. Pavyzdžiui, „recency“ rezultatą galite įvertinti didesne verte nei piniginės išraiškos rezultatą.
    - Lauke **Daugiklis** įveskite vertę, iš kurios bus padaugintas „recency“ rezultatas. Jei neįvesite vertės, rezultatas nebus padaugintas.
    - Lauke **Laikotarpis** pasirinkite laikotarpį, pagal kurį skaičiuojamas „recency“ rezultatas. Pavyzdžiui, pagal savaitę arba pagal mėnesį.

6. „FastTab“ **Dažnis** atlikite toliau nurodytus veiksmus.

    - Lauke **Padaliniai** įveskite daliklių arba grupių numerį, kuris bus naudojamas klientų dažnio rezultatui apskaičiuoti.
    - Lauke **Prioritetas** pasirinkite, kokią reikšmę, skaičiuojant kliento RFM rezultatą, suteiksite dažnio parametrui kitų parametrų atžvilgiu.
    - Lauke **Daugiklis** įveskite vertę, iš kurios bus padaugintas dažnio rezultatas. Jei neįvesite vertės, rezultatas nebus padaugintas.

7. „FastTab“ **Piniginė išraiška** atlikite toliau nurodytus veiksmus.

    - Lauke **Padaliniai** įveskite daliklių arba grupių numerį, kuris bus naudojamas klientų piniginės išraiškos rezultatui apskaičiuoti.
    - Lauke **Prioritetas** pasirinkite, kokią reikšmę, skaičiuojant kliento RFM rezultatą, suteiksite piniginės išraiškos parametrui kitų parametrų atžvilgiu.
    - Lauke **Daugiklis** įveskite vertę, iš kurios bus padaugintas piniginės išraiškos rezultatas. Jei neįvesite vertės, rezultatas nebus padaugintas.
    - Lauke **Bruto / grynoji** pasirinkite, ar kliento piniginės išraiškos rezultatas turi būti apskaičiuojamas naudojant bruto arba grynąją SF sumą.
    - Jei grąžintinas klientui sumas reikia atimti iš kliento SF bendrosios apskaičiuotos sumos, pažymėkite žymės langelį **Atimti grąžinimus**.

## <a name="view-a-customers-rfm-score"></a>Kliento RFM rezultato peržiūra

Naudokite šią procedūrą norėdami peržiūrėti kliento RFM rezultatą.

1. Pasirinkite **Skambučių centras** \> **Žurnalai** \> **Klientų aptarnavimas**.
2. Puslapio **Klientų aptarnavimas** srities **Klientų aptarnavimas** ieškos laukuose, pasirinkite norimo ieškoti raktažodžio tipą ir įveskite ieškos tekstą.
3. Pasirinkite **Ieškoti**.
4. Puslapyje **Kliento ieška** pasirinkite norimą kliento įrašą ir tada spustelėkite **Pasirinkti klientą**.

RFM rezultatas rodomas grupėje **Užsakymų retrospektyva**, esančioje dešinėje puslapio **Klientų aptarnavimas** pusėje.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>RFM analizės įrašo retrospektyvos peržiūra arba valymas

Naudokite šią procedūrą norėdami peržiūrėti arba išvalyti RFM analizės įrašo retrospektyvą.

1. Pasirinkite **Skambučių centras** \> **Laikotarpio** \> **RFM analizė**.
2. Puslapyje **RFM analizė** pasirinkite norimą peržiūrėti įrašą.
3. Norėdami peržiūrėti įrašo retrospektyvą, pasirinkite „FastTab“**Retrospektyva**.
4. Norėdami išvalyti įrašo retrospektyvą, pasirinkite **Išvalyti retrospektyvą**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]