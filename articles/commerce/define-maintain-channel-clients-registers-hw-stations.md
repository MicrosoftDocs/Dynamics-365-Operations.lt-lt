---
title: Išorinių įrenginių prijungimas prie elektroninio kasos aparato (EKA)
description: Ši tema nurodo, kaip išorinius įrenginius prijungti prie „Retail POS“.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1c53c7215d3a5a182f345d5e040274ae06f9b12
ms.sourcegitcommit: 116898def829c0f78bda8a117242aa308793465d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/01/2022
ms.locfileid: "8370956"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Išorinių įrenginių prijungimas prie elektroninio kasos aparato (EKA)

[!include [banner](includes/banner.md)]

Ši tema nurodo, kaip išorinius įrenginius prijungti prie „Retail POS“.

> [!NOTE]
> Konkrečias įdiegimo instrukcijas rasite [„Retail Hardware Station“ konfigūravimas ir diegimas](retail-hardware-station-configuration-installation.md) ir [„Modern POS“ (MPOS) konfigūravimas, diegimas ir aktyvinimas](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Pagrindiniai komponentai

Galima naudoti kelis komponentus, norint nustatyti ryšius tarp parduotuvės, elektroninio kasos aparato (EKA) registrų arba kanalų parduotuvėje ir išorinių įrenginių, kuriuos tie registrai arba kanalai naudoja operacijoms apdoroti. Šiame skyriuje aprašomi visi komponentai ir paaiškinama, kaip juos naudoti parduotuvėje.

### <a name="pos-registers"></a>EKA registrai

Naršymas: spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **Registrai**.

EKA registras yra objektas, kuris naudojamas konkretaus EKA egzemplioriaus charakteristikoms nustatyti. Šios savybės apima aparatūros profilį arba periferinių įrenginių, kurie bus naudojami registre, sąranką, parduotuvę, kuriai priskiriamas registras, ir vartotojo, kuris prisijungia prie to registro, vaizdinį efektą.

### <a name="devices"></a>Įrenginiai

Naršymas: spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **Įrenginiai**.

Įrenginys yra objektas, nurodantis su EKA registru susieto įrenginio fizinį egzempliorių. Sukūrus įrenginį, jis susiejamas su EKA registru. Įrenginio objektas seka informaciją apie POS registro suaktyvinimo laiką, naudojamo kliento tipą ir programų paketą, kuris buvo įdiegtas konkrečiame įrenginyje. Įrenginiai gali būti dviejų tipų: **„Retail modern POS”** (MPOS) arba **„Retail Cloud POS”** („Cloud POS“).

#### <a name="mpos"></a>MPOS

MPOS yra EKA kliento programa, įdiegta„"Windows 8.1“ arba naujesnės versijos kompiuterio operacinėje sistemoje. Jei tipo **„Retail modern POS”** programa susiejama su įrenginiu, atsisiuntimo paketą galima nurodyti konkrečiam įrenginiui. Atsisiuntimo paketą galima tinkinti, siekiant įtraukti skirtingų diegimo paketo versijų. Galimybė diegti skirtingus paketus suteikia lankstumo tais atvejais, kai skirtingiems EKA registrams gali reikėti skirtingų integravimų. MPOS yra naudojamas kartu su įtaisyta aparatūros stotimi.

#### <a name="cloud-pos"></a>„Cloud POS”

„Cloud POS“ yra naršyklėje veikiantis EKA. Kadangi jis veikia naršyklėje, norint naudoti „Cloud POS“ „Windows 8.1“ arba naujesnės versijos kompiuterio operacinė sistema nėra reikalinga. Jei tipo **„Retail Cloud POS“** programa susiejama su konkrečiu įrenginiu būstinėje, tą įrenginį galima naudoti per naršyklę – atsisiųsti ar įdiegti paketo nereikia. „Cloud POS“ reikalinga aparatūros stotis, jei norima naudoti aparatūrą, kuri nėra klavišinis kredito kortelių skaitytuvas, pagrįstas brūkšninių kodų nuskaitymu.

### <a name="hardware-profile"></a>Aparatūros šablonas

Naršymas: eikite į **"Retail" ir "Commerce \> Channel Setup \> POS" nustatymo \> EKA šablonų \> aparatūros šablonus**.

Aparatūros šablonas identifikuoja aparatūrą, kuri prijungta prie EKA kasos aparatu per integruotą ar bendrai naudojamą aparatūros stotį. Aparatūros šablonas taip pat naudojamas, siekiant nurodyti mokėjimo procesorius parametrus, kurie turėtų būti naudojami palaikant ryšį su mokėjimo programinės įrangos kūrimo rinkiniu (SDK). Mokėjimo SDK diegiamas kaip aparatūros stoties dalis.

### <a name="hardware-station"></a>Aparatūros stotis

Naršymas: eikite **į mažmeninės prekybos ir komercijos \>\>\>** kanalus **Parduotuvės visos parduotuvės, pasirinkite parduotuvę, tada pasirinkite "** FastTab" Aparatūros stotis.

Aparatūros stotis yra verslo logikos pavyzdys, išplečia EKA išorinių įrenginių valdymo galimybes. Aparatūros stotis yra automatiškai diegiama kartu su MPOS. Arta aparatūros stotį taip pat galima įdiegti kaip atskirą komponentą ir tada per žiniatinklio tarnybą ją pasiekti naudojant MPOS arba „Cloud POS“. Aparatūros stotį reikia apibrėžti kanalo lygiu.

## <a name="scenarios"></a>Scenarijai

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS su prijungtais išoriniais įrenginiais

[![Tradicinis, fiksuotas elektroninis kasos aparatas.](./media/traditional-300x279.png)](./media/traditional.png)

Norint MPOS prijungti prie EKA išorinio įrenginio pagal tradicinio, fiksuoto POS scenarijų, pirmiausia naršydami pasirinkite patį registrą ir priskirkite jam aparatūros šabloną. POS registrus galite rasti pasirinkę **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **POS sąranka** &gt; **Registrai**. 

Priskyrę aparatūros šabloną, sinchronizuokite keitimus su kanalo duomenų baze, naudodami paskirstymo grafiką **Registrai**. Paskirstymo grafikus galite rasti pasirinkdami **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Pasiskirstymo grafikas**. 

Tada nustatykite paskirtą aparatūros stotį kanale. Eikite į **"Retail" ir "Commerce \> Channels \> Stores \> All**" parduotuves ir pasirinkite parduotuvę. 

Tada aparatūros stoties "**FastTab"** pasirinkite Įtraukti, kad būtų **galima** įtraukti aparatūros stotį. Pasirinkite **Skirta** kaip aparatūros stoties tipas, tada įveskite aprašymą. Laukas **Aparatūros šablonas** gali būti paliktas tuščias, nes šiame scenarijuje naudojamas aparatūros šablonas gaunamas iš paties EKA kasos aparato. Tada sinchronizuokite pakeitimus su kanalu naudodami kanalo konfigūravimo **paskirstymo** grafiką. Paskirstymo grafikus galima rasti "Retail" ir " **Commerce \> Retail" ir "Commerce IT" paskirstymo \> grafike**. 

Galiausiai MPOS naudokite operaciją Pasirinkti aparatūros stotį, kad pasirinktumėte aparatūros stotį, kuri atitinka vertę, **kurią** anksčiau įvedėte aprašymui, **ir nustatykite aparatūros stotį kaip Aktyvi**. 

> [!NOTE]
> - Atlikus kai kuriuos aparatūros šablono keitimams, pavyzdžiui kasos stalčių keitimus, ir juos sinchronizavus su kanalu, reikia atidaryti naują pamainą.
> - „Cloud POS“ ryšiui su išoriniais įrenginiais palaikyti turi būti naudojama atskira aparatūros stotis.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS arba „Cloud POS“ su atskira aparatūros stotimi

[![Bendrinami išoriniai įrenginiai.](./media/shared-300x254.png)](./media/shared.png)

Tokiu atveju atskira aparatūros stotis bendrai naudojama MPOS ir "Cloud POS" klientams. Šiam scenarijui reikia sukurti bendrai naudojamą aparatūros stotį ir nurodyti atsisiuntimo paketą, prievadą ir aparatūros šabloną, kurį naudoja aparatūros stotis. Apibrėžkite **naują aparatūros stotį konkretaus kanalo (Mažmeninės prekybos ir komercijos** kanalai parduotuvės) **pasirinkdami "\>\>\>** **FastTab" Hardware stotis ir pridėdami naują bendrai naudojamo tipo aparatūros stotį.** 

Tada pateikite aprašymą, kuris kasininkui padės identifikuoti aparatūros stotį. Lauke **Pagrindinio kompiuterio vardas** įveskite pagrindinio kompiuterio mašinos URL šiuo formatu: `https://<MachineName:Port>/HardwareStation`. (Keisti **&lt; Kompiuterio pavadinimas: prievadas&gt;** su faktiniu aparatūros stoties įrenginio pavadinimu.) Norėdami nustatyti atskirą aparatūros stotį, taip pat turite nurodyti elektroninio lėšų pervedimo (EFT) terminalo ID. Ši reikšmė identifikuoja EFT terminalą, kuris yra prijungtas prie aparatūros stoties, kai mokėjimo jungtis užmezga ryšį su mokėjimo paslaugų teikėju. 

Tada iš kompiuterio, kuriame bus aparatūros stotis, eikite į "Headquarters" kanalą ir pasirinkite aparatūros stotį. Tada pasirinkite Atsisiųsti **,** kad atsisiųstumėte aparatūros stoties diegimo programą ir įdiegtumėte aparatūros stotį. Norėdami gauti daugiau informacijos apie aparatūros stoties įdiegimą, žr. " [Retail Hardware" stoties konfigūravimas ir diegimas](retail-hardware-station-configuration-installation.md). 

Tada MPOS arba „Cloud POS“ naudokite operaciją **Pasirinkti aparatūros stotį**, kad pasirinktumėte anksčiau įdiegtą aparatūros stotį. Pasirinkite **Susieti**, kad sukurtumėte saugų ryšį tarp EKA ir aparatūros stoties. Šį veiksmą reikia atlikti kuriant kiekvieno POS ir aparatūros stoties derinio ryšį. 

Susiejus aparatūros stotį, ta pačia operacija naudojama aparatūros stotis suaktyvinama. Šiame scenarijuje aparatūros šablonas turi būti priskirtas bendrai naudojamai aparatūros stotisi, o ne pačiam kasos aparatui. Jei dėl kokių nors priežasčių joks aparatūros šablonas nėra tiesiogiai priskirtas aparatūros stotis, bus naudojamas kasos aparatui priskirtas aparatūros šablonas.

## <a name="client-maintenance"></a>Kliento priežiūra

### <a name="registers"></a>Registrai

POS registrai visų pirma yra valdomi naudojant pačius registrus, taip pat naudojant registrams priskirtus šablonus. Atskiram registrui būdingi atributai yra valdomi registro lygiu. Šie atributai apima parduotuvė, kurioje registras naudojamas, registro numerį, aprašą ir EFT terminalo ID, kuris yra būdingas pačiam registrui.

### <a name="pos-profiles"></a>POS šablonai

POS šablonus galite rasti pasirinkę **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **POS sąranka** &gt; **POS šablonai**. Naudinga valdyti daugelį registro aspektų naudojant šablonus, nes šablonus galima bendrai naudoti daugelyje registrų. Šablonus galima susieti su vienu atskiru registru arba, jei šablonas yra veiksmingas visoje parduotuvėje, su parduotuve. Tolesniuose skyriuose aprašomi POS šablonai ir kaip jie yra naudojami.

#### <a name="offline-profile"></a>Šablonas ne tinkle

Ne tinkle esantis šablonas nustatomas parduotuvės lygiu. Jis naudojamas siekiant nurodyti operacijų, kurios atliekamos su EKA registru, kai tas registras nėra prijungtas prie kanalo duomenų bazės, nusiuntimo parametrus.

#### <a name="functionality-profile"></a>Funkcijų šablonas

Funkcijų šablonas nustatomas parduotuvės lygiu. Jis naudojamas siekiant nurodyti visos parduotuvės funkcijų, kurias galima atlikti su EKA, parametrus. Toliau nurodytos galimybės yra valdomos naudojant funkcijų šabloną. Šios galimybės yra išdėstomos „FastTab“.

- „FastTab“ **Bendra**.

    - Tarptautinė standartizacijos organizacija (ISO).
    - Kliento kūrimas autonominiu režimu.
    - El. laiško kvito šablonas.
    - Pagrindinio darbuotojų prisijungimo autentifikavimas.

- „FastTab“ **Funkcijos**.

    - Prisijungimo ir išplėstinio prisijungimo valdymas.
    - Finansiniai ir su valiuta susiję EKA aspektai, pavyzdžiui, galimybė įvesti kainas ir nustatyti, ar reikia nurodyti smulkios valiutos dešimtaines dalis.
    - Laiko registravimo suaktyvinimas naudojant EKA.
    - Valdymas, kaip produktai ir mokėjimai rodomi EKA ir kvituose.
    - Dienos pabaigos valdymas.
    - Kanalo duomenų bazės operacijų saugojimo parametrai.
    - Valdymas, kaip EKA yra ieškomi ir kuriami klientai.
    - Valdymas, kaip skaičiuojamos nuolaidos.

- „FastTab“ **Suma**.

    - Didžiausios ir mažiausios galimos kainos.
    - Nuolaidų taikymas ir skaičiavimas.

- „FastTab“ **Informacijos kodai**.

    - Visi informacijos kodų valdymo EKA aspektai. Daugiau informacijos rasite [Informacijos kodai ir informacijos kodų grupės](info-codes-retail.md).

- „FastTab“ **Kvitų numeravimas**.

    - Nurodykite kvitų numeravimo šablonus, kuriuose gali būti parduotuvės numerio, mokėjimo terminalo numerio, konstantų ir ar pardavimas, grąžinimas, pardavimo užsakymai ir pasiūlymai spausdinami atskirose sekose, ar jie visi sekami ta pačia seka.

#### <a name="receipt-profiles"></a>Kvitų profiliai

Kvitų profiliai priskirti aparatūros šablono spausdintuvams. Jie naudojami siekiant nurodyti konkrečiu spausdintuvu spausdinamų kvitų tipus. Šablonai apima kvito formatų parametrus ir parametrus, kurie nustato, ar kvitas yra visada spausdinamas, ar kasininkas yra paraginamas nurodyti, ar kvitą reikia spausdinti. Skirtinguose spausdintuvuose taip pat gali būti naudojami skirtingi kvitų šablonai. Pvz., 1 spausdintuvas yra standartinis terminis kvitų spausdintuvas ir todėl spausdina mažesnio formato kvitus. Tačiau 2 spausdintuvas yra viso dydžio kvitų spausdintuvas, kuriuo spausdinami tik tie klientų kvitai, kuriuose reikia daugiau vietos informacijai pateikti. Daugiau informacijos rasite Kvitų [profilio konfigūravimas](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Aparatūros šablonai

Aparatūros profiliai paaiškinti kaip kliento nustatymo komponentas anksčiau šioje temoje. Aparatūros profiliai priskiriami tiesiogiai EKA kasos aparatui arba bendrai naudojamai aparatūros stotyje ir naudojami įrenginių, kurie naudojami konkrečiam EKA kasos aparatui arba aparatūros stotis, tipams nurodyti. Aparatūros šablonai taip pat naudojami siekiant nurodyti EFT parametrus, naudojamus ryšiui su mokėjimo SDK palaikyti.

#### <a name="visual-profiles"></a>Vaizdo šablonai

Vaizdo profiliai naudojami nurodyti konkretaus registro temą ir priskirti kasos aparato lygiu. Profiliai apima naudojamos programos tipo (MPOS arba Debesis EKA), akcento spalvą ir temą, šrifto schemą, prisijungimo puslapio foną ir EKA foną. Daugiau informacijos ieškokite "Create [point of sale (POS)" vaizdo profiliai](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Pasirinktiniai laukai

Galite kurti pasirinktinius laukus, norėdami įtraukti laukų, kurie EKA nėra teikiami parengti naudoti. Daugiau informacijos apie tai, kaip naudoti pasirinktinius laukus, žr. dalį [Darbas su pasirinktiniais laukais (tinklaraščio įrašas)](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Kalbos tekstas

Galite perrašyti numatytuosius EKA parametrus, naudodami kalbos teksto įrašus. Norėdami perrašyti EKA eilutę, įtraukite naują kalbos teksto eilutę. Tada nurodykite ID, numatytąją eilutę, kuri turėtų būti perrašyta, ir tekstą, kuris EKA turėtų būti rodomas vietoj numatytosios eilutės.

### <a name="channel-reports-configuration"></a>Kanalo ataskaitų konfigūravimas

Kanale teikiamas ataskaitas galima nustatyti puslapyje **Kanalo ataskaitų konfigūravimas**. Naujas ataskaitas galite kurti pateikdami ataskaitos XML aprašą ir ataskaitą priskirdami konkrečiai EKA teisių grupei.

### <a name="devices"></a>Įrenginiai

Įrenginiai yra paaiškinti šiame straipsnyje anksčiau. Jie naudojami konkretaus EKA registro aktyvinimui valdyti. Įrenginiai taip pat naudojami siekiant nurodyti programą, skirtą konkrečiam registrui ir diegimo paketui, naudojamam MPOS klientui diegti. Toliau pateikiamos įrenginio aktyvinimo būsenos.

- **Laukiama** – įrenginys paruoštas aktyvinti.
- **Aktyvinta** – įrenginys suaktyvintas.
- **Išaktyvinta** – įrenginys išaktyvintas būstinėje arba naudojant EKA.
- **Išjungta** – įrenginys išjungtas.

Papildoma su aktyvinimu susijusi informacija apima darbuotoją, kuris pakeitė įrenginio aktyvinimo būseną, aktyvinimo laiko antspaudą ir informaciją apie tai, ar įrenginio konfigūracija buvo patvirtinta.

### <a name="client-data-synchronization"></a>Kliento duomenų sinchronizavimas

Visi EKA kliento keitimai, išskyrus įrenginio aktyvinimo būsenos keitimus, turi būti sinchronizuoti su kanalo duomenų baze, kad įsigaliotų. Norėdami sinchronizuoti keitimus su kanalo duomenų baze, pasirinkite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas** ir vykdykite reikiamą paskirstymo grafiką. Atlikę kliento keitimų, turėtumėte vykdyti paskirstymo grafikus **Registrai** ir **Kanalo konfigūracija**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Konfigūruoti ir diegti „Retail Hardware Station“](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
