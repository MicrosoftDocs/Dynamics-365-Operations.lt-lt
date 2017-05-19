---
title: "Įdarbinimo „Power BI“ turinys"
description: "Šioje temoje aprašytas „Dynamics 365 for Operations“ įdarbinimo „Power BI“ turinys. Paaiškinama, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 15780e7db5867a2f6a484ceb663e617345c033c2
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="recruiting-power-bi-content"></a>Įdarbinimo „Power BI“ turinys

[!include[banner](../includes/banner.md)]


Šioje temoje aprašytas „Dynamics 365 for Operations“ įdarbinimo „Power BI“ turinys. Paaiškinama, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

<a name="accessing-the-content-pack"></a>Prieiga prie turinio paketo
--------------------------

Įdarbinimo turinio paketą galite rasti bendrai naudojamo turto bibliotekoje „Microsoft Dynamics Lifecycle Services“ (LCS). Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie „Microsoft Dynamics 365 for Operations“ duomenų, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Į turinio paketą įtrauktos ataskaitos
Prijungus turinio paketą prie „Dynamics 365 for Operations“ duomenų, ataskaitose rodomi jūsų organizacijos duomenys. Jei niekada nenaudojote „Microsoft Power BI“, daugiau apie tai galite sužinoti temoje [„Power BI“ mokymosi vedlio puslapis](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Į turinio paketą įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                       | Turinys                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Pretendento analizė           | Pretendentai pagal darbą, pretendento šaltiniai, pretendentai pagal vietą ir bendras pretendentų skaičius           |
| Pretendento būsena             | Pretendentai pagal tipą ir būseną ir pretendento būsena                                                    |
| Pretendento demografiniai duomenys       | Pretendentai pagal amžių ir lytį ir pretendentai pagal išsilavinimo lygį ir būseną                             |
| Įdarbinimo analizė          | Grynasis įdarbinimo santykis, vidutinės dienos įdarbinti, blogų įdarbinimų procentas ir įdarbinimo išlaidos                    |
| Įdarbinimo projekto analizė | Įdarbinimo projektų skaičius, laisvos vietos pagal įdarbinimo projektą ir pretendentai pagal įdarbinimo projektą |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
„Dynamics 365 for Operations“ duomenys naudojami ataskaitoms įdarbinimo turinio pakete užpildyti. Toliau pateiktoje lentelėje nurodomi objektai, kuriais turinio paketas pagrįstas.

| Objektas                          | Turinys                                                         | Ryšiai su kitais objektais                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Įdarbinimas\_Pretendentas           | Pretendentai, pasamdyti pretendentai, grynosios samdos koeficientas ir išlaidos          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Pretendento vardas, pavardė ir vardas bei pavardė                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Kalendoriaus poslinkiai ataskaitoms skaidyti                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Įmonės, pagal kurias filtruojamos ataskaitos                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Dienos, savaitės, mėnesiai ir metai                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Pretendentas, veiklos efektyvumas, pradžios data ir pretendento tipas           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Pradžios data, pabaigos data ir perėjimo data                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | Miestas, seniūnija, pašto kodas ir šalis arba regionas                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Funkcija, tipas ir pareigos                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Pretendentų šaltinis                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Įvertinimas, aprašas ir įvertinimo modelis                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Projekto aprašas, projekto būsena ir laisvos vietos                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Atleisti pretendentai, priežastis, veiklos efektyvumas ir atleidimo data | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Šie objektai buvo naudojami skaičiuojamiems matams kurti. Tada šie skaičiuojami matai naudojami skaičiuojant pagrindinius efektyvumo indikatorius (KPI) ir ataskaitas, naudojamas turinio pakete. Jei norite į ataskaitas ir ataskaitų sritį įtraukti papildomų skaičiavimų, galite iš LCS atsisiųsti ir modifikuoti failą Recruiting.pbix. Šis failas yra numatytasis duomenų modelis, kuris buvo naudojamas turinio paketui kurti. Atlikę keitimus, galite kurti organizacinį turinio paketą ir ataskaitų sritį, kuriuose yra jūsų įtraukta informacija.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





