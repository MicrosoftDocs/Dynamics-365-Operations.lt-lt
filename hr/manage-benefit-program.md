---
title: "Nustatyti ir tvarkyti išmokų programa"
description: "Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos savo darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbuotojų kompensacijų planus. Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti ir tvarkyti išmokas."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Nustatyti ir tvarkyti išmokų programa

Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos savo darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbuotojų kompensacijų planus. Šioje temoje pateikta informacija apie tai, kaip nustatyti tvarkyti naudą.

<a name="benefit-setup"></a>Naudos nustatymo
-------------

Norėdami, kad darbuotojams būtų paskirtos išmokos, turite sukurti kiekvienos išmokos elementus. Šie elementai sujungia panašius išmokų planus ir nustatyto numatytuosius parametrus, pvz., atskaitymo kursus ir apskaitos informaciją. Daugelį šių parametrų galima koreguoti vėliau, kai darbuotojams paskiriamos išmokos. Kiekvienam išmokų planui organizacija gali pasiūlyti kelias registracijos pasirinktis arba darbuotojas gali atsisakyti registracijos plane. 

[![Naudingas procesas srauto](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Išmokos elementai
Prieš pradėdami kurti išmokas ir registruoti jose darbuotojus, turite nurodyti elementus, kurie sudaro išmoką: tipas, planas ir pasirinktys.

-   **Tipas** – konkrečios išmokos, pvz., medicininės arba automobilio stovėjimo, planų rinkinys.
-   **Planas** – konkreti išmoka, gaunama iš tiekėjo.
-   **Parinktis** – aprėpties lygis, pvz., tik darbuotojas arba darbuotojas ir sutuoktinis / partneris.

Kiekvienam išmokos tipui, pvz., regėjimo ar dantų gydymo, organizacija savo darbuotojams gali pasiūlyti vieną ar kelis planus. Kiekvienam planui organizacija gali pasiūlyti skirtingas pasirinktis. Pvz., darbuotojai, gali įsigyti papildomo laikotarpio gyvybės draudimą, kurio vertė atitinka vieną, du ar tris jų metinius atlyginimus. Kiekvienas plano ir pasirinkčių derinys tampa išmoka, kurią gali gauti darbuotojai. 

[![naudos IPS](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Tinkamumas
Darbuotojo tinkamumas įvairiems darbdavio siūlomiems išmokų tipams priklauso nuo daugelio faktorių. Kai kuriate naudos Microsoft Dynamics "365" operacijoms, galite nustatyti tinkamumo, minimus tos naudos rūšį. 

Jums gali suteikti naudos visiems darbuotojams. Pavyzdžiui, kai kurios kompanijos siūlo automobilių stovėjimo aikštelę eina visi darbuotojai kaip papildomų išmokų. Sukūrę šią išmoką nustatote tinkamumo pasirinktį **Taikoma visiems darbuotojams**. 

Kiti privalumai, pvz garnishments ir mokesčių mokėjimų, negalioja tinkamumo. Išrūgas galite sukurti šių tipų privalumai, galite nustatyti tinkamumo **apeiti reikalavimų atitikimo proceso**. 

Galiausiai, naudai gali būti taisyklėmis pagrįsta. Pvz., įmonė siūlo dviejų rūšių gyvybės draudimo išmokų darbuotojams. Darbuotojai turi teisę gauti vienos gyvybės draudimo planą, kadangi kitų visą darbo dieną dirbantiems asmenims kito gyvybės draudimo plano priklauso. Dynamics 365 operacijoms, galite sukurti naudos tinkamumo taisyklę rasti visų vykdomosios darbuotojų ir kita taisyklė rasti visi visą darbo dieną dirbantys darbuotojai, ir tada taikyti tas taisykles reikia pasinaudoti.

## <a name="enrollment"></a>Registracija
Sukūrę jūsų organizacijos siūlomas išmokas ir nustatę tinkamumą, galite registruoti darbuotojus išmokoms gauti. Išmokoms gauti galite užregistruoti vieną darbuotoją, arba vienai arba kelioms išmokoms gauti galite užregistruoti daug darbuotojų vienu metu. 

Kartais organizacija liaujasi siūliusi tam tikras išmokas. Šiuo atveju turite atnaujinti naudinga ir darbuotojams, kurie mokosi. Masinių naudos galiojimo leidžia pakeisti galiojimo data yra naudingas ir darbuotojas turės tokią naudą, tuo pačiu metu. Taip pat galite pasirinkti kelis darbuotojus, kurie užregistruojami gauti išmoką, ir pakeisti taikymo pabaigos datą. 

Be to, jei nusprendėte, kad išmoką norėsite pasiūlyti ilgesniam laikotarpiui negu buvo planuota, visuotinės išmokos plėtinys leidžia pratęsti išmokos ir darbuotojų registracijos tai išmokai gauti galiojimo datą.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


