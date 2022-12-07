---
title: Atostogų prašymų valdymas „Teams“
description: Šiame straipsnyje rodoma, kaip programoje programoje pateikti užklausą Dynamics 365 Human Resources dėl laiko Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84f1190301e67b49535530f85784561b2e51a2df
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812166"
---
# <a name="manage-leave-requests-in-teams"></a>Atostogų prašymų valdymas „Teams“

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Microsoft Teams“ veikianti programa „Dynamics 365 Human Resources“ leidžia greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“. Galite sąveikauti su robotu, kad prašytumėte informacijos ir pradėtumėte atostogų užklausą. Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija. Galite taip pat nusiųsti asmenų informacija apie jūsų ateinantį nebuvimo laiką komandose ir pokalbius ne personalo programoje.

## <a name="install-the-app"></a>Programos diegimas

Programą „Dynamics 365 Human Resources“ galite rasti „Teams“ parduotuvėje.

1. „Microsoft Teams” pereikite į programų sąrašą.
 
2. Raskite „Dynamics 365 Human Resources“ ir pasirinkite plytelę **Human Resources**.

> [!NOTE]
> Nuo 2021 m. gruodžio 20 d. "Human Resources App bot services" (versija 1.1.4), laikomos "Microsoft" nuomininkuose, bus perimtos. Naujausią plėtinį (versijos 1.1.5) galima įdiegti. Daugiau informacijos ieškokite Tvarkyti atostogų [užklausas komandose](hr-admin-teams-leave-app.md#update-app).

3. Pasirinkite mygtuką **Įtraukti**, kad įdiegtumėte programą.

Jei programa automatiškai jūsų neprijungia, norėdami prisijungti pasirinkite skirtuką **Parametrai**.

> [!NOTE]
> Jei nematote prisijungimo dialogo lango, atnaujinkite naršyklės parametrus, kad būtų leidžiama prisijungti prie laikinųjų langų. 

Jei turite prieigą prie daugiau nei vieno „Human Resources“ egzemplioriaus, galite pasirinkti, kurią aplinką norite prijungti prie skirtuko **Parametrai**.

> [!NOTE]
> Programėlė dabar palaiko sistemos administratoriaus saugos vaidmenį.
 
## <a name="use-the-bot"></a>Roboto naudojimas

Kai programa įdiegiama, rodomas pasveikinimo pranešimas, kuriame informuojama, kokio tipo veiksmus jūsų vardu gali atlikti robotas.

> [!NOTE]
> Kai pirmą kartą bendraujate su bot, gali reikėti prisiregistruoti. Jei nematote prisijungimo dialogo lango, atnaujinkite naršyklės parametrus, kad būtų leidžiama prisijungti prie laikinųjų langų.

Roboto galite prašyti toliau pateiktų dalykų:

- Peržiūrėti savo dabartinius atostogų balansus. Pavyzdžiui, išsiųskite pranešimą „Peržiūrėti atostogų balansus.”

- Pateikti atostogų prašymą už jus. Pavyzdžiui, siųskite pranešimą, kuriame teigiama, kad "Paimti atostogų laiką" arba "Norėčiau paimti atostogų laiką kitą ketvirtadienį ir penktadienį", jei norite prašyti atostogų tipo. 

  ![Atostogų užklausos paleidimas komandos pokalbyje.](./media/hr-teams-leave-app-initiate.png)

- Pokalbių robotas jums užpildys prašymą išeiti atostogų. Pasirinkite **Prašyti išleisti iš darbo** ir redaguokite savo prašymo duomenis.

   Jei norite pateikti kelių tos pačios datos atostogų tipų atostogų užklausas, pasirinkite **Skaidyti dieną** parinktį iš meniu **Daugiau parinkčių**. 

   Jei išeisite pusdieniui, kai atostogų užklausos vienetas pateiktas dienomis, galite nurodyti, ar norite prašyti laisvo laiko pirmoje, ar antroje dienos pusėje, pasirinkdami **Pusės dienos apibrėžimas** parinktį iš meniu **Daugiau parinkčių**.
   
   ![Pusės dienos apibrėžimai.](./media/HalfDayDefinitions.png)

- Kai baigsite redaguoti savo prašymo išeiti atostogų duomenis, pasirinkite **Pateikti** ir pateikite jį patvirtinti.

  ![Prašymo išeiti atostogų pateikimas.](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Atostogų valdymas programoje „Teams“

Skirtuke **Ne darbo laikas** galite peržiūrėti: 

- Kiekvieno atostogų tipo, kuriam esate užsiregistravę, balanso informaciją

- Būsimų atostogų prašymus

- Prašymai išleisti iš darbo

- Atostogų prašymų juodraščius
 
### <a name="create-a-new-request"></a>Naujo prašymo kūrimas

1. Norėdami kurti naują atostogų prašymą, pasirinkite **Naujas prašymas**.

2. Įveskite dieną ar dienas, kuriomis norite nedirbti, tada pasirinkite **Įtraukti**.

   ![„Human Resources Teams“ atostogų programos ne darbo laiko įtraukimas.](./media/TimeOffHours.png)

3. Jei reikia, įveskite priežasties kodą. Taip pat, jei reikia įveskite komentarus ir įtraukite priedus.

4. Pasirinkite **Skaidyti dieną** parinktį iš meniu **Daugiau parinkčių**, jei norite pateikti kelių tos pačios datos atostogų tipų atostogų užklausas.

5. Pasirinkite **Pusės dienos apibrėžimas** parinktį, kad nurodytumėte, ar norite prašyti ne darbo laiko pirmojoje, ar antrojoje dienos pusėje. Ši parinktis yra galima, kai atostogų užklausos vienetas pateikiamas dienomis, o prašoma suma yra 0,5 dienos.

6. Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte ją patvirtinimui. Jūs taip pat galite įvesti **Įrašyti kaip juodraštį**, kad grįžtumėte prie jos vėliau.

### <a name="manage-draft-requests"></a>Prašymų juodraščių valdymas

1. Pasirinkite skirtuką **Juodraščiai**.

2. Norėdami redaguoti prašymą pasirinkite pieštuką arba pasirinkite šiukšlinę, jei prašymą norite panaikinti.

3. Atlikite reikiamus pakeitimus. Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą. Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.
   
### <a name="respond-to-teams-notifications"></a>Atsakyti į „Teams” pranešimus

Kai jūs arba darbuotojas, kurį esate tvirtintojas, kuris pateikia atostogų užklausą, gausite pranešimą personalo komandose. Galite pasirinkti pranešimą atostogų užklausai peržiūrėti. Pranešimai taip pat rodomi **pokalbių** srityje.

Jei esate tvirtintojas, pranešime galite pasirinkti **Patvirtinti** arba **Atmesti**. Taip pat galite pateikti pasirinktinį pranešimą.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Siųsti būsimo laiko išjungimo informaciją savo bendradarbiams

Įdiegę „Human Resources” programėlę, pritaikytą „Teams”, galite lengvai siųsti informaciją apie savo būsimą ne darbo laiką savo bendradarbiams skiltyje „Komandos” arba „Pokalbiai”.

1. „Komandos” arba „Pokalbiai” skiltyje, esančiose programėlėje „Teams”, pasirinkite „Human Resources” mygtuką, esantį po pokalbio langu.

   ![„Human Resources” mygtukas, esantis po pokalbio langu.](./media/hr-teams-leave-app-chat-button.png)

2. Pasirinkite atostogų užklausą, kurią norite bendrinti. Jei norite bendrinti juodraštinę atostogų užklausą, pirmiausia pasirinkite **Juodraščiai**.

Jūsų atostogų užklausa bus rodoma pokalbiuose.

Jei bendrinote juodraštinę užklausą, ji bus rodoma kaip juodraštis.

## <a name="view-your-teams-leave-calendar"></a>Peržiūrėti komandos atostogų kalendorių

Jeigu esate vadovas, valdantis tiesiogines ataskaitas, galite peržiūrėti jūsų komandos patvirtintą ir laukiamą ne darbo laiką.

1. „Human Resources“ programoje „Teams“ pasirinkite **Ne darbo laikas**.

2. Pasirinkite **Komandos kalendorius**. Kalendorius rodo jūsų tiesioginių ataskaitų patvirtintą ir laukiamą ne darbo laiką.

   > [!NOTE]
   > Jei nematote komandos kalendoriaus, paprašykite savo administratoriaus, kad jį įjungtų Daugiau informacijos žr. skyriuje [Diegimas ir sąranka](hr-admin-teams-leave-app.md#install-and-setup).

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
| tr-TR | Turkijos (Vzrkiye) |
| zh-CN | Kinų (supaprastintoji) |

## <a name="troubleshooting"></a>Trikčių šalinimas

Jei kyla problemų prisijungiant arba naudojant „Dynamics 365 Human Resources“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis. Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą. Norėdami gauti daugiau informacijos, [Gauti pagalbos](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nepavyksta prisijungti prie „Teams“ programos „Human Resources“

Jei negalite prisijungti prie programos, gali būti, kad paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, nėra susieta su darbuotojo įrašu „Dynamics 365 Human Resources“. Kreipkitės į sistemos administratorių, kad įsitikintumėte, kad jūsų darbuotojo įrašas yra tinkamai susietas.

### <a name="cant-find-the-dynamics-365-human-resources-environment-in-settings"></a>Parametruose aplinkos Dynamics 365 Human Resources rasti negalima

Jei negalite pasirinkti tinkamos „Dynamics 365” aplinkos, vartotojo įrašas galėjo būti netinkamai sinchronizuotas. Kreipkitės į sistemos administratorių tam, kad iš naujo sukurtumėte vartotojo įrašą ir susietumėte jį su vartotojo kredencialais. Tada po kelių minučių pabandykite prisijungti prie „Microsoft Teams” personalo programos.

### <a name="translations-dont-display-correctly"></a>Vertimai rodomi neteisingai

Jei vertimai nerodomi taip, kaip turėtų, patikrinkite, ar kalba, kurią pasirinkote komandose, sutampa su kalba, kurią pasirinkote personalo skiltyje **Naudotojo parinktys**.

Komandose peržiūrėkite **Programos kalba**, dalyje **Nustatymai**.

![Komandų nustatymai.](./media/hr-teams-leave-app-settings.png)

Personalo dalyje pasirinkite **Nustatymai**, o tada pasirinkite **Naudotojo parinktys**. Patikrinkite, ar laukelis **Kalba** sutampa su komandų laukeliu **Programos kalba**.

![Personalo naudotojo parinktys.](./media/hr-teams-leave-app-user-options.png)

Jei vis dar kyla problemų dėl vertimo, praneškite mums. Daugiau informacijos ieškokite finansų [ir operacijų programėlių arba vykdymo ciklo tarnybų (LCS) palaikyme](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“

Jei gaunate klaidą, kai bandote patvirtinti atostogų užklausas „Teams“ programoje, pabandykite tolesnius trikčių šalinimo žingsnius:

1. Patikrinkite, ar paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, yra ta pati, kurią naudojate prieigai prie „Dynamics 365 Human Resources“.

2. Patikrinkite, ar jus galite patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus. Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Palikti tvirtintojams negauus pokalbių su „Teams“ pranešimais atostogų užklausoms patvirtinti

1. Užtikrinkite, kad aplinkos ir vartotojo pranešimai yra įgalinti. Dėl daugiau informacijos, žiūrėkite [Įjungti „Human Resources“ programos pranešimus „Teams“](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ir [Įjungti „Teams“ pranešimus ir juos išjungti atskiriems vartotojams](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Įsitikinkite, kad vartotojai yra prisiregistravę pokalbių skirtuke naudodami tą **pačią** prisijungimo informaciją, kuriuos jie naudoja atostogų užklausoms patvirtinti. Norėdami prisijungti naudodami tinkamą prisjungimo informaciją, naudokite pranešimus „atsijungti" ir „prisijungti".

3. Jei problema išlieka, patikrinkite verslo įvykių sistemos paketinės **užduoties** būseną kaip sistemos administratorių. Jei jis yra laukimo arba **vykdymo**  **etape**, po kelių minučių patikrinkite dar kartą. Jei būsena nekinta, užregistruokite palaikymo kvitą, kad mūsų komanda galėtų padėti išspręsti problemą.

## <a name="known-accessibility-issues"></a>Sužinokite prieinamumo problemas

Žmogiškųjų išteklių programa „Teams“ turi tolesnes prieinamumo problemas, dėl kurių dirbame siekdami sutaisyti ateities versijose.

| Išdavimas | Apėjimas ir paaiškinimas |
| --- | --- |
| Priartinimas iki 400% darbastalyje paslepia kai kuriuos mygtukų veiksmus iš rodinio. | Rekomenduojame naudoti didinamąjį stiklą, kol palaikysime šį priartinimo lygį. |
| Skirtuke **Laiko išjungimas** naudojant mygtuko perrašo veiksmą, o jis skaito išjungimo tinklelio antraštę. | Antraštė ir elementai tinklelyje yra sugrupuoti pagal metus ir sutraukiami. Interpretuoja šį pristatymą kaip veiksmų elementą, bet tai nėra. |
| Skirtuke **Nebuvimas** yra papildomas paslinkimo gestas naršant į **Priežasties kodą** naujame prašyme. | Nėra jokio paslėpto valdiklio, kurį bando gauti paslinkimo naršymas. |
| Skirtuke **Nebuvimas** jums paslinkus, kai yra atidarytas kalendorius, baigsite ne valdiklyje, o naujos užklausos viršuje arba redaguodami užklausą. | Jums pasiekus **Eiti šiandien**, pagalvokite apie valdiklio pabaigą ir paslinkite atgaline kryptimi, kad grįžtumėte į viršų. |
| Skirtuke **Pokalbis** koncentravimasis nušoka atgal į viršų jums įvedant datą ir naudojant padedantį įrankį ar klaviatūros naršymą. | Naudokite skirtuką, kol pasieksite savo įvesties sritį dar kartą. |

## <a name="privacy-notice"></a>Privatumo pranešimas

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>„Microsoft Language Understanding Intelligent Service” (LUIS)

Naudojant robotą Dynamics 365 Human Resources  Microsoft Teams, vartotojo teksto įvesties duomenys analizuojami siekiant suprasti užklausos ar užklausos priežastį. Vartotojo įvestis, pvz., "Ieškoti sąskaitos "Contoso", nukreipiama į vieną iš Microsoft smanmanų paslaugų, vadinamos "Intelligent Service" (INTEL). Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/). LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra). Tada ši informacija perduodama į "Microsoft [Azure Bot](https://azure.microsoft.com/services/bot-service/)" sistemą, Dynamics 365 Human Resources kuri sąveikauja su duomenimis ir nuskaito norimą vartotojo užklausos informaciją. 

Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure bot framework“ apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi. LUIS tarnyba ir „Azure bot framework“ gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“. Kadangi JŪSŲ tarnyba turi prieigą tik prie vartotojo užklausų ir ji nėra sukurta taip, kad būtų prijungta prie vartotojo duomenų ar sąskaitos, Dynamics 365 Human Resources tiekėjo vartotojas gali per daug įvesti užklausą, kurioje yra Kliento duomenys, Asmeniniai duomenys ar kiti duomenys ir toks užklausos turinys gali būti siunčiamas Dynamics 365 Human Resources į JŪSŲ APTARNAVIMą IR "Azure bot" sistemą. 

Vartotojo užklausų ir pranešimų turinys YRA užkoduojamas IR ne daugiau kaip 30 dienų PAGAL DNS sistemą, šifruojamas ir nėra naudojamas mokymas ar paslaugai tobulinti. Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”

Kai naudojate programą Dynamics 365 Human Resources , tam Microsoft Teams tikri kliento duomenys gali būti siunčiami už geografinės regiono, kuriame įdiegta jūsų nuomininko personalo tarnyba, ribų.

Dynamics 365 Human Resources perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į įvykių Microsoft Azure tinklelį ir Microsoft Teams. Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”. Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui. Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Taip pat žiūrėkite

[„Microsoft Teams“ atsisiuntimas ir diegimas](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[„Microsoft Teams“ pagalbos centras](https://support.office.com/teams)</br>
[„Human Resources“ programa „Teams“](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

