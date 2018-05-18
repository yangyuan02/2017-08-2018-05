Homebrew 基本使用

安装一个包
brew install <package_name> ||e.g: brew cask install visual-studio-code

卸载
brew uninstall <package_name>

搜索是否有包
brew cask search <package_name> 

查看你的包是否需要更新
brew outdated

更新包
brew upgrade <package_name> 

查看你安装过的包列表（包括版本号）
brew list --versions  


Homebrew装软件可以用命令打开

brew主要用来下载一些不带界面的命令行下的工具和第三方库来进行二次开发
brew cask主要用来下载一些带界面的应用软件，下载好后会自动安装，并能在mac中直接运行使用
1.brew cask install visual-studio-code
2.code .打开当前目录