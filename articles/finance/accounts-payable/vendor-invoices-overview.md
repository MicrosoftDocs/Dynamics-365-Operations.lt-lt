---
title: Tiekėjų sąskaitų faktūrų apžvalga
description: Šioje temoje pateikiama bendra informacija apie tiekėjo SF.
author: abruer
ms.date: 02/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b54a60ac3b1868ea7cc5ed88d5a31203b4bd29d3
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358446"
---
# <a name="vendor-invoices-overview"></a>Tiekėjų sąskaitų faktūrų apžvalga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


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

- **Dabartinio gavimo kiekis** – šią parinktį naudokite dalinėms siuntoms. Numatytoji vertė lauke **Kiekis** bus nustatyta kaip pirkimo užsakymo lauke **Gauti dabar** nurodytas kiekis.
- **Užsakytas kiekis** – šią parinktį naudokite baigtoms siuntoms. Numatytoji lauko **Kiekis** vertė bus nustatyta kaip kiekis, nurodytas **pirkimo užsakymo** lauke Užsakyta.
- **Užregistruotas kiekis** – šią parinktį naudokite, jei prekę reikia registruoti, kaip nurodyta **Prekių modelių grupių** puslapyje. Numatytoji reikšmė lauke **Kiekis** yra fizinis užregistruotas naujinimo kiekis.
- **Produkto gavimo kvito kiekis** – šią parinktį naudokite, jei jau gautas užsakymo produkto gavimo kvitas. Numatytoji vertė lauke **Kiekis** yra bendras galimų produkto gavimo kvitų kiekis.
- **Užregistruotas kiekis ir paslaugos** – šią parinktį naudokite, jei gavimo žurnaluose užregistruoti atsargose laikomų arba nelaikomų prekių kiekiai. Ši parinktis taip pat apima paslaugas, nepaisant, ar jos užregistruotos.

Jei jūsų juridinis subjektas naudoja SF gretinimą, kiekio gretinimo rezultatus galite peržiūrėti **Produkto gavimo kvito kiekio gretinimo** stulpelyje. Norėdami peržiūrėti kiekio gretinimo rezultatus, taip pat galite naudoti mygtuką **Gretinimo informacija**, esantį veiksmų srities skirtuke **Peržiūra**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Eilutės, kurios nebuvo pirkimo užsakyme, pridėjimas

Į tiekėjo SF galite įtraukti eilutę, kurios nebuvo pirkimo užsakyme. Turite pasirinkti prekės numerį arba įsigijimo kategoriją. Tada į eilutę galite pridėti kiekius, kainas ir sumas. Eilutė bus įtraukta tik į bendrųjų SF sumų gretinimo strategijas.

## <a name="submitting-a-vendor-invoice-for-review"></a>Tiekėjo SF pateikimas peržiūrai

Jūsų organizacija gali naudoti darbo eigas, kad galėtų valdyti tiekėjų SF peržiūros procesą. Darbo eigos peržiūros gali būti reikalaujama sąskaitos faktūros antraštei, sąskaitos faktūros eilutei arba abiem. Darbo eigos valdikliai taikomi antraštei arba eilutei, tai priklauso nuo židinio vietos pasirenkant valdiklį. Vietoj mygtuko **Registruoti**, pateikimo **mygtukas** siunčia tiekėjo SF peržiūros proceso metu.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Apsauga, kad SF nebūtų pateikta į darbo eigą 

Toliau pateikiami keli būdai, kaip galima išvengti SF pateikimo į darbo eigą.

- **Bendroji SF suma ir užregistruota bendroji suma nėra lygios.** Asmuo pateikęs SF gaus įspėjimą, kad bendros sumos nesutampa. Įspėjime pateikta galimybė taisyti balansus prieš pateikiant sąskaitą į darbo eigą dar kartą. Ši funkcija galima tik tada, kai parametras **Uždrausti pateikti į darbo eigą, kai sąskaitos faktūros ir registruotos sąskaitos faktūros sumos nesutampa** puslapyje **Funkcijų valdymas** yra įjungtas. 
- **SF yra nepriskirtų išlaidų.** Asmuo, kuris pateikė SF, gaus įspėjimą, kad sąskaitoje yra nepriskirtų išlaidų, todėl jis galės pakoreguoti SF prieš pateikdamas ją į darbo eigą. Ši funkcija galima tik tada, kai parametras **Uždrausti pateikti į darbo eigą, kai tiekėjo SF yra nepriskirtų išlaidų** puslapyje **Funkcijų valdymas** yra įjungtas.
- **SF numeris yra toks pats kaip kitos užregistruotos SF.** Asmuo, kuris pateikė sąskaitą faktūrą, gaus pranešimą, nurodantį, kad rasta SF su dublikato numeriu. Dublikato numeris gali būti pataisytas prieš iš naujo pateikiant SF darbo eigai. Šis pranešimas bus rodomas kai **Tikrinti sąskaitos numerį naudotą** parametras mokėtinose Sąskaitose yra nustatytas **Atmestas dublikatas**. Ši funkcija galima, jei parametras **Drausti pateikimą į darbo eigą, kai SF numerį jau turi kita užregistruota SF, o sistema nenustatyta, kad leistų priimti dubliuotus SF numerius** puslapyje **Funkcijų valdymas** yra įjungtas.
- **Sąskaitoje faktūroje yra eilutė, kurioje SF kiekis yra mažesnis nei atitinkamas produkto gavimo kvitų kiekis.** Asmuo, kuris pateikia arba bando registruoti sąskaitą faktūrą, gaus pranešimą, kad kiekiai nėra lygūs. Šis pranešimas suteikia galimybę pataisyti vertes prieš pateikiant sąskaitą į darbo eigą dar kartą. Ši funkcija galima, jei **Tiekėjo sąskaitų faktūrų registravimo ir pateikimo darbo eigai** parametras yra įjungtas **Funkcijų valdymo** puslapyje, o **Registravimo ir pateikimo darbo eigai** parametras įjungtas **Mokėtinų sumų parametrų** puslapyje.

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

Vienu metu galite dirbti su keliomis sąskaitomis faktūromis ir registruoti jas visas vienu metu. Jei turite sukurti kelias SF, naudokite **Laukiančių tiekėjo SF** puslapį. Jeigu turite užregistruoti ir išspausdinti kelias tiekėjo SF, naudokite SF **patvirtinimo žurnalą**. Jei naudojate SF patvirtinimo **žurnalą**, turi būti užregistruotas bent vienas pirkimo užsakymo produkto gavimo kvitas, o pirkimo užsakymo SF turi būti užregistruota SF registre. SF finansinė informacija gaunama iš SF, kuri buvo užregistruota registre.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Naudojamų tiekėjo SF atkūrimas

Kai tiekėjo SF naudojama, jos negali redaguoti kitas vartotojas. Tačiau kartais SF būsena gali nurodyti, kad SF yra naudojama, net jei ji nėra aktyviai redaguojama. Pvz., programa galėjo nustoti reaguoti į komandas, kai SF buvo redaguojama, arba vartotojas galėjo netyčia palikti SF atidarytą programoje.

Galite naudoti puslapį **Tiekėjo SF atkūrimas**, kad atkurtumėte arba išleistumėte tiekėjo SF, kurios buvo naudojamos daugiau nei keturias valandas, kad jas būtų galima redaguoti. Šį puslapį galite atidaryti naršymo skiltyje **Periodinė užduotis** arba darbo srities **Tiekėjo SF įrašas** plytelėje. Atkūrus SF, ją bus galima redaguoti puslapyje **Tiekėjo SF**.

Puslapį **Tiekėjo SF atkūrimas** galite pasiekti tik tada, jei jums priskirta saugumo pareiga ir teisė **Atkurti naudojamas tiekėjo SF**. Be to, reikia įjungti parametrą **Leisti tiekėjo SF atkūrimą**, esantį puslapyje **Mokėtinų sumų parametrai**.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Tiekėjo SF darbo eigos būsenos nustatymas iš naujo iš Nesusigrąžinamos sumos į Juodraštis

Bus nurodyta darbo eigos egzemplioriaus, kuris buvo sustabdytas dėl neištaisomos klaidos, būsena **Neištaisoma**. Kai tiekėjo SF darbo eigos būsena **Nepataisoma**, ją galima nustatyti iš naujo **Juodraštis** nurodant **Atšaukti**. Tada galite redaguoti tiekėjo SF. Šią funkciją galima naudoti, jei įjungtas puslapio **Funkcijų valdymas** parametras **Tiekėjo SF darbo eigos būsenos nustatymas iš naujo iš Nesusigrąžinamos sumos į Juodraštis**.

Naudodamiesi puslapiu **Tiekėjo SF darbo eigos būsenos nustatymas iš naujo** galite iš naujo nustatyti darbo eigos būseną **Juodraštis**. Šį puslapį galite atidaryti iš **Tiekėjo SF** arba **Bendra > Užklausos > Darbo eiga**. Norėdami iš naujo nustatyti darbo eigos būseną į **Juodraštis**, pasirinkite **Atšaukti**. Taip pat galite iš naujo nustatyti darbo eigos būseną į „Juodraštis“, pasirinkdami veiksmą **Atšaukti** puslapyje **Tiekėjo SF** arba **Laukiančios tiekėjo SF**. Iš naujo nustačius darbo eigos būseną **Juodraštis**, ją galima redaguoti puslapyje **Tiekėjo SF**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>SF sumos peržiūra puslapyje Laukiančios tiekėjo SF

SF sumą galite peržiūrėti puslapyje **Laukiančios tiekėjo SF**, įjungdami puslapio **Mokėtinos sumos** parametrą **Laukiančių tiekėjo SF sąraše rodyti bendrą SF sumą**. 

## <a name="vendor-open-transactions-report"></a>Tiekėjo atidarytų operacijų ataskaita

**Tiekėjo atvirų operacijų** ataskaita pateikia išsamią informaciją apie atviras kiekvieno tiekėjo operacijas nuo jūsų nurodytos datos. Ši ataskaita dažnai naudojama audito procedūros metu balansams tarp tiekėjo užsakytų operacijų ir DK sąskaitos operacijų tikrinimui.

Kiekvienos operacijos ataskaitoje pateikiama ši informacija:

- Sąskaitos faktūros numeris
- Operacijos data
- Kvito numeris
- Operacijos suma operacijos valiuta ir apskaitos valiuta
- Kredito balansas operacijos valiuta ir apskaitos valiuta
- Debeto balansas operacijos valiuta ir apskaitos valiuta
- Tarpinė suma, išreikšta apskaitos valiuta
- Mokėjimo terminas

### <a name="filter-the-data-on-the-report"></a>Ataskaitoje pateikiamų duomenų filtravimas

Kai generuojate **Tiekėjo atvirų operacijų** ataskaitą, galimi šie numatytieji parametrai. Juos galite naudoti norėdami filtruoti duomenis, kurie bus įtraukti į ataskaitą.

- **Neįtraukti būsimo sudengimo** – Pasirinkite šį žymės langelį, jei norite neįtraukti operacijų, kurios sudengtos po datos, įvestos laukelyje **Atviros operacijos per**.
- **Atviros operacijos per** – įveskite datą, iki kurios norite įtraukti atviras operacijas. Jei neįvesite datos, šiame lauke bus nustatyta maksimali data. (Maksimali data yra vėliausia data, kurią sistema priims, 2154 m. gruodžio 31 d.) Pagal numatytuosius nustatymus, kitą kartą paleidus ataskaitą, šis laukas bus nustatytas pagal paskutinę įvestą datą.

Norėdami dar labiau sumažinti į ataskaitą įtrauktų operacijų duomenis, galite naudoti **Įtraukti įrašus** lauką.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Nustatyti tiekėjų SF strategijas](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Pagrindiniai SF duomenys AP sistemoje naudojant tiekėjo SF](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Pagrindiniai SF duomenys mokėtinose sumose naudojant patvirtinimo žurnalą](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Pagrindiniai SF duomenys AP sistemoje naudojant SF telkinį](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Įrašyti tiekėjo SF į SF žurnalą](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
