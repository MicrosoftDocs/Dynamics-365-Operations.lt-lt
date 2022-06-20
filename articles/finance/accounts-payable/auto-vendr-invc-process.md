---
title: Automatizuotų tiekėjo SF išrašymo procesų apžvalga
description: Šiame straipsnyje aprašomos galimybės automatizuoti tiekėjo SF apdorojimą ir automatinio proceso naudojimo teikiama nauda.
author: abruer
ms.date: 02/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d2c629ed2d064a3350ec8ffe53940098d12ab0b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883451"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Automatizuotų tiekėjo SF išrašymo procesų apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos galimybės automatizuoti tiekėjo SF apdorojimą ir automatinio proceso naudojimo teikiama nauda. Šią funkciją sudaro funkcijos, įjungtos funkcijų valdyme. Šios funkcijos taikomos tik tiekėjo SF, o ne SF, kurios apdorojamos naudojant puslapius **SF žurnalas** arba **SF registro žurnalas**.

Organizacijos dažnai dirba su trečiosiomis šalimis, kad popierinės SF būtų apdorotos naudojant optinio ženklų atpažinimo (OCR) paslaugų teikėją. Paslaugų teikėjas pateikia kompiuteriu nuskaitomus SF metaduomenis. Modulio Mokėtinos sumos automatizavimo funkcijos leidžia naudoti šiuos artefaktus modulyje Mokėtinos sumos, kad būtų lengviau atlikti automatizavimą.

Galite automatizuoti kai kuriuos modulio Mokėtinos sumos tiekėjo SF išrašymo procesus. Šie procesai apima importuotų tiekėjo SF pateikimą darbo eigos sistemai ir užregistruotų produktų gavimo kvitų eilučių sugretinimas su patvirtinimo laukiančiomis tiekėjo SF eilutėmis. Automatizuotas procesas nurodo informaciją apie tiekėjo SF eigą, kai ji pereina kiekvieną procesą. Ši funkcija gali padėti modulio Mokėtinos sumos tarnautojams ir vadovams apdoroti tiekėjo SF efektyviau. Ji taip pat padeda sumažinti klaidų ir neveiksmingumo atvejų, kurie gali įvykti, kai informacija įvedama ir apdorojama neautomatiniu būdu, skaičių.

Automatizavimo procesai gali būti naudojami norint atlikti toliau nurodytas užduotis.

- Automatiškai taikyti išankstinį mokėjimą tiekėjų sąskaitoms
- Automatiškai pateikti importuotas SF darbo eigos sistemai.
- Gretinti produktų gavimo kvitus su patvirtinimo laukiančiomis tiekėjo SF eilutėmis.
- Imituoti registravimą prieš registruojant tiekėjo SF.
- Greitai ir efektyviai peržiūrėti darbo eigos bei automatizavimo retrospektyvą.
- Peržiūrėti ir analizuoti tiekėjo SF apdorojimo automatizavimo rezultatus.
- Tęsti automatizuotą kelių SF apdorojimą.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Importuotų tiekėjo sąskaitų-faktūrų pateikiamas darbo eigos sistemai

Kaip nenaudingo mokėtinų sumų SF išrašymo proceso dalis, importuota SF gali būti automatiškai pateikta darbo eigos sistemai. Procesas bus vykdomas fone tokiu dažnumu, kokį nurodysite (kas valandą ar kas dieną). Norint automatiškai pateikti importuotas SF darbo eigos sistemai, reikia, kad jūsų procesas prasidėtų importuota SF. Norint užtikrinti, kad SF gali būti apdorota nuo pradžios iki pabaigos be rankinio įsikišimo, automatizuotos registravimo užduotys turi būti įtrauktos į darbo eigos konfigūraciją.


Sąskaitos faktūros, susijusios su pirkimo užsakymais (PU), ir sąskaitos faktūros, kuriose yra ne PU įsigijimo kategorija ir nekaupiamų prekių eilučių, gali būti automatiškai pateiktos darbo eigos sistemai. Sąskaitas-faktūras, kurios yra įvedamos neautomatiniu būdu, ir sąskaitas-faktūras, sukurtas naudojant darbo sritį **Tiekėjo bendradarbiavimo sąskaitos-faktūros išrašymas**, reikia pateikti neautomatiniu būdu darbo eigos sistemai. Išankstinio mokėjimo prašymo apdorojimą importuotoms sąskaitoms-faktūroms reikia atlikti rankiniu būdu. Išankstinius mokėjimus rankiniu būdu galima prisitaikyti prieš registruojant importuotą sąskaitą-faktūrą ar po registravimo. Išankstinius mokėjimus galima rankiniu būdu pritaikyti neregistruotoms standartinėms sąskaitoms-faktūroms, naudojant puslapį **Tiekėjo sąskaitos-faktūros**. Baigus registraciją suderintą išankstinį mokėjimą bus galima rankiniu būdu pritaikyti kitoms šio tiekėjo sąskaitoms-faktūroms puslapyje **Tiekėjai** (**Mokėtinos sumos \> Banda \> Tiekėjai \> Visi tiekėjai \> Sąskaitos skirtukas \> Taikyti**).

Automatizavimo funkcija suteikia lanksčią sistemą, leidžiančią nustatyti įmonei būdingas taikomas taisykles, skirtas pateikti importuotas tiekėjo SF darbo eigos sistemai ir gretinti produktų gavimo kvitų eilutes su patvirtinimo laukiančiomis tiekėjo SF eilutėmis.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Gavimo kvitų sugretinimas su sąskaitos faktūros eilutėmis, kurioms taikoma trišalė atitikimo strategija

Užregistruoti produkto gavimo kvitai gali būti automatiškai sugretinti su SF eilutėmis, kurioms nustatyta triakė atitikimo strategija. Procesas bus vykdomas, kol sugretinto produkto gavimo kvito kiekis bus lygus SF kiekiui. Šio proceso metu galite nurodyti maksimalų kartų, kai sistema turi bandyti sugretinti produkto gavimo kvitus su SF eilute prieš padarydama išvadą, kad procesas nepavyko, skaičių. Procesas bus vykdomas fone kas valandą arba kas dieną. Automatizuotą atitikimo procesą galite vykdyti kaip SF pateikimo darbo eigos sistemai proceso dalį. Taip pat jį galite vykdyti kaip atskirą procesą.

## <a name="pre-validate-vendor-invoice-posting"></a>Išankstinis tiekėjo sąskaitos-faktūros registravimo patvirtinimas

Registravimo modeliavimas užbaigia tikrinimo veiksmus, atliekamus tiekėjo SF registravimo proceso metu, bet sąskaitos neatnaujinamos. Norėdami vykdyti procesą, galite pasirinkti vieną arba kelias SF puslapyje **Laukiančios tiekėjo SF**.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Patobulinta tiekėjo sąskaitų-faktūrų darbo eigos ir automatizavimo retrospektyvos informacijos peržiūra

Pateikiamas lengvai skaitomas tiekėjo SF darbo eigos retrospektyvos rodinys. Tiekėjo SF darbo eigos retrospektyvą galima pasiekti tiesiogiai iš tiekėjo SF. Todėl, norint rasti šią informaciją, reikia atlikti mažiau spustelėjimų. Jei jūsų organizacija yra įjungusi galimybę automatiškai pateikti importuotas tiekėjo SF į darbo eigą, yra pateikiama importuotų SF automatizavimo retrospektyva. Automatizavimo retrospektyva padeda rasti dabartinį proceso veiksmą bei jau baigtus veiksmus. Jei veiksmas nesėkmingas, išsami informacija bus pateikta, kad būtų geriau suprasta trikties priežastis.

## <a name="analytics-and-metrics"></a>Analizė ir metrika

Darbo sritis **Tiekėjo SF įrašas** leidžia sutelkti dėmesį į tiekėjo SF, kurios neperėjo automatizuoto proceso. Darbo srities plytelės teikia informaciją apie tiekėjo SF, kurios nebuvo sėkmingai pateiktos darbo eigos sistemai, importuotos ar sugretintos su produktų gavimo kvitais. Taip pat pateikiama „Microsoft Power BI” metrika, siekiant suteikti modulio Mokėtinos sumos vadovams įžvalgų apie tiekėjo SF automatizavimo efektyvumą.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Kelių sąskaitų-faktūrų apdorojimo automatizavimo tęsimas

Kai importuota sąskaita-faktūra sėkmingai nepateikiama į darbo eigą naudojant automatinį procesą, sistema ją pašalina iš tolesnio automatizuoto apdorojimo. Mokėtinų sumų klerkas gali peržiūrėti ir redaguoti sąskaitą faktūrą, prieš tai, kai automatizuotas procesas iš naujo pateikia ją darbo eigai. Kai gedimo priežastis gali būti išspręsta naudojant tą patį pataisymą keliose SF, galite iš naujo paleisti automatizuotą procesą puslapyje **Automatizuoto SF apdorojimo tęsimas**. 

## <a name="tracking-the-invoice-received-date-value"></a>Sąskaitos-faktūros gavimo datos vertės sekimas

**Sąskaitos-faktūros gavimo datos** vertė rodo datą, kada įmonė sąskaitą-faktūrą gavo iš tiekėjo. Taip pradedamas sekti sąskaitos-faktūros automatizavimo procesų progresas. Šią vertę galima įtraukti į tiekėjo sąskaitos-faktūros importuotus duomenis. Rankiniu būdu sukurtoms sąskaitoms-faktūroms galima nurodyti datą. Neįvedus jokios vertės, numatyta, kad naudojama dabartinė data.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Importuotos sąskaitos-faktūros sumos ir importuotų pardavimų mokesčio sumos reikšmių stebėjimas

**Importuotos SF sumos** ir **Importuotos pardavimų mokesčių sumos** vertes tiekėjo SF galima pateikti tiekėjo SF importavimo faile. Paprastai šios vertės yra iš SF, kurią nuskaitė išorinis tiekėjas ir kuri yra įtraukta į importavimo failą. Kadangi SF apdorojama mokėtinų sumų sąskaitose, vertės bus apskaičiuotos pagal SF duomenis. SF galima registruoti tik jei importuotos vertės atitinka apskaičiuotas vertes. Atitikimo vertės užtikrina, kad SF tiksliai atspindi tiekėjui mokėjimą sumą. Jei jūsų įmonė leidžia importuotas SF pateikti darbo eigos sistemai automatiškai, galite pasirinktinai reikalauti, kad importuotos sumos atitiktų apskaičiuotas sumas prieš pateikiant SF darbo eigos sistemai.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Tiekėjo SF automatizavimas – kelių SF automatizuoto apdorojimo tęsimas
Kai importuota SF nėra sėkmingai pateikta darbo eigai per automatizuotą procesą, ji bus pašalinta iš tolesnio automatinio apdorojimo. Mokėtinų sumų klerkas gali peržiūrėti ir redaguoti sąskaitą faktūrą, prieš tai, kai automatizuotas procesas iš naujo pateikia ją darbo eigai. Kai gedimo priežastis gali būti išspręsta naudojant tą patį pataisymą keliose SF, galite iš naujo paleisti automatizuotą procesą puslapyje **Automatizuoto SF apdorojimo tęsimas**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
