---
title: IoT įžvalgų scenarijaus sąranka
description: Šioje temoje paaiškinama, kaip konfigūruoti IoT įžvalgų scenarijus „Microsoft Dynamics 365 Supply Chain Management”.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91deb080121d50794e6ff6fe79f9ca876b76deb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005257"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT įžvalgų scenarijaus sąranka

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti IoT įžvalgų scenarijus „Microsoft Dynamics 365 Supply Chain Management”. Prieš nustatant scenarijus pirmiausia reikia [nustatyti „Microsoft Dynamics Lifecycle Services” (LCS)](iot-lcs-setup.md).

Šioje temoje konfigūruosite scenarijų **Įrangos prastovos**, kad įrenginiui sugedus, programoje „Supply Chain Management“ būtų sugeneruotas pranešimas. Temoje taip pat rodoma, kaip konfigūruoti scenarijų **Produkto kokybė**, kad būtų sugeneruotas pranešimas, jei prekės atributas yra už nurodyto intervalo ribų, ir kaip konfigūruoti scenarijų **Gamybos atidėjimai**, kad būtų sugeneruotas pranešimas, jei gamybos našumas yra mažesnis už ribinę vertę.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Scenarijaus Įrangos prastovos konfigūravimas programoje „Supply Chain Management“

Scenarijus **Įrangos prastovos** susieja signalą **PartOut** su įrenginio įspėjimo ribine verte. Įrenginys stebimas tik tada, kai jis pasirinktas scenarijuje ir nustatytas į **Vykdomas** programoje „Supply Chain Management“. Jeigu laikas nuo įrenginio paskutinio gauto signalo **PartOut** yra didesnis už įspėjimo ribinę vertę, suaktyvinamas pranešimas **Įrenginys neveikia**. Jeigu įrenginys vis dar veikia, kai gaunamas kitas signalas **PartOut**, suaktyvinamas pranešimas **Įrenginys veikia**. Jei įrenginys neveikia 30 min., suaktyvinamas naujas pranešimas **Įrenginys neveikia**.

Scenarijus **Įrangos prastovos** turi toliau nurodytas priklausomybes.

+ Norint suaktyvinti įspėjimą, susietame įrenginyje turi būti paleistas gamybos užsakymas.
+ Signalas, atitinkantis susieto įrenginio signalą **PartOut**, turi būti išsiųstas į „IoT Hub“ ir turi būti įtrauktas unikalus ypatybės pavadinimas.
+ „UNIX” **laiko žymos** ypatybė, kurioje vertė išreiškiama milisekundėmis (ms), turi būti „Azure IoT Hub” pranešime.

Norėdami konfigūruoti scenarijų, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Supply Chain Management“.
2. Įgalinkite IoT analizės funkcijos vėliavėlę. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
3. Sukonfigūruokite metriką. Daugiau informacijos žr. [Kaip sukonfigūruoti metriką](iot-metrics-setup.md#configure-metrics).
4. Eikite į **Gamybos kontrolė \> Sąranka \> IoT įžvalgos \> Scenarijaus valdymas** .
6. Plytelėje **Įrangos prastovos** pasirinkite **Konfigūruoti**, kad būtų atidarytas konfigūravimo vedlys.

   Konfigūracijos vedlys prasideda puslapiu **Įrangos jutiklio schemos apibrėžimas**. Šiame puslapyje jūsų tikslas yra nustatyti schemą „Supply Chain Management”, kad ji atitiktų „IoT Hub” pranešimų „JavaScript Object Notation” (JSON) formatą. Galima apibrėžti kelias pranešimų schemas. Daugiau informacijos, žr. [Schemų formatai, skirti „IoT Hub“ pranešimams](iot-schema-format.md). Šiame pavyzdyje pranešimų apkrovoje yra pranešimų su toliau pateiktu formatu paketas.

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

7. Įtraukite į lentelę eilutę ir nustatykite toliau pateiktas reikšmes.

    1. Nustatykite lauką **Schemos pavadinimas** į **ID**.
    2. Nustatykite lauką **Schemos kelias** į **/payload\[\*\]/id**.
    3. Nustatykite lauką **Aprašas** į **Pranešimo ID**.

8. Įtraukite kitą eilutę į lentelę ir nustatykite toliau pateiktas reikšmes.

    1. Nustatykite lauką **Schemos pavadinimas** į **Laiko žyma**.
    2. Nustatykite lauką **Schemos kelias** į **/payload\[\*\]/timestamp**.
    3. Nustatykite lauką **Aprašas** į **Pranešimo laiko žyma**.

9. Įtraukite kitą eilutę į lentelę ir nustatykite toliau pateiktas reikšmes.

    1. Nustatykite lauką **Schemos pavadinimas** į **Reikšmė**.
    2. Nustatykite lauką **Schemos kelias** į **/payload\[\*\]/value**.
    3. Nustatykite lauką **Aprašas** į **Pranešimo reikšmė**.

    > [!NOTE]
    > Nereikia nurodyti visų pranešimo ypatybių. Nustatykite tik reikalingas ypatybes. Atlikdami ankstesnius veiksmus, nesukūrėte eilutės **Šakninė laiko žyma** . **Šakninė laiko žyma** kelias bus **/timestamp**.

10. Norėdami eiti į puslapį **Įrangos jutiklio schemos susiejimas** pasirinkite **Pirmyn**.
11. Eilutės **Įrangos išteklių ID** lauke **Schemos pavadinimas** pasirinkite **ID**.
12. Eilutės **UTC laikas** lauke **Schemos pavadinimas** pasirinkite **Laiko žyma**.
13. Eilutės **Dalinai sugeneruotas signalas** lauke **Schemos pavadinimas** pasirinkite **Reikšmė**.
14. Norėdami atidaryti puslapį **Įrangos išteklių ID konfigūracija** pasirinkite **Pirmyn**.
15. Atlikite toliau pateiktus veiksmus, norėdami susieti „IoT Hub“ pranešimų reikšmes su „Supply Chain Management“ ištekliais.

    1. Lentelėje **Signalo duomenų reikšmės** įtraukite naują eilutę. Lauke **Reikšmė** įveskite **IoTInt.Machine1225.PartOut**. Ši reikšmė gaunama iš JSON ypatybės **id** „IoT Hub“ pranešime.
    2. Pasirinkite **Įrašyti**.
    3. Lentelėje **Verslo įrašo susiejimas** pasirinkite **Naujas**. Numatytoji lauko **Verslo įrašo tipas** reikšmė yra įvesta automatiškai ir jums jos keisti nereikia.
    4. Lauke **Verslo įrašas** pasirinkite „Supply Chain Management“ įrenginio išteklių, iš kurio siunčiama ši signalo reikšmė.
    5. Pasirinkite **Įrašyti**.
    6. Kartokite šiuos veiksmus, norėdami įtraukti naujo verslo įrašo **Machine1226** susiejimą. Su vienu „Supply Chain Management“ įrašu galite susieti kelias signalo duomenų reikšmes.

16. Norėdami pasirinkti, kuriuos įrenginius apdoroti, naudokite stulpelį **Pasirinkta**. Jums nebūtina apibrėžti visų signalų reikšmių ir pasirinkti visų įrenginių.
17. Pasirinkite **Pirmyn**, jei norite pereiti į puslapį **Dalinai sugeneruoto signalo konfigūravimas**.
18. Lentelėje **Signalo duomenų reikšmės** įtraukite eilutę ir nustatykite lauką **Reikšmė** į **Teisinga**. Ši reikšmė gaunama iš JSON ypatybės **value** „IoT Hub“ pranešime. Savo scenarijuje galite pridėti tiek reikšmių, kiek reikia.
19. Pasirinkite **Įrašyti**.
20. Norėdami eiti į puslapį **Įrangos prastovos ribinė vertė** pasirinkite **Pirmyn**. Nurodyti įrenginiai yra anksčiau su signalo reikšmėmis susieti įrenginiai. Šiame puslapyje apibrėžiate ribinę vertę, kad nustatytumėte, ar įrenginys sugedo. Pavyzdžiui, jei nustatysite ribinę vertę į **10**, „Supply Chain Management“ sugeneruos pranešimą, jei 10 minučių iš įrenginio nebus gautas pranešimas **PartOut**.
21. Norėdami pereiti puslapį **Įgalinti scenarijų**, pasirinkite **Pirmyn**. Pasirinkite parinktį, norėdami įgalinti scenarijų.
22. Pasirinkite **Baigti**.

Scenarijaus sąranka baigta. IoT įžvalgų papildinys pradės automatiškai apdoroti „IoT Hub“ pranešimus.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Scenarijaus Produkto kokybė konfigūravimas programoje „Supply Chain Management“

Scenarijus **Produkto kokybė** sugeneruoja pranešimą, jei prekės atributas nepatenka į nurodytą diapazoną. Pavyzdžiui, jutiklis siųs kiekvienos prekės svorį į „IoT Hub“. Jei prekė per sunki arba per lengva, „Supply Chain Management“ sugeneruojamas pranešimas.

Scenarijus **Produkto kokybė** turi toliau nurodytas priklausomybes.

+ Tam, kad būtų suaktyvintas įspėjimas, gamybos užsakymas turi būti vykdomas susietame įrenginyje ir generuoti produktą, kuriame yra susieto paketo atributas.
+ Signalas, atitinkantis paketo atributą, turi būti išsiųstas į „IoT Hub“ ir turi būti įtrauktas unikalus ypatybės pavadinimas.
+ „UNIX” **laiko žymos** ypatybė, kurioje vertė išreiškiama milisekundėmis, turi būti „Azure IoT Hub” pranešime.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Scenarijaus Gamybos atidėjimai konfigūravimas programoje „Supply Chain Management“

Scenarijus **Gamybos atidėjimai** generuoja pranešimą, jei gamybos našumas yra mažesnis už ribinę vertę. Šiame scenarijuje signalas **PartOut** siunčiamas į „IoT Hub“ kiekvienai pagamintai prekei. Programoje „Supply Chain Management” užsakymo atidėjimas apskaičiuojamas pagal planuojamą gamybos užsakymo vykdymo laiką, prekių, kurias reikia pagaminti, skaičių, užduoties vykdymo laiką ir gautų signalų **PartOut** skaičių. Perspėjimas dėl atidėjimo sugeneruojamas, jei užduoties signalų **PartOut** skaičius yra mažesnis už ribinę vertę.

Scenarijus **Gamybos atidėjimai** turi toliau nurodytas priklausomybes.

+ Norint suaktyvinti įspėjimą, susietame įrenginyje turi būti paleistas gamybos užsakymas.
+ Signalas, atitinkantis susieto įrenginio signalą **PartOut**, turi būti išsiųstas į „Azure IoT Hub“ ir turi būti įtrauktas unikalus ypatybės pavadinimas.
+ „UNIX” **laiko žymos** ypatybė, kurioje vertė išreiškiama milisekundėmis, turi būti „Azure IoT Hub” pranešime.

## <a name="disable-a-scenario"></a>Scenarijaus išjungimas

Norėdami išjungti scenarijų, atlikite toliau nurodytus veiksmus.

1. Programoje „Supply Chain Management“ eikite į **Gamybos kontrolė \> Sąranka \> IoT įžvalgos \> Scenarijaus valdymas**.
2. Scenarijaus plytelėje pasirinkite **Konfigūruoti** .
3. Norėdami pereiti į paskutinį vedlio puslapį, pasirinkite **Pirmyn**.
4. Pasirinkite parinktį, norėdami išjungti scenarijų.
