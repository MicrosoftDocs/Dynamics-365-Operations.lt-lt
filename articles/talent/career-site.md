---
title: „Attract“ karjeros svetainės funkcijos
description: Šioje temoje pateikiama „Attract“ kandidatams skirtos karjeros svetainės funkcijos apžvalga.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/13/2019
ms.locfileid: "389976"
---
# <a name="career-site-functionality-in-attract"></a>„Attract“ karjeros svetainės funkcijos

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 for Talent: Attract“ kandidatams skirtos karjeros svetainės funkcijos apžvalga. Joje taip pat paaiškinama, kaip šią funkciją nustatyti.

„Attract“ suteikia vieną karjeros svetainę kiekvienai nuomotojo aplinkai. Pvz., jei organizacija naudoja kūrimo aplinką ir tikrinimo aplinką, viena karjeros svetainė skiriama kūrimo aplinkai, o kita karjeros svetainė skiriama tikrinimo aplinkai. Kiekviena karjeros svetainė yra visiškai atskira ir joje veikia atskiras autentifikavimo mechanizmas. Darbai ir kandidatų profiliai nėra bendrinami karjeros svetainėse.

Pagal numatytuosius parametrus karjeros svetainė yra vieša. Todėl kandidatai neprisijungę gali peržiūrėti visas užduotis, kurios pažymėtos kaip išorinės. Tačiau, norėdami atlikti visus kitus veiksmus, kandidatų turi prisijungti.

## <a name="career-site-management"></a>Karjeros svetainės valdymas

Norėdami nustatyti toliau nurodytų elementų reikšmes, prisijunkite prie „Attract“ kaip administratorius, pasirinkite parinktį **Administravimo centras**. pateiktą meniu **Parametrai** (krumpliaračio simbolis), tada pasirinkite skirtuką **Įmonės informacija**.

-   **Organizacijos pavadinimas:** organizacijos pavadinimas rodomas karjeros svetainės naršymo juostos viršuje. Pasirinkdami organizacijos pavadinimą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.

-   **Organizacijos logotipas:** organizacijos logotipo vaizdas rodomas viršutiniame kairiajame karjeros svetainės kampe. Pasirinkdami organizacijos logotipo vaizdą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.

    >   [!NOTE] 
    >   Logotipo vaizdo, kuris rodomas karjeros svetainėje, aukštis yra fiksuotas – 20 pikselių (piks.). Vaizdo, kurį įtraukiate į administravimo centrą, dydis atitinkamai pritaikomas. Todėl, priklausomai nuo vaizdo, plotis gali keistis.
 
Norėdami nustatyti toliau nurodytų elementų reikšmes, prisijunkite prie „Attract“ kaip administratorius, pasirinkite parinktį **Administravimo centras**, pateiktą meniu **Parametrai**, tada pasirinkite skirtuką **Karjeros svetainės valdymas**.

-   **Ieškos mechanizmo optimizavimas** - įjungus, visų viešų darbų, paskelbtų „Attract“ karjeros svetainėje, bus galima ieškoti naudojant ieškos mechanizmus, pvz., „Bing“ ir „Google“.

    >   [!NOTE] 
    >   Įjungus šį parametrą ieškos rezultatai gali būti rodomi ne iš karto, priklausomai nuo naudojamo ieškos mechanizmo.
         
## <a name="career-site-urls"></a>Karjeros svetainės URL

Toliau nurodytame sąraše pateikiami dažnai naudojami karjeros svetainės URL ir nurodoma, kaip juos pasiekti.

-   **Karjeros svetainės pagrindinio puslapio URL** – norėdami peržiūrėti karjeros svetainės pagrindinio puslapio URL, prisijunkite prie „Attract“ kaip administratorius, pasirinkite parinktį **Administravimo centras**, pateiktą meniu **Parametrai**, tada pasirinkite skirtuką **Karjeros svetainės valdymas**.

-   **Atskiro darbo skelbimo prašymo teikimo URL** – kai [registruojate išorinę užduotį](Creating-jobs-Attract.md#postings) pirmą kartą, galite kopijuoti saitą **Teikti prašymą** iš „Attract“ programos. Šio saito URL bus pateiktas tokiu formatu: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **Atskiro darbo skelbimo URL** – darbo skelbimo URL yra antrinė prašymo teikimo URL eilutės eilutė. Ją sudaro visa informacija iki darbo numerio. Todėl prieš tai pateikto prašymo teikimo URL darbo skelbimo URL yra [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Autentifikavimo parinktys

Kandidatai gali naudoti toliau nurodytas prisijungimo prie „Attract“ karjeros svetainės parinktis.

-   Asmeninė paskyra

    -   „LinkedIn“

    -   Microsoft

    -   Google

    -   „Facebook“

-   Darbo arba mokyklos paskyra

    -   Microsoft Azure Active Directory (Azure AD)

„Azure AD“ prisijungimo funkcija skirta tik vidiniams kandidatams. Todėl ją gali naudoti tik vidiniai kandidatai, kurie naudoja savo įmonės „Azure AD“ kredencialus. Pavyzdžiui, kandidatas, kuris šiuo metu yra „Contoso, Ltd“ darbuotojas, nori kreiptis dėl darbo nesusijusioje įmonėje, „Alpine Ski House“. Tokiu atveju prisijungimas bus nesėkmingas, jei darbuotojas bandys naudoti savo „Azure AD“ kredencialus, priklausančius „Contoso, Ltd“.

## <a name="create-and-maintain-a-profile"></a>Profilio kūrimas ir tvarkymas

Prisijungę prie karjeros svetainės, kandidatai gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Mano profilis**, norėdami kurti ir tvarkyti savo profilį.
Profilis apima asmeninę informaciją, informaciją apie darbo patirtį, išsilavinimą, dokumentus, saitus ir informaciją apie įgūdžius. Sukūręs profilį kandidatas gali jį naudoti norėdamas kreiptis dėl dominančio darbo. Be to, naudodama profilius „Attract“ sistema kandidatams gali rekomenduoti tinkamus darbus.

>   [!NOTE]
>   Jei kandidatas naudoja el. pašto ID, kad prisijungtų naudodamas vieną iš pirmiau pateiktų autentifikavimo teikėjų, to el. pašto ID bus nustatytas į kontakto el. pašto ID, susietą su profiliu. Tačiau pastarąjį galima keisti bet kuriuo metu ir jis yra visiškai nepriklausomas nuo pirmojo. Visuose el. laiškuose „Attract“ visada naudos kontakto el. pašto ID, kad susietų su jūsų profiliu.

## <a name="find-the-right-job"></a>Tinkamo darbo paieška

Darbų sąrašo puslapyje kandidatai gali ieškoti konkretaus darbo įvesdami ieškos terminus. Ieškos funkcija ieško paieškos terminų pareigų pavadinimuose ir užduočių aprašymuose bei rodo atitinkamas užduotis kaip rezultatus. Kandidatai gali bet kuriuo metu filtruoti rezultatus pagal užduoties vietą arba užduoties funkciją.

Kandidatai taip pat gali peržiūrėti rekomenduojamų užduočių rinkinį karjeros svetainėje. Užduotys rekomenduojamos kandidatams pagal kandidato ankstesnius prašymus, profilį ir CV.

>   [!NOTE] 
>   Užduočių rekomendacijos rodomos tik jei karjeros svetainėje užregistruota ne mažiau kaip 10 užduočių ir jei kandidatas yra užpildęs savo profilį.

## <a name="apply-for-jobs"></a>Kreipimasis dėl darbo

Radę tinkamą darbą kandidatai gali teikti prašymą naudodami puslapio **Darbo informacija** mygtuką **Teikti prašymą**. Tuo metu kandidatai gali sukurti naują profilį arba peržiūrėti esamo profilio informaciją.
Kandidatų taip pat gali nusiųsti CV, jei reikia, ir tada pateikti prašymą įdarbinti.

## <a name="check-application-status"></a>Prašymo būsenos tikrinimas

Kai kandidatai pateikia prašymą dėl vieno arba kelių darbų, jie gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Programos**, kad peržiūrėtų savo atidarytus ir uždarytus prašymus. Kai kandidatas atidaro vieną iš savo prašymų, jis mato dabartinį etapą ir visus veiksmų laukiančius elementus, kuriuos jie turi užpildyti. Pavyzdžiui, jei kandidatas turi nurodyti galimas asmeninio pokalbio datas, puslapyje rodomos galimos parinktys.

## <a name="internal-jobs"></a>Vidiniai darbai

Šiuo metu darbai, kurie pažymėti kaip vidiniai ir užregistruoti „Attract“ karjeros svetainėje, karjeros svetainėje nerodomi. Jie yra pasiekiami tik naudojant tiesioginį saito **Teikti prašymą** URL, kurį galima nukopijuoti iš „Attract“ programos.
