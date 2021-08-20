---
title: Naujų laukų įtraukimas į verslo dokumento šabloną programoje „Microsoft Excel“
description: Šioje temoje pateikiama informacijos apie tai, kaip programoje „Microsoft Excel“ naudojant funkciją Verslo dokumentų valdymas į verslo dokumento šabloną įtraukti naujų laukų.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 57eebdc38fb3f74690b92c03fa60e10c7610db1fe413320a6d167f05b0658bf1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767247"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Naujų laukų įtraukimas į verslo dokumento šabloną programoje „Microsoft Excel“

[!include[banner](../includes/banner.md)]

Galite įtraukti naujų laukų į šabloną, kurį naudojant generuojami verslo dokumentai „Microsoft Excel“ formatu. Šiuos laukus galima įtraukti kaip vietos rezervavimo ženklus, kuriuos naudojant sugeneruoti dokumentai užpildomi reikiama informacija iš programos. Prie kiekvieno įtraukto lauko taip pat galite nurodyti susiejimą su duomenų šaltiniais, kad nurodytumėte, kokie programos duomenys bus įvedami į lauką, kai, naudojant šabloną, bus generuojami verslo dokumentai.

Norėdami sužinoti daugiau apie šią funkciją, atlikite šioje temoje esantį pavyzdį. Šiame pavyzdyje parodyta, kaip atnaujinti šabloną ir užpildyti sugeneruotos laisvos formos sąskaitos faktūros laukus.

## <a name="configure-business-document-management-to-edit-templates"></a>Funkcijos Verslo dokumentų valdymas konfigūravimas šablonams redaguoti

Kadangi funkcija Verslo dokumentų valdymas (BDM) yra sukurta sistemos [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md) pagrindu, pradėti dirbti su BDM galėsite tik sukonfigūravę reikiamus ER ir BDM parametrus.

1.  Kaip sistemos administratorius prisijunkite prie „Microsoft Dynamics 365 Finance“ egzemplioriaus.
2.  Atlikite tolesnius temoje [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md) pateikto pavyzdžio veiksmus.

    1.  Sukonfigūruokite ER parametrus.
    2.  Įjunkite BDM.

Dabar galite pradėti naudoti BDM ir redaguoti verslo dokumentų šablonus.

## <a name="import-er-solutions-that-contain-a-template"></a>ER sprendimų, kuriuose yra šablonas, importavimas

Šios procedūros pavyzdyje naudojamas oficialiai publikuotas ER sprendimas. Šio sprendimo ER konfigūracijas turite importuoti į savo dabartinį „Finance“ egzempliorių.

Šio sprendimo ER formato konfigūracijoje **Laisvos formos sąskaita faktūra („Excel“)** yra verslo dokumento šablonas „Excel“ formatu, kurį galima redaguoti naudojant BDM. Importuokite naujausią šios ER formato konfigūracijos versiją iš „Microsoft Dynamics“ Lifecycle Services“ (LCS). Atitinkamas ER duomenų modelis ir ER modelio susiejimo konfigūracijos bus importuoti automatiškai.

Norėdami gauti daugiau informacijos apie tai, kaip importuoti ER konfigūracijas, žr. [ER konfigūracijų ciklo valdymas](general-electronic-reporting-manage-configuration-lifecycle.md).

![LCS puslapis Bendrai naudojamo turto biblioteka.](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>ER sprendimo šablono redagavimas

1.  Prisijunkite kaip vartotojas, kuriam suteikta prieiga prie darbo srities **Verslo dokumentų valdymas**.
2.  Darbo sritį **Verslo dokumentų valdymas** atidarykite.

    ![Darbo sritis Verslo dokumentų valdymas.](./media/BDM-AddFldExcel-Workspace.png)

3.  Tinklelyje pasirinkite šabloną **Laisvos formos sąskaita faktūra („Excel“)**.
4.  Dešiniojoje srityje pasirinkite **Naujas šablonas**, kad sukurtumėte naują šabloną pasirinkto šablono pagrindu.
5.  Lauke **Pavadinimas** kaip naujo šablono pavadinimą įveskite **Laisvos formos sąskaita faktūra („Excel“) „Contoso”**.
6.  Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

Atidaromas BDM šablonų rengyklės puslapis. Naudodami „Microsoft 365“, pasirinktą šabloną galite redaguoti internetu, įdėtajame valdiklyje.

![BDM šablonų rengyklės puslapis.](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Naujo lauko žymos įtraukimas į šabloną

1.  BDM šablonų rengyklės puslapio „Excel“ juostelės skirtuke **Rodinys** pažymėkite redaguojamojo „Excel“ šablono žymės langelius **Antraštės ir Tinklelio eilutės**.

    ![Pažymėti žymės langeliai Antraštės ir Tinklelio eilutės.](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Pažymėkite langelius **E8:F8**.
3.  „Excel“ juostelės skirtuke **Pradžia** pasirinkdami **Sulieti ir centruoti**, pažymėtus langelius suliekite į naują sulietą langelį **E8:F8**.
4.  Sulietame langelyje **E8:F8** įveskite **URL**.
5.  Pasirinkite sulietą langelį **E7:F7** , tada – **Formato kopijavimo priemonė** ir sulietą langelį **E8:F8**, kad jį suformatuotumėte taip, kaip sulietas langelis **E7:F7**.

    ![Naujo lauko žyma įtraukta į šabloną.](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Šablono formatavimas norint rezervuoti vietą naujam laukui

1.  BDM šablonų rengyklės puslapyje pasirinkite sulietą langelį **G8:H8**.
2.  „Excel“ juostelės skirtuke **Pradžia** pasirinkdami **Sulieti ir centruoti**, pažymėtus langelius suliekite į naują sulietą langelį **G8:H8**.
3.  Pasirinkite sulietą langelį **G7:H7** , tada – **Formato kopijavimo priemonė** ir sulietą langelį **G8:H8**, kad jį suformatuotumėte taip, kaip sulietas langelis **G7:H7**.

    ![Vieta rezervuota naujam laukui.](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  Langelio lauke **Pavadinimas** pasirinkite **CompanyInfo**.

    Dabartinio „Excel“ šablono intervale **CompanyInfo** yra visi laukai, kuriuos naudojant sugeneruotos ataskaitos antraštė užpildoma dabartinės įmonės kaip pardavėjo šalies informacija.

    ![Parinktas intervalas „CompanyInfo”.](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Naujo lauko įtraukimas į šabloną

1.  Puslapio **BDM šablonų rengyklė** veiksmų srityje pasirinkite **Rodyti formatą**.
2.  Srityje **Šablono struktūra** pasirinkite **Įtraukti**.

    > [!NOTE]
    > Turite koreguoti šablono skyrių, kurį norite naudoti kaip naują lauką. Jį jau pakoregavote formatuodami sulietą langelį **G8:H8**.

    ![Naujo lauko įtraukimas į šabloną.](./media/BDM-AddFldExcel-AddCell.png)

3.  Pasirinkite **„Excel“\langelis**, kad į šabloną kaip langelį įtrauktumėte naują lauką.

    Jei į šabloną norite įtraukti naują intervalą, galite pasirinkti **„Excel“\intervalas**. Įvestame intervale gali būti keli langeliai. Šiuos langelius galite įtraukti vėliau.
    
    Atkreipkite dėmesį, kad srityje **Šablono struktūra** šablono komponentas **CompanyInfo** pasirinktas automatiškai, nes jis dabartinėje šablono struktūroje yra tinkamiausias pirminis komponentas įtraukiamam laukui.
    
4.  Lauke **„Excel“ intervalas** įveskite **CompanyURL_Value**.
5.  Pasirinkite **Gerai**.

    ![Laukas CompanyURL_Value įtrauktas į šablono struktūrą.](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  Srityje **Šablono struktūra** pasirinkite daugtaškio mygtuką (...), tada – **Rodyti susiejimus**.

    ![Pasirinkta Rodyti susiejimus.](./media/BDM-AddFldExcel-ShowBindings.png)

    Srityje **Šablono struktūra** dabar rodomi duomenų šaltiniai, pasiekiami esamame ER formate.

7.  Kaip lauką, kurį planuojate susieti su esamo ER formato duomenų šaltiniu, pasirinkite **CompanyInfo_Value**.
8.  Srities **Šablono struktūra** skyriuje **Duomenų šaltiniai** išplėskite **Modelis \>InvoiceBase \>CompanyInfo**.
9.  Dalyje **CompanyInfo** pasirinkite elementą **WebsiteURI**.

    ![Pasirinktas elementas WebsiteURI.](./media/BDM-AddFldExcel-BindURL.png)

10. Pasirinkite **Susieti**.
11. Srityje **Šablono struktūra** pasirinkite **Įrašyti** ir uždarykite BDM šablonų rengyklės puslapį.

Atnaujintas šablonas rodomas darbo srities **Verslo dokumentų valdymas** skirtuko **Šablonas** dešiniojoje srityje. Atkreipkite dėmesį, kad tinklelyje redaguoto šablono laukas **Būsena** pakeistas į **Juodraštis**, o laukas **Tikslinimas** nebėra tuščias. Šie pokyčiai nurodo, kad pradėtas šio šablono redagavimo procesas.

![Redaguotas šablonas darbo srityje Verslo dokumentų valdymas.](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Įmonės parametrų peržiūra

1.  Nueikite į **Organizacijos administravimas \> Organizacijos \> Juridiniai subjektai**.
2.  Patikrinkite, ar „FastTab“ elemente **Kontaktinė informacija** įvestas įmonės URL.

![Puslapyje Juridiniai subjektai įvestas įmonės URL.](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Verslo dokumentų generavimas atnaujintam šablonui patikrinti

1.  Programoje įmonę pakeiskite į **USMF** ir nueikite į **Gautinos sumos \> Sąskaitos faktūros \> Visos laisvos formos sąskaitos faktūros**.
2.  Pasirinkite sąskaitą-faktūrą **FTI-00000002**, tada – **Spausdinimo valdymas**.
3.  Kairiojoje srityje išplėskite **Modulis – gautinos sumos \> Dokumentai \> Laisvos formos sąskaita faktūra**.
4.  Dalyje **Laisvos formos sąskaita faktūra** pasirinkite lygmenį **Originalus dokumentas**, kad nurodytumėte apdoroti skirtų sąskaitų faktūrų aprėptį.
5.  Dešiniosios srities lauke **Ataskaitos formatas** pasirinkite nurodyto dokumento lygio šabloną **Laisvos formos sąskaita faktūra („Excel“) „Contoso”**.

    ![Pasirinktas šablonas Laisvos formos sąskaita faktūra („Excel“) „Contoso“.](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Paspauskite **„Esc“**, kad uždarytumėte dabartinį puslapį.
7.  Pasirinkite **Spausdinti \> Pasirinkta**.
8.  Atsisiųskite sugeneruotą dokumentą ir jį atidarykite programoje „Excel“.

    ![Laisvos formos sąskaita faktūra programoje „Excel“.](./media/BDM-AddFldExcel-PreviewReport.png)

Modifikuotas šablonas naudojamas pažymėtos prekės laisvos formos sąskaitos-faktūros ataskaitai generuoti. Norėdami išanalizuoti, kaip šią ataskaitą paveikė jūsų atlikti šablono pakeitimai, vykdykite šią ataskaitą viename programos seanse iš karto po to, kai paleičiate šabloną kitame programos seanse.

## <a name="related-links"></a>Susiję saitai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Verslo dokumentų valdymo apžvalga](er-business-document-management.md)

[Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]