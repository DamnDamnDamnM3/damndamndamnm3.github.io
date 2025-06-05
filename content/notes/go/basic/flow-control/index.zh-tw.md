---
title: 流程控制
weight: 30
menu:
  notes:
    name: 流程控制
    identifier: notes-go-basics-flow-control
    parent: notes-go-basics
    weight: 30
---

<!-- Condition -->
{{< note title="條件">}}

```go
if day == "sunday" || day == "saturday" {
  rest()
} else if day == "monday" && isTired() {
  groan()
} else {
  work()
}
```

```go
if _, err := doThing(); err != nil {
  fmt.Println("Uh oh")
```

{{< /note >}}

<!-- Switch -->

{{< note title="Switch 語句" >}}

```go
switch day {
  case "sunday":
    // cases don't "fall through" by default!
    fallthrough

  case "saturday":
    rest()

  default:
    work()
}
```

{{< /note >}}

<!-- Loop -->

{{< note title="迴圈" >}}

```go
for count := 0; count <= 10; count++ {
  fmt.Println("My counter is at", count)
}
```

```go
entry := []string{"Jack","John","Jones"}
for i, val := range entry {
  fmt.Printf("At position %d, the character %s is present\n", i, val)
```

```go
n := 0
x := 42
for n != x {
  n := guess()
}
```

{{< /note >}}