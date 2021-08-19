---
title: 'ER: formato atnaujinimas pritaikant naują pagrindinę to formato versiją'
description: Šioje temoje aprašoma, kaip išlaikyti elektroninių ataskaitų (ER) formato konfigūraciją.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfcb85d964234063fd3c6a8e5ea29f7b222e966124b48e46b72b04f457c91e6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720813"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>ER: formato atnaujinimas pritaikant naują pagrindinę to formato versiją

[!include [banner](../../includes/banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali prižiūrėti elektroninių ataskaitų (ER) formato konfigūraciją. Šia procedūra paaiškinama, kaip pasirinktinę formato versiją galima sukurti pagal iš konfigūracijų teikėjo (KT) gautą formatą. Ja taip pat paaiškinama, kaip pritaikyti naują, pagrindinę to formato versiją.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūrų „Konfigūracijų teikėjo sukūrimas ir jo pažymėjimas kaip aktyvaus‟ ir „Sukurto formato naudojimas generuoti elektroniniams mokėjimų dokumentams‟ veiksmus. Šiuos veiksmus galima atlikti GBSI įmonėje.

## <a name="select-format-configuration-for-customization"></a>Formato konfigūracijos pasirinkimas tinkinti
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.

    Šiame pavyzdyje pavyzdinė įmonė „Litware, Inc.“ (https://www.litware.com) veiks kaip konfigūracijų teikėjas, kuris palaiko konkrečios šalies elektroninių mokėjimų formato konfigūracijas.    Pavyzdinė įmonė „Proseware, Inc.‟ (http://www.proseware.com) veiks kaip formato konfigūracija, kurią pateikė „Litware, Inc.‟ „Proseware, Inc.“ naudoja formatus tam tikruose tos šalies regionuose.  
2. Spustelėkite Ataskaitų konfigūracijos.
3. Spustelėkite Rodyti filtrus.
4. Taikykite šiuos filtrus: lauke „Pavadinimas” įveskite filtro reikšmę „BACS (JK fiktyvus)” naudodami filtro operatorių „prasideda“.
  
    Pasirinkta BACS (JK fiktyvus) formato konfigūracija priklauso teikėjui „Litware, Inc.‟  

5. Spustelėkite Rodyti filtrus.
6. Sąraše raskite ir pasirinkite norimą įrašą.

    Tinkinti „Proseware, Inc.‟ naudos formato versiją, kurios būsena – Baigta.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Naujos savo pasirinktinio elektroninio dokumento formato konfigūracijos kūrimas
„Proseware, Inc.“ gavo 1.1 BACS (JK fiktyvus) konfigūracijos versiją, kurioje yra pradinis formatas, skirtas generuoti elektroninio mokėjimo dokumentams iš „Litware, Inc.‟ pagal jų aptarnavimo abonementą. „Proseware, Inc.“ nori pradėti ją naudoti kaip standartą savo šalyje, tačiau, norint atitikti konkretaus regiono reikalavimus, ją reikia šiek tiek pritaikyti. „Proseware, Inc.“ taip pat nori pasilikti galimybę atnaujinti pasirinktinį formatą, kai tik „Litware, Inc.‟ pateiks naują jo versiją (su pakeitimais, atitinkančiais naujus konkrečios šalies reikalavimus), ir ji atnaujinti nori patirdama kuo mažesnes išlaidas.  

Norėdami tai padaryti, „Proseware, Inc.‟ turi sukurti konfigūraciją, kaip pagrindą naudodama „Litware, Inc.‟ BACS (JK fiktyvus) konfigūraciją.  

1. Uždarykite puslapį.
2. Pasirinkite „Proseware, Inc.‟ kaip aktyvų teikėją.
3. Spustelėkite Nustatyti kaip aktyvų.
4. Spustelėkite Ataskaitų konfigūracijos.
5. Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.
6. Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.

    Iš „Litware, Inc.” pasirinkite BACS (JK fiktyvus) konfigūraciją. „Proseware, Inc.” kaip pasirinktinės versijos pagrindą naudos 1.1 versiją.  

7. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.

    Taip galite sukurti naują pasirinktinio mokėjimo formato konfigūraciją.  

8. Lauke Naujas įveskite „Kildinti iš pavadinimo: BACS (JK fiktyvus), „Litware, Inc.‟.

    Norėdami patvirtinti, kad kaip pasirinktinės versijos kūrimo pagrindas bus naudojamas BACS (JK fiktyvus), pasirinkite parinktį Kildinti.  

9. Lauke Pavadinimas įveskite „BACS (JK fiktyvus pasirinktinis)“.
10. Lauke „Aprašas“ įveskite „BACS tiekėjo mokėjimas (JK fiktyvus pasirinktinis)“.

    Čia automatiškai įvedamas aktyvus konfigūracijų teikėjas („Proseware, Inc.‟). Šis teikėjas galės prižiūrėti šią konfigūraciją. Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.  

11. Spustelėkite Sukurti konfigūraciją.

## <a name="customize-your-format-for-the-electronic-document"></a>Savo elektroninio dokumento formato tinkinimas
1. Spustelėkite Konstruktorius.
2. Spustelėkite Išplėsti / sutraukti.
3. Spustelėkite Išplėsti / sutraukti.
4. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas“.
5. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
6. Medyje pasirinkite „XML \ Elementas“.
7. Lauke „Pavadinimas“, įveskite „IBAN“.
8. Spustelėkite Gerai.
9. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ IBAN“.
10. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
11. Medyje pasirinkite „Tekstas \ Eilutė‟.
12. Spustelėkite Gerai.
13. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas \ Eilutė“.
14. Lauke Didžiausias ilgis įveskite „60‟.
15. Spustelėkite skirtuką „Susiejimas“.
16. Medyje išplėskite „modelis‟.
17. Medyje išplėskite „modelis \ Mokėjimai‟.
18. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.
19. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita‟.
20. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita \ IBAN“.
21. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė = model.Payments \ Tiekėjas \ Bankas \ IBAN \ Eilutė”.
22. Spustelėkite Susieti.
23. Spustelėkite Įrašyti.

## <a name="validate-the-customized-format"></a>Pritaikyto formato tikrinimas
1. Spustelėkite Tikrinti.

    Patikrinkite pritaikytą formato maketą ir duomenų susiejimo pakeitimus ir įsitikinkite, kad visi susiejimai veikia gerai.  

2. Uždarykite puslapį.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Pasirinktinės formato konfigūracijos dabartinės versijos būsenos keitimas
Pakeiskite sukurtos formato konfigūracijos būseną iš Juodraštis į Baigta, kad ją būtų galima naudoti generuojant mokėjimo dokumentus.  

1. Spustelėkite keisti būseną.

    Atkreipkite dėmesį, kad dabartinės pasirinktos konfigūracijos versijos būsena yra Juodraštis.  

2. Spustelėkite Baigti.
3. Lauke Aprašas įveskite reikšmę.
4. Spustelėkite GERAI.
5. Sąraše raskite ir pasirinkite norimą įrašą.

    Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1.1.1 baigta versija. Tai reiškia, kad tai yra 1-oji pasirinktinio BACS (JK fiktyvus pasirinktinis) formato versija, kuri paremta 1-ąja BACS (JK fiktyvus) formato versija, kuri paremta 1-ąja mokėjimų (suprastintasis modelis) duomenų modelio versija.  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Pritaikyto formato tikrinimas generuojant mokėjimo failus
Lygiagrečiame „Finance and Operations” seanse atlikite procedūros „Sukurto formato naudojimas generuoti elektroniniams mokėjimų dokumentams‟ veiksmus. Elektroninio mokėjimo būdo parametruose pasirinkite BACS (JK fiktyvus pasirinktinis) formatą. Įsitikinkite, kad sukurtame mokėjimo faile yra neseniai įdiegtas XML mazgas, pagal regiono reikalavimus pateikiantis IBAN kodą.  

## <a name="update-the-existing-country-specific-configuration"></a>Esamos konkrečios šalies konfigūracijos naujinimas
„Litware, Inc.“ turi atnaujinti BACS (JK fiktyvus) konfigūraciją ir įgyvendinti naujus šalies reikalavimus dėl elektroninio dokumento formato valdymo. Vėliau tai bus įtraukta į naują šios konfigūracijos versiją, kuri bus teikiama aptarnavimo abonentams, įskaitant „Proseware, Inc.‟  

Tikrų su paslaugų teikimu susijusių procesų metu kiekvieną naują BACS (JK fiktyvus) versiją „Proseware, Inc.‟ galima importuoti iš „Litware, Inc.‟ konfigūracijų LCS saugyklos. Atlikdami šią procedūrą tai imituosime BACS (JK fiktyvus) atnaujindami paslaugų teikėjo vardu.  

1. Uždarykite puslapį.
2. Pasirinkite teikėją „Litware, inc.“.
3. Spustelėkite Nustatyti kaip aktyvų.
4. Spustelėkite Ataskaitų konfigūracijos.
5. Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.
6. Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.

    Pasirenkama teikėjui „Litware, Inc.‟ priklausanti BACS (JK fiktyvus) juodraščio versija, siekiant įdiegti keitimus, atitinkančius naujus konkrečios šalies reikalavimus.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Elektroninio dokumento pagrindinio formato lokalizavimas
Tarkime, kad yra naujų šalies reikalavimų, kuriuos turi palaikyti „Litware, Inc.“:  

- Kreditoriaus banko SWIFT kodo reikšmė kiekvienoje mokėjimo operacijoje.
- Tiekėjo pavadinimo teksto generuojamame faile yra 100 simbolių ilgio riba.  
- Nauji konkrečių šalių reikalavimai  
- Pasirinkite norimos konfigūracijos juodraščio versiją, kad įdiegtumėte reikiamus pakeitimus.  


1. Spustelėkite Konstruktorius.
2. Spustelėkite Išplėsti / sutraukti.
3. Spustelėkite Išplėsti / sutraukti.
4. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas“.
5. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
6. Medyje pasirinkite „XML \ Elementas“.
7. Lauke „Pavadinimas“ įveskite „SWIFT“.
8. Spustelėkite Gerai.
9. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ SWIFT“.
10. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
11. Medyje pasirinkite „Tekstas \ Eilutė‟.
12. Spustelėkite Gerai.
13. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas \ Eilutė“.
14. Lauke Didžiausias ilgis įveskite „100‟.
15. Spustelėkite skirtuką „Susiejimas“.
16. Medyje išplėskite „modelis‟.
17. Medyje išplėskite „modelis \ Mokėjimai‟.
18. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.
19. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Agentas‟.
20. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Agentas \ SWIFT“.
21. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė = model.Payments \ Tiekėjas \ Bankas \ SWIFT \ Eilutė”.
22. Spustelėkite Susieti.
23. Spustelėkite Įrašyti.

## <a name="validate-the-localized-format"></a>Lokalizuoto formato tikrinimas
1. Spustelėkite Tikrinti.
2. Uždarykite puslapį.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Pagrindinės formato konfigūracijos dabartinės versijos būsenos keitimas
Atnaujintos pagrindinės formato konfigūracijos būseną iš Juodraštis pakeiskite į Baigta, kad ją būtų galima naudoti generuojant mokėjimo dokumentus ir atnaujinant iš jos gautas formato konfigūracijas.  

1. Spustelėkite keisti būseną.

    Atkreipkite dėmesį, kad dabartinės pasirinktos konfigūracijos versijos būsena yra Juodraštis.  

2. Spustelėkite Baigti.
3. Lauke Aprašas įveskite reikšmę.
4. Spustelėkite GERAI.
5. Sąraše raskite ir pasirinkite norimą įrašą.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Pasirinktinės formato konfigūracijos pagrindinės versijos keitimas

„Proseware, Inc.“ informuota, kad yra nauja 1.2 BACS (JK fiktyvus) konfigūracija, kurią galima naudoti generuojant elektroninio mokėjimo dokumentus pagal neseniai paskelbtus konkrečių šalių reikalavimus. „Proseware, Inc.“ nori pradėti ją naudoti kaip tos šalies standartą.  

Norėdami tai padaryti, „Proseware, Inc.‟ turi pakeisti pagrindinę pasirinktinės BACS (JK fiktyvus pasirinktinis) konfigūracijos versiją. Vietoj 1.1 BACS (JK fiktyvus) versijos naudoti naują 1.2 versiją.  

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Pasirinkite teikėją „Proseware, Inc.” ir pažymėkite jį kaip aktyvų.
3. Spustelėkite Nustatyti kaip aktyvų.
4. Spustelėkite Ataskaitų konfigūracijos.
5. Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.
6. Medyje išskleiskite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.
7. Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus) \ BACS (JK fiktyvus pasirinktinis)“.

    Pasirinkite BACS (JK fiktyvus pasirinktinis) konfigūraciją, kuri priklauso įmonei „Proseware, Inc.‟.  

    Naudokite pasirinktos konfigūracijos juodraščio versiją, kad įdiegtumėte reikiamus pakeitimus.  

8. Spustelėkite Pritaikyti kitoje vietoje.

    Pasirinkite naująją 1.2 pagrindinės konfigūracijos versiją, kuri bus taikoma kaip naujas konfigūracijos naujinimo pagrindas.  

9. Spustelėkite GERAI.

    Atkreipkite dėmesį, kad, suliejant pasirinktinę versiją ir naują pagrindinę versiją, rasta konfliktų, susijusių su tam tikrais formato pakeitimais, kurių automatiškai sulieti negalima.  

## <a name="resolve-rebase-conflicts"></a>Pritaikymo kitoje vietoje konfliktų sprendimas
1. Spustelėkite Konstruktorius.
    
    Atkreipkite dėmesį, kad nepavyko automatiškai išspręsti tiekėjo pavadinimo teksto ilgio limito. Todėl tai pateikiama konfliktų sąraše. Su kiekvienu tipo Naujinimas konfliktu galima naudoti tolesnes parinktis. – Taikyti ankstesnę pagrindinę reikšmę (mygtukas tinklelio viršuje), kad būtų pasirinkta ankstesnė pagrindinės versijos reikšmė (mūsų atveju – 0).  - Taikyti pagrindinę reikšmę (mygtukas tinklelio viršuje), kad būtų pasirinkta nauja pagrindinės versijos reikšmė (mūsų atveju – 100).  - pasilikti savo (pasirinktinę) reikšmę (mūsų atveju – 60).  Spustelėkite Taikyti pagrindinę reikšmę, kad pritaikytumėte konkrečių šalių 100 simbolių limitą tiekėjo pavadinimo teksto ilgiui.  

    Atkreipkite dėmesį, kad „Proseware, Inc.‟ ir „Litware, Inc.‟ turi pasirinktinių ir vietinių šio formato versijų, naudojančių IBAN ir SWIFT kodus su susijusiais komponentais, kurie automatiškai suliejami valdomame formate.  

2. Spustelėkite Taikyti pagrindinę reikšmę.

    Spustelėkite Taikyti pagrindinę reikšmę, kad pritaikytumėte konkrečių šalių 100 simbolių limitą tiekėjų pavadinimams.  

3. Spustelėkite Įrašyti.

    Įrašius formatą iš konfliktų sąrašo bus pašalinti išspręsti konfliktai.  

4. Uždarykite puslapį.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Pasirinktinės formato konfigūracijos naujos versijos būsenos keitimas
1. Spustelėkite keisti būseną.

    Atnaujintos, pasirinktinės formato konfigūracijos būseną pakeiskite iš Juodraštis į Baigta. Taip formato konfigūraciją bus galima naudoti generuojant mokėjimo dokumentus. Atkreipkite dėmesį, kad dabartinės pasirinktos konfigūracijos versijos būsena yra Juodraštis.  

2. Spustelėkite Baigti.
3. Lauke Aprašas įveskite reikšmę.
4. Spustelėkite GERAI.

    Atkreipkite dėmesį, kad sukurtoji konfigūracija įrašoma kaip baigta 1.2.2 versija: 2-oji pagrindinio BACS (JK fiktyvus pasirinktinis) formato versija, paremta 2-ąja pagrindinio BACS (JK fiktyvus) formato versija, kuri paremta 1-ąja mokėjimų (suprastintasis modelis) duomenų modelio versija.  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Pritaikyto formato tikrinimas generuojant mokėjimo failus
Lygiagrečiame „Finance and Operations” seanse atlikite procedūros „Sukurto formato naudojimas generuoti elektroniniams mokėjimų dokumentams‟ veiksmus. Elektroninio mokėjimo būdo parametruose pasirinkite sukurtąjį formatą „BACS (JK fiktyvus pasirinktinis)‟. Įsitikinkite, kad sukurtame mokėjimo faile yra neseniai „Proseware, Inc.“ įdiegtas XML mazgas, pagal regiono reikalavimus pateikiantis IBAN sąskaitos kodą. Faile taip pat turėtų būti neseniai įmonės „Litware, Inc.‟ įdiegtas XML mazgas, pagal šalies reikalavimus pateikiantis SWIFT banko kodą.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]