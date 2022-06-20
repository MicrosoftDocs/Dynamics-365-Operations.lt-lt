---
title: „Modern POS“ (MPOS) ir „Cloud POS“ demonstracinių duomenų ekrano maketai
description: Šiame straipsnyje pateikiama informacija apie ekrano maketus, kurie įtraukti į demonstracinių duomenų rinkinį, nustatytą pardavimo galimybių (EKA) patirtį Dynamics 365 Commerce.
author: josaw1
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: eb7a288b61e8b467dd8ad6a8f7dc42b7fca0d943
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897230"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>„Modern POS“ (MPOS) ir „Cloud POS“ demonstracinių duomenų ekrano maketai

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie ekrano maketus, kurie įtraukti į demonstracinių duomenų rinkinį, nustatytą pardavimo galimybių (EKA) patirtį Dynamics 365 Commerce.

## <a name="overview"></a>Peržiūrėti

Pavyzdinio ekrano maketuose, įtrauktuose kartu su „Commerce“ demonstraciniais duomenimis, pateikiamas turinys, optimizuotas įvairiems mažmeninės prekybos segmentams, parduotuvės darbuotojų vaidmenims ir įrenginiams. Viename makete gali būti keletas maketų dydžių ir mygtukynų kombinacijų, skirtų siekiant užtikrinti apimtį parduotuvės darbuotojams judant tarp įrenginių ir stočių. Šiame straipsnyje aprašomi skirtumai tarp šių maketų, jų atliekamos operacijos ir bendra jų pristatoma patirtis.

![Įvairių įrenginių demonstracinių duomenų maketai.](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Ekrano maketo ID anatomija

Norėdami rasti ekrano maketų, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo sąranka** \> **EKA sąranka** \> **EKA** \> **Ekrano maketai**.

![Ekrano maketų puslapis.](../commerce/media/demo-screen-layouts-fig-2-1.png)

Ekrano maketo ID gali būti sudaryti iš ne daugiau nei 10 simbolių. ID yra eilutė, sudaryta iš trijų informacijos dalių, išdėstytų toliau nurodyta tvarka.

1. Įmonė
2. Maketo versija
3. Asmenys

### <a name="company"></a>Įmonė

| Laiškas | Įmonė         |
|--------|-----------------|
| A      | „Adventure Works” |
| F      | „Fabrikam”        |
| C      | „Contoso“         |

### <a name="layout-version"></a>Maketo versija

| Versijos numeris | aprašymas                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Pagrindinė versija, kurioje palaikomi įvairių įrenginių kelių ekranų dydžiai ir proporcijos |
| 3.1            | Pagrindinė versija, kurioje teikiamas papildomas skydo **Rekomenduojami produktai** palaikymas        |
| 4              | Išplėsta versija išplėstam „Fabrikam“ atnaujintam išdėstymui                                  |

### <a name="persona"></a>Asmenys

| Santrumpa | Asmenys       | Turinys |
|--------------|---------------|----------|
| CSH          | Kasa       | Į kasos maketus įtraukti visi su operacija susiję veiksmai, pvz., klientų užsakymai, grąžinimai, nuolaidos, anuliavimai ir dovanų kortelės. Į šiuos maketus taip pat įtrauktos kasdienės atsargų valdymo užduotys, pvz., kainų patikros, atsargų peržvalgos ir inventorizacijos. Taip pat teikiamas pradinių sumų, pamainų sustabdymo ir laikrodžių pagrindinis pamainos valdymas. |
| MGR          | Parduotuvės vadovas | Parduotuvės vadovo maketuose įtraukti visi su operacija susiję veiksmai, pateikti kasos maketuose, kartu su mokesčių perrašymais. Į šiuos maketus taip pat įtrauktos kasdienės atsargų valdymo užduotys, pvz., kainų patikros, atsargų peržvalgos ir inventorizacijos. Pamainos valdymas taip pat teikiamas pradedant, sustabdant ir uždarant pamainas. Be to, į maketus įtraukti įrašų, išrašų, priemonių deklaravimo, seifo ir inkasavimo stalčiaus operacijos. Galiausiai į šiuos maketus įtraukta prieiga prie veiklos ataskaitų ir suteikiama galimybė atsispausdinti X ir Z ataskaitas. |
| STK          | Sandėliavimo tarnautojas   | Maketai Sandėliavimo tarnautojas optimizuoti atsargoms tvarkyti. Juose suteikiama prieiga prie kasdienių kainos patikros, atsargų peržvalgų, paėmimo ir gavimo, inventorizacijos ir rinkinio išskaidymo užduočių. Šiuose maketuose taip pat pateikiamos pagrindinės laikrodžio ir pamainų sustabdymo operacijos. Nors šie maketai daugiausia skirti tarnybinio biuro užduotims, sandėliavimo tarnautojams priskirtos tokios pačios operacijos kaip ir operacijos ekranų kasininkams. |

### <a name="example-layout"></a>Maketo pavyzdys

Toliau pateikiamas įmonės „Fabrikam“ ekrano maketo ID, 4 maketo versijos ir parduotuvės vadovo asmenų pavyzdys.

F4MGR

Toliau pateiktoje iliustracijoje pavaizduotas „Fabrikam“ parduotuvės vadovo ekrano Darbo pradžia pavyzdys.

![„Fabrikam“ parduotuvės vadovo ekranas Darbo pradžia.](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Maketo dydžiai

### <a name="full-vs-compact-layouts"></a>Visos versijos įrenginių maketai palyginti su kompaktinių įrenginių versijų maketais

Ekrano makete gali būti konfigūracijų, skirtų visoms ir kompaktinėms įrenginių versijoms. Todėl vartotojui gali būti priskirtas vienas ekrano maketas, kuris veiks su įvairiais parduotuvėje esančiais dydžiais ir formos veiksniais.

- **Modernus EKA – pilnas** – paprastai pilni išdėstymai geriausiai tinka didesniems ekranams, pavyzdžiui, stalinių kompiuterių monitoriams arba planšetiniams kompiuteriams. Vartotojai gali pasirinkti vartotojo sąsajos elementus, pateikiamus makete, nurodyti tų elementų dydį bei išdėstymą ir konfigūruoti tikslias ypatybes. Pasirinkus pilnus išdėstymus palaikomos vertikalios ir horizontalios konfigūracijos.
- **Modernus EKA – kompaktinis** – paprastai kompaktiniai maketai naudojami telefonams arba nedideliems planšetiniams kompiuteriams. Kompaktinių įrenginių dizaino galimybės ribotos. Vartotojai gali sukonfigūruoti kvito ir bendrųjų sumų sričių stulpelius ir laukus.

### <a name="screen-resolutions-that-are-provided"></a>Teikiamos ekrano skiriamosios gebos

Toliau pateiktoje lentelėje nurodyti įprasto ekrano skiriamosios gebos maketo dydžiai.

| Maketo tipas | Nutarimas | Proporcijos | Paskirties vietos ekranas          |
|-------------|------------|--------------|-------------------------|
| Glaudinti\*   | 480 × 853  | 16:9         | Telefonai                  |
| Didelė        | 1024 × 768 | 4:3          | Planšetiniai kompiuteriai                 |
| Didelė\*      | 1280 × 720 | 16:9         | Planšetiniai kompiuteriai                 |
| Didelė        | 1366 × 768 | 16:9         | Planšetiniai kompiuteriai, didesni ekranai |
| Pilnas        | 1440 × 960 | 3:2          | Planšetiniai kompiuteriai, didesni ekranai |
| Pilnas\*      | 1536 × 864 | 16:9         | Planšetiniai kompiuteriai, didesni ekranai |

\* Šie papildomi maketų dydžiai pasiekiami tik „Adventure Works“ ir „Fabrikam“ maketuose.

> [!TIP]
> EKA automatiškai parenka maketo dydžius, pritaikydamas juos pagal labiausiai dabartinio programos lango proporcijas atitinkantį dydį. Norėdami rasti tuo metu naudojamą ekrano maketo ID ir maketo skiriamąją gebą, „Modern POS“ (MPOS) arba „Retail Cloud POS“ (CPOS) atidarykite puslapį **Parametrai** ir ieškokite dalyje **Seanso informacija**. Taip pat galite matyti faktinę lango gebą, pritaikytą jūsų dabartinės programos arba naršyklės rėmeliui. Kai jau žinosite šią informaciją, maketo turinio šaltinį galėsite rasti apsilankę parinktyje **Kanalo nustatymas** \> **EKA sąranka** \> **EKA** \> **Ekrano maketai**.

![Ekrano maketai ir maketo gebos / dydžiai, pateikiami „Commerce“ ir EKA.](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Įmonės ir prekių ženklai

Kiekviena fiktyvi įmonė yra priskiriama atskiram mažmeninės prekybos segmentui ir apima produktų katalogus, suaktyvintus įmonės rinkoje. Kiekviena įmonė turi unikalų vaizdo prekės ženklą, pateikiamą kartu su produktais. Prekės ženklo elementai apima akcento spalvą, tamsią arba šviesią temą ir kartu pateikiamas nuotraukas, suteikiančias tikroviškumo.

### <a name="company-segment-and-visual-characteristics"></a>Įmonės segmentas ir vaizdo charakteristikos

| Įmonė         | Buvimo vieta | Segmentas        | Pabrėžti | Tema |
|-----------------|----------|----------------|--------|-------|
| „Adventure Works” | Sietlas  | Sporto prekės | Mėlyna   | Tamsus  |
| „Fabrikam“        | San Franciskas  | Madingos prekės        | Žalia  | Šviesus |
| „Contoso“         | Bostonas   | Elektronika    | Raudona    | Tamsus  |

> [!NOTE]
> „Adventure Works“ ir „Fabrikam“ yra du pagrindiniai prekių ženklai. „Contoso“ yra pasiekiamas, bet pateikti ne visi maketai.

Toliau pateiktose iliustracijose pavaizduoti trijų fiktyvių įmonių darbo pradžios puslapio ir operacijos puslapio pavyzdžiai.

### <a name="adventure-works"></a>„Adventure Works“

![„Adventure Works“ darbo pradžios puslapio demonstraciniai duomenys.](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![„Adventure Works“ operacijos puslapio demonstraciniai duomenys.](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![„Fabrikam“ darbo pradžios puslapio demonstraciniai duomenys.](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![„Fabrikam“ operacijos puslapio demonstraciniai duomenys.](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>„Contoso“

!["Contoso" demonstraciniai duomenų maketai.](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Vartotojo prisijungimo matrica

Vartotojams pateikiami įvairūs ekrano maketai. Naudodamiesi toliau pateikta lentele, turėtumėte pasiekti bet kurį iš ekranų. Tiesiog prisijunkite naudodami atitinkamą operatoriaus ID.

| Įmonė         | Ekrano maketo ID | Asmenys       | Operatoriaus ID           |
|-----------------|------------------|---------------|------------------------|
| „Adventure Works” | A3MGR            | Parduotuvės vadovas | 000154, 000137, 000073 |
| „Adventure Works” | A3CSH            | Kasa       | 000150, 000175, 000165 |
| „Adventure Works” | A3STK            | Sandėliavimo tarnautojas   | 000155, 000181, 000152 |
| „Fabrikam“        | F4MGR            | Parduotuvės vadovas | 000160, 000713         |
| „Fabrikam“        | F3CSH            | Kasa       | 000161, 000113, 000114 |
| „Fabrikam“        | F3STK            | Sandėliavimo tarnautojas   | 000164, 000112, 000123 |
| „Contoso“         | C3MGR            | Parduotuvės vadovas | 000100, 000111         |
| „Contoso“         | C3CSH            | Kasa       | 000110, 000120         |
| „Contoso“         | Netaikoma   | Sandėliavimo tarnautojas   | Netaikoma         |

> [!TIP]
> Norėdami geriausių rezultatų, aparatą suaktyvinkite atitinkamoje parduotuvės vietoje ir asmenų, kuriuos planuojate naudoti prisijungę, įmonei nustatykite įmonę. Tokiu būdu padėsite užtikrinti, kad vaizdo profilis ir prekės ženklo vaizdai bus sulygiuoti. Pavyzdžiui, norėdami pamatyti „Fabrikam“ kasininko maketą, kasos aparatą turėtumėte suaktyvinti Hiustone esančioje parduotuvėje.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce.](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->


[!INCLUDE[footer-include](../includes/footer-banner.md)]