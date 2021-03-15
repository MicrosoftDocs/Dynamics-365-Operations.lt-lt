---
title: Konfigūruoti elektroninių sąskaitų priedus „Regulatory Configuration Services“ (RCS)
description: Šioje temoje paaiškinama, kaip konfigūruoti elektroninių sąskaitų priedus „Dynamics 365 Regulatory Configuration Services“ (RCS).
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: bb4a426bb54ee21197f9954d946d60ea55f5eb76
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104416"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a>Konfigūruoti elektroninių sąskaitų priedus „Regulatory Configuration Services“ (RCS)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie konfigūravimo galimybes elektroninių sąskaitų prieduose „Dynamics 365 Regulatory Configuration Services“ (RCS).

Per galimybių konfigūravimą, kuriuo elektroninės sąskaitos priedas padeda jums atitikti verslo ir reglamentų reikalavimus elektroninėms sąskaitoms be jokio kodavimo. Scenarijų atvejais, kai elektroninės sąskaitos turi būti elektroniniu būdu patvirtintos žiniatinklio paslaugų, konfigūravimo galimybės taip pat jums padeda atitikti reikalavimus pranešimų apsikeitimui su žiniatinklio paslaugomis be jokio kodavimo.

## <a name="electronic-reporting"></a>Elektroninė ataskaita

Elektroninės ataskaitos (ER) palaiko elektroninių sąskaitų priedus.

Duomenų modelio žemėlapio kūrimas ir formatai yra konfigūruojami komponentai, kurie kuriami ir palaikomi per ER ir naudojami elektroninių sąskaitų priede. ER formato kūrimo įrankis yra instrumentas skirtas kurti ir palaikyti failo formatus. Jis naudojamas konfigūruoti elektroninių sąskaitų funkcijas.

Dėl daugiau informacijos, žr. [Elektroninių ataskaitų (ER) apžvalga](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Elektroninės sąskaitos išrašymo funkcijos

Elektroninių sąskaitų funkcijos yra atsakingos už elektroninių sąskaitų kūrimą per elektroninių sąskaitų priedą. Jos įtraukia konfigūracijos taisykles ir naudoja jas duomenims apdoroti, kuriuos „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“ siunčia į elektroninių SF išrašymo priedą ir į elektronines SF.

Priemonės taip pat palaiko scenarijus, kurių reikia, kad būtų laikomasi failo formato specifikacijų, o išeiga yra atskira elektroninė rinkmena. Paprastai rinkmenos formato specifikacijas skelbia mokesčių inspekcija.

Galiausiai priemonės palaiko pranešimų mainus su išorinėmis žiniatinklio paslaugomis, kurias nuomoja mokesčių inspekcija arba kuri nors įgaliota šalis, ir patvirtinimo reikalavimus elektroninėje SF.

### <a name="availability-of-electronic-invoicing-features"></a>Elektroninių SF išrašymo priemonių pasiekiamumas

Elektroninių SF išrašymo priemonių pasiekiamumas priklauso nuo šalies arba regiono. Nors kai kurios priemonės yra bendrai galimos, kitos peržiūrimos.

#### <a name="preview-features"></a>Peržiūros funkcijos

Toliau pateikiamoje lentelėje rodomos šiuo metu peržiūrimos elektroninių SF išrašymo priemonės.

| Šalis/regionas | Funkcijos pavadinimas                         | Verslo dokumentas |
|----------------|--------------------------------------|-------------------|
| Austrija        | Austrijos elektroninės SF (AT)    | Prdavimo SF ir prjekto Sf |
| Belgija        | Belgijos elektroninė SF (BE)      | Prdavimo SF ir prjekto Sf |
| Brazilija         | Brazilijos NF–e (BR)                  | 55 finansinio dokumento modelis, koregavimo laiškai, atšaukimas ir atsisakyta |
| Brazilija         | Brazilijos NFS-e ABRASF Curitiba (BR) | Paslaugų mokestiniai dokumentai |
| Brazilija         | Brazilijos NFS–e San Paulo (BR)       | Paslaugų mokestiniai dokumentai |
| Danija        | Danijos elektroninė SF (DK)       | Prdavimo SF ir prjekto Sf |
| Egiptas          | Egipto elektroninė SF (EG) | Prdavimo SF ir prjekto Sf |
| Estija        | Estijos elektroninė SF (EE)     | Prdavimo SF ir prjekto Sf |
| Suomija        | Suomijos elektroninė SF (FI)      | Prdavimo SF ir prjekto Sf |
| Prancūzija         | Prancūzijos elektroninė SF (FR)       | Prdavimo SF ir prjekto Sf |
| Vokietija        | Vokietijos elektroninė SF (DE)       | Prdavimo SF ir prjekto Sf |
| Italija          | FatturaPA (IT)                       | Prdavimo SF ir prjekto Sf |
| Meksika         | Meksikos CFDI (MX)                    | Pardavimo SF, važtaraščiai, atsargų perkėlimai, mokėjimo papildomi mokėjimai ir atšaukimai |
| Olandija    | Nyderlandų elektroninė SF (NL)        | Prdavimo SF ir prjekto Sf |
| Norvegija         | Norvegijos elektroninė SF (NO)    | Prdavimo SF ir prjekto Sf |
| Ispanija          | Ispanijos elektroninė SF (ES)      | Prdavimo SF ir prjekto Sf |
| Europa         | PEPPOL elektroninė SF            | PEPPOL pardavimo SF ir prjekto SF |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Konfigūruojami elektroninių SF išrašymo priemonių komponentai

Elektroninių SF išrašymo priemones sudaro šios konfigūruojamų komponentų grupės:

- **Formatai** – formatai leidžia konfigūruoti, kuriuos elektroninių SF išrašymo priedą reikia generuoti, kai elektroninis dokumentas tampa elektronine SF. Formatai apima elektroninės SF ir pranešimų, kurie naudojami užklausoms pateikti ir atsakymams gauti, kai reikalingas ryšys su išorine žiniatinklio tarnyba, formato konfigūraciją.
- **Veiksmai** – Veiksmai leidžia konfigūruoti, kaip elektroninio SF išrašymo priedas generuoja elektroninio dokumento, kurį „Finance and Supply Chain Management“ pateikė į elektroninę SF.
- **Taikymo taisyklės** – taikymo taisyklės leidžia konfigūruoti kontekstą, kurį elektroninio SF išrašymo priedas turi apsvarstyti elektroninių SF išrašymo funkcijai apdoroti.
- **Kintamieji** – kintamieji leidžia konfigūruoti konfigūracijos logikos statybos palaikymą. Kintamieji gali veikti kaip verčių įvestis, norint atlikti konkretų veiksmą. Taip pat jie gali veikti kaip „Finance and Supply Chain Management“ ir elektroninių SF išrašymo priedų verčių mainai.
- **Elektroninio dokumento modelio susiejimas** – elektroninio dokumento modelio susiejimas leidžia konfigūruoti ER modelių išdėstymą. Modelio susiejimas nurodo abstrakčios SF, kuri, pateikiama elektroninius dokumentus, yra integruota į elektroninio SF išrašymo priedą, duomenų susiejimą.
- **SF konteksto modelis**– SF konteksto modelis leidžia konfigūruoti ER SF konteksto modelį ir apibrėžti elektroninių SF išrašymo funkcijos kontekstą.
- **Atsakymų tipai**– atsakymų tipai leidžia konfigūruoti tai, ką elektroninio SF išrašymo priedas turi atnaujinti „Finance and Supply Chain Management“, kaip elektroninės SF apdorojimo rezultatą.

### <a name="formats"></a>Formatai

Toliau pateikti sąrašai rodo ER formato konfigūracijas, galimas elektroninių SF išrašymo funkcijoms.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Austrijos (AT) elektroninės SF: Austrijos pardavimo ir projekto SF

- OIOUBL pardavimo SF
- OIOUBL projekto SF
- OIOUBL pardavimo kredito pažyma
- OIOUBL projekto kredito pažyma

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgijos (BE) elektroninės SF: Belgijos pardavimo ir projekto SF

- UBL pardavimo SF BE
- UBL projekto SF BE
- UBL projekto kredito pažyma BE
- UBL pardavimo kredito pažyma BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brazilijos (BR) NF–e: NF-e federalinis (Brazilija)

- NF-e pateikimo eksportavimo formatas (BR)
- NF-e koregavimo laiško eksportavimo formatas (BR)
- NF-e atšaukimo eksportavimo formatas (BR)
- NF-e atmetimo eksportavimo formatas (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brazilijos NFS-e (BR): NFS-e ABRASF Curitiba

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF Užklausa Curitiba (BR)

#### <a name="brazilian-br-nfs-e-nfs-e-so-paulo-city"></a>Brazilian (BR) NFS-e: NFS-e San Paulo miestas

- NFS-e San Paulo (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Danijos (DK) elektroninės SF: Danijos pardavimo ir projekto SF

- OIOUBL pardavimo SF
- OIOUBL projekto SF
- OIOUBL pardavimo kredito pažyma
- OIOUBL projekto kredito pažyma

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Nyderlandų (NL) elektroninės SF: Nyderlandų pardavimo ir projekto SF

- UBL pardavimo SF NL
- UBL projekto SF NL
- UBL projekto kredito pažyma NL
- UBL pardavimo kredito pažyma NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egipto (EG) elektroninės SF: Egipto pardavimo ir projekto SF

- Pardavimo SF (EG)(SF išrašymas)
- Projekto SF (EG)(SF išrašymas)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Estijos (EG) elektroninės SF: Estijos pardavimo ir projekto SF

- Pardavimo SF (EE)
- Projekto SF (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Suomijos (FI) elektroninės SF: Suomijos pardavimo ir projekto SF

- Pardavimo SF (FI)
- Projekto SF (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Prancūzijos (EG) elektroninės SF: Prancūzijos pardavimo ir projekto SF

- UBL pardavimo SF FR
- UBL projekto SF FR
- UBL projekto kredito pažyma FR
- UBL pardavimo kredito pažyma FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Vokietijos (EG) elektroninės SF: Vokietijos pardavimo ir projekto SF

- Pardavimo SF (DE)
- Projekto SF (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Italijos (EG) elektroninės SF: Italijos pardavimo ir projekto SF

- Pardavimo SF (IT)
- Projekto SF (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Meksikos (MX) CFDI: Meksikai skirtas CFDI

- CFDI SF formatas (MX)
- CFDI Pakavimo lapas (MX)
- CFDI Inventoriaus perkėlimas (MX)
- CFDI mokėjimo formatas (MX)
- CFDI SF sąskaitos atšaukimo formatas (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norvegijos (NO) elektroninės SF: Norvegijos pardavimo ir projekto SF

- OIOUBL pardavimo SF
- OIOUBL projekto SF
- OIOUBL pardavimo kredito pažyma
- OIOUBL projekto kredito pažyma

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL elektroninė SF: PEPPOL pardavimo ir projekto sąskaitos

- PEPPOL pardavimo SF
- PEPPOL projekto SF
- PEPPOL pardavimo kredito pažyma
- PEPPOL projekto kredito pažyma

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Ispanijos (ES) elektroninės SF: Ispanijos pardavimo ir projekto SF

- Pardavimo SF (ES)
- Projekto SF (ES)

### <a name="actions"></a>Veiksmai

Šioje lentelėje pateikiami galimi veiksmai ir nurodoma, ar jie šiuo metu yra bendrai pasiekiami, ar vis dar peržiūrimi.

| Operacija                                        | aprašymas                                                                  | Prieinamumas         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Pakeisti dokumentą                            | Vykdyti elektroninės ataskaitos formatą dokumentui transformuoti.                   | Bendrai prieinama  |
| Pasirašyti xml dokumentą                             | Pasirašyti xml dokumentus skaitmeniniu parašu.                                   | Peržiūros režimu           |
| Pasirašyti json dokumentą Egipto mokesčių inspekcijai | Pasirašykite json dokumentus skaitmeniniu parašu Egipto mokesčių inspekcijai.       | Bendrai prieinama  |
| Integruoti su Egipto ETA tarnyba           | Susisiekti su Egipto mokesčių inspekcija.                                     | Bendrai prieinama  |
| Paskambinti Brazilijos SEFAZ tarnybai                  | Integruoti su Brazilijos SEFAZ tarnyba, skirta finansinio dokumento pateikimui.       | Peržiūros režimu           |
| Skambinti Meksikos PAC tarnybai                      | Integruokite su Meksikos ABA tarnyba CFDI pateikimui.                      | Peržiūros režimu           |
| Apdoroti atsakymą                              | Analizuoti iš žiniatinklio tarnybos iškvietimo gautą atsakymą.                     | Bendrai prieinama  |
| Naudoti MS „Power Automate“                         | Integruokite su "Microsoft Power Automate“ sukurtais srautais.                       | Peržiūros režimu           |

## <a name="configuration-providers"></a>Konfigūracijos teikėjai

Konfigūracijos teikėjai suteikia elektroninių SF išrašymo priemones ir jų ER komponentus, pvz., modelio išdėstymą, formato konfigūraciją ir kontekstinį modelį. Jie publikuoja elektroninės SF išrašymo priemones ir ER komponentus susieje visuotinoje saugykloje. Iš ten kitos organizacijos gali jas atsisiųsti.

Prieš konfigūruojant elektroninių SF išrašymo priemones naudojant RCS, reikia konfigūruoti savo organizaciją kaip konfigūracijos teikėją **elektroninių ataskaitų** modulyje. Daugiau informacijos apie tai, kaip konfigūruoti tiekėją į **Aktyvus**, žr. [Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Elektroninių SF išrašymo priemonių peržiūra visuotiniame saugykloje

Norėdami naršyti elektronines SF išrašymo priemones, kurios galimos konkretaus konfigūracijos teikėjo visuotinė saugykloje, sinchronizuokite savo organizacijos RCS egzempliorių. Baigus sinchronizuoti, atnaujinamas galimų elektroninių SF išrašymo priemonių sąrašas.

## <a name="importing-electronic-invoicing-features"></a>Elektroninių SF išrašymo priemonių importavimas

Prieš naudodami arba konfigūruodami elektronines SF išrašymo priemones, turite importuoti jas į savo organizacijos RCS egzempliorių. Importavimo operacija sukuria vietinę priemonių kopiją ir kopijuoja visus ER artefaktus, kuriuos naudoja funkcijos (pvz., formato konfigūracijas ir modelio konfigūracijas) į jūsų organizacijos RCS egzempliorių.

Galite importuoti elektroninių SF išrašymo priemones iš bet kurio konfigūracijos teikėjo.

## <a name="creating-electronic-invoicing-features"></a>Kurti SF išrašymo priemonių funkcijas

Galite kurti elektronines SF nuo pradžių arba išvesti ją iš kito elektroninių SF išrašymo priedo funkcijos.

Kai sukuriate elektroninio SF išrašymo priemonę nuo pradžių, turite rankiniu būdu pridėti ER komponentus (pavyzdžiui, funkcijų versijų konfigūracijas ir kitas konfigūracijas, pavyzdžiui, priemonės versijos nustatymą ir programos nustatymą). Kai sukuriate priemonę išvedę ją iš kitos priemonės, nauja priemonė perima visas konfigūracijas iš originalios. 

## <a name="electronic-invoicing-feature-version"></a>Elektroninių SF išrašymo funkcijos versija

Elektroninių SF išrašymo funkcijos turi versijas. Sukūrus naują versiją, versijos numeris automatiškai padidinamas. Gali būti nustatyta naujos versijos "galiojimo nuo" data.

Elektroninių SF išrašymo priemonių versijos veikia pagal ciklą, kuriame yra iki trijų būsenų:

- **Juodraštis** – jei priemonės versija yra šios būsenos, galite redaguoti jos konfigūracijos atributus ir bet kuriuos jo artefaktus (pvz., failo formato konfigūracijas).
- **Atlikta** – jei šios būsenos funkcijos versija yra tokia, ji buvo publikuota visuotiniame saugykloje, kuri susieta su jūsų organizacija. Nebegalėsite redaguoti priemonės versijos ar jokių ER komponentų.
- **Publikuota** – jei funkcijos versija yra šios būsenos, ji buvo publikuota elektroninio SF išrašymo prieduose. Nebegalėsite redaguoti priemonės versijos ar jokių ER komponentų.

### <a name="feature-configurations"></a>Funkcijų kūrimas

Priemonių konfigūracijose yra visos ER formato konfigūracijos, kurias naudoja elektroninės SF išrašymo priemonės. Visi elektroniniai failai, kuriuos apdorojimo metu naudoja elektroninių SF išrašymo priemonė, gauti iš formato konfigūracijų, kurios buvo pridėtos prie tos priemonės funkcijų konfigūracijų.

Naudodami priemonių konfigūracijas galite prieiti prie ER formato dizainerio, kuris yra ER įrankis, naudojamas formato konfigūracijų kurkite.

### <a name="feature-setup"></a>Funkcijos nustatymas

Priemonių nustatymai naudojami kartu su priemonių konfigūracijoje. Kiekvienos priemonės nustatymas numato veiksmų rinkinį, taikomumo taisykles ir kintamuosius, kurie numato tikėtiną elgseną, kad elektroninių SF išrašymo priemonė galėtų atitikti konkrečius elektroninės SF reikalavimus.

### <a name="application-setup"></a>Programos nustatymas

Programos nustatymas turi būti susietas su anksčiau sukurta prijungta programa.

Naudodami programos nustatymą galite konfigūruoti elektroninių SF išrašymo priemonės dalį, kurią reikia atlikti „Finance and Supply Chain Management“. Mažiausiai trys konfigūruojami komponentai yra privalomi, nepaisant elektroninių SF išrašymo priemonės:

- **Lentelės pavadinimas** – „Finance and Supply Chain Management“ objektas, kuriame yra užregistruotos SF ir pagal kurią yra pagrįsta elektroninio SF išrašymo priemonė.
- **Kontekstas** – SF konteksto modelio, sukonfigūruoto naudojant ER, pavadinimas.
- **Verslo dokumento išdėstymas** – SF išdėstymo modelio, sukonfigūruoto naudojant ER, pavadinimas.

> [!IMPORTANT]
> Konfigūraciją, įvestą programos nustatyme, galima peržiūrėti „Finance and Supply Chain Management“ lange. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametras**. Skirtuke **Elektroninis dokumentas** pasirinkite **Diegti** , tada pasirinkite parinktį **Prijungta** programa.

### <a name="deploying-feature-versions"></a>Funkcijų versijų diegimas

RCS naudojate komandą **Diegti** norėdami publikuoti elektroninių SF išrašymo priemonės versiją paskirties vietai. Rinkitės **Talpinti** ir tuomet rinkitės vieną iš tolesnių parinkčių siekiant nustatyti talpinimo tikslą: 

- **Tarnybos aplinka** – kai diegimo tikslas yra tarnybos aplinka, elektroninio SF išrašymo funkcijos versija publikuojama tarnybos aplinkoje. Elektroninių SF išrašymo priedas yra paruoštas gauti ir apdoroti elektroninius dokumentus, kuriuos siunčia „Finance and Supply Chain Management“.
- **Prijungta programa**– kai diegimo tikslas yra prijungta programa, programos nustatymo pateikta konfigūracija rašoma „Finance and Supply Chain Management“ egzemplioriuje, kuris anksčiau buvo su juo susietas.

Tik elektroninių SF išrašymo funkcijos versijos, kurių būsena yra **Baigta** gali būti įdiegtos paslaugų aplinkoje arba prijungtoje programoje.

### <a name="removing-feature-versions"></a>Funkcijų versijų šalinimas

RCS naudojate **Netalpinti** komandą siekiant pašalinti konkrečią elektroninių sąskaitų funkcijos versiją iš paslaugų aplinkos elektroninių sąskaitų priede.

> [!IMPORTANT]
> **Netalpinti** komanda veikia tik tarnybos aplinkose. Ji neišjungia elektroninių SF išrašymo priemonių versijų iš susijusių programų.

### <a name="rebasing-electronic-invoicing-features"></a>Iš naujo sukurti SF išrašymo priemonių funkcijų pagrindą

Kai viena iš kitos išvedama viena elektroninio SF išrašymo priemonė **Kurti naują pagrindą** komanda atnaujina išvestinę priemonę pakeitimais, kurie buvoįdiegti pradinėje priemonėje.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Išduoti elektronines sąskaitas „Finance and Supply Chain Management”](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]