---
title: "Kaštų apskaitos terminija"
description: "Šioje temoje nurodomi pagrindiniai atliekant kaštų apskaitą naudojami terminai."
author: YuyuScheller
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1ec2f4a407c705fb37681f5593d0f7ea31f4cf0f
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="cost-accounting-terminology"></a>Kaštų apskaitos terminija

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje nurodomi pagrindiniai atliekant kaštų apskaitą naudojami terminai.

**Paskirstymo bazė**

Paskirstymo bazė naudojama matuoti ir kiekybiškai išreikšti veikloms, pvz., mašinos darbo valandų skaičiui, suvartotų kilovatvalandžių skaičiui ar užimamam plotui kvadratinėmis pėdomis. Ji naudojama kaip išlaidų paskirstymo į vieną ar kelis savikainos objektus pagrindas

**Kaštų apskaita**

Naudodami kaštų apskaitą galite rinkti duomenis iš įvairių šaltinių, pvz., didžiosios knygos, antrinių didžiųjų knygų, biudžetų ir statistinės informacijos. Tada galite analizuoti, apibendrinti ir įvertinti išlaidų duomenis, kad vadovybė galėtų priimti geriausius sprendimus dėl kainos atnaujinimų, biudžetų, išlaidų valdymo ir t. t. Išlaidų analizei naudojami šaltinio duomenys kaštų apskaitoje apdorojami atskirai. Todėl kaštų apskaitos naujinimai neturi įtakos šaltinio duomenims. Tačiau, kai surenkate išlaidų duomenis iš įvairių šaltinių ir ypač, kai importuojate pagrindines sąskaitas iš didžiosios knygos į „Microsoft Dynamics 365 for Finance and Operations“ kaip išlaidų elementus, duomenys dubliuojasi, nes tie patys duomenys yra didžiojoje knygoje ir kaštų apskaitoje. Šis dubliavimasis reikalingas, nes išorinėse ataskaitose naudojate finansinį valdymą, o vidinėse ataskaitose – kaštų apskaitą.

**Savikainos apskaitos didžioji knyga**

Ją apibrėžia kalendorius, valiuta bei savikainos elemento dimensija ir ji valdo išlaidų matavimo procesus bei strategijas. 

**Savikainos įrašas**

Išlaidų įrašai atsiranda perkeliant iš didžiosios knygos įrašų, išlaidų paskirstymų ir išlaidų žurnaluose užregistruotų išlaidų įrašų, kai naudojamos duomenų jungtys.

**Išlaidų objektas**

Bet kokio tipo objektas, kuriam pasirinkta taikyti išlaidų kontrolę. Išlaidos ar įplaukos išlaidų objektuose tiesiogiai registruojamos arba į juos paskirstomos. Toliau nurodyti keli įprasti išlaidų objektai.

-  Produktai
-  Projektai
-  Padaliniai
-  Išlaidų centrai

Valdyba naudoja išlaidų objektus ne tik norėdama apskaičiuoti išlaidas, bet ir atlikti pelningumo analizę.

**Savikainos elementas**

Naudojamas kaip funkcija išlaidoms sekti ir kategorizuoti. Yra dviejų tipų savikainos elementai: pirminiai ir antriniai.

Pirminiai savikainos elementai atitinka išlaidų srautą iš finansinės apskaitos į modulį Kaštų apskaita. Struktūra paprastai atitinka pelno ir nuostolio sąskaitos struktūrą didžiojoje knygoje, kai savikainos elementas gali atitikti pagrindinę sąskaitą. Ne visos pagrindinės sąskaitos privalo būti pateikiamos kaip savikainos elementai, priklausomai nuo verslo poreikių. 

Antriniai savikainos elementai atitinka vidinį išlaidų srautą, nes šios išlaidos naudojamos tik modulyje Kaštų apskaita. Jie naudojami išlaidų sumavimo taisyklėse, norint išlaidas telkti į prasmingus rinkinius, naudojamus skaičiuojant pridėtines išlaidas. 

**Išlaidų klasifikacija**

Naudojant išlaidų klasifikavimą išlaidos grupuojamos pagal jų bendro naudojimo savybes. Pavyzdžiui, išlaidas galima grupuoti pagal elementus, atsekamumą ir elgseną.

-   **Pagal elementus** – medžiagas, darbą ir išlaidas.
-   **Pagal atsekamumą** – tiesiogines išlaidas ir netiesiogines išlaidas. Tiesioginės išlaidos priskiriamos tiesiogiai savikainos objektams. Netiesioginės išlaidos nėra tiesiogiai susietos su savikainos objektais. Netiesioginės išlaidos paskirstomos savikainos objektams.
-   **Pagal elgseną** – fiksuotos, kintamosios ir pusiau kintamosios.

**Išlaidų elgsena**

Pagal elgseną išlaidos klasifikuojamos atsižvelgiant į jų elgseną esant pokyčių pagrindinėje verslo veikloje. Norint efektyviai valdyti išlaidas, vadovybė turi suprasti išlaidų elgseną. Yra trijų tipų išlaidų elgsenos modeliai: fiksuotos, kintamosios ir pusiau kintamosios.

- **Fiksuota savikaina** Fiksuota savikaina – tai išlaidos, kurios nekinta trumpuoju laikotarpiu nepaisant veiklos lygio pokyčių. Pavyzdžiui, fiksuotos išlaidos gali būti pagrindinės įmonės veiklos išlaidos, pvz., nuoma, kuri nesikeis net jei padidės arba sumažės veiklos lygis.

- **Kintamos išlaidos** Kintamos išlaidos kinta pagal veiklos lygio pokyčius. Pavyzdžiui, konkrečių tiesioginių medžiagų išlaidos yra susijusios su kiekvienu parduotu produktu. Kuo daugiau produktų parduodama, tuo didesnės tiesioginės išlaidos už medžiagas.

- **Pusiau kintamos išlaidos** Pusiau kintamos išlaidos yra iš dalies fiksuotos ir iš dalies kintamos išlaidos. Pavyzdžiui, interneto prieigos mokestis apima standartinį mėnesinį prieigos mokestį ir plačiajuostį naudojimo mokestį. Šis standartinis mėnesinis prieigos mokestis yra fiksuotos išlaidos, o plačiajuostis naudojimo mokestis yra kintamosios išlaidos.

**Savikainos kontrolės įtaisas**

Savikainos kontrolės įtaisas atitinka išlaidų struktūrą. Struktūra nustato, koks yra išlaidų srautas hierarchijoje tarp išlaidų objektų dimensijų ir jų atitinkamų išlaidų objektų. 

**Išlaidų paskirstymas**

Naudojamas skirstant išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę. Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu ir nenaudojamas abipusis apdorojimas.

**Išlaidų paskirstymas**

Naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo bazę. „Finance and Operations” palaiko abipusio paskirstymo metodą. Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos. Sistema automatiškai nustato tvarką, kuria reikia atlikti ir kartoti paskirstymą. Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą. Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams. Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.

**Savikainos paskirstymo strategija**

Išlaidų paskirstymo strategijoje nurodomos sumos ir kiekiai, kurie turi būti paskirstyti. Paskirstymo taisyklės apima paskirstymo šaltinio taisykles, nurodančias, paskirstytas išlaidas ir paskirstymo tikslų taisykles, nurodančias, kur paskirstomos išlaidos. Pavyzdžiui, visos paslaugų išlaidos yra paskirstymo šaltinis, kurį galima paskirstyti įvairiems organizacijos padaliniams (t. y. paskirstymo tikslams).

**Išlaidų sumavimas**

Išlaidų sumavimo taisyklių tikslas yra išlaidas telkti į prasmingus rinkinius. Telkimo lygį apibrėžia vartotojas ir telkiant priskiriamas antrinis savikainos elementas. Jei išlaidų sumavimas nenaudojamas, kiekvienas išlaidų elementas paskirstomas iš vieno savikainos objekto kitam savikainos objektui

**Išlaidų tarifo strategija**

Išlaidų tarifas naudojamas norint apskaičiuoti vieno savikainos objekto kainą. Norėdami suprasti kainos elementus, nurodote išlaidų tarifo strategijas. Yra dviejų tipų išlaidų tarifai: retrospektyvinių išlaidų tarifas ir suplanuotų išlaidų tarifas. Retrospektyvinių išlaidų tarifas yra apskaičiuotas tarifas, kuris naudojamas kaip savikainos objekto paskirstymo bazės daugiklis. Tarifas apskaičiuojamas pagal ankstesnio laikotarpio išlaidų paskirstymus. Suplanuotas tarifas yra vartotojo nustatytas tarifas.

**Dimensijų hierarchija**

Yra dvi dimensijų hierarchijos: kategorijų hierarchija ir klasifikacijos hierarchiją. Dimensijų kategorizavimo hierarchijos tipas naudojamas ataskaitų rengimo tikslais. Jis palaiko tik išlaidų elemento dimensijas. Dimensijų klasifikacijos hierarchijos tipas naudojamas norint apibrėžti strategijas ir ataskaitų rengimo tikslais. Jis palaiko visas dimensijas, pavyzdžiui, išlaidų objektus, išlaidų elementus ir statistines dimensijas. 

**Duomenų jungtis**

Modulyje Kaštų apskaita duomenis iš šaltinio sistemų galima integruoti naudojant įvairias duomenų jungtis. Galima naudoti tolesnes duomenų jungtis.

-  Importuotos operacijos (sukonfigūruota iš anksto)
-  „Dynamics 365 for Finance and Operations“ (sukonfigūruota iš anksto)
-  „Dynamics AX“ (reikia sukonfigūruoti)

**Pastaba.** Duomenų jungtis Importuotos operacijos paremta duomenų objektais.

**Duomenų teikėjas**

Dauguma šaltinio sistemų gali pateikti duomenų, sutampančių su vienu ar keliais modulio Kaštų apskaita duomenų šaltiniais. Norint šaltinio sistemų duomenis sulygiuoti su modulio Kaštų apskaita duomenų šaltiniu, reikia sukonfigūruoti duomenų teikėją. Tolesnėje lentelėje išvardijama, kokius duomenų teikėjus galima naudoti su kiekviena duomenų jungtimi ir duomenų šaltiniu.

|  **Duomenų šaltiniai** |  **Duomenų jungtis Importuotos operacijos** | **Duomenų jungtis „Dynamics 365 for Finance and Operations“**  | **Duomenų jungtis „Dynamics AX“**  |
|---|---|---|---|
| Savikainos elemento dimensijos nariai  |  Taip | Taip  | Taip  |
|  Savikainos objekto dimensijos nariai |  Taip | Taip  | Taip  |
|  Statistinės dimensijos nariai | Taip  | Nr.  | Nr.  |
|  DK | Taip  | Taip  | Taip  |
|  Biudžeto įrašai  | Taip  | Taip  | Taip  |
|  Statistinės priemonės | Taip  | Taip  | Taip  |

**Formulė**

Naudodami formulės paskirstymo bazes galite nustatyti išplėstines formules, kad sukurtumėte teisingą paskirstymo bazę. Formulės paskirstymo bazes galite sukurti rankiniu būdu. Norėdami nurodyti savo formulę, galite naudoti toliau nurodytus operatorius.

|  **Simboliai** | **Tekstas**  |
|---|---|
|  ( ) | Skliausteliai  |
|  < |  Mažiau negu |
|  > |  Daugiau negu |
|  + |  Priedas |
|  – |  Atimtis |
| *  | Daugyba  |

Tradiciniai IF (jeigu) sakiniai nepalaikomi. Tačiau galite sukurti sakinius ir patikrinti, ar jie teisingi.

|  **Sakinių tikrinimas** | **Rezultatas**  |
|---|---|
|  a > b| True  |
|  a > b |  Netinkama |

**Pridėtinės išlaidos**

Pridėtinės išlaidos yra šiuo metu valdant verslą patiriamos išlaidos. Tai išlaidos, kurių negalima tiesiogiai susieti su konkrečia verslo veikla. Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.

-   Apskaitos mokesčiai
-   Nusidėvėjimas
-   Draudimas
-   Pomėgiai
-   Teisiniai mokesčiai
-   Mokesčiai
-   Išlaidos už komunalines paslaugas

**Pridėtinių išlaidų tarifas**

Tarifai apibrėžiami kiekvienam išlaidų objektui ir išlaidų elementui. Tarifai yra dviejų tipų: ataskaitinio laikotarpio ir nurodytas vartotojo. Ataskaitinio laikotarpio tarifai skaičiuojami skaičiuojant pridėtines išlaidas. Konkretaus vartotojo tarifą apibrėžia vartotojas ir jį galima naudoti norint paskirstyti išlaidas tarp išlaidų objektų iš anksto nustatytu tarifu, skaičiuojant pridėtines išlaidas.

**Publikuota**

Jei šiame lauke nustatysite parinktį Taip, darbo srityje Savikainos kontrolė ataskaitą galės peržiūrėti vartotojas, kuriam priskirtas vienas iš tolesnių vaidmenų.

-  Savikainos apskaitos vadovas
-  Išlaidų buhalteris
-  Išlaidų buhalteris
-  Savikainos objekto valdiklis

Jei šiame lauke nustatysite parinktį Ne, darbo srityje Savikainos kontrolė ataskaitą galės peržiūrėti tik tie vartotojai, kuriems priskirtas vienas iš tolesnių vaidmenų.

-  Savikainos apskaitos vadovas
-  Išlaidų buhalteris
-  Išlaidų buhalteris

**Statistinė dimensija**

Naudojant statistinę dimensiją ir jos narius, modulyje Kaštų apskaita registruojami ir kontroliuojami nepiniginiai įrašai. Statistinių dimensijų narius galima naudoti dviem tolesniais tikslais.

-  Kaip strategijų, pvz., išlaidų paskirstymo ir išlaidų priskyrimo, paskirstymo bazę.
-  Nepiniginiam naudojimui pranešti.

Statistinė dimensija yra veiklos skaičiaus arba sumos išraiška, kurią galima naudoti kaip paskirstymų arba tarifo skaičiavimų pagrindą. Ji sukuriama rankiniu būdu arba importuojama iš šaltinio sistemų. Statistinių dimensijų pavyzdžiai apima darbuotojų skaičių, kiekvieno prietaiso licencijuotos programinės įrangos skaičių, kiekvieno įrenginio elektros energijos sąnaudas arba išlaidų centro kvadratinių metrų plotą.

**Išrašas**

Išrašai yra už išlaidų valdymą atsakingiems vadovams skirti rodiniai. Išrašus apibrėžia išlaidų valdiklis ir juose pateikiama greita faktinių išlaidų, biudžetinių išlaidų ir nuokrypių apžvalga. Jei reikia, vadovas informaciją gali dar labiau detalizuoti. Siekiant užtikrinti, kad vadybininkai matytų tik tuos duomenis, už kuriuos yra atsakingi, išrašuose rodomiems duomenims taikomos prieigos taisyklės.

**Versija**

Norint modeliuoti, peržiūrėti ir palyginti įvairius rezultatus, naudojamos versijos. Pagal numatytuosius parametrus visos faktinės išlaidos rodomos vienoje pagrindinėje versijoje, vadinamoje *faktine*. Dirbdami su biudžetais ir atlikdami skaičiavimus galite dirbti su tiek versijų, kiek jums reikia. Pavyzdžiui, galite importuoti biudžeto duomenis į pradinę versiją, o po to peržiūrėti biudžetą pataisytoje versijoje. Atlikdami skaičiavimus galite sukurti kelias versijas. Tada šiose įvairiose versijose naudodami skirtingas skaičiavimo taisykles, kurios bus taikomos išlaidų paskirstymui, galite sukurti skaičiavimus.



