---
title: „Commerce“ smulkių išlaidų valdymas (Rytų Europa)
description: Šioje temoje aprašoma, kaip nustatyti ir naudoti „Commerce“ grynųjų pinigų valdymo funkcijas Rytų Europoje.
author: epopov
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7a4c2e404b42a10a8d5f8b57135c56ae479a9efc3f5a8cef30831d02a3e53fe6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719914"
---
# <a name="petty-cash-management-for-commerce-for-eastern-europe"></a>„Commerce“ smulkių išlaidų valdymas (Rytų Europa)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacijos apie Rytų Europos prekybos verslo lokalizavimą.

Pagal Rytų Europos apskaitos reikalavimus, galite nustatyti grynųjų pinigų sąskaitų operacijas ir automatizuoti gavimų, grynųjų pinigų dokumentų ir grynųjų pinigų ataskaitų procesus. Daugiau informacijos ieškokite [(EEUR) Nustatyti grynųjų pinigų valdymo parametrus](/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).

Mažmenininkai gali priimti įvairių tipų mokėjimą mainais už produktus ir paslaugas, kurias jie parduoda. Nors dažniausia mokėjimo forma yra grynieji pinigai, mažmenininkai taip pat gali priimti mokėjimą čekiais, kortelėmis ar kvitais. „Retail“ elektroniniame kasos aparate (EKA) grynieji pinigai, kredito kortelių kvitai ir kiti mokėjimai apdorojami naudojant kasos aparatą.

Naudodami „Commerce“ grynųjų pinigų valdymą galite atlikti toliau nurodytus veiksmus.

- Sukurti pasirinkto mokėjimo būdo grynųjų pinigų sąskaitą kiekvienai parduotuvei.
- Naudoti grynųjų pinigų žurnalus grynųjų pinigų operacijoms ir klientų mokėjimams, gautiems mažmeninės prekybos EKA, registruoti.
- Sujungti išrašo eilutės operacijas registruojant išrašą. Galite sujungti pinigų įnešimą į kasą, inkasavimą, kvitų operacijas, mokėjimo priemonės išėmimo operacijas, pinigų srauto įrašo operacijas, pajamų operacijas, išlaidų operacijas, klientų mokėjimus, pardavimo operacijas ir grąžinimo operacijas.

Visos EKA vykstančios operacijos užregistruojamos naudojant didžiosios knygos žurnalą. Norėdami kurti ir registruoti išrašus, galite naudoti grynųjų pinigų mokėjimo žurnalus, klientų mokėjimo žurnalus ir pagrindinius žurnalus. Norėdami gauti daugiau informacijos, eikite į [Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas](/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).

Veiksmų srities puslapyje **Užregistruoti išrašai** galite atlikti toliau nurodytus veiksmus.

- Pasirinkite **Užklausos \> Mokėjimų grynaisiais pinigais žurnalas** ir prisijunkite prie su išrašu susietų mokėjimų grynaisiais pinigais žurnalų.
- Pasirinkite **Užklausos \> Pagrindinis žurnalas** ir prisijunkite prie su išrašu susijusių didžiosios knygos žurnalų (išskyrus klientų mokėjimų ir mokėjimų grynaisiais pinigais).

## <a name="set-up-for-cash-management-for-pos"></a>EKA grynųjų pinigų valdymo nustatymas

Prieš naudodami grynųjų pinigų valdymą, privalote atlikti tolesnę nustatymo procedūrą.

- Puslapyje **Mokėjimo būdai** nustatyti kiekvienam mokėjimo tipui skirtą mokėjimo būdą, su kuriuo sutinka pardavėjas. Galite naudoti skirtingus EKA registravimo operacijų mokėjimo būdus. Daugiau informacijos apie mokėjimo būdus ieškokite [Mokėjimo būdai](/dynamics365/unified-operations/retail/payment-methods).
- Nustatyti grynųjų pinigų operacijų parametrus.
- Nustatyti mokėjimų grynaisiais pinigais parduotuvėje mokėjimo būdą.

### <a name="set-up-parameters-for-cash-operations"></a>Grynųjų pinigų operacijų parametrų nustatymas

Galite nustatyti parametrus, kad galėtumėte kurti ir registruoti „Commerce“ grynųjų pinigų operacijas. Pardavimo ir mokėjimo operacijoms registruoti EKA galite naudoti mokėjimų grynaisiais pinigais žurnalus, kliento mokėjimų žurnalus arba bendruosius žurnalus. Registruodami išrašą galite sujungti operacijas, kurių ypatybės tokios pačios.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**. Kairiojoje srityje spustelėkite **Registravimas**.
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

### <a name="set-up-a-payment-method-for-cash-payments-in-a-store"></a>Mokėjimų grynaisiais pinigais parduotuvėje mokėjimo būdo nustatymas

Naudokite šią procedūrą norėdami nustatyti mokėjimų grynaisiais pinigais parduotuvėje mokėjimo būdą.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Parduotuvės \> Visos parduotuvės**.
2. Sąrašo puslapyje **Visos parduotuvės** pasirinkite parduotuvę, kuriai norite nustatyti mokėjimo būdą.
3. Veiksmų srityje, skirtuke **Nustatymas**, grupėje **Nustatymas** spustelėkite **Mokėjimo būdai**.
4. Puslapyje **Mokėjimo būdas** sukurkite arba pasirinkite mokėjimo būdą.
5. „FastTab“ skirtuke **Registravimas**, lauko grupėje **Sąskaita**, lauke **Sąskaitos tipas** pasirinkite **Grynųjų pinigų sąskaita**.

    > [!NOTE]
    > Parinktis **Grynųjų pinigų sąskaita** lauke **Sąskaitos tipas** galima tik lauke **Funkcija** pasirinkus **Įprasta** arba **Mokėjimo priemonės šalinimas / pinigų srautas**.

6. Lauke **Sąskaitos numeris** pasirinkite mokėjimo būdo grynųjų pinigų sąskaitos numerį.
7. Laukų grupės **Mokėjimo priemonės šalinimas / pinigų srautas** lauke **Korespondentinė sąskaita** pasirinkite korespondentinę sąskaitą, kurioje bus registruojamos mokėjimo būdo mokėjimo priemonės šalinimo arba pinigų srauto įrašo operacijos.

> [!NOTE]
> Parduotuvėje būtina nustatyti ir mokėjimo grynaisiais pinigais priemonės, ir mokėjimo priemonės šalinimo arba pinigų srauto įrašo mokėjimo būdo korespondentines sąskaitas. Tokiu būdu sukuriami subalansuoti mokėjimo priemonės šalinimo arba pinigų srauto operacijų DK įrašai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]