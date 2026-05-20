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