# pattern-parser
A very simple pattern parser and input validator in Elixir.

```elixir
input_valid =
  Interpreter.compare?(
    "This <num:int> is a number and this <str:string> is a \string",
    "This: 15 is a number and this 'hello' is string"
  )

IO.puts("\n\nInput is valid: #{elem(input_valid, 0)}")
IO.puts("Input of 'num' is: #{elem(input_valid, 1)["num"]}\n\n")

# <<OUTPUT>>
# Input is valid: true
# Input of 'num' is: 15
```
