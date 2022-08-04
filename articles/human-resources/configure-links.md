---
title: Kurti saitus iš Personalo į kitą aplinką
description: Šiame straipsnyje paaiškinama, kaip sukurti "Microsoft Dynamics 365 Human Resources " saitą su kita "Dynamics 365" aplinka.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9640f460ed7b0b1a0cfdffb7c318bf833f8627fc
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065300"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Kurti saitus iš Personalo į kitą finansų aplinką

Klientas gali turėti dvi "Dynamics 365" aplinkas, kurioje jie dirba. Pavyzdžiui, klientas gali turėti aplinką Dynamics 365 Human Resources finansų infrastruktūrai ir nori prisijungti prie kitos "Dynamics 365" finansų aplinkos. 

Ši funkcija leis saitus iš personalo puslapio į konkretų kitos finansų aplinkos puslapį. Kai saitai sukonfigūruoti, galite nurodyti, kur saitas bus pasiekiamas personalo portale, ir paskirties puslapį, kuris bus atidarytas kitoje aplinkoje.

> [!Note] 
> Norėdami gauti šią funkciją **, turite įjungti personalo vartotojų** patirties **patobulinimus** funkcijų valdymo srityje.

## <a name="configure-target-systems"></a>Konfigūruoti paskirties sistemas

Personalo sistemos administratoriai gali apibrėžti saitus, kurie bus išviri personalo **puslapiuose**. Konfigūracijos dalys – tai finansinės aplinkos, kurias norėtumėte pasiekti kaip saito tikslinę nuorodą. 

Norėdami konfigūruoti tikslinę sistemą:
1. Puslapyje Konfigūruoti **saitus** pasirinkite Konfigūruoti **paskirties sistemą**.  
2. Įveskite paskirties sistemos pavadinimą ir pateikite finansinės aplinkos URL. Sukonfigūrę savo tikslines sistemas, galite nurodyti saitus.

## <a name="configure-links"></a>Konfigūruoti saitus

Kiekvienas jūsų sukurtas saitas turės šią informaciją:
 - **Saitas**: saito pavadinimas. Naudojama tik identifikuoti.
 - **Įgalinkite šį** saitą: nustatykite **kaip** Taip, jei norite, kad būtų rodomas saitas su personalo vartotojais.
 - **Rodomas pavadinimas**: įveskite pavadinimą, kuris bus rodomas kaip antrinės aplinkos saitas. 
 - **Formos išorinis saitas**: pasirinkite, kuriame puslapyje norite matyti saitą. Saitus galima iškuoti tik darbuotojų savitarnos **darbo** srityje **ir** darbo, **pareigų**, **darbuotojo ir** **supaprastinamų darbuotojų** puslapiuose.
 - **Grupė**: galite tvarkyti saitus naudodami grupes. Pasirinkite esamą grupę arba sukurkite naują, naudodami stulpelį **Grupė**.
 - **Paskirties sistema**: pasirinkite paskirties sistemą, kuri buvo sukurta naudojant parinktį **Konfigūruoti paskirties** sistemą. Tai bus antrinė aplinka, kuri bus naudojama naršant saitą.
 - **Naudokite dabartinę vartotojo įmonę**: pasirinkite **Taip**, jei norite naudoti dabartinę vartotojo įmonę, kai naršote finansų srityje. Jei **norite** pasirinkti įmonę, kurią norite naudoti, pasirinkite Ne.
 - **Paskirties** meniu elementas: įveskite meniu elementą iš finansinės aplinkos, kurį saitas turėtų naudoti naršydami. Yra meniu elementų, į kuriuos galite pereiti tiesiogiai. 

   Norėdami rasti reikiamą meniu elementą:
   1. Eiti į finansų aplinką ir atidaryti puslapį, kuris yra naršymo tikslas. 
   2. Nukopijuokite meniu elementą iš URL. Pavyzdžiui, jei norite, kad saitas įves jus į finansų ir operacijų darbuotojų sąrašą, įveskite vertę, kuri URL lauke rodoma po "&mi". 
   3. Meniu elemento, perkeliančio į darbuotojų sąrašo puslapį, pavyzdys: HcmWorkerListPage_Employees.

 - **Duomenų šaltinio saitas**: pasirinkite duomenų šaltinį, kurį nurodo saitas. Galimi dažniausiai naudojami šaltiniai, pvz., **Darbininkas** ir **Pareigos**.

### <a name="access-to-links"></a>Prieiga prie saitų

Sistemos administratoriai nustatytuose puslapiuose matys naujai sukurtus saitus, net jei pasirinkta parinkties **Įjungti šį saitą** reikšmė yra **Ne**. Tai galima naudoti norint patikrinti saitus prieš pateikiant juos naudoti kitiems darbuotojams. Visi kiti vaidmenys matys tik sukonfigūruotus saitus, kai nustatyta **parinktis** Įgalinti šį saitą kaip **Taip**. Saitus galės pasiekti darbuotojai, turintys prieigą prie puslapių, kuriuose šie saitai yra pridėti.

Vartotojai taip pat turi turėti saugos teises antrinėje aplinkoje, kuri nustatyta prieiga prie tos aplinkos puslapių. Jei jie jų neturi, naudojant saitą bus rodomas saugos dialogo langas.


