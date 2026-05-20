# Redovisning - Datakvalitet RAG-projekt

## Gruppmedlemmar
- Parviz
- Meridona
- Abbe

## 1. Introduktion
Vi har byggt ett enkelt RAG-system med Python och LangChain.

RAG betyder Retrieval Augmented Generation. Det innebär att systemet först hämtar relevant information från vår egen data och sedan använder den informationen som kontext för att skapa ett bättre svar.

## 2. Vår data
Vi använder en CSV-fil med exempeldata om filmer och serier.

Vi har två datafiler:
- original_data.csv
- cleaned_data.csv

## 3. Datakvalitet
Vi undersökte datan genom att kontrollera:
- saknade värden
- dubbletter
- kolumnnamn
- datatyper

Vi skapade sedan en städad version av datan.

## 4. RAG-flöde
Vårt system fungerar så här:

CSV-data → rengöring → text → dokument → chunks → embeddings → vektordatabas → retriever → svar

## 5. Demo
Vi kan visa en fråga, till exempel:

"Which titles are about food?"

Systemet hämtar då relevanta dokument från vår data.

## 6. Koppling till kursen
Vi har arbetat med:
- ETL
- transformera data
- datatyper
- datakvalitet
- optimerad läsning av data
- timeliness

## 7. Nuvarande status
Just nu använder projektet en enkel test-embedding eftersom vi saknar riktig API-nyckel.

När vi får en riktig API-nyckel kan vi byta till OpenAIEmbeddings och ChatOpenAI.

## 8. Fördelning under redovisningen

### Parviz
Parviz presenterar projektets syfte, vår data och hur vi arbetade med datakvalitet.

### Meridona
Meridona presenterar preprocessing-delen: hur vi undersökte datan, tog bort problem och skapade cleaned_data.csv.

### Abbe
Abbe presenterar RAG-delen: dokument, chunks, embeddings, vektordatabas och retriever.

## 9. Kort manus

### Parviz säger:
Vi har byggt ett enkelt RAG-system där användaren kan ställa frågor om vår egen CSV-data. Syftet är att visa hur datakvalitet påverkar hela kedjan från originaldata till svar från systemet.

### Meridona säger:
I preprocessing-notebooken började vi med att läsa in originaldatan. Vi kontrollerade saknade värden, dubbletter och kolumnnamn. Sedan skapade vi en städad version av datan som heter cleaned_data.csv.

### Abbe säger:
I RAG-notebooken gjorde vi om varje rad till dokument. Sedan delade vi upp dokumenten i mindre delar, skapade embeddings och sparade dem i en vektordatabas. Med retrievern kan systemet hämta relevant information när användaren ställer en fråga.