# Natural Functions

Mistral-7B finetuned for function calling!

[HuggingFace](https://huggingface.co/cfahlgren1/natural-functions)
[Ollama](https://ollama.ai/calebfahlgren/natural-functions)
[HuggingFace GGUF](https://huggingface.co/cfahlgren1/natural-functions-GGUF)

### Try Natural Functions on Ollama!

```bash
ollama run calebfahlgren/natural-functions
```

![Ollama Natural Functions](https://pouch.jumpshare.com/preview/ZZCERaAswnBOtGoesf4APEBB280jYQqfpr2Yo1Ff0_yjNcBG3-LdXr80SS7M_WlksMJBct0M9hMbKIJUQ9BzYt78mKKLZcWqWGpguO5JYcY)

### System Prompt via Ollama

Setting System Prompt with Function Definition
You can set the system prompt with /set system with your function definitions.

```bash
>>> /set system """
... You are a helpful assistant with access to the following functions. Use them if required - 
... {
...     "name": "order_pizza",
...     "description": "Order a pizza with custom toppings",
...     "parameters": {
...         "type": "object",
...         "properties": {
...             "size": {
...                 "type": "string",
...                 "description": "Size of the pizza (small, medium, large)"
...             },
...             "crust": {
...                 "type": "string",
...                 "description": "Type of crust (thin, regular, thick)"
...             },
...             "toppings": {
...                 "type": "array",
...                 "items": {
...                     "type": "string"
...                 },
...                 "description": "List of toppings for the pizza"
...             },
...             "delivery_address": {
...                 "type": "string",
...                 "description": "Address where the pizza should be delivered"
...             }
...         },
...         "required": [
...             "size",
...             "crust",
...             "toppings",
...             "delivery_address"
...         ]
...     }
... }  
... """
```