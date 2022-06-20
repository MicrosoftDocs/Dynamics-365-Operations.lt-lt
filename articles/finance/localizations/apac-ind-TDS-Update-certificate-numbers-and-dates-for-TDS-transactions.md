---
title: Naujinkite sertifikato numerius ir datas TDS operacijoms
description: Šiame straipsnyje paaiškinama, kaip atnaujinti susigrąžinamų sertifikatų numerius ir datas, kurios buvo įrašytos tiekėjui, klientui ir ŠALTINIO (TDS) mokesčių atskaitomų mokesčių sąskaitoms.
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
ms.openlocfilehash: 147a27261a4a282550f0bacede78c9edd38b4fe6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904447"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Naujinkite sertifikato numerius ir datas TDS operacijoms

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip atnaujinti susigrąžinamų sertifikatų numerius ir datas, kurios buvo įrašytos tiekėjui, klientui ir ŠALTINIO (TDS) mokesčių atskaitomų mokesčių sąskaitoms. TDS operacijų sertifikatus galite peržiūrėti puslapyje **Atkurtini sertifikatai**. Galite atnaujinti sertifikatus, naudodami puslapį **Atnaujinti sertifikatus**.

Norėdami naujinti sertifikatų numerius ir datas, atlikite šiuos veiksmus TDS operacijoms.

1. Eikite į **Mokestis \> Deklaracijos \> Išskaitomas mokestis \> Naujintas sertifikatas**.

    [![Atnaujinti sertifikato puslapį.](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Skirtuko **Atnaujinti sertifikatą** puslapyje, skyriuje **Pasirinkti**, mokesčių **tipo lauke** pasirinkite **TDS**.
3. Lauke **Sertifikato numeris** pasirinkite kliento arba tiekėjo TDS sertifikato numerį.

    > [!NOTE]
    > Lauke **Sertifikato numeris** išvardyti tik TDS sertifikatų numeriai, kurių žymės langelis **Uždarytas** , skirtas **atkurti sertifikatų** puslapyje yra išvalytas.

    Laukas **Sertifikato data** rodo sertifikato datą. Lauke Sąskaitos tipas rodomas sąskaitos, už kurią gautas TDS sertifikato numeris, tipas, o lauke **Pavadinimas** rodomas sąskaitos **pavadinimas**.

5. Laukeliuose **Nuo datos** iki **Datos** rinkitės laikotarpio pradžios ir pabaigos datas, per kurį rodomos TDS operacijos.
6. Pasirinkite **Rodyti duomenis**, jei norite peržiūrėti TDS operacijas, užregistruotas pasirinktu laikotarpiu.

    Skirtuke **Peržiūra** viršutinės srities tinklelis rodo šią informaciją apie kiekvieną TDS operaciją, kuri buvo užregistruota tiekėjui arba klientui pasirinktu laikotarpiu:

    - **Kvitas** – TDS operacijos kvito numeris
    - **Data** – TDS operacijos registravimo data.
    - **Suma** – Sąskaitos suma, kuriai buvo suskaičiuota TDS.
    - **Mokesčio suma** – TDS mokesčio suma, apskaičiuota operacijai.

7. Norėdami perkelti konkrečias TDS operacijas iš viršutinio tinklelio į apatinį tinklelį, pasirinkite operacijas, tada pasirinkite **Įtraukti**. Arba pasirinkite **Įtraukti viską,** kad visos TDS operacijos būtų perkeltos iš viršutinio tinklelio į apatinį tinklelį.

    Norėdami perkelti konkrečias TDS operacijas arba visas TDS operacijas iš apatinio tinklelio į viršutinį tinklelį, naudokite mygtuką **Neįtraukti** arba **Pašalinti visus**.

8. Pasirinkite **Atnaujinti**, kad būtų **atnaujinti sertifikato** numerio **ir sertifikato datos** laukai, skirti TDS operacijoms apatiniame tinklelyje.
10. Eikite į **Mokesčiai \> Netiesioginiai mokesčiai \> Išskaitomi mokesčiai \> Atkuriami sertifikatai** ir rinkitės **Užklausa** orėdami peržiūrėti atnaujintas operacijų eilutes, kuriose yra naujų sertifikatų numeriai **Sertifikatų operacijos** puslapyje.

    [![Sertifikato operacijų sąrašo puslapis.](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
