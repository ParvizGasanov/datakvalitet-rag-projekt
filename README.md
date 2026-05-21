# Datakvalitet RAG-projekt

## Gruppmedlemmar
- Parviz
- Abbe
- Meridona

## Projektbeskrivning
Detta projekt är en enkel RAG-applikation byggd i Python med LangChain.

RAG betyder Retrieval Augmented Generation. Det innebär att användaren kan ställa en fråga, systemet hämtar relevant information från vår egen data och använder den informationen som kontext för att skapa ett bättre svar.

## Data
Vi använder en CSV-fil med exempeldata om filmer och serier.

Projektet innehåller:
- original_data.csv
- cleaned_data.csv

## Datakvalitet
Vi har arbetat med datakvalitet genom att:
- undersöka saknade värden
- kontrollera dubbletter
- städa kolumnnamn
- transformera varje rad till text
- spara en rengjord version av datan

## RAG-flöde
Vårt system fungerar så här:

CSV-data → rengöring → text → dokument → chunks → embeddings → vektordatabas → retriever → svar

## Viktigt
.env-filen laddas inte upp till GitHub eftersom den kan innehålla API-nycklar.

## Nuvarande status

## Nuvarande status

Projektet innehåller nu en fungerande RAG-applikation med Gemini.

Systemet fungerar så här:

CSV → dokument → chunks → Gemini embeddings → Chroma vektordatabas → retriever → prompt → Gemini LLM-svar

API-nyckeln ligger lokalt i .env-filen och laddas inte upp till GitHub.