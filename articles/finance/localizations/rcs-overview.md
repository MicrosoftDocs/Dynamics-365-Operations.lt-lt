---
title: Regulatory Configuration Service
description: Šioje temoje pateikiama „Regulatory Configuration Service” (RCS) galimybių apžvalga ir paaiškinama, kaip pasiekti paslaugą.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 312fe318009a05de63fdba6aa8e6431836993957
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345178"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

„Regulatory Configuration Service” (RCS) yra atskira dizaino ir ciklo valdymo paslauga, skirta „jokio kodo”/„mažai kodų” globalizavimo funkcijai. RCS leidžia globalizavimo suinteresuotosioms šalims be programų kūrėjų dalyvavimo išplėsti ir tinkinti mokesčių, elektroninių SF išrašymo, teisės aktų nustatytų ataskaitų, bankininkystės ir verslo dokumentų pagrindines globalizavimo sritis. Dėl šio „jokio kodo”/„mažai kodų” globalizavimo požiūrio, globalizavimas yra paprastesnis, greitesnis ir ekonomiškesnis kūrimui ir išplėtimui.

„RCS” suteikia šias galimybes:

- Visų Elektroninių ataskaitų (ER) suteikiamų funkcijų palaikymą.
- Būtinuosius naujų globalizavimo mikropaslaugų konfigūravimo komponentus.
- Elektroninių sąskaitų faktūrų išrašymo palaikymą. Daugiau informacijos rasite [Elektroninių sąskaitų faktūrų išrašymas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Mokesčių skaičiavimo palaikymą. Daugiau informacijos rasite [Mokesčių paslauga](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Naujų globalizavimo funkcijų, kurios supaprastina kelių komponentų funkcijų ciklo valdymą ir suteikia daugiau galimybių konfigūruoti veiksmus ir nustatyti funkcijų parametrus palaikymą. Daugiau informacijos rasite [„Regulatory Configuration Service” – supaprastintas globalizavimo funkcijų valdymas, skirtas globalizavimo paslaugoms](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Pasirinktinių konfigūracijų centralizuoto skelbimo, saugojimo ir bendrinimo bendrojoje saugykloje, kurie supaprastina konfigūracijų valdymą nenaudojant „Microsoft Dynamics Lifecycle Services” (LCS), palaikymą.

## <a name="access-rcs"></a>RCS prieiga

Galite užsiregistruoti arba prisijungti prie RCS iš [„Regulatory Configuration Service” puslapio](https://marketing.configure.global.dynamics.com/).

![RCS registravimasis/prisijungimas.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Puslapyje **„Regulatory Configuration Service”** peržiūrėkite ir priimkite papildomas paslaugos naudojimo sąlygas ir pasirinkite vieną iš šių mygtukų:

- **Registruotis**, jei pirmą kartą naudojatės paslauga ir naudojate darbo el. pašto adresą, kad savo organizacijai parengtumėte paslaugų aplinką
- **Prisijungti**, jeigu anksčiau buvote prisiregistravę prie paslaugos ir norite pasiekti savo organizacijos aplinką

> [!NOTE] 
> Pasirašius rekomenduojame į RCS aplinką įtraukti papildomą SysAdmin vartotoją. Šis vartotojas bus laikomas aplinkos sudėtiuoju administratoriumi. Tai padės užtikrinti RCS aplinkos stabilumą, nes SysAdmin vaidmuo – valdyti tos aplinkos vartotojus. Galite pridėti vartotojus naudodami **RCS darbo sritį > administravimo sistemoje**.

## <a name="regional-availability"></a>Regioninis prieinamumas

RCS yra bendrai prieinamas šiuose regionuose:

- Jungtinės Valstijos
- Indija
- Prancūzija
- Europa

Pilną regionų sąrašą rasite [„Dynamics 365” ir „Power Platform”: Pasiekiamumas, duomenų vieta, kalba ir lokalizavimas](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>RCS numatytoji įmonė

Kūrimo laiko funkcija, naudojama RCS, bendrai naudojama visoms įmonėms. Nėra įmonei specialių funkcijų. Todėl rekomenduojame naudoti vieną įmonę, **DAT**, su savo RCS aplinka.

Tačiau kai kuriuose scenarijuose galite norėti, kad ER formatai būtų naudojami parametrai, susiję su konkrečiu juridiniu subjektu. Tik šiuose scenarijuose turėtumėte naudoti numatytąjį įmonės perjungimo priemonę. Dėl pavyzdžio, žr. [ER formato konfigūravimas, kurį atlikus naudojami juridiniam subjektui nurodyti parametrai](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Susijusi RCS dokumentacija

Daugiau informacijos apie susijusius komponentus rasite šiose temose:

- **Rcs:**

    - [Kurkite ER konfigūracijas RCS ir įkelkite jas į bendrąją saugyklą](rcs-global-repo-upload.md)

- **Bendroji saugykla:**

    - [ER konfigūracijos kūrimas ir įkėlimas į Bendrąją saugyklą](rcs-global-repo-upload.md)
    - [Konfigūracijos bendrinimas Bendrojoje saugykloje](rcs-global-repo-share-configuration.md)
    - [Išplėstinis filtravimas Bendrojoje saugykloje](enhanced-filtering-global-repo.md)
    - [ER konfigūracijų atsisiuntimas iš Bendrosios saugyklos](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Konfigūracijų nutraukimas Bendrojoje saugykloje](discontinuing-configurations-rcs-global-repo.md)
    - [„Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nebegalioja](rcs-lcs-repo-dep-faq.md)

- **Globalizavimo funkcija**

    - [„Regulatory Configuration Service“ (RCS) – Globalizavimo funkcija](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>RCS trikčių šalinimo prisijungimas

Kai prisiregistruojate prie RCS aptarnavimo puslapyje, galite susidurti su problema, kuri susijusi „Azure Active Directory“ („Azure AD“). Klaidos pranešimas, kurį gaunate, nurodo, kad RCS registracija šiuo metu išjungta ir turi būti įjungta prieš užbaigiant registracijos procesą.

![RCS registracijos klaidos pranešimas.](media/01_RCSSignUpError.jpg)

Problema kyla dėl to, kad jūs blokuojate ad hoc abonementų pasirašymą ir ypatybė turi būti įgalinta `AllowAdHocSubscriptions` jūsų nuomininke. 

- Jei jūsų IT padalinys valdo jūsų organizacijos „Azure" nuomininkus, susisiekite su tuo padaliniu ir praneškite apie išdavimą.
- Jei esate atsakingas už „Azure" nuomininkų valdymą, galite išspręsti problemas, atlikite nurodytus veiksmus, nurodytus [Kas yra savitarnos „Azure Active Directory“ registracija](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
