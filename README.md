# lihaoyi-toolkit
A sample toolkit using com-lihaoyi libraries


As of now, this needs to be published locally. You can do it using the command:
```
scala-cli --power publish local --cross LiHaoyiToolkit.scala publish-conf.scala
```

Once this is published locally, we can use the custom toolkit in scala-cli app:
```
//> using toolkit com.yadavan88:0.1.0
```

An working example:
```
//> using toolkit com.yadavan88:0.1.0

@main
def main() = {
  println(fansi.Color.Blue("Hello world!"))
  println("path is : " + os.pwd)
}

```
