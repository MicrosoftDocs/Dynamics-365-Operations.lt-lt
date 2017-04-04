---
title: "Ieškoti produktų ir produkto variantų įvedant užsakymą"
description: "Norėdami ieškoti produktų ir produktų variantų, kai rankiniu būdu sukuriate pardavimo užsakymą arba pardavimo užsakymo eilutę, naudokite lauką <strong>Prekės numeris </strong>.  Taip galite greitai rasti produkto variantus, kai turite tik konfigūracijos eilutę arba vieną iš galimų produkto dimensijų."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5b0f3c1a853f8f5e61dedaf588b6f9d2da3a53b5
ms.lasthandoff: 03/31/2017


---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Ieškoti produktų ir produkto variantų įvedant užsakymą

Norėdami ieškoti produktų ir produktų variantų, kai rankiniu būdu sukuriate pardavimo užsakymą arba pardavimo užsakymo eilutę, naudokite lauką <strong>Prekės numeris </strong>.  Taip galite greitai rasti produkto variantus, kai turite tik konfigūracijos eilutę arba vieną iš galimų produkto dimensijų.

Kartais, turintys per daug kažko nėra geriausia padėtis turi būti, ir tai ypač aktualu, jei jūs parduodate nemažai produktų, kurie yra panašūs, ir norite prisiminti prekių numerius arba produkto paieškos pavadinimas, siekiant rasti tinkamą produktą dėti į pardavimų užsakymą. Galite naudoti su **prekės numeris** lauko pardavimo arba pirkimo užsakymo eilutės kaip paieškos laukas. Galite įvesti bet kurią produkto pavadinimo dalį, numerį ar dimensiją ir gauti peržvalgą, kurioje rodomos visos paieškos žodį atitinkančios prekės.

## <a name="how-search-works"></a>Kaip veikia paieška
Kai ieškote produktų ar produkto variantų, svarbu suprasti, kaip paieškos funkcija randa produktus, kurie atitinka jūsų įvestą tekstą. Pagrindinės paieškos rezultatų pateikimo taisyklės yra šios:

-   Paieškos rezultatuose pateikiami visi kriterijus atitinkantys įrašai, nepriklausomai nuo to, kuriame lauke įvedamas paieškos tekstas.
-   Paieškos kriterijus atitinkančiame įraše turi būti visas paieškos tekstas.
-   Atitikimas rodomas net tais atvejais, kai paieškos tekstas randamas paieškos kriterijus atitinkančio įrašo teksto eilutės viduryje. Jis nebūtinai turi būti teksto eilutės pradžioje.
-   Paieškos tekstas laikomas viena teksto eilute, net jei jame yra tarpų.

### <a name="examples"></a>Pavyzdžiai

Toliau pateikiamuose pavyzdžiuose naudojami produktai ir produktų variantai, kad būtų galima iliustruoti, kaip paieška atliekama įvairiuose scenarijuose. **Būtina sąlyga:** pagal **pardavimo ir rinkodaros &gt;nustatymo &gt;paieškos &gt;paieškos parametrus**&gt;**ieškoti tipo**, pasirinkite į **visišku atitikmeniu** variantas.

| Produkto tipas     | Produkto pavadinimas    | Rodyti produkto numerį | Prekės Nr. | Konfigūravimas |
|------------------|-----------------|------------------------|-------------|---------------|
| Išskirtasis produktas | SpeakerMidRange | D0001                  | D0001       | NA            |
| Produkto variantas  | Aktyvusis garsiakalbis  | D0010:::Juoda:         | D0010       | 000005        |
| Produkto variantas  | Aktyvusis garsiakalbis  | D0010:::Balta:         | D0010       | Balta         |

Jei lauke **Prekės numeris** įvesite „kalbėti“, paieškos rezultatuose pamatysite visus pirmiau išvardytus produktus. Jeigu lauke **Prekės numeris** įvesite „juoda“, rezultatuose pamatysite antrą produktą, nes jo rodomame produkto numeryje yra žodis „juoda“. Šiuose dviejuose pavyzdžiuose parodoma, kad paieška atliekama ne tik lauko pradžioje, atitikimas rodomas net ir tais atvejais, kai paieškos tekstas randamas paieškos kriterijus atitinkančio įrašo teksto eilutės viduryje.  

Įvedus „05“ kaip rezultatas gaunamas tik antras produkto variantas, nes jo konfigūracijoje nurodytas skaičius „05“. Tai parodo, kad paieška veikia visuose įgalintuose puslapio **Paieškos kriterijai** laukuose.  

Jeigu įvesite „ištarti 05“, jokių rezultatų negausite. Taip yra todėl, kad vykstant paieškai ieškoma viso įvesto teksto. Paieška nebandys surasti žodį „ištarti“, o po to susiaurinti rezultatus pateikiant tik tuos, kuriuose yra skaičius „05“.  

Galite apriboti paieškos rezultatų skaičius naudojant į **rezultatų skaičius** lauko ir **pardavimo ir rinkodaros &gt;nustatymo &gt;paieškos &gt;paieškos parametrus** puslapis. Jei nustatyta šio lauko nuostata 0, pateikiami visi paieškos rezultatai. Jei nustatote šio lauko nuostatą, pavyzdžiui, 10, pateikiama ne daugiau negu 10 paieškos rezultatų.

## <a name="configure-the-product-search"></a>Produktų paieškos konfigūravimas
Prieš naudodami produkto ir produkto variantų paieškos funkciją, atlikite toliau nurodytus veiksmus, kad sukonfigūruotimėte produktų paiešką. [![3 veiksmus, kaip konfigūruoti produktų paieškos\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>1 veiksmas: į paieškos kriterijus įtraukite visus atitinkamus produkto ir produkto variantų identifikatorius ir dimensijas

Produkto ir produkto varianto identifikatorių ir dimensijų, pagal kurias galite ieškoti, pavyzdžiai: **Produkto pavadinimas, prekės numeris**, **Rodyti produkto numerį, konfigūraciją, spalvą, dydį, stilių, paieškos pavadinimą ir t. t.**.  

Eikite į **pardavimo ir rinkodaros &gt;nustatymo &gt;paieškos &gt;paieškos kriterijus** puslapis. Puslapyje **Paieškos kriterijai** galite nurodyti kliento, potencialaus kliento ir produkto paieškos kriterijus. Būtinai filtruokite puslapį naudodami produkto paieškos kriterijus. Tai galite atlikti įjungdami puslapio meniu dalį **Produktas**.  

Norėdami įtraukti rodymo produkto numerį į paieškos kriterijus, spustelėkite **naujas** puslapio meniu. Tai bus pridėti naują įrašą, kad **paieškos kriterijus** tinklelį. Atidarykite stulpelio **Lauko pavadinimas** peržvalgą ir pasirinkite **DisplayProductNumber**. Pridėti produkto konfigūracijos paieškos kriterijų, sukurti naują įrašą į ** paieškos kriterijus ** tinklelį ir pasirinko **configId**, į **lauko pavadinimas** stulpelio. Tuo pačiu būdu sukurkite įrašą, kurio **Lauko pavadinimas** **InventColorId**, skirtą spalvos dimensijai, **InventSizeId**, skirtą dydžio dimensijai, ir **InventStyleId**, skirtą stiliaus dimensijai.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>2 veiksmas: automatiškai užpildykite produkto paieškoje naudojamą duomenų bazės lentelę

Puslapyje **Paieškos kriterijai** spustelėkite mygtuką **Atnaujinti paieškos duomenis**. Dialogo lange **Atnaujinti paieškos duomenis** įsitikinkite, kad nustatyta parinkties **Šaltinis** nuostata **Produktas**, ir spustelėkite **Gerai**. Sistema bus kaupti vienoje lentelėje 1 veiksme nurodytą pasirinktus paieškos kriterijus. Jei turite daug produktų ir prekių dimensijų kombinacijoje, ši operacija gali būti gana ilgas ir gali būti parodytas įspėjimas. Rekomenduojame suplanuoti paieškos lentelės automatinį užpildymą paketinio apdorojimo serveryje tada, kai serveris ne per daug užimtas.  

Kol lentelė nebus automatiškai užpildyta, produkto paieška nepateiks teisingų rezultatų. Jei negaunate jokių paieškos rezultatų, patikrinkite, ar ši lentelė užpildyta.  

Lentelė turi būti užpildyta tik tada, kai modifikuojami paieškos kriterijai. Naujai išleisti produktai ir jų variantai automatiškai įtraukiami į lentelę. Panaikinti produktai ir jų variantai automatiškai pašalinami iš lentelės.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>3 žingsnis: įgalinkite produkto paieškos pardavimo ir pirkimo užsakymo eilutėse peržvalgą

Galite įgalinti šią funkciją, eikite į **pardavimo ir rinkodaros &gt;sąrankos &gt;paieškos &gt;paieškos parametrus** ir **įgalinti peržvalgos paieškos** į **taip** ant, **bendrojo** tab.  

Įvedant pardavimo užsakymo eilutę numatytoji elgsena yra pradėjus pildyti lauką **Prekės numeris** atidaryti puslapį **Produkto paieška** ir paspausti klavišą **Skirtuką**. Kuriant užsakymo eilutę pasikeičia puslapio **Produkto paieška** kontekstas ir jis gali būti laikomas nepageidaujamu. Jei norite gauti paieškos rezultatus peržvalgoje ir neprarasti konteksto įvesdami užsakymo eilutę, galite naudoti paieškos peržvalgą. Jei ieškote produkto arba produkto varianto, bet peržvalgoje nieko nepasirenkate ir paspaudžiate klavišą **Skirtukas**, bus rodomas puslapis **Produkto paieška**.


