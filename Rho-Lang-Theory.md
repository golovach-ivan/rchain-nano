# Rho-Lang Theory

```
new HelloWorld in {
  contract HelloWorld(return) = {
    return!("Hello, World!")
  } |
  new myChannel in {
    HelloWorld!(*myChannel)
  }
}
```
