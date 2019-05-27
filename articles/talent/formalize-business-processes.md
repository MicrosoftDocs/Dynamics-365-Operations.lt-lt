---
title: Verslo procesų formalizavimas
description: Šioje temoje paaiškinama, kaip, naudodami funkciją Verslo procesas, galite sukurti verslo proceso šabloną, skirtą procesams, kuriuos reikia atlikti jūsų organizacijoje.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 85950a1413cfd8745bb78a52eb9f7c81b8976605
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518637"
---
# <a name="formalize-business-processes"></a>Verslo procesų formalizavimas

[!include[banner](includes/banner.md)]

Funkcija Verslo procesas leidžia sukurti verslo proceso šabloną, skirtą verslo procesams, kuriuos reikia atlikti jūsų organizacijoje. Pavyzdžiui, jūsų įmonė kiekvienais metais atlieka personalo auditą. Tokiu atveju galite sukurti šabloną, sekantį visas užduotis, kurios sudaro audito procesą. Tada šis šablonas gali padėti užtikrinti, kad kiekvieną kartą atliekant auditą būtų atliktos visos užduotys. Be to, jei užduotis reikia atlikti konkrečia tvarka, šablonas gali padėti užtikrinti, kad jos būtų atliktos teisinga tvarka.

Šablonus galima pakartotinai naudoti atliekant pasikartojančius procesus. Juos taip pat galima kopijuoti ir naudoti kaip pradžios tašką naujiems šablonams kurti.

Sukūrus verslo proceso šabloną, darbo srityje **Verslo procesas** galima pradėti ir sekti verslo procesą. Pradėjus verslo procesą, užduotys priskiriamos atitinkamiems žmonėms ir į jas įtraukiamas terminas.

## <a name="business-process-templates"></a>Verslo procesų šablonai
Verslo proceso šablone pateikiama užduočių, sudarančių verslo procesą, grupė. Pagal numatytuosius parametrus verslo procesus gali kurti personalo vadovai ir asistentai. Tačiau vaidmenis, galinčius kurti verslo procesus, galite keisti modifikuodami saugos konfigūracijos pareigą **Tvarkyti bendruosius verslo procesus**.

Galite nustatyti kiekvieno verslo proceso savininką. Proceso savininkas mato visas proceso užduotis ir gali jas priskirti iš naujo arba keisti terminus. Pavyzdžiui, personalo direktorius sukuria verslo proceso šabloną išmokų peržiūrai bei kaip proceso savininką nurodo kompensacijų ir išmokų vadovą. Tada kompensacijų ir išmokų vadovas mato užduotis, kurias reikia atlikti peržiūrint išmokas.

Proceso savininkas negali kurti naujų verslo procesų ar verslo procesų šablonų ir panaikinti aktyvių verslo procesų ar verslo procesų šablonų.

## <a name="tasks"></a>Užduotys
Verslo procesą dažnai sudaro kelios užduotys. Kai kurias užduotis, pvz., peržiūrėti vidinių kursų pasiūlymus, galima atlikti sprendime „Microsoft Dynamics 365 for Talent“[?]. Tokiu atveju lauke **Užduoties saitas** pasirenkama atitinkama parinktis. Atliekant kitas užduotis gali reikėti peržiūrėti arba užpildyti svetainės puslapius. Tokiu atveju lauke **Užduoties saitas** pasirenkama **URL** – tada galima įvesti žiniatinklio adresą. Galite įvesti tiek išorinių, tiek vidinių svetainių URL adresus. Taip pat galite kurti užduotis, skirtas neautomatiškai atliekamoms veikloms, pvz., visų struktūrų pasiekiamumo peržiūrai. Šiuo atveju užduoties saitas nereikalingas. Toks lankstumas suteikia galimybę sekti įvairių išsamaus proceso rūšių užduotis.

Užduotis galima priskirti konkrečiam darbuotojui arba pareigoms. Pavyzdžiui, draudimo premijas visada peržiūrės Kompensacijų ir išmokų vadovas. Todėl kurdami šią užduotį lauke **Priskyrimo tipas** pasirinkite **Pareigos**, o tada sąraše **Pareigos** pasirinkite **Kompensacijų ir išmokų vadovas**. Kai verslo procesas pradedamas, užduotis priskiriama darbuotojui, užimančiam pareigas **Kompensacijų ir išmokų vadovas**. Norėdami užduotį priskirti konkrečiam darbuotojui, lauke **Priskyrimo tipas** pasirinkite **Darbuotojas**, tada pasirinkite atitinkamą asmenį.

Užduočių terminai priklauso nuo proceso pradžioje įvestos tikslinės datos. Kai kurias užduotis reikia baigti iki tikslinės datos, o kitas gali būti galima baigti po tikslinės datos. Apibrėžiant užduotį, lauke **Termino poslinkis nuo tikslinės datos** nurodomas terminas, susijęs su paskirties data. Pavyzdžiui, kompensacijų ir išmokų vadovas draudimo įmokas turi peržiūrėti 10 dienų anksčiau nei baigiamas personalo auditas. Tokiu atveju peržiūrai sukurtos užduoties lauko **Termino poslinkis nuo tikslinės datos** reikšmė yra **–10**. Todėl, jei verslo procesas pradedamas gegužės 13 d., užduoties terminas yra gegužės 3 d.

> [!NOTE]
> Terminus taip pat galima koreguoti pradėjus verslo procesą.

Sudėtingas užduotis gali sudaryti keli veiksmai arba užduotis atliekantiems asmenims gali reikėti pateikti papildomos informacijos. Tokiose situacijose į užduotį galite įtraukti instrukcijų. Instrukcijos asmeniui, kuriam priskirta atlikti užduotį, gali pateikti papildomos informacijos apie tai, kaip tai padaryti. Instrukcijose net galite naudoti raiškiojo teksto formatavimą.

## <a name="starting-a-business-process"></a>Verslo proceso pradėjimas
Verslo proceso šablone verslo procesą galite pradėti pasirinkdami **Pradėti procesą**. Pradėjus procesą, sukuriamos užduotys, skirtos pasirinktiems darbuotojams ar pareigoms, kurie nustatyti į šabloną įtrauktose užduotyse. Kiekvienai užduočiai taip pat priskiriamas terminas, prie tikslinės datos pridedant ar iš jos atimant poslinkio dienų, kaip paaiškinta skyriuje „Užduotys“. Aktyvius verslo procesus galite peržiūrėti darbo srityje **Verslo procesai**.

## <a name="employee-self-service"></a>Darbuotojų savitarna
Darbuotojui priskyrus užduotį, ją ir visas kitam jam priskirtas užduotis darbuotojas gali peržiūrėti puslapyje **Darbuotojų savitarna**. Darbuotojas gali matyti kiekvienos jam priskirtos verslo proceso užduoties pavadinimą ir aprašą, jos atlikimo instrukcijas bei kontaktinio asmens vardą. Puslapyje **Darbuotojų savitarna** darbuotojas taip pat gali atidaryti susietą „Microsoft Dynamics 365“ puslapį arba susietą tinklalapį ir užduotis gali pažymėti kaip vykdomas, atšauktas arba baigtas.

## <a name="business-process-workspace"></a>Darbo sritis Verslo procesas
Personalo specialistai aktyvius verslo procesus gali peržiūrėti darbo srityje **Verslo procesas**. Šioje darbo srityje pateikiami visi aktyvūs procesai ir su kiekvienu iš jų susietos užduotys. Išsamų užduočių sąrašą galima filtruoti pagal terminą. Šioje darbo srityje taip pat pateikiamos pradelstos užduotys ir užduotys, priskirtos konkrečiai personalo specialistui. Personalo specialistas taip pat gali atnaujinti visų užduočių būseną ir, prireikus, užduotis priskirti iš naujo, kad bendras verslo procesas būtų toliau vykdomas.

## <a name="my-business-processes-workspace"></a>Darbo sritis Mano verslo procesai
Procesų savininkai aktyvius jiems priskirtus verslo procesus gali peržiūrėti darbo srityje **Mano verslo procesai**. Šioje darbo srityje pateikiami visi aktyvūs procesai, priklausantys vartotojui, ir susietos užduotys. Išsamų užduočių sąrašą galima filtruoti pagal terminą. Šioje darbo srityje taip pat pateikiamos užduotys, priskirtos konkrečiai proceso savininkui. Proceso savininkas taip pat gali atnaujinti visų užduočių būseną ir iš naujo priskirti bet kurią užduotį.

## <a name="navigating-business-processes"></a>Verslo procesų naršymas
Norėdami sukurti ar kopijuoti verslo procesų šabloną arba pradėti verslo procesą, eikite į Verslo procesai – saitai – Verslo procesų administravimas. Tada galite atlikti tolesnius veiksmus.

- Pasirinkite **Naujas**, jei norite sukurti naują verslo procesų šabloną.
- Pasirinkite **Kopijuoti iš šablono**, jei pasirinktą šabloną norite nukopijuoti į naują šabloną.
- Pasirinkite **Pradėti procesą**, jei norite pradėti pasirinktą verslo procesą, priskirti užduočių ir skaičiuoti terminus.

Norėdami peržiūrėti aktyvius procesus ir susietas užduotis, atidarykite darbo sritį **Verslo procesai**.

