---
title: Tiekėjų sąskaitų faktūrų apžvalga
description: Šioje temoje pateikiama bendra informacija apie tiekėjo SF.
author: abruer
manager: AnnBe
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0299eb3470f500bf469c3367f1c426715067a5dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993321"
---
# <a name="vendor-invoices-overview"></a>Tiekėjų sąskaitų faktūrų apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama bendra informacija apie tiekėjo SF. Tiekėjo sąskaitos yra užklausas gautiems mokėjimams produktams ir paslaugoms. Tiekėjo sąskaitos gali rodyti sąskaitą esamoms paslaugoms arba gali būti paremtos pirkimo užsakymais konkrečioms prekėms ir paslaugoms.

## <a name="vendor-invoices"></a>Tiekėjo SF

Pardavėjo sąskaita pirkimo užsakyme yra sukuriama, kai prekės ir paslaugos gautos pagal pirkimo užsakymą padarytą su tiekėju. Tiekėjo SF yra antraštė ir viena arba kelios prekių arba paslaugų eilutės. Tiekėjo SF užbaigia ciklą, prasidedantį pirkimo užsakymu ir pasibaigiantį produktų gavimu bei tiekėjo SF išrašymu.

Nepaisant to, kad kai kurios tiekėjo sąskaitos susijusios su pirkimo užsakymu, tiekėjo sąskaitose taip pat yra eilučių neatitinkančių pirkimo užsakymo eilučių. Taip pat galite kurti tiekėjo SF, kurios nėra susijusios su jokiu pirkimo užsakymu. Šios tiekėjo sąskaitos gali rodyti esančias paslaugas, tokias kaip komunaliniai mokesčiai. Neturite nurodyti į pirkimo užsakymą įtraukdami esamas paslaugas.

Įvesti tiekėjo SF galima keliais toliau nurodytais būdais.

- Naudojant tiekėjo SF registrą galima greitai įvesti pirkimo užsakymo nenurodančias SF – tuomet bus galima kaupti išlaidas. Naudojant tiekėjo SF patvirtinimo žurnalą galima pasirinkti tokias SF ir jas užregistruoti tiekėjo balanse, kad būtų anuliuotos sukauptos sumos.
- Tiekėjo SF žurnalas leidžia greitai vienu veiksmu įvesti SF, kurios nenurodo į pirkimo užsakymą.
- Kartu su tiekėjo SF telkiniu tiekėjo SF registras leidžia greitai įvesti SF, kad būtų galima kaupti išlaidas. Susietus pirkimo užsakymus galite atidaryti vėliau ir SF registruoti pagal išlaidų sąskaitą.
- **Atidarytų tiekėjo SF** ir **Laukiančių tiekėjo SF** puslapiuose tiekėjo SF galima kurti iš patvirtintų pirkimo užsakymų.

Toliau pateikiamame aptarime pateikiama daugiau informacijos apie tai, kaip naudoti **Atidarytų tiekėjo SF** arba **Laukiančių tiekėjo SF** puslapį norint tiekėjo SF kurti iš pirkimo užsakymo.

## <a name="understanding-invoice-line-quantities"></a>SF eilučių kiekių supratimas

Jums atvėrus tiekėjo sąskaitą iš susijusio užsakymo, sistema sukuria sąskaitos eilutes iš perkybos užsakymo. Pagal nutylėjimą, sistema paima kiekius iš produkto kvito. Tačiau galite naudoti bet kurią iš toliau nurodytų numatytųjų veiksenų.

- **Dabartinio gavimo kiekis** – šią parinktį naudokite dalinėms siuntoms. Sistema nustato numatytą vertę **Kiekyje** iš kiekio nurodyto **Gauta dabar** laukelyje pirkimo užsakyme.
- **Užsakytas kiekis** – šią parinktį naudokite baigtoms siuntoms. Sistema nustato numatytą vertę **Kiekyje** iš kiekio nurodyto **Užsakyta** laukelyje pirkimo užsakyme.
- **Užregistruotas kiekis** – šią parinktį naudokite, jei prekę reikia registruoti, kaip nurodyta **Prekių modelių grupių** puslapyje. Numatytoji reikšmė lauke **Kiekis** yra fizinis užregistruotas naujinimo kiekis.
- **Produkto gavimo kvito kiekis** – šią parinktį naudokite, jei jau gautas užsakymo produkto gavimo kvitas. Sistema paima numatytąją vertę **Kiekio** laukelyje iš bendro esamų produkto kvitų kiekio.
- **Užregistruotas kiekis ir paslaugos** – šią parinktį naudokite, jei gavimo žurnaluose užregistruoti atsargose laikomų arba nelaikomų prekių kiekiai. Ši parinktis taip pat apima paslaugas, nepaisant, ar jos užregistruotos.

Jei jūsų juridinis subjektas naudoja SF gretinimą, kiekio gretinimo rezultatus galite peržiūrėti **Produkto gavimo kvito kiekio gretinimo** stulpelyje. Norėdami peržiūrėti kiekio gretinimo rezultatus, taip pat galite naudoti mygtuką **Gretinimo informacija**, esantį veiksmų srities skirtuke **Peržiūra**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Eilutės, kurios nebuvo pirkimo užsakyme, pridėjimas

Į tiekėjo SF galite įtraukti eilutę, kurios nebuvo pirkimo užsakyme. Turite pasirinkti prekės numerį arba įsigijimo kategoriją. Tada į eilutę galite pridėti kiekius, kainas ir sumas. Eilutė bus įtraukta tik į bendrųjų SF sumų gretinimo strategijas.

## <a name="submitting-a-vendor-invoice-for-review"></a>Tiekėjo SF pateikimas peržiūrai

Jūsų organizacija gali naudoti darbo eigas, kad galėtų valdyti tiekėjų SF peržiūros procesą. Darbo eigos peržiūros gali būti reikalaujama sąskaitos faktūros antraštei, sąskaitos faktūros eilutei arba abiem. Darbo eigos valdikliai taikomi antraštei arba eilutei, tai priklauso nuo židinio vietos pasirenkant valdiklį. Vietoje **Publikavimo** mygtuko, **Pateikimo** mygtukas rodo nusiųstą tiekėjo sąskaitą per peržiūros procesą.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Apsauga, kad SF nebūtų pateikta į darbo eigą 

Toliau pateikiami keli būdai, kaip galima išvengti SF pateikimo į darbo eigą.

- **Bendroji SF suma ir užregistruota bendroji suma nėra lygios.** Asmuo pateikęs sąskaitą gaus įspėjimą, kad bendros sumos nesutampa. Įspėjime pateikta galimybė taisyti balansus prieš pateikiant sąskaitą į darbo eigą dar kartą. Ši funkcija galima tik tada, kai parametras **Uždrausti pateikti į darbo eigą, kai sąskaitos faktūros ir registruotos sąskaitos faktūros sumos nesutampa** puslapyje **Funkcijų valdymas** yra įjungtas. 

- **SF yra nepriskirtų išlaidų.** Asmuo, kuris pateikė SF, gaus įspėjimą, kad sąskaitoje yra nepriskirtų išlaidų, todėl jis galės pakoreguoti SF prieš pateikdamas ją į darbo eigą. Ši funkcija galima tik tada, kai parametras **Uždrausti pateikti į darbo eigą, kai tiekėjo SF yra nepriskirtų išlaidų** puslapyje **Funkcijų valdymas** yra įjungtas.

- **SF numeris yra toks pats kaip kitos užregistruotos SF.** Asmuo, kuris pateikė SF, gaus įspėjimą, kad rasta sąskaita tokiu pačiu numeriu, todėl jis galės ją pakoreguoti prieš pateikdamas į darbo eigą. Šis pranešimas bus rodomas kai **Tikrinti sąskaitos numerį naudotą** parametras mokėtinose Sąskaitose yra nustatytas **Atmestas dublikatas**. Ši funkcija galima, jei parametras **Drausti pateikimą į darbo eigą, kai SF numerį jau turi kita užregistruota SF, o sistema nenustatyta, kad leistų priimti dubliuotus SF numerius** puslapyje **Funkcijų valdymas** yra įjungtas.  

## <a name="matching-vendor-invoices-to-product-receipts"></a>Tiekėjo SF ir produkto gavimo kvitų gretinimas

Galite įvesti ir įrašyti informaciją apie tiekėjo SF, taip pat galite gretinti sąskaitų faktūrų eilutes su produkto gavimo kvitų eilutėmis. Taip pat galite gretinti dalinius eilutės kiekius.

Galite sukurti tiekėjo SF, kuri paremta produkto gavimo kvito eilutės prekėmis, kurios gautos iki nurodytos dienos, net jei gautos dar ne visos konkretaus pirkimo užsakymo prekės. Pavyzdžiui, šią parinktį galite naudoti, jei tiekėjas siunčia vieną SF per mėnesį, apimančią visus per mėnesį jo išsiųstus pristatymus. Kiekvienas produkto gavimo kvitas parodo dalinį arba visą prekių pristatymą pagal pirkimo užsakymą.

Kai sąskaita yra darbo eigoje, tvirtintojas gali naujinti sąskaitos kiekius taip, kad jie atitiktų vertę **Produkto gautas kiekis atitikmeniui** laukelyje. Tam, kad tą atliktumėte, pasirinkite **Naujinti sąskaitos kiekius, kad jie atitiktų produkto gautus kiekius darbo eigoje** funkciją **Funkcijos valdymas** darbo eigoje ir rinkitės **Įjungti**. Jei patvirtinantis asmuo darbo eigos procese panaikino visus atitikimus nuo produkto gavimo iš sąskaitos eilutės, sąskaitos eilutė bus panaikinta. Jai ši funkcija išjungta, sąskaitos kiekiai nėra naujinami sąskaitoms darbo eigoje.

Kai registruojate SF, kiekvienos prekės **SF likučio** kiekis atnaujinamas visu gautu kiekiu iš pasirinktų produkto gavimo kvitų. Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pirkimo užsakyme yra 0 (nulis), pirkimo užsakymo būsena pakeičiama į **SF išrašyta**. Jeigu **SF likučio** kiekis nėra 0, pirkimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF.

Pasirenkant šią parinktį tariama, kad pirkimo užsakymui užregistruotas bent vienas produkto gavimo kvitas. Tiekimo SF remiasi šiais produktų gavimo kvitais ir atspindi kiekius iš jų. SF finansinė informacija yra paremta informacija, įvesta jums registruojant SF.

Daugiau informacijos žr. [Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Tiekėjo SF darbo eigos automatizuotos užduoties konfigūravimas siekiant užregistruoti tiekėjo SF naudojant paketinę užduotį

Galite pridėti automatizuotą registravimo užduotį prie tiekėjo SF darbo eigos, kad SF būtų apdorotos paketais. SF registravimas paketais leidžia tęsti darbo eigos procesą nelaukiant, kada bus baigtas registravimas, tai pagerina bendrą visų užduočių, pateiktų į darbo eigą, efektyvumą.

Norėdami užregistruoti tiekėjo SF kaip paketą, puslapyje **Funkcijų valdymas** įjunkite parametrą **Tiekėjo SF paketo registravimas**. Tiekėjo SF darbo eigos konfigūruojamos einant į **Mokėtinos sumos > Sąranka > Mokėtinų sumų darbo eigas**.

Užduotį **Registruoti tiekėjo SF naudojant paketą** galite matyti darbo eigos rengyklėje nepaisant to, ar įjungtas parametras **Tiekėjo SF paketo registravimas**. Kai funkcijos parametras neįjungtas, SF, kurioje yra **Registruoti tiekėjo SF naudojant paketines užduotis**, negalima apdoroti darbo eigoje, kol parametras neįjungtas. Užduoties **Registruoti tiekėjo SF naudojant paketą** negalima naudoti toje pačioje darbo eigoje, kurioje yra automatizuota užduotis **Registruoti tiekėjo SF**. Be to, užduotis **Registruojant tiekėjo SF naudojant paketą** turi būti paskutinis elementas darbo eigos konfigūracijoje.

Galite nurodyti, kiek SF turi būti įtraukta į paketą, ir valandų skaičių, kurį reikia laukti prieš perplanuojant paketą, eidami į **Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai > SF > SF darbo eiga**. 

## <a name="working-with-multiple-invoices"></a>Darbas su keliomis SF

Vienu metu galite dirbti su keliomis sąskaitomis faktūromis ir registruoti jas visas vienu metu. Jei turite sukurti kelias SF, naudokite **Laukiančių tiekėjo SF** puslapį. Jei turite registruoti ir spausdinti kelias tiekėjo SF, naudokite SF patvirtinimo žurnalą. Jei naudojate SF patvirtinimo žurnalą, turi būti registruotas bent vienas pirkimo užsakymo produkto gavimo kvitas, o pirkimo SF turi būti registruota SF registre. SF finansinė informacija gaunama iš SF, kuri buvo užregistruota registre.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Naudojamų tiekėjo SF atkūrimas

Kai tiekėjo SF naudojama, jos negali redaguoti kitas vartotojas. Tačiau kartais SF būsena gali nurodyti, kad SF yra naudojama, net jei ji nėra aktyviai redaguojama. Pvz., programa galėjo nustoti reaguoti į komandas, kai SF buvo redaguojama, arba vartotojas galėjo netyčia palikti SF atidarytą programoje.

Galite naudoti puslapį **Tiekėjo SF atkūrimas**, kad atkurtumėte arba išleistumėte tiekėjo SF, kurios buvo naudojamos daugiau nei keturias valandas, kad jas būtų galima redaguoti. Šį puslapį galite atidaryti naršymo skiltyje **Periodinė užduotis** arba darbo srities **Tiekėjo SF įrašas** plytelėje. Atkūrus SF, ją bus galima redaguoti puslapyje **Tiekėjo SF**.

Puslapį **Tiekėjo SF atkūrimas** galite pasiekti tik tada, jei jums priskirta saugumo pareiga ir teisė **Atkurti naudojamas tiekėjo SF**. Be to, reikia įjungti parametrą **Leisti tiekėjo SF atkūrimą**, esantį puslapyje **Mokėtinų sumų parametrai**.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Tiekėjo SF darbo eigos būsenos nustatymas iš naujo iš Nesusigrąžinamos sumos į Juodraštis

Bus nurodyta darbo eigos egzemplioriaus, kuris buvo sustabdytas dėl neištaisomos klaidos, būsena **Neištaisoma**. Kai tiekėjo SF darbo eigos būsena **Nepataisoma**, ją galima nustatyti iš naujo **Juodraštis** nurodant **Atšaukti**. Tada galite redaguoti tiekėjo SF. Šią funkciją galima naudoti, jei įjungtas puslapio **Funkcijų valdymas** parametras **Tiekėjo SF darbo eigos būsenos nustatymas iš naujo iš Nesusigrąžinamos sumos į Juodraštis**.

Naudodamiesi puslapiu **Tiekėjo SF darbo eigos būsenos nustatymas iš naujo** galite iš naujo nustatyti darbo eigos būseną **Juodraštis**. Šį puslapį galite atidaryti iš **Tiekėjo SF** arba **Bendra > Užklausos > Darbo eiga**. Norėdami iš naujo nustatyti darbo eigos būseną į **Juodraštis**, pasirinkite **Atšaukti**. Taip pat galite iš naujo nustatyti darbo eigos būseną į „Juodraštis“, pasirinkdami veiksmą **Atšaukti** puslapyje **Tiekėjo SF** arba **Laukiančios tiekėjo SF**. Iš naujo nustačius darbo eigos būseną **Juodraštis**, ją galima redaguoti puslapyje **Tiekėjo SF**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>SF sumos peržiūra puslapyje Laukiančios tiekėjo SF
SF sumą galite peržiūrėti puslapyje **Laukiančios tiekėjo SF**, įjungdami puslapio **Mokėtinos sumos** parametrą **Laukiančių tiekėjo SF sąraše rodyti bendrą SF sumą**. 



## <a name="additional-resources"></a>Papildomi ištekliai

- [Nustatyti tiekėjų SF strategijas](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Pagrindiniai SF duomenys AP sistemoje naudojant tiekėjo SF](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Pagrindiniai SF duomenys mokėtinose sumose naudojant patvirtinimo žurnalą](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Pagrindiniai SF duomenys AP sistemoje naudojant SF telkinį](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Įrašyti tiekėjo SF į SF žurnalą](tasks/record-vendor-invoice-invoice-journal.md)
