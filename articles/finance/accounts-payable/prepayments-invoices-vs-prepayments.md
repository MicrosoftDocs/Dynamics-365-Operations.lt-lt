---
title: Išankstinio mokėjimo sąskaitos faktūros ir išankstiniai mokėjimai
description: Šiame straipsnyje aprašomi ir priešingai du metodai, kuriuos organizacijos gali naudoti išankstiniams mokėjimams (išankstiniams mokėjimams).
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f828b93075c134778da280243c0875edf99300
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715835"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Išankstinio mokėjimo sąskaitos faktūros ir išankstiniai mokėjimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi ir priešingai du metodai, kuriuos organizacijos gali naudoti išankstiniams mokėjimams (išankstiniams mokėjimams). Vienas metodas sukuria iš anksto mokamą SF, kuri susieta su pirkimo užsakymu. Naudojant kitą būdą, išankstinio mokėjimo žurnalo kvitai kuriami sukuriant žurnalo įrašus ir pažymint juos kaip išankstinio mokėjimo žurnalo kvitus.

Organizacijos gali tiekėjams išduoti išankstinius mokėjimus (mokėjimus iš anksto) už prekes arba paslaugas prieš šių prekių ar paslaugų užsakymų įvykdymą. Tiekėjams galima išduoti išankstinius mokėjimus dviem būdais. Siekdami sumažinti riziką, išankstinius mokėjimus galite sekti, išankstinį mokėjimą nurodydami pirkimo užsakyme. Naudodami šį būdą turite sukurti išankstinio mokėjimo SF, susietą su pirkimo užsakymu. Šis būdas vadinamas išankstinio mokėjimo SF išrašymu. Organizacijos, kurios nenori išankstinių mokėjimų sekti taip atidžiai arba negauna išankstinio mokėjimo SF iš savo tiekėjo, gali naudoti išankstinio mokėjimo žurnalo kvitus, o ne išankstinio mokėjimo SF išrašymo būdą. Išankstinio mokėjimo žurnalo kvitus galite kurti, sukurdami žurnalo įrašus ir pažymėdami juos kaip išankstinio mokėjimo žurnalo kvitus. Naudodami šį būdą negalite sekti, kurie kurių pirkimo užsakymų išankstiniai mokėjimai tiekėjui yra atliekami. Tačiau galite pažymėti užregistruotą išankstinį mokėjimą sudengti pagal pirkimo užsakymą.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Kada naudoti išankstinio mokėjimo SF išrašymo būdą ir išankstinius mokėjimus

| Išankstinio mokėjimo SF išrašymas                                                                | Išankstiniai mokėjimai                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Nurodykite išankstinio mokėjimo vertę pirkimo užsakyme.                                    | Pirkimo užsakyme išankstinio mokėjimo vertė nenurodyta.                    |
| Išankstinio apmokėjimo sąskaita ir paskutinė sąskaita turi būti publikuotos.                       | Išankstinio apmokėjimo SF registruoti nereikia.                                    |
| Išankstinio mokėjimo įsipareigojimai saugomi išankstinio mokėjimo sąskaitoje, o ne AP sąskaitoje. | Išankstinio mokėjimo įsipareigojimai saugomi AP sąskaitoje.                  |
| Tiekėjo balansas neatspindi išankstinio mokėjimo vertės visos proceso metu.     | Tiekėjo balansas atspindi išankstinio mokėjimo vertę visos proceso metu. |
| Išankstinio mokėjimo SF išrašyti galima tik naudojant mokėtinas sumas.                         | Išankstinius mokėjimus atlikti galima naudojant mokėtinas sumas ir gautinas sumas.    |

## <a name="overview-of-the-prepayment-process"></a>Išankstinio mokėjimo proceso apžvalga
Apskaitos praktikos daugelyje šalių ir regionų reikalauja, kad išankstiniai mokėjimai iš kliento ar pardavėjo nebūtų publikuojami į įprastas santraukų kliento ar pardavėjo ataskaitas. Vietoj to šie išankstiniai apmokėjimai registruojami į specialias DK sąskaitas, skirtas išankstiniams apmokėjimams. Kai prekybos užsakymas ar pirkimo užsakymas yra sukuriami, sąskaita yra išraoma klientui ar pardavėjo. Apmokant SF, išankstinis apmokėjimas ir PVM išankstinio mokėjimo kvitas, esantys išankstinių apmokėjimų DK sąskaitoje, atšaukiami, o SF sumos automatiškai užregistruojamos įprastose suminėse sąskaitose. Atlikite toliau nurodytus veiksmus, norėdami sukurti išankstinį mokėjimą.

1.  Nustatykite išankstinių mokėjimų registravimo šablonus.
2.  Puslapiuose Gautinų sumų parametrai ir Mokėtinų sumų parametrai, esančiuose dalyje **DK ir PVM**, pasirinkite naują registravimo šabloną naudodami parametrą **Registravimo šablonas, skirtas mokėjimo žurnalui, su išankstiniu mokėjimu**.
3.  Kurkite mokėjimo žurnalą ir tada kurkite naują mokėjimą.
4.  Mokėjimą galite pažymėti kaip išankstinį mokėjimą. Jei mokėjimas yra pažymėtas kaip išankstinis mokėjimas, jis yra publikuojamas į buhalterinės knygos sąskaitas, kurios yra nustatomos publikavimo profilyje, kurį nustatėte žingsnyje 1 ir 2. Be to, jei mokėjimas pažymėtas kaip išankstinis mokėjimas, skaičiuojami mokesčiai. Kai kurios vyriausybės prašo, kad mokesčiai būtų sumokėti, kai registruojamas išankstini mokėjimas net ir be sąskaitos.
5.  Užregistruokite išankstinį apmokėjimą.
6.  Pasirinktinai: galite nustatyti išankstinį mokėjimą pagal įsigijimo užsakymą ar pardavimo užsakymą prieš sukurdami sąskaitą. Prekybos užsakyme ar pirkimo užsakymo puslapyje, veiksmų juostoje naudokite **Nustatyti transakcijas**.
7.  Po to, kai tiekėjas pristato prekes arba paslaugas, įrašykite SF. Jei išankstinį mokėjimą sudengiate pagal pirkimo arba pardavimo užsakymą (6 veiksmas), išankstinis mokėjimas yra automatiškai sudengiamas pagal jūsų sukurtą SF. Jei nenustatėte išankstinio mokėjima pagal pirkimo ar pardavimo užsakymą, galite rankiniu būdu nustatyti jį pagal sąskaitą naudodami **Nustatyti transakcijas** kliento ar pardavėjo puslapyje. Tada išankstinio mokėjimo suma yra atšaukiama iš laikinos AP/AR DK sąskaitos. Be to, jei buvo apskaičiuoti mokesčiai, jie bus atšaukti, nes SF pateikiami faktiniai mokesčiai.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Išankstinio mokėjimo SF išrašymo proceso apžvalga
Išankstinio mokėjimo sąskaitos yra bendra verslo praktika. Tiekėjas išduoda išankstinio mokėjimo SF, reikalaudamas pirkimo depozito prieš pirkimo užsakymo vykdymą. Pavyzdžiui, kai kurie pardavėjai prašo išankstinio mokėjimo už tinkintas prekes ar paslaugas. Jei tiekėjas išduoda SF, pagal kurią reikalingas išankstinis mokėjimas, galite naudoti išankstinio mokėjimo SF išrašymo funkciją. Išankstinio mokėjimo vertė gali būti nustatyta prekybos užsakyme, išankstinio mokėjimo sąskaita yra užregistruojama ir mokama ir tuomet išankstinio mokėjimo sąskaita taikoma paskutinei sąskaitai. Atlikite toliau nurodytus veiksmus, norėdami sukurti išankstinį mokėjimą.

1.  Pirkimo agentas kuria, tvirtina ir tada pateikia pirkimo užsakymą, už kurį tiekėjas prašė išankstinio mokėjimo. Išankstinio mokėjimo vertė pirkimo užsakyme nurodoma kaip sutarties dalis.
2.  Tiekėjas pateikia išankstinio mokėjimo SF.
3.  Mokėtinų sumų koordinatorius užregistruoja išankstinio mokėjimo SF pagal pirkimo užsakymą, o tada išankstinio mokėjimo SF yra apmokama.
4.  Tiekėjas siunčia mokėjimo užklausą, nurodytą kaip standartinė tiekėjo SF. Po to, kai tiekėjas pristato prekes arba paslaugas, o susijusios standartines tiekėjo SF yra gautos, mokėtinų sumų koordinatorius taiko išankstinio mokėjimo sumą, kuri jau buvo sudengta pagal standartinę SF.
5.  Mokėtinų sumų koordinatorius moka ir sudengia likusią standartinę SF sumą.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Nustatyti parametrus, siekiant įgalinti išankstinio mokėjimo SF išrašymo procesą
Išankstinio apmokėjimo sąskaita turi būti apibrėžta atsargų registravimo puslapio skirtuke **Pirkimo** **užsakymas** **(Atsargų \> valdymo \> nustatymo \> registravimas**). Registruojant išankstinio apmokėjimo SF, išankstinio mokėjimo sąskaita paprastai bus atnaujinta ir debetuojama. Išankstinio mokėjimo sąskaitos balansas bus atšauktas užregistrus standartinę SF, kuri taikoma išankstinio apmokėjimo SF. Jei nesudengisite išankstinio mokėjimo SF su mokėjimu prieš pritaikę išankstinio mokėjimo SF prie standartinės SF, užregistruotos išankstinio apmokėjimo SF apskaitos įrašai bus atšaukti, kai bus užregistruota standartinė SF.

Korespondentinės sąskaitos mokėtinų sumų sąskaita nurodyta tiekėjo **registravimo** šablone. Norėdami nustatyti numatytąjį registravimo šabloną, spustelėkite Mokėtinų sumų nustatymo mokėtinų sumų parametrai DK ir **skirtuke \> PVM \> registravimo\>šablonas su \> išankstinio mokėjimo tiekėjo** SF.

Išankstinio **apmokėjimo programos** strategija nurodo, ar sistema automatiškai tai taikys sudengtas išankstinio apmokėjimo SF galutinai SF, kuri buvo sukurta rankiniu būdu. SF, sukurtos naudojant duomenų objektą, nebus nuorodos į išankstinio **apmokėjimo programos** strategiją. Turite rankiniu būdu taikyti sudengtas išankstinio apmokėjimo SF SF, kurios sukurtos naudojant duomenų objektą. Norėdami nustatyti strategiją, eikite į **Mokėtinų sumų nustatymo mokėtinų sumų parametrus DK ir \>PVM \> skirtuką \> Išankstinio \> apmokėjimo programos** strategija. Jei **išankstinio apmokėjimo** programos strategijos laukas nustatytas kaip **Automatinis**, išankstinio mokėjimo SF bus automatiškai pažymėta sudengti su galutinėje SF. Jei laukas nustatytas kaip Pranešimas, vaizdinis nurodymas, kad galima naudoti išankstinio apmokėjimo SF, bus **rodomas** sukūrus galutinę SF.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Kurti pirkimo užsakymą, kuriame būtų išankstinio mokėjimo SF informacija
Kai tiekėjas jums nurodo, kad reikalauja išankstinio apmokėjimo už pirkimo užsakyme esančias prekes ir paslaugas, turite nustatyti susijusio pirkimo užsakymo išankstinio apmokėjimo vertę. Eiti į **Mokėtinas \> sumas \> Bendrieji \> pirkimo užsakymai** Visi pirkimo užsakymai ir rasti tiekėjo pirkimo užsakymą. Veiksmų juostoje pasirinkite skirtuką **Įsigijimas**, tada pasirinkite **Išankstinis mokėjimas**. Įveskite informaciją apie išankstinį mokėjimą, įskaitant aprašą, išankstinio mokėjimo vertę, ar išankstinis mokėjimas yra fiksuota suma, ar procentas, ir išankstinio mokėjimo kategorijos ID. 

Atkreipkite dėmesį, kad keli išankstinių apmokėjimų apibrėžimai pirkimo užsakyme yra negalimi. Jei turite leisti kelis išankstinius apmokėjimus pirkimo užsakyme, užregistruokite mokėjimus naudodami mokėjimų žurnalą, o ne išankstinio apmokėjimo SF.

Išankstinis mokėjimas gali būti pašalintas iš pirkimo užsakymo, nebent jūs jau sudengėte mokėjimą pagal užregistruotą išankstinio mokėjimo SF arba užregistrnote standartinę SF. Norėdami pašalinti išankstinio apmokėjimo informaciją iš pirkimo užsakymo, pasirinkite Mokėtinos sumos Bendrieji pirkimo užsakymai **Visi pirkimo užsakymai \> ir \> raskite \> tiekėjo** pirkimo užsakymą. Veiksmų juostoje pasirinkite skirtuką **Įsigijimas**, tada pasirinkite **Pašalinti išankstinį mokėjimą**.

## <a name="create-and-post-a-prepayment-invoice"></a>Publikuoti ir kurti išankstinio mokėjimo sąskaitą
Norėdami įrašyti tiekėjo išankstinio apmokėjimo SF, eikite į tiekėjo SF puslapį, pasirinkdami išankstinio apmokėjimo SF pasirinktį pirkimo užsakymų puslapyje Mokėtinos sumos Bendrieji pirkimo **užsakymai** **Visi** **pirkimo** (**užsakymai \> SF \> skirtukas \> Išankstinio \> apmokėjimo \> SF**). Įveskite informaciją apie išankstinio mokėjimo SF, įskaitant SF numerį. Išankstinio mokėjimo SF kiekių keisti negalima. Jei tiekėjas išrašė SF dalį išankstinio mokėjimo vertės, kuri nurodyta pirkimo užsakyme, sumos, galite atnaujinti vieneto kainą, kad atspindėtų dalinę vertę.

Publikuojant išankstinio mokėjimo sąskaitą, bus naujinamas tiekėjo balansas ir išankstinio mokėjimo sąskaita. Bus **atnaujinta ir** išankstinio apmokėjimo prašymo vertė išankstinio apmokėjimo apibrėžime, kuris yra pirkimo užsakyme. Užregistruoti išankstinio mokėjimo kvito numatytieji finansinės dimensijos įrašai bus paimti iš pirkimo užsakymo antraštės informacijos.

Jei tiekėjo **išankstinio** **mokėjimo** SF funkcijos, kurios yra funkcijų valdymo puslapyje, SF eilutėse užrakinti finansines dimensijas, išankstinio apmokėjimo antraštėje arba eilutėse dimensijų atnaujinti negalima. 

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Registruoti ir sudengti išankstinio mokėjimo SF mokėjimus
Po to išankstinio apmokėjimo SF bus sumokėta iš **mokėjimų žurnalo** puslapio. Norėdami pasiekti mokėjimo žurnalus, spustelėkite **Mokėtinų sumų \> žurnalų \> mokėjimų mokėjimų \> žurnalas**. Užregistrus mokėjimo sudengimą išankstinio mokėjimo SF, bus atnaujinta pirkimo užsakymo išankstinio **apmokėjimo** prašymo likusi vertė.

Prieš registruodami standartinę išankstinio mokėjimo SF SF, galite atšaukti mokėjimo sudengimą iš išankstinio mokėjimo SF. Nepaisant to, prieš registruodami standartinę išankstinio mokėjimo SF SF, galite atšaukti mokėjimo sudengimą iš išankstinio mokėjimo SF.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Registruoti standartinę tiekėjo SF pirkimo užsakymui ir taikyti išankstinio apmokėjimo SF standartinei SF
Įrašykite standartinę iš tiekėjo gautą SF. Kaip šio proceso dalį galite taikyti sudengtą išankstinio apmokėjimo SF tiekėjo SF taip, kad SF vertė būtų sumažinta iki jau sumokėtos sumos. Pritaikę išankstinio apmokėjimo SF tiekėjo SF užtikrinsite, kad bus atšaukti išankstinio mokėjimo SF apskaitos įrašai.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Išankstinio mokėjimo SF prašymas užregistrus standartinę SF
Jeigu pamiršote pritaikyti išankstinį apmokėjimą standartinei tiekėjo SF, registruojant tiekėjo SF, sudengtą išankstinį apmokėjimą bus galima taikyti kitoms šio tiekėjo SF, kurias rasite tiekėjų puslapyje Taikomos mokėtinų **sumų** (**bendrosios \> tiekėjų \> sąskaitos \> visiems \> tiekėjams \> SF**).

## <a name="reversal-of-the-prepayment-application-process"></a>Išankstinio mokėjimo prašymo proceso atšaukimas
Jei norite atšaukti išankstinio apmokėjimo SF sudengimas ar atšaukti jo taikymą iš standartinės SF, pasirinkite veiksmą Atšaukti iš tiekėjų puslapio **mokėtinų** iš **sumų** bendrųjų (**tiekėjų \> visų \> tiekėjų \> SF \> skirtukas \> Atšaukti**). Atšaukę išankstinio apmokėjimo prašymą, jį galite taikyti kitai standartinei SF. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
