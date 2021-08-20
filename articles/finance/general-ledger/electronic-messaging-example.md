---
title: Nustatykite ir vykdykite apdorojimą norėdami iškviesti paprastą eksportavimo ER formatą „Excel“ ataskaitai sugeneruoti
description: Šioje temoje pateikiamas pavyzdys, pademonstruojantis, kaip nustatyti ir naudoti elektroninius pranešimus.
author: liza-golub
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a5fd466c98e0855f7a33929eeee42b9147d26ba19780b4ae7c8eb895ac27ea5e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737682"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Nustatykite ir vykdykite apdorojimą norėdami iškviesti paprastą eksportavimo ER formatą „Excel“ ataskaitai sugeneruoti

[!include [banner](../includes/banner.md)]

Sukūrę savo ER formatą, susieję jį su duomenų šaltiniais ir užbaigę, galite paleisti jį iš darbo srities **Elektroninės ataskaitos**. Sugeneravę ataskaitą, galite ją įrašyti vietoje.

Norėdami kontroliuoti šiuos ataskaitų teikimo proceso aspektus, nustatykite elektroninių pranešimų apdorojimą:

- Užregistruokite informaciją apie tai, kas sugeneravo ataskaitą.
- Užregistruokite informaciją apie tai, kada ataskaita buvo sugeneruota.
- Įrašykite ankstesnių laikotarpių sugeneruotas ataskaitas.

Šiame pavyzdyje rodoma, kaip galite nustatyti elektroninius pranešimus generuoti ataskaitai, kuri pagrįsta ER eksportavimo formatu, skirtu „Microsoft Excel”. Jei norite vadovautis šiuo pavyzdžiu, eksportavimo ER formatas, skirtas „Excel”, jau turi būti sukurtas, susietas su duomenų šaltiniais ir užbaigtas. Be to, jau turi būti nustatyta elektroninių pranešimų numeracija.

Tai naudinga, jei kurdami apdorojimą pirmiausia apibrėžiate apdorojimo veiksmus ir būsenas, kurios bus nustatytos. Šioje iliustracijoje rodomas apdorojimas pagal šį pavyzdį.

![Apdorojimo schema](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Kurti pranešimo būsenas

1. Eikite į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimo būsenos**.
2. Kurti toliau nurodytas pranešimo būsenas.

    - Naujas
    - Parengta
    - Sugeneruota

    ![Pranešimo būsenos](media/message-statuses.png)

3. Būsenos **Nauja** eilutėje pasirinkite **Leisti naikinti** žymės langelį, kad vartotojai galėtų panaikinti šią būseną turinčius pranešimus.

## <a name="create-additional-fields"></a>Kurti papildomus laukus

1. Eikite į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Papildomi laukai**.
2. Pridėkite papildomą lauką ir jo vertes.
3. Parinktį **Vartotojo redaguojamas** nustatykite į **Taip**, kad vartotojai galėtų redaguoti lauką.

![Papildomi laukai](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Kurti pranešimų apdorojimo veiksmus

Šiam pavyzdžiui galite sukurti toliau nurodytus pranešimų apdorojimo veiksmus:

- **Kurti pranešimą**
- **Atnaujinti į parengtą**
- **Generuoti ataskaitą**
- **Atnaujinti į pradinę būseną** (pasirinktinai)

Atlikite šiuos žingsnius, kad sukurtumėte veiksmus.

1. Eikite į **Mokesčiai** \> **Nustatymas** \> **Elektroniniai pranešimai** \> **Pranešimų apdorojimo veiksmai**.
2. Kurti veiksmą, kurio pavadinimas **Kurti pranešimą**. „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Kurti pranešimą**.
3. Kurti veiksmą, kurio pavadinimas **Atnaujinti į parengtą**, ir nustatyti toliau nurodytus laukus.

    - „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Pranešimų lygio vartotojų apdorojimas**.
    - „FastTab“ skirtuko **Pradinės būsenos** lauke **Pranešimo būsena** pasirinkite **Nauja**.
    - „FastTab“ skirtuko **Galutinės būsenos** lauke **Pranešimo būsena** pasirinkite **Parengta**. Lauke **Atsakymo tipas** įveskite **Sėkmingai įvykdyta**.

4. Kurti veiksmą, kurio pavadinimas **Generuoti ataskaitą**, ir nustatyti toliau nurodytus laukus.

    - „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Elektroninių ataskaitų eksportavimas**. Lauke **Formato susiejimas** pasirinkite ER eksportavimo formatą. Parinktys yra **Excel**, **XML**, **JSON**, **Tekstas** ir **Kita**.
    - „FastTab“ skirtuko **Pradinės būsenos** lauke **Pranešimo būsena** pasirinkite **Parengta**.
    - „FastTab“ skirtuko **Galutinės būsenos** lauke **Pranešimo būsena** pasirinkite **Sugeneruota**. Lauke **Atsakymo tipas** įveskite **Sėkmingai įvykdyta**.

    ![Generuoti ataskaitos veiksmą](media/generate-report-action.png)

5. Pasirinktinai: Norėdami leisti vartotojams pakartotinai keletą kartų generuoti ataskaitą, sukurkite veiksmą, pavadinimu **Atnaujinti į pradinę būseną** ir nustatykite toliau nurodytus laukus:

    - „FastTab“ skirtuko **Bendras** lauke **Veiksmo tipas** pasirinkite **Pranešimų lygio vartotojų apdorojimas**.
    - „FastTab“ skirtuko **Pradinės būsenos** lauke **Pranešimo būsena** pasirinkite **Sugeneruota**.
    - „FastTab“ konteineryje **Rezultatų būsenos** įtraukite atskirą eilutę kiekvienai iš dviejų pranešimo būsenų (**Paruoštas** ir **Naujas**). Abiejose eilutėse lauką **Atsako tipas** nustatykite kaip **Sėkmingai įvykdytas**.

## <a name="electronic-message-processing"></a>El. pranešimų apdorojimas

Šiam pavyzdžiui visi veiksmai turi būti nustatyti taip, kad jie būtų vykdomi atskirai. Daroma prielaida, kad kiekvieną veiksmą inicijuos vartotojas.

1. Eikite į **Mokesčiai** \> **Sąranka** \> **El. pranešimai** \> **El. pranešimų apdorojimas**.
2. Prie savo apdorojimo pridėkite įrašą ir įtraukite visus anksčiau apibrėžtus veiksmus bei papildomą lauką.
3. Pasirinktinai. „FastTab“ konteineryje **Saugos vaidmenys** apibrėžkite savo apdorojimo saugos vaidmenis, kad apribotumėte prieigą prie konkrečių ataskaitų.
4. Eikite į **Mokesčiai** \> **Užklausos ir ataskaitos** \> **Elektroniniai pranešimai** \> **Elektroniniai pranešimai**.
5. Pasirinkite **Naujas** pranešimui sukurti. Šiuo metu galite pridėti datas ir aprašą. Taip pat galite atnaujinti papildomo lauko vertę, kaip jums reikia.

    ![Elektroninio pranešimo kūrimas](media/create-electronic-message.png)

    „FastTab“ skirtuke **Veiksmų žurnalas** esančiame tinklelyje automatiškai užpildomas visų pranešime atliekamų veiksmų žurnalas.

    Dabar jūs galite panaikinti ar atnaujinti pranešimo būseną. 

6. Norėdami atnaujinti pranešimo būseną, pasirinkite **Atnaujinti būseną**. Lauke **Nauja būsena** pasirinkite **Paruoštas**, tada – **Gerai**.

    ![Pranešimo būsenos atnaujinimas](media/update-status.png)

    Pranešimo būsena atnaujinta į **Paruošta**.

7. Sugeneruokite ataskaitą pasirinkdami **Generuoti ataskaitą**.

    Ataskaita sugeneruota, o pranešimo būsena ir veiksmų žurnalas atnaujinti.

8. Norėdami peržiūrėti sugeneruotą ataskaitą, viršutiniame dešiniajame puslapio kampe pasirinkite mygtuką **Priedas** (sąvaržėlės simbolis).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
