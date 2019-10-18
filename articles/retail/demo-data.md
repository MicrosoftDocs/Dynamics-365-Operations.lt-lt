---
title: „Retail Modern POS“ MPOS ir „Cloud POS“ demonstracinių duomenų ekrano maketai
description: Šioje temoje pateikiama informacija apie ekrano maketus, kurie kartu su demonstraciniais duomenimis, nustatytais elektroniniam kasos aparate (EKA), įtraukti į „Dynamics 365 Retail“.
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 8c8d2fac82541b768f8e0a31049177bdc1262d44
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019329"
---
# <a name="demo-data-screen-layouts-in-retail-modern-pos-mpos-and-cloud-pos"></a>„Retail Modern POS“ MPOS ir „Cloud POS“ demonstracinių duomenų ekrano maketai

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama informacija apie ekrano maketus, kurie kartu su demonstraciniais duomenimis, nustatytais elektroniniam kasos aparate (EKA), įtraukti į „Dynamics 365 Retail“.

## <a name="overview"></a>Peržiūrėti

Pavyzdinio ekrano maketuose, įtrauktuose kartu su „Retail“ demonstraciniais duomenimis, pateikiamas turinys, optimizuotas įvairiems mažmeninės prekybos segmentams, parduotuvės darbuotojo vaidmenims ir įrenginiams. Viename makete gali būti keletas maketų dydžių ir mygtukynų kombinacijų, skirtų siekiant užtikrinti apimtį parduotuvės darbuotojams judant tarp įrenginių ir stočių. Šioje temoje aprašomi šių maketų skirtumai, teikiamos operacijos ir bendras jų naudojimas.

![Įvairių įrenginių demonstracinių duomenų maketai](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Ekrano maketo ID anatomija

Norėdami rasti ekrano maketų, eikite į **Mažmeninė prekyba** \> **Kanalo sąranka** \> **EKA sąranka** \> **EKA** \> **Ekrano maketai**.

![„Retail“ ekrano maketų puslapis](../retail/media/demo-screen-layouts-fig-2-1.png)

Ekrano maketo ID gali būti sudaryti iš ne daugiau nei 10 simbolių. ID yra eilutė, sudaryta iš trijų informacijos dalių, išdėstytų toliau nurodyta tvarka.

1. Įmonė
2. Maketo versija
3. Asmenys

### <a name="company"></a>Įmonė

| Laiškas | Įmonė         |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| M      | „Contoso“         |

### <a name="layout-version"></a>Maketo versija

| Versijos numeris | aprašymas                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Pagrindinė versija, kurioje palaikomi įvairių įrenginių kelių ekranų dydžiai ir proporcijos |
| 3.1            | Pagrindinė versija, kurioje teikiamas papildomas skydo **Rekomenduojami produktai** palaikymas        |

### <a name="persona"></a>Asmenys

| Santrumpa | Asmenys       | Turinys |
|--------------|---------------|----------|
| CSH          | Kasa       | Į kasos maketus įtraukti visi su operacija susiję veiksmai, pvz., klientų užsakymai, grąžinimai, nuolaidos, anuliavimai ir dovanų kortelės. Į šiuos maketus taip pat įtrauktos kasdienės atsargų valdymo užduotys, pvz., kainų patikros, atsargų peržvalgos ir inventorizacijos. Taip pat teikiamas pradinių sumų, pamainų sustabdymo ir laikrodžių pagrindinis pamainos valdymas. |
| MGR          | Parduotuvės vadovas | Parduotuvės vadovo maketuose įtraukti visi su operacija susiję veiksmai, pateikti kasos maketuose, kartu su mokesčių perrašymais. Į šiuos maketus taip pat įtrauktos kasdienės atsargų valdymo užduotys, pvz., kainų patikros, atsargų peržvalgos ir inventorizacijos. Pamainos valdymas taip pat teikiamas pradedant, sustabdant ir uždarant pamainas. Be to, į maketus įtraukti įrašų, išrašų, priemonių deklaravimo, seifo ir inkasavimo stalčiaus operacijos. Galiausiai į šiuos maketus įtraukta prieiga prie veiklos ataskaitų ir suteikiama galimybė atsispausdinti X ir Z ataskaitas. |
| STK          | Sandėliavimo tarnautojas   | Maketai Sandėliavimo tarnautojas optimizuoti atsargoms tvarkyti. Juose suteikiama prieiga prie kasdienių kainos patikros, atsargų peržvalgų, paėmimo ir gavimo, inventorizacijos ir rinkinio išskaidymo užduočių. Šiuose maketuose taip pat pateikiamos pagrindinės laikrodžio ir pamainų sustabdymo operacijos. Nors šie maketai daugiausia skirti tarnybinio biuro užduotims, sandėliavimo tarnautojams priskirtos tokios pačios operacijos kaip ir operacijos ekranų kasininkams. |

### <a name="example-layout"></a>Maketo pavyzdys

Toliau pateikiamas įmonės „Fabrikam“ ekrano maketo ID, 3 maketo versijos ir parduotuvės vadovo asmenų pavyzdys.

F3MGR

Toliau pateiktoje iliustracijoje pavaizduotas „Fabrikam“ parduotuvės vadovo ekrano Darbo pradžia pavyzdys.

![„Fabrikam“ parduotuvės vadovo ekranas Darbo pradžia](../retail/media/demo-screen-layouts-fig-2-2.png)

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
| Didelė        | 1440 × 960 | 3:2          | Planšetiniai kompiuteriai, didesni ekranai |

\* Šie papildomi maketų dydžiai pasiekiami tik „Adventure Works“ ir „Fabrikam“ maketuose.

> [!TIP]
> EKA automatiškai parenka maketo dydžius, pritaikydamas juos pagal labiausiai dabartinio programos lango proporcijas atitinkantį dydį. Norėdami rasti tuo metu naudojamą ekrano maketo ID ir maketo skiriamąją gebą, „Retail Modern POS“ MPOS arba „Retail Cloud POS“ (CPOS) atidarykite puslapį **Parametrai** ir ieškokite dalyje **Seanso informacija**. Taip pat galite matyti faktinę lango gebą, pritaikytą jūsų dabartinės programos arba naršyklės rėmeliui. Kai jau žinosite šią informaciją, maketo turinio šaltinį galėsite rasti apsilankę parinktyje **Kanalo nustatymas** \> **EKA sąranka** \> **EKA** \> **Ekrano maketai**.

![Ekrano maketai ir maketo gebos / dydžiai, pateikiami „Retail“ ir EKA](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Įmonės ir prekių ženklai

Kiekviena fiktyvi įmonė yra priskiriama atskiram mažmeninės prekybos segmentui ir apima produktų katalogus, suaktyvintus įmonės rinkoje. Kiekviena įmonė turi unikalų vaizdo prekės ženklą, pateikiamą kartu su produktais. Prekės ženklo elementai apima akcento spalvą, tamsią arba šviesią temą ir kartu pateikiamas nuotraukas, suteikiančias tikroviškumo.

### <a name="company-segment-and-visual-characteristics"></a>Įmonės segmentas ir vaizdo charakteristikos

| Įmonė         | Buvimo vieta | Segmentas        | Pabrėžti | Tema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Sietlas  | Sporto prekės | Mėlyna   | Tamsu  |
| Fabrikam        | Hiustonas  | Madingos prekės        | Žalia  | Light |
| „Contoso“         | Bostonas   | Elektronika    | Raudona    | Tamsu  |

> [!NOTE]
> „Adventure Works“ ir „Fabrikam“ yra du pagrindiniai prekių ženklai. „Contoso“ yra pasiekiamas, bet pateikti ne visi maketai.

Toliau pateiktose iliustracijose pavaizduoti trijų fiktyvių įmonių darbo pradžios puslapio ir operacijos puslapio pavyzdžiai.

### <a name="adventure-works"></a>Adventure Works

![„Adventure Works“ darbo pradžios puslapio demonstraciniai duomenys](../retail/media/demo-screen-layouts-fig-4-1a.png)

![„Adventure Works“ operacijos puslapio demonstraciniai duomenys](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![„Fabrikam“ darbo pradžios puslapio demonstraciniai duomenys](../retail/media/demo-screen-layouts-fig-4-2a.png)

![„Fabrikam“ operacijos puslapio demonstraciniai duomenys](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>„Contoso“

![„Contoso“ demonstraciniai duomenų maketai](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Vartotojo prisijungimo matrica

Vartotojams pateikiami įvairūs ekrano maketai. Naudodamiesi toliau pateikta lentele, turėtumėte pasiekti bet kurį iš ekranų. Tiesiog prisijunkite naudodami atitinkamą operatoriaus ID.

| Įmonė         | Ekrano maketo ID | Asmenys       | Operatoriaus ID           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | Parduotuvės vadovas | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kasa       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Sandėliavimo tarnautojas   | 000155, 000181, 000152 |
| Fabrikam        | F3MGR            | Parduotuvės vadovas | 000160, 000168, 000163 |
| Fabrikam        | F3CSH            | Kasa       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Sandėliavimo tarnautojas   | 000164, 000112, 000123 |
| „Contoso“         | C3MGR            | Parduotuvės vadovas | 000100, 000111         |
| „Contoso“         | C3CSH            | Kasa       | 000110, 000120         |
| „Contoso“         | Netaikoma   | Sandėliavimo tarnautojas   | Netaikoma         |

> [!TIP]
> Norėdami geriausių rezultatų, aparatą suaktyvinkite atitinkamoje parduotuvės vietoje ir asmenų, kuriuos planuojate naudoti prisijungę, įmonei nustatykite įmonę. Tokiu būdu padėsite užtikrinti, kad vaizdo profilis ir prekės ženklo vaizdai bus sulygiuoti. Pavyzdžiui, norėdami pamatyti „Fabrikam“ kasininko maketą, kasos aparatą turėtumėte suaktyvinti Hiustone esančioje parduotuvėje.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
