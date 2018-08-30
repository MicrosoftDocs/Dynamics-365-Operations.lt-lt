---
title: "„Talent“ parengimas"
description: "Šioje temoje pateikiami veiksmai, skirti paruošti naują aplinką programai „Microsoft Dynamics 365 for Talent“."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 2fc4119f3b33aa583274f4d823e296752cdde41d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="provision-talent"></a>„Talent“ parengimas

[!include [banner](includes/banner.md)]

Šioje temoje pateikiami veiksmai, skirti parengti naują gamybos aplinką programai „Microsoft Dynamics 365 for Talent“. Šioje temoje laikoma, kad įsigijote „Talent“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. Jei turite esamą „Microsoft Dynamics 365“ licenciją, kurioje jau yra „Talent“ paslaugos planas, ir negalite atlikti šioje temoje nurodytų veiksmų, susisiekite su palaikymo tarnyba.

Norint pradėti, visuotinis administratorius turi prisijungti prie [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) ir sukurti naują „Talent“ projektą. Išskyrus atvejus, kai problema dėl licencijos neleidžia paruošti „Talent“, palaikymo tarnybos arba „Dynamics‟ paslaugų inžinierių (DSE) atstovų pagalba nėra būtina.

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
2. „Talent“ visada paruošta „Microsoft PowerApps“ aplinkai, siekiant įgalinti „PowerApps“ integravimą ir išplečiamumą. Prieš tęsdami perskaitykite šios temos dalį „PowerApps“ aplinkos pasirinkimas“. 
3. Jei dar neturite „PowerApps“ aplinkos, prieš tęsdami atlikite veiksmus, nurodytus šios temos dalyje „Naujos „PowerApps“ aplinkos kūrimas (jei reikia)“.

    > [!NOTE]
    > Norėdami peržiūrėti esamas aplinkas arba kurti naujas aplinkas, nuomotojo administratoriui, kuris paruošia „Talent“, turi būti priskirta „PowerApps“ P2 licencija. Jei jūsų organizacija neturi „PowerApps“ P2 licencijos, galite ją gauti iš savo CSP arba [„PowerApps“ kainų puslapyje](https://powerapps.microsoft.com/en-us/pricing/).

4. Pasirinkite **Įtraukti**, tada pasirinkite aplinką, kuriai norite paruošti „Talent“.
5. Pasirinkite parinktį „Įtraukti demonstracinius duomenis“, jei norite, kad jūsų aplinka apimtų tą patį demonstracinių duomenų rinkinį, kuris naudojamas ir „Talent“ bandomosios versijos patirtyje.  Tai yra naudinga ilgalaikių demonstracijų ar mokymų aplinkose, bet niekada neturėtų būti naudojama gamybos aplinkose.  Atkreipkite dėmesį, kad turite pasirinkti šią parinktį atlikus pradinį diegimą, o esamo diegimo vėliau atnaujinti negalėsite.
6. Pasirinkite **Taip**, kad sutiktumėte su sąlygomis ir pradėtumėte diegimą.

    Nauja aplinka pasirodo aplinkų sąraše, kuris yra naršymo srityje, esančioje kairėje. Tačiau negalite pradėti naudoti aplinkos, kol diegimo būsena nebus atnaujinta į **Įdiegta**. Paprastai šis procesas užtrunka tik keletą minučių. Jei parengimo procesas nepavyksta, privalote susisiekti su palaikymo tarnyba.

7. Pasirinkite **Prisijungti prie „Talent“**, kad galėtumėte naudoti naująją aplinką.

> [!NOTE]
> Jei dar nesate patvirtinę galutinių reikalavimų, projekte galite įdiegti „Talent“ bandymo egzempliorių. Tada galite naudoti šį egzempliorių, kad išbandytumėte sprendimą, kol patvirtinsite. Jei naudojate naują aplinką bandymams, turite pakartoti šią procedūrą norėdami sukurti gamybos aplinką.

> [!NOTE]
> Į „Talent“ abonementą galima įtraukti tik dvi LCS aplinkas, todėl taip pat galite 60 dienų nemokamai išbandyti [„Talent“ bandomąją aplinką](https://dynamics.microsoft.com/en-us/talent/overview/). Bandomoji aplinka priklauso tam vartotojui, kuris ją užsakė, bet galima pakviesti ir kitus vartotojus per „Core HR“ sistemos administravimo patirtį. Bandomosiose aplinkose pateikti išgalvoti duomenys, kuriais naudojantis galima saugiai tyrinėti programą. Jos nėra skirtos naudoti kaip gamybos aplinkos. Atkreipkite dėmesį, kad, po 60 dienų pasibaigus bandomosios aplinkos naudojimo terminui, visi joje esantys duomenys panaikinami ir jų nebegalima susigrąžinti. Pasibaigus dabartinės aplinkos naudojimo terminui, galite užsiregistruoti naujai bandomajai aplinkai.

## <a name="select-a-powerapps-environment"></a>Pasirinkite „PowerApps“ aplinką

„Talent“ ir „PowerApps“ aplinkų integracija leidžia integruoti ir išplėsti „Talent“ duomenų naudojimą „PowerApps“ priemonėmis. Informacija apie „PowerApps“ aplinkų tikslą ne tik padės sukurti programų, išplečiančių „Talent“ funkcijas, bet ir pagelbės renkantis tinkamą aplinką „Talent“ rengimo metu. Norėdami gauti daugiau informacijos apie „PowerApps“ aplinkas, įskaitant aplinkų aprėptį, prieigą prie jų ir aplinkų kūrimą bei pasirinkimą, žr. [„PowerApps“ aplinkų paskelbimas](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Svarstydami, kurias „PowerApps“ aplinkas diegti į „Talent“, pasinaudokite toliau pateiktais nurodymais. 
1. LCS pasirinkite Valdyti aplinkas arba eikite tiesiai į „PowerApps“ administravimo centrą, kuriame galėsite peržiūrėti esamą aplinką ir sukurti naujų.
2. Viena „Talent“ aplinka susieta su viena „PowerApps“ aplinka.
3. „PowerApps“ aplinkoje kartu su programa „Talent“ pateikiamos atitinkamos „PowerApps“, srauto ir CDS programos. Panaikinus „PowerApps“ aplinką, panaikinamos ir joje pateikiamos programos.
4. Apsvarstykite, ar nereikėtų numatyti duomenų integravimo ir bandymo strategijų, pvz., smėlio dėžės, UAT, gamybos. Todėl rekomenduojame įvertinti įvairius diegimo padarinius, nes vėliau pakeisti su „PowerApps“ aplinka susietą „Talent“ aplinką nėra paprasta.
5. Toliau nurodytų „PowerApps“ aplinkų negalima naudoti programoje „Talent“ ir LCS esančiame pasirinkimo sąraše jos bus filtruojamos.
 
    **CDS 2.0 aplinkos** CDS 2.0 bus viešai pasiekiama nuo 2018 m. kovo 21 d., todėl „Talent“ dar nepalaiko CDS 2.0. Nors CDS 2.0 duomenų bazes peržiūrėti ir kurti galite „PowerApps“ administravimo centre, programoje „Talent“ jos naudojamos nebus. Galimybė naudoti CDS 2.0 aplinkas „Talent“ įdiegtyse bus pasiekiama vėliau.
   
   > [!Note]
   > Kad administravimo portale CDS 1.0 aplinką atskirtumėte nuo 2.0 aplinkos, pasirinkite aplinką ir peržiūrėkite **išsamią informaciją**. Ties visomis CDS 2.0 aplinkomis bus nurodyta, kad „Šiuos parametrus galite tvarkyti „Dynamics 365“ administravimo centre“, nurodę egzemplioriaus versiją, kurioje nėra duomenų bazės skirtuko. 
 
   **Numatytosios „PowerApps“ aplinkos** Nors kiekvienas nuomotojas automatiškai sukonfigūruojamas pagal numatytąją „PowerApps“ aplinką, nerekomenduojame jų naudoti kartu su „Talent“, nes visi vartotojai, kurie yra nuomotojai, turi prieigą prie „PowerApps“ ir bandydami bei naršydami pasitelkiant „PowerApps“ ar srauto integravimus gali netyčia sugadinti jūsų gamybos duomenis.
   
   <strong>Bandomosios versijos aplinkos</strong> Aplinkos, kurių pavadinimas „Bandomoji versija – alias@domain“, kuriamos pritaikant 60 dienų galiojimo laikotarpį ir šiam pasibaigus nebegalios, o jūsų aplinka bus automatiškai pašalinta.
   
   **Nepalaikomi regionai** Šiuo metu „Talent“ palaikoma tik šiuose regionuose: Jungtinėse Amerikos Valstijose, Europoje ir Australijoje.
  
6. Nusprendus, kuri aplinka tinkamiausia naudoti, nereikia imtis jokių konkrečių veiksmų. Tęsti taikant parengimo procesą. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Naujos „PowerApps“ aplinkos kūrimas (jei reikia)

Paleiskite „PowerShell“ scenarijų, kad galėtumėte sukurti naują „Talent“ skirtą „PowerApps“ aplinką tuo atveju, kai nuomotojo administratorius turi „PowerApps“ 2 plano licenciją. Scenarijaus automatizuoja toliau nurodytus veiksmus.


 + „PowerApps“ aplinkos kūrimą
 + CDS 1.0 duomenų bazės kūrimą
 + Visų duomenų pavyzdžių CDS 1.0 duomenų bazėje išvalymą


Norėdami paleisti scenarijų, atlikite toliau pateiktus nurodymus.

1. Atsisiųskite failą „ProvisionCDSEnvironment.zip“, pateikiamą šioje vietoje: [„ProvisionCDSEnvironment“ scenarijai](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Savo atsisiuntimų aplanke dešiniuoju pelės mygtuku spustelėkite ką tik atsiųstą „ProvisionCDSEnvironment.zip“ failą ir pasirinkite **Ypatybės**.  Jei dialogo lango apačioje yra saugumo pastaba, kuri nurodo, kad „Šis failas gautas iš kito kompiuterio ir gali būti užblokuotas, siekiant apsaugoti šį kompiuterį“, pažymėkite žymės langelį **Atblokuoti**, tada spustelėkite **Taikyti** ir **Gerai**.

3. Visą „ProvisionCDSEnviroinment.zip“ failo turinį išskleiskite į aplanką, kuris nėra šakninis aplankas.

4. Paleiskite „Windows PowerShell“ arba „Windows PowerShell ISE“ programą kaip administratorius.

   Peržiūrėkite temą [Vykdymo strategijos nustatymas](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) ir sužinokite daugiau apie tai, kaip nustatyti vykdymo strategiją, kad scenarijai būtų vykdomi. Rekomenduojame naudoti „Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process“, bet būtinai laikykitės jūsų įmonės saugos strategijų ir uždarykite langą „PowerShell“, kai baigsite. 
  
5. „PowerShell“ sistemoje nueikite į aplanką, kuriame išskleidėte failą, ir paleiskite toliau nurodytą komandą, pakeisdami vertes taip, kaip nurodyta toliau.
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   Reikšmę **MyNewEnvironment** pakeiskite įrašydami savo aplinkos pavadinimą. Šis pavadinimas bus rodomas LCS ir matomas tada, kai vartotojai pažymės, kurią „Talent“ aplinką naudoti. 

   Vertę **YourLocation** reikia pakeisti vienu iš regionų, kuriame palaikoma „Talent“: Jungtinės Amerikos Valstijos, Europa, Australija. 

   Vertė **– Daugiažodis** yra pasirinktinė ir įvykus problemai pateiks išsamios informacijos, kurią bus galima nusiųsti palaikymo tarnybai.

6. Tęsti taikant parengimo procesą.
 

## <a name="grant-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas
Pagal numatytuosius nustatymus, aplinką sukūręs visuotinis administratorius turi prie jos prieigą. Tačiau papildomiems programos vartotojams prieiga turi būti aiškiai suteikta. Norėdami suteikti prieigą, [pridėkite vartotojus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ir [jiems priskirkite atitinkamus vaidmenis](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) „Core HR“ aplinkoje. „Talent“ įdiegęs visuotinis administratorius taip pat turi paleisti „Attract“ ir „Onboard“ programas, kad užbaigtų inicijavimą ir suteiktų prieigą kitiems nuomotojams–vartotojams.  Kol tai nebus atlikta, kiti vartotojai neturės priegos prie „Attract“ ir „Onboard“ programų ir matys prieigos pažeidimo klaidas.


