---
title: Tranzito prekių apdorojimas
description: Šiame straipsnyje aprašoma, kaip dirbti su tranzito prekių užsakymais. Kai užsakymas arba reisas nustatomas naudoti tranzito prekių apdorojimą, prekėms SF galima išrašyti prieš jas gaunant į sandėlį vartojimui.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 47e5ef2ef99fcf23af73cfdb6ec57b92ad62f18c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854390"
---
# <a name="goods-in-transit-processing"></a>Tranzito prekių apdorojimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip dirbti su tranzito prekių užsakymais. Tokio tipo užsakymą naudoja tik modulis **Iškrovimo kaina**. Kai užsakymas arba reisas nustatomas naudoti tranzito prekių apdorojimą, nereikia laukti, kol gausite prekes sandėlyje, kad joms galėtumėte išrašyti SF. Vietoje to, prekėms SF išrašoma tada, kai jos išvežamos iš tiekėjo sandėlio arba iš išvykimo uosto, o finansinės išlaidos pripažįstamos prasidėjus reisui. Šios funkcijos leidžia tinkamai perimti atsargų nuosavybę, nes prekės dažnai tampa jūsų organizacijos nuosavybe, kai jos išvežamos iš siuntimo uosto.

Kai naudojami tranzito prekių užsakymai, finansiškai atnaujintos prekės gaunamos tarpiniame sandėlyje, kuris vadinamas tranzito prekių sandėliu. Tuomet prekės lieka šiame sandėlyje, kol jas galima gauti galutiniame paskirties sandėlyje (tai yra, pirkimo eilutėje nurodytame sandėlyje). Jų rankiniu būdu pašalinti negalima.

Kai prekės yra tranzite, jų pristatymui negalima paimti iš atsargų. Tačiau galima peržiūrėti tranzitinių prekių atsargas. Be to, prekes galima naudoti bendrajam planavimui. Šiuo atveju pirkimo užsakymo eilutėje naudokite patvirtintą pristatymo datą kaip numatytą datą, kai atsargas bus galima naudoti.

Tolesniuose skyriuose aprašomas nustatymas, kurio reikia norint apdoroti atsargas ir reisus, naudojant tranzitinę prekių koncepciją ir funkcijas.

## <a name="terms-of-delivery"></a>Pristatymo sąlygos

Įjungus modulį **Iškrovimo kaina**, standartinis objektas *Pristatymo sąlygos* patobulinimas tranzitinių prekių funkcijai palaikyti.

Kai parinktis **Tranzitinių prekių valdymas** nustatyta kaip *Taip* galiojančioms pristatymo įrašo sąlygoms, prekės perkeliamos į tranzitinių prekių sandėlį. Šis veiksmas suaktyvinamas tik tada, kai atsargų kvitas neapdorojamas prieš apdorojant SF. Kai užsakymo pristatymo sąlygos nustatytos naudoti tranzito prekes, naudotojai nebegali registruoti pirkimo užsakymo produkto gavimo. Jei bandys, įvyks klaida. Klaidos pranešimas rodo, kad norint tęsti reikia naudoti tranzito prekių funkciją.

Norėdami dirbti su tranzito prekių pristatymo sąlygų informacija, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Nustatymas \> Paskirstymas \> Pristatymo sąlygos**. Šioje lentelėje aprašomi laukeliai, kuriuos modulis **Iškrovimo kaina** prideda prie puslapio **Pristatymo sąlygos**, kad palaikytų tranzito prekių funkcijas. Abu laukeliai yra „FastTab“ skirtuke **Bendra**. Daugiau informacijos apie kitus šio puslapio laukelius rasite skyriuje [Pristatymo sąlygos (forma)](/dynamicsax-2012//terms-of-delivery-form).

| Laukas | aprašymas |
|---|---|
| Privalomas siuntimo uostas | Šią parinktį nustatykite kaip *Taip*, jei taikant pristatymo sąlygas būtina nurodyti siuntimo uostą. |
| Tranzito prekių valdymas | Šią parinktį nustatykite kaip *Taip*, kad taikant pristatymo sąlygas naudotumėte tranzito prekių valdymą. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Tranzito prekių sandėliai ir pristatymo trūkumas

Įjungus modulį **Iškrovimo kaina** standartinis objektas *Sandėliai* patobulinamas pirkimo užsakymams įjungti, kad jiems būtų galima išrašyti SF, kai prekės yra tranzito prekių sandėlyje.

Iškrovimo kaina prideda dviejų naujų tipų sandėlį: *Tranzito prekės* ir *Pristatymo trūkumas*. Abiejų tipų sandėlius galima pasirinkti kaip numatytuosius sandėlius. Norint sėkmingai apdoroti tranzito prekių užsakymus, puslapyje **Sandėliai** reikia sukonfigūruoti ir tranzito prekių, ir pristatymo trūkumo sandėlį. Tada kiekvienam numatytam sandėliui, kuris bus naudojamas su iškrovimo kaina ir tranzito prekėmis, tranzito prekių sandėlį ir pristatymo trūkumo sandėlį reikia pasirinkti kiekvieno tipo turimiems sandėliams.

Sandėlio tipas *Tranzito prekės* bus siejamos su tranzito prekių sandėliu, o tas sandėlis bus naudojamas prekėms iš tranzito prekių užsakymų apdoroti prieš jas gaunant galutiniame paskirties sandėlyje. Apskritai, vieno tranzito prekių sandėlio pakanka kiekvienai svetainei, jei svetainė ir sandėlis yra vienintelės atsargų dimensijos, kurios naudojamos atsargų valdymui. Jei taip pat naudojama vietos atsargų dimensija, kiekvienam svetainės ir sandėlio deriniui turi būti nustatytas tranzito prekių sandėlis, kad būtų galima nurodyti ir numatytąją vietą.

Kad savo sandėliuose galėtumėte dirbti su tranzito prekių nustatymais, eikite į **Atsargų valdymas \> Nustatymas \> Atsargų paskirstymas \> Sandėliai**. Šioje lentelėje aprašomi laukeliai, kuriuos modulis **Iškrovimo kaina** prideda prie puslapio **Sandėliai**, kad palaikytų tranzito prekių funkcijas. Abu laukeliai rodomi „FastTab“ skirtuke **Bendra**. Informacijos apie kitus puslapio laukelius žr. skyriuje [Sandėliai (forma)](/dynamicsax-2012//warehouses-form).

| Laukas | aprašymas |
|---|---|
| Tranzito prekių sandėlis | Identifikuokite tranzito prekių sandėlį, susijusį su pagrindiniu sandėliu. |
| Trūkumo pristatymo sandėlis | Identifikuokite pristatymo trūkumo sandėlį, susijusį su pagrindiniu sandėliu. |

## <a name="posting-rules-for-landed-cost"></a>Registravimo taisyklės iškrovimo kainai

Iškrovimo kaina prideda dvi naujas registravimo taisykles, kurias galima konfigūruoti. Šios registravimo taisyklės naudojamos norint finansiškai registruoti tiesioginio pirkimo užsakymo sumas, siekiant nustatyti prekių nuosavybę, kai jos iškeliauja iš kilmės vietos. Šiuo procesu pakeičiama *gautų prekių, kurioms neišrašyta SF*, sąvoka, nes SF prekėms išrašoma prieš jas gaunant. <!-- KFM: Add a link to the related scenario when available. -->

Norėdami dirbti su registravimo profiliais, eikite į **Atsargų valdymas \> Nustatymas \> Registravimas \> Registravimas**. Skirtuke **Pirkimo užsakymas** galima rinktis tokias naujas registravimo taisykles:

- **Iškrovimo kaina, tranzito prekės** – nurodykite registravimo taisykles tranzito prekių valdymui.
- **Iškrovimo kaina, savikainos mokesčio kaupimas** – nurodykite mokesčio sąskaitos kaupimo registravimo taisykles.

## <a name="goods-in-transit-orders"></a>Tranzito prekių užsakymai

Tranzito prekių užsakymus galima peržiūrėti ir valdyti modulyje **Iškrovimo kaina**. Tranzito prekių užsakymus galima apdoroti tiesiogiai puslapyje **Tranzito prekių užsakymai**. Taip pat galite pereiti prie reiso, kuris yra susietas su tranzito prekių užsakymais, ir apdoroti visą reisą, siuntimo konteinerį arba registravimo lapą. Kai reisui išrašote SF ir sukuriate tranzito prekių užsakymus, sukuriamas naujas tranzito prekių užsakymas kiekvienai atsargų ir atsargų dimensijų kombinacijai, susietai su pirkimo užsakymo eilute.

Kad galėtumėte valdyti tranzito prekes, iškrovimo kaina naudoja dviejų etapų procedūrą:

1. Prekė gaunama, kai atsargų SF apdorojama ir kai jai priskiriama būsena *Tranzito*.
1. Tranzito prekių užsakymas apdorojamas puslapyje **Tranzito prekių užsakymai**, o tada yra gaunamas pirkimo užsakyme nurodytame sandėlyje. Tuo metu būsena pakeičiama į *Gauta*.

Norėdami dirbti su tranzito prekių užsakymais, eikite į **Iškrovimo kaina \>Periodinės užduotys \>Tranzito prekių užsakymai**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Atsargų gavimas iš tranzito prekių sandėlis

Atsižvelgiant į sistemos nustatymą galima įvairiais būdais gauti prekes iš tranzito prekių užsakymo.

### <a name="in-transit-receiving"></a>Tranzito priėmimas

Tranzitinį transportavimą galima atlikti iš bet kurio iš šių puslapių:

- Puslapyje **Tranzito prekių užsakymai** pasirinkite eilutę, o tada veiksmų srityje pasirinkite **Gauti**.
- Puslapyje **Visi reisai** pasirinkite arba atidarykite reisą. Tada, veiksmų srities skirtuke **Valdyti**, grupėje **Tranzito prekės** pasirinkite **Priimti tranzito prekes**.
- Puslapyje **Visi siuntimo konteineriai** pasirinkite arba atidarykite siuntimo konteinerį. Tada, veiksmų srities skirtuke **Valdyti**, grupėje **Tranzito prekės** pasirinkite **Priimti tranzito prekes**.
- Puslapyje **Visi registravimo lapai** pasirinkite arba atidarykite registravimo lapą. Tada, veiksmų srities skirtuke **Valdyti**, grupėje **Tranzito prekės** pasirinkite **Priimti tranzito prekes**.

> [!NOTE]
> Tranzitinis gavimas paprastai naudojamas situacijose, kai nenaudojamas vietų ir paketo / serijos sekimas.

### <a name="arrival-journal"></a>Atvykimo žurnalas

Prekes taip pat galite gauti sukurdami atvykimo žurnalą. Gavimo žurnalą galima sukurti tiesiogiai reiso puslapyje. Geriausia jūsų organizacijos nustatyta praktika ar gavimo žurnalas naudojamas prekėms gauti.

1. Atidarykite reisą, konteinerį arba registracijos numerį.
1. Veiksmų srityje, skirtuke **Valdyti**, grupėje **Funkcijos** pasirinkite **Kurti gavimo žurnalą**.
1. Dialogo lange **Sukurti gavimo žurnalą** nustatykite šias vertes:

    - **Inicijuoti kiekį** – nustatykite šią parinktį kaip *Taip*, kad nustatytumėte kiekį iš tranzito kiekio. Jei ši pasirinktis nustatyta kaip *Ne*, tranzito prekių eilutėse nenustatytas numatytasis kiekis.
    - **Kurti iš tranzito prekių** – šią parinktį nustatykite kaip *Taip*, kad paimtumėte kiekius iš pasirinktų tranzito eilučių pasirinktam reisui, konteineriui ar registravimo lapui.
    - **Kurti iš užsakymo eilučių** – šią parinktį nustatykite kaip *Taip*, kad numatytąjį kiekį nustatytumėte iš pirkimo užsakymo eilučių. Numatytąjį kiekį gavimo žurnale tokiu būdu galima nustatyti tik jei kiekis pirkimo užsakymo eilutėje sutampa su kiekiu, nurodytu tranzito prekių užsakyme.

1. Apdorokite gavimo žurnalą, kaip aprašyta skyriuje [Prekių kvitų registravimas prekių gavimo žurnale](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal).

> [!NOTE]
> Gavimo žurnalas paprastai naudojamas situacijose, kai naudojamos vietos ir paketo / serijos sekimas, bet sandėlio valdymas nėra naudojamas.
>
> Užsakymo eilutėse neturėtų būti nurodytos numatytosios gavimo vietos, jei gavimo žurnale bus nurodyta atidavimo vieta.

## <a name="warehouse-management"></a>Sandėlio valdymas

Įjungus modulį **Iškrovimo kaina**, keli puslapiai modulyje **Sandėlio valdymas** keičiami taip, kad užsakymo apdorojimą (ypač tranzito prekių apdorojimą) būtų galima atlikti per modulį **Iškrovimo kaina**. Šiame skyriuje aprašomi laukeliai ir procesai, pridėti prie modulio **Sandėlio valdymas**.

### <a name="mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementai

Prekes galima gauti naudojant mobilųjį įrenginį, jei jo meniu ir modulis **Sandėlio valdymas** nustatyti prekėms, esančioms tranzito prekių užsakyme, gauti. Šiame skyriuje aprašomas nustatymas, susijęs su tranzito prekių gavimu.

Kad mobiliuosius įrenginius nustatytumėte tranzito prekių apdorojimui, eikite į **Sandėlio valdymas \> Nustatymas \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.

Iškrovimo kaina prie mobiliojo įrenginio meniu elementų prideda nurodytus darbo kūrimo procesus tranzito prekėms apdoroti:

- Tranzito prekių priėmimas
- Tranzito prekių gavimas ir atidėjimas

Šių procesų konfigūracijos parametrai yra panašūs į nustatymus [pirkimo užsakymo gavimo ir atidėjimo darbo sukūrimo procesams](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work). Tačiau procesas *Tranzito prekių gavimas ir atidėjimas* taip pat prideda nurodytą laukelį.

- **Siuntimo konteinerio įjungimas baigtas** – jei ši parinktis nustatyta kaip *Taip*, baigus atidėjimo darbą sandėlio valdymo mobiliųjų įrenginių programėlė pateikia papildomą parinktį pavadinimu **Siuntimo konteineris baigtas**. Pasirinkus šią parinktį darbuotojo bus prašoma patvirtinti, kad konteineris baigtas. Tuo metu visi trumpi gaviniai bus apdorojami kaip operacijos dalis.

### <a name="location-directives"></a>Vietos nurodymai

Iškrovimo kaina prideda naują darbo užsakymo tipą, pavadintą *Tranzito prekės* puslapyje **Vietos direktyvos**. Šį darbo užsakymo tipą reikėtų konfigūruoti taip pat, kaip ir [pirkimo užsakymo darbo užsakymo tipus](/dynamicsax-2012/appuser-itpro/create-a-work-template).

### <a name="work-templates"></a>Darbo šablonai

Šiame skyriuje aprašomos priemonės, kurias **Iškrovimo kainos** modulis prideda prie darbo šablonų.

#### <a name="goods-in-transit-work-order-type"></a>Tranzito prekių darbo užsakymo tipas

Iškrovimo kaina prideda naują darbo užsakymo tipą, pavadintą *Tranzito prekės* puslapyje **Darbo šablonai**. Šį darbo užsakymo tipą reikėtų konfigūruoti taip pat, kaip ir [pirkimo užsakymo darbo šablonus](/dynamicsax-2012/appuser-itpro/create-a-work-template).

#### <a name="work-header-breaks"></a>Darbo antraštės pertrauktys

Darbo šablonus, kurių darbo užsakymo tipas yra *Tranzito prekės* galima sukonfigūruoti į suskaidytas darbo antraštes. Puslapyje **Darbo šablonai** atlikite vieną iš toliau nurodytų veiksmų:

- Šablono **Bendrieji** skirtuke nustatykite didžiausias darbo antraštės vertes. Šios maksimalios vertės veikia tokiu pat būdu, kaip ir jos veikia pirkimo užsakymo darbo šablonus. (Daugiau informacijos ieškokite [pirkimo užsakymo darbo šablonuose](/dynamicsax-2012/appuser-itpro/create-a-work-template) .)
- Naudokite **Darbo antraštės pertrūkiai** mygtuką, kad nustatytumėte, kada sistema turi sukurti naują darbo antraštę, remiantis rūšiavimui naudojamasi laukais. Pavyzdžiui, norėdami sukurti darbo antraštę kiekvienam konteinerio ID, veiksmų juostoje pasirinkite **Redaguoti užklausą** ir tada įtraukite **Konteinerio ID** laukelį į **Rūšiavimo** skirtuką užklausos redaktoriuje. Laukeliai yra įtraukti į **Rūšiavimo** skirtuką ir yra prieinami pasirinkimui kaip *laukelių grupavimas*. Norėdami nustatyti savo grupavimo laukelius rinkitės **Darbo antraštės pertraukimas** veiksmų juostoje ir tada kiekvienam laukeliui, kurį norite naudoti kaip laukelių grupavimą, pasirinkite žymės laukelį, esantį **Grupuoti šį laukelį** stulpelyje.

Jei užregistruotas kiekis viršija pradinio užsakymo kiekį, iškrovimo kaina [sukūria operacijos viršijimą](over-under-transactions.md). Kai darbo antraštė baigta, sistema atnaujina pagrindinio užsakymo kiekio atsargų operacijų būseną. Tačiau, pirma ji atnaujina kiekį, kuris susietas su operacijų viršijimu po to, kai pagrindinė yra visiškai nupirkta.

Jei atšauksite jau užregistruotos operacijos viršijimo darbo antraštę, pirmiausia bus sumažintas operacijos viršijimas atšauktu kiekiu. Kai operacijos viršijimas sumažinamas iki 0 (nulio) kiekio, įrašas pašalinamas, o visi papildomi kiekiai neregistruojami pagal pagrindinio užsakymo kiekį.
