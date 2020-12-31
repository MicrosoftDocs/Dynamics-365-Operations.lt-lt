---
title: Išplėstinio banko derinimo importavimo proceso nustatymas
description: Pažangaus banko suderinimo funkcija suteikia galimybę importuoti elektroninius banko išrašus ir automatiškai juos suderinti su banko operacijomis programoje „Microsoft“ „Dynamics 365 Finance“. Šiame straipsnyje paaiškinama, kaip nustatyti banko išrašų importavimo funkciją.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45f997a91701e3fc63278cdba3479dec9dc7a467
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445991"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Išplėstinio banko derinimo importavimo proceso nustatymas

[!include [banner](../includes/banner.md)]

Pažangaus banko suderinimo funkcija suteikia galimybę importuoti elektroninius banko išrašus ir automatiškai juos suderinti su banko operacijomis programoje „Dynamics 365 Finance“. Šiame straipsnyje paaiškinama, kaip nustatyti banko išrašų importavimo funkciją. 

Banko išrašo importavimo nustatymas priklauso nuo elektroninio banko išrašo formato. „Finance“ iš karto palaiko tris banko išrašų formatus: ISO20022, MT940 ir BAI2.

## <a name="set-time-zone-preference"></a>Norimos laiko juostos pasirinkimas
Sukonfigūravus banko išrašų importavimo parametrus, gali būti svarbu atsižvelgti į datos ir laiko duomenų, esančių banko išrašų failuose, kurie bus importuojami, laiko juostą. Pagal numatytąjį parametrą laikoma, kad visos datos ir laiko vertės jau yra Universaliojo laiko (UTC) formatu, todėl importuojant duomenis laiko juostos nebus konvertuojamos. 

Yra parinktis, skirta nustatyti laiko juostą, kuri bus naudojama duomenims importuoti. Ši pasirinktis yra galima lauke **Laiko juostos pasirinkimas**, esančiame kiekviename puslapyje **Šaltinio duomenų formato informacija** („FastTab” **Duomenų valdymo darbo sritis > Duomenų šaltinių konfigūravimas > Duomenų formato pasirinkimas > Regiono parametrai**). Pasirinkta laiko juosta bus taikoma importuojant, kai naudojamas šis šaltinio duomenų formatas. Galite sukurti tiek duomenų šaltinio formatų, kiek reikia duomenims importuoti iš keleto laiko juostų.  

Ši laiko juosta gali nesutapti su vartotojo arba įmonės laiko juosta, todėl būtinai nurodykite, kokia laiko juosta naudojama datos ir laiko duomenyse. Pasirinkdami laiko juostą, rekomenduojame atsižvelgti į toliau pateikiamus punktus. 

 - Pasirinkta laiko juosta bus taikoma importuojant, kai naudojamas atitinkamas šaltinio duomenų formatas. Galite sukurti tiek duomenų šaltinio formatų, kiek reikia duomenims importuoti iš keleto laiko juostų. 
 
 - Pasirinkta laiko juosta turėtų būti importuojamo failo datos ir laiko duomenų vietos laiko juosta. 
 
 - Datos ir laiko duomenų laiko juosta gali nesutapti su vartotojo arba įmonės laiko juosta.
 
 - Vartotojai gali koreguoti savo laiko juostą nustatydami parametrą **Vartotojo parinktys**.

Atkreipkite dėmesį, kad atlikus toliau pateikiamus veiksmus sumažinama galimų datos ir laiko konfliktų importuojant banko išrašus tikimybė. 

 - Venkite keisti banko sąskaitų, kuriose jau yra importuotų išrašų, laiko juostos parametrus. Laiko juostos parametrų keitimas gali turėti įtakos naujų išrašų tvarkai esamų išrašų atžvilgiu dėl laiko juostos koregavimo. 
 
 - Peržiūrėkite visus importuojamus duomenis, kuriuose naudojamas pasirinktas duomenų šaltinio formatas. Nustatyta formato laiko juosta bus taikoma visiems importuojamiems projektams, kuriuose naudojamas minėtas formatas. Įsitikinkite, kad pasirinkta laiko juosta tinka visiems importuojamiems projektams, kuriuose naudojamas minėtas formatas.

## <a name="sample-files"></a>Failų pavyzdžiai
Naudodami bet kurį iš trijų formatų, privalote turėti failus, kurie elektroninio banko išrašo pradinį formatą konvertuoja į „Finance“ naudojamą formatą. Reikiamus šaltinio failus galite rasti „Microsoft Visual Studio“ programų naršyklės mazge **Ištekliai**. Suradę failus, nukopijuokite juos į vieną žinomą vietą, kad sąrankos proceso metu galėtumėte juos lengvai nusiųsti.

| Išteklių pavadinimas                                           | Failo vardas                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Banko išrašų formatų ir techninių maketų pavyzdžiai
Toliau pateikiami išplėstinio banko derinimo importavimo failo techninio maketo aprašų pavyzdžiai ir trys susijusių banko išrašo failų pavyzdžiai. https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Techninio maketo aprašas                             | Banko išrašo failo pavyzdys          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>ISO20022 banko išrašų importavimo nustatymas
Pirmiausia turite nustatyti ISO20022 banko išrašų formato apdorojimo grupę, naudodami duomenų objektų sistemą.

1.  Eikite į **Darbo sritys** &gt; **Duomenų valdymas**.
2.  Spustelėkite **Import**.
3.  Įveskite formato pavadinimą, pvz., **ISO20022**.
4.  Nustatykite lauką **Šaltinio duomenų formatas** į parinktį **XML-Element**.
5.  Nustatykite lauką **Objekto pavadinimas** į parinktį **Banko išrašai**.
6.  Norėdami nusiųsti importuotus failus, spustelėkite **Nusiųsti**, o tada naršykite ir pasirinkite failą **SampleBankCompositeEntity.xml**, kurį įrašėte anksčiau.
7.  Kai banko išrašų objektas yra nusiųstas ir susiejimas baigtas, spustelėkite objekto veiksmą **Peržiūrėti schemą**.
8.  Banko išrašų objektas yra sudėtinis objektas, kuris susideda iš keturių atskirų objektų. Sąraše pasirinkite **BankStatementDocumentEntity**, o tada spustelėkite veiksmą **Peržiūrėti schemą**.
9.  Skirtuke **Pakeitimai** spustelėkite **Naujas**.
10. 1 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **ISO20022XML-to-Reconciliation.xslt**, kurį įrašėte anksčiau. **Pastaba.** Transformavimo failai skirti naudoti standartiniu formatu. Kadangi bankai dažnai naudoja kitus formatus, gali būti, kad turėsite transformacijos failą atnaujinti, kad galėtumėte susieti savo banko išrašo formatą. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Spustelėkite **Naujas**.
12. 2 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **BankReconciliation-to-Composite.xslt**, kurį įrašėte anksčiau.
13. Spustelėkite **Taikyti pakeitimus**.

Nustačius formato apdorojimo grupę, kitu veiksmu reikia nustatyti ISO20022 banko išrašų formato taisykles.

1.  Eikite į **Grynųjų pinigų ir banko valdymas** &gt; **Sąranka** &gt; **Išplėstinio banko derinimo nustatymas** &gt; **Banko išrašo formatas**.
2.  Spustelėkite **Naujas**.
3.  Nurodykite išrašo formatą, pvz., **ISO20022**.
4.  Įveskite formato pavadinimą.
5.  Lauke **Apdorojimo grupė** nurodykite grupę, kurią nustatėte anksčiau, pvz., **ISO20022**.
6.  Pažymėkite žymės langelį **XML failas**.

Paskutiniu veiksmu banko sąskaitoje įjungiamas išplėstinis banko derinimas ir nustatomas išrašo formatas.

1.  Eikite į **Grynųjų pinigų ir banko valdymas** &gt; **Banko sąskaitos**.
2.  Pasirinkite banko sąskaitą ir ją atidarykite, kad peržiūrėtumėte informaciją.
3.  Skirtuke **Derinimas** nustatykite parinktį **Išplėstinis banko sąskaitų derinimas** į **Taip**.
4.  Lauke **Išrašo formatas** nurodykite formatą, kurį sukūrėte anksčiau, pvz., **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>MT940 banko išrašų importavimo nustatymas
Pirmiausia turite nustatyti MT940 banko išrašų formato apdorojimo grupę, naudodami duomenų objektų sistemą.

1.  Eikite į **Darbo sritys** &gt; **Duomenų valdymas**.
2.  Spustelėkite **Importuoti**.
3.  Įveskite formato pavadinimą, pvz., **MT940**.
4.  Nustatykite lauką **Šaltinio duomenų formatas** į parinktį **XML-Element**.
5.  Nustatykite lauką **Objekto pavadinimas** į parinktį **Banko išrašai**.
6.  Norėdami nusiųsti importuotus failus, spustelėkite **Nusiųsti**, o tada naršykite ir pasirinkite failą **SampleBankCompositeEntity.xml**, kurį įrašėte anksčiau.
7.  Kai banko išrašų objektas yra nusiųstas ir susiejimas baigtas, spustelėkite objekto veiksmą **Peržiūrėti schemą**.
8.  Banko išrašų objektas yra sudėtinis objektas, kuris susideda iš keturių atskirų objektų. Sąraše pasirinkite **BankStatementDocumentEntity**, o tada spustelėkite veiksmą **Peržiūrėti schemą**.
9.  Skirtuke **Pakeitimai** spustelėkite **Naujas**.
10. 1 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **MT940TXT-to-MT940XML.xslt**, kurį įrašėte anksčiau.
11. Spustelėkite **Naujas**.
12. 2 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **MT940XML-to-Reconciliation.xslt**, kurį įrašėte anksčiau. **Pastaba.** Transformavimo failai skirti naudoti standartiniu formatu. Kadangi bankai dažnai naudoja kitus formatus, gali būti, kad turėsite transformacijos failą atnaujinti, kad galėtumėte susieti savo banko išrašo formatą. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Spustelėkite **Naujas**.
14. 3 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **BankReconciliation-to-Composite.xslt**, kurį įrašėte anksčiau.
15. Spustelėkite **Taikyti pakeitimus**.

Nustačius formato apdorojimo grupę, kitu veiksmu reikia nustatyti MT940 banko išrašų formato taisykles.

1.  Eikite į **Grynųjų pinigų ir banko valdymas** &gt; **Sąranka** &gt; **Išplėstinio banko derinimo nustatymas** &gt; **Banko išrašo formatas**.
2.  Spustelėkite **Naujas**.
3.  Nurodykite išrašo formatą, pvz., **MT940**.
4.  Įveskite formato pavadinimą.
5.  Lauke **Apdorojimo grupė** nurodykite grupę, kurią nustatėte anksčiau, pvz., **MT940**.
6.  Nustatykite lauko **Failo tipas** reikšmę **txt**.

Paskutiniu veiksmu banko sąskaitoje įjungiamas išplėstinis banko derinimas ir nustatomas išrašo formatas.

1.  Eikite į **Grynųjų pinigų ir banko valdymas** &gt; **Banko sąskaitos**.
2.  Pasirinkite banko sąskaitą ir ją atidarykite, kad peržiūrėtumėte informaciją.
3.  Skirtuke **Derinimas** nustatykite parinktį **Išplėstinis banko sąskaitų derinimas** į **Taip**.
4.  Kai būsite paraginti patvirtinti savo pasirinkimą ir įjungti išplėstinį banko derinimą, spustelėkite **Gerai**.
5.  Lauke **Išrašo formatas** nurodykite formatą, kurį sukūrėte anksčiau, pvz., **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>BAI2 banko išrašų importavimo nustatymas
Pirmiausia turite nustatyti BAI2 banko išrašų formato apdorojimo grupę, naudodami duomenų objektų sistemą.

1.  Eikite į **Darbo sritys** &gt; **Duomenų valdymas**.
2.  Spustelėkite **Importuoti**.
3.  Įveskite formato pavadinimą, pvz., **BAI2**.
4.  Nustatykite lauką **Šaltinio duomenų formatas** į parinktį **XML-Element**.
5.  Nustatykite lauką **Objekto pavadinimas** į parinktį **Banko išrašai**.
6.  Norėdami nusiųsti importuotus failus, spustelėkite **Nusiųsti**, o tada naršykite ir pasirinkite failą **SampleBankCompositeEntity.xml**, kurį įrašėte anksčiau.
7.  Kai banko išrašų objektas yra nusiųstas ir susiejimas baigtas, spustelėkite objekto veiksmą **Peržiūrėti schemą**.
8.  Banko išrašų objektas yra sudėtinis objektas, kuris susideda iš keturių atskirų objektų. Sąraše pasirinkite **BankStatementDocumentEntity**, o tada spustelėkite veiksmą **Peržiūrėti schemą**.
9.  Skirtuke **Pakeitimai** spustelėkite **Naujas**.
10. 1 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **BAI2CSV-to-BAI2XML.xslt**, kurį įrašėte anksčiau.
11. Spustelėkite **Naujas**.
12. 2 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **BAI2XML-to-Reconciliation.xslt**, kurį įrašėte anksčiau. **Pastaba.** Transformavimo failai skirti naudoti standartiniu formatu. Kadangi bankai dažnai naudoja kitus formatus, gali būti, kad turėsite transformacijos failą atnaujinti, kad galėtumėte susieti savo banko išrašo formatą. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Spustelėkite **Naujas**.
14. 3 eilės numeryje spustelėkite **Nusiųsti failą** ir pasirinkite failą **BankReconciliation-to-Composite.xslt**, kurį įrašėte anksčiau.
15. Spustelėkite **Taikyti pakeitimus**.

Nustačius formato apdorojimo grupę, kitu veiksmu reikia nustatyti BAI2 banko išrašų formato taisykles.

1.  Eikite į **Grynųjų pinigų ir banko valdymas** &gt; **Sąranka** &gt; **Išplėstinio banko derinimo nustatymas** &gt; **Banko išrašo formatas**.
2.  Spustelėkite **Naujas**.
3.  Nurodykite išrašo formatą, pvz., **BAI2**.
4.  Įveskite formato pavadinimą.
5.  Lauke **Apdorojimo grupė** nurodykite grupę, kurią nustatėte anksčiau, pvz., **BAI2**.
6.  Nustatykite lauko **Failo tipas** reikšmę **txt**.

Paskutiniu veiksmu banko sąskaitoje įjungiamas išplėstinis banko derinimas ir nustatomas išrašo formatas.

1.  Eikite į **Grynųjų pinigų ir banko valdymas** &gt; **Banko sąskaitos**.
2.  Pasirinkite banko sąskaitą ir ją atidarykite, kad peržiūrėtumėte informaciją.
3.  Skirtuke **Derinimas** nustatykite parinktį **Išplėstinis banko sąskaitų derinimas** į **Taip**.
4.  Kai būsite paraginti patvirtinti savo pasirinkimą ir įjungti išplėstinį banko derinimą, spustelėkite **Gerai**.
5.  Lauke **Išrašo formatas** nurodykite formatą, kurį sukūrėte anksčiau, pvz., **BAI2**.

## <a name="test-the-bank-statement-import"></a>Banko išrašo importavimo tikrinimas
Paskutiniu veiksmu reikia patikrinti, ar savo banko išrašą galima importuoti.

1.  Eikite į **Grynųjų pinigų ir banko valdymas** &gt; **Banko sąskaitos**.
2.  Pasirinkite banko sąskaitą, kurioje įjungta išplėstino banko derinimo funkcija.
3.  Skirtuke **Derinti** spustelėkite **Banko išrašai**.
4.  Puslapyje **Banko išrašas** spustelėkite **Importuoti išrašą**.
5.  Lauke **Banko sąskaita** nurodykite pasirinktą banko sąskaitą. Laukas **Išrašo formatas** bus automatiškai nustatytas pagal banko sąskaitos nustatymą.
6.  Spustelėkite **Naršyti** ir pasirinkite savo elektroninio banko išrašo failą.
7.  Spustelėkite **Nusiųsti**.
8.  Spustelėkite **GERAI**.

Jei pavyko sėkmingai importuoti, bus rodomas pranešimas, kuriame teigiama, kad išrašas buvo importuotas. Jei importuoti nepavyko, suraskite užduotį darbo srities **Duomenų valdymas** dalyje **Užduočių retrospektyva**. Spustelėkite užduoties parinktį **Vykdymo informacija**, kad atidarytumėte puslapį **Vykdymo suvestinė**, o tada spustelėkite **Peržiūrėti vykdymo žurnalą**, kad peržiūrėtumėte importavimo klaidas.



