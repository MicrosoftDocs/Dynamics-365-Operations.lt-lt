---
title: Nuolaidos pagal mokėjimo būdą
description: Šiame straipsnyje aprašomos mokėjimo priemonių mokėjimo priemonės funkcijos, kurios leidžia mažmenininkams konfigūruoti tam tikrų mokėjimo priemonių tipų nuolaidas Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473827"
---
# <a name="tender-based-discount"></a>Mokėjimo priemonės nuolaida

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomos mokėjimo priemonių mokėjimo priemonės funkcijos, kurios leidžia mažmenininkams konfigūruoti tam tikrų mokėjimo priemonių tipų nuolaidas Microsoft Dynamics 365 Commerce.

Pardavėjai dažnai pristato privačias, firmines kredito korteles. Pardavėjams tai yra naudinga, nes jiems bankai pasiūlo pageidaujamus tarifus. Be to, kadangi šios kredito kortelės gali paskatinti klientus dažniau apsilankyti parduotuvėje, jos padeda padidinti bendras pardavėjo pajamas. Todėl pardavėjai yra suinteresuoti skatinti klientus naudoti firmines kredito korteles. Siekdami šio tikslo, jie dažnai teikia papildomas nuolaidas klientams, naudojantiems šias kredito korteles.

Be to, pardavėjai, kurie nesiūlo firminių kredito kortelių, gali skatinti klientus atsiskaityti kitais būdais, pvz., naudojant grynuosius pinigus, dovanų korteles ar lojalumo taškus. Tokiu būdu jie gali sumažinti kredito kortelių aptarnavimo mokesčių išlaidas. Todėl pardavėjai gali teikti nuolaidas klientams, naudojantiems šiuos alternatyvius mokėjimo būdus.

## <a name="tender-based-discount"></a>Mokėjimo priemonės nuolaida

"Commerce" *palaiko* mokėjimo priemones pagrįstas nuolaidas, kurios leidžia mažmenininkams konfigūruoti nuolaidos procentą, kuris taikomas operacijai, jei operacijų suma viršija tam tikrą sumą ir klientas sumoka naudodamas pageidaujamą mokėjimo tipą. Mokėjimo priemonės nuolaida yra pagrįsta pakopa, todėl skirtingi nuolaidos procentai gali būti susieti su skirtingomis sumos ribinėmis vertėmis. Klientas gali nuspręsti atlikti dalinį mokėjimą ar visą mokėjimą, o kainos modulis nustato tinkamą nuolaidos sumą. Mokėjimo priemonės nuolaida visada suteikiama pardavimo eilučių išankstinių mokesčių sumai.

Mokėjimo priemonės nuolaida gali būti taikoma tik pardavimo eilutėms, kurių kainos nėra užrakintos ir proporcingai paskirstytos apibrėžtoms eilutėms. Jei prie užsakymo pridėtos naujos pardavimo eilutės, mokėjimo priemonės nuolaida taikoma tik naujose pardavimo eilutėse mokėjimo metu. Kai pateikiamas kliento užsakymas paimti arba pristatyti, mokėjimo priemonės nuolaida taikoma tik depozito sumai. Pateikus užsakymą, vykdymo metu pardavimo eilučių kainos yra užrakintos. Mokėjimo priemonės nuolaida netaikoma jokiame balanse, sumokamame paėmimo metu arba autorizuotas siuntos metu. Nuolaida pagal mokėjimo būdą gali būti taikoma visai kliento užsakymo sumai tik tuo atveju, jei pardavėjas surenka visą sumą kaip depozitą užsakymo pateikimo metu.

Mokėjimo priemonėse nustatytos nuolaidos nekonkuruoja su preke grindžiamos nuolaidos, pvz., paprastos nuolaidos, kiekio nuolaidos, ribinės nuolaidos, nuolaidos prekių kiekiui ir nuolaidos rankiniu būdu. Mokėjimo priemonės nuolaidos visada sudedamos į prekės nuolaidas. Todėl, net jei prekei taikoma išimtinė nuolaida, mokėjimo priemones galima taikyti ir be nuolaidos. Analogiškai, jei operacijai taikoma ribinė nuolaida, o nuolaida pagal mokėjimo būdą sumažina bendrą sumą iki mažesnės už ribinę vertės, operacijai vis tiek taikoma ribinė nuolaida.

Nors mokėjimo priemonių nuolaidos sumažina operacijos tarpines sumas, automatiniai mokesčiai, taikomi operacijai, nėra paveikiami. Pavyzdžiui, jei pristatymo mokesčiai apskaičiuojami kaip $5 nes tarpinė suma buvo didesnė nei $100, o mokėjimo priemonės nuolaida sumažina sumą taip, kad ji būtų mažesnė nei $100,užsakymo pristatymo $5.

Mokėjimo priemonės nuolaida šiuo metu taikoma tik dviem mokėjimo tipams: kredito kortelėms ir grynieji pinigai. Jei sukonfigūruotos kelios mokėjimo tipo mokėjimo priemonės nuolaidos, taikoma tik geriausia mokėjimo priemonės nuolaida.

## <a name="pos-user-experience"></a>EKA vartotojo patirtis

Jei grynaisiais pinigais taikoma mokėjimo nuolaida yra nustatyta pagal mokėjimo priemones, o kasininkas kasos aparate (EKA) pasirenka mokėjimo grynaisiais pinigais mygtuką, kad ištikrintų grynuosius pinigus **ir** atliktų operaciją, mokėjimo priemonėje taikoma nuolaida automatiškai taikoma operacijai. Tada sumažinta suma rodoma kaip balansas. Tačiau, jei kasininkas pasirenka mokėjimo ekrano mygtuką **Atgal**, nuolaida bus pašalinta, o operacijos ekrane bus rodoma pradinė suma. Jei mokėjimo eilutė tuščia, nuolaida pagal mokėjimo būdą pašalinama.

Kai atliekami mokėjimai kredito kortelėmis, mažmenininkai gali nustatyti mokėjimo priemonių nuolaidą pagal vieną ar daugiau kredito kortelių tipų. Tačiau sistema negali patikrinti naudojamos kredito kortelės tipo, jei kortelė nėra autorizuota. Jei nuolaida taikoma po autorizavimo, mokėjimo autorizavimas bus taikomas didesnei sumai, o mokėjimo fiksavimas bus taikomas mažesnei sumai. Norėdami išvengti tokios situacijos, jei klientas moka kredito kortele, kasininkas paraginamas dialogo lango, kuriame išvardijamos bet kokios pageidaujamos kredito kortelės, kurios klientui suteiks papildomą nuolaidą. Kasininkas gali paklausti, ar klientas nori naudoti vieną iš pageidaujamų kortelių papildomai nuolaidai gauti. Jei kasininkas pasirenka pageidaujamą kortelę, operacijai taikoma mokėjimo priemonė, o sumažinta suma rodoma mokėjimo ekrane. Autorizavimas bus taikomas sumažintai sumai. Jei klientas naudoja kortelę, kuri skiriasi nuo kortelės, kurią pasirinko kasininkas, rodomas klaidos pranešimas ir autorizavimas nebegalioja.

## <a name="call-center-user-experience"></a>Skambučių centro vartotojo patirtis

Jei skambučių centro vartotojas skambučių **centro** užsakymo metu pasirenka Baigti, rodomas **ekranas** Bendrosios sumos. Iš pradžių šio ekrano sumos neapima nuolaidų pagal mokėjimo būdą, nes dar nepasirinktas mokėjimo būdas. Ekrane **Įtraukti mokėjimą**, jei vartotojas pasirenka mokėjimo būdą, kuriam yra sukonfigūruota nuolaida pagal mokėjimo būdą, mokėjimo suma automatiškai koreguojama, kad atitiktų sumą su nuolaidą. Kaip ir EKA klientas skambučių centro klientas gali nuspręsti, ar mokėti visą mokėjimą, ar dalinį mokėjimą. Remiantis sumokėta suma, pardavimo užsakymui taikoma nuolaida pagal mokėjimo būdą.

> [!NOTE]
> Skambučių centro užsakymams kortelių tikrinimas nėra atliekamas. Pavyzdžiui, jei skambučių centro vartotojas pasirenka „Visa“ kredito kortelę, tačiau klientas naudoja „Mastercard“, sistema vis tiek taiko nuolaidą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
