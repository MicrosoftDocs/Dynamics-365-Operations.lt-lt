---
title: Generuoti ir apdoroti kliento grąžinimus
description: Ši procedūra parodo, kaip apdoroti klientų grąžinimus nuo pretenzijos generavimo iki susikaupusių gautinų sumų išmokėjimo.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage, MCRBrokerWriteOffReason, MRCHierarchyAddCust, PdsItemRebateGroup, PdsRebate, PdsRebateProgramTMATable, PdsRebateTable, PdsRebateTableListPagePreviewPane, PdsRebateTrans, PdsRebateType_CustLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a85c027571a6d77ed61cd874bb9d97221b099967
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969092"
---
# <a name="generate-and-process-customer-rebates"></a>Generuoti ir apdoroti kliento grąžinimus

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip apdoroti klientų grąžinimus nuo pretenzijos generavimo iki susikaupusių gautinų sumų išmokėjimo. Ji žingsnis po žingsnio pateikia konkretų pavyzdį, kuris paaiškina, kokią įtaką įvairios grąžinimo eilučių sąlygos daro galutinėms sumoms, kurios bus pervestos klientui. Turėsite naudoti demonstracinių duomenų įmonę USMF ir, prieš paleisdami vadovą, atlikti šias užduotis: (1) eikite į puslapį „Gautinų sumų parametrai“, išplėskite skirtuką „Kainos“, tada skirtuką „Kainų informacija“ ir patikrinkite, ar parinkčiai „Įjungti kainų informaciją“ nustatyta reikšmė „Taip“. (2) Eikite į puslapį „Grąžinimo sutartys“ ir pasirinkite grąžinimo klientui sutartį: USMF-000001. Jei darbo eigos patvirtinimo būsenos laukui nenustatyta reikšmė „Patvirtinta“, turite jį patvirtinti veiksmų srityje spustelėdami „Patvirtinimas“.


## <a name="review-a-customer-rebate-agreement"></a>Peržiūrėti kliento grąžinimo sutartį
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Grąžinimai klientams > Grąžinimo sutartys**.
    - Kiti keli veiksmai skirti sutarties USMF-000001 sąlygų peržiūrai. Tai leidžia lengviau suprasti, kaip atliekant vėlesnius procedūros veiksmus skaičiuojamos kliento kredito reikšmės.  
    - Ši sutartis skirta atskiram klientui, šiame pavyzdyje – klientui US-009.  
    - Klientui nusipirkus konkretų produktą, jam gali būti grąžinama už jį sumokėta suma. Šiuo atveju prekės numeris T0020.   
    - Kliento pardavimo našumas, pagal kurį įvertinamos grąžinamos sumos, turi būti įvertinamas kiekvieną savaitę.  
    - Parametras „Kaina paimta iš“ yra bruto, o tai reiškia, kad iš eilutės pardavimo sumos, kurios pagrindu įvertinama pretenzija, nėra išskaičiuojama eilutės nuolaida.  
    - Lauke „Grąžinimo eilutės ribos tipas“ nurodomas grąžinimų skaičiavimo metodas. Šiuo atveju pardavimo tikslas, pagal kurį įvertinami grąžinimai, yra nustatytas kaip „Kiekis“.   
    - Sutarties eilutės nurodo grąžinimo sumos tipą, faktinę grąžinimo vertę ir ribines reikšmes. Šiame pavyzdyje klientui bus grąžinami 20 USD nuo parduoto vieneto, jei kiekvieną savaitę jis įsigija nuo 1 iki 50 vienetų produkto; ir bus grąžinami 40 USD nuo parduoto vieneto, jei nupirks daugiau nei 50 vienetų.  
2. Uždarykite puslapį.

## <a name="generate-rebate-claims"></a>Generuoti grąžinimo pretenzijas
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Spustelėkite **Naujas**. Siekiant imituoti grąžinimo pretenzijų generavimo būdą, kita užduotis yra sukurti pardavimo užsakymą, kur produktas ir kiekis leis klientui atitikti grąžinimo reikalavimus.    
3. Lauke **Kliento sąskaita** įveskite arba pasirinkite reikšmę.
4. Spustelėkite **Gerai**.
5. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
6. Nustatykite **Kiekis** lauke „40“.
7. Skyriuje **Pardavimo užsakymo eilutės** spustelėkite **Pardavimo užsakymo eilutė**.
8. Spustelėkite **Kainos informacija**. Jei nematote šios parinkties, vadinasi, prieš pradėdami naudotis vadovu nenustatėte parinkties **Įjungti kainų informacijos parinktį** reikšmės „Taip“.     
9. Išplėskite skyrių **Grąžinimai**. Skirtuke **Grąžinimai** išvardijamos visos grąžinimo sutartys, taikomos esamo užsakymo eilutei, ir parodyta numatoma grąžinimo suma. Atkreipkite dėmesį, kad rodomos sumos yra tik pavyzdžiai, kokių grąžinimo pretenzijų galima sulaukti ateityje. Faktinės grąžinimo sumos gali skirtis priklausomai nuo: bendrų pardavimų apimčių, kurias klientas pasiekė pagal periodinę grąžinimo sutartį; ar klientas grąžino visą, ar dalį kiekio; ir ar buvo išrašyta galiojanti sąskaita faktūra už pardavimo užsakymą.
10. Uždarykite puslapį.
11. Spustelėkite **Pridėti eilutę**.
12. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
13. Nustatykite **Kiekis** lauke „60“.
14. Spustelėkite **Įrašyti**.
15. **Veiksmų sritis** spustelėkite **Sąskaita faktūra**.
16. Spustelėkite **Sąskaita faktūra**.
17. Išplėskite skyrių **Parametrai**.
18. Lauke **Kiekis** pasirinkite „Visi‟.
19. Spustelėkite **Gerai**.
20. Spustelėkite **Gerai**.

## <a name="process-rebate-claims"></a>Grąžinimo pretenzijų apdorojimas
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Grąžinimai klientams > Grąžinimai**.
    - Puslapyje „Grąžinimai“ veikia darbo sritis, kurioje galite peržiūrėti, patvirtinti ir apdoroti grąžinimo pretenzijas. Dabar apdorosite pretenzijas, kurios buvo sukurtos išrašius SF pagal pardavimo užsakymą klientui US-009, kuris yra grąžinimo sutarties USMF-000001 subjektas.   
    - Pirmoji eilutė yra 800 USD grąžinimo pretenzija, pagrįsta 40 vienetų produkto T0020 pardavimu – po 20 USD už vienetą. Tai atitinka pirmosios kiekio ribos sąlygas grąžinimo sutartyje.  
    - Antroji pretenzija yra 2400 USD, pagrįsta 60 vienetų produkto T0020 pardavimu – po 40 USD už vienetą, pagal antrąją kiekio ribą, nustatytą sutartyje.  
    - Abiejų pretenzijų būsena yra „Apskaičiuotina“. Tai reiškia, kad jos yra susietos su sutartimi, kuri periodiškai seka kliento pardavimo našumą, ir kad jos turi būti perskaičiuojamos, įvertinant bendrą pardavimų kiekį per atitinkamą laikotarpį.   
2. Spustelėkite **Kaupti**.
3. Lauke **Klientas** įveskite arba pasirinkite reikšmę.
4. Lauke **Pradžios data** pasirinkite šiandienos datą.
5. Spustelėkite **Gerai**. Įvykdžius funkciją **Kaupti**, numatoma pretenzijos suma koreguojama atsižvelgiant į tai, kad kliento bendras pardavimų kiekis per atitinkamą laikotarpį yra didesnis nei tuomet, kai buvo generuojama pirmoji grąžinimo suma. Tiksliau sakant, bendras nupirktas kiekis pasiekė 100 vienetų, todėl dabar klientas gali gauti 40 USD už vienetą (pagal sutarties antrąją kiekio ribą) arba 4,000 USD bendrą grąžinimo sumą. Skirtumas įrašomas kaip nauja pretenzijos „korekcija“ dėl papildomų 800 USD. Grąžinimo pretenzijų, kurios buvo įtrauktos į kaupimo atnaujinimą, būsena dabar yra „Apskaičiuota“. 
6. Sąraše pažymėkite visas eilutes.
7. Spustelėkite **Patvirtinti**.
8. Spustelėkite **Apdoroti**.
9. Lauke **Klientas** įveskite arba pasirinkite reikšmę.
10. Spustelėkite **Gerai**. Pranešimas rodo, kad grąžinimas buvo sėkmingai apdorotas, ir pretenzijų būsena pakeista į „Žymėti“. Tai reiškia, kad užregistravus grąžinimo kaupimo žurnalą:
    - paraiškos buvo perkeltos į laikiną kliento balansą kaip atskaitymai;
    - į grąžinimo kaupimo sąskaitą įskaitytos lėšos siekiant nurodyti būsimą įsipareigojimą klientui;
    - iš grąžinimo išlaidų sąskaitos atskaitytos lėšos siekiant nurodyti išlaidas, kurios buvo patirtos parduodant.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
