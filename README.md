Inlämning 2: Avancerad SQL \& Databashantering

Anna Ljungkvist YH2025




Uppgift:

Syftet med uppgiften var att, med databasen skapad i uppgift 1 som bas, fokusera på att hantera och analysera data, arbeta med constraints, triggers och index samt säkerhetskopiera och återställa databasen.




Metoder:

ER-diagrammet uppdaterades i draw.io och relationsdatabasen uppdaterades i MySQL.


Utförande:

Två av de ursprungliga tre kundernas namn i tabellen Kunder byttes, och ytterligare två kunder lades till i tabellen. 
Tabellen Bocker bytte namn till Produkter och namnet på kolumnen BokID byttes till ISBN i Orderrader samt Produkter.
Fem produkter/böcker lades in i tabellen Produkter.
Därefter följde en förevisning av kommandon som visade:

* Hämtning av kunder och beställningar
* Kunder filtrerade på namn och e-post
* Produkter sorterade efter pris
* Uppdatering av en kunds e-postadress
* Borttagande av en specifik kund samt rollback
* INNER JOIN, LEFT JOIN, GROUP BY samt HAVING
* Skapandet av ett index på e-post i Kunder
* Constraint samt triggers
* Backup samt återställning av databasen
* Testfrågor på den återställda databasen




Reflektion och analys:

Genom att designa en relationell databas kan vi på ett logiskt sätt särskilja de olika delarna av informationen. Detta gör att databasen kan växa - exempelvis med nya tabeller - utan att den befintliga databasen behöver byggas om. Genom användning av Primary Keys samt Foreign Keys säkerställer vi också att de olika tabellerna "hänger ihop" och därmed kan hantera information på ett smidigt sätt samt få fram korrekt efterfrågad information.

Problemet som uppstår när en databas ska hantera större mängder data är en märkbart försämrad prestanda. För att komma till rätta med detta är utökad indexering av de kolumner som används ofta i sökningar en lösning, såsom indexering av kunders namn eller kund-ID. Detta gör det lättare för databasen att hitta den efterfrågade informationen utan att för den skulle behöva söka igenom hela systemet. Jag hade även kunnat korta ner antal tecken på VARCHAR. Att ha max 255 tecken på en e-postadress eller adress till exempel är ett onödigt slöseri av databasens resurser. 

Ett annat alternativ om man enbart ser till snabbhet och prestanda hade varit att använda en annan form av databasstruktur, såsom NoSQL. Dess uppbyggnad med sharding och replikering säkerställer lastbalans och redundans, och dess flexibla struktur gör det snabbare att hantera stora mängder data. Emellertid saknar en NoSQL-databas ofta den säkerhet som ACID-transaktioner i MySQL ger. 

