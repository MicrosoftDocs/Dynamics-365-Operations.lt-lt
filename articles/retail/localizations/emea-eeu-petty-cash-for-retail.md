---
title: „Retail“ smulkių išlaidų valdymas (Rytų Europa)
description: Šioje temoje aprašoma, kaip nustatyti ir naudoti „Retail“ grynųjų pinigų valdymo funkcijas Rytų Europoje.
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 86df4508d897f1534c24e97bb4f4309d0d730c34
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538104"
---
# <a name="petty-cash-management-for-retail-for-eastern-europe"></a>„Retail“ smulkių išlaidų valdymas (Rytų Europa)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacijos apie Rytų Europos „Retail“ verslo lokalizavimą.

Pagal Rytų Europos apskaitos reikalavimus, galite nustatyti grynųjų pinigų sąskaitų operacijas ir automatizuoti gavimų, grynųjų pinigų dokumentų ir grynųjų pinigų ataskaitų procesus. Daugiau informacijos ieškokite [(EEUR) Nustatyti grynųjų pinigų valdymo parametrus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).

Mažmenininkai gali priimti įvairių tipų mokėjimą mainais už produktus ir paslaugas, kurias jie parduoda. Nors dažniausia mokėjimo forma yra grynieji pinigai, mažmenininkai taip pat gali priimti mokėjimą čekiais, kortelėmis ar kvitais. „Retail“ elektroniniame kasos aparate (EKA) grynieji pinigai, kredito kortelių kvitai ir kiti mokėjimai apdorojami naudojant kasos aparatą.

Naudodami „Retail“ grynųjų pinigų valdymą galite atlikti toliau nurodytus veiksmus.

- Sukurti pasirinkto mokėjimo būdo grynųjų pinigų sąskaitą kiekvienai mažmeninės prekybos parduotuvei.
- Naudoti grynųjų pinigų žurnalus grynųjų pinigų operacijoms ir klientų mokėjimams, gautiems mažmeninės prekybos EKA, registruoti.
- Sujungti išrašo eilutės operacijas registruojant mažmeninės prekybos išrašą. Galite sujungti pinigų įnešimą į kasą, inkasavimą, kvitų operacijas, mokėjimo priemonės išėmimo operacijas, pinigų srauto įrašo operacijas, pajamų operacijas, išlaidų operacijas, klientų mokėjimus, pardavimo operacijas ir grąžinimo operacijas.

Visos „Retail“ EKA vykstančios operacijos užregistruojamos naudojant didžiosios knygos žurnalą. Norėdami kurti ir registruoti išrašus, galite naudoti grynųjų pinigų mokėjimo žurnalus, klientų mokėjimo žurnalus ir pagrindinius žurnalus. Norėdami gauti daugiau informacijos, eikite į [Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).

Veiksmų srities puslapyje **Užregistruoti išrašai** galite atlikti toliau nurodytus veiksmus.

- Pasirinkite **Užklausos \> Mokėjimų grynaisiais pinigais žurnalas** ir prisijunkite prie su išrašu susietų mokėjimų grynaisiais pinigais žurnalų.
- Pasirinkite **Užklausos \> Pagrindinis žurnalas** ir prisijunkite prie su išrašu susijusių didžiosios knygos žurnalų (išskyrus klientų mokėjimų ir mokėjimų grynaisiais pinigais).

## <a name="set-up-for-cash-management-for-retail-pos"></a>„Retail POS“ grynųjų pinigų valdymo nustatymas

Prieš naudodami grynųjų pinigų valdymą mažmeninėje prekyboje, privalote baigti tolesnę nustatymo procedūrą:

- Puslapyje **Mokėjimo būdai** nustatyti kiekvienam mokėjimo tipui skirtą mokėjimo būdą, su kuriuo sutinka pardavėjas. Galite naudoti skirtingus „Retail POS“ registravimo operacijų mokėjimo būdus. Daugiau informacijos apie „Retail“ mokėjimo būdus ieškokite [Mokėjimo būdai](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).
- Nustatyti grynųjų pinigų operacijų mažmeninės prekybos parametrus.
- Nustatyti mokėjimų grynaisiais pinigais mažmeninės prekybos parduotuvėje mokėjimo būdą.

### <a name="set-up-retail-parameters-for-cash-operations"></a>Grynųjų pinigų operacijų mažmeninės prekybos parametrų nustatymas

Galite nustatyti parametrus, kad galėtumėte kurti ir registruoti mažmeninės prekybos grynųjų pinigų operacijas. Pardavimo ir mokėjimo operacijoms registruoti „Retail POS“ galite naudoti mokėjimų grynaisiais pinigais žurnalus, kliento mokėjimų žurnalus arba bendruosius žurnalus. Registruodami išrašą galite sujungti operacijas, kurių ypatybės tokios pačios.

1. Eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai**. Kairiojoje srityje spustelėkite **Registravimas**.
2. „FastTab“ skirtuko **Telkimas** srityje **Registravimas** nustatykite **Mokėjimo priemonės šalinimas / pinigų srautas** parinktį **Taip**, jei norite sujungti mokėjimo priemonės išėmimo operacijas arba pinigų srauto įrašo operacijas, susietas su išrašo eilute, kai registruojate išrašą. Mokėjimo priemonės šalinimo operacija sukuriama, kai išimate grynuosius pinigus iš EKA kasos stalčiaus. Pinigų srauto įrašo operacija sukuriama, kai įdedate grynuosius pinigus į EKA kasos stalčių.
3. Kai registruojate išrašą, suaktyvinkite toliau nurodytus atskirus parametrus, jei norite sujungti operacijas, kurios susietos su išrašo eilute.

    - **Inkasavimas** – sujunkite banko operacijas.
    - **Pinigų įnešimas į kasą** – sujunkite kasos operacijas.
    - **Pajamų / išlaidų operacijos** – sujunkite pajamų arba išladų operacijas.
    - **Kvito operacijos** – sujunkite kvito operacijas.
    - **Kliento mokėjimai** – sujunkite kliento mokėjimus.
    - **Pardavimas ir grąžinimai** – sujunkite pardavimo ir grąžinimų operacijas.

4. „FastTab“ skirtuke **Mokėjimai** pasirinkite numatytąjį žurnalo pavadinimą. Galimos šios pasirinktys:

    - **Kliento mokėjimų žurnalas** – šis žurnalas naudojamas kliento mokėjimams registruoti.
    - **Mokėjimų grynaisiais pinigais žurnalas** – šis žurnalas naudojamas mokėjimams grynaisiais pinigais registruoti.
    - **Pagrindinis žurnalas** – šis žurnalas naudojamas norint registruoti kitas operacijas (ne mokėjimų grynaisiais pinigais ir ne kliento mokėjimų operacijas).

### <a name="set-up-a-payment-method-for-cash-payments-in-a-retail-store"></a>Mokėjimų grynaisiais pinigais mažmeninės prekybos parduotuvėje mokėjimo būdo nustatymas

Naudokite šią procedūrą norėdami nustatyti mokėjimų grynaisiais pinigais mažmeninės prekybos parduotuvėje mokėjimo būdą.

1. Pasirinkite **Mažmeninė prekyba \> Kanalai \> Mažmeninės prekybos parduotuvės \> Visos mažmeninės prekybos parduotuvės**.
2. Sąrašo puslapyje **Visos mažmeninės prekybos parduotuvės** pasirinkite parduotuvę, kuriai norite nustatyti mokėjimo būdą.
3. Veiksmų srityje, skirtuke **Nustatymas**, grupėje **Nustatymas** spustelėkite **Mokėjimo būdai**.
4. Puslapyje **Mokėjimo būdas** sukurkite arba pasirinkite mokėjimo būdą.
5. „FastTab“ skirtuke **Registravimas**, lauko grupėje **Sąskaita**, lauke **Sąskaitos tipas** pasirinkite **Grynųjų pinigų sąskaita**.

    > [!NOTE]
    > Parinktis **Grynųjų pinigų sąskaita** lauke **Sąskaitos tipas** galima tik lauke **Funkcija** pasirinkus **Įprasta** arba **Mokėjimo priemonės šalinimas / pinigų srautas**.

6. Lauke **Sąskaitos numeris** pasirinkite mokėjimo būdo grynųjų pinigų sąskaitos numerį.
7. Laukų grupės **Mokėjimo priemonės šalinimas / pinigų srautas** lauke **Korespondentinė sąskaita** pasirinkite korespondentinę sąskaitą, kurioje bus registruojamos mokėjimo būdo mokėjimo priemonės šalinimo arba pinigų srauto įrašo operacijos.

> [!NOTE]
> Parduotuvėje būtina nustatyti ir mokėjimo grynaisiais pinigais priemonės, ir mokėjimo priemonės šalinimo arba pinigų srauto įrašo mokėjimo būdo korespondentines sąskaitas. Tokiu būdu sukuriami subalansuoti mokėjimo priemonės šalinimo arba pinigų srauto operacijų DK įrašai.
