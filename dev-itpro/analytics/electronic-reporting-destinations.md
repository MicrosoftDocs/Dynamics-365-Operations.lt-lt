---
title: "Elektroninių ataskaitų paskirties vietos"
description: "Galite sukonfigūruoti kiekvienos elektroninių ataskaitų (ER) formato konfigūracijos ir jos sukurto komponento paskirties vietą (aplanką arba failą). Vartotojai, turintys reikiamas teises, paskirties vietos parametrus gali taip pat keisti apdorojimo metu. Šiame straipsnyje paaiškinami ER paskirties vietų valdymas, palaikomi paskirties vietų tipai ir saugumo klausimai."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Elektroninių ataskaitų paskirties vietos

Galite sukonfigūruoti kiekvienos elektroninių ataskaitų (ER) formato konfigūracijos ir jos sukurto komponento paskirties vietą (aplanką arba failą). Vartotojai, turintys reikiamas teises, paskirties vietos parametrus gali taip pat keisti apdorojimo metu. Šiame straipsnyje paaiškinami ER paskirties vietų valdymas, palaikomi paskirties vietų tipai ir saugumo klausimai.

Elektroninių ataskaitų (ER) formato konfigūracijos paprastai turi bent vieną išvesties komponentą: failą. Paprastai konfigūracijos kelių skirtingų tipų (pvz., XML, TXT arba XLSX) failų išvesties komponentų, sugrupuotų į vieną arba kelis aplankus. ER paskirties vietos valdymo funkcija suteikia galimybę iš anksto sukonfigūruoti, kas įvyksta vykdant kiekvieną komponentą. Pagal numatytuosius nustatymus, paleidus konfigūraciją, dialogo langas pasirodo, leidžia vartotojui Išsaugoti ar atidaryti failą. Tas pats procesas taip pat vykdomas importuojant ER konfigūraciją ir nesukonfigūruojant jokių konkrečių jos paskirties vietų. Sukūrus pagrindinio išvesties komponento paskirties vietą, ta paskirties vieta perrašo numatytąją ir aplankas arba failas siunčiamas pagal paskirties vietos parametrus.

## <a name="availability-and-general-prerequisites"></a>Prieinamumas ir bendrieji reikalavimai
ER kur vykstate funkcija nėra Microsoft Dynamics 365 operacijų 7.0 (2016 m. vasario) išleidimo. Todėl, turite įdiegti "Microsoft Dynamics 365" (2016 m. vasario išleidimo) operacijoms, skirtoms naudoti visas funkcijas, aprašytas šioje temoje. Taip pat galite įdiegti vieną iš šių sąlygų. Tačiau Turėkite omenyje, kad šie Alternatyvūs užtikrinti mažesnį ER paskirties patirtį.

-   Microsoft Dynamics 365 operacijų programos versijos 7.0.1 (2016 m. gegužės)
-   ER paskirties vietų valdymo [programos karštosios pataisos](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Paskirties vietas galite nustatyti tik importuotoms ER konfigūracijoms ir tik tokiems ER konfigūracijų formatams, kurie pateikti puslapyje **Elektroninių ataskaitų konfigūracijos**.

## <a name="overview"></a>Peržiūra
ER paskirties valdymo funkciją galima rasti **organizacijos administracijos**&gt;**elektroniniai pranešimai**. Čia galite perrašyti numatytuosius konfigūracijos parametrus. Importuotos konfigūracijos čia bus rodomos tik tada, kai spustelėsite **Nauja** ir tada lauke **Nuoroda** pasirinksite, kuriai konfigūracijai norite kurti paskirties vietų parametrus.

[![Pasirinkti konfigūracijos numerį laukelyje](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Kai sukursite nuorodą, galite sukurti failo paskirties vietą kiekvieno aplanko arba failo. 

[![Sukurti failo paskirties](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Pastaba.** Kiekvienam to paties formato išvesties komponentui galite sukurti vieną failų paskirties vietą, pvz., aplanką ar failą, pasirenkamą lauke **Failo vardas**. Tada galite įjungti ir išjungti atskiros vietos į paskirties failą į **paskirties parametrai** dialogo lange. Mygtukas **Parametrai** yra naudojamas siekiant valdyti visas pasirinktos failo paskirties vietos paskirties vietas. Dialogo lange **Paskirties vietos parametrai** galite atskirai valdyti kiekvieną paskirties vietą, nustatydami jos parinktį **Įgalinta**.

[![Paskirties parametrų dialogo langas](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Paskirties vietų tipai
Galima naudoti įvairius paskirties vietų tipus. Galite išjungti arba įjungti visus tipus vienu metu. Tokiu būdu galite nieko nedaryti arba siųsti komponentą į visas sukonfigūruotas paskirties vietas. Tolesniuose skyriuose aprašomos palaikomos paskirties vietos.

### <a name="email-destination"></a>El. pašto paskirties vieta

Nustatykite parinktį **Įgalinta **į **Taip**, norėdami siųsti išvesties failą el. paštu. Po to, kai ši parinktis įjungta, galite nurodyti elektroninio pašto gavėjams ir redaguokite temą ir el. laiško. Galite nustatyti nuolatinis tekstų, skirtų siųsti temą ir kūno arba ER formules galite naudoti dinamiškai sukurti laišką tekstų. Galite konfigūruoti el. pašto adresus už ER dviem būdais. Konfigūracija gali būti baigtas per valdymo funkciją spausdinti Dynamics 365 operacijoms baigia jį taip pat. Kita vertus, el. pašto adresą galite išspręsti naudodami tiesioginė nuoroda į ER konfigūraciją per formulę.

### <a name="email-address-types"></a>El. pašto adresų tipai

Spustelėjus **redaguoti**, į **į** ar **Cc** srityje, į **el. paštu** dialogo langas. Galite pasirinkti kokį el. pašto adresą naudoti.

[![Rašykite į dialogo langą](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Spausdinimo valdymas

Jei pasirinksite į **spausdinimo valdymo elektroninio pašto** tipo, galite įvesti fiksuotą el. pašto adresus, į **į** lauke. Naudoti el. pašto adresų, kurie nėra įtvirtinti, turite pasirinkti failo paskirties el. pašto šaltinio tipas. Palaiko šias vertes: **klientų**, **tiekėjo**, **perspektyva**, **kontaktas**, **konkurentas**, **darbuotojo**, **pareiškėjas**, **potencialių tiekėjų**, ir **apibrėžėte kaip neleistinas tiekėjo**. Pasirinkę el. šaltinio tipas, naudokite mygtuką šalia į **el. pašto paskyrai šaltinio** lauką, kurį norite atidaryti, ** formulių kūrimo priemonę ** forma. Šioje formoje galite pridėti formulę, kuri yra pasirinktos šalies sąskaitos elektroninio pašto paskirties vietą.

[![Konfigūruoti spausdinimo valdymo elektroninio pašto rūšis](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Atkreipkite dėmesį, kad formulės būdingos ER konfigūracijai. Srityje **Formulė** įveskite konkretaus dokumento nuorodą į kliento arba tiekėjo šalies tipą. Užuot rinkę tekstą, galite surasti duomenų šaltinio mazgą, atitinkantį kliento ar tiekėjo sąskaitą ir tada spustelėti **Įtraukti duomenų šaltinį**, kad atnaujintumėte formulę. Pavyzdys: jei naudojate ISO 20022 kredito perkėlimo konfigūraciją, tiekėjo sąskaitą atitinkantis mazgas yra **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Priešingu atveju įveskite bet kokią eilutės reikšmę, pvz., **DE-001**, kad įrašytumėte formulę.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

– Į **el. paštu** dialogo langas, spustelėkite šiukšlinę, esančią šalia į **el. paštu pirminę sąskaitą** lauką, kurį norite visam laikui panaikinti el. paštas pirminę sąskaitą formulė. Taip pat galite atidaryti formulių kūrimo priemonę keisti anksčiau įrašytą formulę. Norėdami priskirti el. pašto adresus, spustelėkite **redaguoti** atidaryti, **priskirti el. pašto adresai** dialogo lange.

[![Priskyrimas el. pašto paskirties el. pašto adresus](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigūravimo el. laiškas

Naudoti šį el. pašto tipą, jei jūsų naudojamą konfigūracijos duomenų šaltiniuose mazgo, kuriame yra el. pašto adresą. Norėdami gauti tinkamai suformatuotas el. pašto adresą galite naudoti duomenų šaltinius ir funkcijas, formulių kūrimo priemonę.

[![Priskyrimas el. pašto paskirties el. pašto adreso duomenų šaltinis](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Pastaba.** Turi būti sukonfigūruotas ir pasiekiamas paprastųjų pašto siuntų protokolo (SMTP) serveris. Nurodykite SMTP serverį Dynamics 365 operacijoms, tuo **sistemos administravimo**&gt;**nustatymo**&gt;**el. paštas**&gt;**el. pašto parametrai**.

### <a name="archive-destination"></a>Archyvo paskirties vieta

Šią parinktį galite naudoti, norėdami išvestį siųsti į „Microsoft SharePoint“ aplanką arba Microsoft Azure“ saugyklą. Nustatykite parinktį **Įgalinta** į **Taip**, norėdami išvestį siųsti į paskirties vietą, kuri nustatoma pagal pasirinkto dokumento tipą. Pasirinkti galima tik tų tipų dokumentus, kurių grupė nustatyta kaip **Failas**. Galite nustatyti dokumento tipų **organizacijos administracijos**&gt;**dokumentų ruošimas**&gt;**dokumentų tipai**. ER paskirties vietų konfigūracija yra tokia pati, kaip dokumentų valdymo sistemos konfigūracija.

[![Dokumento tipų puslapį](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Vieta nurodo, kur failas įrašomas. Po to **Archyvas** paskirties įgalintas, darbas archyve galima įrašyti konfigūracijos vykdymo rezultatus. Galite peržiūrėti rezultatus **organizacijos administracijos**&gt;**elektroniniai pranešimai**&gt;**elektroniniai pranešimai archyvuojami darbo vietų**. **Pastaba:** galite pasirinkti dokumento tipą darbo Archyvas Dynamics 365 operacijoms, tuo **organizacijos administracijos**&gt;**darbo**&gt;**elektroninės**&gt;**elektroninė duomenų perdavimo parametrus**.

#### <a name="sharepoint"></a>„SharePoint“

Failą galite įrašyti į nustatytą „SharePoint“ aplanką. Galite nustatyti numatytąją SharePoint serverio ne **organizacijos administracijos**&gt;**dokumentų ruošimas**&gt;**dokumentų valdymo parametrai**, kad **SharePoint** tab. Po to, kai SharePoint aplankas yra sukonfigūruotas, galite pasirinkti jį kaip aplankas, kur ER produkcija bus saugomi dokumento tipas. 

[![SharePoint aplanko pasirinkimas](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>„Azure“ saugykla

Kai dokumento tipo vieta yra nustatyta kaip **Archyvo katalogas**, galite įrašyti failą į „Azure“ saugyklą.

### <a name="file-destination"></a>Failo paskirties vieta

Jei nustatysite **įgalinta** į **taip**, kad atidaryti arba įrašyti kaip dialogo langas pasirodo, kai konfigūracija jau baigė darbą.

### <a name="screen-destination"></a>Ekrano paskirties

Jei nustatysite **įgalinta** į **taip**, sukuriamas išvesties peržiūra. Kai kurie failų tipai, pvz., XML, TXT arba PDF, galite peržiūrėti tiesiai naršyklės lange. Kitų failų tipų, tokių Microsoft Excel arba Word, naudojami Microsoft Office Online paslauga.

### <a name="power-bi-destination"></a>Galios BI paskirties

Nustatyti **įgalinta** į **taip** naudoti savo ER konfigūracijos organizuoti duomenų perkėlimą iš savo egzempliorių ir Dynamics 365 operacijoms Microsoft Power BI paslaugoms. Persiųstų failų saugomi Microsoft SharePoint serverio egzemplioriuje, kuris turi būti sukonfigūruota šiam tikslui. Daugiau informacijos rasite [naudoti elektroninių ataskaitų konfigūracijos suteikti Power BI duomenys iš Dynamics 365 operacijoms](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Patarimas.** Norėdami perrašyti numatytuosius parametrus (t. y. konfigūracijos dialogo lango rodymą), galite sukurti pagrindinio išvesties komponento paskirties vietos nuorodą ir failo paskirties vietą, o tada išaktyvinti visas paskirties vietas.

## <a name="security-considerations"></a>Saugos klausimai
Naudojamos dviejų tipų ER paskirties vietoms skirtos teisės ir pareigos. Vieno tipo kontroliuoja gebėjimo išlaikyti bendrą paskirties vietas, yra sukonfigūruotas juridinis asmuo (t. y., jis valdo prieigą prie į **elektroninė duomenų perdavimo vietų** puslapis). Kitas tipas valdo galimybę programos vartotojui vykdymo metu perrašyti paskirties vietos parametrus, kuriuos sukonfigūravo ER kūrėjas arba ER funkcijų konsultantas.

| Vaidmuo (AOT pavadinimas)                     | Vaidmens pavadinimas                                  | Pareiga (AOT pavadinimas)                     | Pareigų pavadinimas                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroninės ataskaitos kūrėjas             | ERFormatDestinationConfigure        | Konfigūruoti elektroninių ataskaitų formato paskirties vietą                |
| ERFunctionalConsultant              | Elektroninės ataskaitos funkcijų konsultantas | ERFormatDestinationConfigure        | Konfigūruoti elektroninių ataskaitų formato paskirties vietą                |
| PaymAccountsPayablePaymentsClerk    | Mokėtinų sumų mokėjimo klerkas            | ERFormatDestinationRuntimeConfigure | Konfigūruoti elektroninių ataskaitų formato paskirties vietą vykdymo aplinkoje |
| PaymAccountsReceivablePaymentsClerk | Gautinų sumų mokėjimo klerkas         | ERFormatDestinationRuntimeConfigure | Konfigūruoti elektroninių ataskaitų formato paskirties vietą vykdymo aplinkoje |

**Pastaba.** Anksčiau nurodytoms pareigoms taikomos dvi teisės. Šių teisių pavadinimai yra tokie patys, kaip atitinkamų pareigų pavadinimai: **ERFormatDestinationConfigure** ir **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Importavau elektronines konfigūracijas ir matau jas puslapyje Elektroninių ataskaitų konfigūracijos. Bet kodėl aš nematau jų elektroninių ataskaitų kelionių puslapyje?

Įsitikinkite, kad jūs spustelėkite **naujas** ir pasirinkite konfigūraciją, į **nuoroda** srityje. Puslapyje **Elektroninių ataskaitų paskirties vietos** rodomos tik tos konfigūracijos, kurių paskirties vietos sukonfigūruotos.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Yra koks nors būdas nustatyti, kurios Azure saugyklos abonementą ir Azure Blob saugyklų naudojami?

Nr. Numatytasis Azure Blob saugyklų, kad yra apibrėžtas ir naudojamas dokumentų valdymo sistema yra naudojama.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Koks tikslas failų paskirties paskirties parametrus? Kam šis parametras skirtas?

Paskirties vieta **Failas** yra naudojama dialogo langui valdyti. Jei įjungsite šią paskirties vietą arba paskirtis yra apibrėžta konfigūracija, galite pamatyti atvirą arba dialogo langas Įrašyti sukūrus išvesties failą.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Ar galite pateikti formulės, nurodančios tiekėjo kodą, kuriam galėčiau siųsti el. laišką, pavyzdį?

Formulė yra būdinga ER konfigūracijai. Pavyzdžiui, jei naudojate ISO 20022 kredito pervedimo konfigūraciją, galite naudoti **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** arba **model.Payments.Creditor.Identification.SourceID**, norėdami gauti susijusį tiekėjo kodą.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Vienoje iš mano formato konfigūracijų yra daug failų, sugrupuotų į vieną aplanką (pvz., 1 aplanke yra 1 failas, 2 failas ir 3 failas). Kaip nustatyti paskirties vietas, kad 1 aplankas.zip nebūtų sukurtas, 1 failas būtų siunčiamas el. paštu, 2 failas būtų siunčiamas į „SharePoint“, o 3 failą galėčiau atidaryti iš karto paleidęs konfigūraciją?

Būtina sąlyga, kad savo forma turi būti prieinama ER konfigūracijų. Jei turite savo formatą, atidarykite puslapį **Elektroninių ataskaitų paskirties vietos** ir sukurkite naują nuorodą į šią konfigūraciją. Kiekvienam iš keturių išvesties komponentų turi būti nurodyta po vieną failo paskirties vietą. Sukurkite pirmąją failo paskirties vietą, suteikite jai pavadinimą, pvz., **Aplankas**, ir pasirinkite failo vardą, kuris jūsų konfigūracijoje nurodo aplanką. Tada spustelėkite **Parametrai** ir įsitikinkite, kad visos paskirties vietos yra išaktyvintos. Šio failo paskirties vietos aplankas nebus sukurtas. Pagal numatytuosius parametrus dėl hierarchinės failų ir pirminių aplankų priklausomybės su visais failais bus atliekamas tas pats veiksmas. Kitaip tariant, jie niekur nebus siunčiami. Norėdami perrašyti numatytuosius parametrus, turite sukurti tris papildomas failų paskirties vietas, t. y. po vieną kiekvienam failui. Kiekvieno failo paskirties vietos parametruose turite suaktyvinti paskirties vietą, į kurią failas turėtų būti siunčiamas.

# <a name="see-also"></a>Taip pat žiūrėkite

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)


