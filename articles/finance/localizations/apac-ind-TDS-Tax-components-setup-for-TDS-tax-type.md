---
title: Nustatykite komponentus TDS mokesčių tipui
description: Šioje temoje paaiškinama, kaip nustatyti šaltinio išskaitomo mokesčio komponentus priemonės mokesčių išskaitomos išskaitomo mokesčio šaltinio mokesčių tipui. Taip pat paaiškinama, kaip nustatyti ribinę ribą, naudojamą skaičiuojant kiekvieno TDS komponento TDS.
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
ms.openlocfilehash: 9c86341f7528e2c85b813e4f825ae34f10680a9b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727123"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Nustatykite komponentus TDS mokesčių tipui

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti šaltinio išskaitomo mokesčio komponentus priemonės mokesčių išskaitomos išskaitomo mokesčio šaltinio mokesčių tipui. TDS komponentai yra TDS, papildomas mokestis, PE-Jaus ir SHE paslaugos. Taip pat temoje paaiškinama, kaip nustatyti ribinę ribą, naudojamą skaičiuojant kiekvieno TDS komponento TDS. Be to, galite nustatyti išimties ribinę vertę, naudojamą skaičiuojant kiekvieno TDS komponento TDS.

Atlikite šiuos veiksmus TDS komponentams nustatyti.

1. Eikite į **Mokestis \> Nustatymai \> Išskaitomas mokestis \> Išskaitomo mokesčio komponentai**.

    [![Išskaitomo mokesčio komponentų puslapis.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Mokesčio **tipo lauke** pasirinkite **TDS** norėdami nustatyti TDS mokesčio tipo išskaitomo mokesčio komponentus.
3. Veiksmų srityje pasirinkite **Nauja** eilutei sukurti.
4. Lauke **Išskaitomo mokesčio komponentas** įveskite TDS komponento pavadinimą.
5. Lauke **Išskaitomo mokesčio komponentų grupė** pasirinkite TDS išskaitomo mokesčio komponentų grupę, prie kurios norite pridėti TDS komponentą.
6. **Bendra** „FastTab” skirtuke, **Aprašas** lauke, įveskite TDS komponento aprašą.
7. Veiksmų srityje pasirinkite **slenkstį** norėdami atidaryti **ribinės** vertės puslapį, kad būtų galima nustatyti ribinę vertę, naudojamą TDS komponento TDS apskaičiuoti.
8. Norėdami nustatyti laikotarpį, kada taikoma ribinė vertė, naudokite laukus **Nuo datos** ir **iki datos**.
9. „FastTab“ **Bendri** ribinės **vertės** lauke įveskite ribinės vertės sumą, naudojamą TDS komponento TDS apskaičiuoti. Mokestis iš šaltinio bus atskaitytas tik tada, kai kaupiamoji SF suma peržengia ribinę vertę.

    Pavyzdžiui, jei ribinė suma yra 10 000, TDS apskaičiuojama po kaupiamosios SF sumos, kuri viršija 10 000 (kitaip tariant, kai ji 10 001 ar daugiau).

10. Laukelyje **Išimties slenkstis** įveskite ribinės vertės sumą, naudojamą TDS komponento TDS apskaičiuoti. Mokestis sąskaitose eilutėje iš šaltinio bus atskaitytas tik tada, kai kaupiamoji SF suma peržengia išlygos vertę.

    Pavyzdžiui, jei ribinė išimties suma yra 5000, TDS skaičiuojama pagal konkrečią SF eilutę, jei SF eilutės suma viršija 5000 (kitaip tariant, jei ji 5001 ar daugiau).

    [![Ribinės vertės puslapis.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Ribinė išimties suma turi būti mažesnė už ribinės vertės sumą arba tokia pat.
    >
    > Operacijos mokestis atskaitomas, jei operacijos suma pereuoja išimties ribinę vertę, net jei kaupiamoji SF suma neišsiima ribinės vertės, nurodytos lauke **Ribinė** reikšmė.

11. Norėdami grįžti į **puslapį** Išskaitomo mokesčio **komponentai, uždarykite puslapį** Ribinė vertė.
12. Veiksmų srityje pasirinkite **Kopijuoti** norėdami atidaryti **Kopijuoti išskaitomo mokesčio komponentus** dialogo lauką, kad būtų galima kopijuoti TDS komponentus, kurie buvo nustatyti vienai TDS komponentų grupei į kitą TDS komponentų grupę.
13. Lauke **Iš** pasirinkite TDS komponentų grupę, iš kurios kopijuosite TDS komponentus. Lauke **Į** pasirinkiteišskaitomo mokesčio komponentų grupę, į šią grupę kopijuosite TDS komponentus.

    > [!NOTE]
    > Bendrieji TDS komponentai, pridėti prie abiejų TDS komponentų grupių, nėra kopijuojami.

14. Norėdami **kopijuoti** ir kurti kitos TDS komponentų grupės TDS komponentus puslapyje **Išskaitomo mokesčio komponentai** pasirinkite Gerai.

    [![Kopijuoti išskaitomo mokesčio komponentų dialogo langą.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Uždarykite puslapį.
