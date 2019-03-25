### complete
---
https://github.com/posener/complete

```go
import "github.com/posener/complete"

func main() {
  run := complete.Command{
  　Sub: complete.Commands{
      "build": complete.Command {
        Flags: complete.Flags{
          "-cpus": complete.PredictAnything,
        },
      },
    },
    
    Flags: complete.Flags{
      "-o": complete.PredictFiles("*.out"),
    },
    GlobalFlags: complete.Flags{
      "-h": complete.PredictNothing,
    },
  }
  
  complete.New("run", run).Run()
}
```

```
go get -u github.com/posener/complete/gocomplete
gocomplete -install
```

```
```


