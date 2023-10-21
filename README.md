# clojure-quickstart

## tl;dr

1. Install Java 17

```
sudo apt-get install openjdk-17-jdk openjdk-17-source
```

2. Download `lein` script from `http://leiningen.org`

* https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein

Place the `lein` script on PATH, such as: `~/.local/bin`

3. Run the `lein` script, it will download aind install.

```
lein
```

## first tutorials

Create a project: https://leiningen.org/tutorial.html#creating-a-project

Learn about `ring`: https://github.com/ring-clojure/ring/wiki/Getting-Started



## Discussion of JVM and Build Tool choices

Notes to get started with some basic clojure:

References:
* **Practicalli**: https://practical.li/blog/posts/java-17-lts-for-clojure-development/
* **Clojure.org**: https://clojure.org/guides/install_clojure
* **Clojure Guides**: https://clojure-doc.org/
* **Leiningen**: https://leiningen.org/

### choose a JVM

Don't overthink it, just get the latest LTS release compatible with clojure. (hint: `JDK 17`)
* Clojure has documented support LTS versions up to the latest, currently `JDK 17`
* Leiningen has documented support up to `JDK 11`, but has known issues with `JDK 17` and a documented workaround -- so still choose 17.
* Java programmers will invariably want `JDK 17`, there is no valid reason to choose anything older when starting a new project.


### choosing a build tool

Clojure comes with some newer built in library APIs to support implementing your build script with the clojure language, and core Clojure documentation recomments using these.

Leiningen is still the more populare Clojure build tool embraced by much of the community and is considered for now to be the more mature tool for the job.

For my part, being new to the Clojure ecosystem and wanting to find decent tutorials, I'm choosing to start with Leiningen.


### state of the clojure ecosystem

First impression is that it's very messy compared to any of Java, Python, Swift, R, Scala, Kotlin, JavaScript and most other modern languages.

Some documentation suggested using `brew` to install Clojure, it never quite worked correctly and wouldn't let me choose the JVM I wanted.

Some documentation suggested using Leningen, but Leiningen is documented to be compatible with the JVM I wanted.

Still learning here, but I think Leiningen will let me specify the version of clojure to use.

* You might think the problem is that I wanted a specific JVM, but honestly it's the most recent LTS and it's been out for two years, so really doesn't seem like a high bar.

Here's what I'm staring with:
```
lein -v
Leiningen 2.10.0 on Java 17.0.8.1 OpenJDK 64-Bit Server VM

## not sure if i needed clj from brew, or if lein will provide it, but I do have it installed:
which clj
/home/linuxbrew/.linuxbrew/bin/clj

clj --version
Clojure CLI version 1.11.1.1413
```






### PENDING DOCS... maybe not needed....

Ubuntu: 

```
# we use apt -- but for our use case, brew might have been better
sudo apt install openjdk-17-jdk openjdk-17-source


# Alternative if you want -- but not necessary:

# will ask for your sudo password so it can create the default base path
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# include brew in your PATH
echo 'PATH="$PATH:/home/linuxbrew/.linuxbrew/bin"' >> ~/.profile

# note -- i had JAVA_HOME set, and "java" in my path already -- so brew didn't install some other java thankfully
# the latest clojure is 1.11.1 - released april 5, 2022 -- and that's basically what brew installed, so probably in good shape

# clojure
brew install clojure/tools/clojure
```




