---
title: "Avanso turėtojai"
description: "Sužinokite apie išankstinio turėtojo funkcijas Microsoft Dynamics 365 operacijoms."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262574
ms.assetid: 87924785-6032-4125-8279-5b1a758f4d80
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 8cfe98e3859778e4fdc61f22b437cb1b4d004549
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holders"></a>Avanso turėtojai

Sužinokite apie išankstinio turėtojo funkcijas Microsoft Dynamics 365 operacijoms.

Yra *iš anksto laikiklis* yra darbuotojas, kuris yra atsakingas už išlaidų suma, kurią organizacija teikia. Tik įmonės darbuotojas gali būti išankstinis savininkas. Pirkimo atveju išankstinis savininkas ataskaitas bendrovei apie išlaidas, kurie buvo pagaminti. Įmonė kompensuojamos darbuotojo dėl išlaidų suma. Įmonė kontroliuoja pusiausvyrą už kiekvieną išankstinės turėtojas. Vartotojai – Estijos, Latvijos, Lietuvos, Lenkijos, Čekijos Respublikos, Vengrijos ir Rusijos ūkio subjektai gali atspindėti konkrečias operacijas kartu su įmonės darbuotojų, kurie yra atsakingi už išlaidų suma, kurią organizacija teikia.

## <a name="set-up-an-advance-holder"></a>Nustatyti iš anksto laikiklis
Norėdami nustatyti išankstinio turėtojo, šias užduotis turėtų būti baigtas tvarka.
1.  Kurti išankstinio turėtojo grupes.
2.  Nustatyti darbuotojo registravimo šablonas.
3.  Mokėtinos sąskaitos parametrų nustatymas.
4.  Sukurti konkretų mokėjimo išankstinio leidimo sąlygos.
5.  Sukurti iš anksto laikiklis.

### <a name="advance-holder-groups"></a>Avanso turėtojų grupės

Naudoti ir **iš anksto turėtojas dalyvauja** puslapis sukurti išankstinio turėtojo grupę. Nurodykite pavadinimą, aprašą ir korespondentinę sąskaitą iš anksto turėtojas grupės.
### <a name="employee-posting-profile"></a>Darbuotojų registravimo šablonas

Naudojimą, **darbuotojo registravimo šablonų** puslapį ir sukurkite profilį išankstinio turėtojo sandorių. Galite nurodyti šią informaciją apie darbuotojo registravimo šablonas.
|Laukas |aprašymas|
|------|-----------|
|Registravimo šablonas|Įveskite registravimo profilis identifikavimo kodas išankstinės turėtojas.|
|aprašymas|Įveskite trumpą aprašymą, registravimo šablonas.|
|Galioja|Pasirinkite vieną iš šių parinkčių grupės nustatymo registravimo šablonas lygio: 
**Stalas** – Ši parinktis naudojama nustatyti vieną iš anksto savininko registravimo šablono. Turite nurodyti iš anksto turėtojas kodo numerį laukelyje.
**Grupė** – šis variantas naudojamas registravimo šablonas nustatymas išankstinių savininkų grupė. Turite nurodyti grupės kodo numerį laukelyje.
**Visi** – šis variantas naudojamas registravimo šablonas nustatymas visus išankstinius savininkus. | | Nuoroda | Pasirinkite iš anksto turėtojo kodą, jei lentelė yra pasirinkta lauke galioja, arba pasirinkite iš anksto savininkas grupę, jei grupės yra pasirinkta lauke galioja. | | Suminė sąskaita | Pasirinkite suminė sąskaita, skirta registruoti operacijas. |



### <a name="account-payable-parameters"></a>Sąskaita mokėtinų sumų parametrai

Atspindi išankstinio turėtojo operacijas turite nustatyti šiuos į **sąskaita mokėtinų sumų parametrai** puslapyje, **iš anksto turėtojams** skyriuje.
|                                                |                   |
|------------------------------------------------|-------------------|
|  **Field**                                     | **Description**                                                                                                                                                                  |
| **Posting profile**                            | Pasirinkite Numatytasis profilis atlikti sandoriai, išankstiniai savininkai.                                                                                                         |
| **Advance holder sorting**                     | Jei pasirinkta, išankstiniai savininkai bus rodomas sąrašo pradžioje, **iš anksto turėtojams** puslapis.                                                                     |
| **Issue when balance is open**                 | Nepažymėjus, klausimas galėtų iš anksto turėtojas, kuris yra teigiamas likutis bus leidžiama.                                                                      |
| **Uždarymo elektroniniu pinigų laukų grupės balansas: pavadinimas** | Pasirinkite grynųjų pinigų kvito žurnalo kodą. Šis leidinys kodas naudojamas generuoti pinigų išmokėjimo kvitus ir kompensacijos kvitai uždarant išankstinio turėtojo likučiai per pinigus. |
| **Cash**                                       | Pasirinkite grynųjų pinigų sąskaitą, skirtą nustatyti, čekiai, kurie yra naudojami uždaryti likučiai išankstinio leidimo turėtojas.                                                                 |
| **Likutis uždarant per banko grupe: pavadinimas** | Pasirinkite žurnalo kodas sandoriams uždaryti likučiai per banką.                                                                                                   |
| **Account type**                               | Pasirinkite banką uždaryti likučiai iš anksto turėtojas per banką.                                                                                                        |
| **Main account**                               | Pasirinkite banko sąskaitos kodas uždaryti likučiai iš anksto turėtojas per banką.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Mokėjimo išankstinio leidimo sąlygos

Teisingai užsiregistruoti ir užregistruoti pirkimo užsakymą per iš anksto savininkas, turite naudoti mokėjimo, kuris pirmiau buvo nustatytas su sąlygos į **iš anksto turėtojo** parinktis nustatyta **True**.
### <a name="create-an-advance-holder-creation"></a>Kurti išankstinio turėtojo kūrimas

Prieš kurdami išankstinio turėtojo, turite turėti jau nustatyti darbuotojų. Daugiau informacijos rasite [įvesti darbuotojo informaciją (darbo vadovas).](http://ax.help.dynamics.com/en/wiki/enter-worker-information/) Naudoti ir **iš anksto turėtojams** puslapis nustatyti darbuotoją kaip iš anksto turėtojui. Pasirinkite darbuotojas gali naudoti kaip išankstinio turėtojui, spustelėkite **redaguoti**, ir tada nustatykite į **išankstinis savininkas** į **tiesa**. Jums reikia užpildyti šiuos laukus.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Field**      | **Description**                                                                             |
| **Group**      | Pasirinkite iš anksto savininkas grupę.                                                             |
| **Series**     | Įveskite serijos, dokumento, kuris naudojamas patikrinti iš anksto turėtojo tapatybę. |
| **Number**     | Įveskite dokumento, kuris naudojamas išankstinio turėtojo tapatybės numerį. |
| **Issue date** | Pasirinkite arba įveskite dokumento išdavimo data.                                                    |
| **Issued by**  | Įveskite informaciją apie instituciją ar dokumentą išdavęs asmuo.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Išankstinis savininkas užklausų ir ataskaitų
### <a name="advance-holder-transactions-inquiry"></a>Išankstinis savininkas operacijų tyrimo

Sandorių išankstinio leidimo, sąrašą, spustelėkite į **operacijos** mygtuką ir **iš anksto laikikliai** puslapis. Pamatyti sandorių visoms iš anksto turėtojai arba sukurti konkrečią užklausą pagal išankstinius savininkus operacijas, spustelėkite **mokėtinos sumos**&gt;**užklausų ir ataskaitų**&gt;**iš anksto laikikliai užklausų ir ataskaitų**&gt; operacijas. Spustelėkite **kvito** atidaryti, **kvitų operacijos** puslapis.
### <a name="advance-holder-balance-inquiry"></a>Išankstinis savininkas pusiausvyros tyrimo

Matyti balanse išankstinio leidimo naudoti su **iš anksto turėtojams** puslapis. Norėdami pamatyti likutį už visus iš anksto turėtojai arba sukurti konkrečią užklausą pagal išankstinių savininkų sąskaitas, spustelėkite **mokėtinos sumos**&gt;**užklausų ir ataskaitų**&gt;**iš anksto laikikliai užklausų ir ataskaitų**&gt;**pusiausvyrą.**
### <a name="advance-holder-balance-report"></a>Išankstinė savininko balanso ataskaita

Peržiūrėti ir spausdinti ataskaitą, grindžiamą informacijos apie išankstinius savininkus balansą, spustelėkite **mokėtinos sumos**&gt;**užklausų ir ataskaitų**&gt;**iš anksto laikikliai užklausų ir ataskaitų**&gt;**iš anksto turėtojas balanso ataskaita**.
### <a name="advance-holder-transactions-report"></a>Išankstinė savininko operacijų ataskaita

Peržiūrėti ir spausdinti ataskaitą pagal išankstinius savininkus operacijas, spustelėkite **mokėtinos sumos**&gt;**užklausų ir ataskaitų**&gt;**iš anksto laikikliai užklausų ir ataskaitų**&gt;**iš anksto turėtojo sandorių ataskaita**.



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Advance holder transactions](emea-advance-holders-transactions.md)


