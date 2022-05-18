---
title: Mokesčių funkcijų palaikymos operacijų užsakymams
description: Šioje temoje paaiškinama naujos mokesčių priemonės perkėlimo užsakymų palaikymas naudojant mokesčių skaičiavimo tarnybą.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d95ea6795dc5777bfd37f8fbb3ebc47f2db337a0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689220"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Mokesčių funkcijų palaikymos operacijų užsakymams

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiama informacija apie mokesčių skaičiavimą ir registravimo integravimą perkėlimo užsakymuose. Ši funkcija leidžia nustatyti mokesčių skaičiavimą ir registravimą atsargų perkėlimo užsakymuose. Pagal Europos Sąjungos (ES) pridėtinės vertės mokesčio (PVM) nuostatus, atsargų perkėlimas laikomas vidiniu bendrijos tiekimu ir įsigijimais bendrijos viduje.

Norėdami konfigūruoti ir naudoti šią funkciją, turite atlikti tris pagrindinius veiksmus:

1. **RCS nustatymas: reguliavimo konfigūravimo tarnybose nustatykite mokesčių funkciją, mokesčių kodus ir mokesčių kodų taikomumą mokesčių** kodo nustatymui perkėlimo užsakymuose.
2. **"Dynamics 365" finansų nustatymas:** finansuose įjunkite **perkėlimo** užsakymo mokesčio funkciją, nustatykite atsargų mokesčių skaičiavimo tarnybos parametrus ir nustatykite pagrindinius mokesčių parametrus.
3. **Atsargų nustatymas:** nustatykite perkėlimo užsakymo operacijų atsargų konfigūraciją.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Nustatyti mokesčių ir perkėlimo užsakymo operacijų RCS

Norėdami nustatyti su perkėlimo užsakymu susijusių mokesčių, atlikite šiuos veiksmus. Pavyzdyje, kuris rodomas čia, perkėlimo užsakymas iš Olandijos į Belgiją.

1. Mokesčių priemonių **puslapyje**, skirtuke **Versijos**, pasirinkite juodraščio priemonės versiją, tada pasirinkite **Redaguoti**.

2. Mokesčių priemonių **nustatymo** puslapyje, skirtuke **Mokesčių** kodai, pasirinkite Įtraukti, **kad** sukurtumėte naujus mokesčių kodus. Pavyzdžiui, sukurti trys mokesčių kodai: **NL-atleidimas,** **„BE-RC-21“** ir **„BE-RC+21“**.

    - Kai perkėlimo užsakymas siunčiamas iš Olandijos sandėlio, taikomas Olandijos PVM neapmokestinimo **kodas** (NL-Exempt).
      
        Kurti mokesčio kodą **NL neapmokestinama**.
        1. Pasirinkite **Pridėti**, įveskite **NL-atleidimas** PVM kodo **lauke**.
        2. Pasirinkite **pagal grynąją** sumą mokesčio **komponento** lauke.
        3. Pasirinkite **Įrašyti**.
        4. Pasirinkite **Įtraukti** **Reitingavimo** lentelėje.
        5. Nustatykite **Yra neapmokestinama** į **Taip** **Bendrajame** skyriuje.
        6. Lauke **Neapmokestinimo kodas** įveskite **EC**.

    - Kai perkėlimo užsakymas gaunamas Belgijos sandėlyje, atvirkštinio apmokestinimo mechanizmas taikomas naudojant **„BE-RC-21“ ir** **„BE-RC+21“** mokesčių kodus.
        
        Sukurkite mokesčio kodą **„BE-RC-21“**.      
        1. Pasirinkite **Pridėti**, įveskite **„BE-RC-21“** PVM kodo **lauke**.
        2. Pasirinkite **pagal grynąją** sumą mokesčio **komponento** lauke.
        3. Pasirinkite **Įrašyti**.
        4. Pasirinkite **Įtraukti** **Reitingavimo** lentelėje.
        5. Įveskite **-21** į mokesčio tarifo **lauką**.
        6. Nustatykite **Yra atvirkštinis apmokestinimas** į **Taip** **Bendrajame** skyriuje.
        7. Pasirinkite **Įrašyti**.
        
        Sukurkite mokesčio kodą **„BE-RC+21“**.
        1. Pasirinkite **Pridėti**, įveskite **„BE-RC-21“** PVM kodo **lauke**.
        2. Pasirinkite **pagal grynąją** sumą mokesčio **komponento** lauke.
        3. Pasirinkite **Įrašyti**.
        4. Pasirinkite **Įtraukti** **Reitingavimo** lentelėje.
        5. Įveskite **21** į mokesčio tarifo **lauką**.
        6. Pasirinkite **Įrašyti**.

3. Nurodykite mokesčių grupę.
    1. Pasirinkite **Tvarkyti stulpelius**, tada pasirinkite eilutės lauką **Mokesčių grupė**.
    2. Pasirinkite **->**, tada pasirinkite **Gerai**.
    3. Pasirinkite **Įtraukti**, kad įtrauktumėte mokesčių grupę.
    4. **Mokesčių grupės** stulpelyje įveskite **AR-EU** ir tada pasirinkite **NL-neapmokestinamas** mokesčio kodą.
    5. Pasirinkite **Įtraukti**, kad įtrauktumėte mokesčių grupę.
    6. **Mokesčių grupės** stulpelyje įveskite **RC-PVM** ir tada pasirinkite **BE-RC-21** ir **BE-RC+21** mokesčių kodus.
4. Nurodykite prekės mokesčių grupę.
    1. Pasirinkite **Tvarkyti stulpelius**, tada pasirinkite eilutės lauką **Prekės mokesčių grupė**.
    2. Pasirinkite **->** ir tada pasirinkite **Gerai**.
    3. Pasirinkite **Įtraukti**, kad įtrauktumėte prekės mokesčių grupę.
    4. Įveskite **PILNAS** stulpelyje **Prekės mokesčių grupė**. Pasirinkite mokesčių kodus **BE-RC-21**, **BE-RC+21** ir **NL-exempt**.
5. Nustatykite mokesčių grupės taikomumą.

    1. Pasirinkite **Tvarkyti** stulpelius, tada pasirinkite stulpelius, kurie turėtų būti naudojami kuriant taikomumo lentelę.

        > [!NOTE]
        > Būtinai įtraukite verslo **proceso ir** mokesčių **krypčių stulpelius į** lentelę. Abu stulpeliai yra labai svarbūs perkėlimo užsakymų mokesčių funkcijai.

    2. Taikyti taikomas taisykles. Nepalikite **Mokesčio grupės** lauko tuščio.
        
        Įtraukite naują perkėlimo užsakymo siuntimo taisyklę.
        1. Pasirinkite **Įtraukti** **Taikomos taisyklės** lentelėje.
        2. Verslo proceso **lauke pasirinkite** **Atsargos, kad taisyklė būtų taikoma perkėlimo** užsakymui.
        3. Lauke **Siuntimo iš šalies/** regiono įveskite **„NLD“**.
        4. Lauke **Siuntimo į šalies/** regiono įveskite **„BEL“**.
        5. Mokesčių krypties **lauke pasirinkite** Išvestis, **kad taisyklė būtų taikoma perkėlimo užsakymo** siuntai.
        6. Laukelyje **Mokesčių grupė** pasirinkite **AR-EU**.
        
        Įtraukite kitą perkėlimo užsakymo gavimo taisyklę.
        
        1. Pasirinkite **Įtraukti** **Taikomos taisyklės** lentelėje.
        2. Verslo proceso **lauke pasirinkite** **Atsargos, kad taisyklė būtų taikoma perkėlimo** užsakymui.
        3. Lauke **Siuntimo iš šalies/** regiono įveskite **„NLD“**.
        4. Lauke **Siuntimo į šalies/** regiono įveskite **„BEL“**.
        5. Mokesčių krypties **lauke pasirinkite** Įvestis, **kad taisyklė būtų taikoma perkėlimo užsakymo** gavimai.
        6. Laukelyje **Mokesčių grupė** pasirinkite **RC-VAT**.

6. Nustatykite prekės mokesčių grupės taikomumą.

    1. Pasirinkite **Tvarkyti** stulpelius, tada pasirinkite stulpelius, kurie turėtų būti naudojami kuriant taikomumo lentelę.
    2. Taikyti taikomas taisykles. Nepalikite **Prekės mokesčio grupės** lauko tuščio.
        
        Įtraukite naują perkėlimo užsakymo siuntimo taisyklę ir čekį.
        1. **Taikomumo taisyklės** puslapyje pasirinkite **Įtraukti**.
        2. **Verslo proceso** lauke pasirinkite **Atsargos** kad taisyklė būtų taikoma perkėlimo užsakymui.
        3. Laukelyje **Prekės mokesčių grupė** pasirinkite **PILNAS**.
7. Užpildykite ir publikuokite naują mokesčių priemonės versiją.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Nustatyti „Finance“ ir perkėlimo užsakymo operacijas

Atlikite šiuos žingsnius, kad įjungtumėte ir nustatytumėte mokesčius operacijų užsakymams.

1. „Finance“ eikite į **Darbo sritys** > **Funkcijų valdymas**.
2. Sąraše raskite ir pasirinkite mokestį perkėlimo užsakymo priemonėje, tada, norėdami **jį įjungti** **pasirinkite Įgalinti** dabar.

    > [!IMPORTANT]
    > **Perkėlimo užsakymo mokesčio** funkcija visiškai priklauso nuo mokesčių skaičiavimo paslaugos. Todėl jį galima įjungti tik įdiegus mokesčių skaičiavimo paslaugą.

    ![Mokesčiai operacijų užsakymo funkcijoje.](../media/image7.png)

3. Įgalinkite mokesčių skaičiavimo paslaugą ir pasirinkite **Atsargų** verslo procesą.

    > [!IMPORTANT]
    > Turite atlikti šį žingsnį su kiekvienu finansų juridiniu subjektu, kur norite, kad būtų galima naudoti mokesčių skaičiavimo paslaugą ir perkėlimo užsakymų mokesčių funkciją.

    1. Eikite į **Mokesčiai** > **Sąranka** > **Mokesčių konfigūracija** > **Mokesčių skaičiavimo parametrai**.
    2. Verslo **proceso lauke** pasirinkite **Atsargos**.

4. Patikrinkite, ar nustatytas atvirkštinio apmokestinimo mechanizmas. Eikite į DK nustatymo parametrus, tada skirtuke Atvirkštinis apmokestinimas patikrinkite, **ar** \> **nustatyta** \> **parinktis** **Įgalinti** **atvirkštinį apmokestinimą kaip** **Taip**.

    ![Įjungti atvirkštinio apmokestinimo parinktį.](../media/image9.png)

5. Patikrinkite, ar susiję mokesčių kodai, mokesčių grupės, prekių mokesčių grupės ir PVM registracijos numeriai nustatyti finansuose pagal mokesčių skaičiavimo paslaugos nurodymus.
6. Nustatyti tarpinę tarpinę sąskaitą. Šio veiksmo reikia atlikti tik tada, kai perkėlimo užsakymui taikomas mokestis nėra taikomas pvm mokėjimo arba atvirkštinio apmokestinimo mechanizmui.

    1. Eikite į **Mokesčiai** > **Nustatymas** > **Pardavimų mokesčiai** > **Didžiosios knygos registravimo grupės**.
    2. Lauke **Tarpinis tranzitas** pasirinkite DK sąskaitą.

       ![Pasirinkti tarpinę sąskaitą.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Nustatyti pagrindines atsargas perkėlimo užsakymo operacijoms

Norėdami nustatyti pagrindines atsargas perkėlimo užsakymo operacijoms įgalinti, atlikite šiuos veiksmus.

1. Kurkite siuntimo iš ir siuntimo vietas savo sandėliams skirtingose šalyse ar regionuose ir pridėkite kiekvienos teritorijos pagrindinį adresą.

    1. Eikite į **Sandėlio valdymas** > **Sąranka** > **Sandėlis** > **Vietos**.
    2. Pasirinkite **Nauja**, jei norite sukurti svetainę, kurią priskirsite sandėliui vėliau.
    3. Visoms kitoms svetainėms, kurias turite sukurti, atlikite 2 veiksmą.

    > [!NOTE]
    > Viena iš jūsų sukurtų teritorijų turi būti vadinama **tranzitu**. Vėlesniais šios procedūros veiksmais šią teritoriją priskirsite tranzito sandėliui, kad su mokesčiais susijusius atsargų kvitus būtų galima registruoti perkėlimo užsakymų operacijose „Siųsti" ir „Gauti". Tranzito vietos adresas nesusijęs su mokesčių apskaičiavimu. Dėl to, galite palikti jį tuščią.

    ![Saitų nustatymas.](../media/image11.png)

2. Kurti siuntimo iš, tranzito ir siuntimo sandėlius. Apskaičiuojant mokesčius bet kokia sandėlyje tvarkoma adreso informacija perrašys svetainės adresą.

    1. Eikite į **„Warehouse Management”** > **Nustatymas** > **Sandėlis** > **Sandėliai**.
    2. Pasirinkite **Nauja**, jei norite sukurti svetainę ir priskirkite ją atitinkamam saitui.
    3. Norėdami kiekvienai vietai sukurti sandėlį, pakartokite 2 veiksmą.

       ![Sandėlių nustatymas.](../media/image12.png)

    > [!NOTE]
    > Perkėlimo užsakymo operacijoms atlikti lauke Tranzito sandėlis turi būti pasirinktas siuntimo iš **sandėlio** sandėlio laukas.
    >
    > ![Tranzito sandėlio pasirinkimas.](../media/image13.png)

3. Patvirtinkite, ar atsargų publikavimo konfigūravimas yra nustatytas perlaidos užsakymo operacijoms.

    1. Eikite į **Atsargų valdymas** > **Sąranka** > **Registravimas** > **Registravimas**.
    2. Skirtuke Atsargos patikrinkite, ar nustatyta DK **sąskaita atsargų** išdavimui ir atsargų **gavimo** **registravimui**.

        ![Atsargų išdavimo ir atsargų gavimo registravimo nustatymas.](../media/image14.png)

    3. Patikrinkite, ar DK sąskaita nustatyta mokėtinų **sumų registravimui tarp vienetų**.

        ![Mokėtinų sumų registravimo tarp vienetų nustatymas.](../media/image15.png)

    4. Patikrinkite, ar DK sąskaita nustatyta mokėtinų **sumų publikavimui tarp gaunamų sumų**.

        ![Tarpinių gaunamų sumų publikavimo nustatymas.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
