# Wprowadzenie

Polski przekład oficjalnej internetowej książki do nauki [języka programowania Rust][Rust Book].

Przetłumaczenie tej kolubryny, w rozsądnym czasie, było możliwe dzięki autorskiemu oprogramowaniu [TranAI] napisanemu w języku Rust. To samo oprogramowanie może zostać użyte do tłumaczenie jakiejkolwiek książki napisanej za pomocą [mdBook]. Oprogramowanie [mdBook] jest wykorzystywane szeroko do tworzenia przewodników i dokumentacji w świecie Rusta, ale może być wykorzystane do napisania jakiejkolwiek innej książki.


# Techniczne aspekty
Oprogramowanie [TranAI] jest [preprocesorem][preproc] [mdBook]’a.
Sam [preprocesor][preproc] do tłumaczenie użył modelu [LLM] [Gemini 2.5 Pro] w styczniu 2026 roku.

To repozytorium jest zbiorem narzędzi potrzebnych do budowy [Książki Rusta][Rust Book].

`tranai_cache.json` jest plikiem wykorzystywanym przez [TranAI] ponieważ [Gemini 2.5 Pro], jak na krnąbrny model przystało, przerywa generowanie tokenów w pół żądania https. [TranAI] zrzuca dane, które już udało się uzyskać, aby nie trzeba było ich tłumaczyć ponownie.

Dla większego kontekstu i lepszego tłumaczenia następuje próba przesłania całego tekstu oprócz tego, który został wcześniej zcache’owany.

Szczegółowe dane techniczne jak działa [TranAI] można znaleźć na stronie projektu.



[TranAI]: <https://github.com/CodeServant/mdbook-tranai>
[mdBook]: <https://rust-lang.github.io/mdBook/>
[Gemini 2.5 Pro]: <https://ai.google.dev/gemini-api/docs/models?hl=pl#gemini-2.5-pro>
[preproc]: <https://rust-lang.github.io/mdBook/format/configuration/preprocessors.html>
[LLM]: <https://pl.wikipedia.org/wiki/Du%C5%BCy_model_j%C4%99zykowy>
[Rust Book]: <https://doc.rust-lang.org/book/>