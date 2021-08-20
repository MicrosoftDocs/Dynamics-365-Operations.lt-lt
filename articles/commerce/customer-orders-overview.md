---
title: Kliento užsakymai elektroniniame kasos aparate (EKA)
description: Šioje temoje pateikta informacija apie kliento užsakymus elektroniniame kasos aparate (EKA). Kliento užsakymai dar vadinami specialiais užsakymais. Šioje temoje pateikta susijusių parametrų ir operacijų srautų apžvalga.
author: josaw1
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260594"
- intro-internal
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 44beb4515bf0d2f8fc7ad75feb3164bf1c7c2d5737552b1a06ce59c2edcaf8fe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755088"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Kliento užsakymai elektroniniame kasos aparate (EKA)

[!include [banner](includes/banner.md)]

Šioje temoje pateikta informacija apie tai, kaip kurti ir valdyti kliento užsakymus elektroniniame kasos aparate (EKA). Kliento užsakymai gali būti naudojami pardavimams užfiksuoti, kai pirkėjai nori pasiimti produktus vėliau, pasiimti produktus iš kitos vietos arba kad prekės jiems būtų atsiųstos. 

Integruotų kanalų prekyboje dauguma pardavėjų suteikia galimybę kurti klientų užsakymus (arba specialius užsakymus) įvairiems produktų ir vykdymo reikalavimams įvykdyti. Toliau nurodomi įprasti scenarijai.

- Klientas nori, kad produktai būtų pristatyti konkrečią dieną konkrečiu adresu.
- Klientas nori atsiimti produktus parduotuvėje arba vietoje, kuri nėra parduotuvė arba vieta, kurioje klientas tuos produktus nusipirko.
- Parduotuvėje esantis klientas nori užsisakyti produktus šiandien ir vėliau juos paimti iš tos pačios parduotuvės.

Pardavėjai taip pat naudoja kliento užsakymus, norėdami sumažinti prarasto pardavimo kiekius, kuriuos gali lemti atsargų stygius, kadangi prekes galima pristatyti arba atsiimti kitu laiku arba kitoje vietoje.

## <a name="set-up-customer-orders"></a>Kliento užsakymų nustatymas
Prieš pradėdami naudoti kliento užsakymų funkciją EKA, įsitikinkite, kad atlikote visas būtinas konfigūracijas „Commerce Headquarters“.

### <a name="configure-modes-of-delivery"></a>Pristatymo būdų konfigūravimas

Norėdami naudoti kliento užsakymus, turite sukonfigūruoti pristatymo būdus, kuriuos gali naudoti parduotuvės kanalas. Turite apibrėžti bent vieną pristatymo būdą, kurį galima naudoti, kai užsakymo eilutės siunčiamos klientui iš parduotuvės. Taip pat turite apibrėžti bent vieną pristatymo paėmimo būdą, kurį galima naudoti, kai užsakymo eilutės paimamos iš parduotuvės. Pristatymo būdai apibrėžiami „Commerce Headquarters“ puslapyje **Pristatymo būdai**. Daugiau informacijos apie tai, kaip nustatyti „Commerce“ kanalų pristatymo būdus, žr. [Pristatymo būdų apibrėžimas](./configure-call-center-delivery.md#define-delivery-modes).

![Puslapis Pristatymo būdai.](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Įvykdymo grupių nustatymas

Kai kurios parduotuvės ar sandėlių vietos gali neįvykdyti klientų užsakymų. Konfigūruodama įvykdymo grupes, organizacija gali nurodyti, kurios parduotuvės ir sandėlio vietos rodomos kaip parinktys vartotojams, kuriantiems kliento užsakymus EKA. Įvykdymo grupės konfigūruojamos puslapyje **Įvykdymo grupės**. Organizacijos gali sukurti tiek įvykdymo grupių, kiek joms reikia. Nustačiu įgyvendinimo grupę, susiekite ją su parduotuve pasirinkdami **Įgyvendinimo grupės priskyrimas** iš **Nustatyti** skirtuko veiksmų juostoje **Parduotuvės** puslapyje.

„Commerce“ versijoje 10.0.12 ir vėlesnėse, organizacijos gali nustatyti, ar sandėlis arba sandėlio ir parduotuvės deriniai, nustatyti įgyvendinimo grupėse, gali būti naudojami siuntimui, paėmimui ar ir siuntimui, ir paėmimui. Tai leidžia įtraukti lankstumo į verslą siekiant nustatyti, kurie sandėliai gali būti pasirinkti sukuriant kliento užsakymą siunčiamiems objektams pagal parduotuves, kurias galima pasirinkti sukuriant kliento užsakymą paimamiems objektams. Norėdami konfigūruoti šias parinktis, įjunkite **Galimybė nurodyti vietas kaip „Siuntimas“ ar „Paėmimas“ įjungtas įgyvendinimo grupėje** funkciją. Jei sandėlis susietas su įgyvendinimo grupe nėra parduotuvė, jis gali būti konfigūruojamas tik kaip siuntimo vieta. Jo negalima naudoti, kai paėmimo užsakymai yra sukonfigūruoti EKA.

![Puslapis Įvykdymo grupės.](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanalo parametrų konfigūravimas

Kai dirbate su kliento užsakymais EKA, turite atsižvelgti į kai kuriuos parduotuvės kanalo parametrus. Šiuos parametrus galima rasti „Commerce Headquarters“ puslapyje **Parduotuvės**.

- **Sandėlis** – Šis laukas nurodo sandėlį, kuris bus naudojamas mažėjant atsargoms, skirtoms atsiskaitymo grynaisiais pinigais ir kliento paėmimo užsakymais, susietais su šia parduotuve. Kaip geriausią praktiką, skatiname unikalių sandėlių kiekvienam parduotuvės kanalui naudojimą, kad būtų išvengta veiklos logikos nesuderinamumo problemos tarp parduotuvių.
- **Siuntimo sandėlis** – Šis laukas nurodo sandėlį, kuris bus naudojamas mažėjant atsargoms, skirtoms klientų užsakymams, kurie bus išsiųsti iš pasirinktos parduotuvės. Jei jūsų aplinkoje įgalinta funkcija **Galimybė nurodyti vietas kaip „Siunčiamos” arba „Paėmimo” įgalinta Įvykdymo grupėje**, EKA vartotojai gali pasirinkti konkretų sandėlį, į kurį siųsti iš EKA, vietoj to, kad pasirinkti parduotuvę, iš kurios siųsti. Todėl, kai ši funkcija yra įgalinta, siuntimo sandėlis yra nebenaudojamas, kadangi vartotojas užsakymo kūrimo metu išrinks konkretų sandėlį, iš kurio bus siunčiamas tas užsakymas.
- **Įvykdymo grupės priskyrimas** – pasirinkite šį mygtuką (veiksmų srities skirtuke **Nustatymas**), norėdami susieti įvykdymo grupes, kuriomis nurodomos paėmimo vietų ar siuntimo kilmės parinktys, kai klientų užsakymai sukurti EKA.
- **Naudoti paskirties vietos mokesčius** – ši parinktis nurodo, ar siuntimo adresas naudojamas mokesčių grupei, taikomai užsakymo eilutėms, siunčiamoms kliento adresu, nustatyti.
- **Naudoti kliento mokesčius** – ši parinktis nurodo, ar mokesčių grupė, apibrėžta kliento pristatymo adresui, naudojama apmokestinti klientų užsakymus, sukurtus EKA, siuntimui į kliento namus.

![Parduotuvės kanalo nustatymas puslapyje Parduotuvės.](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Kliento užsakymo parametrų nustatymas

Prieš pradėdami kurti kliento užsakymus EKA, turite sukonfigūruoti tinkamus parametrus „Commerce Headquarters“. Šiuos parametrus galima rasti puslapio **„Commerce” parametrai** skirtuke **Kliento užsakymai**.

- **Numatytasis užsakymo tipas** – galite nurodyti užsakymo tipą, kuris pagal numatytuosius nustatymus priskiriamas klientų užsakymams, sukurtiems EKA. Šie klientų užsakymai gali būti pardavimo arba pasiūlymo užsakymai. Nepaisant numatytojo užsakymo tipo, vartotojai vis tiek gali kurti pardavimo ir kliento užsakymus EKA.
- **Numatytasis įmokos procentas** – nurodykite visos užsakymo sumos procentą, kurį klientas turi sumokėti kaip įmoką, kad būtų galima patvirtinti užsakymą. Priklausomai nuo parduotuvės partnerių teisių, jie gali pakeisti sumą naudodami operaciją **Įmokos keitimas** EKA, jei ši operacija sukonfigūruota operacijos ekrano išdėstymui.
- **Paėmimo pristatymo būdas** – nurodykite pristatymo būdą, kuris turėtų būti taikomas pardavimo užsakymų eilutėms, sukonfigūruotoms paėmimui EKA.
- **Išsivežimo pristatymo būdas** – nurodykite pristatymo būdą, kuris turėtų būti taikomas pardavimo užsakymų eilutėms, kurios laikomos išsivežimo užsakymo eilutėmis, kai sukuriamas mišrus krepšelis, kuriame kai kurios eilutės bus paimtos ar išsiųstos, o kitas eilutes klientas išsiveš nedelsdamas.
- **Atšaukimo mokesčio procentas** – jei atšaukus kliento užsakymą turėtų būti taikomas mokestis, nurodykite to mokesčio sumą.
- **Atšaukimo mokesčio kodas** – nurodykite gautinų sumų mokesčio kodą, kuris turėtų būti naudojamas, kai atšauktiems kliento užsakymams EKA taikomas atšaukimo mokestis. Mokesčio kodas apibrėžia atšaukimo mokesčio finansų registravimo logiką.
- **Siuntimo mokesčio kodas** – jei parinktis **Naudoti išplėstinius automatinius mokesčius** nustatyta į **Taip**, šis parametro nustatymas neturi jokios įtakos. Jei parinktis nustatyta į **Ne**, vartotojai bus raginami rankiniu būdu įvesti siuntimo mokestį, kai jie sukurs kliento užsakymus EKA. Naudokite šį parametrą norėdami susieti gautinų sumų mokesčio kodą, kuris bus taikomas užsakymams, kai vartotojai įves siuntimo mokestį. Mokesčio kodas apibrėžia siuntimo mokesčio finansų registravimo logiką.
- **Naudoti išplėstinius automatinius mokesčius** – nustatykite šią parinktį į **Taip**, norėdami naudoti sistemos apskaičiuotus automatinius mokesčius, kai klientų užsakymai kuriami EKA. Šie automatiniai mokesčiai gali būti naudojami apskaičiuojant siuntimo mokesčius ar kitus užsakymo ar prekės mokesčius. Norėdami gauti daugiau informacijos apie tai, kaip nustatyti ir naudoti išplėstinius automatinius mokesčius, žr. [Daugiakanaliai išplėstiniai automatiniai mokesčiai](./omni-auto-charges.md).

![Skirtukas Kliento užsakymai „Commerce” parametrų puslapyje.](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Operacijų ekrano išdėstymo EKA naujinimas

Įsitikinkite, kad EKA [ekrano išdėstymas](./pos-screen-layouts.md) sukonfigūruotas palaikyti klientų užsakymų kūrimą bei valdymą ir kad visos reikalingos EKA operacijos yra sukonfigūruotos. Toliau nurodytos kelios EKA operacijos, rekomenduojamos siekiant tinkamai palaikyti klientų užsakymų kūrimą ir valdymą.
- **Siųsti visus produktus** – ši operacija naudojama norint nurodyti, kad visos operacijos krepšelio eilutės bus išsiųstos į paskirties vietą.
- **Siųsti pasirinktus produktus** – ši operacija naudojama norint nurodyti, kad pasirinktos operacijos krepšelio eilutės bus išsiųstos į paskirties vietą.
- **Paimti visus produktus** – ši operacija naudojama norint nurodyti, kad visos operacijos krepšelio eilutės bus paimtos iš pasirinktos parduotuvės.
- **Paimti pasirinktus produktus** – ši operacija naudojama norint nurodyti, kad pasirinktos operacijos krepšelio eilutės bus paimtos iš pasirinktos parduotuvės.
- **Išsivežti visus produktus** – ši operacija naudojama norint nurodyti, kad visos operacijos krepšelio eilutės bus išsivežtos. Jei ši operacija naudojama EKA, kliento užsakymas bus konvertuotas į atsiskaitymo grynaisiais ir išsivežimo operaciją.
- **Išsivežti pasirinktus produktus** – ši operacija naudojama norint nurodyti, kad pasirinktas operacijos krepšelio eilutes klientas išsiveš pirkimo metu. Ši operacija naudinga tik [mišraus užsakymo](./hybrid-customer-orders.md) atveju.
- **Atšaukti užsakymą** – ši operacija naudojama klientų užsakymams ieškoti ir gauti, kad EKA vartotojai galėtų redaguoti, atšaukti ar atlikti su jais susijusias operacijas pagal poreikį.
- **Keisti pristatymo būdą** – ši operacija gali būti naudojama norint greitai pakeisti eilučių, kurios jau sukonfigūruotos siuntimui, pristatymo būdą, nereikalaujant, kad vartotojai vėl pereitų srautus „Siųsti visus produktus“ arba „Siųsti pasirinktus produktus“.
- **Įmokos keitimas** – šią operaciją galima naudoti norint pakeisti įmokos sumą, kurią klientas sumokės už pasirinktą kliento užsakymą.

![Operacijos EKA operacijų ekrane.](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>Darbas su kliento užsakymais POS

> [!NOTE]
> Pajamų atpažinimo funkcija šiuo metu palaikoma „Commerce“ kanaluose (e-komercijoje, POS, skambučių centruose). Objektai sukonfigūruoti su pajamų atpažinimu neturėtų būti įtraukti į užsakymus sukurtus „Commerce“ kanaluose. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Kliento užsakymo kūrimas produktams, kurie bus išsiųsti klientui

1. EKA operacijų ekrane įtraukite klientą į operaciją.
2. Įtraukite produktų į krepšelį.
3. Pasirinkite **Siųsti pasirinktus** arba **Siųsti visus**, norėdami išsiųsti produktus kliento abonemente nurodytu adresu.
4. Šią parinktį pasirinkite, norėdami sukurti kliento užsakymą.
5. Patvirtinkite arba pakeiskite „Siųsti iš“ vietą, siuntimo adresą ir pasirinkite siuntimo būdą.
6. Įveskite kliento pageidaujamą užsakymo siuntimo datą.
7. Naudokite mokėjimo funkcijas, kad sumokėtumėte visas apskaičiuotas mokėtinas sumas, arba naudokite operaciją **Įmokos keitimas**, norėdami pakeisti mokėtinas sumas, tada taikykite mokėjimą.
8. Jei visa užsakymo suma nebuvo sumokėta, įveskite kredito kortelę, kuri bus naudojama užfiksuoti mokėtinam užsakymo balansui, kai pateikiama sąskaita faktūra.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Kliento užsakymo kūrimas produktams, kuriuos klientas pasiims

1. EKA operacijų ekrane įtraukite klientą į operaciją.
2. Įtraukite produktų į krepšelį.
3. Rinkitės **Paimti parinktus** ar **Paimti visus** tam, kad pradėtumėte užsakymo paėmimo konfigūravimą.
4. Pasirinkite parduotuvės vietą, kur klientas paims pasirinktus produktus.
5. Rinkitė datą, kai objektas bus paimtas.
6. Naudokite mokėjimo funkcijas, kad sumokėtumėte visas apskaičiuotas mokėtinas sumas, arba naudokite operaciją **Įmokos keitimas**, norėdami pakeisti mokėtinas sumas, tada taikykite mokėjimą.
7. Jei visas užsakymas nebuvo sumokėtas, pasirinkite, ar klientas pateiks mokėjimą vėliau (paėmimo metu), ar kredito kortelė bus pažymima dabar ir tuomet naudojama ir paimama paėmimo metu.

### <a name="edit-an-existing-customer-order"></a>Esamo kliento užsakymo redagavimas

Mažmeninės prekybos užsakymus, sukurtus internetiniame arba parduotuvės kanale, galima atšaukti ir redaguoti naudojant EKA, jei reikia.

> [!IMPORTANT]
> Ne mažmeniniai užsakymai gali būti redaguojami per POS programą. Užsakymų, sukurtų skambučių centro kanale, negalima redaguoti naudojant EKA, jei parametras [Įjungti užsakymų užbaigimą](./set-up-order-processing-options.md#enable-order-completion) įjungtas skambučių centro kanalui. Norint užtikrinti teisingą mokėjimų apdorojimą, užsakymus, gautus iš skambučių centro kanalo ir naudojančius funkciją Įjungti užsakymų užbaigimą, reikia redaguoti naudojant skambučių centro programą, esančią „Commerce Headquarters“.

> [!NOTE]
> EKA, kuriuos sukūrė ne skambučių centro vartotojas, naudojant „Commerce Headquarters", rekomenduojame neredaguoti užsakymų ir pasiūlymų. Tuose užsakymuose ir pasiūlymuose naudojamas "Commerce pricing" modulis, todėl jei jie bus redaguojami naudojant EKA, „Commerce“ kainų variklis juos įkainos iš naujo.


10.0.17 versijoje ir vėlesnėse, vartotojai gali redaguoti galiojančius užsakymus per POS programą, net jei užsakymas yra įvykdytas iš dalies. Tačiau užsakymų, kurių visos SF išrašytos, vis tiek negalima redaguoti naudojant EKA. Norėdami įjungti šią galimybę, įjunkite **Redaguoti iš dalies įvykdytus užsakymos prekybos taške** funkciją **Funkcijos valdymas** darbo srityje. Jei ši funkcija neįjungta arba jei naudojate 10.0.16 versiją ar ankstesnę, vartotojai galės tik redaguoti kliento užsakymus POS, jei užsakyams yra atidarytas iki galo. Taip pat, jei funkcija įjungta, galite apriboti, kurios parduotuvės gali redaguoti iš dalies įvykdytus užsakymus. Parinktis skirta išjungti šią galimybę konkrečioms parduotuvėms gali būti konfigūruojama per **Funkcijų profilį** „FastTab“ **Bendri**.


1. Pažymėkite **Atšaukti užsakymą**.
2. Naudokite **Ieška**, norėdami įvesti filtrus ir rasti užsakymą, tada pasirinkite **Taikyti**.
3. Rezultatų sąraše pažymėkite užsakymą, tada pasirinkite **Redaguoti**. Jei mygtukas **Redaguoti** nepasiekiamas, užsakymas yra būsenos, kurios negalima redaguoti.
4. Operacijų krepšelyje atlikite visus būtinus kliento užsakymo pakeitimus. Kai kurie pakeitimai gali būti draudžiami redagavimo metu.
5. Užbaikite redagavimo procesą pasirinkdami mokėjimo operaciją.
6. Norėdami išeiti iš redagavimo proceso neišsaugodami pakeitimų, galite naudoti operaciją **Anuliavimo operacija**.

#### <a name="pricing-impact-when-orders-are-edited"></a>Kainos poveikis redaguojant užsakymus

Kai užsakymai pateikiami EKA arba "Commerce" el. komercijos svetainėje, klientai turi skirti sumą. Į šią sumą įeina kaina ir į ją taip pat gali būti įtraukta nuolaida. Klientas, kuris priima užsakymą, o vėliau susisieks su skambučių centru ir pakeis užsakymą (pavyzdžiui, norėdami įtraukti kitą prekę), tikisi nuolaidų taikymo. Net jei esamų užsakymo eilučių akcijos nebegalioja, klientas tikisi, kad iš pradžių tose eilutėse taikomos nuolaidos baigs galioti. Tačiau, jei nuolaida galiotų užsakymo pateikimo metu, tačiau nuolaida nebegalios nuo to laiko, klientas tikisi, kad nauja nuolaida bus taikoma pakeistam užsakymui. Kitu atveju klientas gali tik atšaukti esamą užsakymą ir sukurti naują užsakymą, kuriame pritaikyta nauja nuolaida. Kaip nurodyta šiame scenarijuje, kainos ir nuolaidos, kurias klientai įsipareigojo įvykdyti, turi būti išsaugotos. Tuo pat metu EKA ir skambučių centro vartotojai turi turėti galimybę lanksčiau perskaičiuoti pardavimo užsakymų eilučių kainas ir nuolaidas, kaip reikalaujama.

Kai užsakymai atšaukiami ir redaguojami naudojant EKA, esamų užsakymų eilučių kainos ir nuolaidos laikomos užrakintomis. Kitaip tariant, jie nepasikeičia, net jei kai kurios užsakymo eilutės yra atšauktos ar pakeistos, arba pridedami nauji užsakymo eilutės. Norint pakeisti esamų pardavimo eilučių kainas ir nuolaidas, EKA vartotojas turi pasirinkti **Perskaičiuoti**. Kainos užraktas pašalinamas iš esamų užsakymo eilučių. Tačiau prieš išleidžiant "Commerce" 10.0.21 versiją ši galimybė skambučių centre nebuvo galima. Todėl dėl bet kokių užsakymo eilučių pakeitimų kainos ir nuolaidos turi būti perskaičiuotos.

„Commerce" 10.0.21 versijoje nauja funkcija, kurios pavadinimas **Apsaugoti nuo netyčinio komercijos užsakymų kainos skaičiavimo** yra pasiekiama **funkcijų valdymo** darbo srityje. Ši funkcija išjungta pagal nutylėjimą. Kai jis įjungtas, nauja užrakinta **kainos ypatybė** galima visiems el. komercijos užsakymams. Kai užsakymo fiksavimas baigiamas užsakymams, pateiktiems bet kuriame kanale, ši ypatybė automatiškai įgalinamas (t. y. žymės langelis pažymėtas) visose užsakymo eilutėse. Tuomet "Commerce pricing engine" tos užsakymo eilutės neįtraukiamos į visų kainų ir nuolaidų skaičiavimus. Todėl, jei užsakymas redaguojamas, užsakymo eilutės pagal numatytuosius nustatymus neįtraukiamos į kainos ir nuolaidos skaičiavimą. Tačiau skambučių centro vartotojai gali uždrausti bet kurios užsakymo eilutės ypatybę (t. y. išvalyti žymės langelį) ir pasirinkti **Perskaičiuoti,** kad skaičiuojant kainą būtų įtrauktos esamos užsakymo eilutės.

Net jei skambučių centro vartotojai taiko neautomatinę nuolaidą esamai pardavimo eilutei, prieš taikydami rankiniu būdu nuolaidą, skambučių centro vartotojai turi išjungti pardavimo eilutės ypatybę **Užrakinta kaina**.

Skambučių centro vartotojai taip pat gali išjungti **užsakymo ypatybę** Kaina užrakinta masiškai, **užsakymo puslapio veiksmų** srities skirtuke **Pardavimas** pasirinkdami **Pašalinti** kainos **užraktą**. Šiuo atveju kainos užrakinimas pašalinamas iš visų užsakymo eilučių, išskyrus eilutes, kurios neredaguotinos (kitaip tariant, eilutės, kurių būsena yra Iš dalies **išrašyta SF** arba **Išrašyta SF**). Tada, atlikus užsakymo pakeitimus ir po to, kai jie pateikiami, kainų užraktas vėl naudojamas visoms užsakymo eilutėms.

> [!IMPORTANT]
> Kai įjungta prekybos užsakymų funkcijos funkcija **Uždrausti nenu nenumačius kainos skaičiavimą** prekybos sutarties įvertinimo nustatymo bus nepaisoma kainų darbo eigose. Kitaip tariant, prekybos sutarties vertinimo dialogo languose nebus rodomas su **kaina susijęs** skyrius. Taip nutinka, nes prekybos sutarties vertinimo nustatymo ir kainų užrakto funkcijos paskirtis yra panašūs: siekiant išvengti netyčinių kainos pakeitimų. Tačiau vartotojų patirtis vertinant prekybos sutartį nėra gerai tinka dideliems užsakymams, kuriuose vartotojai turi pasirinkti vieną ar daugiau užsakymo eilučių, kad būtų galima keisti.

> [!NOTE]
> Vienos **ar daugiau** pasirinktų eilučių užrakintą ypatybę Kainos galima išjungti tik tada, kai **naudojamas skambučių** centro modulis. EKA veikimo būdas nekinta. Kitaip tariant, EKA vartotojas negali atrakinti pasirinktų užsakymo eilučių kainų. Tačiau jie gali pasirinkti **Perskaičiuoti,** kad pašalintumėte kainos užraktą iš visų esamų užsakymo eilučių.

### <a name="cancel-a-customer-order"></a>Kliento užsakymo atšaukimas

1. Pažymėkite **Atšaukti užsakymą**.
2. Naudokite **Ieška**, norėdami įvesti filtrus ir rasti užsakymą, tada pasirinkite **Taikyti**.
3. Rezultatų sąraše pažymėkite užsakymą, tada pasirinkite **Atšaukti**. Jei mygtukas **Atšaukti** nepasiekiamas, užsakymas yra būsenos, kurios nebegalima atšaukti.
4. Jei sukonfigūruoti atšaukimo mokesčiai, patvirtinkite juos. Prieš patvirtindami, galite pakoreguoti atšaukimo mokesčius pagal poreikį. 
5. Operacijų krepšelyje užbaikite atšaukimo procesą pasirinkdami mokėjimo operaciją. Jei sumokėtos įmokos viršija atšaukimo mokestį, gali būti sumokėti grąžinimo mokėjimai.
6. Norėdami išeiti iš atšaukimo proceso neišsaugodami pakeitimų, galite naudoti operaciją **Anuliavimo operacija**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Kliento užsakymo siuntimo ar paėmimo EKA užbaigimas

Sukūrus užsakymą, prekes klientas paims iš parduotuvės arba jos bus išsiųstos, atsižvelgiant į užsakymo konfigūraciją. Daugiau informacijos apie šį procesą žr. dokumentaciją [Parduotuvės užsakymo įvykdymas](./order-fulfillment-overview.md).

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Kliento užsakymų asinchroninių operacijų srautas

Klientų užsakymus galima kurti EKA sinchroniniu arba asinchroniniu režimu. Jei kurdami klientų užsakymus EKA pastebite našumo problemų ar vartotojų uždelsimų, apsvarstykite galimybę įjungti asinchroninį užsakymų kūrimą.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Kliento užsakymų kūrimo asinchroniniu režimu funkcijos įjungimas

1. „Commerce Headquarters“ puslapyje **Funkcijų profiliai** pasirinkite funkcijos profilį, atitinkantį norimą sukonfigūruoti parduotuvę.
2. „FastTab“ **Bendra** nustatykite parinktį **Kurti kliento užsakymą asinchroniniu režimu** į **Taip**.

Kai parinktis **Kurti kliento užsakymą asinchroniniu režimu** nustatyta į **Taip**, kliento užsakymai visada kuriami asinchroniniu režimu, net jei galima naudoti „Retail Transaction Service“ (RTS). Jei šią parinktį nustatysite į **Ne**, kliento užsakymai bus visada kuriami sinchroniniu režimu naudojant RTS. Kai klientų užsakymai kuriami asinchroniniu režimu, jie įtraukiami ir kuriami kaip mažmeninės prekybos operacijos „Commerce Headquarters“ iš „Commerce“ įtraukimo (P) užduočių. Atitinkami mažmeninės prekybos operacijų pardavimo užsakymai sukuriami, kai funkcija **Sinchronizuoti užsakymus** vykdoma rankiniu būdu arba paketinio proceso metu.

## <a name="additional-resources"></a>Papildomi ištekliai

[Hibridiniai kliento užsakymai](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
