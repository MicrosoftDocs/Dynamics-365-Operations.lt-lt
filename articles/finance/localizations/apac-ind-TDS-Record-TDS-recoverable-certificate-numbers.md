---
title: Įrašykite TDS keičiamas sertifikato numerius
description: Šiame straipsnyje paaiškinama, kaip naudoti "Recoverable" sertifikatų puslapį norint įrašyti sertifikatų numerius ir datas, taikomas šaltinio (TDS) sertifikatams, kurie gauti konkrečiam tiekėjui, klientui arba DK.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 513412e292167795fad9d80b68e6e5e14dbd13c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853262"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Įrašykite TDS keičiamas sertifikato numerius

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip naudoti "Recoverable **" sertifikatų puslapį norint įrašyti sertifikatų numerius ir datas**, taikomas šaltinio (TDS) sertifikatams, kurie gauti konkrečiam tiekėjui, klientui arba DK. Norėdami atnaujinti TDS sertifikatų numerius ir datas, įrašytus šio puslapio TDS operacijoms, naudokite puslapį **Atnaujinti sertifikatą** (**DK \> Periodinis \> išskaitomo mokesčio \> atnaujinimo sertifikatas**). Baigę atnaujinti TDS sertifikatų numerius, uždarykite juos.

Norėdami įrašyti TDS sertifikatų numerius ir datas, atlikite šiuos veiksmus.

1. Pasirinkite **Mokestis \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Keičiamas sertifikatas**.

    [![Atkuriamų sertifikatų puslapis.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Puslapyje **Atkurti sertifikatai** plaukelyje **Mokesčio tipas** rinkitės **TDS**.
3. Pasirinkite **Naujas** pranešimui sukurti.
4. Lauke **Sertifikato numeris** įveskite TDS koncesijos sertifikato numerį.
5. Lauke **Sąskaitos tipas** pasirinkite sąskaitos, kurią TDS sertifikatas gavo, tipą: **Tiekėjas**, **klientas** arba **DK**.
6. Lauke **Sąskaita** pasirinkite tiekėjo, kliento arba DK sąskaitos numerį, atsižvelgdami į pasirinktą sąskaitos tipą. Lauke **Pavadinimas** rodomas tiekėjo, kliento arba DK sąskaitos pavadinimas.
7. Laukelyje **Sertifikato suma** įveskite TDS sertifikato sumą.
8. Lauke **Data** įveskite sertifikato data jo numeriui.
9. Rinkitės **Užklausos** norėdami atidaryti **sertifikato operacijų** puslapį, kuriame galite peržiūrėti TDS operacijas, kurių TDS sertifikato numeris ir data yra atnaujinami. Šią informaciją galima atnaujinti puslapyje **Naujinti sertifikatą** (**Mokesčių \> deklaracijų \> išskaitomo mokesčio \> Naujinti sertifikatą**).

    Atnaujinimo **sertifikato puslapyje** rodoma ši kiekvienos TDS operacijos informacija:

    - **Data** – TDS operacijos registravimo data.
    - **Kvitas** – TDS operacijos kvito numeris
    - **Šaltinis** – modulis, kuriame sukurta TDS operacija.
    - **Sąskaita** – tiekėjo, kliento ar DK sąskaitos numeris, kuriam buvo sukurta TDS operacija.
    - **Pavadinimas** – tiekėjo, kliento ar DK sąskaitos pavadinimas, kuriam buvo sukurta TDS operacija.
    - **Suma** – Sąskaitos suma, kuriai buvo suskaičiuota TDS.
    - **Mokesčio suma** – TDS mokesčio suma, apskaičiuota operacijai.
    - **Sertifikato data** – TDS sertifikato data, kuri buvo atnaujinta TDS operacijai.
    - **Sertifikato numeris** – TDS sertifikato numeris, kuris buvo atnaujinta TDS operacijai.

10. Puslapyje **Atkurtini sertifikatai** pažymėkite **Uždaryta** žymimą laukelį, kad uždarytumėte TDS sertifikato numerį po to, kai užbaigėte TDS operacijų atnaujinimą **Sertifikato naujinimo** puslapyje.

    Norėdami pasirinkti **Uždaryta** žymimą laukelį visiems įrašams puslapyje, rinkitės **Žymėti viską**.

    > [!NOTE]
    > TDS sertifikatų numeriai, kurių **pasirinktas** žymės langelis Uždaryta, nepasiekiami puslapyje **Atnaujinti sertifikatą**.
