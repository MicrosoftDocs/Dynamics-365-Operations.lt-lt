---
title: Pirkimo užsakymo registravimas
description: Šioje temoje aprašomas atsargų registravimo šablono puslapio pirkimo užsakymo skirtukas.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 4b36ab9da22da7d4f3e62bd2d2aba2a2ec80e60f
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2022
ms.locfileid: "8803052"
---
# <a name="purchase-order-posting"></a>Pirkimo užsakymo registravimas

Pirkimo **užsakymo skirtukas**, **kuris yra atsargų registravimo šablonų** puslapyje, naudojamas valdyti, kaip pirkimo užsakymai bus užregistruojami DK. Dvi pagrindinės veiklos registruojasi DK pirkimo užsakyme: 

- Produkto gavimo kvitas
- Sąskaita faktūra

Norint, kad faktinė operacija (produkto gavimo kvitas) būtų užregistruojama DK pirkimo užsakyme, reikia pažymėti šiuos žymės langelius:

- Atsargų **ir sandėlio valdymo parametrų** puslapyje žymės langelis **Registruoti produkto gavimo kvitą** DK.
- Prekių **modelių grupių puslapio** žymės **langeliai Registruoti faktines atsargas ir** **Sukaupti įsipareigojimus produkto gavimo kvite**.

Šių registravimo tipų pagrindinės sąskaitos turi **būti nurodytos** atsargų registravimo šablono puslapyje:

- Gautų pirkimo medžiagų savikaina
- Pirkimo išlaidos, neišskaitytos
- Pirkimas, kaupimas

Norint, kad pirkimo užsakyme būtų registruojamos finansinės operacijos (SF) į DK, turi būti įvykdytos šios sąlygos:

- Prekės **, pasirinktos pirkimo užsakymo** eilutėje, puslapis **Prekių modelių** grupės turi būti pažymėtas žymės langelis Registruoti finansines atsargas.
- Šių registravimo tipų pagrindinės sąskaitos turi **būti nurodytos** atsargų registravimo šablono puslapyje:
  - Nusipirktų medžiagų, kurioms išrašyta SF, savikaina
  - Produkto pirkimo išlaidos
  - Išlaidų pirkimo išlaidos
  - Nuolaida (pasirinktinai)

## <a name="fixed-receipt-price-posting"></a>Fiksuotos gavimo kainos registravimas

Fiksuotą **·** **·** **gavimo** kainą galite naudoti kaip standartinę produkto savikainą, kaip alternatyvą pasirinkties Standartinė savikaina pasirinktis prekės atsargų modelio lauke Prekių modelių grupės. Pagrindinis skirtumas yra tas, **kad kai** naudojama fiksuota gavimo kaina, registruojant atsargų gavimą prekei bus naudojama esama savikaina. Nėra fiksuotos gavimo kainos išlaidų perkainojimo **proceso**; kai užregistruojamas finansinis atnaujinimas, registravimo metu naudojama esama savikaina. Jei yra skirtumas tarp savikainos, naudojamos kvite ir SF, nuokrypis bus užregistruojaas fiksuotos gavimo kainos pelno ir nuostolio sąskaitose.

Norėdami produktui naudoti fiksuotą gavimo kainą, turite sukonfigūruoti:

- Prekių modelių **grupių puslapyje** pažymėkite žymės langelius **Registruoti faktines atsargas** ir **Fiksuota** gavimo kaina. 
- Atsargų ir **sandėlio valdymo parametrų puslapyje** pažymėkite žymės langelį **Registruoti važtaraštį** DK.
- **Atsargų registravimo šablono** puslapyje nurodykite šių registravimo tipų pagrindines sąskaitas:
  - Fiksuotos gavimo kainos pelnas
  - Fiksuotos gavimo kainos nuostolis
  - Fiksuotos gavimo kainos korespondentinė sąskaita

Daugiau informacijos ieškokite Fiksuota [gavimo kaina](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Pirkimo išlaidų ir atsargų pokyčio registravimas

Jei planuojate atlikti pirkimo išlaidų ir atsargų variacijų sąskaitą, atlikite šiuos veiksmus:

- Mokėtinų **sumų parametrų** puslapyje, SF **skirtuke**, pažymėkite žymės langelį **Registruoti į mokesčių** sąskaitą DK.
- Pirkimo užsakymo **eilutėje pasirinktos prekės prekių modelių grupių puslapyje pažymėkite** **žymės langelius** Registruoti faktines atsargas, **·** **Registruoti finansines atsargas ir Sukaupti įsipareigojimus produkto gavimo kvite.**
- Puslapyje Įsigijimas **ir išlaidų tikrinimas pažymėkite** žymės langelį **Generuoti išlaidas produkto gavimo** kvite.
- Atsargų ir **sandėlio valdymo parametrų puslapyje** pažymėkite žymės langelį **Registruoti važtaraštį** DK.

**Atsargų registravimo šablono** puslapyje turite nurodyti šių registravimo tipų pagrindines sąskaitas:

- Pirkimo išlaidos, neišskaitytos
- Produkto pirkimo išlaidos
- Atsargų nuokrypis

> [!NOTE]
> **Išlaidų** registravimo tipas nėra naudojamas, kai pasirinktas **DK parametro registravimo išlaidų** sąskaitoje.

Norėdami gauti daugiau informacijos, eikite į [Registruoti į mokesčių sąskaitos apskaitos principą](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Registravimo šablono konfigūracijos pavyzdys

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų, kurių pagrindinės sąskaitos ir aprašymai yra pavyzdiniai, pavyzdžiai:

- Kliringo **sąskaitos** stulpelis nurodo, kad registravimo tipas yra tarpuskaitos sąskaita. Šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija. 
- Stulpelyje **P/F** nurodomas **finansinio** registravimo faktinio registravimo **P ir F**. 
- Stulpelyje **Sekti** nurodoma, ar konkretaus registravimo tipo pagrindinė sąskaita paprastai yra ta pati, kaip ir kito registravimo tipo. Stulpelio vertė nurodo registravimo tipą, kuris paprastai naudojamas.

> [!NOTE]
> Pagrindinės sąskaitos ir pagrindinės sąskaitos pavadinimai yra tik pasiūlymai. Rekomenduojame<!--note from editor: Via Writing Style Guide.--> , kurią dirbate su savo apskait dirbate norėdami nustatyti geriausią konfigūraciją jūsų verslo poreikiams.


| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | P / F | Atlikite | Aprašymas |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Gautų nusipirktų medžiagų savikaina | 140100</br>140101 | Medžiagų atsargos</br>Išsiųstos medžiagos, kurių SF neišrašyta | Turtas | Debetas | Taip | P | Nusipirktų medžiagų, kurioms išrašyta SF, savikaina | Naudojamas, kai registruojamas pirkimo užsakymo produkto gavimo kvitas. Sąskaitos korespondentinė sąskaita yra pirkimo išlaidos, nenuskaitytos. Šioje sąskaitoje nurodyta suma atšaukiama, kai užregistruojama pirkimo užsakymo SF. |
| Pirkimo išlaidos, neišskaitytos | 600180 | Medžiagų gavimas | Išlaidos | Debetas | Taip | P | |Naudojamas, kai registruojamas pirkimo užsakymo produkto gavimo kvitas. Sukuriami du kvitai gavimui, kad būtų sekami pirkimo kainų nuokrypiai, kai naudojama standartinė savikaina. Pirmo kvito sąskaitos korespondentinė sąskaita yra pirkimo kaupimas. Antrame kvite esantis korespondentinis kvitas yra gautų įsigytų medžiagų išlaidų ir pirkimo kainų nuokrypio sąskaitų suma. Šioje sąskaitoje registruojamos sumos atšaukiamos, kai užregistruojama pirkimo užsakymo SF. |
| Nusipirktų medžiagų, kurioms išrašyta SF, savikaina | 140100 | Medžiagų atsargos | Turtas | Debetas | Ne | Pn.  |Gautų nusipirktų medžiagų savikaina | Naudojamas, kai registruojama pirkimo užsakymo SF. Šios sąskaitos korespondentinė sąskaita yra produkto pirkimo išlaidos. Ši sąskaita rodo atsargas jūsų balanso lape. Paprastai naudojama ta pati sąskaita, kuri naudojama pristatytų vienetų savikainai ir pardavimo užsakymui išrašytų vienetų išlaidų SF. |
| Produkto pirkimo išlaidos | 600180 | Medžiagų gavimas | Išlaidos | Kreditas | Ne | Pn.  | |Naudojamas, kai registruojama pirkimo užsakymo SF. Šios sąskaitos korespondentinė sąskaita yra nupirktų medžiagų savikaina. Ši sąskaita rodo atsargas jūsų balanso lape. |
| Fiksuotos gavimo kainos pelnas (Pirkimas, fiksuotos gavimo kainos pelnas*) | 510310 | Pirkimo kainų nuokrypis | Išlaidos | Kreditas | Ne | Pn. | Fiksuotos gavimo kainos nuostolis | Naudojama, kai užregistruojama pirkimo užsakymo SF ir skiriasi prekės kaina, kurios SF išrašyta, ir numatytosios išlaidos. Ši sąskaita naudojama, kai skirtumas didesnis. Šios sąskaitos korespondentinė sąskaita yra fiksuotos gavimo kainos korespondentinė sąskaita. |
| Fiksuotos gavimo kainos nuostolis (Pirkimas, fiksuotos gavimo kainos nuostolis*) | 510310 | Pirkimo kainų nuokrypis | Išlaidos | Debetas | Ne | Pn. | Fiksuotos gavimo kainos pelnas | Naudojama, kai užregistruojama pirkimo užsakymo SF ir skiriasi prekės kaina, kurios SF išrašyta, ir numatytosios išlaidos. Ši sąskaita naudojama, kai skirtumas mažesnis. Šios sąskaitos korespondentinė sąskaita yra fiksuotos gavimo kainos korespondentinė sąskaita. |
| Fiksuotos gavimo kainos korespondentinė sąskaita (pirkimas, fiksuotos gavimo kainos korespondentinė sąskaita*) | 140900 | Atsargų nuokrypis | Turtas | Abu | Ne | Pn.  | |Naudojama, kai užregistruojama pirkimo užsakymo SF ir skiriasi prekės kaina, kurios SF išrašyta, ir numatytosios išlaidos. Ši sąskaita yra fiksuotos gavimo kainos pelno ir nuostolio sąskaitų korespondentinė sąskaita. |
| Mokestis | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ši sąskaita nebenaudojama. Geriau naudokite atsargų variaciją. |
| Atsargų nuokrypis | 600170 | Atsargų nuokrypis | Išlaidos | Kreditas | Ne | Abu | | Ši sąskaita naudojama, kai: <ul><li>Skiriasi produkto gavimo kvito ir SF vieneto kaina.</li><li>Išlaidos registruojamos prekei.</li><li>Netiesioginės išlaidos buvo<!--note from editor: Edit okay?--> Pridėta prie nupirktų prekių. </li><li>Šios sąskaitos korespondentinė sąskaita yra pirkimo išlaidos, sąskaita, į kurias neišskaitinėta sąskaita.</li></ul> |
| Pirkimas, kaupimas | 200140 | Sukaupti pirkimai | Įsipareigojimai | Kreditas | Y | P | |Naudojama, kai registruojamas pirkimo užsakymo produkto gavimo kvitas ir įgalinta pirkimo sumų kaupimo pasirinktis. |
| Sukauptas PVM gaunant | 250500 | Sukauptas PVM | Įsipareigojimai | Kreditas | Y | Abu  | |Ši sąskaita naudojama, kai atsargų ir **sandėlio** **valdymo** parametruose pasirenkate parinktį Registruoti faktiškai mokestį, o pirkimo užsakymas turi būti apmokestintas. Suma užregistruojama, kai faktiškai atnaujinate pirkimo užsakymą (produkto gavimo kvitą) ir atšaukiate, kai pirkimo užsakymą užregistruojate finansiškai (SF). |
| Ilgalaikio turto gavimas (ilgalaikio turto debetas*) | 180100 | Materialusis ilgalaikis turtas | Turtas | Debetas | N | Abu | Abu | Ši sąskaita naudojama, kai pasirenkate ilgalaikio turto pirkimo užsakymo eilutės pasirinktį. Pirkimo užsakymo integravimas sukonfigūruotas įsigyti ilgalaikį turtą gavimo dokumento ar SF metu. Norėdami gauti daugiau informacijos apie ilgalaikio turto pirkimo užsakymo integravimą, eikite į [Įsigyti turtą per įsigijimą](/fixed-assets/acquire-assets-procurement). |
| Išlaidų pirkimo išlaidos | 618900 | Papildomos išlaidos | Išlaidos | Debetas | N | Abu | |Naudojama registruojant pirkimo užsakymo, kuriame prekės nėra sandėliuotos arba naudojama įsigijimo kategorija, gavimo kvitą ar SF. |
| Išankstinis apmokėjimas | 132190 | Iš anksto apmokėtos išlaidos | Turtas | Debetas | N | Abu | | Naudojama apdorojant išankstinio mokėjimo SF pirkimo užsakyme. |


\* Skliausteliuose rodomos vertės nurodo vertę, kuri naudojama kvito **operacijų** puslapio lauke **Registravimo** tipas. Galite peržiūrėti registravimo **tipą kvito** **operacijų puslapyje**, kuris yra skirtuke **Bendra**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Ilgalaikio turto registravimas su pirkimo užsakymais

Jei naudojate ilgalaikio **turto** modulį ir planuojate ilgalaikio turto pirkimą pirkimo užsakymuose, **·** **·** **turite sukonfigūruoti ilgalaikio turto gavimo registravimo tipą atsargų registravimo šablono puslapio skirtuke Pirkimo** užsakymas. Norėdami gauti daugiau informacijos, eikite į Ilgalaikio [turto integravimas](/fixed-assets/fixed-asset-integration.md) ir [Kurti ir gauti turtą iš Mokėtinų sumų](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Išankstinio mokėjimo pirkimo užsakymo SF registravimas

Jei pirkimo užsakymams **planuojate naudoti išankstinio** mokėjimo SF priemonę, **·** **·** **išankstinio apmokėjimo registravimo tipas turi būti pasirinktas atsargų registravimo šablono puslapio skirtuke Pirkimo** užsakymas. Norėdami gauti daugiau informacijos, eikite į [Išankstinio apmokėjimo SF ir išankstinius apmokėjimus](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Pirkimo paraiškos ir pirkimo užsakymo patvirtinimo registravimas

Pirkimo paraiškas ir pirkimo užsakymų patvirtinimus taip pat galima konfigūruoti, kad DK būtų užregistruoti preliminariai biudžeto rezervavimai ir biudžeto rezervavimai. Šiuos registravimus kontroliuoja registravimo aprašas. Daugiau informacijos rasite eikite [į Apie pirkimo užsakymų biudžeto rezervavimus](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Įsigijimo kategorijos registravimas

Alternatyvą nustatyti visų prekių, prekių grupės arba vienos prekės atsargų registravimą, nustatyti kategorijas ir valdyti DK registravimą pagal įsigijimo kategorijas. Norėdami gauti daugiau informacijos apie kategorijų nustatymą ir jų priskyrimą produktams, eikite į [anksčiau šioje temoje pateiktame pavyzdyje](#sample-posting-profile-configuration) registravimo šablono konfigūraciją.

Naudojant kategorijas su pirkimo užsakymais arba tiekėjo SF, **·** **kategorijų hierarchiją reikia priskirti įsigijimo kategorijų hierarchijos tipui kategorijų hierarchijos tipui kategorijų hierarchijos vaidmenų priskyrimo** puslapyje.

### <a name="vendor-invoices-with-procurement-categories"></a>Tiekėjo SF, kurių įsigijimo kategorijos yra

Jei jūsų organizacija kai kuriems pirkiniams naudoja pirkimo užsakymus, o ne kitiems, galite įvairiais būdais apdoroti su pirkimo užsakymu susijusias SF. Tai apima žurnalų naudojimas mokėtinų **sumų** sąskaitose **arba** laukiančių tiekėjo SF puslapyje, kuris naudojamas pirkimo užsakymų SF generuoti. Kuriant SF, skirtas su pirkimo užsakymu susijusioms SF, reikės sukurti kiekvieno tipo išlaidų įsigijimo kategorijas. Turėsite susieti kategoriją su teisinga išlaidų sąskaita atsargų **registravimo šablonų** puslapyje.

Tikslus kategorijų skaičius skirsis atsižvelgiant į išlaidų sąskaitų, kurias naudojate sąskaitų faktūroms registruoti, skaičių. Jums reikės bent vienos įsigijimo kategorijos kiekvienai pagrindinei sąskaitai, kurios išlaidas sudaro ne pirkimo užsakymo SF. Vienoje pagrindinėje sąskaitoje galima naudoti daug kategorijų. Tai gali būti naudinga tinkamumo naudoti, paieškos ir ataskaitų apie jūsų naudojamas išlaidas ataskaitoms.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Tiekėjo SF įsigijimo kategorijų naudojimo privalumai

Kai kurie tiekėjų SF įsigijimo kategorijų naudojimo privalumai:

- Nuosekli vartotojų patirtis: konfigūruojant visų su pirkimo užsakymu susijusių išlaidų įsigijimo kategorijas **,** vartotojai gali būti kuriami viename SF išrašymo procese, naudojant laukiančių tiekėjo SF puslapį.
- Patobulinta ataskaitų pateikimo patirtis: konfigūruojant visų prekių ir visų su pirkimo užsakymu susijusių išlaidų įsigijimo kategorijas, įsigijimo išlaidų ataskaitoje bus analizuojamos išlaidos pagal tiekėją, kategoriją ir kt.
- Nuosekli darbo eiga: kai **visoms** SF apdoroti naudojate laukiančias tiekėjo SF, galite sukurti nuoseklią darbo eigą ir patvirtinimo procesą naudodami vieną darbo eigą.

## <a name="consignment-inventory-posting"></a>Konsignacijos atsargų registravimas

Konsignacijos atsargos naudoja tą patį DK registravimą kaip ir kitos nupirktos prekės. Pagrindinis skirtumas yra tas, kad kai gaunamas atsargų, DK operacijos neįrašomos. Nuosavybės perdavimui į organizaciją užregistravimo **atsargų** nuosavybės pakeitimo žurnalas, generuojamas kvitas, skirtas įrašyti prekės išlaidas. Norėdami gauti daugiau informacijos, eikite į [Nustatyti konsigną](/supply-chain/inventory/consignment.md).
