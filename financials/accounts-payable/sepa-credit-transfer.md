---
title: "SEPA kredito pervedimų apžvalga"
description: "Šiame straipsnyje pateikiama bendra informacija apie ISO 20022 kredito pervedimai, įskaitant bendros mokėjimų eurais erdvės (SEPA) kredito pervedimų ir kiti elektroniniai mokėjimai tiekėjams. SEPA pervedimas yra tam tikros rūšies mokėjimo eurais iš vienos įmonės ar atskirų kitai įmonei arba individualus. Šia tema taip pat aiškinama, kaip nustatyti ir perduoti kredito pervedimo mokėjimo failą."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>SEPA kredito pervedimų apžvalga

Šiame straipsnyje pateikiama bendra informacija apie ISO 20022 kredito pervedimai, įskaitant bendros mokėjimų eurais erdvės (SEPA) kredito pervedimų ir kiti elektroniniai mokėjimai tiekėjams. SEPA pervedimas yra tam tikros rūšies mokėjimo eurais iš vienos įmonės ar atskirų kitai įmonei arba individualus. Šia tema taip pat aiškinama, kaip nustatyti ir perduoti kredito pervedimo mokėjimo failą.

## <a name="what-is-a-credit-transfer-message"></a>Kas yra kredito pervedimas pranešimą?
Kredito pervedimo žinia yra, Pateikiančioji šalis (jūsų įmonės) siunčia perkelti lėšas iš savo sąskaitos į kreditoriaus prašymą. Šiuo metu daug būdingų šalies ar regiono ir konkrečiai bankams realizavimo kredito pervedimo pranešimus. Kai kurie iš jų yra naudojami per vieną šalį/regioną, ir kai kurie tampa standartus. Vienas gerai žinomų pasaulinis standartas yra ISO 20022 ir jo inicijavimo pranešimų, pvz., kredito pervedimo. Šioje iliustracijoje pateikta santykius ir aprėpties pasirinktą kredito pervedimo pranešimus. 
![Kredito nešiotoja](./media/credit-transfer.jpg) kredito pervedimo pranešimus\[/antraštė\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Kas yra ISO 20022 ir SEPA mokėjimai?
Bendrą mokėjimų eurais erdvę (SEPA) nustato Europos Komisija ir ja nurodoma, kad visi elektroniniai mokėjimai laikomi vietiniais, nepaisant asmens, verslo arba organizacijos buvimo vietos šalies / regiono. Nėra jokio skirtumo tarp nacionalinių mokėjimų ir tarptautinių mokėjimų. SEPA apima 28 valstybių į Europos Sąjungos (ES), ir taip pat Islandija, Lichtenšteinas, Norvegija, Šveicarija, Monakas ir San Marinas. SEPA padeda skurti bendrą mokėjimo operacijų rinką Europos ekonominėje erdvėje (EEE). Galiausiai, naudojant SEPA tikimasi sumažinti mokėjimo formatų, su kuriais dirba bankai, verslo įmonės ir asmenys, skaičių. Europos Komisija SEPA mokėjimų teisinį pagrindą nustatė naudodama mokėjimo paslaugų direktyvą (PSD). Europos mokėjimų taryba (EPC) SEPA palaiko toliau nurodytomis veiklomis.

-   Naudodama ISO 20022 Visuotinės finansų sektoriaus pranešimų schemos XML formatą, ji nustato SEPA elektroninių mokėjimų standartus.
-   Ji nustato mokėjimų eurais tvarkymo taisykles ir gaires.

EPC, kurią sudaro Europos bankai, kuria komercines ir technines SEPA mokėjimo priemonių sistemas. Naudojami toliau pateikti trys SEPA mokėjimų tipai.

-   Kredito pervedimai.
-   Tiesioginis debetas.
-   Kortelės

## <a name="what-is-a-sepa-credit-transfer"></a>Kas yra SEPA kredito pervedimas?
SEPA kredito pervedimas yra mokėjimas iš vienos įmonės ar asmens kitai įmonei ar asmeniui. Mokėjimai turi būti atliekami eurais, ir juose turi būti nurodytas abiejų šalių tarptautinis banko sąskaitos numeris (IBAN) bei banko identifikatoriaus kodas (BIC). (BIC yra taip pat žinomas kaip visame pasaulyje cirkuliacijos draugija \[SWIFT\] kodas.) Be to, sandorio išlaidos turi būti dalijamasi tarp abiejų šalių. Kredito pervedimuose, atliekamuose tarp šalių, turi būti naudojami XML failai, atitinkantys ISO 20022 mokėjimų apdorojimo standartus ir XML formatą, kaip nurodo EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Kaip įgyvendinama kreditinio pervedimo?
Kredito pervedimo mokėjimo formato Europos šalyse yra įgyvendinama naudojant elektroninių ataskaitų (ER) ir metodų apmokėjimas funkcionalumas Dynamics 365 operacijoms. Kelių kredito perdavimo formatais, kurie naudojami kituose regionuose vis tiek naudoti senosios mokėjimo sistemą. Tarp daugelio kitų formatų, yra dvylika ISO 20022 kredito pervedimo failų formatus, kurie yra prieinami. Šias eksporto formatus SEPA ISO 20022 XML standartą. Jie naudojami generuoti ne euro mokėjimų pervedimais šalyse/regionuose, kur jie yra naudojami ir euro mokėjimų kaip nurodyta redakcijos 8.2 SEPA kredito perdavimo sistema taisyklių sąvado, EPK išskiria. Prieš diegdami kredito pervedimus, kreipkitės į banką ir gauti programinę įrangą, kuri gali būti reikalinga elektroninę bankininkystę įkelti. Jūs naudojate šią programinę įrangą perkelti XML failus, kuriuose yra mokėjimo pavedimus į savo banko.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Kokios kredito pervedimo formatus šiuo metu palaikomi Dynamics 365 operacijoms?
Visada reikia eiti į bendro naudojimo turto bibliotekoje Microsoft Dynamics trukmės paslaugų (LCS) ir peržiūrėti naujausią sąrašą rasti failus, kurie turi turto rūšies **GER konfigūracijos**. Kito skyriaus, "Ką aš turiu nustatyti?", pateikiama nuoroda į temą, paaiškina, kaip sukurti LCS saugykla Peržiūrėti galimos konfigūracijos ir importuoti pasirinktos konfigūracijos.

## <a name="what-do-i-have-to-set-up"></a>Ką turiu nustatyti?
-   Prieš kurdami kredito perkelti failus, bent vienas aktyvus kredito perdavimo konfigūracija turi būti importuoti į jūsų ER konfigūracijų. Nurodymai, [Parsisiųsti elektroninę ataskaitų konfigūracijos iš gyvavimo ciklo paslaugų](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Kai konfigūruojate mokėtinų sąskaitų mokėjimo būdus, pasirinkite į **Generic elektroninės** žymės langelį ir pasirinkite atitinkamą kredito perdavimo formatą (pvz., **ISO 20022 kreditiniu pervedimu (AT)**) kaip eksporto formatą konfigūracijos.
-   Taip pat turite nustatyti teisinį asmens ir banko sąskaitų informaciją Dynamics 365 operacijoms.
-   Banko sąskaitos numerius, IBAN ir kartais SWIFT kodus (VIC) arba kita ID yra būtinas siekiant sukurti galiojančią kreditinio pervedimo mokėjimų. Todėl, turite nustatyti juos tiekėjo banko sąskaitos ir banko sąskaitos organizacija, kuri pateikia užklausą dėl perkėlimo.
-   Papildomos informacijos gali būti reikalaujama, pvz., pridėtinės vertės mokestis (PVM) skaičius šalių, kurios yra nurodytos kredito pervedimo pranešimą. Ši informacija turi būti nustatytas tiekėjų ir juridinio subjekto kai prašoma.
-   Kai kurių sąskaitų mokėtinos metodai mokėjimas, daugiausia ISO 20022 – pagal mokėjimo būdus, gali prireikti papildomų nustatymų, **mokėjimo formato kodų rinkinius**, pvz., **paslaugos rūšį** = **SLEV**. Šie kodai yra naudojami kaip papildomas žymėjimas dėl mokėjimo operacijų mokėjimo apdorojimo metu. Numatytosios vertės mokėjimo kodus, kaip **kategorija tikslu**, **už pareikštinių**, **vietos priemonė** ir **eksploatavimo lygiu** gali būti nustatyta dviejose vietose. Pirmiausia yra **sąskaitų mokamos mokėjimo žurnalo antraštės** ir antra **sudaro mokėtinos išmokos metodai**. Pagal mokėjimo žurnalo eilučių kūrimas, mokėjimo kodas mokėjimo žurnalo antraštės vertės yra perkeliamas į žurnalo eilutę, jei ne nustatyti, reikšmės iš mokėjimo būdai yra naudojami.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Generuoti kredito lėšų pervedimus galimi kokie parametrai?
Konkrečių parametrų sąrašas priklauso nuo kredito perdavimo formatas. Šioje lentelėje yra parametrų, kurie yra prieinami, kai jums sukurti ISO 20022 kredito pervedimo mokėjimo failą Vokietijos tiekėjo mokėjimų žurnale. Naudodami parinktis, kurios pasiekiamos ir **fone** skirtuką, galite paleisti mokėjimo kartos paketais.

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
<li><strong>Strd</strong> – pasirinkite šią parinktį Norėdami naudoti struktūros forma, kai vieno mokėjimo eilutės pagal vieną sąskaitą faktūrą. Šios parinkties nėra būdingų šalies ar regiono eksporto formatai, Prancūzija, Vokietija ir Nyderlandai.</li>
<li><strong>Nestruktūrinis</strong> – pasirinkite šią parinktį, jei norite naudoti nestruktūrinį formatą, kai mokėjimas sudengiamas pagal kelias SF. Sudengtų SF numeriai sujungiami ir naudojami kaip pavedimo informacija. Laikantis ISO 20022 gaires, nestruktūrinių pervedimo informacija yra ribotas iki 140 ženklų.</li>
</ul></td>
</tr>
<tr class="even">
<td>SF skaičius</td>
<td>Įvesti sąskaitos faktūros numerį, kad <strong>mokėjimo pažymą</strong> ataskaita spausdinama iš.</td>
</tr>
<tr class="odd">
<td>Eilės numeris</td>
<td>Įveskite sekos numerį failui identifikuoti. Sekos numeris ant to <strong>lydinti pažyma</strong> ataskaita.</td>
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
Banko identifikavimo kodą (BIC) ir tarptautinis banko sąskaitos numeris (IBAN) yra naudojami identifikuoti bet kuriuo abonementu daugelyje šalių ir regionų visame pasaulyje. Tarp 34 SEPA šalyse/regionuose. Įveskite BIC – į **SWIFT kodas** srityje ir IBAN – į **IBAN** srityje. Kreditoriaus banko sąskaitą bei kliento banko sąskaitos, esančius šiose srityse, **papildoma identifikavimo** FastTab ant, **banko sąskaitos** skirtuke, **banko sąskaitų** puslapis. BIC naudojimą SEPA mokėjimų nebėra privalomas.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Kaip mokėjimo failą perduoti bankui?
Kai kuriate mokėjimai, mokėjimo failas yra sukurtas, ir būsite paprašyti jį įrašyti iš žiniatinklio naršyklės galima bet kurioje vietoje. Kitas žingsnis yra atsiųsti XML failą į savo banką. Šis procesas įvairiuose bankuose skiriasi. Norėdami failus pateikti bankui apdoroti, vykdykite iš savo banko gautus nurodymus.


