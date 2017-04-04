---
title: "Įdarbinti Power BI turinys"
description: "Šioje temoje aprašoma Dynamics 365 operacijų - įdarbinti Power BI turinį. Jis paaiškina, kaip pasiekti ataskaitas, kurios įtraukiamos į turinio paketą, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinio paketas."
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Įdarbinti Power BI turinys

Šioje temoje aprašoma Dynamics 365 operacijų - įdarbinti Power BI turinį. Jis paaiškina, kaip pasiekti ataskaitas, kurios įtraukiamos į turinio paketą, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinio paketas.

<a name="accessing-the-content-pack"></a>Prieiga prie turinio paketas
--------------------------

Įdarbinimas turinio paketą galite rasti bendro naudojimo turto bibliotekoje Microsoft Dynamics gyvavimo ciklo paslaugų (LKD). Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie savo "Microsoft Dynamics 365" operacijų duomenų, rasite [LCS iš "Microsoft" ir savo partnerių kiekis Power BI](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Pranešimų, kurie yra įtraukti į turinio paketas
Prijungę turinio pack Dynamics "365" operacijų duomenų ataskaitose nurodoma organizacijos duomenis. Jei niekada nenaudojote "Microsoft" Power BI prieš, galite sužinoti daugiau apie tai ant to [vadovaujasi mokymosi puslapis, Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Pranešimų, kurie yra įtraukti į turinio paketas yra diagramos ir lentelės, kuriose papildomos informacijos. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                       | Turinys                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Pareiškėjas analizė           | Pareiškėjai iš darbo, ieškovė šaltinių, pareiškėjai pagal vietą, ir bendrą pareiškėjų skaičių           |
| Pretendento būsena             | Pareiškėjams pagal tipą ir būklę ir Pretendento būsena                                                    |
| Pareiškėjas demografija       | Pareiškėjams pagal amžių ir lytį, o ieškovės pagal išsilavinimo lygį ir būseną                             |
| Įdarbinti analizė          | Grynasis nuomos santykis, vidutinė dienos samdyti, blogai samdo ir įdarbinimo išlaidos                    |
| Įdarbinimo projekto analizė | Įdarbinimo projektai, angos iš įdarbinimo projekto ir pretendentų iš įdarbinimo projekto skaičius |

Galite filtruoti diagramas bei plyteles ant šios ataskaitos ir grafikai ir plytelės prie prietaisù skydelio. Daugiau informacijos apie filtro ir PIN kodą, Power BI, rasite [kurti ir konfigūruoti ataskaitų srities A](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Dinamika 365 operacijų duomenys yra naudojamas užpildyti ataskaitos įdarbinimas turinio paketas. Šioje lentelėje subjektų buvo pagrįsta turinio paketas.

| Objektas                          | Turinys                                                         | Santykių su kitais subjektais                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Įdarbinimo\_pareiškėjui           | Pareiškėjai, išnuomotą pareiškėjams, grynasis nuomos santykis ir išlaidos          | Įdarbinimo\_ApplicantName įdarbinti\_įmonės įdarbinti\_CalendarOffset Recuriting\_dienos įdarbinti\_GeographicLocation įdarbinti\_gyventojai, įdarbinti\_darbo, įdarbinimo\_Media įdarbinti\_RecruitmentProject                                |
| Įdarbinimo\_ApplicantName       | Pareiškėjo vardas, pavardė ir vardas, pavardė                   | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_CalendarOffset      | Kalendorinių kompensuoja gabaliuką ataskaitas                                | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_įmonė             | Bendrovės filtruoti ataskaitas                                   | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_dienos                | Dienas, savaites, mėnesius ir metus                                   | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_demografija        | Data gimimo, lyties, etninės kilmės ir šeimyninė padėtis         | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_EmployedApplicant   | Pareiškėjas, efektyvumo, pradžios datą ir pareiškėjo tipas           | Įdarbinti\_įmonės įdarbinti\_CalendarOffset įdarbinti\_dienos įdarbinti\_GeographicLocation įdarbinti\_ApplicantName įdarbinti\_darbo įdarbinti\_veiklos įdarbinti\_darbo, įdarbinimo\_Media įdarbinti\_RecruitmentProject          |
| Įdarbinimo\_darbo          | Pradžios data, pabaigos data ir perėjimo data                        | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_GeographicLocation  | Miesto, apskrities, pašto kodas, ir valstiją arba provinciją                 | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_darbo                 | Funkciją, tipas ir pavadinimas                                        | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_Media               | Šaltinis pareiškėjų                                             | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_veiklos         | Reitingas, apibūdinimo ir vertinimo modelis                            | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_RecruitmentProject  | Projekto Aprašymas projekto būseną ir angos                | Įdarbinimo\_pareiškėją įdarbinti\_EmployedApplicant darbą\_TerminatedApplicant                                                                                                                                                               |
| Įdarbinimo\_TerminatedApplicant | Nutraukta pareiškėjų, priežastis, vykdymo ir nutraukimo dienos | Įdarbinti\_įmonės įdarbinti\_CalendarOffset įdarbinti\_dienos įdarbinti\_GeographicLocation įdarbinti\_veiklos įdarbinti\_gyventojai, įdarbinti\_darbo įdarbinti\_Media įdarbinti\_RecruitmentProject įdarbinti\_ApplicantName |

Šių subjektų buvo naudojama siekiant sukurti apskaičiuojamieji matai. Tai apskaičiuojama priemonės naudojami apskaičiuoti pagrindinius veiklos rodiklius (KPI) ir ataskaitų, kurias naudoja turinio paketas. Jei norite įtraukti papildomų skaičiavimų ataskaitos ir prietaisų skydelio, galite atsisiųsti ir pakeisti Recruiting.pbix failą iš LKD. Šis failas yra numatytasis duomenų modelis, kuris buvo naudojamas sukurti turinio paketas. Po to, kai jūs atlikote pakeitimus, galite sukurti organizacijos turinio paketas ir valdymo skydelį, kuriame yra informacija, kurią įtraukėte.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



