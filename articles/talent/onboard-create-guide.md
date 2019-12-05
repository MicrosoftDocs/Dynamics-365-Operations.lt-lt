---
title: Supažindinimo vadovo kūrimas ir siuntimas, naudojant „Dynamics 365 Talent - Onboard”
description: Šioje temoje paaiškinama, kaip sukurti supažindinimo vadovą savo naujiems darbuotojams, naudojant „Microsoft Dynamics 365 Talent - Onboard” programėlę. Ši užduotis yra esminis pirmas žingsnis žmogiškojo kapitalo valdymo (HCM) nuo įdarbinimo iki atleidimo strategijoje.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a095fe97b05898403b501763204a462ee8dcc12a
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814633"
---
# <a name="create-and-send-an-onboarding-guide-by-using-dynamics-365-talent---onboard"></a>Supažindinimo vadovo kūrimas ir siuntimas, naudojant „Dynamics 365 Talent - Onboard”

[!include [banner](includes/banner.md)]

„Microsoft Dynamics 365 Talent: Onboard” leidžia kurti supažindinimo vadovus pagal šablonus, kuriuos sukūrėte patys, pagal šablonus, prieinamus galerijoje, arba nuo pradžių.

Sukūrę supažindinimo vadovą, galite nusiųsti jį naujam darbuotojui. Taip pat galite nusiųsti jį keliems naujiems darbuotojams, kuriuos turite nurodyti iš „Onboard” programėlės atsisiųstame „Microsoft Excel” faile.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Supažindinimo vadovo sukūrimas pagal šabloną ir jo išsiuntimas naujam darbuotojui

1. Kairiajame meniu pasirinkite **Šablonai**.
2. Dalyje **Mano šablonai** pasirinkite šabloną, kurį norite nustatyti kaip supažindinimo vadovą naujam darbuotojui.
3. Redaguokite šabloną pagal savo pageidavimą. Nepamirškite nuolat įrašyti savo darbo.
4. Baigę redaguoti šabloną, pasirinkite **Kurti vadovą**.

    [![Supažindinimo vadovo kūrimas pagal šabloną](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. Lange **Kurti vadovą**, dalyje **Ką supažindinate?**, įveskite naujo darbuotojo vardą arba el. pašto adresą. Jei naujo darbuotojo dar nėra sistemoje, pasirinkite **Įtraukti dabar** ir įveskite darbuotojo informaciją.

    ![[Informacijos įvedimas į supažindinimo vadovą](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. Dalyje **Kada jie pradeda?**, pasirinkite pradžios datą.
7. Jei supažindinimo vadovas turi būti automatiškai išsiųstas naujam darbuotojui konkrečią datą, įsitikinkite, kad parinktis **Planuoti automatinio siuntimo datą** yra įjungta, o tada pasirinkite automatinio siuntimo datą. Norėdami išsiųsti vadovą iš karto, išjunkite parinktį **Planuoti automatinio siuntimo datą**.
8. Pasirinkite **Atlikta**.
9. Baigę redaguoti supažindinimo vadovą, viršutiniame dešiniajame kampe pasirinkite **Siųsti**. Tuomet atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami naujam darbuotojui nusiųsti supažindinimo vadovo saitą, pasirinkite **Kopijuoti saitą**ir tada pasirinkite **Kopijuoti**.
    - Norėdami tinkinti supažindinimo vadovo el. paštą prieš jį siųsdami, pasirinkite **Tinkinti el. laišką prieš siunčiant**, pasirinkite **Pirmyn**, tinkinkite el. paštą pagal savo pageidavimą ir tada pasirinkite **Siųsti**.
    - Norėdami siųsti el. laišką jo netinkindami, pasirinkite **Pirmyn**, tada pasirinkite **Siųsti**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Supažindinimo vadovo kūrimas pagal šabloną ir jo išsiuntimas keliems naujiems darbuotojams

„Onboard” leidžia siųsti supažindinimo vadovą keliems naujiems nuomininkams tuo pačiu metu.

1. Kairiajame meniu pasirinkite **Šablonai**.
2. Dalyje **Mano šablonai** pasirinkite šabloną, kurį norite nustatyti kaip supažindinimo vadovą naujiems darbuotojams.
3. Redaguokite šabloną pagal savo pageidavimą. Nepamirškite nuolat įrašyti savo darbo.
4. Baigę redaguoti šabloną, pasirinkite **Kurti vadovą**.
5. Lange **Sukurti vadovą** pasirinkite **Reikia supažindinti kelis žmones vienu metu?**.

    [![Supažindinimo vadovo, skirto keliems naujiems darbuotojams, kūrimas](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Pasirinkite **naujo darbuotojo šabloną**.
7. Atsisiuntę .xlsx failą, pasirinkite **Atidaryti**, įveskite darbuotojų informaciją „Excel” darbaknygėje ir įrašykite darbaknygę.

    [![„Excel” šablono, skirto siųsti supažindinimo vadovą keliems naujiems darbuotojams, atsisiuntimas](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Kad galėtumėte redaguoti darbaknygę, turite pasirinkti **Įgalinti redagavimą** „Excel”.
    > 
    > [![Įgalinti redagavimą](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Nuvilkite „Excel” darbaknygę į paskirtą sritį lange **Kurti kelis vadovus** arba spustelėkite bet kurioje tos srities vietoje, kad surastumėte failą kompiuteryje.

    [![Redaguotos darbaknygės vilkimas](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Baigę redaguoti supažindinimo vadovą, viršutiniame dešiniajame kampe pasirinkite **Siųsti**. Tuomet atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami naujiems darbuotojams nusiųsti supažindinimo vadovo saitą, pasirinkite **Kopijuoti saitą**ir tada pasirinkite **Kopijuoti**.
    - Norėdami tinkinti supažindinimo vadovo el. paštą prieš jį siųsdami, pasirinkite **Tinkinti el. laišką prieš siunčiant**, pasirinkite **Pirmyn**, tinkinkite el. paštą pagal savo pageidavimą ir tada pasirinkite **Siųsti**.
    - Norėdami siųsti el. laišką jo netinkindami, pasirinkite **Pirmyn**, tada pasirinkite **Siųsti**.

## <a name="create-a-guide-without-using-a-template"></a>Kurti vadovą nenaudojant šablono

Jums ne visada reikia kurti vadovą pagal šabloną. Jei pageidaujate, galite kurti vadovą nuo nulio.

1. Kairiajame meniu pasirinkite **Vadovai**, tada pasirinkite mygtuką **Įtraukti** (pliuso ženklą \[**+**\]).
2. Lange **Kurti vadovą**, dalyje **Ką supažindinate?**, įveskite naujo darbuotojo vardą arba el. pašto adresą. Jei naujo darbuotojo dar nėra sistemoje, pasirinkite **Įtraukti dabar** ir įveskite darbuotojo informaciją.

    ![[Informacijos įvedimas į supažindinimo vadovą](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. Dalyje **Kada jie pradeda?**, pasirinkite pradžios datą.
4. Jei supažindinimo vadovas turi būti automatiškai išsiųstas naujam darbuotojui konkrečią datą, įsitikinkite, kad parinktis **Planuoti automatinio siuntimo datą** yra įjungta, o tada pasirinkite automatinio siuntimo datą. Norėdami išsiųsti vadovą iš karto, išjunkite parinktį **Planuoti automatinio siuntimo datą**.
5. Pasirinkite **Atlikta**.

## <a name="save-a-guide-as-a-template"></a>Vadovo kaip šablono įrašymas

Galite įrašyti supažindinimo vadovą kaip šabloną. Tokiu būdu galite sutaupyti laiko, jei vėliau turite sukurti daugiau supažindinimo vadovų.

1. Kairiajame meniu pasirinkite **Vadovai**.
2. Pasirinkite mygtuką **Daugiau** (daugtaškis \[**...**\]) vadove, kurio šabloną norite sukurti, tada pasirinkite **Įrašyti kaip šabloną**.

    ![[Supažindinimo vadovo kaip šablono įrašymas](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. Lange **Įrašyti kaip naują šabloną** įveskite naujojo šablono pavadinimą, tada pasirinkite **Įrašyti**.

## <a name="next-steps"></a>Kiti veiksmai

- [Supažindinimo vadovų ir šablonų redagavimas](./onboard-edit-guides-templates.md)
- [Turinio bendrinimas su kitais bendraautoriais](./onboard-share-template.md)
- [Užduočių ir darbuotojų supažindinimo būsenos peržiūra](./onboard-view-status.md)
- [Samdos komandų kūrimas „Onboard”](./onboard-create-team.md)

### <a name="see-also"></a>Taip pat žiūrėkite

- [Išbandykite arba įsigykite „Onboard” programėlę](https://dynamics.microsoft.com/talent/onboard/)
- [Kas nauja arba pasikeitė „Dynamics 365 Talent“](./whats-new.md)
- [Leidimo planai](https://docs.microsoft.com/business-applications-release-notes/index)
- [Palaikymo dėl „Microsoft Dynamics 365 Talent“ gavimas](./talent-support.md)
