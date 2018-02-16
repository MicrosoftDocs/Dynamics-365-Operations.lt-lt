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
ms.sourcegitcommit: a53c1997f74ebe572b17cc3090d2e236b6fe78f6
ms.openlocfilehash: 8a84cfe9b73f0c72f3cb0c3843749754c6b3d538
ms.contentlocale: lt-lt
ms.lasthandoff: 01/31/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>„Microsoft Dynamics 365 for Talent“ parengimas
Šioje temoje pateikiami veiksmai, skirti paruošti naują aplinką programai „Microsoft Dynamics 365 for Talent“. Šioje temoje laikoma, kad įsigijote „Talent“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. Jei turite esamą „Microsoft Dynamics 365“ licenciją, kurioje jau yra „Talent“ paslaugos planas, ir negalite atlikti šioje temoje nurodytų veiksmų, susisiekite su palaikymo tarnyba.

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

    Nauja aplinka pasirodo aplinkų sąraše, kuris yra naršymo srityje, esančioje kairėje. Tačiau negalite pradėti naudoti aplinkos, kol diegimo būsena nebus atnaujinta į **Įdiegta**. Paprastai šis procesas užtrunka tik keletą minučių. Jei paruošti nepavyksta, turite susisiekti su palaikymo tarnyba.

6. Pasirinkite **Prisijungti prie „Talent“**, kad galėtumėte naudoti naująją aplinką.

> [!NOTE]
> Jei dar nesate patvirtinę galutinių reikalavimų, projekte galite įdiegti „Talent“ bandymo egzempliorių. Tada galite naudoti šį egzempliorių, kad išbandytumėte sprendimą, kol patvirtinsite. Jei naudojate naują aplinką bandymams, turite pakartoti šią procedūrą norėdami sukurti gamybos aplinką.

## <a name="create-a-new-powerapps-environment-if-required"></a>Naujos „PowerApps“ aplinkos kūrimas (jei reikia)

„Talent“ integravimo su „PowerApps“ aplinkomis vizija – įgalinti duomenų integravimo funkciją ir plėtinių srautus be „Talent“ duomenų naudojant „PowerApps“ įrankius. Todėl, renkantis su „Talent“ naudotiną aplinką, svarbu suprasti „PowerApps“ aplinkų paskirtį. Norėdami gauti daugiau informacijos apie „PowerApps“ aplinkas, įskaitant aplinkų aprėptį, prieigą prie jų ir aplinkų kūrimą bei pasirinkimą, žr. [„PowerApps“ aplinkų paskelbimas](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).  Nors kiekvienas nuomotojas yra automatiškai sukonfigūruotas numatytojoje „PowerApps“ aplinkoje, ji gali būti ne pati geriausia aplinka naudoti su jūsų visuotine „Talent“ įdiegtimi. Atliekant šį veiksmą, reikėtų atsižvelgti į integravimo ir bandymo strategijas, todėl rekomenduojame apsvarstyti įvairius padarinius jūsų visuotinei įdiegčiai, nes vėliau tą pakeisti nelengva.

1. LCS pasirinkite **Aplinkų valdymas**. Būsite nukreipti į [„PowerApps“ administravimo centras](https://preview.admin.powerapps.com/environments), kur galite peržiūrėti esamas ir kurti naujas aplinkas.
2. Pasirinkite mygtuką (**+**) **Nauja aplinka**.
3. Įveskite unikalų aplinkos pavadinimą ir pasirinkite vietą, kurioje norite diegti.

    > [!NOTE]
    > Kai kuriuose regionuose „Talent“ nepasiekiama. Todėl prieš pasirinkdami vietą aplinkai būtinai patikrinkite pasiekiamumą.

4. Kai jūsų paklaus, ar norite sukurti duomenų bazę, pasirinkite **Kurti duomenų bazę**, kad sukurtumėte „Common Data Service“ (CDS) duomenų bazę, kuri turi nuomoti išteklius daliai „Talent“ duomenų. Sukurdami duomenų bazę, taip pat galite integruoti „PowerApps“ su „Talent“.
5. Būsite paprašyti pasirinkti prieigos lygį, kurį norite naudoti duomenų bazėje. Rekomenduojame pasirinkti **Apriboti prieigą**, nes ši parinktis neleidžia „Talent“ vartotojams tiesiogiai pasiekti slaptų duomenų naudojant „PowerApps“ programą.
6. Sukurtoje CDS duomenų bazėje yra demonstraciniai duomenys. Šie demonstraciniai duomenys naudingi, nes bandymams galite naudoti demonstracinių duomenų įmonę arba kurti užduočių įrašus ar užduočių vadovus. Tačiau demonstraciniai duomenys į jūsų gamybos aplinką įtraukia neaktyvius darbuotojus, išgalvotus adresus ir kitą informaciją. Norėdami pašalinti demonstracinius duomenis, baigę kurti CDS duomenų bazę atlikite šiuos veiksmus:

    > [!IMPORTANT]
    > Jei anksčiau sukūrėte CDS duomenų bazę ir į ją įvedėte kokius nors įmonės gamybos duomenis, turėkite omenyje, kad šie veiksmai pašalins **visus** duomenis pasirinktoje duomenų bazėje, net įmonės gamybos duomenis.

    1. Prisijunkite prie [„PowerApps“](https://preview.web.powerapps.com/home) ir dešinėje puslapio pusėje esančiame išplečiamajame meniu pasirinkite aplinką, kurią sukūrėte 2 veiksmu.
    2. Kairėje naršymo srityje išplėskite **„Common Data Service“** ir pasirinkite **Objektai**.
    3. Puslapio dešinėje pusėje pasirinkite daugtaškio (**…**) mygtuką, tada pasirinkite **Išvalyti visus duomenis**.
    4. Pasirinkite **Panaikinti duomenis**, kad patvirtintumėte, jog norite pašalinti duomenis. Šis veiksmas pašalina visus demonstracinius duomenis, įtrauktus į CDS pagal numatytuosius parametrus. Jis taip pat pašalina visus kitus duomenis, įvestus pasirinktoje duomenų bazėje.
    
Dabar galite naudoti naująją aplinką.

## <a name="granting-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas
Pagal numatytuosius parametrus prieigą turės aplinką sukūręs visuotinis administratorius, tačiau papildomiems programos vartotojams prieiga turi būti suteikiama atskirai. Tai galima padaryti [įtraukiant vartotojų](../dev-itpro/sysadmin/tasks/create-new-users.md) ir [jiems priskiriant atitinkamus vaidmenis](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) „Core HR“ aplinkoje. Be to, šiuos vartotojus būtina įtraukti į „PowerApps“ aplinką, kad jie galėtų pasiekti „Attract“ ir „Onboard“ programas.  Padėti atlikti šiuos veiksmus, kurie išdėstyti toliau, jums gali tinklaraščio įrašas [„PowerApps“ administravimo centro pristatymas](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

> 1.    Visuotinis administratorius, visuotinai įdiegęs „Talent“ aplinką, turi nueiti į [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/environments).   
> 2.    Pasirinkite reikiamą (-as) aplinką (-as).
> 3.    Skirtuke Sauga vaidmeniui Aplinkos kūrėjas priskirkite reikiamus vartotojus.

Atkreipkite dėmesį, kad šis paskutinis vartotojų įtraukimo į „PowerApps“ aplinką veiksmas yra laikinas. Ilgainiui įtrauksime funkciją, kad tai būtų galima atlikti automatiškai, vartotoją įtraukus į „Core HR“.


