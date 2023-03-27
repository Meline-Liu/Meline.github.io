
Created: [[ 2023-03-27]]
               12:41
Key: 
Note Cards: 
#👽 My Review: 
REF: Bluehost, Wordpress, Jekyll(wygg 推荐)-Github, Sublime Text(YW推荐，文档查看)

Idea:
1. chinese room paradox
2. explain the process of using chat gpt to install Jekyll (which I do not understand at all at first)
3. 


-------
##### 买域名+Hosting 
![[Screenshot 2023-03-27 at 12.40.44.png]]

- After login, contact coustomer service to purchase the "Real Domaine" with their free token---> wait 3h to contact them agin to asign the domaine (Melineliu.com) as the primary domaine 
	- You can put the website as "PARK" while waiting 

##### Wordpress
1. Get in the dashboard
2. Plugins 
	- delate unnecessary plugins
	- install new plugins
		- Starter Templates 
		- Elementor ![[Screenshot 2023-03-27 at 13.15.22.png]]
		- All in one WP Migration 

#### GPT-Github
 ![[Pasted image 20230327144808.png]]
 ![[Pasted image 20230327145405.png]]
 ![[Pasted image 20230327145415.png]]

### 配置Mac 运行Jekyll的环境
>[!info]
>1. --Install Xcode-Select
>2. /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
>3. brew install ruby
>4. sudo gem install bundler jekyll


 ##### Terminal
<mark class="hltr-red"> --Install Xcode-Select</mark> （管理装Homebrew软件）

Code:
- xcode-select --install
- /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

<mark class="hltr-orange">--Install Homebrew</mark> (装软件的软件)


#👽 reminds me of the [[Chinese Room Paradox]]

#### Trick
![[Screenshot 2023-03-27 at 15.06.43.png]]
- When the password key shows, make sure that you type the password , it won't show in the code area 


##### How do I know If I have instell Homebrew---> Ask Gpt again 
![[Pasted image 20230327151038.png]]


![[Screenshot 2023-03-27 at 15.14.34.png]]
ps: Homebrew 4.0.9 is the version 


install <mark class="hltr-pink">brew install ruby</mark>
(通过Homebrew装ruby)

<mark class="hltr-pink">sudo gem install bundler jekyll</mark>

![[Screenshot 2023-03-27 at 15.19.48.png]]

---
#gpt Why ?
s 2.6.3.62.

1 gem installed

meline@MELINEdeMacBook-Pro ~ % jekyll -v

zsh: command not found: jekyll

meline@MELINEdeMacBook-Pro ~ % jekyll -v

zsh: command not found: jekyll

meline@MELINEdeMacBook-Pro ~ %


The jekll not install correctly on the mac yet 

✔️ Correction ： 

GPT's Answer (put this in Terminal to run the error )
装合适的版本（对版本要求很高，fyi：gpt最开始给的版本是错的）
>[!info]
>gem install sass-embedded -v 1.58.3
>brew install rbenv
>rbenv install 3.1.2
>rbenv global 3.1.2

![[Pasted image 20230327152648.png]]
![[Pasted image 20230327152654.png]]



Fun time 
🍺--->homebrew lol
![[Screenshot 2023-03-27 at 15.30.23.png]]


##### sudo：最高权限，对一切可删、可写、可该


Once the installation is complete, add the Homebrew Ruby path to your shell configuration file (e.g., `.bash_profile`, `.bashrc`, or `.zshrc`, depending on your shell). Open the file with a text editor and add the following lines:

>bash -- 运行环境

----
### GPT - 4
(after gpt3.5 have let us down we decided to buy gpt 4--- and here is the answer )

⚡️⚡️⚡️⚡️⚡️
**Step 1: Install Command Line Tools**

First, you need to install Xcode Command Line Tools, which provide the necessary tools and libraries for building and installing software. Open the Terminal app and type the following command:

luaCopy code

`xcode-select --install`

Click "Install" when prompted to install the Command Line Tools.

**Step 2: Install Homebrew**

Homebrew is a package manager for macOS that helps you install and manage software. To install Homebrew, enter the following command in the Terminal:

bashCopy code

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`

Follow the prompts to complete the installation. Once installed, run this command to ensure Homebrew is properly set up:

Copy code

`brew doctor`

**Step 3: Install Ruby**

macOS comes with a system Ruby installation, but it's best to install a newer version for Jekyll. Use Homebrew to install the latest version of Ruby:

Copy code

`brew install ruby`

Once the installation is complete, add the Homebrew Ruby path to your shell configuration file (e.g., `.bash_profile`, `.bashrc`, or `.zshrc`, depending on your shell). Open the file with a text editor and add the following lines:

bashCopy code

`# Add Homebrew Ruby to PATH export PATH="/usr/local/opt/ruby/bin:$PATH"`

Save and close the file. Restart your terminal or run the following command to update your shell environment:

bashCopy code

`source ~/.bash_profile`

(Replace `.bash_profile
⚡️⚡️⚡️⚡️



⭐️ Important: 
>[!info]
>一直找不到jekll -v
>GPT 提示：
>更改正确路径，在找到路径以后把 ”xxx“变成程序里的东西 （在我的电脑里改成4.3.2
># Add Ruby gems bin to PATH
export PATH="/usr/local/lib/ruby/gems/x.x.x/bin:$PATH"



![[Screenshot 2023-03-27 at 16.27.15.png]]
⚡️

⚡️⚡️⚡️⚡️⚡️
It seems that the `jekyll` command is not in your system's PATH. This can happen if the gem executables directory is not added to your PATH environment variable. Let's fix this issue.

1.  First, find the path where the Jekyll executable is installed:

bashCopy code

`gem which jekyll`

The output should look something like this:

vbnetCopy code

`/usr/local/lib/ruby/gems/x.x.x/gems/jekyll-x.x.x/lib/jekyll.rb`

2.  We are interested in the `/usr/local/lib/ruby/gems/x.x.x/bin` part of the path. Replace `x.x.x` with the actual version numbers from the previous output. Now, add this path to your shell configuration file (e.g., `.bash_profile`, `.bashrc`, or `.zshrc`, depending on your shell). Open the file with a text editor and add the following lines:

bashCopy code

`# Add Ruby gems bin to PATH export PATH="/usr/local/lib/ruby/gems/x.x.x/bin:$PATH"`

Replace `x.x.x` with the actual version numbers from the previous output.

3.  Save and close the file. Restart your terminal or run the following command to update your shell environment:

bashCopy code

`source ~/.bash_profile`

(Replace `.bash_profile` with the appropriate file name for your shell, such as `.bashrc` or `.zshrc`, if necessary.)

4.  Now, try running the Jekyll command again:

Copy code

`jekyll -v`

If you've done everything correctly, you should see the Jekyll version number without any errors.

⚡️⚡️⚡️⚡️⚡️


> [!code] pwd:列出当前文件所在路径

![[Screenshot 2023-03-27 at 16.52.16.png]]




TERMINAL 
Auto-regeneration: enabled for '/Users/meline/my-site'

    Server address: http://127.0.0.1:4000/

  Server running... press ctrl-c to stop.

[2023-03-27 16:51:48] ERROR `/favicon.ico' not found.



>control+c 停止服务器
>bundle exec jekyll serve 开始服务器



exec: 可执行文件