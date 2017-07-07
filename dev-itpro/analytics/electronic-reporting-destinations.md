---
title: "Elektroninių ataskaitų paskirties vietos"
description: "Galite sukonfigūruoti kiekvienos elektroninių ataskaitų (ER) formato konfigūracijos ir jos sukurto komponento paskirties vietą (aplanką arba failą). Vartotojai, turintys reikiamas teises, paskirties vietos parametrus gali taip pat keisti apdorojimo metu. Šiame straipsnyje paaiškinami ER paskirties vietų valdymas, palaikomi paskirties vietų tipai ir saugumo klausimai."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fb2aeee1f38823e7ea96071f773e8448d65ba8ff
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017


---

# <a name="electronic-reporting-destinations"></a>Elektroninių ataskaitų paskirties vietos

[!include[banner](../includes/banner.md)]


Galite sukonfigūruoti kiekvienos elektroninių ataskaitų (ER) formato konfigūracijos ir jos sukurto komponento paskirties vietą (aplanką arba failą). Vartotojai, turintys reikiamas teises, paskirties vietos parametrus gali taip pat keisti apdorojimo metu. Šiame straipsnyje paaiškinami ER paskirties vietų valdymas, palaikomi paskirties vietų tipai ir saugumo klausimai.

Elektroninių ataskaitų (ER) formato konfigūracijos paprastai turi bent vieną išvesties komponentą: failą. Paprastai konfigūracijos kelių skirtingų tipų (pvz., XML, TXT arba XLSX) failų išvesties komponentų, sugrupuotų į vieną arba kelis aplankus. ER paskirties vietos valdymo funkcija suteikia galimybę iš anksto sukonfigūruoti, kas įvyksta vykdant kiekvieną komponentą. Pagal numatytuosius parametrus paleidus konfigūraciją pasirodo dialogo langas, kuriame vartotojas gali įrašyti arba atidaryti failą. Tas pats procesas taip pat vykdomas importuojant ER konfigūraciją ir nesukonfigūruojant jokių konkrečių jos paskirties vietų. Sukūrus pagrindinio išvesties komponento paskirties vietą, ta paskirties vieta perrašo numatytąją ir aplankas arba failas siunčiamas pagal paskirties vietos parametrus.

## <a name="availability-and-general-prerequisites"></a>Prieinamumas ir bendrieji reikalavimai
ER paskirties vietų funkcijų negalima naudoti programoje „Microsoft Dynamics AX“ 7.0 (2016 m. vasario mėn. leidimas). Todėl turite įdiegti „Microsoft Dynamics 365 for Operations“ versiją 1611 (2016 m. lapkričio mėn. leidimą), kad galėtumėte naudoti visas šioje temoje aprašytas funkcijas. Arba galite įdiegti vieną iš toliau nurodytų būtinųjų komponentų. Tačiau nepamirškite, šie alternatyvūs komponentai suteikia labiau ribotą ER paskirties vietos patirtį.

-   „Microsoft Dynamics AX“ 7.0.1 programos versija (2016 m. gegužės mėn.)
-   ER paskirties vietų valdymo [programos karštosios pataisos](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Paskirties vietas galite nustatyti tik importuotoms ER konfigūracijoms ir tik tokiems ER konfigūracijų formatams, kurie pateikti puslapyje **Elektroninių ataskaitų konfigūracijos**.

## <a name="overview"></a>Peržiūra
ER paskirties valdymo funkciją galima rasti pasirinkus **Organizacijos administravimas** &gt; **Elektroninės ataskaitos**. Čia galite perrašyti numatytuosius konfigūracijos parametrus. Importuotos konfigūracijos čia bus rodomos tik tada, kai spustelėsite **Nauja** ir tada lauke **Nuoroda** pasirinksite, kuriai konfigūracijai norite kurti paskirties vietų parametrus.

[![Konfigūracijos pasirinkimas lauke Nuoroda](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Sukūrę nuorodą, galite sukurti failo paskirties vietą kiekvienam aplankui arba failui. 

[![Failo paskirties vietos kūrimas](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Pastaba.** Kiekvienam to paties formato išvesties komponentui galite sukurti vieną failų paskirties vietą, pvz., aplanką ar failą, pasirenkamą lauke **Failo vardas**. Tada galite įjungti ir išjungti atskiras failų paskirties vietas dialogo lange **Paskirties vietų parametrai**. Mygtukas **Parametrai** yra naudojamas siekiant valdyti visas pasirinktos failo paskirties vietos paskirties vietas. Dialogo lange **Paskirties vietos parametrai** galite atskirai valdyti kiekvieną paskirties vietą, nustatydami jos parinktį **Įgalinta**.

[![Dialogo langas Paskirties vietos parametrai](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Paskirties vietų tipai
Galima naudoti įvairius paskirties vietų tipus. Galite išjungti arba įjungti visus tipus vienu metu. Tokiu būdu galite nieko nedaryti arba siųsti komponentą į visas sukonfigūruotas paskirties vietas. Tolesniuose skyriuose aprašomos palaikomos paskirties vietos.

### <a name="email-destination"></a>El. pašto paskirties vieta

Nustatykite parinktį **Įgalinta** į **Taip**, norėdami siųsti išvesties failą el. paštu. Suaktyvinę šią parinktį, galite nurodyti el. laiško gavėjus ir redaguoti el. laiško temą bei tekstą. Galite nustatyti nuolatinį el. laiško temos ir teksto tekstą arba galite naudoti ER formules, norėdami el. laiškų tekstą kurti dinamiškai. ER el. pašto adresus galite konfigūruoti dviem būdais. Konfigūravimą galima atlikti taip pat, kaip jį atlieka spausdinimo valdymo funkcija programoje „Finance and Operations“. Arba galite nustatyti el. pašto adresą naudodami tiesioginę nuorodą į ER konfigūraciją per formulę.

### <a name="email-address-types"></a>El. pašto adresų tipai

Spustelėjus lauko **Kam** arba **Kopija** parinktį **Redaguoti**, rodomas dialogo langas **Siųsti el. laišką**. Tada galite pasirinkti norimą naudoti el. pašto adreso tipą.

[![Dialogo langas Siųsti el. laišką](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Spausdinimo valdymas

Jei pasirinksite tipą **Spausdinimo valdymo el. paštas**, galite įvesti fiksuotus el. pašto adresus lauke **Kam**. Norėdami naudoti nefiksuotus el. pašto adresus, turite pasirinkti failo paskirties vietos el. pašto šaltinio tipą. Palaikomos šios vertės: **Klientas**, **Tiekėjas**, **Potencialus klientas**, **Kontaktas**, **Konkurentas**, **Darbuotojas**, **Pretendentas**, **Galimas tiekėjas** ir **Neleidžiamas tiekėjas**. Pasirinkę el. pašto šaltinio tipą, naudokite šalia lauko **El. pašto šaltinio sąskaita** esantį mygtuką, kad atidarytumėte formą **Formulės dizaino įrankis**. Šią formą galite naudoti norėdami pridėti formulę, kuri nurodo pasirinktos šalies sąskaitą į el. pašto paskirties vietą.

[![Spausdinimo valdymo el. pašto tipo konfigūravimas](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Atkreipkite dėmesį, kad formulės būdingos ER konfigūracijai. Srityje **Formulė** įveskite konkretaus dokumento nuorodą į kliento arba tiekėjo šalies tipą. Užuot rinkę tekstą, galite surasti duomenų šaltinio mazgą, atitinkantį kliento ar tiekėjo sąskaitą ir tada spustelėti **Įtraukti duomenų šaltinį**, kad atnaujintumėte formulę. Pavyzdys: jei naudojate ISO 20022 kredito perkėlimo konfigūraciją, tiekėjo sąskaitą atitinkantis mazgas yra **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Priešingu atveju įveskite bet kokią eilutės reikšmę, pvz., **DE-001**, kad įrašytumėte formulę.

[![Formulės dizaino įrankis](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Dialogo lange **Siųsti el. laišką** spustelėkite šalia lauko **El. pašto šaltinio sąskaita** esančią šiukšlinę, kad visam laikui panaikintumėte el. pašto šaltinio sąskaitos formulę. Arba atidarykite formulės dizaino įrankį, kad pakeistumėte anksčiau įrašytą formulę. Norėdami priskirti el. pašto adresus, spustelėkite **Redaguoti**, kad atidarytumėte dialogo langą **Priskirti el. pašto adresus**.

[![El. pašto paskirties vietos el. pašto adresų priskyrimas](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigūravimo el. laiškas

Naudokite šį el. pašto tipą, jei jūsų naudojamos konfigūracijos duomenų šaltiniuose yra mazgas, nurodantis el. pašto adresą. Galite naudoti duomenų šaltinius ir funkcijas formulės dizaino įrankyje, kad gautumėte teisingai suformatuotą el. pašto adresą.

[![El. pašto paskirties vietos el. pašto adreso duomenų šaltinio priskyrimas](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Pastaba.** Turi būti sukonfigūruotas ir pasiekiamas paprastųjų pašto siuntų protokolo (SMTP) serveris. SMTP serverį galite nurodyti programoje „Finance and Operations“, pasirinkdami **Sistemos administravimas** &gt; **Sąranka** &gt; **El. paštas** &gt; **El. pašto parametrai**.

### <a name="archive-destination"></a>Archyvo paskirties vieta

Šią parinktį galite naudoti, norėdami išvestį siųsti į „Microsoft SharePoint“ aplanką arba Microsoft Azure“ saugyklą. Nustatykite parinktį **Įgalinta** į **Taip**, norėdami išvestį siųsti į paskirties vietą, kuri nustatoma pagal pasirinkto dokumento tipą. Pasirinkti galima tik tų tipų dokumentus, kurių grupė nustatyta kaip **Failas**. Dokumentų tipus galite nustatyti pasirinkdami **Organizacijos administravimas** &gt; **Dokumentų valdymas** &gt; **Dokumentų tipai**. ER paskirties vietų konfigūracija yra tokia pati, kaip dokumentų valdymo sistemos konfigūracija.

[![Puslapis Dokumentų tipai](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Vieta nurodo, kur failas įrašomas. Kai paskirties vieta **Archyvas** suaktyvinta, konfigūracijos vykdymo rezultatus galima įrašyti užduoties archyve. Rezultatus galite peržiūrėti pasirinkdami **Organizacijos administravimas** &gt; **Elektroninės ataskaitos** &gt; **Suarchyvuotos elektroninių ataskaitų užduotys**. **Pastaba.** Norėdami pasirinkti užduočių archyvo dokumento tipą programoje „Finance and Operations“ pasirinkite **Organizacijos administravimas** &gt; **Darbo sritys** &gt; **Elektroninių ataskaitų darbo sritis** &gt; **Elektroninių ataskaitų parametrai**.

#### <a name="sharepoint"></a>„SharePoint“

Failą galite įrašyti į nustatytą „SharePoint“ aplanką. Numatytąjį „SharePoint“ serverį galite nustatyti skirtuke **SharePoint** pasirinkdami **Organizacijos administravimas** &gt; **Dokumentų valdymas** &gt; **Dokumentų valdymo parametrai**. Sukonfigūravus „SharePoint“ aplanką, dokumento tipe galite jį nurodyti kaip aplanką, kuriame ER išvestis bus įrašyta. 

[![„SharePoint“ aplanko pasirinkimas](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>„Azure“ saugykla

Kai dokumento tipo vieta yra nustatyta kaip **Archyvo katalogas**, galite įrašyti failą į „Azure“ saugyklą.

### <a name="file-destination"></a>Failo paskirties vieta

Jei parinktį **Įjungta** nustatysite į **Taip**, kai konfigūracija baigta, rodomas atidarymo arba įrašymo dialogo langas.

### <a name="screen-destination"></a>Ekrano paskirties vieta

Jei parinktį **Įjungta** nustatysite į **Taip**, sukuriama išeigos peržiūra. Kai kuriuos failų tipus, pvz., XML, TXT arba PDF, galite peržiūrėti tiesiogiai naršyklės lange. Kitiems failų tipams, pvz., „Microsoft Excel“ arba „Word“, peržiūrėti naudojama „Microsoft Office“ internetinė paslauga.

### <a name="power-bi-destination"></a>„Power BI“ paskirties vieta

Nustatykite parinktį **Įjungta** į **Taip**, norėdami naudoti ER konfigūraciją, kad išdėstytumėte duomenų perkėlimą iš „Finance and Operations“ egzemplioriaus į „Microsoft Power BI“ tarnybas. Perkelti failai saugomi „Microsoft SharePoint Server“ egzemplioriuje, kuris šiuo tikslu turi būti sukonfigūruotas. Norėdami gauti daugiau informacijos, žr. [Elektroninių ataskaitų konfigūracijos naudojimas norint paslaugai „Power BI“ teikti duomenų iš „Finance and Operations“](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Patarimas.** Norėdami perrašyti numatytuosius parametrus (t. y. konfigūracijos dialogo lango rodymą), galite sukurti pagrindinio išvesties komponento paskirties vietos nuorodą ir failo paskirties vietą, o tada išaktyvinti visas paskirties vietas.

## <a name="security-considerations"></a>Saugos klausimai
Naudojamos dviejų tipų ER paskirties vietoms skirtos teisės ir pareigos. Vienas tipas valdo galimybę išsaugoti sukonfigūruotas bendras juridinio subjekto paskirties vietas (t. y. valdo prieigą prie puslapio **Elektroninių ataskaitų paskirties vietos**). Kitas tipas valdo galimybę programos vartotojui vykdymo metu perrašyti paskirties vietos parametrus, kuriuos sukonfigūravo ER kūrėjas arba ER funkcijų konsultantas.

| Vaidmuo (AOT pavadinimas)                     | Vaidmens pavadinimas                                  | Pareiga (AOT pavadinimas)                     | Pareigų pavadinimas                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroninės ataskaitos kūrėjas             | ERFormatDestinationConfigure        | Konfigūruoti elektroninių ataskaitų formato paskirties vietą                |
| ERFunctionalConsultant              | Elektroninės ataskaitos funkcijų konsultantas | ERFormatDestinationConfigure        | Konfigūruoti elektroninių ataskaitų formato paskirties vietą                |
| PaymAccountsPayablePaymentsClerk    | Mokėtinų sumų mokėjimo klerkas            | ERFormatDestinationRuntimeConfigure | Konfigūruoti elektroninių ataskaitų formato paskirties vietą vykdymo aplinkoje |
| PaymAccountsReceivablePaymentsClerk | Gautinų sumų mokėjimo klerkas         | ERFormatDestinationRuntimeConfigure | Konfigūruoti elektroninių ataskaitų formato paskirties vietą vykdymo aplinkoje |

**Pastaba.** Anksčiau nurodytoms pareigoms taikomos dvi teisės. Šių teisių pavadinimai yra tokie patys, kaip atitinkamų pareigų pavadinimai: **ERFormatDestinationConfigure** ir **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Importavau elektronines konfigūracijas ir matau jas puslapyje Elektroninių ataskaitų konfigūracijos. Tačiau kodėl aš jų nematau puslapyje Elektroninių ataskaitų paskirties vietos?

Įsitikinkite, kad spustelėjote **Nauja** ir tada pasirinkote konfigūraciją lauke **Nuoroda**. Puslapyje **Elektroninių ataskaitų paskirties vietos** rodomos tik tos konfigūracijos, kurių paskirties vietos sukonfigūruotos.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Ar galima nustatyti, kuri „Azure“ saugyklos paskyra ir kuri „Azure‟ didelių dvejetainių objektų saugykla yra naudojamos?

Nr. Naudojama numatytoji „Azure“ „Azure‟ didelių dvejetainių objektų saugykla, kuri nurodyta ir naudojama dokumentų valdymo sistemoje.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Kokia yra paskirties vietos parametrų parinkties Failas paskirties vieta paskirtis? Kam šis parametras skirtas?

Paskirties vieta **Failas** yra naudojama dialogo langui valdyti. Jei suaktyvinsite šią paskirties vietą arba jei jūsų konfigūracijoje nenurodyta jokia paskirties vieta, sukūrus išvesties failą bus rodomas atidarymo arba įrašymo dialogo langas.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Ar galite pateikti formulės, nurodančios tiekėjo kodą, kuriam galėčiau siųsti el. laišką, pavyzdį?

Formulė yra būdinga ER konfigūracijai. Pavyzdžiui, jei naudojate ISO 20022 kredito pervedimo konfigūraciją, galite naudoti **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** arba **model.Payments.Creditor.Identification.SourceID**, norėdami gauti susijusį tiekėjo kodą.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Vienoje iš mano formato konfigūracijų yra daug failų, sugrupuotų į vieną aplanką (pvz., 1 aplanke yra 1 failas, 2 failas ir 3 failas). Kaip nustatyti paskirties vietas, kad 1 aplankas.zip nebūtų sukurtas, 1 failas būtų siunčiamas el. paštu, 2 failas būtų siunčiamas į „SharePoint“, o 3 failą galėčiau atidaryti iš karto paleidęs konfigūraciją?

Jūsų norimas formatas turi būti įjungtas ER konfigūracijose. Jei turite savo formatą, atidarykite puslapį **Elektroninių ataskaitų paskirties vietos** ir sukurkite naują nuorodą į šią konfigūraciją. Kiekvienam iš keturių išvesties komponentų turi būti nurodyta po vieną failo paskirties vietą. Sukurkite pirmąją failo paskirties vietą, suteikite jai pavadinimą, pvz., **Aplankas**, ir pasirinkite failo vardą, kuris jūsų konfigūracijoje nurodo aplanką. Tada spustelėkite **Parametrai** ir įsitikinkite, kad visos paskirties vietos yra išaktyvintos. Šio failo paskirties vietos aplankas nebus sukurtas. Pagal numatytuosius parametrus dėl hierarchinės failų ir pirminių aplankų priklausomybės su visais failais bus atliekamas tas pats veiksmas. Kitaip tariant, jie niekur nebus siunčiami. Norėdami perrašyti numatytuosius parametrus, turite sukurti tris papildomas failų paskirties vietas, t. y. po vieną kiekvienam failui. Kiekvieno failo paskirties vietos parametruose turite suaktyvinti paskirties vietą, į kurią failas turėtų būti siunčiamas.

# <a name="see-also"></a>Taip pat žiūrėkite

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)




