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
