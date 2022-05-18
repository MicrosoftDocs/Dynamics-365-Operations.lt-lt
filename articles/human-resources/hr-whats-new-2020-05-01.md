---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 1 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. gegužės 1 d.
author: andreabichsel
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eedc89be0bbcd92f541c57fb1f99a04e8706eafd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689360"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 1 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3196 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Nauji našumo valdymo objektai, pasiekiami duomenų valdymo sistemoje (DMF)

Dabar galimi tolesni objektai. Jei šių objektų nematote objektų sąraše, naudokite parinktį **Atnaujinti objektus** dalyje **Sistemos parametrai > Objekto parametrai > Atnaujinti objektų sąrašą**.

- **Diskusijų kompetencija**
- **Diskusijų tikslai**
- **Diskusijų matavimas**
- **Diskusijų tema**
- **Efektyvumo žurnalas**
- **Matas**
- **Tikslo matavimas**

Be to, į objektą **Diskusija** buvo įtraukti **Bendras rezultatas** ir **Vidutinis rezultatas**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Atostogų užklausos komentarų ilgio didinimas (275641)

Atostogų užklausos komentaruose dabar galima įvesti daugiau nei 100 simbolių.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Baigiamieji apžvalgų komentarai nerodomi, kai vadovas arba darbuotojas yra prisijungęs prie kitos įmonės (431688)

Peržiūrint atsiliepimus bus rodomi visi komentarai.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Vartotojo nustatytos nuorodos nepalaikomos naujoje darbininko formoje (390374)

Vartotojo nustatytos nuorodos dabar įjungtos supaprastintoje formoje **Darbininkas**.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>„HcmRatingLevelEntity” sukelia „OData” API gedimą (439476)

Šis pakeitimas ištaiso API gedimą. Dublikato pavadinimas įrašo šią klaidą.

## <a name="in-preview"></a>Peržiūros režimu

## <a name="leave-suspension"></a>Atostogų sustabdymas

Programoje „Human Resources” galite sustabdyti darbuotojo atostogas ir neatvykimą. Atostogų sustabdymas sustabdo pasirinktų atostogų tipų atostogų kaupimus. Jei sustabdymas įvyksta po to, kai kaupimas buvo apdorotas, atostogų sustabdymas sukuria proporcingai paskirstytą darbuotojo atostogų balanso koregavimą. Daugiau informacijos žr. [Atostogų sulaikymas](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Vartotojo patirties naujinimas nurodyti, jog kaupimas sustabdytas (429550)

Dabar vartotojo patirtis nurodo, kad plano kaupimas buvo sustabdytas.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Nurodytų atostogų tipų atostogų kaupimo sustabdymas (272447)

Šiame leidime personalas gali sukurti taisyklę, skirtą sustabdyti darbuotojų, įvedusių atostogų užklausas neapmokamoms atostogoms, atostogų kaupimus. Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma. Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF objektas pasiekiamas kaupimo sustabdymams (429549)

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Priežasties kodo įtraukimas į kaupimo sustabdymus (429547)

Į kaupimo sustabdymus įtraukti priežasties kodai.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Perėjimo iš „Human Resources“ parametrų į atostogų ir neatvykimų parametrus pradžia

Šiame leidime pradedama jungti „Human Resources“ parametrus su atostogų ir neatvykimų parametrais.

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Žinomos problemos

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>„SharePoint“ peržiūra neveikia kai kuriose aplinkose

Jei dokumentų peržiūra, skirta dokumentams, saugomiems „SharePoint“, neveikia, bandykite atlikti tolesnę procedūrą.

1. Patikrinkite, ar administratoriaus vartotojo paskyra turi el. pašto adresą, susietą su vartotojo įrašu. Šią informaciją galima peržiūrėti puslapyje **Vartotojas**. Jei el. pašto adresas nenustatytas, turite įtraukti el. pašto adresą ir tiekėją naudodami „OData Excel“ papildinį. Pagal numatytuosius parametrus, „Excel“ dizaine nėra el. pašto adreso. Turėsite redaguoti „Excel“ dizainą, įtraukti visus laukus, taikyti ir atnaujinti. Atlikę šiuos veiksmus, galėsite naujinti administratoriaus paskyrą.

2. Susieję administratoriaus paskyrą su el. pašto paskyra, prisijunkite prie „Human Resources“ naudodami administratoriaus kredencialus.

3. Atidarykite priedą „SharePoint“, kad pradėtumėte dokumento peržiūrą.

4. Prisijunkite su kito vartotojo paskyra, kuri turi prieigą prie priedų, ir patikrinkite, ar peržiūra veikia kaip numatyta.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]