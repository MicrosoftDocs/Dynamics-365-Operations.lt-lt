---
title: Kursų apžvalga
description: Šiame straipsnyje paaiškinama, kaip personalo administratoriai ir vadybininkai gali naudoti kursų funkcijas, kad galėtų prižiūrėti informaciją apie kursus, kuriuos gali naudoti darbuotojai.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716286"
---
# <a name="courses-overview"></a>Kursų apžvalga

Microsoft Dynamics 365 Human Resources suteikia jūsų organizacijos mokymosi poreikių sprendimą. Šis sprendimas siūlo du mokymosi kursų kelius: virtualų *ir* *dėstytotojas*.

*Virtualus mokymasis* yra mokymosi patirtis, patobulinta naudojant interneto išteklius. Instruktoriaus *mokymo* metu dėstytojas palengvina darbuotojų grupės ar pasiūlymų mokymo sesiją.

Mūsų mokymosi modulyje personalo specialistai, administratoriai, mokymo vadybininkai ir vadybininkai gali sukurti ir priskirti darbuotojams abu mokymosi kursų kelius.

> [!NOTE]
> Norėdami naudoti virtualius kursus, turite įgalinti **funkcijų valdymo** kursų patobulinimų priemonę.

## <a name="set-up-virtual-courses"></a>Virtualių kursų nustatykite

Norėdami konfigūruoti virtualius kursus, turite įgalinti **funkcijų valdymo** kursų patobulinimų funkciją. Eikite į **Naujas \> kursas** ir nustatykite virtualią **pasirinktį** **Taip**. Įgalinus funkciją, reikalingas kursų saitas. Kurso **būsenos laukas** bus nustatytas į **Atidaryta**. Parinktis **Leisti darbuotojui prisiregistruoti** automatiškai bus nustatyta kaip **Taip**, bet gali būti nustatyta kaip **Ne**.

Įgalinus **funkcijų valdymo** kursų patobulinimų funkciją, įvyksta šie pakeitimai:

- Turi būti nustatytas kurso priskyrimo terminas.
- Būtina susieti kursus.
- **Darbuotojų savitarnos** paslauga rodo darbuotojo peržiūrą **kursuose**. Vartotojas gali peržiūrėti kursus, kurie yra vėluos, greit sumokėti ir priskirti.
- Darbuotojai gali užbaigti virtualius kursus ir save patvirtinti.

## <a name="set-up-instructor-led-courses"></a>Nustatyti dėstytojas-kursus

Prieš pradedant naudoti dėstytojas neturi būti konfigūruojamas.

Ši informacija yra pasirinktinė ir gali būti nurodyta kursams. Jei ši informacija bus įvesta į kursus, ji turėtų būti nustatyta prieš sukuriant kurso įrašus:

- Kurso tipas
- Auditorijų grupės
- Kursų grupės
- Kursų vietos
- Auditorijos
- Dėstytojai
- Kursų tipai

Kursų tipus galite *naudoti kursams* skirstyti į kategorijas pagal jų struktūrą ar turinį. Galite kurti kursų tipus kursų **tipų** puslapyje.

Minimalus ir maksimalus dalyvių, kuriuos galite registruoti į kursus, skaičius nurodytas **** kursų puslapio **** Bendra FastTab.

### <a name="course-setup-type"></a>Kursų nustatymo tipas 

*Kursų* struktūrą apibrėžia nustatymo tipai. Yra trys kursų nustatymo tipai.

| Sąrankos tipas | Aprašymas |
|------|--------|
| Standartinis | Šio nustatymo tipo kursai neturi kasdienės darbotvarkės. Tai numatytasis nustatymo tipas, kai kuriate naujus kursus. |
| Darbotvarkė | Pasirinkti šį nustatymo tipą, norint planuoti kiekvienos per kelias dienas vykstainos kurso dienos informaciją. |
| Darbotvarkė + sesija | <p>Pasirinkti šį sudėtingesnių kursų nustatymo tipą. Pavyzdžiui, galite padalinti kurso darbotvarkę į *sesijas* *·*:</p><ul><li>*Specialieji* specialieji kursų subjekto sritys.</li><li>*Sesijos padalija specialką ir padeda identifikuoti konkrečius procesus ar technikas*, kurios susijusios su specialkomis.</li></ul> |

### <a name="course-tasks"></a>Kurso užduotys

Užbaikite šias kiekvieno kurso užduotis:

- Registruoti dalyvius.
- Nurodyti paskutinę registracijos datą.
- Nustatyti mažiausią ir didžiausią dalyvių skaičių.
- Priskirti kurso vietą ir auditoriją.
- Kurso dalyviams rekomenduoti viešbučius.
- Sukurkite kursų aprašymą, kurį galima registruoti darbuotojų savitarnoje ****.

> [!NOTE]
> Kursą panaikinti galite tik jei niekas į jį neužsiregistravo.

### <a name="course-statuses"></a>Kurso būsenos

Šioje lentelėje išvardijamos kursų būsenos ir veiksmai, kurie yra atlikti kiekvienam.

| Būsena | Veiksmai |
|------|--------|
| Sukurta | <ul><li>Įvesti ir modifikuoti kurso informaciją.</li><li>Pakeisti kursų būseną į **Atidaryta**, kad darbuotojai galėtų registruotis į kursus.</li></ul> | 
| Atidaryti | <ul><li>Registruoti dalyvius į kursą.</li><li>Šalinti dalyvius iš kurso.</li><li>Patvirtinti kurso dalyvius.</li><li>Keisti dalyvių, kurių būsena **yra** Patvirtinta **, kursų** būseną į Uždaryta arba **Atšaukta**.</li></ul>|
| Uždarytas | Galite iš naujo atidaryti kursą. |
| Anuliuota | Galite iš naujo atidaryti kursą. |

### <a name="course-participants"></a>Kurso dalyviai

*Kurso dalyviai* yra darbuotojai, dalyvaujantiems mokymo kursuose arba įvykyje. Dalyvius galite registruoti tik į atvirus kursus.

### <a name="workflow"></a>Darbo eiga

Darbuotojai, kurie registruojasi į kursus darbuotojų **savitarnos** puslapyje, gali turėti savo registraciją nukreipti į darbo eigą patvirtinti. Galite priskirti darbo eigą kursams puslapio **Kursų bendrajame** FastTab **** .
