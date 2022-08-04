---
title: Elektroninių ataskaitų (ER) apžvalga
description: Šiame straipsnyje pateikiama elektroninės ataskaitos įrankio apžvalga. Aprašomos pagrindinės koncepcijos, palaikomi scenarijai ir formatai, kurie yra sprendimo dalis.
author: NickSelin
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f3853e0c1da0a5abb3f92171370cc4aeabbd829
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109587"
---
# <a name="electronic-reporting-er-overview"></a>Elektroninių ataskaitų (ER) apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama elektroninių ataskaitų (ER) įrankio apžvalga. Jame yra informacijos apie pagrindines koncepcijas, ER palaikomus scenarijus ir išvardyti formatai, kurie sukurti ir išleisti kaip sprendimo dalis.

ER yra konfigūruojamas įrankis, padedantis kurti ir prižiūrėti reguliavimo elektronines ataskaitas ir mokėjimus. Jis remiasi šiomis trimis sąvokomis:

- Konfigūracija, o ne kodavimas:

    - Konfigūraciją gali atlikti verslo vartotojas, kuriam nereikia programuotojo.
    - Duomenų modelis apibrėžiamas verslo sąlygose.
    - Vaizdo doroklis naudojamas visiems ER konfigūracijos komponentams kurti.
    - Duomenų transformacijai naudojama kalba yra panaši į kalbą, kuri naudojama Microsoft Excel.

- Viena konfigūracija, skirta keliems "Dynamics 365" finansų paleidimams:

    - Tvarkyti vieną domeno duomenų modelį, apibrėžtą verslo sąlygose.
    - Isolate programos paleidimo informacija nuo paleidimo priklausomų duomenų modelio susiejimuose.
    - Tvarkyti vieną formato konfigūraciją keliems dabartinės versijos leidimams pagal duomenų modelį.

- Paprastas arba automatinis atnaujinimas:

    - Palaikomas ER konfigūracijų versijos kopijavimas.
    - Ciklo Microsoft Dynamics tarnybų (LCS) turto biblioteką galima naudoti kaip ER konfigūracijų saugyklą, kad būtų galima atlikti versijų mainus.
    - Lokalizavimus, paremtus originalia ER konfigūracija, galima įtraukti kaip antines versijas.
    - ER konfigūracijos medis pateikiamas kaip įrankis, padedantis valdyti versijų priklausomybes.
    - Lokalizavimo arba pokyčių konfigūracijos skirtumai įrašomi, kad įgalintumėte automatinį pradinės ER konfigūracijos versijos atnaujinimą.
    - Neautomatiniu būdu lengviau išspręsti konfliktus, aptiktus automatiškai atnaujinus lokalizavimo versijas.

ER leidžia apibrėžti elektroninio formato struktūras, o tada apibrėžti, kaip struktūros turėtų būti užpildytos naudojant duomenis ir algoritmus. Duomenų transformacijai galite naudoti formulės kalbą, panašią į Excel kalbą. Kad duomenų bazę būtų lengviau valdyti, pakartotinai naudoti ir nepriklausomą nuo formato pakeitimų, bus įvesta tarpinė duomenų modelio koncepcija. Ši sąvoka leidžia paslėpti išsamią diegimo informaciją nuo formato susiejimo ir leidžia vienam duomenų modeliui pakartotinai naudoti keliuose formatų susiejimuose.

Galite naudoti ER gaunamų ir siunčiamų elektroninių dokumentų formatams konfigūruoti, atsižvelgiant į įvairių šalių ir regionų teisinius reikalavimus. ER suteikia galimybę valdyti šiuos formatus per jų naudojimo ciklą. Pavyzdžiui, galite pritaikyti naujus teisinius reikalavimus ir generuoti verslo dokumentus reikiamu formatu, skirtu keistis informacija su valdžios institucijomis, bankais ir kitomis šalimis elektroniniu būdu.

ER mechanizmas skirtas verslo vartotojui, o ne kūrėjui. Kadangi galite konfigūruoti formatus, o ne kodą, elektroninių dokumentų formatų kūrimo ir pritaikymo procesas greitesnis ir lengvesnis.

ER šiuo metu palaiko TEXT, XML, JSON, PDF, Microsoft Word, ir Microsoft Excel OPENXML darbalapių formatus.

## <a name="capabilities"></a>Galimybės

ER mechanizmas turi toliau nurodytas galimybes.

- Jis nurodo vieną bendrą įvairių domenų elektroninių ataskaitų įrankį ir pakeičia daugiau nei 20 skirtingų sistemų, kurios kokio nors tipo finansines ir operacijas.
- Jis atskiria ataskaitos formatą nuo dabartinės įdiegtos versijos. Kitaip tariant, formatą galima taikyti skirtingoms versijoms.
- Jis palaiko pasirinktinio formato kūrimą pagal jo pradinę versiją. Jis taip pat apima galimybes automatiškai naujinti tinkintą formatą, kai pradinis formatas pakeičiamas dėl įvestų lokalizavimo / tinkinimo reikalavimų.
- Jis tampa pagrindiniu standartiniu „Microsoft“ ir „Microsoft“ partnerių elektroninių ataskaitų lokalizavimo reikalavimus palaikančiu įrankiu.
- Jis palaiko galimybę paskirstyti formatus partneriams ir klientams naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="key-concepts"></a>Pagrindinės koncepcijos

### <a name="main-data-flow"></a>Pagrindinių duomenų srautas

[![ER pagrindinių duomenų srautas.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="components"></a>Komponentai

Elektroninės ataskaitos (ER) palaiko šiuos komponentų tipus:

- Duomenų modelis
- Modelio susiejimas
- Formatuoti
- Metaduomenys

Daugiau informacijos žr. [Elektroninės ataskaitos komponentai](er-overview-components.md).


#### <a name="component-versioning"></a>Komponento versijos kūrimas

Palaikomas ER komponento versijos kūrimas. Toliau pateikta ER komponentų pakeitimų valdymo darbo eiga.

1. Pradinė sukurta versija pažymima kaip **Juodraštis**. Šią versiją galima redaguoti ir ją galima tikrinti.
2. Versiją **Juodraštis** galima konvertuoti į versiją **Baigta**. Šią versija galima naudoti vietiniuose ataskaitų teikimo procesuose.
3. Versiją **Baigta** galima konvertuoti į versiją **Bendrai naudojama**. Ši versija publikuojama LCS ir ją galima naudoti visuotiniuose ataskaitų teikimo procesuose.
4. Versiją **Bendrai naudojama** galima konvertuoti į versiją **Nebenaudojama**. Tada šią versiją bus galima naikinti.

Kai versijos būsena yra **Baigta** arba **Bendrai naudojama**, galima keistis duomenimis dar kitu būdu. Jei komponento būsena yra viena iš šių, galima atlikti toliau nurodytus veiksmus.

- Komponentą galima išdėstyti eilutėmis XML formatu ir eksportuoti kaip failą XML formatu.
- Komponentą galima sugrąžinti iš XML failo ir importuoti į programą kaip naują ER komponento versiją.

#### <a name="component-date-effectivity"></a>Komponento galiojimo data

ER komponento versijos turi galiojimo datą. Galite nustatyti ER komponento datą **Galioja nuo**, kad nurodytumėte datą, nuo kurios šis komponentas galioja ir jį galima naudoti ataskaitų teikimo procesuose. Programos seanso data naudojama apibrėžti, ar komponentas yra tinkamas vykdyti. Jei konkrečią dieną galioja daugiau nei viena versija, ataskaitų teikimo procesuose naudojama naujausia versija.

#### <a name="component-access"></a>Prieiga prie komponento

Prieiga prie ER formato komponentų priklauso nuo ISO valstybės / regiono kodo parametro. Kai šis pasirinktos formato konfigūracijos versijos parametras nenurodytas, formato komponentą galima pasiekti iš bet kurios įmonės vykdymo metu. Kai šiame parametre yra ISO valstybės / regiono kodai, formatas komponentą galima pasiekti tik iš tų įmonių, kurių pagrindinis adresas nurodytas kaip vienas iš formato komponento ISO valstybės / regiono kodų.

Skirtingos duomenų formato komponento versijos gali turėti skirtingus ISO valstybės / regiono kodų parametrus.

#### <a name="configuration"></a><a name="Configuration"></a>Konfigūravimas

ER konfigūracija yra tam tikro ER komponento ER viršelis. Šis komponentas gali būti duomenų modelio komponentas arba formato komponentas. Konfigūracija gali apimti skirtingas ER komponento versijas. Kiekviena konfigūracija pažymėta kaip priklausanti konkrečiam konfigūracijos teikėjui. Konfigūracijos komponento versiją **Juodraštis** galima redaguoti, jei konfigūracijos savininkas pasirinktas kaip aktyvus teikėjas programos ER parametruose.

Kiekvienoje modelio konfigūracijoje yra duomenų modelio komponentas. Naują formato konfigūraciją galima gauti iš konkrečios duomenų modelio konfigūracijos. Sukurta formato konfigūracija konfigūracijos medyje atrodo kaip antrinė pradinės duomenų modelio konfigūracijos konfigūracija.

Sukurtoje formato konfigūracijoje yra formato komponentas. Pirminės modelio konfigūracijos duomenų modelio komponentas yra automatiškai įterpiamas į antrinės formato konfigūracijos formato komponentą kaip numatytasis duomenų šaltinis.

Programos įmonės bendrai naudoja ER konfigūraciją.

#### <a name="provider"></a><a name="Provider"></a>Teikėjas

ER teikėjas yra šalies identifikatorius, naudojamas kiekvienos ER konfigūracijos autoriui (savininkui) nurodyti. ER suteikia galimybę valdyti konfigūracijos teikėjų sąrašą. Formato konfigūracijos, išleistos elektroniniams dokumentams kaip finansų ir operacijų sprendimo dalis, pažymėtos kaip "Microsoft **" konfigūracijos** teikėjo dalis.

Norėdami sužinoti, kaip registruoti naują ER teikėją, paleiskite užduočių vedlį **ER: konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų / sprendimų komponentų (10677)** dalis).

#### <a name="repository"></a><a name="Repository"></a>Saugykla

ER saugykloje saugomos ER konfigūracijos. Šiuo metu palaikomos šių tipų ER saugyklos: 

- LCS bendrai naudojama biblioteka
- LCS projektas
- Failų sistema
- RCS
- „Operations“ ištekliai
- Visuotinė saugykla

Saugykloje **LCS bendrai naudojama biblioteka** suteikiama prieiga prie „Lifecycle Services“ (LCS) bendrai naudojamo turto bibliotekos konfigūracijų sąrašo. Šio tipo ER saugyklą galima registruoti tik „Microsoft“ teikėjui. Naujausios versijos ER konfigūracijas iš LCS bendrai naudojamo turto bibliotekos galite importuoti į esamą egzempliorių.

**LCS projekto** saugykla suteikia prieigą prie tam tikro LCS projekto (LCS projekto turto bibliotekos), pasirinkto saugyklos registracijos metu, konfigūracijų sąrašo. ER suteikia galimybę nusiųsti bendrai naudojamas konfigūracijas iš dabartinio egzemplioriaus į konkrečią **LCS projekto** saugyklą. Taip pat galite importuoti konfigūracijas iš **LCS projektų** saugyklos į dabartinį jūsų finansų ir operacijų programėlių egzempliorių.

Saugykla **Failų sistema** suteikia prieigą prie konfigūracijų, konkrečiame įrenginio vietinės failų sistemos aplanke, kuriame priglobta AOS tarnyba, esančių kaip XML failai, sąrašo. Reikiamas aplankas pasirenkamas saugyklos registracijos etapo metu. Konfigūracijas iš **Failų sistema** saugyklos galite importuoti į dabartinį egzempliorių. 

Atminkite, kad šio tipo saugykla pasiekiama toliau nurodytose aplinkose.

- Aplinkos diegimo debesyje įrankis, įdiegtas kūrimo tikslais (pateikiami bandomieji pridėtų komplektų modeliai)
- Vietoje įdiegtos aplinkos (vietinės)

Daugiau informacijos žr. [Elektroninių ataskaitų (ER) konfigūracijų importavimas](./electronic-reporting-import-ger-configurations.md).

**RCS** saugykla suteikia prieigą prie tam tikro [konfigūravimo tarnybos (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) egzemplioriaus, pasirinkto saugyklos registracijos etapo metu, konfigūracijų sąrašo. Jei naudojatės ER, užbaigtas arba bendrai naudojamas konfigūracijas iš pasirinkto RCS egzempliorius galėsite importuoti į dabartinį egzempliorių ir naudoti jas elektroninėms ataskaitoms.

Daugiau informacijos žr. [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš RCS](./rcs-download-configurations.md).

**Bendroji saugykla** suteikia prieigą prie [konfigūravimo tarnybos](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) bendrojoje saugykloje esančių konfigūracijų sąrašo. Šio tipo ER saugyklą galima registruoti tik „Microsoft“ teikėjui. Naujausios versijos ER konfigūracijas iš bendrosios saugyklos galite importuoti į esamą egzempliorių.

Daugiau informacijos rasite [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš konfigūravimo tarnybos bendrosios saugyklos](./er-download-configurations-global-repo.md).

Naudojantis saugykla **Operacijų ištekliai** suteikiama prieiga prie konfigūracijų sąrašo, kurį „Microsoft“ kaip ER konfigūracijų teikėjas pirmiausia išleidžia kaip programos sprendimo dalį. Šias konfigūracijas galima importuoti į esamą egzempliorių ir naudoti elektroninėms ataskaitoms kurti arba pavyzdžio užduočių vadovams paleisti. Taip pat jas galima naudoti tolesniam lokalizavimui ir tinkinimui atlikti. Atkreipkite dėmesį į tai, kad importuojant naujausias „Microsoft“ ER konfigūracijose pateiktas versijas iš LCS bendrai naudojamo turto bibliotekos, būtina naudoti atitinkamą ER saugyklą.

Galima registruoti atskirai kiekvieno dabartinio egzemplioriaus konfigūracijos teikėjo būtinas saugyklas **LCS projektas**, **Failų sistema** ir **„Regulatory Configuration Services” (RCS)**. Kiekvieną saugyklą galima priskirti konkrečiam konfigūracijos teikėjui.

## <a name="supported-scenarios"></a>Palaikomi scenarijai

### <a name="building-a-data-model"></a>Duomenų modelio kūrimas

ER teikia modelių kūrimo įrankį, kurį galite naudoti konkrečiam verslo domenui skirtam duomenų modeliui kurti. Visus domenui būdingus verslo objektus ir jų ryšius galima pateikti duomenų modelyje kaip hierarchinę struktūrą. 

Paleiskite užduočių vedlį **ER konkretaus domeno duomenų modelio kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="translating-data-model-content"></a>Duomenų modelio turinio vertimas

Duomenų modelio turinį (etiketes ir aprašus) galima išversti į kitas programų palaikomas kalbas. Duomenų modelio turinį galite norėti išversti dėl toliau nurodytų priežasčių.

- Norint, kad kitomis kalbomis kalbantys formato kūrėjai, kurie naudos duomenų modelį formato komponentų duomenims susieti, kurdami lengviau suprastų turinį.
- Norint turinį padaryti patogesnį naudoti vykdymo metu, teikiant vykdymo parametrų raginimus ir pagalbą bei sukonfigūruotus tikrinimo pranešimus (klaidų, įspėjimų) tuo metu prisijungusio vartotojo pageidaujama kalba.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Siunčiamų dokumentų modelio susiejimų konfigūravimas

ER teikia modelio susiejimų kūrimo įrankį, kurį naudodami vartotojai gali susieti duomenų modelius, kuriuos jie sukūrė konkretiems programos duomenų šaltiniams. Remiantis susiejimu, vykdymo metu į duomenų modelį bus importuojami duomenys iš pasirinktų duomenų šaltinių. Tada duomenų modelis naudojamas kaip ER formatų, kurie generuoja siunčiamus elektroninius dokumentus, abstrakčių duomenų šaltinis. 

Paleiskite užduočių vedlius **ER modelio susiejimo nustatymas ir duomenų šaltinių pasirinkimas** ir **ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Gaunamų dokumentų modelio susiejimų konfigūravimas

ER teikia modelio susiejimų kūrimo įrankį, kurį naudodami vartotojai gali susieti duomenų modelius, kuriuos sukūrė konkrečioms paskirties vietoms. Pavyzdžiui, duomenų modelius galima susieti su naujintinais duomenų komponentais (lentelėmis, duomenų objektais ir rodiniais). Remiantis susiejimu, vykdymo metu bus atnaujinti duomenys, naudojant duomenis iš duomenų modelio. Kaip ER formato abstrakti saugykla duomenų modelis užpildomas iš gaunamo elektroninio dokumento importuotais duomenimis. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Sukurto modelio komponento saugojimas kaip modelio konfigūracijos

ER gali saugoti sukurtą duomenų modelį su susietais duomenų susiejimais kaip dabartinio egzemplioriaus modelio konfigūraciją. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio konfigūracijos pavyzdys (mokėjimo duomenų modelio konfigūracija).

Paleiskite užduočių vedlį **ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Formato kūrimas pasirenkant duomenų modelį kaip pagrindą

ER palaiko formato kūrimo įrankį, kurį galima naudoti norint kurti pasirinkto verslo domeno elektroninio dokumento formatą pasirenkant modelio komponentą kaip pagrindą. Tas pats ER formato kūrimo įrankis teikia galimybę sukurtą formatą susieti su pasirinkto domeno duomenų modelio susiejimu kaip duomenų šaltiniu. 

Paleiskite užduočių vedlį **ER konkretaus domeno formato kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfigūracijos, skirtos elektroninius dokumentus generuoti OPENXML darbalapio formatu, kūrimas

ER formato kūrimo įrankį galima naudoti, norint kurti elektroninį dokumentą OPENXML darbalapio formatu. 

Paleiskite užduočių vedlį **ER konfigūracijos, skirtos generuoti ataskaitas OPENXML formatu, kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi. Vykdydami užduočių vedlio veiksmą, skirtą importuoti šabloną, kaip šabloną naudokite „Excel“ failą [Mokėjimo ataskaitos šablonas (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Konfigūracijos, skirtos elektroninius dokumentus generuoti „Word“ dokumento formatu, kūrimas

ER formato kūrimo įrankį galima naudoti, norint kurti elektroninį dokumentą „Word“ dokumento formatu. Tolesnėje iliustracijoje pateikiamas šio tipo formato pavyzdys. Atkreipkite dėmesį, kad šis formatas pakartotinai naudoja esamą ER konfigūraciją, kuri iš pradžių buvo skirta ataskaitos išvesčiai OPENXML formatu generuoti.

Norėdami išsamiai susipažinti su šiuo scenarijumi, paleiskite užduočių vedlį ER konfigūracijos, skirtos generuoti ataskaitas „Microsoft WORD“ formatu, kūrimas (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų / sprendimų komponentų (10677) dalis). Vykdant užduoties vadovas veiksmo importuoti šabloną, naudokite šiuos Word failus šablonų nustatymas ER formato:

- [Mokėjimo ataskaitos šablonas (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Susietas mokėjimo ataskaitos šablonas (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Konfigūracijos, skirtos importuoti duomenis iš gaunamų elektroninių dokumentų, kūrimas

ER formato kūrimo įrankį galima naudoti norint aprašyti elektroninį dokumentą, kuriam suplanuotas duomenų importavimas XML arba teksto formatu. Sukurta formatas naudojamas išanalizuoti gaunamą dokumentą. ER formato susiejimo kūrimo įrankį galima naudoti norint apibrėžti sukurto formato elementų susiejimą su duomenų modeliu. 

Norėdami išsamiai susipažinti su šiuo scenarijumi, paleiskite užduočių vedlį ER konfigūracijos, skirtos importuoti duomenis iš išorinio failo, kūrimas (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų / sprendimų komponentų (10677) dalis). Norėdami paleisti šį vedlį, naudokite toliau nurodytus failus.

- [ER duomenų modelio konfigūracija (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER formato konfigūracija (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Gaunamo dokumento XML formatu pavyzdys (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Darbaknygės, skirtos tvarkyti gaunamo dokumento duomenis, pavyzdys (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Sukurto formato komponento saugojimas formato konfigūracijoje

ER gali saugoti sukurtą formatą su sukonfigūruotais duomenų susiejimais kaip dabartinio egzemplioriaus formato konfigūraciją. Ankstesnėje iliustracijoje pateiktas šio tipo formato konfigūracijos pavyzdys (**BACS (Jungtinė Karalystė)** – antrinis **mokėjimo modelio** konfigūracijos elementas). Paleiskite užduočių vedlį **ER konkretaus domeno formato kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>„Finance“ konfigūravimas norint pradėti naudoti sukurtą formatą viduje

Programą galima konfigūruoti, kad ji sukurtą formatą pradėtų naudoti elektroninėms ataskaitoms generuoti. Nuoroda į sukurto formato konfigūraciją turi būti apibrėžta naudojant konkretaus domeno parametrus. Pvz., norint pradėti naudoti ER formato konfigūraciją elektroniniams tiekėjo mokėjimams BACS formatu apdoroti, formato konfigūraciją reikia nurodyti konkrečiuose mokėjimo būduose.

Paleiskite užduočių vedlį **ER formato naudojimas elektroniniams mokėjimų dokumentams generuoti** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="handling-er-components"></a>ER komponentų tvarkymas

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER komponento publikavimas LCS, pateikiant jį naudoti išorėje (lokalizavimas)

Sukurto komponento (modelio arba formato) savininkas gali naudoti ER baigtai komponento versijai publikuoti LCS. Tam būtina dabartinio ER konfigūracijos teikėjo **LCS projekto** tipo saugykla. Kai baigtos komponento versijos būsena pakeičiama iš **BAIGTA** į **BENDRAI NAUDOJAMA**, ta versija publikuojama LCS. Publikavus komponentą LCS, to komponento savininkas tampa paslaugos teikėju, palaikančiu šį komponentą. Pavyzdžiui, jei formato komponentas yra skirtas pagal įstatymus būtinam elektroniniam dokumentui generuoti (pavyzdžiui, pagal lokalizavimo scenarijų), manoma, kad formatas turi atitikti teisės aktų pakeitimus ir kad tiekėjas turi išduoti naujas komponento versijas, kai to reikia naujiems įstatymų reikalavimams taikyti. Paleiskite užduočių vedlį **ER konfigūracijos nusiuntimas į „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER komponento importavimas iš LCS naudoti viduje

ER suteikia galimybę importuoti ER komponentus iš LCS į esamą egzempliorių. Būtina **LCS projekto** tipo saugykla. Importavus ER komponentą iš LCS į esamą egzempliorių, egzemplioriaus savininkas tampa paslaugos, kurią teikia importuoto komponento savininkas (autorius), vartotoju. Pavyzdžiui, jei šis formato komponentas skirtas konkrečiam elektroniniam dokumentui generuoti iš programos tam tikros valstybės / regiono būdingu formatu (lokalizavimo scenarijus), manoma, kad paslaugos vartotojas galės gauti visus šio formato naujinimus, kad formatas atitiktų įstatymų reikalavimus. Paleiskite užduočių vedlį **ER konfigūracijos importavimas iš „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Formato kūrimas pasirinkus kitą formatą kaip pagrindą (tinkinimas)

ER palaiko galimybę kurti (išvesti) naują komponentą iš dabartinės komponento (pagrindo), importuoto iš LCS, versijos. Pavyzdžiui, vartotojas nori išvesti naują formatą, siekdamas patenkinti kai kuriuos specialius elektroninio dokumento reikalavimus (pvz., reikalavimą naudoti papildomą lauką arba išsamų aprašą), kad būtų palaikomas tinkinimo scenarijus. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują jo pagrindinę versiją** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Formato versijos naujinimas pasirenkant naują pagrindinio formato versiją (pagrindo keitimas)

ER suteikia galimybę automatiškai priimti naujausios pagrindinio komponento versijos pakeitimus dabartinėje išvestinio komponento juodraščio versijoje. Šis procesas vadinamas *pritaikymu kitoje vietoje*. Pavyzdžiui, naują reguliavimo pakeitimą, įtrauktą į naujausią komponento, importuoto iš LCS, versiją, galima automatiškai sulieti su pritaikyta šio elektroninio dokumento formato versija. Bet kokie pakeitimai, kurių negalima sulieti automatiškai, yra laikomi konfliktais. Šiuos konfliktus galima išspręsti neautomatiniu būdu naudojant atitinkamo komponento kūrimo įrankį. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują to formato pagrindinę versiją** (verslo proceso **7.5.5.3 Įsigyti / sukurti pakeistų IT paslaugų ir sprendimų komponentų (10683)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>ER konfigūracijų, išleistų „Finance”, sąrašas

„Finance” ER konfigūracijų sąrašas nuolat atnaujinamas. Atidarykite [visuotinę saugyklą](er-download-configurations-global-repo.md) tam, kad peržiūrėtumėte šiuo metu palaikomų ER konfigūracijų sąrašą. „FastTab” **Nutraukimo informacija** galite peržiūrėti informaciją apie konfigūracijas, kurios buvo nutrauktos arba nebėra prižiūrimos. 

![Visuotinės saugyklos turinys konfigūracijų saugyklos puslapyje.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) konfigūracijų kūrimas](electronic-reporting-configuration.md)
- [Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

