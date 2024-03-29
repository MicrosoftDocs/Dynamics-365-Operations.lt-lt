---
title: „Human Resources“ parengimas
description: Šiame straipsnyje paaiškinamas naujos "Microsoft" gamybos aplinkos parengimo procesas Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc44b52e2f7662fc6be609562cec903a8755d1b
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178510"
---
# <a name="provision-human-resources"></a>„Human Resources“ parengimas

_**Taikoma:** žmogiškieji ištekliai autonominėje infrastruktūrose_ 

> [!NOTE]
> Nuo 2022 m. birželio mėn. personalo aplinkas galima įdiegti tik finansų ir operacijų programų infrastruktūrose. Daugiau informacijos ieškokite Finansų [ir operacijų infrastruktūros personalo parengimas](hr-admin-setup-provision-fo.md).

Šiame straipsnyje paaiškinamas naujos "Microsoft" gamybos aplinkos parengimo procesas Dynamics 365 Human Resources. 

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradedant parengti naują gamybos aplinką, turi būti įvykdytos toliau pateikiamos būtinosios sąlygos.

- Įsigijote „Human Resources“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. Jei turite esamą „Microsoft Dynamics 365“ licenciją, kurioje jau yra „Human Resources“ paslaugos planas, ir negalite atlikti šiame straipsnyje nurodytų veiksmų, susisiekite su palaikymo tarnyba.

- Visuotinis administratorius prisijungė prie [„Microsoft Dynamics Lifecycle Services“](https://lcs.dynamics.com) (LCS) ir sukūrė naują „Human Resources“ projektą. 

## <a name="provision-a-human-resources-trial-environment"></a>„Human Resources” bandomosios aplinkos parengimas

>[!NOTE]
> Nuo 2022 m. balandžio mėn. personalo bandomojo aplinkos nebus galimos atskirai programoje. Potencialūs klientai, kurie nori įvertinti personalo pajėgumus finansų ir operacijų programėlėse, gali tai daryti naudodami nemokamą 30 dienų bandomąją versiją ir demonstracinius duomenis. "Dynamics 365 Finance" apims personalo pajėgumus, kuriuos į finansų infrastruktūrą atims atskira programa. Norėdami gauti daugiau informacijos, žr [. personalo pasiūlymų suliejimą klientams kartu](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Daugiau informacijos apie "Dynamics 365" finansų bandymus ieškokite nuoseklioje [vadove](../fin-ops-core/fin-ops/get-started/before-you-buy.md). 


Prieš parengdami savo pirmąją smėlio dėžės arba gamybos aplinką, galite norėti parengti [bandomąją „Human Resources” aplinką](https://go.microsoft.com/fwlink/p/?LinkId=2115962), kad patikrintumėte „Human Resources” funkcionalumą. Bandomosiose aplinkose pateikti išgalvoti duomenys, kuriais naudojantis galima saugiai tyrinėti programą. Nors bandomoji aplinka priklauso vartotojui, kuris to pageidavo, kiti vartotojai gali būti pakviesti per sistemos administravimo galimybę, skirtą žmogiškiesiems ištekliams. 

Bandomoji aplinka padeda įvertinti asmenų, kurie dar neturi prieigos prie personalo aplinkos, personalo funkcijas. Jei jūs parengiate bandomąją aplinką, o autentifikuotas vartotojas jau turi prieigą prie vienos ar daugiau esamų personalo aplinkų, vartotojas bus nukreiptas į esamą aplinką arba aplinkų sąrašą.

Bandomosios aplinkos nėra skirtos naudoti kaip gamybos aplinkos. Jos apribojamos 30 dienų bandomuoju laikotarpiu. Kai bandomasis laikotarpis baigiasi, aplinka ir visi jame esantys duomenys bus panaikinti ir negali būti atkurti. Aplinkos negalima konvertuoti į sandrę arba gamybos aplinką. Pasibaigus dabartinės aplinkos naudojimo terminui, galite užsiregistruoti naujai bandomajai aplinkai.

Kuriant „Human Resources“ bandomąją aplinką, nuomininkams taip pat sukuriama bandomoji aplinka, „Power Apps“ susieta su personalo aplinka. Aplinka, „Power Apps“ pavadinta „TestDrive“ yra, turi tą patį bandomąjį laikotarpį kaip ir „Human Resources“ aplinka.

> [!NOTE]
> „Human Resources“ bandomojo aplinkos parengti nepavyks, jei autentifikuotas vartotojas neturi teisės kurti „Power Apps“ bandomojo aplinkos. Vartotojas turi būti įtrauktas į vartotojų grupę, kuri gali sukurti bandomąją aplinką „Power Platform“ administravimo centre. Norėdami gauti daugiau informacijos, žr. [valdiklį, kuris gali kurti ir valdyti aplinkas „Power Platform“ administravimo centre](/power-platform/admin/control-environment-creation).

## <a name="plan-human-resources-environments"></a>Planuokite „Human Resources“ aplinkas

Prieš jums sukuriant pirma „Human Resources“ aplinką, turėtumėte atsargiai suplanuoti aplinkos poreikius savo projektui. Pagrindinė prenumerata „Human Resources“ apima dvi aplinkas: gamybos ir smėlio dėžės. Atsižvelgiant į jūsų projekto sudėtingumą, norint palaikyti projekto veiklą gali reikėti nupirkti papildomas sand. aplinkas. 

Papildomų aplinkų aspektai.

- **Duomenų perkėlimas**: duomenų perkėlimo veikla, kuri leidžia tikrinti jūsų sandų dėžės aplinką viso projekto metu. Papildomos aplinkos turėjimas leidžia duomenų perkėlimo veiksmus tęsti testuojant ir konfigūruojant veiklas kartu kitoje aplinkoje.
- **Integracija**: konfigūruokite ir patikrinkite integravimą, kuris gali apimti vietinius integravimą, pvz., Ceriforce Dayforce, ar pasirinktinius integravimą.
- **Mokymas**: gali reikėti atskiros aplinkos, sukonfigūruotos su mokymo duomenų lapu, kad jūsų darbuotojai galėtų traukinys naudotis nauja sistema. 
- **Kelių etapų projektas**: palaikyti konfigūraciją, duomenų perkėlimą, bandymą ar kitą veiklą projekto etape, kuris planuojamas po pradinio projekto etapo.

 > [!IMPORTANT]
 > Rekomenduojame svarstant savo aplinką atlikti tolesnius veiksmus.
 > - Naudoti savo gamybos aplinką projekto metu, kaip jūsų GOLD konfigūravimo aplinką. Tai yra svarbu, nes negalite nukopijuoti smėlio dėžės aplinkos į gamybos aplinką. Dėl to, kai paleisite į internetą, jūsų GOLD aplinka bus jūsų gamybos aplinka ir jūs baigsite nukirpimo veiklas šioje aplinkoje.</br></br>
 > - Naudoti savo smėlio dėžę ar kitą aplinką siekiant atlikti nukirpimą prieš paleidimą į internetą. Galite tai padaryti iš naujo paleisdami gamybos aplinką su savo GOLD konfigūravimu į savo smėlio dėžės aplinką.</br></br>
 > - Laikyti išsamų nupjovimo patikrų sąrašą, kuris apima visus duomenų paketus, būtinus norint galutinius duomenis perkelti į gamybos aplinką paleidimo į internetą nukirpimo metu.</br></br>
 > - Naudoti savo smėlio dėžės aplinką projekto metu, kaip jūsų TEST aplinką. Jei jums reikia papildomų aplinkų, jūsų organizacija gali įsigyti jas už papildomą kainą.</br></br>

## <a name="create-an-lcs-project"></a>LCS projekto kūrimas

Norėdami naudoti LCS „Human Resources“ aplinkoms valdyti, pirma turite sukurti LCS projektą.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index) naudodami paskyrą, kurią naudojote prisijungti prie „Human Resources“.

   > [!NOTE]
   > Norint užtikrinti sėkmingą parengimą, abonementas, kurį naudojate personalo aplinkai konfigūruoti, turi būti priskirtas arba sistemos administratoriui, arba sistemos pritaikymo priemonės vaidmeniui aplinkoje, kuri susieta **su** **personalo**„Power Apps“ aplinka. Norėdami „Power Platform“ gauti daugiau informacijos apie saugos vaidmenų priskyrimą programos vartotojams, [peržiūrėkite vartotojo saugos konfigūravimą pagal išteklius](/power-platform/admin/database-security)“.

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
    > Nustačius personalo egzemplioriaus tipą, jo keisti negalima. Prieš tęsdami įsitikinkite, kad pasirinktas teisingas egzemplioriaus tipas.</br></br>
    > „Human Resources“ egzemplioriaus tipas yra atskiras nuo „Microsoft Power Apps“ aplinkos egzemplioriaus tipo, kurį nustatote „Power Apps“ administravimo centre.
    
3. Pasirinkite parinktį **Įtraukti demonstracinius duomenis**, jei norite, kad jūsų aplinka apimtų tą patį demonstracinių duomenų rinkinį, kuris naudojamas ir „Human Resources“ bandomojoje aplinkoje. Demonstraciniai duomenys yra naudingi ilgalaikių demonstracijų ar mokymų aplinkose, bet niekada neturėtų būti naudojami gamybos aplinkose. Turite pasirinkti šią pasirinktį atlikdami pradinį diegimą. Vėliau negalėsite atnaujinti esamo diegimo.

4. „Human Resources“ visada konfigūruojama „Microsoft Power Apps“ aplinkai, siekiant įgalinti „Power Apps“ integravimą ir išplečiamumą. Prieš tęsdami perskaitykite šio straipsnio dalį „Power Apps“ aplinkos pasirinkimas“. Jei dar neturite „Power Apps“ aplinkos, LCS pasirinkite Valdyti aplinkas arba pereikite į „Power Apps“ administravimo centrą. Tada atlikite nurodytus veiksmus, norėdami [Kurti „Power Apps“ aplinką](/powerapps/administrator/create-environment).

5. Pasirinkite aplinką, į kurią parengti „Human Resources“.

6. Pasirinkite **Taip**, kad sutiktumėte su sąlygomis ir pradėtumėte diegimą.

   Nauja aplinka pasirodo aplinkų sąraše, kuris yra naršymo srityje, esančioje kairėje. Tačiau negalima pradėti naudoti aplinkos, kol diegimo būsena nėra **Įdiegta**. Paprastai šis procesas užtrunka keletą minučių. Jei parengimo procesas nesėkmingas, susisiekite su palaikymo tarnyba.

7. Pasirinkite **Prisijungti prie „Human Resources“**, kad galėtumėte naudoti naująją aplinką.

    > [!NOTE]
    > Jei dar nesate patvirtinę galutinių reikalavimų, projekte galite įdiegti „Human Resources“ bandymo egzempliorių. Tada galite naudoti šį egzempliorių, kad išbandytumėte sprendimą, kol patvirtinsite. Jei naudojate naują aplinką bandymams, turite pakartoti šią procedūrą norėdami sukurti gamybos aplinką.

## <a name="select-a-power-apps-environment"></a>„Power Apps“ aplinkos pasirinkimas

Naudodami „Power Apps” įrankius galite integruoti ir išplėsti „Human Resources“ duomenų naudojimą. Norėdami gauti daugiau informacijos apie „Power Apps“ aplinkas, įskaitant aplinkų aprėptį, prieigą prie jų ir aplinkų kūrimą bei pasirinkimą, žr. [„Power Apps“ aplinkų paskelbimas](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Svarstydami, kurioje „Power Apps“ aplinkoje diegti „Human Resources“, pasinaudokite toliau pateiktais nurodymais. 

1. LCS pasirinkite **Valdyti aplinkas**. Taip pat galite tiesiogiai pereiti į „Power Apps“ administravimo centrą, kur galite peržiūrėti esamas aplinkas ir kurti naujas.

2. Viena „Human Resources“ aplinka susieta su viena „Power Apps“ aplinka.

3. „Power Apps“ aplinkoje kartu su programa „Human Resources“ pateikiamos atitinkamos „Power Apps“, „Power Automate“ ir „Dataverse“ programos. Panaikinus „Power Apps“ aplinką, panaikinamos ir joje pateikiamos programos. Rengiant „Human Resources“ aplinką, galima sukonfigūruoti aplinkas **Bandomoji versija** arba **Gamyba**. Pagal tai, kaip aplinka bus naudojama, pasirinkite aplinkos tipą. 

4. Apsvarstykite, ar nereikėtų numatyti duomenų integravimo ir bandymo strategijų, pvz., smėlio dėžės, UAT arba gamybos. Atidžiai apsvarstykite diegimo padarinius, nes pakeisti su „Power Apps“ aplinka susietą „Human Resources“ aplinką nėra paprasta.

5. Programoje „Human Resources“ negalima naudoti toliau pateiktų „Power Apps” aplinkų. Jos filtruojamos LCS esančiame pasirinkimo sąraše.
 
    - **Numatytosios „Power Apps” aplinkos** – nors kiekvienas nuomotojas automatiškai sukonfigūruojamas pagal numatytąją „Power Apps“ aplinką, nerekomenduojame jų naudoti kartu su „Human Resources“. Visi nuomotojo vartotojai turi prieigą prie „Power Apps“ aplinkos ir bandydami bei naršydami naudodami „Power Apps“ ar „Power Automate“ integravimus jie gali netyčia sugadinti gamybos duomenis.
   
    - **Bandomosios aplinkos** – šios aplinkos kuriamos pritaikant galiojimo datą. Baigus galioti, jūsų aplinka ir visi joje esantys „Human Resources“ egzemplioriai bus automatiškai pašalinti.
   
    - **Nepalaikomi geografiniai** grafikai – aplinka turi būti palaikomame geografijos kataloge. Daugiau informacijos rasite skyriuje [Palaikomos geografijos](hr-admin-setup-provision.md#supported-geographies).

6. Dvigubo rašymo galimybes, kurias naudojant galima integruoti personalo duomenis į „Power Apps” aplinką, galima naudoti tik pasirinkus **Įgalinti „Dynamics 365” programas** parinktį aplinkai. Daugiau informacijos ieškokite dvigubo rašymo [titulinis puslapis](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md).

    > [!NOTE]
    > Parinktis **Įgalinti „Dynamics 365” programas** turi būti pažymėta „Power Apps” aplinkos kūrimo metu. Jei ši parinktis nėra pažymėta parengimo metu, negalėsite naudoti dvigubo rašymo duomenų integravimui tarp „Dynamics 365 Human Resources” ir „Power Apps” aplinkos, taip pat įdiegti „Dynamics 365” programų, pavyzdžiui, „Dynamics 365 Sales” ir „Field Service”, aplinkoje. Ši pasirinktis yra negrįžtama. 
    > -  Personalo tarnyba nepalaiko susieto egzemplioriaus keitimo Dataverse, kai į jį įdiegiamas personalo valdymo egzempliorius. </br></br>
    > Daugiau informacijos rasite [Keletas svarbių aplinkybių kuriant naują aplinką](/power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment) „Power Platform” dokumentacijos svetainėje.  

7. Nustatę tinkamą naudotiną aplinką, galite tęsti parengimo procesą. 

### <a name="supported-geographies"></a>Palaikomi geografiniai grafikai

Personalo valdymas šiuo metu palaiko šiuos geografinius grafikus:

- Jungtinės Valstijos
- Europa
- Jungtinė Karalystė
- Australija
- Kanada
- Azija 

Kurdami personalo aplinką pasirinkite aplinką, kurią norite „Power Apps“ susieti su personalo aplinka. Tada personalo aplinka yra numatyta toje pačioje „Azure" geografijos aplinkoje, kaip ir „Power Apps“ pasirinkta aplinka. Galite pasirinkti, kurioje vietoje personalo aplinka ir duomenų bazė yra fiziškai pasirinkdami geografijos katalogą, kai kuriate „Power Apps“ aplinką, kuri bus susieta su „Human Resources” aplinka.

Galite pasirinkti *„Azure" geografijos, kurioje yra aplinka, bet negalite pasirinkti* konkretaus „Azure" *regiono*. Automatizavimas nustato specifinį geografijos regioną, kuriame aplinka yra sukurta apkrovos balansavimui ir našumui optimizuoti. Informaciją apie „Azure" regionams ir regionams galite rasti [„Azure" geografinių diagramų](https://azure.microsoft.com/global-infrastructure/geographies) dokumentuose.

Personalo aplinkos duomenys visada bus „Azure" geografijos, kurioje ji kuriama, viduje. Tačiau jo visada nebus tame pačiame „Azure" regione. Dėl įvykių susigrąžinimo tikslo duomenys bus dubliuoti ir pirminiame „Azure" regione, ir antriniame geografijos failo regione.

 > [!NOTE]
 > „Human Resources“ aplinkos perkėlimas iš vieno „Azure“ regiono į kitą nepalaikomas.

## <a name="grant-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas

Pagal numatytuosius nustatymus, aplinką sukūręs visuotinis administratorius turi prie jos prieigą. Papildomiems programos vartotojams prieiga turi būti aiškiai suteikta. Turite pridėti vartotojų ir priskirti jiems tinkamus vaidmenis „Human Resources“ aplinkoje. Daugiau informacijos rasite [Naujų vartotojų kūrimas](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ir [Vartotojų priskyrimas saugos vaidmenims](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

