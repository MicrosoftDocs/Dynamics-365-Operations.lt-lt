---
title: Parduotuvės operacijų tikrinimas išrašų duomenims apskaičiuoti
description: Šioje temoje aprašomos parduotuvės operacijų tikrinimo funkcijos „Microsoft Dynamics 365 Commerce“.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: f51b1f39aa212fe8587761721194db7791bec5bc
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087454"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Parduotuvės operacijų tikrinimas išrašų duomenims apskaičiuoti

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos parduotuvės operacijų tikrinimo funkcijos „Microsoft Dynamics 365 Commerce“. Vykdant tikrinimo procesą nustatomos ir pažymimos operacijos, kurios gali sukelti registravimo klaidų, prieš tai, kai jos yra paimamos vykdant išrašų registravimo procesą.

Kai bandote užregistruoti išrašą, gali nepavykti atlikti tikrinimo proceso dėl prekybos operacijų lentelėse pateikiamų nenuoseklių duomenų. Štai keli veiksnių, galinčių sukelti šių nenuoseklumų, pavyzdžiai:

- Operacijų suma, nurodyta antraštės lentelėje, nesutampa su eilučių operacijų suma.
- Antraščių lentelėje nurodytas prekių skaičius neatitinka operacijų lentelėje nurodyto prekių skaičiaus.
- Mokesčiai, nurodyti antraštės lentelėje, nesutampa su mokesčių suma eilutėse. 

Jei nesuderinamos operacijos paimamos vykdant išrašo registravimo procesą, dėl sukuriamų pardavimo sąskaitų faktūrų ir mokėjimo žurnalų gali nepavykti užregistruoti išrašo. Vykdant procesą **Tikrinti parduotuvės operacijas** apsaugoma nuo šių problemų, nes užtikrinama, kad į operacijų išrašų duomenų skaičiavimo procesą būtų perduodamos tik operacijų tikrinimo taisykles atitinkančios operacijos.

Toliau pateikiamame paveikslėlyje nurodomi pasikartojantys dienos operacijų įkėlimo, operacijų tikrinimo ir operacijų išrašų duomenų skaičiavimo ir registravimo procesai ir dienos pabaigos finansinės ataskaitos skaičiavimo ir registravimo procesai.

![Paveikslėlyje nurodomi pasikartojantys dienos operacijų įkėlimo, operacijų tikrinimo ir operacijų išrašų duomenų skaičiavimo ir registravimo procesai ir dienos pabaigos finansinės ataskaitos skaičiavimo ir registravimo procesai](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Parduotuvės operacijų tikrinimo taisyklės

Paketinis vykdymas **Tikrinti parduotuvės operacijas** tikrina prekybos operacijų lentelių vientisumą pagal toliau nurodytas tikrinimo taisykles.

> [!NOTE]
> Tikrinimo taisyklės ir toliau bus pridedamos prie vėlesnių leidimų.

### <a name="transaction-header-validation-rules"></a>Operacijų antraščių tikrinimo taisyklės

Toliau esančioje lentelėje pateikiamos operacijų antraščių tikrinimo taisyklės, kurios tikrinamos pagal mažmeninės prekybos operacijų antraštę prieš tas operacijas perduodant į išrašų registravimą.

| Taisyklė | Aprašymas |
|-------|-------------|
| Verslo data | Šia taisykle tikrinama, ar operacijos verslo data susieta su atviru ataskaitiniu laikotarpiu didžiojoje knygoje. |
| Valiutos apvalinimas | Šia taisykle tikrinama, ar operacijos sumos suapvalintos pagal valiutos apvalinimo taisyklę. |
| Kliento kodas | Šia taisykle tikrinama, ar operacijoje naudojamas klientas yra duomenų bazėje. |
| Nuolaidos suma | Šia taisykle tikrinama, ar nuolaidos suma antraštėje yra lygi eilučių nuolaidos sumų sumai. |
| Finansinių dokumentų registravimo būsena (Brazilija) | Šia taisykle tikrinama, ar finansinis dokumentas gali būti sėkmingai užregistruotas. |
| Bendra suma | Šia taisykle tikrinama, ar bendra suma operacijų antraštėje atitinka operacijų eilučių grynąją sumą, įskaitant mokestį, ir išlaidas. |
| Grynoji | Šia taisykle tikrinama, ar grynoji suma operacijų antraštėje atitinka operacijų eilučių grynąją sumą, neįskaitant mokesčio, ir išlaidas. |
| Grynoji ir mokestis | Šia taisykle tikrinama, ar bendra suma operacijų antraštėje atitinka operacijų eilučių grynąją sumą, neįskaitant mokesčio, ir visus mokesčius bei išlaidas. |
| Prekių skaičius | Šia taisykle tikrinama, ar operacijų antraštėje nurodytas prekių skaičius atitinka operacijos eilutėse nurodytų kiekių sumą. |
| Mokėjimo suma | Šia taisyklė tikrinama, ar operacijos antraštėje nurodyta mokėjimo suma atitinka visų mokėjimo operacijų sumą. |
| Atleidimo nuo mokesčių skaičiavimas | Šia taisykle tikrinama, ar apskaičiuotos sumos suma ir mokesčio eilučių atleidimo nuo mokesčių suma yra lygi pradinei apskaičiuotai sumai. |
| Įkainiai su įskaičiuotu mokesčiu | Šia taisykle tikrinama, ar vėliavėlė **Mokestis įtrauktas į kainą** yra nuosekli operacijų antraštėje ir mokesčio operacijose. |
| Operacija nėra tuščia | Šia taisykle tikrinama, ar operacijoje yra eilučių ir ar bent viena eilutė nėra anuliuota. |
| Nepriemoka / permoka | Šia taisykle tikrinama, ar bendros sumos ir mokėjimo sumos skirtumas neviršija didžiausios nepriemokos / permokos konfigūracijos. |

### <a name="transaction-line-validation-rules"></a>Operacijos eilutės tikrinimo taisyklės

Toliau esančioje lentelėje pateikiamos operacijų eilučių tikrinimo taisyklės, kurios tikrinamos pagal mažmeninės prekybos operacijų eilučių informaciją prieš tas operacijas perduodant į išrašų registravimą.

| Taisyklė | Aprašymas |
|-------|-------------|
| Brūkšninis kodas | Šia taisyklė tikrinama, ar duomenų bazėje yra visi prekės brūkšniniai kodai, naudojami operacijos eilutėse. |
| Mokesčio eilutės | Šia taisykle tikrinama, ar apskaičiuotos sumos suma ir mokesčio eilučių atleidimo nuo mokesčių suma yra lygi pradinei apskaičiuotai sumai. |
| Dovanų kortelės grąžinimai | Šia taisykle tikrinama, ar operacijoje nėra dovanų kortelių grąžinimų. |
| Prekės variantas | Šia taisyklė tikrinama, ar duomenų bazėje yra visos prekės ir visi variantai, naudojami operacijos eilutėse. |
| Eilutės nuolaida | Šia taisykle tikrinama, ar eilutės nuolaidos suma atitinka nuolaidos operacijų sumą. |
| Eilutės mokestis | Šia taisykle tikrinama, ar eilutės mokesčio suma atitinka mokesčio operacijų sumą. |
| Neigiama kaina | Šia taisykle tikrinama, ar operacijų eilutėse nėra naudojamos neigiamos kainos. |
| Kontroliuojamos serijos numerio | Šia taisykle tikrinama, ar serijos numerio kontroliuojamų prekių operacijų eilutėje yra serijos numeris. |
| Serijos numerio dimensija | Šia taisykle tikrinama, ar serijos numeris pateikiamas, jei prekės serijos numerio dimensija neaktyvi. |
| Ženklų prieštaravimas | Šia taisykle tikrinama, ar kiekio ir grynosios sumos ženklai yra tokie patys visose operacijų eilutėse. |
| Atleidimas nuo mokesčio | Šia taisykle tikrinama, ar eilutės prekės kainos suma ir atleidimo nuo mokesčių suma yra lygi pradinei kainai. |
| Mokesčių grupės priskyrimas | Šia taisykle tikrinama, ar PVM grupės ir prekės mokesčių grupės derinys sukuria tinkamą mokesčių sankirtą. |
| Matavimo vieneto konvertavimai | Šia taisykle tikrinama, ar visų eilučių matavimo vienetas yra tinkamai konvertuojamas į atsargų matavimo vienetą. |

## <a name="enable-the-store-transaction-validation-process"></a>Įjungti parduotuvės operacijų tikrinimo procesą

Sukonfigūruokite, kad užduotis **Tikrinti parduotuvės operacijas** būtų paleidžiama periodiškai „Commerce“ būstinėje (**„Retail“ ir „Commerce“ \> „Retail“ ir „Commerce“ IT \> EKA registravimas**). Paketinė užduotis planuojama atsižvelgiant į parduotuvės organizacijos hierarchiją. Rekomenduojame sukonfigūruoti šį paketinį vykdymą, kad jis būtų vykdomas tuo pačiu dažniu kaip iš jūsų paketinės užduotys **P užduotis** ir **Operacijų išrašų duomenų skaičiavimas**.

## <a name="results-of-the-validation-process"></a>Tikrinimo proceso rezultatai

Paketinio vykdymo **Tikrinti parduotuvės operacijas** rezultatus galima peržiūrėti kiekvienoje mažmeninės prekybos parduotuvės operacijoje. Operacijos įrašo lauko **Tikrinimo būsena** reikšmė nustatyta kaip **Sėkmingai**, **Klaida** arba **Jokia**. Lauke **Paskutinio tikrinimo laikas** nurodoma paskutinio tikrinimo vykdymo data.

Šioje lentelėje aprašomos visos tikrinimo būsenos.

| Tikrinimo būsena | Aprašymas |
|-------------------|-------------|
| Sėkmingai | Atitiko visas įjungtas tikrinimo taisykles. |
| Klaida | Pagal įjungta tikrinimo taisyklę buvo nustatyta klaida. Daugiau informacijos apie klaidą galite peržiūrėti veiksmų srityje pasirinkdami **Tikrinimo klaidos**. |
| Jokia | Operacijos tipui nereikia taikyti tikrinimo taisyklių. |

![Parduotuvės operacijų puslapis, kuriame rodomas tikrinimo būsenos laukas ir tikrinimo klaidų mygtukas.](./media/valid-checker-validation-status-errors.png)

Tik operacijos, kurių tikrinimo būsena yra **Sėkmingai**, bus įtrauktos į operacijų išrašus. Norėdami peržiūrėti operacijas, kurių būsena yra **Klaida**, peržiūrėkite darbo srityje **Parduotuvės finansai** esančią plytelę **Atsiskaitymo grynaisiais tikrinimo triktys**.

![Darbo srityje Parduotuvės finansai esančios plytelės.](./media/valid-checker-cash-carry-validation-failures.png)

Daugiau informacijos apie tai, kaip taisyti atsiskaitymo grynaisiais pinigais tikrinimo triktis, žr. [Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas](edit-cash-trans.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
