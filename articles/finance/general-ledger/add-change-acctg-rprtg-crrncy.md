---
title: Apskaitos arba ataskaitų valiutos keitimas
description: Šioje temoje paaiškinama, kaip pakeisti apskaitos ar ataskaitų valiutą arba įtraukti ataskaitų valiutą į didžiosios knygos nustatymą.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1fd641d4f60d8ff9710c89f43777f7fd8f378dbc6c73d773ac103f9d9f68e60e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770598"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Apskaitos arba ataskaitų valiutos keitimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip pakeisti apskaitos ar ataskaitų valiutą arba įtraukti ataskaitų valiutą į didžiosios knygos nustatymą.

## <a name="symptom"></a>Požymis

Norite pakeisti apskaitos ar ataskaitų valiutą arba įtraukti ataskaitų valiutą į didžiosios knygos nustatymą. Paprastai taip nutinka šiais atvejais:

- Nustatant juridinį subjektą buvo nurodyta neteisinga apskaitos arba ataskaitų valiuta. Dabar norite pakeisti šią valiutą.
- Nustatant juridinį subjektą buvo nurodyta ataskaitų valiuta, tačiau organizacija dabar nori pašalinti ataskaitų valiutą.
- Organizacija atnaujina arba perkelia į „Microsoft Dynamics 365 Finance“ ir nori pakeisti apskaitos arba ataskaitų valiutą.

Organizacija, kuri anksčiau nenaudojo dviejų valiutų galimybės, nori pradėti ją naudoti. Paprastai ši problema atsiranda toliau pateikiamais atvejais.

- Nustatant juridinį subjektą nebuvo nurodyta ataskaitų valiuta. (Ataskaitų valiuta nėra privaloma.) Dabar norite įtraukti ataskaitų valiutą.

## <a name="resolution"></a>Sprendimas

Svarbiausia atsižvelgti į tai, ar kokios nors operacijos (faktinės arba biudžeto) buvo užregistruotos didžiosios knygos nustatymo juridiniame subjekte. **Negalite keisti apskaitos ar ataskaitų valiutos arba pridėti ataskaitų valiutos, jei kokios nors operacijos (faktinės arba biudžeto) buvo užregistruotos juridiniame subjekte.** Atlikite toliau pateikiamuose skyriuose nurodytus veiksmus, atsižvelgdami į tai, ar operacijos buvo užregistruotos.

### <a name="no-transactions-have-been-posted"></a>Neužregistruota jokių operacijų

1. Juridiniame subjekte, kurio valiutas naujinate, eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> Didžioji knyga**.
2. Puslapyje **Didžioji knyga** pasirinkite **Redaguoti**.
3. „FastTab“ **Valiuta** pasirinkite apskaitos valiutą ir ataskaitų valiutą, kuri bus naudojama juridiniam subjektui.
4. Pasirinkite **Įrašyti**.

Jei puslapyje **Didžioji knyga** nėra apskaitos valiutos ir ataskaitų valiutos laukų, juridiniame subjekte buvo užregistruota viena ar daugiau operacijų (faktinių arba biudžeto). Todėl valiutų keisti negalima. Tokiu atveju atlikite kitame skyriuje nurodytus veiksmus.

### <a name="transactions-have-been-posted"></a>Operacijos buvo užregistruotos

**Jei operacijos užregistruotos juridiniame subjekte, vienintelis būdas pakeisti arba įtraukti apskaitos ir ataskaitų valiutas yra sukurti naują juridinį subjektą, turintį tinkamas valiutas.** Kad šis procesas būtų lengvesnis, naudojant duomenų valdymą sistemoje leidžiama kopijuoti nustatymo įrašus ir pagrindinius įrašus iš dabartinio juridinio subjekto į naują juridinį subjektą.

Apskaitos ir ataskaitų valiutų keitimai yra paplitę. Jie turi įtakos ne tik didžiajai knygai, bet ir kiekvienai papildomai knygai (Gautinos sumos, Mokėtinos sumos, Atsargos, Projektas ir t. t.), visiems nepriklausomo programinės įrangos tiekėjo (ISV) sprendimams ir bet kokiam sukurtam plėtiniui, kuriame saugomos sumos.

Kiekvienos sumos radimo ir perskaičiavimo į kitą valiutą procesas gali būti klaidingas. Todėl inžinierių komanda nepatvirtins scenarijaus, kuris keičia arba įtraukia apskaitos ir ataskaitų valiutas. Be to, nors įrankis, kuris anksčiau buvo prieinamas „Microsoft Dynamics AX 2012“, leidžia keisti arba įtraukti apskaitos ir ataskaitų valiutas, šis įrankis buvo nerekomenduojamas tiek „AX 2012 R3“, tiek „Finance“.

Atlikite šiuos veiksmus, kad nukopijuotumėte nustatymą ir bendruosius duomenis iš dabartinio juridinio subjekto į naują juridinį subjektą.

1. Pasirinkite **Darbo sritys \> Duomenų valdymas**.
2. Grupėje **Importavimas / eksportavimas** pasirinkite **Šablonas**.
3. Įsitikinkite, kad šablonai galimi. Jei šablonų nėra, pasirinkite **Įkelti numatytuosius šablonus** ir palaukite, kol šablonai bus sugeneruoti.
4. Grįžkite į darbo sritį **Duomenų valdymas**.
5. Pasirinkite **Kopijuoti į juridinį subjektą**.
6. Įveskite grupės pavadinimą ir aprašą.
7. Lauke **Šaltinio juridinis subjektas** pasirinkite juridinį subjektą, iš kurio norite kopijuoti duomenis.
8. „FastTab“ **Paskirties juridiniai subjektai** pasirinkite **Kurti juridinius subjektus**, kad sukurtumėte naują juridinį subjektą, į kurį galite kopijuoti šaltinio juridinio subjekto duomenis. Pasirinkite **Pasirinkti esamą**, jei norite kopijuoti duomenis į esamą juridinį subjektą.
9. Pasirinktinai: lauką **Kopijuoti numeraciją** nustatykite į **Taip**. (Šis veiksmas rekomenduojamas kopijuojant duomenis.)
10. Srityje **Pasirinkti subjektai** pasirinkite **Įtraukti šabloną**.
11. Pasirinkti naudotinus šablonus. Siūlomi naujo juridinio subjekto šablonai yra **025 – Didžioji knyga** ir **Finansai**. Rekomenduojame peržiūrėti visus kitus galimus šablonus, kad nustatytumėte, ar kuris nors iš jų atitinka jūsų reikalavimus.
12. Pasirinkite **Kopijuoti į juridinį subjektą**, kad pradėtumėte paketinį vykdymą, per kurį bus sukurti pasirinkti subjektai ir nukopijuoti į paskirties juridinį subjektą.
13. Kai procesas bus užbaigtas, bet prieš tai, kai kuri nors operacija bus užregistruota, eikite į didžiąją knygą ir atnaujinkite apskaitos ir ataskaitų valiutas, kaip aprašyta anksčiau šioje temoje.

Jei sukūrėte naują juridinį subjektą, kad galėtumėte keisti apskaitos arba ataskaitų valiutą, patikrinkite, ar pradiniai balansai perskaičiuojami iš seno juridinio subjekto valiutų į naujas valiutas.

Vaizdo įrašo, kuriame rodomi ankstesni veiksmai, ieškokite dalyje [Kopijuoti į juridinį subjektą](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
