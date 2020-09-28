---
title: Atostogų prašymų valdymas „Teams“
description: Šioje temoje parodyta, kaip prašyti išleisti iš darbo programoje „Dynamics 365 Human Resources“ naudojant „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766765"
---
# <a name="manage-leave-requests-in-teams"></a>Atostogų prašymų valdymas „Teams“

[!include [banner](includes/preview-feature.md)]

„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“. Norėdami prašyti informacijos, galite bendrauti su robotu. Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.

## <a name="install-the-app"></a>Programos diegimas

Programą „Human Resources“ galite rasti „Teams“ parduotuvėje.

1. Programoje „Microsoft Teams“ pasirinkite daugtaškius.

   ![„Human Resources Teams“ atostogų programos daugtaškiai](./media/hr-teams-leave-app-ellipses.png)
 
2. Raskite „Dynamics 365 Human Resources“ ir pasirinkite plytelę **Human Resources**.

   ![„Human Resources Teams“ atostogų programos HR plytelė](./media/hr-teams-leave-app-human-resources-tile.png)

3. Pasirinkite mygtuką **Įtraukti**, kad įdiegtumėte programą.

   ![„Human Resources Teams“ atostogų programos diegimas](./media/hr-teams-leave-app-in-store.png)

Jei programa automatiškai jūsų neprijungia, norėdami prisijungti pasirinkite skirtuką **Parametrai**.

![„Human Resources Teams“ atostogų programos mygtukas Parametrai](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai. 

Jei turite prieigą prie daugiau nei vieno „Human Resources“ egzemplioriaus, galite pasirinkti, kurią aplinką norite prijungti prie skirtuko **Parametrai**.

> [!WARNING]
> Programa šiuo metu nepalaiko sistemos administratoriaus saugos vaidmens ir rodys klaidos pranešimą, jei prisijungsite naudodami sistemos administratoriaus paskyrą. Norėdami prisijungti su kita paskyra, skirtuke **Parametrai** pasirinkite mygtuką **Perjungti paskyras**, tada prisijunkite naudodami vartotojo paskyrą, kuri neturi sistemos administratoriaus teisių.
 
## <a name="use-the-bot"></a>Roboto naudojimas

Kai programa įdiegiama, rodomas pasveikinimo pranešimas, kuriame informuojama, kokio tipo veiksmus jūsų vardu gali atlikti robotas.

![„Human Resources Teams“ atostogų programos roboto pasveikinimo pranešimas](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Pirmą kartą bendraujant su robotu, gali reikėti prisijungti. Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.

Roboto galite prašyti toliau pateiktų dalykų.

- Rodyti kiekvieno atostogų tipo, kuriam esate užsiregistravę, ne darbo laiko balanso informaciją.

   ![„Human Resources Teams“ atostogų programos rodomi balansai](./media/hr-teams-leave-app-bot-balances.png)
 
- Rodyti papildomą informaciją apie konkretų atostogų tipą.

   ![„Human Resources Teams“ atostogų programos rodoma informacija](./media/hr-teams-leave-app-bot-details.png)

- Pateikti atostogų prašymą už jus.

   ![„Human Resources Teams“ atostogų programos atostogų prašymas](./media/hr-teams-leave-app-bot-request.png)
 
Pateikus atostogų užklausą, galite koreguoti dienas pačioje kortelėje.

![„Human Resources Teams“ atostogų programos redagavimo prašymas](./media/hr-teams-leave-app-bot-edit.png)
 
Kai užpildysite visą informaciją, pasirinkite **Pateikti**, kad pateiktumėte patvirtinimą. Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.

![„Human Resources Teams“ atostogų programos prašymo pateikimas](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Atostogų valdymas programoje „Teams“

Skirtuke **Ne darbo laikas** galite peržiūrėti:

- Kiekvieno atostogų tipo, kuriam esate užsiregistravę, balanso informaciją

- Būsimų atostogų prašymus

- Prašymus išleisti iš darbo

- Atostogų prašymų juodraščius

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Naujo prašymo kūrimas

1. Norėdami kurti naują atostogų prašymą, pasirinkite **Naujas prašymas**.

   ![„Human Resources Teams“ atostogų programos naujas prašymas](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Įveskite dieną ar dienas, kuriomis norite nedirbti, tada pasirinkite **Įtraukti**.

   ![„Human Resources Teams“ atostogų programos ne darbo laiko įtraukimas](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Jei reikia, įveskite priežasties kodą. Taip pat, jei reikia įveskite komentarus ir įtraukite priedus.

4. Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą. Taip pat galite įvesti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.

### <a name="manage-draft-requests"></a>Prašymų juodraščių valdymas

1. Pasirinkite skirtuką **Juodraščiai**.

   ![„Human Resources Teams“ atostogų programos skirtukas Juodraščiai](./media/hr-teams-leave-app-drafts-tab.png)

2. Norėdami redaguoti prašymą pasirinkite pieštuką arba pasirinkite šiukšlinę, jei prašymą norite panaikinti.

3. Atlikite reikiamus pakeitimus. Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą. Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.

   ![„Human Resources Teams“ atostogų programos juodraščio redagavimas](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a>„Teams” pranešimai

Kai jūs arba darbuotojas, kurio tvirtintojas esate jūs, pateikiate atostogų užklausą, gausite pranešimą „Human Resources“ programoje „Teams“. Galite pasirinkti pranešimą, norėdami jį peržiūrėti. Pranešimai taip pat rodomi **pokalbių** srityje.

Jei esate tvirtintojas, pranešime galite pasirinkti **Patvirtinti** arba **Atmesti**. Taip pat galite pateikti pasirinktinį pranešimą.

![Atostogų užklausos pranešimas programoje „Human Resources Teams“](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a>Peržiūrėti komandos atostogų kalendorių

Jeigu esate vadovas, valdantis tiesiogines ataskaitas, galite peržiūrėti jūsų komandos patvirtintą ir laukiamą ne darbo laiką.

1. „Human Resources“ programoje „Teams“ pasirinkite **Ne darbo laikas**.

2. Pasirinkite **Komandos kalendorius**.

   ![Kalendoriaus peržiūra „Human Resources Teams“ programoje](./media/hr-teams-leave-app-view-calendar.png)

Kalendorius rodo jūsų tiesioginių ataskaitų patvirtintą ir laukiamą ne darbo laiką.

![Ne darbo laiko kalendorius „Human Resources Teams“ programoje](./media/hr-teams-leave-app-calendar.png)

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
[„Human Resources“ programa „Teams“](hr-admin-teams-leave-app.md)
