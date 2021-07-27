---
title: Darbo užsakymo projekto sąranka
description: Šioje temoje aiškinama darbo užsakymo projekto sąranka modulyje „Turto valdymas”.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 19cdc33fcc9d1293b235facbaffd1ccf62875217
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360058"
---
# <a name="work-order-project-setup"></a>Darbo užsakymo projekto sąranka

[!include [banner](../../includes/banner.md)]

 

Modulyje **Turto valdymas** kiekvieną darbo užsakymo užduotį būtina susieti su projektu. Su darbo užsakymo užduotimi susietas projektas leidžia sekti įvairių projektų, susijusių su moduliu „Turto valdymas”, pvz., vidaus priežiūros, aptarnavimo valdymo ir investicinių projektų, išlaidas. 

## <a name="project-setup-for-a-work-order-job"></a>Darbo užsakymo užduoties projekto sąranka

Kai darbo užsakyme sukuriama darbo užsakymo užduotis, remiantis projekto sąranka modulyje **Projektų valdymas ir apskaita** ir darbo užsakymo projekto sąranka modulyje **Turto valdymas** nustatoma, kaip projektai gali būti naudojami turto, kuris pasirenkamas toje darbo užsakymo užduotyje, išlaidoms valdyti. Šiame skyriuje apibrėžiamos toliau nurodytos projekto sąrankos, naudojamos darbo užsakyme, dalys: pirminis projektas (projekto ID), projekto tipas, projekto veikla ir finansiniai aspektai.

- Kai darbo užsakyme sukuriama darbo užsakymo užduotis, automatiškai sukuriamas šios užduoties unikalus projekto ID ir susijusi projekto veikla. Tačiau jeigu keletas darbo užsakymo užduočių darbo užsakyme apima tą patį turtą, joms naudojamas tas pats projekto ID. Kitaip tariant, kiekvienam turtui darbo užsakyme sukuriamas vienas projekto ID.

    - Darbo užsakymo užduoties pirminis projektas (projekto ID) nurodomas pirminio projekto sąrankoje. (Daugiau informacijos apie pirminio projekto sąranką pateikiama kitame skyriuje.) Pavyzdžiui, jeigu klientas arba funkcinė vieta susiejami su konkrečiu pirminiu projektu, pirminis projektas naudojamas kaskart kuriant to kliento arba tos funkcinės vietos darbo užsakymus. Jeigu konkretaus projekto ID nesusiejamas su, pvz., funkcine vieta, naudojamas kitas pirminis projektas darbo užsakymo projekto sąrankoje.
    - Kiekvieno projekto ID atveju būtina nurodyti projekto tipą. Projekto tipas nurodomas projektų grupės sąrankoje. (Daugiau informacijos apie projektų grupės sąranką pateikiama kitame skyriuje.) Jeigu projektų grupės sąrankoje nėra atitikmens, naudojama projektų grupės sąranka, susijusi su pirminiu projektu.
    - Reikiamos projekto veiklos, susijusios su prognozėmis ir žurnalais, sąranka nukopijuojama iš darbo užsakymo projekte nurodyto pirminio projekto. Jeigu projekto, kuris naudojamas kaip pirminis projektas, parinktys **Valanda**, **Išlaidos** ir **Elementas** pažymėtos **Taip**, kalbant apie prognozes ir žurnalus būtina nurodyti projekto veiklą. (Norėdami nustatyti šias parinktis, eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirikite projektą, kuris naudojamas kaip pirminis projektas. Parinktys pateikiamos skyriuje **Reikalinga su žurnalais susijusi veikla**, esančiame „FastTab” **Sąranka**.)

- Finansiniai aspektai nukopijuojami iš turtui priskiriamo įrašo ir susiejami su pirminiu projektu.

Kitame skyriuje aiškinama, kaip nustatyti pirminius projektus ir projektų grupes. Pirminis projektas ir projektų grupės naudojami darbo užsakymams valdyti. Jie taip pat naudojami darbo užsakymų ataskaitoms teikti.

## <a name="set-up-work-order-projects"></a>Darbo užsakymų projektų nustatymas

Prieš pradėdami kurti darbo užsakymus, turite nustatyti darbo užsakymų projektus. Puslapyje **Darbo užsakymo projekto sąranka** (**Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Projekto sąranka**) yra du skirtukai: **Pirminis projektas** ir **Projektų grupė**.

Pasirinkę skirtuką **Pirminis projektas**, galite nustatyti projekto ryšius, kurie gali būti naudojami, jeigu darbo užsakymo užduotyje pasirinktas turtas nesusietas su jokiu projektu. Pirminio projekto sąranka nereikalinga, jeigu jūsų įmonė naudoja turto projektus. Ji reikalinga tik tuo atveju, jeigu užuot naudoję turto projektus norite naudoti darbo užsakymo projektus. Tokiu atveju turite nustatyti bent vieną pirminį projektą.

Pasirinkę skirtuką **Projektų grupė**, galite nustatyti projektų grupes, kurios gali būti susietos su darbo užsakymų tipais, turto tipais ir turtu.

Projektų grupės gali būti naudojamos siekiant sukurti konkrečias kategorijas (grupes), skirtas išlaidoms valdyti. Pavyzdžiui, kurdami projektų grupes konkretiems turto arba darbo užsakymų tipams, galite išsamiai sekti įvairių tipų išlaidų priežiūrą.

Projektų grupės nėra privalomos. Nenustačius projektų grupių, projektų grupei apibrėžti bus naudojamas pirminis projektas, o pagal pirminio projekto projektų grupę bus sukurtas antrinis projektas.

Sąranka užtikrinamas visapusiškas integravimas su moduliu **Projektų valdymas ir apskaita**. Taigi galite sekti išlaidas, susijusias darbo užsakymais atitinkamuose projektuose. Toliau nurodyta procedūra apibūdinama darbo užsakymų projektų sąranka.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Projekto sąranka**.
2. Skirtuke **Pirminis projektas** pasirinkite **Įtraukti**.
3. Laukuose **Darbo užsakymo tipas**, **Funkcinė vieta**, **Turto tipas** ir **Turtas** pasirinkite norimas vertes. Kiekvienai naujai įtrauktai eilutei galite nustatyti tik vieną arba keletą laukų. Nustatytu laukų skaičiumi apibrėžiamas derinys, naudojamas modulyje „Turto valdymas” pasirinkus projekto ID. 

    Pasirinkus funkcinę vietą, automatiškai įtraukiamos susijusios antrinės vietos. Pasirinkę turtą, tam pačiam turtui galite sukurti daugiau darbo užsakymo projekto sąrankos eilučių, tačiau tam turtui galite pasirinkti ir skirtingus projektus.

4. Lauke **Projekto ID** pasirinkite projektą, kuris turėtų būti susietas su sąranka, kurią sukūrėte atlikę 3 veiksmą.
5. Jeigu projekto sąranka turėtų galioti tik tam tikrą laikotarpį, lauke **Pabaigos data** pasirinkite pabaigos datą. Kitu atveju pasirinkite **Nėra**.

    Pagal numatytuosius nustatymus pradžios data yra data, kai į puslapį įtraukiate darbo užsakymo projektą. Ji valdoma pasirinkus lauką **Galiojimo pradžia**, kuris pagal numatytuosius nustatymus yra paslėptas. Kad laukas **Galiojimo pradžia** būtų rodomas, pasirinkite **Rodyti** \> **Visi**. Galite naudoti lauką **Galiojimo pradžia** kartu su lauku **Pabaigos data**, kad nustatytumėte ribotą darbo užsakymo projekto galiojimo laikotarpį.

    ![Darbo užsakymų projekto sąrankos puslapis.](media/17-setup-for-work-orders.png)

6. Skirtuke **Projektų grupė** pasirinkite **Įtraukti**.
7. Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą.
8. Jeigu norite sukonkretinti projektų grupės sąsają, lauke **Turto tipas** pasirinkite turto tipą arba lauke **Turtas** pasirinkite turtą.
9. Lauke **Projektų grupė** pasirinkite projektų grupę, kuri turėtų būti susieta su darbo užsakymo tipu. Pavyzdžiui, darbo užsakymo tipas **Prevencinė priežiūra** gali būti siejamas su projektų grupe **Prev. priež.** arba **Vidaus**. Arba darbo užsakymo tipas **Investicija**, kuris yra naudojamas darbo užsakymams, susijusiems su investicijomis ir ilgalaikiu turtu, gali būti susietas su projektų grupe **Invest.** arba **Investicija**.
10. Pasirinkite **Įrašyti**.

![Darbo užsakymų projekto sąrankos puslapis, Pridėti darbo užsakymą.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Kaskart sukūrus darbo užsakymo eilutę, modulyje „Turto valdymas” ieškoma projektų grupė, kuri turėtų būti susijusi su darbo užsakymo užduoties projektu. Paieška grindžiama šioje temoje aprašyta sąranka. Kiekviena projektų grupė turi susijusį projekto tipą. Projektų grupės, turinčios projekto tipą **Laikas ir medžiaga** arba **Fiksuota kaina**, galioja tik turtui, kuris yra susijęs su kliento paskyra.
>
> Pirminių projektų ir projektų grupių atveju, kai sistema pasirenka galimą darbo užsakymo projektą arba projektų grupę, pasirinkimas grindžiamas įrašais, kuriuos sukūrėte taikydami ankstesnę procedūrą. Siekiant rasti galimą atitikmenį, modulyje „Turto valdymas” peržiūrimi su darbo užsakymo projektu susiję įrašai. Visada pirmiausia tikrinami konkrečiausi deriniai. Kitaip tariant, darbo užsakymo pirminio projekto atveju modulyje „Turto valdymas” pirmiausia ieškoma galimo lauko **Turtas** atitikmens. Jeigu atitikmens nėra, ieškoma lauko **Turto tipas** atitikmens. Jeigu atitikmens nėra, ieškoma lauko **Funkcinė vieta** atitikmens ir t. t. Kaip galite matyti pažvelgę į puslapio **Darbo užsakymo projekto sąranka** išdėstymą, toks elgesys reiškia, kad siekiant nustatyti konkrečiausią derinį, modulyje „Turto valdymas” atitikmenų ieškoma visus įrašus tikrinant iš dešinės į kairę. Jeigu atitikmens nėra, naudojamas numatytasis įrašas, kai pasirinktas tik projekto ID. Panašus procesas vyksta ieškant susijusios projektų grupės. Modulyje „Turto valdymas” pirmiausia ieškoma galimo lauko **Turtas** atitikmens, vėliau lauko **Turto tipas** atitikmens ir tuomet lauko **Darbo užsakymo tipas** atitikmens. Jeigu atitikmens nėra, naudojamas numatytasis įrašas, kai pasirinkta tik projektų grupė.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]