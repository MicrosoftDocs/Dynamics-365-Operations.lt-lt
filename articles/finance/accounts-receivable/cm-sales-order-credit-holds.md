---
title: Pardavimo užsakymų kredito sulaikymai
description: Šioje temoje aprašoma taisyklių, naudojamų pardavimo užsakymų kredito sulaikymui, sąranka.
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 39f053404348b57de0ad623869ebd7c6cc7a150b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228202"
---
# <a name="credit-holds-for-sales-orders"></a>Pardavimo užsakymų kredito sulaikymai
[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma taisyklių, naudojamų pardavimo užsakymų kredito sulaikymui, sąranka. Kredito valdymo blokavimo taisyklės gali būti taikomos atskiram klientui arba klientų grupei. Blokavimo taisyklės apibrėžia atsakymus esant šioms aplinkybėms:

1. Pradelstų dienų skaičius
2. Sąskaitos būsena
3. Mokėjimo sąlygos
4. Kredito limitas nebegalioja
5. Laiku nesumokėta suma
6. Pardavimo užsakymo suma
7. Išnaudoto kredito turima dalis

Be to, yra du parametrai, kurie valdo papildomus scenarijus, blokuojančius pardavimo užsakymą.

1. Mokėjimo sąlygų pakeitimai
2. Sudengimo nuolaidų pakeitimai

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Blokavimo taisyklių ir pašalinimo taisyklių nustatymas

Kai klientas inicijuoja pardavimo operaciją, pardavimo užsakymo informacija peržiūrima pagal blokavimo taisyklių, pagal kurias priimamas sprendimas, ar pratęsti kliento kreditą ir leisti toliau vykdyti pardavimą, rinkinį. Taip pat galite apibrėžti išimtis, kurios nepaisys blokavimo taisyklių ir leis apdoroti pardavimo užsakymą. Galite nustatyti blokavimo taisykles ir pašalinimo taisykles puslapyje **Kredito valdymas > Sąranka > Kredito valdymo sąranka > Blokavimo taisyklės**.

### <a name="days-overdue"></a>Pradelstos dienos

Atidarykite skirtuką **Pradelstos dienos**, jei blokavimo taisyklė taikoma klientui su viena ar keliomis SF, kurios buvo pradelstos tam tikrą dienų skaičių.
1. Pasirinkite klientų, kuriems ši taisyklė **Galioja**, intervalą.
   - Pasirinkite **Lentelė**, jei taisyklė taikoma konkrečiam klientui.
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų grupės lygiu. 
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams.
2. Nurodę intervalą, turite nurodyti **Sąskaita / grupė**, kuri bus naudojama intervale.
   - Pasirinkus intervalą **Lentelė**, peržvalgoje bus rodomas pasirinktinų klientų sąrašas. 
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų kredito grupei.
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams. 
3. Pasirinkite **Rizikos grupė**, norėdami naudoti kriterijus, kad galėtumėte taikyti kreditų valdymo sulaikymą klientams, kurie sugrupuoti pagal bendrą veiksnių rinkinį, pavyzdžiui, jų „Dun and Bradstreet“ įvertinimą, metų skaičių, kurį jie vykdo verslą, laiką, kurį jie yra jūsų klientai, ir t. t.  
4. Pasirinkti taisyklės, kurią nustatote, tipą. Parinktis **Blokavimas** sukurs taisyklę, kuri blokuoja užsakymą. Parinktis **Pašalinimas** sukurs taisyklę, kuri pašalins kitą taisyklę, kad neblokuotų užsakymo. 
5. Pasirinkite **Vertės tipas**. Numatytasis įrašas yra fiksuotas dienų skaičius. Jei kuriate pašalinimą, galite nurodyti fiksuotą dienų skaičių arba sumą. 
6. Įveskite **Pradelstos** dienų skaičių, kuris bus leistinas pasirinktai blokavimo taisyklei prieš užsakymo pateikimą į kreditų valdymo sulaikymą peržiūrai. Pradelstų dienų skaičius nurodo papildomą atidėjimo dienų skaičių, kuris įtraukiamas į dienų po mokėjimo termino datos skaičių, kuris gali būti taikomas SF, kol ji pradedama laikyti kaip pradelsta. Jei **Vertės tipas** nurodėte kaip pašalinimo sumą, tada įveskite tos sumos sumą ir valiutą.

### <a name="accounts-status"></a>Sąskaitos būsena

Atidaryti skirtuką **Sąskaitos būsena**, jei blokavimo taisyklė taikoma klientui su pasirinkta sąskaitos būsena.
1. Pasirinkti taisyklės, kurią nustatote, tipą.  **Blokavimas** sukurs taisyklę, kuri blokuoja užsakymą. **Pašalinimas** sukurs taisyklę, kuri pašalins kitą taisyklę, kad neblokuotų užsakymo. 
2. Pasirinkite **Sąskaitos būsena**, pagal kurią taisyklė bus taikoma pardavimo užsakymui sulaikyti arba pašalinti.

### <a name="terms-of-payment"></a>Mokėjimo sąlygos

Pasirinkite **Mokėjimo sąlygos**, jei blokavimo taisyklė taikoma pasirinktai mokėjimo sąlygai.
1. Pasirinkti taisyklės, kurią nustatote, tipą.  **Blokavimas** sukurs taisyklę, kuri blokuoja užsakymą. **Pašalinimas** sukurs taisyklę, kuri pašalins kitą taisyklę, kad neblokuotų užsakymo. 
2. Pasirinkite **Mokėjimo sąlygos**, pagal kurią taisyklė bus taikoma pardavimo užsakymui sulaikyti arba pašalinti.

### <a name="credit-limit-expired"></a>Kredito limitas nebegalioja

Atidarykite skirtuką **Kredito limito baigėsi**, jei blokavimo taisyklė taikoma klientams, kurių kredito limitas yra pasibaigęs.
1. Pasirinkite klientų, kuriems ši taisyklė **Galioja**, intervalą.
   - Pasirinkite **Lentelė**, jei taisyklė taikoma konkrečiam klientui.
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų grupės lygiu. 
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams.
2. Nurodę intervalą, turite nurodyti **Sąskaita / grupė**, naudojamą intervale.
   - Pasirinkus intervalą **Lentelė**, peržvalgoje bus rodomas pasirinktinų klientų sąrašas. 
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų kreditų valdymo grupei.
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams. 
3. Pasirinkite **Rizikos grupė**, kad galėtumėte toliau riboti klientų, kurie bus įtraukti į kreditų valdymo sulaikymą, sąrašą. 
4. Pasirinkti taisyklės, kurią nustatote, tipą. 
   - Pasirinkite **Blokavimas**, kad sukurtumėte taisyklę, kuri blokuoja užsakymą. 
   - Pasirinkite **Pašalinimas**, kad sukurtumėte taisyklę, kuri pašalins kitą taisyklę, kad neblokuotų užsakymo. 
5. Pasirinktai blokavimo taisyklei įveskite **Kredito limito galiojimo dienos** prieš užsakymui pritaikydami kreditų valdymo sulaikymą. Pradelstų dienų skaičius nurodo papildomas atidėjimo dienas, kurios pridedamos prie pasibaigusio kredito limito dienų skaičiaus.

### <a name="overdue-amount"></a>Laiku nesumokėta suma

Atidaryti skirtuką **Pradelsta suma**, jei blokavimo taisyklė taikoma klientams, turintiems pradelstų sumų.
1. Pasirinkite klientų, kuriems ši taisyklė **Galioja**, intervalą.
   - Pasirinkite **Lentelė**, jei taisyklė taikoma konkrečiam klientui.
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų grupės lygiu. 
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams.
2. Nurodę intervalą, turite nurodyti **Sąskaita / grupė**, naudojamą intervale.
   - Pasirinkus intervalą **Lentelė**, peržvalgoje bus rodoma klientų peržvalga. 
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų kreditų valdymo grupei.
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams. 
3. Pasirinkite **Rizikos grupė**, jei norite toliau riboti klientų, kurie įtraukiami į kreditų valdymo sulaikymą, sąrašą. 
4. Pasirinkti taisyklės, kurią nustatote, tipą. 
   - Pasirinkite **Blokavimas**, kad sukurtumėte taisyklę, kuri blokuoja užsakymą. 
   - Pasirinkite **Pašalinimas**, kad sukurtumėte taisyklę, kuri pašalins kitą taisyklę, kad neblokuotų užsakymo. 
5. Pasirinktai blokavimo taisyklei įveskite **Pradelsta suma** prieš užsakymo pateikimą į kredito valdymo sulaikymą peržiūrai. 
6. Pasirinkite **Vertės tipas**, kuris nurodo vertės tipą, kuris bus taip pat bus naudojamas siekiant patikrinti, kiek kredito limito išnaudota. Blokavimo taisyklei reikia nurodyti procentus, o pašalinimui – fiksuotą sumą arba procentus. Ribinė vertė yra susijusi su kredito limitu.
7. Pasirinktai taisyklei įveskite **Kredito limito ribinė vertė** prieš klientą įtraukiant į kreditų valdymo sulaikymą. Tai gali būti suma arba procentas, pagrįstas vertės tipu pagal pasirinktą vertės tipą.
8. Taisyklė patikrina, ar viršijama **Pradelsta suma** ir ar viršijama **Kredito limito ribinė vertė**. 

### <a name="sales-order"></a>Pardavimo užsakymas 

Pasirinkite **Pardavimo užsakymas**, jei blokavimo taisyklė taikoma pardavimo užsakymo vertei.
1. Pasirinkite klientų, kuriems ši taisyklė **Galioja**, intervalą.
   - Pasirinkite **Lentelė**, jei taisyklė taikoma konkrečiam klientui.
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų grupės lygiu. 
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams.
2. Nurodę intervalą, turite nurodyti **Sąskaita / grupė**, naudojamą intervale.
   - Pasirinkus intervalą **Lentelė**, peržvalgoje bus rodoma klientų peržvalga. 
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų kreditų valdymo grupei.
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams. 
3. Pasirinkite **Rizikos grupė**, jei norite toliau riboti klientų, kurie įtraukiami į kreditų valdymo sulaikymą, sąrašą. 
4. Pasirinkti taisyklės, kurią nustatote, tipą.  
   - Pasirinkite **Blokavimas**, kad sukurtumėte taisyklę, kuri blokuoja užsakymą. 
   - Pasirinkite **Pašalinimas**, kad sukurtumėte taisyklę, kuri pašalins kitą taisyklę, kad neblokuotų užsakymo. 
5. Pasirinktai blokavimo taisyklei įveskite **Pardavimo užsakymo suma** prieš užsakymo pateikimą į kredito valdymo sulaikymą. 

Pardavimo užsakymo taisyklėje yra papildomas parametras, kuris nepaiso visų kitų taisyklių. Norėdami sukurti pašalinimą, kuris išleis pardavimo užsakymą, neatsižvelgdamas į jokias kitas taisykles, pasirinkite žymės langelį **Išleisti pardavimo užsakymą**, esantį pašalinimo eilutėje.

### <a name="credit-limit-used"></a>Panaudotas kredito limitas

Pasirinkite **Išnaudotas kredito limitas**, jei blokavimo taisyklė taikoma kliento panaudotai kredito limito sumai.
1. Pasirinkite klientų, kuriems ši taisyklė **Galioja**, intervalą.
   - Pasirinkite **Lentelė**, jei taisyklė taikoma konkrečiam klientui.
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų grupės lygiu. 
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams.
2. Nurodę intervalą, turite nurodyti **Sąskaita / grupė**, naudojamą intervale.
   - Pasirinkus intervalą **Lentelė**, peržvalgoje bus rodoma klientų peržvalga. 
   - Pasirinkite **Grupė**, jei taisyklė taikoma klientų kreditų valdymo grupei.
   - Pasirinkite **Visi**, jei taisyklė taikoma visiems klientams. 
3. Pasirinkite **Rizikos grupė**, jei norite toliau riboti klientų, kurie įtraukiami į kreditų valdymo sulaikymą, sąrašą. 
4. Pasirinkti taisyklės, kurią nustatote, tipą.
   - Pasirinkite **Blokavimas**, kad sukurtumėte taisyklę, kuri blokuoja užsakymą. 
   - Pasirinkite **Pašalinimas**, kad sukurtumėte taisyklę, kuri pašalins kitą taisyklę, kad neblokuotų užsakymo. 
5. Pasirinkite **Likusi ribinė vertė**, kuri apibrėžia kredito limito procentą, kurį pasiekus užblokuojamas pardavimo užsakymas. Jei užsakymo vertė padidina kredito limito, išnaudoto daugiau nei minėtas procentas, sumą, užsakymas bus sulaikytas. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Pardavimo užsakymo sulaikymas pagal kitus kriterijus
  
### <a name="rank-payment-terms"></a>Rūšiuoti mokėjimo sąlygas  

Galite priverstinai vykdyti kreditų valdymo taisykles, kai pakeičiamos mokėjimo sąlygos. Turite reitinguoti mokėjimo sąlygas ir priskirti joms reitingavimo vertę. Jei užsakyme mokėjimo sąlygas pakeičiate į mokėjimo sąlygas, kurios įvertintos aukščiau nei senos mokėjimo sąlygos, užsakymas siunčiamas kredito valdytojui, kad patvirtintų.

Galite nustatyti mokėjimo sąlygų reitingus puslapyje **Kreditų valdymas > Sąranka > Kreditų valdymo sąranka > Mokėjimų sąlygų reitingavimas**.

1. Lauke **Mokėjimo sąlygos** pasirinkite reitinguotinas mokėjimo sąlygas; pasirinkus sąlygą, aprašymas bus rodomas lauke **Aprašymas**.
2. Pasirinkite sąlygos reitingą lauke **Reitingas**. Vertės yra susijusios tarpusavyje, kad galėtumėte naudoti 1, 2, 3 arba 10, 20, 30. Taip pat galite naudoti tokią pačią vertę daugumai mokėjimo sąlygų, kad kredito tikrinimas suaktyvintų tik vieną ar dvi mokėjimo sąlygas.

### <a name="rank-settlement-discounts"></a>Rūšiuoti atsiskaitymui taikomas nuolaidas   

Galite priverstinai vykdyti kreditų valdymo taisykles, kai pakeičiamos sudengimo nuolaidos. Turite reitinguoti sudengimo nuolaidas ir priskirti joms reitingavimo vertę. Jei užsakyme sudengimo nuolaidas pakeičiate į sudengimo nuolaidas, kurios įvertintos aukščiau nei senos sudengimo nuolaidos, užsakymas siunčiamas kredito valdytojui, kad patvirtintų.

Galite nustatyti mokėjimo sąlygų reitingus puslapyje **Kreditų valdymas > Sąranka > Kreditų valdymo sąranka > Sudengimo nuolaidų reitingavimas**.

1. Pasirinkite **Mokėjimo nuolaida**, kurią norite reitinguoti. Bus rodomas **Sudengimo nuolaida** aprašymas.
2. Pasirinkite **Reitingas** vertę. Vertės yra susijusios tarpusavyje, kad galėtumėte naudoti 1, 2, 3 arba 10, 20, 30. Taip pat galite naudoti tokią pačią vertę daugumai sudengimo nuolaidų, kad kredito tikrinimas suaktyvintų tik vieną ar dvi sudengimo nuolaidas.

## <a name="sequence-the-application-of-rules"></a>Taisyklių taikymo seka

Taisyklės vykdomos konkrečiam užsakymui, kurį pakeičiate, kad atitiktų jūsų organizacijos poreikius. 

- Vienas pardavimo užsakymo pašalinimo taisyklių egzempliorius leidžia nepaisyti visų taisyklių, kurios gali blokuoti pardavimo užsakymą. Sukurkite pardavimo užsakymo pašalinimo taisyklę ir pažymėkite parinktį **Išleisti pardavimo užsakymą**. Užsakymas nebus sulaikytas, jei ši pašalinimo taisyklė yra teisinga, ir kitos taisyklės nebus patikrintos.
- Blokavimo taisyklės gali sulaikyti užsakymą.
- Pašalinimo taisyklės vykdomos po blokavimo taisyklių. Pašalinimo taisyklės turės įtakos tik taisyklei, kuriai jos apibrėžtos. 
- Blokavimo ir pašalinimo taisyklės vykdomos Lentelėje, tada Grupėje ir galiausiai Visi. Dėl tokios apdorojimo tvarkos, įmanoma turėti blokavimo taisyklę Visi lygiu, kuri nebus vykdoma, nes Lentelėje arba Grupėje vykdoma pašalinimo taisyklė.
- Pašalinimai paiso blokavimo taisyklės, jei yra tame pačiame lygyje. Pavyzdžiui, pašalinimo taisyklė grupės lygyje paisys blokavimo taisyklės grupės lygyje. Turėsite nustatyti pašalinimus Visi lygiu, išskyrus, kaip nurodyta pirmiau, vienam pardavimo užsakymo pašalinimo taisyklės egzemplioriui. 

Taisyklės **Išnaudotas kredito limitas** elgsena keisis pagal parametro **Pardavimo užsakymo kredito limito tikrinimas** parametrus, kurie yra Kredito ir surinkimo parametro formoje.
- Jei parametras nustatytas kaip Ne, išnaudoto kredito limito taisyklė nebus vykdoma.
- Jei parametras nustatytas kaip Taip ir **Pranešti, kai viršijamas kredito limitas** nustatytas, kad įspėtų, gausite įspėjimą, kai bus viršijamas kredito limitas. **Išnaudotas kredito limitas** taisyklės bus vykdomos, kad būtų nustatyta, ar yra taisyklių, kurias norite vykdyti. Tačiau šiam scenarijui paprastai nepridėsite jokių taisyklių.
- Jei parametras nustatytas kaip Taip, o **Pranešti, kai viršijamas kredito limitas** nustatytas kaip klaida, kredito limitas bus patikrintas, o užsakymas bus sulaikytas, jei viršijamas kredito limitas. Be to, **Išnaudotas kredito limitas** taisyklės bus vykdomos, kad būtų nustatyta, ar yra papildomų taisyklių, kurias reikėtų vykdyti. Klaidos pranešimas nebus nerodomas; bus rodoma blokavimo priežastis **Viršytas kredito limitas**. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Parametrai, kurie keičiasi pagal užsakymo sulaikymo būdą

Užsakymai gali būti pašalinti iš kreditų valdymo, net jei jau yra taisyklės. 

- Jei parametrus **Pašalinti klientą iš kreditų valdymo**, esančius „FastTab“ **Visi klientai > Pasirinkti klientą > Kreditas ir surinkimas**, nustatote kaip **Taip**, nebus apdorojami jokie šio kliento užsakymai
- Jei **Pašalinti iš kreditų valdymo** vertę **pardavimo užsakymo antraštėje**, esančioje **Kredito valdymo „fast tab“**, nustatote kaip **Taip**, nebus apdorojamos kreditų valdymo taisyklės. Šį parametrą gali nustatyti tik kreditų valdininkas arba kreditų vadovas.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Sulaikytų užsakymų apdorojimas naudojant kreditų valdymo sulaikymo sąrašą

Kreditų valdymo sulaikymo sąrašas leidžia kreditų vadovams peržiūrėti visus pirkimo užsakymus, kurie yra sulaikyti, ir pašalinti sulaikymus, kai kredito problemos pašalintos. Puslapyje **Kreditų valdymo sulaikymo sąrašas** rodomi visi sulaikyti pardavimo užsakymai. Sąrašą galite peržiūrėti puslapyje **Visi kredito sulaikymai** (**Kreditų valdymas > Kreditų valdymo sulaikymo sąrašas > Visi kredito sulaikymai**).
Pardavimo užsakymai iš visų juridinių asmenų siunčiami į tą patį kreditų valdymo sulaikymo sąrašą, suteikiant centralizuotą visų operacijų, kurioms reikia skirti dėmesį, rodinį. Vartotojas matys tik tą juridinių asmenų informaciją, prie kurios turi prieigą.

Pardavimo užsakymas gali būti įtraukiamas į sulaikymo sąrašą dėl tokių priežasčių.
1. Klientas turi SF, kurią vėluoja apmokėti nustatytą dienų skaičių. 
2. Užsakymas turi konkrečią sąskaitos būseną.
3. Užsakymui nustatytos konkrečios mokėjimo sąlygos.
4. Kliento kredito limitas išnaudotas.
5. Klientas vėluoja sumokėti sumą ir išnaudojo nurodytą kredito limito procentą.
6. Pardavimo užsakymas viršija konkrečią sumą.
7. Klientas viršijo konkrečią savo kredito limito procentinę dalį.
8. Mokėjimo sąlygos skiriasi nuo numatytųjų kliento mokėjimo sąlygų.
9. Sudengimo nuolaidos skiriasi nuo numatytosios kliento sudengimo nuolaidos.

Blokavimo priežastis rodoma kiekvienam pardavimo užsakymui sulaikymo sąraše. Jei yra daugiau nei viena sulaikymo priežastis, ji bus rodoma kaip **Kelios**. Norėdami peržiūrėti visas pardavimo užsakymo sulaikymo priežastis, veiksmų srityje eikite į meniu **Blokavimo priežastys**. **Blokavimo priežastys** taip pat galite peržiūrėti „FactBox“.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Užsakymų, esančių sulaikymų sąraše, išleidimas apdorojimui

Kai išanalizavote sulaikymo priežastis ir jas pašalinote, galite išleisti pardavimo užsakymus tolesniam apdorojimui.

1) Sulaikymų sąraše pasirinkite eilutę. Galite išleisti kelis užsakymus pasirinkdami daugiau nei vieną eilutę.
2) Pasirinkite **Išleidimo priežastis** užsakymui, kurį pasirinkote išleisti.  
3) Įveskite **Peržiūros data** kiekvienam užsakymui, kuriuos pasirinkote išleisti.  
4) Veiksmų srityje pasirinkite meniu **Išleisti**, kad išleistumėte užsakymą. Šis meniu bus pasiekiamas tik pasirinkus operacijas. Vartotojui pateikiamos dvi parinktys.
   - Pasirinkti **Su registravimu**, kad būtų pašalintas sulaikymas ir dokumentas užregistruotas naudojant tą patį registravimo procesą, kuris buvo naudojamas, kai dokumentas buvo sulaikytas. Pavyzdžiui, jei pardavimo užsakymo patvirtinimas sulaikytas, pardavimo užsakymo patvirtinimas bus baigtas po išleidimo. Bus rodoma pardavimo užsakymo registravimo forma, leidžianti vartotojui užregistruoti patvirtinimą.
   - Pasirinkite **Be registravimo**, kad pašalintumėte sulaikymą be tolesnio apdorojimo. Pardavimo užsakymą galima registruoti rankiniu būdu.

### <a name="rejecting-orders-in-the-hold-list"></a>Užsakymų sulaikymų sąraše atmetimas
Galite naudoti veiksmų srities meniu **Atmesti**, kad atmestumėte pardavimo užsakymą.
1. Sulaikymų sąraše pasirinkite eilutę. Galite išleisti kelis užsakymus pasirinkdami daugiau nei vieną eilutę.
2. Užsakymas bus pašalintas iš sulaikymo sąrašo, o pardavimo užsakymo antraštė bus atnaujinta, kad būtų rodoma, kad užsakymas buvo atmestas.

### <a name="automatically-releasing-credit-management-holds"></a>Automatinis kreditų valdymo sulaikymų išleidimas
Pardavimo užsakymai patalpinami į sulaikymų sąrašą remiantis blokavimo taisyklėmis. Tačiau kai kurių sulaikymų priežastys laikui bėgant gali pasikeisti, jei pardavimo užsakymas lieka sulaikymų sąraše tam tikrą laikotarpį. Pavyzdžiui, klientas gali apmokėti sąskaitą ir taip atlaisvinti savo kredito limitą. 

Galite naudoti meniu **Įvertinti išleidimui**, jei norite peržiūrėti pardavimo užsakymus sulaikymų sąraše ir automatiškai juos išleisti, jei sulaikymo priežastis buvo pašalinta.
1.  Pasirinkti meniu **Įvertinimas išleidimui**.
2.  Pasirinkite **Apdoroti blokavimo taisykles**, kad peržiūrėtumėte visus pardavimo užsakymus. Pasirinkite **Apdoroti pasirinktų eilučių blokavimo taisykles**, kad peržiūrėtumėte pasirinktas eilutes.
3. Atsiras slankiklis, kad galėtumėte pasirinkti vieną klientą. Palikite klientų išskleidžiamąjį langą blankų visiems klientams. 
4. Spustelėjus Gerai, procesas paleidžiamas fone, o jūs galite tęsti darbą su kitomis užduotimis. Jei pasirinksite paketinį vykdymą prieš spustelėdami Gerai, procesas bus vykdomas pakete, kai spustelėsite Gerai. Gali šiek tiek užtrukti, kol bus apdoroti sulaikymų sąraše esantys užsakymai, todėl naudokite Atnaujinti, kad atnaujintumėte užsakymų būseną. 
5.  Jei blokavimo priežastis nėra taikoma užsakymui, blokavimo priežastis laikoma nebegaliojanti ir daugiau nebematysite žymės langelio šalia priežasties, kai peržiūrėsite blokavimo priežastis.
6.  Jei išvalytos visos blokavimo priežastys, nauja priežastis **Paruošta išleidimui** įtraukiama į blokavimo priežasčių sąrašą. Pardavimo užsakymus galima automatiškai išleisti.
7.  Jei parametras **Automatiškai išleisti** skirtuke **Kreditas ir surinkimas > Sąranka > Kredito ir surinkimo parametrai > Kreditas> Automatinis išleidimas** nustatytas į **Su registravimu**, būsite paraginti registruoti užblokuotam dokumentui naudojant registravimo formą.
8.  Jei parametras **Automatiškai išleisti** skirtuke **Kreditas ir surinkimas > Sąranka > Kredito ir surinkimo parametrai > Kreditas> Automatinis išleidimas** nustatytas į **Be registravimo**, užsakymą turite registruoti rankiniu būdu.

### <a name="credit-management-approval-workflow"></a>Kredito valdymo patvirtinimo darbo eiga

Taip pat galite sukurti **Kreidų valdymo darbo eigos**, kad galėtumėte valdyti sulaikytų kreditų išleidimą. Nustačius darbo eigą puslapyje **Kredito valdymas > Sąranka > Kreditų valdymo darbo eigos**, užsakymai, pažymėti išleidimui arba atmetimui, bus nusiųsti į darbo eigą, kurioje juos pirmiausia reikia patvirtinti, kol jie bus išleisti arba atmesti. 

Jei į savo darbo eigą įtraukiate išleidimo su registravimu arba išleidimo be registravimo užduotis, darbo eigos patvirtinimas taip pat išleis pardavimo užsakymą. Tačiau, jei išleidimo procesas neįvyksta dėl trūkstamos sąrankos informacijos arba kitų priežasčių, turėsite iš naujo iškviesti pardavimo užsakymą iš darbo eigos, ištaisyti problemą ir vėl pateikti užsakymą į darbo eigą.

Jei į darbo eigą neįtraukiate išleidimo su registravimu arba išleidimo be registravimo užduočių, darbo eigos patvirtinimas jums paprasčiausiai leis išleisti pardavimo užsakymą rankiniu būdu, kai patvirtinimas bus baigtas.

### <a name="forced-credit-hold"></a>Priverstinis kredito sulaikymas  
  
Kartais pardavimo užsakymus gali reikėti užblokuoti, net jei užsakymas neatitinka blokavimo taisyklių kriterijų. Pavyzdžiui, kredito vadovui gali būti pranešta apie su kreditu nesusijusią kliento problemą ir jis gali nuspręsti rankiniu būdu sulaikyti užsakymus, kol problema bus išspręsta. Galite rankiniu būdu priverstinai sulaikyti pardavimo užsakymą, jei yra tokia situacija.

1. Atidarykite pardavimo užsakymą, kurį norite sulaikyti.  
2. Pasirinkite **Priverstinai sulaikyti kreditą** skirtuke **Kreditų valdymas** veiksmų srityje **Kreditų valdymas**.
3. Pasirinkite **Priverstinio sulaikymo priežastis**.
4. Spustelėkite **Gerai**. Pardavimo užsakymas bus grąžintas į kreditų valdymo sulaikymo sąrašą.

Be to, galite priverstinai sulaikyti kelis užsakymus eidami į puslapį **Kreditų valdymas> Periodinės užduotys > Priverstinis kredito sulaikymas**. Pavyzdžiui, galite sulaikyti konkretaus kliento pardavimo užsakymus.
1. Pasirinkite **Priverstinio sulaikymo priežastis**. 
2. Spustelėkite **Įtrauktini įrašai**, kad pasirinktumėte sulaikomus pardavimo užsakymus. 
3. Spustelėkite **Gerai**, kad apdorotumėte pasirinktus pardavimo užsakymus.

Pardavimo užsakymai, kurie buvo priverstinai sulaikyti, negali būti apdorojami darbo eigoje.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Užsakymų, kurie buvo įtraukti į kreditų valdymo sulaikymo sąrašą taikant priverstinį kredito sulaikymą, išleidimas
Pardavimo užsakymai, kurie turi priverstinio sulaikymo priežastį, negali būti automatiškai išleisti. Jei pardavimo užsakymas buvo priverstinai sulaikytas ir jūs naudojote procesą, kuris automatiškai išleidžia pardavimo užsakymus, pardavimo užsakymas bus rodomas kaip **Paruoštas išleidimui** ir liks sulaikymo sąraše. Norėdami išleisti užsakymą, turite naudoti meniu **Išleisti**.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Laisvos formos SF, užsakymų ir projektų SF palaikymas kredito valdyme 
Kredito valdymą šiuo metu galima naudoti tik pardavimo užsakymams. Laisvos formos SF, elektroniniai kasos aparatai ir skambučių centro užsakymai naudos laikinus kredito limitus ir draudimą / garantijas, kurias įtraukiate, kad galėtumėte keisti kredito limitą. Jos nenaudos blokavimo taisyklių ir nebus patalpintos sulaikymo sąraše, jei kyla problemų dėl kredito limito.

Projektų SF kredito valdyme nėra palaikomos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]