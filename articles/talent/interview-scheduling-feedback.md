---
title: Pokalbio planavimas ir atsiliepimas
description: Šioje temoje pateikiama informacija apie pokalbio planavimo ir atsiliepimų veiklas „Attract“.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2019
ms.locfileid: "374947"
---
# <a name="interview-scheduling-and-feedback"></a>Pokalbio planavimas ir atsiliepimas

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Duomenų apsikeitimo valdymo veikla

Planuotojo veikla yra pasirinktinė ir ją sudaro du komponentai: kandidato pasiekiamumo užklausa ir grafikas. Kandidatas pasiekiamumo komponentas suteikia galimybę naudoti el. paštą ir prašyti informacijos apie kandidato pasiekiamumą. Grafiko komponentas suteikia galimybę planuoti pokalbius su kandidatas ir samdos komanda.

### <a name="candidate-availability-request"></a>Kandidato pasiekiamumo užklausa

Norėdami kandidatams siųsti el. laiškus ir prašyti informacijos apie jų pasiekiamumą, pasirinkite lauką **Prašyti informacijos apie kandidato pasiekiamumą**. Jei laukas nebus pasirinktas, šis veiksmas nebus rodomas darbo samdos procese.

Norėdami siųsti pasiekiamumo užklausą, spustelėkite **Siųsti užklausą**, pasirinkite galimas datas ir el. laiško šabloną, tada išsiųskite el. laišką kandidatui.

[![„Attract“ įdarbintojo rodinys, iš kurio siunčiama kandidavo pasiekiamumo užklausa](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Kai kandidatas gauna el. laišką, nurodantį atsakyti į užklausą, jis gali prisijungti prie savo kandidato portalo, pasirinkti datas, kurios atitinka jo pasiekiamumą, ir spustelėti **Pateikti**.

### <a name="schedule"></a>Tvarkaraštis
Pokalbio planuotojas gali naudoti kelias konfigūracijas ir kurti bei siųsti pokalbio informaciją kalbintojams ir kandidatui.

1. Spustelėkite **Kurti grafiką** ir laukelyje **Įtraukti kalbintojų** išvardyti visus kalbintojus, kurie bus įtraukti į pokalbio informacijos siuntimo procesą.
[![„Attract“ įdarbintojo rodinys, iš kurio pradedamas planuoti pokalbio informacijos siuntimo procesas](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Jei kandidatas atsakė į pokalbio pasiekiamumo užklausą, lauke **Pokalbio data** bus įvesta jo pasirinkta reikšmė. Jei reikia, galite pasirinkti kitą datą.
    
    Jei pasirenkate lauką **Šį pokalbį padaryti grupiniu**, kairėje pateiktų kalbintojų grupė perkeliama į vieną pokalbio informacijos grupę, kad būtų sukurtas pokalbis. Tada turėsite nurodyti konkrečią pokalbių seką.
    
    Pokalbio grafikas turėtų būti sudarytas taip, kad kuo labiau atitiktų dalyvių pasiekiamumą. Jei tai yra vidinis kandidatas, jo pasiekiamumą galite įtraukti kaip grafiko rekomendacijos dalį.
    
    Norėdami organizuoti susitikimą internetu, pasirinkite **Įtraukti „Skype“ susitikimų** ir prie kiekvieno pokalbio įvykio bus pateiktas saitas **„Skype“ verslui**.

2. Pasirinkite kiekvieno pokalbio įvykio pokalbio trukmę, o tada spustelėkite **Gerai**, kad pradėtumėte kurti grafiką.

    Jei pasirinktos **Rekomendacijos**, bus rodomi pasiūlymai ir pokalbio tinklelis bus iš anksto užpildytas. Galėsite matyti dabartinio kalendoriaus visų pasirinktų kalbintojų pasiekiamumą. Taip pat galėsite peržiūrėti kandidato kalendorių, jei jis yra vidinis kandidatas.

3. Jei pasiūlymų nėra, stulpelyje **Kalbintojai** spustelėkite laiko intervalą, pateikite pokalbio pavadinimą, informaciją ir įveskite vietos informaciją, jei reikia. Galite pasirinkti įtraukti pokalbio saitą **„Skype“ verslui**.

4. Norėdami įtraukti papildomų kalbintojų, spustelėkite tinklelio stulpelį **Įtraukti pokalbį**, kad pasirinktumėte vieną arba kelis kalbintojus. Galite naudoti daugtaškio (...) parinktį, kad pašalintumėte kalbintoją iš pokalbio informacijos siuntimo proceso.
    
5. Jei pokalbiai suplanuoti skirtingose laiko juostose, pasirinkite reikiamą miesto / laiko juostą iš išplečiamojo sąrašo viršutiniame dešiniajame kampe. Kalbintojo pasiekiamumo tinklelis bus atnaujintas, atsižvelgiant į naują laiko juostą. Šis laiko juostos pasirinkimas dabar taip pat bus rodomas rodinyje **Pokalbio suvestinė**, kuris bus bendrinamas su kalbintojais ir kandidatu. 

6. Spustelėkite **Siųsti kalbintojams**, kad išsiųstumėte pakvietimus į susitikimą susijusiems kalbintojams.

    Išsiuntus pokalbio užklausas kalbintojams, jie gali atsakyti tiesiogiai iš gauto el. laiško pakvietimo.

    >[!NOTE]
    > Individualūs pokalbiai: kalbintojams kas 24 valandas siunčiami priminimai, jei kalbintojas neatsakė į pokalbio užklausą (nepriėmė ir neatmetė).

    > Grupės pokalbiai: nėra jokių automatinių priminimų dėl pokalbio užklausos. Norėdami rankiniu būdu suaktyvinti priminimą, redaguokite pokalbį ir naudokite parinktį **Atnaujinti ir siųsti**, kad nusiųstumėte užklausą kalbintojams.

    Kalbintojų atsakymai užfiksuojami ir rodomi „Attract“. Jei kalbintojas atmeta pakvietimą, jums bus pranešta atlikti pakeitimą. Norėdami peržiūrėti jų atsakymus, tinklelio rodinyje **Duomenų apsikeitimo valdymas** spustelėkite burbulo piktogramą.

[![„Attract“ įdarbintojo rodinys, kuriame rodomas kalbintojo atsakymas](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Kai pokalbio grafikas yra paruoštas bendrinti su kandidatu, spustelėkite **Siųsti kandidatui**. Galite nuo kandidato slėpti arba jam rodyti kalbintojų vardus ir vietas.

8. Pasirinkite el. laiško šabloną ir siųskite pokalbio suvestinę kandidatui. Kandidatas šią informaciją gali peržiūrėti savo el. pašte, taip pat – savo kandidato portale.
    
>[!NOTE] 
> Kandidato kalendoriaus pasiekiamumas rodomas tik jei kandidatas yra vidinis. Taip pat tik vidinius kandidatus galima naudoti norint pagerinti pokalbio grafiko rekomendacijas. Šiuo metu kandidatai (išoriniai arba vidiniai) negauna pakvietimo į susitikimą el. laiško – kandidatas gauna tik pokalbių suvestinę.

## <a name="feedback-activity"></a>Atsiliepimo veikla

Atsiliepimo veikla užduoties šablone yra pasirinktinė. Ši veikla suteikia galimybę pokalbio dalyviams įvesti rekomendacijas arba atsiliepimo komentarus, skirtus pretendentui. Jei pasirenkamas laukas **Gauti atsiliepimų dalyvius iš samdos komandos**, įdarbintojas, samdos vadovas ir kalbintojai automatiškai įvedami atsiliepimo veikloje. Organizacijos gali leisti kalbintojams peržiūrėti kitų žmonių atsiliepimus prieš pateikiant savo atsiliepimus. Organizacijos taip pat gali leisti kalbintojams redaguoti savo atsiliepimą, kai jis pateiktas. Naudojant užduoties šabloną kalbintojams primenama pateikti atsiliepimus už pokalbius, kuriuos jie neseniai vedė, atsižvelgiant į iš anksto nustatytą konfigūraciją. Samdos vadovas arba įdarbintojas taip pat gali užduotyje pasirinkti neautomatiškai priminti kalbintojui pateikti atsiliepimą.

## <a name="interview-activity"></a>Pokalbio veikla

Pokalbio veikla yra neprivaloma veikla, kurią sudaro trys komponentai: kandidato pasiekiamumo užklausa, grafikas ir atsiliepimas. Naudokite pokalbio veiklą užduoties šablone, jei norite kandidato pasiekiamumo užklausą, grafiką ir atsiliepimą sujungti į vieną procesą, o ne naudoti šiuos elementus atskirai samdos proceso metu.
