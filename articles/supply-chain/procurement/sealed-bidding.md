---
title: Užantspauduotas kainos pasiūlymas, skirtas RFQ
description: Šioje temoje aprašoma, kaip nustatyti užantspauduotos kainos pasiūlymą, kad tiekėjo kainų pasiūlymo atsakymai būtų palikti slapti, kol jie nėra atskleisti pirkimo personalo.
author: Henrikan
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 96549b6053ba75f2d5b9a85bcd5b7feb006f0f1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578085"
---
# <a name="sealed-bidding-for-rfqs"></a>Užantspauduotas kainos pasiūlymas, skirtas RFQ

[!include [banner](../includes/banner.md)]

Užantspauduotos kainos pasiūlymas išlaiko tiekėjo kainų pasiūlymo atsakymus slaptus, kol jie nėra atskleisti pirkimo personalo. Visi su pasiūlymo patvirtinimu (RFQ) susiję kainų pasiūlymai pirmiausia yra pasiekiami būti išantspauduoti pasibaigus kainos pasiūlymo galiojimo laikui. Prieš atskleidžiant kainos pasiūlymą tik tie vartotojai, kurie turi paskirtus vartotojų vaidmenis ir kurie atstovauja tiekėjui, gali jį pasiekti.

> [!IMPORTANT]
> Formų modifikavimas ar išplėtimas, taip pat naujų formų ar verslo logikos kūrimas gali pažeisti „Microsoft” teikiamą užantspauduoto kainos pasiūlymo apsaugą. Jūs prisiimate riziką naudoti bet kokius pakeitimus, plėtinius, naujas formas ar verslo logiką, arba negalėjimą naudotis užantspauduoto kainos pasiūlymo funkcija dėl tokių modifikacijų, plėtinių, naujų formų ar verslo logikos.  „Microsoft” nėra atsakingas už žalą, patirtą dėl pakeitimų, plėtinių, naujų formų ar verslo logikų, kuriuos sukūrėte jūs arba trečioji šalis jūsų vardu. „Microsoft” nepateikia jokio techninio ar kitokio palaikymo pakeitimams, plėtiniams, naujoms formoms ar verslo logikoms, kuriuos sukūrėte jūs arba trečioji šalis jūsų vardu. Jūs esate atsakingas už visų taikomų įstatymų ar taisyklių, susijusių su užantspauduotais kainos pasiūlymais, laikymąsi.

## <a name="how-bids-are-kept-secure"></a>Kaip saugomi kainų pasiūlymai

Užantspauduotas kainos pasiūlymas naudoja simetrinį šifravimą, kad būtų išifruotas kainos pasiūlymo šifravimo raktas (KEK) ir simetrinį šifravimą, kad būtų galima iššifruoti faktinį kainos pasiūlymą. Sistema integruojama su Microsoft Azure "Key Vault", kad būtų sugeneruoti ir valdomi šifravimo raktai, naudojami užantspauduotiems kainų pasiūlymų koregavimams užšifruoti. Kiekvienas kainos pasiūlymas turi nuosavą šifravimo raktą. Šis šifravimas saugomas raktų saugykloje, kuri priklauso organizacijai, valdančiai Dynamics 365 Supply Chain Management. Prireikus užšifravimo ir iššifravimo, sistema prieina prie rakto saugyklos.

## <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija

Šiame skyriuje aprašomos būtinosios sąlygos, kurios privalomos prieš išsiunčiant RFQ, kuriems reikalingas užantspauduotos kainos pasiūlymas.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>1 žingsnis: nustatyti vartotojo prieigą prie užantspauduotos kainos pasiūlymo

Kai naudojate užantspauduotą kainos pasiūlymą, tik tie vartotojai, kurie yra nustatyti kaip tiekėjo kontaktinis asmuo, gali peržiūrėti, redaguoti ir pateikti to tiekėjo kainos pasiūlymus, kol pasibaigs kainos pasiūlymo laikotarpis. Šie vartotojai turi turėti i **Tiekėjo (išorinį)** vaidmenį ir jie turi būti nustatyti kaip tiekėjo sąskaitos kontaktiniai asmenys. Kontaktinis asmuo taip pat turi turėti teisę bendradarbiauti su tiekėjais, kaip aprašyta [Tiekėjų bendradarbiavimo nustatymas ir priežiūra skyriuje](set-up-maintain-vendor-collaboration.md).

Kadangi vartotojai, kurie turi atitinkamus leidimus ir kurie nustatyti kaip tiekėjo kontaktai, gali pasiekti užantspauduotas tiekėjo kainos pasiūlymus, svarbu stebėti, kas tie vartotojai yra. Sistemos administratorius, kuris nustato vartotojus ir saugos vaidmenis, yra atsakingas už prieigos prie užantspauduotos kainos pasiūlymų ribą tiems vartotojams, kurie iš tikrųjų gali juos peržiūrėti.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>2 žingsnis: įgalinkite užantspauduotos kainos pasiūlymo funkciją

Prieš pradėdami nustatyti ar naudoti šią savybę, privalote įsitikinti, kad ji yra prieinama jūsų sistemoje. Administratoriai gali naudoti **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbo erdvę, kad patikrintų funkcijos būseną ir ją įjungtų. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Paraiškos*
- **Savybės pavadinimas:** *Užantspauduotas RFQ kainos pasiūlymas*

### <a name="step-3-set-up-azure-key-vault"></a>3 žingsnis: „Azure Key Vault“ nustatymas

„Supply Chain Management“ naudoja šifravimo raktus visiems užantspauduotiems kainų pasiūlymams apsaugoti ir saugoti juos slaptai iki reikiamo laiko. Siekiant sugeneruoti ir valdyti reikalingus raktus, atsižvelgiama į "Key Vault" galimybes. Todėl turite nustatyti ryšį iš „Supply Chain Management“ į rakto saugyklą, kad įgalintumėte sistemą.

> [!IMPORTANT]
> Rakto saugyklos, kurias naudojate užantspauduotame kainos pasiūlymą, turi atitikti šiuos reikalavimus:
>
> - Jei kurti ir tikrinti naudojate sandų dėžę, turite turėti vieną atskirą sanddėlyje skirtą rakto saugyklą ir atskirą gamybai skirtą raktų saugyklą.
> - Kiekviena rakto saugykla turi būti sukurta „Azure“ abonemente, kuris priklauso jūsų organizacijai (ne abonementui, kuriame valdote „Supply Chain Management“).
> - Kiekvienas rakto "vault" turi būti naudojamas tik užantspauduotame kainos pasiūlymą. Jei norite naudoti užantspauduotas kainos pasiūlymo rakto saugyklas, negalite naudoti kitų tikslų.

Kiekvienas kainos pasiūlymas nuskaito savo slaptą raktą. Šis raktas naudojamas kiekvieną kartą, kai vartotojas peržiūrės, atnaujins ar atblokuos kainos pasiūlymą.

Rakto saugykla sugeneruoja raktą, kuris naudojamas nuskaityti slaptažodį, kai tiekėjas pasirenka **Kainos pasiūlymą** tiekėjo bendradarbiavimo sąsajoje. Rakto galiojimas baigiasi po fiksuoto laiko, kurį įsigijimo vadovas nustato **Šaltinio pasirinkimas ir parametrai** puslapyje „Supply Chain Management“. Kai raktas baigs galioti, niekas negalės peržiūrėti, redaguoti arba atskleisti kainos pasiūlymo. Todėl svarbu sukonfigūruoti rakto galiojimo pabaigą, kad būtų pakankamai laiko užbaigti kainos pasiūlymo procesą.

Per kitus tris veiksmus, jūs turėsite nustatyti ryšį su rakto saugyklą. Pirma, jūs nustatote rakto saugyklą, kuri bus naudojama su užantspauduotais kainos pasiūlymais. Po to konfigūruokite „Supply Chain Management“, kad būtų užmegztas ryšys su rakto saugykla. Galiausiai, nustatysite rakto galiojimo pabaigos laiką.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>4 žingsnis: Nustatykite rakto saugyklą, kuri bus naudojama su užantspauduotais kainos pasiūlymais

Norėdami nustatyti rakto saugyklą, atlikite tolesnius veiksmus. Veiksmų seka yra labai svarbi.

1. Jei dar nesukūrėte „Azure“ abonemento, kuris būtų atskiras nuo abonemento, kuriame veikia „Supply Chain Management“, sukurkite jį.
1. Sukurkite kodo saugyklą atskiroje "Azure" saugykloje. Daugiau informacijos žr. [„Azure” rakto saugyklos priežiūra](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Nustatykite „Supply Chain Management“ programą, kad ji veiktų kaip jūsų rakto saugyklos klientas. Daugiau informacijos žr. [„Azure” rakto saugyklos kliento nustatymas](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>5 žingsnis: Sukonfigūruokite pagrindinius saugyklos parametrus „Supply Chain Management“

Norėdami konfigūruoti „Supply Chain Management“, kad užantspauduotos kainos pasiūlymo metu būtų komunikuojama su rakto saugykla, atlikite šiuos veiksmus.

1. Prisiregistruokite prie „Supply Chain Management“ ir eikite į **Sistemos administravimas \> Sąranka \> Rakto Saugyklos parametrai**.
1. Pasirinkite **Naujas**, kad sukurtumėte įrašą ir nustatykite jame šiuos laukus:

    - Dalyje **Pavadinimas**- įveskite pavadinimą.
    - Dalyje **Aprašas** - įveskite aprašą.
    - **Rakto saugyklos URL** – įveskite numatytąjį savo rakto saugyklos URL.
    - **Rakto saugyklos klientas** – įveskite interaktyvios Active Directory programos, susietos su autentifikavimo kodo saugyklos, ID.
    - **Rakto saugyklos slaptas raktas** – įveskite sertifikato slaptą nuorodą.
    - **Įgalintas užantspauduotas kainos pasiūlymas**- nustatykite šią pasirinktį į *Taip*.

![Rakto saugos parametrų puslapis](media/sealed-bidding-key-vault-param.png "Rakto saugos parametrų puslapis")

> [!NOTE]
> Vienu metu galite įjungti tik vieną rakto saugyklos konfigūraciją užantspauduotam kainos pasiūlymui. Prieš išjungdami esamą rakto saugyklos konfigūraciją, turite užtikrinti, kad visi užantspauduoti kainų pasiūlymai, kurie juo naudojasi, būtų atskleisti. Peržiūrėkite kiekvieną RFQ atvejo *Užantspauduotą* tipą ir įsitikinkite, kad visi atsakymai yra atskleisti.

### <a name="step-6-set-the-key-expiration-time"></a>6 žingsnis: rakto galiojimo laiko nustatymas

Norėdami nustatyti galiojimo pabaigos laiką, kuris taikomas raktui, sugeneruotam kiekvienam naujam kainos pasiūlymui, atlikite šiuos veiksmus.

1. Eikite į **Įsigijimas ir šaltinio parametrai \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo parametrai**.
1. **Pasiūlymo patvirtinimas** skirtuke **Korespondentinės dienos** laukelyje įveskite dienų skaičių, kiek turėtų trukti RFQ laikotarpis. Kai sukuriamas RFQ, čia įvedamas dienų skaičius pridedamas prie sistemos datos, kad būtų apibrėžta numatytoji RFQ galiojimo data.
1. **Šifravimo rakto galiojimo korespondentinė diena** laukelyje įveskite įveskite dienų skaičių, kiek kiekvienas šifravimo raktas turi galioti po jo išdavimo. Kai šifravimo raktas baigs galioti, niekas negalės peržiūrėti, redaguoti arba atskleisti užantspauduoto kainos pasiūlymo, kuriuo jis naudojasi.

> [!TIP]
> **Šifravimo rakto galiojimo korespondentinės dienos** laukelio vertė negali būti mažesnė nei **Korespondentinės dienos** laukelio vertė.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>7 žingsnis: numatytojo kainos siūlymo tipo nustatymas

Kiekvienas RFQ atvejis turi kainos pasiūlymo tipą. Kainos pasiūlymo tipas nurodo, ar RFQ atvejis teikia atvirą ar užantspaudavo kainos pasiūlymą.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>RFQ atvejai, kurie neturi siūlymo tipo

Norėdami nustatyti numatytąjį kainos siūlymo tipą, priskirtą naujiems RFQ atvejams, kurie, sukūrus, nepriskirti siūlymo tipui, atlikite šiuos veiksmus.

1. Eikite į **Įsigijimas ir šaltinio parametrai \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo parametrai**.
1. Skirtuke **Pasiūlymo patvirtinimas** nustatykite **Kainos pasiūlymo tipo** laukelį į *Užantspauduota*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>RFQ atvejai, kurie turi siūlymo tipą

Norėdami nustatyti numatytąjį kainos siūlymo tipą, priskirtą naujiems RFQ atvejams, kurie, sukūrus, priskiriami siūlymo tipui, atlikite šiuos veiksmus.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Pasiūlymo patvirtinimas \> Siūlimo tipas**.
1. Sukurkite naują siūlymo tipą arba pasirinkite esamą siūlymo tipą, kuriame norite naudoti kainos siūlymo tipą *Užantspauduota*.
1. Nustatykite **Pasiūlymo tipas** lauką į *Užantspauduotas*.
1. Pakartokite šiuos veiksmus kiekvieno papildomo siūlymo tipo, į kurį norite įtraukti užantspauduotos kainos pasiūlymą, atveju.

> [!TIP]
> Siūlymo tipas neturi būti priskirtas, kai sukuriamas naujas RFQ. Jei priskirtas siūlymo tipas, jį gali nuskaityti numatytasis RFQ kainos siūlymo tipas. Kitu atveju, gali būti naudojamas numatytasis siūlymo tipas, apibrėžtas įsigijimo ir pirkimo šaltinio parametruose.

## <a name="the-sealed-bidding-process"></a>Užantspauduoto kainos siūlymo apdorojimas

Užantspauduotos kainos pasiūlymo apdorojimas beveik toks pats kaip aprašyta [Pasiūlymų patvirtinimų (RFQ) apžvalga](request-quotations.md). Pagrindinis skirtumas yra tai, kad kainos pasiūlymo duomenys ir jo priedai užšifruojami, kol kainos pasiūlymas neatblokuojamas.

> [!IMPORTANT]
> [Klausimynai](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) nėra užšifruoti ir neturėtų būti naudojami slaptai informacijai rinkti

Toliau pateiktas proceso išdėstymas:

1. Sukurkite ir nusiųskite RFQ vienam ar keliems tiekėjams.
1. Tiekėjai reaguoja pateikdami užantspaudavo kainos pasiūlymą.
1. Atskleiskite kainų pasiūlymus pasibaigus kainos pasiūlymo įrašo galiojimo laikui.
1. Kainų pasiūlymai tampa matomi, o jūs galite juos įvertinti ir palyginti.
1. Kai kainos pasiūlymas priimamas, sugeneruokite pirkimo užsakymą, sugeneruojate pirkimo sutartį arba atnaujinkite pirkimo paraišką.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Sukurkite RFQ atvejį, kuriame naudojamas užantspauduotas kainos pasiūlymas

RFQ kurimo užantspauduotam kainos siūlymui procesas yra beveik toks pats, kaip ir neužantspauduoto kainos pasiūlymo procesas. Informacijos, kaip sukurti abu RFQ atvejų tipus, žr. [Kurti pasiūlymo patvirtinimą](tasks/create-request-quotation.md). Šioje dalyje aprašomos kelios svarbios aplinkybės, kai kuriate užantspauduotos kainos pasiūlymo RFQ.

RFQ atvejai užantspauduotos kainos pasiūlymai turi turėti **Pasiūlymo tipo** vertę kaip *Užantspauduota*. Yra trys būdai priskirti šią vertę RFQ atvejui:

- Sukūrę vertę tiesiai RFQ atveju nustatykite ją.
- Nurodykite užantspauduotos kainos pasiūlymą kaip numatytąjį visų RFQ atvejų, nurodytų įsigijimo ir pirkimo parametruose, kainos siūlymo tipą. (Žr. [Nustatykite numatytojo kainos pasiūlymo tipą](#set-default-bid-type) šiame skyriuje aukščiau.)
- Kai sukuriate naują RFQ atvejį, pasirinkite siūlymo tipą, nustatytą užantspauduotam kainos pasiūlymui. (Žr. [Nustatykite numatytąjį kainos pasiūlymo tipo](#set-default-bid-type) skyrių.)

Užantspauduotame kainos pasiūlyme RFQ atvejo **Galiojimo data ir laiko** vertė nustatoma tada, kai pateikti kainų pasiūlymai gali būti atskleisti. Kiekvienos eilutės **Galiojimo data ir laiko** vertė atitiks antraštės vertę.

Nusiuntus RFQ atvejį kainos pasiūlymo tipo pakeisti negalima.

### <a name="vendors-respond-to-an-rfq"></a>Tiekėjai atsako į RFQ

Tiekėjai, kurie reaguoja į užantspauduotos kainos pasiūlymą, naudoja tą pačią procedūrą, kurią jie naudoja atviriesiems kainų pasiūlymams, kaip nurodyta  [Darbo su RFQ užklausomis tiekėjo darbo srityje](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Išsamesnės informacijos apie tai, kaip dirbti su atvirais kainų pasiūlymais ir užantspauduotais kainų pasiūlymais, ieškokite [Įveskite ir palyginkite RFQ kainų pasiūlymų ir premijų sutartis](tasks/enter-compare-rfq-bids-award-contracts.md). Vienintelis skirtumas tarp užantspauduotų kainų pasiūlymų apdorojimo ir atvirų kainų pasiūlymų apdorojimo yra tas, kad, kol nepasibaigs kainos pasiūlymo laikotarpis, įsigijimo specialistai negali atidaryti tiekėjo užantspauduotos kainos pasiūlymo. Tik tiekėjo kontaktinis asmuo gali atidaryti to tiekėjo užantspauduotas kainos pasiūlymą.

> [!IMPORTANT]
> Užantspauduotos kainos pasiūlymo atveju tiekėjai gali įkelti priedus tik PDF formatu. Jokie kiti formatai nėra priimami.

Kai užregistruotas tiekėjo vartotojas pasirenka **Kainos pasiūlymą** užantspauduotos kainos pasiūlymo RFQ, jie gali įvesti savo kainos pasiūlymo duomenis ir duomenys bus laikomi slaptai. Tiekėjai gali išsaugoti savo darbą, kai jie paruošia kainos pasiūlymą, grąžinti jį taip dažnai, kaip reikalaujama, ir pateikti jį tada, kai jis parengtas. Tiekėjai taip pat gali peržiūrėti savo kainos pasiūlymą po jo pateikimo. Jei tiekėjai turi pakeisti savo kainos pasiūlymą po pateikimo, jie gali atšaukti jį, atnaujinti ir bet kuriuo metu pateikti iš naujo, kol pasibaigs kainos pasiūlymo laikotarpis.

Užantspauduoto kainos pasiūlymo metu taikomos šios sąlygos:

- Užantspauduoto kainos pasiūlymo metu sistema sukuria *Pasiūlymo patvirtinimo* žurnalą.
- Kai tiekėjas pateikia kainos pasiūlymą, RFQ žurnalai be eilučių sukuriami ir jie turi užantspauduotą kainą.
- Atskleidus atvejį, sukuriami RFQ žurnalai, kurie turi kainą ir kiekį. Šį žurnalą galite pasiekti pasirinkdami **Pasiūlymo patvirtinimo žurnalai** **Visi pasiūlymų patvirtinimai** puslapyje.
- Sistema išsaugo kiekvieno veiksmo, kurį vartotojai atlieka su užantspauduotais kainos pasiūlymais, žurnalą. Šie veiksmai apima kainos pasiūlymo peržiūrą, redagavimą ir išsaugojimą. Šis žurnalas matomas ir tiekėjui, ir įsigijimo specialistams, kurie turi prieigą prie kainos pasiūlymo.
- Kainų pasiūlymo apdorojimo metu įsigijimo specialistai gali peržiūrėti jo būseną. Tada būsena pasikeičia į *Atnaujina tiekėjas* arba į *Pateikė tiekėjas*.
- Užantspauduoto kainos pasiūlymo eilučių būsena lieka *išsiųsta*, kol kainos pasiūlymas neatskleidžiamas.
- Jei tiekėjas nusprendžia atmesti kainos pasiūlymą, kainos pasiūlymas turės **Atsakymas apdorojamas** būseną *Atmesta tiekėjo*. Ši būsena bus matoma įsigijimo personalui.
- Klausimynų atsakymai **nėra** saugomi užšifruota forma duomenų bazėje. Todėl jie nėra užantspauduojami. Tačiau RFQ vartotojo sąsajoje jie nebus matomi, kol atvejis nebus atskleistas.

### <a name="all-sealed-bid-activities-are-logged"></a>Visos užantspauduotos kainos pasiūlymo veiklos užregistruotos

Išsamiuose žurnaluose įrašomos visos vartotojo veiklos ir veiksmai, skirti kainos pasiūlymui. Veiklos žurnalas leidžia organizacijoms nustatyti, kas per naudojimo laikotarpį atnaujino kainos pasiūlymą ir kokie buvo naujinimai. Tai taip pat leidžia organizacijoms patvirtinti, kad tik įgalioti žmonės turi prieigą prie užantspauduotos kainos pasiūlymo. Veiklos žurnalas prieinamas kiekvieno kainos pasiūlymo **Veiklos** puslapyje.

### <a name="review-rfq-activity"></a>Peržiūrėti RFQ veiklą

Registruojama kiekviena sąveika su kainos pasiūlymu ir ją galima peržiūrėti **Veikla** puslapyje. Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys.

![Veiklos puslapio pavyzdys](media/sealed-bidding-rfq-activity.png "Veiklos puslapio pavyzdys")

Tiekėjai gali pasiekti **Veiklos** puslapį, pasirinkdami **Veikla** **Pasiūlymo patvirtinimo užantspauduotas kainos pasiūlymas** puslapyje. Įsigijimo personalas gali jį pasiekti,pasirenkant **Veikla** **Pasiūlymo patvirtinimo** puslapyje. Veiklos žurnalas teikia pilną matymą tiekėjams ir įsigijimo personalą, kurie turi prieigą prie kainos pasiūlymo. Todėl ji gali parodyti bet kokią neteisėtą prieigą.

### <a name="unseal-sealed-bids"></a>Atskleisti užantspauduotus kainų pasiūlymus

Kai pasibaigia **Galiojimo data ir laiko** vertė, kuri buvo sukonfigūruota užantspauduotos kainos pasiūlymo RFQ atvejui, **Atskleisti** mygtukas tampa aktyvus. Pasirinkite **Atskleisti** norėdami atskleisti visus pasirinkto RFQ atvejo kainos pasiūlymus. Tada visi kainos pasiūlymo duomenys ir priedai tampa matomi, kad būtų galima valdyti atsakymus į atvejį. Be to, sukuriami žurnalai, kuriuose yra pateikti kainos pasiūlymo duomenys.

Atskleidimo veiksmas registruojamas ir jį galima peržiūrėti **Veikla** puslapyje.

### <a name="process-accepted-bids"></a>Apdoroti priimtus kainos pasiūlymus

Anksčiau užantspauduotų kainų pasiūlymų lyginimo ir patvirtinimo procesai yra tokie pat, kaip atvirų kainų pasiūlymų procesas. Norėdami gauti informacijos apie tai, kaip gauti, palyginti, atmesti ir priimti atskleistų kainų pasiūlymus, žr. [Įvesti ir palyginti RFQ pasiūlymus ir premijų sutartis](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>RFQ veiklos žurnalo niekada negalima panaikinti

Niekas, net administratoriai ir "Microsoft" palaikymas negali redaguoti arba naikinti RFQ veiklos žurnalo. Šis apribojimas padeda užtikrinti užantspauduotos kainos pasiūlymo proceso teisingumą. Tai taip pat padeda užtikrinti, kad tvarkomas tikslus audito sekimas.
