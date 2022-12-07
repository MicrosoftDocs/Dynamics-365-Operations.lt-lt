---
title: „Store Commerce“ programos galimybės
description: Šiame straipsnyje aprašomos funkcijos, kurių galima naudoti parduotuvės "Commerce" programoje Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788519"
---
# <a name="store-commerce-app-capabilities"></a>„Store Commerce“ programos galimybės

[!include [banner](includes/banner.md)]

Parduotuvės "Commerce" programa yra modernaus kasos taško (EKA) patirtis Microsoft Dynamics 365 Commerce. Tai leidžia įmonėms apdoroti operacijas parduotuvėje ir tvarkyti operacijas biure, pvz., atsargas ir užsakymų vykdymą. Programa taip pat įgalina įmones valdyti ryšius su klientais, kurių veikla lojalumo ir klientų aptarnavimo funkcija. 

Naudojant "Commerce Scale Unit" (CSU), "Store Commerce" programa suteikia visą kanalų sprendimą. Pavyzdžiui, klientas gali pirkti produktą internete ir paimti jį į artimiausią parduotuvę, tokiu būdu tęsti pirkimo kanalus neprarasdamas jokių duomenų. 

Šiame straipsnyje pateikta "Store Commerce" programų galimybių apžvalga.

## <a name="platform"></a>Platforma

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Tamsos kanalas | Dynamics 365 Commerce teikia išsamų programos kanalų sprendimą, kuris suvienodinta įmonės kasos įstaigos, parduotuvės, skambučių centro ir skaitmeninių patirties. | [Peržiūra](index.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Nuotoliniu būdu valdoma prekyba | "Commerce Scale Unit" nuo pagrindinio kompiuterio yra begališkas komercijos modulis. Begalinis komercijos modulis veikia kaip centrinis taškas visoms komercijos verslo logikai ir baigto kanalų sprendimų priėmimo taškas. | <p>[Architektūros apžvalga](commerce-architecture.md)</p><p>[Besigalinė architektūra](dev-itpro/retail-server-architecture.md)</p> | [Technikas](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| „Commerce Headquarters“ | "Commerce Headquarters" suteikia operacijų pajėgumų, kurios leidžia konfigūruoti produktus, darbuotojus, verslo procesus, kainodarą ir kitas verslui reikalingas funkcijas. | [Architektūros apžvalga](commerce-architecture.md) | |
| Point of sale (EKA) | Parduotuvės "Commerce" programa leidžia naudoti EKA Dynamics 365 Commerce. Ji teikia išsamias ir išsamias EKA funkcijas, kurios padeda susieti pardavimus, kasininkus ir vadybininkus teikia teikiančią paslaugas klientams. Be to, ji teikia keletą mažmenininkų diegimo pasirinkčių, padeda pagerinti našumą ir pagerina programos vykdymo ciklo valdymą (LTL). | [Parduotuvės "Commerce" programa](dev-itpro/store-commerce.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Vaizdo](https://youtu.be/7B332XH_zfs)</p><p>[Perkėlimas iš MPOS į parduotuvės komercijos](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Visuotinis debesies diegimas | Keli "Commerce Scale Units" egzemplioriai gali būti įdiegti krovinio paskirstymui ir geografiniam artumą. | [Visuotinė debesies įdiegtis](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Vietinis dislokaumas | Naudojant vietinį verslo duomenų diegimą" "Commerce" klientai gali didesnę "Dynamics 365" aplinkos nuosavybę ir valdymą. | [Vietinė visuotinė įdiegtis](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Įrenginio valdymas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Keli formų koeficientai | Parduotuvės "Commerce" programa palaikoma dėl kelių įrenginių formos faktorių, pvz., kompiuterių, planšetinių kompiuterių ir mobiliųjų įrenginių. Pereinanti vartotojo sąsaja (UI) leidžia maketą automatiškai keisti ir koreguoti pagal ekrano dydį. | [Vaizdinės konfigūracijos](pos-screen-layouts.md) |  |
| Kryžminė platforma | Parduotuvės "Commerce" programa palaikoma žiniatinklyje, "Windows", "iOS" ir platformose Android . | [Platformos](dev-itpro/hybridapp.md) | |
| Prekės ženklo integravimas | Ekrano dizaineris leidžia pritaikyti ekrano maketus, kad jie atitiktų jūsų verslo poreikius. Be to, temas, maketus, spalvas ir vaizdus galima kurti remiantis darbuotojų vaidmenimis ir bendrai naudoti vartotojams, kad prekės ženklai būtų pastovūs ir būtų lengviau naudotis. | [Vaizdinės konfigūracijos](pos-screen-layouts.md) | [Vaizdo](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topologija | Atsižvelgiant į tinklo prieinamumą, palaikomos skirtingos parduotuvės topologija. | <p>[Topologija](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Informacijos grafinis vaizdą](dev-itpro/retail-in-store-topology.md)</p> | |
| Kelių įrenginių valdymas | Iš "Commerce Headquarters" galima lengvai valdyti kelis įrenginius visose parduotuvėse. | [Aktyvinimas](set-up-activation-accounts-validate-devices-hq.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Darbuotojų valdymas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Prisijungti | Kiekvienas parduotuvės darbuotojas gali turėti paskirtą prisijungimą. Prisijungimo tipai apima vartotojo vardą, brūkšninius kodus, magnetinės juostelės skaitytuvą (MSR), biometrinius duomenis ir Azure Active Directory  (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Išplėstinė prisijungimo informacija](extended-logon.md)</p> | |
| Teisės | Darbuotojai palaiko skirtingus teisių lygius, pvz., teisę kurti užsakymus ir redaguoti užsakymus. | [Teisės](tasks/create-pos-permission-groups.md) | |
| Laiko ir lankomumo valdymas | Lankomumas gali būti valdomas naudojant laikrodžio funkciją. Lankomumo duomenis galima apdoroti į algalapį naudojant Dynamics 365 Human Resources programą. | [Laiko valdymas](retail-time-attendance.md) | |
| Pardavimo komisiniai | Pardavimą gali sekti pardavimo atstovas, kad apskaičiuotų komisinius ar kitus skatinaąsias priemones. | [Komisiniai](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Prekyba

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Asortimento valdymas | Prekybos vadovai gali asortimentuoti produktus, kad juos būtų galima parduoti konkrečiame kanale ir konkrečiu laikotarpiu. | [Asortimentai](assortments.md) | |
| Katalogai | Prekybos vadovai gali tvarkyti katalogus, kad jie identifikuos produktus, kuriuos norite pasiūlyti su katalogo kainomis. | [Katalogai](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Produktų ir kategorijų valdymas | Prekybos vadovai "Commerce Headquarters" gali kurti produktus, kurie turi variantų, atributų, matavimo vienetų ir t. t. Jie taip pat gali apibrėžti kategorijų hierarchiją produktams tvarkyti. | [Produktas](retail-hierarchies.md) | |
| Grupavimai | Prekybos vadovai gali grupuoti produktus, kad jie būtų parduodami kaip grupavimas ar rinkinys. | [Rinkiniai](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Informacijos kodai | Norėdami paraginti kasininką įvesti informaciją, atliekant EKA įvairius veiksmus, pvz., prekės pardavimą, prekių grąžinimus arba kliento pasirinkimą, naudokite informacijos kodus. | [Informacijos kodai](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Susietos prekės | Naudokite susietas prekes norėdami perparduoti produktus, kai į operaciją įtraukiama prekė. | [Susietos prekės](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garantijos | Išplėstinės garantijos gali būti parduodamos kartu su produktais. | [Garantija](extended-warranty.md) | |
| Etikečių spausdinimas | Gali būti generuojamos etiketės, kuriose yra produkto informacija, pvz., paketo numeris, serijos numeris ir galiojimo data. | [Etikečių spausdinimas](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Vykdomas pardavimas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Produktų naršymas | Naršyti produktus pagal kategoriją. | [Produktų hierarchija](retail-hierarchies.md) | |
| Produktų paieška | Ieškoti produktų pagal pavadinimus ir patikslinti paieškas naudojant produkto atributus, pvz., prekės ženklą, kainą ir medžiagas. Šią galimybę naudoja "Azure" pagal "Azure" pagal "Azure" užklausą. | [Ieška debesyje](cloud-powered-search-overview.md) | |
| Puslapis Produkto informacija | Raiškiosios produkto informacijos puslapiuose gali būti paveikslėlių, aprašymų, produkto atributų ir rekomenduojamų produktų. Rekomendacijas priima rekomendacijų tarnyba. | | |
| Produktų palyginimas | Palyginkite kelis produktus ir padėkite klientams pasirinkti vieną ir įtraukti juos į operaciją. | | |
| Begališkas perėjimas | Lengvai peržiūrėti atsargas kitose parduotuvėse ir kurti užsakymus. | [Atsargų peržvalga](pos-inventory-lookup-operation.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Rekomendacijos | Perduoti ir kryžminio pardavimo produktus naudojantis rekomendacijų tarnyba. Ši paslauga naudoja patentuotą technologiją, kad siūlytu rekomendacijas, paremtas pirkimo tendencijomis ir charakteristikomis, tokiomis kaip naujai pristatyta, panašia ir geriausia. Šios rekomendacijos pateikiamos informacijos apie produktą puslapiuose, kliento **informacijos** puslapyje ir **operacijų** puslapyje. | [Rekomendacijos](product-recommendations.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Ryšys su klientais

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Klientų valdymas | Kurti, redaguoti ir valdyti klientų sąskaitas. Kliento sąskaitas galima valdyti "async" režimu, kad nebūtų apdorojama realiuoju laiku. | [Valdymo](customer-mgmt-stores.md) | |
| Kliento atributai | Kliento atributų sistema leidžia fiksuoti papildomus su klientu susijusius duomenis remiantis verslo reikalavimais. | [Atributai](dev-itpro/customer-attributes.md) | |
| Išsamios kliento informacijos puslapis | Raiškiosios kliento informacijos puslapis pateikia kliento sąveikos kanalų ir visų kanalų sąveiką. Šie sąveika apima pirkimą, pageidavimų sąrašus ir lojalumo taškus. | | |
| Debesija paremta kliento paieška | Ieškoti klientų pagal vardą, telefono numerį, el. pašto adresą, lojalumo kortelę, adresą ir t. t. | [Ieška debesyje](pos-search-improvements.md#customer-search) | |
| Lojalumas ir atlygis | Klientai gali prisijungti prie lojalumo programų ir uždirbti bei panaudoti lojalumo taškus kanaluose. | [Lojalumas](set-up-customer-loyalty-program.md) | [Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Ryšiai su klientais | Valdyti pagrindinius klientus naudojant klientų knygą, sekti veiklas ir pastabas kliento profilyje. Dynamics 365 Customer Insights integracija leidžia parduotuvės darbuotojams gauti eiles apie kitą geriausią kiekvieno kliento veiksmą. | [Ryšiai su klientais](clienteling-overview.md#activities-and-notes) | [Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Kainodara ir nuolaidos

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Prekybos sutartys | Kainų vadybininkai gali naudoti prekybos sutartis, norėdami apibrėžti specialias kainas, remsis ilgalaikėmis tam tikrų klientų sutartimis. | [Kainodara](price-management.md)| [Vaizdo](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Pardavimo sutartys | Kainų vadybininkai gali naudoti pardavimo sutartis apibrėžti su sutartimi paremtas kainas "verslas verslui" (B2B) komercijos scenarijuose. | [Kainodara](price-management.md) | |
| Kainos koregavimai | Kainų vadybininkai gali naudoti kainų koregavimo galimybę, norėdami kurti, sekti ir valdyti savo produktų kainų antkainį. | [Kainos koregavimai](price-adjustments-discounts.md) | |
| Nuolaidos | Kainų vadybininkai gali nustatyti kelių tipų nuolaidas, norėdami vykdyti įvairias akcijas. Šios nuolaidos apima paprastas nuolaidas, kiekio nuolaidas, ribines nuolaidas, nuolaidas prekių kiekiui, nuolaidas prekių kiekiui, mokėjimo priemonių nuolaidas ir siuntimo nuolaidas. | [Nuolaidos](retail-discounts-overview.md) | |
| Kuponai | Kainų vadybininkai gali nustatyti kupono kodus arba brūkšninius kodus, susieti juos su nuolaidomis ir paskirstyti juos klientams. Su pardavimu susieti kuponai gali būti įtraukti į pardavimo operacijas arba pašalinti juos. | [Kuponai](coupons.md) | |
| Kainų grupės | Kainų vadybininkai gali naudoti kainų grupės galimybę apibrėžti kontekstines kainas, paremtas kanalais, katalogais, priskyrimais ar lojalumo programomis. | [Kainodara](price-management.md) | |
| Galimos akcijos | Pagal pardavimo susiejimus galima lengvai ieškoti galimų parduotuvės produktų akcijų, į operaciją įtraukti produktai ir t. t. | [Kainos funkcijos](pos-pricing-functions.md) | |
| Kainos tikrinimai | Pardavimo susiejimai gali greitai patikrinti aktyvias parduotuvėje saugomų produktų pardavimo kainas. | [Kainos funkcijos](pos-pricing-functions.md) | |
| Kainų perrašymai | Pardavimas susieja, kas turi reikiamas teises gali perrašyti sistemos konfigūruotas arba apskaičiuotas kainas. | [Kainos funkcijos](pos-pricing-functions.md) | |
| Rankiniu būdu taikomos nuolaidos | Pardavimas susieja, kas turi reikiamas teises, gali taikyti rankiniu būdu taikomas nuolaidas pardavimo operacijai arba pardavimo eilutėms. | [Kainos funkcijos](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektroniniai mokėjimai

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Kreditas ir debetas | Parduotuvės komercijos programa palaiko pagrindinius mokėjimus kredito ir debeto kortelėmis naudojant Adyen mokėjimo šliuzą ir užsakymų įvykdyimą naudojant PayPal. Mokėjimų SDK leidžia naudoti išorinių šliuzų ryšius, kuriuos palaiko nepriklausomas programinės įrangos tiekėjo (ISV) integravimas. | <p>[„Adyen“](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[Paypal](paypal.md)</p><p>[Mokėjimai](payment-methods.md)</p> | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Skaitmeninis palaikymas | Parduotuvės "Commerce" programa palaiko mokėjimus skaitmeniniais metodais ir naudoja nenaudodama banko identifikavimo numerio (BIN) diapazonų kaip tradicinės kredito ir debeto kortelės. Mokėjimo būdai gali būti susieti su skaitmeniniais mokėjimais, pvz., Adyen. | [Piniginė](wallets.md) | |
| Dovanų kortelės palaikymas | Banko identifikavimo numeris "Dynamics 365" dovanų kortelė, saugoma vertės sprendimai (SVS) ir "Givex" dovanų kortelės. Dovanų korteles galima įsigyti ir pateikti užsakyme. | [Dovanų kortelės](dev-itpro/gift-card.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Apsauga nuo sukčiavimo | Dynamics 365 Fraud Protection padės jums išvengti apgaulingos veiklos ir nustatyti vietas, kuriose apgaulė gali būti nepaisoma. | [Apsauga nuo sukčiavimo](dev-itpro/dfp.md) | [Vaizdo](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Mokesčiai ir išlaidos

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Mokesčiai | Parduotuvės "Commerce" programa palaiko daug netiesioginių mokesčių tipų, pvz., PVM, pridėtinės vertės mokestį (PVM), prekių ir paslaugų mokestį (GST), vieneto mokesčius ir išskaitomų mokesčių. | [Mokesčiai](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Išlaidos | Išlaidas galima konfigūruoti eilutės lygyje, antraštės lygyje, kaip automatinius mokesčius, pagal kanalą ir t. t. | [Mokesčiai](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Užsakymo apdorojimas ir įvykdyimas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Užsakymo kūrimas | Užsakymas gali būti sukurtas siuntimui ar paėmimui artimiausioje parduotuvėje. Galima pateikti paėmimo laiko atminties atminties. | [Peržiūra](customer-orders-overview.md) | |
| Užsakymo modifikavimas | Užsakymas gali būti modifikuojamas, grąžinamas, atšaukiamas ir t. t. | <p>[Atšaukti](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Grąžinimai](pos-returns.md)</p> | |
| Paieška | Ieškoti užsakymų ir juos filtruoti naudojant konkretaus užsakymo informaciją. | [Paieška](enhancedorderrecall.md) | |
| Užsakymų atributai | Užsakymo atributų sistema leidžia fiksuoti papildomą su užsakymu susijusią informaciją remiantis verslo reikalavimais. | [Atributai](dev-itpro/order-attributes.md) | |
| Tiesioginis pristatymas | Prekes galima pažymėti kaip tiekėjo tiesioginio pristatymo prekes kliento adresu. Tiesioginis pristatymas taip pat vadinamas pristatymu. | [Tiesioginis pristatymas](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Pasiūlymas | Parduotuvės darbuotojai gali kurti klientams pasiūlymus ir gali nurodyti specialią kainą, rankiniu būdu nustato nuolaidas ir pasiūlymo galiojimo datą. | [Pasiūlymas](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Įvykdymas | Parduotuvės gali paimti, pakuoti ir siųsti užsakymus. Važtaraštis gali būti pridėtas prie paruoštų siuntimui pakuočių. | [Įvykdymas](order-fulfillment-overview.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[Vaizdo](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Paskirstytų užsakymų tvarkymas | "Store Commerce" programa palaiko intelektualų užsakymų įvykdymo optimizavimą, kai verslo strategijas galima konfigūruoti pagal verslo pobūdį, kliento tipą, užsakymo kilmę ir užsakymo pristatymo metodą. | [DOM](dom.md) | [Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Atsargų valdymas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Skirstymas pirkėjams | Supaprastinti galimų atsargų paskirstymą iš paskirstymo centro į kelias parduotuves ar sandėlius. | [Skirstymas pirkėjams](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Prekių skirstymas | Supaprastinti atsargų paskirstymą gaunamuose pirkimo užsakymuose į kelias parduotuves ar sandėlius. | [Prekių skirstymas](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Gaunamos atsargos | Gauti atsargas iš tiekėjo per pirkimo užsakymą arba iš kito sandėlio naudojant perkėlimo užsakymą. Sukurkite gaunamo pirkimo užsakymo ar perkėlimo užsakymo užklausą. | [Gaunama](pos-inbound-inventory-operation.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Siunčiamos atsargos | Siųsti atsargas į kitą sandėlį perkėlimo užsakymu ir sukurti siunčiamo perkėlimo užsakymo užklausą. | [Siunčiama](pos-outbound-inventory-operation.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Atsargų peržvalga | Patikrinti turimas produktų atsargas parduotuvėse ir sandėliuose ir patikrinti galimas atsargų (ATP) atsargas ateities datas. | [Atsargų peržvalga](pos-inventory-lookup-operation.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Atsargų koregavimas | Koreguoti atsargas į parduotuvės sandėlį arba iš jo, kad jos atitiktų konkrečius verslo poreikius, nenaudojant pardavimo, gavimo arba sąskaitos. | [Atsargų koregavimas](work-with-store-inventory.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Inventorizacijos | Skaičiuoti faktines atsargas ir koreguoti sistemos buhalterines atsargas, kad jos sutaptų. | [Skaičiavimas](work-with-store-inventory.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Atsargų perkėlimas | Perkelti atsargas iš vienos parduotuvės vietos į kitą. | [Judėjimas](work-with-store-inventory.md) | <p>[Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Vaizdo](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Finansai

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Grynųjų valdymas | "Store Commerce" programa palaiko grynųjų pinigų ir kitų nurodytų mokėjimo priemonių tvarkymą parduotuvėje. Be to, parduotuvės pamainos suderinimas gali būti įgalintas, kad būtų galima išplėsti grynųjų pinigų valdymo galimybes. | [Grynieji pinigai](cash-mgmt.md) | |
| Finansinės ataskaitos ir suderinimas | Parduotuvės grynųjų pinigų ir operacijų operacijos įrašomos "Commerce Headquarters" vykdant išrašo registravimo procesus. | [Pareiškimai](retail-statements.md) | |
| Pajamų ir išlaidų operacijos | Apdorokite smulkias grynųjų pinigų operacijas parduotuvėje ir įrašykite pajamas, kurios neateis į tradicinį būdą, pvz., prarastus ir surastas pinigus, įplaukų iš jūsų drabužių parduotuvės dalį ir pasikeisite valymo paslaugas. | [Pareiškimai](retail-statements.md) | |
| SF mokėjimai | Fiksuoti mokėjimus pagal SF. | [PVM sąskaita faktūra](payinvoice.md) | |

## <a name="employee-productivity"></a>Darbuotojo produktyvumas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Užduočių valdymas | Sukurkite užduočių sąrašus ir užduotis bei priskirkite juos parduotuvėms ir darbuotojams. Sekite užduočių būsenas parduotuvėse. Pateikiamas nuoseklios Microsoft Teams integracijos procesas. | <p>[Užduočių valdymas](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Vaizdo](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Aparatūra ir išoriniai įrenginiai

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Prijungti išorinius įrenginius | Prijungti išorinius įrenginius, pvz., spausdintuvus, kasų stalčius, skaitytuvus ir mokėjimo įrenginius, prie EKA terminalo. | [Išorinis įrenginys](retail-peripherals-overview.md) ||
| Bendrai naudoti išorinius įrenginius | Kvitų spausdintuvus, kasų stalčius ir mokėjimo įrenginius daugelyje mokėjimo terminalų galima bendrai naudoti prijungiant juos prie bendrai naudojamos aparatūros stoties. | <p>[Aparatūros stotis](retail-peripherals-overview.md) ||
| EKA ir išorinis simuliatorius | Išorinis simuliatorius palaiko scenarijų, kuriems paprastai reikia fizinių EKA išorinių įrenginių, bandymą. Joje taip pat yra EKA simuliatorius, kurį galima naudoti norint patikrinti fizinių periferinių įrenginių suderinamumą ir nereikalauti EKA kliento diegimo. | [Simuliatorius](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Kvitai

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Spausdinti kvitus | Įvairių tipų kvitus, pvz., pardavimo kvitus, kredito kortelės kvitus, dovanų kvitus ir SF, galima išspausdinti pagal numatytuosius nustatymus arba po to, kai išregistravimo metu patvirtinamas kasininko patvirtinimas. Jie taip pat gali būti perspausduoti iš žurnalo. | [Spausdinama](receipt-templates-printing.md) | |
| Kvitai el. paštu | Baigus tikrinti, kvitus galima siųsti el. paštu iš EKA. | [El. pašto adresas](email-receipts.md) | |
| Dizaino gavimų kvitai | Parduotuvės kvitus galima pritaikyti, kad būtų rodomi duomenys ir maketai, tinkami mažmenininkui ir operacijos tipui. Kvitus galima išplėsti ir taip, kad būtų rodomi mažmenininko būtini pasirinktiniai duomenys. | [Dizainas](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Autonominis palaikymas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Sklandus darbas neprisijungus | Vientisas autonominis ryšys leidžia tęsti darbą net tada, kai interneto ryšys ribotas arba negalimas. Duomenų pašalinimas padeda sumažinti autonominės duomenų bazės duomenų dydį ir maksimaliai padidinti našumą. | [Neprisijungęs](pos-operations.md) | |
| Našumui pagrįstas perjungimas | Perjungti į atjungtį, kai aptiktas našumo našumas. | [Neprisijungęs](dev-itpro/implementation-considerations-offline.md) | [Vaizdo](https://youtu.be/sQU-2pgHToI) |
| Skelbimų skelbimų lentos ne tinkle | Būsenos **ne tinkle skelbimų** srityje rodoma kiekvieno įrenginio būsena ne tinkle, klaidos ir išsami informacija apie duomenis. Todėl galite lengvai valdyti daugelio įrenginių būseną. | [Neprisijungęs](dev-itpro/implementation-considerations-offline.md) | [Vaizdo](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Išplečiamumas

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| „Commerce Headquarters“ | "Commerce Headquarters" sprendimus galima pritaikyti pridedant arba modifikuojant verslo procesus. "Commerce Headquarters" palaiko metaduomenų ir kodu pagrįsto plėtinio modelio naudojimą, kad būtų galima įtraukti pasirinktines funkcijas. Jis gali būti lengvai integruotas į išorinius sprendimus. | [Peržiūra](dev-itpro/extend-customer-cdx-package.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Besisktiška prekyba | Extensible Om-channel API sistema gali būti naudojama verslo logikai tinkinti ir pridėti. API, kurie turi užklausų apdorojimo programas, ir išankstinio paleidimo ir paleidimo paleidiklio plėtinių modeliai. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| "Commerce SDK" | "Commerce SDK" yra kodo, kodo pavyzdžiai, šablonai ir įrankiai, reikalingi funkcijoms išplėsti arba Dynamics 365 Commerce tinkinti. SDK publikuojamas skirtingose saugyklose (atstatos) GitHub, atsižvelgiant į plėtinio komponentus. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Elektroninis kasos aparatas | Parduotuvės "Commerce" programą galima išplėsti nepriklausomai naudojant "Commerce SDK" EKA plėtinio funkciją. Sistema palaiko vartotojų patirties (UX), darbo eigų ir verslo logikos pritaikymą. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Technikas](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Ataskaitos

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Pardavimo ataskaitos | Pardavimo ataskaitas pagal darbuotojus, registrą, mokėjimo tipą, grąžinimus, produktus ir t. t. gali naudoti parduotuvių vadybininkai. Vadybininkai gali peržiūrėti šias ataskaitas ir naudoti jas komisiniams paskirstyti bei produktų tendencijoms nustatyti. | | |

## <a name="diagnostics"></a>Diagnostika

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Veikimo žinių apie veiklą | Kliento abonemente galima naudoti parduotuvės paslaugai būdingą patikimumą ir efektyvumo metriką Application Insights . Galimi išplėstiniai įspėjimų ir stebėjimo pajėgumai. | | |
| Sveikatos patikrinimas | Išorinių įrenginių, kurie prijungti prie EKA, pasiekiamumą galima patikrinti vykdant sveikatos tikrinimo operaciją. Tada atskiras išorinius problemas galima išspręsti ir patikrinti. | [Sveikatos patikrinimas](pos-healthcheck.md) | [Vaizdo](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalizacija

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| Kelių rinkų palaikymas | Rinkos priemonės, pavyzdžiui, finansinis integravimas, GST, išplėstinis SF išrašymas ir išankstiniai mokėjimai, palaikomi šiame langelyje. Šios galimybės apima keletą Europos, Amerikos, Rusijos, Azijos, Saudo Arabijos ir t. t. rinkas. | [Globalizacija](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Atitiktis

| Sugebėjimas | Aprašymas | Dokumentacija | Papildomas turinys |
|---|---|---|---|
| "Microsoft" standartai | Parduotuvės Komercijos programa atitinka Microsoft saugos, privatumo, prieinamumo, bendro duomenų apsaugos reglamento (GDPR), Europos Sąjungos (ES) duomenų ribos ir t. t. standartus. | | |

