---
title: Inžineriniai atributai ir inžinerinio atributo paieška
description: Šiame straipsnyje paaiškinama, kaip naudoti inžinerijos atributus, norint nurodyti visas nestandartinių charakteristikų ypatybes, siekiant užtikrinti, kad visi standartinių produktų duomenys būtų registruojami sistemoje. Jis taip pat paaiškina, kaip galite naudoti inžinerinį atributo paiešką tam, kad nesunkiai rastumėte produktus pagal jų registruotas savybes.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4b25ab0bfda08b7aa091de8c6833007c586b9c87
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852569"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Inžineriniai atributai ir inžinerinio atributo paieška

[!include [banner](../includes/banner.md)]

Norėdami, kad visi produkto bendrieji duomenys būtų registruoti sistemoje, turėtumėte naudoti inžinerinius atributus tam, kad nurodytumėte visas nestandartines savybes. Tuomet galite naudoti inžinerinį atributo paiešką tam, kad nesunkiai rastumėte produktus pagal jų registruotas savybes.

## <a name="create-engineering-attributes-and-attribute-types"></a>Sukurkite inžinerinius atributus ir jo tipus

Dažniausiai, inžinerijos produktai turi daug savybių ir ypatybių, kurias turite apimti. Nepaisant to, kad galite registruoti kai kurias savybes naudodami standartinius produkto laukelius, galite taip pat kurti naujas inžinerines ypatybes, kaip reikia. Galite nurodyti savo *inžinerinius atributus* ir padaryti juos produkto sąvokos dalimi.

Bet kuris inžinerinis atributas turi priklausyti *atributo tipui*. Toks reikalavimas egzistuoja dėl to, kad visi inžineriniai atributai turi turėti *duomenų tipą*, kuris nustato jo turimus verčių tipus. Inžinerinio atributo tipas gali būti standartinis tipas (toks kaip laisvas tekstas, integruojantis ar dešimtainė) arba tinkintas tipas (toks kaip tekstas turinti konkretų verčių rinkinį, iš kurių rinktis). Galite dar kartą panaudoti kiekvieną atributo tipą su bet kuriuo inžinerinių atributų numeriu.

### <a name="set-up-engineering-attribute-types"></a>Nustatykite inžinerijos atributo tipą

Norėdami peržiūrėti, sukurti ar redaguoti inžinerinių pakeitimų užklausą, atlikite vieną iš šių žingsnių.

1. Eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Atributai \> Atributo tipai**.
1. Pasirinkite esamą atributo tipą sąrašo juostoje arba rinkitės **Naujas** tam, kad sukurtumėte naują atributo tipą.
1. Užpildykite toliau nurodytus laukus:

    - **Atributo tipo pavadinimas** – Įveskite kainų profilį aprašantį tipą.
    - **Tipas** – Pasirinkite standartinį duomenų tipą (*Valiuta*, *Data ir laikas*, *Dešimtainė*, *Integruojantis*, *Tekstas*, *Boolean* ar *Nuoroda*).
    - **Fiksuotas sąrašas** – Ši parinktis prieinama tik jei nustatėte **Tipo** laukelį į *Tekstas*. Nustatykite jį į *Taip* tam, kad nustatytumėte konkrečias vertes šio tipo atributams. Tokiu atveju, iškrentantis meniu bus sukurtas. Naudojate **Vertės** „FastTab“ siekiant sukurti vertes prieinamas šiam atributo tipui. Nustatykite šią parinktį į *Ne* norėdami leisti vartotojams įvesti bet kurią vertę. Tokiu atveju, įvesties laukelis bus sukurtas.
    - **Vertės intervalas** – Ši parinktis prieinama tik jei nustatėte **Tipo** laukelį į *Integruojantis*, *Dešimtainė* ar *Valiuta*. Nustatykite jį į *Taip* norėdami sukurti minimalias ir maksimalias vertes, kurios bus priimtos šio tipo atributams. Naudojate **Intervalo** „FastTab“ norėdami sukurti minimalias ir maksimalias vertes bei (valiutai) valiutą taikomą jūsų įvestiems apribojimams. Nustatykite šią parinktį į *Ne* norėdami priimti bet kurią vertę. 
    - **Matavimo vienetas** – Šis laukelis prieinamas tik jei nustatėte **Tipo** laukelį į *Integruojantis* ar *Dešimtainis*. Pasirinkite matavimo vienetą taikomą šiam atributo tipui. Jei jokio vieneto nereikia, palikite laukelį tuščią.

### <a name="set-up-engineering-attributes"></a>Nustatykite inžinerijos atributus

Norėdami peržiūrėti, sukurti ar redaguoti inžinerinių pakeitimų užklausą, atlikite vieną iš šių žingsnių.

1. Eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Atributai \> Inžineriniai atributai**.
1. Pasirinkite esamą atributo tipą sąrašo juostoje arba rinkitės **Naujas** tam, kad sukurtumėte naują atributo tipą.
1. Užpildykite toliau nurodytus laukus:

    - **Pavadinimas** – Įveskite kainų profilį aprašantį atributą. Šis vardas pasirodo tik **Inžinerijos atributų** puslapyje. Visu kitur sistemoje, vertė **Draugiškas pavadinimas** laukelis dažniausiai rodomas siekiant nustatyti atributą.
    - **Atributo tipas** – Pasirinkite atributo tipą, kurį nustatėte ankstesniame skyriuje.
    - **Draugiškas pavadinimas** – Įveskite pavadinimą, kuris nustato atributą sistemoje (išskyrus **Inžinerijos atributų** puslapį). 
    - **Aprašas** – Įveskite atributo aprašą.
    - **Pagalbos tekstas** – Įveskite pagalbos tekstą, kuris kitiems vartotojams sako, kam skirtas atributas.
    - **Nustatytoji vertė** – Įveskite nustatytąją vertę atributui. Parinktys yra rodomos priklausomai nuo atributo tipo, kurį rinkotės.
    - **Valiuta** – Jei atributo tipas, kurį pasirinkote yra valiuta, pasirinkite valiutą, kurią atributas priims ir rodys vertes.

1. Jei atributo tipas, kurį pasirinkote yra integruojantis ar dešimtainė, **Intervalas** „FastTab“ yra rodomas. Šiame „FastTab“, nustatykite tolesnius laukelius, kaip būtina:

    - **Paklaidos veiksmas** – Nustatykite, kaip sistema turi atsakyti, jei vartotojas įveda vertę ne nustatytame intervale. Jei pasirinkote *Įspėjimas*, įspėjimas rodo, tačiau vartotojas gali įrašyti vertę. Jei pasirenkate *Neleidžiama*, įspėjimas rodomas ir vertė negali būti įrašyta kol vartotojas jos neištaiso.
    - **Minimalus** – Įveskite minimalią vertę rekomenduojamą ar priimtą.
    - **Maksimalus** – Įveskite maksimalią vertę rekomenduojamą ar priimtą.

### <a name="engineering-attribute-inheritance"></a>Inžinerijos atributo paveldėjimas

Produktų struktūrose, pvz., komplektavimo specifikacijose (KS) arba formulėse, pasirinkti atributai gali būti perduoti iš antrinių prekių iki pirminių prekių. Apie šį procesą galite galvoti kaip apie „atvirkštinį paveldėjimą".

#### <a name="turn-engineering-attribute-inheritance-on-or-off"></a>Įjungti arba išjungti inžinerijos atributų paveldėjimą

Šiai funkcijai reikia, kad jūsų *sistemai būtų įjungtas* *ir inžinerinių pakeitimų valdymo* funkcijų inžinerijos pakeitimų valdymas ir patobulintas atributų paveldėjimas. Išsamesnės informacijos apie šių funkcijų įjungimą ir išjungimą žr. Inžinerinių [pakeitimų valdymo peržiūra](product-engineering-overview.md).

#### <a name="attribute-inheritance-example"></a>Atributų paveldėjimo pavyzdys

Jei tai yra maisto produktas, pvz., automobilio buferis, sistema turi užregistruoti kiekvieną kartą, kai jis yra. Karrot suformavimo modelį sistemoje galima modeliuoti kaip inžinerinį produktą, turiį formulę. Šioje formulėje yra automobilio ingredientai, pvz., kuko, sausainių, sausainių ir papėlidžių. Šiame pavyzdyje įmonė pateikia du automobilio sausainių modelius: pagal vieną, kuriame yra, ir kuris neturi duomenų.

Sudedamosios dalies lygyje turi daug atributų:

- Sudedamoji dalis „iš": atributas „glitimas" = taip
- Sudedamoji dalis „pienas": atributas „laktozė" = taip
- Sudedamoji dalis „riešutai": atributas „riešutai" = taip

Pyrage nėra laktozės, kuri naudoja pieną be laktozės ir turi šiuos ingridiento lygio atributus:

- Sudedamoji dalis „iš": atributas „glitimas" = taip
- Sudedamoji dalis „pienas": atributas „laktozė" = ne
- Sudedamoji dalis „riešutai": atributas „riešutai" = taip

Kadangi šie produktai dažniausiai yra panašūs, gali būti patogu perduoti šiuos atributus iš vaikų (du variantai) pirminiam produktui (pagrindinio sausainių variacijos). Norėdami įdiegti šį „atvirkštinį paveldėjimą", galite naudoti *atributų paveldėjimo* funkciją. Šis funkcionalumas apibrėžiamas kiekvienai [inžinerijos versijai](engineering-versions-product-category.md).

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Sujunkite inžinerijos atributus su inžinerijos produkto kategorija

Kai kurie inžinerijos atributai taikomi visiems produktams, tuo tarpu kiti yra konkretūs atskiriems produktams ar jų kategorijoms. Pavyzdžiui, elektriniai atributai nereikalingi mechaniniams produktams. Dėl to, galite nustatyti *inžinerijos produkto kategorijas*. Inžinerijos produkto kategorija nustato inžinerijos atributų kolekciją, kuri turi būti sąvokos produktams dalis, priklausanti tai kategorijai. Galite taip pat nurodyti, kurie inžinerijos atributai yra privalomi ir ar yra numatytoji vertė.

Dėl daugiau informacijos apie tai, kaip dirbti su inžinerijos produktų kategorijomis, įskaitant informaciją apie tai, kaip sujungti atributus su jomis, žr.  [INžinerijos versijos ir inžinerijos produktų kategorijos](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Nustatykite atributų vertes inžinerijos atributams

Inžinerijos atributai sujungti su inžinerijos produkto kategorijomis yra rodomi, kai kuriate naują inžinerijos produktą paremtą ta kategorija. Tuo metu, galite nustatyti vertes atributams. Vėliau tos vertės gali būti pakeistos **Inžinerijos versijos** puslapyje arba kaip inžinerijos keitimų valdymo dalis inžinerijos keitimo užsakyme. Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Sukurkite inžinerijos produktą

Norėdami sukurti inžinerijos produktą, atidarykite **Išleisti produktai** puslapį. Tuomet, veiksmų juostoje skirtuke **Produktas** grupėje **Naujas** pasirinkite **Inžinerijos produktas**.

Privalote nurodyti inžinerijos kategoriją, kuriai priklauso produktas. Kategorija nustatys numatytąsias vertes ir produkto savybes. Taip pat ji nustatys atributus taikomus produktui. Pasirinkus kategoriją, vertės bus nustatytos atributams. Tuomet galite modifikuoti tas vertes.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Ieškokite produktų naudodami inžinerijos atributų vertes

Galite naudoti inžinerijos atributo paiešką, kad rastumėte produktus ieškodami jų inžinerijos atributų verčių. Dėl to, galite paprastai rasti inžinerijos produktus pagal jų savybes. Galite ieškoti produktų priklausančių inžinerijos produktų kategorijai arba galite ieškoti visų inžinerijos produktų.

Paieška prieinama pagal produkto pagrindinius duomenų puslapius ir perdavimo prekes sistemoje, tokias kaip prekybos užsakymai. Perlaidos prekei, galite naudoti **Inžinerijos atributo paieškos** puslapį, kad ieškotumėte produkto. Tada galite naudoti **Įtraukti kaip naują eilutę** mygtuką, kad įtrauktumėte produktą į prekybos užsakymo eilutes. Produktai paieškos rezultatuose taip pat gali būti įtraukti tiesiogiai į užsakymą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
