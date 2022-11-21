---
title: Apriboti prieigą prie darbuotojų pagal juridinį subjektą
description: Šiame straipsnyje paaiškinama, kaip nustatyti darbuotojo prieigą pagal juridinį subjektą.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780302"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Apriboti prieigą prie darbuotojų pagal juridinį subjektą

Šiame straipsnyje paaiškinama, kaip nustatyti darbuotojo prieigą pagal juridinį subjektą.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darbuotojai įdarbinti juridiniuose subjektuose. Štai keletas pavyzdžių:

- "Šių" con įdarbinta USSI juridiniame subjekte.
- Jav dolerių juosta taikoma JAVmf juridiniame subjekte.
- Alicia Tdfber įdarbintas GLSI ir USMF juridiniuose subjektuose.

Atsižvelgiant į vartotojo vaidmenį įmonėje, jiems gali reikėti prieigos, kad būtų galima peržiūrėti visus darbuotojus visuose juridiniuose subjektuose. Taip pat gali tekti apriboti vartotoją, kad jis galėtų peržiūrėti tik juridinio subjekto, prie kurio jis turi prieigą, darbuotojus. Norėdami kontroliuoti, kuriuos darbuotojus vartotojas gali peržiūrėti, personalo **bendrinamų parametrų puslapyje** **pasirinkite Apriboti prieigą prie darbuotojo informacijos parametrų**.

Pavyzdžiui, vartotojas turi prieigą prie darbuotojo puslapio **ir** turi prieigą tik prie USMF juridinio subjekto. Šiuo atveju, šiame sąraše vartotojas gali peržiūrėti šią darbuotojų informaciją:

- Jei neįgalinta prieigos prie darbuotojo informacijos apribojimo funkcija, vartotojas gali peržiūrėti Rodinys, Semas ir Alicia informaciją.
- Jei funkcija įgalinta, vartotojas gali peržiūrėti tik Alicia ir Semaso informaciją, nes ji taip pat taikoma USMF juridiniame subjekte.

Rodoma informacija skiriasi, atsižvelgiant į jūsų nenaudojamą programą.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources Atskiras

Jei įgalinta prieigos prie darbuotojo informacijos apribojimo funkcija, kai kuriuose sąrašuose, kuriuose yra darbuotojo vardas, apribotas vartotojas matys tuščią reikšmę.

Pavyzdžiui, vartotojas, turintis prieigą tik prie JAVMF juridinio subjekto, gali elgsis taip:

- Aktyvių **pareigų** sąraše **Darbuotojo** stulpelis bus tuščias e. Jav valstijose, kadangi vartotojas neturi prieigos prie USSI juridinio subjekto darbuotojų.
- Jei vartotojas detalizuoti darbuotojo vardą, pasirodys tuščias **darbuotojo** puslapis.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources dėl finansinės infrastruktūros

Jei įgalinta prieigos prie darbuotojo informacijos apribojimo funkcija, apribotas vartotojas kai kuriuose sąrašuose matys darbuotojo vardą.

Pavyzdžiui, vartotojas, turintis prieigą tik prie JAVMF juridinio subjekto, gali elgsis taip:

- Aktyvių **pareigų** sąraše darbuotojo **stulpelyje** bus rodomas Valdiklio vardas. Jei vartotojas pereis prie darbuotojo vardo, bus rodomas tik vardas ir pareigos.
- Jei vartotojas detalizuoti darbuotojo vardą, pasirodys tuščias **darbuotojo** puslapis.

> [!TIP]
> Jei naudojate "Dynamics 365" personalo infrastruktūrą ir norite, kad vartotojai galėtų matyti tuščias darbuotojų vardų reikšmes, **·** **galite** įtraukti prieigos prie darbuotojų saugos teisių apribojimas prie vartotojų vaidmenų saugos konfigūracijos puslapyje.

Įjungę funkciją turite atlikti kai kuriuos papildomus veiksmus, kad teisių nustatymas kiekvienam vartotojui, kurio rodinys turi būti apribotas.

1. Puslapyje **Vartotojai** pasirinkite vartotoją.
2. Pasirinkite vartotojo vaidmenį. Pasirinktis **Priskirti organizacijas** tampa galima.
3. Pasirinkite **Priskirti organizacijas**.
4. Naujame puslapyje pasirinkite **Suteikti prieigą prie konkrečių organizacijų atskirai**, o tada pasirinkite organizacijas, prie kurių vartotojas turi turėti prieigą.
5. Pakartokite 2-4 veiksmus kiekvienam kitam vartotojo turimam vaidmeniui, įskaitant sistemos vartotojo vaidmenį.

> [!NOTE]
> Juridiniai subjektai, prie kurių vartotojas turi prieigą, turi atitikti visus vartotojo vaidmenis.
