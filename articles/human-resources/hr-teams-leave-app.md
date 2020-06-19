---
title: Atostogų prašymų valdymas „Teams“
description: Šioje temoje parodyta, kaip prašyti išleisti iš darbo programoje „Dynamics 365 Human Resources“ naudojant „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428833"
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
 
Pateikus atostogų prašymą, galite koreguoti dienas pačioje kortelėje arba galite pasirinkti **Redaguoti informaciją**, jei norite į prašymą įtraukti papildomos informacijos.

![„Human Resources Teams“ atostogų programos redagavimo prašymas](./media/hr-teams-leave-app-bot-edit.png)
 
Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą. Taip pat galite įvesti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.

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
   
## <a name="privacy-notice"></a>Privatumo pranešimas

Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas. Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS). Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/). LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra). Tada ši informacija perduodama į „Microsoft“  [„Azure“ roboto sistemą](https://azure.microsoft.com/services/bot-service/) , kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją. 

Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi. LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“. LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą. 

Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui. Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Taip pat žiūrėkite

[„Microsoft Teams“ atsisiuntimas ir diegimas](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[„Microsoft Teams“ pagalbos centras](https://support.office.com/teams)</br>
[„Human Resources“ programa platformoje „Teams“](hr-admin-teams-leave-app.md)
