---
title: Atsargų blokavimas
description: Šiame straipsnyje apžvelgiamas atsargų blokavimas, kuris yra „Supply Chain Management‟ kokybės tikrinimo proceso dalis. Naudodami atsargų blokavimą galite neleisti apdoroti ar vartoti prekių.
author: yufeihuang
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7a16c41b56b30098945a6fbdb02577624b6e173
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857814"
---
# <a name="inventory-blocking"></a>Atsargų blokavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamas atsargų blokavimas, kuris yra „Supply Chain Management‟ kokybės tikrinimo proceso dalis. Naudodami atsargų blokavimą galite neleisti apdoroti ar vartoti prekių.

Atsargų prekes blokuoti galite toliau nurodytais būdais.

- Rankiniu būdu
- Sukurdami kokybės užsakymą
- Naudodami procesą, kuris generuoja kokybės užsakymą
- Naudodami atsargų būsenos blokavimo funkciją

## <a name="blocking-items-manually"></a>Blokuodami prekes rankiniu būdu

Galite blokuoti prekės kiekį, sukurdami operaciją puslapyje **Atsargų blokavimas**. Rankiniu būdu galima blokuoti tik atsargose esančias prekes. Jei kiekius užblokuojate rankiniu būdu, turite nuspręsti, ar į veiklos planavimą kaip numatomas turimas kiekis įtrauktini numatomi gavimai. Numanomi gavimai yra užblokuotos prekės, kurios, tikimasi, baigus patikrinimą bus tarp turimų atsargų. Numatomą datą galima išlaikyti. Pagal numatytuosius nustatymus prekėms, užblokuotoms naudojant kokybės užsakymą, pasirinkta pasirinktis **Numatomi gavimai**. Galite atšaukti kiekio rankinį blokavimą panaikindami operaciją puslapyje **Atsargų blokavimas**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Prekių blokavimas sukuriant kokybės užsakymą

Galite nurodyti prekes, kurias reikia patikrinti, kurdami kokybės užsakymą puslapyje **Kokybės užsakymai**. Sukūrus kokybės užsakymą, nurodytas prekės kiekis yra užblokuojamas. Pavyzdžių ėmimo planas, susietas su kokybės užsakymu, valdo tik prekių, kurias reikia patikrinti, kiekį, o ne kiekį, kuris yra užblokuotas. Užblokuojamas tas prekės kiekis, kuris įvestas kokybės užsakyme, neatsižvelgiant į pavyzdžių ėmimo plane nurodytą kaip siųstiną tikrinti kiekį.

> [!NOTE]
> Bendrasis planavimas nepalaiko nei paketo galiojimo datos, nei atsargų būsenos blokavimo funkcijų, kai jos naudojamos kartu. Tai gali lemti dvigubą turimų atsargų neįtraukimą, kuris gali įvykti per bendrąjį planavimą. Norėdami blokuoti nebegaliojančius paketus, naudokite paketo perdavimo kodus, o ne atsargų būseną.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Prekių blokavimas naudojant procesą, kuris generuoja kokybės užsakymą

Jei kokybės procese nurodyta, kad prekę reikia patikrinti, prekių kiekis blokuojamas automatiškai. Todėl, kai automatiškai sugeneruojamas kokybės užsakymas, prekių tikrinimo planas, susijęs su kokybės užsakymu, kontroliuoja blokuojamų prekių kiekį ir prekių, kurias reikia patikrinti, kiekį. Jei puslapyje **Prekės pavyzdžio ėmimas** pasirinkta parinktis **Visiškas blokavimas**, per patikrinimą blokuojamas visas kiekis, pvz., pirkimo užsakymo eilutė, nepaisant prekės tikrinimo kiekio.

### <a name="example"></a>Pavyzdys

Šiame pavyzdyje kokybės užsakymas yra generuojamas užregistravus pirkimo užsakymo važtaraštį. Puslapyje **Kokybės susiejimai** nurodėte, kad pirkimo užsakymo važtaraščio registravimas yra procesas, kuris suaktyvina kokybės užsakymą.

|Sąranka |Vartotojo veiksmas |Rezultatas |
|----|---|---|
| Kokybės susiejimas nurodo, kad reikia sugeneruoti kokybės užsakymą, kai registruojamas pirkimo užsakymo važtaraštis. Kokybės užsakymo prekių pavyzdžių ėmimo nustatymas nurodo, kad turi būti tikrinama 10 procentų pirkimo užsakymo eilutės kiekio. Be to, kadangi pavyzdžių ėmimo nustatyme pasirinkta parinktis **Visiškas blokavimas**, per patikrinimą turi būti užblokuotas visas pirkimo užsakymo eilutės kiekis, neatsižvelgiant į tikrinimui siunčiamą kiekį. | Važtaraštis užregistruotas. | Sugeneruotas kokybės užsakymas. Dešimt procentų pirkimo užsakymo prekės kiekio siunčiama tikrinti. Visas pirkimo užsakymo eilutės kiekis yra užblokuotas. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Prekių blokavimas naudojant atsargų būsenos blokavimo funkciją

Galite nurodyti, kurių atsargų būsenos yra blokavimo būsenos, naudodami parametrą **Atsargų blokavimas**, esantį puslapyje **Atsargų būsenos**. Negalite naudoti atsargų būsenų kaip gamybos užsakymų, pardavimo užsakymų, perkėlimo užsakymų, siuntimo operacijų arba projekto integravimų blokavimo būsenų. Atlikdami siuntimo darbus naudokite prekes, kurių atsargų būsena yra „pasiekiama“. Jei prekių būsena yra **Sugadinta** ir su tomis prekėmis atliekamas bendrasis planavimas, prekės laikomos trūkstamomis ir atsargos automatiškai papildomos.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Pasirūpinkite blokuodami prekes, kurios naudoja ir atsargų būsenos blokavimą, ir kokybės užsakymo blokavimą

Galite sukurti kokybišką užsakymą, susietą su atsargomis, kurių atsargos turi atsargų būseną, kurios **atsargų blokavimo** parametras įjungtas. Šiuo atveju kokybės užsakymas generuos papildomą atsargų blokavimo įrašą kartu su tuo, kurį sukūrė atsargų būsena. Kadangi kokybės užsakymo atsargų blokavimo parametras **Tikėtini kvitai** įjungtas, generuojama papildoma operacija *Užsakytos atsargos*, kurį taip pat blokuoja jo atsargų būsena. Dėl šio derinio gali būti sunku suprasti sugeneruotų atsargų ataskaitų reikšmę, nes atrodys taip, tarsi bendras blokuojamas kiekis yra didesnis nei turimas bendras kiekis. Išnagrinėkime operacijas, imdami pavyzdį, kai gauta 10 prekių A0001 vienetų su kokybės užsakymu, sugeneruotu 1 vieneto mėginiui paimti. Elgesys taip pat priklausys nuo to, ar parinktis **Rezervuoti užsakytas prekes** yra įjungta puslapyje **Atsargų ir sandėlio valdymo parametrai**.

>[!NOTE]
>Jei kartu naudojate atsargų būsenos blokavimo ir kokybiškus užsakymus, labai rekomenduojama įjungti parinktį **Rezervuoti užsakytas prekes**.

### <a name="example-with-reserve-ordered-items-enabled"></a>Pavyzdys, kai funkcija „Rezervuoti užsakytas prekes“ įjungtas

Kai funkcija **Rezervuoti užsakytas prekes** įjungta, visų atsargų blokavimo operacijų būsena bus *Rezervuota faktiškai* arba *Rezervuota užsakytų*.

| Atsargų operacijų nuoroda | Gavimas | Išdavimas | Kiekis | Vieta | Sandėlis | Atsargų būsena | Buvimo vieta | Numerio lentelė | Komentuoti |
|---|---|---|---|---|---|---|---|---|---|
| Pirkimo užsakymas | Nupirkta | | 10 vnt. | 2 | 24 | Blokavimas | RECV | receiptLp1 | | 
| Atsargų blokavimas | | Rezervuota faktiškai | -9 vnt. | 2 | 24 | Blokavimas | | | Operacija, sugeneruota atsargų būsenos blokavimo |
| Atsargų blokavimas | | Rezervuota faktiškai | -1 vnt. | 2 | 24 | Blokavimas | RECV | receiptLp1 | Operacija, sugeneruota kokybės užsakymo pavyzdžių ėmimo blokavimo |
| Atsargų blokavimas | Užsakyta | | 1 vnt. | 2 | 24 | Blokavimas | RECV | receiptLp1 | Numatomi gavimų iš kokybės užsakymo pavyzdžių ėmimo blokavimo |
| Atsargų blokavimas | | Rezervuota užsakytų | 1 vnt. | 2 | 24 | Blokavimas | | | Operacija, sugeneruota atsargų būsenos blokavimo

### <a name="example-with-reserve-ordered-items-disabled"></a>Pavyzdys, kai funkcija „Rezervuoti užsakytas prekes“ išjungtas

Kai funkcija **Rezervuoti užsakytas prekes** išjungta, tikėtinų kvitų negalima rezervuoti, nes jų būsena yra *Užsakyta*, todėl būsena *Užsakyme* gali būti blokuojama.

| Atsargų operacijų nuoroda | Gavimas | Išdavimas | Kiekis | Vieta | Sandėlis | Inventoriaus būsena | Buvimo vieta | Numerio lentelė | Komentuoti |
|---|---|---|---|---|---|---|---|---|---|
| Pirkimo užsakymas | Nupirkta | | 10 vnt. | 2 | 24 | Blokavimas | RECV | receiptLp1 | |
| Atsargų blokavimas | | Rezervuota faktiškai | -9 vnt. | 2 | 24 | Blokavimas | | | Operacija, sugeneruota atsargų būsenos blokavimo |
| Atsargų blokavimas | | Rezervuota faktiškai | -1 vnt. | 2 | 24 | Blokavimas | RECV | receiptLp1 | Operacija, sugeneruota kokybės užsakymo pavyzdžių ėmimo blokavimo |
| Atsargų blokavimas | Užsakyta | | 1 vnt. | 2 | 24 | Blokavimas | RECV | receiptLp1 | Numatomi gavimų iš kokybės užsakymo pavyzdžių ėmimo blokavimo |
| Atsargų blokavimas | | Užsakyta | 1 vnt. | 2 | 24 | Blokavimas | RECV | receiptLp1 | Operacija, sugeneruota atsargų būsenos blokavimo

Atkreipkite dėmesį į dviejų atvejų operacijos būsenos ir dimensijų skirtumą. Dėl šios priežasties rekomenduojame įjungti parinktį **Rezervuoti užsakytas prekes**.

### <a name="disable-expected-receipts-from-quality-orders-that-sample-blocked-inventory-feature"></a>Išjungti numatomus gavimus iš kokybės užsakymų, kurie pavyzdžio yra užblokuotų atsargų funkcija

Kad atsargų operacijos būtų paprastesnės kokybės užsakymų, kurių atsargų pavyzdys užblokuotas dėl atsargų būsenos, atveju, sistema suteikia priemonę, kuri uždraus numatomus tokių kokybės užsakymų gavimus. Kadangi numatomą gavimą iš karto užblokuoja atsargų būsenos blokavimas, dėl šio pakeitimo turimų atsargų mažinti negalima.

Ši funkcija išjungta pagal nutylėjimą. Administratoriai gali jį įjungti arba *išjungti*[ieškodami](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kokybės užsakymų, kurie pvz., užblokuotų atsargų funkcija funkcijų valdymo darbo srityje, numatomų gavimų iš kokybės užsakymų.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kurti ir tvarkyti atsargų blokavimą](tasks/create-maintain-inventory-blocking.md)

[Kokybės valdymo procesai](quality-management-processes.md)

[Tikrinti prekių kokybę](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]