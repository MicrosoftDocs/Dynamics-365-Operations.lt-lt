---
title: "Užsakymo pranešimų rodymas elektroniniame kasos aparate"
description: "Šioje temoje aprašyta, kaip įjungti užsakymo pranešimų rodymą elektroniniame kasos aparate ir pranešimų sistemoje, kurią galima išplėsti į kitas operacijas."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Pranešimų rodymas elektroniniame kasos aparate

Šiandieninėje modernios mažmeninės prekybos aplinkoje parduotuvės atstovams priskiriamos įvairios užduotys, pvz., pagalba klientams, operacijų įvedimas, inventorizacijos atlikimas ir užsakymų parduotuvėje priėmimas. Elektroninio kasos aparato (EKA) klientas atstovams suteikia galimybę atlikti šias ir kitas užduotis vienoje programoje. Atstovams, turintiems atlikti įvairias dienos užduotis, gali reikėti pranešti, kada kam reikia skirti dėmesio. EKA pranešimų sistema šią problemą išsprendžia suteikdama mažmenininkams galimybę konfigūruoti pranešimus pagal vaidmenį. Įdiegus „Dynamics 365 for Retail“ su 5 programos naujiniu, galima konfigūruoti šiuos EKA operacijų pranešimus.

Šiuo metu sistema suteikia galimybę rodyti užsakymo įvykdymo operacijos pranešimus, tačiau sistema sukurta taip, kad ją būtų galima išplėsti – kad ateityje kūrėjai galėtų rašyti pranešimų apdorojimo programą, skirtą bet kuriai operacijai, ir rodyti pranešimus EKA.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Užsakymo įvykdymo operacijų pranešimų įjungimas

Norėdami įjungti užsakymo įvykdymo operacijų pranešimus, peržiūrėkite toliau nurodytus veiksmus.

 - Atidarykite puslapį **Operacijos** (**Mažmeninė prekyba** > **Kanalo sąranka** > **EKA sąranka** > **EKA** > **Operacijos**).
 - Raskite užsakymo įvykdymo operaciją ir pasirinkite šios operacijos žymės langelį **Įjungti pranešimus**. Tokiu būdu pranešimų sistemai nurodysite klausyti užsakymo įvykdymo operacijos apdorojimo programos. Jei apdorojimo programa įdiegta, pranešimai bus rodomi EKA, kitu atveju šios operacijos pranešimai nebus rodomi.
- Pasirinkite su darbuotojais susijusias EKA teises „FastTab“ **Pranešimai** įtraukite užsakymo įvykdymo operaciją, parinktį Rodymo tvarka nustatydami į parametrą 1. Kai sukonfigūruotas daugiau nei vienas pranešimas, rodymo tvarka naudojama pranešimo iš viršaus į apačią išdėstyti, 1 pateikiant viršuje. Galima įtraukti tik tas operacijas, kurių žymės langelis **Įjungti pranešimus** pažymėtas. Be to, bus rodomi pranešimai, skirti tik operacijoms, kurios buvo įtrauktos čia, ir tik darbuotojams, kurių operacijos įtrauktos į atitinkamas EKA teises. 

> [!NOTE]
> Pranešimus galima perrašyti vartotojo lygmeniu, atidarant darbuotojo įrašą ir pasirenkant **EKA teisės**, tada redaguojant to vartotojo pranešimų prenumeratą.

 - Atidarykite puslapį **Funkcijų šablonas** (**Mažmeninė prekyba** > **Kanalo sąranka** > **EKA sąranka** > **EKA profiliai** > **Funkcijų šablonai**). Atnaujinkite ypatybę **Pranešimų intervalas** ir nustatykite minučių intervalą, pagal kurį pranešimai turėtų būti rodomi. Rekomenduojame nustatyti šią reikšmę į 10 minučių, kad išvengtumėte nereikalingo ryšio su būstine. Nustačius pranešimų intervalą į 0, pranešimai bus išjungti.  

 - Pasirinkite **Mažmeninė prekyba** > **Mažmeninės prekybos IT** > **Paskirstymo grafikas**. Pasirinkite grafiką 1060 – darbuotojai, kad sinchronizuotumėte pranešimų prenumeratos parametrus, tada spustelėkite **Vykdyti dabar**. Tada sinchronizuokite teisių intervalą, pasirinkdami 1070 – kanalo konfigūravimas, ir spustelėkite **Vykdyti dabar**. 

## <a name="view-notifications-in-pos"></a>Pranešimų peržiūra EKA

Atlikę pirmiau aprašytus veiksmus, darbuotojai, kurių pranešimai nustatyti, gali peržiūrėti pranešimus EKA. Norėdami peržiūrėti pranešimus, spustelėkite pranešimo piktogramą EKA antraštės juostoje. Bus parodytas pranešimų centras ir užsakymo įvykdymo operacijos pranešimai. Pranešimų centras užsakymo įvykdymo operacijoje turėtų rodyti toliau nurodytas grupes. 

- **Laukiantys užsakymai** – šioje grupėje rodomas užsakymų, kurie yra laukimo būsenos, skaičius; pvz., užsakymų, kuriuos turi priimti EKA darbuotojas, turintis reikiamas parduotuvės vykdymo teises. Spustelėjus grupėje pateiktą skaičių, bus atidarytas puslapis **Užsakymų įvykdymas**, kuris filtruojamas rodyti tik vykdytinus laukiančius užsakymus, priskirtus parduotuvei. Jei parduotuvės užsakymai priimami automatiškai, tada šioje grupėje pateiktas skaičius lygus nuliui.

- **Paėmimas parduotuvėje** – šioje grupėje rodomas užsakymų, kurių pristatymo būdas **Paėmimas**, o paėmimas suplanuotas dabartinėje parduotuvėje, skaičius. Spustelėjus grupėje pateiktą skaičių, bus atidarytas puslapis **Užsakymų įvykdymas**, kuris filtruojamas rodyti aktyvius užsakymus, kurie nustatyti paimti iš dabartinės parduotuvės.

- **Siųsti iš parduotuvės** – šioje grupėje rodomas užsakymų, kurių pristatymo būdas **Siuntimas**, o siuntimas suplanuotas dabartinėje parduotuvėje, skaičius. Spustelėjus grupėje pateiktą skaičių, bus atidarytas puslapis **Užsakymų įvykdymas**, kuris filtruojamas rodyti aktyvius užsakymus, kurie nustatyti siųsti iš dabartinės parduotuvės.

Kai parduotuvei priskirti nauji vykdytini užsakymai, pranešimo piktograma pasikeis ir nurodys, kad yra naujų pranešimų, o atitinkamose grupėse rodomas skaičius bus atnaujintas. Vartotojas taip pat gali spustelėti atnaujinimo piktogramą, esančią šalia operacijos pavadinimo, kad iš karto atnaujintų grupėse pateiktą skaičių. Be to, skaičius bus atnaujintas iš anksto nustatytu intervalu. Bet kurioje grupėje, kurioje yra nauja dabartinio darbuotojo nematyta prekė, bus rodoma sprogimo piktograma, nurodanti, kad šioje grupėje yra nauja prekė. Spustelėjus plyteles pranešimuose bus atidaryta konkreti operacija, kuriai priskirtas ir sukonfigūruotas tas pranešimas. Aukščiau aprašytais atvejais spustelėjus pranešimus bus atidarytas puslapis **Užsakymų įvykdymas** ir perduoti atitinkami parametrai: laukiantys užsakymai, paėmimas parduotuvėje ir siuntimas iš parduotuvės. 

> [!NOTE]
> Laukiančių užsakymų pranešimai bus įjungti būsimame „Dynamics 365 for Retail“ naujinyje. 


