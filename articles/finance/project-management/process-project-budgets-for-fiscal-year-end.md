---
title: Projekto biudžetų perkėlimas finansinių metų pabaigoje
description: Šiame straipsnyje pateikiama inoformation apie tai, kaip perkelti likusias biudžeto sumas į būsimus metus ir sukurti biudžeto registro informaciją.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172335"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projekto biudžetų perkėlimas finansinių metų pabaigoje

[!include [banner](../includes/banner.md)]

Dirbant su daugiamečiu projektu gali likti biudžeto finansinių metų pabaigoje. Galite perkelti likusias biudžeto sumas būsimiems metams ir sukurti tų sumų biudžeto registro išsamią informaciją susietosiose DK sąskaitose. Prieš perkeldami likusias sumas, peržiūrėkite ir išanalizuokite likusias biudžeto sumas.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Likusių biudžeto sumų peržiūra ir analizė

Atlikite toliau nurodytus veiksmus, kad peržiūrėtumėte metų pabaigos biudžeto sumas, taikomas projektams, jų neperkeldami.

1. Eikite į **Projektų valdymas ir apskaita** > **Periodiniai** > **Biudžetai** > **Perkeliami biudžetai**. 
2. Puslapyje **Projekto biudžeto perkėlimo procesas**, skirtuke **Metų pabaigos parinktys**, patikrinkite, ar neįgalinta **Perkelti likusias projekto biudžeto sumas**.
3. Skirtuke **Parametrai** tab, lauke **Projekto biudžeto metai**, pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti. 
4. Lauke **Atviri finansiniai metai** pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti. 
5. Lauke **Iš prognozės modelio** pasirinkite **Likęs biudžetas**. 
6. Norėdami įtraukti atitinkančius pasirinktus kriterijus ir neturinčius likusio biudžeto projektus, pasirinkite **Rodyti nulinį likutį**.  
7. Skirtuke **Pasirinkti biudžetus** pasirinkite **Grąžinti visus biudžetus**, kad būtų įkelti visi jūsų pasirinktus kriterijus atitinkantys biudžetai, tada pasirinkite **Apdoroti**. 
8. Norėdami sukurti duomenų bazės užklausą, kuri įkelia konkretų biudžetų rinkinį į sritį, pasirinkite **Grąžinti pasirinktus biudžetus**.

Norėdami gauti daugiau informacijos apie konkrečią srities eilutę, pasirinkite eilutę ir pasirinkite **Peržiūrėti biudžeto išsamią informaciją** arba **Peržiūrėti sąskaitas**.

## <a name="carry-forward-remaining-budget-amounts"></a>Likusių biudžeto sumų perkėlimas 

Kai apdorojate likusias biudžeto sumas, galite sukurti operacijas DK, taikomas sumoms, kurias perkeliate. Norėdami sukurti DK operacijas, atlikite skyriaus veiksmus, [Biudžeto sumų perkėlimas kuriant DK operacijas](#carry-forward). 

> [!NOTE]
> Perkeliamos biudžeto sumos perkeliamos į prognozės modelį, kuris pasirinktas puslapyje **Prognozių modeliai** kaip perkėlimo prognozės modelis.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Biudžeto sumų perkėlimas kuriant DK operacijas

1.  Pasirinkite **Projektų valdymas ir apskaita** > **Periodiniai** > **Biudžetai** > **Perkeliami biudžetai**. 
2. Puslapyje **Projekto biudžeto perkėlimo procesas** pasirinkite **Metų pabaiga** ir įgalinkite **Perkelti likusias projekto biudžeto sumas** ir **Sukurti biudžeto registro įrašus DK**. 
3. Skirtuke **Parametrai**, esančiame laukų grupėje **Projekto parametrai**, pasirinkite šiuos veiksmus:

   - **Projekto biudžeto metai**: pasirinkite finansinių metų, kurių likusias biudžeto sumas norite peržiūrėti, pradžią. 
   - **Pelnas ir nuostolis**: sukurkite pelno ir nuostolio operacijų Didžiojoje knygoje. 
   -  **NG**: sukurkite nebaigtos gamybos (NG) operacijų Didžiojoje knygoje.
   -  **Algalapis**: sukurkite algalapių paskirstymo operacijų Didžiojoje knygoje. 

5. Laukų grupėje **Didžioji knyga** pateikta toliau nurodyta informacija. 

   - Lauke **Atviri finansiniai metai** pasirinkite finansinių metų, į kuriuos norite perkelti likusias biudžeto sumas, taikomas projektams. Numatytoji reikšmė yra vieni metai po reikšmės, nurodytos lauke **Projekto biudžeto metai**.
   -  Lauke **Perkeliamas laikotarpis** pasirinkite laikotarpį, kuriam DK norite sukurti biudžeto registro išsamią informaciją. Taip paprastai yra pirmasis atvirų finansinių metų laikotarpis.

6. Laukų grupėje **Kopijuoti iš / į** pateikta toliau nurodyta informacija.

   - Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis biudžeto sumomis, taikomomis projektams, kurias norite perkelti. 
   - Lauke **Į DK biudžeto modelį** pasirinkite DK biudžeto modelį, susietą su biudžeto sumomis,, kurias norite perkelti į DK. 
   -  Norėdami naudoti projekto pardavimo valiutą DK operacijose, kurios sukurtos perkeliant biudžeto sumas, taikomas projektams, pažymėkite **Perkelti pardavimo valiutą**. Jei parinktis nepažymėta, operacijos naudoja apskaitos valiutą. 
   -  Norėdami įtraukti projektus, kurių likusių biudžeto sumų nėra, bet kurie atitinka kitus kriterijus, kuriuos pasirinkote apatinėje srityje rodomiems projektams, pažymėkite **Rodyti nulinį likutį**.

7. Skirtuke **Pasirinkti biudžetus** pasirinkite **Grąžinti visus biudžetus**, kad būtų įkelti visi jūsų pasirinktus kriterijus atitinkantys biudžetai. Jei pageidaujate, galite sukurti duomenų bazės užklausą, kuri įkelia konkretų projekto biudžetų rinkinį į sritį, pasirinkite **Grąžinti pasirinktus biudžetus**.
8. Pažymėkite kiekvieno norimo apdoroti projekto parinktį projekto eilutės pradžioje.

    > [!TIP]
    > Norėdami pasirinkti visus arba daugumą projektų, viršutiniame kairiajame kampe pasirinkite žymės langelį. Norėdami neįtraukti projekto apdorojimo, atžymėkite projekto žymės langelį.

9. Pasirinkite **Apdoroti**, norėdami perkelti likusias biudžeto sumas, taikomas pasirinktiems projektams, į pasirinktus finansinius metus ir sukurtumėte biudžeto registro išsamią informaciją DK.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Biudžeto sumų perkėlimas nekuriant DK operacijų

1. Eikite į **Projektų valdymas ir apskaita** > **Periodiniai** > **Biudžetai** > **Perkeliami biudžetai**.
2. Puslapyje **Projekto biudžeto perkėlimo procesas**, lauke **Metų pabaigos parinktys**, pasirinkite **Perkelti likusias projekto biudžeto sumas**.
3. Grupėje **Parametrai**, lauke **Projekto biudžeto metai**, pasirinkite finansinius metus, kurių likusias biudžeto sumas norite peržiūrėti.
4. Grupėje **Kopijuoti iš / į** pateikta toliau nurodyta informacija.

   - Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis biudžeto sumomis, taikomomis projektams, kurias norite perkelti. 
   - Pasirinkite **Rodyti nulinį likutį**, norėdami įtraukti neturinčius likusio biudžeto sumų, tačiau atitinkančius kitus pasirinktus kriterijus, projektus.
   - Grupėje **Pasirinkti biudžetus** pasirinkite **Grąžinti visus biudžetus**, kad būtų įkelti visi jūsų pasirinktus kriterijus atitinkantys biudžetai. Norėdami sukurti duomenų bazės užklausą, kuri įkelia konkretų projekto biudžetų rinkinį į sritį, pasirinkite **Grąžinti pasirinktus biudžetus**.

5. Pažymėkite kiekvieno norimo apdoroti projekto parinktį projekto eilutės pradžioje. 
6. Pasirinkite **Apdoroti**, kad perkeltumėte likusias biudžeto sumas, taikomas pasirinktiems projektams, į pasirinktus finansinius metus.

