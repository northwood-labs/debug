# Debug

## GetSpew

Spew is a library that can print the contents of a data structure, much like `PrettyPrint` in Python, or `print_r()` or `var_dump()` in PHP. This implementation provides a specific configuration for Spew that is repeatable.

```go
import "github.com/northwood-labs/debug"

func main() {
    var results map[string]interface{}

    // Do some stuff to a variable.
    err := json.Unmarshal(data, &results)
    if err != nil {
        log.Fatalf("there was an error: %w", err)
    }

    // Pretty-print the contents of the variable.
    pp := debug.GetSpew()
    pp.Dump(results)
}
```
