---
title: Išmokų programos nustatymas ir valdymas
description: Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos savo darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbuotojų kompensacijų planus. Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti ir tvarkyti išmokas.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 08b80f4f90ce6b4a286120cd6329a45a4ebd3f71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877807"
---
# <a name="define-and-manage-a-benefits-program"></a>Išmokų programos nustatymas ir valdymas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos savo darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbuotojų kompensacijų planus. Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti ir tvarkyti išmokas.

## <a name="benefit-setup"></a>Išmokų nustatymas

Norėdami, kad darbuotojams būtų paskirtos išmokos, turite sukurti kiekvienos išmokos elementus. Šie elementai sujungia panašius išmokų planus ir nustatyto numatytuosius parametrus, pvz., atskaitymo kursus ir apskaitos informaciją. Daugelį šių parametrų galima koreguoti vėliau, kai darbuotojams paskiriamos išmokos. Kiekvienam išmokų planui organizacija gali pasiūlyti kelias registracijos pasirinktis arba darbuotojas gali atsisakyti registracijos plane. 

[![Išmokos proceso srautas.](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Išmokos elementai

Prieš pradėdami kurti išmokas ir registruoti jose darbuotojus, turite nurodyti elementus, kurie sudaro išmoką: tipas, planas ir pasirinktys.

-   **Tipas** – konkrečios išmokos, pvz., medicininės arba automobilio stovėjimo, planų rinkinys.
-   **Planas** – konkreti išmoka, gaunama iš tiekėjo.
-   **Parinktis** – aprėpties lygis, pvz., tik darbuotojas arba darbuotojas ir sutuoktinis / partneris.

Kiekvienam išmokos tipui, pvz., regėjimo ar dantų gydymo, organizacija savo darbuotojams gali pasiūlyti vieną ar kelis planus. Kiekvienam planui organizacija gali pasiūlyti skirtingas pasirinktis. Pvz., darbuotojai, gali įsigyti papildomo laikotarpio gyvybės draudimą, kurio vertė atitinka vieną, du ar tris jų metinius atlyginimus. Kiekvienas plano ir pasirinkčių derinys tampa išmoka, kurią gali gauti darbuotojai. 

[![išmokų paveikslėlis.](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Tinkamumas
Darbuotojo tinkamumas įvairiems darbdavio siūlomiems išmokų tipams priklauso nuo daugelio faktorių. Kai sukuriate „Dynamics 365 Human Resources“ išmoką, galite nustatyti tai išmokai taikomą tinkamumo tipą. 

Galite nustatyti, kad išmoka būtų prieinama visiems darbuotojams. Pavyzdžiui, kai kuriose įmonėse kaip papildoma išmoka siūlomi automobilių stovėjimo leidimai. Sukūrę šią išmoką nustatote tinkamumo pasirinktį **Taikoma visiems darbuotojams**. 

Kitoms išmokoms, pvz., pinigų arešto ir mokesčių, tinkamumas negalioja. Kai kuriate šiuos išmokų tipus, galite nustatyti tinkamumo pasirinktį **Apeiti tinkamumo procesą**. 

Galiausiai tinkamumas išmokai gali būti pagrįstas taisykle. Pavyzdžiui, įmonė darbuotojams siūlo dviejų tipų gyvybės draudimo išmokas. Vadovaujantys darbuotojai gali gauti vieną gyvybės draudimo planą, o visi kiti visu etatu dirbantys darbuotojai – kitą gyvybės draudimo planą. Programoje „Human Resources“ norėdami rasti visus vadovaujančius darbuotojus, galite sukurti tinkamumo išmokai taisyklę, o norėdami rasti visus kitus visu etatu dirbančius darbuotojus – kitą taisyklę ir taikyti šias taisykles atitinkamai išmokai.

## <a name="enrollment"></a>Registracija
Sukūrę jūsų organizacijos siūlomas išmokas ir nustatę tinkamumą, galite registruoti darbuotojus išmokoms gauti. Išmokoms gauti galite užregistruoti vieną darbuotoją, arba vienai arba kelioms išmokoms gauti galite užregistruoti daug darbuotojų vienu metu. 

Kartais organizacija liaujasi siūliusi tam tikras išmokas. Tokiu atveju turite atnaujinti išmoką ir darbuotojus, kurie užregistruoti jai gauti. Visuotinės išmokos galiojimo pabaigos parinktis vienu metu leidžia keisti išmokos ir darbuotojų registracijos tai išmokai gauti galiojimo datą. Taip pat galite pasirinkti kelis darbuotojus, kurie užregistruojami gauti išmoką, ir pakeisti taikymo pabaigos datą. 

Be to, jei nusprendėte, kad išmoką norėsite pasiūlyti ilgesniam laikotarpiui negu buvo planuota, visuotinės išmokos plėtinys leidžia pratęsti išmokos ir darbuotojų registracijos tai išmokai gauti galiojimo datą.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
