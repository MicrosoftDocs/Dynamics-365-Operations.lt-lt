---
title: Kliento užsakymai elektroniniame kasos aparate (EKA)
description: Šioje temoje pateikta informacija apie kliento užsakymus elektroniniame kasos aparate (EKA). Kliento užsakymai dar vadinami specialiais užsakymais. Šioje temoje pateikta susijusių parametrų ir operacijų srautų apžvalga.
author: josaw1
manager: AnnBe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f60e07c1faae9bc3cb6d3c843e72e6000cff7591
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220515"
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

Norėdami naudoti kliento užsakymus, turite sukonfigūruoti pristatymo būdus, kuriuos gali naudoti parduotuvės kanalas. Turite apibrėžti bent vieną pristatymo būdą, kurį galima naudoti, kai užsakymo eilutės siunčiamos klientui iš parduotuvės. Taip pat turite apibrėžti bent vieną pristatymo paėmimo būdą, kurį galima naudoti, kai užsakymo eilutės paimamos iš parduotuvės. Pristatymo būdai apibrėžiami „Commerce Headquarters“ puslapyje **Pristatymo būdai**. Daugiau informacijos apie tai, kaip nustatyti „Commerce“ kanalų pristatymo būdus, žr. [Pristatymo būdų apibrėžimas](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Puslapis pristatymo būdai](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Įvykdymo grupių nustatymas

Kai kurios parduotuvės ar sandėlių vietos gali neįvykdyti klientų užsakymų. Konfigūruodama įvykdymo grupes, organizacija gali nurodyti, kurios parduotuvės ir sandėlio vietos rodomos kaip parinktys vartotojams, kuriantiems kliento užsakymus EKA. Įvykdymo grupės konfigūruojamos puslapyje **Įvykdymo grupės**. Organizacijos gali sukurti tiek įvykdymo grupių, kiek joms reikia. Nustačiu įgyvendinimo grupę, susiekite ją su parduotuve pasirinkdami **Įgyvendinimo grupės priskyrimas** iš **Nustatyti** skirtuko veiksmų juostoje **Parduotuvės** puslapyje.

„Commerce“ versijoje 10.0.12 ir vėlesnėse, organizacijos gali nustatyti, ar sandėlis arba sandėlio ir parduotuvės deriniai, nustatyti įgyvendinimo grupėse, gali būti naudojami siuntimui, paėmimui ar ir siuntimui, ir paėmimui. Tai leidžia įtraukti lankstumo į verslą siekiant nustatyti, kurie sandėliai gali būti pasirinkti sukuriant kliento užsakymą siunčiamiems objektams pagal parduotuves, kurias galima pasirinkti sukuriant kliento užsakymą paimamiems objektams. Norėdami konfigūruoti šias parinktis, įjunkite **Galimybė nurodyti vietas kaip „Siuntimas“ ar „Paėmimas“ įjungtas įgyvendinimo grupėje** funkciją. Jei sandėlis susietas su įgyvendinimo grupe nėra parduotuvė, jis gali būti konfigūruojamas tik kaip siuntimo vieta. Jo negalima naudoti, kai paėmimo užsakymai yra sukonfigūruoti EKA.

![Puslapis Įvykdymo grupės](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanalo parametrų konfigūravimas

Kai dirbate su kliento užsakymais EKA, turite atsižvelgti į kai kuriuos parduotuvės kanalo parametrus. Šiuos parametrus galima rasti „Commerce Headquarters“ puslapyje **Parduotuvės**.

- **Sandėlis** – šiame lauke nurodomas sandėlis, naudojamas užsakymams, sukonfigūruotiems siuntimui iš parduotuvės, įvykdyti.
- **Įvykdymo grupės priskyrimas** – pasirinkite šį mygtuką (veiksmų srities skirtuke **Nustatymas**), norėdami susieti įvykdymo grupes, kuriomis nurodomos paėmimo vietų ar siuntimo kilmės parinktys, kai klientų užsakymai sukurti EKA.
- **Naudoti paskirties vietos mokesčius** – ši parinktis nurodo, ar siuntimo adresas naudojamas mokesčių grupei, taikomai užsakymo eilutėms, siunčiamoms kliento adresu, nustatyti.
- **Naudoti kliento mokesčius** – ši parinktis nurodo, ar mokesčių grupė, apibrėžta kliento pristatymo adresui, naudojama apmokestinti klientų užsakymus, sukurtus EKA, siuntimui į kliento namus.

![Parduotuvės kanalo nustatymas puslapyje Parduotuvės](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Kliento užsakymo parametrų nustatymas

Prieš pradėdami kurti kliento užsakymus EKA, turite sukonfigūruoti tinkamus parametrus „Commerce Headquarters“. Šiuos parametrus galima rasti puslapio **„Commerce” parametrai** skirtuke **Kliento užsakymai**.

- **Numatytasis užsakymo tipas** – galite nurodyti užsakymo tipą, kuris pagal numatytuosius nustatymus priskiriamas klientų užsakymams, sukurtiems EKA. Šie klientų užsakymai gali būti pardavimo arba pasiūlymo užsakymai. Nepaisant numatytojo užsakymo tipo, vartotojai vis tiek gali kurti pardavimo ir kliento užsakymus EKA.
- **Numatytasis įmokos procentas** – nurodykite visos užsakymo sumos procentą, kurį klientas turi sumokėti kaip įmoką, kad būtų galima patvirtinti užsakymą. Priklausomai nuo parduotuvės partnerių teisių, jie gali pakeisti sumą naudodami operaciją **Įmokos keitimas** EKA, jei ši operacija sukonfigūruota operacijos ekrano išdėstymui.
- **Paėmimo pristatymo būdas** – nurodykite pristatymo būdą, kuris turėtų būti taikomas pardavimo užsakymų eilutėms, sukonfigūruotoms paėmimui EKA.
- **Išsivežimo pristatymo būdas** – nurodykite pristatymo būdą, kuris turėtų būti taikomas pardavimo užsakymų eilutėms, kurios laikomos išsivežimo užsakymo eilutėmis, kai sukuriamas mišrus krepšelis, kuriame kai kurios eilutės bus paimtos ar išsiųstos, o kitas eilutes klientas išsiveš nedelsdamas.
- **Atšaukimo mokesčio procentas** – jei atšaukus kliento užsakymą turėtų būti taikomas mokestis, nurodykite to mokesčio sumą.
- **Atšaukimo mokesčio kodas** – nurodykite gautinų sumų mokesčio kodą, kuris turėtų būti naudojamas, kai atšauktiems kliento užsakymams EKA taikomas atšaukimo mokestis. Mokesčio kodas apibrėžia atšaukimo mokesčio finansų registravimo logiką.
- **Siuntimo mokesčio kodas** – jei parinktis **Naudoti išplėstinius automatinius mokesčius** nustatyta į **Taip**, šis parametro nustatymas neturi jokios įtakos. Jei parinktis nustatyta į **Ne**, vartotojai bus raginami rankiniu būdu įvesti siuntimo mokestį, kai jie sukurs kliento užsakymus EKA. Naudokite šį parametrą norėdami susieti gautinų sumų mokesčio kodą, kuris bus taikomas užsakymams, kai vartotojai įves siuntimo mokestį. Mokesčio kodas apibrėžia siuntimo mokesčio finansų registravimo logiką.
- **Naudoti išplėstinius automatinius mokesčius** – nustatykite šią parinktį į **Taip**, norėdami naudoti sistemos apskaičiuotus automatinius mokesčius, kai klientų užsakymai kuriami EKA. Šie automatiniai mokesčiai gali būti naudojami apskaičiuojant siuntimo mokesčius ar kitus užsakymo ar prekės mokesčius. Norėdami gauti daugiau informacijos apie tai, kaip nustatyti ir naudoti išplėstinius automatinius mokesčius, žr. [Daugiakanaliai išplėstiniai automatiniai mokesčiai](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Skirtukas Kliento užsakymai „Commerce” parametrų puslapyje](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Operacijų ekrano išdėstymo EKA naujinimas

Įsitikinkite, kad EKA [ekrano išdėstymas](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) sukonfigūruotas palaikyti klientų užsakymų kūrimą bei valdymą ir kad visos reikalingos EKA operacijos yra sukonfigūruotos. Toliau nurodytos kelios EKA operacijos, rekomenduojamos siekiant tinkamai palaikyti klientų užsakymų kūrimą ir valdymą.
- **Siųsti visus produktus** – ši operacija naudojama norint nurodyti, kad visos operacijos krepšelio eilutės bus išsiųstos į paskirties vietą.
- **Siųsti pasirinktus produktus** – ši operacija naudojama norint nurodyti, kad pasirinktos operacijos krepšelio eilutės bus išsiųstos į paskirties vietą.
- **Paimti visus produktus** – ši operacija naudojama norint nurodyti, kad visos operacijos krepšelio eilutės bus paimtos iš pasirinktos parduotuvės.
- **Paimti pasirinktus produktus** – ši operacija naudojama norint nurodyti, kad pasirinktos operacijos krepšelio eilutės bus paimtos iš pasirinktos parduotuvės.
- **Išsivežti visus produktus** – ši operacija naudojama norint nurodyti, kad visos operacijos krepšelio eilutės bus išsivežtos. Jei ši operacija naudojama EKA, kliento užsakymas bus konvertuotas į atsiskaitymo grynaisiais ir išsivežimo operaciją.
- **Išsivežti pasirinktus produktus** – ši operacija naudojama norint nurodyti, kad pasirinktas operacijos krepšelio eilutes klientas išsiveš pirkimo metu. Ši operacija naudinga tik [mišraus užsakymo](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders) atveju.
- **Atšaukti užsakymą** – ši operacija naudojama klientų užsakymams ieškoti ir gauti, kad EKA vartotojai galėtų redaguoti, atšaukti ar atlikti su jais susijusias operacijas pagal poreikį.
- **Keisti pristatymo būdą** – ši operacija gali būti naudojama norint greitai pakeisti eilučių, kurios jau sukonfigūruotos siuntimui, pristatymo būdą, nereikalaujant, kad vartotojai vėl pereitų srautus „Siųsti visus produktus“ arba „Siųsti pasirinktus produktus“.
- **Įmokos keitimas** – šią operaciją galima naudoti norint pakeisti įmokos sumą, kurią klientas sumokės už pasirinktą kliento užsakymą.

![Operacijos EKA operacijų ekrane](media/customer-order-screen-layout.png)

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
> Ne mažmeniniai užsakymai gali būti redaguojami per POS programą. Užsakymų, sukurtų skambučių centro kanale, negalima redaguoti naudojant EKA, jei parametras [Įjungti užsakymų užbaigimą](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) įjungtas skambučių centro kanalui. Norint užtikrinti teisingą mokėjimų apdorojimą, užsakymus, gautus iš skambučių centro kanalo ir naudojančius funkciją Įjungti užsakymų užbaigimą, reikia redaguoti naudojant skambučių centro programą, esančią „Commerce Headquarters“.

10.0.17 versijoje ir vėlesnėse, vartotojai gali redaguoti galiojančius užsakymus per POS programą, net jei užsakymas yra įvykdytas iš dalies. Tačiau užsakymų, kurių visos SF išrašytos, vis tiek negalima redaguoti naudojant EKA. Norėdami įjungti šią galimybę, įjunkite **Redaguoti iš dalies įvykdytus užsakymos prekybos taške** funkciją **Funkcijos valdymas** darbo srityje. Jei ši funkcija neįjungta arba jei naudojate 10.0.16 versiją ar ankstesnę, vartotojai galės tik redaguoti kliento užsakymus POS, jei užsakyams yra atidarytas iki galo. Taip pat, jei funkcija įjungta, galite apriboti, kurios parduotuvės gali redaguoti iš dalies įvykdytus užsakymus. Parinktis skirta išjungti šią galimybę konkrečioms parduotuvėms gali būti konfigūruojama per **Funkcijų profilį** „FastTab“ **Bendri**.


1. Pažymėkite **Atšaukti užsakymą**.
2. Naudokite **Ieška**, norėdami įvesti filtrus ir rasti užsakymą, tada pasirinkite **Taikyti**.
3. Rezultatų sąraše pažymėkite užsakymą, tada pasirinkite **Redaguoti**. Jei mygtukas **Redaguoti** nepasiekiamas, užsakymas yra būsenos, kurios negalima redaguoti.
4. Operacijų krepšelyje atlikite visus būtinus kliento užsakymo pakeitimus. Kai kurie pakeitimai gali būti draudžiami redagavimo metu.
5. Užbaikite redagavimo procesą pasirinkdami mokėjimo operaciją.
6. Norėdami išeiti iš redagavimo proceso neišsaugodami pakeitimų, galite naudoti operaciją **Anuliavimo operacija**.



### <a name="cancel-a-customer-order"></a>Kliento užsakymo atšaukimas

1. Pažymėkite **Atšaukti užsakymą**.
2. Naudokite **Ieška**, norėdami įvesti filtrus ir rasti užsakymą, tada pasirinkite **Taikyti**.
3. Rezultatų sąraše pažymėkite užsakymą, tada pasirinkite **Atšaukti**. Jei mygtukas **Atšaukti** nepasiekiamas, užsakymas yra būsenos, kurios nebegalima atšaukti.
4. Jei sukonfigūruoti atšaukimo mokesčiai, patvirtinkite juos. Prieš patvirtindami, galite pakoreguoti atšaukimo mokesčius pagal poreikį. 
5. Operacijų krepšelyje užbaikite atšaukimo procesą pasirinkdami mokėjimo operaciją. Jei sumokėtos įmokos viršija atšaukimo mokestį, gali būti sumokėti grąžinimo mokėjimai.
6. Norėdami išeiti iš atšaukimo proceso neišsaugodami pakeitimų, galite naudoti operaciją **Anuliavimo operacija**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Kliento užsakymo siuntimo ar paėmimo EKA užbaigimas

Sukūrus užsakymą, prekes klientas paims iš parduotuvės arba jos bus išsiųstos, atsižvelgiant į užsakymo konfigūraciją. Daugiau informacijos apie šį procesą žr. dokumentaciją [Parduotuvės užsakymo įvykdymas](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview).

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Kliento užsakymų asinchroninių operacijų srautas

Klientų užsakymus galima kurti EKA sinchroniniu arba asinchroniniu režimu. Jei kurdami klientų užsakymus EKA pastebite našumo problemų ar vartotojų uždelsimų, apsvarstykite galimybę įjungti asinchroninį užsakymų kūrimą.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Kliento užsakymų kūrimo asinchroniniu režimu funkcijos įjungimas

1. „Commerce Headquarters“ puslapyje **Funkcijų profiliai** pasirinkite funkcijos profilį, atitinkantį norimą sukonfigūruoti parduotuvę.
2. „FastTab“ **Bendra** nustatykite parinktį **Kurti kliento užsakymą asinchroniniu režimu** į **Taip**.

Kai parinktis **Kurti kliento užsakymą asinchroniniu režimu** nustatyta į **Taip**, kliento užsakymai visada kuriami asinchroniniu režimu, net jei galima naudoti „Retail Transaction Service“ (RTS). Jei šią parinktį nustatysite į **Ne**, kliento užsakymai bus visada kuriami sinchroniniu režimu naudojant RTS. Kai klientų užsakymai kuriami asinchroniniu režimu, jie įtraukiami ir kuriami kaip mažmeninės prekybos operacijos „Commerce Headquarters“ iš „Commerce“ įtraukimo (P) užduočių. Atitinkami mažmeninės prekybos operacijų pardavimo užsakymai sukuriami, kai funkcija **Sinchronizuoti užsakymus** vykdoma rankiniu būdu arba paketinio proceso metu.

## <a name="additional-resources"></a>Papildomi ištekliai

[Hibridiniai kliento užsakymai](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]