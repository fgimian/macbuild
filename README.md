# Mac Build (using Ansible) #
*Automating OS X setup from the ground up*

![](images/osx-yosemite-logo.png)

The goal of this project is fully automate my OS X Yosemite workstation using
Ansible.  I Have currently implemented the following:

* **OS X Defaults**: Updating of defaults for various aspects of OS X such as
  enabling zoom, configuring Finder and so on.
* **Dot Files**: Configuration of .bash_profile, .gitconfig and other dot 
  files.
* **Terminal Package Installation**: This is being accomplish with the use of
  [homebrew](https://github.com/Homebrew/homebrew).
* **Desktop Application Installation**: This is being performed with the use
  of [homebrew-cask](https://github.com/caskroom/homebrew-cask).
* **Appstore Application Check**: Since there is currently no way to automate
  installation of App Store applications, I perform a check to see if the app
  is installed, and notify the user that they must install it from the App 
  Store if it isn't.
* **Python Base Setup**: Installation of essentials such as virtualenv are
  being performed using [pip](https://github.com/pypa/pip).
* **Application Settings**: Automating configuration of Sublime Text, MacDown,
  Textual and other applications which are of interest to me.
  
## Building your System ##

Run the following in your Terminal to use my configuration:

```bash
# Install Homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Install Ansible
brew install ansible

# Clone my macbuild repository
git clone https://github.com/fgimian/macbuild.git

# Perform the build
cd macbuild
ansible-playbook -K site.yml
```

## License ##

Mac Build is released under the **MIT** license. Please see the
[LICENSE](https://github.com/fgimian/macbuild/blob/master/LICENSE) file for
more details.  Feel froo take what you like and use it in your own Ansible
scripts.
