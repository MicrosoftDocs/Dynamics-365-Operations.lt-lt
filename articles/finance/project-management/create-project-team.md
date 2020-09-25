---
title: Projekto komandos kūrimas
description: Šioje temoje pateikiama informacija apie tai, kaip kurti ir valdyti projekto komandas.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760614"
---
# <a name="create-a-project-team"></a>Projekto komandos kūrimas

[!include [banner](../includes/banner.md)]

Norėdamas naudoti vaidmenis, kurie buvo anksčiau nustatyti projekte, projekto vadovas tuos vaidmenis turi susieti su projektu. Projektui galima priskirti kelis vaidmenis. Kad būtų išvengta painiavos, rezervavimo metu šie vaidmenys automatiškai pažymimi. Pavyzdžiui, jei projekto vadovui reikia trijų programinės įrangos inžinierių, automatiškai sugeneruojami trys programinės įrangos inžinieriaus vaidmenys, kurių žymos – **1 programinės įrangos inžinierius**, **2 programinės įrangos inžinierius** ir **3 programinės įrangos inžinierius**. Jei anksčiau buvo nustatytos vaidmenų charakteristikos, ieškant ištekliaus jos taikomos kaip filtras. Pagal poreikį galima pridėti papildomų charakteristikų ir taip dar patikslinti iešką.

Taip pat galima tinkinti rodinio parametrus, kad būtų galima geriau matyti išteklių prieinamumą. Parinktimis galima nustatyti valandos, dienos, savaitės, mėnesio, ketvirčio ir metų prieinamumo rodymą. Taip pat galima parinktis rodyti turimą ir likusį išteklių pajėgumą. Ši parinktis naudinga valdant laiką, kai vertinamas turimas veikloms skirtas laikas ar išteklių prieinamumas.

Projekto vadovas puslapyje gali pasirinkti vaidmenį ir, jei turimas reikalavimą atitinkantis išteklius, pasirinkti rezervuoti išteklių vaidmeniui užimti. Atkreipkite dėmesį, kad šiame planavimo etape išteklių rezervuoti nereikia. Kai kuriate WBS, vaidmenis galite pakeisti darbuotojams priskirtais projekto ištekliais. Jei WBS vaidmenys pakeičiami darbuotojams priskirtais ištekliais, nustatant išteklius automatiškai atnaujinamas projekto komandos sąrašas ir planavimas.

[![Projekto komandos sąrašas tiek su vaidmenimis, tiek su faktiniais ištekliais](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projekto vadovas turi įvairių projekto ištekliaus rezervavimo parinkčių, pvz., **Likęs pajėgumas**, **Visas pajėgumas**, **Pajėgumo procentas** ir **Nurodyti valandas**. Pakitus išteklių priskyrimams, šias rezervavimo parinktis galima bet kuriuo metu atšaukti. Palaikomi du tolesni rezervavimo tipai.

- **Tikslus rezervavimas** – išteklių rezervavimas buvo patvirtintas įtraukimo darbui nurodytą trukmę.
- **Apytikslis rezervavimas** – išteklių rezervavimas buvo preliminariai nustatytas įtraukimo darbui nurodytą trukmę.

Tolesne procedūra paaiškinama, kaip sukurti projekto komandą.

## <a name="create-a-project-team"></a>Projekto komandos kūrimas

1. Sąrašo puslapyje **Visi projektai** pasirinkite projektą ir pasirinkite **Redaguoti**.
2. Skirtuke **Projekto komanda ir planavimas**, lauke **Grafiko pabaigos data** įveskite grafiko pradžios datą ir pridėkite vieną mėnesį. Pavyzdžiui, jei grafiko pradžios data yra 2017 m. birželio 24 d. (2017-06-24), įveskite **2017-07-24**.
3. Pasirinkite **Įtraukti**.
4. Srityje **Į projektą įtraukti vaidmenų**, lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
5. Pasirinkite **Būtinosios kompetencijos**.
6. Puslapyje **Pasirinkti charakteristikas** pagal numatytuosius parametrus pasirenkamos anksčiau jūsų nustatytos vyresniojo projektų vadovo vaidmens charakteristikos. Pasirinkite **Gerai**.
7. Puslapyje **Į projektą įtraukti vaidmenų**, lauke **Išteklių skaičius** įveskite **1**.
8. Lauke **Išteklius** peržvalga rodo visus išteklius, turinčius reikiamas kompetencijas. Pasirinkite **Danielis Goldschmidtas**, tada – **Kurti**.
9. Puslapyje **Projektas** pasirinkite **Įtraukti**.
10. Srityje **Į projektą įtraukti vaidmenų**, lauke **Vaidmuo** pasirinkite **Komandos narys**. Lauke **Išteklių skaičius** įveskite **5**.
11. Pasirinkite **Kurti**.
12. Puslapyje **Projektai** pasirinkite **Panaudoti išteklių**.

## <a name="monitor-project-teams"></a>Projekto komandų stebėjimas
1. Puslapyje **Visi projektai** pasirinkite projekto **XYZ atnaujinimas, 2 etapas** saitą **Projekto ID**.
2. „FastTab‟ **Projekto komanda ir planavimas** patikrinkite, ar išvardyti projekto ištekliai yra teisingi.
