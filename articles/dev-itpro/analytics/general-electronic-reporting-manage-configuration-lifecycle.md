---
title: "Elektroninių ataskaitų konfigūracijos ciklo valdymas"
description: "Šioje temoje aprašoma, kaip valdyti „Microsoft Dynamics 365 for Finance and Operations‟ sprendimo elektroninių ataskaitų (ER) konfigūracijų ciklą."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 35288f5c2edfa8a340f963a5c7216041765a58b4
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Elektroninių ataskaitų konfigūracijų ciklo valdymas

[!include[banner](../includes/banner.md)]


Šioje temoje aprašoma, kaip valdyti „Microsoft Dynamics 365 for Finance and Operations‟ sprendimo elektroninių ataskaitų (ER) konfigūracijų ciklą.

<a name="overview"></a>Apžvalga
--------

Elektroninės ataskaitos (ER) yra mechanizmas, palaikantis įstatymiškai privalomus ir šaliai būdingus elektroninius dokumentus programoje „Microsoft Dynamics 365 for Finance and Operations“. Apskritai, ER suteikia galimybę atlikti tolesnes su vienu elektroniniu dokumentu susijusias užduotis. Daugiau informacijos žr. puslapyje [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md).

-   Sukurti elektroninio dokumento šabloną.
    -   Identifikuoti toliau nurodytus reikiamus duomenų šaltinius, kuriuos galima pateikti dokumente.
        -   Pagrindiniai „Finance and Operations‟ duomenys, pvz., duomenų lentelės, duomenų objektai ir klasės.
        -   Konkretaus proceso ypatybės, pvz., vykdymo data ir laikas bei laiko juosta.
        -   Vartotojo įvesties parametrai, kuriuos vykdymo metu nurodė galutinis vartotojas.
    -   Apibrėžti reikiamus dokumento elementus ir jų topologiją siekiant nurodyti galutinį dokumento formatą.
    -   Konfigūruoti norimą duomenų srautą iš pasirinktų duomenų šaltinių į nustatytus dokumento elementus (naudojant duomenų šaltinių susiejimus su dokumento formato komponentais) ir nurodyti proceso kontrolės logiką.
-   Sukurti šabloną, kurį būtų galima naudoti kituose „Finance and Operations‟ egzemplioriuose.
    -   Programoje „Finance and Operations‟ sukurtą dokumento šabloną transformuoti į ER konfigūraciją ir šią eksportuoti iš dabartinio „Finance and Operations‟ egzemplioriaus kaip XML paketą, kurį būtų galima išsaugoti vietoje arba LCS.
    -   ER konfigūraciją transformuoti į „Finance and Operations‟ dokumento šabloną.
    -   XML paketą, saugomą vietoje arba LCS, importuoti į dabartinį „Finance and Operations‟ egzempliorių.
-   Tinkinti elektroninio dokumento šabloną.
    -   Šabloną iš LCS perduoti į dabartinį „Finance and Operations‟ egzempliorių kaip ER konfigūraciją.
    -   Kurti pasirinktinę ER konfigūracijos versiją ir išsaugoti nuorodą į pagrindinę versiją.
-   Šabloną integruoti su konkrečiu verslo procesu, kad jį būtų galima naudoti programoje „Finance and Operations‟.
    -   Konfigūruoti „Finance and Operations‟ parametrus, kad joje būtų pradėta naudoti ER konfigūracija, į ją nurodant su procesu susijusiu parametru. Pvz., į ER konfigūraciją nurodyti konkrečiu mokėtinų sumų mokėjimo metodu, kad būtų generuojamas elektroninio mokėjimo pranešimas apie SF apdorojimą.
-   Šabloną naudoti konkrečiame verslo procese.
    -   ER konfigūraciją paleisti konkrečiame verslo procese. Pvz., siekiant generuoti SF apdorojimo elektroninio mokėjimo pranešimą, kai pasirenkamas mokėjimo metodas, nurodantis į ER konfigūraciją.

## <a name="concepts"></a>Koncepcijos
Su ER konfigūracijos ciklu susieti tolesni vaidmenys ir susijusios veiklos.

| Vaidmuo                                       | Veikla                                                      | aprašymas                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektroninės ataskaitos funkcijų konsultantas | Kurti ir valdyti ER komponentus (modelius ir formatus).           | Verslininkas, kuriantis konkrečių ER domenų duomenų modelius, kuria reikiamus elektroninių dokumentų šablonus ir atitinkamai juos susieja.                                                                           |
| Elektroninės ataskaitos kūrėjas             | Kurti ir valdyti duomenų modelių susiejimus.                          | „Finance and Operations‟ specialistas, kuris parenka reikiamus „Finance and Operations‟ duomenų šaltinius ir juos susieja su konkrečių ER domenų duomenų modeliais.                                                                 |
| Apskaitos prižiūrėtojas                      | Konfigūruoti su procesu susijusius parametrus, nurodančius į ER artefaktus. | Pavyzdžiui, **Apskaitos prižiūrėtojo** vaidmuo, leidžiantis ER konfigūracijos parametrus naudoti su konkrečiu mokėtinų sumų mokėjimo metodu, kad būtų galima generuoti elektroninio mokėjimo pranešimą apie SF apdorojimą. |
| Mokėtinų sumų mokėjimo klerkas            | ER artefaktus naudoti konkrečiame verslo procese.                | Pvz., **Mokėtinų sumų mokėjimo klerko** vaidmuo, leidžiantis pagal sukonfigūruotą konkretaus mokėjimo metodo ER formatą generuoti elektroninio mokėjimo pranešimus apie SF apdorojimą.           |

## <a name="er-configuration-development-lifecycle"></a>ER konfigūracijos plėtros ciklas
Dėl tolesnių su ER susijusių priežasčių rekomenduojame ER konfigūracijas kurti programavimo aplinkoje kaip atskirame „Finance and Operations“ egzemplioriuje.

-   Vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**, gali konfigūracijas redaguoti ir vykdyti bandymams. Tokiu atveju gali būti iškviesti klasių ir lentelių, kurios gali būti potencialiai kenksmingos verslo duomenims ir „Finance and Operations‟ egzemplioriaus naudojimo efektyvumui, metodai.
-   „Finance and Operations‟ įvesties vietos neapriboja klasių ir lentelių kaip ER konfigūracijų ER duomenų šaltinių metodų iškvietimų ir jie yra užregistruoti įmonės turinyje. Todėl slaptus verslo duomenis gali pasiekti vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**.

Programavimo aplinkoje sukurtas ER konfigūracijas galima nusiųsti į tikrinimo aplinką konfigūracijai (tinkamam proceso integravimui, rezultatų tikslumui ir našumui) įvertinti ir kokybei (vaidmenų valdomų prieigos teisių teisingumui ir pareigų atskyrimui) užtikrinti. Šiuo tikslu galima naudoti funkcijas, leidžiančias mainytis ER konfigūracijomis. Galiausiai patvirtintas ER konfigūracijas galima įkelti į LCS, kur jas būtų galima bendrinti su paslaugų prenumeratoriais arba į gamybos aplinką ir naudoti viduje, kaip parodyta tolesniame paveikslėlyje. ![ER konfigūracijos ciklas](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)




