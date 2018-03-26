---
title: "Atributai, atributų grupės ir jų susiejimai su įvairiais „Retail“ objektais sprendime „Finance and Operations“"
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 6fde46c35d5efbb72ad97628d7d5a3f9eeba7c8e
ms.contentlocale: lt-lt
ms.lasthandoff: 03/13/2018

---

# <a name="attributes-attribute-groups-and-their-associations-with-various-retail-entities-in-finance-and-operations"></a>Atributai, atributų grupės ir jų susiejimai su įvairiais „Retail“ objektais sprendime „Finance and Operations“

[!include[banner](includes/banner.md)]

*Atributai* yra būdas išsamiau apibūdinti produktą ir jo charakteristikas naudojant vartotojų apibrėžtus laukus (pvz., **Atminties dydis**, **Kietojo disko talpa**, **Atitinka „Energy Star“ reikalavimus** ir t. t.). Sprendime „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ atributus galima susieti su įvairiais „Retail“ objektais, pvz., produktų kategorijomis ir mažmeninės prekybos kanalais, bei galima nustatyti numatytąsias jų reikšmes. Tada produktai paveldi atributus ir numatytąsias reikšmes, kai jie susiejami su produktų kategorijomis ar mažmeninės prekybos kanalais. Numatytųjų reikšmių galima nepaisyti atskiro produkto lygiu, mažmeninės prekybos kanalo lygiu arba mažmeninės prekybos kataloge.
 
Pavyzdžiui, įprastas televizijos produktas gali turėti tolesnius atributus.

| Kategorija   | Atributas                | Leistinos reikšmės          | Numatytoji vertė |
|------------|--------------------------|-----------------------------|---------------|
| TV ir vaizdo įrašai | Rūšis                    | Bet kuri tinkama prekės ženklo reikšmė       | None          |
| TV         | Ekrano dydis              | 20–80 colių                | None          |
|            | Vertikali skiriamoji geba      | 480 i, 720 p, 1080 i arba 1080 p | 1080 p         |
|            | Ekrano naujinimo dažnis      | 60 hz, 120 hz arba 240 hz       | 60 hz          |
|            | HDMI įvestys              | 0–10                        | 3             |
|            | DVI įvestys               | 0–10                        | 1             |
|            | Sudėtinės įvestys         | 0–10                        | 2             |
|            | Komponento įvestys         | 0–10                        | 1             |
| LCD        | 3D parengta                 | Taip arba Ne                   | Taip           |
|            | 3D įgalinta               | Taip arba Ne                   | Nr.            |
| Plazminis     | Veiklos šablonas nuo      | 32–110 laipsnių              | 32            |
|            | Veiklos šablonas iki        | 32–110 laipsnių              | 100           |
| Projekcinis | Projekcijos vamzdelio garantija | 6, 12 arba 18 mėnesiai (-ių)         | 12            |
|            | Projekcijos vamzdelių skaičius    | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Atributai ir atributų tipai

Atributai pagrįsti *atributų tipais*. Atributo tipas identifikuoja duomenų, kuriuos galima įvesti konkrečiam atributui, tipą. „Finance and Operations“ šiuo metu palaiko tolesnius atributų tipus.

- **Valiuta** – šis tipas palaiko valiutos reikšmę. Jis gali būti apribotas (t. y., jis gali palaikyti reikšmių intervalą) arba jis gali būti neapibrėžtas.
- **Data ir laikas** – šis tipas palaiko datos ir laiko reikšmę. Jį galima apibrėžti arba palikti neapibrėžtą.
- **Dešimtainis skaičius** – šis tipas palaiko skaitinę reikšmę su skaitmenimis po kablelio. Jis taip pat palaiko matavimo vienetą. Jį galima apibrėžti arba palikti neapibrėžtą.
- **Sveikasis skaičius** – šis tipas palaiko skaitinę reikšmę. Jis taip pat palaiko matavimo vienetą. Jį galima apibrėžti arba palikti neapibrėžtą.
- **Tekstas** – šis tipas palaiko teksto reikšmę. Jis taip pat palaiko iš anksto apibrėžtąjį galimų reikšmių rinkinį (tai yra, *išvardijimą*).
- **Bulio logika** – šis tipas palaiko dvejetainę reikšmę (**true** arba **false**).
- **Nuoroda** – šis tipas nurodo į kitus atributus.

### <a name="set-up-attribute-types-in-finance-and-operations"></a>Atributų tipų nustatymas sprendime „Finance and Operations“

1. Prisijunkite prie „Finance and Operations“ tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Produktų informacijos valdymas** &gt; **Sąranka** &gt; **Kategorijos ir atributai** &gt; **Atributų tipai**.
3. Sukurkite du tipo **Tekstas** atributų tipus, parinktį **Fiksuotas sąrašas** nustatykite kaip **Taip** ir įtraukite tolesnį reikšmių sąrašą.

    - Vieną atributų tipą pavadinkite **Lęšio forma** ir įtraukite šias reikšmes: **Ovalas**, **Kvadratas** ir **Stačiakampis**.
    - Kitą atributų tipą pavadinkite **Akinių nuo saulės prekės ženklas** ir įtraukite šias reikšmes: **„Ray ban“**, **„Aviator“** ir **„Oakley“**.

![Atributų tipai](media/AttributeType.png)

### <a name="set-up-an-attribute-in-finance-and-operations"></a>Atributo nustatymas sprendime „Finance and Operations“

1. Prisijunkite prie tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Produktų informacijos valdymas** &gt; **Sąranka** &gt; **Kategorijos ir atributai** &gt; **Atributai**.
3. Sukurkite atributą pavadinimu **Lęšis**.
4. Lauką **Atributo tipas** nustatykite kaip **Lęšio forma**.

![Atributai](media/Attribute.png)

## <a name="attribute-metadata"></a>Atributo metaduomenys

*Atributų metaduomenys* leidžia pasirinkti parinktis, kad galėtumėte nurodyti, kaip turėtų veikti kiekvieno produkto atributai. Pavyzdžiui, galite nurodyti, ar atributai reikalingi, ar juos galima naudoti ieškant ir ar juos galima naudoti kaip filtrą.

Mažmeninės prekybos produktų atributų metaduomenų parametrų galima nepaisyti kanalo lygiu. Ši galimybė bus aptarta toliau šioje temoje.

Galbūt pastebėjote, kad puslapyje **Atributai** pateiktos parinktys, susijusios su atributų metaduomenimis. Dalyje **EKA atributų metaduomenys** esanti parinktis **Galima patikslinti** turi įtakos atributų reikšmių veikimui mažmeninės prekybos elektroniniame kasos aparate (EKA) arba tam, kaip sistema tas atributų reikšmes apdoroja. Mažmeninės prekybos el. kasos aparate bus rodomi tik tie tikslintini ar filtruotini atributai, kuriems parinktį **Galima patikslinti** galite nustatyti kaip **Taip**.

Toliau pateiktos likusios puslapyje **Atributai** esančios atributų metaduomenų parinktys.

- Galimas ieškoti
- Atgaunamas
- Galima užklausti
- Galimas rikiuoti
- Leisti kelias vertes
- Nepaisyti atvejo ir formato
- Visiška atitiktis

Šios parinktys iš pradžių buvo skirtos pagerinti internetinės parduotuvės ieškos funkcijas. Nors į „Finance and Operations“ internetinė parduotuvė iš karto nėra įtraukta, į sprendimą įtrauktas el. komercijos publikavimo programinės įrangos kūrimo rinkinys (SDK). Naudodami šį SDK klientai produktus gali įtraukti į pasirinktą ieškos indeksą. Nors produktų duomenys importuojami, klientai vis tiek turėtų galėti atskirti ieškotinus duomenis, duomenis, dėl kurių galima teikti užklausas, ir t. t. Taip jie gali sukurti optimalų indeksą ir užtikrinti, kad būtų indeksuojami tik tie atributai, kurie, *jų nuomone*, turi būti suindeksuoti.

Norėdami gauti informacijos apie šių likusių parinkčių paskirtį, žr. [„SharePoint Server 2013“ ieškos schemos apžvalga](https://technet.microsoft.com/en-us/library/jj219669.aspx).

## <a name="filter-settings-for-attributes"></a>Atributų filtrų parametrai

Atributų filtrų parametrai leidžia apibrėžti, kaip atributų filtrai rodomi mažmeninės prekybos el. kasos aparate. Norėdami pasiekti kokio nors atributo filtrų parametrus, „Finance and Operations“ puslapyje **Atributai** pasirinkite tą atributą ir veiksmų srityje pasirinkite **Filtrų parametrai**.

Puslapyje **Filtrų rodymo nuostatos** pateikti tolesni laukai.

- **Pavadinimas** – pagal numatytuosius parametrus šis laukas yra nustatytas kaip atributo pavadinimas. Tačiau reikšmę galite keisti.
- **Rodymo parinktis** – galimos tolesnės parinktys.

    - **Viena reikšmė** – šią parinktį galima naudoti su šių tipų atributais: **Bulio logika**, **Valiuta**, **Dešimtainis skaičius**, **Sveikasis skaičius** ir **Tekstas**. Ši parinktis leidžia kliente tikslinti pasirinkti vieną šių atributų reikšmę.
    - **Kelios reikšmės** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius**, **Sveikasis skaičius** ir **Tekstas**. Ši parinktis leidžia kliente tikslinti pasirinkti kelias šio atributo reikšmes.

- **Rodymo valdiklis** – galimos tolesnės parinktys.

    - **Sąrašas** – šią parinktį galima naudoti su visų tipų atributais.
    - **Intervalas** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius** ir **Sveikasis skaičius**. 
    - **Slankiklis** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius** ir **Sveikasis skaičius**.
    - **Slankiklis su juostomis** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius** ir **Sveikasis skaičius**.

- **Ribinė reikšmė** – šis parametras reikalingas, jei kaip rodymo valdiklio tipą pasirinkote **Intervalas**. Apibrėžti reikšmes galite kaip skyriklį naudodami kabliataškį (;).

    Pavyzdžiui, tokio filtro kaip **Maišelio tūris** ribinė reikšmė gali būti **10; 20; 50; 100; 200; 500; 1000; 5000**. Tokiu atveju mažmeninės prekybos el. kasos aparate bus rodomi tolesni intervalai. Visi intervalai, kurių rezultatų rinkinyje nebus produktų, bus rodomi blankiau.

    - Mažiau nei 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 ar daugiau

![Atributų filtrų parametrai](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Atributų grupės

Atributus apibrėžus, juos galima priskirti atributų grupėms. *Atributų grupė* naudojama grupuojant atskirus komponento arba pakomponenčio atributus produktų konfigūracijos modelyje. Atributą galima įtraukti į daugiau nei vieną atributų grupę. Atributų grupės vartotojams gali padėti konfigūruoti produktus, nes įvairios pasirinktys išdėstomos konkrečiame kontekste. Atributų grupes galima priskirti mažmeninės prekybos kategorijoms arba mažmeninės prekybos kanalams.

Taip pat galite nustatyti į atributų grupę įtrauktų atributų numatytąsias reikšmes. Pavyzdžiui, į atributų grupę įtraukiate spalvos atributą ir kaip numatytąją atributo reikšmę pasirenkate **Mėlyna**. Tokiu atveju, kai atributų grupė įtraukiama į mažmeninės prekybos produktą, kurio vienas iš atributų yra spalva, kaip numatytoji to produkto spalva rodoma **Mėlyna**.

![Atributų grupės](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Atributų grupės kūrimas

1. Prisijunkite prie tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Produktų informacijos valdymas** &gt; **Sąranka** &gt; **Kategorijos ir atributai** &gt; **Atributų grupės**.
3. Sukurkite atributų grupę pavadinimu **Madingi akiniai nuo saulės**.
4. Įtraukite šiuos atributus: **Lęšio forma** ir **Akinių nuo saulės prekės ženklas**.

### <a name="assign-attribute-groups-to-retail-categories"></a>Atributų grupių priskyrimas mažmeninės prekybos kategorijoms

Šių tipų mažmeninės prekybos kategorijų hierarchijose – Mažmeninės prekybos produktų hierarchija, Kanalo naršymo kategorijų hierarchija ir Papildomų produktų kategorijų hierarchija – su kategorijų mazgais galima susieti vieną ar kelias atributų grupes. Produktus suskirsčius į kategorijas, jie paveldi atributus, įtrauktus į atributų grupes.

![Mažmeninės prekybos produktų hierarchija – produktų atributų grupės](media/AGRetailProdHierarchy.PNG)

Norėdami atributų grupes priskirti mažmeninės prekybos produktų hierarchijos kategorijoms, atlikite tolesnius veiksmus.

1. Prisijunkite prie tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Mažmeninė prekyba** &gt; **Kategorijų ir produktų valdymas** &gt; **Mažmeninės prekybos produktų hierarchija**.
3. Pasirinkite **Madingų prekių naršymo hierarchija**.
4. Dalyje **Vyriški drabužiai** pasirinkite kategoriją **Kelnės**, tada „FastTab“ skirtuke **Produktų atributų grupės** įtraukite atributų grupę pavadinimu **Vyriškas diržas**.
5. Pasirinkite kategoriją **Madingi akiniai nuo saulės** ir patikrinkite naujus atributų grupės **Madingi akiniai nuo saulės** atributus pasirinkdami **Peržiūrėti atributus**.

    Atributų grupėje turi būti rodomi nauji atributai **Lęšio forma** ir **Akinių nuo saulės prekės ženklas**.

6. Dalyje **Vyriški drabužiai** pasirinkite kategoriją **Kelnės** ir patikrinkite atributų grupės **Vyriškas diržas** atributus pasirinkdami **Peržiūrėti atributus**.

    Atributų grupėje turi būti rodomi atributai **Vyriško diržo prekės ženklas**, **Diržo medžiaga** ir **Diržo dydis**.

> [!NOTE]
> Naudojant šią procedūrą, atributų grupes taip pat galima priskirti kanalo naršymo kategorijų hierarchijos ir papildomų produktų kategorijų hierarchijos kategorijoms. Atlikdami 2 veiksmą, naudokite tolesnius naršymo kelius.
>
> - **Mažmeninė prekyba** &gt; **Kategorijų ir produktų valdymas** &gt; **Kanalo naršymo kategorijos**
> - **Mažmeninė prekyba** &gt; **Kategorijų ir produktų valdymas** &gt; **Papildomų produktų kategorijos**

### <a name="assign-attribute-groups-to-retail-stores"></a>Atributų grupių priskyrimas mažmeninės prekybos parduotuvėms

Vieną ar kelias atributų grupes galima susieti su viena ar keliomis mažmeninės prekybos parduotuvių hierarchijos mažmeninės prekybos parduotuvėmis. Tada, produktais papildžius konkrečias mažmeninės prekybos parduotuves, jie paveldi atributus, įtrauktus į atributų grupes.

1. Prisijunkite prie tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Mažmeninė prekyba** &gt; **Kanalo sąranka** &gt; **Kanalo kategorijos ir produktų atributai**.
3. Atributų grupes priskirkite kanalui „Houston“.

    1. Pasirinkite kanalą **„Houston“**.
    2. „FastTab“ skirtuke **Atributų grupė** pasirinkite **Įtraukti**, tada lauke **Pavadinimas** pasirinkite **SharePointProvisionedProductAttributeGroup**.
    3. Dar kartą pasirinkite **Įtraukti**, tada lauke **Pavadinimas** pasirinkite **Vyriškas diržas**.
    4. Dar kartą pasirinkite **Įtraukti**, tada lauke **Pavadinimas** pasirinkite **Madingi akiniai nuo saulės**.

        > [!NOTE]
        > Parinktis leidžia nurodyti, kad šis kanalas atributų grupes turi paveldėti iš pirminio hierarchijos kanalo. Jei parinktį **Paveldėti** nustatote kaip **Taip**, antrinis kanalo mazgas paveldi visas atributų grupes ir visus tų atributų grupių atributus.

4. Įjunkite atributus, kad jie būtų prieinami kanale „Houston“.

    1. Veiksmų srityje pasirinkite **Nustatyti atributų metaduomenis**.
    2. Pasirinkite kategorijos mazgą **Madingos prekės**, tada „FastTab“ skirtuke **Kanalo produktų atributai** kiekvienam atributui parinkite **Įtraukti atributą**.
    3. Pasirinkite kategorijos mazgą **Madingi priedai**, pasirinkite kategoriją **Madingi akiniai nuo saulės**, tada „FastTab“ skirtuke **Kanalo produktų atributai** kiekvienam atributui parinkite **Įtraukti atributą**.
    4. Pasirinkite kategorijos mazgą **Vyriški drabužiai**, pasirinkite kategoriją **Kelnės**, tada „FastTab“ skirtuke **Kanalo produktų atributai** kiekvienam atributui parinkite **Įtraukti atributą**.

![Kanalų kategorijos ir produktų atributai – atributų grupės](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Atributo reikšmių nepaisymas

Atskirų produktų atributų numatytųjų reikšmių galima nepaisyti produkto lygiu. Atskirų produktų numatytųjų reikšmių taip pat galima nepaisyti konkrečiuose kataloguose, skirtuose konkretiems mažmeninės prekybos kanalams.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Atskiro produkto atributų reikšmių nepaisymas

1. Prisijunkite prie tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Mažmeninė prekyba** &gt; **Kategorijų ir produktų valdymas** &gt; **Išleisti produktai pagal kategoriją**.
3. Pasirinkite kategorijos mazgą **Madingos prekės** &gt; **Madingi priedai** &gt; **Madingi akiniai nuo saulės**.
4. Tinklelyje pasirinkite reikiamą produktą. Tada veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Produktų atributai**.
5. Pasirinkite atributą kairiojoje srityje, tada atnaujinkite jo reikšmę dešiniojoje srityje.

![Išsamios produktų informacijos puslapis – produktų atributų grupės](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Katalogo produktų atributų reikšmių nepaisymas

1. Prisijunkite prie tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Mažmeninė prekyba** &gt; **Katalogų valdymas** &gt; **Visi katalogai**.
3. Pasirinkite katalogą **„Fabrikam“ pagrindinis katalogas**.
4. Pasirinkite kategorijos mazgą **Madingos prekės** &gt; **Madingi priedai** &gt; **Madingi akiniai nuo saulės**.
5. „FastTab“ skirtuke **Produktai** pasirinkite reikiamą produktą, tada virš produktų tinklelio pasirinkite **Atributai**.
6. Tolesniuose „FastTab“ atnaujinkite reikiamų atributų reikšmes.

    - Bendrinami produktų publikavimo kanalai
    - Bendrai naudojami produkto atributai
    - Publikavimo kanalas
    - Kanalo produkto atributai

    > [!NOTE]
    > Jei sprendime „Finance and Operations“ sukuriama bendrai naudojama produktų medija ir bendrai naudojami produktų atributai, jie taikomi visiems mažmeninės prekybos produktams.

![Katalogų produktų atributų grupės](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Kanalo produktų atributų reikšmių nepaisymas

1. Prisijunkite prie tarnybinio biuro kliento kaip mažmeninės prekybos reklamavimo parduotuvėje vadovas.
2. Eikite į **Mažmeninė prekyba** &gt; **Kanalo sąranka** &gt; **Kanalo kategorijos ir produktų atributai**.
3. Pasirinkite kanalą **„Houston“**.
4. „FastTab“ skirtuke **Produktai** pasirinkite reikiamą produktą, tada virš produktų tinklelio pasirinkite **Atributai**.

    > [!NOTE]
    > Jei produktų nėra, jų įtraukite „FastTab“ skirtuke **Produktai** pasirinkdami **Įtraukti** ir dialogo lange **Produktų įtraukimas** pasirinkdami reikiamus produktus.

5. Tolesniuose „FastTab“ atnaujinkite reikiamų atributų reikšmes.

    - Bendrinami produktų publikavimo kanalai
    - Bendrai naudojami produkto atributai
    - Publikavimo kanalas
    - Kanalo produkto atributai

    > [!NOTE]
    > Jei sprendime „Finance and Operations“ sukuriama bendrai naudojama produktų medija ir bendrai naudojami produktų atributai, jie taikomi visiems mažmeninės prekybos produktams.

