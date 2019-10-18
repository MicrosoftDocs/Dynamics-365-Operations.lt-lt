---
title: Verslo dokumentų valdymo apžvalga
description: Šioje temoje pateikiama informacija apie tai, kaip naudotis ER sistemos verslo dokumentų valdymo funkcija.
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c84b08ec45dfa7aa9c7b913087a2518bfeedf87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181570"
---
# <a name="business-document-management-overview"></a>Verslo dokumentų valdymo apžvalga

Verslo vartotojai naudoja [Elektroninių ataskaitų (ER) sistemą](general-electronic-reporting.md), kad konfigūruotų siunčiamų dokumentų formatus pagal įvairių šalių / regionų teisinius reikalavimus. Vartotojai taip pat gali apibrėžti duomenų srautą, kad nurodytų kokie programos duomenys išdėstyti sugeneruotuose dokumentuose. ER sistema generuoja išsiunčiamus dokumentus „Microsoft Office“ formatais („Excel“ darbaknygėmis arba „Word“ dokumentais) naudojant iš anksto nustatytus šablonus. Šablonai yra užpildomi reikiama informacija pagal sukonfigūruotą duomenų srautą, kol reikalingi dokumentai yra generuojami. Kiekvienas sukonfigūruotas formatas gali būti publikuojamas kaip ER sprendimo dalis tam tikriems išsiunčiamiems dokumentams generuoti. Tai parodo ER formato konfigūracija, kurioje yra šablonų, kuriuos galite naudoti skirtingiems išsiunčiamiems dokumentams generuoti. Verslo vartotojai gali naudoti šią sistemą reikalingiems verslo dokumentams valdyti.

**Verslo dokumentų valdymas** sukurtas papildant ER sistemą ir leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft Office 365“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą. Dokumentų redagavimai gali apimti verslo dokumento dizaino keitimą ir vietos rezervavimo ženklų pridėjimą prie papildomų duomenų be šaltinio kodo keitimo ir naujų diegimų. Verslo dokumentų šablonų naujinimui nereikalingas joks ER sistemos išmanymas.

> [!NOTE]
> Atminkite, kad verslo dokumentų valdymas leidžia jums modifikuoti šablonus, kurie naudojami verslo dokumentų, pvz., užsakymų, sąskaitų-faktūrų ir kt., kūrimui. Nors šablonas buvo modifikuotas ir buvo išleista nauja versija, ši versija naudojama reikalingiems verslo dokumentams generuoti. Verslo dokumentų valdymas negali būti naudojamas jau sugeneruotų verslo dokumentų modifikavimui.

## <a name="supported-deployments"></a>Palaikomi diegimai

Dabar verslo dokumentų valdymo funkcija įdiegta tik debesies diegimams. Jei ši funkcija yra svarbi jūsų vietiniui diegimui, praneškite mums pateikdami atsiliepimą svetainėje [Idėjos](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Palaikomos „Microsoft Office“ taikomosios programos

Norėdami naudoti verslo dokumentų valdymą šablonų redagavimui „Excel“ arba „Word“ formatais naudojant „Microsoft Office“ darbalaukio programas, turite įdiegti „Microsoft Office 2010“ arba naujesnę versiją. Tą galima padaryti atliekant diegimą debesyje ir vietinį diegimą.

## <a name="business-document-availability"></a>Verslo dokumentų pasiekiamumas

Toliau nurodytos ataskaitos (kartu su „Excel“ pagrįstais šablonais) bus prieinamos su viešosios peržiūros versijos išleidimu:

**Gautinos sumos** (2019 m. rugpjūčio mėn.)

- Išankstinė pardavimo sąskaita faktūra
- Pardavimo užsakymo važtaraštis

**Mokėtinos sumos** (2019 m. rugpjūčio mėn.)

- Išankstinės sąskaitos-faktūros pirkimas
- Pirkimo užsakymas
- Užsakymo važtaraščio pirkimas

Daugiau ataskaitų bus pasiekiamos. Specialūs pranešimai apie papildomas ataskaitas bus atsiųsti atskirai. 

Pilną visų ataskaitų, suplanuotų 2019 m. spalio mėn. leidimui, sąrašą galite rasti čia: [Konfigūruotinų verslo dokumentų ataskaitos programose „Word“ ir „Excel“](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

# <a name="example-enable-configure-and-use-business-document-management"></a>Pavyzdys: Įjunkite, konfigūruokite ir naudokite verslo dokumentų valdymą

Norėdami sužinoti daugiau apie šią funkciją, atlikite šioje temoje esantį pavyzdį.

## <a name="configure-er-parameters"></a>ER parametrų konfigūravimas

Kadangi verslo dokumentų valdymas sukurtas papildant ER sistemą, turite sukonfigūruoti ER parametrus, kad pradėtumėte darbą su verslo dokumentų valdymu. Norėdami tai atlikti, turite nustatyti ER parametrus kaip nurodyta temoje [ER sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md). Taip pat turite įtraukti naują konfigūracijos tiekėją kaip nurodyta temoje [Kurkite konfigūracijos tiekėjus ir žymėkite juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER darbo sritis](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>ER sprendimų importavimas

Turite importuoti ER konfigūracijas, kuriose yra verslo dokumentų šablonų, į dabartinį egzempliorių. Atsisiųskite ir išsaugokite vietinėje sistemoje šiuos failus, kad užbaigtumėte procedūrą.

**Pavyzdinis ER klientų sąskaitos-faktūros išrašymo sprendimas**

| **Failas**                                  | **Turinys**                                |
|-------------------------------------------|--------------------------------------------|
| Customer invoicing model.version.2.xml    | [ER duomenų modelio konfigūracija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Laisvos formos sąskaitos-faktūros ER formato konfigūracija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Pavyzdinis ER mokėjimo kvitų sprendimas**

| **Failas**                                  | **Turinys**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [ER duomenų modelio konfigūracija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [Mokėjimo kvito ER formato konfigūracija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Pavyzdinis ER užsienio prekybos sprendimas**

| **Failas**                                  | **Turinys**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [ER duomenų modelio konfigūracija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [Intrastat valdiklio ataskaitos ER formato konfigūracija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Norėdami importuoti kiekvieną failą, atlikite toliau nurodytą procedūrą. Importuokite kiekvieno aukščiau lentelėse nurodyto ER sprendimo ER *duomenų modelio* konfigūraciją prieš importuodami atitinkamą ER *formato* konfigūraciją.

1. Atidarykite puslapį **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio viršuje pasirinkite **Keisti**.
3. Pasirinkite **Įkelti iš XML failo**.
4. Pasirinkite **Naršyti**, kad įkeltumėte reikalingą XML failą.
5. Pasirinkite **Gerai**, kad patvirtintumėte konfigūracijos importavimą.

![ER konfigūracijų puslapis](./media/BDM-Overview-ERSolutions.png)

Daugiau informacijos apie ER konfigūracijų importavimą rasite temoje [ER konfigūracijos ciklo valdymas](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Verslo dokumentų valdymo įjungimas

Norėdami pradėti verslo dokumentų valdymą, turite atidaryti parinkties **Funkcijos valdymas** darbo sritį ir įjungti funkciją **Verslo dokumentų valdymas**.

Atlikite toliau nurodytą procedūrą, kad įjungtumėte verslo dokumentų valdymo funkciją visiems juridiniams subjektams.

1. Atidarykite parinkties **Funkcijos valdymas** darbo sritį.
2. Atidarykite skirtuką **Naujas** ir sąraše pasirinkite funkciją **Verslo dokumentų valdymas**.
3. Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.
4. Norėdami pasiekti naują funkciją, atnaujinkite puslapį.

![Funkcijos valdymo darbo sritis](./media/BDM-Overview-FMEnabling.png)

Daugiau informacijos apie naujų funkcijų aktyvavimą žr. temoje [Funkcijos valdymo apžvalga](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Parametrų konfigūravimas

Norėdami nustatyti pagrindinius verslo dokumentų valdymo parametrus, sekite tolesniuose skyriuose pristatytą informaciją.

### <a name="prerequisites-for-parameter-setup"></a>Parametrų nustatymo būtinosios sąlygos
Prieš nustatydami verslo dokumentų valdymą, turite nustatyti reikalingą dokumento tipą dokumentų valdymo sistemoje. Dokumento tipas nurodo laikiną dokumentų „Office“ formatais („Excel“ ir „Word“), naudojamų kaip ER ataskaitų šablonai, saugyklą. Laikinos saugyklos šablonas gali būti redaguojamas naudojant „Office“ darbalaukio programas.

Šiam dokumento tipui turi būti pasirinktos toliau nurodytos atributų vertės.

| **Atributo pavadinimas**  | **Atributo vertė**   |
|---------------------|-----------------------|
| Klasė               | Pridėti failą           |
| Grupuoti               | Failas                  |
| Vieta            | „SharePoint“            |

Daugiau informacijos apie tai, kaip nustatyti reikalingus dokumentų valdymo parametrus ir dokumentų tipus rasite temoje [Dokumentų valdymo konfigūravimas](../../fin-and-ops/organization-administration/configure-document-management.md).

![Dokumentų valdymo dokumento tipo nustatymas](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a>Parametrų nustatymas

Pagrindinius verslo dokumentų valdymo parametrus galite nustatyti puslapyje **Verslo dokumentų parametrai**. Puslapis pasiekiamas tik konkretiems vartotojams. Vartotojai, galintys pasiekti puslapį:

- Vartotojai, kuriems priskirtas **Sistemos administratoriaus** vaidmuo.
- Vartotojai, kuriems priskirtas bet kuris vaidmuo, sukonfigūruotas atlikti pareigą, **Palaikyti verslo dokumentų valdymo parametrus** (AOT pavadinimas **ERBDMaintainParameters**).

Atlikite toliau nurodytą procedūrą, kad nustatytumėte pagrindinius parametrus visiems juridiniams subjektams.

1. Prisijunkite kaip vartotojas, kuriam suteikta prieiga prie puslapio **Verslo dokumentų parametrai**.
2. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Verslo dokumentų valdymas** \> **Verslo dokumentų parametrai**.
3.  Puslapyje **Verslo dokumentų parametrai**, skirtuke **Priedai**, lauke **„SharePoint“ dokumento tipas** apibrėžkite dokumento tipą, kuris turėtų būti naudojamas laikinai saugoti šablonus „Office“ formatais, kol jie redaguojami naudojant „Office“ darbalaukio programas. 

> [!NOTE]
> Šis parametras pasiekiamas tik dokumentų tipams, kurie sukonfigūruoti naudojant „SharePoint“ vietą.

![Verslo dokumentų valdymo parametrų nustatymas](./media/BDM-Overview-BDMSetting.png)

Pasirinktas dokumento tipas yra būdingas įmonei ir bus naudojamas, kai vartotojas dirba su verslo dokumentų valdymu įmonėje, kuriai sukonfigūruotas pasirinktas dokumento tipas. Kai vartotojas dirba su verslo dokumentų valdymu kitoje įmonėje, tas pats pasirinktas dokumento tipas bus naudojamas jei jis nebuvo sukonfigūruotas šiai įmonei. Kai dokumento tipas sukonfigūruotas, jis bus naudojamas vietoje to, kuris pasirinktas lauke **„SharePoint“ dokumento tipas**.

## <a name="configure-access-permissions"></a>Prieigos teisių konfigūravimas

Pagal numatytuosius nustatymus, kai prieiga prie verslo dokumentų valdymo teisių neįgalinta, kiekvienas vartotojas, kuriam suteikta prieiga prie verslo dokumentų valdymo darbo srities, matys visus prieinamus ER sprendimo šablonus. Verslo dokumentų valdymo darbo srityje bus rodomi tik tie šablonai, kurie yra ER formato konfigūracijose ir pažymėti žyme **Verslo dokumentų tipas**.

![ER konfigūracijų puslapis](./media/BDM-Overview-ERFormatTags.png)

Šablonų, prieinamų verslo dokumentų valdymo darbo srityje, sąrašas gali būti apribotas konfigūruojant prieigos teises. Tai svarbu, kai skirtingi šablonai naudojami skirtingų verslo domenų (funkcinių sričių) verslo dokumentams kurti, o jūs norite suteikti konkretiems vartotojams prieigą prie skirtingų šablonų, kad jie galėtų juos redaguoti verslo dokumentų valdymo darbo srityje.

Prieigos prie verslo dokumentų valdymo teises galite nustatyti parinktyje **Prieigos teisių konfigūratorius**. Puslapis pasiekiamas tik toliau nurodytiems vartotojams:

- Vartotojai, kuriems priskirtas **Sistemos administratoriaus** vaidmuo.
- Vartotojai, kuriems priskirtas bet kuris kitas vaidmuo, sukonfigūruotas atlikti pareigą, **Konfigūruoti teises pasiekti verslo dokumentų šablonus redagavimui** (AOT pavadinimas **ERBDTemplatesSecurity**).

Atlikite toliau nurodytą procedūrą, kad nustatytumėte prieigos prie verslo dokumentų valdymo teises visiems juridiniams subjektams.

1. Prisijunkite prie kaip vartotojas, kuriam suteikta prieiga prie puslapio **Prieigos teisių konfigūratorius**.
2. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Verslo dokumentų valdymas** \> **Valdyti prieigos teises**.

Atkreipkite dėmesį į pranešimą, kuris informuoja, kad prieigos prie verslo dokumentų valdymo teisių naudojimas šiuo metu neįjungtas.

![Verslo dokumentų valdymo prieigos teisių puslapio konfigūratorius](./media/BDM-Overview-TemplatesAccess1.png)

Pagal šį parametrą kiekvienas vartotojas, kuriam priskirtas bet kuris saugos vaidmuo, sukonfigūruotas atlikti pareigą **Verslo dokumentų šablonų valdymas** (AOT pavadinimas **ERBDManageTemplates**), gali atidaryti verslo dokumentų valdymo darbo sritį ir redaguoti bet kurį prieinamą šabloną.

Toliau pateiktame grafiniame elemente parodyta, kas prieinama verslo dokumentų valdymo darbo srityje vartotojams, kuriems suteiktas **Gautinų sumų klerkas** vaidmuo. Pagal dabartinį prieigos teisių parametrą, vartotojas gali redaguoti skirtingų funkcinių sričių, įskaitant sąskaitos-faktūros išrašymą, teisės aktų nustatytas ataskaitas ir mokėjimus, verslo dokumentų šablonus.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-TemplatesForAlice1.png)

3. Puslapyje **Prieigos teisių konfigūratorius** pasirinkite **Prieigos teisių parametras**.
4. Dialogo lange **Parametrai prieigos teisių šablonų redagavimui** įjunkite parinktį **Taikyti sukonfigūruotas prieigos teises**.
5. Pasirinkite **Gerai**, kad patvirtintumėte, jog verslo dokumentų valdymo prieigos teisės buvo įjungtos.

![Verslo dokumentų valdymo prieigos teisių puslapio konfigūravimas](./media/BDM-Overview-TemplatesAccess2.png)

6. Pasirinkite **Įtraukti**, kad įvestumėte naują verslo vaidmenį, kuriam reikia sukonfigūruoti teises pasiekti verslo dokumentų valdymo šablonus.
7. Dialogo lange **Saugos vaidmenys** pasirinkite vaidmenį **Gautinų sumų klerkas** ir tada pažymėkite **Gerai**, kad patvirtintumėte vaidmens pasirinkimą.
8. Skirtuke **Prieigos teisės konfigūracijų žymėms** pasirinkite **Naujas**.
9. Lauke **Žymės tipas** pasirinkite **Funkcinė sritis**, o lauke **ID** pasirinkite **Sąskaitos-faktūros išrašymas**.
10. Pasirinkite **Įrašyti**, kad išsaugotumėte sukonfigūruotas prieigos teises pasirinktam vaidmeniui.

  Dabartinis parametras reiškia, kad kiekvienam vartotojui, kuriam priskirtas **Gautinų sumų klerkas** vaidmuo ir kuris atlieka pareigą **Verslo dokumentų šablonų valdymas** (AOT pavadinimas **ERBDManageTemplates**), ER formato konfigūracijos šablonai, turintys vertę **Sąskaitos-faktūros išrašymas** žymėje **Funkcinė sritis**, bus prieinami redaguoti verslo dokumentų valdymo darbo srityje.

11. Perjunkite sritį **Susijusi informacija** iš dabartinio puslapio dešinės pusės. Srityje **Susijusi informacija** rodoma, kaip bus taikomos sukonfigūruotos prieigos teisės, taip pat kokie ER konfigūracijų šablonai bus prieinami vartotojams, kuriems priskirtas **Gautinų sumų klerkas** vaidmuo.

![Verslo dokumentų valdymo prieigos teisių puslapio konfigūravimas](./media/BDM-Overview-TemplatesAccess3.png)

12. Skirtuke **Prieigos teisės konfigūracijų žymėms** pasirinkite parinktį **Įtraukti**.
13. Dialogo lange **Pasirinkti konfigūraciją** pažymėkite **Intrastat ataskaita** ER formato konfigūraciją.
14. Pasirinkite **Gerai**, kad patvirtintumėte pasirinktos konfigūracijos įvedimą, o tada pasirinkite **Įrašyti**, kad išsaugotumėte sukonfigūruotas prieigos teises pasirinktam vaidmeniui.

Dabartinis parametras reiškia, kad kiekvienam vartotojui, kuriam priskirtas **Gautinų sumų klerkas** vaidmuo ir kuris atlieka pareigą **Verslo dokumentų šablonų valdymas** (AOT pavadinimas **ERBDManageTemplates**), toliau nurodyti šablonai bus prieinami redaguoti verslo dokumentų valdymo darbo srityje:

- Šablonai, turintys vertę **Sąskaitos-faktūros išrašymas** žymei **Funkcinė sritis**.
- Iš ER formato konfigūracijų sukurti šablonai, kurie išvardyti žymėje **Prieigos teisės konfigūracijoms** (šiame pavyzdyje, šablonai iš **Intrastat ataskaita** formato konfigūracijos domene **Privalomos ataskaitos**).

![Verslo dokumentų valdymo prieigos teisių puslapio konfigūravimas](./media/BDM-Overview-TemplatesAccess4.png)

Toliau pateiktame grafiniame elemente parodyta, ką teikia verslo dokumentų valdymo darbo sritis vartotojui, kuriam suteiktas **Gautinų sumų klerkas** vaidmuo. Pagal dabartinį verslo dokumentų valdymo prieigos teisių parametrą, vartotojas gali redaguoti verslo dokumentų šablonus iš domeno **Sąskaitos-faktūros išrašymas** ir **Intrastat ataskaita** ER formato konfigūracijos. Šablonai iš domeno **Mokėjimai** nepasiekiami vaidmeniui **Gautinų sumų klerkas**.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **Prieigos teisių konfigūracijų** taisyklės saugomos naudojant ER formato konfigūracijos unikalaus identifikavimo ID. Tai reiškia, kad šios taisyklės nebus panaikintos, kai jomis besiremianti ER konfigūracija yra panaikinama. Kai importuojate panaikintas konfigūracijas atgal į šį egzempliorių, šios taisyklės vėl bus joms priskirtos. Nereikia dar kartą nustatyti taisyklių, kai vėl importuojate panaikintas konfigūracijas.

## <a name="use-business-document-management-to-edit-templates"></a>Verslo dokumentų valdymo naudojimas šablonams redaguoti

Verslo vartotojai gali pasiekti verslo dokumentų šablonus, skirtus redaguoti verslo dokumentų valdymo darbo srityje. Tik toliau nurodyti vartotojai gali pasiekti verslo dokumentų valdymo darbo sritį:

- Vartotojai, kuriems priskirtas **Sistemos administratoriaus** vaidmuo.
- Vartotojai, kuriems priskirtas bet kuris vaidmuo, sukonfigūruotas atlikti pareigą, **Valdyti verslo dokumentų šablonus** (AOT pavadinimas **ERBDManageTemplates**).

Atlikite toliau nurodytą procedūrą, kad galėtumėte redaguoti laisvos formos sąskaitos-faktūros šablonus verslo dokumentų valdymo darbo srityje. Prieš įvykdydami šią procedūrą turite būti įvykdę visas ankstesnes šioje temoje pristatytas procedūras.

1. Prisijunkite kaip vartotojas, kuriam suteikta prieiga prie verslo dokumentų valdymo darbo srities.
2. Atidarykite verslo dokumentų valdymo darbo sritį.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-EditingTemplate1.png)

Skirtuke **Šablonas** pristatomas pasirinkto šablono turinys. Pasirinkite skirtuką **Išsami informacija**, kad peržiūrėtumėte išsamią pasirinkto šablono informaciją, taip pat ER formato konfigūracijos, kurioje yra šis šablonas, išsamią informaciją. Atkreipkite dėmesį, kad visi šablonai turi būseną **Paskelbta** ir neturi jokios išsamios informacijos stulpelyje **Tikslinimas**. Tai reiškia, kad šie šablonai šiuo metu neredaguojami.

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Redagavimo šablonų, priklausančių jūsų konfigūracijos teikėjui, iniciavimas

1. Verslo dokumentų valdymo darbo srityje sąraše pasirinkite šabloną **Kvitų spausdinimo formatas**.
2. Pažymėkite skirtuką **Išsami informacija**.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-EditingTemplate2.png)

Pasirinktam šablonui pasiekiama parinktis **Redaguoti šabloną**. Ši parinktis visada pasiekiama ER formato konfigūracijos, priklausančios aktyvios ER konfigūracijos tiekėjui (šiame pavyzdyje – **„Litware, Inc.“**), šablonui. Kai pasirenkate parinktį **Redaguoti šabloną**, galite redaguoti esamą šabloną iš esamo ER formato konfigūracijos juodraščio versijos.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Redagavimo šablonų, priklausančių kitiems teikėjams, iniciavimas

1. Verslo dokumentų valdymo darbo srityje sąraše pasirinkite šabloną **Kliento laisvos formos sąskaitos-faktūros ataskaita (GER)**.
2. Pažymėkite skirtuką **Išsami informacija**.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-EditingTemplate3.png)

Pasirinktam šablonui pasiekiama parinktis **Naujas dokumentas**. Ši parinktis visada pasiekiama ER formato konfigūracijos šablonui, kurį teikia kitas tiekėjas (šiame pavyzdyje – **„Microsoft“**). Kai pasirinktas **Naujas dokumentas**, naują šabloną bus galima redaguoti. Redaguotas šablonas bus išsaugotas naujoje automatiškai sugeneruotoje ER formato konfigūracijoje.

### <a name="start-editing-a-template"></a>Pradėkite redaguoti šabloną

1. Iš pasirinkto šablono pasirinkite **Naujas dokumentas**.
2. Jei reikia, lauke **Pavadinimas** pakeiskite redaguojamo šablono pavadinimą. Tekstas bus naudojamas automatiškai sukurtai ER formato konfigūracijai pavadinti. Atkreipkite dėmesį, kad šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**), kurioje bus suredaguotas šablonas, juodraščio versija bus automatiškai pažymėta vykdyti šį ER formatą dabartiniam vartotojui. Tuo pat metu, nemodifikuotas originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas šiam bet kuriam kitam vartotojui skirtam ER formatui vykdyti.
3. Lauke **Pavadinimas** pakeiskite automatiškai sukurto redaguojamo šablono pirmo pataisymo pavadinimą.
4. Lauke **Komentaras** pakeiskite redaguojamo šablono automatiškai sukurto pataisymo pastabą.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-EditingTemplate4.png)

5. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

Bus atidarytas puslapis **BDM šablono redaktorius**. Pasirinktą šabloną bus galima redaguoti internetu naudojant „Office 365“.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a>Šablono redagavimas naudojant „Office 365“

Modifikuokite šabloną naudojant „Office 365“ funkciją. Pavyzdžiui, programoje „Office Online“ pakeiskite lauko raginimų šablono antraštėje šriftą iš **Paprastasis** į **Paryškintasis**. Šie pakeitimai automatiškai saugomi šiam redaguojamam šablonui, kuris saugomas pirminėje šablono saugykloje (pagal numatytuosius nustatymus – „Azure“ didelių dvejetainių objektų saugykloje), kuri konfigūruojama ER sistemai.

![Verslo dokumentų valdymo šablonų redaktoriaus puslapis](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a>Šablono redagavimas „Office“ darbalaukio programoje

1. Pasirinkite parinktį **Atidaryti darbalaukio programoje**, kad modifikuotumėte šabloną naudojant „Office“darbalaukio programų (šiame pavyzdyje – „Excel“) funkciją. Redaguojamas šablonas nukopijuojamas iš nuolatinės saugyklos į laikiną saugyklą, sukonfigūruotą verslo dokumentų valdymo parametruose kaip „SharePoint“ aplankas.
2. Patvirtinkite, kad norite atidaryti šabloną iš laikinos failų saugyklos „Office“ darbalaukio „Excel“ programoje.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-EditingLayout3.png)

3. Modifikuokite šabloną. Pavyzdžiui, programoje „Office Online“ pakeiskite laukų raginimų šablono antraštėje šriftą pakeisdami spalvą iš **Juoda** į **Mėlyna**.

![Verslo dokumentų valdymo šablonų redaktoriaus puslapis](./media/BDM-Overview-EditingLayout4.png)

4. Pasirinkite **Įrašyti** „Excel“ darbalaukio programoje, kad įrašytumėte šablono pakeitimus laikinoje saugykloje.

![Verslo dokumentų valdymo šablonų redaktoriaus puslapis](./media/BDM-Overview-EditingLayout5.png)

5. Uždarykite „Excel“ darbalaukio programą.
6. Pasirinkite **Sinchronizuoti išsaugotą kopiją**, kad sinchronizuotumėte laikiną šablonų saugyklą į nuolatinę šablonų saugyklą.

> [!NOTE]
> Redaguojamo šablono kopija saugoma laikinoje failų saugykloje tik šablono redagavimo dabartinio seanso metu. Kai baigiate seansą uždarydami puslapį **BDM šablono redaktorius**, ši kopija panaikinama. Jei pakoregavote šabloną laikinoje failų saugykloje ir nepasirinkote **Sinchronizuoti išsaugotą kopiją**, kai bandysite uždaryti puslapį **BDM šablono redaktorius**, iššoks pranešimas, klausiantis ar norite išsaugoti pristatytus pakeitimus. Pasirinkite **Taip**, jei norite išsaugoti pakeitimus šablonui nuolatinėje failų vietoje.

### <a name="validate-a-template"></a>Šablono tikrinimas

1. Puslapyje **BDM šablono redaktorius** pasirinkite **Ieškoti problemų**, kad patikrintumėte modifikuotą šabloną pagal esamą ER formato konfigūraciją. Sekite rekomendacijas (jei yra), kad sulygiuotumėte šabloną su formato struktūra iš pagrindinės ER formato konfigūracijos.
2. Pasirinkite **Rodyti formatą**, kad peržiūrėtumėte dabartinę formato struktūrą iš pagrindinės ER formato konfigūracijos, kuri turi būti sulygiuota su redaguojamu šablonu. 
3. Norėdami uždaryti sritį, pasirinkite **Slėpti formatą**.

![BDM BDM šablono redaktoriaus puslapis](./media/BDM-Overview-EditingTemplate6.png)

4. Uždarykite puslapį **BDM šablono redaktorius**.

Atnaujintas šablonas rodomas skirtuke **Šablonas**. Atkreipkite dėmesį, kad redaguojamo šablono būsena dabar yra **Juodraštis** ir dabartinis pataisymas nebėra tuščias. Tai reiškia, kad šio šablono redagavimo procesas prasidėjo.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Modifikuoto šablono testavimas 

1. Programoje įmonę pakeiskite į **USMF**.
2. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
3. Pasirinkite sąskaitą-faktūrą **FTI-00000002**, o tada pasirinkite **Spausdinimo valdymas**.
4. Pasirinkite lygį **Modulis – gautinos sumos** \> **Dokumentai** \> **Laisvos formos sąskaitos-faktūra** \> **Originalus dokumentas**, kad nurodytumėte apdorojimui skirtų sąskaitų-faktūrų aprėptį.
5. Lauke **Ataskaitos formatas** pasirinkite **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija** ER formatą nurodytam dokumento lygiui.

![Spausdinimo valdymo parametro puslapis](./media/BDM-Overview-TestRun1.png)

6. Norėdami uždaryti dabartinį puslapį, paspauskite **Išeiti**.
7. Pasirinkite **Spausdinti**, o tada spustelėkite **Pasirinkta**.
8. Atsisiųskite dokumentą ir jį atidarykite naudojant „Excel“ darbalaukio programą.

![Laisvos formos sąskaitos-faktūros puslapis](./media/BDM-Overview-TestRun2.png)

Modifikuotas šablonas naudojamas pažymėtos prekės laisvos formos sąskaitos-faktūros ataskaitai generuoti. Norėdami išanalizuoti, kaip šią ataskaitą paveikė jūsų pristatyti šablono pakeitimai, galite vykdyti šią ataskaitą viename programos seanse iš karto po to, kai modifikavote šabloną kitame programos seanse.

### <a name="create-an-alternative-template-revision"></a>Alternatyvaus šablono pataisymo kūrimas

1. Atidarykite puslapį **BDM šablono redaktorius** ir pasirinkite šabloną **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**.
2. Skirtuke **Pataisymai** pasirinkite **Naujas**.
3. Jei reikia, lauke **Pavadinimas** pakeiskite antro pataisymo pavadinimą ir pagrįsite jį šiuo metu aktyviu pirmu pataisymu.
4. Jei reikia, lauke **Komentaras** pakeiskite redaguojamo šablono automatiškai sukurto pataisymo pastabą.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-AddRevision.png)

Sukūrėte naują šablono pataisymą, kuris buvo išsaugotas nuolatinėje šablono saugykloje. Dabar galite tęsti antro pataisymo, kuris šiuo metu pažymėtas kaip aktyvus, šablono redagavimą.

5. Pasirinkite pirmą pataisymą, o tada pasirinkite **Nustatyti kaip aktyvų**. Galite pasirinkti kitą pataisymą kaip aktyvų jei kuriuo nors metu norėsite grąžinti tą šablono pataisymą.
6. Pasirinkite antrą pataisymą ir tada pasirinkite **Naikinti**.
7. Norėdami patvirtinti, kad norite panaikinti pažymėtą pataisymą, pasirinkite **Gerai**. Galite panaikinti bet kurį neaktyvų pataisymą, kai jis nebereikalingas.

### <a name="delete-a-modified-template"></a>Modifikuoto šablono naikinimas

1. Puslapyje **BDM šablono redaktorius** pasirinkite skirtuką **Šablonas**.
2. Pasirinkite **Naikinti**.
3. Jei pasirenkate **Gerai**, kad patvirtintumėte naikinimą, ER formatas **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija** su modifikuotu šablonu bus panaikinti. Norėdami peržiūrėti kitas parinktis, pasirinkite **Atšaukti**.

### <a name="revoke-changes-of-template"></a>Šablono pakeitimų atšaukimas

Kai redaguojate šabloną iš ER formato, priklausančio dabartiniam aktyviam tiekėjui, jums bus suteikta galimybė atšaukti šablonui pristatytus pakeitimus.

![Verslo dokumentų valdymo darbo srities puslapis](./media/BDM-Overview-RevokeChanges.png)

1. Puslapyje **BDM šablono redaktorius** pasirinkite skirtuką **Šablonas**.
2. Pasirinkite **Anuliuoti**.
3. Jei pasirenkate **Gerai**, kad atšauktumėte šablonui pristatytus pakeitimus, modifikuotas šablonas bus pakeistas originaliu šablonu, o visi pakeitimai bus pašalinti. Kai atšaukiate šablono pakeitimus, galėsite ištrinti šabloną. Norėdami peržiūrėti kitas parinktis, pasirinkite **Atšaukti**.

### <a name="publish-a-modified-template"></a>Modifikuoto šablono publikavimas
1. Puslapio **BDM šablono redaktorius** skirtuke **Šablonas** pasirinkite **Publikuoti**.
2. Jei pasirenkate **Gerai**, kad patvirtintumėte publikavimą, išvestinio ER formato **Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija** juodraščio versija, kurioje yra modifikuotas šablonas, bus pažymėta kaip užbaigta. Modifikuotas šablonas taps pasiekiamas kitiems vartotojams. Užbaigtose šio ER formato versijose liks tik paskutinis aktyvus jūsų šablono pataisymas. Kiti pataisymai bus panaikinti. Norėdami peržiūrėti kitas parinktis, pasirinkite **Atšaukti**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

#### <a name="i-selected-new-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>Pasirinkau parinktį **Naujas dokumentas**, tačiau vietoje puslapio **BDM šablono redaktorius** atidarymo programoje „Finance and Operations“, atsidarė „Office 365“ tinklalapis.
Tai žinoma problema su „Office 365“ peradresavimu. Tai atsitinka, kai pirmą kartą prisijungiate prie „Office 365“. Norėdami išspręsti šią problemą, pasirinkite naršyklės mygtuką **Atgal**, kad grįžtumėte atgal.

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>Aš suprantu, kaip redaguoti šabloną naudojant „Office 365“ pirmame programos seanse ir kaip naudoti šabloną antrame programos seanse koreguojant šabloną, kad pamatyčiau, kaip pakeitimai paveikia sugeneruotą verslo dokumentą. Ar galiu tai atlikti naudojant „Office“ darbalaukio programą?
Taip, galite. Pirmame programos seanse pasirinkite **Atidaryti darbalaukio programoje**. Jūsų šablonas bus išsaugotas laikinoje failų saugykloje ir atidarytas „Office“ darbalaukio programoje. Tada atlikite toliau nurodytus veiksmus, kad peržiūrėtumėte jūsų šablono pakeitimus sugeneruotame verslo dokumente:

1. Atlikite šablono pakeitimus naudojant „Office“ darbalaukio programą.
2. „Office“ darbalaukio programoje pasirinkite **Įrašyti**.
3. Pirmo programos seanso puslapyje **BDM šablono redaktorius** pasirinkite **Sinchronizuoti išsaugotą kopiją**.
4. Vykdykite šio šablono ER formatą antrame programos seanse.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>Man rodoma klaida „Reikšmė negali būti nulinė“. Parametro pavadinimas: „externalId’“, kai pasirenku **Atidaryti darbalaukio programoje**. Kaip galiu tai išspręsti? 
Tikėtina, kad prisijungėte prie dabartinio „Azure AD“ domeno programos egzemplioriaus, kuris skiriasi nuo „Azure AD“ domeno, kuris buvo naudojamas diegiant šį egzempliorių. Kadangi „SharePoint“ paslauga, naudojama šablonams saugoti, kad jie būtų prieinami redagavimui naudojant „Office“ darbalaukio programas, priklauso tam pačiam domenui, mes neturime teisių pasiekti „SharePoint“ paslaugą. Norėdami išspręsti šią problemą, prisijunkite prie dabartinio egzemplioriaus naudodami vartotojo kredencialus tinkamame „Azure AD“ domene.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](tasks/er-design-reports-openxml-2016-11.md)

[ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu](tasks/er-design-configuration-word-2016-11.md)

[Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md)

[Įrankio Elektroninės ataskaitos konfigūravimas duomenims perkelti į „Power BI“](general-electronic-reporting-report-configuration-get-data-powerbi.md)
