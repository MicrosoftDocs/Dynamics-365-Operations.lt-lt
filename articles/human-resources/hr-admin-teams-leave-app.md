---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: andreabichsel
manager: tfehr
ms.date: 09/30/2020
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
ms.openlocfilehash: ba520f873de5b20111f9134e87281bcdf4025785
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113561"
---
# <a name="human-resources-app-in-teams"></a>„Human Resources“ programa platformoje „Teams“

[!include [banner](includes/preview-feature.md)]

„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia darbuotojams greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“. Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu. Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija. Be to, jie gali siųsti žmonėms informaciją apie būsimą ne darbo laiką skiltyse „Komandos” ir „Pokalbiai” už „Human Resources” programėlės ribų.

![„Human Resources Teams“ atostogų programos robotas](./media/hr-admin-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)

![„Human Resources” atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-card.png)

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
| Balansas yra netinkamas, kai ne darbo laikas pateikiamas būsimo laikotarpio datai. | Prognozavimas dar negalimas. Rodomas dabartinio laikotarpio balansas. |
| Nepavyksta atšaukti užklausos **Peržiūrima**. | Ši funkcija šiuo metu nepalaikoma ir bus įtraukta į būsimą leidimą. |
| Balanso informacija skaičiuojama iki šios dienos. | Sistema šiuo metu nerodo balansų iki kaupimo laikotarpio, net jei tai sukonfigūruotaa atostogų ir neatvykimo parametruose. |

## <a name="troubleshooting"></a>Trikčių šalinimas

Jei vartotojui kyla problemų prisijungiant arba naudojant „Human Resources Teams“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis. Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą. Norėdami gauti daugiau informacijos, [Gauti pagalbos](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nepavyksta prisijungti prie „Teams“ programos „Human Resources“

Jei vartotojas susisiekia su jumis, nes jis negali prisijungti prie programos, patikrinkite, ar vartotojas „Human Resources“ turi susijusį darbuotojo įrašą.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“

Jei vartotojas gauna klaidą bandydamas patvirtinti atostogų prašymą programoje „Teams“, atlikite šiuos trikčių šalinimo veiksmus:

1. Įsitikinkite, kad jo „Teams“ paskyra sutampa su naudojama prieigai prie „Human Resources“ paskyra.

2. Patikrinkite, ar vartotojas gali patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus. Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).

## <a name="privacy-notice"></a>Privatumo pranešimas

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>„Microsoft Language Understanding Intelligent Service” (LUIS)

Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas. Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS). Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/). LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra). Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją. 

Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi. LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“. LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą. 

Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui. Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”

Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.

„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”. Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”. Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Taip pat žiūrėkite 

[„Microsoft Teams“ atsisiuntimas ir diegimas](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[„Microsoft Teams“ pagalbos centras](https://support.office.com/teams)</br>
[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md)

