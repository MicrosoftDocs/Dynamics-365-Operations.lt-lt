---
title: El. pašto ER paskirties vietos tipas
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti el. pašto paskirties vietą kiekvienam aplanko arba failo komponentui elektroninės ataskaitos (ER) formatu.
author: kfend
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 5e58618618d9125db4c81f49f62f48c2ce2f5e62
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285432"
---
# <a name="email-er-destination-type"></a>El. pašto ER paskirties vietos tipas

[!include [banner](../includes/banner.md)]

Paleidus elektroninių ataskaitų (ER) formatą, gali būti sugeneruotas vienas arba daugiau siunčiamų dokumentų. ER formato komponentai **Aplankas** ar **Failas** naudojami norint nurodyti siunčiamų dokumentų struktūrą. Galite konfigūruoti el. pašto paskirties vietą šiems komponentų tipams siųsti siunčiamus dokumentus kaip el. pašto priedus.

Galite konfigūruoti el. pašto paskirties vietą kiekvienam ER formato komponentui **Aplankas** ar **Failas**. Šiuo atveju **kiekvienas siunčiamas dokumentas el. paštu siunčiamas atskirai**. Remiantis šiuo paskirties vietos nustatymu, sugeneruotas dokumentas pristatomas kaip el. laiško priedas. 

> [!NOTE]
> Jei dokumentas nesugeneruotas, nes atitinkamo komponento **Failas** išraiška **Įjungta** sukonfigūruota pateikti Bulio logikos reikšmę **False**, el. laiškas nesiunčiamas, net jei komponento el. pašto paskirties vieta sukonfigūruota ir įjungta.

Taip pat galite [sugrupuoti](#grouping) kelis komponentus **Aplankas** ar **Failas** ir konfigūruoti visų grupės komponentų el. pašto paskirties vietą. Šiuo atveju visi siunčiami dokumentai, kuriuos sugeneravo grupei priklausantys komponentai, **siunčiami kaip keli vieno el. laiško priedai**. Remiantis šiuo paskirties vietos nustatymu, kiekvienas sugeneruotas dokumentas pristatomas kaip vieno el. laiško priedas.

> [!NOTE]
> Jei bent vieną dokumentą sugeneruojama grupės grupės komponentų komponentas **Failas**, siunčiamas el. laiškas. Jei grupės komponentai dokumento nesugeneruoja, nes komponento **Failas** išraiška **Įjungta** sukonfigūruota pateikti Bulio logikos reikšmę **False**, el. laiškas nesiunčiamas, net jei tos komponentų grupės el. pašto paskirties vieta sukonfigūruota ir įjungta.
>
> **El. paštas** yra vienintelė paskirties vieta, kuri gali būti konfigūruojama komponentų grupei. Norėdami pristatyti dokumentą, siunčiamą el. paštu atsižvelgiant į grupės el. pašto paskirties vietos parametrą, pridėkite dar vieną paskirties vietos įrašą, pasirinkite norimą komponentą ir konfigūruokite kitą šio įrašo paskirties vietą.

Vieno ER formato konfigūracijoje galima sukonfigūruoti kelias komponentų grupes. Tokiu būdu galite konfigūruoti el. pašto paskirties vietą kiekvienai komponentų grupei ir el. pašto paskirties vietą kiekvienam komponentui.

## <a name="enable-an-email-destination"></a>El. pašto paskirties vietos įgalinimas

Norėdami siųsti vieną ar daugiau išvesties failų el. paštu, atlikite šiuos veiksmus.

1. Norėdami **Elektroninės SF vietą** puslapyje **Failo paskirtis** „FastTab“, rinkitės komponentą ar jų grupę tinklelyje..
2. Rinkitės **Nustatymai** ir tada **Paskirties nustatymai** teksto laukelyje **El. paštas** skirtuke nustatykite **Įjungti** paskirtį į **Taip**.

[![El. pašto paskirties vietą parinkties Įjungta nustatymas į parametrą Taip.](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="configure-an-email-destination"></a>El. pašto paskirties vietos konfigūravimas

### <a name="email-content"></a>El. laiško turinys

Galite redaguoti el. laiško temą ir tekstą.

Lauke **Tema** įveskite el. laiško temos tekstą, kuris turi būti rodomas vykdymo metu sugeneruoto elektroninio laiško temos lauke. Lauke **Tekstas** įveskite el. laiško tekstą, kuris turi būti rodomas elektroninio laiško teksto lauke. Galite nustatyti nuolatinį el. laiško temos tekstą ir turinio tekstą arba galite naudoti ER [formules](er-formula-language.md), norėdami el. laiškų tekstą kurti dinamiškai vykdymo metu. Sukonfigūruota formulė turi pateikti tipo [Eilutė](er-formula-supported-data-types-primitive.md#string) vertę.

Jūsų el. laiško tekstas kuriamas TEKSTINIU arba HTML formatu, tai priklauso nuo el. pašto kliento. Galite naudoti bet kurį maketą, stilių ir prekės ženklus, kuriuos leidžia HTML ir įdėtieji pakopinio stiliaus aprašai (CSS).

> [!NOTE]
> El. pašto klientai įveda maketo ir stiliaus apribojimus, dėl kurių gali reikėti atlikti HTML ir CSS, naudojamų pranešimo tekste, koregavimus. Rekomenduojame susipažinti su geriausia HTML kūrimo praktika, kurią palaikys populiariausi el. pašto klientai.
>
> Naudokite tinkamą kodavimą, kad įdiegtumėte grįžimo į eilutės pradžią funkciją, priklausančią nuo teksto formatavimo. Daugiau informacijos ieškokite duomenų tipo [Eilutė](er-formula-supported-data-types-primitive.md#string) apibrėžtyje.

### <a name="email-addresses"></a>El. pašto adresai

Galite nurodyti el. laiško siuntėją ir el. laiško gavėjus. Pagal numatytuosius parametrus el. laiškas siunčiamas dabartinio vartotojo vardu. Norėdami nurodyti kitą el. laiško siuntėją, turite konfigūruoti lauką **Iš**.

> [!NOTE]
> Kai el. pašto paskirties vieta sukonfigūruota, **Iš** lauko, kuris matomas tik vartotojams turintiems `ERFormatDestinationSenderEmailConfigure` saugumo teises, **Konfigūruoti siuntėjo el. pašto adresą ER formato paskirtims**.
>
> Kai el. pašto paskirtis yra siūloma keisti [vykdymo laiku](electronic-reporting-destinations.md#security-considerations), laukelyje **Froma** yra matoma tik vartotojams, turintiems `ERFormatDestinationSenderEmailMaintain` saugos teises, **Išlaikyti siuntėjo el. pašto adresą ER formato paskirčiai**.
>
> Kai **Fromos** laukelis yra konfigūruojamas siekiant naudoti el. pašto adresą, o ne esamo vartotojo, arba **Siųsti kaip** ar **Siųsti kieno vardu** teisės turi būti tinkamai [nustatytos](/microsoft-365/solutions/allow-members-to-send-as-or-send-on-behalf-of-group) iš anksto. Kitu atveju vykdymo metu pateikiama ši išimtis: „Nepavyko siųsti el. laiško kaip iš abonemento, patikrinkite teises Siųsti kaip" skyriuje \<from email account\> iš \<current user account\> bei\<from email account\>.

Galite konfigūruoti lauką **Iš**, kad būtų grąžinamas daugiau nei vienas el. pašto adresas. Šiuo atveju, vardas sąraše naudojamas kaip el. pašto siuntėjo adresas.

Norėdami nurodyti el. pašto gavėjus, turite sukonfigūruoti **Į** ir **Kopija** (pasirinktinai).

ER el. pašto adresus galite konfigūruoti dviem būdais. Konfigūravimą galima baigti taip pat, kaip jį baigia spausdinimo valdymo funkcija, arba galima nustatyti el. pašto adresą, naudojant tiesioginę nuorodą į ER konfigūraciją per formulę.

## <a name="email-address-types"></a>El. pašto adresų tipai

Jei rinksitės **Redaguoti** šalia **Iš**, **į** ar **Kopijos** laukelio **Paskirties nustatymų** teksto laukelyje, atitinkamas **El. paštas iš**, **El. laiško kam**, ar **El. laiško kopija** teksto laukelis pasirodys. Ten galite konfigūruoti el. laiško siuntėją ir el. pašto gavėjus. Pasirinkite **Įtraukti**, tada pasirinkite norimą naudoti el. pašto adreso tipą. Šiuo metu palaikomi du tipai: **Spausdinimo valdymo el. laiškas** ir **Konfigūravimo el. laiškas**.

[![El. pašto adreso tipo pasirinkimas.](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Spausdinimo valdymo el. paštas

Jei rinksitės **Spausdinti valdymo el. paštą** kaip el. pašto adreso tipą, galite įvesti pastovius el. pašto adresus **El. laiškas iš**, **El. laiškas kam**, ar **El. laiško kopija** teksto laukelį nustatydami tolesnius laukelius:

- Lauke **El. pašto šaltinis** pasirinkite **Nėra**.
- Lauke **Papildomi el. pašto adresai, atskirti „;“** įveskite fiksuotus el. pašto adresus.

Taip pat galite gauti el. pašto adresus iš šalies, kurios siuntimo dokumentas generuojamas, kontaktinės informacijos. Norėdami naudoti nefiksuotus el. pašto adresus, lauke **El. pašto šaltinis** pasirinkite failo paskirties vietos [vaidmenį](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles). Palaikomi toliau nurodyti vaidmenys.

- Klientas
- Tiekėjas
- Potencialus klientas
- Kontaktas
- Konkurentas
- Darbuotojas
- Pretendentas
- Galimas tiekėjas
- Neleidžiamas tiekėjas
- Juridinis subjektas

Pavyzdžiui, norėdami sukonfigūruoti ER formato el. pašto paskirties vietą, kuri naudojama tiekėjo mokėjimams apdoroti, pasirinkite vaidmenį **Tiekėjas**.

Pasirinkę pageidaujamą vaidmenį, spustelėkite mygtuką **Susieti** (grandinės simbolis), esantį greta lauko **El. pašto šaltinio sąskaita**, kad galėtumėte atidaryti puslapį [Formulės dizaino įrankis](general-electronic-reporting-formula-designer.md). Tada galite naudoti šį puslapį, kad sukonfigūruotumėte formulę, kuri vykdymo metu pateikia šalies, kuriai priskirtas sukonfigūruotas vaidmuo, numerį iš apdoroto dokumento į el. pašto paskirties vietą.

> [!NOTE]
> Formulės būdingos ER konfigūracijai.

Puslapio **Formulės dizino įrankis** lauke **Formulė** įveskite konkretaus dokumento nuorodą į palaikomą vaidmenį. Užuot įvedę nuorodą, srityje **Duomenų šaltinis** raskite ir pasirinkite duomenų šaltinio mazgą, kuris nurodo sukonfigūruoto vaidmens sąskaitą, tada pasirinkite **Įtraukti duomenų šaltinį**, kad atnaujintumėte formulę. Pvz., jei sukonfigūruosite el. pašto paskirties vietą, skirtą konfigūracijai **ISO 20022 kreditų perkėlimas**, kuri naudojama tiekėjo mokėjimams apdoroti, tiekėjo sąskaitą nurodantis mazgas yra `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![El. pašto šaltinio sąskaitos konfigūravimas.](./media/er_destinations-emaildefineaddresssource.gif)

Jei sukonfigūruoto Microsoft Dynamics vaidmens sąskaitų numeriai yra unikalūs visam 365 finansų egzemplioriui, **·** **el**. paštu siunčiamų laiškų šaltinio įmonės laukas dialogo lange El. laiške gali išlikti tuščias.

Taip pat gali būti, kad skirtingose įmonėse ([juridiniuose subjektuose](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) užregistruotos skirtingos [bendrosios adresų knygelės](../../fin-ops/organization-administration/overview-global-address-book.md) šalys taip, kad jos naudoja tą patį sąskaitos numerį, kad užpildytų sukonfigūruotą vaidmenį. Šiuo atveju sukonfigūruoto vaidmens sąskaitų numeriai nėra unikalūs visame „Finance“ egzemplioriuje. Todėl tam, kad tiesiogiai pasirinktumėte šalį, negalite nurodyti tik sąskaitos numerio. Taip pat turite nurodyti įmonę, kurioje šalis buvo įregistruota, kad būtų galima įvesti sukonfigūruotą vaidmenį. Pasirinkę mygtuką **Susieti** (grandinės simbolis), esantį greta dialogo lango **Siųsti el. laišką** lauko **El. pašto šaltinio įmonė**, kad atidarytumėte puslapį [Formulės dizaino įrankis](general-electronic-reporting-formula-designer.md). Tada galite naudoti šį puslapį, kad sukonfigūruotumėte formulę, kuri vykdymo metu pateikė, įmonės, kuriai reikia surasti pageidaujamą šaltinį, kodą.

> [!TIP]
> Jei reikia naudoti įmonės kodą, kad būtų vykdomas ER formatas, bet ER formatas nepateikia jokio duomenų šaltinio, kurį įmonės kodas gali gauti, konfigūruokite formulę `GetCurrentCompany()` naudodami įtaisytąją ER funkciją [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Formulės būdingos ER konfigūracijai.

Norėdami nurodyti el. pašto adresų, kurie turi būti naudojami vykdymo metu, tipą, dialogo lange **Siųsti el. laišką** pasirinkite **Redaguoti** šalia lauko **Kam**, kad būtų atidarytas išskleidžiamasis dialogo langas **Priskirti el. pašto adresą**. Tada nustatykite toliau nurodytus laukus.

- Lauke **Paskirtis** pasirinkite tikslus. Bus naudojami tik pasirinktos paskirties el. pašto adresai iš aptiktos šalies kontaktų.
- Nustatykite parinktį **Pirminis kontaktas** į parametrą **Taip**, kad naudotumėte el. pašto adresą, sukonfigūruotą kaip pagrindinį aptiktos šalies el. pašto adresą.

> [!NOTE]
> Jei lauke **Paskirtis** pasirenkami tikslai ir parinktis **Pagrindinis kontaktas** nustatoma į parametrą **Taip** tuo pačiu metu, kiekvienas el. laiškas, atitinkantis bent vieną sukonfigūruotą kriterijų, bus naudojamas vykdymo metu.

### <a name="configuration-email"></a>Konfigūravimo el. laiškas

Pasirinkite **konfigūracijos el. pašto adresą** kaip el. pašto adreso tipą, jei naudojama konfigūracija yra duomenų šaltinių, kurie pateikia vieną el. pašto adresą arba keletą el. pašto adresų, atskirtų kabliataškiais (;), mazgas. Norėdami gauti tinkamai suformatuotą [el](er-formula-language.md#Functions) . pašto adresą arba tinkamai suformatuotą el. pašto adresus, atskirtus kabliataškiais, galite naudoti duomenų šaltinius ir funkcijas. Pavyzdžiui, jei naudojate konfigūraciją **ISO 20022 kredito perkėlimas**, mazgas, kuris nurodo pirminį tiekėjo el. pašto adresą iš tiekėjo kontaktinės informacijos, į kurią turi būti siunčiamas lydraštis, yra `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![El. pašto adreso šaltinio konfigūravimas.](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Formato komponentų grupė

Norėdami grupuoti formato komponentus, puslapyje **Elektroninių ataskaitų paskirties vieta**, „FastTab“ **Failo paskirties vieta** pasirinkite komponentus tinklelyje, tada pasirinkite **Grupė**.

**El. paštas** yra vienintelė anksčiau sukonfigūruota paskirties vieta, kuri vis dar prieinama pasirinktiems komponentams. Nėra kitų anksčiau sukonfigūruotų paskirties vietų, nes laikoma, kad komponentų grupė jų nepalaiko. Jums bus pranešta apie šiuos pakeitimus.

Anksčiau pridėtas įrašas laikomas sukurtos grupės antrašte. Šiame antraštės įraše yra grupės el. pašto paskirties parametrai. Kituose įrašuose yra grupės nariai, kurie naudos el. pašto paskirties parametrus grupės antraštės įraše.

Norėdami išgrupuoti formato komponentus, „FastTab“ **Failo paskirties vieta** pasirinkite įrašą, kuris priklauso grupei, tada pasirinkite **Išgrupuoti**.

- Jei pasirinksite antraštės įrašą, visa grupė bus išgrupuota.
- Jei pasirinksite nario įrašą ir tai bus paskutinio grupės nario įrašas, visa grupė bus išgrupuota.
- Jei pasirinksite nario, kuris nėra paskutinis grupės narys, įrašą, šis įrašas nebus įtrauktas į dabartinę grupę.

Toliau pateiktoje iliustracijoje vaizduojama ER formato struktūra, sukonfigūruota, kad būtų sukurtas suglaudintas siunčiamas failas, kuriame yra priminimo laiško pastaba ir tinkamos kliento SF PDF formatu.

[![Siuntimo dokumentus generuojančio ER formato struktūra.](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Toliau esanti iliustracija rodo procesą, kaip aprašyta šiame straipsnyje, **atskirų** komponentų grupavimą ir naujos grupės el. pašto paskirties vietos įgalinimą, kad priminimo laiško pastaba būtų siunčiama kartu su atitinkamomis kliento SF kaip el. laiškų priedai.

[![Atskirų komponentų grupavimas ir el. pašto paskirties vietos įjungimas.](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)
- [Elektroninių ataskaitų (ER) formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
