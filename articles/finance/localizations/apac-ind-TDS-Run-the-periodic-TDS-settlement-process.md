---
title: Vykdyti periodinį TDS sudengimo procesą
description: Šioje temoje paaiškinama, kaip sudengti šaltinyje (TDS) išskaitomą periodinį mokestį.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: cfab08a4190bf51518bd4a9b445b229a5081e87d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023437"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Vykdyti periodinį TDS sudengimo procesą

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sudengti šaltinyje (TDS) išskaitomą periodinį mokestį.

1. Eikite į **Mokestis \> Deklaracijos \> Išskaitomas mokestis \> Išskaitomo mokesčio mokėjimas**.

    [![Išskaitomo mokesčio mokėjimo teksto laukelis](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Teksto laukelyje **Išskaitomo mokesčio mokėjimas** laukelyje **mokesčio tipas** rinkitės **TDS**.
3. Lauke **Mokesčių sąskaitos numeris (TAN)** pasirinkite mokesčių sąskaitos numerį (TAN), norėdami vykdyti sudengimo procesą.
4. Lauke **Išskaitomo mokesčio komponentų grupė** pasirinkite TDS komponentų grupę, kurios sudengimo procesą norite vykdyti.
5. Lauke **Sudengimo laikotarpis** pasirinkite TDS sudengimo laikotarpį, vykdyti sudengimo procesą.

    > [!NOTE]
    > TDS sudengimo procesas vykdomas visiems laikotarpiams, kurie nustatyti TDS sudengimo **laikotarpiui** skirtuke **išskaitomo mokesčio sudengimo laikotarpių** puslapyje (**Mokesčių \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Išskaitomų mokesčių sudengimo laikotarpiai**).

6. Lauke **Pradžios data** pasirinkite pradžios datą, nuo kurios bus vykdomas TDS sudengimo procesas.

    Tam tikro laikotarpio sudengimo laikotarpio pradžios data, nurodyta laikotarpiui, yra paimta kaip „nuo" data. Pavyzdžiui, TDS sudengimo laikotarpis turi du laikotarpius: nuo balandžio 1 iki 2009 m. balandžio 30 d. ir nuo 2009 m. gegužės 1 d. iki gegužės 31 d. Jei pasirinkote **2009 06 04** (2009 m. balandžio 6 d.), sudengimo procesas vis tiek bus vykdomas **nuo** 2009 m. balandžio 1 d.

    Jei į lauką **Pradžios data** įvesite vėlesnį laikotarpį, bet nesudengsite ankstesnio sudengimo laikotarpio, sudengimas nebus taikomas jokiam ankstesniam laikotarpiui. Pavyzdžiui, TDS sudengimo laikotarpis yra trijų laikotarpių: nuo balandžio 1 iki 2009 m. balandžio 30 d., nuo 2009 m. gegužės 1 iki gegužės 31 d. ir nuo 2009 m. birželio 1 d. iki birželio 30 d. Jei kaip pradžios datą pasirinksite **2009-05-01** (2009 m. gegužės 1 d.), lauke Nuo datos bus vykdoma sudengimo procesas tik nuo 2009 m. gegužės 1 **iki** gegužės 31 d. Sudengimas nebus sudengtas nuo 2009 m. balandžio 1 d. iki balandžio 30 d.

7. Lauke **Operacijos data** pasirinkite pradžios datą, nuo kurios bus publikuojama TDS sudengimo operacija.
8. Teksto laukelyje **Išskaitomo mokesčio mokėjimas** rinkitės TDS išskaitymo versiją:

     - **Originalas** – naudokite šią pasirinktį, norėdami pirmą kartą vykdyti TDS sudengimo procesą. Pradinė mokėjimo versija naudojama tik vieną kartą, norint paleisti TDS sudengimo procesą, kai naudojama TAN, išskaitomo mokesčio komponentų grupės ir išskaitomo mokesčio sudengimo laikotarpio kombinacija.
    - **Paskutinės versijos** – naudokite šią pasirinktį, jei TDS sudengimo procesas tam tikrą laikotarpį jau buvo paleistas. Įtraukti operacijas atgalinės datos, kurios buvo užregistruotos po to, kai laikotarpio sudengimo procesas buvo paleistas anksčiau. Šią pasirinktį galite naudoti norėdami bet kiek kartų vykdyti sudengimo procesą.

9. Pažymėkite žymės **langelį** Atnaujinti, norėdami vykdyti TDS sudengimo procesą ir registruoti sumas DK sąskaitose. Jei šis žymės langelis išvalytas, sudengimo procesas nebus vykdomas ir nebus sugeneruoti finansiniai įrašai.
10. Pasirinkite **Gerai** norėdami vykdyti TDS sudengimo procesą ir sugeneruoti išskaitomo mokesčio mokėjimo ataskaitą. Į sudengimo procesą įtrauktų TDS operacijų būsena rodoma kaip **Sudengta** puslapyje **Sudengta** (eikite į **Mokėtinos sumos \> Mokėjimai \> Tiekėjo mokėjimo žurnalas**, rinkitės **Eilutės**, rinkitės **Funkcijos** ir tada **Sudengimas**).

### <a name="important-points"></a>Svarbūs taškai

- Jei išskaitomo mokesčio komponentų grupė nėra pasirinkta sudengimo proceso metu, sudengimas įvyksta visoms pasirinkto TAN ir sudengimo laikotarpio išskaitomo mokesčio komponentų grupėms. Kiekvienai išskaitomo mokesčio komponentų grupei sukuriama atskira eilutė **atvirų operacijų redagavimo** puslapyje.
- Sudengimo procesas pagrįstas sudengimo laikotarpio vertinimo kategorijos būdu. Operacijos, kurių vertinimo tikslas yra **Įmonė** sudengtos ir yra rodomos kaip viena eilutė **atvirų operacijų redagavimo** puslapyje. Operacijos, kurių vertinimo tikslas yra kas nors, o ne **Įmonė** sudengtos ir yra rodomos kaip viena eilutė **atvirų operacijų redagavimo** puslapyje.
- Sudengtos TDS operacijos eilučių terminas **atvirų operacijų redagavimo** puslapyje yra pagrįstas mokėjimo sąlygomis, apibrėžtomis TDS institucijos tiekėjui **tiekėjų** puslapyje. Jei TDS institucijos tiekėjui mokėjimo sąlygos nėra nustatytos, kaip terminas rodoma paskutinė sudengimo laikotarpio diena.
