---
title: Finansinis konsolidavimas tinkle
description: Šioje temoje aprašomas finansinis konsolidavimas Didžiojoje knygoje.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 86be6d4cc0af3f2fd92523d4ecd3825f2383fc48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445987"
---
# <a name="online-financial-consolidations"></a>Finansinis konsolidavimas tinkle

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas finansinis konsolidavimas Didžiojoje knygoje. Prieš skaitydami šią temą, būtinai perskaitykite temą [Finansinio konsolidavimo ir valiutos konvertavimo apžvalga](financial-consolidations-currency-translation.md).

Atlikę sąranką įveskite konsolidavimo informaciją puslapyje **Konsolidavimas [tinkle]**. Baigę galite spustelėti **Gerai** arba **Paketas**, kad apdorotumėte konsolidavimą.

## <a name="criteria"></a>Kriterijai
Puslapio **Konsolidavimas [tinkle]** skirtuke **Kriterijai** galite nustatyti konsolidavimo sąskaitas, laikotarpius ir duomenų tipą.

![Kriterijų skirtukas](./media/criteria-consolidate-online.png "Kriterijų skirtukas")

Čia pateikiamas šiame skirtuke esančių įvairių laukų paaiškinimas.

- **Aprašas** – įveskite tikslų konsoliduojamo laikotarpio aprašą.
- **Pagrindinė sąskaita** – naudokite laukus šioje skiltyje, kad nustatytumėte pagrindines sąskaitas, kurios bus apdorojamos.

    - **Nuo** ir **Iki** – nurodykite apdorojamų sąskaitų diapazoną. Jei šie laukai paliekami tuščias, visos visų įmonių sąskaitos bus perkeltos į konsoliduotą įmonę. Todėl, jei konsoliduojate keturias įmones, o kiekviena įmonė turi skirtingą sąskaitų planą, visos visų keturių įmonių sąskaitos bus sukurtos konsoliduotoje įmonėje.
    - **Naudoti konsolidavimo sąskaitą** – jei šią pasirinktį nustatote į **Taip**, galima naudoti lauką **Pasirinkti konsolidavimo sąskaitą iš**. Šiame lauke pasirinkite, ar visos sąskaitos turi būti konsoliduotos konsolidavimo sąskaitoje, kuri yra nustatyta puslapyje **Pagrindinės sąskaitos**, ar norite pasirinkti sąskaitą iš vienos iš konsolidavimo sąskaitų grupių.
    - **Konsolidavimo sąskaitų grupės** – pasirinkite grupę, kurią naudosite susiedami konsolidavimo pagrindinę sąskaitą.

- **Konsolidavimo laikotarpis** – naudokite laukus šioje skiltyje, kad nurodytumėte konsolidavimo laikotarpį.

    - **Nuo** ir **Iki** – nurodykite konsolidavimo datų diapazoną. Jei šis laukas paliekamas tuščias, konsolidavimas bus taikomas visiems laikotarpiams, kurie apibrėžti įmonės DK kalendoriuje. Nerekomenduojama palikti šiuos laukus tuščius.
    - **Įtraukti faktines sumas** – nustatykite šią parinktį į **Taip**, konsoliduotumėte savo faktinius duomenis.
    - **Įtraukti biudžeto sumas** – nustatykite šią parinktį į **Taip**, kad konsoliduotumėte duomenis iš biudžeto registro.
    - **Perkurti balansus vykdant konsolidavimą** – nerekomenduojame nustatyti šią parinktį į **Taip**. Vietoje to atkurkite balansus kaip atskirą paketinę užduotį.

- **Biudžeto modeliai** – jei pasirinkote konsoliduoti biudžeto duomenis, naudokite laukus šioje skiltyje, kad nustatytumėte biudžeto modelius.

    - **Nuo** ir **Iki** – nurodykite naudotinų modelių diapazoną.
    - **Biudžeto kurso tipas** – pasirinkite biudžeto kurso tipą, kuris bus naudojamas konvertuojant biudžeto duomenų valiutą.

## <a name="financial-dimensions"></a>Finansinės dimensijos
Skirtuke **Finansinės dimensijos** galite nustatyti dimensijas, kurios turi būti įtrauktos į konsoliduotą įmonę. Norėdami pasirinkti dimensiją, nustatyti lauką **Specifikacija** į parinktį **Dimensijos**, o tada nurodykite dimensijų tvarką konsoliduotoje įmonėje.

![Finansinių dimensijų skirtukas](./media/financial-dimensions-cons.png "Finansinių dimensijų skirtukas")

Nepaisant nurodytos tvarkos, **Pagrindinės sąskaita** visada bus pirmajame segmente.

## <a name="legal-entities"></a>Juridiniai subjektai
Skirtuke **Juridiniai subjektai** galite nustatyti įmones, kurios turi būti įtrauktos į konsoliduotą įmonę. Taip pat galite nustatyti tų įmonių nuosavybės procentą. Jei nurodysite mažiau nei 100 procentų nuosavybės, nurodytas procentas bus sumuojamas konsoliduotoje įmonėje. Jei yra konvertavimo skirtumų, laukas **Skirtumų konvertavimo sąskaitos tipas** naudojamas norint pasirinkti pagrindinę sąskaitą iš sąrankos puslapyje **Automatinių operacijų sąskaitos**.

![Juridinių subjektų skirtukas](./media/legal-entities-cons.png "Juridinių subjektų skirtukas")

![Automatinių operacijų sąskaitų puslapis](./media/accounts-for-automatic-cons.png "Automatinių operacijų sąskaitų puslapis")

## <a name="elimination"></a>Pašalinimas
Skirtuke **Pašalinimas** galite rinktis iš trijų toliau nurodytų apdorojimo pašalinimo parinkčių.

- Pasirinkite pašalinimo taisyklę, tada lauke **Pasiūlymo pasirinktys** pasirinkite **Tik pasiūlymas**. Pasirinkus šią parinktį pašalinimas bus apdorotas konsolidavimo proceso metu, tačiau viskas nebus registruojama vienu veiksmu. Žurnalą galima užregistruoti vėliau.
- Pasirinkite pašalinimo taisyklę, tada lauke **Pasiūlymo pasirinktys** pasirinkite **Tik registravimas**. Pasirinkus šią parinktį pašalinimas bus apdorotas konsolidavimo proceso metu ir viskas bus registruojama vienu veiksmu.
- Pašalinimo procesą vykdykite atskirai nuo konsolidavimo proceso naudodami pašalinimo žurnalą.

![Pašalinimo skirtukas](./media/elimination-cons-onl.png "Pašalinimo skirtukas")

Daugiau informacijos apie pašalinimą žr. [Pašalinimo taisyklės](./elimination-rules.md).

## <a name="currency-translation"></a>Valiutos konvertavimas
Skirtuke **Valiutos konvertavimas** galite nurodyti juridinį subjektą, sąskaitą ir valiutos kurso tipą bei kursą. Galima rinktis iš trijų parinkčių lauke **Taikyti valiutos kursą iš**.

- **Konsolidavimo data** – konsolidavimo data bus naudojama valiutos kursui nustatyti. Šis kursas yra lygus vietos ar mėnesio pabaigos kursui. Matysite kurso peržiūrą, tačiau negalėsite jo redaguoti.
- **Operacijos data** – kiekvienos operacijos data bus naudojama pasirenkant valiutos kursą. Ši parinktis dažniausiai taikoma ilgalaikiam turtui ir dažnai vadinama retrospektyviniu kursu. Negalite matyti kurso peržiūros, nes sąskaitų diapazone bus pateikta daug įvairių operacijų kursų.
- **Vartotojo nurodytas kursas** – pasirinkę šią parinktį, galite įvesti norimą valiutos kursą. Ši parinktis gali būti naudinga taikant vidutinius valiutos keitimo kursus arba konsoliduojant pagal fiksuotą valiutos kursą.

![Valiutos konvertavimo skirtukas](./media/currency-translation-cons-online.png "Valiutos konvertavimo skirtukas")

## <a name="additional-resources"></a>Papildomi ištekliai

Daugiau informacijos apie konsolidavimą ir valiutų konvertavimą žr. pagrindinėje šios temos temoje [Finansinio konsolidavimo ir valiutų konvertavimo apžvalga](./financial-consolidations-currency-translation.md).

Informacijos apie scenarijus, kuriais galite generuoti konsoliduotas finansines ataskaitas, žr. [Konsoliduotų finansinių ataskaitų generavimas](./generating-consolidated-financial-statements.md).
