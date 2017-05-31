---
title: "Kaštų apskaitos terminija"
description: "Šioje temoje nurodomi pagrindiniai atliekant kaštų apskaitą naudojami terminai."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7ce12337c22542aea2002ffc5abd09e4f4d770c1
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="cost-accounting-terminology"></a>Kaštų apskaitos terminija

[!include[banner](../includes/banner.md)]


Šioje temoje nurodomi pagrindiniai atliekant kaštų apskaitą naudojami terminai.

**Kaštų apskaita**

Naudodami kaštų apskaitą galite rinkti duomenis iš įvairių šaltinių, pvz., didžiosios knygos, antrinių didžiųjų knygų, biudžetų ir statistinės informacijos. Tada galite analizuoti, apibendrinti ir įvertinti išlaidų duomenis, kad vadovybė galėtų priimti geriausius sprendimus dėl kainos atnaujinimų, biudžetų, išlaidų valdymo ir t. t. Išlaidų analizei naudojami šaltinio duomenys kaštų apskaitoje apdorojami atskirai. Todėl kaštų apskaitos naujinimai neturi įtakos šaltinio duomenims. Tačiau, kai surenkate išlaidų duomenis iš įvairių šaltinių ir ypač, kai importuojate pagrindines sąskaitas iš didžiosios knygos į „Microsoft Dynamics 365 for Operation“ kaip išlaidų elementus, duomenys dubliuojasi, nes tie patys duomenys yra didžiojoje knygoje ir kaštų apskaitoje. Šis dubliavimasis reikalingas, nes išorinėse ataskaitose naudojate finansinį valdymą, o vidinėse ataskaitose – kaštų apskaitą.

**Kaštų apskaitos didžioji knyga**

Kaštų apskaitos didžioji knyga yra specializuota sistema, kuri nustato, kaip tam tikroje kaštų apskaitos srityje įvedami ir pateikiami procesai, vertės ir kiekiai. Kaštų apskaitos didžiojoje knygoje nurodomi išlaidų objektų išlaidų matavimo procesai ir taisyklės. Joje tvarkomos išlaidų operacijos ir valdomi dokumentai, kuriuose įrašomi išlaidų operacijų sukurti vertės ir kiekio pokyčiai.

**Išlaidų įrašas**

Išlaidų įrašai atsiranda perkeliant iš didžiosios knygos įrašų, išlaidų paskirstymų ir išlaidų žurnaluose užregistruotų išlaidų įrašų, kai naudojamos duomenų jungtys.

**Išlaidų objektas**

Išlaidų objektai yra bet kokio tipo objektas, kuriam paskirstomos išlaidos. Toliau nurodomi įprasti išlaidų objektai.

-   Produktai
-   Projektai
-   Ištekliai
-   Padaliniai
-   Išlaidų centrai
-   Geografiniai regionai

Valdyba naudoja išlaidų objektus ne tik norėdama apskaičiuoti išlaidas, bet ir atlikti pelningumo analizę.

**Savikainos elementas**

Savikainos elementai naudojami kaip funkcija norint sekti ir kategorizuoti išlaidų srautą. Yra dviejų tipų savikainos elementai: pirminės išlaidos ir antrinės išlaidos. **Pirminės išlaidos** Pirminių išlaidų elementai nurodo išlaidų srautą iš finansinės apskaitos į kaštų apskaitą. Savikainos elemento struktūra atitinka pelno ir nuostolio sąskaitos struktūrą didžiojoje knygoje, kai savikainos elementas gali atitikti pagrindinę sąskaitą. Ne visos pagrindinės sąskaitos privalo būti pateikiamos kaip savikainos elementai, priklausomai nuo verslo poreikių. Toliau pateikiami kai kurie pirminių savikainos elementų pavyzdžiai.

-   Parduotų prekių savikaina (COG)
-   Netiesioginės medžiagų išlaidos
-   Personalo išlaidos
-   Energijos išlaidos

**Antrinių išlaidų elementas** 

Antriniai savikainos elementai atitinka vidinį išlaidų srautą, nes šios išlaidos sukurtos ir naudojamos tik kaštų apskaitoje. Antriniai savikainos elementai padeda užtikrinti, kad išlaidų šaltinis būtų atsekamas. Šie savikainos elementai naudojami savikainos paskirstymuose ir skaičiuojant papildomas išlaidas. Toliau pateikiami kai kurie antrinių savikainos elementų pavyzdžiai.

-   Gamybos išlaidos
-   Pridėtinės išlaidos už gamybą, medžiagas ir rinkodarą

**Savikainos kontrolės įtaisas**

Savikainos kontrolės įtaisas atitinka išlaidų struktūrą. Savikainos apskaitos didžiojoje knygoje jis turi būti susietas su savikainos objekto dimensijomis.

**Versija**

Norint modeliuoti, peržiūrėti ir palyginti įvairius rezultatus, naudojamos versijos. Pagal numatytuosius parametrus visos faktinės išlaidos rodomos vienoje pagrindinėje versijoje, vadinamoje *faktine*. Dirbdami su biudžetais ir atlikdami skaičiavimus galite dirbti su tiek versijų, kiek jums reikia. Pavyzdžiui, galite importuoti biudžeto duomenis į pradinę versiją, o po to peržiūrėti biudžetą pataisytoje versijoje. Atlikdami skaičiavimus galite sukurti kelias versijas. Tada šiose įvairiose versijose naudodami skirtingas skaičiavimo taisykles, kurios bus taikomos išlaidų paskirstymui, galite sukurti skaičiavimus.

**Išrašas**

Išrašai yra už išlaidų valdymą atsakingiems vadovams skirti rodiniai. Išrašus apibrėžia išlaidų valdiklis ir juose pateikiama greita faktinių ir biudžetinių išlaidų apžvalga ir netgi nuokrypiai ir skaičiavimo versijos. Siekiant užtikrinti, kad vadybininkai matytų tik tuos duomenis, už kuriuos yra atsakingi, išrašuose rodomiems duomenims taikomos prieigos taisyklės.

**Duomenų jungtis**

Duomenis į kaštų apskaitą gali būti importuojami iš išorinių sistemų naudojant duomenų jungtis. Pavyzdžiui, galite importuoti sąskaitų struktūras, dimensijas, didžiosios knygos įrašus ir biudžeto įrašus. Importuodami duomenis ir kurdami duomenų jungtis galite naudoti iš anksto sukonfigūruotas duomenų jungtis arba pasirinktines jungtis.

**Išlaidų klasifikavimas**

Naudojant išlaidų klasifikavimą išlaidos grupuojamos pagal jų bendro naudojimo savybes. Pavyzdžiui, išlaidas galima grupuoti pagal elementus, atsekamumą ir elgseną.

-   **Pagal elementus** – medžiagas, darbą ir išlaidas.
-   **Pagal atsekamumą** – tiesiogines išlaidas ir netiesiogines išlaidas. Tiesioginės išlaidos priskiriamos tiesiogiai savikainos objektams. Netiesioginės išlaidos nėra tiesiogiai susietos su savikainos objektais. Netiesioginės išlaidos paskirstomos savikainos objektams.
-   **Pagal elgseną** – fiksuotos, kintamosios ir pusiau kintamosios.

**Išlaidų elgsena**

Pagal elgseną išlaidos klasifikuojamos atsižvelgiant į jų elgseną esant pokyčių pagrindinėje verslo veikloje. Norint efektyviai valdyti išlaidas, vadovybė turi suprasti išlaidų elgseną. Yra trijų tipų išlaidų elgsenos modeliai: fiksuotos, kintamosios ir pusiau kintamosios.

- **Fiksuota savikaina** Fiksuota savikaina – tai išlaidos, kurios nekinta trumpuoju laikotarpiu nepaisant veiklos lygio pokyčių. Pavyzdžiui, fiksuotos išlaidos gali būti pagrindinės įmonės veiklos išlaidos, pvz., nuoma, kuri nesikeis net jei padidės arba sumažės veiklos lygis.

- **Kintamos išlaidos** Kintamos išlaidos kinta pagal veiklos lygio pokyčius. Pavyzdžiui, konkrečių tiesioginių medžiagų išlaidos yra susijusios su kiekvienu parduotu produktu. Kuo daugiau produktų parduodama, tuo didesnės tiesioginės išlaidos už medžiagas.

- **Pusiau kintamos išlaidos** Pusiau kintamos išlaidos yra iš dalies fiksuotos ir iš dalies kintamos išlaidos. Pavyzdžiui, interneto prieigos mokestis apima standartinį mėnesinį prieigos mokestį ir plačiajuostį naudojimo mokestį. Šis standartinis mėnesinis prieigos mokestis yra fiksuotos išlaidos, o plačiajuostis naudojimo mokestis yra kintamosios išlaidos.

**Pridėtinės išlaidos**

Pridėtinės išlaidos yra šiuo metu valdant verslą patiriamos išlaidos. Tai išlaidos, kurių negalima tiesiogiai susieti su konkrečia verslo veikla. Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.

-   Apskaitos mokesčiai
-   Nusidėvėjimas
-   Draudimas
-   Pomėgiai
-   Teisiniai mokesčiai
-   Mokesčiai
-   Išlaidos už komunalines paslaugas

**Išlaidų paskirstymas**

Išlaidų paskirstymas yra procesas, kurio metu priskiriamos ir paskirstomos išlaidos pagal pagrindines bendrųjų išlaidų priežastis. Paskirstote išlaidų sumas ir kiekius iš vieno savikainos objekto vienam ar keliems kitiems savikainos objektams. Pavyzdžiui, visos paslaugų išlaidos priskiriamos įvairiems bendrąjį biuro pastatą naudojantiems padaliniams.

**Išlaidų paskirstymo strategija**

Išlaidų paskirstymo strategijoje nurodomos sumos ir kiekiai, kurie turi būti paskirstyti. Paskirstymo taisyklės apima paskirstymo šaltinio taisykles, nurodančias, paskirstytas išlaidas ir paskirstymo tikslų taisykles, nurodančias, kur paskirstomos išlaidos. Pavyzdžiui, visos paslaugų išlaidos yra paskirstymo šaltinis, kurį galima paskirstyti įvairiems organizacijos padaliniams (t. y. paskirstymo tikslams).

**Paskirstymo bazė**

Paskirstymo bazė yra pagrindas, kurį galima naudoti norint išmatuoti ir nustatyti veiklų kiekį, pavyzdžiui, mašinos darbo valandų skaičių, suvartojamų kilovatvalandžių skaičių, sugaištas tiesioginio darbo valandas arba užimamą plotą kvadratinėmis pėdomis. Ji naudojama norint paskirstyti išlaidas į vieną ar kelis savikainos objektus.

**Paskirstymo principas**

Vienas iš paskirstymo principų yra paskirstyti išlaidas pagal išlaidų tarifą. Galite paskirstyti išlaidas naudodami faktinį laikotarpio tarifą arba retrospektyvinį tarifą. Naudojant abipusį metodą naudojantį paskirstymą galima lengviau užtikrinti, kad prieš atliekant paskirstymą naudojant faktinį laikotarpio tarifą paskirstymo bazė nustatoma pagal vienu metu atliekamas lygtis.

**Išlaidų sumavimas**

Išlaidų sumavimo paskirtis yra įtraukti visas pateikto savikainos objekto išlaidas. Telkimo lygį nustato vartotojas. Naudodami išlaidų sumavimą galite telkti išlaidų elementus, kurie turi būti paskirstomi iš vieno savikainos objekto kitam savikainos objektui. Kai išlaidų sumavimas nenaudojamas, kiekvienas išlaidų elementas paskirstomas iš vieno savikainos objekto kitam savikainos objektui.

**Išlaidų tarifo strategija**

Išlaidų tarifas naudojamas norint apskaičiuoti vieno savikainos objekto kainą. Norėdami suprasti kainos elementus, nurodote išlaidų tarifo strategijas. Yra dviejų tipų išlaidų tarifai: retrospektyvinių išlaidų tarifas ir suplanuotų išlaidų tarifas. Retrospektyvinių išlaidų tarifas yra apskaičiuotas tarifas, kuris naudojamas kaip savikainos objekto paskirstymo bazės daugiklis. Tarifas apskaičiuojamas pagal ankstesnio laikotarpio išlaidų paskirstymus. Suplanuotas tarifas yra vartotojo nustatytas tarifas.

**Dimensijų hierarchija**

Dimensijų hierarchijos naudojamos kaip ataskaitų struktūros nustatant paskirstymo, išlaidų tarifo ir išlaidų sumavimo taisyklės, programoje „Microsoft Excel“ peržiūrint išrašus arba duomenis ir nustatant prieigą prie sutelktų duomenų. Yra dvi dimensijų hierarchijos: kategorijų hierarchija ir klasifikacijos hierarchiją. Kategorijų hierarchija nustatoma pagal savikainos elementus, o klasifikacijos hierarchija nustatoma pagal savikainos objektus.

**Statistinė dimensija**

Statistinė dimensija yra objekto skaičiaus arba sumos išraiška, kurią galima naudoti kaip paskirstymų arba savikainos tarifo skaičiavimų pagrindą. Ji sukuriama rankiniu būdu arba importuojama iš šaltinio sistemų. Statistinių dimensijų pavyzdžiai apima darbuotojų skaičių, kiekvieno prietaiso licencijuotos programinės įrangos skaičių, kiekvieno įrenginio elektros energijos sąnaudas arba išlaidų centro kvadratinių metrų plotą.

**Statistinis įrašas**

Statistiniuose įrašuose įrašyta suma arba skaičiaus vertė atidedama nurodytai statistinei dimensijai. Įrašyta suma arba skaičiaus vertė dar vadinamos reikšme.




