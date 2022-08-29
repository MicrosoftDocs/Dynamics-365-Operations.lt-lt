---
title: Verslo dokumentų valdymo apžvalga
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudoti ER sistemos verslo dokumentų valdymo funkciją.
author: kfend
ms.date: 04/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.assetid: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
ms.openlocfilehash: 0fab7e1a36d9b4092cf4353533704859e83bed26
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288295"
---
# <a name="business-document-management-overview"></a>Verslo dokumentų valdymo apžvalga

[!include [banner](../includes/banner.md)]

Verslo vartotojai naudoja [elektroninių ataskaitų (ER)](general-electronic-reporting.md) sistemą, kad konfigūruotų siunčiamų dokumentų formatus pagal įvairių šalių / regionų teisinius reikalavimus. Vartotojai taip pat gali apibrėžti duomenų srautą, kad nurodytų kokie programos duomenys išdėstyti sugeneruotuose dokumentuose. ER sistema generuoja išsiunčiamus dokumentus „Microsoft Office“ formatais („Excel“ darbaknygėmis arba „Word“ dokumentais) naudojant iš anksto nustatytus šablonus. Šablonai yra užpildomi reikiama informacija pagal sukonfigūruotą duomenų srautą, kol reikalingi dokumentai yra generuojami. Kiekvienas sukonfigūruotas formatas gali būti publikuojamas kaip ER sprendimo dalis tam tikriems išsiunčiamiems dokumentams generuoti. Tai parodo ER formato konfigūracija, kurioje yra šablonų, kuriuos galite naudoti skirtingiems išsiunčiamiems dokumentams generuoti. Verslo vartotojai gali naudoti šią sistemą reikalingiems verslo dokumentams valdyti.

**Verslo dokumentų valdymas** sukurtas papildant ER sistemą ir leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft 365“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą. Dokumentų redagavimai gali apimti verslo dokumento dizaino keitimą ir vietos rezervavimo ženklų pridėjimą prie papildomų duomenų be šaltinio kodo keitimo ir naujų diegimų. Verslo dokumentų šablonų naujinimui nereikalingas joks ER sistemos išmanymas.

> [!NOTE]
> Atminkite, kad verslo dokumentų valdymas leidžia jums modifikuoti šablonus, kurie naudojami verslo dokumentų, pvz., užsakymų, sąskaitų-faktūrų ir kt., kūrimui. Nors šablonas buvo modifikuotas ir buvo išleista nauja versija, ši versija naudojama reikalingiems verslo dokumentams generuoti. Verslo dokumentų valdymas negali būti naudojamas jau sugeneruotų verslo dokumentų modifikavimui.

## <a name="supported-deployments"></a>Palaikomi diegimai

Dabar verslo dokumentų valdymo funkcija įdiegta tik debesies diegimams. Jei ši funkcija yra svarbi jūsų vietiniui diegimui, praneškite mums pateikdami atsiliepimą svetainėje [Idėjos](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Palaikomos „Microsoft Office“ taikomosios programos

Norėdami naudoti verslo dokumentų valdymą šablonų redagavimui „Excel“ arba „Word“ formatais naudojant „Microsoft Office“ darbalaukio programas, turite įdiegti „Microsoft Office 2010“ arba naujesnę versiją. Tai palaikoma atliekant diegimą debesyje ir vietinį diegimą.

Jei norite naudoti verslo dokumentų valdymą, norėdami redaguoti šablonus "Excel" arba "Word Microsoft 365 " formatuose naudodami programas, turite Microsoft 365 turėti žiniatinklio abonemento Office. Tai palaikoma debesies diegime.

## <a name="business-document-availability"></a>Verslo dokumentų pasiekiamumas

Pilnam visų ataskaitų, suplanuotų 2019 m. spalio mėn leidimui, žiūrėkite [Konfigūruotinų verslo dokumentų ataskaitos programose „Word“ ir „Excel“](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

Pilnam visų ataskaitų, suplanuotų 2020 m. spalio mėn leidimui, žiūrėkite [Konfigūruotini verslo dokumentai – „Word“ šablonai](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Būsimuose leidimuose bus prieinama daugiau ataskaitų. Specialūs pranešimai apie papildomas ataskaitas bus atsiųsti atskirai. Norėdami sužinoti, kaip peržiūrėti šiuo metu galimų ataskaitų sąrašą, žiūrėkite [ER konfigūracijų, išleistų „Finance” tam kad būtų palaikomi toliau pateikti konfigūruojami verslo dokumentai, sąrašas](#list-of-configurations-cbd) skyrių žemiau.

Norėdami daugiau sužinoti apie šią funkciją, užpildykite pavyzdį šiame straipsnyje.

## <a name="configure-er-parameters"></a>ER parametrų konfigūravimas

Kadangi verslo dokumentų valdymas sukurtas papildant ER sistemą, turite sukonfigūruoti ER parametrus, kad pradėtumėte darbą su verslo dokumentų valdymu. Norėdami tai atlikti, turite nustatyti ER parametrus taip, kaip nurodyta temoje [Elektroninių ataskaitų (ER) sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md). Taip pat turite įtraukti naują konfigūracijos tiekėją kaip nurodyta temoje [Kurkite konfigūracijos tiekėjus ir žymėkite juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER darbo sritis.](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>ER sprendimų importavimas

Šios procedūros pavyzdyje naudojami ER konfigūracijų pavyzdžiai. Į dabartinį "Dynamics 365 Finance" egzempliorių turite importuoti ER konfigūracijas, kuriose yra verslo dokumentų šablonai, kuriuos galima redaguoti naudojant verslo dokumentų valdymą. Atsisiųskite ir vietinėje sistemoje išsaugokite tolesnius failus, kad užbaigtumėte procedūrą.

**Pavyzdinis ER klientų sąskaitos-faktūros išrašymo sprendimas**

| Failas                                      | Turinys |
|-------------------------------------------|---------|
| Customer invoicing model.version.2.xml    | [ER duomenų modelio konfigūracija](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| Customer FTI report (GER).version.2.3.xml | [Laisvos formos sąskaitos-faktūros ER formato konfigūracija](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**Pavyzdinis ER mokėjimo kvitų sprendimas**

| Failas                                     | Turinys |
|------------------------------------------|---------|
| Model for cheques.version.10.xml         | [ER duomenų modelio konfigūracija](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Cheques printing format.version.10.9.xml | [Mokėjimo kvito ER formato konfigūracija](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**Pavyzdinis ER užsienio prekybos sprendimas**

| Failas                             | Turinys |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [ER duomenų modelio konfigūracija](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat report.version.1.9.xml | [Intrastat valdiklio ataskaitos ER formato konfigūracija](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

Norėdami importuoti kiekvieną failą, atlikite toliau nurodytą procedūrą. Importuokite kiekvieno aukščiau lentelėse nurodyto ER sprendimo ER *duomenų modelio* konfigūraciją prieš importuodami atitinkamą ER *formato* konfigūraciją.

1. Atidarykite puslapį **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio viršuje pasirinkite **Keisti**.
3. Pasirinkite **Įkelti iš XML failo**.
4. Pasirinkite **Naršyti**, kad įkeltumėte reikalingą XML failą.
5. Pasirinkite **Gerai**, kad patvirtintumėte konfigūracijos importavimą.

![ER konfigūracijų puslapis, patvirtinantis konfigūracijos importavimą.](./media/BDM-Overview-ERSolutions.png)

Taip pat galite importuoti oficialiai publikuotas ER formato konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS). Pavyzdžiui, norėdami atlikti šią procedūrą, galite importuoti naujausią ER formato konfigūraciją **Laisvos formos sąskaita faktūra („Excel“)**. Atitinkamas ER duomenų modelis ir ER modelio susiejimo konfigūracijos bus importuoti automatiškai.

![LCS bendrai naudojamo turto bibliotekos turinio puslapis.](./media/BDM-Overview-SharedAssetLibrary.png)

Daugiau informacijos apie ER konfigūracijų importavimą rasite temoje [ER konfigūracijos ciklo valdymas](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Verslo dokumentų valdymo įjungimas

Norėdami pradėti verslo dokumentų valdymą, turite atidaryti parinkties **Funkcijos valdymas** darbo sritį ir įjungti funkciją **Verslo dokumentų valdymas**.

Atlikite toliau nurodytą procedūrą, kad įjungtumėte verslo dokumentų valdymo funkciją visiems juridiniams subjektams.

1. Atidarykite parinkties **Funkcijos valdymas** darbo sritį.
2. Atidarykite skirtuką **Naujas** ir sąraše pasirinkite funkciją **Verslo dokumentų valdymas**.
3. Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.
4. Norėdami pasiekti naują funkciją, atnaujinkite puslapį.

> [!NOTE]
> Daugiau informacijos apie tai, kaip naudoti naujo dokumento vartotojo sąsają funkcijoje Verslo dokumentų valdymas, žr. [Naujo dokumento vartotojo sąsaja funkcijoje Verslo dokumentų valdymas](er-business-document-management-new-template-ui.md).

![Funkcijos valdymo darbo sritis.](./media/BDM-Overview-FMEnabling.png)

Daugiau informacijos apie naujų funkcijų aktyvavimą žr. temoje [Funkcijos valdymo apžvalga](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Parametrų konfigūravimas

Norėdami nustatyti pagrindinius verslo dokumentų valdymo parametrus, sekite tolesniuose skyriuose pristatytą informaciją.

### <a name="prerequisites-for-parameter-setup"></a>Parametrų nustatymo būtinosios sąlygos

Prieš nustatydami verslo dokumentų valdymą, turite nustatyti reikalingą dokumento tipą dokumentų valdymo sistemoje. Dokumento tipas nurodo laikiną dokumentų „Office“ formatais („Excel“ ir „Word“), naudojamų kaip ER ataskaitų šablonai, saugyklą. Laikinos saugyklos šablonas gali būti redaguojamas naudojant „Office“ darbalaukio programas.

Šiam dokumento tipui turi būti pasirinktos toliau nurodytos atributų vertės.

| Atributo pavadinimas | Atributo vertė |
|----------------|-----------------|
| Klasė          | Pridėti failą     |
| Grupuoti          | Failas            |
| Vieta       | „SharePoint“      |

Daugiau informacijos apie tai, kaip nustatyti reikalingus dokumentų valdymo parametrus ir dokumentų tipus rasite temoje [Dokumentų valdymo konfigūravimas](../../fin-ops/organization-administration/configure-document-management.md).

![Dokumentų valdymo dokumento tipo nustatymas.](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Parametrų nustatymas

Pagrindinius verslo dokumentų valdymo parametrus galite nustatyti puslapyje **Verslo dokumentų parametrai**. Puslapis pasiekiamas tik konkretiems vartotojams. Vartotojai, galintys pasiekti puslapį:

- Vartotojai, kuriems priskirtas **Sistemos administratoriaus** vaidmuo.
- Vartotojai, kuriems priskirtas bet kuris vaidmuo, sukonfigūruotas atlikti pareigą, **Palaikyti verslo dokumentų valdymo parametrus** (AOT pavadinimas **ERBDMaintainParameters**).

Atlikite toliau nurodytą procedūrą, kad nustatytumėte pagrindinius parametrus visiems juridiniams subjektams.

1. Prisijunkite kaip vartotojas, kuriam suteikta prieiga prie puslapio **Verslo dokumentų parametrai**.
2. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Verslo dokumentų valdymas** \> **Verslo dokumentų parametrai**.
3. Puslapyje **Verslo dokumentų parametrai**, skirtuke **Priedai**, lauke **„SharePoint“ dokumento tipas** apibrėžkite dokumento tipą, kuris turėtų būti naudojamas laikinai saugoti šablonus „Office“ formatais, kol jie redaguojami naudojant „Office“ darbalaukio programas. 

> [!NOTE]
> Šis parametras pasiekiamas tik dokumentų tipams, kurie sukonfigūruoti naudojant „SharePoint“ vietą.

![Verslo dokumentų valdymo parametrų nustatymas.](./media/BDM-Overview-BDMSetting.png)

Pasirinktas dokumento tipas yra būdingas įmonei ir bus naudojamas, kai vartotojas dirba su verslo dokumentų valdymu įmonėje, kuriai sukonfigūruotas pasirinktas dokumento tipas. Kai vartotojas dirba su verslo dokumentų valdymu kitoje įmonėje, tas pats pasirinktas dokumento tipas bus naudojamas jei jis nebuvo sukonfigūruotas šiai įmonei. Kai dokumento tipas sukonfigūruotas, jis bus naudojamas vietoje to, kuris pasirinktas lauke **„SharePoint“ dokumento tipas**.

> [!NOTE]
> Parametre **„SharePoint“ dokumento tipas** „SharePoint“ aplankas apibrėžiamas kaip laikina šablonų, kuriuos galima redaguoti naudojant „Microsoft Excel“ arba „Word“, saugykla. Turite nustatyti šį parametrą, jei planuojate naudoti šias „Office“ darbalaukio programas šablonams redaguoti. Norėdami gauti daugiau informacijos, žr. [Šablono redagavimas „Office“ darbalaukio programoje](#EditInOfficeDesktopApp). Šį parametrą galite palikti tuščią, jei planuojate modifikuoti šabloną tik naudodami funkciją, esaą programoje Microsoft 365. Daugiau informacijos žr. [Šablono redagavimas naudojant „Microsoft 365“](#EditInOffice365).

## <a name="configure-access-permissions"></a>Prieigos teisių konfigūravimas

Pagal numatytuosius nustatymus, kai prieiga prie verslo dokumentų valdymo teisių neįgalinta, kiekvienas vartotojas, kuriam suteikta prieiga prie verslo dokumentų valdymo darbo srities, matys visus prieinamus ER sprendimo šablonus. Verslo dokumentų valdymo darbo srityje bus rodomi tik tie šablonai, kurie yra ER formato konfigūracijose ir pažymėti žyme **Verslo dokumentų tipas**.

![ER konfigūracijų puslapis su verslo dokumento tipo žyme.](./media/BDM-Overview-ERFormatTags.png)

Šablonų, prieinamų verslo dokumentų valdymo darbo srityje, sąrašas gali būti apribotas konfigūruojant prieigos teises. Tai svarbu, kai skirtingi šablonai naudojami skirtingų verslo domenų (funkcinių sričių) verslo dokumentams kurti, o jūs norite suteikti konkretiems vartotojams prieigą prie skirtingų šablonų, kad jie galėtų juos redaguoti verslo dokumentų valdymo darbo srityje.

Prieigos prie verslo dokumentų valdymo teises galite nustatyti parinktyje **Prieigos teisių konfigūratorius**. Puslapis pasiekiamas tik toliau nurodytiems vartotojams:

- Vartotojai, kuriems priskirtas **Sistemos administratoriaus** vaidmuo.
- Vartotojai, kuriems priskirtas bet kuris kitas vaidmuo, sukonfigūruotas atlikti pareigą, **Konfigūruoti teises pasiekti verslo dokumentų šablonus redagavimui** (AOT pavadinimas **ERBDTemplatesSecurity**).

Atlikite toliau nurodytą procedūrą, kad nustatytumėte prieigos prie verslo dokumentų valdymo teises visiems juridiniams subjektams.

1. Prisijunkite prie kaip vartotojas, kuriam suteikta prieiga prie puslapio **Prieigos teisių konfigūratorius**.
2. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Verslo dokumentų valdymas** \> **Valdyti prieigos teises**.

    Atkreipkite dėmesį į pranešimą, kuris informuoja, kad prieigos prie verslo dokumentų valdymo teisių naudojimas šiuo metu neįjungtas.

    ![Verslo dokumentų valdymo prieigos teisių puslapio konfigūratorius.](./media/BDM-Overview-TemplatesAccess1.png)

    Pagal šį parametrą kiekvienas vartotojas, kuriam priskirtas bet kuris saugos vaidmuo, sukonfigūruotas atlikti pareigą **Verslo dokumentų šablonų valdymas** (AOT pavadinimas **ERBDManageTemplates**), gali atidaryti verslo dokumentų valdymo darbo sritį ir redaguoti bet kurį prieinamą šabloną.

    Toliau pateiktame grafiniame elemente parodyta, kas prieinama verslo dokumentų valdymo darbo srityje vartotojams, kuriems suteiktas **Gautinų sumų klerkas** vaidmuo. Pagal dabartinį prieigos teisių parametrą, vartotojas gali redaguoti skirtingų funkcinių sričių, įskaitant sąskaitos-faktūros išrašymą, teisės aktų nustatytas ataskaitas ir mokėjimus, verslo dokumentų šablonus.

    ![Verslo dokumentų valdymo darbo srities puslapis, skirtas gautinų sumų klerkui.](./media/BDM-Overview-TemplatesForAlice1.png)

3. Puslapyje **Prieigos teisių konfigūratorius** pasirinkite **Prieigos teisių parametras**.
4. Dialogo lange **Parametrai prieigos teisių šablonų redagavimui** įjunkite parinktį **Taikyti sukonfigūruotas prieigos teises**.
5. Pasirinkite **Gerai**, kad patvirtintumėte, jog verslo dokumentų valdymo prieigos teisės buvo įjungtos.

    ![Verslo dokumentų valdymo prieigos teisių patvirtinimas.](./media/BDM-Overview-TemplatesAccess2.png)

6. Pasirinkite **Įtraukti**, kad įvestumėte naują verslo vaidmenį, kuriam reikia sukonfigūruoti teises pasiekti verslo dokumentų valdymo šablonus.
7. Dialogo lange **Saugos vaidmenys** pasirinkite vaidmenį **Gautinų sumų klerkas** ir tada pažymėkite **Gerai**, kad patvirtintumėte vaidmens pasirinkimą.
8. Skirtuke **Prieigos teisės konfigūracijų žymėms** pasirinkite **Naujas**.
9. Lauke **Žymės tipas** pasirinkite **Funkcinė sritis**, o lauke **ID** pasirinkite **Sąskaitos-faktūros išrašymas**.
10. Pasirinkite **Įrašyti**, kad išsaugotumėte sukonfigūruotas prieigos teises pasirinktam vaidmeniui.

    Dabartinis parametras reiškia, kad kiekvienam vartotojui, kuriam priskirtas **Gautinų sumų klerkas** vaidmuo ir kuris atlieka pareigą **Verslo dokumentų šablonų valdymas** (AOT pavadinimas **ERBDManageTemplates**), ER formato konfigūracijos šablonai, turintys vertę **Sąskaitos-faktūros išrašymas** žymėje **Funkcinė sritis**, bus prieinami redaguoti verslo dokumentų valdymo darbo srityje.

11. Perjunkite sritį **Susijusi informacija** iš dabartinio puslapio dešinės pusės. Srityje **Susijusi informacija** rodoma, kaip bus taikomos sukonfigūruotos prieigos teisės, taip pat kokie ER konfigūracijų šablonai bus prieinami vartotojams, kuriems priskirtas **Gautinų sumų klerkas** vaidmuo.

    ![Susijusios informacijos sritis prieigos teisių konfigūratoriaus puslapyje.](./media/BDM-Overview-TemplatesAccess3.png)

12. Skirtuke **Prieigos teisės konfigūracijų žymėms** pasirinkite parinktį **Įtraukti**.
13. Dialogo lange **Pasirinkti konfigūraciją** pažymėkite **Intrastat ataskaita** ER formato konfigūraciją.
14. Pasirinkite **Gerai**, kad patvirtintumėte pasirinktos konfigūracijos įvedimą, o tada pasirinkite **Įrašyti**, kad išsaugotumėte sukonfigūruotas prieigos teises pasirinktam vaidmeniui.

Dabartinis parametras reiškia, kad kiekvienam vartotojui, kuriam priskirtas **Gautinų sumų klerkas** vaidmuo ir kuris atlieka pareigą **Verslo dokumentų šablonų valdymas** (AOT pavadinimas **ERBDManageTemplates**), toliau nurodyti šablonai bus prieinami redaguoti verslo dokumentų valdymo darbo srityje:

- Šablonai, turintys vertę **Sąskaitos-faktūros išrašymas** žymei **Funkcinė sritis**.
- Iš ER formato konfigūracijų sukurti šablonai, kurie išvardyti žymėje **Prieigos teisės konfigūracijoms** (šiame pavyzdyje, šablonai iš **Intrastat ataskaita** formato konfigūracijos domene **Privalomos ataskaitos**).

![Prieigos teisių „FastTabs” prieigos teisių konfigūratoriaus puslapyje.](./media/BDM-Overview-TemplatesAccess4.png)

Toliau pateiktame grafiniame elemente parodyta, ką teikia verslo dokumentų valdymo darbo sritis vartotojui, kuriam suteiktas **Gautinų sumų klerkas** vaidmuo. Pagal dabartinį verslo dokumentų valdymo prieigos teisių parametrą, vartotojas gali redaguoti verslo dokumentų šablonus iš domeno **Sąskaitos-faktūros išrašymas** ir **Intrastat ataskaita** ER formato konfigūracijos. Šablonai iš domeno **Mokėjimai** nepasiekiami vaidmeniui **Gautinų sumų klerkas**.

![Verslo dokumentų šablonų redagavimas verslo dokumentų valdymo darbo srities puslapyje.](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **Prieigos teisių konfigūracijų** taisyklės saugomos naudojant ER formato konfigūracijos unikalaus identifikavimo ID. Tai reiškia, kad šios taisyklės nebus panaikintos, kai jomis besiremianti ER konfigūracija yra panaikinama. Kai importuojate panaikintas konfigūracijas atgal į šį egzempliorių, šios taisyklės vėl bus joms priskirtos. Nereikia dar kartą nustatyti taisyklių, kai vėl importuojate panaikintas konfigūracijas.

## <a name="use-business-document-management-to-edit-templates"></a>Verslo dokumentų valdymo naudojimas šablonams redaguoti

Verslo vartotojai gali pasiekti verslo dokumentų šablonus, skirtus redaguoti verslo dokumentų valdymo darbo srityje. Tik toliau nurodyti vartotojai gali pasiekti verslo dokumentų valdymo darbo sritį:

- Vartotojai, kuriems priskirtas **Sistemos administratoriaus** vaidmuo.
- Vartotojai, kuriems priskirtas bet kuris vaidmuo, sukonfigūruotas atlikti pareigą, **Valdyti verslo dokumentų šablonus** (AOT pavadinimas **ERBDManageTemplates**).

Atlikite toliau nurodytą procedūrą, kad galėtumėte redaguoti laisvos formos sąskaitos-faktūros šablonus verslo dokumentų valdymo darbo srityje. Prieš baigdami šią procedūrą, turite būti baigę visas šiame straipsnyje nurodytas procedūras.

1. Prisijunkite kaip vartotojas, kuriam suteikta prieiga prie verslo dokumentų valdymo darbo srities.
2. Atidarykite verslo dokumentų valdymo darbo sritį.

Kai funkcija **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** yra išjungta darbo srityje **Funkcijų valdymas**, darbo srities **Verslo dokumentų valdymas** pagrindiniame tinklelyje rodomi toliau pateikti šablonai.

- Šablonai, priklausantys jūsų ER konfigūracijos teikėjui (t. y. teikėjui, kuris šiuo metu pažymėtas kaip aktyvus darbo srityje **Elektroninės ataskaitos**). Pasirinkę vieną iš šių šablonų, galite pasirinkti **Redaguoti šabloną**, kad pradėtumėte jį redaguoti arba tęstumėte darbą.
- Šablonai, priklausantys kitiems ER konfigūracijos teikėjams. Pasirinkę vieną iš šių šablonų, galite pasirinkti **Naujas dokumentas**, kad sukurtumėte kopiją, priklausančią jūsų ER konfigūracijos teikėjui, o tada pradėti redaguoti kopiją.

![Šablonų įrašai verslo dokumentų valdymo darbo srities puslapyje.](./media/BDM-Overview-EditingTemplate1.png)

Skirtuke **Šablonas** pristatomas pasirinkto šablono turinys. Pasirinkite skirtuką **Išsami informacija**, kad peržiūrėtumėte išsamią pasirinkto šablono informaciją, taip pat ER formato konfigūracijos, kurioje yra šis šablonas, išsamią informaciją. Atkreipkite dėmesį, kad visi šablonai turi būseną **Paskelbta** ir neturi jokios išsamios informacijos stulpelyje **Tikslinimas**. Tai reiškia, kad šie šablonai šiuo metu neredaguojami.

Kai funkcija **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** įjungta darbo srityje **Funkcijų valdymas**, darbo srities **Verslo dokumentų valdymas** pagrindiniame tinklelyje rodomi šablonai, priklausantys jūsų ER konfigūracijos teikėjui (t. y. teikėjui, kuris šiuo metu pažymėtas kaip aktyvus darbo srityje **Elektroninės ataskaitos**). Pasirinkę vieną iš šių šablonų, galite pasirinkti **Redaguoti šabloną**, kad pradėtumėte jį redaguoti arba tęstumėte darbą.

Norėdami dirbti su šablonais, priklausančiais kitiems ER konfigūracijos teikėjams, pasirinkite **Naujas dokumentas**, kad sukurtumėte šablono, priklausančio jūsų ER teikėjui, kopiją. Tada galite pradėti redaguoti kopiją. Daugiau informacijos žr. [Nauja dokumento vartotojo sąsaja verslo dokumentų valdyme](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Redagavimo šablonų, priklausančių jūsų konfigūracijos teikėjui, iniciavimas

1. Verslo dokumentų valdymo darbo srityje sąraše pasirinkite šabloną **Kvitų spausdinimo formatas**.
2. Pažymėkite skirtuką **Išsami informacija**.

![Verslo dokumentų valdymo darbo srities puslapis, Išsamios informacijos skirtukas.](./media/BDM-Overview-EditingTemplate2.png)

Pasirinktam šablonui pasiekiama parinktis **Redaguoti šabloną**. Ši parinktis visada pasiekiama ER formato konfigūracijos, priklausančios aktyvios ER konfigūracijos tiekėjui (šiame pavyzdyje – **„Litware, Inc.“**), šablonui. Kai pasirenkate parinktį **Redaguoti šabloną**, galite redaguoti esamą šabloną iš esamo ER formato konfigūracijos juodraščio versijos.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Redagavimo šablonų, priklausančių kitiems teikėjams, iniciavimas

1. Darbo srityje Verslo dokumentų valdymas pasirinkite dokumentą, kurį norite naudoti kaip šabloną.

    ![Pasirinkite dokumentą verslo dokumentų valdymo darbo srities puslapyje.](./media/BDM-Overview-EditingTemplate3.png)

2. Pasirinkite **Naujas dokumentas** ir, jei reikia, lauke **Pavadinimas** pakeiskite redaguojamo šablono pavadinimą. Tekstas bus naudojamas automatiškai sukurtai ER formato konfigūracijai pavadinti. Atkreipkite dėmesį, kad šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**), kurioje bus suredaguotas šablonas, juodraščio versija bus automatiškai pažymėta vykdyti šį ER formatą dabartiniam vartotojui. Tuo pat metu, nemodifikuotas originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas šiam bet kuriam kitam vartotojui skirtam ER formatui vykdyti.
3. Lauke **Pavadinimas** pakeiskite automatiškai sukurto redaguojamo šablono pirmo pataisymo pavadinimą.
4. Lauke **Komentaras** pakeiskite redaguojamo šablono automatiškai sukurto pataisymo komentarą.
5. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

![Redagavimo proceso pradžios patvirtinimas naujo šablono kūrimui.](./media/BDM-Overview-EditingTemplate4.png)

Jeigu nėra jokio teikėjo, jį bus siūloma sukurti. Jeigu nėra jokio aktyvaus teikėjo, bus siūloma jį pasirinkti aktyvavimui.

Norėdami sukurti teikėją, pakeiskite teikėjo pavadinimą lauke **Pavadinimas**, atnaujinkite naujo teikėjo internetinį adresą lauke **Internetinis adresas** ir pasirinkite **Gerai** patvirtinimui.

   ![Naujo BDM teikėjo kūrimas.](./media/bdm_create_provider.png)

Norėdami aktyvuoti esamą teikėją, pasirinkite teikėjo pavadinimą lauke **Konfigūracijos teikėjas** ir pasirinkite **Gerai** nustatyti teikėjui kaip aktyviam.

   ![BDM teikėjo aktyvavimas.](./media/bdm_choose_provider.png)

> [!NOTE]
> Kiekvienas BDM šablonas kreipiasi į teikėją kaip į konfigūracijos autorių. Štai todėl šablonui reikia aktyvaus teikėjo.


Parinktis **Naujas dokumentas** visada pasiekiama ER formato konfigūracijos šablonui, kurį teikia dabartinis ir kitas tiekėjas (šiame pavyzdyje – „Microsoft“) ir kuriame nėra pataisymų. Redaguotas šablonas bus išsaugotas naujoje automatiškai sugeneruotoje ER formato konfigūracijoje.



### <a name="start-editing-a-template"></a>Pradėkite redaguoti šabloną

1. Pasirinktame šablone pasirinkite **Redaguoti dokumentą**.
2. Lauke **Pavadinimas** pakeiskite automatiškai sukurto redaguojamo šablono pirmo pataisymo pavadinimą.
3. Lauke **Komentaras** pakeiskite redaguojamo šablono automatiškai sukurto pataisymo pastabą.

    ![Šablono redagavimas verslo dokumentų valdymo darbo srities puslapyje.](./media/BDM-Overview-EditingTemplate5.png)

4. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

Bus atidarytas puslapis **BDM šablono redaktorius**. Pasirinktą šabloną bus galima redaguoti internetu naudojant „Microsoft 365“.

![Verslo dokumentų valdymo šablonų redaktoriaus puslapis.](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Šablono redagavimas naudojant „Microsoft 365“

Šabloną galima modifikuoti naudojant „Microsoft 365“. Pavyzdžiui, programoje „Office Online“ pakeiskite lauko raginimų šablono antraštėje šriftą iš **Paprastasis** į **Paryškintasis**. Šie pakeitimai automatiškai išsaugomi redaguojamame šablone, kuris saugomas pirminėje šablono saugykloje (pagal numatytuosius nustatymus – „Azure“ didelių dvejetainių objektų saugykloje). Ji konfigūruojama ER sistemai.

![Šablono antraštės šrifto keitimas į paryškintąjį verslo dokumentų valdymo šablonų rengyklės puslapyje.](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Šablono redagavimas „Office“ darbalaukio programoje

> [!NOTE]
> Ši funkcija galima tik tada, kai parametras **„SharePoint“ dokumento tipas** tinkamai sukonfigūruotas. Daugiau informacijos žr. [Parametrų konfigūravimas](#SetupBdmParameters).

1. Pasirinkite parinktį **Atidaryti darbalaukio programoje**, kad modifikuotumėte šabloną naudojant „Office“darbalaukio programų (šiame pavyzdyje – „Excel“) funkciją. Redaguojamas šablonas nukopijuojamas iš nuolatinės saugyklos į laikiną saugyklą, sukonfigūruotą verslo dokumentų valdymo parametruose kaip „SharePoint“ aplankas.
2. Patvirtinkite, kad norite atidaryti šabloną iš laikinos failų saugyklos „Office“ darbalaukio „Excel“ programoje.

    ![Šablonas atidarytas darbalaukio „Excel” programoje.](./media/BDM-Overview-EditingLayout3.png)

3. Modifikuokite šabloną. Pavyzdžiui, programoje „Office Online“ pakeiskite laukų raginimų šablono antraštėje šriftą pakeisdami spalvą iš **Juoda** į **Mėlyna**.

    ![Šablono antraštės šrifto spalvos modifikavimas naudojant darbalaukio „Excel” programą.](./media/BDM-Overview-EditingLayout4.png)

4. Pasirinkite **Įrašyti** „Excel“ darbalaukio programoje, kad įrašytumėte šablono pakeitimus laikinoje saugykloje.

    ![Įrašykite pakeitimus į verslo dokumentų valdymo šablonų rengyklės puslapį naudojant darbalaukio „Excel” programą.](./media/BDM-Overview-EditingLayout5.png)

5. Uždarykite „Excel“ darbalaukio programą.
6. Pasirinkite **Sinchronizuoti išsaugotą kopiją**, kad sinchronizuotumėte laikiną šablonų saugyklą į nuolatinę šablonų saugyklą.

> [!NOTE]
> Redaguojamo šablono kopija saugoma laikinoje failų saugykloje tik šablono redagavimo dabartinio seanso metu. Kai baigiate seansą uždarydami puslapį **BDM šablono redaktorius**, ši kopija panaikinama. Jei pakoregavote šabloną laikinoje failų saugykloje ir nepasirinkote **Sinchronizuoti išsaugotą kopiją**, kai bandysite uždaryti puslapį **BDM šablono redaktorius**, iššoks pranešimas, klausiantis ar norite išsaugoti pristatytus pakeitimus. Pasirinkite **Taip**, jei norite išsaugoti pakeitimus šablonui nuolatinėje failų vietoje.

### <a name="validate-a-template"></a>Šablono tikrinimas

1. Puslapyje **BDM šablono redaktorius** pasirinkite **Ieškoti problemų**, kad patikrintumėte modifikuotą šabloną pagal esamą ER formato konfigūraciją. Sekite rekomendacijas (jei yra), kad sulygiuotumėte šabloną su formato struktūra iš pagrindinės ER formato konfigūracijos.
2. Pasirinkite **Rodyti formatą**, kad peržiūrėtumėte dabartinę formato struktūrą iš pagrindinės ER formato konfigūracijos, kuri turi būti sulygiuota su redaguojamu šablonu. 
3. Norėdami uždaryti sritį, pasirinkite **Slėpti formatą**.

    ![BDM BDM šablono redaktoriaus puslapis.](./media/BDM-Overview-EditingTemplate6.png)

4. Uždarykite puslapį **BDM šablono redaktorius**.

Atnaujintas šablonas rodomas skirtuke **Šablonas**. Atkreipkite dėmesį, kad redaguojamo šablono būsena dabar yra **Juodraštis** ir dabartinis pataisymas nebėra tuščias. Tai reiškia, kad šio šablono redagavimo procesas prasidėjo.

![Atnaujinto šablono verslo dokumentų valdymo darbo srities puslapyje peržiūra.](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Modifikuoto šablono testavimas 

1. Programoje įmonę pakeiskite į **USMF**.
2. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
3. Pasirinkite sąskaitą-faktūrą **FTI-00000002**, o tada pasirinkite **Spausdinimo valdymas**.
4. Pasirinkite lygį **Modulis – gautinos sumos** \> **Dokumentai** \> **Laisvos formos sąskaitos-faktūra** \> **Originalus dokumentas**, kad nurodytumėte apdorojimui skirtų sąskaitų-faktūrų aprėptį.
5. Lauke **Ataskaitos formatas** pasirinkite **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija** ER formatą nurodytam dokumento lygiui.

    ![Spausdinimo valdymo parametro puslapis.](./media/BDM-Overview-TestRun1.png)

6. Norėdami uždaryti dabartinį puslapį, paspauskite **Išeiti**.
7. Pasirinkite **Spausdinti**, o tada pasirinkite **Pasirinkta**.
8. Atsisiųskite dokumentą ir jį atidarykite naudojant „Excel“ darbalaukio programą.

![Laisvos formos sąskaitos-faktūros puslapis.](./media/BDM-Overview-TestRun2.png)

Modifikuotas šablonas naudojamas pažymėtos prekės laisvos formos sąskaitos-faktūros ataskaitai generuoti. Norėdami išanalizuoti, kaip šią ataskaitą paveikė jūsų pristatyti šablono pakeitimai, galite vykdyti šią ataskaitą viename programos seanse iš karto po to, kai modifikavote šabloną kitame programos seanse.

### <a name="create-an-alternative-template-revision"></a>Alternatyvaus šablono pataisymo kūrimas

1. Atidarykite puslapį **BDM šablono redaktorius** ir pasirinkite šabloną **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**.
2. Skirtuke **Pataisymai** pasirinkite **Naujas**.
3. Jei reikia, lauke **Pavadinimas** pakeiskite antro pataisymo pavadinimą ir pagrįsite jį šiuo metu aktyviu pirmu pataisymu.
4. Jei reikia, lauke **Komentaras** pakeiskite redaguojamo šablono automatiškai sukurto pataisymo pastabą.

    ![Šablono tikslinimų verslo dokumentų valdymo darbo srities puslapyje kūrimas.](./media/BDM-Overview-AddRevision.png)

    Sukūrėte naują šablono versiją, kuri buvo išsaugota nuolatinėje šablono saugykloje. Dabar galite tęsti antro pataisymo, kuris šiuo metu pažymėtas kaip aktyvus, šablono redagavimą.

5. Pasirinkite pirmą pataisymą, o tada pasirinkite **Nustatyti kaip aktyvų**. Galite pasirinkti kitą pataisymą kaip aktyvų jei kuriuo nors metu norėsite grąžinti tą šablono pataisymą.
6. Pasirinkite antrą pataisymą ir tada pasirinkite **Naikinti**.
7. Norėdami patvirtinti, kad norite panaikinti pažymėtą pataisymą, pasirinkite **Gerai**. Galite panaikinti bet kurį neaktyvų pataisymą, kai jis nebereikalingas.

### <a name="delete-a-modified-template"></a>Modifikuoto šablono naikinimas

1. Puslapyje **BDM šablono redaktorius** pasirinkite skirtuką **Šablonas**.
2. Pasirinkite **Naikinti**.
3. Jei pasirenkate **Gerai**, kad patvirtintumėte naikinimą, ER formatas **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija** su modifikuotu šablonu bus panaikinti. Norėdami peržiūrėti kitas parinktis, pasirinkite **Atšaukti**.

### <a name="revoke-changes-of-template"></a>Šablono pakeitimų atšaukimas

Kai redaguojate šabloną iš ER formato, priklausančio dabartiniam aktyviam tiekėjui, jums bus suteikta galimybė atšaukti šablonui pristatytus pakeitimus.

![Šablono pakeitimų verslo dokumentų valdymo darbo srities puslapyje atmetimas.](./media/BDM-Overview-RevokeChanges.png)

1. Puslapyje **BDM šablono redaktorius** pasirinkite skirtuką **Šablonas**.
2. Pasirinkite **Anuliuoti**.
3. Jei pasirenkate **Gerai**, kad atšauktumėte šablonui pristatytus pakeitimus, modifikuotas šablonas bus pakeistas originaliu šablonu, o visi pakeitimai bus pašalinti. Kai atšaukiate šablono pakeitimus, galėsite ištrinti šabloną. Norėdami peržiūrėti kitas parinktis, pasirinkite **Atšaukti**.

### <a name="publish-a-modified-template"></a>Modifikuoto šablono publikavimas

1. Puslapio **BDM šablono redaktorius** skirtuke **Šablonas** pasirinkite **Publikuoti**.
2. Jei pasirenkate **Gerai**, kad patvirtintumėte publikavimą, išvestinio ER formato **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija** juodraščio versija, kurioje yra modifikuotas šablonas, bus pažymėta kaip užbaigta. Modifikuotas šablonas taps pasiekiamas kitiems vartotojams. Užbaigtose šio ER formato versijose liks tik paskutinis aktyvus jūsų šablono pataisymas. Kiti pataisymai bus panaikinti. Norėdami peržiūrėti kitas parinktis, pasirinkite **Atšaukti**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Aš pasirinkote redaguoti dokumentą, bet vietoj to, kad nueisite į BDM šablono rengyklės puslapį finansuose, aš esu nusiųstas į tinklalapį Microsoft 365.

Ši problema yra žinoma problema, apimanti nukreipimą Microsoft 365. Jis įvyksta, kai pasirašote Microsoft 365 pirmą kartą. Norėdami išspręsti šią problemą, jūsų naršyklėje pasirinkite **Atgal** tam, kad grįžtumėte į ankstesnį puslapį.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Su suprasti, kaip Microsoft 365 redaguoti šabloną, naudojant pirmą programos seansą, ir kaip naudoti šabloną antroje programos seanse ir koreguoti šabloną, kad pamatytumėte, kaip mano pakeitimai paveiks sugeneruotą verslo dokumentą. Ar galiu naudoti „Office” darbalaukio programą tuo pačiu būdu?

Taip, galite. Pirmame programos seanse pasirinkite **Atidaryti darbalaukio programoje**. Jūsų šablonas bus išsaugotas laikinoje failų saugykloje ir atidarytas „Office“ darbalaukio programoje. Tada atlikite toliau nurodytus veiksmus, kad peržiūrėtumėte jūsų šablono pakeitimus sugeneruotame verslo dokumente:

1. Atlikite šablono pakeitimus naudojant „Office“ darbalaukio programą.
2. „Office“ darbalaukio programoje pasirinkite **Įrašyti**.
3. Pirmo programos seanso puslapyje **BDM šablono redaktorius** pasirinkite **Sinchronizuoti išsaugotą kopiją**.
4. Vykdykite šio šablono ER formatą antrame programos seanse.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Kai darbalaukio programoje pasirenku Atidaryti, rodomas šis klaidos pranešimas: „Vertė negali būti neapibrėžta. Parametro pavadinimas: externalId.” Kaip galiu išspręsti šią problemą?

Tikėtina, kad prisijungėte prie dabartinio „Azure AD“ domeno programos egzemplioriaus, kuris skiriasi nuo „Azure AD“ domeno, kuris buvo naudojamas diegiant šį egzempliorių. Kadangi „SharePoint“ paslauga, naudojama šablonams saugoti, kad jie būtų prieinami redagavimui naudojant „Office“ darbalaukio programas, priklauso tam pačiam domenui, mes neturime teisių pasiekti „SharePoint“ paslaugą. Norėdami išspręsti šią problemą, prisijunkite prie dabartinio egzemplioriaus naudodami vartotojo kredencialus tinkamame „Azure AD“ domene.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[ER: konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas (2016 m. lapkričio mėn.)](tasks/er-design-reports-openxml-2016-11.md)

[ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu](tasks/er-design-configuration-word-2016-11.md)

[Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md)

[Elektroninių ataskaitų (ER) konfigūravimas duomenims perkelti į „Power BI“](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>ER konfigūracijų, išleistų „Finance” tam, kad būtų galima palaikyti konfigūruojamus verslo dokumentus, sąrašas

„Finance” ER konfigūracijų [sąrašas](general-electronic-reporting.md#list-of-configurations) yra nuolat atnaujinamas. Atidarykite [visuotinę saugyklą](er-download-configurations-global-repo.md) tam, kad peržiūrėtumėte šiuo metu palaikomų ER konfigūracijų sąrašą. Galite [filtruoti](../../../finance/localizations/enhanced-filtering-global-repo.md) visuotinę saugyklą tam, kad peržiūrėtumėte ER konfigūracijų, naudojamų konfigūruotiniems verslo dokumentams palaikyti, sąrašą.

![Visuotinės saugyklos turinio konfigūracijų saugyklos puslapyje filtravimas.](./media/bdm-overview-filterglobalrepo.gif)

Šioje lentelėje pateikiamas ER konfigūracijų, palaikančių konfigūruotinus verslo dokumentus ir kurios buvo išleistos „Finance” iki 2020 m. gruodžio mėn, sąrašas.

| Duomenų modelio konfigūracija    | Formato konfigūracija                           |
|-----------------------------|-------------------------------------------------|
| Važtaraščio modelis        | Važtaraštis („Excel”)                          |
|                             | Važtaraštis („Word”)                           |
| Kilmės sertifikato modelis | Kilmės sertifikatas („Excel”)                   |
|                             | Kilmės sertifikatas („Word”)                    |
| Sąskaitos faktūros modelis               | Klientų debeto ir kredito pažyma („Excel”)          |
|                             | Klientų debeto ir kredito pažyma („Word”)           |
|                             | Laisvos formos sąskaita faktūra („Excel“)                       |
|                             | Laisvos formos sąskaita faktūra („Excel“) (BH)                  |
|                             | Laisvos formos sąskaita faktūra (FR) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra (LT) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra (LV) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra (PL) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra (CZ) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra (EE) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra (HU) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra (TH) („Excel“)                  |
|                             | Laisvos formos sąskaita faktūra („Word”)                        |
|                             | Projekto sutarties eilutės elementai („Excel”)             |
|                             | Projekto sutarties eilutės elementai (CZ) („Excel”)        |
|                             | Projekto sutarties eilutės elementai („Excel”) (BH)        |
|                             | Projekto sutarties eilutės elementai (HU) („Excel”)        |
|                             | Projekto sutarties eilutės elementai (LT) („Excel”)        |
|                             | Projekto sutarties eilutės elementai (PL) („Excel”)        |
|                             | Projekto sutarties eilutės elementai („Word”)              |
|                             | Projekto kliento saugojimo išleidimas („Excel”)      |
|                             | Projekto kliento saugojimo išleidimas (CZ) („Excel”) |
|                             | Projekto kliento saugojimo išleidimas (HU) („Excel”) |
|                             | Projekto kliento saugojimo išleidimas (LT) („Excel”) |
|                             | Projekto kliento saugojimo išleidimas (PL) („Excel”) |
|                             | Projekto kliento saugojimo išleidimas (TH) („Excel”) |
|                             | Projekto kliento saugojimo išleidimas („Word”)       |
|                             | Projekto sąskaita faktūra („Excel”)                         |
|                             | Projekto sąskaita faktūra („Word”)                          |
|                             | Projekto sąskaita faktūra (AE) („Excel”)                    |
|                             | Projekto sąskaita faktūra (CZ) („Excel”)                    |
|                             | Projekto sąskaita faktūra („Excel”) (BH)                    |
|                             | Projekto sąskaita faktūra (HU) („Excel”)                    |
|                             | Projekto sąskaita faktūra (JP) („Excel”)                    |
|                             | Projekto sąskaita faktūra (LT) („Excel”)                    |
|                             | Projekto sąskaita faktūra (PL) („Excel”)                    |
|                             | Projekto sąskaita faktūra (TH) („Excel”)                    |
|                             | Pilna projekto sąskaita faktūra (MY) („Excel”)               |
|                             | Paprasta projekto sąskaita faktūra (MY) („Excel”)             |
|                             | Projekto tvarkymo sąskaita faktūra („Excel”)                  |
|                             | Projekto tvarkymo sąskaita faktūra (CZ) („Excel”)             |
|                             | Projekto tvarkymo sąskaita faktūra („Excel”) (BH)             |
|                             | Projekto tvarkymo sąskaita faktūra (HU) („Excel”)             |
|                             | Projekto tvarkymo sąskaita faktūra (JP) („Excel”)             |
|                             | Projekto tvarkymo sąskaita faktūra (LT) („Excel”)             |
|                             | Projekto tvarkymo sąskaita faktūra (PL) („Excel”)             |
|                             | Projekto tvarkymo sąskaita faktūra („Word”)                   |
|                             | Išankstinė pirkimo sąskaita faktūra („Excel”)                |
|                             | Išankstinė pirkimo sąskaita faktūra („Word”)                 |
|                             | Išankstinė pardavimo sąskaita faktūra („Excel”)                   |
|                             | Išankstinė pardavimo sąskaita faktūra („Word”)                    |
|                             | Išankstinė pardavimo sąskaita faktūra (PL) („Excel”)              |
|                             | Pardavimo sąskaita faktūra („Excel”)                           |
|                             | Pardavimo sąskaita faktūra („Excel”) (BH)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (CZ)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (EE)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (FR)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (HU)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (IN)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (LT)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (LV)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (PL)                      |
|                             | Pardavimo sąskaita faktūra („Excel”) (TH)                      |
|                             | Pardavimo sąskaita faktūra („Word”)                            |
|                             | TMS Prekybinė sąskaita faktūra („Excel”)                  |
|                             | TMS Prekybinė sąskaita faktūra („Word”)                   |
|                             | Tiekėjo SF dokumentas („Excel”)                 |
|                             | Tiekėjo SF dokumentas (CZ) („Excel”)            |
|                             | Tiekėjo SF dokumentas (HU) („Excel”)            |
|                             | Tiekėjo SF dokumentas (IN) („Excel”)            |
|                             | Tiekėjo SF dokumentas (LT) („Excel”)            |
|                             | Tiekėjo SF dokumentas (LV) („Excel”)            |
|                             | Tiekėjo SF dokumentas (MY) („Excel”)            |
|                             | Tiekėjo SF dokumentas („Word”)                  |
| Užsakymo modelis                 | Sutarties patvirtinimas („Excel”)                  |
|                             | Sutarties patvirtinimas („Word”)                   |
|                             | Pirkimo sutarties patvirtinimas („Excel”)         |
|                             | Pirkimo sutarties patvirtinimas („Word”)          |
|                             | Pirkimo užsakymas („Excel”)                          |
|                             | Pirkimo užsakymas (CZ) („Excel”)                     |
|                             | Pirkimo užsakymo užklausa (CZ) („Excel”)             |
|                             | Pirkimo užsakymas (HU) („Excel”)                     |
|                             | Pirkimo užsakymo užklausa (HU) („Excel”)             |
|                             | Pirkimo užsakymas („Word”)                           |
|                             | Pirkimo užsakymo užklausa („Excel”)                  |
|                             | Pirkimo užsakymo užklausa („Word”)                   |
|                             | Pardavimo užsakymo patvirtinimas („Excel”)                |
|                             | Pardavimo užsakymo patvirtinimas (CZ) („Excel”)           |
|                             | Pardavimo užsakymo patvirtinimas (HU) („Excel”)           |
|                             | Pardavimo užsakymo patvirtinimas („Word”)                 |
| Važtaraščio modelis          | Konteinerio turinys („Excel”)                      |
|                             | Konteinerio turinys („Word”)                       |
|                             | Krovinių sąrašas („Excel”)                               |
|                             | Krovinių sąrašas („Word”)                                |
|                             | Išrinkimo dokumentas („Excel”)                            |
|                             | Išrinkimo dokumentas (CZ) („Excel”)                       |
|                             | Išrinkimo dokumentas („Word”)                             |
|                             | Gamybos išrinkimo dokumentas („Excel”)                    |
|                             | Gamybos išrinkimo dokumentas („Word”)                     |
|                             | Krovinių išrinkimo dokumentas („Excel”)             |
|                             | Krovinių išrinkimo dokumentas („Word”)              |
|                             | Siuntų išrinkimo dokumentas („Excel”)         |
|                             | Siuntų išrinkimo dokumentas („Word”)          |
|                             | Bangų išrinkimo dokumentas („Excel”)             |
|                             | Bangų išrinkimo dokumentas („Word”)              |
| Mokėjimo modelis               | Kliento mokėjimo pažyma („Excel”)                 |
|                             | Kliento mokėjimo pažyma („Word”)                  |
|                             | Tiekėjo mokėjimo pažyma („Excel”)                   |
|                             | Tiekėjo mokėjimo pažyma („Word”)                    |
| Pasiūlymo modelis             | Projekto pasiūlymas („Excel”)                       |
|                             | Projekto pasiūlymas („Word”)                        |
|                             | Pasiūlymo patvirtinimas („Excel”)                   |
|                             | Pasiūlymo patvirtinimas (Priimti) („Excel”)          |
|                             | Pasiūlymo patvirtinimas (Priimti) („Word”)           |
|                             | Pasiūlymo patvirtinimas (Atmesti) („Excel”)          |
|                             | Pasiūlymo patvirtinimas (Atmesti) („Word”)           |
|                             | Pasiūlymo patvirtinimas (Sugrąžinti) („Excel”)          |
|                             | Pasiūlymo patvirtinimas (Sugrąžinti) („Word”)           |
|                             | Pasiūlymo patvirtinimas („Word”)                    |
|                             | Pardavimo pasiūlymas („Excel”)                         |
|                             | Pardavimo pasiūlymas (CZ) („Excel”)                    |
|                             | Pardavimo pasiūlymas (HU) („Excel”)                    |
|                             | Pardavimo pasiūlymas („Word”)                          |
|                             | Pardavimo pasiūlymo patvirtinimas („Excel”)            |
|                             | Pardavimo pasiūlymo patvirtinimas („Word”)             |
| Derinimo modelis        | Kliento sąskaitos išrašas, plėt („Excel”)             |
|                             | Kliento sąskaitos išrašas, plėt (CN) („Excel”)        |
|                             | Kliento sąskaitos išrašas, plėt („Word”)              |
|                             | Kliento sąskaitos išrašas, Prancūzija („Excel”)          |
| Priminimo modelis              | Priminimo laiško pastaba (Excel)                  |
|                             | Priminimo laiško pastaba (CN) (Excel)             |
|                             | Priminimo laiško pastaba („Word”)                   |
|                             | Kliento delspinigių pažyma („Excel”)                  |
|                             | Kliento delspinigių pažyma („Word”)                   |
| Krovinio važtaraščio modelis               | Krovinio mokėjimo priemonė („Excel”)                             |
|                             | Krovinio mokėjimo priemonė („Word”)                              |
|                             | Pirkimo užsakymo važtaraštis („Excel”)             |
|                             | Pirkimo užsakymo važtaraštis (CZ) („Excel”)        |
|                             | Pirkimo užsakymo važtaraštis („Word”)              |
|                             | Maršrutas („Excel”)                                   |
|                             | Maršrutas („Word”)                                    |
|                             | Pardavimo užsakymo važtaraštis („Excel”)                |
|                             | Pardavimo užsakymo važtaraštis (CZ) („Excel”)           |
|                             | Pardavimo užsakymo važtaraštis (LT) („Excel”)           |
|                             | Pardavimo užsakymo važtaraštis (PL) („Excel”)           |
|                             | Pardavimo užsakymo važtaraštis („Word”)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
