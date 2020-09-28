---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776313"
---
# <a name="human-resources-app-in-teams"></a>„Human Resources“ programa platformoje „Teams“

[!include [banner](includes/preview-feature.md)]

„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia darbuotojams greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“. Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu. Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.

![„Human Resources Teams“ atostogų programos robotas](./media/hr-admin-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Diegimas ir nustatymas

Programą „Human Resources“ galite rasti „Teams“ parduotuvėje. Daugiau informacijos, kaip įdiegti „Teams“ programą, žr. [Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md).

Informacijos apie programų teisių valdymą „Teams“ žr. [Programų teisių strategijų valdymas programoje „Microsoft Teams“](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>„Human Resources“ programos „Teams“ pranešimų įjungimas

Jei norite, kad vartotojai gautų atostogų užklausų pranešimus „Teams” programoje, turite įjungti pranešimus „Human Resources”.

>[!NOTE]
>Pranešimus gaus tik tie vartotojai, kurie yra prisijungę prie „Teams” ir naudoja „Human Resources Teams” programą.

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. Pasirinkite **Nuorodos**.

3. Dalyje **Sąranka** pasirinkite **Sistemos parametrai**.

4. Skirtuke **Bendra** nustatykite **Įjungti „Teams” programos pranešimus** į **Taip**.

   ![„Teams” programos pranešimų įjungimas sistemos parametruose](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Norėdami įjungti „Teams” pranešimus visiems vartotojams, paraginti pasirinkite **Taip**.

   ![„Teams” pranešimų įjungimas visiems vartotojams](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams

Įjungę „Human Resources Teams” programos pranešimus, galite įjungti arba išjungti pranešimus atskiriems vartotojams.

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. Pasirinkite **Nuorodos**.

3. Dalyje **Vartotojai** pasirinkite **Vartotojo parinktys**.

4. Pasirinkite skirtuką **Darbo eiga**.

5. Nustatykite parinktį **Įjungti „Teams” programos pranešimus** į **Taip**, norėdami įjungti pranešimus vartotojui, arba į **Ne**, norėdami išjungti pranešimus.

   ![„Teams” programos pranešimų įjungimas darbo eigos skirtuke Vartotojo parinktys](./media/hr-admin-teams-leave-app-notifications.png)

6. Pasirinkite **Įrašyti**.

## <a name="known-issues"></a>Žinomos problemos

| Išdavimas | Būsena |
| --- | --- |
| Horizontalus slankiojimas neveikia „Android“ telefonuose | Horizontalus slankiojimas nėra problema „iOS“ ar stacionariuose prietaisuose. Dirbame, kad ištaisytumėme šią problemą „Android“. |
| Klaida: kyla problemų ieškant aplinkos, prie kurios reikia prisijungti. | Galite gauti šią klaidą, net jei patikrinote, kad vartotojas gali pasiekti vieną ar daugiau „Human Resources“ aplinkų. Taip pat, galite nematyti visų jūsų norimų aplinkų. Kol išspręsite šią problemą, panaikinkite vartotoją ir importuokite juos dar kartą, kad išspręstumėte problemą. |
| Balansas yra netinkamas, kai ne darbo laikas pateikiamas būsimo laikotarpio datai. | Prognozavimas dar negalimas. Rodomas dabartinio laikotarpio balansas. |
| Nepavyksta atšaukti užklausos **Peržiūrima**. | Ši funkcija šiuo metu nepalaikoma ir bus įtraukta į būsimą leidimą. |
| Balanso informacija skaičiuojama iki šios dienos. | Sistema šiuo metu nerodo balansų iki kaupimo laikotarpio, net jei tai sukonfigūruotaa atostogų ir neatvykimo parametruose. |

## <a name="privacy-notice"></a>Privatumo pranešimas

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>„Microsoft Language Understanding Intelligent Service” (LUIS)

Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas. Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS). Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/). LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra). Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją. 

Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi. LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“. LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą. 

Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui. Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>„Microsoft Azure” įvykių tinklelis ir „Microsoft Teams”

Naudojant pranešimų funkciją, skirtą „Dynamics 365 Human Resources” programai „Teams”, tam tikri kliento duomenys bus naudojami už geografinio regiono, kuriame įdiegta jūsų nuomotojo „Human Resources“ paslauga, ribų. „Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure Event Grid” ir „Microsoft Teams”. Šie duomenys gali būti saugomi iki 24 val. ir apdorojami Jungtinėse Valstijose, jie yra užšifruojami tranzito bei neaktyvioje būsenose ir „Microsoft” arba jos antriniai procesoriai jų nenaudoja mokymui ar paslaugų tobulinimui.

## <a name="see-also"></a>Taip pat žiūrėkite 

[„Microsoft Teams“ atsisiuntimas ir diegimas](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[„Microsoft Teams“ pagalbos centras](https://support.office.com/teams)</br>
[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md)

