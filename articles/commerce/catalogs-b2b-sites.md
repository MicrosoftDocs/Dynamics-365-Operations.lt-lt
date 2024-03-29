---
title: B2B svetainių „Commerce“ katalogų kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti "Commerce" katalogus Microsoft Dynamics 365 Commerce " verslo įmonių (B2B) svetainėms.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136832"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>B2B svetainių „Commerce“ katalogų kūrimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti "Commerce" produktų Microsoft Dynamics 365 Commerce katalogus "Business-to-business" (B2B) svetainėms. Atsakymus į dažnai užduodamus klausimus apie B2B svetainių "Commerce" katalogus žr [. B2B DUK "Commerce" kataloguose](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Šis straipsnis taikomas Dynamics 365 Commerce 10.0.27 ir vėlesniams leidimams.

Norėdami identifikuoti produktus, kuriuos norite pasiūlyti savo B2B interneto parduotuvėse, galite naudoti "Commerce" katalogus. Kai sukuriate katalogą, identifikuojate interneto parduotuves, kurių produktai yra siūlomi, įtraukiate norimus įtraukti produktus ir pagerinate produktų siūlymas įtraukdami prekybos informaciją. Galite sukurti kelis katalogus kiekvienai B2B interneto parduotuvei, kaip parodyta toliau pateiktame pavyzdyje.

!["Commerce" produktų katalogų peržiūra.](./media/Commerce_Catalogs.png)

"Commerce" produktų katalogai leidžia nurodyti šią informaciją:

- **Katalogo tipas** – sukonfigūruokite vertę kaip **B2B**. Galite nustatyti B2B katalogui brastos ypatybės, pvz., naršymo hierarchija, klientų hierarchija ir atributo metaduomenys katalogui. 
- **Katalogo konkreti naršymo hierarchija** – organizacijos gali sukurti savo konkretaus katalogo atskiros kategorijos struktūrą.
- **Katalogo atributų metaduomenys** – atributuose yra informacijos apie produktą. Priskirdami atributus naršymo hierarchijos kategorijai, galite nustatyti tų atributų vertes tai kategorijai priskirtų produktų lygyje. Tada organizacijos gali atlikti šias užduotis:

    - Apibrėžti katalogo atributų vertes.
    - Valdyti atributų matomumą katalogo lygyje.
    - Pasirinkti kiekvienam katalogui basias tikslinimo programas.

- **Kanalai** – organizacijos gali susieti daugiau nei vieną B2B interneto kanalą su katalogu. Šiuo metu galutinis katalogų palaikymas galimas tik B2B interneto parduotuvėms.
- **Klientų hierarchijos** – pagal nurodytą B2B kanalą organizacijos gali pasirinktam B2B partneriams pateikti specialų katalogą, sąstingio klientų hierarchijas su tuo katalogu.
- **Kainų grupės** – galite konfigūruoti konkretaus katalogo kainas ir akcijas. Ši galimybė yra pagrindinė B2B kanalo katalogo nustatymo priežastis. Katalogų kainų grupės leidžia organizacijoms gauti produktus savo numatytose B2B organizacijose ir taikyti pageidaujamą kainodarą ir nuolaidas. B2B klientai, kurie užsakė iš sukonfigūruoto katalogo, gali gauti specialių kainų ir akcijų po to, kai jie prisiregistruoja prie "Commerce B2B" svetainės. Norėdami konfigūruoti konkretaus katalogo kainas, skirtuke **·** **Katalogai** pasirinkite Kainų grupes, kad vieną ar daugiau kainų grupių susiekite su katalogu. Visos prekybos sutartys, kainos koregavimo žurnalai ir išplėstinės nuolaidos, susietos su ta pačia kainų grupe, bus taikomos klientų užsakymams iš to katalogo. (Išplėstinės nuolaidos apima ribinę vertę, kiekį ir nuolaidas prekių kiekiui.) Daugiau informacijos apie kainų grupes žr. Kainos [grupės](price-management.md#price-groups).

> [!NOTE]
> Šią funkciją galima naudoti pradedant nuo Dynamics 365 Commerce 10.0.27 versijos. Norėdami konfigūruoti katalogui skirtas konfigūracijas, pvz., naršymo hierarchiją ir klientų hierarchiją "Commerce Headquarters", **eikite** į funkcijų valdymo darbo sritį (**Sistemos administravimo \>\> darbo sričių funkcijų valdymas**),**įgalinkite** kelių katalogų naudojimą mažmeninės prekybos kanalų funkcijai ir **paleiskite 1110 CDX** užduotį. Kai įgalinate šią funkciją, visi esami katalogai, naudojami EKA parduotuvėms **arba skambučių centrui, bus pažymėti kaip katalogo tipas = B2C** **katalogų** puslapyje. EKA parduotuvėms ir skambučių **centrui taikomi tik esami ir nauji katalogai, pažymėti kaip Katalogo tipas = B2C**. 

## <a name="b2b-catalog-process-flow"></a>B2B katalogo proceso srautas

Katalogo kūrimo ir apdorojimo procesas turi keturis bendruosius veiksmus. Kiekvienas veiksmas išsamiai paaiškintas kitame skyriuje.

> [!NOTE]
> Prieš tęsdami įsitikinkite, kad katalogas pažymėtas kaip **Katalogo tipas = B2B**.

1. **[Konfigūracija](#configure-the-catalog)**

    - Susieti naršymo hierarchiją.
    - Nurodykite galiojimo pabaigos ir galiojimo datas, jei jos yra taikomos.
    - Įtraukite ir skirstykite produktus į kategorijas.
    - Susiekite kainų grupes.
    - Susiekite klientų hierarchiją, basą su jūsų B2B organizacijomis. 
    - Susiekite numatytąją dimensijos atributų grupę, skirta tikslinimams, pvz., dydžiui, stilius ir spalvai.
    - Nustatyti atributo metaduomenis.

1. **[Tikrinimas](#validate-the-catalog)** – šiame veiksme vykdote tikrinimo taisykles, kurios vykdo konkretų veikimą. Štai keletas pavyzdžių:

    - Įsitikinkite, kad nėra nekategorizuotų produktų.
    - Įsitikinkite, kad visos kiekvienam kanalui pateikti elementai yra susieti su katalogu.

1. **[Patvirtinimas](#approve-the-catalog)**
1. **[Publikuojama](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Nustatyti katalogą

Norėdami nustatyti katalogą naudokite šio skyriaus informaciją.

### <a name="configure-the-catalog"></a>Sukonfigūruoti katalogą

Norėdami sukonfigūruoti savo katalogus, **"Commerce Headquarters \>" eikite į "Retail" ir "Commerce \>" katalogus** ir asortimentus Visi katalogai.

Kai sukuriate naują katalogą, pirma turite jį susieti su vienu arba daugiau kanalų. Kuriant katalogą galima naudoti tik su [pasirinktais](/dynamics365/unified-operations/retail/assortments) kanalo asortimentais susietas prekes. Norėdami susieti katalogą su vienu arba daugiau kanalų, pasirinkite **Įtraukti** " **Commerce" kanalų "** FastTab", kuris yra **katalogo nustatymo** puslapyje. Įsitikinkite, kad katalogas pažymėtas kaip **katalogo tipas = B2B**.

#### <a name="associate-the-navigation-hierarchy"></a>Susieti naršymo hierarchiją

Norėdami įtraukti produktų į katalogą, turite pasirinkti naršymo hierarchiją. Naršymo hierarchija palaiko katalogo kategorijų struktūrą. Turite pasirinkti vieną iš naršymo hierarchijų **, susietų su kanalais, kuriuos pasirinkote katalogo nustatymo puslapio "FastTab" "Commerce** " **kanaluose**. Norėdami su kiekvienu kanalu susieti numatytąją naršymo hierarchiją, eikite į mažmeninės **prekybos ir komercijos kanalo \> nustatymo kanalo \> kategorijas ir produkto atributus**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Nurodyti galiojimo laiko ir galiojimo pabaigos datas

Norėdami nurodyti katalogo laiko ir galiojimo pabaigos datas, pasirinkite katalogo hierarchijos viršutinį mazgą, kad grįžkite į pagrindinio katalogo antraštės rodinį. Tada bendrajame " **FastTab"** konfigūruokite reikiamas galiojimo ir galiojimo datas.

#### <a name="add-and-categorize-products"></a>Įtraukti ir skirstyti produktus į kategorijas

Norėdami konfigūruoti produktus įtraukti į katalogą, "Commerce Headquarters **" eikite į "Retail" ir "Commerce \> " katalogus ir asortimentus \> Visi katalogai**. Tada skirtuke **Katalogai** pasirinkite Įtraukti **produktų**.

Arba naršymo hierarchijoje pasirinkite mazgą. Tada galėsite įtraukti produktų tiesiai į katalogo kategoriją.

#### <a name="associate-price-groups"></a>Susieti kainų grupes

Norėdami konfigūruoti produktus įtraukti į katalogą, "Commerce Headquarters **" eikite į "Retail" ir "Commerce \> " katalogus ir asortimentus \> Visi katalogai**. Tada skirtuke **Katalogai** pasirinkite Įtraukti **produktų**. 

Produktai, įtraukti **į** katalogą iš naršymo hierarchijos šakninio mazgo, veiksmų srityje pasirinkus Įtraukti produktų, paveldės savo kategorijas, jei šaltinio naršymo hierarchija taip pat susieta su katalogu. Kategorijų, kurios atliktus šaltinio naršymo hierarchijoje, pakeitimai bus nedelsiant atspindėti kataloguose. Norėdami atnaujinti kanalus turite iš naujo publikuoti katalogus.

Arba galite pasirinkti naršymo hierarchijos mazgą ir įtraukti produktus tiesiai į pasirinktą katalogo kategoriją. 

Kai įtraukiate produktus, **automatiškai įtraukiami visi variantai, kai pasirinkta pasirinktis Tik** bendrasis produktas. Norėdami išvengti visų variantų įtraukimo, pasirinkite bent vieną bendrojo produkto variantą. 

> [!NOTE]
> Jei pasirinksite automatiškai įtraukti visus variantus į didelio bendrojo produkto pasirinkimą, gali į ilgesnį apdorojimo laiką. Jei norite pasirinkti didelius **pasirinkimus**, pasirinkite Įtraukti visus variantus į katalogų puslapio veiksmų sritį, kad operacija būtų vykdoma paketiniu režimu. Jei į katalogą įtraukėte tik bendrąjį produktą ir neįtraukė jokių variantų, variantų išrinkiklis gali būti negalimas, kai perėjote į produkto informacijos puslapį. 

Norėdami konfigūruoti katalogui brangų kainas, turite susieti vieną ar daugiau kainų grupių su katalogu. Norėdami susieti kainų grupes su katalogu, "Commerce Headquarters", **eikite į "Retail" ir "Commerce \> " katalogus ir asortimentus \> Visi katalogai**. Tada skirtuko Katalogai **dalyje** Kaina **pasirinkite** Kainų **grupės**. Visos su ta pačia kainų grupe susietos prekybos sutartys, kainos koregavimo žurnalai ir išplėstinės nuolaidos (ribinės vertės, kiekis ir nuolaidos prekių kiekiui) bus taikomos klientų užsakymams iš katalogo.

Daugiau informacijos apie kainų grupes žr. Kainos [grupės](price-management.md#price-groups).

> [!NOTE]
> Naujos kainų grupės negalite sukurti puslapyje Visi **katalogai**. Turite jį sukurti puslapyje Visos **kainos** grupės. Tada turite jį susieti su katalogu puslapyje **Visi katalogai**.

#### <a name="associate-a-customer-hierarchy"></a>Susieti klientų hierarchiją

Norėdami susieti klientų hierarchijas, "Commerce Headquarters", eikite į " **Retail" ir "Commerce \> " katalogus ir asortimentus \> Visi katalogai**. Tada skirtuko Katalogai **klientų** **hierarchijoje** pasirinkite Priskirti hierarchijas **,** norėdami susieti vieną ar daugiau klientų hierarchijų su katalogu.

> [!NOTE]
> Negalite sukurti naujos klientų hierarchijos puslapyje **Visi katalogai**. Turite jį sukurti klientų **hierarchijų puslapyje**. Tada turite jį susieti su katalogu puslapyje **Visi katalogai**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Susieti numatytąją dimensijos atributų grupę, skirta tikslinimams, pvz., dydžiui, stilius ir spalvai

Norėdami susieti numatytąją "Commerce Headquarters" patikslintijų dimensijų atributų grupę, pvz., dydį, stilių ir spalvą, **eikite į "Retail" ir "Commerce \> Catalogs" ir asortimentus \> Visi katalogai**. Tada skirtuko Katalogai **dalyje** Atributai **pasirinkite** Atributų **grupės**.

#### <a name="set-attribute-metadata"></a>Nustatyti atributo metaduomenis

Norėdami konfigūruoti atributų metaduomenis, "Commerce Headquarters **" eikite į "Retail" ir "Commerce \> " katalogus ir asortimentus \> Visi katalogai**. Tada skirtuko Katalogai **dalyje** Atributai **pasirinkite** Nustatyti atributo **metaduomenis**. Norėdami pasirinkti atributus, kuriuos galima peržiūrėti ir patikslinti, susijusioje katalogo naršymo hierarchijoje pasirinkite kategoriją, **tada** dalyje Katalogo produkto atributai pasirinkite atributą. Tada pasirinkite **Rodyti atributą kanale**. Pagal numatytuosius nustatymus visų peržiūrėtimų atributų galima ieškoti. Jei norite patikslinti atributus (nebūtina), pasirinkite **Galima patikslinti**.

### <a name="validate-the-catalog"></a>Patikrinkite katalogą

Prieš naudojant naują katalogą, jį reikia patikrinti ir publikuoti.

Norėdami tikrinti katalogą, atlikite toliau nurodytus veiksmus.

1. Puslapio Visi **katalogai** skirtuke **Katalogai** dalyje **Tikrinti pasirinkite** Tikrinti **katalogą,** kad būtų vykdomas tikrinimas. Šis veiksmas yra būtinas. Programa patikrins, ar reikiamas nustatymas yra tikslus.
1. Norėdami **peržiūrėti tikrinimo** informaciją, pasirinkite Peržiūrėti rezultatus. Jei randama klaidų, turite ištaisyti duomenis ir tada vykdyti tikrinimą dar kartą, kol ji pereis.

> [!NOTE]
> Jei **katalogo tipas = B2B, patikrinimas** nesėkmingas, jei į katalogą įtraukėte EKA parduotuves arba skambučių centrą. B2B katalogai turi turėti tik su jais susietus B2B interneto kanalus. Tikrinimas bus nesėkmingas, jei su B2B katalogu nėra susieta jokia klientų hierarchija. 

### <a name="approve-the-catalog"></a>Patvirtinti katalogą

Po to, kai katalogas patikrintas, jis turi būti patvirtintas.

Norėdami pradėti katalogo patvirtinimo darbo eigą, atlikite šiuos veiksmus.

1. Visų katalogų puslapio **veiksmų srityje pasirinkite** Darbo eigos **\> pateiktis**.
1. Pereikite į " **Retail" ir "Commerce \> Headquarters" nustatymo \> "Commerce Workflows"**, norėdami konfigūruoti darbo eigos veiksmus ir įgaliotus vartotojus. Darbo eiga apibrėžs veiksmus, kurių reikia norint gauti katalogą į būseną **Patvirtinta**.

### <a name="publish-the-catalog"></a>Katalogo publikavimas

Kai katalogo būsena yra **Patvirtinta**, galite jį publikuoti **meniu Katalogai** pasirinkdami **Publikuoti**. Kai katalogo būsena Paskelbta **, jį** galima naudoti įraše skambučių centro užsakyme ir siųsti katalogo procesus. Katalogą galite publikuoti rankiniu būdu arba naudodami paketinį procesą. Nurodyta katalogo įsigaliojimo data nulemia, kada produktai pasiekiami interneto parduotuvėje. Jūsų nustatyta galiojimo pabaigos data nustato, kada produktai pašalinami iš interneto parduotuvės.

> [!NOTE]
> Galite publikuoti katalogą, kuriame yra produktai su įspėjimais. Tačiau šie produktai nebus rodomi interneto parduotuvėje.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce“ katalogų išplečiamumo poveikis, skirtas B2B tinkinimams](catalogs-b2b-sites-dev.md)

[B2B DUK svetainių „Commerce“ katalogai](catalogs-b2b-sites-FAQ.md)

[Katalogo išrinkiklio modulis](catalog-picker.md)
