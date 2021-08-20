---
title: Neatitikimo kūrimas ir apdorojimas
description: Šioje temoje aprašoma, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 933efff1be545816504ab31f7a3135bf79996d7b8a50dac9fcc5b994e57a8965
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747966"
---
# <a name="create-and-process-nonconformances"></a>Neatitikimo kūrimas ir apdorojimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu. Paprastai neatitikties valdymą atliko kokybės klerkas. Jei būtina, turite turėti prieinamą kokybės užsakymą. (Daugiau informacijos apie tai, kaip kurti ir dirbti su kokybės užsakymais rasite [Stebėkite prekių kokybę](inspect-quality-goods.md).)

Kad vartotojas galėtų apdoroti neatitikties patvirtinimą, darbuotojas turi būti jam priskirtas vartotojų **puslapio** lauke **Asmuo**. Be to, prieš vartotojui naudojant dokumentų pastabas jų vartotojo pasirinktyse turi būti nustatyta parinktis **Įgalinti** dokumentų *tvarkymą*.

## <a name="create-a-nonconformance"></a>Neatitikties kūrimas

Norėdami sukurti neatitiktis, atlikite tolesnius veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Veiksmų juostoje pasirinkite **Nauja**.
1. Dialogo lange Kurti neatitikčių žymėjimą lauke Problemos tipas **pasirinkite** problemos **, kuri** buvo rasta tikrinimo proceso metu, tipą.
1. Pasirinkite **Gerai**.

## <a name="approve-or-reject-a-nonconformance"></a>Neatitikties tvirtinimas ar atmetimas

Norėdami patvirtinti arba atmesti neatitiktis, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.

    > [!NOTE]
    > Pataisymus galite įtraukti tik į patvirtintas neatitiktis.

1. Veiksmų srityje pasirinkite **Funkcijos \> Tvirtinti neatitiktis** norėdami patvirtinti neatitiktis ar **Funkcijos \> Atsisakyti neatitikčių** norėdami jas atmesti. Patvirtintas neatitiktis galima susieti su [susijusiomis](../quality-operations.md) operacijomis. Tokiu būdu galite įrašyti darbą, įvertinimą, o taisymą – kaip neatitikties tvarkymo dalį.
1. Jus paragins patvirtinti savo pasirinkimą. Pasirinkite **Taip** tam, kad tęstumėte.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Prie neatitikimų pridėkite operacijas ir kitą informaciją

Sukūrę neatitiką, galite pradėti pridėti susijusias operacijas ir nurodyti papildomą informaciją apie tas operacijas. Susijusias operacijas galite įtraukti tik į patvirtintas neatitiktis.

Be pagrindinės informacijos, operacijai galite pridėti ir toliau nurodytą informaciją:

- **Prekės** – galite sukurti prekių, suvartotų atlikti koregavimą, sąrašą. Pavyzdžiui, prekės gali būti produktai, kurių reikia norint remontuoti įrangą arba ingredientus, reikalingus baigtam produktui perkurti.
- **Kokybės išlaidos** – galite sukurti išlaidų, kurios patirtos arba išrašomos iš išorinių šaltinių, sąrašą.
- **Tabelis** – galite sukurti laiko, kurį kiekvienas darbuotojas praleidžia operacijoje, žurnalą.

Likę nustatymai yra neprivalomi. Susumuojamos kiekvienos prekės išlaidos, kokybės išlaidos ir tabelis bei rodomas operacijoje. Operacijos lauko Išlaidos **tiesiogiai** redaguoti negalima.

### <a name="create-an-operation-for-a-nonconformance"></a>Kurti neatitikties operaciją

Norėdami sukurti neatitikčių operaciją, atlikite tolesnius veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.

    > [!NOTE]
    > Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.

1. Veiksmų srityje spustelėkite **Susijusios operacijos**.
1. Puslapyje **Susijusios operacijos** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Operacija** – pasirinkite operacijos, kuri bus atliekama neatitikti, kodą.
    - **Priežastis** – įveskite išsamų aprašymą, paaiškinaį, kodėl operacija reikalinga.
    - **Pardavimo užsakymas – jei pasirinktas operacijos kodas yra susijęs su pardavimo užsakymo tipu, pasirinkite pardavimo užsakymą, su** kurį susiesite operaciją.
    - **Pirkimo užsakymas – jei pasirinktas operacijos kodas yra susijęs su pirkimo užsakymo tipu, pasirinkite pirkimo užsakymą, su** kurį susiesite operaciją.

1. Uždarykite puslapius.

### <a name="add-items-to-an-operation"></a>Prekių įtraukimas į operaciją

Norėdami į operaciją įtraukti prekes, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.

    > [!NOTE]
    > Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.

1. Veiksmų srityje spustelėkite **Susijusios operacijos**.
1. Puslapyje **Susijusios operacijos** pasirinkite operaciją, į kurią norite įtraukti prekes.
1. Veiksmų srityje pasirinkite **Prekės**.
1. Puslapyje **Susijusios operacijos** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Prekės numeris** – pasirinkite produktą, kuris bus suvartotas kaip pasirinktos operacijos dalis.
    - **Kiekis** – įveskite suvartotų prekių skaičių.

    > [!NOTE]
    > Prekės išlaidas galite peržiūrėti skirtuko **Bendra** lauke **Išlaidos**. Išlaidos, kurios rodomos, yra iš išlaidų, kurios yra nustatytos **išleisto produkto** puslapyje. Išlaidų negalima tiesiogiai atnaujinti puslapyje Susijusios **operacijos** elementas. Visų prekių, kurios pridėtos puslapyje Susijusios operacijos elementai, išlaidos automatiškai pridėtos prie **lauko Išlaidos puslapyje** **Susijusios** **operacijos**.

1. Pakartokite ankstesnį veiksmą su kiekviena papildoma preke, kurią turite įtraukti.
1. Uždarykite puslapius.

### <a name="add-quality-charges-to-an-operation"></a>Į operaciją įtraukti kokybės išlaidas

Norėdami įtraukti kokybės keitimus, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.

    > [!NOTE]
    > Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.

1. Veiksmų srityje spustelėkite **Susijusios operacijos**.
1. Puslapyje **Susijusios operacijos** pasirinkite operaciją, į kurią norite įtraukti kokybės keitimus.
1. Veiksmų srityje pasirinkite **Kokybės keitimai**.
1. Puslapyje **Susiję operacijų keitimai** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Kodo mokesčiai** – Pasirinkite kokybės grupę, kurią norite įtraukti.
    - **Aprašas** – įveskite išsamų keitimo aprašą.
    - **Vertės mokesčiai** – Įvesti taikytiną mokesčio sumą.

1. Pakartokite ankstesnį veiksmą su kiekvienu papildomu mokesčiu, kurią turite įtraukti.
1. Uždarykite puslapius.

> [!NOTE]
> Lauke Išlaidų vertė automatiškai sumuojamos visos kokybės išlaidos ir pridedama prie visų kitų sumų  **lauke** **Išlaidos** **puslapyje Susijusios** operacijos.

### <a name="create-a-timesheet-on-an-operation"></a>Sukurkite operacijos tabelį

Norėdami įtraukti tabelį į operaciją, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.

    > [!NOTE]
    > Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.

1. Veiksmų srityje spustelėkite **Susijusios operacijos**.
1. Puslapyje **Susijusios operacijos** pasirinkite operaciją, į kurią norite įtraukti tabelį.
1. Veiksmų srityje pasirinkite **Tabelis**.
1. Puslapyje **Susiję operacijų tabeliai** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Data** – nurodykite datą, kada darbas buvo atliktas. Pagal numatytą laukelį, nustatoma esama data.
    - **Darbuotojas** – Pasirinkite darbuotoją, kuris nedirbo. Pagal numatytuosius nustatymus šis laukas nustatomas darbuotojui, kuris priskirtas dabartiniam vartotojui.
    - **Operacijos valandos** – įveskite valandų skaičių, kuris buvo valandų skaičius, pagal kurį buvo dirbama su pasirinkta operacija.
    - **Išrašyta SF – pažymėkite šį žymės langelį, jei SF** klientams arba tiekėjui išrašoma sąskaita faktūra.

    > [!NOTE]
    > Galite peržiūrėti išlaidas lauke **Išlaidos** skirtuke **Bendra**. Išlaidos apskaičiuojamos naudojant tarifą, kurį nurodote **atsargų valdymo parametrų** puslapyje.

1. Pakartokite ankstesnį veiksmą su kiekvienu papildomu tabeliu, kurį turite įtraukti.
1. Uždarykite puslapius.

> [!NOTE]
> Lauke Išlaidų vertė automatiškai sumuojamos visi kokybės kaštai ir pridedama prie visų kitų tabelių eilučių  **Kaštai** **Išlaidos** **puslapyje Susijusios** operacijos.

## <a name="add-a-correction-to-a-nonconformance"></a>Taisymo pridėjimas prie neatitikties

Norėdami įtraukti taisymą į neatitiktis, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.

    > [!NOTE]
    > Pataisymus galite įtraukti tik į patvirtintas neatitiktis.

1. Veiksmų srityje pasirinkite **Taisymai**.
1. Puslapyje **Taisymai** tam, kad įtrauktumėte eilutę tinklelyje **Peržiūros** skyriuje. Tada nustatykite šiuos laukus naujai eilutei:

    - **Diagnostika** – pasirinkite diagnozės tipą, kuris identifikuoja kuriamo pataisos tipą.
    - **Darbuotojas** – Pasirinkite už taisymus atsakingą asmenį.
    - **Koregavimo prioritetas – pasirinkite pasirinktį, norėdami nurodyti, kaip turi būti taisymo prioritetas** (*Žemas*, *Įprastas* arba *Aukštas*).
    - **Pareikalauta data** – įveskite datą, kada pareikalauta baudos veiksmo.
    - **Suplanuota** data – įveskite datą, kada tikimasi atlikti pataisymą.
    - **Trumpalaikis sprendimas** – pasirinkite šį žymės langelį, jei koreguojamuoju veiksmu neatitiktis taisoma tik trumpą laiką.

1. Uždarykite puslapius.

## <a name="mark-a-correction-as-completed"></a>Žymėti taisymą kaip užbaigtą

Norėdami pažymėti neatitikties taisymą kaip baigtą, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.

    > [!NOTE]
    > Pataisymus galite įtraukti tik į patvirtintas neatitiktis.

1. Veiksmų srityje pasirinkite **Taisymai**.
1. Skirtuko **Taisymų** puslapyje tinklelyje pasirinkite taisymą, kurį norite pažymėti kaip užbaigtą.
1. Veiksmų srityje spustelėkite **Žymėjimas baigtas**.
1. Jus paragins patvirtinti savo pasirinkimą. Norėdami tęsti **Rinkitės** GERAI. Lauke **Baigimo data** ir laikas nustatyti dabartiniai data ir laikas, ir **pažymėtas žymės langelis** Baigta.
1. Uždarykite puslapį.

## <a name="reopen-a-completed-correction"></a>Atidarykite baigtą taisymą iš naujo

Norėdami atidaryti iš naujo baigtą taisymą, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.
1. Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.
1. Veiksmų juostoje pasirinkite **Taisymai**.
1. Skirtuko **Taisymų** puslapyje tinklelyje pasirinkite taisymą, kurį norite atidaryti iš naujo.
1. Veiksmų srityje pasirinkite **Atidaryti iš naujo**.
1. Jus paragins patvirtinti savo pasirinkimą. Norėdami tęsti **Rinkitės** GERAI. Vertė išvalo lauką **Užbaigimo data ir** laikas, o žymės **langelis Baigtas** išvalomas.
1. Uždarykite puslapį.

Dabar galite atlikti papildomus pataisymų redagavimus ar atnaujinimus. Baigę pataisymą galite žymėti kaip užbaigtą dar kartą.

## <a name="close-a-nonconformance"></a>Neatitikties uždarymas

Norėdami uždaryti neatitiktis, atlikite tolesnius veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.
1. Tinklelyje pasirinkite kokybės užsakymą.
1. Veiksmų srityje pasirinkite **Užklausos \> Neatitiktys**.
1. Neatitikties **puslapyje** tinklelyje pasirinkite tikslinę neatitikčių tikslą.
1. Veiksmų srityje pasirinkite **Funkcijos \> Uždaryti neatitiktis**.
1. Jus paragins patvirtinti savo pasirinkimą. Pasirinkite **Taip** tam, kad tęstumėte.
1. Uždarykite puslapius.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo apžvalga](../quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](../enable-quality-management.md)
- [Darbuotojai, atsakingi už neatitikties tvirtinimą](../quality-responsible-workers.md)
- [Neatitikimų sulaikymo zonos](../quality-quarantine-zones.md)
- [Neatitikimų diagnostikos tipai](../quality-diagnostic-types.md)
- [Neatitikimų kokybės mokesčiai](../quality-charges.md)
- [Neatitikties operacijos](../quality-operations.md)
- [Sandėlio procesų kokybės valdymas](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
