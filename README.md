# iOS-Swift-Logical-Interview-Questions

### 1) Given the following code snippet:
```swift
DispatchQueue.main.async {
    print("statement A")
    DispatchQueue.main.async {
        print("statement B")
    }
    print("statement C")
}
```

### 2) Given the following code snippet:
```swift
DispatchQueue.global().async {
    print("statement 1")
    DispatchQueue.global().async {
        print("print statement 2")
    }
    print("print statement 3")
}
```

### 3) Given the following code snippet:
```swift
DispatchQueue.main.async {
    print("statement X")
}
DispatchQueue.main.async {
    print("statement Y")
}
print("statement Z")
```

### 4) Given the following code snippet:
```swift
DispatchQueue.global(qos: .userInitiated).async {
    print("statement M")
    DispatchQueue.global(qos: .background).async {
        print("statement N")
    }
    print("statement O")
}
```

### 5) Given the following code snippet:
```swift
DispatchQueue.global().async {
    DispatchQueue.main.async {
        print("statement P")
    }
    print("statement Q")
}
print("statement R")
```

### 6) Given the following code snippet:
```swift
DispatchQueue.main.sync {
    print("statement A")
    DispatchQueue.main.sync {
        print("statement B")
    }
    print("statement C")
}
```

### 7) Given the following code snippet:
```swift
DispatchQueue.global().sync {
    print("statement 1")
    DispatchQueue.global().sync {
        print("statement 2")
    }
    print("statement 3")
}
```

### 8) Given the following code snippet:
```swift
print("statement X")
DispatchQueue.global().sync {
    print("statement Y")
}
print("statement Z")
```

### 9) Given the following code snippet:
```swift
DispatchQueue.global().sync {
    print("statement M")
    DispatchQueue.main.sync {
        print("statement N")
    }
    print("statement O")
}
```

### 10) Given the following code snippet:
```swift
print("statement A")
DispatchQueue.main.sync {
    print("statement B")
}
print("statement C")
```

### 11) Given the following code snippet:
```swift
let customQueue = DispatchQueue(label: "custom.queue")
customQueue.async {
    print("statement A")
    DispatchQueue.main.sync {
        print("statement B")
    }
    print("statement C")
}
print("statement D")
```

### 12) Given the following code snippet:
```swift
DispatchQueue.global().async {
    print("statement 1")
    DispatchQueue.global().sync {
        print("statement 2")
    }
    print("statement 3")
}
DispatchQueue.main.async {
    print("statement 4")
}
print("statement 5")
```

### 13) Given the following code snippet:
```swift
let customQueue = DispatchQueue(label: "custom.queue", qos: .userInitiated)
customQueue.async {
    print("statement X")
    DispatchQueue.global().async {
        print("statement Y")
    }
    DispatchQueue.global(qos: .background).sync {
        print("statement Z")
    }
}
print("statement W")
```

### 14) Given the following code snippet:
```swift
DispatchQueue.main.async {
    print("statement A")
    DispatchQueue.global(qos: .userInteractive).async {
        print("statement B")
    }
    DispatchQueue.main.sync {
        print("statement C")
    }
}
print("statement D")
```

### 15) Given the following code snippet:
```swift
let customQueue = DispatchQueue(label: "custom.queue", attributes: .concurrent)
customQueue.async {
    print("statement M")
    customQueue.sync {
        print("statement N")
    }
    print("statement O")
}
DispatchQueue.main.async {
    print("statement P")
}
print("statement Q")
```
