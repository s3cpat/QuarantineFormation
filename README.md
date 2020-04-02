# QuarantineFormation
> CloudFormation + Quarantine = Templates for Things I Can Do With Friends Over the Internet

![This is Fine](https://www.dailydot.com/wp-content/uploads/2020/03/coronavirus-memes.jpg)

---

## Available Templates

### [Jeopardy](templates/jeopardy.yml)

The [Jeopardy](templates/jeopardy.yml) template spins up [theGrue](https://github.com/theGrue)/[jeopardy](https://github.com/theGrue/jeopardy) in an EC2 instance on port 80. 

![Jeopardy Stack Configuration](https://i.imgur.com/h21QGx5.png)

Enter an identifying Stack name, pick your preferred instance type (t2.micro by default as the instance does not require many resources), an SSH key for management, and CIDR ranges for connecting to the app. GameServerLocation specifies where users can reach port 80 (the game board). ManagementLocation specifies where all ports are accessible (mainly for SSH management). At minimum, you should set ManagementLocation to your/a trusted IP. 

Pairs well with [BuzzIn.live](https://buzzin.live/) as a way for users to buzz in with their smartphone/computer. 

### [Minecraft](templates/minecraft.yml)

The [Minecraft](templates/minecraft.yml) template spins up a Minecraft server using Spigot. 

![Minecraft Stack Configuration](https://i.imgur.com/Up4Avho.png)

Enter an identifying Stack name, pick your preferred instance type (t2.medium by default), an SSH key for management, and CIDR ranges for connecting to the server. GameServerLocation specifies where users can reach port 25565 (for connecting within the game). ManagementLocation specifies where all ports are accessible (mainly for SSH management). At minimum, you should set ManagementLocation to your/a trusted IP. 

Template only spins up the base Spigot-flavor Minecraft server. If you would like to add plugins or further configure the server (i.e. whitelist/blacklist IPs, set MOTD, etc), you must manage on your own.
