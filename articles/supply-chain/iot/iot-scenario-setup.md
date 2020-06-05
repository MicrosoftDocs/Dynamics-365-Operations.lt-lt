---
title: IoT analizės scenarijaus sąranka
description: Šioje temoje aprašoma, kaip konfigūruoti IoT analizės scenarijų programoje „Supply Chain Management“.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386542"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT analizės scenarijaus sąranka

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip konfigūruoti IoT analizės scenarijų programoje „Supply Chain Management“. Prieš konfigūruodami scenarijus turite [sukonfigūruoti LCS](iot-lcs-setup.md).

Šioje temoje konfigūruosite scenarijų **Įrangos prastovos**, kad įrenginiui sugedus, programoje „Supply Chain Management“ būtų sugeneruotas pranešimas.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Scenarijaus **Įrangos prastovos** konfigūravimas programoje „Supply Chain Management“

Scenarijus **Įrangos prastovos** susieja dalinio išjungimo signalą su įrenginio įspėjimo ribine verte. Įrenginys stebimas tik tada, kai jis pasirinktas scenarijuje ir nustatytas veikti programoje „Supply Chain Management“. Jeigu laikas nuo įrengino paskutinio gauto dalinio išjungimo signalo yra didesnis už įspėjimo ribinę vertę, suaktyvinamas pranešimas **Įrenginys neveikia**. Jeigu įrenginys vis dar veikia, kai gaunamas kitas **Dalinio išjungimo** signalas, suaktyvinamas pranešimas **Įrenginys veikia**. Jei įrenginys neveikia 30 min., suaktyvinamas naujas pranešimas **Įrenginys neveikia**.

Scenarijus **Įrangos prastovos** turi toliau nurodytas priklausomybes.

+ Norint suaktyvinti įspėjimą, susietame įrenginyje turi būti paleistas gamybos užsakymas.
+ Signalas, atitinkantis susieto įrenginio dalinio išjungimo signalą, turi būti išsiųstas į „IoT Hub“ su unikaliu ypatybės pavadinimu.
+ „IoT Hub“ pranešime turi būti „Unix“ milisekundžių laiko žymos ypatybė.

Norėdami konfigūruoti scenarijų, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Supply Chain Management“.
2. Įgalinkite IoT analizės funkcijos vėliavėlę. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Sukonfigūruokite metriką. Daugiau informacijos žr. [Kaip sukonfigūruoti metriką](iot-metrics-setup.md#configure-metrics).
4. Eikite į **Gamybos kontrolė**.
5. Eikite į **Sąranka \> IoT analizė \> Scenarijaus valdymas**.
6. Plytelėje **Įrangos prastovos** spustelėkite **Konfigūruoti**. Konfigūracijos vedlys prasideda puslapiu **Įrangos jutiklio schemos apibrėžimas**. Tikslas – programoje „Supply Chain Management“ nustatyti schemą, kuri atitiktų IoT pranešimų JSON formatą. Galima apibrėžti kelias pranešimų schemas. Daugiau informacijos, žr. [Pranešimų schemų formatai, skirti „IoT Hub“](iot-schema-format.md). Šiame pavyzdyje pranešimų apkrovoje yra pranešimų su šiuo formatu paketas:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Įtraukite į lentelę eilutę.

    1. Nustatykite **Schemos pavadinimas** reikšmę kaip **ID**.
    2. Nustatykite **Schemos kelias** reikšmę kaip **/payload[\*]/id**.
    3. Nustatykite **Aprašas** reikšmę kaip **Pranešimo ID**.

8. Įtraukite į lentelę eilutę.

    1. Nustatykite **Schemos pavadinimas** reikšmę kaip **Laiko žyma**.
    2. Nustatykite **Schemos kelias** reikšmę kaip **/payload[\*]/timestamp**.
    3. Nustatykite **Aprašas** reikšmę kaip **Pranešimo laiko žyma**.

9. Įtraukite į lentelę eilutę.

    1. Nustatykite **Schemos pavadinimas** reikšmę kaip **Reikšmė**.
    2. Nustatykite **Schemos kelias** reikšmę kaip **/payload[\*]/value**.
    3. Nustatykite **Aprašas** reikšmę kaip **Pranešimo reikšmė**.

    Jums nebūtina pranešime apibrėžti visų ypatybių. Apibrėžkite tik tas, kurios jums reikalingos. Šiame pavyzdyje nesukūrėte eilutės **Šakninė laiko žyma**. **Šakninė laiko žyma** kelias bus **/timestamp**.
  
10. Norėdami eiti į puslapį **Įrangos jutiklio schemos susiejimas** spustelėkite **Pirmyn**.
11. Eilutėje **Įrangos išteklių ID** nustatykite **Schemos pavadinimas** reikšmę kaip **ID**. Leistinos reikšmės rodomos išplėčiamojoje lentelėje.
12. Eilutėje **UTC laikas** nustatykite **Schemos pavadinimas** reikšmę kaip **Laiko žyma**. Leistinos reikšmės rodomos išplėčiamojoje lentelėje.
13. Eilutėje **Dalinai sugeneruotas signalas** nustatykite **Schemos pavadinimas** reikšmę kaip **Reikšmė**. Leistinos reikšmės rodomos išplėčiamojoje lentelėje.
14. Norėdami atidaryti puslapį **Įrangos išteklių ID konfigūracija** spustelėkite **Pirmyn**.
15. Atlikdami šį veiksmą galite susieti „IoT Hub“ pranešimų reikšmes su „Supply Chain Management“ ištekliais.

    1. Lentelėje **Signalo duomenų reikšmės** įtraukite naują eilutę ir stulpelyje **Reikšmė** įveskite **IoTInt.Machine1225.PartOut**. Reikšmė **IoTInt.Machine1225.PartOut** gaunama iš JSON ypatybės **id** „IoT Hub“ pranešime.
    2. Spustelėkite **Įrašyti**.
    3. Lentelėje **Verslo įrašo susiejimas** spustelėkite **Naujas**. Numatytoji ypatybės **Verslo įrašo tipas** reikšmė yra įvesta automatiškai, ir jums jos keisti nereikia.
    4. Stulpelyje **Verslo įrašas** pasirinkite „Supple Chain Management“ įrenginio išteklių, iš kurio siunčiama ši signalo reikšmė.
    5. Spustelėkite **Įrašyti**.
    6. Kartokite šiuos veiksmus įtraukdami naujo verslo įrašo **Machine1226** susiejimą. Su vienu „Supply Chain Management“ įrašu galite susieti kelias signalo duomenų reikšmes.

16. Norėdami pasirinkti, kuriuos įrenginius apdoroti, naudokite stulpelį **Pasirinkta**. Jums nebūtina apibrėžti visų signalų reikšmių ir pasirinkti visų įrenginių.
17. Spustelėkite **Pirmyn**, jei norite pereiti į puslapį **Dalinai sugeneruoto signalo konfigūravimas**.
18. Lentelėje **Signalo duomenų reikšmės** įtraukite eilutę ir nustatykite ypatybės **Reikšmė** reikšmę kaip **Teisinga**. Reikšmė **Teisinga** gaunama iš JSON ypatybės **value** „IoT Hub“ pranešime. Savo scenarijuje galite pridėti tiek reikšmių, kiek reikia.
19. Spustelėkite **Įrašyti**.
20. Norėdami eiti į puslapį **Įrangos prastovos ribinė vertė** spustelėkite **Pirmyn**. Nurodyti įrenginiai yra anksčiau su signalo reikšmėmis susieti įrenginiai. Šiame veiksme apibrėžiate ribinę vertę, kad nustatytumėte, ar įrenginys sugedo. Pavyzdžiui, jei nustatysite ribinę vertę 10, „Supply Chain Management“ sugeneruos pranešimą, jei 10 minučių iš įrenginio nebus gautas dalinio išjungimo pranešimas.
21. Norėdami pereiti puslapį **Įgalinti scenarijų**, spustelėkite **Pirmyn**. Norėdami įgalinti scenarijų, perjunkite slankiklį.
22. Spustelėkite **Baigti**.

Scenarijaus sąranka baigta. IoT analizės papildinys pradės automatiškai apdoroti „IoT Hub“ pranešimus.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Scenarijaus **Produkto kokybė** konfigūravimas programoje „Supply Chain Management“

Scenarijus **Produkto kokybė** sugeneruoja pranešimą, jei prekės atributas nepatenka į nurodytą diapazoną. Pavyzdžiui, jutiklis galėtų siųsti kiekvienos prekės svorį į „IoT Hub“. Jei prekė per sunki arba per lengva, programoje „Supply Chain Management“ būtų sugeneruotas pranešimas.

Scenarijus turi toliau nurodytas priklausomybes.

+ Tam, kad būtų suaktyvintas įspėjimas, gamybos užsakymas turi būti vykdomas susietame įrenginyje ir generuoti produktą su susieto paketo atributu.
+ Signalas, atitinkantis paketo atributą, turi būti išsiųstas į „IoT Hub“ su unikaliu ypatybės pavadinimu.
+ „IoT Hub“ pranešime turi būti „Unix“ milisekundžių laiko žymos ypatybė.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Scenarijaus **Gamybos atidėjimai** konfigūravimas programoje „Supply Chain Management“

Scenarijus **Gamybos atidėjimai** generuoja pranešimą, jei gamybos našumas yra mažesnis už ribinę vertę. Šiame scenarijuje signalas **PartOut** siunčiamas į „IoT Hub“ kiekvienai pagamintai prekei. Programoje „Supply Chain Management“ užsakymo atidėjimas apskaičiuojamas pagal tai, kiek laiko suplanuota vykdyti gamybos užsakymą, kiek prekių turėtų būti pagaminta, kaip ilgai vykdoma užduotis ir kiek signalų **PartOut** gauta. Perspėjimas dėl atidėjimo būtų sugeneruotas, jei užduoties signalų **PartOut** skaičius yra mažesnis už numatytos reikšmės ribinę vertę.

Scenarijus turi toliau nurodytas priklausomybes.

+ Norint suaktyvinti įspėjimą, susietame įrenginyje turi būti paleistas gamybos užsakymas.
+ Signalas, atitinkantis susieto įrenginio dalinio išjungimo signalą, turi būti išsiųstas į „IoT Hub“ su unikaliu ypatybės pavadinimu.
+ „IoT Hub“ pranešime turi būti „Unix“ milisekundžių laiko žymos ypatybė.

## <a name="how-to-disable-a-scenario"></a>Kaip išjungti scenarijų

Norėdami išjungti scenarijų, atlikite toliau nurodytus veiksmus.

1. Programoje „Supply Chain Management“ eikite į **Gamybos kontrolė \> Sąranka \> IoT analizė \> Scenarijaus valdymas**.
2. Scenarijuje spustelėkite **Konfigūruoti**.
3. Norėdami pereiti į paskutinį vedlio skirtuką spustelėkite **Pirmyn**.
4. Norėdami išjungti scenarijų, perjunkite slankiklį.
