---
title: Nomenklatūros irr kokybės valdymo peržiūra
description: Šioje temoje supažindinimo kokybės ir neatitikties valdymo funkcijos ir paaiškinama, kaip jos gali padėti „Microsoft Dynamics 365 Supply Chain Management“ pagerinti produkto kokybę jūsų tiekimo grandinėje.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8bb3862b2a082dd975af8bbb30961caf209c5ad
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344525"
---
# <a name="quality-and-nonconformance-management-overview"></a>Nomenklatūros irr kokybės valdymo peržiūra

[!include [banner](../includes/banner.md)]

Šioje temoje supažindinimo kokybės ir neatitikties valdymo funkcijos ir paaiškinama, kaip jos gali padėti „Microsoft Dynamics 365 Supply Chain Management“ pagerinti produkto kokybę jūsų tiekimo grandinėje.

Kokybės užtikrinimas apima produktų bandymą ir neatitinkančių medžiagų valdymą. Kokybės valdymo procesai padeda užtikrinti aukštą produktų kokybę jūsų tiekimo grandinėje. Šie procesai taip pat padeda optimizuoti tiekimo grandinės procesus ir padidinti klientų pasitenkinimą. Kokybės valdymas gali padėti valdyti apgręžimo laiką, kai dirbate su neatitinkančiais produktais, neatsižvelgiant į jų kilmę. Diagnostikos rezultatus galite susieti su koregavimo užduotimis. Sistema gali planuoti užduotis taisyti problemoms ir taip padėti išvengti šių problemų pasikartojimo ateityje. Kokybės valdymas taip pat leidžia problemas (įskaitant vidaus problemas) sekti pagal problemos tipą ir leidžia sprendimus identifikuoti kaip trumpalaikius arba ilgalaikius. Statistika apie pagrindinius našumo indikatorius (KPI) teikia įžvalgų apie ankstesnes neatitikimo problemas ir sprendimus, kurie buvo taikomi joms taisyti. Galite naudoti praeities duomenis, kad būtų lengviau peržiūrėti anksčiau naudotų kokybės priemonių efektyvumą bei nustatyti tinkamas priemones, kurios bus naudojamos ateityje.

Kokybės valdymas gali padėti valdyti apgręžimo laiką tvarkant neatitinkančius produktus, neatsižvelgiant į kilmę. Kadangi diagnostikos tipai yra susiję su koregavimo ataskaitomis, „Supply Chain Management‟ gali planuoti užduotis ir jomis taisyti problemas bei neleisti joms pasikartoti.

Be funkcijų, skirtų valdyti neatitikimui, kokybės valdymas apima funkcijas, skirtas problemoms sekti pagal jų tipą (net jei tia vidaus problemos) ir sprendimams identifikuoti kaip trumpalaikiams ar ilgalaikiams. Statistika apie pagrindinius našumo indikatorius (KPI) teikia įžvalgų apie ankstesnių neatitikimo problemų istoriją ir sprendimus, kurie buvo naudojami joms taisyti. Galite naudoti praeities duomenis ir peržiūrėti ankstesnių kokybės priemonių efektyvumą bei nustatyti tinkamas priemones, kurios bus naudojamos ateityje.

Kai nustatote kokybės susiejimą, „Supply Chain Management‟ gali generuoti įvairių verslo procesų, įvykių ir sąlygų kokybės užsakymus. Kokybės susiejimas gali apimti konkrečią prekę, konkrečią prekių grupę arba visas prekes.

## <a name="examples-of-the-use-of-quality-management"></a>Kokybės valdymo naudojimo pavyzdžiai

Kokybės valdymas yra lankstus ir gali būti diegiamas įvairiais būdais, siekiant atitikti konkrečių tiekimo grandinės operacijų lygių reikalavimus. Toliau pateikti pavyzdžiai iliustruoja galimą šių funkcijų naudojimą.

- Pagal iš anksto nustatytus kriterijus automatiškai paleisti kokybės kontrolės procesą (pvz., sandėlyje registravus pirkimo užsakymą iš konkretaus tiekėjo).
- Tikrinimo metu blokuoti atsargas, siekiant neleisti naudoti nepatvirtintų atsargų (visiškas pirkimo užsakymų kiekių blokavimas).
- Kaip kokybės susiejimo dalį naudoti prekių pavyzdžių ėmimą, siekiant apibrėžti dabartinių faktinių atsargų, kurias reikia tikrinti, sumą. Pavyzdžių ėmimas gali būti paremtas fiksuotais kiekiais, procentine dalimi arba visa numerio lentele.
- kurkite dalinių kvitų kokybės užsakymus. Norėdami kurti kokybės užsakymą, pagrįstą faktiškai su užsakymu gautu kiekiu, formoje **Prekės pavyzdžio ėmimas** turite pažymėti žymės langelį **Pagal atnaujintą kiekį** puslapyje.
- Kurti testų tipus, apimančius minimalias, maksimalias ir paskirties testo reikšmes, ir atlikti kokybės–kiekybės tikrinimą su iš anksto nustatytais tikrinimo rezultatais.
- Nurodyti priimtiną kokybės lygį (AQL), siekiant kontroliuoti leistinus kokybės matavimo nuokrypius.
- Nurodyti išteklius, kurių reikia tikrinimo operacijai, pvz., tikrinimo sritį ir tikrinimo priemones.

> [!NOTE]
> Funkcija _Sandėlio procesų kokybės valdymas_ išplečia kokybės valdymo galimybes. Jei naudojate šią funkciją, žr. [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md) pateiktus pavyzdžius, kaip veikia įgalintas kokybės valdymas.

## <a name="controlling-the-quality-management-process"></a>Kokybės valdymo proceso kontroliavimas

Toliau pateikti keletas būdų, kaip galite kontroliuoti kokybės valdymo procesą.

- Kurti kokybės užsakymus, paremtus aktyvinimo taškais, pvz., „gaunant produktus‟ (gavimo operacijomis) arba „paimant produktus‟ (siuntimo operacijoms).
- Dokumentuoti bandymų rezultatus ir nustatyti, ar rezultatai atitinka nustatytus bandymų kriterijus ir priimtiną kokybės lygį.
- Teikiant ataskaitas, tikrinimo proceso metu naudoti dokumentų valdymą, skirtą išsamioms produkto specifikacijoms ir konkrečių naudotojų pastaboms.
- Prižiūrėti neatitinkančius produktus ir juos koreliuoti su papildoma neatitikimo informacija, kad būtų galima atsekti pradinę problemos priežastį.
- Dokumentuoti neatitikimo valdymo išlaidas. Išlaidos gali būt prekės (pvz., atsarginės dalys), papildomos išlaidos ir tabelio valandos, kurių reikia norint ištaisyti neatitikimą.
- Naudojant taisymų apdorojimą, kuris yra susijęs su kokybės užsakymais, planuoti klaidų taisymo procesus.

[![Kokybės valdymo procesas.](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>Produktų bandymai ir kokybės užsakymai

Produktų bandymai paprastai vadinami kokybės kontrole ir naudoja kokybės užsakymus. Naudodami kokybės kontrolės funkcijas, galite atlikti toliau nurodytus veiksmus.

- Apibrėžti turimus atlikti medžiagos bandymus. Šie bandymai apima kokybės specifikacijas, naudojamą bandymo prietaisą, bandymą aprašančius dokumentus, pavyzdžių ėmimo planą ir priimtiną kokybės lygį (AQL).
- Sukurti kokybės užsakymą, identifikuojantį bandymus, kurie turi būti atliekami tam tikram užsakymui, pvz., pirkimo arba gamybos užsakymui arba atsargų kiekiui. Kokybės užsakymą galima sukurti rankiniu būdu arba gali būti automatiškai generuoti remiantis kokybės rekomendacijomis.
- Apibrėžti kokybės rekomendacijas, kiekviename verslo procese susijusias su pirkimu, sulaikymu, gamyba arba pardavimo užsakymais, kad kokybės užsakymą, identifikuojantį bandymų reikalavimus gaunamoms arba išsiunčiamoms medžiagoms, būtų galima generuoti automatiškai.
- Įrašyti bandymų rezultatus kokybės užsakyme, tikrinti bandymų rezultatus AQL atžvilgiu ir išspausdinti analizės sertifikatą, rodantį bandymų rezultatus.

## <a name="nonconformance"></a>Neatitikimas

Neatitikimas apibūdina prekę, kuri turi kokybės problemą. Neatitiki procesas suteikia galimybę kurti neatitikimo užsakymą, aprašantį neatitikimo medžiagos kiekį, problemos šaltinį, problemos tipą ir aiškinamąsias pastabas. Galima apibrėžti problemų tipų klasifikaciją, siekiant palengvinti neatitinkančios medžiagos analizę. Norėdami kreipti neatitinkančios medžiagos perdavimą, taip pat galite spausdinti neatitikimo žymę ir neatitikimo ataskaitą. Pavyzdžiui, žymė ir ataskaita gali nurodyti **Netinkamo naudoti** arba **Apriboto naudojimo** būklę.

Toliau pateiktoje lentelėje išvardyti šeši numatytieji neatitikimo tipai ir aprašoma kiekvieno tipo informacija, kurią reikia įrašyti.

| Neatitikties tipas | Šaltinio informacija |
|---|---|
| Klientas | Kliento sąskaitos numeris, pardavimo užsakymo numeris arba pardavimo užsakymo operacijos partijos numeris. Pavyzdžiui, neatitikimas gali būti susijęs su konkrečia pardavimo užsakymo siunta arba kliento grįžtamuoju ryšiu apie produkto kokybę. |
| Aptarnavimo užklausa | Kliento sąskaitos numeris, pardavimo užsakymo numeris arba pardavimo užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su konkrečia pardavimo užsakymo siunta arba su kliento nusiskundimu dėl prekės kokybės. |
| Tiekėjas | Tiekėjo sąskaitos numeris, pirkimo užsakymo numeris arba pirkimo užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su pirkimo užsakymo gavimu arba tiekėjo rūpesčiu dėl dalies, kurią jis tiekia. |
| Gamyba | Gamybos užsakymo numeris arba gamybos užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su konkrečiu pagamintu paketu. |
| Vidinis | Kokybės užsakymo numeris arba kokybės užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su bandymais, kurie atliekami kaip kokybės užsakymo dalis arba su darbuotojo rūpesčiu dėl produkto kokybės. |
| Sudėtinio produkto gamyba | Sudėtinio produkto gamybos užsakymo neatitikimas, susijęs su paketinės gamybos užsakymais. |

Neatitikimai susieti su problemos tipu. Problemų tipai apibrėžiami puslapyje **Problemų tipai**, kuriame nurodote, kuriuos problemų tipus galima susieti su kiekvienu neatitikimo tipu. Pvz., **Aptarnavimo užklausos** tipo neatitikimo problemų tipai gali atspindėti kliento nusiskundimų klasifikaciją, o **Vidinio** tipo neatitiktimo problemų tipai gali nurodyti defekto kodų klasifikaciją.

Kuriant naują neatitikimą, pasirenkamas neatitikimo tipas ir problemos tipas. Pradinė patvirtinimo būsena yra **Naujas**, kuri nurodo užklausą veikti. Kitas veiksmas yra patvirtinimo būseną pakeisti į **Patvirtinta** arba **Atsisakyta**, kad nurodytumėte, jog dėl neatitikimo veiksmų imsitės arba ne. Neatitikimą taip pat galite uždaryti (pasirinkdami atskirą žymės langelį), taip nurodydami, kad veiksmus su juo baigėte, arba neatitikimą galite atidaryti iš naujo, kad parodytumėte, jog jį reikia labiau apsvarstyti.

Įvesti neatitikimo komentarus galite pridėdami dokumentą. Naudinga naudojant **Dokumento tipo** puslapį apibrėžti unikalų neatitikimų dokumento tipą. Tada galite naudoti puslapį **Ataskaitos sąranka** ir apibrėžti, ar neatitikimo ataskaitoje ir neatitikimo žymėje turėtų būti spausdinami šio dokumento tipo komentarai. Atitikimo ataskaita ir neatitikimo žymė gali padėti atlikti medžiagų perdavimą. Pagal pasirinkimo kriterijus, kurie susieti su neatitikimu, galite selektyviai generuoti ataskaitas ir žymes. Šie kriterijai apima neatitikimo numerį, prekę, klientą, tiekėją ir būseną.

Neatitikimo ataskaitoje rodomas neatitikimo numeris, prekė ir problemos tipas. Atsižvelgiant į jūsų ataskaitos sąrankos strategiją, ataskaitoje taip pat gali būti rodomos susijusios pastabos apie neatitikimą. Neatitikimo žymėje rodoma panaši informacija, ir ji taip pat apima sulaikymo zoną bei tipą (pvz., **Apriboto naudojimo** ar **Netinkamo naudoti**), kurį priskyrėte neatitikimui norėdami palengvinti brokuotų medžiagų perdavimą.

## <a name="approved-nonconformance"></a>Patvirtintas neatitikimas

Patvirtintai neatitikčiai galite pasirinktinai nurodyti vieną ar daugiau susijusių operacijų. Susijusioje operacijoje apibūdinamas darbas, kuris turi būti atliktas, ir pateikiamas jūsų nustatytas kokybės operacijų sąrašas ir darbo priežasties aprašomasis tekstas. Neprivaloma: apibrėžę operaciją galite apibrėžti papildomas išlaidas, prekes ir tabelio darbo valandas, kurių reikia norint atlikti darbą. Rodomos apskaičiuotos susijusios operacijos išlaidos ir bendroji neatitikties išlaidų suma. Apskaičiuotos išlaidos ir pridėta išsami informacija (apie prekes, darbo valandas ir papildomas išlaidas) pateikiama kaip nuorodos informacija, ir jos naudojamos tik su kokybės valdymo funkcija.

Neprivaloma: galite sukurti kokybės užsakymą pagal neatitikimą – pirmiausia atlikite kokybės užsakymų užklausą ir tada sukurkite naują kokybės užsakymą. Pvz., kokybės užsakyme gali būti identifikuotas poreikis bandyti (arba iš naujo bandyti) brokuotą medžiagą. Naujai sukurtame kokybės užsakyme rodomas saitas su pradiniu neatitikimu.

Neprivaloma: galite susieti vieną neatitikimą su kitu ir sukurti naują neatitikimą iš esamo. Pvz., saitas gali atspindėti kokybės problemų tarpusavio ryšį.

## <a name="correction-handling"></a>Taisymų apdorojimas

**Taisymų** puslapyje galima sukurti neatitikimų, kuriuos reikia ištaisyti, sąrašą. Kiekvienas taisymo elementas yra susietas su diagnostikos tipu, dėl kurio aptikta problema. Puslapyje **Taisymai** taip pat pateikiama informacija apie tai, kas ir kada turi atlikti taisymo veiksmą. Prie taisymo pridėdami dokumentą galite pateikti išsamią informaciją apie problemą ir reikiamą taisymo veiksmą. Neatitikimą apsvarsčius ar ištaisius, taisymo elementas „uždaromas‟ pasirenkant parinktį **Baigta**. Taip pat galite nurodyti, kad sprendimas buvo trumpalaikis.

Naudinga naudojant **Dokumento tipo** puslapį apibrėžti unikalų taisymų dokumento tipą. Tada galite naudoti puslapį **Ataskaitos sąranka** ir apibrėžti, ar taisymo ataskaitoje spausdinami šio dokumento tipo komentarai. Išspausdintoje taisymo ataskaitoje rodoma informacija apie neatitikimą ir susijusios neatitikimo pastabos. Ataskaitoje taip pat pateikiama taisymo informacija, pvz., diagnostikos tipas ir susijusios taisymo pastabos.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Atsargų blokavimas](inventory-blocking.md)
- [Sulaikymo užsakymai](quarantine-orders.md)
- [Prekių kokybės tikrinimas](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
