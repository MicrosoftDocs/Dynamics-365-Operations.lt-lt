---
title: Pardavimo užsakymo registravimas
description: Šioje temoje pateikiama informacija apie atsargų registravimo šablono puslapio pardavimo užsakymo skirtuką.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5d84723b51d6977867fa162c4a47befa61bd9ef6
ms.sourcegitcommit: dc3053625dfe24aef64399dd1d002214e7f7619f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755934"
---
# <a name="sales-order-posting"></a>Pardavimo užsakymo registravimas

Skirtuko **Pardavimo užsakymas**, kuris yra **atsargų registravimo šablonų** puslapyje, valdymas, kaip pardavimo užsakymai bus registruojami DK. Dvi pagrindinės veiklos užregistruojamos pardavimo užsakymo DK: 

- Važtaraštis
- Sąskaita faktūra

Norint, kad faktinė operacija (važtaraštis) būtų užregistruojama DK pardavimo užsakyme, turi būti tenkinamos šios sąlygos:

- Atsargų ir **sandėlio valdymo parametrų puslapyje**, žymės langelis **Registruoti važtaraštį DK** turi būti pažymėtas.
- **Pardavimo užsakymo eilutėje** pasirinktos prekės prekių modelių grupės puslapyje žymės **langelis** Registruoti faktines atsargas DK turi būti pažymėtas.
- **Atsargų registravimo šablono puslapyje** turi būti nurodytos šių registravimo tipų pagrindinės sąskaitos:
  - Pristatytų vienetų savikaina
  - Parduotų ir pristatytų prekių savikaina

Norint, kad finansinė operacija (SF) būtų užregistruojama DK pardavimo užsakyme, turi būti tenkinamos šios sąlygos:

- **Pardavimo užsakymo eilutėje** pasirinktos prekės prekių modelių grupės puslapyje žymės **langelis Registruoti finansines** atsargas DK turi būti pažymėtas.
- Šių registravimo tipų pagrindinės sąskaitos **turi būti nurodytos atsargų** registravimo šablono puslapyje:
  - Vienetų, kuriems išrašyta SF, savikaina
  - Parduotų prekių savikaina, išrašyta SF
  - Įplaukos
  - Nuolaida\*

> [!NOTE]
> Nuolaidos sąskaita yra pasirinktinė. Daugelis apskaitos taisyklių, pvz., GAAP ir IFRS, reikalauja, kad nuolaidos sumažintų pardavimo įplaukas, todėl šios sąskaitos nėra naudojamos daugelyje scenarijų. Jei leidžia vietinės taisyklės, pardavimo kainos dalį, su nuolaida, naudokite atskirą pagrindinę sąskaitą.

Norint atidėtą (numatomą) įplaukų vertę registruoti DK, kai generuojate pardavimo užsakymo važtaraštį, reikia įvykdyti šias sąlygas:

- **Pardavimo užsakymo eilutėje** pasirinktos prekės prekių modelių grupės puslapyje žymės **langelis** Registruoti faktines atsargas DK turi būti pažymėtas.
- Prekių modelių **grupės puslapyje turi** būti pažymėtas **žymės langelis Registruoti atidėtų įplaukų sąskaitoje, kuri yra** Pardavimo pristatymas.
- Atsargų ir **sandėlio valdymo parametrų puslapyje**, pažymėkite **žymės langelį Registruoti važtaraštį** DK.
- Atsargų ir **sandėlio valdymo parametrų puslapyje** turi būti pažymėtas **žymės langelis Registruoti** fizinį PVM.
- Puslapyje Gautinų **sumų parametrai** turi būti **pažymėtas žymės langelis Registruoti** važtaraštį DK.
- **Atsargų registravimo šablono puslapyje** turi būti nurodytos šių registravimo tipų pagrindinės sąskaitos:
  - Atidėtos įplaukos pristatant
  - Pristatymo atidėtų įplaukų korespondentinė sąskaita
  - Atidėtas PVM pristatant

> [!NOTE]
> Paprastai rekomenduojame įgalinti šias pasirinktis: Registruoti **faktines atsargas ir** **registruoti važtaraštį DK**. Įgalinus šias pasirinktis gali būti pagreitintos mėnesio pabaigos uždarymo procedūros, nes atidėjimų nereikia apskaičiuoti ir registruoti rankiniu būdu. Be to, neautomatinio vykdymo finansinėse ataskaitose bus automatiškai nurodytos atidėtos sumos.

> [!IMPORTANT]
> Parinktis **Registruoti atidėtųjų įplaukų sąskaitoje** pardavimo pristatyme nėra naudojama su įplaukų pripažinimu. Norėdami gauti daugiau informacijos apie įplaukų pripažinimą, eikite į Įplaukų [pripažinimo apžvalgą](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Registravimo šablono konfigūracijos pavyzdys 

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų, kurių pagrindinės sąskaitos ir aprašymai yra pavyzdiniai, pavyzdžiai:
 
- Kliringo **sąskaitos** stulpelis nurodo, kad registravimo tipas yra tarpuskaitos sąskaita. Šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija. 
- Stulpelyje **P/F** nurodomas **finansinio** registravimo faktinio registravimo **P ir F**. 
- Stulpelyje **Sekti** nurodoma, ar konkretaus registravimo tipo pagrindinė sąskaita paprastai yra ta pati, kaip ir kitas registravimo tipas. Stulpelio vertė nurodo registravimo tipą, kuris paprastai naudojamas.

> [!NOTE]
> Šios pagrindinės sąskaitos ir pagrindinės sąskaitos pavadinimai yra tik pasiūlymai. Rekomenduojame dirbti su savo buhalteriu, kad nustatytumėte geriausią konfigūraciją savo verslo poreikiams.


| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | P / F | Atlikite | Aprašymas |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Pristatytų vienetų savikaina | 140100</br>140101 | Medžiagų atsargos</br>Išsiųstos medžiagos, kurių SF neišrašyta | Turtas | Kreditas | Taip | P | Vienetų, kuriems išrašyta SF, savikaina | Naudojamas registruojant pardavimo užsakymo važtaraštį. Korespondentinė sąskaita yra parduotų, pristatytų prekių savikaina. Šioje sąskaitoje nurodyta suma atšaukiama, kai užregistruojama pardavimo užsakymo SF. Galbūt norėsite naudoti medžiagų, kurioms neišrašyta SF, sąskaitą, kad ji atspindėtų faktines atsargas, ir rezervuoti medžiagų atsargų sąskaitą finansinio atnaujinimo metu. |
| Parduotų ir pristatytų prekių savikaina | 500150 | Atidėta PPK | Išlaidos | Debetas | Taip | P  | Naudojamas registruojant pardavimo užsakymo važtaraštį. Sąskaitos korespondentinė sąskaita yra pristatytų vienetų išlaidos. Šioje sąskaitoje nurodyta suma atšaukiama, kai užregistruojama pardavimo užsakymo SF. |
| Vienetų, kuriems išrašyta SF, savikaina | 140100 | Medžiagų atsargos | Turtas | Kreditas | Ne | Pn. | Pristatytų vienetų savikaina | Naudojamas, kai registruojama pardavimo užsakymo SF. Šios sąskaitos korespondentinė sąskaita yra parduotų prekių savikaina, kurios SF išrašyta. Ši sąskaita rodo atsargas jūsų balanso lape. |
| Parduotų prekių savikaina, išrašyta SF | 500100 | PPK medžiagos | Išlaidos | Debetas | Ne | Pn.  | Naudojamas, kai registruojama pardavimo užsakymo SF. Šios sąskaitos korespondentinė sąskaita yra vienetų išlaidos, kurioms išrašyta SF. Ši sąskaita jūsų PL išraše nurodo PGS&amp;. |
| Įplaukos (pardavimo užsakymo įplaukos*) | 400100 | Įplaukų medžiagos | Įplaukos | Kreditas | Ne | Pn.   | Naudojamas, kai registruojama pardavimo užsakymo SF. **Šios sąskaitos korespondentinė sąskaita** yra gautinų sumų registravimo šablone pateikta su suvestine sąskaita (kliento balansas*). |
| Komisiniai (pardavimai, komisiniai*) | 602150 | Komisinių išlaidos | Išlaidos | Debetas | Ne | Pn.  | Naudojama, kai įgalinti ir apskaičiuoti pardavimo komisiniai ir užregistruoti pardavimo užsakymo SF proceso metu. Šios sąskaitos korespondentinė sąskaita yra mokėtinos sumos Komisiniai. |
| Komisinių korespondentinė sąskaita (pardavimas, komisinių korespondentinė sąskaita*) | 201110 | Mokėtini komisiniai | Įsipareigojimai | Kreditas | Taip | Pn. | Naudojama, kai įgalinti ir apskaičiuoti pardavimo komisiniai ir užregistruoti pardavimo užsakymo SF proceso metu. Šios sąskaitos korespondentinė sąskaita yra Komisinių išlaidos. |
| Atidėtos pristatymo įplaukos (pardavimas – važtaraščio įplaukos*) | 401400 | Sukauptas pardavimas | Įplaukos | Kreditas | Taip | P  | Naudojama, kai yra įgalintos atidėtos pristatymo įplaukos ir yra užregistruojamos, kai apdorosite pardavimo užsakymo važtaraštį. Šios sąskaitos korespondentinė sąskaita yra atidėtų įplaukų korespondentinė sąskaita. Šioje sąskaitoje sumos automatiškai atšaukiamos, kai registruojate pardavimo užsakymo SF. |
| Atidėtų įplaukų korespondentinė sąskaita pristatyme (Pardavimas – važtaraščio įplaukų korespondentinė)* | 130400 | Gautinos sumos – neišrašyta SF | Turtas | Debetas | Taip | P  | Naudojama, kai atidėtos pristatymo įplaukos įgalintos ir užregistruojamos, kai apdorosite pardavimo užsakymo važtaraštį. Šios sąskaitos korespondentinė sąskaita yra atidėtos pristatymo įplaukos. Šioje sąskaitoje sumos automatiškai atšaukiamos, kai registruojate pardavimo užsakymo SF. |
| Atidėtas PVM pristatuojant (pardavimas, važtaraščio mokestis*) | 250500 | Atidėtas PVM | Įsipareigojimai | Kreditas | Taip | P  | Naudojama, kai yra įgalintos atidėtos pristatymo įplaukos ir įgalintas faktinio PVM registruoti. Mokesčio suma registruojama, kai apdorosite pardavimo užsakymo važtaraštį. |

\* Vertės, rodomos skliausteliuose šioje lentelėje nurodo vertę, **kuri** naudojama kvito operacijų puslapio **lauke Registravimo** tipas. Galite peržiūrėti registravimo **tipą kvito** **operacijų puslapyje**, kuris yra skirtuke **Bendra**.

## <a name="sales-category-posting"></a>Pardavimo kategorijos registravimas

Alternatyvą nustatyti visų prekių, prekių grupės arba vienos prekės atsargų registravimą, nustatyti kategorijas ir valdyti DK registravimą pagal pardavimo kategorijas. Norėdami gauti daugiau informacijos apie kategorijų hierarchijos nustatymą ir kategorijų priskyrimą produktams, [...](/supply-chain/pim/tasks/create-hierarchy-product-classification.md)[eikite į Produktų klasifikacijos hierarchijos kūrimas ir Klasifikuoti produktą naudojant kategorijų hierarchijas.](/supply-chain/pim/tasks/classify-product-category-hierarchies.md)

Sukūrę kategorijų hierarchiją, turite priskirti hierarchiją vienam arba daugiau tipų. Norėdami naudoti kategorijų hierarchiją pardavimo užsakymuose, turite priskirti kategoriją pardavimo kategorijų hierarchijos tipui. Daugiau informacijos rasite kategorijų [hierarchijoms.](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md)

## <a name="create-revenue-posting-by-sales-category"></a>Kurti įplaukų registravimą pagal pardavimo kategoriją

Norėdami priskirti dk registravimus pardavimo užsakymui pagal pardavimo kategoriją, atlikite šiuos veiksmus:

1. Eikite į **Atsargų valdymas** > **Sąranka** > **Registravimas** > **Registravimas**.
2. Pasirinkite skirtuką **Pardavimas**.
3. Pasirinkite radijo mygtuką, kurį norite konfigūruoti registravimo tipui (pvz., **Įplaukos**).
4. Pasirinkite **Nauja**.
5. **Lauke Prekės kodas** pasirinkite **Kategorija**.
6. Naudokite lauką **Kategorijos** ryšys, kad pasirinktumėte registravimo šablono kategoriją.
7. Lauke Sąskaitos **kodas pasirinkite** pasirinktį Lentelė **, Grupė** **arba** **Visi.** Pavyzdžiui, norėdami pritaikyti registravimo šabloną visiems klientams, pasirinkite **Visi**.
   - **Jei 6 veiksme** pasirinkote Lentelė, lauke **Sąskaitos** ryšys pasirinkite konkretų registravimo šablono **tiekėjo** numerį.
   - **Jei 6 veiksme** pasirinkote Grupė, lauke **Sąskaitos** ryšys pasirinkite registravimo šablono **tiekėjų** grupę.
   - **Jei 6 veiksme** pasirinkote Visi **, sąskaitos ryšio** laukas bus paliktas tuščias.

8. Norėdami susieti tam tikrą pvm grupę, kurios registravimo tipas pasirinktas, pasirinkite **PVM grupę**. Jei šį lauką paliksite tuščią, registravimo tipas bus taikomas visoms esamoms mokesčių grupėms. Nurodytas mokesčių grupių registravimas taikomas tik su pardavimu ir pirkimu atliktioms operacijoms.

9. Lauke Pagrindinė **sąskaita nurodykite** sąskaitos, kurioje norite registruoti sąskaitos tipą, numerį. Sąskaitų lentelėje pasirinkite vieną iš esamų sąskaitų plano sąskaitos numerių.
