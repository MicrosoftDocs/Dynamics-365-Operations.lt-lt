---
title: "Avanso turėtojai"
description: "Sužinokite apie avanso turėtojo funkciją programoje „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise‟)."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 262574
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c6cbc225d6ac8eb4c4c22dc50c42bf9563cec02a
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="advance-holders"></a>Avanso turėtojai

[!include[banner](../includes/banner.md)]


Sužinokite apie avanso turėtojo funkciją programoje „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise‟).

*Avanso turėtojas* yra įmonės darbuotojas, kuris yra atsakingas už organizacijos pateiktą išlaidų sumą. Tik įmonės darbuotojas gali būti avanso turėtojas. Vykdant įsigijimą, avanso turėtojas įmonei praneša apie patirtas išlaidas. Įmonė darbuotojui kompensuoja išlaidų sumą. Įmonė valdo kiekvieno avanso turėtojo balansą. Juridinių subjektų Estijoje, Latvijoje, Lietuvoje, Lenkijoje, Čekijos Respublikoje, Vengrijoje ir Rusijoje vartotojai gali nurodyti konkrečias operacijas ir operacijas su įmonės darbuotojais, kurie yra atsakingi už organizacijos pateiktą išlaidų sumą.

## <a name="set-up-an-advance-holder"></a>Avanso turėtojo nustatymas
Norint nustatyti avanso turėtoją, reikia nurodyta tvarka atlikti toliau pateiktas užduotis.
1.  Sukurkite avanso turėtojų grupes.
2.  Nustatykite darbuotojų registravimo šabloną.
3.  Nustatykite mokėtinų sumų parametrus.
4.  Sukurkite konkrečias kiekvieno avanso turėtojo mokėjimo sąlygas.
5.  Sukurkite avanso turėtoją.

### <a name="advance-holder-groups"></a>Avanso turėtojų grupės

Naudokite puslapį **Avanso turėtojų grupės**, kad sukurtumėte avanso turėtojų grupę. Galite nurodyti avanso turėtojų grupės pavadinimą, aprašą ir korespondentinę sąskaitą.
### <a name="employee-posting-profile"></a>Darbuotojų registravimo šablonas

Naudokite puslapį **Darbuotojų registravimo šablonai**, kad sukurtumėte avanso turėtojų operacijų šabloną. Galite nurodyti toliau pateiktą darbuotojų registravimo šablono informaciją.
|Laukas |aprašymas|
|------|-----------|
|Registravimo šablonas|Įveskite avanso turėtojo registravimo šablono identifikavimo kodą.|
|aprašymas|Įveskite trumpą registravimo šablono aprašą.|
|Galioja|Pasirinkite vieną iš tolesnių registravimo šablono nustatymo grupavimo lygio parinkčių. 
**Lentelė** – ši parinktis naudojama nustatant vieno avanso turėtojo registravimo šabloną. Turite nurodyti avanso turėtojo kodą lauke Nuoroda.
**Grupė** – ši parinktis naudojama nustatant avanso turėtojų grupės registravimo šabloną. Turite nurodyti grupės kodą lauke Nuoroda.
**Visi** – ši parinktis naudojama nustatant visų avanso turėtojų registravimo šabloną.| |Nuoroda|Pasirinkite avanso turėtojo kodą, jei lauke Galioja pasirinkta parinktis Lentelė, arba pasirinkite avanso turėtojo grupę, jei lauke Galioja pasirinkta parinktis Grupė.| |Suminė sąskaita|Pasirinkite operacijų registravimo suminę sąskaitą.|



### <a name="account-payable-parameters"></a>Mokėtinų sumų parametrai

Norėdami nurodyti avanso turėtojo operacijas, puslapio **Mokėtinų sumų parametrai** dalyje **Avanso turėtojai** turite nustatyti toliau pateiktą informaciją.
|                                                |                   |
|------------------------------------------------|-------------------|
|  **Laukas**                                     | **Aprašas**                                                                                                                                                                  |
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
### <a name="create-an-advance-holder-creation"></a>Avanso turėtojo kūrimas

Prieš kurdami avanso turėtoją, turite būti jau nustatę darbuotojus. Daugiau informacijos žr. [Darbuotojo informacijos įvedimas (užduočių vedlys)](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enter-worker-information) Naudokite puslapį **Avanso turėtojai**, kad darbuotoją nustatytumėte kaip avanso turėtoją. Pasirinkite darbuotoją, kurį nustatysite kaip avanso turėtoją, spustelėkite **Redaguoti** ir tada nustatykite parinktį **Avanso turėtojas** į **True**. Taip pat turite užpildyti tolesnius laukus.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Laukas**      | **Aprašas**                                                                             |
| **Grupė**      | Pasirinkite avanso turėtojų grupę.                                                             |
| **Serija**     | Įveskite dokumento, kuris naudojamas avanso turėtojo tapatybei patvirtinti, seriją. |
| **Numeris**     | Įveskite dokumento, kuris naudojamas avanso turėtojo tapatybei patvirtinti, numerį. |
| **Išdavimo data** | Pasirinkite arba įveskite dokumento išdavimo datą.                                                    |
| **Išdavė**  | Įveskite institucijos arba asmens, kuris išdavė dokumentą, informaciją.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Avanso turėtojo užklausos ir ataskaitos
### <a name="advance-holder-transactions-inquiry"></a>Avanso turėtojo operacijų užklausa

Norėdami peržiūrėti avanso turėtojo operacijų sąrašą, puslapyje **Avanso turėtojai** spustelėkite mygtuką **Operacijos**. Norėdami peržiūrėti visų avanso turėtojų operacijas arba kurti konkrečią užklausą pagal avanso turėtojų operacijas, spustelėkite **Mokėtinos sumos** &gt; **Užklausos ir ataskaitos** &gt; **Avanso turėtojų užklausos ir ataskaitos** &gt; Operacijos. Spustelėkite **Kvitas**, kad atidarytumėte puslapį **Kvitų operacijos**.
### <a name="advance-holder-balance-inquiry"></a>Avanso turėtojo balanso užklausa

Norėdami peržiūrėti avanso turėtojo balansą, naudokite puslapį **Avanso turėtojai**. Norėdami peržiūrėti visų avanso turėtojų balansą arba kurti konkrečią užklausą pagal avanso turėtojų sąskaitas, spustelėkite **Mokėtinos sumos** &gt; **Užklausos ir ataskaitos** &gt; **Avanso turėtojų užklausos ir ataskaitos** &gt; **Balansas**.
### <a name="advance-holder-balance-report"></a>Avanso turėtojo balanso ataskaita

Norėdami peržiūrėti ir spausdinti ataskaitą, pagrįstą avanso turėtojų balanso informacija, spustelėkite **Mokėtinos sumos** &gt; **Užklausos ir ataskaitos** &gt; **Avanso turėtojų užklausos ir ataskaitos** &gt; **Avanso turėtojo balanso ataskaita**.
### <a name="advance-holder-transactions-report"></a>Avanso turėtojo operacijų ataskaita

Norėdami peržiūrėti ir spausdinti ataskaitą, pagrįstą avanso turėtojų operacijomis, spustelėkite **Mokėtinos sumos** &gt; **Užklausos ir ataskaitos** &gt; **Avanso turėtojų užklausos ir ataskaitos** &gt; **Avanso turėtojo operacijų ataskaita**.



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Avanso turėtojo operacijos](emea-advance-holders-transactions.md)




