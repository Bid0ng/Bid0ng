### Hey Workers 👋

```go
// getMockWorkFunc returns a func that returns nil for the given times running, or returns the given error.
func getMockWorkFunc(num int, err error) func() error {
	cnt := 0
	return func() error {
		cnt++
		if num == cnt {
			return nil
		}
		return err
	}
}
```
