
```SWIFT

//p1
let names = ["aaa", "bbb" , "ccc" , "ddd"]

for name in names {
    print (name + " good")
}

/p1
let names = ["aaa", "bob" , "ccc" , "ddd"]

for name in names {
    print (name + " good")
}

let ans1 = names.map({ (a:String) -> (String) in
    return "\(a)" + " good"
})


//p2
var evens = [Int]()

for i in 1...10 {
    if i % 2 == 0 {
        evens.append(i)
    }
}
print(evens)

//p2
var evens = [Int]()

for i in 1…10 {
    if i % 2 == 0 {
        evens.append(i)
    }
}
print(evens)

let ans2 = (1…10).filter({ (v: Int) -> (Bool) in
    if v % 2 == 0 { return true }
    return false
})

print(ans2)

//p3
var evens2 = [Int]()
for i in 1...10 {
    if i % 2 == 0 {
        evens2.append(i)
    }
}
var evenSum = 0
for i in evens2 {
    evenSum += i
}
print(evenSum)

p3.
var even2 = [Int](1...10)
var sum = 0
even2.filter({ (v:Int) -> (Bool) in
    if v % 2 == 0 { sum += v }
    return false
})

print(sum)



//p4
let datas = [ "Mike" : [ "red":3,"blue":5,"green":5],"Sangwoo": [ "red":10,"blue":5,"green":5],"James": [ "red":10,"blue":9,"green":4],"Sarah": [ "red":3,"blue":1,"green":100] ];
var riches:[String] = [];
let NUMBER_RICH = 20;

for student in datas {
    var sumOfBeads = 0;
    for bead in student.1 {
        sumOfBeads += bead.1
    }
    if sumOfBeads > NUMBER_RICH {
        riches.append(student.0)
    }
}
print(riches)




//p5
let p1 = [ 1, 2, 3, 4, 5]
let p2 = [ 6, 7, 8, 9, 10]

var p3: [Int] = []

for i in 0...(p1.count-1){
    p3 += [p1[i] , p2[i]]
}
print(p3)

```
