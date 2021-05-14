---
title: „Human Resources“ parengimas
description: Šiame straipsnyje pateikiami veiksmai, skirti paruošti naują gamybos aplinką programai „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fee496157db581bf77f444674ca858aa4383e27c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963220"
---
# <a name="provision-human-resources"></a>„Human Resources“ parengimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje pateikiami veiksmai, skirti paruošti naują gamybos aplinką programai „Microsoft Dynamics 365 Human Resources“. Šiame straipsnyje laikoma, kad įsigijote „Human Resources“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. Jei turite esamą „Microsoft Dynamics 365“ licenciją, kurioje jau yra „Human Resources“ paslaugos planas, ir negalite atlikti šiame straipsnyje nurodytų veiksmų, susisiekite su palaikymo tarnyba.

Norint pradėti, visuotinis administratorius turi prisijungti prie [„Microsoft Dynamics Lifecycle Services“](https://lcs.dynamics.com) (LCS) ir sukurti naują „Human Resources“ projektą. Išskyrus atvejus, kai problema dėl licencijos neleidžia paruošti „Human Resources“, palaikymo tarnybos arba „Dynamics‟ paslaugų inžinierių (DSE) atstovų pagalba nėra būtina.

## <a name="plan-human-resources-environments"></a>Planuokite „Human Resources“ aplinkas

Prieš jums sukuriant pirma „Human Resources“ aplinką, turėtumėte atsargiai suplanuoti aplinkos poreikius savo projektui. Pagrindinė prenumerata „Human Resources“ apima dvi aplinkas: gamybos ir smėlio dėžės. Priklausomai nuo projekto kompleksiškumo, jums gali reikėti įsigyti papildomas smėlio dėžės aplinkas, kad palaikytumėte projekto veiklas. 

Svarstymai dėl papildomų aplinkų įtraukimo, tačiau neapsiribojantys, yra tokie:

- **Duomenų perkėlimas**: Jums gali reikėti apgalvoti papildomą aplinką dėl duomenų perkėlimo veiksmų, kad leistumėte savo smėlio dėžės aplinkai būti naudojamai testavimo tikslais per projektą. Papildomos aplinkos turėjimas leidžia duomenų perkėlimo veiksmus tęsti testuojant ir konfigūruojant veiklas kartu kitoje aplinkoje.
- **Integravimas**: Jums gali reikėti apgalvoti papildomas aplinkas tam, kad konfigūruotumėte ir testuotumėte integravimus. Tai gali apimti įgimtus integravimus, tokius kaip „Ceridian Dayforce LinkedIn Talent Hub“ integravimus ar tinkintus integravimus, tokius kaip algalapio, aplikanto sekimo sistemos ar išmokų sistemos ir tiekėjai.
- **Mokymai**: Jums gali reikėti atskiros aplinkos, kuri konfigūruota su nustatytais mokymų duomenimis tam, kad apmokytumėte savo darbuotojus naudoti naują sistemą. 
- **Kelių etapų projektas**: Jums gali reikėti apgalvoti papildomą aplinką siekiant palaikyti konfigūravimą, duomenų perkėlimą, testavimą ir kitas veiklas projekto etape, kuris suplanuotas po pradinio paleidimo projekto į internetą.

 > [!IMPORTANT]
 > Rekomenduojame jums naudoti savo gamybos aplinką projekto metu, kaip jūsų GOLD konfigūravimo aplinką. Tai yra svarbu, nes negalite nukopijuoti smėlio dėžės aplinkos į gamybos aplinką. Dėl to, kai paleisite į internetą, jūsų GOLD aplinka bus jūsų gamybos aplinka ir jūs baigsite nukirpimo veiklas šioje aplinkoje.</br></br>
 > Jums rekomenduojame naudoti jūsų smėlio dėžę ir kitą aplinką siekiant atlikti nukirpimą prieš paleidimą į internetą. Galite tai padaryti iš naujo paleisdami gamybos aplinką su savo GOLD konfigūravimu į savo smėlio dėžės aplinką.</br></br>
 > Rekomenduojame jums laikyti išsamų nupjovimo patikrų sąrašą, kuris apima visus duomenų paketus, būtinus perkelti galutinius duomenis į gamybos aplinką paleidimo į internetą nukirpimo metu.</br></br>
 > Taip pat rekomenduojame jums naudoti jūsų smėlio dėžės aplinką per projektą, kaip jūsų TESTAVIMO aplinką. Jei jums reikia papildomų aplinkų, jūsų organizacija gali įsigyti jas už papildomą kainą.</br></br>

## <a name="create-an-lcs-project"></a>LCS projekto kūrimas

Norėdami naudoti LCS „Human Resources“ aplinkoms valdyti, pirma turite sukurti LCS projektą.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index) naudodami paskyrą, kurią naudojote prisijungti prie „Human Resources“.

   > [!NOTE]
   > Norint užtikrinti sėkmingą parengimą, abonementas, kurį naudojate personalo aplinkai konfigūruoti, turi būti priskirtas arba sistemos administratoriui, arba sistemos pritaikymo priemonės vaidmeniui aplinkoje, kuri susieta **su** **personalo**„Power Apps“ aplinka. Norėdami [gauti daugiau informacijos apie saugos vaidmenų priskyrimą programos](https://docs.microsoft.com/power-platform/admin/database-security) vartotojams, peržiūrėkite vartotojo saugos konfigūravimą pagal išteklius „Power Platform“.

2. Pasirinkite pliuso ženklą (**+**), kad sukurtumėte projektą.

3. Pasirinkite **Microsoft Dynamics 365 Human Resources** kaip produkto pavadinimą ir produkto versiją.

4. Pasirinkite **Dynamics 365 Human Resources** metodiką.

5. Pasirinkite **Kurti**.

Informacijos apie tai, kaip pradėti dirbti su „Human Resources“, žr. **„Human Resources“** metodiką, kurią sukūrėte savo naujame projekte. Baigę kurti projektą, atlikite šią procedūrą, kad paruoštumėte „Human Resources“ aplinką.

## <a name="provision-a-human-resources-project"></a>„Human Resources“ projekto parengimas

Sukūrę LCS projektą, galite aplinkai paruošti „Human Resources“.

1. LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.

2. Nurodykite, ar ši aplinka yra smėlio dėžės, ar gamybos „Human Resources“ egzempliorius. „Smėlio dėžės“ egzemplioriuose gali būti prieinamos išankstinės peržiūros funkcijos, kad būtų galima pateikti išankstinį grįžtamąjį ryšį ir atlikti bandymus.
   
    > [!NOTE]
    > Jau nustatytas „Human Resources“ egzemplioriaus tipas negali būti pakeistas. Prieš tęsdami įsitikinkite, kad pasirinktas teisingas egzemplioriaus tipas.</br></br>
    > „Human Resources“ egzemplioriaus tipas yra atskiras nuo „Microsoft Power Apps“ aplinkos egzemplioriaus tipo, kurį nustatote „Power Apps“ administravimo centre.
    
3. Pasirinkite parinktį **Įtraukti demonstracinius duomenis**, jei norite, kad jūsų aplinka apimtų tą patį demonstracinių duomenų rinkinį, kuris naudojamas ir „Human Resources“ bandomosios versijos funkcijose. Demonstraciniai duomenys yra naudingi ilgalaikių demonstracijų ar mokymų aplinkose, bet niekada neturėtų būti naudojami gamybos aplinkose. Turite pasirinkti šią pasirinktį atlikdami pradinį diegimą. Vėliau negalėsite atnaujinti esamo diegimo.

4. „Human Resources“ visada konfigūruojama „Microsoft Power Apps“ aplinkai, siekiant įgalinti „Power Apps“ integravimą ir išplečiamumą. Prieš tęsdami perskaitykite šio straipsnio dalį „Power Apps“ aplinkos pasirinkimas“. Jei dar neturite „Power Apps“ aplinkos, LCS pasirinkite Valdyti aplinkas arba pereikite į „Power Apps“ administravimo centrą. Tada atlikite nurodytus veiksmus, norėdami [Kurti „Power Apps“ aplinką](/powerapps/administrator/create-environment).

5. Pasirinkite aplinką, į kurią parengti „Human Resources“.

6. Pasirinkite **Taip**, kad sutiktumėte su sąlygomis ir pradėtumėte diegimą.

   Nauja aplinka pasirodo aplinkų sąraše, kuris yra naršymo srityje, esančioje kairėje. Tačiau negalite pradėti naudoti aplinkos, kol diegimo būsena nebus atnaujinta į **Įdiegta**. Paprastai šis procesas užtrunka keletą minučių. Jei parengimo procesas nepavyksta, privalote susisiekti su palaikymo tarnyba.

7. Pasirinkite **Prisijungti prie „Human Resources“**, kad galėtumėte naudoti naująją aplinką.

    > [!NOTE]
    > Jei dar nesate patvirtinę galutinių reikalavimų, projekte galite įdiegti „Human Resources“ bandymo egzempliorių. Tada galite naudoti šį egzempliorių, kad išbandytumėte sprendimą, kol patvirtinsite. Jei naudojate naują aplinką bandymams, turite pakartoti šią procedūrą norėdami sukurti gamybos aplinką.

    > Galbūt norėsite 60 dienų nemokamai naudotis [„Human Resources“ bandomoji aplinka ](https://go.microsoft.com/fwlink/p/?LinkId=2115962). Nors bandomoji aplinka priklauso vartotojui, kuris to pageidavo, kiti vartotojai gali būti pakviesti per sistemos administravimo galimybę, skirtą žmogiškiesiems ištekliams. Bandomosiose aplinkose pateikti išgalvoti duomenys, kuriais naudojantis galima saugiai tyrinėti programą. Jos nėra skirtos naudoti kaip gamybos aplinkos. Atkreipkite dėmesį, kad, po 60 dienų pasibaigus bandomosios aplinkos naudojimo terminui, visi joje esantys duomenys panaikinami ir jų nebegalima susigrąžinti. Pasibaigus dabartinės aplinkos naudojimo terminui, galite užsiregistruoti naujai bandomajai aplinkai.

## <a name="select-a-power-apps-environment"></a>„Power Apps“ aplinkos pasirinkimas

Naudodami „Power Apps” įrankius galite integruoti ir išplėsti „Human Resources“ duomenų naudojimą. Norėdami gauti daugiau informacijos apie „Power Apps“ aplinkas, įskaitant aplinkų aprėptį, prieigą prie jų ir aplinkų kūrimą bei pasirinkimą, žr. [„Power Apps“ aplinkų paskelbimas](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Svarstydami, kurioje „Power Apps“ aplinkoje diegti „Human Resources“, pasinaudokite toliau pateiktais nurodymais. 

1. LCS pasirinkite **Valdyti aplinkas**. Taip pat galite tiesiogiai pereiti į „Power Apps“ administravimo centrą, kur galite peržiūrėti esamas aplinkas ir kurti naujas.

2. Viena „Human Resources“ aplinka susieta su viena „Power Apps“ aplinka.

3. „Power Apps“ aplinkoje kartu su programa „Human Resources“ pateikiamos atitinkamos „Power Apps“, „Power Automate“ ir „Dataverse“ programos. Panaikinus „Power Apps“ aplinką, panaikinamos ir joje pateikiamos programos. Rengiant „Human Resources“ aplinką, galima sukonfigūruoti aplinkas **Bandomoji versija** arba **Gamyba**. Pagal tai, kaip aplinka bus naudojama, pasirinkite aplinkos tipą. 

4. Apsvarstykite, ar nereikėtų numatyti duomenų integravimo ir bandymo strategijų, pvz., smėlio dėžės, UAT arba gamybos. Atidžiai apsvarstykite diegimo padarinius, nes pakeisti su „Power Apps“ aplinka susietą „Human Resources“ aplinką nėra paprasta.

5. Programoje „Human Resources“ negalite naudoti toliau pateiktų „Power Apps” aplinkų. Jos filtruojamos LCS esančiame pasirinkimo sąraše.
 
    - **Numatytosios „Power Apps” aplinkos** – nors kiekvienas nuomotojas automatiškai sukonfigūruojamas pagal numatytąją „Power Apps“ aplinką, nerekomenduojame jų naudoti kartu su „Human Resources“. Visi nuomotojo vartotojai turi prieigą prie „Power Apps“ aplinkos ir bandydami bei naršydami naudodami „Power Apps“ ar „Power Automate“ integravimus jie gali netyčia sugadinti gamybos duomenis.
   
    - **Bandomosios aplinkos** – šios aplinkos kuriamos pritaikant galiojimo datą. Baigus galioti, jūsų aplinka ir visi joje esantys „Human Resources“ egzemplioriai bus automatiškai pašalinti.
   
    - **Nepalaikomi geografiniai** grafikai – aplinka turi būti palaikomame geografijos kataloge. Daugiau informacijos rasite skyriuje [Palaikomos geografijos](hr-admin-setup-provision.md#supported-geographies).

6. Nustatę tinkamą naudotiną aplinką, galite tęsti parengimo procesą. 

### <a name="supported-geographies"></a>Palaikomi geografiniai grafikai

Personalo valdymas šiuo metu palaiko šiuos geografinius grafikus:

- Jungtinės Valstijos
- Europa
- Jungtinė Karalystė
- Australija
- Kanada
- Azija 

Kurdami personalo aplinką pasirinkite aplinką, kurią norite „Power Apps“ susieti su personalo aplinka. Tada personalo aplinka yra numatyta toje pačioje „Azure" geografijos aplinkoje, kaip ir „Power Apps“ pasirinkta aplinka. Galite pasirinkti, kurioje vietoje personalo aplinka ir duomenų bazė yra faktiškai, pasirinkdami geografijos katalogą, kur bus siejama su „Power Apps“ personalo aplinka.

Galite pasirinkti *„Azure" geografijos, kurioje yra aplinka, bet negalite pasirinkti* konkretaus „Azure" *regiono*. Automatizavimas nustato specifinį geografijos regioną, kuriame aplinka yra sukurta apkrovos balansavimui ir našumui optimizuoti. Informaciją apie „Azure" regionams ir regionams galite rasti [„Azure" geografinių diagramų](https://azure.microsoft.com/global-infrastructure/geographies) dokumentuose.

Personalo aplinkos duomenys visada bus „Azure" geografijos, kurioje ji kuriama, viduje. Tačiau jo visada nebus tame pačiame „Azure" regione. Dėl įvykių susigrąžinimo tikslo duomenys bus dubliuoti ir pirminiame „Azure" regione, ir antriniame geografijos failo regione.

 > [!NOTE]
 > „Human Resources“ aplinkos perkėlimas iš vieno „Azure“ regiono į kitą nepalaikomas.

## <a name="grant-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas

Pagal numatytuosius nustatymus, aplinką sukūręs visuotinis administratorius turi prie jos prieigą. Papildomiems programos vartotojams prieiga turi būti aiškiai suteikta. Turite pridėti vartotojų ir priskirti jiems tinkamus vaidmenis „Human Resources“ aplinkoje. „Human Resources“ įdiegęs visuotinis administratorius taip pat turi paleisti „Attract“ ir „Onboard“ programas, kad užbaigtų inicijavimą ir suteiktų prieigą kitiems vartotojams, kurie yra nuomotojai. Kol tai nebus atlikta, kiti vartotojai neturės prieigos prie „Attract“ ir „Onboard“ programų ir matys prieigos pažeidimo klaidas. Daugiau informacijos rasite [Naujų vartotojų kūrimas](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ir [Vartotojų priskyrimas saugos vaidmenims](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
