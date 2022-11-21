---
title: Tiekėjo SF datos
description: Šiame straipsnyje aprašomos datos, kurios rodomos tiekėjo SF. Taip pat paaiškinama, kaip automatiškai koreguoti registravimo datą.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775278"
---
# <a name="vendor-invoice-dates"></a>Tiekėjo SF datos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos datos, kurios rodomos tiekėjo SF. Taip pat paaiškinama, kaip automatiškai koreguoti registravimo datą.

Išsamaus **laukiančios tiekėjo SF puslapio** SF antraštėje rodomos keturios datos: **SF gavimo data**,**SF** data, **registravimo** data ir **terminas**. Kai sukuriama tiekėjo SF, pagal numatytuosius nustatymus įvedamos šios datos:

- **SF gavimo data** – šis laukas nustatytas kaip dabartinė sistemos data.
- **Registravimo data** – šis laukas nustatytas kaip dabartinė sistemos data. 
- **Terminas** – data šiame lauke skaičiuojama pagal registravimo datą ir mokėjimo terminus.
- **SF data** – pagal numatytąjį nustatymą šis laukas yra tuščias. Tačiau šio lauko reikšmę galite įvesti kokia jums reikalinga. Tokiu atveju, data laukelyje **Terminas** yra perskaičiuojama pagal SF datą ir mokėjimo terminus.

Kartais tiekėjo SF būsena gali būti laukiama daug laiko po laikotarpio uždarymo. Kai jis parengtas registruoti, vis dar naudojama senoji praėjusio registravimo laikotarpio registravimo data. Tačiau šis laikotarpis dabar uždarytas. Todėl mokėtinų sumų (AP) klerkas neautomatiniu būdu turi pakeisti visas registravimo datas į naują registravimo laikotarpį visoms anksčiau sukurtoms laukiančioms SF.

Šiame straipsnyje aprašyta funkcija leidžia automatiškai koreguoti registravimo datą pagal verslo poreikius.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parametras, skirtas tiekėjo SF registravimo datai automatiškai koreguoti

Norėdami automatiškai koreguoti tiekėjo SF registravimo datą, atlikite šiuos veiksmus.

1.  Eikite į **Mokėtina suma \> Sąranka \> Mokėtinos sumos parametrai**.
2.  Skirtuko **DK ir PVM** lauke **Koreguoti registravimo datą automatiškai** pasirinkite vieną iš šių verčių:

    - **Nėra pakeitimų** – sistema registravimo datos automatiškai nekeičia registravimo metu. Pagal numatytuosius nustatymus ši vertė yra pasirinkta.
    - **Visada keisti registravimo datą į sistemos datą** – registravimo data registravimo metu automatiškai keičiama į sistemos datą.
    - **Keisti registravimo** datą į sistemos datą, kai registravimo datos laikotarpis uždarytas arba sulaikytas – registravimo data registravimo metu automatiškai keičiama į sistemos datą, tačiau tik tuo atveju, **·** **jei atitinkamo registravimo datos laikotarpio būsena yra Uždaryta arba Sulaikyta.**
    - **Keisti registravimo** datą į pirmą naujo laikotarpio dieną, kai registravimo datos laikotarpis uždarytas arba sulaikytas – registravimo data pakeičiama į pirmą naujo atviro laikotarpio dieną, tačiau tik tuo atveju, **·** **jei atitinkamo registravimo datos laikotarpio būsena yra Uždaryta arba Sulaikyta.**

> [!NOTE]
> Jei nauja automatiškai pakoreguota registravimo data yra naujais finansiniais metais, SF registravimo data nebus atnaujinta. Vartotojas gaus klaidą "Finansiniai metai pasikeitė. Patikrinkite ir iš naujo įveskite registravimo datą. Norint registruoti, SF registravimo data turi būti atnaujinta į naujus finansinius metus.

## <a name="impact-of-posting-date-changes"></a>Registravimo datos keitimų poveikis

Kai laukiančio tiekėjo SF registravimo data pakeičiama, keitimas turi tokį poveikį:

- **Terminas**

    - Jei **SF datos** laukelis yra tuščias, termino data yra perskaičiuojama pagal naują registracijos datą ir mokėjimo terminus.
    - Jei **SF datos** laukas buvo anksčiau nustatytas, registravimo datos pakeitimas neturi įtakos termino datai.

- **Mokėjimo nuolaidos data**

    - Jei **SF datos** laukas yra tuščias, mokėjimo nuolaidai apskaičiuoti naudojama nauja registravimo data.
    - Jei **SF datos** laukas buvo nustatytas anksčiau, mokėjimo nuolaida nėra keičiama.

- **Valiutos kursas** – valiutos kurso data nurodoma nustatant **Tiekėjo apskaitos naujinimo parametrą, naudojant SF datos** parinktį **SF** skirtuke **Mokėtinų sumų parametrai** puslapyje (**Mokėtina suma \> Parametrai \> Mokėtinų sumų parametrai**).

    - Jei ši pasirinktis nustatyta **kaip Taip** **, naudojama** SF data, **o** registravimo datos pakeitimas neturi įtakos valiutos kursui.
    - Jei ši pasirinktis nustatyta kaip **Ne**, registravimo data naudojama valiutos keitimo kursams skaičiuoti. Kai registravimo data atnaujinama, apskaitos ir ataskaitų sumos perskaičiuojamos. Todėl tikrinimą reikia patikrinti dar kartą.

## <a name="validation"></a>Patikrinimas

Kiti du **SF** skirtuko laukai **Mokėtinų sumų parametrai** puslapyje (**Mokėtinos sumos \> Parametrai \> Mokėtinos sumos parametrai**) paveikia SF apdorojimą:

- Jei lauke **Tikrinti naudojamą SF numerį** **nustatyta** atmesti finansinių metų dublikatus, registravimo data bus naudojama norint patikrinti, ar SF registravimo metu nėra pasikartojančių SF.
- Jei **Reikalaujama dokumento data tiekėjo SF** lauke nustatyta kaip **Klaidinga parinktis** **Laukiančios SF antraštės SF data** laukas reikalaujamas. Jei SF data yra vėlesnė nei registravimo data, bus rodomas klaidos pranešimas.
