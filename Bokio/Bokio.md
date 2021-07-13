# Hej <img src="https://webbdesigner.se/assets/bokio_logo.svg" alt="Bokio" height="24" />!

Jag har, förutom er, provat [Wint](https://www.wint.se/), [Dooer](https://www.dooer.com/), [SpeedLedger](https://www.speedledger.se/) och [FortNox](https://www.fortnox.se/).

Min favorit har blivit **FortNox**, av två enkla anledningar. Först och främst är det kraftfullt, det är ett ordentligt bokföringsprogram, med allt vad det innebär. Dessutom har dom ett API som jag kan använda. Jag älskar att automatisera saker, och tack vare att jag kan både *bokföring* och *programmering* så har jag möjlighet att skapa exakt det jag behöver.

**Men**, det är något som saknas. FortNox passar inte i alla mina bolag. För en del bolag behövs det något enklare. Något som även dom som inte är redovisningskonsult eller utvecklare kan använda sig av. Och det är därför det finns en marknad för någon som er.

Av de *"enkla"* alternativen, så tycker jag absolut bäst om Bokio. Det är tydligt, enkelt, billigt. Man har möjlighet att bokföra exakt som man vill, om man kan, men ni har genom smarta funktioner gjort att det är extremt smidigt och lätt, även för någon som inte är så insatt.

Det finns några saker som jag gärna skulle se, och som skulle göra det helt solklart enkelt att använda er istället för någon annan.

## 1. API

Ni måste öppna upp ett API. Det måste inte vara världens mest kompletta API till en början, men om vi bara kan få till enkla saker som t.ex. att visa eller skapa kunder och fakturor.

## 2. Webhooks

Jag skulle också gärna se att ni erbjöd webhooks. Varför inte hooks för precis allt som kan hända. Inspireras gärna av Stripe, som har [sanslöst bra hooks](https://stripe.com/docs/webhooks)! Ni må pricka av fakturan när den är betald, men jag kanske även skulle vilja ha möjlighet att t.ex. skicka en vara till kunden, där jag väntat på betalning, eller något så enkelt som att få en bot på Slack att säga till mig att fakturan är betald.

Eller varför inte bygga en app hos [Zapier](https://zapier.com/platform)? Det är en no-code-plattform där man lätt kan koppla ihop saker, t.ex. om en faktura blir betald så uppdateras ett spreadsheet och man får ett sms.

## 3. Avtalsfakturor

Nästan alla mina kunder är på avtal. Vi har återkommande fakturor. Helst skulle man ju vilja ha extremt avancerade faktura-möjligheter, med både grundavgift och en varierande del (t.ex. beroende på antal timmar dom köpt, eller antal dagar dom nyttjat en tjänst). Dom mest avancerade lösningarna kan man ju lösa själv om det finns ett API, men något som ni iallafall redan nu skulle kunna erbjuda, vore **återkommande fakturor**. Jag sätter ett belopp, och en frekvens (5500 kronor i månaden) samt väljer när den skall skickas.

- Varje vecka/månad/kvartal/halvår/år
- Den X:e
- X gånger / tills vidare

<img src="https://mossberg.xyz/wp-content/uploads/2021/06/Screenshot-2021-06-10-at-23.10.59.png" width="582">

Detta är guld värt om man t.ex.:

- Hyr ut kontorsplats
- Tar betalt för medlemskap i en förening
- Har ett löpande support-avtal som konsult

### Steget längre

I en drömvärld så skulle man ju vilja kombinera detta med möjligheten att (via API eller er sajt) lägga till rörliga delar. T.ex. kanske man har kunder som betalar en fast avgift på X kronor i månaden ör att ha möjlighet att ringa en, men att man dessutom tar Y kronor i timmen dom gånger som kunden faktiskt utnyttjar detta.

I så fall tänker jag mig att detta skulle kunna vara en sektion som heter "Avtal" eller "Prenumerationer".

<img src="https://mossberg.xyz/wp-content/uploads/2021/06/Screenshot-2021-06-10-at-23.20.17.png" width="335">

Då skulle man dessutom kunna säga till, om man försöker skapa en ny faktura till en kund, som redan har ett avtal:

<img src="https://mossberg.xyz/wp-content/uploads/2021/06/Screenshot-2021-06-10-at-23.25.18.png" width="482">

Och om man verkligen får önska något, så vore det att kunna få välja hur grund-priset på fakturan skall fungera:

<table>
  <tr>
    <td></td>
    <th>Vad</th>

  </tr>
  <tr>
    <th>Fast&nbsp;avgift</th>
    <td>Denna avgift kommer alltid att vara på fakturan, eventuella rörliga delar blir tillägg.</td>

  </tr>
  <tr>
    <th>Minsta&nbsp;belopp</th>
    <td>Om den rörliga delen av fakturan inte kommer upp i detta belopp, så läggs mellanskillnaden på. Som "kvar till minsta beställning" på Uber Eats.</td>


  </tr>
  </table>

## 4. Epost-scanning

I de bolag där jag använder FortNox, så använder jag **Pleo** för att hantera alla småkvitton som kommer via mail. Jag har anslutit min mailbox till Pleo genom

[Gmail's API](https://developers.google.com/gmail/api/reference/rest/v1/users.messages/list) är en bra start. Ni vet ju själva vilka mailtjänster som är populärast hos era användare, och om man använder sig av ert betalkort, så har ni ju redan koll på transaktionen.

Eftersom ni redan idag har full koll på vilka leverantörer era kunder spendera sina pengar hos genom [railsbank](https://www.railsbank.com/), så skulle ni kunna fokusera på att automatisera kvitto-hämtning för de leverantörer som används mest, och ta bort en av de jobbigaste delarna med att driva bolag.

Inspireras av [Pleo Fetch](https://pleo.io/se/fetch)!

## 5. Kivra-integration

FortNox har en integration mot kivra, så att inkommande post hamnar rätt direkt. Detta vore ju grymt att ha hos er med!

## 6. Autogiro

Jag har förstått att man bara får ett bankgiro-nummer, och inte ett riktigt konto, när man använder er konto-tjänst. Men det vore guld för oss att kunna erbjuda våra kunder att betala till oss med autogiro.

## 7. En app store?

Ge oss möjlighet att utveckla applikationer till Bokio. Detta har gjorts med framgång på [FortNox](https://www.fortnox.se/kopplingar/).

# Men helst av allt..

### Bjud in oss till ert repo! 🙏

Jag menar **inte** att ni skall släppa källkoden till er produkt fri, men vad sägs om att hitta ett sätt där vi som är nördar, har möjlighet att hjälpa er med vissa saker så att ni kan fokusera på att leverera en bättre produkt.

Jag föreslår att ni öppnar följande delar av ert git-repo:

1. [Hjälp-sidan](https://www.bokio.se/hjalp/)
2. [Ert frontend](https://www.bokio.se/)

Det kanske låter helt galet. Men hear me out.

Cunninghams lag säger:

> the best way to get the right answer on the internet is not to ask a question; it's to post the wrong answer

Ju mer ni växer, och ju mer kompetent ert verktyg blir, desto lättare kommer det vara att någon bit av dokumentationen inte hänger med. Ni kanske skriver om en lag som ändras, det finns ett svar som blir inaktuellt på grund av att en funktion i ert system byts ut.

Genom att öppna upp dokumentationen till oss som använder tjänsten, så kommer ni att få hjälp att rätta alt från stavfel till att förbättra copy, eller till och med lägga till nya hjälp sektioner som ni inte redan själva tänkt på.

Genom att öppna upp ert frontend så skulle ni kunna få hjälp att fixa småsaker. Jag är utvecklare, och om en tjänst jag gillar har en bugg som irriterar mig, så skulle jag gärna fixa den om jag kunde. Det skulle ju fortfarande vara ni som godkänner pull requests etc., men om jag hade en möjlighet att använda min kompetens för att förbättra de tjänster jag verkligen gillar, så skulle jag gärna göra det.

<details>
  <summary>:beetle: Knappen klipps vid vissa skärmstorlekar, sedan ni började bjuda in redovisningsbyråer</summary>

|                       ![Bug](https://webbdesigner.se/assets/bug.png)                        |
| :-----------------------------------------------------------------------------------------: |
| *Knappen klipps vid vissa skärmstorlekar,<br>sedan ni började bjuda in redovisningsbyråer.* |

</details>

Även om ni inte skulle öppna upp källkoden till oss, så skulle ni ju kunna öppna upp [Discussions](https://docs.github.com/en/discussions), det skulle vara ett lätt sätt för er att låta folk rösta på funktioner, rapportera buggar eller fel etc.

Ni idag en grym [facebook-grupp](https://www.facebook.com/groups/240735629672293/) där medlemmarna kan hjälpa varandra. Detta är grymt bra och förflyttar er från att bara vara ett varumärke eller en produkt, till att bli en rörelse. Något man kan känna sig delaktig i. Era kunder är era bästa ambassadörer, och jag tror att ni har allt att vinna på att öppna upp dörren lite mer, för dom som vill.

Genom att ha ordentliga och tydliga mallar för bugg-rapportering etc., gör ni det enkelt för oss att hjälpa er, och det blir tydligt att ni faktiskt lyssnar på era kunder, dessutom blir det ett sätt för oss användare att kunna visa er vilka förslag som vi vill att ni prioriterar.

Tack för en bra tjänst!<br>
/Fabian
