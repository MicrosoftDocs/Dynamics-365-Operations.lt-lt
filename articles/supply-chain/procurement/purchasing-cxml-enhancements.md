---
title: cXML patobulinimų pirkimas
description: cXML patobulinimų pirkimo funkcija kuriama pagal esamą išorinio katalogo funkciją „PunchOut” (išėjimo laiko žymėjimas), kuri naudojama pirkimo paraiškoms.
author: dasani-madipalli
manager: tfehr
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: cd0435fd89050311ecd4f24400d5830cbcf8fdfd
ms.sourcegitcommit: b281ac04157f6ccbd159fc89f58910b430a3b6a9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826930"
---
# <a name="purchasing-cxml-enhancements"></a>cXML patobulinimų pirkimas

[!include [banner](../includes/banner.md)]

Funkcija _cXML patobulinimų pirkimas_ kuriama pagal [esamą išorinio katalogo funkciją](set-up-external-catalog-for-punchout.md), kuri naudojama pirkimo paraiškoms. Ši esama funkcija žinoma kaip _„PunchOut_”. Nors pirkimo užsakymas nebūtinai turi būti sukurtas pirkimo paraiškoje, tačiau turi būti ryšys tarp tiekėjo pirkimo užsakyme ir parametrų, kurie naudojami pirkimo užsakymo dokumento siuntimui.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>cXML patobulinimų pirkimo funkcijos įjungimas

Norėdami įjungti funkciją, atidarykite **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** puslapį ir ieškokite funkcijos, pavadintos *cXML patobulinimų pirkimas*. Pasirinkite funkciją ir tada pasirinkite **Įgalinti dabar**, kad ją įjungtumėte.

Įjungę funkciją, konfigūruokite parametrus šiose trijose srityse:

- **[cXML parametrai](#cxml-parameters)** – Naudokite šiuos parametrus, kad nustatytumėte kai kuriuos bendruosius pirkimo užsakymų siuntimo funkcijos parametrus.
- **[Tiekėjo sąranka](#vendor-setup)** – Jei commerce eXtensible Markup Language (cXML) turi būti naudojama pagal numatytuosius nustatymus visiems naujiems pirkimo užsakymams, sukurtiems bet kuriam tiekėjui, tuomet nustatykite pasirinktį **Pirkimo užsakymo siuntimas per cXML** kaip _Taip_ tam tiekėjui.
- **[Išoriniai katalogai](#external-catalog-setup)** – Naudokite naujus **Užsakymo ypatybių** parametrus, kad nustatytumėte pirkimo užsakymo dokumento formatą ir kaip jis bus siunčiamas.

Toliau pateiktoje iliustracijoje apibendrinama ši konfigūracija.

![cXML funkcijų nustatymo sritys](media/cxml-settings-areas.png "cXML funkcijų nustatymo sritys")

Be to, turite nustatyti [Pirkimo užsakymo užklausos paketinę užduotį](#po-batch). Ši paketinė užduotis naudojama patvirtintiems pirkimo užsakymams siųsti.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Bendrųjų cXML parametrų nustatymas

Naudokite **cXML parametrai** puslapį, kad nustatytumėte kelis bendruosius pirkimo užsakymų siuntimo funkcijos parametrus.

![cXML parametrų puslapis](media/cxml-parameters.png "cXML parametrų puslapis")

Eikite į **Paraiškos \> Nustatymai \> cXML valdymas \> cXML parametrai** ir nustatykite šiuos parametrus:

- **cXML testavimo režimas** – Šis bendrasis parametras veikia taip, kad pirkimo užsakymai faktiškai siunčiami iš paketinės užduoties. Pasirinkite vieną iš šių reikšmių:

    - **Tikrinimas** – Šiame režime gali būti paleista paketinė užduotis ir sugeneruotas pranešimo XML dokumentas, bet nėra siunčiamas. Vietoj to, jis įrašomas į pirkimo užsakymo užklausą peržiūros tikslais. Šis režimas naudingas, kai atliekate pradinį diegimą, ir norite matyti, kaip įvedami duomenys į cXML pranešimą. Galbūt norėsite generuoti laiškų pavyzdžius, kuriuos galite siųsti tiekėjams, kad atliktų pradinį tikrinimą.
    - **Tiesiogiai** – Šiame režime funkcija naudoja [išorinio katalogo parametrus](#external-catalog-setup), kad fiziškai perduotų kiekvieną dokumentą tiekėjui.

- **Siųsti pirkimo užklausos naujinimus** – Nustatykite šią pasirinktį kaip *Taip*, kad išsiųstumėte naujinimo pranešimą pirkimo užsakymams. Nustatykite šią pasirinktį kaip *Ne*, kad būtų išvengta pranešimo siuntimo. Dauguma tiekėjų nenori gauti naujinimo pranešimų. Vietoj to, jie reikalauja, kad klientai susisiektų su jais telefonu arba elektroniniu paštu, jei reikia pakeisti pirkimo užsakymą. Šis parametras yra bendrasis parametras, todėl kiekvieno tiekėjo išoriniame kataloge negalima nurodyti jokio perrašymo. Pirkimo užsakymas bus pažymėtas kaip atnaujintas, jei užregistruosite antrą patvirtinimą pirkimo užsakyme, o pirmasis patvirtinimas jau bus išsiųstas ir patvirtintas tiekėjo. Jei yra antrasis patvirtinimas, bet pirmasis patvirtinimas nebuvo išsiųstas, antrasis patvirtinimas bus laikomas nauju dokumentu. Galite patvirtinti pirkimo užsakymą tiek kartų, kiek norite, kol bus išsiųstas patvirtinimas. Kitas patvirtinimas tada bus laikomas naujinimo pranešimu.
- **Siųsti pirkimo užklausos naikinimą** – Nustatykite šią pasirinktį kaip *Taip*, kad išsiųstumėte naikinimo pranešimą pirkimo užsakymams. Nustatykite šią pasirinktį kaip *Ne*, kad būtų išvengta pranešimo siuntimo. Dauguma tiekėjų nenori gauti naikinimo pranešimų. Vietoj to, jie reikalauja, kad klientai susisiektų su jais telefonu arba elektroniniu paštu, jei pirkimo užsakymas buvo išsiųstas per klaidą. Šis parametras yra bendrasis parametras, todėl kiekvieno tiekėjo išoriniame kataloge negalima nurodyti jokio perrašymo. Pirkimo užsakymas bus pažymėtas kaip panaikintas, jei atšauksite pirkimo užsakymą „Supply Chain Management“.
- **Archyvuojami failai** – Nurodykite failo maršrutą, kur norite eksportuoti ir įrašyti archyvuotus cXML dokumentus. Maršrutas naudojamas paleidus šalinimo funkciją **Pirkimo užsakymo užklausos** puslapyje.
- **Maksimalus simbolių skaičius adreso eilutei** – Įveskite maksimalų simbolių skaičių, kurį galima naudoti lauke Gatvė, skirtame adresams, esančiuose cXML dokumente. Šis bendrasis parametras turi įtakos visiems tiekėjams, išskyrus atvejus, kai išorinio katalogo ypatybėse nurodytas perrašymas.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Nustatyti cXML naudojimą tiekėjo pirkimo užsakymams

Kiekvieną kartą, kai patvirtinate pirkimo užsakymą, kur pasirinktis **Siųsti pirkimo užsakymą naudojant cXML** nustatyta kaip _Taip_, sistema automatiškai sugeneruoja cXML pranešimą ir pateikia jį tiekėjui, susijusiam su tuo pirkimo užsakymu. Yra du būdai valdyti šią pasirinktį Jūsų pirkimo užsakymams:

- Norėdami nustatyti tiekėją taip, kad jis automatiškai naudos cXML visiems naujiems pirkimo užsakymams, sukurtiems iš paraiškos, eikite į **Paraiškos \> Tiekėjai \> Visi tiekėjai** ir pasirinkite arba sukurkite tiekėją, kad atidarytumėte jo informacijos puslapį. Tada „FastTab” **Pirkimo užsakymo numatytosios vertės** nustatykite pasirinktį **Siųsti pirkimo užsakymą naudojant cXML** kaip _Taip_. Jei cXML taip pat turi būti automatiškai naudojamas naujiems pirkimo užsakymams, kurie **nėra** sukurti iš paraiškos, taip pat turite nustatyti **ENABLEMANUALPO** užsakymo ypatybę kaip _Teisinga_ susijusiems išoriniams katalogams, taip kaip aprašyta šios temos vėlesniame skyriuje [Nustatyti užsakymo ypatybes](#set-order-properties).
- Atskiriems pirkimo užsakymams, eikite į **Paraiškos \> Pirkimo užsakymai \> Visi pirkimo užsakymai** ir pasirinkite arba sukurkite pirkimo užsakymą, kad atidarytumėte jo informacijos puslapį. Pereikite į rodinį **Antraštė**, o tada „FastTab” **Nustatymai** nustatykite pasirinktį **Siųsti pirkimo užsakymą naudojant cXML** kaip privalomą.

![Numatytieji tiekėjo pirkimo užsakymų parametrai](media/cxml-order-defaults.png "Numatytieji tiekėjo pirkimo užsakymų parametrai")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>cXML naudojimo išoriniam katalogui nustatymas

Puslapyje **Išoriniai katalogai** kiekvienam savo katalogui galite nustatyti „PunchOut” funkciją ir pirkimo užsakymų siuntimo funkciją. Norėdami rasti atitinkamus parametrus, eikite į **Paraiškos \> Katalogai \> Išoriniai katalogai**. Pradėkite nuo [kiekvieno katalogo nustatymo kaip įprasta](set-up-external-catalog-for-punchout.md). Šis procesas apima tiekėjo priskyrimą, kategorijų, kurias tiekėjas gali tiekti, pasirinkimą ir katalogo aktyvinimą. Tada konfigūruokite papildomus parametrus, aprašytus šiame skyriuje.

> [!NOTE]
> Kai patvirtinate pirkimo užsakymą, kuris gali būti siunčiamas per cXML, sistema peržvelgia su pirkimo užsakymu susietą tiekėją, o tada suranda pirmąjį aktyvų išorinį katalogą, susietą su tuo tiekėju. Tada sistema naudoja to išorinio katalogo parametrus, kad galėtų siųsti pirkimo užsakymą. Jei nustatyti keli išoriniai katalogai, sistema, remdamasi pirkimo užsakymo tiekėju, naudoja tik pirmąjį išorinį katalogą, kurį suranda. Todėl rekomenduojame sukurti tik po vieną išorinį katalogą kiekvienam tiekėjui.

![Išorinio katalogo parametrai](media/cxml-supplier-catalog.png "Išorinio katalogo parametrai")

### <a name="set-the-punchout-protocol-type"></a>„PunchOut” protokolo tipo nustatymas

Puslapio **Išoriniai katalogai** „FastTab” **Bendra**, nustatykite **„Punchout” protokolo tipas** lauką kaip _cXML_. Ši pasirinktis bus vienintelė galima pasirinktis, išskyrus tuos atvejus, kai partneris išplėtė funkcijas ir pateikia papildomą pasirinktį plėtinyje.

Jei taip pat naudojate „PunchOut” katalogą, taip pat turite [nustatyti pranešimo formatą](set-up-external-catalog-for-punchout.md). Pranešimo formatas naudojamas norint užmegzti ryšį su tiekėju paraiškos „PunchOut” operacijoje. Kai pirkimo užsakymas išsiųstas, užsakymo ypatybės bus naudojamos užmegzti ryšį su tiekėju.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Užsakymo ypatybių nustatymas

Funkcija _cXML patobulinimų pirkimas_ prideda naują **Užsakymo ypatybės** „FastTab” išoriniams katalogams. Šis „FastTab” pateikia tinklelį, kuriame galite apibrėžti užsakymo ypatybes. Jis taip pat pateikia įrankių juostą. Į šią įrankių juostą įeina šie trys mygtukai, kuriuos galite naudoti užsakymo ypatybėms tvarkyti:

- **Numatytosios ypatybės** – Kai nustatote naują katalogą, pasirinkite šį mygtuką, kad įtrauktumėte iš anksto apibrėžtą dažniausiai naudojamų ypatybių rinkinį į tinklelį.
- **Naujas** – Įtraukite naują ypatybę į tinklelį.
- **Naikinti** – Naikinti šiuo metu tinklelyje pasirinktą ypatybę. Jei netyčia panaikinote numatytąją ypatybę, pasirinkite **Numatytąsias ypatybes**, kad atkurtumėte visas trūkstamas ypatybes.

Kiekvieną kartą, kai į tinklelį įtraukiate vieną ar daugiau ypatybių, naudokite dešinįjį stulpelį, kad nurodytumėte kiekvienos ypatybės reikšmę.

Naudokite numatytąsias ypatybes tokiu būdu:

- **PIRKĖJO\_SLAPUKAS** – Šis sekimo laukas gali būti naudojamas norint nurodyti konkrečią Jūsų įmonės informaciją. Jei neturite sutarties su tiekėju dėl šios ypatybės naudojimo, tuomet nesvarbu kada siųsti pirkimo užsakymą. Todėl turite ją nustatyti kaip paprastą reikšmę.
- **PRISTATYTI** – Kai siuntimo adresas įvedamas į pirkimo užsakymo dokumentą, laukas **Svarbi informacija** naudojamas norint nustatyti **Pristatyti** lauką XML pranešime. Jei reikalaujate, kad ši reikšmė būtų prašytojo pavadinimas ir nustatysite lauką prašytojui pirkimo užsakymo antraštėje, įveskite _PRAŠYTOJAS_ reikšmę šiai ypatybei, tam, kad prašytojo pavadinimas būtų įvestas į **Pristatyti** lauką, esantį XML. Šiuo atveju, pagrindinis el. pašto adresas ir telefono numeris, kurie yra naudojami, bus iš prašytojo, o ne užsakovo.
- **DIEGIMOREŽIMAS** – Nustatykite šią ypatybę, kaip reikalauja tiekėjas. Paprastai reikšmės yra _GAMYBA_ arba _TIKRINIMAS_. Nustatykite reikšmę pagal Jūsų ryšį su tiekėju. Paprastai ji turi atitikti numatytą sistemą, esančią už **UŽSAKYMOPATIKROSURL** reikšmės, kurią tiekėjas nurodo kaip tikrinimo ar gamybos sistemą.
- **FIKSUOTOADRESOID** – Kai **adresoID** laukas nustatytas XML pranešime, jis paima vietą, nurodytą ant adreso. Jei ID reikšmė, kurią pranešėte tiekėjui, dėl tam tikrų priežasčių skiriasi nuo reikšmės, nurodytos ant adreso vietos, galite priverstinai vykdyti perrašymą, nurodydami reikšmę čia. Prielaida yra ta, kad su tiekėju naudosite tik vieną adresą, ir kad adresas bus nustatytas tiekėjo sistemoje. Saskaitų siuntimo adresas yra pirminis juridinio subjekto, esančio „Supply Chain Management“, SF adresas.
- **FIKSUOTOSIUNTIMOADRESOID** – Kai **adresoID** laukas nustatytas XML pranešime, jis paima vietą, nurodytą ant adreso. Jei ID reikšmė, kurią pranešėte tiekėjui, dėl tam tikrų priežasčių skiriasi nuo reikšmės, nurodytos ant adreso vietos, galite priverstinai vykdyti perrašymą, nurodydami reikšmę čia. Prielaida yra ta, kad su tiekėju naudosite tik vieną adresą, ir kad adresas bus nustatytas tiekėjo sistemoje. Siuntimo adresas yra adresas, nurodytas pirkimo užsakymo antraštėje. Dauguma tiekėjų priima tik antraštės adresus, o ne eilutės adresus. Nors XML yra laukų, skirtų eilučių adresams, jie bus nustatyti kaip antraštės adresas.
- **IŠ\_DOMENO** – Įveskite reikšmę, kuri bus naudojama pirkimo užsakymo dokumentų siuntimui. Šią reikšmę pateikia Jūsų tiekėjas.
- **IŠ\_TAPATYBĖS** – Įveskite reikšmę, kuri bus naudojama pirkimo užsakymo dokumentų siuntimui. Šią reikšmę pateikia Jūsų tiekėjas.
- **UŽSAKYMOPATIKROSURL** – Įveskite URL, kur persiųsite pirkimo užsakymo dokumentus. Šis URL prasideda `https://` ir pateikiamas Jūsų tiekėjo.
- **MOKAMOSIOSKROVOS\_ID** – Įveskite mokamosios krovos ID prefikso vertę, kaip to reikalaujama verslo procesams, esantiems dabartinio tiekėjo vietoje.
- **SIUNTĖJO\_DOMENAS** – Įveskite reikšmę, kuri bus naudojama pirkimo užsakymo dokumentų siuntimui. Šią reikšmę pateikia Jūsų tiekėjas.
- **SIUNTĖJO\_TAPATYBĖ** – Įveskite reikšmę, kuri bus naudojama pirkimo užsakymo dokumentų siuntimui. Šią reikšmę pateikia Jūsų tiekėjas.
- **BENDRINAMAS\_SLAPTASIS RAKTAS** – Įveskite reikšmę, kuri bus naudojama pirkimo užsakymo dokumentų siuntimui. Šią reikšmę pateikia Jūsų tiekėjas.
- **GATVĖSILGIS** – Įveskite skaičių, kuris žymi didžiausią simbolių skaičių, kurį tiekėjas priims kaip gatvės pavadinimą. Jei reikšmė įvesta čia, ji keičia reikšmę, nurodytą **cXML parametrų** puslapyje. Sistema panaikins eilučių lūžius ir tarpus, kad bandytų sutalpinti standartinį „Supply Chain Management“ adresą į čia nurodytą simbolių skaičių. Bet kurie papildomi simboliai bus sutrumpinti.
- **Į\_DOMENĄ** – Įveskite reikšmę, kuri bus naudojama pirkimo užsakymo dokumentų siuntimui. Šią reikšmę pateikia Jūsų tiekėjas.
- **Į\_TAPATYBĘ** – Įveskite reikšmę, kuri bus naudojama pirkimo užsakymo dokumentų siuntimui. Šią reikšmę pateikia Jūsų tiekėjas.
- **VARTOTOJOAGENTAS** – Įveskite reikšmę, kad nustatytumėte sistemą, kurią naudojate. Pavyzdžiui, įveskite _„Dynamics 365 Supply Chain Management”_.
- **VERSIJA** – Įveskite cXML versijos numerį, jei tiekėjas prašo šios informacijos. Numatytoji versija yra *1.2.008*. Ši versija yra stabili ir ją priima dauguma tiekėjų.
- **ATSAKYMOTEKSTAS** – Įveskite bet kokį pasirinktinį tekstą, kurį tikitės, kad tiekėjas grąžins kaip cXML atsakymo pranešimą po to, kai užsakymas buvo išsiųstas. Tokiu būdu sistema gali pažymėti pranešimą kaip _Patvirtintą_. Jei atsakymas nesutampa su standartiniu tekstu arba kliento tekstu, kurį čia įvedėte, užklausa bus pažymėta kaip _Klaida_.
- **PAPILDOMASATSAKYMOTEKSTAS** – Nustatykite šią ypatybę kaip _TEISINGĄ_, jei norite ieškoti tiekėjo atsakymo teksto apie reikšmes, nurodytas lauke **ATSAKYMOTEKSTAS**. Pavyzdžiui, tiekėjas gali grąžinti ilgą eilutę, į kurią įtraukiamas atsakymas „Gerai”. Tokiu atveju galite įvesti _Gerai_ lauke **ATSAKYMOTEKSTAS** ir nustatyti **PAPILDOMĄATSAKYMOTEKSTĄ** kaip _TEISINGĄ_, kad būtų galima ieškoti funkcijos „Gerai” bet kurioje atsakymo vietoje. Tada užsakymą galima nustatyti kaip _Patvirtintą_.
- **TURINIOTIPAS** – Įprastoje katalogo sąrankoje nereikia nustatyti šios ypatybės. Jei siųsdami pirkimo užsakymą gaunate serverio 500 klaidą iš tiekėjo sistemos, galite atlikti tikrinimą, nustatydami šią ypatybę kaip _KLAIDINGA_. Ši reikšmė pakeis svetainės užklausos parametrą ir galbūt įgalins pranešimo siuntimą kai kurioms platformoms.
- **ĮGALINTIANTRAŠTES** – Nustatykite šią ypatybę kaip _TEISINGĄ_, kad antraštės būtų siunčiamos kartu su pirkimo užsakymu. Šią ypatybę turite nustatyti tik tuo atveju, jei tiekėjas to reikalauja. Jei šią ypatybę nustatysite kaip _TEISINGĄ_, pridėkite papildomas pasirinktines ypatybes, kurios pagrįstos tiekėjo teikiamais pavadinimais, ir prie jų pridėkite prefiksą _H\__. Tipiniai pavyzdžiai yra **H\_VARTOTOJOID**, **H\_SLAPTAŽODIS**, **H\_GAVĖJOID** ir **H\_VEIKSMOUŽKLAUSA**. Šios pasirinktinės ypatybės įtrauktos į numatytąsias ypatybes:

    - **H\_VARTOTOJOID** – Jei prekybos partneris reikalauja, kad atsiųstumėte vartotojo ID kaip URL dalį, kad būtų galima pateikti pirkimo užsakymą, įveskite reikšmę čia.
    - **H\_SLAPTAŽODIS** – Jei prekybos partneris reikalauja, kad atsiųstumėte slaptažodį kaip URL dalį, kad būtų galima pateikti pirkimo užsakymą, įveskite reikšmę čia.

- **ĮGALINTIRANKINĮPU** – Jei ši ypatybė nustatyta kaip _TEISINGA_, kai vartotojai rankiniu būdu sukuria pirkimo užsakymus (t.y. kai jie nepradedami iš paraiškos), šie pirkimo užsakymai perims iš tiekėjo **Pirkimo užsakymo siuntimas naudojant cXML** pasirinkties parametrą. Jei ši ypatybė nenustatyta, arba, jei ji nustatyta kaip _KLAIDINGA_, pasirinktis **Pirkimo užsakymo siuntimas naudojant cXML** nebus nustatyta pirkimo užsakymo antraštėje rankiniu būdu sukurtiems pirkimo užsakymams. Pirkimo užsakymams, sukurtiems iš paraiškos, pasirinkties **Pirkimo užsakymo siuntimas naudojant cXML** parametras visada yra perimtas iš tiekėjo, nepaisant šios ypatybės parametro. Norėdami gauti daugiau informacijos, žr. [Nustatyti cXML naudojimą tiekėjo pirkimo užsakymams](#vendor-setup) skyrių, esantį šioje temoje anksčiau.
- **TIKPUNCHOUTPU** – Jei ši ypatybė nustatyta kaip _TEISINGA_, tuomet tik „PunchOut” proceso metu sukurtos pirkimo paraiškos eilutės nustatys **Pirkimo užsakymo siuntimas naudojant cXML** pasirinktį pirkimo užsakymo antraštėje. Be to, visų pirkimo užsakymo eilučių pirkimo paraiškos eilutės tipas privalo būti _Išorinio katalogo prekė_. Kitu atveju, negalima sukurti cXML pirkimo užsakymo.
- **PUNCHOUTGAVĖJAS** – Jei ši ypatybė nustatyta kaip _TEISINGA_, numatytasis juridinio subjekto adresas bus pridėtas į „PunchOut” sąrankos užklausos pranešimą, kai vartotojas atidaro išorinį katalogą. Šis adresas pridedamas kaip **Siuntosgavėjo** adresas. Tiekėjai naudos **Siuntosgavėjo** adresą, kad būtų rodomi įkainiai, pagrįsti įmonės vieta.
- **PUNCHOUTSEKIMAS** – Nustatyti šią ypatybę kaip _TEISINGĄ_, jei bandant peržiūrėti išorinį katalogą iš paraiškos gaunate klaidos pranešimą. Sekimo informacija tuomet bus įrašyta **„PunchOut”nustatymoužklausa** ir **„PunchOut”atsakymas** pranešimuose, kurie siunčiami tarp „Supply Chain Management“ ir tiekėjo svetainės. Šią informaciją galite peržiūrėti **cXML krepšelio pranešimų žurnalo** puslapyje, kurį galite atidaryti **Išorinio katalogo sąrankos** puslapyje, skirtame tiekėjo katalogui, su kuriuo turite problemų. Šią ypatybę turite nustatyti kaip _TEISINGĄ_ tik tuo atveju, jei atliekate trikčių diagnostiką, nes ji sukuria per didelį našumą duomenų bazėje kiekvienam „PunchOut”. Norėdami gauti daugiau informacijos, žr. [Peržiūrėti išorinio katalogo „PunchOut” cXML krepšelio pranešimų žurnalą](#message-log) skyrių, esantį šioje temoje vėliau.
- **PAKEISTINAUJĄEILUTĘ** – Nustatykite šią ypatybę kaip _TEISINGĄ_, jei iškilo problema, nes tiekėjo sistema siunčia **„PunchOut”atsakymas** pranešimą, į kurį įtraukiami naujos eilutės simboliai (\\n). Ši problema gali kilti, jei tiekėjo pranešimai yra išanalizuoti naudojant programinę įrangą arba įsigijimų stebulę. Jeigu kyla problemų dėl naujo tiekėjo nustatymo, nustatykite **PUNCHOUTSEKIMAS** ypatybę kaip _TEISINGĄ_, kad peržiūrėtumėte **„PunchOut”atsakymo** pranešimą ir nustatytumėte, ar XML žymės išskaidomos naujų eilučių simbolių.
- **PUKOMENTARAI** – Nustatykite šią ypatybę kaip _TEISINGĄ_, jei norite, kad į cXML dokumentą būtų įtrauktos pastabos, pridėtos prie pirkimo užsakymo „Supply Chain Management“. Priedo tekstas yra įtrauktas į antraštės komentarus pirkimo užsakymo pranešime. Norėdami gauti daugiau informacijos apie tai, kaip sistema pasirenka ir apdoroja šiuos priedus, žr. [Pridėti pastabas pirkimo užsakyme](#attach-po-notes) skyrių, esantį šioje temoje vėliau.
- **TIEKĖJOKOMENTARAI** – Nustatykite šią ypatybę kaip _TEISINGĄ_, jei norite, kad į cXML dokumentą būtų įtrauktos pastabos, pridėtos prie pirkimo užsakymo „Supply Chain Management“. Priedo tekstas yra įtrauktas į antraštės komentarus pirkimo užsakymo pranešime. Norėdami gauti daugiau informacijos apie tai, kaip sistema pasirenka ir apdoroja šiuos priedus, žr. [Pridėti pastabas prie pirkimo užsakymo](#attach-po-notes) skyrių.
- **VALYTIAMP** – Nustatykite šią ypatybę kaip _TEISINGĄ_, jei gaunate klaidos pranešimą, kai bandote atlikti „PunchOut” tiekėjui, o tiekėjo grąžinimo URL apima neteisingai užkoduotus ampersandus (\&).
- **PUNCHOUTTZ** – Nustatykite šią ypatybę kaip _TEISINGĄ_, jei tiekėjas su kuriuo dirbate naudoja tarptautinės standartizacijos organizacijos (ISO) 8601 standartą tam, kad būtų galima atlikti „PunchOut” užklausos pranešimo datos/laiko specialų patikrinimą. „Supply Chain Management“ naudoja pasaulinio koordinuotojo laiko (UTC) datą **„PunchOut”sąrankosužklausos** pranešime. Todėl, kai nustatysite šią ypatybę kaip _TEISINGĄ_, *+ 00:00* bus pridėtas prie datos/laiko formato.
- **WMSADRESOID** – Nustatykite šią ypatybę kaip _TEISINGĄ_, jei norite naudoti sandėlio numerį, esantį pirkimo užsakymo antraštėje, kaip **adresoID** vertę, nurodytą ant pirkimo užsakymo užklausos, kuri siunčiama tiekėjui, **Siuntimogavėjo** adreso. Jei nustatysite vertę **FIKSUOTOSIUNTIMOADRESOID** ypatybei, ta reikšmė bus viršesnė už šią reikšmę. Todėl turėtumėte naudoti vieną iš ypatybių, norėdami **Siuntimogavėjo** adrese nustatyti **adresoID** vertę dokumentui.
- **PUNCHOUTSIŲSTIVARTOTOJUI** – Ši ypatybė naudojama kartu su **PUNCHOUTGAVĖJO** ypatybe. Jei **PUNCHOUTGAVĖJAS** nustatytas kaip _TEISINGAS_, juridinio subjekto adresas paimamas. Jei **PUNCHOUTSIŲSTIVARTOTOJUI** nustatyta kaip _TEISINGA_, naudojamas „PunchOut” vartotojo pagrindinis adresas vietoj juridinio subjekto adreso.

### <a name="activate-the-external-catalog"></a>Išorinio katalogo suaktyvinimas

Kai baigsite nustatyti visas ypatybes ir konfigūruosite kitus Jūsų išorinio katalogo parametrus, grįžkite atgal į „FastTab” **Bendra**, esantį **Išorinių katalogų** puslapyje ir nustatykite pasirinktį **Aktyvus** kaip *Taip*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Pridėti pastabas prie pirkimo užsakymo

Kaip buvo minėta skyriuje [Nustatyti užsakymo ypatybes](#set-order-properties), jei norite, kad į Jums pristatytą cXML būtų įtrauktas tekstas iš pastabų, pridėtų prie atitinkamo pirkimo užsakymo ir/arba tiekėjo įrašų, galite nustatyti **PUKOMENTARAI** ir/arba **TIEKĖJOKOMENTARAI** ypatybę kaip _TEISINGĄ_ išorinio katalogo nustatyme. Šiame skyriuje pateikiama išsamesnė informacija apie tai, kaip sistema pasirenka ir apdoroja šiuos priedus, jei juos naudojate.

Norėdami nustatyti pastabų, kurias sistema ieškos, tipus, eikite į **Paraiškos \> Nustatymai \> Formos \> Formos nustatymai**. Tada skirtuke **Pirkimo užsakymas** nustatykite lauką **Įterpiamų dokumentų tipas** tokiam pastabų tipui, kurį norėtumėte įterpti. Bus įtrauktos tik teksto pastabos, o ne dokumentų priedai.

![Formuoti sąrankos puslapį](media/cxml-form-setup.png "Formuoti sąrankos puslapį")

Priedai bus įtraukti į pirkimo užsakymą tik jei jų **Tipo** laukas nustatytas kaip reikšmė, kurią pasirinkote **Įterpiamų dokumentų tipas** lauke, ir jei jų **Apribojimų** laukas nustatytas kaip _Išorinis_. Norėdami sukurti, peržiūrėti arba redaguoti pirkimo užsakymo priedus, eikite į **Paraiškos \> Visi pirkimo užsakymai**, pasirinkite arba sukurkite pirkimo užsakymą, o tada pasirinkite **Priedai** mygtuką (sąvaržėlės simbolis), esantį viršutiniame dešiniajame kampe.

![Pridėta pastaba, nustatyta siųsti tiekėjui](media/cxml-note-to-vendor.png "Pridėta pastaba, nustatyta siųsti tiekėjui")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Peržiūrėti „PunchOut” išorinio katalogo cXML krepšelio pranešimų žurnalą

Kai nustatysite **„Punchout” protokolo tipo** lauką kaip _cXML_ išoriniam katalogui, sistema užfiksuos iš tiekėjų grįžtančių krepšelių pranešimų žurnalą. Šį žurnalą galima naudoti trikčių diagnostikai ir kitiems duomenų tikslams.

Norėdami atidaryti išorinio katalogo žurnalą, pasirinkite atitinkamą katalogą ir tada veiksmų srityje pasirinkite **cXML krepšelio pranešimų žurnalą**. **cXML krepšelio pranešimų žurnalo** puslapyje rodomas grąžintų krepšelių sąrašas, XML, susijęs su tais krepšeliais, ir eilutės, kurios buvo sukurtos atitinkamoje pirkimo paraiškoje.

![cXML krepšelio pranešimų žurnalo puslapis](media/cxml-cart-message-log.png "cXML krepšelio pranešimų žurnalo puslapis")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Nustatyti išorinio katalogo „PunchOut” išorinius elementus

Nustatę **„Punchout” protokolo tipo** lauką kaip *cXML* išoriniam katalogui, galite pridėti pasirinktinius išorinius elementus, kurie bus įterpiami į tinkamą vietą XML užklausos pranešime.

Norėdami į išorinį katalogą įtraukti išorinius elementus, atlikite šiuos veiksmus.

1. Eikite į **Paraiškos \> Katalogai \> Išoriniai katalogai**.
1. Pasirinkite reikalingą katalogą.
1. „FastTab” **Pranešimo formatas**, skyriuje **Išorinis**, pasirinkite **Pridėti**, kad pridėtumėte eilutę į kiekvieno išorinio elemento, kurį norite įtraukti, tinklelį. Kiekvienoje eilutėje nustatykite šiuos laukus:

    - **Pavadinimas** – Įveskite pavadinimą elementui. Ši vertė taps **Išorinio** XML elemento, sukurto pagal kiekvieną eilutę, **pavadinimo** atributo verte. Paprastai dirbsite su savo tiekėju, kad susitartumėte dėl kiekvieno išorinio elemento pavadinimo.
    - **Vertė** – Pasirinkite elemento vertę. Ši vertė taps XML elemento, sukurto pagal kiekvieną eilutę, verte. Galimos šios vertės:

        - **Vartotojo vardas** – Naudokite vartotojo, atliekančio „PunchOut”, vardą. Šis vardas yra „Supply Chain Management“ prisijungimo vardas.
        - **Vartotojo el. paštas** – Naudokite vartotojo, atliekančio „PunchOut”, el. pašto adresą. Šis adresas yra adresas, kurį vartotojas nustatė **Vartotojo pasirinkčių** puslapyje, skirtuke **Paskyra**.
        - **Atsitiktinė vertė** – Naudokite skirtingą atsitiktinę vertę.
        - **Vartotojo visas vardas** – Naudokite visą kontaktinio asmens, kuris yra susijęs su vartotoju, turinčiu prieigą prie išorinio katalogo, vardą.
        - **Vardas** – Naudokite kontaktinio asmens, kuris yra susijęs su vartotoju, turinčiu prieigą prie išorinio katalogo, vardą.
        - **Pavardė** – Naudokite kontaktinio asmens, kuris yra susijęs su vartotoju, turinčiu prieigą prie išorinio katalogo, pavardę.
        - **Telefono numeris** – Naudokite kontaktinio asmens, kuris yra susijęs su vartotoju, turinčiu prieigą prie išorinio katalogo, pagrindinį telefono numerį.

![Išorinių elementų parametrai](media/cxml-extrinsics.png "Išorinių elementų parametrai")

Vartotojas arba administratorius nematys išorinių elementų, nes jie nėra įtraukiami, kol vartotojas neatliks „PunchOut”. Jie bus automatiškai įterpti tarp **Pirkėjoslapuko** ir **Naršyklėsformosįrašo** elementų cXML nustatymo užklausos pranešime. Todėl konfigūruojant išorinį katalogą Jums nereikia nustatyti jų rankiniu būdu XML.

![Išoriniai elementai įtraukti į XML](media/cxml-extrinsics-xml.png "Išoriniai elementai įtraukti į XML")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Pirkimo užsakymo kūrimas ir apdorojimas

Kai kuriate pirkimo užsakymą tiekėjui, jis perims **Pirkimo užsakymo siuntimas naudojant cXML** pasirinkties parametrą iš to tiekėjo. Tačiau parametras išlieka pasiekiamas pirkimo užsakymo **Antraštės** rodinio „FastTab” **Nustatymai**, tam kad galėtumėte jį vėliau pakeisti kaip būtiną.

![Pirkimo užsakymas nustatytas cXML naudojimui](media/cxml-purchase-order.png "Pirkimo užsakymas nustatytas cXML naudojimui")

Kai sukursite pirkimo užsakymą iš pirkimo paraiškos, kuri buvo gauta iš „PunchOut” srauto, bus įrašyta visa reikiama eilutės informacija. Tada galite rankiniu būdu pridėti pirkimo užsakymo eilutes arba nukopijuoti jas iš kitų pirkimo užsakymų. Įsitikinkite, kad nustatėte visus privalomus laukus. Šie privalomi laukai apima išorinį nuorodos numerį, kuris yra tiekėjo numeris ir kuris bus naudojamas cXML pranešime.

![Išorinio nuorodos numerio pavyzdys](media/cxml-line-details.png "Išorinio nuorodos numerio pavyzdys")

Baigę užpildyti visą pirkimo užsakymo informaciją, įsitikinkite, kad patvirtinote. Joks pranešimas nebus išsiųstas, jei nebus patvirtintas pirkimo užsakymas. Kad patvirtintumėte pirkimo užsakymą, veiksmų srityje, skirtuke **Pirkimai**, grupėje **Veiksmai** pasirinkite **Patvirtinti**. 

Patvirtinus pirkimo užsakymą, patvirtinimo būseną galite peržiūrėti **Pirkimo užsakymų patvirtinimų** žurnaluose. Veiksmų srityje, skirtuke **Pirkimai**, grupėje **Žurnalai**, pasirinkite **Pirkimo užsakymų patvirtinimai**.

Kiekvienas pirkimo užsakymas gali turėti daug patvirtinimų. Kiekvienas patvirtinimas pažymėtas papildančiuoju numeriu. Šioje iliustracijoje pirkimo užsakymas yra *00000275*, o patvirtinimas yra *00000275-1*. Šis numeravimas atspindi standartines „Supply Chain Management“ funkcijas, kur pirkimo užsakymo pakeitimai ir todėl cXML pranešimo tipas, kuris turi būti siunčiamas tiekėjui, yra nustatomi remiantis patvirtinimu. Kaip rodo iliustracija, į **Pirkimo užsakymų patvirtinimų** puslapį taip pat įtraukti **Užsakymo siuntimo būsenos** ir **Užsakymo užklausos tiekėjo būsenos** laukai. Daugiau informacijos apie įvairias būsenos reikšmes, kurias galbūt matysite šiame puslapyje, žr. [Pirkimo užsakymo užklausų stebėjimas](#monitor-po-requests) skyrių, esantį šioje temoje vėliau.

![Pirkimo užsakymų patvirtinimų puslapis](media/cxml-po-confirmations.png "Pirkimo užsakymų patvirtinimų puslapis")

Norėdami peržiūrėti daugiau informacijos apie dokumentą, virš tinklelio pasirinkite **Pirkimo užsakymo užklausą**.

**Pirkimo užsakymo užklausos** puslapyje yra du tinkleliai. Tinklelyje, esančiame viršutinėje puslapio dalyje, yra po vieną kiekvieno pirkimo užsakymo, kuris pažymėtas siųsti, įrašą. Tinklelis skirtuke **Pirkimo užsakymo užklausos retrospektyva**, esančiame apatinėje puslapio dalyje, gali apimti kelis pasirinkto pirkimo užsakymo įrašus, kad nurodyti kiekvieno patvirtinimo būseną. Šioje iliustracijoje rodomas pirkimo užsakymas 00000275, esantis viršutiniame tinklelyje, ir dokumentas 00000275-1, esantis tinklelyje, esančiame skirtuke **Pirkimo užsakymo užklausos retrospektyva**.

![Pirkimo užsakymo užklausos puslapis](media/cxml-po-request.png "Pirkimo užsakymų užklausos puslapis")

Jei nustatyta ir paleista paketinė užduotis, dokumentas bus išsiųstas. Po to, kai dokumentas bus išsiųstas, galite peržiūrėti būsenos pasikeitimą. Šioje iliustracijoje **Užsakymo siuntimo būsenos** laukas nustatytas kaip _Išsiųsta_. **Užsakymo užklausos tiekėjo būsenos** laukas nustatytas kaip _Patvirtinta_, kad nurodyti, jog tiekėjas gavo dokumentą ir pavyko jį perskaityti bei saugoti savo sistemoje. **Pirkimo užsakymo užklausos retrospektyvos** skirtuke esantis tinklelis nurodo laiką, kada dokumentas buvo išsiųstas. Daugiau informacijos apie įvairias būsenos reikšmes, kurias galbūt matysite šiame puslapyje, žr. [Pirkimo užsakymo užklausų stebėjimas](#monitor-po-requests) skyrių.

![Būsenos pranešimai pirkimo užsakymo užklausos puslapyje](media/cxml-po-request-2.png "Būsenos pranešimai pirkimo užsakymo užklausos puslapyje")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Pirkimo užsakymo paketinės užduoties planavimas

Norėdami suaktyvinti paketines užduotis, skirtas pirkimo užsakymo užklausoms siųsti, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Nustatymas \>cXML valdymas \> Pirkimo užsakymo užklausa**, tada veiksmų srities skirtuke **Pirkimo užsakymo užklausa** esančioje **Paketų grupėje** pasirinkite **Pateikti užduotį**, kad būtų atidarytas **Pirkimo užklausos parengimas ir siuntimo** dialogo langas. Galite naudoti šį dialogo langą, kad nustatytumėte pasikartojimą, taip pat, kaip įprastai atliekate paketines užduotis „Supply Chain Management“. Pasirinkite intervalą, pagrįstą jūsų užsakymo kiekiu. Nors jūs galite vykdyti paketinę užduotį kas minutę, turbūt geriausia siųsti paketus visą darbo dieną, remiantis užsakymo gavimo langai, kurie atitinka jūsų tiekėjų grafikus.

Pavyzdžiui, jūsų tiekėjas turi strategiją, kuri nurodo, kad visi užsakymai, gauti iki 13 val. bus išsiųsti tą pačią dieną. Tokiu atveju jums gali tekti paleisti paketą tik kelis kartus ryte, kad galėtumėte pateikti visus turimus užsakymus. Tada likę užsakymai bus siunčiami kitą dieną. Šis sprendimas yra grynai verslo sprendimas. Galite jį peržiūrėti ir jo parametrus nustatyti atitinkamai.

Procesas ieškos pirkimo užsakymo užklausos dokumentų, kurių būsena yra *Laukiama*. Jei turite užsakymą, kurį turite nusiųsti tiekėjui nedelsiant, galite pasirinkti **Pateikti užduotį** ir nustatyti pasirinktį **Paketinis vykdymas** į *Ne*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Pirkimo užsakymo užklausų stebėjimas

### <a name="view-the-status-of-a-purchase-order"></a>Pirkimo užsakymo būsenos peržiūra

Kai užsakymai, kuriuos galima siųsti per cXML, yra patvirtinami, jie eina į _Laukiama_ būseną. Kaip buvo aprašyta skyriuje [Pirkimo užsakymo sukūrimas ir apdorojimas](#create-po), pirkimo užsakymo užklausos būseną galite peržiūrėti puslapyje **Pirkimo užsakymo užklausa**. Kiekviena pirkimo užsakymo užklausa gali turėti vieną iš kelių būsenų, atsižvelgiant į jos parametrus ir duomenis. Šiame skyriuje aprašomi įvairūs būsenos tipai ir reikšmės, kurias jie gali turėti. Ši informacija gali padėti jums valdyti problemas ir suprasti jūsų pirkimo užsakymų būseną.

![Pirkimo užsakymo būsena pirkimo užsakymo užklausos puslapyje](media/cxml-monitor-po-request.png "Pirkimo užsakymo būsena pirkimo užsakymo užklausos puslapyje")

Tinklelyje, esančiame viršutinėje **Pirkimo užsakymo užklausos** puslapio dalyje gali būti rodomos šios būsenos reikšmės:

- **Užsakymo siuntimo būsena** – šis laukas gali turėti vieną iš toliau nurodytų reikšmių:

    - **Laukiama** – dokumentas laukia išsiuntimo.
    - **Išsiųsta** – dokumentas yra išsiųstas.
    - **Sustabdyta** – dokumentas buvo pažymėtas kaip _sustabdytas_ prieš jį išsiunčiant . (Norėdami pažymėti dokumentą kaip _Sustabdytą,_ veiksmų srities puslapyje **Pirkimo užklausos** pasirinkite **Sustabdyti**.)
    - **Archyvuota** – dokumentas buvo išvalytas. (Norėdami išvalyti dokumentą, pasirinkite **Išvalyti** veiksmų srities puslapyje **Pirkimo užklausos**.)

- **Užsakymo tiekėjo užklausos būsena** – šis laukas gali turėti vieną iš toliau nurodytų reikšmių:

    - **Laukiama** – dokumentas laukia išsiuntimo.
    - **Patvirtintas** – tiekėjas patvirtino, kad dokumentas buvo gautas. Galite peržiūrėti išsamų iš tiekėjo grąžinamą XML pranešimą, pasirinkdami **Atsakymo XML** skirtuką apatinėje puslapio dalyje.
    - **Klaida** – dokumentas buvo išsiųstas tiekėjui, tačiau įvyko klaida. Galite peržiūrėti klaidos pranešimą, pasirinkdami **Atsakymo XML** skirtuką apatinėje puslapio dalyje.

Tinklelyje **Pirkimo užsakymo užklausų istorija,** esančiame apatinėje puslapio **Pirkimo užsakymo užklausos** dalyje gali būti rodomos šios vertės:

- **Užsakymo užklausos tipas** – šis laukas gali turėti vieną iš toliau nurodytų reikšmių:

    - **Nauja** – eilutė pažymima kaip nauja iškart po pirkimo užsakymo patvirtinimo.
    - **Atnaujinta** – jei patvirtinimas jau buvo išsiųstas ir patvirtintas tiekėjo, kitas patvirtinimas bus pažymėtas kaip _Atnaujinimas_. Atnaujinimai bus siunčiami tik jei parinktis **Siųsti pirkimo užklausos atnaujinimus** nustatyta į *Taip* [visuotiniuose cXML parametruose](#cxml-parameters).
    - **Panaikinta** – jei patvirtinimas jau išsiųstas ir patvirtintas tiekėjo, bet pirkimo užsakymas atšauktas, laukiantis patvirtinimas bus pažymėtas kaip _Panaikinta_. Panaikinimai bus siunčiami tik jei parinktis **Siųsti pirkimo užklausos panaikinimus** nustatyta į *Taip* [visuotiniuose cXML parametruose](#cxml-parameters).

- **Užklausos laikas** – laikas, kada buvo sukurtas užsakymo patvirtinimas. Galite palyginti užklausos laiką su užsakymo būsenos laiku, kad nustatytumėte laiką tarp patvirtinimo ir tiekėjo patvirtinimo.
- **Užsakymo siuntimo būsena** – šis laukas yra toks pat kaip ir laukas **Užsakymo siuntimo būsena** viršutinėje puslapio dalyje. Jis kartojamas čia, kad būtų lengviau peržiūrėti būseną patvirtinimo lygiu. Jei laukas **Užsakymo užklausos tipas** nustatytas kaip *Naujas* ir pirkimo užsakymas dar kartą patvirtinamas prieš išsiunčiant patvirtinimą, laukas **Užsakymo siuntimo būsena** nustatoma kaip *Archyvuota*.
- **Užsakymo būsenos laikas** – laikas, kada paskutinį kartą buvo atnaujintas pirkimo užsakymo užklausos istorijos įrašas. (Naujinimai apima būsenos pakeitimus.)
- **Užsakymo tiekėjo užklausos būsena** – šis laukas yra toks pat kaip ir laukas **Užsakymo tiekėjo užklausos būsena** viršutinėje puslapio dalyje. Jis kartojamas čia, kad būtų lengviau peržiūrėti būseną patvirtinimo lygiu.
- **Pateikimo iš naujo laikas** – laikas, kai įrašas buvo pateiktas iš naujo.
- **Pateikimų iš naujo skaičiavimas** – kartų, kai įrašas buvo pateiktas iš naujo, skaičius. Didelis skaičius nurodo kelis gedimus, todėl gali nurodyti problemą, susijusią su jūsų arba jūsų tiekėjo nustatymais.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Pirkimo užsakymo užklausos pranešimo XML formatu peržiūra

Norėdami peržiūrėti pirkimo užsakymo užklausos pranešimą XML formatu, pasirinkite skirtuką **Reikalauti XML teksto** apatinėje puslapio **Pirkimo užsakymo užklausa** dalyje. Šiame skirtuke pateikiama informacija gali būti naudinga testavimo arba klaidų tikrinimo metu. Norėdami palengvinti informacijos skaitymą, galite ją peržiūrėti kaip formatuotą pranešimą. Nukopijuokite skirtuko turinį į tekstinį failą, tada peržiūrėkite jį XML rengyklėje.

![XML teksto skirtuko užklausa](media/cxml-request-xml-text.png "XML teksto skirtuko užklausa")

### <a name="view-the-details-of-the-vendor-response"></a>Peržiūrėkite tiekėjo atsakymo informaciją.

Norėdami peržiūrėti tiekėjo patvirtinimo ar klaidos atsakymo turinį, pasirinkite **XML atsakymo** skirtuką, esantį **Pirkimo užsakymo užklausos** puslapio apačioje.

![Atsakymo XML skirtukas](media/cxml-response-xml.png "XML atsakymo skirtukas")

## <a name="additional-resources"></a>Papildomi ištekliai

- [Išorinio katalogo nustatymas el. pirkimo išėjimo laikui žymėti](set-up-external-catalog-for-punchout.md)
- [Išorinių katalogų naudojimas el. įsigijimų išėjimo laikui žymėti](use-external-catalogs-for-punchout.md)
