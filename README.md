# Install Rails on Mac

Hopefully you have a recent version of Mac OSX installed.

01. You can install Command Line Tools using this command. Choose to install and follow the prompts.

  In your terminal, type `xcode-select --install`

02. Check that Command Line Tools have installed

  In your terminal, type `gcc --version`

  You should see a similar output to this:
    ```
    Configured with: --prefix=/Applications/Xcode.app/Contents/Developer/usr --with-gxx-include-dir=/usr/include/c++/4.2.1
    Apple LLVM version 5.1 (clang-503.0.40) (based on LLVM 3.4svn)
    Target: x86_64-apple-darwin13.2.0
    Thread model: posix
    ```

04. Install HomeBrew
    ```
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

05. When that finishes, run `brew doctor`

06. Install RVM by copying this into your terminal:
    ```
    \curl -sSL https://get.rvm.io | bash -s stable
    ```

07. Copy the following into the terminal:
    ```
    source ~/.rvm/scripts/rvm
    ```

08. Install the latest Ruby by typing this in your terminal:
    ```
    rvm install 2.4.1
    ```

09. Install Rails

  In your terminal type:
    ```
    rvm use ruby-2.4.1@rails514 --create
    ```

10. Now install the latest Rails:
    ```
    gem install rails --no-ri --no-rdoc
    ```

  When it's finished, check the version with `rails -v`. It should be 5.1.4

11. Now set this as the default gemset:
    ```
    rvm use ruby-2.4.1@rails514 --default
    ```

You're done!
