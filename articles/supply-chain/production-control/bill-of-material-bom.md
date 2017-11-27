---
title: "KS ir formulės"
description: "Šioje temoje pateikiama informacija apie KS ir formules, kurios yra svarbi produktų ir produktų variantų aprašų dalis."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 430e2ab0c4438222ceb9102c011940af803acfbc
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="bills-of-materials-and-formulas"></a>KS ir formulės

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie KS ir formules, kurios yra svarbi produktų ir produktų variantų aprašų dalis. KS ir formulės nurodo reikiamas konkretaus produkto medžiagas arba sudedamąsias dalis. Formulės taip pat nurodo sudėtinius produktus arba šalutinius produktus, kurie gauname konkrečiame gamybos kontekste. 

<a name="bills-of-materials"></a>Komplektavimo specifikacijos
------------------

Komplektavimo specifikacija (KS) apibrėžia komponentus, kurių reikia norint pagaminti produktą. Komponentai gali būti žaliavos, pusiau baigti produktai arba ingredientai. Kai kuriais atvejais KS specifikacijoje gali būti nurodoma į paslaugas. Tačiau paprastai KS specifikacijose apibūdinami reikalingi *medžiagų ištekliai*.  

Kai KS sujungta su maršrutu ar gamybos eiga, kuriais aprašomos operacijos ir ištekliai, reikalingi norint sukurti produktą, KS sudaro įvertintų produkto išlaidų skaičiavimo pagrindą.  

KS yra atskiras objektas, kurį apibūdina tolesnė informacija.

-   BOM ID.
-   KS pavadinimas
-   KS eilutės, kurios apibūdina komponentus ir ingredientus.
-   KS versijos, kurios apibrėžia produktą ir laikotarpį, su kuriais KS gali būti naudojama.

Viena KS apibūdina vieną lygį, kuris identifikuojamas pagal unikalų ID. Komponentai gali turėti savo KS, į kurias nurodo KS versijos. KS konstruktoriuje galite rodyti ir redaguoti visą konkretaus produkto KS hierarchiją.

### <a name="formulas-co-products-and-by-products"></a>Formulės, sudėtiniai produktai ir šalutiniai produktai

Formulė yra KS potipis, paprastai naudojama proceso gamyboje. Be komponentų ir ingredientų, formulė apibūdina sudėtinius produktus ir šalutinius produktus. Faktinėje versijoje norint apibrėžti formulės sudėtinius produktus ir šalutinius produktus, reikia formulės versijos. Paprastai apibrėžiama vieno konkretaus galutinio produkto (formulės ar planavimo prekės), apibrėžto formulės versijoje, formulė.

### <a name="boms-in-the-product-lifecycle"></a>KS specifikacijos produkto cikle

Produkto cikle dėl įvairių priežasčių galima kurti įvairių tipų KS.

-   **Eskizinė / juodraščio KS** – šioje KS pradiniame kūrimo etape pateikiamas reikalingų medžiagų įvertinimo juodraštis, ir ši KS padeda apytikriai įvertinti išlaidas ir produktų atributus. Įmonės išteklių planavimo (ERP) modulyje ši KS paprastai nenaudojama.
-   **Inžinerinė KS** – ši KS paprastai naudojama kuriant produktus, paremtus esamais produktų portfeliais. Inžinerinių KS struktūra skirta supaprastinti kūrimo procesui ir sudėtingams produktams grupuoti į inžinerijos modulius. Paprastų produktų KS gali būti įmanoma kurti faktinės gamybos procesui. Tačiau kitų produktų inžinerines KS reikia konvertuoti į faktinės gamybos KS. KS hierarchijoje inžinerines KS paprastai vaizduoja fiktyvios eilutės. Nors inžinerines KS galima naudoti planuojant ir vykdant gamybos operacijas, naudoti šį būdą gali būti neefektyvu, ypač vykdant pasikartojančias operacijas, kai kuriama daug užsakymų.
-   **Planavimo KS** – ši KS naudojama planuoti medžiagų poreikiams. Komponentų ir ingredientų poreikis apskaičiuojamas pagal galutinių produktų poreikį. Kaip ir įkainojimo KS specifikacijos, planavimo KS specifikacijos gali nurodyti konkretų medžiagų mišinį, naudojamą tam tikru laikotarpiu.
-   **Gamybos KS** – tai KS, naudojama konkrečioje gamyboje. Gamybos KS specifikacijoje reikia atsižvelgti į faktinius išteklius, kurie naudojami gaminant produktą. Sukūrus gamybos užsakymą, paketinį užsakymą ar „kanban‟, keli KS specifikacijų lygiai, kuriuos vaizduoja fiktyvios eilutės, sutraukiami į vieną lygį ir paskirstomi užsakymo operacijoms.
-   **Įkainojimo KS** – ši KS naudojama įvertintai produkto savikainai apskaičiuoti. Pvz., įkainojimo KS galite naudoti, kai naudojama standartinė savikaina arba skaičiuojama nurodyto produkto įvertinta suplanuota savikaina. Įkainojimo KS specifikacijos gali nurodyti į planuojamą naudoti konkretų medžiagų ir išteklių mišinį. Todėl įkainojimo KS galite naudoti kurdami reprezentatyvią įvertintą laikotarpio savikainą ir siekdami išvengti per laiką atsirandančių nuokrypių.

Sistemoje faktiškai naudojami KS tipai priklauso nuo diegimo bei verslo scenarijų ir reikalavimų. Paprastuose diegimuose planavimo KS, gamybos KS ir įkainojimo KS galima modeliuoti kaip vieną KS. Aplinkose, kuriose dažni inžineriniai pakeitimai ir keli alternatyvūs maršrutai, tikriausiai reikės įvairesnių KS tipų.

### <a name="approval-of-boms-and-formulas"></a>KS specifikacijų ir formulių patvirtinimas

Galima atskirai patvirtinti arba nepatvirtinti kiekvieną KS ir formulę. Paprastai KS arba formulė patvirtinama, patvirtinus pirmąją aktualią KS versiją. Tačiau kai kuriais verslo scenarijais šie patvirtinimai gali būti skirtingi proceso veiksmai, ir, juos atliekant, gali dalyvauti skirtingi procesų savininkai.  

Atkreipkite dėmesį, kad, jei KS nepatvirtinta, taip pat nepatvirtintos visos susijusios KS versijos.

## <a name="bom-and-formula-versions"></a>KS specifikacijų ir formulių versijos
Norėdami konkrečią KS ar formulę susieti su galimo pagaminti produkto variantu, turite sukurti KS versiją arba formulės versiją. KS versijų ir formulės versijų galiojimą galima apriboti laikotarpiu, kiekiu, teritorija, konkrečiomis produkto dimensijomis ir kitais kriterijais. Formulės versijos turi papildomų svarbių atributų, pvz., išeiga, sudėtinių produktų ir šalutinių produktų apibrėžtys bei formulės išlaidų paskirstymo instrukcijos.

### <a name="approval-of-bom-and-formula-versions"></a>KS ir formulės versijų patvirtinimas

Prieš KS versiją naudojant planavimo ar gamybos procese, ją reikia patvirtinti. Kai KS versija patvirtinama, taip pat galima patvirtinti susijusią KS – tai priklauso nuo naudotojo pasirinkties ir autentifikavimo teisių. Atkreipkite dėmesį, kad KS versiją patvirtinti galima tik jei patvirtinta susijusi KS.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Numatytosios KS ar formulės versijos aktyvinimas

Norėdami konkrečią KS ar formulę nustatyti kaip numatytąją KS versiją ar formulės versiją, kurią naudos bendrasis planavimas arba kuri bus naudojama kuriant gamybos užsakymus, šią versiją turite suaktyvinti. Kai versija suaktyvinama, pagal nurodytus apribojimus (pvz., laikotarpį, teritoriją ar kiekį) patikrinamas versijos unikalumas. Jei versija, kurią mėginate suaktyvinti, nesuderinama su jau aktyvia versija, gaunate klaidos pranešimą. Tada, siekiant išvengti nevienareikšmiško suaktyvinimo, reikia arba išaktyvinti nesuderinamą versiją, arba modifikuoti versijos apribojimus (paprastai laikotarpį).

### <a name="product-change-with-case-management"></a>Produkto keitimas naudojant atvejų valdymą

Produkto keitimo atvejis, skirtas tvirtinti ir aktyvinti naujoms ar pakeistoms KS ir KS versijoms, suteikia lengvą būdą apžvelgti KS versijos apribojimus. Taip pat pagal vieną aktyvinimo datą galite patvirtinti ir aktyvinti visas KS bei formules, susijusias su konkrečiu keitimu.

### <a name="alternative-bom-versions"></a>Alternatyvios KS versijos

Kartais aktyvios KS versijos ar formulės versijos nereikėtų naudoti prognozėse, pardavimuose ar pirminiame produkte. Tokiu atveju, jei egzistuoja patvirtinta alternatyvios KS ar formulės versija, konkrečią patvirtintą KS galite pasirinkti kaip reikalavimo dalį (prognozės eilutės, pardavimo eilutės ar KS eilutės).  

Kai kuriami suplanuoti užsakymai, gamybos užsakymai ar „kanban‟, planuotojas ar darbo laiko prižiūrėtojas gali naudoti bet kokią patvirtintą KS versiją, galiojančią pageidaujamą suplanuotos gamybos dieną ir planuoti ar gaminti konkretų produktą. Naudojamos KS versijos nebūtina suaktyvinti kaip numatytosios KS versijos.

## <a name="bom-and-formula-lines"></a>KS ir formulių eilutės
Sukuriama kiekvienos medžiagos, paslaugos ar ingrediento KS eilutė. Eilutėje apibrėžiamas planuojamas nurodyto produkto varianto naudojimas ir įvairūs atributai, susiję su planuojamu naudojimu.  

KS eilučių tipai gali būti: **Prekės**, **Fiktyvi**, **Iškviesto tiekimo**, **Tiekėjo**.

### <a name="item"></a>Prekė

**Prekių** eilučių tipą parinkite toms medžiagoms ar paslaugoms, kurios naudojamos tiesiogiai ir kurių nereikia labiau išskleisti bei kurioms nereikia iškviesto tiekimo.

### <a name="phantom"></a>Fiktyvus

**Fiktyvių** eilučių tipą pasirinkite, norėdami išskleisti bet kurias žemesniojo lygio KS prekes, esančias KS eilutėje. Atliekant bendrąjį planavimą, skaičiuojant suplanuotą savikainą ar vertinant gamybos užsakymą, kuriame naudojamas **Fiktyvių** KS eilučių tipas, pirminę KS eilutę, kuri nurodo į produkto variantą, turintį fiktyvią KS, pakeičia sudedamosios prekės, kurios toje KS išvardytos kaip KS eilutės, kaip nustato taikytina aktyvi to produkto varianto KS versija. Jei produkto variantas turi taikytiną aktyvų maršrutą, to maršruto operacijos suliejamos į pirminį maršrutą.  

Atkreipkite dėmesį, kad fiktyvios eilutės paprastai naudojamos palengvinti inžinerijos procesui. Plačiai daugeliu lygių naudojant fiktyvias KS, paveikiamas našumas, ypač dažnai pasikartojančiais gamybos scenarijais. Norėdami našumą pagerinti, turėtumėte vengti gilių fiktyvių eilučių hierarchijų. Geriau naudokite iš anksto išskleistas gamybos KS ir maršrutus.

### <a name="pegged-supply"></a>Iškviestas tiekimas

**Iškviesto tiekimo** eilučių tipą pasirinkite, kai norite sukurti tarpinę gamybą, KS eilutės įvykio „kanban‟ arba bet kurio produkto varianto, į kurį nurodo KS eilutė, tiesioginį pirkimo užsakymą. Tarpinė gamyba, įvykio „kanban‟ arba pirkimo užsakymas sukuriami įvertinant gamybos užsakymą. Reikiami prekių kiekiai automatiškai rezervuojami naudojimo gamybos užsakymui.

### <a name="vendor"></a>Tiekėjas

Pasirinkite **Tiekėjo** eilučių tipą, jei gamybos procese dalyvauja subrangovas ir norite automatiškai subrangovui sukurti tarpinę gamybą arba pirkimo užsakymą.  

**Pastaba apie KS subrangos operacijas.** Paslaugą ar darbą, kurį atlieka subrangovas, reikia sukurti kaip aptarnavimo prekę, sekamą atsargose. Aptarnavimo prekę kaip KS eilutę turite pridėti prie pirminės prekės. Maršrute turi būti operacija, priskirta subrangovo operacijų ištekliui.




