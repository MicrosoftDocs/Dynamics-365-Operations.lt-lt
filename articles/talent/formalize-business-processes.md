---
title: "Verslo procesų formalizavimas"
description: "Verslo proceso funkcija suteikia galimybę kurti verslo proceso šabloną, skirtą procesams, kuriuos reikia atlikti jūsų organizacijoje."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1b50a97f5e2fc94255ff71702faf91ab36e68eb4
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="formalize-business-processes"></a>Verslo procesų formalizavimas
Verslo proceso funkcija suteikia galimybę kurti verslo proceso šabloną, skirtą procesams, kuriuos reikia atlikti jūsų organizacijoje. Pavyzdžiui, jūsų įmonė gali vykdyti personalo auditą kiekvienais metais. Galima sukurti šabloną, skirtą sekti visas užduotis, kurios sudaro auditą, kad visos užduotys būtų atliekamos kiekvieną kartą baigus procesą, ir, jei reikia, užduotys būtų atliekamos tinkama tvarka. Šablonus galima pakartotinai naudoti pasikartojančiuose procesuose arba kopijuoti ir naudoti kaip naujų šablonų kūrimo pagrindą.

Sukūrus šabloną, procesą galima pradėti ir sekti darbo srityje Verslo procesas.  Pradėjus verslo procesą, atitinkamiems žmonėms bus priskirta užduotis ir įtraukta termino data. Toliau aprašysime kiekvieną komponentą išsamiau.

## <a name="business-process-template"></a>Verslo proceso šablonas
Verslo proceso šablone pateikiama užduočių, sudarančių verslo procesą, grupė. Personalo vadovai ir asistentai gali kurti verslo procesus pagal numatytuosius parametrus.  Tačiau tai galima pakeisti saugos konfigūracijoje redaguojant pareigą Tvarkyti bendruosius verslo procesus.

Galima nurodyti kiekvieno proceso savininką. Proceso savininkas galės matyti visas proceso užduotis ir iš naujo priskirti užduotis arba keisti terminus.  Pavyzdžiui, personalo direktorius gali sukurti verslo proceso šabloną, skirtą išmokoms peržiūrėti.  Kompensacijų ir išmokų vadovas gali būti nustatytas kaip proceso savininkas, kad turėtų įžvalgų apie užduotis, kurias reikia atlikti peržiūros metu.  Proceso savininkas negali kurti arba naikinti aktyvių verslo procesų arba verslo procesų šablonų.

## <a name="task"></a>Užduotis
Verslo procesą dažnai sudaro kelios užduotys. Kai kurias užduotis galima atlikti „Dynamics 365 for Talent“, pvz., peržiūrėti vidinių kursų pasiūlymus. Tokiu atveju lauke Užduoties saitas pasirenkamas meniu elementas. Atliekant kitas užduotis gali reikėti peržiūrėti arba užpildyti formas svetainėje. Lauke Užduoties saitas pasirinkus URL, galima įvesti žiniatinklio adresą. Šiame lauke galite įvesti tiek išorinių, tiek vidinių svetainių URL. Taip pat galite kurti užduotis, skirtas neautomatiškai atliekamoms veikloms, pvz., visų struktūrų pasiekiamumo peržiūrai. Šiuo atveju užduoties saitas nebūtinas. Toks lankstumas suteikia galimybę sekti įvairių išsamaus proceso rūšių užduotis.

Užduotis galima priskirti konkrečiam darbuotojui arba pareigoms. Pavyzdžiui, kompensacijų ir išmokų vadovas visada bus asmuo, kuris peržiūri draudimo premijas.   Kurdami šią užduotį, pasirinkite pareigas kaip priskyrimo tipą ir tada pasirinkite kompensacijų bei išmokų vadovą iš pareigų sąrašo. Kai procesas prasidės, užduotis bus priskirta darbuotojui, kuris dirba kompensacijų ir išmokų vadovo pareigose. Taip pat galite priskirti užduotį konkrečiam darbuotojui lauke Priskyrimo tipas pasirinkdami parinktį Darbuotojas, o tada pasirinkdami atitinkamą asmenį.

Užduočių terminai priklauso nuo proceso pradžioje įvestos tikslinės datos. Kai kurias užduotis reikia baigti iki tikslinės datos, o kitas galima baigti po tikslinės datos.  Apibrėždami užduotį turite įvesti terminą, susijusį su paskirties data termino data, lauke Termino poslinkis nuo tikslinės datos. Pavyzdžiui, kompensacijų ir išmokų vadovas turi peržiūrėti draudimo įmokas 10 dienų anksčiau nei baigiamas personalo auditas. Sukurtos užduoties terminas bus susijęs su tiksline data pagal formulę –10. Todėl, jei procesas prasidės gegužės 13 d., užduoties terminas bus gegužės 3 d. Pastaba: terminus taip pat galima koreguoti pradėjus procesą.

Sudėtingas užduotis gali sudaryti keli veiksmai arba gali būti, kad užduotis atliekantis asmuo privalo pateikti papildomos informacijos. Į užduotį galite įtraukti instrukcijų ir jas pateikti raiškiojo teksto formatu. Instrukcijose galima pateikti papildomos informacijos apie tai, kaip asmuo, kuriam užduotis priskirta, reikia ją tą užduotį atlikti.

## <a name="starting-a-process"></a>Proceso pradžia
Procesą galima pradėti verslo proceso šablone pasirinkus Pradėti procesą.  Pradėjus procesą, bus sukurtos užduotys, skirtos pasirinktiems darbuotojams ir (arba) pareigoms, kurie nurodyti į verslo proceso šabloną įtrauktose užduotyse. Terminas taip pat bus priskirtas kiekvienai užduočiai, pridedant arba atimant korespondentines dienas iš tikslinės datos (žr. užduočių skyriuje pateikiamą informaciją apie korespondentines dienas). Aktyvius verslo procesus srityje galima peržiūrėti darbo srityje Verslo procesai. 

## <a name="employee-self-service"></a>Darbuotojų savitarna
Kai užduotis yra priskiriama darbuotojui, jiems priskirtas užduotis galima peržiūrėti puslapyje Darbuotojų savitarna. Darbuotojai, kuriems priskirta verslo proceso užduotis, gali matyti užduotį, jos aprašą, atlikimo instrukcijas ir kontaktinio asmens vardą bei pavardę, be to, jie gali atidaryti susijusį „Dynamics 365“ puslapį arba tinklalapį iš savo puslapio Darbuotojų savitarna. Užduotis galima pažymėti kaip vykdomas, atšauktas arba baigtas.

## <a name="business-process-workspace"></a>Darbo sritis Verslo procesas
Personalo specialistai gali peržiūrėti aktyvius verslo procesus darbo srityje Verslo procesas. Darbo srityje pateikiami visi aktyvūs procesai ir kiekvienam jų priskiriamos užduotys. Išsamų užduočių sąrašą galima filtruoti pagal terminą. Puslapyje taip pat pateikiamos pradelstos užduotys ir užduotys, kurios konkrečiai priskirtos personalo specialistui. Jie taip pat gali naujinti visų užduočių būsenas ir, jei reikia, iš naujo priskirti užduotis, kad bendras verslo procesas būtų toliau vykdomas.

## <a name="my-business-processes-workspace"></a>Darbo sritis Mano verslo procesai
Proceso savininkai gali peržiūrėti aktyvius verslo procesus, kurie jiems priskirti, darbo srityje Mano verslo procesai. Darbo srityje pateikiami visi aktyvūs procesai ir susijusios užduotys, kurios priklauso vartotojui.  Išsamų užduočių sąrašą galima filtruoti pagal terminą. Puslapyje taip pat pateikiamos užduotys, konkrečiai priskirtos proceso savininkui. Proceso savininkas taip pat gali naujinti visų užduočių būsenas, be to, jis gali iš naujo priskirti bet kurią užduotį.

## <a name="navigating-business-processes"></a>Verslo procesų naršymas
1. Norėdami įtraukti verslo proceso šabloną, pasirinkite Verslo procesai – nuorodos – Verslo procesų administravimas.
   - A.   Pasirinkus Naujas, bus sukurtas naujas šablonas.
   - B.   Pasirinkus Kopijuoti iš šablono, pasirinktas šablonas bus nukopijuotas į naują šabloną.
   - C.   Pasirinkus Pradėti procesą, bus pradėtas pasirinktas verslo procesas, priskiriamos užduotys ir apskaičiuojami terminai.  
2. Norėdami peržiūrėti aktyvius verslo procesus ir susietas užduotis, pasirinkite darbo sritį Verslo procesai.

