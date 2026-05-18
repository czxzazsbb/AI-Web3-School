---
timezone: UTC+8
---

# klizz

**GitHub ID:** klizz111

**Telegram:** 

## Self-introduction

AI x Web3 School

## Notes

<!-- Content_START -->
# 2026-05-18
<!-- DAILY_CHECKIN_2026-05-18_START -->
# Langchain 与 Pydantic 集成

```python
from pydantic import BaseModel, Field
from typing import List
from langchain.output_parsers import PydanticOutputParser
from langchain.prompts import PromptTemplate
from langchain.llms import OpenAI

class Author(BaseModel):
    name: str = Field(description="Name of the author")
    birth_year: int = Field(description="Year the author was born")

class Book(BaseModel):
    title: str = Field(description="Title of the book")
    author: Author = Field(description="Author of the book")
    publication_year: int = Field(description="Year the book was published")

class Library(BaseModel):
    name: str = Field(description="Name of the library")
    books: List[Book] = Field(description="List of books in the library")

parser = PydanticOutputParser(pydantic_object=Library)

prompt = PromptTemplate(
    template="Provide information about a library and its books.\n{format_instructions}\n{query}",
    input_variables=["query"],
    partial_variables={"format_instructions": parser.get_format_instructions()}
)

llm = OpenAI(temperature=0)

_input = prompt.format_prompt(query="Describe a small library with 2 books")
output = llm(_input.to_string())
result = parser.parse(output)

print(result)
```
<!-- DAILY_CHECKIN_2026-05-18_END -->
<!-- Content_END -->
