---
title: Produkto identifikatoriai
description: Šioje temoje pateikiama informacija apie įvairių tipų produkto identifikatorius ir paaiškinama, kaip produktų duomenyse galite pridėti produkto identifikatorių.
author: cvocph
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: c3f82834fa7fc5eec6411d92729439dfd49a1fcc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820255"
---
# <a name="product-identifiers"></a>Produkto identifikatoriai

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie įvairių tipų produkto identifikatorius ir paaiškinama, kaip produktų duomenyse galite pridėti produkto identifikatorių.

Kai su produktais ceche arba sandėlyje dirbate naudodami „Microsoft Dynamics“ ERP arba „Microsoft Dynamics CRM”, turite būti numatę gerą strategiją produktams ir jų variantams identifikuoti.

## <a name="unique-product-numberproduct-id"></a>Unikalus produkto numeris / produkto ID

„Dynamics 365 Supply Chain Management“ pirminis produkto identifikatorius yra produkto numeris (t. y. unikalus produkto ID). Šį numerį galima sugeneruoti automatiškai naudojant skaičių seką arba rankiniu būdu susieti su produktu. Produkto variantų atveju numerius galima nustatyti naudojant produkto nomenklatūros šabloną.

Daugeliu atvejų produkto numerio „Dynamics 365 Supply Chain Management“ iš pradžių nesukuria. Vietoj to, numeris su produktu susiejamas produktų ciklo valdymo (PLM) sistemoje arba produktų duomenų valdymo (PDM) sistemoje. Tokius atveju produktams ir produkto variantams importuoti reikia naudoti duomenų objektus. Tada „Supply Chain Management” naudoja numerius visose operacijose.

„Supply Chain Management” diegimo metu produktų numerių strategiją reikia ypač gerai apsvarstyti. Gera numeravimo sistema pagerina logistikos srautus ir padeda išvengti klaidų. Geras produkto identifikatorius turi būti sudarytas iš ne daugiau kaip 15 simbolių. Geriausia, jei jis būtų sudarytas iš mažiau nei 10 ir ne daugiau kaip penkių klasifikavimo simbolių. Norėdami įgalinti sparčiąsias ieškas, taip pat galite naudoti ieškos pavadinimus. Ieškos pavadinimas – tai papildomas pavadinimas, kuriuo nurodomos produkto klasifikacijos.

Naudojant „Microsoft Dataverse“, produkto numeris „Supply Chain Management” taip pat yra produkto numeris „Microsoft Dataverse“. Produkto variantai su „Dataverse“ sinchronizuojami kaip išskirtieji produktai.

## <a name="item-number-and-product-dimensions"></a>Prekės numeris ir produkto dimensijos

Prekės numeris – tai produkto identifikatorius, kurį naudoja konkretus juridinis subjektas. Geriausia, kad prekės numeris būtų toks pat, kaip ir produkto numeris. Jei kiekvieno juridinio subjekto nomenklatūra skiriasi, sekti produktą visoje tiekimo grandinėje tampa sunku, taip pat apsunkinami perženklinimo ir susiejimo procesai. Siekdami išlaikyti suderinamumą su senesnėmis versijomis (t. y. su „Microsoft Dynamics AX 2009“ ir ankstesnėmis), palikome šį modelį. Tačiau, kai tik galėsite, rekomenduojame pašalinti identifikatorius, būdingus juridiniams subjektams, ir vietoje to kaip pirminį identifikatorių naudoti unikalų produkto numerį.

Be to, produkto varianto pagal prekės numerį unikaliai identifikuoti negalima. Identifikatorių visada turi sudaryti prekės numerio ir produkto dimensijų, nurodytų bendrajame produkte, kombinacija. Šis reikalavimas gali tapti sudėtingu ir sulėtinti identifikavimo procesus. Dėl to, kai tik įmanoma, vietoje prekės numerio rekomenduojame naudoti unikalų produkto numerį.

Daugelyje puslapių prekės numeris ir produkto dimensijos vis dar laikomos pirminiais identifikatoriais. Tačiau produktų numerius galima naudoti atliekant ieškas. Apsilankę parinktyje **Pardavimas ir rinkodara** &gt; **Sąranka** &gt; **Ieška** &gt; **Ieškos parametrai** ieškos peržvalgas galite pakeisti taip, kad vietoje prekių numerių kaip pirminė ieškos strategija būtų naudojami produktų numeriai. Jei parinktį **Įjungti produkto ieškos peržvalgą** nustatysite į **Taip**, peržiūroje bus rodomi ne tik bendrieji produktai, bet ir produkto variantai. Daugiau informacijos rasite perskaitę [Ieškoti produktų ir produkto variantų įvedant užsakymą](search-products-product-variants.md).

Be to, galėsite ieškoti ir filtruoti pagal produkto numerį, produkto pavadinimą ir aprašą bei produkto varianto produkto dimensijų ID. Pasirinkus variantą, bus pasirinktas susijęs prekės numeris ir visi produkto dimensijos ID. Todėl rasti ir pasirinkti tinkamą variantą taps dar paprasčiau. Šį parametrą ypač rekomenduojama naudoti tuo atveju, jei kaip pirminius produkto identifikatorius naudojate produkto variantus ir unikalų produkto numerį. Vienintelė išimtis gali būti taikoma mados pramonei, kurioje, dėl tenai vykstančių verslo procesų, dažnai reikalaujama, kad prieš pasirenkant variantą būtų pasirinktas bendrasis produktas. Prieš įdiegdami numeravimo sistemą, atidžiai įvertinkite šią parinktį.

> [!NOTE]
> Produkto prekės numerio negalima pakeisti, kai yra vienas ar daugiau to produkto operacijų.

## <a name="product-name-and-description"></a>Produkto pavadinimas ir aprašas

Produkto pavadinimas ir aprašas yra žmonėms suprantami produkto identifikatoriai, kuriuos galima tvarkyti įvairiomis kalbomis. Pagal numatytuosius nustatymus, „Supply Chain Management” kliente visų produktų informacija rodoma numatytąja įmonės kalba, o ne vartotojo kalba. Tačiau išversti produkto pavadinimai ir aprašai naudojami bendraujant su visais klientais ir tiekėjais. Vertimai yra paremti pagal kliento ir tiekėjo abonementų kalbos kodą.

Produkto variantų atveju produkto pavadinimą galima sugeneruoti naudojant produkto nomenklatūros šabloną. Produktų pavadinimai neturi būti unikalūs, todėl galite rasti keletą produktų tuo pačiu pavadinimu.

## <a name="product-and-item-search-names"></a>Produkto ir prekės ieškos pavadinimai

„Supply Chain Management” galima nurodyti antrinį produktų ir prekių (patvirtintų produktų) ieškos pavadinimą. Šis ieškos pavadinimas nebūtinai turi būti unikalus ir sukūrus produktą arba produkto variantą jį galima pakeisti. Ieškant produktų pagal kategorijas rekomenduojame naudoti ieškos pavadinimą. Naudojant ieškos pavadinimus galima atlikti sparčiąsias ieškas, ypač pardavimo ir pirkimo procesuose.

Ieškos pavadinime taip pat gali būti nurodytas kliento arba tiekėjo produkto ID ar kitas išorinis produkto ID, jei šis išorinis ID yra produkto pirminis ieškos kriterijus.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Išoriniai produkto identifikatoriai (kliento ir tiekėjo identifikatoriai)

Patvirtintų produktų atveju galite tvarkyti kliento arba tiekėjo naudojamus prekių numerius, prekių pavadinimus ir prekių aprašus. Nuorodos pateikiamos išoriniuose dokumentuose, pvz., pardavimo užsakymuose, pirkimo užsakymuose, važtaraščiuose ir SF. Dabartinės versijos „Supply Chain Management” išorinės nuorodos nerodomos pagrindinių operacijų puslapiuose. Vienintelė išimtis taikoma tiekėjo prekės numeriui. Jei apibrėžtas patvirtinto produkto numatytasis tiekėjas, šis numeris pateikiamas dialogo lange **Produkto informacija**.

Išorinius produkto identifikatorius galite tvarkyti pagal patvirtintą produktą, patvirtinto produkto variantą, klientą arba klientų grupę, tiekėją arba tiekėjų grupę.

Puslapyje **Patvirtinti produktai** atlikite vieną iš toliau nurodytų veiksmų.

- Klientų atveju skirtuko **Pardavimas** grupėje **Susijusi informacija** pasirinkite **Išorinis prekės aprašas**.
- Tiekėjų atveju skirtuko **Pirkimas** grupėje **Susijusi informacija** pasirinkite **Išorinis prekės aprašas**.

Puslapyje **Išoriniai prekių aprašai** kliento arba tiekėjo prekės numerį galite susieti su patvirtintu produktu. Šį susiejimą reikia atlikti kiekvienam juridiniam subjektui. Galima užfiksuoti toliau nurodytą informaciją. Deja, dabartinėje „Supply Chain Management” versijoje etiketės yra šiek tiek netikslios. Tačiau būsimoje versijoje šias etiketes bus galima pakeisti.

| Laukas | Atitinkama su klientu susijusi informacija | Atitinkama su tiekėju susijusi informacija |
|-------|------------------------------------|----------------------------------|
| Išorinis prekės numeris | Kliento prekės numeris. | Tiekėjo prekės numeris. |
| aprašymas | Pavadinimas, kurį klientas susieja su preke | Pavadinimas, kurį tiekėjas susieja su preke |
| Išorinis prekės tekstas | Kliento prekės aprašas | Tiekėjo prekės aprašas |

Jei dauguma klientų ar tiekėjų naudoja tuos pačius prekių numerius (pavyzdžiui, pirkimų asociacijos ar prekybos grupės atveju), galite sudaryti klientų ar tiekėjų grupes, kad būtų paprasčiau sekti išorinę informaciją apie produktą.

- Klientų grupių atveju eikite į parinktį **Pardavimai** &gt; **Sąranka** &gt; **Prekės** &gt; **Išorinis prekės aprašas**, kad galėtumėte sukurti ir tvarkyti grupes bei susijusius prekių numerius. Norėdami klientus susieti su grupe, eikite į parinktį **Gautinos sumos** &gt; **Klientai** &gt; **Visi klientai**, tada „FastTab“ **Pardavimo užsakymo numatytieji nustatymai** lauke **Prekė – klientų grupė** nustatykite vertę.
- Tiekėjų grupių atveju eikite į parinktį **Paraiškos** &gt; **Sąranka** &gt; **Išorinio prekės aprašo grupė** , kad galėtumėte sukurti ir tvarkyti grupes bei susijusius prekių numerius. Norėdami tiekėjus susieti su grupe, eikite į parinktį **Mokėtinos sumos** &gt; **Tiekėjai** &gt; **Visi tiekėjai**, tada „FastTab“ **Pirkimo užsakymo numatytieji nustatymai** lauke **Prekė – tiekėjų grupė** nustatykite vertę.
 
## <a name="bar-codes"></a>Brūkšniniai kodai

Jei produktams identifikuoti norite naudoti brūkšninių kodų skaitytuvą, produkto identifikatorius turi atitikti naudojamo brūkšninio kodo standarto reikalavimus. Todėl brūkšniniuose koduose vietoje neapdoroto produkto numerio paprastai pateikiamas specialiai pagal pasirinktą brūkšninio kodo technologiją sugeneruotas numeris. Keletą brūkšninių kodų galite tvarkyti pagal brūkšninio kodo tipą. Tą patį brūkšninį kodą galite susieti su keletu produktų, o brūkšninio kodo nuskaitymo metu pasirinkti faktinį aktyvų susiejimą.

Prieš nustatydami brūkšninius kodus, galite nustatyti vieną arba keletą brūkšninio kodo sąrankų. Brūkšninio kodo sąrankos gali padėti patikrinti, ar brūkšniniai kodai atitinka reikiamus nurodymus ir ar juos pavyks efektyviai atspausdinti ir nuskaityti. Taip pat galite tvarkyti konkretaus produkto kiekio specialius brūkšninius kodus.

Norėdami tvarkyti pasaulinio prekybos prekės numerio (GTIN) arba tarptautinio prekės numerio (EAN) kodus, rekomenduojame naudoti brūkšninio kodo sąranką.

Norėdami tvarkyti brūkšninius kodus, puslapyje **Patvirtinti produktai** pateikiamo skirtuko **Atsargų tvarkymas** grupėje **Sandėlis** pasirinkite **Brūkšniniai kodai**.

## <a name="gtin-codes"></a>GTIN kodai

El. komercijai labai svarbu, kad visos šalys bendrautų viena kalba ir produktų ieškotų naudodamos bendrą identifikatorių rinkinį. Todėl kai kuriose pramonės šakose pasikliaunama [GTIN](https://www.gs1.org/id-keys/gtin) – pasauline prekių numerių sistema, kurią teikia GS1.

Rekomenduojame tvarkyti GTIN kaip brūkšninį kodą. Tačiau GTIN taip pat galite tvarkyti ir puslapyje **Prekė – GTIN**. Norėdami atidaryti šį puslapį, puslapyje **Patvirtinti produktai** pateikiamo skirtuko **Atsargų tvarkymas** grupėje **Sandėlis** pasirinkite **GTIN kodai**. GTIN nėra tvarkomas kaip bendrasis numeris. Vietoj to, jis tvarkomas kaip juridinis subjektas.

„Supply Chain Management” pakavimo variantus reikia nurodyti sandėlio operacijose apibrėžiant konkrečius matavimo vienetus. Pavyzdžiui, prekę galima laikyti vienetais, sugrupavus po šešias, ant padėklų po 18 arba išdėsčius ant viso padėklo ploto. Kiekvienam iš šių pakavimo variantų bus nurodytas konkretus matavimo vienetas. GTIN paprastai yra susijęs su produkto pakavimo vienetu, todėl puslapyje **Prekė – GTIN** galite tvarkyti kelis GTIN produkto kodus ir matavimo vienetą. Tačiau to paties GTIN kodo skirtingoms juridinio subjekto prekėms arba produkto variantams negalite naudoti daugiau nei vieną kartą.

Norėdami tvarkyti **GTIN kodus**, puslapyje **Patvirtinti produktai** pateikiamo skirtuko **Atsargų tvarkymas** grupėje **Sandėlis** pasirinkite **GTIN**.

## <a name="external-codes"></a>Išoriniai kodai

Daugeliui objektų galima nustatyti išorinius kodus. Pavyzdžiui, galite nurodyti išorinius kodus, kuriais identifikuojami produktai ir patvirtinti produktais. Šiuos išorinius kodus galima panaudoti statistikos ar mokesčių kodams su patvirtintais produktais ir patvirtinto produkto variantais susieti. Išoriniai kodai nurodomi pagal juridinį subjektą ir kodo tipą. Šių kodų juridinis subjektas, kodo tipas ir lentelės nuoroda turi būti unikalūs.

Deja, nėra jokių standartinių funkcijų, kurios leistų ieškoti produktų pagal išorinius kodus.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Duomenų objektai, naudojami produkto identifikatoriams importuoti arba eksportuoti

| Objekto pavadinimas | Identifikatorių importavimas | Identifikatorių eksportavimas | Komentarai |
|-------------|--------------------|--------------------|----------|
| Produktai V2 | Produkto numeris, produkto ieškos pavadinimas, produkto pavadinimas, produkto aprašas | Produkto numeris, produkto ieškos pavadinimas, produkto pavadinimas, produkto aprašas | Priklausomai nuo subjekto parametrų ir produkto numeriui taikomos numeracijos, produkto numerį galima sukurti automatiškai importavimo metu. |
| Produkto variantai | Produkto numeris, produkto ieškos pavadinimas, produkto pavadinimas, produkto aprašas | Produkto numeris, produkto ieškos pavadinimas, produkto pavadinimas, produkto aprašas | Priklausomai nuo produkto nomenklatūros šablono, produkto numerį galima sukurti automatiškai importavimo metu. Tačiau galite importuoti bet kokį unikalų produkto numerį ir šis produkto numeris neturi atitikti produkto nomenklatūros šablonų struktūros. |
| Produkto vertimai | Produkto pavadinimas, produkto aprašas | Produkto pavadinimas, produkto aprašas | Šis subjektas perrašo bet kokią kalbą. Kai perrašoma juridinio subjekto pavadinimo arba aprašo pagrindinė kalba, pakinta paties produkto pavadinimas ir aprašas. |
| Išleisto produkto kūrimas V2 | Prekės numeris, produkto numeris, prekės ieškos pavadinimas| Prekės numeris, produkto numeris, prekės ieškos pavadinimas, produkto ieškos pavadinimas, produkto pavadinimas | Šis subjektas gali kelti sunkumų, kai naujai patvirtintų produktų kūrimo metu naudojamos numeracijos. Įtakos turi tiek numeracija pagal **prekės numerį**, tiek ir numeracija pagal **produkto numerį**. Vis dėlto, numeracija pagal **prekės numerį** atliekama atskirame juridiniame subjekte, o numeracija pagal **produkto numerį** yra bendrinė. Dėl šios priežasties numeracijos pagal **prekės numerį** nerekomenduojame naudoti diegiant naujus patvirtintus produktus. Savaime suprantama, kai subjektas naudojamas esamam produktui išleisti, subjekte būtina pateikti produkto numerį. Daugiau informacijos ieškokite šios temos skyriuje „Numeracijos pagal produktą ir prekės numerį“. |
| Patvirtinto produkto variantai | Prekės numeris, produkto dimensijos, produkto numeris | Produkto numeris, produkto ieškos pavadinimas, produkto pavadinimas, produkto aprašas, produkto dimensijos | Šį subjektą, kaip ir subjektą **Produkto variantai**, galima panaudoti naujiems produktams, atitinkantiems produkto nomenklatūros šabloną arba produktams, kuriuose naudojami turimi varianto produktų numeriai, kurti. |
| Klientų išorinis prekės aprašas | Kliento prekės numeris, kliento prekės pavadinimas, kliento aprašas, kliento kodas | Kliento prekės numeris, kliento prekės pavadinimas, kliento aprašas, kliento kodas | Klientų grupę (pvz., pirkėjo asociaciją) į vieną grupę apjungti galima panaudojus subjektą **Išorinių prekių aprašų klientų grupės**. |
| Tiekėjų išorinis prekių aprašas | Tiekėjo prekės numeris, tiekėjo prekės pavadinimas, tiekėjo aprašas, tiekėjo kodas | Tiekėjo prekės numeris, tiekėjo prekės pavadinimas, tiekėjo aprašas, tiekėjo kodas | Tiekėjų grupę (pvz., pirkėjo asociaciją arba pramonės organizaciją) į vieną grupę apjungti galima panaudojus subjektą **Išorinių prekių aprašų tiekėjų grupės**. |
| Prekės brūkšninis kodas | Brūkšninis kodas | Brūkšninis kodas | Importavimo metu turite atsižvelgti į brūkšninio kodo sąranką, nustatytą paskirties sistemoje. Importuoto brūkšninio kodo nuorodos patvirtinamos pagal brūkšninio kodo sąranką, o jei brūkšniniai kodai neatitinka reikalavimų, nustatytų sąrankoje, nuorodos atmetamos. |
| Išleistų produktų išoriniai kodai | Išorinis kodas | Išorinis kodas, išorinio kodo klasės, prekės numeris | Išoriniai kodai priklauso nuo juridinio subjekto. Importuodami turite atsižvelgti į nustatytą kodo klasę. Kodo klases importuokite pasinaudodami subjektu **Patvirtintų produktų išorinio kodo klasės**. |
| Išleistų produktų variantų išoriniai kodai | Išorinis kodas | Išorinis kodas, išorinio kodo klasės, prekės numeris, produkto dimensijos | Išoriniai kodai priklauso nuo juridinio subjekto. Importuodami turite atsižvelgti į nustatytą kodo klasę. Kodo klases importuokite pasinaudodami subjektu **Patvirtintų produktų išorinio kodo klasės**. Šis objektas nurodo produkto variantus pagal prekės numerį ir produkto dimensijas. |
| Pagal produkto numerį patvirtintų produkto variantų išorinių kodų identifikatorius | Išorinis kodas | Išorinis kodas, išorinio kodo klasės, produkto numeris | Išoriniai kodai priklauso nuo juridinio subjekto. Importuodami turite atsižvelgti į nustatytą kodo klasę. Kodo klases importuokite pasinaudodami subjektu **Patvirtintų produktų išorinio kodo klasės**. Šis subjektas nurodo produkto variantus pagal varianto produkto numerį. (Nuo kito pagrindinio leidimo) |
| GTIN | Netaikoma | Netaikoma | Šiuo metu specialių subjektų, naudojamų GTIN kodams importuoti ir eksportuoti, nėra. Vietoj to rekomenduojame naudoti subjektą **Prekės brūkšninis kodas**. |
| Produkto subjekto „Common Data Service“ identifikatoriaus subjektas | Netaikoma | Prekės numeris, prekės ieškos pavadinimas, produkto ieškos pavadinimas, tiekėjo prekės numeris, kliento prekės numeris, išoriniai kodai, GTIN kodai, brūkšniniai kodai | Šis subjektas visus identifikatorius sujungia į „One Data Model”, kad visus identifikatorius ir susijusius jų tipus būtų galima lengvai eksportuoti naudojant vieną sąsają. Identifikatoriaus kodams ir aprašams eksportuoti naudokite subjektą **Produkto subjekto identifikatoriaus kodas**. Papildomai aprėpties informacijai, pvz., šalis, teisinis subjektas, kiekis ar vienetas, į identifikatorių eksportuoti naudokite subjektą **Produkto subjekto identifikatoriaus aprėptis**. |

### <a name="product-and-item-number-sequences"></a>Numeracijos pagal produktą ir prekės numerį

Galite nurodyti dvi skirtingas numeracijas.

- Bendrojo produkto numerio numeracija pagal **produkto numerį**
- Atskiro teisinio subjekto prekės numerio numeraciją pagal **prekės numerį**

> [!NOTE]
> Prekės numerį kaip atskirą identifikatorių turėtumėte naudoti tik tada, kai perkeliate skirtingų šaltinių, kuriuose naudojamos skirtingos numeravimo sistemos, skirtingus teisinius subjektus. Turite stengtis visada naudoti visuose teisiniuose subjektuose unikalų produkto identifikatorių. Dėl šios priežasties parinktį **Neautomatinis**, skirtą numeracijai pagal **prekės numerį**, reikia nustatyti į **Taip**. Tokiu būdu kūrimo metu prekės numeris atitiks produkto numerį. Jei „Supply Chain Management” nėra pagrindinė naujų produktų numerių sistema, numeracijos pagal **prekės numerį** ir **produkto numerį** parinktį **Neautomatinis** turite nustatyti į **Taip**.

Kai naudojate subjektą **Išleisto produkto kūrimas V2** produktams kurti, tai, kaip numeracijos naudojamos produkto numeriui ir prekės numeriui kurti, įtakos gali turėti keletas parametrų.

- Numeracijos pagal **produkto numerį** parametrai
- Numeracijos pagal **prekės numerį** parametrai
- Prekės numerio susiejimas 
- Produkto numerio susiejimas

Toliau esančioje lentelėje pateikiama importavimo ir neautomatinio kūrimo, kai naudojamos specifinės numeracijos kombinacijos ir laukų susiejimo parametrai, rezultatų apžvalga.

| Numeracija pagal produkto numerį | Numeracija pagal prekės numerį | Prekės numerio susiejimas | Produkto numerio susiejimas | Subjekto importavimo rezultatas | Neautomatinio kūrimo rezultatas | Išvada |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Neautomatinis = ne | Neautomatinis = ne | Nėra susiejimo | Nėra susiejimo | Produktų numeriai numeruojami pagal **produkto numerį**. Prekės numeriai numeruojami pagal **prekės numerį**. | Produktų numeriai numeruojami pagal **produkto numerį**. Prekės numeriai numeruojami pagal **prekės numerį**. | Naudojant šią konfigūraciją, produktų numeriai atitiks produkto numeraciją, o prekių numeriai atitiks prekės numeraciją. Tačiau ši konfigūracija neveikia, jei yra daugiau nei viena prekė (eilutė), kurią reikia importuoti. |
| Neautomatinis = ne | Neautomatinis = taip | Automatinis generavimas | Nėra susiejimo | Produktų ir prekių numeriai numeruojami pagal **prekės numerį**. | Produktų ir prekių numeriai numeruojami pagal **produkto numerį**. | Produktų ir prekių numeriai atitinka produkto numeraciją. Tai rekomenduojamas metodas importuoti didelius produktus, naudojant išleistą produkto kūrimo V2 duomenų objektą.<br><br>Galite naudoti šį būdą tik masiškai importuodami prekes (kelias eilutes) ir kai nekuriate prekių naudodami vartotojo sąsają. Jei turite atlikti masinį importavimą ir kurti produktus naudodami vartotojo sąsają, naudokite procedūrą, esančią kitoje šios lentelės eilutėje. Norėdami pereiti nuo masinio importavimo prie vartotojo sąsajos naudojimo importuoti ir kurti produktus rankiniu būdu, turite rankiniu būdu pakoreguoti prekės numeracijos reikšmę **Kitas numeris**, kad ji sutaptų su produkto numeracijos reikšme **Kitas numeris**. Tada galite pereiti prie kitoje šios lentelės eilutėje nurodyto būdo. |
| Neautomatinis = ne | Neautomatinis = taip | Nėra susiejimo | Nėra susiejimo | Produktų ir prekių numeriai numeruojami pagal **produkto numerį**. | Produktų ir prekių numeriai numeruojami pagal **produkto numerį**. | Produktų ir prekių numeriams naudojama produkto numeracija. Tačiau ši konfigūracija neveikia, jei yra daugiau nei viena prekė (eilutė), kurią reikia importuoti.<br><br>Jei reikia ir importuoti produktus naudojant objektus (vienu metu galima importuoti tik vieną eilutę) ir sukurti produktus naudojant vartotojo sąsają, turite naudoti šį būdą. |
| Neautomatinis = taip | Netaikoma | Netaikoma | Automatinis generavimas | Jūs gaunate šį klaidos pranešimą: „Negalima nustatyti numeracijos“. | Remiantis numeracija pagal **prekės numerį** | Importuojant šis parametras nepalaikomas. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Produkto subjekto identifikatorius (visų produkto identifikatorių eksportavimas)

Produkto objekto identifikatoriaus modelis sukurtas siekiant įjungti 1.0 versijos „Dataverse” konfigūravimą su visais identifikatoriais, naudojamais produktui įvardyti. Siekiant palengvinti šią užduotį, visi identifikatoriai sujungti į vieną bendrą identifikatorių lentelę, kad juos būtų galima eksportuoti kaip vieną modelį. Atkreipkite dėmesį, kad šioje „Dataverse” versijoje nenaudojamas produkto identifikatorių modelis. Dėl šios priežasties subjektas **Produkto subjekto „Common Data Service“ identifikatoriaus subjektas** ir šis procesas praktiškai bus naudojamas labai ribotai, o ateityje jokių galimų keitimų nenumatyta.

Produkto identifikatorių lentelė yra bendroji, t. y. yra sukurta remiantis visomis pagrindinio juridinio subjekto nuorodų lentelėmis, atlikus pasikartojančią paketinę užduotį. Kaip visuotinio bendrojo produkto aprėpties apibrėžimą turite pasirinkti juridinį subjektą ir produktų kategorijų hierarchiją. Bendrosios produkto identifikatorių lentelės generavimas yra ribojamas produktams, išleistiems pagal pasirinktą juridinį subjektą, ir produktams, kurie priklauso produkto hierarchijai, kategorijų hierarchijoje parinktai pagal **„Common Data Service“** priskirtą vaidmenį.

Atliekant šį procesą manoma, kad produkto bendrieji duomenys pirmiausia tvarkomi viename centriniame juridiniame subjekte. (Tačiau šis juridinis subjektas gali būti virtualus juridinis subjektas, kuris naudojamas visuotiniams bendriesiems duomenims tvarkyti.)

Atlikite šiuos veiksmus, norėdami sukonfigūruoti aplinką.

1. Pasirinkite „Dataverse” kategorijų hierarchiją. Jei puslapyje **Kategorijų hierarchijos vaidmenų susiejimai** su vaidmeniu **„Common Data Service“** nesusieta jokia hierarchija, turite sukurti naują susiejimą. Pasirinkite **„Common Data Service“** vaidmenį ir tada susiekite kategorijų hierarchiją, atspindinčią produktų portfelį, kurį reikia sinchronizuoti su „Dataverse”.
2. Pasirinkite visuotinio produkto bendrųjų duomenų juridinį subjektą. Puslapyje **Produkto informacijos valdymo parametrai** pateikiamame skirtuke **Produkto atributai** pasirinkite bendrąją įmonę, kurioje pirmiausia tvarkomas produktas ir prekės identifikatoriai.
3. Nustatykite identifikatorius kodų tipus ir kodus, kuriuos norite eksportuoti. Eikite į parinktį **Produktų informacijos valdymas** &gt; **Sąranka** &gt; **Produkto identifikatoriaus kodai**. Norėdami sugeneruoti identifikatorius kodų tipus, pasirinkite **Generuoti kodus**. Kiekvienam identifikatoriui, randamam pasirinktame juridiniame subjekte, bus sugeneruota kodo tipo įvestis.

    Brūkšninių kodų atveju kodas sugeneruojamas kiekvienai brūkšninio kodo sąrankai. Išorinių kodų atveju brūkšninis kodas sugeneruojamas kiekvienai išorinei kodo klasei.

    Tada jau galite tvarkyti kodo tipų sąrašą. Galite keisti kodą, pavadinimą ir aprašą. Taip pat galite panaikinti kodų tipus. Kodų tipai, kurios panaikinsite, nebus naudojami bendrajai produkto subjekto identifikatorių lentelei užpildyti.

4. Baigę nustatyti produkto identifikatorius kodo tipus, bendroje lentelėje identifikatorius sukurti galėsite pradėję užduotį **Produkto subjekto identifikatorių kūrimas**, pateikiamą puslapyje **Produkto subjekto identifikatoriaus kodai**. Šią užduotį turite paleisti pakete. Šią užduotį reikia nustatyti kaip periodinę paketinę užduotį, kad lentelė būtų užpildyta pagal naujas įvestis.

Dabar identifikatoriams iš bet kurios paskirties sistemos eksportuoti galite naudoti subjektą **Produkto subjekto „Common Data Service“ identifikatoriaus subjektas**, **Produkto subjekto identifikatoriaus kodas** ir **Produkto subjekto identifikatoriaus aprėptis**.

## <a name="related-topic"></a>Susijusi tema

[Ieškoti produktų ir produkto variantų įvedant užsakymą](search-products-product-variants.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
