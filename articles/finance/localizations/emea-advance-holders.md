---
title: Avanso turėtojų apžvalga
description: Šiame straipsnyje pateikiama informacija apie išankstinio savininko funkcijas.
author: AdamTrukawka
ms.date: 09/15/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 262574,  ""intro-internal
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
ms.openlocfilehash: 4b4c28c342f82ecd265bc70a51b3aa88dc0d7038
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285766"
---
# <a name="advance-holders-overview"></a>Avanso turėtojų apžvalga

[!include [banner](../includes/banner.md)]

*Avanso turėtojas* yra įmonės darbuotojas, kuris yra atsakingas už organizacijos pateiktą išlaidų sumą. Tik įmonės darbuotojas gali būti avanso turėtojas. Vykdant įsigijimą, avanso turėtojas įmonei praneša apie patirtas išlaidas. Įmonė darbuotojui kompensuoja išlaidų sumą. Įmonė valdo kiekvieno avanso turėtojo balansą. Juridinių subjektų Estijoje, Latvijoje, Lietuvoje, Lenkijoje, Čekijos Respublikoje, Vengrijoje ir Rusijoje vartotojai gali nurodyti konkrečias operacijas ir operacijas su įmonės darbuotojais, kurie yra atsakingi už organizacijos pateiktą išlaidų sumą.

## <a name="set-up-an-advance-holder"></a>Avanso turėtojo nustatymas
Atlikite pateiktas užduotis, kad nustatytumėte avanso turėtoją. Šias užduotis būtinai atlikite toliau nurodyta tvarka.

1. Avanso turėtojų grupių kūrimas.
2. Darbuotojų registravimo šablono nustatymas.
3. Mokėtinų sumų parametrų nustatymas.
4. Konkrečių kiekvieno avanso turėtojo mokėjimo sąlygų kūrimas.
5. Konkrečių kiekvieno avanso turėtojo mokėjimo sąlygų kūrimas.
6. Avanso turėtojo kūrimas.


### <a name="advance-holder-groups"></a>Avanso turėtojų grupės

Naudokite puslapį **Avanso turėtojų grupės**, kad sukurtumėte avanso turėtojų grupę. Galite nurodyti avanso turėtojų grupės pavadinimą, aprašą ir korespondentinę sąskaitą.
### <a name="employee-posting-profile"></a>Darbuotojų registravimo šablonas

Naudokite puslapį **Darbuotojų registravimo šablonai**, kad sukurtumėte avanso turėtojų operacijų šabloną. Galite nurodyti toliau pateiktą darbuotojų registravimo šablono informaciją.

|      Laukas      |                                            Aprašymas                                            |
|-----------------|---------------------------------------------------------------------------------------------------|
| **Registravimo šablonas** |  Įveskite avanso turėtojo registravimo šablono identifikavimo kodą.               |
|   **Aprašymas**   |  Įveskite trumpą registravimo šablono aprašą.                         |
|    **Galioja**    |  Pasirinkite vieną iš tolesnių registravimo šablono nustatymo grupavimo lygio parinkčių. <ul> <li>**Lentelė** – ši parinktis naudojama nustatant vieno avanso turėtojo registravimo šabloną. Turite nurodyti avanso turėtojo kodą lauke **Nuoroda**.</li> <li>**Grupė** – ši parinktis naudojama nustatant avanso turėtojų grupės registravimo šabloną. Turite nurodyti grupės kodą lauke **Nuoroda**.</li> <li>**Visi** – ši parinktis naudojama nustatant visų avanso turėtojų registravimo šabloną.</li></ul> |
| **Nuoroda** | Jei **Lentelė** pasirinkta lauke **Kam galioja**, pasirinkite avanso turėtojo kodą, o jei **Grupė** pasirinkta lauke **Kam galioja**, pasirinkite avanso turėtojo grupę. |
| **Suminė sąskaita** | Pasirinkite suminę sąskaitą operacijoms registruoti. |



### <a name="account-payable-parameters"></a>Mokėtinų sumų parametrai

Norėdami nurodyti avanso turėtojo operacijas, puslapio **Mokėtinų sumų parametrai** dalyje **Avanso turėtojai** turite nustatyti toliau pateiktus laukus.

|  Laukas                                         | Aprašymas       |
|------------------------------------------------|-------------------|
| **Registravimo šablonas**                            | Pasirinkite numatytąjį avanso turėtojų operacijų baigimo šabloną.                                                                                                         |
| **Avanso turėtojų rūšiavimas**                     | Jei pažymėta, avanso turėtojai bus rodomi puslapio **Avanso turėtojai** sąrašo pradžioje.                                                                     |
| **Išduoti, kai balansas atidarytas**                 | Jei pažymėta, bus leidžiamas avanso grynaisiais pinigais išdavimas avanso turėtojui, kurio atidarytas balansas teigiamas.                                                                      |
| **Laukų grupė Balanso uždarymas per grynuosius: pavadinimas** | Pasirinkite grynųjų pinigų kvitų žurnalo kodą. Žurnalo kodas naudojamas grynųjų pinigų išmokėjimo kvitams ir kompensavimo kvitams generuoti, kai avanso turėtojo balansas uždaromas per grynuosius pinigus. |
| **Grynieji pinigai**                                       | Pasirinkite grynųjų pinigų sąskaitą, kad nurodytumėte kvitus, naudojamus uždarant avanso turėtojo balansus.                                                                 |
| **Laukų grupė Balanso uždarymas per banką: pavadinimas** | Pasirinkite operacijų žurnalo kodą, kad uždarytumėte balansus per banką.                                                                                                   |
| **Sąskaitos tipas**                               | Pasirinkite banką, kad uždarytumėte avanso turėtojo balansus per banką.                                                                                                        |
| **Pagrindinė sąskaita**                               | Pasirinkite banko sąskaitos kodą, kad uždarytumėte avanso turėtojo balansus per banką.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Avanso turėtojo mokėjimo sąlygos

Norėdami tinkamai užregistruoti pirkimo užsakymą per avanso turėtoją, turite naudoti mokėjimo sąlygas, kurių parinktis **Iš avanso turėtojo** nustatyta į **Taip**.

### <a name="create-an-advance-holder"></a>Avanso turėtojo kūrimas

Prieš kurdami avanso turėtoją, turite būti jau nustatę darbuotojus. Norėdami gauti daugiau informacijos, žr. [Darbuotojo informacijos įvedimas (užduočių vedlys)](../../human-resources/hr-personnel-enter-worker-information.md). 

1. Pasirinkite **Mokėtinos sumos** > **Avanso turėtojai** > **Avanso turėtojai**.

    > [!NOTE]
    > Puslapyje **Avanso turėtojai** darbuotojų įtraukti arba pašalinti negalima. Darbuotojus pirmiausia būtina pasamdyti modulyje **Personalas**. Puslapyje **Darbuotojų registravimo šablonai** galite nustatyti darbuotojų registravimo šabloną, kuris naudojamas registruoti avanso turėtojų balansams.

2. Pažymėkite darbuotoją, paskui paspauskite **Redaguoti**.
3. „FastTab“ elemente **Bendra** nustatykite srities **Avanso turėtojas** parinktį **Taip**, kad būtų nurodoma, jog darbuotojas yra avanso turėtojas.
4. Lauke **Grupė** pasirinkite avanso turėtojų grupę, kuriai darbuotojas priklauso.
5. Srityje **Tapatybės dokumentas** pateikite išsamią informaciją apie identifikavimo dokumentą.
    - **Serija**: įveskite dokumento, kuris naudojamas avanso turėtojo tapatybei patvirtinti, seriją.
    - **Numeris**: įveskite dokumento, kuris naudojamas avanso turėtojo tapatybei patvirtinti, numerį.
    - **Išdavimo data**: pasirinkite arba įveskite dokumento išdavimo datą.
    - **Išdavė**: įveskite institucijos arba asmens, kuris išdavė dokumentą, informaciją.
6. Paspauskite **Įrašyti** arba uždarykite puslapį.

> [!NOTE]
> Jei puslapyje **Mokėtinų sumų parametrai** nustatyta srities **Avanso turėtojų rūšiavimas** parinktis **Taip**, avanso turėtojai rodomi puslapio **Avanso turėtojai** tinklelio viršuje.


## <a name="advance-holder-inquiries-and-reports"></a>Avanso turėtojo užklausos ir ataskaitos

### <a name="advance-holder-transactions-inquiry"></a>Avanso turėtojo operacijų užklausa

Norėdami peržiūrėti avanso turėtojo operacijų sąrašą, puslapyje **Avanso turėtojai** pasirinkite **Operacijos**. Norėdami peržiūrėti visų avanso turėtojų operacijas arba sukurti konkrečią užklausą pagal avanso turėtojų operacijas, eikite į **Mokėtinos sumos** > **Užklausos ir ataskaitos** > **Avanso turėtojų užklausos ir ataskaitos** > **Operacijos**. Pasirinkite **Kvitas**, kad atidarytumėte **Kvitų operacijų** puslapį.

### <a name="advance-holder-balance-inquiry"></a>Avanso turėtojo balanso užklausa

Norėdami peržiūrėti avanso turėtojo balansą, naudokite puslapį **Avanso turėtojai**. Norėdami peržiūrėti visų avanso turėtojų balansą arba kurti konkrečią užklausą pagal avanso turėtojų sąskaitas, spustelėkite **Mokėtinos sumos** &gt; **Užklausos ir ataskaitos** &gt; **Avanso turėtojų užklausos ir ataskaitos** &gt; **Balansas**.
### <a name="advance-holder-balance-report"></a>Avanso turėtojo balanso ataskaita

Norėdami peržiūrėti ir spausdinti ataskaitą, pagrįstą avanso turėtojų balanso informacija, spustelėkite **Mokėtinos sumos** &gt; **Užklausos ir ataskaitos** &gt; **Avanso turėtojų užklausos ir ataskaitos** &gt; **Avanso turėtojo balanso ataskaita**.
### <a name="advance-holder-transactions-report"></a>Avanso turėtojo operacijų ataskaita

Norėdami peržiūrėti ir spausdinti ataskaitą, pagrįstą avanso turėtojų operacijomis, spustelėkite **Mokėtinos sumos** &gt; **Užklausos ir ataskaitos** &gt; **Avanso turėtojų užklausos ir ataskaitos** &gt; **Avanso turėtojo operacijų ataskaita**.

## <a name="advance-holder-transactions"></a>Išankstinio savininko operacijos

Darbuotojų, kurie yra avanso turėtojai, operacijas galima registruoti naudojant avanso turėtojo sąskaitas. Darbuotojo ID, kuris priskirtas kiekvienam išankstiniams savininkui, galima naudoti norint sekti visas avanso turėtojo operacijas. Šis numeris yra nuskaitomas kaip avanso turėtojo operacijų sąskaitos numeris puslapiuose **Bendrieji žurnalai** ir **Avanso turėtojo operacijos**.

### <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Pirkimo užsakymo su avanso turėtojo informacija kūrimas ir registravimas
Daugiau bendros informacijos apie pirkimo užsakymus žr. temoje [Pirkimo užsakymo apžvalga](../../supply-chain/procurement/purchase-order-overview.md). Jei tiekėjo SF sukuriama ir užregistruojama su avanso turėtojo informacija, avanso turėtojo balansas bus užregistruotas darbuotojo balanso sąskaitoje, o ne tiekėjo balanso sąskaitoje. Norėdami avanso turėtojo informaciją įtraukti į pirkimo užsakymą, atlikite tolesnius veiksmus.

1. Dalies **Kaina ir nuolaida** lauke **Mokėjimo sąlygos** pasirinkite mokėjimo sąlygą. Daugiau informacijos apie **Mokėjimo sąlygas** ieškokite [Apibrėžkite tiekėjo mokėjimo sąlygas](../accounts-payable/tasks/define-vendor-payment-terms.md). 
2. Pasirinkite mokėjimo sąlygą, kurios parinktis **Iš avanso turėtojo**, esanti puslapyje **Mokėjimo sąlygos**, pažymėta. 
3. „FastTab“ **Kaina ir nuolaida**, esančiame lauke **Avanso turėtojas**, pasirinkite pirkimo užsakymo avanso turėtoją.

Pirkimo užsakymo registravimo proceso metu sukuriamos dvi tiekėjo operacijos su priešingomis sumomis ir viena avanso turėtojo operacija. Sukuriama tik viena tiekėjo operacija be avanso turėtojo informacijos.

### <a name="settle-advance-holder-balances-by-using-the-bank"></a>Avanso turėtojo balansų sudengimas naudojant banką
Kai avanso turėtojų balansus sudengiate naudodami banką, žurnalo įrašai apie avanso turėtojo balansų uždarymą sukuriami pagrindiniame žurnale. Žurnalo ir banko kodus galite nustatyti puslapio **Mokėtinų sumų parametrai** dalyje **Avanso turėtojai**. 

1. Norėdami uždaryti avanso turėtojo balansą naudodami banką, eikite į **Mokėtinos sumos** > **Avanso turėtojai** > **Avanso turėtojai**. 
2. Veiksmų srityje pasirinkite **Balansas** > **Uždaryti per banką**. 
3. Puslapyje **Uždaryti per banką** įveskite toliau nurodytą informaciją.

    | Laukas                    | Aprašymas |
    |------------------------------|-------------------|
    | **Mokėjimo data**          | Įvesti mokėjimo registravimo datą.|
    | **Suma, skirta perkelti** | Įveskite balanso sumą uždarymo metu. Suma, kuri yra nurodyta puslapio **Balansas** lauke **Suma**, yra rodoma pagal numatytuosius parametrus. |
    | **Automatinis**                | Norėdami automatiškai sukurti ir registruoti žurnalą, kuris yra iš anksto nustatytas puslapyje **Gautinų sumų parametrai**, pažymėkite žymės laukelį **Automatiškai**.|

### <a name="settle-advance-holder-balances-by-using-cash"></a>Avanso turėtojo balansų sudengimas naudojant grynuosius pinigus
Kai avanso turėtojų balansus nustatote naudodami grynuosius pinigus, žurnalo įrašai apie avanso turėtojo balansų uždarymą sukuriami važtaraščių žurnale. Žurnalo ir kasos kodus galite nustatyti puslapio **Mokėtinų sumų parametrai** skirtuke **Avanso turėtojai**. 

1. Norėdami uždaryti avanso turėtojo balansą naudodami grynuosius pinigus, eikite į **Mokėtinos sumos** > **Avanso turėtojai** > **Avanso turėtojai**. 
2. Veiksmų srityje pasirinkite **Balansas** > **Uždaryti naudojant grynuosius pinigus**. 
3. Puslapyje **Uždaryti per kasą** įveskite toliau nurodytą informaciją.

    | Laukas                    | Aprašymas
    |------------------------------|-----------------|
    | **Mokėjimo data**          | Įvesti mokėjimo registravimo datą.|
    | **Suma, skirta perkelti** | Įveskite balanso sumą uždarymo metu. Suma, kuri yra nurodyta puslapio **Balansas** lauke **Suma**, yra rodoma pagal numatytuosius parametrus. |
    | **Automatinis**                | Norėdami automatiškai sukurti ir registruoti žurnalą, kuris yra iš anksto nustatytas puslapyje **Gautinų sumų parametrai**, pažymėkite žymės laukelį **Automatiškai**.     |

Apdorojus važtaraščių žurnalą, jei suma, esanti lauke **Suma, skirta perkelti** yra neigiama, uždarius balansą generuojamas avanso turėtojo išmokėjimo kvitas. Jei suma lauke **Suma, skirta perkelti** yra teigiama, generuojamas kompensacijos kvitas.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Avanso mokėjimas darbuotojui (Rytų Europa)](tasks/advance-payment-employee.md)
- [Rusijos avanso turėtojų apžvalga](rus-advance-holders.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
