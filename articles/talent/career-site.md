---
title: "„Attract“ karjeros svetainės funkcijos"
description: "Šiame straipsnyje pateikta kandidatams skirtos karjeros svetainės funkcijos programoje „Microsoft Dynamics 365 for Talent - Attract“ apžvalga. Jame taip pat paaiškinama, kaip šią funkciją nustatyti."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: lt-lt
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>„Attract“ karjeros svetainės funkcijos

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikta kandidatams skirtos karjeros svetainės funkcijos programoje „Microsoft Dynamics 365 for Talent: Attract“ apžvalga. Jame taip pat paaiškinama, kaip šią funkciją nustatyti.

## <a name="overview"></a>Apžvalga

„Attract“ suteikia vieną karjeros svetainę kiekvienai nuomotojo aplinkai. Pvz., jei organizacija naudoja kūrimo aplinką ir tikrinimo aplinką, viena karjeros svetainė skiriama kūrimo aplinkai, o kita karjeros svetainė skiriama tikrinimo aplinkai. Kiekviena karjeros svetainė yra **visiškai atskira** ir joje veikia atskiras autentifikavimo mechanizmas. Darbai ir kandidatų profiliai nėra bendrinami karjeros svetainėse.

Pagal numatytuosius parametrus karjeros svetainė yra vieša. Todėl kandidatai neprisijungę gali peržiūrėti visas užduotis, kurios pažymėtos kaip išorinės. Tačiau, norėdami atlikti visus kitus veiksmus, kandidatų turi prisijungti.

## <a name="career-site-management"></a>Karjeros svetainės valdymas

Parametrai valdo toliau nurodytus karjeros svetainės elementus.

- **Organizacijos pavadinimas:** organizacijos pavadinimas rodomas karjeros svetainės naršymo juostos viršuje. Pasirinkdami organizacijos pavadinimą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.
- **Organizacijos logotipas:** organizacijos logotipo vaizdas rodomas viršutiniame kairiajame karjeros svetainės kampe. Pasirinkdami organizacijos logotipo vaizdą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.

Norėdami nustatyti organizacijos pavadinimo ir logotipo reikšmes, prisijunkite prie „Attract“ kaip administratorius, pasirinkite **Administravimo centras** meniu **Parametrai** meniu (krumpliaračio simbolis), tada pasirinkite skirtuką **Įmonės informacija**.

> [!NOTE]
> Logotipo vaizdo, kuris rodomas karjeros svetainėje, aukštis yra fiksuotas – 20 pikselių (piks.). Vaizdo, kurį įtraukiate į administravimo centrą, dydis atitinkamai pritaikomas. Todėl, priklausomai nuo vaizdo, plotis gali keistis.

## <a name="career-site-url"></a>Karjeros svetainės URL

Kai [registruojate išorinę užduotį](./Creating-jobs-Attract.md#postings) pirmą kartą, galite kopijuoti saitą **Teikti prašymą** iš „Attract“ programos. Šio saito URL bus pateiktas tokiu formatu: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Karjeros svetainės URL yra antrinė saito **Teikti prašymą** URL eilutė. Jį sudaro visa informacija iki įmonės pavadinimo (imtinai). Todėl prieš tai pateikiamo nuorodos **Teikti prašymą** URL karjeros svetainės URL yra `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Autentifikavimo parinktys

Kandidatai gali naudoti toliau nurodytas prisijungimo prie „Attract“ karjeros svetainės parinktis.

- Asmeninė paskyra

    - „LinkedIn“
    - „Microsoft“
    - Google
    - „Facebook“

- Darbo arba mokyklos paskyra

    - Microsoft Azure Active Directory (Azure AD)

„Azure AD“ prisijungimo funkcija skirta tik vidiniams kandidatams. Todėl ją gali naudoti tik vidiniai kandidatai, kurie naudoja savo įmonės „Azure AD“ kredencialus. Pavyzdžiui, kandidatas, kuris šiuo metu yra „Contoso, Ltd“ darbuotojas, nori kreiptis dėl darbo nesusijusioje įmonėje, „Alpine Ski House“. Tokiu atveju prisijungimas bus nesėkmingas, jei darbuotojas bandys naudoti savo „Azure AD“ kredencialus, priklausančius „Contoso, Ltd“.

## <a name="create-and-maintain-a-profile"></a>Profilio kūrimas ir tvarkymas

Prisijungę prie karjeros svetainės, kandidatai gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Mano profilis**, norėdami kurti ir tvarkyti savo profilį. Profilis apima asmeninę informaciją, informaciją apie darbo patirtį, išsilavinimą, dokumentus, saitus ir informaciją apie įgūdžius. Sukūręs profilį kandidatas gali jį naudoti norėdamas kreiptis dėl dominančio darbo. Be to, naudodama profilius „Attract“ sistema kandidatams gali rekomenduoti tinkamus darbus.

## <a name="find-the-right-job"></a>Tinkamo darbo paieška

Darbų sąrašo puslapyje kandidatai gali ieškoti konkretaus darbo įvesdami ieškos terminus. Ieškos funkcija ieško paieškos terminų pareigų pavadinimuose ir užduočių aprašymuose bei rodo atitinkamas užduotis kaip rezultatus. Kandidatai gali bet kuriuo metu filtruoti rezultatus pagal užduoties vietą arba užduoties funkciją.

Kandidatai taip pat gali peržiūrėti rekomenduojamų užduočių rinkinį karjeros svetainėje. Užduotys rekomenduojamos kandidatams pagal kandidato ankstesnius prašymus, profilį ir CV.

> [!NOTE]
> Užduočių rekomendacijos rodomos tik jei karjeros svetainėje užregistruota ne mažiau kaip 10 užduočių ir jei kandidatas yra užpildęs savo profilį.

## <a name="apply-for-jobs"></a>Kreipimasis dėl darbo

Radę tinkamą darbą kandidatai gali teikti prašymą naudodami darbo informacijos puslapio mygtuką **Teikti prašymą**. Tuo metu kandidatai gali sukurti visiškai naują profilį arba peržiūrėti esamo profilio informaciją. Kandidatų taip pat gali nusiųsti CV, jei reikia, ir tada pateikti prašymą įdarbinti.

## <a name="check-application-status"></a>Prašymo būsenos tikrinimas

Kai kandidatai pateikia prašymą dėl vieno arba kelių darbų, jie gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Programos**, kad peržiūrėtų savo atidarytus ir uždarytus prašymus. Kai kandidatas atidaro vieną iš savo prašymų, jis mato dabartinį etapą ir visus veiksmų laukiančius elementus, kuriuos jie turi užpildyti. Pavyzdžiui, jei kandidatas turi nurodyti galimas asmeninio pokalbio datas, puslapyje rodomos galimos parinktys.

## <a name="internal-jobs"></a>Vidiniai darbai

Šiuo metu darbai, kurie pažymėti kaip vidiniai ir užregistruoti „Attract“ karjeros svetainėje, karjeros svetainėje nerodomi. Jie yra pasiekiami tik naudojant tiesioginį saito **Teikti prašymą** URL, kurį galima nukopijuoti iš „Attract“ programos.

