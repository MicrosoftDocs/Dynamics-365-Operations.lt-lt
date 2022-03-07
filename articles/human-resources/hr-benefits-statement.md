---
title: Išmokų ataskaita
description: Išmokų išrašo ataskaitoje paaiškinamos išmokos, į kurias darbuotojas yra šiuo metu įtrauktas.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 65bf91faba049b3fed4d80e020d77b82e48cceb6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069000"
---
# <a name="benefit-statement"></a>Išmokų ataskaita


[!INCLUDE [PEAP](../includes/peap-2.md)]

Išmokų **išrašo ataskaitoje** paaiškinamos išmokos, į kurias darbuotojas yra šiuo metu įtrauktas. Ataskaitą gali pasiekti darbuotojas tiesiogiai arba išmokų administratorius. Išmokų **išraše pateikiamas** užregistruotų darbuotojo išmokų, padengimo parinkčių, išlaidų ir visų užregistruotų priklausomųjų arba gavėjų sąrašas. Galima išspausdinti vieno darbuotojo arba kelių darbuotojų išrašą.

> [!NOTE]
Funkcija **Išmokų pareiškimas** turi būti įjungta darbo srityje **Funkcijų valdymas**. Norint tai padaryti, išmokų valdymo funkcija turi būti įjungta funkcijų **valdymo srityje**. 


## <a name="importing-the-benefit-statement"></a>Importuojamas išmokų išrašas 

Turite importuoti **išmokų išrašą** naudodami ataskaitos konfigūraciją, kad būtų galima gauti **išmokų išrašą**. Norėdami tai padaryti, atlikite toliau nurodytus veiksmus:

1.  Eikite į **Sistemos administravimas** darbo sritį.

2.  Rinktis **elektroninės ataskaitos** plytelę.

3.  Eikite **į konfigūracijos teikėjus** ir pasirinkite **Saugyklos**.

  ![Pasirinkite Saugyklas.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Iš sąrašo pasirinkite **Personalo ištekliai**, tada pasirinkite **Atidaryti**.

    ![Konfigūracijų saugyklos.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Pasirinkite **išmokų išrašo modelį** kairiojoje srityje ir išplėskite jį, kad būtų **rodomas išmokų išrašo** formatas.

6.  Kairiojoje **srityje pasirinkite išmokų** išrašo formatą.

7.  Dešinėje ekrano pusėje bus **versijos** „FastTab". Pasirinkite **Importuoti**.

    ![„FastTab“ versijos.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Generuoti išmokų išrašą kaip PDF failą

Pagal numatytuosius nustatymus **išmokų išrašas** bus išspausdinta kaip „Microsoft Word“ dokumentas. Norėdami spausdinti PDF formatu, elektroninio ataskaitų paskirties vietoje **turėsite sukonfigūruoti pasirinktį**. 

1. Norėdami tai padaryti, eikite į **sistemos administravimo darbo sritį** > **elektroninėmis ataskaitomis** > **susijusios nuorodos** > **elektroninės ataskaitos paskirties**.

1.  Pasirinkite **Naujas**.

2.  Lauke **Nuoroda** pasirinkite formatą **Išmokų pareiškimo formatas**.

3.  **Failo paskirties** "FastTab" pasirinkite **Naujas**.

4.  Lauke **Pavadinimas** įveskite **Išmokų pareiškimo (PDF)**.

5.  Lauke **Failo komponento pavadinimas** įveskite arba pasirinkite **Išmokų pareiškimas**.

6.  Rinkitės **Konvertuoti į PDF** žymės langelį.

7.  Pasirinkti **parametrus** iš meniu elemento. 

    ![Failo paskirties vieta.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Pasirinkite **Failo** „FastTab", tada pasirinkite **Įgalinta**.

9.  Pasirinkite **Gerai**.
   
> [!NOTE]
> Išmokų valdymo funkcija yra peržiūros būsenos. Naudojant el. pašto paskirties vietos parametrą elektroninių ataskaitų **paskirties ataskaitoje yra žinoma** problema. Galite gauti klaidos pranešimą ir el. laiško išsiųsti nepavyks.

Išmokų **išrašą galima** generuoti iš šių puslapių:

-   **Išmokų valdymo darbo srities** > **saitų** > **ataskaitų** > **išmokų išrašas**

-   **Darbuotojų (senesnių formos)** > **asmeninės informacijos skirtuko** > **išmokų išrašas**

-   **Supaprastintas darbuotojo įrašų** > **išmokų ataskaitų** > **išmokų išrašas**

-   **Darbuotojų savitarnos** > **išmokų** > **Peržiūrėti išmokų išrašą**

> [!NOTE]
>  Prieigą prie **išmokų išrašo** darbuotojų **savitarnoje kontroliuoja** teisių **rodinio išmokų išrašas**. Tai yra **darbuotojų savitarnos išmokų** pareiga. Numatyta, kad ši teisė suteikiama darbuotojams.

## <a name="report-contents"></a>Ataskaitos turinys

Išmokų **išraše bus** išspausdinti patvirtinti darbuotojo plano pasirinkimai, įskaitant visus atsisakyus planus. Tolesnis paveikslėlis rodo šios ataskaitos pavyzdys. 

![Išmokų pareiškimo ataskaita.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Ataskaitoje bus rodomas **planas**, **padengimo pasirinktis**, **darbuotojo išlaidos**, ir **darbdavio išlaidos**. Ataskaitoje taip pat bus išvardyti visi įtraukti priklausomieji. Jei yra su planu susietų gavėjų, bus rodomi gavėjai ir jų paskirstymo prioritetas bei procentas.

Išmokų **išrašo ataskaitą** galima spausdinti keliems darbuotojams vienu metu naudojant įrašus, kad būtų **Įtraukti įrašai** „FastTab“ puslapyje **išmokų išrašas**.
