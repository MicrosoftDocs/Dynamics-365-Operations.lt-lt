---
title: Mažmeninės prekybos kanalų fiskalinės integracijos apžvalga
description: Šioje temoje pateikiama fiskalinės integracijos galimybių, teikiamų „Microsoft Dynamics 365 for Retail“, apžvalga.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: c6fcc93cfed35d73ae749856f33857ba84dbfd82
ms.sourcegitcommit: 70aeb93612ccd45ee88c605a1a4b87c469e3ff57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/01/2019
ms.locfileid: "773282"
---
# <a name="overview-of-fiscal-integration-for-retail-channels"></a>Mažmeninės prekybos kanalų fiskalinės integracijos apžvalga

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Įžanga

Ši tema yra fiskalinės integracijos galimybių, teikiamų „Microsoft Dynamics 365 for Retail“, apžvalga. Fiskalinė integracija apima integravimą įvairiais finansiniais įrenginiais ir tarnybomis, kurie užtikrina mažmeninės prekybos pardavimo fiskalinę integraciją su vietos mokesčių įstatymais, kuriais siekiama užkirsti kelią mokesčių sukčiavimui mažmeninės prekybos srityje. Toliau pateikti keli įprasti scenarijai, kurių atveju būtų galima naudotis fiskaline integracija.

- Užregistruokite mažmeninės prekybos pardavimą finansiniame įrenginyje, prijungtame prie mažmeninės prekybos elektroninio kasos aparato (EKA), pvz., fiskalinio spausdintuvo, ir išspausdinkite klientui skirtą fiskalinį kvitą.
- Saugiai pateikite informaciją, susijusią su pardavimu ir grąžinimu, kurie yra užbaigti „Retail POS“, į išorinę žiniatinklio tarnybą, kurią valdo mokesčių inspekcija.
- Padėkite užtikrinti pardavimo operacijų duomenų nekeičiamumą naudodami skaitmeninius parašus.

Mažmeninės prekybos fiskalinės integracijos funkcija yra sistema, kuri suteikia bendrą „Retail POS“ ir finansinių įrenginių bei tarnybų integravimo tolesnės plėtros bei tinkinimo sprendimą. Funkcija taip pat apima fiskalinės integracijos pavyzdžius, kurie palaiko pagrindinius mažmeninės prekybos scenarijus konkrečiose šalyse ar regionuose ir kurie tinka konkretiems finansiniams įrenginiams arba tarnyboms. Fiskalinės integracijos pavyzdį sudaro keli mažmeninės prekybos komponentų plėtiniai ir jis įtrauktas į mažmeninės prekybos programinės įrangos kūrimo rinkinį (SDK). Daugiau informacijos apie fiskalinės integracijos pavyzdžius, kurie teikiami mažmeninės prekybos SDK, žr. [Fiskalinės integracijos pavyzdžiai mažmeninės prekybos SDK](#fiscal-integration-samples-in-the-retail-sdk). Informacijos apie tai, kaip įdiegti ir naudoti mažmeninės prekybos SDK, žr. [Mažmeninės prekybos SDK peržiūra](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Tam, kad būtų palaikomi kiti scenarijai, kurių nepalaiko fiskalinės integracijos pavyzdys, būtų integruojama „Retail POS“ su kitais finansiniais įrenginiais ar tarnybomis arba būtų išpildomi kitų šalių ar regionų reikalavimai, turite išplėsti esamą fiskalinės integracijos pavyzdį arba sukurti naują pavyzdį naudodami dėl esamą pavyzdį kaip pavyzdį.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Finansinių įrenginių fiskalinės integracijos procesas ir fiskalinės integracijos pavyzdžiai

„Retail POS“ fiskalinės integracijos procesą gali sudaryti vienas ar daugiau veiksmų. Kiekvieną veiksmas apima konkrečių mažmeninės prekybos operacijų arba įvykių fiskalinę integraciją viename finansiniame įrenginyje arba tarnyboje. Toliau nurodyti sprendimo komponentai įtraukti į fiskalinę integraciją finansiniame įrenginyje, kuris prijungtas prie aparatūros stoties.

- **„Commerce Runtime“ (CRT) plėtinys** – šis komponentas sudėlioja mažmeninės prekybos operacijos / įvykio duomenis tokiu formatu, kuris taip pat naudojamas sąveikaujant su finansiniu įrenginiu, analizuoja atsakymus iš finansinio įrenginio ir saugo atsakymus kanalo duomenų bazėje. Plėtinys taip pat apibrėžia konkrečias operacijas ir įvykius, kurie turi būti registruojami. Šis komponentas yra dažnai vadinamas *finansinio dokumento teikėju*.
- **Aparatūros stoties plėtinys** – šis komponentas inicijuoja ryšį su finansiniu įrenginiu, siunčia užklausas ir teikia komandas finansiniam įrenginiui pagal mažmeninės prekybos operacijos / įvykio duomenis, kurie gaunami iš finansinio dokumento, ir gauna atsakymus iš finansinio įrenginio. Šis komponentas yra dažnai vadinamas *fiskaline jungtimi*.

Finansinio įrenginio fiskalinės integracijos pavyzdyje pateikiami CRT ir aparatūros stoties plėtiniai, atitinkamai skirti finansinio dokumento teikėjo ir fiskalinei jungčiai. Jame taip pat yra tolesnių komponentų konfigūracijos.

- **Finansinio dokumento teikėjo konfigūracija** – ši konfigūracija nurodo finansinių dokumentų išvesties metodą ir formatą. Jame taip pat pateikiamas mokesčių ir mokėjimo metodų duomenų susiejimas, kad „Retail POS“ duomenys būtų suderinami su iš anksto nustatytomis finansinio įrenginio programinės aparatinės įrangos reikšmėmis.
- **Fiskalinės jungties konfigūracija** – ši konfigūracija apibrėžia faktinį ryšį su konkrečiu finansiniu įrenginiu.

Konkretaus EKA registro fiskalinės registracijos procesą apibrėžia atitinkamas parametras EKA funkcijų šablone. Daugiau informacijos apie tai, kaip konfigūruoti fiskalinės registracijos procesą, įkelti finansinio dokumento teikėjo ir fiskalinės jungties konfigūracijas bei keisti jų parametrus, žr. [Fiskalinės registracijos proceso nustatymas](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Toliau pateiktame pavyzdyje parodytas įprasta finansinio įrenginio fiskalinės registracijos vykdymo eiga. Eiga prasideda nuo įvykio EKA (pvz., pardavimo operacijos užbaigimo) ir nustato toliau nurodytą veiksmų seką.

1. EKA reikalauja finansinio dokumento iš CRT.
2. CRT nustato, ar dabartinis įvykiam įvykiui būtina fiskalinė registracija.
3. Remiantis fiskalinės registracijos proceso parametrais, CRT identifikuoja fiskalinę jungtį ir atitinkamą finansinio dokumento teikėją, kurie bus naudojami atliekant fiskalinę registraciją.
4. CRT paleidžia finansinio dokumento teikėją, kuris sugeneruoja finansinį dokumentą (pvz., XML dokumentą), nurodantį mažmeninės prekybos operaciją arba įvykį.
5. EKA aparatūros stočiai siunčia CRT paruoštą finansinį dokumentą.
6. Aparatūros stotis paleidžia fiskalinę jungtį, kuri apdoroja finansinį dokumentą ir pateikia jo informaciją finansiniam įrenginiui arba tarnybai.
7. EKA analizuoja atsakymą iš finansinio įrenginio arba tarnybos ir nustato, ar fiskalinė registracija atlikta sėkmingai.
8. CRT įrašo atsakymą kanalo duomenų bazėje.

![Sprendimo schema](media/emea-fiscal-integration-solution.png "Sprendimo schema")

## <a name="error-handling"></a>Klaidos taisymas

Fiskalinės integracijos sistema teikia toliau nurodytas parinktis, skirtas spręsti problemas, kylančias fiskalinės registracijos metu.

- **Kartoti** – operatoriai gali naudoti šią parinktį, kai problemą galima išspręsti greitai ir fiskalinę registraciją galima vykdyti iš naujo. Pvz., šią parinktį galima naudoti, kai finansinis įrenginys yra neprijungtas, fiskaliniame spausdintuve nėra popieriaus arba yra fiskaliniame spausdintuve kilo popieriaus strigtis.
- **Atšaukti** – ši parinktis operatoriams suteikia galimybę atidėti dabartinės operacijos arba įvykio fiskalinę registraciją, jei ji nepavyksta. Po registracija atidedama, operatorius gali tęsti darbą EKA ir baigti bet kokią operaciją, kuriai fiskalinė registracija nėra būtina. Kai EKA įvyksta bet koks įvykis, kuriam būtina fiskalinė registracija (pvz., atidaroma nauja operacija), automatiškai parodomas klaidų tvarkymo dialogo langas, kuris praneša operatoriui, kad ankstesnė operacija nebuvo tinkamai užregistruota, ir pateikia klaidų tvarkymo parinktis.
- **Praleisti** – operatoriai gali naudoti šią parinktį, kai tam tikromis aplinkybėmis galima praleisti fiskalinę registraciją ir reguliarias operacijas galima tęsti EKA. Pvz., šią parinktį galima naudoti, kai pardavimo operaciją, kurios fiskalinė registracija nepavyko, galima registruoti specialiame popieriniame žurnale.
- **Pažymėti kaip užregistruotą** – operatoriai gali naudoti šią parinktį, kai operacija iš tikrųjų buvo užregistruota finansiniame įrenginyje (pavyzdžiui, išspausdintas finansinis kvitas), bet kilo problema, kai finansinis atsakymas buvo įrašomas kanalo duomenų bazėje.

> [!NOTE]
> Parinktys **Praleisti** ir **Pažymėti kaip užregistruotą** turi būti suaktyvintos fiskalinės registracijos proceso metu, kad jas būtų galima naudoti. Be to, operatoriams turi būti suteiktos atitinkamos teisės.

Parinktys **Praleisti** ir **Pažymėti kaip užregistruotą** suteikia galimybę informacijos kodams užfiksuoti šiek tiek konkrečios informacijos apie triktį, pvz., gedimo priežastį, fiskalinės registracijos praleidimo priežastį arba operacijos pažymėjimo užregistruota priežastį. Daugiau informacijos apie tai, kaip nustatyti klaidų tvarlymo parametrus, žr. [Klaidų tvarkymo parametrai](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Finansinio atsakymo saugojimas finansinėje operacijoje

Kai operacijos arba įvykio fiskalinė registracija sėkminga, finansinė operacija sukuriama kanalo duomenų bazėje ir susiejama su pradine operacija arba įvykiu. Be to, pasirenkama nepavykusios finansinės registracijos parinktis **Praleisti** arba **Pažymėti kaip užregistruotą**, ši informacija yra saugoma finansinėje operacijoje. Finansinėje operacijoje saugomas finansinis atsakymas iš finansinio įrenginio ar tarnybos. Jei fiskalinės registracijos procesą sudaro keli etapai, finansinė operacija sukuriamas atliekant kiekvieną proceso veiksmą, po kurio registracija pavyko arba nepavyko.

*P užduotis* perkelia finansines operacijas į mažmeninių pardavimų valdymą kartu su mažmeninės prekybos operacijomis. Puslapio **Mažmeninės prekybos parduotuvės operacijos** „FastTab“ **Finansinės operacijos** galite peržiūrėti finansines operacijas, susietas su mažmeninės prekybos operacijomis.


Finansinėje operacijoje saugoma toliau nurodyta informacija.

- Fiskalinės registracijos proceso informacija (procesas, jungčių grupė, jungtis ir t. t.). Jos lauke **Registro numeris** taip pat saugomas finansinio įrenginio serijos numeris, jei ši informacija įtraukta į finansinį atsakymą.
- Fiskalinės registracijos būsena: **Baigta**, jei registracija baigta sėkmingai, **Praleista**, jei operatorius pasirinko parinktį **Praleisti**, kai registracija nepavyko, arba **Pažymėta kaip užregistruota**, jei operatorius pasirinko parinktį **Pažymėti kaip užregistruotą**.
- Informacijos kodo operacijos, susijusios su pasirinkta finansine operacija. Norėdami peržiūrėti informacijos kodų operacijas, „FastTab“ **Finansinės operacijos** pasirinkite finansinę operaciją, kurios būsena yra **Praleista** arba **Pažymėta kaip užregistruota**, tada pasirinkite **Informacijos kodų operacijos**.

## <a name="fiscal-texts-for-discounts"></a>Nuolaidų finansinis tekstas

Kai kuriose šalyse ar regionuose taikomi specialūs reikalavimai dėl papildomo teksto, kuris turi būti išspausdintas ant finansinių kvitų, kai taikomas skirtingų tipų nuolaidos. Fiskalinės integracijos funkcija suteikia galimybę nustatyti specialų nuolaidos tekstą, kuris išspausdinamas po nuolaidos eilute finansiniame kvite. Jei nuolaidos neautomatinės, galite sukonfigūruoti finansinį tekstą, taikomą informacijos kodui, nurodytam EKA funkcijų šablono informacijos kode **Produkto nuolaida**. Daugiau informacijos apie tai, kaip nustatyti nuolaidų finansinį tekstą, žr. [Nuolaidų finansinio teksto nustatymas](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Finansinių X ir Z ataskaitų spausdinimas

Fiskalinės integracijos funkcija palaiko konkretaus integruoto finansinio įrenginio arba tarnybos dienos pabaigos išrašų generavimą.

- Nauji mygtukai, kurie vykdo atitinkamas operacijas, turėtų būti įtraukti į EKA ekrano maketą. Daugiau informacijos žr. [Finansinio X / Z ataskaitų nustatymas iš EKA](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Fiskalinės integracijos pavyzdyje šios operacijos turėtų būti sugretintos su atitinkamomis finansinio įrenginio operacijomis.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Mažmeninės prekybos SDK fiskalinės integracijos pavyzdžiai

Toliau pateikti fiskalinės integracijos pavyzdžiai šiuo metu teikiami „Retail SDK“, kuris leidžiamas kartu su „Retail“.

- [Fiskalinio spausdintuvo integracijos pavyzdys (Italija)](emea-ita-fpi-sample.md)
- [Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)](emea-pol-fpi-sample.md)

Toliau nurodyta fiskalinės integracijos funkcija taip pat teikiama „Retail SDK“, bet šiuo metu ji nenaudoja fiskalinės integracijos sistemos. Šios funkcijos perkėlimas į fiskalinės integracijos sistemą planuojama vėlesniuose naujinimuose.

- [Prancūzijos skaitmeninis parašas](emea-fra-cash-registers.md)
- [Norvegijos skaitmeninis parašas](emea-nor-cash-registers.md)
- [Švedijos kontrolės įtaiso integracijos pavyzdys](./retail-sdk-control-unit-sample.md)

