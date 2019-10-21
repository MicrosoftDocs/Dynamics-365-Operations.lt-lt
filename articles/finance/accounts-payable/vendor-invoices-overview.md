---
title: Tiekėjų sąskaitų faktūrų apžvalga
description: Šioje temoje pateikiama bendra informacija apie tiekėjo SF. Tiekėjo SF yra mokėjimo už gautus produktus ir paslaugas užklausos. Tiekėjo SF gali būti atitikti sąskaitą už vykdomas paslaugas, arba jos gali būti pagrįstos konkrečių prekių ir paslaugų pirkimo užsakymais.
author: abruer
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c69291214796847af7169cf261865860998f0d27
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189320"
---
# <a name="vendor-invoices-overview"></a>Tiekėjų sąskaitų faktūrų apžvalga

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šioje temoje pateikiama bendra informacija apie tiekėjo SF. Tiekėjo SF yra mokėjimo už gautus produktus ir paslaugas užklausos. Tiekėjo SF gali būti atitikti sąskaitą už vykdomas paslaugas, arba jos gali būti pagrįstos konkrečių prekių ir paslaugų pirkimo užsakymais.

## <a name="vendor-invoices"></a>Tiekėjo SF

Tiekėjo SF iš pirkimo užsakymo yra SF, sukuriama, kai pagal pirkimo užsakymą, pateiktą tiekėjui, gaunami produktai ar paslaugos. Tiekėjo SF yra antraštė ir viena arba kelios prekių arba paslaugų eilutės. Tiekėjo SF užbaigia ciklą, prasidedantį pirkimo užsakymu ir pasibaigiantį produktų gavimu bei tiekėjo SF išrašymu.

Nors kai kurios tiekėjo SF yra susijusios su pirkimo užsakymu, jose taip pat gali būti eilučių, kurios neatitinka pirkimo užsakymo eilučių. Taip pat galite kurti tiekėjo SF, kurios nėra susijusios su jokiu pirkimo užsakymu. Šios tiekėjo SF gali būti naudojamos nuolatinėms paslaugoms, pvz., sąskaitai už komunalines paslaugas, ir, jas pridedant, nereikia nurodyti į pirkimo užsakymą.

Įvesti tiekėjo SF galima keliais toliau nurodytais būdais.

- Naudojant tiekėjo SF registrą galima greitai įvesti pirkimo užsakymo nenurodančias SF – tuomet bus galima kaupti išlaidas. Naudojant tiekėjo SF patvirtinimo žurnalą galima pasirinkti tokias SF ir jas užregistruoti tiekėjo balanse, kad būtų anuliuotos sukauptos sumos.
- Tiekėjo SF žurnalas leidžia greitai vienu veiksmu įvesti SF, kurios nenurodo į pirkimo užsakymą.
- Kartu su tiekėjo SF telkiniu tiekėjo SF registras leidžia greitai įvesti SF, kad būtų galima kaupti išlaidas. Susietus pirkimo užsakymus galite atidaryti vėliau ir SF registruoti pagal išlaidų sąskaitą.
- **Atidarytų tiekėjo SF** ir **Laukiančių tiekėjo SF** puslapiuose tiekėjo SF galima kurti iš patvirtintų pirkimo užsakymų.

Toliau pateikiamame aptarime pateikiama daugiau informacijos apie tai, kaip naudoti **Atidarytų tiekėjo SF** arba **Laukiančių tiekėjo SF** puslapį norint tiekėjo SF kurti iš pirkimo užsakymo.

## <a name="understanding-invoice-line-quantities"></a>SF eilučių kiekių supratimas

Kai tiekėjo SF atidarote iš susijusio pirkimo užsakymo, SF eilutės kuriamos iš pirkimo užsakymo. Pagal numatytąsias nuostatas kiekiai paimami iš produkto gavimo kvito kiekio. Tačiau galite naudoti bet kurią iš toliau nurodytų numatytųjų veiksenų.

- **Dabartinio gavimo kiekis** – šią parinktį naudokite dalinėms siuntoms. Numatytoji lauke **Kiekis** nurodyta reikšmė paimama iš pirkimo užsakymo lauke **Gauti dabar** nurodyto kiekio.
- **Užsakytas kiekis** – šią parinktį naudokite baigtoms siuntoms. Numatytoji lauke **Kiekis** nurodyta reikšmė paimama iš pirkimo užsakymo lauke **Užsakyta** nurodyto kiekio.
- **Užregistruotas kiekis** – šią parinktį naudokite, jei prekę reikia registruoti, kaip nurodyta **Prekių modelių grupių** puslapyje. Numatytoji reikšmė lauke **Kiekis** yra fizinis užregistruotas naujinimo kiekis.
- **Produkto gavimo kvito kiekis** – šią parinktį naudokite, jei jau gautas užsakymo produkto gavimo kvitas. Numatytoji reikšmė lauke **Kiekis** paimama iš viso galimų produktų gavimo kvitų kiekio.
- **Užregistruotas kiekis ir paslaugos** – šią parinktį naudokite, jei gavimo žurnaluose užregistruoti atsargose laikomų arba nelaikomų prekių kiekiai. Ši parinktis taip pat apima paslaugas, nepaisant, ar jos užregistruotos.

Jei jūsų juridinis subjektas naudoja SF gretinimą, kiekio gretinimo rezultatus galite peržiūrėti **Produkto gavimo kvito kiekio gretinimo** stulpelyje. Norėdami peržiūrėti kiekio gretinimo rezultatus, taip pat galite naudoti mygtuką **Gretinimo informacija**, esantį veiksmų srities skirtuke **Peržiūra**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Eilutės, kurios nebuvo pirkimo užsakyme, pridėjimas

Į tiekėjo SF galite įtraukti eilutę, kurios nebuvo pirkimo užsakyme. Turite pasirinkti prekės numerį arba įsigijimo kategoriją. Tada į eilutę galite pridėti kiekius, kainas ir sumas. Eilutė bus įtraukta tik į bendrųjų SF sumų gretinimo strategijas.

## <a name="submitting-a-vendor-invoice-for-review"></a>Tiekėjo SF pateikimas peržiūrai

Jūsų organizacija gali naudoti darbo eigas, kad galėtų valdyti tiekėjų SF peržiūros procesą. Darbo eigos peržiūros gali būti reikalaujama sąskaitos faktūros antraštei, sąskaitos faktūros eilutei arba abiem. Darbo eigos valdikliai taikomi antraštei arba eilutei, tai priklauso nuo židinio vietos pasirenkant valdiklį. Vietoj mygtuko **Registruoti** matysite mygtuką **Pateikti**, kurį galite naudoti siųsti tiekėjo SF pro peržiūros procesą.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Tiekėjo SF ir produkto gavimo kvitų gretinimas

Galite įvesti ir įrašyti informaciją apie tiekėjo SF, taip pat galite gretinti sąskaitų faktūrų eilutes su produkto gavimo kvitų eilutėmis. Taip pat galite gretinti dalinius eilutės kiekius.

Galite sukurti tiekėjo SF, kuri paremta produkto gavimo kvito eilutės prekėmis, kurios gautos iki nurodytos dienos, net jei gautos dar ne visos konkretaus pirkimo užsakymo prekės. Pavyzdžiui, šią parinktį galite naudoti, jei tiekėjas siunčia vieną SF per mėnesį, apimančią visus per mėnesį jo išsiųstus pristatymus. Kiekvienas produkto gavimo kvitas parodo dalinį arba visą prekių pristatymą pagal pirkimo užsakymą.

Kai registruojate SF, kiekvienos prekės **SF likučio** kiekis atnaujinamas visu gautu kiekiu iš pasirinktų produkto gavimo kvitų. Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pirkimo užsakyme yra 0 (nulis), pirkimo užsakymo būsena pakeičiama į **SF išrašyta**. Jeigu **SF likučio** kiekis nėra 0, pirkimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF.

Pasirenkant šią parinktį tariama, kad pirkimo užsakymui užregistruotas bent vienas produkto gavimo kvitas. Tiekimo SF remiasi šiais produktų gavimo kvitais ir atspindi kiekius iš jų. SF finansinė informacija yra paremta informacija, įvesta jums registruojant SF.

Daugiau informacijos žr. [Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="working-with-multiple-invoices"></a>Darbas su keliomis SF

Vienu metu galite dirbti su keliomis sąskaitomis faktūromis ir registruoti jas visas vienu metu. Jei turite sukurti kelias SF, naudokite **Laukiančių tiekėjo SF** puslapį. Jei turite registruoti ir spausdinti kelias tiekėjo SF, naudokite SF patvirtinimo žurnalą. Jei naudojate SF patvirtinimo žurnalą, turi būti registruotas bent vienas pirkimo užsakymo produkto gavimo kvitas, o pirkimo SF turi būti registruota SF registre. SF finansinė informacija gaunama iš SF, kuri buvo užregistruota registre.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Naudojamų tiekėjo SF atkūrimas

Kai tiekėjo SF naudojama, jos negali redaguoti kitas vartotojas. Tačiau kartais SF būsena gali nurodyti, kad SF yra naudojama, net jei ji nėra aktyviai redaguojama. Pvz., programa galėjo nustoti reaguoti į komandas, kai SF buvo redaguojama, arba vartotojas galėjo netyčia palikti SF atidarytą programoje.

Galite naudoti puslapį **Tiekėjo SF atkūrimas**, kad atkurtumėte arba išleistumėte tiekėjo SF, kurios buvo naudojamos daugiau nei keturias valandas, kad jas būtų galima redaguoti. Šį puslapį galite atidaryti naršymo skiltyje **Periodinė užduotis** arba darbo srities **Tiekėjo SF įrašas** plytelėje. Atkūrus SF, ją bus galima redaguoti puslapyje **Tiekėjo SF**.

Puslapį **Tiekėjo SF atkūrimas** galite pasiekti tik tada, jei jums priskirta saugumo pareiga ir teisė **Atkurti naudojamas tiekėjo SF**. Be to, reikia įjungti parametrą **Leisti tiekėjo SF atkūrimą**, esantį puslapyje **Mokėtinų sumų parametrai**.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Tiekėjo SF darbo eigos būsenos nustatymas iš naujo iš Nesusigrąžinamos sumos į Juodraštis

Bus nurodyta darbo eigos egzemplioriaus, kuris buvo sustabdytas dėl neištaisomos klaidos, būsena **Neištaisoma**. Kai tiekėjo SF darbo eigos būsena **Nepataisoma**, ją galima nustatyti iš naujo **Juodraštis** nurodant **Atšaukti**. Tada galite redaguoti tiekėjo SF. Šią funkciją galima naudoti, jei įjungtas puslapio **Funkcijų valdymas** parametras **Tiekėjo SF darbo eigos juodraščio būsenos nustatymas iš naujo**.

Naudodamiesi puslapiu **Tiekėjo SF darbo eigos būsenos nustatymas iš naujo** galite iš naujo nustatyti darbo eigos būseną **Juodraštis**. Šį puslapį galite atidaryti iš **Tiekėjo SF** arba **Bendra > Užklausos > Darbo eiga**. Norėdami iš naujo nustatyti darbo eigos būseną į **Juodraštis**, pasirinkite **Atšaukti**. Taip pat galite iš naujo nustatyti darbo eigos būseną į „Juodraštis“, pasirinkdami veiksmą **Atšaukti** puslapyje **Tiekėjo SF** arba **Laukiančios tiekėjo SF**. Iš naujo nustačius darbo eigos būseną **Juodraštis**, ją galima redaguoti puslapyje **Tiekėjo SF**.



## <a name="additional-resources"></a>Papildomi ištekliai

- [Tiekėjų sąskaitų faktūrų strategijų nustatymas](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Pagrindiniai SF duomenys apie mokėtinas sumas naudojant tiekėjo SF](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Pagrindiniai SF duomenys mokėtinose sumose naudojant patvirtinimo žurnalą](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Pagrindiniai SF duomenys AP sistemoje naudojant SF telkinį](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Įrašyti tiekėjo SF į SF žurnalą](tasks/record-vendor-invoice-invoice-journal.md)
