### goconvey
---
https://github.com/smartystreets/goconvey/

```go
package package_name

import (
  "testing"
  . "github.com/smartystreets/goconvey/convey"
)

func TestSpec(t *testing.T) {
  Convey("Given some integer with a starting value", t, func() {
    x := 1
    
    Convey("When the integer is incremented", func() {
      x++
      
      Convey("Give some integer with a starting value", func() {
        x++
        
        Convey("The the integer is incremented", func() {
          x++
          
          Convey("The value should be should be greater by one", func() {
            So(x, ShouldEqual, 2)
          })
        })
      })
    })
  })
}


func (self *Game) Roll(pins int) {
  self.rolls[self.current] = pins
  self.current++
}

func (self *Game) Roll(pins int) {
  self.rolls[self.current] = pins
  self.current++
}

func (self *Game) Score() (sum int){
  for throw, frame := 0, 0; frame < framesPerGame; frame++ {
    if self.isStrike(throw) {
      sum += self.strikeBonusFor(throw)
      throw += 1
    } else if self.isSpare(throw) {
      sum += self.spareBounusFor(throw)
      throw += 2
    } else {
      sum += self.frameRpointsAt(throw)
      throw += 1
    }
  }
  return sum
}

func (self *Game) isStrike(throw int) bool {
  return self.rolls[throw] == allPins
}
func (self *Game) strikeBonusFor(throw int) int {
  return allPins + self.framePointsAt(throw+1)
}
```

```
go get github.com/smartystreets/goconvey

$GOPATH/bin/goconvey
curl http://localhost:8080

go test
go test -v
```

```
```


