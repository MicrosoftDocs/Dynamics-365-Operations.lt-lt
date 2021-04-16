---
title: Tiekėjo SF įrašo darbo sritis
description: Šioje temoje paaiškinama, kaip nustatyti darbo sritį, kuri susijusi su tiekėjo SF ir kurioje pateikiama informacija, pasiekiama naudojant „Microsoft Power BI”.
author: abruer
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bac57056af6d85bb30600e13628279801508741d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837265"
---
# <a name="vendor-invoice-entry-workspace"></a>Tiekėjo SF įrašo darbo sritis

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip nustatyti darbo sritį, kuri susijusi su tiekėjo SF ir kurioje pateikiama informacija, pasiekiama naudojant „Microsoft Power BI”. Šios darbo srities tiekėjo SF informacija filtruojama konkretiems vartotojams ir rodoma grafiniu formatu.

## <a name="overview"></a>Peržiūra

Darbo srityje **Tiekėjo SF įrašas** rodoma informacija, susijusi su tiekėjo SF apdorojimu. Joje yra rodinys **Mano darbas** ir puslapis **Analizė – visos įmonės**. Rodinyje **Mano darbas** rodomos suvestinės plytelės, tiekėjų operacijų tinkleliai ir susijusi tiekėjų informacija. Puslapyje **Analizė – visos įmonės** naudojantis „Microsoft Power BI“ galimybėmis parodomos su tiekėjų SF susijusios vizualizacijos.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Darbo srities nustatymas, kad būtų rodomas „Power BI” turinys

Turite užbaigti šį nustatymą, kad duomenys būtų rodomi darbo srities **Tiekėjo SF įrašas** „Power BI” vizualizacijose.

1. Darbo srityje **Funkcijų valdymas** filtruokite sąrašą, kad rastumėte funkciją **Tiekėjo SF automatizavimas**.
3. Pasirinkite **Įjungti dabar**.
4. Norėdami užtikrinti, kad SF galima būti apdoroti nuo pradžios iki pabaigos be rankinio įsikišimo, nustatykite tiekėjo SF darbo eigą. Norėdami sukonfigūruoti darbo eigą, eikite į **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų darbo eigos**.
5. Eiti į **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai** ir pasirinkite skirtuką **Tiekėjo SF automatizavimas**. Daugiau informacijos žr. [Tiekėjo SF automatizavimo nustatymo parinktys](vnd-invoice-set-up-options.md).
6. Nustatykite parinktį **Automatiškai pateikti importuotas SF darbo eigos sistemai** į **Taip**.
7. Jei produkto gavimo kvitai turi būti automatiškai sugretinti, nustatykite parinktį **Automatiškai sugretinti produktų gavimo kvitus su SF eilutėmis** į **Taip**.
8. Peržiūrėkite likusius pasirinktinius parametrus ir konfigūruokite juos pagal jūsų organizacijos reikalavimus.
9. Eikite į **Sistemos administravimas \> Sąranka \> Sistemos parametrai** ir nustatykite laukus **Sistemos valiuta** ir **Sistemos valiutos kursas**.
10. Eikite į **Didžioji knyga \> Sąranka \> Didžioji knyga** ir nustatykite laukus **Apskaitos valiuta** ir **Valiutos kurso tipas**.
11. Eikite į **Didžioji knyga \> Valiutos \> Valiutų kursai** ir įveskite valiutos kursus tarp operacijos valiutos ir apskaitos valiutos bei tarp apskaitos valiutos ir sistemos valiutos.
12. Eikite į **Sistemos administravimas \> Sąranka \> Objektų saugykla** ir ieškokite **Tiekėjo SF automatizavimo matavimas**. Pasirinkite **Atnaujinti**.

Norėdami peržiūrėti informaciją, rodomą darbo srityje, turite turėti mokėtinų sumų vadovo arba mokėtinų sumų klerko saugos vaidmenį.

## <a name="my-work-view"></a>Mano darbo rodinys

### <a name="company-selection"></a>Įmonės pasirinkimas

Kai funkcija **Automatizuoti tiekėjo SF** įjungta, darbo srities viršuje atsiranda laukas **Įmonė**. Pasirinkus lauką **Įmonė**, paveikiama visa darbo srityje rodoma informacija. Pagal numatytuosius nustatymus rodinyje rodoma įmonės, prie kurios prisijungėte, informacija. Pasirinkus kitą įmonę lauke **Įmonė**, galima rodyti tos įmonės informaciją darbo srityje. Tada galite pasirinkti darbo srities plytelę, norėdami eiti į susijusį pasirinktos įmonės puslapį.

### <a name="summary-tiles"></a>Suvestinės išklotinės

Rodinio **Mano darbas** dalies **Laukiančių SF suvestinė** plytelėse pateikiama jūsų tiekėjo SF būsenų apžvalga. Galite peržiūrėti dar neregistruotus žurnalus ir sulaikytas SF. Be to, yra keturios toliau pateiktos plytelės, susietos su funkcija Tiekėjo SF automatizavimas.

- Būtinas rankinis gavimo kvito gretinimas
- Gretinimo tikrinimas nesėkmingas
- SF nepateiktos darbo srautui
- SF neimportuotos

(Šios keturios plytelės reikalauja, kad funkcijų valdyme būtų įjungta funkcija Tiekėjo SF automatizavimas.)

Norint naudoti plytelę **Atkurti tiekėjo SF**, funkcija turi būti įjungta mokėtinų sumų parametruose. Eikite į **Mokėtinos sumos \> Mokėtinų sumų parametrai**, tada skirtuke **SF** nustatykite parinktį **Leisti tiekėjo SF atkūrimą** į **Taip**.

Kai funkcija įjungta, darbo srities skyriuje **Žurnalai** matysite tris sugrupuotas plyteles. Plytelių pavadinimai yra **Žurnalai**, **Žurnalai – priskirti man** ir **SF telkinys**. 

Dalyje **Laukiančių SF suvestinė** esanti informacija skirta įmonei, kuri nustatyta kaip numatytoji jūsų prisijungimo įmonė.

### <a name="creating-new-records"></a>Naujų įrašų kūrimas

Norėdami sukurti naują SF įrašą, pasirinkite **Naujas**, tada sąraše pasirinkite vieną iš toliau pateiktų įrašų tipų.

- Tiekėjo SF
- SF žurnalas
- Visuotinis sąskaitų faktūrų žurnalas
- SF registras
- SF patvirtinimas

Atkreipkite dėmesį, kad jūsų sukurtas įrašas yra paremtas įmonės filtru, o ne įmone, prie kurios esate prisijungęs. Pavyzdžiui, esate prisijungęs prie įmonės **UMSF**, bet įmonės filtras nustatytas į **GBSI**. Šiuo atveju, kai pasirenkate **Naujas** ir tada pasirenkate įrašo tipą sąraše, įrašas sukuriamas GBSI įmonėje.

### <a name="documents-not-invoiced-grids"></a>Tinkleliai srityje Dokumentai, kurių SF neišrašytos

Skyriuje **Dokumentai, kurių SF neišrašytos** yra tinklelių, kurie nurodo dokumentus, laukiančius tiekėjo SF.

Tinklelyje **Atidaryti pirkimo užsakymai** pateikiami visi pirkimo užsakymai, kurių visos SF dar nėra išrašytos. Norėdami sukurti pirkimo užsakymo tiekėjo SF, galite naudoti mygtuką **Išrašyti SF dabar**. Norėdami sukurti pirkimo užsakymo tiekėjo išankstinio mokėjimo SF, galite naudoti mygtuką **Išrašyti išankstinio mokėjimo SF dabar**.

Tinklelyje **Produkto gavimo kvitai** pateikiamos pirkimo gavimo operacijos, kurių visos SF dar nėra išrašytos. Norėdami sukurti pirkimo užsakymo tiekėjo SF, galite naudoti mygtuką **Išrašyti SF dabar**.

Tinklelyje **Laukiančios tiekėjo SF** rodomos visos tiekėjo SF, kurios dar nepateiktos darbo eigos sistemai. Norėdami ieškoti konkrečios tiekėjo SF, galite naudoti lauką **Ieška** ir (arba) įmonės filtrą. Norėdami redaguoti tinklelyje rodomą operaciją, galite naudoti mygtuką **Redaguoti**.

Norėdami ieškoti konkretaus pirkimo užsakymo, galite naudoti lauką **Ieška**, esantį tinklelyje **Rasti pirkimo užsakymą**.

### <a name="related-information"></a>Susijusi informacija

Galite peržiūrėti informaciją apie užregistruotas SF naudodami saitus, esančius dešinėje darbo srities pusėje. Šie saitai apima **Atidarytos tiekėjo SF**, **SF žurnalas** ir **SF retrospektyva ir gretinimo informacija**. Dalyje **Tiekėjai** galite pasiekti filtruotą sąrašą, kuriame rodomi visi sulaikyti tiekėjai, arba galite naudoti saitą **Visi tiekėjai**. Taip pat galimi saitai **Visi pirkimo užsakymai** ir **Atidaryti išankstiniai mokėjimai**.

### <a name="analytics--all-companies-page"></a>Puslapis Analizė – visos įmonės

Kai puslapyje **Mokėtinų sumų parametrai** parinktis **Automatiškai pateikti importuotas SF darbo eigos sistemai** nustatyta į **Taip**, galite peržiūrėti automatizavimo analizę. Puslapis **Analizė – visos įmonės** teikia svarbią metriką, pvz., tiekėjo SF, kurias tvirtina tvirtintojas ir įmonė. Šiame puslapyje yra penki ataskaitos puslapiai. Viename puslapyje pateikiama apžvalga, o kituose puslapiuose pateikiama informacija apie mokėtinų sumų automatizavimo metriką.

Toliau pateikiamoje lentelėje nurodyti kiekviename ataskaitos puslapyje pateikiami vaizdai.

| Ataskaitų puslapis                    | Vizualizacijos |
|--------------------------------|----------------|
| Tiekėjo SF apžvalga        | <ul><li>Laukiančios tiekėjo SF sistemos valiuta automatizavimo metu</li><li>SF, kurių importavimas nepavyko</li><li>SF darbo eigoje</li><li>Bekontaktės SF per paskutines 30 dienų</li><li>Iš viso automatizuotų SF per paskutines 30 dienų</li><li>Atidarytų SF balansas sistemos valiuta</li><li>Klaidų priežastys per paskutines 30 dienų</li><li>Automatiškai apdorotų užregistruotų SF procentinė dalis</li><li>SF apdorojimo dienos</ul></li> |
| Automatizavimo būsena              | <ul><li>Bekontaktės SF per paskutines 30 dienų</li><li>Bekontaktės SF per paskutines 30 dienų pagal įmonę</li><li>Bekontaktės SF per paskutines 30 dienų pagal tiekėjų grupę</li><li>Automatiškai apdorotų užregistruotų SF procentinė dalis</li><li>SF apdorojimo dienos</li></ul> |
| SF, kurių importavimas nepavyko | <ul><li>SF, kurių importavimas nepavyko</li><li>SF, kurių importavimas nepavyko, pagal įmonę</li></ul> |
| Automatizavimo klaidų priežastys | <ul><li>Nepavykusios SF</li><li>Nepavykusios SF pagal įmonę</li><li>Nepavykusios SF pagal tiekėjų grupę</li></ul> |
| Darbo eigos būsena                | <ul><li>SF darbo eigoje</li><li>Tiekėjo SF darbo eigos egzemplioriai</li><li>Priskyrimai vienam tvirtintojui</li><li>Tiekėjo SF darbo eigos vienai įmonei</li><li>Vidutinis darbo eigos dienų skaičius pagal tvirtintoją</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]