# talend_combinations_generator
Project for Talend to generate arbitrary dictionary given desired chars and and combinations length.

**Mmmm... why???**
This combination generator just generates a zip with a .txt inside containing all the potential combinations, given a charset and the number of chars you want the combination length is. A sentence to better describe its functionality could be "Oh mighty, give me all the possibile 10 length combinations made only by letters a, b and c."


**How to:**
This tool, is Java based, platform indipendent and into `BUILD/generate_combinations/` folder you can find a .SH and a .BAT: suitable for launching it with linux/osx, Windows. You only have to download the `BUILD` folder and edit the properties file as follow:

_Properties file:_ `BUILD/generate_combinations/local_project/generate_combinations_0_1/contexts/Default.properties`

_Properties:_ 

`charset=abc`: these are the chars used to build combinations. 

`combination_length=10`: this is the length of each combination.

`output_path=/home/unknown/Desktop/`: this is the path where the .ZIP will be saved in. Notice the "/" at the end. ..And yes, forward slash even in Windows (Ex. D:/unknown/Desktop/).

In this case it will produce something like:
```
aabaaabaaa
babaaabaaa
cabaaabaaa
...
```

**Behavior:**
Actually, it also implements a basic filter to discard all the combinations that have a repeated char 4+ times. Finally, it produces a real-time-compressing .ZIP that, at the end of the process, contains a compressed .TXT with the list of every combination. With this tool, I reached the generation of 1M+ combination/sec on a i5 cpu and SSD.


**Importing in Talend:**
You can import this project into Talend, anyway you have to define a ImplicitContext file to valorize parameters from an external source. You can find a sample into the above cited file: `BUILD/generate_combinations/local_project/generate_combinations_0_1/contexts/Default.properties`

**License:**
Please folks, <a href="http://www.wtfpl.net/"><img
       src="http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-4.png"
       width="80" height="15" alt="WTFPL" /></a>
