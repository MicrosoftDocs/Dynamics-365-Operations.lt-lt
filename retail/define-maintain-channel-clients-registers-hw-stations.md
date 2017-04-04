---
title: "Nustatyti ir išlaikyti kanalo klientams, registrus ir aparatūros stotys"
description: "Šis „wiki“ nurodo, kaip išorinius įrenginius prijungti prie „Retail POS“."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dee5745670ad86000795f2913f99f49c0f123a00
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Nustatyti ir išlaikyti kanalo klientams, registrus ir aparatūros stotys

Šis „wiki“ nurodo, kaip išorinius įrenginius prijungti prie „Retail POS“.

**Pastaba.** Norėdami konkrečių diegimo instrukcijų, žr. dalis [„Retail hardware station‟ konfigūravimas ir diegimas](retail-hardware-station-configuration-installation.md) ir [„Retail Modern POS‟ savitarnos savitarnos atsisiuntimas / diegimas ir „Modern POS“ bei „Cloud POS“ įrenginio aktyvinimas](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Pagrindiniai komponentai
Galima naudoti kelis komponentus, norint nustatyti ryšius tarp parduotuvės, elektroninio kasos aparato (EKA) registrų arba kanalų parduotuvėje ir mažmeninės prekybos išorinių įrenginių, kuriuos tie registrai arba kanalai naudoja operacijoms apdoroti. Šiame skyriuje aprašomi visi komponentai ir paaiškinama, kaip juos naudoti mažmeninės prekybos parduotuvėje.

### <a name="pos-registers"></a>EKA registrai

Navigacija: Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**registrų**. POS registras yra subjektas, kuris yra naudojamas nustatyti konkrečiu atveju į gamintojų organizacijų ypatybes. Šios savybės apima aparatūros profilis arba sąrankos mažmeninės prekybos periferiniai įrenginiai, kuris bus naudojamas registrą, kuris registre yra susietas su parduotuvės ir regėjimo patirtį vartotojo, kuris įeina į, registruotis.

### <a name="devices"></a>Įrenginiai

Navigacija: Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**įrenginiai**. Įrenginys yra objektas, nurodantis su EKA registru susieto įrenginio fizinį egzempliorių. Sukūrus įrenginį, jis susiejamas su EKA registru. Įrenginio objektas seka informaciją apie POS registro suaktyvinimo laiką, naudojamo kliento tipą ir programų paketą, kuris buvo įdiegtas konkrečiame įrenginyje. Įrenginiai gali būti dviejų tipų: **Retail Modern POS** (MPOS) arba **Retail Cloud POS** („Cloud POS“).

#### <a name="mpos"></a>MPOS

MPOS yra EKA kliento programa, įdiegta„"Windows 8.1“ arba naujesnės versijos kompiuterio operacinėje sistemoje. Jei tipo **Retail modern POS** programa susiejama su įrenginiu, atsisiuntimo paketą galima nurodyti konkrečiam įrenginiui. Atsisiuntimo paketą galima tinkinti, siekiant įtraukti skirtingų diegimo paketo versijų. Galimybė diegti skirtingus paketus suteikia lankstumo tais atvejais, kai skirtingiems EKA registrams gali reikėti skirtingų integravimų. MPOS yra naudojamas kartu su įtaisyta aparatūros stotimi.

#### <a name="cloud-pos"></a>Cloud POS

POS debesiui naršyklės pagrindu POS. Nes tai veikia naršyklėje, debesies POS nereikalauja Windows 8.1 arba naujesnė kompiuterio operacinė sistema. Jei tipo **Retail Cloud POS** programa susiejama su konkrečiu įrenginiu tarnybiniame biure, tą įrenginį galima naudoti per naršyklę – atsisiųsti ar įdiegti paketo nereikia. „Cloud POS“ reikalinga aparatūros stotis, jei norima naudoti aparatūrą, kuri nėra klavišinis kredito kortelių skaitytuvas, pagrįstas brūkšninių kodų nuskaitymu.

### <a name="hardware-profile"></a>Aparatūros šablonas

Navigacija: Spustelėkite **prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros profiliai**. Aparatūros šablonas nurodo aparatūrą, kuri yra prijungta prie EKA registro arba aparatūros stoties. Aparatūros šablonas taip pat naudojamas, siekiant nurodyti mokėjimo procesorius parametrus, kurie turėtų būti naudojami palaikant ryšį su mokėjimo programinės įrangos kūrimo rinkiniu (SDK). (Mokėjimo SDK įdiegiamas kaip aparatūros stoties dalis.)

### <a name="hardware-station"></a>Aparatūros stotis

Navigacija: Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalai**&gt;**mažmeninės prekybos parduotuvėse**&gt;**visi mažmeninės prekybos parduotuvėse**. Pasirinkite parduotuvę, tada spustelėkite „FastTab“ **Aparatūros stotys**. Aparatūros stotis yra verslo logikos pavyzdys, išplečia EKA išorinių įrenginių valdymo galimybes. Aparatūros stotis yra automatiškai diegiama kartu su MPOS. Arta aparatūros stotį taip pat galima įdiegti kaip atskirą komponentą ir tada per žiniatinklio tarnybą ją pasiekti naudojant MPOS arba „Cloud POS“. Aparatūros stotį reikia apibrėžti kanalo lygiu.

### <a name="hardware-station-profile"></a>Aparatūros stoties profilis

Navigacija: Spustelėkite **prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros stoties profiliai**. Kadangi pati aparatūros stotis yra nurodyta kanalo lygiu ir apima egzemplioriui būdingą informaciją, pvz., aparatūros stoties URL, aparatūros stoties šablonas apima informaciją, kuri gali būti statinė arba bendrai naudojama keliose aparatūros stotyse. Statinė informacija apima naudotiną prievadą, aparatūros stoties paketą ir aparatūros šabloną. Statinė informacija taip pat apima naudojamos aparatūros stoties aprašą, pvz., **Kasa **arba **Grąžinimai**, priklausomai nuo aparatūros, reikalingos kiekvienai konkrečiai aparatūros stočiai.

## <a name="scenarios"></a>Scenarijai
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS su prijungtais išoriniais įrenginiais

[![Tradiciniai, fiksuoto taško pardavimo](./media/traditional-300x279.png)](./media/traditional.png) prie POS periferinę įrangą POS tokiu, tradicinių, pastovaus MPOS, pirmiausia eikite į registrą, pati ir aparatūros šabloną priskirti. Galite rasti ne POS registrų **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**registrų**. Priskyrę aparatūros šabloną, sinchronizuokite keitimus su kanalo duomenų baze, naudodami paskirstymo grafiką „Registrai“. Jūs galite rasti ir paskirstymo schemas **mažmeninės prekybos ir komercijos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**. Tada kanale nustatykite „vietos“ aparatūros stotį. Spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalai**&gt;**mažmeninės prekybos parduotuvėse**&gt;**visi mažmeninės prekybos parduotuvėse**, ir pasirinkite saugoti. Tada „FastTab“ **Aparatūros stotys** spustelėkite **Įtraukti**, kad įtrauktumėte aparatūros stotį. Įveskite aprašą, įveskite **localhost** kaip pagrindinio kompiuterio vardą, o tada sinchronizuokite keitimus su kanalu, naudodami paskirstymo grafiką „Kanalo konfigūravimas“. Jūs galite rasti ir paskirstymo schemas **mažmeninės prekybos ir komercijos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo grafikas**. Galiausiai MPOS naudokite operaciją **Pasirinkti aparatūros stotį**, kad pasirinktumėte **localhost** aparatūros stotį. Nustatykite aparatūros stotį parinktį **Aktyvi**. Šiame scenarijuje naudojamas aparatūros šablonas turėtų būti gautas iš pačio POS registro. Šiame scenarijuje aparatūros stoties šablonas nereikalingas. **Pastaba.** Atlikus kai kuriuos aparatūros šablono keitimams, pavyzdžiui kasos stalčių keitimus, ir juos sinchronizavus su kanalu, reikia atidaryti naują pamainą. **Pastaba.** „Cloud POS“ ryšiui su mažmeninės prekybos išoriniais įrenginiais palaikyti turi būti naudojama atskira aparatūros stotis.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS arba „Cloud POS“ su atskira aparatūros stotimi

\[antraštės id = "priedas\_340041" suderinti = "alignleft" Plotis = "300"\][![bendras periferiniai](./media/shared-300x254.png)](./media/shared.png) bendras periferiniai\[/antraštė\] tokiu atveju atskiras aparatūros stoties bendrai naudoja MPOS ir debesies POS klientams. Šiame scenarijuje reikia sukurti aparatūros stoties šabloną ir nurodyti aparatūros stoties naudojamus atsisiuntimo paketą, prievadą ir aparatūros šabloną. Jūs galite rasti aparatūros stoties profilyje **mažmeninės prekybos ir komercijos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**&gt;**aparatūros stoties profiliai**. Sukūrę aparatūros stoties profilis, pereikite prie konkrečios mažmeninės prekybos kanalo (**mažmeninės prekybos ir prekybos**&gt;**kanalai**&gt;**mažmeninės prekybos parduotuvėse**&gt;**visi mažmeninės prekybos parduotuvėse**), ir pridėti naują aparatūros stotis. Susiekite šią naują aparatūros stotį su anksčiau sukurtu aparatūros stoties šablonu. Tada pateikite aprašymą, kuris kasininkui padės identifikuoti aparatūros stotį. – Į **pagrindinio kompiuterio pavadinimas** pagrindinio kompiuterio mašina URL įveskite šiuo formatu: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Pakeisti **&lt;MachineName:Port&gt;** su aparatūros stoties ir uosto, aparatūros stoties profilyje nurodytos faktinės mašinos pavadinimą.) Atskiras įrangos stotis, jūs taip pat turėtų nurodyti elektroninių lėšų pervedimą (EFT) terminalo ID. Ši reikšmė identifikuoja EFT terminalą, kuris yra prijungtas prie aparatūros stoties, kai mokėjimo jungtis užmezga ryšį su mokėjimo paslaugų teikėju. Tada naršydami faktinę aparatūros stoties mašiną pasirinkite kanalą ir pasirinkite aparatūros stotį. Spustelėkite **Atsisiųsti** ir įdiekite aparatūros stotį. Tada MPOS arba „Cloud POS“ naudokite operaciją **Pasirinkti aparatūros stotį**, kad pasirinktumėte anksčiau įdiegtą aparatūros stotį. Pasirinkite **Susieti**, kad sukurtumėte saugų ryšį tarp EKA ir aparatūros stoties. Šį veiksmą reikia atlikti kuriant kiekvieno POS ir aparatūros stoties derinio ryšį. Susiejus aparatūros stotį, ta pačia operacija naudojama aparatūros stotis suaktyvinama. Pagal šį scenarijų, aparatūros profilis turėtų būti priskirta aparatūros stoties profilis, o ne pati registrą. Jei dėl tam tikrų priežasčių aparatūra stotis neturi techninės įrangos profilį, tiesiogiai priskirtas, tada naudojama techninės įrangos profilį, priskirtas registras

## <a name="client-maintenance"></a>Kliento priežiūra
### <a name="registers"></a>Registrai

POS registrai visų pirma yra valdomi naudojant pačius registrus, taip pat naudojant registrams priskirtus šablonus. Atskiram registrui būdingi atributai yra valdomi registro lygiu. Šie atributai apima parduotuvė, kurioje registras naudojamas, registro numerį, aprašą ir EFT terminalo ID, kuris yra būdingas pačiam registrui.

### <a name="pos-profiles"></a>POS šablonai

Galite rasti ne POS profiliai **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profiliai**. Naudinga valdyti daugelį registro aspektų naudojant šablonus, nes šablonus galima bendrai naudoti daugelyje registrų. Šablonus galima susieti su vienu atskiru registru arba, jei šablonas yra veiksmingas visoje parduotuvėje, su mažmeninės prekybos parduotuve. Tolesniuose skyriuose aprašomi POS šablonai ir kaip jie yra naudojami.

#### <a name="offline-profile"></a>Šablonas ne tinkle

Ne tinkle esantis šablonas nustatomas parduotuvės lygiu. Jis naudojamas siekiant nurodyti operacijų, kurios atliekamos su EKA registru, kai tas registras nėra prijungtas prie kanalo duomenų bazės, nusiuntimo parametrus.

#### <a name="functionality-profile"></a>Funkcijų šablonas

Funkcijų šablonas nustatomas parduotuvės lygiu. Jis naudojamas nurodyti parduotuvėje esantys parametrai apie funkcijas, kurios gali būti atliekamos EKA. Šias galimybes yra valdoma funkcijų šabloną. Šios galimybės yra išdėstomos „FastTab“.

-   „FastTab“ **Bendra**.
    -   Tarptautinė standartizacijos organizacija (ISO).
    -   Kliento kūrimas autonominiu režimu.
    -   El. laiško kvito šablonas.
    -   Pagrindinio darbuotojų prisijungimo autentifikavimas.
-   „FastTab“ **Funkcijos**.
    -   Prisijungimo ir išplėstinio prisijungimo valdymas.
    -   Finansiniai ir su valiuta susiję EKA aspektai, pavyzdžiui, galimybė įvesti kainas ir nustatyti, ar reikia nurodyti smulkios valiutos dešimtaines dalis.
    -   Laiko registravimo suaktyvinimas naudojant EKA.
    -   Valdymas, kaip produktai ir mokėjimai rodomi EKA ir kvituose.
    -   Dienos pabaigos valdymas.
    -   Kanalo duomenų bazės operacijų saugojimo parametrai.
    -   Valdymas, kaip EKA yra ieškomi ir kuriami klientai.
    -   Valdymas, kaip skaičiuojamos nuolaidos.
-   „FastTab“ **Suma**.
    -   Didžiausios ir mažiausios galimos kainos.
    -   Nuolaidų taikymas ir skaičiavimas.
-   „FastTab“ **Info codes**.
    -   Visais aspektais kaip informacijos kodai valdomi EKA. Daugiau informacijos rasite [informacijos kodai](info-codes-retail.md).
-   „FastTab“ **Kvitų numeravimas**.
    -   Galimybė nurodyti kvito numeravimo šablonus; tai gali apimti parduotuvės numerio, terminalo numerio, konstantų segmentus bei valdymą, ar pardavimas, grąžinimai, pardavimo užsakymai ir pasiūlymai yra spausdinami atskiromis sekomis, ar ta pačia seka.

#### <a name="receipt-profiles"></a>Kvitų profiliai

Kvitų šablonai yra priskiriami aparatūros šablono spausdintuvams. Jie naudojami siekiant nurodyti konkrečiu spausdintuvu spausdinamų kvitų tipus. Šablonai apima kvito formatų parametrus ir parametrus, kurie nustato, ar kvitas yra visada spausdinamas, ar kasininkas yra paraginamas nurodyti, ar kvitą reikia spausdinti. Skirtinguose spausdintuvuose taip pat gali būti naudojami skirtingi kvitų šablonai. Pvz., 1 spausdintuvas yra standartinis terminis kvitų spausdintuvas ir todėl spausdina mažesnio formato kvitus. Tačiau 2 spausdintuvas yra viso dydžio kvitų spausdintuvas, kuriuo spausdinami tik tie klientų kvitai, kuriuose reikia daugiau vietos informacijai pateikti.

#### <a name="hardware-profiles"></a>Aparatūros šablonai

Aparatūros šablonai anksčiau šiame straipsnyje yra apibūdinti kaip kliento sąrankos komponentai. Aparatūros šablonai yra tiesiogiai priskiriami EKA registrui arba aparatūros stoties šablonui. Jie naudojami siekiant nurodyti įrenginių, kuriuos naudoja konkretus EKA registras arba aparatūros stotis, tipus. Aparatūros šablonai taip pat naudojami siekiant nurodyti EFT parametrus, naudojamus ryšiui su mokėjimo SDK palaikyti.

#### <a name="visual-profiles"></a>Vaizdo šablonai

Vaizdo šablonai priskiriami registro lygiu. Jie naudojami konkretaus registro temai nurodyti. Šablonai apima parametrus, skirtus naudojamos programos tipui (MPOS arba „Cloud POS“), akcento spalvai ir temai, šrifto schemai, registravimosi rodinio fonui ir POS fonui.

### <a name="custom-fields"></a>Pasirinktiniai laukai

Galite sukurti pasirinktinius laukus, pridėti laukų, kurie nėra teikiama go out of the box. Daugiau informacijos apie tai, kaip naudoti pasirinktinius laukus, peržiūrėkite, [darbas su laukų dienoraštyje](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Kalbos tekstas

Galite perrašyti numatytuosius EKA parametrus, naudodami kalbos teksto įrašus. Norėdami perrašyti EKA eilutę, įtraukite naują kalbos teksto eilutę. Tada nurodykite ID, numatytąją eilutę, kuri turėtų būti perrašyta, ir tekstą, kuris EKA turėtų būti rodomas vietoj numatytosios eilutės.

### <a name="hardware-station-profiles"></a>Aparatūros stoties profiliai

Aparatūros stočių šablonai yra paaiškinti šiame straipsnyje anksčiau. Jie naudojami siekiant aparatūros stotims priskirti egzemplioriams nebūdingą informaciją.

### <a name="channel-reports-configuration"></a>Kanalo ataskaitų konfigūravimas

Mažmeninės prekybos kanale teikiamas ataskaitas galima nustatyti puslapyje **Mažmeninės prekybos kanalo ataskaitų konfigūravimas**. Naujas ataskaitas galite kurti pateikdami ataskaitos XML aprašą ir ataskaitą priskirdami konkrečiai EKA teisių grupei.

### <a name="devices"></a>Įrenginiai

Įrenginiai yra paaiškinti šiame straipsnyje anksčiau. Jie naudojami konkretaus EKA registro aktyvinimui valdyti. Įrenginiai taip pat naudojami siekiant nurodyti programą, skirtą konkrečiam registrui ir diegimo paketui, naudojamam MPOS klientui diegti. Toliau pateikiamos įrenginio aktyvinimo būsenos.

-   **Laukiama** – įrenginys paruoštas aktyvinti.
-   **Aktyvinta** – įrenginys suaktyvintas.
-   **Išaktyvinta** – įrenginys išaktyvintas tarnybiniame biure arba naudojant EKA.
-   **Išjungta** – įrenginys išjungtas.

Papildoma su aktyvinimu susijusi informacija apima darbuotoją, kuris pakeitė įrenginio aktyvinimo būseną, aktyvinimo laiko antspaudą ir informaciją apie tai, ar įrenginio konfigūracija buvo patvirtinta.

### <a name="client-data-synchronization"></a>Kliento duomenų sinchronizavimas

Visi EKA kliento keitimai, išskyrus įrenginio aktyvinimo būsenos keitimus, turi būti sinchronizuoti su kanalo duomenų baze, kad įsigaliotų. Norėdami sinchronizuoti keitimus kanalo duomenų bazės, eikite į **mažmeninės prekybos ir komercijos**&gt;**mažmeninės prekybos ji**&gt;**paskirstymo grafiko**, ir paleisti reikiamą paskirstymo grafikas. Atlikę kliento keitimų, turėtumėte vykdyti paskirstymo grafikus „Registrai“ ir „Kanalo konfigūracija“.


