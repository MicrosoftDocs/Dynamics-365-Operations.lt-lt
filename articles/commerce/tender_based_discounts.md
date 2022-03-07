---
title: Nuolaidos pagal mokėjimo būdą
description: Šioje temoje pateikiama funkcijų, kurios leidžia pardavėjams konfigūruoti nuolaidas pagal konkrečius mokėjimo būdus, apžvalga.
author: bebeale
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 52b9510b2c22157aec27b865115273064bb0e803443306ea20468b93a2ea3ca7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719470"
---
# <a name="tender-based-discounts"></a>Nuolaidos pagal mokėjimo būdą

[!include [banner](includes/banner.md)]


Pardavėjai dažnai pristato privačias, firmines kredito korteles. Pardavėjams tai yra naudinga, nes jiems bankai pasiūlo pageidaujamus tarifus. Be to, kadangi šios kredito kortelės gali paskatinti klientus dažniau apsilankyti parduotuvėje, jos padeda padidinti bendras pardavėjo pajamas. Todėl pardavėjai yra suinteresuoti skatinti klientus naudoti firmines kredito korteles. Siekdami šio tikslo, jie dažnai teikia papildomas nuolaidas klientams, naudojantiems šias kredito korteles.

Be to, pardavėjai, kurie nesiūlo firminių kredito kortelių, gali skatinti klientus atsiskaityti kitais būdais, pvz., naudojant grynuosius pinigus, dovanų korteles ar lojalumo taškus. Tokiu būdu jie gali sumažinti kredito kortelių aptarnavimo mokesčių išlaidas. Todėl pardavėjai gali teikti nuolaidas klientams, naudojantiems šiuos alternatyvius mokėjimo būdus.

Dirbdami su „Microsoft Dynamics 365 Commerce“, pardavėjai gali konfigūruoti nuolaidos procentus, taikomus atitinkamoms eilutėms, jei klientas moka naudodamas pageidaujamą mokėjimo priemonės tipą. Klientas gali pasirinkti atlikti dalinį arba pilną apmokėjimą, o „Commerce” nustato atitinkamą nuolaidos sumą. Atkreipkite dėmesį, kad nuolaida visada taikoma atitinkamų prekių sumai prieš mokesčius.

Nuolaidos pagal mokėjimo būdą nekonkuruoja su nuolaidomis, susijusiomis su preke, pvz., periodinėmis arba neautomatinėmis nuolaidomis. Jos visada skaičiuojamos kartu su prekių nuolaidomis. Todėl net jei prekei taikoma išskirtinė periodinė nuolaida, nuolaida pagal mokėjimo būdą vis tiek taikoma kartu su išskirtinėje periodine nuolaida. Analogiškai, jei operacijai taikoma ribinė nuolaida, o nuolaida pagal mokėjimo būdą sumažina bendrą sumą iki mažesnės už ribinę vertės, operacijai vis tiek taikoma ribinė nuolaida.

Nors nuolaidos pagal mokėjimo būdą sumažina operacijos tarpinę sumą, tai neturi įtakos automatiniams mokesčiams, taikomiems operacijai. Pavyzdžiui, jei dėl to, kad tarpinė suma buvo didesnė nei 100 JAV dol., buvo apskaičiuotos 5 JAV dol. pristatymo išlaidos, o nuolaida pagal mokėjimo būdą sumažina sumą iki mažesnės nei 100 JAV dol., užsakymo pristatymo išlaidos vis tiek yra 5 JAV dol.


> [!NOTE]
> Nuolaidos pagal mokėjimo būdą proporcingai paskirstomos atitinkamoms pardavimo eilutėms ir sumažina atskirų eilučių sumą prieš mokesčius. Jei mokėjimo priemonės tipui yra sukonfigūruotos kelios nuolaidos pagal mokėjimo būdą (pavyzdžiui, grynaisiais pinigais), taikoma tik didžiausia nuolaida pagal mokėjimo būdą.

Nuolaidas pagal mokėjimo būdą galima taikyti tik pardavimo eilutėms, kuriose kainos nėra užrakintos. Jei į užsakymą įtraukiamos naujos pardavimo eilutės, nuolaida pagal mokėjimo būdą taikoma naujoms pardavimo eilutėms tik mokėjimo metu. Tuo metu, kai pateikiamas kliento paėmimo arba siuntimo užsakymas, nuolaida pagal mokėjimo priemonę taikoma tik depozito sumai. Pateikus užsakymą, vykdymo metu pardavimo eilučių kainos yra užrakintos. Todėl jokia nuolaida pagal mokėjimo būdą netaikoma jokiam balansui, kuris apmokamas paėmimo metu arba autorizuojamas pristatymo metu. Nuolaida pagal mokėjimo būdą gali būti taikoma visai kliento užsakymo sumai tik tuo atveju, jei pardavėjas surenka visą sumą kaip depozitą užsakymo pateikimo metu.

> [!IMPORTANT]
> Dirbant su „Commerce“, nuolaidos pagal mokėjimo būdą šiuo metu galimos dviem mokėjimo tipams: kredito kortele ir grynaisiais pinigais.

## <a name="pos-user-experience"></a>EKA vartotojo patirtis

Jei nuolaida pagal mokėjimo būda yra nustatyta gryniesiems pinigams, o kasininkas, dirbantis su elektroniniu kasos aparatu (EKA), pasirenka mygtuką, kuris yra susietas su mokėjimo grynaisiais operacija, nuolaida pagal mokėjimo būdą operacijai taikoma automatiškai. Tada sumažinta suma rodoma kaip balansas. Tačiau, jei kasininkas pasirenka mokėjimo ekrano mygtuką **Atgal**, nuolaida bus pašalinta, o operacijos ekrane bus rodoma pradinė suma. Jei mokėjimo eilutė tuščia, nuolaida pagal mokėjimo būdą pašalinama.

Mokant kortele, pardavėjai gali nustatyti nuolaidą pagal mokėjimo būdą vienam ar daugiau kredito kortelių tipų. Tačiau sistema negali patikrinti naudojamos kredito kortelės tipo, jei kortelė nėra autorizuota. Jei nuolaida taikoma po autorizavimo, mokėjimo autorizavimas bus taikomas didesnei sumai, o mokėjimo fiksavimas bus taikomas mažesnei sumai.

Siekiant išvengti šios situacijos, jei klientas moka kredito kortele, kasininkas mato dialogo langą, kuriame rodomos kredito kortelės, leisiančios klientui sutaupyti papildomai. Kasininkas gali paklausti, ar klientas nori naudoti vieną iš pageidaujamų kortelių papildomai nuolaidai gauti. Jei kasininkas naudoja pageidaujamą kortelę, nuolaida pagal mokėjimo būdą taikoma operacijai, o sumažinta suma rodoma mokėjimo ekrane. Autorizavimas bus taikomas sumažintai sumai. Jei klientas naudoja kortelę, kuri skiriasi nuo kortelės, kurią pasirinko kasininkas, rodomas klaidos pranešimas ir autorizavimas nebegalioja.


## <a name="call-center-user-experience"></a>Skambučių centro vartotojo patirtis

Kai skambučių centro užsakymo metu vartotojas pasirenka **Baigti**, rodomas ekranas **Sumos**. Iš pradžių šio ekrano sumos neapima nuolaidų pagal mokėjimo būdą, nes dar nepasirinktas mokėjimo būdas. Ekrane **Įtraukti mokėjimą**, jei vartotojas pasirenka mokėjimo būdą, kuriam yra sukonfigūruota nuolaida pagal mokėjimo būdą, mokėjimo suma automatiškai koreguojama, kad atitiktų sumą su nuolaidą. Kaip ir EKA kliento atveju, skambučių centro klientas gali nuspręsti, ar atlikti pilną mokėjimą, ar dalinį mokėjimą. Remiantis sumokėta suma, pardavimo užsakymui taikoma nuolaida pagal mokėjimo būdą.

> [!NOTE]
> Skambučių centro užsakymams kortelių tikrinimas nėra atliekamas. Pavyzdžiui, jei skambučių centro vartotojas pasirenka „Visa“ kredito kortelę, tačiau klientas naudoja „Mastercard“, sistema vis tiek taiko nuolaidą.

## <a name="exclude-items-from-discounts"></a>Netaikyti nuolaidų prekėms

Pardavėjai dažnai pasirenka netaikyti nuolaidų kai kuriems produktams, pvz., naujoms prekėms arba paklausioms prekėms. Tačiau jie vis dar gali norėti taikyti nuolaidas pagal mokėjimo būdą. Pavyzdžiui, pardavėjas gali sukonfigūruoti „Commerce“, kad nebūtų taikomos su preke susijusios nuolaidos arba neautomatinės nuolaidos. Tačiau, jei klientas moka naudodamas pageidaujamą mokėjimo priemonę, „Commerce“ vis dar taiko nuolaidą pagal mokėjimo būdą. Norėdami nustatyti „Commerce“ šiuo būdu, pardavėjai turi eiti į **Produkto informacijos valdymas > Produktai > Išleisti produktai**, pasirinkti prekę, tada „FastTab“ **Commerce** parinktis **Neleisti jokių nuolaidų** ir **Neleisti mokėjimo priemone pagrįstų nuolaidų** nustatyti į **Ne**, o parinktis **Neleisti nuolaidų** ir **Neleisti rankiniu būdu įvedamų nuolaidų** į **Taip**.

> [!NOTE]
> Kaip konfigūracija **Neleisti jokių nuolaidų** nustatyta į **Taip**, produktui nebus taikoma jokių nuolaidų. Nebus taikomos netgi nuolaidos pagal mokėjimo būdą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]