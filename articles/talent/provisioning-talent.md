---
title: "„Microsoft Dynamics 365 for Talent“ parengimas"
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
ms.sourcegitcommit: 8b59ea6a2ac8c1c4e5df6e251fa3390639ff3f30
ms.openlocfilehash: e6266ef5890b5caaf33db76eeccfc8a7a6888a11
ms.contentlocale: lt-lt
ms.lasthandoff: 03/02/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>„Microsoft Dynamics 365 for Talent“ parengimas

[!include[banner](includes/banner.md)]

[!include[banner](includes/banner.md)]

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
2. „Talent“ visada paruošta „Microsoft PowerApps“ aplinkai, siekiant įgalinti „PowerApps“ integravimą ir išplečiamumą. Jei dar neturite „PowerApps“ aplinkos, prieš tęsdami atlikite veiksmus, nurodytus šios temos dalyje „Naujos „PowerApps“ aplinkos kūrimas (jei reikia)“.

    > [!NOTE]
    > Norėdami peržiūrėti esamas aplinkas arba kurti naujas aplinkas, nuomotojo administratoriui, kuris paruošia „Talent“, turi būti priskirta „PowerApps“ P2 licencija. Jei jūsų organizacija neturi „PowerApps“ P2 licencijos, galite ją gauti iš savo CSP arba [„PowerApps“ kainų puslapyje](https://powerapps.microsoft.com/en-us/pricing/).

3. Pasirinkite **Įtraukti**, tada pasirinkite aplinką, kuriai norite paruošti „Talent“.
4. Pasirinkite **Taip**, kad sutiktumėte su sąlygomis ir pradėtumėte diegimą.

    Nauja aplinka pasirodo aplinkų sąraše, kuris yra naršymo srityje, esančioje kairėje. Tačiau negalite pradėti naudoti aplinkos, kol diegimo būsena nebus atnaujinta į **Įdiegta**. Paprastai šis procesas užtrunka tik keletą minučių. Jei parengimo procesas nepavyksta, privalote susisiekti su palaikymo tarnyba.

6. Pasirinkite **Prisijungti prie „Talent“**, kad galėtumėte naudoti naująją aplinką.

> [!NOTE]
> Jei dar nesate patvirtinę galutinių reikalavimų, projekte galite įdiegti „Talent“ bandymo egzempliorių. Tada galite naudoti šį egzempliorių, kad išbandytumėte sprendimą, kol patvirtinsite. Jei naudojate naują aplinką bandymams, turite pakartoti šią procedūrą norėdami sukurti gamybos aplinką.

> [!NOTE]
> Per LCS parengiamoje „Talent“ aplinkoje nėra demonstracinių duomenų, kurie sukonfigūruojami žmogiškųjų išteklių (HR) užduotims, arba kurie yra skirti konkrečiai „Talent“.  Jei jums reikia aplinkos, kurioje būtų demonstraciniai duomenys, rekomenduojame užsiregistruoti nemokamai 60 dienų [„Talent“ bandomajai aplinkai](https://dynamics.microsoft.com/en-us/talent/overview/). Bandomoji aplinka priklauso tam vartotojui, kuris ją užsakė, bet galima pakviesti ir kitus vartotojus per „Core HR“ sistemos administravimo patirtį. Bandomosiose aplinkose pateikti išgalvoti duomenys, kuriais naudojantis galima saugiai tyrinėti programą. Jos nėra skirtos naudoti kaip gamybos aplinkos. Atkreipkite dėmesį, kad kai bandomosios aplinkos naudojimo terminas baigiasi po 60 dienų, visi joje esantys duomenys panaikinami ir jų nebegalima susigrąžinti. Pasibaigus dabartinės aplinkos naudojimo terminui, galite užsiregistruoti naujai bandomajai aplinkai.

## <a name="create-a-new-powerapps-environment-if-required"></a>Naujos „PowerApps“ aplinkos kūrimas (jei reikia)
„Talent“ ir „PowerApps“ aplinkų integracija leidžia integruoti ir išplėsti „Talent“ duomenų naudojimą „PowerApps“ priemonėmis. „PowerApps“ aplinkų paskirties supratimas padės kurti programas, atitinkančias jūsų „Talent“ išplėtimo poreikius. Norėdami gauti daugiau informacijos apie „PowerApps“ aplinkas, įskaitant aplinkų aprėptį, prieigą prie jų ir aplinkų kūrimą bei pasirinkimą, žr. [„PowerApps“ aplinkų paskelbimas](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Kiekvienam nuomotojui automatiškai parengiama numatytoji „PowerApps“ aplinka, tačiau tai gali būti ne pati geriausia aplinka jūsų „Talent“ diegimui. Atliekant šį veiksmą, reikėtų atsižvelgti į integravimo ir bandymo strategijas, todėl rekomenduojame įvertinti galimus padarinius jūsų diegimui, nes vėliau kai kuriuos sprendimus pakeisti nebus lengva. 

Kiekvienas nuomotojas automatiškai parengiamas numatytojoje „PowerApps“ aplinkoje, tačiau ši aplinka gali būti ne pati geriausia jūsų „Talent“ diegimui. Duomenų integravimo ir bandymo strategijas reikia įvertinti atliekant šį veiksmą. Todėl rekomenduojame įvertinti įvairius diegimo padarinius, nes vėliau pakeisti „PowerApps“ aplinką nėra lengva.

1. LCS pasirinkite **Valdyti aplinkas**. Būsite nukreipti į [„PowerApps“ administravimo centras](https://preview.admin.powerapps.com/environments), kur galite peržiūrėti esamas ir kurti naujas aplinkas.
2. Pasirinkite **Nauja aplinka**.
3. Įveskite unikalų aplinkos pavadinimą ir pasirinkite vietą, kurioje norite diegti.

    > [!NOTE]
    > Kai kuriuose regionuose „Talent“ nepasiekiama. Todėl prieš pasirinkdami vietą aplinkai būtinai patikrinkite pasiekiamumą.

4. Kai jūsų paklaus, ar norite sukurti duomenų bazę, pasirinkite **Kurti duomenų bazę**, kad sukurtumėte „Common Data Service“ (CDS) duomenų bazę, kuri turi nuomoti išteklius daliai „Talent“ duomenų. Sukurdami duomenų bazę, taip pat galite integruoti „PowerApps“ su „Talent“.
5. Būsite paprašyti pasirinkti prieigos lygį, kurį norite taikyti duomenų bazei. Rekomenduojame pasirinkti **Apriboti prieigą**, nes ši parinktis neleidžia „Talent“ vartotojams tiesiogiai pasiekti slaptų duomenų naudojant „PowerApps“ programą.
6. Sukurtoje CDS duomenų bazėje pateikiami demonstraciniai duomenys, kurie į jūsų gamybos aplinką įtraukia neaktyvius darbuotojus, išgalvotus adresus ir kitą informaciją. Norėdami pašalinti demonstracinius duomenis, baigę kurti CDS duomenų bazę atlikite šiuos veiksmus:

    > [!IMPORTANT]
    > Jei anksčiau sukūrėte CDS duomenų bazę ir į ją įvedėte kokius nors įmonės gamybos duomenis, šie veiksmai pašalins **visus** duomenis pasirinktoje duomenų bazėje, net įmonės gamybos duomenis.

    1. Prisijunkite prie [„PowerApps“](https://preview.web.powerapps.com/home).
    2. Viršutiniame dešiniajame kampe esančiame išplečiamajame sąraše pasirinkite aplinką, kurią sukūrėte 2 veiksme.
    3. Kairėje esančioje naršymo srityje išplėskite **„Common Data Service“** ir pasirinkite **Objektai**.
    4. Puslapio dešinėje pusėje pasirinkite daugtaškio (**…**) mygtuką, tada pasirinkite **Išvalyti visus duomenis**.
    5. Pasirinkite **Panaikinti duomenis**, kad patvirtintumėte, jog norite pašalinti duomenis. Šis veiksmas pašalina visus demonstracinius duomenis, įtrauktus į CDS pagal numatytuosius parametrus. Jis taip pat pašalina visus kitus duomenis, įvestus pasirinktoje duomenų bazėje.

Dabar galite naudoti naująją aplinką.

## <a name="grant-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas
Pagal numatytuosius nustatymus, aplinką sukūręs visuotinis administratorius turi prie jos prieigą. Tačiau papildomiems programos vartotojams prieiga turi būti aiškiai suteikta. Norėdami suteikti prieigą, [pridėkite vartotojus](../dev-itpro/sysadmin/tasks/create-new-users.md) ir [jiems priskirkite atitinkamus vaidmenis](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) „Core HR“ aplinkoje. Be to, šiuos vartotojus būtina įtraukti į „PowerApps“ aplinką, kad jie galėtų naudoti „Attract“ ir „Onboard“ programas. Ši procedūra pateikta čia. Jei jums reikia pagalbos šiems veiksmams atlikti, žr. tinklaraščio įrašą [„PowerApps“ administravimo centro pristatymas](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Šią procedūrą atlieka visuotinis administratorius, kuris įdiegė „Talent“ aplinką.

1. Atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/environments).
2. Pasirinkite atitinkamas aplinkas.
3. Skirtuke **Sauga** prie vaidmens **Aplinkos kūrėjas** pridėkite reikiamus vartotojus.

Atkreipkite dėmesį, kad šis paskutinis veiksmas, kuriuo rankiniu būdu pridedate vartotojus į „PowerApps“ aplinką, yra laikinas. Galiausiai jis bus atliktas automatiškai, kai vartotojai bus pridėti prie „Core HR“.

