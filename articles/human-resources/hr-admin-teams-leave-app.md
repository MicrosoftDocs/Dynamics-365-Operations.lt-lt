---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3b717cf2fb8663ed8e4981981d563672c9e645c4f9b592ee1896cfef4236396
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772722"
---
# <a name="human-resources-app-in-teams"></a>„Human Resources“ programa platformoje „Teams“

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia darbuotojams greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“. Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu. Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija. Be to, jie gali siųsti žmonėms informaciją apie būsimą ne darbo laiką skiltyse „Komandos” ir „Pokalbiai” už „Human Resources” programėlės ribų.

![„Human Resources Teams“ atostogų programos robotas.](./media/hr-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas.](./media/hr-teams-leave-app-timeoff-tab.png)

![„Human Resources” atostogų užklausos kortelė.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Diegimas ir nustatymas

Programą „Dynamics 365 Human Resources“ galite rasti „Teams“ parduotuvėje. Daugiau informacijos, kaip įdiegti „Teams“ programą, žr. [Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md).

Informacijos apie programų teisių valdymą „Teams“ žr. [Programų teisių strategijų valdymas programoje „Microsoft Teams“](/MicrosoftTeams/teams-app-permission-policies).

Jei norite, kad jūsų naudotojai programėlėje peržiūrėti atostogų ir neatvykimo kalendorių, funkcijų valdymo srityje turėsite įjungti **Atostogų ir neatvykimo kalendorių komandose**. Daugiau informacijos apie funkcijų įjungimą žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>„Human Resources“ programos „Teams“ pranešimų įjungimas

Jei norite, kad vartotojai gautų atostogų užklausų pranešimus „Teams” programoje, turite įjungti pranešimus „Dynamics 365 Human Resources”.

>[!NOTE]
>Pranešimus gaus tik tie vartotojai, kurie yra prisijungę prie „Teams” ir naudoja „Dynamics 365 Human Resources” programą.

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. Pasirinkite **Nuorodos**.

3. Dalyje **Sąranka** pasirinkite **Sistemos parametrai**.

4. Skirtuke **Bendra** nustatykite **Įjungti „Teams” programos pranešimus** į **Taip**.

   ![„Teams” programos pranešimų įjungimas sistemos parametruose.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Norėdami įjungti „Teams” pranešimus visiems vartotojams, paraginti pasirinkite **Taip**.

   ![„Teams” pranešimų įjungimas visiems vartotojams.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams

Įjungę „Dynamics 365 Human Resources” komandų programos pranešimus, galite įjungti arba išjungti pranešimus atskiriems vartotojams.

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. Pasirinkite **Nuorodos**.

3. Dalyje **Vartotojai** pasirinkite **Vartotojo parinktys**.

4. Pasirinkite skirtuką **Darbo eiga**.

5. Nustatykite parinktį **Įjungti „Teams” programos pranešimus** į **Taip**, norėdami įjungti pranešimus vartotojui, arba į **Ne**, norėdami išjungti pranešimus.

   ![„Teams” programos pranešimų įjungimas darbo eigos skirtuke Vartotojo parinktys.](./media/hr-admin-teams-leave-app-notifications.png)

6. Pasirinkite **Įrašyti**.

## <a name="supported-languages"></a>Palaikomos kalbos

Programa „Dynamics 365 Human Resources“ komandose palaiko šias kalbas:

| Vietos ID | Kalba |
| --- | --- |
| de-DE | Vokiečių (Vokietija) |
| es-ES | Ispanų (Ispanija) |
| es-MX | Ispanų (Meksika) |
| fr-CA | Prancūzų (Kanada) |
| fr-FR | Prancūzų (Prancūzija) |
| it-IT | Italų (Italija) |
| nl-NL | Olandų (Nyderlandai) |
| pt-BR | Portugalų (Brazilija) |
| tr-TR | Turkų (Turkija) |
| zh-CN | Kinų (supaprastintoji) |

## <a name="notes"></a>Pastabos

Toliau nurodyti darbo elementai perduodami tolesniems leidimams:

| Darbo elementas | Būsena |
| --- | --- |
| Balansas yra netinkamas, kai ne darbo laikas pateikiamas būsimo laikotarpio datai. | Prognozavimas dar negalimas. Rodomas dabartinio laikotarpio balansas. |
| Nepavyksta atšaukti užklausos **Peržiūrima**. | Ši funkcija šiuo metu nepalaikoma ir bus įtraukta į būsimą leidimą. |
| Balanso informacija skaičiuojama iki šios dienos. | Sistema šiuo metu nerodo balansų iki kaupimo laikotarpio, net jei tai sukonfigūruota atostogų ir neatvykimo parametruose. |

## <a name="troubleshooting"></a>Trikčių šalinimas

Jei vartotojui kyla problemų prisijungiant arba naudojant „Human Resources Teams“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis. Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą. Norėdami gauti daugiau informacijos, [Gauti pagalbos](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nepavyksta prisijungti prie „Teams“ programos „Human Resources“

Jei naudotojas susisiekia su jumis, nes jis negali prisijungti prie programos, patikrinkite, ar jis turi „Human Resources“ turi susijusį darbuotojo įrašą.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“

Jei vartotojas gauna klaidą bandydamas patvirtinti atostogų prašymą programoje „Teams“, išbandykite šiuos trikčių šalinimo veiksmus:

1. Įsitikinkite, kad jo „Teams“ paskyra sutampa su naudojama prieigai prie „Human Resources“ paskyra.

2. Patikrinkite, ar vartotojas gali patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus. Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Palikti tvirtintojams negauus pokalbių su „Teams“ pranešimais atostogų užklausoms patvirtinti

1. Užtikrinkite, kad aplinkos ir vartotojo pranešimai yra įgalinti. Dėl daugiau informacijos, žiūrėkite [Įjungti „Human Resources“ programos pranešimus „Teams“](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ir [Įjungti „Teams“ pranešimus ir juos išjungti atskiriems vartotojams](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Įsitikinkite, kad vartotojai yra prisiregistravę pokalbių skirtuke naudodami tą **pačią** prisijungimo informaciją, kuriuos jie naudoja atostogų užklausoms patvirtinti. Norėdami prisijungti naudodami tinkamą prisjungimo informaciją, naudokite pranešimus „atsijungti" ir „prisijungti".

3. Jei problema išlieka, patikrinkite verslo įvykių sistemos paketinės užduoties būseną kaip sistemos administratorių. Jei jis yra laukimo ar vykdymo etape, po kelių minučių patikrinkite atgal. Jei būsena nekinta, užregistruokite palaikymo bilietą, kad mūsų komanda galėtų padėti išspręsti problemą.

## <a name="privacy-notice"></a>Privatumo pranešimas

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>„Microsoft Language Understanding Intelligent Service” (LUIS)

Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas. Vartotojo įvestis, pavyzdžiui, „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų, pavadinimu „Language Understanding Intelligent Service“ (LUIS). Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/). LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra paskyra, pavadinta „Contoso”). Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.

Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure bot framework“ apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi. LUIS tarnyba ir „Azure bot framework“ gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“. LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išsiųstas į LUIS tarnybą ir „Azure bot framework“. 

Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui. Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”

Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.

„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”. Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”. Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Taip pat žiūrėkite 

[„Microsoft Teams“ atsisiuntimas ir diegimas](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[„Microsoft Teams“ pagalbos centras](https://support.office.com/teams)</br>
[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]