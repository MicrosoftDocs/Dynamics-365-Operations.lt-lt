---
title: Numatytosios finansinių žurnalų finansinės dimensijos
description: Šioje temoje aprašomos taisyklės, apibrėžiančios, kaip nustatomos finansinių dimensijų reikšmės operacijose, kurios įvedamos naudojant finansinius žurnalus. Joje taip pat pateikiama informacija apie scenarijus, kuriuose naudojamos fiksuotos dimensijos.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 51235b8a5dac50aad5031456760c970e50506d66
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713112"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Numatytosios finansinių žurnalų finansinės dimensijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos taisyklės, apibrėžiančios, kaip nustatomos finansinių dimensijų reikšmės operacijose, kurios įvedamos naudojant finansinius žurnalus (bet ne atsargų žurnalus arba projektų žurnalus). Joje taip pat pateikiama informacija apie scenarijus, kuriuose naudojamos fiksuotos dimensijos.

## <a name="symptom"></a>Požymis

Finansinių dimensijų reikšmės nėra nustatytos, kaip tikėtasi, finansiniame žurnale sąskaitoje arba korespondentinėje sąskaitoje. Toliau pateikiami scenarijai yra du pavyzdžiai:

Kvitas įvedamas į žurnalą (bendrąjį žurnalą). Sąskaita yra tiekėjo sąskaita, o korespondentinė sąskaita yra banko sąskaita. Tiekėjo finansinės dimensijos įvedamos sąskaitoje pagal numatytuosius nustatymus, bet banko finansinės dimensijos nėra įvedamos korespondentinėje sąskaitoje pagal numatytuosius nustatymus. Dimensijų reikšmės iš sąskaitos įvedamos į korespondentinę sąskaitą pagal numatytuosius nustatymus.

Klientui priskirtos numatytosios finansinių dimensijų reikšmės, o įplaukų pagrindinei sąskaitai priskirta fiksuotos dimensijos reikšmė padalinio finansinei dimensijai. Kvitas įvedamas į bendrąjį žurnalą.  Sąskaita yra klientas, o korespondentinė sąskaita yra didžiosios knygos sąskaita, ypač įplaukų sąskaita su fiksuotos dimensijos reikšme. Fiksuotoji dimensija nėra nustatyta įplaukų pagrindinės sąskaitos korespondentinėje sąskaitoje. Ji nustatoma kaip padalinio dimensijos reikšmė iš sąskaitos, kurią pateikė klientas.  Užregistravus kvitą, fiksuotos dimensijos reikšmė naudojama užregistruotame apskaitos įraše, bet kvite vis dar rodoma kliento padalinio reikšmė įplaukų sąskaitoje. 

Kokios taisyklės taikomos finansinių dimensijų reikšmėms, nustatytoms kvituose žurnale?

## <a name="resolution"></a>Sprendimas

Toliau nurodytos taisyklės yra taikomos, norint finansinių dimensijų reikšmes įvesti kvito eilutėse finansiniuose žurnaluose, pvz., bendrajame žurnale arba tiekėjo SF žurnale, pagal numatytuosius nustatymus. 

1. **Žurnalo antraštė**

   - Žurnalo antraštės dimensijos įvedamos iš žurnalo pavadinimo dimensijų pagal numatytuosius nustatymus.

2. **Žurnalo eilutės sąskaita**

   - Žurnalo eilutės sąskaitos dimensijos įvedamos iš žurnalo antraštės dimensijų pagal numatytuosius nustatymus.
   - Jei kurios nors finansinės dimensijos yra tuščios, jų reikšmės įvedamos pagal numatytuosius nustatymus iš kliento, tiekėjo, banko, ilgalaikio turto, projekto ar didžiosios knygos dimensijų.

     - Jei sąskaitos tipas yra **Didžioji knyga**, įvedant operaciją fiksuotoji dimensija didžiosios knygos sąskaitoje laikoma numatytąja dimensija.
     - Jei sąskaitos tipas yra **Klientas**, **Tiekėjas**, **Bankas**, **Ilgalaikis turtas** arba **Projektas**, pagrindinės sąskaitos dar negalima nustatyti. Todėl fiksuotoji dimensija niekada nebus įvesta sąskaitai pagal numatytuosius nustatymus.

3. **Žurnalo eilutės korespondentinė sąskaita**

 - Pirmiausia, žurnalo eilutės korespondentinė sąskaitos dimensijos yra paimtos iš žurnalo eilutės sąskaitos dimensijų.

 - Jei kurios nors finansinės dimensijos yra tuščios, kitas numatytasis įrašas bus pateiktas iš numatytųjų dimensijų iš kliento, tiekėjo, banko, ilgalaikio turto, projekto arba didžiosios knygos.
   1. Jei korespondentinės sąskaitos tipas yra **Didžioji knyga**, įvedant operaciją fiksuotoji dimensija didžiosios knygos sąskaitoje laikoma numatytąja dimensija. Jei dimensijos reikšmė jau buvo įvesta iš sąskaitos pagal numatytuosius nustatymus, pagrindinės sąskaitos numatytosios arba fiksuotosios dimensijos reikšmė nepaisys esamos reikšmės.
   2. Jei korespondentinės sąskaitos tipas yra **Klientas**, **Tiekėjas**, **Bankas**, **Ilgalaikis turtas** arba **Projektas**, pagrindinė sąskaita dar nėra žinoma, todėl fiksuotoji dimensija niekada nebus numatytoji korespondentinei sąskaitai.

4. **Registravimas**

    1. Registruojant pagrindinė sąskaita kiekvienai apskaitos įrašo eilutei (tiek sąskaitai, tiek korespondentinei sąskaitai) vertinama siekiant nustatyti, ar yra fiksuotosios dimensijos reikšmė. Jei fiksuotoji dimensija nustatyta, bet kurios esamos arba tuščios reikšmės pakeičiamos ta fiksuotosios dimensijos reikšme.

        Fiksuotosios dimensijos reikšmė **nėra** rodoma žurnalo eilutėse užregistravus. Ji rodoma apskaitos įraše, kai peržiūrite kvitą jį užregistravus.

    2. Registruojant neįvedamos jokios kitos dimensijos reikšmės, įskaitant papildomas didžiosios knygos sąskaitas, kurios gali būti pridėtos registruojant, pavyzdžiui, apvalinimo centais sąskaitos ir vidinės įmonės mokėtinos kam ir mokėtinos iš sąskaitos. Numatytieji papildomų didžiosios knygos sąskaitų dimensijos įrašai paimti iš sąskaitos arba korespondentinės sąskaitos.

Norint pagal numatytuosius nustatymus įvesti dimensijų reikšmes, žurnalo numatytuoju procesu negalima nustatyti, ar tuščia dimensijos reikšmė buvo sąmoningai palikta tuščia, ar numatytasis įrašas nebuvo sukurtas. Jei dimensijos reikšmė sąmoningai paliekama tuščia, ji gali būti įvesta pagal numatytuosius nustatymus naudojant anksčiau apibūdintą numatytąjį užsakymą. Jei norite, kad dimensija turėtų tuščią reikšmę, gali tekti sukurti dimensiją, kurios reikšmė būtų **0** (nulis) arba **Tuščia**, kad ją būtų galima naudoti vietoj tuščios dimensijos.

Peržiūrėkite toliau nurodytus scenarijus, kad gautumėte numatytojo finansinių dimensijų užsakymo pavyzdžių.

### <a name="scenario-1"></a>1 scenarijus

Eikit į **Didžioji knyga \> Žurnalo nustatymas \> Žurnalų pavadinimai** ir pasirinkite žurnalo pavadinimą **GenJrn**. Tada „FastTab“ **Finansinės dimensijos** nustatykite šias numatytųjų finansinių dimensijų reikšmes:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Žurnalų pavadinimų puslapis](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Eikite į **Didžioji knyga \> Žurnalo įrašai \> Bendrasis žurnalas** ir sukurkit naują bendrąjį žurnalą pavadinimu **GenJrn**. Dimensijos įvedamos pagal numatytuosius nustatymus iš žurnalo pavadinimo (lentelė LedgerJournalName) į žurnalo antraštę (lentelė LedgerJournalTable), kaip parodyta skirtuke **Finansinės dimensijos**.

[![Skirtukas Finansinės dimensijos bendrųjų žurnalų puslapyje](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Eikite į **Eilutės**. Lauke **Sąskaitos tipas** pasirinkite **Didžioji knyga** ir lauke **Sąskaita** įveskite **170150**. Tada pažymėkite **tabuliavimo** klavišą, kad išeitumėte iš lauko. Dimensijos įvedamos pagal numatytuosius nustatymus iš žurnalo antraštės. Todėl **sąskaitos** reikšmė rodoma kaip **170150-001-024**.

[![Bendrojo žurnalo eilutės žurnalo kvito puslapyje](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Pakeiskite **sąskaitos** reikšmę į **170150-001-023**. Įveskite arba debeto sumą, arba kredito sumą. Lauke **Korespondentinės sąskaitos tipas** pasirinkite **Didžioji knyga** ir lauke **Korespondentinė sąskaita** įveskite **600150**. Dimensijos reikšmės įvedamos pagal numatytuosius nustatymus iš sąskaitos. Todėl **korespondentinė sąskaitos** reikšmė rodoma kaip **600150-001-023**.

### <a name="scenario-2"></a>2 scenarijus

Naudokite tas pačias finansines dimensijas, kurias 1 scenarijuje nustatėte žurnalo pavadinimui. Tada eikite į **Gautinos sumos \> Klientai \> Visi klientai** ir nurodykite numatytąsias finansinių dimensijų reikšmes klientui US-001. Pasirinkite klientą ir atidarykite išsamią kliento informaciją. Skirtuke **Finansinės dimensijos** palikit numatytąją dimensijos **BUSINESSUNIT** reikšmę (**001**). Įtraukite dimensiją **COSTCENTER** ir kaip reikšmę įveskite **007**.

Sukurkite naują bendrąjį žurnalą pavadinimu **GenJrn**. Skirtuke **Finansinės dimensijos** pakeiskite numatytąją reikšmę **BUSINESSUNIT** iš **001** į **002**.

Eikite į **Eilutės**. Lauke **Sąskaitos tipas** pasirinkite **Klientas** ir lauke **Sąskaita** įveskite **US-001**. Norėdami peržiūrėti ne didžiosios knygos sąskaitų tipų finansines dimensijas, pasirinkite **Finansinės dimensijos \> Sąskaita**. Įvedami šie numatytieji finansinių dimensijų reikšmių įrašai:

- **BUSINESSUNIT:** 002 – numatytasis įrašas paimtas iš žurnalo antraštės. Reikšmė **001** nėra įvedama pagal numatytuosius nustatymus iš kliento US-001, nes numatytoji reikšmė jau buvo įvesta.
- **COSTCENTER:** 007 – numatytasis įrašas paimtas iš kliento US-001 nustatymo.
- **DEPARTMENT:** 024 – numatytasis įrašas paimtas iš žurnalo antraštės.

Grįžę į eilutę, lauke **Korespondentinės sąskaitos tipas** pasirinkite **Didžioji knyga** ir lauke **Korespondentinė sąskaita** įveskite **600150**. Eilutėje įvedamos šios numatytosios finansinių dimensijų reikšmės:

- **BUSINESSUNIT:** 002 – numatytasis įrašas paimtas iš sąskaitos finansinių dimensijų. (Iš pradžių jis buvo įvestas pagal numatytuosius nustatymus iš žurnalo antraštės.)
- **DEPARTMENT:** 024 – numatytasis įrašas paimtas iš sąskaitos finansinių dimensijų. (Iš pradžių jis buvo įvestas pagal numatytuosius nustatymus iš žurnalo antraštės.)
- **COSTCENTER:** 007 – numatytasis įrašas paimtas iš sąskaitos finansinių dimensijų. (Iš pradžių jis buvo įvestas pagal numatytuosius nustatymus iš kliento.)

### <a name="scenario-3"></a>3 scenarijus

Tame pačiame žurnale, kurį naudojote 2 scenarijui, pridėkite naują eilutę. Lauke **Sąskaitos tipas** pasirinkite **Didžioji knyga** ir lauke **Sąskaita** įveskite **170150**. Išvalykite numatytąsias dimensijų reikšmes, kad liktų tik 170150 pagrindinė sąskaita. Lauke **Korespondentinės sąskaitos tipas** pasirinkite **Klientas** ir lauke **Korespondentinė sąskaita** įveskite **US-001**. Įvedami šie numatytieji finansinių dimensijų reikšmių įrašai:

- **BUSINESSUNIT:** 002 – numatytasis įrašas yra paimtas iš žurnalo antraštės, nes sąskaitos dimensijos reikšmė yra tuščia. Reikšmė **001** nėra įvedama pagal numatytuosius nustatymus iš kliento US-001, nes numatytoji reikšmė jau buvo paimta iš žurnalo antraštės. Jei **BUSINESSUNIT** reikšmė sąmoningai paliekama tuščia, taip pat turite pašalinti finansinę dimensiją korespondentinėje sąskaitoje.
- **COSTCENTER:** 007 – numatytasis įrašas paimtas iš kliento US-001, nes sąskaitos dimensijos ir žurnalo antraštės dimensijos reikšmės yra tuščios. Jei **COSTCENTER** reikšmė sąmoningai paliekama tuščia, taip pat turite pašalinti finansinę dimensiją korespondentinėje sąskaitoje.
- **DEPARTMENT:** 024 – numatytasis įrašas yra paimtas iš žurnalo antraštės, nes sąskaitos dimensijos reikšmė yra tuščia. Jei **DEPARTMENT** reikšmė sąmoningai paliekama tuščia, taip pat turite pašalinti finansinę dimensiją korespondentinėje sąskaitoje.

### <a name="scenario-4"></a>4 scenarijus

Naudokite tas pačias numatytąsias finansinių dimensijų reikšmes, kurias nustatėte žurnalo pavadinimui ir klientui 1 ir 2 scenarijuose. Tada nustatykite fiksuotosios dimensijos reikšmę dimensijai **BUSINESSUNIT** pagrindinėje sąskaitoje 170150. Eikite į **Didžioji knyga \> Sąskaitų planas \> Sąskaitos \> Pagrindinės sąskaitos**. Lauke **Pagrindinė sąskaita** pasirinkite **170150**, tada skirtuke **Juridinio subjekto nepaisymai** pasirinkite **Įtraukti**. Pasirinkite **USMF** kaip juridinį subjektą, tada pasirinkite **Įtraukti**. Pasirinkite tą įrašą, tada pasirinkite **Numatytosios dimensijos**. Pakeiskite dimensiją **BUSINESSUNIT** į **Fiksuota reikšmė** ir kaip reikšmę įveskite **003**.

Sukurkite naują bendrąjį žurnalą pavadinimu **GenJrn**. Skirtuke **Finansinės dimensijos** pašalinkite visas numatytųjų dimensijų reikšmes.

Eikite į **Eilutės**. Lauke **Sąskaitos tipas** pasirinkite **Didžioji knyga** ir lauke **Sąskaita** įveskite **170150**. Tada pažymėkite **tabuliavimo** klavišą, kad išeitumėte iš lauko. Dimensijų reikšmės įvedamos pagal numatytuosius nustatymus iš pagrindinės sąskaitos nustatymo sąskaitai 170150. Todėl **sąskaitos** reikšmė rodoma kaip **170150-003-**.

Pakeiskite **sąskaitos** reikšmę į **170150-004-**. **Žurnalo funkcija neapsaugo fiksuotos dimensijos reikšmės nuo keitimo.** Įveskite arba debeto sumą, arba kredito sumą. Lauke **Korespondentinės sąskaitos tipas** pasirinkite **Didžioji knyga** ir lauke **Korespondentinė sąskaita** įveskite **170250**. Finansinės dimensijos reikšmė 004 iš sąskaitos įvedama kaip numatytoji. Tada užregistruokite dokumentą. Žurnale pasirinkite **Kvitas**. Atkreipkite dėmesį, kad registruojant **BUSINESSUNIT** reikšmė buvo grąžinta į fiksuotosios dimensijos reikšmę **003**.

Kai grįžtate prie žurnalo kvito, **BUSINESSUNIT** dimensija **neatspindi** fiksuotosios dimensijos reikšmės. Visada pateikiama reikšmė, kuri buvo rodoma ekrane prieš registruojant. Registravimo procesu niekas, kas įvesta kvite, nekeičiama. Registruojant pakeistas tik apskaitos įrašas.

## <a name="developer-notes"></a>Kūrėjo pastabos

Jei esate kūrėjas ir norite peržiūrėti numatytojo proceso kodą, peržiūrėkite šiuos metodus:

- **LedgerJournalEngine.accountModified()** – šis metodas yra pagrindinis pirminės sąskaitos dimensijos numatytojo proceso, kuris yra standartinis visiems žurnalams (ir jo nepaiso kai kurių tipų žurnalai), įvesties taškas.
- **LedgerJournalEngine.offsetAccountModified()** – šis metodas yra pagrindinis korespondentinės sąskaitos dimensijos numatytojo proceso įvesties taškas.
