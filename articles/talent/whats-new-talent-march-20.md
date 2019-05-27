---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. kovo 20 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d69294b64c841c5486d694b129cf6c0f26fd93fd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518662"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-20-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. kovo 20 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="setting-the-audience-on-activities"></a>Veiklų auditorijos nustatymas
Dabar galima nustatyti sistemos veiklų auditoriją. Galima nustatyti šias su procesais susijusių veiklų (pvz., pokalbio, grafiko, atsiliepimo ir EEO) parinktis: Visi kandidatai, Vidiniai kandidatai ir Išoriniai kandidatai. Pasirinktinės veiklos, pvz., „Microsoft Forms“, „YouTube“ vaizdo įrašai ir žiniatinklio turinį galima teikti visiems kandidatams, vidiniams kandidatams, išoriniams kandidatams arba samdos komandai.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Karjeros svetainės užduočių suradimo padidinimas: ieškos mechanizmo optimizavimas
Ši funkcija suteikia galimybę duomenų šliaužikliams pasiekti ir indeksuoti darbo skelbimus „Attract“ karjeros svetainėje. Tai padeda kandidatams rasti darbus, užregistruotus „Attract“ karjeros svetainėje, naudojant populiariausius ieškos mechanizmus.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Prisijungimo užuominos rodymas kandidatams, kurie pamiršo savo kredencialus
Jei kandidatas pamiršo socialinių tinklų kredencialus, kuriuos naudodamas pateikė prašymą dėl darbo, kai atidarė įrašytą arba el. paštu jiems atsiųstą saitą, dabar jam bus rodoma užuomina, kurioje pateikiami teikėjo pavadinimas ir vartotojo vardas (neskaidrūs). Tokiu atveju vairuotojui padedama pasirinkti tinkamus kredencialus darbo prašymui pasiekti.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Pagalba vidiniams kandidatams naršant vidinius darbus
Pašalinta problema, dėl kurios išoriniai kandidatai galėjo matyti darbo samdos vadovo vardą ir pavardę. Dabar tik vidiniai kandidatai gali matyti darbo samdos komandos narius. Be to, dabar vidiniams kandidatams lengviau peržiūrėti ir teikti prašymus tik dėl vidinių darbų. Kai kandidatas bando pasiekti saitą, kad peržiūrėtų arba teiktų prašymą tik dėl vidinio darbo, jis turi autentifikuoti naudodamas „Azure Active Directory“ kredencialus. Vidiniai kandidatai taip pat gali susisiekti samdos komandos nariu ir išreikšti susidomėjimą arba sužinoti daugiau apie darbą. Ši funkcija teikiama tik vidiniams kandidatams, pretenduojantiems į bet kurį darbą. Daugiau informacijos žr. [Karjeros svetainės funkcija sprendime „Attract“](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Sidabro medalių laimėtojų nustatymas siekiant ateityje į pareigas paskirti vertingiausius pretendentus
Įdarbintojai ir samdos vadovai dažnai naudoja sąrašą, kurį sudaro pretendentai, kurie tiko eiti pareigas, bet nepavyko jiems pateikti pasiūlymo, nes darbo vieta jau buvo užimta. Tokie pretendentai, vadinami sidabro medalių laimėtojais, yra naudingi, nes jie gali padėti sutaupyti laiko samdant kandidatus į atsilaisvinusias panašias pareigas. Dabar „Attract“ suteikia galimybę įdarbintojams ir samdos vadybininkams nurodyti sidabro medalių laimėtojus pretendentų sąraše, jei pretendentas pasiekė etapą Pasiūlymas. Sidabro medalio laimėtojo nurodymas bus matomas darbo pretendentų sąraše, taip pat – talentų telkinio rodinyje, kai pretendentai yra priklauso bet kuriam įdarbintojo arba samdos vadovo telkiniui. Be to, paskyrimas bus rodomas darbų retrospektyvoje kaip kandidato talentų telkinio profilio dalis. Šią funkciją galite peržiūrėti, jei paprašysite administratoriaus ją įjungti naudojant [Administratorių centro funkcijų valdymas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Pretendentų įtraukimas į talentų telkinius
Dabar lengviau įtraukti pretendentus į talentų telkinius pateikiant naują veiksmą pretendentų sąraše. Pasirinkdamas piktogramą **Įtraukti į talentų telkinį**, įdarbintojas arba samdos vadovas gali rinktis iš savo talentų telkinių ir lengvai įtraukti pretendentų į talentų telkinius iš paties darbo pretendentų sąrašo.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Konfigūravimas, ar reikalingas gyvenimo aprašymas norint teikti prašymą dėl tam tikros darbo vietos
Atsižvelgiant į klientų atsiliepimus, įdarbintojai dabar gali konfigūruoti, ar teikiant paraišką dėl konkretaus darbo reikalingas darbo aprašymas (formoje arba kaip įkeltas failas). Ši konfigūracija priklauso prašymo veiklai, kuri pasiekiama samdos procese. Ją įjungus, kiekvienas potencialus pretendentas bus paragintas nusiųsti gyvenimo aprašymą, kai teiks prašymą dėl šių pareigų. Prašymas nebus laikomas išsamiu, jei gyvenimo aprašymas nebus nusiųstas. Tai padeda sumažinti nereikalingą informaciją pretendentų telkinyje užtikrinant, kad kiekvienas pretendentas pateiks pakankamai informacijos ir įdarbintojas galės jį kategorizuoti.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidatai gali teikti prašymą dėl darbo naudodami savo „LinkedIn“ profilį
Kandidatai, kurių profiliai jau atnaujinti platformoje „LinkedIn“, gali teikti prašymus dėl darbo vienu spustelėjimu tame profilyje.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Sekimas, kaip kandidato profilis yra kilęs iš sistemos ir kur jūsų pretendentai randa darbus, dėl kurių jie teikia prašymus
Dabar galite sužinoti, kaip tam tikro kandidato profilis yra kilęs iš „Attract“, peržiūrėję profilio šaltinį kandidato informacijoje pretendento puslapyje **Profilis** arba talentų telkinio profilyje. Taip pat galite sužinoti, kaip bet kuris pretendentas atrado darbą, peržiūrėję prašymo šaltinį, pateiktą prašymo veiklos sklaidos kanale **Programos veikla**. Ši informacija taip pat teikiama darbo retrospektyvoje talentų telkinio profilyje. Kai įdarbintojai arba samdos vadovai įtraukia kandidatus neautomatiškai, jie taip pat bus paraginti nurodyti prašymo šaltinį arba kandidato profilį. Kai kandidatas teikia prašymą pirmą kartą, jų profilio šaltinis bus toks pat kaip jų prašymo originalas. Šią funkciją galite peržiūrėti, jei paprašysite administratoriaus ją įjungti naudojant [Administratorių centro funkcijų valdymas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature). Atminkite, kad esami kandidatai ir pretendentai neturės prieigos prie jokios šaltinio informacijos. Tačiau įdarbintojai gali įtraukti šią informaciją neautomatiniu būdu.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime įtraukti smulkūs klaidų ištaisymai, skirti „Dynamics 365 Talent: Onboard“

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2195 komponavimo versijai

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>„Attract“ integravimas sukelia įrašų dublikatų klaidą pasirinkus Pretendentai
Šiame naujinyje pašalinta įrašų dublikatų klaida. Ši problema kyla atidarant darbo sritį **Personalo valdymas**.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Nepavyksta uždaryti formos redaguojant vardų seką
Atlikti pakeitimai ir pašalinta problema, kuri kildavo redaguojant vardų seką darbininko formoje.

## <a name="coming-soon"></a>Jau greitai

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Išplėstinės kompensacijos sauga (fiksuota ir kintama)
Daugelyje organizacijų kompensacijų ir išmokų vadovai gali turėti prieigą tik prie konkrečių kompensacijų įrašų. Šie įrašai gali būti skirti vadovams arba regionų darbuotojams. Atlikus šį pakeitimą, personalo skyrius gali valdyti ir tvarkyti kompensacijų planus, skirtus skirtingoms darbuotojų grupėms jūsų organizacijoje. Fiksuotam ir kintamam planams galima priskirti saugos vaidmenis – tokiu būdu nustatysite prieigą prie planų ir darbuotojų duomenų, susijusių su planais, pvz., pajamų arba premijų įrašai. Tik asmenys, kuriems priskirti reikiami vaidmenys, galės apdoroti tų darbuotojų kompensaciją.

###  <a name="email-support-for-alerts"></a>Įspėjimų el. pašto palaikymas
24 platformos naujinį įdiegę vartotojai gali kurti įspėjimo taisykles, kurios automatiškai išsiunčia el. pašto pranešimus kontaktams, kai jas suaktyvina įvykis.

### <a name="duplicate-employee-check-interface-changes"></a>Darbuotojų dublikatų patikra: sąsajos pakeitimai
Atlikus šį pakeitimą dublikatai aptinkami, kai įvedate laukų pavadinimus, o būsena rodo, kiek dublikatų rasta. Galite pasirinkti pateiktą nuorodą, kad atidarytumėte naują puslapį ir įvertintumėte, ar naudoti aptiktą dublikatą. Dublikatų forma nėra atidaroma automatiškai, kad nebūtų trukdoma įvesti duomenis.


