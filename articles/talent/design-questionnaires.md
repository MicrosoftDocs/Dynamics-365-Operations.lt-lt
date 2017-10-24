---
title: Klausimyno sudarymas
description: "Šioje temoje aprašomas klausimyno kūrimo procesas. Pirmasis veiksmas yra sukurti klausimyno dizainą. Kai kuriate klausimyno dizainą, ne tik rašote klausimus ir atsakymus, tačiau taip pat sukuriate struktūrą, kuri leidžia atsakymus įrašyti ir tabuliuoti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 65720297b43af49d8c8382ee2e3dde903d05ed14
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="design-a-questionnaire"></a>Klausimyno sudarymas

Šioje temoje aprašomas klausimyno kūrimo procesas. Pirmasis veiksmas yra sukurti klausimyno dizainą. Kai kuriate klausimyno dizainą, ne tik rašote klausimus ir atsakymus, tačiau taip pat sukuriate struktūrą, kuri leidžia atsakymus įrašyti ir tabuliuoti. 

Kruopščiai sudarytas klausimynas gali padėti padidinti surenkamų duomenų kokybę. Kruopščiai sudarydami klausimyną, galite geriau tinkamu laiku parinkti tinkamas klausimyno parinktis. Tolesni punktai gali padėti suplanuoti efektyvų klausimyną.

-   Aiškiai apibrėžkite klausimyno paskirtį, kad užtikrintumėte, jog klausimai atitinka paskirtį.
-   Nustatykite atskirą asmenį arba asmenų grupę, kurie turėtų pildyti klausimyną.
-   Užrašykite klausimus, kurie bus rodomi klausimyne, ir, jei taikytina, pateikite atsakymų pasirinkimus.
-   Įsitikinkite, kad klausimyno tėkmė logiška, kad respondentai liktų įsitraukę.
-   Klausimus ir atsakymus išdėstykite tokia tvarka, kuria jie turėtų būti pateikti respondentams.
-   Jei reikia, nuspręskite, kaip reikėtų vertinti rezultatus.
-   Nuspręskite, ar jums reikės papildomų funkcijų. Pvz., nustatykite, ar ir kaip turėtų būti kategorizuojami rezultatai, ar reikalingas laiko limitas ir ar visi klausimai bus privalomi.

Dizaino etapas apima keturias kategorijas užduočių, kurias turite atlikti tolesne tvarka.

1.  Pagal poreikį nustatykite būtinąsias sąlygas.
2.  Jei reikia, nustatykite atsakymų grupes ir atsakymus.
3.  Nustatykite klausimus ir jų susiejimą su atsakymų grupėmis.
4.  Nustatykite patį klausimyną ir prie jo pridėkite klausimų.

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš kuriant klausimynus, atsakymus ir klausimus, turi būti nustatytos kai kurios būtinosios sąlygos. Tačiau, norint naudoti visas funkcijas, visų būtinųjų salygų nereikia.

### <a name="required"></a>Būtina

| Būtinoji sąlyga        | Prekės/Paslaugos pavadinimas                |
|---------------------|----------------------------|
| Klausimynų tipai | Kategorizuokite klausimynus. |
| Klausimų tipai      | Kategorizuokite klausimus.      |

### <a name="optional"></a>Pasirinktinis

| Būtinoji sąlyga             | Prekės/Paslaugos pavadinimas                                                    |
|--------------------------|----------------------------------------------------------------|
| Klausimynų parametrai | Modifikuokite pagrindinius klausimynų valdiklius ir numatytąsias nuostatas. |

### <a name="questionnaire-types"></a>Klausimynų tipai

Kuriant klausimyną reikia priskirti jo tipą. Klausimynų tipai padeda juos lengviau valdyti ir klasifikuoti. Klausimynų tipus naudokite jiems klasifikuoti ir atskirti vienam nuo kito. Pavyzdžiui, jei yra keli klausimynai, iš kurių galima rinktis, kad būtų lengviau rasti konkretų klausimyną, galite juos filtruoti pagal tipą. Toliau pateikiami keli klausimynų tipų pavyzdžiai.

-   Personalo lavinimas
-   Klientų apklausos
-   Peržiūros procesas

### <a name="question-types"></a>Klausimų tipai

Kuriant klasuimą reikia priskirti jo tipą. 

Klausimų tipus naudokite norėdami skirstyti klausimus į kategorijas, naudojamas ataskaitoms kurti. Naudojant klausimų tipus, taip pat lengviau rasti klausimus, nes **Klausimų** puslapyje tipus galite naudoti kaip filtrus. Toliau pateikiami keli klausimų tipų pavyzdžiai.

-   Žmogiškieji ištekliai.
-   Verslo valdymas.
-   Kursų vertinimas.

### <a name="questionnaire-parameters"></a>Klausimynų parametrai

Klausimynų parametrų nėra privalomi. Galite jų ir naudoti – tai priklauso nuo jūsų įmonės poreikių. 

Klausimynų parametrai apibrėžia klausimyno anonimiškumą, numeracijos kodus ir nuorodos tipus. Kai organizacija platina klausimyną, gali tekti atsižvelgti į parinktį respondentams leisti likti anonimiškiems. 

Numeracijos kodai naudojami tvarkyti klausimams ir atsakymams. Pagal šiuos numeracijos kodus elementams automatiškai priskiriamos reikšmės. 

Prieš pradėdami kurti savo duomenis, turėtumėte apibrėžti visus parametrus. Klausimyno parametrų nuostatas modifikuoti galite bet kuriuo metu.

## <a name="questionnaire-components"></a>Klausimynų komponentai
Klausimynus sudaro trys pagrindiniai elementai: atsakymų grupės, kuriose pateikiami atsakymai į klausimus su keliais pasirinkimas, klausimai ir pats klausimynas. Neprivaloma: klausimyno klausimus galite grupuoti į rezultatų grupes. Rezultatų grupės leidžia kategorizuoti klausimus ir pateikti išsamesnę klausimyno analizę. 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Atsakymų grupės ir atsakymai

Respondentai į klausimą gali atsakyti dvejopai; tai priklauso nuo klausimo temos.

-   Į atvirus klausimus konkrečiu formatu atsakyti nebūtina. Respondentai atsakymą surinkti gali kaip tekstą, skaičių, datą ar laiką. Užduodant tokius klausimus paprastai reikalaujama, kad respondentai atsakydami pateiktų subjektyvią informaciją, pvz., savo nuomonę, apibūdinimą, įvertinimą ar apskaičiavimą.
-   Į uždarus klausimus respondentas turi atsakyti pasirinkdamas atsakymą iš galimų teisingų atsakymų sąrašo.

Kurti galimų atsakymų į uždarus klausimus sąrašą galite **Atsakymų grupių** puslapyje. 

Atsakymų grupės ir atsakymai yra komponentai, kurie sudaro informacijos pagrindą, iš kurio kuriami klausimai. Sukūrę atsakymų grupę, **Klausimų** puslapio lauke **Atsakymų grupė** ją galite susieti su klausimu. 

Atsakymų grupė gali būti naudojama daugiau nei vienam to paties klausimyno klausimui ir taip pat gali būt naudojama daugiau nei viename klausimyne. 

**Pastaba.** Jei atsakymo tekstą modifikuojate atsakymų grupėse, kurios jau panaudotos užpildytuose klausimynuose, gali tapti sunku įvertinti duomenis, o klausimyno rezultatai gali nebegalioti. Jei reikia pakeisti atsakymų grupę, pagalvokite, ar ne geriau, užuot keičiant esamą atsakymų grupę, sukurti naują. Atsakymų grupių, pridėtų prie klausimo ar atsakymo, arba atsakytų atsakymų grupių naikinti negalima.

### <a name="questions"></a>Klausimai

Klausimyne turi būti klausimų. Klausimai gali būti atviri arba uždari.

-   Atsakymai į atvirus klausimus nėra kontroliuojami, ir respondentai gali surinkti savo atsakymus.
-   Uždariems klausimams reikalingas iš anksto apibrėžtų atsakymų parinkčių sąrašas, ir klausimus galima sukurti taip, kad respondentas galėtų pasirinkti kelis atsakymus. Klausimai turėtų būti sudaryti taip, kad iš respondento išgautų konkrečią informaciją ir juos reikia susieti su atsakymų grupe, kurioje pateikiamos kiekvieno uždaro klausimo atsakymų parinktys. 
     -  **Pastaba.** Prieš nustatydami uždarus klausimus, turite sukurti atsakymų grupes ir atsakymus.

Klausimai gali būti išdėstyti sąlyginių klausimų hierarchija, kad antriniai klausimai priklausytų nuo atsakymo, kurį respondentas pasirenka į ankstesnį klausimą. Pirmiausia galite parašyti klausimus, o juos išdėstyti į hierarchiją vėliau.

## <a name="setting-up-questionnaires"></a>Klausimynų nustatymas
**Pastaba.** Prieš nustatydami klausimyną, turite nustatyti atsakymus, klausimus ir būtinąsias sąlygas. 

Kiekvienam klausimynui galite nurodyti tolesnę informaciją.

-   Bendrą laiką arba laiko ribą, skirtą atsakyti į privalomus klausimus.
-   Ar visi klausimai privalomi.
-   Ar klausimyne skaičiuoti taškus.
-   Kaip kategorizuoti rezultatus.
-   Ar klausimynas bus prieinamas tik ribotam respondentų skaičiui.
-   Ar kaip kiekvieno klausimyno puslapio fonas turėtų būti rodomas formos šablonas.
-   Ar, siekiant respondentams paaiškinti klausimyno tikslą, reikalingos papildomos pastabos.
-   Ar klausimus rodyti fiksuota tvarka, ar juos atsitiktinai pasirinkti iš telkinio.
-   Ar klausimai bus užduoti tik jei į ankstesnius klausimus pateikiami konkretus atsakymai.

### <a name="set-up-a-questionnaire"></a>Nustatyti klausimyną

Pagrindinis puslapis, naudojamas nustatyti klausimynui, yra **Klausimynų** puslapis. Norėdami nustatyti klausimyną, nurodyta tvarka atlikite tolesnes užduotis.

1.  Sukurkite klausimyną.
2.  Norėdami į klausimyną pridėti klausimų, atlikite vieną iš tolesnių veiksmų.
    -   Jei naudojate rezultatų grupes, pridėti klausimų į klausimyną galite naudodami jas. Pirmiausia nustatykite klausimyno rezultatų grupes ir tada į jas pridėkite klausimų.
    -   Jei rezultatų grupių nenaudojate, klausimus galite pridėti tiesiai į klausimyną.

3.  Jei reikia sąlyginių klausimų hierarchijos, ją nustatykite.
4.  Išbandykite klausimyną.

Norėdami išbandyti, ar klausimynas tinkamai sudarytas, puslapyje **Klausimynai** spustelėkite **Tikrinti**. Tačiau taip pat yra naudinga prieš klausimyną platinant, jį užpildyti ir išbandyti patiems.

### <a name="modify-a-questionnaire"></a>Modifikuoti klausimyną

Tolesnes užduotis galite atlikti **Klausimynų** puslapyje.

-   Modifikuoti klausimyno informaciją, pvz., rezultatų grupes ir klausimus.
-   Naikinti ir pridėti klausimų.
-   Keisti rezultatų grupes ir sekos numerį. 

**Perspėjimas.** Būkite atsargūs keisdami jau atsakytus klausimynus. Keitimai gali sumažinti statistikos tikslumą, o tai gali būti prasto įvertinimo pagrindas. Užuot keitę jau atsakytą klausimą, apsvarstykite galimybę sukurti naują.

Klausimyne negalite panaikinti tolesnių klausimų tipų.

-   Klausimai, pridėti prie klausimyno
-   Klausimai, į kuriuos jau atsakyta, ir kurie todėl rodomi **Atsakymų** dialogo lange.

### <a name="result-groups"></a>Rezultatų grupės

Į klausimyną pridedant klausimų, rezultatų grupės nėra privalomos. 

Rezultatų grupė naudojama skaičiuoti klausimyno taškams ir kategorizuoti jo rezultatams. Jei naudojate rezultatų grupės, galite atlikti tolesnes užduotis.

-   Remiantis taškų statistika įvertinti klausimyno rezultatus.
-   Įvertinti kiekvienos nustatytos rezultatų grupės respondento rezultatą.
-   Generuoti kiekvienos rezultatų grupės statistiką, kuri padeda analizuoti rezultatus.
-   Spausdinti ataskaitą, kurioje rodomi kiekvienos rezultatų grupės rezultatai ir pasirinktiniai taškai / tekstai, paremti taškais, gaunamais kiekvienoje rezultatų grupėje.

**Pastaba.** Prieš nustatydami rezultatų grupes, turite atlikti tolesnes užduotis.

-   Nustatyti uždarus klausimus. Uždarų klausimų įvesties tipas **Klausimų** puslapyje turi būti **Žymės langelis**, **Alternatyvus mygtukas** arba **Pasirinktinio įvedimo laukas**.
-   Apibrėžti kiekvienam klausimui priskirtų atsakymų grupių atsakymų taškus.
-   Nustatyti klausimyną.

Norėdami į klausimyną pridėti klausimų naudojant rezultatų grupes, pirmiausia nustatykite klausimyno rezultatų grupes ir tada į jas pridėkite klausimų. Jei rezultatų grupių nenaudojate, klausimų pridėti galite tiesiai į klausimyną. 

Galite nustatyti kelias rezultatų grupes, kad įvertintumėte taškus, kuriuos respondentas gauna kiekvienoje kategorijoje. Kai klausimynas baigtas, galite peržiūrėti surinktus kiekvienos rezultatų grupės taškus. 

**Patarimas.** Norėdami klausimyną įvertinti naudojant taškus, bet ne atskiras kategorijas, visus klausimus galite pridėti į vieną rezultatų grupę. 

Kiekvienai rezultatų grupei taip pat galite nustatyti vieną ar kelis taškais paremtus pranešimus, kuriuos užpildę klausimyną gauna respondentai. Rodomas tekstas gali skirtis – tai priklauso nuo rezultatų grupės rezultato, kurį respondentas pasiekia. Norėdami naudoti taškais paremtus pranešimus, turite apibrėžti taškų intervalus ir kiekvieno intervalo aprašą. Kai respondentas pasiekia rezultatų konkrečiame intervale, to intervalo tekstas yra įtraukiamas rezultatų ataskaitoje. 

Kadangi rezultatų grupė yra susijusi su taškais, susietais su konkrečiais klausimyno klausimų rinkiniais, klausimyne galite naudoti tik konkrečią rezultatų grupę.

#### <a name="example-pointstexts-for-result-group-3"></a>Pavyzdys: 3 rezultatų grupės taškai / tekstai

Naudojate lyderystei tikrinti skirtą klausimyną, kuriame 3 kategorijose yra 15 klausimų. Sukuriate tris rezultatų grupes ir į kiekvieną grupę pridedate penkis klausimus. Tada tose trijose grupėse sumuojami taškai. Šios trys rezultatų grupės nurodytos toliau.

-   Kūrybiniai gebėjimai
-   Vadovavimo gebėjimai
-   Techniniai gebėjimai

Norint naudoti taškais paremtus pranešimus, nustatomi kiekvienos rezultatų grupės teksto intervalai. Kiekvienam klausimui priskiriami du taškai. Todėl maksimali kiekvienos rezultatų grupės taškų suma yra 10. 

Toliau pateikiamoje lentelėje rodomi taškais paremti pranešimai, apibrėžiami „lyderystės gebėjimų‟ rezultatų grupei.

| Taškų intervalas | Tekstas                                       |
|----------------|--------------------------------------------|
| Nuo 1 iki 3         | Jūsų lyderystės gebėjimai vidutiniai.     |
| Nuo 4 iki 7         | Jūsų lyderystės gebėjimai geri.        |
| Nuo 8 iki 10        | Jūsų lyderystės gebėjimai puikūs. |

Galite nustatyti kiekvienos klausimyno rezultatų grupės taškų intervalus ir tekstus. Rodomi kiekvienos rezultatų grupės tekstai, atitinkantys kiekvieno respondento rezultatą. 

**Pastaba.** Intervalus ir tekstus galite keisti. Tačiau, jei klausimynas baigtas, pakeitimai gali sukelti skirtumų tarp ankstesnių ir naujų rezultatų ataskaitų.

### <a name="conditional-question-hierarchies"></a>Sąlyginių klausimų hierarchijos

Nustatant klausimyną, sąlyginių klausimų hierarchijos nėra privalomos. 

**Pastaba.** Prieš nustatydami sąlyginių klausimų hierarchiją, į klausimyną turite pridėti klausimų, kuriems priskirtos atsakymų grupės. 

Norėdami naudoti sąlyginius klausimus sukurti klausimyno klausimų hierarchijai, galite nustatyti, kad seka, kuria pateikiami klausimai, priklausytų nuo atsakymo, kurį respondentas pasirenka kiekviename klausime. Klausimų seką grįsdami respondento atsakymu, klausimyną galite modifikuoti respondentui jį pildant.

#### <a name="examples"></a>Pavyzdžiai

Juridinis subjektas savo klientams siūlo tiek prekes, tiek paslaugas. Kaip paprastai būna tokiais atvejais, kai kurie klientai perka tik prekes, kai kurie perka tik paslaugas, o kai kurie perka ir prekes, ir paslaugas. Todėl, kai juridinis subjektas išplatina klientų pasitenkinimo apklausą, klausimynui jis pritaiko sąlyginę struktūrą, kad klientams, perkantiems tik paslaugas, nereikėtų atsakinėti į klausimus apie prekes. 

Arba klausimyną galite nustatyti taip, kad, jei 1 klausime respondentas pasirenka atsakymą A, klausimų sekoje kitas būtų 2 klausimas. Tačiau, jei 1 klausime respondentas pasirenka atsakymą B, kitas yra 5 klausimas.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Klausimynų naudojimas](questionnaires.md)

[Klausimynų platinimas ir pildymas](distribute-questionnaires.md)

[Klausimyno rezultatų peržiūra ir vertinimas](evaluate-questionnaire-results.md)


