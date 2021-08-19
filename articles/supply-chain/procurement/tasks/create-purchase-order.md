---
title: Pirkimo užsakymo kūrimas
description: Šioje temoje parodyta, kaip kurti pirkimo užsakymą rankiniu būdu.
author: kamaybac
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f55e7d59f0e228b5642148540946b2ed0a589fb842b60b7613e20ad893476ccc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720329"
---
# <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje parodyta, kaip kurti pirkimo užsakymą rankiniu būdu. Pirkimo užsakymai dažniau kuriami automatiškai – atliekant bendrąjį planavimą, tiesioginį pristatymą ir kitus procesus. Pirkimo užsakymus paprastai kuria pirkimo agentas. Čia rodomą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF, naudojant įvairių veiksmų pastabose siūlomas reikšmes.


## <a name="create-the-purchase-order-header"></a>Pirkimo užsakymo antraštės kūrimas
1. Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Pasirinkti tiekėjo klientą **US-101**. Pasirinkus tiekėją, į užsakymo antraštę kaip numatytosios reikšmės bus nukopijuota tokia tiekėjo įrašo informacija kaip adresas, SF sąskaita, pristatymo sąlygos ir pristatymo būdas. Šias reikšmes galima bet kada pakeisti.  
4. Išplėskite skyrių **Bendra**.

    - Laukuose **Vieta** ir **Sandėlis** nurodoma, kur pristatyti įsigytas prekes ar paslaugas. Numatytasis pristatymo adresas yra vieta. Abu laukus galima užpildyti nustatytomis pasirinkto tiekėjo reikšmėmis, arba jas nustatyti galite rankiniu būdu.  
    - Laukas **Pristatymo data** naudojamas norint nurodyti, kada įsigytas prekes ir paslaugas reikia pristatyti, Galite nurodyti vieną užsakymo pristatymo datą, arba atskiroms užsakymo eilutėms galima nustatyti unikalias pristatymo datas. Jei konkrečių produktų ar paslaugų nepavyksta spėti pristatyti iki čia nurodytos pristatymo datos, nes jų vykdymo laikas ilgesnis, bus nustatyta vėlesnė tų eilučių pristatymo data, kad būtų galima spėti.  

5. Išplėskite skyrių **Administravimas**. Lauką **Užsakytojas** galima nurodyti, kas pateikė užsakymą. Jį gali būti patogu bendrinti su tiekėju – galbūt šiam reikės su tuo asmeniui susisiekti. Laukui reikšmė gali būti priskirta automatiškai, jei esamas vartotojo klientas yra susietas su vardu puslapyje **Vartotojai**.  
6. Pasirinkite **Gerai**. Užsakymo antraštė sukurta. Kai dirbate su pirkimo užsakymo eilutėmis, rodoma tik antraštės informacijos suvestinė. Jei reikia peržiūrėti likusią informaciją, pažymėkite **Antraštė**.  

## <a name="add-a-purchase-order-line"></a>Pirkimo užsakymo eilutės įtraukimas
1. Pasirinkite **„Pirkimo užsakymo eilutė“**.
2. Pasirinkite **Dimensijos**. Gali būti produktų variantų, skiriamų pagal dimensijas, pvz., spalvą, dydį ar stilių. Taip pat galima nustatyti, kad produktai naudotų saugojimo dimensijas, pvz., vietą ir sandėlį. Taip pat yra neprivalomų sekimo dimensijų, pvz., paketo ir serijos numeriai. Norėdami pagerinti užsakymų įvedimo efektyvumą, dažnai naudojamus dimensijų laukus galite įtraukti tiesiai į užsakymo tinklelį.  
3. Pažymėkite žymės langelį **Spalva**. Arba, jei pažymite lauką **Įrašyti sąranką**, pasirinkti matmenys taip pat bus rodomi užsakymo eilutės tinklelyje, kai kitą kartą atidarysite pirkimo užsakymo puslapį.  
4. Pasirinkite **Gerai**.
5. Lauke **Prekės numeris** pasirinkite **T0004**.

    - Produktų ir paslaugų užsakymo eilutės kuriamos nurodant prekės numerį, o kaip išlaidos – nurodant įsigijimo kategoriją. 
    - Kategorijos laukas **Įsigijimas** naudojamas norint įtraukti eilučių, kuriose įsigyti elementai yra įkainojami tiesiogiai, o ne einant į atsargas. Tai reiškia, kad, jei reikia į išlaidas nurašyti pirkimą, tai padaryti galite sukurdami pirkimo užsakymo eilutę, kurioje nurodoma įsigijimo kategorija, o ne kurdami eilutę su prekės numeriu. Prekes taip pat galima susieti su įsigijimo kategorija, ir šiuo atveju įsigijimo kategorija rodoma tik informaciniu tikslu.  

6. Lauke **Spalva** įveskite arba pasirinkite reikšmę. Laukuose **Vieta** ir **Sandėlis** paprastai įrašytos reikšmės iš užsakymo antraštės, tačiau laukus galima perrašyti, jei kai kurias eilutes reikia pristatyti į skirtingas vietas.  
7. Lauke **Kiekis** įveskite skaičių.

    - Pasirinkite norimą pirkti kiekį. Laukas **Kiekis** automatiškai užpildomas minimaliu produkto užsakymo kiekiu, jei tai yra nustatyta, arba įrašoma reikšmė 1.  
    - Laukas **Vienetas** nurodo užsakyto kiekio matavimo vienetą. Paprastai šis vienetas automatiškai pateikiamas iš produkto bendrųjų duomenų pirkimo vieneto, tačiau jį galite pakeisti.  
    - Lauke **Vieneto kaina** paprastai nurodyta vertė arba iš pirkimo sutarties, arba iš prekybos sutarties. Atskirų užsakymo eilučių vieneto kainą galima keisti, pvz., jei su tiekėju suderama dėl unikalios kainos.  
    - Lauke **Nuolaida** pateikiama vieneto nuolaidos suma. Taigi ši nuolaida savo reikšme sumažina vieneto kainą. Paprastai ši nuolaida automatiškai pateikiama pirkimo sutartyse ar prekybos sutartyse, tačiau, jei su tiekėju suderėta dėl unikalių nuolaidų, jas atskirose eilutėse galima perrašyti.  
    - Galima įvesti nuolaidos procentą, kuriuo atitinkamai sumažinama grynoji eilutės suma. Dažnai nuolaidos procentas automatiškai pateikiamas pirkimo sutartyse ar prekybos sutartyse, tačiau, jei su tiekėju suderėta dėl unikalaus nuolaidos procento, jį atskirose eilutėse galima perrašyti.  
    - Reikšmė lauke **Neto suma** apskaičiuojama iš kitų eilutės laukų, įskaitant kiekio, vieneto kainos, nuolaidos ir nuolaidos procento. Galima keisti neto sumą, tačiau tada laukai **Vieneto kaina**, **Nuolaida** ir **Nuolaidos kodas** bus tušti ir kai registruosite eilutę, užregistruota suma bus proporcinga neto sumai. Paprastai, laukas **Neto suma** naudojamas rodyti neto sumos eilutę.  

8. Išplėskite skyrių **Eilutės informacija** section.
9. Pažymėkite skirtuką **Pristatymas**. Kiekvienai užsakymo eilutei galima priskirti unikalią pristatymo datą. Ši data paveldima iš pirkimo užsakymo antraštės lauko, tačiau ją galite pakeisti.  

## <a name="review-order-totals"></a>Užsakymo bendrųjų sumų peržiūra
1. Pasirinkite **Bendrosios sumos**.

    - Jei nematote veiksmo **Bendrosios sumos**, veiksmų srityje pažymėkite skirtuką **Pirkimo užsakymas**.  
    - Šiame dialogo lange rodomos viso užsakymo bendrosios sumos.  
    - Laukas **Pasirinkimas** leidžia keisti pagrindą, pagal kurį skaičiuojamos bendrosios sumos. Pavyzdžiui, galite pasirinkti **Produkto gavimo kiekis**, kad būtų rodomos bendrosios sumos, susijusios su gauto (-ų) produkto (-ų) kiekiu, arba **Užsakytas kiekis**, kad būtų rodomas užsakytas produkto kiekis.  

2. Pasirinkite **Gerai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]