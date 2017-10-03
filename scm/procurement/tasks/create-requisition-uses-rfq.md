--- 
title: "Kurti paraišką, kurioje naudojamas RFQ"
description: "Šiame vedlyje parodoma, kaip iš RFQ proceso kainos ir tiekėjo informaciją įtraukti į pirkimo paraišką."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 14eed7982041b7af7dad5453b10f07f063ba1855
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Kurti paraišką, kurioje naudojamas RFQ

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šiame vedlyje parodoma, kaip iš RFQ proceso kainos ir tiekėjo informaciją įtraukti į pirkimo paraišką. Šiame vedlyje pateiktą pavyzdį galite naudoti demonstracinių duomenų įmonėje USMF, o norėdami atlikti visus veiksmus turite būti prisijungęs kaip Administratorius. Paprastai šio vedlio užduotis atlieka įsigijimo specialistai.


## <a name="create-a-requisition"></a>Kurti paraišką
1. Pasirinkite Pirkimai ir tiekėjų parinkimas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke „Pageidaujama data“ įveskite datą.
5. Lauke „Apskaitos data“ įveskite datą.
6. Spustelėkite Gerai.
7. Lauke Priežastis įveskite arba pasirinkite vertę.
8. Spustelėkite Pridėti eilutę.
9. Lauke Įsigijimo kategorija pasirinkite kategoriją medyje ir tada spustelėkite Gerai.
10. Lauke „Produkto pavadinimas“ įveskite reikšmę.
11. Lauke Kiekis įveskite skaičių.
12. Lauke Vienetas įveskite arba pasirinkite reikšmę.
13. Spustelėkite Įrašyti.
14. Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.
15. Spustelėkite Pateikti.
16. Uždarykite puslapį.
17. Spustelėkite Pateikti.

## <a name="reassign-a-workflow-task"></a>Iš naujo priskirti darbo eigos užduotį
    * Kitos užduoties metu kuriamas RFQ, siekiant gauti tiekėjų kainų pasiūlymus už produktą. USMF demonstraciniuose duomenyse paraiškos darbo eiga nustatoma naudojant taisyklę, pagal kurią RFQ kūrimo užduotis priskiriama konkrečiam darbuotojui, jei nėra pasirinktas tiekėjas arba jei eilutės vieneto kaina yra 0. Norėdami toliau vykdyti šio vedlio užduotis, tą užduotį turite priskirti kitam vartotojui (sau). Tai galite atlikti tik jei esate prisijungęs kaip Administratorius.  
1. Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.
2. Spustelėkite Peržiūrėti retrospektyvą.
3. Atnaujinkite puslapį.
4. Išplėskite sekciją Sekimo informacija.
5. Medyje pasirinkite eilutę, kuri prasideda „Eilutės darbo eiga suaktyvinta“.
6. Spustelėkite Peržiūrėti darbo eigos informaciją.
7. Išplėskite sekciją Darbo elementai.
8. Spustelėkite Priskirti iš naujo.
9. Lauke Vartotojas pasirinkite Administratorius.
10. Spustelėkite Priskirti iš naujo.
11. Uždarykite puslapį.
12. Uždarykite puslapį.

## <a name="create-an-rfq"></a>Kurti RFQ
1. Atnaujinkite puslapį.
2. Spustelėkite Pasiūlymo patvirtinimas.
3. Lauke Perkantis juridinis subjektas pasirinkite USMF.
    * Turite pasirinkti tokį patį juridinį subjektą, koks nurodytas paraiškos eilutėje.  
4. Sąraše pažymėkite pasirinktą eilutę.
    * Jei pirkimo paraiškoje yra kelios eilutės, pasirinkite visas eilutes, kurias norite įtraukti į RFQ.  
5. Spustelėkite GERAI.
6. Atnaujinkite puslapį.
7. Atidarykite „FactBox“ ir tada išplėskite sekciją Susiję dokumentai.
    * Gali būti, kad „FactBox“ jau atidarytas. Jame suraskite piktogramą su rodykle (dešinėje eilučių / antraštės perjungimo mygtukų pusėje). Jei rodyklė rodo į dešinę, „FactBox“ jau atidarytas. Jei rodyklė rodo į kairę, spustelėkite ją, kad atidarytumėte „FactBox“.  
8. Spustelėkite lauko Pasiūlymo patvirtinimas saitą, kad atidarytumėte ką tik sukurtą RFQ.
9. Spustelėkite Antraštė.
10. Spustelėkite Pridėti.
11. Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.
12. Spustelėkite Pridėti.
13. Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.
14. Spustelėkite Siųsti.
15. Spustelėkite GERAI.
16. Spustelėkite Įvesti atsakymą.
17. Veiksmų srityje spustelėkite Atsakymas.
18. Spustelėkite Kopijuoti duomenis į atsakymą.
    * Tokiu būdu iš RFQ į atsakymą nukopijuojami duomenys, pvz., kiekis ir datos.  
19. Lauke Vieneto kaina įveskite skaičių.
    * Tai yra kaina, gauta iš tiekėjo. Galbūt taip pat norėsite įvesti papildomą tiekėjo informaciją.  
20. Spustelėkite Priimti.
21. Spustelėkite GERAI.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Patikrinti, ar tiekėjas ir kaina perkelti į paraišką
1. Uždarykite puslapį.
2. Spustelėkite Eilutės.
3. Spustelėkite Susijusi informacija.
4. Spustelėkite Pirkimo paraiška.
5. Pasirinkite eilutę, kuri buvo perkelta į RFQ.
    * Patikrinkite, ar kaina ir tiekėjas nukopijuoti į paraišką.  
6. Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.
7. Spustelėkite Baigti.
8. Uždarykite puslapį.
9. Spustelėkite Baigti.


