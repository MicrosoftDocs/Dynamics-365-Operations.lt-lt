---
title: "Spausdintinų LFSF formų generavimas"
description: "Šioje temoje paaiškinama, kaip naudoti elektroninių ataskaitų (ER) sistemą, norint spausdintinas laisvos formos SF (LFSF) sugeneruoti kaip „Microsoft Office“ dokumentus."
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d27a11a0d925b0f1164578f9c04e6abd4736b2b2
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="generate-printable-fti-forms"></a>Spausdintinų LFSF formų generavimas

[!include[banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) sistema leidžia spausdintinas laisvos formos SF (LFSF) sugeneruoti kaip „Microsoft Office“ dokumentus. Šioje temoje pateikiama informacija apie tai, kaip sukurti savo konfigūracijas, taip pat išsami informacija apie pasiekiamus konfigūracijos šablonus.

## <a name="overview"></a>Apžvalga

Dabar spausdintinas LFSF formas galite sugeneruoti ne tik naudodami „Microsoft“ SQL serverio ataskaitų tarnybas (SSRS), bet ir ER sistemą. Spausdintinas LFSF formas galite tvarkyti programose „Microsoft Office Excel“ ir „Word“. Taip pat galite keisti maketą, duomenų srautą ir formatavimą, kad šie atitiktų tam tikrus reikalavimus neatliekant kodo keitimų.

> [!NOTE]
> Jei norite pradėti esamų šio pavyzdžio spausdintinų LFSF formų sprendimo ER konfigūracijų apžvalgą, galite eiti tiesiai į skyrių **Pavyzdinių ER konfigūracijų atsisiuntimas, norint sugeneruoti spausdintinas LFSF formas**, kuris pateikiamas toliau šioje temoje.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Spausdintinų LFSF formų tinkintų konfigūracijų kūrimas
Taikydami tinkintą spausdintinų LFSF formų sprendimą, taip pat turite sukurti ER konfigūracijų rinkinį.

### <a name="configure-the-er-data-model"></a>ER duomenų modelio konfigūravimas
Jūsų programoje turi būti įtraukta ER duomenų modelio konfigūracija, kurioje yra duomenų modelis, apibūdinantis kliento SF išrašymo verslo domeną. Kaip reikalaujama, duomenų modeliui turi būti suteiktas pavadinimas **CustomersInvoicing**. Informacijos apie tai, kaip kurti ER duomenų modelius, ieškokite [Elektroninių ataskaitų (ER) specifinio domeno duomenų modelio kūrimas](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>ER modelio susiejimo konfigūravimas
Jūsų programoje turi būti įtrauktas duomenų modelio CustomersInvoicing ER modelio susiejimas. Modelio susiejimas gali būti pateiktas ER duomenų modelio arba ER modelio susiejimo konfigūracijoje. Tačiau šakninio modelio susiejimo aprašo pavadinimas turi būti **FreeTextInvoice**.

Susiejime turi būti toliau nurodyti duomenų šaltiniai.

- Duomenų šaltinio tipas: **Lentelės įrašai**

    - Šiam duomenų šaltiniui turi būti suteiktas pavadinimas **CustInvoiceJour**.
    - Pavadinimas turi nurodyti į programos lentelę CustInvoiceJour.
    - Lentelė naudojama apdorojimo metu, kad iš programos į ER modelio susiejimą būtų galima perduoti pasirinktų spausdinti sąskaitų faktūrų sąrašą.

- Duomenų šaltinio tipas: **Object**

    - Šiam duomenų šaltiniui turi būti suteiktas pavadinimas **PrintMgmtPrintSettingDetail**.
    - Pavadinimas turi nurodyti į programos klasę **PrintMgmtPrintSettingDetail**.
    - Ji naudojama apdorojimo metu, kad iš programos į ER modelio susiejimą būtų galima perduoti vykdomo ER formato spausdinimo valdymo parametrų informaciją.

Programos integravimo su ER sistema informaciją galima rasti klasėje **ERPrintMgmtReportFormatSubscriber** (ER programų paketo integravimo modelis), kuri pateikiama programos šaltinio kode.

Daugiau informacijos apie ER modelio susiejimų kūrimą ieškokite [Elektroninių ataskaitų (ER) modelio susiejimo apibrėžimas ir duomenų šaltinių pasirinkimas](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>ER formato konfigūravimas
Jūsų programos egzemplioriuje turi būti ER formato konfigūracija, kuri bus naudojama LFSF formoms kurti. 

> [!NOTE]
> Ši formato konfigūracija turi būti sukurta duomenų modeliui CustomersInvoicing ir jame turi būti naudojamas modelio susiejimas, turintis šakninį aprašą **FreeTextInvoice**.

Informacijos, kaip konfigūruoti ER formatus ieškokite [Elektroninių ataskaitų (ER) formato konfigūracijos kūrimas](tasks/er-format-configuration-2016-11.md). Informacijos, kaip kurti ER formatus norint ataskaitas generuoti „OpenXML“ formatu, ieškokite [Konfigūracijos, skirtos ataskaitoms „OpenXML” formatu generuoti, kūrimas elektroninėse ataskaitose (ER)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Spausdinimo valdymo konfigūravimas
Norėdami LFSF formas generuoti naudodami ER sistemą, ER formatus galite priskirti tokiu pačiu būdu, kaip ir priskiriant SSRS ataskaitas. Norėdami ER formatą susieti su visomis gautinų sumų LFSF, eikite į **Gautinos sumos** \> **Sąranka** \> **Formos** \> **Formos sąranka** \> **Bendra** \> **Spausdinimo valdymas** \> **Laisvos formos SF** \> **Pradinė versija**. Norėdami ER formatą susieti su konkrečiu klientu arba sąskaita faktūra, atlikite toliau nurodytus veiksmus.

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Pasirinkite LFSF, kurią norite susieti su ER formatu, ir atidarykite puslapį **Spausdinimo valdymo sąranka**.
3. Pasirinkti dokumento lygį ir nurodykite SF aprėptį, reikalingą apdorojimo procedūrai.
4. Pasirinkite nurodyto dokumento lygio ER formatą.

![Spausdinimo valdymo nustatymas](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Pasirinkto formato lauke **Ataskaitos formato peržvalga** bus rodomi tik tie ER formatai, kuriuose naudojamas duomenų modelio **CustomersInvoicing** šakninis aprašas **FreeTextInvoice**.

## <a name="generate-fti-forms"></a>LFSF formų generavimas
LFSF formos ER sistemoje sugeneruojamos tokiu pačiu būdu, kaip ir SSRS ataskaitos.

Generuodami LFSF formas, sąskaitas faktūras galite pasirinkti pagal diapazoną arba pasirinkimą. 

![Sąskaitos faktūros pasirinkimas](media/FTIbyGER-InvoiceSelection.png)

![Sąskaitos faktūros peržiūra](media/FTIbyGER-InvoiceExcelPreview.png)

Naudojant ER formatus LFSF formoms spausdinti, kai taikomas šis būdas, naudojamos numatytosios ER failo paskirties vietos. Paskirties vietos keisti negalite. Daugiau informacijos, kaip konfigūruoti ER formatų ER paskirties vietas, ieškokite [Elektroninių ataskaitų paskirties vietos](electronic-reporting-destinations.md).

LFSF formas taip pat sugeneruoti galite LFSF registravimo metu, parinktį **Spausdinti SF** įjungę, o parinktį **Naudoti spausdinimo valdymo paskirties vietas** išjungę.

> [!NOTE]
> Naudojant ER formatus LFSF formoms spausdinti, kai taikomas šis būdas, naudojamos numatytosios ER failo paskirties vietos. Numatytąją paskirties vietą pakeisti galite vykdymo metu, jei paskirties vieta jau sukonfigūruota. Norėdami pakeisti paskirties vietą, turite turėti toliau nurodytą saugos teisę.
>
> - **Pavadinimas:** ERFormatDestinationRuntimeMaintain
> - **Žymė**: tvarkyti elektroninių ataskaitų formato paskirties vietą vykdymo aplinkoje

![Elektroninių ataskaitų paskirties vieta](media/FTIbyGER-ERFileDestinationSetting.png)

![Elektroninių ataskaitų formato paskirties vieta](media/FTIbyGER-ERFileDestinationUsage.png)

ER sistemoje šiuo metu palaikomos toliau nurodytos sugeneruotų dokumentų paskirties vietos.

- **Atsisiųstas failas** – sugeneruotos formos siūlomos kaip atsisiuntimai, kuriuos galite įrašyti naudodami naršyklę.
- **Ekranas** – sugeneruotoms LFSF formoms „Excel“ formatu peržiūrėti naudojama programa „Microsoft Office 365 Excel“.
- **„SharePoint“ aplankas** – sugeneruotos formos saugomos kaip nurodyta Dokumentų valdymo sistemos parametruose.
- **Programos archyvas** – sugeneruotos formos saugomos kaip vykdymo žurnalo įrašų priedai „Microsoft Azure“ saugykloje.
- **El. paštas** – sugeneruotos formos siunčiamos kaip el. laiškų priedai.

> [!NOTE]
> Tiesiai į spausdintuvą sugeneruotų LFSF formų siųsti negalite, nes spausdinimo tiesiogiai funkcija, naudojanti „Dynamics“ maršruto planavimo agentą, šiuo metu nepalaikoma.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Pavyzdinių ER konfigūracijų, skirtų spausdintinoms LFSF formos generuoti, atsisiuntimas
Pavyzdines ER konfigūracijas galite atsisiųsti ir naudoti kaip LFSF sprendimo šabloną. Konfigūracijos saugomos „Microsoft Dynamics Lifecycle Services“ (LCS) bendrai naudojamo turto bibliotekoje. Toliau nurodytos pateikiamos konfigūracijos.

- Konfigūracijoje **Kliento sąskaitų faktūrų išrašymas** pateikiamas būtinas duomenų modelis ir modelio susiejimas.
- Konfigūracijoje **Kliento LFSF ataskaita (GER)** pateikiamas formato pavyzdys.

> [!NOTE]
> Šios konfigūracijos sukurtos kaip pavyzdinės, siekiant padėti išsiaiškinti galimus scenarijus. Kas su šiomis konfigūracijomis bus daroma ateityje, priklauso vertinimo rezultatų ir gautų atsiliepimų.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Funkcijos, įdiegtos ER formato pavyzdyje
ER formato konfigūracijos pavyzdyje LFSF formoms sugeneruoti kaip šablonas naudojamas „Excel“ failas.

![Formato kūrimo įrankis](media/FTIbyGER-ERFormat.png)

Šiuo metu šiame ER formato pavyzdyje LFSF formoms sugeneruoti palaikomos toliau nurodytos formos.

- Sugeneruojamos tiek pradinių SF, kurios buvo užregistruotos, tiek ir pradinių SF, kurios nebuvo užregistruotos, LFSF formos. Pataisytos SF ir kredito pažymos nepalaikomos.
- LFSF formos sugeneruojamos sąskaitos faktūros kalba. Sugeneruotose formose naudojamas verčių ir datų formatas priklauso nuo vartotojo kliento vietos parametrų.
- Jei apdorojamose SF nėra eilučių, sugeneruotose SF rodomi pranešimai, susiję su duomenų nepasiekiamumu.
- Sugeneruotos sąskaitos faktūros antraštės priklauso nuo popieriaus formato, LFSF formai parinkto puslapyje **Gautinų sumų parametrai**. Įmonės informacija sugeneruotos sąskaitos faktūros formos antraštėje rodoma tik tada, jei nenurodytas popieriaus formatas.
- Sugeneruotose sąskaitų faktūrų formose įmonės numeris ir kliento neapmokestinamo PVM kodas rodomi tik pasirinkus atitinkamą LFSF formos, pateikiamos puslapyje **Gautinų sumų parametrai**, parinktį.
- Sugeneruotos sąskaitos faktūros eilutėse ir bendrųjų sumų sekcijose rodoma piniginė sąskaitos faktūros išraiška, pateikiama sąskaitos faktūros registracijos valiuta.
- Sugeneruotos sąskaitos faktūros bendrųjų sumų sekcijoje piniginė išraiška eurų valiuta ir sąskaitos faktūros registracijos valiuta gali būti rodoma, kai puslapyje **Gautinų sumų parametrai** įgalinama parinktis **Spausdinti sumą eurais**.
- Sugeneruotose sąskaitų faktūrų formose, priklausomai nuo puslapyje **Gautinų sumų parametrai** pasirinktų parametrų, rodomos pasiekiamos apdorojamos sąskaitos faktūros pastabos. Įtraukiamos visos sąskaitos faktūros ir atskiros sąskaitos faktūros eilutės pastabos.
- Sugeneruotose sąskaitų faktūrų formose įtraukiamos kliento LFSF formos ir su apdorojamos sąskaitos faktūros kalba susijusios pastabos, kai šios sukonfigūruojamos AR formos pastabų sąraše.
- Priklausomai nuo spausdinimo valdymo parametrų, tinkintas poraštės tektas sugeneruotose sąskaitose faktūrose įtraukiamas, kai sukonfigūruojama sąskaitos faktūros kalba, ER formatas ir LFSF dokumento apimtis.
- Sugeneruotų sąskaitų faktūrų formų bendrųjų sumų sekcijoje pateikiama pasiekiama mokėjimo nuolaidų informacija.
- Sugeneruotų sąskaitų faktūrų formų mokėjimo grafiko sekcijoje pateikiama pasiekiama mokėjimo grafiko informacija.
- Sugeneruotų sąskaitų faktūrų formų antkainio sekcijoje pateikiamos pasiekiamos papildomos išlaidos.
- Sugeneruotose sąskaitų faktūrų formose pateikiama PVM informacija, kuri priklauso nuo parametro **PVM specifikacija**, pateikiamo puslapyje **Gautinų sumų parametrai**. Šioje sekcijoje PVM informacija gali būti rodoma tik sąskaitos faktūros registracijos valiuta arba tuo pat metu sąskaitos faktūros registracijos valiuta ir įmonės apskaitos valiuta.
- Sugeneruotų sąskaitų faktūrų formose pateikiama tiesioginio debeto pranešimų informacija. Pavyzdžiui, rodoma, kada mokėjimo, turinčio privalomą tiesioginio debeto įgaliojimo ID, būdas parinktas sąskaitai faktūrai, kada apdorojama sąskaita faktūra registruota eurų valiuta bei kada apibrėžtas sąskaitai faktūrai skirtas tiesioginio debeto įgaliojimo ID.
- Sugeneruotose sąskaitose faktūrose rodoma pasiekiama registruotų sąskaitų faktūrų išankstinio apmokėjimo informacija.
- Sugeneruotas sąskaitų faktūrų formas SF klientui galima siųsti kaip el. laiško priedą. Naudojamam ER formatui reikia sukonfigūruoti atitinkamą ER paskirties vietos failą.

### <a name="countryregion-specific-features"></a>Šaliai / regionui būdingos priemonės 
Toliau nurodytos šaliai / regionui būdingos funkcijos į ER formato pavyzdį įtrauktos tam, kad būtų galima parodyti, kaip tam tikrus reikalavimus galima apdoroti ER konfigūracijose.

#### <a name="norway"></a>Norvegija
Įmonės registro terminas į sugeneruotos sąskaitos faktūros formą įtraukiamas tada, kai sąskaita faktūra apdorojama juridiniam subjektui, sukonfigūruotam toliau nurodytu būdu.

- Naudojamas Norvegijos šalies / regiono kontekstas.
- Parametras **Spausdinti Foretaksregisteret** yra aktyvus pardavimo dokumentuose.

#### <a name="spain"></a>Ispanija
Terminas **Specialusis apskaitos grynaisiais pinigais metodo režimas** į sugeneruotos sąskaitos faktūros formą įtraukiamas tada, kai sąskaita faktūra apdorojama juridiniam subjektui, sukonfigūruotam toliau nurodytu būdu.

- Naudojamas Ispanijos šalies / regiono kontekstas.
- Specialusis grynųjų pinigų apskaitos metodas įgalinamas sąskaitos faktūros apdorojimo dieną.

Kai pasiekiama mokėjimo nuolaidos informacija, pvz., mokėjimo nuolaidos suma ir SF eilutės grynoji suma, ji sugeneruotos SF formos bendrųjų sumų sekcijoje pateikiama tada, kai informacija apdorojama juridiniam subjektui, kuris sukonfigūruotas toliau nurodytu būdu.

- Naudojamas Ispanijos šalies / regiono kontekstas.
- Parinktis **SF taikoma mokėjimo nuolaida** įjungta sąskaitos faktūros parinktyje (**DK parametrai** \> **PVM sekcija**).

#### <a name="italy"></a>Italija
Kai sąskaita faktūra apdorojama juridiniam subjektui, kuris sukonfigūruotas naudojant Italijos šalies / regiono kontekstą, sugeneruotos sąskaitos faktūros SF eilutėse įtraukiama prekių nuolaidos žymė.

#### <a name="finland"></a>Suomija
Be to, galima sugeneruoti ne tik sąskaitos faktūros formą, bet ir žiro mokėjimo dokumentus, kaip nurodyta toliau.

- Juridiniam subjektui, kuriame naudojamas Suomijos šalies / regiono kontekstas, kuriame bent viena banko sąskaita pažymėta kaip **Žiro sąskaita** ir **Banko brūkšninis kodas**. 
- Sąskaitai faktūrai, pažymėtai kaip reikalaujama **Suomijos** susietame mokėjimo priede.

![Žiro kvitas](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> ER formato pavyzdys, sukonfigūruotas taip, kad žiro mokėjimo dokumentus būtų galima pasirinktinai sugeneruoti atskirame darbalapyje.

> [!NOTE]
> Kai sugeneruotos sąskaitos faktūros forma „Excel“ formatu bus peržiūrima, pirmiausia turėsite įdiegti šriftą, naudojamą brūkšniniam kodui vietiniame kompiuteryje sugeneruoti.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>ER formato pavyzdžio naudojimas el. pašto paskirties vietoms konfigūruoti
Norėdami sukonfigūruoti el. pašto paskirties vietas, naudokite toliau pateiktus ER formato pavyzdžio elementus.

- Kliento kontakto el. pašto adresą galima pasiekti naudojant šią ER išraišką: **model.InvoiceBase.Contact.ElectronicMail**.
- El. laiško temos tekstą galima pasiekti naudojant šią ER išraišką: **Emailing.TxtToUse.Subject**.
- El. laiško tekstą galima pasiekti naudojant šią ER išraišką: **Emailing.TxtToUse.Body**.

![Paskirties vietos parametrai](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Numatytasis el. laiško temos tekstas ir paties el. laiško tekstas apibrėžiamas kaip ER formato pavyzdys. Kalba priklauso nuo formato žymų. Šis numatytasis tekstas el. laiškuose bus naudojamas tada, jei nebus įtrauktas tinkintas organizacijos el. laiško šablonas, turintis iš anksto apibrėžtą **ERFTITMP** ID.

> [!NOTE]
> **ERFTITMP** el. laiško šablono ID apibrėžtas ER formato pavyzdyje. Jį pakeisti galima taip, kaip reikalaujama naujame ER formate, sukuriamame pagal šio formato pavyzdį.

Jei organizacijos el. laiško šablonas, turintis **ERFTITMP** ID, buvo įtrauktas į juridinį subjektą, kuriam skirtą SF apdorojate, el. laiškui sugeneruoti bus naudojamas el. laiško temos ir teksto šablonas. 

![Organizacijos el. laiškų šablonai](media/FTIbyGER-EmailTemplate.png)

![Nusiųsti el. laiško šabloną](media/FTIbyGER-EmailTemplateBody.png)

ER formato pavyzdžio ER išraiška **Emailing.TxtToUse.Subject** sukonfigūruojama, kad vietos rezervavimo ženklo %1 pasikartojimus būtų galima pakeisti apdorojamos sąskaitos faktūros ID.

Formato pavyzdžio išraiška **Emailing.TxtToUse.Body** sukonfigūruojama, siekiant pakeisti toliau nurodytus vietos rezervavimo ženklus.

- „%1“ pakeičiamas kliento kontaktinio asmens vardu ir pavarde.
- „%2“ pakeičiamas įmonės pavadinimu.
- „%3“ pakeičiamas kliento vardu ir pavarde.
- „%4“ pakeičiamas įmonės kliento kontaktinio asmens vardu ir pavarde.
- „%5“ pakeičiamas įmonės kliento kontaktinio asmens pareigomis.
- „%6“ pakeičiamas įmonės kontaktinio asmens el. pašto adresu.

![El. pašto adresas](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Papildomi ištekliai
[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

