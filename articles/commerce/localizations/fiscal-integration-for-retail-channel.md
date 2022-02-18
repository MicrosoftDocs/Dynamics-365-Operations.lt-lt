---
title: „Commerce“ kanalų fiskalinės integracijos apžvalga
description: Šioje temoje pateikiama fiskalinės integracijos galimybių, teikiamų „Dynamics 365 Commerce“, apžvalga.
author: EvgenyPopovMBS
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82913eaca1d56a5b0609480d8825717278eca132
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077197"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>„Commerce“ kanalų fiskalinės integracijos apžvalga

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Ši tema yra fiskalinės integracijos galimybių, teikiamų „Dynamics 365 Commerce“, apžvalga. 

Fiskalinė integracija apima integravimą įvairiais finansiniais įrenginiais ir tarnybomis, kurie užtikrina „Commerce“ pardavimo fiskalinę integraciją su vietos mokesčių įstatymais, kuriais siekiama užkirsti kelią mokesčių sukčiavimui mažmeninės prekybos srityje. Toliau pateikti keli įprasti scenarijai, kurių atveju būtų galima naudotis fiskaline integracija.

- Užregistruokite pardavimą finansiniame įrenginyje, prijungtame prie elektroninio kasos aparato (EKA), pvz., fiskalinio spausdintuvo, ir išspausdinkite klientui skirtą fiskalinį kvitą.
- Saugiai pateikite informaciją, susijusią su pardavimu ir grąžinimu, kurie yra užbaigti „Retail POS“, į išorinę žiniatinklio tarnybą, kurią valdo mokesčių inspekcija.
- Padėkite užtikrinti pardavimo operacijų duomenų nekeičiamumą naudodami skaitmeninius parašus.

Fiskalinės integracijos funkcija yra sistema, kuri suteikia bendrą „Retail POS“ ir finansinių įrenginių bei tarnybų integravimo tolesnės plėtros bei tinkinimo sprendimą. Funkcija taip pat apima fiskalinės integracijos pavyzdžius, kurie palaiko pagrindinius scenarijus konkrečiose šalyse ar regionuose ir kurie tinka konkretiems finansiniams įrenginiams arba tarnyboms. Fiskalinės integracijos pavyzdį sudaro keli „Commerce“ komponentų plėtiniai ir jis įtrauktas į programinės įrangos kūrimo rinkinį (SDK). Daugiau informacijos apie fiskalinės integracijos pavyzdžius žr. dalyje [„Commerce“ SDK fiskalinės integracijos pavyzdžiai](#fiscal-integration-samples-in-the-commerce-sdk). Informaciją, kaip įdiegti ir naudoti „Commerce“ SDK, žr. dalyje [Mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Tam, kad būtų palaikomi kiti scenarijai, kurių nepalaiko fiskalinės integracijos pavyzdys, būtų integruojama „Retail POS“ su kitais finansiniais įrenginiais ar tarnybomis arba būtų išpildomi kitų šalių ar regionų reikalavimai, turite išplėsti esamą fiskalinės integracijos pavyzdį arba sukurti naują pavyzdį naudodami dėl esamą pavyzdį kaip pavyzdį.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Fiskalinės registracijos procesas ir fiskalinės integracijos pavyzdžiai fiskaliniams įrenginiams ir paslaugoms

„Retail POS“ fiskalinės integracijos procesą gali sudaryti vienas ar daugiau veiksmų. Kiekvienas veiksmas apima konkrečių operacijų arba įvykių fiskalinę integraciją viename finansiniame įrenginyje arba tarnyboje. Šie sprendimo komponentai dalyvauja fiskalinėje registracijoje fiskaliniame įrenginyje ar paslaugoje:

- **Fiskalinių dokumentų teikėjas** – Šis komponentas nuosekliai sutvarko operacijų / įvykių duomenis tokiu formatu, kuris taip pat naudojamas sąveikai su fiskaliniu įrenginiu arba paslauga, analizuoja fiskalinio įrenginio ar paslaugos atsakymus ir išsaugo atsakymus kanalo duomenų bazėje. Plėtinys taip pat apibrėžia konkrečias operacijas ir įvykius, kurie turi būti registruojami.
- **Fiskalinė jungtis** – Šis komponentas inicijuoja ryšį su fiskaliniu įrenginiu arba paslauga, siunčia užklausas arba tiesiogines komandas fiskaliniam įrenginiui ar paslaugai, remdamasis operacijos / įvykio duomenimis, išgautais iš fiskalinio dokumento, ir gauna atsakymus iš fiskalinio įrenginio ar paslaugos.

Fiskalinės integracijos pavyzdyje gali būti „Commerce“ vykdymo laikas (CRT), Fiskalinių dokumentų teikėjo ir fiskalinės jungties aparatinės įrangos stotis ir POS plėtiniai. Jame taip pat yra tolesnių komponentų konfigūracijos.

- **Finansinio dokumento teikėjo konfigūracija** – ši konfigūracija nurodo finansinių dokumentų išvesties metodą ir formatą. Jame taip pat yra mokesčių ir mokėjimo metodų duomenų atvaizdas, kad mažmeninės prekybos POS duomenys būtų suderinami su fiskaliniame įrenginyje arba paslaugos programinėje įrangoje iš anksto nustatytomis vertėmis.
- **Fiskalinės jungties konfigūracija** – Ši konfigūracija apibrėžia fizinį ryšį su konkrečiu fiskaliniu įrenginiu arba paslauga.

Konkretaus EKA registro fiskalinės registracijos procesą apibrėžia atitinkamas parametras EKA funkcijų šablone. Norėdami gauti daugiau informacijos apie tai, kaip sukonfigūruoti fiskalinės registracijos procesą, įkelti mokesčių dokumentų teikėjo ir mokesčių jungties konfigūracijas bei pakeisti konfigūracijos parametrus, žr.[Nustatykite fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Toliau nurodytas tipiškas fiskalinės registracijos srautas prasideda įvykiu POS (pvz., pardavimo operacijos užbaigimu) ir įgyvendinama iš anksto nustatyta veiksmų seka, apimanti kitus prekybos komponentus (pvz.,CRT ir aparatinės įrangos stotis).

1. POS prašo fiskalinio dokumento iš fiskalinės integracijos sistemos (FIF).
1. FIF nustato, ar dabartiniam įvykiui reikalinga fiskalinė registracija.
1. Remdamasis fiskalinės registracijos proceso nustatymais, FIF nustato fiskalinę jungtį ir atitinkamą fiskalinių dokumentų teikėją, naudojamą fiskalinei registracijai.
1. FIF valdo fiskalinių dokumentų teikėją, kuris generuoja fiskalinį dokumentą (pavyzdžiui, XML dokumentą), atspindintį operaciją arba įvykį.
1. FIF grąžina sugeneruotą fiskalinį dokumentą į POS.
1. POS reikalauja, kad FIF pateiktų fiskalinį dokumentą fiskaliniam įrenginiui ar tarnybai.
1. FIF paleidžia fiskalinę jungtį, kuri apdoroja fiskalinį dokumentą ir pateikia jį fiskaliniam įrenginiui arba tarnybai.
1. FIF grąžina fiskalinį atsakymą (ty fiskalinio įrenginio ar paslaugos atsaką) į POS.
1. POS analizuoja fiskalinį atsaką, kad nustatytų, ar fiskalinė registracija buvo sėkminga. Jei reikia, POS prašo, kad FIF apdorotų visas įvykusias klaidas. 
1. POS prašo, kad FIF apdorotų ir išsaugotų fiskalinį atsakymą.
1. Fiskalinio dokumento teikėjas apdoroja fiskalinį atsakymą. Vykdydamas šį apdorojimą, mokesčių dokumento teikėjas analizuoja atsakymą ir iš jo ištraukia išplėstinius duomenis.
1. FIF išsaugo atsakymą ir išplėstinius duomenis kanalo duomenų bazėje.
1. Jei reikia, POS spausdina kvitą per įprastą kvitų spausdintuvą, kuris yra prijungtas prie aparatinės įrangos stoties. Kvite gali būti pateikti reikalingi duomenys iš fiskalinio atsakymo.
 
Toliau pateikti pavyzdžiai rodo fiskalinės registracijos vykdymo srautus tipiniams fiskaliniams įrenginiams arba paslaugoms.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Fiskalinė registracija atliekama per įrenginį, prijungtą prie aparatinės įrangos stoties

Ši konfigūracija naudojama, kai prie aparatinės įrangos stoties yra prijungtas fizinis fiskalinis įrenginys, pvz., mokesčių spausdintuvas. Tai taip pat taikoma, kai ryšys su fiskaliniu įrenginiu arba paslauga vykdomas naudojant programinę įrangą, įdiegtą aparatinės įrangos stotyje. Šiuo atveju mokesčių dokumento teikėjas yra adresu CRT, o fiskalinė jungtis yra aparatūros stotyje.

![Fiskalinė registracija atliekama per įrenginį, prijungtą prie aparatinės įrangos stoties.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Fiskalinė registracija atliekama per išorinę paslaugą

Ši konfigūracija naudojama, kai mokesčių registracija atliekama naudojant išorinę paslaugą, pvz., žiniatinklio paslaugą, kurią valdo mokesčių institucija. Šiuo atveju tiek mokesčių dokumentų teikėjas, tiek fiskalinė jungtis yra ant CRT.

![Fiskalinė registracija atliekama per išorinę paslaugą.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Fiskalinė registracija atliekama viduje CRT

Ši konfigūracija naudojama, kai fiskalinei registracijai nereikia išorinio fiskalinio įrenginio ar paslaugos. Pavyzdžiui, jis naudojamas, kai fiskalinė registracija atliekama skaitmeniniu būdu pasirašant pardavimo operacijas. Šiuo atveju tiek mokesčių dokumentų teikėjas, tiek fiskalinė jungtis yra ant CRT.

![Fiskalinė registracija atliekama viduje CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Fiskalinė registracija atliekama naudojant įrenginį arba paslaugą vietiniame tinkle

Ši konfigūracija naudojama, kai parduotuvės vietiniame tinkle yra fizinis fiskalinis įrenginys arba fiskalinė paslauga ir ji suteikia HTTPS taikomųjų programų programavimo sąsają (API). Šiuo atveju mokesčių dokumento teikėjas yra adresu CRT, o fiskalinė jungtis yra POS.

![Fiskalinė registracija atliekama naudojant įrenginį arba paslaugą vietiniame tinkle.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Klaidos taisymas

Fiskalinės integracijos sistema teikia toliau nurodytas parinktis, skirtas spręsti problemas, kylančias fiskalinės registracijos metu.

- **Kartoti** – operatoriai gali naudoti šią parinktį, kai problemą galima išspręsti greitai ir fiskalinę registraciją galima vykdyti iš naujo. Pvz., šią parinktį galima naudoti, kai finansinis įrenginys yra neprijungtas, fiskaliniame spausdintuve nėra popieriaus arba yra fiskaliniame spausdintuve kilo popieriaus strigtis.
- **Atšaukti** – ši parinktis operatoriams suteikia galimybę atidėti dabartinės operacijos arba įvykio fiskalinę registraciją, jei ji nepavyksta. Po registracija atidedama, operatorius gali tęsti darbą EKA ir baigti bet kokią operaciją, kuriai fiskalinė registracija nėra būtina. Kai EKA įvyksta bet koks įvykis, kuriam būtina fiskalinė registracija (pvz., atidaroma nauja operacija), automatiškai parodomas klaidų tvarkymo dialogo langas, kuris praneša operatoriui, kad ankstesnė operacija nebuvo tinkamai užregistruota, ir pateikia klaidų tvarkymo parinktis.
- **Praleisti** – operatoriai gali naudoti šią parinktį, kai tam tikromis aplinkybėmis galima praleisti fiskalinę registraciją ir reguliarias operacijas galima tęsti EKA. Pvz., šią parinktį galima naudoti, kai pardavimo operaciją, kurios fiskalinė registracija nepavyko, galima registruoti specialiame popieriniame žurnale.
- **Pažymėti kaip užregistruotą** – operatoriai gali naudoti šią parinktį, kai operacija iš tikrųjų buvo užregistruota finansiniame įrenginyje (pavyzdžiui, išspausdintas finansinis kvitas), bet kilo problema, kai finansinis atsakymas buvo įrašomas kanalo duomenų bazėje.
- **Atidėti** – Operatoriai gali naudoti šią parinktį, kai operacija nebuvo užregistruota, nes registravimo paslauga nepasiekiama. 

> [!NOTE]
> The **Praleisti**, **kaip registruotą**, ir **Atidėti** parinktys turi būti suaktyvintos fiskalinės registracijos procese prieš jas naudojant. Be to, operatoriams turi būti suteiktos atitinkamos teisės.

The **Praleisti**, **kaip registruotą**, ir **Atidėti** parinktys leidžia informacijos kodams užfiksuoti tam tikrą informaciją apie gedimą, pvz., gedimo priežastį arba pateisinimą praleisti fiskalinę registraciją arba pažymėti, kad operacija yra registruota. Daugiau informacijos apie tai, kaip nustatyti klaidų tvarlymo parametrus, žr. [Klaidų tvarkymo parametrai](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Nebūtina fiskalinė registracija

Fiskalinė registracija gali būti privaloma tik atliekant tam tikras operacijas. Pavyzdžiui, įprastų pardavimų ir grąžinimų atveju fiskalinė registracija gali būti privaloma, bet su kliento mokama suma susijusių operacijų fiskalinė registracija nebūtina. Neatlikus pardavimo fiskalinės registracijos, kiti pardavimai blokuojami, o neatlikus kliento mokamos sumos fiskalinės registracijos kiti pardavimai neblokuojami. Tam, kad galėtumėte atskirti privalomas ir neprivalomas operacijas, rekomenduojame jas atliekant naudotis skirtingų dokumentų teikėjų paslaugomis ir nustatyti atskirus tų teikėjų fiskalinės registracijos proceso etapus. Parametras **Tęsti įvykus klaidai** turi būti įgalintas atliekant bet kokį su nebūtina fiskaline registracija susijusį veiksmą. Daugiau informacijos apie tai, kaip nustatyti klaidų tvarlymo parametrus, žr. [Klaidų tvarkymo parametrai](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Rankiniu būdu iš naujo paleiskite fiskalinę registraciją

Jei įvykus klaidai (pvz., klaidų tvarkymo dialogo lange operatoriui paspaudus **Atšaukti**) operacijos arba įvykio fiskalinė registracija atidėta, suaktyvinę atitinkamą operaciją galite patys iš naujo paleisti fiskalinę registraciją. Daugiau informacijos rasite [Rankinio atidėtos fiskalinės registracijos vykdymo įgalinimas](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Atidėti variantą

The **Atidėti** parinktis leidžia tęsti fiskalinės registracijos procesą, jei dabartinis veiksmas nepavyksta. Jis gali būti naudojamas, kai yra fiskalinės registracijos atsarginė parinktis.

### <a name="fiscal-registration-health-check"></a>Fiskalinės registracijos būsenos patikra

Atliekant fiskalinės registracijos būsenos patikros procedūrą patikrinamas finansinio įrenginio ar paslaugos prieinamumas įvykus tam tikriems įvykiams. Jei šiuo metu fiskalinės registracijos atlikti neįmanoma, apie tai iš anksto pranešama operatoriui.

EKA būsenos patikrą atlieka įvykus toliau išvardytiems įvykiams.

- Atidaroma nauja operacija.
- Atšaukiama sulaikyta operacija.
- Užbaigiama pardavimo arba grąžinimo operacija.

Jei būsenos patikros rezultatai neigiami, EKA rodomas būsenos patikros dialogo langas. Šiame dialogo lange rodomi toliau išvardyti mygtukai.

- **Gerai** – paspaudęs šį mygtuką operatorius gali nepaisyti būsenos patikros klaidos ir toliau vykdyti operaciją. Operatoriai gali paspausti šį mygtuką tik tuo atveju, jei jiems įgalinta teisė **Leisti nepaisyti būsenos patikros klaidos**.
- **Atšaukti** – operatoriui paspaudus šį mygtuką, EKA atšaukia paskutinį veiksmą (pvz., prekė neįtraukiama į naują operaciją).

> [!NOTE]
> Sveikatos patikrinimas vykdomas tik tuo atveju, jei dabartinei operacijai reikalinga fiskalinė registracija ir jei **Tęskite klaidą** parametras yra išjungtas dabartiniam fiskalinės registracijos proceso veiksmui. Daugiau informacijos rasite [Klaidų tvarkymo parametrų nustatymas](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Finansinio atsakymo saugojimas finansinėje operacijoje

Kai operacijos arba įvykio fiskalinė registracija sėkminga, finansinė operacija sukuriama kanalo duomenų bazėje ir susiejama su pradine operacija arba įvykiu. Be to, pasirenkama nepavykusios finansinės registracijos parinktis **Praleisti** arba **Pažymėti kaip užregistruotą**, ši informacija yra saugoma finansinėje operacijoje. Finansinėje operacijoje saugomas finansinis atsakymas iš finansinio įrenginio ar tarnybos. Jei fiskalinės registracijos procesą sudaro keli etapai, finansinė operacija sukuriamas atliekant kiekvieną proceso veiksmą, po kurio registracija pavyko arba nepavyko.

*P užduotis* perkelia finansines operacijas į Būstinę kartu su operacijomis. Puslapio **Parduotuvės operacijos** „FastTab“ **Finansinės operacijos** galite peržiūrėti finansines operacijas, susietas su operacijomis.

Finansinėje operacijoje saugoma toliau nurodyta informacija.

- Fiskalinės registracijos proceso informacija (procesas, jungčių grupė, jungtis ir t. t.). Jos lauke **Registro numeris** taip pat saugomas finansinio įrenginio serijos numeris, jei ši informacija įtraukta į finansinį atsakymą.
- Fiskalinės registracijos būsena: **Užbaigta** už sėkmingą registraciją, **Praleistas** jei operatorius pasirinko **Praleisti** nepavykusios registracijos galimybė, **Pažymėta kaip registruota** jei operatorius pasirinko **Pažymėti kaip registruotą** variantas arba **Atidėtas** jei operatorius pasirinko **Atidėti** variantas.
- Informacijos kodo operacijos, susijusios su pasirinkta finansine operacija. Norėdami peržiūrėti informacijos kodo operacijas, apsilankykite **Fiskalinės operacijos** FastTab, pasirinkite fiskalinę operaciją, kurios būsena **Praleistas**, **kaip registruota**, arba **Atidėtas**, tada pasirinkite **Info kodo operacijos**.

Pasirinkę **Išplėstiniai duomenys**, taip pat galite peržiūrėti kai kurias fiskalinės operacijos ypatybes. Ypatybių, kurias galima peržiūrėti, sąrašas priklauso nuo konkrečios fiskalinio registravimo funkcijos, kuri sugeneravo fiskalinę operaciją. Pavyzdžiui, naudodami Prancūzijos skaitmeninio parašo funkcijas, galite peržiūrėti skaitmeninį parašą, sekos numerį, sertifikato kontrolinį kodą, maišos algoritmo identifikaciją ir kitas fiskalinių operacijų ypatybes.

## <a name="fiscal-texts-for-discounts"></a>Nuolaidų finansinis tekstas

Kai kuriose šalyse ar regionuose taikomi specialūs reikalavimai dėl papildomo teksto, kuris turi būti išspausdintas ant finansinių kvitų, kai taikomas skirtingų tipų nuolaidos. Fiskalinės integracijos funkcija suteikia galimybę nustatyti specialų nuolaidos tekstą, kuris išspausdinamas po nuolaidos eilute finansiniame kvite. Jei nuolaidos neautomatinės, galite sukonfigūruoti finansinį tekstą, taikomą informacijos kodui, nurodytam EKA funkcijų šablono informacijos kode **Produkto nuolaida**. Daugiau informacijos apie tai, kaip nustatyti nuolaidų finansinį tekstą, žr. [Nuolaidų finansinio teksto nustatymas](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Finansinių X ir Z ataskaitų spausdinimas

Fiskalinės integracijos funkcija palaiko konkretaus integruoto finansinio įrenginio arba tarnybos dienos pabaigos išrašų generavimą.

- Nauji mygtukai, kurie vykdo atitinkamas operacijas, turėtų būti įtraukti į EKA ekrano maketą. Daugiau informacijos žr. [Finansinio X / Z ataskaitų nustatymas iš EKA](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Fiskalinės integracijos pavyzdyje šios operacijos turėtų būti sugretintos su atitinkamomis finansinio įrenginio operacijomis.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>„Commerce“ SDK fiskalinės integracijos pavyzdžiai

Toliau pateikti fiskalinės integracijos pavyzdžiai šiuo metu teikiami „Commerce“ SDK rinkinyje.

- [Fiskalinio spausdintuvo integracijos pavyzdys (Italija)](./emea-ita-fpi-sample.md)
- [Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)](./emea-pol-fpi-sample.md)
- [Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai](./emea-aut-fi-sample.md)
- [Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Čekijos Respublikai](./emea-cze-fi-sample.md)
- [Švedijos kontrolės įtaiso integracijos pavyzdys](./emea-swe-fi-sample.md)
- [Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Vokietijai](./emea-deu-fi-sample.md)
- [Fiskalinio spausdintuvo integracijos pavyzdys Rusija](./rus-fpi-sample.md)

Tolesnės fiskalinio integravimo funkcijos taip pat įdiegiamos naudojant fiskalinio integravimo sistemą, bet jos jau yra perengtos naudoti ir nėra įtrauktos į „Commerce“ SDK.

- [Fiskalinis registravimas Brazilijoje](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Prancūzijos skaitmeninis parašas](./emea-fra-cash-registers.md)

Toliau nurodytos fiskalinės integracijos funkcijos taip pat teikiamos „Commerce“ SDK rinkinyje, bet šiuo metu ji nenaudoja fiskalinės integracijos sistemos. Šios funkcijos perkėlimas į fiskalinės integracijos sistemą planuojama vėlesniuose naujinimuose.

- [Norvegijos skaitmeninis parašas](./emea-nor-cash-registers.md)

Tolesnė senoji fiskalinės integracijos funkcija, kuri pasiekiama „Commerce“ SDK rinkinyje, nenaudoja fiskalinio integravimo sistemos ir nebus pasiekiama vėlesniuose naujinimuose.

- [Švedijos kontrolės įtaiso integracijos pavyzdys (senoji)](./retail-sdk-control-unit-sample.md)
- [Prancūzijos skaitmeninis parašas (senoji versija)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
