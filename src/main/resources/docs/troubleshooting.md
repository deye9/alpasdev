<div class="sublist">

- **After scaffolding the project, `alpas serve` throws an error.**
> /help/ <span> Try building your app first by running `alpas build` command.</span>
 
- **I get `Error: Got unexpected extra arguments` when running a console command.**
> /help/ <span> Double check the command name and arguments. Make sure that the command is actually
available by running `alpas help` first. </span>

- **`alpas help` doesn't list the commands that I'm looking for.**
> /help/ <span> Most probably because the service provider that actually provides those commands are not registered.
Check `ConsoleKernel.kt` file and make sure the service provider is actually registered. If it is not register
it, and then run `alpas build`. The commands should be available now. </span>

- **`Setting JDK > 9` via Brew.**
> /help/ <span> If you are a Mac user and prefer installing dependencies using [brew](https://brew.sh/), you can follow these steps:            
 <div class="ordered-list"> 

    1. Update your brew and prepare for the needed installations: `brew update`
    2. Install the latest version of Gradle: `brew install gradle`
    3. Install the latest version of Java: `brew cask install java`                
 </div>
 </span>

- **`Setting JDK > 9` via sdkman.**
> /help/ <span> A much better way to install and manage Java dependencies and something that we highly recommend is using [sdkman](https://sdkman.io/install):
 <div class="ordered-list"> 

    1. Install sdkman: `curl -s “https://get.sdkman.io” | bash`
    2. Restart the terminal or just source the sdk: `source "$HOME/.sdkman/bin/sdkman-init.sh"`
    2. Check the version to be sure: `sdk version`
    3. Install the minimum version of Java required: `sdk install java 9.0.7-zulu`
    4. Install the minimum version of gradle required: `sdk install gradle 5.6.4`
                                
 </div>
 </span>

- **`alpas migrate` doesn't run new migrations.**
> /help/ <span> Most probably because you haven't built the app after adding a new migration. Run `alpas build`
to build the app first and then run the migration. </span>

- **Am getting `Unresolved reference: StackWalker` exception.**
> /help/ <span> Most probably because you are yet to update your IntelliJ SDK to use a higher Java version.
> Goto File -> Project Structure to make sure you are using a version of Java greater than 9.0. 
> If you are using a version lesser than that follow the steps listed below:
> Get your Java p /usr/libexec/java_home -v <your_java_version>.
> You should have something like this displayed: /Library/Java/JavaVirtualMachines/openjdk-13.0.1.jdk/Contents/Home
> Now go to Platform Settings -> SDKs and click on the + icon.
> Navigate to the path returned from your java home command and save it. Restart your IDE for the changes to take effect.
></span>
>
- **I'm stuck. I'm having other issues. I need to ask something else. I just want to hangout with cool Alpas devs.**
> /help/ <span>Please [join our Slack channel][alpas-slack] and say hi. </span>
>
- **I found a bug. I've a feature request.**
> /help/ <span> If you found a security related bug, please email us. For other issues and feature/enhancement
requests, please [open an issue][alpas-github-issue] on GitHub. </span>

</div>

[alpas-slack]: https://join.slack.com/t/alpasdev/shared_invite/enQtODcwMjE1MzMxODQ3LTJjZWMzOWE5MzBlYzIzMWQ2MTcxN2M2YjU3MTQ5ZDE4NjBmYjY1YTljOGIwYmJmYWFlYjc4YTcwMDFmZDIzNDE
[alpas-github-issue]: https://github.com/ashokgelal/alpas/issues/new
