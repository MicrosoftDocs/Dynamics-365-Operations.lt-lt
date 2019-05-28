---
title: „Talent“ parengimas
description: Šioje temoje pateikiami veiksmai, skirti paruošti naują aplinką programai „Microsoft Dynamics 365 for Talent“.
author: andreabichsel
manager: AnnBe
ms.date: 00/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 98f60e466b8b97215fdba0f48ca53ca57157283b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518655"
---
# <a name="provision-talent"></a>„Talent“ parengimas

[!include [banner](includes/banner.md)]

Šioje temoje pateikiami veiksmai, skirti paruošti naują gamybos aplinką programai „Microsoft Dynamics 365 for Talent“. Šioje temoje laikoma, kad įsigijote „Talent“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. Jei turite esamą „Microsoft Dynamics 365“ licenciją, kurioje jau yra „Talent“ paslaugos planas, ir negalite atlikti šioje temoje nurodytų veiksmų, susisiekite su palaikymo tarnyba.

Norint pradėti, visuotinis administratorius turi prisijungti prie [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) ir sukurti naują „Talent“ projektą. Išskyrus atvejus, kai problema dėl licencijos neleidžia paruošti „Talent“, palaikymo tarnybos arba „Dynamics‟ paslaugų inžinierių (DSE) atstovų pagalba nėra būtina.

## <a name="create-an-lcs-project"></a>LCS projekto kūrimas
Norėdami naudoti LCS „Talent“ aplinkoms valdyti, pirma turite sukurti LCS projektą.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index) naudodami abonementą, kurį naudojote prisijungti prie „Talent“.
2. Pasirinkite pliuso ženklą (**+**), kad sukurtumėte projektą.
3. Pasirinkite **Microsoft Dynamics 365 for Talent** kaip produkto pavadinimą ir produkto versiją.
4. Pasirinkite **Dynamics 365 for Talent** metodiką.
5. Pasirinkite **Kurti**.

Informacijos apie tai, kaip pradėti dirbti su „Talent“, žr. **Talent** metodiką, kurią sukūrėte savo naujame projekte. Baigę kurti projektą, atlikite šią procedūrą, kad paruoštumėte „Talent“ aplinką.

## <a name="provision-a-talent-project"></a>„Talent“ projekto paruošimas
Sukūrę LCS projektą, galite aplinkai paruošti „Talent“.

1. LCS projekte pasirinkite plytelę **Programos „Talent“ valdymas**.
2. „Talent“ visada paruošta „Microsoft PowerApps“ aplinkai, siekiant įgalinti „PowerApps“ integravimą ir išplečiamumą. Prieš tęsdami perskaitykite šios temos dalį „PowerApps“ aplinkos pasirinkimas“. Jei dar neturite „PowerApps“ aplinkos, LCS pasirinkite Valdyti aplinkas arba pereikite į „PowerApps“ administravimo centrą. Tada atlikite nurodytus veiksmus, kad [sukurtumėte „PowerApps“ aplinką](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment).

    > [!NOTE]
    > Norėdami peržiūrėti esamas aplinkas arba kurti naujas aplinkas, nuomotojo administratoriui, kuris paruošia „Talent“, turi būti priskirta „PowerApps“ P2 licencija. Jei jūsų organizacija neturi „PowerApps“ P2 licencijos, galite ją gauti iš savo CSP arba [„PowerApps“ kainų puslapyje](https://powerapps.microsoft.com/en-us/pricing/).

4. Pasirinkite **Įtraukti**, tada pasirinkite aplinką, kuriai norite paruošti „Talent“.
5. Pasirinkite parinktį **Įtraukti demonstracinius duomenis**, jei norite, kad jūsų aplinka apimtų tą patį demonstracinių duomenų rinkinį, kuris naudojamas ir „Talent“ bandomosios versijos patirtyje. Tai yra naudinga ilgalaikių demonstracijų ar mokymų aplinkose, bet niekada neturėtų būti naudojama gamybos aplinkose.  Atkreipkite dėmesį į tai, kad turite pasirinkti šią pasirinktį atlikdami pradinį diegimą. Vėliau negalėsite atnaujinti esamo diegimo.
6. Pasirinkite **Taip**, kad sutiktumėte su sąlygomis ir pradėtumėte diegimą.

    Nauja aplinka pasirodo aplinkų sąraše, kuris yra naršymo srityje, esančioje kairėje. Tačiau negalite pradėti naudoti aplinkos, kol diegimo būsena nebus atnaujinta į **Įdiegta**. Paprastai šis procesas užtrunka keletą minučių. Jei parengimo procesas nepavyksta, privalote susisiekti su palaikymo tarnyba.

7. Pasirinkite **Prisijungti prie „Talent“**, kad galėtumėte naudoti naująją aplinką.

    > [!NOTE]
    > Jei dar nesate patvirtinę galutinių reikalavimų, projekte galite įdiegti „Talent“ bandymo egzempliorių. Tada galite naudoti šį egzempliorių, kad išbandytumėte sprendimą, kol patvirtinsite. Jei naudojate naują aplinką bandymams, turite pakartoti šią procedūrą norėdami sukurti gamybos aplinką.

    > Į „Talent“ abonementą galima įtraukti tik dvi LCS aplinkas, todėl galbūt norėsite 60 dienų nemokamai išbandyti [„Talent“ bandomąją aplinką](https://dynamics.microsoft.com/en-us/talent/overview/). Bandomoji aplinka priklauso tam vartotojui, kuris ją užsakė, bet galima pakviesti ir kitus vartotojus per „Core HR“ sistemos administravimo patirtį. Bandomosiose aplinkose pateikti išgalvoti duomenys, kuriais naudojantis galima saugiai tyrinėti programą. Jos nėra skirtos naudoti kaip gamybos aplinkos. Atkreipkite dėmesį, kad, po 60 dienų pasibaigus bandomosios aplinkos naudojimo terminui, visi joje esantys duomenys panaikinami ir jų nebegalima susigrąžinti. Pasibaigus dabartinės aplinkos naudojimo terminui, galite užsiregistruoti naujai bandomajai aplinkai.

## <a name="select-a-powerapps-environment"></a>Pasirinkite „PowerApps“ aplinką

„Talent“ ir „PowerApps“ aplinkų integracija leidžia integruoti ir išplėsti „Talent“ duomenų naudojimą „PowerApps“ priemonėmis. Informacija apie „PowerApps“ aplinkų tikslą ne tik padės sukurti programų, išplečiančių „Talent“ funkcijas, bet ir pagelbės renkantis tinkamą aplinką „Talent“ rengimo metu. Norėdami gauti daugiau informacijos apie „PowerApps“ aplinkas, įskaitant aplinkų aprėptį, prieigą prie jų ir aplinkų kūrimą bei pasirinkimą, žr. [„PowerApps“ aplinkų paskelbimas](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Svarstydami, kurias „PowerApps“ aplinkas diegti į „Talent“, pasinaudokite toliau pateiktais nurodymais. 

1. LCS pasirinkite **Valdyti aplinkas** arba eikite tiesiai į „PowerApps“ administravimo centrą, kuriame galėsite peržiūrėti esamas aplinkas ir sukurti naujų.
2. Viena „Talent“ aplinka susieta su viena „PowerApps“ aplinka.
3. „PowerApps“ aplinkoje kartu su programa „Talent“ pateikiamos atitinkamos „PowerApps“, srauto ir „Common Data Service“ programos. Panaikinus „PowerApps“ aplinką, panaikinamos ir joje pateikiamos programos. Rengiant „Talent“ aplinką, galima sukonfigūruoti aplinkas „Bandomoji versija“ arba „Gamyba“. Pagal tai, kaip aplinka bus naudojama, pasirinkite aplinkos tipą. 
4. Apsvarstykite, ar nereikėtų numatyti duomenų integravimo ir bandymo strategijų, pvz., smėlio dėžės, UAT arba gamybos. Rekomenduojame įvertinti įvairius diegimo padarinius, nes vėliau pakeisti su „PowerApps“ aplinka susietą „Talent“ aplinką nėra paprasta.
5. Toliau nurodytų „PowerApps“ aplinkų negalima naudoti programoje „Talent“ ir LCS esančiame pasirinkimo sąraše jos bus filtruojamos.
 
    - **Numatytosios „PowerApps“ aplinkos** – Nors kiekvienas nuomotojas automatiškai sukonfigūruojamas pagal numatytąją „PowerApps“ aplinką, nerekomenduojame jų naudoti kartu su „Talent“, nes visi vartotojai, kurie yra nuomotojai, turi prieigą prie „PowerApps“ ir bandydami bei naršydami pasitelkiant „PowerApps“ ar srauto integravimus gali netyčia sugadinti jūsų gamybos duomenis.
   
    - **Bandomosios aplinkos** – Šios aplinkos kuriamos pritaikant galiojimo laikotarpį ir šiam pasibaigus nebegalios, o jūsų aplinka ir visi joje esantys „Talent“ egzemplioriai bus automatiškai pašalinti.
   
    - **Nepalaikomi regionai** – Šiuo metu „Talent“ palaikoma tik šiuose regionuose: Jungtinėse Amerikos Valstijose, Jungtinėje Karalystėje ir Australijoje.
  
6. Nustatę tinkamą naudotiną aplinką, galite tęsti parengimo procesą. 
 
## <a name="grant-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas
Pagal numatytuosius nustatymus, aplinką sukūręs visuotinis administratorius turi prie jos prieigą. Tačiau papildomiems programos vartotojams prieiga turi būti aiškiai suteikta. Norėdami suteikti prieigą, turėsite pridėti vartotojų ir jiems priskirti atitinkamus vaidmenis „Core HR“ aplinkoje. „Talent“ įdiegęs visuotinis administratorius taip pat turi paleisti „Attract“ ir „Onboard“ programas, kad užbaigtų inicijavimą ir suteiktų prieigą kitiems nuomotojams–vartotojams.  Kol tai nebus atlikta, kiti vartotojai neturės priegos prie „Attract“ ir „Onboard“ programų ir matys prieigos pažeidimo klaidas. Daugiau informacijos rasite [Naujų vartotojų kūrimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ir [Vartotojų priskyrimas saugos vaidmenims](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
