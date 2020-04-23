---
title: Ieškoti produktų ir produkto variantų įvedant užsakymą
description: Norėdami ieškoti produktų ir produktų variantų, kai rankiniu būdu sukuriate pardavimo užsakymą arba pardavimo užsakymo eilutę, naudokite lauką **Prekės numeris**. Taip galite greitai rasti produkto variantus, kai turite tik konfigūracijos eilutę arba vieną iš galimų produkto dimensijų.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 15a6439595174978e379aaf248cd565bdf636428
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209426"
---
# <a name="search-for-products-and-product-variants-during-order-entry"></a>Ieškoti produktų ir produkto variantų įvedant užsakymą

[!include [banner](../includes/banner.md)]

Norėdami ieškoti produktų ir produktų variantų, kai rankiniu būdu sukuriate pardavimo užsakymą arba pardavimo užsakymo eilutę, naudokite lauką **Prekės numeris**.  Taip galite greitai rasti produkto variantus, kai turite tik konfigūracijos eilutę arba vieną iš galimų produkto dimensijų.

Kartais turėti ko nors per daug nėra geriausia situacija, kurioje norėtum atsidurti, ir tai ypač teisinga tais atvejais, kai parduodate kelis panašius produktus, ir bandote prisiminti prekių numerius arba produkto paieškos pavadinimus, kad galėtumėte rasti pardavimo užsakymui tinkamiausią produktą.Kaip paieškos lauką galite naudoti pardavimo užsakymo eilutės arba pirkimo užsakymo eilutės lauką **Prekės numeris**. Galite įvesti bet kurią produkto pavadinimo dalį, numerį ar dimensiją ir gauti peržvalgą, kurioje rodomos visos paieškos žodį atitinkančios prekės.

## <a name="how-searchworks"></a>Kaip veikia paieška
Kai ieškote produktų ar produkto variantų, svarbu suprasti, kaip paieškos funkcija randa produktus, kurie atitinka jūsų įvestą tekstą. Pagrindinės paieškos rezultatų pateikimo taisyklės yra šios:

-   Paieškos rezultatuose pateikiami visi kriterijus atitinkantys įrašai, nepriklausomai nuo to, kuriame lauke įvedamas paieškos tekstas.
-   Paieškos kriterijus atitinkančiame įraše turi būti visas paieškos tekstas.
-   Atitikimas rodomas net tais atvejais, kai paieškos tekstas randamas paieškos kriterijus atitinkančio įrašo teksto eilutės viduryje. Jis nebūtinai turi būti teksto eilutės pradžioje.
-   Paieškos tekstas laikomas viena teksto eilute, net jei jame yra tarpų.

### <a name="examples"></a>Pavyzdžiai

Toliau pateikiamuose pavyzdžiuose naudojami produktai ir produktų variantai, kad būtų galima iliustruoti, kaip paieška atliekama įvairiuose scenarijuose. **Būtinoji sąlyga:** dalyje **Pardavimas ir rinkodara &gt; Sąranka &gt; Paieška &gt; Paieškos parametrai &gt; Paieškos tipas** pažymėkite parinktį  **Visiška atitiktis**.

| Produkto tipas     | Produkto pavadinimas    | Rodyti produkto numerį | Prekės Nr. | Konfigūravimas |
|------------------|-----------------|------------------------|-------------|---------------|
| Išskirtasis produktas | SpeakerMidRange | D0001                  | D0001       | NA            |
| Produkto variantas  | Aktyvusis garsiakalbis  | D0010:::Juoda:         | D0010       | 000005        |
| Produkto variantas  | Aktyvusis garsiakalbis  | D0010:::Balta:         | D0010       | Balta         |

Jei lauke **Prekės numeris** įvesite „kalbėti“, paieškos rezultatuose pamatysite visus pirmiau išvardytus produktus. Jeigu lauke **Prekės numeris** įvesite „juoda“, rezultatuose pamatysite antrą produktą, nes jo rodomame produkto numeryje yra žodis „juoda“. Šiuose dviejuose pavyzdžiuose parodoma, kad paieška atliekama ne tik lauko pradžioje, atitikimas rodomas net ir tais atvejais, kai paieškos tekstas randamas paieškos kriterijus atitinkančio įrašo teksto eilutės viduryje.  

Įvedus „05“ kaip rezultatas gaunamas tik antras produkto variantas, nes jo konfigūracijoje nurodytas skaičius „05“. Tai parodo, kad paieška veikia visuose įgalintuose puslapio **Paieškos kriterijai** laukuose.  

Jeigu įvesite „ištarti 05“, jokių rezultatų negausite. Taip yra todėl, kad vykstant paieškai ieškoma viso įvesto teksto. Paieška nebandys surasti žodį „ištarti“, o po to susiaurinti rezultatus pateikiant tik tuos, kuriuose yra skaičius „05“.  

Galite apriboti paieškos rezultatų skaičių puslapyje **Pardavimas ir rinkodara &gt; Sąranka &gt; Paieška &gt; Paieškos parametrai** naudodami lauką **Rezultatų skaičius**. Jei nustatyta šio lauko nuostata 0, pateikiami visi paieškos rezultatai. Jei nustatote šio lauko nuostatą, pavyzdžiui, 10, pateikiama ne daugiau negu 10 paieškos rezultatų.

## <a name="configure-the-productsearch"></a>Produktų paieškos konfigūravimas
Prieš naudodami produkto ir produkto variantų paieškos funkciją, atlikite toliau nurodytus veiksmus, kad sukonfigūruotimėte produktų paiešką. [![3 veiksmai norint sukonfigūruoti produkto paiešką\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>1 veiksmas: į paieškos kriterijus įtraukite visus atitinkamus produkto ir produkto variantų identifikatorius ir dimensijas

Produkto ir produkto varianto identifikatorių ir dimensijų, pagal kurias galite ieškoti, pavyzdžiai:  **Produkto pavadinimas, prekės numeris**, **Rodyti produkto numerį, konfigūraciją, spalvą, dydį, stilių, paieškos pavadinimą ir t. t**.  

Eikite į puslapį **Pardavimas ir rinkodara &gt; Sąranka &gt; Paieška &gt; Paieškos kriterijai**. Puslapyje **Paieškos kriterijai** galite nurodyti kliento, potencialaus kliento ir produkto paieškos kriterijus. Būtinai filtruokite puslapį naudodami produkto paieškos kriterijus. Tai galite atlikti įjungdami puslapio meniu dalį **Produktas**.  

Norėdami į paieškos kriterijus įtraukti rodomą produkto numerį, puslapio meniu spustelėkite **Naujas**. Taip į tinklelį **Paieškos kriterijai** bus įtrauktas naujas įrašas. Atidarykite stulpelio **Lauko pavadinimas** peržvalgą ir pasirinkite **DisplayProductNumber**. Norėdami į paieškos kriterijus įtraukti produkto konfigūraciją, tinklelyje **Paieškos kriterijai** sukurkite naują įrašą ir stulpelyje **Lauko pavadinimas** pasirinkite **configId**. Tuo pačiu būdu sukurkite įrašą, kurio **Lauko pavadinimas** **InventColorId**, skirtą spalvos dimensijai, **InventSizeId**, skirtą dydžio dimensijai, ir **InventStyleId**, skirtą stiliaus dimensijai.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>2 veiksmas: automatiškai užpildykite produkto paieškoje naudojamą duomenų bazės lentelę

Puslapyje **Paieškos kriterijai** spustelėkite mygtuką **Atnaujinti paieškos duomenis**. Dialogo lange **Atnaujinti paieškos duomenis** įsitikinkite, kad nustatyta parinkties  **Šaltinis** nuostata **Produktas**, ir spustelėkite **Gerai**. Sistema į vieną lentelę sujungs visus 1 veiksmu nurodytus paieškos kriterijus. Jei turite daug produktų ir produktų variantų, ši operacija gali gana ilgai užtrukti ir galite gauti įspėjimą. Rekomenduojame suplanuoti paieškos lentelės automatinį užpildymą paketinio apdorojimo serveryje tada, kai serveris ne per daug užimtas.  

Kol lentelė nebus automatiškai užpildyta, produkto paieška nepateiks teisingų rezultatų. Jei negaunate jokių paieškos rezultatų, patikrinkite, ar ši lentelė užpildyta.  

Lentelė turi būti užpildyta tik tada, kai modifikuojami paieškos kriterijai. Naujai išleisti produktai ir jų variantai automatiškai įtraukiami į lentelę. Panaikinti produktai ir jų variantai automatiškai pašalinami iš lentelės.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>3 žingsnis: įgalinkite produkto paieškos pardavimo ir pirkimo užsakymo eilutėse peržvalgą

Galite įgalinti šią funkciją, nuėję į **Pardavimas ir rinkodara &gt; Sąranka &gt; Paieška &gt; Paieškos parametrai** ir nustatydami parinkties **Įjungti paieškos peržvalgą** į **Taip** skirtuke **Bendroji informacija**.  

Įvedant pardavimo užsakymo eilutę numatytoji elgsena yra pradėjus pildyti lauką  **Prekės numeris** atidaryti puslapį **Produkto paieška** ir paspausti klavišą  **Tab**. Kuriant užsakymo eilutę pasikeičia puslapio **Produkto paieška** kontekstas ir jis gali būti laikomas nepageidaujamu. Jei norite gauti paieškos rezultatus peržvalgoje ir neprarasti konteksto įvesdami užsakymo eilutę, galite naudoti paieškos peržvalgą. Jei ieškote produkto arba produkto varianto, bet peržvalgoje nieko nepasirenkate ir paspaudžiate klavišą **Skirtukas**, bus rodomas puslapis **Produkto paieška**.



