# lihaoyi-toolkit 
A sample custom [toolkit](https://docs.scala-lang.org/toolkit/introduction.html) using `com-lihaoyi` libraries


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

We can also use the test toolkit. For that, we can publish the test toolkit using:
```
scala-cli --power publish local --cross LiHaoyiToolkitTest.scala publish-conf.scala
```

Now, we can create a test and use it. 
Make sure that the test file is having the extension `.test.scala` or it is placed under `test` directory for the toolkit to consider it as test source. Read more [here](https://scala-cli.virtuslab.org/docs/commands/test/#test-sources).

A sample `CustomTest.test.scala` file:
```
//> using scala 3
//> using test.toolkit com.yadavan88:0.1.0
import utest._
object CustomToolkitTest extends TestSuite {
  val tests = Tests {
    test("simple test") {
      println("executing test... ")
    }
  }
}
```
