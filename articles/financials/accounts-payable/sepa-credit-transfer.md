---
title: "SEPA kredito pervedimų apžvalga"
description: "Šiame straipsnyje pateikiama bendra informacija apie ISO 20022 kredito pervedimus, kurie apima bendros mokėjimų eurais erdvės (SEPA) kredito pervedimus ir bet kurį kitą elektroninį mokėjimą tiekėjams. SEPA kredito pervedimas yra konkretaus tipo mokėjimas eurais iš vienos įmonės ar asmens kitai įmonei ar asmeniui. Temoje taip pat paaiškinta, kaip nustatyti ir perduoti SEPA kredito pervedimo mokėjimo failą."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1aa70dea3b0e7056afbdba96f4475c3e7e71f57c
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="sepa-credit-transfer-overview"></a>SEPA kredito pervedimų apžvalga

[!INCLUDE [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama bendra informacija apie ISO 20022 kredito pervedimus, kurie apima bendros mokėjimų eurais erdvės (SEPA) kredito pervedimus ir bet kurį kitą elektroninį mokėjimą tiekėjams. SEPA kredito pervedimas yra konkretaus tipo mokėjimas eurais iš vienos įmonės ar asmens kitai įmonei ar asmeniui. Temoje taip pat paaiškinta, kaip nustatyti ir perduoti SEPA kredito pervedimo mokėjimo failą.

## <a name="what-is-a-credit-transfer-message"></a>Kas yra kredito pervedimo pranešimas?
Kredito pervedimo pranešimas yra reikalavimas, kurį pradedanti pusė (jūsų įmonė) išsiunčia, norėdama perkelti fondus iš savo paties sąskaitos kreditoriui. Yra daug šaliai / regionui būdingų ir bankams būdingų kredito pervedimo pranešimų diegimų. Kai kurie iš jų naudojami vienoje šalyje / regione, o kai kurie tampa stanfatbais. Vienas nusistovėjęs pasaulinis standartas yra ISO 20022 ir jo inicijavimo pranešimai, pvz., Kredito pervedimas. Šioje iliustracijoje pavaizduoti pasirinktų kredito pervedimo pranešimų ryšiai ir draudimas. 
![Kredito pervedimas](./media/credit-transfer.jpg) Kredito pervedimo pranešimai 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Kas yra ISO 20022 ir SEPA mokėjimai?
Bendrą mokėjimų eurais erdvę (SEPA) nustato Europos Komisija ir ja nurodoma, kad visi elektroniniai mokėjimai laikomi vietiniais, nepaisant asmens, verslo arba organizacijos buvimo vietos šalies / regiono. Nacionaai mokėjimai ir tarptautiniai mokėjimai niekuo nesiskiria. SEPA apima 28 Europos Sąjungos (ES) valstybes nares ir Islandiją, Lichtenšteiną, Norvegiją, Šveicariją, Monaką ir San Mariną. SEPA padeda skurti bendrą mokėjimo operacijų rinką Europos ekonominėje erdvėje (EEE). Galiausiai, naudojant SEPA tikimasi sumažinti mokėjimo formatų, su kuriais dirba bankai, verslo įmonės ir asmenys, skaičių. Europos Komisija SEPA mokėjimų teisinį pagrindą nustatė naudodama mokėjimo paslaugų direktyvą (PSD). Europos mokėjimų taryba (EPC) SEPA palaiko toliau nurodytomis veiklomis.

-   Naudodama ISO 20022 Visuotinės finansų sektoriaus pranešimų schemos XML formatą, ji nustato SEPA elektroninių mokėjimų standartus.
-   Ji nustato mokėjimų eurais tvarkymo taisykles ir gaires.

EPC, kurią sudaro Europos bankai, kuria komercines ir technines SEPA mokėjimo priemonių sistemas. Naudojami toliau pateikti trys SEPA mokėjimų tipai.

-   Kredito pervedimai.
-   Tiesioginis debetas.
-   Kortelės

## <a name="what-is-a-sepa-credit-transfer"></a>Kas yra SEPA kredito pervedimas?
SEPA kredito pervedimas yra mokėjimas iš vienos įmonės ar asmens kitai įmonei ar asmeniui. Mokėjimai turi būti atliekami eurais, ir juose turi būti nurodytas abiejų šalių tarptautinis banko sąskaitos numeris (IBAN) bei banko identifikatoriaus kodas (BIC). (Tarptautinės organizacijos, teikiančios finansinių pranešimų perdavimo paslaugas \[SWIFT\] kodas taip pat vadinamas banko identifikacijos kodu (BIC).) Be to, operacijos išlaidas turi dalintis abi šalys. Kredito pervedimuose, atliekamuose tarp šalių, turi būti naudojami XML failai, atitinkantys ISO 20022 mokėjimų apdorojimo standartus ir XML formatą, kaip nurodo EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Kaip kredito pervedimas atliekamas?
Europos šalių kredito pervedimo mokėjimo formatas diegiamas naudojant „Microsoft Dynamics 365 for Finance and Operations‟ leidimo funkcijas Elektroninės ataskaitos (ER) ir Mokėjimo būdai. Keletas kredito pervedimo formatų, naudojamų kituose regionuose, vis dar naudoja mokėjimo formatų sistemą. Be daugelio kitų formatų, yra dvylika ISO 20022 kredito pervedimo failų formatai, kurie yra pasiekiami. Šie eksportavimo formatai atitinka SEPA ISO 20022 XML standartą. Jie naudojami generuoti mokėjimo pervedimus ne eurais tose šalyse / regionuose, kuriose jie naudojami, ir mokėjimus eurais, kaip nurodyta SEPA redito pervedimo schemos taisyklių sąvado 8.2 versijoje. Prieš naudodami kredito pervedimus, turite susisiekite su savo banku ir gauti programinę įrangą, kurios reikia norint įkelti elektroninės bankininkystės failus. Tą programinę įrangą naudosite XML failams, kuriuose bus mokėjimo užsakymai, perduoti bankui.

## <a name="what-credit-transfer-formats-are-currently-supported-in-finance-and-operations"></a>Kokie kredito pervedimo formatai šiuo metu palaikomi sprendime „Finance and Operations“?
Visada turite eiti į bendrai naudojamo turto biblioteką „Microsoft Dynamics“ skirtą „Lifecycle services“ (LCS) ir peržiūrėti naujausią prieinamų failų, kurių turto tipas yra **GER konfigūracija**, sąrašą. Kitame skyriuje – „Ką turiu nustatyti?“ – pateikiama nuoroda į temą, kurioje paaiškinta, kaip sukurti LCS saugyklą norint peržiūrėti galimas konfigūracijas ir importuoti pasirinktas konfigūracijas.

## <a name="what-do-i-have-to-set-up"></a>Ką turiu nustatyti?
-   Prieš kuriant kredito pervedimo failus, į jūsų Bendrųjų elektroninių ataskaitų konfigūracijas reikia importuoti bent vieną aktyvią ER kredito pervedimų konfigūraciją. Instrukcijų ieškokite [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Konfigūruodami Mokėtinų sumų mokėjimo būdus, pažymėkite žymės langelį **Bendrosios elektroninės ataskaitos** ir pasirinkite atitinkamą kredito pervedimo formatą (pvz.,, **ISO 20022 kredito pervedimas (AT)**) kaip eksporto formato konfigūraciją.
-   Taip pat sprendime „Finance and Operations‟ turite nustatyti juridinio subjekto ir banko sąskaitos informaciją.
-   Banko sąskaitų numeriai, IBAN ir kartais SWIFT kodai (BIC) arba kiti ID reikalingi norint sukurti tinkamus kredito pervedimo mokėjimus. Todėl turite juos nustatyti tiek tiekėjo banko sąskaitoje, tiek organizacijos, pageidaujančios pervedimo, banko sąskaitoje.
-   Gali būti reikalaujama kredito pervedimo pranešime nurodytų šalių papildomos informacijos, pvz., pridėtinės vertės mokesčio (PVM). Šią tiekėjų ir juridinio subjekto informaciją turite nustatyti, kai jos reikalaujama.
-   Kai kuriems Mokėtinų sumų mokėjimo metodams, daugiausia ISO 20022 pagrįstiems metodams, gali reikėti papildomo **Mokėjimo formatų kodų rinkiniai**, pvz., **Paslaugos tipas** = **SLEV**, nustatymo. Šie kodai naudojami kaip papildomas mokėjimo operacijų žymėjimas mokėjimo apdorojimo metu. Numatytąsias Mokėjimo kodų vertes, pvz., **Kategorijos paskirtis**, **Mokesčio mokėtojas**, **Vietinis garantas** ir **Paslaugos lygis**, galima nustatyti dviejose vietose. Pirmoji vieta – **Mokėtinų sumų mokėjimų žurnalo antraštė**, antroji vieta – **Mokėtinų sumų mokėjimo metodai**. Kuriant mokėjimo žurnalo eilutes, Mokėjimo kodo vertės, nustatytos mokėjimo žurnalo antraštėje, perkeliamos į žurnalo eilutę, jei nėra nustatytos, naudojamos vertės iš Mokėjimo metodų.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Kokie prieinami kredito pervedimo mokėjimų generavimo parametrai?
Konkrečių parametrų sąrašas priklauso nuo kredito pervedimo formato. Toliau pateikiamoje lentelėje parodyti parametrai, pasiekiami generuojant ISO 20022 kredito pervedimo mokėjimo failą, skirtą Vokietijai, tiekėjo mokėjimo žurnale. Naudodami parinktis, esančias skirtuke **Vykdyti fone**, mokėjimų generavimą galite vykdyti paketiniu režimu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Laukas</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Paketinis rezervavimas</td>
<td>Pažymėkite šį žymės langelį, kad į XML failą būtų įtraukta paketinio rezervavimo žymė.</td>
</tr>
<tr class="even">
<td>Vykdymo data</td>
<td>Įveskite datą, kada bankas turėtų apdoroti mokėjimus.</td>
</tr>
<tr class="odd">
<td>Formatuoti</td>
<td>Atsižvelgdami į savo šalies / regiono ar banko reikalavimus, pasirinkite pavedimo informacijos formatą.
<ul>
<li><strong>Struktūrinis</strong> – pasirinkite šią parinktį, jei norite naudoti struktūrinį formatą, kai viena mokėjimo eilutė sudengiama pagal vieną SF. Ši parinktis su Prancūzijos, Vokietijos ar Nyderlandų konkrečios šalies / regiono eksportavimo formatais negalima.</li>
<li><strong>Nestruktūrinis</strong> – pasirinkite šią parinktį, jei norite naudoti nestruktūrinį formatą, kai mokėjimas sudengiamas pagal kelias SF. Sudengtų SF numeriai sujungiami ir naudojami kaip pavedimo informacija. Laikantis ISO 20022 gairių, nestruktūrinio pavedimo informacija apribota iki 140 simbolių.</li>
</ul></td>
</tr>
<tr class="even">
<td>SF skaičius</td>
<td>Įveskite sąskaitų faktūrų skaičių, pagal kurį spausdinama <strong>Mokėjimo pažyma</strong> ataskaita.</td>
</tr>
<tr class="odd">
<td>Eilės numeris</td>
<td>Įveskite sekos numerį failui identifikuoti. Sekos numeris rodomas ataskaitoje <strong>Lydinti pažyma</strong>.</td>
</tr>
<tr class="even">
<td>Spausdinti lydinčią pažymą</td>
<td>Pažymėkite šį žymės langelį, jei norite spausdinti <strong>Lydinčios pažymos</strong> ataskaitą.</td>
</tr>
<tr class="odd">
<td>Spausdinti kontrolės ataskaitą</td>
<td>Pažymėkite šį žymės langelį, jei norite spausdinti ataskaitą, kurioje pateikiama mokėjimo informacija.</td>
</tr>
<tr class="even">
<td>Spausdinti lydraštį</td>
<td>Pažymėkite šį žymės langelį, jei norite spausdinti <strong>Mokėjimo pažymos</strong> ataskaitą.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Kas yra IBAN ir BIC?
Tarptautinis banko sąskaitos numeris (IBAN) ir banko identifikavimo kodas (BIC) yra naudojami norint nustatyti bet kurią sąskaitą daugelyje šalių / regionų visame Pasaulyje. Jos apima 34 SEPA šalis / regionus. Įveskite BIC lauke **SWIFT kodas** ir IBAN – lauke **IBAN**. Šie kreditoriaus banko sąskaitos ir kliento banko sąskaitos laukai yra „FastTab“ **Papildoma identifikacija** skirtuke **Banko sąskaita**, esančiame puslapyje **Banko sąskaitos**. BIC naudojimas SEPA mokėjimuose nebėra privalomas.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Kaip mokėjimo failą perduoti bankui?
Kai generuojate mokėjimus, sugeneruojamas mokėjimo failas ir jūs raginami jį iš interneto naršyklės įrašyti į bet kurią galimą vietą. Kitas veiksmas yra XML failą nusiųsti bankui. Šis procesas įvairiuose bankuose skiriasi. Norėdami failus pateikti bankui apdoroti, vykdykite iš savo banko gautus nurodymus.




