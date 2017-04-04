---
title: "Elektroninių ataskaitų konfigūracijos ciklo valdymas"
description: "Šioje temoje aprašoma, kaip valdyti elektroninio ataskaitų (ER) konfigūracijos Microsoft Dynamics 365 operacijų tirpalo gyvavimo ciklo."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Elektroninių ataskaitų konfigūracijos ciklo valdymas

Šioje temoje aprašoma, kaip valdyti elektroninio ataskaitų (ER) konfigūracijos Microsoft Dynamics 365 operacijų tirpalo gyvavimo ciklo.

<a name="overview"></a>Apžvalga
--------

Elektroninės ataskaitos (ER) yra mechanizmas, palaikantis įstatymiškai privalomus ir šaliai būdingus elektroninius dokumentus programoje „Microsoft Dynamics 365 for Operations“. Apskritai, ER suteikia galimybę atlikti tolesnes su vienu elektroniniu dokumentu susijusias užduotis. Daugiau informacijos rasite [elektroninių ataskaitų apžvalga](general-electronic-reporting.md).

-   Sukurti elektroninio dokumento šabloną.
    -   Identifikuoti toliau nurodytus reikiamus duomenų šaltinius, kuriuos galima pateikti dokumente.
        -   Pagrindinių dinamika 365 operacijų duomenims, pvz., duomenų lenteles ir duomenų objektų klases.
        -   Specifinės proceso ypatybes, pvz., vykdymo data ir laikas ir laiko juostos.
        -   Vartotojo įvesties parametrai, nurodyti galutinio vartotojo vykdymo metu.
    -   Apibrėžti reikiamus dokumento elementus ir jų topologiją siekiant nurodyti galutinį dokumento formatą.
    -   Konfigūruoti norimą duomenų srautą iš pasirinktų duomenų šaltinių į nustatytus dokumento elementus (naudojant duomenų šaltinių susiejimus su dokumento formato komponentais) ir nurodyti proceso kontrolės logiką.
-   Sukurti šabloną, kurį būtų galima naudoti kituose „Dynamics 365 for Operations‟ egzemplioriuose.
    -   Programoje „Dynamics 365 for Operations‟ sukurtą dokumento šabloną transformuoti į ER konfigūraciją ir šią eksportuoti iš dabartinio „Dynamics 365 for Operations‟ egzemplioriaus kaip XML paketą, kurį būtų galima išsaugoti vietoje arba LCS.
    -   ER konfigūraciją transformuoti į „Dynamics 365 for Operations‟ dokumento šabloną.
    -   XML paketą, saugomą vietoje arba LCS, importuoti į dabartinį „Dynamics 365 for Operations‟ egzempliorių.
-   Tinkinti elektroninio dokumento šabloną.
    -   Šabloną iš LCS perduoti į dabartinį „Dynamics 365 for Operations‟ egzempliorių kaip ER konfigūraciją.
    -   Kurti pasirinktinę ER konfigūracijos versiją ir išsaugoti nuorodą į pagrindinę versiją.
-   Šabloną integruoti su konkrečiu verslo procesu, kad jį būtų galima naudoti programoje „Dynamics 365 for Operations‟.
    -   Konfigūruoti „Dynamics 365 for Operations‟ parametrus, kad joje būtų pradėta naudoti ER konfigūracija, į ją nurodant su procesu susijusiu parametru. Pvz., nurodyti konkrečių sąskaitų mokamos mokėjimo būdą kurti elektroninio mokėjimo pranešimą tvarkyti sąskaitas-faktūras ER konfigūraciją.
-   Šabloną naudoti konkrečiame verslo procese.
    -   Paleisti ER konfigūracijos tam tikram verslo procesui. Pvz., sukurti elektroninio mokėjimo pranešimą perdirbimo kai mokėjimo būdą, kuris nurodo ER konfigūraciją SF yra pažymėtas.

## <a name="concepts"></a>Koncepcijos
Šie vaidmenys ir susijusi veikla yra susiję su ER konfigūracijos gyvavimo ciklą.

| Vaidmuo                                       | Veikla                                                      | aprašymas                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektroninės ataskaitos funkcijų konsultantas | Kurti ir valdyti ER komponentus (modelius ir formatus).           | Verslo asmuo, kuris projektuoja ER domeno konkrečių duomenų modelių, dizainų reikalaujama elektroninius dokumentus, šablonus ir suriša juos atitinkamai.                                                                           |
| Elektroninės ataskaitos kūrėjas             | Kurti ir valdyti duomenų modelių susiejimus.                          | Dynamics 365 operacijų specialistas, kuris parenka reikiamą Dynamics 365 operacijų duomenų šaltinių ir suriša juos ER domeno konkrečių duomenų modeliai.                                                                 |
| Apskaitos prižiūrėtojas                      | Konfigūruoti su procesu susijusius parametrus, nurodančius į ER artefaktus. | Pvz., su **apskaitos vadovo** vaidmenį, kuris leistų ER konfigūracijos parametrus naudoti ypač sąskaitų mokamos mokėjimo būdą kurti elektroninio mokėjimo pranešimą tvarkyti sąskaitas-faktūras. |
| Mokėtinų sumų mokėjimo klerkas            | ER artefaktus naudoti konkrečiame verslo procese.                | Pvz., su **sąskaitų mokėtinos išmokos sekretorius** vaidmenį, kuris leistų elektroninio mokėjimo pranešimus, tvarkyti sąskaitas, sugeneruotas pagal ER formatą, kuris yra sukonfigūruotas naudoti konkretų mokėjimo būdą.           |

## <a name="er-configuration-development-lifecycle"></a>ER konfigūracijos plėtros ciklas
Dėl tolesnių su ER susijusių priežasčių rekomenduojame ER konfigūracijas kurti programavimo aplinkoje kaip atskirame „Dynamics 365 for Operations“ egzemplioriuje.

-   Vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**, gali konfigūracijas redaguoti ir vykdyti bandymams. Tokiu atveju gali būti iškviesti klasių ir lentelių, kurios gali būti potencialiai kenksmingos verslo duomenims ir „Dynamics 365 for Operations‟ egzemplioriaus naudojimo efektyvumui, metodai.
-   „Dynamics 365 for Operations‟ įvesties vietos neapriboja klasių ir lentelių kaip ER konfigūracijų ER duomenų šaltinių metodų iškvietimų ir jie yra užregistruoti įmonės turinyje. Todėl slaptus verslo duomenis gali pasiekti vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**.

ER konfigūracijas, skirtas kūrimo aplinka gali būti įkeltas prie tyrimų aplinkos konfigūracijos vertinimo (tinkamo proceso integracijos, rezultatus ir efektyvumą, teisingumą) ir kokybės užtikrinimą, pvz., teisingumas vaidmuo skatina bendravimo teisių ir pareigų atskyrimas. Funkcijos, kurios leidžia ER konfigūracijos mainai gali būti naudojamas šiam tikslui. Galiausiai pasirodė ER konfigūracijų galima įkelti LKD, kur jie gali būti dalijamasi su paslaugos abonentai, arba gamybos aplinkoje vidiniam naudojimui, kaip parodyta šioje iliustracijoje. ![ER konfigūracijos gyvavimo ciklo](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)


