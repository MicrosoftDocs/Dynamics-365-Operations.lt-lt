---
title: "\"Commerce\" kanalų finansinio integravimo apžvalga"
description: Šioje temoje pateikiama fiskalinės integracijos galimybių, teikiamų „Dynamics 365 Commerce“, apžvalga.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 46e0afd5a8cb692da56a7d5f261ca30d9b3aaa80
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388318"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>"Commerce" kanalų finansinio integravimo apžvalga

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Ši tema yra fiskalinės integracijos galimybių, teikiamų „Dynamics 365 Commerce“, apžvalga. 

Fiskalinė integracija apima integravimą įvairiais finansiniais įrenginiais ir tarnybomis, kurie užtikrina „Commerce“ pardavimo fiskalinę integraciją su vietos mokesčių įstatymais, kuriais siekiama užkirsti kelią mokesčių sukčiavimui mažmeninės prekybos srityje. Toliau pateikti keli įprasti scenarijai, kurių atveju būtų galima naudotis fiskaline integracija.

- Užregistruokite pardavimą finansiniame įrenginyje, prijungtame prie elektroninio kasos aparato (EKA), pvz., fiskalinio spausdintuvo, ir išspausdinkite klientui skirtą fiskalinį kvitą.
- Saugiai pateikite informaciją, susijusią su pardavimu ir grąžinimu, kurie yra užbaigti „Retail POS“, į išorinę žiniatinklio tarnybą, kurią valdo mokesčių inspekcija.
- Padėti užtikrinti pardavimo operacijų duomenų neįgalumą naudojant skaitmeninius parašus.

Fiskalinės integracijos funkcija yra sistema, kuri suteikia bendrą „Retail POS“ ir finansinių įrenginių bei tarnybų integravimo tolesnės plėtros bei tinkinimo sprendimą. Funkcija taip pat apima fiskalinės integracijos pavyzdžius, kurie palaiko pagrindinius scenarijus konkrečiose šalyse ar regionuose ir kurie tinka konkretiems finansiniams įrenginiams arba tarnyboms. Fiskalinės integracijos pavyzdį sudaro keli „Commerce“ komponentų plėtiniai ir jis įtrauktas į programinės įrangos kūrimo rinkinį (SDK). Daugiau informacijos apie fiskalinės integracijos pavyzdžius žr. dalyje [„Commerce“ SDK fiskalinės integracijos pavyzdžiai](#fiscal-integration-samples-in-the-commerce-sdk). Informaciją, kaip įdiegti ir naudoti „Commerce“ SDK, žr. dalyje [Mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Tam, kad būtų palaikomi kiti scenarijai, kurių nepalaiko fiskalinės integracijos pavyzdys, būtų integruojama „Retail POS“ su kitais finansiniais įrenginiais ar tarnybomis arba būtų išpildomi kitų šalių ar regionų reikalavimai, turite išplėsti esamą fiskalinės integracijos pavyzdį arba sukurti naują pavyzdį naudodami dėl esamą pavyzdį kaip pavyzdį.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Finansinio įrenginių ir paslaugų finansinio registravimo procesas ir finansinio integravimo pavyzdžiai

„Retail POS“ fiskalinės integracijos procesą gali sudaryti vienas ar daugiau veiksmų. Kiekvienas veiksmas apima konkrečių operacijų arba įvykių fiskalinę integraciją viename finansiniame įrenginyje arba tarnyboje. Šie sprendimo komponentai dalyvauja finansinio įrenginio arba paslaugos finansinio įrenginio registracijoje:

- **Fiskalinio dokumento** teikėjas – šis komponentas eilutėmis išduoja operacijos/įvykio duomenis formatu, kuris taip pat naudojamas sąveikoje su fiskaliniu įrenginiu ar paslauga, išanalizuoti atsakymus iš fiskalinio įrenginio ar paslaugos ir saugomi atsakymai kanalo duomenų bazėje. Plėtinys taip pat apibrėžia konkrečias operacijas ir įvykius, kurie turi būti registruojami.
- **Fiskalinė** jungtis – šis komponentas inicijuoja ryšį su fiskaliniu įrenginiu arba paslauga, siunčia užklausas arba tiesiogines komandas į fiskalinį įrenginį arba paslaugą, remiantis operacijos / įvykio duomenimis, kurie išskleisti iš fiskalinio dokumento, ir gauna atsakymus iš fiskalinio įrenginio arba paslaugos

Finansinio integravimo pavyzdyje gali būti "Commerce Runtime (CRT), Hardware" stotis ir finansinio dokumento teikėjo ir "Fiscal Connector" EKA plėtiniai. Jame taip pat yra tolesnių komponentų konfigūracijos.

- **Finansinio dokumento teikėjo konfigūracija** – ši konfigūracija nurodo finansinių dokumentų išvesties metodą ir formatą. Be to, joje yra mokesčių ir mokėjimo metodų duomenų susiejimas, siekiant, kad duomenys iš "Retail POS" būtų suderinami su vertėmis, kurios iš anksto nustatytos fiskalinio įrenginio arba paslaugos metode.
- **Iždo jungties** konfigūracija – ši konfigūracija apibrėžia fizinį ryšį su konkrečiu fiskaliniu įrenginiu arba paslauga.

Konkretaus EKA registro fiskalinės registracijos procesą apibrėžia atitinkamas parametras EKA funkcijų šablone. Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti finansinio registravimo procesą, įkelti finansinio dokumento teikėją ir finansinių jungčių konfigūracijas ir keisti konfigūracijos parametrus, [žr. Finansinio registravimo proceso nustatymą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Jei reikia nefinansinių operacijų įrenginių, pvz., produktų katalogo ieškos, klientų peržvalgos ar operacijos juodraščio kūrimo, galite pasirinkti juos kaip registrus, kuriems taikomi finansinio proceso apribojimai. Norėdami gauti daugiau informacijos, žr [. Registrų, kuriuose taikomi finansinio registravimo apribojimai, rinkinį](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Toliau pateiktas įprastas finansinio registravimo srautas prasideda įvykiu EKA (pvz., pardavimo operacijos galutinis procesas) ir įdiegia iš anksto nustatytą veiksmų seką, apimamą kitų "Commerce" komponentų (CRT pvz., "Hardware" stoties).

1. EKA prašo finansinio dokumento iš finansinio integravimo sistemos (FIF).
1. FIF nustato, ar dabartiniam įvykiui reikia finansinio registravimo.
1. Pagal finansinio registravimo proceso parametrus FIF identifikuoja fiskalinę jungtį ir atitinkamą fiskalinio dokumento teikėją, kad jis būtų naudojamas registruojant finansinius duomenis.
1. FIF vykdo fiskalinio dokumento teikėją, kuris sugeneruoja fiskalinį dokumentą (pvz., XML dokumentą), kuris rodo operaciją ar įvykį.
1. FIF grąžina sugeneruotą fiskalinį dokumentą į EKA.
1. EKA užklausos, kad FIF pateiktų fiskalinį dokumentą į fiskalinį įrenginį arba paslaugą.
1. FIF vykdo fiskalinę jungtį, kuri apdoroja fiskalinį dokumentą ir pateikia jį fiskalinei įrenginiui arba tarnybai.
1. FIF pateikia fiskalinį atsakymą (t. y. fiskalinio įrenginio arba paslaugos atsakymą) į EKA.
1. EKA analizuoja fiskalinį atsakymą, kad nustatytų, ar iždo registracija sėkminga. Jei reikia, EKA reikalauja, kad FIF apdorotų visas įvyko klaidas. 
1. EKA reikalauja, kad FIF procesas būtų išsaugokite fiskalinį atsakymą.
1. Finansinio dokumento teikėjas apdoroja fiskalinį atsakymą. Kaip šio apdorojimo dalį fiskalinio dokumento teikėjas išanalizuotų atsakymą ir iš jo išskleistus išplėstinius duomenis.
1. FIF įrašo atsakymą ir išplėstinius duomenis į kanalo duomenų bazę.
1. Jei reikia, EKA išspausdina kvitą įprastu kvitų spausdintuvu, prijungtu prie "Hardware" stoties. Kvite gali būti būtini finansinio atsakymo duomenys.
 
Toliau pateikti pavyzdžiai rodo įprastų finansinių įrenginių arba tarnybų finansinės registracijos vykdymo eigas.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Finansinis registravimas atliekamas naudojant įrenginį, prijungtą prie aparatūros stoties

Ši konfigūracija naudojama, kai fizinis fiskalinis įrenginys, pvz., fiskalinis spausdintuvas, prijungtas prie aparatūros stoties. Tai taikoma ir tada, kai ryšys su finansiniu įrenginiu arba paslauga atliekamas naudojant programinę įrangą, įdiegtą "Hardware" stotyje. Tokiu atveju fiskalinio dokumento teikėjas yra "Hardware CRT" stotis, o fiskalinė jungtis – aparatūros stotyje.

![Finansinis registravimas atliktas naudojant įrenginį, prijungtą prie aparatūros stoties.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Iždo registracija atliekama per išorinę tarnybą

Ši konfigūracija naudojama, kai finansinis registravimas atliekamas per išorinę tarnybą, pvz., mokesčių inspekcijos naudojamą žiniatinklio tarnybą. Šiuo atveju skirtuke yra ir fiskalinio dokumento teikėjas, ir fiskalinė jungtis CRT.

![Iždo registracija atlikta per išorinę tarnybą.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Finansinis registravimas atliekamas viduje CRT

Ši konfigūracija naudojama, kai registruojant finansinius duomenis nereikia jokio išorinio finansinio įrenginio arba paslaugos. Pavyzdžiui, jis naudojamas, kai finansinis registravimas atliekamas skaitmeniniu būdu pasirašant pardavimo operacijas. Šiuo atveju skirtuke yra ir fiskalinio dokumento teikėjas, ir fiskalinė jungtis CRT.

![Finansinis registravimas atliekamas viduje CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Finansinis registravimas atliekamas naudojant įrenginį arba paslaugą vietiniame tinkle

Ši konfigūracija naudojama, kai fizinis finansinis įrenginys arba finansinis aptarnavimas yra vietiniame parduotuvės tinkle ir suteikia HTTPS programos programavimo sąsają (API). Šiuo atveju fiskalinio dokumento teikėjas yra CRT EKA, o fiskalinė jungtis – EKA.

![Finansinis registravimas atliekamas naudojant įrenginį arba paslaugą vietiniame tinkle.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Klaidos taisymas

Fiskalinės integracijos sistema teikia toliau nurodytas parinktis, skirtas spręsti problemas, kylančias fiskalinės registracijos metu.

- **Kartoti** – operatoriai gali naudoti šią parinktį, kai problemą galima išspręsti greitai ir fiskalinę registraciją galima vykdyti iš naujo. Pvz., šią parinktį galima naudoti, kai finansinis įrenginys yra neprijungtas, fiskaliniame spausdintuve nėra popieriaus arba yra fiskaliniame spausdintuve kilo popieriaus strigtis.
- **Atšaukti** – ši parinktis operatoriams suteikia galimybę atidėti dabartinės operacijos arba įvykio fiskalinę registraciją, jei ji nepavyksta. Po registracija atidedama, operatorius gali tęsti darbą EKA ir baigti bet kokią operaciją, kuriai fiskalinė registracija nėra būtina. Kai EKA įvyksta bet koks įvykis, kuriam būtina fiskalinė registracija (pvz., atidaroma nauja operacija), automatiškai parodomas klaidų tvarkymo dialogo langas, kuris praneša operatoriui, kad ankstesnė operacija nebuvo tinkamai užregistruota, ir pateikia klaidų tvarkymo parinktis.
- **Praleisti** – operatoriai gali naudoti šią parinktį, kai tam tikromis aplinkybėmis galima praleisti fiskalinę registraciją ir reguliarias operacijas galima tęsti EKA. Pvz., šią parinktį galima naudoti, kai pardavimo operaciją, kurios fiskalinė registracija nepavyko, galima registruoti specialiame popieriniame žurnale.
- **Pažymėti kaip užregistruotą** – operatoriai gali naudoti šią parinktį, kai operacija iš tikrųjų buvo užregistruota finansiniame įrenginyje (pavyzdžiui, išspausdintas finansinis kvitas), bet kilo problema, kai finansinis atsakymas buvo įrašomas kanalo duomenų bazėje.
- **Atidėti** – operatoriai gali naudoti šią pasirinktį, kai operacija nebuvo užregistruota dėl to, kad registracijos paslauga nebuvo galima. 

> [!NOTE]
> Prieš **pradedant** naudoti, **pasirinktis** Praleisti, **Pažymėti** kaip registruotas ir Atidėti turi būti suaktyvintos finansinio registravimo procese. Be to, operatoriams turi būti suteiktos atitinkamos teisės.

Pasirinktys **Praleisti**, **·** **Pažymėti** kaip užregistruotos ir Atidėti įgalina informacijos kodus, kad būtų galima fiksuoti konkrečią informaciją apie triktį, pvz., trikties priežastį, arba pagrindimą praleisti fiskalinę registraciją arba pažymėti operaciją kaip užregistruotą. Daugiau informacijos apie tai, kaip nustatyti klaidų tvarlymo parametrus, žr. [Klaidų tvarkymo parametrai](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Nebūtina fiskalinė registracija

Fiskalinė registracija gali būti privaloma tik atliekant tam tikras operacijas. Pavyzdžiui, įprastų pardavimų ir grąžinimų atveju fiskalinė registracija gali būti privaloma, bet su kliento mokama suma susijusių operacijų fiskalinė registracija nebūtina. Neatlikus pardavimo fiskalinės registracijos, kiti pardavimai blokuojami, o neatlikus kliento mokamos sumos fiskalinės registracijos kiti pardavimai neblokuojami. Tam, kad galėtumėte atskirti privalomas ir neprivalomas operacijas, rekomenduojame jas atliekant naudotis skirtingų dokumentų teikėjų paslaugomis ir nustatyti atskirus tų teikėjų fiskalinės registracijos proceso etapus. Parametras **Tęsti įvykus klaidai** turi būti įgalintas atliekant bet kokį su nebūtina fiskaline registracija susijusį veiksmą. Daugiau informacijos apie tai, kaip nustatyti klaidų tvarlymo parametrus, žr. [Klaidų tvarkymo parametrai](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Rankiniu būdu iš naujo vykdyti iždo registravimą

Jei įvykus klaidai (pvz., klaidų tvarkymo dialogo lange operatoriui paspaudus **Atšaukti**) operacijos arba įvykio fiskalinė registracija atidėta, suaktyvinę atitinkamą operaciją galite patys iš naujo paleisti fiskalinę registraciją. Daugiau informacijos rasite [Rankinio atidėtos fiskalinės registracijos vykdymo įgalinimas](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Atidėti pasirinktį

Naudodami **pasirinktį** Atidėti galite tęsti finansinio registravimo procesą, jei dabartinis žingsnis nepavyksta. Jį galima naudoti, kai yra finansinio registravimo atsarginės kopijos pasirinktis.

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
> Sveikatos tikrinimas vykdomas tik tada, jei dabartinei operacijai reikalingas finansinis registravimas ir **jei** išjungtas dabartinio finansinio registravimo proceso veiksmo parametras Tęsti esant klaidai. Daugiau informacijos rasite [Klaidų tvarkymo parametrų nustatymas](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Finansinio atsakymo saugojimas finansinėje operacijoje

Kai operacijos arba įvykio fiskalinė registracija sėkminga, finansinė operacija sukuriama kanalo duomenų bazėje ir susiejama su pradine operacija arba įvykiu. Be to, pasirenkama nepavykusios finansinės registracijos parinktis **Praleisti** arba **Pažymėti kaip užregistruotą**, ši informacija yra saugoma finansinėje operacijoje. Finansinėje operacijoje saugomas finansinis atsakymas iš finansinio įrenginio ar tarnybos. Jei fiskalinės registracijos procesą sudaro keli etapai, finansinė operacija sukuriamas atliekant kiekvieną proceso veiksmą, po kurio registracija pavyko arba nepavyko.

*P užduotis* perkelia finansines operacijas į Būstinę kartu su operacijomis. Puslapio **Parduotuvės operacijos** „FastTab“ **Finansinės operacijos** galite peržiūrėti finansines operacijas, susietas su operacijomis.

Finansinėje operacijoje saugoma toliau nurodyta informacija.

- Fiskalinės registracijos proceso informacija (procesas, jungčių grupė, jungtis ir t. t.). Jos lauke **Registro numeris** taip pat saugomas finansinio įrenginio serijos numeris, jei ši informacija įtraukta į finansinį atsakymą.
- Iždo registracija: atlikta sėkmingos registracijos būsena. Praleista, **jei** operatorius **pasirinkote** nepavykusios registracijos parinktį Praleisti, Pažymėta kaip užregistruota, **jei** operatorius **pasirinkote** parinktį Pažymėti kaip užregistruotą arba Atidėta, **jei** operatorius **pasirinkote** pasirinktį Atidėti. **·**
- Informacijos kodo operacijos, susijusios su pasirinkta finansine operacija. Norėdami peržiūrėti informacijos kodo operacijas, **finansinių** operacijų "FastTab" pasirinkite fiskalinę operaciją, **kurios** būsena yra Praleista, **·** **Pažymėta** kaip užregistruota arba Atidėta, tada pasirinkite Informacijos **kodo operacijos**.

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
