---
title: Pasenusios funkcijos
description: "Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Platform
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: Human Translation
ms.sourcegitcommit: 3267bd1cbd738b5ced9996fc3b28eee211627591
ms.openlocfilehash: 8feffb27b5d08a9c90e97ac0d7e00abf0448d0df
ms.contentlocale: lt-lt
ms.lasthandoff: 06/16/2017


---

# <a name="deprecated-features"></a>Pasenusios funkcijos

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Funkcijos, kurios nebenaudojamos „Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo 2017 m. liepos mėn. naujinime

### <a name="warehouse-mobile-devices-portal"></a>Sandėlio mobiliųjų įrenginių portalas

Sandėlio mobiliųjų įrenginių portalas (WMDP) buvo atskiras komponentas, kuris buvo skirtas vietiniam savarankiškam diegimui. Naudojant „Microsoft Dynamics 365 for Finance and Operations‟ leidimą „Enterprise‟ šis komponentas nebepalaikomas. Vietinė vartotojo patirtį pagerinanti programa pakeitė WMDP funkcijas. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Nebenaudojimo priežastis**       | Besidubliuojančios funkcijos.                        |
| **Pakeitė kita funkcija?** | Taip. Šią funkciją pakeitė „Finance and Operations“ – versija „Warehousing“. Norėdami gauti daugiau informacijos apie sąranką ir būtinąsias sąlygas, žr. [„Microsoft Dynamics 365 for Finance and Operations“ – versijos „Warehousing“ diegimas ir konfigūravimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Paveikti moduliai**             | Sandėlio valdymas, transportavimo valdymas |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Pažangaus banko derinimo ir rankinio gretinimo taisyklė

Gretinimo taisyklė buvo naudojama norint pasirinkti ir pažymėti banko dokumentą rankiniu būdu gretinant dokumentus suderinimo darbalapyje.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Nebenaudojimo priežastis**       | Ribotas naudojimas.                                                                         |
| **Pakeitė kita funkcija?** | Nr. Stulpelio filtravimo galimybės turėtų būti naudojamos norint surasti suderinimui skirtus dokumentus. |
| **Paveikti moduliai**             | Grynųjų pinigų ir banko valdymas                                                               |

### <a name="windows-8-tablet-app"></a>„Windows 8“ planšetinių kompiuterių programėlė

„Windows 8“ planšetinių kompiuterių programėlė turėdavo išlaidų pateikimo ir patvirtinimo funkciją.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Nebenaudojimo priežastis**       | „Finance and Operations” suderinama su planšetiniais kompiuteriais. Planšetinių kompiuterių programėlės nebereikia. |
| **Pakeitė kita funkcija?** | Nr.                                                                                      |
| **Paveikti moduliai**             | Išlaidų valdymas                                                                       |


<a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Funkcijos, kurios nebenaudojamos „Dynamics 365 for Operations“ 1611 versijoje su 3 platformos naujinimu
---------------------------------------------------------------------------------------------

### <a name="aeb-payment-formats-for-spain"></a>AEB mokėjimo formatai, skirti Ispanijai

Consejo Superior Bancario mokėjimo formatai naudojami siunčiant kliento ir tiekėjo mokėjimų pavedimo failus į banką. Šių formatų turinį nustato Asociación Española de Banca. Ji apima Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                                  |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito pervedimo ir tiesioginio debeto mokėjimo formatai, skirti Ispanijai |
| Paveikti moduliai             | Mokėtinos sumos, gautinos sumos                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Banko mokėjimų perkėlimas, skirtas Lietuvai

Banko mokėjimų pervedimai generuojami ir spausdinami naudojant Lietuvos mokėjimo pervedimo (LT) eksportavimo formatą. Lietuvos rinkoje 2005 m. pradėta naudoti LITAS, suvienodinta elektroninės bankininkystės sistema.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                    |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Lietuvai |
| Paveikti moduliai             | Mokėtinos sumos                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS „Direkte Remittering“ mokėjimo formatai, skirti Norvegijai

BBS „Direkte Remittering“ mokėjimo formatai apima kliento mokėjimų rinkinio eksportavimą (tiesioginis debetas) ir grąžinimo pranešimo importavimą.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                                                                                                                        |
| Pakeitė kita funkcija? | „AvtaleGiro“ kliento mokėjimų formatą, skirtą Norvegijai, galima naudoti norint generuoti tiesioginio debeto pranešimus. Grąžinimo pranešimo importavimo funkciją bus galima naudoti būsimuose leidimuose. |
| Paveikti moduliai             | Mokėtinos sumos, gautinos sumos                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Sąskaitų plano įrankis, skirtas Ispanijai

Šis įrankis naudojama, kai sąskaitų plane, skirtame Ispanijai, reikia atlikti didelių keitimų. Vartotojai gali importuoti naują sąskaitų planą, naudodami „Microsoft Excel“ arba teksto formatu, ir taip pat gali importuoti finansines ataskaitas.

|                              |                |
|------------------------------|----------------|
| Nebenaudojimo priežastis       | Ribotas naudojimas  |
| Pakeitė kita funkcija? | Nr.             |
| Paveikti moduliai             | DK |

### <a name="dom80-payment-format-for-belgium"></a>„Dom80“ mokėjimo formatas, skirtas Belgijai

Senesnės versijos Belgijos mokėjimų rinkinio mokėjimo formatas (tiesioginis debetas).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatas nebenaudojamas.                  |
| Pakeitė kita funkcija? | Taip, ISO 20022 tiesioginio debeto mokėjimo formatas, skirtas Belgijai |
| Paveikti moduliai             | Gautinos sumos                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA / EZAG mokėjimo formatai, skirti Šveicarijai

ATM / EZAG formatai yra integruoti į ESR sistemą, nes jie turi nuorodos numerius. Nuorodos numeriai nėra būtini, todėl naudojant šiuos formatus galima apdoroti bet kurį tiekėjo mokėjimą. Šiuos formatus naudoja įmonės, turinčios ne „Postfinance“ esančias banko sąskaitas.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                      |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Šveicarijai |
| Paveikti moduliai             | Mokėtinos sumos                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB tiesioginio debeto mokėjimo formatas, skirtas Austrijai

EDIFACT-DIRDEB mokėjimų rinkinio mokėjimo formatas (tiesioginis debetas).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatas nebenaudojamas.                  |
| Pakeitė kita funkcija? | Taip, ISO 20022 tiesioginio debeto mokėjimo formatas, skirtas Austrijai |
| Paveikti moduliai             | Gautinos sumos                                    |

### <a name="edivat-for-belgium"></a>EDIVAT, skirtas Belgijai

EDIVAT yra pasenęs Belgijos elektroninių deklaracijų teikimo saugiu paštu standartas. „Microsoft Dynamics AX 2012“ lieka tik skaitymo sprendimas, kad būtų galima prieiga prie retrospektyvos duomenų.

|                              |                                      |
|------------------------------|--------------------------------------|
| Nebenaudojimo priežastis       | Funkcija nebenaudojama. |
| Pakeitė kita funkcija? | Nr.                                   |
| Paveikti moduliai             | DK                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>„eGiro“ EDIFACT CREMUL mokėjimo importavimo formatas, skirtas Norvegijai

„eGiro“ yra pagrįstas tarptautiniu JT standartu EDIFACT CREMUL (pakartotinis kredito pažymų pranešimas), kuris naudojamas automatiškai registruojant kliento mokėjimus. „Microsoft Dynamics AX“ „eGiro“ naudojamas kaip kliento mokėjimo importavimo formatas.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatas nebenaudojamas.                                                     |
| Pakeitė kita funkcija? | Nr. Būsimuose leidimuose formatą bus pakeis ISO 20022 išrašo importavimo formatas. |
| Paveikti moduliai             | Gautinos sumos                                                                       |

### <a name="external-inventory-for-poland"></a>Išorinės atsargos, skirtos Lenkijai

Įrodymas, kad iš tiekėjo paimtos parduotinos prekės be pirkimo. Prekės, tvarkomos išorinėse atsargose, neturi įtakos standartinėms atsargoms ir gali būti parduotos bei automatiškai nupirktos. Šiuo procesu sukuriami tikri atsargų perkėlimai.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| Nebenaudojimo priežastis       | Pakeitė kita funkcija                     |
| Pakeitė kita funkcija? | Taip, pagrindinė gaunamos konsignacijos funkcija |
| Paveikti moduliai             | Mokėtinos sumos, atsargų valdymas          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finansinių ataskaitų generatorius, skirtas Rytų Europai

Įrankis yra skirtas apskaitos ir mokesčių ataskaitų duomenų rinkiniui nustatyti ir duomenims į XLS ir DOC ataskaitų šablonus eksportuoti.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Ribotas naudojimas                                                                            |
| Pakeitė kita funkcija? | Nr. Būsimuose leidimuose įrankį pakeis elektroninių ataskaitų konfigūracijos. |
| Paveikti moduliai             | DK                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Kliento mokėjimo operacijų importavimas, skirtas Suomijai

Galite pasirinkti Suomijos mokėjimų importavimo formatą, kurį naudojant kliento mokėjimo operacijos importuojamos iš išorinio banko pateikto failo.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatas nebenaudojamas.                                                     |
| Pakeitė kita funkcija? | Nr. Būsimuose leidimuose formatą bus pakeis ISO 20022 išrašo importavimo formatas. |
| Paveikti moduliai             | Gautinos sumos                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Mokėjimo operacijų importavimas į DK žurnalą, skirtas Suomijai

Suomijai būdingas formatas naudojamas apskaitos operacijoms į DK importuoti.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatas nebenaudojamas.                                                     |
| Pakeitė kita funkcija? | Nr. Būsimuose leidimuose formatą bus pakeis ISO 20022 išrašo importavimo formatas. |
| Paveikti moduliai             | Gautinos sumos                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Sinchronizuotas integravimas su „Isabel“ (CIS), skirtas Belgijai

„Isabel“ yra elektroninės bankininkystės sistema Europoje ir de facto standartinė sistema Belgijoje.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Integravimas su „Isabel“ klientu nebepalaikomas.                                                                |
| Pakeitė kita funkcija? | Nr. Mokėjimo formatai nebenaudojami, juos pakeitė ISO20022 kredito pervedimo mokėjimo formatas, skirtas Belgijai. |
| Paveikti moduliai             | Mokėtinos sumos                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Sąskaitų plano ir apskaitos taisyklių modifikavimai, skirti Ispanijai

Ši funkcija naudojama Ispanijos sąskaitų plano ir apskaitos taisyklių keitimams atlikti. Ji sąskaitas susieja ir padeda seną sąskaitų planą paversti nauju sąskaitų planu bei palygina ankstesnius finansinius metus su naujais finansiniais metais, net jei jie buvo užregistruotu kituose sąskaitos numeriuose.

|                              |                |
|------------------------------|----------------|
| Nebenaudojimo priežastis       | Ribotas naudojimas  |
| Pakeitė kita funkcija? | Nr.             |
| Paveikti moduliai             | DK |

### <a name="pagamento-fornittori-vendor-payment-format"></a>„Pagamento Fornittori“ tiekėjo mokėjimo formatas

Senesnės versijos Italijos kredito perkėlimų mokėjimo formatas.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatas nebenaudojamas.                  |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Italijai |
| Paveikti moduliai             | Mokėtinos sumos                                       |

### <a name="payment-export-formats-for-estonia"></a>Mokėjimų eksportavimo formatai, skirti Estijai

„Telehansa“ ir „Teleservice“ formatai naudojami banko mokėjimams eksportuoti.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                  |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Estijai |
| Paveikti moduliai             | Mokėtinos sumos                                         |

### <a name="payment-file-archive-for-norway"></a>Mokėjimo failo archyvas, skirtas Norvegijai

Generuojant mokėjimo failus, failų archyvas automatiškai suarchyvuoja visus sukurtus failus, įskaitant net anksčiau rašytus ar skaitytis failus.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Pakeitė kita funkcija                                        |
| Pakeitė kita funkcija? | Taip, suarchyvuotos elektroninių ataskaitų užduotys                            |
| Paveikti moduliai             | Mokėtinos sumos, gautinos sumos, organizacijos administravimas |

### <a name="payment-import-formats-for-estonia"></a>Mokėjimų importavimo formatai, skirti Estijai

„Telehansa“ ir „TeleTeenus“ formatai naudojami banko mokėjimams importuoti.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                                                    |
| Pakeitė kita funkcija? | Nr. Būsimuose leidimuose formatus bus pakeis ISO 20022 išrašo importavimo formatas. |
| Paveikti moduliai             | Gautinos sumos                                                                        |

### <a name="performance-management-goal-workflow"></a>Efektyvumo valdymo tikslų darbo eiga

Efektyvumo valdymas apima tikslų valdymą ir integravimą su efektyvumo apžvalgomis.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Efektyvumo valdymas buvo atnaujintas ir tikslo puslapių skaičius buvo sumažintas siekiant supaprastinti procesą.                 |
| Pakeitė kita funkcija? | Nr. Tikslus gali vadovai mato naudodami portalą Vadovų savitarna ir vadovas gali juos keisti bei peržiūrėti. |
| Paveikti moduliai             | Žmogiškojo kapitalo valdymas                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>„Postgirot“ ir „Postgirot Utland“ mokėjimo formatai, skirti Švedijai

„Postgirot“ ir „Postgirot Utland“ mokėjimo formatai, skirti Švedijai.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                 |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Švedijai |
| Paveikti moduliai             | Mokėtinos sumos                                        |

### <a name="radio-frequency-identifier"></a>Radijo dažnio identifikatorius

Radijo dažnio identifikavimas (RFID) yra duomenų surinkimo technologija, naudojanti elektronines žymes identifikavimo duomenims saugoti ir tiesioginio matymo skaitytuvą jiems gauti.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| Nebenaudojimo priežastis       | Naudojo mažai klientų ir ribotas funkcijų rinkinys. |
| Pakeitė kita funkcija? | Nr.                                            |
| Paveikti moduliai             | Atsargų valdymas                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Valstybinių SF numeravimo ataskaita, skirta Latvijai

Pagal Latvijos įstatymus galioja konkrečios pardavimo SF numeravimo taisyklės. Ši funkcija suteikia galimybę pardavimo SF priskirti konkrečius numerius pagal vartotoją arba vartotojų grupę. Tada galima generuoti ataskaitą arba XML failą. Taip pat galite spausdinti naudojamų SF numerių ataskaitą.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Valstybinių SF numeravimo tvarkyti nebereikia. Anksčiau naudota SF numerių ataskaita nebereikalinga. |
| Pakeitė kita funkcija? | Nr.                                                                                                                       |
| Paveikti moduliai             | Gautinos sumos                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Lietuvos įmonės vadovo ir vyriausiojo buhalterio vardų nustatymas

Įmonės vadovo ir vyriausiojo buhalterio vardus galima nurodyti įmonės informacijoje ir naudoti skirtinguose vietos ataskaitų spaudiniuose.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Nebenaudojimo priežastis       | Pakeitė kita funkcija                                     |
| Pakeitė kita funkcija? | Taip, tarnautojų nustatymo funkciją galima naudoti tais pačiais tikslais.   |
| Paveikti moduliai             | Mokėtinos sumos, Gautinos sumos, Grynųjų pinigų ir banko valdymas |

### <a name="telepay-payment-formats-for-norway"></a>„Telepay“ mokėjimo formatai, skirti Norvegijai

„Telepay“ mokėjimo formatai apima tiekėjo mokėjimo eksportavimą (kredito pervedimas) ir kliento mokėjimo surinkimą (tiesioginis debetas).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                                                        |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito pervedimo mokėjimo formatas ir „AvtaleGiro“ kliento mokėjimo formatas, skirti Norvegijai |
| Paveikti moduliai             | Mokėtinos sumos, gautinos sumos                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Tiekėjo mokėjimo eksportavimo formatai, skirti Suomijai

Suomijai skirti du mokėjimų eksportavimo formatai. LM02 (FI) naudojamas vietiniams mokėjimams, o LUM2 (FI) naudojamas užsienio mokėjimams.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Nebenaudojimo priežastis       | Mokėjimo formatai nebenaudojami.                  |
| Pakeitė kita funkcija? | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Suomijai |
| Paveikti moduliai             | Mokėtinos sumos                                         |

### <a name="workflow-for-creating-goals"></a>Tikslų kūrimo darbo eiga

Darbo eiga, skirta darbuotojų tikslų kūrimui valdyti, yra viena iš kelių darbo eigų, kurias buvo galima naudoti norint geriau koordinuoti efektyvumo valdymo procesą.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | „Microsoft Dynamics 365 Finance and Operations“ efektyvumo valdymas buvo visiškai perkurtas.                                                                                                                                                                                                                                        |
| Pakeitė kita funkcija? | Perkurta efektyvumo valdymo funkcija suteikia galimybę geriau kontroliuoti tikslų turinį, matavimus, naudojamus eigai sekti, ir patvirtinamųjų dokumentų pridėjimą. Tikslai gali būti saugomi kaip šablonai ir naudojami pakartotinai. Naudodami šią funkciją galite greičiau nustatyti papildomus darbuotojų tikslus. |
| Paveikti moduliai             | Žmogiškojo kapitalo valdymas                                                                                                                                                                                                                                                                                                               |

## <a name="features-deprecated-in-dynamics-ax-70-releases"></a>Funkcijos, nebenaudojamos „Dynamics AX“ 7.0 leidimuose
### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Galimybė atšaukti tiekėjo SF pakeitimus

|                              |                         |
|------------------------------|-------------------------|
| Nebenaudojimo priežastis       | Našumo padidinimas |
| Pakeitė kita funkcija? | Ne                      |
| Paveikti moduliai             | Mokėtinos sumos        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD ir AxBC integracijos

Programos integravimo sistemoje (AIF) duomenimis su išorinėmis sistemomis galima keistis naudojant verslo logiką, rodomą kaip paslaugas. „Dynamics AX‟ apima paslaugas, paremtas dokumentais ir „.NET Business Connector‟ (AxBC). Dokumentas sukuriamas naudojant XML. XML yra antraštės informacija, kuri pridedama sukurti *pranešimui*, kuris gali būti perkeliamas į „Dynamics AX‟ arba iš jos. Dokumentų pavyzdžiai apima pardavimo užsakymus ir pirkimo užsakymus. Tačiau dokumentas gali atstoti beveik visus objektus, pvz., klientą. Paslaugos, paremtos dokumentais, naudoja **Axd &lt;*dokumentų*&gt;** klases.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | AIF ir AxDs architektūros dydžio negalima keisti pagal debesies tarnybą. Atliekant masinį importą, buvo našumo problemų.                                                                               |
| Pakeitė kita funkcija? | Dabartinėje „Dynamics AX‟ versijoje šią funkciją pakeitė Duomenų importavimo / eksportavimo sistema, kuri palaiko pasikartojantį masinį importavimą / eksportavimą. Su AxBC rekomenduojame naudoti faktines lenteles. |
| Paveikti moduliai             | AxD, AxBC ir AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>KS be KS versijų

Kai **KS versijų** konfigūracijos raktas buvo išjungtas, komplektavimo specifikacijų (KS) versijos buvo paslėptos visose formose, ir sistema tarp išleistų produktų ir KS priverstinai taikė ryšį 1:1. Dabartinėje „Dynamics AX‟ versijoje konfigūracijos rakto **KS versijos** išjungti negalima.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Naudojant konfigūracijos raktą KS versijoms kontroliuoti, dydžio keisti debesies aplinkoje negalima. |
| Pakeitė kita funkcija? | Ne                                                                                      |
| Paveikti moduliai             | Produktų informacijos valdymas, Atsargų valdymas                                    |

### <a name="brazilian-bordero"></a>Brazilijos „Bordero“

Konkretus mokėjimo būdas, skirtas Brazilijos įmonėms

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Brazilijos „Bordero“ mokėjimo būdo lokalizavimas nebepalaikomas |
| Pakeitė kita funkcija? | Nr.                                                                                                    |
| Paveikti moduliai             | Mokėtinos sumos                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brazilijos „Sintegra“ išrašas

ICMS mokesčio federalinių mokesčių ataskaita

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Šis išrašas kai kuriose Brazilijos apskrityse nebetaikomas.                                                     |
| Pakeitė kita funkcija? | Nr. Vartotojai gali naudoti įrankį Bendrosios elektroninės ataskaitos, norėdami konfigūruoti išrašą, jei to reikalaujama konkrečiose situacijose. |
| Paveikti moduliai             | Finansų knygos                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brazilijos SCAN atsakomųjų priemonių režimas, skirtas NF-e

(SCAN) atsakomųjų priemonių režimas naudojamas norint generuoti, eksportuoti ir importuoti „Nota Fiscal eletrônica“ (NF-e) būseną, kai „Secretaria da Fazenda“ (SEFAZ) režimo naudoti negalima.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Šis atsakomųjų priemonių metodas nebetaikomas nė vienoje Brazilijos apskrityje |
| Pakeitė kita funkcija? | Nr.                                                                          |
| Paveikti moduliai             | Gautinos sumos                                                         |

### <a name="business-analyzer"></a>Veiklos analizatorius

Ši mobilioji programa naudotojams leidžia peržiūrėti pagrindinę verslo metriką.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Šią funkciją pakeitė kita funkcija.                                                                                                      |
| Pakeitė kita funkcija? | „Microsoft Power BI‟ turinio pakete Stebėti finansinį našumą bus įtraukta pagrindinė finansų metrika, kuri anksčiau buvo prieinama programoje „Business Analyzer‟. |
| Paveikti moduliai             | DK                                                                                                                                                |

### <a name="business-statistics"></a>Verslo statistika

Verslo statistikos užklausų, galinčių padėti analizuoti organizacijos efektyvumą, sąranka

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Senesnės verslo įžvalgų (BI) versijos, mažas klientų naudojimas ir ribotas funkcijų rinkinys |
| Pakeitė kita funkcija? | Nauji dabartinės „Dynamics AX‟ versijos BI sprendimai                                      |
| Paveikti moduliai             | Įsigijimas ir šaltinio parinkimas, Mokėtinos sumos, Pardavimas ir rinkodara, Gautinos sumos         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Keisti dokumento datos funkciją SF patvirtinimo žurnale

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mažai naudojama                                                               |
| Pakeitė kita funkcija? | Taip. Užregistruotos tiekėjo operacijos dokumento datą galima keisti. |
| Paveikti moduliai             | Mokėtinos sumos                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Nyderlandų mokėjimo formatas ClieOp03

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Formatas Nyderlanduose nebetaikomas, nes jį pakeitė (SEPA) funkcija. |
| Pakeitė kita funkcija? | SEPA mokėjimų eksportas                                                                                       |
| Paveikti moduliai             | Visi                                                                                                        |

### <a name="compliance-center"></a>Atitikties centras

Atitikties centras buvo įmonės portalo svetainė, skirta valdyti atitikties iniciatyvų, susijusių su Sarbanes-Oxley įstatymu, dokumentų reikalavimams.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Naudojo mažai klientų. „Microsoft SharePoint‟ apima tuos pačius pajėgumus, kurie buvo prieinami atitikties centre. |
| Pakeitė kita funkcija? | Ne                                                                                                                     |
| Paveikti moduliai             | Atitikties ir vidiniai valdikliai                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>„Microsoft Dynamics“ jungtis

Šis įrankis buvo naudojamas integruoti pagrindiniams duomenims iš „Microsoft Dynamics CRM‟ į „Microsoft Dynamics ERP‟ programas.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Nebenaudojimo priežastis       | Šią funkciją pakeitė kita funkcija. |
| Pakeitė kita funkcija? | Dynamics Integrator                                      |
| Paveikti moduliai             | „Microsoft Dynamics“ jungtis                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Turimas konteinerių vienetas ir kelios dimensijos

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Besidubliuojančios funkcijos                                                                                                                                         |
| Pakeitė kita funkcija? | Taip. Nuo AX 2012 šią funkciją pakeitė konsoliduotųjų paketinius užsakymų funkcijų rinkinys. Šis funkcijų rinkinys apima konsoliduotąjį turimų objektų rodinį. |
| Paveikti moduliai             | Produktų informacijos valdymas, Gamybos kontrolė, Atsargų valdymas, Pardavimas ir rinkodara                                                                   |

### <a name="cue-group-metadata"></a>Eilių grupės metaduomenys

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Eilių grupės buvo naudojamos rodyti vienai ar kelioms Eilėms „FactBox‟ srityje. Naudojimas buvo ribotas, taip pat buvo našumo klausimų, kadangi pirminės formos įrašo pakeitimas lėmė vieną Eilės užklausą Eilių grupėje. |
| Pakeitė kita funkcija? | Ne                                                                                                                                                                                                                            |
| Paveikti moduliai             | Visi                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Eilių metaduomenys

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Eilių metaduomenys buvo apriboti skaičių ar sumos informacija.                                                                                                                                                                                   |
| Pakeitė kita funkcija? | Plytelių metaduomenys buvo įdiegti siekiant suteikti daugiau modeliavimo lankstumo. Pavyzdžiui, galite modeliuoti dabartinius skaičiavimus, naršymą ir pagrindinius našumo indikatorius (KPI). Skaičiavimo plytelių metaduomenys tiesiogiai pakeičia Eilių metaduomenis. |
| Paveikti moduliai             | Visi                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Daniška čekio forma

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Danijos čekio formato maketo palaikymas nutrauktas, o ataskaita pašalinta iš DK lokalizacijos. |
| Pakeitė kita funkcija? | Ne                                                                                                                      |
| Paveikti moduliai             | Visi                                                                                                                     |

### <a name="data-partitions"></a>Duomenų skaidiniai

Naudojant duomenų skaidinius duomenys logiškai suskaidomi „Microsoft Dynamics AX“ duomenų bazėje.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Duomenų skaidiniai pristatyti „Microsoft Dynamics AX 2012 R2“, kad būtų galima duomenis atskirti. Įprastu scenarijumi įmonė turi dukterinių įmonių ir vienos dukterinės įmonės duomenų kita dukterinė įmonė neturėtų matyti, nors abi dukterinės įmonės valdomos to paties IT skyriaus. Tačiau visoje programoje buvo reikalingi papildomi scenarijai ir pridėtinės valdymo išlaidos, siekiant sukurti naujus skaidinius ir užpildyti juos duomenimis bei sukurti skaidinio duomenų atsarginę kopiją. Debesyje teikiama prieiga prie paslauginės platformos duomenų bazės tarnybų („Microsoft Azure“ SQL duomenų bazės), todėl tai yra daug efektyvesnis būdas duomenų bazę naudoti kaip atskirtą konteinerį negu atskyrimą atlikti programoje. Nesvarbu, ar duomenų skaidymas reikalingas dukterinėms įmonėms, keliems nuomininkams, ar tiesiog dėl masto, manome, kad scenarijus galima tvarkyti geriau naudojant kelias duomenų bazes arba kelis „Dynamics AX“ egzempliorius. |
| Pakeitė kita funkcija? | Ateities leidimuose duomenų skaidinius pakeis galimybė naudoti kelias duomenų bazes arba „Dynamics AX“ egzempliorius.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Paveikti moduliai             | Visi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

### <a name="delimitation"></a>Apribojimas

|                              |                                        |
|------------------------------|----------------------------------------|
| Nebenaudojimo priežastis       | Funkcijomis nesinaudota. |
| Pakeitė kita funkcija? | Ne                                     |
| Paveikti moduliai             | Laikas ir buvimas darbe                    |

### <a name="desktop-client"></a>Darbalaukio klientas

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | „Dynamics AX‟ kliento patirtis perkurta, siekiant pagerinti naudojimą keliose platformose ir įrenginiuose.                      |
| Pakeitė kita funkcija? | Naujasis žiniatinklio klientas paremtas darbalaukio formos metaduomenimis ir programavimo modeliu, kurie modifikuoti siekiant suteikti turiningą žiniatinklio platformą. |
| Paveikti moduliai             | Visos                                                                                                                                    |

### <a name="direct-database-connection"></a>Tiesioginis duomenų bazės ryšys

Programoje „Dynamics AX 2012 R3“ „Retail Modern POS“ gali tiesiogiai prisijungti prie kanalo duomenų bazės panašiai kaip įmonės EKA. Tai yra papildomas ryšio metodas, teikiamas kartu su standartiniu „Retail Modern POS“ ryšio per „Retail Server“ metodu.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Tiesioginiam duomenų bazės ryšiui reikia žemesnio lygio saugos protokolų ir jis daugiausia buvo naudojamas siekiant aukščiausio lygio efektyvumo. Dėl „Dynamics 365 Finance and Operations‟ įdiegtų efektyvumo ir saugos patobulinimų dabar ši funkcija sukelia daugiau problemų, negu išsprendžia. |
| Pakeitė kita funkcija? | Nr. Dabar palaikomas tik standartinis „Retail Server“ ryšys.    |
| Paveikti moduliai             | Kanalo duomenų bazė / „Retail Modern POS“                                    |

### <a name="dutch-swift-mt940"></a>Nyderlandų SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Vietoj lokalizuotų funkcijų dabar naudojamos bendrosios funkcijos.                                                                                                                                                                 |
| Pakeitė kita funkcija? | Taip, šią funkciją pakeitė funkcija Išplėstinis banko suderinimas. Be to, su kitu „Dynamics AX“ atnaujinimu Bendrajam žurnalui planuojama įgyvendinti camt.053 ISO20022 sąskaitos išrašo importavimą. |
| Paveikti moduliai             | Visi                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>„eBilanz‟ (Vokietijos XBRL)

Ši funkcija teikė išplėstinės verslo ataskaitų kalbos (XBRL) išeigą, kuri skirta konkrečiai Vokietijos „eBilanz‟ taksonomijai.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Naudojo mažai klientų                                                                                                                                                 |
| Pakeitė kita funkcija? | Ši funkcija nėra pakeista kita funkcija, o Vokietijos rinkai prieinami keli specializuoti XBRL paketai, kurie teikia XBRL funkcijas. |
| Paveikti moduliai             | „Management Reporter“                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Įmonės portalo klientas

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Suteikta viena kliento platforma.                                                                                            |
| Pakeitė kita funkcija? | Naujasis žiniatinklio klientas paremtas darbalaukio formos metaduomenimis ir programavimo modeliu, kurie modifikuoti siekiant suteikti turiningą žiniatinklio platformą. |
| Paveikti moduliai             | Visi                                                                                                                                    |

### <a name="environmental-sustainability"></a>Aplinkos tvarumas

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| Nebenaudojimo priežastis       | Naudojo mažai klientų ir ribotas funkcijų rinkinys       |
| Pakeitė kita funkcija? | Ne                                                 |
| Paveikti moduliai             | Atitikties ir vidiniai valdikliai, Mokėtinos sumos |

### <a name="form-activex-and-managed-host-controls"></a>Forma „ActiveX‟ ir Tvarkomo pagrindinio kompiuterio valdikliai

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | „ActiveX‟ ir Tvarkomo pagrindinio kompiuterio valdikliai paremti pasenusiu darbalaukio klientu.                                                                                                             |
| Pakeitė kita funkcija? | Išplečiamoji valdymo sistema palaiko naujų valdiklių, paremtų HTML, CSS ir „JavaScript‟, kūrimą ir yra aukščiausios klasės valdiklis „Microsoft Visual Studio‟ įrankių aplinkoje. |
| Paveikti moduliai             | Visi                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Generuoti išankstinius pranešimus naudojant paketą

Išankstinių pranešimų generavimo negalima atlikti naudojant paketą, bet jį vis dar gali atlikti naudotojas.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Nėra jokios formos, kurioje išliktų ir būtų rodomas gautas išankstinis pranešimas, kai jis generuojamas naudojant paketą. |
| Pakeitė kita funkcija? | Išankstiniai pranešimai vis dar gali būti generuojami, ir naudotojas gali kontroliuoti vietą, kur failas įrašomas.   |
| Paveikti moduliai             | Mokėtinos sumos, Gautinos sumos, Grynųjų pinigų ir banko valdymas                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Vokietijos DTAUS mokėjimo eksportas ir sąskaitos išrašo importas (bendrosios sumos ir operacijos)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Formatas Vokietijoje nebetaikomas, nes jį pakeitė bendros mokėjimų eurais erdvės (SEPA) funkcija.                                                                                                                                                                 |
| Pakeitė kita funkcija? | Taip, šią funkciją pakeitė SEPA mokėjimo eksportavimo ir išplėstinio banko suderinimo funkcija, skirta importuoti sąskaitų išrašams. Be to, su kitu „Dynamics AX“ atnaujinimu Bendrajam žurnalui planuojama įgyvendinti camt.053 ISO20022 sąskaitos išrašo importavimą. |
| Paveikti moduliai             | Visi                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Vokietijos DTAZV mokėjimo formatas

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Formatas Vokietijoje nebetaikomas, nes jį pakeitė (SEPA) funkcija. |
| Pakeitė kita funkcija? | SEPA mokėjimų eksportas                                                                               |
| Paveikti moduliai             | Visi                                                                                                |

### <a name="german-mt940-import"></a>Vokietijos MT940 importas

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Vietoj lokalizuotų funkcijų dabar naudojamos bendrosios funkcijos.                                                                                                                                                                 |
| Pakeitė kita funkcija? | Taip, šią funkciją pakeitė funkcija Išplėstinis banko suderinimas. Be to, su kitu „Dynamics AX“ atnaujinimu Bendrajam žurnalui planuojama įgyvendinti camt.053 ISO20022 sąskaitos išrašo importavimą. |
| Paveikti moduliai             | Visi                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Vokietijos XML ES pardavimo sąrašas

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | XML formatas, skirtas Vokietijos ES pardavimo sąrašo ataskaitoms, nebepalaikomas. Galima naudoti tik ELMA5 teksto failo formatą, ES pardavimo sąrašo ataskaitai pateikti Vokietijos mokesčių inspekcijai. |
| Pakeitė kita funkcija? | Ne                                                                                                                                                                                 |
| Paveikti moduliai             | Mokesčiai                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>DK SSRS ataskaitos

Ataskaitos, kurios apima šiuos meniu elementus, pašalintos: **Bandomojo balanso suvestinė**, **Išsamus bandomasis balansas**, **Sąskaitų planas**, **Audito sekimas**, **Balansai** ir **Balansų sąrašas**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Finansines „Microsoft SQL‟ serverio ataskaitų tarnybų (SSRS) ataskaitas pakeitė „Management Reporter‟ galimybės ir numatytosios ataskaitos. |
| Pakeitė kita funkcija? | „Management Reporter‟ (dabartinėje „Dynamics AX‟ versijoje pažymėta **Finansinės ataskaitos**)                                                  |
| Paveikti moduliai             | DK                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>„InfoPart‟ ir „FormPart‟ metaduomenys

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | „InfoPart‟ ir „FormPart‟ metaduomenys įgalino „FactBox‟ kūrimą dviem skirtingiems klientams.                                                                                                                                    |
| Pakeitė kita funkcija? | „InfoPart‟ metaduomenys, kurie buvo supaprastinta formos apibrėžtis, konvertuojami į formą naudojant naujinimo įrankius. „FormPart‟ metaduomenis, kurie nurodė į formą, pakeičia labiau tiesioginė nuoroda, kuri sukurta naudojant naujinimo įrankius. |
| Paveikti moduliai             | Visi                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Pagrindinės sąskaitos sąrašo puslapis

Juridinio subjekto sąskaitų ir susijusios balanso informacijos sąrašas

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Balanso informacija pagal sąskaitą ir dimensiją prieinama **Bandomojo balanso** sąrašo puslapyje.                                                                                      |
| Pakeitė kita funkcija? | **Pagrindinėse sąskaitose** yra tas pats sąskaitų sąrašas, kuris buvo **Pagrindinės sąskaitos** sąrašo puslapyje. **Pagrindinių sąskaitų** tinklelio rodinyje taip pat rodomas dar mažesnis, tinklelio vaizdas. |
| Paveikti moduliai             | DK                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaizijos ir Singapūro bankų grynųjų pinigų srauto ataskaita

Ši funkcija naudotojui leidžia spausdinti pinigų srauto ataskaitą, kurioje rodomos pasirinktų banko sąskaitų operacijos ir išsami pinigų įplaukų bei išmokų informacija tam tikru laikotarpiu.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Tą pačią informaciją galima gauti iš Užklausos apie banko operaciją. |
| Pakeitė kita funkcija? | Užklausa apie banko operaciją                                            |
| Paveikti moduliai             | Grynųjų pinigų ir banko valdymas                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikos CFD elektroninė SF

Ši funkcija leido generuoti Meksikos elektronines SF naudojant „Comprobante Fiscal Digital‟ (CFD) metodą, kai įmonė pasirašo SF reikalaudama susijusio autorizavimo iš vyriausybės. Ši funkcija taip pat pateikia mėnesio ataskaitą, kurioje įtrauktos visos elektroninės SF, išduotos tuo laikotarpiu.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Šis metodas nebetaikomas. Elektroninių sąskaitų faktūrų generavimas naudojant CFD metodą nebenaudojamas, nes mokesčių institucijos jį pakeitė Comprobante Fiscal Digital a través de Internet (CFDI) metodu, kuriuo pasirašymas perduodamas trečiosios šalies teikėjui (PAC). Mėnesio ataskaita pašalinta, o užklausos parinktis naudotojams leidžia paklausti apie praeities operacijas. |
| Pakeitė kita funkcija? | Ne                                                                                                                                                                                                                                                                                                                                                                                                        |
| Paveikti moduliai             | Gautinos sumos, Projektas                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksikos sumokėtas ir nesumokėtas PVM

„Microsoft Dynamics AX 2012‟ nesumokėtą pridėtinės vertės mokestį (PVM) valdė naudodama tik Meksikai skirtas „nesumokėto mokesčio" funkcijas.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Besidubliuojančios funkcijos                                                                                             |
| Pakeitė kita funkcija? | Taip, šią funkciją pakeitė standartinė sąlyginio PVM funkcija, kurią teikia „Core‟. |
| Paveikti moduliai             | Mokesčiai                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>„Microsoft Outlook“ integravimas

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Šią funkciją pakeitė „Microsoft Exchange Server“ integracija. |
| Pakeitė kita funkcija? | Taip                                                                            |
| Paveikti moduliai             | Pardavimas ir rinkodara                                                            |

### <a name="payroll-information-in-human-resources"></a>Algalapio informacija Žmogiškuosiuose ištekliuose

Žmogiškųjų išteklių Algalapio informacija

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Šią funkciją pakeitė pagrindiniai puslapiai Algalapis ir Žmogiškieji ištekliai.                                                                                                                                                                                                                                              |
| Pakeitė kita funkcija? | **Išmokų**, **Pajamų** ir kiti susiję puslapiai, kurie anksčiau buvo JAV algalapyje, perkonfigūruoti ir dabar yra pagrindinės Žmogiškųjų išteklių konfigūracijos dalis, siekiant padėti teikti palaikymą išoriniam algalapių apdorojimui. Ši funkcija pasiekiama naudojant konfigūracijos raktą **1 žmogiškieji ištekliai** &gt; **Algalapis**. |
| Paveikti moduliai             | Žmogiškieji ištekliai, Algalapis                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Privatus atsargų ir sandėlio valdymo žurnalų blokavimas

Atsargų ir sandėlio žurnalai nebepalaiko galimybės pasirinkto naudotojo žurnalą pažymėti kaip privatų. Palaikomas tik naudotojų grupių privačių žurnalų blokavimo procesas ir blokavimas redaguojant.

|                              |                                        |
|------------------------------|----------------------------------------|
| Nebenaudojimo priežastis       | Funkcijomis nesinaudota. |
| Pakeitė kita funkcija? | Ne                                     |
| Paveikti moduliai             | Atsargų valdymas                   |

### <a name="product-builder"></a>Produkto generatorius

Produkto generatorius buvo naudojamas dinamiškai konfigūruoti prekėms iš pardavimo užsakymo, pirkimo užsakymo, gamybos užsakymo, pardavimo pasiūlymo, projekto pasiūlymo ar prekės reikalavimo. Pagal produkto modelį, turintį modeliavimo kintamųjų, naudotojas galėdavo pasirinkti reikšmes, kurios atitikdavo kliento reikalavimus ir gauti unikalų produkto variantą, turintį KS ir maršrutą.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Produkto generatorius X++ kodą rodydavo galutiniams naudotojams ir dabartinėje „Dynamics AX‟ versijoje nėra palaikomas. Jis pašalintas siekiant išvengti besidubliuojančių priežiūros darbų sutampančiose, keičiamo dydio kodų bazėse. |
| Pakeitė kita funkcija? | Produkto konfigūracija                                                                                                                                                                                   |
| Paveikti moduliai             | Produktų informacijos valdymas, Pardavimas ir rinkodara                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Pervardyti produkto dimensiją

Ši funkcija leidžia pakeisti vienos iš trijų standartinių produktų dimensijų (dydžio, spalvos arba stiliaus) pavadinimą į tokį, kuris geriau tinka jūsų verslo poreikiams. Pervardijimas apėmė visas etiketes, kuriose buvo naudojamas produkto dimensijos pavadinimas.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Dabartinė „Dynamics AX‟ versija nepalaiko etikečių keitimo vykdymo metu. |
| Pakeitė kita funkcija? | Nr.                                                                            |
| Paveikti moduliai             | Produkto informacijos valdymas                                                |

### <a name="retail-server-connectivity-using-http"></a>„Retail Server“ ryšys naudojant HTTP

Programoje „Dynamics AX 2012 R3“ „Retail Server“ galėjo veikti naudojant HTTP ryšį (nesaugų). Tai buvo papildomas metodas, teikiamas kartu su standartiniu ryšiu naudojant HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Dėl naujų saugos reikalavimuų dabar palaikomas tik saugus ryšys naudojant TLS 1.2 (arba naujesnę versiją, jei yra). Savitarnos diegimo programa automatiškai sukonfigūruos kompiuterį šiam ryšiui užmegzti. |
| Pakeitė kita funkcija? | Nr. Dabar palaikomas tik standartinis HTTPS ryšys.                                                                           |
| Paveikti moduliai             | Parduotuvės serveris                                                |

### <a name="role-center-pages"></a>Vaidmenų centrų puslapiai

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Vaidmenų centrų puslapiai buvo sukurti pasenusioje įmonės portalo platformoje, kurią dabartinėje „Dynamics AX‟ versijoje pakeitė naujoji žiniatinklio kliento programa. |
| Pakeitė kita funkcija? | Naujasis Darbo srities formos modelis naudotojams pateikia į procesą orientuotą dizainą, kuris suteikia lengvą prieigą prie dažniausiai naudojamų užduočių tame procese.                       |
| Paveikti moduliai             | Visi                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>PVM jurisdikcijos

|                              |                                              |
|------------------------------|----------------------------------------------|
| Nebenaudojimo priežastis       | Naudojo mažai klientų ir ribotas funkcijų rinkinys |
| Pakeitė kita funkcija? | Ne                                           |
| Paveikti moduliai             | JAV PVM                                 |

### <a name="shipping-carrier-interface"></a>Vežėjo sąsaja

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Besidubliuojančios funkcijos                                                                                                                         |
| Pakeitė kita funkcija? | Taip, šią funkciją iš dalies pakeitė Transportavimo valdymas, bet dar nepakeitė pagrindinis Sandėlio valdymas (WMS I). |
| Paveikti moduliai             | Pardavimas ir rinkodara, Atsargų valdymas                                                                                                       |

### <a name="sites-services"></a>„Sites Services“

„Sites Services“ leidžia kurti svetaines, išplečiančias jūsų verslo procesus į internetą be IT palaikymo.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | „Microsoft Azure“ infrastruktūra, kurią naudoja „Dynamics AX“, turi naujų galimybių, kurias galima naudoti vietoje jų (pvz., „Azure“ svetainės). |
| Pakeitė kita funkcija? | Ne                                                                                                                                       |
| Paveikti moduliai             | Personalo įdarbinimas, Atvejų valdymas, Pasiūlymų užklausa, Tiekėjo registracija                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS poreikio prognozės strategija

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Naujoje debesies architektūroje funkcijos dizainas nepalaikomas. |
| Pakeitė kita funkcija? | „Azure“ mašininio mokymo poreikio prognozės strategija                           |
| Paveikti moduliai             | Planavimas                                                                     |

### <a name="travel-requisitions"></a>Kelionės paraiškos

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mažai naudotasi ir dauguma funkcijų buvo įmonės portale. |
| Pakeitė kita funkcija? | Ne                                                              |
| Paveikti moduliai             | Išlaidų valdymas                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Tiekėjo SF telkinys be registravimo informacijos

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mažai naudotasi. Ši funkcija buvo pakeista SF žurnalu, kuriame yra darbo eigos funkcija. |
| Pakeitė kita funkcija? | SF žurnalo darbo eigos galimybės.                                                           |
| Paveikti moduliai             | Mokėtinos sumos                                                                                        |

### <a name="virtual-company-accounts"></a>Virtualios įmonės

Virtualių įmonių funkcija programoje „Dynamics AX‟ nebepalaikoma. Virtualių įmonių funkcija naudotojams leidžia nustatyti lenteles, kurias gali bendrai naudoti įmonių grupė. Funkcijos aprašo žr.: [Įmonių sąskaitos ir Virtualių įmonių sąskaitos](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funkcija veikia grupuodama lenteles į rinkinius, kurie yra priskiriami virtualioms įmonėms, kurios yra esamų „tikrų‟ įmonių grupės. Užklausos kuriamos taip, kad visos įmonės virtualioje įmonėje galėtų prieiti prie lentelių duomenų, susietų lentelių rinkiniuose.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Nebenaudojimo priežastis</td>
<td><ul>
<li>Prieš lentelėse saugant duomenis, reikia nustatyti virtualias įmones. Virtualias įmones pertvarkyti į esamą diegimą yra labai sunku.</li>
<li>Kadangi dabartinėje „Microsoft Dynamics AX‟ versijoje buvo tiek daug duomenų normalizavimo, pasidarė sudėtinga sužinoti, ką įtraukti į lentelių rinkinius. Pvz., sunku žinoti, kurias lenteles bendrai naudoti. Taip pat reikia pridėti visas lenteles, į kurias nurodoma iš lentelių, esančių virtualioje įmonėje. Dėl lentelių normalizavimo net paprasti bendrieji duomenys, paskirstyti daugybėje lentelių, turi būti virtualios įmonės dalis. Bet kokia čia padaryta klaida sukels funkcinių problemų.</li>
<li>Kai lentelė yra virtualios įmonės dalis, ji praranda informaciją apie duomenų šaltinį, ir įrašoma tik virtuali įmonė.</li>
</ul></td>
</tr>
<tr class="even">
<td>Pakeitė kita funkcija?</td>
<td>Kad lentelės būtų pasiekiamos iš visų įmonių, gali būti naudojamos visuotinės lentelės. Šiuo metu nėra pakeitimo.</td>
</tr>
<tr class="odd">
<td>Paveikti moduliai</td>
<td>Netaikoma</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>II sandėlio valdymas

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Sandėlio valdymo II sprendimas (WMS II), kuris buvo prieinamas modulyje **Atsargų valdymas**, dubliuoja funkcijas, kurios yra modulyje **Sandėlio valdymas**, kuris buvo išleistas programoje „Microsoft Dynamics AX 2012 R3‟.                                                                         |
| Pakeitė kita funkcija? | Modulis **Sandėlio valdymas**, kuris buvo išleistas programoje AX 2012 R3, „Microsoft Dynamics AX 2012 R3 CU8‟ ir „Microsoft Dynamics AX 2012 R3 CU9‟, pakeičia II sandėlio valdymo funkcijas. Naujasis modulis turi daugiau išplėstinių funkcijų ir lankstesnių sandėlio valdymo procesų nei tie, kurie buvo II sandėlio valdyme. |
| Paveikti moduliai             | Atsargų valdymas, Pardavimas ir rinkodara, Įsigijimas ir šaltinio parinkimas                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Darbuotojų priminimai Žmogiškuosiuose ištekliuose

Žmogiškųjų išteklių Algalapio informacija

|                              |                 |
|------------------------------|-----------------|
| Nebenaudojimo priežastis       | Mažai naudojama       |
| Pakeitė kita funkcija? | Ne              |
| Paveikti moduliai             | Personalas |

### <a name="workplanner"></a>Darbo planuotuvas

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Mažai naudojama                                                                                                                                                            |
| Pakeitė kita funkcija? | Ne, bet puslapis **Šablono ryšys**, kuris atidaromas iš puslapio **Šablonų grupės**, palaiko tą patį verslo scenarijų kaip ir pasenęs puslapis **Darbo planuotuvas**. |
| Paveikti moduliai             | Laikas ir buvimas darbe                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++ finansinės ataskaitos

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| Nebenaudojimo priežastis       | Šią funkciją pakeitė kita funkcija.                                    |
| Pakeitė kita funkcija? | „Management Reporter‟ (dabartinėje „Dynamics AX‟ versijoje pažymėta **Finansinės ataskaitos**) |
| Paveikti moduliai             | DK                                                                              |


