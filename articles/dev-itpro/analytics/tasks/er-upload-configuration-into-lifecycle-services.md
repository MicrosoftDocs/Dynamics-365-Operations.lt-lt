--- 
title: "Konfigūracijos nusiuntimas į „Lifecycle Services“, kad būtų galima naudoti elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją ir ją nusiųsti į „Microsoft Lifecycle Services‟ (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d24679a380ec824fe08c56aacb4bc348ff40440a
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a>Konfigūracijos nusiuntimas į „Lifecycle Services“, kad būtų galima naudoti elektroninėse ataskaitose (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją ir ją nusiųsti į „Microsoft Lifecycle Services‟ (LCS).

Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai. Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“. Norint atlikti šiuos veiksmus, taip pat reikia prieigos prie LCS.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Pasirinkite „Litware, Inc.“ ir nustatykite kaip aktyvią.
3. Spustelėkite „Konfigūracijos“.

## <a name="create-a-new-data-model-configuration"></a>Sukurti naują duomenų modelio konfigūraciją
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
    * Sukursite konfigūraciją, apimančią elektroninių dokumentų duomenų modelio pavyzdį. Ši duomenų modelio konfigūracija vėliau bus nusiųsta į LCS.  
2. Lauke Pavadinimas įveskite „Modelio konfigūracijos pavyzdys“.
    * Modelio konfigūracijos pavyzdys  
3. Lauke Aprašas įveskite „Modelio konfigūracijos pavyzdys“.
    * Modelio konfigūracijos pavyzdys  
4. Spustelėkite Sukurti konfigūraciją.
5. Spustelėkite „Modelių kūrimo įrankis“.
6. Spustelėkite Naujas.
7. Lauke Pavadinimas įveskite „Įvesties vieta“.
    * Įvesties taškas  
8. Spustelėkite Pridėti.
9. Spustelėkite Įrašyti.
10. Uždarykite puslapį.
11. Spustelėkite keisti būseną.
12. Spustelėkite Baigti.
13. Spustelėkite GERAI.

## <a name="register-a-new--repository"></a>Naujos saugyklos registravimas
1. Uždarykite puslapį.
2. Spustelėkite Saugyklos.
    * Taip galima atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.  
3. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
    * Taip galima įtraukti naują saugyklą.  
4. Lauke Konfigūracijų saugyklos tipas pasirinkite LCS.
5. Spustelėkite Kurti saugyklą.
6. Lauke Projektas įveskite arba pasirinkite vertę.
    * Pasirinkite norimą LCS projektą. Turite turėti prieigos prie projekto teisę.  
7. Spustelėkite GERAI.
    * Baikite naują saugyklos įrašą.  
8. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite LCS saugyklos įrašą.  
    * Atkreipkite dėmesį, kad registruotą saugyklą pažymėjo dabartinis teikėjas, todėl perkelti į šią saugyklą ir vėliau nusiųsti į pasirinktą LCS projektą galima tik tam tiekėjui priklausančias konfigūracijas.  
9. Spustelėkite Atidaryti.
    * Atidarę saugyklą galėsite peržiūrėti ER konfigūracijų sąrašą. Jei šis projektas dar nenaudotas bendrinant ER konfigūracijas, sąrašas bus tuščias.  
10. Uždarykite puslapį.
11. Uždarykite puslapį.

## <a name="upload-configuration-into-lcs"></a>Konfigūracijos nusiuntimas į LCS
1. Spustelėkite „Konfigūracijos“.
2. Medyje pasirinkite „Modelio konfigūracijos pavyzdys‟.
    * Pasirinkite sukurtą, jau baigtą konfigūraciją.  
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite pasirinktos konfigūracijos versiją, kurios būsena – Baigta.  
4. Spustelėkite keisti būseną.
5. Spustelėkite Bendrinti.
    * Kai konfigūracija bus publikuota LCS portale, jos būsena iš „Baigta“ pasikeis į „Bendrai naudojama“.  
6. Spustelėkite GERAI.
7. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite konfigūracijos versiją, kurios būsena – „Bendrai naudojama‟.  
    * Atkreipkite dėmesį, kad pasirinktos versijos būsena pasikeitė iš „Baigta‟ į „Bendrai naudojama‟.  
8. Uždarykite puslapį.
9. Spustelėkite Saugyklos.
    * Taip galima atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.  
10. Spustelėkite Atidaryti.
    * Pasirinkite LCS saugyklą ir ją atidarykite.  
    * Atkreipkite dėmesį, kad pasirinkta konfigūracija rodoma kaip pasirinkto LCS projekto turtas.  
    * Naudodami https://lcs.dynamics.com atidarykite LCS. Atidarykite projektą, kuris buvo ankščiau naudotas registruojant saugyklas, atidarykite šio projekto turto biblioteką ir išskleiskite turto tipo „GER konfigūracija“ turinį – bus galima naudoti nusiųstąją ER konfigūraciją. Atkreipkite dėmesį, kad, jei tiekėjai turi prieigą prie šio LCS projekto, nusiųstąją LCS konfigūraciją galima importuoti į kitą „ Microsoft Dynamics 365 for Finance and Operations“, „Enterprise‟ leidimo egzempliorių.  


