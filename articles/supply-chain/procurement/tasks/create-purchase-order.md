--- 
title: "Pirkimo užsakymo kūrimas"
description: "Šia procedūra parodoma, kaip rankiniu būdu kurti pirkimo užsakymą."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 27ed15e6d9a376c4203e5446d056f221bd3eb730
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra parodoma, kaip rankiniu būdu kurti pirkimo užsakymą. Pirkimo užsakymai dažniau kuriami automatiškai – atliekant bendrąjį planavimą, tiesioginį pristatymą ir kitus procesus. Pirkimo užsakymus paprastai kuria pirkimo agentas. Čia rodomą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF, naudojant įvairių veiksmų pastabose siūlomas reikšmes.


## <a name="create-the-purchase-order-header"></a>Pirkimo užsakymo antraštės kūrimas
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Pasirinkite tiekėjo sąskaitą US-101.
    * Pasirinkus tiekėją, į užsakymo antraštę kaip numatytosios reikšmės bus nukopijuota tokia tiekėjo įrašo informacija kaip adresas, SF sąskaita, pristatymo sąlygos ir pristatymo būdas. Šias reikšmes galima bet kada pakeisti.  
4. Išplėskite skyrių Bendra.
    * Lauke Vieta ir lauke Sandėlis nurodoma, kur reikia pristatyti įsigytas prekes ar paslaugas. Numatytasis pristatymo adresas yra vieta. Abu laukus galima užpildyti nustatytomis pasirinkto tiekėjo reikšmėmis, arba jas nustatyti galite rankiniu būdu.  
    * Laukas Pristatymo data naudojamas nurodyti, kada reikia pristatyti įsigytas prekes ir paslaugas. Galite nurodyti vieną užsakymo pristatymo datą, arba atskiroms užsakymo eilutėms galima nustatyti unikalias pristatymo datas. Jei konkrečių produktų ar paslaugų nepavyksta spėti pristatyti iki čia nurodytos pristatymo datos, nes jų vykdymo laikas ilgesnis, bus nustatyta vėlesnė tų eilučių pristatymo data, kad būtų galima spėti.  
5. Sutraukite dalį Bendra.
6. Išplėskite dalį Administravimas.
    * Lauką Užsakovas galima naudoti norint nurodyti, kas atlieka užsakymą. Jį gali būti patogu bendrinti su tiekėju – galbūt šiam reikės su tuo asmeniui susisiekti. Jei puslapyje Vartotojai dabartinio vartotojo paskyra susieta su vardu, šiam laukui reikšmę galima priskirti automatiškai.  
7. Sutraukite dalį Administravimas.
8. Spustelėkite GERAI.
    * Užsakymo antraštė sukurta. Kai dirbate su pirkimo užsakymo eilutėmis, rodoma tik antraštės informacijos suvestinė. Jei reikia peržiūrėti likusią informaciją, spustelėkite Antraštė.  

## <a name="add-a-purchase-order-line"></a>Pirkimo užsakymo eilutės įtraukimas
1. Spustelėkite Pirkimo užsakymo eilutė.
2. Spustelėkite Dimensijos.
    * Gali būti produktų variantų, skiriamų pagal dimensijas, pvz., spalvą, dydį ar stilių. Taip pat galima nustatyti, kad produktai naudotų saugojimo dimensijas, pvz., vietą ir sandėlį. Taip pat yra neprivalomų sekimo dimensijų, pvz., paketo ir serijos numeriai. Norėdami pagerinti užsakymų įvedimo efektyvumą, dažnai naudojamus dimensijų laukus galite įtraukti tiesiai į užsakymo tinklelį.  
3. Pažymėkite žymės langelį Spalva.
    * Neprivaloma. Jei pasirinksite lauką Įrašyti nustatymą, jūsų pasirinktos dimensijos užsakymo eilučių tinklelyje bus rodomos ir kitą kartą atidarius pirkimo užsakymų puslapį.  
4. Spustelėkite GERAI.
5. Lauke Prekės numeris pasirinkite T0004.
    * Produktų ir paslaugų užsakymo eilutės kuriamos nurodant prekės numerį, o kaip išlaidos – nurodant įsigijimo kategoriją.  
    * Laukas Įsigijimo kategorija naudojamas įtraukti eilutėms, kai įsigytos prekės į išlaidas nurašomos tiesiogiai, o ne perkeliamos į atsargas. Tai reiškia, kad, jei reikia į išlaidas nurašyti pirkimą, tai padaryti galite sukurdami pirkimo užsakymo eilutę, kurioje nurodoma įsigijimo kategorija, o ne kurdami eilutę su prekės numeriu. Prekes taip pat galima susieti su įsigijimo kategorija, ir šiuo atveju įsigijimo kategorija rodoma tik informaciniu tikslu.  
6. Lauke Spalva įveskite arba pasirinkite reikšmę.
    * Paprastai laukai Vieta ir Sandėlis užpildomi reikšmėmis iš užsakymo antraštės, tačiau, jei kai kurias eilutes reikia pristatyti į skirtingas vietas, galima šiuos laukus perrašyti.  
7. Lauke Kiekis įveskite skaičių.
    * Pasirinkite norimą pirkti kiekį. Jei nustatytas mažiausias užsakymo kiekis, laukas Kiekis automatiškai užpildomas juo, arba reikšme 1.  
    * Lauke Vienetas nurodomas užsakyto kiekio matavimo vienetas. Paprastai šis vienetas automatiškai pateikiamas iš produkto bendrųjų duomenų pirkimo vieneto, tačiau jį galite pakeisti.  
    * Lauke Vieneto kaina paprastai pateikiama reikšmė iš pirkimo sutarties arba prekybos sutarties. Atskirų užsakymo eilučių vieneto kainą galima keisti, pvz., jei su tiekėju suderama dėl unikalios kainos.  
    * Lauke Nuolaida nurodoma vieneto nuolaidos suma. Taigi ši nuolaida savo reikšme sumažina vieneto kainą. Paprastai ši nuolaida automatiškai pateikiama pirkimo sutartyse ar prekybos sutartyse, tačiau, jei su tiekėju suderėta dėl unikalių nuolaidų, jas atskirose eilutėse galima perrašyti.  
    * Galima įvesti nuolaidos procentą, kuriuo atitinkamai sumažinama grynoji eilutės suma. Dažnai nuolaidos procentas automatiškai pateikiamas pirkimo sutartyse ar prekybos sutartyse, tačiau, jei su tiekėju suderėta dėl unikalaus nuolaidos procento, jį atskirose eilutėse galima perrašyti.  
    * Lauko Grynoji suma reikšmė apskaičiuojama iš kitų eilutės laukų – kiekio, vieneto kainos, nuolaidos ir nuolaidos procento. Grynąją sumą galima pakeisti, tačiau tada laukai Vieneto kaina, Nuolaida ir Nuolaidos procentas bus tušti, ir, registruojant eilutėje, užregistruota suma bus proporcinga grynajai sumai. Paprastai laukas Grynoji suma naudojamas tik rodyti eilutės grynajai sumai.  
8. Išplėskite skyrių Eilutės informacija.
9. Spustelėkite skirtuką Pristatymas.
    * Kiekvienai užsakymo eilutei galima priskirti unikalią pristatymo datą. Ši data paveldima iš pirkimo užsakymo antraštės lauko, tačiau ją galite pakeisti.  
10. Sutraukite skyrių „Eilutės informacija“.

## <a name="review-order-totals"></a>Užsakymo bendrųjų sumų peržiūra
1. Spustelėkite Sumos.
    * Jei nematote veiksmo Bendrosios sumos, veiksmų juostoje spustelėkite skirtuką Pirkimo užsakymas.  
    * Šiame dialogo lange rodomos viso užsakymo bendrosios sumos.  
    * Lauku Pasirinkimas galima keisti, kaip apskaičiuojamos bendrosios sumos. Pavyzdžiui, galite pasirinkti Gavimo dokumento kiekis – bus rodomos bendrosios sumos, susijusios su gauto produkto (-ų) kiekiu, arba Užsakytas kiekis – bus rodomas užsakytas produkto kiekis.  
2. Spustelėkite GERAI.


