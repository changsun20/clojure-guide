# Editors for Clojure development

The best editor to use for learning Clojure is the editor already familiar with (or want to learn).

Use SublimeText & ClojureSublimed if unsure where to start as it will be the simplest tool to use.

## Clojure editor features

An ideal Clojure editor includes the these core features

* running / connecting to a REPL process
* evaluation results inline or in a repl window (fast feedback on what the code does)
* syntax highlighting (including highlight of matching parens)
* structural editing to ensure parens are balanced when writing and refactor code
* data inspector to visualise large and nested data, or connection to [:fontawesome-solid-book-open: data inpector tools](/clojure/data-inspector/)

![Clojure REPL driven development with Clojure aware editors](https://raw.githubusercontent.com/practicalli/graphic-design/live/clojure/clojure-repl-driven-development-clojure-aware-editor.png)

## Clojure aware editors

Emacs (Spacemacs, Doom, Prelude), Neovim (Conjure) and VSCode (Calva) are the most common open source Editors for Clojure and ClojureScript development.

SublimeText and IntelliJ are commercial editors (with limited free editions) which also provide Clojure support

=== "Emacs"
    ![GNU Emacs logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/logos/emacs-icon.svg){align=right loading=lazy style="height:128px;width:128px"}

    Emacs is a very powerful editor with thousands of packages enabling a person to do almost any digital task concievable.  Emacs is highly extensible via the ELisp programming language used to write configuration and the numerous Emacs packages. Native Compilation of Emacs packages dramatically speeds up many common tasks.

    Emacs uses CIDER and Clojure LSP for a feature rich clojure development experience.

    Use one of the popular community configurations for Emacs or visit the [:fontawesome-solid-globe: CIDER documentation](https://docs.cider.mx/) to learn how to add Clojure support to Emacs.

    === "Spacemacs"
        ![Spacemacs logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/logos/spacemacs-logo.svg){align=right loading=lazy style="height:128px;width:128px"}

        [:fontawesome-solid-globe: Spacemacs](https://spacemacs.org/){target=_blank} is a community configuration bringing [:fontawesome-solid-globe: Emacs](https://www.gnu.org/software/emacs/){target=_blank} features and [:fontawesome-solid-book-open: Vim style editing](https://practical.li/spacemacs/spacemacs-basics/evil/){target=_blank} together.  Spacemacs uses a mnemonic menu system that makes it easy to learn and provides detailed documentation for configuring and using Emacs.

        [:fontawesome-solid-book-open: Practicalli Spacemacs](https://practical.li/spacemacs){target=_blank} provides a guide to Clojure development, vim-style editing, documenting with org-mode, Git version control with Magit, Issues & Pull Requests with Forge and dozens of other features.

        [:fontawesome-brands-github: Practicalli Spacemacs Config](https://github.com/practicalli/spacemacs-config){target=_blank} contains a customised configuration for Clojure development and supporting tools.

        === "Free Desktop XDG Config"
            ```shell
            git clone https://github.com/practicalli/spacemacs.d.git $XDG_CONFIG_HOME/spacemacs`
            ```

        === "Classic Config"
            ```shell
            git clone https://github.com/practicalli/spacemacs.d.git $HOME/.spacemacs.d`
            ```

        The Practicalli configuration should replace the `~/.spacemacs` file if it exists

        [Spacemacs install guide - Practicalli Spacemacs](https://practicalli.github.io/spacemacs/install-spacemacs/){target=_blank .md-button}

        <p style="text-align:center">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/NDrpclY54E0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </p>

    === "Prelude Emacs"
         [:fontawesome-solid-globe: Emacs Prelude](https://prelude.emacsredux.com/en/stable/) is an easy to use Emacs configuration for Emacs newcomers and lots of additional power for Emacs power users, from the author of [CIDER - the definitive Clojure IDE for Emacs](https://docs.cider.mx/).

         Prelude uses the traditional chorded key bindings to drive Emacs, e.g. ++ctrl+"c"++ ++ctrl+"c"++ to evaluate the current top-level form.

         [:fontawesome-solid-globe: Prelude Install Guide](https://prelude.emacsredux.com/en/stable/installation/){target=_blank .md-button}


    === "Doom Emacs"
        ![Doom Emacs logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/logos/doom-emacs-logo.png){align=right loading=lazy style="height:128px"}

        [:fontawesome-brands-github: Doom Emacs](https://github.com/doomemacs/doomemacs){target=_blank} is a community configuration for [Emacs](https://www.gnu.org/software/emacs/){target=_blank} that provides a minimalistic configuration that is readily customisable.  Doom Emacs is most suited to those coming from Vim and have a strong experience for multi-modal editing.

        [:fontawesome-solid-book-open: Practicalli Doom Emacs Book](https://practical.li/doom-emacs/){target=_blank .md-button}

        [:fontawesome-brands-github: Practicalli Doom Emacs Config](https://github.com/practicalli/doom-emacs-config){target=_blank} contains a customised configuration for Clojure development and supporting tools.

        === "Free Desktop XDG Config"
            ```shell
            git clone https://github.com/practicalli/doom-emacs-config.git $XDG_CONFIG_HOME/doom`
            ```
            The Practicalli configuration should replace the `~/.config/doom/` directory created by the `doom install` command.

        === "Classic Config"
            ```shell
            git clone https://github.com/practicalli/doom-emacs-config.git $HOME/.doom.d`
            ```
            The Practicalli configuration should replace the `~/.doom.d/` directory created by the `doom install` command.


        ![Emacs Doom with Practicalli customisations](https://raw.githubusercontent.com/practicalli/graphic-design/live/doom-emacs/doom-emacs-practicalli-dark.png#only-dark)
        ![Emacs Doom with Practicalli customisations](https://raw.githubusercontent.com/practicalli/graphic-design/live/doom-emacs/doom-emacs-practicalli-light.png#only-light)


    === "Vanilla Emacs & Cider"
        Emacs 29 is recommended as it includes native compilation support and optomised JSON support which is valuable for Language Server Protocol servers.

        Emacs is available for Linux, MacOSX and Windows.

        === "Ubuntu / Debian"
            `apt-cache show emacs` to check available versions of Emacs in the Ubuntu package manager. If version 28 is available, install Emacs using the Ubuntu package manager.

            ```shell
            sudo apt install emacs
            ```

            Additional versions of Emacs are available via the [Ubuntu Emacs Team Personal Package Archive](https://launchpad.net/~ubuntu-elisp/+archive/ubuntu/ppa).

            `sudo apt install emacs-snapshot` package to use the latest nightly build of Emacs, although be aware that some things may break.


            ??? HINT "Build Emacs from source"
                [Building Emacs from source code](https://practical.li/blog/build-emacs-from-source-on-debian-linux/) has a few steps to ensure dependencies are present.

                Building Emacs allows customisation of features included in Emacs, e.g. JSON support, XWidgets or native compilatin of elisp to enhance the performance of Emacs.

                Emacs will take 15-30 minutes to compile, then the binary created can be installed.



        === "Homebrew / MacOSX"
            [Emacs Plus](https://github.com/d12frosted/homebrew-emacs-plus) from Homebrew provides many options, including native compilation and Spacemacs Icon for application launchers.

            ```
            brew tap d12frosted/emacs-plus`
            brew install emacs-plus@28 --with-native-comp --with-spacemacs-icon
            ```

            Emacs.app is installed to: `/usr/local/opt/emacs-plus@28`

            Optionally run Emacs plus as a service
            ```
            brew services start d12frosted/emacs-plus/emacs-plus@28
            ```

            Run `emacs`

            Get a hot cup of something as Emacs native compilation compiles all the things.


            > The [Spacemacs README lists other options for MacOSX](https://github.com/syl20bnr/spacemacs#macos).


        === "Windows"
            Download Emacs-28.2 from the [GNU repository](http://ftp.gnu.org/gnu/emacs/windows/emacs-26) and extract the zip file to `%AppData%/local/Programs/emacs`.

            Alternatively, if you are using the [Chocolatey package manager](https://chocolatey.org/){target=_blank} then install [Emacs version 28](https://chocolatey.org/packages/emacs){target=_blank}

            Add the Emacs directory to the `PATH` variable in your user account environment variables.

            To start Emacs run the command `runemacs.exe`.  You can also pin this to the start menu or task bar.

            ??? HINT "Access to common Unix tools"
                Command line tools, such as `diff`, are used by Emacs.  To have these command line tools available in Windows, install Emacs as above but then run emacs from a Unix shell such as [GitBash](https://git-scm.com/){target=_blank}.


        === "Msys2"
            Install Emacs (64bits build) with the following:

            ```
            pacman -S mingw-w64-x86_64-emacs
            ```

        Once Emacs is installed, add the cider package for essential Clojure support.

        [Cider Install Guide](https://docs.cider.mx/cider/basics/installation.html){target=_blank .md-button}

=== "Neovim"
    ![Neovim logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/logos/neovim-logo-small.svg){align=right loading=lazy style="height:128px;width:128px"}

    Neovim is a hyper-extensible text editor that runs in a terminal, configured with the [Lua programming language](http://www.lua.org/). Configuration can also be written in [Fennel](/neovim/introduction/fennel/) (a lisp dialect), using [nfnl](https://github.com/Olical/nfnl) to generate Lua code.

    Neovim is based on multi-model editing (e.g. normal, insert, visual editing states) providing a highly effective tool for writing code, configuration and documentation.

    Neovim includes Treesitter which understands the syntax of a great many programming and configuration languages, which can be coupled with analysist from Language Sever Protocol (LSP) servers to provide live feedback on code quality.

    ![Conjure logo](https://github.com/practicalli/graphic-design/blob/live/logos/conjure-logo-wizard.png?raw=true){align=right loading=lazy style="height:128px;width:128px"}

    [Conjure](https://github.com/Olical/conjure) provides Clojure interactive (REPL) development, supporting Clojure CLI, Leiningen and Babashka projects (as well as several other Lisp dialects and interesting languages)

    Try the Conjure interactive `:ConjureSchool` tutorial which only requires a recent version of neovim
    ```shell
    curl -fL conjure.fun/school | sh
    ```
    ![Clojure editors - neovim and conjure tutorial](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/neovim/screenshots/neovim-conjure-conjure-fun-school-light.png#only-light)
    ![Clojure editors - neovim and conjure tutorial](https://raw.githubusercontent.com/practicalli/graphic-design/live/editors/neovim/screenshots/neovim-conjure-conjure-fun-school-dark.png#only-dark)

    `:q` to quit the tutorial.


    === "Practicalli Astro"

        [:fontawesome-solid-book-open: Practicalli Neovim - Astro install](https://practical.li/neovim/install/neovim/){target=_blank .md-button}

        AstroNvim community configuration for Neovim provides an engaging UI, using Lazy plugin manger and Mason to manage LSP servers, format & lint tools.

        [:fontawesome-brands-github: Practicalli Astro](https://github.com/practicalli/astronvim-config) provides a user configuration for Astronvim, including Conjure, parinfer, LSP server and treesitter parser for Clojure development.

        [:fontawesome-solid-book-open: Practicalli Neovim](https://practical.li/neovim/) provides an install and user guide for Neovim and Conjure for Clojure development, folloiwng a REPL driven workflow.

        ![Practicalli Neovim in action](https://github.com/practicalli/graphic-design/blob/live/editors/neovim/astronvim/astronvim-clojure-development-example-light.png?raw=true#only-light)
        ![Practicalli Neovim in action](https://github.com/practicalli/graphic-design/blob/live/editors/neovim/astronvim/astronvim-clojure-development-example-dark.png?raw=true#only-dark)


    === "SpaceVim"
        [SpaceVim](https://spacevim.org/) is a fully featured vim experience that includes [a minimal Clojure development environment](https://spacevim.org/layers/lang/clojure/) based around [vim-fireplace](https://github.com/tpope/vim-fireplace)

        Follow the [Quick Start Guide to install SpaceVim](https://spacevim.org/quick-start-guide/)

        Add the Clojure layer to the SpaceVim custom configuration file
        ```shell title="~/.SpaceVim.d/init.toml"
        [[layers]]
          name = "lang#clojure"
        ```

        [SpaceVim quickstart guide](https://spacevim.org/quick-start-guide/){target=_blank .md-button}
        [SpaceVim - Clojure Layer](https://spacevim.org/layers/lang/clojure/){target=_blank .md-button}


    === "VimIced"
        ![vim-iced logo](https://raw.githubusercontent.com/liquidz/vim-iced/master/doc/pages/assets/logo.svg){align=right loading=lazy style="height:128px;width:128px"}

        Interactive Clojure Environment for Vim8/Neovim, aimed at the more experienced Vim/Neovim user.

        vim-iced uses vim-sexp for structural editing

        vim-plug is required to install the vim-iced packages.

        [vim-iced documentation](https://liquidz.github.io/vim-iced/){target=_blank .md-button}

=== "VSCode"
    ![VS Code logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/icons/vs-code.svg){align=right loading=lazy style="height:128px;width:128px"}

    [VS Code](https://code.visualstudio.com/) is a freely available editor build on open source and available for Linux, MacOS and Microsoft Windows.

    [VSCode Getting Started Guide](https://code.visualstudio.com/docs/introvideos/basics){target=_blank .md-button}

    [VS Code has a large marketplace of extensions](https://marketplace.visualstudio.com/VSCode), proiding additional tools for a complete development environment.

    **Calva** is the most commonly used extension for Clojure support and aims to provide similar features to Emacs Cider (and uses some of the same Clojure libraries).

    !!! WARNING "Clojure CLI User Aliases not directly supported"
        Calva does not support Clojure CLI user aliases directly (only project deps.edn).  A JSON mapping must be added to the Calva configuration for each user alias (duplicating configuration)

        Practicalli recommends starting the Clojure REPL in a terminal and specifying the required Clojure CLI user aliases, using Calva connect once the REPL has started.


    **VSpaceCode** provides a mnemonic menu to drive VS Code by keyboard alone, vim editing and rich Git client (edamagit).  VSpaceCode extension also provides key bindings for common Calva commands.  Users experienced with Neovim and Emacs (Spacemacs / Doom) will find this extension makes VS Code easiter to use than vanilla VS Code or VS Code with an Neovim backend.

    **Clover** provides a mininal, highly customisable environment using Socket REPL.


    === "Calva"
        ![Calva logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/logos/calva-name-logo.svg){align=right loading=lazy style="height:128px;width:128px"}

        The Calva extension adds Clojure REPL support to VS Code editor, including Clojure LSP, formatting, structural editing and many other features.

        Calva is under active development and the [#calva channel on the Clojurians Slack community](clojurians.slack.com/messages/calva) can be supportive.

        [Calva Getting Started Guide](https://calva.io/getting-started/){target=_blank .md-button}
        [Calva - VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=betterthantomorrow.calva){target=_blank .md-button}

        <p style="text-align:center">
          <iframe width="560" height="315" src="https://www.youtube.com/embed/a2vRDYXDAug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </p>


    === "VSpaceCode"
        ![VSpaceCode logo](https://vspacecode.github.io/img/logo.png){align=right loading=lazy style="height:128px;width:128px"}

        [VSpaceCode](https://github.com/VSpaceCode/VSpaceCode) is a Spacemacs-like community configuration for Microsoft VS Code. Drive VS Code entirely from the keyboard, using easy to remember mnemonic keys for all commands and full vim-stile editing tools.

        Calva extension must be added as it is not part of VSpaceCode, although Calva commands are included in the VSpaceCode mneomoic menu when a Clojure file is open.

        Edamagit is a sophisticated text based Git client (like magit for Emacs) is also included in the VSpacemacs extension.

        [Practicalli VSpaceCode install guide](https://practical.li/vspacecode/install/){target=_blank .md-button}
        [Practicalli VSpaceCode user guide](vspacecode-guide/){target=_blank .md-button}

        ![VSpaceCode in action](https://raw.githubusercontent.com/VSpaceCode/vspacecode.github.io/master/static/img/demo.gif)

        <p style="text-align:center">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/1VNNtaUfHs4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </p>


    === "Clover"
        [Clover](https://marketplace.visualstudio.com/items?itemName=mauricioszabo.clover){target=_blank} is a Socket REPL based development tool for Clojure with some ClojureScript support (not including Figwheel).

        [Clojure GitLab repository](https://gitlab.com/clj-editors/clover) includes usage details.

=== "SublimeText"
    ![Clojure Sublimed Text logo](https://raw.githubusercontent.com/practicalli/graphic-design/live/logos/clojure-sublimed-logo.png){align=right loading=lazy style="height:128px;width:128px"}

    [SublimeText 4](https://www.sublimetext.com/) is a lightweight and feature rich text editor, especially of interest to those that like a simple and uncluttered UI.  SublimeText is a commercial project although has free trial version available (check [conditions of use](https://www.sublimehq.com/store/text)).

    [Clojure-Sublimed](https://github.com/tonsky/Clojure-Sublimed) provides Clojure support for SublimeText 4, with support for Clojure & Edn syntax, code formatting and an nREPL client to connect to a Clojure REPL process.

    > [Tutkain](https://tutkain.flowthing.me/) is an Sublime 4 package that supports Clojure development (self-described as alpha software).

    !!! HINT "Build configuration to start a REPL"
        Clojure Sublime connects to a REPL via an nREPL server.  Run a [terminal REPL using Clojure CLI](/clojure/clojure-cli/repl/), Leinginen (`lein repl`) or Shadow-cljs (`shadow-cljs watch app`)

        Alternatively, configure Clojure Sublimed to run a REPL process by creating a new build system via **Tools** » **Build System** » **New Build System**. The following example starts a Clojure CLI REPL with nREPL server and assumes [Java and Clojure CLI are installed](/clojure/install/).
        ```shell
        {"env": {"JAVA_HOME": "/path/to/java"},
         "cmd": ["/usr/local/bin/clojure", "-Sdeps", "{:deps {nrepl/nrepl {:mvn/version \"1.0.0\"}}}", "-M", "-m", "nrepl.cmdline"]}
        ```
        Run a REPL process via **Tools** » **Build With…** and connect to the REPL using the command **Clojure Sublimed: Connect**

    [SublimeText install](https://www.sublimetext.com/download){target=_blank .md-button}
    [Clojure-Sublimed install](https://github.com/tonsky/Clojure-Sublimed#installation){target=_blank .md-button}
    [SublimeText Documentation](https://www.sublimetext.com/docs/index.html){target=_blank .md-button}

=== "Pulsar (Atom)"
    ![Chlorine for Pulsar Editor](https://gitlab.com/clj-editors/atom-chlorine/raw/HEAD/docs/chlorine-logo.png){align=right loading=lazy style="height:128px;width:128px"}

    [Pulsar Community-led Hyper-Hackable Editor](https://pulsar-edit.dev/) is a very new project to create a community version of the Atom editor from GitHub.

    [Chlorine plugin](https://web.pulsar-edit.dev/packages/chlorine) provides a Clojure and ClojureScript development environment using Socket-REPL integration

    [Pulsar Community-led Hyper-Hackable Editor](https://pulsar-edit.dev/){target=_blank .md-button}
    [Pulsar Chlorine plugin](https://web.pulsar-edit.dev/packages/chlorine){target=_blank .md-button}

    !!! WARNING "Atom not actively developed"
        Atom will be archived on December 15 2022 with no further updates from GitHub team

        Consider using VSCode with Clover or Calva plugin or help support the evolution of the Pulsar project

=== "Intellij"

    [:globe_with_meridians: IntelliJ IDEA](https://www.jetbrains.com/idea/) is a commercial product that provides an editor for Java and Kotlin.  An IntelliJ IDEA Community Edition is a version of the product that is distributed under the Apache 2.0 licence and can be used for commercial and non-commercial work.

    IntelliJ may be an appropriate choice when working with Java and Clojure projects or where there is already familiar with IntelliJ.

    Clojure support is avaialbe via plugins, either open source or commercial closed source (requiring license key).

    === "Open Source plugins"
        [:fontawesome-brands-github: Clojure-REPL-Intellij](https://github.com/afucher/clojure-repl-intellij) plugin provides a Clojure REPL client which can start an nREPL server from IntelliJ or connect to an existing nREPL process.  The REPL client can evaluate code, run tests, reload / refresh namespaces, interupt evaluation and navigate the history of commands sent to the REPL.

        ![IntelliJ IDEA Open Source REPL plugin](https://github.com/afucher/clojure-repl-intellij/raw/master/images/demo.png){loading=lazy}

        [:fontawesome-brands-github: Clojure-LSP-Intellij](https://github.com/clojure-lsp/clojure-lsp-intellij) plugin provides an Language Server Protocol (LSP) server implementation for Clojure and ClojureScript, providing static analysis of a code base to show diagnostics and provide code completion data.  The LSP server also enables tools to refactor Clojure and ClojureScript code.

        ![IntelliJ IDEA Open Source LSP Server plugin](https://github.com/clojure-lsp/clojure-lsp-intellij/raw/master/images/demo.png){loading=lazy}


    === "Commercial Closed Source plugin"

        [:globe_with_meridians: Cursive](https://cursive-ide.com/){target=_blank} is a commercial and closed source plugin for IntelliJ which provides a Clojure REPL client, evaluation and test running tools.

        Cursive uses the IntelliJ proprietary static analysis tools (rather than the Language Server Protocol standard).

        Follow the [:globe_with_meridians: Cursive user guide](https://cursive-ide.com/userguide/){target=_blank} to configure IntelliJ and install Cursive.

        !!! HINT "Requires license for commercial development"
            There is a free license when development is not for commercial projects, however, a Cursive license must be purchased for each developer working on a commercial project.

        [:globe_with_meridians: IntelliJ & Cursive install guide](https://cursive-ide.com/userguide/){target=_blank .md-button}

        ![Cursive IDE](https://cursive-ide.com/images/cursive-screenshot.png)
