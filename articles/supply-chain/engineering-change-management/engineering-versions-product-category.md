---
title: Inžinerijos versijos ir inžinerijos produkto kategorijos
description: Šioje temoje pateikta informacija apie inžinerijos versijų sąvoką. Inžinerijos versijos užtikrina, kad kitos produkto būsenos ir jo duomenys yra laikomi dabar ir aiškiai ir kad jos gali būti rodomos sistemoje.
author: t-benebo
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a4d057c603e6592e491af7597e50fce2497860ec
ms.sourcegitcommit: b96e0c70553bca9b3f5eb65105a52cb71d978a36
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2022
ms.locfileid: "8553368"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Inžinerijos versijos ir inžinerijos produkto kategorijos

[!include [banner](../includes/banner.md)]

Inžinerijos produktai vystosi jų produkto gyvavimo cikle dėl daugelio priežasčių. Pavyzdžiui, keitimai gali būti įtraukti siekiant pagerinti produkto aptinkamumą, keisti komponentą dėl to, kad tiekėjas jo nebesiūlo, atsakymo į naujas įžvalgas ar taisymo klaidas pradiniame kūrinyje. Taip pat yra daug priežasčių, kodėl šie keitimai turi būti talpinami kaip einamojo produkto dalis, tokiu būdu, kad ankstesni duomenys nebūtų užrašyti. Štai keletas priežasčių:

- Norite sekti produktą, nes jis buvo pagamintas ir pristatytas jūsų klientams ankstesnio gyvavimo ciklo būsenų.
- Jums reikia pagrindinio laiko prieš tai, kai bus patvirtinti ir pritaikyti keitimai.
- Norite turėti laiko atkarpą kiekvienam keitimui ir norite galėti pristatyti anksčiau sukurtus produktus atskirai vienas nuo kito.

*Inžinerijos versijos* užtikrina, kad skirtingos produkto būsenos ir jo duomenys yra laikomi dabar ir aiškiai ir kad jos gali būti rodomos sistemoje. Ši sąvoka padeda išlaikyti nuoseklumą, užrakinti komplektavimo specifikaciją (KS) gamybai, eliminuoti kintamumą ir paprastai nustatyti pakeitimus.

Bendrai, taisyklė *forma atitinka funkciją* taikoma siekiant nustatyti, ar keitimui reikia naujo produkto, naujos versijos ar naujinimo esančiai versijai. Bet kuri iš trijų sąvokų šios taisyklės pavadinime reiškia konkretų dalies aspektą, kuris padeda inžinieriams sujungti reikiamas dalis. Formos atitikimo funkcijos taisyklė padidina kūrimo pokyčių lankstumą, nes mažiausiai dokumentai ir dizaino kaštai būtini norint pakeisti dalį, su sąlyga, kad produkto atitiktis, forma ir funkcija yra išlaikytos.

- **Atitiktis** reiškia dalies ar funkcijos galimybę susijungti tarpusavyje, susilieti ar susijungti su kita funkcija ar dalimi rinkinyje. Susijungimas leidžia daliai atitikti reikiamas rinkinio paklaidas taip, kad ji galėtų būti naudinga.
- **Forma** reiškia dalies ar rinkinio savybes, tokias kaip išorės dimensijos, svoris, dydis ir išvaizda. Forma yra aspektas, kurį dažniausiai veikia inžinerijos estetiniai pasirinkimai. Ji apima struktūrą, korpusą ir valdymo skydelį, kuris tampa produkto išorės „veidas“.
- **Funkcija** yra kriterijus, kuris atitinka, kai dalis efektyviai ir patikimai atlieka savo tikslą. Pavyzdžiui, elektroniniuose produktuose, funkcija gali priklausyti nuo solidžios būsenos komponentų, kurie naudojami ir programinės įrangos bei ugniasienės. Dažnai, jis taip pat priklauso nuo pasirinktos struktūros funkcijų. Du iš dažniausiai pasitaikančių priežasčių, kurių struktūrai gali nepavykti funkcijos kriterijai netinkamai padėti ar netinkamo dydžio prievadai bei netikslus ar trūkstamas ženklinimas. 

## <a name="engineering-versions"></a>Inžinerinės versijos

Jums naudojant inžinerinius produktus, kiekvienas produktas turi mažiausiai vieną inžinerijos versiją. Pradinė inžinerijos versija automatiškai sukuriama jums sukuriant inžinerijos produktą. Kiekviena inžinerijos versija talpina su inžinerija susijusius duomenis, kurie konkretūs tai versijai. Čia pateikiami keli šių duomenų pavyzdžiai:

- Versijos skaičius ir ankstesnės versijos skaičius (jei taikomas)
- Efektyvi forma ir efektyvi datoms
- Produkto versijos aktyvi būsena, kuri rodo, ar versija gali būti išleista ir naudojama perlaidose (Dėl daugiau informacijos, žr. [Produkto parengimas](product-readiness.md).)
- Inžinerijos bendrovė, kuri sukūrė ir turi produktą (Dėl daugiau informacijos, žr. [Inžinerijos įmonės ir duomenų turėjimo taisyklės](engineering-org-data-ownership-rules.md).)
- Susiję inžinerijos dokumentai, kurie yra rinkinio rankinis, vartotojo instrukcijos, paveikslėliai ir nuorodos
- Inžinerijos atributai (Dėl daugiau informacijos, žr. [Inžinerijos atributai ir inžinerijos atributų paieška](engineering-attributes-and-search.md).)
- Inžinerinių produktų komplektavimo specifikacija (KS)
- Produktų gamybos proceso formulės
- Inžineriniai maršrutai

Galite naujinti šiuos duomenis esančioje versijoje arba sukurti naują naudodami *inžinerijos keitimo užsakymas*. (Dėl daugiau informacijos, žr. [Valdyti keitimus inžineriniams produktams](engineering-change-management.md).) Jei sukuriate naują produkto versiją, sistema kopijuoja visus su inžinerija susijusius duomenis į tą naują versiją. Galite tada keisti naujos versijos duomenis. Tokiu būdu, galite stebėti konkrečius duomenis kiekvienai paskesnei versijai. Norėdami palyginti skirtumus tarp inžinerinių versijų, peržiūrėkite inžinerinių keitimų užsakymą, kuris apima keitimo tipus, rodančius visus keitimus.

Kaip buvo pasakyta, pradinė inžinerijos versija automatiškai sukuriama jums sukuriant inžinerijos produktą. Versijos numeris šiai versijai atitinka versijos numerio taisyklę, kuri nustatyta inžinerijos produkto kategorijoje. Norėdami perduoti tolesnę versiją, privalote įtraukti produktą į inžinerijos keitimo užsakymą kaip eilutę ir privalote nustatyti **Poveikio** laukelį į *Nauja versija*. Inžinerijos keitimo užsakymas apims išsamią keitimo informaciją iš esamos versijos į kitą versiją.

Atminkite, kad inžinerijos produktas gali būti tik viename inžinerijos keitimo užsakyme vienu metu. Apribojimas užtikrina duomenų tikslumą ir padeda išvengti persidengimo ar prieštaraujančių produkto keitimų. Taip pat, atminkite, kad **Inžinierius** laukelyje **Antraštėje** inžinerinių pokyčių užsakymas rodo inžinierių, kuris yra atsakingas už keitimo užsakymą. Jei inžinierius priklauso komandai, kuri nustatyta sistemoje, laukelis **Atsakingas** rodo tos komandos lyderį.

## <a name="track-versions-in-transactions"></a>Sekti versijas perlaidose

Jums naudojant inžinerijos keitimo valdymą, jūsų produkto pagrindiniai duomenys visada apima vieną ar daugiau inžinerijos versijų. Jūsų inžinerijos produktų nustatyme, galite rinktis, ar inžinerijos versija yra taip pat *logistinių perlaidų* dalis. (Dėl daugiau informacijos, žr. [Nustatyti inžinerijos produkto kategorijų](#product-category) skyrių toliau šioje temoje.) Jei logistikos poveikis yra svarbus, jis skiriasi pagal produktą ir priklausomai nuo bendrovės. Kartais yra naudojama tik naujausia produkto versija. Dėl to, jums pristatant naują versiją, ankstesnė versija nebegali būti naudojama. Kitais atvejais, ankstesnė versija yra būtina logistinėse perlaidose siekiant įveikti tolesnius iššūkius:

- Logistikos skyrius turi išsiųsti du vienetus produkto klientui. Tokiu atveju, turite nuspręsti, ar norite ar leisti siųsti dvi versijas.
- Vėliau suprantama, kad problema įvyko ir ji susijusi su konkrečiu keitimu. Tokiu atveju, gali būti naudinga nuspręsti tiksliai, kuri versija buvo išsiųsta kuriame užsakyme.
- Bendrovės dažniausiai nori siųsti senąją versiją pirma siekiant suderinti inventorių. Ypač mažo kiekio produktams toks elgesys dažnai gali būti atliekamas siekiant nustatyti naujos versijos efektyvias datas susijusias su spėjimais apie tada, kai senoji atsargų versija bus panaikinta. Nepaisant to, kartais jums gali reikėti atlikti palyginimą arba galite pagalvoti apie atsargų lygio spėjimų netikrumą.

Sprendimas apie tai, ar padaryti versijas matomas inventoriuje priklauso nuo faktorių, tokių kaip tie, kurie anksčiau paminėti, kartu bendrovės praktika ir kiti svarstymai, kurie yra konkretūs kiekvienai bendrovei. Galite nurodyti elgesį *inžinerijos produkto kategorijai*. Jis bus tuomet taikomas visiems produktams sukurtiems iš tos kategorijos, visoms bendrovėms, kurioms išleistas produktas.

Nustatytiems produktams taip, kad jie turėtų logistinį poveikį, inžinerijos versijos turi būti nurodytos kiekvienoje perlaidoje. Nepaisant to, kad sistema siūlo *naujausią veikiančią versiją*, galite pasirinkti iš visų veikiančių versijų, prieinamų bendrovei. Nustatytiems produktams taip, kad jie neturėtų logistinio poveikio, inžinerijos versijos neturi būti nurodytos kiekvienoje perlaidose. Nepaisant to, sistema naudoja naujausią veikiančią versiją. Pavyzdžiui, kai įtraukiate produktą į gamybos KS, naujausia versija bus naudojama ir tada vykdote pagrindinį planavimą, naujausia versija bus naudojama.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Nustatykite inžinerijos produkto kategorijas

Inžinerijos produkto kategorija pateikia pagrindus siekiant sukurti konkretų inžinerijos produktą. Kiekviena kategorija įsteigia numatytų verčių ir politikų rinkinį. Dėl to, jums kuriant inžinerijos produktą, pirmiausia pasirinkite kategoriją, iš kurios kuriate.

Įsidėmėkite, kad naujas kategorijos hierarchijos tipas (*inžinerinio produkto hierarchija*) jums yra automatiškai nustatomas. Galite rankiniu būdu sukurti kategorijas patekę į **Inžinerijos keitimo valdymas \> Nustatymai \> Inžinerijos produkto kategorijos išsami informacija**.

Kiekviena inžinerijos produkto kategorija nustato numatytąjį elgesį inžineriniams produktams, kurie buvo sukurti tai kategorijai. Jums sukūrus inžinerijos produktą, negalite keisti jo kategorijos. Nepaisant to, jei pasirinkote netinkamą kategoriją, galite panaikinti produktą ir jį sukurti iš naujo.

Sukūrus inžinerinio produkto kategoriją, esate apsaugoti nuo šių nustatymų keitimo:

- Inžinerijos bendrovė
- Produkto tipas
- Produkto potipis
- Produkto dimensijų grupė
- Konfigūracijos technologija
- Versijos numerio taisyklė

Kiti nustatymai gali paveldėti nustatytąsias vertes, kurios yra nustatytos inžinerinio produkto kategorijai. Nepaisant to, pagal sistemos taisykles, tos vertės gali kisti.

Norėdami dirbti su inžinerinio produkto kategorijomis, eikite į **Inžinerijos keitimo valdymas \> Nustatymai \> Inžinerijos produkto kategorijos išsami informacija**. Tuomet atlikite vieną iš šių žingsnių.

- Norėdami sukurti naują kategoriją, rinkitės **Naujas** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami redaguoti esančią kategoriją, sąrašo juostoje ją pasirinkite ir rinkitės **Redaguoti** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami panaikinti kategoriją, sąrašo juostoje ją pasirinkite ir rinkitės **Naikinti** veiksmų juostoje.

### <a name="header"></a>Antraštė

Nustatykite tolesnius laukelius inžinerinio produkto kategorijos antraštėje.

| Laukas | Aprašas |
|---|---|
| Pavadinimas | Įveskite inžinerinio produkto kategorijos pavadinimą. |
| Inžinerijos bendrovė | Pasirinkite inžinerijos bendrovę, kurioje produktai šioje inžinerijos produkto kategorijoje gali būti sukurti ir kur jie turi būti laikomi. |

### <a name="details-fasttab"></a>Išsamios informacijos „FastTab“

Nustatykite tolesnius laukelius **Išsamios informacijos** „FastTab“ inžinerinio produkto kategorijoje.

| Laukas | Aprašas |
|---|---|
| Produkto tipas | Pasirinkite, ar kategorija taikoma produktams ar paslaugoms. |
| Gamybos tipas | Šis laukas pasirodys tik tada, kai įgalinsite [formulių keitimo valdymą](manage-formula-changes.md) savo sistemoje. Pasirinkite gamybos, kuriai taikoma ši inžinerijos produktų kategorija, tipą:<ul><li>**Prekės planavimas** – Naudokite šią inžinerijos kategoriją planavimo prekių formulių keitimo valdymui atlikti. Prekių planavimui naudojamos formulės. Jos yra panašios į sudėtines prekes, tačiau jos naudojamos tik sudėtiniams ir šalutiniams, bet ne baigtiems produktams gaminti. Formulės yra naudojamos gamybos proceso metu.</li><li>**KS** – Naudokite šią inžinerijos kategoriją inžinerijos produktų, nenaudojančių formulių ir įprastai (tačiau nebūtinai) turinčių KS, valdymui.</li><li>**Formulė** – Naudokite šią inžinerijos kategoriją baigtų produktų formulių keitimo valdymui atlikti. Šios prekės turės formulę, bet ne KS. Formulės yra naudojamos gamybos proceso metu.</li></ul> |
| Esamas svoris | Ši parinktis pasirodys tik tada, kai įgalinsite [formulių keitimo valdymą](manage-formula-changes.md) savo sistemoje. Ji galima tik tada, kai **Gamybos tipo** laukas nustatytas į *Prekės planavimas* arba *Formulė*. Nustatykite šią pasirinktį į *Taip*, jei šią inžinerijos kategoriją naudosite prekėms, kurioms reikalingas esamo svorio palaikymas, valdyti. |
| Sekti versijas perlaidose | Pasirinkite, ar produkto versija turi būti su antspaudu visose perlaidose (logistinis poveikis). Pavyzdžiui, jei sekate versiją perlaidose, visi prekybos užsakymai rodys, kurie konkreti produkto versija buvo parduota tame prekybos užsakyme. Jei nesekate versijos perlaidose, visi prekybos užsakymai nerodys, kuri konkreti produkto versija buvo parduota. Vietoje to, jie visada rodys naujausią versiją.<ul><li>Jei ši parinktis nustatyta į *Taip*, produkto pagrindiniai duomenys sukruti produktui ir kiekviena produkto versija bus variantas naudojantis *versijos* produkto matmenis. **Laukelis Produkto potipis automatiškai nustatomas į** Pagrindinį produktą *ir* Produkto matmenų grupės laukelyje turite įvesti **produkto** matmenų grupę, kurioje *versijos* matmenys įjungti. Tik produkto matmenų grupės, kuriose *versija* yra įjungti matmenys bus rodoma. Galite sukurti naują produkto matmenų grupę pasirinkę **Redaguoti** mygtuką (pieštuko simbolis).</li><li>Jei ši parinktis nustatyta į *Ne*, tai *versijos* produkto matmenys nebus naudojami. Tuomet galite pasirinkite, ar sukurti produktą ar pagrindinį produktą, kuris naudos kitus matmenis.</li></ul><p>Ši parinktis dažnai naudojama produktams, kurie turi kaštų skirtumus tarp versijų arba produktams, kuriems taikomos skirtingos sąlygos dėl klientų. Dėl to, svarbu nurodyti, kuri versija buvo naudojame konkrečioje perlaidoje.</p> |
| Produkto potipis | Pasirinkite, ar kategorija turės produktus ar pagrindinį produktą. Pagrindiniam produktui, jo matmenys bus naudojami.
| Produkto dimensijų grupė | Nustatymai **Sekti versijas perlaidose** nustatymai padeda jums parinkti dimensijos grupę. Jei nustatėte, kad norite sekti versijas perlaidose, produkto dimensijos grupės, kuriose *versija* dimensija naudojama bus rodomos. Kitu atveju, tik produkto dimensijos grupės, kai *versija* dimensija nėra naudojama, bus rodomos. |
| Produkto ciklo būsena kūrimo metu | Nustatykite numatytąjį produkto gyvavimo ciklo būseną, kurią inžinerijos produktas turi turėti, kai tik bus sukurtas. Dėl daugiau informacijos, žr. [Produkto gyvavimo ciklo būsenos ir perlaidos](product-lifecycle-state-transactions.md). |
| Versijos numerio taisyklė | Pasirinkite versijos numerio taisyklę, taikomą kategorijai:<ul><li>**Rankinė** – Pasirenkate versijos numerį kiekvienai naujai versijai.</li><li>**Automatinė** – Sistema nustato versijos numerį pagal jūsų nustatytą formatą. Jums nustačius formatą, naudokite skaičiaus ženklą (\#) norėdami parodyti skaitmenį ar bet kurį kitą ženklą nuolatinei vertei. Pavyzdžiui, jei nurodote formatą kaip *V-\#\#*, pirmoji versija bus "V-01," antroji versija bus "V-02“ ir taip toliau.</li><li>**Sąrašas** – Sistema paima kitą skaičių iš nustatyto sąrašo tinkintoms vertėms, kurį nustatėte.</li></ul> |
| Vykdyti galiojimo taisykles | Pasirinkite, ar efektyvumo datos inžinerinėms versijoms turi būti nuolatinės ar gali būti įtrūkimų ir persidengimų. Šie nustatymai veikia jūsų naudojamą būdą **Galioja nuo** iki **Galioja iki** laukelius kiekvienai inžinerijos versijai, kuriai taikoma kategorija.<ul><li>Jei ši parinktis nustatyta į *Taip*, vertė **Galiojanti nuo** turi būti nurodyta kiekvienai versijai ir nei persidengimams, nei pertraukoms, kurios neleidžiamos tarp versijų. Duomenų intervalas kiekvienai inžinerijos versijai yra sujungtas tiesiai su ankstesniu ir kitomis inžinerijos versijomis, jei jie yra. Šiuo scenarijumi, naujausia versija visada yra naudojama, o senesnės daugiau nebenaudojamos.</li><li>Jei ši parinktis nustatyta į **Ne**, nėra daugiau jokių apribojimų efektyvumo datos laukeliams inžinerinėje versijoje, persidengimai ir pertraukos yra leidžiami. Tokiu scenarijumi, kelios versijos gali būti įjungtos tuo pat metu ir galite dirbti su bet kuria galiojančia versija.</li></ul><p>Ši parinktis taip pat veikia KS ir maršrutus, kurie yra susieti su produkto versija. Dėl daugiau informacijos, žr. [Sujungti KS ir maršrutus su inžinerijos versijomis](#boms-routes) tolesniame skyriuje šioje temoje.</p> |
| Naudoti skaičių taisyklės nomenklatūrą | Nustatykite šią parinktį į *Taip* norėdami įjungti taisyklės produkto skaičiaus nustatymui naudojant skaičių seką, inžinerinių atributų pavadinimus ir vertes bei teksto konstantas kaip segmentus. Norėdami sukurti ir keisti taisykles, rinkitės **Redaguoti** mygtuką. |
| Naudoti pavadinimų taisyklės nomenklatūrą | Nustatykite šią parinktį į *Taip* norėdami nustatytu pavadinimą naudojant inžinerinių atributų pavadinimus ir inžinerinių atributų vertes bei teksto konstantas kaip segmentus. Norėdami sukurti ir keisti taisykles, rinkitės **Redaguoti** mygtuką. |
| Naudoti aprašymo taisyklės nomenklatūrą | Nustatykite šią parinktį į *Taip* norėdami nustatyti aprašą naudojant inžinerinių atributų pavadinimus ir inžinerinių atributų vertes bei teksto konstantas kaip segmentus. Norėdami sukurti ir keisti taisykles, rinkitės **Redaguoti** mygtuką. |

### <a name="attributes-fasttab"></a>„FastTab“ atributai

Naudokite tinklelį **Atributų** „FastTab“ norėdami nustatyti inžinerijos atributus, kurie taikomi produktams priklausantiems šiai kategorijai. Dėl daugiau informacijos apie tai, kaip sukurti inžinerijos atributus kategorijas, žr. [Inžinerijos atributai ir inžinerijos atributų paieška](engineering-attributes-and-search.md).

Naudokite mygtukus **Atributai** „FastTab“ norėdami pašalinti ir suorganizuoti atributus tinklelyje.

Jei keičiate atributų pasirinkimą inžinerijos įmonei ir produktai jau yra paremti kategorijai, privalote nuspręsti, ar taikyti savo keitimus tiems produktams. Jei norite, kad esantys produktai būtų su pakeitimais, rinkitės **Naujinti esamus produktus** „FastTab“ **Atributai**.

Kiekvienai įtrauktai eilutei įtrauktai į tinklelį, nustatykite tolesnius laukelius.

| Laukas | Aprašas |
|---|---|
| Pavadinimas | Pasirinkite įtraukiamą atributą. |
| Reikšmė | Pasirinkite atributui numatytąją vertę. |
| Privalomas | Pasirinkite, ar atributas yra privalomas; tai reiškia, kad vartotojai turi nurodyti tinkamą atributo vertę prieš įrašant produktą. Šio parametro poveikis šiek tiek skiriasi, atsižvelgiant į pasirinkto atributo duomenų tipą, kaip apibūdinta toliau pateiktame sąraše.<ul><li>**Būlio logikos** *·* *– nustatykite tai kaip Taip, norėdami reikalauti, kad atributo vertė būtų Taip* (sistema neprisirašys įrašyti produkto, kai atributas nustatytas kaip *Ne).* Nustatykite, kad *būtų* ne, jei norite priimti vertę *Taip* arba *Ne*. (Tipo atributai *Būlio* logikos reikšmė negali būti tuščia.)</li><li>**Sveikojo skaičiaus arba dešimtainės** trupmenos *– nustatykite tai kaip Taip,* jei reikia, kad vartotojai turėtų įvesti šio atributo vertę, kuri būtų ne nulinė. Nustatykite tai kaip *Ne*, jei norite leisti vartotojams įrašyti nulinę vertę.  (Šių tipų atributai negali turėti tuščios vertės.)</li><li>**Sąrašas** – sąrašai turi duomenų tipą Tekstas *, bet* taip pat apima iš anksto nustatytą galimų verčių sąrašą. Todėl šio tipo atributų tuščios vertės įvesti neįmanoma, todėl šis parametras neturi įtakos ir yra tik informacinis.</li><li>**Visi kiti duomenų tipai** – nustatykite tai kaip *Taip,* kad atributas būtų privalomas. Nustatykite kaip *Ne*, jei norite leisti vartotojams išsaugoti produktą, net jei pateikiate šio atributo vertę.</li></ul> |
| Paketo atributas | Pasirinkite, ar atributas turi būti skatinamas per bendras funkcijas. |

### <a name="readiness-policy-fasttab"></a>Parengimo politikos „FastTab“

Naudokite **Produkto parengimo politikos** lauką tam, kad pasirinktumėte pasirengimo politiką, kuri turėtų būti taikoma produktams, sukurtiems pagal šią inžinerijos kategoriją. Dėl daugiau informacijos, žr. [Produkto parengimas](product-readiness.md).

> [!NOTE]
> **Produkto pasirengimo strategijos** laukas šiek tiek skiriasi, jei savo sistemoje įjungėte *Produkto pasirengimo tikrinimo* funkciją. (Ši priemonė leidžia taikyti pasirengimo strategijas standartiniams \[ne inžineriniams\] produktams). Daugiau informacijos rasite [Pasirengimo strategijų priskyrimas standartiniams ir inžineriniams produktams](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Leidimo politikos „FastTab“

Naudokite **Produkto leidimo politikos** laukelį tam, kad pasirinktumėte leidimo politiką, kuri taikoma produktams priklausantiems šiai kategorijai. Dėl daugiau informacijos, žr. [Leidžiamo produkto struktūros](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Sujunkite KS ir maršrutus su inžinerijos versijomis

Nustatymo **Vykdyti efektyvumą** parinktis yra svarbi KS jungčiai ir maršrutams su kiekviena inžinerijos versija. Galite aktyvuoti keletą KS ar maršrutus pagal produktą, tik jei yra skirtumas bet kuriuose tolesniuose nustatymuose:

- Produkto dimensija
- Kiekis
- Vieta
- Efektyvumo datos

Inžinerijos KS ir maršrutai yra sukurti iš inžinerijos versijos, kurioje buvome taikomi. Jie gali būti atpažinti pagal tikrinimo ženklą **Inžinerijos valdoma** žymimą laukelį. Kai jūsų darbas su inžinerijos KS ir maršrutai, negalėsite dažniausiai nustatyti jų naudodami skirtingus kiekius. Jūs taip pat dažniausiai nekursite kitų KS saitui. Taip pat, inžineriniams KS ir maršrutams, efektyvumo datos visuomet yra paimamos iš inžinerijos versijos. Dėl to, inžinerijos versijos KS ir jos maršrutai visada turės tas pačias efektyvumo datas.

Produktams, kai naudojate *versijos* produkto matmenis (kartu su logistiniu poveikiu perlaidoms) versija taip pat įtraukiama į KS ir maršrutus. Toks elgesys padeda atskirti KS ir maršrutus tolesnėse versijose nepriklausomai nuo **Vykdyti efektyvumą** nustatymų.

Produktams, kai naudojate *versijos* produkto matmenis (kartu su logistiniu poveikiu perlaidoms) versija taip pat įtraukiama į KS ir maršrutus. Dėl to, nebus jokio skirtumo tarp KS ir atitinkamų versijų maršrutų. Tokiu atveju, primygtinai rekomenduojame jums nustatyti **Vykdyti efektyvumą** parinktį į *Taip*. Tokiu būdu, padėsite apsisaugoti inžinerijos versijoms nuo persidengimo ir taip pat įjungti KS ir maršrutą naujesnėje versijoje be poreikio išjungti KS ir maršrutą ankstesnėje. Jei nustatote **Įjungti efektyvumą** parinktį į *Taip* tokiu atveju, privalote rankiniu būdu išjungti KS ir senesnių versijų maršrutus prieš tai, kai galėsite įjungti naujausią versiją.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
