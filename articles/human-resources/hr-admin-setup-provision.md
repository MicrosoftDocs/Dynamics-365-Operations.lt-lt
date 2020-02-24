---
title: „Human Resources“ parengimas
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3a7987a9b385fb6ba0294dc46b0d66be8228f06
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026272"
---
# <a name="provision-human-resources"></a>„Human Resources“ parengimas

Šiame straipsnyje pateikiami veiksmai, skirti paruošti naują gamybos aplinką programai „Microsoft Dynamics 365 Human Resources“. Šiame straipsnyje laikoma, kad įsigijote „Human Resources“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. Jei turite esamą „Microsoft Dynamics 365“ licenciją, kurioje jau yra „Human Resources“ paslaugos planas, ir negalite atlikti šiame straipsnyje nurodytų veiksmų, susisiekite su palaikymo tarnyba.

Norint pradėti, visuotinis administratorius turi prisijungti prie [„Microsoft Dynamics Lifecycle Services“](https://lcs.dynamics.com) (LCS) ir sukurti naują „Human Resources“ projektą. Išskyrus atvejus, kai problema dėl licencijos neleidžia paruošti „Human Resources“, palaikymo tarnybos arba „Dynamics‟ paslaugų inžinierių (DSE) atstovų pagalba nėra būtina.

## <a name="create-an-lcs-project"></a>LCS projekto kūrimas

Norėdami naudoti LCS „Human Resources“ aplinkoms valdyti, pirma turite sukurti LCS projektą.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index) naudodami paskyrą, kurią naudojote prisijungti prie „Human Resources“.

2. Pasirinkite pliuso ženklą (**+**), kad sukurtumėte projektą.

3. Pasirinkite **Microsoft Dynamics 365 Human Resources** kaip produkto pavadinimą ir produkto versiją.

4. Pasirinkite **Dynamics 365 Human Resources** metodiką.

5. Pasirinkite **Kurti**.

Informacijos apie tai, kaip pradėti dirbti su „Human Resources“, žr. **„Human Resources“** metodiką, kurią sukūrėte savo naujame projekte. Baigę kurti projektą, atlikite šią procedūrą, kad paruoštumėte „Human Resources“ aplinką.

## <a name="provision-a-human-resources-project"></a>„Human Resources“ projekto parengimas

Sukūrę LCS projektą, galite aplinkai paruošti „Human Resources“.

1. LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.

2. Nurodykite, ar tai smėlio dėžės ar gamybos „Human Resources“ egzempliorius. „Smėlio dėžės“ egzemplioriuose gali būti prieinamos išankstinės peržiūros funkcijos, kad būtų galima pateikti išankstinį grįžtamąjį ryšį ir atlikti bandymus.
   
    > [!NOTE]
    > Jau nustatytas „Talent“ egzemplioriaus tipas negali būti pakeistas. Prieš tęsdami įsitikinkite, kad pasirinktas teisingas egzemplioriaus tipas.</br></br>
    > „Human Resources“ egzemplioriaus tipas yra atskiras nuo „Microsoft Power Apps“ aplinkos egzemplioriaus tipo, kurį nustatote „Power Apps“ administravimo centre.
    
3. Pasirinkite parinktį **Įtraukti demonstracinius duomenis**, jei norite, kad jūsų aplinka apimtų tą patį demonstracinių duomenų rinkinį, kuris naudojamas ir „Human Resources“ bandomosios versijos funkcijose. Tai yra naudinga ilgalaikių demonstracijų ar mokymų aplinkose, bet niekada neturėtų būti naudojama gamybos aplinkose.  Atkreipkite dėmesį į tai, kad turite pasirinkti šią pasirinktį atlikdami pradinį diegimą. Vėliau negalėsite atnaujinti esamo diegimo.

4. „Human Resources“ visada konfigūruojama „Microsoft Power Apps“ aplinkai, siekiant įgalinti „Power Apps“ integravimą ir išplečiamumą. Prieš tęsdami perskaitykite šio straipsnio dalį „Power Apps“ aplinkos pasirinkimas“. Jei dar neturite „Power Apps“ aplinkos, LCS pasirinkite Valdyti aplinkas arba pereikite į „Power Apps“ administravimo centrą. Tada atlikite nurodytus veiksmus, norėdami [Kurti „Power Apps“ aplinką](https://docs.microsoft.com/powerapps/administrator/create-environment).

    > [!NOTE]
    > Norėdami peržiūrėti esamas aplinkas arba kurti naujas aplinkas, nuomotojo administratoriui, kuris konfigūruoja „Human Resources“, turi būti priskirta „Power Apps“ P2 licencija. Jei jūsų organizacija neturi „Power Apps“ P2 licencijos, galite ją gauti iš savo CSP arba [„Power Apps“ kainų puslapyje](https://powerapps.microsoft.com/pricing/).

5. Pasirinkite aplinką, į kurią parengti „Human Resources“.

6. Pasirinkite **Taip**, kad sutiktumėte su sąlygomis ir pradėtumėte diegimą.

   Nauja aplinka pasirodo aplinkų sąraše, kuris yra naršymo srityje, esančioje kairėje. Tačiau negalite pradėti naudoti aplinkos, kol diegimo būsena nebus atnaujinta į **Įdiegta**. Paprastai šis procesas užtrunka keletą minučių. Jei parengimo procesas nepavyksta, privalote susisiekti su palaikymo tarnyba.

7. Pasirinkite **Prisijungti prie „Human Resources“**, kad galėtumėte naudoti naująją aplinką.

    > [!NOTE]
    > Jei dar nesate patvirtinę galutinių reikalavimų, projekte galite įdiegti „Human Resources“ bandymo egzempliorių. Tada galite naudoti šį egzempliorių, kad išbandytumėte sprendimą, kol patvirtinsite. Jei naudojate naują aplinką bandymams, turite pakartoti šią procedūrą norėdami sukurti gamybos aplinką.

    > Į „Human Resources“ paskyrą galima įtraukti tik dvi LCS aplinkas, todėl galbūt norėsite 60 dienų nemokamai išbandyti [„Human Resources“ bandomąją aplinką](https://dynamics.microsoft.com/talent/overview/). Nors bandomoji aplinka priklauso vartotojui, kuris to pageidavo, kiti vartotojai gali būti pakviesti per sistemos administravimo galimybę, skirtą žmogiškiesiems ištekliams. Bandomosiose aplinkose pateikti išgalvoti duomenys, kuriais naudojantis galima saugiai tyrinėti programą. Jos nėra skirtos naudoti kaip gamybos aplinkos. Atkreipkite dėmesį, kad, po 60 dienų pasibaigus bandomosios aplinkos naudojimo terminui, visi joje esantys duomenys panaikinami ir jų nebegalima susigrąžinti. Pasibaigus dabartinės aplinkos naudojimo terminui, galite užsiregistruoti naujai bandomajai aplinkai.

## <a name="select-a-power-apps-environment"></a>„Power Apps“ aplinkos pasirinkimas

„Human Resources“ ir „Power Apps“ aplinkų integracija leidžia integruoti ir išplėsti „Human Resources“ duomenų naudojimą „Power Apps“ įrankiams. Informacija apie „Power Apps“ aplinkų tikslą ne tik padės sukurti programų, išplečiančių „Human Resources“ funkcijas, bet ir pagelbės renkantis tinkamą aplinką „Human resources“ parengimo metu. Norėdami gauti daugiau informacijos apie „Power Apps“ aplinkas, įskaitant aplinkų aprėptį, prieigą prie jų ir aplinkų kūrimą bei pasirinkimą, žr. [„Power Apps“ aplinkų paskelbimas](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Svarstydami, kurioje „Power Apps“ aplinkoje diegti „Human Resources“, pasinaudokite toliau pateiktais nurodymais. 

1. LCS pasirinkite **Valdyti aplinkas** arba eikite tiesiai į „Power Apps“ administravimo centrą, kuriame galėsite peržiūrėti esamas aplinkas ir sukurti naujų.

2. Viena „Human Resources“ aplinka susieta su viena „Power Apps“ aplinka.

3. „Power Apps“ aplinkoje kartu su programa „Human Resources“ pateikiamos atitinkamos „Power Apps“, „Power Automate“ ir „Common Data Service“ programos. Panaikinus „Power Apps“ aplinką, panaikinamos ir joje pateikiamos programos. Rengiant „Human Resources“ aplinką, galima sukonfigūruoti aplinkas **Bandomoji versija** arba **Gamyba**. Pagal tai, kaip aplinka bus naudojama, pasirinkite aplinkos tipą. 

4. Apsvarstykite, ar nereikėtų numatyti duomenų integravimo ir bandymo strategijų, pvz., smėlio dėžės, UAT arba gamybos. Rekomenduojame įvertinti įvairius diegimo padarinius, nes vėliau pakeisti su „Power Apps“ aplinka susietą „Human Resources“ aplinką nėra paprasta.

5. Toliau nurodytų „Power Apps“ aplinkų negalima naudoti programoje „Human Resources“ ir LCS esančiame pasirinkimo sąraše jos bus filtruojamos.
 
    - **Numatytosios „Power Apps“ aplinkos** – nors kiekvienas nuomotojas automatiškai parengiamas pagal numatytąją „Power Apps“ aplinką, nerekomenduojame jų naudoti kartu su „Human Resources“, nes visi vartotojai, kurie yra nuomotojai, turi prieigą prie „Power Apps “ aplinkos ir bandydami bei naršydami pasitelkiant „Power Apps“ ar „Power Automate“ integravimus gali netyčia sugadinti jūsų gamybos duomenis.
   
    - **Bandomosios aplinkos** – šios aplinkos kuriamos pritaikant galiojimo datą ir šiai pasibaigus nebegalios, o jūsų aplinka ir visi joje esantys „Human Resources“ egzemplioriai bus automatiškai pašalinti.
   
    - **Nepalaikomi regionai** – šiuo metu „Human Resources“ palaikoma tik šiuose regionuose: Jungtinėse Amerikos Valstijose, Europoje, Jungtinėje Karalystėje, Australijoje, Kanadoje ir Azijoje.
  
6. Nustatę tinkamą naudotiną aplinką, galite tęsti parengimo procesą. 
 
## <a name="grant-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas

Pagal numatytuosius nustatymus, aplinką sukūręs visuotinis administratorius turi prie jos prieigą. Tačiau papildomiems programos vartotojams prieiga turi būti aiškiai suteikta. Norėdami suteikti prieigą, turite pridėti vartotojų ir priskirti jiems tinkamus vaidmenis žmogiškųjų išteklių aplinkoje. „Human Resources“ įdiegęs visuotinis administratorius taip pat turi paleisti „Attract“ ir „Onboard“ programas, kad užbaigtų inicijavimą ir suteiktų prieigą kitiems vartotojams, kurie yra nuomotojai.  Kol tai nebus atlikta, kiti vartotojai neturės prieigos prie „Attract“ ir „Onboard“ programų ir matys prieigos pažeidimo klaidas. Daugiau informacijos rasite [Naujų vartotojų kūrimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ir [Vartotojų priskyrimas saugos vaidmenims](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
