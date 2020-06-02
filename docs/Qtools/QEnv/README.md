## [Home](http://lib-nexus.github.io/site) | [Docs](https://lib-nexus.github.io/site/docs) | [Blog](https://www.youtube.com/watch?v=dQw4w9WgXcQ) | [My Media](https://lib-nexus.github.io/site/my/media) | [My Projects](https://lib-nexus.github.io/site/my/projects) | [Tutorials](https://lib-nexus.github.io/site/my/tutorials)

````python
from Qtools import QEnv as Q

class HelloWorldCommand(EnvironCommand):

    def __init__(self):

        super().__init__('HelloWorld', self.DoCommand)

    def DoCommand(self, ctx):

        Args = ctx.Args(list)
        ArgsRaw = ctx.ArgsRaw(list)
        
        ctx.print('Hello World')

class MyEnvironment(Q.Environment):

    def __init__(self):

        super().__init__()
        self.EnvironCommands.append(HelloWorldCommand)

MyEnvironment.Run()
````

Sample
