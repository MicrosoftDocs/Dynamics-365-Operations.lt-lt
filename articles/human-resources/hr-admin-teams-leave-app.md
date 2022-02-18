---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: twheeloc
ms.date: 12/15/2021
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
ms.openlocfilehash: ffd6967431227b578e227ee570dbe06c356fb8d6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067056"
---
# <a name="human-resources-app-in-teams"></a>„Human Resources“ programa platformoje „Teams“


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Microsoft“.Dynamics 365 Human Resources programėlėje Microsoft Teams leiskime darbuotojams greitai paprašyti laisvo laiko ir peržiūrėti informaciją apie jų nebuvimo balansą Microsoft Teams. Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu. Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija. Be to, jie gali siųsti žmonėms informaciją apie būsimą ne darbo laiką skiltyse „Komandos” ir „Pokalbiai” už „Human Resources” programėlės ribų.

![„Human Resources Teams“ atostogų programos robotas.](./media/hr-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas.](./media/hr-teams-leave-app-timeoff-tab.png)

![„Human Resources” atostogų užklausos kortelė.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Diegimas ir nustatymas

Programą „Dynamics 365 Human Resources“ galite rasti „Teams“ parduotuvėje. Daugiau informacijos, kaip įdiegti „Teams“ programą, žr. [Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md).

Informacijos apie programų teisių valdymą „Teams“ žr. [Programų teisių strategijų valdymas programoje „Microsoft Teams“](/MicrosoftTeams/teams-app-permission-policies).

Jei norite, kad jūsų naudotojai programėlėje peržiūrėti atostogų ir neatvykimo kalendorių, funkcijų valdymo srityje turėsite įjungti **Atostogų ir neatvykimo kalendorių komandose**. Daugiau informacijos apie funkcijų įjungimą žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).

## <a name="update-app"></a>Atnaujinkite programą
>[!NOTE]
> Nuo 2021 m. gruodžio 20 d. „Microsoft“ nuomininke priglobtos „Human Resources App“ roboto paslaugos bus nutrauktos. Neturės įtakos atnaujintam plėtiniui (versija 1.1.5), kurį galima įdiegti. Pagrindinis poveikis bus pasenusiam plėtiniui (versija 1.1.4). Šios versijos pokalbių robotas nustos veikti. The **Laikas baigėsi** skirtukas ir toliau veiks abiejuose plėtiniuose.

1.1.4 versijos pokalbių robotas nustos reaguoti į bet kokį pranešimą. Pavyzdžiui, **Prisijungti**, **likučius**, ir **Žiūrėkite poilsio laiką**. Programa turi būti atnaujinta rankiniu būdu į naujausią versiją. Daugiau informacijos žr [Atnaujinkite programas Microsoft Teams](/MicrosoftTeams/apps-update-experience).

Norėdami atnaujinti į 1.1.5 versiją, atlikite šiuos veiksmus:
1. Į Microsoft Teams, eiti į **Programėlės**.
2. Surask **Žmogiškieji ištekliai** programėlė.
3. Pasirinkite **Patobulinti**.

Žmogiškųjų išteklių programos versiją galite patikrinti apsilankę adresu **Apie** skirtuke arba eidami į **Asmeninė programėlė** skyrius. 

![Žmogiškieji ištekliai **Apie** skirtuką.](./media/HR-teams-about.png)

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
| Balanso informacija skaičiuojama iki šios dienos. | Sistema šiuo metu nerodo likučių kaupimo laikotarpiu, net jei ji sukonfigūruota **Atostogų ir nebuvimo parametrai** puslapį. |

## <a name="troubleshooting"></a>Trikčių šalinimas

Jei vartotojui kyla problemų prisijungiant arba naudojant „Human Resources Teams“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis. Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą. Norėdami gauti daugiau informacijos, [Gauti pagalbos](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Įsitikinkite, kad Teams žmogiškųjų išteklių programa yra atnaujinta
Jei susiduriate su problemomis su Teams Human Resources programėle, turite patvirtinti, kad naudojate naujausią versiją. Mažiausiai palaikoma versija yra 1.1.5. Instrukcijas, kaip atnaujinti Teams programą, žr [Komandos dokumentacija](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nepavyksta prisijungti prie „Teams“ programos „Human Resources“

Jei naudotojas susisiekia su jumis, nes jis negali prisijungti prie programos, patikrinkite, ar jis turi „Human Resources“ turi susijusį darbuotojo įrašą.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“

Jei vartotojas gauna klaidą bandydamas patvirtinti atostogų užklausas Teams programoje, pabandykite atlikti šiuos trikčių šalinimo veiksmus:

1. Įsitikinkite, kad jo „Teams“ paskyra sutampa su naudojama prieigai prie „Human Resources“ paskyra.

2. Patikrinkite, ar vartotojas gali patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus. Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Palikti tvirtintojams negauus pokalbių su „Teams“ pranešimais atostogų užklausoms patvirtinti

1. Užtikrinkite, kad aplinkos ir vartotojo pranešimai yra įgalinti. Dėl daugiau informacijos, žiūrėkite [Įjungti „Human Resources“ programos pranešimus „Teams“](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ir [Įjungti „Teams“ pranešimus ir juos išjungti atskiriems vartotojams](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Įsitikinkite, kad vartotojai yra prisiregistravę pokalbių skirtuke naudodami tą **pačią** prisijungimo informaciją, kuriuos jie naudoja atostogų užklausoms patvirtinti. Norėdami prisijungti naudodami tinkamą prisjungimo informaciją, naudokite pranešimus „atsijungti" ir „prisijungti".

3. Jei problema išlieka, patikrinkite būseną **Verslo renginių sistema** paketinis sistemos administratoriaus darbas. Jei jis yra a **Laukia** arba **Vykdymas** etape, patikrinkite dar kartą po kelių minučių. Jei būsena nesikeičia, užregistruokite palaikymo bilietą, kad mūsų komanda galėtų padėti išspręsti problemą.

## <a name="privacy-notice"></a>Privatumo pranešimas

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>„Microsoft Language Understanding Intelligent Service” (LUIS)

Su Dynamics 365 Human Resources bot in Microsoft Teams, vartotojo teksto įvestis analizuojamos siekiant suprasti pagrindinę užklausą / tikslą. Vartotojo įvestis, pvz., „Paieškos paskyra Contoso“, nukreipiama į vieną iš „Microsoft“ pažinimo paslaugų, vadinamų kalbos supratimo intelektualiąja tarnyba (LUIS). Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/). LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra). Tada ši informacija perduodama „Microsoft“. [Azure botų sistema](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis iš Dynamics 365 Human Resources ir nuskaito pageidaujamą informaciją vartotojo užklausai.

Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure bot framework“ apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi. LUIS tarnyba ir „Azure bot framework“ gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“. Nors LUIS paslauga turi prieigą tik prie vartotojo užklausų ir nėra skirta prisijungti prie vartotojo Dynamics 365 Human Resources duomenis ar paskyrą, vartotojas Dynamics 365 Human Resources robotas gali savanoriškai įvesti užklausą, kurioje yra Kliento duomenų, asmens duomenų ar kitų duomenų, ir toks užklausos turinys gali būti išsiųstas į LUIS paslaugą ir Azure roboto sistemą. 

Vartotojo užklausų ir pranešimų turinys LUIS sistemoje saugomas ne ilgiau kaip 30 dienų, ramybės būsenoje yra šifruojamas ir nenaudojamas mokymams ar paslaugų tobulinimui. Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”

Kai naudojate Dynamics 365 Human Resources programėlėje Microsoft Teams, tam tikri klientų duomenys gali būti perduodami už geografinio regiono, kuriame yra įdiegta jūsų nuomininko žmogiškųjų išteklių paslauga, ribų.

Dynamics 365 Human Resources perduoda darbuotojo atostogų prašymą ir darbo eigos užduoties duomenis Microsoft Azure Renginių tinklelis ir Microsoft Teams. Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”. Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Taip pat žiūrėkite 

[„Microsoft Teams“ atsisiuntimas ir diegimas](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[„Microsoft Teams“ pagalbos centras](https://support.office.com/teams)</br>
[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
