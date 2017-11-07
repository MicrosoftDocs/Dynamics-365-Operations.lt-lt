---
title: "Sandėlio mobiliojo įrenginio rodymo parametrai"
description: "Šiame straipsnyje aprašoma, kaip nustatyti mobiliojo įrenginio ekrano išvaizdą ir susieti klaviatūros sparčiuosius klavišus su valdikliais, pvz., mygtukais."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 799cd4a940813e39f8be6b4c127b9efabc88e909
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-mobile-device-display-settings"></a>Sandėlio mobiliojo įrenginio rodymo parametrai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašoma, kaip nustatyti mobiliojo įrenginio ekrano išvaizdą ir susieti klaviatūros sparčiuosius klavišus su valdikliais, pvz., mygtukais. 

Šis straipsnis taikomas sandėlio valdymo „patobulinto sandėliavimo“ funkcijoms. Mobiliuosius įrenginius galima naudoti daugeliui sandėlio darbuotojų užduočių atlikti.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Stiliaus nurodymas ir sparčiųjų klavišų susiejimas
Atlikdami mobiliojo įrenginio konfigūravimą galite nurodyti skirtingus mobiliųjų įrenginių maketus. Norėdami tai atlikti, turite žinoti pakopinių stilių sąrašo (CSS) failo ir aktyviojo serverio puslapio plėtinio (ASPX) failo pavadinimus. Numatytieji failai yra įdiegiami atliekant sandėlio mobiliųjų įrenginių portalo diegimą. Jei nežinote failų vardų, kreipkitės į sistemos administratorių. Puslapyje **Mobiliojo įrenginio ekrano parametrai** galite nurodyti naują stilių.

-    Lauke **CSS failas** įveskite CSS failo pavadinimą. Įtraukite .css failo vardo plėtinį.
-   Lauke **Mobiliojo įrenginio ekrano parametrų rodinys** nurodykite ASPX failą. **Neįtraukite** .aspx failo vardo plėtinio.

CSS ir ASPX failai turi būti konkrečiame kataloge, kad informacinių interneto paslaugų (IIS) programa galėtų juos įkelti. Tai gali būti naudinga nustatyti skirtingus CSS failus, jei mobiliojo įrenginio funkciją naudojate skirtingose naršyklėse arba skirtingų tipų aparatūrose, kuriose būtina skirtingų maketų kontrolė. Naudojant įvairius CSS failus galima valdyti parastus parametrus, pvz., fono spalvą, teksto šriftą ir šrifto dydį bei mygtukų plotį ir elgseną. ASPX failas naudojamas mobiliajai svetainei serverio ASP.NET programoje rodyti. Failas kontroliuoja visos HTML struktūros išdėstymą. Šią funkciją pritaikyti naudinga tik tada, jei turite rimtų struktūrinių problemų su HTML ir „JavaScript“ bei turite pakeisti šį kodą konkretiems įrenginiams. Norėdami mobiliojo įrenginio puslapyje susieti HTML valdiklius su klaviatūros sparčiaisiais klavišais, puslapio **Mobiliojo įrenginio ekrano parametrai** lauke **Klaviatūros spartieji klavišai** priskirkite klavišams skaitinius kodus. Galite naudoti mobiliojo įrenginio meniu **Peržiūrėti sparčiųjų klaviatūros klavišų kodus**, norėdami rasti skaitinių simbolių kodus. Atkreipkite dėmesį, kad susiejimai gali skirtis, atsižvelgiant į naudojamą aparatūrą. Norėdami susieti naudokite toliau nurodytą sintaksę:

&lt;valdiklio pavadinimas&gt;(&lt;klavišo pavadinimas&gt;)=&lt;klavišo kodas&gt;;

Toliau pateikiamas sintaksės dalių paaiškinimas.

-   **&lt;valdiklio pavadinimas&gt;** – valdiklio (pvz., mygtuko), kuris rodomas HTML, pavadinimas.
-   **(&lt;klavišo pavadinimas&gt;)** – klaviatūros klavišo, kuriam skirtą spartųjį klavišą kuriate, pavadinimas.
-   **&lt;klavišo kodas&gt;** – skaitinis klavišo, kurį norite naudoti kaip spartųjį klavišą, kodas.

Toliau pateikiamas pavyzdys.

Atšaukti (ESC) = 27; visas (F2) = 113

Visuose puslapiuose, kuriuose yra mygtukas **Atšaukti**, šio mygtuko tekstas bus:

**(ESC) Atšaukti**

Klaviatūroje paspaudus klavišą ESC bus suaktyvintas mygtukas **Atšaukti**. Norėdami stiliaus ir klaviatūros klavišų parametrus taikyti konkrečiam įrenginiui, turite sukurti susiejimą lauke **Kriterijai**. Norėdami kurti susiejimą, turite naudoti .NET paprastąją išraišką ir ta išraiška turi būti sudaryta iš trijų dalių, atskirtų vertikaliu brūkšniu (|), kaip parodyta čia:

Request.UserHostAddress=&lt;vartotojo pagrindinio kompiuterio adresas&gt;|HostName=&lt;vartotojo pagrindinio kompiuterio pavadinimas&gt;|Request.UserAgent=&lt;vartotojo agentas&gt;

Toliau pateikiamas išraiškos dalių paaiškinimas.

-   **&lt;vartotojo pagrindinio kompiuterio adresas&gt;** – .NET paprastoji išraiška, kuri sutampa su prašytojo IP adresu.
-   **&lt;vartotojo pagrindinio kompiuterio pavadinimas&gt;** – .NET paprastoji išraiška, kuri sutampa su prašytojo tinklo pavadinimu.
-   **&lt;vartotojo agentas&gt;** – .NET paprastoji išraiška, kuri sutampa su prašytojo naudojamos naršyklės identifikatoriumi.

Šiame pavyzdyje įgalinama galimybė naudoti „Internet Explorer 8“.

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

Galite naudoti mobiliojo įrenginio meniu **Peržiūrėti ekrano parametrus serverio konfigūracijoje**, norėdami rasti informacijos apie sąranką.

## <a name="define-text-colors-for-messages"></a>Pranešimų teksto spalvos nustatymas
Galite naudoti puslapį **Mobiliojo įrenginio teksto spalvos**, norėdami valdyti įvairias spalvas, naudojamas sistemos sugeneruotuose pranešimuose, pvz., klaidų pranešimuose. Pvz., teksto spalva gali nurodyti pranešimo paskirtį arba svarbą. Toliau pateikiami rodomi pranešimų tipai.

| Pranešimo tipas | Prekės/Paslaugos pavadinimas                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Numatytoji      | Numatytuose pranešimuose naudojami numatytieji visų pranešimų spalvų parametrai, kaip nurodyta sandėlio mobiliųjų įrenginių portalo CSS faile.                                                   |
| Klaida        | Klaidų pranešimai nurodo problemą, kurią vartotojas turi išspręsti, jei jis arba ji nori tęsti.                                                                                             |
| Sėkmingai      | Pranešimai apie pavykusią operaciją patvirtina, kad veiksmas atliktas sėkmingai.                                                                                                                                |
| Įspėjimas      | Įspėjamieji pranešimai darbuotojui praneša, kad kilo problema arba kad problema gali kilti, jei darbuotojas tęs darbą. Tačiau, norėdamas tęsti, darbuotojas neturi problemos išspręsti. |

Norėdami pasirinkti spalvą, puslapyje **Pasirinkti spalvą** spustelėkite paletę arba įveskite spalvos kodą šešioliktaine reikšme.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Nurodykite datos formatą, kuris bus naudojamas mobiliuosiuose įrenginiuose
Galite išplėsti kiekvienos įdiegties priimtinų datos formatų sąrašą. Pavyzdžiui, ši galimybė gali būti naudinga, jei norite pateikti formatą, kuris leidžia darbuotojui paprasčiau įvesti datas mobiliajame įrenginyje. Numatytasis formatas priklauso nuo vartotojo numatytosios kalbos, kuri nurodyta puslapio **Vartotojo parinktys** lauke **Kalba**. (The same page is also used to associate an employee with a specific warehouse work user.) **Pastaba:** sandėlio mobiliųjų įrenginių portale nenaudojamas lauko **Datos, laiko ir numerių formatas**, esančio puslapyje **Kalbos ir regiono nuostatos**, parametras. Norėdami pakeisti datos formatą, turite būti susipažinę su „Microsoft .NET Framework“ paprastosiomis išraiškomis. Daugiau informacijos žr. [ „.NET Framework“ paprastosios išraiškos](http://go.microsoft.com/fwlink/?LinkId=391260). Norėdami nurodyti datos formatus, redaguokite failą Dates.ini, esantį sandėlio mobiliųjų įrenginių portale adresu Content\\Settings\\Dates.ini. Šis failas naudoja .NET paprastąsias išraiškas datos formatui nurodyti. Paprastojoje išraiškoje turi būti antrinių išraiškų, kurios kuria įvardytas dienos, mėnesio ir metų (DDMMYY) grupes, kaip parodyta toliau pateiktame pavyzdyje.

^(?&lt;diena&gt;\\d{2})(?&lt;mėnuo&gt;\\d{2})(?&lt;metai&gt;\\d{2})$

Kiekvienoje antrinėje išraiškoje turi būti vienas arba du dienos ir mėnesio skaitmenys ir nuo vieno iki keturių metų skaitmenų. Pavyzdžiui, toliau pateikta antrinė išraiška apibrėžia įvardytą metų grupę ir joje reikia nurodyti nuo dviejų iki keturių skaitmenų.

(?&lt;metai&gt;\\d{2,4})

Tame pačiame faile galite nurodyti daugiau nei vieną išraišką. Kiekviena išraiška turi būti atskiroje eilutėje. Pirmoji kriterijus atitinkanti išraiška yra naudojama datai išanalizuoti.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Mobiliųjų įrenginių konfigūravimas darbui sandėlyje](configure-mobile-devices-warehouse.md)




